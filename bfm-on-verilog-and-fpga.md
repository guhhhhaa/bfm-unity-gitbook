# 【硬件】BFM on Verilog & FPGA

{% hint style="info" %}
本章纯属 Ctrl + C&V，不爽可以 [**跳过**](https://guhhhhaa.gitbook.io/bfm/bfm-on-python)。
{% endhint %}

```c
`include "Const.vh"

module Bellman(input logic clk, bellman_reset,

input logic [`PRED_WIDTH:0] src,

/*Vertmat/Adjmat Read Inputs*/

input logic [`VERT_WIDTH:0] vertmat_q_a,

input logic [`VERT_WIDTH:0] vertmat_q_b,

input logic [`WEIGHT_WIDTH:0] adjmat_q,

/*VertMat Memory*/

output logic [`VERT_WIDTH:0] vertmat_data_a,

output logic [`VERT_WIDTH:0] vertmat_data_b,

output logic [`PRED_WIDTH:0] vertmat_addr_a,

output logic [`PRED_WIDTH:0] vertmat_addr_b,

output logic vertmat_we_a,

output logic vertmat_we_b, /*AdjMat Memory*/

output logic [`PRED_WIDTH:0] adjmat_row_addr,

output logic [`PRED_WIDTH:0] adjmat_col_addr,

output logic bellman_done);

enum logic [3:0] {SETUP, READ, IDLE, WRITE, DONE} state;

logic [`PRED_WIDTH:0] i, j, k; //Indices

logic signed [`WEIGHT_WIDTH:0] svw, dvw; //Source Vertex Weight, Destination Vertex Weight,

Signed

logic signed [`WEIGHT_WIDTH:0] e; //Edge Weight, Signed

assign adjmat_row_addr = i;

assign adjmat_col_addr = j;

assign e = adjmat_q;

assign svw = vertmat_q_a[`WEIGHT_WIDTH:0];

assign dvw = vertmat_q_b[`WEIGHT_WIDTH:0];

always_comb begin

vertmat_we_a = 0;

vertmat_addr_a = 0;

vertmat_addr_b = 0;

vertmat_data_a = 0;

vertmat_we_b = 0;

vertmat_data_b = 0;

case (state)

SETUP: begin

vertmat_we_a = 1;

vertmat_addr_a = k;

if (k + 1 == `NODES) ;

else if (k == src) begin

vertmat_data_a[`WEIGHT_WIDTH:0] = 0;

end else begin

vertmat_data_a[`WEIGHT_WIDTH:0] = 31'h777fffff; //INT MAX; THIS WILL CHANGE WITH WIDTH

end

end

READ: begin

vertmat_addr_a = i;

vertmat_addr_b = j;

end

IDLE: begin

vertmat_addr_a = i;

vertmat_addr_b = j;

end

WRITE:begin

vertmat_addr_a = i;

vertmat_addr_b = j;

if (e != 0 && $signed(svw + e) < $signed(dvw)) begin

vertmat_we_b = 1;

vertmat_data_b = {1'b0,i, $signed(svw + e)};

end

end

default: ;

endcase

end

always_ff @(posedge clk) begin

if (bellman_reset) begin i <= 0;

j <= 0;

k <= 0;

bellman_done <= 0;

state <= SETUP;

end else case (state)

SETUP: begin

if (k + 1 == `NODES) begin

k <= 0; //V Iterations below

state <= WRITE;

end else if (k == src) begin

k <= k + 1;

state <= SETUP;

end else begin

k <= k + 1;

state <= SETUP;

end

end

READ: begin

if (j + 1 == `NODES && i + 1 == `NODES && k + 1 == `NODES) begin //V Times

state <= DONE;

end else if (j + 1 == `NODES && i + 1 == `NODES) begin

i <= 0;

j <= 0;

k <= k + 1;

state <= IDLE;

end else if (j + 1 == `NODES) begin

i <= i + 1;

j <= 0;

state <= IDLE;

end else begin

j <= j + 1;

state <= IDLE;

end

end

IDLE: state <= WRITE;

WRITE: state <= READ;

DONE: bellman_done <= 1;

default: state <= DONE;

endcase

end

endmodule
```

## 硬件优化

### FPGA

{% embed url="https://github.com/G-ram/HFT/tree/master/FOREX" caption="" %}

[http://www.cs.columbia.edu/~sedwards/classes/2016/4840-spring/designs/FOREX.pdf](http://www.cs.columbia.edu/~sedwards/classes/2016/4840-spring/designs/FOREX.pdf)

{% embed url="http://www.cs.columbia.edu/~sedwards/classes/2016/4840-spring/designs/FOREX.pdf" caption="" %}

[http://www.cs.columbia.edu/~sedwards/classes/2016/4840-spring/reports/FOREX.pdf](http://www.cs.columbia.edu/~sedwards/classes/2016/4840-spring/reports/FOREX.pdf)

{% embed url="http://www.cs.columbia.edu/~sedwards/classes/2016/4840-spring/reports/FOREX.pdf" caption="" %}


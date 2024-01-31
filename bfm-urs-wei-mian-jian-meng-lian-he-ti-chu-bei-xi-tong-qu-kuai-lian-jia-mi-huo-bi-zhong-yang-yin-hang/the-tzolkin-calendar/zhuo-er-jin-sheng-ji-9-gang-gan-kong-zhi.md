# 卓尔金升级9——杠杆控制

![](../../.gitbook/assets/杠杆率控制.png)

## **w\_aS**

**w\_aS = MAX(-x/a , 0)**

## **w\_1L ，w\_aL**

**w\_1L = MAX(MIN(x , -(x-a)/(a-1)) , 0)**\
**w\_aL = MAX(MIN((x-1)/(a-1) , x/a) , 0)**

## **w\_1S ，w\_2S**

**w\_1S = MAX(MIN(x+2 , -x) , 0)**\
**w\_2S = MAX(MIN(-x-1 , -x/2) , 0)**

## **w\_1L ，w\_2L ，w\_3L**

**w\_1L = MAX(MIN(x , 2-x) , 0)**\
**w\_2L = MAX(MIN(x-1 , 3-x) , 0)**\
**w\_3L = MAX(MIN(x-2 , x/3) , 0)**

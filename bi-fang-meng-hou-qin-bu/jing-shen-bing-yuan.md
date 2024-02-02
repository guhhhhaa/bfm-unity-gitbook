# 精神病院

如果你很不幸，住院了，住院以后，你要知道，精神病医院的潜规则：

我用（A，B，C，D）表示

A：认知对象类型，1=自己，2=别人，3=所有人

B：有没有病，0=没病，1=有病

C：分不分析病情原因，0=不分析，1=分析

D：需不需要治疗，0=不需要治疗，1=需要治疗

其中X表示：0或1

觉得自己没病，拒绝吃药（1，0，X，0）：医院里闹事的病人

觉得自己没病，但是喜欢吃药，喜欢住院（1，0，X，1）：药物成瘾的病人，或者来医院避难的病人。

承认自己有病（1，1，X，1）：可以出院并继续吃药的普通病人

承认自己有病，但是停药了（1，1，X，0）：可以出院后各种原因停药的普通病人

试图证明别人没病（2，0，X，X ）：人缘不错的精神病人。

试图证明别人有病，不分析，也不管治不治（2，1，0，0）：往医院一扔，然后不管的家属

试图证明别人有病，分析了（2，1，1， 0）：陪护家属或心理咨询师

试图证明别人有病，不分析，直接开药（2，1，0，1）：医院里混日子的普通医生

试图证明别人有病，让你填量表或者做心理咨询，分析后开药（2，1，1，1）：医院里的主任医生

认为所有人都没病，但是叮嘱大家按时吃药（3，0，X，1）：医院里地位最高的病人，零号病人，病人王

认为所有人都没病，但是拒绝吃药（3，0，X，0）：医院里地位最低的病人，被绑的病人

试图证明，所有人都有病，有病是正常现象，且不需要治疗（3，1，1，0）：精神分析师

认为，所有人都有病，且都需要治疗（3，1，0，1）：不怪好意的垃圾人，但是是正常人

认为，所有人都有病，且不分析，并且认为不需要治疗（3，1，0，0）：普通正常人

认为，所有人都有病，分析了，认为都需要治疗（3，1，1，1）：哲学家
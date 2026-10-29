# Y86_Instructions

| Name | Bytes |
| --- | --- | 
|`halt` | 0 0 |
|`nop` | 1 0 |
|`rrmovq rA,rB` | 2 0 rA rB |
|`irmovq V,rB`| 3 0  F rB  V_8  | 
|`rmmovq rA,D(rB)`| 4 0 rA rB D_8 |
|`mrmovq D(rB),rA`| 5 0 rA rB D_8 |
|`OPq rA,rB`| 6 fn rA rB |
|`jXX Dest`| 7 fn Dest_8 |
|`cmovXX rA,rB`| 2 fn rA rB |
|`call Dest`| 8 0 Dest_8 |
|`ret`| 9 0 |
|`pushq rA`| A 0 rA F |
|`popq rA`| B 0 rA F |

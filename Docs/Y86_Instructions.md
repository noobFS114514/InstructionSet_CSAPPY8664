# Y86_Instructions

## 基础指令 *Basic Instructions*

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

## fn具体细节 *Detailed numbers in fn*

|`OPq`| fn | 
| --- | --- |
|`addq`| 6 0 |
|`subq`| 6 1 |
|`andq`| 6 2 |
|`xorq`| 6 3 |

|`jXX`| fn |
| --- | --- |
| `jmp` | 7 0 |
|`jle`| 7 1 |
|`jl`| 7 2 |
|`je`| 7 3 |
|`jne`| 7 4 |
|`jge`| 7 5 |
|`jg`| 7 6 |

|`cmovXX`| fn |
| --- | --- |
|`cmovle`| 2 1 |
|`cmovl`| 2 2 |
|`cmove`| 2 3 |
|`cmovne`| 2 4 |
|`cmovge`| 2 5 |
|`cmovg`| 2 6 |

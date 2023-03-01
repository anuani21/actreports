
# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature.
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update signature
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x800000f8', '0x800004b0')]      |
| SIG_REGION                | [('0x80002210', '0x80002320', '68 words')]      |
| COV_LABELS                | fcvt.h.s_b22      |
| TEST_NAME                 | /home/anusha/new/RV32H/fcvt.h.s/work/fcvt.h.s_b22-01.S/ref.S    |
| Total Number of coverpoints| 75     |
| Total Coverpoints Hit     | 75      |
| Total Signature Updates   | 33      |
| STAT1                     | 33      |
| STAT2                     | 0      |
| STAT3                     | 0     |
| STAT4                     | 0     |
| STAT5                     | 0     |

## Details for STAT2:

```


```

## Details of STAT3

```


```

## Details of STAT4:

```

```

## Details of STAT5:



## Details of STAT1:

- The first column indicates the signature address and the data at that location in hexadecimal in the following format: 
  ```
  [Address]
  Data
  ```

- The second column captures all the coverpoints which have been captured by that particular signature location

- The third column captures all the insrtuctions since the time a coverpoint was
  hit to the point when a store to the signature was performed. Each line has
  the following format:
  ```
  [PC of instruction] : mnemonic
  ```
- The order in the table is based on the order of signatures occuring in the
  test. These need not necessarily be in increasing or decreasing order of the
  address in the signature region.

|s.no|        signature         |                                                                             coverpoints                                                                              |                                                                       code                                                                       |
|---:|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
|   1|[0x80002218]<br>0x00000001|- mnemonic : fcvt.h.s<br> - rs1 : f30<br> - rd : f31<br> - rs1 != rd<br> - fs1 == 0 and fe1 == 0x7c and fm1 == 0x4923b8 and  fcsr == 0x0 and rm_val == 7   #nosat<br> |[0x80000120]:fcvt.h.s ft11, ft10, dyn<br> [0x80000124]:csrrs tp, fcsr, zero<br> [0x80000128]:fsw ft11, 0(ra)<br> [0x8000012c]:sw tp, 4(ra)<br>    |
|   2|[0x80002220]<br>0x00000001|- rs1 : f29<br> - rd : f29<br> - rs1 == rd<br> - fs1 == 0 and fe1 == 0x7d and fm1 == 0x36e5d6 and  fcsr == 0x0 and rm_val == 7   #nosat<br>                           |[0x8000013c]:fcvt.h.s ft9, ft9, dyn<br> [0x80000140]:csrrs tp, fcsr, zero<br> [0x80000144]:fsw ft9, 8(ra)<br> [0x80000148]:sw tp, 12(ra)<br>      |
|   3|[0x80002228]<br>0x00000001|- rs1 : f31<br> - rd : f30<br> - fs1 == 0 and fe1 == 0x7e and fm1 == 0x49fee5 and  fcsr == 0x0 and rm_val == 7   #nosat<br>                                           |[0x80000158]:fcvt.h.s ft10, ft11, dyn<br> [0x8000015c]:csrrs tp, fcsr, zero<br> [0x80000160]:fsw ft10, 16(ra)<br> [0x80000164]:sw tp, 20(ra)<br>  |
|   4|[0x80002230]<br>0x00000001|- rs1 : f27<br> - rd : f28<br> - fs1 == 0 and fe1 == 0x7f and fm1 == 0x1a616d and  fcsr == 0x0 and rm_val == 7   #nosat<br>                                           |[0x80000174]:fcvt.h.s ft8, fs11, dyn<br> [0x80000178]:csrrs tp, fcsr, zero<br> [0x8000017c]:fsw ft8, 24(ra)<br> [0x80000180]:sw tp, 28(ra)<br>    |
|   5|[0x80002238]<br>0x00000001|- rs1 : f28<br> - rd : f27<br> - fs1 == 0 and fe1 == 0x80 and fm1 == 0x681ae9 and  fcsr == 0x0 and rm_val == 7   #nosat<br>                                           |[0x80000190]:fcvt.h.s fs11, ft8, dyn<br> [0x80000194]:csrrs tp, fcsr, zero<br> [0x80000198]:fsw fs11, 32(ra)<br> [0x8000019c]:sw tp, 36(ra)<br>   |
|   6|[0x80002240]<br>0x00000001|- rs1 : f25<br> - rd : f26<br> - fs1 == 0 and fe1 == 0x81 and fm1 == 0x696b5c and  fcsr == 0x0 and rm_val == 7   #nosat<br>                                           |[0x800001ac]:fcvt.h.s fs10, fs9, dyn<br> [0x800001b0]:csrrs tp, fcsr, zero<br> [0x800001b4]:fsw fs10, 40(ra)<br> [0x800001b8]:sw tp, 44(ra)<br>   |
|   7|[0x80002248]<br>0x00000003|- rs1 : f26<br> - rd : f25<br> - fs1 == 0 and fe1 == 0x67 and fm1 == 0x53a4fc and  fcsr == 0x0 and rm_val == 7   #nosat<br>                                           |[0x800001c8]:fcvt.h.s fs9, fs10, dyn<br> [0x800001cc]:csrrs tp, fcsr, zero<br> [0x800001d0]:fsw fs9, 48(ra)<br> [0x800001d4]:sw tp, 52(ra)<br>    |
|   8|[0x80002250]<br>0x00000005|- rs1 : f23<br> - rd : f24<br> - fs1 == 0 and fe1 == 0xc4 and fm1 == 0x046756 and  fcsr == 0x0 and rm_val == 7   #nosat<br>                                           |[0x800001e4]:fcvt.h.s fs8, fs7, dyn<br> [0x800001e8]:csrrs tp, fcsr, zero<br> [0x800001ec]:fsw fs8, 56(ra)<br> [0x800001f0]:sw tp, 60(ra)<br>     |
|   9|[0x80002258]<br>0x00000000|- rs1 : f24<br> - rd : f23<br>                                                                                                                                        |[0x80000200]:fcvt.h.s fs7, fs8, dyn<br> [0x80000204]:csrrs tp, fcsr, zero<br> [0x80000208]:fsw fs7, 64(ra)<br> [0x8000020c]:sw tp, 68(ra)<br>     |
|  10|[0x80002260]<br>0x00000000|- rs1 : f21<br> - rd : f22<br>                                                                                                                                        |[0x8000021c]:fcvt.h.s fs6, fs5, dyn<br> [0x80000220]:csrrs tp, fcsr, zero<br> [0x80000224]:fsw fs6, 72(ra)<br> [0x80000228]:sw tp, 76(ra)<br>     |
|  11|[0x80002268]<br>0x00000000|- rs1 : f22<br> - rd : f21<br>                                                                                                                                        |[0x80000238]:fcvt.h.s fs5, fs6, dyn<br> [0x8000023c]:csrrs tp, fcsr, zero<br> [0x80000240]:fsw fs5, 80(ra)<br> [0x80000244]:sw tp, 84(ra)<br>     |
|  12|[0x80002270]<br>0x00000000|- rs1 : f19<br> - rd : f20<br>                                                                                                                                        |[0x80000254]:fcvt.h.s fs4, fs3, dyn<br> [0x80000258]:csrrs tp, fcsr, zero<br> [0x8000025c]:fsw fs4, 88(ra)<br> [0x80000260]:sw tp, 92(ra)<br>     |
|  13|[0x80002278]<br>0x00000000|- rs1 : f20<br> - rd : f19<br>                                                                                                                                        |[0x80000270]:fcvt.h.s fs3, fs4, dyn<br> [0x80000274]:csrrs tp, fcsr, zero<br> [0x80000278]:fsw fs3, 96(ra)<br> [0x8000027c]:sw tp, 100(ra)<br>    |
|  14|[0x80002280]<br>0x00000000|- rs1 : f17<br> - rd : f18<br>                                                                                                                                        |[0x8000028c]:fcvt.h.s fs2, fa7, dyn<br> [0x80000290]:csrrs tp, fcsr, zero<br> [0x80000294]:fsw fs2, 104(ra)<br> [0x80000298]:sw tp, 108(ra)<br>   |
|  15|[0x80002288]<br>0x00000000|- rs1 : f18<br> - rd : f17<br>                                                                                                                                        |[0x800002a8]:fcvt.h.s fa7, fs2, dyn<br> [0x800002ac]:csrrs tp, fcsr, zero<br> [0x800002b0]:fsw fa7, 112(ra)<br> [0x800002b4]:sw tp, 116(ra)<br>   |
|  16|[0x80002290]<br>0x00000000|- rs1 : f15<br> - rd : f16<br>                                                                                                                                        |[0x800002c4]:fcvt.h.s fa6, fa5, dyn<br> [0x800002c8]:csrrs tp, fcsr, zero<br> [0x800002cc]:fsw fa6, 120(ra)<br> [0x800002d0]:sw tp, 124(ra)<br>   |
|  17|[0x80002298]<br>0x00000000|- rs1 : f16<br> - rd : f15<br>                                                                                                                                        |[0x800002e0]:fcvt.h.s fa5, fa6, dyn<br> [0x800002e4]:csrrs tp, fcsr, zero<br> [0x800002e8]:fsw fa5, 128(ra)<br> [0x800002ec]:sw tp, 132(ra)<br>   |
|  18|[0x800022a0]<br>0x00000000|- rs1 : f13<br> - rd : f14<br>                                                                                                                                        |[0x800002fc]:fcvt.h.s fa4, fa3, dyn<br> [0x80000300]:csrrs tp, fcsr, zero<br> [0x80000304]:fsw fa4, 136(ra)<br> [0x80000308]:sw tp, 140(ra)<br>   |
|  19|[0x800022a8]<br>0x00000000|- rs1 : f14<br> - rd : f13<br>                                                                                                                                        |[0x80000318]:fcvt.h.s fa3, fa4, dyn<br> [0x8000031c]:csrrs tp, fcsr, zero<br> [0x80000320]:fsw fa3, 144(ra)<br> [0x80000324]:sw tp, 148(ra)<br>   |
|  20|[0x800022b0]<br>0x00000000|- rs1 : f11<br> - rd : f12<br>                                                                                                                                        |[0x80000334]:fcvt.h.s fa2, fa1, dyn<br> [0x80000338]:csrrs tp, fcsr, zero<br> [0x8000033c]:fsw fa2, 152(ra)<br> [0x80000340]:sw tp, 156(ra)<br>   |
|  21|[0x800022b8]<br>0x00000000|- rs1 : f12<br> - rd : f11<br>                                                                                                                                        |[0x80000350]:fcvt.h.s fa1, fa2, dyn<br> [0x80000354]:csrrs tp, fcsr, zero<br> [0x80000358]:fsw fa1, 160(ra)<br> [0x8000035c]:sw tp, 164(ra)<br>   |
|  22|[0x800022c0]<br>0x00000000|- rs1 : f9<br> - rd : f10<br>                                                                                                                                         |[0x8000036c]:fcvt.h.s fa0, fs1, dyn<br> [0x80000370]:csrrs tp, fcsr, zero<br> [0x80000374]:fsw fa0, 168(ra)<br> [0x80000378]:sw tp, 172(ra)<br>   |
|  23|[0x800022c8]<br>0x00000000|- rs1 : f10<br> - rd : f9<br>                                                                                                                                         |[0x80000388]:fcvt.h.s fs1, fa0, dyn<br> [0x8000038c]:csrrs tp, fcsr, zero<br> [0x80000390]:fsw fs1, 176(ra)<br> [0x80000394]:sw tp, 180(ra)<br>   |
|  24|[0x800022d0]<br>0x00000000|- rs1 : f7<br> - rd : f8<br>                                                                                                                                          |[0x800003a4]:fcvt.h.s fs0, ft7, dyn<br> [0x800003a8]:csrrs tp, fcsr, zero<br> [0x800003ac]:fsw fs0, 184(ra)<br> [0x800003b0]:sw tp, 188(ra)<br>   |
|  25|[0x800022d8]<br>0x00000000|- rs1 : f8<br> - rd : f7<br>                                                                                                                                          |[0x800003c0]:fcvt.h.s ft7, fs0, dyn<br> [0x800003c4]:csrrs tp, fcsr, zero<br> [0x800003c8]:fsw ft7, 192(ra)<br> [0x800003cc]:sw tp, 196(ra)<br>   |
|  26|[0x800022e0]<br>0x00000000|- rs1 : f5<br> - rd : f6<br>                                                                                                                                          |[0x800003dc]:fcvt.h.s ft6, ft5, dyn<br> [0x800003e0]:csrrs tp, fcsr, zero<br> [0x800003e4]:fsw ft6, 200(ra)<br> [0x800003e8]:sw tp, 204(ra)<br>   |
|  27|[0x800022e8]<br>0x00000000|- rs1 : f6<br> - rd : f5<br>                                                                                                                                          |[0x800003f8]:fcvt.h.s ft5, ft6, dyn<br> [0x800003fc]:csrrs tp, fcsr, zero<br> [0x80000400]:fsw ft5, 208(ra)<br> [0x80000404]:sw tp, 212(ra)<br>   |
|  28|[0x800022f0]<br>0x00000000|- rs1 : f3<br> - rd : f4<br>                                                                                                                                          |[0x80000414]:fcvt.h.s ft4, ft3, dyn<br> [0x80000418]:csrrs tp, fcsr, zero<br> [0x8000041c]:fsw ft4, 216(ra)<br> [0x80000420]:sw tp, 220(ra)<br>   |
|  29|[0x800022f8]<br>0x00000000|- rs1 : f4<br> - rd : f3<br>                                                                                                                                          |[0x80000430]:fcvt.h.s ft3, ft4, dyn<br> [0x80000434]:csrrs tp, fcsr, zero<br> [0x80000438]:fsw ft3, 224(ra)<br> [0x8000043c]:sw tp, 228(ra)<br>   |
|  30|[0x80002300]<br>0x00000000|- rs1 : f1<br> - rd : f2<br>                                                                                                                                          |[0x8000044c]:fcvt.h.s ft2, ft1, dyn<br> [0x80000450]:csrrs tp, fcsr, zero<br> [0x80000454]:fsw ft2, 232(ra)<br> [0x80000458]:sw tp, 236(ra)<br>   |
|  31|[0x80002308]<br>0x00000000|- rs1 : f2<br> - rd : f1<br>                                                                                                                                          |[0x80000468]:fcvt.h.s ft1, ft2, dyn<br> [0x8000046c]:csrrs tp, fcsr, zero<br> [0x80000470]:fsw ft1, 240(ra)<br> [0x80000474]:sw tp, 244(ra)<br>   |
|  32|[0x80002310]<br>0x00000000|- rs1 : f0<br>                                                                                                                                                        |[0x80000484]:fcvt.h.s ft11, ft0, dyn<br> [0x80000488]:csrrs tp, fcsr, zero<br> [0x8000048c]:fsw ft11, 248(ra)<br> [0x80000490]:sw tp, 252(ra)<br> |
|  33|[0x80002318]<br>0x00000000|- rd : f0<br>                                                                                                                                                         |[0x800004a0]:fcvt.h.s ft0, ft11, dyn<br> [0x800004a4]:csrrs tp, fcsr, zero<br> [0x800004a8]:fsw ft0, 256(ra)<br> [0x800004ac]:sw tp, 260(ra)<br>  |

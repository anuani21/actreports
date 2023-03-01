
# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature.
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update signature
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x800000f8', '0x80000580')]      |
| SIG_REGION                | [('0x80002310', '0x80002430', '72 words')]      |
| COV_LABELS                | fsub_b10      |
| TEST_NAME                 | /home/anusha/new/RV32H/fsub/work/fsub_b10-01.S/ref.S    |
| Total Number of coverpoints| 106     |
| Total Coverpoints Hit     | 106      |
| Total Signature Updates   | 35      |
| STAT1                     | 35      |
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

|s.no|        signature         |                                                                                                                                                      coverpoints                                                                                                                                                      |                                                                         code                                                                         |
|---:|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|   1|[0x80002318]<br>0x00000000|- mnemonic : fsub.h<br> - rs1 : f30<br> - rs2 : f29<br> - rd : f31<br> - rs1 != rs2  and rs1 != rd and rs2 != rd<br> - fs1 == 0 and fe1 == 0x12 and fm1 == 0x0d5 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br> |[0x80000124]:fsub.h ft11, ft10, ft9, dyn<br> [0x80000128]:csrrs tp, fcsr, zero<br> [0x8000012c]:fsw ft11, 0(ra)<br> [0x80000130]:sw tp, 4(ra)<br>     |
|   2|[0x80002320]<br>0x00000000|- rs1 : f28<br> - rs2 : f28<br> - rd : f28<br> - rs1 == rs2 == rd<br>                                                                                                                                                                                                                                                  |[0x80000144]:fsub.h ft8, ft8, ft8, dyn<br> [0x80000148]:csrrs tp, fcsr, zero<br> [0x8000014c]:fsw ft8, 8(ra)<br> [0x80000150]:sw tp, 12(ra)<br>       |
|   3|[0x80002328]<br>0x00000000|- rs1 : f31<br> - rs2 : f30<br> - rd : f30<br> - rs2 == rd != rs1<br> - fs1 == 0 and fe1 == 0x12 and fm1 == 0x0d5 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x190 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                |[0x80000164]:fsub.h ft10, ft11, ft10, dyn<br> [0x80000168]:csrrs tp, fcsr, zero<br> [0x8000016c]:fsw ft10, 16(ra)<br> [0x80000170]:sw tp, 20(ra)<br>  |
|   4|[0x80002330]<br>0x00000000|- rs1 : f29<br> - rs2 : f31<br> - rd : f29<br> - rs1 == rd != rs2<br> - fs1 == 0 and fe1 == 0x12 and fm1 == 0x0d5 and fs2 == 0 and fe2 == 0x14 and fm2 == 0x2f5 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                |[0x80000184]:fsub.h ft9, ft9, ft11, dyn<br> [0x80000188]:csrrs tp, fcsr, zero<br> [0x8000018c]:fsw ft9, 24(ra)<br> [0x80000190]:sw tp, 28(ra)<br>     |
|   5|[0x80002338]<br>0x00000000|- rs1 : f26<br> - rs2 : f26<br> - rd : f27<br> - rs1 == rs2 != rd<br>                                                                                                                                                                                                                                                  |[0x800001a4]:fsub.h fs11, fs10, fs10, dyn<br> [0x800001a8]:csrrs tp, fcsr, zero<br> [0x800001ac]:fsw fs11, 32(ra)<br> [0x800001b0]:sw tp, 36(ra)<br>  |
|   6|[0x80002340]<br>0x00000000|- rs1 : f27<br> - rs2 : f25<br> - rd : f26<br>                                                                                                                                                                                                                                                                         |[0x800001c4]:fsub.h fs10, fs11, fs9, dyn<br> [0x800001c8]:csrrs tp, fcsr, zero<br> [0x800001cc]:fsw fs10, 40(ra)<br> [0x800001d0]:sw tp, 44(ra)<br>   |
|   7|[0x80002348]<br>0x00000000|- rs1 : f24<br> - rs2 : f27<br> - rd : f25<br>                                                                                                                                                                                                                                                                         |[0x800001e4]:fsub.h fs9, fs8, fs11, dyn<br> [0x800001e8]:csrrs tp, fcsr, zero<br> [0x800001ec]:fsw fs9, 48(ra)<br> [0x800001f0]:sw tp, 52(ra)<br>     |
|   8|[0x80002350]<br>0x00000000|- rs1 : f25<br> - rs2 : f23<br> - rd : f24<br>                                                                                                                                                                                                                                                                         |[0x80000204]:fsub.h fs8, fs9, fs7, dyn<br> [0x80000208]:csrrs tp, fcsr, zero<br> [0x8000020c]:fsw fs8, 56(ra)<br> [0x80000210]:sw tp, 60(ra)<br>      |
|   9|[0x80002358]<br>0x00000000|- rs1 : f22<br> - rs2 : f24<br> - rd : f23<br>                                                                                                                                                                                                                                                                         |[0x80000224]:fsub.h fs7, fs6, fs8, dyn<br> [0x80000228]:csrrs tp, fcsr, zero<br> [0x8000022c]:fsw fs7, 64(ra)<br> [0x80000230]:sw tp, 68(ra)<br>      |
|  10|[0x80002360]<br>0x00000000|- rs1 : f23<br> - rs2 : f21<br> - rd : f22<br>                                                                                                                                                                                                                                                                         |[0x80000244]:fsub.h fs6, fs7, fs5, dyn<br> [0x80000248]:csrrs tp, fcsr, zero<br> [0x8000024c]:fsw fs6, 72(ra)<br> [0x80000250]:sw tp, 76(ra)<br>      |
|  11|[0x80002368]<br>0x00000000|- rs1 : f20<br> - rs2 : f22<br> - rd : f21<br>                                                                                                                                                                                                                                                                         |[0x80000264]:fsub.h fs5, fs4, fs6, dyn<br> [0x80000268]:csrrs tp, fcsr, zero<br> [0x8000026c]:fsw fs5, 80(ra)<br> [0x80000270]:sw tp, 84(ra)<br>      |
|  12|[0x80002370]<br>0x00000000|- rs1 : f21<br> - rs2 : f19<br> - rd : f20<br>                                                                                                                                                                                                                                                                         |[0x80000284]:fsub.h fs4, fs5, fs3, dyn<br> [0x80000288]:csrrs tp, fcsr, zero<br> [0x8000028c]:fsw fs4, 88(ra)<br> [0x80000290]:sw tp, 92(ra)<br>      |
|  13|[0x80002378]<br>0x00000000|- rs1 : f18<br> - rs2 : f20<br> - rd : f19<br>                                                                                                                                                                                                                                                                         |[0x800002a4]:fsub.h fs3, fs2, fs4, dyn<br> [0x800002a8]:csrrs tp, fcsr, zero<br> [0x800002ac]:fsw fs3, 96(ra)<br> [0x800002b0]:sw tp, 100(ra)<br>     |
|  14|[0x80002380]<br>0x00000000|- rs1 : f19<br> - rs2 : f17<br> - rd : f18<br>                                                                                                                                                                                                                                                                         |[0x800002c4]:fsub.h fs2, fs3, fa7, dyn<br> [0x800002c8]:csrrs tp, fcsr, zero<br> [0x800002cc]:fsw fs2, 104(ra)<br> [0x800002d0]:sw tp, 108(ra)<br>    |
|  15|[0x80002388]<br>0x00000000|- rs1 : f16<br> - rs2 : f18<br> - rd : f17<br>                                                                                                                                                                                                                                                                         |[0x800002e4]:fsub.h fa7, fa6, fs2, dyn<br> [0x800002e8]:csrrs tp, fcsr, zero<br> [0x800002ec]:fsw fa7, 112(ra)<br> [0x800002f0]:sw tp, 116(ra)<br>    |
|  16|[0x80002390]<br>0x00000000|- rs1 : f17<br> - rs2 : f15<br> - rd : f16<br>                                                                                                                                                                                                                                                                         |[0x80000304]:fsub.h fa6, fa7, fa5, dyn<br> [0x80000308]:csrrs tp, fcsr, zero<br> [0x8000030c]:fsw fa6, 120(ra)<br> [0x80000310]:sw tp, 124(ra)<br>    |
|  17|[0x80002398]<br>0x00000000|- rs1 : f14<br> - rs2 : f16<br> - rd : f15<br>                                                                                                                                                                                                                                                                         |[0x80000324]:fsub.h fa5, fa4, fa6, dyn<br> [0x80000328]:csrrs tp, fcsr, zero<br> [0x8000032c]:fsw fa5, 128(ra)<br> [0x80000330]:sw tp, 132(ra)<br>    |
|  18|[0x800023a0]<br>0x00000000|- rs1 : f15<br> - rs2 : f13<br> - rd : f14<br>                                                                                                                                                                                                                                                                         |[0x80000344]:fsub.h fa4, fa5, fa3, dyn<br> [0x80000348]:csrrs tp, fcsr, zero<br> [0x8000034c]:fsw fa4, 136(ra)<br> [0x80000350]:sw tp, 140(ra)<br>    |
|  19|[0x800023a8]<br>0x00000000|- rs1 : f12<br> - rs2 : f14<br> - rd : f13<br>                                                                                                                                                                                                                                                                         |[0x80000364]:fsub.h fa3, fa2, fa4, dyn<br> [0x80000368]:csrrs tp, fcsr, zero<br> [0x8000036c]:fsw fa3, 144(ra)<br> [0x80000370]:sw tp, 148(ra)<br>    |
|  20|[0x800023b0]<br>0x00000000|- rs1 : f13<br> - rs2 : f11<br> - rd : f12<br>                                                                                                                                                                                                                                                                         |[0x80000384]:fsub.h fa2, fa3, fa1, dyn<br> [0x80000388]:csrrs tp, fcsr, zero<br> [0x8000038c]:fsw fa2, 152(ra)<br> [0x80000390]:sw tp, 156(ra)<br>    |
|  21|[0x800023b8]<br>0x00000000|- rs1 : f10<br> - rs2 : f12<br> - rd : f11<br>                                                                                                                                                                                                                                                                         |[0x800003a4]:fsub.h fa1, fa0, fa2, dyn<br> [0x800003a8]:csrrs tp, fcsr, zero<br> [0x800003ac]:fsw fa1, 160(ra)<br> [0x800003b0]:sw tp, 164(ra)<br>    |
|  22|[0x800023c0]<br>0x00000000|- rs1 : f11<br> - rs2 : f9<br> - rd : f10<br>                                                                                                                                                                                                                                                                          |[0x800003c4]:fsub.h fa0, fa1, fs1, dyn<br> [0x800003c8]:csrrs tp, fcsr, zero<br> [0x800003cc]:fsw fa0, 168(ra)<br> [0x800003d0]:sw tp, 172(ra)<br>    |
|  23|[0x800023c8]<br>0x00000000|- rs1 : f8<br> - rs2 : f10<br> - rd : f9<br>                                                                                                                                                                                                                                                                           |[0x800003e4]:fsub.h fs1, fs0, fa0, dyn<br> [0x800003e8]:csrrs tp, fcsr, zero<br> [0x800003ec]:fsw fs1, 176(ra)<br> [0x800003f0]:sw tp, 180(ra)<br>    |
|  24|[0x800023d0]<br>0x00000000|- rs1 : f9<br> - rs2 : f7<br> - rd : f8<br>                                                                                                                                                                                                                                                                            |[0x80000404]:fsub.h fs0, fs1, ft7, dyn<br> [0x80000408]:csrrs tp, fcsr, zero<br> [0x8000040c]:fsw fs0, 184(ra)<br> [0x80000410]:sw tp, 188(ra)<br>    |
|  25|[0x800023d8]<br>0x00000000|- rs1 : f6<br> - rs2 : f8<br> - rd : f7<br>                                                                                                                                                                                                                                                                            |[0x80000424]:fsub.h ft7, ft6, fs0, dyn<br> [0x80000428]:csrrs tp, fcsr, zero<br> [0x8000042c]:fsw ft7, 192(ra)<br> [0x80000430]:sw tp, 196(ra)<br>    |
|  26|[0x800023e0]<br>0x00000000|- rs1 : f7<br> - rs2 : f5<br> - rd : f6<br>                                                                                                                                                                                                                                                                            |[0x80000444]:fsub.h ft6, ft7, ft5, dyn<br> [0x80000448]:csrrs tp, fcsr, zero<br> [0x8000044c]:fsw ft6, 200(ra)<br> [0x80000450]:sw tp, 204(ra)<br>    |
|  27|[0x800023e8]<br>0x00000000|- rs1 : f4<br> - rs2 : f6<br> - rd : f5<br>                                                                                                                                                                                                                                                                            |[0x80000464]:fsub.h ft5, ft4, ft6, dyn<br> [0x80000468]:csrrs tp, fcsr, zero<br> [0x8000046c]:fsw ft5, 208(ra)<br> [0x80000470]:sw tp, 212(ra)<br>    |
|  28|[0x800023f0]<br>0x00000000|- rs1 : f5<br> - rs2 : f3<br> - rd : f4<br>                                                                                                                                                                                                                                                                            |[0x80000484]:fsub.h ft4, ft5, ft3, dyn<br> [0x80000488]:csrrs tp, fcsr, zero<br> [0x8000048c]:fsw ft4, 216(ra)<br> [0x80000490]:sw tp, 220(ra)<br>    |
|  29|[0x800023f8]<br>0x00000000|- rs1 : f2<br> - rs2 : f4<br> - rd : f3<br>                                                                                                                                                                                                                                                                            |[0x800004a4]:fsub.h ft3, ft2, ft4, dyn<br> [0x800004a8]:csrrs tp, fcsr, zero<br> [0x800004ac]:fsw ft3, 224(ra)<br> [0x800004b0]:sw tp, 228(ra)<br>    |
|  30|[0x80002400]<br>0x00000000|- rs1 : f3<br> - rs2 : f1<br> - rd : f2<br>                                                                                                                                                                                                                                                                            |[0x800004c4]:fsub.h ft2, ft3, ft1, dyn<br> [0x800004c8]:csrrs tp, fcsr, zero<br> [0x800004cc]:fsw ft2, 232(ra)<br> [0x800004d0]:sw tp, 236(ra)<br>    |
|  31|[0x80002408]<br>0x00000000|- rs1 : f0<br> - rs2 : f2<br> - rd : f1<br>                                                                                                                                                                                                                                                                            |[0x800004e4]:fsub.h ft1, ft0, ft2, dyn<br> [0x800004e8]:csrrs tp, fcsr, zero<br> [0x800004ec]:fsw ft1, 240(ra)<br> [0x800004f0]:sw tp, 244(ra)<br>    |
|  32|[0x80002410]<br>0x00000000|- rs1 : f1<br>                                                                                                                                                                                                                                                                                                         |[0x80000504]:fsub.h ft11, ft1, ft10, dyn<br> [0x80000508]:csrrs tp, fcsr, zero<br> [0x8000050c]:fsw ft11, 248(ra)<br> [0x80000510]:sw tp, 252(ra)<br> |
|  33|[0x80002418]<br>0x00000000|- rs2 : f0<br>                                                                                                                                                                                                                                                                                                         |[0x80000524]:fsub.h ft11, ft10, ft0, dyn<br> [0x80000528]:csrrs tp, fcsr, zero<br> [0x8000052c]:fsw ft11, 256(ra)<br> [0x80000530]:sw tp, 260(ra)<br> |
|  34|[0x80002420]<br>0x00000000|- rd : f0<br>                                                                                                                                                                                                                                                                                                          |[0x80000544]:fsub.h ft0, ft11, ft10, dyn<br> [0x80000548]:csrrs tp, fcsr, zero<br> [0x8000054c]:fsw ft0, 264(ra)<br> [0x80000550]:sw tp, 268(ra)<br>  |
|  35|[0x80002428]<br>0x00000000|- fs1 == 0 and fe1 == 0x12 and fm1 == 0x0d5 and fs2 == 0 and fe2 == 0x0e and fm2 == 0x073 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                                                      |[0x80000564]:fsub.h ft11, ft10, ft9, dyn<br> [0x80000568]:csrrs tp, fcsr, zero<br> [0x8000056c]:fsw ft11, 272(ra)<br> [0x80000570]:sw tp, 276(ra)<br> |

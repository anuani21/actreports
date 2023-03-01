
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
| COV_LABELS                | fcvt.h.w_b25      |
| TEST_NAME                 | /home/anusha/new/RV32H/fcvt.h.w/work/fcvt.h.w_b25-01.S/ref.S    |
| Total Number of coverpoints| 72     |
| Total Coverpoints Hit     | 72      |
| Total Signature Updates   | 32      |
| STAT1                     | 32      |
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

|s.no|        signature         |                                                    coverpoints                                                    |                                                                      code                                                                      |
|---:|--------------------------|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
|   1|[0x80002218]<br>0x00000000|- mnemonic : fcvt.h.w<br> - rs1 : x31<br> - rd : f31<br> - rs1_val == 0 and  fcsr == 0 and rm_val == 7  #nosat<br> |[0x80000120]:fcvt.h.w ft11, t6, dyn<br> [0x80000124]:csrrs tp, fcsr, zero<br> [0x80000128]:fsw ft11, 0(ra)<br> [0x8000012c]:sw tp, 4(ra)<br>    |
|   2|[0x80002220]<br>0x00000000|- rs1 : x30<br> - rd : f30<br> - rs1_val == 1 and  fcsr == 0 and rm_val == 7  #nosat<br>                           |[0x8000013c]:fcvt.h.w ft10, t5, dyn<br> [0x80000140]:csrrs tp, fcsr, zero<br> [0x80000144]:fsw ft10, 8(ra)<br> [0x80000148]:sw tp, 12(ra)<br>   |
|   3|[0x80002228]<br>0x00000000|- rs1 : x29<br> - rd : f29<br> - rs1_val == -1 and  fcsr == 0 and rm_val == 7  #nosat<br>                          |[0x80000158]:fcvt.h.w ft9, t4, dyn<br> [0x8000015c]:csrrs tp, fcsr, zero<br> [0x80000160]:fsw ft9, 16(ra)<br> [0x80000164]:sw tp, 20(ra)<br>    |
|   4|[0x80002230]<br>0x00000005|- rs1 : x28<br> - rd : f28<br> - rs1_val == 2147483647 and  fcsr == 0 and rm_val == 7  #nosat<br>                  |[0x80000174]:fcvt.h.w ft8, t3, dyn<br> [0x80000178]:csrrs tp, fcsr, zero<br> [0x8000017c]:fsw ft8, 24(ra)<br> [0x80000180]:sw tp, 28(ra)<br>    |
|   5|[0x80002238]<br>0x00000005|- rs1 : x27<br> - rd : f27<br> - rs1_val == -2147483647 and  fcsr == 0 and rm_val == 7  #nosat<br>                 |[0x80000190]:fcvt.h.w fs11, s11, dyn<br> [0x80000194]:csrrs tp, fcsr, zero<br> [0x80000198]:fsw fs11, 32(ra)<br> [0x8000019c]:sw tp, 36(ra)<br> |
|   6|[0x80002240]<br>0x00000005|- rs1 : x26<br> - rd : f26<br> - rs1_val == 1227077728 and  fcsr == 0 and rm_val == 7  #nosat<br>                  |[0x800001ac]:fcvt.h.w fs10, s10, dyn<br> [0x800001b0]:csrrs tp, fcsr, zero<br> [0x800001b4]:fsw fs10, 40(ra)<br> [0x800001b8]:sw tp, 44(ra)<br> |
|   7|[0x80002248]<br>0x00000005|- rs1 : x25<br> - rd : f25<br> - rs1_val == -1227077728 and  fcsr == 0 and rm_val == 7  #nosat<br>                 |[0x800001c8]:fcvt.h.w fs9, s9, dyn<br> [0x800001cc]:csrrs tp, fcsr, zero<br> [0x800001d0]:fsw fs9, 48(ra)<br> [0x800001d4]:sw tp, 52(ra)<br>    |
|   8|[0x80002250]<br>0x00000000|- rs1 : x24<br> - rd : f24<br>                                                                                     |[0x800001e4]:fcvt.h.w fs8, s8, dyn<br> [0x800001e8]:csrrs tp, fcsr, zero<br> [0x800001ec]:fsw fs8, 56(ra)<br> [0x800001f0]:sw tp, 60(ra)<br>    |
|   9|[0x80002258]<br>0x00000000|- rs1 : x23<br> - rd : f23<br>                                                                                     |[0x80000200]:fcvt.h.w fs7, s7, dyn<br> [0x80000204]:csrrs tp, fcsr, zero<br> [0x80000208]:fsw fs7, 64(ra)<br> [0x8000020c]:sw tp, 68(ra)<br>    |
|  10|[0x80002260]<br>0x00000000|- rs1 : x22<br> - rd : f22<br>                                                                                     |[0x8000021c]:fcvt.h.w fs6, s6, dyn<br> [0x80000220]:csrrs tp, fcsr, zero<br> [0x80000224]:fsw fs6, 72(ra)<br> [0x80000228]:sw tp, 76(ra)<br>    |
|  11|[0x80002268]<br>0x00000000|- rs1 : x21<br> - rd : f21<br>                                                                                     |[0x80000238]:fcvt.h.w fs5, s5, dyn<br> [0x8000023c]:csrrs tp, fcsr, zero<br> [0x80000240]:fsw fs5, 80(ra)<br> [0x80000244]:sw tp, 84(ra)<br>    |
|  12|[0x80002270]<br>0x00000000|- rs1 : x20<br> - rd : f20<br>                                                                                     |[0x80000254]:fcvt.h.w fs4, s4, dyn<br> [0x80000258]:csrrs tp, fcsr, zero<br> [0x8000025c]:fsw fs4, 88(ra)<br> [0x80000260]:sw tp, 92(ra)<br>    |
|  13|[0x80002278]<br>0x00000000|- rs1 : x19<br> - rd : f19<br>                                                                                     |[0x80000270]:fcvt.h.w fs3, s3, dyn<br> [0x80000274]:csrrs tp, fcsr, zero<br> [0x80000278]:fsw fs3, 96(ra)<br> [0x8000027c]:sw tp, 100(ra)<br>   |
|  14|[0x80002280]<br>0x00000000|- rs1 : x18<br> - rd : f18<br>                                                                                     |[0x8000028c]:fcvt.h.w fs2, s2, dyn<br> [0x80000290]:csrrs tp, fcsr, zero<br> [0x80000294]:fsw fs2, 104(ra)<br> [0x80000298]:sw tp, 108(ra)<br>  |
|  15|[0x80002288]<br>0x00000000|- rs1 : x17<br> - rd : f17<br>                                                                                     |[0x800002a8]:fcvt.h.w fa7, a7, dyn<br> [0x800002ac]:csrrs tp, fcsr, zero<br> [0x800002b0]:fsw fa7, 112(ra)<br> [0x800002b4]:sw tp, 116(ra)<br>  |
|  16|[0x80002290]<br>0x00000000|- rs1 : x16<br> - rd : f16<br>                                                                                     |[0x800002c4]:fcvt.h.w fa6, a6, dyn<br> [0x800002c8]:csrrs tp, fcsr, zero<br> [0x800002cc]:fsw fa6, 120(ra)<br> [0x800002d0]:sw tp, 124(ra)<br>  |
|  17|[0x80002298]<br>0x00000000|- rs1 : x15<br> - rd : f15<br>                                                                                     |[0x800002e0]:fcvt.h.w fa5, a5, dyn<br> [0x800002e4]:csrrs tp, fcsr, zero<br> [0x800002e8]:fsw fa5, 128(ra)<br> [0x800002ec]:sw tp, 132(ra)<br>  |
|  18|[0x800022a0]<br>0x00000000|- rs1 : x14<br> - rd : f14<br>                                                                                     |[0x800002fc]:fcvt.h.w fa4, a4, dyn<br> [0x80000300]:csrrs tp, fcsr, zero<br> [0x80000304]:fsw fa4, 136(ra)<br> [0x80000308]:sw tp, 140(ra)<br>  |
|  19|[0x800022a8]<br>0x00000000|- rs1 : x13<br> - rd : f13<br>                                                                                     |[0x80000318]:fcvt.h.w fa3, a3, dyn<br> [0x8000031c]:csrrs tp, fcsr, zero<br> [0x80000320]:fsw fa3, 144(ra)<br> [0x80000324]:sw tp, 148(ra)<br>  |
|  20|[0x800022b0]<br>0x00000000|- rs1 : x12<br> - rd : f12<br>                                                                                     |[0x80000334]:fcvt.h.w fa2, a2, dyn<br> [0x80000338]:csrrs tp, fcsr, zero<br> [0x8000033c]:fsw fa2, 152(ra)<br> [0x80000340]:sw tp, 156(ra)<br>  |
|  21|[0x800022b8]<br>0x00000000|- rs1 : x11<br> - rd : f11<br>                                                                                     |[0x80000350]:fcvt.h.w fa1, a1, dyn<br> [0x80000354]:csrrs tp, fcsr, zero<br> [0x80000358]:fsw fa1, 160(ra)<br> [0x8000035c]:sw tp, 164(ra)<br>  |
|  22|[0x800022c0]<br>0x00000000|- rs1 : x10<br> - rd : f10<br>                                                                                     |[0x8000036c]:fcvt.h.w fa0, a0, dyn<br> [0x80000370]:csrrs tp, fcsr, zero<br> [0x80000374]:fsw fa0, 168(ra)<br> [0x80000378]:sw tp, 172(ra)<br>  |
|  23|[0x800022c8]<br>0x00000000|- rs1 : x9<br> - rd : f9<br>                                                                                       |[0x80000388]:fcvt.h.w fs1, s1, dyn<br> [0x8000038c]:csrrs tp, fcsr, zero<br> [0x80000390]:fsw fs1, 176(ra)<br> [0x80000394]:sw tp, 180(ra)<br>  |
|  24|[0x800022d0]<br>0x00000000|- rs1 : x8<br> - rd : f8<br>                                                                                       |[0x800003a4]:fcvt.h.w fs0, fp, dyn<br> [0x800003a8]:csrrs tp, fcsr, zero<br> [0x800003ac]:fsw fs0, 184(ra)<br> [0x800003b0]:sw tp, 188(ra)<br>  |
|  25|[0x800022d8]<br>0x00000000|- rs1 : x7<br> - rd : f7<br>                                                                                       |[0x800003c8]:fcvt.h.w ft7, t2, dyn<br> [0x800003cc]:csrrs s1, fcsr, zero<br> [0x800003d0]:fsw ft7, 192(ra)<br> [0x800003d4]:sw s1, 196(ra)<br>  |
|  26|[0x800022e0]<br>0x00000000|- rs1 : x6<br> - rd : f6<br>                                                                                       |[0x800003e4]:fcvt.h.w ft6, t1, dyn<br> [0x800003e8]:csrrs s1, fcsr, zero<br> [0x800003ec]:fsw ft6, 200(ra)<br> [0x800003f0]:sw s1, 204(ra)<br>  |
|  27|[0x800022e8]<br>0x00000000|- rs1 : x5<br> - rd : f5<br>                                                                                       |[0x80000400]:fcvt.h.w ft5, t0, dyn<br> [0x80000404]:csrrs s1, fcsr, zero<br> [0x80000408]:fsw ft5, 208(ra)<br> [0x8000040c]:sw s1, 212(ra)<br>  |
|  28|[0x800022f0]<br>0x00000000|- rs1 : x4<br> - rd : f4<br>                                                                                       |[0x80000424]:fcvt.h.w ft4, tp, dyn<br> [0x80000428]:csrrs s1, fcsr, zero<br> [0x8000042c]:fsw ft4, 0(t0)<br> [0x80000430]:sw s1, 4(t0)<br>      |
|  29|[0x800022f8]<br>0x00000000|- rs1 : x3<br> - rd : f3<br>                                                                                       |[0x80000440]:fcvt.h.w ft3, gp, dyn<br> [0x80000444]:csrrs s1, fcsr, zero<br> [0x80000448]:fsw ft3, 8(t0)<br> [0x8000044c]:sw s1, 12(t0)<br>     |
|  30|[0x80002300]<br>0x00000000|- rs1 : x2<br> - rd : f2<br>                                                                                       |[0x8000045c]:fcvt.h.w ft2, sp, dyn<br> [0x80000460]:csrrs s1, fcsr, zero<br> [0x80000464]:fsw ft2, 16(t0)<br> [0x80000468]:sw s1, 20(t0)<br>    |
|  31|[0x80002308]<br>0x00000000|- rs1 : x1<br> - rd : f1<br>                                                                                       |[0x80000478]:fcvt.h.w ft1, ra, dyn<br> [0x8000047c]:csrrs s1, fcsr, zero<br> [0x80000480]:fsw ft1, 24(t0)<br> [0x80000484]:sw s1, 28(t0)<br>    |
|  32|[0x80002310]<br>0x00000000|- rs1 : x0<br> - rd : f0<br>                                                                                       |[0x80000494]:fcvt.h.w ft0, zero, dyn<br> [0x80000498]:csrrs s1, fcsr, zero<br> [0x8000049c]:fsw ft0, 32(t0)<br> [0x800004a0]:sw s1, 36(t0)<br>  |


# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature.
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update signature
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x800000f8', '0x80000630')]      |
| SIG_REGION                | [('0x80002210', '0x80002320', '68 words')]      |
| COV_LABELS                | flh-align      |
| TEST_NAME                 | /home/anusha/new/RV32H/flh/work/flh-align-01.S/ref.S    |
| Total Number of coverpoints| 71     |
| Total Coverpoints Hit     | 71      |
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

|s.no|        signature         |                                                   coverpoints                                                   |                                                                                                        code                                                                                                        |
|---:|--------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   1|[0x80002218]<br>0x0000009F|- mnemonic : flh<br> - rs1 : x31<br> - rd : f31<br> - ea_align == 0 and (imm_val % 4) == 0<br> - imm_val < 0<br> |[0x80000124]:flh ft11, 4092(t6)<br> [0x80000128]:addi zero, zero, 0<br> [0x8000012c]:addi zero, zero, 0<br> [0x80000130]:csrrs tp, fcsr, zero<br> [0x80000134]:fsw ft11, 0(ra)<br> [0x80000138]:sw tp, 4(ra)<br>    |
|   2|[0x80002220]<br>0x0000009F|- rs1 : x30<br> - rd : f30<br> - ea_align == 0 and (imm_val % 4) == 1<br>                                        |[0x8000014c]:flh ft10, 4093(t5)<br> [0x80000150]:addi zero, zero, 0<br> [0x80000154]:addi zero, zero, 0<br> [0x80000158]:csrrs tp, fcsr, zero<br> [0x8000015c]:fsw ft10, 8(ra)<br> [0x80000160]:sw tp, 12(ra)<br>   |
|   3|[0x80002228]<br>0x0000009F|- rs1 : x29<br> - rd : f29<br> - ea_align == 0 and (imm_val % 4) == 2<br>                                        |[0x80000174]:flh ft9, 4090(t4)<br> [0x80000178]:addi zero, zero, 0<br> [0x8000017c]:addi zero, zero, 0<br> [0x80000180]:csrrs tp, fcsr, zero<br> [0x80000184]:fsw ft9, 16(ra)<br> [0x80000188]:sw tp, 20(ra)<br>    |
|   4|[0x80002230]<br>0x0000009F|- rs1 : x28<br> - rd : f28<br> - ea_align == 0 and (imm_val % 4) == 3<br> - imm_val > 0<br>                      |[0x8000019c]:flh ft8, 2047(t3)<br> [0x800001a0]:addi zero, zero, 0<br> [0x800001a4]:addi zero, zero, 0<br> [0x800001a8]:csrrs tp, fcsr, zero<br> [0x800001ac]:fsw ft8, 24(ra)<br> [0x800001b0]:sw tp, 28(ra)<br>    |
|   5|[0x80002238]<br>0x0000009F|- rs1 : x27<br> - rd : f27<br> - imm_val == 0<br>                                                                |[0x800001c4]:flh fs11, 0(s11)<br> [0x800001c8]:addi zero, zero, 0<br> [0x800001cc]:addi zero, zero, 0<br> [0x800001d0]:csrrs tp, fcsr, zero<br> [0x800001d4]:fsw fs11, 32(ra)<br> [0x800001d8]:sw tp, 36(ra)<br>    |
|   6|[0x80002240]<br>0x00000000|- rs1 : x26<br> - rd : f26<br>                                                                                   |[0x800001ec]:flh fs10, 2048(s10)<br> [0x800001f0]:addi zero, zero, 0<br> [0x800001f4]:addi zero, zero, 0<br> [0x800001f8]:csrrs tp, fcsr, zero<br> [0x800001fc]:fsw fs10, 40(ra)<br> [0x80000200]:sw tp, 44(ra)<br> |
|   7|[0x80002248]<br>0x00000000|- rs1 : x25<br> - rd : f25<br>                                                                                   |[0x80000214]:flh fs9, 2048(s9)<br> [0x80000218]:addi zero, zero, 0<br> [0x8000021c]:addi zero, zero, 0<br> [0x80000220]:csrrs tp, fcsr, zero<br> [0x80000224]:fsw fs9, 48(ra)<br> [0x80000228]:sw tp, 52(ra)<br>    |
|   8|[0x80002250]<br>0x00000000|- rs1 : x24<br> - rd : f24<br>                                                                                   |[0x8000023c]:flh fs8, 2048(s8)<br> [0x80000240]:addi zero, zero, 0<br> [0x80000244]:addi zero, zero, 0<br> [0x80000248]:csrrs tp, fcsr, zero<br> [0x8000024c]:fsw fs8, 56(ra)<br> [0x80000250]:sw tp, 60(ra)<br>    |
|   9|[0x80002258]<br>0x00000000|- rs1 : x23<br> - rd : f23<br>                                                                                   |[0x80000264]:flh fs7, 2048(s7)<br> [0x80000268]:addi zero, zero, 0<br> [0x8000026c]:addi zero, zero, 0<br> [0x80000270]:csrrs tp, fcsr, zero<br> [0x80000274]:fsw fs7, 64(ra)<br> [0x80000278]:sw tp, 68(ra)<br>    |
|  10|[0x80002260]<br>0x00000000|- rs1 : x22<br> - rd : f22<br>                                                                                   |[0x8000028c]:flh fs6, 2048(s6)<br> [0x80000290]:addi zero, zero, 0<br> [0x80000294]:addi zero, zero, 0<br> [0x80000298]:csrrs tp, fcsr, zero<br> [0x8000029c]:fsw fs6, 72(ra)<br> [0x800002a0]:sw tp, 76(ra)<br>    |
|  11|[0x80002268]<br>0x00000000|- rs1 : x21<br> - rd : f21<br>                                                                                   |[0x800002b4]:flh fs5, 2048(s5)<br> [0x800002b8]:addi zero, zero, 0<br> [0x800002bc]:addi zero, zero, 0<br> [0x800002c0]:csrrs tp, fcsr, zero<br> [0x800002c4]:fsw fs5, 80(ra)<br> [0x800002c8]:sw tp, 84(ra)<br>    |
|  12|[0x80002270]<br>0x00000000|- rs1 : x20<br> - rd : f20<br>                                                                                   |[0x800002dc]:flh fs4, 2048(s4)<br> [0x800002e0]:addi zero, zero, 0<br> [0x800002e4]:addi zero, zero, 0<br> [0x800002e8]:csrrs tp, fcsr, zero<br> [0x800002ec]:fsw fs4, 88(ra)<br> [0x800002f0]:sw tp, 92(ra)<br>    |
|  13|[0x80002278]<br>0x00000000|- rs1 : x19<br> - rd : f19<br>                                                                                   |[0x80000304]:flh fs3, 2048(s3)<br> [0x80000308]:addi zero, zero, 0<br> [0x8000030c]:addi zero, zero, 0<br> [0x80000310]:csrrs tp, fcsr, zero<br> [0x80000314]:fsw fs3, 96(ra)<br> [0x80000318]:sw tp, 100(ra)<br>   |
|  14|[0x80002280]<br>0x00000000|- rs1 : x18<br> - rd : f18<br>                                                                                   |[0x8000032c]:flh fs2, 2048(s2)<br> [0x80000330]:addi zero, zero, 0<br> [0x80000334]:addi zero, zero, 0<br> [0x80000338]:csrrs tp, fcsr, zero<br> [0x8000033c]:fsw fs2, 104(ra)<br> [0x80000340]:sw tp, 108(ra)<br>  |
|  15|[0x80002288]<br>0x00000000|- rs1 : x17<br> - rd : f17<br>                                                                                   |[0x80000354]:flh fa7, 2048(a7)<br> [0x80000358]:addi zero, zero, 0<br> [0x8000035c]:addi zero, zero, 0<br> [0x80000360]:csrrs tp, fcsr, zero<br> [0x80000364]:fsw fa7, 112(ra)<br> [0x80000368]:sw tp, 116(ra)<br>  |
|  16|[0x80002290]<br>0x00000000|- rs1 : x16<br> - rd : f16<br>                                                                                   |[0x8000037c]:flh fa6, 2048(a6)<br> [0x80000380]:addi zero, zero, 0<br> [0x80000384]:addi zero, zero, 0<br> [0x80000388]:csrrs tp, fcsr, zero<br> [0x8000038c]:fsw fa6, 120(ra)<br> [0x80000390]:sw tp, 124(ra)<br>  |
|  17|[0x80002298]<br>0x00000000|- rs1 : x15<br> - rd : f15<br>                                                                                   |[0x800003a4]:flh fa5, 2048(a5)<br> [0x800003a8]:addi zero, zero, 0<br> [0x800003ac]:addi zero, zero, 0<br> [0x800003b0]:csrrs tp, fcsr, zero<br> [0x800003b4]:fsw fa5, 128(ra)<br> [0x800003b8]:sw tp, 132(ra)<br>  |
|  18|[0x800022a0]<br>0x00000000|- rs1 : x14<br> - rd : f14<br>                                                                                   |[0x800003cc]:flh fa4, 2048(a4)<br> [0x800003d0]:addi zero, zero, 0<br> [0x800003d4]:addi zero, zero, 0<br> [0x800003d8]:csrrs tp, fcsr, zero<br> [0x800003dc]:fsw fa4, 136(ra)<br> [0x800003e0]:sw tp, 140(ra)<br>  |
|  19|[0x800022a8]<br>0x00000000|- rs1 : x13<br> - rd : f13<br>                                                                                   |[0x800003f4]:flh fa3, 2048(a3)<br> [0x800003f8]:addi zero, zero, 0<br> [0x800003fc]:addi zero, zero, 0<br> [0x80000400]:csrrs tp, fcsr, zero<br> [0x80000404]:fsw fa3, 144(ra)<br> [0x80000408]:sw tp, 148(ra)<br>  |
|  20|[0x800022b0]<br>0x00000000|- rs1 : x12<br> - rd : f12<br>                                                                                   |[0x8000041c]:flh fa2, 2048(a2)<br> [0x80000420]:addi zero, zero, 0<br> [0x80000424]:addi zero, zero, 0<br> [0x80000428]:csrrs tp, fcsr, zero<br> [0x8000042c]:fsw fa2, 152(ra)<br> [0x80000430]:sw tp, 156(ra)<br>  |
|  21|[0x800022b8]<br>0x00000000|- rs1 : x11<br> - rd : f11<br>                                                                                   |[0x80000444]:flh fa1, 2048(a1)<br> [0x80000448]:addi zero, zero, 0<br> [0x8000044c]:addi zero, zero, 0<br> [0x80000450]:csrrs tp, fcsr, zero<br> [0x80000454]:fsw fa1, 160(ra)<br> [0x80000458]:sw tp, 164(ra)<br>  |
|  22|[0x800022c0]<br>0x00000000|- rs1 : x10<br> - rd : f10<br>                                                                                   |[0x8000046c]:flh fa0, 2048(a0)<br> [0x80000470]:addi zero, zero, 0<br> [0x80000474]:addi zero, zero, 0<br> [0x80000478]:csrrs tp, fcsr, zero<br> [0x8000047c]:fsw fa0, 168(ra)<br> [0x80000480]:sw tp, 172(ra)<br>  |
|  23|[0x800022c8]<br>0x00000000|- rs1 : x9<br> - rd : f9<br>                                                                                     |[0x80000494]:flh fs1, 2048(s1)<br> [0x80000498]:addi zero, zero, 0<br> [0x8000049c]:addi zero, zero, 0<br> [0x800004a0]:csrrs tp, fcsr, zero<br> [0x800004a4]:fsw fs1, 176(ra)<br> [0x800004a8]:sw tp, 180(ra)<br>  |
|  24|[0x800022d0]<br>0x00000000|- rs1 : x8<br> - rd : f8<br>                                                                                     |[0x800004bc]:flh fs0, 2048(fp)<br> [0x800004c0]:addi zero, zero, 0<br> [0x800004c4]:addi zero, zero, 0<br> [0x800004c8]:csrrs tp, fcsr, zero<br> [0x800004cc]:fsw fs0, 184(ra)<br> [0x800004d0]:sw tp, 188(ra)<br>  |
|  25|[0x800022d8]<br>0x00000000|- rs1 : x7<br> - rd : f7<br>                                                                                     |[0x800004ec]:flh ft7, 2048(t2)<br> [0x800004f0]:addi zero, zero, 0<br> [0x800004f4]:addi zero, zero, 0<br> [0x800004f8]:csrrs s1, fcsr, zero<br> [0x800004fc]:fsw ft7, 192(ra)<br> [0x80000500]:sw s1, 196(ra)<br>  |
|  26|[0x800022e0]<br>0x00000000|- rs1 : x6<br> - rd : f6<br>                                                                                     |[0x80000514]:flh ft6, 2048(t1)<br> [0x80000518]:addi zero, zero, 0<br> [0x8000051c]:addi zero, zero, 0<br> [0x80000520]:csrrs s1, fcsr, zero<br> [0x80000524]:fsw ft6, 200(ra)<br> [0x80000528]:sw s1, 204(ra)<br>  |
|  27|[0x800022e8]<br>0x00000000|- rs1 : x5<br> - rd : f5<br>                                                                                     |[0x8000053c]:flh ft5, 2048(t0)<br> [0x80000540]:addi zero, zero, 0<br> [0x80000544]:addi zero, zero, 0<br> [0x80000548]:csrrs s1, fcsr, zero<br> [0x8000054c]:fsw ft5, 208(ra)<br> [0x80000550]:sw s1, 212(ra)<br>  |
|  28|[0x800022f0]<br>0x00000000|- rs1 : x4<br> - rd : f4<br>                                                                                     |[0x8000056c]:flh ft4, 2048(tp)<br> [0x80000570]:addi zero, zero, 0<br> [0x80000574]:addi zero, zero, 0<br> [0x80000578]:csrrs s1, fcsr, zero<br> [0x8000057c]:fsw ft4, 0(t0)<br> [0x80000580]:sw s1, 4(t0)<br>      |
|  29|[0x800022f8]<br>0x00000000|- rs1 : x3<br> - rd : f3<br>                                                                                     |[0x80000594]:flh ft3, 2048(gp)<br> [0x80000598]:addi zero, zero, 0<br> [0x8000059c]:addi zero, zero, 0<br> [0x800005a0]:csrrs s1, fcsr, zero<br> [0x800005a4]:fsw ft3, 8(t0)<br> [0x800005a8]:sw s1, 12(t0)<br>     |
|  30|[0x80002300]<br>0x00000000|- rs1 : x2<br> - rd : f2<br>                                                                                     |[0x800005bc]:flh ft2, 2048(sp)<br> [0x800005c0]:addi zero, zero, 0<br> [0x800005c4]:addi zero, zero, 0<br> [0x800005c8]:csrrs s1, fcsr, zero<br> [0x800005cc]:fsw ft2, 16(t0)<br> [0x800005d0]:sw s1, 20(t0)<br>    |
|  31|[0x80002308]<br>0x00000000|- rs1 : x1<br> - rd : f1<br>                                                                                     |[0x800005e4]:flh ft1, 2048(ra)<br> [0x800005e8]:addi zero, zero, 0<br> [0x800005ec]:addi zero, zero, 0<br> [0x800005f0]:csrrs s1, fcsr, zero<br> [0x800005f4]:fsw ft1, 24(t0)<br> [0x800005f8]:sw s1, 28(t0)<br>    |
|  32|[0x80002310]<br>0x00000000|- rd : f0<br>                                                                                                    |[0x8000060c]:flh ft0, 2048(t6)<br> [0x80000610]:addi zero, zero, 0<br> [0x80000614]:addi zero, zero, 0<br> [0x80000618]:csrrs s1, fcsr, zero<br> [0x8000061c]:fsw ft0, 32(t0)<br> [0x80000620]:sw s1, 36(t0)<br>    |

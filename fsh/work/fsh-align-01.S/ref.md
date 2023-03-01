
# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature.
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update signature
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x800000f8', '0x800005b0')]      |
| SIG_REGION                | [('0x80002310', '0x80002420', '68 words')]      |
| COV_LABELS                | fsh-align      |
| TEST_NAME                 | /home/anusha/new/RV32H/fsh/work/fsh-align-01.S/ref.S    |
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

|s.no|        signature         |                                                   coverpoints                                                    |                                                                                       code                                                                                       |
|---:|--------------------------|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   1|[0x80002318]<br>0x00000000|- mnemonic : fsh<br> - rs1 : x31<br> - rs2 : f31<br> - ea_align == 0 and (imm_val % 4) == 0<br> - imm_val < 0<br> |[0x80000124]:fsh ft11, 4092(t6)<br> [0x80000128]:addi zero, zero, 0<br> [0x8000012c]:addi zero, zero, 0<br> [0x80000130]:csrrs tp, fcsr, zero<br> [0x80000134]:sw tp, 4(ra)<br>   |
|   2|[0x80002320]<br>0x00000000|- rs1 : x30<br> - rs2 : f30<br> - ea_align == 0 and (imm_val % 4) == 1<br>                                        |[0x80000148]:fsh ft10, 4093(t5)<br> [0x8000014c]:addi zero, zero, 0<br> [0x80000150]:addi zero, zero, 0<br> [0x80000154]:csrrs tp, fcsr, zero<br> [0x80000158]:sw tp, 12(ra)<br>  |
|   3|[0x80002328]<br>0x00000000|- rs1 : x29<br> - rs2 : f29<br> - ea_align == 0 and (imm_val % 4) == 2<br>                                        |[0x8000016c]:fsh ft9, 4090(t4)<br> [0x80000170]:addi zero, zero, 0<br> [0x80000174]:addi zero, zero, 0<br> [0x80000178]:csrrs tp, fcsr, zero<br> [0x8000017c]:sw tp, 20(ra)<br>   |
|   4|[0x80002330]<br>0x00000000|- rs1 : x28<br> - rs2 : f28<br> - ea_align == 0 and (imm_val % 4) == 3<br> - imm_val > 0<br>                      |[0x80000190]:fsh ft8, 2047(t3)<br> [0x80000194]:addi zero, zero, 0<br> [0x80000198]:addi zero, zero, 0<br> [0x8000019c]:csrrs tp, fcsr, zero<br> [0x800001a0]:sw tp, 28(ra)<br>   |
|   5|[0x80002338]<br>0x00000000|- rs1 : x27<br> - rs2 : f27<br> - imm_val == 0<br>                                                                |[0x800001b4]:fsh fs11, 0(s11)<br> [0x800001b8]:addi zero, zero, 0<br> [0x800001bc]:addi zero, zero, 0<br> [0x800001c0]:csrrs tp, fcsr, zero<br> [0x800001c4]:sw tp, 36(ra)<br>    |
|   6|[0x80002340]<br>0x00000000|- rs1 : x26<br> - rs2 : f26<br>                                                                                   |[0x800001d8]:fsh fs10, 2048(s10)<br> [0x800001dc]:addi zero, zero, 0<br> [0x800001e0]:addi zero, zero, 0<br> [0x800001e4]:csrrs tp, fcsr, zero<br> [0x800001e8]:sw tp, 44(ra)<br> |
|   7|[0x80002348]<br>0x00000000|- rs1 : x25<br> - rs2 : f25<br>                                                                                   |[0x800001fc]:fsh fs9, 2048(s9)<br> [0x80000200]:addi zero, zero, 0<br> [0x80000204]:addi zero, zero, 0<br> [0x80000208]:csrrs tp, fcsr, zero<br> [0x8000020c]:sw tp, 52(ra)<br>   |
|   8|[0x80002350]<br>0x00000000|- rs1 : x24<br> - rs2 : f24<br>                                                                                   |[0x80000220]:fsh fs8, 2048(s8)<br> [0x80000224]:addi zero, zero, 0<br> [0x80000228]:addi zero, zero, 0<br> [0x8000022c]:csrrs tp, fcsr, zero<br> [0x80000230]:sw tp, 60(ra)<br>   |
|   9|[0x80002358]<br>0x00000000|- rs1 : x23<br> - rs2 : f23<br>                                                                                   |[0x80000244]:fsh fs7, 2048(s7)<br> [0x80000248]:addi zero, zero, 0<br> [0x8000024c]:addi zero, zero, 0<br> [0x80000250]:csrrs tp, fcsr, zero<br> [0x80000254]:sw tp, 68(ra)<br>   |
|  10|[0x80002360]<br>0x00000000|- rs1 : x22<br> - rs2 : f22<br>                                                                                   |[0x80000268]:fsh fs6, 2048(s6)<br> [0x8000026c]:addi zero, zero, 0<br> [0x80000270]:addi zero, zero, 0<br> [0x80000274]:csrrs tp, fcsr, zero<br> [0x80000278]:sw tp, 76(ra)<br>   |
|  11|[0x80002368]<br>0x00000000|- rs1 : x21<br> - rs2 : f21<br>                                                                                   |[0x8000028c]:fsh fs5, 2048(s5)<br> [0x80000290]:addi zero, zero, 0<br> [0x80000294]:addi zero, zero, 0<br> [0x80000298]:csrrs tp, fcsr, zero<br> [0x8000029c]:sw tp, 84(ra)<br>   |
|  12|[0x80002370]<br>0x00000000|- rs1 : x20<br> - rs2 : f20<br>                                                                                   |[0x800002b0]:fsh fs4, 2048(s4)<br> [0x800002b4]:addi zero, zero, 0<br> [0x800002b8]:addi zero, zero, 0<br> [0x800002bc]:csrrs tp, fcsr, zero<br> [0x800002c0]:sw tp, 92(ra)<br>   |
|  13|[0x80002378]<br>0x00000000|- rs1 : x19<br> - rs2 : f19<br>                                                                                   |[0x800002d4]:fsh fs3, 2048(s3)<br> [0x800002d8]:addi zero, zero, 0<br> [0x800002dc]:addi zero, zero, 0<br> [0x800002e0]:csrrs tp, fcsr, zero<br> [0x800002e4]:sw tp, 100(ra)<br>  |
|  14|[0x80002380]<br>0x00000000|- rs1 : x18<br> - rs2 : f18<br>                                                                                   |[0x800002f8]:fsh fs2, 2048(s2)<br> [0x800002fc]:addi zero, zero, 0<br> [0x80000300]:addi zero, zero, 0<br> [0x80000304]:csrrs tp, fcsr, zero<br> [0x80000308]:sw tp, 108(ra)<br>  |
|  15|[0x80002388]<br>0x00000000|- rs1 : x17<br> - rs2 : f17<br>                                                                                   |[0x8000031c]:fsh fa7, 2048(a7)<br> [0x80000320]:addi zero, zero, 0<br> [0x80000324]:addi zero, zero, 0<br> [0x80000328]:csrrs tp, fcsr, zero<br> [0x8000032c]:sw tp, 116(ra)<br>  |
|  16|[0x80002390]<br>0x00000000|- rs1 : x16<br> - rs2 : f16<br>                                                                                   |[0x80000340]:fsh fa6, 2048(a6)<br> [0x80000344]:addi zero, zero, 0<br> [0x80000348]:addi zero, zero, 0<br> [0x8000034c]:csrrs tp, fcsr, zero<br> [0x80000350]:sw tp, 124(ra)<br>  |
|  17|[0x80002398]<br>0x00000000|- rs1 : x15<br> - rs2 : f15<br>                                                                                   |[0x80000364]:fsh fa5, 2048(a5)<br> [0x80000368]:addi zero, zero, 0<br> [0x8000036c]:addi zero, zero, 0<br> [0x80000370]:csrrs tp, fcsr, zero<br> [0x80000374]:sw tp, 132(ra)<br>  |
|  18|[0x800023a0]<br>0x00000000|- rs1 : x14<br> - rs2 : f14<br>                                                                                   |[0x80000388]:fsh fa4, 2048(a4)<br> [0x8000038c]:addi zero, zero, 0<br> [0x80000390]:addi zero, zero, 0<br> [0x80000394]:csrrs tp, fcsr, zero<br> [0x80000398]:sw tp, 140(ra)<br>  |
|  19|[0x800023a8]<br>0x00000000|- rs1 : x13<br> - rs2 : f13<br>                                                                                   |[0x800003ac]:fsh fa3, 2048(a3)<br> [0x800003b0]:addi zero, zero, 0<br> [0x800003b4]:addi zero, zero, 0<br> [0x800003b8]:csrrs tp, fcsr, zero<br> [0x800003bc]:sw tp, 148(ra)<br>  |
|  20|[0x800023b0]<br>0x00000000|- rs1 : x12<br> - rs2 : f12<br>                                                                                   |[0x800003d0]:fsh fa2, 2048(a2)<br> [0x800003d4]:addi zero, zero, 0<br> [0x800003d8]:addi zero, zero, 0<br> [0x800003dc]:csrrs tp, fcsr, zero<br> [0x800003e0]:sw tp, 156(ra)<br>  |
|  21|[0x800023b8]<br>0x00000000|- rs1 : x11<br> - rs2 : f11<br>                                                                                   |[0x800003f4]:fsh fa1, 2048(a1)<br> [0x800003f8]:addi zero, zero, 0<br> [0x800003fc]:addi zero, zero, 0<br> [0x80000400]:csrrs tp, fcsr, zero<br> [0x80000404]:sw tp, 164(ra)<br>  |
|  22|[0x800023c0]<br>0x00000000|- rs1 : x10<br> - rs2 : f10<br>                                                                                   |[0x80000418]:fsh fa0, 2048(a0)<br> [0x8000041c]:addi zero, zero, 0<br> [0x80000420]:addi zero, zero, 0<br> [0x80000424]:csrrs tp, fcsr, zero<br> [0x80000428]:sw tp, 172(ra)<br>  |
|  23|[0x800023c8]<br>0x00000000|- rs1 : x9<br> - rs2 : f9<br>                                                                                     |[0x8000043c]:fsh fs1, 2048(s1)<br> [0x80000440]:addi zero, zero, 0<br> [0x80000444]:addi zero, zero, 0<br> [0x80000448]:csrrs tp, fcsr, zero<br> [0x8000044c]:sw tp, 180(ra)<br>  |
|  24|[0x800023d0]<br>0x00000000|- rs1 : x8<br> - rs2 : f8<br>                                                                                     |[0x80000460]:fsh fs0, 2048(fp)<br> [0x80000464]:addi zero, zero, 0<br> [0x80000468]:addi zero, zero, 0<br> [0x8000046c]:csrrs tp, fcsr, zero<br> [0x80000470]:sw tp, 188(ra)<br>  |
|  25|[0x800023d8]<br>0x00000000|- rs1 : x7<br> - rs2 : f7<br>                                                                                     |[0x8000048c]:fsh ft7, 2048(t2)<br> [0x80000490]:addi zero, zero, 0<br> [0x80000494]:addi zero, zero, 0<br> [0x80000498]:csrrs s1, fcsr, zero<br> [0x8000049c]:sw s1, 196(ra)<br>  |
|  26|[0x800023e0]<br>0x00000000|- rs1 : x6<br> - rs2 : f6<br>                                                                                     |[0x800004b0]:fsh ft6, 2048(t1)<br> [0x800004b4]:addi zero, zero, 0<br> [0x800004b8]:addi zero, zero, 0<br> [0x800004bc]:csrrs s1, fcsr, zero<br> [0x800004c0]:sw s1, 204(ra)<br>  |
|  27|[0x800023e8]<br>0x00000000|- rs1 : x5<br> - rs2 : f5<br>                                                                                     |[0x800004d4]:fsh ft5, 2048(t0)<br> [0x800004d8]:addi zero, zero, 0<br> [0x800004dc]:addi zero, zero, 0<br> [0x800004e0]:csrrs s1, fcsr, zero<br> [0x800004e4]:sw s1, 212(ra)<br>  |
|  28|[0x800023f0]<br>0x00000000|- rs1 : x4<br> - rs2 : f4<br>                                                                                     |[0x80000500]:fsh ft4, 2048(tp)<br> [0x80000504]:addi zero, zero, 0<br> [0x80000508]:addi zero, zero, 0<br> [0x8000050c]:csrrs s1, fcsr, zero<br> [0x80000510]:sw s1, 4(t0)<br>    |
|  29|[0x800023f8]<br>0x00000000|- rs1 : x3<br> - rs2 : f3<br>                                                                                     |[0x80000524]:fsh ft3, 2048(gp)<br> [0x80000528]:addi zero, zero, 0<br> [0x8000052c]:addi zero, zero, 0<br> [0x80000530]:csrrs s1, fcsr, zero<br> [0x80000534]:sw s1, 12(t0)<br>   |
|  30|[0x80002400]<br>0x00000000|- rs1 : x2<br> - rs2 : f2<br>                                                                                     |[0x80000548]:fsh ft2, 2048(sp)<br> [0x8000054c]:addi zero, zero, 0<br> [0x80000550]:addi zero, zero, 0<br> [0x80000554]:csrrs s1, fcsr, zero<br> [0x80000558]:sw s1, 20(t0)<br>   |
|  31|[0x80002408]<br>0x00000000|- rs1 : x1<br> - rs2 : f1<br>                                                                                     |[0x8000056c]:fsh ft1, 2048(ra)<br> [0x80000570]:addi zero, zero, 0<br> [0x80000574]:addi zero, zero, 0<br> [0x80000578]:csrrs s1, fcsr, zero<br> [0x8000057c]:sw s1, 28(t0)<br>   |
|  32|[0x80002410]<br>0x00000000|- rs2 : f0<br>                                                                                                    |[0x80000590]:fsh ft0, 2048(t6)<br> [0x80000594]:addi zero, zero, 0<br> [0x80000598]:addi zero, zero, 0<br> [0x8000059c]:csrrs s1, fcsr, zero<br> [0x800005a0]:sw s1, 36(t0)<br>   |

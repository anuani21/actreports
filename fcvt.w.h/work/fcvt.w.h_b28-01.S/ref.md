
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
| COV_LABELS                | fcvt.w.h_b28      |
| TEST_NAME                 | /home/anusha/new/RV32H/fcvt.w.h/work/fcvt.w.h_b28-01.S/ref.S    |
| Total Number of coverpoints| 93     |
| Total Coverpoints Hit     | 93      |
| Total Signature Updates   | 64      |
| STAT1                     | 32      |
| STAT2                     | 0      |
| STAT3                     | 0     |
| STAT4                     | 32     |
| STAT5                     | 0     |

## Details for STAT2:

```


```

## Details of STAT3

```


```

## Details of STAT4:

```
Last Coverpoint : ['mnemonic : fcvt.w.h', 'rs1 : f31', 'rd : x31', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000120]:fcvt.w.h t6, ft11, dyn
	-[0x80000124]:csrrs tp, fcsr, zero
	-[0x80000128]:sw t6, 0(ra)
Current Store : [0x8000012c] : sw tp, 4(ra) -- Store: [0x80002218]:0x00000010




Last Coverpoint : ['rs1 : f30', 'rd : x30', 'fs1 == 0 and fe1 == 0x0e and fm1 == 0x092 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000013c]:fcvt.w.h t5, ft10, dyn
	-[0x80000140]:csrrs tp, fcsr, zero
	-[0x80000144]:sw t5, 8(ra)
Current Store : [0x80000148] : sw tp, 12(ra) -- Store: [0x80002220]:0x00000010




Last Coverpoint : ['rs1 : f29', 'rd : x29', 'fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000158]:fcvt.w.h t4, ft9, dyn
	-[0x8000015c]:csrrs tp, fcsr, zero
	-[0x80000160]:sw t4, 16(ra)
Current Store : [0x80000164] : sw tp, 20(ra) -- Store: [0x80002228]:0x00000010




Last Coverpoint : ['rs1 : f28', 'rd : x28', 'fs1 == 0 and fe1 == 0x0f and fm1 == 0x100 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000174]:fcvt.w.h t3, ft8, dyn
	-[0x80000178]:csrrs tp, fcsr, zero
	-[0x8000017c]:sw t3, 24(ra)
Current Store : [0x80000180] : sw tp, 28(ra) -- Store: [0x80002230]:0x00000010




Last Coverpoint : ['rs1 : f27', 'rd : x27', 'fs1 == 0 and fe1 == 0x0f and fm1 == 0x200 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000190]:fcvt.w.h s11, fs11, dyn
	-[0x80000194]:csrrs tp, fcsr, zero
	-[0x80000198]:sw s11, 32(ra)
Current Store : [0x8000019c] : sw tp, 36(ra) -- Store: [0x80002238]:0x00000010




Last Coverpoint : ['rs1 : f26', 'rd : x26', 'fs1 == 0 and fe1 == 0x0f and fm1 == 0x300 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001ac]:fcvt.w.h s10, fs10, dyn
	-[0x800001b0]:csrrs tp, fcsr, zero
	-[0x800001b4]:sw s10, 40(ra)
Current Store : [0x800001b8] : sw tp, 44(ra) -- Store: [0x80002240]:0x00000010




Last Coverpoint : ['rs1 : f25', 'rd : x25', 'fs1 == 0 and fe1 == 0x10 and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001c8]:fcvt.w.h s9, fs9, dyn
	-[0x800001cc]:csrrs tp, fcsr, zero
	-[0x800001d0]:sw s9, 48(ra)
Current Store : [0x800001d4] : sw tp, 52(ra) -- Store: [0x80002248]:0x00000010




Last Coverpoint : ['rs1 : f24', 'rd : x24', 'fs1 == 0 and fe1 == 0x10 and fm1 == 0x080 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001e4]:fcvt.w.h s8, fs8, dyn
	-[0x800001e8]:csrrs tp, fcsr, zero
	-[0x800001ec]:sw s8, 56(ra)
Current Store : [0x800001f0] : sw tp, 60(ra) -- Store: [0x80002250]:0x00000010




Last Coverpoint : ['rs1 : f23', 'rd : x23', 'fs1 == 0 and fe1 == 0x10 and fm1 == 0x100 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000200]:fcvt.w.h s7, fs7, dyn
	-[0x80000204]:csrrs tp, fcsr, zero
	-[0x80000208]:sw s7, 64(ra)
Current Store : [0x8000020c] : sw tp, 68(ra) -- Store: [0x80002258]:0x00000010




Last Coverpoint : ['rs1 : f22', 'rd : x22', 'fs1 == 0 and fe1 == 0x10 and fm1 == 0x180 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000021c]:fcvt.w.h s6, fs6, dyn
	-[0x80000220]:csrrs tp, fcsr, zero
	-[0x80000224]:sw s6, 72(ra)
Current Store : [0x80000228] : sw tp, 76(ra) -- Store: [0x80002260]:0x00000010




Last Coverpoint : ['rs1 : f21', 'rd : x21', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x2dc and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000238]:fcvt.w.h s5, fs5, dyn
	-[0x8000023c]:csrrs tp, fcsr, zero
	-[0x80000240]:sw s5, 80(ra)
Current Store : [0x80000244] : sw tp, 84(ra) -- Store: [0x80002268]:0x00000010




Last Coverpoint : ['rs1 : f20', 'rd : x20', 'fs1 == 0 and fe1 == 0x1d and fm1 == 0x3ff and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000254]:fcvt.w.h s4, fs4, dyn
	-[0x80000258]:csrrs tp, fcsr, zero
	-[0x8000025c]:sw s4, 88(ra)
Current Store : [0x80000260] : sw tp, 92(ra) -- Store: [0x80002270]:0x00000010




Last Coverpoint : ['rs1 : f19', 'rd : x19', 'fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000270]:fcvt.w.h s3, fs3, dyn
	-[0x80000274]:csrrs tp, fcsr, zero
	-[0x80000278]:sw s3, 96(ra)
Current Store : [0x8000027c] : sw tp, 100(ra) -- Store: [0x80002278]:0x00000010




Last Coverpoint : ['rs1 : f18', 'rd : x18', 'fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000028c]:fcvt.w.h s2, fs2, dyn
	-[0x80000290]:csrrs tp, fcsr, zero
	-[0x80000294]:sw s2, 104(ra)
Current Store : [0x80000298] : sw tp, 108(ra) -- Store: [0x80002280]:0x00000010




Last Coverpoint : ['rs1 : f17', 'rd : x17', 'fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002a8]:fcvt.w.h a7, fa7, dyn
	-[0x800002ac]:csrrs tp, fcsr, zero
	-[0x800002b0]:sw a7, 112(ra)
Current Store : [0x800002b4] : sw tp, 116(ra) -- Store: [0x80002288]:0x00000010




Last Coverpoint : ['rs1 : f16', 'rd : x16', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002c4]:fcvt.w.h a6, fa6, dyn
	-[0x800002c8]:csrrs tp, fcsr, zero
	-[0x800002cc]:sw a6, 120(ra)
Current Store : [0x800002d0] : sw tp, 124(ra) -- Store: [0x80002290]:0x00000010




Last Coverpoint : ['rs1 : f15', 'rd : x15', 'fs1 == 1 and fe1 == 0x0d and fm1 == 0x2c0 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002e0]:fcvt.w.h a5, fa5, dyn
	-[0x800002e4]:csrrs tp, fcsr, zero
	-[0x800002e8]:sw a5, 128(ra)
Current Store : [0x800002ec] : sw tp, 132(ra) -- Store: [0x80002298]:0x00000010




Last Coverpoint : ['rs1 : f14', 'rd : x14', 'fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002fc]:fcvt.w.h a4, fa4, dyn
	-[0x80000300]:csrrs tp, fcsr, zero
	-[0x80000304]:sw a4, 136(ra)
Current Store : [0x80000308] : sw tp, 140(ra) -- Store: [0x800022a0]:0x00000010




Last Coverpoint : ['rs1 : f13', 'rd : x13', 'fs1 == 1 and fe1 == 0x10 and fm1 == 0x180 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000318]:fcvt.w.h a3, fa3, dyn
	-[0x8000031c]:csrrs tp, fcsr, zero
	-[0x80000320]:sw a3, 144(ra)
Current Store : [0x80000324] : sw tp, 148(ra) -- Store: [0x800022a8]:0x00000010




Last Coverpoint : ['rs1 : f12', 'rd : x12', 'fs1 == 1 and fe1 == 0x10 and fm1 == 0x100 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000334]:fcvt.w.h a2, fa2, dyn
	-[0x80000338]:csrrs tp, fcsr, zero
	-[0x8000033c]:sw a2, 152(ra)
Current Store : [0x80000340] : sw tp, 156(ra) -- Store: [0x800022b0]:0x00000010




Last Coverpoint : ['rs1 : f11', 'rd : x11', 'fs1 == 1 and fe1 == 0x10 and fm1 == 0x080 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000350]:fcvt.w.h a1, fa1, dyn
	-[0x80000354]:csrrs tp, fcsr, zero
	-[0x80000358]:sw a1, 160(ra)
Current Store : [0x8000035c] : sw tp, 164(ra) -- Store: [0x800022b8]:0x00000010




Last Coverpoint : ['rs1 : f10', 'rd : x10', 'fs1 == 1 and fe1 == 0x10 and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000036c]:fcvt.w.h a0, fa0, dyn
	-[0x80000370]:csrrs tp, fcsr, zero
	-[0x80000374]:sw a0, 168(ra)
Current Store : [0x80000378] : sw tp, 172(ra) -- Store: [0x800022c0]:0x00000010




Last Coverpoint : ['rs1 : f9', 'rd : x9', 'fs1 == 1 and fe1 == 0x0f and fm1 == 0x300 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000388]:fcvt.w.h s1, fs1, dyn
	-[0x8000038c]:csrrs tp, fcsr, zero
	-[0x80000390]:sw s1, 176(ra)
Current Store : [0x80000394] : sw tp, 180(ra) -- Store: [0x800022c8]:0x00000010




Last Coverpoint : ['rs1 : f8', 'rd : x8', 'fs1 == 1 and fe1 == 0x0f and fm1 == 0x200 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003a4]:fcvt.w.h fp, fs0, dyn
	-[0x800003a8]:csrrs tp, fcsr, zero
	-[0x800003ac]:sw fp, 184(ra)
Current Store : [0x800003b0] : sw tp, 188(ra) -- Store: [0x800022d0]:0x00000010




Last Coverpoint : ['rs1 : f7', 'rd : x7', 'fs1 == 1 and fe1 == 0x0f and fm1 == 0x100 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003c8]:fcvt.w.h t2, ft7, dyn
	-[0x800003cc]:csrrs s1, fcsr, zero
	-[0x800003d0]:sw t2, 192(ra)
Current Store : [0x800003d4] : sw s1, 196(ra) -- Store: [0x800022d8]:0x00000010




Last Coverpoint : ['rs1 : f6', 'rd : x6', 'fs1 == 1 and fe1 == 0x1d and fm1 == 0x259 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003e4]:fcvt.w.h t1, ft6, dyn
	-[0x800003e8]:csrrs s1, fcsr, zero
	-[0x800003ec]:sw t1, 200(ra)
Current Store : [0x800003f0] : sw s1, 204(ra) -- Store: [0x800022e0]:0x00000010




Last Coverpoint : ['rs1 : f5', 'rd : x5', 'fs1 == 1 and fe1 == 0x1e and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000400]:fcvt.w.h t0, ft5, dyn
	-[0x80000404]:csrrs s1, fcsr, zero
	-[0x80000408]:sw t0, 208(ra)
Current Store : [0x8000040c] : sw s1, 212(ra) -- Store: [0x800022e8]:0x00000010




Last Coverpoint : ['rs1 : f4', 'rd : x4', 'fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000424]:fcvt.w.h tp, ft4, dyn
	-[0x80000428]:csrrs s1, fcsr, zero
	-[0x8000042c]:sw tp, 0(t0)
Current Store : [0x80000430] : sw s1, 4(t0) -- Store: [0x800022f0]:0x00000010




Last Coverpoint : ['rs1 : f3', 'rd : x3']
Last Code Sequence : 
	-[0x80000440]:fcvt.w.h gp, ft3, dyn
	-[0x80000444]:csrrs s1, fcsr, zero
	-[0x80000448]:sw gp, 8(t0)
Current Store : [0x8000044c] : sw s1, 12(t0) -- Store: [0x800022f8]:0x00000010




Last Coverpoint : ['rs1 : f2', 'rd : x2']
Last Code Sequence : 
	-[0x8000045c]:fcvt.w.h sp, ft2, dyn
	-[0x80000460]:csrrs s1, fcsr, zero
	-[0x80000464]:sw sp, 16(t0)
Current Store : [0x80000468] : sw s1, 20(t0) -- Store: [0x80002300]:0x00000010




Last Coverpoint : ['rs1 : f1', 'rd : x1']
Last Code Sequence : 
	-[0x80000478]:fcvt.w.h ra, ft1, dyn
	-[0x8000047c]:csrrs s1, fcsr, zero
	-[0x80000480]:sw ra, 24(t0)
Current Store : [0x80000484] : sw s1, 28(t0) -- Store: [0x80002308]:0x00000010




Last Coverpoint : ['rs1 : f0', 'rd : x0']
Last Code Sequence : 
	-[0x80000494]:fcvt.w.h zero, ft0, dyn
	-[0x80000498]:csrrs s1, fcsr, zero
	-[0x8000049c]:sw zero, 32(t0)
Current Store : [0x800004a0] : sw s1, 36(t0) -- Store: [0x80002310]:0x00000010





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

|s.no|        signature         |                                                                                  coverpoints                                                                                   |                                                      code                                                      |
|---:|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
|   1|[0x80002214]<br>0x7FFFFFFF|- mnemonic : fcvt.w.h<br> - rs1 : f31<br> - rd : x31<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br> |[0x80000120]:fcvt.w.h t6, ft11, dyn<br> [0x80000124]:csrrs tp, fcsr, zero<br> [0x80000128]:sw t6, 0(ra)<br>     |
|   2|[0x8000221c]<br>0x7FFFFFFF|- rs1 : f30<br> - rd : x30<br> - fs1 == 0 and fe1 == 0x0e and fm1 == 0x092 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x8000013c]:fcvt.w.h t5, ft10, dyn<br> [0x80000140]:csrrs tp, fcsr, zero<br> [0x80000144]:sw t5, 8(ra)<br>     |
|   3|[0x80002224]<br>0x7FFFFFFF|- rs1 : f29<br> - rd : x29<br> - fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000158]:fcvt.w.h t4, ft9, dyn<br> [0x8000015c]:csrrs tp, fcsr, zero<br> [0x80000160]:sw t4, 16(ra)<br>     |
|   4|[0x8000222c]<br>0x7FFFFFFF|- rs1 : f28<br> - rd : x28<br> - fs1 == 0 and fe1 == 0x0f and fm1 == 0x100 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000174]:fcvt.w.h t3, ft8, dyn<br> [0x80000178]:csrrs tp, fcsr, zero<br> [0x8000017c]:sw t3, 24(ra)<br>     |
|   5|[0x80002234]<br>0x7FFFFFFF|- rs1 : f27<br> - rd : x27<br> - fs1 == 0 and fe1 == 0x0f and fm1 == 0x200 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000190]:fcvt.w.h s11, fs11, dyn<br> [0x80000194]:csrrs tp, fcsr, zero<br> [0x80000198]:sw s11, 32(ra)<br>  |
|   6|[0x8000223c]<br>0x7FFFFFFF|- rs1 : f26<br> - rd : x26<br> - fs1 == 0 and fe1 == 0x0f and fm1 == 0x300 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800001ac]:fcvt.w.h s10, fs10, dyn<br> [0x800001b0]:csrrs tp, fcsr, zero<br> [0x800001b4]:sw s10, 40(ra)<br>  |
|   7|[0x80002244]<br>0x7FFFFFFF|- rs1 : f25<br> - rd : x25<br> - fs1 == 0 and fe1 == 0x10 and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800001c8]:fcvt.w.h s9, fs9, dyn<br> [0x800001cc]:csrrs tp, fcsr, zero<br> [0x800001d0]:sw s9, 48(ra)<br>     |
|   8|[0x8000224c]<br>0x7FFFFFFF|- rs1 : f24<br> - rd : x24<br> - fs1 == 0 and fe1 == 0x10 and fm1 == 0x080 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800001e4]:fcvt.w.h s8, fs8, dyn<br> [0x800001e8]:csrrs tp, fcsr, zero<br> [0x800001ec]:sw s8, 56(ra)<br>     |
|   9|[0x80002254]<br>0x7FFFFFFF|- rs1 : f23<br> - rd : x23<br> - fs1 == 0 and fe1 == 0x10 and fm1 == 0x100 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000200]:fcvt.w.h s7, fs7, dyn<br> [0x80000204]:csrrs tp, fcsr, zero<br> [0x80000208]:sw s7, 64(ra)<br>     |
|  10|[0x8000225c]<br>0x7FFFFFFF|- rs1 : f22<br> - rd : x22<br> - fs1 == 0 and fe1 == 0x10 and fm1 == 0x180 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x8000021c]:fcvt.w.h s6, fs6, dyn<br> [0x80000220]:csrrs tp, fcsr, zero<br> [0x80000224]:sw s6, 72(ra)<br>     |
|  11|[0x80002264]<br>0x7FFFFFFF|- rs1 : f21<br> - rd : x21<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x2dc and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000238]:fcvt.w.h s5, fs5, dyn<br> [0x8000023c]:csrrs tp, fcsr, zero<br> [0x80000240]:sw s5, 80(ra)<br>     |
|  12|[0x8000226c]<br>0x7FFFFFFF|- rs1 : f20<br> - rd : x20<br> - fs1 == 0 and fe1 == 0x1d and fm1 == 0x3ff and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000254]:fcvt.w.h s4, fs4, dyn<br> [0x80000258]:csrrs tp, fcsr, zero<br> [0x8000025c]:sw s4, 88(ra)<br>     |
|  13|[0x80002274]<br>0x7FFFFFFF|- rs1 : f19<br> - rd : x19<br> - fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000270]:fcvt.w.h s3, fs3, dyn<br> [0x80000274]:csrrs tp, fcsr, zero<br> [0x80000278]:sw s3, 96(ra)<br>     |
|  14|[0x8000227c]<br>0x7FFFFFFF|- rs1 : f18<br> - rd : x18<br> - fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x8000028c]:fcvt.w.h s2, fs2, dyn<br> [0x80000290]:csrrs tp, fcsr, zero<br> [0x80000294]:sw s2, 104(ra)<br>    |
|  15|[0x80002284]<br>0x7FFFFFFF|- rs1 : f17<br> - rd : x17<br> - fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800002a8]:fcvt.w.h a7, fa7, dyn<br> [0x800002ac]:csrrs tp, fcsr, zero<br> [0x800002b0]:sw a7, 112(ra)<br>    |
|  16|[0x8000228c]<br>0x7FFFFFFF|- rs1 : f16<br> - rd : x16<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800002c4]:fcvt.w.h a6, fa6, dyn<br> [0x800002c8]:csrrs tp, fcsr, zero<br> [0x800002cc]:sw a6, 120(ra)<br>    |
|  17|[0x80002294]<br>0x7FFFFFFF|- rs1 : f15<br> - rd : x15<br> - fs1 == 1 and fe1 == 0x0d and fm1 == 0x2c0 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800002e0]:fcvt.w.h a5, fa5, dyn<br> [0x800002e4]:csrrs tp, fcsr, zero<br> [0x800002e8]:sw a5, 128(ra)<br>    |
|  18|[0x8000229c]<br>0x7FFFFFFF|- rs1 : f14<br> - rd : x14<br> - fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800002fc]:fcvt.w.h a4, fa4, dyn<br> [0x80000300]:csrrs tp, fcsr, zero<br> [0x80000304]:sw a4, 136(ra)<br>    |
|  19|[0x800022a4]<br>0x7FFFFFFF|- rs1 : f13<br> - rd : x13<br> - fs1 == 1 and fe1 == 0x10 and fm1 == 0x180 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000318]:fcvt.w.h a3, fa3, dyn<br> [0x8000031c]:csrrs tp, fcsr, zero<br> [0x80000320]:sw a3, 144(ra)<br>    |
|  20|[0x800022ac]<br>0x7FFFFFFF|- rs1 : f12<br> - rd : x12<br> - fs1 == 1 and fe1 == 0x10 and fm1 == 0x100 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000334]:fcvt.w.h a2, fa2, dyn<br> [0x80000338]:csrrs tp, fcsr, zero<br> [0x8000033c]:sw a2, 152(ra)<br>    |
|  21|[0x800022b4]<br>0x7FFFFFFF|- rs1 : f11<br> - rd : x11<br> - fs1 == 1 and fe1 == 0x10 and fm1 == 0x080 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000350]:fcvt.w.h a1, fa1, dyn<br> [0x80000354]:csrrs tp, fcsr, zero<br> [0x80000358]:sw a1, 160(ra)<br>    |
|  22|[0x800022bc]<br>0x7FFFFFFF|- rs1 : f10<br> - rd : x10<br> - fs1 == 1 and fe1 == 0x10 and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x8000036c]:fcvt.w.h a0, fa0, dyn<br> [0x80000370]:csrrs tp, fcsr, zero<br> [0x80000374]:sw a0, 168(ra)<br>    |
|  23|[0x800022c4]<br>0x7FFFFFFF|- rs1 : f9<br> - rd : x9<br> - fs1 == 1 and fe1 == 0x0f and fm1 == 0x300 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x80000388]:fcvt.w.h s1, fs1, dyn<br> [0x8000038c]:csrrs tp, fcsr, zero<br> [0x80000390]:sw s1, 176(ra)<br>    |
|  24|[0x800022cc]<br>0x7FFFFFFF|- rs1 : f8<br> - rd : x8<br> - fs1 == 1 and fe1 == 0x0f and fm1 == 0x200 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x800003a4]:fcvt.w.h fp, fs0, dyn<br> [0x800003a8]:csrrs tp, fcsr, zero<br> [0x800003ac]:sw fp, 184(ra)<br>    |
|  25|[0x800022d4]<br>0x7FFFFFFF|- rs1 : f7<br> - rd : x7<br> - fs1 == 1 and fe1 == 0x0f and fm1 == 0x100 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x800003c8]:fcvt.w.h t2, ft7, dyn<br> [0x800003cc]:csrrs s1, fcsr, zero<br> [0x800003d0]:sw t2, 192(ra)<br>    |
|  26|[0x800022dc]<br>0x7FFFFFFF|- rs1 : f6<br> - rd : x6<br> - fs1 == 1 and fe1 == 0x1d and fm1 == 0x259 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x800003e4]:fcvt.w.h t1, ft6, dyn<br> [0x800003e8]:csrrs s1, fcsr, zero<br> [0x800003ec]:sw t1, 200(ra)<br>    |
|  27|[0x800022e4]<br>0x7FFFFFFF|- rs1 : f5<br> - rd : x5<br> - fs1 == 1 and fe1 == 0x1e and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x80000400]:fcvt.w.h t0, ft5, dyn<br> [0x80000404]:csrrs s1, fcsr, zero<br> [0x80000408]:sw t0, 208(ra)<br>    |
|  28|[0x800022ec]<br>0x7FFFFFFF|- rs1 : f4<br> - rd : x4<br> - fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x80000424]:fcvt.w.h tp, ft4, dyn<br> [0x80000428]:csrrs s1, fcsr, zero<br> [0x8000042c]:sw tp, 0(t0)<br>      |
|  29|[0x800022f4]<br>0x7FFFFFFF|- rs1 : f3<br> - rd : x3<br>                                                                                                                                                    |[0x80000440]:fcvt.w.h gp, ft3, dyn<br> [0x80000444]:csrrs s1, fcsr, zero<br> [0x80000448]:sw gp, 8(t0)<br>      |
|  30|[0x800022fc]<br>0x7FFFFFFF|- rs1 : f2<br> - rd : x2<br>                                                                                                                                                    |[0x8000045c]:fcvt.w.h sp, ft2, dyn<br> [0x80000460]:csrrs s1, fcsr, zero<br> [0x80000464]:sw sp, 16(t0)<br>     |
|  31|[0x80002304]<br>0x7FFFFFFF|- rs1 : f1<br> - rd : x1<br>                                                                                                                                                    |[0x80000478]:fcvt.w.h ra, ft1, dyn<br> [0x8000047c]:csrrs s1, fcsr, zero<br> [0x80000480]:sw ra, 24(t0)<br>     |
|  32|[0x8000230c]<br>0x00000000|- rs1 : f0<br> - rd : x0<br>                                                                                                                                                    |[0x80000494]:fcvt.w.h zero, ft0, dyn<br> [0x80000498]:csrrs s1, fcsr, zero<br> [0x8000049c]:sw zero, 32(t0)<br> |

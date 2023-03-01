
# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature.
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update signature
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x800000f8', '0x80000a00')]      |
| SIG_REGION                | [('0x80002310', '0x800025a0', '164 words')]      |
| COV_LABELS                | fcvt.wu.h_b29      |
| TEST_NAME                 | /home/anusha/new/RV32H/fcvt.wu.h/work/fcvt.wu.h_b29-01.S/ref.S    |
| Total Number of coverpoints| 145     |
| Total Coverpoints Hit     | 145      |
| Total Signature Updates   | 162      |
| STAT1                     | 80      |
| STAT2                     | 1      |
| STAT3                     | 0     |
| STAT4                     | 81     |
| STAT5                     | 0     |

## Details for STAT2:

```
Op without unique coverpoint updates Signature
 -- Code Sequence:
      [0x800009f0]:fcvt.wu.h t6, ft11, dyn
      [0x800009f4]:csrrs s1, fcsr, zero
      [0x800009f8]:sw t6, 424(t0)
 -- Signature Address: 0x80002594 Data: 0xFFFFFFFF
 -- Redundant Coverpoints hit by the op
      - mnemonic : fcvt.wu.h
      - rs1 : f31
      - rd : x31
      - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat






```

## Details of STAT3

```


```

## Details of STAT4:

```
Last Coverpoint : ['mnemonic : fcvt.wu.h', 'rs1 : f31', 'rd : x31', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000120]:fcvt.wu.h t6, ft11, dyn
	-[0x80000124]:csrrs tp, fcsr, zero
	-[0x80000128]:sw t6, 0(ra)
Current Store : [0x8000012c] : sw tp, 4(ra) -- Store: [0x80002318]:0x00000010




Last Coverpoint : ['rs1 : f30', 'rd : x30', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000013c]:fcvt.wu.h t5, ft10, dyn
	-[0x80000140]:csrrs tp, fcsr, zero
	-[0x80000144]:sw t5, 8(ra)
Current Store : [0x80000148] : sw tp, 12(ra) -- Store: [0x80002320]:0x00000030




Last Coverpoint : ['rs1 : f29', 'rd : x29', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000158]:fcvt.wu.h t4, ft9, dyn
	-[0x8000015c]:csrrs tp, fcsr, zero
	-[0x80000160]:sw t4, 16(ra)
Current Store : [0x80000164] : sw tp, 20(ra) -- Store: [0x80002328]:0x00000050




Last Coverpoint : ['rs1 : f28', 'rd : x28', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000174]:fcvt.wu.h t3, ft8, dyn
	-[0x80000178]:csrrs tp, fcsr, zero
	-[0x8000017c]:sw t3, 24(ra)
Current Store : [0x80000180] : sw tp, 28(ra) -- Store: [0x80002330]:0x00000070




Last Coverpoint : ['rs1 : f27', 'rd : x27', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000190]:fcvt.wu.h s11, fs11, dyn
	-[0x80000194]:csrrs tp, fcsr, zero
	-[0x80000198]:sw s11, 32(ra)
Current Store : [0x8000019c] : sw tp, 36(ra) -- Store: [0x80002338]:0x00000090




Last Coverpoint : ['rs1 : f26', 'rd : x26', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001ac]:fcvt.wu.h s10, fs10, dyn
	-[0x800001b0]:csrrs tp, fcsr, zero
	-[0x800001b4]:sw s10, 40(ra)
Current Store : [0x800001b8] : sw tp, 44(ra) -- Store: [0x80002340]:0x00000010




Last Coverpoint : ['rs1 : f25', 'rd : x25', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001c8]:fcvt.wu.h s9, fs9, dyn
	-[0x800001cc]:csrrs tp, fcsr, zero
	-[0x800001d0]:sw s9, 48(ra)
Current Store : [0x800001d4] : sw tp, 52(ra) -- Store: [0x80002348]:0x00000030




Last Coverpoint : ['rs1 : f24', 'rd : x24', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001e4]:fcvt.wu.h s8, fs8, dyn
	-[0x800001e8]:csrrs tp, fcsr, zero
	-[0x800001ec]:sw s8, 56(ra)
Current Store : [0x800001f0] : sw tp, 60(ra) -- Store: [0x80002350]:0x00000050




Last Coverpoint : ['rs1 : f23', 'rd : x23', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000200]:fcvt.wu.h s7, fs7, dyn
	-[0x80000204]:csrrs tp, fcsr, zero
	-[0x80000208]:sw s7, 64(ra)
Current Store : [0x8000020c] : sw tp, 68(ra) -- Store: [0x80002358]:0x00000070




Last Coverpoint : ['rs1 : f22', 'rd : x22', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000021c]:fcvt.wu.h s6, fs6, dyn
	-[0x80000220]:csrrs tp, fcsr, zero
	-[0x80000224]:sw s6, 72(ra)
Current Store : [0x80000228] : sw tp, 76(ra) -- Store: [0x80002360]:0x00000090




Last Coverpoint : ['rs1 : f21', 'rd : x21', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000238]:fcvt.wu.h s5, fs5, dyn
	-[0x8000023c]:csrrs tp, fcsr, zero
	-[0x80000240]:sw s5, 80(ra)
Current Store : [0x80000244] : sw tp, 84(ra) -- Store: [0x80002368]:0x00000010




Last Coverpoint : ['rs1 : f20', 'rd : x20', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000254]:fcvt.wu.h s4, fs4, dyn
	-[0x80000258]:csrrs tp, fcsr, zero
	-[0x8000025c]:sw s4, 88(ra)
Current Store : [0x80000260] : sw tp, 92(ra) -- Store: [0x80002370]:0x00000030




Last Coverpoint : ['rs1 : f19', 'rd : x19', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000270]:fcvt.wu.h s3, fs3, dyn
	-[0x80000274]:csrrs tp, fcsr, zero
	-[0x80000278]:sw s3, 96(ra)
Current Store : [0x8000027c] : sw tp, 100(ra) -- Store: [0x80002378]:0x00000050




Last Coverpoint : ['rs1 : f18', 'rd : x18', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000028c]:fcvt.wu.h s2, fs2, dyn
	-[0x80000290]:csrrs tp, fcsr, zero
	-[0x80000294]:sw s2, 104(ra)
Current Store : [0x80000298] : sw tp, 108(ra) -- Store: [0x80002380]:0x00000070




Last Coverpoint : ['rs1 : f17', 'rd : x17', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002a8]:fcvt.wu.h a7, fa7, dyn
	-[0x800002ac]:csrrs tp, fcsr, zero
	-[0x800002b0]:sw a7, 112(ra)
Current Store : [0x800002b4] : sw tp, 116(ra) -- Store: [0x80002388]:0x00000090




Last Coverpoint : ['rs1 : f16', 'rd : x16', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002c4]:fcvt.wu.h a6, fa6, dyn
	-[0x800002c8]:csrrs tp, fcsr, zero
	-[0x800002cc]:sw a6, 120(ra)
Current Store : [0x800002d0] : sw tp, 124(ra) -- Store: [0x80002390]:0x00000010




Last Coverpoint : ['rs1 : f15', 'rd : x15', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002e0]:fcvt.wu.h a5, fa5, dyn
	-[0x800002e4]:csrrs tp, fcsr, zero
	-[0x800002e8]:sw a5, 128(ra)
Current Store : [0x800002ec] : sw tp, 132(ra) -- Store: [0x80002398]:0x00000030




Last Coverpoint : ['rs1 : f14', 'rd : x14', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002fc]:fcvt.wu.h a4, fa4, dyn
	-[0x80000300]:csrrs tp, fcsr, zero
	-[0x80000304]:sw a4, 136(ra)
Current Store : [0x80000308] : sw tp, 140(ra) -- Store: [0x800023a0]:0x00000050




Last Coverpoint : ['rs1 : f13', 'rd : x13', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000318]:fcvt.wu.h a3, fa3, dyn
	-[0x8000031c]:csrrs tp, fcsr, zero
	-[0x80000320]:sw a3, 144(ra)
Current Store : [0x80000324] : sw tp, 148(ra) -- Store: [0x800023a8]:0x00000070




Last Coverpoint : ['rs1 : f12', 'rd : x12', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000334]:fcvt.wu.h a2, fa2, dyn
	-[0x80000338]:csrrs tp, fcsr, zero
	-[0x8000033c]:sw a2, 152(ra)
Current Store : [0x80000340] : sw tp, 156(ra) -- Store: [0x800023b0]:0x00000090




Last Coverpoint : ['rs1 : f11', 'rd : x11', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000350]:fcvt.wu.h a1, fa1, dyn
	-[0x80000354]:csrrs tp, fcsr, zero
	-[0x80000358]:sw a1, 160(ra)
Current Store : [0x8000035c] : sw tp, 164(ra) -- Store: [0x800023b8]:0x00000010




Last Coverpoint : ['rs1 : f10', 'rd : x10', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000036c]:fcvt.wu.h a0, fa0, dyn
	-[0x80000370]:csrrs tp, fcsr, zero
	-[0x80000374]:sw a0, 168(ra)
Current Store : [0x80000378] : sw tp, 172(ra) -- Store: [0x800023c0]:0x00000030




Last Coverpoint : ['rs1 : f9', 'rd : x9', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000388]:fcvt.wu.h s1, fs1, dyn
	-[0x8000038c]:csrrs tp, fcsr, zero
	-[0x80000390]:sw s1, 176(ra)
Current Store : [0x80000394] : sw tp, 180(ra) -- Store: [0x800023c8]:0x00000050




Last Coverpoint : ['rs1 : f8', 'rd : x8', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003a4]:fcvt.wu.h fp, fs0, dyn
	-[0x800003a8]:csrrs tp, fcsr, zero
	-[0x800003ac]:sw fp, 184(ra)
Current Store : [0x800003b0] : sw tp, 188(ra) -- Store: [0x800023d0]:0x00000070




Last Coverpoint : ['rs1 : f7', 'rd : x7', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003c8]:fcvt.wu.h t2, ft7, dyn
	-[0x800003cc]:csrrs s1, fcsr, zero
	-[0x800003d0]:sw t2, 192(ra)
Current Store : [0x800003d4] : sw s1, 196(ra) -- Store: [0x800023d8]:0x00000090




Last Coverpoint : ['rs1 : f6', 'rd : x6', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003e4]:fcvt.wu.h t1, ft6, dyn
	-[0x800003e8]:csrrs s1, fcsr, zero
	-[0x800003ec]:sw t1, 200(ra)
Current Store : [0x800003f0] : sw s1, 204(ra) -- Store: [0x800023e0]:0x00000010




Last Coverpoint : ['rs1 : f5', 'rd : x5', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000400]:fcvt.wu.h t0, ft5, dyn
	-[0x80000404]:csrrs s1, fcsr, zero
	-[0x80000408]:sw t0, 208(ra)
Current Store : [0x8000040c] : sw s1, 212(ra) -- Store: [0x800023e8]:0x00000030




Last Coverpoint : ['rs1 : f4', 'rd : x4', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000424]:fcvt.wu.h tp, ft4, dyn
	-[0x80000428]:csrrs s1, fcsr, zero
	-[0x8000042c]:sw tp, 0(t0)
Current Store : [0x80000430] : sw s1, 4(t0) -- Store: [0x800023f0]:0x00000050




Last Coverpoint : ['rs1 : f3', 'rd : x3', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000440]:fcvt.wu.h gp, ft3, dyn
	-[0x80000444]:csrrs s1, fcsr, zero
	-[0x80000448]:sw gp, 8(t0)
Current Store : [0x8000044c] : sw s1, 12(t0) -- Store: [0x800023f8]:0x00000070




Last Coverpoint : ['rs1 : f2', 'rd : x2', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000045c]:fcvt.wu.h sp, ft2, dyn
	-[0x80000460]:csrrs s1, fcsr, zero
	-[0x80000464]:sw sp, 16(t0)
Current Store : [0x80000468] : sw s1, 20(t0) -- Store: [0x80002400]:0x00000090




Last Coverpoint : ['rs1 : f1', 'rd : x1', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000478]:fcvt.wu.h ra, ft1, dyn
	-[0x8000047c]:csrrs s1, fcsr, zero
	-[0x80000480]:sw ra, 24(t0)
Current Store : [0x80000484] : sw s1, 28(t0) -- Store: [0x80002408]:0x00000010




Last Coverpoint : ['rs1 : f0', 'rd : x0', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000494]:fcvt.wu.h zero, ft0, dyn
	-[0x80000498]:csrrs s1, fcsr, zero
	-[0x8000049c]:sw zero, 32(t0)
Current Store : [0x800004a0] : sw s1, 36(t0) -- Store: [0x80002410]:0x00000030




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800004b0]:fcvt.wu.h t6, ft11, dyn
	-[0x800004b4]:csrrs s1, fcsr, zero
	-[0x800004b8]:sw t6, 40(t0)
Current Store : [0x800004bc] : sw s1, 44(t0) -- Store: [0x80002418]:0x00000050




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800004cc]:fcvt.wu.h t6, ft11, dyn
	-[0x800004d0]:csrrs s1, fcsr, zero
	-[0x800004d4]:sw t6, 48(t0)
Current Store : [0x800004d8] : sw s1, 52(t0) -- Store: [0x80002420]:0x00000070




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800004e8]:fcvt.wu.h t6, ft11, dyn
	-[0x800004ec]:csrrs s1, fcsr, zero
	-[0x800004f0]:sw t6, 56(t0)
Current Store : [0x800004f4] : sw s1, 60(t0) -- Store: [0x80002428]:0x00000090




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000504]:fcvt.wu.h t6, ft11, dyn
	-[0x80000508]:csrrs s1, fcsr, zero
	-[0x8000050c]:sw t6, 64(t0)
Current Store : [0x80000510] : sw s1, 68(t0) -- Store: [0x80002430]:0x00000010




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000520]:fcvt.wu.h t6, ft11, dyn
	-[0x80000524]:csrrs s1, fcsr, zero
	-[0x80000528]:sw t6, 72(t0)
Current Store : [0x8000052c] : sw s1, 76(t0) -- Store: [0x80002438]:0x00000030




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000053c]:fcvt.wu.h t6, ft11, dyn
	-[0x80000540]:csrrs s1, fcsr, zero
	-[0x80000544]:sw t6, 80(t0)
Current Store : [0x80000548] : sw s1, 84(t0) -- Store: [0x80002440]:0x00000050




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000558]:fcvt.wu.h t6, ft11, dyn
	-[0x8000055c]:csrrs s1, fcsr, zero
	-[0x80000560]:sw t6, 88(t0)
Current Store : [0x80000564] : sw s1, 92(t0) -- Store: [0x80002448]:0x00000070




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000574]:fcvt.wu.h t6, ft11, dyn
	-[0x80000578]:csrrs s1, fcsr, zero
	-[0x8000057c]:sw t6, 96(t0)
Current Store : [0x80000580] : sw s1, 100(t0) -- Store: [0x80002450]:0x00000090




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000590]:fcvt.wu.h t6, ft11, dyn
	-[0x80000594]:csrrs s1, fcsr, zero
	-[0x80000598]:sw t6, 104(t0)
Current Store : [0x8000059c] : sw s1, 108(t0) -- Store: [0x80002458]:0x00000010




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800005ac]:fcvt.wu.h t6, ft11, dyn
	-[0x800005b0]:csrrs s1, fcsr, zero
	-[0x800005b4]:sw t6, 112(t0)
Current Store : [0x800005b8] : sw s1, 116(t0) -- Store: [0x80002460]:0x00000030




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800005c8]:fcvt.wu.h t6, ft11, dyn
	-[0x800005cc]:csrrs s1, fcsr, zero
	-[0x800005d0]:sw t6, 120(t0)
Current Store : [0x800005d4] : sw s1, 124(t0) -- Store: [0x80002468]:0x00000050




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800005e4]:fcvt.wu.h t6, ft11, dyn
	-[0x800005e8]:csrrs s1, fcsr, zero
	-[0x800005ec]:sw t6, 128(t0)
Current Store : [0x800005f0] : sw s1, 132(t0) -- Store: [0x80002470]:0x00000070




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000600]:fcvt.wu.h t6, ft11, dyn
	-[0x80000604]:csrrs s1, fcsr, zero
	-[0x80000608]:sw t6, 136(t0)
Current Store : [0x8000060c] : sw s1, 140(t0) -- Store: [0x80002478]:0x00000090




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000061c]:fcvt.wu.h t6, ft11, dyn
	-[0x80000620]:csrrs s1, fcsr, zero
	-[0x80000624]:sw t6, 144(t0)
Current Store : [0x80000628] : sw s1, 148(t0) -- Store: [0x80002480]:0x00000010




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000638]:fcvt.wu.h t6, ft11, dyn
	-[0x8000063c]:csrrs s1, fcsr, zero
	-[0x80000640]:sw t6, 152(t0)
Current Store : [0x80000644] : sw s1, 156(t0) -- Store: [0x80002488]:0x00000030




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000654]:fcvt.wu.h t6, ft11, dyn
	-[0x80000658]:csrrs s1, fcsr, zero
	-[0x8000065c]:sw t6, 160(t0)
Current Store : [0x80000660] : sw s1, 164(t0) -- Store: [0x80002490]:0x00000050




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000670]:fcvt.wu.h t6, ft11, dyn
	-[0x80000674]:csrrs s1, fcsr, zero
	-[0x80000678]:sw t6, 168(t0)
Current Store : [0x8000067c] : sw s1, 172(t0) -- Store: [0x80002498]:0x00000070




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000068c]:fcvt.wu.h t6, ft11, dyn
	-[0x80000690]:csrrs s1, fcsr, zero
	-[0x80000694]:sw t6, 176(t0)
Current Store : [0x80000698] : sw s1, 180(t0) -- Store: [0x800024a0]:0x00000090




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006a8]:fcvt.wu.h t6, ft11, dyn
	-[0x800006ac]:csrrs s1, fcsr, zero
	-[0x800006b0]:sw t6, 184(t0)
Current Store : [0x800006b4] : sw s1, 188(t0) -- Store: [0x800024a8]:0x00000010




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006c4]:fcvt.wu.h t6, ft11, dyn
	-[0x800006c8]:csrrs s1, fcsr, zero
	-[0x800006cc]:sw t6, 192(t0)
Current Store : [0x800006d0] : sw s1, 196(t0) -- Store: [0x800024b0]:0x00000030




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006e0]:fcvt.wu.h t6, ft11, dyn
	-[0x800006e4]:csrrs s1, fcsr, zero
	-[0x800006e8]:sw t6, 200(t0)
Current Store : [0x800006ec] : sw s1, 204(t0) -- Store: [0x800024b8]:0x00000050




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006fc]:fcvt.wu.h t6, ft11, dyn
	-[0x80000700]:csrrs s1, fcsr, zero
	-[0x80000704]:sw t6, 208(t0)
Current Store : [0x80000708] : sw s1, 212(t0) -- Store: [0x800024c0]:0x00000070




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000718]:fcvt.wu.h t6, ft11, dyn
	-[0x8000071c]:csrrs s1, fcsr, zero
	-[0x80000720]:sw t6, 216(t0)
Current Store : [0x80000724] : sw s1, 220(t0) -- Store: [0x800024c8]:0x00000090




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000734]:fcvt.wu.h t6, ft11, dyn
	-[0x80000738]:csrrs s1, fcsr, zero
	-[0x8000073c]:sw t6, 224(t0)
Current Store : [0x80000740] : sw s1, 228(t0) -- Store: [0x800024d0]:0x00000010




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000750]:fcvt.wu.h t6, ft11, dyn
	-[0x80000754]:csrrs s1, fcsr, zero
	-[0x80000758]:sw t6, 232(t0)
Current Store : [0x8000075c] : sw s1, 236(t0) -- Store: [0x800024d8]:0x00000030




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000076c]:fcvt.wu.h t6, ft11, dyn
	-[0x80000770]:csrrs s1, fcsr, zero
	-[0x80000774]:sw t6, 240(t0)
Current Store : [0x80000778] : sw s1, 244(t0) -- Store: [0x800024e0]:0x00000050




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000788]:fcvt.wu.h t6, ft11, dyn
	-[0x8000078c]:csrrs s1, fcsr, zero
	-[0x80000790]:sw t6, 248(t0)
Current Store : [0x80000794] : sw s1, 252(t0) -- Store: [0x800024e8]:0x00000070




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007a4]:fcvt.wu.h t6, ft11, dyn
	-[0x800007a8]:csrrs s1, fcsr, zero
	-[0x800007ac]:sw t6, 256(t0)
Current Store : [0x800007b0] : sw s1, 260(t0) -- Store: [0x800024f0]:0x00000090




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007c0]:fcvt.wu.h t6, ft11, dyn
	-[0x800007c4]:csrrs s1, fcsr, zero
	-[0x800007c8]:sw t6, 264(t0)
Current Store : [0x800007cc] : sw s1, 268(t0) -- Store: [0x800024f8]:0x00000010




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007dc]:fcvt.wu.h t6, ft11, dyn
	-[0x800007e0]:csrrs s1, fcsr, zero
	-[0x800007e4]:sw t6, 272(t0)
Current Store : [0x800007e8] : sw s1, 276(t0) -- Store: [0x80002500]:0x00000030




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007f8]:fcvt.wu.h t6, ft11, dyn
	-[0x800007fc]:csrrs s1, fcsr, zero
	-[0x80000800]:sw t6, 280(t0)
Current Store : [0x80000804] : sw s1, 284(t0) -- Store: [0x80002508]:0x00000050




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000814]:fcvt.wu.h t6, ft11, dyn
	-[0x80000818]:csrrs s1, fcsr, zero
	-[0x8000081c]:sw t6, 288(t0)
Current Store : [0x80000820] : sw s1, 292(t0) -- Store: [0x80002510]:0x00000070




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000830]:fcvt.wu.h t6, ft11, dyn
	-[0x80000834]:csrrs s1, fcsr, zero
	-[0x80000838]:sw t6, 296(t0)
Current Store : [0x8000083c] : sw s1, 300(t0) -- Store: [0x80002518]:0x00000090




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000084c]:fcvt.wu.h t6, ft11, dyn
	-[0x80000850]:csrrs s1, fcsr, zero
	-[0x80000854]:sw t6, 304(t0)
Current Store : [0x80000858] : sw s1, 308(t0) -- Store: [0x80002520]:0x00000010




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000868]:fcvt.wu.h t6, ft11, dyn
	-[0x8000086c]:csrrs s1, fcsr, zero
	-[0x80000870]:sw t6, 312(t0)
Current Store : [0x80000874] : sw s1, 316(t0) -- Store: [0x80002528]:0x00000030




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000884]:fcvt.wu.h t6, ft11, dyn
	-[0x80000888]:csrrs s1, fcsr, zero
	-[0x8000088c]:sw t6, 320(t0)
Current Store : [0x80000890] : sw s1, 324(t0) -- Store: [0x80002530]:0x00000050




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008a0]:fcvt.wu.h t6, ft11, dyn
	-[0x800008a4]:csrrs s1, fcsr, zero
	-[0x800008a8]:sw t6, 328(t0)
Current Store : [0x800008ac] : sw s1, 332(t0) -- Store: [0x80002538]:0x00000070




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008bc]:fcvt.wu.h t6, ft11, dyn
	-[0x800008c0]:csrrs s1, fcsr, zero
	-[0x800008c4]:sw t6, 336(t0)
Current Store : [0x800008c8] : sw s1, 340(t0) -- Store: [0x80002540]:0x00000090




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008d8]:fcvt.wu.h t6, ft11, dyn
	-[0x800008dc]:csrrs s1, fcsr, zero
	-[0x800008e0]:sw t6, 344(t0)
Current Store : [0x800008e4] : sw s1, 348(t0) -- Store: [0x80002548]:0x00000010




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008f4]:fcvt.wu.h t6, ft11, dyn
	-[0x800008f8]:csrrs s1, fcsr, zero
	-[0x800008fc]:sw t6, 352(t0)
Current Store : [0x80000900] : sw s1, 356(t0) -- Store: [0x80002550]:0x00000030




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000910]:fcvt.wu.h t6, ft11, dyn
	-[0x80000914]:csrrs s1, fcsr, zero
	-[0x80000918]:sw t6, 360(t0)
Current Store : [0x8000091c] : sw s1, 364(t0) -- Store: [0x80002558]:0x00000050




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000092c]:fcvt.wu.h t6, ft11, dyn
	-[0x80000930]:csrrs s1, fcsr, zero
	-[0x80000934]:sw t6, 368(t0)
Current Store : [0x80000938] : sw s1, 372(t0) -- Store: [0x80002560]:0x00000070




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000948]:fcvt.wu.h t6, ft11, dyn
	-[0x8000094c]:csrrs s1, fcsr, zero
	-[0x80000950]:sw t6, 376(t0)
Current Store : [0x80000954] : sw s1, 380(t0) -- Store: [0x80002568]:0x00000090




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000964]:fcvt.wu.h t6, ft11, dyn
	-[0x80000968]:csrrs s1, fcsr, zero
	-[0x8000096c]:sw t6, 384(t0)
Current Store : [0x80000970] : sw s1, 388(t0) -- Store: [0x80002570]:0x00000010




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000980]:fcvt.wu.h t6, ft11, dyn
	-[0x80000984]:csrrs s1, fcsr, zero
	-[0x80000988]:sw t6, 392(t0)
Current Store : [0x8000098c] : sw s1, 396(t0) -- Store: [0x80002578]:0x00000030




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000099c]:fcvt.wu.h t6, ft11, dyn
	-[0x800009a0]:csrrs s1, fcsr, zero
	-[0x800009a4]:sw t6, 400(t0)
Current Store : [0x800009a8] : sw s1, 404(t0) -- Store: [0x80002580]:0x00000050




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800009b8]:fcvt.wu.h t6, ft11, dyn
	-[0x800009bc]:csrrs s1, fcsr, zero
	-[0x800009c0]:sw t6, 408(t0)
Current Store : [0x800009c4] : sw s1, 412(t0) -- Store: [0x80002588]:0x00000070




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800009d4]:fcvt.wu.h t6, ft11, dyn
	-[0x800009d8]:csrrs s1, fcsr, zero
	-[0x800009dc]:sw t6, 416(t0)
Current Store : [0x800009e0] : sw s1, 420(t0) -- Store: [0x80002590]:0x00000090




Last Coverpoint : ['mnemonic : fcvt.wu.h', 'rs1 : f31', 'rd : x31', 'fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800009f0]:fcvt.wu.h t6, ft11, dyn
	-[0x800009f4]:csrrs s1, fcsr, zero
	-[0x800009f8]:sw t6, 424(t0)
Current Store : [0x800009fc] : sw s1, 428(t0) -- Store: [0x80002598]:0x00000030





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

|s.no|        signature         |                                                                                   coverpoints                                                                                   |                                                      code                                                       |
|---:|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
|   1|[0x80002314]<br>0xFFFFFFFF|- mnemonic : fcvt.wu.h<br> - rs1 : f31<br> - rd : x31<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br> |[0x80000120]:fcvt.wu.h t6, ft11, dyn<br> [0x80000124]:csrrs tp, fcsr, zero<br> [0x80000128]:sw t6, 0(ra)<br>     |
|   2|[0x8000231c]<br>0xFFFFFFFF|- rs1 : f30<br> - rd : x30<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x8000013c]:fcvt.wu.h t5, ft10, dyn<br> [0x80000140]:csrrs tp, fcsr, zero<br> [0x80000144]:sw t5, 8(ra)<br>     |
|   3|[0x80002324]<br>0xFFFFFFFF|- rs1 : f29<br> - rd : x29<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000158]:fcvt.wu.h t4, ft9, dyn<br> [0x8000015c]:csrrs tp, fcsr, zero<br> [0x80000160]:sw t4, 16(ra)<br>     |
|   4|[0x8000232c]<br>0xFFFFFFFF|- rs1 : f28<br> - rd : x28<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000174]:fcvt.wu.h t3, ft8, dyn<br> [0x80000178]:csrrs tp, fcsr, zero<br> [0x8000017c]:sw t3, 24(ra)<br>     |
|   5|[0x80002334]<br>0xFFFFFFFF|- rs1 : f27<br> - rd : x27<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000190]:fcvt.wu.h s11, fs11, dyn<br> [0x80000194]:csrrs tp, fcsr, zero<br> [0x80000198]:sw s11, 32(ra)<br>  |
|   6|[0x8000233c]<br>0xFFFFFFFF|- rs1 : f26<br> - rd : x26<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                            |[0x800001ac]:fcvt.wu.h s10, fs10, dyn<br> [0x800001b0]:csrrs tp, fcsr, zero<br> [0x800001b4]:sw s10, 40(ra)<br>  |
|   7|[0x80002344]<br>0xFFFFFFFF|- rs1 : f25<br> - rd : x25<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800001c8]:fcvt.wu.h s9, fs9, dyn<br> [0x800001cc]:csrrs tp, fcsr, zero<br> [0x800001d0]:sw s9, 48(ra)<br>     |
|   8|[0x8000234c]<br>0xFFFFFFFF|- rs1 : f24<br> - rd : x24<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800001e4]:fcvt.wu.h s8, fs8, dyn<br> [0x800001e8]:csrrs tp, fcsr, zero<br> [0x800001ec]:sw s8, 56(ra)<br>     |
|   9|[0x80002354]<br>0xFFFFFFFF|- rs1 : f23<br> - rd : x23<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000200]:fcvt.wu.h s7, fs7, dyn<br> [0x80000204]:csrrs tp, fcsr, zero<br> [0x80000208]:sw s7, 64(ra)<br>     |
|  10|[0x8000235c]<br>0xFFFFFFFF|- rs1 : f22<br> - rd : x22<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x8000021c]:fcvt.wu.h s6, fs6, dyn<br> [0x80000220]:csrrs tp, fcsr, zero<br> [0x80000224]:sw s6, 72(ra)<br>     |
|  11|[0x80002364]<br>0xFFFFFFFF|- rs1 : f21<br> - rd : x21<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                            |[0x80000238]:fcvt.wu.h s5, fs5, dyn<br> [0x8000023c]:csrrs tp, fcsr, zero<br> [0x80000240]:sw s5, 80(ra)<br>     |
|  12|[0x8000236c]<br>0xFFFFFFFF|- rs1 : f20<br> - rd : x20<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000254]:fcvt.wu.h s4, fs4, dyn<br> [0x80000258]:csrrs tp, fcsr, zero<br> [0x8000025c]:sw s4, 88(ra)<br>     |
|  13|[0x80002374]<br>0xFFFFFFFF|- rs1 : f19<br> - rd : x19<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000270]:fcvt.wu.h s3, fs3, dyn<br> [0x80000274]:csrrs tp, fcsr, zero<br> [0x80000278]:sw s3, 96(ra)<br>     |
|  14|[0x8000237c]<br>0xFFFFFFFF|- rs1 : f18<br> - rd : x18<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x8000028c]:fcvt.wu.h s2, fs2, dyn<br> [0x80000290]:csrrs tp, fcsr, zero<br> [0x80000294]:sw s2, 104(ra)<br>    |
|  15|[0x80002384]<br>0xFFFFFFFF|- rs1 : f17<br> - rd : x17<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800002a8]:fcvt.wu.h a7, fa7, dyn<br> [0x800002ac]:csrrs tp, fcsr, zero<br> [0x800002b0]:sw a7, 112(ra)<br>    |
|  16|[0x8000238c]<br>0xFFFFFFFF|- rs1 : f16<br> - rd : x16<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                            |[0x800002c4]:fcvt.wu.h a6, fa6, dyn<br> [0x800002c8]:csrrs tp, fcsr, zero<br> [0x800002cc]:sw a6, 120(ra)<br>    |
|  17|[0x80002394]<br>0xFFFFFFFF|- rs1 : f15<br> - rd : x15<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800002e0]:fcvt.wu.h a5, fa5, dyn<br> [0x800002e4]:csrrs tp, fcsr, zero<br> [0x800002e8]:sw a5, 128(ra)<br>    |
|  18|[0x8000239c]<br>0xFFFFFFFF|- rs1 : f14<br> - rd : x14<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x800002fc]:fcvt.wu.h a4, fa4, dyn<br> [0x80000300]:csrrs tp, fcsr, zero<br> [0x80000304]:sw a4, 136(ra)<br>    |
|  19|[0x800023a4]<br>0xFFFFFFFF|- rs1 : f13<br> - rd : x13<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000318]:fcvt.wu.h a3, fa3, dyn<br> [0x8000031c]:csrrs tp, fcsr, zero<br> [0x80000320]:sw a3, 144(ra)<br>    |
|  20|[0x800023ac]<br>0xFFFFFFFF|- rs1 : f12<br> - rd : x12<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x80000334]:fcvt.wu.h a2, fa2, dyn<br> [0x80000338]:csrrs tp, fcsr, zero<br> [0x8000033c]:sw a2, 152(ra)<br>    |
|  21|[0x800023b4]<br>0xFFFFFFFF|- rs1 : f11<br> - rd : x11<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                            |[0x80000350]:fcvt.wu.h a1, fa1, dyn<br> [0x80000354]:csrrs tp, fcsr, zero<br> [0x80000358]:sw a1, 160(ra)<br>    |
|  22|[0x800023bc]<br>0xFFFFFFFF|- rs1 : f10<br> - rd : x10<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                           |[0x8000036c]:fcvt.wu.h a0, fa0, dyn<br> [0x80000370]:csrrs tp, fcsr, zero<br> [0x80000374]:sw a0, 168(ra)<br>    |
|  23|[0x800023c4]<br>0xFFFFFFFF|- rs1 : f9<br> - rd : x9<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x80000388]:fcvt.wu.h s1, fs1, dyn<br> [0x8000038c]:csrrs tp, fcsr, zero<br> [0x80000390]:sw s1, 176(ra)<br>    |
|  24|[0x800023cc]<br>0xFFFFFFFF|- rs1 : f8<br> - rd : x8<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x800003a4]:fcvt.wu.h fp, fs0, dyn<br> [0x800003a8]:csrrs tp, fcsr, zero<br> [0x800003ac]:sw fp, 184(ra)<br>    |
|  25|[0x800023d4]<br>0xFFFFFFFF|- rs1 : f7<br> - rd : x7<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x800003c8]:fcvt.wu.h t2, ft7, dyn<br> [0x800003cc]:csrrs s1, fcsr, zero<br> [0x800003d0]:sw t2, 192(ra)<br>    |
|  26|[0x800023dc]<br>0xFFFFFFFF|- rs1 : f6<br> - rd : x6<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                              |[0x800003e4]:fcvt.wu.h t1, ft6, dyn<br> [0x800003e8]:csrrs s1, fcsr, zero<br> [0x800003ec]:sw t1, 200(ra)<br>    |
|  27|[0x800023e4]<br>0xFFFFFFFF|- rs1 : f5<br> - rd : x5<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x80000400]:fcvt.wu.h t0, ft5, dyn<br> [0x80000404]:csrrs s1, fcsr, zero<br> [0x80000408]:sw t0, 208(ra)<br>    |
|  28|[0x800023ec]<br>0xFFFFFFFF|- rs1 : f4<br> - rd : x4<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x80000424]:fcvt.wu.h tp, ft4, dyn<br> [0x80000428]:csrrs s1, fcsr, zero<br> [0x8000042c]:sw tp, 0(t0)<br>      |
|  29|[0x800023f4]<br>0xFFFFFFFF|- rs1 : f3<br> - rd : x3<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x80000440]:fcvt.wu.h gp, ft3, dyn<br> [0x80000444]:csrrs s1, fcsr, zero<br> [0x80000448]:sw gp, 8(t0)<br>      |
|  30|[0x800023fc]<br>0xFFFFFFFF|- rs1 : f2<br> - rd : x2<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x8000045c]:fcvt.wu.h sp, ft2, dyn<br> [0x80000460]:csrrs s1, fcsr, zero<br> [0x80000464]:sw sp, 16(t0)<br>     |
|  31|[0x80002404]<br>0xFFFFFFFF|- rs1 : f1<br> - rd : x1<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                              |[0x80000478]:fcvt.wu.h ra, ft1, dyn<br> [0x8000047c]:csrrs s1, fcsr, zero<br> [0x80000480]:sw ra, 24(t0)<br>     |
|  32|[0x8000240c]<br>0x00000000|- rs1 : f0<br> - rd : x0<br> - fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                             |[0x80000494]:fcvt.wu.h zero, ft0, dyn<br> [0x80000498]:csrrs s1, fcsr, zero<br> [0x8000049c]:sw zero, 32(t0)<br> |
|  33|[0x80002414]<br>0xFFFFFFFF|- fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800004b0]:fcvt.wu.h t6, ft11, dyn<br> [0x800004b4]:csrrs s1, fcsr, zero<br> [0x800004b8]:sw t6, 40(t0)<br>    |
|  34|[0x8000241c]<br>0xFFFFFFFF|- fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800004cc]:fcvt.wu.h t6, ft11, dyn<br> [0x800004d0]:csrrs s1, fcsr, zero<br> [0x800004d4]:sw t6, 48(t0)<br>    |
|  35|[0x80002424]<br>0xFFFFFFFF|- fs1 == 0 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800004e8]:fcvt.wu.h t6, ft11, dyn<br> [0x800004ec]:csrrs s1, fcsr, zero<br> [0x800004f0]:sw t6, 56(t0)<br>    |
|  36|[0x8000242c]<br>0xFFFFFFFF|- fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                           |[0x80000504]:fcvt.wu.h t6, ft11, dyn<br> [0x80000508]:csrrs s1, fcsr, zero<br> [0x8000050c]:sw t6, 64(t0)<br>    |
|  37|[0x80002434]<br>0xFFFFFFFF|- fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000520]:fcvt.wu.h t6, ft11, dyn<br> [0x80000524]:csrrs s1, fcsr, zero<br> [0x80000528]:sw t6, 72(t0)<br>    |
|  38|[0x8000243c]<br>0xFFFFFFFF|- fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x8000053c]:fcvt.wu.h t6, ft11, dyn<br> [0x80000540]:csrrs s1, fcsr, zero<br> [0x80000544]:sw t6, 80(t0)<br>    |
|  39|[0x80002444]<br>0xFFFFFFFF|- fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000558]:fcvt.wu.h t6, ft11, dyn<br> [0x8000055c]:csrrs s1, fcsr, zero<br> [0x80000560]:sw t6, 88(t0)<br>    |
|  40|[0x8000244c]<br>0xFFFFFFFF|- fs1 == 0 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000574]:fcvt.wu.h t6, ft11, dyn<br> [0x80000578]:csrrs s1, fcsr, zero<br> [0x8000057c]:sw t6, 96(t0)<br>    |
|  41|[0x80002454]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                           |[0x80000590]:fcvt.wu.h t6, ft11, dyn<br> [0x80000594]:csrrs s1, fcsr, zero<br> [0x80000598]:sw t6, 104(t0)<br>   |
|  42|[0x8000245c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800005ac]:fcvt.wu.h t6, ft11, dyn<br> [0x800005b0]:csrrs s1, fcsr, zero<br> [0x800005b4]:sw t6, 112(t0)<br>   |
|  43|[0x80002464]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800005c8]:fcvt.wu.h t6, ft11, dyn<br> [0x800005cc]:csrrs s1, fcsr, zero<br> [0x800005d0]:sw t6, 120(t0)<br>   |
|  44|[0x8000246c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800005e4]:fcvt.wu.h t6, ft11, dyn<br> [0x800005e8]:csrrs s1, fcsr, zero<br> [0x800005ec]:sw t6, 128(t0)<br>   |
|  45|[0x80002474]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x248 and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000600]:fcvt.wu.h t6, ft11, dyn<br> [0x80000604]:csrrs s1, fcsr, zero<br> [0x80000608]:sw t6, 136(t0)<br>   |
|  46|[0x8000247c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                           |[0x8000061c]:fcvt.wu.h t6, ft11, dyn<br> [0x80000620]:csrrs s1, fcsr, zero<br> [0x80000624]:sw t6, 144(t0)<br>   |
|  47|[0x80002484]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000638]:fcvt.wu.h t6, ft11, dyn<br> [0x8000063c]:csrrs s1, fcsr, zero<br> [0x80000640]:sw t6, 152(t0)<br>   |
|  48|[0x8000248c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000654]:fcvt.wu.h t6, ft11, dyn<br> [0x80000658]:csrrs s1, fcsr, zero<br> [0x8000065c]:sw t6, 160(t0)<br>   |
|  49|[0x80002494]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000670]:fcvt.wu.h t6, ft11, dyn<br> [0x80000674]:csrrs s1, fcsr, zero<br> [0x80000678]:sw t6, 168(t0)<br>   |
|  50|[0x8000249c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x249 and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x8000068c]:fcvt.wu.h t6, ft11, dyn<br> [0x80000690]:csrrs s1, fcsr, zero<br> [0x80000694]:sw t6, 176(t0)<br>   |
|  51|[0x800024a4]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                           |[0x800006a8]:fcvt.wu.h t6, ft11, dyn<br> [0x800006ac]:csrrs s1, fcsr, zero<br> [0x800006b0]:sw t6, 184(t0)<br>   |
|  52|[0x800024ac]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800006c4]:fcvt.wu.h t6, ft11, dyn<br> [0x800006c8]:csrrs s1, fcsr, zero<br> [0x800006cc]:sw t6, 192(t0)<br>   |
|  53|[0x800024b4]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800006e0]:fcvt.wu.h t6, ft11, dyn<br> [0x800006e4]:csrrs s1, fcsr, zero<br> [0x800006e8]:sw t6, 200(t0)<br>   |
|  54|[0x800024bc]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800006fc]:fcvt.wu.h t6, ft11, dyn<br> [0x80000700]:csrrs s1, fcsr, zero<br> [0x80000704]:sw t6, 208(t0)<br>   |
|  55|[0x800024c4]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24a and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000718]:fcvt.wu.h t6, ft11, dyn<br> [0x8000071c]:csrrs s1, fcsr, zero<br> [0x80000720]:sw t6, 216(t0)<br>   |
|  56|[0x800024cc]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                           |[0x80000734]:fcvt.wu.h t6, ft11, dyn<br> [0x80000738]:csrrs s1, fcsr, zero<br> [0x8000073c]:sw t6, 224(t0)<br>   |
|  57|[0x800024d4]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000750]:fcvt.wu.h t6, ft11, dyn<br> [0x80000754]:csrrs s1, fcsr, zero<br> [0x80000758]:sw t6, 232(t0)<br>   |
|  58|[0x800024dc]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x8000076c]:fcvt.wu.h t6, ft11, dyn<br> [0x80000770]:csrrs s1, fcsr, zero<br> [0x80000774]:sw t6, 240(t0)<br>   |
|  59|[0x800024e4]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000788]:fcvt.wu.h t6, ft11, dyn<br> [0x8000078c]:csrrs s1, fcsr, zero<br> [0x80000790]:sw t6, 248(t0)<br>   |
|  60|[0x800024ec]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24b and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800007a4]:fcvt.wu.h t6, ft11, dyn<br> [0x800007a8]:csrrs s1, fcsr, zero<br> [0x800007ac]:sw t6, 256(t0)<br>   |
|  61|[0x800024f4]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                           |[0x800007c0]:fcvt.wu.h t6, ft11, dyn<br> [0x800007c4]:csrrs s1, fcsr, zero<br> [0x800007c8]:sw t6, 264(t0)<br>   |
|  62|[0x800024fc]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800007dc]:fcvt.wu.h t6, ft11, dyn<br> [0x800007e0]:csrrs s1, fcsr, zero<br> [0x800007e4]:sw t6, 272(t0)<br>   |
|  63|[0x80002504]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800007f8]:fcvt.wu.h t6, ft11, dyn<br> [0x800007fc]:csrrs s1, fcsr, zero<br> [0x80000800]:sw t6, 280(t0)<br>   |
|  64|[0x8000250c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000814]:fcvt.wu.h t6, ft11, dyn<br> [0x80000818]:csrrs s1, fcsr, zero<br> [0x8000081c]:sw t6, 288(t0)<br>   |
|  65|[0x80002514]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24c and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000830]:fcvt.wu.h t6, ft11, dyn<br> [0x80000834]:csrrs s1, fcsr, zero<br> [0x80000838]:sw t6, 296(t0)<br>   |
|  66|[0x8000251c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                           |[0x8000084c]:fcvt.wu.h t6, ft11, dyn<br> [0x80000850]:csrrs s1, fcsr, zero<br> [0x80000854]:sw t6, 304(t0)<br>   |
|  67|[0x80002524]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000868]:fcvt.wu.h t6, ft11, dyn<br> [0x8000086c]:csrrs s1, fcsr, zero<br> [0x80000870]:sw t6, 312(t0)<br>   |
|  68|[0x8000252c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000884]:fcvt.wu.h t6, ft11, dyn<br> [0x80000888]:csrrs s1, fcsr, zero<br> [0x8000088c]:sw t6, 320(t0)<br>   |
|  69|[0x80002534]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800008a0]:fcvt.wu.h t6, ft11, dyn<br> [0x800008a4]:csrrs s1, fcsr, zero<br> [0x800008a8]:sw t6, 328(t0)<br>   |
|  70|[0x8000253c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24d and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800008bc]:fcvt.wu.h t6, ft11, dyn<br> [0x800008c0]:csrrs s1, fcsr, zero<br> [0x800008c4]:sw t6, 336(t0)<br>   |
|  71|[0x80002544]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                           |[0x800008d8]:fcvt.wu.h t6, ft11, dyn<br> [0x800008dc]:csrrs s1, fcsr, zero<br> [0x800008e0]:sw t6, 344(t0)<br>   |
|  72|[0x8000254c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800008f4]:fcvt.wu.h t6, ft11, dyn<br> [0x800008f8]:csrrs s1, fcsr, zero<br> [0x800008fc]:sw t6, 352(t0)<br>   |
|  73|[0x80002554]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000910]:fcvt.wu.h t6, ft11, dyn<br> [0x80000914]:csrrs s1, fcsr, zero<br> [0x80000918]:sw t6, 360(t0)<br>   |
|  74|[0x8000255c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x8000092c]:fcvt.wu.h t6, ft11, dyn<br> [0x80000930]:csrrs s1, fcsr, zero<br> [0x80000934]:sw t6, 368(t0)<br>   |
|  75|[0x80002564]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24e and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000948]:fcvt.wu.h t6, ft11, dyn<br> [0x8000094c]:csrrs s1, fcsr, zero<br> [0x80000950]:sw t6, 376(t0)<br>   |
|  76|[0x8000256c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x0 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                           |[0x80000964]:fcvt.wu.h t6, ft11, dyn<br> [0x80000968]:csrrs s1, fcsr, zero<br> [0x8000096c]:sw t6, 384(t0)<br>   |
|  77|[0x80002574]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x20 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x80000980]:fcvt.wu.h t6, ft11, dyn<br> [0x80000984]:csrrs s1, fcsr, zero<br> [0x80000988]:sw t6, 392(t0)<br>   |
|  78|[0x8000257c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x40 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x8000099c]:fcvt.wu.h t6, ft11, dyn<br> [0x800009a0]:csrrs s1, fcsr, zero<br> [0x800009a4]:sw t6, 400(t0)<br>   |
|  79|[0x80002584]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x60 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800009b8]:fcvt.wu.h t6, ft11, dyn<br> [0x800009bc]:csrrs s1, fcsr, zero<br> [0x800009c0]:sw t6, 408(t0)<br>   |
|  80|[0x8000258c]<br>0xFFFFFFFF|- fs1 == 1 and fe1 == 0x0c and fm1 == 0x24f and  fcsr == 0x80 and rm_val == 7  and rs1_nan_prefix == 0xffff  #nosat<br>                                                          |[0x800009d4]:fcvt.wu.h t6, ft11, dyn<br> [0x800009d8]:csrrs s1, fcsr, zero<br> [0x800009dc]:sw t6, 416(t0)<br>   |

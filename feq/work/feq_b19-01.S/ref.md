
# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature.
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update signature
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x800000f8', '0x8000e070')]      |
| SIG_REGION                | [('0x80012310', '0x80014470', '2136 words')]      |
| COV_LABELS                | feq_b19      |
| TEST_NAME                 | /home/anusha/new/RV32H/feq/work/feq_b19-01.S/ref.S    |
| Total Number of coverpoints| 1163     |
| Total Coverpoints Hit     | 1163      |
| Total Signature Updates   | 2132      |
| STAT1                     | 1065      |
| STAT2                     | 1      |
| STAT3                     | 0     |
| STAT4                     | 1066     |
| STAT5                     | 0     |

## Details for STAT2:

```
Op without unique coverpoint updates Signature
 -- Code Sequence:
      [0x8000e05c]:feq.h t6, ft11, ft10
      [0x8000e060]:csrrs a0, fcsr, zero
      [0x8000e064]:sw t6, 120(t1)
 -- Signature Address: 0x8001445c Data: 0x00000000
 -- Redundant Coverpoints hit by the op
      - mnemonic : feq.h
      - rs1 : f31
      - rs2 : f30
      - rd : x31
      - rs1 != rs2
      - fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat






```

## Details of STAT3

```


```

## Details of STAT4:

```
Last Coverpoint : ['mnemonic : feq.h', 'rs1 : f31', 'rs2 : f30', 'rd : x31', 'rs1 != rs2', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000124]:feq.h t6, ft11, ft10
	-[0x80000128]:csrrs tp, fcsr, zero
	-[0x8000012c]:sw t6, 0(ra)
Current Store : [0x80000130] : sw tp, 4(ra) -- Store: [0x80012318]:0x00000000




Last Coverpoint : ['rs1 : f29', 'rs2 : f29', 'rd : x30', 'rs1 == rs2']
Last Code Sequence : 
	-[0x80000144]:feq.h t5, ft9, ft9
	-[0x80000148]:csrrs tp, fcsr, zero
	-[0x8000014c]:sw t5, 8(ra)
Current Store : [0x80000150] : sw tp, 12(ra) -- Store: [0x80012320]:0x00000000




Last Coverpoint : ['rs1 : f30', 'rs2 : f31', 'rd : x29', 'fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000164]:feq.h t4, ft10, ft11
	-[0x80000168]:csrrs tp, fcsr, zero
	-[0x8000016c]:sw t4, 16(ra)
Current Store : [0x80000170] : sw tp, 20(ra) -- Store: [0x80012328]:0x00000000




Last Coverpoint : ['rs1 : f28', 'rs2 : f27', 'rd : x28', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000184]:feq.h t3, ft8, fs11
	-[0x80000188]:csrrs tp, fcsr, zero
	-[0x8000018c]:sw t3, 24(ra)
Current Store : [0x80000190] : sw tp, 28(ra) -- Store: [0x80012330]:0x00000000




Last Coverpoint : ['rs1 : f27', 'rs2 : f28', 'rd : x27', 'fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001a4]:feq.h s11, fs11, ft8
	-[0x800001a8]:csrrs tp, fcsr, zero
	-[0x800001ac]:sw s11, 32(ra)
Current Store : [0x800001b0] : sw tp, 36(ra) -- Store: [0x80012338]:0x00000000




Last Coverpoint : ['rs1 : f26', 'rs2 : f25', 'rd : x26', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001c4]:feq.h s10, fs10, fs9
	-[0x800001c8]:csrrs tp, fcsr, zero
	-[0x800001cc]:sw s10, 40(ra)
Current Store : [0x800001d0] : sw tp, 44(ra) -- Store: [0x80012340]:0x00000000




Last Coverpoint : ['rs1 : f25', 'rs2 : f26', 'rd : x25', 'fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001e4]:feq.h s9, fs9, fs10
	-[0x800001e8]:csrrs tp, fcsr, zero
	-[0x800001ec]:sw s9, 48(ra)
Current Store : [0x800001f0] : sw tp, 52(ra) -- Store: [0x80012348]:0x00000000




Last Coverpoint : ['rs1 : f24', 'rs2 : f23', 'rd : x24', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000204]:feq.h s8, fs8, fs7
	-[0x80000208]:csrrs tp, fcsr, zero
	-[0x8000020c]:sw s8, 56(ra)
Current Store : [0x80000210] : sw tp, 60(ra) -- Store: [0x80012350]:0x00000000




Last Coverpoint : ['rs1 : f23', 'rs2 : f24', 'rd : x23', 'fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000224]:feq.h s7, fs7, fs8
	-[0x80000228]:csrrs tp, fcsr, zero
	-[0x8000022c]:sw s7, 64(ra)
Current Store : [0x80000230] : sw tp, 68(ra) -- Store: [0x80012358]:0x00000000




Last Coverpoint : ['rs1 : f22', 'rs2 : f21', 'rd : x22', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000244]:feq.h s6, fs6, fs5
	-[0x80000248]:csrrs tp, fcsr, zero
	-[0x8000024c]:sw s6, 72(ra)
Current Store : [0x80000250] : sw tp, 76(ra) -- Store: [0x80012360]:0x00000000




Last Coverpoint : ['rs1 : f21', 'rs2 : f22', 'rd : x21', 'fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000264]:feq.h s5, fs5, fs6
	-[0x80000268]:csrrs tp, fcsr, zero
	-[0x8000026c]:sw s5, 80(ra)
Current Store : [0x80000270] : sw tp, 84(ra) -- Store: [0x80012368]:0x00000000




Last Coverpoint : ['rs1 : f20', 'rs2 : f19', 'rd : x20', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000284]:feq.h s4, fs4, fs3
	-[0x80000288]:csrrs tp, fcsr, zero
	-[0x8000028c]:sw s4, 88(ra)
Current Store : [0x80000290] : sw tp, 92(ra) -- Store: [0x80012370]:0x00000000




Last Coverpoint : ['rs1 : f19', 'rs2 : f20', 'rd : x19', 'fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002a4]:feq.h s3, fs3, fs4
	-[0x800002a8]:csrrs tp, fcsr, zero
	-[0x800002ac]:sw s3, 96(ra)
Current Store : [0x800002b0] : sw tp, 100(ra) -- Store: [0x80012378]:0x00000000




Last Coverpoint : ['rs1 : f18', 'rs2 : f17', 'rd : x18', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002c4]:feq.h s2, fs2, fa7
	-[0x800002c8]:csrrs tp, fcsr, zero
	-[0x800002cc]:sw s2, 104(ra)
Current Store : [0x800002d0] : sw tp, 108(ra) -- Store: [0x80012380]:0x00000000




Last Coverpoint : ['rs1 : f17', 'rs2 : f18', 'rd : x17', 'fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002e4]:feq.h a7, fa7, fs2
	-[0x800002e8]:csrrs tp, fcsr, zero
	-[0x800002ec]:sw a7, 112(ra)
Current Store : [0x800002f0] : sw tp, 116(ra) -- Store: [0x80012388]:0x00000000




Last Coverpoint : ['rs1 : f16', 'rs2 : f15', 'rd : x16', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000304]:feq.h a6, fa6, fa5
	-[0x80000308]:csrrs tp, fcsr, zero
	-[0x8000030c]:sw a6, 120(ra)
Current Store : [0x80000310] : sw tp, 124(ra) -- Store: [0x80012390]:0x00000000




Last Coverpoint : ['rs1 : f15', 'rs2 : f16', 'rd : x15', 'fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000324]:feq.h a5, fa5, fa6
	-[0x80000328]:csrrs tp, fcsr, zero
	-[0x8000032c]:sw a5, 128(ra)
Current Store : [0x80000330] : sw tp, 132(ra) -- Store: [0x80012398]:0x00000000




Last Coverpoint : ['rs1 : f14', 'rs2 : f13', 'rd : x14', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000344]:feq.h a4, fa4, fa3
	-[0x80000348]:csrrs tp, fcsr, zero
	-[0x8000034c]:sw a4, 136(ra)
Current Store : [0x80000350] : sw tp, 140(ra) -- Store: [0x800123a0]:0x00000000




Last Coverpoint : ['rs1 : f13', 'rs2 : f14', 'rd : x13', 'fs1 == 0 and fe1 == 0x19 and fm1 == 0x216 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000364]:feq.h a3, fa3, fa4
	-[0x80000368]:csrrs tp, fcsr, zero
	-[0x8000036c]:sw a3, 144(ra)
Current Store : [0x80000370] : sw tp, 148(ra) -- Store: [0x800123a8]:0x00000000




Last Coverpoint : ['rs1 : f12', 'rs2 : f11', 'rd : x12', 'fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x19 and fm2 == 0x216 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000384]:feq.h a2, fa2, fa1
	-[0x80000388]:csrrs tp, fcsr, zero
	-[0x8000038c]:sw a2, 152(ra)
Current Store : [0x80000390] : sw tp, 156(ra) -- Store: [0x800123b0]:0x00000000




Last Coverpoint : ['rs1 : f11', 'rs2 : f12', 'rd : x11', 'fs1 == 0 and fe1 == 0x19 and fm1 == 0x216 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003a4]:feq.h a1, fa1, fa2
	-[0x800003a8]:csrrs tp, fcsr, zero
	-[0x800003ac]:sw a1, 160(ra)
Current Store : [0x800003b0] : sw tp, 164(ra) -- Store: [0x800123b8]:0x00000000




Last Coverpoint : ['rs1 : f10', 'rs2 : f9', 'rd : x10', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x19 and fm2 == 0x216 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003c4]:feq.h a0, fa0, fs1
	-[0x800003c8]:csrrs tp, fcsr, zero
	-[0x800003cc]:sw a0, 168(ra)
Current Store : [0x800003d0] : sw tp, 172(ra) -- Store: [0x800123c0]:0x00000000




Last Coverpoint : ['rs1 : f9', 'rs2 : f10', 'rd : x9', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003e4]:feq.h s1, fs1, fa0
	-[0x800003e8]:csrrs tp, fcsr, zero
	-[0x800003ec]:sw s1, 176(ra)
Current Store : [0x800003f0] : sw tp, 180(ra) -- Store: [0x800123c8]:0x00000000




Last Coverpoint : ['rs1 : f8', 'rs2 : f7', 'rd : x8', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000040c]:feq.h fp, fs0, ft7
	-[0x80000410]:csrrs a0, fcsr, zero
	-[0x80000414]:sw fp, 184(ra)
Current Store : [0x80000418] : sw a0, 188(ra) -- Store: [0x800123d0]:0x00000000




Last Coverpoint : ['rs1 : f7', 'rs2 : f8', 'rd : x7', 'fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000042c]:feq.h t2, ft7, fs0
	-[0x80000430]:csrrs a0, fcsr, zero
	-[0x80000434]:sw t2, 192(ra)
Current Store : [0x80000438] : sw a0, 196(ra) -- Store: [0x800123d8]:0x00000000




Last Coverpoint : ['rs1 : f6', 'rs2 : f5', 'rd : x6', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000044c]:feq.h t1, ft6, ft5
	-[0x80000450]:csrrs a0, fcsr, zero
	-[0x80000454]:sw t1, 200(ra)
Current Store : [0x80000458] : sw a0, 204(ra) -- Store: [0x800123e0]:0x00000000




Last Coverpoint : ['rs1 : f5', 'rs2 : f6', 'rd : x5', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000474]:feq.h t0, ft5, ft6
	-[0x80000478]:csrrs a0, fcsr, zero
	-[0x8000047c]:sw t0, 0(t1)
Current Store : [0x80000480] : sw a0, 4(t1) -- Store: [0x800123e8]:0x00000000




Last Coverpoint : ['rs1 : f4', 'rs2 : f3', 'rd : x4', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000494]:feq.h tp, ft4, ft3
	-[0x80000498]:csrrs a0, fcsr, zero
	-[0x8000049c]:sw tp, 8(t1)
Current Store : [0x800004a0] : sw a0, 12(t1) -- Store: [0x800123f0]:0x00000000




Last Coverpoint : ['rs1 : f3', 'rs2 : f4', 'rd : x3', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800004b4]:feq.h gp, ft3, ft4
	-[0x800004b8]:csrrs a0, fcsr, zero
	-[0x800004bc]:sw gp, 16(t1)
Current Store : [0x800004c0] : sw a0, 20(t1) -- Store: [0x800123f8]:0x00000000




Last Coverpoint : ['rs1 : f2', 'rs2 : f1', 'rd : x2', 'fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800004d4]:feq.h sp, ft2, ft1
	-[0x800004d8]:csrrs a0, fcsr, zero
	-[0x800004dc]:sw sp, 24(t1)
Current Store : [0x800004e0] : sw a0, 28(t1) -- Store: [0x80012400]:0x00000000




Last Coverpoint : ['rs1 : f1', 'rs2 : f2', 'rd : x1', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800004f4]:feq.h ra, ft1, ft2
	-[0x800004f8]:csrrs a0, fcsr, zero
	-[0x800004fc]:sw ra, 32(t1)
Current Store : [0x80000500] : sw a0, 36(t1) -- Store: [0x80012408]:0x00000000




Last Coverpoint : ['rs1 : f0', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000514]:feq.h t6, ft0, ft11
	-[0x80000518]:csrrs a0, fcsr, zero
	-[0x8000051c]:sw t6, 40(t1)
Current Store : [0x80000520] : sw a0, 44(t1) -- Store: [0x80012410]:0x00000000




Last Coverpoint : ['rs2 : f0', 'fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000534]:feq.h t6, ft11, ft0
	-[0x80000538]:csrrs a0, fcsr, zero
	-[0x8000053c]:sw t6, 48(t1)
Current Store : [0x80000540] : sw a0, 52(t1) -- Store: [0x80012418]:0x00000000




Last Coverpoint : ['rd : x0', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000554]:feq.h zero, ft11, ft10
	-[0x80000558]:csrrs a0, fcsr, zero
	-[0x8000055c]:sw zero, 56(t1)
Current Store : [0x80000560] : sw a0, 60(t1) -- Store: [0x80012420]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000574]:feq.h t6, ft11, ft10
	-[0x80000578]:csrrs a0, fcsr, zero
	-[0x8000057c]:sw t6, 64(t1)
Current Store : [0x80000580] : sw a0, 68(t1) -- Store: [0x80012428]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000594]:feq.h t6, ft11, ft10
	-[0x80000598]:csrrs a0, fcsr, zero
	-[0x8000059c]:sw t6, 72(t1)
Current Store : [0x800005a0] : sw a0, 76(t1) -- Store: [0x80012430]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800005b4]:feq.h t6, ft11, ft10
	-[0x800005b8]:csrrs a0, fcsr, zero
	-[0x800005bc]:sw t6, 80(t1)
Current Store : [0x800005c0] : sw a0, 84(t1) -- Store: [0x80012438]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800005d4]:feq.h t6, ft11, ft10
	-[0x800005d8]:csrrs a0, fcsr, zero
	-[0x800005dc]:sw t6, 88(t1)
Current Store : [0x800005e0] : sw a0, 92(t1) -- Store: [0x80012440]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800005f4]:feq.h t6, ft11, ft10
	-[0x800005f8]:csrrs a0, fcsr, zero
	-[0x800005fc]:sw t6, 96(t1)
Current Store : [0x80000600] : sw a0, 100(t1) -- Store: [0x80012448]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000614]:feq.h t6, ft11, ft10
	-[0x80000618]:csrrs a0, fcsr, zero
	-[0x8000061c]:sw t6, 104(t1)
Current Store : [0x80000620] : sw a0, 108(t1) -- Store: [0x80012450]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000634]:feq.h t6, ft11, ft10
	-[0x80000638]:csrrs a0, fcsr, zero
	-[0x8000063c]:sw t6, 112(t1)
Current Store : [0x80000640] : sw a0, 116(t1) -- Store: [0x80012458]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000654]:feq.h t6, ft11, ft10
	-[0x80000658]:csrrs a0, fcsr, zero
	-[0x8000065c]:sw t6, 120(t1)
Current Store : [0x80000660] : sw a0, 124(t1) -- Store: [0x80012460]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000674]:feq.h t6, ft11, ft10
	-[0x80000678]:csrrs a0, fcsr, zero
	-[0x8000067c]:sw t6, 128(t1)
Current Store : [0x80000680] : sw a0, 132(t1) -- Store: [0x80012468]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000694]:feq.h t6, ft11, ft10
	-[0x80000698]:csrrs a0, fcsr, zero
	-[0x8000069c]:sw t6, 136(t1)
Current Store : [0x800006a0] : sw a0, 140(t1) -- Store: [0x80012470]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006b4]:feq.h t6, ft11, ft10
	-[0x800006b8]:csrrs a0, fcsr, zero
	-[0x800006bc]:sw t6, 144(t1)
Current Store : [0x800006c0] : sw a0, 148(t1) -- Store: [0x80012478]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006d4]:feq.h t6, ft11, ft10
	-[0x800006d8]:csrrs a0, fcsr, zero
	-[0x800006dc]:sw t6, 152(t1)
Current Store : [0x800006e0] : sw a0, 156(t1) -- Store: [0x80012480]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006f4]:feq.h t6, ft11, ft10
	-[0x800006f8]:csrrs a0, fcsr, zero
	-[0x800006fc]:sw t6, 160(t1)
Current Store : [0x80000700] : sw a0, 164(t1) -- Store: [0x80012488]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000714]:feq.h t6, ft11, ft10
	-[0x80000718]:csrrs a0, fcsr, zero
	-[0x8000071c]:sw t6, 168(t1)
Current Store : [0x80000720] : sw a0, 172(t1) -- Store: [0x80012490]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000734]:feq.h t6, ft11, ft10
	-[0x80000738]:csrrs a0, fcsr, zero
	-[0x8000073c]:sw t6, 176(t1)
Current Store : [0x80000740] : sw a0, 180(t1) -- Store: [0x80012498]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x01a and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000754]:feq.h t6, ft11, ft10
	-[0x80000758]:csrrs a0, fcsr, zero
	-[0x8000075c]:sw t6, 184(t1)
Current Store : [0x80000760] : sw a0, 188(t1) -- Store: [0x800124a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x01a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000774]:feq.h t6, ft11, ft10
	-[0x80000778]:csrrs a0, fcsr, zero
	-[0x8000077c]:sw t6, 192(t1)
Current Store : [0x80000780] : sw a0, 196(t1) -- Store: [0x800124a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x01a and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000794]:feq.h t6, ft11, ft10
	-[0x80000798]:csrrs a0, fcsr, zero
	-[0x8000079c]:sw t6, 200(t1)
Current Store : [0x800007a0] : sw a0, 204(t1) -- Store: [0x800124b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x01a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007b4]:feq.h t6, ft11, ft10
	-[0x800007b8]:csrrs a0, fcsr, zero
	-[0x800007bc]:sw t6, 208(t1)
Current Store : [0x800007c0] : sw a0, 212(t1) -- Store: [0x800124b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007d4]:feq.h t6, ft11, ft10
	-[0x800007d8]:csrrs a0, fcsr, zero
	-[0x800007dc]:sw t6, 216(t1)
Current Store : [0x800007e0] : sw a0, 220(t1) -- Store: [0x800124c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007f4]:feq.h t6, ft11, ft10
	-[0x800007f8]:csrrs a0, fcsr, zero
	-[0x800007fc]:sw t6, 224(t1)
Current Store : [0x80000800] : sw a0, 228(t1) -- Store: [0x800124c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000814]:feq.h t6, ft11, ft10
	-[0x80000818]:csrrs a0, fcsr, zero
	-[0x8000081c]:sw t6, 232(t1)
Current Store : [0x80000820] : sw a0, 236(t1) -- Store: [0x800124d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000834]:feq.h t6, ft11, ft10
	-[0x80000838]:csrrs a0, fcsr, zero
	-[0x8000083c]:sw t6, 240(t1)
Current Store : [0x80000840] : sw a0, 244(t1) -- Store: [0x800124d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000854]:feq.h t6, ft11, ft10
	-[0x80000858]:csrrs a0, fcsr, zero
	-[0x8000085c]:sw t6, 248(t1)
Current Store : [0x80000860] : sw a0, 252(t1) -- Store: [0x800124e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000874]:feq.h t6, ft11, ft10
	-[0x80000878]:csrrs a0, fcsr, zero
	-[0x8000087c]:sw t6, 256(t1)
Current Store : [0x80000880] : sw a0, 260(t1) -- Store: [0x800124e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000894]:feq.h t6, ft11, ft10
	-[0x80000898]:csrrs a0, fcsr, zero
	-[0x8000089c]:sw t6, 264(t1)
Current Store : [0x800008a0] : sw a0, 268(t1) -- Store: [0x800124f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008b4]:feq.h t6, ft11, ft10
	-[0x800008b8]:csrrs a0, fcsr, zero
	-[0x800008bc]:sw t6, 272(t1)
Current Store : [0x800008c0] : sw a0, 276(t1) -- Store: [0x800124f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008d4]:feq.h t6, ft11, ft10
	-[0x800008d8]:csrrs a0, fcsr, zero
	-[0x800008dc]:sw t6, 280(t1)
Current Store : [0x800008e0] : sw a0, 284(t1) -- Store: [0x80012500]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008f4]:feq.h t6, ft11, ft10
	-[0x800008f8]:csrrs a0, fcsr, zero
	-[0x800008fc]:sw t6, 288(t1)
Current Store : [0x80000900] : sw a0, 292(t1) -- Store: [0x80012508]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000914]:feq.h t6, ft11, ft10
	-[0x80000918]:csrrs a0, fcsr, zero
	-[0x8000091c]:sw t6, 296(t1)
Current Store : [0x80000920] : sw a0, 300(t1) -- Store: [0x80012510]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000934]:feq.h t6, ft11, ft10
	-[0x80000938]:csrrs a0, fcsr, zero
	-[0x8000093c]:sw t6, 304(t1)
Current Store : [0x80000940] : sw a0, 308(t1) -- Store: [0x80012518]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000954]:feq.h t6, ft11, ft10
	-[0x80000958]:csrrs a0, fcsr, zero
	-[0x8000095c]:sw t6, 312(t1)
Current Store : [0x80000960] : sw a0, 316(t1) -- Store: [0x80012520]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x23c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000974]:feq.h t6, ft11, ft10
	-[0x80000978]:csrrs a0, fcsr, zero
	-[0x8000097c]:sw t6, 320(t1)
Current Store : [0x80000980] : sw a0, 324(t1) -- Store: [0x80012528]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x23c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000994]:feq.h t6, ft11, ft10
	-[0x80000998]:csrrs a0, fcsr, zero
	-[0x8000099c]:sw t6, 328(t1)
Current Store : [0x800009a0] : sw a0, 332(t1) -- Store: [0x80012530]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x0f and fm2 == 0x23c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800009b4]:feq.h t6, ft11, ft10
	-[0x800009b8]:csrrs a0, fcsr, zero
	-[0x800009bc]:sw t6, 336(t1)
Current Store : [0x800009c0] : sw a0, 340(t1) -- Store: [0x80012538]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800009d4]:feq.h t6, ft11, ft10
	-[0x800009d8]:csrrs a0, fcsr, zero
	-[0x800009dc]:sw t6, 344(t1)
Current Store : [0x800009e0] : sw a0, 348(t1) -- Store: [0x80012540]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800009f4]:feq.h t6, ft11, ft10
	-[0x800009f8]:csrrs a0, fcsr, zero
	-[0x800009fc]:sw t6, 352(t1)
Current Store : [0x80000a00] : sw a0, 356(t1) -- Store: [0x80012548]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a14]:feq.h t6, ft11, ft10
	-[0x80000a18]:csrrs a0, fcsr, zero
	-[0x80000a1c]:sw t6, 360(t1)
Current Store : [0x80000a20] : sw a0, 364(t1) -- Store: [0x80012550]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a34]:feq.h t6, ft11, ft10
	-[0x80000a38]:csrrs a0, fcsr, zero
	-[0x80000a3c]:sw t6, 368(t1)
Current Store : [0x80000a40] : sw a0, 372(t1) -- Store: [0x80012558]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a54]:feq.h t6, ft11, ft10
	-[0x80000a58]:csrrs a0, fcsr, zero
	-[0x80000a5c]:sw t6, 376(t1)
Current Store : [0x80000a60] : sw a0, 380(t1) -- Store: [0x80012560]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a74]:feq.h t6, ft11, ft10
	-[0x80000a78]:csrrs a0, fcsr, zero
	-[0x80000a7c]:sw t6, 384(t1)
Current Store : [0x80000a80] : sw a0, 388(t1) -- Store: [0x80012568]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a94]:feq.h t6, ft11, ft10
	-[0x80000a98]:csrrs a0, fcsr, zero
	-[0x80000a9c]:sw t6, 392(t1)
Current Store : [0x80000aa0] : sw a0, 396(t1) -- Store: [0x80012570]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ab4]:feq.h t6, ft11, ft10
	-[0x80000ab8]:csrrs a0, fcsr, zero
	-[0x80000abc]:sw t6, 400(t1)
Current Store : [0x80000ac0] : sw a0, 404(t1) -- Store: [0x80012578]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ad4]:feq.h t6, ft11, ft10
	-[0x80000ad8]:csrrs a0, fcsr, zero
	-[0x80000adc]:sw t6, 408(t1)
Current Store : [0x80000ae0] : sw a0, 412(t1) -- Store: [0x80012580]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000af4]:feq.h t6, ft11, ft10
	-[0x80000af8]:csrrs a0, fcsr, zero
	-[0x80000afc]:sw t6, 416(t1)
Current Store : [0x80000b00] : sw a0, 420(t1) -- Store: [0x80012588]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b14]:feq.h t6, ft11, ft10
	-[0x80000b18]:csrrs a0, fcsr, zero
	-[0x80000b1c]:sw t6, 424(t1)
Current Store : [0x80000b20] : sw a0, 428(t1) -- Store: [0x80012590]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b34]:feq.h t6, ft11, ft10
	-[0x80000b38]:csrrs a0, fcsr, zero
	-[0x80000b3c]:sw t6, 432(t1)
Current Store : [0x80000b40] : sw a0, 436(t1) -- Store: [0x80012598]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b54]:feq.h t6, ft11, ft10
	-[0x80000b58]:csrrs a0, fcsr, zero
	-[0x80000b5c]:sw t6, 440(t1)
Current Store : [0x80000b60] : sw a0, 444(t1) -- Store: [0x800125a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b74]:feq.h t6, ft11, ft10
	-[0x80000b78]:csrrs a0, fcsr, zero
	-[0x80000b7c]:sw t6, 448(t1)
Current Store : [0x80000b80] : sw a0, 452(t1) -- Store: [0x800125a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b94]:feq.h t6, ft11, ft10
	-[0x80000b98]:csrrs a0, fcsr, zero
	-[0x80000b9c]:sw t6, 456(t1)
Current Store : [0x80000ba0] : sw a0, 460(t1) -- Store: [0x800125b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000bb4]:feq.h t6, ft11, ft10
	-[0x80000bb8]:csrrs a0, fcsr, zero
	-[0x80000bbc]:sw t6, 464(t1)
Current Store : [0x80000bc0] : sw a0, 468(t1) -- Store: [0x800125b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1b and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000bd4]:feq.h t6, ft11, ft10
	-[0x80000bd8]:csrrs a0, fcsr, zero
	-[0x80000bdc]:sw t6, 472(t1)
Current Store : [0x80000be0] : sw a0, 476(t1) -- Store: [0x800125c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1b and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000bf4]:feq.h t6, ft11, ft10
	-[0x80000bf8]:csrrs a0, fcsr, zero
	-[0x80000bfc]:sw t6, 480(t1)
Current Store : [0x80000c00] : sw a0, 484(t1) -- Store: [0x800125c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1b and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c14]:feq.h t6, ft11, ft10
	-[0x80000c18]:csrrs a0, fcsr, zero
	-[0x80000c1c]:sw t6, 488(t1)
Current Store : [0x80000c20] : sw a0, 492(t1) -- Store: [0x800125d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1b and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c34]:feq.h t6, ft11, ft10
	-[0x80000c38]:csrrs a0, fcsr, zero
	-[0x80000c3c]:sw t6, 496(t1)
Current Store : [0x80000c40] : sw a0, 500(t1) -- Store: [0x800125d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c54]:feq.h t6, ft11, ft10
	-[0x80000c58]:csrrs a0, fcsr, zero
	-[0x80000c5c]:sw t6, 504(t1)
Current Store : [0x80000c60] : sw a0, 508(t1) -- Store: [0x800125e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c74]:feq.h t6, ft11, ft10
	-[0x80000c78]:csrrs a0, fcsr, zero
	-[0x80000c7c]:sw t6, 512(t1)
Current Store : [0x80000c80] : sw a0, 516(t1) -- Store: [0x800125e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c94]:feq.h t6, ft11, ft10
	-[0x80000c98]:csrrs a0, fcsr, zero
	-[0x80000c9c]:sw t6, 520(t1)
Current Store : [0x80000ca0] : sw a0, 524(t1) -- Store: [0x800125f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000cb4]:feq.h t6, ft11, ft10
	-[0x80000cb8]:csrrs a0, fcsr, zero
	-[0x80000cbc]:sw t6, 528(t1)
Current Store : [0x80000cc0] : sw a0, 532(t1) -- Store: [0x800125f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000cd4]:feq.h t6, ft11, ft10
	-[0x80000cd8]:csrrs a0, fcsr, zero
	-[0x80000cdc]:sw t6, 536(t1)
Current Store : [0x80000ce0] : sw a0, 540(t1) -- Store: [0x80012600]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000cf4]:feq.h t6, ft11, ft10
	-[0x80000cf8]:csrrs a0, fcsr, zero
	-[0x80000cfc]:sw t6, 544(t1)
Current Store : [0x80000d00] : sw a0, 548(t1) -- Store: [0x80012608]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x006 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d14]:feq.h t6, ft11, ft10
	-[0x80000d18]:csrrs a0, fcsr, zero
	-[0x80000d1c]:sw t6, 552(t1)
Current Store : [0x80000d20] : sw a0, 556(t1) -- Store: [0x80012610]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d34]:feq.h t6, ft11, ft10
	-[0x80000d38]:csrrs a0, fcsr, zero
	-[0x80000d3c]:sw t6, 560(t1)
Current Store : [0x80000d40] : sw a0, 564(t1) -- Store: [0x80012618]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x006 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d54]:feq.h t6, ft11, ft10
	-[0x80000d58]:csrrs a0, fcsr, zero
	-[0x80000d5c]:sw t6, 568(t1)
Current Store : [0x80000d60] : sw a0, 572(t1) -- Store: [0x80012620]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d74]:feq.h t6, ft11, ft10
	-[0x80000d78]:csrrs a0, fcsr, zero
	-[0x80000d7c]:sw t6, 576(t1)
Current Store : [0x80000d80] : sw a0, 580(t1) -- Store: [0x80012628]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d94]:feq.h t6, ft11, ft10
	-[0x80000d98]:csrrs a0, fcsr, zero
	-[0x80000d9c]:sw t6, 584(t1)
Current Store : [0x80000da0] : sw a0, 588(t1) -- Store: [0x80012630]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000db4]:feq.h t6, ft11, ft10
	-[0x80000db8]:csrrs a0, fcsr, zero
	-[0x80000dbc]:sw t6, 592(t1)
Current Store : [0x80000dc0] : sw a0, 596(t1) -- Store: [0x80012638]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000dd4]:feq.h t6, ft11, ft10
	-[0x80000dd8]:csrrs a0, fcsr, zero
	-[0x80000ddc]:sw t6, 600(t1)
Current Store : [0x80000de0] : sw a0, 604(t1) -- Store: [0x80012640]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000df4]:feq.h t6, ft11, ft10
	-[0x80000df8]:csrrs a0, fcsr, zero
	-[0x80000dfc]:sw t6, 608(t1)
Current Store : [0x80000e00] : sw a0, 612(t1) -- Store: [0x80012648]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e14]:feq.h t6, ft11, ft10
	-[0x80000e18]:csrrs a0, fcsr, zero
	-[0x80000e1c]:sw t6, 616(t1)
Current Store : [0x80000e20] : sw a0, 620(t1) -- Store: [0x80012650]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e34]:feq.h t6, ft11, ft10
	-[0x80000e38]:csrrs a0, fcsr, zero
	-[0x80000e3c]:sw t6, 624(t1)
Current Store : [0x80000e40] : sw a0, 628(t1) -- Store: [0x80012658]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e54]:feq.h t6, ft11, ft10
	-[0x80000e58]:csrrs a0, fcsr, zero
	-[0x80000e5c]:sw t6, 632(t1)
Current Store : [0x80000e60] : sw a0, 636(t1) -- Store: [0x80012660]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e74]:feq.h t6, ft11, ft10
	-[0x80000e78]:csrrs a0, fcsr, zero
	-[0x80000e7c]:sw t6, 640(t1)
Current Store : [0x80000e80] : sw a0, 644(t1) -- Store: [0x80012668]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e94]:feq.h t6, ft11, ft10
	-[0x80000e98]:csrrs a0, fcsr, zero
	-[0x80000e9c]:sw t6, 648(t1)
Current Store : [0x80000ea0] : sw a0, 652(t1) -- Store: [0x80012670]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000eb4]:feq.h t6, ft11, ft10
	-[0x80000eb8]:csrrs a0, fcsr, zero
	-[0x80000ebc]:sw t6, 656(t1)
Current Store : [0x80000ec0] : sw a0, 660(t1) -- Store: [0x80012678]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ed4]:feq.h t6, ft11, ft10
	-[0x80000ed8]:csrrs a0, fcsr, zero
	-[0x80000edc]:sw t6, 664(t1)
Current Store : [0x80000ee0] : sw a0, 668(t1) -- Store: [0x80012680]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ef4]:feq.h t6, ft11, ft10
	-[0x80000ef8]:csrrs a0, fcsr, zero
	-[0x80000efc]:sw t6, 672(t1)
Current Store : [0x80000f00] : sw a0, 676(t1) -- Store: [0x80012688]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f14]:feq.h t6, ft11, ft10
	-[0x80000f18]:csrrs a0, fcsr, zero
	-[0x80000f1c]:sw t6, 680(t1)
Current Store : [0x80000f20] : sw a0, 684(t1) -- Store: [0x80012690]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f34]:feq.h t6, ft11, ft10
	-[0x80000f38]:csrrs a0, fcsr, zero
	-[0x80000f3c]:sw t6, 688(t1)
Current Store : [0x80000f40] : sw a0, 692(t1) -- Store: [0x80012698]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f54]:feq.h t6, ft11, ft10
	-[0x80000f58]:csrrs a0, fcsr, zero
	-[0x80000f5c]:sw t6, 696(t1)
Current Store : [0x80000f60] : sw a0, 700(t1) -- Store: [0x800126a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f74]:feq.h t6, ft11, ft10
	-[0x80000f78]:csrrs a0, fcsr, zero
	-[0x80000f7c]:sw t6, 704(t1)
Current Store : [0x80000f80] : sw a0, 708(t1) -- Store: [0x800126a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f94]:feq.h t6, ft11, ft10
	-[0x80000f98]:csrrs a0, fcsr, zero
	-[0x80000f9c]:sw t6, 712(t1)
Current Store : [0x80000fa0] : sw a0, 716(t1) -- Store: [0x800126b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x044 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000fb4]:feq.h t6, ft11, ft10
	-[0x80000fb8]:csrrs a0, fcsr, zero
	-[0x80000fbc]:sw t6, 720(t1)
Current Store : [0x80000fc0] : sw a0, 724(t1) -- Store: [0x800126b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x044 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000fd4]:feq.h t6, ft11, ft10
	-[0x80000fd8]:csrrs a0, fcsr, zero
	-[0x80000fdc]:sw t6, 728(t1)
Current Store : [0x80000fe0] : sw a0, 732(t1) -- Store: [0x800126c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x044 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ff4]:feq.h t6, ft11, ft10
	-[0x80000ff8]:csrrs a0, fcsr, zero
	-[0x80000ffc]:sw t6, 736(t1)
Current Store : [0x80001000] : sw a0, 740(t1) -- Store: [0x800126c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x044 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001014]:feq.h t6, ft11, ft10
	-[0x80001018]:csrrs a0, fcsr, zero
	-[0x8000101c]:sw t6, 744(t1)
Current Store : [0x80001020] : sw a0, 748(t1) -- Store: [0x800126d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001034]:feq.h t6, ft11, ft10
	-[0x80001038]:csrrs a0, fcsr, zero
	-[0x8000103c]:sw t6, 752(t1)
Current Store : [0x80001040] : sw a0, 756(t1) -- Store: [0x800126d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001054]:feq.h t6, ft11, ft10
	-[0x80001058]:csrrs a0, fcsr, zero
	-[0x8000105c]:sw t6, 760(t1)
Current Store : [0x80001060] : sw a0, 764(t1) -- Store: [0x800126e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001074]:feq.h t6, ft11, ft10
	-[0x80001078]:csrrs a0, fcsr, zero
	-[0x8000107c]:sw t6, 768(t1)
Current Store : [0x80001080] : sw a0, 772(t1) -- Store: [0x800126e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001094]:feq.h t6, ft11, ft10
	-[0x80001098]:csrrs a0, fcsr, zero
	-[0x8000109c]:sw t6, 776(t1)
Current Store : [0x800010a0] : sw a0, 780(t1) -- Store: [0x800126f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800010b4]:feq.h t6, ft11, ft10
	-[0x800010b8]:csrrs a0, fcsr, zero
	-[0x800010bc]:sw t6, 784(t1)
Current Store : [0x800010c0] : sw a0, 788(t1) -- Store: [0x800126f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800010d4]:feq.h t6, ft11, ft10
	-[0x800010d8]:csrrs a0, fcsr, zero
	-[0x800010dc]:sw t6, 792(t1)
Current Store : [0x800010e0] : sw a0, 796(t1) -- Store: [0x80012700]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800010f4]:feq.h t6, ft11, ft10
	-[0x800010f8]:csrrs a0, fcsr, zero
	-[0x800010fc]:sw t6, 800(t1)
Current Store : [0x80001100] : sw a0, 804(t1) -- Store: [0x80012708]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001114]:feq.h t6, ft11, ft10
	-[0x80001118]:csrrs a0, fcsr, zero
	-[0x8000111c]:sw t6, 808(t1)
Current Store : [0x80001120] : sw a0, 812(t1) -- Store: [0x80012710]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001134]:feq.h t6, ft11, ft10
	-[0x80001138]:csrrs a0, fcsr, zero
	-[0x8000113c]:sw t6, 816(t1)
Current Store : [0x80001140] : sw a0, 820(t1) -- Store: [0x80012718]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001154]:feq.h t6, ft11, ft10
	-[0x80001158]:csrrs a0, fcsr, zero
	-[0x8000115c]:sw t6, 824(t1)
Current Store : [0x80001160] : sw a0, 828(t1) -- Store: [0x80012720]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001174]:feq.h t6, ft11, ft10
	-[0x80001178]:csrrs a0, fcsr, zero
	-[0x8000117c]:sw t6, 832(t1)
Current Store : [0x80001180] : sw a0, 836(t1) -- Store: [0x80012728]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001194]:feq.h t6, ft11, ft10
	-[0x80001198]:csrrs a0, fcsr, zero
	-[0x8000119c]:sw t6, 840(t1)
Current Store : [0x800011a0] : sw a0, 844(t1) -- Store: [0x80012730]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800011b4]:feq.h t6, ft11, ft10
	-[0x800011b8]:csrrs a0, fcsr, zero
	-[0x800011bc]:sw t6, 848(t1)
Current Store : [0x800011c0] : sw a0, 852(t1) -- Store: [0x80012738]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x11 and fm1 == 0x019 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800011d4]:feq.h t6, ft11, ft10
	-[0x800011d8]:csrrs a0, fcsr, zero
	-[0x800011dc]:sw t6, 856(t1)
Current Store : [0x800011e0] : sw a0, 860(t1) -- Store: [0x80012740]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x019 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800011f4]:feq.h t6, ft11, ft10
	-[0x800011f8]:csrrs a0, fcsr, zero
	-[0x800011fc]:sw t6, 864(t1)
Current Store : [0x80001200] : sw a0, 868(t1) -- Store: [0x80012748]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x019 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001214]:feq.h t6, ft11, ft10
	-[0x80001218]:csrrs a0, fcsr, zero
	-[0x8000121c]:sw t6, 872(t1)
Current Store : [0x80001220] : sw a0, 876(t1) -- Store: [0x80012750]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001234]:feq.h t6, ft11, ft10
	-[0x80001238]:csrrs a0, fcsr, zero
	-[0x8000123c]:sw t6, 880(t1)
Current Store : [0x80001240] : sw a0, 884(t1) -- Store: [0x80012758]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001254]:feq.h t6, ft11, ft10
	-[0x80001258]:csrrs a0, fcsr, zero
	-[0x8000125c]:sw t6, 888(t1)
Current Store : [0x80001260] : sw a0, 892(t1) -- Store: [0x80012760]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001274]:feq.h t6, ft11, ft10
	-[0x80001278]:csrrs a0, fcsr, zero
	-[0x8000127c]:sw t6, 896(t1)
Current Store : [0x80001280] : sw a0, 900(t1) -- Store: [0x80012768]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001294]:feq.h t6, ft11, ft10
	-[0x80001298]:csrrs a0, fcsr, zero
	-[0x8000129c]:sw t6, 904(t1)
Current Store : [0x800012a0] : sw a0, 908(t1) -- Store: [0x80012770]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800012b4]:feq.h t6, ft11, ft10
	-[0x800012b8]:csrrs a0, fcsr, zero
	-[0x800012bc]:sw t6, 912(t1)
Current Store : [0x800012c0] : sw a0, 916(t1) -- Store: [0x80012778]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800012d4]:feq.h t6, ft11, ft10
	-[0x800012d8]:csrrs a0, fcsr, zero
	-[0x800012dc]:sw t6, 920(t1)
Current Store : [0x800012e0] : sw a0, 924(t1) -- Store: [0x80012780]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800012f4]:feq.h t6, ft11, ft10
	-[0x800012f8]:csrrs a0, fcsr, zero
	-[0x800012fc]:sw t6, 928(t1)
Current Store : [0x80001300] : sw a0, 932(t1) -- Store: [0x80012788]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001314]:feq.h t6, ft11, ft10
	-[0x80001318]:csrrs a0, fcsr, zero
	-[0x8000131c]:sw t6, 936(t1)
Current Store : [0x80001320] : sw a0, 940(t1) -- Store: [0x80012790]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001334]:feq.h t6, ft11, ft10
	-[0x80001338]:csrrs a0, fcsr, zero
	-[0x8000133c]:sw t6, 944(t1)
Current Store : [0x80001340] : sw a0, 948(t1) -- Store: [0x80012798]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001354]:feq.h t6, ft11, ft10
	-[0x80001358]:csrrs a0, fcsr, zero
	-[0x8000135c]:sw t6, 952(t1)
Current Store : [0x80001360] : sw a0, 956(t1) -- Store: [0x800127a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001374]:feq.h t6, ft11, ft10
	-[0x80001378]:csrrs a0, fcsr, zero
	-[0x8000137c]:sw t6, 960(t1)
Current Store : [0x80001380] : sw a0, 964(t1) -- Store: [0x800127a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001394]:feq.h t6, ft11, ft10
	-[0x80001398]:csrrs a0, fcsr, zero
	-[0x8000139c]:sw t6, 968(t1)
Current Store : [0x800013a0] : sw a0, 972(t1) -- Store: [0x800127b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800013b4]:feq.h t6, ft11, ft10
	-[0x800013b8]:csrrs a0, fcsr, zero
	-[0x800013bc]:sw t6, 976(t1)
Current Store : [0x800013c0] : sw a0, 980(t1) -- Store: [0x800127b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800013d4]:feq.h t6, ft11, ft10
	-[0x800013d8]:csrrs a0, fcsr, zero
	-[0x800013dc]:sw t6, 984(t1)
Current Store : [0x800013e0] : sw a0, 988(t1) -- Store: [0x800127c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x19 and fm1 == 0x2a2 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800013f4]:feq.h t6, ft11, ft10
	-[0x800013f8]:csrrs a0, fcsr, zero
	-[0x800013fc]:sw t6, 992(t1)
Current Store : [0x80001400] : sw a0, 996(t1) -- Store: [0x800127c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x19 and fm2 == 0x2a2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001414]:feq.h t6, ft11, ft10
	-[0x80001418]:csrrs a0, fcsr, zero
	-[0x8000141c]:sw t6, 1000(t1)
Current Store : [0x80001420] : sw a0, 1004(t1) -- Store: [0x800127d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x19 and fm1 == 0x2a2 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001434]:feq.h t6, ft11, ft10
	-[0x80001438]:csrrs a0, fcsr, zero
	-[0x8000143c]:sw t6, 1008(t1)
Current Store : [0x80001440] : sw a0, 1012(t1) -- Store: [0x800127d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x19 and fm2 == 0x2a2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001454]:feq.h t6, ft11, ft10
	-[0x80001458]:csrrs a0, fcsr, zero
	-[0x8000145c]:sw t6, 1016(t1)
Current Store : [0x80001460] : sw a0, 1020(t1) -- Store: [0x800127e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000147c]:feq.h t6, ft11, ft10
	-[0x80001480]:csrrs a0, fcsr, zero
	-[0x80001484]:sw t6, 0(t1)
Current Store : [0x80001488] : sw a0, 4(t1) -- Store: [0x800127e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000149c]:feq.h t6, ft11, ft10
	-[0x800014a0]:csrrs a0, fcsr, zero
	-[0x800014a4]:sw t6, 8(t1)
Current Store : [0x800014a8] : sw a0, 12(t1) -- Store: [0x800127f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800014bc]:feq.h t6, ft11, ft10
	-[0x800014c0]:csrrs a0, fcsr, zero
	-[0x800014c4]:sw t6, 16(t1)
Current Store : [0x800014c8] : sw a0, 20(t1) -- Store: [0x800127f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800014dc]:feq.h t6, ft11, ft10
	-[0x800014e0]:csrrs a0, fcsr, zero
	-[0x800014e4]:sw t6, 24(t1)
Current Store : [0x800014e8] : sw a0, 28(t1) -- Store: [0x80012800]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800014fc]:feq.h t6, ft11, ft10
	-[0x80001500]:csrrs a0, fcsr, zero
	-[0x80001504]:sw t6, 32(t1)
Current Store : [0x80001508] : sw a0, 36(t1) -- Store: [0x80012808]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000151c]:feq.h t6, ft11, ft10
	-[0x80001520]:csrrs a0, fcsr, zero
	-[0x80001524]:sw t6, 40(t1)
Current Store : [0x80001528] : sw a0, 44(t1) -- Store: [0x80012810]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000153c]:feq.h t6, ft11, ft10
	-[0x80001540]:csrrs a0, fcsr, zero
	-[0x80001544]:sw t6, 48(t1)
Current Store : [0x80001548] : sw a0, 52(t1) -- Store: [0x80012818]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000155c]:feq.h t6, ft11, ft10
	-[0x80001560]:csrrs a0, fcsr, zero
	-[0x80001564]:sw t6, 56(t1)
Current Store : [0x80001568] : sw a0, 60(t1) -- Store: [0x80012820]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000157c]:feq.h t6, ft11, ft10
	-[0x80001580]:csrrs a0, fcsr, zero
	-[0x80001584]:sw t6, 64(t1)
Current Store : [0x80001588] : sw a0, 68(t1) -- Store: [0x80012828]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000159c]:feq.h t6, ft11, ft10
	-[0x800015a0]:csrrs a0, fcsr, zero
	-[0x800015a4]:sw t6, 72(t1)
Current Store : [0x800015a8] : sw a0, 76(t1) -- Store: [0x80012830]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800015bc]:feq.h t6, ft11, ft10
	-[0x800015c0]:csrrs a0, fcsr, zero
	-[0x800015c4]:sw t6, 80(t1)
Current Store : [0x800015c8] : sw a0, 84(t1) -- Store: [0x80012838]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800015dc]:feq.h t6, ft11, ft10
	-[0x800015e0]:csrrs a0, fcsr, zero
	-[0x800015e4]:sw t6, 88(t1)
Current Store : [0x800015e8] : sw a0, 92(t1) -- Store: [0x80012840]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800015fc]:feq.h t6, ft11, ft10
	-[0x80001600]:csrrs a0, fcsr, zero
	-[0x80001604]:sw t6, 96(t1)
Current Store : [0x80001608] : sw a0, 100(t1) -- Store: [0x80012848]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000161c]:feq.h t6, ft11, ft10
	-[0x80001620]:csrrs a0, fcsr, zero
	-[0x80001624]:sw t6, 104(t1)
Current Store : [0x80001628] : sw a0, 108(t1) -- Store: [0x80012850]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000163c]:feq.h t6, ft11, ft10
	-[0x80001640]:csrrs a0, fcsr, zero
	-[0x80001644]:sw t6, 112(t1)
Current Store : [0x80001648] : sw a0, 116(t1) -- Store: [0x80012858]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000165c]:feq.h t6, ft11, ft10
	-[0x80001660]:csrrs a0, fcsr, zero
	-[0x80001664]:sw t6, 120(t1)
Current Store : [0x80001668] : sw a0, 124(t1) -- Store: [0x80012860]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000167c]:feq.h t6, ft11, ft10
	-[0x80001680]:csrrs a0, fcsr, zero
	-[0x80001684]:sw t6, 128(t1)
Current Store : [0x80001688] : sw a0, 132(t1) -- Store: [0x80012868]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000169c]:feq.h t6, ft11, ft10
	-[0x800016a0]:csrrs a0, fcsr, zero
	-[0x800016a4]:sw t6, 136(t1)
Current Store : [0x800016a8] : sw a0, 140(t1) -- Store: [0x80012870]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800016bc]:feq.h t6, ft11, ft10
	-[0x800016c0]:csrrs a0, fcsr, zero
	-[0x800016c4]:sw t6, 144(t1)
Current Store : [0x800016c8] : sw a0, 148(t1) -- Store: [0x80012878]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800016dc]:feq.h t6, ft11, ft10
	-[0x800016e0]:csrrs a0, fcsr, zero
	-[0x800016e4]:sw t6, 152(t1)
Current Store : [0x800016e8] : sw a0, 156(t1) -- Store: [0x80012880]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800016fc]:feq.h t6, ft11, ft10
	-[0x80001700]:csrrs a0, fcsr, zero
	-[0x80001704]:sw t6, 160(t1)
Current Store : [0x80001708] : sw a0, 164(t1) -- Store: [0x80012888]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000171c]:feq.h t6, ft11, ft10
	-[0x80001720]:csrrs a0, fcsr, zero
	-[0x80001724]:sw t6, 168(t1)
Current Store : [0x80001728] : sw a0, 172(t1) -- Store: [0x80012890]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000173c]:feq.h t6, ft11, ft10
	-[0x80001740]:csrrs a0, fcsr, zero
	-[0x80001744]:sw t6, 176(t1)
Current Store : [0x80001748] : sw a0, 180(t1) -- Store: [0x80012898]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000175c]:feq.h t6, ft11, ft10
	-[0x80001760]:csrrs a0, fcsr, zero
	-[0x80001764]:sw t6, 184(t1)
Current Store : [0x80001768] : sw a0, 188(t1) -- Store: [0x800128a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x01c and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000177c]:feq.h t6, ft11, ft10
	-[0x80001780]:csrrs a0, fcsr, zero
	-[0x80001784]:sw t6, 192(t1)
Current Store : [0x80001788] : sw a0, 196(t1) -- Store: [0x800128a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x01c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000179c]:feq.h t6, ft11, ft10
	-[0x800017a0]:csrrs a0, fcsr, zero
	-[0x800017a4]:sw t6, 200(t1)
Current Store : [0x800017a8] : sw a0, 204(t1) -- Store: [0x800128b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x01c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800017bc]:feq.h t6, ft11, ft10
	-[0x800017c0]:csrrs a0, fcsr, zero
	-[0x800017c4]:sw t6, 208(t1)
Current Store : [0x800017c8] : sw a0, 212(t1) -- Store: [0x800128b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x01c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800017dc]:feq.h t6, ft11, ft10
	-[0x800017e0]:csrrs a0, fcsr, zero
	-[0x800017e4]:sw t6, 216(t1)
Current Store : [0x800017e8] : sw a0, 220(t1) -- Store: [0x800128c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800017fc]:feq.h t6, ft11, ft10
	-[0x80001800]:csrrs a0, fcsr, zero
	-[0x80001804]:sw t6, 224(t1)
Current Store : [0x80001808] : sw a0, 228(t1) -- Store: [0x800128c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000181c]:feq.h t6, ft11, ft10
	-[0x80001820]:csrrs a0, fcsr, zero
	-[0x80001824]:sw t6, 232(t1)
Current Store : [0x80001828] : sw a0, 236(t1) -- Store: [0x800128d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000183c]:feq.h t6, ft11, ft10
	-[0x80001840]:csrrs a0, fcsr, zero
	-[0x80001844]:sw t6, 240(t1)
Current Store : [0x80001848] : sw a0, 244(t1) -- Store: [0x800128d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000185c]:feq.h t6, ft11, ft10
	-[0x80001860]:csrrs a0, fcsr, zero
	-[0x80001864]:sw t6, 248(t1)
Current Store : [0x80001868] : sw a0, 252(t1) -- Store: [0x800128e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000187c]:feq.h t6, ft11, ft10
	-[0x80001880]:csrrs a0, fcsr, zero
	-[0x80001884]:sw t6, 256(t1)
Current Store : [0x80001888] : sw a0, 260(t1) -- Store: [0x800128e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000189c]:feq.h t6, ft11, ft10
	-[0x800018a0]:csrrs a0, fcsr, zero
	-[0x800018a4]:sw t6, 264(t1)
Current Store : [0x800018a8] : sw a0, 268(t1) -- Store: [0x800128f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800018bc]:feq.h t6, ft11, ft10
	-[0x800018c0]:csrrs a0, fcsr, zero
	-[0x800018c4]:sw t6, 272(t1)
Current Store : [0x800018c8] : sw a0, 276(t1) -- Store: [0x800128f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800018dc]:feq.h t6, ft11, ft10
	-[0x800018e0]:csrrs a0, fcsr, zero
	-[0x800018e4]:sw t6, 280(t1)
Current Store : [0x800018e8] : sw a0, 284(t1) -- Store: [0x80012900]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800018fc]:feq.h t6, ft11, ft10
	-[0x80001900]:csrrs a0, fcsr, zero
	-[0x80001904]:sw t6, 288(t1)
Current Store : [0x80001908] : sw a0, 292(t1) -- Store: [0x80012908]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000191c]:feq.h t6, ft11, ft10
	-[0x80001920]:csrrs a0, fcsr, zero
	-[0x80001924]:sw t6, 296(t1)
Current Store : [0x80001928] : sw a0, 300(t1) -- Store: [0x80012910]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000193c]:feq.h t6, ft11, ft10
	-[0x80001940]:csrrs a0, fcsr, zero
	-[0x80001944]:sw t6, 304(t1)
Current Store : [0x80001948] : sw a0, 308(t1) -- Store: [0x80012918]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000195c]:feq.h t6, ft11, ft10
	-[0x80001960]:csrrs a0, fcsr, zero
	-[0x80001964]:sw t6, 312(t1)
Current Store : [0x80001968] : sw a0, 316(t1) -- Store: [0x80012920]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000197c]:feq.h t6, ft11, ft10
	-[0x80001980]:csrrs a0, fcsr, zero
	-[0x80001984]:sw t6, 320(t1)
Current Store : [0x80001988] : sw a0, 324(t1) -- Store: [0x80012928]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x2cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000199c]:feq.h t6, ft11, ft10
	-[0x800019a0]:csrrs a0, fcsr, zero
	-[0x800019a4]:sw t6, 328(t1)
Current Store : [0x800019a8] : sw a0, 332(t1) -- Store: [0x80012930]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x2cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800019bc]:feq.h t6, ft11, ft10
	-[0x800019c0]:csrrs a0, fcsr, zero
	-[0x800019c4]:sw t6, 336(t1)
Current Store : [0x800019c8] : sw a0, 340(t1) -- Store: [0x80012938]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x2cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800019dc]:feq.h t6, ft11, ft10
	-[0x800019e0]:csrrs a0, fcsr, zero
	-[0x800019e4]:sw t6, 344(t1)
Current Store : [0x800019e8] : sw a0, 348(t1) -- Store: [0x80012940]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800019fc]:feq.h t6, ft11, ft10
	-[0x80001a00]:csrrs a0, fcsr, zero
	-[0x80001a04]:sw t6, 352(t1)
Current Store : [0x80001a08] : sw a0, 356(t1) -- Store: [0x80012948]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a1c]:feq.h t6, ft11, ft10
	-[0x80001a20]:csrrs a0, fcsr, zero
	-[0x80001a24]:sw t6, 360(t1)
Current Store : [0x80001a28] : sw a0, 364(t1) -- Store: [0x80012950]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a3c]:feq.h t6, ft11, ft10
	-[0x80001a40]:csrrs a0, fcsr, zero
	-[0x80001a44]:sw t6, 368(t1)
Current Store : [0x80001a48] : sw a0, 372(t1) -- Store: [0x80012958]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a5c]:feq.h t6, ft11, ft10
	-[0x80001a60]:csrrs a0, fcsr, zero
	-[0x80001a64]:sw t6, 376(t1)
Current Store : [0x80001a68] : sw a0, 380(t1) -- Store: [0x80012960]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a7c]:feq.h t6, ft11, ft10
	-[0x80001a80]:csrrs a0, fcsr, zero
	-[0x80001a84]:sw t6, 384(t1)
Current Store : [0x80001a88] : sw a0, 388(t1) -- Store: [0x80012968]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a9c]:feq.h t6, ft11, ft10
	-[0x80001aa0]:csrrs a0, fcsr, zero
	-[0x80001aa4]:sw t6, 392(t1)
Current Store : [0x80001aa8] : sw a0, 396(t1) -- Store: [0x80012970]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001abc]:feq.h t6, ft11, ft10
	-[0x80001ac0]:csrrs a0, fcsr, zero
	-[0x80001ac4]:sw t6, 400(t1)
Current Store : [0x80001ac8] : sw a0, 404(t1) -- Store: [0x80012978]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001adc]:feq.h t6, ft11, ft10
	-[0x80001ae0]:csrrs a0, fcsr, zero
	-[0x80001ae4]:sw t6, 408(t1)
Current Store : [0x80001ae8] : sw a0, 412(t1) -- Store: [0x80012980]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001afc]:feq.h t6, ft11, ft10
	-[0x80001b00]:csrrs a0, fcsr, zero
	-[0x80001b04]:sw t6, 416(t1)
Current Store : [0x80001b08] : sw a0, 420(t1) -- Store: [0x80012988]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b1c]:feq.h t6, ft11, ft10
	-[0x80001b20]:csrrs a0, fcsr, zero
	-[0x80001b24]:sw t6, 424(t1)
Current Store : [0x80001b28] : sw a0, 428(t1) -- Store: [0x80012990]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b3c]:feq.h t6, ft11, ft10
	-[0x80001b40]:csrrs a0, fcsr, zero
	-[0x80001b44]:sw t6, 432(t1)
Current Store : [0x80001b48] : sw a0, 436(t1) -- Store: [0x80012998]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b5c]:feq.h t6, ft11, ft10
	-[0x80001b60]:csrrs a0, fcsr, zero
	-[0x80001b64]:sw t6, 440(t1)
Current Store : [0x80001b68] : sw a0, 444(t1) -- Store: [0x800129a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1b and fm1 == 0x159 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b7c]:feq.h t6, ft11, ft10
	-[0x80001b80]:csrrs a0, fcsr, zero
	-[0x80001b84]:sw t6, 448(t1)
Current Store : [0x80001b88] : sw a0, 452(t1) -- Store: [0x800129a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1b and fm2 == 0x159 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b9c]:feq.h t6, ft11, ft10
	-[0x80001ba0]:csrrs a0, fcsr, zero
	-[0x80001ba4]:sw t6, 456(t1)
Current Store : [0x80001ba8] : sw a0, 460(t1) -- Store: [0x800129b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1b and fm1 == 0x159 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001bbc]:feq.h t6, ft11, ft10
	-[0x80001bc0]:csrrs a0, fcsr, zero
	-[0x80001bc4]:sw t6, 464(t1)
Current Store : [0x80001bc8] : sw a0, 468(t1) -- Store: [0x800129b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1b and fm2 == 0x159 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001bdc]:feq.h t6, ft11, ft10
	-[0x80001be0]:csrrs a0, fcsr, zero
	-[0x80001be4]:sw t6, 472(t1)
Current Store : [0x80001be8] : sw a0, 476(t1) -- Store: [0x800129c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001bfc]:feq.h t6, ft11, ft10
	-[0x80001c00]:csrrs a0, fcsr, zero
	-[0x80001c04]:sw t6, 480(t1)
Current Store : [0x80001c08] : sw a0, 484(t1) -- Store: [0x800129c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c1c]:feq.h t6, ft11, ft10
	-[0x80001c20]:csrrs a0, fcsr, zero
	-[0x80001c24]:sw t6, 488(t1)
Current Store : [0x80001c28] : sw a0, 492(t1) -- Store: [0x800129d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c3c]:feq.h t6, ft11, ft10
	-[0x80001c40]:csrrs a0, fcsr, zero
	-[0x80001c44]:sw t6, 496(t1)
Current Store : [0x80001c48] : sw a0, 500(t1) -- Store: [0x800129d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c5c]:feq.h t6, ft11, ft10
	-[0x80001c60]:csrrs a0, fcsr, zero
	-[0x80001c64]:sw t6, 504(t1)
Current Store : [0x80001c68] : sw a0, 508(t1) -- Store: [0x800129e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c7c]:feq.h t6, ft11, ft10
	-[0x80001c80]:csrrs a0, fcsr, zero
	-[0x80001c84]:sw t6, 512(t1)
Current Store : [0x80001c88] : sw a0, 516(t1) -- Store: [0x800129e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c9c]:feq.h t6, ft11, ft10
	-[0x80001ca0]:csrrs a0, fcsr, zero
	-[0x80001ca4]:sw t6, 520(t1)
Current Store : [0x80001ca8] : sw a0, 524(t1) -- Store: [0x800129f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x009 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001cbc]:feq.h t6, ft11, ft10
	-[0x80001cc0]:csrrs a0, fcsr, zero
	-[0x80001cc4]:sw t6, 528(t1)
Current Store : [0x80001cc8] : sw a0, 532(t1) -- Store: [0x800129f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x009 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001cdc]:feq.h t6, ft11, ft10
	-[0x80001ce0]:csrrs a0, fcsr, zero
	-[0x80001ce4]:sw t6, 536(t1)
Current Store : [0x80001ce8] : sw a0, 540(t1) -- Store: [0x80012a00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x009 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001cfc]:feq.h t6, ft11, ft10
	-[0x80001d00]:csrrs a0, fcsr, zero
	-[0x80001d04]:sw t6, 544(t1)
Current Store : [0x80001d08] : sw a0, 548(t1) -- Store: [0x80012a08]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x009 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d1c]:feq.h t6, ft11, ft10
	-[0x80001d20]:csrrs a0, fcsr, zero
	-[0x80001d24]:sw t6, 552(t1)
Current Store : [0x80001d28] : sw a0, 556(t1) -- Store: [0x80012a10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d3c]:feq.h t6, ft11, ft10
	-[0x80001d40]:csrrs a0, fcsr, zero
	-[0x80001d44]:sw t6, 560(t1)
Current Store : [0x80001d48] : sw a0, 564(t1) -- Store: [0x80012a18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d5c]:feq.h t6, ft11, ft10
	-[0x80001d60]:csrrs a0, fcsr, zero
	-[0x80001d64]:sw t6, 568(t1)
Current Store : [0x80001d68] : sw a0, 572(t1) -- Store: [0x80012a20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d7c]:feq.h t6, ft11, ft10
	-[0x80001d80]:csrrs a0, fcsr, zero
	-[0x80001d84]:sw t6, 576(t1)
Current Store : [0x80001d88] : sw a0, 580(t1) -- Store: [0x80012a28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d9c]:feq.h t6, ft11, ft10
	-[0x80001da0]:csrrs a0, fcsr, zero
	-[0x80001da4]:sw t6, 584(t1)
Current Store : [0x80001da8] : sw a0, 588(t1) -- Store: [0x80012a30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001dbc]:feq.h t6, ft11, ft10
	-[0x80001dc0]:csrrs a0, fcsr, zero
	-[0x80001dc4]:sw t6, 592(t1)
Current Store : [0x80001dc8] : sw a0, 596(t1) -- Store: [0x80012a38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001ddc]:feq.h t6, ft11, ft10
	-[0x80001de0]:csrrs a0, fcsr, zero
	-[0x80001de4]:sw t6, 600(t1)
Current Store : [0x80001de8] : sw a0, 604(t1) -- Store: [0x80012a40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001dfc]:feq.h t6, ft11, ft10
	-[0x80001e00]:csrrs a0, fcsr, zero
	-[0x80001e04]:sw t6, 608(t1)
Current Store : [0x80001e08] : sw a0, 612(t1) -- Store: [0x80012a48]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e1c]:feq.h t6, ft11, ft10
	-[0x80001e20]:csrrs a0, fcsr, zero
	-[0x80001e24]:sw t6, 616(t1)
Current Store : [0x80001e28] : sw a0, 620(t1) -- Store: [0x80012a50]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e3c]:feq.h t6, ft11, ft10
	-[0x80001e40]:csrrs a0, fcsr, zero
	-[0x80001e44]:sw t6, 624(t1)
Current Store : [0x80001e48] : sw a0, 628(t1) -- Store: [0x80012a58]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e5c]:feq.h t6, ft11, ft10
	-[0x80001e60]:csrrs a0, fcsr, zero
	-[0x80001e64]:sw t6, 632(t1)
Current Store : [0x80001e68] : sw a0, 636(t1) -- Store: [0x80012a60]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e7c]:feq.h t6, ft11, ft10
	-[0x80001e80]:csrrs a0, fcsr, zero
	-[0x80001e84]:sw t6, 640(t1)
Current Store : [0x80001e88] : sw a0, 644(t1) -- Store: [0x80012a68]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e9c]:feq.h t6, ft11, ft10
	-[0x80001ea0]:csrrs a0, fcsr, zero
	-[0x80001ea4]:sw t6, 648(t1)
Current Store : [0x80001ea8] : sw a0, 652(t1) -- Store: [0x80012a70]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001ebc]:feq.h t6, ft11, ft10
	-[0x80001ec0]:csrrs a0, fcsr, zero
	-[0x80001ec4]:sw t6, 656(t1)
Current Store : [0x80001ec8] : sw a0, 660(t1) -- Store: [0x80012a78]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001edc]:feq.h t6, ft11, ft10
	-[0x80001ee0]:csrrs a0, fcsr, zero
	-[0x80001ee4]:sw t6, 664(t1)
Current Store : [0x80001ee8] : sw a0, 668(t1) -- Store: [0x80012a80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001efc]:feq.h t6, ft11, ft10
	-[0x80001f00]:csrrs a0, fcsr, zero
	-[0x80001f04]:sw t6, 672(t1)
Current Store : [0x80001f08] : sw a0, 676(t1) -- Store: [0x80012a88]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f1c]:feq.h t6, ft11, ft10
	-[0x80001f20]:csrrs a0, fcsr, zero
	-[0x80001f24]:sw t6, 680(t1)
Current Store : [0x80001f28] : sw a0, 684(t1) -- Store: [0x80012a90]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f3c]:feq.h t6, ft11, ft10
	-[0x80001f40]:csrrs a0, fcsr, zero
	-[0x80001f44]:sw t6, 688(t1)
Current Store : [0x80001f48] : sw a0, 692(t1) -- Store: [0x80012a98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x05b and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f5c]:feq.h t6, ft11, ft10
	-[0x80001f60]:csrrs a0, fcsr, zero
	-[0x80001f64]:sw t6, 696(t1)
Current Store : [0x80001f68] : sw a0, 700(t1) -- Store: [0x80012aa0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x05b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f7c]:feq.h t6, ft11, ft10
	-[0x80001f80]:csrrs a0, fcsr, zero
	-[0x80001f84]:sw t6, 704(t1)
Current Store : [0x80001f88] : sw a0, 708(t1) -- Store: [0x80012aa8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x05b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f9c]:feq.h t6, ft11, ft10
	-[0x80001fa0]:csrrs a0, fcsr, zero
	-[0x80001fa4]:sw t6, 712(t1)
Current Store : [0x80001fa8] : sw a0, 716(t1) -- Store: [0x80012ab0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x05b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001fbc]:feq.h t6, ft11, ft10
	-[0x80001fc0]:csrrs a0, fcsr, zero
	-[0x80001fc4]:sw t6, 720(t1)
Current Store : [0x80001fc8] : sw a0, 724(t1) -- Store: [0x80012ab8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001fdc]:feq.h t6, ft11, ft10
	-[0x80001fe0]:csrrs a0, fcsr, zero
	-[0x80001fe4]:sw t6, 728(t1)
Current Store : [0x80001fe8] : sw a0, 732(t1) -- Store: [0x80012ac0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001ffc]:feq.h t6, ft11, ft10
	-[0x80002000]:csrrs a0, fcsr, zero
	-[0x80002004]:sw t6, 736(t1)
Current Store : [0x80002008] : sw a0, 740(t1) -- Store: [0x80012ac8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000201c]:feq.h t6, ft11, ft10
	-[0x80002020]:csrrs a0, fcsr, zero
	-[0x80002024]:sw t6, 744(t1)
Current Store : [0x80002028] : sw a0, 748(t1) -- Store: [0x80012ad0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000203c]:feq.h t6, ft11, ft10
	-[0x80002040]:csrrs a0, fcsr, zero
	-[0x80002044]:sw t6, 752(t1)
Current Store : [0x80002048] : sw a0, 756(t1) -- Store: [0x80012ad8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000205c]:feq.h t6, ft11, ft10
	-[0x80002060]:csrrs a0, fcsr, zero
	-[0x80002064]:sw t6, 760(t1)
Current Store : [0x80002068] : sw a0, 764(t1) -- Store: [0x80012ae0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000207c]:feq.h t6, ft11, ft10
	-[0x80002080]:csrrs a0, fcsr, zero
	-[0x80002084]:sw t6, 768(t1)
Current Store : [0x80002088] : sw a0, 772(t1) -- Store: [0x80012ae8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000209c]:feq.h t6, ft11, ft10
	-[0x800020a0]:csrrs a0, fcsr, zero
	-[0x800020a4]:sw t6, 776(t1)
Current Store : [0x800020a8] : sw a0, 780(t1) -- Store: [0x80012af0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800020bc]:feq.h t6, ft11, ft10
	-[0x800020c0]:csrrs a0, fcsr, zero
	-[0x800020c4]:sw t6, 784(t1)
Current Store : [0x800020c8] : sw a0, 788(t1) -- Store: [0x80012af8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800020dc]:feq.h t6, ft11, ft10
	-[0x800020e0]:csrrs a0, fcsr, zero
	-[0x800020e4]:sw t6, 792(t1)
Current Store : [0x800020e8] : sw a0, 796(t1) -- Store: [0x80012b00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800020fc]:feq.h t6, ft11, ft10
	-[0x80002100]:csrrs a0, fcsr, zero
	-[0x80002104]:sw t6, 800(t1)
Current Store : [0x80002108] : sw a0, 804(t1) -- Store: [0x80012b08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000211c]:feq.h t6, ft11, ft10
	-[0x80002120]:csrrs a0, fcsr, zero
	-[0x80002124]:sw t6, 808(t1)
Current Store : [0x80002128] : sw a0, 812(t1) -- Store: [0x80012b10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000213c]:feq.h t6, ft11, ft10
	-[0x80002140]:csrrs a0, fcsr, zero
	-[0x80002144]:sw t6, 816(t1)
Current Store : [0x80002148] : sw a0, 820(t1) -- Store: [0x80012b18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000215c]:feq.h t6, ft11, ft10
	-[0x80002160]:csrrs a0, fcsr, zero
	-[0x80002164]:sw t6, 824(t1)
Current Store : [0x80002168] : sw a0, 828(t1) -- Store: [0x80012b20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x11 and fm1 == 0x17a and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000217c]:feq.h t6, ft11, ft10
	-[0x80002180]:csrrs a0, fcsr, zero
	-[0x80002184]:sw t6, 832(t1)
Current Store : [0x80002188] : sw a0, 836(t1) -- Store: [0x80012b28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x17a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000219c]:feq.h t6, ft11, ft10
	-[0x800021a0]:csrrs a0, fcsr, zero
	-[0x800021a4]:sw t6, 840(t1)
Current Store : [0x800021a8] : sw a0, 844(t1) -- Store: [0x80012b30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x17a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800021bc]:feq.h t6, ft11, ft10
	-[0x800021c0]:csrrs a0, fcsr, zero
	-[0x800021c4]:sw t6, 848(t1)
Current Store : [0x800021c8] : sw a0, 852(t1) -- Store: [0x80012b38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800021dc]:feq.h t6, ft11, ft10
	-[0x800021e0]:csrrs a0, fcsr, zero
	-[0x800021e4]:sw t6, 856(t1)
Current Store : [0x800021e8] : sw a0, 860(t1) -- Store: [0x80012b40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800021fc]:feq.h t6, ft11, ft10
	-[0x80002200]:csrrs a0, fcsr, zero
	-[0x80002204]:sw t6, 864(t1)
Current Store : [0x80002208] : sw a0, 868(t1) -- Store: [0x80012b48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000221c]:feq.h t6, ft11, ft10
	-[0x80002220]:csrrs a0, fcsr, zero
	-[0x80002224]:sw t6, 872(t1)
Current Store : [0x80002228] : sw a0, 876(t1) -- Store: [0x80012b50]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000223c]:feq.h t6, ft11, ft10
	-[0x80002240]:csrrs a0, fcsr, zero
	-[0x80002244]:sw t6, 880(t1)
Current Store : [0x80002248] : sw a0, 884(t1) -- Store: [0x80012b58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000225c]:feq.h t6, ft11, ft10
	-[0x80002260]:csrrs a0, fcsr, zero
	-[0x80002264]:sw t6, 888(t1)
Current Store : [0x80002268] : sw a0, 892(t1) -- Store: [0x80012b60]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000227c]:feq.h t6, ft11, ft10
	-[0x80002280]:csrrs a0, fcsr, zero
	-[0x80002284]:sw t6, 896(t1)
Current Store : [0x80002288] : sw a0, 900(t1) -- Store: [0x80012b68]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000229c]:feq.h t6, ft11, ft10
	-[0x800022a0]:csrrs a0, fcsr, zero
	-[0x800022a4]:sw t6, 904(t1)
Current Store : [0x800022a8] : sw a0, 908(t1) -- Store: [0x80012b70]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800022bc]:feq.h t6, ft11, ft10
	-[0x800022c0]:csrrs a0, fcsr, zero
	-[0x800022c4]:sw t6, 912(t1)
Current Store : [0x800022c8] : sw a0, 916(t1) -- Store: [0x80012b78]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800022dc]:feq.h t6, ft11, ft10
	-[0x800022e0]:csrrs a0, fcsr, zero
	-[0x800022e4]:sw t6, 920(t1)
Current Store : [0x800022e8] : sw a0, 924(t1) -- Store: [0x80012b80]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800022fc]:feq.h t6, ft11, ft10
	-[0x80002300]:csrrs a0, fcsr, zero
	-[0x80002304]:sw t6, 928(t1)
Current Store : [0x80002308] : sw a0, 932(t1) -- Store: [0x80012b88]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1b and fm1 == 0x00f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000231c]:feq.h t6, ft11, ft10
	-[0x80002320]:csrrs a0, fcsr, zero
	-[0x80002324]:sw t6, 936(t1)
Current Store : [0x80002328] : sw a0, 940(t1) -- Store: [0x80012b90]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1b and fm2 == 0x00f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000233c]:feq.h t6, ft11, ft10
	-[0x80002340]:csrrs a0, fcsr, zero
	-[0x80002344]:sw t6, 944(t1)
Current Store : [0x80002348] : sw a0, 948(t1) -- Store: [0x80012b98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1b and fm1 == 0x00f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000235c]:feq.h t6, ft11, ft10
	-[0x80002360]:csrrs a0, fcsr, zero
	-[0x80002364]:sw t6, 952(t1)
Current Store : [0x80002368] : sw a0, 956(t1) -- Store: [0x80012ba0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1b and fm2 == 0x00f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000237c]:feq.h t6, ft11, ft10
	-[0x80002380]:csrrs a0, fcsr, zero
	-[0x80002384]:sw t6, 960(t1)
Current Store : [0x80002388] : sw a0, 964(t1) -- Store: [0x80012ba8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000239c]:feq.h t6, ft11, ft10
	-[0x800023a0]:csrrs a0, fcsr, zero
	-[0x800023a4]:sw t6, 968(t1)
Current Store : [0x800023a8] : sw a0, 972(t1) -- Store: [0x80012bb0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800023bc]:feq.h t6, ft11, ft10
	-[0x800023c0]:csrrs a0, fcsr, zero
	-[0x800023c4]:sw t6, 976(t1)
Current Store : [0x800023c8] : sw a0, 980(t1) -- Store: [0x80012bb8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800023dc]:feq.h t6, ft11, ft10
	-[0x800023e0]:csrrs a0, fcsr, zero
	-[0x800023e4]:sw t6, 984(t1)
Current Store : [0x800023e8] : sw a0, 988(t1) -- Store: [0x80012bc0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800023fc]:feq.h t6, ft11, ft10
	-[0x80002400]:csrrs a0, fcsr, zero
	-[0x80002404]:sw t6, 992(t1)
Current Store : [0x80002408] : sw a0, 996(t1) -- Store: [0x80012bc8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000243c]:feq.h t6, ft11, ft10
	-[0x80002440]:csrrs a0, fcsr, zero
	-[0x80002444]:sw t6, 1000(t1)
Current Store : [0x80002448] : sw a0, 1004(t1) -- Store: [0x80012bd0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000247c]:feq.h t6, ft11, ft10
	-[0x80002480]:csrrs a0, fcsr, zero
	-[0x80002484]:sw t6, 1008(t1)
Current Store : [0x80002488] : sw a0, 1012(t1) -- Store: [0x80012bd8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800024bc]:feq.h t6, ft11, ft10
	-[0x800024c0]:csrrs a0, fcsr, zero
	-[0x800024c4]:sw t6, 1016(t1)
Current Store : [0x800024c8] : sw a0, 1020(t1) -- Store: [0x80012be0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002504]:feq.h t6, ft11, ft10
	-[0x80002508]:csrrs a0, fcsr, zero
	-[0x8000250c]:sw t6, 0(t1)
Current Store : [0x80002510] : sw a0, 4(t1) -- Store: [0x80012be8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002544]:feq.h t6, ft11, ft10
	-[0x80002548]:csrrs a0, fcsr, zero
	-[0x8000254c]:sw t6, 8(t1)
Current Store : [0x80002550] : sw a0, 12(t1) -- Store: [0x80012bf0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002584]:feq.h t6, ft11, ft10
	-[0x80002588]:csrrs a0, fcsr, zero
	-[0x8000258c]:sw t6, 16(t1)
Current Store : [0x80002590] : sw a0, 20(t1) -- Store: [0x80012bf8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800025c4]:feq.h t6, ft11, ft10
	-[0x800025c8]:csrrs a0, fcsr, zero
	-[0x800025cc]:sw t6, 24(t1)
Current Store : [0x800025d0] : sw a0, 28(t1) -- Store: [0x80012c00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002604]:feq.h t6, ft11, ft10
	-[0x80002608]:csrrs a0, fcsr, zero
	-[0x8000260c]:sw t6, 32(t1)
Current Store : [0x80002610] : sw a0, 36(t1) -- Store: [0x80012c08]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002644]:feq.h t6, ft11, ft10
	-[0x80002648]:csrrs a0, fcsr, zero
	-[0x8000264c]:sw t6, 40(t1)
Current Store : [0x80002650] : sw a0, 44(t1) -- Store: [0x80012c10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002684]:feq.h t6, ft11, ft10
	-[0x80002688]:csrrs a0, fcsr, zero
	-[0x8000268c]:sw t6, 48(t1)
Current Store : [0x80002690] : sw a0, 52(t1) -- Store: [0x80012c18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800026c4]:feq.h t6, ft11, ft10
	-[0x800026c8]:csrrs a0, fcsr, zero
	-[0x800026cc]:sw t6, 56(t1)
Current Store : [0x800026d0] : sw a0, 60(t1) -- Store: [0x80012c20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002704]:feq.h t6, ft11, ft10
	-[0x80002708]:csrrs a0, fcsr, zero
	-[0x8000270c]:sw t6, 64(t1)
Current Store : [0x80002710] : sw a0, 68(t1) -- Store: [0x80012c28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002744]:feq.h t6, ft11, ft10
	-[0x80002748]:csrrs a0, fcsr, zero
	-[0x8000274c]:sw t6, 72(t1)
Current Store : [0x80002750] : sw a0, 76(t1) -- Store: [0x80012c30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002784]:feq.h t6, ft11, ft10
	-[0x80002788]:csrrs a0, fcsr, zero
	-[0x8000278c]:sw t6, 80(t1)
Current Store : [0x80002790] : sw a0, 84(t1) -- Store: [0x80012c38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800027c4]:feq.h t6, ft11, ft10
	-[0x800027c8]:csrrs a0, fcsr, zero
	-[0x800027cc]:sw t6, 88(t1)
Current Store : [0x800027d0] : sw a0, 92(t1) -- Store: [0x80012c40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002804]:feq.h t6, ft11, ft10
	-[0x80002808]:csrrs a0, fcsr, zero
	-[0x8000280c]:sw t6, 96(t1)
Current Store : [0x80002810] : sw a0, 100(t1) -- Store: [0x80012c48]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002844]:feq.h t6, ft11, ft10
	-[0x80002848]:csrrs a0, fcsr, zero
	-[0x8000284c]:sw t6, 104(t1)
Current Store : [0x80002850] : sw a0, 108(t1) -- Store: [0x80012c50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002884]:feq.h t6, ft11, ft10
	-[0x80002888]:csrrs a0, fcsr, zero
	-[0x8000288c]:sw t6, 112(t1)
Current Store : [0x80002890] : sw a0, 116(t1) -- Store: [0x80012c58]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800028c4]:feq.h t6, ft11, ft10
	-[0x800028c8]:csrrs a0, fcsr, zero
	-[0x800028cc]:sw t6, 120(t1)
Current Store : [0x800028d0] : sw a0, 124(t1) -- Store: [0x80012c60]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002904]:feq.h t6, ft11, ft10
	-[0x80002908]:csrrs a0, fcsr, zero
	-[0x8000290c]:sw t6, 128(t1)
Current Store : [0x80002910] : sw a0, 132(t1) -- Store: [0x80012c68]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x045 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002944]:feq.h t6, ft11, ft10
	-[0x80002948]:csrrs a0, fcsr, zero
	-[0x8000294c]:sw t6, 136(t1)
Current Store : [0x80002950] : sw a0, 140(t1) -- Store: [0x80012c70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x045 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002984]:feq.h t6, ft11, ft10
	-[0x80002988]:csrrs a0, fcsr, zero
	-[0x8000298c]:sw t6, 144(t1)
Current Store : [0x80002990] : sw a0, 148(t1) -- Store: [0x80012c78]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x045 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800029c4]:feq.h t6, ft11, ft10
	-[0x800029c8]:csrrs a0, fcsr, zero
	-[0x800029cc]:sw t6, 152(t1)
Current Store : [0x800029d0] : sw a0, 156(t1) -- Store: [0x80012c80]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x045 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002a04]:feq.h t6, ft11, ft10
	-[0x80002a08]:csrrs a0, fcsr, zero
	-[0x80002a0c]:sw t6, 160(t1)
Current Store : [0x80002a10] : sw a0, 164(t1) -- Store: [0x80012c88]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002a44]:feq.h t6, ft11, ft10
	-[0x80002a48]:csrrs a0, fcsr, zero
	-[0x80002a4c]:sw t6, 168(t1)
Current Store : [0x80002a50] : sw a0, 172(t1) -- Store: [0x80012c90]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002a84]:feq.h t6, ft11, ft10
	-[0x80002a88]:csrrs a0, fcsr, zero
	-[0x80002a8c]:sw t6, 176(t1)
Current Store : [0x80002a90] : sw a0, 180(t1) -- Store: [0x80012c98]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002ac4]:feq.h t6, ft11, ft10
	-[0x80002ac8]:csrrs a0, fcsr, zero
	-[0x80002acc]:sw t6, 184(t1)
Current Store : [0x80002ad0] : sw a0, 188(t1) -- Store: [0x80012ca0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002b04]:feq.h t6, ft11, ft10
	-[0x80002b08]:csrrs a0, fcsr, zero
	-[0x80002b0c]:sw t6, 192(t1)
Current Store : [0x80002b10] : sw a0, 196(t1) -- Store: [0x80012ca8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002b44]:feq.h t6, ft11, ft10
	-[0x80002b48]:csrrs a0, fcsr, zero
	-[0x80002b4c]:sw t6, 200(t1)
Current Store : [0x80002b50] : sw a0, 204(t1) -- Store: [0x80012cb0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002b84]:feq.h t6, ft11, ft10
	-[0x80002b88]:csrrs a0, fcsr, zero
	-[0x80002b8c]:sw t6, 208(t1)
Current Store : [0x80002b90] : sw a0, 212(t1) -- Store: [0x80012cb8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002bc4]:feq.h t6, ft11, ft10
	-[0x80002bc8]:csrrs a0, fcsr, zero
	-[0x80002bcc]:sw t6, 216(t1)
Current Store : [0x80002bd0] : sw a0, 220(t1) -- Store: [0x80012cc0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002c04]:feq.h t6, ft11, ft10
	-[0x80002c08]:csrrs a0, fcsr, zero
	-[0x80002c0c]:sw t6, 224(t1)
Current Store : [0x80002c10] : sw a0, 228(t1) -- Store: [0x80012cc8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002c44]:feq.h t6, ft11, ft10
	-[0x80002c48]:csrrs a0, fcsr, zero
	-[0x80002c4c]:sw t6, 232(t1)
Current Store : [0x80002c50] : sw a0, 236(t1) -- Store: [0x80012cd0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002c84]:feq.h t6, ft11, ft10
	-[0x80002c88]:csrrs a0, fcsr, zero
	-[0x80002c8c]:sw t6, 240(t1)
Current Store : [0x80002c90] : sw a0, 244(t1) -- Store: [0x80012cd8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002cc4]:feq.h t6, ft11, ft10
	-[0x80002cc8]:csrrs a0, fcsr, zero
	-[0x80002ccc]:sw t6, 248(t1)
Current Store : [0x80002cd0] : sw a0, 252(t1) -- Store: [0x80012ce0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002d04]:feq.h t6, ft11, ft10
	-[0x80002d08]:csrrs a0, fcsr, zero
	-[0x80002d0c]:sw t6, 256(t1)
Current Store : [0x80002d10] : sw a0, 260(t1) -- Store: [0x80012ce8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002d44]:feq.h t6, ft11, ft10
	-[0x80002d48]:csrrs a0, fcsr, zero
	-[0x80002d4c]:sw t6, 264(t1)
Current Store : [0x80002d50] : sw a0, 268(t1) -- Store: [0x80012cf0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x11 and fm1 == 0x028 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002d84]:feq.h t6, ft11, ft10
	-[0x80002d88]:csrrs a0, fcsr, zero
	-[0x80002d8c]:sw t6, 272(t1)
Current Store : [0x80002d90] : sw a0, 276(t1) -- Store: [0x80012cf8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x028 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002dc4]:feq.h t6, ft11, ft10
	-[0x80002dc8]:csrrs a0, fcsr, zero
	-[0x80002dcc]:sw t6, 280(t1)
Current Store : [0x80002dd0] : sw a0, 284(t1) -- Store: [0x80012d00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x028 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002e04]:feq.h t6, ft11, ft10
	-[0x80002e08]:csrrs a0, fcsr, zero
	-[0x80002e0c]:sw t6, 288(t1)
Current Store : [0x80002e10] : sw a0, 292(t1) -- Store: [0x80012d08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002e44]:feq.h t6, ft11, ft10
	-[0x80002e48]:csrrs a0, fcsr, zero
	-[0x80002e4c]:sw t6, 296(t1)
Current Store : [0x80002e50] : sw a0, 300(t1) -- Store: [0x80012d10]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002e84]:feq.h t6, ft11, ft10
	-[0x80002e88]:csrrs a0, fcsr, zero
	-[0x80002e8c]:sw t6, 304(t1)
Current Store : [0x80002e90] : sw a0, 308(t1) -- Store: [0x80012d18]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002ec4]:feq.h t6, ft11, ft10
	-[0x80002ec8]:csrrs a0, fcsr, zero
	-[0x80002ecc]:sw t6, 312(t1)
Current Store : [0x80002ed0] : sw a0, 316(t1) -- Store: [0x80012d20]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002f04]:feq.h t6, ft11, ft10
	-[0x80002f08]:csrrs a0, fcsr, zero
	-[0x80002f0c]:sw t6, 320(t1)
Current Store : [0x80002f10] : sw a0, 324(t1) -- Store: [0x80012d28]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002f44]:feq.h t6, ft11, ft10
	-[0x80002f48]:csrrs a0, fcsr, zero
	-[0x80002f4c]:sw t6, 328(t1)
Current Store : [0x80002f50] : sw a0, 332(t1) -- Store: [0x80012d30]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002f84]:feq.h t6, ft11, ft10
	-[0x80002f88]:csrrs a0, fcsr, zero
	-[0x80002f8c]:sw t6, 336(t1)
Current Store : [0x80002f90] : sw a0, 340(t1) -- Store: [0x80012d38]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002fc4]:feq.h t6, ft11, ft10
	-[0x80002fc8]:csrrs a0, fcsr, zero
	-[0x80002fcc]:sw t6, 344(t1)
Current Store : [0x80002fd0] : sw a0, 348(t1) -- Store: [0x80012d40]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003004]:feq.h t6, ft11, ft10
	-[0x80003008]:csrrs a0, fcsr, zero
	-[0x8000300c]:sw t6, 352(t1)
Current Store : [0x80003010] : sw a0, 356(t1) -- Store: [0x80012d48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1a and fm1 == 0x1d4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003044]:feq.h t6, ft11, ft10
	-[0x80003048]:csrrs a0, fcsr, zero
	-[0x8000304c]:sw t6, 360(t1)
Current Store : [0x80003050] : sw a0, 364(t1) -- Store: [0x80012d50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1a and fm2 == 0x1d4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003084]:feq.h t6, ft11, ft10
	-[0x80003088]:csrrs a0, fcsr, zero
	-[0x8000308c]:sw t6, 368(t1)
Current Store : [0x80003090] : sw a0, 372(t1) -- Store: [0x80012d58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1a and fm1 == 0x1d4 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800030c4]:feq.h t6, ft11, ft10
	-[0x800030c8]:csrrs a0, fcsr, zero
	-[0x800030cc]:sw t6, 376(t1)
Current Store : [0x800030d0] : sw a0, 380(t1) -- Store: [0x80012d60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1a and fm2 == 0x1d4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003104]:feq.h t6, ft11, ft10
	-[0x80003108]:csrrs a0, fcsr, zero
	-[0x8000310c]:sw t6, 384(t1)
Current Store : [0x80003110] : sw a0, 388(t1) -- Store: [0x80012d68]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003144]:feq.h t6, ft11, ft10
	-[0x80003148]:csrrs a0, fcsr, zero
	-[0x8000314c]:sw t6, 392(t1)
Current Store : [0x80003150] : sw a0, 396(t1) -- Store: [0x80012d70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003184]:feq.h t6, ft11, ft10
	-[0x80003188]:csrrs a0, fcsr, zero
	-[0x8000318c]:sw t6, 400(t1)
Current Store : [0x80003190] : sw a0, 404(t1) -- Store: [0x80012d78]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800031c4]:feq.h t6, ft11, ft10
	-[0x800031c8]:csrrs a0, fcsr, zero
	-[0x800031cc]:sw t6, 408(t1)
Current Store : [0x800031d0] : sw a0, 412(t1) -- Store: [0x80012d80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003204]:feq.h t6, ft11, ft10
	-[0x80003208]:csrrs a0, fcsr, zero
	-[0x8000320c]:sw t6, 416(t1)
Current Store : [0x80003210] : sw a0, 420(t1) -- Store: [0x80012d88]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003244]:feq.h t6, ft11, ft10
	-[0x80003248]:csrrs a0, fcsr, zero
	-[0x8000324c]:sw t6, 424(t1)
Current Store : [0x80003250] : sw a0, 428(t1) -- Store: [0x80012d90]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003284]:feq.h t6, ft11, ft10
	-[0x80003288]:csrrs a0, fcsr, zero
	-[0x8000328c]:sw t6, 432(t1)
Current Store : [0x80003290] : sw a0, 436(t1) -- Store: [0x80012d98]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800032c4]:feq.h t6, ft11, ft10
	-[0x800032c8]:csrrs a0, fcsr, zero
	-[0x800032cc]:sw t6, 440(t1)
Current Store : [0x800032d0] : sw a0, 444(t1) -- Store: [0x80012da0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003304]:feq.h t6, ft11, ft10
	-[0x80003308]:csrrs a0, fcsr, zero
	-[0x8000330c]:sw t6, 448(t1)
Current Store : [0x80003310] : sw a0, 452(t1) -- Store: [0x80012da8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003344]:feq.h t6, ft11, ft10
	-[0x80003348]:csrrs a0, fcsr, zero
	-[0x8000334c]:sw t6, 456(t1)
Current Store : [0x80003350] : sw a0, 460(t1) -- Store: [0x80012db0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003384]:feq.h t6, ft11, ft10
	-[0x80003388]:csrrs a0, fcsr, zero
	-[0x8000338c]:sw t6, 464(t1)
Current Store : [0x80003390] : sw a0, 468(t1) -- Store: [0x80012db8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800033c4]:feq.h t6, ft11, ft10
	-[0x800033c8]:csrrs a0, fcsr, zero
	-[0x800033cc]:sw t6, 472(t1)
Current Store : [0x800033d0] : sw a0, 476(t1) -- Store: [0x80012dc0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003404]:feq.h t6, ft11, ft10
	-[0x80003408]:csrrs a0, fcsr, zero
	-[0x8000340c]:sw t6, 480(t1)
Current Store : [0x80003410] : sw a0, 484(t1) -- Store: [0x80012dc8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003444]:feq.h t6, ft11, ft10
	-[0x80003448]:csrrs a0, fcsr, zero
	-[0x8000344c]:sw t6, 488(t1)
Current Store : [0x80003450] : sw a0, 492(t1) -- Store: [0x80012dd0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003484]:feq.h t6, ft11, ft10
	-[0x80003488]:csrrs a0, fcsr, zero
	-[0x8000348c]:sw t6, 496(t1)
Current Store : [0x80003490] : sw a0, 500(t1) -- Store: [0x80012dd8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800034c4]:feq.h t6, ft11, ft10
	-[0x800034c8]:csrrs a0, fcsr, zero
	-[0x800034cc]:sw t6, 504(t1)
Current Store : [0x800034d0] : sw a0, 508(t1) -- Store: [0x80012de0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003504]:feq.h t6, ft11, ft10
	-[0x80003508]:csrrs a0, fcsr, zero
	-[0x8000350c]:sw t6, 512(t1)
Current Store : [0x80003510] : sw a0, 516(t1) -- Store: [0x80012de8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003544]:feq.h t6, ft11, ft10
	-[0x80003548]:csrrs a0, fcsr, zero
	-[0x8000354c]:sw t6, 520(t1)
Current Store : [0x80003550] : sw a0, 524(t1) -- Store: [0x80012df0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003584]:feq.h t6, ft11, ft10
	-[0x80003588]:csrrs a0, fcsr, zero
	-[0x8000358c]:sw t6, 528(t1)
Current Store : [0x80003590] : sw a0, 532(t1) -- Store: [0x80012df8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800035c4]:feq.h t6, ft11, ft10
	-[0x800035c8]:csrrs a0, fcsr, zero
	-[0x800035cc]:sw t6, 536(t1)
Current Store : [0x800035d0] : sw a0, 540(t1) -- Store: [0x80012e00]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003604]:feq.h t6, ft11, ft10
	-[0x80003608]:csrrs a0, fcsr, zero
	-[0x8000360c]:sw t6, 544(t1)
Current Store : [0x80003610] : sw a0, 548(t1) -- Store: [0x80012e08]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003644]:feq.h t6, ft11, ft10
	-[0x80003648]:csrrs a0, fcsr, zero
	-[0x8000364c]:sw t6, 552(t1)
Current Store : [0x80003650] : sw a0, 556(t1) -- Store: [0x80012e10]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003684]:feq.h t6, ft11, ft10
	-[0x80003688]:csrrs a0, fcsr, zero
	-[0x8000368c]:sw t6, 560(t1)
Current Store : [0x80003690] : sw a0, 564(t1) -- Store: [0x80012e18]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800036c4]:feq.h t6, ft11, ft10
	-[0x800036c8]:csrrs a0, fcsr, zero
	-[0x800036cc]:sw t6, 568(t1)
Current Store : [0x800036d0] : sw a0, 572(t1) -- Store: [0x80012e20]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003704]:feq.h t6, ft11, ft10
	-[0x80003708]:csrrs a0, fcsr, zero
	-[0x8000370c]:sw t6, 576(t1)
Current Store : [0x80003710] : sw a0, 580(t1) -- Store: [0x80012e28]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003744]:feq.h t6, ft11, ft10
	-[0x80003748]:csrrs a0, fcsr, zero
	-[0x8000374c]:sw t6, 584(t1)
Current Store : [0x80003750] : sw a0, 588(t1) -- Store: [0x80012e30]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003784]:feq.h t6, ft11, ft10
	-[0x80003788]:csrrs a0, fcsr, zero
	-[0x8000378c]:sw t6, 592(t1)
Current Store : [0x80003790] : sw a0, 596(t1) -- Store: [0x80012e38]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800037c4]:feq.h t6, ft11, ft10
	-[0x800037c8]:csrrs a0, fcsr, zero
	-[0x800037cc]:sw t6, 600(t1)
Current Store : [0x800037d0] : sw a0, 604(t1) -- Store: [0x80012e40]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x032 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003804]:feq.h t6, ft11, ft10
	-[0x80003808]:csrrs a0, fcsr, zero
	-[0x8000380c]:sw t6, 608(t1)
Current Store : [0x80003810] : sw a0, 612(t1) -- Store: [0x80012e48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x032 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003844]:feq.h t6, ft11, ft10
	-[0x80003848]:csrrs a0, fcsr, zero
	-[0x8000384c]:sw t6, 616(t1)
Current Store : [0x80003850] : sw a0, 620(t1) -- Store: [0x80012e50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x032 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003884]:feq.h t6, ft11, ft10
	-[0x80003888]:csrrs a0, fcsr, zero
	-[0x8000388c]:sw t6, 624(t1)
Current Store : [0x80003890] : sw a0, 628(t1) -- Store: [0x80012e58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x032 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800038c4]:feq.h t6, ft11, ft10
	-[0x800038c8]:csrrs a0, fcsr, zero
	-[0x800038cc]:sw t6, 632(t1)
Current Store : [0x800038d0] : sw a0, 636(t1) -- Store: [0x80012e60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003904]:feq.h t6, ft11, ft10
	-[0x80003908]:csrrs a0, fcsr, zero
	-[0x8000390c]:sw t6, 640(t1)
Current Store : [0x80003910] : sw a0, 644(t1) -- Store: [0x80012e68]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003944]:feq.h t6, ft11, ft10
	-[0x80003948]:csrrs a0, fcsr, zero
	-[0x8000394c]:sw t6, 648(t1)
Current Store : [0x80003950] : sw a0, 652(t1) -- Store: [0x80012e70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003984]:feq.h t6, ft11, ft10
	-[0x80003988]:csrrs a0, fcsr, zero
	-[0x8000398c]:sw t6, 656(t1)
Current Store : [0x80003990] : sw a0, 660(t1) -- Store: [0x80012e78]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800039c4]:feq.h t6, ft11, ft10
	-[0x800039c8]:csrrs a0, fcsr, zero
	-[0x800039cc]:sw t6, 664(t1)
Current Store : [0x800039d0] : sw a0, 668(t1) -- Store: [0x80012e80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003a04]:feq.h t6, ft11, ft10
	-[0x80003a08]:csrrs a0, fcsr, zero
	-[0x80003a0c]:sw t6, 672(t1)
Current Store : [0x80003a10] : sw a0, 676(t1) -- Store: [0x80012e88]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003a44]:feq.h t6, ft11, ft10
	-[0x80003a48]:csrrs a0, fcsr, zero
	-[0x80003a4c]:sw t6, 680(t1)
Current Store : [0x80003a50] : sw a0, 684(t1) -- Store: [0x80012e90]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003a84]:feq.h t6, ft11, ft10
	-[0x80003a88]:csrrs a0, fcsr, zero
	-[0x80003a8c]:sw t6, 688(t1)
Current Store : [0x80003a90] : sw a0, 692(t1) -- Store: [0x80012e98]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003ac4]:feq.h t6, ft11, ft10
	-[0x80003ac8]:csrrs a0, fcsr, zero
	-[0x80003acc]:sw t6, 696(t1)
Current Store : [0x80003ad0] : sw a0, 700(t1) -- Store: [0x80012ea0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003b04]:feq.h t6, ft11, ft10
	-[0x80003b08]:csrrs a0, fcsr, zero
	-[0x80003b0c]:sw t6, 704(t1)
Current Store : [0x80003b10] : sw a0, 708(t1) -- Store: [0x80012ea8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003b44]:feq.h t6, ft11, ft10
	-[0x80003b48]:csrrs a0, fcsr, zero
	-[0x80003b4c]:sw t6, 712(t1)
Current Store : [0x80003b50] : sw a0, 716(t1) -- Store: [0x80012eb0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003b84]:feq.h t6, ft11, ft10
	-[0x80003b88]:csrrs a0, fcsr, zero
	-[0x80003b8c]:sw t6, 720(t1)
Current Store : [0x80003b90] : sw a0, 724(t1) -- Store: [0x80012eb8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003bc4]:feq.h t6, ft11, ft10
	-[0x80003bc8]:csrrs a0, fcsr, zero
	-[0x80003bcc]:sw t6, 728(t1)
Current Store : [0x80003bd0] : sw a0, 732(t1) -- Store: [0x80012ec0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003c04]:feq.h t6, ft11, ft10
	-[0x80003c08]:csrrs a0, fcsr, zero
	-[0x80003c0c]:sw t6, 736(t1)
Current Store : [0x80003c10] : sw a0, 740(t1) -- Store: [0x80012ec8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x10 and fm1 == 0x1f8 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003c44]:feq.h t6, ft11, ft10
	-[0x80003c48]:csrrs a0, fcsr, zero
	-[0x80003c4c]:sw t6, 744(t1)
Current Store : [0x80003c50] : sw a0, 748(t1) -- Store: [0x80012ed0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x1f8 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003c84]:feq.h t6, ft11, ft10
	-[0x80003c88]:csrrs a0, fcsr, zero
	-[0x80003c8c]:sw t6, 752(t1)
Current Store : [0x80003c90] : sw a0, 756(t1) -- Store: [0x80012ed8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x1f8 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003cc4]:feq.h t6, ft11, ft10
	-[0x80003cc8]:csrrs a0, fcsr, zero
	-[0x80003ccc]:sw t6, 760(t1)
Current Store : [0x80003cd0] : sw a0, 764(t1) -- Store: [0x80012ee0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003d04]:feq.h t6, ft11, ft10
	-[0x80003d08]:csrrs a0, fcsr, zero
	-[0x80003d0c]:sw t6, 768(t1)
Current Store : [0x80003d10] : sw a0, 772(t1) -- Store: [0x80012ee8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003d44]:feq.h t6, ft11, ft10
	-[0x80003d48]:csrrs a0, fcsr, zero
	-[0x80003d4c]:sw t6, 776(t1)
Current Store : [0x80003d50] : sw a0, 780(t1) -- Store: [0x80012ef0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003d84]:feq.h t6, ft11, ft10
	-[0x80003d88]:csrrs a0, fcsr, zero
	-[0x80003d8c]:sw t6, 784(t1)
Current Store : [0x80003d90] : sw a0, 788(t1) -- Store: [0x80012ef8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003dc4]:feq.h t6, ft11, ft10
	-[0x80003dc8]:csrrs a0, fcsr, zero
	-[0x80003dcc]:sw t6, 792(t1)
Current Store : [0x80003dd0] : sw a0, 796(t1) -- Store: [0x80012f00]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003e04]:feq.h t6, ft11, ft10
	-[0x80003e08]:csrrs a0, fcsr, zero
	-[0x80003e0c]:sw t6, 800(t1)
Current Store : [0x80003e10] : sw a0, 804(t1) -- Store: [0x80012f08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003e44]:feq.h t6, ft11, ft10
	-[0x80003e48]:csrrs a0, fcsr, zero
	-[0x80003e4c]:sw t6, 808(t1)
Current Store : [0x80003e50] : sw a0, 812(t1) -- Store: [0x80012f10]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1b and fm1 == 0x1fa and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003e84]:feq.h t6, ft11, ft10
	-[0x80003e88]:csrrs a0, fcsr, zero
	-[0x80003e8c]:sw t6, 816(t1)
Current Store : [0x80003e90] : sw a0, 820(t1) -- Store: [0x80012f18]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1b and fm2 == 0x1fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003ec4]:feq.h t6, ft11, ft10
	-[0x80003ec8]:csrrs a0, fcsr, zero
	-[0x80003ecc]:sw t6, 824(t1)
Current Store : [0x80003ed0] : sw a0, 828(t1) -- Store: [0x80012f20]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1b and fm1 == 0x1fa and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003f04]:feq.h t6, ft11, ft10
	-[0x80003f08]:csrrs a0, fcsr, zero
	-[0x80003f0c]:sw t6, 832(t1)
Current Store : [0x80003f10] : sw a0, 836(t1) -- Store: [0x80012f28]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1b and fm2 == 0x1fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003f44]:feq.h t6, ft11, ft10
	-[0x80003f48]:csrrs a0, fcsr, zero
	-[0x80003f4c]:sw t6, 840(t1)
Current Store : [0x80003f50] : sw a0, 844(t1) -- Store: [0x80012f30]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003f84]:feq.h t6, ft11, ft10
	-[0x80003f88]:csrrs a0, fcsr, zero
	-[0x80003f8c]:sw t6, 848(t1)
Current Store : [0x80003f90] : sw a0, 852(t1) -- Store: [0x80012f38]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003fc4]:feq.h t6, ft11, ft10
	-[0x80003fc8]:csrrs a0, fcsr, zero
	-[0x80003fcc]:sw t6, 856(t1)
Current Store : [0x80003fd0] : sw a0, 860(t1) -- Store: [0x80012f40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004004]:feq.h t6, ft11, ft10
	-[0x80004008]:csrrs a0, fcsr, zero
	-[0x8000400c]:sw t6, 864(t1)
Current Store : [0x80004010] : sw a0, 868(t1) -- Store: [0x80012f48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004044]:feq.h t6, ft11, ft10
	-[0x80004048]:csrrs a0, fcsr, zero
	-[0x8000404c]:sw t6, 872(t1)
Current Store : [0x80004050] : sw a0, 876(t1) -- Store: [0x80012f50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004084]:feq.h t6, ft11, ft10
	-[0x80004088]:csrrs a0, fcsr, zero
	-[0x8000408c]:sw t6, 880(t1)
Current Store : [0x80004090] : sw a0, 884(t1) -- Store: [0x80012f58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800040c4]:feq.h t6, ft11, ft10
	-[0x800040c8]:csrrs a0, fcsr, zero
	-[0x800040cc]:sw t6, 888(t1)
Current Store : [0x800040d0] : sw a0, 892(t1) -- Store: [0x80012f60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x00a and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004104]:feq.h t6, ft11, ft10
	-[0x80004108]:csrrs a0, fcsr, zero
	-[0x8000410c]:sw t6, 896(t1)
Current Store : [0x80004110] : sw a0, 900(t1) -- Store: [0x80012f68]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x00a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004144]:feq.h t6, ft11, ft10
	-[0x80004148]:csrrs a0, fcsr, zero
	-[0x8000414c]:sw t6, 904(t1)
Current Store : [0x80004150] : sw a0, 908(t1) -- Store: [0x80012f70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x00a and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004184]:feq.h t6, ft11, ft10
	-[0x80004188]:csrrs a0, fcsr, zero
	-[0x8000418c]:sw t6, 912(t1)
Current Store : [0x80004190] : sw a0, 916(t1) -- Store: [0x80012f78]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x00a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800041c4]:feq.h t6, ft11, ft10
	-[0x800041c8]:csrrs a0, fcsr, zero
	-[0x800041cc]:sw t6, 920(t1)
Current Store : [0x800041d0] : sw a0, 924(t1) -- Store: [0x80012f80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004204]:feq.h t6, ft11, ft10
	-[0x80004208]:csrrs a0, fcsr, zero
	-[0x8000420c]:sw t6, 928(t1)
Current Store : [0x80004210] : sw a0, 932(t1) -- Store: [0x80012f88]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004244]:feq.h t6, ft11, ft10
	-[0x80004248]:csrrs a0, fcsr, zero
	-[0x8000424c]:sw t6, 936(t1)
Current Store : [0x80004250] : sw a0, 940(t1) -- Store: [0x80012f90]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004284]:feq.h t6, ft11, ft10
	-[0x80004288]:csrrs a0, fcsr, zero
	-[0x8000428c]:sw t6, 944(t1)
Current Store : [0x80004290] : sw a0, 948(t1) -- Store: [0x80012f98]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800042c4]:feq.h t6, ft11, ft10
	-[0x800042c8]:csrrs a0, fcsr, zero
	-[0x800042cc]:sw t6, 952(t1)
Current Store : [0x800042d0] : sw a0, 956(t1) -- Store: [0x80012fa0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004304]:feq.h t6, ft11, ft10
	-[0x80004308]:csrrs a0, fcsr, zero
	-[0x8000430c]:sw t6, 960(t1)
Current Store : [0x80004310] : sw a0, 964(t1) -- Store: [0x80012fa8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004344]:feq.h t6, ft11, ft10
	-[0x80004348]:csrrs a0, fcsr, zero
	-[0x8000434c]:sw t6, 968(t1)
Current Store : [0x80004350] : sw a0, 972(t1) -- Store: [0x80012fb0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004384]:feq.h t6, ft11, ft10
	-[0x80004388]:csrrs a0, fcsr, zero
	-[0x8000438c]:sw t6, 976(t1)
Current Store : [0x80004390] : sw a0, 980(t1) -- Store: [0x80012fb8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800043c4]:feq.h t6, ft11, ft10
	-[0x800043c8]:csrrs a0, fcsr, zero
	-[0x800043cc]:sw t6, 984(t1)
Current Store : [0x800043d0] : sw a0, 988(t1) -- Store: [0x80012fc0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004404]:feq.h t6, ft11, ft10
	-[0x80004408]:csrrs a0, fcsr, zero
	-[0x8000440c]:sw t6, 992(t1)
Current Store : [0x80004410] : sw a0, 996(t1) -- Store: [0x80012fc8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004444]:feq.h t6, ft11, ft10
	-[0x80004448]:csrrs a0, fcsr, zero
	-[0x8000444c]:sw t6, 1000(t1)
Current Store : [0x80004450] : sw a0, 1004(t1) -- Store: [0x80012fd0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004484]:feq.h t6, ft11, ft10
	-[0x80004488]:csrrs a0, fcsr, zero
	-[0x8000448c]:sw t6, 1008(t1)
Current Store : [0x80004490] : sw a0, 1012(t1) -- Store: [0x80012fd8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800044c4]:feq.h t6, ft11, ft10
	-[0x800044c8]:csrrs a0, fcsr, zero
	-[0x800044cc]:sw t6, 1016(t1)
Current Store : [0x800044d0] : sw a0, 1020(t1) -- Store: [0x80012fe0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000450c]:feq.h t6, ft11, ft10
	-[0x80004510]:csrrs a0, fcsr, zero
	-[0x80004514]:sw t6, 0(t1)
Current Store : [0x80004518] : sw a0, 4(t1) -- Store: [0x80012fe8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000454c]:feq.h t6, ft11, ft10
	-[0x80004550]:csrrs a0, fcsr, zero
	-[0x80004554]:sw t6, 8(t1)
Current Store : [0x80004558] : sw a0, 12(t1) -- Store: [0x80012ff0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000458c]:feq.h t6, ft11, ft10
	-[0x80004590]:csrrs a0, fcsr, zero
	-[0x80004594]:sw t6, 16(t1)
Current Store : [0x80004598] : sw a0, 20(t1) -- Store: [0x80012ff8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800045cc]:feq.h t6, ft11, ft10
	-[0x800045d0]:csrrs a0, fcsr, zero
	-[0x800045d4]:sw t6, 24(t1)
Current Store : [0x800045d8] : sw a0, 28(t1) -- Store: [0x80013000]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000460c]:feq.h t6, ft11, ft10
	-[0x80004610]:csrrs a0, fcsr, zero
	-[0x80004614]:sw t6, 32(t1)
Current Store : [0x80004618] : sw a0, 36(t1) -- Store: [0x80013008]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x066 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000464c]:feq.h t6, ft11, ft10
	-[0x80004650]:csrrs a0, fcsr, zero
	-[0x80004654]:sw t6, 40(t1)
Current Store : [0x80004658] : sw a0, 44(t1) -- Store: [0x80013010]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x066 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000468c]:feq.h t6, ft11, ft10
	-[0x80004690]:csrrs a0, fcsr, zero
	-[0x80004694]:sw t6, 48(t1)
Current Store : [0x80004698] : sw a0, 52(t1) -- Store: [0x80013018]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x066 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800046cc]:feq.h t6, ft11, ft10
	-[0x800046d0]:csrrs a0, fcsr, zero
	-[0x800046d4]:sw t6, 56(t1)
Current Store : [0x800046d8] : sw a0, 60(t1) -- Store: [0x80013020]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x066 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000470c]:feq.h t6, ft11, ft10
	-[0x80004710]:csrrs a0, fcsr, zero
	-[0x80004714]:sw t6, 64(t1)
Current Store : [0x80004718] : sw a0, 68(t1) -- Store: [0x80013028]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000474c]:feq.h t6, ft11, ft10
	-[0x80004750]:csrrs a0, fcsr, zero
	-[0x80004754]:sw t6, 72(t1)
Current Store : [0x80004758] : sw a0, 76(t1) -- Store: [0x80013030]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000478c]:feq.h t6, ft11, ft10
	-[0x80004790]:csrrs a0, fcsr, zero
	-[0x80004794]:sw t6, 80(t1)
Current Store : [0x80004798] : sw a0, 84(t1) -- Store: [0x80013038]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800047cc]:feq.h t6, ft11, ft10
	-[0x800047d0]:csrrs a0, fcsr, zero
	-[0x800047d4]:sw t6, 88(t1)
Current Store : [0x800047d8] : sw a0, 92(t1) -- Store: [0x80013040]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000480c]:feq.h t6, ft11, ft10
	-[0x80004810]:csrrs a0, fcsr, zero
	-[0x80004814]:sw t6, 96(t1)
Current Store : [0x80004818] : sw a0, 100(t1) -- Store: [0x80013048]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000484c]:feq.h t6, ft11, ft10
	-[0x80004850]:csrrs a0, fcsr, zero
	-[0x80004854]:sw t6, 104(t1)
Current Store : [0x80004858] : sw a0, 108(t1) -- Store: [0x80013050]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000488c]:feq.h t6, ft11, ft10
	-[0x80004890]:csrrs a0, fcsr, zero
	-[0x80004894]:sw t6, 112(t1)
Current Store : [0x80004898] : sw a0, 116(t1) -- Store: [0x80013058]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800048cc]:feq.h t6, ft11, ft10
	-[0x800048d0]:csrrs a0, fcsr, zero
	-[0x800048d4]:sw t6, 120(t1)
Current Store : [0x800048d8] : sw a0, 124(t1) -- Store: [0x80013060]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000490c]:feq.h t6, ft11, ft10
	-[0x80004910]:csrrs a0, fcsr, zero
	-[0x80004914]:sw t6, 128(t1)
Current Store : [0x80004918] : sw a0, 132(t1) -- Store: [0x80013068]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000494c]:feq.h t6, ft11, ft10
	-[0x80004950]:csrrs a0, fcsr, zero
	-[0x80004954]:sw t6, 136(t1)
Current Store : [0x80004958] : sw a0, 140(t1) -- Store: [0x80013070]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000498c]:feq.h t6, ft11, ft10
	-[0x80004990]:csrrs a0, fcsr, zero
	-[0x80004994]:sw t6, 144(t1)
Current Store : [0x80004998] : sw a0, 148(t1) -- Store: [0x80013078]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800049cc]:feq.h t6, ft11, ft10
	-[0x800049d0]:csrrs a0, fcsr, zero
	-[0x800049d4]:sw t6, 152(t1)
Current Store : [0x800049d8] : sw a0, 156(t1) -- Store: [0x80013080]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004a0c]:feq.h t6, ft11, ft10
	-[0x80004a10]:csrrs a0, fcsr, zero
	-[0x80004a14]:sw t6, 160(t1)
Current Store : [0x80004a18] : sw a0, 164(t1) -- Store: [0x80013088]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004a4c]:feq.h t6, ft11, ft10
	-[0x80004a50]:csrrs a0, fcsr, zero
	-[0x80004a54]:sw t6, 168(t1)
Current Store : [0x80004a58] : sw a0, 172(t1) -- Store: [0x80013090]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x11 and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004a8c]:feq.h t6, ft11, ft10
	-[0x80004a90]:csrrs a0, fcsr, zero
	-[0x80004a94]:sw t6, 176(t1)
Current Store : [0x80004a98] : sw a0, 180(t1) -- Store: [0x80013098]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004acc]:feq.h t6, ft11, ft10
	-[0x80004ad0]:csrrs a0, fcsr, zero
	-[0x80004ad4]:sw t6, 184(t1)
Current Store : [0x80004ad8] : sw a0, 188(t1) -- Store: [0x800130a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004b0c]:feq.h t6, ft11, ft10
	-[0x80004b10]:csrrs a0, fcsr, zero
	-[0x80004b14]:sw t6, 192(t1)
Current Store : [0x80004b18] : sw a0, 196(t1) -- Store: [0x800130a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004b4c]:feq.h t6, ft11, ft10
	-[0x80004b50]:csrrs a0, fcsr, zero
	-[0x80004b54]:sw t6, 200(t1)
Current Store : [0x80004b58] : sw a0, 204(t1) -- Store: [0x800130b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004b8c]:feq.h t6, ft11, ft10
	-[0x80004b90]:csrrs a0, fcsr, zero
	-[0x80004b94]:sw t6, 208(t1)
Current Store : [0x80004b98] : sw a0, 212(t1) -- Store: [0x800130b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004bcc]:feq.h t6, ft11, ft10
	-[0x80004bd0]:csrrs a0, fcsr, zero
	-[0x80004bd4]:sw t6, 216(t1)
Current Store : [0x80004bd8] : sw a0, 220(t1) -- Store: [0x800130c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004c0c]:feq.h t6, ft11, ft10
	-[0x80004c10]:csrrs a0, fcsr, zero
	-[0x80004c14]:sw t6, 224(t1)
Current Store : [0x80004c18] : sw a0, 228(t1) -- Store: [0x800130c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1b and fm1 == 0x0e5 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004c4c]:feq.h t6, ft11, ft10
	-[0x80004c50]:csrrs a0, fcsr, zero
	-[0x80004c54]:sw t6, 232(t1)
Current Store : [0x80004c58] : sw a0, 236(t1) -- Store: [0x800130d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1b and fm2 == 0x0e5 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004c8c]:feq.h t6, ft11, ft10
	-[0x80004c90]:csrrs a0, fcsr, zero
	-[0x80004c94]:sw t6, 240(t1)
Current Store : [0x80004c98] : sw a0, 244(t1) -- Store: [0x800130d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1b and fm1 == 0x0e5 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004ccc]:feq.h t6, ft11, ft10
	-[0x80004cd0]:csrrs a0, fcsr, zero
	-[0x80004cd4]:sw t6, 248(t1)
Current Store : [0x80004cd8] : sw a0, 252(t1) -- Store: [0x800130e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1b and fm2 == 0x0e5 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004d0c]:feq.h t6, ft11, ft10
	-[0x80004d10]:csrrs a0, fcsr, zero
	-[0x80004d14]:sw t6, 256(t1)
Current Store : [0x80004d18] : sw a0, 260(t1) -- Store: [0x800130e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004d4c]:feq.h t6, ft11, ft10
	-[0x80004d50]:csrrs a0, fcsr, zero
	-[0x80004d54]:sw t6, 264(t1)
Current Store : [0x80004d58] : sw a0, 268(t1) -- Store: [0x800130f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004d8c]:feq.h t6, ft11, ft10
	-[0x80004d90]:csrrs a0, fcsr, zero
	-[0x80004d94]:sw t6, 272(t1)
Current Store : [0x80004d98] : sw a0, 276(t1) -- Store: [0x800130f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004dcc]:feq.h t6, ft11, ft10
	-[0x80004dd0]:csrrs a0, fcsr, zero
	-[0x80004dd4]:sw t6, 280(t1)
Current Store : [0x80004dd8] : sw a0, 284(t1) -- Store: [0x80013100]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004e0c]:feq.h t6, ft11, ft10
	-[0x80004e10]:csrrs a0, fcsr, zero
	-[0x80004e14]:sw t6, 288(t1)
Current Store : [0x80004e18] : sw a0, 292(t1) -- Store: [0x80013108]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004e4c]:feq.h t6, ft11, ft10
	-[0x80004e50]:csrrs a0, fcsr, zero
	-[0x80004e54]:sw t6, 296(t1)
Current Store : [0x80004e58] : sw a0, 300(t1) -- Store: [0x80013110]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004e8c]:feq.h t6, ft11, ft10
	-[0x80004e90]:csrrs a0, fcsr, zero
	-[0x80004e94]:sw t6, 304(t1)
Current Store : [0x80004e98] : sw a0, 308(t1) -- Store: [0x80013118]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x008 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004ecc]:feq.h t6, ft11, ft10
	-[0x80004ed0]:csrrs a0, fcsr, zero
	-[0x80004ed4]:sw t6, 312(t1)
Current Store : [0x80004ed8] : sw a0, 316(t1) -- Store: [0x80013120]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x008 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004f0c]:feq.h t6, ft11, ft10
	-[0x80004f10]:csrrs a0, fcsr, zero
	-[0x80004f14]:sw t6, 320(t1)
Current Store : [0x80004f18] : sw a0, 324(t1) -- Store: [0x80013128]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x008 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004f4c]:feq.h t6, ft11, ft10
	-[0x80004f50]:csrrs a0, fcsr, zero
	-[0x80004f54]:sw t6, 328(t1)
Current Store : [0x80004f58] : sw a0, 332(t1) -- Store: [0x80013130]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x008 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004f8c]:feq.h t6, ft11, ft10
	-[0x80004f90]:csrrs a0, fcsr, zero
	-[0x80004f94]:sw t6, 336(t1)
Current Store : [0x80004f98] : sw a0, 340(t1) -- Store: [0x80013138]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004fcc]:feq.h t6, ft11, ft10
	-[0x80004fd0]:csrrs a0, fcsr, zero
	-[0x80004fd4]:sw t6, 344(t1)
Current Store : [0x80004fd8] : sw a0, 348(t1) -- Store: [0x80013140]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000500c]:feq.h t6, ft11, ft10
	-[0x80005010]:csrrs a0, fcsr, zero
	-[0x80005014]:sw t6, 352(t1)
Current Store : [0x80005018] : sw a0, 356(t1) -- Store: [0x80013148]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000504c]:feq.h t6, ft11, ft10
	-[0x80005050]:csrrs a0, fcsr, zero
	-[0x80005054]:sw t6, 360(t1)
Current Store : [0x80005058] : sw a0, 364(t1) -- Store: [0x80013150]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000508c]:feq.h t6, ft11, ft10
	-[0x80005090]:csrrs a0, fcsr, zero
	-[0x80005094]:sw t6, 368(t1)
Current Store : [0x80005098] : sw a0, 372(t1) -- Store: [0x80013158]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800050cc]:feq.h t6, ft11, ft10
	-[0x800050d0]:csrrs a0, fcsr, zero
	-[0x800050d4]:sw t6, 376(t1)
Current Store : [0x800050d8] : sw a0, 380(t1) -- Store: [0x80013160]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000510c]:feq.h t6, ft11, ft10
	-[0x80005110]:csrrs a0, fcsr, zero
	-[0x80005114]:sw t6, 384(t1)
Current Store : [0x80005118] : sw a0, 388(t1) -- Store: [0x80013168]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000514c]:feq.h t6, ft11, ft10
	-[0x80005150]:csrrs a0, fcsr, zero
	-[0x80005154]:sw t6, 392(t1)
Current Store : [0x80005158] : sw a0, 396(t1) -- Store: [0x80013170]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000518c]:feq.h t6, ft11, ft10
	-[0x80005190]:csrrs a0, fcsr, zero
	-[0x80005194]:sw t6, 400(t1)
Current Store : [0x80005198] : sw a0, 404(t1) -- Store: [0x80013178]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800051cc]:feq.h t6, ft11, ft10
	-[0x800051d0]:csrrs a0, fcsr, zero
	-[0x800051d4]:sw t6, 408(t1)
Current Store : [0x800051d8] : sw a0, 412(t1) -- Store: [0x80013180]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000520c]:feq.h t6, ft11, ft10
	-[0x80005210]:csrrs a0, fcsr, zero
	-[0x80005214]:sw t6, 416(t1)
Current Store : [0x80005218] : sw a0, 420(t1) -- Store: [0x80013188]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000524c]:feq.h t6, ft11, ft10
	-[0x80005250]:csrrs a0, fcsr, zero
	-[0x80005254]:sw t6, 424(t1)
Current Store : [0x80005258] : sw a0, 428(t1) -- Store: [0x80013190]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000528c]:feq.h t6, ft11, ft10
	-[0x80005290]:csrrs a0, fcsr, zero
	-[0x80005294]:sw t6, 432(t1)
Current Store : [0x80005298] : sw a0, 436(t1) -- Store: [0x80013198]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800052cc]:feq.h t6, ft11, ft10
	-[0x800052d0]:csrrs a0, fcsr, zero
	-[0x800052d4]:sw t6, 440(t1)
Current Store : [0x800052d8] : sw a0, 444(t1) -- Store: [0x800131a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000530c]:feq.h t6, ft11, ft10
	-[0x80005310]:csrrs a0, fcsr, zero
	-[0x80005314]:sw t6, 448(t1)
Current Store : [0x80005318] : sw a0, 452(t1) -- Store: [0x800131a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000534c]:feq.h t6, ft11, ft10
	-[0x80005350]:csrrs a0, fcsr, zero
	-[0x80005354]:sw t6, 456(t1)
Current Store : [0x80005358] : sw a0, 460(t1) -- Store: [0x800131b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000538c]:feq.h t6, ft11, ft10
	-[0x80005390]:csrrs a0, fcsr, zero
	-[0x80005394]:sw t6, 464(t1)
Current Store : [0x80005398] : sw a0, 468(t1) -- Store: [0x800131b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800053cc]:feq.h t6, ft11, ft10
	-[0x800053d0]:csrrs a0, fcsr, zero
	-[0x800053d4]:sw t6, 472(t1)
Current Store : [0x800053d8] : sw a0, 476(t1) -- Store: [0x800131c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x054 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000540c]:feq.h t6, ft11, ft10
	-[0x80005410]:csrrs a0, fcsr, zero
	-[0x80005414]:sw t6, 480(t1)
Current Store : [0x80005418] : sw a0, 484(t1) -- Store: [0x800131c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x054 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000544c]:feq.h t6, ft11, ft10
	-[0x80005450]:csrrs a0, fcsr, zero
	-[0x80005454]:sw t6, 488(t1)
Current Store : [0x80005458] : sw a0, 492(t1) -- Store: [0x800131d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x054 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000548c]:feq.h t6, ft11, ft10
	-[0x80005490]:csrrs a0, fcsr, zero
	-[0x80005494]:sw t6, 496(t1)
Current Store : [0x80005498] : sw a0, 500(t1) -- Store: [0x800131d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x054 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800054cc]:feq.h t6, ft11, ft10
	-[0x800054d0]:csrrs a0, fcsr, zero
	-[0x800054d4]:sw t6, 504(t1)
Current Store : [0x800054d8] : sw a0, 508(t1) -- Store: [0x800131e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000550c]:feq.h t6, ft11, ft10
	-[0x80005510]:csrrs a0, fcsr, zero
	-[0x80005514]:sw t6, 512(t1)
Current Store : [0x80005518] : sw a0, 516(t1) -- Store: [0x800131e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000554c]:feq.h t6, ft11, ft10
	-[0x80005550]:csrrs a0, fcsr, zero
	-[0x80005554]:sw t6, 520(t1)
Current Store : [0x80005558] : sw a0, 524(t1) -- Store: [0x800131f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000558c]:feq.h t6, ft11, ft10
	-[0x80005590]:csrrs a0, fcsr, zero
	-[0x80005594]:sw t6, 528(t1)
Current Store : [0x80005598] : sw a0, 532(t1) -- Store: [0x800131f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800055cc]:feq.h t6, ft11, ft10
	-[0x800055d0]:csrrs a0, fcsr, zero
	-[0x800055d4]:sw t6, 536(t1)
Current Store : [0x800055d8] : sw a0, 540(t1) -- Store: [0x80013200]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000560c]:feq.h t6, ft11, ft10
	-[0x80005610]:csrrs a0, fcsr, zero
	-[0x80005614]:sw t6, 544(t1)
Current Store : [0x80005618] : sw a0, 548(t1) -- Store: [0x80013208]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000564c]:feq.h t6, ft11, ft10
	-[0x80005650]:csrrs a0, fcsr, zero
	-[0x80005654]:sw t6, 552(t1)
Current Store : [0x80005658] : sw a0, 556(t1) -- Store: [0x80013210]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000568c]:feq.h t6, ft11, ft10
	-[0x80005690]:csrrs a0, fcsr, zero
	-[0x80005694]:sw t6, 560(t1)
Current Store : [0x80005698] : sw a0, 564(t1) -- Store: [0x80013218]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800056cc]:feq.h t6, ft11, ft10
	-[0x800056d0]:csrrs a0, fcsr, zero
	-[0x800056d4]:sw t6, 568(t1)
Current Store : [0x800056d8] : sw a0, 572(t1) -- Store: [0x80013220]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000570c]:feq.h t6, ft11, ft10
	-[0x80005710]:csrrs a0, fcsr, zero
	-[0x80005714]:sw t6, 576(t1)
Current Store : [0x80005718] : sw a0, 580(t1) -- Store: [0x80013228]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000574c]:feq.h t6, ft11, ft10
	-[0x80005750]:csrrs a0, fcsr, zero
	-[0x80005754]:sw t6, 584(t1)
Current Store : [0x80005758] : sw a0, 588(t1) -- Store: [0x80013230]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000578c]:feq.h t6, ft11, ft10
	-[0x80005790]:csrrs a0, fcsr, zero
	-[0x80005794]:sw t6, 592(t1)
Current Store : [0x80005798] : sw a0, 596(t1) -- Store: [0x80013238]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800057cc]:feq.h t6, ft11, ft10
	-[0x800057d0]:csrrs a0, fcsr, zero
	-[0x800057d4]:sw t6, 600(t1)
Current Store : [0x800057d8] : sw a0, 604(t1) -- Store: [0x80013240]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000580c]:feq.h t6, ft11, ft10
	-[0x80005810]:csrrs a0, fcsr, zero
	-[0x80005814]:sw t6, 608(t1)
Current Store : [0x80005818] : sw a0, 612(t1) -- Store: [0x80013248]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x11 and fm1 == 0x103 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000584c]:feq.h t6, ft11, ft10
	-[0x80005850]:csrrs a0, fcsr, zero
	-[0x80005854]:sw t6, 616(t1)
Current Store : [0x80005858] : sw a0, 620(t1) -- Store: [0x80013250]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x103 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000588c]:feq.h t6, ft11, ft10
	-[0x80005890]:csrrs a0, fcsr, zero
	-[0x80005894]:sw t6, 624(t1)
Current Store : [0x80005898] : sw a0, 628(t1) -- Store: [0x80013258]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x11 and fm2 == 0x103 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800058cc]:feq.h t6, ft11, ft10
	-[0x800058d0]:csrrs a0, fcsr, zero
	-[0x800058d4]:sw t6, 632(t1)
Current Store : [0x800058d8] : sw a0, 636(t1) -- Store: [0x80013260]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000590c]:feq.h t6, ft11, ft10
	-[0x80005910]:csrrs a0, fcsr, zero
	-[0x80005914]:sw t6, 640(t1)
Current Store : [0x80005918] : sw a0, 644(t1) -- Store: [0x80013268]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000594c]:feq.h t6, ft11, ft10
	-[0x80005950]:csrrs a0, fcsr, zero
	-[0x80005954]:sw t6, 648(t1)
Current Store : [0x80005958] : sw a0, 652(t1) -- Store: [0x80013270]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1a and fm1 == 0x2b3 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000598c]:feq.h t6, ft11, ft10
	-[0x80005990]:csrrs a0, fcsr, zero
	-[0x80005994]:sw t6, 656(t1)
Current Store : [0x80005998] : sw a0, 660(t1) -- Store: [0x80013278]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1a and fm2 == 0x2b3 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800059cc]:feq.h t6, ft11, ft10
	-[0x800059d0]:csrrs a0, fcsr, zero
	-[0x800059d4]:sw t6, 664(t1)
Current Store : [0x800059d8] : sw a0, 668(t1) -- Store: [0x80013280]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1a and fm1 == 0x2b3 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005a0c]:feq.h t6, ft11, ft10
	-[0x80005a10]:csrrs a0, fcsr, zero
	-[0x80005a14]:sw t6, 672(t1)
Current Store : [0x80005a18] : sw a0, 676(t1) -- Store: [0x80013288]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1a and fm2 == 0x2b3 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005a4c]:feq.h t6, ft11, ft10
	-[0x80005a50]:csrrs a0, fcsr, zero
	-[0x80005a54]:sw t6, 680(t1)
Current Store : [0x80005a58] : sw a0, 684(t1) -- Store: [0x80013290]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005a8c]:feq.h t6, ft11, ft10
	-[0x80005a90]:csrrs a0, fcsr, zero
	-[0x80005a94]:sw t6, 688(t1)
Current Store : [0x80005a98] : sw a0, 692(t1) -- Store: [0x80013298]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005acc]:feq.h t6, ft11, ft10
	-[0x80005ad0]:csrrs a0, fcsr, zero
	-[0x80005ad4]:sw t6, 696(t1)
Current Store : [0x80005ad8] : sw a0, 700(t1) -- Store: [0x800132a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005b0c]:feq.h t6, ft11, ft10
	-[0x80005b10]:csrrs a0, fcsr, zero
	-[0x80005b14]:sw t6, 704(t1)
Current Store : [0x80005b18] : sw a0, 708(t1) -- Store: [0x800132a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005b4c]:feq.h t6, ft11, ft10
	-[0x80005b50]:csrrs a0, fcsr, zero
	-[0x80005b54]:sw t6, 712(t1)
Current Store : [0x80005b58] : sw a0, 716(t1) -- Store: [0x800132b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005b8c]:feq.h t6, ft11, ft10
	-[0x80005b90]:csrrs a0, fcsr, zero
	-[0x80005b94]:sw t6, 720(t1)
Current Store : [0x80005b98] : sw a0, 724(t1) -- Store: [0x800132b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005bcc]:feq.h t6, ft11, ft10
	-[0x80005bd0]:csrrs a0, fcsr, zero
	-[0x80005bd4]:sw t6, 728(t1)
Current Store : [0x80005bd8] : sw a0, 732(t1) -- Store: [0x800132c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005c0c]:feq.h t6, ft11, ft10
	-[0x80005c10]:csrrs a0, fcsr, zero
	-[0x80005c14]:sw t6, 736(t1)
Current Store : [0x80005c18] : sw a0, 740(t1) -- Store: [0x800132c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005c4c]:feq.h t6, ft11, ft10
	-[0x80005c50]:csrrs a0, fcsr, zero
	-[0x80005c54]:sw t6, 744(t1)
Current Store : [0x80005c58] : sw a0, 748(t1) -- Store: [0x800132d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005c8c]:feq.h t6, ft11, ft10
	-[0x80005c90]:csrrs a0, fcsr, zero
	-[0x80005c94]:sw t6, 752(t1)
Current Store : [0x80005c98] : sw a0, 756(t1) -- Store: [0x800132d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005ccc]:feq.h t6, ft11, ft10
	-[0x80005cd0]:csrrs a0, fcsr, zero
	-[0x80005cd4]:sw t6, 760(t1)
Current Store : [0x80005cd8] : sw a0, 764(t1) -- Store: [0x800132e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005d0c]:feq.h t6, ft11, ft10
	-[0x80005d10]:csrrs a0, fcsr, zero
	-[0x80005d14]:sw t6, 768(t1)
Current Store : [0x80005d18] : sw a0, 772(t1) -- Store: [0x800132e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005d4c]:feq.h t6, ft11, ft10
	-[0x80005d50]:csrrs a0, fcsr, zero
	-[0x80005d54]:sw t6, 776(t1)
Current Store : [0x80005d58] : sw a0, 780(t1) -- Store: [0x800132f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005d8c]:feq.h t6, ft11, ft10
	-[0x80005d90]:csrrs a0, fcsr, zero
	-[0x80005d94]:sw t6, 784(t1)
Current Store : [0x80005d98] : sw a0, 788(t1) -- Store: [0x800132f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005dcc]:feq.h t6, ft11, ft10
	-[0x80005dd0]:csrrs a0, fcsr, zero
	-[0x80005dd4]:sw t6, 792(t1)
Current Store : [0x80005dd8] : sw a0, 796(t1) -- Store: [0x80013300]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005e0c]:feq.h t6, ft11, ft10
	-[0x80005e10]:csrrs a0, fcsr, zero
	-[0x80005e14]:sw t6, 800(t1)
Current Store : [0x80005e18] : sw a0, 804(t1) -- Store: [0x80013308]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005e4c]:feq.h t6, ft11, ft10
	-[0x80005e50]:csrrs a0, fcsr, zero
	-[0x80005e54]:sw t6, 808(t1)
Current Store : [0x80005e58] : sw a0, 812(t1) -- Store: [0x80013310]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005e8c]:feq.h t6, ft11, ft10
	-[0x80005e90]:csrrs a0, fcsr, zero
	-[0x80005e94]:sw t6, 816(t1)
Current Store : [0x80005e98] : sw a0, 820(t1) -- Store: [0x80013318]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005ecc]:feq.h t6, ft11, ft10
	-[0x80005ed0]:csrrs a0, fcsr, zero
	-[0x80005ed4]:sw t6, 824(t1)
Current Store : [0x80005ed8] : sw a0, 828(t1) -- Store: [0x80013320]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005f0c]:feq.h t6, ft11, ft10
	-[0x80005f10]:csrrs a0, fcsr, zero
	-[0x80005f14]:sw t6, 832(t1)
Current Store : [0x80005f18] : sw a0, 836(t1) -- Store: [0x80013328]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005f4c]:feq.h t6, ft11, ft10
	-[0x80005f50]:csrrs a0, fcsr, zero
	-[0x80005f54]:sw t6, 840(t1)
Current Store : [0x80005f58] : sw a0, 844(t1) -- Store: [0x80013330]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005f8c]:feq.h t6, ft11, ft10
	-[0x80005f90]:csrrs a0, fcsr, zero
	-[0x80005f94]:sw t6, 848(t1)
Current Store : [0x80005f98] : sw a0, 852(t1) -- Store: [0x80013338]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005fcc]:feq.h t6, ft11, ft10
	-[0x80005fd0]:csrrs a0, fcsr, zero
	-[0x80005fd4]:sw t6, 856(t1)
Current Store : [0x80005fd8] : sw a0, 860(t1) -- Store: [0x80013340]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000600c]:feq.h t6, ft11, ft10
	-[0x80006010]:csrrs a0, fcsr, zero
	-[0x80006014]:sw t6, 864(t1)
Current Store : [0x80006018] : sw a0, 868(t1) -- Store: [0x80013348]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000604c]:feq.h t6, ft11, ft10
	-[0x80006050]:csrrs a0, fcsr, zero
	-[0x80006054]:sw t6, 872(t1)
Current Store : [0x80006058] : sw a0, 876(t1) -- Store: [0x80013350]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x039 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000608c]:feq.h t6, ft11, ft10
	-[0x80006090]:csrrs a0, fcsr, zero
	-[0x80006094]:sw t6, 880(t1)
Current Store : [0x80006098] : sw a0, 884(t1) -- Store: [0x80013358]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x039 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800060cc]:feq.h t6, ft11, ft10
	-[0x800060d0]:csrrs a0, fcsr, zero
	-[0x800060d4]:sw t6, 888(t1)
Current Store : [0x800060d8] : sw a0, 892(t1) -- Store: [0x80013360]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x039 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000610c]:feq.h t6, ft11, ft10
	-[0x80006110]:csrrs a0, fcsr, zero
	-[0x80006114]:sw t6, 896(t1)
Current Store : [0x80006118] : sw a0, 900(t1) -- Store: [0x80013368]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x039 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000614c]:feq.h t6, ft11, ft10
	-[0x80006150]:csrrs a0, fcsr, zero
	-[0x80006154]:sw t6, 904(t1)
Current Store : [0x80006158] : sw a0, 908(t1) -- Store: [0x80013370]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000618c]:feq.h t6, ft11, ft10
	-[0x80006190]:csrrs a0, fcsr, zero
	-[0x80006194]:sw t6, 912(t1)
Current Store : [0x80006198] : sw a0, 916(t1) -- Store: [0x80013378]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800061cc]:feq.h t6, ft11, ft10
	-[0x800061d0]:csrrs a0, fcsr, zero
	-[0x800061d4]:sw t6, 920(t1)
Current Store : [0x800061d8] : sw a0, 924(t1) -- Store: [0x80013380]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000620c]:feq.h t6, ft11, ft10
	-[0x80006210]:csrrs a0, fcsr, zero
	-[0x80006214]:sw t6, 928(t1)
Current Store : [0x80006218] : sw a0, 932(t1) -- Store: [0x80013388]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000624c]:feq.h t6, ft11, ft10
	-[0x80006250]:csrrs a0, fcsr, zero
	-[0x80006254]:sw t6, 936(t1)
Current Store : [0x80006258] : sw a0, 940(t1) -- Store: [0x80013390]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000628c]:feq.h t6, ft11, ft10
	-[0x80006290]:csrrs a0, fcsr, zero
	-[0x80006294]:sw t6, 944(t1)
Current Store : [0x80006298] : sw a0, 948(t1) -- Store: [0x80013398]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800062cc]:feq.h t6, ft11, ft10
	-[0x800062d0]:csrrs a0, fcsr, zero
	-[0x800062d4]:sw t6, 952(t1)
Current Store : [0x800062d8] : sw a0, 956(t1) -- Store: [0x800133a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000630c]:feq.h t6, ft11, ft10
	-[0x80006310]:csrrs a0, fcsr, zero
	-[0x80006314]:sw t6, 960(t1)
Current Store : [0x80006318] : sw a0, 964(t1) -- Store: [0x800133a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000634c]:feq.h t6, ft11, ft10
	-[0x80006350]:csrrs a0, fcsr, zero
	-[0x80006354]:sw t6, 968(t1)
Current Store : [0x80006358] : sw a0, 972(t1) -- Store: [0x800133b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000638c]:feq.h t6, ft11, ft10
	-[0x80006390]:csrrs a0, fcsr, zero
	-[0x80006394]:sw t6, 976(t1)
Current Store : [0x80006398] : sw a0, 980(t1) -- Store: [0x800133b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800063cc]:feq.h t6, ft11, ft10
	-[0x800063d0]:csrrs a0, fcsr, zero
	-[0x800063d4]:sw t6, 984(t1)
Current Store : [0x800063d8] : sw a0, 988(t1) -- Store: [0x800133c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000640c]:feq.h t6, ft11, ft10
	-[0x80006410]:csrrs a0, fcsr, zero
	-[0x80006414]:sw t6, 992(t1)
Current Store : [0x80006418] : sw a0, 996(t1) -- Store: [0x800133c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006444]:feq.h t6, ft11, ft10
	-[0x80006448]:csrrs a0, fcsr, zero
	-[0x8000644c]:sw t6, 1000(t1)
Current Store : [0x80006450] : sw a0, 1004(t1) -- Store: [0x800133d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000647c]:feq.h t6, ft11, ft10
	-[0x80006480]:csrrs a0, fcsr, zero
	-[0x80006484]:sw t6, 1008(t1)
Current Store : [0x80006488] : sw a0, 1012(t1) -- Store: [0x800133d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x10 and fm1 == 0x2dc and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800064b4]:feq.h t6, ft11, ft10
	-[0x800064b8]:csrrs a0, fcsr, zero
	-[0x800064bc]:sw t6, 1016(t1)
Current Store : [0x800064c0] : sw a0, 1020(t1) -- Store: [0x800133e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x2dc and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800064f4]:feq.h t6, ft11, ft10
	-[0x800064f8]:csrrs a0, fcsr, zero
	-[0x800064fc]:sw t6, 0(t1)
Current Store : [0x80006500] : sw a0, 4(t1) -- Store: [0x800133e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x10 and fm2 == 0x2dc and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000652c]:feq.h t6, ft11, ft10
	-[0x80006530]:csrrs a0, fcsr, zero
	-[0x80006534]:sw t6, 8(t1)
Current Store : [0x80006538] : sw a0, 12(t1) -- Store: [0x800133f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006564]:feq.h t6, ft11, ft10
	-[0x80006568]:csrrs a0, fcsr, zero
	-[0x8000656c]:sw t6, 16(t1)
Current Store : [0x80006570] : sw a0, 20(t1) -- Store: [0x800133f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000659c]:feq.h t6, ft11, ft10
	-[0x800065a0]:csrrs a0, fcsr, zero
	-[0x800065a4]:sw t6, 24(t1)
Current Store : [0x800065a8] : sw a0, 28(t1) -- Store: [0x80013400]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800065d4]:feq.h t6, ft11, ft10
	-[0x800065d8]:csrrs a0, fcsr, zero
	-[0x800065dc]:sw t6, 32(t1)
Current Store : [0x800065e0] : sw a0, 36(t1) -- Store: [0x80013408]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000660c]:feq.h t6, ft11, ft10
	-[0x80006610]:csrrs a0, fcsr, zero
	-[0x80006614]:sw t6, 40(t1)
Current Store : [0x80006618] : sw a0, 44(t1) -- Store: [0x80013410]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006644]:feq.h t6, ft11, ft10
	-[0x80006648]:csrrs a0, fcsr, zero
	-[0x8000664c]:sw t6, 48(t1)
Current Store : [0x80006650] : sw a0, 52(t1) -- Store: [0x80013418]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000667c]:feq.h t6, ft11, ft10
	-[0x80006680]:csrrs a0, fcsr, zero
	-[0x80006684]:sw t6, 56(t1)
Current Store : [0x80006688] : sw a0, 60(t1) -- Store: [0x80013420]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800066b4]:feq.h t6, ft11, ft10
	-[0x800066b8]:csrrs a0, fcsr, zero
	-[0x800066bc]:sw t6, 64(t1)
Current Store : [0x800066c0] : sw a0, 68(t1) -- Store: [0x80013428]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800066ec]:feq.h t6, ft11, ft10
	-[0x800066f0]:csrrs a0, fcsr, zero
	-[0x800066f4]:sw t6, 72(t1)
Current Store : [0x800066f8] : sw a0, 76(t1) -- Store: [0x80013430]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006724]:feq.h t6, ft11, ft10
	-[0x80006728]:csrrs a0, fcsr, zero
	-[0x8000672c]:sw t6, 80(t1)
Current Store : [0x80006730] : sw a0, 84(t1) -- Store: [0x80013438]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000675c]:feq.h t6, ft11, ft10
	-[0x80006760]:csrrs a0, fcsr, zero
	-[0x80006764]:sw t6, 88(t1)
Current Store : [0x80006768] : sw a0, 92(t1) -- Store: [0x80013440]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006794]:feq.h t6, ft11, ft10
	-[0x80006798]:csrrs a0, fcsr, zero
	-[0x8000679c]:sw t6, 96(t1)
Current Store : [0x800067a0] : sw a0, 100(t1) -- Store: [0x80013448]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800067cc]:feq.h t6, ft11, ft10
	-[0x800067d0]:csrrs a0, fcsr, zero
	-[0x800067d4]:sw t6, 104(t1)
Current Store : [0x800067d8] : sw a0, 108(t1) -- Store: [0x80013450]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006804]:feq.h t6, ft11, ft10
	-[0x80006808]:csrrs a0, fcsr, zero
	-[0x8000680c]:sw t6, 112(t1)
Current Store : [0x80006810] : sw a0, 116(t1) -- Store: [0x80013458]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000683c]:feq.h t6, ft11, ft10
	-[0x80006840]:csrrs a0, fcsr, zero
	-[0x80006844]:sw t6, 120(t1)
Current Store : [0x80006848] : sw a0, 124(t1) -- Store: [0x80013460]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006874]:feq.h t6, ft11, ft10
	-[0x80006878]:csrrs a0, fcsr, zero
	-[0x8000687c]:sw t6, 128(t1)
Current Store : [0x80006880] : sw a0, 132(t1) -- Store: [0x80013468]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800068ac]:feq.h t6, ft11, ft10
	-[0x800068b0]:csrrs a0, fcsr, zero
	-[0x800068b4]:sw t6, 136(t1)
Current Store : [0x800068b8] : sw a0, 140(t1) -- Store: [0x80013470]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800068e4]:feq.h t6, ft11, ft10
	-[0x800068e8]:csrrs a0, fcsr, zero
	-[0x800068ec]:sw t6, 144(t1)
Current Store : [0x800068f0] : sw a0, 148(t1) -- Store: [0x80013478]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000691c]:feq.h t6, ft11, ft10
	-[0x80006920]:csrrs a0, fcsr, zero
	-[0x80006924]:sw t6, 152(t1)
Current Store : [0x80006928] : sw a0, 156(t1) -- Store: [0x80013480]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006954]:feq.h t6, ft11, ft10
	-[0x80006958]:csrrs a0, fcsr, zero
	-[0x8000695c]:sw t6, 160(t1)
Current Store : [0x80006960] : sw a0, 164(t1) -- Store: [0x80013488]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000698c]:feq.h t6, ft11, ft10
	-[0x80006990]:csrrs a0, fcsr, zero
	-[0x80006994]:sw t6, 168(t1)
Current Store : [0x80006998] : sw a0, 172(t1) -- Store: [0x80013490]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800069c4]:feq.h t6, ft11, ft10
	-[0x800069c8]:csrrs a0, fcsr, zero
	-[0x800069cc]:sw t6, 176(t1)
Current Store : [0x800069d0] : sw a0, 180(t1) -- Store: [0x80013498]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x1a and fm2 == 0x069 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800069fc]:feq.h t6, ft11, ft10
	-[0x80006a00]:csrrs a0, fcsr, zero
	-[0x80006a04]:sw t6, 184(t1)
Current Store : [0x80006a08] : sw a0, 188(t1) -- Store: [0x800134a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1a and fm1 == 0x069 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006a34]:feq.h t6, ft11, ft10
	-[0x80006a38]:csrrs a0, fcsr, zero
	-[0x80006a3c]:sw t6, 192(t1)
Current Store : [0x80006a40] : sw a0, 196(t1) -- Store: [0x800134a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006a6c]:feq.h t6, ft11, ft10
	-[0x80006a70]:csrrs a0, fcsr, zero
	-[0x80006a74]:sw t6, 200(t1)
Current Store : [0x80006a78] : sw a0, 204(t1) -- Store: [0x800134b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006aa4]:feq.h t6, ft11, ft10
	-[0x80006aa8]:csrrs a0, fcsr, zero
	-[0x80006aac]:sw t6, 208(t1)
Current Store : [0x80006ab0] : sw a0, 212(t1) -- Store: [0x800134b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006adc]:feq.h t6, ft11, ft10
	-[0x80006ae0]:csrrs a0, fcsr, zero
	-[0x80006ae4]:sw t6, 216(t1)
Current Store : [0x80006ae8] : sw a0, 220(t1) -- Store: [0x800134c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x035 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006b14]:feq.h t6, ft11, ft10
	-[0x80006b18]:csrrs a0, fcsr, zero
	-[0x80006b1c]:sw t6, 224(t1)
Current Store : [0x80006b20] : sw a0, 228(t1) -- Store: [0x800134c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x035 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006b4c]:feq.h t6, ft11, ft10
	-[0x80006b50]:csrrs a0, fcsr, zero
	-[0x80006b54]:sw t6, 232(t1)
Current Store : [0x80006b58] : sw a0, 236(t1) -- Store: [0x800134d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006b84]:feq.h t6, ft11, ft10
	-[0x80006b88]:csrrs a0, fcsr, zero
	-[0x80006b8c]:sw t6, 240(t1)
Current Store : [0x80006b90] : sw a0, 244(t1) -- Store: [0x800134d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006bbc]:feq.h t6, ft11, ft10
	-[0x80006bc0]:csrrs a0, fcsr, zero
	-[0x80006bc4]:sw t6, 248(t1)
Current Store : [0x80006bc8] : sw a0, 252(t1) -- Store: [0x800134e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006bf4]:feq.h t6, ft11, ft10
	-[0x80006bf8]:csrrs a0, fcsr, zero
	-[0x80006bfc]:sw t6, 256(t1)
Current Store : [0x80006c00] : sw a0, 260(t1) -- Store: [0x800134e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x1b and fm2 == 0x1ed and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006c2c]:feq.h t6, ft11, ft10
	-[0x80006c30]:csrrs a0, fcsr, zero
	-[0x80006c34]:sw t6, 264(t1)
Current Store : [0x80006c38] : sw a0, 268(t1) -- Store: [0x800134f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1b and fm1 == 0x1ed and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006c64]:feq.h t6, ft11, ft10
	-[0x80006c68]:csrrs a0, fcsr, zero
	-[0x80006c6c]:sw t6, 272(t1)
Current Store : [0x80006c70] : sw a0, 276(t1) -- Store: [0x800134f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006c9c]:feq.h t6, ft11, ft10
	-[0x80006ca0]:csrrs a0, fcsr, zero
	-[0x80006ca4]:sw t6, 280(t1)
Current Store : [0x80006ca8] : sw a0, 284(t1) -- Store: [0x80013500]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006cd4]:feq.h t6, ft11, ft10
	-[0x80006cd8]:csrrs a0, fcsr, zero
	-[0x80006cdc]:sw t6, 288(t1)
Current Store : [0x80006ce0] : sw a0, 292(t1) -- Store: [0x80013508]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x1a and fm2 == 0x39d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006d0c]:feq.h t6, ft11, ft10
	-[0x80006d10]:csrrs a0, fcsr, zero
	-[0x80006d14]:sw t6, 296(t1)
Current Store : [0x80006d18] : sw a0, 300(t1) -- Store: [0x80013510]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1a and fm1 == 0x39d and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006d44]:feq.h t6, ft11, ft10
	-[0x80006d48]:csrrs a0, fcsr, zero
	-[0x80006d4c]:sw t6, 304(t1)
Current Store : [0x80006d50] : sw a0, 308(t1) -- Store: [0x80013518]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006d7c]:feq.h t6, ft11, ft10
	-[0x80006d80]:csrrs a0, fcsr, zero
	-[0x80006d84]:sw t6, 312(t1)
Current Store : [0x80006d88] : sw a0, 316(t1) -- Store: [0x80013520]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006db4]:feq.h t6, ft11, ft10
	-[0x80006db8]:csrrs a0, fcsr, zero
	-[0x80006dbc]:sw t6, 320(t1)
Current Store : [0x80006dc0] : sw a0, 324(t1) -- Store: [0x80013528]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x1a and fm2 == 0x23c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006dec]:feq.h t6, ft11, ft10
	-[0x80006df0]:csrrs a0, fcsr, zero
	-[0x80006df4]:sw t6, 328(t1)
Current Store : [0x80006df8] : sw a0, 332(t1) -- Store: [0x80013530]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1a and fm1 == 0x23c and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006e24]:feq.h t6, ft11, ft10
	-[0x80006e28]:csrrs a0, fcsr, zero
	-[0x80006e2c]:sw t6, 336(t1)
Current Store : [0x80006e30] : sw a0, 340(t1) -- Store: [0x80013538]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006e5c]:feq.h t6, ft11, ft10
	-[0x80006e60]:csrrs a0, fcsr, zero
	-[0x80006e64]:sw t6, 344(t1)
Current Store : [0x80006e68] : sw a0, 348(t1) -- Store: [0x80013540]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006e94]:feq.h t6, ft11, ft10
	-[0x80006e98]:csrrs a0, fcsr, zero
	-[0x80006e9c]:sw t6, 352(t1)
Current Store : [0x80006ea0] : sw a0, 356(t1) -- Store: [0x80013548]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x1a and fm2 == 0x0b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006ecc]:feq.h t6, ft11, ft10
	-[0x80006ed0]:csrrs a0, fcsr, zero
	-[0x80006ed4]:sw t6, 360(t1)
Current Store : [0x80006ed8] : sw a0, 364(t1) -- Store: [0x80013550]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1a and fm1 == 0x0b9 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006f04]:feq.h t6, ft11, ft10
	-[0x80006f08]:csrrs a0, fcsr, zero
	-[0x80006f0c]:sw t6, 368(t1)
Current Store : [0x80006f10] : sw a0, 372(t1) -- Store: [0x80013558]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006f3c]:feq.h t6, ft11, ft10
	-[0x80006f40]:csrrs a0, fcsr, zero
	-[0x80006f44]:sw t6, 376(t1)
Current Store : [0x80006f48] : sw a0, 380(t1) -- Store: [0x80013560]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006f74]:feq.h t6, ft11, ft10
	-[0x80006f78]:csrrs a0, fcsr, zero
	-[0x80006f7c]:sw t6, 384(t1)
Current Store : [0x80006f80] : sw a0, 388(t1) -- Store: [0x80013568]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x091 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x0dd and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006fac]:feq.h t6, ft11, ft10
	-[0x80006fb0]:csrrs a0, fcsr, zero
	-[0x80006fb4]:sw t6, 392(t1)
Current Store : [0x80006fb8] : sw a0, 396(t1) -- Store: [0x80013570]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x0dd and fs2 == 1 and fe2 == 0x00 and fm2 == 0x091 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006fe4]:feq.h t6, ft11, ft10
	-[0x80006fe8]:csrrs a0, fcsr, zero
	-[0x80006fec]:sw t6, 400(t1)
Current Store : [0x80006ff0] : sw a0, 404(t1) -- Store: [0x80013578]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x091 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000701c]:feq.h t6, ft11, ft10
	-[0x80007020]:csrrs a0, fcsr, zero
	-[0x80007024]:sw t6, 408(t1)
Current Store : [0x80007028] : sw a0, 412(t1) -- Store: [0x80013580]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x091 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007054]:feq.h t6, ft11, ft10
	-[0x80007058]:csrrs a0, fcsr, zero
	-[0x8000705c]:sw t6, 416(t1)
Current Store : [0x80007060] : sw a0, 420(t1) -- Store: [0x80013588]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000708c]:feq.h t6, ft11, ft10
	-[0x80007090]:csrrs a0, fcsr, zero
	-[0x80007094]:sw t6, 424(t1)
Current Store : [0x80007098] : sw a0, 428(t1) -- Store: [0x80013590]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x1a and fm2 == 0x250 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800070c4]:feq.h t6, ft11, ft10
	-[0x800070c8]:csrrs a0, fcsr, zero
	-[0x800070cc]:sw t6, 432(t1)
Current Store : [0x800070d0] : sw a0, 436(t1) -- Store: [0x80013598]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1a and fm1 == 0x250 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800070fc]:feq.h t6, ft11, ft10
	-[0x80007100]:csrrs a0, fcsr, zero
	-[0x80007104]:sw t6, 440(t1)
Current Store : [0x80007108] : sw a0, 444(t1) -- Store: [0x800135a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007134]:feq.h t6, ft11, ft10
	-[0x80007138]:csrrs a0, fcsr, zero
	-[0x8000713c]:sw t6, 448(t1)
Current Store : [0x80007140] : sw a0, 452(t1) -- Store: [0x800135a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000716c]:feq.h t6, ft11, ft10
	-[0x80007170]:csrrs a0, fcsr, zero
	-[0x80007174]:sw t6, 456(t1)
Current Store : [0x80007178] : sw a0, 460(t1) -- Store: [0x800135b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x1b and fm2 == 0x10f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800071a4]:feq.h t6, ft11, ft10
	-[0x800071a8]:csrrs a0, fcsr, zero
	-[0x800071ac]:sw t6, 464(t1)
Current Store : [0x800071b0] : sw a0, 468(t1) -- Store: [0x800135b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1b and fm1 == 0x10f and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800071dc]:feq.h t6, ft11, ft10
	-[0x800071e0]:csrrs a0, fcsr, zero
	-[0x800071e4]:sw t6, 472(t1)
Current Store : [0x800071e8] : sw a0, 476(t1) -- Store: [0x800135c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007214]:feq.h t6, ft11, ft10
	-[0x80007218]:csrrs a0, fcsr, zero
	-[0x8000721c]:sw t6, 480(t1)
Current Store : [0x80007220] : sw a0, 484(t1) -- Store: [0x800135c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000724c]:feq.h t6, ft11, ft10
	-[0x80007250]:csrrs a0, fcsr, zero
	-[0x80007254]:sw t6, 488(t1)
Current Store : [0x80007258] : sw a0, 492(t1) -- Store: [0x800135d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x19 and fm2 == 0x22e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007284]:feq.h t6, ft11, ft10
	-[0x80007288]:csrrs a0, fcsr, zero
	-[0x8000728c]:sw t6, 496(t1)
Current Store : [0x80007290] : sw a0, 500(t1) -- Store: [0x800135d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x19 and fm1 == 0x22e and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800072bc]:feq.h t6, ft11, ft10
	-[0x800072c0]:csrrs a0, fcsr, zero
	-[0x800072c4]:sw t6, 504(t1)
Current Store : [0x800072c8] : sw a0, 508(t1) -- Store: [0x800135e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800072f4]:feq.h t6, ft11, ft10
	-[0x800072f8]:csrrs a0, fcsr, zero
	-[0x800072fc]:sw t6, 512(t1)
Current Store : [0x80007300] : sw a0, 516(t1) -- Store: [0x800135e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000732c]:feq.h t6, ft11, ft10
	-[0x80007330]:csrrs a0, fcsr, zero
	-[0x80007334]:sw t6, 520(t1)
Current Store : [0x80007338] : sw a0, 524(t1) -- Store: [0x800135f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x12 and fm1 == 0x052 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007364]:feq.h t6, ft11, ft10
	-[0x80007368]:csrrs a0, fcsr, zero
	-[0x8000736c]:sw t6, 528(t1)
Current Store : [0x80007370] : sw a0, 532(t1) -- Store: [0x800135f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x12 and fm2 == 0x052 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000739c]:feq.h t6, ft11, ft10
	-[0x800073a0]:csrrs a0, fcsr, zero
	-[0x800073a4]:sw t6, 536(t1)
Current Store : [0x800073a8] : sw a0, 540(t1) -- Store: [0x80013600]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x12 and fm2 == 0x052 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800073d4]:feq.h t6, ft11, ft10
	-[0x800073d8]:csrrs a0, fcsr, zero
	-[0x800073dc]:sw t6, 544(t1)
Current Store : [0x800073e0] : sw a0, 548(t1) -- Store: [0x80013608]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000740c]:feq.h t6, ft11, ft10
	-[0x80007410]:csrrs a0, fcsr, zero
	-[0x80007414]:sw t6, 552(t1)
Current Store : [0x80007418] : sw a0, 556(t1) -- Store: [0x80013610]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007444]:feq.h t6, ft11, ft10
	-[0x80007448]:csrrs a0, fcsr, zero
	-[0x8000744c]:sw t6, 560(t1)
Current Store : [0x80007450] : sw a0, 564(t1) -- Store: [0x80013618]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000747c]:feq.h t6, ft11, ft10
	-[0x80007480]:csrrs a0, fcsr, zero
	-[0x80007484]:sw t6, 568(t1)
Current Store : [0x80007488] : sw a0, 572(t1) -- Store: [0x80013620]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800074b4]:feq.h t6, ft11, ft10
	-[0x800074b8]:csrrs a0, fcsr, zero
	-[0x800074bc]:sw t6, 576(t1)
Current Store : [0x800074c0] : sw a0, 580(t1) -- Store: [0x80013628]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800074ec]:feq.h t6, ft11, ft10
	-[0x800074f0]:csrrs a0, fcsr, zero
	-[0x800074f4]:sw t6, 584(t1)
Current Store : [0x800074f8] : sw a0, 588(t1) -- Store: [0x80013630]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007524]:feq.h t6, ft11, ft10
	-[0x80007528]:csrrs a0, fcsr, zero
	-[0x8000752c]:sw t6, 592(t1)
Current Store : [0x80007530] : sw a0, 596(t1) -- Store: [0x80013638]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000755c]:feq.h t6, ft11, ft10
	-[0x80007560]:csrrs a0, fcsr, zero
	-[0x80007564]:sw t6, 600(t1)
Current Store : [0x80007568] : sw a0, 604(t1) -- Store: [0x80013640]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007594]:feq.h t6, ft11, ft10
	-[0x80007598]:csrrs a0, fcsr, zero
	-[0x8000759c]:sw t6, 608(t1)
Current Store : [0x800075a0] : sw a0, 612(t1) -- Store: [0x80013648]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800075cc]:feq.h t6, ft11, ft10
	-[0x800075d0]:csrrs a0, fcsr, zero
	-[0x800075d4]:sw t6, 616(t1)
Current Store : [0x800075d8] : sw a0, 620(t1) -- Store: [0x80013650]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007604]:feq.h t6, ft11, ft10
	-[0x80007608]:csrrs a0, fcsr, zero
	-[0x8000760c]:sw t6, 624(t1)
Current Store : [0x80007610] : sw a0, 628(t1) -- Store: [0x80013658]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000763c]:feq.h t6, ft11, ft10
	-[0x80007640]:csrrs a0, fcsr, zero
	-[0x80007644]:sw t6, 632(t1)
Current Store : [0x80007648] : sw a0, 636(t1) -- Store: [0x80013660]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007674]:feq.h t6, ft11, ft10
	-[0x80007678]:csrrs a0, fcsr, zero
	-[0x8000767c]:sw t6, 640(t1)
Current Store : [0x80007680] : sw a0, 644(t1) -- Store: [0x80013668]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800076ac]:feq.h t6, ft11, ft10
	-[0x800076b0]:csrrs a0, fcsr, zero
	-[0x800076b4]:sw t6, 648(t1)
Current Store : [0x800076b8] : sw a0, 652(t1) -- Store: [0x80013670]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800076e4]:feq.h t6, ft11, ft10
	-[0x800076e8]:csrrs a0, fcsr, zero
	-[0x800076ec]:sw t6, 656(t1)
Current Store : [0x800076f0] : sw a0, 660(t1) -- Store: [0x80013678]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000771c]:feq.h t6, ft11, ft10
	-[0x80007720]:csrrs a0, fcsr, zero
	-[0x80007724]:sw t6, 664(t1)
Current Store : [0x80007728] : sw a0, 668(t1) -- Store: [0x80013680]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007754]:feq.h t6, ft11, ft10
	-[0x80007758]:csrrs a0, fcsr, zero
	-[0x8000775c]:sw t6, 672(t1)
Current Store : [0x80007760] : sw a0, 676(t1) -- Store: [0x80013688]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000778c]:feq.h t6, ft11, ft10
	-[0x80007790]:csrrs a0, fcsr, zero
	-[0x80007794]:sw t6, 680(t1)
Current Store : [0x80007798] : sw a0, 684(t1) -- Store: [0x80013690]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800077c4]:feq.h t6, ft11, ft10
	-[0x800077c8]:csrrs a0, fcsr, zero
	-[0x800077cc]:sw t6, 688(t1)
Current Store : [0x800077d0] : sw a0, 692(t1) -- Store: [0x80013698]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800077fc]:feq.h t6, ft11, ft10
	-[0x80007800]:csrrs a0, fcsr, zero
	-[0x80007804]:sw t6, 696(t1)
Current Store : [0x80007808] : sw a0, 700(t1) -- Store: [0x800136a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007834]:feq.h t6, ft11, ft10
	-[0x80007838]:csrrs a0, fcsr, zero
	-[0x8000783c]:sw t6, 704(t1)
Current Store : [0x80007840] : sw a0, 708(t1) -- Store: [0x800136a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000786c]:feq.h t6, ft11, ft10
	-[0x80007870]:csrrs a0, fcsr, zero
	-[0x80007874]:sw t6, 712(t1)
Current Store : [0x80007878] : sw a0, 716(t1) -- Store: [0x800136b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1a and fm1 == 0x069 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800078a4]:feq.h t6, ft11, ft10
	-[0x800078a8]:csrrs a0, fcsr, zero
	-[0x800078ac]:sw t6, 720(t1)
Current Store : [0x800078b0] : sw a0, 724(t1) -- Store: [0x800136b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1a and fm2 == 0x069 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800078dc]:feq.h t6, ft11, ft10
	-[0x800078e0]:csrrs a0, fcsr, zero
	-[0x800078e4]:sw t6, 728(t1)
Current Store : [0x800078e8] : sw a0, 732(t1) -- Store: [0x800136c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007914]:feq.h t6, ft11, ft10
	-[0x80007918]:csrrs a0, fcsr, zero
	-[0x8000791c]:sw t6, 736(t1)
Current Store : [0x80007920] : sw a0, 740(t1) -- Store: [0x800136c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x003 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000794c]:feq.h t6, ft11, ft10
	-[0x80007950]:csrrs a0, fcsr, zero
	-[0x80007954]:sw t6, 744(t1)
Current Store : [0x80007958] : sw a0, 748(t1) -- Store: [0x800136d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x003 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007984]:feq.h t6, ft11, ft10
	-[0x80007988]:csrrs a0, fcsr, zero
	-[0x8000798c]:sw t6, 752(t1)
Current Store : [0x80007990] : sw a0, 756(t1) -- Store: [0x800136d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x003 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800079bc]:feq.h t6, ft11, ft10
	-[0x800079c0]:csrrs a0, fcsr, zero
	-[0x800079c4]:sw t6, 760(t1)
Current Store : [0x800079c8] : sw a0, 764(t1) -- Store: [0x800136e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x003 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800079f4]:feq.h t6, ft11, ft10
	-[0x800079f8]:csrrs a0, fcsr, zero
	-[0x800079fc]:sw t6, 768(t1)
Current Store : [0x80007a00] : sw a0, 772(t1) -- Store: [0x800136e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007a2c]:feq.h t6, ft11, ft10
	-[0x80007a30]:csrrs a0, fcsr, zero
	-[0x80007a34]:sw t6, 776(t1)
Current Store : [0x80007a38] : sw a0, 780(t1) -- Store: [0x800136f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007a64]:feq.h t6, ft11, ft10
	-[0x80007a68]:csrrs a0, fcsr, zero
	-[0x80007a6c]:sw t6, 784(t1)
Current Store : [0x80007a70] : sw a0, 788(t1) -- Store: [0x800136f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007a9c]:feq.h t6, ft11, ft10
	-[0x80007aa0]:csrrs a0, fcsr, zero
	-[0x80007aa4]:sw t6, 792(t1)
Current Store : [0x80007aa8] : sw a0, 796(t1) -- Store: [0x80013700]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007ad4]:feq.h t6, ft11, ft10
	-[0x80007ad8]:csrrs a0, fcsr, zero
	-[0x80007adc]:sw t6, 800(t1)
Current Store : [0x80007ae0] : sw a0, 804(t1) -- Store: [0x80013708]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007b0c]:feq.h t6, ft11, ft10
	-[0x80007b10]:csrrs a0, fcsr, zero
	-[0x80007b14]:sw t6, 808(t1)
Current Store : [0x80007b18] : sw a0, 812(t1) -- Store: [0x80013710]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007b44]:feq.h t6, ft11, ft10
	-[0x80007b48]:csrrs a0, fcsr, zero
	-[0x80007b4c]:sw t6, 816(t1)
Current Store : [0x80007b50] : sw a0, 820(t1) -- Store: [0x80013718]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007b7c]:feq.h t6, ft11, ft10
	-[0x80007b80]:csrrs a0, fcsr, zero
	-[0x80007b84]:sw t6, 824(t1)
Current Store : [0x80007b88] : sw a0, 828(t1) -- Store: [0x80013720]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007bb4]:feq.h t6, ft11, ft10
	-[0x80007bb8]:csrrs a0, fcsr, zero
	-[0x80007bbc]:sw t6, 832(t1)
Current Store : [0x80007bc0] : sw a0, 836(t1) -- Store: [0x80013728]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007bec]:feq.h t6, ft11, ft10
	-[0x80007bf0]:csrrs a0, fcsr, zero
	-[0x80007bf4]:sw t6, 840(t1)
Current Store : [0x80007bf8] : sw a0, 844(t1) -- Store: [0x80013730]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x025 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007c24]:feq.h t6, ft11, ft10
	-[0x80007c28]:csrrs a0, fcsr, zero
	-[0x80007c2c]:sw t6, 848(t1)
Current Store : [0x80007c30] : sw a0, 852(t1) -- Store: [0x80013738]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007c5c]:feq.h t6, ft11, ft10
	-[0x80007c60]:csrrs a0, fcsr, zero
	-[0x80007c64]:sw t6, 856(t1)
Current Store : [0x80007c68] : sw a0, 860(t1) -- Store: [0x80013740]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007c94]:feq.h t6, ft11, ft10
	-[0x80007c98]:csrrs a0, fcsr, zero
	-[0x80007c9c]:sw t6, 864(t1)
Current Store : [0x80007ca0] : sw a0, 868(t1) -- Store: [0x80013748]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007ccc]:feq.h t6, ft11, ft10
	-[0x80007cd0]:csrrs a0, fcsr, zero
	-[0x80007cd4]:sw t6, 872(t1)
Current Store : [0x80007cd8] : sw a0, 876(t1) -- Store: [0x80013750]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007d04]:feq.h t6, ft11, ft10
	-[0x80007d08]:csrrs a0, fcsr, zero
	-[0x80007d0c]:sw t6, 880(t1)
Current Store : [0x80007d10] : sw a0, 884(t1) -- Store: [0x80013758]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007d3c]:feq.h t6, ft11, ft10
	-[0x80007d40]:csrrs a0, fcsr, zero
	-[0x80007d44]:sw t6, 888(t1)
Current Store : [0x80007d48] : sw a0, 892(t1) -- Store: [0x80013760]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007d74]:feq.h t6, ft11, ft10
	-[0x80007d78]:csrrs a0, fcsr, zero
	-[0x80007d7c]:sw t6, 896(t1)
Current Store : [0x80007d80] : sw a0, 900(t1) -- Store: [0x80013768]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007dac]:feq.h t6, ft11, ft10
	-[0x80007db0]:csrrs a0, fcsr, zero
	-[0x80007db4]:sw t6, 904(t1)
Current Store : [0x80007db8] : sw a0, 908(t1) -- Store: [0x80013770]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007de4]:feq.h t6, ft11, ft10
	-[0x80007de8]:csrrs a0, fcsr, zero
	-[0x80007dec]:sw t6, 912(t1)
Current Store : [0x80007df0] : sw a0, 916(t1) -- Store: [0x80013778]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007e1c]:feq.h t6, ft11, ft10
	-[0x80007e20]:csrrs a0, fcsr, zero
	-[0x80007e24]:sw t6, 920(t1)
Current Store : [0x80007e28] : sw a0, 924(t1) -- Store: [0x80013780]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007e54]:feq.h t6, ft11, ft10
	-[0x80007e58]:csrrs a0, fcsr, zero
	-[0x80007e5c]:sw t6, 928(t1)
Current Store : [0x80007e60] : sw a0, 932(t1) -- Store: [0x80013788]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x10 and fm1 == 0x084 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007e8c]:feq.h t6, ft11, ft10
	-[0x80007e90]:csrrs a0, fcsr, zero
	-[0x80007e94]:sw t6, 936(t1)
Current Store : [0x80007e98] : sw a0, 940(t1) -- Store: [0x80013790]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x10 and fm2 == 0x084 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007ec4]:feq.h t6, ft11, ft10
	-[0x80007ec8]:csrrs a0, fcsr, zero
	-[0x80007ecc]:sw t6, 944(t1)
Current Store : [0x80007ed0] : sw a0, 948(t1) -- Store: [0x80013798]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x10 and fm2 == 0x084 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007efc]:feq.h t6, ft11, ft10
	-[0x80007f00]:csrrs a0, fcsr, zero
	-[0x80007f04]:sw t6, 952(t1)
Current Store : [0x80007f08] : sw a0, 956(t1) -- Store: [0x800137a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007f34]:feq.h t6, ft11, ft10
	-[0x80007f38]:csrrs a0, fcsr, zero
	-[0x80007f3c]:sw t6, 960(t1)
Current Store : [0x80007f40] : sw a0, 964(t1) -- Store: [0x800137a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007f6c]:feq.h t6, ft11, ft10
	-[0x80007f70]:csrrs a0, fcsr, zero
	-[0x80007f74]:sw t6, 968(t1)
Current Store : [0x80007f78] : sw a0, 972(t1) -- Store: [0x800137b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007fa4]:feq.h t6, ft11, ft10
	-[0x80007fa8]:csrrs a0, fcsr, zero
	-[0x80007fac]:sw t6, 976(t1)
Current Store : [0x80007fb0] : sw a0, 980(t1) -- Store: [0x800137b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80007fdc]:feq.h t6, ft11, ft10
	-[0x80007fe0]:csrrs a0, fcsr, zero
	-[0x80007fe4]:sw t6, 984(t1)
Current Store : [0x80007fe8] : sw a0, 988(t1) -- Store: [0x800137c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008014]:feq.h t6, ft11, ft10
	-[0x80008018]:csrrs a0, fcsr, zero
	-[0x8000801c]:sw t6, 992(t1)
Current Store : [0x80008020] : sw a0, 996(t1) -- Store: [0x800137c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000804c]:feq.h t6, ft11, ft10
	-[0x80008050]:csrrs a0, fcsr, zero
	-[0x80008054]:sw t6, 1000(t1)
Current Store : [0x80008058] : sw a0, 1004(t1) -- Store: [0x800137d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008084]:feq.h t6, ft11, ft10
	-[0x80008088]:csrrs a0, fcsr, zero
	-[0x8000808c]:sw t6, 1008(t1)
Current Store : [0x80008090] : sw a0, 1012(t1) -- Store: [0x800137d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800080bc]:feq.h t6, ft11, ft10
	-[0x800080c0]:csrrs a0, fcsr, zero
	-[0x800080c4]:sw t6, 1016(t1)
Current Store : [0x800080c8] : sw a0, 1020(t1) -- Store: [0x800137e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800080fc]:feq.h t6, ft11, ft10
	-[0x80008100]:csrrs a0, fcsr, zero
	-[0x80008104]:sw t6, 0(t1)
Current Store : [0x80008108] : sw a0, 4(t1) -- Store: [0x800137e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008134]:feq.h t6, ft11, ft10
	-[0x80008138]:csrrs a0, fcsr, zero
	-[0x8000813c]:sw t6, 8(t1)
Current Store : [0x80008140] : sw a0, 12(t1) -- Store: [0x800137f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000816c]:feq.h t6, ft11, ft10
	-[0x80008170]:csrrs a0, fcsr, zero
	-[0x80008174]:sw t6, 16(t1)
Current Store : [0x80008178] : sw a0, 20(t1) -- Store: [0x800137f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800081a4]:feq.h t6, ft11, ft10
	-[0x800081a8]:csrrs a0, fcsr, zero
	-[0x800081ac]:sw t6, 24(t1)
Current Store : [0x800081b0] : sw a0, 28(t1) -- Store: [0x80013800]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800081dc]:feq.h t6, ft11, ft10
	-[0x800081e0]:csrrs a0, fcsr, zero
	-[0x800081e4]:sw t6, 32(t1)
Current Store : [0x800081e8] : sw a0, 36(t1) -- Store: [0x80013808]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008214]:feq.h t6, ft11, ft10
	-[0x80008218]:csrrs a0, fcsr, zero
	-[0x8000821c]:sw t6, 40(t1)
Current Store : [0x80008220] : sw a0, 44(t1) -- Store: [0x80013810]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000824c]:feq.h t6, ft11, ft10
	-[0x80008250]:csrrs a0, fcsr, zero
	-[0x80008254]:sw t6, 48(t1)
Current Store : [0x80008258] : sw a0, 52(t1) -- Store: [0x80013818]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008284]:feq.h t6, ft11, ft10
	-[0x80008288]:csrrs a0, fcsr, zero
	-[0x8000828c]:sw t6, 56(t1)
Current Store : [0x80008290] : sw a0, 60(t1) -- Store: [0x80013820]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800082bc]:feq.h t6, ft11, ft10
	-[0x800082c0]:csrrs a0, fcsr, zero
	-[0x800082c4]:sw t6, 64(t1)
Current Store : [0x800082c8] : sw a0, 68(t1) -- Store: [0x80013828]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800082f4]:feq.h t6, ft11, ft10
	-[0x800082f8]:csrrs a0, fcsr, zero
	-[0x800082fc]:sw t6, 72(t1)
Current Store : [0x80008300] : sw a0, 76(t1) -- Store: [0x80013830]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000832c]:feq.h t6, ft11, ft10
	-[0x80008330]:csrrs a0, fcsr, zero
	-[0x80008334]:sw t6, 80(t1)
Current Store : [0x80008338] : sw a0, 84(t1) -- Store: [0x80013838]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008364]:feq.h t6, ft11, ft10
	-[0x80008368]:csrrs a0, fcsr, zero
	-[0x8000836c]:sw t6, 88(t1)
Current Store : [0x80008370] : sw a0, 92(t1) -- Store: [0x80013840]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000839c]:feq.h t6, ft11, ft10
	-[0x800083a0]:csrrs a0, fcsr, zero
	-[0x800083a4]:sw t6, 96(t1)
Current Store : [0x800083a8] : sw a0, 100(t1) -- Store: [0x80013848]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x035 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800083d4]:feq.h t6, ft11, ft10
	-[0x800083d8]:csrrs a0, fcsr, zero
	-[0x800083dc]:sw t6, 104(t1)
Current Store : [0x800083e0] : sw a0, 108(t1) -- Store: [0x80013850]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x035 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000840c]:feq.h t6, ft11, ft10
	-[0x80008410]:csrrs a0, fcsr, zero
	-[0x80008414]:sw t6, 112(t1)
Current Store : [0x80008418] : sw a0, 116(t1) -- Store: [0x80013858]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008444]:feq.h t6, ft11, ft10
	-[0x80008448]:csrrs a0, fcsr, zero
	-[0x8000844c]:sw t6, 120(t1)
Current Store : [0x80008450] : sw a0, 124(t1) -- Store: [0x80013860]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000847c]:feq.h t6, ft11, ft10
	-[0x80008480]:csrrs a0, fcsr, zero
	-[0x80008484]:sw t6, 128(t1)
Current Store : [0x80008488] : sw a0, 132(t1) -- Store: [0x80013868]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800084b4]:feq.h t6, ft11, ft10
	-[0x800084b8]:csrrs a0, fcsr, zero
	-[0x800084bc]:sw t6, 136(t1)
Current Store : [0x800084c0] : sw a0, 140(t1) -- Store: [0x80013870]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800084ec]:feq.h t6, ft11, ft10
	-[0x800084f0]:csrrs a0, fcsr, zero
	-[0x800084f4]:sw t6, 144(t1)
Current Store : [0x800084f8] : sw a0, 148(t1) -- Store: [0x80013878]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008524]:feq.h t6, ft11, ft10
	-[0x80008528]:csrrs a0, fcsr, zero
	-[0x8000852c]:sw t6, 152(t1)
Current Store : [0x80008530] : sw a0, 156(t1) -- Store: [0x80013880]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00a and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000855c]:feq.h t6, ft11, ft10
	-[0x80008560]:csrrs a0, fcsr, zero
	-[0x80008564]:sw t6, 160(t1)
Current Store : [0x80008568] : sw a0, 164(t1) -- Store: [0x80013888]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008594]:feq.h t6, ft11, ft10
	-[0x80008598]:csrrs a0, fcsr, zero
	-[0x8000859c]:sw t6, 168(t1)
Current Store : [0x800085a0] : sw a0, 172(t1) -- Store: [0x80013890]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800085cc]:feq.h t6, ft11, ft10
	-[0x800085d0]:csrrs a0, fcsr, zero
	-[0x800085d4]:sw t6, 176(t1)
Current Store : [0x800085d8] : sw a0, 180(t1) -- Store: [0x80013898]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008604]:feq.h t6, ft11, ft10
	-[0x80008608]:csrrs a0, fcsr, zero
	-[0x8000860c]:sw t6, 184(t1)
Current Store : [0x80008610] : sw a0, 188(t1) -- Store: [0x800138a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x006 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000863c]:feq.h t6, ft11, ft10
	-[0x80008640]:csrrs a0, fcsr, zero
	-[0x80008644]:sw t6, 192(t1)
Current Store : [0x80008648] : sw a0, 196(t1) -- Store: [0x800138a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008674]:feq.h t6, ft11, ft10
	-[0x80008678]:csrrs a0, fcsr, zero
	-[0x8000867c]:sw t6, 200(t1)
Current Store : [0x80008680] : sw a0, 204(t1) -- Store: [0x800138b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800086ac]:feq.h t6, ft11, ft10
	-[0x800086b0]:csrrs a0, fcsr, zero
	-[0x800086b4]:sw t6, 208(t1)
Current Store : [0x800086b8] : sw a0, 212(t1) -- Store: [0x800138b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800086e4]:feq.h t6, ft11, ft10
	-[0x800086e8]:csrrs a0, fcsr, zero
	-[0x800086ec]:sw t6, 216(t1)
Current Store : [0x800086f0] : sw a0, 220(t1) -- Store: [0x800138c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000871c]:feq.h t6, ft11, ft10
	-[0x80008720]:csrrs a0, fcsr, zero
	-[0x80008724]:sw t6, 224(t1)
Current Store : [0x80008728] : sw a0, 228(t1) -- Store: [0x800138c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008754]:feq.h t6, ft11, ft10
	-[0x80008758]:csrrs a0, fcsr, zero
	-[0x8000875c]:sw t6, 232(t1)
Current Store : [0x80008760] : sw a0, 236(t1) -- Store: [0x800138d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000878c]:feq.h t6, ft11, ft10
	-[0x80008790]:csrrs a0, fcsr, zero
	-[0x80008794]:sw t6, 240(t1)
Current Store : [0x80008798] : sw a0, 244(t1) -- Store: [0x800138d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x004 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800087c4]:feq.h t6, ft11, ft10
	-[0x800087c8]:csrrs a0, fcsr, zero
	-[0x800087cc]:sw t6, 248(t1)
Current Store : [0x800087d0] : sw a0, 252(t1) -- Store: [0x800138e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x004 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800087fc]:feq.h t6, ft11, ft10
	-[0x80008800]:csrrs a0, fcsr, zero
	-[0x80008804]:sw t6, 256(t1)
Current Store : [0x80008808] : sw a0, 260(t1) -- Store: [0x800138e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008834]:feq.h t6, ft11, ft10
	-[0x80008838]:csrrs a0, fcsr, zero
	-[0x8000883c]:sw t6, 264(t1)
Current Store : [0x80008840] : sw a0, 268(t1) -- Store: [0x800138f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000886c]:feq.h t6, ft11, ft10
	-[0x80008870]:csrrs a0, fcsr, zero
	-[0x80008874]:sw t6, 272(t1)
Current Store : [0x80008878] : sw a0, 276(t1) -- Store: [0x800138f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x090 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x010 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800088a4]:feq.h t6, ft11, ft10
	-[0x800088a8]:csrrs a0, fcsr, zero
	-[0x800088ac]:sw t6, 280(t1)
Current Store : [0x800088b0] : sw a0, 284(t1) -- Store: [0x80013900]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x010 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x090 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800088dc]:feq.h t6, ft11, ft10
	-[0x800088e0]:csrrs a0, fcsr, zero
	-[0x800088e4]:sw t6, 288(t1)
Current Store : [0x800088e8] : sw a0, 292(t1) -- Store: [0x80013908]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x090 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008914]:feq.h t6, ft11, ft10
	-[0x80008918]:csrrs a0, fcsr, zero
	-[0x8000891c]:sw t6, 296(t1)
Current Store : [0x80008920] : sw a0, 300(t1) -- Store: [0x80013910]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x090 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000894c]:feq.h t6, ft11, ft10
	-[0x80008950]:csrrs a0, fcsr, zero
	-[0x80008954]:sw t6, 304(t1)
Current Store : [0x80008958] : sw a0, 308(t1) -- Store: [0x80013918]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008984]:feq.h t6, ft11, ft10
	-[0x80008988]:csrrs a0, fcsr, zero
	-[0x8000898c]:sw t6, 312(t1)
Current Store : [0x80008990] : sw a0, 316(t1) -- Store: [0x80013920]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800089bc]:feq.h t6, ft11, ft10
	-[0x800089c0]:csrrs a0, fcsr, zero
	-[0x800089c4]:sw t6, 320(t1)
Current Store : [0x800089c8] : sw a0, 324(t1) -- Store: [0x80013928]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800089f4]:feq.h t6, ft11, ft10
	-[0x800089f8]:csrrs a0, fcsr, zero
	-[0x800089fc]:sw t6, 328(t1)
Current Store : [0x80008a00] : sw a0, 332(t1) -- Store: [0x80013930]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008a2c]:feq.h t6, ft11, ft10
	-[0x80008a30]:csrrs a0, fcsr, zero
	-[0x80008a34]:sw t6, 336(t1)
Current Store : [0x80008a38] : sw a0, 340(t1) -- Store: [0x80013938]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008a64]:feq.h t6, ft11, ft10
	-[0x80008a68]:csrrs a0, fcsr, zero
	-[0x80008a6c]:sw t6, 344(t1)
Current Store : [0x80008a70] : sw a0, 348(t1) -- Store: [0x80013940]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x008 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008a9c]:feq.h t6, ft11, ft10
	-[0x80008aa0]:csrrs a0, fcsr, zero
	-[0x80008aa4]:sw t6, 352(t1)
Current Store : [0x80008aa8] : sw a0, 356(t1) -- Store: [0x80013948]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x008 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008ad4]:feq.h t6, ft11, ft10
	-[0x80008ad8]:csrrs a0, fcsr, zero
	-[0x80008adc]:sw t6, 360(t1)
Current Store : [0x80008ae0] : sw a0, 364(t1) -- Store: [0x80013950]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008b0c]:feq.h t6, ft11, ft10
	-[0x80008b10]:csrrs a0, fcsr, zero
	-[0x80008b14]:sw t6, 368(t1)
Current Store : [0x80008b18] : sw a0, 372(t1) -- Store: [0x80013958]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008b44]:feq.h t6, ft11, ft10
	-[0x80008b48]:csrrs a0, fcsr, zero
	-[0x80008b4c]:sw t6, 376(t1)
Current Store : [0x80008b50] : sw a0, 380(t1) -- Store: [0x80013960]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008b7c]:feq.h t6, ft11, ft10
	-[0x80008b80]:csrrs a0, fcsr, zero
	-[0x80008b84]:sw t6, 384(t1)
Current Store : [0x80008b88] : sw a0, 388(t1) -- Store: [0x80013968]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008bb4]:feq.h t6, ft11, ft10
	-[0x80008bb8]:csrrs a0, fcsr, zero
	-[0x80008bbc]:sw t6, 392(t1)
Current Store : [0x80008bc0] : sw a0, 396(t1) -- Store: [0x80013970]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008bec]:feq.h t6, ft11, ft10
	-[0x80008bf0]:csrrs a0, fcsr, zero
	-[0x80008bf4]:sw t6, 400(t1)
Current Store : [0x80008bf8] : sw a0, 404(t1) -- Store: [0x80013978]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008c24]:feq.h t6, ft11, ft10
	-[0x80008c28]:csrrs a0, fcsr, zero
	-[0x80008c2c]:sw t6, 408(t1)
Current Store : [0x80008c30] : sw a0, 412(t1) -- Store: [0x80013980]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x12 and fm1 == 0x04f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008c5c]:feq.h t6, ft11, ft10
	-[0x80008c60]:csrrs a0, fcsr, zero
	-[0x80008c64]:sw t6, 416(t1)
Current Store : [0x80008c68] : sw a0, 420(t1) -- Store: [0x80013988]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x12 and fm2 == 0x04f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008c94]:feq.h t6, ft11, ft10
	-[0x80008c98]:csrrs a0, fcsr, zero
	-[0x80008c9c]:sw t6, 424(t1)
Current Store : [0x80008ca0] : sw a0, 428(t1) -- Store: [0x80013990]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x12 and fm2 == 0x04f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008ccc]:feq.h t6, ft11, ft10
	-[0x80008cd0]:csrrs a0, fcsr, zero
	-[0x80008cd4]:sw t6, 432(t1)
Current Store : [0x80008cd8] : sw a0, 436(t1) -- Store: [0x80013998]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008d04]:feq.h t6, ft11, ft10
	-[0x80008d08]:csrrs a0, fcsr, zero
	-[0x80008d0c]:sw t6, 440(t1)
Current Store : [0x80008d10] : sw a0, 444(t1) -- Store: [0x800139a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008d3c]:feq.h t6, ft11, ft10
	-[0x80008d40]:csrrs a0, fcsr, zero
	-[0x80008d44]:sw t6, 448(t1)
Current Store : [0x80008d48] : sw a0, 452(t1) -- Store: [0x800139a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008d74]:feq.h t6, ft11, ft10
	-[0x80008d78]:csrrs a0, fcsr, zero
	-[0x80008d7c]:sw t6, 456(t1)
Current Store : [0x80008d80] : sw a0, 460(t1) -- Store: [0x800139b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008dac]:feq.h t6, ft11, ft10
	-[0x80008db0]:csrrs a0, fcsr, zero
	-[0x80008db4]:sw t6, 464(t1)
Current Store : [0x80008db8] : sw a0, 468(t1) -- Store: [0x800139b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008de4]:feq.h t6, ft11, ft10
	-[0x80008de8]:csrrs a0, fcsr, zero
	-[0x80008dec]:sw t6, 472(t1)
Current Store : [0x80008df0] : sw a0, 476(t1) -- Store: [0x800139c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008e1c]:feq.h t6, ft11, ft10
	-[0x80008e20]:csrrs a0, fcsr, zero
	-[0x80008e24]:sw t6, 480(t1)
Current Store : [0x80008e28] : sw a0, 484(t1) -- Store: [0x800139c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008e54]:feq.h t6, ft11, ft10
	-[0x80008e58]:csrrs a0, fcsr, zero
	-[0x80008e5c]:sw t6, 488(t1)
Current Store : [0x80008e60] : sw a0, 492(t1) -- Store: [0x800139d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008e8c]:feq.h t6, ft11, ft10
	-[0x80008e90]:csrrs a0, fcsr, zero
	-[0x80008e94]:sw t6, 496(t1)
Current Store : [0x80008e98] : sw a0, 500(t1) -- Store: [0x800139d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008ec4]:feq.h t6, ft11, ft10
	-[0x80008ec8]:csrrs a0, fcsr, zero
	-[0x80008ecc]:sw t6, 504(t1)
Current Store : [0x80008ed0] : sw a0, 508(t1) -- Store: [0x800139e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008efc]:feq.h t6, ft11, ft10
	-[0x80008f00]:csrrs a0, fcsr, zero
	-[0x80008f04]:sw t6, 512(t1)
Current Store : [0x80008f08] : sw a0, 516(t1) -- Store: [0x800139e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008f34]:feq.h t6, ft11, ft10
	-[0x80008f38]:csrrs a0, fcsr, zero
	-[0x80008f3c]:sw t6, 520(t1)
Current Store : [0x80008f40] : sw a0, 524(t1) -- Store: [0x800139f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008f6c]:feq.h t6, ft11, ft10
	-[0x80008f70]:csrrs a0, fcsr, zero
	-[0x80008f74]:sw t6, 528(t1)
Current Store : [0x80008f78] : sw a0, 532(t1) -- Store: [0x800139f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008fa4]:feq.h t6, ft11, ft10
	-[0x80008fa8]:csrrs a0, fcsr, zero
	-[0x80008fac]:sw t6, 536(t1)
Current Store : [0x80008fb0] : sw a0, 540(t1) -- Store: [0x80013a00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80008fdc]:feq.h t6, ft11, ft10
	-[0x80008fe0]:csrrs a0, fcsr, zero
	-[0x80008fe4]:sw t6, 544(t1)
Current Store : [0x80008fe8] : sw a0, 548(t1) -- Store: [0x80013a08]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009014]:feq.h t6, ft11, ft10
	-[0x80009018]:csrrs a0, fcsr, zero
	-[0x8000901c]:sw t6, 552(t1)
Current Store : [0x80009020] : sw a0, 556(t1) -- Store: [0x80013a10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000904c]:feq.h t6, ft11, ft10
	-[0x80009050]:csrrs a0, fcsr, zero
	-[0x80009054]:sw t6, 560(t1)
Current Store : [0x80009058] : sw a0, 564(t1) -- Store: [0x80013a18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009084]:feq.h t6, ft11, ft10
	-[0x80009088]:csrrs a0, fcsr, zero
	-[0x8000908c]:sw t6, 568(t1)
Current Store : [0x80009090] : sw a0, 572(t1) -- Store: [0x80013a20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800090bc]:feq.h t6, ft11, ft10
	-[0x800090c0]:csrrs a0, fcsr, zero
	-[0x800090c4]:sw t6, 576(t1)
Current Store : [0x800090c8] : sw a0, 580(t1) -- Store: [0x80013a28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800090f4]:feq.h t6, ft11, ft10
	-[0x800090f8]:csrrs a0, fcsr, zero
	-[0x800090fc]:sw t6, 584(t1)
Current Store : [0x80009100] : sw a0, 588(t1) -- Store: [0x80013a30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000912c]:feq.h t6, ft11, ft10
	-[0x80009130]:csrrs a0, fcsr, zero
	-[0x80009134]:sw t6, 592(t1)
Current Store : [0x80009138] : sw a0, 596(t1) -- Store: [0x80013a38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009164]:feq.h t6, ft11, ft10
	-[0x80009168]:csrrs a0, fcsr, zero
	-[0x8000916c]:sw t6, 600(t1)
Current Store : [0x80009170] : sw a0, 604(t1) -- Store: [0x80013a40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1b and fm1 == 0x1ed and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000919c]:feq.h t6, ft11, ft10
	-[0x800091a0]:csrrs a0, fcsr, zero
	-[0x800091a4]:sw t6, 608(t1)
Current Store : [0x800091a8] : sw a0, 612(t1) -- Store: [0x80013a48]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1b and fm2 == 0x1ed and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800091d4]:feq.h t6, ft11, ft10
	-[0x800091d8]:csrrs a0, fcsr, zero
	-[0x800091dc]:sw t6, 616(t1)
Current Store : [0x800091e0] : sw a0, 620(t1) -- Store: [0x80013a50]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000920c]:feq.h t6, ft11, ft10
	-[0x80009210]:csrrs a0, fcsr, zero
	-[0x80009214]:sw t6, 624(t1)
Current Store : [0x80009218] : sw a0, 628(t1) -- Store: [0x80013a58]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x00a and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009244]:feq.h t6, ft11, ft10
	-[0x80009248]:csrrs a0, fcsr, zero
	-[0x8000924c]:sw t6, 632(t1)
Current Store : [0x80009250] : sw a0, 636(t1) -- Store: [0x80013a60]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000927c]:feq.h t6, ft11, ft10
	-[0x80009280]:csrrs a0, fcsr, zero
	-[0x80009284]:sw t6, 640(t1)
Current Store : [0x80009288] : sw a0, 644(t1) -- Store: [0x80013a68]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800092b4]:feq.h t6, ft11, ft10
	-[0x800092b8]:csrrs a0, fcsr, zero
	-[0x800092bc]:sw t6, 648(t1)
Current Store : [0x800092c0] : sw a0, 652(t1) -- Store: [0x80013a70]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800092ec]:feq.h t6, ft11, ft10
	-[0x800092f0]:csrrs a0, fcsr, zero
	-[0x800092f4]:sw t6, 656(t1)
Current Store : [0x800092f8] : sw a0, 660(t1) -- Store: [0x80013a78]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009324]:feq.h t6, ft11, ft10
	-[0x80009328]:csrrs a0, fcsr, zero
	-[0x8000932c]:sw t6, 664(t1)
Current Store : [0x80009330] : sw a0, 668(t1) -- Store: [0x80013a80]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000935c]:feq.h t6, ft11, ft10
	-[0x80009360]:csrrs a0, fcsr, zero
	-[0x80009364]:sw t6, 672(t1)
Current Store : [0x80009368] : sw a0, 676(t1) -- Store: [0x80013a88]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009394]:feq.h t6, ft11, ft10
	-[0x80009398]:csrrs a0, fcsr, zero
	-[0x8000939c]:sw t6, 680(t1)
Current Store : [0x800093a0] : sw a0, 684(t1) -- Store: [0x80013a90]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800093cc]:feq.h t6, ft11, ft10
	-[0x800093d0]:csrrs a0, fcsr, zero
	-[0x800093d4]:sw t6, 688(t1)
Current Store : [0x800093d8] : sw a0, 692(t1) -- Store: [0x80013a98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009404]:feq.h t6, ft11, ft10
	-[0x80009408]:csrrs a0, fcsr, zero
	-[0x8000940c]:sw t6, 696(t1)
Current Store : [0x80009410] : sw a0, 700(t1) -- Store: [0x80013aa0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x065 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000943c]:feq.h t6, ft11, ft10
	-[0x80009440]:csrrs a0, fcsr, zero
	-[0x80009444]:sw t6, 704(t1)
Current Store : [0x80009448] : sw a0, 708(t1) -- Store: [0x80013aa8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x065 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009474]:feq.h t6, ft11, ft10
	-[0x80009478]:csrrs a0, fcsr, zero
	-[0x8000947c]:sw t6, 712(t1)
Current Store : [0x80009480] : sw a0, 716(t1) -- Store: [0x80013ab0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x065 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800094ac]:feq.h t6, ft11, ft10
	-[0x800094b0]:csrrs a0, fcsr, zero
	-[0x800094b4]:sw t6, 720(t1)
Current Store : [0x800094b8] : sw a0, 724(t1) -- Store: [0x80013ab8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x065 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800094e4]:feq.h t6, ft11, ft10
	-[0x800094e8]:csrrs a0, fcsr, zero
	-[0x800094ec]:sw t6, 728(t1)
Current Store : [0x800094f0] : sw a0, 732(t1) -- Store: [0x80013ac0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000951c]:feq.h t6, ft11, ft10
	-[0x80009520]:csrrs a0, fcsr, zero
	-[0x80009524]:sw t6, 736(t1)
Current Store : [0x80009528] : sw a0, 740(t1) -- Store: [0x80013ac8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009554]:feq.h t6, ft11, ft10
	-[0x80009558]:csrrs a0, fcsr, zero
	-[0x8000955c]:sw t6, 744(t1)
Current Store : [0x80009560] : sw a0, 748(t1) -- Store: [0x80013ad0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000958c]:feq.h t6, ft11, ft10
	-[0x80009590]:csrrs a0, fcsr, zero
	-[0x80009594]:sw t6, 752(t1)
Current Store : [0x80009598] : sw a0, 756(t1) -- Store: [0x80013ad8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800095c4]:feq.h t6, ft11, ft10
	-[0x800095c8]:csrrs a0, fcsr, zero
	-[0x800095cc]:sw t6, 760(t1)
Current Store : [0x800095d0] : sw a0, 764(t1) -- Store: [0x80013ae0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800095fc]:feq.h t6, ft11, ft10
	-[0x80009600]:csrrs a0, fcsr, zero
	-[0x80009604]:sw t6, 768(t1)
Current Store : [0x80009608] : sw a0, 772(t1) -- Store: [0x80013ae8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009634]:feq.h t6, ft11, ft10
	-[0x80009638]:csrrs a0, fcsr, zero
	-[0x8000963c]:sw t6, 776(t1)
Current Store : [0x80009640] : sw a0, 780(t1) -- Store: [0x80013af0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000966c]:feq.h t6, ft11, ft10
	-[0x80009670]:csrrs a0, fcsr, zero
	-[0x80009674]:sw t6, 784(t1)
Current Store : [0x80009678] : sw a0, 788(t1) -- Store: [0x80013af8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x11 and fm1 == 0x212 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800096a4]:feq.h t6, ft11, ft10
	-[0x800096a8]:csrrs a0, fcsr, zero
	-[0x800096ac]:sw t6, 792(t1)
Current Store : [0x800096b0] : sw a0, 796(t1) -- Store: [0x80013b00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x212 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800096dc]:feq.h t6, ft11, ft10
	-[0x800096e0]:csrrs a0, fcsr, zero
	-[0x800096e4]:sw t6, 800(t1)
Current Store : [0x800096e8] : sw a0, 804(t1) -- Store: [0x80013b08]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x11 and fm2 == 0x212 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009714]:feq.h t6, ft11, ft10
	-[0x80009718]:csrrs a0, fcsr, zero
	-[0x8000971c]:sw t6, 808(t1)
Current Store : [0x80009720] : sw a0, 812(t1) -- Store: [0x80013b10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000974c]:feq.h t6, ft11, ft10
	-[0x80009750]:csrrs a0, fcsr, zero
	-[0x80009754]:sw t6, 816(t1)
Current Store : [0x80009758] : sw a0, 820(t1) -- Store: [0x80013b18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009784]:feq.h t6, ft11, ft10
	-[0x80009788]:csrrs a0, fcsr, zero
	-[0x8000978c]:sw t6, 824(t1)
Current Store : [0x80009790] : sw a0, 828(t1) -- Store: [0x80013b20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800097bc]:feq.h t6, ft11, ft10
	-[0x800097c0]:csrrs a0, fcsr, zero
	-[0x800097c4]:sw t6, 832(t1)
Current Store : [0x800097c8] : sw a0, 836(t1) -- Store: [0x80013b28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800097f4]:feq.h t6, ft11, ft10
	-[0x800097f8]:csrrs a0, fcsr, zero
	-[0x800097fc]:sw t6, 840(t1)
Current Store : [0x80009800] : sw a0, 844(t1) -- Store: [0x80013b30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000982c]:feq.h t6, ft11, ft10
	-[0x80009830]:csrrs a0, fcsr, zero
	-[0x80009834]:sw t6, 848(t1)
Current Store : [0x80009838] : sw a0, 852(t1) -- Store: [0x80013b38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009864]:feq.h t6, ft11, ft10
	-[0x80009868]:csrrs a0, fcsr, zero
	-[0x8000986c]:sw t6, 856(t1)
Current Store : [0x80009870] : sw a0, 860(t1) -- Store: [0x80013b40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000989c]:feq.h t6, ft11, ft10
	-[0x800098a0]:csrrs a0, fcsr, zero
	-[0x800098a4]:sw t6, 864(t1)
Current Store : [0x800098a8] : sw a0, 868(t1) -- Store: [0x80013b48]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800098d4]:feq.h t6, ft11, ft10
	-[0x800098d8]:csrrs a0, fcsr, zero
	-[0x800098dc]:sw t6, 872(t1)
Current Store : [0x800098e0] : sw a0, 876(t1) -- Store: [0x80013b50]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000990c]:feq.h t6, ft11, ft10
	-[0x80009910]:csrrs a0, fcsr, zero
	-[0x80009914]:sw t6, 880(t1)
Current Store : [0x80009918] : sw a0, 884(t1) -- Store: [0x80013b58]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009944]:feq.h t6, ft11, ft10
	-[0x80009948]:csrrs a0, fcsr, zero
	-[0x8000994c]:sw t6, 888(t1)
Current Store : [0x80009950] : sw a0, 892(t1) -- Store: [0x80013b60]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000997c]:feq.h t6, ft11, ft10
	-[0x80009980]:csrrs a0, fcsr, zero
	-[0x80009984]:sw t6, 896(t1)
Current Store : [0x80009988] : sw a0, 900(t1) -- Store: [0x80013b68]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800099b4]:feq.h t6, ft11, ft10
	-[0x800099b8]:csrrs a0, fcsr, zero
	-[0x800099bc]:sw t6, 904(t1)
Current Store : [0x800099c0] : sw a0, 908(t1) -- Store: [0x80013b70]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800099ec]:feq.h t6, ft11, ft10
	-[0x800099f0]:csrrs a0, fcsr, zero
	-[0x800099f4]:sw t6, 912(t1)
Current Store : [0x800099f8] : sw a0, 916(t1) -- Store: [0x80013b78]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009a24]:feq.h t6, ft11, ft10
	-[0x80009a28]:csrrs a0, fcsr, zero
	-[0x80009a2c]:sw t6, 920(t1)
Current Store : [0x80009a30] : sw a0, 924(t1) -- Store: [0x80013b80]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009a5c]:feq.h t6, ft11, ft10
	-[0x80009a60]:csrrs a0, fcsr, zero
	-[0x80009a64]:sw t6, 928(t1)
Current Store : [0x80009a68] : sw a0, 932(t1) -- Store: [0x80013b88]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009a94]:feq.h t6, ft11, ft10
	-[0x80009a98]:csrrs a0, fcsr, zero
	-[0x80009a9c]:sw t6, 936(t1)
Current Store : [0x80009aa0] : sw a0, 940(t1) -- Store: [0x80013b90]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009acc]:feq.h t6, ft11, ft10
	-[0x80009ad0]:csrrs a0, fcsr, zero
	-[0x80009ad4]:sw t6, 944(t1)
Current Store : [0x80009ad8] : sw a0, 948(t1) -- Store: [0x80013b98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009b04]:feq.h t6, ft11, ft10
	-[0x80009b08]:csrrs a0, fcsr, zero
	-[0x80009b0c]:sw t6, 952(t1)
Current Store : [0x80009b10] : sw a0, 956(t1) -- Store: [0x80013ba0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009b3c]:feq.h t6, ft11, ft10
	-[0x80009b40]:csrrs a0, fcsr, zero
	-[0x80009b44]:sw t6, 960(t1)
Current Store : [0x80009b48] : sw a0, 964(t1) -- Store: [0x80013ba8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009b74]:feq.h t6, ft11, ft10
	-[0x80009b78]:csrrs a0, fcsr, zero
	-[0x80009b7c]:sw t6, 968(t1)
Current Store : [0x80009b80] : sw a0, 972(t1) -- Store: [0x80013bb0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009bac]:feq.h t6, ft11, ft10
	-[0x80009bb0]:csrrs a0, fcsr, zero
	-[0x80009bb4]:sw t6, 976(t1)
Current Store : [0x80009bb8] : sw a0, 980(t1) -- Store: [0x80013bb8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1a and fm1 == 0x39d and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009be4]:feq.h t6, ft11, ft10
	-[0x80009be8]:csrrs a0, fcsr, zero
	-[0x80009bec]:sw t6, 984(t1)
Current Store : [0x80009bf0] : sw a0, 988(t1) -- Store: [0x80013bc0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1a and fm2 == 0x39d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009c1c]:feq.h t6, ft11, ft10
	-[0x80009c20]:csrrs a0, fcsr, zero
	-[0x80009c24]:sw t6, 992(t1)
Current Store : [0x80009c28] : sw a0, 996(t1) -- Store: [0x80013bc8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009c5c]:feq.h t6, ft11, ft10
	-[0x80009c60]:csrrs a0, fcsr, zero
	-[0x80009c64]:sw t6, 1000(t1)
Current Store : [0x80009c68] : sw a0, 1004(t1) -- Store: [0x80013bd0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009c9c]:feq.h t6, ft11, ft10
	-[0x80009ca0]:csrrs a0, fcsr, zero
	-[0x80009ca4]:sw t6, 1008(t1)
Current Store : [0x80009ca8] : sw a0, 1012(t1) -- Store: [0x80013bd8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009cdc]:feq.h t6, ft11, ft10
	-[0x80009ce0]:csrrs a0, fcsr, zero
	-[0x80009ce4]:sw t6, 1016(t1)
Current Store : [0x80009ce8] : sw a0, 1020(t1) -- Store: [0x80013be0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009d24]:feq.h t6, ft11, ft10
	-[0x80009d28]:csrrs a0, fcsr, zero
	-[0x80009d2c]:sw t6, 0(t1)
Current Store : [0x80009d30] : sw a0, 4(t1) -- Store: [0x80013be8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009d64]:feq.h t6, ft11, ft10
	-[0x80009d68]:csrrs a0, fcsr, zero
	-[0x80009d6c]:sw t6, 8(t1)
Current Store : [0x80009d70] : sw a0, 12(t1) -- Store: [0x80013bf0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009da4]:feq.h t6, ft11, ft10
	-[0x80009da8]:csrrs a0, fcsr, zero
	-[0x80009dac]:sw t6, 16(t1)
Current Store : [0x80009db0] : sw a0, 20(t1) -- Store: [0x80013bf8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009de4]:feq.h t6, ft11, ft10
	-[0x80009de8]:csrrs a0, fcsr, zero
	-[0x80009dec]:sw t6, 24(t1)
Current Store : [0x80009df0] : sw a0, 28(t1) -- Store: [0x80013c00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x041 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009e24]:feq.h t6, ft11, ft10
	-[0x80009e28]:csrrs a0, fcsr, zero
	-[0x80009e2c]:sw t6, 32(t1)
Current Store : [0x80009e30] : sw a0, 36(t1) -- Store: [0x80013c08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x041 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009e64]:feq.h t6, ft11, ft10
	-[0x80009e68]:csrrs a0, fcsr, zero
	-[0x80009e6c]:sw t6, 40(t1)
Current Store : [0x80009e70] : sw a0, 44(t1) -- Store: [0x80013c10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x041 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009ea4]:feq.h t6, ft11, ft10
	-[0x80009ea8]:csrrs a0, fcsr, zero
	-[0x80009eac]:sw t6, 48(t1)
Current Store : [0x80009eb0] : sw a0, 52(t1) -- Store: [0x80013c18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x041 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009ee4]:feq.h t6, ft11, ft10
	-[0x80009ee8]:csrrs a0, fcsr, zero
	-[0x80009eec]:sw t6, 56(t1)
Current Store : [0x80009ef0] : sw a0, 60(t1) -- Store: [0x80013c20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009f24]:feq.h t6, ft11, ft10
	-[0x80009f28]:csrrs a0, fcsr, zero
	-[0x80009f2c]:sw t6, 64(t1)
Current Store : [0x80009f30] : sw a0, 68(t1) -- Store: [0x80013c28]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009f64]:feq.h t6, ft11, ft10
	-[0x80009f68]:csrrs a0, fcsr, zero
	-[0x80009f6c]:sw t6, 72(t1)
Current Store : [0x80009f70] : sw a0, 76(t1) -- Store: [0x80013c30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009fa4]:feq.h t6, ft11, ft10
	-[0x80009fa8]:csrrs a0, fcsr, zero
	-[0x80009fac]:sw t6, 80(t1)
Current Store : [0x80009fb0] : sw a0, 84(t1) -- Store: [0x80013c38]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80009fe4]:feq.h t6, ft11, ft10
	-[0x80009fe8]:csrrs a0, fcsr, zero
	-[0x80009fec]:sw t6, 88(t1)
Current Store : [0x80009ff0] : sw a0, 92(t1) -- Store: [0x80013c40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a024]:feq.h t6, ft11, ft10
	-[0x8000a028]:csrrs a0, fcsr, zero
	-[0x8000a02c]:sw t6, 96(t1)
Current Store : [0x8000a030] : sw a0, 100(t1) -- Store: [0x80013c48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a064]:feq.h t6, ft11, ft10
	-[0x8000a068]:csrrs a0, fcsr, zero
	-[0x8000a06c]:sw t6, 104(t1)
Current Store : [0x8000a070] : sw a0, 108(t1) -- Store: [0x80013c50]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a0a4]:feq.h t6, ft11, ft10
	-[0x8000a0a8]:csrrs a0, fcsr, zero
	-[0x8000a0ac]:sw t6, 112(t1)
Current Store : [0x8000a0b0] : sw a0, 116(t1) -- Store: [0x80013c58]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x10 and fm1 == 0x3cc and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a0e4]:feq.h t6, ft11, ft10
	-[0x8000a0e8]:csrrs a0, fcsr, zero
	-[0x8000a0ec]:sw t6, 120(t1)
Current Store : [0x8000a0f0] : sw a0, 124(t1) -- Store: [0x80013c60]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x10 and fm2 == 0x3cc and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a124]:feq.h t6, ft11, ft10
	-[0x8000a128]:csrrs a0, fcsr, zero
	-[0x8000a12c]:sw t6, 128(t1)
Current Store : [0x8000a130] : sw a0, 132(t1) -- Store: [0x80013c68]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x10 and fm2 == 0x3cc and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a164]:feq.h t6, ft11, ft10
	-[0x8000a168]:csrrs a0, fcsr, zero
	-[0x8000a16c]:sw t6, 136(t1)
Current Store : [0x8000a170] : sw a0, 140(t1) -- Store: [0x80013c70]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a1a4]:feq.h t6, ft11, ft10
	-[0x8000a1a8]:csrrs a0, fcsr, zero
	-[0x8000a1ac]:sw t6, 144(t1)
Current Store : [0x8000a1b0] : sw a0, 148(t1) -- Store: [0x80013c78]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a1e4]:feq.h t6, ft11, ft10
	-[0x8000a1e8]:csrrs a0, fcsr, zero
	-[0x8000a1ec]:sw t6, 152(t1)
Current Store : [0x8000a1f0] : sw a0, 156(t1) -- Store: [0x80013c80]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a224]:feq.h t6, ft11, ft10
	-[0x8000a228]:csrrs a0, fcsr, zero
	-[0x8000a22c]:sw t6, 160(t1)
Current Store : [0x8000a230] : sw a0, 164(t1) -- Store: [0x80013c88]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a264]:feq.h t6, ft11, ft10
	-[0x8000a268]:csrrs a0, fcsr, zero
	-[0x8000a26c]:sw t6, 168(t1)
Current Store : [0x8000a270] : sw a0, 172(t1) -- Store: [0x80013c90]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a2a4]:feq.h t6, ft11, ft10
	-[0x8000a2a8]:csrrs a0, fcsr, zero
	-[0x8000a2ac]:sw t6, 176(t1)
Current Store : [0x8000a2b0] : sw a0, 180(t1) -- Store: [0x80013c98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a2e4]:feq.h t6, ft11, ft10
	-[0x8000a2e8]:csrrs a0, fcsr, zero
	-[0x8000a2ec]:sw t6, 184(t1)
Current Store : [0x8000a2f0] : sw a0, 188(t1) -- Store: [0x80013ca0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a324]:feq.h t6, ft11, ft10
	-[0x8000a328]:csrrs a0, fcsr, zero
	-[0x8000a32c]:sw t6, 192(t1)
Current Store : [0x8000a330] : sw a0, 196(t1) -- Store: [0x80013ca8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a364]:feq.h t6, ft11, ft10
	-[0x8000a368]:csrrs a0, fcsr, zero
	-[0x8000a36c]:sw t6, 200(t1)
Current Store : [0x8000a370] : sw a0, 204(t1) -- Store: [0x80013cb0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a3a4]:feq.h t6, ft11, ft10
	-[0x8000a3a8]:csrrs a0, fcsr, zero
	-[0x8000a3ac]:sw t6, 208(t1)
Current Store : [0x8000a3b0] : sw a0, 212(t1) -- Store: [0x80013cb8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a3e4]:feq.h t6, ft11, ft10
	-[0x8000a3e8]:csrrs a0, fcsr, zero
	-[0x8000a3ec]:sw t6, 216(t1)
Current Store : [0x8000a3f0] : sw a0, 220(t1) -- Store: [0x80013cc0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a424]:feq.h t6, ft11, ft10
	-[0x8000a428]:csrrs a0, fcsr, zero
	-[0x8000a42c]:sw t6, 224(t1)
Current Store : [0x8000a430] : sw a0, 228(t1) -- Store: [0x80013cc8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a464]:feq.h t6, ft11, ft10
	-[0x8000a468]:csrrs a0, fcsr, zero
	-[0x8000a46c]:sw t6, 232(t1)
Current Store : [0x8000a470] : sw a0, 236(t1) -- Store: [0x80013cd0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a4a4]:feq.h t6, ft11, ft10
	-[0x8000a4a8]:csrrs a0, fcsr, zero
	-[0x8000a4ac]:sw t6, 240(t1)
Current Store : [0x8000a4b0] : sw a0, 244(t1) -- Store: [0x80013cd8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a4e4]:feq.h t6, ft11, ft10
	-[0x8000a4e8]:csrrs a0, fcsr, zero
	-[0x8000a4ec]:sw t6, 248(t1)
Current Store : [0x8000a4f0] : sw a0, 252(t1) -- Store: [0x80013ce0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a524]:feq.h t6, ft11, ft10
	-[0x8000a528]:csrrs a0, fcsr, zero
	-[0x8000a52c]:sw t6, 256(t1)
Current Store : [0x8000a530] : sw a0, 260(t1) -- Store: [0x80013ce8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a564]:feq.h t6, ft11, ft10
	-[0x8000a568]:csrrs a0, fcsr, zero
	-[0x8000a56c]:sw t6, 264(t1)
Current Store : [0x8000a570] : sw a0, 268(t1) -- Store: [0x80013cf0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a5a4]:feq.h t6, ft11, ft10
	-[0x8000a5a8]:csrrs a0, fcsr, zero
	-[0x8000a5ac]:sw t6, 272(t1)
Current Store : [0x8000a5b0] : sw a0, 276(t1) -- Store: [0x80013cf8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a5e4]:feq.h t6, ft11, ft10
	-[0x8000a5e8]:csrrs a0, fcsr, zero
	-[0x8000a5ec]:sw t6, 280(t1)
Current Store : [0x8000a5f0] : sw a0, 284(t1) -- Store: [0x80013d00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a624]:feq.h t6, ft11, ft10
	-[0x8000a628]:csrrs a0, fcsr, zero
	-[0x8000a62c]:sw t6, 288(t1)
Current Store : [0x8000a630] : sw a0, 292(t1) -- Store: [0x80013d08]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a664]:feq.h t6, ft11, ft10
	-[0x8000a668]:csrrs a0, fcsr, zero
	-[0x8000a66c]:sw t6, 296(t1)
Current Store : [0x8000a670] : sw a0, 300(t1) -- Store: [0x80013d10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a6a4]:feq.h t6, ft11, ft10
	-[0x8000a6a8]:csrrs a0, fcsr, zero
	-[0x8000a6ac]:sw t6, 304(t1)
Current Store : [0x8000a6b0] : sw a0, 308(t1) -- Store: [0x80013d18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1a and fm1 == 0x23c and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a6e4]:feq.h t6, ft11, ft10
	-[0x8000a6e8]:csrrs a0, fcsr, zero
	-[0x8000a6ec]:sw t6, 312(t1)
Current Store : [0x8000a6f0] : sw a0, 316(t1) -- Store: [0x80013d20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1a and fm2 == 0x23c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a724]:feq.h t6, ft11, ft10
	-[0x8000a728]:csrrs a0, fcsr, zero
	-[0x8000a72c]:sw t6, 320(t1)
Current Store : [0x8000a730] : sw a0, 324(t1) -- Store: [0x80013d28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a764]:feq.h t6, ft11, ft10
	-[0x8000a768]:csrrs a0, fcsr, zero
	-[0x8000a76c]:sw t6, 328(t1)
Current Store : [0x8000a770] : sw a0, 332(t1) -- Store: [0x80013d30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a7a4]:feq.h t6, ft11, ft10
	-[0x8000a7a8]:csrrs a0, fcsr, zero
	-[0x8000a7ac]:sw t6, 336(t1)
Current Store : [0x8000a7b0] : sw a0, 340(t1) -- Store: [0x80013d38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a7e4]:feq.h t6, ft11, ft10
	-[0x8000a7e8]:csrrs a0, fcsr, zero
	-[0x8000a7ec]:sw t6, 344(t1)
Current Store : [0x8000a7f0] : sw a0, 348(t1) -- Store: [0x80013d40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a824]:feq.h t6, ft11, ft10
	-[0x8000a828]:csrrs a0, fcsr, zero
	-[0x8000a82c]:sw t6, 352(t1)
Current Store : [0x8000a830] : sw a0, 356(t1) -- Store: [0x80013d48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a864]:feq.h t6, ft11, ft10
	-[0x8000a868]:csrrs a0, fcsr, zero
	-[0x8000a86c]:sw t6, 360(t1)
Current Store : [0x8000a870] : sw a0, 364(t1) -- Store: [0x80013d50]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a8a4]:feq.h t6, ft11, ft10
	-[0x8000a8a8]:csrrs a0, fcsr, zero
	-[0x8000a8ac]:sw t6, 368(t1)
Current Store : [0x8000a8b0] : sw a0, 372(t1) -- Store: [0x80013d58]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x035 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a8e4]:feq.h t6, ft11, ft10
	-[0x8000a8e8]:csrrs a0, fcsr, zero
	-[0x8000a8ec]:sw t6, 376(t1)
Current Store : [0x8000a8f0] : sw a0, 380(t1) -- Store: [0x80013d60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x035 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a924]:feq.h t6, ft11, ft10
	-[0x8000a928]:csrrs a0, fcsr, zero
	-[0x8000a92c]:sw t6, 384(t1)
Current Store : [0x8000a930] : sw a0, 388(t1) -- Store: [0x80013d68]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x035 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a964]:feq.h t6, ft11, ft10
	-[0x8000a968]:csrrs a0, fcsr, zero
	-[0x8000a96c]:sw t6, 392(t1)
Current Store : [0x8000a970] : sw a0, 396(t1) -- Store: [0x80013d70]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x035 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a9a4]:feq.h t6, ft11, ft10
	-[0x8000a9a8]:csrrs a0, fcsr, zero
	-[0x8000a9ac]:sw t6, 400(t1)
Current Store : [0x8000a9b0] : sw a0, 404(t1) -- Store: [0x80013d78]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000a9e4]:feq.h t6, ft11, ft10
	-[0x8000a9e8]:csrrs a0, fcsr, zero
	-[0x8000a9ec]:sw t6, 408(t1)
Current Store : [0x8000a9f0] : sw a0, 412(t1) -- Store: [0x80013d80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000aa24]:feq.h t6, ft11, ft10
	-[0x8000aa28]:csrrs a0, fcsr, zero
	-[0x8000aa2c]:sw t6, 416(t1)
Current Store : [0x8000aa30] : sw a0, 420(t1) -- Store: [0x80013d88]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000aa64]:feq.h t6, ft11, ft10
	-[0x8000aa68]:csrrs a0, fcsr, zero
	-[0x8000aa6c]:sw t6, 424(t1)
Current Store : [0x8000aa70] : sw a0, 428(t1) -- Store: [0x80013d90]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000aaa4]:feq.h t6, ft11, ft10
	-[0x8000aaa8]:csrrs a0, fcsr, zero
	-[0x8000aaac]:sw t6, 432(t1)
Current Store : [0x8000aab0] : sw a0, 436(t1) -- Store: [0x80013d98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000aae4]:feq.h t6, ft11, ft10
	-[0x8000aae8]:csrrs a0, fcsr, zero
	-[0x8000aaec]:sw t6, 440(t1)
Current Store : [0x8000aaf0] : sw a0, 444(t1) -- Store: [0x80013da0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ab24]:feq.h t6, ft11, ft10
	-[0x8000ab28]:csrrs a0, fcsr, zero
	-[0x8000ab2c]:sw t6, 448(t1)
Current Store : [0x8000ab30] : sw a0, 452(t1) -- Store: [0x80013da8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ab64]:feq.h t6, ft11, ft10
	-[0x8000ab68]:csrrs a0, fcsr, zero
	-[0x8000ab6c]:sw t6, 456(t1)
Current Store : [0x8000ab70] : sw a0, 460(t1) -- Store: [0x80013db0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x10 and fm1 == 0x262 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000aba4]:feq.h t6, ft11, ft10
	-[0x8000aba8]:csrrs a0, fcsr, zero
	-[0x8000abac]:sw t6, 464(t1)
Current Store : [0x8000abb0] : sw a0, 468(t1) -- Store: [0x80013db8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x10 and fm2 == 0x262 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000abe4]:feq.h t6, ft11, ft10
	-[0x8000abe8]:csrrs a0, fcsr, zero
	-[0x8000abec]:sw t6, 472(t1)
Current Store : [0x8000abf0] : sw a0, 476(t1) -- Store: [0x80013dc0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x10 and fm2 == 0x262 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ac24]:feq.h t6, ft11, ft10
	-[0x8000ac28]:csrrs a0, fcsr, zero
	-[0x8000ac2c]:sw t6, 480(t1)
Current Store : [0x8000ac30] : sw a0, 484(t1) -- Store: [0x80013dc8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ac64]:feq.h t6, ft11, ft10
	-[0x8000ac68]:csrrs a0, fcsr, zero
	-[0x8000ac6c]:sw t6, 488(t1)
Current Store : [0x8000ac70] : sw a0, 492(t1) -- Store: [0x80013dd0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000aca4]:feq.h t6, ft11, ft10
	-[0x8000aca8]:csrrs a0, fcsr, zero
	-[0x8000acac]:sw t6, 496(t1)
Current Store : [0x8000acb0] : sw a0, 500(t1) -- Store: [0x80013dd8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ace4]:feq.h t6, ft11, ft10
	-[0x8000ace8]:csrrs a0, fcsr, zero
	-[0x8000acec]:sw t6, 504(t1)
Current Store : [0x8000acf0] : sw a0, 508(t1) -- Store: [0x80013de0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ad24]:feq.h t6, ft11, ft10
	-[0x8000ad28]:csrrs a0, fcsr, zero
	-[0x8000ad2c]:sw t6, 512(t1)
Current Store : [0x8000ad30] : sw a0, 516(t1) -- Store: [0x80013de8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ad64]:feq.h t6, ft11, ft10
	-[0x8000ad68]:csrrs a0, fcsr, zero
	-[0x8000ad6c]:sw t6, 520(t1)
Current Store : [0x8000ad70] : sw a0, 524(t1) -- Store: [0x80013df0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ada4]:feq.h t6, ft11, ft10
	-[0x8000ada8]:csrrs a0, fcsr, zero
	-[0x8000adac]:sw t6, 528(t1)
Current Store : [0x8000adb0] : sw a0, 532(t1) -- Store: [0x80013df8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ade4]:feq.h t6, ft11, ft10
	-[0x8000ade8]:csrrs a0, fcsr, zero
	-[0x8000adec]:sw t6, 536(t1)
Current Store : [0x8000adf0] : sw a0, 540(t1) -- Store: [0x80013e00]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ae24]:feq.h t6, ft11, ft10
	-[0x8000ae28]:csrrs a0, fcsr, zero
	-[0x8000ae2c]:sw t6, 544(t1)
Current Store : [0x8000ae30] : sw a0, 548(t1) -- Store: [0x80013e08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ae64]:feq.h t6, ft11, ft10
	-[0x8000ae68]:csrrs a0, fcsr, zero
	-[0x8000ae6c]:sw t6, 552(t1)
Current Store : [0x8000ae70] : sw a0, 556(t1) -- Store: [0x80013e10]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000aea4]:feq.h t6, ft11, ft10
	-[0x8000aea8]:csrrs a0, fcsr, zero
	-[0x8000aeac]:sw t6, 560(t1)
Current Store : [0x8000aeb0] : sw a0, 564(t1) -- Store: [0x80013e18]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000aee4]:feq.h t6, ft11, ft10
	-[0x8000aee8]:csrrs a0, fcsr, zero
	-[0x8000aeec]:sw t6, 568(t1)
Current Store : [0x8000aef0] : sw a0, 572(t1) -- Store: [0x80013e20]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000af24]:feq.h t6, ft11, ft10
	-[0x8000af28]:csrrs a0, fcsr, zero
	-[0x8000af2c]:sw t6, 576(t1)
Current Store : [0x8000af30] : sw a0, 580(t1) -- Store: [0x80013e28]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000af64]:feq.h t6, ft11, ft10
	-[0x8000af68]:csrrs a0, fcsr, zero
	-[0x8000af6c]:sw t6, 584(t1)
Current Store : [0x8000af70] : sw a0, 588(t1) -- Store: [0x80013e30]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000afa4]:feq.h t6, ft11, ft10
	-[0x8000afa8]:csrrs a0, fcsr, zero
	-[0x8000afac]:sw t6, 592(t1)
Current Store : [0x8000afb0] : sw a0, 596(t1) -- Store: [0x80013e38]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000afe4]:feq.h t6, ft11, ft10
	-[0x8000afe8]:csrrs a0, fcsr, zero
	-[0x8000afec]:sw t6, 600(t1)
Current Store : [0x8000aff0] : sw a0, 604(t1) -- Store: [0x80013e40]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b024]:feq.h t6, ft11, ft10
	-[0x8000b028]:csrrs a0, fcsr, zero
	-[0x8000b02c]:sw t6, 608(t1)
Current Store : [0x8000b030] : sw a0, 612(t1) -- Store: [0x80013e48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b064]:feq.h t6, ft11, ft10
	-[0x8000b068]:csrrs a0, fcsr, zero
	-[0x8000b06c]:sw t6, 616(t1)
Current Store : [0x8000b070] : sw a0, 620(t1) -- Store: [0x80013e50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b0a4]:feq.h t6, ft11, ft10
	-[0x8000b0a8]:csrrs a0, fcsr, zero
	-[0x8000b0ac]:sw t6, 624(t1)
Current Store : [0x8000b0b0] : sw a0, 628(t1) -- Store: [0x80013e58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b0e4]:feq.h t6, ft11, ft10
	-[0x8000b0e8]:csrrs a0, fcsr, zero
	-[0x8000b0ec]:sw t6, 632(t1)
Current Store : [0x8000b0f0] : sw a0, 636(t1) -- Store: [0x80013e60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b124]:feq.h t6, ft11, ft10
	-[0x8000b128]:csrrs a0, fcsr, zero
	-[0x8000b12c]:sw t6, 640(t1)
Current Store : [0x8000b130] : sw a0, 644(t1) -- Store: [0x80013e68]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b164]:feq.h t6, ft11, ft10
	-[0x8000b168]:csrrs a0, fcsr, zero
	-[0x8000b16c]:sw t6, 648(t1)
Current Store : [0x8000b170] : sw a0, 652(t1) -- Store: [0x80013e70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1a and fm1 == 0x0b9 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b1a4]:feq.h t6, ft11, ft10
	-[0x8000b1a8]:csrrs a0, fcsr, zero
	-[0x8000b1ac]:sw t6, 656(t1)
Current Store : [0x8000b1b0] : sw a0, 660(t1) -- Store: [0x80013e78]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1a and fm2 == 0x0b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b1e4]:feq.h t6, ft11, ft10
	-[0x8000b1e8]:csrrs a0, fcsr, zero
	-[0x8000b1ec]:sw t6, 664(t1)
Current Store : [0x8000b1f0] : sw a0, 668(t1) -- Store: [0x80013e80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b224]:feq.h t6, ft11, ft10
	-[0x8000b228]:csrrs a0, fcsr, zero
	-[0x8000b22c]:sw t6, 672(t1)
Current Store : [0x8000b230] : sw a0, 676(t1) -- Store: [0x80013e88]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x004 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b264]:feq.h t6, ft11, ft10
	-[0x8000b268]:csrrs a0, fcsr, zero
	-[0x8000b26c]:sw t6, 680(t1)
Current Store : [0x8000b270] : sw a0, 684(t1) -- Store: [0x80013e90]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x004 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b2a4]:feq.h t6, ft11, ft10
	-[0x8000b2a8]:csrrs a0, fcsr, zero
	-[0x8000b2ac]:sw t6, 688(t1)
Current Store : [0x8000b2b0] : sw a0, 692(t1) -- Store: [0x80013e98]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b2e4]:feq.h t6, ft11, ft10
	-[0x8000b2e8]:csrrs a0, fcsr, zero
	-[0x8000b2ec]:sw t6, 696(t1)
Current Store : [0x8000b2f0] : sw a0, 700(t1) -- Store: [0x80013ea0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x028 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b324]:feq.h t6, ft11, ft10
	-[0x8000b328]:csrrs a0, fcsr, zero
	-[0x8000b32c]:sw t6, 704(t1)
Current Store : [0x8000b330] : sw a0, 708(t1) -- Store: [0x80013ea8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x028 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b364]:feq.h t6, ft11, ft10
	-[0x8000b368]:csrrs a0, fcsr, zero
	-[0x8000b36c]:sw t6, 712(t1)
Current Store : [0x8000b370] : sw a0, 716(t1) -- Store: [0x80013eb0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x028 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b3a4]:feq.h t6, ft11, ft10
	-[0x8000b3a8]:csrrs a0, fcsr, zero
	-[0x8000b3ac]:sw t6, 720(t1)
Current Store : [0x8000b3b0] : sw a0, 724(t1) -- Store: [0x80013eb8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x028 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b3e4]:feq.h t6, ft11, ft10
	-[0x8000b3e8]:csrrs a0, fcsr, zero
	-[0x8000b3ec]:sw t6, 728(t1)
Current Store : [0x8000b3f0] : sw a0, 732(t1) -- Store: [0x80013ec0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b424]:feq.h t6, ft11, ft10
	-[0x8000b428]:csrrs a0, fcsr, zero
	-[0x8000b42c]:sw t6, 736(t1)
Current Store : [0x8000b430] : sw a0, 740(t1) -- Store: [0x80013ec8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b464]:feq.h t6, ft11, ft10
	-[0x8000b468]:csrrs a0, fcsr, zero
	-[0x8000b46c]:sw t6, 744(t1)
Current Store : [0x8000b470] : sw a0, 748(t1) -- Store: [0x80013ed0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b4a4]:feq.h t6, ft11, ft10
	-[0x8000b4a8]:csrrs a0, fcsr, zero
	-[0x8000b4ac]:sw t6, 752(t1)
Current Store : [0x8000b4b0] : sw a0, 756(t1) -- Store: [0x80013ed8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b4e4]:feq.h t6, ft11, ft10
	-[0x8000b4e8]:csrrs a0, fcsr, zero
	-[0x8000b4ec]:sw t6, 760(t1)
Current Store : [0x8000b4f0] : sw a0, 764(t1) -- Store: [0x80013ee0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b524]:feq.h t6, ft11, ft10
	-[0x8000b528]:csrrs a0, fcsr, zero
	-[0x8000b52c]:sw t6, 768(t1)
Current Store : [0x8000b530] : sw a0, 772(t1) -- Store: [0x80013ee8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b564]:feq.h t6, ft11, ft10
	-[0x8000b568]:csrrs a0, fcsr, zero
	-[0x8000b56c]:sw t6, 776(t1)
Current Store : [0x8000b570] : sw a0, 780(t1) -- Store: [0x80013ef0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b5a4]:feq.h t6, ft11, ft10
	-[0x8000b5a8]:csrrs a0, fcsr, zero
	-[0x8000b5ac]:sw t6, 784(t1)
Current Store : [0x8000b5b0] : sw a0, 788(t1) -- Store: [0x80013ef8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x10 and fm1 == 0x0d6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b5e4]:feq.h t6, ft11, ft10
	-[0x8000b5e8]:csrrs a0, fcsr, zero
	-[0x8000b5ec]:sw t6, 792(t1)
Current Store : [0x8000b5f0] : sw a0, 796(t1) -- Store: [0x80013f00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x0d6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b624]:feq.h t6, ft11, ft10
	-[0x8000b628]:csrrs a0, fcsr, zero
	-[0x8000b62c]:sw t6, 800(t1)
Current Store : [0x8000b630] : sw a0, 804(t1) -- Store: [0x80013f08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x0d6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b664]:feq.h t6, ft11, ft10
	-[0x8000b668]:csrrs a0, fcsr, zero
	-[0x8000b66c]:sw t6, 808(t1)
Current Store : [0x8000b670] : sw a0, 812(t1) -- Store: [0x80013f10]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b6a4]:feq.h t6, ft11, ft10
	-[0x8000b6a8]:csrrs a0, fcsr, zero
	-[0x8000b6ac]:sw t6, 816(t1)
Current Store : [0x8000b6b0] : sw a0, 820(t1) -- Store: [0x80013f18]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b6e4]:feq.h t6, ft11, ft10
	-[0x8000b6e8]:csrrs a0, fcsr, zero
	-[0x8000b6ec]:sw t6, 824(t1)
Current Store : [0x8000b6f0] : sw a0, 828(t1) -- Store: [0x80013f20]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b724]:feq.h t6, ft11, ft10
	-[0x8000b728]:csrrs a0, fcsr, zero
	-[0x8000b72c]:sw t6, 832(t1)
Current Store : [0x8000b730] : sw a0, 836(t1) -- Store: [0x80013f28]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b764]:feq.h t6, ft11, ft10
	-[0x8000b768]:csrrs a0, fcsr, zero
	-[0x8000b76c]:sw t6, 840(t1)
Current Store : [0x8000b770] : sw a0, 844(t1) -- Store: [0x80013f30]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b7a4]:feq.h t6, ft11, ft10
	-[0x8000b7a8]:csrrs a0, fcsr, zero
	-[0x8000b7ac]:sw t6, 848(t1)
Current Store : [0x8000b7b0] : sw a0, 852(t1) -- Store: [0x80013f38]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b7e4]:feq.h t6, ft11, ft10
	-[0x8000b7e8]:csrrs a0, fcsr, zero
	-[0x8000b7ec]:sw t6, 856(t1)
Current Store : [0x8000b7f0] : sw a0, 860(t1) -- Store: [0x80013f40]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b824]:feq.h t6, ft11, ft10
	-[0x8000b828]:csrrs a0, fcsr, zero
	-[0x8000b82c]:sw t6, 864(t1)
Current Store : [0x8000b830] : sw a0, 868(t1) -- Store: [0x80013f48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b864]:feq.h t6, ft11, ft10
	-[0x8000b868]:csrrs a0, fcsr, zero
	-[0x8000b86c]:sw t6, 872(t1)
Current Store : [0x8000b870] : sw a0, 876(t1) -- Store: [0x80013f50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b8a4]:feq.h t6, ft11, ft10
	-[0x8000b8a8]:csrrs a0, fcsr, zero
	-[0x8000b8ac]:sw t6, 880(t1)
Current Store : [0x8000b8b0] : sw a0, 884(t1) -- Store: [0x80013f58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b8e4]:feq.h t6, ft11, ft10
	-[0x8000b8e8]:csrrs a0, fcsr, zero
	-[0x8000b8ec]:sw t6, 888(t1)
Current Store : [0x8000b8f0] : sw a0, 892(t1) -- Store: [0x80013f60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b924]:feq.h t6, ft11, ft10
	-[0x8000b928]:csrrs a0, fcsr, zero
	-[0x8000b92c]:sw t6, 896(t1)
Current Store : [0x8000b930] : sw a0, 900(t1) -- Store: [0x80013f68]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b964]:feq.h t6, ft11, ft10
	-[0x8000b968]:csrrs a0, fcsr, zero
	-[0x8000b96c]:sw t6, 904(t1)
Current Store : [0x8000b970] : sw a0, 908(t1) -- Store: [0x80013f70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x0dd and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b9a4]:feq.h t6, ft11, ft10
	-[0x8000b9a8]:csrrs a0, fcsr, zero
	-[0x8000b9ac]:sw t6, 912(t1)
Current Store : [0x8000b9b0] : sw a0, 916(t1) -- Store: [0x80013f78]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x0dd and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000b9e4]:feq.h t6, ft11, ft10
	-[0x8000b9e8]:csrrs a0, fcsr, zero
	-[0x8000b9ec]:sw t6, 920(t1)
Current Store : [0x8000b9f0] : sw a0, 924(t1) -- Store: [0x80013f80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ba24]:feq.h t6, ft11, ft10
	-[0x8000ba28]:csrrs a0, fcsr, zero
	-[0x8000ba2c]:sw t6, 928(t1)
Current Store : [0x8000ba30] : sw a0, 932(t1) -- Store: [0x80013f88]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ba64]:feq.h t6, ft11, ft10
	-[0x8000ba68]:csrrs a0, fcsr, zero
	-[0x8000ba6c]:sw t6, 936(t1)
Current Store : [0x8000ba70] : sw a0, 940(t1) -- Store: [0x80013f90]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000baa4]:feq.h t6, ft11, ft10
	-[0x8000baa8]:csrrs a0, fcsr, zero
	-[0x8000baac]:sw t6, 944(t1)
Current Store : [0x8000bab0] : sw a0, 948(t1) -- Store: [0x80013f98]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bae4]:feq.h t6, ft11, ft10
	-[0x8000bae8]:csrrs a0, fcsr, zero
	-[0x8000baec]:sw t6, 952(t1)
Current Store : [0x8000baf0] : sw a0, 956(t1) -- Store: [0x80013fa0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x010 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bb24]:feq.h t6, ft11, ft10
	-[0x8000bb28]:csrrs a0, fcsr, zero
	-[0x8000bb2c]:sw t6, 960(t1)
Current Store : [0x8000bb30] : sw a0, 964(t1) -- Store: [0x80013fa8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x010 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bb64]:feq.h t6, ft11, ft10
	-[0x8000bb68]:csrrs a0, fcsr, zero
	-[0x8000bb6c]:sw t6, 968(t1)
Current Store : [0x8000bb70] : sw a0, 972(t1) -- Store: [0x80013fb0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bba4]:feq.h t6, ft11, ft10
	-[0x8000bba8]:csrrs a0, fcsr, zero
	-[0x8000bbac]:sw t6, 976(t1)
Current Store : [0x8000bbb0] : sw a0, 980(t1) -- Store: [0x80013fb8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bbe4]:feq.h t6, ft11, ft10
	-[0x8000bbe8]:csrrs a0, fcsr, zero
	-[0x8000bbec]:sw t6, 984(t1)
Current Store : [0x8000bbf0] : sw a0, 988(t1) -- Store: [0x80013fc0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bc24]:feq.h t6, ft11, ft10
	-[0x8000bc28]:csrrs a0, fcsr, zero
	-[0x8000bc2c]:sw t6, 992(t1)
Current Store : [0x8000bc30] : sw a0, 996(t1) -- Store: [0x80013fc8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bc64]:feq.h t6, ft11, ft10
	-[0x8000bc68]:csrrs a0, fcsr, zero
	-[0x8000bc6c]:sw t6, 1000(t1)
Current Store : [0x8000bc70] : sw a0, 1004(t1) -- Store: [0x80013fd0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bca4]:feq.h t6, ft11, ft10
	-[0x8000bca8]:csrrs a0, fcsr, zero
	-[0x8000bcac]:sw t6, 1008(t1)
Current Store : [0x8000bcb0] : sw a0, 1012(t1) -- Store: [0x80013fd8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bce4]:feq.h t6, ft11, ft10
	-[0x8000bce8]:csrrs a0, fcsr, zero
	-[0x8000bcec]:sw t6, 1016(t1)
Current Store : [0x8000bcf0] : sw a0, 1020(t1) -- Store: [0x80013fe0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bd2c]:feq.h t6, ft11, ft10
	-[0x8000bd30]:csrrs a0, fcsr, zero
	-[0x8000bd34]:sw t6, 0(t1)
Current Store : [0x8000bd38] : sw a0, 4(t1) -- Store: [0x80013fe8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bd6c]:feq.h t6, ft11, ft10
	-[0x8000bd70]:csrrs a0, fcsr, zero
	-[0x8000bd74]:sw t6, 8(t1)
Current Store : [0x8000bd78] : sw a0, 12(t1) -- Store: [0x80013ff0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bdac]:feq.h t6, ft11, ft10
	-[0x8000bdb0]:csrrs a0, fcsr, zero
	-[0x8000bdb4]:sw t6, 16(t1)
Current Store : [0x8000bdb8] : sw a0, 20(t1) -- Store: [0x80013ff8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x036 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bdec]:feq.h t6, ft11, ft10
	-[0x8000bdf0]:csrrs a0, fcsr, zero
	-[0x8000bdf4]:sw t6, 24(t1)
Current Store : [0x8000bdf8] : sw a0, 28(t1) -- Store: [0x80014000]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x036 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000be2c]:feq.h t6, ft11, ft10
	-[0x8000be30]:csrrs a0, fcsr, zero
	-[0x8000be34]:sw t6, 32(t1)
Current Store : [0x8000be38] : sw a0, 36(t1) -- Store: [0x80014008]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000be6c]:feq.h t6, ft11, ft10
	-[0x8000be70]:csrrs a0, fcsr, zero
	-[0x8000be74]:sw t6, 40(t1)
Current Store : [0x8000be78] : sw a0, 44(t1) -- Store: [0x80014010]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000beac]:feq.h t6, ft11, ft10
	-[0x8000beb0]:csrrs a0, fcsr, zero
	-[0x8000beb4]:sw t6, 48(t1)
Current Store : [0x8000beb8] : sw a0, 52(t1) -- Store: [0x80014018]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x056 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000beec]:feq.h t6, ft11, ft10
	-[0x8000bef0]:csrrs a0, fcsr, zero
	-[0x8000bef4]:sw t6, 56(t1)
Current Store : [0x8000bef8] : sw a0, 60(t1) -- Store: [0x80014020]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x056 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bf2c]:feq.h t6, ft11, ft10
	-[0x8000bf30]:csrrs a0, fcsr, zero
	-[0x8000bf34]:sw t6, 64(t1)
Current Store : [0x8000bf38] : sw a0, 68(t1) -- Store: [0x80014028]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bf6c]:feq.h t6, ft11, ft10
	-[0x8000bf70]:csrrs a0, fcsr, zero
	-[0x8000bf74]:sw t6, 72(t1)
Current Store : [0x8000bf78] : sw a0, 76(t1) -- Store: [0x80014030]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bfac]:feq.h t6, ft11, ft10
	-[0x8000bfb0]:csrrs a0, fcsr, zero
	-[0x8000bfb4]:sw t6, 80(t1)
Current Store : [0x8000bfb8] : sw a0, 84(t1) -- Store: [0x80014038]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x01a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000bfec]:feq.h t6, ft11, ft10
	-[0x8000bff0]:csrrs a0, fcsr, zero
	-[0x8000bff4]:sw t6, 88(t1)
Current Store : [0x8000bff8] : sw a0, 92(t1) -- Store: [0x80014040]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x01a and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c02c]:feq.h t6, ft11, ft10
	-[0x8000c030]:csrrs a0, fcsr, zero
	-[0x8000c034]:sw t6, 96(t1)
Current Store : [0x8000c038] : sw a0, 100(t1) -- Store: [0x80014048]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c06c]:feq.h t6, ft11, ft10
	-[0x8000c070]:csrrs a0, fcsr, zero
	-[0x8000c074]:sw t6, 104(t1)
Current Store : [0x8000c078] : sw a0, 108(t1) -- Store: [0x80014050]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c0ac]:feq.h t6, ft11, ft10
	-[0x8000c0b0]:csrrs a0, fcsr, zero
	-[0x8000c0b4]:sw t6, 112(t1)
Current Store : [0x8000c0b8] : sw a0, 116(t1) -- Store: [0x80014058]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x12 and fm1 == 0x0fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c0ec]:feq.h t6, ft11, ft10
	-[0x8000c0f0]:csrrs a0, fcsr, zero
	-[0x8000c0f4]:sw t6, 120(t1)
Current Store : [0x8000c0f8] : sw a0, 124(t1) -- Store: [0x80014060]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x12 and fm2 == 0x0fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c12c]:feq.h t6, ft11, ft10
	-[0x8000c130]:csrrs a0, fcsr, zero
	-[0x8000c134]:sw t6, 128(t1)
Current Store : [0x8000c138] : sw a0, 132(t1) -- Store: [0x80014068]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x12 and fm2 == 0x0fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c16c]:feq.h t6, ft11, ft10
	-[0x8000c170]:csrrs a0, fcsr, zero
	-[0x8000c174]:sw t6, 136(t1)
Current Store : [0x8000c178] : sw a0, 140(t1) -- Store: [0x80014070]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c1ac]:feq.h t6, ft11, ft10
	-[0x8000c1b0]:csrrs a0, fcsr, zero
	-[0x8000c1b4]:sw t6, 144(t1)
Current Store : [0x8000c1b8] : sw a0, 148(t1) -- Store: [0x80014078]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c1ec]:feq.h t6, ft11, ft10
	-[0x8000c1f0]:csrrs a0, fcsr, zero
	-[0x8000c1f4]:sw t6, 152(t1)
Current Store : [0x8000c1f8] : sw a0, 156(t1) -- Store: [0x80014080]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c22c]:feq.h t6, ft11, ft10
	-[0x8000c230]:csrrs a0, fcsr, zero
	-[0x8000c234]:sw t6, 160(t1)
Current Store : [0x8000c238] : sw a0, 164(t1) -- Store: [0x80014088]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c26c]:feq.h t6, ft11, ft10
	-[0x8000c270]:csrrs a0, fcsr, zero
	-[0x8000c274]:sw t6, 168(t1)
Current Store : [0x8000c278] : sw a0, 172(t1) -- Store: [0x80014090]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c2ac]:feq.h t6, ft11, ft10
	-[0x8000c2b0]:csrrs a0, fcsr, zero
	-[0x8000c2b4]:sw t6, 176(t1)
Current Store : [0x8000c2b8] : sw a0, 180(t1) -- Store: [0x80014098]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c2ec]:feq.h t6, ft11, ft10
	-[0x8000c2f0]:csrrs a0, fcsr, zero
	-[0x8000c2f4]:sw t6, 184(t1)
Current Store : [0x8000c2f8] : sw a0, 188(t1) -- Store: [0x800140a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c32c]:feq.h t6, ft11, ft10
	-[0x8000c330]:csrrs a0, fcsr, zero
	-[0x8000c334]:sw t6, 192(t1)
Current Store : [0x8000c338] : sw a0, 196(t1) -- Store: [0x800140a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c36c]:feq.h t6, ft11, ft10
	-[0x8000c370]:csrrs a0, fcsr, zero
	-[0x8000c374]:sw t6, 200(t1)
Current Store : [0x8000c378] : sw a0, 204(t1) -- Store: [0x800140b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c3ac]:feq.h t6, ft11, ft10
	-[0x8000c3b0]:csrrs a0, fcsr, zero
	-[0x8000c3b4]:sw t6, 208(t1)
Current Store : [0x8000c3b8] : sw a0, 212(t1) -- Store: [0x800140b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c3ec]:feq.h t6, ft11, ft10
	-[0x8000c3f0]:csrrs a0, fcsr, zero
	-[0x8000c3f4]:sw t6, 216(t1)
Current Store : [0x8000c3f8] : sw a0, 220(t1) -- Store: [0x800140c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c42c]:feq.h t6, ft11, ft10
	-[0x8000c430]:csrrs a0, fcsr, zero
	-[0x8000c434]:sw t6, 224(t1)
Current Store : [0x8000c438] : sw a0, 228(t1) -- Store: [0x800140c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c46c]:feq.h t6, ft11, ft10
	-[0x8000c470]:csrrs a0, fcsr, zero
	-[0x8000c474]:sw t6, 232(t1)
Current Store : [0x8000c478] : sw a0, 236(t1) -- Store: [0x800140d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c4ac]:feq.h t6, ft11, ft10
	-[0x8000c4b0]:csrrs a0, fcsr, zero
	-[0x8000c4b4]:sw t6, 240(t1)
Current Store : [0x8000c4b8] : sw a0, 244(t1) -- Store: [0x800140d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c4ec]:feq.h t6, ft11, ft10
	-[0x8000c4f0]:csrrs a0, fcsr, zero
	-[0x8000c4f4]:sw t6, 248(t1)
Current Store : [0x8000c4f8] : sw a0, 252(t1) -- Store: [0x800140e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c52c]:feq.h t6, ft11, ft10
	-[0x8000c530]:csrrs a0, fcsr, zero
	-[0x8000c534]:sw t6, 256(t1)
Current Store : [0x8000c538] : sw a0, 260(t1) -- Store: [0x800140e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c56c]:feq.h t6, ft11, ft10
	-[0x8000c570]:csrrs a0, fcsr, zero
	-[0x8000c574]:sw t6, 264(t1)
Current Store : [0x8000c578] : sw a0, 268(t1) -- Store: [0x800140f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c5ac]:feq.h t6, ft11, ft10
	-[0x8000c5b0]:csrrs a0, fcsr, zero
	-[0x8000c5b4]:sw t6, 272(t1)
Current Store : [0x8000c5b8] : sw a0, 276(t1) -- Store: [0x800140f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c5ec]:feq.h t6, ft11, ft10
	-[0x8000c5f0]:csrrs a0, fcsr, zero
	-[0x8000c5f4]:sw t6, 280(t1)
Current Store : [0x8000c5f8] : sw a0, 284(t1) -- Store: [0x80014100]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c62c]:feq.h t6, ft11, ft10
	-[0x8000c630]:csrrs a0, fcsr, zero
	-[0x8000c634]:sw t6, 288(t1)
Current Store : [0x8000c638] : sw a0, 292(t1) -- Store: [0x80014108]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c66c]:feq.h t6, ft11, ft10
	-[0x8000c670]:csrrs a0, fcsr, zero
	-[0x8000c674]:sw t6, 296(t1)
Current Store : [0x8000c678] : sw a0, 300(t1) -- Store: [0x80014110]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c6ac]:feq.h t6, ft11, ft10
	-[0x8000c6b0]:csrrs a0, fcsr, zero
	-[0x8000c6b4]:sw t6, 304(t1)
Current Store : [0x8000c6b8] : sw a0, 308(t1) -- Store: [0x80014118]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1a and fm1 == 0x250 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c6ec]:feq.h t6, ft11, ft10
	-[0x8000c6f0]:csrrs a0, fcsr, zero
	-[0x8000c6f4]:sw t6, 312(t1)
Current Store : [0x8000c6f8] : sw a0, 316(t1) -- Store: [0x80014120]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1a and fm2 == 0x250 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c72c]:feq.h t6, ft11, ft10
	-[0x8000c730]:csrrs a0, fcsr, zero
	-[0x8000c734]:sw t6, 320(t1)
Current Store : [0x8000c738] : sw a0, 324(t1) -- Store: [0x80014128]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c76c]:feq.h t6, ft11, ft10
	-[0x8000c770]:csrrs a0, fcsr, zero
	-[0x8000c774]:sw t6, 328(t1)
Current Store : [0x8000c778] : sw a0, 332(t1) -- Store: [0x80014130]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c7ac]:feq.h t6, ft11, ft10
	-[0x8000c7b0]:csrrs a0, fcsr, zero
	-[0x8000c7b4]:sw t6, 336(t1)
Current Store : [0x8000c7b8] : sw a0, 340(t1) -- Store: [0x80014138]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c7ec]:feq.h t6, ft11, ft10
	-[0x8000c7f0]:csrrs a0, fcsr, zero
	-[0x8000c7f4]:sw t6, 344(t1)
Current Store : [0x8000c7f8] : sw a0, 348(t1) -- Store: [0x80014140]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x036 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c82c]:feq.h t6, ft11, ft10
	-[0x8000c830]:csrrs a0, fcsr, zero
	-[0x8000c834]:sw t6, 352(t1)
Current Store : [0x8000c838] : sw a0, 356(t1) -- Store: [0x80014148]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x036 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c86c]:feq.h t6, ft11, ft10
	-[0x8000c870]:csrrs a0, fcsr, zero
	-[0x8000c874]:sw t6, 360(t1)
Current Store : [0x8000c878] : sw a0, 364(t1) -- Store: [0x80014150]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c8ac]:feq.h t6, ft11, ft10
	-[0x8000c8b0]:csrrs a0, fcsr, zero
	-[0x8000c8b4]:sw t6, 368(t1)
Current Store : [0x8000c8b8] : sw a0, 372(t1) -- Store: [0x80014158]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c8ec]:feq.h t6, ft11, ft10
	-[0x8000c8f0]:csrrs a0, fcsr, zero
	-[0x8000c8f4]:sw t6, 376(t1)
Current Store : [0x8000c8f8] : sw a0, 380(t1) -- Store: [0x80014160]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c92c]:feq.h t6, ft11, ft10
	-[0x8000c930]:csrrs a0, fcsr, zero
	-[0x8000c934]:sw t6, 384(t1)
Current Store : [0x8000c938] : sw a0, 388(t1) -- Store: [0x80014168]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c96c]:feq.h t6, ft11, ft10
	-[0x8000c970]:csrrs a0, fcsr, zero
	-[0x8000c974]:sw t6, 392(t1)
Current Store : [0x8000c978] : sw a0, 396(t1) -- Store: [0x80014170]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c9ac]:feq.h t6, ft11, ft10
	-[0x8000c9b0]:csrrs a0, fcsr, zero
	-[0x8000c9b4]:sw t6, 400(t1)
Current Store : [0x8000c9b8] : sw a0, 404(t1) -- Store: [0x80014178]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x10 and fm1 == 0x277 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000c9ec]:feq.h t6, ft11, ft10
	-[0x8000c9f0]:csrrs a0, fcsr, zero
	-[0x8000c9f4]:sw t6, 408(t1)
Current Store : [0x8000c9f8] : sw a0, 412(t1) -- Store: [0x80014180]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x277 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ca2c]:feq.h t6, ft11, ft10
	-[0x8000ca30]:csrrs a0, fcsr, zero
	-[0x8000ca34]:sw t6, 416(t1)
Current Store : [0x8000ca38] : sw a0, 420(t1) -- Store: [0x80014188]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x10 and fm2 == 0x277 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ca6c]:feq.h t6, ft11, ft10
	-[0x8000ca70]:csrrs a0, fcsr, zero
	-[0x8000ca74]:sw t6, 424(t1)
Current Store : [0x8000ca78] : sw a0, 428(t1) -- Store: [0x80014190]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000caac]:feq.h t6, ft11, ft10
	-[0x8000cab0]:csrrs a0, fcsr, zero
	-[0x8000cab4]:sw t6, 432(t1)
Current Store : [0x8000cab8] : sw a0, 436(t1) -- Store: [0x80014198]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000caec]:feq.h t6, ft11, ft10
	-[0x8000caf0]:csrrs a0, fcsr, zero
	-[0x8000caf4]:sw t6, 440(t1)
Current Store : [0x8000caf8] : sw a0, 444(t1) -- Store: [0x800141a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cb2c]:feq.h t6, ft11, ft10
	-[0x8000cb30]:csrrs a0, fcsr, zero
	-[0x8000cb34]:sw t6, 448(t1)
Current Store : [0x8000cb38] : sw a0, 452(t1) -- Store: [0x800141a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cb6c]:feq.h t6, ft11, ft10
	-[0x8000cb70]:csrrs a0, fcsr, zero
	-[0x8000cb74]:sw t6, 456(t1)
Current Store : [0x8000cb78] : sw a0, 460(t1) -- Store: [0x800141b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cbac]:feq.h t6, ft11, ft10
	-[0x8000cbb0]:csrrs a0, fcsr, zero
	-[0x8000cbb4]:sw t6, 464(t1)
Current Store : [0x8000cbb8] : sw a0, 468(t1) -- Store: [0x800141b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cbec]:feq.h t6, ft11, ft10
	-[0x8000cbf0]:csrrs a0, fcsr, zero
	-[0x8000cbf4]:sw t6, 472(t1)
Current Store : [0x8000cbf8] : sw a0, 476(t1) -- Store: [0x800141c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cc2c]:feq.h t6, ft11, ft10
	-[0x8000cc30]:csrrs a0, fcsr, zero
	-[0x8000cc34]:sw t6, 480(t1)
Current Store : [0x8000cc38] : sw a0, 484(t1) -- Store: [0x800141c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cc6c]:feq.h t6, ft11, ft10
	-[0x8000cc70]:csrrs a0, fcsr, zero
	-[0x8000cc74]:sw t6, 488(t1)
Current Store : [0x8000cc78] : sw a0, 492(t1) -- Store: [0x800141d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ccac]:feq.h t6, ft11, ft10
	-[0x8000ccb0]:csrrs a0, fcsr, zero
	-[0x8000ccb4]:sw t6, 496(t1)
Current Store : [0x8000ccb8] : sw a0, 500(t1) -- Store: [0x800141d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ccec]:feq.h t6, ft11, ft10
	-[0x8000ccf0]:csrrs a0, fcsr, zero
	-[0x8000ccf4]:sw t6, 504(t1)
Current Store : [0x8000ccf8] : sw a0, 508(t1) -- Store: [0x800141e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cd2c]:feq.h t6, ft11, ft10
	-[0x8000cd30]:csrrs a0, fcsr, zero
	-[0x8000cd34]:sw t6, 512(t1)
Current Store : [0x8000cd38] : sw a0, 516(t1) -- Store: [0x800141e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cd6c]:feq.h t6, ft11, ft10
	-[0x8000cd70]:csrrs a0, fcsr, zero
	-[0x8000cd74]:sw t6, 520(t1)
Current Store : [0x8000cd78] : sw a0, 524(t1) -- Store: [0x800141f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cdac]:feq.h t6, ft11, ft10
	-[0x8000cdb0]:csrrs a0, fcsr, zero
	-[0x8000cdb4]:sw t6, 528(t1)
Current Store : [0x8000cdb8] : sw a0, 532(t1) -- Store: [0x800141f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cdec]:feq.h t6, ft11, ft10
	-[0x8000cdf0]:csrrs a0, fcsr, zero
	-[0x8000cdf4]:sw t6, 536(t1)
Current Store : [0x8000cdf8] : sw a0, 540(t1) -- Store: [0x80014200]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ce2c]:feq.h t6, ft11, ft10
	-[0x8000ce30]:csrrs a0, fcsr, zero
	-[0x8000ce34]:sw t6, 544(t1)
Current Store : [0x8000ce38] : sw a0, 548(t1) -- Store: [0x80014208]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ce6c]:feq.h t6, ft11, ft10
	-[0x8000ce70]:csrrs a0, fcsr, zero
	-[0x8000ce74]:sw t6, 552(t1)
Current Store : [0x8000ce78] : sw a0, 556(t1) -- Store: [0x80014210]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ceac]:feq.h t6, ft11, ft10
	-[0x8000ceb0]:csrrs a0, fcsr, zero
	-[0x8000ceb4]:sw t6, 560(t1)
Current Store : [0x8000ceb8] : sw a0, 564(t1) -- Store: [0x80014218]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ceec]:feq.h t6, ft11, ft10
	-[0x8000cef0]:csrrs a0, fcsr, zero
	-[0x8000cef4]:sw t6, 568(t1)
Current Store : [0x8000cef8] : sw a0, 572(t1) -- Store: [0x80014220]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cf2c]:feq.h t6, ft11, ft10
	-[0x8000cf30]:csrrs a0, fcsr, zero
	-[0x8000cf34]:sw t6, 576(t1)
Current Store : [0x8000cf38] : sw a0, 580(t1) -- Store: [0x80014228]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cf6c]:feq.h t6, ft11, ft10
	-[0x8000cf70]:csrrs a0, fcsr, zero
	-[0x8000cf74]:sw t6, 584(t1)
Current Store : [0x8000cf78] : sw a0, 588(t1) -- Store: [0x80014230]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cfac]:feq.h t6, ft11, ft10
	-[0x8000cfb0]:csrrs a0, fcsr, zero
	-[0x8000cfb4]:sw t6, 592(t1)
Current Store : [0x8000cfb8] : sw a0, 596(t1) -- Store: [0x80014238]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1b and fm1 == 0x10f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000cfec]:feq.h t6, ft11, ft10
	-[0x8000cff0]:csrrs a0, fcsr, zero
	-[0x8000cff4]:sw t6, 600(t1)
Current Store : [0x8000cff8] : sw a0, 604(t1) -- Store: [0x80014240]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1b and fm2 == 0x10f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d02c]:feq.h t6, ft11, ft10
	-[0x8000d030]:csrrs a0, fcsr, zero
	-[0x8000d034]:sw t6, 608(t1)
Current Store : [0x8000d038] : sw a0, 612(t1) -- Store: [0x80014248]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d06c]:feq.h t6, ft11, ft10
	-[0x8000d070]:csrrs a0, fcsr, zero
	-[0x8000d074]:sw t6, 616(t1)
Current Store : [0x8000d078] : sw a0, 620(t1) -- Store: [0x80014250]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x008 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d0ac]:feq.h t6, ft11, ft10
	-[0x8000d0b0]:csrrs a0, fcsr, zero
	-[0x8000d0b4]:sw t6, 624(t1)
Current Store : [0x8000d0b8] : sw a0, 628(t1) -- Store: [0x80014258]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d0ec]:feq.h t6, ft11, ft10
	-[0x8000d0f0]:csrrs a0, fcsr, zero
	-[0x8000d0f4]:sw t6, 632(t1)
Current Store : [0x8000d0f8] : sw a0, 636(t1) -- Store: [0x80014260]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x056 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d12c]:feq.h t6, ft11, ft10
	-[0x8000d130]:csrrs a0, fcsr, zero
	-[0x8000d134]:sw t6, 640(t1)
Current Store : [0x8000d138] : sw a0, 644(t1) -- Store: [0x80014268]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x056 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d16c]:feq.h t6, ft11, ft10
	-[0x8000d170]:csrrs a0, fcsr, zero
	-[0x8000d174]:sw t6, 648(t1)
Current Store : [0x8000d178] : sw a0, 652(t1) -- Store: [0x80014270]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d1ac]:feq.h t6, ft11, ft10
	-[0x8000d1b0]:csrrs a0, fcsr, zero
	-[0x8000d1b4]:sw t6, 656(t1)
Current Store : [0x8000d1b8] : sw a0, 660(t1) -- Store: [0x80014278]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d1ec]:feq.h t6, ft11, ft10
	-[0x8000d1f0]:csrrs a0, fcsr, zero
	-[0x8000d1f4]:sw t6, 664(t1)
Current Store : [0x8000d1f8] : sw a0, 668(t1) -- Store: [0x80014280]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d22c]:feq.h t6, ft11, ft10
	-[0x8000d230]:csrrs a0, fcsr, zero
	-[0x8000d234]:sw t6, 672(t1)
Current Store : [0x8000d238] : sw a0, 676(t1) -- Store: [0x80014288]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x11 and fm1 == 0x12e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d26c]:feq.h t6, ft11, ft10
	-[0x8000d270]:csrrs a0, fcsr, zero
	-[0x8000d274]:sw t6, 680(t1)
Current Store : [0x8000d278] : sw a0, 684(t1) -- Store: [0x80014290]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x12e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d2ac]:feq.h t6, ft11, ft10
	-[0x8000d2b0]:csrrs a0, fcsr, zero
	-[0x8000d2b4]:sw t6, 688(t1)
Current Store : [0x8000d2b8] : sw a0, 692(t1) -- Store: [0x80014298]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x12e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d2ec]:feq.h t6, ft11, ft10
	-[0x8000d2f0]:csrrs a0, fcsr, zero
	-[0x8000d2f4]:sw t6, 696(t1)
Current Store : [0x8000d2f8] : sw a0, 700(t1) -- Store: [0x800142a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d32c]:feq.h t6, ft11, ft10
	-[0x8000d330]:csrrs a0, fcsr, zero
	-[0x8000d334]:sw t6, 704(t1)
Current Store : [0x8000d338] : sw a0, 708(t1) -- Store: [0x800142a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d36c]:feq.h t6, ft11, ft10
	-[0x8000d370]:csrrs a0, fcsr, zero
	-[0x8000d374]:sw t6, 712(t1)
Current Store : [0x8000d378] : sw a0, 716(t1) -- Store: [0x800142b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d3ac]:feq.h t6, ft11, ft10
	-[0x8000d3b0]:csrrs a0, fcsr, zero
	-[0x8000d3b4]:sw t6, 720(t1)
Current Store : [0x8000d3b8] : sw a0, 724(t1) -- Store: [0x800142b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d3ec]:feq.h t6, ft11, ft10
	-[0x8000d3f0]:csrrs a0, fcsr, zero
	-[0x8000d3f4]:sw t6, 728(t1)
Current Store : [0x8000d3f8] : sw a0, 732(t1) -- Store: [0x800142c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d42c]:feq.h t6, ft11, ft10
	-[0x8000d430]:csrrs a0, fcsr, zero
	-[0x8000d434]:sw t6, 736(t1)
Current Store : [0x8000d438] : sw a0, 740(t1) -- Store: [0x800142c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d46c]:feq.h t6, ft11, ft10
	-[0x8000d470]:csrrs a0, fcsr, zero
	-[0x8000d474]:sw t6, 744(t1)
Current Store : [0x8000d478] : sw a0, 748(t1) -- Store: [0x800142d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d4ac]:feq.h t6, ft11, ft10
	-[0x8000d4b0]:csrrs a0, fcsr, zero
	-[0x8000d4b4]:sw t6, 752(t1)
Current Store : [0x8000d4b8] : sw a0, 756(t1) -- Store: [0x800142d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d4ec]:feq.h t6, ft11, ft10
	-[0x8000d4f0]:csrrs a0, fcsr, zero
	-[0x8000d4f4]:sw t6, 760(t1)
Current Store : [0x8000d4f8] : sw a0, 764(t1) -- Store: [0x800142e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d52c]:feq.h t6, ft11, ft10
	-[0x8000d530]:csrrs a0, fcsr, zero
	-[0x8000d534]:sw t6, 768(t1)
Current Store : [0x8000d538] : sw a0, 772(t1) -- Store: [0x800142e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d56c]:feq.h t6, ft11, ft10
	-[0x8000d570]:csrrs a0, fcsr, zero
	-[0x8000d574]:sw t6, 776(t1)
Current Store : [0x8000d578] : sw a0, 780(t1) -- Store: [0x800142f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d5ac]:feq.h t6, ft11, ft10
	-[0x8000d5b0]:csrrs a0, fcsr, zero
	-[0x8000d5b4]:sw t6, 784(t1)
Current Store : [0x8000d5b8] : sw a0, 788(t1) -- Store: [0x800142f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d5ec]:feq.h t6, ft11, ft10
	-[0x8000d5f0]:csrrs a0, fcsr, zero
	-[0x8000d5f4]:sw t6, 792(t1)
Current Store : [0x8000d5f8] : sw a0, 796(t1) -- Store: [0x80014300]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d62c]:feq.h t6, ft11, ft10
	-[0x8000d630]:csrrs a0, fcsr, zero
	-[0x8000d634]:sw t6, 800(t1)
Current Store : [0x8000d638] : sw a0, 804(t1) -- Store: [0x80014308]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d66c]:feq.h t6, ft11, ft10
	-[0x8000d670]:csrrs a0, fcsr, zero
	-[0x8000d674]:sw t6, 808(t1)
Current Store : [0x8000d678] : sw a0, 812(t1) -- Store: [0x80014310]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d6ac]:feq.h t6, ft11, ft10
	-[0x8000d6b0]:csrrs a0, fcsr, zero
	-[0x8000d6b4]:sw t6, 816(t1)
Current Store : [0x8000d6b8] : sw a0, 820(t1) -- Store: [0x80014318]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d6ec]:feq.h t6, ft11, ft10
	-[0x8000d6f0]:csrrs a0, fcsr, zero
	-[0x8000d6f4]:sw t6, 824(t1)
Current Store : [0x8000d6f8] : sw a0, 828(t1) -- Store: [0x80014320]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d72c]:feq.h t6, ft11, ft10
	-[0x8000d730]:csrrs a0, fcsr, zero
	-[0x8000d734]:sw t6, 832(t1)
Current Store : [0x8000d738] : sw a0, 836(t1) -- Store: [0x80014328]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d76c]:feq.h t6, ft11, ft10
	-[0x8000d770]:csrrs a0, fcsr, zero
	-[0x8000d774]:sw t6, 840(t1)
Current Store : [0x8000d778] : sw a0, 844(t1) -- Store: [0x80014330]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d7ac]:feq.h t6, ft11, ft10
	-[0x8000d7b0]:csrrs a0, fcsr, zero
	-[0x8000d7b4]:sw t6, 848(t1)
Current Store : [0x8000d7b8] : sw a0, 852(t1) -- Store: [0x80014338]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d7ec]:feq.h t6, ft11, ft10
	-[0x8000d7f0]:csrrs a0, fcsr, zero
	-[0x8000d7f4]:sw t6, 856(t1)
Current Store : [0x8000d7f8] : sw a0, 860(t1) -- Store: [0x80014340]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d82c]:feq.h t6, ft11, ft10
	-[0x8000d830]:csrrs a0, fcsr, zero
	-[0x8000d834]:sw t6, 864(t1)
Current Store : [0x8000d838] : sw a0, 868(t1) -- Store: [0x80014348]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x19 and fm1 == 0x22e and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d86c]:feq.h t6, ft11, ft10
	-[0x8000d870]:csrrs a0, fcsr, zero
	-[0x8000d874]:sw t6, 872(t1)
Current Store : [0x8000d878] : sw a0, 876(t1) -- Store: [0x80014350]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x19 and fm2 == 0x22e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d8ac]:feq.h t6, ft11, ft10
	-[0x8000d8b0]:csrrs a0, fcsr, zero
	-[0x8000d8b4]:sw t6, 880(t1)
Current Store : [0x8000d8b8] : sw a0, 884(t1) -- Store: [0x80014358]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d8ec]:feq.h t6, ft11, ft10
	-[0x8000d8f0]:csrrs a0, fcsr, zero
	-[0x8000d8f4]:sw t6, 888(t1)
Current Store : [0x8000d8f8] : sw a0, 892(t1) -- Store: [0x80014360]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d92c]:feq.h t6, ft11, ft10
	-[0x8000d930]:csrrs a0, fcsr, zero
	-[0x8000d934]:sw t6, 896(t1)
Current Store : [0x8000d938] : sw a0, 900(t1) -- Store: [0x80014368]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d96c]:feq.h t6, ft11, ft10
	-[0x8000d970]:csrrs a0, fcsr, zero
	-[0x8000d974]:sw t6, 904(t1)
Current Store : [0x8000d978] : sw a0, 908(t1) -- Store: [0x80014370]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d9ac]:feq.h t6, ft11, ft10
	-[0x8000d9b0]:csrrs a0, fcsr, zero
	-[0x8000d9b4]:sw t6, 912(t1)
Current Store : [0x8000d9b8] : sw a0, 916(t1) -- Store: [0x80014378]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x01a and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000d9ec]:feq.h t6, ft11, ft10
	-[0x8000d9f0]:csrrs a0, fcsr, zero
	-[0x8000d9f4]:sw t6, 920(t1)
Current Store : [0x8000d9f8] : sw a0, 924(t1) -- Store: [0x80014380]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x01a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000da2c]:feq.h t6, ft11, ft10
	-[0x8000da30]:csrrs a0, fcsr, zero
	-[0x8000da34]:sw t6, 928(t1)
Current Store : [0x8000da38] : sw a0, 932(t1) -- Store: [0x80014388]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000da6c]:feq.h t6, ft11, ft10
	-[0x8000da70]:csrrs a0, fcsr, zero
	-[0x8000da74]:sw t6, 936(t1)
Current Store : [0x8000da78] : sw a0, 940(t1) -- Store: [0x80014390]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x254 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000daac]:feq.h t6, ft11, ft10
	-[0x8000dab0]:csrrs a0, fcsr, zero
	-[0x8000dab4]:sw t6, 944(t1)
Current Store : [0x8000dab8] : sw a0, 948(t1) -- Store: [0x80014398]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x254 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000daec]:feq.h t6, ft11, ft10
	-[0x8000daf0]:csrrs a0, fcsr, zero
	-[0x8000daf4]:sw t6, 952(t1)
Current Store : [0x8000daf8] : sw a0, 956(t1) -- Store: [0x800143a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x254 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000db2c]:feq.h t6, ft11, ft10
	-[0x8000db30]:csrrs a0, fcsr, zero
	-[0x8000db34]:sw t6, 960(t1)
Current Store : [0x8000db38] : sw a0, 964(t1) -- Store: [0x800143a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000db6c]:feq.h t6, ft11, ft10
	-[0x8000db70]:csrrs a0, fcsr, zero
	-[0x8000db74]:sw t6, 968(t1)
Current Store : [0x8000db78] : sw a0, 972(t1) -- Store: [0x800143b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dbac]:feq.h t6, ft11, ft10
	-[0x8000dbb0]:csrrs a0, fcsr, zero
	-[0x8000dbb4]:sw t6, 976(t1)
Current Store : [0x8000dbb8] : sw a0, 980(t1) -- Store: [0x800143b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dbec]:feq.h t6, ft11, ft10
	-[0x8000dbf0]:csrrs a0, fcsr, zero
	-[0x8000dbf4]:sw t6, 984(t1)
Current Store : [0x8000dbf8] : sw a0, 988(t1) -- Store: [0x800143c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dc2c]:feq.h t6, ft11, ft10
	-[0x8000dc30]:csrrs a0, fcsr, zero
	-[0x8000dc34]:sw t6, 992(t1)
Current Store : [0x8000dc38] : sw a0, 996(t1) -- Store: [0x800143c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dc64]:feq.h t6, ft11, ft10
	-[0x8000dc68]:csrrs a0, fcsr, zero
	-[0x8000dc6c]:sw t6, 1000(t1)
Current Store : [0x8000dc70] : sw a0, 1004(t1) -- Store: [0x800143d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dc9c]:feq.h t6, ft11, ft10
	-[0x8000dca0]:csrrs a0, fcsr, zero
	-[0x8000dca4]:sw t6, 1008(t1)
Current Store : [0x8000dca8] : sw a0, 1012(t1) -- Store: [0x800143d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dcd4]:feq.h t6, ft11, ft10
	-[0x8000dcd8]:csrrs a0, fcsr, zero
	-[0x8000dcdc]:sw t6, 1016(t1)
Current Store : [0x8000dce0] : sw a0, 1020(t1) -- Store: [0x800143e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dd14]:feq.h t6, ft11, ft10
	-[0x8000dd18]:csrrs a0, fcsr, zero
	-[0x8000dd1c]:sw t6, 0(t1)
Current Store : [0x8000dd20] : sw a0, 4(t1) -- Store: [0x800143e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dd4c]:feq.h t6, ft11, ft10
	-[0x8000dd50]:csrrs a0, fcsr, zero
	-[0x8000dd54]:sw t6, 8(t1)
Current Store : [0x8000dd58] : sw a0, 12(t1) -- Store: [0x800143f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dd84]:feq.h t6, ft11, ft10
	-[0x8000dd88]:csrrs a0, fcsr, zero
	-[0x8000dd8c]:sw t6, 16(t1)
Current Store : [0x8000dd90] : sw a0, 20(t1) -- Store: [0x800143f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ddbc]:feq.h t6, ft11, ft10
	-[0x8000ddc0]:csrrs a0, fcsr, zero
	-[0x8000ddc4]:sw t6, 24(t1)
Current Store : [0x8000ddc8] : sw a0, 28(t1) -- Store: [0x80014400]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ddf4]:feq.h t6, ft11, ft10
	-[0x8000ddf8]:csrrs a0, fcsr, zero
	-[0x8000ddfc]:sw t6, 32(t1)
Current Store : [0x8000de00] : sw a0, 36(t1) -- Store: [0x80014408]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000de2c]:feq.h t6, ft11, ft10
	-[0x8000de30]:csrrs a0, fcsr, zero
	-[0x8000de34]:sw t6, 40(t1)
Current Store : [0x8000de38] : sw a0, 44(t1) -- Store: [0x80014410]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000de64]:feq.h t6, ft11, ft10
	-[0x8000de68]:csrrs a0, fcsr, zero
	-[0x8000de6c]:sw t6, 48(t1)
Current Store : [0x8000de70] : sw a0, 52(t1) -- Store: [0x80014418]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000de9c]:feq.h t6, ft11, ft10
	-[0x8000dea0]:csrrs a0, fcsr, zero
	-[0x8000dea4]:sw t6, 56(t1)
Current Store : [0x8000dea8] : sw a0, 60(t1) -- Store: [0x80014420]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000ded4]:feq.h t6, ft11, ft10
	-[0x8000ded8]:csrrs a0, fcsr, zero
	-[0x8000dedc]:sw t6, 64(t1)
Current Store : [0x8000dee0] : sw a0, 68(t1) -- Store: [0x80014428]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000df0c]:feq.h t6, ft11, ft10
	-[0x8000df10]:csrrs a0, fcsr, zero
	-[0x8000df14]:sw t6, 72(t1)
Current Store : [0x8000df18] : sw a0, 76(t1) -- Store: [0x80014430]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000df44]:feq.h t6, ft11, ft10
	-[0x8000df48]:csrrs a0, fcsr, zero
	-[0x8000df4c]:sw t6, 80(t1)
Current Store : [0x8000df50] : sw a0, 84(t1) -- Store: [0x80014438]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000df7c]:feq.h t6, ft11, ft10
	-[0x8000df80]:csrrs a0, fcsr, zero
	-[0x8000df84]:sw t6, 88(t1)
Current Store : [0x8000df88] : sw a0, 92(t1) -- Store: [0x80014440]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dfb4]:feq.h t6, ft11, ft10
	-[0x8000dfb8]:csrrs a0, fcsr, zero
	-[0x8000dfbc]:sw t6, 96(t1)
Current Store : [0x8000dfc0] : sw a0, 100(t1) -- Store: [0x80014448]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000dfec]:feq.h t6, ft11, ft10
	-[0x8000dff0]:csrrs a0, fcsr, zero
	-[0x8000dff4]:sw t6, 104(t1)
Current Store : [0x8000dff8] : sw a0, 108(t1) -- Store: [0x80014450]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000e024]:feq.h t6, ft11, ft10
	-[0x8000e028]:csrrs a0, fcsr, zero
	-[0x8000e02c]:sw t6, 112(t1)
Current Store : [0x8000e030] : sw a0, 116(t1) -- Store: [0x80014458]:0x00000000




Last Coverpoint : ['mnemonic : feq.h', 'rs1 : f31', 'rs2 : f30', 'rd : x31', 'rs1 != rs2', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000e05c]:feq.h t6, ft11, ft10
	-[0x8000e060]:csrrs a0, fcsr, zero
	-[0x8000e064]:sw t6, 120(t1)
Current Store : [0x8000e068] : sw a0, 124(t1) -- Store: [0x80014460]:0x00000000





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

|s.no|        signature         |                                                                                                                             coverpoints                                                                                                                              |                                                     code                                                      |
|---:|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
|   1|[0x80012314]<br>0x00000000|- mnemonic : feq.h<br> - rs1 : f31<br> - rs2 : f30<br> - rd : x31<br> - rs1 != rs2<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br> |[0x80000124]:feq.h t6, ft11, ft10<br> [0x80000128]:csrrs tp, fcsr, zero<br> [0x8000012c]:sw t6, 0(ra)<br>      |
|   2|[0x8001231c]<br>0x00000000|- rs1 : f29<br> - rs2 : f29<br> - rd : x30<br> - rs1 == rs2<br>                                                                                                                                                                                                       |[0x80000144]:feq.h t5, ft9, ft9<br> [0x80000148]:csrrs tp, fcsr, zero<br> [0x8000014c]:sw t5, 8(ra)<br>        |
|   3|[0x80012324]<br>0x00000000|- rs1 : f30<br> - rs2 : f31<br> - rd : x29<br> - fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000164]:feq.h t4, ft10, ft11<br> [0x80000168]:csrrs tp, fcsr, zero<br> [0x8000016c]:sw t4, 16(ra)<br>     |
|   4|[0x8001232c]<br>0x00000000|- rs1 : f28<br> - rs2 : f27<br> - rd : x28<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000184]:feq.h t3, ft8, fs11<br> [0x80000188]:csrrs tp, fcsr, zero<br> [0x8000018c]:sw t3, 24(ra)<br>      |
|   5|[0x80012334]<br>0x00000000|- rs1 : f27<br> - rs2 : f28<br> - rd : x27<br> - fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800001a4]:feq.h s11, fs11, ft8<br> [0x800001a8]:csrrs tp, fcsr, zero<br> [0x800001ac]:sw s11, 32(ra)<br>    |
|   6|[0x8001233c]<br>0x00000000|- rs1 : f26<br> - rs2 : f25<br> - rd : x26<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800001c4]:feq.h s10, fs10, fs9<br> [0x800001c8]:csrrs tp, fcsr, zero<br> [0x800001cc]:sw s10, 40(ra)<br>    |
|   7|[0x80012344]<br>0x00000000|- rs1 : f25<br> - rs2 : f26<br> - rd : x25<br> - fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800001e4]:feq.h s9, fs9, fs10<br> [0x800001e8]:csrrs tp, fcsr, zero<br> [0x800001ec]:sw s9, 48(ra)<br>      |
|   8|[0x8001234c]<br>0x00000000|- rs1 : f24<br> - rs2 : f23<br> - rd : x24<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000204]:feq.h s8, fs8, fs7<br> [0x80000208]:csrrs tp, fcsr, zero<br> [0x8000020c]:sw s8, 56(ra)<br>       |
|   9|[0x80012354]<br>0x00000000|- rs1 : f23<br> - rs2 : f24<br> - rd : x23<br> - fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000224]:feq.h s7, fs7, fs8<br> [0x80000228]:csrrs tp, fcsr, zero<br> [0x8000022c]:sw s7, 64(ra)<br>       |
|  10|[0x8001235c]<br>0x00000000|- rs1 : f22<br> - rs2 : f21<br> - rd : x22<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000244]:feq.h s6, fs6, fs5<br> [0x80000248]:csrrs tp, fcsr, zero<br> [0x8000024c]:sw s6, 72(ra)<br>       |
|  11|[0x80012364]<br>0x00000000|- rs1 : f21<br> - rs2 : f22<br> - rd : x21<br> - fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000264]:feq.h s5, fs5, fs6<br> [0x80000268]:csrrs tp, fcsr, zero<br> [0x8000026c]:sw s5, 80(ra)<br>       |
|  12|[0x8001236c]<br>0x00000000|- rs1 : f20<br> - rs2 : f19<br> - rd : x20<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000284]:feq.h s4, fs4, fs3<br> [0x80000288]:csrrs tp, fcsr, zero<br> [0x8000028c]:sw s4, 88(ra)<br>       |
|  13|[0x80012374]<br>0x00000000|- rs1 : f19<br> - rs2 : f20<br> - rd : x19<br> - fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800002a4]:feq.h s3, fs3, fs4<br> [0x800002a8]:csrrs tp, fcsr, zero<br> [0x800002ac]:sw s3, 96(ra)<br>       |
|  14|[0x8001237c]<br>0x00000000|- rs1 : f18<br> - rs2 : f17<br> - rd : x18<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800002c4]:feq.h s2, fs2, fa7<br> [0x800002c8]:csrrs tp, fcsr, zero<br> [0x800002cc]:sw s2, 104(ra)<br>      |
|  15|[0x80012384]<br>0x00000000|- rs1 : f17<br> - rs2 : f18<br> - rd : x17<br> - fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800002e4]:feq.h a7, fa7, fs2<br> [0x800002e8]:csrrs tp, fcsr, zero<br> [0x800002ec]:sw a7, 112(ra)<br>      |
|  16|[0x8001238c]<br>0x00000000|- rs1 : f16<br> - rs2 : f15<br> - rd : x16<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000304]:feq.h a6, fa6, fa5<br> [0x80000308]:csrrs tp, fcsr, zero<br> [0x8000030c]:sw a6, 120(ra)<br>      |
|  17|[0x80012394]<br>0x00000000|- rs1 : f15<br> - rs2 : f16<br> - rd : x15<br> - fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000324]:feq.h a5, fa5, fa6<br> [0x80000328]:csrrs tp, fcsr, zero<br> [0x8000032c]:sw a5, 128(ra)<br>      |
|  18|[0x8001239c]<br>0x00000000|- rs1 : f14<br> - rs2 : f13<br> - rd : x14<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000344]:feq.h a4, fa4, fa3<br> [0x80000348]:csrrs tp, fcsr, zero<br> [0x8000034c]:sw a4, 136(ra)<br>      |
|  19|[0x800123a4]<br>0x00000000|- rs1 : f13<br> - rs2 : f14<br> - rd : x13<br> - fs1 == 0 and fe1 == 0x19 and fm1 == 0x216 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000364]:feq.h a3, fa3, fa4<br> [0x80000368]:csrrs tp, fcsr, zero<br> [0x8000036c]:sw a3, 144(ra)<br>      |
|  20|[0x800123ac]<br>0x00000000|- rs1 : f12<br> - rs2 : f11<br> - rd : x12<br> - fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x19 and fm2 == 0x216 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000384]:feq.h a2, fa2, fa1<br> [0x80000388]:csrrs tp, fcsr, zero<br> [0x8000038c]:sw a2, 152(ra)<br>      |
|  21|[0x800123b4]<br>0x00000000|- rs1 : f11<br> - rs2 : f12<br> - rd : x11<br> - fs1 == 0 and fe1 == 0x19 and fm1 == 0x216 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800003a4]:feq.h a1, fa1, fa2<br> [0x800003a8]:csrrs tp, fcsr, zero<br> [0x800003ac]:sw a1, 160(ra)<br>      |
|  22|[0x800123bc]<br>0x00000000|- rs1 : f10<br> - rs2 : f9<br> - rd : x10<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x19 and fm2 == 0x216 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                          |[0x800003c4]:feq.h a0, fa0, fs1<br> [0x800003c8]:csrrs tp, fcsr, zero<br> [0x800003cc]:sw a0, 168(ra)<br>      |
|  23|[0x800123c4]<br>0x00000000|- rs1 : f9<br> - rs2 : f10<br> - rd : x9<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                           |[0x800003e4]:feq.h s1, fs1, fa0<br> [0x800003e8]:csrrs tp, fcsr, zero<br> [0x800003ec]:sw s1, 176(ra)<br>      |
|  24|[0x800123cc]<br>0x00000000|- rs1 : f8<br> - rs2 : f7<br> - rd : x8<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x8000040c]:feq.h fp, fs0, ft7<br> [0x80000410]:csrrs a0, fcsr, zero<br> [0x80000414]:sw fp, 184(ra)<br>      |
|  25|[0x800123d4]<br>0x00000000|- rs1 : f7<br> - rs2 : f8<br> - rd : x7<br> - fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x8000042c]:feq.h t2, ft7, fs0<br> [0x80000430]:csrrs a0, fcsr, zero<br> [0x80000434]:sw t2, 192(ra)<br>      |
|  26|[0x800123dc]<br>0x00000000|- rs1 : f6<br> - rs2 : f5<br> - rd : x6<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x8000044c]:feq.h t1, ft6, ft5<br> [0x80000450]:csrrs a0, fcsr, zero<br> [0x80000454]:sw t1, 200(ra)<br>      |
|  27|[0x800123e4]<br>0x00000000|- rs1 : f5<br> - rs2 : f6<br> - rd : x5<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x80000474]:feq.h t0, ft5, ft6<br> [0x80000478]:csrrs a0, fcsr, zero<br> [0x8000047c]:sw t0, 0(t1)<br>        |
|  28|[0x800123ec]<br>0x00000000|- rs1 : f4<br> - rs2 : f3<br> - rd : x4<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x80000494]:feq.h tp, ft4, ft3<br> [0x80000498]:csrrs a0, fcsr, zero<br> [0x8000049c]:sw tp, 8(t1)<br>        |
|  29|[0x800123f4]<br>0x00000000|- rs1 : f3<br> - rs2 : f4<br> - rd : x3<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x800004b4]:feq.h gp, ft3, ft4<br> [0x800004b8]:csrrs a0, fcsr, zero<br> [0x800004bc]:sw gp, 16(t1)<br>       |
|  30|[0x800123fc]<br>0x00000000|- rs1 : f2<br> - rs2 : f1<br> - rd : x2<br> - fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x800004d4]:feq.h sp, ft2, ft1<br> [0x800004d8]:csrrs a0, fcsr, zero<br> [0x800004dc]:sw sp, 24(t1)<br>       |
|  31|[0x80012404]<br>0x00000000|- rs1 : f1<br> - rs2 : f2<br> - rd : x1<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x800004f4]:feq.h ra, ft1, ft2<br> [0x800004f8]:csrrs a0, fcsr, zero<br> [0x800004fc]:sw ra, 32(t1)<br>       |
|  32|[0x8001240c]<br>0x00000000|- rs1 : f0<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                         |[0x80000514]:feq.h t6, ft0, ft11<br> [0x80000518]:csrrs a0, fcsr, zero<br> [0x8000051c]:sw t6, 40(t1)<br>      |
|  33|[0x80012414]<br>0x00000000|- rs2 : f0<br> - fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                         |[0x80000534]:feq.h t6, ft11, ft0<br> [0x80000538]:csrrs a0, fcsr, zero<br> [0x8000053c]:sw t6, 48(t1)<br>      |
|  34|[0x8001241c]<br>0x00000000|- rd : x0<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                          |[0x80000554]:feq.h zero, ft11, ft10<br> [0x80000558]:csrrs a0, fcsr, zero<br> [0x8000055c]:sw zero, 56(t1)<br> |
|  35|[0x80012424]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000574]:feq.h t6, ft11, ft10<br> [0x80000578]:csrrs a0, fcsr, zero<br> [0x8000057c]:sw t6, 64(t1)<br>     |
|  36|[0x8001242c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000594]:feq.h t6, ft11, ft10<br> [0x80000598]:csrrs a0, fcsr, zero<br> [0x8000059c]:sw t6, 72(t1)<br>     |
|  37|[0x80012434]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800005b4]:feq.h t6, ft11, ft10<br> [0x800005b8]:csrrs a0, fcsr, zero<br> [0x800005bc]:sw t6, 80(t1)<br>     |
|  38|[0x8001243c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800005d4]:feq.h t6, ft11, ft10<br> [0x800005d8]:csrrs a0, fcsr, zero<br> [0x800005dc]:sw t6, 88(t1)<br>     |
|  39|[0x80012444]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800005f4]:feq.h t6, ft11, ft10<br> [0x800005f8]:csrrs a0, fcsr, zero<br> [0x800005fc]:sw t6, 96(t1)<br>     |
|  40|[0x8001244c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000614]:feq.h t6, ft11, ft10<br> [0x80000618]:csrrs a0, fcsr, zero<br> [0x8000061c]:sw t6, 104(t1)<br>    |
|  41|[0x80012454]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000634]:feq.h t6, ft11, ft10<br> [0x80000638]:csrrs a0, fcsr, zero<br> [0x8000063c]:sw t6, 112(t1)<br>    |
|  42|[0x8001245c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000654]:feq.h t6, ft11, ft10<br> [0x80000658]:csrrs a0, fcsr, zero<br> [0x8000065c]:sw t6, 120(t1)<br>    |
|  43|[0x80012464]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000674]:feq.h t6, ft11, ft10<br> [0x80000678]:csrrs a0, fcsr, zero<br> [0x8000067c]:sw t6, 128(t1)<br>    |
|  44|[0x8001246c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000694]:feq.h t6, ft11, ft10<br> [0x80000698]:csrrs a0, fcsr, zero<br> [0x8000069c]:sw t6, 136(t1)<br>    |
|  45|[0x80012474]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800006b4]:feq.h t6, ft11, ft10<br> [0x800006b8]:csrrs a0, fcsr, zero<br> [0x800006bc]:sw t6, 144(t1)<br>    |
|  46|[0x8001247c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800006d4]:feq.h t6, ft11, ft10<br> [0x800006d8]:csrrs a0, fcsr, zero<br> [0x800006dc]:sw t6, 152(t1)<br>    |
|  47|[0x80012484]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800006f4]:feq.h t6, ft11, ft10<br> [0x800006f8]:csrrs a0, fcsr, zero<br> [0x800006fc]:sw t6, 160(t1)<br>    |
|  48|[0x8001248c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000714]:feq.h t6, ft11, ft10<br> [0x80000718]:csrrs a0, fcsr, zero<br> [0x8000071c]:sw t6, 168(t1)<br>    |
|  49|[0x80012494]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000734]:feq.h t6, ft11, ft10<br> [0x80000738]:csrrs a0, fcsr, zero<br> [0x8000073c]:sw t6, 176(t1)<br>    |
|  50|[0x8001249c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x01a and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000754]:feq.h t6, ft11, ft10<br> [0x80000758]:csrrs a0, fcsr, zero<br> [0x8000075c]:sw t6, 184(t1)<br>    |
|  51|[0x800124a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x01a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000774]:feq.h t6, ft11, ft10<br> [0x80000778]:csrrs a0, fcsr, zero<br> [0x8000077c]:sw t6, 192(t1)<br>    |
|  52|[0x800124ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x01a and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000794]:feq.h t6, ft11, ft10<br> [0x80000798]:csrrs a0, fcsr, zero<br> [0x8000079c]:sw t6, 200(t1)<br>    |
|  53|[0x800124b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x01a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800007b4]:feq.h t6, ft11, ft10<br> [0x800007b8]:csrrs a0, fcsr, zero<br> [0x800007bc]:sw t6, 208(t1)<br>    |
|  54|[0x800124bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800007d4]:feq.h t6, ft11, ft10<br> [0x800007d8]:csrrs a0, fcsr, zero<br> [0x800007dc]:sw t6, 216(t1)<br>    |
|  55|[0x800124c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800007f4]:feq.h t6, ft11, ft10<br> [0x800007f8]:csrrs a0, fcsr, zero<br> [0x800007fc]:sw t6, 224(t1)<br>    |
|  56|[0x800124cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000814]:feq.h t6, ft11, ft10<br> [0x80000818]:csrrs a0, fcsr, zero<br> [0x8000081c]:sw t6, 232(t1)<br>    |
|  57|[0x800124d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000834]:feq.h t6, ft11, ft10<br> [0x80000838]:csrrs a0, fcsr, zero<br> [0x8000083c]:sw t6, 240(t1)<br>    |
|  58|[0x800124dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000854]:feq.h t6, ft11, ft10<br> [0x80000858]:csrrs a0, fcsr, zero<br> [0x8000085c]:sw t6, 248(t1)<br>    |
|  59|[0x800124e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000874]:feq.h t6, ft11, ft10<br> [0x80000878]:csrrs a0, fcsr, zero<br> [0x8000087c]:sw t6, 256(t1)<br>    |
|  60|[0x800124ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000894]:feq.h t6, ft11, ft10<br> [0x80000898]:csrrs a0, fcsr, zero<br> [0x8000089c]:sw t6, 264(t1)<br>    |
|  61|[0x800124f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800008b4]:feq.h t6, ft11, ft10<br> [0x800008b8]:csrrs a0, fcsr, zero<br> [0x800008bc]:sw t6, 272(t1)<br>    |
|  62|[0x800124fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800008d4]:feq.h t6, ft11, ft10<br> [0x800008d8]:csrrs a0, fcsr, zero<br> [0x800008dc]:sw t6, 280(t1)<br>    |
|  63|[0x80012504]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800008f4]:feq.h t6, ft11, ft10<br> [0x800008f8]:csrrs a0, fcsr, zero<br> [0x800008fc]:sw t6, 288(t1)<br>    |
|  64|[0x8001250c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x105 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000914]:feq.h t6, ft11, ft10<br> [0x80000918]:csrrs a0, fcsr, zero<br> [0x8000091c]:sw t6, 296(t1)<br>    |
|  65|[0x80012514]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x105 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000934]:feq.h t6, ft11, ft10<br> [0x80000938]:csrrs a0, fcsr, zero<br> [0x8000093c]:sw t6, 304(t1)<br>    |
|  66|[0x8001251c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000954]:feq.h t6, ft11, ft10<br> [0x80000958]:csrrs a0, fcsr, zero<br> [0x8000095c]:sw t6, 312(t1)<br>    |
|  67|[0x80012524]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x23c and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000974]:feq.h t6, ft11, ft10<br> [0x80000978]:csrrs a0, fcsr, zero<br> [0x8000097c]:sw t6, 320(t1)<br>    |
|  68|[0x8001252c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x23c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000994]:feq.h t6, ft11, ft10<br> [0x80000998]:csrrs a0, fcsr, zero<br> [0x8000099c]:sw t6, 328(t1)<br>    |
|  69|[0x80012534]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x0f and fm2 == 0x23c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800009b4]:feq.h t6, ft11, ft10<br> [0x800009b8]:csrrs a0, fcsr, zero<br> [0x800009bc]:sw t6, 336(t1)<br>    |
|  70|[0x8001253c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800009d4]:feq.h t6, ft11, ft10<br> [0x800009d8]:csrrs a0, fcsr, zero<br> [0x800009dc]:sw t6, 344(t1)<br>    |
|  71|[0x80012544]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800009f4]:feq.h t6, ft11, ft10<br> [0x800009f8]:csrrs a0, fcsr, zero<br> [0x800009fc]:sw t6, 352(t1)<br>    |
|  72|[0x8001254c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a14]:feq.h t6, ft11, ft10<br> [0x80000a18]:csrrs a0, fcsr, zero<br> [0x80000a1c]:sw t6, 360(t1)<br>    |
|  73|[0x80012554]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a34]:feq.h t6, ft11, ft10<br> [0x80000a38]:csrrs a0, fcsr, zero<br> [0x80000a3c]:sw t6, 368(t1)<br>    |
|  74|[0x8001255c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a54]:feq.h t6, ft11, ft10<br> [0x80000a58]:csrrs a0, fcsr, zero<br> [0x80000a5c]:sw t6, 376(t1)<br>    |
|  75|[0x80012564]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a74]:feq.h t6, ft11, ft10<br> [0x80000a78]:csrrs a0, fcsr, zero<br> [0x80000a7c]:sw t6, 384(t1)<br>    |
|  76|[0x8001256c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a94]:feq.h t6, ft11, ft10<br> [0x80000a98]:csrrs a0, fcsr, zero<br> [0x80000a9c]:sw t6, 392(t1)<br>    |
|  77|[0x80012574]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ab4]:feq.h t6, ft11, ft10<br> [0x80000ab8]:csrrs a0, fcsr, zero<br> [0x80000abc]:sw t6, 400(t1)<br>    |
|  78|[0x8001257c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ad4]:feq.h t6, ft11, ft10<br> [0x80000ad8]:csrrs a0, fcsr, zero<br> [0x80000adc]:sw t6, 408(t1)<br>    |
|  79|[0x80012584]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000af4]:feq.h t6, ft11, ft10<br> [0x80000af8]:csrrs a0, fcsr, zero<br> [0x80000afc]:sw t6, 416(t1)<br>    |
|  80|[0x8001258c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b14]:feq.h t6, ft11, ft10<br> [0x80000b18]:csrrs a0, fcsr, zero<br> [0x80000b1c]:sw t6, 424(t1)<br>    |
|  81|[0x80012594]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b34]:feq.h t6, ft11, ft10<br> [0x80000b38]:csrrs a0, fcsr, zero<br> [0x80000b3c]:sw t6, 432(t1)<br>    |
|  82|[0x8001259c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b54]:feq.h t6, ft11, ft10<br> [0x80000b58]:csrrs a0, fcsr, zero<br> [0x80000b5c]:sw t6, 440(t1)<br>    |
|  83|[0x800125a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b74]:feq.h t6, ft11, ft10<br> [0x80000b78]:csrrs a0, fcsr, zero<br> [0x80000b7c]:sw t6, 448(t1)<br>    |
|  84|[0x800125ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b94]:feq.h t6, ft11, ft10<br> [0x80000b98]:csrrs a0, fcsr, zero<br> [0x80000b9c]:sw t6, 456(t1)<br>    |
|  85|[0x800125b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000bb4]:feq.h t6, ft11, ft10<br> [0x80000bb8]:csrrs a0, fcsr, zero<br> [0x80000bbc]:sw t6, 464(t1)<br>    |
|  86|[0x800125bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1b and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000bd4]:feq.h t6, ft11, ft10<br> [0x80000bd8]:csrrs a0, fcsr, zero<br> [0x80000bdc]:sw t6, 472(t1)<br>    |
|  87|[0x800125c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1b and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000bf4]:feq.h t6, ft11, ft10<br> [0x80000bf8]:csrrs a0, fcsr, zero<br> [0x80000bfc]:sw t6, 480(t1)<br>    |
|  88|[0x800125cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1b and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c14]:feq.h t6, ft11, ft10<br> [0x80000c18]:csrrs a0, fcsr, zero<br> [0x80000c1c]:sw t6, 488(t1)<br>    |
|  89|[0x800125d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x1b and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c34]:feq.h t6, ft11, ft10<br> [0x80000c38]:csrrs a0, fcsr, zero<br> [0x80000c3c]:sw t6, 496(t1)<br>    |
|  90|[0x800125dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c54]:feq.h t6, ft11, ft10<br> [0x80000c58]:csrrs a0, fcsr, zero<br> [0x80000c5c]:sw t6, 504(t1)<br>    |
|  91|[0x800125e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c74]:feq.h t6, ft11, ft10<br> [0x80000c78]:csrrs a0, fcsr, zero<br> [0x80000c7c]:sw t6, 512(t1)<br>    |
|  92|[0x800125ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c94]:feq.h t6, ft11, ft10<br> [0x80000c98]:csrrs a0, fcsr, zero<br> [0x80000c9c]:sw t6, 520(t1)<br>    |
|  93|[0x800125f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000cb4]:feq.h t6, ft11, ft10<br> [0x80000cb8]:csrrs a0, fcsr, zero<br> [0x80000cbc]:sw t6, 528(t1)<br>    |
|  94|[0x800125fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000cd4]:feq.h t6, ft11, ft10<br> [0x80000cd8]:csrrs a0, fcsr, zero<br> [0x80000cdc]:sw t6, 536(t1)<br>    |
|  95|[0x80012604]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000cf4]:feq.h t6, ft11, ft10<br> [0x80000cf8]:csrrs a0, fcsr, zero<br> [0x80000cfc]:sw t6, 544(t1)<br>    |
|  96|[0x8001260c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x006 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d14]:feq.h t6, ft11, ft10<br> [0x80000d18]:csrrs a0, fcsr, zero<br> [0x80000d1c]:sw t6, 552(t1)<br>    |
|  97|[0x80012614]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d34]:feq.h t6, ft11, ft10<br> [0x80000d38]:csrrs a0, fcsr, zero<br> [0x80000d3c]:sw t6, 560(t1)<br>    |
|  98|[0x8001261c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x006 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d54]:feq.h t6, ft11, ft10<br> [0x80000d58]:csrrs a0, fcsr, zero<br> [0x80000d5c]:sw t6, 568(t1)<br>    |
|  99|[0x80012624]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d74]:feq.h t6, ft11, ft10<br> [0x80000d78]:csrrs a0, fcsr, zero<br> [0x80000d7c]:sw t6, 576(t1)<br>    |
| 100|[0x8001262c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d94]:feq.h t6, ft11, ft10<br> [0x80000d98]:csrrs a0, fcsr, zero<br> [0x80000d9c]:sw t6, 584(t1)<br>    |
| 101|[0x80012634]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000db4]:feq.h t6, ft11, ft10<br> [0x80000db8]:csrrs a0, fcsr, zero<br> [0x80000dbc]:sw t6, 592(t1)<br>    |
| 102|[0x8001263c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000dd4]:feq.h t6, ft11, ft10<br> [0x80000dd8]:csrrs a0, fcsr, zero<br> [0x80000ddc]:sw t6, 600(t1)<br>    |
| 103|[0x80012644]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000df4]:feq.h t6, ft11, ft10<br> [0x80000df8]:csrrs a0, fcsr, zero<br> [0x80000dfc]:sw t6, 608(t1)<br>    |
| 104|[0x8001264c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e14]:feq.h t6, ft11, ft10<br> [0x80000e18]:csrrs a0, fcsr, zero<br> [0x80000e1c]:sw t6, 616(t1)<br>    |
| 105|[0x80012654]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e34]:feq.h t6, ft11, ft10<br> [0x80000e38]:csrrs a0, fcsr, zero<br> [0x80000e3c]:sw t6, 624(t1)<br>    |
| 106|[0x8001265c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e54]:feq.h t6, ft11, ft10<br> [0x80000e58]:csrrs a0, fcsr, zero<br> [0x80000e5c]:sw t6, 632(t1)<br>    |
| 107|[0x80012664]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e74]:feq.h t6, ft11, ft10<br> [0x80000e78]:csrrs a0, fcsr, zero<br> [0x80000e7c]:sw t6, 640(t1)<br>    |
| 108|[0x8001266c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e94]:feq.h t6, ft11, ft10<br> [0x80000e98]:csrrs a0, fcsr, zero<br> [0x80000e9c]:sw t6, 648(t1)<br>    |
| 109|[0x80012674]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000eb4]:feq.h t6, ft11, ft10<br> [0x80000eb8]:csrrs a0, fcsr, zero<br> [0x80000ebc]:sw t6, 656(t1)<br>    |
| 110|[0x8001267c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ed4]:feq.h t6, ft11, ft10<br> [0x80000ed8]:csrrs a0, fcsr, zero<br> [0x80000edc]:sw t6, 664(t1)<br>    |
| 111|[0x80012684]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ef4]:feq.h t6, ft11, ft10<br> [0x80000ef8]:csrrs a0, fcsr, zero<br> [0x80000efc]:sw t6, 672(t1)<br>    |
| 112|[0x8001268c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f14]:feq.h t6, ft11, ft10<br> [0x80000f18]:csrrs a0, fcsr, zero<br> [0x80000f1c]:sw t6, 680(t1)<br>    |
| 113|[0x80012694]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f34]:feq.h t6, ft11, ft10<br> [0x80000f38]:csrrs a0, fcsr, zero<br> [0x80000f3c]:sw t6, 688(t1)<br>    |
| 114|[0x8001269c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f54]:feq.h t6, ft11, ft10<br> [0x80000f58]:csrrs a0, fcsr, zero<br> [0x80000f5c]:sw t6, 696(t1)<br>    |
| 115|[0x800126a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f74]:feq.h t6, ft11, ft10<br> [0x80000f78]:csrrs a0, fcsr, zero<br> [0x80000f7c]:sw t6, 704(t1)<br>    |
| 116|[0x800126ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f94]:feq.h t6, ft11, ft10<br> [0x80000f98]:csrrs a0, fcsr, zero<br> [0x80000f9c]:sw t6, 712(t1)<br>    |
| 117|[0x800126b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x044 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000fb4]:feq.h t6, ft11, ft10<br> [0x80000fb8]:csrrs a0, fcsr, zero<br> [0x80000fbc]:sw t6, 720(t1)<br>    |
| 118|[0x800126bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x044 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000fd4]:feq.h t6, ft11, ft10<br> [0x80000fd8]:csrrs a0, fcsr, zero<br> [0x80000fdc]:sw t6, 728(t1)<br>    |
| 119|[0x800126c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x044 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ff4]:feq.h t6, ft11, ft10<br> [0x80000ff8]:csrrs a0, fcsr, zero<br> [0x80000ffc]:sw t6, 736(t1)<br>    |
| 120|[0x800126cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x044 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001014]:feq.h t6, ft11, ft10<br> [0x80001018]:csrrs a0, fcsr, zero<br> [0x8000101c]:sw t6, 744(t1)<br>    |
| 121|[0x800126d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001034]:feq.h t6, ft11, ft10<br> [0x80001038]:csrrs a0, fcsr, zero<br> [0x8000103c]:sw t6, 752(t1)<br>    |
| 122|[0x800126dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001054]:feq.h t6, ft11, ft10<br> [0x80001058]:csrrs a0, fcsr, zero<br> [0x8000105c]:sw t6, 760(t1)<br>    |
| 123|[0x800126e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001074]:feq.h t6, ft11, ft10<br> [0x80001078]:csrrs a0, fcsr, zero<br> [0x8000107c]:sw t6, 768(t1)<br>    |
| 124|[0x800126ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001094]:feq.h t6, ft11, ft10<br> [0x80001098]:csrrs a0, fcsr, zero<br> [0x8000109c]:sw t6, 776(t1)<br>    |
| 125|[0x800126f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800010b4]:feq.h t6, ft11, ft10<br> [0x800010b8]:csrrs a0, fcsr, zero<br> [0x800010bc]:sw t6, 784(t1)<br>    |
| 126|[0x800126fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800010d4]:feq.h t6, ft11, ft10<br> [0x800010d8]:csrrs a0, fcsr, zero<br> [0x800010dc]:sw t6, 792(t1)<br>    |
| 127|[0x80012704]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800010f4]:feq.h t6, ft11, ft10<br> [0x800010f8]:csrrs a0, fcsr, zero<br> [0x800010fc]:sw t6, 800(t1)<br>    |
| 128|[0x8001270c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001114]:feq.h t6, ft11, ft10<br> [0x80001118]:csrrs a0, fcsr, zero<br> [0x8000111c]:sw t6, 808(t1)<br>    |
| 129|[0x80012714]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001134]:feq.h t6, ft11, ft10<br> [0x80001138]:csrrs a0, fcsr, zero<br> [0x8000113c]:sw t6, 816(t1)<br>    |
| 130|[0x8001271c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001154]:feq.h t6, ft11, ft10<br> [0x80001158]:csrrs a0, fcsr, zero<br> [0x8000115c]:sw t6, 824(t1)<br>    |
| 131|[0x80012724]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2af and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001174]:feq.h t6, ft11, ft10<br> [0x80001178]:csrrs a0, fcsr, zero<br> [0x8000117c]:sw t6, 832(t1)<br>    |
| 132|[0x8001272c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2af and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001194]:feq.h t6, ft11, ft10<br> [0x80001198]:csrrs a0, fcsr, zero<br> [0x8000119c]:sw t6, 840(t1)<br>    |
| 133|[0x80012734]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800011b4]:feq.h t6, ft11, ft10<br> [0x800011b8]:csrrs a0, fcsr, zero<br> [0x800011bc]:sw t6, 848(t1)<br>    |
| 134|[0x8001273c]<br>0x00000000|- fs1 == 0 and fe1 == 0x11 and fm1 == 0x019 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800011d4]:feq.h t6, ft11, ft10<br> [0x800011d8]:csrrs a0, fcsr, zero<br> [0x800011dc]:sw t6, 856(t1)<br>    |
| 135|[0x80012744]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x019 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800011f4]:feq.h t6, ft11, ft10<br> [0x800011f8]:csrrs a0, fcsr, zero<br> [0x800011fc]:sw t6, 864(t1)<br>    |
| 136|[0x8001274c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x100 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x019 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001214]:feq.h t6, ft11, ft10<br> [0x80001218]:csrrs a0, fcsr, zero<br> [0x8000121c]:sw t6, 872(t1)<br>    |
| 137|[0x80012754]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001234]:feq.h t6, ft11, ft10<br> [0x80001238]:csrrs a0, fcsr, zero<br> [0x8000123c]:sw t6, 880(t1)<br>    |
| 138|[0x8001275c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001254]:feq.h t6, ft11, ft10<br> [0x80001258]:csrrs a0, fcsr, zero<br> [0x8000125c]:sw t6, 888(t1)<br>    |
| 139|[0x80012764]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001274]:feq.h t6, ft11, ft10<br> [0x80001278]:csrrs a0, fcsr, zero<br> [0x8000127c]:sw t6, 896(t1)<br>    |
| 140|[0x8001276c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001294]:feq.h t6, ft11, ft10<br> [0x80001298]:csrrs a0, fcsr, zero<br> [0x8000129c]:sw t6, 904(t1)<br>    |
| 141|[0x80012774]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800012b4]:feq.h t6, ft11, ft10<br> [0x800012b8]:csrrs a0, fcsr, zero<br> [0x800012bc]:sw t6, 912(t1)<br>    |
| 142|[0x8001277c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800012d4]:feq.h t6, ft11, ft10<br> [0x800012d8]:csrrs a0, fcsr, zero<br> [0x800012dc]:sw t6, 920(t1)<br>    |
| 143|[0x80012784]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800012f4]:feq.h t6, ft11, ft10<br> [0x800012f8]:csrrs a0, fcsr, zero<br> [0x800012fc]:sw t6, 928(t1)<br>    |
| 144|[0x8001278c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001314]:feq.h t6, ft11, ft10<br> [0x80001318]:csrrs a0, fcsr, zero<br> [0x8000131c]:sw t6, 936(t1)<br>    |
| 145|[0x80012794]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001334]:feq.h t6, ft11, ft10<br> [0x80001338]:csrrs a0, fcsr, zero<br> [0x8000133c]:sw t6, 944(t1)<br>    |
| 146|[0x8001279c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001354]:feq.h t6, ft11, ft10<br> [0x80001358]:csrrs a0, fcsr, zero<br> [0x8000135c]:sw t6, 952(t1)<br>    |
| 147|[0x800127a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001374]:feq.h t6, ft11, ft10<br> [0x80001378]:csrrs a0, fcsr, zero<br> [0x8000137c]:sw t6, 960(t1)<br>    |
| 148|[0x800127ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001394]:feq.h t6, ft11, ft10<br> [0x80001398]:csrrs a0, fcsr, zero<br> [0x8000139c]:sw t6, 968(t1)<br>    |
| 149|[0x800127b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800013b4]:feq.h t6, ft11, ft10<br> [0x800013b8]:csrrs a0, fcsr, zero<br> [0x800013bc]:sw t6, 976(t1)<br>    |
| 150|[0x800127bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800013d4]:feq.h t6, ft11, ft10<br> [0x800013d8]:csrrs a0, fcsr, zero<br> [0x800013dc]:sw t6, 984(t1)<br>    |
| 151|[0x800127c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x19 and fm1 == 0x2a2 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800013f4]:feq.h t6, ft11, ft10<br> [0x800013f8]:csrrs a0, fcsr, zero<br> [0x800013fc]:sw t6, 992(t1)<br>    |
| 152|[0x800127cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x19 and fm2 == 0x2a2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001414]:feq.h t6, ft11, ft10<br> [0x80001418]:csrrs a0, fcsr, zero<br> [0x8000141c]:sw t6, 1000(t1)<br>   |
| 153|[0x800127d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x19 and fm1 == 0x2a2 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001434]:feq.h t6, ft11, ft10<br> [0x80001438]:csrrs a0, fcsr, zero<br> [0x8000143c]:sw t6, 1008(t1)<br>   |
| 154|[0x800127dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x19 and fm2 == 0x2a2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001454]:feq.h t6, ft11, ft10<br> [0x80001458]:csrrs a0, fcsr, zero<br> [0x8000145c]:sw t6, 1016(t1)<br>   |
| 155|[0x800127e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000147c]:feq.h t6, ft11, ft10<br> [0x80001480]:csrrs a0, fcsr, zero<br> [0x80001484]:sw t6, 0(t1)<br>      |
| 156|[0x800127ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000149c]:feq.h t6, ft11, ft10<br> [0x800014a0]:csrrs a0, fcsr, zero<br> [0x800014a4]:sw t6, 8(t1)<br>      |
| 157|[0x800127f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800014bc]:feq.h t6, ft11, ft10<br> [0x800014c0]:csrrs a0, fcsr, zero<br> [0x800014c4]:sw t6, 16(t1)<br>     |
| 158|[0x800127fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800014dc]:feq.h t6, ft11, ft10<br> [0x800014e0]:csrrs a0, fcsr, zero<br> [0x800014e4]:sw t6, 24(t1)<br>     |
| 159|[0x80012804]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800014fc]:feq.h t6, ft11, ft10<br> [0x80001500]:csrrs a0, fcsr, zero<br> [0x80001504]:sw t6, 32(t1)<br>     |
| 160|[0x8001280c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000151c]:feq.h t6, ft11, ft10<br> [0x80001520]:csrrs a0, fcsr, zero<br> [0x80001524]:sw t6, 40(t1)<br>     |
| 161|[0x80012814]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000153c]:feq.h t6, ft11, ft10<br> [0x80001540]:csrrs a0, fcsr, zero<br> [0x80001544]:sw t6, 48(t1)<br>     |
| 162|[0x8001281c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000155c]:feq.h t6, ft11, ft10<br> [0x80001560]:csrrs a0, fcsr, zero<br> [0x80001564]:sw t6, 56(t1)<br>     |
| 163|[0x80012824]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000157c]:feq.h t6, ft11, ft10<br> [0x80001580]:csrrs a0, fcsr, zero<br> [0x80001584]:sw t6, 64(t1)<br>     |
| 164|[0x8001282c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000159c]:feq.h t6, ft11, ft10<br> [0x800015a0]:csrrs a0, fcsr, zero<br> [0x800015a4]:sw t6, 72(t1)<br>     |
| 165|[0x80012834]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800015bc]:feq.h t6, ft11, ft10<br> [0x800015c0]:csrrs a0, fcsr, zero<br> [0x800015c4]:sw t6, 80(t1)<br>     |
| 166|[0x8001283c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800015dc]:feq.h t6, ft11, ft10<br> [0x800015e0]:csrrs a0, fcsr, zero<br> [0x800015e4]:sw t6, 88(t1)<br>     |
| 167|[0x80012844]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800015fc]:feq.h t6, ft11, ft10<br> [0x80001600]:csrrs a0, fcsr, zero<br> [0x80001604]:sw t6, 96(t1)<br>     |
| 168|[0x8001284c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000161c]:feq.h t6, ft11, ft10<br> [0x80001620]:csrrs a0, fcsr, zero<br> [0x80001624]:sw t6, 104(t1)<br>    |
| 169|[0x80012854]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000163c]:feq.h t6, ft11, ft10<br> [0x80001640]:csrrs a0, fcsr, zero<br> [0x80001644]:sw t6, 112(t1)<br>    |
| 170|[0x8001285c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000165c]:feq.h t6, ft11, ft10<br> [0x80001660]:csrrs a0, fcsr, zero<br> [0x80001664]:sw t6, 120(t1)<br>    |
| 171|[0x80012864]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000167c]:feq.h t6, ft11, ft10<br> [0x80001680]:csrrs a0, fcsr, zero<br> [0x80001684]:sw t6, 128(t1)<br>    |
| 172|[0x8001286c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000169c]:feq.h t6, ft11, ft10<br> [0x800016a0]:csrrs a0, fcsr, zero<br> [0x800016a4]:sw t6, 136(t1)<br>    |
| 173|[0x80012874]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800016bc]:feq.h t6, ft11, ft10<br> [0x800016c0]:csrrs a0, fcsr, zero<br> [0x800016c4]:sw t6, 144(t1)<br>    |
| 174|[0x8001287c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800016dc]:feq.h t6, ft11, ft10<br> [0x800016e0]:csrrs a0, fcsr, zero<br> [0x800016e4]:sw t6, 152(t1)<br>    |
| 175|[0x80012884]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800016fc]:feq.h t6, ft11, ft10<br> [0x80001700]:csrrs a0, fcsr, zero<br> [0x80001704]:sw t6, 160(t1)<br>    |
| 176|[0x8001288c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000171c]:feq.h t6, ft11, ft10<br> [0x80001720]:csrrs a0, fcsr, zero<br> [0x80001724]:sw t6, 168(t1)<br>    |
| 177|[0x80012894]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000173c]:feq.h t6, ft11, ft10<br> [0x80001740]:csrrs a0, fcsr, zero<br> [0x80001744]:sw t6, 176(t1)<br>    |
| 178|[0x8001289c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000175c]:feq.h t6, ft11, ft10<br> [0x80001760]:csrrs a0, fcsr, zero<br> [0x80001764]:sw t6, 184(t1)<br>    |
| 179|[0x800128a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x01c and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000177c]:feq.h t6, ft11, ft10<br> [0x80001780]:csrrs a0, fcsr, zero<br> [0x80001784]:sw t6, 192(t1)<br>    |
| 180|[0x800128ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x01c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000179c]:feq.h t6, ft11, ft10<br> [0x800017a0]:csrrs a0, fcsr, zero<br> [0x800017a4]:sw t6, 200(t1)<br>    |
| 181|[0x800128b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x01c and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800017bc]:feq.h t6, ft11, ft10<br> [0x800017c0]:csrrs a0, fcsr, zero<br> [0x800017c4]:sw t6, 208(t1)<br>    |
| 182|[0x800128bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x01c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800017dc]:feq.h t6, ft11, ft10<br> [0x800017e0]:csrrs a0, fcsr, zero<br> [0x800017e4]:sw t6, 216(t1)<br>    |
| 183|[0x800128c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800017fc]:feq.h t6, ft11, ft10<br> [0x80001800]:csrrs a0, fcsr, zero<br> [0x80001804]:sw t6, 224(t1)<br>    |
| 184|[0x800128cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000181c]:feq.h t6, ft11, ft10<br> [0x80001820]:csrrs a0, fcsr, zero<br> [0x80001824]:sw t6, 232(t1)<br>    |
| 185|[0x800128d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000183c]:feq.h t6, ft11, ft10<br> [0x80001840]:csrrs a0, fcsr, zero<br> [0x80001844]:sw t6, 240(t1)<br>    |
| 186|[0x800128dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000185c]:feq.h t6, ft11, ft10<br> [0x80001860]:csrrs a0, fcsr, zero<br> [0x80001864]:sw t6, 248(t1)<br>    |
| 187|[0x800128e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000187c]:feq.h t6, ft11, ft10<br> [0x80001880]:csrrs a0, fcsr, zero<br> [0x80001884]:sw t6, 256(t1)<br>    |
| 188|[0x800128ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000189c]:feq.h t6, ft11, ft10<br> [0x800018a0]:csrrs a0, fcsr, zero<br> [0x800018a4]:sw t6, 264(t1)<br>    |
| 189|[0x800128f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800018bc]:feq.h t6, ft11, ft10<br> [0x800018c0]:csrrs a0, fcsr, zero<br> [0x800018c4]:sw t6, 272(t1)<br>    |
| 190|[0x800128fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800018dc]:feq.h t6, ft11, ft10<br> [0x800018e0]:csrrs a0, fcsr, zero<br> [0x800018e4]:sw t6, 280(t1)<br>    |
| 191|[0x80012904]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800018fc]:feq.h t6, ft11, ft10<br> [0x80001900]:csrrs a0, fcsr, zero<br> [0x80001904]:sw t6, 288(t1)<br>    |
| 192|[0x8001290c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000191c]:feq.h t6, ft11, ft10<br> [0x80001920]:csrrs a0, fcsr, zero<br> [0x80001924]:sw t6, 296(t1)<br>    |
| 193|[0x80012914]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x11d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000193c]:feq.h t6, ft11, ft10<br> [0x80001940]:csrrs a0, fcsr, zero<br> [0x80001944]:sw t6, 304(t1)<br>    |
| 194|[0x8001291c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x11d and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000195c]:feq.h t6, ft11, ft10<br> [0x80001960]:csrrs a0, fcsr, zero<br> [0x80001964]:sw t6, 312(t1)<br>    |
| 195|[0x80012924]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000197c]:feq.h t6, ft11, ft10<br> [0x80001980]:csrrs a0, fcsr, zero<br> [0x80001984]:sw t6, 320(t1)<br>    |
| 196|[0x8001292c]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x2cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000199c]:feq.h t6, ft11, ft10<br> [0x800019a0]:csrrs a0, fcsr, zero<br> [0x800019a4]:sw t6, 328(t1)<br>    |
| 197|[0x80012934]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x2cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800019bc]:feq.h t6, ft11, ft10<br> [0x800019c0]:csrrs a0, fcsr, zero<br> [0x800019c4]:sw t6, 336(t1)<br>    |
| 198|[0x8001293c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x025 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x2cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800019dc]:feq.h t6, ft11, ft10<br> [0x800019e0]:csrrs a0, fcsr, zero<br> [0x800019e4]:sw t6, 344(t1)<br>    |
| 199|[0x80012944]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800019fc]:feq.h t6, ft11, ft10<br> [0x80001a00]:csrrs a0, fcsr, zero<br> [0x80001a04]:sw t6, 352(t1)<br>    |
| 200|[0x8001294c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a1c]:feq.h t6, ft11, ft10<br> [0x80001a20]:csrrs a0, fcsr, zero<br> [0x80001a24]:sw t6, 360(t1)<br>    |
| 201|[0x80012954]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a3c]:feq.h t6, ft11, ft10<br> [0x80001a40]:csrrs a0, fcsr, zero<br> [0x80001a44]:sw t6, 368(t1)<br>    |
| 202|[0x8001295c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a5c]:feq.h t6, ft11, ft10<br> [0x80001a60]:csrrs a0, fcsr, zero<br> [0x80001a64]:sw t6, 376(t1)<br>    |
| 203|[0x80012964]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a7c]:feq.h t6, ft11, ft10<br> [0x80001a80]:csrrs a0, fcsr, zero<br> [0x80001a84]:sw t6, 384(t1)<br>    |
| 204|[0x8001296c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a9c]:feq.h t6, ft11, ft10<br> [0x80001aa0]:csrrs a0, fcsr, zero<br> [0x80001aa4]:sw t6, 392(t1)<br>    |
| 205|[0x80012974]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001abc]:feq.h t6, ft11, ft10<br> [0x80001ac0]:csrrs a0, fcsr, zero<br> [0x80001ac4]:sw t6, 400(t1)<br>    |
| 206|[0x8001297c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001adc]:feq.h t6, ft11, ft10<br> [0x80001ae0]:csrrs a0, fcsr, zero<br> [0x80001ae4]:sw t6, 408(t1)<br>    |
| 207|[0x80012984]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001afc]:feq.h t6, ft11, ft10<br> [0x80001b00]:csrrs a0, fcsr, zero<br> [0x80001b04]:sw t6, 416(t1)<br>    |
| 208|[0x8001298c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b1c]:feq.h t6, ft11, ft10<br> [0x80001b20]:csrrs a0, fcsr, zero<br> [0x80001b24]:sw t6, 424(t1)<br>    |
| 209|[0x80012994]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b3c]:feq.h t6, ft11, ft10<br> [0x80001b40]:csrrs a0, fcsr, zero<br> [0x80001b44]:sw t6, 432(t1)<br>    |
| 210|[0x8001299c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b5c]:feq.h t6, ft11, ft10<br> [0x80001b60]:csrrs a0, fcsr, zero<br> [0x80001b64]:sw t6, 440(t1)<br>    |
| 211|[0x800129a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1b and fm1 == 0x159 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b7c]:feq.h t6, ft11, ft10<br> [0x80001b80]:csrrs a0, fcsr, zero<br> [0x80001b84]:sw t6, 448(t1)<br>    |
| 212|[0x800129ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1b and fm2 == 0x159 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b9c]:feq.h t6, ft11, ft10<br> [0x80001ba0]:csrrs a0, fcsr, zero<br> [0x80001ba4]:sw t6, 456(t1)<br>    |
| 213|[0x800129b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1b and fm1 == 0x159 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001bbc]:feq.h t6, ft11, ft10<br> [0x80001bc0]:csrrs a0, fcsr, zero<br> [0x80001bc4]:sw t6, 464(t1)<br>    |
| 214|[0x800129bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x1b and fm2 == 0x159 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001bdc]:feq.h t6, ft11, ft10<br> [0x80001be0]:csrrs a0, fcsr, zero<br> [0x80001be4]:sw t6, 472(t1)<br>    |
| 215|[0x800129c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001bfc]:feq.h t6, ft11, ft10<br> [0x80001c00]:csrrs a0, fcsr, zero<br> [0x80001c04]:sw t6, 480(t1)<br>    |
| 216|[0x800129cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c1c]:feq.h t6, ft11, ft10<br> [0x80001c20]:csrrs a0, fcsr, zero<br> [0x80001c24]:sw t6, 488(t1)<br>    |
| 217|[0x800129d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c3c]:feq.h t6, ft11, ft10<br> [0x80001c40]:csrrs a0, fcsr, zero<br> [0x80001c44]:sw t6, 496(t1)<br>    |
| 218|[0x800129dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c5c]:feq.h t6, ft11, ft10<br> [0x80001c60]:csrrs a0, fcsr, zero<br> [0x80001c64]:sw t6, 504(t1)<br>    |
| 219|[0x800129e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c7c]:feq.h t6, ft11, ft10<br> [0x80001c80]:csrrs a0, fcsr, zero<br> [0x80001c84]:sw t6, 512(t1)<br>    |
| 220|[0x800129ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c9c]:feq.h t6, ft11, ft10<br> [0x80001ca0]:csrrs a0, fcsr, zero<br> [0x80001ca4]:sw t6, 520(t1)<br>    |
| 221|[0x800129f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x009 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001cbc]:feq.h t6, ft11, ft10<br> [0x80001cc0]:csrrs a0, fcsr, zero<br> [0x80001cc4]:sw t6, 528(t1)<br>    |
| 222|[0x800129fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x009 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001cdc]:feq.h t6, ft11, ft10<br> [0x80001ce0]:csrrs a0, fcsr, zero<br> [0x80001ce4]:sw t6, 536(t1)<br>    |
| 223|[0x80012a04]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x009 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001cfc]:feq.h t6, ft11, ft10<br> [0x80001d00]:csrrs a0, fcsr, zero<br> [0x80001d04]:sw t6, 544(t1)<br>    |
| 224|[0x80012a0c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x009 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d1c]:feq.h t6, ft11, ft10<br> [0x80001d20]:csrrs a0, fcsr, zero<br> [0x80001d24]:sw t6, 552(t1)<br>    |
| 225|[0x80012a14]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d3c]:feq.h t6, ft11, ft10<br> [0x80001d40]:csrrs a0, fcsr, zero<br> [0x80001d44]:sw t6, 560(t1)<br>    |
| 226|[0x80012a1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d5c]:feq.h t6, ft11, ft10<br> [0x80001d60]:csrrs a0, fcsr, zero<br> [0x80001d64]:sw t6, 568(t1)<br>    |
| 227|[0x80012a24]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d7c]:feq.h t6, ft11, ft10<br> [0x80001d80]:csrrs a0, fcsr, zero<br> [0x80001d84]:sw t6, 576(t1)<br>    |
| 228|[0x80012a2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d9c]:feq.h t6, ft11, ft10<br> [0x80001da0]:csrrs a0, fcsr, zero<br> [0x80001da4]:sw t6, 584(t1)<br>    |
| 229|[0x80012a34]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001dbc]:feq.h t6, ft11, ft10<br> [0x80001dc0]:csrrs a0, fcsr, zero<br> [0x80001dc4]:sw t6, 592(t1)<br>    |
| 230|[0x80012a3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001ddc]:feq.h t6, ft11, ft10<br> [0x80001de0]:csrrs a0, fcsr, zero<br> [0x80001de4]:sw t6, 600(t1)<br>    |
| 231|[0x80012a44]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001dfc]:feq.h t6, ft11, ft10<br> [0x80001e00]:csrrs a0, fcsr, zero<br> [0x80001e04]:sw t6, 608(t1)<br>    |
| 232|[0x80012a4c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e1c]:feq.h t6, ft11, ft10<br> [0x80001e20]:csrrs a0, fcsr, zero<br> [0x80001e24]:sw t6, 616(t1)<br>    |
| 233|[0x80012a54]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e3c]:feq.h t6, ft11, ft10<br> [0x80001e40]:csrrs a0, fcsr, zero<br> [0x80001e44]:sw t6, 624(t1)<br>    |
| 234|[0x80012a5c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e5c]:feq.h t6, ft11, ft10<br> [0x80001e60]:csrrs a0, fcsr, zero<br> [0x80001e64]:sw t6, 632(t1)<br>    |
| 235|[0x80012a64]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e7c]:feq.h t6, ft11, ft10<br> [0x80001e80]:csrrs a0, fcsr, zero<br> [0x80001e84]:sw t6, 640(t1)<br>    |
| 236|[0x80012a6c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e9c]:feq.h t6, ft11, ft10<br> [0x80001ea0]:csrrs a0, fcsr, zero<br> [0x80001ea4]:sw t6, 648(t1)<br>    |
| 237|[0x80012a74]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001ebc]:feq.h t6, ft11, ft10<br> [0x80001ec0]:csrrs a0, fcsr, zero<br> [0x80001ec4]:sw t6, 656(t1)<br>    |
| 238|[0x80012a7c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001edc]:feq.h t6, ft11, ft10<br> [0x80001ee0]:csrrs a0, fcsr, zero<br> [0x80001ee4]:sw t6, 664(t1)<br>    |
| 239|[0x80012a84]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001efc]:feq.h t6, ft11, ft10<br> [0x80001f00]:csrrs a0, fcsr, zero<br> [0x80001f04]:sw t6, 672(t1)<br>    |
| 240|[0x80012a8c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f1c]:feq.h t6, ft11, ft10<br> [0x80001f20]:csrrs a0, fcsr, zero<br> [0x80001f24]:sw t6, 680(t1)<br>    |
| 241|[0x80012a94]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f3c]:feq.h t6, ft11, ft10<br> [0x80001f40]:csrrs a0, fcsr, zero<br> [0x80001f44]:sw t6, 688(t1)<br>    |
| 242|[0x80012a9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x05b and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f5c]:feq.h t6, ft11, ft10<br> [0x80001f60]:csrrs a0, fcsr, zero<br> [0x80001f64]:sw t6, 696(t1)<br>    |
| 243|[0x80012aa4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x05b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f7c]:feq.h t6, ft11, ft10<br> [0x80001f80]:csrrs a0, fcsr, zero<br> [0x80001f84]:sw t6, 704(t1)<br>    |
| 244|[0x80012aac]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x05b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f9c]:feq.h t6, ft11, ft10<br> [0x80001fa0]:csrrs a0, fcsr, zero<br> [0x80001fa4]:sw t6, 712(t1)<br>    |
| 245|[0x80012ab4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x05b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001fbc]:feq.h t6, ft11, ft10<br> [0x80001fc0]:csrrs a0, fcsr, zero<br> [0x80001fc4]:sw t6, 720(t1)<br>    |
| 246|[0x80012abc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001fdc]:feq.h t6, ft11, ft10<br> [0x80001fe0]:csrrs a0, fcsr, zero<br> [0x80001fe4]:sw t6, 728(t1)<br>    |
| 247|[0x80012ac4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001ffc]:feq.h t6, ft11, ft10<br> [0x80002000]:csrrs a0, fcsr, zero<br> [0x80002004]:sw t6, 736(t1)<br>    |
| 248|[0x80012acc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000201c]:feq.h t6, ft11, ft10<br> [0x80002020]:csrrs a0, fcsr, zero<br> [0x80002024]:sw t6, 744(t1)<br>    |
| 249|[0x80012ad4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000203c]:feq.h t6, ft11, ft10<br> [0x80002040]:csrrs a0, fcsr, zero<br> [0x80002044]:sw t6, 752(t1)<br>    |
| 250|[0x80012adc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000205c]:feq.h t6, ft11, ft10<br> [0x80002060]:csrrs a0, fcsr, zero<br> [0x80002064]:sw t6, 760(t1)<br>    |
| 251|[0x80012ae4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000207c]:feq.h t6, ft11, ft10<br> [0x80002080]:csrrs a0, fcsr, zero<br> [0x80002084]:sw t6, 768(t1)<br>    |
| 252|[0x80012aec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000209c]:feq.h t6, ft11, ft10<br> [0x800020a0]:csrrs a0, fcsr, zero<br> [0x800020a4]:sw t6, 776(t1)<br>    |
| 253|[0x80012af4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800020bc]:feq.h t6, ft11, ft10<br> [0x800020c0]:csrrs a0, fcsr, zero<br> [0x800020c4]:sw t6, 784(t1)<br>    |
| 254|[0x80012afc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800020dc]:feq.h t6, ft11, ft10<br> [0x800020e0]:csrrs a0, fcsr, zero<br> [0x800020e4]:sw t6, 792(t1)<br>    |
| 255|[0x80012b04]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800020fc]:feq.h t6, ft11, ft10<br> [0x80002100]:csrrs a0, fcsr, zero<br> [0x80002104]:sw t6, 800(t1)<br>    |
| 256|[0x80012b0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x397 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000211c]:feq.h t6, ft11, ft10<br> [0x80002120]:csrrs a0, fcsr, zero<br> [0x80002124]:sw t6, 808(t1)<br>    |
| 257|[0x80012b14]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x397 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000213c]:feq.h t6, ft11, ft10<br> [0x80002140]:csrrs a0, fcsr, zero<br> [0x80002144]:sw t6, 816(t1)<br>    |
| 258|[0x80012b1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000215c]:feq.h t6, ft11, ft10<br> [0x80002160]:csrrs a0, fcsr, zero<br> [0x80002164]:sw t6, 824(t1)<br>    |
| 259|[0x80012b24]<br>0x00000000|- fs1 == 0 and fe1 == 0x11 and fm1 == 0x17a and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000217c]:feq.h t6, ft11, ft10<br> [0x80002180]:csrrs a0, fcsr, zero<br> [0x80002184]:sw t6, 832(t1)<br>    |
| 260|[0x80012b2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x17a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000219c]:feq.h t6, ft11, ft10<br> [0x800021a0]:csrrs a0, fcsr, zero<br> [0x800021a4]:sw t6, 840(t1)<br>    |
| 261|[0x80012b34]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x2b0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x17a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800021bc]:feq.h t6, ft11, ft10<br> [0x800021c0]:csrrs a0, fcsr, zero<br> [0x800021c4]:sw t6, 848(t1)<br>    |
| 262|[0x80012b3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800021dc]:feq.h t6, ft11, ft10<br> [0x800021e0]:csrrs a0, fcsr, zero<br> [0x800021e4]:sw t6, 856(t1)<br>    |
| 263|[0x80012b44]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800021fc]:feq.h t6, ft11, ft10<br> [0x80002200]:csrrs a0, fcsr, zero<br> [0x80002204]:sw t6, 864(t1)<br>    |
| 264|[0x80012b4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000221c]:feq.h t6, ft11, ft10<br> [0x80002220]:csrrs a0, fcsr, zero<br> [0x80002224]:sw t6, 872(t1)<br>    |
| 265|[0x80012b54]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000223c]:feq.h t6, ft11, ft10<br> [0x80002240]:csrrs a0, fcsr, zero<br> [0x80002244]:sw t6, 880(t1)<br>    |
| 266|[0x80012b5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000225c]:feq.h t6, ft11, ft10<br> [0x80002260]:csrrs a0, fcsr, zero<br> [0x80002264]:sw t6, 888(t1)<br>    |
| 267|[0x80012b64]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000227c]:feq.h t6, ft11, ft10<br> [0x80002280]:csrrs a0, fcsr, zero<br> [0x80002284]:sw t6, 896(t1)<br>    |
| 268|[0x80012b6c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000229c]:feq.h t6, ft11, ft10<br> [0x800022a0]:csrrs a0, fcsr, zero<br> [0x800022a4]:sw t6, 904(t1)<br>    |
| 269|[0x80012b74]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800022bc]:feq.h t6, ft11, ft10<br> [0x800022c0]:csrrs a0, fcsr, zero<br> [0x800022c4]:sw t6, 912(t1)<br>    |
| 270|[0x80012b7c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800022dc]:feq.h t6, ft11, ft10<br> [0x800022e0]:csrrs a0, fcsr, zero<br> [0x800022e4]:sw t6, 920(t1)<br>    |
| 271|[0x80012b84]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800022fc]:feq.h t6, ft11, ft10<br> [0x80002300]:csrrs a0, fcsr, zero<br> [0x80002304]:sw t6, 928(t1)<br>    |
| 272|[0x80012b8c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1b and fm1 == 0x00f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000231c]:feq.h t6, ft11, ft10<br> [0x80002320]:csrrs a0, fcsr, zero<br> [0x80002324]:sw t6, 936(t1)<br>    |
| 273|[0x80012b94]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1b and fm2 == 0x00f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000233c]:feq.h t6, ft11, ft10<br> [0x80002340]:csrrs a0, fcsr, zero<br> [0x80002344]:sw t6, 944(t1)<br>    |
| 274|[0x80012b9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1b and fm1 == 0x00f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000235c]:feq.h t6, ft11, ft10<br> [0x80002360]:csrrs a0, fcsr, zero<br> [0x80002364]:sw t6, 952(t1)<br>    |
| 275|[0x80012ba4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x1b and fm2 == 0x00f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000237c]:feq.h t6, ft11, ft10<br> [0x80002380]:csrrs a0, fcsr, zero<br> [0x80002384]:sw t6, 960(t1)<br>    |
| 276|[0x80012bac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000239c]:feq.h t6, ft11, ft10<br> [0x800023a0]:csrrs a0, fcsr, zero<br> [0x800023a4]:sw t6, 968(t1)<br>    |
| 277|[0x80012bb4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800023bc]:feq.h t6, ft11, ft10<br> [0x800023c0]:csrrs a0, fcsr, zero<br> [0x800023c4]:sw t6, 976(t1)<br>    |
| 278|[0x80012bbc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800023dc]:feq.h t6, ft11, ft10<br> [0x800023e0]:csrrs a0, fcsr, zero<br> [0x800023e4]:sw t6, 984(t1)<br>    |
| 279|[0x80012bc4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800023fc]:feq.h t6, ft11, ft10<br> [0x80002400]:csrrs a0, fcsr, zero<br> [0x80002404]:sw t6, 992(t1)<br>    |
| 280|[0x80012bcc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000243c]:feq.h t6, ft11, ft10<br> [0x80002440]:csrrs a0, fcsr, zero<br> [0x80002444]:sw t6, 1000(t1)<br>   |
| 281|[0x80012bd4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000247c]:feq.h t6, ft11, ft10<br> [0x80002480]:csrrs a0, fcsr, zero<br> [0x80002484]:sw t6, 1008(t1)<br>   |
| 282|[0x80012bdc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800024bc]:feq.h t6, ft11, ft10<br> [0x800024c0]:csrrs a0, fcsr, zero<br> [0x800024c4]:sw t6, 1016(t1)<br>   |
| 283|[0x80012be4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002504]:feq.h t6, ft11, ft10<br> [0x80002508]:csrrs a0, fcsr, zero<br> [0x8000250c]:sw t6, 0(t1)<br>      |
| 284|[0x80012bec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002544]:feq.h t6, ft11, ft10<br> [0x80002548]:csrrs a0, fcsr, zero<br> [0x8000254c]:sw t6, 8(t1)<br>      |
| 285|[0x80012bf4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002584]:feq.h t6, ft11, ft10<br> [0x80002588]:csrrs a0, fcsr, zero<br> [0x8000258c]:sw t6, 16(t1)<br>     |
| 286|[0x80012bfc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800025c4]:feq.h t6, ft11, ft10<br> [0x800025c8]:csrrs a0, fcsr, zero<br> [0x800025cc]:sw t6, 24(t1)<br>     |
| 287|[0x80012c04]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002604]:feq.h t6, ft11, ft10<br> [0x80002608]:csrrs a0, fcsr, zero<br> [0x8000260c]:sw t6, 32(t1)<br>     |
| 288|[0x80012c0c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002644]:feq.h t6, ft11, ft10<br> [0x80002648]:csrrs a0, fcsr, zero<br> [0x8000264c]:sw t6, 40(t1)<br>     |
| 289|[0x80012c14]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002684]:feq.h t6, ft11, ft10<br> [0x80002688]:csrrs a0, fcsr, zero<br> [0x8000268c]:sw t6, 48(t1)<br>     |
| 290|[0x80012c1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800026c4]:feq.h t6, ft11, ft10<br> [0x800026c8]:csrrs a0, fcsr, zero<br> [0x800026cc]:sw t6, 56(t1)<br>     |
| 291|[0x80012c24]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002704]:feq.h t6, ft11, ft10<br> [0x80002708]:csrrs a0, fcsr, zero<br> [0x8000270c]:sw t6, 64(t1)<br>     |
| 292|[0x80012c2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002744]:feq.h t6, ft11, ft10<br> [0x80002748]:csrrs a0, fcsr, zero<br> [0x8000274c]:sw t6, 72(t1)<br>     |
| 293|[0x80012c34]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002784]:feq.h t6, ft11, ft10<br> [0x80002788]:csrrs a0, fcsr, zero<br> [0x8000278c]:sw t6, 80(t1)<br>     |
| 294|[0x80012c3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800027c4]:feq.h t6, ft11, ft10<br> [0x800027c8]:csrrs a0, fcsr, zero<br> [0x800027cc]:sw t6, 88(t1)<br>     |
| 295|[0x80012c44]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002804]:feq.h t6, ft11, ft10<br> [0x80002808]:csrrs a0, fcsr, zero<br> [0x8000280c]:sw t6, 96(t1)<br>     |
| 296|[0x80012c4c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002844]:feq.h t6, ft11, ft10<br> [0x80002848]:csrrs a0, fcsr, zero<br> [0x8000284c]:sw t6, 104(t1)<br>    |
| 297|[0x80012c54]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002884]:feq.h t6, ft11, ft10<br> [0x80002888]:csrrs a0, fcsr, zero<br> [0x8000288c]:sw t6, 112(t1)<br>    |
| 298|[0x80012c5c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800028c4]:feq.h t6, ft11, ft10<br> [0x800028c8]:csrrs a0, fcsr, zero<br> [0x800028cc]:sw t6, 120(t1)<br>    |
| 299|[0x80012c64]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002904]:feq.h t6, ft11, ft10<br> [0x80002908]:csrrs a0, fcsr, zero<br> [0x8000290c]:sw t6, 128(t1)<br>    |
| 300|[0x80012c6c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x045 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002944]:feq.h t6, ft11, ft10<br> [0x80002948]:csrrs a0, fcsr, zero<br> [0x8000294c]:sw t6, 136(t1)<br>    |
| 301|[0x80012c74]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x045 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002984]:feq.h t6, ft11, ft10<br> [0x80002988]:csrrs a0, fcsr, zero<br> [0x8000298c]:sw t6, 144(t1)<br>    |
| 302|[0x80012c7c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x045 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800029c4]:feq.h t6, ft11, ft10<br> [0x800029c8]:csrrs a0, fcsr, zero<br> [0x800029cc]:sw t6, 152(t1)<br>    |
| 303|[0x80012c84]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x045 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002a04]:feq.h t6, ft11, ft10<br> [0x80002a08]:csrrs a0, fcsr, zero<br> [0x80002a0c]:sw t6, 160(t1)<br>    |
| 304|[0x80012c8c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002a44]:feq.h t6, ft11, ft10<br> [0x80002a48]:csrrs a0, fcsr, zero<br> [0x80002a4c]:sw t6, 168(t1)<br>    |
| 305|[0x80012c94]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002a84]:feq.h t6, ft11, ft10<br> [0x80002a88]:csrrs a0, fcsr, zero<br> [0x80002a8c]:sw t6, 176(t1)<br>    |
| 306|[0x80012c9c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002ac4]:feq.h t6, ft11, ft10<br> [0x80002ac8]:csrrs a0, fcsr, zero<br> [0x80002acc]:sw t6, 184(t1)<br>    |
| 307|[0x80012ca4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002b04]:feq.h t6, ft11, ft10<br> [0x80002b08]:csrrs a0, fcsr, zero<br> [0x80002b0c]:sw t6, 192(t1)<br>    |
| 308|[0x80012cac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002b44]:feq.h t6, ft11, ft10<br> [0x80002b48]:csrrs a0, fcsr, zero<br> [0x80002b4c]:sw t6, 200(t1)<br>    |
| 309|[0x80012cb4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002b84]:feq.h t6, ft11, ft10<br> [0x80002b88]:csrrs a0, fcsr, zero<br> [0x80002b8c]:sw t6, 208(t1)<br>    |
| 310|[0x80012cbc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002bc4]:feq.h t6, ft11, ft10<br> [0x80002bc8]:csrrs a0, fcsr, zero<br> [0x80002bcc]:sw t6, 216(t1)<br>    |
| 311|[0x80012cc4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002c04]:feq.h t6, ft11, ft10<br> [0x80002c08]:csrrs a0, fcsr, zero<br> [0x80002c0c]:sw t6, 224(t1)<br>    |
| 312|[0x80012ccc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002c44]:feq.h t6, ft11, ft10<br> [0x80002c48]:csrrs a0, fcsr, zero<br> [0x80002c4c]:sw t6, 232(t1)<br>    |
| 313|[0x80012cd4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002c84]:feq.h t6, ft11, ft10<br> [0x80002c88]:csrrs a0, fcsr, zero<br> [0x80002c8c]:sw t6, 240(t1)<br>    |
| 314|[0x80012cdc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x2b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002cc4]:feq.h t6, ft11, ft10<br> [0x80002cc8]:csrrs a0, fcsr, zero<br> [0x80002ccc]:sw t6, 248(t1)<br>    |
| 315|[0x80012ce4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x2b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002d04]:feq.h t6, ft11, ft10<br> [0x80002d08]:csrrs a0, fcsr, zero<br> [0x80002d0c]:sw t6, 256(t1)<br>    |
| 316|[0x80012cec]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002d44]:feq.h t6, ft11, ft10<br> [0x80002d48]:csrrs a0, fcsr, zero<br> [0x80002d4c]:sw t6, 264(t1)<br>    |
| 317|[0x80012cf4]<br>0x00000000|- fs1 == 0 and fe1 == 0x11 and fm1 == 0x028 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002d84]:feq.h t6, ft11, ft10<br> [0x80002d88]:csrrs a0, fcsr, zero<br> [0x80002d8c]:sw t6, 272(t1)<br>    |
| 318|[0x80012cfc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x028 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002dc4]:feq.h t6, ft11, ft10<br> [0x80002dc8]:csrrs a0, fcsr, zero<br> [0x80002dcc]:sw t6, 280(t1)<br>    |
| 319|[0x80012d04]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x113 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x028 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002e04]:feq.h t6, ft11, ft10<br> [0x80002e08]:csrrs a0, fcsr, zero<br> [0x80002e0c]:sw t6, 288(t1)<br>    |
| 320|[0x80012d0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002e44]:feq.h t6, ft11, ft10<br> [0x80002e48]:csrrs a0, fcsr, zero<br> [0x80002e4c]:sw t6, 296(t1)<br>    |
| 321|[0x80012d14]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002e84]:feq.h t6, ft11, ft10<br> [0x80002e88]:csrrs a0, fcsr, zero<br> [0x80002e8c]:sw t6, 304(t1)<br>    |
| 322|[0x80012d1c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002ec4]:feq.h t6, ft11, ft10<br> [0x80002ec8]:csrrs a0, fcsr, zero<br> [0x80002ecc]:sw t6, 312(t1)<br>    |
| 323|[0x80012d24]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002f04]:feq.h t6, ft11, ft10<br> [0x80002f08]:csrrs a0, fcsr, zero<br> [0x80002f0c]:sw t6, 320(t1)<br>    |
| 324|[0x80012d2c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002f44]:feq.h t6, ft11, ft10<br> [0x80002f48]:csrrs a0, fcsr, zero<br> [0x80002f4c]:sw t6, 328(t1)<br>    |
| 325|[0x80012d34]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002f84]:feq.h t6, ft11, ft10<br> [0x80002f88]:csrrs a0, fcsr, zero<br> [0x80002f8c]:sw t6, 336(t1)<br>    |
| 326|[0x80012d3c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002fc4]:feq.h t6, ft11, ft10<br> [0x80002fc8]:csrrs a0, fcsr, zero<br> [0x80002fcc]:sw t6, 344(t1)<br>    |
| 327|[0x80012d44]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003004]:feq.h t6, ft11, ft10<br> [0x80003008]:csrrs a0, fcsr, zero<br> [0x8000300c]:sw t6, 352(t1)<br>    |
| 328|[0x80012d4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1a and fm1 == 0x1d4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003044]:feq.h t6, ft11, ft10<br> [0x80003048]:csrrs a0, fcsr, zero<br> [0x8000304c]:sw t6, 360(t1)<br>    |
| 329|[0x80012d54]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1a and fm2 == 0x1d4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003084]:feq.h t6, ft11, ft10<br> [0x80003088]:csrrs a0, fcsr, zero<br> [0x8000308c]:sw t6, 368(t1)<br>    |
| 330|[0x80012d5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1a and fm1 == 0x1d4 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800030c4]:feq.h t6, ft11, ft10<br> [0x800030c8]:csrrs a0, fcsr, zero<br> [0x800030cc]:sw t6, 376(t1)<br>    |
| 331|[0x80012d64]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1a and fm2 == 0x1d4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003104]:feq.h t6, ft11, ft10<br> [0x80003108]:csrrs a0, fcsr, zero<br> [0x8000310c]:sw t6, 384(t1)<br>    |
| 332|[0x80012d6c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003144]:feq.h t6, ft11, ft10<br> [0x80003148]:csrrs a0, fcsr, zero<br> [0x8000314c]:sw t6, 392(t1)<br>    |
| 333|[0x80012d74]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003184]:feq.h t6, ft11, ft10<br> [0x80003188]:csrrs a0, fcsr, zero<br> [0x8000318c]:sw t6, 400(t1)<br>    |
| 334|[0x80012d7c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800031c4]:feq.h t6, ft11, ft10<br> [0x800031c8]:csrrs a0, fcsr, zero<br> [0x800031cc]:sw t6, 408(t1)<br>    |
| 335|[0x80012d84]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003204]:feq.h t6, ft11, ft10<br> [0x80003208]:csrrs a0, fcsr, zero<br> [0x8000320c]:sw t6, 416(t1)<br>    |
| 336|[0x80012d8c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003244]:feq.h t6, ft11, ft10<br> [0x80003248]:csrrs a0, fcsr, zero<br> [0x8000324c]:sw t6, 424(t1)<br>    |
| 337|[0x80012d94]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003284]:feq.h t6, ft11, ft10<br> [0x80003288]:csrrs a0, fcsr, zero<br> [0x8000328c]:sw t6, 432(t1)<br>    |
| 338|[0x80012d9c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800032c4]:feq.h t6, ft11, ft10<br> [0x800032c8]:csrrs a0, fcsr, zero<br> [0x800032cc]:sw t6, 440(t1)<br>    |
| 339|[0x80012da4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003304]:feq.h t6, ft11, ft10<br> [0x80003308]:csrrs a0, fcsr, zero<br> [0x8000330c]:sw t6, 448(t1)<br>    |
| 340|[0x80012dac]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003344]:feq.h t6, ft11, ft10<br> [0x80003348]:csrrs a0, fcsr, zero<br> [0x8000334c]:sw t6, 456(t1)<br>    |
| 341|[0x80012db4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003384]:feq.h t6, ft11, ft10<br> [0x80003388]:csrrs a0, fcsr, zero<br> [0x8000338c]:sw t6, 464(t1)<br>    |
| 342|[0x80012dbc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800033c4]:feq.h t6, ft11, ft10<br> [0x800033c8]:csrrs a0, fcsr, zero<br> [0x800033cc]:sw t6, 472(t1)<br>    |
| 343|[0x80012dc4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003404]:feq.h t6, ft11, ft10<br> [0x80003408]:csrrs a0, fcsr, zero<br> [0x8000340c]:sw t6, 480(t1)<br>    |
| 344|[0x80012dcc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003444]:feq.h t6, ft11, ft10<br> [0x80003448]:csrrs a0, fcsr, zero<br> [0x8000344c]:sw t6, 488(t1)<br>    |
| 345|[0x80012dd4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003484]:feq.h t6, ft11, ft10<br> [0x80003488]:csrrs a0, fcsr, zero<br> [0x8000348c]:sw t6, 496(t1)<br>    |
| 346|[0x80012ddc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800034c4]:feq.h t6, ft11, ft10<br> [0x800034c8]:csrrs a0, fcsr, zero<br> [0x800034cc]:sw t6, 504(t1)<br>    |
| 347|[0x80012de4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003504]:feq.h t6, ft11, ft10<br> [0x80003508]:csrrs a0, fcsr, zero<br> [0x8000350c]:sw t6, 512(t1)<br>    |
| 348|[0x80012dec]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003544]:feq.h t6, ft11, ft10<br> [0x80003548]:csrrs a0, fcsr, zero<br> [0x8000354c]:sw t6, 520(t1)<br>    |
| 349|[0x80012df4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003584]:feq.h t6, ft11, ft10<br> [0x80003588]:csrrs a0, fcsr, zero<br> [0x8000358c]:sw t6, 528(t1)<br>    |
| 350|[0x80012dfc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800035c4]:feq.h t6, ft11, ft10<br> [0x800035c8]:csrrs a0, fcsr, zero<br> [0x800035cc]:sw t6, 536(t1)<br>    |
| 351|[0x80012e04]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003604]:feq.h t6, ft11, ft10<br> [0x80003608]:csrrs a0, fcsr, zero<br> [0x8000360c]:sw t6, 544(t1)<br>    |
| 352|[0x80012e0c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003644]:feq.h t6, ft11, ft10<br> [0x80003648]:csrrs a0, fcsr, zero<br> [0x8000364c]:sw t6, 552(t1)<br>    |
| 353|[0x80012e14]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003684]:feq.h t6, ft11, ft10<br> [0x80003688]:csrrs a0, fcsr, zero<br> [0x8000368c]:sw t6, 560(t1)<br>    |
| 354|[0x80012e1c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800036c4]:feq.h t6, ft11, ft10<br> [0x800036c8]:csrrs a0, fcsr, zero<br> [0x800036cc]:sw t6, 568(t1)<br>    |
| 355|[0x80012e24]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003704]:feq.h t6, ft11, ft10<br> [0x80003708]:csrrs a0, fcsr, zero<br> [0x8000370c]:sw t6, 576(t1)<br>    |
| 356|[0x80012e2c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003744]:feq.h t6, ft11, ft10<br> [0x80003748]:csrrs a0, fcsr, zero<br> [0x8000374c]:sw t6, 584(t1)<br>    |
| 357|[0x80012e34]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003784]:feq.h t6, ft11, ft10<br> [0x80003788]:csrrs a0, fcsr, zero<br> [0x8000378c]:sw t6, 592(t1)<br>    |
| 358|[0x80012e3c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800037c4]:feq.h t6, ft11, ft10<br> [0x800037c8]:csrrs a0, fcsr, zero<br> [0x800037cc]:sw t6, 600(t1)<br>    |
| 359|[0x80012e44]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x032 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003804]:feq.h t6, ft11, ft10<br> [0x80003808]:csrrs a0, fcsr, zero<br> [0x8000380c]:sw t6, 608(t1)<br>    |
| 360|[0x80012e4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x032 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003844]:feq.h t6, ft11, ft10<br> [0x80003848]:csrrs a0, fcsr, zero<br> [0x8000384c]:sw t6, 616(t1)<br>    |
| 361|[0x80012e54]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x032 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003884]:feq.h t6, ft11, ft10<br> [0x80003888]:csrrs a0, fcsr, zero<br> [0x8000388c]:sw t6, 624(t1)<br>    |
| 362|[0x80012e5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x032 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800038c4]:feq.h t6, ft11, ft10<br> [0x800038c8]:csrrs a0, fcsr, zero<br> [0x800038cc]:sw t6, 632(t1)<br>    |
| 363|[0x80012e64]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003904]:feq.h t6, ft11, ft10<br> [0x80003908]:csrrs a0, fcsr, zero<br> [0x8000390c]:sw t6, 640(t1)<br>    |
| 364|[0x80012e6c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003944]:feq.h t6, ft11, ft10<br> [0x80003948]:csrrs a0, fcsr, zero<br> [0x8000394c]:sw t6, 648(t1)<br>    |
| 365|[0x80012e74]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003984]:feq.h t6, ft11, ft10<br> [0x80003988]:csrrs a0, fcsr, zero<br> [0x8000398c]:sw t6, 656(t1)<br>    |
| 366|[0x80012e7c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800039c4]:feq.h t6, ft11, ft10<br> [0x800039c8]:csrrs a0, fcsr, zero<br> [0x800039cc]:sw t6, 664(t1)<br>    |
| 367|[0x80012e84]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003a04]:feq.h t6, ft11, ft10<br> [0x80003a08]:csrrs a0, fcsr, zero<br> [0x80003a0c]:sw t6, 672(t1)<br>    |
| 368|[0x80012e8c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003a44]:feq.h t6, ft11, ft10<br> [0x80003a48]:csrrs a0, fcsr, zero<br> [0x80003a4c]:sw t6, 680(t1)<br>    |
| 369|[0x80012e94]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003a84]:feq.h t6, ft11, ft10<br> [0x80003a88]:csrrs a0, fcsr, zero<br> [0x80003a8c]:sw t6, 688(t1)<br>    |
| 370|[0x80012e9c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003ac4]:feq.h t6, ft11, ft10<br> [0x80003ac8]:csrrs a0, fcsr, zero<br> [0x80003acc]:sw t6, 696(t1)<br>    |
| 371|[0x80012ea4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003b04]:feq.h t6, ft11, ft10<br> [0x80003b08]:csrrs a0, fcsr, zero<br> [0x80003b0c]:sw t6, 704(t1)<br>    |
| 372|[0x80012eac]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003b44]:feq.h t6, ft11, ft10<br> [0x80003b48]:csrrs a0, fcsr, zero<br> [0x80003b4c]:sw t6, 712(t1)<br>    |
| 373|[0x80012eb4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x1f4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003b84]:feq.h t6, ft11, ft10<br> [0x80003b88]:csrrs a0, fcsr, zero<br> [0x80003b8c]:sw t6, 720(t1)<br>    |
| 374|[0x80012ebc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x1f4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003bc4]:feq.h t6, ft11, ft10<br> [0x80003bc8]:csrrs a0, fcsr, zero<br> [0x80003bcc]:sw t6, 728(t1)<br>    |
| 375|[0x80012ec4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003c04]:feq.h t6, ft11, ft10<br> [0x80003c08]:csrrs a0, fcsr, zero<br> [0x80003c0c]:sw t6, 736(t1)<br>    |
| 376|[0x80012ecc]<br>0x00000000|- fs1 == 1 and fe1 == 0x10 and fm1 == 0x1f8 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003c44]:feq.h t6, ft11, ft10<br> [0x80003c48]:csrrs a0, fcsr, zero<br> [0x80003c4c]:sw t6, 744(t1)<br>    |
| 377|[0x80012ed4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x1f8 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003c84]:feq.h t6, ft11, ft10<br> [0x80003c88]:csrrs a0, fcsr, zero<br> [0x80003c8c]:sw t6, 752(t1)<br>    |
| 378|[0x80012edc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x349 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x1f8 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003cc4]:feq.h t6, ft11, ft10<br> [0x80003cc8]:csrrs a0, fcsr, zero<br> [0x80003ccc]:sw t6, 760(t1)<br>    |
| 379|[0x80012ee4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003d04]:feq.h t6, ft11, ft10<br> [0x80003d08]:csrrs a0, fcsr, zero<br> [0x80003d0c]:sw t6, 768(t1)<br>    |
| 380|[0x80012eec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003d44]:feq.h t6, ft11, ft10<br> [0x80003d48]:csrrs a0, fcsr, zero<br> [0x80003d4c]:sw t6, 776(t1)<br>    |
| 381|[0x80012ef4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003d84]:feq.h t6, ft11, ft10<br> [0x80003d88]:csrrs a0, fcsr, zero<br> [0x80003d8c]:sw t6, 784(t1)<br>    |
| 382|[0x80012efc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003dc4]:feq.h t6, ft11, ft10<br> [0x80003dc8]:csrrs a0, fcsr, zero<br> [0x80003dcc]:sw t6, 792(t1)<br>    |
| 383|[0x80012f04]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003e04]:feq.h t6, ft11, ft10<br> [0x80003e08]:csrrs a0, fcsr, zero<br> [0x80003e0c]:sw t6, 800(t1)<br>    |
| 384|[0x80012f0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003e44]:feq.h t6, ft11, ft10<br> [0x80003e48]:csrrs a0, fcsr, zero<br> [0x80003e4c]:sw t6, 808(t1)<br>    |
| 385|[0x80012f14]<br>0x00000000|- fs1 == 1 and fe1 == 0x1b and fm1 == 0x1fa and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003e84]:feq.h t6, ft11, ft10<br> [0x80003e88]:csrrs a0, fcsr, zero<br> [0x80003e8c]:sw t6, 816(t1)<br>    |
| 386|[0x80012f1c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1b and fm2 == 0x1fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003ec4]:feq.h t6, ft11, ft10<br> [0x80003ec8]:csrrs a0, fcsr, zero<br> [0x80003ecc]:sw t6, 824(t1)<br>    |
| 387|[0x80012f24]<br>0x00000000|- fs1 == 1 and fe1 == 0x1b and fm1 == 0x1fa and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003f04]:feq.h t6, ft11, ft10<br> [0x80003f08]:csrrs a0, fcsr, zero<br> [0x80003f0c]:sw t6, 832(t1)<br>    |
| 388|[0x80012f2c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x1b and fm2 == 0x1fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003f44]:feq.h t6, ft11, ft10<br> [0x80003f48]:csrrs a0, fcsr, zero<br> [0x80003f4c]:sw t6, 840(t1)<br>    |
| 389|[0x80012f34]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003f84]:feq.h t6, ft11, ft10<br> [0x80003f88]:csrrs a0, fcsr, zero<br> [0x80003f8c]:sw t6, 848(t1)<br>    |
| 390|[0x80012f3c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003fc4]:feq.h t6, ft11, ft10<br> [0x80003fc8]:csrrs a0, fcsr, zero<br> [0x80003fcc]:sw t6, 856(t1)<br>    |
| 391|[0x80012f44]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004004]:feq.h t6, ft11, ft10<br> [0x80004008]:csrrs a0, fcsr, zero<br> [0x8000400c]:sw t6, 864(t1)<br>    |
| 392|[0x80012f4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004044]:feq.h t6, ft11, ft10<br> [0x80004048]:csrrs a0, fcsr, zero<br> [0x8000404c]:sw t6, 872(t1)<br>    |
| 393|[0x80012f54]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004084]:feq.h t6, ft11, ft10<br> [0x80004088]:csrrs a0, fcsr, zero<br> [0x8000408c]:sw t6, 880(t1)<br>    |
| 394|[0x80012f5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800040c4]:feq.h t6, ft11, ft10<br> [0x800040c8]:csrrs a0, fcsr, zero<br> [0x800040cc]:sw t6, 888(t1)<br>    |
| 395|[0x80012f64]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x00a and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004104]:feq.h t6, ft11, ft10<br> [0x80004108]:csrrs a0, fcsr, zero<br> [0x8000410c]:sw t6, 896(t1)<br>    |
| 396|[0x80012f6c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x00a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004144]:feq.h t6, ft11, ft10<br> [0x80004148]:csrrs a0, fcsr, zero<br> [0x8000414c]:sw t6, 904(t1)<br>    |
| 397|[0x80012f74]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x00a and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004184]:feq.h t6, ft11, ft10<br> [0x80004188]:csrrs a0, fcsr, zero<br> [0x8000418c]:sw t6, 912(t1)<br>    |
| 398|[0x80012f7c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x00a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800041c4]:feq.h t6, ft11, ft10<br> [0x800041c8]:csrrs a0, fcsr, zero<br> [0x800041cc]:sw t6, 920(t1)<br>    |
| 399|[0x80012f84]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004204]:feq.h t6, ft11, ft10<br> [0x80004208]:csrrs a0, fcsr, zero<br> [0x8000420c]:sw t6, 928(t1)<br>    |
| 400|[0x80012f8c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004244]:feq.h t6, ft11, ft10<br> [0x80004248]:csrrs a0, fcsr, zero<br> [0x8000424c]:sw t6, 936(t1)<br>    |
| 401|[0x80012f94]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004284]:feq.h t6, ft11, ft10<br> [0x80004288]:csrrs a0, fcsr, zero<br> [0x8000428c]:sw t6, 944(t1)<br>    |
| 402|[0x80012f9c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800042c4]:feq.h t6, ft11, ft10<br> [0x800042c8]:csrrs a0, fcsr, zero<br> [0x800042cc]:sw t6, 952(t1)<br>    |
| 403|[0x80012fa4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004304]:feq.h t6, ft11, ft10<br> [0x80004308]:csrrs a0, fcsr, zero<br> [0x8000430c]:sw t6, 960(t1)<br>    |
| 404|[0x80012fac]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004344]:feq.h t6, ft11, ft10<br> [0x80004348]:csrrs a0, fcsr, zero<br> [0x8000434c]:sw t6, 968(t1)<br>    |
| 405|[0x80012fb4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004384]:feq.h t6, ft11, ft10<br> [0x80004388]:csrrs a0, fcsr, zero<br> [0x8000438c]:sw t6, 976(t1)<br>    |
| 406|[0x80012fbc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800043c4]:feq.h t6, ft11, ft10<br> [0x800043c8]:csrrs a0, fcsr, zero<br> [0x800043cc]:sw t6, 984(t1)<br>    |
| 407|[0x80012fc4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004404]:feq.h t6, ft11, ft10<br> [0x80004408]:csrrs a0, fcsr, zero<br> [0x8000440c]:sw t6, 992(t1)<br>    |
| 408|[0x80012fcc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004444]:feq.h t6, ft11, ft10<br> [0x80004448]:csrrs a0, fcsr, zero<br> [0x8000444c]:sw t6, 1000(t1)<br>   |
| 409|[0x80012fd4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004484]:feq.h t6, ft11, ft10<br> [0x80004488]:csrrs a0, fcsr, zero<br> [0x8000448c]:sw t6, 1008(t1)<br>   |
| 410|[0x80012fdc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800044c4]:feq.h t6, ft11, ft10<br> [0x800044c8]:csrrs a0, fcsr, zero<br> [0x800044cc]:sw t6, 1016(t1)<br>   |
| 411|[0x80012fe4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000450c]:feq.h t6, ft11, ft10<br> [0x80004510]:csrrs a0, fcsr, zero<br> [0x80004514]:sw t6, 0(t1)<br>      |
| 412|[0x80012fec]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000454c]:feq.h t6, ft11, ft10<br> [0x80004550]:csrrs a0, fcsr, zero<br> [0x80004554]:sw t6, 8(t1)<br>      |
| 413|[0x80012ff4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000458c]:feq.h t6, ft11, ft10<br> [0x80004590]:csrrs a0, fcsr, zero<br> [0x80004594]:sw t6, 16(t1)<br>     |
| 414|[0x80012ffc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800045cc]:feq.h t6, ft11, ft10<br> [0x800045d0]:csrrs a0, fcsr, zero<br> [0x800045d4]:sw t6, 24(t1)<br>     |
| 415|[0x80013004]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000460c]:feq.h t6, ft11, ft10<br> [0x80004610]:csrrs a0, fcsr, zero<br> [0x80004614]:sw t6, 32(t1)<br>     |
| 416|[0x8001300c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x066 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000464c]:feq.h t6, ft11, ft10<br> [0x80004650]:csrrs a0, fcsr, zero<br> [0x80004654]:sw t6, 40(t1)<br>     |
| 417|[0x80013014]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x066 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000468c]:feq.h t6, ft11, ft10<br> [0x80004690]:csrrs a0, fcsr, zero<br> [0x80004694]:sw t6, 48(t1)<br>     |
| 418|[0x8001301c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x066 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800046cc]:feq.h t6, ft11, ft10<br> [0x800046d0]:csrrs a0, fcsr, zero<br> [0x800046d4]:sw t6, 56(t1)<br>     |
| 419|[0x80013024]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x066 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000470c]:feq.h t6, ft11, ft10<br> [0x80004710]:csrrs a0, fcsr, zero<br> [0x80004714]:sw t6, 64(t1)<br>     |
| 420|[0x8001302c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000474c]:feq.h t6, ft11, ft10<br> [0x80004750]:csrrs a0, fcsr, zero<br> [0x80004754]:sw t6, 72(t1)<br>     |
| 421|[0x80013034]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000478c]:feq.h t6, ft11, ft10<br> [0x80004790]:csrrs a0, fcsr, zero<br> [0x80004794]:sw t6, 80(t1)<br>     |
| 422|[0x8001303c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800047cc]:feq.h t6, ft11, ft10<br> [0x800047d0]:csrrs a0, fcsr, zero<br> [0x800047d4]:sw t6, 88(t1)<br>     |
| 423|[0x80013044]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000480c]:feq.h t6, ft11, ft10<br> [0x80004810]:csrrs a0, fcsr, zero<br> [0x80004814]:sw t6, 96(t1)<br>     |
| 424|[0x8001304c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000484c]:feq.h t6, ft11, ft10<br> [0x80004850]:csrrs a0, fcsr, zero<br> [0x80004854]:sw t6, 104(t1)<br>    |
| 425|[0x80013054]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000488c]:feq.h t6, ft11, ft10<br> [0x80004890]:csrrs a0, fcsr, zero<br> [0x80004894]:sw t6, 112(t1)<br>    |
| 426|[0x8001305c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800048cc]:feq.h t6, ft11, ft10<br> [0x800048d0]:csrrs a0, fcsr, zero<br> [0x800048d4]:sw t6, 120(t1)<br>    |
| 427|[0x80013064]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000490c]:feq.h t6, ft11, ft10<br> [0x80004910]:csrrs a0, fcsr, zero<br> [0x80004914]:sw t6, 128(t1)<br>    |
| 428|[0x8001306c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000494c]:feq.h t6, ft11, ft10<br> [0x80004950]:csrrs a0, fcsr, zero<br> [0x80004954]:sw t6, 136(t1)<br>    |
| 429|[0x80013074]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000498c]:feq.h t6, ft11, ft10<br> [0x80004990]:csrrs a0, fcsr, zero<br> [0x80004994]:sw t6, 144(t1)<br>    |
| 430|[0x8001307c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800049cc]:feq.h t6, ft11, ft10<br> [0x800049d0]:csrrs a0, fcsr, zero<br> [0x800049d4]:sw t6, 152(t1)<br>    |
| 431|[0x80013084]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004a0c]:feq.h t6, ft11, ft10<br> [0x80004a10]:csrrs a0, fcsr, zero<br> [0x80004a14]:sw t6, 160(t1)<br>    |
| 432|[0x8001308c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004a4c]:feq.h t6, ft11, ft10<br> [0x80004a50]:csrrs a0, fcsr, zero<br> [0x80004a54]:sw t6, 168(t1)<br>    |
| 433|[0x80013094]<br>0x00000000|- fs1 == 1 and fe1 == 0x11 and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004a8c]:feq.h t6, ft11, ft10<br> [0x80004a90]:csrrs a0, fcsr, zero<br> [0x80004a94]:sw t6, 176(t1)<br>    |
| 434|[0x8001309c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004acc]:feq.h t6, ft11, ft10<br> [0x80004ad0]:csrrs a0, fcsr, zero<br> [0x80004ad4]:sw t6, 184(t1)<br>    |
| 435|[0x800130a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x378 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004b0c]:feq.h t6, ft11, ft10<br> [0x80004b10]:csrrs a0, fcsr, zero<br> [0x80004b14]:sw t6, 192(t1)<br>    |
| 436|[0x800130ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004b4c]:feq.h t6, ft11, ft10<br> [0x80004b50]:csrrs a0, fcsr, zero<br> [0x80004b54]:sw t6, 200(t1)<br>    |
| 437|[0x800130b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004b8c]:feq.h t6, ft11, ft10<br> [0x80004b90]:csrrs a0, fcsr, zero<br> [0x80004b94]:sw t6, 208(t1)<br>    |
| 438|[0x800130bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004bcc]:feq.h t6, ft11, ft10<br> [0x80004bd0]:csrrs a0, fcsr, zero<br> [0x80004bd4]:sw t6, 216(t1)<br>    |
| 439|[0x800130c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004c0c]:feq.h t6, ft11, ft10<br> [0x80004c10]:csrrs a0, fcsr, zero<br> [0x80004c14]:sw t6, 224(t1)<br>    |
| 440|[0x800130cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1b and fm1 == 0x0e5 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004c4c]:feq.h t6, ft11, ft10<br> [0x80004c50]:csrrs a0, fcsr, zero<br> [0x80004c54]:sw t6, 232(t1)<br>    |
| 441|[0x800130d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1b and fm2 == 0x0e5 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004c8c]:feq.h t6, ft11, ft10<br> [0x80004c90]:csrrs a0, fcsr, zero<br> [0x80004c94]:sw t6, 240(t1)<br>    |
| 442|[0x800130dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1b and fm1 == 0x0e5 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004ccc]:feq.h t6, ft11, ft10<br> [0x80004cd0]:csrrs a0, fcsr, zero<br> [0x80004cd4]:sw t6, 248(t1)<br>    |
| 443|[0x800130e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x1b and fm2 == 0x0e5 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004d0c]:feq.h t6, ft11, ft10<br> [0x80004d10]:csrrs a0, fcsr, zero<br> [0x80004d14]:sw t6, 256(t1)<br>    |
| 444|[0x800130ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004d4c]:feq.h t6, ft11, ft10<br> [0x80004d50]:csrrs a0, fcsr, zero<br> [0x80004d54]:sw t6, 264(t1)<br>    |
| 445|[0x800130f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004d8c]:feq.h t6, ft11, ft10<br> [0x80004d90]:csrrs a0, fcsr, zero<br> [0x80004d94]:sw t6, 272(t1)<br>    |
| 446|[0x800130fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004dcc]:feq.h t6, ft11, ft10<br> [0x80004dd0]:csrrs a0, fcsr, zero<br> [0x80004dd4]:sw t6, 280(t1)<br>    |
| 447|[0x80013104]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004e0c]:feq.h t6, ft11, ft10<br> [0x80004e10]:csrrs a0, fcsr, zero<br> [0x80004e14]:sw t6, 288(t1)<br>    |
| 448|[0x8001310c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004e4c]:feq.h t6, ft11, ft10<br> [0x80004e50]:csrrs a0, fcsr, zero<br> [0x80004e54]:sw t6, 296(t1)<br>    |
| 449|[0x80013114]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004e8c]:feq.h t6, ft11, ft10<br> [0x80004e90]:csrrs a0, fcsr, zero<br> [0x80004e94]:sw t6, 304(t1)<br>    |
| 450|[0x8001311c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x008 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004ecc]:feq.h t6, ft11, ft10<br> [0x80004ed0]:csrrs a0, fcsr, zero<br> [0x80004ed4]:sw t6, 312(t1)<br>    |
| 451|[0x80013124]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x008 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004f0c]:feq.h t6, ft11, ft10<br> [0x80004f10]:csrrs a0, fcsr, zero<br> [0x80004f14]:sw t6, 320(t1)<br>    |
| 452|[0x8001312c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x008 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004f4c]:feq.h t6, ft11, ft10<br> [0x80004f50]:csrrs a0, fcsr, zero<br> [0x80004f54]:sw t6, 328(t1)<br>    |
| 453|[0x80013134]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x008 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004f8c]:feq.h t6, ft11, ft10<br> [0x80004f90]:csrrs a0, fcsr, zero<br> [0x80004f94]:sw t6, 336(t1)<br>    |
| 454|[0x8001313c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004fcc]:feq.h t6, ft11, ft10<br> [0x80004fd0]:csrrs a0, fcsr, zero<br> [0x80004fd4]:sw t6, 344(t1)<br>    |
| 455|[0x80013144]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000500c]:feq.h t6, ft11, ft10<br> [0x80005010]:csrrs a0, fcsr, zero<br> [0x80005014]:sw t6, 352(t1)<br>    |
| 456|[0x8001314c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000504c]:feq.h t6, ft11, ft10<br> [0x80005050]:csrrs a0, fcsr, zero<br> [0x80005054]:sw t6, 360(t1)<br>    |
| 457|[0x80013154]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000508c]:feq.h t6, ft11, ft10<br> [0x80005090]:csrrs a0, fcsr, zero<br> [0x80005094]:sw t6, 368(t1)<br>    |
| 458|[0x8001315c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800050cc]:feq.h t6, ft11, ft10<br> [0x800050d0]:csrrs a0, fcsr, zero<br> [0x800050d4]:sw t6, 376(t1)<br>    |
| 459|[0x80013164]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000510c]:feq.h t6, ft11, ft10<br> [0x80005110]:csrrs a0, fcsr, zero<br> [0x80005114]:sw t6, 384(t1)<br>    |
| 460|[0x8001316c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000514c]:feq.h t6, ft11, ft10<br> [0x80005150]:csrrs a0, fcsr, zero<br> [0x80005154]:sw t6, 392(t1)<br>    |
| 461|[0x80013174]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000518c]:feq.h t6, ft11, ft10<br> [0x80005190]:csrrs a0, fcsr, zero<br> [0x80005194]:sw t6, 400(t1)<br>    |
| 462|[0x8001317c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800051cc]:feq.h t6, ft11, ft10<br> [0x800051d0]:csrrs a0, fcsr, zero<br> [0x800051d4]:sw t6, 408(t1)<br>    |
| 463|[0x80013184]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000520c]:feq.h t6, ft11, ft10<br> [0x80005210]:csrrs a0, fcsr, zero<br> [0x80005214]:sw t6, 416(t1)<br>    |
| 464|[0x8001318c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000524c]:feq.h t6, ft11, ft10<br> [0x80005250]:csrrs a0, fcsr, zero<br> [0x80005254]:sw t6, 424(t1)<br>    |
| 465|[0x80013194]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000528c]:feq.h t6, ft11, ft10<br> [0x80005290]:csrrs a0, fcsr, zero<br> [0x80005294]:sw t6, 432(t1)<br>    |
| 466|[0x8001319c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800052cc]:feq.h t6, ft11, ft10<br> [0x800052d0]:csrrs a0, fcsr, zero<br> [0x800052d4]:sw t6, 440(t1)<br>    |
| 467|[0x800131a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000530c]:feq.h t6, ft11, ft10<br> [0x80005310]:csrrs a0, fcsr, zero<br> [0x80005314]:sw t6, 448(t1)<br>    |
| 468|[0x800131ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000534c]:feq.h t6, ft11, ft10<br> [0x80005350]:csrrs a0, fcsr, zero<br> [0x80005354]:sw t6, 456(t1)<br>    |
| 469|[0x800131b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000538c]:feq.h t6, ft11, ft10<br> [0x80005390]:csrrs a0, fcsr, zero<br> [0x80005394]:sw t6, 464(t1)<br>    |
| 470|[0x800131bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800053cc]:feq.h t6, ft11, ft10<br> [0x800053d0]:csrrs a0, fcsr, zero<br> [0x800053d4]:sw t6, 472(t1)<br>    |
| 471|[0x800131c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x054 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000540c]:feq.h t6, ft11, ft10<br> [0x80005410]:csrrs a0, fcsr, zero<br> [0x80005414]:sw t6, 480(t1)<br>    |
| 472|[0x800131cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x054 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000544c]:feq.h t6, ft11, ft10<br> [0x80005450]:csrrs a0, fcsr, zero<br> [0x80005454]:sw t6, 488(t1)<br>    |
| 473|[0x800131d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x054 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000548c]:feq.h t6, ft11, ft10<br> [0x80005490]:csrrs a0, fcsr, zero<br> [0x80005494]:sw t6, 496(t1)<br>    |
| 474|[0x800131dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x054 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800054cc]:feq.h t6, ft11, ft10<br> [0x800054d0]:csrrs a0, fcsr, zero<br> [0x800054d4]:sw t6, 504(t1)<br>    |
| 475|[0x800131e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000550c]:feq.h t6, ft11, ft10<br> [0x80005510]:csrrs a0, fcsr, zero<br> [0x80005514]:sw t6, 512(t1)<br>    |
| 476|[0x800131ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000554c]:feq.h t6, ft11, ft10<br> [0x80005550]:csrrs a0, fcsr, zero<br> [0x80005554]:sw t6, 520(t1)<br>    |
| 477|[0x800131f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000558c]:feq.h t6, ft11, ft10<br> [0x80005590]:csrrs a0, fcsr, zero<br> [0x80005594]:sw t6, 528(t1)<br>    |
| 478|[0x800131fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800055cc]:feq.h t6, ft11, ft10<br> [0x800055d0]:csrrs a0, fcsr, zero<br> [0x800055d4]:sw t6, 536(t1)<br>    |
| 479|[0x80013204]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000560c]:feq.h t6, ft11, ft10<br> [0x80005610]:csrrs a0, fcsr, zero<br> [0x80005614]:sw t6, 544(t1)<br>    |
| 480|[0x8001320c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000564c]:feq.h t6, ft11, ft10<br> [0x80005650]:csrrs a0, fcsr, zero<br> [0x80005654]:sw t6, 552(t1)<br>    |
| 481|[0x80013214]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000568c]:feq.h t6, ft11, ft10<br> [0x80005690]:csrrs a0, fcsr, zero<br> [0x80005694]:sw t6, 560(t1)<br>    |
| 482|[0x8001321c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800056cc]:feq.h t6, ft11, ft10<br> [0x800056d0]:csrrs a0, fcsr, zero<br> [0x800056d4]:sw t6, 568(t1)<br>    |
| 483|[0x80013224]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000570c]:feq.h t6, ft11, ft10<br> [0x80005710]:csrrs a0, fcsr, zero<br> [0x80005714]:sw t6, 576(t1)<br>    |
| 484|[0x8001322c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000574c]:feq.h t6, ft11, ft10<br> [0x80005750]:csrrs a0, fcsr, zero<br> [0x80005754]:sw t6, 584(t1)<br>    |
| 485|[0x80013234]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000578c]:feq.h t6, ft11, ft10<br> [0x80005790]:csrrs a0, fcsr, zero<br> [0x80005794]:sw t6, 592(t1)<br>    |
| 486|[0x8001323c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x349 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800057cc]:feq.h t6, ft11, ft10<br> [0x800057d0]:csrrs a0, fcsr, zero<br> [0x800057d4]:sw t6, 600(t1)<br>    |
| 487|[0x80013244]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000580c]:feq.h t6, ft11, ft10<br> [0x80005810]:csrrs a0, fcsr, zero<br> [0x80005814]:sw t6, 608(t1)<br>    |
| 488|[0x8001324c]<br>0x00000000|- fs1 == 1 and fe1 == 0x11 and fm1 == 0x103 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000584c]:feq.h t6, ft11, ft10<br> [0x80005850]:csrrs a0, fcsr, zero<br> [0x80005854]:sw t6, 616(t1)<br>    |
| 489|[0x80013254]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x103 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000588c]:feq.h t6, ft11, ft10<br> [0x80005890]:csrrs a0, fcsr, zero<br> [0x80005894]:sw t6, 624(t1)<br>    |
| 490|[0x8001325c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x21f and fs2 == 1 and fe2 == 0x11 and fm2 == 0x103 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800058cc]:feq.h t6, ft11, ft10<br> [0x800058d0]:csrrs a0, fcsr, zero<br> [0x800058d4]:sw t6, 632(t1)<br>    |
| 491|[0x80013264]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000590c]:feq.h t6, ft11, ft10<br> [0x80005910]:csrrs a0, fcsr, zero<br> [0x80005914]:sw t6, 640(t1)<br>    |
| 492|[0x8001326c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000594c]:feq.h t6, ft11, ft10<br> [0x80005950]:csrrs a0, fcsr, zero<br> [0x80005954]:sw t6, 648(t1)<br>    |
| 493|[0x80013274]<br>0x00000000|- fs1 == 1 and fe1 == 0x1a and fm1 == 0x2b3 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000598c]:feq.h t6, ft11, ft10<br> [0x80005990]:csrrs a0, fcsr, zero<br> [0x80005994]:sw t6, 656(t1)<br>    |
| 494|[0x8001327c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1a and fm2 == 0x2b3 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800059cc]:feq.h t6, ft11, ft10<br> [0x800059d0]:csrrs a0, fcsr, zero<br> [0x800059d4]:sw t6, 664(t1)<br>    |
| 495|[0x80013284]<br>0x00000000|- fs1 == 1 and fe1 == 0x1a and fm1 == 0x2b3 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005a0c]:feq.h t6, ft11, ft10<br> [0x80005a10]:csrrs a0, fcsr, zero<br> [0x80005a14]:sw t6, 672(t1)<br>    |
| 496|[0x8001328c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x1a and fm2 == 0x2b3 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005a4c]:feq.h t6, ft11, ft10<br> [0x80005a50]:csrrs a0, fcsr, zero<br> [0x80005a54]:sw t6, 680(t1)<br>    |
| 497|[0x80013294]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005a8c]:feq.h t6, ft11, ft10<br> [0x80005a90]:csrrs a0, fcsr, zero<br> [0x80005a94]:sw t6, 688(t1)<br>    |
| 498|[0x8001329c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005acc]:feq.h t6, ft11, ft10<br> [0x80005ad0]:csrrs a0, fcsr, zero<br> [0x80005ad4]:sw t6, 696(t1)<br>    |
| 499|[0x800132a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005b0c]:feq.h t6, ft11, ft10<br> [0x80005b10]:csrrs a0, fcsr, zero<br> [0x80005b14]:sw t6, 704(t1)<br>    |
| 500|[0x800132ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005b4c]:feq.h t6, ft11, ft10<br> [0x80005b50]:csrrs a0, fcsr, zero<br> [0x80005b54]:sw t6, 712(t1)<br>    |
| 501|[0x800132b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005b8c]:feq.h t6, ft11, ft10<br> [0x80005b90]:csrrs a0, fcsr, zero<br> [0x80005b94]:sw t6, 720(t1)<br>    |
| 502|[0x800132bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005bcc]:feq.h t6, ft11, ft10<br> [0x80005bd0]:csrrs a0, fcsr, zero<br> [0x80005bd4]:sw t6, 728(t1)<br>    |
| 503|[0x800132c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005c0c]:feq.h t6, ft11, ft10<br> [0x80005c10]:csrrs a0, fcsr, zero<br> [0x80005c14]:sw t6, 736(t1)<br>    |
| 504|[0x800132cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005c4c]:feq.h t6, ft11, ft10<br> [0x80005c50]:csrrs a0, fcsr, zero<br> [0x80005c54]:sw t6, 744(t1)<br>    |
| 505|[0x800132d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005c8c]:feq.h t6, ft11, ft10<br> [0x80005c90]:csrrs a0, fcsr, zero<br> [0x80005c94]:sw t6, 752(t1)<br>    |
| 506|[0x800132dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005ccc]:feq.h t6, ft11, ft10<br> [0x80005cd0]:csrrs a0, fcsr, zero<br> [0x80005cd4]:sw t6, 760(t1)<br>    |
| 507|[0x800132e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005d0c]:feq.h t6, ft11, ft10<br> [0x80005d10]:csrrs a0, fcsr, zero<br> [0x80005d14]:sw t6, 768(t1)<br>    |
| 508|[0x800132ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005d4c]:feq.h t6, ft11, ft10<br> [0x80005d50]:csrrs a0, fcsr, zero<br> [0x80005d54]:sw t6, 776(t1)<br>    |
| 509|[0x800132f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005d8c]:feq.h t6, ft11, ft10<br> [0x80005d90]:csrrs a0, fcsr, zero<br> [0x80005d94]:sw t6, 784(t1)<br>    |
| 510|[0x800132fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005dcc]:feq.h t6, ft11, ft10<br> [0x80005dd0]:csrrs a0, fcsr, zero<br> [0x80005dd4]:sw t6, 792(t1)<br>    |
| 511|[0x80013304]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005e0c]:feq.h t6, ft11, ft10<br> [0x80005e10]:csrrs a0, fcsr, zero<br> [0x80005e14]:sw t6, 800(t1)<br>    |
| 512|[0x8001330c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005e4c]:feq.h t6, ft11, ft10<br> [0x80005e50]:csrrs a0, fcsr, zero<br> [0x80005e54]:sw t6, 808(t1)<br>    |
| 513|[0x80013314]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005e8c]:feq.h t6, ft11, ft10<br> [0x80005e90]:csrrs a0, fcsr, zero<br> [0x80005e94]:sw t6, 816(t1)<br>    |
| 514|[0x8001331c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005ecc]:feq.h t6, ft11, ft10<br> [0x80005ed0]:csrrs a0, fcsr, zero<br> [0x80005ed4]:sw t6, 824(t1)<br>    |
| 515|[0x80013324]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005f0c]:feq.h t6, ft11, ft10<br> [0x80005f10]:csrrs a0, fcsr, zero<br> [0x80005f14]:sw t6, 832(t1)<br>    |
| 516|[0x8001332c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005f4c]:feq.h t6, ft11, ft10<br> [0x80005f50]:csrrs a0, fcsr, zero<br> [0x80005f54]:sw t6, 840(t1)<br>    |
| 517|[0x80013334]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005f8c]:feq.h t6, ft11, ft10<br> [0x80005f90]:csrrs a0, fcsr, zero<br> [0x80005f94]:sw t6, 848(t1)<br>    |
| 518|[0x8001333c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005fcc]:feq.h t6, ft11, ft10<br> [0x80005fd0]:csrrs a0, fcsr, zero<br> [0x80005fd4]:sw t6, 856(t1)<br>    |
| 519|[0x80013344]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000600c]:feq.h t6, ft11, ft10<br> [0x80006010]:csrrs a0, fcsr, zero<br> [0x80006014]:sw t6, 864(t1)<br>    |
| 520|[0x8001334c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000604c]:feq.h t6, ft11, ft10<br> [0x80006050]:csrrs a0, fcsr, zero<br> [0x80006054]:sw t6, 872(t1)<br>    |
| 521|[0x80013354]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x039 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000608c]:feq.h t6, ft11, ft10<br> [0x80006090]:csrrs a0, fcsr, zero<br> [0x80006094]:sw t6, 880(t1)<br>    |
| 522|[0x8001335c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x039 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800060cc]:feq.h t6, ft11, ft10<br> [0x800060d0]:csrrs a0, fcsr, zero<br> [0x800060d4]:sw t6, 888(t1)<br>    |
| 523|[0x80013364]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x039 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000610c]:feq.h t6, ft11, ft10<br> [0x80006110]:csrrs a0, fcsr, zero<br> [0x80006114]:sw t6, 896(t1)<br>    |
| 524|[0x8001336c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x039 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000614c]:feq.h t6, ft11, ft10<br> [0x80006150]:csrrs a0, fcsr, zero<br> [0x80006154]:sw t6, 904(t1)<br>    |
| 525|[0x80013374]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000618c]:feq.h t6, ft11, ft10<br> [0x80006190]:csrrs a0, fcsr, zero<br> [0x80006194]:sw t6, 912(t1)<br>    |
| 526|[0x8001337c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800061cc]:feq.h t6, ft11, ft10<br> [0x800061d0]:csrrs a0, fcsr, zero<br> [0x800061d4]:sw t6, 920(t1)<br>    |
| 527|[0x80013384]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000620c]:feq.h t6, ft11, ft10<br> [0x80006210]:csrrs a0, fcsr, zero<br> [0x80006214]:sw t6, 928(t1)<br>    |
| 528|[0x8001338c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000624c]:feq.h t6, ft11, ft10<br> [0x80006250]:csrrs a0, fcsr, zero<br> [0x80006254]:sw t6, 936(t1)<br>    |
| 529|[0x80013394]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000628c]:feq.h t6, ft11, ft10<br> [0x80006290]:csrrs a0, fcsr, zero<br> [0x80006294]:sw t6, 944(t1)<br>    |
| 530|[0x8001339c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800062cc]:feq.h t6, ft11, ft10<br> [0x800062d0]:csrrs a0, fcsr, zero<br> [0x800062d4]:sw t6, 952(t1)<br>    |
| 531|[0x800133a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000630c]:feq.h t6, ft11, ft10<br> [0x80006310]:csrrs a0, fcsr, zero<br> [0x80006314]:sw t6, 960(t1)<br>    |
| 532|[0x800133ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000634c]:feq.h t6, ft11, ft10<br> [0x80006350]:csrrs a0, fcsr, zero<br> [0x80006354]:sw t6, 968(t1)<br>    |
| 533|[0x800133b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000638c]:feq.h t6, ft11, ft10<br> [0x80006390]:csrrs a0, fcsr, zero<br> [0x80006394]:sw t6, 976(t1)<br>    |
| 534|[0x800133bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800063cc]:feq.h t6, ft11, ft10<br> [0x800063d0]:csrrs a0, fcsr, zero<br> [0x800063d4]:sw t6, 984(t1)<br>    |
| 535|[0x800133c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x23f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000640c]:feq.h t6, ft11, ft10<br> [0x80006410]:csrrs a0, fcsr, zero<br> [0x80006414]:sw t6, 992(t1)<br>    |
| 536|[0x800133cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x23f and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006444]:feq.h t6, ft11, ft10<br> [0x80006448]:csrrs a0, fcsr, zero<br> [0x8000644c]:sw t6, 1000(t1)<br>   |
| 537|[0x800133d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000647c]:feq.h t6, ft11, ft10<br> [0x80006480]:csrrs a0, fcsr, zero<br> [0x80006484]:sw t6, 1008(t1)<br>   |
| 538|[0x800133dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x10 and fm1 == 0x2dc and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800064b4]:feq.h t6, ft11, ft10<br> [0x800064b8]:csrrs a0, fcsr, zero<br> [0x800064bc]:sw t6, 1016(t1)<br>   |
| 539|[0x800133e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x2dc and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800064f4]:feq.h t6, ft11, ft10<br> [0x800064f8]:csrrs a0, fcsr, zero<br> [0x800064fc]:sw t6, 0(t1)<br>      |
| 540|[0x800133ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x02f and fs2 == 1 and fe2 == 0x10 and fm2 == 0x2dc and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000652c]:feq.h t6, ft11, ft10<br> [0x80006530]:csrrs a0, fcsr, zero<br> [0x80006534]:sw t6, 8(t1)<br>      |
| 541|[0x800133f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006564]:feq.h t6, ft11, ft10<br> [0x80006568]:csrrs a0, fcsr, zero<br> [0x8000656c]:sw t6, 16(t1)<br>     |
| 542|[0x800133fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000659c]:feq.h t6, ft11, ft10<br> [0x800065a0]:csrrs a0, fcsr, zero<br> [0x800065a4]:sw t6, 24(t1)<br>     |
| 543|[0x80013404]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800065d4]:feq.h t6, ft11, ft10<br> [0x800065d8]:csrrs a0, fcsr, zero<br> [0x800065dc]:sw t6, 32(t1)<br>     |
| 544|[0x8001340c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000660c]:feq.h t6, ft11, ft10<br> [0x80006610]:csrrs a0, fcsr, zero<br> [0x80006614]:sw t6, 40(t1)<br>     |
| 545|[0x80013414]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006644]:feq.h t6, ft11, ft10<br> [0x80006648]:csrrs a0, fcsr, zero<br> [0x8000664c]:sw t6, 48(t1)<br>     |
| 546|[0x8001341c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000667c]:feq.h t6, ft11, ft10<br> [0x80006680]:csrrs a0, fcsr, zero<br> [0x80006684]:sw t6, 56(t1)<br>     |
| 547|[0x80013424]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800066b4]:feq.h t6, ft11, ft10<br> [0x800066b8]:csrrs a0, fcsr, zero<br> [0x800066bc]:sw t6, 64(t1)<br>     |
| 548|[0x8001342c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800066ec]:feq.h t6, ft11, ft10<br> [0x800066f0]:csrrs a0, fcsr, zero<br> [0x800066f4]:sw t6, 72(t1)<br>     |
| 549|[0x80013434]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006724]:feq.h t6, ft11, ft10<br> [0x80006728]:csrrs a0, fcsr, zero<br> [0x8000672c]:sw t6, 80(t1)<br>     |
| 550|[0x8001343c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000675c]:feq.h t6, ft11, ft10<br> [0x80006760]:csrrs a0, fcsr, zero<br> [0x80006764]:sw t6, 88(t1)<br>     |
| 551|[0x80013444]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006794]:feq.h t6, ft11, ft10<br> [0x80006798]:csrrs a0, fcsr, zero<br> [0x8000679c]:sw t6, 96(t1)<br>     |
| 552|[0x8001344c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800067cc]:feq.h t6, ft11, ft10<br> [0x800067d0]:csrrs a0, fcsr, zero<br> [0x800067d4]:sw t6, 104(t1)<br>    |
| 553|[0x80013454]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006804]:feq.h t6, ft11, ft10<br> [0x80006808]:csrrs a0, fcsr, zero<br> [0x8000680c]:sw t6, 112(t1)<br>    |
| 554|[0x8001345c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000683c]:feq.h t6, ft11, ft10<br> [0x80006840]:csrrs a0, fcsr, zero<br> [0x80006844]:sw t6, 120(t1)<br>    |
| 555|[0x80013464]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006874]:feq.h t6, ft11, ft10<br> [0x80006878]:csrrs a0, fcsr, zero<br> [0x8000687c]:sw t6, 128(t1)<br>    |
| 556|[0x8001346c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800068ac]:feq.h t6, ft11, ft10<br> [0x800068b0]:csrrs a0, fcsr, zero<br> [0x800068b4]:sw t6, 136(t1)<br>    |
| 557|[0x80013474]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800068e4]:feq.h t6, ft11, ft10<br> [0x800068e8]:csrrs a0, fcsr, zero<br> [0x800068ec]:sw t6, 144(t1)<br>    |
| 558|[0x8001347c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000691c]:feq.h t6, ft11, ft10<br> [0x80006920]:csrrs a0, fcsr, zero<br> [0x80006924]:sw t6, 152(t1)<br>    |
| 559|[0x80013484]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006954]:feq.h t6, ft11, ft10<br> [0x80006958]:csrrs a0, fcsr, zero<br> [0x8000695c]:sw t6, 160(t1)<br>    |
| 560|[0x8001348c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000698c]:feq.h t6, ft11, ft10<br> [0x80006990]:csrrs a0, fcsr, zero<br> [0x80006994]:sw t6, 168(t1)<br>    |
| 561|[0x80013494]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800069c4]:feq.h t6, ft11, ft10<br> [0x800069c8]:csrrs a0, fcsr, zero<br> [0x800069cc]:sw t6, 176(t1)<br>    |
| 562|[0x8001349c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x1a and fm2 == 0x069 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800069fc]:feq.h t6, ft11, ft10<br> [0x80006a00]:csrrs a0, fcsr, zero<br> [0x80006a04]:sw t6, 184(t1)<br>    |
| 563|[0x800134a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1a and fm1 == 0x069 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006a34]:feq.h t6, ft11, ft10<br> [0x80006a38]:csrrs a0, fcsr, zero<br> [0x80006a3c]:sw t6, 192(t1)<br>    |
| 564|[0x800134ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006a6c]:feq.h t6, ft11, ft10<br> [0x80006a70]:csrrs a0, fcsr, zero<br> [0x80006a74]:sw t6, 200(t1)<br>    |
| 565|[0x800134b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006aa4]:feq.h t6, ft11, ft10<br> [0x80006aa8]:csrrs a0, fcsr, zero<br> [0x80006aac]:sw t6, 208(t1)<br>    |
| 566|[0x800134bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006adc]:feq.h t6, ft11, ft10<br> [0x80006ae0]:csrrs a0, fcsr, zero<br> [0x80006ae4]:sw t6, 216(t1)<br>    |
| 567|[0x800134c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x035 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006b14]:feq.h t6, ft11, ft10<br> [0x80006b18]:csrrs a0, fcsr, zero<br> [0x80006b1c]:sw t6, 224(t1)<br>    |
| 568|[0x800134cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x035 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006b4c]:feq.h t6, ft11, ft10<br> [0x80006b50]:csrrs a0, fcsr, zero<br> [0x80006b54]:sw t6, 232(t1)<br>    |
| 569|[0x800134d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006b84]:feq.h t6, ft11, ft10<br> [0x80006b88]:csrrs a0, fcsr, zero<br> [0x80006b8c]:sw t6, 240(t1)<br>    |
| 570|[0x800134dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006bbc]:feq.h t6, ft11, ft10<br> [0x80006bc0]:csrrs a0, fcsr, zero<br> [0x80006bc4]:sw t6, 248(t1)<br>    |
| 571|[0x800134e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006bf4]:feq.h t6, ft11, ft10<br> [0x80006bf8]:csrrs a0, fcsr, zero<br> [0x80006bfc]:sw t6, 256(t1)<br>    |
| 572|[0x800134ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x1b and fm2 == 0x1ed and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006c2c]:feq.h t6, ft11, ft10<br> [0x80006c30]:csrrs a0, fcsr, zero<br> [0x80006c34]:sw t6, 264(t1)<br>    |
| 573|[0x800134f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1b and fm1 == 0x1ed and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006c64]:feq.h t6, ft11, ft10<br> [0x80006c68]:csrrs a0, fcsr, zero<br> [0x80006c6c]:sw t6, 272(t1)<br>    |
| 574|[0x800134fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006c9c]:feq.h t6, ft11, ft10<br> [0x80006ca0]:csrrs a0, fcsr, zero<br> [0x80006ca4]:sw t6, 280(t1)<br>    |
| 575|[0x80013504]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006cd4]:feq.h t6, ft11, ft10<br> [0x80006cd8]:csrrs a0, fcsr, zero<br> [0x80006cdc]:sw t6, 288(t1)<br>    |
| 576|[0x8001350c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x1a and fm2 == 0x39d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006d0c]:feq.h t6, ft11, ft10<br> [0x80006d10]:csrrs a0, fcsr, zero<br> [0x80006d14]:sw t6, 296(t1)<br>    |
| 577|[0x80013514]<br>0x00000000|- fs1 == 0 and fe1 == 0x1a and fm1 == 0x39d and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006d44]:feq.h t6, ft11, ft10<br> [0x80006d48]:csrrs a0, fcsr, zero<br> [0x80006d4c]:sw t6, 304(t1)<br>    |
| 578|[0x8001351c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006d7c]:feq.h t6, ft11, ft10<br> [0x80006d80]:csrrs a0, fcsr, zero<br> [0x80006d84]:sw t6, 312(t1)<br>    |
| 579|[0x80013524]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006db4]:feq.h t6, ft11, ft10<br> [0x80006db8]:csrrs a0, fcsr, zero<br> [0x80006dbc]:sw t6, 320(t1)<br>    |
| 580|[0x8001352c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x1a and fm2 == 0x23c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006dec]:feq.h t6, ft11, ft10<br> [0x80006df0]:csrrs a0, fcsr, zero<br> [0x80006df4]:sw t6, 328(t1)<br>    |
| 581|[0x80013534]<br>0x00000000|- fs1 == 0 and fe1 == 0x1a and fm1 == 0x23c and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006e24]:feq.h t6, ft11, ft10<br> [0x80006e28]:csrrs a0, fcsr, zero<br> [0x80006e2c]:sw t6, 336(t1)<br>    |
| 582|[0x8001353c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006e5c]:feq.h t6, ft11, ft10<br> [0x80006e60]:csrrs a0, fcsr, zero<br> [0x80006e64]:sw t6, 344(t1)<br>    |
| 583|[0x80013544]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006e94]:feq.h t6, ft11, ft10<br> [0x80006e98]:csrrs a0, fcsr, zero<br> [0x80006e9c]:sw t6, 352(t1)<br>    |
| 584|[0x8001354c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x1a and fm2 == 0x0b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006ecc]:feq.h t6, ft11, ft10<br> [0x80006ed0]:csrrs a0, fcsr, zero<br> [0x80006ed4]:sw t6, 360(t1)<br>    |
| 585|[0x80013554]<br>0x00000000|- fs1 == 1 and fe1 == 0x1a and fm1 == 0x0b9 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006f04]:feq.h t6, ft11, ft10<br> [0x80006f08]:csrrs a0, fcsr, zero<br> [0x80006f0c]:sw t6, 368(t1)<br>    |
| 586|[0x8001355c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006f3c]:feq.h t6, ft11, ft10<br> [0x80006f40]:csrrs a0, fcsr, zero<br> [0x80006f44]:sw t6, 376(t1)<br>    |
| 587|[0x80013564]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006f74]:feq.h t6, ft11, ft10<br> [0x80006f78]:csrrs a0, fcsr, zero<br> [0x80006f7c]:sw t6, 384(t1)<br>    |
| 588|[0x8001356c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x091 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x0dd and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006fac]:feq.h t6, ft11, ft10<br> [0x80006fb0]:csrrs a0, fcsr, zero<br> [0x80006fb4]:sw t6, 392(t1)<br>    |
| 589|[0x80013574]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x0dd and fs2 == 1 and fe2 == 0x00 and fm2 == 0x091 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006fe4]:feq.h t6, ft11, ft10<br> [0x80006fe8]:csrrs a0, fcsr, zero<br> [0x80006fec]:sw t6, 400(t1)<br>    |
| 590|[0x8001357c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x091 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000701c]:feq.h t6, ft11, ft10<br> [0x80007020]:csrrs a0, fcsr, zero<br> [0x80007024]:sw t6, 408(t1)<br>    |
| 591|[0x80013584]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x091 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007054]:feq.h t6, ft11, ft10<br> [0x80007058]:csrrs a0, fcsr, zero<br> [0x8000705c]:sw t6, 416(t1)<br>    |
| 592|[0x8001358c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000708c]:feq.h t6, ft11, ft10<br> [0x80007090]:csrrs a0, fcsr, zero<br> [0x80007094]:sw t6, 424(t1)<br>    |
| 593|[0x80013594]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x1a and fm2 == 0x250 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800070c4]:feq.h t6, ft11, ft10<br> [0x800070c8]:csrrs a0, fcsr, zero<br> [0x800070cc]:sw t6, 432(t1)<br>    |
| 594|[0x8001359c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1a and fm1 == 0x250 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800070fc]:feq.h t6, ft11, ft10<br> [0x80007100]:csrrs a0, fcsr, zero<br> [0x80007104]:sw t6, 440(t1)<br>    |
| 595|[0x800135a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007134]:feq.h t6, ft11, ft10<br> [0x80007138]:csrrs a0, fcsr, zero<br> [0x8000713c]:sw t6, 448(t1)<br>    |
| 596|[0x800135ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000716c]:feq.h t6, ft11, ft10<br> [0x80007170]:csrrs a0, fcsr, zero<br> [0x80007174]:sw t6, 456(t1)<br>    |
| 597|[0x800135b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x1b and fm2 == 0x10f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800071a4]:feq.h t6, ft11, ft10<br> [0x800071a8]:csrrs a0, fcsr, zero<br> [0x800071ac]:sw t6, 464(t1)<br>    |
| 598|[0x800135bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1b and fm1 == 0x10f and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800071dc]:feq.h t6, ft11, ft10<br> [0x800071e0]:csrrs a0, fcsr, zero<br> [0x800071e4]:sw t6, 472(t1)<br>    |
| 599|[0x800135c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007214]:feq.h t6, ft11, ft10<br> [0x80007218]:csrrs a0, fcsr, zero<br> [0x8000721c]:sw t6, 480(t1)<br>    |
| 600|[0x800135cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000724c]:feq.h t6, ft11, ft10<br> [0x80007250]:csrrs a0, fcsr, zero<br> [0x80007254]:sw t6, 488(t1)<br>    |
| 601|[0x800135d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x19 and fm2 == 0x22e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007284]:feq.h t6, ft11, ft10<br> [0x80007288]:csrrs a0, fcsr, zero<br> [0x8000728c]:sw t6, 496(t1)<br>    |
| 602|[0x800135dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x19 and fm1 == 0x22e and fs2 == 1 and fe2 == 0x01 and fm2 == 0x1aa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800072bc]:feq.h t6, ft11, ft10<br> [0x800072c0]:csrrs a0, fcsr, zero<br> [0x800072c4]:sw t6, 504(t1)<br>    |
| 603|[0x800135e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x1aa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800072f4]:feq.h t6, ft11, ft10<br> [0x800072f8]:csrrs a0, fcsr, zero<br> [0x800072fc]:sw t6, 512(t1)<br>    |
| 604|[0x800135ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000732c]:feq.h t6, ft11, ft10<br> [0x80007330]:csrrs a0, fcsr, zero<br> [0x80007334]:sw t6, 520(t1)<br>    |
| 605|[0x800135f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x12 and fm1 == 0x052 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007364]:feq.h t6, ft11, ft10<br> [0x80007368]:csrrs a0, fcsr, zero<br> [0x8000736c]:sw t6, 528(t1)<br>    |
| 606|[0x800135fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x12 and fm2 == 0x052 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000739c]:feq.h t6, ft11, ft10<br> [0x800073a0]:csrrs a0, fcsr, zero<br> [0x800073a4]:sw t6, 536(t1)<br>    |
| 607|[0x80013604]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x038 and fs2 == 1 and fe2 == 0x12 and fm2 == 0x052 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800073d4]:feq.h t6, ft11, ft10<br> [0x800073d8]:csrrs a0, fcsr, zero<br> [0x800073dc]:sw t6, 544(t1)<br>    |
| 608|[0x8001360c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000740c]:feq.h t6, ft11, ft10<br> [0x80007410]:csrrs a0, fcsr, zero<br> [0x80007414]:sw t6, 552(t1)<br>    |
| 609|[0x80013614]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007444]:feq.h t6, ft11, ft10<br> [0x80007448]:csrrs a0, fcsr, zero<br> [0x8000744c]:sw t6, 560(t1)<br>    |
| 610|[0x8001361c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1d and fm2 == 0x184 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000747c]:feq.h t6, ft11, ft10<br> [0x80007480]:csrrs a0, fcsr, zero<br> [0x80007484]:sw t6, 568(t1)<br>    |
| 611|[0x80013624]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800074b4]:feq.h t6, ft11, ft10<br> [0x800074b8]:csrrs a0, fcsr, zero<br> [0x800074bc]:sw t6, 576(t1)<br>    |
| 612|[0x8001362c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800074ec]:feq.h t6, ft11, ft10<br> [0x800074f0]:csrrs a0, fcsr, zero<br> [0x800074f4]:sw t6, 584(t1)<br>    |
| 613|[0x80013634]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007524]:feq.h t6, ft11, ft10<br> [0x80007528]:csrrs a0, fcsr, zero<br> [0x8000752c]:sw t6, 592(t1)<br>    |
| 614|[0x8001363c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000755c]:feq.h t6, ft11, ft10<br> [0x80007560]:csrrs a0, fcsr, zero<br> [0x80007564]:sw t6, 600(t1)<br>    |
| 615|[0x80013644]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007594]:feq.h t6, ft11, ft10<br> [0x80007598]:csrrs a0, fcsr, zero<br> [0x8000759c]:sw t6, 608(t1)<br>    |
| 616|[0x8001364c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800075cc]:feq.h t6, ft11, ft10<br> [0x800075d0]:csrrs a0, fcsr, zero<br> [0x800075d4]:sw t6, 616(t1)<br>    |
| 617|[0x80013654]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007604]:feq.h t6, ft11, ft10<br> [0x80007608]:csrrs a0, fcsr, zero<br> [0x8000760c]:sw t6, 624(t1)<br>    |
| 618|[0x8001365c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000763c]:feq.h t6, ft11, ft10<br> [0x80007640]:csrrs a0, fcsr, zero<br> [0x80007644]:sw t6, 632(t1)<br>    |
| 619|[0x80013664]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007674]:feq.h t6, ft11, ft10<br> [0x80007678]:csrrs a0, fcsr, zero<br> [0x8000767c]:sw t6, 640(t1)<br>    |
| 620|[0x8001366c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800076ac]:feq.h t6, ft11, ft10<br> [0x800076b0]:csrrs a0, fcsr, zero<br> [0x800076b4]:sw t6, 648(t1)<br>    |
| 621|[0x80013674]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800076e4]:feq.h t6, ft11, ft10<br> [0x800076e8]:csrrs a0, fcsr, zero<br> [0x800076ec]:sw t6, 656(t1)<br>    |
| 622|[0x8001367c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000771c]:feq.h t6, ft11, ft10<br> [0x80007720]:csrrs a0, fcsr, zero<br> [0x80007724]:sw t6, 664(t1)<br>    |
| 623|[0x80013684]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007754]:feq.h t6, ft11, ft10<br> [0x80007758]:csrrs a0, fcsr, zero<br> [0x8000775c]:sw t6, 672(t1)<br>    |
| 624|[0x8001368c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000778c]:feq.h t6, ft11, ft10<br> [0x80007790]:csrrs a0, fcsr, zero<br> [0x80007794]:sw t6, 680(t1)<br>    |
| 625|[0x80013694]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800077c4]:feq.h t6, ft11, ft10<br> [0x800077c8]:csrrs a0, fcsr, zero<br> [0x800077cc]:sw t6, 688(t1)<br>    |
| 626|[0x8001369c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800077fc]:feq.h t6, ft11, ft10<br> [0x80007800]:csrrs a0, fcsr, zero<br> [0x80007804]:sw t6, 696(t1)<br>    |
| 627|[0x800136a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x184 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007834]:feq.h t6, ft11, ft10<br> [0x80007838]:csrrs a0, fcsr, zero<br> [0x8000783c]:sw t6, 704(t1)<br>    |
| 628|[0x800136ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000786c]:feq.h t6, ft11, ft10<br> [0x80007870]:csrrs a0, fcsr, zero<br> [0x80007874]:sw t6, 712(t1)<br>    |
| 629|[0x800136b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1a and fm1 == 0x069 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800078a4]:feq.h t6, ft11, ft10<br> [0x800078a8]:csrrs a0, fcsr, zero<br> [0x800078ac]:sw t6, 720(t1)<br>    |
| 630|[0x800136bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x1a and fm2 == 0x069 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800078dc]:feq.h t6, ft11, ft10<br> [0x800078e0]:csrrs a0, fcsr, zero<br> [0x800078e4]:sw t6, 728(t1)<br>    |
| 631|[0x800136c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007914]:feq.h t6, ft11, ft10<br> [0x80007918]:csrrs a0, fcsr, zero<br> [0x8000791c]:sw t6, 736(t1)<br>    |
| 632|[0x800136cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x003 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000794c]:feq.h t6, ft11, ft10<br> [0x80007950]:csrrs a0, fcsr, zero<br> [0x80007954]:sw t6, 744(t1)<br>    |
| 633|[0x800136d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x003 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007984]:feq.h t6, ft11, ft10<br> [0x80007988]:csrrs a0, fcsr, zero<br> [0x8000798c]:sw t6, 752(t1)<br>    |
| 634|[0x800136dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x003 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800079bc]:feq.h t6, ft11, ft10<br> [0x800079c0]:csrrs a0, fcsr, zero<br> [0x800079c4]:sw t6, 760(t1)<br>    |
| 635|[0x800136e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x003 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800079f4]:feq.h t6, ft11, ft10<br> [0x800079f8]:csrrs a0, fcsr, zero<br> [0x800079fc]:sw t6, 768(t1)<br>    |
| 636|[0x800136ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007a2c]:feq.h t6, ft11, ft10<br> [0x80007a30]:csrrs a0, fcsr, zero<br> [0x80007a34]:sw t6, 776(t1)<br>    |
| 637|[0x800136f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007a64]:feq.h t6, ft11, ft10<br> [0x80007a68]:csrrs a0, fcsr, zero<br> [0x80007a6c]:sw t6, 784(t1)<br>    |
| 638|[0x800136fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007a9c]:feq.h t6, ft11, ft10<br> [0x80007aa0]:csrrs a0, fcsr, zero<br> [0x80007aa4]:sw t6, 792(t1)<br>    |
| 639|[0x80013704]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007ad4]:feq.h t6, ft11, ft10<br> [0x80007ad8]:csrrs a0, fcsr, zero<br> [0x80007adc]:sw t6, 800(t1)<br>    |
| 640|[0x8001370c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007b0c]:feq.h t6, ft11, ft10<br> [0x80007b10]:csrrs a0, fcsr, zero<br> [0x80007b14]:sw t6, 808(t1)<br>    |
| 641|[0x80013714]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007b44]:feq.h t6, ft11, ft10<br> [0x80007b48]:csrrs a0, fcsr, zero<br> [0x80007b4c]:sw t6, 816(t1)<br>    |
| 642|[0x8001371c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007b7c]:feq.h t6, ft11, ft10<br> [0x80007b80]:csrrs a0, fcsr, zero<br> [0x80007b84]:sw t6, 824(t1)<br>    |
| 643|[0x80013724]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007bb4]:feq.h t6, ft11, ft10<br> [0x80007bb8]:csrrs a0, fcsr, zero<br> [0x80007bbc]:sw t6, 832(t1)<br>    |
| 644|[0x8001372c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007bec]:feq.h t6, ft11, ft10<br> [0x80007bf0]:csrrs a0, fcsr, zero<br> [0x80007bf4]:sw t6, 840(t1)<br>    |
| 645|[0x80013734]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x025 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007c24]:feq.h t6, ft11, ft10<br> [0x80007c28]:csrrs a0, fcsr, zero<br> [0x80007c2c]:sw t6, 848(t1)<br>    |
| 646|[0x8001373c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007c5c]:feq.h t6, ft11, ft10<br> [0x80007c60]:csrrs a0, fcsr, zero<br> [0x80007c64]:sw t6, 856(t1)<br>    |
| 647|[0x80013744]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x025 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007c94]:feq.h t6, ft11, ft10<br> [0x80007c98]:csrrs a0, fcsr, zero<br> [0x80007c9c]:sw t6, 864(t1)<br>    |
| 648|[0x8001374c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007ccc]:feq.h t6, ft11, ft10<br> [0x80007cd0]:csrrs a0, fcsr, zero<br> [0x80007cd4]:sw t6, 872(t1)<br>    |
| 649|[0x80013754]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007d04]:feq.h t6, ft11, ft10<br> [0x80007d08]:csrrs a0, fcsr, zero<br> [0x80007d0c]:sw t6, 880(t1)<br>    |
| 650|[0x8001375c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007d3c]:feq.h t6, ft11, ft10<br> [0x80007d40]:csrrs a0, fcsr, zero<br> [0x80007d44]:sw t6, 888(t1)<br>    |
| 651|[0x80013764]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007d74]:feq.h t6, ft11, ft10<br> [0x80007d78]:csrrs a0, fcsr, zero<br> [0x80007d7c]:sw t6, 896(t1)<br>    |
| 652|[0x8001376c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007dac]:feq.h t6, ft11, ft10<br> [0x80007db0]:csrrs a0, fcsr, zero<br> [0x80007db4]:sw t6, 904(t1)<br>    |
| 653|[0x80013774]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007de4]:feq.h t6, ft11, ft10<br> [0x80007de8]:csrrs a0, fcsr, zero<br> [0x80007dec]:sw t6, 912(t1)<br>    |
| 654|[0x8001377c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007e1c]:feq.h t6, ft11, ft10<br> [0x80007e20]:csrrs a0, fcsr, zero<br> [0x80007e24]:sw t6, 920(t1)<br>    |
| 655|[0x80013784]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007e54]:feq.h t6, ft11, ft10<br> [0x80007e58]:csrrs a0, fcsr, zero<br> [0x80007e5c]:sw t6, 928(t1)<br>    |
| 656|[0x8001378c]<br>0x00000000|- fs1 == 0 and fe1 == 0x10 and fm1 == 0x084 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007e8c]:feq.h t6, ft11, ft10<br> [0x80007e90]:csrrs a0, fcsr, zero<br> [0x80007e94]:sw t6, 936(t1)<br>    |
| 657|[0x80013794]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x10 and fm2 == 0x084 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007ec4]:feq.h t6, ft11, ft10<br> [0x80007ec8]:csrrs a0, fcsr, zero<br> [0x80007ecc]:sw t6, 944(t1)<br>    |
| 658|[0x8001379c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x17b and fs2 == 0 and fe2 == 0x10 and fm2 == 0x084 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007efc]:feq.h t6, ft11, ft10<br> [0x80007f00]:csrrs a0, fcsr, zero<br> [0x80007f04]:sw t6, 952(t1)<br>    |
| 659|[0x800137a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007f34]:feq.h t6, ft11, ft10<br> [0x80007f38]:csrrs a0, fcsr, zero<br> [0x80007f3c]:sw t6, 960(t1)<br>    |
| 660|[0x800137ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007f6c]:feq.h t6, ft11, ft10<br> [0x80007f70]:csrrs a0, fcsr, zero<br> [0x80007f74]:sw t6, 968(t1)<br>    |
| 661|[0x800137b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007fa4]:feq.h t6, ft11, ft10<br> [0x80007fa8]:csrrs a0, fcsr, zero<br> [0x80007fac]:sw t6, 976(t1)<br>    |
| 662|[0x800137bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80007fdc]:feq.h t6, ft11, ft10<br> [0x80007fe0]:csrrs a0, fcsr, zero<br> [0x80007fe4]:sw t6, 984(t1)<br>    |
| 663|[0x800137c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008014]:feq.h t6, ft11, ft10<br> [0x80008018]:csrrs a0, fcsr, zero<br> [0x8000801c]:sw t6, 992(t1)<br>    |
| 664|[0x800137cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000804c]:feq.h t6, ft11, ft10<br> [0x80008050]:csrrs a0, fcsr, zero<br> [0x80008054]:sw t6, 1000(t1)<br>   |
| 665|[0x800137d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008084]:feq.h t6, ft11, ft10<br> [0x80008088]:csrrs a0, fcsr, zero<br> [0x8000808c]:sw t6, 1008(t1)<br>   |
| 666|[0x800137dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800080bc]:feq.h t6, ft11, ft10<br> [0x800080c0]:csrrs a0, fcsr, zero<br> [0x800080c4]:sw t6, 1016(t1)<br>   |
| 667|[0x800137e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800080fc]:feq.h t6, ft11, ft10<br> [0x80008100]:csrrs a0, fcsr, zero<br> [0x80008104]:sw t6, 0(t1)<br>      |
| 668|[0x800137ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008134]:feq.h t6, ft11, ft10<br> [0x80008138]:csrrs a0, fcsr, zero<br> [0x8000813c]:sw t6, 8(t1)<br>      |
| 669|[0x800137f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000816c]:feq.h t6, ft11, ft10<br> [0x80008170]:csrrs a0, fcsr, zero<br> [0x80008174]:sw t6, 16(t1)<br>     |
| 670|[0x800137fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800081a4]:feq.h t6, ft11, ft10<br> [0x800081a8]:csrrs a0, fcsr, zero<br> [0x800081ac]:sw t6, 24(t1)<br>     |
| 671|[0x80013804]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800081dc]:feq.h t6, ft11, ft10<br> [0x800081e0]:csrrs a0, fcsr, zero<br> [0x800081e4]:sw t6, 32(t1)<br>     |
| 672|[0x8001380c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008214]:feq.h t6, ft11, ft10<br> [0x80008218]:csrrs a0, fcsr, zero<br> [0x8000821c]:sw t6, 40(t1)<br>     |
| 673|[0x80013814]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000824c]:feq.h t6, ft11, ft10<br> [0x80008250]:csrrs a0, fcsr, zero<br> [0x80008254]:sw t6, 48(t1)<br>     |
| 674|[0x8001381c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008284]:feq.h t6, ft11, ft10<br> [0x80008288]:csrrs a0, fcsr, zero<br> [0x8000828c]:sw t6, 56(t1)<br>     |
| 675|[0x80013824]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800082bc]:feq.h t6, ft11, ft10<br> [0x800082c0]:csrrs a0, fcsr, zero<br> [0x800082c4]:sw t6, 64(t1)<br>     |
| 676|[0x8001382c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800082f4]:feq.h t6, ft11, ft10<br> [0x800082f8]:csrrs a0, fcsr, zero<br> [0x800082fc]:sw t6, 72(t1)<br>     |
| 677|[0x80013834]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000832c]:feq.h t6, ft11, ft10<br> [0x80008330]:csrrs a0, fcsr, zero<br> [0x80008334]:sw t6, 80(t1)<br>     |
| 678|[0x8001383c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008364]:feq.h t6, ft11, ft10<br> [0x80008368]:csrrs a0, fcsr, zero<br> [0x8000836c]:sw t6, 88(t1)<br>     |
| 679|[0x80013844]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000839c]:feq.h t6, ft11, ft10<br> [0x800083a0]:csrrs a0, fcsr, zero<br> [0x800083a4]:sw t6, 96(t1)<br>     |
| 680|[0x8001384c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x035 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800083d4]:feq.h t6, ft11, ft10<br> [0x800083d8]:csrrs a0, fcsr, zero<br> [0x800083dc]:sw t6, 104(t1)<br>    |
| 681|[0x80013854]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x035 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000840c]:feq.h t6, ft11, ft10<br> [0x80008410]:csrrs a0, fcsr, zero<br> [0x80008414]:sw t6, 112(t1)<br>    |
| 682|[0x8001385c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008444]:feq.h t6, ft11, ft10<br> [0x80008448]:csrrs a0, fcsr, zero<br> [0x8000844c]:sw t6, 120(t1)<br>    |
| 683|[0x80013864]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000847c]:feq.h t6, ft11, ft10<br> [0x80008480]:csrrs a0, fcsr, zero<br> [0x80008484]:sw t6, 128(t1)<br>    |
| 684|[0x8001386c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800084b4]:feq.h t6, ft11, ft10<br> [0x800084b8]:csrrs a0, fcsr, zero<br> [0x800084bc]:sw t6, 136(t1)<br>    |
| 685|[0x80013874]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800084ec]:feq.h t6, ft11, ft10<br> [0x800084f0]:csrrs a0, fcsr, zero<br> [0x800084f4]:sw t6, 144(t1)<br>    |
| 686|[0x8001387c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008524]:feq.h t6, ft11, ft10<br> [0x80008528]:csrrs a0, fcsr, zero<br> [0x8000852c]:sw t6, 152(t1)<br>    |
| 687|[0x80013884]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00a and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000855c]:feq.h t6, ft11, ft10<br> [0x80008560]:csrrs a0, fcsr, zero<br> [0x80008564]:sw t6, 160(t1)<br>    |
| 688|[0x8001388c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008594]:feq.h t6, ft11, ft10<br> [0x80008598]:csrrs a0, fcsr, zero<br> [0x8000859c]:sw t6, 168(t1)<br>    |
| 689|[0x80013894]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800085cc]:feq.h t6, ft11, ft10<br> [0x800085d0]:csrrs a0, fcsr, zero<br> [0x800085d4]:sw t6, 176(t1)<br>    |
| 690|[0x8001389c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008604]:feq.h t6, ft11, ft10<br> [0x80008608]:csrrs a0, fcsr, zero<br> [0x8000860c]:sw t6, 184(t1)<br>    |
| 691|[0x800138a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x006 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000863c]:feq.h t6, ft11, ft10<br> [0x80008640]:csrrs a0, fcsr, zero<br> [0x80008644]:sw t6, 192(t1)<br>    |
| 692|[0x800138ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008674]:feq.h t6, ft11, ft10<br> [0x80008678]:csrrs a0, fcsr, zero<br> [0x8000867c]:sw t6, 200(t1)<br>    |
| 693|[0x800138b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800086ac]:feq.h t6, ft11, ft10<br> [0x800086b0]:csrrs a0, fcsr, zero<br> [0x800086b4]:sw t6, 208(t1)<br>    |
| 694|[0x800138bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800086e4]:feq.h t6, ft11, ft10<br> [0x800086e8]:csrrs a0, fcsr, zero<br> [0x800086ec]:sw t6, 216(t1)<br>    |
| 695|[0x800138c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000871c]:feq.h t6, ft11, ft10<br> [0x80008720]:csrrs a0, fcsr, zero<br> [0x80008724]:sw t6, 224(t1)<br>    |
| 696|[0x800138cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008754]:feq.h t6, ft11, ft10<br> [0x80008758]:csrrs a0, fcsr, zero<br> [0x8000875c]:sw t6, 232(t1)<br>    |
| 697|[0x800138d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000878c]:feq.h t6, ft11, ft10<br> [0x80008790]:csrrs a0, fcsr, zero<br> [0x80008794]:sw t6, 240(t1)<br>    |
| 698|[0x800138dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x004 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800087c4]:feq.h t6, ft11, ft10<br> [0x800087c8]:csrrs a0, fcsr, zero<br> [0x800087cc]:sw t6, 248(t1)<br>    |
| 699|[0x800138e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x004 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800087fc]:feq.h t6, ft11, ft10<br> [0x80008800]:csrrs a0, fcsr, zero<br> [0x80008804]:sw t6, 256(t1)<br>    |
| 700|[0x800138ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008834]:feq.h t6, ft11, ft10<br> [0x80008838]:csrrs a0, fcsr, zero<br> [0x8000883c]:sw t6, 264(t1)<br>    |
| 701|[0x800138f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000886c]:feq.h t6, ft11, ft10<br> [0x80008870]:csrrs a0, fcsr, zero<br> [0x80008874]:sw t6, 272(t1)<br>    |
| 702|[0x800138fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x090 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x010 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800088a4]:feq.h t6, ft11, ft10<br> [0x800088a8]:csrrs a0, fcsr, zero<br> [0x800088ac]:sw t6, 280(t1)<br>    |
| 703|[0x80013904]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x010 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x090 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800088dc]:feq.h t6, ft11, ft10<br> [0x800088e0]:csrrs a0, fcsr, zero<br> [0x800088e4]:sw t6, 288(t1)<br>    |
| 704|[0x8001390c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x090 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008914]:feq.h t6, ft11, ft10<br> [0x80008918]:csrrs a0, fcsr, zero<br> [0x8000891c]:sw t6, 296(t1)<br>    |
| 705|[0x80013914]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x090 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000894c]:feq.h t6, ft11, ft10<br> [0x80008950]:csrrs a0, fcsr, zero<br> [0x80008954]:sw t6, 304(t1)<br>    |
| 706|[0x8001391c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008984]:feq.h t6, ft11, ft10<br> [0x80008988]:csrrs a0, fcsr, zero<br> [0x8000898c]:sw t6, 312(t1)<br>    |
| 707|[0x80013924]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800089bc]:feq.h t6, ft11, ft10<br> [0x800089c0]:csrrs a0, fcsr, zero<br> [0x800089c4]:sw t6, 320(t1)<br>    |
| 708|[0x8001392c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800089f4]:feq.h t6, ft11, ft10<br> [0x800089f8]:csrrs a0, fcsr, zero<br> [0x800089fc]:sw t6, 328(t1)<br>    |
| 709|[0x80013934]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008a2c]:feq.h t6, ft11, ft10<br> [0x80008a30]:csrrs a0, fcsr, zero<br> [0x80008a34]:sw t6, 336(t1)<br>    |
| 710|[0x8001393c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008a64]:feq.h t6, ft11, ft10<br> [0x80008a68]:csrrs a0, fcsr, zero<br> [0x80008a6c]:sw t6, 344(t1)<br>    |
| 711|[0x80013944]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x008 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008a9c]:feq.h t6, ft11, ft10<br> [0x80008aa0]:csrrs a0, fcsr, zero<br> [0x80008aa4]:sw t6, 352(t1)<br>    |
| 712|[0x8001394c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x008 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008ad4]:feq.h t6, ft11, ft10<br> [0x80008ad8]:csrrs a0, fcsr, zero<br> [0x80008adc]:sw t6, 360(t1)<br>    |
| 713|[0x80013954]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008b0c]:feq.h t6, ft11, ft10<br> [0x80008b10]:csrrs a0, fcsr, zero<br> [0x80008b14]:sw t6, 368(t1)<br>    |
| 714|[0x8001395c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008b44]:feq.h t6, ft11, ft10<br> [0x80008b48]:csrrs a0, fcsr, zero<br> [0x80008b4c]:sw t6, 376(t1)<br>    |
| 715|[0x80013964]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008b7c]:feq.h t6, ft11, ft10<br> [0x80008b80]:csrrs a0, fcsr, zero<br> [0x80008b84]:sw t6, 384(t1)<br>    |
| 716|[0x8001396c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x1a6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008bb4]:feq.h t6, ft11, ft10<br> [0x80008bb8]:csrrs a0, fcsr, zero<br> [0x80008bbc]:sw t6, 392(t1)<br>    |
| 717|[0x80013974]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x1a6 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008bec]:feq.h t6, ft11, ft10<br> [0x80008bf0]:csrrs a0, fcsr, zero<br> [0x80008bf4]:sw t6, 400(t1)<br>    |
| 718|[0x8001397c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008c24]:feq.h t6, ft11, ft10<br> [0x80008c28]:csrrs a0, fcsr, zero<br> [0x80008c2c]:sw t6, 408(t1)<br>    |
| 719|[0x80013984]<br>0x00000000|- fs1 == 0 and fe1 == 0x12 and fm1 == 0x04f and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008c5c]:feq.h t6, ft11, ft10<br> [0x80008c60]:csrrs a0, fcsr, zero<br> [0x80008c64]:sw t6, 416(t1)<br>    |
| 720|[0x8001398c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x12 and fm2 == 0x04f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008c94]:feq.h t6, ft11, ft10<br> [0x80008c98]:csrrs a0, fcsr, zero<br> [0x80008c9c]:sw t6, 424(t1)<br>    |
| 721|[0x80013994]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00e and fs2 == 0 and fe2 == 0x12 and fm2 == 0x04f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008ccc]:feq.h t6, ft11, ft10<br> [0x80008cd0]:csrrs a0, fcsr, zero<br> [0x80008cd4]:sw t6, 432(t1)<br>    |
| 722|[0x8001399c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008d04]:feq.h t6, ft11, ft10<br> [0x80008d08]:csrrs a0, fcsr, zero<br> [0x80008d0c]:sw t6, 440(t1)<br>    |
| 723|[0x800139a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008d3c]:feq.h t6, ft11, ft10<br> [0x80008d40]:csrrs a0, fcsr, zero<br> [0x80008d44]:sw t6, 448(t1)<br>    |
| 724|[0x800139ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1e and fm2 == 0x369 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008d74]:feq.h t6, ft11, ft10<br> [0x80008d78]:csrrs a0, fcsr, zero<br> [0x80008d7c]:sw t6, 456(t1)<br>    |
| 725|[0x800139b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008dac]:feq.h t6, ft11, ft10<br> [0x80008db0]:csrrs a0, fcsr, zero<br> [0x80008db4]:sw t6, 464(t1)<br>    |
| 726|[0x800139bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008de4]:feq.h t6, ft11, ft10<br> [0x80008de8]:csrrs a0, fcsr, zero<br> [0x80008dec]:sw t6, 472(t1)<br>    |
| 727|[0x800139c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008e1c]:feq.h t6, ft11, ft10<br> [0x80008e20]:csrrs a0, fcsr, zero<br> [0x80008e24]:sw t6, 480(t1)<br>    |
| 728|[0x800139cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008e54]:feq.h t6, ft11, ft10<br> [0x80008e58]:csrrs a0, fcsr, zero<br> [0x80008e5c]:sw t6, 488(t1)<br>    |
| 729|[0x800139d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008e8c]:feq.h t6, ft11, ft10<br> [0x80008e90]:csrrs a0, fcsr, zero<br> [0x80008e94]:sw t6, 496(t1)<br>    |
| 730|[0x800139dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008ec4]:feq.h t6, ft11, ft10<br> [0x80008ec8]:csrrs a0, fcsr, zero<br> [0x80008ecc]:sw t6, 504(t1)<br>    |
| 731|[0x800139e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008efc]:feq.h t6, ft11, ft10<br> [0x80008f00]:csrrs a0, fcsr, zero<br> [0x80008f04]:sw t6, 512(t1)<br>    |
| 732|[0x800139ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008f34]:feq.h t6, ft11, ft10<br> [0x80008f38]:csrrs a0, fcsr, zero<br> [0x80008f3c]:sw t6, 520(t1)<br>    |
| 733|[0x800139f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008f6c]:feq.h t6, ft11, ft10<br> [0x80008f70]:csrrs a0, fcsr, zero<br> [0x80008f74]:sw t6, 528(t1)<br>    |
| 734|[0x800139fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008fa4]:feq.h t6, ft11, ft10<br> [0x80008fa8]:csrrs a0, fcsr, zero<br> [0x80008fac]:sw t6, 536(t1)<br>    |
| 735|[0x80013a04]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80008fdc]:feq.h t6, ft11, ft10<br> [0x80008fe0]:csrrs a0, fcsr, zero<br> [0x80008fe4]:sw t6, 544(t1)<br>    |
| 736|[0x80013a0c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009014]:feq.h t6, ft11, ft10<br> [0x80009018]:csrrs a0, fcsr, zero<br> [0x8000901c]:sw t6, 552(t1)<br>    |
| 737|[0x80013a14]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000904c]:feq.h t6, ft11, ft10<br> [0x80009050]:csrrs a0, fcsr, zero<br> [0x80009054]:sw t6, 560(t1)<br>    |
| 738|[0x80013a1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009084]:feq.h t6, ft11, ft10<br> [0x80009088]:csrrs a0, fcsr, zero<br> [0x8000908c]:sw t6, 568(t1)<br>    |
| 739|[0x80013a24]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800090bc]:feq.h t6, ft11, ft10<br> [0x800090c0]:csrrs a0, fcsr, zero<br> [0x800090c4]:sw t6, 576(t1)<br>    |
| 740|[0x80013a2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800090f4]:feq.h t6, ft11, ft10<br> [0x800090f8]:csrrs a0, fcsr, zero<br> [0x800090fc]:sw t6, 584(t1)<br>    |
| 741|[0x80013a34]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x369 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000912c]:feq.h t6, ft11, ft10<br> [0x80009130]:csrrs a0, fcsr, zero<br> [0x80009134]:sw t6, 592(t1)<br>    |
| 742|[0x80013a3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009164]:feq.h t6, ft11, ft10<br> [0x80009168]:csrrs a0, fcsr, zero<br> [0x8000916c]:sw t6, 600(t1)<br>    |
| 743|[0x80013a44]<br>0x00000000|- fs1 == 0 and fe1 == 0x1b and fm1 == 0x1ed and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000919c]:feq.h t6, ft11, ft10<br> [0x800091a0]:csrrs a0, fcsr, zero<br> [0x800091a4]:sw t6, 608(t1)<br>    |
| 744|[0x80013a4c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x1b and fm2 == 0x1ed and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800091d4]:feq.h t6, ft11, ft10<br> [0x800091d8]:csrrs a0, fcsr, zero<br> [0x800091dc]:sw t6, 616(t1)<br>    |
| 745|[0x80013a54]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000920c]:feq.h t6, ft11, ft10<br> [0x80009210]:csrrs a0, fcsr, zero<br> [0x80009214]:sw t6, 624(t1)<br>    |
| 746|[0x80013a5c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x00a and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009244]:feq.h t6, ft11, ft10<br> [0x80009248]:csrrs a0, fcsr, zero<br> [0x8000924c]:sw t6, 632(t1)<br>    |
| 747|[0x80013a64]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000927c]:feq.h t6, ft11, ft10<br> [0x80009280]:csrrs a0, fcsr, zero<br> [0x80009284]:sw t6, 640(t1)<br>    |
| 748|[0x80013a6c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800092b4]:feq.h t6, ft11, ft10<br> [0x800092b8]:csrrs a0, fcsr, zero<br> [0x800092bc]:sw t6, 648(t1)<br>    |
| 749|[0x80013a74]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800092ec]:feq.h t6, ft11, ft10<br> [0x800092f0]:csrrs a0, fcsr, zero<br> [0x800092f4]:sw t6, 656(t1)<br>    |
| 750|[0x80013a7c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009324]:feq.h t6, ft11, ft10<br> [0x80009328]:csrrs a0, fcsr, zero<br> [0x8000932c]:sw t6, 664(t1)<br>    |
| 751|[0x80013a84]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000935c]:feq.h t6, ft11, ft10<br> [0x80009360]:csrrs a0, fcsr, zero<br> [0x80009364]:sw t6, 672(t1)<br>    |
| 752|[0x80013a8c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009394]:feq.h t6, ft11, ft10<br> [0x80009398]:csrrs a0, fcsr, zero<br> [0x8000939c]:sw t6, 680(t1)<br>    |
| 753|[0x80013a94]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800093cc]:feq.h t6, ft11, ft10<br> [0x800093d0]:csrrs a0, fcsr, zero<br> [0x800093d4]:sw t6, 688(t1)<br>    |
| 754|[0x80013a9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009404]:feq.h t6, ft11, ft10<br> [0x80009408]:csrrs a0, fcsr, zero<br> [0x8000940c]:sw t6, 696(t1)<br>    |
| 755|[0x80013aa4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x065 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000943c]:feq.h t6, ft11, ft10<br> [0x80009440]:csrrs a0, fcsr, zero<br> [0x80009444]:sw t6, 704(t1)<br>    |
| 756|[0x80013aac]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x065 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009474]:feq.h t6, ft11, ft10<br> [0x80009478]:csrrs a0, fcsr, zero<br> [0x8000947c]:sw t6, 712(t1)<br>    |
| 757|[0x80013ab4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x065 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800094ac]:feq.h t6, ft11, ft10<br> [0x800094b0]:csrrs a0, fcsr, zero<br> [0x800094b4]:sw t6, 720(t1)<br>    |
| 758|[0x80013abc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x065 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800094e4]:feq.h t6, ft11, ft10<br> [0x800094e8]:csrrs a0, fcsr, zero<br> [0x800094ec]:sw t6, 728(t1)<br>    |
| 759|[0x80013ac4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000951c]:feq.h t6, ft11, ft10<br> [0x80009520]:csrrs a0, fcsr, zero<br> [0x80009524]:sw t6, 736(t1)<br>    |
| 760|[0x80013acc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009554]:feq.h t6, ft11, ft10<br> [0x80009558]:csrrs a0, fcsr, zero<br> [0x8000955c]:sw t6, 744(t1)<br>    |
| 761|[0x80013ad4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000958c]:feq.h t6, ft11, ft10<br> [0x80009590]:csrrs a0, fcsr, zero<br> [0x80009594]:sw t6, 752(t1)<br>    |
| 762|[0x80013adc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800095c4]:feq.h t6, ft11, ft10<br> [0x800095c8]:csrrs a0, fcsr, zero<br> [0x800095cc]:sw t6, 760(t1)<br>    |
| 763|[0x80013ae4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800095fc]:feq.h t6, ft11, ft10<br> [0x80009600]:csrrs a0, fcsr, zero<br> [0x80009604]:sw t6, 768(t1)<br>    |
| 764|[0x80013aec]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009634]:feq.h t6, ft11, ft10<br> [0x80009638]:csrrs a0, fcsr, zero<br> [0x8000963c]:sw t6, 776(t1)<br>    |
| 765|[0x80013af4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000966c]:feq.h t6, ft11, ft10<br> [0x80009670]:csrrs a0, fcsr, zero<br> [0x80009674]:sw t6, 784(t1)<br>    |
| 766|[0x80013afc]<br>0x00000000|- fs1 == 0 and fe1 == 0x11 and fm1 == 0x212 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800096a4]:feq.h t6, ft11, ft10<br> [0x800096a8]:csrrs a0, fcsr, zero<br> [0x800096ac]:sw t6, 792(t1)<br>    |
| 767|[0x80013b04]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x11 and fm2 == 0x212 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800096dc]:feq.h t6, ft11, ft10<br> [0x800096e0]:csrrs a0, fcsr, zero<br> [0x800096e4]:sw t6, 800(t1)<br>    |
| 768|[0x80013b0c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3fa and fs2 == 0 and fe2 == 0x11 and fm2 == 0x212 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009714]:feq.h t6, ft11, ft10<br> [0x80009718]:csrrs a0, fcsr, zero<br> [0x8000971c]:sw t6, 808(t1)<br>    |
| 769|[0x80013b14]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000974c]:feq.h t6, ft11, ft10<br> [0x80009750]:csrrs a0, fcsr, zero<br> [0x80009754]:sw t6, 816(t1)<br>    |
| 770|[0x80013b1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009784]:feq.h t6, ft11, ft10<br> [0x80009788]:csrrs a0, fcsr, zero<br> [0x8000978c]:sw t6, 824(t1)<br>    |
| 771|[0x80013b24]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x0c2 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800097bc]:feq.h t6, ft11, ft10<br> [0x800097c0]:csrrs a0, fcsr, zero<br> [0x800097c4]:sw t6, 832(t1)<br>    |
| 772|[0x80013b2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800097f4]:feq.h t6, ft11, ft10<br> [0x800097f8]:csrrs a0, fcsr, zero<br> [0x800097fc]:sw t6, 840(t1)<br>    |
| 773|[0x80013b34]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000982c]:feq.h t6, ft11, ft10<br> [0x80009830]:csrrs a0, fcsr, zero<br> [0x80009834]:sw t6, 848(t1)<br>    |
| 774|[0x80013b3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009864]:feq.h t6, ft11, ft10<br> [0x80009868]:csrrs a0, fcsr, zero<br> [0x8000986c]:sw t6, 856(t1)<br>    |
| 775|[0x80013b44]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000989c]:feq.h t6, ft11, ft10<br> [0x800098a0]:csrrs a0, fcsr, zero<br> [0x800098a4]:sw t6, 864(t1)<br>    |
| 776|[0x80013b4c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800098d4]:feq.h t6, ft11, ft10<br> [0x800098d8]:csrrs a0, fcsr, zero<br> [0x800098dc]:sw t6, 872(t1)<br>    |
| 777|[0x80013b54]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000990c]:feq.h t6, ft11, ft10<br> [0x80009910]:csrrs a0, fcsr, zero<br> [0x80009914]:sw t6, 880(t1)<br>    |
| 778|[0x80013b5c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009944]:feq.h t6, ft11, ft10<br> [0x80009948]:csrrs a0, fcsr, zero<br> [0x8000994c]:sw t6, 888(t1)<br>    |
| 779|[0x80013b64]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000997c]:feq.h t6, ft11, ft10<br> [0x80009980]:csrrs a0, fcsr, zero<br> [0x80009984]:sw t6, 896(t1)<br>    |
| 780|[0x80013b6c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800099b4]:feq.h t6, ft11, ft10<br> [0x800099b8]:csrrs a0, fcsr, zero<br> [0x800099bc]:sw t6, 904(t1)<br>    |
| 781|[0x80013b74]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800099ec]:feq.h t6, ft11, ft10<br> [0x800099f0]:csrrs a0, fcsr, zero<br> [0x800099f4]:sw t6, 912(t1)<br>    |
| 782|[0x80013b7c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009a24]:feq.h t6, ft11, ft10<br> [0x80009a28]:csrrs a0, fcsr, zero<br> [0x80009a2c]:sw t6, 920(t1)<br>    |
| 783|[0x80013b84]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009a5c]:feq.h t6, ft11, ft10<br> [0x80009a60]:csrrs a0, fcsr, zero<br> [0x80009a64]:sw t6, 928(t1)<br>    |
| 784|[0x80013b8c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009a94]:feq.h t6, ft11, ft10<br> [0x80009a98]:csrrs a0, fcsr, zero<br> [0x80009a9c]:sw t6, 936(t1)<br>    |
| 785|[0x80013b94]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009acc]:feq.h t6, ft11, ft10<br> [0x80009ad0]:csrrs a0, fcsr, zero<br> [0x80009ad4]:sw t6, 944(t1)<br>    |
| 786|[0x80013b9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009b04]:feq.h t6, ft11, ft10<br> [0x80009b08]:csrrs a0, fcsr, zero<br> [0x80009b0c]:sw t6, 952(t1)<br>    |
| 787|[0x80013ba4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009b3c]:feq.h t6, ft11, ft10<br> [0x80009b40]:csrrs a0, fcsr, zero<br> [0x80009b44]:sw t6, 960(t1)<br>    |
| 788|[0x80013bac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x0c2 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009b74]:feq.h t6, ft11, ft10<br> [0x80009b78]:csrrs a0, fcsr, zero<br> [0x80009b7c]:sw t6, 968(t1)<br>    |
| 789|[0x80013bb4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009bac]:feq.h t6, ft11, ft10<br> [0x80009bb0]:csrrs a0, fcsr, zero<br> [0x80009bb4]:sw t6, 976(t1)<br>    |
| 790|[0x80013bbc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1a and fm1 == 0x39d and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009be4]:feq.h t6, ft11, ft10<br> [0x80009be8]:csrrs a0, fcsr, zero<br> [0x80009bec]:sw t6, 984(t1)<br>    |
| 791|[0x80013bc4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x1a and fm2 == 0x39d and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009c1c]:feq.h t6, ft11, ft10<br> [0x80009c20]:csrrs a0, fcsr, zero<br> [0x80009c24]:sw t6, 992(t1)<br>    |
| 792|[0x80013bcc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009c5c]:feq.h t6, ft11, ft10<br> [0x80009c60]:csrrs a0, fcsr, zero<br> [0x80009c64]:sw t6, 1000(t1)<br>   |
| 793|[0x80013bd4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x006 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009c9c]:feq.h t6, ft11, ft10<br> [0x80009ca0]:csrrs a0, fcsr, zero<br> [0x80009ca4]:sw t6, 1008(t1)<br>   |
| 794|[0x80013bdc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009cdc]:feq.h t6, ft11, ft10<br> [0x80009ce0]:csrrs a0, fcsr, zero<br> [0x80009ce4]:sw t6, 1016(t1)<br>   |
| 795|[0x80013be4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009d24]:feq.h t6, ft11, ft10<br> [0x80009d28]:csrrs a0, fcsr, zero<br> [0x80009d2c]:sw t6, 0(t1)<br>      |
| 796|[0x80013bec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009d64]:feq.h t6, ft11, ft10<br> [0x80009d68]:csrrs a0, fcsr, zero<br> [0x80009d6c]:sw t6, 8(t1)<br>      |
| 797|[0x80013bf4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009da4]:feq.h t6, ft11, ft10<br> [0x80009da8]:csrrs a0, fcsr, zero<br> [0x80009dac]:sw t6, 16(t1)<br>     |
| 798|[0x80013bfc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009de4]:feq.h t6, ft11, ft10<br> [0x80009de8]:csrrs a0, fcsr, zero<br> [0x80009dec]:sw t6, 24(t1)<br>     |
| 799|[0x80013c04]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x041 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009e24]:feq.h t6, ft11, ft10<br> [0x80009e28]:csrrs a0, fcsr, zero<br> [0x80009e2c]:sw t6, 32(t1)<br>     |
| 800|[0x80013c0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x041 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009e64]:feq.h t6, ft11, ft10<br> [0x80009e68]:csrrs a0, fcsr, zero<br> [0x80009e6c]:sw t6, 40(t1)<br>     |
| 801|[0x80013c14]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x041 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009ea4]:feq.h t6, ft11, ft10<br> [0x80009ea8]:csrrs a0, fcsr, zero<br> [0x80009eac]:sw t6, 48(t1)<br>     |
| 802|[0x80013c1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x041 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009ee4]:feq.h t6, ft11, ft10<br> [0x80009ee8]:csrrs a0, fcsr, zero<br> [0x80009eec]:sw t6, 56(t1)<br>     |
| 803|[0x80013c24]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009f24]:feq.h t6, ft11, ft10<br> [0x80009f28]:csrrs a0, fcsr, zero<br> [0x80009f2c]:sw t6, 64(t1)<br>     |
| 804|[0x80013c2c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009f64]:feq.h t6, ft11, ft10<br> [0x80009f68]:csrrs a0, fcsr, zero<br> [0x80009f6c]:sw t6, 72(t1)<br>     |
| 805|[0x80013c34]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009fa4]:feq.h t6, ft11, ft10<br> [0x80009fa8]:csrrs a0, fcsr, zero<br> [0x80009fac]:sw t6, 80(t1)<br>     |
| 806|[0x80013c3c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80009fe4]:feq.h t6, ft11, ft10<br> [0x80009fe8]:csrrs a0, fcsr, zero<br> [0x80009fec]:sw t6, 88(t1)<br>     |
| 807|[0x80013c44]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a024]:feq.h t6, ft11, ft10<br> [0x8000a028]:csrrs a0, fcsr, zero<br> [0x8000a02c]:sw t6, 96(t1)<br>     |
| 808|[0x80013c4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a064]:feq.h t6, ft11, ft10<br> [0x8000a068]:csrrs a0, fcsr, zero<br> [0x8000a06c]:sw t6, 104(t1)<br>    |
| 809|[0x80013c54]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a0a4]:feq.h t6, ft11, ft10<br> [0x8000a0a8]:csrrs a0, fcsr, zero<br> [0x8000a0ac]:sw t6, 112(t1)<br>    |
| 810|[0x80013c5c]<br>0x00000000|- fs1 == 0 and fe1 == 0x10 and fm1 == 0x3cc and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a0e4]:feq.h t6, ft11, ft10<br> [0x8000a0e8]:csrrs a0, fcsr, zero<br> [0x8000a0ec]:sw t6, 120(t1)<br>    |
| 811|[0x80013c64]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x10 and fm2 == 0x3cc and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a124]:feq.h t6, ft11, ft10<br> [0x8000a128]:csrrs a0, fcsr, zero<br> [0x8000a12c]:sw t6, 128(t1)<br>    |
| 812|[0x80013c6c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x28e and fs2 == 0 and fe2 == 0x10 and fm2 == 0x3cc and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a164]:feq.h t6, ft11, ft10<br> [0x8000a168]:csrrs a0, fcsr, zero<br> [0x8000a16c]:sw t6, 136(t1)<br>    |
| 813|[0x80013c74]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a1a4]:feq.h t6, ft11, ft10<br> [0x8000a1a8]:csrrs a0, fcsr, zero<br> [0x8000a1ac]:sw t6, 144(t1)<br>    |
| 814|[0x80013c7c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a1e4]:feq.h t6, ft11, ft10<br> [0x8000a1e8]:csrrs a0, fcsr, zero<br> [0x8000a1ec]:sw t6, 152(t1)<br>    |
| 815|[0x80013c84]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x3cb and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a224]:feq.h t6, ft11, ft10<br> [0x8000a228]:csrrs a0, fcsr, zero<br> [0x8000a22c]:sw t6, 160(t1)<br>    |
| 816|[0x80013c8c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a264]:feq.h t6, ft11, ft10<br> [0x8000a268]:csrrs a0, fcsr, zero<br> [0x8000a26c]:sw t6, 168(t1)<br>    |
| 817|[0x80013c94]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a2a4]:feq.h t6, ft11, ft10<br> [0x8000a2a8]:csrrs a0, fcsr, zero<br> [0x8000a2ac]:sw t6, 176(t1)<br>    |
| 818|[0x80013c9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a2e4]:feq.h t6, ft11, ft10<br> [0x8000a2e8]:csrrs a0, fcsr, zero<br> [0x8000a2ec]:sw t6, 184(t1)<br>    |
| 819|[0x80013ca4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a324]:feq.h t6, ft11, ft10<br> [0x8000a328]:csrrs a0, fcsr, zero<br> [0x8000a32c]:sw t6, 192(t1)<br>    |
| 820|[0x80013cac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a364]:feq.h t6, ft11, ft10<br> [0x8000a368]:csrrs a0, fcsr, zero<br> [0x8000a36c]:sw t6, 200(t1)<br>    |
| 821|[0x80013cb4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a3a4]:feq.h t6, ft11, ft10<br> [0x8000a3a8]:csrrs a0, fcsr, zero<br> [0x8000a3ac]:sw t6, 208(t1)<br>    |
| 822|[0x80013cbc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a3e4]:feq.h t6, ft11, ft10<br> [0x8000a3e8]:csrrs a0, fcsr, zero<br> [0x8000a3ec]:sw t6, 216(t1)<br>    |
| 823|[0x80013cc4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a424]:feq.h t6, ft11, ft10<br> [0x8000a428]:csrrs a0, fcsr, zero<br> [0x8000a42c]:sw t6, 224(t1)<br>    |
| 824|[0x80013ccc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a464]:feq.h t6, ft11, ft10<br> [0x8000a468]:csrrs a0, fcsr, zero<br> [0x8000a46c]:sw t6, 232(t1)<br>    |
| 825|[0x80013cd4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a4a4]:feq.h t6, ft11, ft10<br> [0x8000a4a8]:csrrs a0, fcsr, zero<br> [0x8000a4ac]:sw t6, 240(t1)<br>    |
| 826|[0x80013cdc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a4e4]:feq.h t6, ft11, ft10<br> [0x8000a4e8]:csrrs a0, fcsr, zero<br> [0x8000a4ec]:sw t6, 248(t1)<br>    |
| 827|[0x80013ce4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a524]:feq.h t6, ft11, ft10<br> [0x8000a528]:csrrs a0, fcsr, zero<br> [0x8000a52c]:sw t6, 256(t1)<br>    |
| 828|[0x80013cec]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a564]:feq.h t6, ft11, ft10<br> [0x8000a568]:csrrs a0, fcsr, zero<br> [0x8000a56c]:sw t6, 264(t1)<br>    |
| 829|[0x80013cf4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a5a4]:feq.h t6, ft11, ft10<br> [0x8000a5a8]:csrrs a0, fcsr, zero<br> [0x8000a5ac]:sw t6, 272(t1)<br>    |
| 830|[0x80013cfc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a5e4]:feq.h t6, ft11, ft10<br> [0x8000a5e8]:csrrs a0, fcsr, zero<br> [0x8000a5ec]:sw t6, 280(t1)<br>    |
| 831|[0x80013d04]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a624]:feq.h t6, ft11, ft10<br> [0x8000a628]:csrrs a0, fcsr, zero<br> [0x8000a62c]:sw t6, 288(t1)<br>    |
| 832|[0x80013d0c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1d and fm1 == 0x3cb and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a664]:feq.h t6, ft11, ft10<br> [0x8000a668]:csrrs a0, fcsr, zero<br> [0x8000a66c]:sw t6, 296(t1)<br>    |
| 833|[0x80013d14]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a6a4]:feq.h t6, ft11, ft10<br> [0x8000a6a8]:csrrs a0, fcsr, zero<br> [0x8000a6ac]:sw t6, 304(t1)<br>    |
| 834|[0x80013d1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1a and fm1 == 0x23c and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a6e4]:feq.h t6, ft11, ft10<br> [0x8000a6e8]:csrrs a0, fcsr, zero<br> [0x8000a6ec]:sw t6, 312(t1)<br>    |
| 835|[0x80013d24]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x1a and fm2 == 0x23c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a724]:feq.h t6, ft11, ft10<br> [0x8000a728]:csrrs a0, fcsr, zero<br> [0x8000a72c]:sw t6, 320(t1)<br>    |
| 836|[0x80013d2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a764]:feq.h t6, ft11, ft10<br> [0x8000a768]:csrrs a0, fcsr, zero<br> [0x8000a76c]:sw t6, 328(t1)<br>    |
| 837|[0x80013d34]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x005 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a7a4]:feq.h t6, ft11, ft10<br> [0x8000a7a8]:csrrs a0, fcsr, zero<br> [0x8000a7ac]:sw t6, 336(t1)<br>    |
| 838|[0x80013d3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a7e4]:feq.h t6, ft11, ft10<br> [0x8000a7e8]:csrrs a0, fcsr, zero<br> [0x8000a7ec]:sw t6, 344(t1)<br>    |
| 839|[0x80013d44]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a824]:feq.h t6, ft11, ft10<br> [0x8000a828]:csrrs a0, fcsr, zero<br> [0x8000a82c]:sw t6, 352(t1)<br>    |
| 840|[0x80013d4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a864]:feq.h t6, ft11, ft10<br> [0x8000a868]:csrrs a0, fcsr, zero<br> [0x8000a86c]:sw t6, 360(t1)<br>    |
| 841|[0x80013d54]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a8a4]:feq.h t6, ft11, ft10<br> [0x8000a8a8]:csrrs a0, fcsr, zero<br> [0x8000a8ac]:sw t6, 368(t1)<br>    |
| 842|[0x80013d5c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x035 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a8e4]:feq.h t6, ft11, ft10<br> [0x8000a8e8]:csrrs a0, fcsr, zero<br> [0x8000a8ec]:sw t6, 376(t1)<br>    |
| 843|[0x80013d64]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x035 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a924]:feq.h t6, ft11, ft10<br> [0x8000a928]:csrrs a0, fcsr, zero<br> [0x8000a92c]:sw t6, 384(t1)<br>    |
| 844|[0x80013d6c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x035 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a964]:feq.h t6, ft11, ft10<br> [0x8000a968]:csrrs a0, fcsr, zero<br> [0x8000a96c]:sw t6, 392(t1)<br>    |
| 845|[0x80013d74]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x035 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a9a4]:feq.h t6, ft11, ft10<br> [0x8000a9a8]:csrrs a0, fcsr, zero<br> [0x8000a9ac]:sw t6, 400(t1)<br>    |
| 846|[0x80013d7c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000a9e4]:feq.h t6, ft11, ft10<br> [0x8000a9e8]:csrrs a0, fcsr, zero<br> [0x8000a9ec]:sw t6, 408(t1)<br>    |
| 847|[0x80013d84]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000aa24]:feq.h t6, ft11, ft10<br> [0x8000aa28]:csrrs a0, fcsr, zero<br> [0x8000aa2c]:sw t6, 416(t1)<br>    |
| 848|[0x80013d8c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000aa64]:feq.h t6, ft11, ft10<br> [0x8000aa68]:csrrs a0, fcsr, zero<br> [0x8000aa6c]:sw t6, 424(t1)<br>    |
| 849|[0x80013d94]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000aaa4]:feq.h t6, ft11, ft10<br> [0x8000aaa8]:csrrs a0, fcsr, zero<br> [0x8000aaac]:sw t6, 432(t1)<br>    |
| 850|[0x80013d9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000aae4]:feq.h t6, ft11, ft10<br> [0x8000aae8]:csrrs a0, fcsr, zero<br> [0x8000aaec]:sw t6, 440(t1)<br>    |
| 851|[0x80013da4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ab24]:feq.h t6, ft11, ft10<br> [0x8000ab28]:csrrs a0, fcsr, zero<br> [0x8000ab2c]:sw t6, 448(t1)<br>    |
| 852|[0x80013dac]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ab64]:feq.h t6, ft11, ft10<br> [0x8000ab68]:csrrs a0, fcsr, zero<br> [0x8000ab6c]:sw t6, 456(t1)<br>    |
| 853|[0x80013db4]<br>0x00000000|- fs1 == 0 and fe1 == 0x10 and fm1 == 0x262 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000aba4]:feq.h t6, ft11, ft10<br> [0x8000aba8]:csrrs a0, fcsr, zero<br> [0x8000abac]:sw t6, 464(t1)<br>    |
| 854|[0x80013dbc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x10 and fm2 == 0x262 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000abe4]:feq.h t6, ft11, ft10<br> [0x8000abe8]:csrrs a0, fcsr, zero<br> [0x8000abec]:sw t6, 472(t1)<br>    |
| 855|[0x80013dc4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x217 and fs2 == 0 and fe2 == 0x10 and fm2 == 0x262 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ac24]:feq.h t6, ft11, ft10<br> [0x8000ac28]:csrrs a0, fcsr, zero<br> [0x8000ac2c]:sw t6, 480(t1)<br>    |
| 856|[0x80013dcc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ac64]:feq.h t6, ft11, ft10<br> [0x8000ac68]:csrrs a0, fcsr, zero<br> [0x8000ac6c]:sw t6, 488(t1)<br>    |
| 857|[0x80013dd4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000aca4]:feq.h t6, ft11, ft10<br> [0x8000aca8]:csrrs a0, fcsr, zero<br> [0x8000acac]:sw t6, 496(t1)<br>    |
| 858|[0x80013ddc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x1e7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ace4]:feq.h t6, ft11, ft10<br> [0x8000ace8]:csrrs a0, fcsr, zero<br> [0x8000acec]:sw t6, 504(t1)<br>    |
| 859|[0x80013de4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ad24]:feq.h t6, ft11, ft10<br> [0x8000ad28]:csrrs a0, fcsr, zero<br> [0x8000ad2c]:sw t6, 512(t1)<br>    |
| 860|[0x80013dec]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ad64]:feq.h t6, ft11, ft10<br> [0x8000ad68]:csrrs a0, fcsr, zero<br> [0x8000ad6c]:sw t6, 520(t1)<br>    |
| 861|[0x80013df4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ada4]:feq.h t6, ft11, ft10<br> [0x8000ada8]:csrrs a0, fcsr, zero<br> [0x8000adac]:sw t6, 528(t1)<br>    |
| 862|[0x80013dfc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ade4]:feq.h t6, ft11, ft10<br> [0x8000ade8]:csrrs a0, fcsr, zero<br> [0x8000adec]:sw t6, 536(t1)<br>    |
| 863|[0x80013e04]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ae24]:feq.h t6, ft11, ft10<br> [0x8000ae28]:csrrs a0, fcsr, zero<br> [0x8000ae2c]:sw t6, 544(t1)<br>    |
| 864|[0x80013e0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ae64]:feq.h t6, ft11, ft10<br> [0x8000ae68]:csrrs a0, fcsr, zero<br> [0x8000ae6c]:sw t6, 552(t1)<br>    |
| 865|[0x80013e14]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000aea4]:feq.h t6, ft11, ft10<br> [0x8000aea8]:csrrs a0, fcsr, zero<br> [0x8000aeac]:sw t6, 560(t1)<br>    |
| 866|[0x80013e1c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000aee4]:feq.h t6, ft11, ft10<br> [0x8000aee8]:csrrs a0, fcsr, zero<br> [0x8000aeec]:sw t6, 568(t1)<br>    |
| 867|[0x80013e24]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000af24]:feq.h t6, ft11, ft10<br> [0x8000af28]:csrrs a0, fcsr, zero<br> [0x8000af2c]:sw t6, 576(t1)<br>    |
| 868|[0x80013e2c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000af64]:feq.h t6, ft11, ft10<br> [0x8000af68]:csrrs a0, fcsr, zero<br> [0x8000af6c]:sw t6, 584(t1)<br>    |
| 869|[0x80013e34]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000afa4]:feq.h t6, ft11, ft10<br> [0x8000afa8]:csrrs a0, fcsr, zero<br> [0x8000afac]:sw t6, 592(t1)<br>    |
| 870|[0x80013e3c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000afe4]:feq.h t6, ft11, ft10<br> [0x8000afe8]:csrrs a0, fcsr, zero<br> [0x8000afec]:sw t6, 600(t1)<br>    |
| 871|[0x80013e44]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b024]:feq.h t6, ft11, ft10<br> [0x8000b028]:csrrs a0, fcsr, zero<br> [0x8000b02c]:sw t6, 608(t1)<br>    |
| 872|[0x80013e4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b064]:feq.h t6, ft11, ft10<br> [0x8000b068]:csrrs a0, fcsr, zero<br> [0x8000b06c]:sw t6, 616(t1)<br>    |
| 873|[0x80013e54]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b0a4]:feq.h t6, ft11, ft10<br> [0x8000b0a8]:csrrs a0, fcsr, zero<br> [0x8000b0ac]:sw t6, 624(t1)<br>    |
| 874|[0x80013e5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b0e4]:feq.h t6, ft11, ft10<br> [0x8000b0e8]:csrrs a0, fcsr, zero<br> [0x8000b0ec]:sw t6, 632(t1)<br>    |
| 875|[0x80013e64]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x1e7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b124]:feq.h t6, ft11, ft10<br> [0x8000b128]:csrrs a0, fcsr, zero<br> [0x8000b12c]:sw t6, 640(t1)<br>    |
| 876|[0x80013e6c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b164]:feq.h t6, ft11, ft10<br> [0x8000b168]:csrrs a0, fcsr, zero<br> [0x8000b16c]:sw t6, 648(t1)<br>    |
| 877|[0x80013e74]<br>0x00000000|- fs1 == 1 and fe1 == 0x1a and fm1 == 0x0b9 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b1a4]:feq.h t6, ft11, ft10<br> [0x8000b1a8]:csrrs a0, fcsr, zero<br> [0x8000b1ac]:sw t6, 656(t1)<br>    |
| 878|[0x80013e7c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x1a and fm2 == 0x0b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b1e4]:feq.h t6, ft11, ft10<br> [0x8000b1e8]:csrrs a0, fcsr, zero<br> [0x8000b1ec]:sw t6, 664(t1)<br>    |
| 879|[0x80013e84]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b224]:feq.h t6, ft11, ft10<br> [0x8000b228]:csrrs a0, fcsr, zero<br> [0x8000b22c]:sw t6, 672(t1)<br>    |
| 880|[0x80013e8c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x004 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b264]:feq.h t6, ft11, ft10<br> [0x8000b268]:csrrs a0, fcsr, zero<br> [0x8000b26c]:sw t6, 680(t1)<br>    |
| 881|[0x80013e94]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x004 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b2a4]:feq.h t6, ft11, ft10<br> [0x8000b2a8]:csrrs a0, fcsr, zero<br> [0x8000b2ac]:sw t6, 688(t1)<br>    |
| 882|[0x80013e9c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b2e4]:feq.h t6, ft11, ft10<br> [0x8000b2e8]:csrrs a0, fcsr, zero<br> [0x8000b2ec]:sw t6, 696(t1)<br>    |
| 883|[0x80013ea4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x028 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b324]:feq.h t6, ft11, ft10<br> [0x8000b328]:csrrs a0, fcsr, zero<br> [0x8000b32c]:sw t6, 704(t1)<br>    |
| 884|[0x80013eac]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x028 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b364]:feq.h t6, ft11, ft10<br> [0x8000b368]:csrrs a0, fcsr, zero<br> [0x8000b36c]:sw t6, 712(t1)<br>    |
| 885|[0x80013eb4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x028 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b3a4]:feq.h t6, ft11, ft10<br> [0x8000b3a8]:csrrs a0, fcsr, zero<br> [0x8000b3ac]:sw t6, 720(t1)<br>    |
| 886|[0x80013ebc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x028 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b3e4]:feq.h t6, ft11, ft10<br> [0x8000b3e8]:csrrs a0, fcsr, zero<br> [0x8000b3ec]:sw t6, 728(t1)<br>    |
| 887|[0x80013ec4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b424]:feq.h t6, ft11, ft10<br> [0x8000b428]:csrrs a0, fcsr, zero<br> [0x8000b42c]:sw t6, 736(t1)<br>    |
| 888|[0x80013ecc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b464]:feq.h t6, ft11, ft10<br> [0x8000b468]:csrrs a0, fcsr, zero<br> [0x8000b46c]:sw t6, 744(t1)<br>    |
| 889|[0x80013ed4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b4a4]:feq.h t6, ft11, ft10<br> [0x8000b4a8]:csrrs a0, fcsr, zero<br> [0x8000b4ac]:sw t6, 752(t1)<br>    |
| 890|[0x80013edc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b4e4]:feq.h t6, ft11, ft10<br> [0x8000b4e8]:csrrs a0, fcsr, zero<br> [0x8000b4ec]:sw t6, 760(t1)<br>    |
| 891|[0x80013ee4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b524]:feq.h t6, ft11, ft10<br> [0x8000b528]:csrrs a0, fcsr, zero<br> [0x8000b52c]:sw t6, 768(t1)<br>    |
| 892|[0x80013eec]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b564]:feq.h t6, ft11, ft10<br> [0x8000b568]:csrrs a0, fcsr, zero<br> [0x8000b56c]:sw t6, 776(t1)<br>    |
| 893|[0x80013ef4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b5a4]:feq.h t6, ft11, ft10<br> [0x8000b5a8]:csrrs a0, fcsr, zero<br> [0x8000b5ac]:sw t6, 784(t1)<br>    |
| 894|[0x80013efc]<br>0x00000000|- fs1 == 1 and fe1 == 0x10 and fm1 == 0x0d6 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b5e4]:feq.h t6, ft11, ft10<br> [0x8000b5e8]:csrrs a0, fcsr, zero<br> [0x8000b5ec]:sw t6, 792(t1)<br>    |
| 895|[0x80013f04]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x0d6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b624]:feq.h t6, ft11, ft10<br> [0x8000b628]:csrrs a0, fcsr, zero<br> [0x8000b62c]:sw t6, 800(t1)<br>    |
| 896|[0x80013f0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x195 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x0d6 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b664]:feq.h t6, ft11, ft10<br> [0x8000b668]:csrrs a0, fcsr, zero<br> [0x8000b66c]:sw t6, 808(t1)<br>    |
| 897|[0x80013f14]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b6a4]:feq.h t6, ft11, ft10<br> [0x8000b6a8]:csrrs a0, fcsr, zero<br> [0x8000b6ac]:sw t6, 816(t1)<br>    |
| 898|[0x80013f1c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b6e4]:feq.h t6, ft11, ft10<br> [0x8000b6e8]:csrrs a0, fcsr, zero<br> [0x8000b6ec]:sw t6, 824(t1)<br>    |
| 899|[0x80013f24]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b724]:feq.h t6, ft11, ft10<br> [0x8000b728]:csrrs a0, fcsr, zero<br> [0x8000b72c]:sw t6, 832(t1)<br>    |
| 900|[0x80013f2c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b764]:feq.h t6, ft11, ft10<br> [0x8000b768]:csrrs a0, fcsr, zero<br> [0x8000b76c]:sw t6, 840(t1)<br>    |
| 901|[0x80013f34]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b7a4]:feq.h t6, ft11, ft10<br> [0x8000b7a8]:csrrs a0, fcsr, zero<br> [0x8000b7ac]:sw t6, 848(t1)<br>    |
| 902|[0x80013f3c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b7e4]:feq.h t6, ft11, ft10<br> [0x8000b7e8]:csrrs a0, fcsr, zero<br> [0x8000b7ec]:sw t6, 856(t1)<br>    |
| 903|[0x80013f44]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b824]:feq.h t6, ft11, ft10<br> [0x8000b828]:csrrs a0, fcsr, zero<br> [0x8000b82c]:sw t6, 864(t1)<br>    |
| 904|[0x80013f4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b864]:feq.h t6, ft11, ft10<br> [0x8000b868]:csrrs a0, fcsr, zero<br> [0x8000b86c]:sw t6, 872(t1)<br>    |
| 905|[0x80013f54]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b8a4]:feq.h t6, ft11, ft10<br> [0x8000b8a8]:csrrs a0, fcsr, zero<br> [0x8000b8ac]:sw t6, 880(t1)<br>    |
| 906|[0x80013f5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b8e4]:feq.h t6, ft11, ft10<br> [0x8000b8e8]:csrrs a0, fcsr, zero<br> [0x8000b8ec]:sw t6, 888(t1)<br>    |
| 907|[0x80013f64]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b924]:feq.h t6, ft11, ft10<br> [0x8000b928]:csrrs a0, fcsr, zero<br> [0x8000b92c]:sw t6, 896(t1)<br>    |
| 908|[0x80013f6c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b964]:feq.h t6, ft11, ft10<br> [0x8000b968]:csrrs a0, fcsr, zero<br> [0x8000b96c]:sw t6, 904(t1)<br>    |
| 909|[0x80013f74]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x0dd and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b9a4]:feq.h t6, ft11, ft10<br> [0x8000b9a8]:csrrs a0, fcsr, zero<br> [0x8000b9ac]:sw t6, 912(t1)<br>    |
| 910|[0x80013f7c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x0dd and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000b9e4]:feq.h t6, ft11, ft10<br> [0x8000b9e8]:csrrs a0, fcsr, zero<br> [0x8000b9ec]:sw t6, 920(t1)<br>    |
| 911|[0x80013f84]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ba24]:feq.h t6, ft11, ft10<br> [0x8000ba28]:csrrs a0, fcsr, zero<br> [0x8000ba2c]:sw t6, 928(t1)<br>    |
| 912|[0x80013f8c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ba64]:feq.h t6, ft11, ft10<br> [0x8000ba68]:csrrs a0, fcsr, zero<br> [0x8000ba6c]:sw t6, 936(t1)<br>    |
| 913|[0x80013f94]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000baa4]:feq.h t6, ft11, ft10<br> [0x8000baa8]:csrrs a0, fcsr, zero<br> [0x8000baac]:sw t6, 944(t1)<br>    |
| 914|[0x80013f9c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bae4]:feq.h t6, ft11, ft10<br> [0x8000bae8]:csrrs a0, fcsr, zero<br> [0x8000baec]:sw t6, 952(t1)<br>    |
| 915|[0x80013fa4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x010 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bb24]:feq.h t6, ft11, ft10<br> [0x8000bb28]:csrrs a0, fcsr, zero<br> [0x8000bb2c]:sw t6, 960(t1)<br>    |
| 916|[0x80013fac]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x010 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bb64]:feq.h t6, ft11, ft10<br> [0x8000bb68]:csrrs a0, fcsr, zero<br> [0x8000bb6c]:sw t6, 968(t1)<br>    |
| 917|[0x80013fb4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bba4]:feq.h t6, ft11, ft10<br> [0x8000bba8]:csrrs a0, fcsr, zero<br> [0x8000bbac]:sw t6, 976(t1)<br>    |
| 918|[0x80013fbc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bbe4]:feq.h t6, ft11, ft10<br> [0x8000bbe8]:csrrs a0, fcsr, zero<br> [0x8000bbec]:sw t6, 984(t1)<br>    |
| 919|[0x80013fc4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bc24]:feq.h t6, ft11, ft10<br> [0x8000bc28]:csrrs a0, fcsr, zero<br> [0x8000bc2c]:sw t6, 992(t1)<br>    |
| 920|[0x80013fcc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bc64]:feq.h t6, ft11, ft10<br> [0x8000bc68]:csrrs a0, fcsr, zero<br> [0x8000bc6c]:sw t6, 1000(t1)<br>   |
| 921|[0x80013fd4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bca4]:feq.h t6, ft11, ft10<br> [0x8000bca8]:csrrs a0, fcsr, zero<br> [0x8000bcac]:sw t6, 1008(t1)<br>   |
| 922|[0x80013fdc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bce4]:feq.h t6, ft11, ft10<br> [0x8000bce8]:csrrs a0, fcsr, zero<br> [0x8000bcec]:sw t6, 1016(t1)<br>   |
| 923|[0x80013fe4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bd2c]:feq.h t6, ft11, ft10<br> [0x8000bd30]:csrrs a0, fcsr, zero<br> [0x8000bd34]:sw t6, 0(t1)<br>      |
| 924|[0x80013fec]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bd6c]:feq.h t6, ft11, ft10<br> [0x8000bd70]:csrrs a0, fcsr, zero<br> [0x8000bd74]:sw t6, 8(t1)<br>      |
| 925|[0x80013ff4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bdac]:feq.h t6, ft11, ft10<br> [0x8000bdb0]:csrrs a0, fcsr, zero<br> [0x8000bdb4]:sw t6, 16(t1)<br>     |
| 926|[0x80013ffc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x036 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bdec]:feq.h t6, ft11, ft10<br> [0x8000bdf0]:csrrs a0, fcsr, zero<br> [0x8000bdf4]:sw t6, 24(t1)<br>     |
| 927|[0x80014004]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x036 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000be2c]:feq.h t6, ft11, ft10<br> [0x8000be30]:csrrs a0, fcsr, zero<br> [0x8000be34]:sw t6, 32(t1)<br>     |
| 928|[0x8001400c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000be6c]:feq.h t6, ft11, ft10<br> [0x8000be70]:csrrs a0, fcsr, zero<br> [0x8000be74]:sw t6, 40(t1)<br>     |
| 929|[0x80014014]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000beac]:feq.h t6, ft11, ft10<br> [0x8000beb0]:csrrs a0, fcsr, zero<br> [0x8000beb4]:sw t6, 48(t1)<br>     |
| 930|[0x8001401c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x056 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000beec]:feq.h t6, ft11, ft10<br> [0x8000bef0]:csrrs a0, fcsr, zero<br> [0x8000bef4]:sw t6, 56(t1)<br>     |
| 931|[0x80014024]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x056 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bf2c]:feq.h t6, ft11, ft10<br> [0x8000bf30]:csrrs a0, fcsr, zero<br> [0x8000bf34]:sw t6, 64(t1)<br>     |
| 932|[0x8001402c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bf6c]:feq.h t6, ft11, ft10<br> [0x8000bf70]:csrrs a0, fcsr, zero<br> [0x8000bf74]:sw t6, 72(t1)<br>     |
| 933|[0x80014034]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bfac]:feq.h t6, ft11, ft10<br> [0x8000bfb0]:csrrs a0, fcsr, zero<br> [0x8000bfb4]:sw t6, 80(t1)<br>     |
| 934|[0x8001403c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x01a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000bfec]:feq.h t6, ft11, ft10<br> [0x8000bff0]:csrrs a0, fcsr, zero<br> [0x8000bff4]:sw t6, 88(t1)<br>     |
| 935|[0x80014044]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x01a and fs2 == 1 and fe2 == 0x01 and fm2 == 0x287 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c02c]:feq.h t6, ft11, ft10<br> [0x8000c030]:csrrs a0, fcsr, zero<br> [0x8000c034]:sw t6, 96(t1)<br>     |
| 936|[0x8001404c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x287 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c06c]:feq.h t6, ft11, ft10<br> [0x8000c070]:csrrs a0, fcsr, zero<br> [0x8000c074]:sw t6, 104(t1)<br>    |
| 937|[0x80014054]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c0ac]:feq.h t6, ft11, ft10<br> [0x8000c0b0]:csrrs a0, fcsr, zero<br> [0x8000c0b4]:sw t6, 112(t1)<br>    |
| 938|[0x8001405c]<br>0x00000000|- fs1 == 1 and fe1 == 0x12 and fm1 == 0x0fa and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c0ec]:feq.h t6, ft11, ft10<br> [0x8000c0f0]:csrrs a0, fcsr, zero<br> [0x8000c0f4]:sw t6, 120(t1)<br>    |
| 939|[0x80014064]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x12 and fm2 == 0x0fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c12c]:feq.h t6, ft11, ft10<br> [0x8000c130]:csrrs a0, fcsr, zero<br> [0x8000c134]:sw t6, 128(t1)<br>    |
| 940|[0x8001406c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x0a7 and fs2 == 1 and fe2 == 0x12 and fm2 == 0x0fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c16c]:feq.h t6, ft11, ft10<br> [0x8000c170]:csrrs a0, fcsr, zero<br> [0x8000c174]:sw t6, 136(t1)<br>    |
| 941|[0x80014074]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c1ac]:feq.h t6, ft11, ft10<br> [0x8000c1b0]:csrrs a0, fcsr, zero<br> [0x8000c1b4]:sw t6, 144(t1)<br>    |
| 942|[0x8001407c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c1ec]:feq.h t6, ft11, ft10<br> [0x8000c1f0]:csrrs a0, fcsr, zero<br> [0x8000c1f4]:sw t6, 152(t1)<br>    |
| 943|[0x80014084]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1d and fm2 == 0x3e4 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c22c]:feq.h t6, ft11, ft10<br> [0x8000c230]:csrrs a0, fcsr, zero<br> [0x8000c234]:sw t6, 160(t1)<br>    |
| 944|[0x8001408c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c26c]:feq.h t6, ft11, ft10<br> [0x8000c270]:csrrs a0, fcsr, zero<br> [0x8000c274]:sw t6, 168(t1)<br>    |
| 945|[0x80014094]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c2ac]:feq.h t6, ft11, ft10<br> [0x8000c2b0]:csrrs a0, fcsr, zero<br> [0x8000c2b4]:sw t6, 176(t1)<br>    |
| 946|[0x8001409c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c2ec]:feq.h t6, ft11, ft10<br> [0x8000c2f0]:csrrs a0, fcsr, zero<br> [0x8000c2f4]:sw t6, 184(t1)<br>    |
| 947|[0x800140a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c32c]:feq.h t6, ft11, ft10<br> [0x8000c330]:csrrs a0, fcsr, zero<br> [0x8000c334]:sw t6, 192(t1)<br>    |
| 948|[0x800140ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c36c]:feq.h t6, ft11, ft10<br> [0x8000c370]:csrrs a0, fcsr, zero<br> [0x8000c374]:sw t6, 200(t1)<br>    |
| 949|[0x800140b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c3ac]:feq.h t6, ft11, ft10<br> [0x8000c3b0]:csrrs a0, fcsr, zero<br> [0x8000c3b4]:sw t6, 208(t1)<br>    |
| 950|[0x800140bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c3ec]:feq.h t6, ft11, ft10<br> [0x8000c3f0]:csrrs a0, fcsr, zero<br> [0x8000c3f4]:sw t6, 216(t1)<br>    |
| 951|[0x800140c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c42c]:feq.h t6, ft11, ft10<br> [0x8000c430]:csrrs a0, fcsr, zero<br> [0x8000c434]:sw t6, 224(t1)<br>    |
| 952|[0x800140cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c46c]:feq.h t6, ft11, ft10<br> [0x8000c470]:csrrs a0, fcsr, zero<br> [0x8000c474]:sw t6, 232(t1)<br>    |
| 953|[0x800140d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c4ac]:feq.h t6, ft11, ft10<br> [0x8000c4b0]:csrrs a0, fcsr, zero<br> [0x8000c4b4]:sw t6, 240(t1)<br>    |
| 954|[0x800140dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c4ec]:feq.h t6, ft11, ft10<br> [0x8000c4f0]:csrrs a0, fcsr, zero<br> [0x8000c4f4]:sw t6, 248(t1)<br>    |
| 955|[0x800140e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c52c]:feq.h t6, ft11, ft10<br> [0x8000c530]:csrrs a0, fcsr, zero<br> [0x8000c534]:sw t6, 256(t1)<br>    |
| 956|[0x800140ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c56c]:feq.h t6, ft11, ft10<br> [0x8000c570]:csrrs a0, fcsr, zero<br> [0x8000c574]:sw t6, 264(t1)<br>    |
| 957|[0x800140f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c5ac]:feq.h t6, ft11, ft10<br> [0x8000c5b0]:csrrs a0, fcsr, zero<br> [0x8000c5b4]:sw t6, 272(t1)<br>    |
| 958|[0x800140fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c5ec]:feq.h t6, ft11, ft10<br> [0x8000c5f0]:csrrs a0, fcsr, zero<br> [0x8000c5f4]:sw t6, 280(t1)<br>    |
| 959|[0x80014104]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c62c]:feq.h t6, ft11, ft10<br> [0x8000c630]:csrrs a0, fcsr, zero<br> [0x8000c634]:sw t6, 288(t1)<br>    |
| 960|[0x8001410c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1d and fm1 == 0x3e4 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c66c]:feq.h t6, ft11, ft10<br> [0x8000c670]:csrrs a0, fcsr, zero<br> [0x8000c674]:sw t6, 296(t1)<br>    |
| 961|[0x80014114]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c6ac]:feq.h t6, ft11, ft10<br> [0x8000c6b0]:csrrs a0, fcsr, zero<br> [0x8000c6b4]:sw t6, 304(t1)<br>    |
| 962|[0x8001411c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1a and fm1 == 0x250 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c6ec]:feq.h t6, ft11, ft10<br> [0x8000c6f0]:csrrs a0, fcsr, zero<br> [0x8000c6f4]:sw t6, 312(t1)<br>    |
| 963|[0x80014124]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x1a and fm2 == 0x250 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c72c]:feq.h t6, ft11, ft10<br> [0x8000c730]:csrrs a0, fcsr, zero<br> [0x8000c734]:sw t6, 320(t1)<br>    |
| 964|[0x8001412c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c76c]:feq.h t6, ft11, ft10<br> [0x8000c770]:csrrs a0, fcsr, zero<br> [0x8000c774]:sw t6, 328(t1)<br>    |
| 965|[0x80014134]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x005 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c7ac]:feq.h t6, ft11, ft10<br> [0x8000c7b0]:csrrs a0, fcsr, zero<br> [0x8000c7b4]:sw t6, 336(t1)<br>    |
| 966|[0x8001413c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c7ec]:feq.h t6, ft11, ft10<br> [0x8000c7f0]:csrrs a0, fcsr, zero<br> [0x8000c7f4]:sw t6, 344(t1)<br>    |
| 967|[0x80014144]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x036 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c82c]:feq.h t6, ft11, ft10<br> [0x8000c830]:csrrs a0, fcsr, zero<br> [0x8000c834]:sw t6, 352(t1)<br>    |
| 968|[0x8001414c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x036 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c86c]:feq.h t6, ft11, ft10<br> [0x8000c870]:csrrs a0, fcsr, zero<br> [0x8000c874]:sw t6, 360(t1)<br>    |
| 969|[0x80014154]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c8ac]:feq.h t6, ft11, ft10<br> [0x8000c8b0]:csrrs a0, fcsr, zero<br> [0x8000c8b4]:sw t6, 368(t1)<br>    |
| 970|[0x8001415c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c8ec]:feq.h t6, ft11, ft10<br> [0x8000c8f0]:csrrs a0, fcsr, zero<br> [0x8000c8f4]:sw t6, 376(t1)<br>    |
| 971|[0x80014164]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c92c]:feq.h t6, ft11, ft10<br> [0x8000c930]:csrrs a0, fcsr, zero<br> [0x8000c934]:sw t6, 384(t1)<br>    |
| 972|[0x8001416c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c96c]:feq.h t6, ft11, ft10<br> [0x8000c970]:csrrs a0, fcsr, zero<br> [0x8000c974]:sw t6, 392(t1)<br>    |
| 973|[0x80014174]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c9ac]:feq.h t6, ft11, ft10<br> [0x8000c9b0]:csrrs a0, fcsr, zero<br> [0x8000c9b4]:sw t6, 400(t1)<br>    |
| 974|[0x8001417c]<br>0x00000000|- fs1 == 1 and fe1 == 0x10 and fm1 == 0x277 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000c9ec]:feq.h t6, ft11, ft10<br> [0x8000c9f0]:csrrs a0, fcsr, zero<br> [0x8000c9f4]:sw t6, 408(t1)<br>    |
| 975|[0x80014184]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x10 and fm2 == 0x277 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ca2c]:feq.h t6, ft11, ft10<br> [0x8000ca30]:csrrs a0, fcsr, zero<br> [0x8000ca34]:sw t6, 416(t1)<br>    |
| 976|[0x8001418c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x21e and fs2 == 1 and fe2 == 0x10 and fm2 == 0x277 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ca6c]:feq.h t6, ft11, ft10<br> [0x8000ca70]:csrrs a0, fcsr, zero<br> [0x8000ca74]:sw t6, 424(t1)<br>    |
| 977|[0x80014194]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000caac]:feq.h t6, ft11, ft10<br> [0x8000cab0]:csrrs a0, fcsr, zero<br> [0x8000cab4]:sw t6, 432(t1)<br>    |
| 978|[0x8001419c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000caec]:feq.h t6, ft11, ft10<br> [0x8000caf0]:csrrs a0, fcsr, zero<br> [0x8000caf4]:sw t6, 440(t1)<br>    |
| 979|[0x800141a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x252 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cb2c]:feq.h t6, ft11, ft10<br> [0x8000cb30]:csrrs a0, fcsr, zero<br> [0x8000cb34]:sw t6, 448(t1)<br>    |
| 980|[0x800141ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cb6c]:feq.h t6, ft11, ft10<br> [0x8000cb70]:csrrs a0, fcsr, zero<br> [0x8000cb74]:sw t6, 456(t1)<br>    |
| 981|[0x800141b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cbac]:feq.h t6, ft11, ft10<br> [0x8000cbb0]:csrrs a0, fcsr, zero<br> [0x8000cbb4]:sw t6, 464(t1)<br>    |
| 982|[0x800141bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cbec]:feq.h t6, ft11, ft10<br> [0x8000cbf0]:csrrs a0, fcsr, zero<br> [0x8000cbf4]:sw t6, 472(t1)<br>    |
| 983|[0x800141c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cc2c]:feq.h t6, ft11, ft10<br> [0x8000cc30]:csrrs a0, fcsr, zero<br> [0x8000cc34]:sw t6, 480(t1)<br>    |
| 984|[0x800141cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cc6c]:feq.h t6, ft11, ft10<br> [0x8000cc70]:csrrs a0, fcsr, zero<br> [0x8000cc74]:sw t6, 488(t1)<br>    |
| 985|[0x800141d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ccac]:feq.h t6, ft11, ft10<br> [0x8000ccb0]:csrrs a0, fcsr, zero<br> [0x8000ccb4]:sw t6, 496(t1)<br>    |
| 986|[0x800141dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ccec]:feq.h t6, ft11, ft10<br> [0x8000ccf0]:csrrs a0, fcsr, zero<br> [0x8000ccf4]:sw t6, 504(t1)<br>    |
| 987|[0x800141e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cd2c]:feq.h t6, ft11, ft10<br> [0x8000cd30]:csrrs a0, fcsr, zero<br> [0x8000cd34]:sw t6, 512(t1)<br>    |
| 988|[0x800141ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cd6c]:feq.h t6, ft11, ft10<br> [0x8000cd70]:csrrs a0, fcsr, zero<br> [0x8000cd74]:sw t6, 520(t1)<br>    |
| 989|[0x800141f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cdac]:feq.h t6, ft11, ft10<br> [0x8000cdb0]:csrrs a0, fcsr, zero<br> [0x8000cdb4]:sw t6, 528(t1)<br>    |
| 990|[0x800141fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cdec]:feq.h t6, ft11, ft10<br> [0x8000cdf0]:csrrs a0, fcsr, zero<br> [0x8000cdf4]:sw t6, 536(t1)<br>    |
| 991|[0x80014204]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ce2c]:feq.h t6, ft11, ft10<br> [0x8000ce30]:csrrs a0, fcsr, zero<br> [0x8000ce34]:sw t6, 544(t1)<br>    |
| 992|[0x8001420c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ce6c]:feq.h t6, ft11, ft10<br> [0x8000ce70]:csrrs a0, fcsr, zero<br> [0x8000ce74]:sw t6, 552(t1)<br>    |
| 993|[0x80014214]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ceac]:feq.h t6, ft11, ft10<br> [0x8000ceb0]:csrrs a0, fcsr, zero<br> [0x8000ceb4]:sw t6, 560(t1)<br>    |
| 994|[0x8001421c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ceec]:feq.h t6, ft11, ft10<br> [0x8000cef0]:csrrs a0, fcsr, zero<br> [0x8000cef4]:sw t6, 568(t1)<br>    |
| 995|[0x80014224]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cf2c]:feq.h t6, ft11, ft10<br> [0x8000cf30]:csrrs a0, fcsr, zero<br> [0x8000cf34]:sw t6, 576(t1)<br>    |
| 996|[0x8001422c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x252 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cf6c]:feq.h t6, ft11, ft10<br> [0x8000cf70]:csrrs a0, fcsr, zero<br> [0x8000cf74]:sw t6, 584(t1)<br>    |
| 997|[0x80014234]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cfac]:feq.h t6, ft11, ft10<br> [0x8000cfb0]:csrrs a0, fcsr, zero<br> [0x8000cfb4]:sw t6, 592(t1)<br>    |
| 998|[0x8001423c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1b and fm1 == 0x10f and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000cfec]:feq.h t6, ft11, ft10<br> [0x8000cff0]:csrrs a0, fcsr, zero<br> [0x8000cff4]:sw t6, 600(t1)<br>    |
| 999|[0x80014244]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x1b and fm2 == 0x10f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d02c]:feq.h t6, ft11, ft10<br> [0x8000d030]:csrrs a0, fcsr, zero<br> [0x8000d034]:sw t6, 608(t1)<br>    |
|1000|[0x8001424c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d06c]:feq.h t6, ft11, ft10<br> [0x8000d070]:csrrs a0, fcsr, zero<br> [0x8000d074]:sw t6, 616(t1)<br>    |
|1001|[0x80014254]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x008 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d0ac]:feq.h t6, ft11, ft10<br> [0x8000d0b0]:csrrs a0, fcsr, zero<br> [0x8000d0b4]:sw t6, 624(t1)<br>    |
|1002|[0x8001425c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d0ec]:feq.h t6, ft11, ft10<br> [0x8000d0f0]:csrrs a0, fcsr, zero<br> [0x8000d0f4]:sw t6, 632(t1)<br>    |
|1003|[0x80014264]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x056 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d12c]:feq.h t6, ft11, ft10<br> [0x8000d130]:csrrs a0, fcsr, zero<br> [0x8000d134]:sw t6, 640(t1)<br>    |
|1004|[0x8001426c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x056 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d16c]:feq.h t6, ft11, ft10<br> [0x8000d170]:csrrs a0, fcsr, zero<br> [0x8000d174]:sw t6, 648(t1)<br>    |
|1005|[0x80014274]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d1ac]:feq.h t6, ft11, ft10<br> [0x8000d1b0]:csrrs a0, fcsr, zero<br> [0x8000d1b4]:sw t6, 656(t1)<br>    |
|1006|[0x8001427c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d1ec]:feq.h t6, ft11, ft10<br> [0x8000d1f0]:csrrs a0, fcsr, zero<br> [0x8000d1f4]:sw t6, 664(t1)<br>    |
|1007|[0x80014284]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d22c]:feq.h t6, ft11, ft10<br> [0x8000d230]:csrrs a0, fcsr, zero<br> [0x8000d234]:sw t6, 672(t1)<br>    |
|1008|[0x8001428c]<br>0x00000000|- fs1 == 1 and fe1 == 0x11 and fm1 == 0x12e and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d26c]:feq.h t6, ft11, ft10<br> [0x8000d270]:csrrs a0, fcsr, zero<br> [0x8000d274]:sw t6, 680(t1)<br>    |
|1009|[0x80014294]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x12e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d2ac]:feq.h t6, ft11, ft10<br> [0x8000d2b0]:csrrs a0, fcsr, zero<br> [0x8000d2b4]:sw t6, 688(t1)<br>    |
|1010|[0x8001429c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x365 and fs2 == 1 and fe2 == 0x11 and fm2 == 0x12e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d2ec]:feq.h t6, ft11, ft10<br> [0x8000d2f0]:csrrs a0, fcsr, zero<br> [0x8000d2f4]:sw t6, 696(t1)<br>    |
|1011|[0x800142a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d32c]:feq.h t6, ft11, ft10<br> [0x8000d330]:csrrs a0, fcsr, zero<br> [0x8000d334]:sw t6, 704(t1)<br>    |
|1012|[0x800142ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d36c]:feq.h t6, ft11, ft10<br> [0x8000d370]:csrrs a0, fcsr, zero<br> [0x8000d374]:sw t6, 712(t1)<br>    |
|1013|[0x800142b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x3b9 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d3ac]:feq.h t6, ft11, ft10<br> [0x8000d3b0]:csrrs a0, fcsr, zero<br> [0x8000d3b4]:sw t6, 720(t1)<br>    |
|1014|[0x800142bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d3ec]:feq.h t6, ft11, ft10<br> [0x8000d3f0]:csrrs a0, fcsr, zero<br> [0x8000d3f4]:sw t6, 728(t1)<br>    |
|1015|[0x800142c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d42c]:feq.h t6, ft11, ft10<br> [0x8000d430]:csrrs a0, fcsr, zero<br> [0x8000d434]:sw t6, 736(t1)<br>    |
|1016|[0x800142cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d46c]:feq.h t6, ft11, ft10<br> [0x8000d470]:csrrs a0, fcsr, zero<br> [0x8000d474]:sw t6, 744(t1)<br>    |
|1017|[0x800142d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d4ac]:feq.h t6, ft11, ft10<br> [0x8000d4b0]:csrrs a0, fcsr, zero<br> [0x8000d4b4]:sw t6, 752(t1)<br>    |
|1018|[0x800142dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d4ec]:feq.h t6, ft11, ft10<br> [0x8000d4f0]:csrrs a0, fcsr, zero<br> [0x8000d4f4]:sw t6, 760(t1)<br>    |
|1019|[0x800142e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d52c]:feq.h t6, ft11, ft10<br> [0x8000d530]:csrrs a0, fcsr, zero<br> [0x8000d534]:sw t6, 768(t1)<br>    |
|1020|[0x800142ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d56c]:feq.h t6, ft11, ft10<br> [0x8000d570]:csrrs a0, fcsr, zero<br> [0x8000d574]:sw t6, 776(t1)<br>    |
|1021|[0x800142f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d5ac]:feq.h t6, ft11, ft10<br> [0x8000d5b0]:csrrs a0, fcsr, zero<br> [0x8000d5b4]:sw t6, 784(t1)<br>    |
|1022|[0x800142fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d5ec]:feq.h t6, ft11, ft10<br> [0x8000d5f0]:csrrs a0, fcsr, zero<br> [0x8000d5f4]:sw t6, 792(t1)<br>    |
|1023|[0x80014304]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d62c]:feq.h t6, ft11, ft10<br> [0x8000d630]:csrrs a0, fcsr, zero<br> [0x8000d634]:sw t6, 800(t1)<br>    |
|1024|[0x8001430c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d66c]:feq.h t6, ft11, ft10<br> [0x8000d670]:csrrs a0, fcsr, zero<br> [0x8000d674]:sw t6, 808(t1)<br>    |
|1025|[0x80014314]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d6ac]:feq.h t6, ft11, ft10<br> [0x8000d6b0]:csrrs a0, fcsr, zero<br> [0x8000d6b4]:sw t6, 816(t1)<br>    |
|1026|[0x8001431c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d6ec]:feq.h t6, ft11, ft10<br> [0x8000d6f0]:csrrs a0, fcsr, zero<br> [0x8000d6f4]:sw t6, 824(t1)<br>    |
|1027|[0x80014324]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d72c]:feq.h t6, ft11, ft10<br> [0x8000d730]:csrrs a0, fcsr, zero<br> [0x8000d734]:sw t6, 832(t1)<br>    |
|1028|[0x8001432c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d76c]:feq.h t6, ft11, ft10<br> [0x8000d770]:csrrs a0, fcsr, zero<br> [0x8000d774]:sw t6, 840(t1)<br>    |
|1029|[0x80014334]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d7ac]:feq.h t6, ft11, ft10<br> [0x8000d7b0]:csrrs a0, fcsr, zero<br> [0x8000d7b4]:sw t6, 848(t1)<br>    |
|1030|[0x8001433c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1c and fm1 == 0x3b9 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d7ec]:feq.h t6, ft11, ft10<br> [0x8000d7f0]:csrrs a0, fcsr, zero<br> [0x8000d7f4]:sw t6, 856(t1)<br>    |
|1031|[0x80014344]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d82c]:feq.h t6, ft11, ft10<br> [0x8000d830]:csrrs a0, fcsr, zero<br> [0x8000d834]:sw t6, 864(t1)<br>    |
|1032|[0x8001434c]<br>0x00000000|- fs1 == 1 and fe1 == 0x19 and fm1 == 0x22e and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d86c]:feq.h t6, ft11, ft10<br> [0x8000d870]:csrrs a0, fcsr, zero<br> [0x8000d874]:sw t6, 872(t1)<br>    |
|1033|[0x80014354]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x19 and fm2 == 0x22e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d8ac]:feq.h t6, ft11, ft10<br> [0x8000d8b0]:csrrs a0, fcsr, zero<br> [0x8000d8b4]:sw t6, 880(t1)<br>    |
|1034|[0x8001435c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d8ec]:feq.h t6, ft11, ft10<br> [0x8000d8f0]:csrrs a0, fcsr, zero<br> [0x8000d8f4]:sw t6, 888(t1)<br>    |
|1035|[0x80014364]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d92c]:feq.h t6, ft11, ft10<br> [0x8000d930]:csrrs a0, fcsr, zero<br> [0x8000d934]:sw t6, 896(t1)<br>    |
|1036|[0x8001436c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d96c]:feq.h t6, ft11, ft10<br> [0x8000d970]:csrrs a0, fcsr, zero<br> [0x8000d974]:sw t6, 904(t1)<br>    |
|1037|[0x80014374]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d9ac]:feq.h t6, ft11, ft10<br> [0x8000d9b0]:csrrs a0, fcsr, zero<br> [0x8000d9b4]:sw t6, 912(t1)<br>    |
|1038|[0x8001437c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x01a and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000d9ec]:feq.h t6, ft11, ft10<br> [0x8000d9f0]:csrrs a0, fcsr, zero<br> [0x8000d9f4]:sw t6, 920(t1)<br>    |
|1039|[0x80014384]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x01a and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000da2c]:feq.h t6, ft11, ft10<br> [0x8000da30]:csrrs a0, fcsr, zero<br> [0x8000da34]:sw t6, 928(t1)<br>    |
|1040|[0x8001438c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000da6c]:feq.h t6, ft11, ft10<br> [0x8000da70]:csrrs a0, fcsr, zero<br> [0x8000da74]:sw t6, 936(t1)<br>    |
|1041|[0x80014394]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x254 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000daac]:feq.h t6, ft11, ft10<br> [0x8000dab0]:csrrs a0, fcsr, zero<br> [0x8000dab4]:sw t6, 944(t1)<br>    |
|1042|[0x8001439c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x254 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000daec]:feq.h t6, ft11, ft10<br> [0x8000daf0]:csrrs a0, fcsr, zero<br> [0x8000daf4]:sw t6, 952(t1)<br>    |
|1043|[0x800143a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x109 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x254 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000db2c]:feq.h t6, ft11, ft10<br> [0x8000db30]:csrrs a0, fcsr, zero<br> [0x8000db34]:sw t6, 960(t1)<br>    |
|1044|[0x800143ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1c and fm2 == 0x39c and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000db6c]:feq.h t6, ft11, ft10<br> [0x8000db70]:csrrs a0, fcsr, zero<br> [0x8000db74]:sw t6, 968(t1)<br>    |
|1045|[0x800143b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x0f0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dbac]:feq.h t6, ft11, ft10<br> [0x8000dbb0]:csrrs a0, fcsr, zero<br> [0x8000dbb4]:sw t6, 976(t1)<br>    |
|1046|[0x800143bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dbec]:feq.h t6, ft11, ft10<br> [0x8000dbf0]:csrrs a0, fcsr, zero<br> [0x8000dbf4]:sw t6, 984(t1)<br>    |
|1047|[0x800143c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1d and fm2 == 0x025 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dc2c]:feq.h t6, ft11, ft10<br> [0x8000dc30]:csrrs a0, fcsr, zero<br> [0x8000dc34]:sw t6, 992(t1)<br>    |
|1048|[0x800143cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x2b0 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dc64]:feq.h t6, ft11, ft10<br> [0x8000dc68]:csrrs a0, fcsr, zero<br> [0x8000dc6c]:sw t6, 1000(t1)<br>   |
|1049|[0x800143d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x113 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dc9c]:feq.h t6, ft11, ft10<br> [0x8000dca0]:csrrs a0, fcsr, zero<br> [0x8000dca4]:sw t6, 1008(t1)<br>   |
|1050|[0x800143dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1d and fm2 == 0x349 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dcd4]:feq.h t6, ft11, ft10<br> [0x8000dcd8]:csrrs a0, fcsr, zero<br> [0x8000dcdc]:sw t6, 1016(t1)<br>   |
|1051|[0x800143e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x378 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dd14]:feq.h t6, ft11, ft10<br> [0x8000dd18]:csrrs a0, fcsr, zero<br> [0x8000dd1c]:sw t6, 0(t1)<br>      |
|1052|[0x800143ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x21f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dd4c]:feq.h t6, ft11, ft10<br> [0x8000dd50]:csrrs a0, fcsr, zero<br> [0x8000dd54]:sw t6, 8(t1)<br>      |
|1053|[0x800143f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x02f and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dd84]:feq.h t6, ft11, ft10<br> [0x8000dd88]:csrrs a0, fcsr, zero<br> [0x8000dd8c]:sw t6, 16(t1)<br>     |
|1054|[0x800143fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x1c and fm2 == 0x038 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ddbc]:feq.h t6, ft11, ft10<br> [0x8000ddc0]:csrrs a0, fcsr, zero<br> [0x8000ddc4]:sw t6, 24(t1)<br>     |
|1055|[0x80014404]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x17b and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ddf4]:feq.h t6, ft11, ft10<br> [0x8000ddf8]:csrrs a0, fcsr, zero<br> [0x8000ddfc]:sw t6, 32(t1)<br>     |
|1056|[0x8001440c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x00e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000de2c]:feq.h t6, ft11, ft10<br> [0x8000de30]:csrrs a0, fcsr, zero<br> [0x8000de34]:sw t6, 40(t1)<br>     |
|1057|[0x80014414]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3fa and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000de64]:feq.h t6, ft11, ft10<br> [0x8000de68]:csrrs a0, fcsr, zero<br> [0x8000de6c]:sw t6, 48(t1)<br>     |
|1058|[0x8001441c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x28e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000de9c]:feq.h t6, ft11, ft10<br> [0x8000dea0]:csrrs a0, fcsr, zero<br> [0x8000dea4]:sw t6, 56(t1)<br>     |
|1059|[0x80014424]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x217 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000ded4]:feq.h t6, ft11, ft10<br> [0x8000ded8]:csrrs a0, fcsr, zero<br> [0x8000dedc]:sw t6, 64(t1)<br>     |
|1060|[0x8001442c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x195 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000df0c]:feq.h t6, ft11, ft10<br> [0x8000df10]:csrrs a0, fcsr, zero<br> [0x8000df14]:sw t6, 72(t1)<br>     |
|1061|[0x80014434]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x0a7 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000df44]:feq.h t6, ft11, ft10<br> [0x8000df48]:csrrs a0, fcsr, zero<br> [0x8000df4c]:sw t6, 80(t1)<br>     |
|1062|[0x8001443c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x21e and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000df7c]:feq.h t6, ft11, ft10<br> [0x8000df80]:csrrs a0, fcsr, zero<br> [0x8000df84]:sw t6, 88(t1)<br>     |
|1063|[0x80014444]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x365 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dfb4]:feq.h t6, ft11, ft10<br> [0x8000dfb8]:csrrs a0, fcsr, zero<br> [0x8000dfbc]:sw t6, 96(t1)<br>     |
|1064|[0x8001444c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x0f0 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x109 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000dfec]:feq.h t6, ft11, ft10<br> [0x8000dff0]:csrrs a0, fcsr, zero<br> [0x8000dff4]:sw t6, 104(t1)<br>    |
|1065|[0x80014454]<br>0x00000000|- fs1 == 0 and fe1 == 0x1c and fm1 == 0x39c and fs2 == 0 and fe2 == 0x1e and fm2 == 0x100 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000e024]:feq.h t6, ft11, ft10<br> [0x8000e028]:csrrs a0, fcsr, zero<br> [0x8000e02c]:sw t6, 112(t1)<br>    |

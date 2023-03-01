
# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature.
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update signature
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x800000f8', '0x80006d90')]      |
| SIG_REGION                | [('0x80009410', '0x8000a630', '1160 words')]      |
| COV_LABELS                | feq_b1      |
| TEST_NAME                 | /home/anusha/new/RV32H/feq/work/feq_b1-01.S/ref.S    |
| Total Number of coverpoints| 675     |
| Total Coverpoints Hit     | 675      |
| Total Signature Updates   | 1156      |
| STAT1                     | 577      |
| STAT2                     | 1      |
| STAT3                     | 0     |
| STAT4                     | 578     |
| STAT5                     | 0     |

## Details for STAT2:

```
Op without unique coverpoint updates Signature
 -- Code Sequence:
      [0x80006d7c]:feq.h t6, ft11, ft10
      [0x80006d80]:csrrs a0, fcsr, zero
      [0x80006d84]:sw t6, 312(t1)
 -- Signature Address: 0x8000a61c Data: 0x00000000
 -- Redundant Coverpoints hit by the op
      - mnemonic : feq.h
      - rs1 : f31
      - rs2 : f30
      - rd : x31
      - rs1 != rs2
      - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat






```

## Details of STAT3

```


```

## Details of STAT4:

```
Last Coverpoint : ['mnemonic : feq.h', 'rs1 : f31', 'rs2 : f30', 'rd : x31', 'rs1 != rs2', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000124]:feq.h t6, ft11, ft10
	-[0x80000128]:csrrs tp, fcsr, zero
	-[0x8000012c]:sw t6, 0(ra)
Current Store : [0x80000130] : sw tp, 4(ra) -- Store: [0x80009418]:0x00000000




Last Coverpoint : ['rs1 : f29', 'rs2 : f29', 'rd : x30', 'rs1 == rs2']
Last Code Sequence : 
	-[0x80000144]:feq.h t5, ft9, ft9
	-[0x80000148]:csrrs tp, fcsr, zero
	-[0x8000014c]:sw t5, 8(ra)
Current Store : [0x80000150] : sw tp, 12(ra) -- Store: [0x80009420]:0x00000000




Last Coverpoint : ['rs1 : f30', 'rs2 : f31', 'rd : x29', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000164]:feq.h t4, ft10, ft11
	-[0x80000168]:csrrs tp, fcsr, zero
	-[0x8000016c]:sw t4, 16(ra)
Current Store : [0x80000170] : sw tp, 20(ra) -- Store: [0x80009428]:0x00000000




Last Coverpoint : ['rs1 : f28', 'rs2 : f27', 'rd : x28', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000184]:feq.h t3, ft8, fs11
	-[0x80000188]:csrrs tp, fcsr, zero
	-[0x8000018c]:sw t3, 24(ra)
Current Store : [0x80000190] : sw tp, 28(ra) -- Store: [0x80009430]:0x00000000




Last Coverpoint : ['rs1 : f27', 'rs2 : f28', 'rd : x27', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001a4]:feq.h s11, fs11, ft8
	-[0x800001a8]:csrrs tp, fcsr, zero
	-[0x800001ac]:sw s11, 32(ra)
Current Store : [0x800001b0] : sw tp, 36(ra) -- Store: [0x80009438]:0x00000000




Last Coverpoint : ['rs1 : f26', 'rs2 : f25', 'rd : x26', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001c4]:feq.h s10, fs10, fs9
	-[0x800001c8]:csrrs tp, fcsr, zero
	-[0x800001cc]:sw s10, 40(ra)
Current Store : [0x800001d0] : sw tp, 44(ra) -- Store: [0x80009440]:0x00000000




Last Coverpoint : ['rs1 : f25', 'rs2 : f26', 'rd : x25', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800001e4]:feq.h s9, fs9, fs10
	-[0x800001e8]:csrrs tp, fcsr, zero
	-[0x800001ec]:sw s9, 48(ra)
Current Store : [0x800001f0] : sw tp, 52(ra) -- Store: [0x80009448]:0x00000000




Last Coverpoint : ['rs1 : f24', 'rs2 : f23', 'rd : x24', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000204]:feq.h s8, fs8, fs7
	-[0x80000208]:csrrs tp, fcsr, zero
	-[0x8000020c]:sw s8, 56(ra)
Current Store : [0x80000210] : sw tp, 60(ra) -- Store: [0x80009450]:0x00000000




Last Coverpoint : ['rs1 : f23', 'rs2 : f24', 'rd : x23', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000224]:feq.h s7, fs7, fs8
	-[0x80000228]:csrrs tp, fcsr, zero
	-[0x8000022c]:sw s7, 64(ra)
Current Store : [0x80000230] : sw tp, 68(ra) -- Store: [0x80009458]:0x00000000




Last Coverpoint : ['rs1 : f22', 'rs2 : f21', 'rd : x22', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000244]:feq.h s6, fs6, fs5
	-[0x80000248]:csrrs tp, fcsr, zero
	-[0x8000024c]:sw s6, 72(ra)
Current Store : [0x80000250] : sw tp, 76(ra) -- Store: [0x80009460]:0x00000000




Last Coverpoint : ['rs1 : f21', 'rs2 : f22', 'rd : x21', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000264]:feq.h s5, fs5, fs6
	-[0x80000268]:csrrs tp, fcsr, zero
	-[0x8000026c]:sw s5, 80(ra)
Current Store : [0x80000270] : sw tp, 84(ra) -- Store: [0x80009468]:0x00000000




Last Coverpoint : ['rs1 : f20', 'rs2 : f19', 'rd : x20', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000284]:feq.h s4, fs4, fs3
	-[0x80000288]:csrrs tp, fcsr, zero
	-[0x8000028c]:sw s4, 88(ra)
Current Store : [0x80000290] : sw tp, 92(ra) -- Store: [0x80009470]:0x00000000




Last Coverpoint : ['rs1 : f19', 'rs2 : f20', 'rd : x19', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002a4]:feq.h s3, fs3, fs4
	-[0x800002a8]:csrrs tp, fcsr, zero
	-[0x800002ac]:sw s3, 96(ra)
Current Store : [0x800002b0] : sw tp, 100(ra) -- Store: [0x80009478]:0x00000000




Last Coverpoint : ['rs1 : f18', 'rs2 : f17', 'rd : x18', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002c4]:feq.h s2, fs2, fa7
	-[0x800002c8]:csrrs tp, fcsr, zero
	-[0x800002cc]:sw s2, 104(ra)
Current Store : [0x800002d0] : sw tp, 108(ra) -- Store: [0x80009480]:0x00000000




Last Coverpoint : ['rs1 : f17', 'rs2 : f18', 'rd : x17', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800002e4]:feq.h a7, fa7, fs2
	-[0x800002e8]:csrrs tp, fcsr, zero
	-[0x800002ec]:sw a7, 112(ra)
Current Store : [0x800002f0] : sw tp, 116(ra) -- Store: [0x80009488]:0x00000000




Last Coverpoint : ['rs1 : f16', 'rs2 : f15', 'rd : x16', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000304]:feq.h a6, fa6, fa5
	-[0x80000308]:csrrs tp, fcsr, zero
	-[0x8000030c]:sw a6, 120(ra)
Current Store : [0x80000310] : sw tp, 124(ra) -- Store: [0x80009490]:0x00000000




Last Coverpoint : ['rs1 : f15', 'rs2 : f16', 'rd : x15', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000324]:feq.h a5, fa5, fa6
	-[0x80000328]:csrrs tp, fcsr, zero
	-[0x8000032c]:sw a5, 128(ra)
Current Store : [0x80000330] : sw tp, 132(ra) -- Store: [0x80009498]:0x00000000




Last Coverpoint : ['rs1 : f14', 'rs2 : f13', 'rd : x14', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000344]:feq.h a4, fa4, fa3
	-[0x80000348]:csrrs tp, fcsr, zero
	-[0x8000034c]:sw a4, 136(ra)
Current Store : [0x80000350] : sw tp, 140(ra) -- Store: [0x800094a0]:0x00000000




Last Coverpoint : ['rs1 : f13', 'rs2 : f14', 'rd : x13', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000364]:feq.h a3, fa3, fa4
	-[0x80000368]:csrrs tp, fcsr, zero
	-[0x8000036c]:sw a3, 144(ra)
Current Store : [0x80000370] : sw tp, 148(ra) -- Store: [0x800094a8]:0x00000000




Last Coverpoint : ['rs1 : f12', 'rs2 : f11', 'rd : x12', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000384]:feq.h a2, fa2, fa1
	-[0x80000388]:csrrs tp, fcsr, zero
	-[0x8000038c]:sw a2, 152(ra)
Current Store : [0x80000390] : sw tp, 156(ra) -- Store: [0x800094b0]:0x00000000




Last Coverpoint : ['rs1 : f11', 'rs2 : f12', 'rd : x11', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003a4]:feq.h a1, fa1, fa2
	-[0x800003a8]:csrrs tp, fcsr, zero
	-[0x800003ac]:sw a1, 160(ra)
Current Store : [0x800003b0] : sw tp, 164(ra) -- Store: [0x800094b8]:0x00000000




Last Coverpoint : ['rs1 : f10', 'rs2 : f9', 'rd : x10', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003c4]:feq.h a0, fa0, fs1
	-[0x800003c8]:csrrs tp, fcsr, zero
	-[0x800003cc]:sw a0, 168(ra)
Current Store : [0x800003d0] : sw tp, 172(ra) -- Store: [0x800094c0]:0x00000000




Last Coverpoint : ['rs1 : f9', 'rs2 : f10', 'rd : x9', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800003e4]:feq.h s1, fs1, fa0
	-[0x800003e8]:csrrs tp, fcsr, zero
	-[0x800003ec]:sw s1, 176(ra)
Current Store : [0x800003f0] : sw tp, 180(ra) -- Store: [0x800094c8]:0x00000000




Last Coverpoint : ['rs1 : f8', 'rs2 : f7', 'rd : x8', 'fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000040c]:feq.h fp, fs0, ft7
	-[0x80000410]:csrrs a0, fcsr, zero
	-[0x80000414]:sw fp, 184(ra)
Current Store : [0x80000418] : sw a0, 188(ra) -- Store: [0x800094d0]:0x00000000




Last Coverpoint : ['rs1 : f7', 'rs2 : f8', 'rd : x7', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000042c]:feq.h t2, ft7, fs0
	-[0x80000430]:csrrs a0, fcsr, zero
	-[0x80000434]:sw t2, 192(ra)
Current Store : [0x80000438] : sw a0, 196(ra) -- Store: [0x800094d8]:0x00000000




Last Coverpoint : ['rs1 : f6', 'rs2 : f5', 'rd : x6', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000044c]:feq.h t1, ft6, ft5
	-[0x80000450]:csrrs a0, fcsr, zero
	-[0x80000454]:sw t1, 200(ra)
Current Store : [0x80000458] : sw a0, 204(ra) -- Store: [0x800094e0]:0x00000000




Last Coverpoint : ['rs1 : f5', 'rs2 : f6', 'rd : x5', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000474]:feq.h t0, ft5, ft6
	-[0x80000478]:csrrs a0, fcsr, zero
	-[0x8000047c]:sw t0, 0(t1)
Current Store : [0x80000480] : sw a0, 4(t1) -- Store: [0x800094e8]:0x00000000




Last Coverpoint : ['rs1 : f4', 'rs2 : f3', 'rd : x4', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000494]:feq.h tp, ft4, ft3
	-[0x80000498]:csrrs a0, fcsr, zero
	-[0x8000049c]:sw tp, 8(t1)
Current Store : [0x800004a0] : sw a0, 12(t1) -- Store: [0x800094f0]:0x00000000




Last Coverpoint : ['rs1 : f3', 'rs2 : f4', 'rd : x3', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800004b4]:feq.h gp, ft3, ft4
	-[0x800004b8]:csrrs a0, fcsr, zero
	-[0x800004bc]:sw gp, 16(t1)
Current Store : [0x800004c0] : sw a0, 20(t1) -- Store: [0x800094f8]:0x00000000




Last Coverpoint : ['rs1 : f2', 'rs2 : f1', 'rd : x2', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800004d4]:feq.h sp, ft2, ft1
	-[0x800004d8]:csrrs a0, fcsr, zero
	-[0x800004dc]:sw sp, 24(t1)
Current Store : [0x800004e0] : sw a0, 28(t1) -- Store: [0x80009500]:0x00000000




Last Coverpoint : ['rs1 : f1', 'rs2 : f2', 'rd : x1', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800004f4]:feq.h ra, ft1, ft2
	-[0x800004f8]:csrrs a0, fcsr, zero
	-[0x800004fc]:sw ra, 32(t1)
Current Store : [0x80000500] : sw a0, 36(t1) -- Store: [0x80009508]:0x00000000




Last Coverpoint : ['rs1 : f0', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000514]:feq.h t6, ft0, ft11
	-[0x80000518]:csrrs a0, fcsr, zero
	-[0x8000051c]:sw t6, 40(t1)
Current Store : [0x80000520] : sw a0, 44(t1) -- Store: [0x80009510]:0x00000000




Last Coverpoint : ['rs2 : f0', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000534]:feq.h t6, ft11, ft0
	-[0x80000538]:csrrs a0, fcsr, zero
	-[0x8000053c]:sw t6, 48(t1)
Current Store : [0x80000540] : sw a0, 52(t1) -- Store: [0x80009518]:0x00000000




Last Coverpoint : ['rd : x0', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000554]:feq.h zero, ft11, ft10
	-[0x80000558]:csrrs a0, fcsr, zero
	-[0x8000055c]:sw zero, 56(t1)
Current Store : [0x80000560] : sw a0, 60(t1) -- Store: [0x80009520]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000574]:feq.h t6, ft11, ft10
	-[0x80000578]:csrrs a0, fcsr, zero
	-[0x8000057c]:sw t6, 64(t1)
Current Store : [0x80000580] : sw a0, 68(t1) -- Store: [0x80009528]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000594]:feq.h t6, ft11, ft10
	-[0x80000598]:csrrs a0, fcsr, zero
	-[0x8000059c]:sw t6, 72(t1)
Current Store : [0x800005a0] : sw a0, 76(t1) -- Store: [0x80009530]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800005b4]:feq.h t6, ft11, ft10
	-[0x800005b8]:csrrs a0, fcsr, zero
	-[0x800005bc]:sw t6, 80(t1)
Current Store : [0x800005c0] : sw a0, 84(t1) -- Store: [0x80009538]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800005d4]:feq.h t6, ft11, ft10
	-[0x800005d8]:csrrs a0, fcsr, zero
	-[0x800005dc]:sw t6, 88(t1)
Current Store : [0x800005e0] : sw a0, 92(t1) -- Store: [0x80009540]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800005f4]:feq.h t6, ft11, ft10
	-[0x800005f8]:csrrs a0, fcsr, zero
	-[0x800005fc]:sw t6, 96(t1)
Current Store : [0x80000600] : sw a0, 100(t1) -- Store: [0x80009548]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000614]:feq.h t6, ft11, ft10
	-[0x80000618]:csrrs a0, fcsr, zero
	-[0x8000061c]:sw t6, 104(t1)
Current Store : [0x80000620] : sw a0, 108(t1) -- Store: [0x80009550]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000634]:feq.h t6, ft11, ft10
	-[0x80000638]:csrrs a0, fcsr, zero
	-[0x8000063c]:sw t6, 112(t1)
Current Store : [0x80000640] : sw a0, 116(t1) -- Store: [0x80009558]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000654]:feq.h t6, ft11, ft10
	-[0x80000658]:csrrs a0, fcsr, zero
	-[0x8000065c]:sw t6, 120(t1)
Current Store : [0x80000660] : sw a0, 124(t1) -- Store: [0x80009560]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000674]:feq.h t6, ft11, ft10
	-[0x80000678]:csrrs a0, fcsr, zero
	-[0x8000067c]:sw t6, 128(t1)
Current Store : [0x80000680] : sw a0, 132(t1) -- Store: [0x80009568]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000694]:feq.h t6, ft11, ft10
	-[0x80000698]:csrrs a0, fcsr, zero
	-[0x8000069c]:sw t6, 136(t1)
Current Store : [0x800006a0] : sw a0, 140(t1) -- Store: [0x80009570]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006b4]:feq.h t6, ft11, ft10
	-[0x800006b8]:csrrs a0, fcsr, zero
	-[0x800006bc]:sw t6, 144(t1)
Current Store : [0x800006c0] : sw a0, 148(t1) -- Store: [0x80009578]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006d4]:feq.h t6, ft11, ft10
	-[0x800006d8]:csrrs a0, fcsr, zero
	-[0x800006dc]:sw t6, 152(t1)
Current Store : [0x800006e0] : sw a0, 156(t1) -- Store: [0x80009580]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800006f4]:feq.h t6, ft11, ft10
	-[0x800006f8]:csrrs a0, fcsr, zero
	-[0x800006fc]:sw t6, 160(t1)
Current Store : [0x80000700] : sw a0, 164(t1) -- Store: [0x80009588]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000714]:feq.h t6, ft11, ft10
	-[0x80000718]:csrrs a0, fcsr, zero
	-[0x8000071c]:sw t6, 168(t1)
Current Store : [0x80000720] : sw a0, 172(t1) -- Store: [0x80009590]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000734]:feq.h t6, ft11, ft10
	-[0x80000738]:csrrs a0, fcsr, zero
	-[0x8000073c]:sw t6, 176(t1)
Current Store : [0x80000740] : sw a0, 180(t1) -- Store: [0x80009598]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000754]:feq.h t6, ft11, ft10
	-[0x80000758]:csrrs a0, fcsr, zero
	-[0x8000075c]:sw t6, 184(t1)
Current Store : [0x80000760] : sw a0, 188(t1) -- Store: [0x800095a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000774]:feq.h t6, ft11, ft10
	-[0x80000778]:csrrs a0, fcsr, zero
	-[0x8000077c]:sw t6, 192(t1)
Current Store : [0x80000780] : sw a0, 196(t1) -- Store: [0x800095a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000794]:feq.h t6, ft11, ft10
	-[0x80000798]:csrrs a0, fcsr, zero
	-[0x8000079c]:sw t6, 200(t1)
Current Store : [0x800007a0] : sw a0, 204(t1) -- Store: [0x800095b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007b4]:feq.h t6, ft11, ft10
	-[0x800007b8]:csrrs a0, fcsr, zero
	-[0x800007bc]:sw t6, 208(t1)
Current Store : [0x800007c0] : sw a0, 212(t1) -- Store: [0x800095b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007d4]:feq.h t6, ft11, ft10
	-[0x800007d8]:csrrs a0, fcsr, zero
	-[0x800007dc]:sw t6, 216(t1)
Current Store : [0x800007e0] : sw a0, 220(t1) -- Store: [0x800095c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800007f4]:feq.h t6, ft11, ft10
	-[0x800007f8]:csrrs a0, fcsr, zero
	-[0x800007fc]:sw t6, 224(t1)
Current Store : [0x80000800] : sw a0, 228(t1) -- Store: [0x800095c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000814]:feq.h t6, ft11, ft10
	-[0x80000818]:csrrs a0, fcsr, zero
	-[0x8000081c]:sw t6, 232(t1)
Current Store : [0x80000820] : sw a0, 236(t1) -- Store: [0x800095d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000834]:feq.h t6, ft11, ft10
	-[0x80000838]:csrrs a0, fcsr, zero
	-[0x8000083c]:sw t6, 240(t1)
Current Store : [0x80000840] : sw a0, 244(t1) -- Store: [0x800095d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000854]:feq.h t6, ft11, ft10
	-[0x80000858]:csrrs a0, fcsr, zero
	-[0x8000085c]:sw t6, 248(t1)
Current Store : [0x80000860] : sw a0, 252(t1) -- Store: [0x800095e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000874]:feq.h t6, ft11, ft10
	-[0x80000878]:csrrs a0, fcsr, zero
	-[0x8000087c]:sw t6, 256(t1)
Current Store : [0x80000880] : sw a0, 260(t1) -- Store: [0x800095e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000894]:feq.h t6, ft11, ft10
	-[0x80000898]:csrrs a0, fcsr, zero
	-[0x8000089c]:sw t6, 264(t1)
Current Store : [0x800008a0] : sw a0, 268(t1) -- Store: [0x800095f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008b4]:feq.h t6, ft11, ft10
	-[0x800008b8]:csrrs a0, fcsr, zero
	-[0x800008bc]:sw t6, 272(t1)
Current Store : [0x800008c0] : sw a0, 276(t1) -- Store: [0x800095f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008d4]:feq.h t6, ft11, ft10
	-[0x800008d8]:csrrs a0, fcsr, zero
	-[0x800008dc]:sw t6, 280(t1)
Current Store : [0x800008e0] : sw a0, 284(t1) -- Store: [0x80009600]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800008f4]:feq.h t6, ft11, ft10
	-[0x800008f8]:csrrs a0, fcsr, zero
	-[0x800008fc]:sw t6, 288(t1)
Current Store : [0x80000900] : sw a0, 292(t1) -- Store: [0x80009608]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000914]:feq.h t6, ft11, ft10
	-[0x80000918]:csrrs a0, fcsr, zero
	-[0x8000091c]:sw t6, 296(t1)
Current Store : [0x80000920] : sw a0, 300(t1) -- Store: [0x80009610]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000934]:feq.h t6, ft11, ft10
	-[0x80000938]:csrrs a0, fcsr, zero
	-[0x8000093c]:sw t6, 304(t1)
Current Store : [0x80000940] : sw a0, 308(t1) -- Store: [0x80009618]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000954]:feq.h t6, ft11, ft10
	-[0x80000958]:csrrs a0, fcsr, zero
	-[0x8000095c]:sw t6, 312(t1)
Current Store : [0x80000960] : sw a0, 316(t1) -- Store: [0x80009620]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000974]:feq.h t6, ft11, ft10
	-[0x80000978]:csrrs a0, fcsr, zero
	-[0x8000097c]:sw t6, 320(t1)
Current Store : [0x80000980] : sw a0, 324(t1) -- Store: [0x80009628]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000994]:feq.h t6, ft11, ft10
	-[0x80000998]:csrrs a0, fcsr, zero
	-[0x8000099c]:sw t6, 328(t1)
Current Store : [0x800009a0] : sw a0, 332(t1) -- Store: [0x80009630]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800009b4]:feq.h t6, ft11, ft10
	-[0x800009b8]:csrrs a0, fcsr, zero
	-[0x800009bc]:sw t6, 336(t1)
Current Store : [0x800009c0] : sw a0, 340(t1) -- Store: [0x80009638]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800009d4]:feq.h t6, ft11, ft10
	-[0x800009d8]:csrrs a0, fcsr, zero
	-[0x800009dc]:sw t6, 344(t1)
Current Store : [0x800009e0] : sw a0, 348(t1) -- Store: [0x80009640]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800009f4]:feq.h t6, ft11, ft10
	-[0x800009f8]:csrrs a0, fcsr, zero
	-[0x800009fc]:sw t6, 352(t1)
Current Store : [0x80000a00] : sw a0, 356(t1) -- Store: [0x80009648]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a14]:feq.h t6, ft11, ft10
	-[0x80000a18]:csrrs a0, fcsr, zero
	-[0x80000a1c]:sw t6, 360(t1)
Current Store : [0x80000a20] : sw a0, 364(t1) -- Store: [0x80009650]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a34]:feq.h t6, ft11, ft10
	-[0x80000a38]:csrrs a0, fcsr, zero
	-[0x80000a3c]:sw t6, 368(t1)
Current Store : [0x80000a40] : sw a0, 372(t1) -- Store: [0x80009658]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a54]:feq.h t6, ft11, ft10
	-[0x80000a58]:csrrs a0, fcsr, zero
	-[0x80000a5c]:sw t6, 376(t1)
Current Store : [0x80000a60] : sw a0, 380(t1) -- Store: [0x80009660]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a74]:feq.h t6, ft11, ft10
	-[0x80000a78]:csrrs a0, fcsr, zero
	-[0x80000a7c]:sw t6, 384(t1)
Current Store : [0x80000a80] : sw a0, 388(t1) -- Store: [0x80009668]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000a94]:feq.h t6, ft11, ft10
	-[0x80000a98]:csrrs a0, fcsr, zero
	-[0x80000a9c]:sw t6, 392(t1)
Current Store : [0x80000aa0] : sw a0, 396(t1) -- Store: [0x80009670]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ab4]:feq.h t6, ft11, ft10
	-[0x80000ab8]:csrrs a0, fcsr, zero
	-[0x80000abc]:sw t6, 400(t1)
Current Store : [0x80000ac0] : sw a0, 404(t1) -- Store: [0x80009678]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ad4]:feq.h t6, ft11, ft10
	-[0x80000ad8]:csrrs a0, fcsr, zero
	-[0x80000adc]:sw t6, 408(t1)
Current Store : [0x80000ae0] : sw a0, 412(t1) -- Store: [0x80009680]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000af4]:feq.h t6, ft11, ft10
	-[0x80000af8]:csrrs a0, fcsr, zero
	-[0x80000afc]:sw t6, 416(t1)
Current Store : [0x80000b00] : sw a0, 420(t1) -- Store: [0x80009688]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b14]:feq.h t6, ft11, ft10
	-[0x80000b18]:csrrs a0, fcsr, zero
	-[0x80000b1c]:sw t6, 424(t1)
Current Store : [0x80000b20] : sw a0, 428(t1) -- Store: [0x80009690]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b34]:feq.h t6, ft11, ft10
	-[0x80000b38]:csrrs a0, fcsr, zero
	-[0x80000b3c]:sw t6, 432(t1)
Current Store : [0x80000b40] : sw a0, 436(t1) -- Store: [0x80009698]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b54]:feq.h t6, ft11, ft10
	-[0x80000b58]:csrrs a0, fcsr, zero
	-[0x80000b5c]:sw t6, 440(t1)
Current Store : [0x80000b60] : sw a0, 444(t1) -- Store: [0x800096a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b74]:feq.h t6, ft11, ft10
	-[0x80000b78]:csrrs a0, fcsr, zero
	-[0x80000b7c]:sw t6, 448(t1)
Current Store : [0x80000b80] : sw a0, 452(t1) -- Store: [0x800096a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000b94]:feq.h t6, ft11, ft10
	-[0x80000b98]:csrrs a0, fcsr, zero
	-[0x80000b9c]:sw t6, 456(t1)
Current Store : [0x80000ba0] : sw a0, 460(t1) -- Store: [0x800096b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000bb4]:feq.h t6, ft11, ft10
	-[0x80000bb8]:csrrs a0, fcsr, zero
	-[0x80000bbc]:sw t6, 464(t1)
Current Store : [0x80000bc0] : sw a0, 468(t1) -- Store: [0x800096b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000bd4]:feq.h t6, ft11, ft10
	-[0x80000bd8]:csrrs a0, fcsr, zero
	-[0x80000bdc]:sw t6, 472(t1)
Current Store : [0x80000be0] : sw a0, 476(t1) -- Store: [0x800096c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000bf4]:feq.h t6, ft11, ft10
	-[0x80000bf8]:csrrs a0, fcsr, zero
	-[0x80000bfc]:sw t6, 480(t1)
Current Store : [0x80000c00] : sw a0, 484(t1) -- Store: [0x800096c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c14]:feq.h t6, ft11, ft10
	-[0x80000c18]:csrrs a0, fcsr, zero
	-[0x80000c1c]:sw t6, 488(t1)
Current Store : [0x80000c20] : sw a0, 492(t1) -- Store: [0x800096d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c34]:feq.h t6, ft11, ft10
	-[0x80000c38]:csrrs a0, fcsr, zero
	-[0x80000c3c]:sw t6, 496(t1)
Current Store : [0x80000c40] : sw a0, 500(t1) -- Store: [0x800096d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c54]:feq.h t6, ft11, ft10
	-[0x80000c58]:csrrs a0, fcsr, zero
	-[0x80000c5c]:sw t6, 504(t1)
Current Store : [0x80000c60] : sw a0, 508(t1) -- Store: [0x800096e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c74]:feq.h t6, ft11, ft10
	-[0x80000c78]:csrrs a0, fcsr, zero
	-[0x80000c7c]:sw t6, 512(t1)
Current Store : [0x80000c80] : sw a0, 516(t1) -- Store: [0x800096e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000c94]:feq.h t6, ft11, ft10
	-[0x80000c98]:csrrs a0, fcsr, zero
	-[0x80000c9c]:sw t6, 520(t1)
Current Store : [0x80000ca0] : sw a0, 524(t1) -- Store: [0x800096f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000cb4]:feq.h t6, ft11, ft10
	-[0x80000cb8]:csrrs a0, fcsr, zero
	-[0x80000cbc]:sw t6, 528(t1)
Current Store : [0x80000cc0] : sw a0, 532(t1) -- Store: [0x800096f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000cd4]:feq.h t6, ft11, ft10
	-[0x80000cd8]:csrrs a0, fcsr, zero
	-[0x80000cdc]:sw t6, 536(t1)
Current Store : [0x80000ce0] : sw a0, 540(t1) -- Store: [0x80009700]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000cf4]:feq.h t6, ft11, ft10
	-[0x80000cf8]:csrrs a0, fcsr, zero
	-[0x80000cfc]:sw t6, 544(t1)
Current Store : [0x80000d00] : sw a0, 548(t1) -- Store: [0x80009708]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d14]:feq.h t6, ft11, ft10
	-[0x80000d18]:csrrs a0, fcsr, zero
	-[0x80000d1c]:sw t6, 552(t1)
Current Store : [0x80000d20] : sw a0, 556(t1) -- Store: [0x80009710]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d34]:feq.h t6, ft11, ft10
	-[0x80000d38]:csrrs a0, fcsr, zero
	-[0x80000d3c]:sw t6, 560(t1)
Current Store : [0x80000d40] : sw a0, 564(t1) -- Store: [0x80009718]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d54]:feq.h t6, ft11, ft10
	-[0x80000d58]:csrrs a0, fcsr, zero
	-[0x80000d5c]:sw t6, 568(t1)
Current Store : [0x80000d60] : sw a0, 572(t1) -- Store: [0x80009720]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d74]:feq.h t6, ft11, ft10
	-[0x80000d78]:csrrs a0, fcsr, zero
	-[0x80000d7c]:sw t6, 576(t1)
Current Store : [0x80000d80] : sw a0, 580(t1) -- Store: [0x80009728]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000d94]:feq.h t6, ft11, ft10
	-[0x80000d98]:csrrs a0, fcsr, zero
	-[0x80000d9c]:sw t6, 584(t1)
Current Store : [0x80000da0] : sw a0, 588(t1) -- Store: [0x80009730]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000db4]:feq.h t6, ft11, ft10
	-[0x80000db8]:csrrs a0, fcsr, zero
	-[0x80000dbc]:sw t6, 592(t1)
Current Store : [0x80000dc0] : sw a0, 596(t1) -- Store: [0x80009738]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000dd4]:feq.h t6, ft11, ft10
	-[0x80000dd8]:csrrs a0, fcsr, zero
	-[0x80000ddc]:sw t6, 600(t1)
Current Store : [0x80000de0] : sw a0, 604(t1) -- Store: [0x80009740]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000df4]:feq.h t6, ft11, ft10
	-[0x80000df8]:csrrs a0, fcsr, zero
	-[0x80000dfc]:sw t6, 608(t1)
Current Store : [0x80000e00] : sw a0, 612(t1) -- Store: [0x80009748]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e14]:feq.h t6, ft11, ft10
	-[0x80000e18]:csrrs a0, fcsr, zero
	-[0x80000e1c]:sw t6, 616(t1)
Current Store : [0x80000e20] : sw a0, 620(t1) -- Store: [0x80009750]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e34]:feq.h t6, ft11, ft10
	-[0x80000e38]:csrrs a0, fcsr, zero
	-[0x80000e3c]:sw t6, 624(t1)
Current Store : [0x80000e40] : sw a0, 628(t1) -- Store: [0x80009758]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e54]:feq.h t6, ft11, ft10
	-[0x80000e58]:csrrs a0, fcsr, zero
	-[0x80000e5c]:sw t6, 632(t1)
Current Store : [0x80000e60] : sw a0, 636(t1) -- Store: [0x80009760]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e74]:feq.h t6, ft11, ft10
	-[0x80000e78]:csrrs a0, fcsr, zero
	-[0x80000e7c]:sw t6, 640(t1)
Current Store : [0x80000e80] : sw a0, 644(t1) -- Store: [0x80009768]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000e94]:feq.h t6, ft11, ft10
	-[0x80000e98]:csrrs a0, fcsr, zero
	-[0x80000e9c]:sw t6, 648(t1)
Current Store : [0x80000ea0] : sw a0, 652(t1) -- Store: [0x80009770]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000eb4]:feq.h t6, ft11, ft10
	-[0x80000eb8]:csrrs a0, fcsr, zero
	-[0x80000ebc]:sw t6, 656(t1)
Current Store : [0x80000ec0] : sw a0, 660(t1) -- Store: [0x80009778]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ed4]:feq.h t6, ft11, ft10
	-[0x80000ed8]:csrrs a0, fcsr, zero
	-[0x80000edc]:sw t6, 664(t1)
Current Store : [0x80000ee0] : sw a0, 668(t1) -- Store: [0x80009780]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ef4]:feq.h t6, ft11, ft10
	-[0x80000ef8]:csrrs a0, fcsr, zero
	-[0x80000efc]:sw t6, 672(t1)
Current Store : [0x80000f00] : sw a0, 676(t1) -- Store: [0x80009788]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f14]:feq.h t6, ft11, ft10
	-[0x80000f18]:csrrs a0, fcsr, zero
	-[0x80000f1c]:sw t6, 680(t1)
Current Store : [0x80000f20] : sw a0, 684(t1) -- Store: [0x80009790]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f34]:feq.h t6, ft11, ft10
	-[0x80000f38]:csrrs a0, fcsr, zero
	-[0x80000f3c]:sw t6, 688(t1)
Current Store : [0x80000f40] : sw a0, 692(t1) -- Store: [0x80009798]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f54]:feq.h t6, ft11, ft10
	-[0x80000f58]:csrrs a0, fcsr, zero
	-[0x80000f5c]:sw t6, 696(t1)
Current Store : [0x80000f60] : sw a0, 700(t1) -- Store: [0x800097a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f74]:feq.h t6, ft11, ft10
	-[0x80000f78]:csrrs a0, fcsr, zero
	-[0x80000f7c]:sw t6, 704(t1)
Current Store : [0x80000f80] : sw a0, 708(t1) -- Store: [0x800097a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000f94]:feq.h t6, ft11, ft10
	-[0x80000f98]:csrrs a0, fcsr, zero
	-[0x80000f9c]:sw t6, 712(t1)
Current Store : [0x80000fa0] : sw a0, 716(t1) -- Store: [0x800097b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000fb4]:feq.h t6, ft11, ft10
	-[0x80000fb8]:csrrs a0, fcsr, zero
	-[0x80000fbc]:sw t6, 720(t1)
Current Store : [0x80000fc0] : sw a0, 724(t1) -- Store: [0x800097b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000fd4]:feq.h t6, ft11, ft10
	-[0x80000fd8]:csrrs a0, fcsr, zero
	-[0x80000fdc]:sw t6, 728(t1)
Current Store : [0x80000fe0] : sw a0, 732(t1) -- Store: [0x800097c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80000ff4]:feq.h t6, ft11, ft10
	-[0x80000ff8]:csrrs a0, fcsr, zero
	-[0x80000ffc]:sw t6, 736(t1)
Current Store : [0x80001000] : sw a0, 740(t1) -- Store: [0x800097c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001014]:feq.h t6, ft11, ft10
	-[0x80001018]:csrrs a0, fcsr, zero
	-[0x8000101c]:sw t6, 744(t1)
Current Store : [0x80001020] : sw a0, 748(t1) -- Store: [0x800097d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001034]:feq.h t6, ft11, ft10
	-[0x80001038]:csrrs a0, fcsr, zero
	-[0x8000103c]:sw t6, 752(t1)
Current Store : [0x80001040] : sw a0, 756(t1) -- Store: [0x800097d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001054]:feq.h t6, ft11, ft10
	-[0x80001058]:csrrs a0, fcsr, zero
	-[0x8000105c]:sw t6, 760(t1)
Current Store : [0x80001060] : sw a0, 764(t1) -- Store: [0x800097e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001074]:feq.h t6, ft11, ft10
	-[0x80001078]:csrrs a0, fcsr, zero
	-[0x8000107c]:sw t6, 768(t1)
Current Store : [0x80001080] : sw a0, 772(t1) -- Store: [0x800097e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001094]:feq.h t6, ft11, ft10
	-[0x80001098]:csrrs a0, fcsr, zero
	-[0x8000109c]:sw t6, 776(t1)
Current Store : [0x800010a0] : sw a0, 780(t1) -- Store: [0x800097f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800010b4]:feq.h t6, ft11, ft10
	-[0x800010b8]:csrrs a0, fcsr, zero
	-[0x800010bc]:sw t6, 784(t1)
Current Store : [0x800010c0] : sw a0, 788(t1) -- Store: [0x800097f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800010d4]:feq.h t6, ft11, ft10
	-[0x800010d8]:csrrs a0, fcsr, zero
	-[0x800010dc]:sw t6, 792(t1)
Current Store : [0x800010e0] : sw a0, 796(t1) -- Store: [0x80009800]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800010f4]:feq.h t6, ft11, ft10
	-[0x800010f8]:csrrs a0, fcsr, zero
	-[0x800010fc]:sw t6, 800(t1)
Current Store : [0x80001100] : sw a0, 804(t1) -- Store: [0x80009808]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001114]:feq.h t6, ft11, ft10
	-[0x80001118]:csrrs a0, fcsr, zero
	-[0x8000111c]:sw t6, 808(t1)
Current Store : [0x80001120] : sw a0, 812(t1) -- Store: [0x80009810]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001134]:feq.h t6, ft11, ft10
	-[0x80001138]:csrrs a0, fcsr, zero
	-[0x8000113c]:sw t6, 816(t1)
Current Store : [0x80001140] : sw a0, 820(t1) -- Store: [0x80009818]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001154]:feq.h t6, ft11, ft10
	-[0x80001158]:csrrs a0, fcsr, zero
	-[0x8000115c]:sw t6, 824(t1)
Current Store : [0x80001160] : sw a0, 828(t1) -- Store: [0x80009820]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001174]:feq.h t6, ft11, ft10
	-[0x80001178]:csrrs a0, fcsr, zero
	-[0x8000117c]:sw t6, 832(t1)
Current Store : [0x80001180] : sw a0, 836(t1) -- Store: [0x80009828]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001194]:feq.h t6, ft11, ft10
	-[0x80001198]:csrrs a0, fcsr, zero
	-[0x8000119c]:sw t6, 840(t1)
Current Store : [0x800011a0] : sw a0, 844(t1) -- Store: [0x80009830]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800011b4]:feq.h t6, ft11, ft10
	-[0x800011b8]:csrrs a0, fcsr, zero
	-[0x800011bc]:sw t6, 848(t1)
Current Store : [0x800011c0] : sw a0, 852(t1) -- Store: [0x80009838]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800011d4]:feq.h t6, ft11, ft10
	-[0x800011d8]:csrrs a0, fcsr, zero
	-[0x800011dc]:sw t6, 856(t1)
Current Store : [0x800011e0] : sw a0, 860(t1) -- Store: [0x80009840]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800011f4]:feq.h t6, ft11, ft10
	-[0x800011f8]:csrrs a0, fcsr, zero
	-[0x800011fc]:sw t6, 864(t1)
Current Store : [0x80001200] : sw a0, 868(t1) -- Store: [0x80009848]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001214]:feq.h t6, ft11, ft10
	-[0x80001218]:csrrs a0, fcsr, zero
	-[0x8000121c]:sw t6, 872(t1)
Current Store : [0x80001220] : sw a0, 876(t1) -- Store: [0x80009850]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001234]:feq.h t6, ft11, ft10
	-[0x80001238]:csrrs a0, fcsr, zero
	-[0x8000123c]:sw t6, 880(t1)
Current Store : [0x80001240] : sw a0, 884(t1) -- Store: [0x80009858]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001254]:feq.h t6, ft11, ft10
	-[0x80001258]:csrrs a0, fcsr, zero
	-[0x8000125c]:sw t6, 888(t1)
Current Store : [0x80001260] : sw a0, 892(t1) -- Store: [0x80009860]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001274]:feq.h t6, ft11, ft10
	-[0x80001278]:csrrs a0, fcsr, zero
	-[0x8000127c]:sw t6, 896(t1)
Current Store : [0x80001280] : sw a0, 900(t1) -- Store: [0x80009868]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001294]:feq.h t6, ft11, ft10
	-[0x80001298]:csrrs a0, fcsr, zero
	-[0x8000129c]:sw t6, 904(t1)
Current Store : [0x800012a0] : sw a0, 908(t1) -- Store: [0x80009870]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800012b4]:feq.h t6, ft11, ft10
	-[0x800012b8]:csrrs a0, fcsr, zero
	-[0x800012bc]:sw t6, 912(t1)
Current Store : [0x800012c0] : sw a0, 916(t1) -- Store: [0x80009878]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800012d4]:feq.h t6, ft11, ft10
	-[0x800012d8]:csrrs a0, fcsr, zero
	-[0x800012dc]:sw t6, 920(t1)
Current Store : [0x800012e0] : sw a0, 924(t1) -- Store: [0x80009880]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800012f4]:feq.h t6, ft11, ft10
	-[0x800012f8]:csrrs a0, fcsr, zero
	-[0x800012fc]:sw t6, 928(t1)
Current Store : [0x80001300] : sw a0, 932(t1) -- Store: [0x80009888]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001314]:feq.h t6, ft11, ft10
	-[0x80001318]:csrrs a0, fcsr, zero
	-[0x8000131c]:sw t6, 936(t1)
Current Store : [0x80001320] : sw a0, 940(t1) -- Store: [0x80009890]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001334]:feq.h t6, ft11, ft10
	-[0x80001338]:csrrs a0, fcsr, zero
	-[0x8000133c]:sw t6, 944(t1)
Current Store : [0x80001340] : sw a0, 948(t1) -- Store: [0x80009898]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001354]:feq.h t6, ft11, ft10
	-[0x80001358]:csrrs a0, fcsr, zero
	-[0x8000135c]:sw t6, 952(t1)
Current Store : [0x80001360] : sw a0, 956(t1) -- Store: [0x800098a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001374]:feq.h t6, ft11, ft10
	-[0x80001378]:csrrs a0, fcsr, zero
	-[0x8000137c]:sw t6, 960(t1)
Current Store : [0x80001380] : sw a0, 964(t1) -- Store: [0x800098a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001394]:feq.h t6, ft11, ft10
	-[0x80001398]:csrrs a0, fcsr, zero
	-[0x8000139c]:sw t6, 968(t1)
Current Store : [0x800013a0] : sw a0, 972(t1) -- Store: [0x800098b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800013b4]:feq.h t6, ft11, ft10
	-[0x800013b8]:csrrs a0, fcsr, zero
	-[0x800013bc]:sw t6, 976(t1)
Current Store : [0x800013c0] : sw a0, 980(t1) -- Store: [0x800098b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800013d4]:feq.h t6, ft11, ft10
	-[0x800013d8]:csrrs a0, fcsr, zero
	-[0x800013dc]:sw t6, 984(t1)
Current Store : [0x800013e0] : sw a0, 988(t1) -- Store: [0x800098c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800013f4]:feq.h t6, ft11, ft10
	-[0x800013f8]:csrrs a0, fcsr, zero
	-[0x800013fc]:sw t6, 992(t1)
Current Store : [0x80001400] : sw a0, 996(t1) -- Store: [0x800098c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001414]:feq.h t6, ft11, ft10
	-[0x80001418]:csrrs a0, fcsr, zero
	-[0x8000141c]:sw t6, 1000(t1)
Current Store : [0x80001420] : sw a0, 1004(t1) -- Store: [0x800098d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001434]:feq.h t6, ft11, ft10
	-[0x80001438]:csrrs a0, fcsr, zero
	-[0x8000143c]:sw t6, 1008(t1)
Current Store : [0x80001440] : sw a0, 1012(t1) -- Store: [0x800098d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001454]:feq.h t6, ft11, ft10
	-[0x80001458]:csrrs a0, fcsr, zero
	-[0x8000145c]:sw t6, 1016(t1)
Current Store : [0x80001460] : sw a0, 1020(t1) -- Store: [0x800098e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000147c]:feq.h t6, ft11, ft10
	-[0x80001480]:csrrs a0, fcsr, zero
	-[0x80001484]:sw t6, 0(t1)
Current Store : [0x80001488] : sw a0, 4(t1) -- Store: [0x800098e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000149c]:feq.h t6, ft11, ft10
	-[0x800014a0]:csrrs a0, fcsr, zero
	-[0x800014a4]:sw t6, 8(t1)
Current Store : [0x800014a8] : sw a0, 12(t1) -- Store: [0x800098f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800014bc]:feq.h t6, ft11, ft10
	-[0x800014c0]:csrrs a0, fcsr, zero
	-[0x800014c4]:sw t6, 16(t1)
Current Store : [0x800014c8] : sw a0, 20(t1) -- Store: [0x800098f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800014dc]:feq.h t6, ft11, ft10
	-[0x800014e0]:csrrs a0, fcsr, zero
	-[0x800014e4]:sw t6, 24(t1)
Current Store : [0x800014e8] : sw a0, 28(t1) -- Store: [0x80009900]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800014fc]:feq.h t6, ft11, ft10
	-[0x80001500]:csrrs a0, fcsr, zero
	-[0x80001504]:sw t6, 32(t1)
Current Store : [0x80001508] : sw a0, 36(t1) -- Store: [0x80009908]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000151c]:feq.h t6, ft11, ft10
	-[0x80001520]:csrrs a0, fcsr, zero
	-[0x80001524]:sw t6, 40(t1)
Current Store : [0x80001528] : sw a0, 44(t1) -- Store: [0x80009910]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000153c]:feq.h t6, ft11, ft10
	-[0x80001540]:csrrs a0, fcsr, zero
	-[0x80001544]:sw t6, 48(t1)
Current Store : [0x80001548] : sw a0, 52(t1) -- Store: [0x80009918]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000155c]:feq.h t6, ft11, ft10
	-[0x80001560]:csrrs a0, fcsr, zero
	-[0x80001564]:sw t6, 56(t1)
Current Store : [0x80001568] : sw a0, 60(t1) -- Store: [0x80009920]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000157c]:feq.h t6, ft11, ft10
	-[0x80001580]:csrrs a0, fcsr, zero
	-[0x80001584]:sw t6, 64(t1)
Current Store : [0x80001588] : sw a0, 68(t1) -- Store: [0x80009928]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000159c]:feq.h t6, ft11, ft10
	-[0x800015a0]:csrrs a0, fcsr, zero
	-[0x800015a4]:sw t6, 72(t1)
Current Store : [0x800015a8] : sw a0, 76(t1) -- Store: [0x80009930]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800015bc]:feq.h t6, ft11, ft10
	-[0x800015c0]:csrrs a0, fcsr, zero
	-[0x800015c4]:sw t6, 80(t1)
Current Store : [0x800015c8] : sw a0, 84(t1) -- Store: [0x80009938]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800015dc]:feq.h t6, ft11, ft10
	-[0x800015e0]:csrrs a0, fcsr, zero
	-[0x800015e4]:sw t6, 88(t1)
Current Store : [0x800015e8] : sw a0, 92(t1) -- Store: [0x80009940]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800015fc]:feq.h t6, ft11, ft10
	-[0x80001600]:csrrs a0, fcsr, zero
	-[0x80001604]:sw t6, 96(t1)
Current Store : [0x80001608] : sw a0, 100(t1) -- Store: [0x80009948]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000161c]:feq.h t6, ft11, ft10
	-[0x80001620]:csrrs a0, fcsr, zero
	-[0x80001624]:sw t6, 104(t1)
Current Store : [0x80001628] : sw a0, 108(t1) -- Store: [0x80009950]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000163c]:feq.h t6, ft11, ft10
	-[0x80001640]:csrrs a0, fcsr, zero
	-[0x80001644]:sw t6, 112(t1)
Current Store : [0x80001648] : sw a0, 116(t1) -- Store: [0x80009958]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000165c]:feq.h t6, ft11, ft10
	-[0x80001660]:csrrs a0, fcsr, zero
	-[0x80001664]:sw t6, 120(t1)
Current Store : [0x80001668] : sw a0, 124(t1) -- Store: [0x80009960]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000167c]:feq.h t6, ft11, ft10
	-[0x80001680]:csrrs a0, fcsr, zero
	-[0x80001684]:sw t6, 128(t1)
Current Store : [0x80001688] : sw a0, 132(t1) -- Store: [0x80009968]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000169c]:feq.h t6, ft11, ft10
	-[0x800016a0]:csrrs a0, fcsr, zero
	-[0x800016a4]:sw t6, 136(t1)
Current Store : [0x800016a8] : sw a0, 140(t1) -- Store: [0x80009970]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800016bc]:feq.h t6, ft11, ft10
	-[0x800016c0]:csrrs a0, fcsr, zero
	-[0x800016c4]:sw t6, 144(t1)
Current Store : [0x800016c8] : sw a0, 148(t1) -- Store: [0x80009978]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800016dc]:feq.h t6, ft11, ft10
	-[0x800016e0]:csrrs a0, fcsr, zero
	-[0x800016e4]:sw t6, 152(t1)
Current Store : [0x800016e8] : sw a0, 156(t1) -- Store: [0x80009980]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800016fc]:feq.h t6, ft11, ft10
	-[0x80001700]:csrrs a0, fcsr, zero
	-[0x80001704]:sw t6, 160(t1)
Current Store : [0x80001708] : sw a0, 164(t1) -- Store: [0x80009988]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000171c]:feq.h t6, ft11, ft10
	-[0x80001720]:csrrs a0, fcsr, zero
	-[0x80001724]:sw t6, 168(t1)
Current Store : [0x80001728] : sw a0, 172(t1) -- Store: [0x80009990]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000173c]:feq.h t6, ft11, ft10
	-[0x80001740]:csrrs a0, fcsr, zero
	-[0x80001744]:sw t6, 176(t1)
Current Store : [0x80001748] : sw a0, 180(t1) -- Store: [0x80009998]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000175c]:feq.h t6, ft11, ft10
	-[0x80001760]:csrrs a0, fcsr, zero
	-[0x80001764]:sw t6, 184(t1)
Current Store : [0x80001768] : sw a0, 188(t1) -- Store: [0x800099a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000177c]:feq.h t6, ft11, ft10
	-[0x80001780]:csrrs a0, fcsr, zero
	-[0x80001784]:sw t6, 192(t1)
Current Store : [0x80001788] : sw a0, 196(t1) -- Store: [0x800099a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000179c]:feq.h t6, ft11, ft10
	-[0x800017a0]:csrrs a0, fcsr, zero
	-[0x800017a4]:sw t6, 200(t1)
Current Store : [0x800017a8] : sw a0, 204(t1) -- Store: [0x800099b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800017bc]:feq.h t6, ft11, ft10
	-[0x800017c0]:csrrs a0, fcsr, zero
	-[0x800017c4]:sw t6, 208(t1)
Current Store : [0x800017c8] : sw a0, 212(t1) -- Store: [0x800099b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800017dc]:feq.h t6, ft11, ft10
	-[0x800017e0]:csrrs a0, fcsr, zero
	-[0x800017e4]:sw t6, 216(t1)
Current Store : [0x800017e8] : sw a0, 220(t1) -- Store: [0x800099c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800017fc]:feq.h t6, ft11, ft10
	-[0x80001800]:csrrs a0, fcsr, zero
	-[0x80001804]:sw t6, 224(t1)
Current Store : [0x80001808] : sw a0, 228(t1) -- Store: [0x800099c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000181c]:feq.h t6, ft11, ft10
	-[0x80001820]:csrrs a0, fcsr, zero
	-[0x80001824]:sw t6, 232(t1)
Current Store : [0x80001828] : sw a0, 236(t1) -- Store: [0x800099d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000183c]:feq.h t6, ft11, ft10
	-[0x80001840]:csrrs a0, fcsr, zero
	-[0x80001844]:sw t6, 240(t1)
Current Store : [0x80001848] : sw a0, 244(t1) -- Store: [0x800099d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000185c]:feq.h t6, ft11, ft10
	-[0x80001860]:csrrs a0, fcsr, zero
	-[0x80001864]:sw t6, 248(t1)
Current Store : [0x80001868] : sw a0, 252(t1) -- Store: [0x800099e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000187c]:feq.h t6, ft11, ft10
	-[0x80001880]:csrrs a0, fcsr, zero
	-[0x80001884]:sw t6, 256(t1)
Current Store : [0x80001888] : sw a0, 260(t1) -- Store: [0x800099e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000189c]:feq.h t6, ft11, ft10
	-[0x800018a0]:csrrs a0, fcsr, zero
	-[0x800018a4]:sw t6, 264(t1)
Current Store : [0x800018a8] : sw a0, 268(t1) -- Store: [0x800099f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800018bc]:feq.h t6, ft11, ft10
	-[0x800018c0]:csrrs a0, fcsr, zero
	-[0x800018c4]:sw t6, 272(t1)
Current Store : [0x800018c8] : sw a0, 276(t1) -- Store: [0x800099f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800018dc]:feq.h t6, ft11, ft10
	-[0x800018e0]:csrrs a0, fcsr, zero
	-[0x800018e4]:sw t6, 280(t1)
Current Store : [0x800018e8] : sw a0, 284(t1) -- Store: [0x80009a00]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800018fc]:feq.h t6, ft11, ft10
	-[0x80001900]:csrrs a0, fcsr, zero
	-[0x80001904]:sw t6, 288(t1)
Current Store : [0x80001908] : sw a0, 292(t1) -- Store: [0x80009a08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000191c]:feq.h t6, ft11, ft10
	-[0x80001920]:csrrs a0, fcsr, zero
	-[0x80001924]:sw t6, 296(t1)
Current Store : [0x80001928] : sw a0, 300(t1) -- Store: [0x80009a10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000193c]:feq.h t6, ft11, ft10
	-[0x80001940]:csrrs a0, fcsr, zero
	-[0x80001944]:sw t6, 304(t1)
Current Store : [0x80001948] : sw a0, 308(t1) -- Store: [0x80009a18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000195c]:feq.h t6, ft11, ft10
	-[0x80001960]:csrrs a0, fcsr, zero
	-[0x80001964]:sw t6, 312(t1)
Current Store : [0x80001968] : sw a0, 316(t1) -- Store: [0x80009a20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000197c]:feq.h t6, ft11, ft10
	-[0x80001980]:csrrs a0, fcsr, zero
	-[0x80001984]:sw t6, 320(t1)
Current Store : [0x80001988] : sw a0, 324(t1) -- Store: [0x80009a28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000199c]:feq.h t6, ft11, ft10
	-[0x800019a0]:csrrs a0, fcsr, zero
	-[0x800019a4]:sw t6, 328(t1)
Current Store : [0x800019a8] : sw a0, 332(t1) -- Store: [0x80009a30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800019bc]:feq.h t6, ft11, ft10
	-[0x800019c0]:csrrs a0, fcsr, zero
	-[0x800019c4]:sw t6, 336(t1)
Current Store : [0x800019c8] : sw a0, 340(t1) -- Store: [0x80009a38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800019dc]:feq.h t6, ft11, ft10
	-[0x800019e0]:csrrs a0, fcsr, zero
	-[0x800019e4]:sw t6, 344(t1)
Current Store : [0x800019e8] : sw a0, 348(t1) -- Store: [0x80009a40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800019fc]:feq.h t6, ft11, ft10
	-[0x80001a00]:csrrs a0, fcsr, zero
	-[0x80001a04]:sw t6, 352(t1)
Current Store : [0x80001a08] : sw a0, 356(t1) -- Store: [0x80009a48]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a1c]:feq.h t6, ft11, ft10
	-[0x80001a20]:csrrs a0, fcsr, zero
	-[0x80001a24]:sw t6, 360(t1)
Current Store : [0x80001a28] : sw a0, 364(t1) -- Store: [0x80009a50]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a3c]:feq.h t6, ft11, ft10
	-[0x80001a40]:csrrs a0, fcsr, zero
	-[0x80001a44]:sw t6, 368(t1)
Current Store : [0x80001a48] : sw a0, 372(t1) -- Store: [0x80009a58]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a5c]:feq.h t6, ft11, ft10
	-[0x80001a60]:csrrs a0, fcsr, zero
	-[0x80001a64]:sw t6, 376(t1)
Current Store : [0x80001a68] : sw a0, 380(t1) -- Store: [0x80009a60]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a7c]:feq.h t6, ft11, ft10
	-[0x80001a80]:csrrs a0, fcsr, zero
	-[0x80001a84]:sw t6, 384(t1)
Current Store : [0x80001a88] : sw a0, 388(t1) -- Store: [0x80009a68]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001a9c]:feq.h t6, ft11, ft10
	-[0x80001aa0]:csrrs a0, fcsr, zero
	-[0x80001aa4]:sw t6, 392(t1)
Current Store : [0x80001aa8] : sw a0, 396(t1) -- Store: [0x80009a70]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001abc]:feq.h t6, ft11, ft10
	-[0x80001ac0]:csrrs a0, fcsr, zero
	-[0x80001ac4]:sw t6, 400(t1)
Current Store : [0x80001ac8] : sw a0, 404(t1) -- Store: [0x80009a78]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001adc]:feq.h t6, ft11, ft10
	-[0x80001ae0]:csrrs a0, fcsr, zero
	-[0x80001ae4]:sw t6, 408(t1)
Current Store : [0x80001ae8] : sw a0, 412(t1) -- Store: [0x80009a80]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001afc]:feq.h t6, ft11, ft10
	-[0x80001b00]:csrrs a0, fcsr, zero
	-[0x80001b04]:sw t6, 416(t1)
Current Store : [0x80001b08] : sw a0, 420(t1) -- Store: [0x80009a88]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b1c]:feq.h t6, ft11, ft10
	-[0x80001b20]:csrrs a0, fcsr, zero
	-[0x80001b24]:sw t6, 424(t1)
Current Store : [0x80001b28] : sw a0, 428(t1) -- Store: [0x80009a90]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b3c]:feq.h t6, ft11, ft10
	-[0x80001b40]:csrrs a0, fcsr, zero
	-[0x80001b44]:sw t6, 432(t1)
Current Store : [0x80001b48] : sw a0, 436(t1) -- Store: [0x80009a98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b5c]:feq.h t6, ft11, ft10
	-[0x80001b60]:csrrs a0, fcsr, zero
	-[0x80001b64]:sw t6, 440(t1)
Current Store : [0x80001b68] : sw a0, 444(t1) -- Store: [0x80009aa0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b7c]:feq.h t6, ft11, ft10
	-[0x80001b80]:csrrs a0, fcsr, zero
	-[0x80001b84]:sw t6, 448(t1)
Current Store : [0x80001b88] : sw a0, 452(t1) -- Store: [0x80009aa8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001b9c]:feq.h t6, ft11, ft10
	-[0x80001ba0]:csrrs a0, fcsr, zero
	-[0x80001ba4]:sw t6, 456(t1)
Current Store : [0x80001ba8] : sw a0, 460(t1) -- Store: [0x80009ab0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001bbc]:feq.h t6, ft11, ft10
	-[0x80001bc0]:csrrs a0, fcsr, zero
	-[0x80001bc4]:sw t6, 464(t1)
Current Store : [0x80001bc8] : sw a0, 468(t1) -- Store: [0x80009ab8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001bdc]:feq.h t6, ft11, ft10
	-[0x80001be0]:csrrs a0, fcsr, zero
	-[0x80001be4]:sw t6, 472(t1)
Current Store : [0x80001be8] : sw a0, 476(t1) -- Store: [0x80009ac0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001bfc]:feq.h t6, ft11, ft10
	-[0x80001c00]:csrrs a0, fcsr, zero
	-[0x80001c04]:sw t6, 480(t1)
Current Store : [0x80001c08] : sw a0, 484(t1) -- Store: [0x80009ac8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c1c]:feq.h t6, ft11, ft10
	-[0x80001c20]:csrrs a0, fcsr, zero
	-[0x80001c24]:sw t6, 488(t1)
Current Store : [0x80001c28] : sw a0, 492(t1) -- Store: [0x80009ad0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c3c]:feq.h t6, ft11, ft10
	-[0x80001c40]:csrrs a0, fcsr, zero
	-[0x80001c44]:sw t6, 496(t1)
Current Store : [0x80001c48] : sw a0, 500(t1) -- Store: [0x80009ad8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c5c]:feq.h t6, ft11, ft10
	-[0x80001c60]:csrrs a0, fcsr, zero
	-[0x80001c64]:sw t6, 504(t1)
Current Store : [0x80001c68] : sw a0, 508(t1) -- Store: [0x80009ae0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c7c]:feq.h t6, ft11, ft10
	-[0x80001c80]:csrrs a0, fcsr, zero
	-[0x80001c84]:sw t6, 512(t1)
Current Store : [0x80001c88] : sw a0, 516(t1) -- Store: [0x80009ae8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001c9c]:feq.h t6, ft11, ft10
	-[0x80001ca0]:csrrs a0, fcsr, zero
	-[0x80001ca4]:sw t6, 520(t1)
Current Store : [0x80001ca8] : sw a0, 524(t1) -- Store: [0x80009af0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001cbc]:feq.h t6, ft11, ft10
	-[0x80001cc0]:csrrs a0, fcsr, zero
	-[0x80001cc4]:sw t6, 528(t1)
Current Store : [0x80001cc8] : sw a0, 532(t1) -- Store: [0x80009af8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001cdc]:feq.h t6, ft11, ft10
	-[0x80001ce0]:csrrs a0, fcsr, zero
	-[0x80001ce4]:sw t6, 536(t1)
Current Store : [0x80001ce8] : sw a0, 540(t1) -- Store: [0x80009b00]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001cfc]:feq.h t6, ft11, ft10
	-[0x80001d00]:csrrs a0, fcsr, zero
	-[0x80001d04]:sw t6, 544(t1)
Current Store : [0x80001d08] : sw a0, 548(t1) -- Store: [0x80009b08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d1c]:feq.h t6, ft11, ft10
	-[0x80001d20]:csrrs a0, fcsr, zero
	-[0x80001d24]:sw t6, 552(t1)
Current Store : [0x80001d28] : sw a0, 556(t1) -- Store: [0x80009b10]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d3c]:feq.h t6, ft11, ft10
	-[0x80001d40]:csrrs a0, fcsr, zero
	-[0x80001d44]:sw t6, 560(t1)
Current Store : [0x80001d48] : sw a0, 564(t1) -- Store: [0x80009b18]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d5c]:feq.h t6, ft11, ft10
	-[0x80001d60]:csrrs a0, fcsr, zero
	-[0x80001d64]:sw t6, 568(t1)
Current Store : [0x80001d68] : sw a0, 572(t1) -- Store: [0x80009b20]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d7c]:feq.h t6, ft11, ft10
	-[0x80001d80]:csrrs a0, fcsr, zero
	-[0x80001d84]:sw t6, 576(t1)
Current Store : [0x80001d88] : sw a0, 580(t1) -- Store: [0x80009b28]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001d9c]:feq.h t6, ft11, ft10
	-[0x80001da0]:csrrs a0, fcsr, zero
	-[0x80001da4]:sw t6, 584(t1)
Current Store : [0x80001da8] : sw a0, 588(t1) -- Store: [0x80009b30]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001dbc]:feq.h t6, ft11, ft10
	-[0x80001dc0]:csrrs a0, fcsr, zero
	-[0x80001dc4]:sw t6, 592(t1)
Current Store : [0x80001dc8] : sw a0, 596(t1) -- Store: [0x80009b38]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001ddc]:feq.h t6, ft11, ft10
	-[0x80001de0]:csrrs a0, fcsr, zero
	-[0x80001de4]:sw t6, 600(t1)
Current Store : [0x80001de8] : sw a0, 604(t1) -- Store: [0x80009b40]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001dfc]:feq.h t6, ft11, ft10
	-[0x80001e00]:csrrs a0, fcsr, zero
	-[0x80001e04]:sw t6, 608(t1)
Current Store : [0x80001e08] : sw a0, 612(t1) -- Store: [0x80009b48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e1c]:feq.h t6, ft11, ft10
	-[0x80001e20]:csrrs a0, fcsr, zero
	-[0x80001e24]:sw t6, 616(t1)
Current Store : [0x80001e28] : sw a0, 620(t1) -- Store: [0x80009b50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e3c]:feq.h t6, ft11, ft10
	-[0x80001e40]:csrrs a0, fcsr, zero
	-[0x80001e44]:sw t6, 624(t1)
Current Store : [0x80001e48] : sw a0, 628(t1) -- Store: [0x80009b58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e5c]:feq.h t6, ft11, ft10
	-[0x80001e60]:csrrs a0, fcsr, zero
	-[0x80001e64]:sw t6, 632(t1)
Current Store : [0x80001e68] : sw a0, 636(t1) -- Store: [0x80009b60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e7c]:feq.h t6, ft11, ft10
	-[0x80001e80]:csrrs a0, fcsr, zero
	-[0x80001e84]:sw t6, 640(t1)
Current Store : [0x80001e88] : sw a0, 644(t1) -- Store: [0x80009b68]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001e9c]:feq.h t6, ft11, ft10
	-[0x80001ea0]:csrrs a0, fcsr, zero
	-[0x80001ea4]:sw t6, 648(t1)
Current Store : [0x80001ea8] : sw a0, 652(t1) -- Store: [0x80009b70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001ebc]:feq.h t6, ft11, ft10
	-[0x80001ec0]:csrrs a0, fcsr, zero
	-[0x80001ec4]:sw t6, 656(t1)
Current Store : [0x80001ec8] : sw a0, 660(t1) -- Store: [0x80009b78]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001edc]:feq.h t6, ft11, ft10
	-[0x80001ee0]:csrrs a0, fcsr, zero
	-[0x80001ee4]:sw t6, 664(t1)
Current Store : [0x80001ee8] : sw a0, 668(t1) -- Store: [0x80009b80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001efc]:feq.h t6, ft11, ft10
	-[0x80001f00]:csrrs a0, fcsr, zero
	-[0x80001f04]:sw t6, 672(t1)
Current Store : [0x80001f08] : sw a0, 676(t1) -- Store: [0x80009b88]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f1c]:feq.h t6, ft11, ft10
	-[0x80001f20]:csrrs a0, fcsr, zero
	-[0x80001f24]:sw t6, 680(t1)
Current Store : [0x80001f28] : sw a0, 684(t1) -- Store: [0x80009b90]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f3c]:feq.h t6, ft11, ft10
	-[0x80001f40]:csrrs a0, fcsr, zero
	-[0x80001f44]:sw t6, 688(t1)
Current Store : [0x80001f48] : sw a0, 692(t1) -- Store: [0x80009b98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f5c]:feq.h t6, ft11, ft10
	-[0x80001f60]:csrrs a0, fcsr, zero
	-[0x80001f64]:sw t6, 696(t1)
Current Store : [0x80001f68] : sw a0, 700(t1) -- Store: [0x80009ba0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f7c]:feq.h t6, ft11, ft10
	-[0x80001f80]:csrrs a0, fcsr, zero
	-[0x80001f84]:sw t6, 704(t1)
Current Store : [0x80001f88] : sw a0, 708(t1) -- Store: [0x80009ba8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001f9c]:feq.h t6, ft11, ft10
	-[0x80001fa0]:csrrs a0, fcsr, zero
	-[0x80001fa4]:sw t6, 712(t1)
Current Store : [0x80001fa8] : sw a0, 716(t1) -- Store: [0x80009bb0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001fbc]:feq.h t6, ft11, ft10
	-[0x80001fc0]:csrrs a0, fcsr, zero
	-[0x80001fc4]:sw t6, 720(t1)
Current Store : [0x80001fc8] : sw a0, 724(t1) -- Store: [0x80009bb8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001fdc]:feq.h t6, ft11, ft10
	-[0x80001fe0]:csrrs a0, fcsr, zero
	-[0x80001fe4]:sw t6, 728(t1)
Current Store : [0x80001fe8] : sw a0, 732(t1) -- Store: [0x80009bc0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80001ffc]:feq.h t6, ft11, ft10
	-[0x80002000]:csrrs a0, fcsr, zero
	-[0x80002004]:sw t6, 736(t1)
Current Store : [0x80002008] : sw a0, 740(t1) -- Store: [0x80009bc8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000201c]:feq.h t6, ft11, ft10
	-[0x80002020]:csrrs a0, fcsr, zero
	-[0x80002024]:sw t6, 744(t1)
Current Store : [0x80002028] : sw a0, 748(t1) -- Store: [0x80009bd0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000203c]:feq.h t6, ft11, ft10
	-[0x80002040]:csrrs a0, fcsr, zero
	-[0x80002044]:sw t6, 752(t1)
Current Store : [0x80002048] : sw a0, 756(t1) -- Store: [0x80009bd8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000205c]:feq.h t6, ft11, ft10
	-[0x80002060]:csrrs a0, fcsr, zero
	-[0x80002064]:sw t6, 760(t1)
Current Store : [0x80002068] : sw a0, 764(t1) -- Store: [0x80009be0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000207c]:feq.h t6, ft11, ft10
	-[0x80002080]:csrrs a0, fcsr, zero
	-[0x80002084]:sw t6, 768(t1)
Current Store : [0x80002088] : sw a0, 772(t1) -- Store: [0x80009be8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000209c]:feq.h t6, ft11, ft10
	-[0x800020a0]:csrrs a0, fcsr, zero
	-[0x800020a4]:sw t6, 776(t1)
Current Store : [0x800020a8] : sw a0, 780(t1) -- Store: [0x80009bf0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800020bc]:feq.h t6, ft11, ft10
	-[0x800020c0]:csrrs a0, fcsr, zero
	-[0x800020c4]:sw t6, 784(t1)
Current Store : [0x800020c8] : sw a0, 788(t1) -- Store: [0x80009bf8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800020dc]:feq.h t6, ft11, ft10
	-[0x800020e0]:csrrs a0, fcsr, zero
	-[0x800020e4]:sw t6, 792(t1)
Current Store : [0x800020e8] : sw a0, 796(t1) -- Store: [0x80009c00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800020fc]:feq.h t6, ft11, ft10
	-[0x80002100]:csrrs a0, fcsr, zero
	-[0x80002104]:sw t6, 800(t1)
Current Store : [0x80002108] : sw a0, 804(t1) -- Store: [0x80009c08]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000211c]:feq.h t6, ft11, ft10
	-[0x80002120]:csrrs a0, fcsr, zero
	-[0x80002124]:sw t6, 808(t1)
Current Store : [0x80002128] : sw a0, 812(t1) -- Store: [0x80009c10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000213c]:feq.h t6, ft11, ft10
	-[0x80002140]:csrrs a0, fcsr, zero
	-[0x80002144]:sw t6, 816(t1)
Current Store : [0x80002148] : sw a0, 820(t1) -- Store: [0x80009c18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000215c]:feq.h t6, ft11, ft10
	-[0x80002160]:csrrs a0, fcsr, zero
	-[0x80002164]:sw t6, 824(t1)
Current Store : [0x80002168] : sw a0, 828(t1) -- Store: [0x80009c20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000217c]:feq.h t6, ft11, ft10
	-[0x80002180]:csrrs a0, fcsr, zero
	-[0x80002184]:sw t6, 832(t1)
Current Store : [0x80002188] : sw a0, 836(t1) -- Store: [0x80009c28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000219c]:feq.h t6, ft11, ft10
	-[0x800021a0]:csrrs a0, fcsr, zero
	-[0x800021a4]:sw t6, 840(t1)
Current Store : [0x800021a8] : sw a0, 844(t1) -- Store: [0x80009c30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800021bc]:feq.h t6, ft11, ft10
	-[0x800021c0]:csrrs a0, fcsr, zero
	-[0x800021c4]:sw t6, 848(t1)
Current Store : [0x800021c8] : sw a0, 852(t1) -- Store: [0x80009c38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800021dc]:feq.h t6, ft11, ft10
	-[0x800021e0]:csrrs a0, fcsr, zero
	-[0x800021e4]:sw t6, 856(t1)
Current Store : [0x800021e8] : sw a0, 860(t1) -- Store: [0x80009c40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800021fc]:feq.h t6, ft11, ft10
	-[0x80002200]:csrrs a0, fcsr, zero
	-[0x80002204]:sw t6, 864(t1)
Current Store : [0x80002208] : sw a0, 868(t1) -- Store: [0x80009c48]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000221c]:feq.h t6, ft11, ft10
	-[0x80002220]:csrrs a0, fcsr, zero
	-[0x80002224]:sw t6, 872(t1)
Current Store : [0x80002228] : sw a0, 876(t1) -- Store: [0x80009c50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000223c]:feq.h t6, ft11, ft10
	-[0x80002240]:csrrs a0, fcsr, zero
	-[0x80002244]:sw t6, 880(t1)
Current Store : [0x80002248] : sw a0, 884(t1) -- Store: [0x80009c58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000225c]:feq.h t6, ft11, ft10
	-[0x80002260]:csrrs a0, fcsr, zero
	-[0x80002264]:sw t6, 888(t1)
Current Store : [0x80002268] : sw a0, 892(t1) -- Store: [0x80009c60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000227c]:feq.h t6, ft11, ft10
	-[0x80002280]:csrrs a0, fcsr, zero
	-[0x80002284]:sw t6, 896(t1)
Current Store : [0x80002288] : sw a0, 900(t1) -- Store: [0x80009c68]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000229c]:feq.h t6, ft11, ft10
	-[0x800022a0]:csrrs a0, fcsr, zero
	-[0x800022a4]:sw t6, 904(t1)
Current Store : [0x800022a8] : sw a0, 908(t1) -- Store: [0x80009c70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800022bc]:feq.h t6, ft11, ft10
	-[0x800022c0]:csrrs a0, fcsr, zero
	-[0x800022c4]:sw t6, 912(t1)
Current Store : [0x800022c8] : sw a0, 916(t1) -- Store: [0x80009c78]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800022dc]:feq.h t6, ft11, ft10
	-[0x800022e0]:csrrs a0, fcsr, zero
	-[0x800022e4]:sw t6, 920(t1)
Current Store : [0x800022e8] : sw a0, 924(t1) -- Store: [0x80009c80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800022fc]:feq.h t6, ft11, ft10
	-[0x80002300]:csrrs a0, fcsr, zero
	-[0x80002304]:sw t6, 928(t1)
Current Store : [0x80002308] : sw a0, 932(t1) -- Store: [0x80009c88]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000231c]:feq.h t6, ft11, ft10
	-[0x80002320]:csrrs a0, fcsr, zero
	-[0x80002324]:sw t6, 936(t1)
Current Store : [0x80002328] : sw a0, 940(t1) -- Store: [0x80009c90]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000233c]:feq.h t6, ft11, ft10
	-[0x80002340]:csrrs a0, fcsr, zero
	-[0x80002344]:sw t6, 944(t1)
Current Store : [0x80002348] : sw a0, 948(t1) -- Store: [0x80009c98]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000235c]:feq.h t6, ft11, ft10
	-[0x80002360]:csrrs a0, fcsr, zero
	-[0x80002364]:sw t6, 952(t1)
Current Store : [0x80002368] : sw a0, 956(t1) -- Store: [0x80009ca0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000237c]:feq.h t6, ft11, ft10
	-[0x80002380]:csrrs a0, fcsr, zero
	-[0x80002384]:sw t6, 960(t1)
Current Store : [0x80002388] : sw a0, 964(t1) -- Store: [0x80009ca8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000239c]:feq.h t6, ft11, ft10
	-[0x800023a0]:csrrs a0, fcsr, zero
	-[0x800023a4]:sw t6, 968(t1)
Current Store : [0x800023a8] : sw a0, 972(t1) -- Store: [0x80009cb0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800023bc]:feq.h t6, ft11, ft10
	-[0x800023c0]:csrrs a0, fcsr, zero
	-[0x800023c4]:sw t6, 976(t1)
Current Store : [0x800023c8] : sw a0, 980(t1) -- Store: [0x80009cb8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800023dc]:feq.h t6, ft11, ft10
	-[0x800023e0]:csrrs a0, fcsr, zero
	-[0x800023e4]:sw t6, 984(t1)
Current Store : [0x800023e8] : sw a0, 988(t1) -- Store: [0x80009cc0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800023fc]:feq.h t6, ft11, ft10
	-[0x80002400]:csrrs a0, fcsr, zero
	-[0x80002404]:sw t6, 992(t1)
Current Store : [0x80002408] : sw a0, 996(t1) -- Store: [0x80009cc8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000243c]:feq.h t6, ft11, ft10
	-[0x80002440]:csrrs a0, fcsr, zero
	-[0x80002444]:sw t6, 1000(t1)
Current Store : [0x80002448] : sw a0, 1004(t1) -- Store: [0x80009cd0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000247c]:feq.h t6, ft11, ft10
	-[0x80002480]:csrrs a0, fcsr, zero
	-[0x80002484]:sw t6, 1008(t1)
Current Store : [0x80002488] : sw a0, 1012(t1) -- Store: [0x80009cd8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800024bc]:feq.h t6, ft11, ft10
	-[0x800024c0]:csrrs a0, fcsr, zero
	-[0x800024c4]:sw t6, 1016(t1)
Current Store : [0x800024c8] : sw a0, 1020(t1) -- Store: [0x80009ce0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002504]:feq.h t6, ft11, ft10
	-[0x80002508]:csrrs a0, fcsr, zero
	-[0x8000250c]:sw t6, 0(t1)
Current Store : [0x80002510] : sw a0, 4(t1) -- Store: [0x80009ce8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002544]:feq.h t6, ft11, ft10
	-[0x80002548]:csrrs a0, fcsr, zero
	-[0x8000254c]:sw t6, 8(t1)
Current Store : [0x80002550] : sw a0, 12(t1) -- Store: [0x80009cf0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002584]:feq.h t6, ft11, ft10
	-[0x80002588]:csrrs a0, fcsr, zero
	-[0x8000258c]:sw t6, 16(t1)
Current Store : [0x80002590] : sw a0, 20(t1) -- Store: [0x80009cf8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800025c4]:feq.h t6, ft11, ft10
	-[0x800025c8]:csrrs a0, fcsr, zero
	-[0x800025cc]:sw t6, 24(t1)
Current Store : [0x800025d0] : sw a0, 28(t1) -- Store: [0x80009d00]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002604]:feq.h t6, ft11, ft10
	-[0x80002608]:csrrs a0, fcsr, zero
	-[0x8000260c]:sw t6, 32(t1)
Current Store : [0x80002610] : sw a0, 36(t1) -- Store: [0x80009d08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002644]:feq.h t6, ft11, ft10
	-[0x80002648]:csrrs a0, fcsr, zero
	-[0x8000264c]:sw t6, 40(t1)
Current Store : [0x80002650] : sw a0, 44(t1) -- Store: [0x80009d10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002684]:feq.h t6, ft11, ft10
	-[0x80002688]:csrrs a0, fcsr, zero
	-[0x8000268c]:sw t6, 48(t1)
Current Store : [0x80002690] : sw a0, 52(t1) -- Store: [0x80009d18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800026c4]:feq.h t6, ft11, ft10
	-[0x800026c8]:csrrs a0, fcsr, zero
	-[0x800026cc]:sw t6, 56(t1)
Current Store : [0x800026d0] : sw a0, 60(t1) -- Store: [0x80009d20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002704]:feq.h t6, ft11, ft10
	-[0x80002708]:csrrs a0, fcsr, zero
	-[0x8000270c]:sw t6, 64(t1)
Current Store : [0x80002710] : sw a0, 68(t1) -- Store: [0x80009d28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002744]:feq.h t6, ft11, ft10
	-[0x80002748]:csrrs a0, fcsr, zero
	-[0x8000274c]:sw t6, 72(t1)
Current Store : [0x80002750] : sw a0, 76(t1) -- Store: [0x80009d30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002784]:feq.h t6, ft11, ft10
	-[0x80002788]:csrrs a0, fcsr, zero
	-[0x8000278c]:sw t6, 80(t1)
Current Store : [0x80002790] : sw a0, 84(t1) -- Store: [0x80009d38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800027c4]:feq.h t6, ft11, ft10
	-[0x800027c8]:csrrs a0, fcsr, zero
	-[0x800027cc]:sw t6, 88(t1)
Current Store : [0x800027d0] : sw a0, 92(t1) -- Store: [0x80009d40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002804]:feq.h t6, ft11, ft10
	-[0x80002808]:csrrs a0, fcsr, zero
	-[0x8000280c]:sw t6, 96(t1)
Current Store : [0x80002810] : sw a0, 100(t1) -- Store: [0x80009d48]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002844]:feq.h t6, ft11, ft10
	-[0x80002848]:csrrs a0, fcsr, zero
	-[0x8000284c]:sw t6, 104(t1)
Current Store : [0x80002850] : sw a0, 108(t1) -- Store: [0x80009d50]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002884]:feq.h t6, ft11, ft10
	-[0x80002888]:csrrs a0, fcsr, zero
	-[0x8000288c]:sw t6, 112(t1)
Current Store : [0x80002890] : sw a0, 116(t1) -- Store: [0x80009d58]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800028c4]:feq.h t6, ft11, ft10
	-[0x800028c8]:csrrs a0, fcsr, zero
	-[0x800028cc]:sw t6, 120(t1)
Current Store : [0x800028d0] : sw a0, 124(t1) -- Store: [0x80009d60]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002904]:feq.h t6, ft11, ft10
	-[0x80002908]:csrrs a0, fcsr, zero
	-[0x8000290c]:sw t6, 128(t1)
Current Store : [0x80002910] : sw a0, 132(t1) -- Store: [0x80009d68]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002944]:feq.h t6, ft11, ft10
	-[0x80002948]:csrrs a0, fcsr, zero
	-[0x8000294c]:sw t6, 136(t1)
Current Store : [0x80002950] : sw a0, 140(t1) -- Store: [0x80009d70]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002984]:feq.h t6, ft11, ft10
	-[0x80002988]:csrrs a0, fcsr, zero
	-[0x8000298c]:sw t6, 144(t1)
Current Store : [0x80002990] : sw a0, 148(t1) -- Store: [0x80009d78]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800029c4]:feq.h t6, ft11, ft10
	-[0x800029c8]:csrrs a0, fcsr, zero
	-[0x800029cc]:sw t6, 152(t1)
Current Store : [0x800029d0] : sw a0, 156(t1) -- Store: [0x80009d80]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002a04]:feq.h t6, ft11, ft10
	-[0x80002a08]:csrrs a0, fcsr, zero
	-[0x80002a0c]:sw t6, 160(t1)
Current Store : [0x80002a10] : sw a0, 164(t1) -- Store: [0x80009d88]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002a44]:feq.h t6, ft11, ft10
	-[0x80002a48]:csrrs a0, fcsr, zero
	-[0x80002a4c]:sw t6, 168(t1)
Current Store : [0x80002a50] : sw a0, 172(t1) -- Store: [0x80009d90]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002a84]:feq.h t6, ft11, ft10
	-[0x80002a88]:csrrs a0, fcsr, zero
	-[0x80002a8c]:sw t6, 176(t1)
Current Store : [0x80002a90] : sw a0, 180(t1) -- Store: [0x80009d98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002ac4]:feq.h t6, ft11, ft10
	-[0x80002ac8]:csrrs a0, fcsr, zero
	-[0x80002acc]:sw t6, 184(t1)
Current Store : [0x80002ad0] : sw a0, 188(t1) -- Store: [0x80009da0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002b04]:feq.h t6, ft11, ft10
	-[0x80002b08]:csrrs a0, fcsr, zero
	-[0x80002b0c]:sw t6, 192(t1)
Current Store : [0x80002b10] : sw a0, 196(t1) -- Store: [0x80009da8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002b44]:feq.h t6, ft11, ft10
	-[0x80002b48]:csrrs a0, fcsr, zero
	-[0x80002b4c]:sw t6, 200(t1)
Current Store : [0x80002b50] : sw a0, 204(t1) -- Store: [0x80009db0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002b84]:feq.h t6, ft11, ft10
	-[0x80002b88]:csrrs a0, fcsr, zero
	-[0x80002b8c]:sw t6, 208(t1)
Current Store : [0x80002b90] : sw a0, 212(t1) -- Store: [0x80009db8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002bc4]:feq.h t6, ft11, ft10
	-[0x80002bc8]:csrrs a0, fcsr, zero
	-[0x80002bcc]:sw t6, 216(t1)
Current Store : [0x80002bd0] : sw a0, 220(t1) -- Store: [0x80009dc0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002c04]:feq.h t6, ft11, ft10
	-[0x80002c08]:csrrs a0, fcsr, zero
	-[0x80002c0c]:sw t6, 224(t1)
Current Store : [0x80002c10] : sw a0, 228(t1) -- Store: [0x80009dc8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002c44]:feq.h t6, ft11, ft10
	-[0x80002c48]:csrrs a0, fcsr, zero
	-[0x80002c4c]:sw t6, 232(t1)
Current Store : [0x80002c50] : sw a0, 236(t1) -- Store: [0x80009dd0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002c84]:feq.h t6, ft11, ft10
	-[0x80002c88]:csrrs a0, fcsr, zero
	-[0x80002c8c]:sw t6, 240(t1)
Current Store : [0x80002c90] : sw a0, 244(t1) -- Store: [0x80009dd8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002cc4]:feq.h t6, ft11, ft10
	-[0x80002cc8]:csrrs a0, fcsr, zero
	-[0x80002ccc]:sw t6, 248(t1)
Current Store : [0x80002cd0] : sw a0, 252(t1) -- Store: [0x80009de0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002d04]:feq.h t6, ft11, ft10
	-[0x80002d08]:csrrs a0, fcsr, zero
	-[0x80002d0c]:sw t6, 256(t1)
Current Store : [0x80002d10] : sw a0, 260(t1) -- Store: [0x80009de8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002d44]:feq.h t6, ft11, ft10
	-[0x80002d48]:csrrs a0, fcsr, zero
	-[0x80002d4c]:sw t6, 264(t1)
Current Store : [0x80002d50] : sw a0, 268(t1) -- Store: [0x80009df0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002d84]:feq.h t6, ft11, ft10
	-[0x80002d88]:csrrs a0, fcsr, zero
	-[0x80002d8c]:sw t6, 272(t1)
Current Store : [0x80002d90] : sw a0, 276(t1) -- Store: [0x80009df8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002dc4]:feq.h t6, ft11, ft10
	-[0x80002dc8]:csrrs a0, fcsr, zero
	-[0x80002dcc]:sw t6, 280(t1)
Current Store : [0x80002dd0] : sw a0, 284(t1) -- Store: [0x80009e00]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002e04]:feq.h t6, ft11, ft10
	-[0x80002e08]:csrrs a0, fcsr, zero
	-[0x80002e0c]:sw t6, 288(t1)
Current Store : [0x80002e10] : sw a0, 292(t1) -- Store: [0x80009e08]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002e44]:feq.h t6, ft11, ft10
	-[0x80002e48]:csrrs a0, fcsr, zero
	-[0x80002e4c]:sw t6, 296(t1)
Current Store : [0x80002e50] : sw a0, 300(t1) -- Store: [0x80009e10]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002e84]:feq.h t6, ft11, ft10
	-[0x80002e88]:csrrs a0, fcsr, zero
	-[0x80002e8c]:sw t6, 304(t1)
Current Store : [0x80002e90] : sw a0, 308(t1) -- Store: [0x80009e18]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002ec4]:feq.h t6, ft11, ft10
	-[0x80002ec8]:csrrs a0, fcsr, zero
	-[0x80002ecc]:sw t6, 312(t1)
Current Store : [0x80002ed0] : sw a0, 316(t1) -- Store: [0x80009e20]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002f04]:feq.h t6, ft11, ft10
	-[0x80002f08]:csrrs a0, fcsr, zero
	-[0x80002f0c]:sw t6, 320(t1)
Current Store : [0x80002f10] : sw a0, 324(t1) -- Store: [0x80009e28]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002f44]:feq.h t6, ft11, ft10
	-[0x80002f48]:csrrs a0, fcsr, zero
	-[0x80002f4c]:sw t6, 328(t1)
Current Store : [0x80002f50] : sw a0, 332(t1) -- Store: [0x80009e30]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002f84]:feq.h t6, ft11, ft10
	-[0x80002f88]:csrrs a0, fcsr, zero
	-[0x80002f8c]:sw t6, 336(t1)
Current Store : [0x80002f90] : sw a0, 340(t1) -- Store: [0x80009e38]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80002fc4]:feq.h t6, ft11, ft10
	-[0x80002fc8]:csrrs a0, fcsr, zero
	-[0x80002fcc]:sw t6, 344(t1)
Current Store : [0x80002fd0] : sw a0, 348(t1) -- Store: [0x80009e40]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003004]:feq.h t6, ft11, ft10
	-[0x80003008]:csrrs a0, fcsr, zero
	-[0x8000300c]:sw t6, 352(t1)
Current Store : [0x80003010] : sw a0, 356(t1) -- Store: [0x80009e48]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003044]:feq.h t6, ft11, ft10
	-[0x80003048]:csrrs a0, fcsr, zero
	-[0x8000304c]:sw t6, 360(t1)
Current Store : [0x80003050] : sw a0, 364(t1) -- Store: [0x80009e50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003084]:feq.h t6, ft11, ft10
	-[0x80003088]:csrrs a0, fcsr, zero
	-[0x8000308c]:sw t6, 368(t1)
Current Store : [0x80003090] : sw a0, 372(t1) -- Store: [0x80009e58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800030c4]:feq.h t6, ft11, ft10
	-[0x800030c8]:csrrs a0, fcsr, zero
	-[0x800030cc]:sw t6, 376(t1)
Current Store : [0x800030d0] : sw a0, 380(t1) -- Store: [0x80009e60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003104]:feq.h t6, ft11, ft10
	-[0x80003108]:csrrs a0, fcsr, zero
	-[0x8000310c]:sw t6, 384(t1)
Current Store : [0x80003110] : sw a0, 388(t1) -- Store: [0x80009e68]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003144]:feq.h t6, ft11, ft10
	-[0x80003148]:csrrs a0, fcsr, zero
	-[0x8000314c]:sw t6, 392(t1)
Current Store : [0x80003150] : sw a0, 396(t1) -- Store: [0x80009e70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003184]:feq.h t6, ft11, ft10
	-[0x80003188]:csrrs a0, fcsr, zero
	-[0x8000318c]:sw t6, 400(t1)
Current Store : [0x80003190] : sw a0, 404(t1) -- Store: [0x80009e78]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800031c4]:feq.h t6, ft11, ft10
	-[0x800031c8]:csrrs a0, fcsr, zero
	-[0x800031cc]:sw t6, 408(t1)
Current Store : [0x800031d0] : sw a0, 412(t1) -- Store: [0x80009e80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003204]:feq.h t6, ft11, ft10
	-[0x80003208]:csrrs a0, fcsr, zero
	-[0x8000320c]:sw t6, 416(t1)
Current Store : [0x80003210] : sw a0, 420(t1) -- Store: [0x80009e88]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003244]:feq.h t6, ft11, ft10
	-[0x80003248]:csrrs a0, fcsr, zero
	-[0x8000324c]:sw t6, 424(t1)
Current Store : [0x80003250] : sw a0, 428(t1) -- Store: [0x80009e90]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003284]:feq.h t6, ft11, ft10
	-[0x80003288]:csrrs a0, fcsr, zero
	-[0x8000328c]:sw t6, 432(t1)
Current Store : [0x80003290] : sw a0, 436(t1) -- Store: [0x80009e98]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800032c4]:feq.h t6, ft11, ft10
	-[0x800032c8]:csrrs a0, fcsr, zero
	-[0x800032cc]:sw t6, 440(t1)
Current Store : [0x800032d0] : sw a0, 444(t1) -- Store: [0x80009ea0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003304]:feq.h t6, ft11, ft10
	-[0x80003308]:csrrs a0, fcsr, zero
	-[0x8000330c]:sw t6, 448(t1)
Current Store : [0x80003310] : sw a0, 452(t1) -- Store: [0x80009ea8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003344]:feq.h t6, ft11, ft10
	-[0x80003348]:csrrs a0, fcsr, zero
	-[0x8000334c]:sw t6, 456(t1)
Current Store : [0x80003350] : sw a0, 460(t1) -- Store: [0x80009eb0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003384]:feq.h t6, ft11, ft10
	-[0x80003388]:csrrs a0, fcsr, zero
	-[0x8000338c]:sw t6, 464(t1)
Current Store : [0x80003390] : sw a0, 468(t1) -- Store: [0x80009eb8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800033c4]:feq.h t6, ft11, ft10
	-[0x800033c8]:csrrs a0, fcsr, zero
	-[0x800033cc]:sw t6, 472(t1)
Current Store : [0x800033d0] : sw a0, 476(t1) -- Store: [0x80009ec0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003404]:feq.h t6, ft11, ft10
	-[0x80003408]:csrrs a0, fcsr, zero
	-[0x8000340c]:sw t6, 480(t1)
Current Store : [0x80003410] : sw a0, 484(t1) -- Store: [0x80009ec8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003444]:feq.h t6, ft11, ft10
	-[0x80003448]:csrrs a0, fcsr, zero
	-[0x8000344c]:sw t6, 488(t1)
Current Store : [0x80003450] : sw a0, 492(t1) -- Store: [0x80009ed0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003484]:feq.h t6, ft11, ft10
	-[0x80003488]:csrrs a0, fcsr, zero
	-[0x8000348c]:sw t6, 496(t1)
Current Store : [0x80003490] : sw a0, 500(t1) -- Store: [0x80009ed8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800034c4]:feq.h t6, ft11, ft10
	-[0x800034c8]:csrrs a0, fcsr, zero
	-[0x800034cc]:sw t6, 504(t1)
Current Store : [0x800034d0] : sw a0, 508(t1) -- Store: [0x80009ee0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003504]:feq.h t6, ft11, ft10
	-[0x80003508]:csrrs a0, fcsr, zero
	-[0x8000350c]:sw t6, 512(t1)
Current Store : [0x80003510] : sw a0, 516(t1) -- Store: [0x80009ee8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003544]:feq.h t6, ft11, ft10
	-[0x80003548]:csrrs a0, fcsr, zero
	-[0x8000354c]:sw t6, 520(t1)
Current Store : [0x80003550] : sw a0, 524(t1) -- Store: [0x80009ef0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003584]:feq.h t6, ft11, ft10
	-[0x80003588]:csrrs a0, fcsr, zero
	-[0x8000358c]:sw t6, 528(t1)
Current Store : [0x80003590] : sw a0, 532(t1) -- Store: [0x80009ef8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800035c4]:feq.h t6, ft11, ft10
	-[0x800035c8]:csrrs a0, fcsr, zero
	-[0x800035cc]:sw t6, 536(t1)
Current Store : [0x800035d0] : sw a0, 540(t1) -- Store: [0x80009f00]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003604]:feq.h t6, ft11, ft10
	-[0x80003608]:csrrs a0, fcsr, zero
	-[0x8000360c]:sw t6, 544(t1)
Current Store : [0x80003610] : sw a0, 548(t1) -- Store: [0x80009f08]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003644]:feq.h t6, ft11, ft10
	-[0x80003648]:csrrs a0, fcsr, zero
	-[0x8000364c]:sw t6, 552(t1)
Current Store : [0x80003650] : sw a0, 556(t1) -- Store: [0x80009f10]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003684]:feq.h t6, ft11, ft10
	-[0x80003688]:csrrs a0, fcsr, zero
	-[0x8000368c]:sw t6, 560(t1)
Current Store : [0x80003690] : sw a0, 564(t1) -- Store: [0x80009f18]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800036c4]:feq.h t6, ft11, ft10
	-[0x800036c8]:csrrs a0, fcsr, zero
	-[0x800036cc]:sw t6, 568(t1)
Current Store : [0x800036d0] : sw a0, 572(t1) -- Store: [0x80009f20]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003704]:feq.h t6, ft11, ft10
	-[0x80003708]:csrrs a0, fcsr, zero
	-[0x8000370c]:sw t6, 576(t1)
Current Store : [0x80003710] : sw a0, 580(t1) -- Store: [0x80009f28]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003744]:feq.h t6, ft11, ft10
	-[0x80003748]:csrrs a0, fcsr, zero
	-[0x8000374c]:sw t6, 584(t1)
Current Store : [0x80003750] : sw a0, 588(t1) -- Store: [0x80009f30]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003784]:feq.h t6, ft11, ft10
	-[0x80003788]:csrrs a0, fcsr, zero
	-[0x8000378c]:sw t6, 592(t1)
Current Store : [0x80003790] : sw a0, 596(t1) -- Store: [0x80009f38]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800037c4]:feq.h t6, ft11, ft10
	-[0x800037c8]:csrrs a0, fcsr, zero
	-[0x800037cc]:sw t6, 600(t1)
Current Store : [0x800037d0] : sw a0, 604(t1) -- Store: [0x80009f40]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003804]:feq.h t6, ft11, ft10
	-[0x80003808]:csrrs a0, fcsr, zero
	-[0x8000380c]:sw t6, 608(t1)
Current Store : [0x80003810] : sw a0, 612(t1) -- Store: [0x80009f48]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003844]:feq.h t6, ft11, ft10
	-[0x80003848]:csrrs a0, fcsr, zero
	-[0x8000384c]:sw t6, 616(t1)
Current Store : [0x80003850] : sw a0, 620(t1) -- Store: [0x80009f50]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003884]:feq.h t6, ft11, ft10
	-[0x80003888]:csrrs a0, fcsr, zero
	-[0x8000388c]:sw t6, 624(t1)
Current Store : [0x80003890] : sw a0, 628(t1) -- Store: [0x80009f58]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800038c4]:feq.h t6, ft11, ft10
	-[0x800038c8]:csrrs a0, fcsr, zero
	-[0x800038cc]:sw t6, 632(t1)
Current Store : [0x800038d0] : sw a0, 636(t1) -- Store: [0x80009f60]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003904]:feq.h t6, ft11, ft10
	-[0x80003908]:csrrs a0, fcsr, zero
	-[0x8000390c]:sw t6, 640(t1)
Current Store : [0x80003910] : sw a0, 644(t1) -- Store: [0x80009f68]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003944]:feq.h t6, ft11, ft10
	-[0x80003948]:csrrs a0, fcsr, zero
	-[0x8000394c]:sw t6, 648(t1)
Current Store : [0x80003950] : sw a0, 652(t1) -- Store: [0x80009f70]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003984]:feq.h t6, ft11, ft10
	-[0x80003988]:csrrs a0, fcsr, zero
	-[0x8000398c]:sw t6, 656(t1)
Current Store : [0x80003990] : sw a0, 660(t1) -- Store: [0x80009f78]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800039c4]:feq.h t6, ft11, ft10
	-[0x800039c8]:csrrs a0, fcsr, zero
	-[0x800039cc]:sw t6, 664(t1)
Current Store : [0x800039d0] : sw a0, 668(t1) -- Store: [0x80009f80]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003a04]:feq.h t6, ft11, ft10
	-[0x80003a08]:csrrs a0, fcsr, zero
	-[0x80003a0c]:sw t6, 672(t1)
Current Store : [0x80003a10] : sw a0, 676(t1) -- Store: [0x80009f88]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003a44]:feq.h t6, ft11, ft10
	-[0x80003a48]:csrrs a0, fcsr, zero
	-[0x80003a4c]:sw t6, 680(t1)
Current Store : [0x80003a50] : sw a0, 684(t1) -- Store: [0x80009f90]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003a84]:feq.h t6, ft11, ft10
	-[0x80003a88]:csrrs a0, fcsr, zero
	-[0x80003a8c]:sw t6, 688(t1)
Current Store : [0x80003a90] : sw a0, 692(t1) -- Store: [0x80009f98]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003ac4]:feq.h t6, ft11, ft10
	-[0x80003ac8]:csrrs a0, fcsr, zero
	-[0x80003acc]:sw t6, 696(t1)
Current Store : [0x80003ad0] : sw a0, 700(t1) -- Store: [0x80009fa0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003b04]:feq.h t6, ft11, ft10
	-[0x80003b08]:csrrs a0, fcsr, zero
	-[0x80003b0c]:sw t6, 704(t1)
Current Store : [0x80003b10] : sw a0, 708(t1) -- Store: [0x80009fa8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003b44]:feq.h t6, ft11, ft10
	-[0x80003b48]:csrrs a0, fcsr, zero
	-[0x80003b4c]:sw t6, 712(t1)
Current Store : [0x80003b50] : sw a0, 716(t1) -- Store: [0x80009fb0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003b84]:feq.h t6, ft11, ft10
	-[0x80003b88]:csrrs a0, fcsr, zero
	-[0x80003b8c]:sw t6, 720(t1)
Current Store : [0x80003b90] : sw a0, 724(t1) -- Store: [0x80009fb8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003bc4]:feq.h t6, ft11, ft10
	-[0x80003bc8]:csrrs a0, fcsr, zero
	-[0x80003bcc]:sw t6, 728(t1)
Current Store : [0x80003bd0] : sw a0, 732(t1) -- Store: [0x80009fc0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003c04]:feq.h t6, ft11, ft10
	-[0x80003c08]:csrrs a0, fcsr, zero
	-[0x80003c0c]:sw t6, 736(t1)
Current Store : [0x80003c10] : sw a0, 740(t1) -- Store: [0x80009fc8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003c44]:feq.h t6, ft11, ft10
	-[0x80003c48]:csrrs a0, fcsr, zero
	-[0x80003c4c]:sw t6, 744(t1)
Current Store : [0x80003c50] : sw a0, 748(t1) -- Store: [0x80009fd0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003c84]:feq.h t6, ft11, ft10
	-[0x80003c88]:csrrs a0, fcsr, zero
	-[0x80003c8c]:sw t6, 752(t1)
Current Store : [0x80003c90] : sw a0, 756(t1) -- Store: [0x80009fd8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003cc4]:feq.h t6, ft11, ft10
	-[0x80003cc8]:csrrs a0, fcsr, zero
	-[0x80003ccc]:sw t6, 760(t1)
Current Store : [0x80003cd0] : sw a0, 764(t1) -- Store: [0x80009fe0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003d04]:feq.h t6, ft11, ft10
	-[0x80003d08]:csrrs a0, fcsr, zero
	-[0x80003d0c]:sw t6, 768(t1)
Current Store : [0x80003d10] : sw a0, 772(t1) -- Store: [0x80009fe8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003d44]:feq.h t6, ft11, ft10
	-[0x80003d48]:csrrs a0, fcsr, zero
	-[0x80003d4c]:sw t6, 776(t1)
Current Store : [0x80003d50] : sw a0, 780(t1) -- Store: [0x80009ff0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003d84]:feq.h t6, ft11, ft10
	-[0x80003d88]:csrrs a0, fcsr, zero
	-[0x80003d8c]:sw t6, 784(t1)
Current Store : [0x80003d90] : sw a0, 788(t1) -- Store: [0x80009ff8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003dc4]:feq.h t6, ft11, ft10
	-[0x80003dc8]:csrrs a0, fcsr, zero
	-[0x80003dcc]:sw t6, 792(t1)
Current Store : [0x80003dd0] : sw a0, 796(t1) -- Store: [0x8000a000]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003e04]:feq.h t6, ft11, ft10
	-[0x80003e08]:csrrs a0, fcsr, zero
	-[0x80003e0c]:sw t6, 800(t1)
Current Store : [0x80003e10] : sw a0, 804(t1) -- Store: [0x8000a008]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003e44]:feq.h t6, ft11, ft10
	-[0x80003e48]:csrrs a0, fcsr, zero
	-[0x80003e4c]:sw t6, 808(t1)
Current Store : [0x80003e50] : sw a0, 812(t1) -- Store: [0x8000a010]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003e84]:feq.h t6, ft11, ft10
	-[0x80003e88]:csrrs a0, fcsr, zero
	-[0x80003e8c]:sw t6, 816(t1)
Current Store : [0x80003e90] : sw a0, 820(t1) -- Store: [0x8000a018]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003ec4]:feq.h t6, ft11, ft10
	-[0x80003ec8]:csrrs a0, fcsr, zero
	-[0x80003ecc]:sw t6, 824(t1)
Current Store : [0x80003ed0] : sw a0, 828(t1) -- Store: [0x8000a020]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003f04]:feq.h t6, ft11, ft10
	-[0x80003f08]:csrrs a0, fcsr, zero
	-[0x80003f0c]:sw t6, 832(t1)
Current Store : [0x80003f10] : sw a0, 836(t1) -- Store: [0x8000a028]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003f44]:feq.h t6, ft11, ft10
	-[0x80003f48]:csrrs a0, fcsr, zero
	-[0x80003f4c]:sw t6, 840(t1)
Current Store : [0x80003f50] : sw a0, 844(t1) -- Store: [0x8000a030]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003f84]:feq.h t6, ft11, ft10
	-[0x80003f88]:csrrs a0, fcsr, zero
	-[0x80003f8c]:sw t6, 848(t1)
Current Store : [0x80003f90] : sw a0, 852(t1) -- Store: [0x8000a038]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80003fc4]:feq.h t6, ft11, ft10
	-[0x80003fc8]:csrrs a0, fcsr, zero
	-[0x80003fcc]:sw t6, 856(t1)
Current Store : [0x80003fd0] : sw a0, 860(t1) -- Store: [0x8000a040]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004004]:feq.h t6, ft11, ft10
	-[0x80004008]:csrrs a0, fcsr, zero
	-[0x8000400c]:sw t6, 864(t1)
Current Store : [0x80004010] : sw a0, 868(t1) -- Store: [0x8000a048]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004044]:feq.h t6, ft11, ft10
	-[0x80004048]:csrrs a0, fcsr, zero
	-[0x8000404c]:sw t6, 872(t1)
Current Store : [0x80004050] : sw a0, 876(t1) -- Store: [0x8000a050]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004084]:feq.h t6, ft11, ft10
	-[0x80004088]:csrrs a0, fcsr, zero
	-[0x8000408c]:sw t6, 880(t1)
Current Store : [0x80004090] : sw a0, 884(t1) -- Store: [0x8000a058]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800040c4]:feq.h t6, ft11, ft10
	-[0x800040c8]:csrrs a0, fcsr, zero
	-[0x800040cc]:sw t6, 888(t1)
Current Store : [0x800040d0] : sw a0, 892(t1) -- Store: [0x8000a060]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004104]:feq.h t6, ft11, ft10
	-[0x80004108]:csrrs a0, fcsr, zero
	-[0x8000410c]:sw t6, 896(t1)
Current Store : [0x80004110] : sw a0, 900(t1) -- Store: [0x8000a068]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004144]:feq.h t6, ft11, ft10
	-[0x80004148]:csrrs a0, fcsr, zero
	-[0x8000414c]:sw t6, 904(t1)
Current Store : [0x80004150] : sw a0, 908(t1) -- Store: [0x8000a070]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004184]:feq.h t6, ft11, ft10
	-[0x80004188]:csrrs a0, fcsr, zero
	-[0x8000418c]:sw t6, 912(t1)
Current Store : [0x80004190] : sw a0, 916(t1) -- Store: [0x8000a078]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800041c4]:feq.h t6, ft11, ft10
	-[0x800041c8]:csrrs a0, fcsr, zero
	-[0x800041cc]:sw t6, 920(t1)
Current Store : [0x800041d0] : sw a0, 924(t1) -- Store: [0x8000a080]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004204]:feq.h t6, ft11, ft10
	-[0x80004208]:csrrs a0, fcsr, zero
	-[0x8000420c]:sw t6, 928(t1)
Current Store : [0x80004210] : sw a0, 932(t1) -- Store: [0x8000a088]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004244]:feq.h t6, ft11, ft10
	-[0x80004248]:csrrs a0, fcsr, zero
	-[0x8000424c]:sw t6, 936(t1)
Current Store : [0x80004250] : sw a0, 940(t1) -- Store: [0x8000a090]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004284]:feq.h t6, ft11, ft10
	-[0x80004288]:csrrs a0, fcsr, zero
	-[0x8000428c]:sw t6, 944(t1)
Current Store : [0x80004290] : sw a0, 948(t1) -- Store: [0x8000a098]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800042c4]:feq.h t6, ft11, ft10
	-[0x800042c8]:csrrs a0, fcsr, zero
	-[0x800042cc]:sw t6, 952(t1)
Current Store : [0x800042d0] : sw a0, 956(t1) -- Store: [0x8000a0a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004304]:feq.h t6, ft11, ft10
	-[0x80004308]:csrrs a0, fcsr, zero
	-[0x8000430c]:sw t6, 960(t1)
Current Store : [0x80004310] : sw a0, 964(t1) -- Store: [0x8000a0a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004344]:feq.h t6, ft11, ft10
	-[0x80004348]:csrrs a0, fcsr, zero
	-[0x8000434c]:sw t6, 968(t1)
Current Store : [0x80004350] : sw a0, 972(t1) -- Store: [0x8000a0b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004384]:feq.h t6, ft11, ft10
	-[0x80004388]:csrrs a0, fcsr, zero
	-[0x8000438c]:sw t6, 976(t1)
Current Store : [0x80004390] : sw a0, 980(t1) -- Store: [0x8000a0b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800043c4]:feq.h t6, ft11, ft10
	-[0x800043c8]:csrrs a0, fcsr, zero
	-[0x800043cc]:sw t6, 984(t1)
Current Store : [0x800043d0] : sw a0, 988(t1) -- Store: [0x8000a0c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004404]:feq.h t6, ft11, ft10
	-[0x80004408]:csrrs a0, fcsr, zero
	-[0x8000440c]:sw t6, 992(t1)
Current Store : [0x80004410] : sw a0, 996(t1) -- Store: [0x8000a0c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004444]:feq.h t6, ft11, ft10
	-[0x80004448]:csrrs a0, fcsr, zero
	-[0x8000444c]:sw t6, 1000(t1)
Current Store : [0x80004450] : sw a0, 1004(t1) -- Store: [0x8000a0d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004484]:feq.h t6, ft11, ft10
	-[0x80004488]:csrrs a0, fcsr, zero
	-[0x8000448c]:sw t6, 1008(t1)
Current Store : [0x80004490] : sw a0, 1012(t1) -- Store: [0x8000a0d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800044c4]:feq.h t6, ft11, ft10
	-[0x800044c8]:csrrs a0, fcsr, zero
	-[0x800044cc]:sw t6, 1016(t1)
Current Store : [0x800044d0] : sw a0, 1020(t1) -- Store: [0x8000a0e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000450c]:feq.h t6, ft11, ft10
	-[0x80004510]:csrrs a0, fcsr, zero
	-[0x80004514]:sw t6, 0(t1)
Current Store : [0x80004518] : sw a0, 4(t1) -- Store: [0x8000a0e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000454c]:feq.h t6, ft11, ft10
	-[0x80004550]:csrrs a0, fcsr, zero
	-[0x80004554]:sw t6, 8(t1)
Current Store : [0x80004558] : sw a0, 12(t1) -- Store: [0x8000a0f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000458c]:feq.h t6, ft11, ft10
	-[0x80004590]:csrrs a0, fcsr, zero
	-[0x80004594]:sw t6, 16(t1)
Current Store : [0x80004598] : sw a0, 20(t1) -- Store: [0x8000a0f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800045cc]:feq.h t6, ft11, ft10
	-[0x800045d0]:csrrs a0, fcsr, zero
	-[0x800045d4]:sw t6, 24(t1)
Current Store : [0x800045d8] : sw a0, 28(t1) -- Store: [0x8000a100]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000460c]:feq.h t6, ft11, ft10
	-[0x80004610]:csrrs a0, fcsr, zero
	-[0x80004614]:sw t6, 32(t1)
Current Store : [0x80004618] : sw a0, 36(t1) -- Store: [0x8000a108]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000464c]:feq.h t6, ft11, ft10
	-[0x80004650]:csrrs a0, fcsr, zero
	-[0x80004654]:sw t6, 40(t1)
Current Store : [0x80004658] : sw a0, 44(t1) -- Store: [0x8000a110]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000468c]:feq.h t6, ft11, ft10
	-[0x80004690]:csrrs a0, fcsr, zero
	-[0x80004694]:sw t6, 48(t1)
Current Store : [0x80004698] : sw a0, 52(t1) -- Store: [0x8000a118]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800046cc]:feq.h t6, ft11, ft10
	-[0x800046d0]:csrrs a0, fcsr, zero
	-[0x800046d4]:sw t6, 56(t1)
Current Store : [0x800046d8] : sw a0, 60(t1) -- Store: [0x8000a120]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000470c]:feq.h t6, ft11, ft10
	-[0x80004710]:csrrs a0, fcsr, zero
	-[0x80004714]:sw t6, 64(t1)
Current Store : [0x80004718] : sw a0, 68(t1) -- Store: [0x8000a128]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000474c]:feq.h t6, ft11, ft10
	-[0x80004750]:csrrs a0, fcsr, zero
	-[0x80004754]:sw t6, 72(t1)
Current Store : [0x80004758] : sw a0, 76(t1) -- Store: [0x8000a130]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000478c]:feq.h t6, ft11, ft10
	-[0x80004790]:csrrs a0, fcsr, zero
	-[0x80004794]:sw t6, 80(t1)
Current Store : [0x80004798] : sw a0, 84(t1) -- Store: [0x8000a138]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800047cc]:feq.h t6, ft11, ft10
	-[0x800047d0]:csrrs a0, fcsr, zero
	-[0x800047d4]:sw t6, 88(t1)
Current Store : [0x800047d8] : sw a0, 92(t1) -- Store: [0x8000a140]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000480c]:feq.h t6, ft11, ft10
	-[0x80004810]:csrrs a0, fcsr, zero
	-[0x80004814]:sw t6, 96(t1)
Current Store : [0x80004818] : sw a0, 100(t1) -- Store: [0x8000a148]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000484c]:feq.h t6, ft11, ft10
	-[0x80004850]:csrrs a0, fcsr, zero
	-[0x80004854]:sw t6, 104(t1)
Current Store : [0x80004858] : sw a0, 108(t1) -- Store: [0x8000a150]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000488c]:feq.h t6, ft11, ft10
	-[0x80004890]:csrrs a0, fcsr, zero
	-[0x80004894]:sw t6, 112(t1)
Current Store : [0x80004898] : sw a0, 116(t1) -- Store: [0x8000a158]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800048cc]:feq.h t6, ft11, ft10
	-[0x800048d0]:csrrs a0, fcsr, zero
	-[0x800048d4]:sw t6, 120(t1)
Current Store : [0x800048d8] : sw a0, 124(t1) -- Store: [0x8000a160]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000490c]:feq.h t6, ft11, ft10
	-[0x80004910]:csrrs a0, fcsr, zero
	-[0x80004914]:sw t6, 128(t1)
Current Store : [0x80004918] : sw a0, 132(t1) -- Store: [0x8000a168]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000494c]:feq.h t6, ft11, ft10
	-[0x80004950]:csrrs a0, fcsr, zero
	-[0x80004954]:sw t6, 136(t1)
Current Store : [0x80004958] : sw a0, 140(t1) -- Store: [0x8000a170]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000498c]:feq.h t6, ft11, ft10
	-[0x80004990]:csrrs a0, fcsr, zero
	-[0x80004994]:sw t6, 144(t1)
Current Store : [0x80004998] : sw a0, 148(t1) -- Store: [0x8000a178]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800049cc]:feq.h t6, ft11, ft10
	-[0x800049d0]:csrrs a0, fcsr, zero
	-[0x800049d4]:sw t6, 152(t1)
Current Store : [0x800049d8] : sw a0, 156(t1) -- Store: [0x8000a180]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004a0c]:feq.h t6, ft11, ft10
	-[0x80004a10]:csrrs a0, fcsr, zero
	-[0x80004a14]:sw t6, 160(t1)
Current Store : [0x80004a18] : sw a0, 164(t1) -- Store: [0x8000a188]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004a4c]:feq.h t6, ft11, ft10
	-[0x80004a50]:csrrs a0, fcsr, zero
	-[0x80004a54]:sw t6, 168(t1)
Current Store : [0x80004a58] : sw a0, 172(t1) -- Store: [0x8000a190]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004a8c]:feq.h t6, ft11, ft10
	-[0x80004a90]:csrrs a0, fcsr, zero
	-[0x80004a94]:sw t6, 176(t1)
Current Store : [0x80004a98] : sw a0, 180(t1) -- Store: [0x8000a198]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004acc]:feq.h t6, ft11, ft10
	-[0x80004ad0]:csrrs a0, fcsr, zero
	-[0x80004ad4]:sw t6, 184(t1)
Current Store : [0x80004ad8] : sw a0, 188(t1) -- Store: [0x8000a1a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004b0c]:feq.h t6, ft11, ft10
	-[0x80004b10]:csrrs a0, fcsr, zero
	-[0x80004b14]:sw t6, 192(t1)
Current Store : [0x80004b18] : sw a0, 196(t1) -- Store: [0x8000a1a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004b4c]:feq.h t6, ft11, ft10
	-[0x80004b50]:csrrs a0, fcsr, zero
	-[0x80004b54]:sw t6, 200(t1)
Current Store : [0x80004b58] : sw a0, 204(t1) -- Store: [0x8000a1b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004b8c]:feq.h t6, ft11, ft10
	-[0x80004b90]:csrrs a0, fcsr, zero
	-[0x80004b94]:sw t6, 208(t1)
Current Store : [0x80004b98] : sw a0, 212(t1) -- Store: [0x8000a1b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004bcc]:feq.h t6, ft11, ft10
	-[0x80004bd0]:csrrs a0, fcsr, zero
	-[0x80004bd4]:sw t6, 216(t1)
Current Store : [0x80004bd8] : sw a0, 220(t1) -- Store: [0x8000a1c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004c0c]:feq.h t6, ft11, ft10
	-[0x80004c10]:csrrs a0, fcsr, zero
	-[0x80004c14]:sw t6, 224(t1)
Current Store : [0x80004c18] : sw a0, 228(t1) -- Store: [0x8000a1c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004c4c]:feq.h t6, ft11, ft10
	-[0x80004c50]:csrrs a0, fcsr, zero
	-[0x80004c54]:sw t6, 232(t1)
Current Store : [0x80004c58] : sw a0, 236(t1) -- Store: [0x8000a1d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004c8c]:feq.h t6, ft11, ft10
	-[0x80004c90]:csrrs a0, fcsr, zero
	-[0x80004c94]:sw t6, 240(t1)
Current Store : [0x80004c98] : sw a0, 244(t1) -- Store: [0x8000a1d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004ccc]:feq.h t6, ft11, ft10
	-[0x80004cd0]:csrrs a0, fcsr, zero
	-[0x80004cd4]:sw t6, 248(t1)
Current Store : [0x80004cd8] : sw a0, 252(t1) -- Store: [0x8000a1e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004d0c]:feq.h t6, ft11, ft10
	-[0x80004d10]:csrrs a0, fcsr, zero
	-[0x80004d14]:sw t6, 256(t1)
Current Store : [0x80004d18] : sw a0, 260(t1) -- Store: [0x8000a1e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004d4c]:feq.h t6, ft11, ft10
	-[0x80004d50]:csrrs a0, fcsr, zero
	-[0x80004d54]:sw t6, 264(t1)
Current Store : [0x80004d58] : sw a0, 268(t1) -- Store: [0x8000a1f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004d8c]:feq.h t6, ft11, ft10
	-[0x80004d90]:csrrs a0, fcsr, zero
	-[0x80004d94]:sw t6, 272(t1)
Current Store : [0x80004d98] : sw a0, 276(t1) -- Store: [0x8000a1f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004dcc]:feq.h t6, ft11, ft10
	-[0x80004dd0]:csrrs a0, fcsr, zero
	-[0x80004dd4]:sw t6, 280(t1)
Current Store : [0x80004dd8] : sw a0, 284(t1) -- Store: [0x8000a200]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004e0c]:feq.h t6, ft11, ft10
	-[0x80004e10]:csrrs a0, fcsr, zero
	-[0x80004e14]:sw t6, 288(t1)
Current Store : [0x80004e18] : sw a0, 292(t1) -- Store: [0x8000a208]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004e4c]:feq.h t6, ft11, ft10
	-[0x80004e50]:csrrs a0, fcsr, zero
	-[0x80004e54]:sw t6, 296(t1)
Current Store : [0x80004e58] : sw a0, 300(t1) -- Store: [0x8000a210]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004e8c]:feq.h t6, ft11, ft10
	-[0x80004e90]:csrrs a0, fcsr, zero
	-[0x80004e94]:sw t6, 304(t1)
Current Store : [0x80004e98] : sw a0, 308(t1) -- Store: [0x8000a218]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004ecc]:feq.h t6, ft11, ft10
	-[0x80004ed0]:csrrs a0, fcsr, zero
	-[0x80004ed4]:sw t6, 312(t1)
Current Store : [0x80004ed8] : sw a0, 316(t1) -- Store: [0x8000a220]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004f0c]:feq.h t6, ft11, ft10
	-[0x80004f10]:csrrs a0, fcsr, zero
	-[0x80004f14]:sw t6, 320(t1)
Current Store : [0x80004f18] : sw a0, 324(t1) -- Store: [0x8000a228]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004f4c]:feq.h t6, ft11, ft10
	-[0x80004f50]:csrrs a0, fcsr, zero
	-[0x80004f54]:sw t6, 328(t1)
Current Store : [0x80004f58] : sw a0, 332(t1) -- Store: [0x8000a230]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004f8c]:feq.h t6, ft11, ft10
	-[0x80004f90]:csrrs a0, fcsr, zero
	-[0x80004f94]:sw t6, 336(t1)
Current Store : [0x80004f98] : sw a0, 340(t1) -- Store: [0x8000a238]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80004fcc]:feq.h t6, ft11, ft10
	-[0x80004fd0]:csrrs a0, fcsr, zero
	-[0x80004fd4]:sw t6, 344(t1)
Current Store : [0x80004fd8] : sw a0, 348(t1) -- Store: [0x8000a240]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000500c]:feq.h t6, ft11, ft10
	-[0x80005010]:csrrs a0, fcsr, zero
	-[0x80005014]:sw t6, 352(t1)
Current Store : [0x80005018] : sw a0, 356(t1) -- Store: [0x8000a248]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000504c]:feq.h t6, ft11, ft10
	-[0x80005050]:csrrs a0, fcsr, zero
	-[0x80005054]:sw t6, 360(t1)
Current Store : [0x80005058] : sw a0, 364(t1) -- Store: [0x8000a250]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000508c]:feq.h t6, ft11, ft10
	-[0x80005090]:csrrs a0, fcsr, zero
	-[0x80005094]:sw t6, 368(t1)
Current Store : [0x80005098] : sw a0, 372(t1) -- Store: [0x8000a258]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800050cc]:feq.h t6, ft11, ft10
	-[0x800050d0]:csrrs a0, fcsr, zero
	-[0x800050d4]:sw t6, 376(t1)
Current Store : [0x800050d8] : sw a0, 380(t1) -- Store: [0x8000a260]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000510c]:feq.h t6, ft11, ft10
	-[0x80005110]:csrrs a0, fcsr, zero
	-[0x80005114]:sw t6, 384(t1)
Current Store : [0x80005118] : sw a0, 388(t1) -- Store: [0x8000a268]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000514c]:feq.h t6, ft11, ft10
	-[0x80005150]:csrrs a0, fcsr, zero
	-[0x80005154]:sw t6, 392(t1)
Current Store : [0x80005158] : sw a0, 396(t1) -- Store: [0x8000a270]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000518c]:feq.h t6, ft11, ft10
	-[0x80005190]:csrrs a0, fcsr, zero
	-[0x80005194]:sw t6, 400(t1)
Current Store : [0x80005198] : sw a0, 404(t1) -- Store: [0x8000a278]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800051cc]:feq.h t6, ft11, ft10
	-[0x800051d0]:csrrs a0, fcsr, zero
	-[0x800051d4]:sw t6, 408(t1)
Current Store : [0x800051d8] : sw a0, 412(t1) -- Store: [0x8000a280]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000520c]:feq.h t6, ft11, ft10
	-[0x80005210]:csrrs a0, fcsr, zero
	-[0x80005214]:sw t6, 416(t1)
Current Store : [0x80005218] : sw a0, 420(t1) -- Store: [0x8000a288]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000524c]:feq.h t6, ft11, ft10
	-[0x80005250]:csrrs a0, fcsr, zero
	-[0x80005254]:sw t6, 424(t1)
Current Store : [0x80005258] : sw a0, 428(t1) -- Store: [0x8000a290]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000528c]:feq.h t6, ft11, ft10
	-[0x80005290]:csrrs a0, fcsr, zero
	-[0x80005294]:sw t6, 432(t1)
Current Store : [0x80005298] : sw a0, 436(t1) -- Store: [0x8000a298]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800052cc]:feq.h t6, ft11, ft10
	-[0x800052d0]:csrrs a0, fcsr, zero
	-[0x800052d4]:sw t6, 440(t1)
Current Store : [0x800052d8] : sw a0, 444(t1) -- Store: [0x8000a2a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000530c]:feq.h t6, ft11, ft10
	-[0x80005310]:csrrs a0, fcsr, zero
	-[0x80005314]:sw t6, 448(t1)
Current Store : [0x80005318] : sw a0, 452(t1) -- Store: [0x8000a2a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000534c]:feq.h t6, ft11, ft10
	-[0x80005350]:csrrs a0, fcsr, zero
	-[0x80005354]:sw t6, 456(t1)
Current Store : [0x80005358] : sw a0, 460(t1) -- Store: [0x8000a2b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000538c]:feq.h t6, ft11, ft10
	-[0x80005390]:csrrs a0, fcsr, zero
	-[0x80005394]:sw t6, 464(t1)
Current Store : [0x80005398] : sw a0, 468(t1) -- Store: [0x8000a2b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800053cc]:feq.h t6, ft11, ft10
	-[0x800053d0]:csrrs a0, fcsr, zero
	-[0x800053d4]:sw t6, 472(t1)
Current Store : [0x800053d8] : sw a0, 476(t1) -- Store: [0x8000a2c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000540c]:feq.h t6, ft11, ft10
	-[0x80005410]:csrrs a0, fcsr, zero
	-[0x80005414]:sw t6, 480(t1)
Current Store : [0x80005418] : sw a0, 484(t1) -- Store: [0x8000a2c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000544c]:feq.h t6, ft11, ft10
	-[0x80005450]:csrrs a0, fcsr, zero
	-[0x80005454]:sw t6, 488(t1)
Current Store : [0x80005458] : sw a0, 492(t1) -- Store: [0x8000a2d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000548c]:feq.h t6, ft11, ft10
	-[0x80005490]:csrrs a0, fcsr, zero
	-[0x80005494]:sw t6, 496(t1)
Current Store : [0x80005498] : sw a0, 500(t1) -- Store: [0x8000a2d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800054cc]:feq.h t6, ft11, ft10
	-[0x800054d0]:csrrs a0, fcsr, zero
	-[0x800054d4]:sw t6, 504(t1)
Current Store : [0x800054d8] : sw a0, 508(t1) -- Store: [0x8000a2e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000550c]:feq.h t6, ft11, ft10
	-[0x80005510]:csrrs a0, fcsr, zero
	-[0x80005514]:sw t6, 512(t1)
Current Store : [0x80005518] : sw a0, 516(t1) -- Store: [0x8000a2e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000554c]:feq.h t6, ft11, ft10
	-[0x80005550]:csrrs a0, fcsr, zero
	-[0x80005554]:sw t6, 520(t1)
Current Store : [0x80005558] : sw a0, 524(t1) -- Store: [0x8000a2f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000558c]:feq.h t6, ft11, ft10
	-[0x80005590]:csrrs a0, fcsr, zero
	-[0x80005594]:sw t6, 528(t1)
Current Store : [0x80005598] : sw a0, 532(t1) -- Store: [0x8000a2f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800055cc]:feq.h t6, ft11, ft10
	-[0x800055d0]:csrrs a0, fcsr, zero
	-[0x800055d4]:sw t6, 536(t1)
Current Store : [0x800055d8] : sw a0, 540(t1) -- Store: [0x8000a300]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000560c]:feq.h t6, ft11, ft10
	-[0x80005610]:csrrs a0, fcsr, zero
	-[0x80005614]:sw t6, 544(t1)
Current Store : [0x80005618] : sw a0, 548(t1) -- Store: [0x8000a308]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000564c]:feq.h t6, ft11, ft10
	-[0x80005650]:csrrs a0, fcsr, zero
	-[0x80005654]:sw t6, 552(t1)
Current Store : [0x80005658] : sw a0, 556(t1) -- Store: [0x8000a310]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000568c]:feq.h t6, ft11, ft10
	-[0x80005690]:csrrs a0, fcsr, zero
	-[0x80005694]:sw t6, 560(t1)
Current Store : [0x80005698] : sw a0, 564(t1) -- Store: [0x8000a318]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800056cc]:feq.h t6, ft11, ft10
	-[0x800056d0]:csrrs a0, fcsr, zero
	-[0x800056d4]:sw t6, 568(t1)
Current Store : [0x800056d8] : sw a0, 572(t1) -- Store: [0x8000a320]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000570c]:feq.h t6, ft11, ft10
	-[0x80005710]:csrrs a0, fcsr, zero
	-[0x80005714]:sw t6, 576(t1)
Current Store : [0x80005718] : sw a0, 580(t1) -- Store: [0x8000a328]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000574c]:feq.h t6, ft11, ft10
	-[0x80005750]:csrrs a0, fcsr, zero
	-[0x80005754]:sw t6, 584(t1)
Current Store : [0x80005758] : sw a0, 588(t1) -- Store: [0x8000a330]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000578c]:feq.h t6, ft11, ft10
	-[0x80005790]:csrrs a0, fcsr, zero
	-[0x80005794]:sw t6, 592(t1)
Current Store : [0x80005798] : sw a0, 596(t1) -- Store: [0x8000a338]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800057cc]:feq.h t6, ft11, ft10
	-[0x800057d0]:csrrs a0, fcsr, zero
	-[0x800057d4]:sw t6, 600(t1)
Current Store : [0x800057d8] : sw a0, 604(t1) -- Store: [0x8000a340]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000580c]:feq.h t6, ft11, ft10
	-[0x80005810]:csrrs a0, fcsr, zero
	-[0x80005814]:sw t6, 608(t1)
Current Store : [0x80005818] : sw a0, 612(t1) -- Store: [0x8000a348]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000584c]:feq.h t6, ft11, ft10
	-[0x80005850]:csrrs a0, fcsr, zero
	-[0x80005854]:sw t6, 616(t1)
Current Store : [0x80005858] : sw a0, 620(t1) -- Store: [0x8000a350]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000588c]:feq.h t6, ft11, ft10
	-[0x80005890]:csrrs a0, fcsr, zero
	-[0x80005894]:sw t6, 624(t1)
Current Store : [0x80005898] : sw a0, 628(t1) -- Store: [0x8000a358]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800058cc]:feq.h t6, ft11, ft10
	-[0x800058d0]:csrrs a0, fcsr, zero
	-[0x800058d4]:sw t6, 632(t1)
Current Store : [0x800058d8] : sw a0, 636(t1) -- Store: [0x8000a360]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000590c]:feq.h t6, ft11, ft10
	-[0x80005910]:csrrs a0, fcsr, zero
	-[0x80005914]:sw t6, 640(t1)
Current Store : [0x80005918] : sw a0, 644(t1) -- Store: [0x8000a368]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000594c]:feq.h t6, ft11, ft10
	-[0x80005950]:csrrs a0, fcsr, zero
	-[0x80005954]:sw t6, 648(t1)
Current Store : [0x80005958] : sw a0, 652(t1) -- Store: [0x8000a370]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000598c]:feq.h t6, ft11, ft10
	-[0x80005990]:csrrs a0, fcsr, zero
	-[0x80005994]:sw t6, 656(t1)
Current Store : [0x80005998] : sw a0, 660(t1) -- Store: [0x8000a378]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800059cc]:feq.h t6, ft11, ft10
	-[0x800059d0]:csrrs a0, fcsr, zero
	-[0x800059d4]:sw t6, 664(t1)
Current Store : [0x800059d8] : sw a0, 668(t1) -- Store: [0x8000a380]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005a0c]:feq.h t6, ft11, ft10
	-[0x80005a10]:csrrs a0, fcsr, zero
	-[0x80005a14]:sw t6, 672(t1)
Current Store : [0x80005a18] : sw a0, 676(t1) -- Store: [0x8000a388]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005a4c]:feq.h t6, ft11, ft10
	-[0x80005a50]:csrrs a0, fcsr, zero
	-[0x80005a54]:sw t6, 680(t1)
Current Store : [0x80005a58] : sw a0, 684(t1) -- Store: [0x8000a390]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005a8c]:feq.h t6, ft11, ft10
	-[0x80005a90]:csrrs a0, fcsr, zero
	-[0x80005a94]:sw t6, 688(t1)
Current Store : [0x80005a98] : sw a0, 692(t1) -- Store: [0x8000a398]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005acc]:feq.h t6, ft11, ft10
	-[0x80005ad0]:csrrs a0, fcsr, zero
	-[0x80005ad4]:sw t6, 696(t1)
Current Store : [0x80005ad8] : sw a0, 700(t1) -- Store: [0x8000a3a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005b0c]:feq.h t6, ft11, ft10
	-[0x80005b10]:csrrs a0, fcsr, zero
	-[0x80005b14]:sw t6, 704(t1)
Current Store : [0x80005b18] : sw a0, 708(t1) -- Store: [0x8000a3a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005b4c]:feq.h t6, ft11, ft10
	-[0x80005b50]:csrrs a0, fcsr, zero
	-[0x80005b54]:sw t6, 712(t1)
Current Store : [0x80005b58] : sw a0, 716(t1) -- Store: [0x8000a3b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005b8c]:feq.h t6, ft11, ft10
	-[0x80005b90]:csrrs a0, fcsr, zero
	-[0x80005b94]:sw t6, 720(t1)
Current Store : [0x80005b98] : sw a0, 724(t1) -- Store: [0x8000a3b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005bcc]:feq.h t6, ft11, ft10
	-[0x80005bd0]:csrrs a0, fcsr, zero
	-[0x80005bd4]:sw t6, 728(t1)
Current Store : [0x80005bd8] : sw a0, 732(t1) -- Store: [0x8000a3c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005c0c]:feq.h t6, ft11, ft10
	-[0x80005c10]:csrrs a0, fcsr, zero
	-[0x80005c14]:sw t6, 736(t1)
Current Store : [0x80005c18] : sw a0, 740(t1) -- Store: [0x8000a3c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005c4c]:feq.h t6, ft11, ft10
	-[0x80005c50]:csrrs a0, fcsr, zero
	-[0x80005c54]:sw t6, 744(t1)
Current Store : [0x80005c58] : sw a0, 748(t1) -- Store: [0x8000a3d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005c8c]:feq.h t6, ft11, ft10
	-[0x80005c90]:csrrs a0, fcsr, zero
	-[0x80005c94]:sw t6, 752(t1)
Current Store : [0x80005c98] : sw a0, 756(t1) -- Store: [0x8000a3d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005ccc]:feq.h t6, ft11, ft10
	-[0x80005cd0]:csrrs a0, fcsr, zero
	-[0x80005cd4]:sw t6, 760(t1)
Current Store : [0x80005cd8] : sw a0, 764(t1) -- Store: [0x8000a3e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005d0c]:feq.h t6, ft11, ft10
	-[0x80005d10]:csrrs a0, fcsr, zero
	-[0x80005d14]:sw t6, 768(t1)
Current Store : [0x80005d18] : sw a0, 772(t1) -- Store: [0x8000a3e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005d4c]:feq.h t6, ft11, ft10
	-[0x80005d50]:csrrs a0, fcsr, zero
	-[0x80005d54]:sw t6, 776(t1)
Current Store : [0x80005d58] : sw a0, 780(t1) -- Store: [0x8000a3f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005d8c]:feq.h t6, ft11, ft10
	-[0x80005d90]:csrrs a0, fcsr, zero
	-[0x80005d94]:sw t6, 784(t1)
Current Store : [0x80005d98] : sw a0, 788(t1) -- Store: [0x8000a3f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005dcc]:feq.h t6, ft11, ft10
	-[0x80005dd0]:csrrs a0, fcsr, zero
	-[0x80005dd4]:sw t6, 792(t1)
Current Store : [0x80005dd8] : sw a0, 796(t1) -- Store: [0x8000a400]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005e0c]:feq.h t6, ft11, ft10
	-[0x80005e10]:csrrs a0, fcsr, zero
	-[0x80005e14]:sw t6, 800(t1)
Current Store : [0x80005e18] : sw a0, 804(t1) -- Store: [0x8000a408]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005e4c]:feq.h t6, ft11, ft10
	-[0x80005e50]:csrrs a0, fcsr, zero
	-[0x80005e54]:sw t6, 808(t1)
Current Store : [0x80005e58] : sw a0, 812(t1) -- Store: [0x8000a410]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005e8c]:feq.h t6, ft11, ft10
	-[0x80005e90]:csrrs a0, fcsr, zero
	-[0x80005e94]:sw t6, 816(t1)
Current Store : [0x80005e98] : sw a0, 820(t1) -- Store: [0x8000a418]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005ecc]:feq.h t6, ft11, ft10
	-[0x80005ed0]:csrrs a0, fcsr, zero
	-[0x80005ed4]:sw t6, 824(t1)
Current Store : [0x80005ed8] : sw a0, 828(t1) -- Store: [0x8000a420]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005f0c]:feq.h t6, ft11, ft10
	-[0x80005f10]:csrrs a0, fcsr, zero
	-[0x80005f14]:sw t6, 832(t1)
Current Store : [0x80005f18] : sw a0, 836(t1) -- Store: [0x8000a428]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005f4c]:feq.h t6, ft11, ft10
	-[0x80005f50]:csrrs a0, fcsr, zero
	-[0x80005f54]:sw t6, 840(t1)
Current Store : [0x80005f58] : sw a0, 844(t1) -- Store: [0x8000a430]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005f8c]:feq.h t6, ft11, ft10
	-[0x80005f90]:csrrs a0, fcsr, zero
	-[0x80005f94]:sw t6, 848(t1)
Current Store : [0x80005f98] : sw a0, 852(t1) -- Store: [0x8000a438]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80005fcc]:feq.h t6, ft11, ft10
	-[0x80005fd0]:csrrs a0, fcsr, zero
	-[0x80005fd4]:sw t6, 856(t1)
Current Store : [0x80005fd8] : sw a0, 860(t1) -- Store: [0x8000a440]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000600c]:feq.h t6, ft11, ft10
	-[0x80006010]:csrrs a0, fcsr, zero
	-[0x80006014]:sw t6, 864(t1)
Current Store : [0x80006018] : sw a0, 868(t1) -- Store: [0x8000a448]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000604c]:feq.h t6, ft11, ft10
	-[0x80006050]:csrrs a0, fcsr, zero
	-[0x80006054]:sw t6, 872(t1)
Current Store : [0x80006058] : sw a0, 876(t1) -- Store: [0x8000a450]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000608c]:feq.h t6, ft11, ft10
	-[0x80006090]:csrrs a0, fcsr, zero
	-[0x80006094]:sw t6, 880(t1)
Current Store : [0x80006098] : sw a0, 884(t1) -- Store: [0x8000a458]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800060cc]:feq.h t6, ft11, ft10
	-[0x800060d0]:csrrs a0, fcsr, zero
	-[0x800060d4]:sw t6, 888(t1)
Current Store : [0x800060d8] : sw a0, 892(t1) -- Store: [0x8000a460]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000610c]:feq.h t6, ft11, ft10
	-[0x80006110]:csrrs a0, fcsr, zero
	-[0x80006114]:sw t6, 896(t1)
Current Store : [0x80006118] : sw a0, 900(t1) -- Store: [0x8000a468]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000614c]:feq.h t6, ft11, ft10
	-[0x80006150]:csrrs a0, fcsr, zero
	-[0x80006154]:sw t6, 904(t1)
Current Store : [0x80006158] : sw a0, 908(t1) -- Store: [0x8000a470]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000618c]:feq.h t6, ft11, ft10
	-[0x80006190]:csrrs a0, fcsr, zero
	-[0x80006194]:sw t6, 912(t1)
Current Store : [0x80006198] : sw a0, 916(t1) -- Store: [0x8000a478]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800061cc]:feq.h t6, ft11, ft10
	-[0x800061d0]:csrrs a0, fcsr, zero
	-[0x800061d4]:sw t6, 920(t1)
Current Store : [0x800061d8] : sw a0, 924(t1) -- Store: [0x8000a480]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000620c]:feq.h t6, ft11, ft10
	-[0x80006210]:csrrs a0, fcsr, zero
	-[0x80006214]:sw t6, 928(t1)
Current Store : [0x80006218] : sw a0, 932(t1) -- Store: [0x8000a488]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000624c]:feq.h t6, ft11, ft10
	-[0x80006250]:csrrs a0, fcsr, zero
	-[0x80006254]:sw t6, 936(t1)
Current Store : [0x80006258] : sw a0, 940(t1) -- Store: [0x8000a490]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000628c]:feq.h t6, ft11, ft10
	-[0x80006290]:csrrs a0, fcsr, zero
	-[0x80006294]:sw t6, 944(t1)
Current Store : [0x80006298] : sw a0, 948(t1) -- Store: [0x8000a498]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800062cc]:feq.h t6, ft11, ft10
	-[0x800062d0]:csrrs a0, fcsr, zero
	-[0x800062d4]:sw t6, 952(t1)
Current Store : [0x800062d8] : sw a0, 956(t1) -- Store: [0x8000a4a0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000630c]:feq.h t6, ft11, ft10
	-[0x80006310]:csrrs a0, fcsr, zero
	-[0x80006314]:sw t6, 960(t1)
Current Store : [0x80006318] : sw a0, 964(t1) -- Store: [0x8000a4a8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000634c]:feq.h t6, ft11, ft10
	-[0x80006350]:csrrs a0, fcsr, zero
	-[0x80006354]:sw t6, 968(t1)
Current Store : [0x80006358] : sw a0, 972(t1) -- Store: [0x8000a4b0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000638c]:feq.h t6, ft11, ft10
	-[0x80006390]:csrrs a0, fcsr, zero
	-[0x80006394]:sw t6, 976(t1)
Current Store : [0x80006398] : sw a0, 980(t1) -- Store: [0x8000a4b8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800063cc]:feq.h t6, ft11, ft10
	-[0x800063d0]:csrrs a0, fcsr, zero
	-[0x800063d4]:sw t6, 984(t1)
Current Store : [0x800063d8] : sw a0, 988(t1) -- Store: [0x8000a4c0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000640c]:feq.h t6, ft11, ft10
	-[0x80006410]:csrrs a0, fcsr, zero
	-[0x80006414]:sw t6, 992(t1)
Current Store : [0x80006418] : sw a0, 996(t1) -- Store: [0x8000a4c8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006444]:feq.h t6, ft11, ft10
	-[0x80006448]:csrrs a0, fcsr, zero
	-[0x8000644c]:sw t6, 1000(t1)
Current Store : [0x80006450] : sw a0, 1004(t1) -- Store: [0x8000a4d0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000647c]:feq.h t6, ft11, ft10
	-[0x80006480]:csrrs a0, fcsr, zero
	-[0x80006484]:sw t6, 1008(t1)
Current Store : [0x80006488] : sw a0, 1012(t1) -- Store: [0x8000a4d8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800064b4]:feq.h t6, ft11, ft10
	-[0x800064b8]:csrrs a0, fcsr, zero
	-[0x800064bc]:sw t6, 1016(t1)
Current Store : [0x800064c0] : sw a0, 1020(t1) -- Store: [0x8000a4e0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800064f4]:feq.h t6, ft11, ft10
	-[0x800064f8]:csrrs a0, fcsr, zero
	-[0x800064fc]:sw t6, 0(t1)
Current Store : [0x80006500] : sw a0, 4(t1) -- Store: [0x8000a4e8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000652c]:feq.h t6, ft11, ft10
	-[0x80006530]:csrrs a0, fcsr, zero
	-[0x80006534]:sw t6, 8(t1)
Current Store : [0x80006538] : sw a0, 12(t1) -- Store: [0x8000a4f0]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006564]:feq.h t6, ft11, ft10
	-[0x80006568]:csrrs a0, fcsr, zero
	-[0x8000656c]:sw t6, 16(t1)
Current Store : [0x80006570] : sw a0, 20(t1) -- Store: [0x8000a4f8]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000659c]:feq.h t6, ft11, ft10
	-[0x800065a0]:csrrs a0, fcsr, zero
	-[0x800065a4]:sw t6, 24(t1)
Current Store : [0x800065a8] : sw a0, 28(t1) -- Store: [0x8000a500]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800065d4]:feq.h t6, ft11, ft10
	-[0x800065d8]:csrrs a0, fcsr, zero
	-[0x800065dc]:sw t6, 32(t1)
Current Store : [0x800065e0] : sw a0, 36(t1) -- Store: [0x8000a508]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000660c]:feq.h t6, ft11, ft10
	-[0x80006610]:csrrs a0, fcsr, zero
	-[0x80006614]:sw t6, 40(t1)
Current Store : [0x80006618] : sw a0, 44(t1) -- Store: [0x8000a510]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006644]:feq.h t6, ft11, ft10
	-[0x80006648]:csrrs a0, fcsr, zero
	-[0x8000664c]:sw t6, 48(t1)
Current Store : [0x80006650] : sw a0, 52(t1) -- Store: [0x8000a518]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000667c]:feq.h t6, ft11, ft10
	-[0x80006680]:csrrs a0, fcsr, zero
	-[0x80006684]:sw t6, 56(t1)
Current Store : [0x80006688] : sw a0, 60(t1) -- Store: [0x8000a520]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800066b4]:feq.h t6, ft11, ft10
	-[0x800066b8]:csrrs a0, fcsr, zero
	-[0x800066bc]:sw t6, 64(t1)
Current Store : [0x800066c0] : sw a0, 68(t1) -- Store: [0x8000a528]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800066ec]:feq.h t6, ft11, ft10
	-[0x800066f0]:csrrs a0, fcsr, zero
	-[0x800066f4]:sw t6, 72(t1)
Current Store : [0x800066f8] : sw a0, 76(t1) -- Store: [0x8000a530]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006724]:feq.h t6, ft11, ft10
	-[0x80006728]:csrrs a0, fcsr, zero
	-[0x8000672c]:sw t6, 80(t1)
Current Store : [0x80006730] : sw a0, 84(t1) -- Store: [0x8000a538]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000675c]:feq.h t6, ft11, ft10
	-[0x80006760]:csrrs a0, fcsr, zero
	-[0x80006764]:sw t6, 88(t1)
Current Store : [0x80006768] : sw a0, 92(t1) -- Store: [0x8000a540]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006794]:feq.h t6, ft11, ft10
	-[0x80006798]:csrrs a0, fcsr, zero
	-[0x8000679c]:sw t6, 96(t1)
Current Store : [0x800067a0] : sw a0, 100(t1) -- Store: [0x8000a548]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800067cc]:feq.h t6, ft11, ft10
	-[0x800067d0]:csrrs a0, fcsr, zero
	-[0x800067d4]:sw t6, 104(t1)
Current Store : [0x800067d8] : sw a0, 108(t1) -- Store: [0x8000a550]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006804]:feq.h t6, ft11, ft10
	-[0x80006808]:csrrs a0, fcsr, zero
	-[0x8000680c]:sw t6, 112(t1)
Current Store : [0x80006810] : sw a0, 116(t1) -- Store: [0x8000a558]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000683c]:feq.h t6, ft11, ft10
	-[0x80006840]:csrrs a0, fcsr, zero
	-[0x80006844]:sw t6, 120(t1)
Current Store : [0x80006848] : sw a0, 124(t1) -- Store: [0x8000a560]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006874]:feq.h t6, ft11, ft10
	-[0x80006878]:csrrs a0, fcsr, zero
	-[0x8000687c]:sw t6, 128(t1)
Current Store : [0x80006880] : sw a0, 132(t1) -- Store: [0x8000a568]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800068ac]:feq.h t6, ft11, ft10
	-[0x800068b0]:csrrs a0, fcsr, zero
	-[0x800068b4]:sw t6, 136(t1)
Current Store : [0x800068b8] : sw a0, 140(t1) -- Store: [0x8000a570]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800068e4]:feq.h t6, ft11, ft10
	-[0x800068e8]:csrrs a0, fcsr, zero
	-[0x800068ec]:sw t6, 144(t1)
Current Store : [0x800068f0] : sw a0, 148(t1) -- Store: [0x8000a578]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000691c]:feq.h t6, ft11, ft10
	-[0x80006920]:csrrs a0, fcsr, zero
	-[0x80006924]:sw t6, 152(t1)
Current Store : [0x80006928] : sw a0, 156(t1) -- Store: [0x8000a580]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006954]:feq.h t6, ft11, ft10
	-[0x80006958]:csrrs a0, fcsr, zero
	-[0x8000695c]:sw t6, 160(t1)
Current Store : [0x80006960] : sw a0, 164(t1) -- Store: [0x8000a588]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x8000698c]:feq.h t6, ft11, ft10
	-[0x80006990]:csrrs a0, fcsr, zero
	-[0x80006994]:sw t6, 168(t1)
Current Store : [0x80006998] : sw a0, 172(t1) -- Store: [0x8000a590]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800069c4]:feq.h t6, ft11, ft10
	-[0x800069c8]:csrrs a0, fcsr, zero
	-[0x800069cc]:sw t6, 176(t1)
Current Store : [0x800069d0] : sw a0, 180(t1) -- Store: [0x8000a598]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x800069fc]:feq.h t6, ft11, ft10
	-[0x80006a00]:csrrs a0, fcsr, zero
	-[0x80006a04]:sw t6, 184(t1)
Current Store : [0x80006a08] : sw a0, 188(t1) -- Store: [0x8000a5a0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006a34]:feq.h t6, ft11, ft10
	-[0x80006a38]:csrrs a0, fcsr, zero
	-[0x80006a3c]:sw t6, 192(t1)
Current Store : [0x80006a40] : sw a0, 196(t1) -- Store: [0x8000a5a8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006a6c]:feq.h t6, ft11, ft10
	-[0x80006a70]:csrrs a0, fcsr, zero
	-[0x80006a74]:sw t6, 200(t1)
Current Store : [0x80006a78] : sw a0, 204(t1) -- Store: [0x8000a5b0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006aa4]:feq.h t6, ft11, ft10
	-[0x80006aa8]:csrrs a0, fcsr, zero
	-[0x80006aac]:sw t6, 208(t1)
Current Store : [0x80006ab0] : sw a0, 212(t1) -- Store: [0x8000a5b8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006adc]:feq.h t6, ft11, ft10
	-[0x80006ae0]:csrrs a0, fcsr, zero
	-[0x80006ae4]:sw t6, 216(t1)
Current Store : [0x80006ae8] : sw a0, 220(t1) -- Store: [0x8000a5c0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006b14]:feq.h t6, ft11, ft10
	-[0x80006b18]:csrrs a0, fcsr, zero
	-[0x80006b1c]:sw t6, 224(t1)
Current Store : [0x80006b20] : sw a0, 228(t1) -- Store: [0x8000a5c8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006b4c]:feq.h t6, ft11, ft10
	-[0x80006b50]:csrrs a0, fcsr, zero
	-[0x80006b54]:sw t6, 232(t1)
Current Store : [0x80006b58] : sw a0, 236(t1) -- Store: [0x8000a5d0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006b84]:feq.h t6, ft11, ft10
	-[0x80006b88]:csrrs a0, fcsr, zero
	-[0x80006b8c]:sw t6, 240(t1)
Current Store : [0x80006b90] : sw a0, 244(t1) -- Store: [0x8000a5d8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006bbc]:feq.h t6, ft11, ft10
	-[0x80006bc0]:csrrs a0, fcsr, zero
	-[0x80006bc4]:sw t6, 248(t1)
Current Store : [0x80006bc8] : sw a0, 252(t1) -- Store: [0x8000a5e0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006bf4]:feq.h t6, ft11, ft10
	-[0x80006bf8]:csrrs a0, fcsr, zero
	-[0x80006bfc]:sw t6, 256(t1)
Current Store : [0x80006c00] : sw a0, 260(t1) -- Store: [0x8000a5e8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006c2c]:feq.h t6, ft11, ft10
	-[0x80006c30]:csrrs a0, fcsr, zero
	-[0x80006c34]:sw t6, 264(t1)
Current Store : [0x80006c38] : sw a0, 268(t1) -- Store: [0x8000a5f0]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006c64]:feq.h t6, ft11, ft10
	-[0x80006c68]:csrrs a0, fcsr, zero
	-[0x80006c6c]:sw t6, 272(t1)
Current Store : [0x80006c70] : sw a0, 276(t1) -- Store: [0x8000a5f8]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006c9c]:feq.h t6, ft11, ft10
	-[0x80006ca0]:csrrs a0, fcsr, zero
	-[0x80006ca4]:sw t6, 280(t1)
Current Store : [0x80006ca8] : sw a0, 284(t1) -- Store: [0x8000a600]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006cd4]:feq.h t6, ft11, ft10
	-[0x80006cd8]:csrrs a0, fcsr, zero
	-[0x80006cdc]:sw t6, 288(t1)
Current Store : [0x80006ce0] : sw a0, 292(t1) -- Store: [0x8000a608]:0x00000000




Last Coverpoint : ['fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006d0c]:feq.h t6, ft11, ft10
	-[0x80006d10]:csrrs a0, fcsr, zero
	-[0x80006d14]:sw t6, 296(t1)
Current Store : [0x80006d18] : sw a0, 300(t1) -- Store: [0x8000a610]:0x00000000




Last Coverpoint : ['fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006d44]:feq.h t6, ft11, ft10
	-[0x80006d48]:csrrs a0, fcsr, zero
	-[0x80006d4c]:sw t6, 304(t1)
Current Store : [0x80006d50] : sw a0, 308(t1) -- Store: [0x8000a618]:0x00000000




Last Coverpoint : ['mnemonic : feq.h', 'rs1 : f31', 'rs2 : f30', 'rd : x31', 'rs1 != rs2', 'fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat']
Last Code Sequence : 
	-[0x80006d7c]:feq.h t6, ft11, ft10
	-[0x80006d80]:csrrs a0, fcsr, zero
	-[0x80006d84]:sw t6, 312(t1)
Current Store : [0x80006d88] : sw a0, 316(t1) -- Store: [0x8000a620]:0x00000000





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
|   1|[0x80009414]<br>0x00000000|- mnemonic : feq.h<br> - rs1 : f31<br> - rs2 : f30<br> - rd : x31<br> - rs1 != rs2<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br> |[0x80000124]:feq.h t6, ft11, ft10<br> [0x80000128]:csrrs tp, fcsr, zero<br> [0x8000012c]:sw t6, 0(ra)<br>      |
|   2|[0x8000941c]<br>0x00000000|- rs1 : f29<br> - rs2 : f29<br> - rd : x30<br> - rs1 == rs2<br>                                                                                                                                                                                                       |[0x80000144]:feq.h t5, ft9, ft9<br> [0x80000148]:csrrs tp, fcsr, zero<br> [0x8000014c]:sw t5, 8(ra)<br>        |
|   3|[0x80009424]<br>0x00000000|- rs1 : f30<br> - rs2 : f31<br> - rd : x29<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000164]:feq.h t4, ft10, ft11<br> [0x80000168]:csrrs tp, fcsr, zero<br> [0x8000016c]:sw t4, 16(ra)<br>     |
|   4|[0x8000942c]<br>0x00000000|- rs1 : f28<br> - rs2 : f27<br> - rd : x28<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000184]:feq.h t3, ft8, fs11<br> [0x80000188]:csrrs tp, fcsr, zero<br> [0x8000018c]:sw t3, 24(ra)<br>      |
|   5|[0x80009434]<br>0x00000000|- rs1 : f27<br> - rs2 : f28<br> - rd : x27<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800001a4]:feq.h s11, fs11, ft8<br> [0x800001a8]:csrrs tp, fcsr, zero<br> [0x800001ac]:sw s11, 32(ra)<br>    |
|   6|[0x8000943c]<br>0x00000000|- rs1 : f26<br> - rs2 : f25<br> - rd : x26<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800001c4]:feq.h s10, fs10, fs9<br> [0x800001c8]:csrrs tp, fcsr, zero<br> [0x800001cc]:sw s10, 40(ra)<br>    |
|   7|[0x80009444]<br>0x00000000|- rs1 : f25<br> - rs2 : f26<br> - rd : x25<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800001e4]:feq.h s9, fs9, fs10<br> [0x800001e8]:csrrs tp, fcsr, zero<br> [0x800001ec]:sw s9, 48(ra)<br>      |
|   8|[0x8000944c]<br>0x00000000|- rs1 : f24<br> - rs2 : f23<br> - rd : x24<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000204]:feq.h s8, fs8, fs7<br> [0x80000208]:csrrs tp, fcsr, zero<br> [0x8000020c]:sw s8, 56(ra)<br>       |
|   9|[0x80009454]<br>0x00000000|- rs1 : f23<br> - rs2 : f24<br> - rd : x23<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000224]:feq.h s7, fs7, fs8<br> [0x80000228]:csrrs tp, fcsr, zero<br> [0x8000022c]:sw s7, 64(ra)<br>       |
|  10|[0x8000945c]<br>0x00000000|- rs1 : f22<br> - rs2 : f21<br> - rd : x22<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000244]:feq.h s6, fs6, fs5<br> [0x80000248]:csrrs tp, fcsr, zero<br> [0x8000024c]:sw s6, 72(ra)<br>       |
|  11|[0x80009464]<br>0x00000000|- rs1 : f21<br> - rs2 : f22<br> - rd : x21<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000264]:feq.h s5, fs5, fs6<br> [0x80000268]:csrrs tp, fcsr, zero<br> [0x8000026c]:sw s5, 80(ra)<br>       |
|  12|[0x8000946c]<br>0x00000000|- rs1 : f20<br> - rs2 : f19<br> - rd : x20<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000284]:feq.h s4, fs4, fs3<br> [0x80000288]:csrrs tp, fcsr, zero<br> [0x8000028c]:sw s4, 88(ra)<br>       |
|  13|[0x80009474]<br>0x00000000|- rs1 : f19<br> - rs2 : f20<br> - rd : x19<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800002a4]:feq.h s3, fs3, fs4<br> [0x800002a8]:csrrs tp, fcsr, zero<br> [0x800002ac]:sw s3, 96(ra)<br>       |
|  14|[0x8000947c]<br>0x00000000|- rs1 : f18<br> - rs2 : f17<br> - rd : x18<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800002c4]:feq.h s2, fs2, fa7<br> [0x800002c8]:csrrs tp, fcsr, zero<br> [0x800002cc]:sw s2, 104(ra)<br>      |
|  15|[0x80009484]<br>0x00000000|- rs1 : f17<br> - rs2 : f18<br> - rd : x17<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800002e4]:feq.h a7, fa7, fs2<br> [0x800002e8]:csrrs tp, fcsr, zero<br> [0x800002ec]:sw a7, 112(ra)<br>      |
|  16|[0x8000948c]<br>0x00000000|- rs1 : f16<br> - rs2 : f15<br> - rd : x16<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000304]:feq.h a6, fa6, fa5<br> [0x80000308]:csrrs tp, fcsr, zero<br> [0x8000030c]:sw a6, 120(ra)<br>      |
|  17|[0x80009494]<br>0x00000000|- rs1 : f15<br> - rs2 : f16<br> - rd : x15<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000324]:feq.h a5, fa5, fa6<br> [0x80000328]:csrrs tp, fcsr, zero<br> [0x8000032c]:sw a5, 128(ra)<br>      |
|  18|[0x8000949c]<br>0x00000000|- rs1 : f14<br> - rs2 : f13<br> - rd : x14<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000344]:feq.h a4, fa4, fa3<br> [0x80000348]:csrrs tp, fcsr, zero<br> [0x8000034c]:sw a4, 136(ra)<br>      |
|  19|[0x800094a4]<br>0x00000000|- rs1 : f13<br> - rs2 : f14<br> - rd : x13<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000364]:feq.h a3, fa3, fa4<br> [0x80000368]:csrrs tp, fcsr, zero<br> [0x8000036c]:sw a3, 144(ra)<br>      |
|  20|[0x800094ac]<br>0x00000000|- rs1 : f12<br> - rs2 : f11<br> - rd : x12<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x80000384]:feq.h a2, fa2, fa1<br> [0x80000388]:csrrs tp, fcsr, zero<br> [0x8000038c]:sw a2, 152(ra)<br>      |
|  21|[0x800094b4]<br>0x00000000|- rs1 : f11<br> - rs2 : f12<br> - rd : x11<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                         |[0x800003a4]:feq.h a1, fa1, fa2<br> [0x800003a8]:csrrs tp, fcsr, zero<br> [0x800003ac]:sw a1, 160(ra)<br>      |
|  22|[0x800094bc]<br>0x00000000|- rs1 : f10<br> - rs2 : f9<br> - rd : x10<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                          |[0x800003c4]:feq.h a0, fa0, fs1<br> [0x800003c8]:csrrs tp, fcsr, zero<br> [0x800003cc]:sw a0, 168(ra)<br>      |
|  23|[0x800094c4]<br>0x00000000|- rs1 : f9<br> - rs2 : f10<br> - rd : x9<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                           |[0x800003e4]:feq.h s1, fs1, fa0<br> [0x800003e8]:csrrs tp, fcsr, zero<br> [0x800003ec]:sw s1, 176(ra)<br>      |
|  24|[0x800094cc]<br>0x00000000|- rs1 : f8<br> - rs2 : f7<br> - rd : x8<br> - fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x8000040c]:feq.h fp, fs0, ft7<br> [0x80000410]:csrrs a0, fcsr, zero<br> [0x80000414]:sw fp, 184(ra)<br>      |
|  25|[0x800094d4]<br>0x00000000|- rs1 : f7<br> - rs2 : f8<br> - rd : x7<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x8000042c]:feq.h t2, ft7, fs0<br> [0x80000430]:csrrs a0, fcsr, zero<br> [0x80000434]:sw t2, 192(ra)<br>      |
|  26|[0x800094dc]<br>0x00000000|- rs1 : f6<br> - rs2 : f5<br> - rd : x6<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x8000044c]:feq.h t1, ft6, ft5<br> [0x80000450]:csrrs a0, fcsr, zero<br> [0x80000454]:sw t1, 200(ra)<br>      |
|  27|[0x800094e4]<br>0x00000000|- rs1 : f5<br> - rs2 : f6<br> - rd : x5<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x80000474]:feq.h t0, ft5, ft6<br> [0x80000478]:csrrs a0, fcsr, zero<br> [0x8000047c]:sw t0, 0(t1)<br>        |
|  28|[0x800094ec]<br>0x00000000|- rs1 : f4<br> - rs2 : f3<br> - rd : x4<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x80000494]:feq.h tp, ft4, ft3<br> [0x80000498]:csrrs a0, fcsr, zero<br> [0x8000049c]:sw tp, 8(t1)<br>        |
|  29|[0x800094f4]<br>0x00000000|- rs1 : f3<br> - rs2 : f4<br> - rd : x3<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x800004b4]:feq.h gp, ft3, ft4<br> [0x800004b8]:csrrs a0, fcsr, zero<br> [0x800004bc]:sw gp, 16(t1)<br>       |
|  30|[0x800094fc]<br>0x00000000|- rs1 : f2<br> - rs2 : f1<br> - rd : x2<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x800004d4]:feq.h sp, ft2, ft1<br> [0x800004d8]:csrrs a0, fcsr, zero<br> [0x800004dc]:sw sp, 24(t1)<br>       |
|  31|[0x80009504]<br>0x00000000|- rs1 : f1<br> - rs2 : f2<br> - rd : x1<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                            |[0x800004f4]:feq.h ra, ft1, ft2<br> [0x800004f8]:csrrs a0, fcsr, zero<br> [0x800004fc]:sw ra, 32(t1)<br>       |
|  32|[0x8000950c]<br>0x00000000|- rs1 : f0<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                         |[0x80000514]:feq.h t6, ft0, ft11<br> [0x80000518]:csrrs a0, fcsr, zero<br> [0x8000051c]:sw t6, 40(t1)<br>      |
|  33|[0x80009514]<br>0x00000000|- rs2 : f0<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                         |[0x80000534]:feq.h t6, ft11, ft0<br> [0x80000538]:csrrs a0, fcsr, zero<br> [0x8000053c]:sw t6, 48(t1)<br>      |
|  34|[0x8000951c]<br>0x00000000|- rd : x0<br> - fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                          |[0x80000554]:feq.h zero, ft11, ft10<br> [0x80000558]:csrrs a0, fcsr, zero<br> [0x8000055c]:sw zero, 56(t1)<br> |
|  35|[0x80009524]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000574]:feq.h t6, ft11, ft10<br> [0x80000578]:csrrs a0, fcsr, zero<br> [0x8000057c]:sw t6, 64(t1)<br>     |
|  36|[0x8000952c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000594]:feq.h t6, ft11, ft10<br> [0x80000598]:csrrs a0, fcsr, zero<br> [0x8000059c]:sw t6, 72(t1)<br>     |
|  37|[0x80009534]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800005b4]:feq.h t6, ft11, ft10<br> [0x800005b8]:csrrs a0, fcsr, zero<br> [0x800005bc]:sw t6, 80(t1)<br>     |
|  38|[0x8000953c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800005d4]:feq.h t6, ft11, ft10<br> [0x800005d8]:csrrs a0, fcsr, zero<br> [0x800005dc]:sw t6, 88(t1)<br>     |
|  39|[0x80009544]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800005f4]:feq.h t6, ft11, ft10<br> [0x800005f8]:csrrs a0, fcsr, zero<br> [0x800005fc]:sw t6, 96(t1)<br>     |
|  40|[0x8000954c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000614]:feq.h t6, ft11, ft10<br> [0x80000618]:csrrs a0, fcsr, zero<br> [0x8000061c]:sw t6, 104(t1)<br>    |
|  41|[0x80009554]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000634]:feq.h t6, ft11, ft10<br> [0x80000638]:csrrs a0, fcsr, zero<br> [0x8000063c]:sw t6, 112(t1)<br>    |
|  42|[0x8000955c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000654]:feq.h t6, ft11, ft10<br> [0x80000658]:csrrs a0, fcsr, zero<br> [0x8000065c]:sw t6, 120(t1)<br>    |
|  43|[0x80009564]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000674]:feq.h t6, ft11, ft10<br> [0x80000678]:csrrs a0, fcsr, zero<br> [0x8000067c]:sw t6, 128(t1)<br>    |
|  44|[0x8000956c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000694]:feq.h t6, ft11, ft10<br> [0x80000698]:csrrs a0, fcsr, zero<br> [0x8000069c]:sw t6, 136(t1)<br>    |
|  45|[0x80009574]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800006b4]:feq.h t6, ft11, ft10<br> [0x800006b8]:csrrs a0, fcsr, zero<br> [0x800006bc]:sw t6, 144(t1)<br>    |
|  46|[0x8000957c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800006d4]:feq.h t6, ft11, ft10<br> [0x800006d8]:csrrs a0, fcsr, zero<br> [0x800006dc]:sw t6, 152(t1)<br>    |
|  47|[0x80009584]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800006f4]:feq.h t6, ft11, ft10<br> [0x800006f8]:csrrs a0, fcsr, zero<br> [0x800006fc]:sw t6, 160(t1)<br>    |
|  48|[0x8000958c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000714]:feq.h t6, ft11, ft10<br> [0x80000718]:csrrs a0, fcsr, zero<br> [0x8000071c]:sw t6, 168(t1)<br>    |
|  49|[0x80009594]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000734]:feq.h t6, ft11, ft10<br> [0x80000738]:csrrs a0, fcsr, zero<br> [0x8000073c]:sw t6, 176(t1)<br>    |
|  50|[0x8000959c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000754]:feq.h t6, ft11, ft10<br> [0x80000758]:csrrs a0, fcsr, zero<br> [0x8000075c]:sw t6, 184(t1)<br>    |
|  51|[0x800095a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000774]:feq.h t6, ft11, ft10<br> [0x80000778]:csrrs a0, fcsr, zero<br> [0x8000077c]:sw t6, 192(t1)<br>    |
|  52|[0x800095ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000794]:feq.h t6, ft11, ft10<br> [0x80000798]:csrrs a0, fcsr, zero<br> [0x8000079c]:sw t6, 200(t1)<br>    |
|  53|[0x800095b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800007b4]:feq.h t6, ft11, ft10<br> [0x800007b8]:csrrs a0, fcsr, zero<br> [0x800007bc]:sw t6, 208(t1)<br>    |
|  54|[0x800095bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800007d4]:feq.h t6, ft11, ft10<br> [0x800007d8]:csrrs a0, fcsr, zero<br> [0x800007dc]:sw t6, 216(t1)<br>    |
|  55|[0x800095c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800007f4]:feq.h t6, ft11, ft10<br> [0x800007f8]:csrrs a0, fcsr, zero<br> [0x800007fc]:sw t6, 224(t1)<br>    |
|  56|[0x800095cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000814]:feq.h t6, ft11, ft10<br> [0x80000818]:csrrs a0, fcsr, zero<br> [0x8000081c]:sw t6, 232(t1)<br>    |
|  57|[0x800095d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000834]:feq.h t6, ft11, ft10<br> [0x80000838]:csrrs a0, fcsr, zero<br> [0x8000083c]:sw t6, 240(t1)<br>    |
|  58|[0x800095dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000854]:feq.h t6, ft11, ft10<br> [0x80000858]:csrrs a0, fcsr, zero<br> [0x8000085c]:sw t6, 248(t1)<br>    |
|  59|[0x800095e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000874]:feq.h t6, ft11, ft10<br> [0x80000878]:csrrs a0, fcsr, zero<br> [0x8000087c]:sw t6, 256(t1)<br>    |
|  60|[0x800095ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000894]:feq.h t6, ft11, ft10<br> [0x80000898]:csrrs a0, fcsr, zero<br> [0x8000089c]:sw t6, 264(t1)<br>    |
|  61|[0x800095f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800008b4]:feq.h t6, ft11, ft10<br> [0x800008b8]:csrrs a0, fcsr, zero<br> [0x800008bc]:sw t6, 272(t1)<br>    |
|  62|[0x800095fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800008d4]:feq.h t6, ft11, ft10<br> [0x800008d8]:csrrs a0, fcsr, zero<br> [0x800008dc]:sw t6, 280(t1)<br>    |
|  63|[0x80009604]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800008f4]:feq.h t6, ft11, ft10<br> [0x800008f8]:csrrs a0, fcsr, zero<br> [0x800008fc]:sw t6, 288(t1)<br>    |
|  64|[0x8000960c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000914]:feq.h t6, ft11, ft10<br> [0x80000918]:csrrs a0, fcsr, zero<br> [0x8000091c]:sw t6, 296(t1)<br>    |
|  65|[0x80009614]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000934]:feq.h t6, ft11, ft10<br> [0x80000938]:csrrs a0, fcsr, zero<br> [0x8000093c]:sw t6, 304(t1)<br>    |
|  66|[0x8000961c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000954]:feq.h t6, ft11, ft10<br> [0x80000958]:csrrs a0, fcsr, zero<br> [0x8000095c]:sw t6, 312(t1)<br>    |
|  67|[0x80009624]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000974]:feq.h t6, ft11, ft10<br> [0x80000978]:csrrs a0, fcsr, zero<br> [0x8000097c]:sw t6, 320(t1)<br>    |
|  68|[0x8000962c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000994]:feq.h t6, ft11, ft10<br> [0x80000998]:csrrs a0, fcsr, zero<br> [0x8000099c]:sw t6, 328(t1)<br>    |
|  69|[0x80009634]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800009b4]:feq.h t6, ft11, ft10<br> [0x800009b8]:csrrs a0, fcsr, zero<br> [0x800009bc]:sw t6, 336(t1)<br>    |
|  70|[0x8000963c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800009d4]:feq.h t6, ft11, ft10<br> [0x800009d8]:csrrs a0, fcsr, zero<br> [0x800009dc]:sw t6, 344(t1)<br>    |
|  71|[0x80009644]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800009f4]:feq.h t6, ft11, ft10<br> [0x800009f8]:csrrs a0, fcsr, zero<br> [0x800009fc]:sw t6, 352(t1)<br>    |
|  72|[0x8000964c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a14]:feq.h t6, ft11, ft10<br> [0x80000a18]:csrrs a0, fcsr, zero<br> [0x80000a1c]:sw t6, 360(t1)<br>    |
|  73|[0x80009654]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a34]:feq.h t6, ft11, ft10<br> [0x80000a38]:csrrs a0, fcsr, zero<br> [0x80000a3c]:sw t6, 368(t1)<br>    |
|  74|[0x8000965c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a54]:feq.h t6, ft11, ft10<br> [0x80000a58]:csrrs a0, fcsr, zero<br> [0x80000a5c]:sw t6, 376(t1)<br>    |
|  75|[0x80009664]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a74]:feq.h t6, ft11, ft10<br> [0x80000a78]:csrrs a0, fcsr, zero<br> [0x80000a7c]:sw t6, 384(t1)<br>    |
|  76|[0x8000966c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000a94]:feq.h t6, ft11, ft10<br> [0x80000a98]:csrrs a0, fcsr, zero<br> [0x80000a9c]:sw t6, 392(t1)<br>    |
|  77|[0x80009674]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ab4]:feq.h t6, ft11, ft10<br> [0x80000ab8]:csrrs a0, fcsr, zero<br> [0x80000abc]:sw t6, 400(t1)<br>    |
|  78|[0x8000967c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ad4]:feq.h t6, ft11, ft10<br> [0x80000ad8]:csrrs a0, fcsr, zero<br> [0x80000adc]:sw t6, 408(t1)<br>    |
|  79|[0x80009684]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000af4]:feq.h t6, ft11, ft10<br> [0x80000af8]:csrrs a0, fcsr, zero<br> [0x80000afc]:sw t6, 416(t1)<br>    |
|  80|[0x8000968c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b14]:feq.h t6, ft11, ft10<br> [0x80000b18]:csrrs a0, fcsr, zero<br> [0x80000b1c]:sw t6, 424(t1)<br>    |
|  81|[0x80009694]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b34]:feq.h t6, ft11, ft10<br> [0x80000b38]:csrrs a0, fcsr, zero<br> [0x80000b3c]:sw t6, 432(t1)<br>    |
|  82|[0x8000969c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b54]:feq.h t6, ft11, ft10<br> [0x80000b58]:csrrs a0, fcsr, zero<br> [0x80000b5c]:sw t6, 440(t1)<br>    |
|  83|[0x800096a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b74]:feq.h t6, ft11, ft10<br> [0x80000b78]:csrrs a0, fcsr, zero<br> [0x80000b7c]:sw t6, 448(t1)<br>    |
|  84|[0x800096ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000b94]:feq.h t6, ft11, ft10<br> [0x80000b98]:csrrs a0, fcsr, zero<br> [0x80000b9c]:sw t6, 456(t1)<br>    |
|  85|[0x800096b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000bb4]:feq.h t6, ft11, ft10<br> [0x80000bb8]:csrrs a0, fcsr, zero<br> [0x80000bbc]:sw t6, 464(t1)<br>    |
|  86|[0x800096bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000bd4]:feq.h t6, ft11, ft10<br> [0x80000bd8]:csrrs a0, fcsr, zero<br> [0x80000bdc]:sw t6, 472(t1)<br>    |
|  87|[0x800096c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000bf4]:feq.h t6, ft11, ft10<br> [0x80000bf8]:csrrs a0, fcsr, zero<br> [0x80000bfc]:sw t6, 480(t1)<br>    |
|  88|[0x800096cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c14]:feq.h t6, ft11, ft10<br> [0x80000c18]:csrrs a0, fcsr, zero<br> [0x80000c1c]:sw t6, 488(t1)<br>    |
|  89|[0x800096d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c34]:feq.h t6, ft11, ft10<br> [0x80000c38]:csrrs a0, fcsr, zero<br> [0x80000c3c]:sw t6, 496(t1)<br>    |
|  90|[0x800096dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c54]:feq.h t6, ft11, ft10<br> [0x80000c58]:csrrs a0, fcsr, zero<br> [0x80000c5c]:sw t6, 504(t1)<br>    |
|  91|[0x800096e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c74]:feq.h t6, ft11, ft10<br> [0x80000c78]:csrrs a0, fcsr, zero<br> [0x80000c7c]:sw t6, 512(t1)<br>    |
|  92|[0x800096ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000c94]:feq.h t6, ft11, ft10<br> [0x80000c98]:csrrs a0, fcsr, zero<br> [0x80000c9c]:sw t6, 520(t1)<br>    |
|  93|[0x800096f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000cb4]:feq.h t6, ft11, ft10<br> [0x80000cb8]:csrrs a0, fcsr, zero<br> [0x80000cbc]:sw t6, 528(t1)<br>    |
|  94|[0x800096fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000cd4]:feq.h t6, ft11, ft10<br> [0x80000cd8]:csrrs a0, fcsr, zero<br> [0x80000cdc]:sw t6, 536(t1)<br>    |
|  95|[0x80009704]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000cf4]:feq.h t6, ft11, ft10<br> [0x80000cf8]:csrrs a0, fcsr, zero<br> [0x80000cfc]:sw t6, 544(t1)<br>    |
|  96|[0x8000970c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d14]:feq.h t6, ft11, ft10<br> [0x80000d18]:csrrs a0, fcsr, zero<br> [0x80000d1c]:sw t6, 552(t1)<br>    |
|  97|[0x80009714]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d34]:feq.h t6, ft11, ft10<br> [0x80000d38]:csrrs a0, fcsr, zero<br> [0x80000d3c]:sw t6, 560(t1)<br>    |
|  98|[0x8000971c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d54]:feq.h t6, ft11, ft10<br> [0x80000d58]:csrrs a0, fcsr, zero<br> [0x80000d5c]:sw t6, 568(t1)<br>    |
|  99|[0x80009724]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d74]:feq.h t6, ft11, ft10<br> [0x80000d78]:csrrs a0, fcsr, zero<br> [0x80000d7c]:sw t6, 576(t1)<br>    |
| 100|[0x8000972c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000d94]:feq.h t6, ft11, ft10<br> [0x80000d98]:csrrs a0, fcsr, zero<br> [0x80000d9c]:sw t6, 584(t1)<br>    |
| 101|[0x80009734]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000db4]:feq.h t6, ft11, ft10<br> [0x80000db8]:csrrs a0, fcsr, zero<br> [0x80000dbc]:sw t6, 592(t1)<br>    |
| 102|[0x8000973c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000dd4]:feq.h t6, ft11, ft10<br> [0x80000dd8]:csrrs a0, fcsr, zero<br> [0x80000ddc]:sw t6, 600(t1)<br>    |
| 103|[0x80009744]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000df4]:feq.h t6, ft11, ft10<br> [0x80000df8]:csrrs a0, fcsr, zero<br> [0x80000dfc]:sw t6, 608(t1)<br>    |
| 104|[0x8000974c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e14]:feq.h t6, ft11, ft10<br> [0x80000e18]:csrrs a0, fcsr, zero<br> [0x80000e1c]:sw t6, 616(t1)<br>    |
| 105|[0x80009754]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e34]:feq.h t6, ft11, ft10<br> [0x80000e38]:csrrs a0, fcsr, zero<br> [0x80000e3c]:sw t6, 624(t1)<br>    |
| 106|[0x8000975c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e54]:feq.h t6, ft11, ft10<br> [0x80000e58]:csrrs a0, fcsr, zero<br> [0x80000e5c]:sw t6, 632(t1)<br>    |
| 107|[0x80009764]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e74]:feq.h t6, ft11, ft10<br> [0x80000e78]:csrrs a0, fcsr, zero<br> [0x80000e7c]:sw t6, 640(t1)<br>    |
| 108|[0x8000976c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000e94]:feq.h t6, ft11, ft10<br> [0x80000e98]:csrrs a0, fcsr, zero<br> [0x80000e9c]:sw t6, 648(t1)<br>    |
| 109|[0x80009774]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000eb4]:feq.h t6, ft11, ft10<br> [0x80000eb8]:csrrs a0, fcsr, zero<br> [0x80000ebc]:sw t6, 656(t1)<br>    |
| 110|[0x8000977c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ed4]:feq.h t6, ft11, ft10<br> [0x80000ed8]:csrrs a0, fcsr, zero<br> [0x80000edc]:sw t6, 664(t1)<br>    |
| 111|[0x80009784]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ef4]:feq.h t6, ft11, ft10<br> [0x80000ef8]:csrrs a0, fcsr, zero<br> [0x80000efc]:sw t6, 672(t1)<br>    |
| 112|[0x8000978c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f14]:feq.h t6, ft11, ft10<br> [0x80000f18]:csrrs a0, fcsr, zero<br> [0x80000f1c]:sw t6, 680(t1)<br>    |
| 113|[0x80009794]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f34]:feq.h t6, ft11, ft10<br> [0x80000f38]:csrrs a0, fcsr, zero<br> [0x80000f3c]:sw t6, 688(t1)<br>    |
| 114|[0x8000979c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f54]:feq.h t6, ft11, ft10<br> [0x80000f58]:csrrs a0, fcsr, zero<br> [0x80000f5c]:sw t6, 696(t1)<br>    |
| 115|[0x800097a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f74]:feq.h t6, ft11, ft10<br> [0x80000f78]:csrrs a0, fcsr, zero<br> [0x80000f7c]:sw t6, 704(t1)<br>    |
| 116|[0x800097ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000f94]:feq.h t6, ft11, ft10<br> [0x80000f98]:csrrs a0, fcsr, zero<br> [0x80000f9c]:sw t6, 712(t1)<br>    |
| 117|[0x800097b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000fb4]:feq.h t6, ft11, ft10<br> [0x80000fb8]:csrrs a0, fcsr, zero<br> [0x80000fbc]:sw t6, 720(t1)<br>    |
| 118|[0x800097bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000fd4]:feq.h t6, ft11, ft10<br> [0x80000fd8]:csrrs a0, fcsr, zero<br> [0x80000fdc]:sw t6, 728(t1)<br>    |
| 119|[0x800097c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80000ff4]:feq.h t6, ft11, ft10<br> [0x80000ff8]:csrrs a0, fcsr, zero<br> [0x80000ffc]:sw t6, 736(t1)<br>    |
| 120|[0x800097cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x002 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001014]:feq.h t6, ft11, ft10<br> [0x80001018]:csrrs a0, fcsr, zero<br> [0x8000101c]:sw t6, 744(t1)<br>    |
| 121|[0x800097d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001034]:feq.h t6, ft11, ft10<br> [0x80001038]:csrrs a0, fcsr, zero<br> [0x8000103c]:sw t6, 752(t1)<br>    |
| 122|[0x800097dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001054]:feq.h t6, ft11, ft10<br> [0x80001058]:csrrs a0, fcsr, zero<br> [0x8000105c]:sw t6, 760(t1)<br>    |
| 123|[0x800097e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001074]:feq.h t6, ft11, ft10<br> [0x80001078]:csrrs a0, fcsr, zero<br> [0x8000107c]:sw t6, 768(t1)<br>    |
| 124|[0x800097ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001094]:feq.h t6, ft11, ft10<br> [0x80001098]:csrrs a0, fcsr, zero<br> [0x8000109c]:sw t6, 776(t1)<br>    |
| 125|[0x800097f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800010b4]:feq.h t6, ft11, ft10<br> [0x800010b8]:csrrs a0, fcsr, zero<br> [0x800010bc]:sw t6, 784(t1)<br>    |
| 126|[0x800097fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800010d4]:feq.h t6, ft11, ft10<br> [0x800010d8]:csrrs a0, fcsr, zero<br> [0x800010dc]:sw t6, 792(t1)<br>    |
| 127|[0x80009804]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800010f4]:feq.h t6, ft11, ft10<br> [0x800010f8]:csrrs a0, fcsr, zero<br> [0x800010fc]:sw t6, 800(t1)<br>    |
| 128|[0x8000980c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001114]:feq.h t6, ft11, ft10<br> [0x80001118]:csrrs a0, fcsr, zero<br> [0x8000111c]:sw t6, 808(t1)<br>    |
| 129|[0x80009814]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001134]:feq.h t6, ft11, ft10<br> [0x80001138]:csrrs a0, fcsr, zero<br> [0x8000113c]:sw t6, 816(t1)<br>    |
| 130|[0x8000981c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001154]:feq.h t6, ft11, ft10<br> [0x80001158]:csrrs a0, fcsr, zero<br> [0x8000115c]:sw t6, 824(t1)<br>    |
| 131|[0x80009824]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001174]:feq.h t6, ft11, ft10<br> [0x80001178]:csrrs a0, fcsr, zero<br> [0x8000117c]:sw t6, 832(t1)<br>    |
| 132|[0x8000982c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001194]:feq.h t6, ft11, ft10<br> [0x80001198]:csrrs a0, fcsr, zero<br> [0x8000119c]:sw t6, 840(t1)<br>    |
| 133|[0x80009834]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800011b4]:feq.h t6, ft11, ft10<br> [0x800011b8]:csrrs a0, fcsr, zero<br> [0x800011bc]:sw t6, 848(t1)<br>    |
| 134|[0x8000983c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800011d4]:feq.h t6, ft11, ft10<br> [0x800011d8]:csrrs a0, fcsr, zero<br> [0x800011dc]:sw t6, 856(t1)<br>    |
| 135|[0x80009844]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800011f4]:feq.h t6, ft11, ft10<br> [0x800011f8]:csrrs a0, fcsr, zero<br> [0x800011fc]:sw t6, 864(t1)<br>    |
| 136|[0x8000984c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001214]:feq.h t6, ft11, ft10<br> [0x80001218]:csrrs a0, fcsr, zero<br> [0x8000121c]:sw t6, 872(t1)<br>    |
| 137|[0x80009854]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001234]:feq.h t6, ft11, ft10<br> [0x80001238]:csrrs a0, fcsr, zero<br> [0x8000123c]:sw t6, 880(t1)<br>    |
| 138|[0x8000985c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001254]:feq.h t6, ft11, ft10<br> [0x80001258]:csrrs a0, fcsr, zero<br> [0x8000125c]:sw t6, 888(t1)<br>    |
| 139|[0x80009864]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001274]:feq.h t6, ft11, ft10<br> [0x80001278]:csrrs a0, fcsr, zero<br> [0x8000127c]:sw t6, 896(t1)<br>    |
| 140|[0x8000986c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001294]:feq.h t6, ft11, ft10<br> [0x80001298]:csrrs a0, fcsr, zero<br> [0x8000129c]:sw t6, 904(t1)<br>    |
| 141|[0x80009874]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800012b4]:feq.h t6, ft11, ft10<br> [0x800012b8]:csrrs a0, fcsr, zero<br> [0x800012bc]:sw t6, 912(t1)<br>    |
| 142|[0x8000987c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800012d4]:feq.h t6, ft11, ft10<br> [0x800012d8]:csrrs a0, fcsr, zero<br> [0x800012dc]:sw t6, 920(t1)<br>    |
| 143|[0x80009884]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800012f4]:feq.h t6, ft11, ft10<br> [0x800012f8]:csrrs a0, fcsr, zero<br> [0x800012fc]:sw t6, 928(t1)<br>    |
| 144|[0x8000988c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3fe and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001314]:feq.h t6, ft11, ft10<br> [0x80001318]:csrrs a0, fcsr, zero<br> [0x8000131c]:sw t6, 936(t1)<br>    |
| 145|[0x80009894]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001334]:feq.h t6, ft11, ft10<br> [0x80001338]:csrrs a0, fcsr, zero<br> [0x8000133c]:sw t6, 944(t1)<br>    |
| 146|[0x8000989c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001354]:feq.h t6, ft11, ft10<br> [0x80001358]:csrrs a0, fcsr, zero<br> [0x8000135c]:sw t6, 952(t1)<br>    |
| 147|[0x800098a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001374]:feq.h t6, ft11, ft10<br> [0x80001378]:csrrs a0, fcsr, zero<br> [0x8000137c]:sw t6, 960(t1)<br>    |
| 148|[0x800098ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001394]:feq.h t6, ft11, ft10<br> [0x80001398]:csrrs a0, fcsr, zero<br> [0x8000139c]:sw t6, 968(t1)<br>    |
| 149|[0x800098b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800013b4]:feq.h t6, ft11, ft10<br> [0x800013b8]:csrrs a0, fcsr, zero<br> [0x800013bc]:sw t6, 976(t1)<br>    |
| 150|[0x800098bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800013d4]:feq.h t6, ft11, ft10<br> [0x800013d8]:csrrs a0, fcsr, zero<br> [0x800013dc]:sw t6, 984(t1)<br>    |
| 151|[0x800098c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800013f4]:feq.h t6, ft11, ft10<br> [0x800013f8]:csrrs a0, fcsr, zero<br> [0x800013fc]:sw t6, 992(t1)<br>    |
| 152|[0x800098cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001414]:feq.h t6, ft11, ft10<br> [0x80001418]:csrrs a0, fcsr, zero<br> [0x8000141c]:sw t6, 1000(t1)<br>   |
| 153|[0x800098d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001434]:feq.h t6, ft11, ft10<br> [0x80001438]:csrrs a0, fcsr, zero<br> [0x8000143c]:sw t6, 1008(t1)<br>   |
| 154|[0x800098dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001454]:feq.h t6, ft11, ft10<br> [0x80001458]:csrrs a0, fcsr, zero<br> [0x8000145c]:sw t6, 1016(t1)<br>   |
| 155|[0x800098e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000147c]:feq.h t6, ft11, ft10<br> [0x80001480]:csrrs a0, fcsr, zero<br> [0x80001484]:sw t6, 0(t1)<br>      |
| 156|[0x800098ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000149c]:feq.h t6, ft11, ft10<br> [0x800014a0]:csrrs a0, fcsr, zero<br> [0x800014a4]:sw t6, 8(t1)<br>      |
| 157|[0x800098f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800014bc]:feq.h t6, ft11, ft10<br> [0x800014c0]:csrrs a0, fcsr, zero<br> [0x800014c4]:sw t6, 16(t1)<br>     |
| 158|[0x800098fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800014dc]:feq.h t6, ft11, ft10<br> [0x800014e0]:csrrs a0, fcsr, zero<br> [0x800014e4]:sw t6, 24(t1)<br>     |
| 159|[0x80009904]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800014fc]:feq.h t6, ft11, ft10<br> [0x80001500]:csrrs a0, fcsr, zero<br> [0x80001504]:sw t6, 32(t1)<br>     |
| 160|[0x8000990c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000151c]:feq.h t6, ft11, ft10<br> [0x80001520]:csrrs a0, fcsr, zero<br> [0x80001524]:sw t6, 40(t1)<br>     |
| 161|[0x80009914]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000153c]:feq.h t6, ft11, ft10<br> [0x80001540]:csrrs a0, fcsr, zero<br> [0x80001544]:sw t6, 48(t1)<br>     |
| 162|[0x8000991c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000155c]:feq.h t6, ft11, ft10<br> [0x80001560]:csrrs a0, fcsr, zero<br> [0x80001564]:sw t6, 56(t1)<br>     |
| 163|[0x80009924]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000157c]:feq.h t6, ft11, ft10<br> [0x80001580]:csrrs a0, fcsr, zero<br> [0x80001584]:sw t6, 64(t1)<br>     |
| 164|[0x8000992c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000159c]:feq.h t6, ft11, ft10<br> [0x800015a0]:csrrs a0, fcsr, zero<br> [0x800015a4]:sw t6, 72(t1)<br>     |
| 165|[0x80009934]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800015bc]:feq.h t6, ft11, ft10<br> [0x800015c0]:csrrs a0, fcsr, zero<br> [0x800015c4]:sw t6, 80(t1)<br>     |
| 166|[0x8000993c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800015dc]:feq.h t6, ft11, ft10<br> [0x800015e0]:csrrs a0, fcsr, zero<br> [0x800015e4]:sw t6, 88(t1)<br>     |
| 167|[0x80009944]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800015fc]:feq.h t6, ft11, ft10<br> [0x80001600]:csrrs a0, fcsr, zero<br> [0x80001604]:sw t6, 96(t1)<br>     |
| 168|[0x8000994c]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000161c]:feq.h t6, ft11, ft10<br> [0x80001620]:csrrs a0, fcsr, zero<br> [0x80001624]:sw t6, 104(t1)<br>    |
| 169|[0x80009954]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000163c]:feq.h t6, ft11, ft10<br> [0x80001640]:csrrs a0, fcsr, zero<br> [0x80001644]:sw t6, 112(t1)<br>    |
| 170|[0x8000995c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000165c]:feq.h t6, ft11, ft10<br> [0x80001660]:csrrs a0, fcsr, zero<br> [0x80001664]:sw t6, 120(t1)<br>    |
| 171|[0x80009964]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000167c]:feq.h t6, ft11, ft10<br> [0x80001680]:csrrs a0, fcsr, zero<br> [0x80001684]:sw t6, 128(t1)<br>    |
| 172|[0x8000996c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000169c]:feq.h t6, ft11, ft10<br> [0x800016a0]:csrrs a0, fcsr, zero<br> [0x800016a4]:sw t6, 136(t1)<br>    |
| 173|[0x80009974]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800016bc]:feq.h t6, ft11, ft10<br> [0x800016c0]:csrrs a0, fcsr, zero<br> [0x800016c4]:sw t6, 144(t1)<br>    |
| 174|[0x8000997c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800016dc]:feq.h t6, ft11, ft10<br> [0x800016e0]:csrrs a0, fcsr, zero<br> [0x800016e4]:sw t6, 152(t1)<br>    |
| 175|[0x80009984]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800016fc]:feq.h t6, ft11, ft10<br> [0x80001700]:csrrs a0, fcsr, zero<br> [0x80001704]:sw t6, 160(t1)<br>    |
| 176|[0x8000998c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000171c]:feq.h t6, ft11, ft10<br> [0x80001720]:csrrs a0, fcsr, zero<br> [0x80001724]:sw t6, 168(t1)<br>    |
| 177|[0x80009994]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000173c]:feq.h t6, ft11, ft10<br> [0x80001740]:csrrs a0, fcsr, zero<br> [0x80001744]:sw t6, 176(t1)<br>    |
| 178|[0x8000999c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000175c]:feq.h t6, ft11, ft10<br> [0x80001760]:csrrs a0, fcsr, zero<br> [0x80001764]:sw t6, 184(t1)<br>    |
| 179|[0x800099a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000177c]:feq.h t6, ft11, ft10<br> [0x80001780]:csrrs a0, fcsr, zero<br> [0x80001784]:sw t6, 192(t1)<br>    |
| 180|[0x800099ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000179c]:feq.h t6, ft11, ft10<br> [0x800017a0]:csrrs a0, fcsr, zero<br> [0x800017a4]:sw t6, 200(t1)<br>    |
| 181|[0x800099b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800017bc]:feq.h t6, ft11, ft10<br> [0x800017c0]:csrrs a0, fcsr, zero<br> [0x800017c4]:sw t6, 208(t1)<br>    |
| 182|[0x800099bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800017dc]:feq.h t6, ft11, ft10<br> [0x800017e0]:csrrs a0, fcsr, zero<br> [0x800017e4]:sw t6, 216(t1)<br>    |
| 183|[0x800099c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800017fc]:feq.h t6, ft11, ft10<br> [0x80001800]:csrrs a0, fcsr, zero<br> [0x80001804]:sw t6, 224(t1)<br>    |
| 184|[0x800099cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000181c]:feq.h t6, ft11, ft10<br> [0x80001820]:csrrs a0, fcsr, zero<br> [0x80001824]:sw t6, 232(t1)<br>    |
| 185|[0x800099d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000183c]:feq.h t6, ft11, ft10<br> [0x80001840]:csrrs a0, fcsr, zero<br> [0x80001844]:sw t6, 240(t1)<br>    |
| 186|[0x800099dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000185c]:feq.h t6, ft11, ft10<br> [0x80001860]:csrrs a0, fcsr, zero<br> [0x80001864]:sw t6, 248(t1)<br>    |
| 187|[0x800099e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000187c]:feq.h t6, ft11, ft10<br> [0x80001880]:csrrs a0, fcsr, zero<br> [0x80001884]:sw t6, 256(t1)<br>    |
| 188|[0x800099ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000189c]:feq.h t6, ft11, ft10<br> [0x800018a0]:csrrs a0, fcsr, zero<br> [0x800018a4]:sw t6, 264(t1)<br>    |
| 189|[0x800099f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800018bc]:feq.h t6, ft11, ft10<br> [0x800018c0]:csrrs a0, fcsr, zero<br> [0x800018c4]:sw t6, 272(t1)<br>    |
| 190|[0x800099fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800018dc]:feq.h t6, ft11, ft10<br> [0x800018e0]:csrrs a0, fcsr, zero<br> [0x800018e4]:sw t6, 280(t1)<br>    |
| 191|[0x80009a04]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800018fc]:feq.h t6, ft11, ft10<br> [0x80001900]:csrrs a0, fcsr, zero<br> [0x80001904]:sw t6, 288(t1)<br>    |
| 192|[0x80009a0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x00 and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000191c]:feq.h t6, ft11, ft10<br> [0x80001920]:csrrs a0, fcsr, zero<br> [0x80001924]:sw t6, 296(t1)<br>    |
| 193|[0x80009a14]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000193c]:feq.h t6, ft11, ft10<br> [0x80001940]:csrrs a0, fcsr, zero<br> [0x80001944]:sw t6, 304(t1)<br>    |
| 194|[0x80009a1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000195c]:feq.h t6, ft11, ft10<br> [0x80001960]:csrrs a0, fcsr, zero<br> [0x80001964]:sw t6, 312(t1)<br>    |
| 195|[0x80009a24]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000197c]:feq.h t6, ft11, ft10<br> [0x80001980]:csrrs a0, fcsr, zero<br> [0x80001984]:sw t6, 320(t1)<br>    |
| 196|[0x80009a2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000199c]:feq.h t6, ft11, ft10<br> [0x800019a0]:csrrs a0, fcsr, zero<br> [0x800019a4]:sw t6, 328(t1)<br>    |
| 197|[0x80009a34]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800019bc]:feq.h t6, ft11, ft10<br> [0x800019c0]:csrrs a0, fcsr, zero<br> [0x800019c4]:sw t6, 336(t1)<br>    |
| 198|[0x80009a3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800019dc]:feq.h t6, ft11, ft10<br> [0x800019e0]:csrrs a0, fcsr, zero<br> [0x800019e4]:sw t6, 344(t1)<br>    |
| 199|[0x80009a44]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800019fc]:feq.h t6, ft11, ft10<br> [0x80001a00]:csrrs a0, fcsr, zero<br> [0x80001a04]:sw t6, 352(t1)<br>    |
| 200|[0x80009a4c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a1c]:feq.h t6, ft11, ft10<br> [0x80001a20]:csrrs a0, fcsr, zero<br> [0x80001a24]:sw t6, 360(t1)<br>    |
| 201|[0x80009a54]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a3c]:feq.h t6, ft11, ft10<br> [0x80001a40]:csrrs a0, fcsr, zero<br> [0x80001a44]:sw t6, 368(t1)<br>    |
| 202|[0x80009a5c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a5c]:feq.h t6, ft11, ft10<br> [0x80001a60]:csrrs a0, fcsr, zero<br> [0x80001a64]:sw t6, 376(t1)<br>    |
| 203|[0x80009a64]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a7c]:feq.h t6, ft11, ft10<br> [0x80001a80]:csrrs a0, fcsr, zero<br> [0x80001a84]:sw t6, 384(t1)<br>    |
| 204|[0x80009a6c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001a9c]:feq.h t6, ft11, ft10<br> [0x80001aa0]:csrrs a0, fcsr, zero<br> [0x80001aa4]:sw t6, 392(t1)<br>    |
| 205|[0x80009a74]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001abc]:feq.h t6, ft11, ft10<br> [0x80001ac0]:csrrs a0, fcsr, zero<br> [0x80001ac4]:sw t6, 400(t1)<br>    |
| 206|[0x80009a7c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001adc]:feq.h t6, ft11, ft10<br> [0x80001ae0]:csrrs a0, fcsr, zero<br> [0x80001ae4]:sw t6, 408(t1)<br>    |
| 207|[0x80009a84]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001afc]:feq.h t6, ft11, ft10<br> [0x80001b00]:csrrs a0, fcsr, zero<br> [0x80001b04]:sw t6, 416(t1)<br>    |
| 208|[0x80009a8c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b1c]:feq.h t6, ft11, ft10<br> [0x80001b20]:csrrs a0, fcsr, zero<br> [0x80001b24]:sw t6, 424(t1)<br>    |
| 209|[0x80009a94]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b3c]:feq.h t6, ft11, ft10<br> [0x80001b40]:csrrs a0, fcsr, zero<br> [0x80001b44]:sw t6, 432(t1)<br>    |
| 210|[0x80009a9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b5c]:feq.h t6, ft11, ft10<br> [0x80001b60]:csrrs a0, fcsr, zero<br> [0x80001b64]:sw t6, 440(t1)<br>    |
| 211|[0x80009aa4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b7c]:feq.h t6, ft11, ft10<br> [0x80001b80]:csrrs a0, fcsr, zero<br> [0x80001b84]:sw t6, 448(t1)<br>    |
| 212|[0x80009aac]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001b9c]:feq.h t6, ft11, ft10<br> [0x80001ba0]:csrrs a0, fcsr, zero<br> [0x80001ba4]:sw t6, 456(t1)<br>    |
| 213|[0x80009ab4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001bbc]:feq.h t6, ft11, ft10<br> [0x80001bc0]:csrrs a0, fcsr, zero<br> [0x80001bc4]:sw t6, 464(t1)<br>    |
| 214|[0x80009abc]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001bdc]:feq.h t6, ft11, ft10<br> [0x80001be0]:csrrs a0, fcsr, zero<br> [0x80001be4]:sw t6, 472(t1)<br>    |
| 215|[0x80009ac4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001bfc]:feq.h t6, ft11, ft10<br> [0x80001c00]:csrrs a0, fcsr, zero<br> [0x80001c04]:sw t6, 480(t1)<br>    |
| 216|[0x80009acc]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c1c]:feq.h t6, ft11, ft10<br> [0x80001c20]:csrrs a0, fcsr, zero<br> [0x80001c24]:sw t6, 488(t1)<br>    |
| 217|[0x80009ad4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c3c]:feq.h t6, ft11, ft10<br> [0x80001c40]:csrrs a0, fcsr, zero<br> [0x80001c44]:sw t6, 496(t1)<br>    |
| 218|[0x80009adc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c5c]:feq.h t6, ft11, ft10<br> [0x80001c60]:csrrs a0, fcsr, zero<br> [0x80001c64]:sw t6, 504(t1)<br>    |
| 219|[0x80009ae4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c7c]:feq.h t6, ft11, ft10<br> [0x80001c80]:csrrs a0, fcsr, zero<br> [0x80001c84]:sw t6, 512(t1)<br>    |
| 220|[0x80009aec]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001c9c]:feq.h t6, ft11, ft10<br> [0x80001ca0]:csrrs a0, fcsr, zero<br> [0x80001ca4]:sw t6, 520(t1)<br>    |
| 221|[0x80009af4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001cbc]:feq.h t6, ft11, ft10<br> [0x80001cc0]:csrrs a0, fcsr, zero<br> [0x80001cc4]:sw t6, 528(t1)<br>    |
| 222|[0x80009afc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001cdc]:feq.h t6, ft11, ft10<br> [0x80001ce0]:csrrs a0, fcsr, zero<br> [0x80001ce4]:sw t6, 536(t1)<br>    |
| 223|[0x80009b04]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001cfc]:feq.h t6, ft11, ft10<br> [0x80001d00]:csrrs a0, fcsr, zero<br> [0x80001d04]:sw t6, 544(t1)<br>    |
| 224|[0x80009b0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d1c]:feq.h t6, ft11, ft10<br> [0x80001d20]:csrrs a0, fcsr, zero<br> [0x80001d24]:sw t6, 552(t1)<br>    |
| 225|[0x80009b14]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d3c]:feq.h t6, ft11, ft10<br> [0x80001d40]:csrrs a0, fcsr, zero<br> [0x80001d44]:sw t6, 560(t1)<br>    |
| 226|[0x80009b1c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d5c]:feq.h t6, ft11, ft10<br> [0x80001d60]:csrrs a0, fcsr, zero<br> [0x80001d64]:sw t6, 568(t1)<br>    |
| 227|[0x80009b24]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d7c]:feq.h t6, ft11, ft10<br> [0x80001d80]:csrrs a0, fcsr, zero<br> [0x80001d84]:sw t6, 576(t1)<br>    |
| 228|[0x80009b2c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001d9c]:feq.h t6, ft11, ft10<br> [0x80001da0]:csrrs a0, fcsr, zero<br> [0x80001da4]:sw t6, 584(t1)<br>    |
| 229|[0x80009b34]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001dbc]:feq.h t6, ft11, ft10<br> [0x80001dc0]:csrrs a0, fcsr, zero<br> [0x80001dc4]:sw t6, 592(t1)<br>    |
| 230|[0x80009b3c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001ddc]:feq.h t6, ft11, ft10<br> [0x80001de0]:csrrs a0, fcsr, zero<br> [0x80001de4]:sw t6, 600(t1)<br>    |
| 231|[0x80009b44]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001dfc]:feq.h t6, ft11, ft10<br> [0x80001e00]:csrrs a0, fcsr, zero<br> [0x80001e04]:sw t6, 608(t1)<br>    |
| 232|[0x80009b4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e1c]:feq.h t6, ft11, ft10<br> [0x80001e20]:csrrs a0, fcsr, zero<br> [0x80001e24]:sw t6, 616(t1)<br>    |
| 233|[0x80009b54]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e3c]:feq.h t6, ft11, ft10<br> [0x80001e40]:csrrs a0, fcsr, zero<br> [0x80001e44]:sw t6, 624(t1)<br>    |
| 234|[0x80009b5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e5c]:feq.h t6, ft11, ft10<br> [0x80001e60]:csrrs a0, fcsr, zero<br> [0x80001e64]:sw t6, 632(t1)<br>    |
| 235|[0x80009b64]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e7c]:feq.h t6, ft11, ft10<br> [0x80001e80]:csrrs a0, fcsr, zero<br> [0x80001e84]:sw t6, 640(t1)<br>    |
| 236|[0x80009b6c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001e9c]:feq.h t6, ft11, ft10<br> [0x80001ea0]:csrrs a0, fcsr, zero<br> [0x80001ea4]:sw t6, 648(t1)<br>    |
| 237|[0x80009b74]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001ebc]:feq.h t6, ft11, ft10<br> [0x80001ec0]:csrrs a0, fcsr, zero<br> [0x80001ec4]:sw t6, 656(t1)<br>    |
| 238|[0x80009b7c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001edc]:feq.h t6, ft11, ft10<br> [0x80001ee0]:csrrs a0, fcsr, zero<br> [0x80001ee4]:sw t6, 664(t1)<br>    |
| 239|[0x80009b84]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001efc]:feq.h t6, ft11, ft10<br> [0x80001f00]:csrrs a0, fcsr, zero<br> [0x80001f04]:sw t6, 672(t1)<br>    |
| 240|[0x80009b8c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f1c]:feq.h t6, ft11, ft10<br> [0x80001f20]:csrrs a0, fcsr, zero<br> [0x80001f24]:sw t6, 680(t1)<br>    |
| 241|[0x80009b94]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f3c]:feq.h t6, ft11, ft10<br> [0x80001f40]:csrrs a0, fcsr, zero<br> [0x80001f44]:sw t6, 688(t1)<br>    |
| 242|[0x80009b9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f5c]:feq.h t6, ft11, ft10<br> [0x80001f60]:csrrs a0, fcsr, zero<br> [0x80001f64]:sw t6, 696(t1)<br>    |
| 243|[0x80009ba4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f7c]:feq.h t6, ft11, ft10<br> [0x80001f80]:csrrs a0, fcsr, zero<br> [0x80001f84]:sw t6, 704(t1)<br>    |
| 244|[0x80009bac]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001f9c]:feq.h t6, ft11, ft10<br> [0x80001fa0]:csrrs a0, fcsr, zero<br> [0x80001fa4]:sw t6, 712(t1)<br>    |
| 245|[0x80009bb4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001fbc]:feq.h t6, ft11, ft10<br> [0x80001fc0]:csrrs a0, fcsr, zero<br> [0x80001fc4]:sw t6, 720(t1)<br>    |
| 246|[0x80009bbc]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001fdc]:feq.h t6, ft11, ft10<br> [0x80001fe0]:csrrs a0, fcsr, zero<br> [0x80001fe4]:sw t6, 728(t1)<br>    |
| 247|[0x80009bc4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80001ffc]:feq.h t6, ft11, ft10<br> [0x80002000]:csrrs a0, fcsr, zero<br> [0x80002004]:sw t6, 736(t1)<br>    |
| 248|[0x80009bcc]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000201c]:feq.h t6, ft11, ft10<br> [0x80002020]:csrrs a0, fcsr, zero<br> [0x80002024]:sw t6, 744(t1)<br>    |
| 249|[0x80009bd4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000203c]:feq.h t6, ft11, ft10<br> [0x80002040]:csrrs a0, fcsr, zero<br> [0x80002044]:sw t6, 752(t1)<br>    |
| 250|[0x80009bdc]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000205c]:feq.h t6, ft11, ft10<br> [0x80002060]:csrrs a0, fcsr, zero<br> [0x80002064]:sw t6, 760(t1)<br>    |
| 251|[0x80009be4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000207c]:feq.h t6, ft11, ft10<br> [0x80002080]:csrrs a0, fcsr, zero<br> [0x80002084]:sw t6, 768(t1)<br>    |
| 252|[0x80009bec]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000209c]:feq.h t6, ft11, ft10<br> [0x800020a0]:csrrs a0, fcsr, zero<br> [0x800020a4]:sw t6, 776(t1)<br>    |
| 253|[0x80009bf4]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800020bc]:feq.h t6, ft11, ft10<br> [0x800020c0]:csrrs a0, fcsr, zero<br> [0x800020c4]:sw t6, 784(t1)<br>    |
| 254|[0x80009bfc]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800020dc]:feq.h t6, ft11, ft10<br> [0x800020e0]:csrrs a0, fcsr, zero<br> [0x800020e4]:sw t6, 792(t1)<br>    |
| 255|[0x80009c04]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800020fc]:feq.h t6, ft11, ft10<br> [0x80002100]:csrrs a0, fcsr, zero<br> [0x80002104]:sw t6, 800(t1)<br>    |
| 256|[0x80009c0c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000211c]:feq.h t6, ft11, ft10<br> [0x80002120]:csrrs a0, fcsr, zero<br> [0x80002124]:sw t6, 808(t1)<br>    |
| 257|[0x80009c14]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000213c]:feq.h t6, ft11, ft10<br> [0x80002140]:csrrs a0, fcsr, zero<br> [0x80002144]:sw t6, 816(t1)<br>    |
| 258|[0x80009c1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000215c]:feq.h t6, ft11, ft10<br> [0x80002160]:csrrs a0, fcsr, zero<br> [0x80002164]:sw t6, 824(t1)<br>    |
| 259|[0x80009c24]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000217c]:feq.h t6, ft11, ft10<br> [0x80002180]:csrrs a0, fcsr, zero<br> [0x80002184]:sw t6, 832(t1)<br>    |
| 260|[0x80009c2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000219c]:feq.h t6, ft11, ft10<br> [0x800021a0]:csrrs a0, fcsr, zero<br> [0x800021a4]:sw t6, 840(t1)<br>    |
| 261|[0x80009c34]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800021bc]:feq.h t6, ft11, ft10<br> [0x800021c0]:csrrs a0, fcsr, zero<br> [0x800021c4]:sw t6, 848(t1)<br>    |
| 262|[0x80009c3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800021dc]:feq.h t6, ft11, ft10<br> [0x800021e0]:csrrs a0, fcsr, zero<br> [0x800021e4]:sw t6, 856(t1)<br>    |
| 263|[0x80009c44]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800021fc]:feq.h t6, ft11, ft10<br> [0x80002200]:csrrs a0, fcsr, zero<br> [0x80002204]:sw t6, 864(t1)<br>    |
| 264|[0x80009c4c]<br>0x00000000|- fs1 == 0 and fe1 == 0x01 and fm1 == 0x001 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000221c]:feq.h t6, ft11, ft10<br> [0x80002220]:csrrs a0, fcsr, zero<br> [0x80002224]:sw t6, 872(t1)<br>    |
| 265|[0x80009c54]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000223c]:feq.h t6, ft11, ft10<br> [0x80002240]:csrrs a0, fcsr, zero<br> [0x80002244]:sw t6, 880(t1)<br>    |
| 266|[0x80009c5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000225c]:feq.h t6, ft11, ft10<br> [0x80002260]:csrrs a0, fcsr, zero<br> [0x80002264]:sw t6, 888(t1)<br>    |
| 267|[0x80009c64]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000227c]:feq.h t6, ft11, ft10<br> [0x80002280]:csrrs a0, fcsr, zero<br> [0x80002284]:sw t6, 896(t1)<br>    |
| 268|[0x80009c6c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000229c]:feq.h t6, ft11, ft10<br> [0x800022a0]:csrrs a0, fcsr, zero<br> [0x800022a4]:sw t6, 904(t1)<br>    |
| 269|[0x80009c74]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800022bc]:feq.h t6, ft11, ft10<br> [0x800022c0]:csrrs a0, fcsr, zero<br> [0x800022c4]:sw t6, 912(t1)<br>    |
| 270|[0x80009c7c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800022dc]:feq.h t6, ft11, ft10<br> [0x800022e0]:csrrs a0, fcsr, zero<br> [0x800022e4]:sw t6, 920(t1)<br>    |
| 271|[0x80009c84]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800022fc]:feq.h t6, ft11, ft10<br> [0x80002300]:csrrs a0, fcsr, zero<br> [0x80002304]:sw t6, 928(t1)<br>    |
| 272|[0x80009c8c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000231c]:feq.h t6, ft11, ft10<br> [0x80002320]:csrrs a0, fcsr, zero<br> [0x80002324]:sw t6, 936(t1)<br>    |
| 273|[0x80009c94]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000233c]:feq.h t6, ft11, ft10<br> [0x80002340]:csrrs a0, fcsr, zero<br> [0x80002344]:sw t6, 944(t1)<br>    |
| 274|[0x80009c9c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000235c]:feq.h t6, ft11, ft10<br> [0x80002360]:csrrs a0, fcsr, zero<br> [0x80002364]:sw t6, 952(t1)<br>    |
| 275|[0x80009ca4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000237c]:feq.h t6, ft11, ft10<br> [0x80002380]:csrrs a0, fcsr, zero<br> [0x80002384]:sw t6, 960(t1)<br>    |
| 276|[0x80009cac]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000239c]:feq.h t6, ft11, ft10<br> [0x800023a0]:csrrs a0, fcsr, zero<br> [0x800023a4]:sw t6, 968(t1)<br>    |
| 277|[0x80009cb4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800023bc]:feq.h t6, ft11, ft10<br> [0x800023c0]:csrrs a0, fcsr, zero<br> [0x800023c4]:sw t6, 976(t1)<br>    |
| 278|[0x80009cbc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800023dc]:feq.h t6, ft11, ft10<br> [0x800023e0]:csrrs a0, fcsr, zero<br> [0x800023e4]:sw t6, 984(t1)<br>    |
| 279|[0x80009cc4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800023fc]:feq.h t6, ft11, ft10<br> [0x80002400]:csrrs a0, fcsr, zero<br> [0x80002404]:sw t6, 992(t1)<br>    |
| 280|[0x80009ccc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000243c]:feq.h t6, ft11, ft10<br> [0x80002440]:csrrs a0, fcsr, zero<br> [0x80002444]:sw t6, 1000(t1)<br>   |
| 281|[0x80009cd4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000247c]:feq.h t6, ft11, ft10<br> [0x80002480]:csrrs a0, fcsr, zero<br> [0x80002484]:sw t6, 1008(t1)<br>   |
| 282|[0x80009cdc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800024bc]:feq.h t6, ft11, ft10<br> [0x800024c0]:csrrs a0, fcsr, zero<br> [0x800024c4]:sw t6, 1016(t1)<br>   |
| 283|[0x80009ce4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002504]:feq.h t6, ft11, ft10<br> [0x80002508]:csrrs a0, fcsr, zero<br> [0x8000250c]:sw t6, 0(t1)<br>      |
| 284|[0x80009cec]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002544]:feq.h t6, ft11, ft10<br> [0x80002548]:csrrs a0, fcsr, zero<br> [0x8000254c]:sw t6, 8(t1)<br>      |
| 285|[0x80009cf4]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002584]:feq.h t6, ft11, ft10<br> [0x80002588]:csrrs a0, fcsr, zero<br> [0x8000258c]:sw t6, 16(t1)<br>     |
| 286|[0x80009cfc]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800025c4]:feq.h t6, ft11, ft10<br> [0x800025c8]:csrrs a0, fcsr, zero<br> [0x800025cc]:sw t6, 24(t1)<br>     |
| 287|[0x80009d04]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002604]:feq.h t6, ft11, ft10<br> [0x80002608]:csrrs a0, fcsr, zero<br> [0x8000260c]:sw t6, 32(t1)<br>     |
| 288|[0x80009d0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x01 and fm1 == 0x055 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002644]:feq.h t6, ft11, ft10<br> [0x80002648]:csrrs a0, fcsr, zero<br> [0x8000264c]:sw t6, 40(t1)<br>     |
| 289|[0x80009d14]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002684]:feq.h t6, ft11, ft10<br> [0x80002688]:csrrs a0, fcsr, zero<br> [0x8000268c]:sw t6, 48(t1)<br>     |
| 290|[0x80009d1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800026c4]:feq.h t6, ft11, ft10<br> [0x800026c8]:csrrs a0, fcsr, zero<br> [0x800026cc]:sw t6, 56(t1)<br>     |
| 291|[0x80009d24]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002704]:feq.h t6, ft11, ft10<br> [0x80002708]:csrrs a0, fcsr, zero<br> [0x8000270c]:sw t6, 64(t1)<br>     |
| 292|[0x80009d2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002744]:feq.h t6, ft11, ft10<br> [0x80002748]:csrrs a0, fcsr, zero<br> [0x8000274c]:sw t6, 72(t1)<br>     |
| 293|[0x80009d34]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002784]:feq.h t6, ft11, ft10<br> [0x80002788]:csrrs a0, fcsr, zero<br> [0x8000278c]:sw t6, 80(t1)<br>     |
| 294|[0x80009d3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800027c4]:feq.h t6, ft11, ft10<br> [0x800027c8]:csrrs a0, fcsr, zero<br> [0x800027cc]:sw t6, 88(t1)<br>     |
| 295|[0x80009d44]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002804]:feq.h t6, ft11, ft10<br> [0x80002808]:csrrs a0, fcsr, zero<br> [0x8000280c]:sw t6, 96(t1)<br>     |
| 296|[0x80009d4c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002844]:feq.h t6, ft11, ft10<br> [0x80002848]:csrrs a0, fcsr, zero<br> [0x8000284c]:sw t6, 104(t1)<br>    |
| 297|[0x80009d54]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002884]:feq.h t6, ft11, ft10<br> [0x80002888]:csrrs a0, fcsr, zero<br> [0x8000288c]:sw t6, 112(t1)<br>    |
| 298|[0x80009d5c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800028c4]:feq.h t6, ft11, ft10<br> [0x800028c8]:csrrs a0, fcsr, zero<br> [0x800028cc]:sw t6, 120(t1)<br>    |
| 299|[0x80009d64]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002904]:feq.h t6, ft11, ft10<br> [0x80002908]:csrrs a0, fcsr, zero<br> [0x8000290c]:sw t6, 128(t1)<br>    |
| 300|[0x80009d6c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002944]:feq.h t6, ft11, ft10<br> [0x80002948]:csrrs a0, fcsr, zero<br> [0x8000294c]:sw t6, 136(t1)<br>    |
| 301|[0x80009d74]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002984]:feq.h t6, ft11, ft10<br> [0x80002988]:csrrs a0, fcsr, zero<br> [0x8000298c]:sw t6, 144(t1)<br>    |
| 302|[0x80009d7c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800029c4]:feq.h t6, ft11, ft10<br> [0x800029c8]:csrrs a0, fcsr, zero<br> [0x800029cc]:sw t6, 152(t1)<br>    |
| 303|[0x80009d84]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002a04]:feq.h t6, ft11, ft10<br> [0x80002a08]:csrrs a0, fcsr, zero<br> [0x80002a0c]:sw t6, 160(t1)<br>    |
| 304|[0x80009d8c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002a44]:feq.h t6, ft11, ft10<br> [0x80002a48]:csrrs a0, fcsr, zero<br> [0x80002a4c]:sw t6, 168(t1)<br>    |
| 305|[0x80009d94]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002a84]:feq.h t6, ft11, ft10<br> [0x80002a88]:csrrs a0, fcsr, zero<br> [0x80002a8c]:sw t6, 176(t1)<br>    |
| 306|[0x80009d9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002ac4]:feq.h t6, ft11, ft10<br> [0x80002ac8]:csrrs a0, fcsr, zero<br> [0x80002acc]:sw t6, 184(t1)<br>    |
| 307|[0x80009da4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002b04]:feq.h t6, ft11, ft10<br> [0x80002b08]:csrrs a0, fcsr, zero<br> [0x80002b0c]:sw t6, 192(t1)<br>    |
| 308|[0x80009dac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002b44]:feq.h t6, ft11, ft10<br> [0x80002b48]:csrrs a0, fcsr, zero<br> [0x80002b4c]:sw t6, 200(t1)<br>    |
| 309|[0x80009db4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002b84]:feq.h t6, ft11, ft10<br> [0x80002b88]:csrrs a0, fcsr, zero<br> [0x80002b8c]:sw t6, 208(t1)<br>    |
| 310|[0x80009dbc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002bc4]:feq.h t6, ft11, ft10<br> [0x80002bc8]:csrrs a0, fcsr, zero<br> [0x80002bcc]:sw t6, 216(t1)<br>    |
| 311|[0x80009dc4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002c04]:feq.h t6, ft11, ft10<br> [0x80002c08]:csrrs a0, fcsr, zero<br> [0x80002c0c]:sw t6, 224(t1)<br>    |
| 312|[0x80009dcc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002c44]:feq.h t6, ft11, ft10<br> [0x80002c48]:csrrs a0, fcsr, zero<br> [0x80002c4c]:sw t6, 232(t1)<br>    |
| 313|[0x80009dd4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002c84]:feq.h t6, ft11, ft10<br> [0x80002c88]:csrrs a0, fcsr, zero<br> [0x80002c8c]:sw t6, 240(t1)<br>    |
| 314|[0x80009ddc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002cc4]:feq.h t6, ft11, ft10<br> [0x80002cc8]:csrrs a0, fcsr, zero<br> [0x80002ccc]:sw t6, 248(t1)<br>    |
| 315|[0x80009de4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002d04]:feq.h t6, ft11, ft10<br> [0x80002d08]:csrrs a0, fcsr, zero<br> [0x80002d0c]:sw t6, 256(t1)<br>    |
| 316|[0x80009dec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002d44]:feq.h t6, ft11, ft10<br> [0x80002d48]:csrrs a0, fcsr, zero<br> [0x80002d4c]:sw t6, 264(t1)<br>    |
| 317|[0x80009df4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002d84]:feq.h t6, ft11, ft10<br> [0x80002d88]:csrrs a0, fcsr, zero<br> [0x80002d8c]:sw t6, 272(t1)<br>    |
| 318|[0x80009dfc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002dc4]:feq.h t6, ft11, ft10<br> [0x80002dc8]:csrrs a0, fcsr, zero<br> [0x80002dcc]:sw t6, 280(t1)<br>    |
| 319|[0x80009e04]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002e04]:feq.h t6, ft11, ft10<br> [0x80002e08]:csrrs a0, fcsr, zero<br> [0x80002e0c]:sw t6, 288(t1)<br>    |
| 320|[0x80009e0c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002e44]:feq.h t6, ft11, ft10<br> [0x80002e48]:csrrs a0, fcsr, zero<br> [0x80002e4c]:sw t6, 296(t1)<br>    |
| 321|[0x80009e14]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002e84]:feq.h t6, ft11, ft10<br> [0x80002e88]:csrrs a0, fcsr, zero<br> [0x80002e8c]:sw t6, 304(t1)<br>    |
| 322|[0x80009e1c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002ec4]:feq.h t6, ft11, ft10<br> [0x80002ec8]:csrrs a0, fcsr, zero<br> [0x80002ecc]:sw t6, 312(t1)<br>    |
| 323|[0x80009e24]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002f04]:feq.h t6, ft11, ft10<br> [0x80002f08]:csrrs a0, fcsr, zero<br> [0x80002f0c]:sw t6, 320(t1)<br>    |
| 324|[0x80009e2c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002f44]:feq.h t6, ft11, ft10<br> [0x80002f48]:csrrs a0, fcsr, zero<br> [0x80002f4c]:sw t6, 328(t1)<br>    |
| 325|[0x80009e34]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002f84]:feq.h t6, ft11, ft10<br> [0x80002f88]:csrrs a0, fcsr, zero<br> [0x80002f8c]:sw t6, 336(t1)<br>    |
| 326|[0x80009e3c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80002fc4]:feq.h t6, ft11, ft10<br> [0x80002fc8]:csrrs a0, fcsr, zero<br> [0x80002fcc]:sw t6, 344(t1)<br>    |
| 327|[0x80009e44]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003004]:feq.h t6, ft11, ft10<br> [0x80003008]:csrrs a0, fcsr, zero<br> [0x8000300c]:sw t6, 352(t1)<br>    |
| 328|[0x80009e4c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003044]:feq.h t6, ft11, ft10<br> [0x80003048]:csrrs a0, fcsr, zero<br> [0x8000304c]:sw t6, 360(t1)<br>    |
| 329|[0x80009e54]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003084]:feq.h t6, ft11, ft10<br> [0x80003088]:csrrs a0, fcsr, zero<br> [0x8000308c]:sw t6, 368(t1)<br>    |
| 330|[0x80009e5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800030c4]:feq.h t6, ft11, ft10<br> [0x800030c8]:csrrs a0, fcsr, zero<br> [0x800030cc]:sw t6, 376(t1)<br>    |
| 331|[0x80009e64]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003104]:feq.h t6, ft11, ft10<br> [0x80003108]:csrrs a0, fcsr, zero<br> [0x8000310c]:sw t6, 384(t1)<br>    |
| 332|[0x80009e6c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003144]:feq.h t6, ft11, ft10<br> [0x80003148]:csrrs a0, fcsr, zero<br> [0x8000314c]:sw t6, 392(t1)<br>    |
| 333|[0x80009e74]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003184]:feq.h t6, ft11, ft10<br> [0x80003188]:csrrs a0, fcsr, zero<br> [0x8000318c]:sw t6, 400(t1)<br>    |
| 334|[0x80009e7c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800031c4]:feq.h t6, ft11, ft10<br> [0x800031c8]:csrrs a0, fcsr, zero<br> [0x800031cc]:sw t6, 408(t1)<br>    |
| 335|[0x80009e84]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003204]:feq.h t6, ft11, ft10<br> [0x80003208]:csrrs a0, fcsr, zero<br> [0x8000320c]:sw t6, 416(t1)<br>    |
| 336|[0x80009e8c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1e and fm1 == 0x3ff and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003244]:feq.h t6, ft11, ft10<br> [0x80003248]:csrrs a0, fcsr, zero<br> [0x8000324c]:sw t6, 424(t1)<br>    |
| 337|[0x80009e94]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003284]:feq.h t6, ft11, ft10<br> [0x80003288]:csrrs a0, fcsr, zero<br> [0x8000328c]:sw t6, 432(t1)<br>    |
| 338|[0x80009e9c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800032c4]:feq.h t6, ft11, ft10<br> [0x800032c8]:csrrs a0, fcsr, zero<br> [0x800032cc]:sw t6, 440(t1)<br>    |
| 339|[0x80009ea4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003304]:feq.h t6, ft11, ft10<br> [0x80003308]:csrrs a0, fcsr, zero<br> [0x8000330c]:sw t6, 448(t1)<br>    |
| 340|[0x80009eac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003344]:feq.h t6, ft11, ft10<br> [0x80003348]:csrrs a0, fcsr, zero<br> [0x8000334c]:sw t6, 456(t1)<br>    |
| 341|[0x80009eb4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003384]:feq.h t6, ft11, ft10<br> [0x80003388]:csrrs a0, fcsr, zero<br> [0x8000338c]:sw t6, 464(t1)<br>    |
| 342|[0x80009ebc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800033c4]:feq.h t6, ft11, ft10<br> [0x800033c8]:csrrs a0, fcsr, zero<br> [0x800033cc]:sw t6, 472(t1)<br>    |
| 343|[0x80009ec4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003404]:feq.h t6, ft11, ft10<br> [0x80003408]:csrrs a0, fcsr, zero<br> [0x8000340c]:sw t6, 480(t1)<br>    |
| 344|[0x80009ecc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003444]:feq.h t6, ft11, ft10<br> [0x80003448]:csrrs a0, fcsr, zero<br> [0x8000344c]:sw t6, 488(t1)<br>    |
| 345|[0x80009ed4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003484]:feq.h t6, ft11, ft10<br> [0x80003488]:csrrs a0, fcsr, zero<br> [0x8000348c]:sw t6, 496(t1)<br>    |
| 346|[0x80009edc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800034c4]:feq.h t6, ft11, ft10<br> [0x800034c8]:csrrs a0, fcsr, zero<br> [0x800034cc]:sw t6, 504(t1)<br>    |
| 347|[0x80009ee4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003504]:feq.h t6, ft11, ft10<br> [0x80003508]:csrrs a0, fcsr, zero<br> [0x8000350c]:sw t6, 512(t1)<br>    |
| 348|[0x80009eec]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003544]:feq.h t6, ft11, ft10<br> [0x80003548]:csrrs a0, fcsr, zero<br> [0x8000354c]:sw t6, 520(t1)<br>    |
| 349|[0x80009ef4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003584]:feq.h t6, ft11, ft10<br> [0x80003588]:csrrs a0, fcsr, zero<br> [0x8000358c]:sw t6, 528(t1)<br>    |
| 350|[0x80009efc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800035c4]:feq.h t6, ft11, ft10<br> [0x800035c8]:csrrs a0, fcsr, zero<br> [0x800035cc]:sw t6, 536(t1)<br>    |
| 351|[0x80009f04]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003604]:feq.h t6, ft11, ft10<br> [0x80003608]:csrrs a0, fcsr, zero<br> [0x8000360c]:sw t6, 544(t1)<br>    |
| 352|[0x80009f0c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003644]:feq.h t6, ft11, ft10<br> [0x80003648]:csrrs a0, fcsr, zero<br> [0x8000364c]:sw t6, 552(t1)<br>    |
| 353|[0x80009f14]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003684]:feq.h t6, ft11, ft10<br> [0x80003688]:csrrs a0, fcsr, zero<br> [0x8000368c]:sw t6, 560(t1)<br>    |
| 354|[0x80009f1c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800036c4]:feq.h t6, ft11, ft10<br> [0x800036c8]:csrrs a0, fcsr, zero<br> [0x800036cc]:sw t6, 568(t1)<br>    |
| 355|[0x80009f24]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003704]:feq.h t6, ft11, ft10<br> [0x80003708]:csrrs a0, fcsr, zero<br> [0x8000370c]:sw t6, 576(t1)<br>    |
| 356|[0x80009f2c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003744]:feq.h t6, ft11, ft10<br> [0x80003748]:csrrs a0, fcsr, zero<br> [0x8000374c]:sw t6, 584(t1)<br>    |
| 357|[0x80009f34]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003784]:feq.h t6, ft11, ft10<br> [0x80003788]:csrrs a0, fcsr, zero<br> [0x8000378c]:sw t6, 592(t1)<br>    |
| 358|[0x80009f3c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800037c4]:feq.h t6, ft11, ft10<br> [0x800037c8]:csrrs a0, fcsr, zero<br> [0x800037cc]:sw t6, 600(t1)<br>    |
| 359|[0x80009f44]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003804]:feq.h t6, ft11, ft10<br> [0x80003808]:csrrs a0, fcsr, zero<br> [0x8000380c]:sw t6, 608(t1)<br>    |
| 360|[0x80009f4c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003844]:feq.h t6, ft11, ft10<br> [0x80003848]:csrrs a0, fcsr, zero<br> [0x8000384c]:sw t6, 616(t1)<br>    |
| 361|[0x80009f54]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003884]:feq.h t6, ft11, ft10<br> [0x80003888]:csrrs a0, fcsr, zero<br> [0x8000388c]:sw t6, 624(t1)<br>    |
| 362|[0x80009f5c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800038c4]:feq.h t6, ft11, ft10<br> [0x800038c8]:csrrs a0, fcsr, zero<br> [0x800038cc]:sw t6, 632(t1)<br>    |
| 363|[0x80009f64]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003904]:feq.h t6, ft11, ft10<br> [0x80003908]:csrrs a0, fcsr, zero<br> [0x8000390c]:sw t6, 640(t1)<br>    |
| 364|[0x80009f6c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003944]:feq.h t6, ft11, ft10<br> [0x80003948]:csrrs a0, fcsr, zero<br> [0x8000394c]:sw t6, 648(t1)<br>    |
| 365|[0x80009f74]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003984]:feq.h t6, ft11, ft10<br> [0x80003988]:csrrs a0, fcsr, zero<br> [0x8000398c]:sw t6, 656(t1)<br>    |
| 366|[0x80009f7c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800039c4]:feq.h t6, ft11, ft10<br> [0x800039c8]:csrrs a0, fcsr, zero<br> [0x800039cc]:sw t6, 664(t1)<br>    |
| 367|[0x80009f84]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003a04]:feq.h t6, ft11, ft10<br> [0x80003a08]:csrrs a0, fcsr, zero<br> [0x80003a0c]:sw t6, 672(t1)<br>    |
| 368|[0x80009f8c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003a44]:feq.h t6, ft11, ft10<br> [0x80003a48]:csrrs a0, fcsr, zero<br> [0x80003a4c]:sw t6, 680(t1)<br>    |
| 369|[0x80009f94]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003a84]:feq.h t6, ft11, ft10<br> [0x80003a88]:csrrs a0, fcsr, zero<br> [0x80003a8c]:sw t6, 688(t1)<br>    |
| 370|[0x80009f9c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003ac4]:feq.h t6, ft11, ft10<br> [0x80003ac8]:csrrs a0, fcsr, zero<br> [0x80003acc]:sw t6, 696(t1)<br>    |
| 371|[0x80009fa4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003b04]:feq.h t6, ft11, ft10<br> [0x80003b08]:csrrs a0, fcsr, zero<br> [0x80003b0c]:sw t6, 704(t1)<br>    |
| 372|[0x80009fac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003b44]:feq.h t6, ft11, ft10<br> [0x80003b48]:csrrs a0, fcsr, zero<br> [0x80003b4c]:sw t6, 712(t1)<br>    |
| 373|[0x80009fb4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003b84]:feq.h t6, ft11, ft10<br> [0x80003b88]:csrrs a0, fcsr, zero<br> [0x80003b8c]:sw t6, 720(t1)<br>    |
| 374|[0x80009fbc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003bc4]:feq.h t6, ft11, ft10<br> [0x80003bc8]:csrrs a0, fcsr, zero<br> [0x80003bcc]:sw t6, 728(t1)<br>    |
| 375|[0x80009fc4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003c04]:feq.h t6, ft11, ft10<br> [0x80003c08]:csrrs a0, fcsr, zero<br> [0x80003c0c]:sw t6, 736(t1)<br>    |
| 376|[0x80009fcc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003c44]:feq.h t6, ft11, ft10<br> [0x80003c48]:csrrs a0, fcsr, zero<br> [0x80003c4c]:sw t6, 744(t1)<br>    |
| 377|[0x80009fd4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003c84]:feq.h t6, ft11, ft10<br> [0x80003c88]:csrrs a0, fcsr, zero<br> [0x80003c8c]:sw t6, 752(t1)<br>    |
| 378|[0x80009fdc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003cc4]:feq.h t6, ft11, ft10<br> [0x80003cc8]:csrrs a0, fcsr, zero<br> [0x80003ccc]:sw t6, 760(t1)<br>    |
| 379|[0x80009fe4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003d04]:feq.h t6, ft11, ft10<br> [0x80003d08]:csrrs a0, fcsr, zero<br> [0x80003d0c]:sw t6, 768(t1)<br>    |
| 380|[0x80009fec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003d44]:feq.h t6, ft11, ft10<br> [0x80003d48]:csrrs a0, fcsr, zero<br> [0x80003d4c]:sw t6, 776(t1)<br>    |
| 381|[0x80009ff4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003d84]:feq.h t6, ft11, ft10<br> [0x80003d88]:csrrs a0, fcsr, zero<br> [0x80003d8c]:sw t6, 784(t1)<br>    |
| 382|[0x80009ffc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003dc4]:feq.h t6, ft11, ft10<br> [0x80003dc8]:csrrs a0, fcsr, zero<br> [0x80003dcc]:sw t6, 792(t1)<br>    |
| 383|[0x8000a004]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003e04]:feq.h t6, ft11, ft10<br> [0x80003e08]:csrrs a0, fcsr, zero<br> [0x80003e0c]:sw t6, 800(t1)<br>    |
| 384|[0x8000a00c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003e44]:feq.h t6, ft11, ft10<br> [0x80003e48]:csrrs a0, fcsr, zero<br> [0x80003e4c]:sw t6, 808(t1)<br>    |
| 385|[0x8000a014]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003e84]:feq.h t6, ft11, ft10<br> [0x80003e88]:csrrs a0, fcsr, zero<br> [0x80003e8c]:sw t6, 816(t1)<br>    |
| 386|[0x8000a01c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003ec4]:feq.h t6, ft11, ft10<br> [0x80003ec8]:csrrs a0, fcsr, zero<br> [0x80003ecc]:sw t6, 824(t1)<br>    |
| 387|[0x8000a024]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003f04]:feq.h t6, ft11, ft10<br> [0x80003f08]:csrrs a0, fcsr, zero<br> [0x80003f0c]:sw t6, 832(t1)<br>    |
| 388|[0x8000a02c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003f44]:feq.h t6, ft11, ft10<br> [0x80003f48]:csrrs a0, fcsr, zero<br> [0x80003f4c]:sw t6, 840(t1)<br>    |
| 389|[0x8000a034]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003f84]:feq.h t6, ft11, ft10<br> [0x80003f88]:csrrs a0, fcsr, zero<br> [0x80003f8c]:sw t6, 848(t1)<br>    |
| 390|[0x8000a03c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80003fc4]:feq.h t6, ft11, ft10<br> [0x80003fc8]:csrrs a0, fcsr, zero<br> [0x80003fcc]:sw t6, 856(t1)<br>    |
| 391|[0x8000a044]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004004]:feq.h t6, ft11, ft10<br> [0x80004008]:csrrs a0, fcsr, zero<br> [0x8000400c]:sw t6, 864(t1)<br>    |
| 392|[0x8000a04c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004044]:feq.h t6, ft11, ft10<br> [0x80004048]:csrrs a0, fcsr, zero<br> [0x8000404c]:sw t6, 872(t1)<br>    |
| 393|[0x8000a054]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004084]:feq.h t6, ft11, ft10<br> [0x80004088]:csrrs a0, fcsr, zero<br> [0x8000408c]:sw t6, 880(t1)<br>    |
| 394|[0x8000a05c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800040c4]:feq.h t6, ft11, ft10<br> [0x800040c8]:csrrs a0, fcsr, zero<br> [0x800040cc]:sw t6, 888(t1)<br>    |
| 395|[0x8000a064]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004104]:feq.h t6, ft11, ft10<br> [0x80004108]:csrrs a0, fcsr, zero<br> [0x8000410c]:sw t6, 896(t1)<br>    |
| 396|[0x8000a06c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004144]:feq.h t6, ft11, ft10<br> [0x80004148]:csrrs a0, fcsr, zero<br> [0x8000414c]:sw t6, 904(t1)<br>    |
| 397|[0x8000a074]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004184]:feq.h t6, ft11, ft10<br> [0x80004188]:csrrs a0, fcsr, zero<br> [0x8000418c]:sw t6, 912(t1)<br>    |
| 398|[0x8000a07c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800041c4]:feq.h t6, ft11, ft10<br> [0x800041c8]:csrrs a0, fcsr, zero<br> [0x800041cc]:sw t6, 920(t1)<br>    |
| 399|[0x8000a084]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004204]:feq.h t6, ft11, ft10<br> [0x80004208]:csrrs a0, fcsr, zero<br> [0x8000420c]:sw t6, 928(t1)<br>    |
| 400|[0x8000a08c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004244]:feq.h t6, ft11, ft10<br> [0x80004248]:csrrs a0, fcsr, zero<br> [0x8000424c]:sw t6, 936(t1)<br>    |
| 401|[0x8000a094]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004284]:feq.h t6, ft11, ft10<br> [0x80004288]:csrrs a0, fcsr, zero<br> [0x8000428c]:sw t6, 944(t1)<br>    |
| 402|[0x8000a09c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800042c4]:feq.h t6, ft11, ft10<br> [0x800042c8]:csrrs a0, fcsr, zero<br> [0x800042cc]:sw t6, 952(t1)<br>    |
| 403|[0x8000a0a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004304]:feq.h t6, ft11, ft10<br> [0x80004308]:csrrs a0, fcsr, zero<br> [0x8000430c]:sw t6, 960(t1)<br>    |
| 404|[0x8000a0ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004344]:feq.h t6, ft11, ft10<br> [0x80004348]:csrrs a0, fcsr, zero<br> [0x8000434c]:sw t6, 968(t1)<br>    |
| 405|[0x8000a0b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004384]:feq.h t6, ft11, ft10<br> [0x80004388]:csrrs a0, fcsr, zero<br> [0x8000438c]:sw t6, 976(t1)<br>    |
| 406|[0x8000a0bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800043c4]:feq.h t6, ft11, ft10<br> [0x800043c8]:csrrs a0, fcsr, zero<br> [0x800043cc]:sw t6, 984(t1)<br>    |
| 407|[0x8000a0c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004404]:feq.h t6, ft11, ft10<br> [0x80004408]:csrrs a0, fcsr, zero<br> [0x8000440c]:sw t6, 992(t1)<br>    |
| 408|[0x8000a0cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004444]:feq.h t6, ft11, ft10<br> [0x80004448]:csrrs a0, fcsr, zero<br> [0x8000444c]:sw t6, 1000(t1)<br>   |
| 409|[0x8000a0d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004484]:feq.h t6, ft11, ft10<br> [0x80004488]:csrrs a0, fcsr, zero<br> [0x8000448c]:sw t6, 1008(t1)<br>   |
| 410|[0x8000a0dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800044c4]:feq.h t6, ft11, ft10<br> [0x800044c8]:csrrs a0, fcsr, zero<br> [0x800044cc]:sw t6, 1016(t1)<br>   |
| 411|[0x8000a0e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000450c]:feq.h t6, ft11, ft10<br> [0x80004510]:csrrs a0, fcsr, zero<br> [0x80004514]:sw t6, 0(t1)<br>      |
| 412|[0x8000a0ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000454c]:feq.h t6, ft11, ft10<br> [0x80004550]:csrrs a0, fcsr, zero<br> [0x80004554]:sw t6, 8(t1)<br>      |
| 413|[0x8000a0f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000458c]:feq.h t6, ft11, ft10<br> [0x80004590]:csrrs a0, fcsr, zero<br> [0x80004594]:sw t6, 16(t1)<br>     |
| 414|[0x8000a0fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800045cc]:feq.h t6, ft11, ft10<br> [0x800045d0]:csrrs a0, fcsr, zero<br> [0x800045d4]:sw t6, 24(t1)<br>     |
| 415|[0x8000a104]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000460c]:feq.h t6, ft11, ft10<br> [0x80004610]:csrrs a0, fcsr, zero<br> [0x80004614]:sw t6, 32(t1)<br>     |
| 416|[0x8000a10c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000464c]:feq.h t6, ft11, ft10<br> [0x80004650]:csrrs a0, fcsr, zero<br> [0x80004654]:sw t6, 40(t1)<br>     |
| 417|[0x8000a114]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000468c]:feq.h t6, ft11, ft10<br> [0x80004690]:csrrs a0, fcsr, zero<br> [0x80004694]:sw t6, 48(t1)<br>     |
| 418|[0x8000a11c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800046cc]:feq.h t6, ft11, ft10<br> [0x800046d0]:csrrs a0, fcsr, zero<br> [0x800046d4]:sw t6, 56(t1)<br>     |
| 419|[0x8000a124]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000470c]:feq.h t6, ft11, ft10<br> [0x80004710]:csrrs a0, fcsr, zero<br> [0x80004714]:sw t6, 64(t1)<br>     |
| 420|[0x8000a12c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000474c]:feq.h t6, ft11, ft10<br> [0x80004750]:csrrs a0, fcsr, zero<br> [0x80004754]:sw t6, 72(t1)<br>     |
| 421|[0x8000a134]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000478c]:feq.h t6, ft11, ft10<br> [0x80004790]:csrrs a0, fcsr, zero<br> [0x80004794]:sw t6, 80(t1)<br>     |
| 422|[0x8000a13c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800047cc]:feq.h t6, ft11, ft10<br> [0x800047d0]:csrrs a0, fcsr, zero<br> [0x800047d4]:sw t6, 88(t1)<br>     |
| 423|[0x8000a144]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000480c]:feq.h t6, ft11, ft10<br> [0x80004810]:csrrs a0, fcsr, zero<br> [0x80004814]:sw t6, 96(t1)<br>     |
| 424|[0x8000a14c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000484c]:feq.h t6, ft11, ft10<br> [0x80004850]:csrrs a0, fcsr, zero<br> [0x80004854]:sw t6, 104(t1)<br>    |
| 425|[0x8000a154]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000488c]:feq.h t6, ft11, ft10<br> [0x80004890]:csrrs a0, fcsr, zero<br> [0x80004894]:sw t6, 112(t1)<br>    |
| 426|[0x8000a15c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800048cc]:feq.h t6, ft11, ft10<br> [0x800048d0]:csrrs a0, fcsr, zero<br> [0x800048d4]:sw t6, 120(t1)<br>    |
| 427|[0x8000a164]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000490c]:feq.h t6, ft11, ft10<br> [0x80004910]:csrrs a0, fcsr, zero<br> [0x80004914]:sw t6, 128(t1)<br>    |
| 428|[0x8000a16c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000494c]:feq.h t6, ft11, ft10<br> [0x80004950]:csrrs a0, fcsr, zero<br> [0x80004954]:sw t6, 136(t1)<br>    |
| 429|[0x8000a174]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000498c]:feq.h t6, ft11, ft10<br> [0x80004990]:csrrs a0, fcsr, zero<br> [0x80004994]:sw t6, 144(t1)<br>    |
| 430|[0x8000a17c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800049cc]:feq.h t6, ft11, ft10<br> [0x800049d0]:csrrs a0, fcsr, zero<br> [0x800049d4]:sw t6, 152(t1)<br>    |
| 431|[0x8000a184]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004a0c]:feq.h t6, ft11, ft10<br> [0x80004a10]:csrrs a0, fcsr, zero<br> [0x80004a14]:sw t6, 160(t1)<br>    |
| 432|[0x8000a18c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x200 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004a4c]:feq.h t6, ft11, ft10<br> [0x80004a50]:csrrs a0, fcsr, zero<br> [0x80004a54]:sw t6, 168(t1)<br>    |
| 433|[0x8000a194]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004a8c]:feq.h t6, ft11, ft10<br> [0x80004a90]:csrrs a0, fcsr, zero<br> [0x80004a94]:sw t6, 176(t1)<br>    |
| 434|[0x8000a19c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004acc]:feq.h t6, ft11, ft10<br> [0x80004ad0]:csrrs a0, fcsr, zero<br> [0x80004ad4]:sw t6, 184(t1)<br>    |
| 435|[0x8000a1a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004b0c]:feq.h t6, ft11, ft10<br> [0x80004b10]:csrrs a0, fcsr, zero<br> [0x80004b14]:sw t6, 192(t1)<br>    |
| 436|[0x8000a1ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004b4c]:feq.h t6, ft11, ft10<br> [0x80004b50]:csrrs a0, fcsr, zero<br> [0x80004b54]:sw t6, 200(t1)<br>    |
| 437|[0x8000a1b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004b8c]:feq.h t6, ft11, ft10<br> [0x80004b90]:csrrs a0, fcsr, zero<br> [0x80004b94]:sw t6, 208(t1)<br>    |
| 438|[0x8000a1bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004bcc]:feq.h t6, ft11, ft10<br> [0x80004bd0]:csrrs a0, fcsr, zero<br> [0x80004bd4]:sw t6, 216(t1)<br>    |
| 439|[0x8000a1c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004c0c]:feq.h t6, ft11, ft10<br> [0x80004c10]:csrrs a0, fcsr, zero<br> [0x80004c14]:sw t6, 224(t1)<br>    |
| 440|[0x8000a1cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004c4c]:feq.h t6, ft11, ft10<br> [0x80004c50]:csrrs a0, fcsr, zero<br> [0x80004c54]:sw t6, 232(t1)<br>    |
| 441|[0x8000a1d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004c8c]:feq.h t6, ft11, ft10<br> [0x80004c90]:csrrs a0, fcsr, zero<br> [0x80004c94]:sw t6, 240(t1)<br>    |
| 442|[0x8000a1dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004ccc]:feq.h t6, ft11, ft10<br> [0x80004cd0]:csrrs a0, fcsr, zero<br> [0x80004cd4]:sw t6, 248(t1)<br>    |
| 443|[0x8000a1e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004d0c]:feq.h t6, ft11, ft10<br> [0x80004d10]:csrrs a0, fcsr, zero<br> [0x80004d14]:sw t6, 256(t1)<br>    |
| 444|[0x8000a1ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004d4c]:feq.h t6, ft11, ft10<br> [0x80004d50]:csrrs a0, fcsr, zero<br> [0x80004d54]:sw t6, 264(t1)<br>    |
| 445|[0x8000a1f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004d8c]:feq.h t6, ft11, ft10<br> [0x80004d90]:csrrs a0, fcsr, zero<br> [0x80004d94]:sw t6, 272(t1)<br>    |
| 446|[0x8000a1fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004dcc]:feq.h t6, ft11, ft10<br> [0x80004dd0]:csrrs a0, fcsr, zero<br> [0x80004dd4]:sw t6, 280(t1)<br>    |
| 447|[0x8000a204]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004e0c]:feq.h t6, ft11, ft10<br> [0x80004e10]:csrrs a0, fcsr, zero<br> [0x80004e14]:sw t6, 288(t1)<br>    |
| 448|[0x8000a20c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004e4c]:feq.h t6, ft11, ft10<br> [0x80004e50]:csrrs a0, fcsr, zero<br> [0x80004e54]:sw t6, 296(t1)<br>    |
| 449|[0x8000a214]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004e8c]:feq.h t6, ft11, ft10<br> [0x80004e90]:csrrs a0, fcsr, zero<br> [0x80004e94]:sw t6, 304(t1)<br>    |
| 450|[0x8000a21c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004ecc]:feq.h t6, ft11, ft10<br> [0x80004ed0]:csrrs a0, fcsr, zero<br> [0x80004ed4]:sw t6, 312(t1)<br>    |
| 451|[0x8000a224]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004f0c]:feq.h t6, ft11, ft10<br> [0x80004f10]:csrrs a0, fcsr, zero<br> [0x80004f14]:sw t6, 320(t1)<br>    |
| 452|[0x8000a22c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004f4c]:feq.h t6, ft11, ft10<br> [0x80004f50]:csrrs a0, fcsr, zero<br> [0x80004f54]:sw t6, 328(t1)<br>    |
| 453|[0x8000a234]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004f8c]:feq.h t6, ft11, ft10<br> [0x80004f90]:csrrs a0, fcsr, zero<br> [0x80004f94]:sw t6, 336(t1)<br>    |
| 454|[0x8000a23c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80004fcc]:feq.h t6, ft11, ft10<br> [0x80004fd0]:csrrs a0, fcsr, zero<br> [0x80004fd4]:sw t6, 344(t1)<br>    |
| 455|[0x8000a244]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000500c]:feq.h t6, ft11, ft10<br> [0x80005010]:csrrs a0, fcsr, zero<br> [0x80005014]:sw t6, 352(t1)<br>    |
| 456|[0x8000a24c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x201 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000504c]:feq.h t6, ft11, ft10<br> [0x80005050]:csrrs a0, fcsr, zero<br> [0x80005054]:sw t6, 360(t1)<br>    |
| 457|[0x8000a254]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000508c]:feq.h t6, ft11, ft10<br> [0x80005090]:csrrs a0, fcsr, zero<br> [0x80005094]:sw t6, 368(t1)<br>    |
| 458|[0x8000a25c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800050cc]:feq.h t6, ft11, ft10<br> [0x800050d0]:csrrs a0, fcsr, zero<br> [0x800050d4]:sw t6, 376(t1)<br>    |
| 459|[0x8000a264]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000510c]:feq.h t6, ft11, ft10<br> [0x80005110]:csrrs a0, fcsr, zero<br> [0x80005114]:sw t6, 384(t1)<br>    |
| 460|[0x8000a26c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000514c]:feq.h t6, ft11, ft10<br> [0x80005150]:csrrs a0, fcsr, zero<br> [0x80005154]:sw t6, 392(t1)<br>    |
| 461|[0x8000a274]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000518c]:feq.h t6, ft11, ft10<br> [0x80005190]:csrrs a0, fcsr, zero<br> [0x80005194]:sw t6, 400(t1)<br>    |
| 462|[0x8000a27c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800051cc]:feq.h t6, ft11, ft10<br> [0x800051d0]:csrrs a0, fcsr, zero<br> [0x800051d4]:sw t6, 408(t1)<br>    |
| 463|[0x8000a284]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000520c]:feq.h t6, ft11, ft10<br> [0x80005210]:csrrs a0, fcsr, zero<br> [0x80005214]:sw t6, 416(t1)<br>    |
| 464|[0x8000a28c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000524c]:feq.h t6, ft11, ft10<br> [0x80005250]:csrrs a0, fcsr, zero<br> [0x80005254]:sw t6, 424(t1)<br>    |
| 465|[0x8000a294]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000528c]:feq.h t6, ft11, ft10<br> [0x80005290]:csrrs a0, fcsr, zero<br> [0x80005294]:sw t6, 432(t1)<br>    |
| 466|[0x8000a29c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800052cc]:feq.h t6, ft11, ft10<br> [0x800052d0]:csrrs a0, fcsr, zero<br> [0x800052d4]:sw t6, 440(t1)<br>    |
| 467|[0x8000a2a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000530c]:feq.h t6, ft11, ft10<br> [0x80005310]:csrrs a0, fcsr, zero<br> [0x80005314]:sw t6, 448(t1)<br>    |
| 468|[0x8000a2ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000534c]:feq.h t6, ft11, ft10<br> [0x80005350]:csrrs a0, fcsr, zero<br> [0x80005354]:sw t6, 456(t1)<br>    |
| 469|[0x8000a2b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000538c]:feq.h t6, ft11, ft10<br> [0x80005390]:csrrs a0, fcsr, zero<br> [0x80005394]:sw t6, 464(t1)<br>    |
| 470|[0x8000a2bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800053cc]:feq.h t6, ft11, ft10<br> [0x800053d0]:csrrs a0, fcsr, zero<br> [0x800053d4]:sw t6, 472(t1)<br>    |
| 471|[0x8000a2c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000540c]:feq.h t6, ft11, ft10<br> [0x80005410]:csrrs a0, fcsr, zero<br> [0x80005414]:sw t6, 480(t1)<br>    |
| 472|[0x8000a2cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000544c]:feq.h t6, ft11, ft10<br> [0x80005450]:csrrs a0, fcsr, zero<br> [0x80005454]:sw t6, 488(t1)<br>    |
| 473|[0x8000a2d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000548c]:feq.h t6, ft11, ft10<br> [0x80005490]:csrrs a0, fcsr, zero<br> [0x80005494]:sw t6, 496(t1)<br>    |
| 474|[0x8000a2dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800054cc]:feq.h t6, ft11, ft10<br> [0x800054d0]:csrrs a0, fcsr, zero<br> [0x800054d4]:sw t6, 504(t1)<br>    |
| 475|[0x8000a2e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000550c]:feq.h t6, ft11, ft10<br> [0x80005510]:csrrs a0, fcsr, zero<br> [0x80005514]:sw t6, 512(t1)<br>    |
| 476|[0x8000a2ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000554c]:feq.h t6, ft11, ft10<br> [0x80005550]:csrrs a0, fcsr, zero<br> [0x80005554]:sw t6, 520(t1)<br>    |
| 477|[0x8000a2f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000558c]:feq.h t6, ft11, ft10<br> [0x80005590]:csrrs a0, fcsr, zero<br> [0x80005594]:sw t6, 528(t1)<br>    |
| 478|[0x8000a2fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800055cc]:feq.h t6, ft11, ft10<br> [0x800055d0]:csrrs a0, fcsr, zero<br> [0x800055d4]:sw t6, 536(t1)<br>    |
| 479|[0x8000a304]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000560c]:feq.h t6, ft11, ft10<br> [0x80005610]:csrrs a0, fcsr, zero<br> [0x80005614]:sw t6, 544(t1)<br>    |
| 480|[0x8000a30c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x255 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000564c]:feq.h t6, ft11, ft10<br> [0x80005650]:csrrs a0, fcsr, zero<br> [0x80005654]:sw t6, 552(t1)<br>    |
| 481|[0x8000a314]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000568c]:feq.h t6, ft11, ft10<br> [0x80005690]:csrrs a0, fcsr, zero<br> [0x80005694]:sw t6, 560(t1)<br>    |
| 482|[0x8000a31c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800056cc]:feq.h t6, ft11, ft10<br> [0x800056d0]:csrrs a0, fcsr, zero<br> [0x800056d4]:sw t6, 568(t1)<br>    |
| 483|[0x8000a324]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000570c]:feq.h t6, ft11, ft10<br> [0x80005710]:csrrs a0, fcsr, zero<br> [0x80005714]:sw t6, 576(t1)<br>    |
| 484|[0x8000a32c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000574c]:feq.h t6, ft11, ft10<br> [0x80005750]:csrrs a0, fcsr, zero<br> [0x80005754]:sw t6, 584(t1)<br>    |
| 485|[0x8000a334]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000578c]:feq.h t6, ft11, ft10<br> [0x80005790]:csrrs a0, fcsr, zero<br> [0x80005794]:sw t6, 592(t1)<br>    |
| 486|[0x8000a33c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800057cc]:feq.h t6, ft11, ft10<br> [0x800057d0]:csrrs a0, fcsr, zero<br> [0x800057d4]:sw t6, 600(t1)<br>    |
| 487|[0x8000a344]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000580c]:feq.h t6, ft11, ft10<br> [0x80005810]:csrrs a0, fcsr, zero<br> [0x80005814]:sw t6, 608(t1)<br>    |
| 488|[0x8000a34c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000584c]:feq.h t6, ft11, ft10<br> [0x80005850]:csrrs a0, fcsr, zero<br> [0x80005854]:sw t6, 616(t1)<br>    |
| 489|[0x8000a354]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000588c]:feq.h t6, ft11, ft10<br> [0x80005890]:csrrs a0, fcsr, zero<br> [0x80005894]:sw t6, 624(t1)<br>    |
| 490|[0x8000a35c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800058cc]:feq.h t6, ft11, ft10<br> [0x800058d0]:csrrs a0, fcsr, zero<br> [0x800058d4]:sw t6, 632(t1)<br>    |
| 491|[0x8000a364]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000590c]:feq.h t6, ft11, ft10<br> [0x80005910]:csrrs a0, fcsr, zero<br> [0x80005914]:sw t6, 640(t1)<br>    |
| 492|[0x8000a36c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000594c]:feq.h t6, ft11, ft10<br> [0x80005950]:csrrs a0, fcsr, zero<br> [0x80005954]:sw t6, 648(t1)<br>    |
| 493|[0x8000a374]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000598c]:feq.h t6, ft11, ft10<br> [0x80005990]:csrrs a0, fcsr, zero<br> [0x80005994]:sw t6, 656(t1)<br>    |
| 494|[0x8000a37c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800059cc]:feq.h t6, ft11, ft10<br> [0x800059d0]:csrrs a0, fcsr, zero<br> [0x800059d4]:sw t6, 664(t1)<br>    |
| 495|[0x8000a384]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005a0c]:feq.h t6, ft11, ft10<br> [0x80005a10]:csrrs a0, fcsr, zero<br> [0x80005a14]:sw t6, 672(t1)<br>    |
| 496|[0x8000a38c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005a4c]:feq.h t6, ft11, ft10<br> [0x80005a50]:csrrs a0, fcsr, zero<br> [0x80005a54]:sw t6, 680(t1)<br>    |
| 497|[0x8000a394]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005a8c]:feq.h t6, ft11, ft10<br> [0x80005a90]:csrrs a0, fcsr, zero<br> [0x80005a94]:sw t6, 688(t1)<br>    |
| 498|[0x8000a39c]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005acc]:feq.h t6, ft11, ft10<br> [0x80005ad0]:csrrs a0, fcsr, zero<br> [0x80005ad4]:sw t6, 696(t1)<br>    |
| 499|[0x8000a3a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005b0c]:feq.h t6, ft11, ft10<br> [0x80005b10]:csrrs a0, fcsr, zero<br> [0x80005b14]:sw t6, 704(t1)<br>    |
| 500|[0x8000a3ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005b4c]:feq.h t6, ft11, ft10<br> [0x80005b50]:csrrs a0, fcsr, zero<br> [0x80005b54]:sw t6, 712(t1)<br>    |
| 501|[0x8000a3b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005b8c]:feq.h t6, ft11, ft10<br> [0x80005b90]:csrrs a0, fcsr, zero<br> [0x80005b94]:sw t6, 720(t1)<br>    |
| 502|[0x8000a3bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005bcc]:feq.h t6, ft11, ft10<br> [0x80005bd0]:csrrs a0, fcsr, zero<br> [0x80005bd4]:sw t6, 728(t1)<br>    |
| 503|[0x8000a3c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005c0c]:feq.h t6, ft11, ft10<br> [0x80005c10]:csrrs a0, fcsr, zero<br> [0x80005c14]:sw t6, 736(t1)<br>    |
| 504|[0x8000a3cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x1f and fm1 == 0x001 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005c4c]:feq.h t6, ft11, ft10<br> [0x80005c50]:csrrs a0, fcsr, zero<br> [0x80005c54]:sw t6, 744(t1)<br>    |
| 505|[0x8000a3d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005c8c]:feq.h t6, ft11, ft10<br> [0x80005c90]:csrrs a0, fcsr, zero<br> [0x80005c94]:sw t6, 752(t1)<br>    |
| 506|[0x8000a3dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005ccc]:feq.h t6, ft11, ft10<br> [0x80005cd0]:csrrs a0, fcsr, zero<br> [0x80005cd4]:sw t6, 760(t1)<br>    |
| 507|[0x8000a3e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005d0c]:feq.h t6, ft11, ft10<br> [0x80005d10]:csrrs a0, fcsr, zero<br> [0x80005d14]:sw t6, 768(t1)<br>    |
| 508|[0x8000a3ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005d4c]:feq.h t6, ft11, ft10<br> [0x80005d50]:csrrs a0, fcsr, zero<br> [0x80005d54]:sw t6, 776(t1)<br>    |
| 509|[0x8000a3f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005d8c]:feq.h t6, ft11, ft10<br> [0x80005d90]:csrrs a0, fcsr, zero<br> [0x80005d94]:sw t6, 784(t1)<br>    |
| 510|[0x8000a3fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005dcc]:feq.h t6, ft11, ft10<br> [0x80005dd0]:csrrs a0, fcsr, zero<br> [0x80005dd4]:sw t6, 792(t1)<br>    |
| 511|[0x8000a404]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005e0c]:feq.h t6, ft11, ft10<br> [0x80005e10]:csrrs a0, fcsr, zero<br> [0x80005e14]:sw t6, 800(t1)<br>    |
| 512|[0x8000a40c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005e4c]:feq.h t6, ft11, ft10<br> [0x80005e50]:csrrs a0, fcsr, zero<br> [0x80005e54]:sw t6, 808(t1)<br>    |
| 513|[0x8000a414]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005e8c]:feq.h t6, ft11, ft10<br> [0x80005e90]:csrrs a0, fcsr, zero<br> [0x80005e94]:sw t6, 816(t1)<br>    |
| 514|[0x8000a41c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005ecc]:feq.h t6, ft11, ft10<br> [0x80005ed0]:csrrs a0, fcsr, zero<br> [0x80005ed4]:sw t6, 824(t1)<br>    |
| 515|[0x8000a424]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005f0c]:feq.h t6, ft11, ft10<br> [0x80005f10]:csrrs a0, fcsr, zero<br> [0x80005f14]:sw t6, 832(t1)<br>    |
| 516|[0x8000a42c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005f4c]:feq.h t6, ft11, ft10<br> [0x80005f50]:csrrs a0, fcsr, zero<br> [0x80005f54]:sw t6, 840(t1)<br>    |
| 517|[0x8000a434]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005f8c]:feq.h t6, ft11, ft10<br> [0x80005f90]:csrrs a0, fcsr, zero<br> [0x80005f94]:sw t6, 848(t1)<br>    |
| 518|[0x8000a43c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80005fcc]:feq.h t6, ft11, ft10<br> [0x80005fd0]:csrrs a0, fcsr, zero<br> [0x80005fd4]:sw t6, 856(t1)<br>    |
| 519|[0x8000a444]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000600c]:feq.h t6, ft11, ft10<br> [0x80006010]:csrrs a0, fcsr, zero<br> [0x80006014]:sw t6, 864(t1)<br>    |
| 520|[0x8000a44c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000604c]:feq.h t6, ft11, ft10<br> [0x80006050]:csrrs a0, fcsr, zero<br> [0x80006054]:sw t6, 872(t1)<br>    |
| 521|[0x8000a454]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000608c]:feq.h t6, ft11, ft10<br> [0x80006090]:csrrs a0, fcsr, zero<br> [0x80006094]:sw t6, 880(t1)<br>    |
| 522|[0x8000a45c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800060cc]:feq.h t6, ft11, ft10<br> [0x800060d0]:csrrs a0, fcsr, zero<br> [0x800060d4]:sw t6, 888(t1)<br>    |
| 523|[0x8000a464]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000610c]:feq.h t6, ft11, ft10<br> [0x80006110]:csrrs a0, fcsr, zero<br> [0x80006114]:sw t6, 896(t1)<br>    |
| 524|[0x8000a46c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000614c]:feq.h t6, ft11, ft10<br> [0x80006150]:csrrs a0, fcsr, zero<br> [0x80006154]:sw t6, 904(t1)<br>    |
| 525|[0x8000a474]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000618c]:feq.h t6, ft11, ft10<br> [0x80006190]:csrrs a0, fcsr, zero<br> [0x80006194]:sw t6, 912(t1)<br>    |
| 526|[0x8000a47c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800061cc]:feq.h t6, ft11, ft10<br> [0x800061d0]:csrrs a0, fcsr, zero<br> [0x800061d4]:sw t6, 920(t1)<br>    |
| 527|[0x8000a484]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000620c]:feq.h t6, ft11, ft10<br> [0x80006210]:csrrs a0, fcsr, zero<br> [0x80006214]:sw t6, 928(t1)<br>    |
| 528|[0x8000a48c]<br>0x00000000|- fs1 == 1 and fe1 == 0x1f and fm1 == 0x155 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000624c]:feq.h t6, ft11, ft10<br> [0x80006250]:csrrs a0, fcsr, zero<br> [0x80006254]:sw t6, 936(t1)<br>    |
| 529|[0x8000a494]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000628c]:feq.h t6, ft11, ft10<br> [0x80006290]:csrrs a0, fcsr, zero<br> [0x80006294]:sw t6, 944(t1)<br>    |
| 530|[0x8000a49c]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800062cc]:feq.h t6, ft11, ft10<br> [0x800062d0]:csrrs a0, fcsr, zero<br> [0x800062d4]:sw t6, 952(t1)<br>    |
| 531|[0x8000a4a4]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000630c]:feq.h t6, ft11, ft10<br> [0x80006310]:csrrs a0, fcsr, zero<br> [0x80006314]:sw t6, 960(t1)<br>    |
| 532|[0x8000a4ac]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000634c]:feq.h t6, ft11, ft10<br> [0x80006350]:csrrs a0, fcsr, zero<br> [0x80006354]:sw t6, 968(t1)<br>    |
| 533|[0x8000a4b4]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000638c]:feq.h t6, ft11, ft10<br> [0x80006390]:csrrs a0, fcsr, zero<br> [0x80006394]:sw t6, 976(t1)<br>    |
| 534|[0x8000a4bc]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800063cc]:feq.h t6, ft11, ft10<br> [0x800063d0]:csrrs a0, fcsr, zero<br> [0x800063d4]:sw t6, 984(t1)<br>    |
| 535|[0x8000a4c4]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000640c]:feq.h t6, ft11, ft10<br> [0x80006410]:csrrs a0, fcsr, zero<br> [0x80006414]:sw t6, 992(t1)<br>    |
| 536|[0x8000a4cc]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006444]:feq.h t6, ft11, ft10<br> [0x80006448]:csrrs a0, fcsr, zero<br> [0x8000644c]:sw t6, 1000(t1)<br>   |
| 537|[0x8000a4d4]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000647c]:feq.h t6, ft11, ft10<br> [0x80006480]:csrrs a0, fcsr, zero<br> [0x80006484]:sw t6, 1008(t1)<br>   |
| 538|[0x8000a4dc]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800064b4]:feq.h t6, ft11, ft10<br> [0x800064b8]:csrrs a0, fcsr, zero<br> [0x800064bc]:sw t6, 1016(t1)<br>   |
| 539|[0x8000a4e4]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800064f4]:feq.h t6, ft11, ft10<br> [0x800064f8]:csrrs a0, fcsr, zero<br> [0x800064fc]:sw t6, 0(t1)<br>      |
| 540|[0x8000a4ec]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000652c]:feq.h t6, ft11, ft10<br> [0x80006530]:csrrs a0, fcsr, zero<br> [0x80006534]:sw t6, 8(t1)<br>      |
| 541|[0x8000a4f4]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006564]:feq.h t6, ft11, ft10<br> [0x80006568]:csrrs a0, fcsr, zero<br> [0x8000656c]:sw t6, 16(t1)<br>     |
| 542|[0x8000a4fc]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000659c]:feq.h t6, ft11, ft10<br> [0x800065a0]:csrrs a0, fcsr, zero<br> [0x800065a4]:sw t6, 24(t1)<br>     |
| 543|[0x8000a504]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800065d4]:feq.h t6, ft11, ft10<br> [0x800065d8]:csrrs a0, fcsr, zero<br> [0x800065dc]:sw t6, 32(t1)<br>     |
| 544|[0x8000a50c]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000660c]:feq.h t6, ft11, ft10<br> [0x80006610]:csrrs a0, fcsr, zero<br> [0x80006614]:sw t6, 40(t1)<br>     |
| 545|[0x8000a514]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006644]:feq.h t6, ft11, ft10<br> [0x80006648]:csrrs a0, fcsr, zero<br> [0x8000664c]:sw t6, 48(t1)<br>     |
| 546|[0x8000a51c]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000667c]:feq.h t6, ft11, ft10<br> [0x80006680]:csrrs a0, fcsr, zero<br> [0x80006684]:sw t6, 56(t1)<br>     |
| 547|[0x8000a524]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800066b4]:feq.h t6, ft11, ft10<br> [0x800066b8]:csrrs a0, fcsr, zero<br> [0x800066bc]:sw t6, 64(t1)<br>     |
| 548|[0x8000a52c]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800066ec]:feq.h t6, ft11, ft10<br> [0x800066f0]:csrrs a0, fcsr, zero<br> [0x800066f4]:sw t6, 72(t1)<br>     |
| 549|[0x8000a534]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006724]:feq.h t6, ft11, ft10<br> [0x80006728]:csrrs a0, fcsr, zero<br> [0x8000672c]:sw t6, 80(t1)<br>     |
| 550|[0x8000a53c]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000675c]:feq.h t6, ft11, ft10<br> [0x80006760]:csrrs a0, fcsr, zero<br> [0x80006764]:sw t6, 88(t1)<br>     |
| 551|[0x8000a544]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006794]:feq.h t6, ft11, ft10<br> [0x80006798]:csrrs a0, fcsr, zero<br> [0x8000679c]:sw t6, 96(t1)<br>     |
| 552|[0x8000a54c]<br>0x00000000|- fs1 == 0 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800067cc]:feq.h t6, ft11, ft10<br> [0x800067d0]:csrrs a0, fcsr, zero<br> [0x800067d4]:sw t6, 104(t1)<br>    |
| 553|[0x8000a554]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006804]:feq.h t6, ft11, ft10<br> [0x80006808]:csrrs a0, fcsr, zero<br> [0x8000680c]:sw t6, 112(t1)<br>    |
| 554|[0x8000a55c]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000683c]:feq.h t6, ft11, ft10<br> [0x80006840]:csrrs a0, fcsr, zero<br> [0x80006844]:sw t6, 120(t1)<br>    |
| 555|[0x8000a564]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006874]:feq.h t6, ft11, ft10<br> [0x80006878]:csrrs a0, fcsr, zero<br> [0x8000687c]:sw t6, 128(t1)<br>    |
| 556|[0x8000a56c]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800068ac]:feq.h t6, ft11, ft10<br> [0x800068b0]:csrrs a0, fcsr, zero<br> [0x800068b4]:sw t6, 136(t1)<br>    |
| 557|[0x8000a574]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x002 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800068e4]:feq.h t6, ft11, ft10<br> [0x800068e8]:csrrs a0, fcsr, zero<br> [0x800068ec]:sw t6, 144(t1)<br>    |
| 558|[0x8000a57c]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3fe and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000691c]:feq.h t6, ft11, ft10<br> [0x80006920]:csrrs a0, fcsr, zero<br> [0x80006924]:sw t6, 152(t1)<br>    |
| 559|[0x8000a584]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006954]:feq.h t6, ft11, ft10<br> [0x80006958]:csrrs a0, fcsr, zero<br> [0x8000695c]:sw t6, 160(t1)<br>    |
| 560|[0x8000a58c]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x8000698c]:feq.h t6, ft11, ft10<br> [0x80006990]:csrrs a0, fcsr, zero<br> [0x80006994]:sw t6, 168(t1)<br>    |
| 561|[0x8000a594]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800069c4]:feq.h t6, ft11, ft10<br> [0x800069c8]:csrrs a0, fcsr, zero<br> [0x800069cc]:sw t6, 176(t1)<br>    |
| 562|[0x8000a59c]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x800069fc]:feq.h t6, ft11, ft10<br> [0x80006a00]:csrrs a0, fcsr, zero<br> [0x80006a04]:sw t6, 184(t1)<br>    |
| 563|[0x8000a5a4]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x01 and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006a34]:feq.h t6, ft11, ft10<br> [0x80006a38]:csrrs a0, fcsr, zero<br> [0x80006a3c]:sw t6, 192(t1)<br>    |
| 564|[0x8000a5ac]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x01 and fm2 == 0x055 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006a6c]:feq.h t6, ft11, ft10<br> [0x80006a70]:csrrs a0, fcsr, zero<br> [0x80006a74]:sw t6, 200(t1)<br>    |
| 565|[0x8000a5b4]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006aa4]:feq.h t6, ft11, ft10<br> [0x80006aa8]:csrrs a0, fcsr, zero<br> [0x80006aac]:sw t6, 208(t1)<br>    |
| 566|[0x8000a5bc]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1e and fm2 == 0x3ff and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006adc]:feq.h t6, ft11, ft10<br> [0x80006ae0]:csrrs a0, fcsr, zero<br> [0x80006ae4]:sw t6, 216(t1)<br>    |
| 567|[0x8000a5c4]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006b14]:feq.h t6, ft11, ft10<br> [0x80006b18]:csrrs a0, fcsr, zero<br> [0x80006b1c]:sw t6, 224(t1)<br>    |
| 568|[0x8000a5cc]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006b4c]:feq.h t6, ft11, ft10<br> [0x80006b50]:csrrs a0, fcsr, zero<br> [0x80006b54]:sw t6, 232(t1)<br>    |
| 569|[0x8000a5d4]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006b84]:feq.h t6, ft11, ft10<br> [0x80006b88]:csrrs a0, fcsr, zero<br> [0x80006b8c]:sw t6, 240(t1)<br>    |
| 570|[0x8000a5dc]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x200 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006bbc]:feq.h t6, ft11, ft10<br> [0x80006bc0]:csrrs a0, fcsr, zero<br> [0x80006bc4]:sw t6, 248(t1)<br>    |
| 571|[0x8000a5e4]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x201 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006bf4]:feq.h t6, ft11, ft10<br> [0x80006bf8]:csrrs a0, fcsr, zero<br> [0x80006bfc]:sw t6, 256(t1)<br>    |
| 572|[0x8000a5ec]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x255 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006c2c]:feq.h t6, ft11, ft10<br> [0x80006c30]:csrrs a0, fcsr, zero<br> [0x80006c34]:sw t6, 264(t1)<br>    |
| 573|[0x8000a5f4]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x1f and fm2 == 0x001 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006c64]:feq.h t6, ft11, ft10<br> [0x80006c68]:csrrs a0, fcsr, zero<br> [0x80006c6c]:sw t6, 272(t1)<br>    |
| 574|[0x8000a5fc]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x1f and fm2 == 0x155 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006c9c]:feq.h t6, ft11, ft10<br> [0x80006ca0]:csrrs a0, fcsr, zero<br> [0x80006ca4]:sw t6, 280(t1)<br>    |
| 575|[0x8000a604]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 0 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006cd4]:feq.h t6, ft11, ft10<br> [0x80006cd8]:csrrs a0, fcsr, zero<br> [0x80006cdc]:sw t6, 288(t1)<br>    |
| 576|[0x8000a60c]<br>0x00000000|- fs1 == 1 and fe1 == 0x0f and fm1 == 0x000 and fs2 == 1 and fe2 == 0x0f and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006d0c]:feq.h t6, ft11, ft10<br> [0x80006d10]:csrrs a0, fcsr, zero<br> [0x80006d14]:sw t6, 296(t1)<br>    |
| 577|[0x8000a614]<br>0x00000000|- fs1 == 0 and fe1 == 0x00 and fm1 == 0x000 and fs2 == 1 and fe2 == 0x00 and fm2 == 0x000 and  fcsr == 0 and rs1_nan_prefix == 0xffff and rs2_nan_prefix == 0xffff  #nosat<br>                                                                                        |[0x80006d44]:feq.h t6, ft11, ft10<br> [0x80006d48]:csrrs a0, fcsr, zero<br> [0x80006d4c]:sw t6, 304(t1)<br>    |

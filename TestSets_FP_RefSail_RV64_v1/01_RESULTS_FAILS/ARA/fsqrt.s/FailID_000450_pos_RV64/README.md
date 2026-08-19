# FailID_000450 ARA pos RV64 fsqrt.s

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 450
* Isolated failing instruction: `fsqrt.s`
* Minimized failing test case: [cblock_minimized_test_case.json](cblock_minimized_test_case.json)
* Resulting REF machine state: [mstate_RefSail.json](mstate_RefSail.json)
* Resulting DUT machine state: [mstate_DUT_ARA.json](mstate_DUT_ARA.json)
* Automated failure characterization report: [AFC_FP_report.log](AFC_FP_report.log)

## Report

### Minimized Failing Test Case
```
    // FLOATINGPOINT STATE DATA
    j _float_data_end
    .align 4
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x40,0x0a,0x01,0x03,0xe0,0x41
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x8c,0xe0,0x06,0x91,0x41
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x8c,0xe0,0x06,0x91,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0xf8,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x40,0x41,0x00,0xfa,0xdf,0xc1
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x4e,0x50,0xe0,0x4e,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x8c,0xe0,0x06,0x91,0x41
_float_data_end:
    // FLOATINTPOINT STATE
    la t0, _reg_f0
    fld  f0, 0(t0)
    la t0, _reg_f1
    fld  f1, 0(t0)
    la t0, _reg_f2
    fld  f2, 0(t0)
    la t0, _reg_f3
    fld  f3, 0(t0)
    la t0, _reg_f4
    fld  f4, 0(t0)
    la t0, _reg_f5
    fld  f5, 0(t0)
    la t0, _reg_f6
    fld  f6, 0(t0)
    la t0, _reg_f7
    fld  f7, 0(t0)
    la t0, _reg_f8
    fld  f8, 0(t0)
    la t0, _reg_f9
    fld  f9, 0(t0)
    la t0, _reg_f10
    fld  f10, 0(t0)
    la t0, _reg_f11
    fld  f11, 0(t0)
    la t0, _reg_f12
    fld  f12, 0(t0)
    la t0, _reg_f13
    fld  f13, 0(t0)
    la t0, _reg_f14
    fld  f14, 0(t0)
    la t0, _reg_f15
    fld  f15, 0(t0)
    la t0, _reg_f16
    fld  f16, 0(t0)
    la t0, _reg_f17
    fld  f17, 0(t0)
    la t0, _reg_f18
    fld  f18, 0(t0)
    la t0, _reg_f19
    fld  f19, 0(t0)
    la t0, _reg_f20
    fld  f20, 0(t0)
    la t0, _reg_f21
    fld  f21, 0(t0)
    la t0, _reg_f22
    fld  f22, 0(t0)
    la t0, _reg_f23
    fld  f23, 0(t0)
    la t0, _reg_f24
    fld  f24, 0(t0)
    la t0, _reg_f25
    fld  f25, 0(t0)
    la t0, _reg_f26
    fld  f26, 0(t0)
    la t0, _reg_f27
    fld  f27, 0(t0)
    la t0, _reg_f28
    fld  f28, 0(t0)
    la t0, _reg_f29
    fld  f29, 0(t0)
    la t0, _reg_f30
    fld  f30, 0(t0)
    la t0, _reg_f31
    fld  f31, 0(t0)

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x5d
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x200                 // ra
    li x2, 0x80180291            // sp
    li x3, 0x801804              // gp
    li x4, 0x0                   // tp
    li x5, 0x800000ec            // t0
    li x6, 0x0                   // t1
    li x7, 0x70282718            // t2
    li x8, 0x0                   // fp
    li x9, 0x8017f9e2            // s1
    li x10, 0x0                  // a0
    li x11, 0x800000ec           // a1
    li x12, 0x800003b6           // a2
    li x13, 0x8017fdef           // a3
    li x14, 0x8008090c           // a4
    li x15, 0x441b823            // a5
    li x16, 0x8008090c           // a6
    li x17, 0x80180331           // a7
    li x18, 0x0                  // s2
    li x19, 0x10000076c0000      // s3
    li x20, 0x0                  // s4
    li x21, 0xfffffffff6c56000   // s5
    li x22, 0xffffffffffffffff   // s6
    li x23, 0xffffffff7fe7ffcc   // s7
    li x24, 0x7fffffff           // s8
    li x25, 0x801ffc83           // s9
    li x26, 0x80000667           // s10
    li x27, 0x1                  // s11
    li x28, 0x0                  // t3
    li x29, 0x643                // t4
    li x30, 0x91f3               // t5
    li x31, 0x8017f9b5           // t6
    // INSTRUCTION ({'dep': {'f30', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'f2'}})
    fsqrt.s f2, f30, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f2                  0xffffffff47297254(43378.328125_s)              0xffffffff47297255(43378.33203125_s)            X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.s f2, f30, dyn
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f2                  0xffffffff47297254(43378.328125_s)              0xffffffff47297255(43378.33203125_s)            X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f2, f30
f2                  0xffffffff47297254(43378.328125_s)              0xffffffff47297255(43378.33203125_s)            X
f30                 0xffffffff4ee0504e(1881679616.0_s)              0xffffffff4ee0504e(1881679616.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000200(512)                         0x0000000000000200(512)                         
sp(x2)              0x0000000080180291(2149057169)                  0x0000000080180291(2149057169)                  
gp(x3)              0x0000000000801804(8394756)                     0x0000000000801804(8394756)                     
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x00000000800000ec(2147483884)                  0x00000000800000ec(2147483884)                  
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000070282718(1881679640)                  0x0000000070282718(1881679640)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x000000008017f9e2(2149054946)                  0x000000008017f9e2(2149054946)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x00000000800000ec(2147483884)                  0x00000000800000ec(2147483884)                  
a2(x12)             0x00000000800003b6(2147484598)                  0x00000000800003b6(2147484598)                  
a3(x13)             0x000000008017fdef(2149055983)                  0x000000008017fdef(2149055983)                  
a4(x14)             0x000000008008090c(2148010252)                  0x000000008008090c(2148010252)                  
a5(x15)             0x000000000441b823(71415843)                    0x000000000441b823(71415843)                    
a6(x16)             0x000000008008090c(2148010252)                  0x000000008008090c(2148010252)                  
a7(x17)             0x0000000080180331(2149057329)                  0x0000000080180331(2149057329)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x00010000076c0000(281475101229056)             0x00010000076c0000(281475101229056)             
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0xfffffffff6c56000(18446744073554714624)        0xfffffffff6c56000(18446744073554714624)        
s6(x22)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s7(x23)             0xffffffff7fe7ffcc(18446744071560495052)        0xffffffff7fe7ffcc(18446744071560495052)        
s8(x24)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s9(x25)             0x00000000801ffc83(2149579907)                  0x00000000801ffc83(2149579907)                  
s10(x26)            0x0000000080000667(2147485287)                  0x0000000080000667(2147485287)                  
s11(x27)            0x0000000000000001(1)                           0x0000000000000001(1)                           
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x0000000000000643(1603)                        0x0000000000000643(1603)                        
t5(x30)             0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
t6(x31)             0x000000008017f9b5(2149054901)                  0x000000008017f9b5(2149054901)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            6fc1f54a83c988b86f56a59c099681b7ef07612a        6fc1f54a83c988b86f56a59c099681b7ef07612a        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000071c(2147485468)                  0x000000008000071c(2147485468)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000005d(93)                          0x000000000000005d(93)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff47297254(43378.328125_s)              0xffffffff47297255(43378.33203125_s)            X
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x41e003010a400000(2149058642.0_d)              0x41e003010a400000(2149058642.0_d)              
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x419106e08c000000(71415843.0_d)                0x419106e08c000000(71415843.0_d)                
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x419106e08c000000(71415843.0_d)                0x419106e08c000000(71415843.0_d)                
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff4efffff8(2147482624.0_s)              0xffffffff4efffff8(2147482624.0_s)              
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xc1dffa0041400000(-2145911045.0_d)             0xc1dffa0041400000(-2145911045.0_d)             
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff4ee0504e(1881679616.0_s)              0xffffffff4ee0504e(1881679616.0_s)              
f31                 0x419106e08c000000(71415843.0_d)                0x419106e08c000000(71415843.0_d)                
STATES DIFFER: True
```

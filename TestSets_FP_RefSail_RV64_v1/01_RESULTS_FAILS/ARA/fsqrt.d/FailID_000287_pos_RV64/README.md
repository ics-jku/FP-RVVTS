# FailID_000287 ARA pos RV64 fsqrt.d

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 287
* Isolated failing instruction: `fsqrt.d`
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
_reg_f1: .byte 0x00,0x00,0x40,0x03,0x01,0x03,0xe0,0x41
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f4: .byte 0xe6,0x6e,0xab,0x4c,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0xf7,0xfe,0xff,0x7f,0x00,0x00,0x00,0x00
_reg_f12:.byte 0x03,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f14:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x10,0xb7,0x1b,0xbe,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x40,0x03,0x01,0x03,0xe0,0x41
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x24,0xf7,0x06,0xd9,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x1a,0x04,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0xbf
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0xe0,0xff,0xff,0xff,0xef,0x41
_reg_f31:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': True, 'of': True, 'dz': True, 'nv': True, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x9f
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x80000f0e            // ra
    li x2, 0x0                   // sp
    li x3, 0x80200ba6            // gp
    li x4, 0x8017fe6b            // tp
    li x5, 0x0                   // t0
    li x6, 0x0                   // t1
    li x7, 0x1                   // t2
    li x8, 0x0                   // fp
    li x9, 0x1b49970c            // s1
    li x10, 0x4f000003           // a0
    li x11, 0x0                  // a1
    li x12, 0x0                  // a2
    li x13, 0xffffffffffffffff   // a3
    li x14, 0x8000057c           // a4
    li x15, 0x0                  // a5
    li x16, 0x167                // a6
    li x17, 0x1ffffffffffffff    // a7
    li x18, 0xfffffffffff80000   // s2
    li x19, 0x0                  // s3
    li x20, 0x7ffffb48           // s4
    li x21, 0xffffffff4f000003   // s5
    li x22, 0xffffffffffffffff   // s6
    li x23, 0x80180236           // s7
    li x24, 0xfffffffff8000000   // s8
    li x25, 0x0                  // s9
    li x26, 0x0                  // s10
    li x27, 0x0                  // s11
    li x28, 0x7ffffef7           // t3
    li x29, 0x7ffffef7           // t4
    li x30, 0x340191f3           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f9', 'mstatus.fs/vs.fs'}, 'clob': {'f11'}})
    fsqrt.d f11, f9, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f11                 0x1f817ebe20856c37(6.371305271655502e-157_d)    0x1f817ebe20856c36(6.371305271655501e-157_d)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.d f11, f9, dyn
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'underflow', 'overflow', 'div-by-0', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f11                 0x1f817ebe20856c37(6.371305271655502e-157_d)    0x1f817ebe20856c36(6.371305271655501e-157_d)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f11, f9
f9                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)
f11                 0x1f817ebe20856c37(6.371305271655502e-157_d)    0x1f817ebe20856c36(6.371305271655501e-157_d)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080000f0e(2147487502)                  0x0000000080000f0e(2147487502)                  
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000080200ba6(2149583782)                  0x0000000080200ba6(2149583782)                  
tp(x4)              0x000000008017fe6b(2149056107)                  0x000000008017fe6b(2149056107)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000000000001(1)                           0x0000000000000001(1)                           
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x000000001b49970c(457807628)                   0x000000001b49970c(457807628)                   
a0(x10)             0x000000004f000003(1325400067)                  0x000000004f000003(1325400067)                  
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a4(x14)             0x000000008000057c(2147485052)                  0x000000008000057c(2147485052)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x0000000000000167(359)                         0x0000000000000167(359)                         
a7(x17)             0x01ffffffffffffff(144115188075855871)          0x01ffffffffffffff(144115188075855871)          
s2(x18)             0xfffffffffff80000(18446744073709027328)        0xfffffffffff80000(18446744073709027328)        
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000007ffffb48(2147482440)                  0x000000007ffffb48(2147482440)                  
s5(x21)             0xffffffff4f000003(18446744070739984387)        0xffffffff4f000003(18446744070739984387)        
s6(x22)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s7(x23)             0x0000000080180236(2149057078)                  0x0000000080180236(2149057078)                  
s8(x24)             0xfffffffff8000000(18446744073575333888)        0xfffffffff8000000(18446744073575333888)        
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x000000007ffffef7(2147483383)                  0x000000007ffffef7(2147483383)                  
t4(x29)             0x000000007ffffef7(2147483383)                  0x000000007ffffef7(2147483383)                  
t5(x30)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            0a565d9d111835f294db341e9dee56c05fb94552        0a565d9d111835f294db341e9dee56c05fb94552        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800006d8(2147485400)                  0x00000000800006d8(2147485400)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000009f(159)                         0x000000000000009f(159)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            True                                            True                                            
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x41e0030103400000(2149058586.0_d)              0x41e0030103400000(2149058586.0_d)              
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f4                  0xffffffff4cab6ee6(89880368.0_s)                0xffffffff4cab6ee6(89880368.0_s)                
f5                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x1f817ebe20856c37(6.371305271655502e-157_d)    0x1f817ebe20856c36(6.371305271655501e-157_d)    X
f12                 0xffffffff4f000003(2147484416.0_s)              0xffffffff4f000003(2147484416.0_s)              
f13                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f14                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffffbe1bb710(-0.15206551551818848_s)      0xffffffffbe1bb710(-0.15206551551818848_s)      
f21                 0x41e0030103400000(2149058586.0_d)              0x41e0030103400000(2149058586.0_d)              
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x00000000d906f724(1.7989485277e-314_d)         0x00000000d906f724(1.7989485277e-314_d)         
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x000000008018041a(1.0617755123e-314_d)         0x000000008018041a(1.0617755123e-314_d)         
f27                 0xbff0000000000000(-1.0_d)                      0xbff0000000000000(-1.0_d)                      
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x41efffffffe00000(4294967295.0_d)              0x41efffffffe00000(4294967295.0_d)              
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

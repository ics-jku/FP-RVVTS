# FailID_000292 ARA pos RV64 fsqrt.d

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 292
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x80,0x42,0x00,0x00,0xe0,0x41
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x01,0x20,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x07,0x04,0x00,0x80,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0xd4,0xfe,0xff,0x7f,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x0f,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f26:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x54
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x0                   // sp
    li x3, 0x6000                // gp
    li x4, 0x0                   // tp
    li x5, 0x0                   // t0
    li x6, 0x0                   // t1
    li x7, 0x0                   // t2
    li x8, 0x73                  // fp
    li x9, 0x9793000             // s1
    li x10, 0x0                  // a0
    li x11, 0x801807c9           // a1
    li x12, 0x801ffa6f           // a2
    li x13, 0x7fffffffffffffff   // a3
    li x14, 0xcc7c000            // a4
    li x15, 0x44                 // a5
    li x16, 0x7fffffff           // a6
    li x17, 0x8027fcff           // a7
    li x18, 0x0                  // s2
    li x19, 0x0                  // s3
    li x20, 0x2005fea240000000   // s4
    li x21, 0x7fffffff           // s5
    li x22, 0x0                  // s6
    li x23, 0x7fffffffffffffff   // s7
    li x24, 0xffffffffffffffff   // s8
    li x25, 0x802006d8           // s9
    li x26, 0xffffffffffffffff   // s10
    li x27, 0x200                // s11
    li x28, 0x0                  // t3
    li x29, 0x1                  // t4
    li x30, 0x800000d4           // t5
    li x31, 0x80000407           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f13'}, 'clob': {'f26'}})
    fsqrt.d f26, f13
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f26                 0x1f56a09ec1a01903(1.0300477682439377e-157_d)   0x1f56a09ec1a01904(1.0300477682439378e-157_d)   X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.d f26, f13
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f26                 0x1f56a09ec1a01903(1.0300477682439377e-157_d)   0x1f56a09ec1a01904(1.0300477682439378e-157_d)   X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f26, f13
f13                 0x0000000080000407(1.060998405e-314_d)          0x0000000080000407(1.060998405e-314_d)
f26                 0x1f56a09ec1a01903(1.0300477682439377e-157_d)   0x1f56a09ec1a01904(1.0300477682439378e-157_d)   X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x0000000000000073(115)                         0x0000000000000073(115)                         
s1(x9)              0x0000000009793000(158937088)                   0x0000000009793000(158937088)                   
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x00000000801807c9(2149058505)                  0x00000000801807c9(2149058505)                  
a2(x12)             0x00000000801ffa6f(2149579375)                  0x00000000801ffa6f(2149579375)                  
a3(x13)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
a4(x14)             0x000000000cc7c000(214417408)                   0x000000000cc7c000(214417408)                   
a5(x15)             0x0000000000000044(68)                          0x0000000000000044(68)                          
a6(x16)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a7(x17)             0x000000008027fcff(2150104319)                  0x000000008027fcff(2150104319)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x2005fea240000000(2307530356909146112)         0x2005fea240000000(2307530356909146112)         
s5(x21)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s8(x24)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s9(x25)             0x00000000802006d8(2149582552)                  0x00000000802006d8(2149582552)                  
s10(x26)            0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s11(x27)            0x0000000000000200(512)                         0x0000000000000200(512)                         
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x00000000800000d4(2147483860)                  0x00000000800000d4(2147483860)                  
t6(x31)             0x0000000080000407(2147484679)                  0x0000000080000407(2147484679)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            486d7313a6cb78d793434610eae468f6da1a1a7b        486d7313a6cb78d793434610eae468f6da1a1a7b        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800006d8(2147485400)                  0x00000000800006d8(2147485400)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000055(85)                          0x0000000000000055(85)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0x41e0000042800000(2147484180.0_d)              0x41e0000042800000(2147484180.0_d)              
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7fffffff4f002001(nan_d)                       0x7fffffff4f002001(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000080000407(1.060998405e-314_d)          0x0000000080000407(1.060998405e-314_d)          
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x000000007ffffed4(1.0609977473e-314_d)         0x000000007ffffed4(1.0609977473e-314_d)         
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff4f00180f(2149060352.0_s)              0xffffffff4f00180f(2149060352.0_s)              
f25                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f26                 0x1f56a09ec1a01903(1.0300477682439377e-157_d)   0x1f56a09ec1a01904(1.0300477682439378e-157_d)   X
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f31                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
STATES DIFFER: True
```

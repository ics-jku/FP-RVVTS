# FailID_001493 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1493
* Isolated failing instruction: `flw`
* Minimized failing test case: [cblock_minimized_test_case.json](cblock_minimized_test_case.json)
* Resulting REF machine state: [mstate_RefSail.json](mstate_RefSail.json)
* Resulting DUT machine state: [mstate_DUT_VPpp_FF.json](mstate_DUT_VPpp_FF.json)
* Automated failure characterization report: [AFC_FP_report.log](AFC_FP_report.log)

## Report

### Minimized Failing Test Case
```
    // FLOATINGPOINT STATE DATA
    j _float_data_end
    .align 4
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x5e,0xa8,0x2a,0x48,0xf4,0xb7,0xd9,0xce
_reg_f10:.byte 0x5a,0x7c,0x7c,0x84,0x6d,0x5a,0x28,0xba
_reg_f11:.byte 0xf2,0x06,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0x00,0x90,0xfe,0xff,0x7f,0x41
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x1f,0x0e,0x49,0xca,0x93,0x07,0x92,0xd1
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x2d,0x00,0x00,0xe0,0x41
_reg_f17:.byte 0x5a,0x7c,0x7c,0x84,0x6d,0x5a,0x28,0xba
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0xe7,0x1f,0xb3,0x8c,0xe2,0xc6,0x9b,0x22
_reg_f21:.byte 0x81,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x44,0x53,0x8e,0x0e,0x33,0x02,0xb8,0x29
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x76,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x44,0x53,0x8e,0x0e,0x33,0x02,0xb8,0x29
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x67,0xa0,0xa1,0xe8,0x3f,0x0d,0xc2,0x1d
_reg_f28:.byte 0x5e,0x69,0xd8,0x61,0x05,0xf4,0xa0,0xf7
_reg_f29:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x4c,0x84,0x8f,0xe4,0xea,0x38,0x36,0xbb
_reg_f31:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'res0(0b101)', 'res': 0}
    li t0, 0xa4
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017f814            // ra
    li x2, 0x8017f2b2            // sp
    li x3, 0x0                   // gp
    li x4, 0x51b023340191f3      // tp
    li x5, 0x100                 // t0
    li x6, 0x7ffffeee            // t1
    li x7, 0x7bfba000            // t2
    li x8, 0x8027f414            // fp
    li x9, 0x80180629            // s1
    li x10, 0x8000007a           // a0
    li x11, 0x7f84114d           // a1
    li x12, 0x1                  // a2
    li x13, 0x8020032f           // a3
    li x14, 0x8000025e           // a4
    li x15, 0x800004bb           // a5
    li x16, 0x7ffff83d           // a6
    li x17, 0x800003e0           // a7
    li x18, 0x801fe339           // s2
    li x19, 0x7ffff83d           // s3
    li x20, 0x801a7616           // s4
    li x21, 0x800002e0           // s5
    li x22, 0x340191f3           // s6
    li x23, 0x93f3b3             // s7
    li x24, 0x80180638           // s8
    li x25, 0x2d685000           // s9
    li x26, 0xd5                 // s10
    li x27, 0x800002bb           // s11
    li x28, 0x801806a2           // t3
    li x29, 0x80180629           // t4
    li x30, 0x8017f8d9           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x7'}, 'clob': {'x7', 'f5', 'x20'}})
    
    li x20, 0x1ffffc
    and x7, x7, x20
    li x20, 0x80000017
    add x7, x7, x20
    flw f5, -0x17(x7)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f5, -0x17(x7)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f5, x17, x7
t2(x7)              0x00000000801ba017(2149294103)                  0x00000000801ba017(2149294103)
a7(x17)             0x00000000800003e0(2147484640)                  0x00000000800003e0(2147484640)
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017f814(2149054484)                  0x000000008017f814(2149054484)                  
sp(x2)              0x000000008017f2b2(2149053106)                  0x000000008017f2b2(2149053106)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x0051b023340191f3(22993138356425203)           0x0051b023340191f3(22993138356425203)           
t0(x5)              0x0000000000000100(256)                         0x0000000000000100(256)                         
t1(x6)              0x000000007ffffeee(2147483374)                  0x000000007ffffeee(2147483374)                  
t2(x7)              0x00000000801ba017(2149294103)                  0x00000000801ba017(2149294103)                  
fp(x8)              0x000000008027f414(2150102036)                  0x000000008027f414(2150102036)                  
s1(x9)              0x0000000080180629(2149058089)                  0x0000000080180629(2149058089)                  
a0(x10)             0x000000008000007a(2147483770)                  0x000000008000007a(2147483770)                  
a1(x11)             0x000000007f84114d(2139361613)                  0x000000007f84114d(2139361613)                  
a2(x12)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a3(x13)             0x000000008020032f(2149581615)                  0x000000008020032f(2149581615)                  
a4(x14)             0x000000008000025e(2147484254)                  0x000000008000025e(2147484254)                  
a5(x15)             0x00000000800004bb(2147484859)                  0x00000000800004bb(2147484859)                  
a6(x16)             0x000000007ffff83d(2147481661)                  0x000000007ffff83d(2147481661)                  
a7(x17)             0x00000000800003e0(2147484640)                  0x00000000800003e0(2147484640)                  
s2(x18)             0x00000000801fe339(2149573433)                  0x00000000801fe339(2149573433)                  
s3(x19)             0x000000007ffff83d(2147481661)                  0x000000007ffff83d(2147481661)                  
s4(x20)             0x0000000080000017(2147483671)                  0x0000000080000017(2147483671)                  
s5(x21)             0x00000000800002e0(2147484384)                  0x00000000800002e0(2147484384)                  
s6(x22)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
s7(x23)             0x000000000093f3b3(9696179)                     0x000000000093f3b3(9696179)                     
s8(x24)             0x0000000080180638(2149058104)                  0x0000000080180638(2149058104)                  
s9(x25)             0x000000002d685000(761810944)                   0x000000002d685000(761810944)                   
s10(x26)            0x00000000000000d5(213)                         0x00000000000000d5(213)                         
s11(x27)            0x00000000800002bb(2147484347)                  0x00000000800002bb(2147484347)                  
t3(x28)             0x00000000801806a2(2149058210)                  0x00000000801806a2(2149058210)                  
t4(x29)             0x0000000080180629(2149058089)                  0x0000000080180629(2149058089)                  
t5(x30)             0x000000008017f8d9(2149054681)                  0x000000008017f8d9(2149054681)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            d6ab37977a0ac6b88e5ca9344b4b03eed5726c13        d6ab37977a0ac6b88e5ca9344b4b03eed5726c13        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000770(2147485552)                  0x0000000080000770(2147485552)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000a4(164)                         0x00000000000000a4(164)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            res0(0b101)                                     res0(0b101)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
f6                  0x7fffffff46c00000(nan_d)                       0x7fffffff46c00000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xced9b7f4482aa85e(-7.100122191866003e+71_d)    0xced9b7f4482aa85e(-7.100122191866003e+71_d)    
f10                 0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   
f11                 0x00000000801806f2(1.061775872e-314_d)          0x00000000801806f2(1.061775872e-314_d)          
f12                 0x417ffffe90000000(33554409.0_d)                0x417ffffe90000000(33554409.0_d)                
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xd1920793ca490e1f(-8.756385205883228e+84_d)    0xd1920793ca490e1f(-8.756385205883228e+84_d)    
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x41e000002d000000(2147484008.0_d)              0x41e000002d000000(2147484008.0_d)              
f17                 0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0x229bc6e28cb31fe7(5.694633027608313e-142_d)    0x229bc6e28cb31fe7(5.694633027608313e-142_d)    
f21                 0xfffffffffffffe81(nan_h)                       0xfffffffffffffe81(nan_h)                       
f22                 0x29b802330e8e5344(1.0222761870252597e-107_d)   0x29b802330e8e5344(1.0222761870252597e-107_d)   
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffffffff7600(24576.0_h)                   0xffffffffffff7600(24576.0_h)                   
f25                 0x29b802330e8e5344(1.0222761870252597e-107_d)   0x29b802330e8e5344(1.0222761870252597e-107_d)   
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x1dc20d3fe8a1a067(2.4490173050100153e-165_d)   0x1dc20d3fe8a1a067(2.4490173050100153e-165_d)   
f28                 0xf7a0f40561d8695e(-1.749274728489661e+268_d)   0xf7a0f40561d8695e(-1.749274728489661e+268_d)   
f29                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f30                 0xbb3638eae48f844c(-1.8381883999299958e-23_d)   0xbb3638eae48f844c(-1.8381883999299958e-23_d)   
f31                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
STATES DIFFER: True
```

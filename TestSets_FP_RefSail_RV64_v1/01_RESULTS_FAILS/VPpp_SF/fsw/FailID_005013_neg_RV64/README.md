# FailID_005013 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 5013
* Isolated failing instruction: `fsw`
* Minimized failing test case: [cblock_minimized_test_case.json](cblock_minimized_test_case.json)
* Resulting REF machine state: [mstate_RefSail.json](mstate_RefSail.json)
* Resulting DUT machine state: [mstate_DUT_VPpp_SF.json](mstate_DUT_VPpp_SF.json)
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
    li x1, 0x7ffff8e1            // ra
    li x2, 0x8017f2b2            // sp
    li x3, 0x0                   // gp
    li x4, 0xff                  // tp
    li x5, 0x80000168            // t0
    li x6, 0x8086371c            // t1
    li x7, 0x0                   // t2
    li x8, 0x1fffffffc00         // fp
    li x9, 0x80180758            // s1
    li x10, 0x8000006f           // a0
    li x11, 0x8028068a           // a1
    li x12, 0x1                  // a2
    li x13, 0x8020032f           // a3
    li x14, 0x8017fdff           // a4
    li x15, 0x200                // a5
    li x16, 0x7ffffc56           // a6
    li x17, 0x100                // a7
    li x18, 0x801fe339           // s2
    li x19, 0x0                  // s3
    li x20, 0xd1a7728            // s4
    li x21, 0x2c                 // s5
    li x22, 0x340191f3           // s6
    li x23, 0x8017fee3           // s7
    li x24, 0x80000139           // s8
    li x25, 0x2d685000           // s9
    li x26, 0xd5                 // s10
    li x27, 0x80000168           // s11
    li x28, 0x801806a2           // t3
    li x29, 0x10030087600000     // t4
    li x30, 0xba                 // t5
    li x31, 0x7fffffff           // t6
    // INSTRUCTION ({'dep': {'f31', 'fcsr.rm', 'x8', 'mstatus.fs/vs.fs'}, 'clob': {'x1', 'x8'}})
    
    li x1, 0xffffc
    and x8, x8, x1
    li x1, 0x8017f814
    add x8, x8, x1
    fsw f31, 0x7ec(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f31, 0x7ec(x8)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f31, x7, x8
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)
fp(x8)              0x000000008027f414(2150102036)                  0x000000008027f414(2150102036)
f31                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017f814(2149054484)                  0x000000008017f814(2149054484)                  
sp(x2)              0x000000008017f2b2(2149053106)                  0x000000008017f2b2(2149053106)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x00000000000000ff(255)                         0x00000000000000ff(255)                         
t0(x5)              0x0000000080000168(2147484008)                  0x0000000080000168(2147484008)                  
t1(x6)              0x000000008086371c(2156279580)                  0x000000008086371c(2156279580)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x000000008027f414(2150102036)                  0x000000008027f414(2150102036)                  
s1(x9)              0x0000000080180758(2149058392)                  0x0000000080180758(2149058392)                  
a0(x10)             0x000000008000006f(2147483759)                  0x000000008000006f(2147483759)                  
a1(x11)             0x000000008028068a(2150106762)                  0x000000008028068a(2150106762)                  
a2(x12)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a3(x13)             0x000000008020032f(2149581615)                  0x000000008020032f(2149581615)                  
a4(x14)             0x000000008017fdff(2149055999)                  0x000000008017fdff(2149055999)                  
a5(x15)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a6(x16)             0x000000007ffffc56(2147482710)                  0x000000007ffffc56(2147482710)                  
a7(x17)             0x0000000000000100(256)                         0x0000000000000100(256)                         
s2(x18)             0x00000000801fe339(2149573433)                  0x00000000801fe339(2149573433)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000000d1a7728(219838248)                   0x000000000d1a7728(219838248)                   
s5(x21)             0x000000000000002c(44)                          0x000000000000002c(44)                          
s6(x22)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
s7(x23)             0x000000008017fee3(2149056227)                  0x000000008017fee3(2149056227)                  
s8(x24)             0x0000000080000139(2147483961)                  0x0000000080000139(2147483961)                  
s9(x25)             0x000000002d685000(761810944)                   0x000000002d685000(761810944)                   
s10(x26)            0x00000000000000d5(213)                         0x00000000000000d5(213)                         
s11(x27)            0x0000000080000168(2147484008)                  0x0000000080000168(2147484008)                  
t3(x28)             0x00000000801806a2(2149058210)                  0x00000000801806a2(2149058210)                  
t4(x29)             0x0010030087600000(4506900433469440)            0x0010030087600000(4506900433469440)            
t5(x30)             0x00000000000000ba(186)                         0x00000000000000ba(186)                         
t6(x31)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            ba7925caa365aef5cc15ebc3dd36ca8ee5f23345        ba7925caa365aef5cc15ebc3dd36ca8ee5f23345        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000074c(2147485516)                  0x000000008000074c(2147485516)                  
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
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
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

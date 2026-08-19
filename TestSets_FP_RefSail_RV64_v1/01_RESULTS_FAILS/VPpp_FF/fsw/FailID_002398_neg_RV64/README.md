# FailID_002398 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2398
* Isolated failing instruction: `fsw`
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
_reg_f1: .byte 0xbb,0x9f,0x0f,0x0b,0xc6,0x70,0x56,0xdf
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x5e,0xa8,0x2a,0x48,0xf4,0xb7,0xd9,0xce
_reg_f4: .byte 0x5e,0x69,0xd8,0x61,0x05,0xf4,0xa0,0xf7
_reg_f5: .byte 0xfa,0xfb,0xd2,0xc2,0xa7,0xff,0x83,0x57
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x5a,0x7c,0x7c,0x84,0x6d,0x5a,0x28,0xba
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x5e,0xa8,0x2a,0x48,0xf4,0xb7,0xd9,0xce
_reg_f10:.byte 0x5a,0x7c,0x7c,0x84,0x6d,0x5a,0x28,0xba
_reg_f11:.byte 0xf2,0x06,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x1f,0x0e,0x49,0xca,0x93,0x07,0x92,0xd1
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0xdb,0x1b,0xb6,0x3c,0xae,0xb5,0x4f,0x1c
_reg_f17:.byte 0x5a,0x7c,0x7c,0x84,0x6d,0x5a,0x28,0xba
_reg_f18:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f19:.byte 0xc1,0x80,0x3a,0xeb,0xf4,0xf0,0x38,0xeb
_reg_f20:.byte 0xe7,0x1f,0xb3,0x8c,0xe2,0xc6,0x9b,0x22
_reg_f21:.byte 0x81,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x44,0x53,0x8e,0x0e,0x33,0x02,0xb8,0x29
_reg_f23:.byte 0x41,0x44,0x32,0x3c,0x2e,0x4e,0x76,0x4e
_reg_f24:.byte 0x33,0x07,0x9a,0x3b,0xe2,0xdf,0x5b,0x1c
_reg_f25:.byte 0x65,0x13,0xef,0x7d,0x42,0xf7,0xd6,0x1d
_reg_f26:.byte 0xdb,0x1b,0xb6,0x3c,0xae,0xb5,0x4f,0x1c
_reg_f27:.byte 0x67,0xa0,0xa1,0xe8,0x3f,0x0d,0xc2,0x1d
_reg_f28:.byte 0x5e,0x69,0xd8,0x61,0x05,0xf4,0xa0,0xf7
_reg_f29:.byte 0xfd,0x23,0x18,0x60,0xca,0xd9,0x45,0xe1
_reg_f30:.byte 0x4c,0x84,0x8f,0xe4,0xea,0x38,0x36,0xbb
_reg_f31:.byte 0x5e,0xa8,0x2a,0x48,0xf4,0xb7,0xd9,0xce
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x7d
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7c                  // ra
    li x2, 0x6000                // sp
    li x3, 0x8027a1fd            // gp
    li x4, 0xffffffffffffffff    // tp
    li x5, 0x801805bf            // t0
    li x6, 0x2                   // t1
    li x7, 0x7fffffffffffffff    // t2
    li x8, 0xffffffb09           // fp
    li x9, 0x0                   // s1
    li x10, 0xffffffffe          // a0
    li x11, 0x58246a57           // a1
    li x12, 0x8017fa64           // a2
    li x13, 0x8017fa64           // a3
    li x14, 0x8017fc73           // a4
    li x15, 0x2e                 // a5
    li x16, 0x7fffffff           // a6
    li x17, 0x80180245           // a7
    li x18, 0x0                  // s2
    li x19, 0x7ffffe81           // s3
    li x20, 0x6000               // s4
    li x21, 0x0                  // s5
    li x22, 0x0                  // s6
    li x23, 0x200                // s7
    li x24, 0x0                  // s8
    li x25, 0x6000               // s9
    li x26, 0x0                  // s10
    li x27, 0x8000057e           // s11
    li x28, 0x801803e5           // t3
    li x29, 0xa7                 // t4
    li x30, 0x0                  // t5
    li x31, 0xffffffffffffffff   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f9', 'x3'}, 'clob': {'x2', 'x3'}})
    
    li x2, 0xffffc
    and x3, x3, x2
    li x2, 0x8017f851
    add x3, x3, x2
    fsw f9, 0x7af(x3)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        989542c81868f6dfc47dcb7d6aba20225b1be94b        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f9, 0x7af(x3)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        989542c81868f6dfc47dcb7d6aba20225b1be94b        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x7, x3
gp(x3)              0x00000000801f9a4d(2149554765)                  0x00000000801f9a4d(2149554765)
t2(x7)              0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)
f9                  0xced9b7f4482aa85e(-7.100122191866003e+71_d)    0xced9b7f4482aa85e(-7.100122191866003e+71_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000000000007c(124)                         0x000000000000007c(124)                         
sp(x2)              0x000000008017f851(2149054545)                  0x000000008017f851(2149054545)                  
gp(x3)              0x00000000801f9a4d(2149554765)                  0x00000000801f9a4d(2149554765)                  
tp(x4)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t0(x5)              0x00000000801805bf(2149057983)                  0x00000000801805bf(2149057983)                  
t1(x6)              0x0000000000000002(2)                           0x0000000000000002(2)                           
t2(x7)              0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
fp(x8)              0x0000000ffffffb09(68719475465)                 0x0000000ffffffb09(68719475465)                 
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x0000000ffffffffe(68719476734)                 0x0000000ffffffffe(68719476734)                 
a1(x11)             0x0000000058246a57(1478781527)                  0x0000000058246a57(1478781527)                  
a2(x12)             0x000000008017fa64(2149055076)                  0x000000008017fa64(2149055076)                  
a3(x13)             0x000000008017fa64(2149055076)                  0x000000008017fa64(2149055076)                  
a4(x14)             0x000000008017fc73(2149055603)                  0x000000008017fc73(2149055603)                  
a5(x15)             0x000000000000002e(46)                          0x000000000000002e(46)                          
a6(x16)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a7(x17)             0x0000000080180245(2149057093)                  0x0000000080180245(2149057093)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000007ffffe81(2147483265)                  0x000000007ffffe81(2147483265)                  
s4(x20)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000008000057e(2147485054)                  0x000000008000057e(2147485054)                  
t3(x28)             0x00000000801803e5(2149057509)                  0x00000000801803e5(2149057509)                  
t4(x29)             0x00000000000000a7(167)                         0x00000000000000a7(167)                         
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        

STATE               REF                                             DUT                                             DIFF
xmemhash            df9fe4f1f2ff0d1e9b7768e07134ff53cee05986        df9fe4f1f2ff0d1e9b7768e07134ff53cee05986        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        989542c81868f6dfc47dcb7d6aba20225b1be94b        X
lastPC              0x0000000080000718(2147485464)                  0x0000000080000718(2147485464)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000007d(125)                         0x000000000000007d(125)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0xdf5670c60b0f9fbb(-1.8364148405546734e+151_d)  0xdf5670c60b0f9fbb(-1.8364148405546734e+151_d)  
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xced9b7f4482aa85e(-7.100122191866003e+71_d)    0xced9b7f4482aa85e(-7.100122191866003e+71_d)    
f4                  0xf7a0f40561d8695e(-1.749274728489661e+268_d)   0xf7a0f40561d8695e(-1.749274728489661e+268_d)   
f5                  0x5783ffa7c2d2fbfa(3.847593126398991e+113_d)    0x5783ffa7c2d2fbfa(3.847593126398991e+113_d)    
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xced9b7f4482aa85e(-7.100122191866003e+71_d)    0xced9b7f4482aa85e(-7.100122191866003e+71_d)    
f10                 0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   
f11                 0x00000000801806f2(1.061775872e-314_d)          0x00000000801806f2(1.061775872e-314_d)          
f12                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f13                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f14                 0xd1920793ca490e1f(-8.756385205883228e+84_d)    0xd1920793ca490e1f(-8.756385205883228e+84_d)    
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x1c4fb5ae3cb61bdb(2.564156262967477e-172_d)    0x1c4fb5ae3cb61bdb(2.564156262967477e-172_d)    
f17                 0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   
f18                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f19                 0xeb38f0f4eb3a80c1(-3.202985767625313e+208_d)   0xeb38f0f4eb3a80c1(-3.202985767625313e+208_d)   
f20                 0x229bc6e28cb31fe7(5.694633027608313e-142_d)    0x229bc6e28cb31fe7(5.694633027608313e-142_d)    
f21                 0xfffffffffffffe81(nan_h)                       0xfffffffffffffe81(nan_h)                       
f22                 0x29b802330e8e5344(1.0222761870252597e-107_d)   0x29b802330e8e5344(1.0222761870252597e-107_d)   
f23                 0x4e764e2e3c324441(9.621635287386913e+69_d)     0x4e764e2e3c324441(9.621635287386913e+69_d)     
f24                 0x1c5bdfe23b9a0733(4.508066234129458e-172_d)    0x1c5bdfe23b9a0733(4.508066234129458e-172_d)    
f25                 0x1dd6f7427def1365(6.231391913634826e-165_d)    0x1dd6f7427def1365(6.231391913634826e-165_d)    
f26                 0x1c4fb5ae3cb61bdb(2.564156262967477e-172_d)    0x1c4fb5ae3cb61bdb(2.564156262967477e-172_d)    
f27                 0x1dc20d3fe8a1a067(2.4490173050100153e-165_d)   0x1dc20d3fe8a1a067(2.4490173050100153e-165_d)   
f28                 0xf7a0f40561d8695e(-1.749274728489661e+268_d)   0xf7a0f40561d8695e(-1.749274728489661e+268_d)   
f29                 0xe145d9ca601823fd(-3.840024013324784e+160_d)   0xe145d9ca601823fd(-3.840024013324784e+160_d)   
f30                 0xbb3638eae48f844c(-1.8381883999299958e-23_d)   0xbb3638eae48f844c(-1.8381883999299958e-23_d)   
f31                 0xced9b7f4482aa85e(-7.100122191866003e+71_d)    0xced9b7f4482aa85e(-7.100122191866003e+71_d)    
STATES DIFFER: True
```

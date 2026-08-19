# FailID_002188 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2188
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0xfe,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x01,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0xf4,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x0b,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x0f,0xff,0xff,0x7f,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xc8
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x1da041              // sp
    li x3, 0xe8                  // gp
    li x4, 0xffffffffc2a7d000    // tp
    li x5, 0xfffffffea2949884    // t0
    li x6, 0xffffffff7ffff99f    // t1
    li x7, 0x8017fdc2            // t2
    li x8, 0x0                   // fp
    li x9, 0x8017f73f            // s1
    li x10, 0x0                  // a0
    li x11, 0x1                  // a1
    li x12, 0x80180f62           // a2
    li x13, 0x5a                 // a3
    li x14, 0x809                // a4
    li x15, 0x8018068d           // a5
    li x16, 0x2a02e              // a6
    li x17, 0x23fc0738           // a7
    li x18, 0x80180483           // s2
    li x19, 0x340191f3           // s3
    li x20, 0xffffffff84e2d000   // s4
    li x21, 0x7ffffee9           // s5
    li x22, 0x801da0cd           // s6
    li x23, 0x801e4cb1           // s7
    li x24, 0x80000661           // s8
    li x25, 0x8017f92f           // s9
    li x26, 0xe24e377c           // s10
    li x27, 0x0                  // s11
    li x28, 0x801801dc           // t3
    li x29, 0x1                  // t4
    li x30, 0x1758974c           // t5
    li x31, 0xdb                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f13', 'mstatus.fs/vs.fs', 'x9'}, 'clob': {'x9', 'x28'}})
    
    li x28, 0xffffc
    and x9, x9, x28
    li x28, 0x8017fa21
    add x9, x9, x28
    fsw f13, 0x5df(x9)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ad65a972b7aac824b7c5b0acd40e486f3245e170        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f13, 0x5df(x9)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ad65a972b7aac824b7c5b0acd40e486f3245e170        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x5, x9
t0(x5)              0xfffffffea2949884(18446744067847264388)        0xfffffffea2949884(18446744067847264388)
s1(x9)              0x00000000801ff15d(2149577053)                  0x00000000801ff15d(2149577053)
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x00000000001da041(1941569)                     0x00000000001da041(1941569)                     
gp(x3)              0x00000000000000e8(232)                         0x00000000000000e8(232)                         
tp(x4)              0xffffffffc2a7d000(18446744072680361984)        0xffffffffc2a7d000(18446744072680361984)        
t0(x5)              0xfffffffea2949884(18446744067847264388)        0xfffffffea2949884(18446744067847264388)        
t1(x6)              0xffffffff7ffff99f(18446744071562066335)        0xffffffff7ffff99f(18446744071562066335)        
t2(x7)              0x000000008017fdc2(2149055938)                  0x000000008017fdc2(2149055938)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x00000000801ff15d(2149577053)                  0x00000000801ff15d(2149577053)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x0000000080180f62(2149060450)                  0x0000000080180f62(2149060450)                  
a3(x13)             0x000000000000005a(90)                          0x000000000000005a(90)                          
a4(x14)             0x0000000000000809(2057)                        0x0000000000000809(2057)                        
a5(x15)             0x000000008018068d(2149058189)                  0x000000008018068d(2149058189)                  
a6(x16)             0x000000000002a02e(172078)                      0x000000000002a02e(172078)                      
a7(x17)             0x0000000023fc0738(603719480)                   0x0000000023fc0738(603719480)                   
s2(x18)             0x0000000080180483(2149057667)                  0x0000000080180483(2149057667)                  
s3(x19)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
s4(x20)             0xffffffff84e2d000(18446744071644041216)        0xffffffff84e2d000(18446744071644041216)        
s5(x21)             0x000000007ffffee9(2147483369)                  0x000000007ffffee9(2147483369)                  
s6(x22)             0x00000000801da0cd(2149425357)                  0x00000000801da0cd(2149425357)                  
s7(x23)             0x00000000801e4cb1(2149469361)                  0x00000000801e4cb1(2149469361)                  
s8(x24)             0x0000000080000661(2147485281)                  0x0000000080000661(2147485281)                  
s9(x25)             0x000000008017f92f(2149054767)                  0x000000008017f92f(2149054767)                  
s10(x26)            0x00000000e24e377c(3796776828)                  0x00000000e24e377c(3796776828)                  
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x000000008017fa21(2149055009)                  0x000000008017fa21(2149055009)                  
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x000000001758974c(391681868)                   0x000000001758974c(391681868)                   
t6(x31)             0x00000000000000db(219)                         0x00000000000000db(219)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            9210ee3d84f3d22f6856f8a48a14a861396f9c4d        9210ee3d84f3d22f6856f8a48a14a861396f9c4d        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ad65a972b7aac824b7c5b0acd40e486f3245e170        X
lastPC              0x0000000080000748(2147485512)                  0x0000000080000748(2147485512)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000c8(200)                         0x00000000000000c8(200)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff4efffffe(2147483392.0_s)              0xffffffff4efffffe(2147483392.0_s)              
f3                  0x0000000000000001(5e-324_d)                    0x0000000000000001(5e-324_d)                    
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff4f0017f4(2149053440.0_s)              0xffffffff4f0017f4(2149053440.0_s)              
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff8000000b(-1.5414283107572988e-44_s)   0xffffffff8000000b(-1.5414283107572988e-44_s)   
f22                 0x000000007fffff0f(1.0609977764e-314_d)         0x000000007fffff0f(1.0609977764e-314_d)         
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

# FailID_001012 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1012
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x1a,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f26:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f28:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
_reg_f29:.byte 0xfe,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x64
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x1ffc00000           // ra
    li x2, 0x6000                // sp
    li x3, 0xe5                  // gp
    li x4, 0x8017fcd1            // tp
    li x5, 0x0                   // t0
    li x6, 0x8019d8f5            // t1
    li x7, 0x0                   // t2
    li x8, 0x8017fcc9            // fp
    li x9, 0x7ff                 // s1
    li x10, 0x8017fafa           // a0
    li x11, 0x180000000          // a1
    li x12, 0x0                  // a2
    li x13, 0x0                  // a3
    li x14, 0x6000               // a4
    li x15, 0x400c00             // a5
    li x16, 0x801fff29           // a6
    li x17, 0x7fffffb4           // a7
    li x18, 0x801fffab           // s2
    li x19, 0x43                 // s3
    li x20, 0x80180727           // s4
    li x21, 0x0                  // s5
    li x22, 0x8017fa9b           // s6
    li x23, 0xc6                 // s7
    li x24, 0x8019b1b6           // s8
    li x25, 0x8018054c           // s9
    li x26, 0x8017f85e           // s10
    li x27, 0x77                 // s11
    li x28, 0x0                  // t3
    li x29, 0x0                  // t4
    li x30, 0x80180727           // t5
    li x31, 0x800065c6           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x12', 'mstatus.fs/vs.fs'}, 'clob': {'x12', 'f18', 'x28'}})
    
    li x28, 0x1ffff8
    and x12, x12, x28
    li x28, 0x8000027a
    add x12, x12, x28
    fld f18, -0x27a(x12)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f18                 0xffffffff00000000(0.0_s)                       0x000000132140006f(4.05935308646e-313_d)        X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f18, -0x27a(x12)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f18                 0xffffffff00000000(0.0_s)                       0x000000132140006f(4.05935308646e-313_d)        X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f18, x27, x12
a2(x12)             0x000000008000027a(2147484282)                  0x000000008000027a(2147484282)
s11(x27)            0x0000000000000077(119)                         0x0000000000000077(119)
f18                 0xffffffff00000000(0.0_s)                       0x000000132140006f(4.05935308646e-313_d)        X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000001ffc00000(8585740288)                  0x00000001ffc00000(8585740288)                  
sp(x2)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
gp(x3)              0x00000000000000e5(229)                         0x00000000000000e5(229)                         
tp(x4)              0x000000008017fcd1(2149055697)                  0x000000008017fcd1(2149055697)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x000000008019d8f5(2149177589)                  0x000000008019d8f5(2149177589)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x000000008017fcc9(2149055689)                  0x000000008017fcc9(2149055689)                  
s1(x9)              0x00000000000007ff(2047)                        0x00000000000007ff(2047)                        
a0(x10)             0x000000008017fafa(2149055226)                  0x000000008017fafa(2149055226)                  
a1(x11)             0x0000000180000000(6442450944)                  0x0000000180000000(6442450944)                  
a2(x12)             0x000000008000027a(2147484282)                  0x000000008000027a(2147484282)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x0000000000400c00(4197376)                     0x0000000000400c00(4197376)                     
a6(x16)             0x00000000801fff29(2149580585)                  0x00000000801fff29(2149580585)                  
a7(x17)             0x000000007fffffb4(2147483572)                  0x000000007fffffb4(2147483572)                  
s2(x18)             0x00000000801fffab(2149580715)                  0x00000000801fffab(2149580715)                  
s3(x19)             0x0000000000000043(67)                          0x0000000000000043(67)                          
s4(x20)             0x0000000080180727(2149058343)                  0x0000000080180727(2149058343)                  
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x000000008017fa9b(2149055131)                  0x000000008017fa9b(2149055131)                  
s7(x23)             0x00000000000000c6(198)                         0x00000000000000c6(198)                         
s8(x24)             0x000000008019b1b6(2149167542)                  0x000000008019b1b6(2149167542)                  
s9(x25)             0x000000008018054c(2149057868)                  0x000000008018054c(2149057868)                  
s10(x26)            0x000000008017f85e(2149054558)                  0x000000008017f85e(2149054558)                  
s11(x27)            0x0000000000000077(119)                         0x0000000000000077(119)                         
t3(x28)             0x000000008000027a(2147484282)                  0x000000008000027a(2147484282)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x0000000080180727(2149058343)                  0x0000000080180727(2149058343)                  
t6(x31)             0x00000000800065c6(2147509702)                  0x00000000800065c6(2147509702)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            b26729b5f6946444ea1296a8033f29e39d148c1d        b26729b5f6946444ea1296a8033f29e39d148c1d        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000064(100)                         0x0000000000000064(100)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff0000001a(3.6433760072445244e-44_s)    0xffffffff0000001a(3.6433760072445244e-44_s)    
f3                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f10                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff00000000(0.0_s)                       0x000000132140006f(4.05935308646e-313_d)        X
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f21                 0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f25                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f26                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f27                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f28                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f29                 0xffffffff4efffffe(2147483392.0_s)              0xffffffff4efffffe(2147483392.0_s)              
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

# FailID_001605 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1605
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xf0,0xe0,0xc2,0x41
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0xfc,0xff,0xff,0xce,0xff,0xff,0xff,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xfc,0xff,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xe0,0xaf,0xff,0x03,0xe0,0x41
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x24,0xfb,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x22
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7ffffcd2            // ra
    li x2, 0x7ffffcf1            // sp
    li x3, 0x8017f947            // gp
    li x4, 0x8017f947            // tp
    li x5, 0x27                  // t0
    li x6, 0x7ffffcf1            // t1
    li x7, 0x7ffffa1c            // t2
    li x8, 0x0                   // fp
    li x9, 0x2005fe2300000000    // s1
    li x10, 0x6000               // a0
    li x11, 0x0                  // a1
    li x12, 0x8017fd3e           // a2
    li x13, 0x8027f850           // a3
    li x14, 0x7ffffbb3           // a4
    li x15, 0xce58000            // a5
    li x16, 0x1                  // a6
    li x17, 0x5d                 // a7
    li x18, 0x801807a7           // s2
    li x19, 0x8017f88c           // s3
    li x20, 0x340191f3           // s4
    li x21, 0x80180732           // s5
    li x22, 0xd5                 // s6
    li x23, 0x80180144           // s7
    li x24, 0x0                  // s8
    li x25, 0x801ffcb7           // s9
    li x26, 0x71                 // s10
    li x27, 0x7a                 // s11
    li x28, 0x800004ab           // t3
    li x29, 0x80180731           // t4
    li x30, 0x8017fcd1           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x3'}, 'clob': {'x17', 'f28', 'x3'}})
    
    li x17, 0x1ffffc
    and x3, x3, x17
    li x17, 0x7ffffba9
    add x3, x3, x17
    flw f28, 0x457(x3)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f28                 0x4080000000000000(512.0_d)                     0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f28, 0x457(x3)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f28                 0x4080000000000000(512.0_d)                     0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f28, x457, x3
gp(x3)              0x000000008017f4ed(2149053677)                  0x000000008017f4ed(2149053677)
f28                 0x4080000000000000(512.0_d)                     0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffffcd2(2147482834)                  0x000000007ffffcd2(2147482834)                  
sp(x2)              0x000000007ffffcf1(2147482865)                  0x000000007ffffcf1(2147482865)                  
gp(x3)              0x000000008017f4ed(2149053677)                  0x000000008017f4ed(2149053677)                  
tp(x4)              0x000000008017f947(2149054791)                  0x000000008017f947(2149054791)                  
t0(x5)              0x0000000000000027(39)                          0x0000000000000027(39)                          
t1(x6)              0x000000007ffffcf1(2147482865)                  0x000000007ffffcf1(2147482865)                  
t2(x7)              0x000000007ffffa1c(2147482140)                  0x000000007ffffa1c(2147482140)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x2005fe2300000000(2307529810374557696)         0x2005fe2300000000(2307529810374557696)         
a0(x10)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x000000008017fd3e(2149055806)                  0x000000008017fd3e(2149055806)                  
a3(x13)             0x000000008027f850(2150103120)                  0x000000008027f850(2150103120)                  
a4(x14)             0x000000007ffffbb3(2147482547)                  0x000000007ffffbb3(2147482547)                  
a5(x15)             0x000000000ce58000(216367104)                   0x000000000ce58000(216367104)                   
a6(x16)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a7(x17)             0x000000007ffffba9(2147482537)                  0x000000007ffffba9(2147482537)                  
s2(x18)             0x00000000801807a7(2149058471)                  0x00000000801807a7(2149058471)                  
s3(x19)             0x000000008017f88c(2149054604)                  0x000000008017f88c(2149054604)                  
s4(x20)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
s5(x21)             0x0000000080180732(2149058354)                  0x0000000080180732(2149058354)                  
s6(x22)             0x00000000000000d5(213)                         0x00000000000000d5(213)                         
s7(x23)             0x0000000080180144(2149056836)                  0x0000000080180144(2149056836)                  
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x00000000801ffcb7(2149579959)                  0x00000000801ffcb7(2149579959)                  
s10(x26)            0x0000000000000071(113)                         0x0000000000000071(113)                         
s11(x27)            0x000000000000007a(122)                         0x000000000000007a(122)                         
t3(x28)             0x00000000800004ab(2147484843)                  0x00000000800004ab(2147484843)                  
t4(x29)             0x0000000080180731(2149058353)                  0x0000000080180731(2149058353)                  
t5(x30)             0x000000008017fcd1(2149055697)                  0x000000008017fcd1(2149055697)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            dff336c0c072be381f9784530d3508f2c4577c44        dff336c0c072be381f9784530d3508f2c4577c44        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000022(34)                          0x0000000000000022(34)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff4f0017fd(2149055744.0_s)              0xffffffff4f0017fd(2149055744.0_s)              
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff4f0017fd(2149055744.0_s)              0xffffffff4f0017fd(2149055744.0_s)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x41c2e0f000000000(633462784.0_d)               0x41c2e0f000000000(633462784.0_d)               
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7fffffffcefffffc(nan_d)                       0x7fffffffcefffffc(nan_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffffcefffffc(-2147483136.0_s)             0xffffffffcefffffc(-2147483136.0_s)             
f13                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f14                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f15                 0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x41e003ffafe00000(2149580159.0_d)              0x41e003ffafe00000(2149580159.0_d)              
f28                 0x4080000000000000(512.0_d)                     0xffffffff00000000(0.0_s)                       X
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff8017fb24(-2.202308692502169e-39_s)    0xffffffff8017fb24(-2.202308692502169e-39_s)    
f31                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
STATES DIFFER: True
```

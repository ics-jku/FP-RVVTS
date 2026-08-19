# FailID_003595 VP++ SF neg RV64 flh

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3595
* Isolated failing instruction: `flh`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x11,0x43,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f9: .byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0x41
_reg_f10:.byte 0x1b,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x04,0x43,0xff,0xff,0xff,0xff
_reg_f13:.byte 0xf2,0x04,0x35,0x47,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0xc1
_reg_f15:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x8e,0xb1,0xcc,0x4e,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0xe0,0xb5,0x44,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0xff,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0x41
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0xff,0xff,0xff,0xce,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x42
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80180626            // ra
    li x2, 0x3be8b000            // sp
    li x3, 0x7ffffd62            // gp
    li x4, 0x0                   // tp
    li x5, 0x8018634a            // t0
    li x6, 0x11524770            // t1
    li x7, 0x80000136            // t2
    li x8, 0x8020096d            // fp
    li x9, 0x7fffff52            // s1
    li x10, 0x7fc00000           // a0
    li x11, 0x8000018d           // a1
    li x12, 0x801ffef5           // a2
    li x13, 0x10                 // a3
    li x14, 0x7fffffffffffffff   // a4
    li x15, 0x8017fd42           // a5
    li x16, 0x40002              // a6
    li x17, 0x8017f897           // a7
    li x18, 0x8000018d           // s2
    li x19, 0x80180019           // s3
    li x20, 0x42                 // s4
    li x21, 0x8018052d           // s5
    li x22, 0x8018023f           // s6
    li x23, 0x80005d62           // s7
    li x24, 0x6000               // s8
    li x25, 0x20                 // s9
    li x26, 0x801ffd96           // s10
    li x27, 0xffffffff83f08000   // s11
    li x28, 0x8017fcab           // t3
    li x29, 0x8020050c           // t4
    li x30, 0x1                  // t5
    li x31, 0x4da8c774           // t6
    // INSTRUCTION ({'dep': {'x12', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'x12', 'f14', 'x8'}})
    
    li x8, 0x1ffffe
    and x12, x12, x8
    li x8, 0x7fffff8d
    add x12, x12, x8
    flh f14, 0x73(x12)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f14                 0xc1e0030003200000(-2149056537.0_d)             0xffffffffffff0000(0.0_h)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flh f14, 0x73(x12)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f14                 0xc1e0030003200000(-2149056537.0_d)             0xffffffffffff0000(0.0_h)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x73, x12
a2(x12)             0x00000000801ffe81(2149580417)                  0x00000000801ffe81(2149580417)
f14                 0xc1e0030003200000(-2149056537.0_d)             0xffffffffffff0000(0.0_h)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080180626(2149058086)                  0x0000000080180626(2149058086)                  
sp(x2)              0x000000003be8b000(1005105152)                  0x000000003be8b000(1005105152)                  
gp(x3)              0x000000007ffffd62(2147482978)                  0x000000007ffffd62(2147482978)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x000000008018634a(2149081930)                  0x000000008018634a(2149081930)                  
t1(x6)              0x0000000011524770(290604912)                   0x0000000011524770(290604912)                   
t2(x7)              0x0000000080000136(2147483958)                  0x0000000080000136(2147483958)                  
fp(x8)              0x000000007fffff8d(2147483533)                  0x000000007fffff8d(2147483533)                  
s1(x9)              0x000000007fffff52(2147483474)                  0x000000007fffff52(2147483474)                  
a0(x10)             0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
a1(x11)             0x000000008000018d(2147484045)                  0x000000008000018d(2147484045)                  
a2(x12)             0x00000000801ffe81(2149580417)                  0x00000000801ffe81(2149580417)                  
a3(x13)             0x0000000000000010(16)                          0x0000000000000010(16)                          
a4(x14)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
a5(x15)             0x000000008017fd42(2149055810)                  0x000000008017fd42(2149055810)                  
a6(x16)             0x0000000000040002(262146)                      0x0000000000040002(262146)                      
a7(x17)             0x000000008017f897(2149054615)                  0x000000008017f897(2149054615)                  
s2(x18)             0x000000008000018d(2147484045)                  0x000000008000018d(2147484045)                  
s3(x19)             0x0000000080180019(2149056537)                  0x0000000080180019(2149056537)                  
s4(x20)             0x0000000000000042(66)                          0x0000000000000042(66)                          
s5(x21)             0x000000008018052d(2149057837)                  0x000000008018052d(2149057837)                  
s6(x22)             0x000000008018023f(2149057087)                  0x000000008018023f(2149057087)                  
s7(x23)             0x0000000080005d62(2147507554)                  0x0000000080005d62(2147507554)                  
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x0000000000000020(32)                          0x0000000000000020(32)                          
s10(x26)            0x00000000801ffd96(2149580182)                  0x00000000801ffd96(2149580182)                  
s11(x27)            0xffffffff83f08000(18446744071628161024)        0xffffffff83f08000(18446744071628161024)        
t3(x28)             0x000000008017fcab(2149055659)                  0x000000008017fcab(2149055659)                  
t4(x29)             0x000000008020050c(2149582092)                  0x000000008020050c(2149582092)                  
t5(x30)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t6(x31)             0x000000004da8c774(1302906740)                  0x000000004da8c774(1302906740)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            a6b819a198d8b928f51171cb8934b5346c797ff3        a6b819a198d8b928f51171cb8934b5346c797ff3        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000754(2147485524)                  0x0000000080000754(2147485524)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000042(66)                          0x0000000000000042(66)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff43110000(145.0_s)                     0xffffffff43110000(145.0_s)                     
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f5                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f6                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f9                  0x41e0030003200000(2149056537.0_d)              0x41e0030003200000(2149056537.0_d)              
f10                 0x000000000000001b(1.33e-322_d)                 0x000000000000001b(1.33e-322_d)                 
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff43040000(132.0_s)                     0xffffffff43040000(132.0_s)                     
f13                 0xffffffff473504f2(46340.9453125_s)             0xffffffff473504f2(46340.9453125_s)             
f14                 0xc1e0030003200000(-2149056537.0_d)             0xffffffffffff0000(0.0_h)                       X
f15                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f16                 0xffffffff4eccb18e(1717094144.0_s)              0xffffffff4eccb18e(1717094144.0_s)              
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff44b5e000(1455.0_s)                    0xffffffff44b5e000(1455.0_s)                    
f19                 0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f20                 0xffffffff4effffff(2147483520.0_s)              0xffffffff4effffff(2147483520.0_s)              
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x41e0030003200000(2149056537.0_d)              0x41e0030003200000(2149056537.0_d)              
f28                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffffceffffff(-2147483520.0_s)             0xffffffffceffffff(-2147483520.0_s)             
STATES DIFFER: True
```

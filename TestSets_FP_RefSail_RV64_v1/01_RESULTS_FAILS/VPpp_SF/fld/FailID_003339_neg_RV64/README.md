# FailID_003339 VP++ SF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3339
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0x48,0x47,0xe3,0xe9,0x8f,0xad,0x05,0xe5
_reg_f1: .byte 0x00,0x00,0xe0,0x8e,0xd5,0x03,0xe0,0x41
_reg_f2: .byte 0xef,0x9d,0x11,0x89,0x0a,0x13,0x15,0x41
_reg_f3: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x81,0xcc,0x89,0xec,0xac,0x74,0x38,0x04
_reg_f7: .byte 0x2b,0x87,0xd2,0xab,0x9d,0xbb,0x10,0x6c
_reg_f8: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x1c,0xaf,0xcd,0xa8,0x30,0x6e,0x0a,0xfd
_reg_f10:.byte 0x4d,0xc2,0x2b,0x45,0x6c,0x01,0xa5,0x6a
_reg_f11:.byte 0x04,0xcd,0x72,0xd0,0xcf,0x04,0x34,0xc1
_reg_f12:.byte 0xe7,0x52,0x19,0x56,0x63,0xb7,0x4a,0xb9
_reg_f13:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f14:.byte 0xd3,0x64,0xd4,0x05,0xc7,0x7d,0x7c,0x12
_reg_f15:.byte 0x7f,0x64,0xda,0x61,0x32,0xd3,0xfb,0x03
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x6d,0xb4,0x88,0x69,0xc0,0xd8,0x6a,0x0f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x04,0xa2,0xa2,0xeb,0x53,0xb8,0x0d,0xbc
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x11,0x67,0xe5,0xbe,0x53,0x84,0xcf,0x0d
_reg_f27:.byte 0xcf,0x74,0xd5,0x63,0x6b,0x2c,0xbe,0x91
_reg_f28:.byte 0x1c,0xaf,0xcd,0xa8,0x30,0x6e,0x0a,0xfd
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0xca,0x13,0x93,0x38,0x51,0x0c,0x97,0xd6
_reg_f31:.byte 0x04,0xa2,0xa2,0xeb,0x53,0xb8,0x0d,0xbc
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x45
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xc000000000000000    // ra
    li x2, 0x7ffffc43            // sp
    li x3, 0x44                  // gp
    li x4, 0x801                 // tp
    li x5, 0x0                   // t0
    li x6, 0x93b0e99e2a85c9cd    // t1
    li x7, 0x8003ebe5            // t2
    li x8, 0x801e597a            // fp
    li x9, 0x1c0fa47d2cfa7e10    // s1
    li x10, 0x80000106           // a0
    li x11, 0x801fdbbc           // a1
    li x12, 0x0                  // a2
    li x13, 0x6000               // a3
    li x14, 0xf91af8ea26b91800   // a4
    li x15, 0xffffffff94e16000   // a5
    li x16, 0x6000011a           // a6
    li x17, 0x800002ba           // a7
    li x18, 0x0                  // s2
    li x19, 0xe2                 // s3
    li x20, 0x8018004c           // s4
    li x21, 0xffffffff801eac77   // s5
    li x22, 0x8000003c           // s6
    li x23, 0x8021735e           // s7
    li x24, 0x8017fe02           // s8
    li x25, 0xffffffffffffffff   // s9
    li x26, 0x6000               // s10
    li x27, 0x0                  // s11
    li x28, 0x0                  // t3
    li x29, 0xe00002ba           // t4
    li x30, 0x8017ffff           // t5
    li x31, 0x800003f5           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x13'}, 'clob': {'x13', 'f7', 'x7'}})
    
    li x7, 0x1ffff8
    and x13, x13, x7
    li x7, 0x8000046c
    add x13, x13, x7
    fld f7, -0x46c(x13)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f7                  0x6c10bb9dabd2872b(3.520687781263141e+212_d)    0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f7, -0x46c(x13)
+========================================================================================================================+
Attributes:  fcsr ['overflow', 'inexact'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f7                  0x6c10bb9dabd2872b(3.520687781263141e+212_d)    0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f7, x46, x13
a3(x13)             0x000000008000646c(2147509356)                  0x000000008000646c(2147509356)
f7                  0x6c10bb9dabd2872b(3.520687781263141e+212_d)    0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xc000000000000000(13835058055282163712)        0xc000000000000000(13835058055282163712)        
sp(x2)              0x000000007ffffc43(2147482691)                  0x000000007ffffc43(2147482691)                  
gp(x3)              0x0000000000000044(68)                          0x0000000000000044(68)                          
tp(x4)              0x0000000000000801(2049)                        0x0000000000000801(2049)                        
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x93b0e99e2a85c9cd(10642262785003997645)        0x93b0e99e2a85c9cd(10642262785003997645)        
t2(x7)              0x000000008000046c(2147484780)                  0x000000008000046c(2147484780)                  
fp(x8)              0x00000000801e597a(2149472634)                  0x00000000801e597a(2149472634)                  
s1(x9)              0x1c0fa47d2cfa7e10(2022015615245123088)         0x1c0fa47d2cfa7e10(2022015615245123088)         
a0(x10)             0x0000000080000106(2147483910)                  0x0000000080000106(2147483910)                  
a1(x11)             0x00000000801fdbbc(2149571516)                  0x00000000801fdbbc(2149571516)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x000000008000646c(2147509356)                  0x000000008000646c(2147509356)                  
a4(x14)             0xf91af8ea26b91800(17949932949394233344)        0xf91af8ea26b91800(17949932949394233344)        
a5(x15)             0xffffffff94e16000(18446744071912382464)        0xffffffff94e16000(18446744071912382464)        
a6(x16)             0x000000006000011a(1610613018)                  0x000000006000011a(1610613018)                  
a7(x17)             0x00000000800002ba(2147484346)                  0x00000000800002ba(2147484346)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x00000000000000e2(226)                         0x00000000000000e2(226)                         
s4(x20)             0x000000008018004c(2149056588)                  0x000000008018004c(2149056588)                  
s5(x21)             0xffffffff801eac77(18446744071564078199)        0xffffffff801eac77(18446744071564078199)        
s6(x22)             0x000000008000003c(2147483708)                  0x000000008000003c(2147483708)                  
s7(x23)             0x000000008021735e(2149675870)                  0x000000008021735e(2149675870)                  
s8(x24)             0x000000008017fe02(2149056002)                  0x000000008017fe02(2149056002)                  
s9(x25)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s10(x26)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x00000000e00002ba(3758097082)                  0x00000000e00002ba(3758097082)                  
t5(x30)             0x000000008017ffff(2149056511)                  0x000000008017ffff(2149056511)                  
t6(x31)             0x00000000800003f5(2147484661)                  0x00000000800003f5(2147484661)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            c3b560bf18e04e58041a69ab2948e8a523bb4481        c3b560bf18e04e58041a69ab2948e8a523bb4481        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000778(2147485560)                  0x0000000080000778(2147485560)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000045(69)                          0x0000000000000045(69)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  
f1                  0x41e003d58ee00000(2149493879.0_d)              0x41e003d58ee00000(2149493879.0_d)              
f2                  0x4115130a89119def(345282.63385626575_d)        0x4115130a89119def(345282.63385626575_d)        
f3                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x043874acec89cc81(2.50948954357864e-288_d)     0x043874acec89cc81(2.50948954357864e-288_d)     
f7                  0x6c10bb9dabd2872b(3.520687781263141e+212_d)    0x0000000000000000(0.0_d)                       X
f8                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f9                  0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  
f10                 0x6aa5016c452bc24d(5.268673489679908e+205_d)    0x6aa5016c452bc24d(5.268673489679908e+205_d)    
f11                 0xc13404cfd072cd04(-1311951.8142517218_d)       0xc13404cfd072cd04(-1311951.8142517218_d)       
f12                 0xb94ab763561952e7(-1.0290767353988184e-32_d)   0xb94ab763561952e7(-1.0290767353988184e-32_d)   
f13                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f14                 0x127c7dc705d464d3(1.2611179739675923e-219_d)   0x127c7dc705d464d3(1.2611179739675923e-219_d)   
f15                 0x03fbd33261da647f(1.784510707492511e-289_d)    0x03fbd33261da647f(1.784510707492511e-289_d)    
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f18                 0x0f6ad8c06988b46d(2.1108825482638558e-234_d)   0x0f6ad8c06988b46d(2.1108825482638558e-234_d)   
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xbc0db853eba2a204(-2.013907603808987e-19_d)    0xbc0db853eba2a204(-2.013907603808987e-19_d)    
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f26                 0x0dcf8453bee56711(3.6926405312250583e-242_d)   0x0dcf8453bee56711(3.6926405312250583e-242_d)   
f27                 0x91be2c6b63d574cf(-3.2606869983951326e-223_d)  0x91be2c6b63d574cf(-3.2606869983951326e-223_d)  
f28                 0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xd6970c51389313ca(-1.353236949152047e+109_d)   0xd6970c51389313ca(-1.353236949152047e+109_d)   
f31                 0xbc0db853eba2a204(-2.013907603808987e-19_d)    0xbc0db853eba2a204(-2.013907603808987e-19_d)    
STATES DIFFER: True
```

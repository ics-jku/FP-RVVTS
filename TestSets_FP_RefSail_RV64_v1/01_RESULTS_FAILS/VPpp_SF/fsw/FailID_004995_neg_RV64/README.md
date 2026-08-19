# FailID_004995 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4995
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x3f,0xb7,0x57,0x4f,0x25,0x9d,0xef,0x40
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0xe4,0x9c,0xc0
_reg_f5: .byte 0x00,0x00,0x00,0x65,0x2e,0xff,0xda,0x41
_reg_f6: .byte 0x00,0x00,0x00,0x30,0x4a,0xe0,0xd2,0xc1
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x45,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x7c,0x3b,0xef,0x41
_reg_f16:.byte 0x00,0x00,0x40,0xb3,0xfe,0xff,0xdf,0x41
_reg_f17:.byte 0xc7,0x72,0xed,0xec,0x26,0x82,0x15,0x44
_reg_f18:.byte 0x00,0xd7,0x9f,0x73,0x00,0x00,0x00,0x00
_reg_f19:.byte 0x00,0x00,0x40,0xb3,0xfe,0xff,0xdf,0x41
_reg_f20:.byte 0xfc,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x5c,0x00,0x03,0xe0,0xc1
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0xc0,0x86,0x00,0x00,0xe0,0x41
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x41
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x8017feea            // sp
    li x3, 0x8027deaa            // gp
    li x4, 0xffffffffd1670000    // tp
    li x5, 0x69a0c778            // t0
    li x6, 0x80205a1d            // t1
    li x7, 0x80000436            // t2
    li x8, 0x8020087e            // fp
    li x9, 0x802001de            // s1
    li x10, 0x800007d4           // a0
    li x11, 0x80185b91           // a1
    li x12, 0x8017f8c4           // a2
    li x13, 0x801801aa           // a3
    li x14, 0xa1ea5744           // a4
    li x15, 0x565127d4           // a5
    li x16, 0x6000               // a6
    li x17, 0x8017fa0a           // a7
    li x18, 0x801807bb           // s2
    li x19, 0x1                  // s3
    li x20, 0x10000086c0000      // s4
    li x21, 0x8017fdae           // s5
    li x22, 0x6000               // s6
    li x23, 0x801901a2           // s7
    li x24, 0x8020087e           // s8
    li x25, 0x55                 // s9
    li x26, 0xff                 // s10
    li x27, 0xb5                 // s11
    li x28, 0x1                  // t3
    li x29, 0x801807d8           // t4
    li x30, 0x7ffffeeb           // t5
    li x31, 0x802806a3           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f25', 'x3'}, 'clob': {'x17', 'x3'}})
    
    li x17, 0xffffc
    and x3, x3, x17
    li x17, 0x8017fd1a
    add x3, x3, x17
    fsw f25, 0x2e6(x3)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        db5826c295150146cf82ddd6239a348561ae8de1        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f25, 0x2e6(x3)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        db5826c295150146cf82ddd6239a348561ae8de1        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, x2, e6, x3
sp(x2)              0x000000008017feea(2149056234)                  0x000000008017feea(2149056234)
gp(x3)              0x00000000801fdbc2(2149571522)                  0x00000000801fdbc2(2149571522)
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x000000008017feea(2149056234)                  0x000000008017feea(2149056234)                  
gp(x3)              0x00000000801fdbc2(2149571522)                  0x00000000801fdbc2(2149571522)                  
tp(x4)              0xffffffffd1670000(18446744072927772672)        0xffffffffd1670000(18446744072927772672)        
t0(x5)              0x0000000069a0c778(1772144504)                  0x0000000069a0c778(1772144504)                  
t1(x6)              0x0000000080205a1d(2149603869)                  0x0000000080205a1d(2149603869)                  
t2(x7)              0x0000000080000436(2147484726)                  0x0000000080000436(2147484726)                  
fp(x8)              0x000000008020087e(2149582974)                  0x000000008020087e(2149582974)                  
s1(x9)              0x00000000802001de(2149581278)                  0x00000000802001de(2149581278)                  
a0(x10)             0x00000000800007d4(2147485652)                  0x00000000800007d4(2147485652)                  
a1(x11)             0x0000000080185b91(2149079953)                  0x0000000080185b91(2149079953)                  
a2(x12)             0x000000008017f8c4(2149054660)                  0x000000008017f8c4(2149054660)                  
a3(x13)             0x00000000801801aa(2149056938)                  0x00000000801801aa(2149056938)                  
a4(x14)             0x00000000a1ea5744(2716489540)                  0x00000000a1ea5744(2716489540)                  
a5(x15)             0x00000000565127d4(1448159188)                  0x00000000565127d4(1448159188)                  
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x000000008017fd1a(2149055770)                  0x000000008017fd1a(2149055770)                  
s2(x18)             0x00000000801807bb(2149058491)                  0x00000000801807bb(2149058491)                  
s3(x19)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s4(x20)             0x00010000086c0000(281475118006272)             0x00010000086c0000(281475118006272)             
s5(x21)             0x000000008017fdae(2149055918)                  0x000000008017fdae(2149055918)                  
s6(x22)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s7(x23)             0x00000000801901a2(2149122466)                  0x00000000801901a2(2149122466)                  
s8(x24)             0x000000008020087e(2149582974)                  0x000000008020087e(2149582974)                  
s9(x25)             0x0000000000000055(85)                          0x0000000000000055(85)                          
s10(x26)            0x00000000000000ff(255)                         0x00000000000000ff(255)                         
s11(x27)            0x00000000000000b5(181)                         0x00000000000000b5(181)                         
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x00000000801807d8(2149058520)                  0x00000000801807d8(2149058520)                  
t5(x30)             0x000000007ffffeeb(2147483371)                  0x000000007ffffeeb(2147483371)                  
t6(x31)             0x00000000802806a3(2150106787)                  0x00000000802806a3(2150106787)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            efe8615b7af34e30f29ed39f8ca90942ba29ea2c        efe8615b7af34e30f29ed39f8ca90942ba29ea2c        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        db5826c295150146cf82ddd6239a348561ae8de1        X
lastPC              0x0000000080000778(2147485560)                  0x0000000080000778(2147485560)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000041(65)                          0x0000000000000041(65)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x40ef9d254f57b73f(64745.16593538084_d)         0x40ef9d254f57b73f(64745.16593538084_d)         
f4                  0xc09ce40000000000(-1849.0_d)                   0xc09ce40000000000(-1849.0_d)                   
f5                  0x41daff2e65000000(1811724692.0_d)              0x41daff2e65000000(1811724692.0_d)              
f6                  0xc1d2e04a30000000(-1266755776.0_d)             0xc1d2e04a30000000(-1266755776.0_d)             
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0xffffffff45000000(2048.0_s)                    0xffffffff45000000(2048.0_s)                    
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f15                 0x41ef3b7c00000000(4191936512.0_d)              0x41ef3b7c00000000(4191936512.0_d)              
f16                 0x41dffffeb3400000(2147482317.0_d)              0x41dffffeb3400000(2147482317.0_d)              
f17                 0x44158226eced72c7(9.919001733163082e+19_d)     0x44158226eced72c7(9.919001733163082e+19_d)     
f18                 0x00000000739fd700(9.58415765e-315_d)           0x00000000739fd700(9.58415765e-315_d)           
f19                 0x41dffffeb3400000(2147482317.0_d)              0x41dffffeb3400000(2147482317.0_d)              
f20                 0xffffffff4f0017fc(2149055488.0_s)              0xffffffff4f0017fc(2149055488.0_s)              
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xc1e003005cc00000(-2149057254.0_d)             0xc1e003005cc00000(-2149057254.0_d)             
f27                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x41e0000086c00000(2147484726.0_d)              0x41e0000086c00000(2147484726.0_d)              
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

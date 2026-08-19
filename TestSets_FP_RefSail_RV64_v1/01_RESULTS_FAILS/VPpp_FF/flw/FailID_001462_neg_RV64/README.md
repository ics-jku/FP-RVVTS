# FailID_001462 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1462
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
_reg_f0: .byte 0xd8,0xb3,0x4e,0x63,0x9d,0x14,0x56,0x13
_reg_f1: .byte 0xd8,0xf1,0xa6,0x18,0xf3,0x75,0x2b,0xf2
_reg_f2: .byte 0x9f,0xdf,0xa3,0xdd,0xa1,0xde,0x43,0xe9
_reg_f3: .byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f4: .byte 0xbc,0xde,0x79,0xd7,0xb2,0x08,0x42,0x27
_reg_f5: .byte 0x17,0x0c,0xce,0x03,0x47,0xf0,0x69,0x6d
_reg_f6: .byte 0x75,0x1a,0xb8,0x44,0x85,0xd0,0x51,0x01
_reg_f7: .byte 0x5d,0x7f,0x74,0x54,0x68,0x31,0x06,0xa1
_reg_f8: .byte 0xc8,0xf3,0x86,0x34,0x2f,0x98,0x1b,0x5c
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x6f,0xcf,0x03,0xee,0xfd,0x37,0x49,0x37
_reg_f11:.byte 0xc9,0x66,0x4d,0xbe,0xaf,0xf5,0x37,0x8b
_reg_f12:.byte 0x45,0x4c,0xb8,0x50,0xcb,0x1e,0x79,0xaa
_reg_f13:.byte 0x82,0x61,0xcd,0xae,0x68,0x11,0x58,0x10
_reg_f14:.byte 0x9c,0x70,0x0e,0x39,0x16,0x9e,0xd4,0x70
_reg_f15:.byte 0xa3,0xa1,0x80,0x3e,0x30,0x13,0xc4,0xae
_reg_f16:.byte 0x1e,0x61,0xc5,0x9b,0x9b,0x63,0x54,0x73
_reg_f17:.byte 0xf8,0x3e,0xa7,0xcc,0x40,0x98,0x6d,0xa1
_reg_f18:.byte 0xc9,0x09,0xce,0xd3,0xff,0x42,0x88,0x3a
_reg_f19:.byte 0x00,0x00,0x00,0x65,0x2e,0xff,0xda,0x41
_reg_f20:.byte 0x46,0x22,0x89,0xec,0x16,0x00,0x68,0x83
_reg_f21:.byte 0x0e,0xaf,0xab,0x00,0xf8,0x1c,0x3f,0xde
_reg_f22:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x1b,0x6e,0x91,0x6d,0x38,0xbb,0xad,0xb6
_reg_f24:.byte 0xc7,0x72,0xed,0xec,0x26,0x82,0x15,0x44
_reg_f25:.byte 0x87,0x13,0x7a,0xe3,0xb6,0x4e,0x18,0xdb
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0xde,0x1a,0xb8,0x9d,0x44,0xb4,0x8d,0xaf
_reg_f28:.byte 0x4c,0x6b,0x6f,0x14,0x2a,0xfb,0x46,0xfd
_reg_f29:.byte 0xd7,0x5f,0xea,0x8c,0x15,0x2c,0x47,0x19
_reg_f30:.byte 0x2a,0xe0,0x55,0xc7,0x3e,0x22,0xae,0x36
_reg_f31:.byte 0x15,0xcb,0x6d,0xe0,0x4d,0x4c,0x61,0x68
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x30
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x1000f90ac           // ra
    li x2, 0x8011d86f            // sp
    li x3, 0x801f107b            // gp
    li x4, 0xf55c6f887b63fe7f    // tp
    li x5, 0x8027fe46            // t0
    li x6, 0x800f96eb            // t1
    li x7, 0x0                   // t2
    li x8, 0x0                   // fp
    li x9, 0xbca3cb92e8cc3130    // s1
    li x10, 0x72623f3015efebeb   // a0
    li x11, 0x7ffff9c1           // a1
    li x12, 0xf55c6f887b63f82c   // a2
    li x13, 0x0                  // a3
    li x14, 0x80000543           // a4
    li x15, 0xd                  // a5
    li x16, 0x8018042e           // a6
    li x17, 0x614                // a7
    li x18, 0xf7                 // s2
    li x19, 0x802001bd           // s3
    li x20, 0x80180105           // s4
    li x21, 0x801800b9           // s5
    li x22, 0xffffffffffffffff   // s6
    li x23, 0x80180606           // s7
    li x24, 0x18db16bcd44bb121   // s8
    li x25, 0x8bfd6e0708f9620    // s9
    li x26, 0x10030020           // s10
    li x27, 0x4c                 // s11
    li x28, 0xca42bae7eba8b805   // t3
    li x29, 0x6000               // t4
    li x30, 0x7ffffea8           // t5
    li x31, 0xffffffff86ab2000   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x6'}, 'clob': {'x2', 'f1', 'x6'}})
    
    li x2, 0x1ffffc
    and x6, x6, x2
    li x2, 0x7ffffb05
    add x6, x6, x2
    flw f1, 0x4fb(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f1                  0xf22b75f318a6f1d8(-9.15543073462667e+241_d)    0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f1, 0x4fb(x6)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f1                  0xf22b75f318a6f1d8(-9.15543073462667e+241_d)    0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f1, x4, x6
tp(x4)              0xf55c6f887b63fe7f(17680128869126110847)        0xf55c6f887b63fe7f(17680128869126110847)
t1(x6)              0x00000000800f91ed(2148504045)                  0x00000000800f91ed(2148504045)
f1                  0xf22b75f318a6f1d8(-9.15543073462667e+241_d)    0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000001000f90ac(4295987372)                  0x00000001000f90ac(4295987372)                  
sp(x2)              0x000000007ffffb05(2147482373)                  0x000000007ffffb05(2147482373)                  
gp(x3)              0x00000000801f107b(2149519483)                  0x00000000801f107b(2149519483)                  
tp(x4)              0xf55c6f887b63fe7f(17680128869126110847)        0xf55c6f887b63fe7f(17680128869126110847)        
t0(x5)              0x000000008027fe46(2150104646)                  0x000000008027fe46(2150104646)                  
t1(x6)              0x00000000800f91ed(2148504045)                  0x00000000800f91ed(2148504045)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0xbca3cb92e8cc3130(13592931932165648688)        0xbca3cb92e8cc3130(13592931932165648688)        
a0(x10)             0x72623f3015efebeb(8242219743800454123)         0x72623f3015efebeb(8242219743800454123)         
a1(x11)             0x000000007ffff9c1(2147482049)                  0x000000007ffff9c1(2147482049)                  
a2(x12)             0xf55c6f887b63f82c(17680128869126109228)        0xf55c6f887b63f82c(17680128869126109228)        
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x0000000080000543(2147484995)                  0x0000000080000543(2147484995)                  
a5(x15)             0x000000000000000d(13)                          0x000000000000000d(13)                          
a6(x16)             0x000000008018042e(2149057582)                  0x000000008018042e(2149057582)                  
a7(x17)             0x0000000000000614(1556)                        0x0000000000000614(1556)                        
s2(x18)             0x00000000000000f7(247)                         0x00000000000000f7(247)                         
s3(x19)             0x00000000802001bd(2149581245)                  0x00000000802001bd(2149581245)                  
s4(x20)             0x0000000080180105(2149056773)                  0x0000000080180105(2149056773)                  
s5(x21)             0x00000000801800b9(2149056697)                  0x00000000801800b9(2149056697)                  
s6(x22)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s7(x23)             0x0000000080180606(2149058054)                  0x0000000080180606(2149058054)                  
s8(x24)             0x18db16bcd44bb121(1791050277081297185)         0x18db16bcd44bb121(1791050277081297185)         
s9(x25)             0x08bfd6e0708f9620(630458732304635424)          0x08bfd6e0708f9620(630458732304635424)          
s10(x26)            0x0000000010030020(268632096)                   0x0000000010030020(268632096)                   
s11(x27)            0x000000000000004c(76)                          0x000000000000004c(76)                          
t3(x28)             0xca42bae7eba8b805(14574416849378260997)        0xca42bae7eba8b805(14574416849378260997)        
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x000000007ffffea8(2147483304)                  0x000000007ffffea8(2147483304)                  
t6(x31)             0xffffffff86ab2000(18446744071673946112)        0xffffffff86ab2000(18446744071673946112)        

STATE               REF                                             DUT                                             DIFF
xmemhash            5f17285d8c4abc19684b150c0ce4429b8185e0d0        5f17285d8c4abc19684b150c0ce4429b8185e0d0        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800007cc(2147485644)                  0x00000000800007cc(2147485644)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000030(48)                          0x0000000000000030(48)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x1356149d634eb3d8(1.6012993927683887e-215_d)   0x1356149d634eb3d8(1.6012993927683887e-215_d)   
f1                  0xf22b75f318a6f1d8(-9.15543073462667e+241_d)    0xffffffff00000000(0.0_s)                       X
f2                  0xe943dea1dda3df9f(-1.1882218372422584e+199_d)  0xe943dea1dda3df9f(-1.1882218372422584e+199_d)  
f3                  0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f4                  0x274208b2d779debc(1.3967648182202668e-119_d)   0x274208b2d779debc(1.3967648182202668e-119_d)   
f5                  0x6d69f04703ce0c17(1.1445456587158075e+219_d)   0x6d69f04703ce0c17(1.1445456587158075e+219_d)   
f6                  0x0151d08544b81a75(2.597758751576056e-302_d)    0x0151d08544b81a75(2.597758751576056e-302_d)    
f7                  0xa106316854747f5d(-1.3559639442016137e-149_d)  0xa106316854747f5d(-1.3559639442016137e-149_d)  
f8                  0x5c1b982f3486f3c8(5.014182396516635e+135_d)    0x5c1b982f3486f3c8(5.014182396516635e+135_d)    
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x374937fdee03cf6f(2.2616928883692246e-42_d)    0x374937fdee03cf6f(2.2616928883692246e-42_d)    
f11                 0x8b37f5afbe4d66c9(-1.2765719173115515e-254_d)  0x8b37f5afbe4d66c9(-1.2765719173115515e-254_d)  
f12                 0xaa791ecb50b84c45(-4.3811301511716665e-104_d)  0xaa791ecb50b84c45(-4.3811301511716665e-104_d)  
f13                 0x10581168aecd6182(6.201023666635093e-230_d)    0x10581168aecd6182(6.201023666635093e-230_d)    
f14                 0x70d49e16390e709c(3.277730104930821e+235_d)    0x70d49e16390e709c(3.277730104930821e+235_d)    
f15                 0xaec413303e80a1a3(-2.0667397287977667e-83_d)   0xaec413303e80a1a3(-2.0667397287977667e-83_d)   
f16                 0x7354639b9bc5611e(3.5639726539380704e+247_d)   0x7354639b9bc5611e(3.5639726539380704e+247_d)   
f17                 0xa16d9840cca73ef8(-1.1572485581900932e-147_d)  0xa16d9840cca73ef8(-1.1572485581900932e-147_d)  
f18                 0x3a8842ffd3ce09c9(9.799229100695556e-27_d)     0x3a8842ffd3ce09c9(9.799229100695556e-27_d)     
f19                 0x41daff2e65000000(1811724692.0_d)              0x41daff2e65000000(1811724692.0_d)              
f20                 0x83680016ec892246(-3.0062963551402056e-292_d)  0x83680016ec892246(-3.0062963551402056e-292_d)  
f21                 0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    
f22                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f23                 0xb6adbb386d916e1b(-2.603904172073479e-45_d)    0xb6adbb386d916e1b(-2.603904172073479e-45_d)    
f24                 0x44158226eced72c7(9.919001733163082e+19_d)     0x44158226eced72c7(9.919001733163082e+19_d)     
f25                 0xdb184eb6e37a1387(-6.739660802998555e+130_d)   0xdb184eb6e37a1387(-6.739660802998555e+130_d)   
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xaf8db4449db81ade(-1.252589043789733e-79_d)    0xaf8db4449db81ade(-1.252589043789733e-79_d)    
f28                 0xfd46fb2a146f6b4c(-2.935464151470059e+295_d)   0xfd46fb2a146f6b4c(-2.935464151470059e+295_d)   
f29                 0x19472c158cea5fd7(6.657022754819872e-187_d)    0x19472c158cea5fd7(6.657022754819872e-187_d)    
f30                 0x36ae223ec755e02a(2.639150388912977e-45_d)     0x36ae223ec755e02a(2.639150388912977e-45_d)     
f31                 0x68614c4de06dcb15(6.31371092986251e+194_d)     0x68614c4de06dcb15(6.31371092986251e+194_d)     
STATES DIFFER: True
```

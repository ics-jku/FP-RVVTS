# FailID_002365 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2365
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
_reg_f0: .byte 0xd8,0xb3,0x4e,0x63,0x9d,0x14,0x56,0x13
_reg_f1: .byte 0xd8,0xf1,0xa6,0x18,0xf3,0x75,0x2b,0xf2
_reg_f2: .byte 0x9f,0xdf,0xa3,0xdd,0xa1,0xde,0x43,0xe9
_reg_f3: .byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f4: .byte 0xbc,0xde,0x79,0xd7,0xb2,0x08,0x42,0x27
_reg_f5: .byte 0xc8,0xf3,0x86,0x34,0x2f,0x98,0x1b,0x5c
_reg_f6: .byte 0x13,0x6b,0xe8,0x1f,0x8f,0x30,0x49,0x37
_reg_f7: .byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f8: .byte 0xc8,0xf3,0x86,0x34,0x2f,0x98,0x1b,0x5c
_reg_f9: .byte 0xd0,0xa9,0xf2,0x4e,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x82,0x13,0x80,0xe0,0xfc,0xff,0xcf,0xc3
_reg_f11:.byte 0xc9,0x66,0x4d,0xbe,0xaf,0xf5,0x37,0x8b
_reg_f12:.byte 0x45,0x4c,0xb8,0x50,0xcb,0x1e,0x79,0xaa
_reg_f13:.byte 0x82,0x61,0xcd,0xae,0x68,0x11,0x58,0x10
_reg_f14:.byte 0x9c,0x70,0x0e,0x39,0x16,0x9e,0xd4,0x70
_reg_f15:.byte 0xa3,0xa1,0x80,0x3e,0x30,0x13,0xc4,0xae
_reg_f16:.byte 0x1e,0x61,0xc5,0x9b,0x9b,0x63,0x54,0x73
_reg_f17:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0xc9,0x09,0xce,0xd3,0xff,0x42,0x88,0x3a
_reg_f19:.byte 0x00,0x00,0x00,0x65,0x2e,0xff,0xda,0x41
_reg_f20:.byte 0x9b,0x70,0x0e,0x39,0x16,0x9e,0xd4,0x70
_reg_f21:.byte 0x0e,0xaf,0xab,0x00,0xf8,0x1c,0x3f,0xde
_reg_f22:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0xc7,0x72,0xed,0xec,0x26,0x82,0x15,0x44
_reg_f25:.byte 0x87,0x13,0x7a,0xe3,0xb6,0x4e,0x18,0xdb
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0xde,0x1a,0xb8,0x9d,0x44,0xb4,0x8d,0xaf
_reg_f28:.byte 0x4c,0x6b,0x6f,0x14,0x2a,0xfb,0x46,0xfd
_reg_f29:.byte 0xd7,0x5f,0xea,0x8c,0x15,0x2c,0x47,0x19
_reg_f30:.byte 0x2a,0xe0,0x55,0xc7,0x3e,0x22,0xae,0x36
_reg_f31:.byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'res0(0b101)', 'res': 0}
    li t0, 0xa2
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x1000f90ac           // ra
    li x2, 0x7954e826            // sp
    li x3, 0x801ffd5c            // gp
    li x4, 0x9f                  // tp
    li x5, 0x8007f880            // t0
    li x6, 0x0                   // t1
    li x7, 0x801800d2            // t2
    li x8, 0xa2                  // fp
    li x9, 0x75                  // s1
    li x10, 0x3ffffce080000000   // a0
    li x11, 0x7ffff9c1           // a1
    li x12, 0xffffffffd3ce09c9   // a2
    li x13, 0x8017fffd           // a3
    li x14, 0x7ffff89f           // a4
    li x15, 0xffffffff8ca1e000   // a5
    li x16, 0x6000               // a6
    li x17, 0x0                  // a7
    li x18, 0x0                  // s2
    li x19, 0x8017f9de           // s3
    li x20, 0x7954e826           // s4
    li x21, 0x3ffffce08000009f   // s5
    li x22, 0x5e3                // s6
    li x23, 0xffffffffde776000   // s7
    li x24, 0x8023a667           // s8
    li x25, 0x0                  // s9
    li x26, 0xe7                 // s10
    li x27, 0x6000               // s11
    li x28, 0xe2                 // t3
    li x29, 0x1                  // t4
    li x30, 0x10000              // t5
    li x31, 0xffffffffffffffff   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x17', 'f18'}, 'clob': {'x16', 'x17'}})
    
    li x16, 0xffffc
    and x17, x17, x16
    li x16, 0x8017fe75
    add x17, x17, x16
    fsw f18, 0x18b(x17)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        80287d30872811e4258864aae8e276fc6d0b7ff2        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f18, 0x18b(x17)
+========================================================================================================================+
Attributes:  fcsr ['underflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        80287d30872811e4258864aae8e276fc6d0b7ff2        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f18, x18, x17
a7(x17)             0x000000008017fe75(2149056117)                  0x000000008017fe75(2149056117)
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)
f18                 0x3a8842ffd3ce09c9(9.799229100695556e-27_d)     0x3a8842ffd3ce09c9(9.799229100695556e-27_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000001000f90ac(4295987372)                  0x00000001000f90ac(4295987372)                  
sp(x2)              0x000000007954e826(2035607590)                  0x000000007954e826(2035607590)                  
gp(x3)              0x00000000801ffd5c(2149580124)                  0x00000000801ffd5c(2149580124)                  
tp(x4)              0x000000000000009f(159)                         0x000000000000009f(159)                         
t0(x5)              0x000000008007f880(2148006016)                  0x000000008007f880(2148006016)                  
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x00000000801800d2(2149056722)                  0x00000000801800d2(2149056722)                  
fp(x8)              0x00000000000000a2(162)                         0x00000000000000a2(162)                         
s1(x9)              0x0000000000000075(117)                         0x0000000000000075(117)                         
a0(x10)             0x3ffffce080000000(4611682584601034752)         0x3ffffce080000000(4611682584601034752)         
a1(x11)             0x000000007ffff9c1(2147482049)                  0x000000007ffff9c1(2147482049)                  
a2(x12)             0xffffffffd3ce09c9(18446744072968079817)        0xffffffffd3ce09c9(18446744072968079817)        
a3(x13)             0x000000008017fffd(2149056509)                  0x000000008017fffd(2149056509)                  
a4(x14)             0x000000007ffff89f(2147481759)                  0x000000007ffff89f(2147481759)                  
a5(x15)             0xffffffff8ca1e000(18446744071774003200)        0xffffffff8ca1e000(18446744071774003200)        
a6(x16)             0x000000008017fe75(2149056117)                  0x000000008017fe75(2149056117)                  
a7(x17)             0x000000008017fe75(2149056117)                  0x000000008017fe75(2149056117)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000008017f9de(2149054942)                  0x000000008017f9de(2149054942)                  
s4(x20)             0x000000007954e826(2035607590)                  0x000000007954e826(2035607590)                  
s5(x21)             0x3ffffce08000009f(4611682584601034911)         0x3ffffce08000009f(4611682584601034911)         
s6(x22)             0x00000000000005e3(1507)                        0x00000000000005e3(1507)                        
s7(x23)             0xffffffffde776000(18446744073146949632)        0xffffffffde776000(18446744073146949632)        
s8(x24)             0x000000008023a667(2149820007)                  0x000000008023a667(2149820007)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x00000000000000e7(231)                         0x00000000000000e7(231)                         
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x00000000000000e2(226)                         0x00000000000000e2(226)                         
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x0000000000010000(65536)                       0x0000000000010000(65536)                       
t6(x31)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        

STATE               REF                                             DUT                                             DIFF
xmemhash            eee4fbc58211b8f1beb04c16138911ff12f049bd        eee4fbc58211b8f1beb04c16138911ff12f049bd        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        80287d30872811e4258864aae8e276fc6d0b7ff2        X
lastPC              0x0000000080000710(2147485456)                  0x0000000080000710(2147485456)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000a2(162)                         0x00000000000000a2(162)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            res0(0b101)                                     res0(0b101)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x1356149d634eb3d8(1.6012993927683887e-215_d)   0x1356149d634eb3d8(1.6012993927683887e-215_d)   
f1                  0xf22b75f318a6f1d8(-9.15543073462667e+241_d)    0xf22b75f318a6f1d8(-9.15543073462667e+241_d)    
f2                  0xe943dea1dda3df9f(-1.1882218372422584e+199_d)  0xe943dea1dda3df9f(-1.1882218372422584e+199_d)  
f3                  0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f4                  0x274208b2d779debc(1.3967648182202668e-119_d)   0x274208b2d779debc(1.3967648182202668e-119_d)   
f5                  0x5c1b982f3486f3c8(5.014182396516635e+135_d)    0x5c1b982f3486f3c8(5.014182396516635e+135_d)    
f6                  0x3749308f1fe86b13(2.259088984197151e-42_d)     0x3749308f1fe86b13(2.259088984197151e-42_d)     
f7                  0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f8                  0x5c1b982f3486f3c8(5.014182396516635e+135_d)    0x5c1b982f3486f3c8(5.014182396516635e+135_d)    
f9                  0xffffffff4ef2a9d0(2035607552.0_s)              0xffffffff4ef2a9d0(2035607552.0_s)              
f10                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0xc3cffffce0801382(-4.6116791507772385e+18_d)   
f11                 0x8b37f5afbe4d66c9(-1.2765719173115515e-254_d)  0x8b37f5afbe4d66c9(-1.2765719173115515e-254_d)  
f12                 0xaa791ecb50b84c45(-4.3811301511716665e-104_d)  0xaa791ecb50b84c45(-4.3811301511716665e-104_d)  
f13                 0x10581168aecd6182(6.201023666635093e-230_d)    0x10581168aecd6182(6.201023666635093e-230_d)    
f14                 0x70d49e16390e709c(3.277730104930821e+235_d)    0x70d49e16390e709c(3.277730104930821e+235_d)    
f15                 0xaec413303e80a1a3(-2.0667397287977667e-83_d)   0xaec413303e80a1a3(-2.0667397287977667e-83_d)   
f16                 0x7354639b9bc5611e(3.5639726539380704e+247_d)   0x7354639b9bc5611e(3.5639726539380704e+247_d)   
f17                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f18                 0x3a8842ffd3ce09c9(9.799229100695556e-27_d)     0x3a8842ffd3ce09c9(9.799229100695556e-27_d)     
f19                 0x41daff2e65000000(1811724692.0_d)              0x41daff2e65000000(1811724692.0_d)              
f20                 0x70d49e16390e709b(3.2777301049308207e+235_d)   0x70d49e16390e709b(3.2777301049308207e+235_d)   
f21                 0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    
f22                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f23                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f24                 0x44158226eced72c7(9.919001733163082e+19_d)     0x44158226eced72c7(9.919001733163082e+19_d)     
f25                 0xdb184eb6e37a1387(-6.739660802998555e+130_d)   0xdb184eb6e37a1387(-6.739660802998555e+130_d)   
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xaf8db4449db81ade(-1.252589043789733e-79_d)    0xaf8db4449db81ade(-1.252589043789733e-79_d)    
f28                 0xfd46fb2a146f6b4c(-2.935464151470059e+295_d)   0xfd46fb2a146f6b4c(-2.935464151470059e+295_d)   
f29                 0x19472c158cea5fd7(6.657022754819872e-187_d)    0x19472c158cea5fd7(6.657022754819872e-187_d)    
f30                 0x36ae223ec755e02a(2.639150388912977e-45_d)     0x36ae223ec755e02a(2.639150388912977e-45_d)     
f31                 0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
STATES DIFFER: True
```

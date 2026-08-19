# FailID_000939 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 939
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
_reg_f0: .byte 0xd8,0xb3,0x4e,0x63,0x9d,0x14,0x56,0x13
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x9f,0xdf,0xa3,0xdd,0xa1,0xde,0x43,0xe9
_reg_f3: .byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x13,0x6b,0xe8,0x1f,0x8f,0x30,0x49,0x37
_reg_f7: .byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x82,0x13,0x80,0xe0,0xfc,0xff,0xcf,0xc3
_reg_f11:.byte 0xc9,0x66,0x4d,0xbe,0xaf,0xf5,0x37,0x8b
_reg_f12:.byte 0x00,0x00,0xc0,0x5c,0x00,0x03,0xe0,0x41
_reg_f13:.byte 0x82,0x13,0x80,0xe0,0xfc,0xff,0xcf,0xc3
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x0b,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x1e,0x61,0xc5,0x9b,0x9b,0x63,0x54,0x73
_reg_f17:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0xc9,0x09,0xce,0xd3,0xff,0x42,0x88,0x3a
_reg_f19:.byte 0x00,0x00,0x00,0x65,0x2e,0xff,0xda,0x41
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x0e,0xaf,0xab,0x00,0xf8,0x1c,0x3f,0xde
_reg_f22:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0xc7,0x72,0xed,0xec,0x26,0x82,0x15,0x44
_reg_f25:.byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x87,0x6d,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0xaf,0x1c,0xc2,0xc3,0x53,0x40,0x35,0x39
_reg_f30:.byte 0x00,0x00,0x1f,0x43,0xff,0xff,0xff,0xff
_reg_f31:.byte 0xc8,0xf3,0x86,0x34,0x2f,0x98,0x1b,0x5c
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
    li x1, 0x8027fcd9            // ra
    li x2, 0x802003ae            // sp
    li x3, 0xffffffff945e4000    // gp
    li x4, 0x400003a700000000    // tp
    li x5, 0x80001296            // t0
    li x6, 0x8017f931            // t1
    li x7, 0x6000                // t2
    li x8, 0x60                  // fp
    li x9, 0x8018059e            // s1
    li x10, 0x80000106           // a0
    li x11, 0x2fb84916           // a1
    li x12, 0xc000000            // a2
    li x13, 0x800001c1           // a3
    li x14, 0x0                  // a4
    li x15, 0x7ffffe7e           // a5
    li x16, 0x800000cd           // a6
    li x17, 0x8017fc30           // a7
    li x18, 0xffffffff7fe806ea   // s2
    li x19, 0x0                  // s3
    li x20, 0x8017f930           // s4
    li x21, 0x0                  // s5
    li x22, 0x801ff84e           // s6
    li x23, 0x8017fbee           // s7
    li x24, 0x8017fede           // s8
    li x25, 0xffffffffe6380000   // s9
    li x26, 0x8018037b           // s10
    li x27, 0x80000cf0           // s11
    li x28, 0x7ffffddc           // t3
    li x29, 0x8020074a           // t4
    li x30, 0x7                  // t5
    li x31, 0x8000c36e           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x18'}, 'clob': {'f13', 'x18', 'x25'}})
    
    li x25, 0x1ffff8
    and x18, x18, x25
    li x25, 0x80000586
    add x18, x18, x25
    fld f13, -0x586(x18)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f13, -0x586(x18)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x586, x18
s2(x18)             0x0000000080080c6e(2148011118)                  0x0000000080080c6e(2148011118)
f13                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008027fcd9(2150104281)                  0x000000008027fcd9(2150104281)                  
sp(x2)              0x00000000802003ae(2149581742)                  0x00000000802003ae(2149581742)                  
gp(x3)              0xffffffff945e4000(18446744071903789056)        0xffffffff945e4000(18446744071903789056)        
tp(x4)              0x400003a700000000(4611690034221809664)         0x400003a700000000(4611690034221809664)         
t0(x5)              0x0000000080001296(2147488406)                  0x0000000080001296(2147488406)                  
t1(x6)              0x000000008017f931(2149054769)                  0x000000008017f931(2149054769)                  
t2(x7)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
fp(x8)              0x0000000000000060(96)                          0x0000000000000060(96)                          
s1(x9)              0x000000008018059e(2149057950)                  0x000000008018059e(2149057950)                  
a0(x10)             0x0000000080000106(2147483910)                  0x0000000080000106(2147483910)                  
a1(x11)             0x000000002fb84916(800606486)                   0x000000002fb84916(800606486)                   
a2(x12)             0x000000000c000000(201326592)                   0x000000000c000000(201326592)                   
a3(x13)             0x00000000800001c1(2147484097)                  0x00000000800001c1(2147484097)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x000000007ffffe7e(2147483262)                  0x000000007ffffe7e(2147483262)                  
a6(x16)             0x00000000800000cd(2147483853)                  0x00000000800000cd(2147483853)                  
a7(x17)             0x000000008017fc30(2149055536)                  0x000000008017fc30(2149055536)                  
s2(x18)             0x0000000080080c6e(2148011118)                  0x0000000080080c6e(2148011118)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000008017f930(2149054768)                  0x000000008017f930(2149054768)                  
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x00000000801ff84e(2149578830)                  0x00000000801ff84e(2149578830)                  
s7(x23)             0x000000008017fbee(2149055470)                  0x000000008017fbee(2149055470)                  
s8(x24)             0x000000008017fede(2149056222)                  0x000000008017fede(2149056222)                  
s9(x25)             0x0000000080000586(2147485062)                  0x0000000080000586(2147485062)                  
s10(x26)            0x000000008018037b(2149057403)                  0x000000008018037b(2149057403)                  
s11(x27)            0x0000000080000cf0(2147486960)                  0x0000000080000cf0(2147486960)                  
t3(x28)             0x000000007ffffddc(2147483100)                  0x000000007ffffddc(2147483100)                  
t4(x29)             0x000000008020074a(2149582666)                  0x000000008020074a(2149582666)                  
t5(x30)             0x0000000000000007(7)                           0x0000000000000007(7)                           
t6(x31)             0x000000008000c36e(2147533678)                  0x000000008000c36e(2147533678)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            98c8f770006c7a3de17a9eb80e283d307d84bc22        98c8f770006c7a3de17a9eb80e283d307d84bc22        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000768(2147485544)                  0x0000000080000768(2147485544)                  
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
f0                  0x1356149d634eb3d8(1.6012993927683887e-215_d)   0x1356149d634eb3d8(1.6012993927683887e-215_d)   
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xe943dea1dda3df9f(-1.1882218372422584e+199_d)  0xe943dea1dda3df9f(-1.1882218372422584e+199_d)  
f3                  0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x3749308f1fe86b13(2.259088984197151e-42_d)     0x3749308f1fe86b13(2.259088984197151e-42_d)     
f7                  0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0xc3cffffce0801382(-4.6116791507772385e+18_d)   
f11                 0x8b37f5afbe4d66c9(-1.2765719173115515e-254_d)  0x8b37f5afbe4d66c9(-1.2765719173115515e-254_d)  
f12                 0x41e003005cc00000(2149057254.0_d)              0x41e003005cc00000(2149057254.0_d)              
f13                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0x0000000000000000(0.0_d)                       X
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff4f00180b(2149059328.0_s)              0xffffffff4f00180b(2149059328.0_s)              
f16                 0x7354639b9bc5611e(3.5639726539380704e+247_d)   0x7354639b9bc5611e(3.5639726539380704e+247_d)   
f17                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f18                 0x3a8842ffd3ce09c9(9.799229100695556e-27_d)     0x3a8842ffd3ce09c9(9.799229100695556e-27_d)     
f19                 0x41daff2e65000000(1811724692.0_d)              0x41daff2e65000000(1811724692.0_d)              
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    
f22                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f23                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f24                 0x44158226eced72c7(9.919001733163082e+19_d)     0x44158226eced72c7(9.919001733163082e+19_d)     
f25                 0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffffffff6d87(5660.0_h)                    0xffffffffffff6d87(5660.0_h)                    
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x39354053c3c21caf(4.092847294095176e-33_d)     0x39354053c3c21caf(4.092847294095176e-33_d)     
f30                 0xffffffff431f0000(159.0_s)                     0xffffffff431f0000(159.0_s)                     
f31                 0x5c1b982f3486f3c8(5.014182396516635e+135_d)    0x5c1b982f3486f3c8(5.014182396516635e+135_d)    
STATES DIFFER: True
```

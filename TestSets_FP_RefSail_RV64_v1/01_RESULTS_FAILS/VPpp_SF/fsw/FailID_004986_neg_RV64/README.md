# FailID_004986 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4986
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
_reg_f0: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x9f,0xdf,0xa3,0xdd,0xa1,0xde,0x43,0xe9
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x13,0x6b,0xe8,0x1f,0x8f,0x30,0x49,0x37
_reg_f7: .byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x82,0x13,0x80,0xe0,0xfc,0xff,0xcf,0xc3
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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
_reg_f27:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
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
    li x1, 0x0                   // ra
    li x2, 0x8017fbd9            // sp
    li x3, 0xffffffff945e4000    // gp
    li x4, 0x801805a2            // tp
    li x5, 0x7ffffce9            // t0
    li x6, 0x8017f8c9            // t1
    li x7, 0x8000060c            // t2
    li x8, 0x6000                // fp
    li x9, 0x1                   // s1
    li x10, 0x1                  // a0
    li x11, 0x80000c88           // a1
    li x12, 0x801805a2           // a2
    li x13, 0x4d                 // a3
    li x14, 0x8017fb02           // a4
    li x15, 0x7f                 // a5
    li x16, 0x801807a1           // a6
    li x17, 0x8017fb02           // a7
    li x18, 0x1                  // s2
    li x19, 0x41e0000000000000   // s3
    li x20, 0xddb5c770           // s4
    li x21, 0x85                 // s5
    li x22, 0x41e0               // s6
    li x23, 0x8017fef5           // s7
    li x24, 0xb5                 // s8
    li x25, 0x801bff11           // s9
    li x26, 0x1078               // s10
    li x27, 0x38                 // s11
    li x28, 0x8000662f           // t3
    li x29, 0x0                  // t4
    li x30, 0x7ffffc1e           // t5
    li x31, 0x8017fd51           // t6
    // INSTRUCTION ({'dep': {'f20', 'fcsr.rm', 'x25', 'mstatus.fs/vs.fs'}, 'clob': {'x10', 'x25'}})
    
    li x10, 0xffffc
    and x25, x25, x10
    li x10, 0x8017fc97
    add x25, x25, x10
    fsw f20, 0x369(x25)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f20, 0x369(x25)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f20, x369, x25
s9(x25)             0x000000008023fba7(2149841831)                  0x000000008023fba7(2149841831)
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x000000008017fbd9(2149055449)                  0x000000008017fbd9(2149055449)                  
gp(x3)              0xffffffff945e4000(18446744071903789056)        0xffffffff945e4000(18446744071903789056)        
tp(x4)              0x00000000801805a2(2149057954)                  0x00000000801805a2(2149057954)                  
t0(x5)              0x000000007ffffce9(2147482857)                  0x000000007ffffce9(2147482857)                  
t1(x6)              0x000000008017f8c9(2149054665)                  0x000000008017f8c9(2149054665)                  
t2(x7)              0x000000008000060c(2147485196)                  0x000000008000060c(2147485196)                  
fp(x8)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x000000008017fc97(2149055639)                  0x000000008017fc97(2149055639)                  
a1(x11)             0x0000000080000c88(2147486856)                  0x0000000080000c88(2147486856)                  
a2(x12)             0x00000000801805a2(2149057954)                  0x00000000801805a2(2149057954)                  
a3(x13)             0x000000000000004d(77)                          0x000000000000004d(77)                          
a4(x14)             0x000000008017fb02(2149055234)                  0x000000008017fb02(2149055234)                  
a5(x15)             0x000000000000007f(127)                         0x000000000000007f(127)                         
a6(x16)             0x00000000801807a1(2149058465)                  0x00000000801807a1(2149058465)                  
a7(x17)             0x000000008017fb02(2149055234)                  0x000000008017fb02(2149055234)                  
s2(x18)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s3(x19)             0x41e0000000000000(4746794007248502784)         0x41e0000000000000(4746794007248502784)         
s4(x20)             0x00000000ddb5c770(3719677808)                  0x00000000ddb5c770(3719677808)                  
s5(x21)             0x0000000000000085(133)                         0x0000000000000085(133)                         
s6(x22)             0x00000000000041e0(16864)                       0x00000000000041e0(16864)                       
s7(x23)             0x000000008017fef5(2149056245)                  0x000000008017fef5(2149056245)                  
s8(x24)             0x00000000000000b5(181)                         0x00000000000000b5(181)                         
s9(x25)             0x000000008023fba7(2149841831)                  0x000000008023fba7(2149841831)                  
s10(x26)            0x0000000000001078(4216)                        0x0000000000001078(4216)                        
s11(x27)            0x0000000000000038(56)                          0x0000000000000038(56)                          
t3(x28)             0x000000008000662f(2147509807)                  0x000000008000662f(2147509807)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x000000007ffffc1e(2147482654)                  0x000000007ffffc1e(2147482654)                  
t6(x31)             0x000000008017fd51(2149055825)                  0x000000008017fd51(2149055825)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            dda8a51c7160c6e9d79b22975f804140cb091540        dda8a51c7160c6e9d79b22975f804140cb091540        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000750(2147485520)                  0x0000000080000750(2147485520)                  
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
f0                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xe943dea1dda3df9f(-1.1882218372422584e+199_d)  0xe943dea1dda3df9f(-1.1882218372422584e+199_d)  
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x3749308f1fe86b13(2.259088984197151e-42_d)     0x3749308f1fe86b13(2.259088984197151e-42_d)     
f7                  0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0xc3cffffce0801382(-4.6116791507772385e+18_d)   
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x41e003005cc00000(2149057254.0_d)              0x41e003005cc00000(2149057254.0_d)              
f13                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0xc3cffffce0801382(-4.6116791507772385e+18_d)   
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
f27                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x39354053c3c21caf(4.092847294095176e-33_d)     0x39354053c3c21caf(4.092847294095176e-33_d)     
f30                 0xffffffff431f0000(159.0_s)                     0xffffffff431f0000(159.0_s)                     
f31                 0x5c1b982f3486f3c8(5.014182396516635e+135_d)    0x5c1b982f3486f3c8(5.014182396516635e+135_d)    
STATES DIFFER: True
```

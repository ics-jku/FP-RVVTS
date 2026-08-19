# FailID_003963 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3963
* Isolated failing instruction: `flw`
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
    li x1, 0x6000                // ra
    li x2, 0x8017fbd9            // sp
    li x3, 0xffffffff945e4000    // gp
    li x4, 0x20000007            // tp
    li x5, 0x7ffffce9            // t0
    li x6, 0x80036d81            // t1
    li x7, 0x8000038d            // t2
    li x8, 0x80180065            // fp
    li x9, 0x271b423             // s1
    li x10, 0x80000106           // a0
    li x11, 0x80000c88           // a1
    li x12, 0x7ffffc78           // a2
    li x13, 0x7ffffe2d           // a3
    li x14, 0x8017fb02           // a4
    li x15, 0x80000296           // a5
    li x16, 0x8000001e           // a6
    li x17, 0x8017fb02           // a7
    li x18, 0x1                  // s2
    li x19, 0x80000cf0           // s3
    li x20, 0x6000               // s4
    li x21, 0x80180795           // s5
    li x22, 0x41e0               // s6
    li x23, 0x8000062f           // s7
    li x24, 0xb01b823            // s8
    li x25, 0x800007ef           // s9
    li x26, 0x8000042f           // s10
    li x27, 0x80000cf0           // s11
    li x28, 0x8000662f           // t3
    li x29, 0x0                  // t4
    li x30, 0x7ffffebd           // t5
    li x31, 0x30                 // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x9', 'fcsr.rm'}, 'clob': {'x9', 'f3', 'x20'}})
    
    li x20, 0x1ffffc
    and x9, x9, x20
    li x20, 0x800003d4
    add x9, x9, x20
    flw f3, -0x3d4(x9)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f3, -0x3d4(x9)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f3, x3, d4, x9
gp(x3)              0xffffffff945e4000(18446744071903789056)        0xffffffff945e4000(18446744071903789056)
s1(x9)              0x000000008011b7f4(2148644852)                  0x000000008011b7f4(2148644852)
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
sp(x2)              0x000000008017fbd9(2149055449)                  0x000000008017fbd9(2149055449)                  
gp(x3)              0xffffffff945e4000(18446744071903789056)        0xffffffff945e4000(18446744071903789056)        
tp(x4)              0x0000000020000007(536870919)                   0x0000000020000007(536870919)                   
t0(x5)              0x000000007ffffce9(2147482857)                  0x000000007ffffce9(2147482857)                  
t1(x6)              0x0000000080036d81(2147708289)                  0x0000000080036d81(2147708289)                  
t2(x7)              0x000000008000038d(2147484557)                  0x000000008000038d(2147484557)                  
fp(x8)              0x0000000080180065(2149056613)                  0x0000000080180065(2149056613)                  
s1(x9)              0x000000008011b7f4(2148644852)                  0x000000008011b7f4(2148644852)                  
a0(x10)             0x0000000080000106(2147483910)                  0x0000000080000106(2147483910)                  
a1(x11)             0x0000000080000c88(2147486856)                  0x0000000080000c88(2147486856)                  
a2(x12)             0x000000007ffffc78(2147482744)                  0x000000007ffffc78(2147482744)                  
a3(x13)             0x000000007ffffe2d(2147483181)                  0x000000007ffffe2d(2147483181)                  
a4(x14)             0x000000008017fb02(2149055234)                  0x000000008017fb02(2149055234)                  
a5(x15)             0x0000000080000296(2147484310)                  0x0000000080000296(2147484310)                  
a6(x16)             0x000000008000001e(2147483678)                  0x000000008000001e(2147483678)                  
a7(x17)             0x000000008017fb02(2149055234)                  0x000000008017fb02(2149055234)                  
s2(x18)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s3(x19)             0x0000000080000cf0(2147486960)                  0x0000000080000cf0(2147486960)                  
s4(x20)             0x00000000800003d4(2147484628)                  0x00000000800003d4(2147484628)                  
s5(x21)             0x0000000080180795(2149058453)                  0x0000000080180795(2149058453)                  
s6(x22)             0x00000000000041e0(16864)                       0x00000000000041e0(16864)                       
s7(x23)             0x000000008000062f(2147485231)                  0x000000008000062f(2147485231)                  
s8(x24)             0x000000000b01b823(184662051)                   0x000000000b01b823(184662051)                   
s9(x25)             0x00000000800007ef(2147485679)                  0x00000000800007ef(2147485679)                  
s10(x26)            0x000000008000042f(2147484719)                  0x000000008000042f(2147484719)                  
s11(x27)            0x0000000080000cf0(2147486960)                  0x0000000080000cf0(2147486960)                  
t3(x28)             0x000000008000662f(2147509807)                  0x000000008000662f(2147509807)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x000000007ffffebd(2147483325)                  0x000000007ffffebd(2147483325)                  
t6(x31)             0x0000000000000030(48)                          0x0000000000000030(48)                          

STATE               REF                                             DUT                                             DIFF
xmemhash            87657dd1dd5321bf26f869e455640caedce27143        87657dd1dd5321bf26f869e455640caedce27143        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000764(2147485540)                  0x0000000080000764(2147485540)                  
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
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
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

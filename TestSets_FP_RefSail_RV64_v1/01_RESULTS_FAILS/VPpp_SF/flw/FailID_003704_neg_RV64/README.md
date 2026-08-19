# FailID_003704 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3704
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
_reg_f0: .byte 0x08,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x93,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x9f,0xc6,0x2d,0x21,0x36,0x22,0xbc,0x65
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x93,0x17,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x80,0xbf,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0xbc,0x6d,0x47,0xe2,0xcd,0xd0,0x0c,0x74
_reg_f30:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x48
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xffffffffb219d000    // ra
    li x2, 0x7ffffcf7            // sp
    li x3, 0x8017fd21            // gp
    li x4, 0x0                   // tp
    li x5, 0x80000487            // t0
    li x6, 0x7ffffd90            // t1
    li x7, 0x802807a3            // t2
    li x8, 0xffffffff001803c1    // fp
    li x9, 0xffffffff8000032e    // s1
    li x10, 0x17590748           // a0
    li x11, 0x80180a5a           // a1
    li x12, 0x80180000           // a2
    li x13, 0x7ffff93a           // a3
    li x14, 0x7ffffcdd           // a4
    li x15, 0x8018068a           // a5
    li x16, 0x801800ef           // a6
    li x17, 0xc7                 // a7
    li x18, 0x10030086a0000000   // s2
    li x19, 0x25                 // s3
    li x20, 0x80000586           // s4
    li x21, 0x8027f768           // s5
    li x22, 0x0                  // s6
    li x23, 0x7fffffffffffffff   // s7
    li x24, 0xfffff9b            // s8
    li x25, 0xff                 // s9
    li x26, 0x8018e177           // s10
    li x27, 0x9d                 // s11
    li x28, 0x80180435           // t3
    li x29, 0x0                  // t4
    li x30, 0x7ffffd90           // t5
    li x31, 0x801800ef           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x23'}, 'clob': {'f27', 'x20', 'x23'}})
    
    li x20, 0x1ffffc
    and x23, x23, x20
    li x20, 0x7fffff79
    add x23, x23, x20
    flw f27, 0x87(x23)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f27                 0xffffffffbf800000(-1.0_s)                      0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f27, 0x87(x23)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f27                 0xffffffffbf800000(-1.0_s)                      0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f27, x87, x23
s7(x23)             0x00000000801fff75(2149580661)                  0x00000000801fff75(2149580661)
f27                 0xffffffffbf800000(-1.0_s)                      0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xffffffffb219d000(18446744072402620416)        0xffffffffb219d000(18446744072402620416)        
sp(x2)              0x000000007ffffcf7(2147482871)                  0x000000007ffffcf7(2147482871)                  
gp(x3)              0x000000008017fd21(2149055777)                  0x000000008017fd21(2149055777)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000080000487(2147484807)                  0x0000000080000487(2147484807)                  
t1(x6)              0x000000007ffffd90(2147483024)                  0x000000007ffffd90(2147483024)                  
t2(x7)              0x00000000802807a3(2150107043)                  0x00000000802807a3(2150107043)                  
fp(x8)              0xffffffff001803c1(18446744069416158145)        0xffffffff001803c1(18446744069416158145)        
s1(x9)              0xffffffff8000032e(18446744071562068782)        0xffffffff8000032e(18446744071562068782)        
a0(x10)             0x0000000017590748(391710536)                   0x0000000017590748(391710536)                   
a1(x11)             0x0000000080180a5a(2149059162)                  0x0000000080180a5a(2149059162)                  
a2(x12)             0x0000000080180000(2149056512)                  0x0000000080180000(2149056512)                  
a3(x13)             0x000000007ffff93a(2147481914)                  0x000000007ffff93a(2147481914)                  
a4(x14)             0x000000007ffffcdd(2147482845)                  0x000000007ffffcdd(2147482845)                  
a5(x15)             0x000000008018068a(2149058186)                  0x000000008018068a(2149058186)                  
a6(x16)             0x00000000801800ef(2149056751)                  0x00000000801800ef(2149056751)                  
a7(x17)             0x00000000000000c7(199)                         0x00000000000000c7(199)                         
s2(x18)             0x10030086a0000000(1153766507746951168)         0x10030086a0000000(1153766507746951168)         
s3(x19)             0x0000000000000025(37)                          0x0000000000000025(37)                          
s4(x20)             0x000000007fffff79(2147483513)                  0x000000007fffff79(2147483513)                  
s5(x21)             0x000000008027f768(2150102888)                  0x000000008027f768(2150102888)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x00000000801fff75(2149580661)                  0x00000000801fff75(2149580661)                  
s8(x24)             0x000000000fffff9b(268435355)                   0x000000000fffff9b(268435355)                   
s9(x25)             0x00000000000000ff(255)                         0x00000000000000ff(255)                         
s10(x26)            0x000000008018e177(2149114231)                  0x000000008018e177(2149114231)                  
s11(x27)            0x000000000000009d(157)                         0x000000000000009d(157)                         
t3(x28)             0x0000000080180435(2149057589)                  0x0000000080180435(2149057589)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x000000007ffffd90(2147483024)                  0x000000007ffffd90(2147483024)                  
t6(x31)             0x00000000801800ef(2149056751)                  0x00000000801800ef(2149056751)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            301e214ecf3de406162c77e206822a67c63e9e14        301e214ecf3de406162c77e206822a67c63e9e14        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000758(2147485528)                  0x0000000080000758(2147485528)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000048(72)                          0x0000000000000048(72)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff4f000008(2147485696.0_s)              0xffffffff4f000008(2147485696.0_s)              
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff4f001793(2149028608.0_s)              0xffffffff4f001793(2149028608.0_s)              
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0x65bc2236212dc69f(1.1674097076675866e+182_d)   0x65bc2236212dc69f(1.1674097076675866e+182_d)   
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xfffffffffffffe00(nan_h)                       0xfffffffffffffe00(nan_h)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7fffffff4f001793(nan_d)                       0x7fffffff4f001793(nan_d)                       
f22                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0x7fffffff3f800000(nan_d)                       0x7fffffff3f800000(nan_d)                       
f25                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffffbf800000(-1.0_s)                      0xffffffff00000000(0.0_s)                       X
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x740cd0cde2476dbc(1.0315604867321677e+251_d)   0x740cd0cde2476dbc(1.0315604867321677e+251_d)   
f30                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

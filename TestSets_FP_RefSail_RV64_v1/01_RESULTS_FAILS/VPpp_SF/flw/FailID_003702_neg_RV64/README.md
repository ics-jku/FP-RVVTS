# FailID_003702 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3702
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
_reg_f0: .byte 0x24,0x39,0x8b,0x6c,0xf7,0x98,0x6a,0x36
_reg_f1: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x93,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x27,0xd9,0x31,0x4a,0xdf,0x5f,0x7f,0xd5
_reg_f6: .byte 0xa7,0x28,0x75,0x18,0x81,0xf2,0xbb,0x8b
_reg_f7: .byte 0x8b,0x1e,0xbc,0x6d,0x08,0x03,0x9b,0x9e
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x9f,0xc6,0x2d,0x21,0x36,0x22,0xbc,0x65
_reg_f11:.byte 0xb9,0x9f,0x8d,0x90,0xee,0x40,0x90,0xc6
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0xc7,0xb9,0x06,0x78,0x74,0xe8,0x8b,0x1a
_reg_f14:.byte 0x83,0xf2,0xb1,0x38,0x72,0xe2,0x1a,0x4b
_reg_f15:.byte 0x9f,0xc6,0x2d,0x21,0x36,0x22,0xbc,0x65
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f17:.byte 0x11,0xcb,0xb7,0x1f,0x0e,0x7a,0x03,0x79
_reg_f18:.byte 0xbc,0x6d,0x47,0xe2,0xcd,0xd0,0x0c,0x74
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0xc9,0xa4,0x04,0x97,0xfe,0xca,0x2b,0x81
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x08,0xe6,0x04,0x84,0x77,0xb9,0xda,0x3e
_reg_f23:.byte 0x2b,0x85,0xc3,0xfa,0x19,0x5e,0x39,0xee
_reg_f24:.byte 0x13,0x2a,0x8a,0x51,0xe5,0xc2,0x57,0x69
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0xfb,0x1a,0x42,0x87,0x41,0xa3,0x9f,0xc3
_reg_f27:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x08,0x81,0xf6,0xfd,0x05,0xfa,0x71,0x8b
_reg_f30:.byte 0x07,0x8e,0xca,0x2c,0xdf,0x1a,0xb7,0xdb
_reg_f31:.byte 0x79,0xd2,0xf5,0x3c,0x67,0x16,0x61,0x37
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': True, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x9d
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7fffffffffffffff    // ra
    li x2, 0x0                   // sp
    li x3, 0x6000                // gp
    li x4, 0x0                   // tp
    li x5, 0xe28e5285f4945981    // t0
    li x6, 0x70106b707c64b3f9    // t1
    li x7, 0x7bf1b000            // t2
    li x8, 0x7371c4a4bd250737    // fp
    li x9, 0x0                   // s1
    li x10, 0x7ffffe9c           // a0
    li x11, 0x7ffffe99           // a1
    li x12, 0x271c206a0424f3c5   // a2
    li x13, 0xa363a810           // a3
    li x14, 0x800062c1           // a4
    li x15, 0x6000               // a5
    li x16, 0x7fffffff           // a6
    li x17, 0x80179356           // a7
    li x18, 0xf8172f9e2f794122   // s2
    li x19, 0x800002c1           // s3
    li x20, 0x7ffffd11           // s4
    li x21, 0x300000000000       // s5
    li x22, 0xffffffdfc16e0704   // s6
    li x23, 0x8018b3e0           // s7
    li x24, 0x1                  // s8
    li x25, 0x0                  // s9
    li x26, 0xbf82dc0e0964ccdf   // s10
    li x27, 0x801ffc5d           // s11
    li x28, 0x8000022c           // t3
    li x29, 0x7ffffd11           // t4
    li x30, 0x8000040a           // t5
    li x31, 0x5de4c2c1ae235d30   // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x30'}, 'clob': {'x29', 'f9', 'x30'}})
    
    li x29, 0x1ffffc
    and x30, x30, x29
    li x29, 0x7ffffd36
    add x30, x30, x29
    flw f9, 0x2ca(x30)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f9                  0xffffffff4f000000(2147483648.0_s)              0xffffffff7fc00000(nan_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f9, 0x2ca(x30)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f9                  0xffffffff4f000000(2147483648.0_s)              0xffffffff7fc00000(nan_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x2, x30
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)
t5(x30)             0x000000008000013e(2147483966)                  0x000000008000013e(2147483966)
f9                  0xffffffff4f000000(2147483648.0_s)              0xffffffff7fc00000(nan_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0xe28e5285f4945981(16325076434552117633)        0xe28e5285f4945981(16325076434552117633)        
t1(x6)              0x70106b707c64b3f9(8075072262742782969)         0x70106b707c64b3f9(8075072262742782969)         
t2(x7)              0x000000007bf1b000(2079436800)                  0x000000007bf1b000(2079436800)                  
fp(x8)              0x7371c4a4bd250737(8318646198557017911)         0x7371c4a4bd250737(8318646198557017911)         
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x000000007ffffe9c(2147483292)                  0x000000007ffffe9c(2147483292)                  
a1(x11)             0x000000007ffffe99(2147483289)                  0x000000007ffffe99(2147483289)                  
a2(x12)             0x271c206a0424f3c5(2818163106535240645)         0x271c206a0424f3c5(2818163106535240645)         
a3(x13)             0x00000000a363a810(2741217296)                  0x00000000a363a810(2741217296)                  
a4(x14)             0x00000000800062c1(2147508929)                  0x00000000800062c1(2147508929)                  
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a7(x17)             0x0000000080179356(2149028694)                  0x0000000080179356(2149028694)                  
s2(x18)             0xf8172f9e2f794122(17876809602318287138)        0xf8172f9e2f794122(17876809602318287138)        
s3(x19)             0x00000000800002c1(2147484353)                  0x00000000800002c1(2147484353)                  
s4(x20)             0x000000007ffffd11(2147482897)                  0x000000007ffffd11(2147482897)                  
s5(x21)             0x0000300000000000(52776558133248)              0x0000300000000000(52776558133248)              
s6(x22)             0xffffffdfc16e0704(18446743935220844292)        0xffffffdfc16e0704(18446743935220844292)        
s7(x23)             0x000000008018b3e0(2149102560)                  0x000000008018b3e0(2149102560)                  
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0xbf82dc0e0964ccdf(13799834161061874911)        0xbf82dc0e0964ccdf(13799834161061874911)        
s11(x27)            0x00000000801ffc5d(2149579869)                  0x00000000801ffc5d(2149579869)                  
t3(x28)             0x000000008000022c(2147484204)                  0x000000008000022c(2147484204)                  
t4(x29)             0x000000007ffffd36(2147482934)                  0x000000007ffffd36(2147482934)                  
t5(x30)             0x000000008000013e(2147483966)                  0x000000008000013e(2147483966)                  
t6(x31)             0x5de4c2c1ae235d30(6765746677323357488)         0x5de4c2c1ae235d30(6765746677323357488)         

STATE               REF                                             DUT                                             DIFF
xmemhash            8b5f448a43465eebb956919da22c00004c22c44e        8b5f448a43465eebb956919da22c00004c22c44e        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800007c8(2147485640)                  0x00000000800007c8(2147485640)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000009d(157)                         0x000000000000009d(157)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x366a98f76c8b3924(1.4559012298714779e-46_d)    0x366a98f76c8b3924(1.4559012298714779e-46_d)    
f1                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff4f001793(2149028608.0_s)              0xffffffff4f001793(2149028608.0_s)              
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xd57f5fdf4a31d927(-7.027087338960861e+103_d)   0xd57f5fdf4a31d927(-7.027087338960861e+103_d)   
f6                  0x8bbbf281187528a7(-3.8119151472262454e-252_d)  0x8bbbf281187528a7(-3.8119151472262454e-252_d)  
f7                  0x9e9b03086dbc1e8b(-3.002041003072988e-161_d)   0x9e9b03086dbc1e8b(-3.002041003072988e-161_d)   
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff4f000000(2147483648.0_s)              0xffffffff7fc00000(nan_s)                       X
f10                 0x65bc2236212dc69f(1.1674097076675866e+182_d)   0x65bc2236212dc69f(1.1674097076675866e+182_d)   
f11                 0xc69040ee908d9fb9(-8.24157470614488e+31_d)     0xc69040ee908d9fb9(-8.24157470614488e+31_d)     
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x1a8be8747806b9c7(8.407013635202656e-181_d)    0x1a8be8747806b9c7(8.407013635202656e-181_d)    
f14                 0x4b1ae27238b1f283(6.437572068737457e+53_d)     0x4b1ae27238b1f283(6.437572068737457e+53_d)     
f15                 0x65bc2236212dc69f(1.1674097076675866e+182_d)   0x65bc2236212dc69f(1.1674097076675866e+182_d)   
f16                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f17                 0x79037a0e1fb7cb11(8.429138172903063e+274_d)    0x79037a0e1fb7cb11(8.429138172903063e+274_d)    
f18                 0x740cd0cde2476dbc(1.0315604867321677e+251_d)   0x740cd0cde2476dbc(1.0315604867321677e+251_d)   
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0x812bcafe9704a4c9(-5.0660442391190137e-303_d)  0x812bcafe9704a4c9(-5.0660442391190137e-303_d)  
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x3edab9778404e608(6.3716125285272795e-06_d)    0x3edab9778404e608(6.3716125285272795e-06_d)    
f23                 0xee395e19fac3852b(-9.169716618066727e+222_d)   0xee395e19fac3852b(-9.169716618066727e+222_d)   
f24                 0x6957c2e5518a2a13(2.8418919176870444e+199_d)   0x6957c2e5518a2a13(2.8418919176870444e+199_d)   
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xc39fa34187421afb(-5.6993447139126445e+17_d)   0xc39fa34187421afb(-5.6993447139126445e+17_d)   
f27                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x8b71fa05fdf68108(-1.5324718916244918e-253_d)  0x8b71fa05fdf68108(-1.5324718916244918e-253_d)  
f30                 0xdbb71adf2cca8e07(-6.559994288512194e+133_d)   0xdbb71adf2cca8e07(-6.559994288512194e+133_d)   
f31                 0x376116673cf5d279(6.129844590094841e-42_d)     0x376116673cf5d279(6.129844590094841e-42_d)     
STATES DIFFER: True
```

# FailID_003840 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3840
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
_reg_f0: .byte 0x48,0x47,0xe3,0xe9,0x8f,0xad,0x05,0xe5
_reg_f1: .byte 0x00,0x00,0xe0,0x8e,0xd5,0x03,0xe0,0x41
_reg_f2: .byte 0xef,0x9d,0x11,0x89,0x0a,0x13,0x15,0x41
_reg_f3: .byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0xfb,0xf9,0xff,0x7f,0x00,0x00,0x00,0x00
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x1c,0xaf,0xcd,0xa8,0x30,0x6e,0x0a,0xfd
_reg_f10:.byte 0x4d,0xc2,0x2b,0x45,0x6c,0x01,0xa5,0x6a
_reg_f11:.byte 0x00,0x00,0x00,0xe0,0x2e,0x99,0xd2,0xc1
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x97,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x82,0x1b,0x30,0x4d,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x6d,0xb4,0x88,0x69,0xc0,0xd8,0x6a,0x0f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x70
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x800002d1            // ra
    li x2, 0x801801d3            // sp
    li x3, 0x37a                 // gp
    li x4, 0x0                   // tp
    li x5, 0xcb                  // t0
    li x6, 0x0                   // t1
    li x7, 0x3f4bb768            // t2
    li x8, 0x8018054f            // fp
    li x9, 0x7ffffa8b            // s1
    li x10, 0x6000               // a0
    li x11, 0x8017fd87           // a1
    li x12, 0x6000               // a2
    li x13, 0x7ffff9be           // a3
    li x14, 0x8027fe2e           // a4
    li x15, 0x6000               // a5
    li x16, 0x80003b41           // a6
    li x17, 0x80075aa6           // a7
    li x18, 0x0                  // s2
    li x19, 0x8018067e           // s3
    li x20, 0x800ce9e9           // s4
    li x21, 0x80000807           // s5
    li x22, 0x0                  // s6
    li x23, 0x8000035a           // s7
    li x24, 0x1                  // s8
    li x25, 0x7f                 // s9
    li x26, 0x800004d3           // s10
    li x27, 0x0                  // s11
    li x28, 0x70                 // t3
    li x29, 0x800003e3           // t4
    li x30, 0x6000               // t5
    li x31, 0x802802f5           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x25'}, 'clob': {'x13', 'f5', 'x25'}})
    
    li x13, 0x1ffffc
    and x25, x25, x13
    li x13, 0x7ffffa0c
    add x25, x25, x13
    flw f5, 0x5f4(x25)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f5                  0x000000007ffff9fb(1.060997134e-314_d)          0xffffffff340090f3(1.1973661173669825e-07_s)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f5, 0x5f4(x25)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f5                  0x000000007ffff9fb(1.060997134e-314_d)          0xffffffff340090f3(1.1973661173669825e-07_s)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f5, x5, f4, x25
t0(x5)              0x00000000000000cb(203)                         0x00000000000000cb(203)
s9(x25)             0x000000007ffffa88(2147482248)                  0x000000007ffffa88(2147482248)
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
f5                  0x000000007ffff9fb(1.060997134e-314_d)          0xffffffff340090f3(1.1973661173669825e-07_s)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000800002d1(2147484369)                  0x00000000800002d1(2147484369)                  
sp(x2)              0x00000000801801d3(2149056979)                  0x00000000801801d3(2149056979)                  
gp(x3)              0x000000000000037a(890)                         0x000000000000037a(890)                         
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x00000000000000cb(203)                         0x00000000000000cb(203)                         
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x000000003f4bb768(1061926760)                  0x000000003f4bb768(1061926760)                  
fp(x8)              0x000000008018054f(2149057871)                  0x000000008018054f(2149057871)                  
s1(x9)              0x000000007ffffa8b(2147482251)                  0x000000007ffffa8b(2147482251)                  
a0(x10)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a1(x11)             0x000000008017fd87(2149055879)                  0x000000008017fd87(2149055879)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x000000007ffffa0c(2147482124)                  0x000000007ffffa0c(2147482124)                  
a4(x14)             0x000000008027fe2e(2150104622)                  0x000000008027fe2e(2150104622)                  
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x0000000080003b41(2147498817)                  0x0000000080003b41(2147498817)                  
a7(x17)             0x0000000080075aa6(2147965606)                  0x0000000080075aa6(2147965606)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000008018067e(2149058174)                  0x000000008018067e(2149058174)                  
s4(x20)             0x00000000800ce9e9(2148329961)                  0x00000000800ce9e9(2148329961)                  
s5(x21)             0x0000000080000807(2147485703)                  0x0000000080000807(2147485703)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x000000008000035a(2147484506)                  0x000000008000035a(2147484506)                  
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x000000007ffffa88(2147482248)                  0x000000007ffffa88(2147482248)                  
s10(x26)            0x00000000800004d3(2147484883)                  0x00000000800004d3(2147484883)                  
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x0000000000000070(112)                         0x0000000000000070(112)                         
t4(x29)             0x00000000800003e3(2147484643)                  0x00000000800003e3(2147484643)                  
t5(x30)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t6(x31)             0x00000000802802f5(2150105845)                  0x00000000802802f5(2150105845)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            27938619417f552e08a4adf7dbd2e82856a863a9        27938619417f552e08a4adf7dbd2e82856a863a9        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000734(2147485492)                  0x0000000080000734(2147485492)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000070(112)                         0x0000000000000070(112)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  
f1                  0x41e003d58ee00000(2149493879.0_d)              0x41e003d58ee00000(2149493879.0_d)              
f2                  0x4115130a89119def(345282.63385626575_d)        0x4115130a89119def(345282.63385626575_d)        
f3                  0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x000000007ffff9fb(1.060997134e-314_d)          0xffffffff340090f3(1.1973661173669825e-07_s)    X
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  
f10                 0x6aa5016c452bc24d(5.268673489679908e+205_d)    0x6aa5016c452bc24d(5.268673489679908e+205_d)    
f11                 0xc1d2992ee0000000(-1248115584.0_d)             0xc1d2992ee0000000(-1248115584.0_d)             
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f14                 0xffffffff00000297(9.290608818473537e-43_s)     0xffffffff00000297(9.290608818473537e-43_s)     
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffff4f000000(2147483648.0_s)              0xffffffff4f000000(2147483648.0_s)              
f17                 0xffffffff4d301b82(184662048.0_s)               0xffffffff4d301b82(184662048.0_s)               
f18                 0x0f6ad8c06988b46d(2.1108825482638558e-234_d)   0x0f6ad8c06988b46d(2.1108825482638558e-234_d)   
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f23                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

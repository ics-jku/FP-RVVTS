# FailID_004201 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4201
* Isolated failing instruction: `fsd`
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
_reg_f0: .byte 0x46,0xe7,0xd2,0x01,0xeb,0xfe,0xde,0xc0
_reg_f1: .byte 0x82,0x1e,0x50,0x56,0x55,0xdb,0xee,0x7e
_reg_f2: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x00,0x60,0xc9,0x00,0x00,0xe0,0x41
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f6: .byte 0xb8,0x03,0x08,0x8c,0x58,0xfd,0xaa,0xb8
_reg_f7: .byte 0x00,0x00,0x10,0x41,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x9b,0x5c,0xfa,0x6d,0x32,0x4b,0xca,0xcd
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f11:.byte 0xcb,0xe1,0xb6,0xbd,0xa6,0xa5,0x2d,0x9d
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0xf5,0x23,0x56,0x01,0x25,0x80,0x47,0xad
_reg_f15:.byte 0x5c,0xe9,0xbe,0xf7,0x1c,0xf0,0x59,0x9e
_reg_f16:.byte 0x69,0xff,0x7e,0x97,0xae,0x15,0x1a,0x0b
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x22,0x40
_reg_f20:.byte 0x9b,0x5c,0xfa,0x6d,0x32,0x4b,0xca,0x4d
_reg_f21:.byte 0x01,0x17,0x4e,0x4e,0xa3,0xc2,0x21,0x2a
_reg_f22:.byte 0x0c,0x37,0x68,0xc8,0x1e,0xad,0x09,0x16
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0xaf,0x68,0xa8,0xdd,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x08,0x56,0x08,0xdf,0xcb,0x87,0x85,0x45
_reg_f26:.byte 0x95,0x27,0x4e,0xd1,0x94,0x7d,0xd1,0x41
_reg_f27:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f31:.byte 0xa9,0xe4,0x48,0xd7,0x3c,0xdc,0x4d,0x99
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
    li x1, 0x7ffffcd7            // ra
    li x2, 0x5c519c74b729e9d1    // sp
    li x3, 0x800eb4fd            // gp
    li x4, 0x200                 // tp
    li x5, 0x8017f8e0            // t0
    li x6, 0x12c5d983d7d1456     // t1
    li x7, 0x801f41a3            // t2
    li x8, 0x2                   // fp
    li x9, 0x371c3481b19e2e98    // s1
    li x10, 0x371c3481b19e29f7   // a0
    li x11, 0x8017fc62           // a1
    li x12, 0x64                 // a2
    li x13, 0xffffffffac08e000   // a3
    li x14, 0x8017f8e0           // a4
    li x15, 0x8017fc62           // a5
    li x16, 0x6000               // a6
    li x17, 0x8000062b           // a7
    li x18, 0xa55ac4bb7b8c5a21   // s2
    li x19, 0x9                  // s3
    li x20, 0x800a53d1           // s4
    li x21, 0x4d09208dd1         // s5
    li x22, 0x80000636           // s6
    li x23, 0x0                  // s7
    li x24, 0xffffffffde822946   // s8
    li x25, 0xe                  // s9
    li x26, 0xffffffffffffffff   // s10
    li x27, 0x6000               // s11
    li x28, 0x0                  // t3
    li x29, 0x166673e017d6f72c   // t4
    li x30, 0x40a0e980           // t5
    li x31, 0x8000062b           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'f14', 'fcsr.rm', 'x22'}, 'clob': {'x22', 'x7'}})
    
    li x7, 0xffff8
    and x22, x22, x7
    li x7, 0x8017fe40
    add x22, x22, x7
    fsd f14, 0x1c0(x22)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        aaf20c144dd9ad5387d44bb02a6dd981df51e7e3        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f14, 0x1c0(x22)
+========================================================================================================================+
Attributes:  fcsr ['overflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        aaf20c144dd9ad5387d44bb02a6dd981df51e7e3        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x1, c0, x22
ra(x1)              0x000000007ffffcd7(2147482839)                  0x000000007ffffcd7(2147482839)
s6(x22)             0x0000000080180470(2149057648)                  0x0000000080180470(2149057648)
f14                 0xad478025015623f5(-1.4420808547245098e-90_d)   0xad478025015623f5(-1.4420808547245098e-90_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffffcd7(2147482839)                  0x000000007ffffcd7(2147482839)                  
sp(x2)              0x5c519c74b729e9d1(6652270149706050001)         0x5c519c74b729e9d1(6652270149706050001)         
gp(x3)              0x00000000800eb4fd(2148447485)                  0x00000000800eb4fd(2148447485)                  
tp(x4)              0x0000000000000200(512)                         0x0000000000000200(512)                         
t0(x5)              0x000000008017f8e0(2149054688)                  0x000000008017f8e0(2149054688)                  
t1(x6)              0x012c5d983d7d1456(84545401461216342)           0x012c5d983d7d1456(84545401461216342)           
t2(x7)              0x000000008017fe40(2149056064)                  0x000000008017fe40(2149056064)                  
fp(x8)              0x0000000000000002(2)                           0x0000000000000002(2)                           
s1(x9)              0x371c3481b19e2e98(3971106703069294232)         0x371c3481b19e2e98(3971106703069294232)         
a0(x10)             0x371c3481b19e29f7(3971106703069293047)         0x371c3481b19e29f7(3971106703069293047)         
a1(x11)             0x000000008017fc62(2149055586)                  0x000000008017fc62(2149055586)                  
a2(x12)             0x0000000000000064(100)                         0x0000000000000064(100)                         
a3(x13)             0xffffffffac08e000(18446744072300847104)        0xffffffffac08e000(18446744072300847104)        
a4(x14)             0x000000008017f8e0(2149054688)                  0x000000008017f8e0(2149054688)                  
a5(x15)             0x000000008017fc62(2149055586)                  0x000000008017fc62(2149055586)                  
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x000000008000062b(2147485227)                  0x000000008000062b(2147485227)                  
s2(x18)             0xa55ac4bb7b8c5a21(11915052073672792609)        0xa55ac4bb7b8c5a21(11915052073672792609)        
s3(x19)             0x0000000000000009(9)                           0x0000000000000009(9)                           
s4(x20)             0x00000000800a53d1(2148160465)                  0x00000000800a53d1(2148160465)                  
s5(x21)             0x0000004d09208dd1(330865610193)                0x0000004d09208dd1(330865610193)                
s6(x22)             0x0000000080180470(2149057648)                  0x0000000080180470(2149057648)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0xffffffffde822946(18446744073147656518)        0xffffffffde822946(18446744073147656518)        
s9(x25)             0x000000000000000e(14)                          0x000000000000000e(14)                          
s10(x26)            0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x166673e017d6f72c(1614104922768733996)         0x166673e017d6f72c(1614104922768733996)         
t5(x30)             0x0000000040a0e980(1084287360)                  0x0000000040a0e980(1084287360)                  
t6(x31)             0x000000008000062b(2147485227)                  0x000000008000062b(2147485227)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            76708b9db3b765076025eb245e85813fc4682aee        76708b9db3b765076025eb245e85813fc4682aee        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        aaf20c144dd9ad5387d44bb02a6dd981df51e7e3        X
lastPC              0x00000000800007c4(2147485636)                  0x00000000800007c4(2147485636)                  
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
f0                  0xc0defeeb01d2e746(-31739.671986318448_d)       0xc0defeeb01d2e746(-31739.671986318448_d)       
f1                  0x7eeedb5556501e82(2.6450636480365518e+303_d)   0x7eeedb5556501e82(2.6450636480365518e+303_d)   
f2                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f3                  0x41e00000c9600000(2147485259.0_d)              0x41e00000c9600000(2147485259.0_d)              
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f6                  0xb8aafd588c0803b8(-1.0152371322128331e-35_d)   0xb8aafd588c0803b8(-1.0152371322128331e-35_d)   
f7                  0xffffffff41100000(9.0_s)                       0xffffffff41100000(9.0_s)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0xcdca4b326dfa5c9b(-5.538107662154827e+66_d)    0xcdca4b326dfa5c9b(-5.538107662154827e+66_d)    
f10                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f11                 0x9d2da5a6bdb6e1cb(-3.9278445542876183e-168_d)  0x9d2da5a6bdb6e1cb(-3.9278445542876183e-168_d)  
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xad478025015623f5(-1.4420808547245098e-90_d)   0xad478025015623f5(-1.4420808547245098e-90_d)   
f15                 0x9e59f01cf7bee95c(-1.801680861024694e-162_d)   0x9e59f01cf7bee95c(-1.801680861024694e-162_d)   
f16                 0x0b1a15ae977eff69(3.4744771012814677e-255_d)   0x0b1a15ae977eff69(3.4744771012814677e-255_d)   
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x4022000000000000(9.0_d)                       0x4022000000000000(9.0_d)                       
f20                 0x4dca4b326dfa5c9b(5.538107662154827e+66_d)     0x4dca4b326dfa5c9b(5.538107662154827e+66_d)     
f21                 0x2a21c2a34e4e1701(9.679700821562473e-106_d)    0x2a21c2a34e4e1701(9.679700821562473e-106_d)    
f22                 0x1609ad1ec868370c(1.6378892730900231e-202_d)   0x1609ad1ec868370c(1.6378892730900231e-202_d)   
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffffdda868af(-1.5168927013105828e+18_s)   0xffffffffdda868af(-1.5168927013105828e+18_s)   
f25                 0x458587cbdf085608(8.329191183146061e+26_d)     0x458587cbdf085608(8.329191183146061e+26_d)     
f26                 0x41d17d94d14e2795(1173771077.221166_d)         0x41d17d94d14e2795(1173771077.221166_d)         
f27                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f31                 0x994ddc3cd748e4a9(-8.578412323428339e-187_d)   0x994ddc3cd748e4a9(-8.578412323428339e-187_d)   
STATES DIFFER: True
```

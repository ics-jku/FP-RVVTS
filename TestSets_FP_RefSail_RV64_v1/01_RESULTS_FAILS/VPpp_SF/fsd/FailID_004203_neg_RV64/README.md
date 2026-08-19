# FailID_004203 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4203
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
    li x1, 0x1                   // ra
    li x2, 0x6000                // sp
    li x3, 0xffffffff7fffffed    // gp
    li x4, 0x8027fff0            // tp
    li x5, 0xc                   // t0
    li x6, 0x801d1940            // t1
    li x7, 0x80180327            // t2
    li x8, 0x371c3481b19e2912    // fp
    li x9, 0x42b                 // s1
    li x10, 0x11                 // a0
    li x11, 0x8017f993           // a1
    li x12, 0xffffffff88b63000   // a2
    li x13, 0x8018015a           // a3
    li x14, 0x6000               // a4
    li x15, 0x80000805           // a5
    li x16, 0x8016f082           // a6
    li x17, 0x80180462           // a7
    li x18, 0x0                  // s2
    li x19, 0x8018069c           // s3
    li x20, 0xdc8cf79c           // s4
    li x21, 0x15c8cf48b          // s5
    li x22, 0x7ffffcef           // s6
    li x23, 0x8027fb19           // s7
    li x24, 0x8000031f           // s8
    li x25, 0x80180775           // s9
    li x26, 0x7ffffc7f           // s10
    li x27, 0x7ffffbc4           // s11
    li x28, 0xe5                 // t3
    li x29, 0x8016f082           // t4
    li x30, 0x8020ea83           // t5
    li x31, 0x8000062b           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x8', 'f16'}, 'clob': {'x12', 'x8'}})
    
    li x12, 0xffff8
    and x8, x8, x12
    li x12, 0x80180288
    add x8, x8, x12
    fsd f16, -0x288(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2884268dd560b7860093239085318b9a191be6d3        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f16, -0x288(x8)
+========================================================================================================================+
Attributes:  fcsr ['overflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2884268dd560b7860093239085318b9a191be6d3        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f16, x288, x8
fp(x8)              0x0000000080262b98(2149985176)                  0x0000000080262b98(2149985176)
f16                 0x0b1a15ae977eff69(3.4744771012814677e-255_d)   0x0b1a15ae977eff69(3.4744771012814677e-255_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000001(1)                           0x0000000000000001(1)                           
sp(x2)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
gp(x3)              0xffffffff7fffffed(18446744071562067949)        0xffffffff7fffffed(18446744071562067949)        
tp(x4)              0x000000008027fff0(2150105072)                  0x000000008027fff0(2150105072)                  
t0(x5)              0x000000000000000c(12)                          0x000000000000000c(12)                          
t1(x6)              0x00000000801d1940(2149390656)                  0x00000000801d1940(2149390656)                  
t2(x7)              0x0000000080180327(2149057319)                  0x0000000080180327(2149057319)                  
fp(x8)              0x0000000080262b98(2149985176)                  0x0000000080262b98(2149985176)                  
s1(x9)              0x000000000000042b(1067)                        0x000000000000042b(1067)                        
a0(x10)             0x0000000000000011(17)                          0x0000000000000011(17)                          
a1(x11)             0x000000008017f993(2149054867)                  0x000000008017f993(2149054867)                  
a2(x12)             0x0000000080180288(2149057160)                  0x0000000080180288(2149057160)                  
a3(x13)             0x000000008018015a(2149056858)                  0x000000008018015a(2149056858)                  
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x0000000080000805(2147485701)                  0x0000000080000805(2147485701)                  
a6(x16)             0x000000008016f082(2148987010)                  0x000000008016f082(2148987010)                  
a7(x17)             0x0000000080180462(2149057634)                  0x0000000080180462(2149057634)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000008018069c(2149058204)                  0x000000008018069c(2149058204)                  
s4(x20)             0x00000000dc8cf79c(3700225948)                  0x00000000dc8cf79c(3700225948)                  
s5(x21)             0x000000015c8cf48b(5847708811)                  0x000000015c8cf48b(5847708811)                  
s6(x22)             0x000000007ffffcef(2147482863)                  0x000000007ffffcef(2147482863)                  
s7(x23)             0x000000008027fb19(2150103833)                  0x000000008027fb19(2150103833)                  
s8(x24)             0x000000008000031f(2147484447)                  0x000000008000031f(2147484447)                  
s9(x25)             0x0000000080180775(2149058421)                  0x0000000080180775(2149058421)                  
s10(x26)            0x000000007ffffc7f(2147482751)                  0x000000007ffffc7f(2147482751)                  
s11(x27)            0x000000007ffffbc4(2147482564)                  0x000000007ffffbc4(2147482564)                  
t3(x28)             0x00000000000000e5(229)                         0x00000000000000e5(229)                         
t4(x29)             0x000000008016f082(2148987010)                  0x000000008016f082(2148987010)                  
t5(x30)             0x000000008020ea83(2149640835)                  0x000000008020ea83(2149640835)                  
t6(x31)             0x000000008000062b(2147485227)                  0x000000008000062b(2147485227)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            c9a3c746811a18274e8cfd5eeb9f0a5213e8c1c9        c9a3c746811a18274e8cfd5eeb9f0a5213e8c1c9        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2884268dd560b7860093239085318b9a191be6d3        X
lastPC              0x000000008000078c(2147485580)                  0x000000008000078c(2147485580)                  
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

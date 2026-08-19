# FailID_004030 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4030
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x5a,0x79,0x82,0x4f,0x2e,0x3a,0x42,0x27
_reg_f2: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0xd6,0x62,0x54,0xad,0x9b,0x11,0x0e,0x6d
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0xd7,0xdd,0x7c,0x96,0xf4,0x9b,0x21,0xc6
_reg_f10:.byte 0x49,0x2c,0x32,0x33,0x61,0x83,0x13,0x28
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x49,0x2c,0x32,0x33,0x61,0x83,0x13,0x28
_reg_f16:.byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0xe0,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xd9,0x37,0x41,0x8e,0x5e,0xe5,0xdd,0x04
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x03,0x00,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0xb0,0x44,0xc6,0x7a,0xb2,0x6e,0xf1,0xc2
_reg_f26:.byte 0x8d,0xd0,0xa9,0xf7,0xc3,0x9b,0xf8,0xec
_reg_f27:.byte 0x03,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x39,0xfe,0x17,0x80,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'dyn(0b111)', 'res': 0}
    li t0, 0xf0
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80200d84            // ra
    li x2, 0xffffffffffe798a8    // sp
    li x3, 0x801860a5            // gp
    li x4, 0x800001dd            // tp
    li x5, 0x801ff306            // t0
    li x6, 0x100                 // t1
    li x7, 0x80180700            // t2
    li x8, 0x8018054b            // fp
    li x9, 0x7ffff94d            // s1
    li x10, 0x8017f823           // a0
    li x11, 0x0                  // a1
    li x12, 0x0                  // a2
    li x13, 0x801806b6           // a3
    li x14, 0x0                  // a4
    li x15, 0x6000               // a5
    li x16, 0x801805ff           // a6
    li x17, 0xf06                // a7
    li x18, 0xf069178c           // s2
    li x19, 0x8018054b0000000    // s3
    li x20, 0x7ffffad3           // s4
    li x21, 0x80000447           // s5
    li x22, 0x801ff60a           // s6
    li x23, 0xc53d07bc           // s7
    li x24, 0x2006               // s8
    li x25, 0xd2000ed3           // s9
    li x26, 0x2864d768           // s10
    li x27, 0x801ffb76           // s11
    li x28, 0xffffffff7fe00f0f   // t3
    li x29, 0x1                  // t4
    li x30, 0x8017fad6           // t5
    li x31, 0x7ffff661           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x17'}, 'clob': {'x14', 'f15', 'x17'}})
    
    li x14, 0x1ffffc
    and x17, x17, x14
    li x14, 0x800000cf
    add x17, x17, x14
    flw f15, -0xcf(x17)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f15                 0x2813836133322c49(1.238084287307389e-115_d)    0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f15, -0xcf(x17)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f15                 0x2813836133322c49(1.238084287307389e-115_d)    0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f15, x17
a7(x17)             0x0000000080000fd3(2147487699)                  0x0000000080000fd3(2147487699)
f15                 0x2813836133322c49(1.238084287307389e-115_d)    0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080200d84(2149584260)                  0x0000000080200d84(2149584260)                  
sp(x2)              0xffffffffffe798a8(18446744073707952296)        0xffffffffffe798a8(18446744073707952296)        
gp(x3)              0x00000000801860a5(2149081253)                  0x00000000801860a5(2149081253)                  
tp(x4)              0x00000000800001dd(2147484125)                  0x00000000800001dd(2147484125)                  
t0(x5)              0x00000000801ff306(2149577478)                  0x00000000801ff306(2149577478)                  
t1(x6)              0x0000000000000100(256)                         0x0000000000000100(256)                         
t2(x7)              0x0000000080180700(2149058304)                  0x0000000080180700(2149058304)                  
fp(x8)              0x000000008018054b(2149057867)                  0x000000008018054b(2149057867)                  
s1(x9)              0x000000007ffff94d(2147481933)                  0x000000007ffff94d(2147481933)                  
a0(x10)             0x000000008017f823(2149054499)                  0x000000008017f823(2149054499)                  
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x00000000801806b6(2149058230)                  0x00000000801806b6(2149058230)                  
a4(x14)             0x00000000800000cf(2147483855)                  0x00000000800000cf(2147483855)                  
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x00000000801805ff(2149058047)                  0x00000000801805ff(2149058047)                  
a7(x17)             0x0000000080000fd3(2147487699)                  0x0000000080000fd3(2147487699)                  
s2(x18)             0x00000000f069178c(4033419148)                  0x00000000f069178c(4033419148)                  
s3(x19)             0x08018054b0000000(576883328498532352)          0x08018054b0000000(576883328498532352)          
s4(x20)             0x000000007ffffad3(2147482323)                  0x000000007ffffad3(2147482323)                  
s5(x21)             0x0000000080000447(2147484743)                  0x0000000080000447(2147484743)                  
s6(x22)             0x00000000801ff60a(2149578250)                  0x00000000801ff60a(2149578250)                  
s7(x23)             0x00000000c53d07bc(3309111228)                  0x00000000c53d07bc(3309111228)                  
s8(x24)             0x0000000000002006(8198)                        0x0000000000002006(8198)                        
s9(x25)             0x00000000d2000ed3(3523219155)                  0x00000000d2000ed3(3523219155)                  
s10(x26)            0x000000002864d768(677697384)                   0x000000002864d768(677697384)                   
s11(x27)            0x00000000801ffb76(2149579638)                  0x00000000801ffb76(2149579638)                  
t3(x28)             0xffffffff7fe00f0f(18446744071559974671)        0xffffffff7fe00f0f(18446744071559974671)        
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x000000008017fad6(2149055190)                  0x000000008017fad6(2149055190)                  
t6(x31)             0x000000007ffff661(2147481185)                  0x000000007ffff661(2147481185)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            8678f1452537dfca8e3a558142e0ed30c1493c20        8678f1452537dfca8e3a558142e0ed30c1493c20        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000780(2147485568)                  0x0000000080000780(2147485568)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000f0(240)                         0x00000000000000f0(240)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            dyn(0b111)                                      dyn(0b111)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x27423a2e4f82795a(1.4117355022935317e-119_d)   0x27423a2e4f82795a(1.4117355022935317e-119_d)   
f2                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x6d0e119bad5462d6(2.073111797459765e+217_d)    0x6d0e119bad5462d6(2.073111797459765e+217_d)    
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0xc6219bf4967cddd7(-6.97572313911571e+29_d)     0xc6219bf4967cddd7(-6.97572313911571e+29_d)     
f10                 0x2813836133322c49(1.238084287307389e-115_d)    0x2813836133322c49(1.238084287307389e-115_d)    
f11                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x2813836133322c49(1.238084287307389e-115_d)    0xffffffff00000000(0.0_s)                       X
f16                 0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f17                 0x00000000000000e0(1.107e-321_d)                0x00000000000000e0(1.107e-321_d)                
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0x04dde55e8e4137d9(3.1413536184395884e-285_d)   0x04dde55e8e4137d9(3.1413536184395884e-285_d)   
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff80000000(-0.0_s)                      0xffffffff80000000(-0.0_s)                      
f24                 0x7fffffff4f000003(nan_d)                       0x7fffffff4f000003(nan_d)                       
f25                 0xc2f16eb27ac644b0(-306674215445579.0_d)        0xc2f16eb27ac644b0(-306674215445579.0_d)        
f26                 0xecf89bc3f7a9d08d(-8.483231402566356e+216_d)   0xecf89bc3f7a9d08d(-8.483231402566356e+216_d)   
f27                 0xffffffff4f000003(2147484416.0_s)              0xffffffff4f000003(2147484416.0_s)              
f28                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff8017fe39(-2.2034143169905213e-39_s)   0xffffffff8017fe39(-2.2034143169905213e-39_s)   
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

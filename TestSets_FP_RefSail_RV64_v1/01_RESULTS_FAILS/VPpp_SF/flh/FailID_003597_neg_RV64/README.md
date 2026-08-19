# FailID_003597 VP++ SF neg RV64 flh

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3597
* Isolated failing instruction: `flh`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x01,0x00,0x20,0x00,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x40,0xfb,0x00,0x00,0xe0,0x41
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x30,0x40
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f18:.byte 0x00,0x00,0x80,0xe1,0xe6,0xc2,0xe8,0x41
_reg_f19:.byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x71
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xffffffffffffffff    // ra
    li x2, 0x0                   // sp
    li x3, 0x80180620            // gp
    li x4, 0x0                   // tp
    li x5, 0x8017fb42            // t0
    li x6, 0x0                   // t1
    li x7, 0x8017fd89            // t2
    li x8, 0x7fffffff            // fp
    li x9, 0x8017ff9f            // s1
    li x10, 0x80185b42           // a0
    li x11, 0x0                  // a1
    li x12, 0x60                 // a2
    li x13, 0x1                  // a3
    li x14, 0x8017fa61           // a4
    li x15, 0x801fa5f0           // a5
    li x16, 0x71                 // a6
    li x17, 0x2cd5f000           // a7
    li x18, 0x80005cf7           // s2
    li x19, 0x800006f4           // s3
    li x20, 0x80000516           // s4
    li x21, 0x0                  // s5
    li x22, 0x0                  // s6
    li x23, 0x200001             // s7
    li x24, 0x8000019f           // s8
    li x25, 0x85                 // s9
    li x26, 0x200                // s10
    li x27, 0x8017fc9c           // s11
    li x28, 0x0                  // t3
    li x29, 0xf3                 // t4
    li x30, 0x800007da           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x8'}, 'clob': {'x9', 'x8', 'f25'}})
    
    li x9, 0x1ffffe
    and x8, x8, x9
    li x9, 0x7ffffcda
    add x8, x8, x9
    flh f25, 0x326(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f25                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flh f25, 0x326(x8)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'inexact'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f25                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, x326, x8
fp(x8)              0x00000000801ffcd8(2149579992)                  0x00000000801ffcd8(2149579992)
f25                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000080180620(2149058080)                  0x0000000080180620(2149058080)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x000000008017fb42(2149055298)                  0x000000008017fb42(2149055298)                  
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x000000008017fd89(2149055881)                  0x000000008017fd89(2149055881)                  
fp(x8)              0x00000000801ffcd8(2149579992)                  0x00000000801ffcd8(2149579992)                  
s1(x9)              0x000000007ffffcda(2147482842)                  0x000000007ffffcda(2147482842)                  
a0(x10)             0x0000000080185b42(2149079874)                  0x0000000080185b42(2149079874)                  
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x0000000000000060(96)                          0x0000000000000060(96)                          
a3(x13)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a4(x14)             0x000000008017fa61(2149055073)                  0x000000008017fa61(2149055073)                  
a5(x15)             0x00000000801fa5f0(2149557744)                  0x00000000801fa5f0(2149557744)                  
a6(x16)             0x0000000000000071(113)                         0x0000000000000071(113)                         
a7(x17)             0x000000002cd5f000(752218112)                   0x000000002cd5f000(752218112)                   
s2(x18)             0x0000000080005cf7(2147507447)                  0x0000000080005cf7(2147507447)                  
s3(x19)             0x00000000800006f4(2147485428)                  0x00000000800006f4(2147485428)                  
s4(x20)             0x0000000080000516(2147484950)                  0x0000000080000516(2147484950)                  
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000000200001(2097153)                     0x0000000000200001(2097153)                     
s8(x24)             0x000000008000019f(2147484063)                  0x000000008000019f(2147484063)                  
s9(x25)             0x0000000000000085(133)                         0x0000000000000085(133)                         
s10(x26)            0x0000000000000200(512)                         0x0000000000000200(512)                         
s11(x27)            0x000000008017fc9c(2149055644)                  0x000000008017fc9c(2149055644)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x00000000000000f3(243)                         0x00000000000000f3(243)                         
t5(x30)             0x00000000800007da(2147485658)                  0x00000000800007da(2147485658)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            f54f4e7c70926a9fd3d25018b97d09ebed62fef7        f54f4e7c70926a9fd3d25018b97d09ebed62fef7        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000724(2147485476)                  0x0000000080000724(2147485476)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000071(113)                         0x0000000000000071(113)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff00200001(2.938737278354183e-39_s)     0xffffffff00200001(2.938737278354183e-39_s)     
f12                 0x41e00000fb400000(2147485658.0_d)              0x41e00000fb400000(2147485658.0_d)              
f13                 0x4030000000000000(16.0_d)                      0x4030000000000000(16.0_d)                      
f14                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f17                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f18                 0x41e8c2e6e1800000(3323410188.0_d)              0x41e8c2e6e1800000(3323410188.0_d)              
f19                 0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
STATES DIFFER: True
```

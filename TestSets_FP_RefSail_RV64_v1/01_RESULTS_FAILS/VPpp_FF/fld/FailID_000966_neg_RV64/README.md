# FailID_000966 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 966
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x58,0xfb,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x01,0x20,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x60,0xc5,0x00,0x00,0xe0,0x41
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x60,0xd5,0x0a,0x03,0xe0,0x41
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x43
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0xc9,0x41,0x6b,0xd3,0x41
_reg_f25:.byte 0x00,0x00,0xc0,0x23,0x00,0x04,0xe0,0x41
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x60,0xd5,0x0a,0x03,0xe0,0x41
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x28
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801fcd2e            // ra
    li x2, 0x91f3                // sp
    li x3, 0x80000a4a            // gp
    li x4, 0x0                   // tp
    li x5, 0x8017fa55            // t0
    li x6, 0x8018037c            // t1
    li x7, 0x800006b0            // t2
    li x8, 0x4727a000            // fp
    li x9, 0x800006b0            // s1
    li x10, 0x80180032           // a0
    li x11, 0x80000789           // a1
    li x12, 0x80000790           // a2
    li x13, 0x800067d0           // a3
    li x14, 0x800003e0           // a4
    li x15, 0x8018037c           // a5
    li x16, 0x80180110           // a6
    li x17, 0xffffffff7fe001be   // a7
    li x18, 0x80000167           // s2
    li x19, 0x0                  // s3
    li x20, 0x0                  // s4
    li x21, 0x100180b0c          // s5
    li x22, 0x1003006f8          // s6
    li x23, 0x800005d9           // s7
    li x24, 0x80195c60           // s8
    li x25, 0x4676378c           // s9
    li x26, 0xb0                 // s10
    li x27, 0x200019f4000        // s11
    li x28, 0x80180696           // t3
    li x29, 0x80000662           // t4
    li x30, 0x0                  // t5
    li x31, 0x8f                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x30', 'mstatus.fs/vs.fs'}, 'clob': {'x30', 'f25', 'x15'}})
    
    li x15, 0x1ffff8
    and x30, x30, x15
    li x15, 0x7ffffe0f
    add x30, x30, x15
    fld f25, 0x1f1(x30)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f25                 0x41e0040023c00000(2149581086.0_d)              0x000000132140006f(4.05935308646e-313_d)        X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f25, 0x1f1(x30)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f25                 0x41e0040023c00000(2149581086.0_d)              0x000000132140006f(4.05935308646e-313_d)        X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, x1, f1, x30
ra(x1)              0x00000000801fcd2e(2149567790)                  0x00000000801fcd2e(2149567790)
t5(x30)             0x000000007ffffe0f(2147483151)                  0x000000007ffffe0f(2147483151)
f1                  0xffffffff8017fb58(-2.202381560022314e-39_s)    0xffffffff8017fb58(-2.202381560022314e-39_s)
f25                 0x41e0040023c00000(2149581086.0_d)              0x000000132140006f(4.05935308646e-313_d)        X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801fcd2e(2149567790)                  0x00000000801fcd2e(2149567790)                  
sp(x2)              0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
gp(x3)              0x0000000080000a4a(2147486282)                  0x0000000080000a4a(2147486282)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x000000008017fa55(2149055061)                  0x000000008017fa55(2149055061)                  
t1(x6)              0x000000008018037c(2149057404)                  0x000000008018037c(2149057404)                  
t2(x7)              0x00000000800006b0(2147485360)                  0x00000000800006b0(2147485360)                  
fp(x8)              0x000000004727a000(1193779200)                  0x000000004727a000(1193779200)                  
s1(x9)              0x00000000800006b0(2147485360)                  0x00000000800006b0(2147485360)                  
a0(x10)             0x0000000080180032(2149056562)                  0x0000000080180032(2149056562)                  
a1(x11)             0x0000000080000789(2147485577)                  0x0000000080000789(2147485577)                  
a2(x12)             0x0000000080000790(2147485584)                  0x0000000080000790(2147485584)                  
a3(x13)             0x00000000800067d0(2147510224)                  0x00000000800067d0(2147510224)                  
a4(x14)             0x00000000800003e0(2147484640)                  0x00000000800003e0(2147484640)                  
a5(x15)             0x000000007ffffe0f(2147483151)                  0x000000007ffffe0f(2147483151)                  
a6(x16)             0x0000000080180110(2149056784)                  0x0000000080180110(2149056784)                  
a7(x17)             0xffffffff7fe001be(18446744071559971262)        0xffffffff7fe001be(18446744071559971262)        
s2(x18)             0x0000000080000167(2147484007)                  0x0000000080000167(2147484007)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x0000000100180b0c(4296542988)                  0x0000000100180b0c(4296542988)                  
s6(x22)             0x00000001003006f8(4298114808)                  0x00000001003006f8(4298114808)                  
s7(x23)             0x00000000800005d9(2147485145)                  0x00000000800005d9(2147485145)                  
s8(x24)             0x0000000080195c60(2149145696)                  0x0000000080195c60(2149145696)                  
s9(x25)             0x000000004676378c(1182152588)                  0x000000004676378c(1182152588)                  
s10(x26)            0x00000000000000b0(176)                         0x00000000000000b0(176)                         
s11(x27)            0x00000200019f4000(2199050469376)               0x00000200019f4000(2199050469376)               
t3(x28)             0x0000000080180696(2149058198)                  0x0000000080180696(2149058198)                  
t4(x29)             0x0000000080000662(2147485282)                  0x0000000080000662(2147485282)                  
t5(x30)             0x000000007ffffe0f(2147483151)                  0x000000007ffffe0f(2147483151)                  
t6(x31)             0x000000000000008f(143)                         0x000000000000008f(143)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            0521884eeaed02a996560a9ee38ac21dd86b61e4        0521884eeaed02a996560a9ee38ac21dd86b61e4        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000778(2147485560)                  0x0000000080000778(2147485560)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000028(40)                          0x0000000000000028(40)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff8017fb58(-2.202381560022314e-39_s)    0xffffffff8017fb58(-2.202381560022314e-39_s)    
f2                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f3                  0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff4f002001(2149581056.0_s)              0xffffffff4f002001(2149581056.0_s)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0x41e00000c5600000(2147485227.0_d)              0x41e00000c5600000(2147485227.0_d)              
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f16                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x41e0030ad5600000(2149078699.0_d)              0x41e0030ad5600000(2149078699.0_d)              
f20                 0x43f0000000000000(1.8446744073709552e+19_d)    0x43f0000000000000(1.8446744073709552e+19_d)    
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x41d36b41c9000000(1303185188.0_d)              0x41d36b41c9000000(1303185188.0_d)              
f25                 0x41e0040023c00000(2149581086.0_d)              0x000000132140006f(4.05935308646e-313_d)        X
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x41e0030ad5600000(2149078699.0_d)              0x41e0030ad5600000(2149078699.0_d)              
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

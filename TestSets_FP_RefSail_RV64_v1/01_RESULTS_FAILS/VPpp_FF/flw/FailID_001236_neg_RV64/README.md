# FailID_001236 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1236
* Isolated failing instruction: `flw`
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
_reg_f0: .byte 0xd7,0x6d,0x3f,0x92,0x80,0x30,0x29,0xa8
_reg_f1: .byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x00,0x00,0xed,0xcc,0x6b,0xea,0x41
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f6: .byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x0b,0x8a,0xae,0x7b,0x89,0x93,0x2c,0x06
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x0b,0x8a,0xae,0x7b,0x89,0x93,0x2c,0x06
_reg_f13:.byte 0xd4,0x26,0x42,0xed,0x0d,0x68,0x56,0xf7
_reg_f14:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x8d,0x30,0xe2,0x54,0xa5,0x5d,0x2f,0x48
_reg_f20:.byte 0xac,0xd7,0xef,0x99,0xc8,0x1c,0x81,0x62
_reg_f21:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0xd4,0x26,0x42,0xed,0x0d,0x68,0x56,0xf7
_reg_f24:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f25:.byte 0x1d,0xb7,0x27,0x2d,0xb2,0x99,0x1d,0xbe
_reg_f26:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x12,0xa1,0xea,0x71,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': True, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x3d
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x2                   // sp
    li x3, 0x7ffffb37            // gp
    li x4, 0x0                   // tp
    li x5, 0xffffffff8bba4000    // t0
    li x6, 0x0                   // t1
    li x7, 0x40                  // t2
    li x8, 0x1e3                 // fp
    li x9, 0x1                   // s1
    li x10, 0xd35e6768           // a0
    li x11, 0x100300df20000      // a1
    li x12, 0x6000               // a2
    li x13, 0x0                  // a3
    li x14, 0x6000               // a4
    li x15, 0x2006fe             // a5
    li x16, 0x7ffff817           // a6
    li x17, 0x8017fa48           // a7
    li x18, 0x8003f476           // s2
    li x19, 0x80200171           // s3
    li x20, 0x6000               // s4
    li x21, 0x0                  // s5
    li x22, 0x8017f91d           // s6
    li x23, 0x1                  // s7
    li x24, 0x80180375           // s8
    li x25, 0xffffffffffffffff   // s9
    li x26, 0x800003fa           // s10
    li x27, 0x801806f9           // s11
    li x28, 0x0                  // t3
    li x29, 0xffffffffffc65ce0   // t4
    li x30, 0xe2                 // t5
    li x31, 0x8011e087           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x8', 'mstatus.fs/vs.fs'}, 'clob': {'x8', 'f10', 'x14'}})
    
    li x14, 0x1ffffc
    and x8, x8, x14
    li x14, 0x7ffffbcc
    add x8, x8, x14
    flw f10, 0x434(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f10                 0xffffffffffc00000(nan_s)                       0xffffffff0281b383(1.905788108049426e-37_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f10, 0x434(x8)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f10                 0xffffffffffc00000(nan_s)                       0xffffffff0281b383(1.905788108049426e-37_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f10, x434, x8
fp(x8)              0x000000007ffffdac(2147483052)                  0x000000007ffffdac(2147483052)
f10                 0xffffffffffc00000(nan_s)                       0xffffffff0281b383(1.905788108049426e-37_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x0000000000000002(2)                           0x0000000000000002(2)                           
gp(x3)              0x000000007ffffb37(2147482423)                  0x000000007ffffb37(2147482423)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0xffffffff8bba4000(18446744071758823424)        0xffffffff8bba4000(18446744071758823424)        
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000000000040(64)                          0x0000000000000040(64)                          
fp(x8)              0x000000007ffffdac(2147483052)                  0x000000007ffffdac(2147483052)                  
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x00000000d35e6768(3546179432)                  0x00000000d35e6768(3546179432)                  
a1(x11)             0x000100300df20000(281681369104384)             0x000100300df20000(281681369104384)             
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x000000007ffffbcc(2147482572)                  0x000000007ffffbcc(2147482572)                  
a5(x15)             0x00000000002006fe(2098942)                     0x00000000002006fe(2098942)                     
a6(x16)             0x000000007ffff817(2147481623)                  0x000000007ffff817(2147481623)                  
a7(x17)             0x000000008017fa48(2149055048)                  0x000000008017fa48(2149055048)                  
s2(x18)             0x000000008003f476(2147742838)                  0x000000008003f476(2147742838)                  
s3(x19)             0x0000000080200171(2149581169)                  0x0000000080200171(2149581169)                  
s4(x20)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x000000008017f91d(2149054749)                  0x000000008017f91d(2149054749)                  
s7(x23)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s8(x24)             0x0000000080180375(2149057397)                  0x0000000080180375(2149057397)                  
s9(x25)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s10(x26)            0x00000000800003fa(2147484666)                  0x00000000800003fa(2147484666)                  
s11(x27)            0x00000000801806f9(2149058297)                  0x00000000801806f9(2149058297)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0xffffffffffc65ce0(18446744073705774304)        0xffffffffffc65ce0(18446744073705774304)        
t5(x30)             0x00000000000000e2(226)                         0x00000000000000e2(226)                         
t6(x31)             0x000000008011e087(2148655239)                  0x000000008011e087(2148655239)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            ba12466e8cd6ad141cd94ea453e3792e17482b5d        ba12466e8cd6ad141cd94ea453e3792e17482b5d        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000714(2147485460)                  0x0000000080000714(2147485460)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000003d(61)                          0x000000000000003d(61)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xa8293080923f6dd7(-3.1964694534197797e-115_d)  0xa8293080923f6dd7(-3.1964694534197797e-115_d)  
f1                  0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f2                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f3                  0x41ea6bcced000000(3546179432.0_d)              0x41ea6bcced000000(3546179432.0_d)              
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f6                  0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f7                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f8                  0x062c93897bae8a0b(6.297095454849657e-279_d)    0x062c93897bae8a0b(6.297095454849657e-279_d)    
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffffffc00000(nan_s)                       0xffffffff0281b383(1.905788108049426e-37_s)     X
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x062c93897bae8a0b(6.297095454849657e-279_d)    0x062c93897bae8a0b(6.297095454849657e-279_d)    
f13                 0xf756680ded4226d4(-7.224860598141725e+266_d)   0xf756680ded4226d4(-7.224860598141725e+266_d)   
f14                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x482f5da554e2308d(5.3366150143908725e+39_d)    0x482f5da554e2308d(5.3366150143908725e+39_d)    
f20                 0x62811cc899efd7ac(3.153402842233095e+166_d)    0x62811cc899efd7ac(3.153402842233095e+166_d)    
f21                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xf756680ded4226d4(-7.224860598141725e+266_d)   0xf756680ded4226d4(-7.224860598141725e+266_d)   
f24                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f25                 0xbe1d99b22d27b71d(-1.7229685912554313e-09_d)   0xbe1d99b22d27b71d(-1.7229685912554313e-09_d)   
f26                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f30                 0xffffffff71eaa112(2.3236548594479806e+30_s)    0xffffffff71eaa112(2.3236548594479806e+30_s)    
f31                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
STATES DIFFER: True
```

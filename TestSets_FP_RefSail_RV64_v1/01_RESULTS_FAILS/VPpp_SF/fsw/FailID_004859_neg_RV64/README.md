# FailID_004859 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4859
* Isolated failing instruction: `fsw`
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f2: .byte 0x00,0x00,0xd0,0x42,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f6: .byte 0x00,0x00,0x00,0xfc,0xfa,0x87,0xae,0xc1
_reg_f7: .byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x02,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xfa,0x27,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xfa,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0x40,0xfb,0xff,0xff,0xdf,0x41
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x80,0x46,0x00,0x00,0xe0,0x41
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x63,0x40
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x41
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x400c2f960000000     // ra
    li x2, 0x100                 // sp
    li x3, 0x8017fbc2            // gp
    li x4, 0x68                  // tp
    li x5, 0x80180ada            // t0
    li x6, 0x800000c7            // t1
    li x7, 0x801ff8ef            // t2
    li x8, 0x801803ce            // fp
    li x9, 0xfe75800000000000    // s1
    li x10, 0x8017f8e2           // a0
    li x11, 0x1                  // a1
    li x12, 0x8017fef0           // a2
    li x13, 0xd5                 // a3
    li x14, 0x8f                 // a4
    li x15, 0x800002fa           // a5
    li x16, 0x1                  // a6
    li x17, 0x801805f2           // a7
    li x18, 0x1f                 // s2
    li x19, 0x8017fd2d           // s3
    li x20, 0x800                // s4
    li x21, 0x801802df           // s5
    li x22, 0xa6                 // s6
    li x23, 0x8017fceb           // s7
    li x24, 0x7ffffc21           // s8
    li x25, 0xffffffffffffffff   // s9
    li x26, 0x8017fcfe           // s10
    li x27, 0xffffffff82d4f000   // s11
    li x28, 0x6000               // t3
    li x29, 0x45                 // t4
    li x30, 0x8017ff2c           // t5
    li x31, 0x1a652001           // t6
    // INSTRUCTION ({'dep': {'x12', 'fcsr.rm', 'f8', 'mstatus.fs/vs.fs'}, 'clob': {'x12', 'x5'}})
    
    li x5, 0xffffc
    and x12, x12, x5
    li x5, 0x801802bf
    add x12, x12, x5
    fsw f8, -0x2bf(x12)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        f976c907a0490aabff0a9a44bca05cb4d05e6b3f        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f8, -0x2bf(x12)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        f976c907a0490aabff0a9a44bca05cb4d05e6b3f        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x2, x12
sp(x2)              0x0000000000000100(256)                         0x0000000000000100(256)
a2(x12)             0x00000000802001af(2149581231)                  0x00000000802001af(2149581231)
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0400c2f960000000(288444752464969728)          0x0400c2f960000000(288444752464969728)          
sp(x2)              0x0000000000000100(256)                         0x0000000000000100(256)                         
gp(x3)              0x000000008017fbc2(2149055426)                  0x000000008017fbc2(2149055426)                  
tp(x4)              0x0000000000000068(104)                         0x0000000000000068(104)                         
t0(x5)              0x00000000801802bf(2149057215)                  0x00000000801802bf(2149057215)                  
t1(x6)              0x00000000800000c7(2147483847)                  0x00000000800000c7(2147483847)                  
t2(x7)              0x00000000801ff8ef(2149578991)                  0x00000000801ff8ef(2149578991)                  
fp(x8)              0x00000000801803ce(2149057486)                  0x00000000801803ce(2149057486)                  
s1(x9)              0xfe75800000000000(18335702195397197824)        0xfe75800000000000(18335702195397197824)        
a0(x10)             0x000000008017f8e2(2149054690)                  0x000000008017f8e2(2149054690)                  
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x00000000802001af(2149581231)                  0x00000000802001af(2149581231)                  
a3(x13)             0x00000000000000d5(213)                         0x00000000000000d5(213)                         
a4(x14)             0x000000000000008f(143)                         0x000000000000008f(143)                         
a5(x15)             0x00000000800002fa(2147484410)                  0x00000000800002fa(2147484410)                  
a6(x16)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a7(x17)             0x00000000801805f2(2149058034)                  0x00000000801805f2(2149058034)                  
s2(x18)             0x000000000000001f(31)                          0x000000000000001f(31)                          
s3(x19)             0x000000008017fd2d(2149055789)                  0x000000008017fd2d(2149055789)                  
s4(x20)             0x0000000000000800(2048)                        0x0000000000000800(2048)                        
s5(x21)             0x00000000801802df(2149057247)                  0x00000000801802df(2149057247)                  
s6(x22)             0x00000000000000a6(166)                         0x00000000000000a6(166)                         
s7(x23)             0x000000008017fceb(2149055723)                  0x000000008017fceb(2149055723)                  
s8(x24)             0x000000007ffffc21(2147482657)                  0x000000007ffffc21(2147482657)                  
s9(x25)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s10(x26)            0x000000008017fcfe(2149055742)                  0x000000008017fcfe(2149055742)                  
s11(x27)            0xffffffff82d4f000(18446744071609577472)        0xffffffff82d4f000(18446744071609577472)        
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x0000000000000045(69)                          0x0000000000000045(69)                          
t5(x30)             0x000000008017ff2c(2149056300)                  0x000000008017ff2c(2149056300)                  
t6(x31)             0x000000001a652001(442834945)                   0x000000001a652001(442834945)                   

STATE               REF                                             DUT                                             DIFF
xmemhash            02cff2cf1cffb60116cb41329e926d02b793725b        02cff2cf1cffb60116cb41329e926d02b793725b        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        f976c907a0490aabff0a9a44bca05cb4d05e6b3f        X
lastPC              0x000000008000074c(2147485516)                  0x000000008000074c(2147485516)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000041(65)                          0x0000000000000041(65)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f2                  0xffffffff42d00000(104.0_s)                     0xffffffff42d00000(104.0_s)                     
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f6                  0xc1ae87fafc000000(-256114046.0_d)              0xc1ae87fafc000000(-256114046.0_d)              
f7                  0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff4f000002(2147484160.0_s)              0xffffffff4f000002(2147484160.0_s)              
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff4f0027fa(2150103552.0_s)              0xffffffff4f0027fa(2150103552.0_s)              
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff4f0017fa(2149054976.0_s)              0xffffffff4f0017fa(2149054976.0_s)              
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0x41dffffffb400000(2147483629.0_d)              0x41dffffffb400000(2147483629.0_d)              
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x41e0000046800000(2147484212.0_d)              0x41e0000046800000(2147484212.0_d)              
f30                 0x4063000000000000(152.0_d)                     0x4063000000000000(152.0_d)                     
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

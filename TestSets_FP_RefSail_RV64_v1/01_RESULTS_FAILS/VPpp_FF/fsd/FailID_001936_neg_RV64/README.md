# FailID_001936 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1936
* Isolated failing instruction: `fsd`
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
_reg_f0: .byte 0x00,0x00,0x00,0xe9,0xfe,0x02,0xe0,0x41
_reg_f1: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x80
_reg_f7: .byte 0x6d,0x01,0x00,0x80,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f9: .byte 0xf4,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f15:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xf4,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x48,0xf7,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x36,0xf8,0x17,0x80,0x00,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'res0(0b101)', 'res': 0}
    li t0, 0xa8
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801fa900            // ra
    li x2, 0x400bf8b4            // sp
    li x3, 0x1                   // gp
    li x4, 0x801801cf            // tp
    li x5, 0x80180498            // t0
    li x6, 0x7fffffe7            // t1
    li x7, 0x8000079a            // t2
    li x8, 0xffffffffd4206000    // fp
    li x9, 0x13                  // s1
    li x10, 0x0                  // a0
    li x11, 0x2005f              // a1
    li x12, 0x8009d259           // a2
    li x13, 0x7ffffeff           // a3
    li x14, 0x92                 // a4
    li x15, 0x7ffff900           // a5
    li x16, 0x0                  // a6
    li x17, 0xe94e6758           // a7
    li x18, 0x0                  // s2
    li x19, 0x8000015d           // s3
    li x20, 0x8017f80d           // s4
    li x21, 0x80000259           // s5
    li x22, 0x0                  // s6
    li x23, 0xffffff             // s7
    li x24, 0x8017f168           // s8
    li x25, 0x800007b7           // s9
    li x26, 0x0                  // s10
    li x27, 0x8017f168           // s11
    li x28, 0x8000079a           // t3
    li x29, 0x8017fe57           // t4
    li x30, 0x86                 // t5
    li x31, 0x6000               // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f13', 'mstatus.fs/vs.fs', 'x13'}, 'clob': {'x13', 'x16'}})
    
    li x16, 0xffff8
    and x13, x13, x16
    li x16, 0x8017feb3
    add x13, x13, x16
    fsd f13, 0x14d(x13)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c63a236b22359c158e29582ceb49fa56f1f194c4        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f13, 0x14d(x13)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c63a236b22359c158e29582ceb49fa56f1f194c4        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x14, x13
a3(x13)             0x000000008027fdab(2150104491)                  0x000000008027fdab(2150104491)
a4(x14)             0x0000000000000092(146)                         0x0000000000000092(146)
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801fa900(2149558528)                  0x00000000801fa900(2149558528)                  
sp(x2)              0x00000000400bf8b4(1074526388)                  0x00000000400bf8b4(1074526388)                  
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x00000000801801cf(2149056975)                  0x00000000801801cf(2149056975)                  
t0(x5)              0x0000000080180498(2149057688)                  0x0000000080180498(2149057688)                  
t1(x6)              0x000000007fffffe7(2147483623)                  0x000000007fffffe7(2147483623)                  
t2(x7)              0x000000008000079a(2147485594)                  0x000000008000079a(2147485594)                  
fp(x8)              0xffffffffd4206000(18446744072973475840)        0xffffffffd4206000(18446744072973475840)        
s1(x9)              0x0000000000000013(19)                          0x0000000000000013(19)                          
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x000000000002005f(131167)                      0x000000000002005f(131167)                      
a2(x12)             0x000000008009d259(2148127321)                  0x000000008009d259(2148127321)                  
a3(x13)             0x000000008027fdab(2150104491)                  0x000000008027fdab(2150104491)                  
a4(x14)             0x0000000000000092(146)                         0x0000000000000092(146)                         
a5(x15)             0x000000007ffff900(2147481856)                  0x000000007ffff900(2147481856)                  
a6(x16)             0x000000008017feb3(2149056179)                  0x000000008017feb3(2149056179)                  
a7(x17)             0x00000000e94e6758(3914229592)                  0x00000000e94e6758(3914229592)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000008000015d(2147483997)                  0x000000008000015d(2147483997)                  
s4(x20)             0x000000008017f80d(2149054477)                  0x000000008017f80d(2149054477)                  
s5(x21)             0x0000000080000259(2147484249)                  0x0000000080000259(2147484249)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000000ffffff(16777215)                    0x0000000000ffffff(16777215)                    
s8(x24)             0x000000008017f168(2149052776)                  0x000000008017f168(2149052776)                  
s9(x25)             0x00000000800007b7(2147485623)                  0x00000000800007b7(2147485623)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000008017f168(2149052776)                  0x000000008017f168(2149052776)                  
t3(x28)             0x000000008000079a(2147485594)                  0x000000008000079a(2147485594)                  
t4(x29)             0x000000008017fe57(2149056087)                  0x000000008017fe57(2149056087)                  
t5(x30)             0x0000000000000086(134)                         0x0000000000000086(134)                         
t6(x31)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       

STATE               REF                                             DUT                                             DIFF
xmemhash            a256e8a48ea60a68e7c33e82ab49df42bae7f99e        a256e8a48ea60a68e7c33e82ab49df42bae7f99e        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c63a236b22359c158e29582ceb49fa56f1f194c4        X
lastPC              0x0000000080000744(2147485508)                  0x0000000080000744(2147485508)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000a8(168)                         0x00000000000000a8(168)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            res0(0b101)                                     res0(0b101)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x41e002fee9000000(2149054280.0_d)              0x41e002fee9000000(2149054280.0_d)              
f1                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x8000000000000000(-0.0_d)                      0x8000000000000000(-0.0_d)                      
f7                  0x000000008000016d(1.060998076e-314_d)          0x000000008000016d(1.060998076e-314_d)          
f8                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f9                  0xffffffff4efffff4(2147482112.0_s)              0xffffffff4efffff4(2147482112.0_s)              
f10                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f15                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff4efffff4(2147482112.0_s)              0xffffffff4efffff4(2147482112.0_s)              
f22                 0xffffffff8017f748(-2.200924209619416e-39_s)    0xffffffff8017f748(-2.200924209619416e-39_s)    
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x000000008017f836(1.0617740084e-314_d)         0x000000008017f836(1.0617740084e-314_d)         
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

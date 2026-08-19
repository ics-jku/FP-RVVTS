# FailID_002387 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2387
* Isolated failing instruction: `fsw`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x40,0xdd,0xff,0x02,0xe0,0xc1
_reg_f4: .byte 0x52,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x30,0x4a,0xe0,0xd2,0xc1
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x44,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x96,0x00,0x04,0xe0,0x41
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0xd7,0x9f,0x73,0x00,0x00,0x00,0x00
_reg_f19:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x03,0xb3,0x01,0x02,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x04,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x40,0x35,0x00,0x03,0xe0,0x41
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x42
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801ff983            // ra
    li x2, 0xffffffffffff91f3    // sp
    li x3, 0x8017fe91            // gp
    li x4, 0x8017feb1            // tp
    li x5, 0x8018019f            // t0
    li x6, 0x8017f831            // t1
    li x7, 0x8018014e            // t2
    li x8, 0x0                   // fp
    li x9, 0x5a                  // s1
    li x10, 0x1                  // a0
    li x11, 0x3e                 // a1
    li x12, 0x801803e4           // a2
    li x13, 0xf3                 // a3
    li x14, 0x801803e4           // a4
    li x15, 0x7ffffb08           // a5
    li x16, 0x80185e1b           // a6
    li x17, 0x5c                 // a7
    li x18, 0x800005f9           // s2
    li x19, 0x8017ff9d           // s3
    li x20, 0x7ffffa41           // s4
    li x21, 0x0                  // s5
    li x22, 0x0                  // s6
    li x23, 0x800002c0           // s7
    li x24, 0x1                  // s8
    li x25, 0x801ffdc8           // s9
    li x26, 0x8017fdd3           // s10
    li x27, 0x801ff902           // s11
    li x28, 0x800004f9           // t3
    li x29, 0x1                  // t4
    li x30, 0x0                  // t5
    li x31, 0x80000218           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f25', 'x15'}, 'clob': {'x24', 'x15'}})
    
    li x24, 0xffffc
    and x15, x15, x24
    li x24, 0x8017fcbb
    add x15, x15, x24
    fsw f25, 0x345(x15)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        4167bd4ce44d1cbbc933b1f39985b50a566ff66f        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f25, 0x345(x15)
+========================================================================================================================+
Attributes:  fcsr ['underflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        4167bd4ce44d1cbbc933b1f39985b50a566ff66f        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, x345, x15
a5(x15)             0x000000008027f7c3(2150102979)                  0x000000008027f7c3(2150102979)
f25                 0xffffffff4f001804(2149057536.0_s)              0xffffffff4f001804(2149057536.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801ff983(2149579139)                  0x00000000801ff983(2149579139)                  
sp(x2)              0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)        
gp(x3)              0x000000008017fe91(2149056145)                  0x000000008017fe91(2149056145)                  
tp(x4)              0x000000008017feb1(2149056177)                  0x000000008017feb1(2149056177)                  
t0(x5)              0x000000008018019f(2149056927)                  0x000000008018019f(2149056927)                  
t1(x6)              0x000000008017f831(2149054513)                  0x000000008017f831(2149054513)                  
t2(x7)              0x000000008018014e(2149056846)                  0x000000008018014e(2149056846)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x000000000000005a(90)                          0x000000000000005a(90)                          
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x000000000000003e(62)                          0x000000000000003e(62)                          
a2(x12)             0x00000000801803e4(2149057508)                  0x00000000801803e4(2149057508)                  
a3(x13)             0x00000000000000f3(243)                         0x00000000000000f3(243)                         
a4(x14)             0x00000000801803e4(2149057508)                  0x00000000801803e4(2149057508)                  
a5(x15)             0x000000008027f7c3(2150102979)                  0x000000008027f7c3(2150102979)                  
a6(x16)             0x0000000080185e1b(2149080603)                  0x0000000080185e1b(2149080603)                  
a7(x17)             0x000000000000005c(92)                          0x000000000000005c(92)                          
s2(x18)             0x00000000800005f9(2147485177)                  0x00000000800005f9(2147485177)                  
s3(x19)             0x000000008017ff9d(2149056413)                  0x000000008017ff9d(2149056413)                  
s4(x20)             0x000000007ffffa41(2147482177)                  0x000000007ffffa41(2147482177)                  
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x00000000800002c0(2147484352)                  0x00000000800002c0(2147484352)                  
s8(x24)             0x000000008017fcbb(2149055675)                  0x000000008017fcbb(2149055675)                  
s9(x25)             0x00000000801ffdc8(2149580232)                  0x00000000801ffdc8(2149580232)                  
s10(x26)            0x000000008017fdd3(2149055955)                  0x000000008017fdd3(2149055955)                  
s11(x27)            0x00000000801ff902(2149579010)                  0x00000000801ff902(2149579010)                  
t3(x28)             0x00000000800004f9(2147484921)                  0x00000000800004f9(2147484921)                  
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x0000000080000218(2147484184)                  0x0000000080000218(2147484184)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            5af78ef7f93fbbf401b62b1407aec013448b2fed        5af78ef7f93fbbf401b62b1407aec013448b2fed        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        4167bd4ce44d1cbbc933b1f39985b50a566ff66f        X
lastPC              0x0000000080000754(2147485524)                  0x0000000080000754(2147485524)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000042(66)                          0x0000000000000042(66)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xc1e002ffdd400000(-2149056234.0_d)             0xc1e002ffdd400000(-2149056234.0_d)             
f4                  0xffffffffffffff52(nan_h)                       0xffffffffffffff52(nan_h)                       
f5                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f6                  0xc1d2e04a30000000(-1266755776.0_d)             0xc1d2e04a30000000(-1266755776.0_d)             
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)                     
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x41e0040096000000(2149582000.0_d)              0x41e0040096000000(2149582000.0_d)              
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x00000000739fd700(9.58415765e-315_d)           0x00000000739fd700(9.58415765e-315_d)           
f19                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f20                 0xffffffff0201b303(9.528797047284384e-38_s)     0xffffffff0201b303(9.528797047284384e-38_s)     
f21                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f24                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f25                 0xffffffff4f001804(2149057536.0_s)              0xffffffff4f001804(2149057536.0_s)              
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x41e0030035400000(2149056938.0_d)              0x41e0030035400000(2149056938.0_d)              
STATES DIFFER: True
```

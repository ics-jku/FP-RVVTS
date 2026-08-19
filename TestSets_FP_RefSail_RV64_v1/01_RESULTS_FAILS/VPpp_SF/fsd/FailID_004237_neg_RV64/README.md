# FailID_004237 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4237
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
_reg_f0: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x60,0xd7,0xc4,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0xf6,0x04,0x20,0x80,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f12:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xdf,0x43
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x60,0xd7,0x44,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f23:.byte 0x2c,0x02,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x1
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8018a0a0            // ra
    li x2, 0x6000                // sp
    li x3, 0x859                 // gp
    li x4, 0x6000                // tp
    li x5, 0x6000                // t0
    li x6, 0x0                   // t1
    li x7, 0x54                  // t2
    li x8, 0x801800a0            // fp
    li x9, 0x1f6                 // s1
    li x10, 0x6000               // a0
    li x11, 0x80000423           // a1
    li x12, 0x8                  // a2
    li x13, 0xca                 // a3
    li x14, 0x14f                // a4
    li x15, 0x1                  // a5
    li x16, 0x10                 // a6
    li x17, 0x8017fb5d           // a7
    li x18, 0x1                  // s2
    li x19, 0x2005fefa800        // s3
    li x20, 0x0                  // s4
    li x21, 0x80180226           // s5
    li x22, 0x801805e0           // s6
    li x23, 0x1                  // s7
    li x24, 0x801ffe89           // s8
    li x25, 0xffffffffbca04000   // s9
    li x26, 0x1                  // s10
    li x27, 0x6000               // s11
    li x28, 0x0                  // t3
    li x29, 0x0                  // t4
    li x30, 0x7ffffc6f           // t5
    li x31, 0x8000063e           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f22', 'x18'}, 'clob': {'x18', 'x10'}})
    
    li x10, 0xffff8
    and x18, x18, x10
    li x10, 0x8018064a
    add x18, x18, x10
    fsd f22, -0x64a(x18)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        f8fa8b89f6afdd5b28272d6cefc6764c91351ced        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f22, -0x64a(x18)
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        f8fa8b89f6afdd5b28272d6cefc6764c91351ced        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f22, x64, x18
s2(x18)             0x000000008018064a(2149058122)                  0x000000008018064a(2149058122)
f22                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008018a0a0(2149097632)                  0x000000008018a0a0(2149097632)                  
sp(x2)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
gp(x3)              0x0000000000000859(2137)                        0x0000000000000859(2137)                        
tp(x4)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000000000054(84)                          0x0000000000000054(84)                          
fp(x8)              0x00000000801800a0(2149056672)                  0x00000000801800a0(2149056672)                  
s1(x9)              0x00000000000001f6(502)                         0x00000000000001f6(502)                         
a0(x10)             0x000000008018064a(2149058122)                  0x000000008018064a(2149058122)                  
a1(x11)             0x0000000080000423(2147484707)                  0x0000000080000423(2147484707)                  
a2(x12)             0x0000000000000008(8)                           0x0000000000000008(8)                           
a3(x13)             0x00000000000000ca(202)                         0x00000000000000ca(202)                         
a4(x14)             0x000000000000014f(335)                         0x000000000000014f(335)                         
a5(x15)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a6(x16)             0x0000000000000010(16)                          0x0000000000000010(16)                          
a7(x17)             0x000000008017fb5d(2149055325)                  0x000000008017fb5d(2149055325)                  
s2(x18)             0x000000008018064a(2149058122)                  0x000000008018064a(2149058122)                  
s3(x19)             0x000002005fefa800(2200632797184)               0x000002005fefa800(2200632797184)               
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x0000000080180226(2149057062)                  0x0000000080180226(2149057062)                  
s6(x22)             0x00000000801805e0(2149058016)                  0x00000000801805e0(2149058016)                  
s7(x23)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s8(x24)             0x00000000801ffe89(2149580425)                  0x00000000801ffe89(2149580425)                  
s9(x25)             0xffffffffbca04000(18446744072579203072)        0xffffffffbca04000(18446744072579203072)        
s10(x26)            0x0000000000000001(1)                           0x0000000000000001(1)                           
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x000000007ffffc6f(2147482735)                  0x000000007ffffc6f(2147482735)                  
t6(x31)             0x000000008000063e(2147485246)                  0x000000008000063e(2147485246)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            9267eb95139dc57bfd4e15bb906355c37191e0b1        9267eb95139dc57bfd4e15bb906355c37191e0b1        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        f8fa8b89f6afdd5b28272d6cefc6764c91351ced        X
lastPC              0x0000000080000700(2147485440)                  0x0000000080000700(2147485440)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000001(1)                           0x0000000000000001(1)                           
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f1                  0xffffffffc4d76000(-1723.0_s)                   0xffffffffc4d76000(-1723.0_s)                   
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff802004f6(-2.940515526105411e-39_s)    0xffffffff802004f6(-2.940515526105411e-39_s)    
f11                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f12                 0x43dfffffffffffff(9.223372036854775e+18_d)     0x43dfffffffffffff(9.223372036854775e+18_d)     
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff44d76000(1723.0_s)                    0xffffffff44d76000(1723.0_s)                    
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f22                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f23                 0x000000008018022c(1.0617752683e-314_d)         0x000000008018022c(1.0617752683e-314_d)         
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

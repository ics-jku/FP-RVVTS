# FailID_000902 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 902
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
_reg_f0: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f1: .byte 0xb4,0xd0,0xa5,0xba,0xfa,0x00,0xfd,0xb3
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f3: .byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0xd9,0xfc,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xd0
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x201b303             // sp
    li x3, 0x0                   // gp
    li x4, 0x8017f6fd            // tp
    li x5, 0x80000140            // t0
    li x6, 0xcc                  // t1
    li x7, 0x80180063            // t2
    li x8, 0xfffffffffa16e000    // fp
    li x9, 0x7ffffc55            // s1
    li x10, 0x801807fa           // a0
    li x11, 0x80180003           // a1
    li x12, 0x8                  // a2
    li x13, 0x7fffff6e           // a3
    li x14, 0x0                  // a4
    li x15, 0x20080              // a5
    li x16, 0x0                  // a6
    li x17, 0x801ff21e           // a7
    li x18, 0x44a8c000           // s2
    li x19, 0x400bfeb9           // s3
    li x20, 0x4000000            // s4
    li x21, 0x800006b6           // s5
    li x22, 0x7fffff84           // s6
    li x23, 0x51b023b4199318     // s7
    li x24, 0x1                  // s8
    li x25, 0x8017f887           // s9
    li x26, 0x1                  // s10
    li x27, 0x8017f9c5           // s11
    li x28, 0x801ff438           // t3
    li x29, 0x4000035b           // t4
    li x30, 0x8017f8f6           // t5
    li x31, 0x1                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x10'}, 'clob': {'x10', 'f11', 'x28'}})
    
    li x28, 0x1ffff8
    and x10, x10, x28
    li x28, 0x8000064a
    add x10, x10, x28
    fld f11, -0x64a(x10)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f11                 0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f11, -0x64a(x10)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f11                 0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f11, x64, x10
a0(x10)             0x0000000080180e42(2149060162)                  0x0000000080180e42(2149060162)
f11                 0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x000000000201b303(33665795)                    0x000000000201b303(33665795)                    
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x000000008017f6fd(2149054205)                  0x000000008017f6fd(2149054205)                  
t0(x5)              0x0000000080000140(2147483968)                  0x0000000080000140(2147483968)                  
t1(x6)              0x00000000000000cc(204)                         0x00000000000000cc(204)                         
t2(x7)              0x0000000080180063(2149056611)                  0x0000000080180063(2149056611)                  
fp(x8)              0xfffffffffa16e000(18446744073610387456)        0xfffffffffa16e000(18446744073610387456)        
s1(x9)              0x000000007ffffc55(2147482709)                  0x000000007ffffc55(2147482709)                  
a0(x10)             0x0000000080180e42(2149060162)                  0x0000000080180e42(2149060162)                  
a1(x11)             0x0000000080180003(2149056515)                  0x0000000080180003(2149056515)                  
a2(x12)             0x0000000000000008(8)                           0x0000000000000008(8)                           
a3(x13)             0x000000007fffff6e(2147483502)                  0x000000007fffff6e(2147483502)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000000020080(131200)                      0x0000000000020080(131200)                      
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x00000000801ff21e(2149577246)                  0x00000000801ff21e(2149577246)                  
s2(x18)             0x0000000044a8c000(1151909888)                  0x0000000044a8c000(1151909888)                  
s3(x19)             0x00000000400bfeb9(1074527929)                  0x00000000400bfeb9(1074527929)                  
s4(x20)             0x0000000004000000(67108864)                    0x0000000004000000(67108864)                    
s5(x21)             0x00000000800006b6(2147485366)                  0x00000000800006b6(2147485366)                  
s6(x22)             0x000000007fffff84(2147483524)                  0x000000007fffff84(2147483524)                  
s7(x23)             0x0051b023b4199318(22993140505482008)           0x0051b023b4199318(22993140505482008)           
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x000000008017f887(2149054599)                  0x000000008017f887(2149054599)                  
s10(x26)            0x0000000000000001(1)                           0x0000000000000001(1)                           
s11(x27)            0x000000008017f9c5(2149054917)                  0x000000008017f9c5(2149054917)                  
t3(x28)             0x000000008000064a(2147485258)                  0x000000008000064a(2147485258)                  
t4(x29)             0x000000004000035b(1073742683)                  0x000000004000035b(1073742683)                  
t5(x30)             0x000000008017f8f6(2149054710)                  0x000000008017f8f6(2149054710)                  
t6(x31)             0x0000000000000001(1)                           0x0000000000000001(1)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            cf73c58d0ded7174ff34e0e0a95670a8462c5f32        cf73c58d0ded7174ff34e0e0a95670a8462c5f32        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000d0(208)                         0x00000000000000d0(208)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f1                  0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    
f2                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f3                  0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
f12                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xfffffffffffffcd9(nan_h)                       0xfffffffffffffcd9(nan_h)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f20                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f28                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f29                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
STATES DIFFER: True
```

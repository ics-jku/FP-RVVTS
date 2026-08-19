# FailID_004256 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4256
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0xfe,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x01,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0xf4,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x0b,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x0f,0xff,0xff,0x7f,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xc8
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x1                   // sp
    li x3, 0x80180192            // gp
    li x4, 0x801fd37c            // tp
    li x5, 0x8000019a            // t0
    li x6, 0xffffffff7ffff99f    // t1
    li x7, 0x0                   // t2
    li x8, 0x1f8                 // fp
    li x9, 0x80180483            // s1
    li x10, 0x0                  // a0
    li x11, 0x7ffffdc5           // a1
    li x12, 0x801804d4           // a2
    li x13, 0x8017f99e           // a3
    li x14, 0x8c                 // a4
    li x15, 0x0                  // a5
    li x16, 0x80029c59           // a6
    li x17, 0xfffffffffffffa0b   // a7
    li x18, 0x809                // s2
    li x19, 0x340191f3           // s3
    li x20, 0xffffffff84e2d000   // s4
    li x21, 0x7ffffee9           // s5
    li x22, 0x801da0cd           // s6
    li x23, 0x8117720            // s7
    li x24, 0x400c026            // s8
    li x25, 0x8017f92f           // s9
    li x26, 0x80                 // s10
    li x27, 0x0                  // s11
    li x28, 0x8017fa21           // t3
    li x29, 0x1                  // t4
    li x30, 0x80005dc5           // t5
    li x31, 0x801fff48           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f29', 'x26'}, 'clob': {'x16', 'x26'}})
    
    li x16, 0xffff8
    and x26, x26, x16
    li x16, 0x8017fd1b
    add x26, x26, x16
    fsd f29, 0x2e5(x26)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c1c41863849d8fe283c977d0f5d4772981786c17        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f29, 0x2e5(x26)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c1c41863849d8fe283c977d0f5d4772981786c17        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f29, x2, e5, x26
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)
s10(x26)            0x000000008017fd9b(2149055899)                  0x000000008017fd9b(2149055899)
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)                           
gp(x3)              0x0000000080180192(2149056914)                  0x0000000080180192(2149056914)                  
tp(x4)              0x00000000801fd37c(2149569404)                  0x00000000801fd37c(2149569404)                  
t0(x5)              0x000000008000019a(2147484058)                  0x000000008000019a(2147484058)                  
t1(x6)              0xffffffff7ffff99f(18446744071562066335)        0xffffffff7ffff99f(18446744071562066335)        
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x00000000000001f8(504)                         0x00000000000001f8(504)                         
s1(x9)              0x0000000080180483(2149057667)                  0x0000000080180483(2149057667)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x000000007ffffdc5(2147483077)                  0x000000007ffffdc5(2147483077)                  
a2(x12)             0x00000000801804d4(2149057748)                  0x00000000801804d4(2149057748)                  
a3(x13)             0x000000008017f99e(2149054878)                  0x000000008017f99e(2149054878)                  
a4(x14)             0x000000000000008c(140)                         0x000000000000008c(140)                         
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x000000008017fd1b(2149055771)                  0x000000008017fd1b(2149055771)                  
a7(x17)             0xfffffffffffffa0b(18446744073709550091)        0xfffffffffffffa0b(18446744073709550091)        
s2(x18)             0x0000000000000809(2057)                        0x0000000000000809(2057)                        
s3(x19)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
s4(x20)             0xffffffff84e2d000(18446744071644041216)        0xffffffff84e2d000(18446744071644041216)        
s5(x21)             0x000000007ffffee9(2147483369)                  0x000000007ffffee9(2147483369)                  
s6(x22)             0x00000000801da0cd(2149425357)                  0x00000000801da0cd(2149425357)                  
s7(x23)             0x0000000008117720(135362336)                   0x0000000008117720(135362336)                   
s8(x24)             0x000000000400c026(67158054)                    0x000000000400c026(67158054)                    
s9(x25)             0x000000008017f92f(2149054767)                  0x000000008017f92f(2149054767)                  
s10(x26)            0x000000008017fd9b(2149055899)                  0x000000008017fd9b(2149055899)                  
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x000000008017fa21(2149055009)                  0x000000008017fa21(2149055009)                  
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x0000000080005dc5(2147507653)                  0x0000000080005dc5(2147507653)                  
t6(x31)             0x00000000801fff48(2149580616)                  0x00000000801fff48(2149580616)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            f4aecb31f77c099b746d8e3be12f66fa7b66c9c3        f4aecb31f77c099b746d8e3be12f66fa7b66c9c3        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c1c41863849d8fe283c977d0f5d4772981786c17        X
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000c8(200)                         0x00000000000000c8(200)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff4efffffe(2147483392.0_s)              0xffffffff4efffffe(2147483392.0_s)              
f3                  0x0000000000000001(5e-324_d)                    0x0000000000000001(5e-324_d)                    
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff4f0017f4(2149053440.0_s)              0xffffffff4f0017f4(2149053440.0_s)              
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff8000000b(-1.5414283107572988e-44_s)   0xffffffff8000000b(-1.5414283107572988e-44_s)   
f22                 0x000000007fffff0f(1.0609977764e-314_d)         0x000000007fffff0f(1.0609977764e-314_d)         
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

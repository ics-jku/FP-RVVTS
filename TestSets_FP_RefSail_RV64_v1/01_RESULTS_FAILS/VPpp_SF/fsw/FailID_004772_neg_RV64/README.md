# FailID_004772 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4772
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
_reg_f0: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f2: .byte 0x23,0xb4,0x71,0x02,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x01,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f4: .byte 0xf5,0xff,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x80
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x50,0x07,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x6d,0xf5,0x17,0x80,0x00,0x00,0x00,0x00
_reg_f25:.byte 0x00,0x00,0xa0,0x41,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': True, 'nv': True, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xd9
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xc9                  // ra
    li x2, 0x8017fca1            // sp
    li x3, 0x3c0                 // gp
    li x4, 0x0                   // tp
    li x5, 0x0                   // t0
    li x6, 0x0                   // t1
    li x7, 0x14                  // t2
    li x8, 0x7ffffb4d            // fp
    li x9, 0xffffffffffffffff    // s1
    li x10, 0x80000504           // a0
    li x11, 0x0                  // a1
    li x12, 0x801ff7e5           // a2
    li x13, 0x8017ff5e           // a3
    li x14, 0x1                  // a4
    li x15, 0x6000               // a5
    li x16, 0x0                  // a6
    li x17, 0x80000750           // a7
    li x18, 0x69                 // s2
    li x19, 0x1                  // s3
    li x20, 0x21                 // s4
    li x21, 0xc4                 // s5
    li x22, 0xffffffffffff91f3   // s6
    li x23, 0x200                // s7
    li x24, 0x41a00000           // s8
    li x25, 0x6000               // s9
    li x26, 0x8017f9a5           // s10
    li x27, 0x8027fd18           // s11
    li x28, 0x8017fca1           // t3
    li x29, 0x0                  // t4
    li x30, 0x0                  // t5
    li x31, 0x7ffffb4d           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x6', 'f15', 'fcsr.rm'}, 'clob': {'x6', 'x27'}})
    
    li x27, 0xffffc
    and x6, x6, x27
    li x27, 0x8017fe6f
    add x6, x6, x27
    fsw f15, 0x191(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        3cfc50187a9febfe44b5c11e592e549b5119bd02        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f15, 0x191(x6)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'div-by-0', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        3cfc50187a9febfe44b5c11e592e549b5119bd02        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f15, x191, x6
t1(x6)              0x000000008017fe6f(2149056111)                  0x000000008017fe6f(2149056111)
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000000000c9(201)                         0x00000000000000c9(201)                         
sp(x2)              0x000000008017fca1(2149055649)                  0x000000008017fca1(2149055649)                  
gp(x3)              0x00000000000003c0(960)                         0x00000000000003c0(960)                         
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x000000008017fe6f(2149056111)                  0x000000008017fe6f(2149056111)                  
t2(x7)              0x0000000000000014(20)                          0x0000000000000014(20)                          
fp(x8)              0x000000007ffffb4d(2147482445)                  0x000000007ffffb4d(2147482445)                  
s1(x9)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a0(x10)             0x0000000080000504(2147484932)                  0x0000000080000504(2147484932)                  
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x00000000801ff7e5(2149578725)                  0x00000000801ff7e5(2149578725)                  
a3(x13)             0x000000008017ff5e(2149056350)                  0x000000008017ff5e(2149056350)                  
a4(x14)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x0000000080000750(2147485520)                  0x0000000080000750(2147485520)                  
s2(x18)             0x0000000000000069(105)                         0x0000000000000069(105)                         
s3(x19)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s4(x20)             0x0000000000000021(33)                          0x0000000000000021(33)                          
s5(x21)             0x00000000000000c4(196)                         0x00000000000000c4(196)                         
s6(x22)             0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)        
s7(x23)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s8(x24)             0x0000000041a00000(1101004800)                  0x0000000041a00000(1101004800)                  
s9(x25)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s10(x26)            0x000000008017f9a5(2149054885)                  0x000000008017f9a5(2149054885)                  
s11(x27)            0x000000008017fe6f(2149056111)                  0x000000008017fe6f(2149056111)                  
t3(x28)             0x000000008017fca1(2149055649)                  0x000000008017fca1(2149055649)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x000000007ffffb4d(2147482445)                  0x000000007ffffb4d(2147482445)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            d7e35de03ca671e5d3de64dfe2e0029c1b41108e        d7e35de03ca671e5d3de64dfe2e0029c1b41108e        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        3cfc50187a9febfe44b5c11e592e549b5119bd02        X
lastPC              0x00000000800006fc(2147485436)                  0x00000000800006fc(2147485436)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000d9(217)                         0x00000000000000d9(217)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f1                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f2                  0xffffffff0271b423(1.7757580362206577e-37_s)    0xffffffff0271b423(1.7757580362206577e-37_s)    
f3                  0x0000000000000001(5e-324_d)                    0x0000000000000001(5e-324_d)                    
f4                  0xffffffffcefffff5(-2147482240.0_s)             0xffffffffcefffff5(-2147482240.0_s)             
f5                  0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x8000000000000000(-0.0_d)                      0x8000000000000000(-0.0_d)                      
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff80000750(-2.6232307252160576e-42_s)   0xffffffff80000750(-2.6232307252160576e-42_s)   
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x000000008017f56d(1.061773656e-314_d)          0x000000008017f56d(1.061773656e-314_d)          
f25                 0xffffffff41a00000(20.0_s)                      0xffffffff41a00000(20.0_s)                      
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
STATES DIFFER: True
```

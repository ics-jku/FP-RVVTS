# FailID_002135 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2135
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0xb6,0x81,0x03,0x00,0x43
_reg_f3: .byte 0x00,0x00,0x5b,0x4e,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xe0,0xd0,0x00,0x03,0xe0,0x41
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f26:.byte 0x00,0x80,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x81
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017fcd0            // ra
    li x2, 0x7fffffff            // sp
    li x3, 0x200                 // gp
    li x4, 0x200                 // tp
    li x5, 0x6000                // t0
    li x6, 0x2007036c00000       // t1
    li x7, 0xffffffffffffffff    // t2
    li x8, 0x80180e61            // fp
    li x9, 0xfffffffffffff89c    // s1
    li x10, 0x0                  // a0
    li x11, 0xffffffffffffffff   // a1
    li x12, 0x7ffffbfa           // a2
    li x13, 0x6000               // a3
    li x14, 0x8017fc50           // a4
    li x15, 0x10030              // a5
    li x16, 0x801c0db0           // a6
    li x17, 0xffffffffffff006f   // a7
    li x18, 0x81                 // s2
    li x19, 0x7ff8000000000000   // s3
    li x20, 0x1                  // s4
    li x21, 0xffffffff7fc00000   // s5
    li x22, 0x7ffffbfa           // s6
    li x23, 0x340191f3           // s7
    li x24, 0x3a                 // s8
    li x25, 0x8017fa18           // s9
    li x26, 0x801ffe40           // s10
    li x27, 0x1                  // s11
    li x28, 0x37                 // t3
    li x29, 0x801806dc           // t4
    li x30, 0x1                  // t5
    li x31, 0x69                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x30', 'mstatus.fs/vs.fs', 'f25'}, 'clob': {'x30', 'x18'}})
    
    li x18, 0xffffc
    and x30, x30, x18
    li x18, 0x8017fa84
    add x30, x30, x18
    fsw f25, 0x57c(x30)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f25, 0x57c(x30)
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, x57, x30
t5(x30)             0x000000008017fa84(2149055108)                  0x000000008017fa84(2149055108)
f25                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fcd0(2149055696)                  0x000000008017fcd0(2149055696)                  
sp(x2)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
gp(x3)              0x0000000000000200(512)                         0x0000000000000200(512)                         
tp(x4)              0x0000000000000200(512)                         0x0000000000000200(512)                         
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t1(x6)              0x0002007036c00000(563431908311040)             0x0002007036c00000(563431908311040)             
t2(x7)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
fp(x8)              0x0000000080180e61(2149060193)                  0x0000000080180e61(2149060193)                  
s1(x9)              0xfffffffffffff89c(18446744073709549724)        0xfffffffffffff89c(18446744073709549724)        
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a2(x12)             0x000000007ffffbfa(2147482618)                  0x000000007ffffbfa(2147482618)                  
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x000000008017fc50(2149055568)                  0x000000008017fc50(2149055568)                  
a5(x15)             0x0000000000010030(65584)                       0x0000000000010030(65584)                       
a6(x16)             0x00000000801c0db0(2149322160)                  0x00000000801c0db0(2149322160)                  
a7(x17)             0xffffffffffff006f(18446744073709486191)        0xffffffffffff006f(18446744073709486191)        
s2(x18)             0x000000008017fa84(2149055108)                  0x000000008017fa84(2149055108)                  
s3(x19)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
s4(x20)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s5(x21)             0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
s6(x22)             0x000000007ffffbfa(2147482618)                  0x000000007ffffbfa(2147482618)                  
s7(x23)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
s8(x24)             0x000000000000003a(58)                          0x000000000000003a(58)                          
s9(x25)             0x000000008017fa18(2149055000)                  0x000000008017fa18(2149055000)                  
s10(x26)            0x00000000801ffe40(2149580352)                  0x00000000801ffe40(2149580352)                  
s11(x27)            0x0000000000000001(1)                           0x0000000000000001(1)                           
t3(x28)             0x0000000000000037(55)                          0x0000000000000037(55)                          
t4(x29)             0x00000000801806dc(2149058268)                  0x00000000801806dc(2149058268)                  
t5(x30)             0x000000008017fa84(2149055108)                  0x000000008017fa84(2149055108)                  
t6(x31)             0x0000000000000069(105)                         0x0000000000000069(105)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            4faf6736f9b7d0b21bda11c323d1ad794841fdce        4faf6736f9b7d0b21bda11c323d1ad794841fdce        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000714(2147485460)                  0x0000000080000714(2147485460)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000081(129)                         0x0000000000000081(129)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f2                  0x43000381b6000000(563431908311040.0_d)         0x43000381b6000000(563431908311040.0_d)         
f3                  0xffffffff4e5b0000(918552576.0_s)               0xffffffff4e5b0000(918552576.0_s)               
f4                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0x41e00300d0e00000(2149058183.0_d)              0x41e00300d0e00000(2149058183.0_d)              
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff4f0017fd(2149055744.0_s)              0xffffffff4f0017fd(2149055744.0_s)              
f25                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f26                 0xffffffff4eff8000(2143289344.0_s)              0xffffffff4eff8000(2143289344.0_s)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

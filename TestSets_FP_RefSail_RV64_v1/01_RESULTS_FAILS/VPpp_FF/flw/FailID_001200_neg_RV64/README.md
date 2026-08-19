# FailID_001200 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1200
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
_reg_f0: .byte 0x00,0x00,0x00,0x66,0x6c,0x2e,0xcc,0xc1
_reg_f1: .byte 0x4f,0xfd,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0xbf,0xf9,0x17,0x80,0x00,0x00,0x00,0x00
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x58,0xfe,0xff,0xdf,0x41
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x4f,0xfd,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x09,0x02,0xe8,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x09,0x02,0xe8,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x34,0x27,0xa3,0xc7,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0xbf
_reg_f30:.byte 0xfb,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x04,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': False, 'nv': True, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x15
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801ffaa2            // ra
    li x2, 0x80180065            // sp
    li x3, 0x801ffd83            // gp
    li x4, 0x6000                // tp
    li x5, 0xfffffffffffffd8b    // t0
    li x6, 0x8028005d            // t1
    li x7, 0xc3                  // t2
    li x8, 0x1                   // fp
    li x9, 0x800003f2            // s1
    li x10, 0x802486a6           // a0
    li x11, 0x1002ff77800000     // a1
    li x12, 0x7ffffb46           // a2
    li x13, 0x80005f44           // a3
    li x14, 0x20                 // a4
    li x15, 0x6d5c6748           // a5
    li x16, 0x2007f              // a6
    li x17, 0x7fffff3a           // a7
    li x18, 0x1                  // s2
    li x19, 0x1                  // s3
    li x20, 0x0                  // s4
    li x21, 0x8017fbbc           // s5
    li x22, 0x0                  // s6
    li x23, 0x80180753           // s7
    li x24, 0x1                  // s8
    li x25, 0x95                 // s9
    li x26, 0x800000e2           // s10
    li x27, 0x80180150           // s11
    li x28, 0x1ae1b827           // t3
    li x29, 0x801fffa2           // t4
    li x30, 0xffffffffe4ad4000   // t5
    li x31, 0x7ffffde2           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x26', 'mstatus.fs/vs.fs'}, 'clob': {'x26', 'x6', 'f16'}})
    
    li x6, 0x1ffffc
    and x26, x26, x6
    li x6, 0x8000024c
    add x26, x26, x6
    flw f16, -0x24c(x26)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f16                 0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffff11c1b823(3.0563513956091643e-28_s)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f16, -0x24c(x26)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f16                 0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffff11c1b823(3.0563513956091643e-28_s)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f16, x24, x26
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)
s10(x26)            0x000000008000032c(2147484460)                  0x000000008000032c(2147484460)
f16                 0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffff11c1b823(3.0563513956091643e-28_s)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801ffaa2(2149579426)                  0x00000000801ffaa2(2149579426)                  
sp(x2)              0x0000000080180065(2149056613)                  0x0000000080180065(2149056613)                  
gp(x3)              0x00000000801ffd83(2149580163)                  0x00000000801ffd83(2149580163)                  
tp(x4)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t0(x5)              0xfffffffffffffd8b(18446744073709550987)        0xfffffffffffffd8b(18446744073709550987)        
t1(x6)              0x000000008000024c(2147484236)                  0x000000008000024c(2147484236)                  
t2(x7)              0x00000000000000c3(195)                         0x00000000000000c3(195)                         
fp(x8)              0x0000000000000001(1)                           0x0000000000000001(1)                           
s1(x9)              0x00000000800003f2(2147484658)                  0x00000000800003f2(2147484658)                  
a0(x10)             0x00000000802486a6(2149877414)                  0x00000000802486a6(2149877414)                  
a1(x11)             0x001002ff77800000(4506895872163840)            0x001002ff77800000(4506895872163840)            
a2(x12)             0x000000007ffffb46(2147482438)                  0x000000007ffffb46(2147482438)                  
a3(x13)             0x0000000080005f44(2147508036)                  0x0000000080005f44(2147508036)                  
a4(x14)             0x0000000000000020(32)                          0x0000000000000020(32)                          
a5(x15)             0x000000006d5c6748(1834772296)                  0x000000006d5c6748(1834772296)                  
a6(x16)             0x000000000002007f(131199)                      0x000000000002007f(131199)                      
a7(x17)             0x000000007fffff3a(2147483450)                  0x000000007fffff3a(2147483450)                  
s2(x18)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s3(x19)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x000000008017fbbc(2149055420)                  0x000000008017fbbc(2149055420)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000080180753(2149058387)                  0x0000000080180753(2149058387)                  
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x0000000000000095(149)                         0x0000000000000095(149)                         
s10(x26)            0x000000008000032c(2147484460)                  0x000000008000032c(2147484460)                  
s11(x27)            0x0000000080180150(2149056848)                  0x0000000080180150(2149056848)                  
t3(x28)             0x000000001ae1b827(451000359)                   0x000000001ae1b827(451000359)                   
t4(x29)             0x00000000801fffa2(2149580706)                  0x00000000801fffa2(2149580706)                  
t5(x30)             0xffffffffe4ad4000(18446744073251143680)        0xffffffffe4ad4000(18446744073251143680)        
t6(x31)             0x000000007ffffde2(2147483106)                  0x000000007ffffde2(2147483106)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            344a2dadca39b44b728b2e9e2eb9608321318c0c        344a2dadca39b44b728b2e9e2eb9608321318c0c        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000730(2147485488)                  0x0000000080000730(2147485488)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000015(21)                          0x0000000000000015(21)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xc1cc2e6c66000000(-945608908.0_d)              0xc1cc2e6c66000000(-945608908.0_d)              
f1                  0xffffffff8017fd4f(-2.2030864131498693e-39_s)   0xffffffff8017fd4f(-2.2030864131498693e-39_s)   
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x000000008017f9bf(1.0617742026e-314_d)         0x000000008017f9bf(1.0617742026e-314_d)         
f6                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x41dffffe58000000(2147481952.0_d)              0x41dffffe58000000(2147481952.0_d)              
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff8017fd4f(-2.2030864131498693e-39_s)   0xffffffff8017fd4f(-2.2030864131498693e-39_s)   
f15                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f16                 0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffff11c1b823(3.0563513956091643e-28_s)    X
f17                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fe80209(nan_s)                       0xffffffff7fe80209(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f25                 0xffffffff7fe80209(nan_s)                       0xffffffff7fe80209(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f28                 0xffffffffc7a32734(-83534.40625_s)              0xffffffffc7a32734(-83534.40625_s)              
f29                 0xbff0000000000000(-1.0_d)                      0xbff0000000000000(-1.0_d)                      
f30                 0xffffffff4efffffb(2147483008.0_s)              0xffffffff4efffffb(2147483008.0_s)              
f31                 0xffffffffffff0400(6.103515625e-05_h)           0xffffffffffff0400(6.103515625e-05_h)           
STATES DIFFER: True
```

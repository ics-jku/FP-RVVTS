# FailID_001202 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1202
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x4f,0xfd,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0xbf,0xf9,0x17,0x80,0x00,0x00,0x00,0x00
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x74,0xea,0xbf,0x8e,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x34,0x27,0xa3,0xc7,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0xbf
_reg_f30:.byte 0xfb,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'res0(0b101)', 'res': 0}
    li t0, 0xa2
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x20                  // ra
    li x2, 0x1                   // sp
    li x3, 0x0                   // gp
    li x4, 0x6000                // tp
    li x5, 0x7ffff919            // t0
    li x6, 0x8000024c            // t1
    li x7, 0x7ffffd68            // t2
    li x8, 0x21                  // fp
    li x9, 0xc00                 // s1
    li x10, 0x1                  // a0
    li x11, 0x801804a8           // a1
    li x12, 0x800001cd           // a2
    li x13, 0x0                  // a3
    li x14, 0xffffffffaef3c000   // a4
    li x15, 0x8000008f           // a5
    li x16, 0x7ffffdf3           // a6
    li x17, 0x0                  // a7
    li x18, 0x801807a9           // s2
    li x19, 0xfd7e9754           // s3
    li x20, 0x80005d68           // s4
    li x21, 0x51b023340191f3     // s5
    li x22, 0xa2                 // s6
    li x23, 0x801ffdb1           // s7
    li x24, 0xb                  // s8
    li x25, 0x800061cd           // s9
    li x26, 0x0                  // s10
    li x27, 0x7ffffb52           // s11
    li x28, 0x80180687           // t3
    li x29, 0x408                // t4
    li x30, 0x80180426           // t5
    li x31, 0xdd                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x2'}, 'clob': {'x2', 'x19', 'f19'}})
    
    li x19, 0x1ffffc
    and x2, x2, x19
    li x19, 0x7ffff8ef
    add x2, x2, x19
    flw f19, 0x711(x2)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f19, 0x711(x2)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f19, x711, x2
sp(x2)              0x000000007ffff8ef(2147481839)                  0x000000007ffff8ef(2147481839)
f19                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000020(32)                          0x0000000000000020(32)                          
sp(x2)              0x000000007ffff8ef(2147481839)                  0x000000007ffff8ef(2147481839)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t0(x5)              0x000000007ffff919(2147481881)                  0x000000007ffff919(2147481881)                  
t1(x6)              0x000000008000024c(2147484236)                  0x000000008000024c(2147484236)                  
t2(x7)              0x000000007ffffd68(2147482984)                  0x000000007ffffd68(2147482984)                  
fp(x8)              0x0000000000000021(33)                          0x0000000000000021(33)                          
s1(x9)              0x0000000000000c00(3072)                        0x0000000000000c00(3072)                        
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x00000000801804a8(2149057704)                  0x00000000801804a8(2149057704)                  
a2(x12)             0x00000000800001cd(2147484109)                  0x00000000800001cd(2147484109)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0xffffffffaef3c000(18446744072349794304)        0xffffffffaef3c000(18446744072349794304)        
a5(x15)             0x000000008000008f(2147483791)                  0x000000008000008f(2147483791)                  
a6(x16)             0x000000007ffffdf3(2147483123)                  0x000000007ffffdf3(2147483123)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x00000000801807a9(2149058473)                  0x00000000801807a9(2149058473)                  
s3(x19)             0x000000007ffff8ef(2147481839)                  0x000000007ffff8ef(2147481839)                  
s4(x20)             0x0000000080005d68(2147507560)                  0x0000000080005d68(2147507560)                  
s5(x21)             0x0051b023340191f3(22993138356425203)           0x0051b023340191f3(22993138356425203)           
s6(x22)             0x00000000000000a2(162)                         0x00000000000000a2(162)                         
s7(x23)             0x00000000801ffdb1(2149580209)                  0x00000000801ffdb1(2149580209)                  
s8(x24)             0x000000000000000b(11)                          0x000000000000000b(11)                          
s9(x25)             0x00000000800061cd(2147508685)                  0x00000000800061cd(2147508685)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000007ffffb52(2147482450)                  0x000000007ffffb52(2147482450)                  
t3(x28)             0x0000000080180687(2149058183)                  0x0000000080180687(2149058183)                  
t4(x29)             0x0000000000000408(1032)                        0x0000000000000408(1032)                        
t5(x30)             0x0000000080180426(2149057574)                  0x0000000080180426(2149057574)                  
t6(x31)             0x00000000000000dd(221)                         0x00000000000000dd(221)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            b3991d5f27cc8eddcd8adb489f7054c917130e7b        b3991d5f27cc8eddcd8adb489f7054c917130e7b        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000a2(162)                         0x00000000000000a2(162)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            res0(0b101)                                     res0(0b101)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff8017fd4f(-2.2030864131498693e-39_s)   0xffffffff8017fd4f(-2.2030864131498693e-39_s)   
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x000000008017f9bf(1.0617742026e-314_d)         0x000000008017f9bf(1.0617742026e-314_d)         
f6                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff8ebfea74(-4.7310905427375474e-30_s)   0xffffffff8ebfea74(-4.7310905427375474e-30_s)   
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f17                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffffc7a32734(-83534.40625_s)              0xffffffffc7a32734(-83534.40625_s)              
f29                 0xbff0000000000000(-1.0_d)                      0xbff0000000000000(-1.0_d)                      
f30                 0xffffffff4efffffb(2147483008.0_s)              0xffffffff4efffffb(2147483008.0_s)              
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

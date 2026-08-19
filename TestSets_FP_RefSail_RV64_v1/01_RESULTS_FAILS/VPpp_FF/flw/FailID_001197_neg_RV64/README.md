# FailID_001197 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1197
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
    li x1, 0x7fffff5d            // ra
    li x2, 0x800326e5            // sp
    li x3, 0x8018035c            // gp
    li x4, 0x80180676            // tp
    li x5, 0xfffffffffffffd8b    // t0
    li x6, 0x7fffffff            // t1
    li x7, 0x400                 // t2
    li x8, 0x1                   // fp
    li x9, 0x1                   // s1
    li x10, 0x801c7f7b           // a0
    li x11, 0x80185f7b           // a1
    li x12, 0x7fffffb1           // a2
    li x13, 0x80005f44           // a3
    li x14, 0x8017f552           // a4
    li x15, 0x80005e59           // a5
    li x16, 0x80185afd           // a6
    li x17, 0x80000158           // a7
    li x18, 0x80180457           // s2
    li x19, 0x7ffffde4           // s3
    li x20, 0x80000321           // s4
    li x21, 0x7ffffde4           // s5
    li x22, 0x6000               // s6
    li x23, 0x80180753           // s7
    li x24, 0x0                  // s8
    li x25, 0x3632000            // s9
    li x26, 0x800000e2           // s10
    li x27, 0x0                  // s11
    li x28, 0x6000               // t3
    li x29, 0x801fffa2           // t4
    li x30, 0x80185f7b           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x31'}, 'clob': {'f20', 'x22', 'x31'}})
    
    li x22, 0x1ffffc
    and x31, x31, x22
    li x22, 0x800004fc
    add x31, x31, x22
    flw f20, -0x4fc(x31)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f20                 0xffffffff7fe80209(nan_s)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f20, -0x4fc(x31)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f20                 0xffffffff7fe80209(nan_s)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f20, x4, x31
tp(x4)              0x0000000080180676(2149058166)                  0x0000000080180676(2149058166)
t6(x31)             0x00000000800004fc(2147484924)                  0x00000000800004fc(2147484924)
f20                 0xffffffff7fe80209(nan_s)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007fffff5d(2147483485)                  0x000000007fffff5d(2147483485)                  
sp(x2)              0x00000000800326e5(2147690213)                  0x00000000800326e5(2147690213)                  
gp(x3)              0x000000008018035c(2149057372)                  0x000000008018035c(2149057372)                  
tp(x4)              0x0000000080180676(2149058166)                  0x0000000080180676(2149058166)                  
t0(x5)              0xfffffffffffffd8b(18446744073709550987)        0xfffffffffffffd8b(18446744073709550987)        
t1(x6)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
t2(x7)              0x0000000000000400(1024)                        0x0000000000000400(1024)                        
fp(x8)              0x0000000000000001(1)                           0x0000000000000001(1)                           
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x00000000801c7f7b(2149351291)                  0x00000000801c7f7b(2149351291)                  
a1(x11)             0x0000000080185f7b(2149080955)                  0x0000000080185f7b(2149080955)                  
a2(x12)             0x000000007fffffb1(2147483569)                  0x000000007fffffb1(2147483569)                  
a3(x13)             0x0000000080005f44(2147508036)                  0x0000000080005f44(2147508036)                  
a4(x14)             0x000000008017f552(2149053778)                  0x000000008017f552(2149053778)                  
a5(x15)             0x0000000080005e59(2147507801)                  0x0000000080005e59(2147507801)                  
a6(x16)             0x0000000080185afd(2149079805)                  0x0000000080185afd(2149079805)                  
a7(x17)             0x0000000080000158(2147483992)                  0x0000000080000158(2147483992)                  
s2(x18)             0x0000000080180457(2149057623)                  0x0000000080180457(2149057623)                  
s3(x19)             0x000000007ffffde4(2147483108)                  0x000000007ffffde4(2147483108)                  
s4(x20)             0x0000000080000321(2147484449)                  0x0000000080000321(2147484449)                  
s5(x21)             0x000000007ffffde4(2147483108)                  0x000000007ffffde4(2147483108)                  
s6(x22)             0x00000000800004fc(2147484924)                  0x00000000800004fc(2147484924)                  
s7(x23)             0x0000000080180753(2149058387)                  0x0000000080180753(2149058387)                  
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x0000000003632000(56827904)                    0x0000000003632000(56827904)                    
s10(x26)            0x00000000800000e2(2147483874)                  0x00000000800000e2(2147483874)                  
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x00000000801fffa2(2149580706)                  0x00000000801fffa2(2149580706)                  
t5(x30)             0x0000000080185f7b(2149080955)                  0x0000000080185f7b(2149080955)                  
t6(x31)             0x00000000800004fc(2147484924)                  0x00000000800004fc(2147484924)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            ca51e9aabd936ccba3f7017ec8e15b1f562125dd        ca51e9aabd936ccba3f7017ec8e15b1f562125dd        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000758(2147485528)                  0x0000000080000758(2147485528)                  
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
f16                 0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f17                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fe80209(nan_s)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
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

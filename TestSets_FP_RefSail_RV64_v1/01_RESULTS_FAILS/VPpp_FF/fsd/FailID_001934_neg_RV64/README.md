# FailID_001934 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1934
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
    li x1, 0x40                  // ra
    li x2, 0x8017f967            // sp
    li x3, 0x1                   // gp
    li x4, 0x0                   // tp
    li x5, 0x0                   // t0
    li x6, 0xe8080000            // t1
    li x7, 0x800007a5            // t2
    li x8, 0x8017f748            // fp
    li x9, 0x0                   // s1
    li x10, 0x802005f4           // a0
    li x11, 0x801ff4e0           // a1
    li x12, 0x8018022d           // a2
    li x13, 0x80200086           // a3
    li x14, 0x8017f967           // a4
    li x15, 0x21                 // a5
    li x16, 0x7ffffb77           // a6
    li x17, 0xe94e6758           // a7
    li x18, 0x8017fbb9           // s2
    li x19, 0x7fffffff           // s3
    li x20, 0x0                  // s4
    li x21, 0xa8                 // s5
    li x22, 0x6000               // s6
    li x23, 0x91f3               // s7
    li x24, 0x8017f168           // s8
    li x25, 0x800005f8           // s9
    li x26, 0x7ffffed9           // s10
    li x27, 0xfffffffff8381000   // s11
    li x28, 0x6000               // t3
    li x29, 0x8017fe57           // t4
    li x30, 0x86                 // t5
    li x31, 0x8027f9cf           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f28', 'x4'}, 'clob': {'x4', 'x14'}})
    
    li x14, 0xffff8
    and x4, x4, x14
    li x14, 0x8017fde1
    add x4, x4, x14
    fsd f28, 0x21f(x4)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        6495492cd41c551d4d7ccd512c4120e46cea29aa        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f28, 0x21f(x4)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        6495492cd41c551d4d7ccd512c4120e46cea29aa        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f28, x21, x4
tp(x4)              0x000000008017fde1(2149055969)                  0x000000008017fde1(2149055969)
s5(x21)             0x00000000000000a8(168)                         0x00000000000000a8(168)
f28                 0x000000008017f836(1.0617740084e-314_d)         0x000000008017f836(1.0617740084e-314_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000040(64)                          0x0000000000000040(64)                          
sp(x2)              0x000000008017f967(2149054823)                  0x000000008017f967(2149054823)                  
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x000000008017fde1(2149055969)                  0x000000008017fde1(2149055969)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x00000000e8080000(3892838400)                  0x00000000e8080000(3892838400)                  
t2(x7)              0x00000000800007a5(2147485605)                  0x00000000800007a5(2147485605)                  
fp(x8)              0x000000008017f748(2149054280)                  0x000000008017f748(2149054280)                  
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x00000000802005f4(2149582324)                  0x00000000802005f4(2149582324)                  
a1(x11)             0x00000000801ff4e0(2149577952)                  0x00000000801ff4e0(2149577952)                  
a2(x12)             0x000000008018022d(2149057069)                  0x000000008018022d(2149057069)                  
a3(x13)             0x0000000080200086(2149580934)                  0x0000000080200086(2149580934)                  
a4(x14)             0x000000008017fde1(2149055969)                  0x000000008017fde1(2149055969)                  
a5(x15)             0x0000000000000021(33)                          0x0000000000000021(33)                          
a6(x16)             0x000000007ffffb77(2147482487)                  0x000000007ffffb77(2147482487)                  
a7(x17)             0x00000000e94e6758(3914229592)                  0x00000000e94e6758(3914229592)                  
s2(x18)             0x000000008017fbb9(2149055417)                  0x000000008017fbb9(2149055417)                  
s3(x19)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x00000000000000a8(168)                         0x00000000000000a8(168)                         
s6(x22)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s7(x23)             0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
s8(x24)             0x000000008017f168(2149052776)                  0x000000008017f168(2149052776)                  
s9(x25)             0x00000000800005f8(2147485176)                  0x00000000800005f8(2147485176)                  
s10(x26)            0x000000007ffffed9(2147483353)                  0x000000007ffffed9(2147483353)                  
s11(x27)            0xfffffffff8381000(18446744073579008000)        0xfffffffff8381000(18446744073579008000)        
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x000000008017fe57(2149056087)                  0x000000008017fe57(2149056087)                  
t5(x30)             0x0000000000000086(134)                         0x0000000000000086(134)                         
t6(x31)             0x000000008027f9cf(2150103503)                  0x000000008027f9cf(2150103503)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            53fe03978e519f26aece1d22b9574892fce75ecb        53fe03978e519f26aece1d22b9574892fce75ecb        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        6495492cd41c551d4d7ccd512c4120e46cea29aa        X
lastPC              0x0000000080000748(2147485512)                  0x0000000080000748(2147485512)                  
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

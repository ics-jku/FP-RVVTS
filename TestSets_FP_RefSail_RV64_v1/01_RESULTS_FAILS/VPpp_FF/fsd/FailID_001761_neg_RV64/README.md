# FailID_001761 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1761
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
_reg_f0: .byte 0x48,0x47,0xe3,0xe9,0x8f,0xad,0x05,0xe5
_reg_f1: .byte 0x00,0x00,0xe0,0x8e,0xd5,0x03,0xe0,0x41
_reg_f2: .byte 0xef,0x9d,0x11,0x89,0x0a,0x13,0x15,0x41
_reg_f3: .byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f4: .byte 0xf3,0x91,0x01,0x34,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x1c,0xaf,0xcd,0xa8,0x30,0x6e,0x0a,0xfd
_reg_f10:.byte 0x4d,0xc2,0x2b,0x45,0x6c,0x01,0xa5,0x6a
_reg_f11:.byte 0x00,0x00,0x00,0xe0,0x2e,0x99,0xd2,0xc1
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x97,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x6d,0xb4,0x88,0x69,0xc0,0xd8,0x6a,0x0f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x83,0xb2,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x84
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x3fffff1a0000000     // ra
    li x2, 0x7ffffc43            // sp
    li x3, 0x80199200            // gp
    li x4, 0x80180512            // tp
    li x5, 0x80180478            // t0
    li x6, 0x8000059b            // t1
    li x7, 0xffffffffd2bce000    // t2
    li x8, 0x800003ee            // fp
    li x9, 0x91                  // s1
    li x10, 0x8018038d           // a0
    li x11, 0x21                 // a1
    li x12, 0x7ffffb9b           // a2
    li x13, 0x56                 // a3
    li x14, 0x4                  // a4
    li x15, 0x8                  // a5
    li x16, 0x802003fd           // a6
    li x17, 0x1                  // a7
    li x18, 0x80000f22           // s2
    li x19, 0x10c71768           // s3
    li x20, 0x8018023d           // s4
    li x21, 0x800004d8           // s5
    li x22, 0x1                  // s6
    li x23, 0x0                  // s7
    li x24, 0x82                 // s8
    li x25, 0x7f                 // s9
    li x26, 0x80199200           // s10
    li x27, 0x84                 // s11
    li x28, 0x802002b0           // t3
    li x29, 0x6000               // t4
    li x30, 0x80180023           // t5
    li x31, 0x7ffffb9d           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f24', 'x3'}, 'clob': {'x30', 'x3'}})
    
    li x30, 0xffff8
    and x3, x3, x30
    li x30, 0x8017fde6
    add x3, x3, x30
    fsd f24, 0x21a(x3)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2ba996a5c61025117f95931c9f37364d54740e0a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f24, 0x21a(x3)
+========================================================================================================================+
Attributes:  fcsr ['overflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2ba996a5c61025117f95931c9f37364d54740e0a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f24, x21, x3
gp(x3)              0x0000000080218fe6(2149683174)                  0x0000000080218fe6(2149683174)
s5(x21)             0x00000000800004d8(2147484888)                  0x00000000800004d8(2147484888)
f24                 0xffffffffffffb283(-0.2034912109375_h)          0xffffffffffffb283(-0.2034912109375_h)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x03fffff1a0000000(288230314411556864)          0x03fffff1a0000000(288230314411556864)          
sp(x2)              0x000000007ffffc43(2147482691)                  0x000000007ffffc43(2147482691)                  
gp(x3)              0x0000000080218fe6(2149683174)                  0x0000000080218fe6(2149683174)                  
tp(x4)              0x0000000080180512(2149057810)                  0x0000000080180512(2149057810)                  
t0(x5)              0x0000000080180478(2149057656)                  0x0000000080180478(2149057656)                  
t1(x6)              0x000000008000059b(2147485083)                  0x000000008000059b(2147485083)                  
t2(x7)              0xffffffffd2bce000(18446744072950177792)        0xffffffffd2bce000(18446744072950177792)        
fp(x8)              0x00000000800003ee(2147484654)                  0x00000000800003ee(2147484654)                  
s1(x9)              0x0000000000000091(145)                         0x0000000000000091(145)                         
a0(x10)             0x000000008018038d(2149057421)                  0x000000008018038d(2149057421)                  
a1(x11)             0x0000000000000021(33)                          0x0000000000000021(33)                          
a2(x12)             0x000000007ffffb9b(2147482523)                  0x000000007ffffb9b(2147482523)                  
a3(x13)             0x0000000000000056(86)                          0x0000000000000056(86)                          
a4(x14)             0x0000000000000004(4)                           0x0000000000000004(4)                           
a5(x15)             0x0000000000000008(8)                           0x0000000000000008(8)                           
a6(x16)             0x00000000802003fd(2149581821)                  0x00000000802003fd(2149581821)                  
a7(x17)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s2(x18)             0x0000000080000f22(2147487522)                  0x0000000080000f22(2147487522)                  
s3(x19)             0x0000000010c71768(281483112)                   0x0000000010c71768(281483112)                   
s4(x20)             0x000000008018023d(2149057085)                  0x000000008018023d(2149057085)                  
s5(x21)             0x00000000800004d8(2147484888)                  0x00000000800004d8(2147484888)                  
s6(x22)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x0000000000000082(130)                         0x0000000000000082(130)                         
s9(x25)             0x000000000000007f(127)                         0x000000000000007f(127)                         
s10(x26)            0x0000000080199200(2149159424)                  0x0000000080199200(2149159424)                  
s11(x27)            0x0000000000000084(132)                         0x0000000000000084(132)                         
t3(x28)             0x00000000802002b0(2149581488)                  0x00000000802002b0(2149581488)                  
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x000000008017fde6(2149055974)                  0x000000008017fde6(2149055974)                  
t6(x31)             0x000000007ffffb9d(2147482525)                  0x000000007ffffb9d(2147482525)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            4472b4ec98a3a1db022d5553c9dbccaa05036355        4472b4ec98a3a1db022d5553c9dbccaa05036355        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2ba996a5c61025117f95931c9f37364d54740e0a        X
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000084(132)                         0x0000000000000084(132)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  
f1                  0x41e003d58ee00000(2149493879.0_d)              0x41e003d58ee00000(2149493879.0_d)              
f2                  0x4115130a89119def(345282.63385626575_d)        0x4115130a89119def(345282.63385626575_d)        
f3                  0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f4                  0xffffffff340191f3(1.2067157229012082e-07_s)    0xffffffff340191f3(1.2067157229012082e-07_s)    
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  
f10                 0x6aa5016c452bc24d(5.268673489679908e+205_d)    0x6aa5016c452bc24d(5.268673489679908e+205_d)    
f11                 0xc1d2992ee0000000(-1248115584.0_d)             0xc1d2992ee0000000(-1248115584.0_d)             
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f14                 0xffffffff00000297(9.290608818473537e-43_s)     0xffffffff00000297(9.290608818473537e-43_s)     
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffff4f000000(2147483648.0_s)              0xffffffff4f000000(2147483648.0_s)              
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x0f6ad8c06988b46d(2.1108825482638558e-234_d)   0x0f6ad8c06988b46d(2.1108825482638558e-234_d)   
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f23                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f24                 0xffffffffffffb283(-0.2034912109375_h)          0xffffffffffffb283(-0.2034912109375_h)          
f25                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f26                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

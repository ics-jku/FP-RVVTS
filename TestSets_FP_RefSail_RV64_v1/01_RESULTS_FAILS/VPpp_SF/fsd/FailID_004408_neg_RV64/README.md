# FailID_004408 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4408
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x04,0x01,0x20,0x80,0x00,0x00,0x00,0x00
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x80,0xff,0x03,0xe0,0x41
_reg_f11:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x20,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f21:.byte 0x1f,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0xf7,0x04,0x35,0x47,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x21
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017fb4e            // ra
    li x2, 0x80000262            // sp
    li x3, 0x1                   // gp
    li x4, 0x211bc230201b823     // tp
    li x5, 0xfffffffffffffded    // t0
    li x6, 0x802009b1            // t1
    li x7, 0x11803               // t2
    li x8, 0x1                   // fp
    li x9, 0x0                   // s1
    li x10, 0x89                 // a0
    li x11, 0x8000058c           // a1
    li x12, 0x8017fc27           // a2
    li x13, 0x801ff23d           // a3
    li x14, 0x80180552           // a4
    li x15, 0x800000ae           // a5
    li x16, 0x1004               // a6
    li x17, 0x4a141000           // a7
    li x18, 0x801809b6           // s2
    li x19, 0x80000380           // s3
    li x20, 0x8017fd5f           // s4
    li x21, 0xd2000553           // s5
    li x22, 0x0                  // s6
    li x23, 0x80031d1f           // s7
    li x24, 0x1                  // s8
    li x25, 0x4c                 // s9
    li x26, 0x7ffffda6           // s10
    li x27, 0x8000032c           // s11
    li x28, 0x80200222           // t3
    li x29, 0x8017fc72           // t4
    li x30, 0x3ffff              // t5
    li x31, 0x8017fdd0           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x26', 'f19'}, 'clob': {'x9', 'x26'}})
    
    li x9, 0xffff8
    and x26, x26, x9
    li x9, 0x8017fb7b
    add x26, x26, x9
    fsd f19, 0x485(x26)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        29307558edfa6e5122e21d1fa8fbae7f5db9f24a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f19, 0x485(x26)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        29307558edfa6e5122e21d1fa8fbae7f5db9f24a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f19, x485, x26
s10(x26)            0x000000008027f91b(2150103323)                  0x000000008027f91b(2150103323)
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fb4e(2149055310)                  0x000000008017fb4e(2149055310)                  
sp(x2)              0x0000000080000262(2147484258)                  0x0000000080000262(2147484258)                  
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x0211bc230201b823(149107121223481379)          0x0211bc230201b823(149107121223481379)          
t0(x5)              0xfffffffffffffded(18446744073709551085)        0xfffffffffffffded(18446744073709551085)        
t1(x6)              0x00000000802009b1(2149583281)                  0x00000000802009b1(2149583281)                  
t2(x7)              0x0000000000011803(71683)                       0x0000000000011803(71683)                       
fp(x8)              0x0000000000000001(1)                           0x0000000000000001(1)                           
s1(x9)              0x000000008017fb7b(2149055355)                  0x000000008017fb7b(2149055355)                  
a0(x10)             0x0000000000000089(137)                         0x0000000000000089(137)                         
a1(x11)             0x000000008000058c(2147485068)                  0x000000008000058c(2147485068)                  
a2(x12)             0x000000008017fc27(2149055527)                  0x000000008017fc27(2149055527)                  
a3(x13)             0x00000000801ff23d(2149577277)                  0x00000000801ff23d(2149577277)                  
a4(x14)             0x0000000080180552(2149057874)                  0x0000000080180552(2149057874)                  
a5(x15)             0x00000000800000ae(2147483822)                  0x00000000800000ae(2147483822)                  
a6(x16)             0x0000000000001004(4100)                        0x0000000000001004(4100)                        
a7(x17)             0x000000004a141000(1242828800)                  0x000000004a141000(1242828800)                  
s2(x18)             0x00000000801809b6(2149058998)                  0x00000000801809b6(2149058998)                  
s3(x19)             0x0000000080000380(2147484544)                  0x0000000080000380(2147484544)                  
s4(x20)             0x000000008017fd5f(2149055839)                  0x000000008017fd5f(2149055839)                  
s5(x21)             0x00000000d2000553(3523216723)                  0x00000000d2000553(3523216723)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000080031d1f(2147687711)                  0x0000000080031d1f(2147687711)                  
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x000000000000004c(76)                          0x000000000000004c(76)                          
s10(x26)            0x000000008027f91b(2150103323)                  0x000000008027f91b(2150103323)                  
s11(x27)            0x000000008000032c(2147484460)                  0x000000008000032c(2147484460)                  
t3(x28)             0x0000000080200222(2149581346)                  0x0000000080200222(2149581346)                  
t4(x29)             0x000000008017fc72(2149055602)                  0x000000008017fc72(2149055602)                  
t5(x30)             0x000000000003ffff(262143)                      0x000000000003ffff(262143)                      
t6(x31)             0x000000008017fdd0(2149055952)                  0x000000008017fdd0(2149055952)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            90606150454ea0a3cbddd740c097b0c9633877a1        90606150454ea0a3cbddd740c097b0c9633877a1        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        29307558edfa6e5122e21d1fa8fbae7f5db9f24a        X
lastPC              0x0000000080000774(2147485556)                  0x0000000080000774(2147485556)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000021(33)                          0x0000000000000021(33)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f3                  0x0000000080200104(1.0620341547e-314_d)         0x0000000080200104(1.0620341547e-314_d)         
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x41e003ff80000000(2149579776.0_d)              0x41e003ff80000000(2149579776.0_d)              
f11                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff80000000(-0.0_s)                      0xffffffff80000000(-0.0_s)                      
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0x0000000000000020(1.6e-322_d)                  0x0000000000000020(1.6e-322_d)                  
f21                 0xffffffff0000001f(4.344025239406933e-44_s)     0xffffffff0000001f(4.344025239406933e-44_s)     
f22                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffff473504f7(46340.96484375_s)            0xffffffff473504f7(46340.96484375_s)            
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

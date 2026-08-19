# FailID_001823 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1823
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f2: .byte 0x40,0x07,0x18,0x80,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x05,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x20,0xc5,0x00,0x00,0xe0,0x41
_reg_f7: .byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x77,0x01,0x00,0x80,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x88
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x6000                // ra
    li x2, 0x80000595            // sp
    li x3, 0x801800d8            // gp
    li x4, 0x800004e8            // tp
    li x5, 0x801804e5            // t0
    li x6, 0x0                   // t1
    li x7, 0x0                   // t2
    li x8, 0x8028059d00          // fp
    li x9, 0x80000633            // s1
    li x10, 0x801804c7           // a0
    li x11, 0x6000               // a1
    li x12, 0x80000177           // a2
    li x13, 0x80180801           // a3
    li x14, 0x60                 // a4
    li x15, 0x0                  // a5
    li x16, 0xfffffffff64af000   // a6
    li x17, 0x8017f9b9           // a7
    li x18, 0x801804a7           // s2
    li x19, 0x8018066c           // s3
    li x20, 0xcb                 // s4
    li x21, 0x8017f9e1           // s5
    li x22, 0x801804e5           // s6
    li x23, 0x800009ee           // s7
    li x24, 0x1                  // s8
    li x25, 0x300000             // s9
    li x26, 0x802802             // s10
    li x27, 0x800007ee           // s11
    li x28, 0xffffffffffff91f3   // t3
    li x29, 0xbdb80760           // t4
    li x30, 0x80180621           // t5
    li x31, 0x1                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f10', 'x9'}, 'clob': {'x9', 'x17'}})
    
    li x17, 0xffff8
    and x9, x9, x17
    li x17, 0x8017fba6
    add x9, x9, x17
    fsd f10, 0x45a(x9)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        4b62543c95b97252583aa56bce51b81ca3658977        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f10, 0x45a(x9)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        4b62543c95b97252583aa56bce51b81ca3658977        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f10, x45, x9
s1(x9)              0x00000000801801d6(2149056982)                  0x00000000801801d6(2149056982)
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
sp(x2)              0x0000000080000595(2147485077)                  0x0000000080000595(2147485077)                  
gp(x3)              0x00000000801800d8(2149056728)                  0x00000000801800d8(2149056728)                  
tp(x4)              0x00000000800004e8(2147484904)                  0x00000000800004e8(2147484904)                  
t0(x5)              0x00000000801804e5(2149057765)                  0x00000000801804e5(2149057765)                  
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x0000008028059d00(550427270400)                0x0000008028059d00(550427270400)                
s1(x9)              0x00000000801801d6(2149056982)                  0x00000000801801d6(2149056982)                  
a0(x10)             0x00000000801804c7(2149057735)                  0x00000000801804c7(2149057735)                  
a1(x11)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a2(x12)             0x0000000080000177(2147484023)                  0x0000000080000177(2147484023)                  
a3(x13)             0x0000000080180801(2149058561)                  0x0000000080180801(2149058561)                  
a4(x14)             0x0000000000000060(96)                          0x0000000000000060(96)                          
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0xfffffffff64af000(18446744073546690560)        0xfffffffff64af000(18446744073546690560)        
a7(x17)             0x000000008017fba6(2149055398)                  0x000000008017fba6(2149055398)                  
s2(x18)             0x00000000801804a7(2149057703)                  0x00000000801804a7(2149057703)                  
s3(x19)             0x000000008018066c(2149058156)                  0x000000008018066c(2149058156)                  
s4(x20)             0x00000000000000cb(203)                         0x00000000000000cb(203)                         
s5(x21)             0x000000008017f9e1(2149054945)                  0x000000008017f9e1(2149054945)                  
s6(x22)             0x00000000801804e5(2149057765)                  0x00000000801804e5(2149057765)                  
s7(x23)             0x00000000800009ee(2147486190)                  0x00000000800009ee(2147486190)                  
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x0000000000300000(3145728)                     0x0000000000300000(3145728)                     
s10(x26)            0x0000000000802802(8398850)                     0x0000000000802802(8398850)                     
s11(x27)            0x00000000800007ee(2147485678)                  0x00000000800007ee(2147485678)                  
t3(x28)             0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)        
t4(x29)             0x00000000bdb80760(3182954336)                  0x00000000bdb80760(3182954336)                  
t5(x30)             0x0000000080180621(2149058081)                  0x0000000080180621(2149058081)                  
t6(x31)             0x0000000000000001(1)                           0x0000000000000001(1)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            0ac83595cb12217ac7bce5ad86bcec8459980d56        0ac83595cb12217ac7bce5ad86bcec8459980d56        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        4b62543c95b97252583aa56bce51b81ca3658977        X
lastPC              0x0000000080000764(2147485540)                  0x0000000080000764(2147485540)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000088(136)                         0x0000000000000088(136)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f2                  0xffffffff80180740(-2.206652717741576e-39_s)    0xffffffff80180740(-2.206652717741576e-39_s)    
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff4f000005(2147484928.0_s)              0xffffffff4f000005(2147484928.0_s)              
f6                  0x41e00000c5200000(2147485225.0_d)              0x41e00000c5200000(2147485225.0_d)              
f7                  0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x0000000080000177(1.060998081e-314_d)          0x0000000080000177(1.060998081e-314_d)          
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
STATES DIFFER: True
```

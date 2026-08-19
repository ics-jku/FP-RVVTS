# FailID_001810 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1810
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
_reg_f0: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f1: .byte 0xb4,0xd0,0xa5,0xba,0xfa,0x00,0xfd,0xb3
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f3: .byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0xd9,0xfc,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xd0
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x37                  // ra
    li x2, 0x9cb4c760            // sp
    li x3, 0x0                   // gp
    li x4, 0x8017fdc8            // tp
    li x5, 0x6000                // t0
    li x6, 0xffffffffffffffff    // t1
    li x7, 0x80180063            // t2
    li x8, 0x7ffffe14            // fp
    li x9, 0x8017fabf            // s1
    li x10, 0x6ffe000            // a0
    li x11, 0x1                  // a1
    li x12, 0x8018011f           // a2
    li x13, 0x8017fe49           // a3
    li x14, 0x80134a1e           // a4
    li x15, 0x1                  // a5
    li x16, 0x8017fe49           // a6
    li x17, 0x6000               // a7
    li x18, 0x200                // s2
    li x19, 0x80000ae4           // s3
    li x20, 0x80000326           // s4
    li x21, 0x200                // s5
    li x22, 0xa8464730           // s6
    li x23, 0x6c                 // s7
    li x24, 0x8007f18a           // s8
    li x25, 0x6000               // s9
    li x26, 0x0                  // s10
    li x27, 0x8000023c           // s11
    li x28, 0x0                  // t3
    li x29, 0x65130760           // t4
    li x30, 0xffffffffcd24c000   // t5
    li x31, 0xfffffffffffffaa5   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x31', 'f17'}, 'clob': {'x12', 'x31'}})
    
    li x12, 0xffff8
    and x31, x31, x12
    li x12, 0x80180344
    add x31, x31, x12
    fsd f17, -0x344(x31)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5f55cb22d7913b31b9bb6149cfd8edad7b1731cd        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f17, -0x344(x31)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5f55cb22d7913b31b9bb6149cfd8edad7b1731cd        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f17, x344, x31
t6(x31)             0x000000008027fde4(2150104548)                  0x000000008027fde4(2150104548)
f17                 0xfffffffffffffcd9(nan_h)                       0xfffffffffffffcd9(nan_h)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000037(55)                          0x0000000000000037(55)                          
sp(x2)              0x000000009cb4c760(2629093216)                  0x000000009cb4c760(2629093216)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x000000008017fdc8(2149055944)                  0x000000008017fdc8(2149055944)                  
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t1(x6)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t2(x7)              0x0000000080180063(2149056611)                  0x0000000080180063(2149056611)                  
fp(x8)              0x000000007ffffe14(2147483156)                  0x000000007ffffe14(2147483156)                  
s1(x9)              0x000000008017fabf(2149055167)                  0x000000008017fabf(2149055167)                  
a0(x10)             0x0000000006ffe000(117432320)                   0x0000000006ffe000(117432320)                   
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x0000000080180344(2149057348)                  0x0000000080180344(2149057348)                  
a3(x13)             0x000000008017fe49(2149056073)                  0x000000008017fe49(2149056073)                  
a4(x14)             0x0000000080134a1e(2148747806)                  0x0000000080134a1e(2148747806)                  
a5(x15)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a6(x16)             0x000000008017fe49(2149056073)                  0x000000008017fe49(2149056073)                  
a7(x17)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s2(x18)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s3(x19)             0x0000000080000ae4(2147486436)                  0x0000000080000ae4(2147486436)                  
s4(x20)             0x0000000080000326(2147484454)                  0x0000000080000326(2147484454)                  
s5(x21)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s6(x22)             0x00000000a8464730(2823178032)                  0x00000000a8464730(2823178032)                  
s7(x23)             0x000000000000006c(108)                         0x000000000000006c(108)                         
s8(x24)             0x000000008007f18a(2148004234)                  0x000000008007f18a(2148004234)                  
s9(x25)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000008000023c(2147484220)                  0x000000008000023c(2147484220)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x0000000065130760(1695745888)                  0x0000000065130760(1695745888)                  
t5(x30)             0xffffffffcd24c000(18446744072856322048)        0xffffffffcd24c000(18446744072856322048)        
t6(x31)             0x000000008027fde4(2150104548)                  0x000000008027fde4(2150104548)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            8080cfc6ef886ebd2389d7024dc7cc8c0b459ae4        8080cfc6ef886ebd2389d7024dc7cc8c0b459ae4        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5f55cb22d7913b31b9bb6149cfd8edad7b1731cd        X
lastPC              0x0000000080000734(2147485492)                  0x0000000080000734(2147485492)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000d0(208)                         0x00000000000000d0(208)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f1                  0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    
f2                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f3                  0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xfffffffffffffcd9(nan_h)                       0xfffffffffffffcd9(nan_h)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f20                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f28                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f29                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
STATES DIFFER: True
```

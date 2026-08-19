# FailID_000284 ARA pos RV64 fsqrt.d

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 284
* Isolated failing instruction: `fsqrt.d`
* Minimized failing test case: [cblock_minimized_test_case.json](cblock_minimized_test_case.json)
* Resulting REF machine state: [mstate_RefSail.json](mstate_RefSail.json)
* Resulting DUT machine state: [mstate_DUT_ARA.json](mstate_DUT_ARA.json)
* Automated failure characterization report: [AFC_FP_report.log](AFC_FP_report.log)

## Report

### Minimized Failing Test Case
```
    // FLOATINGPOINT STATE DATA
    j _float_data_end
    .align 4
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x53,0x07,0x00,0xd2,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x08,0x40
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0xe0,0xb3,0x00,0x03,0xe0,0x41
_reg_f10:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0xb0,0x68,0xe8,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x1a,0xd0,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x20,0x42,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x1e,0xff,0x02,0xe0,0x41
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x44,0x40
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f31:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x50
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x0                   // sp
    li x3, 0x0                   // gp
    li x4, 0xffffffffffffffff    // tp
    li x5, 0x7ff8000000000000    // t0
    li x6, 0x801801a6            // t1
    li x7, 0x8017f95c            // t2
    li x8, 0xffffffffffffffff    // fp
    li x9, 0x1                   // s1
    li x10, 0xffffffffffffffff   // a0
    li x11, 0x1                  // a1
    li x12, 0x0                  // a2
    li x13, 0x0                  // a3
    li x14, 0x8018040b           // a4
    li x15, 0x0                  // a5
    li x16, 0x6e650000           // a6
    li x17, 0x0                  // a7
    li x18, 0x801805ed           // s2
    li x19, 0x800006a3           // s3
    li x20, 0x801805ed           // s4
    li x21, 0x8018035d           // s5
    li x22, 0x0                  // s6
    li x23, 0xffffffffffffffff   // s7
    li x24, 0x80180aab           // s8
    li x25, 0xffffffff7fe80769   // s9
    li x26, 0x6000               // s10
    li x27, 0x28                 // s11
    li x28, 0x1                  // t3
    li x29, 0xffffffffffffffff   // t4
    li x30, 0x3                  // t5
    li x31, 0x70901000           // t6
    // INSTRUCTION ({'dep': {'f20', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'f13'}})
    fsqrt.d f13, f20, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f13                 0x40e6a2bcbc272086(46357.89796787598_d)         0x40e6a2bcbc272087(46357.897967875986_d)        X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.d f13, f20, dyn
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f13                 0x40e6a2bcbc272086(46357.89796787598_d)         0x40e6a2bcbc272087(46357.897967875986_d)        X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, f20
f13                 0x40e6a2bcbc272086(46357.89796787598_d)         0x40e6a2bcbc272087(46357.897967875986_d)        X
f20                 0x41e002ff1e000000(2149054704.0_d)              0x41e002ff1e000000(2149054704.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t0(x5)              0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
t1(x6)              0x00000000801801a6(2149056934)                  0x00000000801801a6(2149056934)                  
t2(x7)              0x000000008017f95c(2149054812)                  0x000000008017f95c(2149054812)                  
fp(x8)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x000000008018040b(2149057547)                  0x000000008018040b(2149057547)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x000000006e650000(1852112896)                  0x000000006e650000(1852112896)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x00000000801805ed(2149058029)                  0x00000000801805ed(2149058029)                  
s3(x19)             0x00000000800006a3(2147485347)                  0x00000000800006a3(2147485347)                  
s4(x20)             0x00000000801805ed(2149058029)                  0x00000000801805ed(2149058029)                  
s5(x21)             0x000000008018035d(2149057373)                  0x000000008018035d(2149057373)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s8(x24)             0x0000000080180aab(2149059243)                  0x0000000080180aab(2149059243)                  
s9(x25)             0xffffffff7fe80769(18446744071560497001)        0xffffffff7fe80769(18446744071560497001)        
s10(x26)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s11(x27)            0x0000000000000028(40)                          0x0000000000000028(40)                          
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t5(x30)             0x0000000000000003(3)                           0x0000000000000003(3)                           
t6(x31)             0x0000000070901000(1888489472)                  0x0000000070901000(1888489472)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            27e6fe72a5d6aac18f4ec83a7a987b7e9e0e3a6c        27e6fe72a5d6aac18f4ec83a7a987b7e9e0e3a6c        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800006e8(2147485416)                  0x00000000800006e8(2147485416)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000051(81)                          0x0000000000000051(81)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffffd2000753(-137469673472.0_s)           0xffffffffd2000753(-137469673472.0_s)           
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x4008000000000000(3.0_d)                       0x4008000000000000(3.0_d)                       
f6                  0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x41e00300b3e00000(2149057951.0_d)              0x41e00300b3e00000(2149057951.0_d)              
f10                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x40e6a2bcbc272086(46357.89796787598_d)         0x40e6a2bcbc272087(46357.897967875986_d)        X
f14                 0xffffffffceffd01a(-2145914112.0_s)             0xffffffffceffd01a(-2145914112.0_s)             
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff42200000(40.0_s)                      0xffffffff42200000(40.0_s)                      
f20                 0x41e002ff1e000000(2149054704.0_d)              0x41e002ff1e000000(2149054704.0_d)              
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x4044000000000000(40.0_d)                      0x4044000000000000(40.0_d)                      
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

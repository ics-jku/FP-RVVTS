# FailID_002149 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2149
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x89,0x79,0x4d,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x93,0x17,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0xfc,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0xbc,0x6d,0x47,0xe2,0xcd,0xd0,0x0c,0x74
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'dyn(0b111)', 'res': 0}
    li t0, 0xe4
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x9298a720            // ra
    li x2, 0x7fffffd9            // sp
    li x3, 0x0                   // gp
    li x4, 0x0                   // tp
    li x5, 0xffffffffffffb303    // t0
    li x6, 0x802065db            // t1
    li x7, 0x8018042e            // t2
    li x8, 0x6000                // fp
    li x9, 0x80200392            // s1
    li x10, 0x80180516           // a0
    li x11, 0x200                // a1
    li x12, 0x80000755           // a2
    li x13, 0x7fffffff           // a3
    li x14, 0xe4                 // a4
    li x15, 0x800002e4           // a5
    li x16, 0x8017f956           // a6
    li x17, 0x6000               // a7
    li x18, 0x8018076b           // s2
    li x19, 0xffffffffe3346000   // s3
    li x20, 0x7fffffff           // s4
    li x21, 0x80180634           // s5
    li x22, 0x8018063400000      // s6
    li x23, 0x800000cf           // s7
    li x24, 0x0                  // s8
    li x25, 0x0                  // s9
    li x26, 0x1                  // s10
    li x27, 0x800062e4           // s11
    li x28, 0x0                  // t3
    li x29, 0x1805e5             // t4
    li x30, 0x0                  // t5
    li x31, 0x8017f956           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f4', 'x23'}, 'clob': {'x30', 'x23'}})
    
    li x30, 0xffffc
    and x23, x23, x30
    li x30, 0x8017fe48
    add x23, x23, x30
    fsw f4, 0x1b8(x23)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        638bc6bc5ef63dd4b0e6e421f19204bfb285d4c0        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f4, 0x1b8(x23)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        638bc6bc5ef63dd4b0e6e421f19204bfb285d4c0        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f4, x1, b8, x23
ra(x1)              0x000000009298a720(2459477792)                  0x000000009298a720(2459477792)
s7(x23)             0x000000008017ff14(2149056276)                  0x000000008017ff14(2149056276)
f4                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000009298a720(2459477792)                  0x000000009298a720(2459477792)                  
sp(x2)              0x000000007fffffd9(2147483609)                  0x000000007fffffd9(2147483609)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0xffffffffffffb303(18446744073709531907)        0xffffffffffffb303(18446744073709531907)        
t1(x6)              0x00000000802065db(2149606875)                  0x00000000802065db(2149606875)                  
t2(x7)              0x000000008018042e(2149057582)                  0x000000008018042e(2149057582)                  
fp(x8)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s1(x9)              0x0000000080200392(2149581714)                  0x0000000080200392(2149581714)                  
a0(x10)             0x0000000080180516(2149057814)                  0x0000000080180516(2149057814)                  
a1(x11)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a2(x12)             0x0000000080000755(2147485525)                  0x0000000080000755(2147485525)                  
a3(x13)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a4(x14)             0x00000000000000e4(228)                         0x00000000000000e4(228)                         
a5(x15)             0x00000000800002e4(2147484388)                  0x00000000800002e4(2147484388)                  
a6(x16)             0x000000008017f956(2149054806)                  0x000000008017f956(2149054806)                  
a7(x17)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s2(x18)             0x000000008018076b(2149058411)                  0x000000008018076b(2149058411)                  
s3(x19)             0xffffffffe3346000(18446744073226444800)        0xffffffffe3346000(18446744073226444800)        
s4(x20)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s5(x21)             0x0000000080180634(2149058100)                  0x0000000080180634(2149058100)                  
s6(x22)             0x0008018063400000(2253450746265600)            0x0008018063400000(2253450746265600)            
s7(x23)             0x000000008017ff14(2149056276)                  0x000000008017ff14(2149056276)                  
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000001(1)                           0x0000000000000001(1)                           
s11(x27)            0x00000000800062e4(2147508964)                  0x00000000800062e4(2147508964)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x00000000001805e5(1574373)                     0x00000000001805e5(1574373)                     
t5(x30)             0x000000008017fe48(2149056072)                  0x000000008017fe48(2149056072)                  
t6(x31)             0x000000008017f956(2149054806)                  0x000000008017f956(2149054806)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            9f78e9119ab8779e27dd09fe193991fe8bba4e35        9f78e9119ab8779e27dd09fe193991fe8bba4e35        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        638bc6bc5ef63dd4b0e6e421f19204bfb285d4c0        X
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000e4(228)                         0x00000000000000e4(228)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            dyn(0b111)                                      dyn(0b111)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff4d798900(261656576.0_s)               0xffffffff4d798900(261656576.0_s)               
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7fffffff4f001793(nan_d)                       0x7fffffff4f001793(nan_d)                       
f22                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xfffffffffffffc00(-inf_h)                      0xfffffffffffffc00(-inf_h)                      
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x740cd0cde2476dbc(1.0315604867321677e+251_d)   0x740cd0cde2476dbc(1.0315604867321677e+251_d)   
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

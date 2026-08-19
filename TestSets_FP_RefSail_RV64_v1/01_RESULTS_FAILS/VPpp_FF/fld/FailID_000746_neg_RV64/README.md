# FailID_000746 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 746
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0x08,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x93,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x9f,0xc6,0x2d,0x21,0x36,0x22,0xbc,0x65
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x93,0x17,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x80,0xbf,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0xbc,0x6d,0x47,0xe2,0xcd,0xd0,0x0c,0x74
_reg_f30:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x48
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8000035c            // ra
    li x2, 0x0                   // sp
    li x3, 0x8017fd21            // gp
    li x4, 0x0                   // tp
    li x5, 0x1                   // t0
    li x6, 0x8000035c            // t1
    li x7, 0x802004fb            // t2
    li x8, 0x0                   // fp
    li x9, 0x800007e4            // s1
    li x10, 0x80000642           // a0
    li x11, 0x229aa000           // a1
    li x12, 0x65bc2236212dc69f   // a2
    li x13, 0xffffffffffffffff   // a3
    li x14, 0x800006ab           // a4
    li x15, 0x91f3               // a5
    li x16, 0x0                  // a6
    li x17, 0x7c3                // a7
    li x18, 0x6000               // s2
    li x19, 0x7fffffff           // s3
    li x20, 0xffffffff7ffffe23   // s4
    li x21, 0x0                  // s5
    li x22, 0x80000439           // s6
    li x23, 0x7fffffffffffffff   // s7
    li x24, 0x8017f95b           // s8
    li x25, 0x800007e4           // s9
    li x26, 0x0                  // s10
    li x27, 0x8018027d           // s11
    li x28, 0xffffffffffffffff   // t3
    li x29, 0x7fffffff           // t4
    li x30, 0x8000000000000396   // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x15'}, 'clob': {'x11', 'f19', 'x15'}})
    
    li x11, 0x1ffff8
    and x15, x15, x11
    li x11, 0x8000044e
    add x15, x15, x11
    fld f19, -0x44e(x15)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f19, -0x44e(x15)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f19, x44, x15
a5(x15)             0x000000008000963e(2147522110)                  0x000000008000963e(2147522110)
f19                 0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008000035c(2147484508)                  0x000000008000035c(2147484508)                  
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x000000008017fd21(2149055777)                  0x000000008017fd21(2149055777)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t1(x6)              0x000000008000035c(2147484508)                  0x000000008000035c(2147484508)                  
t2(x7)              0x00000000802004fb(2149582075)                  0x00000000802004fb(2149582075)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x00000000800007e4(2147485668)                  0x00000000800007e4(2147485668)                  
a0(x10)             0x0000000080000642(2147485250)                  0x0000000080000642(2147485250)                  
a1(x11)             0x000000008000044e(2147484750)                  0x000000008000044e(2147484750)                  
a2(x12)             0x65bc2236212dc69f(7330771909332551327)         0x65bc2236212dc69f(7330771909332551327)         
a3(x13)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a4(x14)             0x00000000800006ab(2147485355)                  0x00000000800006ab(2147485355)                  
a5(x15)             0x000000008000963e(2147522110)                  0x000000008000963e(2147522110)                  
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x00000000000007c3(1987)                        0x00000000000007c3(1987)                        
s2(x18)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s3(x19)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s4(x20)             0xffffffff7ffffe23(18446744071562067491)        0xffffffff7ffffe23(18446744071562067491)        
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000080000439(2147484729)                  0x0000000080000439(2147484729)                  
s7(x23)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s8(x24)             0x000000008017f95b(2149054811)                  0x000000008017f95b(2149054811)                  
s9(x25)             0x00000000800007e4(2147485668)                  0x00000000800007e4(2147485668)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000008018027d(2149057149)                  0x000000008018027d(2149057149)                  
t3(x28)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t4(x29)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
t5(x30)             0x8000000000000396(9223372036854776726)         0x8000000000000396(9223372036854776726)         
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            7e059e0a6bb23b51583425ee46ebbde98564b101        7e059e0a6bb23b51583425ee46ebbde98564b101        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000048(72)                          0x0000000000000048(72)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff4f000008(2147485696.0_s)              0xffffffff4f000008(2147485696.0_s)              
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff4f001793(2149028608.0_s)              0xffffffff4f001793(2149028608.0_s)              
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0x65bc2236212dc69f(1.1674097076675866e+182_d)   0x65bc2236212dc69f(1.1674097076675866e+182_d)   
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xfffffffffffffe00(nan_h)                       0xfffffffffffffe00(nan_h)                       
f19                 0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7fffffff4f001793(nan_d)                       0x7fffffff4f001793(nan_d)                       
f22                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0x7fffffff3f800000(nan_d)                       0x7fffffff3f800000(nan_d)                       
f25                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffffbf800000(-1.0_s)                      0xffffffffbf800000(-1.0_s)                      
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x740cd0cde2476dbc(1.0315604867321677e+251_d)   0x740cd0cde2476dbc(1.0315604867321677e+251_d)   
f30                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

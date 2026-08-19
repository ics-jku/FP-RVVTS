# FailID_000848 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 848
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x80,0x27,0x00,0x00,0xe0,0x41
_reg_f25:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f30:.byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x2
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7ffffdc2            // ra
    li x2, 0x1                   // sp
    li x3, 0x8017fd71            // gp
    li x4, 0x0                   // tp
    li x5, 0x80005fd1            // t0
    li x6, 0x81                  // t1
    li x7, 0x7fffffd1            // t2
    li x8, 0x1                   // fp
    li x9, 0x0                   // s1
    li x10, 0x80180330           // a0
    li x11, 0x7ffff88a           // a1
    li x12, 0x80005cad           // a2
    li x13, 0x8017fd6b           // a3
    li x14, 0x80180330           // a4
    li x15, 0xffffffffaf1e7000   // a5
    li x16, 0x80180215           // a6
    li x17, 0x800007d6           // a7
    li x18, 0x7fffffffffffffff   // s2
    li x19, 0x8017fc35           // s3
    li x20, 0x8017fb2b2bb        // s4
    li x21, 0x200                // s5
    li x22, 0x80000071           // s6
    li x23, 0x0                  // s7
    li x24, 0x7ffffa8a           // s8
    li x25, 0x80180494           // s9
    li x26, 0x0                  // s10
    li x27, 0x80000071           // s11
    li x28, 0xb5                 // t3
    li x29, 0x800007d6000000     // t4
    li x30, 0x0                  // t5
    li x31, 0xffffffffffffffff   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x30', 'mstatus.fs/vs.fs'}, 'clob': {'x30', 'x12', 'f19'}})
    
    li x12, 0x1ffff8
    and x30, x30, x12
    li x12, 0x7ffff9fc
    add x30, x30, x12
    fld f19, 0x604(x30)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0x0000000000000000(0.0_d)                       0x000000132140006f(4.05935308646e-313_d)        X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f19, 0x604(x30)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0x0000000000000000(0.0_d)                       0x000000132140006f(4.05935308646e-313_d)        X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f19, x604, x30
t5(x30)             0x000000007ffff9fc(2147482108)                  0x000000007ffff9fc(2147482108)
f19                 0x0000000000000000(0.0_d)                       0x000000132140006f(4.05935308646e-313_d)        X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffffdc2(2147483074)                  0x000000007ffffdc2(2147483074)                  
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)                           
gp(x3)              0x000000008017fd71(2149055857)                  0x000000008017fd71(2149055857)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000080005fd1(2147508177)                  0x0000000080005fd1(2147508177)                  
t1(x6)              0x0000000000000081(129)                         0x0000000000000081(129)                         
t2(x7)              0x000000007fffffd1(2147483601)                  0x000000007fffffd1(2147483601)                  
fp(x8)              0x0000000000000001(1)                           0x0000000000000001(1)                           
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x0000000080180330(2149057328)                  0x0000000080180330(2149057328)                  
a1(x11)             0x000000007ffff88a(2147481738)                  0x000000007ffff88a(2147481738)                  
a2(x12)             0x000000007ffff9fc(2147482108)                  0x000000007ffff9fc(2147482108)                  
a3(x13)             0x000000008017fd6b(2149055851)                  0x000000008017fd6b(2149055851)                  
a4(x14)             0x0000000080180330(2149057328)                  0x0000000080180330(2149057328)                  
a5(x15)             0xffffffffaf1e7000(18446744072352591872)        0xffffffffaf1e7000(18446744072352591872)        
a6(x16)             0x0000000080180215(2149057045)                  0x0000000080180215(2149057045)                  
a7(x17)             0x00000000800007d6(2147485654)                  0x00000000800007d6(2147485654)                  
s2(x18)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s3(x19)             0x000000008017fc35(2149055541)                  0x000000008017fc35(2149055541)                  
s4(x20)             0x000008017fb2b2bb(8802530407099)               0x000008017fb2b2bb(8802530407099)               
s5(x21)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s6(x22)             0x0000000080000071(2147483761)                  0x0000000080000071(2147483761)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x000000007ffffa8a(2147482250)                  0x000000007ffffa8a(2147482250)                  
s9(x25)             0x0000000080180494(2149057684)                  0x0000000080180494(2149057684)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x0000000080000071(2147483761)                  0x0000000080000071(2147483761)                  
t3(x28)             0x00000000000000b5(181)                         0x00000000000000b5(181)                         
t4(x29)             0x00800007d6000000(36028830674059264)           0x00800007d6000000(36028830674059264)           
t5(x30)             0x000000007ffff9fc(2147482108)                  0x000000007ffff9fc(2147482108)                  
t6(x31)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        

STATE               REF                                             DUT                                             DIFF
xmemhash            daef134ff73860b161ebf42ffb4a85276f62678d        daef134ff73860b161ebf42ffb4a85276f62678d        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000748(2147485512)                  0x0000000080000748(2147485512)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000002(2)                           0x0000000000000002(2)                           
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f8                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f16                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f17                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x0000000000000000(0.0_d)                       0x000000132140006f(4.05935308646e-313_d)        X
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x41e0000027800000(2147483964.0_d)              0x41e0000027800000(2147483964.0_d)              
f25                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f30                 0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

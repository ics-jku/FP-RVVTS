# FailID_001913 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1913
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x37,0xdd,0x64,0x28,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x07,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0xd7,0xdd,0x7c,0x96,0xf4,0x9b,0x21,0xc6
_reg_f10:.byte 0x07,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x48,0x40
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f15:.byte 0x49,0x2c,0x32,0x33,0x61,0x83,0x13,0x28
_reg_f16:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f17:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x39,0xfe,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x39,0xfe,0x17,0x80,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x30
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7fffffff            // ra
    li x2, 0x7ffffe47            // sp
    li x3, 0x801804ea            // gp
    li x4, 0x8017f937            // tp
    li x5, 0x80180764            // t0
    li x6, 0xa6                  // t1
    li x7, 0xcc1a0778            // t2
    li x8, 0x801806ea            // fp
    li x9, 0x0                   // s1
    li x10, 0xa3                 // a0
    li x11, 0x0                  // a1
    li x12, 0x0                  // a2
    li x13, 0x8017ff9f           // a3
    li x14, 0x7fc00000           // a4
    li x15, 0x271b423            // a5
    li x16, 0x0                  // a6
    li x17, 0x8017feb7           // a7
    li x18, 0x0                  // s2
    li x19, 0x80180622           // s3
    li x20, 0xf                  // s4
    li x21, 0xffffffffffffffff   // s5
    li x22, 0x7fc00000           // s6
    li x23, 0x0                  // s7
    li x24, 0x6000               // s8
    li x25, 0x6000               // s9
    li x26, 0x6000               // s10
    li x27, 0x7fffffffffffffff   // s11
    li x28, 0x80180643           // t3
    li x29, 0x7ffff9b6           // t4
    li x30, 0x7ffffa4f           // t5
    li x31, 0x800c0597           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f8', 'x20'}, 'clob': {'x23', 'x20'}})
    
    li x23, 0xffff8
    and x20, x20, x23
    li x23, 0x801800bf
    add x20, x20, x23
    fsd f8, -0xbf(x20)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        47d73e6f94b8e338a86f56223f9915a23067246d        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f8, -0xbf(x20)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        47d73e6f94b8e338a86f56223f9915a23067246d        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x20
s4(x20)             0x00000000801800c7(2149056711)                  0x00000000801800c7(2149056711)
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
sp(x2)              0x000000007ffffe47(2147483207)                  0x000000007ffffe47(2147483207)                  
gp(x3)              0x00000000801804ea(2149057770)                  0x00000000801804ea(2149057770)                  
tp(x4)              0x000000008017f937(2149054775)                  0x000000008017f937(2149054775)                  
t0(x5)              0x0000000080180764(2149058404)                  0x0000000080180764(2149058404)                  
t1(x6)              0x00000000000000a6(166)                         0x00000000000000a6(166)                         
t2(x7)              0x00000000cc1a0778(3424257912)                  0x00000000cc1a0778(3424257912)                  
fp(x8)              0x00000000801806ea(2149058282)                  0x00000000801806ea(2149058282)                  
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x00000000000000a3(163)                         0x00000000000000a3(163)                         
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x000000008017ff9f(2149056415)                  0x000000008017ff9f(2149056415)                  
a4(x14)             0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
a5(x15)             0x000000000271b423(41006115)                    0x000000000271b423(41006115)                    
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x000000008017feb7(2149056183)                  0x000000008017feb7(2149056183)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x0000000080180622(2149058082)                  0x0000000080180622(2149058082)                  
s4(x20)             0x00000000801800c7(2149056711)                  0x00000000801800c7(2149056711)                  
s5(x21)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s6(x22)             0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
s7(x23)             0x00000000801800bf(2149056703)                  0x00000000801800bf(2149056703)                  
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s10(x26)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s11(x27)            0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
t3(x28)             0x0000000080180643(2149058115)                  0x0000000080180643(2149058115)                  
t4(x29)             0x000000007ffff9b6(2147482038)                  0x000000007ffff9b6(2147482038)                  
t5(x30)             0x000000007ffffa4f(2147482191)                  0x000000007ffffa4f(2147482191)                  
t6(x31)             0x00000000800c0597(2148271511)                  0x00000000800c0597(2148271511)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            d6095b54b2ab8bf785ed7e5441a155b4facbdf77        d6095b54b2ab8bf785ed7e5441a155b4facbdf77        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        47d73e6f94b8e338a86f56223f9915a23067246d        X
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000030(48)                          0x0000000000000030(48)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff2864dd37(1.2704510803562743e-14_s)    0xffffffff2864dd37(1.2704510803562743e-14_s)    
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff4f000007(2147485440.0_s)              0xffffffff4f000007(2147485440.0_s)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0xc6219bf4967cddd7(-6.97572313911571e+29_d)     0xc6219bf4967cddd7(-6.97572313911571e+29_d)     
f10                 0xffffffff4f000007(2147485440.0_s)              0xffffffff4f000007(2147485440.0_s)              
f11                 0x4048000000000000(48.0_d)                      0x4048000000000000(48.0_d)                      
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f15                 0x2813836133322c49(1.238084287307389e-115_d)    0x2813836133322c49(1.238084287307389e-115_d)    
f16                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f17                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f25                 0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f28                 0x7fffffff4f000001(nan_d)                       0x7fffffff4f000001(nan_d)                       
f29                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f30                 0xffffffff8017fe39(-2.2034143169905213e-39_s)   0xffffffff8017fe39(-2.2034143169905213e-39_s)   
f31                 0xffffffff8017fe39(-2.2034143169905213e-39_s)   0xffffffff8017fe39(-2.2034143169905213e-39_s)   
STATES DIFFER: True
```

# FailID_001996 VP++ FF neg RV64 fsh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1996
* Isolated failing instruction: `fsh`
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
_reg_f0: .byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x6f,0x00,0x40,0xa1,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x00,0x00,0xed,0xcc,0x6b,0xea,0x41
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xa5,0xf9,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0xd3,0x4b,0xb7,0x8a,0x9b,0x66,0x37,0x51
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x8d,0x30,0xe2,0x54,0xa5,0x5d,0x2f,0x48
_reg_f20:.byte 0xac,0xd7,0xef,0x99,0xc8,0x1c,0x81,0x62
_reg_f21:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0xd4,0x26,0x42,0xed,0x0d,0x68,0x56,0xf7
_reg_f24:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x1d,0xb7,0x27,0x2d,0xb2,0x99,0x1d,0xbe
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': True, 'dz': True, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x2e
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x800000e4            // ra
    li x2, 0xb0c9470c            // sp
    li x3, 0x7ffffb37            // gp
    li x4, 0x0                   // tp
    li x5, 0xffffffff8bba4000    // t0
    li x6, 0x0                   // t1
    li x7, 0x800002a8            // t2
    li x8, 0xffffffffcf81a000    // fp
    li x9, 0xffffffffffffffff    // s1
    li x10, 0x80000268           // a0
    li x11, 0x1c34aae88          // a1
    li x12, 0x6000               // a2
    li x13, 0x8017f967           // a3
    li x14, 0xffffffff7fe800b9   // a4
    li x15, 0x0                  // a5
    li x16, 0x8027f1bb           // a6
    li x17, 0x8017fa48           // a7
    li x18, 0xffffffffffffa000   // s2
    li x19, 0x80200171           // s3
    li x20, 0x6000               // s4
    li x21, 0x0                  // s5
    li x22, 0x6737               // s6
    li x23, 0x0                  // s7
    li x24, 0xffffffffffffffff   // s8
    li x25, 0x6000               // s9
    li x26, 0x800003fa           // s10
    li x27, 0x801806f9           // s11
    li x28, 0xe5                 // t3
    li x29, 0x6000               // t4
    li x30, 0xe2                 // t5
    li x31, 0x2e                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f28', 'x19'}, 'clob': {'x19', 'x24'}})
    
    li x24, 0xffffe
    and x19, x19, x24
    li x24, 0x80180748
    add x19, x19, x24
    fsh f28, -0x748(x19)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsh f28, -0x748(x19)
+========================================================================================================================+
Attributes:  fcsr ['underflow', 'overflow', 'div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f28, x748, x19
s3(x19)             0x00000000801808b8(2149058744)                  0x00000000801808b8(2149058744)
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000800000e4(2147483876)                  0x00000000800000e4(2147483876)                  
sp(x2)              0x00000000b0c9470c(2965980940)                  0x00000000b0c9470c(2965980940)                  
gp(x3)              0x000000007ffffb37(2147482423)                  0x000000007ffffb37(2147482423)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0xffffffff8bba4000(18446744071758823424)        0xffffffff8bba4000(18446744071758823424)        
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x00000000800002a8(2147484328)                  0x00000000800002a8(2147484328)                  
fp(x8)              0xffffffffcf81a000(18446744072895963136)        0xffffffffcf81a000(18446744072895963136)        
s1(x9)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a0(x10)             0x0000000080000268(2147484264)                  0x0000000080000268(2147484264)                  
a1(x11)             0x00000001c34aae88(7571418760)                  0x00000001c34aae88(7571418760)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x000000008017f967(2149054823)                  0x000000008017f967(2149054823)                  
a4(x14)             0xffffffff7fe800b9(18446744071560495289)        0xffffffff7fe800b9(18446744071560495289)        
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x000000008027f1bb(2150101435)                  0x000000008027f1bb(2150101435)                  
a7(x17)             0x000000008017fa48(2149055048)                  0x000000008017fa48(2149055048)                  
s2(x18)             0xffffffffffffa000(18446744073709527040)        0xffffffffffffa000(18446744073709527040)        
s3(x19)             0x00000000801808b8(2149058744)                  0x00000000801808b8(2149058744)                  
s4(x20)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000000006737(26423)                       0x0000000000006737(26423)                       
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x0000000080180748(2149058376)                  0x0000000080180748(2149058376)                  
s9(x25)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s10(x26)            0x00000000800003fa(2147484666)                  0x00000000800003fa(2147484666)                  
s11(x27)            0x00000000801806f9(2149058297)                  0x00000000801806f9(2149058297)                  
t3(x28)             0x00000000000000e5(229)                         0x00000000000000e5(229)                         
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x00000000000000e2(226)                         0x00000000000000e2(226)                         
t6(x31)             0x000000000000002e(46)                          0x000000000000002e(46)                          

STATE               REF                                             DUT                                             DIFF
xmemhash            27ed59c1f5ec8676d9a17a3425dead411dad8711        27ed59c1f5ec8676d9a17a3425dead411dad8711        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000071c(2147485468)                  0x000000008000071c(2147485468)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000002e(46)                          0x000000000000002e(46)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f1                  0xffffffffa140006f(-6.505270420568022e-19_s)    0xffffffffa140006f(-6.505270420568022e-19_s)    
f2                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f3                  0x41ea6bcced000000(3546179432.0_d)              0x41ea6bcced000000(3546179432.0_d)              
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f7                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff8017f9a5(-2.2017719951903326e-39_s)   0xffffffff8017f9a5(-2.2017719951903326e-39_s)   
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x5137669b8ab74bd3(1.7757823183693137e+83_d)    0x5137669b8ab74bd3(1.7757823183693137e+83_d)    
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x482f5da554e2308d(5.3366150143908725e+39_d)    0x482f5da554e2308d(5.3366150143908725e+39_d)    
f20                 0x62811cc899efd7ac(3.153402842233095e+166_d)    0x62811cc899efd7ac(3.153402842233095e+166_d)    
f21                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xf756680ded4226d4(-7.224860598141725e+266_d)   0xf756680ded4226d4(-7.224860598141725e+266_d)   
f24                 0x7fffffffffc00000(nan_d)                       0x7fffffffffc00000(nan_d)                       
f25                 0xbe1d99b22d27b71d(-1.7229685912554313e-09_d)   0xbe1d99b22d27b71d(-1.7229685912554313e-09_d)   
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

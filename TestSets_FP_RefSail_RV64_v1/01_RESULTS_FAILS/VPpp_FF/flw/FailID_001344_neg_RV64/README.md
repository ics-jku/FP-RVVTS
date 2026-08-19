# FailID_001344 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1344
* Isolated failing instruction: `flw`
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
    li x1, 0x801806e3            // ra
    li x2, 0x8017fd04            // sp
    li x3, 0x8017fd71            // gp
    li x4, 0x8017fd2e            // tp
    li x5, 0x80005fd1            // t0
    li x6, 0x8017fd34            // t1
    li x7, 0x1                   // t2
    li x8, 0x8018047c            // fp
    li x9, 0x6434a000            // s1
    li x10, 0x8017f84d           // a0
    li x11, 0x6000               // a1
    li x12, 0x801804fd           // a2
    li x13, 0x0                  // a3
    li x14, 0x42dab000           // a4
    li x15, 0xffffffffaf1e7000   // a5
    li x16, 0x80180215           // a6
    li x17, 0x43                 // a7
    li x18, 0x1                  // s2
    li x19, 0x800001c4           // s3
    li x20, 0x0                  // s4
    li x21, 0x8017f84d000        // s5
    li x22, 0x80000071           // s6
    li x23, 0x1                  // s7
    li x24, 0x7ffffa8a           // s8
    li x25, 0x8017f807           // s9
    li x26, 0x8017fd2e           // s10
    li x27, 0x80200517           // s11
    li x28, 0xb5                 // t3
    li x29, 0x800007d6000000     // t4
    li x30, 0xffffffff806d4000   // t5
    li x31, 0xad6b4768           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x6'}, 'clob': {'f13', 'x19', 'x6'}})
    
    li x19, 0x1ffffc
    and x6, x6, x19
    li x19, 0x800005ea
    add x6, x6, x19
    flw f13, -0x5ea(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f13, -0x5ea(x6)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x5, x6
t0(x5)              0x0000000080005fd1(2147508177)                  0x0000000080005fd1(2147508177)
t1(x6)              0x000000008018031e(2149057310)                  0x000000008018031e(2149057310)
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801806e3(2149058275)                  0x00000000801806e3(2149058275)                  
sp(x2)              0x000000008017fd04(2149055748)                  0x000000008017fd04(2149055748)                  
gp(x3)              0x000000008017fd71(2149055857)                  0x000000008017fd71(2149055857)                  
tp(x4)              0x000000008017fd2e(2149055790)                  0x000000008017fd2e(2149055790)                  
t0(x5)              0x0000000080005fd1(2147508177)                  0x0000000080005fd1(2147508177)                  
t1(x6)              0x000000008018031e(2149057310)                  0x000000008018031e(2149057310)                  
t2(x7)              0x0000000000000001(1)                           0x0000000000000001(1)                           
fp(x8)              0x000000008018047c(2149057660)                  0x000000008018047c(2149057660)                  
s1(x9)              0x000000006434a000(1681170432)                  0x000000006434a000(1681170432)                  
a0(x10)             0x000000008017f84d(2149054541)                  0x000000008017f84d(2149054541)                  
a1(x11)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a2(x12)             0x00000000801804fd(2149057789)                  0x00000000801804fd(2149057789)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x0000000042dab000(1121628160)                  0x0000000042dab000(1121628160)                  
a5(x15)             0xffffffffaf1e7000(18446744072352591872)        0xffffffffaf1e7000(18446744072352591872)        
a6(x16)             0x0000000080180215(2149057045)                  0x0000000080180215(2149057045)                  
a7(x17)             0x0000000000000043(67)                          0x0000000000000043(67)                          
s2(x18)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s3(x19)             0x00000000800005ea(2147485162)                  0x00000000800005ea(2147485162)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x000008017f84d000(8802527399936)               0x000008017f84d000(8802527399936)               
s6(x22)             0x0000000080000071(2147483761)                  0x0000000080000071(2147483761)                  
s7(x23)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s8(x24)             0x000000007ffffa8a(2147482250)                  0x000000007ffffa8a(2147482250)                  
s9(x25)             0x000000008017f807(2149054471)                  0x000000008017f807(2149054471)                  
s10(x26)            0x000000008017fd2e(2149055790)                  0x000000008017fd2e(2149055790)                  
s11(x27)            0x0000000080200517(2149582103)                  0x0000000080200517(2149582103)                  
t3(x28)             0x00000000000000b5(181)                         0x00000000000000b5(181)                         
t4(x29)             0x00800007d6000000(36028830674059264)           0x00800007d6000000(36028830674059264)           
t5(x30)             0xffffffff806d4000(18446744071569227776)        0xffffffff806d4000(18446744071569227776)        
t6(x31)             0x00000000ad6b4768(2909489000)                  0x00000000ad6b4768(2909489000)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            ba84b8e8637f70e7431c9af237d91f1d385c624b        ba84b8e8637f70e7431c9af237d91f1d385c624b        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000764(2147485540)                  0x0000000080000764(2147485540)                  
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
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f16                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f17                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
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

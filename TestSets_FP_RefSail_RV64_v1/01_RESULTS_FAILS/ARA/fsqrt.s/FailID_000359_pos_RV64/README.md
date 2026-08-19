# FailID_000359 ARA pos RV64 fsqrt.s

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 359
* Isolated failing instruction: `fsqrt.s`
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
_reg_f1: .byte 0x00,0x80,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x30,0xd6,0xd6,0x41
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x40,0x58,0xff,0xff,0xdf,0x41
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x80,0xb1,0xb6,0xce,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x40,0x58,0xff,0xff,0xdf,0x41
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x5d
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017f8e9            // ra
    li x2, 0x0                   // sp
    li x3, 0x0                   // gp
    li x4, 0x80000203            // tp
    li x5, 0x8017fc9a            // t0
    li x6, 0x800006d6            // t1
    li x7, 0x7ffff8a5            // t2
    li x8, 0x8027fc96            // fp
    li x9, 0x80080eb9            // s1
    li x10, 0x7ffffa17           // a0
    li x11, 0x800002ed           // a1
    li x12, 0x7ffff8a5           // a2
    li x13, 0x0                  // a3
    li x14, 0x0                  // a4
    li x15, 0x800004a7           // a5
    li x16, 0x800000df           // a6
    li x17, 0xffffffffffffffff   // a7
    li x18, 0x200                // s2
    li x19, 0x200                // s3
    li x20, 0x6000               // s4
    li x21, 0xfffffffffffffff3   // s5
    li x22, 0x801ffd42           // s6
    li x23, 0x0                  // s7
    li x24, 0x8000038b           // s8
    li x25, 0x200                // s9
    li x26, 0x801807e4           // s10
    li x27, 0x7fc00000           // s11
    li x28, 0xffffffff7fc00000   // t3
    li x29, 0x7fffffff           // t4
    li x30, 0xffffffffffffffff   // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'f3', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'f19'}})
    fsqrt.s f19, f3
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f19                 0xffffffff1e6bd568(1.2484927790946947e-20_s)    0xffffffff1e6bd569(1.2484928598740514e-20_s)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.s f19, f3
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f19                 0xffffffff1e6bd568(1.2484927790946947e-20_s)    0xffffffff1e6bd569(1.2484928598740514e-20_s)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f19, f3
f3                  0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)
f19                 0xffffffff1e6bd568(1.2484927790946947e-20_s)    0xffffffff1e6bd569(1.2484928598740514e-20_s)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017f8e9(2149054697)                  0x000000008017f8e9(2149054697)                  
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x0000000080000203(2147484163)                  0x0000000080000203(2147484163)                  
t0(x5)              0x000000008017fc9a(2149055642)                  0x000000008017fc9a(2149055642)                  
t1(x6)              0x00000000800006d6(2147485398)                  0x00000000800006d6(2147485398)                  
t2(x7)              0x000000007ffff8a5(2147481765)                  0x000000007ffff8a5(2147481765)                  
fp(x8)              0x000000008027fc96(2150104214)                  0x000000008027fc96(2150104214)                  
s1(x9)              0x0000000080080eb9(2148011705)                  0x0000000080080eb9(2148011705)                  
a0(x10)             0x000000007ffffa17(2147482135)                  0x000000007ffffa17(2147482135)                  
a1(x11)             0x00000000800002ed(2147484397)                  0x00000000800002ed(2147484397)                  
a2(x12)             0x000000007ffff8a5(2147481765)                  0x000000007ffff8a5(2147481765)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x00000000800004a7(2147484839)                  0x00000000800004a7(2147484839)                  
a6(x16)             0x00000000800000df(2147483871)                  0x00000000800000df(2147483871)                  
a7(x17)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s2(x18)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s3(x19)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s4(x20)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s5(x21)             0xfffffffffffffff3(18446744073709551603)        0xfffffffffffffff3(18446744073709551603)        
s6(x22)             0x00000000801ffd42(2149580098)                  0x00000000801ffd42(2149580098)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x000000008000038b(2147484555)                  0x000000008000038b(2147484555)                  
s9(x25)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s10(x26)            0x00000000801807e4(2149058532)                  0x00000000801807e4(2149058532)                  
s11(x27)            0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
t3(x28)             0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
t4(x29)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
t5(x30)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            12524a30b0afba4d9f288acb21e62c24a94eeed7        12524a30b0afba4d9f288acb21e62c24a94eeed7        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000700(2147485440)                  0x0000000080000700(2147485440)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000005d(93)                          0x000000000000005d(93)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff4eff8000(2143289344.0_s)              0xffffffff4eff8000(2143289344.0_s)              
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x41d6d63000000000(1532542976.0_d)              0x41d6d63000000000(1532542976.0_d)              
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x41dfffff58400000(2147482977.0_d)              0x41dfffff58400000(2147482977.0_d)              
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffffceb6b180(-1532542976.0_s)             0xffffffffceb6b180(-1532542976.0_s)             
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xffffffff1e6bd568(1.2484927790946947e-20_s)    0xffffffff1e6bd569(1.2484928598740514e-20_s)    X
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f30                 0x41dfffff58400000(2147482977.0_d)              0x41dfffff58400000(2147482977.0_d)              
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

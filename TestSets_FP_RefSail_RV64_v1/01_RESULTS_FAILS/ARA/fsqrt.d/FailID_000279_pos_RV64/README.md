# FailID_000279 ARA pos RV64 fsqrt.d

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 279
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0xca,0xfe,0xff,0xdf,0x41
_reg_f8: .byte 0x39,0x6b,0xa4,0x4d,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x80,0xa6,0xff,0xff,0xdf,0x41
_reg_f10:.byte 0x39,0x6b,0xa4,0x4d,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0xb0,0xbb,0x7f,0x00,0x00,0x00,0x00
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x73,0x90,0x01,0x34,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x80,0x5f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0xf4,0xcf,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x80,0x34,0xff,0xff,0xdf,0x41
_reg_f31:.byte 0x00,0x00,0x00,0x80,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x41
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x200                 // ra
    li x2, 0x0                   // sp
    li x3, 0x7ffffb2b            // gp
    li x4, 0x801ff71b            // tp
    li x5, 0x148d6728            // t0
    li x6, 0x7ffffca8            // t1
    li x7, 0x7ffff99b            // t2
    li x8, 0x802003ff            // fp
    li x9, 0x0                   // s1
    li x10, 0x7fffffff           // a0
    li x11, 0x2c                 // a1
    li x12, 0x99                 // a2
    li x13, 0x34019073           // a3
    li x14, 0x7ff8000000000000   // a4
    li x15, 0x6000               // a5
    li x16, 0x6000               // a6
    li x17, 0x800009fe           // a7
    li x18, 0x8018062c           // s2
    li x19, 0x4                  // s3
    li x20, 0x8000072f           // s4
    li x21, 0x6000               // s5
    li x22, 0xffffffffffffffff   // s6
    li x23, 0x7fffffffffffffff   // s7
    li x24, 0x7ffff99b           // s8
    li x25, 0x0                  // s9
    li x26, 0x7ffffca0           // s10
    li x27, 0x7fffffff           // s11
    li x28, 0x7ffffe9a           // t3
    li x29, 0x0                  // t4
    li x30, 0x800005b9           // t5
    li x31, 0x41                 // t6
    // INSTRUCTION ({'dep': {'f14', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'f19'}})
    fsqrt.d f19, f14, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f19                 0x1f569a93dbc6e084(1.0289732742685454e-157_d)   0x1f569a93dbc6e085(1.0289732742685456e-157_d)   X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.d f19, f14, dyn
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f19                 0x1f569a93dbc6e084(1.0289732742685454e-157_d)   0x1f569a93dbc6e085(1.0289732742685456e-157_d)   X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f19, f14
f14                 0x000000007fbbb000(1.058785999e-314_d)          0x000000007fbbb000(1.058785999e-314_d)
f19                 0x1f569a93dbc6e084(1.0289732742685454e-157_d)   0x1f569a93dbc6e085(1.0289732742685456e-157_d)   X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000200(512)                         0x0000000000000200(512)                         
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x000000007ffffb2b(2147482411)                  0x000000007ffffb2b(2147482411)                  
tp(x4)              0x00000000801ff71b(2149578523)                  0x00000000801ff71b(2149578523)                  
t0(x5)              0x00000000148d6728(344811304)                   0x00000000148d6728(344811304)                   
t1(x6)              0x000000007ffffca8(2147482792)                  0x000000007ffffca8(2147482792)                  
t2(x7)              0x000000007ffff99b(2147482011)                  0x000000007ffff99b(2147482011)                  
fp(x8)              0x00000000802003ff(2149581823)                  0x00000000802003ff(2149581823)                  
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a1(x11)             0x000000000000002c(44)                          0x000000000000002c(44)                          
a2(x12)             0x0000000000000099(153)                         0x0000000000000099(153)                         
a3(x13)             0x0000000034019073(872517747)                   0x0000000034019073(872517747)                   
a4(x14)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x00000000800009fe(2147486206)                  0x00000000800009fe(2147486206)                  
s2(x18)             0x000000008018062c(2149058092)                  0x000000008018062c(2149058092)                  
s3(x19)             0x0000000000000004(4)                           0x0000000000000004(4)                           
s4(x20)             0x000000008000072f(2147485487)                  0x000000008000072f(2147485487)                  
s5(x21)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s6(x22)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s7(x23)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s8(x24)             0x000000007ffff99b(2147482011)                  0x000000007ffff99b(2147482011)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x000000007ffffca0(2147482784)                  0x000000007ffffca0(2147482784)                  
s11(x27)            0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
t3(x28)             0x000000007ffffe9a(2147483290)                  0x000000007ffffe9a(2147483290)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x00000000800005b9(2147485113)                  0x00000000800005b9(2147485113)                  
t6(x31)             0x0000000000000041(65)                          0x0000000000000041(65)                          

STATE               REF                                             DUT                                             DIFF
xmemhash            d1e779421902d34ea4d150612b3fbe5f05af1628        d1e779421902d34ea4d150612b3fbe5f05af1628        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800006ec(2147485420)                  0x00000000800006ec(2147485420)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000041(65)                          0x0000000000000041(65)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f7                  0x41dffffecac00000(2147482411.0_d)              0x41dffffecac00000(2147482411.0_d)              
f8                  0xffffffff4da46b39(344811296.0_s)               0xffffffff4da46b39(344811296.0_s)               
f9                  0x41dfffffa6800000(2147483290.0_d)              0x41dfffffa6800000(2147483290.0_d)              
f10                 0xffffffff4da46b39(344811296.0_s)               0xffffffff4da46b39(344811296.0_s)               
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x000000007fbbb000(1.058785999e-314_d)          0x000000007fbbb000(1.058785999e-314_d)          
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f18                 0xffffffff34019073(1.2066611532191018e-07_s)    0xffffffff34019073(1.2066611532191018e-07_s)    
f19                 0x1f569a93dbc6e084(1.0289732742685454e-157_d)   0x1f569a93dbc6e085(1.0289732742685456e-157_d)   X
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff5f800000(1.8446744073709552e+19_s)    0xffffffff5f800000(1.8446744073709552e+19_s)    
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xffffffffceffcff4(-2145909248.0_s)             0xffffffffceffcff4(-2145909248.0_s)             
f27                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f28                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x41dfffff34800000(2147482834.0_d)              0x41dfffff34800000(2147482834.0_d)              
f31                 0xffffffff80000000(-0.0_s)                      0xffffffff80000000(-0.0_s)                      
STATES DIFFER: True
```

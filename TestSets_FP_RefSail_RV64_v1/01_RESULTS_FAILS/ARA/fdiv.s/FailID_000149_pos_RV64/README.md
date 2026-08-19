# FailID_000149 ARA pos RV64 fdiv.s

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 149
* Isolated failing instruction: `fdiv.s`
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
_reg_f0: .byte 0xf0,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f2: .byte 0xb7,0x62,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x40,0x00,0xcf,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0xfd,0xfe,0x27,0x80,0x00,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f29:.byte 0xf0,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': True, 'uf': True, 'of': True, 'dz': False, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x67
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x6000                // ra
    li x2, 0x0                   // sp
    li x3, 0xffffffff7fc00000    // gp
    li x4, 0xffffffff7fe003f4    // tp
    li x5, 0x80186846            // t0
    li x6, 0x62                  // t1
    li x7, 0x0                   // t2
    li x8, 0x80163142            // fp
    li x9, 0x8027fdc4            // s1
    li x10, 0x8028038d           // a0
    li x11, 0xffffffffffffffff   // a1
    li x12, 0x80000217           // a2
    li x13, 0x67                 // a3
    li x14, 0x3213a744           // a4
    li x15, 0x8027fb31           // a5
    li x16, 0x0                  // a6
    li x17, 0x7ffffc8b           // a7
    li x18, 0x29a                // s2
    li x19, 0x0                  // s3
    li x20, 0x8000000000000362   // s4
    li x21, 0x0                  // s5
    li x22, 0x200                // s6
    li x23, 0xc0689740           // s7
    li x24, 0x8018063e           // s8
    li x25, 0x0                  // s9
    li x26, 0x0                  // s10
    li x27, 0x0                  // s11
    li x28, 0x7ff8000000000000   // t3
    li x29, 0x7fffffffffffffff   // t4
    li x30, 0xffffffffffffffff   // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'f23', 'fcsr.rm', 'f17', 'mstatus.fs/vs.fs'}, 'clob': {'f22'}})
    fdiv.s f22, f23, f17, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f22                 0xffffffff91bfa09e(-3.0233474563759294e-28_s)   0xffffffff91bfa09f(-3.0233476971171724e-28_s)   X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fdiv.s f22, f23, f17, dyn
+========================================================================================================================+
Attributes:  fcsr ['underflow', 'overflow', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f22                 0xffffffff91bfa09e(-3.0233474563759294e-28_s)   0xffffffff91bfa09f(-3.0233476971171724e-28_s)   X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f22, f23, f17
f17                 0xffffffffcf004000(-2151677952.0_s)             0xffffffffcf004000(-2151677952.0_s)
f22                 0xffffffff91bfa09e(-3.0233474563759294e-28_s)   0xffffffff91bfa09f(-3.0233476971171724e-28_s)   X
f23                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
tp(x4)              0xffffffff7fe003f4(18446744071559971828)        0xffffffff7fe003f4(18446744071559971828)        
t0(x5)              0x0000000080186846(2149083206)                  0x0000000080186846(2149083206)                  
t1(x6)              0x0000000000000062(98)                          0x0000000000000062(98)                          
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x0000000080163142(2148938050)                  0x0000000080163142(2148938050)                  
s1(x9)              0x000000008027fdc4(2150104516)                  0x000000008027fdc4(2150104516)                  
a0(x10)             0x000000008028038d(2150105997)                  0x000000008028038d(2150105997)                  
a1(x11)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a2(x12)             0x0000000080000217(2147484183)                  0x0000000080000217(2147484183)                  
a3(x13)             0x0000000000000067(103)                         0x0000000000000067(103)                         
a4(x14)             0x000000003213a744(840148804)                   0x000000003213a744(840148804)                   
a5(x15)             0x000000008027fb31(2150103857)                  0x000000008027fb31(2150103857)                  
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x000000007ffffc8b(2147482763)                  0x000000007ffffc8b(2147482763)                  
s2(x18)             0x000000000000029a(666)                         0x000000000000029a(666)                         
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x8000000000000362(9223372036854776674)         0x8000000000000362(9223372036854776674)         
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s7(x23)             0x00000000c0689740(3228079936)                  0x00000000c0689740(3228079936)                  
s8(x24)             0x000000008018063e(2149058110)                  0x000000008018063e(2149058110)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
t4(x29)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
t5(x30)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            ae8af93293c7fdae04afe07ec0c5efa36933c6e0        ae8af93293c7fdae04afe07ec0c5efa36933c6e0        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000700(2147485440)                  0x0000000080000700(2147485440)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000067(103)                         0x0000000000000067(103)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            True                                            True                                            
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff4efffff0(2147481600.0_s)              0xffffffff4efffff0(2147481600.0_s)              
f1                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f2                  0xffffffff000062b7(3.541221349195245e-41_s)     0xffffffff000062b7(3.541221349195245e-41_s)     
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f6                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffffcf004000(-2151677952.0_s)             0xffffffffcf004000(-2151677952.0_s)             
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x000000008027fefd(1.062292931e-314_d)          0x000000008027fefd(1.062292931e-314_d)          
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff91bfa09e(-3.0233474563759294e-28_s)   0xffffffff91bfa09f(-3.0233476971171724e-28_s)   X
f23                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0xffffffff4efffff0(2147481600.0_s)              0xffffffff4efffff0(2147481600.0_s)              
f30                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f31                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
STATES DIFFER: True
```

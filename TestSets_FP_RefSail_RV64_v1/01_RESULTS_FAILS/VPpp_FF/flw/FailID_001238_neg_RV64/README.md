# FailID_001238 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1238
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
_reg_f2: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x20,0xff,0xff,0xdf,0x41
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x40,0x40
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x44,0xff,0xff,0xff,0xff
_reg_f26:.byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x05,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x62
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x1                   // ra
    li x2, 0x7ffffac6            // sp
    li x3, 0x0                   // gp
    li x4, 0x802805f7            // tp
    li x5, 0xae3bb70c            // t0
    li x6, 0xfffffffff6afa000    // t1
    li x7, 0x801805fb            // t2
    li x8, 0x8000011e            // fp
    li x9, 0x0                   // s1
    li x10, 0x1                  // a0
    li x11, 0x6000               // a1
    li x12, 0x8017f836           // a2
    li x13, 0x801efc12           // a3
    li x14, 0x0                  // a4
    li x15, 0xb                  // a5
    li x16, 0x100000             // a6
    li x17, 0x80180556           // a7
    li x18, 0x400                // s2
    li x19, 0x8017f8ae           // s3
    li x20, 0x7ffffabe           // s4
    li x21, 0x200                // s5
    li x22, 0x80000474           // s6
    li x23, 0x801ff59a           // s7
    li x24, 0x693f0              // s8
    li x25, 0x7ffffb28           // s9
    li x26, 0x8017f836           // s10
    li x27, 0x80200084           // s11
    li x28, 0xcbf8072c           // t3
    li x29, 0x8017f7f9           // t4
    li x30, 0xfffffffffffffbfb   // t5
    li x31, 0x6000               // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x9'}, 'clob': {'x9', 'x26', 'f8'}})
    
    li x26, 0x1ffffc
    and x9, x9, x26
    li x26, 0x80000180
    add x9, x9, x26
    flw f8, -0x180(x9)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f8                  0xffffffff46c00000(24576.0_s)                   0xffffffff2140006f(6.505270420568022e-19_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f8, -0x180(x9)
+========================================================================================================================+
Attributes:  fcsr ['underflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f8                  0xffffffff46c00000(24576.0_s)                   0xffffffff2140006f(6.505270420568022e-19_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x180, x9
s1(x9)              0x0000000080000180(2147484032)                  0x0000000080000180(2147484032)
f8                  0xffffffff46c00000(24576.0_s)                   0xffffffff2140006f(6.505270420568022e-19_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000001(1)                           0x0000000000000001(1)                           
sp(x2)              0x000000007ffffac6(2147482310)                  0x000000007ffffac6(2147482310)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x00000000802805f7(2150106615)                  0x00000000802805f7(2150106615)                  
t0(x5)              0x00000000ae3bb70c(2923149068)                  0x00000000ae3bb70c(2923149068)                  
t1(x6)              0xfffffffff6afa000(18446744073553289216)        0xfffffffff6afa000(18446744073553289216)        
t2(x7)              0x00000000801805fb(2149058043)                  0x00000000801805fb(2149058043)                  
fp(x8)              0x000000008000011e(2147483934)                  0x000000008000011e(2147483934)                  
s1(x9)              0x0000000080000180(2147484032)                  0x0000000080000180(2147484032)                  
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a2(x12)             0x000000008017f836(2149054518)                  0x000000008017f836(2149054518)                  
a3(x13)             0x00000000801efc12(2149514258)                  0x00000000801efc12(2149514258)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x000000000000000b(11)                          0x000000000000000b(11)                          
a6(x16)             0x0000000000100000(1048576)                     0x0000000000100000(1048576)                     
a7(x17)             0x0000000080180556(2149057878)                  0x0000000080180556(2149057878)                  
s2(x18)             0x0000000000000400(1024)                        0x0000000000000400(1024)                        
s3(x19)             0x000000008017f8ae(2149054638)                  0x000000008017f8ae(2149054638)                  
s4(x20)             0x000000007ffffabe(2147482302)                  0x000000007ffffabe(2147482302)                  
s5(x21)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s6(x22)             0x0000000080000474(2147484788)                  0x0000000080000474(2147484788)                  
s7(x23)             0x00000000801ff59a(2149578138)                  0x00000000801ff59a(2149578138)                  
s8(x24)             0x00000000000693f0(431088)                      0x00000000000693f0(431088)                      
s9(x25)             0x000000007ffffb28(2147482408)                  0x000000007ffffb28(2147482408)                  
s10(x26)            0x0000000080000180(2147484032)                  0x0000000080000180(2147484032)                  
s11(x27)            0x0000000080200084(2149580932)                  0x0000000080200084(2149580932)                  
t3(x28)             0x00000000cbf8072c(3422029612)                  0x00000000cbf8072c(3422029612)                  
t4(x29)             0x000000008017f7f9(2149054457)                  0x000000008017f7f9(2149054457)                  
t5(x30)             0xfffffffffffffbfb(18446744073709550587)        0xfffffffffffffbfb(18446744073709550587)        
t6(x31)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       

STATE               REF                                             DUT                                             DIFF
xmemhash            9be3c37ea5d240097ce7e48808cf70146881ec80        9be3c37ea5d240097ce7e48808cf70146881ec80        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000062(98)                          0x0000000000000062(98)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f3                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff46c00000(24576.0_s)                   0xffffffff2140006f(6.505270420568022e-19_s)     X
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x41dfffff20000000(2147482752.0_d)              0x41dfffff20000000(2147482752.0_d)              
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x4040000000000000(32.0_d)                      0x4040000000000000(32.0_d)                      
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)                     
f26                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff4f001805(2149057792.0_s)              0xffffffff4f001805(2149057792.0_s)              
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

# FailID_001576 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1576
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xe0,0x31,0x00,0x00,0xe0,0x41
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x93,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0xfa,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x5a,0xfe,0x27,0x80,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x4
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xfffffffffff00000    // ra
    li x2, 0x6f26ff              // sp
    li x3, 0x20000104c00         // gp
    li x4, 0x20000104c00         // tp
    li x5, 0x800004ba            // t0
    li x6, 0x801ffd40            // t1
    li x7, 0x4                   // t2
    li x8, 0x5e5a014             // fp
    li x9, 0xffffffffffffffff    // s1
    li x10, 0x8017fdee           // a0
    li x11, 0x6000               // a1
    li x12, 0x6000               // a2
    li x13, 0xe1c9f73c           // a3
    li x14, 0x8017f75c           // a4
    li x15, 0xe7                 // a5
    li x16, 0xde4dfff4           // a6
    li x17, 0x801a0602           // a7
    li x18, 0x80000671           // s2
    li x19, 0xffffffffffffffff   // s3
    li x20, 0x7ffffbc3           // s4
    li x21, 0x8000038c           // s5
    li x22, 0x7fffffffffffffff   // s6
    li x23, 0xffffffffffffff06   // s7
    li x24, 0x7ffff99c           // s8
    li x25, 0x80241dee           // s9
    li x26, 0x80000671           // s10
    li x27, 0x7ffff99c           // s11
    li x28, 0x0                  // t3
    li x29, 0x30bce72c           // t4
    li x30, 0xfffffffffff        // t5
    li x31, 0x1                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x11'}, 'clob': {'x18', 'x11', 'f9'}})
    
    li x18, 0x1ffffc
    and x11, x11, x18
    li x18, 0x7ffffd54
    add x11, x11, x18
    flw f9, 0x2ac(x11)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f9                  0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f9, 0x2ac(x11)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f9                  0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x2, x11
sp(x2)              0x00000000006f26ff(7284479)                     0x00000000006f26ff(7284479)
a1(x11)             0x0000000080005d54(2147507540)                  0x0000000080005d54(2147507540)
f9                  0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xfffffffffff00000(18446744073708503040)        0xfffffffffff00000(18446744073708503040)        
sp(x2)              0x00000000006f26ff(7284479)                     0x00000000006f26ff(7284479)                     
gp(x3)              0x0000020000104c00(2199024323584)               0x0000020000104c00(2199024323584)               
tp(x4)              0x0000020000104c00(2199024323584)               0x0000020000104c00(2199024323584)               
t0(x5)              0x00000000800004ba(2147484858)                  0x00000000800004ba(2147484858)                  
t1(x6)              0x00000000801ffd40(2149580096)                  0x00000000801ffd40(2149580096)                  
t2(x7)              0x0000000000000004(4)                           0x0000000000000004(4)                           
fp(x8)              0x0000000005e5a014(98934804)                    0x0000000005e5a014(98934804)                    
s1(x9)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a0(x10)             0x000000008017fdee(2149055982)                  0x000000008017fdee(2149055982)                  
a1(x11)             0x0000000080005d54(2147507540)                  0x0000000080005d54(2147507540)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x00000000e1c9f73c(3788109628)                  0x00000000e1c9f73c(3788109628)                  
a4(x14)             0x000000008017f75c(2149054300)                  0x000000008017f75c(2149054300)                  
a5(x15)             0x00000000000000e7(231)                         0x00000000000000e7(231)                         
a6(x16)             0x00000000de4dfff4(3729653748)                  0x00000000de4dfff4(3729653748)                  
a7(x17)             0x00000000801a0602(2149189122)                  0x00000000801a0602(2149189122)                  
s2(x18)             0x000000007ffffd54(2147482964)                  0x000000007ffffd54(2147482964)                  
s3(x19)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s4(x20)             0x000000007ffffbc3(2147482563)                  0x000000007ffffbc3(2147482563)                  
s5(x21)             0x000000008000038c(2147484556)                  0x000000008000038c(2147484556)                  
s6(x22)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s7(x23)             0xffffffffffffff06(18446744073709551366)        0xffffffffffffff06(18446744073709551366)        
s8(x24)             0x000000007ffff99c(2147482012)                  0x000000007ffff99c(2147482012)                  
s9(x25)             0x0000000080241dee(2149850606)                  0x0000000080241dee(2149850606)                  
s10(x26)            0x0000000080000671(2147485297)                  0x0000000080000671(2147485297)                  
s11(x27)            0x000000007ffff99c(2147482012)                  0x000000007ffff99c(2147482012)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x0000000030bce72c(817686316)                   0x0000000030bce72c(817686316)                   
t5(x30)             0x00000fffffffffff(17592186044415)              0x00000fffffffffff(17592186044415)              
t6(x31)             0x0000000000000001(1)                           0x0000000000000001(1)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            6cab9b5303c996a8b9ac323948571ce1502f1683        6cab9b5303c996a8b9ac323948571ce1502f1683        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000004(4)                           0x0000000000000004(4)                           
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x41e0000031e00000(2147484047.0_d)              0x41e0000031e00000(2147484047.0_d)              
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff00000293(9.234556879900544e-43_s)     0xffffffff00000293(9.234556879900544e-43_s)     
f9                  0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
f10                 0xffffffff4efffffa(2147482880.0_s)              0xffffffff4efffffa(2147482880.0_s)              
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f15                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f20                 0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x000000008027fe5a(1.0622928504e-314_d)         0x000000008027fe5a(1.0622928504e-314_d)         
f24                 0x7ffffffffffffe00(nan_d)                       0x7ffffffffffffe00(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ffffffffffffe00(nan_d)                       0x7ffffffffffffe00(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

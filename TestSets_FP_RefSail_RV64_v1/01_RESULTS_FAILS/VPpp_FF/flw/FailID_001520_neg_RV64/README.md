# FailID_001520 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1520
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
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x04,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x80
_reg_f10:.byte 0x04,0x00,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x08,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x3d,0xb1,0xaf,0xdd,0x48,0xf5,0x3e,0xde
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f25:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x18,0x40
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0xd7,0xb3,0xdd,0x1d,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x70
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x70                  // ra
    li x2, 0x7fffffff            // sp
    li x3, 0x80000285            // gp
    li x4, 0xffffffffffffffff    // tp
    li x5, 0x80180639            // t0
    li x6, 0x8000025a            // t1
    li x7, 0x801806e4            // t2
    li x8, 0x800007ec            // fp
    li x9, 0x800067ec            // s1
    li x10, 0x7fffffffffffffff   // a0
    li x11, 0x80180582           // a1
    li x12, 0x80180270           // a2
    li x13, 0x8018039a           // a3
    li x14, 0x8017fe06           // a4
    li x15, 0x80180582           // a5
    li x16, 0x0                  // a6
    li x17, 0x340191f3           // a7
    li x18, 0x0                  // s2
    li x19, 0x801804bc           // s3
    li x20, 0x8017f3fa           // s4
    li x21, 0x800006f9           // s5
    li x22, 0x7ffff982           // s6
    li x23, 0x80000bd1           // s7
    li x24, 0x7ffffffffffffece   // s8
    li x25, 0x80200668           // s9
    li x26, 0x6000               // s10
    li x27, 0x200                // s11
    li x28, 0x6000               // t3
    li x29, 0x340191f3           // t4
    li x30, 0x80200a2c           // t5
    li x31, 0x801804bc           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x3'}, 'clob': {'x4', 'f6', 'x3'}})
    
    li x4, 0x1ffffc
    and x3, x3, x4
    li x4, 0x7ffff875
    add x3, x3, x4
    flw f6, 0x78b(x3)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f6                  0xffffffff4f000004(2147484672.0_s)              0xffffffffd20005d3(-137463382016.0_s)           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f6, 0x78b(x3)
+========================================================================================================================+
Attributes:  fcsr ['invalid']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f6                  0xffffffff4f000004(2147484672.0_s)              0xffffffffd20005d3(-137463382016.0_s)           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f6, x78, x3
gp(x3)              0x000000007ffffaf9(2147482361)                  0x000000007ffffaf9(2147482361)
f6                  0xffffffff4f000004(2147484672.0_s)              0xffffffffd20005d3(-137463382016.0_s)           X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000070(112)                         0x0000000000000070(112)                         
sp(x2)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
gp(x3)              0x000000007ffffaf9(2147482361)                  0x000000007ffffaf9(2147482361)                  
tp(x4)              0x000000007ffff875(2147481717)                  0x000000007ffff875(2147481717)                  
t0(x5)              0x0000000080180639(2149058105)                  0x0000000080180639(2149058105)                  
t1(x6)              0x000000008000025a(2147484250)                  0x000000008000025a(2147484250)                  
t2(x7)              0x00000000801806e4(2149058276)                  0x00000000801806e4(2149058276)                  
fp(x8)              0x00000000800007ec(2147485676)                  0x00000000800007ec(2147485676)                  
s1(x9)              0x00000000800067ec(2147510252)                  0x00000000800067ec(2147510252)                  
a0(x10)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
a1(x11)             0x0000000080180582(2149057922)                  0x0000000080180582(2149057922)                  
a2(x12)             0x0000000080180270(2149057136)                  0x0000000080180270(2149057136)                  
a3(x13)             0x000000008018039a(2149057434)                  0x000000008018039a(2149057434)                  
a4(x14)             0x000000008017fe06(2149056006)                  0x000000008017fe06(2149056006)                  
a5(x15)             0x0000000080180582(2149057922)                  0x0000000080180582(2149057922)                  
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x00000000801804bc(2149057724)                  0x00000000801804bc(2149057724)                  
s4(x20)             0x000000008017f3fa(2149053434)                  0x000000008017f3fa(2149053434)                  
s5(x21)             0x00000000800006f9(2147485433)                  0x00000000800006f9(2147485433)                  
s6(x22)             0x000000007ffff982(2147481986)                  0x000000007ffff982(2147481986)                  
s7(x23)             0x0000000080000bd1(2147486673)                  0x0000000080000bd1(2147486673)                  
s8(x24)             0x7ffffffffffffece(9223372036854775502)         0x7ffffffffffffece(9223372036854775502)         
s9(x25)             0x0000000080200668(2149582440)                  0x0000000080200668(2149582440)                  
s10(x26)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s11(x27)            0x0000000000000200(512)                         0x0000000000000200(512)                         
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
t5(x30)             0x0000000080200a2c(2149583404)                  0x0000000080200a2c(2149583404)                  
t6(x31)             0x00000000801804bc(2149057724)                  0x00000000801804bc(2149057724)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            38849174ad5061ef8f67262eca5461c2a20f7b2a        38849174ad5061ef8f67262eca5461c2a20f7b2a        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000774(2147485556)                  0x0000000080000774(2147485556)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000070(112)                         0x0000000000000070(112)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff4f000004(2147484672.0_s)              0xffffffffd20005d3(-137463382016.0_s)           X
f7                  0xffffffff42140000(37.0_s)                      0xffffffff42140000(37.0_s)                      
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x8000000000000000(-0.0_d)                      0x8000000000000000(-0.0_d)                      
f10                 0x7fffffff4f000004(nan_d)                       0x7fffffff4f000004(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff4f001808(2149058560.0_s)              0xffffffff4f001808(2149058560.0_s)              
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xde3ef548ddafb13d(-9.664353833149178e+145_d)   0xde3ef548ddafb13d(-9.664353833149178e+145_d)   
f24                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f25                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x4018000000000000(6.0_d)                       0x4018000000000000(6.0_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff1dddb3d7(5.8684162959893324e-21_s)    0xffffffff1dddb3d7(5.8684162959893324e-21_s)    
STATES DIFFER: True
```

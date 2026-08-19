# FailID_000767 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 767
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
_reg_f0: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0xd1,0xfe,0xf9,0xdf,0xc1
_reg_f2: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0x20,0x9f,0x02,0x00,0xe0,0x41
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xe0,0x66,0x00,0x00,0xe0,0x41
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x60,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x00,0x20,0x9f,0x02,0x00,0xe0,0x41
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x44
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xda                  // ra
    li x2, 0x8018041b            // sp
    li x3, 0xcc76775c            // gp
    li x4, 0x4f8e1c11            // tp
    li x5, 0x80180150            // t0
    li x6, 0x3f                  // t1
    li x7, 0x4c                  // t2
    li x8, 0x80180792            // fp
    li x9, 0x8017fd98            // s1
    li x10, 0x1                  // a0
    li x11, 0x801ffda0           // a1
    li x12, 0x80180cba           // a2
    li x13, 0x80271f06           // a3
    li x14, 0x800003a0           // a4
    li x15, 0x80181660           // a5
    li x16, 0x3f                 // a6
    li x17, 0x0                  // a7
    li x18, 0x801dff16           // s2
    li x19, 0x0                  // s3
    li x20, 0x44                 // s4
    li x21, 0x802005cb           // s5
    li x22, 0x8017fb34           // s6
    li x23, 0x8026241b           // s7
    li x24, 0x80181225           // s8
    li x25, 0x7ffffaf8           // s9
    li x26, 0x1                  // s10
    li x27, 0x73                 // s11
    li x28, 0x7ffffab3           // t3
    li x29, 0x6000               // t4
    li x30, 0x0                  // t5
    li x31, 0x8000049e           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x6'}, 'clob': {'x4', 'f13', 'x6'}})
    
    li x4, 0x1ffff8
    and x6, x6, x4
    li x4, 0x8000039c
    add x6, x6, x4
    fld f13, -0x39c(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0x7fffffff7fc00000(nan_d)                       0x000002970281b383(1.406903987109e-311_d)       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f13, -0x39c(x6)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0x7fffffff7fc00000(nan_d)                       0x000002970281b383(1.406903987109e-311_d)       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x39, x6
t1(x6)              0x00000000800003d4(2147484628)                  0x00000000800003d4(2147484628)
f13                 0x7fffffff7fc00000(nan_d)                       0x000002970281b383(1.406903987109e-311_d)       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000000000da(218)                         0x00000000000000da(218)                         
sp(x2)              0x000000008018041b(2149057563)                  0x000000008018041b(2149057563)                  
gp(x3)              0x00000000cc76775c(3430315868)                  0x00000000cc76775c(3430315868)                  
tp(x4)              0x000000008000039c(2147484572)                  0x000000008000039c(2147484572)                  
t0(x5)              0x0000000080180150(2149056848)                  0x0000000080180150(2149056848)                  
t1(x6)              0x00000000800003d4(2147484628)                  0x00000000800003d4(2147484628)                  
t2(x7)              0x000000000000004c(76)                          0x000000000000004c(76)                          
fp(x8)              0x0000000080180792(2149058450)                  0x0000000080180792(2149058450)                  
s1(x9)              0x000000008017fd98(2149055896)                  0x000000008017fd98(2149055896)                  
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x00000000801ffda0(2149580192)                  0x00000000801ffda0(2149580192)                  
a2(x12)             0x0000000080180cba(2149059770)                  0x0000000080180cba(2149059770)                  
a3(x13)             0x0000000080271f06(2150047494)                  0x0000000080271f06(2150047494)                  
a4(x14)             0x00000000800003a0(2147484576)                  0x00000000800003a0(2147484576)                  
a5(x15)             0x0000000080181660(2149062240)                  0x0000000080181660(2149062240)                  
a6(x16)             0x000000000000003f(63)                          0x000000000000003f(63)                          
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x00000000801dff16(2149449494)                  0x00000000801dff16(2149449494)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x0000000000000044(68)                          0x0000000000000044(68)                          
s5(x21)             0x00000000802005cb(2149582283)                  0x00000000802005cb(2149582283)                  
s6(x22)             0x000000008017fb34(2149055284)                  0x000000008017fb34(2149055284)                  
s7(x23)             0x000000008026241b(2149983259)                  0x000000008026241b(2149983259)                  
s8(x24)             0x0000000080181225(2149061157)                  0x0000000080181225(2149061157)                  
s9(x25)             0x000000007ffffaf8(2147482360)                  0x000000007ffffaf8(2147482360)                  
s10(x26)            0x0000000000000001(1)                           0x0000000000000001(1)                           
s11(x27)            0x0000000000000073(115)                         0x0000000000000073(115)                         
t3(x28)             0x000000007ffffab3(2147482291)                  0x000000007ffffab3(2147482291)                  
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x000000008000049e(2147484830)                  0x000000008000049e(2147484830)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            3f884edc73149b2cb0c4898763961bdf432d356a        3f884edc73149b2cb0c4898763961bdf432d356a        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000750(2147485520)                  0x0000000080000750(2147485520)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000044(68)                          0x0000000000000044(68)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f1                  0xc1dff9fed1c00000(-2145909575.0_d)             0xc1dff9fed1c00000(-2145909575.0_d)             
f2                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f10                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f13                 0x7fffffff7fc00000(nan_d)                       0x000002970281b383(1.406903987109e-311_d)       X
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0x41e000029f200000(2147489017.0_d)              0x41e000029f200000(2147489017.0_d)              
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x41e0000066e00000(2147484471.0_d)              0x41e0000066e00000(2147484471.0_d)              
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffffffff6000(512.0_h)                     0xffffffffffff6000(512.0_h)                     
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x41e000029f200000(2147489017.0_d)              0x41e000029f200000(2147489017.0_d)              
STATES DIFFER: True
```

# FailID_000894 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 894
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
_reg_f0: .byte 0xb4,0xd0,0xa5,0xba,0xfa,0x00,0xfd,0xb3
_reg_f1: .byte 0x1c,0x01,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f2: .byte 0xad,0x01,0xc4,0x3c,0x92,0x90,0x3f,0xa4
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x80,0xb0,0xfe,0xff,0xdf,0x41
_reg_f6: .byte 0x00,0x00,0x40,0x13,0xff,0xff,0xdf,0x41
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0xd7,0xc9,0xb6,0x57,0xe4,0x7d,0xf9,0x4c
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x6b,0x25,0xda,0x9f,0x8b,0xfb,0xec,0x35
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x23,0xb0,0x61,0x06,0xff,0xff,0xff,0xff
_reg_f13:.byte 0xff,0x10,0xae,0x23,0x80,0x14,0x7c,0xde
_reg_f14:.byte 0x00,0x00,0xc0,0x30,0x01,0xfa,0xdf,0xc1
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xd3,0xff,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0xff,0x10,0xae,0x23,0x80,0x14,0x7c,0xde
_reg_f20:.byte 0x00,0x00,0x00,0xac,0xbb,0x34,0xcd,0x41
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x40,0x39,0xff,0xff,0xdf,0xc1
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x40,0xac,0x90,0x41
_reg_f26:.byte 0xf7,0x7d,0x2f,0x4f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0xe9,0x41,0xb9,0x5e,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x78,0x2a,0xdc,0x41
_reg_f29:.byte 0x23,0xb0,0x61,0x06,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x1c,0x01,0x18,0x80,0x00,0x00,0x00,0x00
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
    li x1, 0x7ffff8f8            // ra
    li x2, 0x0                   // sp
    li x3, 0x400c0451            // gp
    li x4, 0x80000092            // tp
    li x5, 0xffffffffffffffff    // t0
    li x6, 0xe63ae738            // t1
    li x7, 0x7ffff95f            // t2
    li x8, 0x801805aa            // fp
    li x9, 0x80180302            // s1
    li x10, 0x80                 // a0
    li x11, 0xffffffffaf3ad000   // a1
    li x12, 0x8017fb3d           // a2
    li x13, 0x7ffffc4d           // a3
    li x14, 0x0                  // a4
    li x15, 0x7fffffffc          // a5
    li x16, 0x8dd6724            // a6
    li x17, 0x800001f0           // a7
    li x18, 0x80180302           // s2
    li x19, 0x0                  // s3
    li x20, 0x40000049           // s4
    li x21, 0x800001f0           // s5
    li x22, 0x8018062c           // s6
    li x23, 0x4c2                // s7
    li x24, 0x6000               // s8
    li x25, 0x0                  // s9
    li x26, 0x80180b0b           // s10
    li x27, 0x93                 // s11
    li x28, 0xffffffffdcea4000   // t3
    li x29, 0xffffffff99cf1000   // t4
    li x30, 0x80249ab9           // t5
    li x31, 0x801808a3           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x20'}, 'clob': {'x30', 'f15', 'x20'}})
    
    li x30, 0x1ffff8
    and x20, x20, x30
    li x30, 0x800003f3
    add x20, x20, x30
    fld f15, -0x3f3(x20)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f15                 0xffffffff7fc00000(nan_s)                       0x0261b0230051bc23(3.380756211011658e-297_d)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f15, -0x3f3(x20)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f15                 0xffffffff7fc00000(nan_s)                       0x0261b0230051bc23(3.380756211011658e-297_d)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f15, x3, f3, x20
gp(x3)              0x00000000400c0451(1074529361)                  0x00000000400c0451(1074529361)
s4(x20)             0x000000008000043b(2147484731)                  0x000000008000043b(2147484731)
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
f15                 0xffffffff7fc00000(nan_s)                       0x0261b0230051bc23(3.380756211011658e-297_d)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffff8f8(2147481848)                  0x000000007ffff8f8(2147481848)                  
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x00000000400c0451(1074529361)                  0x00000000400c0451(1074529361)                  
tp(x4)              0x0000000080000092(2147483794)                  0x0000000080000092(2147483794)                  
t0(x5)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t1(x6)              0x00000000e63ae738(3862619960)                  0x00000000e63ae738(3862619960)                  
t2(x7)              0x000000007ffff95f(2147481951)                  0x000000007ffff95f(2147481951)                  
fp(x8)              0x00000000801805aa(2149057962)                  0x00000000801805aa(2149057962)                  
s1(x9)              0x0000000080180302(2149057282)                  0x0000000080180302(2149057282)                  
a0(x10)             0x0000000000000080(128)                         0x0000000000000080(128)                         
a1(x11)             0xffffffffaf3ad000(18446744072354451456)        0xffffffffaf3ad000(18446744072354451456)        
a2(x12)             0x000000008017fb3d(2149055293)                  0x000000008017fb3d(2149055293)                  
a3(x13)             0x000000007ffffc4d(2147482701)                  0x000000007ffffc4d(2147482701)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x00000007fffffffc(34359738364)                 0x00000007fffffffc(34359738364)                 
a6(x16)             0x0000000008dd6724(148727588)                   0x0000000008dd6724(148727588)                   
a7(x17)             0x00000000800001f0(2147484144)                  0x00000000800001f0(2147484144)                  
s2(x18)             0x0000000080180302(2149057282)                  0x0000000080180302(2149057282)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000008000043b(2147484731)                  0x000000008000043b(2147484731)                  
s5(x21)             0x00000000800001f0(2147484144)                  0x00000000800001f0(2147484144)                  
s6(x22)             0x000000008018062c(2149058092)                  0x000000008018062c(2149058092)                  
s7(x23)             0x00000000000004c2(1218)                        0x00000000000004c2(1218)                        
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000080180b0b(2149059339)                  0x0000000080180b0b(2149059339)                  
s11(x27)            0x0000000000000093(147)                         0x0000000000000093(147)                         
t3(x28)             0xffffffffdcea4000(18446744073120923648)        0xffffffffdcea4000(18446744073120923648)        
t4(x29)             0xffffffff99cf1000(18446744071995068416)        0xffffffff99cf1000(18446744071995068416)        
t5(x30)             0x00000000800003f3(2147484659)                  0x00000000800003f3(2147484659)                  
t6(x31)             0x00000000801808a3(2149058723)                  0x00000000801808a3(2149058723)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            81f679df6e61dea67eb75aa4848dea277c6d02b0        81f679df6e61dea67eb75aa4848dea277c6d02b0        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
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
f0                  0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    
f1                  0x000000008018011c(1.061775134e-314_d)          0x000000008018011c(1.061775134e-314_d)          
f2                  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x41dffffeb0800000(2147482306.0_d)              0x41dffffeb0800000(2147482306.0_d)              
f6                  0x41dfffff13400000(2147482701.0_d)              0x41dfffff13400000(2147482701.0_d)              
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x4cf97de457b6c9d7(6.554190042954392e+62_d)     0x4cf97de457b6c9d7(6.554190042954392e+62_d)     
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x35ecfb8b9fda256b(6.197093478488027e-49_d)     0x35ecfb8b9fda256b(6.197093478488027e-49_d)     
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff0661b023(4.2447201453266725e-35_s)    0xffffffff0661b023(4.2447201453266725e-35_s)    
f13                 0xde7c148023ae10ff(-1.4025431970955475e+147_d)  0xde7c148023ae10ff(-1.4025431970955475e+147_d)  
f14                 0xc1dffa0130c00000(-2145912003.0_d)             0xc1dffa0130c00000(-2145912003.0_d)             
f15                 0xffffffff7fc00000(nan_s)                       0x0261b0230051bc23(3.380756211011658e-297_d)    X
f16                 0xffffffff8017ffd3(-2.2039888493608945e-39_s)   0xffffffff8017ffd3(-2.2039888493608945e-39_s)   
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xde7c148023ae10ff(-1.4025431970955475e+147_d)  0xde7c148023ae10ff(-1.4025431970955475e+147_d)  
f20                 0x41cd34bbac000000(979990360.0_d)               0x41cd34bbac000000(979990360.0_d)               
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0xc1dfffff39400000(-2147482853.0_d)             0xc1dfffff39400000(-2147482853.0_d)             
f25                 0x4190ac4000000000(69931008.0_d)                0x4190ac4000000000(69931008.0_d)                
f26                 0xffffffff4f2f7df7(2944268032.0_s)              0xffffffff4f2f7df7(2944268032.0_s)              
f27                 0xffffffff5eb941e9(6.674603478356066e+18_s)     0xffffffff5eb941e9(6.674603478356066e+18_s)     
f28                 0x41dc2a7800000000(1890181120.0_d)              0x41dc2a7800000000(1890181120.0_d)              
f29                 0xffffffff0661b023(4.2447201453266725e-35_s)    0xffffffff0661b023(4.2447201453266725e-35_s)    
f30                 0x000000008018011c(1.061775134e-314_d)          0x000000008018011c(1.061775134e-314_d)          
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

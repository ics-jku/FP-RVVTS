# FailID_005119 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 5119
* Isolated failing instruction: `fsw`
* Minimized failing test case: [cblock_minimized_test_case.json](cblock_minimized_test_case.json)
* Resulting REF machine state: [mstate_RefSail.json](mstate_RefSail.json)
* Resulting DUT machine state: [mstate_DUT_VPpp_SF.json](mstate_DUT_VPpp_SF.json)
* Automated failure characterization report: [AFC_FP_report.log](AFC_FP_report.log)

## Report

### Minimized Failing Test Case
```
    // FLOATINGPOINT STATE DATA
    j _float_data_end
    .align 4
_reg_f0: .byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x80,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x80,0x5f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x07,0xf0,0xc5,0x81,0xbe,0x4c,0x74,0x4f
_reg_f28:.byte 0x6e,0x03,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x40,0x38,0xff,0xf9,0xdf,0xc1
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x28
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80109011            // ra
    li x2, 0x4941a000            // sp
    li x3, 0xba                  // gp
    li x4, 0x7ffffff7            // tp
    li x5, 0x80198698            // t0
    li x6, 0x8018022f            // t1
    li x7, 0xffffffff7fe8024e    // t2
    li x8, 0x8017fd63            // fp
    li x9, 0x7ffffccf            // s1
    li x10, 0x8017f7d7           // a0
    li x11, 0x7ffffccf           // a1
    li x12, 0x7ffffe49           // a2
    li x13, 0x8027f819           // a3
    li x14, 0x6000               // a4
    li x15, 0xfffffffffffffead   // a5
    li x16, 0x802005fa           // a6
    li x17, 0x7ffffe63           // a7
    li x18, 0x200601edc0         // s2
    li x19, 0x12                 // s3
    li x20, 0x92                 // s4
    li x21, 0x801807b7           // s5
    li x22, 0x7ffffc0d           // s6
    li x23, 0x8017fa33           // s7
    li x24, 0x8017fd71           // s8
    li x25, 0x7fff               // s9
    li x26, 0x0                  // s10
    li x27, 0x8f                 // s11
    li x28, 0x7fffff37           // t3
    li x29, 0x1                  // t4
    li x30, 0x7ffff985           // t5
    li x31, 0x801ffc67           // t6
    // INSTRUCTION ({'dep': {'f30', 'x19', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'x19', 'x10'}})
    
    li x10, 0xffffc
    and x19, x19, x10
    li x10, 0x8017f93b
    add x19, x19, x10
    fsw f30, 0x6c5(x19)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        0d0aae6e08bdc46facc5fb2a2f43fd82be54e897        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f30, 0x6c5(x19)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        0d0aae6e08bdc46facc5fb2a2f43fd82be54e897        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f30, x6, c5, x19
t1(x6)              0x000000008018022f(2149057071)                  0x000000008018022f(2149057071)
s3(x19)             0x000000008017f94b(2149054795)                  0x000000008017f94b(2149054795)
f30                 0xc1dff9ff38400000(-2145909985.0_d)             0xc1dff9ff38400000(-2145909985.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080109011(2148569105)                  0x0000000080109011(2148569105)                  
sp(x2)              0x000000004941a000(1229037568)                  0x000000004941a000(1229037568)                  
gp(x3)              0x00000000000000ba(186)                         0x00000000000000ba(186)                         
tp(x4)              0x000000007ffffff7(2147483639)                  0x000000007ffffff7(2147483639)                  
t0(x5)              0x0000000080198698(2149156504)                  0x0000000080198698(2149156504)                  
t1(x6)              0x000000008018022f(2149057071)                  0x000000008018022f(2149057071)                  
t2(x7)              0xffffffff7fe8024e(18446744071560495694)        0xffffffff7fe8024e(18446744071560495694)        
fp(x8)              0x000000008017fd63(2149055843)                  0x000000008017fd63(2149055843)                  
s1(x9)              0x000000007ffffccf(2147482831)                  0x000000007ffffccf(2147482831)                  
a0(x10)             0x000000008017f93b(2149054779)                  0x000000008017f93b(2149054779)                  
a1(x11)             0x000000007ffffccf(2147482831)                  0x000000007ffffccf(2147482831)                  
a2(x12)             0x000000007ffffe49(2147483209)                  0x000000007ffffe49(2147483209)                  
a3(x13)             0x000000008027f819(2150103065)                  0x000000008027f819(2150103065)                  
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0xfffffffffffffead(18446744073709551277)        0xfffffffffffffead(18446744073709551277)        
a6(x16)             0x00000000802005fa(2149582330)                  0x00000000802005fa(2149582330)                  
a7(x17)             0x000000007ffffe63(2147483235)                  0x000000007ffffe63(2147483235)                  
s2(x18)             0x000000200601edc0(137539743168)                0x000000200601edc0(137539743168)                
s3(x19)             0x000000008017f94b(2149054795)                  0x000000008017f94b(2149054795)                  
s4(x20)             0x0000000000000092(146)                         0x0000000000000092(146)                         
s5(x21)             0x00000000801807b7(2149058487)                  0x00000000801807b7(2149058487)                  
s6(x22)             0x000000007ffffc0d(2147482637)                  0x000000007ffffc0d(2147482637)                  
s7(x23)             0x000000008017fa33(2149055027)                  0x000000008017fa33(2149055027)                  
s8(x24)             0x000000008017fd71(2149055857)                  0x000000008017fd71(2149055857)                  
s9(x25)             0x0000000000007fff(32767)                       0x0000000000007fff(32767)                       
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000000000008f(143)                         0x000000000000008f(143)                         
t3(x28)             0x000000007fffff37(2147483447)                  0x000000007fffff37(2147483447)                  
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x000000007ffff985(2147481989)                  0x000000007ffff985(2147481989)                  
t6(x31)             0x00000000801ffc67(2149579879)                  0x00000000801ffc67(2149579879)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            0edddb42e79f53c32922dcb54f138fbe2c25073d        0edddb42e79f53c32922dcb54f138fbe2c25073d        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        0d0aae6e08bdc46facc5fb2a2f43fd82be54e897        X
lastPC              0x0000000080000750(2147485520)                  0x0000000080000750(2147485520)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000028(40)                          0x0000000000000028(40)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f1                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff4f0017fd(2149055744.0_s)              0xffffffff4f0017fd(2149055744.0_s)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f16                 0xffffffff4eff8000(2143289344.0_s)              0xffffffff4eff8000(2143289344.0_s)              
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff5f800000(1.8446744073709552e+19_s)    0xffffffff5f800000(1.8446744073709552e+19_s)    
f20                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f21                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f26                 0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f27                 0x4f744cbe81c5f007(5.738657611920474e+74_d)     0x4f744cbe81c5f007(5.738657611920474e+74_d)     
f28                 0xffffffff8000036e(-1.2303400516771894e-42_s)   0xffffffff8000036e(-1.2303400516771894e-42_s)   
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xc1dff9ff38400000(-2145909985.0_d)             0xc1dff9ff38400000(-2145909985.0_d)             
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

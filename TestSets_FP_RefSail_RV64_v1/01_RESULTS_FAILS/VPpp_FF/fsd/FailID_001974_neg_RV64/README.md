# FailID_001974 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1974
* Isolated failing instruction: `fsd`
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x80,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x80,0x5f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x6e,0x03,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x07,0xf0,0xc5,0x81,0xbe,0x4c,0x74,0x4f
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x40,0x00,0x03,0xe0,0x41
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x10
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8028003c            // ra
    li x2, 0x8017fec0            // sp
    li x3, 0x80180985            // gp
    li x4, 0x7ffffc41            // tp
    li x5, 0x6000                // t0
    li x6, 0x7fffffb1            // t1
    li x7, 0x0                   // t2
    li x8, 0x0                   // fp
    li x9, 0x8000057d            // s1
    li x10, 0x8018008c           // a0
    li x11, 0x8                  // a1
    li x12, 0x801ff49d           // a2
    li x13, 0x0                  // a3
    li x14, 0x0                  // a4
    li x15, 0x80188ece           // a5
    li x16, 0x0                  // a6
    li x17, 0x7fffffffffffffff   // a7
    li x18, 0x8000076a           // s2
    li x19, 0x80180178           // s3
    li x20, 0x0                  // s4
    li x21, 0x8018076d           // s5
    li x22, 0xe3                 // s6
    li x23, 0x7ffffeed           // s7
    li x24, 0x6000               // s8
    li x25, 0x2                  // s9
    li x26, 0x6000               // s10
    li x27, 0x8017f480           // s11
    li x28, 0x6000               // t3
    li x29, 0x80000309           // t4
    li x30, 0x8001b156           // t5
    li x31, 0x7ffffc08           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f7', 'x31'}, 'clob': {'x31', 'x21'}})
    
    li x21, 0xffff8
    and x31, x31, x21
    li x21, 0x8018068a
    add x31, x31, x21
    fsd f7, -0x68a(x31)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        1975909b10ebd8da1ea1f30261dabc3957abcdb5        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f7, -0x68a(x31)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        1975909b10ebd8da1ea1f30261dabc3957abcdb5        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f7, x68, x31
t6(x31)             0x0000000080280292(2150105746)                  0x0000000080280292(2150105746)
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008028003c(2150105148)                  0x000000008028003c(2150105148)                  
sp(x2)              0x000000008017fec0(2149056192)                  0x000000008017fec0(2149056192)                  
gp(x3)              0x0000000080180985(2149058949)                  0x0000000080180985(2149058949)                  
tp(x4)              0x000000007ffffc41(2147482689)                  0x000000007ffffc41(2147482689)                  
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t1(x6)              0x000000007fffffb1(2147483569)                  0x000000007fffffb1(2147483569)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x000000008000057d(2147485053)                  0x000000008000057d(2147485053)                  
a0(x10)             0x000000008018008c(2149056652)                  0x000000008018008c(2149056652)                  
a1(x11)             0x0000000000000008(8)                           0x0000000000000008(8)                           
a2(x12)             0x00000000801ff49d(2149577885)                  0x00000000801ff49d(2149577885)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000080188ece(2149093070)                  0x0000000080188ece(2149093070)                  
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s2(x18)             0x000000008000076a(2147485546)                  0x000000008000076a(2147485546)                  
s3(x19)             0x0000000080180178(2149056888)                  0x0000000080180178(2149056888)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x000000008018068a(2149058186)                  0x000000008018068a(2149058186)                  
s6(x22)             0x00000000000000e3(227)                         0x00000000000000e3(227)                         
s7(x23)             0x000000007ffffeed(2147483373)                  0x000000007ffffeed(2147483373)                  
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x0000000000000002(2)                           0x0000000000000002(2)                           
s10(x26)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s11(x27)            0x000000008017f480(2149053568)                  0x000000008017f480(2149053568)                  
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x0000000080000309(2147484425)                  0x0000000080000309(2147484425)                  
t5(x30)             0x000000008001b156(2147594582)                  0x000000008001b156(2147594582)                  
t6(x31)             0x0000000080280292(2150105746)                  0x0000000080280292(2150105746)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            07b5eb354dc2aceea068dafbd1d57bd8a5c94af5        07b5eb354dc2aceea068dafbd1d57bd8a5c94af5        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        1975909b10ebd8da1ea1f30261dabc3957abcdb5        X
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000010(16)                          0x0000000000000010(16)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff4f0017fd(2149055744.0_s)              0xffffffff4f0017fd(2149055744.0_s)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f16                 0xffffffff4eff8000(2143289344.0_s)              0xffffffff4eff8000(2143289344.0_s)              
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff5f800000(1.8446744073709552e+19_s)    0xffffffff5f800000(1.8446744073709552e+19_s)    
f20                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f21                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f22                 0xffffffff8000036e(-1.2303400516771894e-42_s)   0xffffffff8000036e(-1.2303400516771894e-42_s)   
f23                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xffffffff4f0017fd(2149055744.0_s)              0xffffffff4f0017fd(2149055744.0_s)              
f27                 0x4f744cbe81c5f007(5.738657611920474e+74_d)     0x4f744cbe81c5f007(5.738657611920474e+74_d)     
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x41e0030040000000(2149057024.0_d)              0x41e0030040000000(2149057024.0_d)              
f30                 0xc1dff9ff38400000(-2145909985.0_d)             0xc1dff9ff38400000(-2145909985.0_d)             
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

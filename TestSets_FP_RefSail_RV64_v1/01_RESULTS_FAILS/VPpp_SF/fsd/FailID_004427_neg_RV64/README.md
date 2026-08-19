# FailID_004427 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4427
* Isolated failing instruction: `fsd`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x40,0xdd,0xff,0x02,0xe0,0xc1
_reg_f4: .byte 0x52,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x30,0x4a,0xe0,0xd2,0xc1
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x44,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x96,0x00,0x04,0xe0,0x41
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0xd7,0x9f,0x73,0x00,0x00,0x00,0x00
_reg_f19:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x03,0xb3,0x01,0x02,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x04,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x40,0x35,0x00,0x03,0xe0,0x41
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x42
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017fbb2            // ra
    li x2, 0x67                  // sp
    li x3, 0x8017fea9            // gp
    li x4, 0x801ffbe5            // tp
    li x5, 0x7ffffc95            // t0
    li x6, 0x42                  // t1
    li x7, 0x8018014e            // t2
    li x8, 0x7fffffcc            // fp
    li x9, 0x5a                  // s1
    li x10, 0x8017fea9           // a0
    li x11, 0x80185ae2           // a1
    li x12, 0x452da708           // a2
    li x13, 0x801801aa           // a3
    li x14, 0x801804b1           // a4
    li x15, 0x0                  // a5
    li x16, 0x6000               // a6
    li x17, 0x0                  // a7
    li x18, 0x801807bb           // s2
    li x19, 0x0                  // s3
    li x20, 0x8000016a           // s4
    li x21, 0x0                  // s5
    li x22, 0x80005aa4           // s6
    li x23, 0x8009b16a           // s7
    li x24, 0x1                  // s8
    li x25, 0x4a62c704           // s9
    li x26, 0xff                 // s10
    li x27, 0x0                  // s11
    li x28, 0x800004f9           // t3
    li x29, 0x800004f9           // t4
    li x30, 0x6000               // t5
    li x31, 0x800005e5           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f28', 'x30'}, 'clob': {'x8', 'x30'}})
    
    li x8, 0xffff8
    and x30, x30, x8
    li x8, 0x801806b5
    add x30, x30, x8
    fsd f28, -0x6b5(x30)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        749d9c6e1de6086be3f6be023ff262da50a45044        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f28, -0x6b5(x30)
+========================================================================================================================+
Attributes:  fcsr ['underflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        749d9c6e1de6086be3f6be023ff262da50a45044        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f28, x6, b5, x30
t1(x6)              0x0000000000000042(66)                          0x0000000000000042(66)
t5(x30)             0x00000000801866b5(2149082805)                  0x00000000801866b5(2149082805)
f28                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fbb2(2149055410)                  0x000000008017fbb2(2149055410)                  
sp(x2)              0x0000000000000067(103)                         0x0000000000000067(103)                         
gp(x3)              0x000000008017fea9(2149056169)                  0x000000008017fea9(2149056169)                  
tp(x4)              0x00000000801ffbe5(2149579749)                  0x00000000801ffbe5(2149579749)                  
t0(x5)              0x000000007ffffc95(2147482773)                  0x000000007ffffc95(2147482773)                  
t1(x6)              0x0000000000000042(66)                          0x0000000000000042(66)                          
t2(x7)              0x000000008018014e(2149056846)                  0x000000008018014e(2149056846)                  
fp(x8)              0x00000000801806b5(2149058229)                  0x00000000801806b5(2149058229)                  
s1(x9)              0x000000000000005a(90)                          0x000000000000005a(90)                          
a0(x10)             0x000000008017fea9(2149056169)                  0x000000008017fea9(2149056169)                  
a1(x11)             0x0000000080185ae2(2149079778)                  0x0000000080185ae2(2149079778)                  
a2(x12)             0x00000000452da708(1160619784)                  0x00000000452da708(1160619784)                  
a3(x13)             0x00000000801801aa(2149056938)                  0x00000000801801aa(2149056938)                  
a4(x14)             0x00000000801804b1(2149057713)                  0x00000000801804b1(2149057713)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x00000000801807bb(2149058491)                  0x00000000801807bb(2149058491)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000008000016a(2147484010)                  0x000000008000016a(2147484010)                  
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000080005aa4(2147506852)                  0x0000000080005aa4(2147506852)                  
s7(x23)             0x000000008009b16a(2148118890)                  0x000000008009b16a(2148118890)                  
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x000000004a62c704(1247987460)                  0x000000004a62c704(1247987460)                  
s10(x26)            0x00000000000000ff(255)                         0x00000000000000ff(255)                         
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x00000000800004f9(2147484921)                  0x00000000800004f9(2147484921)                  
t4(x29)             0x00000000800004f9(2147484921)                  0x00000000800004f9(2147484921)                  
t5(x30)             0x00000000801866b5(2149082805)                  0x00000000801866b5(2149082805)                  
t6(x31)             0x00000000800005e5(2147485157)                  0x00000000800005e5(2147485157)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            a24a5751b981568f22a49bb6ccf3481bd1a4776e        a24a5751b981568f22a49bb6ccf3481bd1a4776e        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        749d9c6e1de6086be3f6be023ff262da50a45044        X
lastPC              0x0000000080000748(2147485512)                  0x0000000080000748(2147485512)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000042(66)                          0x0000000000000042(66)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xc1e002ffdd400000(-2149056234.0_d)             0xc1e002ffdd400000(-2149056234.0_d)             
f4                  0xffffffffffffff52(nan_h)                       0xffffffffffffff52(nan_h)                       
f5                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f6                  0xc1d2e04a30000000(-1266755776.0_d)             0xc1d2e04a30000000(-1266755776.0_d)             
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)                     
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x41e0040096000000(2149582000.0_d)              0x41e0040096000000(2149582000.0_d)              
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x00000000739fd700(9.58415765e-315_d)           0x00000000739fd700(9.58415765e-315_d)           
f19                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f20                 0xffffffff0201b303(9.528797047284384e-38_s)     0xffffffff0201b303(9.528797047284384e-38_s)     
f21                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f24                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f25                 0xffffffff4f001804(2149057536.0_s)              0xffffffff4f001804(2149057536.0_s)              
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x41e0030035400000(2149056938.0_d)              0x41e0030035400000(2149056938.0_d)              
STATES DIFFER: True
```

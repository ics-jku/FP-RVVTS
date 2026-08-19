# FailID_001675 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1675
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
    li x1, 0x7ffffe93            // ra
    li x2, 0x8000067c            // sp
    li x3, 0x8017ff2f            // gp
    li x4, 0x4f8e1c11            // tp
    li x5, 0x801807b2            // t0
    li x6, 0x1aa85000            // t1
    li x7, 0x0                   // t2
    li x8, 0x801800c1            // fp
    li x9, 0x80000254            // s1
    li x10, 0x6000               // a0
    li x11, 0x8018000e           // a1
    li x12, 0x1                  // a2
    li x13, 0x8028033a           // a3
    li x14, 0x0                  // a4
    li x15, 0x800014f9           // a5
    li x16, 0x80180885           // a6
    li x17, 0x1                  // a7
    li x18, 0x801dff16           // s2
    li x19, 0x0                  // s3
    li x20, 0x8017fb4e           // s4
    li x21, 0x802005cb           // s5
    li x22, 0x8017fb34           // s6
    li x23, 0xffffffffe6be2000   // s7
    li x24, 0xeb                 // s8
    li x25, 0x1                  // s9
    li x26, 0x8000072c           // s10
    li x27, 0x73                 // s11
    li x28, 0x6000               // t3
    li x29, 0x8000047c           // t4
    li x30, 0x0                  // t5
    li x31, 0x8017fdbf           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f26', 'x1'}, 'clob': {'x5', 'x1'}})
    
    li x5, 0xffff8
    and x1, x1, x5
    li x5, 0x8017f8d1
    add x1, x1, x5
    fsd f26, 0x72f(x1)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        6ac8b21389208e0e54b7964179e2df790e9f0d15        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f26, 0x72f(x1)
+========================================================================================================================+
Attributes:  fcsr ['overflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        6ac8b21389208e0e54b7964179e2df790e9f0d15        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f26, x72, x1
ra(x1)              0x000000008027f761(2150102881)                  0x000000008027f761(2150102881)
f26                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008027f761(2150102881)                  0x000000008027f761(2150102881)                  
sp(x2)              0x000000008000067c(2147485308)                  0x000000008000067c(2147485308)                  
gp(x3)              0x000000008017ff2f(2149056303)                  0x000000008017ff2f(2149056303)                  
tp(x4)              0x000000004f8e1c11(1334713361)                  0x000000004f8e1c11(1334713361)                  
t0(x5)              0x000000008017f8d1(2149054673)                  0x000000008017f8d1(2149054673)                  
t1(x6)              0x000000001aa85000(447238144)                   0x000000001aa85000(447238144)                   
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x00000000801800c1(2149056705)                  0x00000000801800c1(2149056705)                  
s1(x9)              0x0000000080000254(2147484244)                  0x0000000080000254(2147484244)                  
a0(x10)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a1(x11)             0x000000008018000e(2149056526)                  0x000000008018000e(2149056526)                  
a2(x12)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a3(x13)             0x000000008028033a(2150105914)                  0x000000008028033a(2150105914)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x00000000800014f9(2147489017)                  0x00000000800014f9(2147489017)                  
a6(x16)             0x0000000080180885(2149058693)                  0x0000000080180885(2149058693)                  
a7(x17)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s2(x18)             0x00000000801dff16(2149449494)                  0x00000000801dff16(2149449494)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000008017fb4e(2149055310)                  0x000000008017fb4e(2149055310)                  
s5(x21)             0x00000000802005cb(2149582283)                  0x00000000802005cb(2149582283)                  
s6(x22)             0x000000008017fb34(2149055284)                  0x000000008017fb34(2149055284)                  
s7(x23)             0xffffffffe6be2000(18446744073285804032)        0xffffffffe6be2000(18446744073285804032)        
s8(x24)             0x00000000000000eb(235)                         0x00000000000000eb(235)                         
s9(x25)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s10(x26)            0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
s11(x27)            0x0000000000000073(115)                         0x0000000000000073(115)                         
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x000000008000047c(2147484796)                  0x000000008000047c(2147484796)                  
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x000000008017fdbf(2149055935)                  0x000000008017fdbf(2149055935)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            87f283372eac4580e9251015557e25e1cf84be01        87f283372eac4580e9251015557e25e1cf84be01        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        6ac8b21389208e0e54b7964179e2df790e9f0d15        X
lastPC              0x000000008000074c(2147485516)                  0x000000008000074c(2147485516)                  
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
f13                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
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

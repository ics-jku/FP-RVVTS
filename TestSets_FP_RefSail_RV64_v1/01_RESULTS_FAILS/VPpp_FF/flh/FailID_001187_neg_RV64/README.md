# FailID_001187 VP++ FF neg RV64 flh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1187
* Isolated failing instruction: `flh`
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
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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
_reg_f22:.byte 0x6e,0x03,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x07,0xf0,0xc5,0x81,0xbe,0x4c,0x74,0x4f
_reg_f28:.byte 0x6e,0x03,0x00,0x80,0xff,0xff,0xff,0xff
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
    li x1, 0x8000034a            // ra
    li x2, 0x8017fec0            // sp
    li x3, 0x80180985            // gp
    li x4, 0x7ffffc41            // tp
    li x5, 0x80017c60            // t0
    li x6, 0x6428174c            // t1
    li x7, 0x801807ed            // t2
    li x8, 0x800e68ae            // fp
    li x9, 0x800006c4            // s1
    li x10, 0x7ffffba8           // a0
    li x11, 0xee                 // a1
    li x12, 0x801ff49d           // a2
    li x13, 0x1                  // a3
    li x14, 0x1                  // a4
    li x15, 0x43788764           // a5
    li x16, 0x0                  // a6
    li x17, 0x8018076d           // a7
    li x18, 0xffffffffff840000   // s2
    li x19, 0x80180178           // s3
    li x20, 0x80180078           // s4
    li x21, 0x8018076d           // s5
    li x22, 0xe3                 // s6
    li x23, 0x0                  // s7
    li x24, 0x1                  // s8
    li x25, 0x2                  // s9
    li x26, 0x1d                 // s10
    li x27, 0x0                  // s11
    li x28, 0x73e53760           // t3
    li x29, 0x80000282           // t4
    li x30, 0x13e1b023           // t5
    li x31, 0x7ffffc08           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x30', 'mstatus.fs/vs.fs'}, 'clob': {'f14', 'x30', 'x9'}})
    
    li x9, 0x1ffffe
    and x30, x30, x9
    li x9, 0x80000134
    add x30, x30, x9
    flh f14, -0x134(x30)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f14                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flh f14, -0x134(x30)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f14                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x134, x30
t5(x30)             0x000000008001b156(2147594582)                  0x000000008001b156(2147594582)
f14                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008000034a(2147484490)                  0x000000008000034a(2147484490)                  
sp(x2)              0x000000008017fec0(2149056192)                  0x000000008017fec0(2149056192)                  
gp(x3)              0x0000000080180985(2149058949)                  0x0000000080180985(2149058949)                  
tp(x4)              0x000000007ffffc41(2147482689)                  0x000000007ffffc41(2147482689)                  
t0(x5)              0x0000000080017c60(2147581024)                  0x0000000080017c60(2147581024)                  
t1(x6)              0x000000006428174c(1680349004)                  0x000000006428174c(1680349004)                  
t2(x7)              0x00000000801807ed(2149058541)                  0x00000000801807ed(2149058541)                  
fp(x8)              0x00000000800e68ae(2148427950)                  0x00000000800e68ae(2148427950)                  
s1(x9)              0x0000000080000134(2147483956)                  0x0000000080000134(2147483956)                  
a0(x10)             0x000000007ffffba8(2147482536)                  0x000000007ffffba8(2147482536)                  
a1(x11)             0x00000000000000ee(238)                         0x00000000000000ee(238)                         
a2(x12)             0x00000000801ff49d(2149577885)                  0x00000000801ff49d(2149577885)                  
a3(x13)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a4(x14)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a5(x15)             0x0000000043788764(1131972452)                  0x0000000043788764(1131972452)                  
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x000000008018076d(2149058413)                  0x000000008018076d(2149058413)                  
s2(x18)             0xffffffffff840000(18446744073701425152)        0xffffffffff840000(18446744073701425152)        
s3(x19)             0x0000000080180178(2149056888)                  0x0000000080180178(2149056888)                  
s4(x20)             0x0000000080180078(2149056632)                  0x0000000080180078(2149056632)                  
s5(x21)             0x000000008018076d(2149058413)                  0x000000008018076d(2149058413)                  
s6(x22)             0x00000000000000e3(227)                         0x00000000000000e3(227)                         
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x0000000000000002(2)                           0x0000000000000002(2)                           
s10(x26)            0x000000000000001d(29)                          0x000000000000001d(29)                          
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x0000000073e53760(1944401760)                  0x0000000073e53760(1944401760)                  
t4(x29)             0x0000000080000282(2147484290)                  0x0000000080000282(2147484290)                  
t5(x30)             0x000000008001b156(2147594582)                  0x000000008001b156(2147594582)                  
t6(x31)             0x000000007ffffc08(2147482632)                  0x000000007ffffc08(2147482632)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            0f8a3455e524f95ffbef9cede2ca42a8b2dada33        0f8a3455e524f95ffbef9cede2ca42a8b2dada33        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
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
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f14                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
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
f28                 0xffffffff8000036e(-1.2303400516771894e-42_s)   0xffffffff8000036e(-1.2303400516771894e-42_s)   
f29                 0x41e0030040000000(2149057024.0_d)              0x41e0030040000000(2149057024.0_d)              
f30                 0xc1dff9ff38400000(-2145909985.0_d)             0xc1dff9ff38400000(-2145909985.0_d)             
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

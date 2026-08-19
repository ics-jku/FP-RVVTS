# FailID_001325 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1325
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x60,0x5a,0x00,0x00,0xe0,0x41
_reg_f10:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x23,0xb8,0x81,0x06,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xfa,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0xd0,0x42,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
_reg_f28:.byte 0x97,0x02,0x00,0x00,0x93,0x82,0x02,0xf0
_reg_f29:.byte 0x00,0x00,0x80,0x46,0x00,0x00,0xe0,0x41
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x88
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80180264            // ra
    li x2, 0x0                   // sp
    li x3, 0x801804fa            // gp
    li x4, 0x7ffffd75            // tp
    li x5, 0x644fa000            // t0
    li x6, 0x3ed6000             // t1
    li x7, 0x80180701            // t2
    li x8, 0x8017fba6            // fp
    li x9, 0x800002d3            // s1
    li x10, 0x7f1dd74c           // a0
    li x11, 0x80186701           // a1
    li x12, 0x1                  // a2
    li x13, 0x6000               // a3
    li x14, 0x801eae9a           // a4
    li x15, 0x80000625           // a5
    li x16, 0x0                  // a6
    li x17, 0x800007d8           // a7
    li x18, 0x8017fba6           // s2
    li x19, 0x0                  // s3
    li x20, 0xff                 // s4
    li x21, 0x8018060a           // s5
    li x22, 0x16                 // s6
    li x23, 0x98                 // s7
    li x24, 0x1                  // s8
    li x25, 0x6000               // s9
    li x26, 0x1                  // s10
    li x27, 0x80000838           // s11
    li x28, 0x8000073c           // t3
    li x29, 0x7ffffbbc           // t4
    li x30, 0x7fffff1e           // t5
    li x31, 0xab                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x17'}, 'clob': {'x17', 'x29', 'f22'}})
    
    li x29, 0x1ffffc
    and x17, x17, x29
    li x29, 0x7ffffb99
    add x17, x17, x29
    flw f22, 0x467(x17)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f22                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f22, 0x467(x17)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f22                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f22, x467, x17
a7(x17)             0x0000000080000371(2147484529)                  0x0000000080000371(2147484529)
f22                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080180264(2149057124)                  0x0000000080180264(2149057124)                  
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x00000000801804fa(2149057786)                  0x00000000801804fa(2149057786)                  
tp(x4)              0x000000007ffffd75(2147482997)                  0x000000007ffffd75(2147482997)                  
t0(x5)              0x00000000644fa000(1682939904)                  0x00000000644fa000(1682939904)                  
t1(x6)              0x0000000003ed6000(65888256)                    0x0000000003ed6000(65888256)                    
t2(x7)              0x0000000080180701(2149058305)                  0x0000000080180701(2149058305)                  
fp(x8)              0x000000008017fba6(2149055398)                  0x000000008017fba6(2149055398)                  
s1(x9)              0x00000000800002d3(2147484371)                  0x00000000800002d3(2147484371)                  
a0(x10)             0x000000007f1dd74c(2132662092)                  0x000000007f1dd74c(2132662092)                  
a1(x11)             0x0000000080186701(2149082881)                  0x0000000080186701(2149082881)                  
a2(x12)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x00000000801eae9a(2149494426)                  0x00000000801eae9a(2149494426)                  
a5(x15)             0x0000000080000625(2147485221)                  0x0000000080000625(2147485221)                  
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x0000000080000371(2147484529)                  0x0000000080000371(2147484529)                  
s2(x18)             0x000000008017fba6(2149055398)                  0x000000008017fba6(2149055398)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x00000000000000ff(255)                         0x00000000000000ff(255)                         
s5(x21)             0x000000008018060a(2149058058)                  0x000000008018060a(2149058058)                  
s6(x22)             0x0000000000000016(22)                          0x0000000000000016(22)                          
s7(x23)             0x0000000000000098(152)                         0x0000000000000098(152)                         
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s10(x26)            0x0000000000000001(1)                           0x0000000000000001(1)                           
s11(x27)            0x0000000080000838(2147485752)                  0x0000000080000838(2147485752)                  
t3(x28)             0x000000008000073c(2147485500)                  0x000000008000073c(2147485500)                  
t4(x29)             0x000000007ffffb99(2147482521)                  0x000000007ffffb99(2147482521)                  
t5(x30)             0x000000007fffff1e(2147483422)                  0x000000007fffff1e(2147483422)                  
t6(x31)             0x00000000000000ab(171)                         0x00000000000000ab(171)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            16a255db4de393a267a2efb871091e42bb2fd8cb        16a255db4de393a267a2efb871091e42bb2fd8cb        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000088(136)                         0x0000000000000088(136)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f6                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x41e000005a600000(2147484371.0_d)              0x41e000005a600000(2147484371.0_d)              
f10                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f18                 0xffffffff0681b823(4.8794971392781e-35_s)       0xffffffff0681b823(4.8794971392781e-35_s)       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff4f0017fa(2149054976.0_s)              0xffffffff4f0017fa(2149054976.0_s)              
f22                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
f23                 0xffffffff42d00000(104.0_s)                     0xffffffff42d00000(104.0_s)                     
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f28                 0xf002829300000297(-3.5921495148046916e+231_d)  0xf002829300000297(-3.5921495148046916e+231_d)  
f29                 0x41e0000046800000(2147484212.0_d)              0x41e0000046800000(2147484212.0_d)              
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
STATES DIFFER: True
```

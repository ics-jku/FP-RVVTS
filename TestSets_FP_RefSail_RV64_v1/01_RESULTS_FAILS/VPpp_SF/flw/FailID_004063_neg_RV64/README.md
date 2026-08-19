# FailID_004063 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4063
* Isolated failing instruction: `flw`
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xe0,0x31,0x00,0x00,0xe0,0x41
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0xfa,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x40,0x8d,0xcb,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0xcc,0xf9,0x2e,0xd7,0x41
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x5a,0xfe,0x27,0x80,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0xfe,0xff,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0xd3,0x0e,0x00,0xd2,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x22
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x5e41e734            // ra
    li x2, 0x2cc39000            // sp
    li x3, 0x8017fe91            // gp
    li x4, 0x8017fcba            // tp
    li x5, 0x8017fe5a            // t0
    li x6, 0x80180960            // t1
    li x7, 0x80000563            // t2
    li x8, 0x801894a9            // fp
    li x9, 0x0                   // s1
    li x10, 0x8018003f           // a0
    li x11, 0x8017fdb5           // a1
    li x12, 0xf2                 // a2
    li x13, 0xffffffff8000018f   // a3
    li x14, 0xffffffffffffffff   // a4
    li x15, 0x801801b9           // a5
    li x16, 0xde4dfff4           // a6
    li x17, 0x8025e003           // a7
    li x18, 0x80185db5           // s2
    li x19, 0x0                  // s3
    li x20, 0x7ffffed6           // s4
    li x21, 0x7ffffb47           // s5
    li x22, 0x5cbbe730           // s6
    li x23, 0xfbc9475c           // s7
    li x24, 0x80280130           // s8
    li x25, 0x80000095           // s9
    li x26, 0x801801f9           // s10
    li x27, 0x8027fc51           // s11
    li x28, 0x1                  // t3
    li x29, 0x7fc00000           // t4
    li x30, 0x8017f806           // t5
    li x31, 0x6000               // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x29', 'fcsr.rm'}, 'clob': {'x29', 'x24', 'f5'}})
    
    li x24, 0x1ffffc
    and x29, x29, x24
    li x24, 0x8000058a
    add x29, x29, x24
    flw f5, -0x58a(x29)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f5                  0x7fffffff7fc00000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f5, -0x58a(x29)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f5                  0x7fffffff7fc00000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f5, x58, x29
t4(x29)             0x000000008000058a(2147485066)                  0x000000008000058a(2147485066)
f5                  0x7fffffff7fc00000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000005e41e734(1581377332)                  0x000000005e41e734(1581377332)                  
sp(x2)              0x000000002cc39000(751013888)                   0x000000002cc39000(751013888)                   
gp(x3)              0x000000008017fe91(2149056145)                  0x000000008017fe91(2149056145)                  
tp(x4)              0x000000008017fcba(2149055674)                  0x000000008017fcba(2149055674)                  
t0(x5)              0x000000008017fe5a(2149056090)                  0x000000008017fe5a(2149056090)                  
t1(x6)              0x0000000080180960(2149058912)                  0x0000000080180960(2149058912)                  
t2(x7)              0x0000000080000563(2147485027)                  0x0000000080000563(2147485027)                  
fp(x8)              0x00000000801894a9(2149094569)                  0x00000000801894a9(2149094569)                  
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x000000008018003f(2149056575)                  0x000000008018003f(2149056575)                  
a1(x11)             0x000000008017fdb5(2149055925)                  0x000000008017fdb5(2149055925)                  
a2(x12)             0x00000000000000f2(242)                         0x00000000000000f2(242)                         
a3(x13)             0xffffffff8000018f(18446744071562068367)        0xffffffff8000018f(18446744071562068367)        
a4(x14)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a5(x15)             0x00000000801801b9(2149056953)                  0x00000000801801b9(2149056953)                  
a6(x16)             0x00000000de4dfff4(3729653748)                  0x00000000de4dfff4(3729653748)                  
a7(x17)             0x000000008025e003(2149965827)                  0x000000008025e003(2149965827)                  
s2(x18)             0x0000000080185db5(2149080501)                  0x0000000080185db5(2149080501)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000007ffffed6(2147483350)                  0x000000007ffffed6(2147483350)                  
s5(x21)             0x000000007ffffb47(2147482439)                  0x000000007ffffb47(2147482439)                  
s6(x22)             0x000000005cbbe730(1555818288)                  0x000000005cbbe730(1555818288)                  
s7(x23)             0x00000000fbc9475c(4224272220)                  0x00000000fbc9475c(4224272220)                  
s8(x24)             0x000000008000058a(2147485066)                  0x000000008000058a(2147485066)                  
s9(x25)             0x0000000080000095(2147483797)                  0x0000000080000095(2147483797)                  
s10(x26)            0x00000000801801f9(2149057017)                  0x00000000801801f9(2149057017)                  
s11(x27)            0x000000008027fc51(2150104145)                  0x000000008027fc51(2150104145)                  
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x000000008000058a(2147485066)                  0x000000008000058a(2147485066)                  
t5(x30)             0x000000008017f806(2149054470)                  0x000000008017f806(2149054470)                  
t6(x31)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       

STATE               REF                                             DUT                                             DIFF
xmemhash            449067a98b4443be1073bb6905977490c841fe87        449067a98b4443be1073bb6905977490c841fe87        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000778(2147485560)                  0x0000000080000778(2147485560)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000022(34)                          0x0000000000000022(34)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x41e0000031e00000(2147484047.0_d)              0x41e0000031e00000(2147484047.0_d)              
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f5                  0x7fffffff7fc00000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff4efffffa(2147482880.0_s)              0xffffffff4efffffa(2147482880.0_s)              
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffffcb8d4000(-18513920.0_s)               0xffffffffcb8d4000(-18513920.0_s)               
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x41d72ef9cc000000(1555818288.0_d)              0x41d72ef9cc000000(1555818288.0_d)              
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f23                 0x000000008027fe5a(1.0622928504e-314_d)         0x000000008027fe5a(1.0622928504e-314_d)         
f24                 0x7ffffffffffffe00(nan_d)                       0x7ffffffffffffe00(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffffcefffffe(-2147483392.0_s)             0xffffffffcefffffe(-2147483392.0_s)             
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0xffffffffd2000ed3(-137501130752.0_s)           0xffffffffd2000ed3(-137501130752.0_s)           
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

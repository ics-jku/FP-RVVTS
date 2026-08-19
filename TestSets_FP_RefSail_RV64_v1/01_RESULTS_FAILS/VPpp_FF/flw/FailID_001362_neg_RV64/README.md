# FailID_001362 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1362
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x1b,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x04,0x43,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x30,0x40
_reg_f14:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0xc1
_reg_f15:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0xff,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0xfa,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0x41
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x21
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x3be8b000            // sp
    li x3, 0x80000758            // gp
    li x4, 0x6000                // tp
    li x5, 0x8018634a            // t0
    li x6, 0x11524770            // t1
    li x7, 0x8018063d            // t2
    li x8, 0x0                   // fp
    li x9, 0x801ff7e5            // s1
    li x10, 0xfaac2734           // a0
    li x11, 0x1                  // a1
    li x12, 0x0                  // a2
    li x13, 0x10                 // a3
    li x14, 0x8017ff55           // a4
    li x15, 0x6000               // a5
    li x16, 0x0                  // a6
    li x17, 0x0                  // a7
    li x18, 0x8000018d           // s2
    li x19, 0x80180019           // s3
    li x20, 0x42                 // s4
    li x21, 0x0                  // s5
    li x22, 0x80180990           // s6
    li x23, 0x80005d62           // s7
    li x24, 0x18                 // s8
    li x25, 0x80000532           // s9
    li x26, 0x80000532           // s10
    li x27, 0xffffffff83f08000   // s11
    li x28, 0x1                  // t3
    li x29, 0x8020050c           // t4
    li x30, 0x6000               // t5
    li x31, 0x47                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x11'}, 'clob': {'f23', 'x17', 'x11'}})
    
    li x17, 0x1ffffc
    and x11, x11, x17
    li x17, 0x800007f5
    add x11, x11, x17
    flw f23, -0x7f5(x11)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f23                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f23, -0x7f5(x11)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f23                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f23, x7, f5, x11
t2(x7)              0x000000008018063d(2149058109)                  0x000000008018063d(2149058109)
a1(x11)             0x00000000800007f5(2147485685)                  0x00000000800007f5(2147485685)
f5                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)
f23                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x000000003be8b000(1005105152)                  0x000000003be8b000(1005105152)                  
gp(x3)              0x0000000080000758(2147485528)                  0x0000000080000758(2147485528)                  
tp(x4)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t0(x5)              0x000000008018634a(2149081930)                  0x000000008018634a(2149081930)                  
t1(x6)              0x0000000011524770(290604912)                   0x0000000011524770(290604912)                   
t2(x7)              0x000000008018063d(2149058109)                  0x000000008018063d(2149058109)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x00000000801ff7e5(2149578725)                  0x00000000801ff7e5(2149578725)                  
a0(x10)             0x00000000faac2734(4205586228)                  0x00000000faac2734(4205586228)                  
a1(x11)             0x00000000800007f5(2147485685)                  0x00000000800007f5(2147485685)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x0000000000000010(16)                          0x0000000000000010(16)                          
a4(x14)             0x000000008017ff55(2149056341)                  0x000000008017ff55(2149056341)                  
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x00000000800007f5(2147485685)                  0x00000000800007f5(2147485685)                  
s2(x18)             0x000000008000018d(2147484045)                  0x000000008000018d(2147484045)                  
s3(x19)             0x0000000080180019(2149056537)                  0x0000000080180019(2149056537)                  
s4(x20)             0x0000000000000042(66)                          0x0000000000000042(66)                          
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000080180990(2149058960)                  0x0000000080180990(2149058960)                  
s7(x23)             0x0000000080005d62(2147507554)                  0x0000000080005d62(2147507554)                  
s8(x24)             0x0000000000000018(24)                          0x0000000000000018(24)                          
s9(x25)             0x0000000080000532(2147484978)                  0x0000000080000532(2147484978)                  
s10(x26)            0x0000000080000532(2147484978)                  0x0000000080000532(2147484978)                  
s11(x27)            0xffffffff83f08000(18446744071628161024)        0xffffffff83f08000(18446744071628161024)        
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x000000008020050c(2149582092)                  0x000000008020050c(2149582092)                  
t5(x30)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t6(x31)             0x0000000000000047(71)                          0x0000000000000047(71)                          

STATE               REF                                             DUT                                             DIFF
xmemhash            d38cfd7d2d1f609fe9560f968a49776e419b2446        d38cfd7d2d1f609fe9560f968a49776e419b2446        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000720(2147485472)                  0x0000000080000720(2147485472)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000021(33)                          0x0000000000000021(33)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f5                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f6                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0x000000000000001b(1.33e-322_d)                 0x000000000000001b(1.33e-322_d)                 
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff43040000(132.0_s)                     0xffffffff43040000(132.0_s)                     
f13                 0x4030000000000000(16.0_d)                      0x4030000000000000(16.0_d)                      
f14                 0xc1e0030003200000(-2149056537.0_d)             0xc1e0030003200000(-2149056537.0_d)             
f15                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f16                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f20                 0xffffffff4effffff(2147483520.0_s)              0xffffffff4effffff(2147483520.0_s)              
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff4efffffa(2147482880.0_s)              0xffffffff4efffffa(2147482880.0_s)              
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x41e0030003200000(2149056537.0_d)              0x41e0030003200000(2149056537.0_d)              
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
STATES DIFFER: True
```

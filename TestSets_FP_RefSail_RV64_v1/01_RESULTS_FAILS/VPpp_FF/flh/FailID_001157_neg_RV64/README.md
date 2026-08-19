# FailID_001157 VP++ FF neg RV64 flh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1157
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0xf0,0xe1,0xd1,0xc1
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x82,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xfa,0xf4,0x27,0x80,0x00,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x80,0x49,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x83,0x03,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x5
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017fef8            // ra
    li x2, 0x8017fd80            // sp
    li x3, 0x8027fb2e            // gp
    li x4, 0x39                  // tp
    li x5, 0x800ffb17            // t0
    li x6, 0x8b                  // t1
    li x7, 0x80000056            // t2
    li x8, 0x80000052            // fp
    li x9, 0x801807f7            // s1
    li x10, 0x8018000f           // a0
    li x11, 0x80180400           // a1
    li x12, 0x6000               // a2
    li x13, 0x6000               // a3
    li x14, 0x8017fda8           // a4
    li x15, 0x801ffc8f           // a5
    li x16, 0x7ffff868           // a6
    li x17, 0x7ff8000000000000   // a7
    li x18, 0x0                  // s2
    li x19, 0x8017fc80           // s3
    li x20, 0x1                  // s4
    li x21, 0x8017ff6e           // s5
    li x22, 0x80180763           // s6
    li x23, 0x51b023340191f3     // s7
    li x24, 0x7ffffd86           // s8
    li x25, 0x6000               // s9
    li x26, 0x80184050           // s10
    li x27, 0x6000               // s11
    li x28, 0x80000345           // t3
    li x29, 0x801809d3           // t4
    li x30, 0x6e                 // t5
    li x31, 0x8007f1a6           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x14'}, 'clob': {'f0', 'x2', 'x14'}})
    
    li x2, 0x1ffffe
    and x14, x14, x2
    li x2, 0x7ffffb85
    add x14, x14, x2
    flh f0, 0x47b(x14)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f0                  0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flh f0, 0x47b(x14)
+========================================================================================================================+
Attributes:  fcsr ['overflow', 'inexact'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f0                  0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f0, x47, x14
a4(x14)             0x000000008017f92d(2149054765)                  0x000000008017f92d(2149054765)
f0                  0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fef8(2149056248)                  0x000000008017fef8(2149056248)                  
sp(x2)              0x000000007ffffb85(2147482501)                  0x000000007ffffb85(2147482501)                  
gp(x3)              0x000000008027fb2e(2150103854)                  0x000000008027fb2e(2150103854)                  
tp(x4)              0x0000000000000039(57)                          0x0000000000000039(57)                          
t0(x5)              0x00000000800ffb17(2148530967)                  0x00000000800ffb17(2148530967)                  
t1(x6)              0x000000000000008b(139)                         0x000000000000008b(139)                         
t2(x7)              0x0000000080000056(2147483734)                  0x0000000080000056(2147483734)                  
fp(x8)              0x0000000080000052(2147483730)                  0x0000000080000052(2147483730)                  
s1(x9)              0x00000000801807f7(2149058551)                  0x00000000801807f7(2149058551)                  
a0(x10)             0x000000008018000f(2149056527)                  0x000000008018000f(2149056527)                  
a1(x11)             0x0000000080180400(2149057536)                  0x0000000080180400(2149057536)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x000000008017f92d(2149054765)                  0x000000008017f92d(2149054765)                  
a5(x15)             0x00000000801ffc8f(2149579919)                  0x00000000801ffc8f(2149579919)                  
a6(x16)             0x000000007ffff868(2147481704)                  0x000000007ffff868(2147481704)                  
a7(x17)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000008017fc80(2149055616)                  0x000000008017fc80(2149055616)                  
s4(x20)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s5(x21)             0x000000008017ff6e(2149056366)                  0x000000008017ff6e(2149056366)                  
s6(x22)             0x0000000080180763(2149058403)                  0x0000000080180763(2149058403)                  
s7(x23)             0x0051b023340191f3(22993138356425203)           0x0051b023340191f3(22993138356425203)           
s8(x24)             0x000000007ffffd86(2147483014)                  0x000000007ffffd86(2147483014)                  
s9(x25)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s10(x26)            0x0000000080184050(2149072976)                  0x0000000080184050(2149072976)                  
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x0000000080000345(2147484485)                  0x0000000080000345(2147484485)                  
t4(x29)             0x00000000801809d3(2149059027)                  0x00000000801809d3(2149059027)                  
t5(x30)             0x000000000000006e(110)                         0x000000000000006e(110)                         
t6(x31)             0x000000008007f1a6(2148004262)                  0x000000008007f1a6(2148004262)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            4be2397aa96cfc15d5685f50355fd9d3302f9d91        4be2397aa96cfc15d5685f50355fd9d3302f9d91        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000077c(2147485564)                  0x000000008000077c(2147485564)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000005(5)                           0x0000000000000005(5)                           
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f3                  0xc1d1e1f000000000(-1200078848.0_d)             0xc1d1e1f000000000(-1200078848.0_d)             
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x0000000000000082(6.4e-322_d)                  0x0000000000000082(6.4e-322_d)                  
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x000000008027f4fa(1.0622916647e-314_d)         0x000000008027f4fa(1.0622916647e-314_d)         
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f24                 0x7fffffff42140000(nan_d)                       0x7fffffff42140000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff49800000(1048576.0_s)                 0xffffffff49800000(1048576.0_s)                 
f29                 0xffffffff80000383(-1.2597673194280105e-42_s)   0xffffffff80000383(-1.2597673194280105e-42_s)   
f30                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

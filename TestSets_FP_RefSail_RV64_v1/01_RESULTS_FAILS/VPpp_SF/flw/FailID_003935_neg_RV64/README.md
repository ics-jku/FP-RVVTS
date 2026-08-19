# FailID_003935 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3935
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
_reg_f0: .byte 0x00,0x00,0xc0,0x0f,0x00,0x03,0xe0,0x41
_reg_f1: .byte 0x00,0x00,0x80,0xf1,0xec,0xcf,0xea,0x41
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f4: .byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xf3,0xcf,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x20,0x9b,0x00,0x03,0xe0,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0xa0,0x77,0x4c,0x00,0x00,0x00,0x00
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x40,0xd2,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x01,0xfe,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x01,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0xf3,0xcf,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0xc0,0x9d,0xff,0xff,0xdf,0x41
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xc2
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8018001c            // ra
    li x2, 0x0                   // sp
    li x3, 0x801ffb45            // gp
    li x4, 0x8017fce2            // tp
    li x5, 0x0                   // t0
    li x6, 0x0                   // t1
    li x7, 0x801800df            // t2
    li x8, 0x0                   // fp
    li x9, 0x800005f5            // s1
    li x10, 0x8007f39a           // a0
    li x11, 0x8017f8f7           // a1
    li x12, 0x6000               // a2
    li x13, 0x80000562           // a3
    li x14, 0x6000               // a4
    li x15, 0xf824971c           // a5
    li x16, 0x8017fe95           // a6
    li x17, 0x0                  // a7
    li x18, 0x0                  // s2
    li x19, 0x801ffa20           // s3
    li x20, 0x80180120           // s4
    li x21, 0x800004f5           // s5
    li x22, 0xf9                 // s6
    li x23, 0x8017fd51           // s7
    li x24, 0x2                  // s8
    li x25, 0x80000057           // s9
    li x26, 0x80280178           // s10
    li x27, 0x1e8ee000           // s11
    li x28, 0x0                  // t3
    li x29, 0x801db402           // t4
    li x30, 0x66                 // t5
    li x31, 0x8018064e           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x2'}, 'clob': {'x6', 'f24', 'x2'}})
    
    li x6, 0x1ffffc
    and x2, x2, x6
    li x6, 0x800002b9
    add x2, x2, x6
    flw f24, -0x2b9(x2)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f24                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f24, -0x2b9(x2)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f24                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f24, x2, b9, x2
sp(x2)              0x00000000800002b9(2147484345)                  0x00000000800002b9(2147484345)
f24                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008018001c(2149056540)                  0x000000008018001c(2149056540)                  
sp(x2)              0x00000000800002b9(2147484345)                  0x00000000800002b9(2147484345)                  
gp(x3)              0x00000000801ffb45(2149579589)                  0x00000000801ffb45(2149579589)                  
tp(x4)              0x000000008017fce2(2149055714)                  0x000000008017fce2(2149055714)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x00000000800002b9(2147484345)                  0x00000000800002b9(2147484345)                  
t2(x7)              0x00000000801800df(2149056735)                  0x00000000801800df(2149056735)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x00000000800005f5(2147485173)                  0x00000000800005f5(2147485173)                  
a0(x10)             0x000000008007f39a(2148004762)                  0x000000008007f39a(2148004762)                  
a1(x11)             0x000000008017f8f7(2149054711)                  0x000000008017f8f7(2149054711)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x0000000080000562(2147485026)                  0x0000000080000562(2147485026)                  
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x00000000f824971c(4163147548)                  0x00000000f824971c(4163147548)                  
a6(x16)             0x000000008017fe95(2149056149)                  0x000000008017fe95(2149056149)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x00000000801ffa20(2149579296)                  0x00000000801ffa20(2149579296)                  
s4(x20)             0x0000000080180120(2149056800)                  0x0000000080180120(2149056800)                  
s5(x21)             0x00000000800004f5(2147484917)                  0x00000000800004f5(2147484917)                  
s6(x22)             0x00000000000000f9(249)                         0x00000000000000f9(249)                         
s7(x23)             0x000000008017fd51(2149055825)                  0x000000008017fd51(2149055825)                  
s8(x24)             0x0000000000000002(2)                           0x0000000000000002(2)                           
s9(x25)             0x0000000080000057(2147483735)                  0x0000000080000057(2147483735)                  
s10(x26)            0x0000000080280178(2150105464)                  0x0000000080280178(2150105464)                  
s11(x27)            0x000000001e8ee000(512679936)                   0x000000001e8ee000(512679936)                   
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x00000000801db402(2149430274)                  0x00000000801db402(2149430274)                  
t5(x30)             0x0000000000000066(102)                         0x0000000000000066(102)                         
t6(x31)             0x000000008018064e(2149058126)                  0x000000008018064e(2149058126)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            c96b505082f765961288123160a15e3eedb7aacc        c96b505082f765961288123160a15e3eedb7aacc        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000754(2147485524)                  0x0000000080000754(2147485524)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000c2(194)                         0x00000000000000c2(194)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x41e003000fc00000(2149056638.0_d)              0x41e003000fc00000(2149056638.0_d)              
f1                  0x41eacfecf1800000(3598673804.0_d)              0x41eacfecf1800000(3598673804.0_d)              
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f4                  0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f8                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f9                  0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffffceffcff3(-2145909120.0_s)             0xffffffffceffcff3(-2145909120.0_s)             
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41e003009b200000(2149057753.0_d)              0x41e003009b200000(2149057753.0_d)              
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x000000004c77a000(6.338408486e-315_d)          0x000000004c77a000(6.338408486e-315_d)          
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffffd2400000(-206158430208.0_s)           0xffffffffd2400000(-206158430208.0_s)           
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff7ffffe01(nan_s)                       0xffffffff7ffffe01(nan_s)                       
f22                 0xffffffff4f001801(2149056768.0_s)              0xffffffff4f001801(2149056768.0_s)              
f23                 0xffffffffceffcff3(-2145909120.0_s)             0xffffffffceffcff3(-2145909120.0_s)             
f24                 0x7ff8000000000000(nan_d)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x41dfffff9dc00000(2147483255.0_d)              0x41dfffff9dc00000(2147483255.0_d)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

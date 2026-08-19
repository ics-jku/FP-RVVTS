# FailID_005069 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 5069
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x37,0xdd,0x64,0x28,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x07,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0xd7,0xdd,0x7c,0x96,0xf4,0x9b,0x21,0xc6
_reg_f10:.byte 0x07,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x48,0x40
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f15:.byte 0x49,0x2c,0x32,0x33,0x61,0x83,0x13,0x28
_reg_f16:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f17:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x39,0xfe,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x39,0xfe,0x17,0x80,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x30
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x8017fb5f            // sp
    li x3, 0x1d11b427            // gp
    li x4, 0x8017f937            // tp
    li x5, 0x80180764            // t0
    li x6, 0x801807e9            // t1
    li x7, 0x7ffffdfd            // t2
    li x8, 0x801806ea            // fp
    li x9, 0x0                   // s1
    li x10, 0xa3                 // a0
    li x11, 0x801803af           // a1
    li x12, 0x7ffffe65           // a2
    li x13, 0x8017ff9f           // a3
    li x14, 0x80180cbd           // a4
    li x15, 0x271b423            // a5
    li x16, 0x801802e7           // a6
    li x17, 0x8017feb7           // a7
    li x18, 0x91f3               // s2
    li x19, 0x80180622           // s3
    li x20, 0xffffffff7fe8064e   // s4
    li x21, 0x7ffff98c           // s5
    li x22, 0x7fffff61           // s6
    li x23, 0xffffffff7fe80273   // s7
    li x24, 0x6000               // s8
    li x25, 0x8027f21a           // s9
    li x26, 0x8017fb18           // s10
    li x27, 0x6000               // s11
    li x28, 0x801801f3           // t3
    li x29, 0x8027fde7           // t4
    li x30, 0x8017f808           // t5
    li x31, 0x802400f3           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x21', 'fcsr.rm', 'f9'}, 'clob': {'x21', 'x24'}})
    
    li x24, 0xffffc
    and x21, x21, x24
    li x24, 0x80180108
    add x21, x21, x24
    fsw f9, -0x108(x21)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        795d415902d914cdbbfbc9aac84b4942bb0ccdea        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f9, -0x108(x21)
+========================================================================================================================+
Attributes:  fcsr ['invalid']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        795d415902d914cdbbfbc9aac84b4942bb0ccdea        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x108, x21
s5(x21)             0x000000008027fa94(2150103700)                  0x000000008027fa94(2150103700)
f9                  0xc6219bf4967cddd7(-6.97572313911571e+29_d)     0xc6219bf4967cddd7(-6.97572313911571e+29_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x000000008017fb5f(2149055327)                  0x000000008017fb5f(2149055327)                  
gp(x3)              0x000000001d11b427(487699495)                   0x000000001d11b427(487699495)                   
tp(x4)              0x000000008017f937(2149054775)                  0x000000008017f937(2149054775)                  
t0(x5)              0x0000000080180764(2149058404)                  0x0000000080180764(2149058404)                  
t1(x6)              0x00000000801807e9(2149058537)                  0x00000000801807e9(2149058537)                  
t2(x7)              0x000000007ffffdfd(2147483133)                  0x000000007ffffdfd(2147483133)                  
fp(x8)              0x00000000801806ea(2149058282)                  0x00000000801806ea(2149058282)                  
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x00000000000000a3(163)                         0x00000000000000a3(163)                         
a1(x11)             0x00000000801803af(2149057455)                  0x00000000801803af(2149057455)                  
a2(x12)             0x000000007ffffe65(2147483237)                  0x000000007ffffe65(2147483237)                  
a3(x13)             0x000000008017ff9f(2149056415)                  0x000000008017ff9f(2149056415)                  
a4(x14)             0x0000000080180cbd(2149059773)                  0x0000000080180cbd(2149059773)                  
a5(x15)             0x000000000271b423(41006115)                    0x000000000271b423(41006115)                    
a6(x16)             0x00000000801802e7(2149057255)                  0x00000000801802e7(2149057255)                  
a7(x17)             0x000000008017feb7(2149056183)                  0x000000008017feb7(2149056183)                  
s2(x18)             0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
s3(x19)             0x0000000080180622(2149058082)                  0x0000000080180622(2149058082)                  
s4(x20)             0xffffffff7fe8064e(18446744071560496718)        0xffffffff7fe8064e(18446744071560496718)        
s5(x21)             0x000000008027fa94(2150103700)                  0x000000008027fa94(2150103700)                  
s6(x22)             0x000000007fffff61(2147483489)                  0x000000007fffff61(2147483489)                  
s7(x23)             0xffffffff7fe80273(18446744071560495731)        0xffffffff7fe80273(18446744071560495731)        
s8(x24)             0x0000000080180108(2149056776)                  0x0000000080180108(2149056776)                  
s9(x25)             0x000000008027f21a(2150101530)                  0x000000008027f21a(2150101530)                  
s10(x26)            0x000000008017fb18(2149055256)                  0x000000008017fb18(2149055256)                  
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x00000000801801f3(2149057011)                  0x00000000801801f3(2149057011)                  
t4(x29)             0x000000008027fde7(2150104551)                  0x000000008027fde7(2150104551)                  
t5(x30)             0x000000008017f808(2149054472)                  0x000000008017f808(2149054472)                  
t6(x31)             0x00000000802400f3(2149843187)                  0x00000000802400f3(2149843187)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            08513040b8afe9199bf7370d6244d834b04986c6        08513040b8afe9199bf7370d6244d834b04986c6        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        795d415902d914cdbbfbc9aac84b4942bb0ccdea        X
lastPC              0x0000000080000798(2147485592)                  0x0000000080000798(2147485592)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000030(48)                          0x0000000000000030(48)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff2864dd37(1.2704510803562743e-14_s)    0xffffffff2864dd37(1.2704510803562743e-14_s)    
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff4f000007(2147485440.0_s)              0xffffffff4f000007(2147485440.0_s)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0xc6219bf4967cddd7(-6.97572313911571e+29_d)     0xc6219bf4967cddd7(-6.97572313911571e+29_d)     
f10                 0xffffffff4f000007(2147485440.0_s)              0xffffffff4f000007(2147485440.0_s)              
f11                 0x4048000000000000(48.0_d)                      0x4048000000000000(48.0_d)                      
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f15                 0x2813836133322c49(1.238084287307389e-115_d)    0x2813836133322c49(1.238084287307389e-115_d)    
f16                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f17                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f25                 0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f28                 0x7fffffff4f000001(nan_d)                       0x7fffffff4f000001(nan_d)                       
f29                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f30                 0xffffffff8017fe39(-2.2034143169905213e-39_s)   0xffffffff8017fe39(-2.2034143169905213e-39_s)   
f31                 0xffffffff8017fe39(-2.2034143169905213e-39_s)   0xffffffff8017fe39(-2.2034143169905213e-39_s)   
STATES DIFFER: True
```

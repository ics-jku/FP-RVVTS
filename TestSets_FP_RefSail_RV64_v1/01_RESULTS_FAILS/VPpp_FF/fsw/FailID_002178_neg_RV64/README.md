# FailID_002178 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2178
* Isolated failing instruction: `fsw`
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f3: .byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f11:.byte 0x00,0x80,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0xf9,0xff,0x7f,0x4f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xa9,0xc1
_reg_f17:.byte 0x00,0x00,0xe0,0x66,0x00,0x00,0xe0,0x41
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0x80,0x6c,0x07,0xf6,0xdf,0xc1
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x90
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x1fffff3             // ra
    li x2, 0xffffffff003fffff    // sp
    li x3, 0x801804c0            // gp
    li x4, 0x801801a8            // tp
    li x5, 0x0                   // t0
    li x6, 0x80000b76            // t1
    li x7, 0x5f34                // t2
    li x8, 0x0                   // fp
    li x9, 0x80180751            // s1
    li x10, 0x80000366           // a0
    li x11, 0x80180000           // a1
    li x12, 0x7ffffc80           // a2
    li x13, 0x6000               // a3
    li x14, 0x801865ff           // a4
    li x15, 0x7ffff8c9           // a5
    li x16, 0x7ffffead           // a6
    li x17, 0xfffffffffffff97a   // a7
    li x18, 0xffffffff90749000   // s2
    li x19, 0x7ffffcfa           // s3
    li x20, 0x0                  // s4
    li x21, 0x801ffc6a           // s5
    li x22, 0x80180329           // s6
    li x23, 0x6000               // s7
    li x24, 0x19e83000           // s8
    li x25, 0xffffffff803ffa56   // s9
    li x26, 0x0                  // s10
    li x27, 0x7ffffc6b           // s11
    li x28, 0x6000               // t3
    li x29, 0x800003b6           // t4
    li x30, 0x6000               // t5
    li x31, 0x7ffffdeb           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f11', 'mstatus.fs/vs.fs', 'x6'}, 'clob': {'x6', 'x31'}})
    
    li x31, 0xffffc
    and x6, x6, x31
    li x31, 0x801806ac
    add x6, x6, x31
    fsw f11, -0x6ac(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        a6170ca26eac30bb2d95a6972cccf96400d7c975        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f11, -0x6ac(x6)
+========================================================================================================================+
Attributes:  fcsr ['invalid']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        a6170ca26eac30bb2d95a6972cccf96400d7c975        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f11, x6, x6
t1(x6)              0x0000000080181220(2149061152)                  0x0000000080181220(2149061152)
f11                 0xffffffff4eff8000(2143289344.0_s)              0xffffffff4eff8000(2143289344.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000001fffff3(33554419)                    0x0000000001fffff3(33554419)                    
sp(x2)              0xffffffff003fffff(18446744069418778623)        0xffffffff003fffff(18446744069418778623)        
gp(x3)              0x00000000801804c0(2149057728)                  0x00000000801804c0(2149057728)                  
tp(x4)              0x00000000801801a8(2149056936)                  0x00000000801801a8(2149056936)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x0000000080181220(2149061152)                  0x0000000080181220(2149061152)                  
t2(x7)              0x0000000000005f34(24372)                       0x0000000000005f34(24372)                       
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x0000000080180751(2149058385)                  0x0000000080180751(2149058385)                  
a0(x10)             0x0000000080000366(2147484518)                  0x0000000080000366(2147484518)                  
a1(x11)             0x0000000080180000(2149056512)                  0x0000000080180000(2149056512)                  
a2(x12)             0x000000007ffffc80(2147482752)                  0x000000007ffffc80(2147482752)                  
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x00000000801865ff(2149082623)                  0x00000000801865ff(2149082623)                  
a5(x15)             0x000000007ffff8c9(2147481801)                  0x000000007ffff8c9(2147481801)                  
a6(x16)             0x000000007ffffead(2147483309)                  0x000000007ffffead(2147483309)                  
a7(x17)             0xfffffffffffff97a(18446744073709549946)        0xfffffffffffff97a(18446744073709549946)        
s2(x18)             0xffffffff90749000(18446744071838142464)        0xffffffff90749000(18446744071838142464)        
s3(x19)             0x000000007ffffcfa(2147482874)                  0x000000007ffffcfa(2147482874)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x00000000801ffc6a(2149579882)                  0x00000000801ffc6a(2149579882)                  
s6(x22)             0x0000000080180329(2149057321)                  0x0000000080180329(2149057321)                  
s7(x23)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s8(x24)             0x0000000019e83000(434647040)                   0x0000000019e83000(434647040)                   
s9(x25)             0xffffffff803ffa56(18446744071566260822)        0xffffffff803ffa56(18446744071566260822)        
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000007ffffc6b(2147482731)                  0x000000007ffffc6b(2147482731)                  
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x00000000800003b6(2147484598)                  0x00000000800003b6(2147484598)                  
t5(x30)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t6(x31)             0x00000000801806ac(2149058220)                  0x00000000801806ac(2149058220)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            36b32d08a467b2e0cef2ce32189de5a39baad744        36b32d08a467b2e0cef2ce32189de5a39baad744        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        a6170ca26eac30bb2d95a6972cccf96400d7c975        X
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000090(144)                         0x0000000000000090(144)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f3                  0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f11                 0xffffffff4eff8000(2143289344.0_s)              0xffffffff4eff8000(2143289344.0_s)              
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff4f7ffff9(4294965504.0_s)              0xffffffff4f7ffff9(4294965504.0_s)              
f16                 0xc1a9000000000000(-209715200.0_d)              0xc1a9000000000000(-209715200.0_d)              
f17                 0x41e0000066e00000(2147484471.0_d)              0x41e0000066e00000(2147484471.0_d)              
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f27                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0xc1dff6076c800000(-2144869810.0_d)             0xc1dff6076c800000(-2144869810.0_d)             
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

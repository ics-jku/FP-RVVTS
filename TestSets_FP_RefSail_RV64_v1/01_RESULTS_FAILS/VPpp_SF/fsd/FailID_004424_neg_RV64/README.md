# FailID_004424 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4424
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
_reg_f0: .byte 0x93,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x40,0xdd,0xff,0x02,0xe0,0xc1
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x40,0xdd,0xff,0x02,0xe0,0x41
_reg_f6: .byte 0x00,0x00,0x00,0x30,0x4a,0xe0,0xd2,0xc1
_reg_f7: .byte 0x8f,0xcd,0x49,0x80,0x8b,0xc8,0xe4,0x40
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x45,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x7c,0x3b,0xef,0x41
_reg_f16:.byte 0x00,0x00,0x40,0xb3,0xfe,0xff,0xdf,0x41
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0xd7,0x9f,0x73,0x00,0x00,0x00,0x00
_reg_f19:.byte 0x00,0x00,0x40,0xb3,0xfe,0xff,0xdf,0x41
_reg_f20:.byte 0xcb,0x2a,0xde,0x54,0x05,0x8d,0x02,0x42
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x6b,0xff,0xe0,0x15,0x47,0xf0,0x0b,0xc5
_reg_f26:.byte 0x00,0x00,0xc0,0x5c,0x00,0x03,0xe0,0xc1
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x11
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x247b470c            // ra
    li x2, 0x8017feea            // sp
    li x3, 0x801fdbc2            // gp
    li x4, 0x0                   // tp
    li x5, 0xffffffffe7cad000    // t0
    li x6, 0xff                  // t1
    li x7, 0x80000436            // t2
    li x8, 0x8020087e            // fp
    li x9, 0x1                   // s1
    li x10, 0x0                  // a0
    li x11, 0x80185b91           // a1
    li x12, 0x452da708           // a2
    li x13, 0x801801aa           // a3
    li x14, 0x80000304           // a4
    li x15, 0x800006d2           // a5
    li x16, 0x6000               // a6
    li x17, 0x0                  // a7
    li x18, 0x801807bb           // s2
    li x19, 0x801ff81d           // s3
    li x20, 0x0                  // s4
    li x21, 0x7ff8000000000000   // s5
    li x22, 0x200                // s6
    li x23, 0x80180153           // s7
    li x24, 0x247b4284           // s8
    li x25, 0x7fc00000           // s9
    li x26, 0xff                 // s10
    li x27, 0x200                // s11
    li x28, 0x1                  // t3
    li x29, 0xffffffffffffffff   // t4
    li x30, 0x1                  // t5
    li x31, 0x802806a3           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f29', 'x15'}, 'clob': {'x27', 'x15'}})
    
    li x27, 0xffff8
    and x15, x15, x27
    li x27, 0x8017fa7b
    add x15, x15, x27
    fsd f29, 0x585(x15)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        73fb6b98d4651caf62dc896f780bc9916a7e4069        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f29, 0x585(x15)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        73fb6b98d4651caf62dc896f780bc9916a7e4069        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f29, x585, x15
a5(x15)             0x000000008018014b(2149056843)                  0x000000008018014b(2149056843)
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000247b470c(612058892)                   0x00000000247b470c(612058892)                   
sp(x2)              0x000000008017feea(2149056234)                  0x000000008017feea(2149056234)                  
gp(x3)              0x00000000801fdbc2(2149571522)                  0x00000000801fdbc2(2149571522)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0xffffffffe7cad000(18446744073303412736)        0xffffffffe7cad000(18446744073303412736)        
t1(x6)              0x00000000000000ff(255)                         0x00000000000000ff(255)                         
t2(x7)              0x0000000080000436(2147484726)                  0x0000000080000436(2147484726)                  
fp(x8)              0x000000008020087e(2149582974)                  0x000000008020087e(2149582974)                  
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x0000000080185b91(2149079953)                  0x0000000080185b91(2149079953)                  
a2(x12)             0x00000000452da708(1160619784)                  0x00000000452da708(1160619784)                  
a3(x13)             0x00000000801801aa(2149056938)                  0x00000000801801aa(2149056938)                  
a4(x14)             0x0000000080000304(2147484420)                  0x0000000080000304(2147484420)                  
a5(x15)             0x000000008018014b(2149056843)                  0x000000008018014b(2149056843)                  
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x00000000801807bb(2149058491)                  0x00000000801807bb(2149058491)                  
s3(x19)             0x00000000801ff81d(2149578781)                  0x00000000801ff81d(2149578781)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
s6(x22)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s7(x23)             0x0000000080180153(2149056851)                  0x0000000080180153(2149056851)                  
s8(x24)             0x00000000247b4284(612057732)                   0x00000000247b4284(612057732)                   
s9(x25)             0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
s10(x26)            0x00000000000000ff(255)                         0x00000000000000ff(255)                         
s11(x27)            0x000000008017fa7b(2149055099)                  0x000000008017fa7b(2149055099)                  
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t5(x30)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t6(x31)             0x00000000802806a3(2150106787)                  0x00000000802806a3(2150106787)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            941fe0a37d4c50542ea1d888a8d8b0d22b0e68a3        941fe0a37d4c50542ea1d888a8d8b0d22b0e68a3        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        73fb6b98d4651caf62dc896f780bc9916a7e4069        X
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000011(17)                          0x0000000000000011(17)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000293(9.234556879900544e-43_s)     0xffffffff00000293(9.234556879900544e-43_s)     
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xc1e002ffdd400000(-2149056234.0_d)             0xc1e002ffdd400000(-2149056234.0_d)             
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x41e002ffdd400000(2149056234.0_d)              0x41e002ffdd400000(2149056234.0_d)              
f6                  0xc1d2e04a30000000(-1266755776.0_d)             0xc1d2e04a30000000(-1266755776.0_d)             
f7                  0x40e4c88b8049cd8f(42564.359410191995_d)        0x40e4c88b8049cd8f(42564.359410191995_d)        
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0xffffffff45000000(2048.0_s)                    0xffffffff45000000(2048.0_s)                    
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x41ef3b7c00000000(4191936512.0_d)              0x41ef3b7c00000000(4191936512.0_d)              
f16                 0x41dffffeb3400000(2147482317.0_d)              0x41dffffeb3400000(2147482317.0_d)              
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x00000000739fd700(9.58415765e-315_d)           0x00000000739fd700(9.58415765e-315_d)           
f19                 0x41dffffeb3400000(2147482317.0_d)              0x41dffffeb3400000(2147482317.0_d)              
f20                 0x42028d0554de2acb(9959418523.770895_d)         0x42028d0554de2acb(9959418523.770895_d)         
f21                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xc50bf04715e0ff6b(-4.221959547606705e+24_d)    0xc50bf04715e0ff6b(-4.221959547606705e+24_d)    
f26                 0xc1e003005cc00000(-2149057254.0_d)             0xc1e003005cc00000(-2149057254.0_d)             
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

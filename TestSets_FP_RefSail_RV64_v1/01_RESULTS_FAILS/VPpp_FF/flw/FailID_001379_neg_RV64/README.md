# FailID_001379 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1379
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
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xe0,0xb5,0xff,0x02,0xe0,0x41
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x09,0xc0,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xe0,0x9d,0xfe,0x04,0xe0,0x41
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xa9,0xcf,0x62,0x49,0x57,0xe7,0xda,0x97
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x90,0x0d,0x95,0x9b,0x78,0xd2,0xcd,0xed
_reg_f15:.byte 0xa3,0x21,0xca,0x65,0x8e,0x35,0x7b,0x4e
_reg_f16:.byte 0x00,0x00,0x80,0x5f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0xee,0x00,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0x80,0x40,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x50,0x40
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xe0,0xb5,0xff,0x02,0xe0,0xc1
_reg_f30:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x48,0xff,0xff,0xff,0xff
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
    li x1, 0x7227a000            // ra
    li x2, 0x80180656            // sp
    li x3, 0x8018063c            // gp
    li x4, 0x80100410            // tp
    li x5, 0x6000                // t0
    li x6, 0x0                   // t1
    li x7, 0x7ffffd0b            // t2
    li x8, 0x80000220            // fp
    li x9, 0x1                   // s1
    li x10, 0x7fffff5e           // a0
    li x11, 0x1                  // a1
    li x12, 0x8018067f           // a2
    li x13, 0x8017fc07           // a3
    li x14, 0x801800ee           // a4
    li x15, 0x80180583           // a5
    li x16, 0x8020078d           // a6
    li x17, 0x0                  // a7
    li x18, 0xbd                 // s2
    li x19, 0x1                  // s3
    li x20, 0x13082730           // s4
    li x21, 0x80000220           // s5
    li x22, 0x3d                 // s6
    li x23, 0x8017feb4           // s7
    li x24, 0x8017fd83           // s8
    li x25, 0x8018051b           // s9
    li x26, 0xd00647c            // s10
    li x27, 0x6000               // s11
    li x28, 0x80205e0b           // t3
    li x29, 0x6000               // t4
    li x30, 0x0                  // t5
    li x31, 0x8017fc07           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x25'}, 'clob': {'f12', 'x24', 'x25'}})
    
    li x24, 0x1ffffc
    and x25, x25, x24
    li x24, 0x800005a0
    add x25, x25, x24
    flw f12, -0x5a0(x25)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f12                 0x97dae7574962cfa9(-9.213707466843409e-194_d)   0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f12, -0x5a0(x25)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f12                 0x97dae7574962cfa9(-9.213707466843409e-194_d)   0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f12, x5, a0, x25
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)
s9(x25)             0x0000000080180ab8(2149059256)                  0x0000000080180ab8(2149059256)
f12                 0x97dae7574962cfa9(-9.213707466843409e-194_d)   0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007227a000(1915199488)                  0x000000007227a000(1915199488)                  
sp(x2)              0x0000000080180656(2149058134)                  0x0000000080180656(2149058134)                  
gp(x3)              0x000000008018063c(2149058108)                  0x000000008018063c(2149058108)                  
tp(x4)              0x0000000080100410(2148533264)                  0x0000000080100410(2148533264)                  
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x000000007ffffd0b(2147482891)                  0x000000007ffffd0b(2147482891)                  
fp(x8)              0x0000000080000220(2147484192)                  0x0000000080000220(2147484192)                  
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x000000007fffff5e(2147483486)                  0x000000007fffff5e(2147483486)                  
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x000000008018067f(2149058175)                  0x000000008018067f(2149058175)                  
a3(x13)             0x000000008017fc07(2149055495)                  0x000000008017fc07(2149055495)                  
a4(x14)             0x00000000801800ee(2149056750)                  0x00000000801800ee(2149056750)                  
a5(x15)             0x0000000080180583(2149057923)                  0x0000000080180583(2149057923)                  
a6(x16)             0x000000008020078d(2149582733)                  0x000000008020078d(2149582733)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x00000000000000bd(189)                         0x00000000000000bd(189)                         
s3(x19)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s4(x20)             0x0000000013082730(319301424)                   0x0000000013082730(319301424)                   
s5(x21)             0x0000000080000220(2147484192)                  0x0000000080000220(2147484192)                  
s6(x22)             0x000000000000003d(61)                          0x000000000000003d(61)                          
s7(x23)             0x000000008017feb4(2149056180)                  0x000000008017feb4(2149056180)                  
s8(x24)             0x00000000800005a0(2147485088)                  0x00000000800005a0(2147485088)                  
s9(x25)             0x0000000080180ab8(2149059256)                  0x0000000080180ab8(2149059256)                  
s10(x26)            0x000000000d00647c(218129532)                   0x000000000d00647c(218129532)                   
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x0000000080205e0b(2149604875)                  0x0000000080205e0b(2149604875)                  
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x000000008017fc07(2149055495)                  0x000000008017fc07(2149055495)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            591ff061fb58d8a3d2324578b8ba8e7151647116        591ff061fb58d8a3d2324578b8ba8e7151647116        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000074c(2147485516)                  0x000000008000074c(2147485516)                  
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
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x41e002ffb5e00000(2149055919.0_d)              0x41e002ffb5e00000(2149055919.0_d)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffffceffc009(-2145387648.0_s)             0xffffffffceffc009(-2145387648.0_s)             
f8                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x41e004fe9de00000(2150102255.0_d)              0x41e004fe9de00000(2150102255.0_d)              
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x97dae7574962cfa9(-9.213707466843409e-194_d)   0xffffffff00000000(0.0_s)                       X
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xedcdd2789b950d90(-8.421817586531674e+220_d)   0xedcdd2789b950d90(-8.421817586531674e+220_d)   
f15                 0x4e7b358e65ca21a3(1.173693904724524e+70_d)     0x4e7b358e65ca21a3(1.173693904724524e+70_d)     
f16                 0xffffffff5f800000(1.8446744073709552e+19_s)    0xffffffff5f800000(1.8446744073709552e+19_s)    
f17                 0x00000000801800ee(1.061775111e-314_d)          0x00000000801800ee(1.061775111e-314_d)          
f18                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffff40800000(4.0_s)                       0xffffffff40800000(4.0_s)                       
f24                 0x4050000000000000(64.0_d)                      0x4050000000000000(64.0_d)                      
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xc1e002ffb5e00000(-2149055919.0_d)             0xc1e002ffb5e00000(-2149055919.0_d)             
f30                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f31                 0xffffffff48000000(131072.0_s)                  0xffffffff48000000(131072.0_s)                  
STATES DIFFER: True
```

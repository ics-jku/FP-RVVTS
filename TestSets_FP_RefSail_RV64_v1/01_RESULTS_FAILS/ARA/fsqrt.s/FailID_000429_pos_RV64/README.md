# FailID_000429 ARA pos RV64 fsqrt.s

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 429
* Isolated failing instruction: `fsqrt.s`
* Minimized failing test case: [cblock_minimized_test_case.json](cblock_minimized_test_case.json)
* Resulting REF machine state: [mstate_RefSail.json](mstate_RefSail.json)
* Resulting DUT machine state: [mstate_DUT_ARA.json](mstate_DUT_ARA.json)
* Automated failure characterization report: [AFC_FP_report.log](AFC_FP_report.log)

## Report

### Minimized Failing Test Case
```
    // FLOATINGPOINT STATE DATA
    j _float_data_end
    .align 4
_reg_f0: .byte 0x00,0x40,0xd8,0x95,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x08,0xd0,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x40,0xd8,0x15,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x40,0xd8,0xb5,0x41
_reg_f8: .byte 0x00,0x00,0x00,0xfd,0xff,0xff,0xdf,0x41
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x81,0x5f,0xa6,0x2a,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x40,0xd8,0x95,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x0e,0xfe,0xff,0x7f,0x00,0x00,0x00,0x00
_reg_f25:.byte 0xfc,0x27,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x5f,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x07,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x41
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x15d84000            // ra
    li x2, 0x8019bed1            // sp
    li x3, 0x0                   // gp
    li x4, 0x8017fa7c            // tp
    li x5, 0x0                   // t0
    li x6, 0x6000                // t1
    li x7, 0xd419758             // t2
    li x8, 0x6e609000            // fp
    li x9, 0xffffffffffffffee    // s1
    li x10, 0x10017fe79          // a0
    li x11, 0x801806af           // a1
    li x12, 0x801d80f0           // a2
    li x13, 0x0                  // a3
    li x14, 0x8017fc5a           // a4
    li x15, 0x8017fe7c           // a5
    li x16, 0x7fffffd3           // a6
    li x17, 0x80000696           // a7
    li x18, 0x7ffffff4           // s2
    li x19, 0x8017fca3           // s3
    li x20, 0x80180271           // s4
    li x21, 0x80000187           // s5
    li x22, 0x1                  // s6
    li x23, 0x80000837           // s7
    li x24, 0x8017fc5a           // s8
    li x25, 0x8017fe7c           // s9
    li x26, 0x0                  // s10
    li x27, 0x7ffffc2d           // s11
    li x28, 0x8017fc0e           // t3
    li x29, 0x8017fa7c           // t4
    li x30, 0x200                // t5
    li x31, 0x71b823             // t6
    // INSTRUCTION ({'dep': {'f30', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'f26'}})
    fsqrt.s f26, f30, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f26                 0xffffffff473515ef(46357.93359375_s)            0xffffffff473515f0(46357.9375_s)                X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.s f26, f30, dyn
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f26                 0xffffffff473515ef(46357.93359375_s)            0xffffffff473515f0(46357.9375_s)                X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f26, f30
f26                 0xffffffff473515ef(46357.93359375_s)            0xffffffff473515f0(46357.9375_s)                X
f30                 0xffffffff4f001807(2149058304.0_s)              0xffffffff4f001807(2149058304.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000015d84000(366493696)                   0x0000000015d84000(366493696)                   
sp(x2)              0x000000008019bed1(2149170897)                  0x000000008019bed1(2149170897)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x000000008017fa7c(2149055100)                  0x000000008017fa7c(2149055100)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t2(x7)              0x000000000d419758(222402392)                   0x000000000d419758(222402392)                   
fp(x8)              0x000000006e609000(1851822080)                  0x000000006e609000(1851822080)                  
s1(x9)              0xffffffffffffffee(18446744073709551598)        0xffffffffffffffee(18446744073709551598)        
a0(x10)             0x000000010017fe79(4296539769)                  0x000000010017fe79(4296539769)                  
a1(x11)             0x00000000801806af(2149058223)                  0x00000000801806af(2149058223)                  
a2(x12)             0x00000000801d80f0(2149417200)                  0x00000000801d80f0(2149417200)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x000000008017fc5a(2149055578)                  0x000000008017fc5a(2149055578)                  
a5(x15)             0x000000008017fe7c(2149056124)                  0x000000008017fe7c(2149056124)                  
a6(x16)             0x000000007fffffd3(2147483603)                  0x000000007fffffd3(2147483603)                  
a7(x17)             0x0000000080000696(2147485334)                  0x0000000080000696(2147485334)                  
s2(x18)             0x000000007ffffff4(2147483636)                  0x000000007ffffff4(2147483636)                  
s3(x19)             0x000000008017fca3(2149055651)                  0x000000008017fca3(2149055651)                  
s4(x20)             0x0000000080180271(2149057137)                  0x0000000080180271(2149057137)                  
s5(x21)             0x0000000080000187(2147484039)                  0x0000000080000187(2147484039)                  
s6(x22)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s7(x23)             0x0000000080000837(2147485751)                  0x0000000080000837(2147485751)                  
s8(x24)             0x000000008017fc5a(2149055578)                  0x000000008017fc5a(2149055578)                  
s9(x25)             0x000000008017fe7c(2149056124)                  0x000000008017fe7c(2149056124)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000007ffffc2d(2147482669)                  0x000000007ffffc2d(2147482669)                  
t3(x28)             0x000000008017fc0e(2149055502)                  0x000000008017fc0e(2149055502)                  
t4(x29)             0x000000008017fa7c(2149055100)                  0x000000008017fa7c(2149055100)                  
t5(x30)             0x0000000000000200(512)                         0x0000000000000200(512)                         
t6(x31)             0x000000000071b823(7452707)                     0x000000000071b823(7452707)                     

STATE               REF                                             DUT                                             DIFF
xmemhash            e0a0cf06de4ceeafebe3659fc6558d2ec4b1979e        e0a0cf06de4ceeafebe3659fc6558d2ec4b1979e        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000744(2147485508)                  0x0000000080000744(2147485508)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000041(65)                          0x0000000000000041(65)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff95d84000(-8.734267942607043e-26_s)    0xffffffff95d84000(-8.734267942607043e-26_s)    
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f3                  0xffffffffceffd008(-2145911808.0_s)             0xffffffffceffd008(-2145911808.0_s)             
f4                  0xffffffff15d84000(8.734267942607043e-26_s)     0xffffffff15d84000(8.734267942607043e-26_s)     
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x41b5d84000000000(366493696.0_d)               0x41b5d84000000000(366493696.0_d)               
f8                  0x41dffffffd000000(2147483636.0_d)              0x41dffffffd000000(2147483636.0_d)              
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff2aa65f81(2.9553792681331903e-13_s)    0xffffffff2aa65f81(2.9553792681331903e-13_s)    
f16                 0xffffffff95d84000(-8.734267942607043e-26_s)    0xffffffff95d84000(-8.734267942607043e-26_s)    
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x000000007ffffe0e(1.0609976494e-314_d)         0x000000007ffffe0e(1.0609976494e-314_d)         
f25                 0xffffffff4f0027fc(2150104064.0_s)              0xffffffff4f0027fc(2150104064.0_s)              
f26                 0xffffffff473515ef(46357.93359375_s)            0xffffffff473515f0(46357.9375_s)                X
f27                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f28                 0xffffffff4f00005f(2147507968.0_s)              0xffffffff4f00005f(2147507968.0_s)              
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff4f001807(2149058304.0_s)              0xffffffff4f001807(2149058304.0_s)              
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

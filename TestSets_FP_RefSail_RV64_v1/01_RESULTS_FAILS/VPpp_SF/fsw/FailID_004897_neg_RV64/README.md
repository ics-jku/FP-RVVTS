# FailID_004897 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4897
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
_reg_f0: .byte 0xd0,0xf0,0x98,0x14,0x32,0xf0,0xd5,0xed
_reg_f1: .byte 0x83,0x21,0x1c,0xad,0x38,0x76,0x21,0x74
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x2c,0x46,0xac,0x3c,0x1f,0x11,0x3b,0x09
_reg_f5: .byte 0x23,0x40,0x94,0x24,0xe2,0x01,0x75,0x03
_reg_f6: .byte 0x90,0xa5,0xd5,0x5e,0xff,0xff,0xff,0xff
_reg_f7: .byte 0xd0,0xf0,0x98,0x14,0x32,0xf0,0xd5,0x6d
_reg_f8: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f9: .byte 0x22,0x69,0xf8,0x0b,0xc5,0xcd,0x2e,0x12
_reg_f10:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xa9,0xcf,0x62,0x49,0x57,0xe7,0xda,0x97
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x90,0x0d,0x95,0x9b,0x78,0xd2,0xcd,0xed
_reg_f15:.byte 0x00,0x00,0x00,0xa7,0x00,0x03,0xe0,0x41
_reg_f16:.byte 0x86,0xa6,0xa5,0x36,0x64,0x68,0xb2,0x41
_reg_f17:.byte 0x33,0xcb,0xf8,0x97,0xdc,0x12,0x41,0xf4
_reg_f18:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x19,0xee,0xd9,0x2d,0xaf,0x40,0xdd,0xd8
_reg_f20:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0xa3,0x21,0xca,0x65,0x8e,0x35,0x7b,0xce
_reg_f24:.byte 0x75,0x73,0xf3,0x35,0x90,0x3f,0x7d,0x86
_reg_f25:.byte 0x45,0x75,0xc7,0x2c,0xfd,0xe0,0x20,0x1b
_reg_f26:.byte 0x57,0x1b,0xca,0x72,0x0c,0x59,0xbe,0x49
_reg_f27:.byte 0xc2,0x34,0xfd,0x3f,0x63,0x1f,0x40,0xda
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x80,0xc7,0x7f,0xad,0x04,0x34,0x79,0x7e
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x81
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x800002c4            // ra
    li x2, 0x8005b90a            // sp
    li x3, 0x0                   // gp
    li x4, 0xbc                  // tp
    li x5, 0x17f800              // t0
    li x6, 0x802000ec            // t1
    li x7, 0x5fe                 // t2
    li x8, 0x80280450            // fp
    li x9, 0x41                  // s1
    li x10, 0x1                  // a0
    li x11, 0x8012375            // a1
    li x12, 0x8000010a           // a2
    li x13, 0x7ffff97e           // a3
    li x14, 0x8017fabb           // a4
    li x15, 0x0                  // a5
    li x16, 0x7ffff860           // a6
    li x17, 0x80000000           // a7
    li x18, 0x801806aa           // s2
    li x19, 0x0                  // s3
    li x20, 0x0                  // s4
    li x21, 0x80123754           // s5
    li x22, 0x28                 // s6
    li x23, 0xa6846efcd965c5ed   // s7
    li x24, 0x0                  // s8
    li x25, 0x801ffa21           // s9
    li x26, 0x0                  // s10
    li x27, 0x8018040a           // s11
    li x28, 0x6000               // t3
    li x29, 0x8017f83e           // t4
    li x30, 0x2007f              // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f24', 'x20'}, 'clob': {'x6', 'x20'}})
    
    li x6, 0xffffc
    and x20, x20, x6
    li x6, 0x8017f8bb
    add x20, x20, x6
    fsw f24, 0x745(x20)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        15bfdbf2d682b362c3579b96b5d443836d1af306        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f24, 0x745(x20)
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        15bfdbf2d682b362c3579b96b5d443836d1af306        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f24, x745, x20
s4(x20)             0x000000008017f8bb(2149054651)                  0x000000008017f8bb(2149054651)
f24                 0x867d3f9035f37375(-2.062455322268751e-277_d)   0x867d3f9035f37375(-2.062455322268751e-277_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000800002c4(2147484356)                  0x00000000800002c4(2147484356)                  
sp(x2)              0x000000008005b90a(2147858698)                  0x000000008005b90a(2147858698)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x00000000000000bc(188)                         0x00000000000000bc(188)                         
t0(x5)              0x000000000017f800(1570816)                     0x000000000017f800(1570816)                     
t1(x6)              0x000000008017f8bb(2149054651)                  0x000000008017f8bb(2149054651)                  
t2(x7)              0x00000000000005fe(1534)                        0x00000000000005fe(1534)                        
fp(x8)              0x0000000080280450(2150106192)                  0x0000000080280450(2150106192)                  
s1(x9)              0x0000000000000041(65)                          0x0000000000000041(65)                          
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x0000000008012375(134292341)                   0x0000000008012375(134292341)                   
a2(x12)             0x000000008000010a(2147483914)                  0x000000008000010a(2147483914)                  
a3(x13)             0x000000007ffff97e(2147481982)                  0x000000007ffff97e(2147481982)                  
a4(x14)             0x000000008017fabb(2149055163)                  0x000000008017fabb(2149055163)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x000000007ffff860(2147481696)                  0x000000007ffff860(2147481696)                  
a7(x17)             0x0000000080000000(2147483648)                  0x0000000080000000(2147483648)                  
s2(x18)             0x00000000801806aa(2149058218)                  0x00000000801806aa(2149058218)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000008017f8bb(2149054651)                  0x000000008017f8bb(2149054651)                  
s5(x21)             0x0000000080123754(2148677460)                  0x0000000080123754(2148677460)                  
s6(x22)             0x0000000000000028(40)                          0x0000000000000028(40)                          
s7(x23)             0xa6846efcd965c5ed(11998837339479983597)        0xa6846efcd965c5ed(11998837339479983597)        
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x00000000801ffa21(2149579297)                  0x00000000801ffa21(2149579297)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000008018040a(2149057546)                  0x000000008018040a(2149057546)                  
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x000000008017f83e(2149054526)                  0x000000008017f83e(2149054526)                  
t5(x30)             0x000000000002007f(131199)                      0x000000000002007f(131199)                      
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            9a25a4163a65d6fd52fc79867d72501441e6955e        9a25a4163a65d6fd52fc79867d72501441e6955e        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        15bfdbf2d682b362c3579b96b5d443836d1af306        X
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000081(129)                         0x0000000000000081(129)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xedd5f0321498f0d0(-1.2390792847574973e+221_d)  0xedd5f0321498f0d0(-1.2390792847574973e+221_d)  
f1                  0x74217638ad1c2183(2.500434393046269e+251_d)    0x74217638ad1c2183(2.500434393046269e+251_d)    
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x093b111f3cac462c(3.3577013057289645e-264_d)   0x093b111f3cac462c(3.3577013057289645e-264_d)   
f5                  0x037501e224944023(5.262785007461329e-292_d)    0x037501e224944023(5.262785007461329e-292_d)    
f6                  0xffffffff5ed5a590(7.697434615455154e+18_s)     0xffffffff5ed5a590(7.697434615455154e+18_s)     
f7                  0x6dd5f0321498f0d0(1.2390792847574973e+221_d)   0x6dd5f0321498f0d0(1.2390792847574973e+221_d)   
f8                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f9                  0x122ecdc50bf86922(4.260860548824609e-221_d)    0x122ecdc50bf86922(4.260860548824609e-221_d)    
f10                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x97dae7574962cfa9(-9.213707466843409e-194_d)   0x97dae7574962cfa9(-9.213707466843409e-194_d)   
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0xedcdd2789b950d90(-8.421817586531674e+220_d)   0xedcdd2789b950d90(-8.421817586531674e+220_d)   
f15                 0x41e00300a7000000(2149057848.0_d)              0x41e00300a7000000(2149057848.0_d)              
f16                 0x41b2686436a5a686(308831286.6470722_d)         0x41b2686436a5a686(308831286.6470722_d)         
f17                 0xf44112dc97f8cb33(-9.779428757244409e+251_d)   0xf44112dc97f8cb33(-9.779428757244409e+251_d)   
f18                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f19                 0xd8dd40af2dd9ee19(-1.1802767397232151e+120_d)  0xd8dd40af2dd9ee19(-1.1802767397232151e+120_d)  
f20                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0xce7b358e65ca21a3(-1.173693904724524e+70_d)    0xce7b358e65ca21a3(-1.173693904724524e+70_d)    
f24                 0x867d3f9035f37375(-2.062455322268751e-277_d)   0x867d3f9035f37375(-2.062455322268751e-277_d)   
f25                 0x1b20e0fd2cc77545(5.206618571249988e-178_d)    0x1b20e0fd2cc77545(5.206618571249988e-178_d)    
f26                 0x49be590c72ca1b57(1.7325557385565143e+47_d)    0x49be590c72ca1b57(1.7325557385565143e+47_d)    
f27                 0xda401f633ffd34c2(-5.45686854277534e+126_d)    0xda401f633ffd34c2(-5.45686854277534e+126_d)    
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x7e793404ad7fc780(1.6878401153773121e+301_d)   0x7e793404ad7fc780(1.6878401153773121e+301_d)   
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

# FailID_003209 VP++ SF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3209
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0x9d,0xe1,0x2d,0x8e,0x26,0x94,0x9e,0x69
_reg_f1: .byte 0x82,0x1e,0x50,0x56,0x55,0xdb,0xee,0x7e
_reg_f2: .byte 0xfa,0x8e,0x38,0xf1,0x8a,0xf4,0xd2,0xfb
_reg_f3: .byte 0x05,0xe8,0x3f,0xd0,0x7c,0x9e,0x54,0x55
_reg_f4: .byte 0x79,0xc4,0x6c,0x99,0xb8,0xee,0x8a,0x1e
_reg_f5: .byte 0x86,0xee,0xfc,0x74,0xa0,0xe5,0x1c,0x69
_reg_f6: .byte 0xb8,0x03,0x08,0x8c,0x58,0xfd,0xaa,0xb8
_reg_f7: .byte 0x46,0xe7,0xd2,0x01,0xeb,0xfe,0xde,0xc0
_reg_f8: .byte 0x26,0xc2,0xbc,0x47,0x0e,0x30,0x46,0x8c
_reg_f9: .byte 0x9b,0x5c,0xfa,0x6d,0x32,0x4b,0xca,0xcd
_reg_f10:.byte 0x1b,0x1a,0x07,0x55,0x1f,0x95,0xd7,0x14
_reg_f11:.byte 0xcb,0xe1,0xb6,0xbd,0xa6,0xa5,0x2d,0x9d
_reg_f12:.byte 0x1e,0xba,0x1a,0x11,0x64,0xf5,0xf6,0x17
_reg_f13:.byte 0xa5,0x3d,0x5a,0x39,0xdc,0xa3,0xa2,0xc5
_reg_f14:.byte 0xf5,0x23,0x56,0x01,0x25,0x80,0x47,0xad
_reg_f15:.byte 0x5c,0xe9,0xbe,0xf7,0x1c,0xf0,0x59,0x9e
_reg_f16:.byte 0x4d,0xc2,0x9e,0x7f,0xc1,0x7f,0xc3,0xe7
_reg_f17:.byte 0x34,0x6f,0xbd,0x8c,0x5c,0x00,0x96,0x15
_reg_f18:.byte 0x7e,0x62,0xd4,0x08,0xfe,0x01,0xe3,0xb1
_reg_f19:.byte 0x62,0x15,0xee,0xc7,0xac,0xc7,0xee,0x17
_reg_f20:.byte 0x35,0x80,0xd7,0x18,0x69,0x22,0x84,0xa3
_reg_f21:.byte 0x01,0x17,0x4e,0x4e,0xa3,0xc2,0x21,0x2a
_reg_f22:.byte 0x0c,0x37,0x68,0xc8,0x1e,0xad,0x09,0x16
_reg_f23:.byte 0x1a,0xfd,0x3d,0x6d,0xf0,0x93,0x79,0xb7
_reg_f24:.byte 0x86,0xa1,0xdf,0x93,0x55,0xf5,0x35,0x01
_reg_f25:.byte 0x7a,0x99,0xdd,0x49,0xa9,0x9b,0x34,0xc2
_reg_f26:.byte 0x95,0x27,0x4e,0xd1,0x94,0x7d,0xd1,0x41
_reg_f27:.byte 0xdd,0x76,0x6c,0x52,0x8c,0xea,0xf1,0xd3
_reg_f28:.byte 0x1f,0xc9,0x90,0x14,0xe3,0x91,0xcb,0x26
_reg_f29:.byte 0x5b,0x3b,0xbc,0xa4,0x2f,0x62,0xe6,0xfc
_reg_f30:.byte 0x7d,0xd8,0x6d,0x12,0xac,0x3c,0x11,0x71
_reg_f31:.byte 0xa9,0xe4,0x48,0xd7,0x3c,0xdc,0x4d,0x99
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x80
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xb723d1bc196de92a    // ra
    li x2, 0x5c519c74b729e9d1    // sp
    li x3, 0x800eb4fd            // gp
    li x4, 0x80000229            // tp
    li x5, 0x4427136edaf78784    // t0
    li x6, 0x12c5d983d7d1456     // t1
    li x7, 0x1342482374773cf7    // t2
    li x8, 0x7e3e2000            // fp
    li x9, 0x4d6075ee025e22fa    // s1
    li x10, 0x371c3481b19e29f7   // a0
    li x11, 0xd04dac540a22007c   // a1
    li x12, 0x64b0493e6b62e28e   // a2
    li x13, 0xdcd4469c58e82461   // a3
    li x14, 0x2030ba505ef14051   // a4
    li x15, 0xdd60a59d9e25c23f   // a5
    li x16, 0x11081356341421dc   // a6
    li x17, 0xf2feb6b94b281a33   // a7
    li x18, 0xa55ac4bb7b8c5a21   // s2
    li x19, 0xbeeb5d18c8f8790e   // s3
    li x20, 0xcbb7785612aa56fa   // s4
    li x21, 0x4d09208dd1         // s5
    li x22, 0x0                  // s6
    li x23, 0xfa5a1624882f1cb0   // s7
    li x24, 0x6698264fe449854c   // s8
    li x25, 0x908f591c301c68d9   // s9
    li x26, 0xdfa5786c4dcf05dd   // s10
    li x27, 0xb1a15ae977eff69    // s11
    li x28, 0x6636bddd32f603ca   // t3
    li x29, 0x166673e017d6f72c   // t4
    li x30, 0x50ca29ae5e80ce52   // t5
    li x31, 0xeaf2ea0f049eefae   // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x11'}, 'clob': {'x5', 'f18', 'x11'}})
    
    li x5, 0x1ffff8
    and x11, x11, x5
    li x5, 0x80000720
    add x11, x11, x5
    fld f18, -0x720(x11)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f18                 0xb1e301fe08d4627e(-2.2032432435072226e-68_d)   0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f18, -0x720(x11)
+========================================================================================================================+
Attributes:  special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f18                 0xb1e301fe08d4627e(-2.2032432435072226e-68_d)   0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f18, x720, x11
a1(x11)             0x0000000080020798(2147616664)                  0x0000000080020798(2147616664)
f18                 0xb1e301fe08d4627e(-2.2032432435072226e-68_d)   0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xb723d1bc196de92a(13196621938936375594)        0xb723d1bc196de92a(13196621938936375594)        
sp(x2)              0x5c519c74b729e9d1(6652270149706050001)         0x5c519c74b729e9d1(6652270149706050001)         
gp(x3)              0x00000000800eb4fd(2148447485)                  0x00000000800eb4fd(2148447485)                  
tp(x4)              0x0000000080000229(2147484201)                  0x0000000080000229(2147484201)                  
t0(x5)              0x0000000080000720(2147485472)                  0x0000000080000720(2147485472)                  
t1(x6)              0x012c5d983d7d1456(84545401461216342)           0x012c5d983d7d1456(84545401461216342)           
t2(x7)              0x1342482374773cf7(1387750952298560759)         0x1342482374773cf7(1387750952298560759)         
fp(x8)              0x000000007e3e2000(2118000640)                  0x000000007e3e2000(2118000640)                  
s1(x9)              0x4d6075ee025e22fa(5575586003787064058)         0x4d6075ee025e22fa(5575586003787064058)         
a0(x10)             0x371c3481b19e29f7(3971106703069293047)         0x371c3481b19e29f7(3971106703069293047)         
a1(x11)             0x0000000080020798(2147616664)                  0x0000000080020798(2147616664)                  
a2(x12)             0x64b0493e6b62e28e(7255379532132311694)         0x64b0493e6b62e28e(7255379532132311694)         
a3(x13)             0xdcd4469c58e82461(15912421020727256161)        0xdcd4469c58e82461(15912421020727256161)        
a4(x14)             0x2030ba505ef14051(2319558662448824401)         0x2030ba505ef14051(2319558662448824401)         
a5(x15)             0xdd60a59d9e25c23f(15951931976528020031)        0xdd60a59d9e25c23f(15951931976528020031)        
a6(x16)             0x11081356341421dc(1227252159420309980)         0x11081356341421dc(1227252159420309980)         
a7(x17)             0xf2feb6b94b281a33(17509633308209191475)        0xf2feb6b94b281a33(17509633308209191475)        
s2(x18)             0xa55ac4bb7b8c5a21(11915052073672792609)        0xa55ac4bb7b8c5a21(11915052073672792609)        
s3(x19)             0xbeeb5d18c8f8790e(13757191847765637390)        0xbeeb5d18c8f8790e(13757191847765637390)        
s4(x20)             0xcbb7785612aa56fa(14679333821513094906)        0xcbb7785612aa56fa(14679333821513094906)        
s5(x21)             0x0000004d09208dd1(330865610193)                0x0000004d09208dd1(330865610193)                
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0xfa5a1624882f1cb0(18039755603545365680)        0xfa5a1624882f1cb0(18039755603545365680)        
s8(x24)             0x6698264fe449854c(7392700912902964556)         0x6698264fe449854c(7392700912902964556)         
s9(x25)             0x908f591c301c68d9(10416642440732371161)        0x908f591c301c68d9(10416642440732371161)        
s10(x26)            0xdfa5786c4dcf05dd(16115419248172402141)        0xdfa5786c4dcf05dd(16115419248172402141)        
s11(x27)            0x0b1a15ae977eff69(799975723421859689)          0x0b1a15ae977eff69(799975723421859689)          
t3(x28)             0x6636bddd32f603ca(7365282998351430602)         0x6636bddd32f603ca(7365282998351430602)         
t4(x29)             0x166673e017d6f72c(1614104922768733996)         0x166673e017d6f72c(1614104922768733996)         
t5(x30)             0x50ca29ae5e80ce52(5821511297216335442)         0x50ca29ae5e80ce52(5821511297216335442)         
t6(x31)             0xeaf2ea0f049eefae(16929851299462049710)        0xeaf2ea0f049eefae(16929851299462049710)        

STATE               REF                                             DUT                                             DIFF
xmemhash            9e47390e43e73bcf1890fd3b69336b42e1ff4009        9e47390e43e73bcf1890fd3b69336b42e1ff4009        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000984(2147486084)                  0x0000000080000984(2147486084)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000080(128)                         0x0000000000000080(128)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x699e94268e2de19d(5.851622980020159e+200_d)    0x699e94268e2de19d(5.851622980020159e+200_d)    
f1                  0x7eeedb5556501e82(2.6450636480365518e+303_d)   0x7eeedb5556501e82(2.6450636480365518e+303_d)   
f2                  0xfbd2f48af1388efa(-2.88632524332321e+288_d)    0xfbd2f48af1388efa(-2.88632524332321e+288_d)    
f3                  0x55549e7cd03fe805(1.1545375725263908e+103_d)   0x55549e7cd03fe805(1.1545375725263908e+103_d)   
f4                  0x1e8aeeb8996cc479(1.4966114873488691e-161_d)   0x1e8aeeb8996cc479(1.4966114873488691e-161_d)   
f5                  0x691ce5a074fcee86(2.1600789067730766e+198_d)   0x691ce5a074fcee86(2.1600789067730766e+198_d)   
f6                  0xb8aafd588c0803b8(-1.0152371322128331e-35_d)   0xb8aafd588c0803b8(-1.0152371322128331e-35_d)   
f7                  0xc0defeeb01d2e746(-31739.671986318448_d)       0xc0defeeb01d2e746(-31739.671986318448_d)       
f8                  0x8c46300e47bcc226(-1.5494809411761106e-249_d)  0x8c46300e47bcc226(-1.5494809411761106e-249_d)  
f9                  0xcdca4b326dfa5c9b(-5.538107662154827e+66_d)    0xcdca4b326dfa5c9b(-5.538107662154827e+66_d)    
f10                 0x14d7951f55071a1b(2.86928061563642e-208_d)     0x14d7951f55071a1b(2.86928061563642e-208_d)     
f11                 0x9d2da5a6bdb6e1cb(-3.9278445542876183e-168_d)  0x9d2da5a6bdb6e1cb(-3.9278445542876183e-168_d)  
f12                 0x17f6f564111aba1e(3.1450488993396176e-193_d)   0x17f6f564111aba1e(3.1450488993396176e-193_d)   
f13                 0xc5a2a3dc395a3da5(-2.884412531987287e+27_d)    0xc5a2a3dc395a3da5(-2.884412531987287e+27_d)    
f14                 0xad478025015623f5(-1.4420808547245098e-90_d)   0xad478025015623f5(-1.4420808547245098e-90_d)   
f15                 0x9e59f01cf7bee95c(-1.801680861024694e-162_d)   0x9e59f01cf7bee95c(-1.801680861024694e-162_d)   
f16                 0xe7c37fc17f9ec24d(-6.950253192023348e+191_d)   0xe7c37fc17f9ec24d(-6.950253192023348e+191_d)   
f17                 0x1596005c8cbd6f34(1.0964618228522242e-204_d)   0x1596005c8cbd6f34(1.0964618228522242e-204_d)   
f18                 0xb1e301fe08d4627e(-2.2032432435072226e-68_d)   0x0000000000000000(0.0_d)                       X
f19                 0x17eec7acc7ee1562(2.108245259921171e-193_d)    0x17eec7acc7ee1562(2.108245259921171e-193_d)    
f20                 0xa384226918d78035(-1.3526051321766731e-137_d)  0xa384226918d78035(-1.3526051321766731e-137_d)  
f21                 0x2a21c2a34e4e1701(9.679700821562473e-106_d)    0x2a21c2a34e4e1701(9.679700821562473e-106_d)    
f22                 0x1609ad1ec868370c(1.6378892730900231e-202_d)   0x1609ad1ec868370c(1.6378892730900231e-202_d)   
f23                 0xb77993f06d3dfd1a(-1.835123419814649e-41_d)    0xb77993f06d3dfd1a(-1.835123419814649e-41_d)    
f24                 0x0135f55593dfa186(8.005045742922661e-303_d)    0x0135f55593dfa186(8.005045742922661e-303_d)    
f25                 0xc2349ba949dd997a(-88510908893.59952_d)        0xc2349ba949dd997a(-88510908893.59952_d)        
f26                 0x41d17d94d14e2795(1173771077.221166_d)         0x41d17d94d14e2795(1173771077.221166_d)         
f27                 0xd3f1ea8c526c76dd(-2.391798669688445e+96_d)    0xd3f1ea8c526c76dd(-2.391798669688445e+96_d)    
f28                 0x26cb91e31490c91f(8.341160967466725e-122_d)    0x26cb91e31490c91f(8.341160967466725e-122_d)    
f29                 0xfce6622fa4bc3b5b(-4.4673970368384845e+293_d)  0xfce6622fa4bc3b5b(-4.4673970368384845e+293_d)  
f30                 0x71113cac126dd87d(4.38448214905641e+236_d)     0x71113cac126dd87d(4.38448214905641e+236_d)     
f31                 0x994ddc3cd748e4a9(-8.578412323428339e-187_d)   0x994ddc3cd748e4a9(-8.578412323428339e-187_d)   
STATES DIFFER: True
```

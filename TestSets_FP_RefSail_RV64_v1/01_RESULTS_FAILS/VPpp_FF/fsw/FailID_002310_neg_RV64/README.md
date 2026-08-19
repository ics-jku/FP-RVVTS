# FailID_002310 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2310
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
_reg_f0: .byte 0xb4,0xd0,0xa5,0xba,0xfa,0x00,0xfd,0xb3
_reg_f1: .byte 0xea,0xa4,0x61,0x0b,0x2d,0xa0,0xd6,0xd0
_reg_f2: .byte 0x60,0x5e,0x3a,0xf0,0xf6,0x21,0xdf,0xb5
_reg_f3: .byte 0x6f,0x48,0xa0,0xf0,0x6c,0xf5,0xec,0xb1
_reg_f4: .byte 0x64,0x68,0x9a,0xd9,0x30,0x57,0xe1,0xdb
_reg_f5: .byte 0x67,0x1c,0x69,0x36,0x1d,0x3a,0x36,0xc3
_reg_f6: .byte 0x76,0xa4,0xa2,0xb8,0x5f,0x5f,0x97,0xe6
_reg_f7: .byte 0x54,0xcc,0xc0,0x8c,0xbf,0x4a,0xdd,0x79
_reg_f8: .byte 0xd7,0xc9,0xb6,0x57,0xe4,0x7d,0xf9,0x4c
_reg_f9: .byte 0x1e,0x62,0x24,0x49,0x01,0xe2,0x17,0x95
_reg_f10:.byte 0xad,0x01,0xc4,0x3c,0x92,0x90,0x3f,0xa4
_reg_f11:.byte 0x91,0x9d,0x7c,0x30,0x47,0x49,0x1d,0x4c
_reg_f12:.byte 0x30,0x2b,0xfc,0x3f,0x2b,0xb5,0x49,0x33
_reg_f13:.byte 0xff,0x10,0xae,0x23,0x80,0x14,0x7c,0xde
_reg_f14:.byte 0xa4,0x74,0xa8,0xf2,0xba,0x30,0xc3,0x71
_reg_f15:.byte 0xee,0x20,0xe5,0x42,0x62,0x5f,0x95,0xa3
_reg_f16:.byte 0x4e,0x4c,0x58,0xd3,0xfa,0x6f,0x0d,0x6a
_reg_f17:.byte 0x1c,0x0d,0x72,0x89,0x7c,0xaf,0x95,0xa2
_reg_f18:.byte 0xf0,0x55,0xd0,0xe5,0xcc,0xf2,0x54,0x8e
_reg_f19:.byte 0x61,0x0e,0xfa,0x13,0xf8,0xc0,0x25,0x50
_reg_f20:.byte 0x24,0xa4,0x63,0x38,0xcd,0x2d,0xd1,0x4b
_reg_f21:.byte 0x4f,0xe7,0xe2,0x89,0xa4,0x08,0x97,0x0b
_reg_f22:.byte 0xe0,0x79,0xc2,0xf0,0xe2,0x28,0x5c,0x14
_reg_f23:.byte 0x96,0x08,0x22,0x7f,0xf8,0x90,0xf3,0x75
_reg_f24:.byte 0xcb,0x5a,0x66,0xb8,0xef,0xeb,0xae,0x44
_reg_f25:.byte 0x0e,0x08,0xae,0x95,0x1a,0x75,0xd8,0x8d
_reg_f26:.byte 0x99,0x79,0x5d,0xb0,0x95,0xf7,0x9b,0x90
_reg_f27:.byte 0xd1,0x2d,0x6a,0x13,0x9e,0x8f,0x57,0x4b
_reg_f28:.byte 0xab,0x53,0xa0,0x85,0x51,0xc0,0xa3,0x8a
_reg_f29:.byte 0x8c,0x38,0x69,0xa0,0x31,0xf3,0xe3,0xfa
_reg_f30:.byte 0xde,0xee,0x65,0x82,0xf0,0x06,0xa9,0x23
_reg_f31:.byte 0x98,0xa3,0xed,0x57,0x97,0x73,0x65,0xd5
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x0
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xd1c026d1700a3e3f    // ra
    li x2, 0x4c568bc7c09d2889    // sp
    li x3, 0xf38482c7ad6c7576    // gp
    li x4, 0x866664d25e8e39b8    // tp
    li x5, 0x9a316a9edcd43a2     // t0
    li x6, 0x4f96a88d772792d1    // t1
    li x7, 0x9ce639e8            // t2
    li x8, 0xd479ad352b4328b8    // fp
    li x9, 0xf0d8e347b4e57d42    // s1
    li x10, 0xbda3168704182046   // a0
    li x11, 0xee9aeef2dd9e3d3b   // a1
    li x12, 0x65e0d0c24aab6ebe   // a2
    li x13, 0x19d40aeec6b424d1   // a3
    li x14, 0xda5d41e8a55b0b80   // a4
    li x15, 0x8a9e6fcf4c121bce   // a5
    li x16, 0xf38983130859ea9    // a6
    li x17, 0x1091b8231f7a3572   // a7
    li x18, 0x6000               // s2
    li x19, 0x15832480cddbbabd   // s3
    li x20, 0x1e8a0d0f82fcd04    // s4
    li x21, 0x4930c186dd1978ca   // s5
    li x22, 0xf38482c7ad6c6fd6   // s6
    li x23, 0x3ef2b6dcafda307    // s7
    li x24, 0x5ca0f48955b4c515   // s8
    li x25, 0x37ddb4514f73fcda   // s9
    li x26, 0x700670e55876701    // s10
    li x27, 0x96fe75a23c1abcf1   // s11
    li x28, 0x2d137d2da5532b2f   // t3
    li x29, 0x523c97d6a9432278   // t4
    li x30, 0x231fd6d893d3f623   // t5
    li x31, 0xffebd9bde8180335   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f1', 'x29'}, 'clob': {'x29', 'x1'}})
    
    li x1, 0xffffc
    and x29, x29, x1
    li x1, 0x8017ffa3
    add x29, x29, x1
    fsw f1, 0x5d(x29)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        e9b6f848c444b7bd55961ef8847141f7f96dce13        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f1, 0x5d(x29)
+========================================================================================================================+
Attributes:  none
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        e9b6f848c444b7bd55961ef8847141f7f96dce13        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f1, x5, x29
t0(x5)              0x09a316a9edcd43a2(694423686640124834)          0x09a316a9edcd43a2(694423686640124834)
t4(x29)             0x00000000801b221b(2149261851)                  0x00000000801b221b(2149261851)
f1                  0xd0d6a02d0b61a4ea(-2.6827526201998193e+81_d)   0xd0d6a02d0b61a4ea(-2.6827526201998193e+81_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017ffa3(2149056419)                  0x000000008017ffa3(2149056419)                  
sp(x2)              0x4c568bc7c09d2889(5500737684925917321)         0x4c568bc7c09d2889(5500737684925917321)         
gp(x3)              0xf38482c7ad6c7576(17547293842261964150)        0xf38482c7ad6c7576(17547293842261964150)        
tp(x4)              0x866664d25e8e39b8(9684538903399119288)         0x866664d25e8e39b8(9684538903399119288)         
t0(x5)              0x09a316a9edcd43a2(694423686640124834)          0x09a316a9edcd43a2(694423686640124834)          
t1(x6)              0x4f96a88d772792d1(5734956501045842641)         0x4f96a88d772792d1(5734956501045842641)         
t2(x7)              0x000000009ce639e8(2632333800)                  0x000000009ce639e8(2632333800)                  
fp(x8)              0xd479ad352b4328b8(15310458852093405368)        0xd479ad352b4328b8(15310458852093405368)        
s1(x9)              0xf0d8e347b4e57d42(17354871061189328194)        0xf0d8e347b4e57d42(17354871061189328194)        
a0(x10)             0xbda3168704182046(13664790463517302854)        0xbda3168704182046(13664790463517302854)        
a1(x11)             0xee9aeef2dd9e3d3b(17193317254307921211)        0xee9aeef2dd9e3d3b(17193317254307921211)        
a2(x12)             0x65e0d0c24aab6ebe(7341096925508890302)         0x65e0d0c24aab6ebe(7341096925508890302)         
a3(x13)             0x19d40aeec6b424d1(1861124566663046353)         0x19d40aeec6b424d1(1861124566663046353)         
a4(x14)             0xda5d41e8a55b0b80(15734805140564806528)        0xda5d41e8a55b0b80(15734805140564806528)        
a5(x15)             0x8a9e6fcf4c121bce(9988543959679507406)         0x8a9e6fcf4c121bce(9988543959679507406)         
a6(x16)             0x0f38983130859ea9(1096793846299598505)         0x0f38983130859ea9(1096793846299598505)         
a7(x17)             0x1091b8231f7a3572(1193937837221361010)         0x1091b8231f7a3572(1193937837221361010)         
s2(x18)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s3(x19)             0x15832480cddbbabd(1550122832373725885)         0x15832480cddbbabd(1550122832373725885)         
s4(x20)             0x01e8a0d0f82fcd04(137536608012324100)          0x01e8a0d0f82fcd04(137536608012324100)          
s5(x21)             0x4930c186dd1978ca(5273927948630063306)         0x4930c186dd1978ca(5273927948630063306)         
s6(x22)             0xf38482c7ad6c6fd6(17547293842261962710)        0xf38482c7ad6c6fd6(17547293842261962710)        
s7(x23)             0x03ef2b6dcafda307(283493052104680199)          0x03ef2b6dcafda307(283493052104680199)          
s8(x24)             0x5ca0f48955b4c515(6674603518448682261)         0x5ca0f48955b4c515(6674603518448682261)         
s9(x25)             0x37ddb4514f73fcda(4025571903257443546)         0x37ddb4514f73fcda(4025571903257443546)         
s10(x26)            0x0700670e55876701(504516469527635713)          0x0700670e55876701(504516469527635713)          
s11(x27)            0x96fe75a23c1abcf1(10880263089427234033)        0x96fe75a23c1abcf1(10880263089427234033)        
t3(x28)             0x2d137d2da5532b2f(3248077391264951087)         0x2d137d2da5532b2f(3248077391264951087)         
t4(x29)             0x00000000801b221b(2149261851)                  0x00000000801b221b(2149261851)                  
t5(x30)             0x231fd6d893d3f623(2530977741286929955)         0x231fd6d893d3f623(2530977741286929955)         
t6(x31)             0xffebd9bde8180335(18441072508864561973)        0xffebd9bde8180335(18441072508864561973)        

STATE               REF                                             DUT                                             DIFF
xmemhash            237a8abd3fa199af5008f27e03b2a617f85da145        237a8abd3fa199af5008f27e03b2a617f85da145        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        e9b6f848c444b7bd55961ef8847141f7f96dce13        X
lastPC              0x00000000800009c0(2147486144)                  0x00000000800009c0(2147486144)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000000(0)                           0x0000000000000000(0)                           
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    
f1                  0xd0d6a02d0b61a4ea(-2.6827526201998193e+81_d)   0xd0d6a02d0b61a4ea(-2.6827526201998193e+81_d)   
f2                  0xb5df21f6f03a5e60(-3.328412520596668e-49_d)    0xb5df21f6f03a5e60(-3.328412520596668e-49_d)    
f3                  0xb1ecf56cf0a0486f(-3.356680131267773e-68_d)    0xb1ecf56cf0a0486f(-3.356680131267773e-68_d)    
f4                  0xdbe15730d99a6864(-3.938691153290651e+134_d)   0xdbe15730d99a6864(-3.938691153290651e+134_d)   
f5                  0xc3363a1d36691c67(-6256346628955239.0_d)       0xc3363a1d36691c67(-6256346628955239.0_d)       
f6                  0xe6975f5fb8a2a476(-1.5889986046966891e+186_d)  0xe6975f5fb8a2a476(-1.5889986046966891e+186_d)  
f7                  0x79dd4abf8cc0cc54(1.0384959566860558e+279_d)   0x79dd4abf8cc0cc54(1.0384959566860558e+279_d)   
f8                  0x4cf97de457b6c9d7(6.554190042954392e+62_d)     0x4cf97de457b6c9d7(6.554190042954392e+62_d)     
f9                  0x9517e2014924621e(-4.649313353680079e-207_d)   0x9517e2014924621e(-4.649313353680079e-207_d)   
f10                 0xa43f90923cc401ad(-4.3427421173394577e-134_d)  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  
f11                 0x4c1d4947307c9d91(4.595818092699139e+58_d)     0x4c1d4947307c9d91(4.595818092699139e+58_d)     
f12                 0x3349b52b3ffc2b30(1.2498387112867394e-61_d)    0x3349b52b3ffc2b30(1.2498387112867394e-61_d)    
f13                 0xde7c148023ae10ff(-1.4025431970955475e+147_d)  0xde7c148023ae10ff(-1.4025431970955475e+147_d)  
f14                 0x71c330baf2a874a4(9.996995945124462e+239_d)    0x71c330baf2a874a4(9.996995945124462e+239_d)    
f15                 0xa3955f6242e520ee(-2.871568650674459e-137_d)   0xa3955f6242e520ee(-2.871568650674459e-137_d)   
f16                 0x6a0d6ffad3584c4e(7.210524533161241e+202_d)    0x6a0d6ffad3584c4e(7.210524533161241e+202_d)    
f17                 0xa295af7c89720d1c(-4.445814887693426e-142_d)   0xa295af7c89720d1c(-4.445814887693426e-142_d)   
f18                 0x8e54f2cce5d055f0(-1.2566522884319492e-239_d)  0x8e54f2cce5d055f0(-1.2566522884319492e-239_d)  
f19                 0x5025c0f813fa0e61(1.259458128429187e+78_d)     0x5025c0f813fa0e61(1.259458128429187e+78_d)     
f20                 0x4bd12dcd3863a424(1.6849028513723058e+57_d)    0x4bd12dcd3863a424(1.6849028513723058e+57_d)    
f21                 0x0b9708a489e2e74f(7.854318363103068e-253_d)    0x0b9708a489e2e74f(7.854318363103068e-253_d)    
f22                 0x145c28e2f0c279e0(1.3383548145796845e-210_d)   0x145c28e2f0c279e0(1.3383548145796845e-210_d)   
f23                 0x75f390f87f220896(1.5041972699749784e+260_d)   0x75f390f87f220896(1.5041972699749784e+260_d)   
f24                 0x44aeebefb8665acb(7.301162650616101e+22_d)     0x44aeebefb8665acb(7.301162650616101e+22_d)     
f25                 0x8dd8751a95ae080e(-5.7310531554960516e-242_d)  0x8dd8751a95ae080e(-5.7310531554960516e-242_d)  
f26                 0x909bf795b05d7999(-1.1528987581327443e-228_d)  0x909bf795b05d7999(-1.1528987581327443e-228_d)  
f27                 0x4b578f9e136a2dd1(9.026784080126072e+54_d)     0x4b578f9e136a2dd1(9.026784080126072e+54_d)     
f28                 0x8aa3c05185a053ab(-2.055361269188195e-257_d)   0x8aa3c05185a053ab(-2.055361269188195e-257_d)   
f29                 0xfae3f331a069388c(-9.270609882403083e+283_d)   0xfae3f331a069388c(-9.270609882403083e+283_d)   
f30                 0x23a906f08265eede(6.725160268844749e-137_d)    0x23a906f08265eede(6.725160268844749e-137_d)    
f31                 0xd565739757eda398(-2.402297360108333e+103_d)   0xd565739757eda398(-2.402297360108333e+103_d)   
STATES DIFFER: True
```

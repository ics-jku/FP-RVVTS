# FailID_000764 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 764
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0xfd,0xe6,0xec,0x1b,0x6e,0xe9,0xb5,0xbf
_reg_f1: .byte 0x63,0xf8,0xd2,0xe3,0xd3,0xcc,0x9e,0x80
_reg_f2: .byte 0xb5,0x84,0x56,0x64,0x60,0x14,0xae,0x90
_reg_f3: .byte 0x6f,0x1a,0x4a,0x3a,0xb0,0x57,0x27,0xa7
_reg_f4: .byte 0x67,0xdb,0xdb,0xcd,0xef,0x80,0x5a,0xec
_reg_f5: .byte 0x98,0x3b,0xfe,0x8a,0x1e,0xcc,0xb4,0xd0
_reg_f6: .byte 0x48,0x04,0x81,0xaf,0xb0,0x68,0x81,0x9a
_reg_f7: .byte 0x64,0x06,0xa6,0xa4,0x1e,0xc3,0xfd,0x80
_reg_f8: .byte 0x0b,0x8a,0xae,0x7b,0x89,0x93,0x2c,0x06
_reg_f9: .byte 0x75,0x4d,0xdc,0x4e,0x42,0xbb,0x38,0x39
_reg_f10:.byte 0xa4,0xb3,0x9c,0x74,0x37,0x3e,0x68,0xf3
_reg_f11:.byte 0x72,0x71,0x50,0xb9,0x52,0xfd,0x89,0x16
_reg_f12:.byte 0xe8,0xb9,0xa6,0xf3,0xca,0xec,0x48,0xb8
_reg_f13:.byte 0xde,0x57,0x25,0x84,0x09,0xdf,0x3b,0x42
_reg_f14:.byte 0x8d,0x30,0xe2,0x54,0xa5,0x5d,0x2f,0x48
_reg_f15:.byte 0xe2,0xbd,0x7c,0xbe,0xe9,0x95,0x2d,0xba
_reg_f16:.byte 0xe6,0xa6,0xce,0x8e,0xeb,0x15,0x0f,0x9e
_reg_f17:.byte 0xa4,0xa1,0x8d,0x97,0xa8,0xcd,0x42,0x70
_reg_f18:.byte 0x41,0x79,0xee,0x43,0x56,0x2a,0xea,0x8f
_reg_f19:.byte 0xa4,0x72,0xef,0xad,0xc5,0xd7,0x58,0xd1
_reg_f20:.byte 0xac,0xd7,0xef,0x99,0xc8,0x1c,0x81,0x62
_reg_f21:.byte 0x5a,0xd5,0x50,0x07,0xbb,0x02,0xbd,0xdc
_reg_f22:.byte 0xd7,0x6d,0x3f,0x92,0x80,0x30,0x29,0xa8
_reg_f23:.byte 0xd2,0x3d,0x15,0x62,0x04,0x8d,0x7f,0xd3
_reg_f24:.byte 0x35,0xaa,0xe1,0x84,0x22,0xeb,0x75,0x47
_reg_f25:.byte 0x1d,0xb7,0x27,0x2d,0xb2,0x99,0x1d,0xbe
_reg_f26:.byte 0xf1,0x1d,0xc6,0xc0,0x6c,0x13,0x42,0x33
_reg_f27:.byte 0xc7,0xe2,0x55,0x9b,0x98,0x8c,0xa9,0xa3
_reg_f28:.byte 0xb3,0xd0,0x12,0x55,0x41,0x76,0xb2,0x60
_reg_f29:.byte 0xc3,0x9e,0x9d,0x84,0x5a,0x5d,0xfc,0xf7
_reg_f30:.byte 0x14,0x5f,0x58,0x35,0x68,0x81,0x59,0x04
_reg_f31:.byte 0x69,0xc5,0x9b,0xae,0xfa,0xe5,0xae,0x91
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'res0(0b101)', 'res': 0}
    li t0, 0xa0
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80254fd0            // ra
    li x2, 0x8018060a            // sp
    li x3, 0x2372e8970dce21f6    // gp
    li x4, 0xf08b55e40617cd4e    // tp
    li x5, 0x6325ccf957335213    // t0
    li x6, 0x78811c7f1603d0ba    // t1
    li x7, 0xaf1911d3f819d5b6    // t2
    li x8, 0xdc75c3fb4072e221    // fp
    li x9, 0xaf5e14a21c1d516b    // s1
    li x10, 0xfaef0a71889665d4   // a0
    li x11, 0x303651b2dcac6008   // a1
    li x12, 0x52eeb0d071eaa112   // a2
    li x13, 0xb283b623b050cc18   // a3
    li x14, 0x8fb2a84ac0d1b1f3   // a4
    li x15, 0xf9089a5631f108bd   // a5
    li x16, 0x15708ee83dda2325   // a6
    li x17, 0x9dedc23b947d3146   // a7
    li x18, 0xf6bda6794cc3f6ac   // s2
    li x19, 0xfac198f8d6779073   // s3
    li x20, 0x3a51b5a47c1cb18b   // s4
    li x21, 0x45ccd85a775a228f   // s5
    li x22, 0x7a3fe6313ee66f43   // s6
    li x23, 0x6000               // s7
    li x24, 0x64f6b38af23fba7c   // s8
    li x25, 0x6d9ab43939786c8f   // s9
    li x26, 0x195356e07a0edd25   // s10
    li x27, 0xd950a1fda33d1418   // s11
    li x28, 0x8a13e14f7807343d   // t3
    li x29, 0xd081823225ead480   // t4
    li x30, 0x764d9b1ab234964e   // t5
    li x31, 0xf28166a54991e553   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x25'}, 'clob': {'x2', 'x25', 'f15'}})
    
    li x2, 0x1ffff8
    and x25, x25, x2
    li x2, 0x7ffffdb3
    add x25, x25, x2
    fld f15, 0x24d(x25)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f15                 0xba2d95e9be7cbde2(-1.8671137233841021e-28_d)   0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f15, 0x24d(x25)
+========================================================================================================================+
Attributes:  special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f15                 0xba2d95e9be7cbde2(-1.8671137233841021e-28_d)   0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f15, x24, x25
s8(x24)             0x64f6b38af23fba7c(7275199657414736508)         0x64f6b38af23fba7c(7275199657414736508)
s9(x25)             0x0000000080186a3b(2149083707)                  0x0000000080186a3b(2149083707)
f15                 0xba2d95e9be7cbde2(-1.8671137233841021e-28_d)   0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080254fd0(2149928912)                  0x0000000080254fd0(2149928912)                  
sp(x2)              0x000000007ffffdb3(2147483059)                  0x000000007ffffdb3(2147483059)                  
gp(x3)              0x2372e8970dce21f6(2554359674141811190)         0x2372e8970dce21f6(2554359674141811190)         
tp(x4)              0xf08b55e40617cd4e(17333042028708613454)        0xf08b55e40617cd4e(17333042028708613454)        
t0(x5)              0x6325ccf957335213(7144341755175064083)         0x6325ccf957335213(7144341755175064083)         
t1(x6)              0x78811c7f1603d0ba(8683252888702800058)         0x78811c7f1603d0ba(8683252888702800058)         
t2(x7)              0xaf1911d3f819d5b6(12617135433153369526)        0xaf1911d3f819d5b6(12617135433153369526)        
fp(x8)              0xdc75c3fb4072e221(15885818744504771105)        0xdc75c3fb4072e221(15885818744504771105)        
s1(x9)              0xaf5e14a21c1d516b(12636560290937131371)        0xaf5e14a21c1d516b(12636560290937131371)        
a0(x10)             0xfaef0a71889665d4(18081682511654970836)        0xfaef0a71889665d4(18081682511654970836)        
a1(x11)             0x303651b2dcac6008(3474053991211229192)         0x303651b2dcac6008(3474053991211229192)         
a2(x12)             0x52eeb0d071eaa112(5975908164878115090)         0x52eeb0d071eaa112(5975908164878115090)         
a3(x13)             0xb283b623b050cc18(12863325225098464280)        0xb283b623b050cc18(12863325225098464280)        
a4(x14)             0x8fb2a84ac0d1b1f3(10354523532294205939)        0x8fb2a84ac0d1b1f3(10354523532294205939)        
a5(x15)             0xf9089a5631f108bd(17944762410253486269)        0xf9089a5631f108bd(17944762410253486269)        
a6(x16)             0x15708ee83dda2325(1544891800309343013)         0x15708ee83dda2325(1544891800309343013)         
a7(x17)             0x9dedc23b947d3146(11379965394585203014)        0x9dedc23b947d3146(11379965394585203014)        
s2(x18)             0xf6bda6794cc3f6ac(17779549943837750956)        0xf6bda6794cc3f6ac(17779549943837750956)        
s3(x19)             0xfac198f8d6779073(18068891374504611955)        0xfac198f8d6779073(18068891374504611955)        
s4(x20)             0x3a51b5a47c1cb18b(4202339645374902667)         0x3a51b5a47c1cb18b(4202339645374902667)         
s5(x21)             0x45ccd85a775a228f(5029632766927053455)         0x45ccd85a775a228f(5029632766927053455)         
s6(x22)             0x7a3fe6313ee66f43(8809012495343054659)         0x7a3fe6313ee66f43(8809012495343054659)         
s7(x23)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s8(x24)             0x64f6b38af23fba7c(7275199657414736508)         0x64f6b38af23fba7c(7275199657414736508)         
s9(x25)             0x0000000080186a3b(2149083707)                  0x0000000080186a3b(2149083707)                  
s10(x26)            0x195356e07a0edd25(1824897796135640357)         0x195356e07a0edd25(1824897796135640357)         
s11(x27)            0xd950a1fda33d1418(15659194015104701464)        0xd950a1fda33d1418(15659194015104701464)        
t3(x28)             0x8a13e14f7807343d(9949543733223961661)         0x8a13e14f7807343d(9949543733223961661)         
t4(x29)             0xd081823225ead480(15024432983780807808)        0xd081823225ead480(15024432983780807808)        
t5(x30)             0x764d9b1ab234964e(8524640208643462734)         0x764d9b1ab234964e(8524640208643462734)         
t6(x31)             0xf28166a54991e553(17474360889264170323)        0xf28166a54991e553(17474360889264170323)        

STATE               REF                                             DUT                                             DIFF
xmemhash            ac1dcfa141677837dbd33558a8258473ae192938        ac1dcfa141677837dbd33558a8258473ae192938        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800009b8(2147486136)                  0x00000000800009b8(2147486136)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000a0(160)                         0x00000000000000a0(160)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            res0(0b101)                                     res0(0b101)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xbfb5e96e1bece6fd(-0.08559311086437656_d)      0xbfb5e96e1bece6fd(-0.08559311086437656_d)      
f1                  0x809eccd3e3d2f863(-1.096520248945855e-305_d)   0x809eccd3e3d2f863(-1.096520248945855e-305_d)   
f2                  0x90ae1460645684b5(-2.4799635409157955e-228_d)  0x90ae1460645684b5(-2.4799635409157955e-228_d)  
f3                  0xa72757b03a4a1a6f(-4.519805184092313e-120_d)   0xa72757b03a4a1a6f(-4.519805184092313e-120_d)   
f4                  0xec5a80efcddbdb67(-8.922422327253703e+213_d)   0xec5a80efcddbdb67(-8.922422327253703e+213_d)   
f5                  0xd0b4cc1e8afe3b98(-6.164908980644741e+80_d)    0xd0b4cc1e8afe3b98(-6.164908980644741e+80_d)    
f6                  0x9a8168b0af810448(-5.24427060181557e-181_d)    0x9a8168b0af810448(-5.24427060181557e-181_d)    
f7                  0x80fdc31ea4a60664(-6.7812416275780535e-304_d)  0x80fdc31ea4a60664(-6.7812416275780535e-304_d)  
f8                  0x062c93897bae8a0b(6.297095454849657e-279_d)    0x062c93897bae8a0b(6.297095454849657e-279_d)    
f9                  0x3938bb424edc4d75(4.7631098922784594e-33_d)    0x3938bb424edc4d75(4.7631098922784594e-33_d)    
f10                 0xf3683e37749cb3a4(-8.475267484973922e+247_d)   0xf3683e37749cb3a4(-8.475267484973922e+247_d)   
f11                 0x1689fd52b9507172(4.2441580038867603e-200_d)   0x1689fd52b9507172(4.2441580038867603e-200_d)   
f12                 0xb848eccaf3a6b9e8(-1.4649581771558187e-37_d)   0xb848eccaf3a6b9e8(-1.4649581771558187e-37_d)   
f13                 0x423bdf09842557de(119706059813.34323_d)        0x423bdf09842557de(119706059813.34323_d)        
f14                 0x482f5da554e2308d(5.3366150143908725e+39_d)    0x482f5da554e2308d(5.3366150143908725e+39_d)    
f15                 0xba2d95e9be7cbde2(-1.8671137233841021e-28_d)   0x0000000000000000(0.0_d)                       X
f16                 0x9e0f15eb8ecea6e6(-6.747641233925019e-164_d)   0x9e0f15eb8ecea6e6(-6.747641233925019e-164_d)   
f17                 0x7042cda8978da1a4(5.83850938161643e+232_d)     0x7042cda8978da1a4(5.83850938161643e+232_d)     
f18                 0x8fea2a5643ee7941(-5.2667217967246696e-232_d)  0x8fea2a5643ee7941(-5.2667217967246696e-232_d)  
f19                 0xd158d7c5adef72a4(-7.540851798102168e+83_d)    0xd158d7c5adef72a4(-7.540851798102168e+83_d)    
f20                 0x62811cc899efd7ac(3.153402842233095e+166_d)    0x62811cc899efd7ac(3.153402842233095e+166_d)    
f21                 0xdcbd02bb0750d55a(-5.398035380730259e+138_d)   0xdcbd02bb0750d55a(-5.398035380730259e+138_d)   
f22                 0xa8293080923f6dd7(-3.1964694534197797e-115_d)  0xa8293080923f6dd7(-3.1964694534197797e-115_d)  
f23                 0xd37f8d0462153dd2(-1.645317445822467e+94_d)    0xd37f8d0462153dd2(-1.645317445822467e+94_d)    
f24                 0x4775eb2284e1aa35(1.8209173626951743e+36_d)    0x4775eb2284e1aa35(1.8209173626951743e+36_d)    
f25                 0xbe1d99b22d27b71d(-1.7229685912554313e-09_d)   0xbe1d99b22d27b71d(-1.7229685912554313e-09_d)   
f26                 0x3342136cc0c61df1(8.788005166689937e-62_d)     0x3342136cc0c61df1(8.788005166689937e-62_d)     
f27                 0xa3a98c989b55e2c7(-6.865455375835811e-137_d)   0xa3a98c989b55e2c7(-6.865455375835811e-137_d)   
f28                 0x60b276415512d0b3(6.336872200806505e+157_d)    0x60b276415512d0b3(6.336872200806505e+157_d)    
f29                 0xf7fc5d5a849d9ec3(-9.365560029675865e+269_d)   0xf7fc5d5a849d9ec3(-9.365560029675865e+269_d)   
f30                 0x0459816835585f14(1.0468824837803315e-287_d)   0x0459816835585f14(1.0468824837803315e-287_d)   
f31                 0x91aee5faae9bc569(-1.6695083979352228e-223_d)  0x91aee5faae9bc569(-1.6695083979352228e-223_d)  
STATES DIFFER: True
```

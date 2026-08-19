# FailID_001040 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1040
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
_reg_f0: .byte 0xb0,0xc0,0x8b,0x4c,0xf7,0xd6,0x4a,0xf3
_reg_f1: .byte 0xe8,0xe6,0xc9,0x84,0xe7,0x77,0x0b,0x16
_reg_f2: .byte 0x25,0x37,0xf7,0xe3,0x83,0x6b,0x15,0x75
_reg_f3: .byte 0x88,0xa4,0xad,0x41,0x92,0x59,0xc9,0x03
_reg_f4: .byte 0x65,0xe1,0x6c,0x37,0xf7,0x3f,0xd4,0xed
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x5e,0x7f,0xa1,0xed,0x95,0x85,0x1b,0xf4
_reg_f7: .byte 0x50,0x93,0x69,0x57,0x3e,0xbd,0x54,0x81
_reg_f8: .byte 0x9b,0xe4,0x30,0x20,0x16,0x0c,0xe1,0x22
_reg_f9: .byte 0x4e,0x4a,0xe0,0xdc,0xac,0xaa,0x93,0x89
_reg_f10:.byte 0xfe,0x0c,0x05,0x6e,0x36,0x6a,0x91,0xa0
_reg_f11:.byte 0xbd,0xed,0x1a,0x91,0x0a,0x11,0x41,0xf4
_reg_f12:.byte 0xbf,0x0b,0xc8,0x5c,0x72,0xf9,0x61,0x90
_reg_f13:.byte 0xbc,0x2f,0x3f,0x6e,0x84,0x9f,0x8f,0xcf
_reg_f14:.byte 0xe4,0x31,0x25,0xc1,0x33,0x51,0x03,0x36
_reg_f15:.byte 0x94,0x85,0x6d,0xd4,0xf2,0xb0,0xd7,0x08
_reg_f16:.byte 0xa5,0x29,0x75,0x24,0xfc,0x3c,0x4c,0xc2
_reg_f17:.byte 0x3f,0x77,0xe3,0x6a,0xe8,0xbc,0xf4,0x37
_reg_f18:.byte 0xb6,0xd8,0xaa,0x6f,0xe6,0xed,0x3b,0x10
_reg_f19:.byte 0x96,0xdf,0x3b,0xdb,0x8d,0x46,0xa6,0x2e
_reg_f20:.byte 0xff,0x32,0x74,0x08,0x03,0xf3,0xb2,0xb2
_reg_f21:.byte 0xb0,0x16,0x49,0x53,0xc3,0x2f,0xd5,0x8b
_reg_f22:.byte 0x32,0x3a,0x9f,0xe4,0xc5,0x7f,0xd5,0x09
_reg_f23:.byte 0xab,0x8b,0xdc,0x54,0x5c,0xdf,0x7a,0xcb
_reg_f24:.byte 0xab,0xd7,0x5b,0x29,0x8d,0x26,0x10,0xff
_reg_f25:.byte 0xfd,0x6b,0x17,0x75,0xd2,0xa7,0xec,0xd2
_reg_f26:.byte 0xa3,0x6a,0x2e,0xdf,0x11,0x82,0x1d,0xe9
_reg_f27:.byte 0x07,0xf0,0xc5,0x81,0xbe,0x4c,0x74,0x4f
_reg_f28:.byte 0x26,0x37,0xf7,0xe3,0x83,0x6b,0x15,0x75
_reg_f29:.byte 0x1d,0x38,0x76,0xdc,0x70,0x75,0xef,0x06
_reg_f30:.byte 0x09,0x55,0xa2,0xaa,0x61,0x9b,0xe8,0x6f
_reg_f31:.byte 0xa7,0xca,0x5a,0xda,0x64,0x33,0xd0,0x0c
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

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017fd2a            // ra
    li x2, 0x800a2f78            // sp
    li x3, 0x3add2000            // gp
    li x4, 0x801ff728            // tp
    li x5, 0x802592b7            // t0
    li x6, 0x8017fecd            // t1
    li x7, 0x84                  // t2
    li x8, 0x7ffffcba            // fp
    li x9, 0x8005c55b            // s1
    li x10, 0x0                  // a0
    li x11, 0x5a                 // a1
    li x12, 0x8017f9b7           // a2
    li x13, 0x801fddbb           // a3
    li x14, 0x1                  // a4
    li x15, 0x8017fc01           // a5
    li x16, 0x0                  // a6
    li x17, 0xd4                 // a7
    li x18, 0xee                 // s2
    li x19, 0x8017fd78           // s3
    li x20, 0x800003f7           // s4
    li x21, 0x75341000           // s5
    li x22, 0x8018068c           // s6
    li x23, 0x8017ff4f           // s7
    li x24, 0x8017ff0b           // s8
    li x25, 0x7ffffc66           // s9
    li x26, 0x800004a3           // s10
    li x27, 0xfffffffffed57000   // s11
    li x28, 0x0                  // t3
    li x29, 0x801ffbc7000        // t4
    li x30, 0x800000df           // t5
    li x31, 0x801823f7           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x17'}, 'clob': {'f7', 'x17', 'x14'}})
    
    li x14, 0x1ffff8
    and x17, x17, x14
    li x14, 0x7ffff84b
    add x17, x17, x14
    fld f7, 0x7b5(x17)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f7                  0x8154bd3e57699350(-3.024245495733733e-302_d)   0x0f91bc230f81b823(1.1155585313355797e-233_d)   X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f7, 0x7b5(x17)
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f7                  0x8154bd3e57699350(-3.024245495733733e-302_d)   0x0f91bc230f81b823(1.1155585313355797e-233_d)   X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f7, x7, b5, x17
t2(x7)              0x0000000000000084(132)                         0x0000000000000084(132)
a7(x17)             0x000000007ffff91b(2147481883)                  0x000000007ffff91b(2147481883)
f7                  0x8154bd3e57699350(-3.024245495733733e-302_d)   0x0f91bc230f81b823(1.1155585313355797e-233_d)   X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fd2a(2149055786)                  0x000000008017fd2a(2149055786)                  
sp(x2)              0x00000000800a2f78(2148151160)                  0x00000000800a2f78(2148151160)                  
gp(x3)              0x000000003add2000(987570176)                   0x000000003add2000(987570176)                   
tp(x4)              0x00000000801ff728(2149578536)                  0x00000000801ff728(2149578536)                  
t0(x5)              0x00000000802592b7(2149946039)                  0x00000000802592b7(2149946039)                  
t1(x6)              0x000000008017fecd(2149056205)                  0x000000008017fecd(2149056205)                  
t2(x7)              0x0000000000000084(132)                         0x0000000000000084(132)                         
fp(x8)              0x000000007ffffcba(2147482810)                  0x000000007ffffcba(2147482810)                  
s1(x9)              0x000000008005c55b(2147861851)                  0x000000008005c55b(2147861851)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x000000000000005a(90)                          0x000000000000005a(90)                          
a2(x12)             0x000000008017f9b7(2149054903)                  0x000000008017f9b7(2149054903)                  
a3(x13)             0x00000000801fddbb(2149572027)                  0x00000000801fddbb(2149572027)                  
a4(x14)             0x000000007ffff84b(2147481675)                  0x000000007ffff84b(2147481675)                  
a5(x15)             0x000000008017fc01(2149055489)                  0x000000008017fc01(2149055489)                  
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x000000007ffff91b(2147481883)                  0x000000007ffff91b(2147481883)                  
s2(x18)             0x00000000000000ee(238)                         0x00000000000000ee(238)                         
s3(x19)             0x000000008017fd78(2149055864)                  0x000000008017fd78(2149055864)                  
s4(x20)             0x00000000800003f7(2147484663)                  0x00000000800003f7(2147484663)                  
s5(x21)             0x0000000075341000(1966346240)                  0x0000000075341000(1966346240)                  
s6(x22)             0x000000008018068c(2149058188)                  0x000000008018068c(2149058188)                  
s7(x23)             0x000000008017ff4f(2149056335)                  0x000000008017ff4f(2149056335)                  
s8(x24)             0x000000008017ff0b(2149056267)                  0x000000008017ff0b(2149056267)                  
s9(x25)             0x000000007ffffc66(2147482726)                  0x000000007ffffc66(2147482726)                  
s10(x26)            0x00000000800004a3(2147484835)                  0x00000000800004a3(2147484835)                  
s11(x27)            0xfffffffffed57000(18446744073689985024)        0xfffffffffed57000(18446744073689985024)        
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x00000801ffbc7000(8804678529024)               0x00000801ffbc7000(8804678529024)               
t5(x30)             0x00000000800000df(2147483871)                  0x00000000800000df(2147483871)                  
t6(x31)             0x00000000801823f7(2149065719)                  0x00000000801823f7(2149065719)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            4a57906a680acfbcf908e21ed5346fe25c356f16        4a57906a680acfbcf908e21ed5346fe25c356f16        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000764(2147485540)                  0x0000000080000764(2147485540)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000041(65)                          0x0000000000000041(65)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xf34ad6f74c8bc0b0(-2.3457638673490832e+247_d)  0xf34ad6f74c8bc0b0(-2.3457638673490832e+247_d)  
f1                  0x160b77e784c9e6e8(1.7522090433177816e-202_d)   0x160b77e784c9e6e8(1.7522090433177816e-202_d)   
f2                  0x75156b83e3f73725(1.005067935161446e+256_d)    0x75156b83e3f73725(1.005067935161446e+256_d)    
f3                  0x03c9599241ada488(2.0322177342009146e-290_d)   0x03c9599241ada488(2.0322177342009146e-290_d)   
f4                  0xedd43ff7376ce165(-1.1437180834794317e+221_d)  0xedd43ff7376ce165(-1.1437180834794317e+221_d)  
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xf41b8595eda17f5e(-1.9704868231073644e+251_d)  0xf41b8595eda17f5e(-1.9704868231073644e+251_d)  
f7                  0x8154bd3e57699350(-3.024245495733733e-302_d)   0x0f91bc230f81b823(1.1155585313355797e-233_d)   X
f8                  0x22e10c162030e49b(1.118369749095584e-140_d)    0x22e10c162030e49b(1.118369749095584e-140_d)    
f9                  0x8993aaacdce04a4e(-1.561403996397809e-262_d)   0x8993aaacdce04a4e(-1.561403996397809e-262_d)   
f10                 0xa0916a366e050cfe(-8.312717186065277e-152_d)   0xa0916a366e050cfe(-8.312717186065277e-152_d)   
f11                 0xf441110a911aedbd(-9.775355729472116e+251_d)   0xf441110a911aedbd(-9.775355729472116e+251_d)   
f12                 0x9061f9725cc80bbf(-9.262063416224988e-230_d)   0x9061f9725cc80bbf(-9.262063416224988e-230_d)   
f13                 0xcf8f9f846e3f2fbc(-1.7879426240184053e+75_d)   0xcf8f9f846e3f2fbc(-1.7879426240184053e+75_d)   
f14                 0x36035133c12531e4(1.6521702291655622e-48_d)    0x36035133c12531e4(1.6521702291655622e-48_d)    
f15                 0x08d7b0f2d46d8594(4.592096413228869e-266_d)    0x08d7b0f2d46d8594(4.592096413228869e-266_d)    
f16                 0xc24c3cfc247529a5(-242564483306.32535_d)       0xc24c3cfc247529a5(-242564483306.32535_d)       
f17                 0x37f4bce86ae3773f(3.808954603966837e-39_d)     0x37f4bce86ae3773f(3.808954603966837e-39_d)     
f18                 0x103bede66faad8b6(1.798967597600698e-230_d)    0x103bede66faad8b6(1.798967597600698e-230_d)    
f19                 0x2ea6468ddb3bdf96(5.733247221325006e-84_d)     0x2ea6468ddb3bdf96(5.733247221325006e-84_d)     
f20                 0xb2b2f303087432ff(-1.799340298271822e-64_d)    0xb2b2f303087432ff(-1.799340298271822e-64_d)    
f21                 0x8bd52fc3534916b0(-1.1559109331652503e-251_d)  0x8bd52fc3534916b0(-1.1559109331652503e-251_d)  
f22                 0x09d57fc5e49f3a32(2.7310164869327843e-261_d)   0x09d57fc5e49f3a32(2.7310164869327843e-261_d)   
f23                 0xcb7adf5c54dc8bab(-4.1181990432051295e+55_d)   0xcb7adf5c54dc8bab(-4.1181990432051295e+55_d)   
f24                 0xff10268d295bd7ab(-1.1075518562926623e+304_d)  0xff10268d295bd7ab(-1.1075518562926623e+304_d)  
f25                 0xd2eca7d275176bfd(-2.918619830470266e+91_d)    0xd2eca7d275176bfd(-2.918619830470266e+91_d)    
f26                 0xe91d8211df2e6aa3(-2.2057596759920065e+198_d)  0xe91d8211df2e6aa3(-2.2057596759920065e+198_d)  
f27                 0x4f744cbe81c5f007(5.738657611920474e+74_d)     0x4f744cbe81c5f007(5.738657611920474e+74_d)     
f28                 0x75156b83e3f73726(1.0050679351614462e+256_d)   0x75156b83e3f73726(1.0050679351614462e+256_d)   
f29                 0x06ef7570dc76381d(2.839458233206387e-275_d)    0x06ef7570dc76381d(2.839458233206387e-275_d)    
f30                 0x6fe89b61aaa25509(1.1938359087469714e+231_d)   0x6fe89b61aaa25509(1.1938359087469714e+231_d)   
f31                 0x0cd03364da5acaa7(5.792671351716269e-247_d)    0x0cd03364da5acaa7(5.792671351716269e-247_d)    
STATES DIFFER: True
```

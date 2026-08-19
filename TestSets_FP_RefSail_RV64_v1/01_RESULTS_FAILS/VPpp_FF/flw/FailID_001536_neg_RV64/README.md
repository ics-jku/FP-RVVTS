# FailID_001536 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1536
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
_reg_f0: .byte 0xc8,0xdb,0x0d,0x4f,0x12,0xfa,0xc9,0xfc
_reg_f1: .byte 0x5a,0x79,0x82,0x4f,0x2e,0x3a,0x42,0x27
_reg_f2: .byte 0x26,0x83,0xb4,0x6a,0xbd,0xdd,0x41,0xd5
_reg_f3: .byte 0x8c,0x08,0x96,0x48,0x85,0x7c,0x93,0x84
_reg_f4: .byte 0x11,0xb3,0x6c,0x25,0x9a,0xfd,0x64,0x64
_reg_f5: .byte 0xc9,0xd7,0x57,0xdb,0x8c,0x8c,0x97,0xfe
_reg_f6: .byte 0x9c,0xe5,0xa9,0x3b,0x2f,0xc2,0x0a,0x81
_reg_f7: .byte 0xd6,0x62,0x54,0xad,0x9b,0x11,0x0e,0x6d
_reg_f8: .byte 0x05,0xe1,0xc8,0xa9,0x55,0xba,0xe5,0x6e
_reg_f9: .byte 0xe9,0xb9,0xb5,0xe7,0x76,0x28,0x00,0xf6
_reg_f10:.byte 0x2c,0x91,0xec,0x3d,0x81,0x61,0xb6,0x48
_reg_f11:.byte 0x12,0xd8,0x0e,0xed,0x12,0x5b,0xce,0xb9
_reg_f12:.byte 0x7e,0xd5,0xcc,0x48,0x8a,0xba,0x22,0xc9
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0xcc,0x35,0xa1,0x0e,0x23,0x52,0xac,0x2e
_reg_f15:.byte 0x49,0x2c,0x32,0x33,0x61,0x83,0x13,0x28
_reg_f16:.byte 0x7b,0xac,0x8a,0x22,0x6c,0x4e,0xc6,0xeb
_reg_f17:.byte 0x52,0xa1,0x5b,0x70,0xa4,0xea,0xd3,0x69
_reg_f18:.byte 0x5b,0x1d,0x46,0xf9,0xec,0xd2,0xe2,0x43
_reg_f19:.byte 0x8c,0x08,0x96,0x48,0x85,0x7c,0x93,0x84
_reg_f20:.byte 0x3d,0x65,0xf7,0x0e,0x51,0xb6,0x32,0x6c
_reg_f21:.byte 0xd9,0x37,0x41,0x8e,0x5e,0xe5,0xdd,0x04
_reg_f22:.byte 0xd7,0xda,0x0e,0x33,0x81,0xf1,0x3e,0x2c
_reg_f23:.byte 0x9a,0x22,0x87,0x49,0xcc,0xd8,0xef,0xde
_reg_f24:.byte 0x3a,0x6f,0xe0,0x9c,0x6a,0x68,0x78,0x65
_reg_f25:.byte 0x41,0x66,0xbf,0x5a,0xaa,0xe0,0xfc,0xdd
_reg_f26:.byte 0x8d,0xd0,0xa9,0xf7,0xc3,0x9b,0xf8,0xec
_reg_f27:.byte 0x12,0xd8,0x0e,0xed,0x12,0x5b,0xce,0xb9
_reg_f28:.byte 0xa9,0xd8,0x52,0x6f,0x75,0x04,0x5c,0xb8
_reg_f29:.byte 0xb1,0x2f,0xc3,0xec,0x25,0x43,0x08,0xe1
_reg_f30:.byte 0x3a,0x01,0x3c,0x01,0xde,0x85,0xb5,0xa4
_reg_f31:.byte 0x2f,0x98,0xed,0xdc,0xdb,0x86,0xb3,0xb7
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
    li x1, 0x3f307649483561a0    // ra
    li x2, 0x80180513            // sp
    li x3, 0xd10c4857e64ab4c5    // gp
    li x4, 0x71bc6a3d1a8e86ec    // tp
    li x5, 0xb259154521fd274     // t0
    li x6, 0xa6aaf6b8d72eeec9    // t1
    li x7, 0x8013239e            // t2
    li x8, 0x6f26946bf0879cf2    // fp
    li x9, 0x80221b4b            // s1
    li x10, 0x0                  // a0
    li x11, 0xa3afbfe92a6f8d7c   // a1
    li x12, 0x22189b7fbea02b62   // a2
    li x13, 0xc956294aa77152cb   // a3
    li x14, 0x0                  // a4
    li x15, 0xbca0beb62131c0e6   // a5
    li x16, 0x7ffffaee           // a6
    li x17, 0x800003a2           // a7
    li x18, 0x7ffffa37           // s2
    li x19, 0x0                  // s3
    li x20, 0x6ad975f97db72060   // s4
    li x21, 0x5a31726bf7a14b23   // s5
    li x22, 0x0                  // s6
    li x23, 0xa6aaf6b8d72eeec9   // s7
    li x24, 0x51b023340191f3     // s8
    li x25, 0x801803eb           // s9
    li x26, 0x11dd027404479bc2   // s10
    li x27, 0x39                 // s11
    li x28, 0x51e785a49e7321b0   // t3
    li x29, 0xba453614e6ed675e   // t4
    li x30, 0x805f724d98f66de8   // t5
    li x31, 0x7ffffa37           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x30', 'mstatus.fs/vs.fs'}, 'clob': {'x30', 'f2', 'x23'}})
    
    li x23, 0x1ffffc
    and x30, x30, x23
    li x23, 0x80000422
    add x30, x30, x23
    flw f2, -0x422(x30)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f2                  0xd541ddbd6ab48326(-5.00195796594692e+102_d)    0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f2, -0x422(x30)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f2                  0xd541ddbd6ab48326(-5.00195796594692e+102_d)    0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f2, x422, x30
t5(x30)             0x000000008016720a(2148954634)                  0x000000008016720a(2148954634)
f2                  0xd541ddbd6ab48326(-5.00195796594692e+102_d)    0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x3f307649483561a0(4553269280387719584)         0x3f307649483561a0(4553269280387719584)         
sp(x2)              0x0000000080180513(2149057811)                  0x0000000080180513(2149057811)                  
gp(x3)              0xd10c4857e64ab4c5(15063494396010476741)        0xd10c4857e64ab4c5(15063494396010476741)        
tp(x4)              0x71bc6a3d1a8e86ec(8195542232578557676)         0x71bc6a3d1a8e86ec(8195542232578557676)         
t0(x5)              0x0b259154521fd274(803207899896599156)          0x0b259154521fd274(803207899896599156)          
t1(x6)              0xa6aaf6b8d72eeec9(12009682630081441481)        0xa6aaf6b8d72eeec9(12009682630081441481)        
t2(x7)              0x000000008013239e(2148737950)                  0x000000008013239e(2148737950)                  
fp(x8)              0x6f26946bf0879cf2(8009252178642836722)         0x6f26946bf0879cf2(8009252178642836722)         
s1(x9)              0x0000000080221b4b(2149718859)                  0x0000000080221b4b(2149718859)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0xa3afbfe92a6f8d7c(11794856957266857340)        0xa3afbfe92a6f8d7c(11794856957266857340)        
a2(x12)             0x22189b7fbea02b62(2456884569691925346)         0x22189b7fbea02b62(2456884569691925346)         
a3(x13)             0xc956294aa77152cb(14507828650234172107)        0xc956294aa77152cb(14507828650234172107)        
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0xbca0beb62131c0e6(13592073364854391014)        0xbca0beb62131c0e6(13592073364854391014)        
a6(x16)             0x000000007ffffaee(2147482350)                  0x000000007ffffaee(2147482350)                  
a7(x17)             0x00000000800003a2(2147484578)                  0x00000000800003a2(2147484578)                  
s2(x18)             0x000000007ffffa37(2147482167)                  0x000000007ffffa37(2147482167)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x6ad975f97db72060(7699314752383033440)         0x6ad975f97db72060(7699314752383033440)         
s5(x21)             0x5a31726bf7a14b23(6499101545313946403)         0x5a31726bf7a14b23(6499101545313946403)         
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000080000422(2147484706)                  0x0000000080000422(2147484706)                  
s8(x24)             0x0051b023340191f3(22993138356425203)           0x0051b023340191f3(22993138356425203)           
s9(x25)             0x00000000801803eb(2149057515)                  0x00000000801803eb(2149057515)                  
s10(x26)            0x11dd027404479bc2(1287187765809093570)         0x11dd027404479bc2(1287187765809093570)         
s11(x27)            0x0000000000000039(57)                          0x0000000000000039(57)                          
t3(x28)             0x51e785a49e7321b0(5901832778771800496)         0x51e785a49e7321b0(5901832778771800496)         
t4(x29)             0xba453614e6ed675e(13422193727849195358)        0xba453614e6ed675e(13422193727849195358)        
t5(x30)             0x000000008016720a(2148954634)                  0x000000008016720a(2148954634)                  
t6(x31)             0x000000007ffffa37(2147482167)                  0x000000007ffffa37(2147482167)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            364027d85512aa33971caec4fb78487c1ba4edf6        364027d85512aa33971caec4fb78487c1ba4edf6        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800008c8(2147485896)                  0x00000000800008c8(2147485896)                  
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
f0                  0xfcc9fa124f0ddbc8(-1.2961407029736988e+293_d)  0xfcc9fa124f0ddbc8(-1.2961407029736988e+293_d)  
f1                  0x27423a2e4f82795a(1.4117355022935317e-119_d)   0x27423a2e4f82795a(1.4117355022935317e-119_d)   
f2                  0xd541ddbd6ab48326(-5.00195796594692e+102_d)    0xffffffff00000000(0.0_s)                       X
f3                  0x84937c854896088c(-1.2797229091309842e-286_d)  0x84937c854896088c(-1.2797229091309842e-286_d)  
f4                  0x6464fd9a256cb311(4.153297415777152e+175_d)    0x6464fd9a256cb311(4.153297415777152e+175_d)    
f5                  0xfe978c8cdb57d7c9(-6.30824555823432e+301_d)    0xfe978c8cdb57d7c9(-6.30824555823432e+301_d)    
f6                  0x810ac22f3ba9e59c(-1.219373317289968e-303_d)   0x810ac22f3ba9e59c(-1.219373317289968e-303_d)   
f7                  0x6d0e119bad5462d6(2.073111797459765e+217_d)    0x6d0e119bad5462d6(2.073111797459765e+217_d)    
f8                  0x6ee5ba55a9c8e105(1.60851052701873e+226_d)     0x6ee5ba55a9c8e105(1.60851052701873e+226_d)     
f9                  0xf6002876e7b5b9e9(-2.4843661314912884e+260_d)  0xf6002876e7b5b9e9(-2.4843661314912884e+260_d)  
f10                 0x48b661813dec912c(1.9496494720297714e+42_d)    0x48b661813dec912c(1.9496494720297714e+42_d)    
f11                 0xb9ce5b12ed0ed812(-2.9933087962580927e-30_d)   0xb9ce5b12ed0ed812(-2.9933087962580927e-30_d)   
f12                 0xc922ba8a48ccd57e(-2.0883167724573405e+44_d)   0xc922ba8a48ccd57e(-2.0883167724573405e+44_d)   
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x2eac52230ea135cc(7.289159656324523e-84_d)     0x2eac52230ea135cc(7.289159656324523e-84_d)     
f15                 0x2813836133322c49(1.238084287307389e-115_d)    0x2813836133322c49(1.238084287307389e-115_d)    
f16                 0xebc64e6c228aac7b(-1.4666795844777929e+211_d)  0xebc64e6c228aac7b(-1.4666795844777929e+211_d)  
f17                 0x69d3eaa4705ba152(6.098060025322928e+201_d)    0x69d3eaa4705ba152(6.098060025322928e+201_d)    
f18                 0x43e2d2ecf9461d5b(1.0851255945274251e+19_d)    0x43e2d2ecf9461d5b(1.0851255945274251e+19_d)    
f19                 0x84937c854896088c(-1.2797229091309842e-286_d)  0x84937c854896088c(-1.2797229091309842e-286_d)  
f20                 0x6c32b6510ef7653d(1.5748572818464752e+213_d)   0x6c32b6510ef7653d(1.5748572818464752e+213_d)   
f21                 0x04dde55e8e4137d9(3.1413536184395884e-285_d)   0x04dde55e8e4137d9(3.1413536184395884e-285_d)   
f22                 0x2c3ef181330edad7(1.4486687960511741e-95_d)    0x2c3ef181330edad7(1.4486687960511741e-95_d)    
f23                 0xdeefd8cc4987229a(-2.0360788262388952e+149_d)  0xdeefd8cc4987229a(-2.0360788262388952e+149_d)  
f24                 0x6578686a9ce06f3a(6.330054044447038e+180_d)    0x6578686a9ce06f3a(6.330054044447038e+180_d)    
f25                 0xddfce0aa5abf6641(-5.634287754581439e+144_d)   0xddfce0aa5abf6641(-5.634287754581439e+144_d)   
f26                 0xecf89bc3f7a9d08d(-8.483231402566356e+216_d)   0xecf89bc3f7a9d08d(-8.483231402566356e+216_d)   
f27                 0xb9ce5b12ed0ed812(-2.9933087962580927e-30_d)   0xb9ce5b12ed0ed812(-2.9933087962580927e-30_d)   
f28                 0xb85c04756f52d8a9(-3.29343153067166e-37_d)     0xb85c04756f52d8a9(-3.29343153067166e-37_d)     
f29                 0xe1084325ecc32fb1(-2.664892202835564e+159_d)   0xe1084325ecc32fb1(-2.664892202835564e+159_d)   
f30                 0xa4b585de013c013a(-7.580591157515816e-132_d)   0xa4b585de013c013a(-7.580591157515816e-132_d)   
f31                 0xb7b386dbdced982f(-2.241565829008574e-40_d)    0xb7b386dbdced982f(-2.241565829008574e-40_d)    
STATES DIFFER: True
```

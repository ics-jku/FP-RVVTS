# FailID_004803 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4803
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
_reg_f0: .byte 0xd3,0x0a,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f1: .byte 0xce,0x10,0x73,0x12,0x5a,0x17,0xe7,0x4e
_reg_f2: .byte 0x8a,0x38,0xf9,0xb8,0x94,0x5a,0x4d,0x8e
_reg_f3: .byte 0x3a,0x77,0x51,0x1f,0x9c,0x56,0xea,0xf6
_reg_f4: .byte 0x67,0xa3,0x80,0x82,0xed,0x7a,0xea,0x30
_reg_f5: .byte 0x0c,0xc6,0x60,0x5d,0xfc,0xbd,0xb4,0xde
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x5c,0xe6,0xd2,0x1a,0x3d,0x6c,0xc4,0x6d
_reg_f8: .byte 0x03,0xae,0x07,0x1f,0x9a,0x48,0x48,0xaa
_reg_f9: .byte 0xef,0xba,0x0a,0xcb,0xff,0xde,0x3e,0x73
_reg_f10:.byte 0xbe,0xab,0xb2,0xfd,0xb8,0xa7,0x1b,0x13
_reg_f11:.byte 0xa3,0x41,0xed,0x65,0x68,0x4b,0x08,0xc8
_reg_f12:.byte 0xce,0x10,0x73,0x12,0x5a,0x17,0xe7,0x4e
_reg_f13:.byte 0x00,0x00,0x60,0x72,0xc0,0x5a,0xef,0x41
_reg_f14:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x57,0xa2,0x73,0x0b,0x9c,0x3d,0xa7,0xc0
_reg_f16:.byte 0x84,0x9c,0x7c,0x7e,0xe5,0xc3,0x3c,0x95
_reg_f17:.byte 0x62,0x69,0xc0,0x9f,0x89,0x79,0x90,0xe5
_reg_f18:.byte 0x71,0x6f,0xfe,0x9b,0x9b,0x86,0x65,0xf8
_reg_f19:.byte 0x03,0x4b,0x66,0x8f,0x05,0x93,0xb5,0x61
_reg_f20:.byte 0x26,0x0f,0xe0,0x9d,0x6d,0x79,0x5c,0x9d
_reg_f21:.byte 0x3d,0x73,0xcf,0x54,0xf5,0xd9,0x87,0xb8
_reg_f22:.byte 0xd7,0xe0,0x32,0x5d,0x7e,0xd0,0x32,0x36
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f25:.byte 0x89,0xa5,0xe7,0xc8,0x5d,0x29,0x57,0x4c
_reg_f26:.byte 0xa3,0x41,0xed,0x65,0x68,0x4b,0x08,0xc8
_reg_f27:.byte 0x74,0x05,0xbb,0xeb,0xca,0xa4,0x92,0x90
_reg_f28:.byte 0xba,0x6c,0x66,0x23,0xbd,0x5d,0x9c,0x86
_reg_f29:.byte 0x85,0x81,0xe7,0xa5,0x0f,0x26,0xfc,0x95
_reg_f30:.byte 0xc5,0xfc,0x81,0x33,0xdc,0x2b,0xa4,0xf7
_reg_f31:.byte 0xbf,0x1c,0x28,0xc3,0x10,0x10,0x10,0xc8
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x1
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7ffff8dd            // ra
    li x2, 0x801864f5            // sp
    li x3, 0x6000                // gp
    li x4, 0x80028984            // tp
    li x5, 0xa4                  // t0
    li x6, 0x801804f5            // t1
    li x7, 0x800000fa            // t2
    li x8, 0xc6dac774            // fp
    li x9, 0x7ffffe24            // s1
    li x10, 0x801ffed1           // a0
    li x11, 0x7ffffa5d           // a1
    li x12, 0x8016bfbd           // a2
    li x13, 0x80180148           // a3
    li x14, 0x6000               // a4
    li x15, 0x80185b3a           // a5
    li x16, 0x1                  // a6
    li x17, 0x800ab0ba           // a7
    li x18, 0x8017ff09           // s2
    li x19, 0x0                  // s3
    li x20, 0x638aa744           // s4
    li x21, 0x75                 // s5
    li x22, 0x11                 // s6
    li x23, 0x0                  // s7
    li x24, 0x7ffffc08           // s8
    li x25, 0x8015fdef           // s9
    li x26, 0x801b7121           // s10
    li x27, 0x800aeda0           // s11
    li x28, 0xc9                 // t3
    li x29, 0x6000               // t4
    li x30, 0x7ffff924           // t5
    li x31, 0x80000104           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f19', 'x7'}, 'clob': {'x13', 'x7'}})
    
    li x13, 0xffffc
    and x7, x7, x13
    li x13, 0x80180605
    add x7, x7, x13
    fsw f19, -0x605(x7)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        0398b105052f27719179e048d83d02ab3ff560d1        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f19, -0x605(x7)
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        0398b105052f27719179e048d83d02ab3ff560d1        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f19, x605, x7
t2(x7)              0x00000000801806fd(2149058301)                  0x00000000801806fd(2149058301)
f19                 0x61b593058f664b03(4.853046601711578e+162_d)    0x61b593058f664b03(4.853046601711578e+162_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffff8dd(2147481821)                  0x000000007ffff8dd(2147481821)                  
sp(x2)              0x00000000801864f5(2149082357)                  0x00000000801864f5(2149082357)                  
gp(x3)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
tp(x4)              0x0000000080028984(2147649924)                  0x0000000080028984(2147649924)                  
t0(x5)              0x00000000000000a4(164)                         0x00000000000000a4(164)                         
t1(x6)              0x00000000801804f5(2149057781)                  0x00000000801804f5(2149057781)                  
t2(x7)              0x00000000801806fd(2149058301)                  0x00000000801806fd(2149058301)                  
fp(x8)              0x00000000c6dac774(3336226676)                  0x00000000c6dac774(3336226676)                  
s1(x9)              0x000000007ffffe24(2147483172)                  0x000000007ffffe24(2147483172)                  
a0(x10)             0x00000000801ffed1(2149580497)                  0x00000000801ffed1(2149580497)                  
a1(x11)             0x000000007ffffa5d(2147482205)                  0x000000007ffffa5d(2147482205)                  
a2(x12)             0x000000008016bfbd(2148974525)                  0x000000008016bfbd(2148974525)                  
a3(x13)             0x0000000080180605(2149058053)                  0x0000000080180605(2149058053)                  
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x0000000080185b3a(2149079866)                  0x0000000080185b3a(2149079866)                  
a6(x16)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a7(x17)             0x00000000800ab0ba(2148184250)                  0x00000000800ab0ba(2148184250)                  
s2(x18)             0x000000008017ff09(2149056265)                  0x000000008017ff09(2149056265)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x00000000638aa744(1670031172)                  0x00000000638aa744(1670031172)                  
s5(x21)             0x0000000000000075(117)                         0x0000000000000075(117)                         
s6(x22)             0x0000000000000011(17)                          0x0000000000000011(17)                          
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x000000007ffffc08(2147482632)                  0x000000007ffffc08(2147482632)                  
s9(x25)             0x000000008015fdef(2148924911)                  0x000000008015fdef(2148924911)                  
s10(x26)            0x00000000801b7121(2149282081)                  0x00000000801b7121(2149282081)                  
s11(x27)            0x00000000800aeda0(2148199840)                  0x00000000800aeda0(2148199840)                  
t3(x28)             0x00000000000000c9(201)                         0x00000000000000c9(201)                         
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x000000007ffff924(2147481892)                  0x000000007ffff924(2147481892)                  
t6(x31)             0x0000000080000104(2147483908)                  0x0000000080000104(2147483908)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            08646d0a9e4a66205ed4b79ada41bf6beeee97b0        08646d0a9e4a66205ed4b79ada41bf6beeee97b0        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        0398b105052f27719179e048d83d02ab3ff560d1        X
lastPC              0x0000000080000758(2147485528)                  0x0000000080000758(2147485528)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000001(1)                           0x0000000000000001(1)                           
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffffffff0ad3(0.00020825862884521484_h)    0xffffffffffff0ad3(0.00020825862884521484_h)    
f1                  0x4ee7175a127310ce(1.2749578435636118e+72_d)    0x4ee7175a127310ce(1.2749578435636118e+72_d)    
f2                  0x8e4d5a94b8f9388a(-8.804369613034713e-240_d)   0x8e4d5a94b8f9388a(-8.804369613034713e-240_d)   
f3                  0xf6ea569c1f51773a(-6.634898317711435e+264_d)   0xf6ea569c1f51773a(-6.634898317711435e+264_d)   
f4                  0x30ea7aed8280a367(4.68351702933114e-73_d)      0x30ea7aed8280a367(4.68351702933114e-73_d)      
f5                  0xdeb4bdfc5d60c60c(-1.6576440472835102e+148_d)  0xdeb4bdfc5d60c60c(-1.6576440472835102e+148_d)  
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x6dc46c3d1ad2e65c(5.767429313112931e+220_d)    0x6dc46c3d1ad2e65c(5.767429313112931e+220_d)    
f8                  0xaa48489a1f07ae03(-5.294008362103327e-105_d)   0xaa48489a1f07ae03(-5.294008362103327e-105_d)   
f9                  0x733edeffcb0abaef(1.349051204474506e+247_d)    0x733edeffcb0abaef(1.349051204474506e+247_d)    
f10                 0x131ba7b8fdb2abbe(1.253485769659883e-216_d)    0x131ba7b8fdb2abbe(1.253485769659883e-216_d)    
f11                 0xc8084b6865ed41a3(-1.0333763714975547e+39_d)   0xc8084b6865ed41a3(-1.0333763714975547e+39_d)   
f12                 0x4ee7175a127310ce(1.2749578435636118e+72_d)    0x4ee7175a127310ce(1.2749578435636118e+72_d)    
f13                 0x41ef5ac072600000(4208329619.0_d)              0x41ef5ac072600000(4208329619.0_d)              
f14                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f15                 0xc0a73d9c0b73a257(-2974.8047748695058_d)       0xc0a73d9c0b73a257(-2974.8047748695058_d)       
f16                 0x953cc3e57e7c9c84(-2.2399106332191008e-206_d)  0x953cc3e57e7c9c84(-2.2399106332191008e-206_d)  
f17                 0xe59079899fc06962(-1.70905643633674e+181_d)    0xe59079899fc06962(-1.70905643633674e+181_d)    
f18                 0xf865869b9bfe6f71(-9.09757496835836e+271_d)    0xf865869b9bfe6f71(-9.09757496835836e+271_d)    
f19                 0x61b593058f664b03(4.853046601711578e+162_d)    0x61b593058f664b03(4.853046601711578e+162_d)    
f20                 0x9d5c796d9de00f26(-3.017976933827193e-167_d)   0x9d5c796d9de00f26(-3.017976933827193e-167_d)   
f21                 0xb887d9f554cf733d(-2.24297484931534e-36_d)     0xb887d9f554cf733d(-2.24297484931534e-36_d)     
f22                 0x3632d07e5d32e0d7(1.2873354146123362e-47_d)    0x3632d07e5d32e0d7(1.2873354146123362e-47_d)    
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f25                 0x4c57295dc8e7a589(5.8155055914587485e+59_d)    0x4c57295dc8e7a589(5.8155055914587485e+59_d)    
f26                 0xc8084b6865ed41a3(-1.0333763714975547e+39_d)   0xc8084b6865ed41a3(-1.0333763714975547e+39_d)   
f27                 0x9092a4caebbb0574(-7.68556689151021e-229_d)    0x9092a4caebbb0574(-7.68556689151021e-229_d)    
f28                 0x869c5dbd23666cba(-8.001007128548176e-277_d)   0x869c5dbd23666cba(-8.001007128548176e-277_d)   
f29                 0x95fc260fa5e78185(-8.978027008110316e-203_d)   0x95fc260fa5e78185(-8.978027008110316e-203_d)   
f30                 0xf7a42bdc3381fcc5(-2.0813286457650433e+268_d)  0xf7a42bdc3381fcc5(-2.0813286457650433e+268_d)  
f31                 0xc8101010c3281cbf(-1.3664681384163016e+39_d)   0xc8101010c3281cbf(-1.3664681384163016e+39_d)   
STATES DIFFER: True
```

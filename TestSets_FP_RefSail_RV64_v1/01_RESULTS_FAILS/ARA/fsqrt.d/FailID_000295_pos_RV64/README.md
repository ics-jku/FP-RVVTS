# FailID_000295 ARA pos RV64 fsqrt.d

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 295
* Isolated failing instruction: `fsqrt.d`
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
_reg_f0: .byte 0x36,0x56,0x15,0xfd,0xe9,0x15,0x73,0xf9
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0xc1,0x64,0x70,0x5f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0xea,0x45,0xc0,0x3d,0x0b,0xd1,0xe9,0xc2
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f5: .byte 0x27,0x1a,0xcc,0x8b,0x9f,0x57,0xc6,0xf9
_reg_f6: .byte 0xb0,0x0b,0x62,0xcf,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0xc1,0x5f,0x27,0xbf,0x22,0x0e,0x83,0x6c
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x90,0x61,0x0a,0xc2,0xef,0x1a,0x86,0x29
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x3f,0x10,0x21,0x6f,0x8c,0xcf,0xdf,0xfd
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x90,0x61,0x0a,0xc2,0xef,0x1a,0x86,0x29
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0xc4,0xfe,0x4b,0x75,0x00,0x71,0x80,0x1e
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xc4,0xfe,0x4b,0x75,0x00,0x71,0x80,0x9e
_reg_f22:.byte 0x00,0x00,0xc0,0xca,0x00,0x00,0xe0,0x41
_reg_f23:.byte 0x00,0x00,0x00,0xdf,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x80,0xa9,0x2b,0xfd,0xdf,0xc1
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x55,0xe7,0x8a,0x20,0x38,0x47,0xf4,0x20
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017fddc            // ra
    li x2, 0x8017fe7c            // sp
    li x3, 0x800005d4            // gp
    li x4, 0x1                   // tp
    li x5, 0x8007b28f            // t0
    li x6, 0xe0167860c4211825    // t1
    li x7, 0x0                   // t2
    li x8, 0x80                  // fp
    li x9, 0x80180497            // s1
    li x10, 0xffffffff9e0af000   // a0
    li x11, 0x8015550a           // a1
    li x12, 0xbfcc85fce20bb05c   // a2
    li x13, 0x80249688           // a3
    li x14, 0x7fffffff           // a4
    li x15, 0x0                  // a5
    li x16, 0x8017fddc           // a6
    li x17, 0x13307a4f3d872dd3   // a7
    li x18, 0x0                  // s2
    li x19, 0x1                  // s3
    li x20, 0x0                  // s4
    li x21, 0x0                  // s5
    li x22, 0xffffffffffffffff   // s6
    li x23, 0x0                  // s7
    li x24, 0xc2e9d10b3dc045ea   // s8
    li x25, 0x80000656           // s9
    li x26, 0xffffffffffffffff   // s10
    li x27, 0x0                  // s11
    li x28, 0x0                  // t3
    li x29, 0x0                  // t4
    li x30, 0x1a84e6997f811cb6   // t5
    li x31, 0x38059e18310846     // t6
    // INSTRUCTION ({'dep': {'f17', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'f11'}})
    fsqrt.d f11, f17, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f11                 0x34ba98abea99e373(1.0846839569439736e-54_d)    0x34ba98abea99e372(1.0846839569439735e-54_d)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.d f11, f17, dyn
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f11                 0x34ba98abea99e373(1.0846839569439736e-54_d)    0x34ba98abea99e372(1.0846839569439735e-54_d)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f11, f17
f11                 0x34ba98abea99e373(1.0846839569439736e-54_d)    0x34ba98abea99e372(1.0846839569439735e-54_d)    X
f17                 0x29861aefc20a6190(1.176539286451636e-108_d)    0x29861aefc20a6190(1.176539286451636e-108_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fddc(2149055964)                  0x000000008017fddc(2149055964)                  
sp(x2)              0x000000008017fe7c(2149056124)                  0x000000008017fe7c(2149056124)                  
gp(x3)              0x00000000800005d4(2147485140)                  0x00000000800005d4(2147485140)                  
tp(x4)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t0(x5)              0x000000008007b28f(2147988111)                  0x000000008007b28f(2147988111)                  
t1(x6)              0xe0167860c4211825(16147225870986188837)        0xe0167860c4211825(16147225870986188837)        
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x0000000000000080(128)                         0x0000000000000080(128)                         
s1(x9)              0x0000000080180497(2149057687)                  0x0000000080180497(2149057687)                  
a0(x10)             0xffffffff9e0af000(18446744072066101248)        0xffffffff9e0af000(18446744072066101248)        
a1(x11)             0x000000008015550a(2148881674)                  0x000000008015550a(2148881674)                  
a2(x12)             0xbfcc85fce20bb05c(13820568677663879260)        0xbfcc85fce20bb05c(13820568677663879260)        
a3(x13)             0x0000000080249688(2149881480)                  0x0000000080249688(2149881480)                  
a4(x14)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x000000008017fddc(2149055964)                  0x000000008017fddc(2149055964)                  
a7(x17)             0x13307a4f3d872dd3(1382739566356016595)         0x13307a4f3d872dd3(1382739566356016595)         
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0xc2e9d10b3dc045ea(14044986759142458858)        0xc2e9d10b3dc045ea(14044986759142458858)        
s9(x25)             0x0000000080000656(2147485270)                  0x0000000080000656(2147485270)                  
s10(x26)            0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x1a84e6997f811cb6(1910905688855485622)         0x1a84e6997f811cb6(1910905688855485622)         
t6(x31)             0x0038059e18310846(15768775264634950)           0x0038059e18310846(15768775264634950)           

STATE               REF                                             DUT                                             DIFF
xmemhash            de8adbb89e8d1e939362e5bb32fc30c8612a0137        de8adbb89e8d1e939362e5bb32fc30c8612a0137        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000778(2147485560)                  0x0000000080000778(2147485560)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000081(129)                         0x0000000000000081(129)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xf97315e9fd155636(-1.0572601980133604e+277_d)  0xf97315e9fd155636(-1.0572601980133604e+277_d)  
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff5f7064c1(1.732218227251793e+19_s)     0xffffffff5f7064c1(1.732218227251793e+19_s)     
f3                  0xc2e9d10b3dc045ea(-227085019644463.3_d)        0xc2e9d10b3dc045ea(-227085019644463.3_d)        
f4                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f5                  0xf9c6579f8bcc1a27(-3.96053141378956e+278_d)    0xf9c6579f8bcc1a27(-3.96053141378956e+278_d)    
f6                  0xffffffffcf620bb0(-3792416768.0_s)             0xffffffffcf620bb0(-3792416768.0_s)             
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0x6c830e22bf275fc1(5.131931376437674e+214_d)    0x6c830e22bf275fc1(5.131931376437674e+214_d)    
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x34ba98abea99e373(1.0846839569439736e-54_d)    0x34ba98abea99e372(1.0846839569439735e-54_d)    X
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x29861aefc20a6190(1.176539286451636e-108_d)    0x29861aefc20a6190(1.176539286451636e-108_d)    
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xfddfcf8c6f21103f(-2.0804124800063452e+298_d)  0xfddfcf8c6f21103f(-2.0804124800063452e+298_d)  
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x29861aefc20a6190(1.176539286451636e-108_d)    0x29861aefc20a6190(1.176539286451636e-108_d)    
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x1e807100754bfec4(9.136323784076222e-162_d)    0x1e807100754bfec4(9.136323784076222e-162_d)    
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x9e807100754bfec4(-9.136323784076222e-162_d)   0x9e807100754bfec4(-9.136323784076222e-162_d)   
f22                 0x41e00000cac00000(2147485270.0_d)              0x41e00000cac00000(2147485270.0_d)              
f23                 0xffffffffdf000000(-9.223372036854776e+18_s)    0xffffffffdf000000(-9.223372036854776e+18_s)    
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f28                 0xc1dffd2ba9800000(-2146741926.0_d)             0xc1dffd2ba9800000(-2146741926.0_d)             
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x20f44738208ae755(6.194861112194082e-150_d)    0x20f44738208ae755(6.194861112194082e-150_d)    
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

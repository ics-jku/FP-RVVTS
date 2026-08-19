# FailID_004471 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4471
* Isolated failing instruction: `fsd`
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x78,0x57,0x04,0x6e,0xff,0xff,0xff,0x7f
_reg_f2: .byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0xf0,0xe1,0xd1,0xc1
_reg_f4: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xdf,0x41
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x78,0x57,0x04,0x6e,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f12:.byte 0xfa,0xf4,0x27,0x80,0x00,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0x00,0x44,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x20,0x74,0x00,0x03,0xe0,0x41
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xc8
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x801ff958            // sp
    li x3, 0x8023b013            // gp
    li x4, 0x80180695            // tp
    li x5, 0x8018129e            // t0
    li x6, 0x801fff25            // t1
    li x7, 0x80180013            // t2
    li x8, 0x7ffff919            // fp
    li x9, 0x13312000            // s1
    li x10, 0xffffffffcc776000   // a0
    li x11, 0x80000001           // a1
    li x12, 0x0                  // a2
    li x13, 0x7fc00000           // a3
    li x14, 0x80180270           // a4
    li x15, 0x10037fb85          // a5
    li x16, 0x7ffffc84           // a6
    li x17, 0x80000113           // a7
    li x18, 0x0                  // s2
    li x19, 0x8018040d           // s3
    li x20, 0x8020a40d           // s4
    li x21, 0x8000042e           // s5
    li x22, 0x200                // s6
    li x23, 0x800003e5           // s7
    li x24, 0x8020a385           // s8
    li x25, 0x8017f9fd           // s9
    li x26, 0x8017f9fd           // s10
    li x27, 0x801806f8           // s11
    li x28, 0x8017fc57           // t3
    li x29, 0x8000024a           // t4
    li x30, 0x7ffffd72           // t5
    li x31, 0x8017fc60           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'f6', 'fcsr.rm', 'x20'}, 'clob': {'x6', 'x20'}})
    
    li x6, 0xffff8
    and x20, x20, x6
    li x6, 0x8017fdcc
    add x20, x20, x6
    fsd f6, 0x234(x20)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        cf73f9e13a3a4fc30e356964094c91d012de9b11        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f6, 0x234(x20)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        cf73f9e13a3a4fc30e356964094c91d012de9b11        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f6, x234, x20
s4(x20)             0x000000008018a1d4(2149097940)                  0x000000008018a1d4(2149097940)
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x00000000801ff958(2149579096)                  0x00000000801ff958(2149579096)                  
gp(x3)              0x000000008023b013(2149822483)                  0x000000008023b013(2149822483)                  
tp(x4)              0x0000000080180695(2149058197)                  0x0000000080180695(2149058197)                  
t0(x5)              0x000000008018129e(2149061278)                  0x000000008018129e(2149061278)                  
t1(x6)              0x000000008017fdcc(2149055948)                  0x000000008017fdcc(2149055948)                  
t2(x7)              0x0000000080180013(2149056531)                  0x0000000080180013(2149056531)                  
fp(x8)              0x000000007ffff919(2147481881)                  0x000000007ffff919(2147481881)                  
s1(x9)              0x0000000013312000(321986560)                   0x0000000013312000(321986560)                   
a0(x10)             0xffffffffcc776000(18446744072844959744)        0xffffffffcc776000(18446744072844959744)        
a1(x11)             0x0000000080000001(2147483649)                  0x0000000080000001(2147483649)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
a4(x14)             0x0000000080180270(2149057136)                  0x0000000080180270(2149057136)                  
a5(x15)             0x000000010037fb85(4298636165)                  0x000000010037fb85(4298636165)                  
a6(x16)             0x000000007ffffc84(2147482756)                  0x000000007ffffc84(2147482756)                  
a7(x17)             0x0000000080000113(2147483923)                  0x0000000080000113(2147483923)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000008018040d(2149057549)                  0x000000008018040d(2149057549)                  
s4(x20)             0x000000008018a1d4(2149097940)                  0x000000008018a1d4(2149097940)                  
s5(x21)             0x000000008000042e(2147484718)                  0x000000008000042e(2147484718)                  
s6(x22)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s7(x23)             0x00000000800003e5(2147484645)                  0x00000000800003e5(2147484645)                  
s8(x24)             0x000000008020a385(2149622661)                  0x000000008020a385(2149622661)                  
s9(x25)             0x000000008017f9fd(2149054973)                  0x000000008017f9fd(2149054973)                  
s10(x26)            0x000000008017f9fd(2149054973)                  0x000000008017f9fd(2149054973)                  
s11(x27)            0x00000000801806f8(2149058296)                  0x00000000801806f8(2149058296)                  
t3(x28)             0x000000008017fc57(2149055575)                  0x000000008017fc57(2149055575)                  
t4(x29)             0x000000008000024a(2147484234)                  0x000000008000024a(2147484234)                  
t5(x30)             0x000000007ffffd72(2147482994)                  0x000000007ffffd72(2147482994)                  
t6(x31)             0x000000008017fc60(2149055584)                  0x000000008017fc60(2149055584)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            f26eea3ca4acf6206c22b3be23da5182873b3111        f26eea3ca4acf6206c22b3be23da5182873b3111        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        cf73f9e13a3a4fc30e356964094c91d012de9b11        X
lastPC              0x0000000080000784(2147485572)                  0x0000000080000784(2147485572)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000c8(200)                         0x00000000000000c8(200)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7fffffff6e045778(nan_d)                       0x7fffffff6e045778(nan_d)                       
f2                  0xfffffffffffffe00(nan_h)                       0xfffffffffffffe00(nan_h)                       
f3                  0xc1d1e1f000000000(-1200078848.0_d)             0xc1d1e1f000000000(-1200078848.0_d)             
f4                  0x41dfffffffc00000(2147483647.0_d)              0x41dfffffffc00000(2147483647.0_d)              
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff6e045778(1.0239441131675492e+28_s)    0xffffffff6e045778(1.0239441131675492e+28_s)    
f10                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f11                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
f12                 0x000000008027f4fa(1.0622916647e-314_d)         0x000000008027f4fa(1.0622916647e-314_d)         
f13                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)                     
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x41e0030074200000(2149057441.0_d)              0x41e0030074200000(2149057441.0_d)              
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f23                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
f24                 0x7fffffff42140000(nan_d)                       0x7fffffff42140000(nan_d)                       
f25                 0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

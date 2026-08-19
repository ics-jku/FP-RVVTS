# FailID_004915 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4915
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x65,0xe6,0xcc,0x41,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x90,0x0d,0x95,0x9b,0x78,0xd2,0xcd,0xed
_reg_f15:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0xcf,0xc7,0xf8,0xdf,0xc1
_reg_f17:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x90,0x0d,0x95,0x9b,0x78,0xd2,0xcd,0x6d
_reg_f20:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x65,0xe6,0x4c,0x41,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x24,0x43,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x7d,0x07,0x65,0x40,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x00,0x00,0x48,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x20
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x30                  // ra
    li x2, 0x8017fbbb            // sp
    li x3, 0x0                   // gp
    li x4, 0x801ff2ba            // tp
    li x5, 0x801ce0c1            // t0
    li x6, 0x1                   // t1
    li x7, 0x8000039d            // t2
    li x8, 0xcab39774            // fp
    li x9, 0x80000333            // s1
    li x10, 0x800002f8           // a0
    li x11, 0x801ff6fb           // a1
    li x12, 0x6000               // a2
    li x13, 0x7fffff70           // a3
    li x14, 0x1                  // a4
    li x15, 0x0                  // a5
    li x16, 0x8017fae2           // a6
    li x17, 0x25                 // a7
    li x18, 0x0                  // s2
    li x19, 0x68                 // s3
    li x20, 0x6000               // s4
    li x21, 0x8017ff63           // s5
    li x22, 0x8017fbf8           // s6
    li x23, 0x7ffffc3b           // s7
    li x24, 0x8018033a           // s8
    li x25, 0x7fffffff           // s9
    li x26, 0xffffffffffffffff   // s10
    li x27, 0x0                  // s11
    li x28, 0x7fffffff           // t3
    li x29, 0x7ffffe3d           // t4
    li x30, 0x8017fb78           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'x5', 'f14', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'x5', 'x26'}})
    
    li x26, 0xffffc
    and x5, x5, x26
    li x26, 0x80180773
    add x5, x5, x26
    fsw f14, -0x773(x5)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2dd37197a56ece53eb17410f19f12145162b77e4        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f14, -0x773(x5)
+========================================================================================================================+
Attributes:  none
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2dd37197a56ece53eb17410f19f12145162b77e4        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x773, x5
t0(x5)              0x000000008024e833(2149902387)                  0x000000008024e833(2149902387)
f14                 0xedcdd2789b950d90(-8.421817586531674e+220_d)   0xedcdd2789b950d90(-8.421817586531674e+220_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000030(48)                          0x0000000000000030(48)                          
sp(x2)              0x000000008017fbbb(2149055419)                  0x000000008017fbbb(2149055419)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x00000000801ff2ba(2149577402)                  0x00000000801ff2ba(2149577402)                  
t0(x5)              0x000000008024e833(2149902387)                  0x000000008024e833(2149902387)                  
t1(x6)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t2(x7)              0x000000008000039d(2147484573)                  0x000000008000039d(2147484573)                  
fp(x8)              0x00000000cab39774(3400767348)                  0x00000000cab39774(3400767348)                  
s1(x9)              0x0000000080000333(2147484467)                  0x0000000080000333(2147484467)                  
a0(x10)             0x00000000800002f8(2147484408)                  0x00000000800002f8(2147484408)                  
a1(x11)             0x00000000801ff6fb(2149578491)                  0x00000000801ff6fb(2149578491)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x000000007fffff70(2147483504)                  0x000000007fffff70(2147483504)                  
a4(x14)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x000000008017fae2(2149055202)                  0x000000008017fae2(2149055202)                  
a7(x17)             0x0000000000000025(37)                          0x0000000000000025(37)                          
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x0000000000000068(104)                         0x0000000000000068(104)                         
s4(x20)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s5(x21)             0x000000008017ff63(2149056355)                  0x000000008017ff63(2149056355)                  
s6(x22)             0x000000008017fbf8(2149055480)                  0x000000008017fbf8(2149055480)                  
s7(x23)             0x000000007ffffc3b(2147482683)                  0x000000007ffffc3b(2147482683)                  
s8(x24)             0x000000008018033a(2149057338)                  0x000000008018033a(2149057338)                  
s9(x25)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s10(x26)            0x0000000080180773(2149058419)                  0x0000000080180773(2149058419)                  
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
t4(x29)             0x000000007ffffe3d(2147483197)                  0x000000007ffffe3d(2147483197)                  
t5(x30)             0x000000008017fb78(2149055352)                  0x000000008017fb78(2149055352)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            55510bc9fa21f002b6b96f2fd041381dbe940086        55510bc9fa21f002b6b96f2fd041381dbe940086        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2dd37197a56ece53eb17410f19f12145162b77e4        X
lastPC              0x000000008000073c(2147485500)                  0x000000008000073c(2147485500)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000020(32)                          0x0000000000000020(32)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f2                  0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f11                 0xffffffff41cce665(25.612497329711914_s)        0xffffffff41cce665(25.612497329711914_s)        
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xedcdd2789b950d90(-8.421817586531674e+220_d)   0xedcdd2789b950d90(-8.421817586531674e+220_d)   
f15                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f16                 0xc1dff8c7cfc00000(-2145591103.0_d)             0xc1dff8c7cfc00000(-2145591103.0_d)             
f17                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f18                 0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f19                 0x6dcdd2789b950d90(8.421817586531674e+220_d)    0x6dcdd2789b950d90(8.421817586531674e+220_d)    
f20                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f21                 0xffffffff414ce665(12.806248664855957_s)        0xffffffff414ce665(12.806248664855957_s)        
f22                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff43240000(164.0_s)                     0xffffffff43240000(164.0_s)                     
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff4065077d(3.5785820484161377_s)        0xffffffff4065077d(3.5785820484161377_s)        
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff48000000(131072.0_s)                  0xffffffff48000000(131072.0_s)                  
STATES DIFFER: True
```

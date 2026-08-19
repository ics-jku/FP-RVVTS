# FailID_003364 VP++ SF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3364
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
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x65,0xe6,0xcc,0x41,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x90,0x0d,0x95,0x9b,0x78,0xd2,0xcd,0xed
_reg_f15:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x90,0x0d,0x95,0x9b,0x78,0xd2,0xcd,0x6d
_reg_f20:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x65,0xe6,0x4c,0x41,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x64,0x18,0x00,0x4d,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x24,0x43,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x48
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x1000000             // ra
    li x2, 0x1                   // sp
    li x3, 0x7fffff3d            // gp
    li x4, 0x8018026a            // tp
    li x5, 0x801cdb9b            // t0
    li x6, 0x0                   // t1
    li x7, 0xffffffff41cce665    // t2
    li x8, 0xfffffffffffff892    // fp
    li x9, 0x0                   // s1
    li x10, 0x0                  // a0
    li x11, 0x0                  // a1
    li x12, 0x8000006d           // a2
    li x13, 0x26                 // a3
    li x14, 0x1                  // a4
    li x15, 0x48                 // a5
    li x16, 0x0                  // a6
    li x17, 0x801ce1f0           // a7
    li x18, 0x8017fee6           // s2
    li x19, 0xa4                 // s3
    li x20, 0x801803e5           // s4
    li x21, 0x8000606d           // s5
    li x22, 0x80200388           // s6
    li x23, 0x802000f8           // s7
    li x24, 0x8020085a           // s8
    li x25, 0x1                  // s9
    li x26, 0x8018034d           // s10
    li x27, 0xffffffffda675000   // s11
    li x28, 0x8017ff6d           // t3
    li x29, 0x801e5e1b           // t4
    li x30, 0x8017fc9b           // t5
    li x31, 0x800003fa           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x23'}, 'clob': {'x9', 'f24', 'x23'}})
    
    li x9, 0x1ffff8
    and x23, x23, x9
    li x9, 0x80000215
    add x23, x23, x9
    fld f24, -0x215(x23)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f24                 0xffffffff43240000(164.0_s)                     0x0051b02300000393(3.93571821899963e-307_d)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f24, -0x215(x23)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f24                 0xffffffff43240000(164.0_s)                     0x0051b02300000393(3.93571821899963e-307_d)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f24, x215, x23
s7(x23)             0x000000008000030d(2147484429)                  0x000000008000030d(2147484429)
f24                 0xffffffff43240000(164.0_s)                     0x0051b02300000393(3.93571821899963e-307_d)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000001000000(16777216)                    0x0000000001000000(16777216)                    
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)                           
gp(x3)              0x000000007fffff3d(2147483453)                  0x000000007fffff3d(2147483453)                  
tp(x4)              0x000000008018026a(2149057130)                  0x000000008018026a(2149057130)                  
t0(x5)              0x00000000801cdb9b(2149374875)                  0x00000000801cdb9b(2149374875)                  
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0xffffffff41cce665(18446744070518531685)        0xffffffff41cce665(18446744070518531685)        
fp(x8)              0xfffffffffffff892(18446744073709549714)        0xfffffffffffff892(18446744073709549714)        
s1(x9)              0x0000000080000215(2147484181)                  0x0000000080000215(2147484181)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x000000008000006d(2147483757)                  0x000000008000006d(2147483757)                  
a3(x13)             0x0000000000000026(38)                          0x0000000000000026(38)                          
a4(x14)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a5(x15)             0x0000000000000048(72)                          0x0000000000000048(72)                          
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x00000000801ce1f0(2149376496)                  0x00000000801ce1f0(2149376496)                  
s2(x18)             0x000000008017fee6(2149056230)                  0x000000008017fee6(2149056230)                  
s3(x19)             0x00000000000000a4(164)                         0x00000000000000a4(164)                         
s4(x20)             0x00000000801803e5(2149057509)                  0x00000000801803e5(2149057509)                  
s5(x21)             0x000000008000606d(2147508333)                  0x000000008000606d(2147508333)                  
s6(x22)             0x0000000080200388(2149581704)                  0x0000000080200388(2149581704)                  
s7(x23)             0x000000008000030d(2147484429)                  0x000000008000030d(2147484429)                  
s8(x24)             0x000000008020085a(2149582938)                  0x000000008020085a(2149582938)                  
s9(x25)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s10(x26)            0x000000008018034d(2149057357)                  0x000000008018034d(2149057357)                  
s11(x27)            0xffffffffda675000(18446744073078788096)        0xffffffffda675000(18446744073078788096)        
t3(x28)             0x000000008017ff6d(2149056365)                  0x000000008017ff6d(2149056365)                  
t4(x29)             0x00000000801e5e1b(2149473819)                  0x00000000801e5e1b(2149473819)                  
t5(x30)             0x000000008017fc9b(2149055643)                  0x000000008017fc9b(2149055643)                  
t6(x31)             0x00000000800003fa(2147484666)                  0x00000000800003fa(2147484666)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            d9f7186ce1a6e4c49eebb7d0116131128d6ac303        d9f7186ce1a6e4c49eebb7d0116131128d6ac303        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000748(2147485512)                  0x0000000080000748(2147485512)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000048(72)                          0x0000000000000048(72)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
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
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff41cce665(25.612497329711914_s)        0xffffffff41cce665(25.612497329711914_s)        
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xedcdd2789b950d90(-8.421817586531674e+220_d)   0xedcdd2789b950d90(-8.421817586531674e+220_d)   
f15                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f18                 0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f19                 0x6dcdd2789b950d90(8.421817586531674e+220_d)    0x6dcdd2789b950d90(8.421817586531674e+220_d)    
f20                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f21                 0xffffffff414ce665(12.806248664855957_s)        0xffffffff414ce665(12.806248664855957_s)        
f22                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f23                 0xffffffff4d001864(134317632.0_s)               0xffffffff4d001864(134317632.0_s)               
f24                 0xffffffff43240000(164.0_s)                     0x0051b02300000393(3.93571821899963e-307_d)     X
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff4065077d(3.5785820484161377_s)        0xffffffff4065077d(3.5785820484161377_s)        
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff48000000(131072.0_s)                  0xffffffff48000000(131072.0_s)                  
STATES DIFFER: True
```

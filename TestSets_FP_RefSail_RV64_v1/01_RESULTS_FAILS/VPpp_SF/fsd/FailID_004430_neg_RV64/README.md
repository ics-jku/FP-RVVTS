# FailID_004430 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4430
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0xeb,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x90,0xff,0xff,0xdf,0x41
_reg_f6: .byte 0x00,0x00,0x00,0xe8,0xf4,0x80,0xe4,0x41
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0xeb,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x20,0x17,0x1b,0x5c,0x00,0x00,0x00,0x80
_reg_f13:.byte 0x20,0x17,0x1b,0x5c,0x00,0x00,0x00,0x80
_reg_f14:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0xfd,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f25:.byte 0xfc,0xcf,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x5d
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80000072            // ra
    li x2, 0xffffffffffff91f3    // sp
    li x3, 0x0                   // gp
    li x4, 0x51b023340191f3      // tp
    li x5, 0x7fffffffffffffff    // t0
    li x6, 0xf80000              // t1
    li x7, 0x6000                // t2
    li x8, 0x8017f9c2            // fp
    li x9, 0x800003be            // s1
    li x10, 0x800006e6           // a0
    li x11, 0x3efe25cf           // a1
    li x12, 0x0                  // a2
    li x13, 0xffffffffffffffff   // a3
    li x14, 0x801803e4           // a4
    li x15, 0x45a872c            // a5
    li x16, 0x8027f42a           // a6
    li x17, 0x4d                 // a7
    li x18, 0x80000746           // s2
    li x19, 0x80180d6f           // s3
    li x20, 0xa407a740           // s4
    li x21, 0x800000a9           // s5
    li x22, 0x0                  // s6
    li x23, 0x80180d2e           // s7
    li x24, 0x7ffffe43           // s8
    li x25, 0x23f3               // s9
    li x26, 0xffffffffffffffff   // s10
    li x27, 0x801ffa67           // s11
    li x28, 0x802803d1           // t3
    li x29, 0xfbf8973c           // t4
    li x30, 0x800002c2           // t5
    li x31, 0x801807e8           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f4', 'x7'}, 'clob': {'x3', 'x7'}})
    
    li x3, 0xffff8
    and x7, x7, x3
    li x3, 0x8017fd09
    add x7, x7, x3
    fsd f4, 0x2f7(x7)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        91caf6580410e578d46781a22dd0749e34ec22cb        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f4, 0x2f7(x7)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        91caf6580410e578d46781a22dd0749e34ec22cb        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f4, x2, f7, x7
sp(x2)              0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)
t2(x7)              0x0000000080185d09(2149080329)                  0x0000000080185d09(2149080329)
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080000072(2147483762)                  0x0000000080000072(2147483762)                  
sp(x2)              0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)        
gp(x3)              0x000000008017fd09(2149055753)                  0x000000008017fd09(2149055753)                  
tp(x4)              0x0051b023340191f3(22993138356425203)           0x0051b023340191f3(22993138356425203)           
t0(x5)              0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
t1(x6)              0x0000000000f80000(16252928)                    0x0000000000f80000(16252928)                    
t2(x7)              0x0000000080185d09(2149080329)                  0x0000000080185d09(2149080329)                  
fp(x8)              0x000000008017f9c2(2149054914)                  0x000000008017f9c2(2149054914)                  
s1(x9)              0x00000000800003be(2147484606)                  0x00000000800003be(2147484606)                  
a0(x10)             0x00000000800006e6(2147485414)                  0x00000000800006e6(2147485414)                  
a1(x11)             0x000000003efe25cf(1056843215)                  0x000000003efe25cf(1056843215)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a4(x14)             0x00000000801803e4(2149057508)                  0x00000000801803e4(2149057508)                  
a5(x15)             0x00000000045a872c(73041708)                    0x00000000045a872c(73041708)                    
a6(x16)             0x000000008027f42a(2150102058)                  0x000000008027f42a(2150102058)                  
a7(x17)             0x000000000000004d(77)                          0x000000000000004d(77)                          
s2(x18)             0x0000000080000746(2147485510)                  0x0000000080000746(2147485510)                  
s3(x19)             0x0000000080180d6f(2149059951)                  0x0000000080180d6f(2149059951)                  
s4(x20)             0x00000000a407a740(2751964992)                  0x00000000a407a740(2751964992)                  
s5(x21)             0x00000000800000a9(2147483817)                  0x00000000800000a9(2147483817)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000080180d2e(2149059886)                  0x0000000080180d2e(2149059886)                  
s8(x24)             0x000000007ffffe43(2147483203)                  0x000000007ffffe43(2147483203)                  
s9(x25)             0x00000000000023f3(9203)                        0x00000000000023f3(9203)                        
s10(x26)            0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s11(x27)            0x00000000801ffa67(2149579367)                  0x00000000801ffa67(2149579367)                  
t3(x28)             0x00000000802803d1(2150106065)                  0x00000000802803d1(2150106065)                  
t4(x29)             0x00000000fbf8973c(4227372860)                  0x00000000fbf8973c(4227372860)                  
t5(x30)             0x00000000800002c2(2147484354)                  0x00000000800002c2(2147484354)                  
t6(x31)             0x00000000801807e8(2149058536)                  0x00000000801807e8(2149058536)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            7f5358227ce4d3b3af9ccf1c8ade0aeb797488aa        7f5358227ce4d3b3af9ccf1c8ade0aeb797488aa        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        91caf6580410e578d46781a22dd0749e34ec22cb        X
lastPC              0x000000008000076c(2147485548)                  0x000000008000076c(2147485548)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000005d(93)                          0x000000000000005d(93)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff000000eb(3.29305139116332e-43_s)      0xffffffff000000eb(3.29305139116332e-43_s)      
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0x41dfffff90c00000(2147483203.0_d)              0x41dfffff90c00000(2147483203.0_d)              
f6                  0x41e480f4e8000000(2751964992.0_d)              0x41e480f4e8000000(2751964992.0_d)              
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff800000eb(-3.29305139116332e-43_s)     0xffffffff800000eb(-3.29305139116332e-43_s)     
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x800000005c1b1720(-7.634693976e-315_d)         0x800000005c1b1720(-7.634693976e-315_d)         
f13                 0x800000005c1b1720(-7.634693976e-315_d)         0x800000005c1b1720(-7.634693976e-315_d)         
f14                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f15                 0xffffffff4efffffd(2147483264.0_s)              0xffffffff4efffffd(2147483264.0_s)              
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f25                 0xffffffff4effcffc(2145910272.0_s)              0xffffffff4effcffc(2145910272.0_s)              
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

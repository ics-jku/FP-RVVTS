# FailID_002070 VP++ FF neg RV64 fsh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2070
* Isolated failing instruction: `fsh`
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
    li x3, 0x59                  // gp
    li x4, 0x51b023340191f3      // tp
    li x5, 0x7fffffffffffffff    // t0
    li x6, 0x80200784            // t1
    li x7, 0x80181fe3            // t2
    li x8, 0x8027fda5            // fp
    li x9, 0x8017fbf7            // s1
    li x10, 0x8017fce3           // a0
    li x11, 0x801e271b           // a1
    li x12, 0x0                  // a2
    li x13, 0xffffffffffffffff   // a3
    li x14, 0x6000               // a4
    li x15, 0x45a872c            // a5
    li x16, 0x8017faa0           // a6
    li x17, 0x119a00c8f9800000   // a7
    li x18, 0x80000746           // s2
    li x19, 0x802007dc           // s3
    li x20, 0x801fa231           // s4
    li x21, 0x800000a9           // s5
    li x22, 0x8017faa0           // s6
    li x23, 0x80180d2e           // s7
    li x24, 0x7ffffe43           // s8
    li x25, 0x80002a04           // s9
    li x26, 0xffffffffffffffff   // s10
    li x27, 0x801ffa67           // s11
    li x28, 0x801807df           // t3
    li x29, 0xfbf8973c           // t4
    li x30, 0x80000614           // t5
    li x31, 0x801807f1           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f11', 'mstatus.fs/vs.fs', 'x20'}, 'clob': {'x14', 'x20'}})
    
    li x14, 0xffffe
    and x20, x20, x14
    li x14, 0x801802a1
    add x20, x20, x14
    fsh f11, -0x2a1(x20)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsh f11, -0x2a1(x20)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f11, x2, a1, x20
sp(x2)              0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)
s4(x20)             0x000000008027a4d1(2150081745)                  0x000000008027a4d1(2150081745)
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080000072(2147483762)                  0x0000000080000072(2147483762)                  
sp(x2)              0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)        
gp(x3)              0x0000000000000059(89)                          0x0000000000000059(89)                          
tp(x4)              0x0051b023340191f3(22993138356425203)           0x0051b023340191f3(22993138356425203)           
t0(x5)              0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
t1(x6)              0x0000000080200784(2149582724)                  0x0000000080200784(2149582724)                  
t2(x7)              0x0000000080181fe3(2149064675)                  0x0000000080181fe3(2149064675)                  
fp(x8)              0x000000008027fda5(2150104485)                  0x000000008027fda5(2150104485)                  
s1(x9)              0x000000008017fbf7(2149055479)                  0x000000008017fbf7(2149055479)                  
a0(x10)             0x000000008017fce3(2149055715)                  0x000000008017fce3(2149055715)                  
a1(x11)             0x00000000801e271b(2149459739)                  0x00000000801e271b(2149459739)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a4(x14)             0x00000000801802a1(2149057185)                  0x00000000801802a1(2149057185)                  
a5(x15)             0x00000000045a872c(73041708)                    0x00000000045a872c(73041708)                    
a6(x16)             0x000000008017faa0(2149055136)                  0x000000008017faa0(2149055136)                  
a7(x17)             0x119a00c8f9800000(1268327108237590528)         0x119a00c8f9800000(1268327108237590528)         
s2(x18)             0x0000000080000746(2147485510)                  0x0000000080000746(2147485510)                  
s3(x19)             0x00000000802007dc(2149582812)                  0x00000000802007dc(2149582812)                  
s4(x20)             0x000000008027a4d1(2150081745)                  0x000000008027a4d1(2150081745)                  
s5(x21)             0x00000000800000a9(2147483817)                  0x00000000800000a9(2147483817)                  
s6(x22)             0x000000008017faa0(2149055136)                  0x000000008017faa0(2149055136)                  
s7(x23)             0x0000000080180d2e(2149059886)                  0x0000000080180d2e(2149059886)                  
s8(x24)             0x000000007ffffe43(2147483203)                  0x000000007ffffe43(2147483203)                  
s9(x25)             0x0000000080002a04(2147494404)                  0x0000000080002a04(2147494404)                  
s10(x26)            0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s11(x27)            0x00000000801ffa67(2149579367)                  0x00000000801ffa67(2149579367)                  
t3(x28)             0x00000000801807df(2149058527)                  0x00000000801807df(2149058527)                  
t4(x29)             0x00000000fbf8973c(4227372860)                  0x00000000fbf8973c(4227372860)                  
t5(x30)             0x0000000080000614(2147485204)                  0x0000000080000614(2147485204)                  
t6(x31)             0x00000000801807f1(2149058545)                  0x00000000801807f1(2149058545)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            584fea27f4de87e4bda9f78a0364bffd65196cfa        584fea27f4de87e4bda9f78a0364bffd65196cfa        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800007a4(2147485604)                  0x00000000800007a4(2147485604)                  
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

# FailID_002257 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2257
* Isolated failing instruction: `fsw`
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x40,0xff,0x04,0xe0,0x41
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x63,0x40
_reg_f7: .byte 0xfa,0x27,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f10:.byte 0x02,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x63,0x40
_reg_f14:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0xfa,0x27,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x48,0x69,0xc1,0xc1
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xfa,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x63,0x40
_reg_f31:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x28
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x6000                // ra
    li x2, 0xffffffff803c1000    // sp
    li x3, 0x63440740            // gp
    li x4, 0x80186a77            // tp
    li x5, 0x801801d3            // t0
    li x6, 0x6000                // t1
    li x7, 0x801ff67f            // t2
    li x8, 0x8017fcfc            // fp
    li x9, 0x6000                // s1
    li x10, 0x0                  // a0
    li x11, 0x801801d3           // a1
    li x12, 0xffffffffe323fb0d   // a2
    li x13, 0x8017fb83           // a3
    li x14, 0x6000               // a4
    li x15, 0x80200c33           // a5
    li x16, 0x80000800           // a6
    li x17, 0x8020002e           // a7
    li x18, 0xbd                 // s2
    li x19, 0x801807b0           // s3
    li x20, 0x80036fa8           // s4
    li x21, 0x801802df           // s5
    li x22, 0x801ffa38           // s6
    li x23, 0xc9                 // s7
    li x24, 0x0                  // s8
    li x25, 0x8018044f           // s9
    li x26, 0x7fffff97           // s10
    li x27, 0x6000               // s11
    li x28, 0xffffffffffff9d03   // t3
    li x29, 0x3d                 // t4
    li x30, 0x801ff931           // t5
    li x31, 0x57                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x8', 'mstatus.fs/vs.fs', 'f16'}, 'clob': {'x8', 'x1'}})
    
    li x1, 0xffffc
    and x8, x8, x1
    li x1, 0x801806c3
    add x8, x8, x1
    fsw f16, -0x6c3(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        eb34672168c5b52115fa3851e957f84525149e61        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f16, -0x6c3(x8)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        eb34672168c5b52115fa3851e957f84525149e61        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f16, x6, c3, x8
t1(x6)              0x0000000000006000(24576)                       0x0000000000006000(24576)
fp(x8)              0x00000000802003bf(2149581759)                  0x00000000802003bf(2149581759)
f16                 0xffffffff4f0027fa(2150103552.0_s)              0xffffffff4f0027fa(2150103552.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801806c3(2149058243)                  0x00000000801806c3(2149058243)                  
sp(x2)              0xffffffff803c1000(18446744071566004224)        0xffffffff803c1000(18446744071566004224)        
gp(x3)              0x0000000063440740(1665402688)                  0x0000000063440740(1665402688)                  
tp(x4)              0x0000000080186a77(2149083767)                  0x0000000080186a77(2149083767)                  
t0(x5)              0x00000000801801d3(2149056979)                  0x00000000801801d3(2149056979)                  
t1(x6)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t2(x7)              0x00000000801ff67f(2149578367)                  0x00000000801ff67f(2149578367)                  
fp(x8)              0x00000000802003bf(2149581759)                  0x00000000802003bf(2149581759)                  
s1(x9)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x00000000801801d3(2149056979)                  0x00000000801801d3(2149056979)                  
a2(x12)             0xffffffffe323fb0d(18446744073225370381)        0xffffffffe323fb0d(18446744073225370381)        
a3(x13)             0x000000008017fb83(2149055363)                  0x000000008017fb83(2149055363)                  
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x0000000080200c33(2149583923)                  0x0000000080200c33(2149583923)                  
a6(x16)             0x0000000080000800(2147485696)                  0x0000000080000800(2147485696)                  
a7(x17)             0x000000008020002e(2149580846)                  0x000000008020002e(2149580846)                  
s2(x18)             0x00000000000000bd(189)                         0x00000000000000bd(189)                         
s3(x19)             0x00000000801807b0(2149058480)                  0x00000000801807b0(2149058480)                  
s4(x20)             0x0000000080036fa8(2147708840)                  0x0000000080036fa8(2147708840)                  
s5(x21)             0x00000000801802df(2149057247)                  0x00000000801802df(2149057247)                  
s6(x22)             0x00000000801ffa38(2149579320)                  0x00000000801ffa38(2149579320)                  
s7(x23)             0x00000000000000c9(201)                         0x00000000000000c9(201)                         
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x000000008018044f(2149057615)                  0x000000008018044f(2149057615)                  
s10(x26)            0x000000007fffff97(2147483543)                  0x000000007fffff97(2147483543)                  
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0xffffffffffff9d03(18446744073709526275)        0xffffffffffff9d03(18446744073709526275)        
t4(x29)             0x000000000000003d(61)                          0x000000000000003d(61)                          
t5(x30)             0x00000000801ff931(2149579057)                  0x00000000801ff931(2149579057)                  
t6(x31)             0x0000000000000057(87)                          0x0000000000000057(87)                          

STATE               REF                                             DUT                                             DIFF
xmemhash            83958dd7b41d0ae856b72e938c246732e5112183        83958dd7b41d0ae856b72e938c246732e5112183        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        eb34672168c5b52115fa3851e957f84525149e61        X
lastPC              0x0000000080000750(2147485520)                  0x0000000080000750(2147485520)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000028(40)                          0x0000000000000028(40)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x41e004ff40000000(2150103552.0_d)              0x41e004ff40000000(2150103552.0_d)              
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f6                  0x4063000000000000(152.0_d)                     0x4063000000000000(152.0_d)                     
f7                  0xffffffff4f0027fa(2150103552.0_s)              0xffffffff4f0027fa(2150103552.0_s)              
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f10                 0xffffffff4f000002(2147484160.0_s)              0xffffffff4f000002(2147484160.0_s)              
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f13                 0x4063000000000000(152.0_d)                     0x4063000000000000(152.0_d)                     
f14                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f15                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f16                 0xffffffff4f0027fa(2150103552.0_s)              0xffffffff4f0027fa(2150103552.0_s)              
f17                 0xc1c1694800000000(-584224768.0_d)              0xc1c1694800000000(-584224768.0_d)              
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff4f0017fa(2149054976.0_s)              0xffffffff4f0017fa(2149054976.0_s)              
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x4063000000000000(152.0_d)                     0x4063000000000000(152.0_d)                     
f31                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
STATES DIFFER: True
```

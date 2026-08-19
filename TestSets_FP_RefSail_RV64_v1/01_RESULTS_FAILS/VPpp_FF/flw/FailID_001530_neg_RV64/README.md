# FailID_001530 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1530
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
    li x1, 0x1                   // ra
    li x2, 0x0                   // sp
    li x3, 0x800003ea            // gp
    li x4, 0x1                   // tp
    li x5, 0x1                   // t0
    li x6, 0x0                   // t1
    li x7, 0x80180467            // t2
    li x8, 0x8017f966            // fp
    li x9, 0x7ffffcfc            // s1
    li x10, 0x1                  // a0
    li x11, 0x801ffc45           // a1
    li x12, 0x802004f5           // a2
    li x13, 0xb                  // a3
    li x14, 0x801ff463           // a4
    li x15, 0x801b92c8           // a5
    li x16, 0x7ffffb03           // a6
    li x17, 0xe4                 // a7
    li x18, 0x8017fa2b           // s2
    li x19, 0x7ffff962           // s3
    li x20, 0x801802c8           // s4
    li x21, 0x801ffb87           // s5
    li x22, 0x208                // s6
    li x23, 0x801802ed           // s7
    li x24, 0xe3                 // s8
    li x25, 0x80000617           // s9
    li x26, 0x2b                 // s10
    li x27, 0x8017f98e           // s11
    li x28, 0x33c3c20c           // t3
    li x29, 0x3232774            // t4
    li x30, 0x20                 // t5
    li x31, 0x801ff9d0           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x15'}, 'clob': {'f5', 'x29', 'x15'}})
    
    li x29, 0x1ffffc
    and x15, x15, x29
    li x29, 0x800005d4
    add x15, x15, x29
    flw f5, -0x5d4(x15)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f5                  0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f5, -0x5d4(x15)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f5                  0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f5, x5, d4, x15
t0(x5)              0x0000000000000001(1)                           0x0000000000000001(1)
a5(x15)             0x00000000801b989c(2149292188)                  0x00000000801b989c(2149292188)
f5                  0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000001(1)                           0x0000000000000001(1)                           
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x00000000800003ea(2147484650)                  0x00000000800003ea(2147484650)                  
tp(x4)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t0(x5)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000080180467(2149057639)                  0x0000000080180467(2149057639)                  
fp(x8)              0x000000008017f966(2149054822)                  0x000000008017f966(2149054822)                  
s1(x9)              0x000000007ffffcfc(2147482876)                  0x000000007ffffcfc(2147482876)                  
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x00000000801ffc45(2149579845)                  0x00000000801ffc45(2149579845)                  
a2(x12)             0x00000000802004f5(2149582069)                  0x00000000802004f5(2149582069)                  
a3(x13)             0x000000000000000b(11)                          0x000000000000000b(11)                          
a4(x14)             0x00000000801ff463(2149577827)                  0x00000000801ff463(2149577827)                  
a5(x15)             0x00000000801b989c(2149292188)                  0x00000000801b989c(2149292188)                  
a6(x16)             0x000000007ffffb03(2147482371)                  0x000000007ffffb03(2147482371)                  
a7(x17)             0x00000000000000e4(228)                         0x00000000000000e4(228)                         
s2(x18)             0x000000008017fa2b(2149055019)                  0x000000008017fa2b(2149055019)                  
s3(x19)             0x000000007ffff962(2147481954)                  0x000000007ffff962(2147481954)                  
s4(x20)             0x00000000801802c8(2149057224)                  0x00000000801802c8(2149057224)                  
s5(x21)             0x00000000801ffb87(2149579655)                  0x00000000801ffb87(2149579655)                  
s6(x22)             0x0000000000000208(520)                         0x0000000000000208(520)                         
s7(x23)             0x00000000801802ed(2149057261)                  0x00000000801802ed(2149057261)                  
s8(x24)             0x00000000000000e3(227)                         0x00000000000000e3(227)                         
s9(x25)             0x0000000080000617(2147485207)                  0x0000000080000617(2147485207)                  
s10(x26)            0x000000000000002b(43)                          0x000000000000002b(43)                          
s11(x27)            0x000000008017f98e(2149054862)                  0x000000008017f98e(2149054862)                  
t3(x28)             0x0000000033c3c20c(868467212)                   0x0000000033c3c20c(868467212)                   
t4(x29)             0x00000000800005d4(2147485140)                  0x00000000800005d4(2147485140)                  
t5(x30)             0x0000000000000020(32)                          0x0000000000000020(32)                          
t6(x31)             0x00000000801ff9d0(2149579216)                  0x00000000801ff9d0(2149579216)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            c5f832ecd298e26c6a94d4f5e888ae6d93e832a2        c5f832ecd298e26c6a94d4f5e888ae6d93e832a2        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
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
f5                  0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
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

# FailID_004945 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4945
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x20,0xfe,0xff,0xdf,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x5e,0x4f,0x04,0xe0,0x41
_reg_f19:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f25:.byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x4
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017ffcb            // ra
    li x2, 0x200                 // sp
    li x3, 0x8017fa9e            // gp
    li x4, 0x802001ef            // tp
    li x5, 0xa79c77d0            // t0
    li x6, 0x6000                // t1
    li x7, 0x7ffffcc0            // t2
    li x8, 0xad                  // fp
    li x9, 0x801ffcb8            // s1
    li x10, 0x8017fb48           // a0
    li x11, 0x8027f407           // a1
    li x12, 0xfffffffffffffef6   // a2
    li x13, 0x6000               // a3
    li x14, 0x0                  // a4
    li x15, 0x76d                // a5
    li x16, 0x8017ffaf           // a6
    li x17, 0x801805e0           // a7
    li x18, 0x8017f30d           // s2
    li x19, 0x71                 // s3
    li x20, 0x46c002e8           // s4
    li x21, 0xf5                 // s5
    li x22, 0x801ff806           // s6
    li x23, 0x6000               // s7
    li x24, 0x8017fc50           // s8
    li x25, 0x800000f2           // s9
    li x26, 0xa6                 // s10
    li x27, 0x802002a9           // s11
    li x28, 0xffffffff7fe00513   // t3
    li x29, 0x8017fed1           // t4
    li x30, 0x8017fc50           // t5
    li x31, 0x8017fdfd           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x25', 'f7'}, 'clob': {'x25', 'x30'}})
    
    li x30, 0xffffc
    and x25, x25, x30
    li x30, 0x80180217
    add x25, x25, x30
    fsw f7, -0x217(x25)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2de8edfc3355641c150bd650364624bd95cc345c        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f7, -0x217(x25)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2de8edfc3355641c150bd650364624bd95cc345c        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f7, x217, x25
s9(x25)             0x0000000080180307(2149057287)                  0x0000000080180307(2149057287)
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017ffcb(2149056459)                  0x000000008017ffcb(2149056459)                  
sp(x2)              0x0000000000000200(512)                         0x0000000000000200(512)                         
gp(x3)              0x000000008017fa9e(2149055134)                  0x000000008017fa9e(2149055134)                  
tp(x4)              0x00000000802001ef(2149581295)                  0x00000000802001ef(2149581295)                  
t0(x5)              0x00000000a79c77d0(2812049360)                  0x00000000a79c77d0(2812049360)                  
t1(x6)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t2(x7)              0x000000007ffffcc0(2147482816)                  0x000000007ffffcc0(2147482816)                  
fp(x8)              0x00000000000000ad(173)                         0x00000000000000ad(173)                         
s1(x9)              0x00000000801ffcb8(2149579960)                  0x00000000801ffcb8(2149579960)                  
a0(x10)             0x000000008017fb48(2149055304)                  0x000000008017fb48(2149055304)                  
a1(x11)             0x000000008027f407(2150102023)                  0x000000008027f407(2150102023)                  
a2(x12)             0xfffffffffffffef6(18446744073709551350)        0xfffffffffffffef6(18446744073709551350)        
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x000000000000076d(1901)                        0x000000000000076d(1901)                        
a6(x16)             0x000000008017ffaf(2149056431)                  0x000000008017ffaf(2149056431)                  
a7(x17)             0x00000000801805e0(2149058016)                  0x00000000801805e0(2149058016)                  
s2(x18)             0x000000008017f30d(2149053197)                  0x000000008017f30d(2149053197)                  
s3(x19)             0x0000000000000071(113)                         0x0000000000000071(113)                         
s4(x20)             0x0000000046c002e8(1186988776)                  0x0000000046c002e8(1186988776)                  
s5(x21)             0x00000000000000f5(245)                         0x00000000000000f5(245)                         
s6(x22)             0x00000000801ff806(2149578758)                  0x00000000801ff806(2149578758)                  
s7(x23)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s8(x24)             0x000000008017fc50(2149055568)                  0x000000008017fc50(2149055568)                  
s9(x25)             0x0000000080180307(2149057287)                  0x0000000080180307(2149057287)                  
s10(x26)            0x00000000000000a6(166)                         0x00000000000000a6(166)                         
s11(x27)            0x00000000802002a9(2149581481)                  0x00000000802002a9(2149581481)                  
t3(x28)             0xffffffff7fe00513(18446744071559972115)        0xffffffff7fe00513(18446744071559972115)        
t4(x29)             0x000000008017fed1(2149056209)                  0x000000008017fed1(2149056209)                  
t5(x30)             0x0000000080180217(2149057047)                  0x0000000080180217(2149057047)                  
t6(x31)             0x000000008017fdfd(2149055997)                  0x000000008017fdfd(2149055997)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            9f856cd0009745d28a1bbec3a616e362dcea01a3        9f856cd0009745d28a1bbec3a616e362dcea01a3        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2de8edfc3355641c150bd650364624bd95cc345c        X
lastPC              0x0000000080000760(2147485536)                  0x0000000080000760(2147485536)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000004(4)                           0x0000000000000004(4)                           
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x41dffffe20000000(2147481728.0_d)              0x41dffffe20000000(2147481728.0_d)              
f15                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x41e0044f5ec00000(2149743350.0_d)              0x41e0044f5ec00000(2149743350.0_d)              
f19                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f20                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f25                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f26                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
STATES DIFFER: True
```

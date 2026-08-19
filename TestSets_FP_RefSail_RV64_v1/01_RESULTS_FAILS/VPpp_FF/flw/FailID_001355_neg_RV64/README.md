# FailID_001355 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1355
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
_reg_f1: .byte 0xfd,0xff,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x20,0xc3,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x80,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x55,0x43,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x36,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x40,0x75,0x00,0x03,0xe0,0x41
_reg_f30:.byte 0x05,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'dyn(0b111)', 'res': 0}
    li t0, 0xe8
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x0                   // sp
    li x3, 0x1                   // gp
    li x4, 0x80200297            // tp
    li x5, 0x7b9                 // t0
    li x6, 0x801802ad            // t1
    li x7, 0x801802ad            // t2
    li x8, 0xe0                  // fp
    li x9, 0x801ef38d            // s1
    li x10, 0x8000021a           // a0
    li x11, 0x80180631           // a1
    li x12, 0x8018068b           // a2
    li x13, 0x80180b9f           // a3
    li x14, 0x0                  // a4
    li x15, 0x0                  // a5
    li x16, 0x7ffffdf0           // a6
    li x17, 0x800005af           // a7
    li x18, 0x8017fc50           // s2
    li x19, 0x8018047e           // s3
    li x20, 0x8027f6b4           // s4
    li x21, 0x5c0a9000           // s5
    li x22, 0x0                  // s6
    li x23, 0x24                 // s7
    li x24, 0x0                  // s8
    li x25, 0x802193aa           // s9
    li x26, 0x801ef38d           // s10
    li x27, 0xfffffffffffffd3b   // s11
    li x28, 0x91f3               // t3
    li x29, 0x7ffffc8d           // t4
    li x30, 0x0                  // t5
    li x31, 0x80000130           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x27'}, 'clob': {'f13', 'x27', 'x3'}})
    
    li x3, 0x1ffffc
    and x27, x27, x3
    li x3, 0x800004d2
    add x27, x27, x3
    flw f13, -0x4d2(x27)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f13, -0x4d2(x27)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x4, d2, x27
tp(x4)              0x0000000080200297(2149581463)                  0x0000000080200297(2149581463)
s11(x27)            0x000000008020020a(2149581322)                  0x000000008020020a(2149581322)
f13                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x00000000800004d2(2147484882)                  0x00000000800004d2(2147484882)                  
tp(x4)              0x0000000080200297(2149581463)                  0x0000000080200297(2149581463)                  
t0(x5)              0x00000000000007b9(1977)                        0x00000000000007b9(1977)                        
t1(x6)              0x00000000801802ad(2149057197)                  0x00000000801802ad(2149057197)                  
t2(x7)              0x00000000801802ad(2149057197)                  0x00000000801802ad(2149057197)                  
fp(x8)              0x00000000000000e0(224)                         0x00000000000000e0(224)                         
s1(x9)              0x00000000801ef38d(2149512077)                  0x00000000801ef38d(2149512077)                  
a0(x10)             0x000000008000021a(2147484186)                  0x000000008000021a(2147484186)                  
a1(x11)             0x0000000080180631(2149058097)                  0x0000000080180631(2149058097)                  
a2(x12)             0x000000008018068b(2149058187)                  0x000000008018068b(2149058187)                  
a3(x13)             0x0000000080180b9f(2149059487)                  0x0000000080180b9f(2149059487)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x000000007ffffdf0(2147483120)                  0x000000007ffffdf0(2147483120)                  
a7(x17)             0x00000000800005af(2147485103)                  0x00000000800005af(2147485103)                  
s2(x18)             0x000000008017fc50(2149055568)                  0x000000008017fc50(2149055568)                  
s3(x19)             0x000000008018047e(2149057662)                  0x000000008018047e(2149057662)                  
s4(x20)             0x000000008027f6b4(2150102708)                  0x000000008027f6b4(2150102708)                  
s5(x21)             0x000000005c0a9000(1544196096)                  0x000000005c0a9000(1544196096)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000000000024(36)                          0x0000000000000024(36)                          
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x00000000802193aa(2149684138)                  0x00000000802193aa(2149684138)                  
s10(x26)            0x00000000801ef38d(2149512077)                  0x00000000801ef38d(2149512077)                  
s11(x27)            0x000000008020020a(2149581322)                  0x000000008020020a(2149581322)                  
t3(x28)             0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
t4(x29)             0x000000007ffffc8d(2147482765)                  0x000000007ffffc8d(2147482765)                  
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x0000000080000130(2147483952)                  0x0000000080000130(2147483952)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            cc88a749bfac4a7cf625d1dee0b218aace9ec863        cc88a749bfac4a7cf625d1dee0b218aace9ec863        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000744(2147485508)                  0x0000000080000744(2147485508)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000e8(232)                         0x00000000000000e8(232)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            dyn(0b111)                                      dyn(0b111)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffffcefffffd(-2147483264.0_s)             0xffffffffcefffffd(-2147483264.0_s)             
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffffc3200000(-160.0_s)                    0xffffffffc3200000(-160.0_s)                    
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f6                  0xffffffff4eff8000(2143289344.0_s)              0xffffffff4eff8000(2143289344.0_s)              
f7                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff43550000(213.0_s)                     0xffffffff43550000(213.0_s)                     
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffffffffff36(nan_h)                       0xffffffffffffff36(nan_h)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x41e0030075400000(2149057450.0_d)              0x41e0030075400000(2149057450.0_d)              
f30                 0xffffffff4f000005(2147484928.0_s)              0xffffffff4f000005(2147484928.0_s)              
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

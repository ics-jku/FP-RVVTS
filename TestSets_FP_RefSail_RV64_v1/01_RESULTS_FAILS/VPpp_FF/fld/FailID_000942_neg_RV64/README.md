# FailID_000942 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 942
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x65,0x2e,0xff,0xda,0x41
_reg_f6: .byte 0x00,0x00,0x68,0x43,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f10:.byte 0x82,0x13,0x80,0xe0,0xfc,0xff,0xcf,0xc3
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x82,0x13,0x80,0xe0,0xfc,0xff,0xcf,0xc3
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x65,0x2e,0xff,0xda,0x41
_reg_f20:.byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f21:.byte 0x0e,0xaf,0xab,0x00,0xf8,0x1c,0x3f,0xde
_reg_f22:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0xc7,0x72,0xed,0xec,0x26,0x82,0x15,0x44
_reg_f25:.byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0x41
_reg_f26:.byte 0x00,0x00,0xc0,0x5c,0x00,0x03,0xe0,0xc1
_reg_f27:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x40,0x70,0xfe,0xff,0xdf,0xc1
_reg_f29:.byte 0xc7,0x72,0xed,0xec,0x26,0x82,0x15,0x44
_reg_f30:.byte 0x00,0x00,0x1f,0x43,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x10
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xffffffffffffffff    // ra
    li x2, 0x8018055a            // sp
    li x3, 0x1                   // gp
    li x4, 0x0                   // tp
    li x5, 0x80000809            // t0
    li x6, 0x800008              // t1
    li x7, 0x1                   // t2
    li x8, 0x1                   // fp
    li x9, 0x1                   // s1
    li x10, 0x1                  // a0
    li x11, 0x6000               // a1
    li x12, 0x1                  // a2
    li x13, 0xe158f74c           // a3
    li x14, 0x9aef9730           // a4
    li x15, 0x6000               // a5
    li x16, 0x801807a1           // a6
    li x17, 0x37                 // a7
    li x18, 0x7ffffacd           // s2
    li x19, 0xe5                 // s3
    li x20, 0x1                  // s4
    li x21, 0x85                 // s5
    li x22, 0x41e0               // s6
    li x23, 0x0                  // s7
    li x24, 0xb5                 // s8
    li x25, 0x800002c6           // s9
    li x26, 0x83                 // s10
    li x27, 0x80000320           // s11
    li x28, 0x8018055a           // t3
    li x29, 0x200                // t4
    li x30, 0x801807d9           // t5
    li x31, 0x8017fec4           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x24'}, 'clob': {'f21', 'x26', 'x24'}})
    
    li x26, 0x1ffff8
    and x24, x24, x26
    li x26, 0x80000092
    add x24, x24, x26
    fld f21, -0x92(x24)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f21                 0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    0x0b11bc230b01b823(2.3622870408526574e-255_d)   X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f21, -0x92(x24)
+========================================================================================================================+
Attributes:  fcsr ['invalid']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f21                 0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    0x0b11bc230b01b823(2.3622870408526574e-255_d)   X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f21, x92, x24
s8(x24)             0x0000000080000142(2147483970)                  0x0000000080000142(2147483970)
f21                 0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    0x0b11bc230b01b823(2.3622870408526574e-255_d)   X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
sp(x2)              0x000000008018055a(2149057882)                  0x000000008018055a(2149057882)                  
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000080000809(2147485705)                  0x0000000080000809(2147485705)                  
t1(x6)              0x0000000000800008(8388616)                     0x0000000000800008(8388616)                     
t2(x7)              0x0000000000000001(1)                           0x0000000000000001(1)                           
fp(x8)              0x0000000000000001(1)                           0x0000000000000001(1)                           
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a2(x12)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a3(x13)             0x00000000e158f74c(3780704076)                  0x00000000e158f74c(3780704076)                  
a4(x14)             0x000000009aef9730(2599393072)                  0x000000009aef9730(2599393072)                  
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x00000000801807a1(2149058465)                  0x00000000801807a1(2149058465)                  
a7(x17)             0x0000000000000037(55)                          0x0000000000000037(55)                          
s2(x18)             0x000000007ffffacd(2147482317)                  0x000000007ffffacd(2147482317)                  
s3(x19)             0x00000000000000e5(229)                         0x00000000000000e5(229)                         
s4(x20)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s5(x21)             0x0000000000000085(133)                         0x0000000000000085(133)                         
s6(x22)             0x00000000000041e0(16864)                       0x00000000000041e0(16864)                       
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x0000000080000142(2147483970)                  0x0000000080000142(2147483970)                  
s9(x25)             0x00000000800002c6(2147484358)                  0x00000000800002c6(2147484358)                  
s10(x26)            0x0000000080000092(2147483794)                  0x0000000080000092(2147483794)                  
s11(x27)            0x0000000080000320(2147484448)                  0x0000000080000320(2147484448)                  
t3(x28)             0x000000008018055a(2149057882)                  0x000000008018055a(2149057882)                  
t4(x29)             0x0000000000000200(512)                         0x0000000000000200(512)                         
t5(x30)             0x00000000801807d9(2149058521)                  0x00000000801807d9(2149058521)                  
t6(x31)             0x000000008017fec4(2149056196)                  0x000000008017fec4(2149056196)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            e638753d42e1635e361fa807df8a340c4a8b3319        e638753d42e1635e361fa807df8a340c4a8b3319        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000710(2147485456)                  0x0000000080000710(2147485456)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000010(16)                          0x0000000000000010(16)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f5                  0x41daff2e65000000(1811724692.0_d)              0x41daff2e65000000(1811724692.0_d)              
f6                  0xffffffff43680000(232.0_s)                     0xffffffff43680000(232.0_s)                     
f7                  0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f10                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0xc3cffffce0801382(-4.6116791507772385e+18_d)   
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xc3cffffce0801382(-4.6116791507772385e+18_d)   0xc3cffffce0801382(-4.6116791507772385e+18_d)   
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f16                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f17                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x41daff2e65000000(1811724692.0_d)              0x41daff2e65000000(1811724692.0_d)              
f20                 0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f21                 0xde3f1cf800abaf0e(-9.71274596897266e+145_d)    0x0b11bc230b01b823(2.3622870408526574e-255_d)   X
f22                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x44158226eced72c7(9.919001733163082e+19_d)     0x44158226eced72c7(9.919001733163082e+19_d)     
f25                 0x41dffffe70400000(2147482049.0_d)              0x41dffffe70400000(2147482049.0_d)              
f26                 0xc1e003005cc00000(-2149057254.0_d)             0xc1e003005cc00000(-2149057254.0_d)             
f27                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f28                 0xc1dffffe70400000(-2147482049.0_d)             0xc1dffffe70400000(-2147482049.0_d)             
f29                 0x44158226eced72c7(9.919001733163082e+19_d)     0x44158226eced72c7(9.919001733163082e+19_d)     
f30                 0xffffffff431f0000(159.0_s)                     0xffffffff431f0000(159.0_s)                     
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

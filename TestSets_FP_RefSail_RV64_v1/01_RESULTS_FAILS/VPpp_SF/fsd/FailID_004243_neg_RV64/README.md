# FailID_004243 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4243
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
_reg_f1: .byte 0x00,0x00,0xc0,0xd1,0xfe,0xf9,0xdf,0xc1
_reg_f2: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x88,0x37
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xe0,0x66,0x00,0x00,0xe0,0x41
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xe4,0x06,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x60,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f26:.byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x90
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x117                 // ra
    li x2, 0x8027ffb6            // sp
    li x3, 0x8017ff2f            // gp
    li x4, 0x4f8e1c11            // tp
    li x5, 0x80200450            // t0
    li x6, 0x84                  // t1
    li x7, 0x0                   // t2
    li x8, 0x801800c1            // fp
    li x9, 0x7ffff9fb            // s1
    li x10, 0x8017fc26           // a0
    li x11, 0x8018000e           // a1
    li x12, 0x1                  // a2
    li x13, 0x801ffb8b           // a3
    li x14, 0x80185e72           // a4
    li x15, 0x800014f9           // a5
    li x16, 0x80180694           // a6
    li x17, 0x1                  // a7
    li x18, 0x801dff16           // s2
    li x19, 0xffffffff80f208e2   // s3
    li x20, 0x8017fb4e           // s4
    li x21, 0x801807ea           // s5
    li x22, 0x6000               // s6
    li x23, 0xffffffffe6be2000   // s7
    li x24, 0xffe7fe11           // s8
    li x25, 0x7ffffdb6           // s9
    li x26, 0x800004d8           // s10
    li x27, 0xffffffffcb6a2000   // s11
    li x28, 0x7a                 // t3
    li x29, 0x8017fa60           // t4
    li x30, 0x0                  // t5
    li x31, 0x8017ff2f           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x29', 'fcsr.rm', 'f27'}, 'clob': {'x29', 'x22'}})
    
    li x22, 0xffff8
    and x29, x29, x22
    li x22, 0x8017fb34
    add x29, x29, x22
    fsd f27, 0x4cc(x29)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        197495e152421a26d5ab1d7c131684a94861953c        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f27, 0x4cc(x29)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        197495e152421a26d5ab1d7c131684a94861953c        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f27, x4, x29
tp(x4)              0x000000004f8e1c11(1334713361)                  0x000000004f8e1c11(1334713361)
t4(x29)             0x00000000801ff594(2149578132)                  0x00000000801ff594(2149578132)
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000117(279)                         0x0000000000000117(279)                         
sp(x2)              0x000000008027ffb6(2150105014)                  0x000000008027ffb6(2150105014)                  
gp(x3)              0x000000008017ff2f(2149056303)                  0x000000008017ff2f(2149056303)                  
tp(x4)              0x000000004f8e1c11(1334713361)                  0x000000004f8e1c11(1334713361)                  
t0(x5)              0x0000000080200450(2149581904)                  0x0000000080200450(2149581904)                  
t1(x6)              0x0000000000000084(132)                         0x0000000000000084(132)                         
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x00000000801800c1(2149056705)                  0x00000000801800c1(2149056705)                  
s1(x9)              0x000000007ffff9fb(2147482107)                  0x000000007ffff9fb(2147482107)                  
a0(x10)             0x000000008017fc26(2149055526)                  0x000000008017fc26(2149055526)                  
a1(x11)             0x000000008018000e(2149056526)                  0x000000008018000e(2149056526)                  
a2(x12)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a3(x13)             0x00000000801ffb8b(2149579659)                  0x00000000801ffb8b(2149579659)                  
a4(x14)             0x0000000080185e72(2149080690)                  0x0000000080185e72(2149080690)                  
a5(x15)             0x00000000800014f9(2147489017)                  0x00000000800014f9(2147489017)                  
a6(x16)             0x0000000080180694(2149058196)                  0x0000000080180694(2149058196)                  
a7(x17)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s2(x18)             0x00000000801dff16(2149449494)                  0x00000000801dff16(2149449494)                  
s3(x19)             0xffffffff80f208e2(18446744071577929954)        0xffffffff80f208e2(18446744071577929954)        
s4(x20)             0x000000008017fb4e(2149055310)                  0x000000008017fb4e(2149055310)                  
s5(x21)             0x00000000801807ea(2149058538)                  0x00000000801807ea(2149058538)                  
s6(x22)             0x000000008017fb34(2149055284)                  0x000000008017fb34(2149055284)                  
s7(x23)             0xffffffffe6be2000(18446744073285804032)        0xffffffffe6be2000(18446744073285804032)        
s8(x24)             0x00000000ffe7fe11(4293393937)                  0x00000000ffe7fe11(4293393937)                  
s9(x25)             0x000000007ffffdb6(2147483062)                  0x000000007ffffdb6(2147483062)                  
s10(x26)            0x00000000800004d8(2147484888)                  0x00000000800004d8(2147484888)                  
s11(x27)            0xffffffffcb6a2000(18446744072827314176)        0xffffffffcb6a2000(18446744072827314176)        
t3(x28)             0x000000000000007a(122)                         0x000000000000007a(122)                         
t4(x29)             0x00000000801ff594(2149578132)                  0x00000000801ff594(2149578132)                  
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x000000008017ff2f(2149056303)                  0x000000008017ff2f(2149056303)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            684c94508d52c46dc5921d423ba2c032f5abd519        684c94508d52c46dc5921d423ba2c032f5abd519        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        197495e152421a26d5ab1d7c131684a94861953c        X
lastPC              0x0000000080000768(2147485544)                  0x0000000080000768(2147485544)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000090(144)                         0x0000000000000090(144)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xc1dff9fed1c00000(-2145909575.0_d)             0xc1dff9fed1c00000(-2145909575.0_d)             
f2                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f3                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f9                  0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f10                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0x3788000000000000(3.4438311059246704e-41_d)    0x3788000000000000(3.4438311059246704e-41_d)    
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x41e0000066e00000(2147484471.0_d)              0x41e0000066e00000(2147484471.0_d)              
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x00000000801806e4(1.061775865e-314_d)          0x00000000801806e4(1.061775865e-314_d)          
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffffffff6000(512.0_h)                     0xffffffffffff6000(512.0_h)                     
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f26                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

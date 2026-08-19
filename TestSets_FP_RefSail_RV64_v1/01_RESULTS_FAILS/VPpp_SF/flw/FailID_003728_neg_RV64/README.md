# FailID_003728 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3728
* Isolated failing instruction: `flw`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x20,0xff,0xff,0xdf,0x41
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x40,0x40
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x44,0xff,0xff,0xff,0xff
_reg_f26:.byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x05,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x62
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x1                   // ra
    li x2, 0x801fffae            // sp
    li x3, 0x0                   // gp
    li x4, 0x0                   // tp
    li x5, 0x801bbd33            // t0
    li x6, 0x80180223            // t1
    li x7, 0x6000                // t2
    li x8, 0x7ffffff7            // fp
    li x9, 0x7ffff8d6            // s1
    li x10, 0xffffffff6fdaf728   // a0
    li x11, 0x8000058f           // a1
    li x12, 0x8017f836           // a2
    li x13, 0xee831774           // a3
    li x14, 0x801800d3           // a4
    li x15, 0x1                  // a5
    li x16, 0x3                  // a6
    li x17, 0x7ffff9ae           // a7
    li x18, 0x7ffff9ae           // s2
    li x19, 0x8017f945           // s3
    li x20, 0x8027fcdb           // s4
    li x21, 0x803809fe           // s5
    li x22, 0x7ffff93e           // s6
    li x23, 0x50f6c710           // s7
    li x24, 0x57153000           // s8
    li x25, 0x801860a2           // s9
    li x26, 0x801807bc           // s10
    li x27, 0xffffffffeffb0000   // s11
    li x28, 0x802008d8           // t3
    li x29, 0x80180be7           // t4
    li x30, 0x7ffffff7           // t5
    li x31, 0x3fe77760           // t6
    // INSTRUCTION ({'dep': {'x12', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'x12', 'x19', 'f14'}})
    
    li x19, 0x1ffffc
    and x12, x12, x19
    li x19, 0x7ffffc66
    add x12, x12, x19
    flw f14, 0x39a(x12)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f14                 0x4040000000000000(32.0_d)                      0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f14, 0x39a(x12)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f14                 0x4040000000000000(32.0_d)                      0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x39, x12
a2(x12)             0x000000008017f49a(2149053594)                  0x000000008017f49a(2149053594)
f14                 0x4040000000000000(32.0_d)                      0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000001(1)                           0x0000000000000001(1)                           
sp(x2)              0x00000000801fffae(2149580718)                  0x00000000801fffae(2149580718)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x00000000801bbd33(2149301555)                  0x00000000801bbd33(2149301555)                  
t1(x6)              0x0000000080180223(2149057059)                  0x0000000080180223(2149057059)                  
t2(x7)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
fp(x8)              0x000000007ffffff7(2147483639)                  0x000000007ffffff7(2147483639)                  
s1(x9)              0x000000007ffff8d6(2147481814)                  0x000000007ffff8d6(2147481814)                  
a0(x10)             0xffffffff6fdaf728(18446744071291205416)        0xffffffff6fdaf728(18446744071291205416)        
a1(x11)             0x000000008000058f(2147485071)                  0x000000008000058f(2147485071)                  
a2(x12)             0x000000008017f49a(2149053594)                  0x000000008017f49a(2149053594)                  
a3(x13)             0x00000000ee831774(4001568628)                  0x00000000ee831774(4001568628)                  
a4(x14)             0x00000000801800d3(2149056723)                  0x00000000801800d3(2149056723)                  
a5(x15)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a6(x16)             0x0000000000000003(3)                           0x0000000000000003(3)                           
a7(x17)             0x000000007ffff9ae(2147482030)                  0x000000007ffff9ae(2147482030)                  
s2(x18)             0x000000007ffff9ae(2147482030)                  0x000000007ffff9ae(2147482030)                  
s3(x19)             0x000000007ffffc66(2147482726)                  0x000000007ffffc66(2147482726)                  
s4(x20)             0x000000008027fcdb(2150104283)                  0x000000008027fcdb(2150104283)                  
s5(x21)             0x00000000803809fe(2151156222)                  0x00000000803809fe(2151156222)                  
s6(x22)             0x000000007ffff93e(2147481918)                  0x000000007ffff93e(2147481918)                  
s7(x23)             0x0000000050f6c710(1358350096)                  0x0000000050f6c710(1358350096)                  
s8(x24)             0x0000000057153000(1461006336)                  0x0000000057153000(1461006336)                  
s9(x25)             0x00000000801860a2(2149081250)                  0x00000000801860a2(2149081250)                  
s10(x26)            0x00000000801807bc(2149058492)                  0x00000000801807bc(2149058492)                  
s11(x27)            0xffffffffeffb0000(18446744073440788480)        0xffffffffeffb0000(18446744073440788480)        
t3(x28)             0x00000000802008d8(2149583064)                  0x00000000802008d8(2149583064)                  
t4(x29)             0x0000000080180be7(2149059559)                  0x0000000080180be7(2149059559)                  
t5(x30)             0x000000007ffffff7(2147483639)                  0x000000007ffffff7(2147483639)                  
t6(x31)             0x000000003fe77760(1072133984)                  0x000000003fe77760(1072133984)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            cc11fbc6c27fd5c4407544bbe503573ec306ea80        cc11fbc6c27fd5c4407544bbe503573ec306ea80        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000075c(2147485532)                  0x000000008000075c(2147485532)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000062(98)                          0x0000000000000062(98)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f3                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x41dfffff20000000(2147482752.0_d)              0x41dfffff20000000(2147482752.0_d)              
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x4040000000000000(32.0_d)                      0xffffffff00000000(0.0_s)                       X
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)                     
f26                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff4f001805(2149057792.0_s)              0xffffffff4f001805(2149057792.0_s)              
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

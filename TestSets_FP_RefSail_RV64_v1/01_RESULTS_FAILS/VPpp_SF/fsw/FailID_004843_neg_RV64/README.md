# FailID_004843 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4843
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
_reg_f0: .byte 0x00,0x00,0x80,0x94,0x8a,0xfd,0xdf,0xc1
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x2f,0x06,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x20,0x68,0x40
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x80,0xbf,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xe0,0x20,0x00,0x04,0xe0,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xf3,0x91,0x01,0x34,0x00,0x00,0x00,0x00
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x10,0x40
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0xd6,0x09,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x80,0xf9,0xc8,0x00,0xca,0x41
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0xf7,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x41
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x9088d728            // ra
    li x2, 0x3fa03730            // sp
    li x3, 0x0                   // gp
    li x4, 0x0                   // tp
    li x5, 0x801fec22            // t0
    li x6, 0x2a2                 // t1
    li x7, 0x801803a7            // t2
    li x8, 0x8009d5ae            // fp
    li x9, 0xffffffffffffffff    // s1
    li x10, 0x801de559           // a0
    li x11, 0x8027fbeb           // a1
    li x12, 0x6000               // a2
    li x13, 0x0                  // a3
    li x14, 0x7ffffe00           // a4
    li x15, 0x0                  // a5
    li x16, 0x80186537           // a6
    li x17, 0x80180537           // a7
    li x18, 0xfffffffffffffe2b   // s2
    li x19, 0x80180230           // s3
    li x20, 0x80180230           // s4
    li x21, 0x80218ed4           // s5
    li x22, 0x7ffffe29           // s6
    li x23, 0x8000057c           // s7
    li x24, 0x80186600           // s8
    li x25, 0x8020016a           // s9
    li x26, 0x7ffffb99           // s10
    li x27, 0x80200570           // s11
    li x28, 0x7ceda000           // t3
    li x29, 0x7ffff90b           // t4
    li x30, 0x8017f9fd           // t5
    li x31, 0x8017f9fd           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f7', 'x2'}, 'clob': {'x30', 'x2'}})
    
    li x30, 0xffffc
    and x2, x2, x30
    li x30, 0x8017f83d
    add x2, x2, x30
    fsw f7, 0x7c3(x2)
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
Instruction: fsw f7, 0x7c3(x2)
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f7, x7, c3, x2
sp(x2)              0x0000000080182f6d(2149068653)                  0x0000000080182f6d(2149068653)
t2(x7)              0x00000000801803a7(2149057447)                  0x00000000801803a7(2149057447)
f7                  0x4068200000000000(193.0_d)                     0x4068200000000000(193.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000009088d728(2424887080)                  0x000000009088d728(2424887080)                  
sp(x2)              0x0000000080182f6d(2149068653)                  0x0000000080182f6d(2149068653)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x00000000801fec22(2149575714)                  0x00000000801fec22(2149575714)                  
t1(x6)              0x00000000000002a2(674)                         0x00000000000002a2(674)                         
t2(x7)              0x00000000801803a7(2149057447)                  0x00000000801803a7(2149057447)                  
fp(x8)              0x000000008009d5ae(2148128174)                  0x000000008009d5ae(2148128174)                  
s1(x9)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a0(x10)             0x00000000801de559(2149442905)                  0x00000000801de559(2149442905)                  
a1(x11)             0x000000008027fbeb(2150104043)                  0x000000008027fbeb(2150104043)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x000000007ffffe00(2147483136)                  0x000000007ffffe00(2147483136)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x0000000080186537(2149082423)                  0x0000000080186537(2149082423)                  
a7(x17)             0x0000000080180537(2149057847)                  0x0000000080180537(2149057847)                  
s2(x18)             0xfffffffffffffe2b(18446744073709551147)        0xfffffffffffffe2b(18446744073709551147)        
s3(x19)             0x0000000080180230(2149057072)                  0x0000000080180230(2149057072)                  
s4(x20)             0x0000000080180230(2149057072)                  0x0000000080180230(2149057072)                  
s5(x21)             0x0000000080218ed4(2149682900)                  0x0000000080218ed4(2149682900)                  
s6(x22)             0x000000007ffffe29(2147483177)                  0x000000007ffffe29(2147483177)                  
s7(x23)             0x000000008000057c(2147485052)                  0x000000008000057c(2147485052)                  
s8(x24)             0x0000000080186600(2149082624)                  0x0000000080186600(2149082624)                  
s9(x25)             0x000000008020016a(2149581162)                  0x000000008020016a(2149581162)                  
s10(x26)            0x000000007ffffb99(2147482521)                  0x000000007ffffb99(2147482521)                  
s11(x27)            0x0000000080200570(2149582192)                  0x0000000080200570(2149582192)                  
t3(x28)             0x000000007ceda000(2095947776)                  0x000000007ceda000(2095947776)                  
t4(x29)             0x000000007ffff90b(2147481867)                  0x000000007ffff90b(2147481867)                  
t5(x30)             0x000000008017f83d(2149054525)                  0x000000008017f83d(2149054525)                  
t6(x31)             0x000000008017f9fd(2149054973)                  0x000000008017f9fd(2149054973)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            fe9768380f5722fc56b33f86deb023686cb6f300        fe9768380f5722fc56b33f86deb023686cb6f300        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000076c(2147485548)                  0x000000008000076c(2147485548)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000041(65)                          0x0000000000000041(65)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xc1dffd8a94800000(-2146839122.0_d)             0xc1dffd8a94800000(-2146839122.0_d)             
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff8000062f(-2.2182554690261854e-42_s)   0xffffffff8000062f(-2.2182554690261854e-42_s)   
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x4068200000000000(193.0_d)                     0x4068200000000000(193.0_d)                     
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffffbf800000(-1.0_s)                      0xffffffffbf800000(-1.0_s)                      
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41e0040020e00000(2149581063.0_d)              0x41e0040020e00000(2149581063.0_d)              
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x00000000340191f3(4.31081234e-315_d)           0x00000000340191f3(4.31081234e-315_d)           
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x4010000000000000(4.0_d)                       0x4010000000000000(4.0_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff4f0009d6(2148128256.0_s)              0xffffffff4f0009d6(2148128256.0_s)              
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x41ca00c8f9800000(872518131.0_d)               0x41ca00c8f9800000(872518131.0_d)               
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff4efffff7(2147482496.0_s)              0xffffffff4efffff7(2147482496.0_s)              
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

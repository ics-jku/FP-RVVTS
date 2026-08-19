# FailID_003262 VP++ SF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3262
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0xcd,0xd7,0x40
_reg_f2: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x98,0x00,0x03,0xe0,0x41
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f17:.byte 0x00,0x00,0xe0,0x66,0x00,0x00,0xe0,0x41
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xe0,0x66,0x00,0x00,0xe0,0x41
_reg_f26:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0x80,0x6c,0x07,0xf6,0xdf,0xc1
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
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
    li x1, 0x7ffffd07            // ra
    li x2, 0x8017fc11            // sp
    li x3, 0x1                   // gp
    li x4, 0x8017f7ec            // tp
    li x5, 0x6000                // t0
    li x6, 0x801804c0            // t1
    li x7, 0x800001de            // t2
    li x8, 0xa1                  // fp
    li x9, 0x80180751            // s1
    li x10, 0x32ca5718           // a0
    li x11, 0x0                  // a1
    li x12, 0x801fff92           // a2
    li x13, 0x6000               // a3
    li x14, 0x7ffffeea           // a4
    li x15, 0x0                  // a5
    li x16, 0x801800ef           // a6
    li x17, 0xffffffffe4772000   // a7
    li x18, 0xffffffff7fc00000   // s2
    li x19, 0x80180295           // s3
    li x20, 0x0                  // s4
    li x21, 0xffffffff800004a9   // s5
    li x22, 0x8018005d           // s6
    li x23, 0x7fffffff801        // s7
    li x24, 0x79                 // s8
    li x25, 0x9c                 // s9
    li x26, 0x0                  // s10
    li x27, 0xc2                 // s11
    li x28, 0x800000a8           // t3
    li x29, 0x6000               // t4
    li x30, 0x80000808           // t5
    li x31, 0x800002a8           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x21', 'fcsr.rm'}, 'clob': {'x21', 'x20', 'f19'}})
    
    li x20, 0x1ffff8
    and x21, x21, x20
    li x20, 0x7ffffb36
    add x21, x21, x20
    fld f19, 0x4ca(x21)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0xffffffff7fc00000(nan_s)                       0xee82829300000297(-2.1410879581002543e+224_d)  X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f19, 0x4ca(x21)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0xffffffff7fc00000(nan_s)                       0xee82829300000297(-2.1410879581002543e+224_d)  X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f19, x4, x21
tp(x4)              0x000000008017f7ec(2149054444)                  0x000000008017f7ec(2149054444)
s5(x21)             0x000000007fffffde(2147483614)                  0x000000007fffffde(2147483614)
f19                 0xffffffff7fc00000(nan_s)                       0xee82829300000297(-2.1410879581002543e+224_d)  X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffffd07(2147482887)                  0x000000007ffffd07(2147482887)                  
sp(x2)              0x000000008017fc11(2149055505)                  0x000000008017fc11(2149055505)                  
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x000000008017f7ec(2149054444)                  0x000000008017f7ec(2149054444)                  
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t1(x6)              0x00000000801804c0(2149057728)                  0x00000000801804c0(2149057728)                  
t2(x7)              0x00000000800001de(2147484126)                  0x00000000800001de(2147484126)                  
fp(x8)              0x00000000000000a1(161)                         0x00000000000000a1(161)                         
s1(x9)              0x0000000080180751(2149058385)                  0x0000000080180751(2149058385)                  
a0(x10)             0x0000000032ca5718(852121368)                   0x0000000032ca5718(852121368)                   
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x00000000801fff92(2149580690)                  0x00000000801fff92(2149580690)                  
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x000000007ffffeea(2147483370)                  0x000000007ffffeea(2147483370)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x00000000801800ef(2149056751)                  0x00000000801800ef(2149056751)                  
a7(x17)             0xffffffffe4772000(18446744073247596544)        0xffffffffe4772000(18446744073247596544)        
s2(x18)             0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
s3(x19)             0x0000000080180295(2149057173)                  0x0000000080180295(2149057173)                  
s4(x20)             0x000000007ffffb36(2147482422)                  0x000000007ffffb36(2147482422)                  
s5(x21)             0x000000007fffffde(2147483614)                  0x000000007fffffde(2147483614)                  
s6(x22)             0x000000008018005d(2149056605)                  0x000000008018005d(2149056605)                  
s7(x23)             0x000007fffffff801(8796093020161)               0x000007fffffff801(8796093020161)               
s8(x24)             0x0000000000000079(121)                         0x0000000000000079(121)                         
s9(x25)             0x000000000000009c(156)                         0x000000000000009c(156)                         
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x00000000000000c2(194)                         0x00000000000000c2(194)                         
t3(x28)             0x00000000800000a8(2147483816)                  0x00000000800000a8(2147483816)                  
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x0000000080000808(2147485704)                  0x0000000080000808(2147485704)                  
t6(x31)             0x00000000800002a8(2147484328)                  0x00000000800002a8(2147484328)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            2c7a49bbac3469d3bc7e8a16a22ebe72bd6a22ef        2c7a49bbac3469d3bc7e8a16a22ebe72bd6a22ef        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
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
f0                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f1                  0x40d7cd0000000000(24372.0_d)                   0x40d7cd0000000000(24372.0_d)                   
f2                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f7                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f11                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x41e0030098000000(2149057728.0_d)              0x41e0030098000000(2149057728.0_d)              
f16                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f17                 0x41e0000066e00000(2147484471.0_d)              0x41e0000066e00000(2147484471.0_d)              
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xee82829300000297(-2.1410879581002543e+224_d)  X
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x41e0000066e00000(2147484471.0_d)              0x41e0000066e00000(2147484471.0_d)              
f26                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0xc1dff6076c800000(-2144869810.0_d)             0xc1dff6076c800000(-2144869810.0_d)             
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
STATES DIFFER: True
```

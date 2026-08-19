# FailID_002025 VP++ FF neg RV64 fsh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2025
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x2f,0x06,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x20,0x68,0x40
_reg_f8: .byte 0x00,0x00,0xe0,0x20,0x00,0x04,0xe0,0x41
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0xeb,0xfb,0x27,0x80,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xe0,0x20,0x00,0x04,0xe0,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x10,0x40
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0xd6,0x09,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0xf7,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x53,0x09,0x00,0xd2,0xff,0xff,0xff,0xff
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
    li x1, 0x9088d728            // ra
    li x2, 0x8017ffb7            // sp
    li x3, 0x801ffb84            // gp
    li x4, 0x801800b2            // tp
    li x5, 0x801fec22            // t0
    li x6, 0x80180149            // t1
    li x7, 0x6000                // t2
    li x8, 0x340191f3            // fp
    li x9, 0x37523000            // s1
    li x10, 0xbf0b4750           // a0
    li x11, 0x80218ed4           // a1
    li x12, 0x6000               // a2
    li x13, 0xffffffffffff006f   // a3
    li x14, 0x7ffffe00           // a4
    li x15, 0x0                  // a5
    li x16, 0x109                // a6
    li x17, 0x5ab04000           // a7
    li x18, 0x8027fff8           // s2
    li x19, 0x0                  // s3
    li x20, 0x80180230           // s4
    li x21, 0x80218ed4           // s5
    li x22, 0x801800b2           // s6
    li x23, 0x4                  // s7
    li x24, 0x80000340           // s8
    li x25, 0xffffffffffffffff   // s9
    li x26, 0x801801d0           // s10
    li x27, 0x7fffffb1           // s11
    li x28, 0x8017fb26           // t3
    li x29, 0x80185fb7           // t4
    li x30, 0x801ff55b           // t5
    li x31, 0xf1                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f13', 'mstatus.fs/vs.fs', 'x24'}, 'clob': {'x24', 'x21'}})
    
    li x21, 0xffffe
    and x24, x24, x21
    li x21, 0x8018015e
    add x24, x24, x21
    fsh f13, -0x15e(x24)
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
Instruction: fsh f13, -0x15e(x24)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x15, x24
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)
s8(x24)             0x000000008018049e(2149057694)                  0x000000008018049e(2149057694)
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000009088d728(2424887080)                  0x000000009088d728(2424887080)                  
sp(x2)              0x000000008017ffb7(2149056439)                  0x000000008017ffb7(2149056439)                  
gp(x3)              0x00000000801ffb84(2149579652)                  0x00000000801ffb84(2149579652)                  
tp(x4)              0x00000000801800b2(2149056690)                  0x00000000801800b2(2149056690)                  
t0(x5)              0x00000000801fec22(2149575714)                  0x00000000801fec22(2149575714)                  
t1(x6)              0x0000000080180149(2149056841)                  0x0000000080180149(2149056841)                  
t2(x7)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
fp(x8)              0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
s1(x9)              0x0000000037523000(928133120)                   0x0000000037523000(928133120)                   
a0(x10)             0x00000000bf0b4750(3205187408)                  0x00000000bf0b4750(3205187408)                  
a1(x11)             0x0000000080218ed4(2149682900)                  0x0000000080218ed4(2149682900)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0xffffffffffff006f(18446744073709486191)        0xffffffffffff006f(18446744073709486191)        
a4(x14)             0x000000007ffffe00(2147483136)                  0x000000007ffffe00(2147483136)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x0000000000000109(265)                         0x0000000000000109(265)                         
a7(x17)             0x000000005ab04000(1521500160)                  0x000000005ab04000(1521500160)                  
s2(x18)             0x000000008027fff8(2150105080)                  0x000000008027fff8(2150105080)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x0000000080180230(2149057072)                  0x0000000080180230(2149057072)                  
s5(x21)             0x000000008018015e(2149056862)                  0x000000008018015e(2149056862)                  
s6(x22)             0x00000000801800b2(2149056690)                  0x00000000801800b2(2149056690)                  
s7(x23)             0x0000000000000004(4)                           0x0000000000000004(4)                           
s8(x24)             0x000000008018049e(2149057694)                  0x000000008018049e(2149057694)                  
s9(x25)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s10(x26)            0x00000000801801d0(2149056976)                  0x00000000801801d0(2149056976)                  
s11(x27)            0x000000007fffffb1(2147483569)                  0x000000007fffffb1(2147483569)                  
t3(x28)             0x000000008017fb26(2149055270)                  0x000000008017fb26(2149055270)                  
t4(x29)             0x0000000080185fb7(2149081015)                  0x0000000080185fb7(2149081015)                  
t5(x30)             0x00000000801ff55b(2149578075)                  0x00000000801ff55b(2149578075)                  
t6(x31)             0x00000000000000f1(241)                         0x00000000000000f1(241)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            96e3bc1521361e257f5ae7ebce39d225361443b7        96e3bc1521361e257f5ae7ebce39d225361443b7        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000076c(2147485548)                  0x000000008000076c(2147485548)                  
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
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff8000062f(-2.2182554690261854e-42_s)   0xffffffff8000062f(-2.2182554690261854e-42_s)   
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x4068200000000000(193.0_d)                     0x4068200000000000(193.0_d)                     
f8                  0x41e0040020e00000(2149581063.0_d)              0x41e0040020e00000(2149581063.0_d)              
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff8027fbeb(-3.671955489424429e-39_s)    0xffffffff8027fbeb(-3.671955489424429e-39_s)    
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41e0040020e00000(2149581063.0_d)              0x41e0040020e00000(2149581063.0_d)              
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x4010000000000000(4.0_d)                       0x4010000000000000(4.0_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff4f0009d6(2148128256.0_s)              0xffffffff4f0009d6(2148128256.0_s)              
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff4efffff7(2147482496.0_s)              0xffffffff4efffff7(2147482496.0_s)              
f30                 0xffffffffd2000953(-137478062080.0_s)           0xffffffffd2000953(-137478062080.0_s)           
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

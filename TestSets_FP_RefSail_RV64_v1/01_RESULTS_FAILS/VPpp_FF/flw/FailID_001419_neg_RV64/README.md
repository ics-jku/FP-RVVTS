# FailID_001419 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1419
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
    li x1, 0x0                   // ra
    li x2, 0x801806bd            // sp
    li x3, 0x0                   // gp
    li x4, 0x80000029            // tp
    li x5, 0x801ff206            // t0
    li x6, 0x80180740            // t1
    li x7, 0x801ff55d            // t2
    li x8, 0x7ffffca3            // fp
    li x9, 0x801ffcb8            // s1
    li x10, 0xa6                 // a0
    li x11, 0x6515c000           // a1
    li x12, 0x800004f2           // a2
    li x13, 0x800004f2           // a3
    li x14, 0x20                 // a4
    li x15, 0xfffffffffffffff9   // a5
    li x16, 0x1d604720           // a6
    li x17, 0xffffffffa6adc000   // a7
    li x18, 0x695                // s2
    li x19, 0xdd243750           // s3
    li x20, 0x20                 // s4
    li x21, 0x7ffff96f           // s5
    li x22, 0x8017ff77           // s6
    li x23, 0xd6                 // s7
    li x24, 0xf3                 // s8
    li x25, 0x7ffff96f           // s9
    li x26, 0x80180527           // s10
    li x27, 0x802002a9           // s11
    li x28, 0x0                  // t3
    li x29, 0x801803c2           // t4
    li x30, 0x80180045           // t5
    li x31, 0xf3                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x6'}, 'clob': {'x6', 'x23', 'f22'}})
    
    li x23, 0x1ffffc
    and x6, x6, x23
    li x23, 0x800001f4
    add x6, x6, x23
    flw f22, -0x1f4(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f22, -0x1f4(x6)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f22, x1, f4, x6
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)
t1(x6)              0x0000000080180934(2149058868)                  0x0000000080180934(2149058868)
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x00000000801806bd(2149058237)                  0x00000000801806bd(2149058237)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x0000000080000029(2147483689)                  0x0000000080000029(2147483689)                  
t0(x5)              0x00000000801ff206(2149577222)                  0x00000000801ff206(2149577222)                  
t1(x6)              0x0000000080180934(2149058868)                  0x0000000080180934(2149058868)                  
t2(x7)              0x00000000801ff55d(2149578077)                  0x00000000801ff55d(2149578077)                  
fp(x8)              0x000000007ffffca3(2147482787)                  0x000000007ffffca3(2147482787)                  
s1(x9)              0x00000000801ffcb8(2149579960)                  0x00000000801ffcb8(2149579960)                  
a0(x10)             0x00000000000000a6(166)                         0x00000000000000a6(166)                         
a1(x11)             0x000000006515c000(1695924224)                  0x000000006515c000(1695924224)                  
a2(x12)             0x00000000800004f2(2147484914)                  0x00000000800004f2(2147484914)                  
a3(x13)             0x00000000800004f2(2147484914)                  0x00000000800004f2(2147484914)                  
a4(x14)             0x0000000000000020(32)                          0x0000000000000020(32)                          
a5(x15)             0xfffffffffffffff9(18446744073709551609)        0xfffffffffffffff9(18446744073709551609)        
a6(x16)             0x000000001d604720(492848928)                   0x000000001d604720(492848928)                   
a7(x17)             0xffffffffa6adc000(18446744072210989056)        0xffffffffa6adc000(18446744072210989056)        
s2(x18)             0x0000000000000695(1685)                        0x0000000000000695(1685)                        
s3(x19)             0x00000000dd243750(3710138192)                  0x00000000dd243750(3710138192)                  
s4(x20)             0x0000000000000020(32)                          0x0000000000000020(32)                          
s5(x21)             0x000000007ffff96f(2147481967)                  0x000000007ffff96f(2147481967)                  
s6(x22)             0x000000008017ff77(2149056375)                  0x000000008017ff77(2149056375)                  
s7(x23)             0x00000000800001f4(2147484148)                  0x00000000800001f4(2147484148)                  
s8(x24)             0x00000000000000f3(243)                         0x00000000000000f3(243)                         
s9(x25)             0x000000007ffff96f(2147481967)                  0x000000007ffff96f(2147481967)                  
s10(x26)            0x0000000080180527(2149057831)                  0x0000000080180527(2149057831)                  
s11(x27)            0x00000000802002a9(2149581481)                  0x00000000802002a9(2149581481)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x00000000801803c2(2149057474)                  0x00000000801803c2(2149057474)                  
t5(x30)             0x0000000080180045(2149056581)                  0x0000000080180045(2149056581)                  
t6(x31)             0x00000000000000f3(243)                         0x00000000000000f3(243)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            5e3a5f720360d5d69a0bb7d0e547f2cfbab55d75        5e3a5f720360d5d69a0bb7d0e547f2cfbab55d75        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
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
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
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

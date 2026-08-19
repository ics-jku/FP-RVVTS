# FailID_004208 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4208
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x4f,0xfd,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f2: .byte 0xfb,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x04,0x20,0x80,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0xbf,0xf9,0x17,0x80,0x00,0x00,0x00,0x00
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x58,0xfe,0xff,0xdf,0x41
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x4f,0xfd,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x09,0x02,0xe8,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x40,0xc7,0x44,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x09,0x02,0xe8,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0xbf
_reg_f30:.byte 0xfb,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
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
    li x1, 0x80180464            // ra
    li x2, 0x8017dbfe            // sp
    li x3, 0x6000                // gp
    li x4, 0x1                   // tp
    li x5, 0x6000                // t0
    li x6, 0x6000                // t1
    li x7, 0x8018007c            // t2
    li x8, 0x80052efe            // fp
    li x9, 0x200                 // s1
    li x10, 0xffffffffffffffff   // a0
    li x11, 0x0                  // a1
    li x12, 0x7fffffff           // a2
    li x13, 0x8007f83b           // a3
    li x14, 0x0                  // a4
    li x15, 0x80005e59           // a5
    li x16, 0xffffffffffffffff   // a6
    li x17, 0xfffffffffffff9f1   // a7
    li x18, 0xd284730            // s2
    li x19, 0xbe7b0760           // s3
    li x20, 0x801ffdec           // s4
    li x21, 0x2                  // s5
    li x22, 0xffffffff7fe80209   // s6
    li x23, 0x7ffff983           // s7
    li x24, 0x80186464           // s8
    li x25, 0x0                  // s9
    li x26, 0x10                 // s10
    li x27, 0x801807d2           // s11
    li x28, 0x7ffffefe           // t3
    li x29, 0x0                  // t4
    li x30, 0x7ffffd80           // t5
    li x31, 0xffffffffffffffff   // t6
    // INSTRUCTION ({'dep': {'x11', 'fcsr.rm', 'mstatus.fs/vs.fs', 'f1'}, 'clob': {'x11', 'x29'}})
    
    li x29, 0xffff8
    and x11, x11, x29
    li x29, 0x801802a5
    add x11, x11, x29
    fsd f1, -0x2a5(x11)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        909037298e95f8b0fff65bfecae4fbb3b84a04c1        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f1, -0x2a5(x11)
+========================================================================================================================+
Attributes:  fcsr ['invalid']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        909037298e95f8b0fff65bfecae4fbb3b84a04c1        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f1, x2, a5, x11
sp(x2)              0x000000008017dbfe(2149047294)                  0x000000008017dbfe(2149047294)
a1(x11)             0x00000000801802a5(2149057189)                  0x00000000801802a5(2149057189)
f1                  0xffffffff8017fd4f(-2.2030864131498693e-39_s)   0xffffffff8017fd4f(-2.2030864131498693e-39_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080180464(2149057636)                  0x0000000080180464(2149057636)                  
sp(x2)              0x000000008017dbfe(2149047294)                  0x000000008017dbfe(2149047294)                  
gp(x3)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
tp(x4)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t1(x6)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t2(x7)              0x000000008018007c(2149056636)                  0x000000008018007c(2149056636)                  
fp(x8)              0x0000000080052efe(2147823358)                  0x0000000080052efe(2147823358)                  
s1(x9)              0x0000000000000200(512)                         0x0000000000000200(512)                         
a0(x10)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a1(x11)             0x00000000801802a5(2149057189)                  0x00000000801802a5(2149057189)                  
a2(x12)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a3(x13)             0x000000008007f83b(2148005947)                  0x000000008007f83b(2148005947)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000080005e59(2147507801)                  0x0000000080005e59(2147507801)                  
a6(x16)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a7(x17)             0xfffffffffffff9f1(18446744073709550065)        0xfffffffffffff9f1(18446744073709550065)        
s2(x18)             0x000000000d284730(220743472)                   0x000000000d284730(220743472)                   
s3(x19)             0x00000000be7b0760(3195733856)                  0x00000000be7b0760(3195733856)                  
s4(x20)             0x00000000801ffdec(2149580268)                  0x00000000801ffdec(2149580268)                  
s5(x21)             0x0000000000000002(2)                           0x0000000000000002(2)                           
s6(x22)             0xffffffff7fe80209(18446744071560495625)        0xffffffff7fe80209(18446744071560495625)        
s7(x23)             0x000000007ffff983(2147481987)                  0x000000007ffff983(2147481987)                  
s8(x24)             0x0000000080186464(2149082212)                  0x0000000080186464(2149082212)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000010(16)                          0x0000000000000010(16)                          
s11(x27)            0x00000000801807d2(2149058514)                  0x00000000801807d2(2149058514)                  
t3(x28)             0x000000007ffffefe(2147483390)                  0x000000007ffffefe(2147483390)                  
t4(x29)             0x00000000801802a5(2149057189)                  0x00000000801802a5(2149057189)                  
t5(x30)             0x000000007ffffd80(2147483008)                  0x000000007ffffd80(2147483008)                  
t6(x31)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        

STATE               REF                                             DUT                                             DIFF
xmemhash            7d1643e4af48b9e463097cfb63328a06eab41eb9        7d1643e4af48b9e463097cfb63328a06eab41eb9        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        909037298e95f8b0fff65bfecae4fbb3b84a04c1        X
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
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
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff8017fd4f(-2.2030864131498693e-39_s)   0xffffffff8017fd4f(-2.2030864131498693e-39_s)   
f2                  0xffffffff4efffffb(2147483008.0_s)              0xffffffff4efffffb(2147483008.0_s)              
f3                  0xffffffff4f802004(4299163648.0_s)              0xffffffff4f802004(4299163648.0_s)              
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x000000008017f9bf(1.0617742026e-314_d)         0x000000008017f9bf(1.0617742026e-314_d)         
f6                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x41dffffe58000000(2147481952.0_d)              0x41dffffe58000000(2147481952.0_d)              
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff8017fd4f(-2.2030864131498693e-39_s)   0xffffffff8017fd4f(-2.2030864131498693e-39_s)   
f15                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f16                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f17                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fe80209(nan_s)                       0xffffffff7fe80209(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff44c74000(1594.0_s)                    0xffffffff44c74000(1594.0_s)                    
f25                 0xffffffff7fe80209(nan_s)                       0xffffffff7fe80209(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f28                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f29                 0xbff0000000000000(-1.0_d)                      0xbff0000000000000(-1.0_d)                      
f30                 0xffffffff4efffffb(2147483008.0_s)              0xffffffff4efffffb(2147483008.0_s)              
f31                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
STATES DIFFER: True
```

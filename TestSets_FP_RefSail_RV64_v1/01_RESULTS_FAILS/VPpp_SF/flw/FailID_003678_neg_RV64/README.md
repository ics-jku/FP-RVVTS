# FailID_003678 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3678
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x4f,0xfd,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x80,0x44,0xff,0xf9,0xdf,0xc1
_reg_f4: .byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0xde,0x02,0x28,0x80,0x00,0x00,0x00,0x00
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x8b,0xf8,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x4f,0xfd,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x04,0x20,0x80,0x4f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x4f,0xfd,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x00,0x00,0x00,0xa8,0x09,0xca,0x41
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': True, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x38
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x200                 // ra
    li x2, 0x6000                // sp
    li x3, 0x28                  // gp
    li x4, 0x801802ee            // tp
    li x5, 0xffffffffffffffff    // t0
    li x6, 0x7ffff960            // t1
    li x7, 0x7fffffff            // t2
    li x8, 0x6000                // fp
    li x9, 0x34135000            // s1
    li x10, 0x80005960           // a0
    li x11, 0x7fffffff           // a1
    li x12, 0x0                  // a2
    li x13, 0x80000730           // a3
    li x14, 0x7ffffd22           // a4
    li x15, 0x6000               // a5
    li x16, 0x80180686           // a6
    li x17, 0x6c434000           // a7
    li x18, 0x801801bc           // s2
    li x19, 0x800000bc           // s3
    li x20, 0x0                  // s4
    li x21, 0x1                  // s5
    li x22, 0xffffffffffffffff   // s6
    li x23, 0x0                  // s7
    li x24, 0x6000               // s8
    li x25, 0x7fffffff           // s9
    li x26, 0x0                  // s10
    li x27, 0x0                  // s11
    li x28, 0x801802ee           // t3
    li x29, 0x1                  // t4
    li x30, 0x482                // t5
    li x31, 0x7fffffffffffffff   // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x21', 'fcsr.rm'}, 'clob': {'x21', 'f0', 'x19'}})
    
    li x19, 0x1ffffc
    and x21, x21, x19
    li x19, 0x7ffffe71
    add x21, x21, x19
    flw f0, 0x18f(x21)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f0, 0x18f(x21)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f0, x18, x21
s2(x18)             0x00000000801801bc(2149056956)                  0x00000000801801bc(2149056956)
s5(x21)             0x000000007ffffe71(2147483249)                  0x000000007ffffe71(2147483249)
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000200(512)                         0x0000000000000200(512)                         
sp(x2)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
gp(x3)              0x0000000000000028(40)                          0x0000000000000028(40)                          
tp(x4)              0x00000000801802ee(2149057262)                  0x00000000801802ee(2149057262)                  
t0(x5)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t1(x6)              0x000000007ffff960(2147481952)                  0x000000007ffff960(2147481952)                  
t2(x7)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
fp(x8)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s1(x9)              0x0000000034135000(873680896)                   0x0000000034135000(873680896)                   
a0(x10)             0x0000000080005960(2147506528)                  0x0000000080005960(2147506528)                  
a1(x11)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x0000000080000730(2147485488)                  0x0000000080000730(2147485488)                  
a4(x14)             0x000000007ffffd22(2147482914)                  0x000000007ffffd22(2147482914)                  
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x0000000080180686(2149058182)                  0x0000000080180686(2149058182)                  
a7(x17)             0x000000006c434000(1816346624)                  0x000000006c434000(1816346624)                  
s2(x18)             0x00000000801801bc(2149056956)                  0x00000000801801bc(2149056956)                  
s3(x19)             0x000000007ffffe71(2147483249)                  0x000000007ffffe71(2147483249)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x000000007ffffe71(2147483249)                  0x000000007ffffe71(2147483249)                  
s6(x22)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x00000000801802ee(2149057262)                  0x00000000801802ee(2149057262)                  
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x0000000000000482(1154)                        0x0000000000000482(1154)                        
t6(x31)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         

STATE               REF                                             DUT                                             DIFF
xmemhash            4fa1009852a6157076e33d94d6d12ae4cb4b910c        4fa1009852a6157076e33d94d6d12ae4cb4b910c        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800006f8(2147485432)                  0x00000000800006f8(2147485432)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000038(56)                          0x0000000000000038(56)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff2140006f(6.505270420568022e-19_s)     X
f1                  0xffffffff8017fd4f(-2.2030864131498693e-39_s)   0xffffffff8017fd4f(-2.2030864131498693e-39_s)   
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xc1dff9ff44800000(-2145910034.0_d)             0xc1dff9ff44800000(-2145910034.0_d)             
f4                  0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0x00000000802802de(1.0622934216e-314_d)         0x00000000802802de(1.0622934216e-314_d)         
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xfffffffffffff88b(-37216.0_h)                  0xfffffffffffff88b(-37216.0_h)                  
f12                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff8017fd4f(-2.2030864131498693e-39_s)   0xffffffff8017fd4f(-2.2030864131498693e-39_s)   
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff4f802004(4299163648.0_s)              0xffffffff4f802004(4299163648.0_s)              
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff8017fd4f(-2.2030864131498693e-39_s)   0xffffffff8017fd4f(-2.2030864131498693e-39_s)   
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x41ca09a800000000(873680896.0_d)               0x41ca09a800000000(873680896.0_d)               
STATES DIFFER: True
```

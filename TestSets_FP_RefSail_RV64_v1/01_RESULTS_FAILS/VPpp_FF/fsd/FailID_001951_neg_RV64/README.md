# FailID_001951 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1951
* Isolated failing instruction: `fsd`
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
_reg_f2: .byte 0x00,0x00,0xe0,0x31,0x00,0x00,0xe0,0x41
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x93,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0xfa,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x5a,0xfe,0x27,0x80,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0x7f
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
    li x1, 0x8000069f            // ra
    li x2, 0x802009d3            // sp
    li x3, 0xfffffffffffffdf5    // gp
    li x4, 0x20000104c00         // tp
    li x5, 0x8020017f            // t0
    li x6, 0x801ffd40            // t1
    li x7, 0x4                   // t2
    li x8, 0x80180327            // fp
    li x9, 0x7ffffd00            // s1
    li x10, 0x8000016f           // a0
    li x11, 0x800004f1           // a1
    li x12, 0x8000078f           // a2
    li x13, 0x8017febd           // a3
    li x14, 0x1                  // a4
    li x15, 0x2008               // a5
    li x16, 0xde4dfff4           // a6
    li x17, 0x5e5a0149           // a7
    li x18, 0x80000413           // s2
    li x19, 0xffffffffffffffff   // s3
    li x20, 0x98c8c798           // s4
    li x21, 0x8000038c           // s5
    li x22, 0x7fffffffffffffff   // s6
    li x23, 0xfbc9475c           // s7
    li x24, 0x6000               // s8
    li x25, 0x80000095           // s9
    li x26, 0x0                  // s10
    li x27, 0x6000               // s11
    li x28, 0x1                  // t3
    li x29, 0x8000038c           // t4
    li x30, 0xfffffffffff        // t5
    li x31, 0x7ffffbd5           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f11', 'mstatus.fs/vs.fs', 'x9'}, 'clob': {'x9', 'x14'}})
    
    li x14, 0xffff8
    and x9, x9, x14
    li x14, 0x8017fb99
    add x9, x9, x14
    fsd f11, 0x467(x9)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b884e67c817184754e27ee2b86b6b1cc9f81b1a4        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f11, 0x467(x9)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b884e67c817184754e27ee2b86b6b1cc9f81b1a4        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f11, x467, x9
s1(x9)              0x000000008027f899(2150103193)                  0x000000008027f899(2150103193)
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008000069f(2147485343)                  0x000000008000069f(2147485343)                  
sp(x2)              0x00000000802009d3(2149583315)                  0x00000000802009d3(2149583315)                  
gp(x3)              0xfffffffffffffdf5(18446744073709551093)        0xfffffffffffffdf5(18446744073709551093)        
tp(x4)              0x0000020000104c00(2199024323584)               0x0000020000104c00(2199024323584)               
t0(x5)              0x000000008020017f(2149581183)                  0x000000008020017f(2149581183)                  
t1(x6)              0x00000000801ffd40(2149580096)                  0x00000000801ffd40(2149580096)                  
t2(x7)              0x0000000000000004(4)                           0x0000000000000004(4)                           
fp(x8)              0x0000000080180327(2149057319)                  0x0000000080180327(2149057319)                  
s1(x9)              0x000000008027f899(2150103193)                  0x000000008027f899(2150103193)                  
a0(x10)             0x000000008000016f(2147484015)                  0x000000008000016f(2147484015)                  
a1(x11)             0x00000000800004f1(2147484913)                  0x00000000800004f1(2147484913)                  
a2(x12)             0x000000008000078f(2147485583)                  0x000000008000078f(2147485583)                  
a3(x13)             0x000000008017febd(2149056189)                  0x000000008017febd(2149056189)                  
a4(x14)             0x000000008017fb99(2149055385)                  0x000000008017fb99(2149055385)                  
a5(x15)             0x0000000000002008(8200)                        0x0000000000002008(8200)                        
a6(x16)             0x00000000de4dfff4(3729653748)                  0x00000000de4dfff4(3729653748)                  
a7(x17)             0x000000005e5a0149(1582956873)                  0x000000005e5a0149(1582956873)                  
s2(x18)             0x0000000080000413(2147484691)                  0x0000000080000413(2147484691)                  
s3(x19)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s4(x20)             0x0000000098c8c798(2563295128)                  0x0000000098c8c798(2563295128)                  
s5(x21)             0x000000008000038c(2147484556)                  0x000000008000038c(2147484556)                  
s6(x22)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s7(x23)             0x00000000fbc9475c(4224272220)                  0x00000000fbc9475c(4224272220)                  
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x0000000080000095(2147483797)                  0x0000000080000095(2147483797)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x000000008000038c(2147484556)                  0x000000008000038c(2147484556)                  
t5(x30)             0x00000fffffffffff(17592186044415)              0x00000fffffffffff(17592186044415)              
t6(x31)             0x000000007ffffbd5(2147482581)                  0x000000007ffffbd5(2147482581)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            59c5a1262ef82259a90f207c77a6eceb6e1d724a        59c5a1262ef82259a90f207c77a6eceb6e1d724a        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b884e67c817184754e27ee2b86b6b1cc9f81b1a4        X
lastPC              0x000000008000075c(2147485532)                  0x000000008000075c(2147485532)                  
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
f2                  0x41e0000031e00000(2147484047.0_d)              0x41e0000031e00000(2147484047.0_d)              
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff00000293(9.234556879900544e-43_s)     0xffffffff00000293(9.234556879900544e-43_s)     
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff4efffffa(2147482880.0_s)              0xffffffff4efffffa(2147482880.0_s)              
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f15                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f20                 0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x000000008027fe5a(1.0622928504e-314_d)         0x000000008027fe5a(1.0622928504e-314_d)         
f24                 0x7ffffffffffffe00(nan_d)                       0x7ffffffffffffe00(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ffffffffffffe00(nan_d)                       0x7ffffffffffffe00(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

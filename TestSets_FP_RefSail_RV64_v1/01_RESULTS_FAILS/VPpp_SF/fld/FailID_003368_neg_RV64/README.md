# FailID_003368 VP++ SF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3368
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
_reg_f0: .byte 0x00,0x00,0x20,0xa2,0x00,0x03,0xe0,0x41
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f3: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x80,0x64,0x40
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x96,0xfe,0xff,0xdf,0x41
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x20,0xa2,0x00,0x03,0xe0,0x41
_reg_f16:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x80,0xc8,0xff,0xff,0xdf,0x41
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x20,0xa2,0x00,0x03,0xe0,0x41
_reg_f26:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xe8,0xfc,0x1b,0x42
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'dyn(0b111)', 'res': 0}
    li t0, 0xf0
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8000006f            // ra
    li x2, 0x58e6                // sp
    li x3, 0x800001c3            // gp
    li x4, 0x86                  // tp
    li x5, 0x801bf226            // t0
    li x6, 0x800006b5            // t1
    li x7, 0x8017fc93            // t2
    li x8, 0xffffffffffffffff    // fp
    li x9, 0x0                   // s1
    li x10, 0x8018004b           // a0
    li x11, 0x7ffffc25           // a1
    li x12, 0x0                  // a2
    li x13, 0xffffffff9bd71000   // a3
    li x14, 0x0                  // a4
    li x15, 0x70                 // a5
    li x16, 0x1                  // a6
    li x17, 0x6000               // a7
    li x18, 0x0                  // s2
    li x19, 0xfffffffffffffff3   // s3
    li x20, 0x0                  // s4
    li x21, 0x8018014b           // s5
    li x22, 0x0                  // s6
    li x23, 0x1                  // s7
    li x24, 0x0                  // s8
    li x25, 0x8027f7c3           // s9
    li x26, 0x8017fd3f           // s10
    li x27, 0x340191f3           // s11
    li x28, 0x7ffffd2c           // t3
    li x29, 0x80180b6            // t4
    li x30, 0x80180226           // t5
    li x31, 0x637f               // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x13'}, 'clob': {'x13', 'f21', 'x2'}})
    
    li x2, 0x1ffff8
    and x13, x13, x2
    li x2, 0x7ffffff6
    add x13, x13, x2
    fld f21, 0xa(x13)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f21                 0xffffffffffff7e00(nan_h)                       0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f21, 0xa(x13)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f21                 0xffffffffffff7e00(nan_h)                       0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f21, x13
a3(x13)             0x0000000080170ff6(2148995062)                  0x0000000080170ff6(2148995062)
f21                 0xffffffffffff7e00(nan_h)                       0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008000006f(2147483759)                  0x000000008000006f(2147483759)                  
sp(x2)              0x000000007ffffff6(2147483638)                  0x000000007ffffff6(2147483638)                  
gp(x3)              0x00000000800001c3(2147484099)                  0x00000000800001c3(2147484099)                  
tp(x4)              0x0000000000000086(134)                         0x0000000000000086(134)                         
t0(x5)              0x00000000801bf226(2149315110)                  0x00000000801bf226(2149315110)                  
t1(x6)              0x00000000800006b5(2147485365)                  0x00000000800006b5(2147485365)                  
t2(x7)              0x000000008017fc93(2149055635)                  0x000000008017fc93(2149055635)                  
fp(x8)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x000000008018004b(2149056587)                  0x000000008018004b(2149056587)                  
a1(x11)             0x000000007ffffc25(2147482661)                  0x000000007ffffc25(2147482661)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x0000000080170ff6(2148995062)                  0x0000000080170ff6(2148995062)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000000000070(112)                         0x0000000000000070(112)                         
a6(x16)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a7(x17)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0xfffffffffffffff3(18446744073709551603)        0xfffffffffffffff3(18446744073709551603)        
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x000000008018014b(2149056843)                  0x000000008018014b(2149056843)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x000000008027f7c3(2150102979)                  0x000000008027f7c3(2150102979)                  
s10(x26)            0x000000008017fd3f(2149055807)                  0x000000008017fd3f(2149055807)                  
s11(x27)            0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
t3(x28)             0x000000007ffffd2c(2147482924)                  0x000000007ffffd2c(2147482924)                  
t4(x29)             0x00000000080180b6(134316214)                   0x00000000080180b6(134316214)                   
t5(x30)             0x0000000080180226(2149057062)                  0x0000000080180226(2149057062)                  
t6(x31)             0x000000000000637f(25471)                       0x000000000000637f(25471)                       

STATE               REF                                             DUT                                             DIFF
xmemhash            2ecd756b57ee52cc9b9240068c28a662873be0a0        2ecd756b57ee52cc9b9240068c28a662873be0a0        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000714(2147485460)                  0x0000000080000714(2147485460)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000f0(240)                         0x00000000000000f0(240)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            dyn(0b111)                                      dyn(0b111)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x41e00300a2200000(2149057809.0_d)              0x41e00300a2200000(2149057809.0_d)              
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f3                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f4                  0x4064800000000000(164.0_d)                     0x4064800000000000(164.0_d)                     
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x41dffffe96000000(2147482200.0_d)              0x41dffffe96000000(2147482200.0_d)              
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f10                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f11                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x41e00300a2200000(2149057809.0_d)              0x41e00300a2200000(2149057809.0_d)              
f16                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f17                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffffffff7e00(nan_h)                       0x0000000000000000(0.0_d)                       X
f22                 0x41dfffffc8800000(2147483426.0_d)              0x41dfffffc8800000(2147483426.0_d)              
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x41e00300a2200000(2149057809.0_d)              0x41e00300a2200000(2149057809.0_d)              
f26                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x421bfce800000000(30051794944.0_d)             0x421bfce800000000(30051794944.0_d)             
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
STATES DIFFER: True
```

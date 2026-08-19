# FailID_002123 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2123
* Isolated failing instruction: `fsw`
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
_reg_f2: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xe0,0x19,0xff,0x00,0xe0,0x41
_reg_f5: .byte 0x03,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x12,0x02,0x18,0x80,0xff,0xff,0xff,0xff
_reg_f7: .byte 0xf3,0x91,0x01,0x34,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x16,0x93,0x6e,0xfc,0x00,0x3e,0x72,0xde
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x60,0xc9,0x00,0x00,0xe0,0x41
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xef,0x43
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x40,0x3b,0x00,0x00,0xe0,0x41
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f28:.byte 0x03,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': True, 'rm': 'dyn(0b111)', 'res': 0}
    li t0, 0xfd
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801802ce            // ra
    li x2, 0x80000602            // sp
    li x3, 0x8017feac            // gp
    li x4, 0x0                   // tp
    li x5, 0x80180b3e            // t0
    li x6, 0x800000bc            // t1
    li x7, 0x8018063d            // t2
    li x8, 0x8017fd46            // fp
    li x9, 0x7fffffffffffffff    // s1
    li x10, 0x802007a2           // a0
    li x11, 0x80000422           // a1
    li x12, 0x8007f8cf           // a2
    li x13, 0x0                  // a3
    li x14, 0x200                // a4
    li x15, 0x91f3               // a5
    li x16, 0x80180b3e           // a6
    li x17, 0x0                  // a7
    li x18, 0x8017feac           // s2
    li x19, 0x800000bc           // s3
    li x20, 0x0                  // s4
    li x21, 0x80185d46           // s5
    li x22, 0x8017ff77           // s6
    li x23, 0x1d2da5a6bdb6e1cb   // s7
    li x24, 0x8018075e           // s8
    li x25, 0x200                // s9
    li x26, 0x0                  // s10
    li x27, 0x80000602           // s11
    li x28, 0x1                  // t3
    li x29, 0x80180590           // t4
    li x30, 0x800193b0           // t5
    li x31, 0x800001c0           // t6
    // INSTRUCTION ({'dep': {'f0', 'mstatus.fs/vs.fs', 'fcsr.rm', 'x1'}, 'clob': {'x31', 'x1'}})
    
    li x31, 0xffffc
    and x1, x1, x31
    li x31, 0x8017ffe2
    add x1, x1, x31
    fsw f0, 0x1e(x1)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        44eb1442a1d7b1732cdb52ca3b5dfa34c9585cc6        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f0, 0x1e(x1)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        44eb1442a1d7b1732cdb52ca3b5dfa34c9585cc6        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f0, x1, x1
ra(x1)              0x00000000802002ae(2149581486)                  0x00000000802002ae(2149581486)
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000802002ae(2149581486)                  0x00000000802002ae(2149581486)                  
sp(x2)              0x0000000080000602(2147485186)                  0x0000000080000602(2147485186)                  
gp(x3)              0x000000008017feac(2149056172)                  0x000000008017feac(2149056172)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000080180b3e(2149059390)                  0x0000000080180b3e(2149059390)                  
t1(x6)              0x00000000800000bc(2147483836)                  0x00000000800000bc(2147483836)                  
t2(x7)              0x000000008018063d(2149058109)                  0x000000008018063d(2149058109)                  
fp(x8)              0x000000008017fd46(2149055814)                  0x000000008017fd46(2149055814)                  
s1(x9)              0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
a0(x10)             0x00000000802007a2(2149582754)                  0x00000000802007a2(2149582754)                  
a1(x11)             0x0000000080000422(2147484706)                  0x0000000080000422(2147484706)                  
a2(x12)             0x000000008007f8cf(2148006095)                  0x000000008007f8cf(2148006095)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a5(x15)             0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
a6(x16)             0x0000000080180b3e(2149059390)                  0x0000000080180b3e(2149059390)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x000000008017feac(2149056172)                  0x000000008017feac(2149056172)                  
s3(x19)             0x00000000800000bc(2147483836)                  0x00000000800000bc(2147483836)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x0000000080185d46(2149080390)                  0x0000000080185d46(2149080390)                  
s6(x22)             0x000000008017ff77(2149056375)                  0x000000008017ff77(2149056375)                  
s7(x23)             0x1d2da5a6bdb6e1cb(2102518736617923019)         0x1d2da5a6bdb6e1cb(2102518736617923019)         
s8(x24)             0x000000008018075e(2149058398)                  0x000000008018075e(2149058398)                  
s9(x25)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x0000000080000602(2147485186)                  0x0000000080000602(2147485186)                  
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x0000000080180590(2149057936)                  0x0000000080180590(2149057936)                  
t5(x30)             0x00000000800193b0(2147586992)                  0x00000000800193b0(2147586992)                  
t6(x31)             0x000000008017ffe2(2149056482)                  0x000000008017ffe2(2149056482)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            47ed4c1b727471f57f186625f9956b25b54e9e74        47ed4c1b727471f57f186625f9956b25b54e9e74        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        44eb1442a1d7b1732cdb52ca3b5dfa34c9585cc6        X
lastPC              0x0000000080000794(2147485588)                  0x0000000080000794(2147485588)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000fd(253)                         0x00000000000000fd(253)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            dyn(0b111)                                      dyn(0b111)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x41e000ff19e00000(2148006095.0_d)              0x41e000ff19e00000(2148006095.0_d)              
f5                  0xffffffff4f001803(2149057280.0_s)              0xffffffff4f001803(2149057280.0_s)              
f6                  0xffffffff80180212(-2.2047945959778812e-39_s)   0xffffffff80180212(-2.2047945959778812e-39_s)   
f7                  0x00000000340191f3(4.31081234e-315_d)           0x00000000340191f3(4.31081234e-315_d)           
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xde723e00fc6e9316(-9.111611096465146e+146_d)   0xde723e00fc6e9316(-9.111611096465146e+146_d)   
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x41e00000c9600000(2147485259.0_d)              0x41e00000c9600000(2147485259.0_d)              
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x43efffffffffffff(1.844674407370955e+19_d)     0x43efffffffffffff(1.844674407370955e+19_d)     
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x41e000003b400000(2147484122.0_d)              0x41e000003b400000(2147484122.0_d)              
f27                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f28                 0xffffffff4f001803(2149057280.0_s)              0xffffffff4f001803(2149057280.0_s)              
f29                 0xfffffffffffffe00(nan_h)                       0xfffffffffffffe00(nan_h)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

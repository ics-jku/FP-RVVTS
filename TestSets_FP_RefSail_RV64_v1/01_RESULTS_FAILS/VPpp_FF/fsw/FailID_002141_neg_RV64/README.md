# FailID_002141 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2141
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
_reg_f2: .byte 0x00,0x46,0x23,0x08,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x5b,0x4e,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0xab,0x5c,0x4e,0xff,0xff,0xff,0xff
_reg_f12:.byte 0xfb,0xff,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f14:.byte 0xf7,0xff,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x14,0x7c,0xd8,0x41
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f26:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x68
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x8000046e            // sp
    li x3, 0x7fffff1d            // gp
    li x4, 0x7ffffd0e            // tp
    li x5, 0xffffffffc3be5000    // t0
    li x6, 0x97                  // t1
    li x7, 0x80180b14            // t2
    li x8, 0x800003aa            // fp
    li x9, 0x8027ffee            // s1
    li x10, 0x0                  // a0
    li x11, 0x0                  // a1
    li x12, 0xa400b718           // a2
    li x13, 0x0                  // a3
    li x14, 0x8017ff04           // a4
    li x15, 0x22                 // a5
    li x16, 0x801802eb           // a6
    li x17, 0x7ffffd0e           // a7
    li x18, 0x7fffffff           // s2
    li x19, 0x6000               // s3
    li x20, 0x6cae7758           // s4
    li x21, 0x1758000000000000   // s5
    li x22, 0x80180080           // s6
    li x23, 0x80000bd6           // s7
    li x24, 0x801802eb           // s8
    li x25, 0x8000007e           // s9
    li x26, 0x0                  // s10
    li x27, 0x7e                 // s11
    li x28, 0x80180333           // t3
    li x29, 0x1d4aa714           // t4
    li x30, 0x80000755           // t5
    li x31, 0x801800ce           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x8', 'mstatus.fs/vs.fs', 'f17'}, 'clob': {'x8', 'x22'}})
    
    li x22, 0xffffc
    and x8, x8, x22
    li x22, 0x8017fc84
    add x8, x8, x22
    fsw f17, 0x37c(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        68150267165d0caa8008c1b8a6655871d08c67e2        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f17, 0x37c(x8)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        68150267165d0caa8008c1b8a6655871d08c67e2        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f17, x37, x8
fp(x8)              0x000000008018002c(2149056556)                  0x000000008018002c(2149056556)
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x000000008000046e(2147484782)                  0x000000008000046e(2147484782)                  
gp(x3)              0x000000007fffff1d(2147483421)                  0x000000007fffff1d(2147483421)                  
tp(x4)              0x000000007ffffd0e(2147482894)                  0x000000007ffffd0e(2147482894)                  
t0(x5)              0xffffffffc3be5000(18446744072698613760)        0xffffffffc3be5000(18446744072698613760)        
t1(x6)              0x0000000000000097(151)                         0x0000000000000097(151)                         
t2(x7)              0x0000000080180b14(2149059348)                  0x0000000080180b14(2149059348)                  
fp(x8)              0x000000008018002c(2149056556)                  0x000000008018002c(2149056556)                  
s1(x9)              0x000000008027ffee(2150105070)                  0x000000008027ffee(2150105070)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x00000000a400b718(2751510296)                  0x00000000a400b718(2751510296)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x000000008017ff04(2149056260)                  0x000000008017ff04(2149056260)                  
a5(x15)             0x0000000000000022(34)                          0x0000000000000022(34)                          
a6(x16)             0x00000000801802eb(2149057259)                  0x00000000801802eb(2149057259)                  
a7(x17)             0x000000007ffffd0e(2147482894)                  0x000000007ffffd0e(2147482894)                  
s2(x18)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s3(x19)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s4(x20)             0x000000006cae7758(1823373144)                  0x000000006cae7758(1823373144)                  
s5(x21)             0x1758000000000000(1682094460822880256)         0x1758000000000000(1682094460822880256)         
s6(x22)             0x000000008017fc84(2149055620)                  0x000000008017fc84(2149055620)                  
s7(x23)             0x0000000080000bd6(2147486678)                  0x0000000080000bd6(2147486678)                  
s8(x24)             0x00000000801802eb(2149057259)                  0x00000000801802eb(2149057259)                  
s9(x25)             0x000000008000007e(2147483774)                  0x000000008000007e(2147483774)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000000000007e(126)                         0x000000000000007e(126)                         
t3(x28)             0x0000000080180333(2149057331)                  0x0000000080180333(2149057331)                  
t4(x29)             0x000000001d4aa714(491431700)                   0x000000001d4aa714(491431700)                   
t5(x30)             0x0000000080000755(2147485525)                  0x0000000080000755(2147485525)                  
t6(x31)             0x00000000801800ce(2149056718)                  0x00000000801800ce(2149056718)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            6be1c33f1dc16fd70190f66508b89e533539c01e        6be1c33f1dc16fd70190f66508b89e533539c01e        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        68150267165d0caa8008c1b8a6655871d08c67e2        X
lastPC              0x000000008000074c(2147485516)                  0x000000008000074c(2147485516)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000068(104)                         0x0000000000000068(104)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff08234600(4.913331287566997e-34_s)     0xffffffff08234600(4.913331287566997e-34_s)     
f3                  0xffffffff4e5b0000(918552576.0_s)               0xffffffff4e5b0000(918552576.0_s)               
f4                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff4e5cab00(925548544.0_s)               0xffffffff4e5cab00(925548544.0_s)               
f12                 0xffffffffcefffffb(-2147483008.0_s)             0xffffffffcefffffb(-2147483008.0_s)             
f13                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f14                 0xffffffffcefffff7(-2147482496.0_s)             0xffffffffcefffff7(-2147482496.0_s)             
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x41d87c1400000000(1643139072.0_d)              0x41d87c1400000000(1643139072.0_d)              
f25                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f26                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

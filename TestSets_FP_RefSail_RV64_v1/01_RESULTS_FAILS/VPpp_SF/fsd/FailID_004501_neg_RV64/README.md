# FailID_004501 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4501
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x80,0x5f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x80,0x5f,0xff,0xff,0xff,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0xfc,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x50
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80180349            // ra
    li x2, 0x7c                  // sp
    li x3, 0x800005e1            // gp
    li x4, 0x801802aa            // tp
    li x5, 0x6000                // t0
    li x6, 0x0                   // t1
    li x7, 0x80180154            // t2
    li x8, 0x8028024f            // fp
    li x9, 0x0                   // s1
    li x10, 0x0                  // a0
    li x11, 0x801fff3f           // a1
    li x12, 0x800003e1           // a2
    li x13, 0x801ffc04           // a3
    li x14, 0x8c1                // a4
    li x15, 0x801801e6           // a5
    li x16, 0x9073               // a6
    li x17, 0x2                  // a7
    li x18, 0x0                  // s2
    li x19, 0x1                  // s3
    li x20, 0x800007b6           // s4
    li x21, 0x8018004f           // s5
    li x22, 0x801806a3           // s6
    li x23, 0x801806cd           // s7
    li x24, 0x8000073e           // s8
    li x25, 0x8017f9fb           // s9
    li x26, 0x801800e0           // s10
    li x27, 0x802009db           // s11
    li x28, 0x223                // t3
    li x29, 0x801806ff           // t4
    li x30, 0x6000               // t5
    li x31, 0x75f1c000           // t6
    // INSTRUCTION ({'dep': {'f8', 'x19', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'x19', 'x2'}})
    
    li x2, 0xffff8
    and x19, x19, x2
    li x2, 0x8018032f
    add x19, x19, x2
    fsd f8, -0x32f(x19)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        62ca3486298f70a21f191cd85cef9af4c6a0ac08        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f8, -0x32f(x19)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        62ca3486298f70a21f191cd85cef9af4c6a0ac08        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x32, x19
s3(x19)             0x000000008018032f(2149057327)                  0x000000008018032f(2149057327)
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080180349(2149057353)                  0x0000000080180349(2149057353)                  
sp(x2)              0x000000008018032f(2149057327)                  0x000000008018032f(2149057327)                  
gp(x3)              0x00000000800005e1(2147485153)                  0x00000000800005e1(2147485153)                  
tp(x4)              0x00000000801802aa(2149057194)                  0x00000000801802aa(2149057194)                  
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000080180154(2149056852)                  0x0000000080180154(2149056852)                  
fp(x8)              0x000000008028024f(2150105679)                  0x000000008028024f(2150105679)                  
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x00000000801fff3f(2149580607)                  0x00000000801fff3f(2149580607)                  
a2(x12)             0x00000000800003e1(2147484641)                  0x00000000800003e1(2147484641)                  
a3(x13)             0x00000000801ffc04(2149579780)                  0x00000000801ffc04(2149579780)                  
a4(x14)             0x00000000000008c1(2241)                        0x00000000000008c1(2241)                        
a5(x15)             0x00000000801801e6(2149056998)                  0x00000000801801e6(2149056998)                  
a6(x16)             0x0000000000009073(36979)                       0x0000000000009073(36979)                       
a7(x17)             0x0000000000000002(2)                           0x0000000000000002(2)                           
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000008018032f(2149057327)                  0x000000008018032f(2149057327)                  
s4(x20)             0x00000000800007b6(2147485622)                  0x00000000800007b6(2147485622)                  
s5(x21)             0x000000008018004f(2149056591)                  0x000000008018004f(2149056591)                  
s6(x22)             0x00000000801806a3(2149058211)                  0x00000000801806a3(2149058211)                  
s7(x23)             0x00000000801806cd(2149058253)                  0x00000000801806cd(2149058253)                  
s8(x24)             0x000000008000073e(2147485502)                  0x000000008000073e(2147485502)                  
s9(x25)             0x000000008017f9fb(2149054971)                  0x000000008017f9fb(2149054971)                  
s10(x26)            0x00000000801800e0(2149056736)                  0x00000000801800e0(2149056736)                  
s11(x27)            0x00000000802009db(2149583323)                  0x00000000802009db(2149583323)                  
t3(x28)             0x0000000000000223(547)                         0x0000000000000223(547)                         
t4(x29)             0x00000000801806ff(2149058303)                  0x00000000801806ff(2149058303)                  
t5(x30)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t6(x31)             0x0000000075f1c000(1978777600)                  0x0000000075f1c000(1978777600)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            204c6ddafbe1857296249c430f459e818cccf3e8        204c6ddafbe1857296249c430f459e818cccf3e8        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        62ca3486298f70a21f191cd85cef9af4c6a0ac08        X
lastPC              0x0000000080000760(2147485536)                  0x0000000080000760(2147485536)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000050(80)                          0x0000000000000050(80)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff5f800000(1.8446744073709552e+19_s)    0xffffffff5f800000(1.8446744073709552e+19_s)    
f5                  0x7fffffff5f800000(nan_d)                       0x7fffffff5f800000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xfffffffffffffe00(nan_h)                       0xfffffffffffffe00(nan_h)                       
f11                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f12                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f15                 0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffff4f0017fc(2149055488.0_s)              0xffffffff4f0017fc(2149055488.0_s)              
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

# FailID_003644 VP++ SF neg RV64 flh

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3644
* Isolated failing instruction: `flh`
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x04,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x2a,0x05,0x18,0x80,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x40,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x80,0xf9,0xc8,0x00,0xca,0x41
_reg_f19:.byte 0x92,0x27,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xa9,0x97,0x01,0x64,0xd1,0xf7,0xb3,0xa9
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x3d,0xb1,0xaf,0xdd,0x48,0xf5,0x3e,0xde
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x6a,0x8c,0xcf,0x17,0x46,0x60,0x09,0x21
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x18,0x40
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x30
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x6000                // ra
    li x2, 0x0                   // sp
    li x3, 0x1                   // gp
    li x4, 0xffffffffa28de000    // tp
    li x5, 0x80180160            // t0
    li x6, 0x800794a4            // t1
    li x7, 0x80180032            // t2
    li x8, 0x1                   // fp
    li x9, 0x6000                // s1
    li x10, 0x6000               // a0
    li x11, 0x80018f1f           // a1
    li x12, 0x8000000000000000   // a2
    li x13, 0x8018031b           // a3
    li x14, 0x8017feae           // a4
    li x15, 0x6000               // a5
    li x16, 0x0                  // a6
    li x17, 0x0                  // a7
    li x18, 0x0                  // s2
    li x19, 0x80180308           // s3
    li x20, 0x6000               // s4
    li x21, 0x7ffff82a           // s5
    li x22, 0x5eb0d73c           // s6
    li x23, 0x1                  // s7
    li x24, 0x0                  // s8
    li x25, 0x80180036           // s9
    li x26, 0x8017fe1f           // s10
    li x27, 0x80200544           // s11
    li x28, 0x30                 // t3
    li x29, 0x801fff27           // t4
    li x30, 0xf1                 // t5
    li x31, 0x7ffffd2f           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x27', 'fcsr.rm'}, 'clob': {'x29', 'f15', 'x27'}})
    
    li x29, 0x1ffffe
    and x27, x27, x29
    li x29, 0x80000154
    add x27, x27, x29
    flh f15, -0x154(x27)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f15                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0297(3.9517879486083984e-05_h)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flh f15, -0x154(x27)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f15                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0297(3.9517879486083984e-05_h)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f15, x154, x27
s11(x27)            0x0000000080000698(2147485336)                  0x0000000080000698(2147485336)
f15                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0297(3.9517879486083984e-05_h)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0xffffffffa28de000(18446744072141791232)        0xffffffffa28de000(18446744072141791232)        
t0(x5)              0x0000000080180160(2149056864)                  0x0000000080180160(2149056864)                  
t1(x6)              0x00000000800794a4(2147980452)                  0x00000000800794a4(2147980452)                  
t2(x7)              0x0000000080180032(2149056562)                  0x0000000080180032(2149056562)                  
fp(x8)              0x0000000000000001(1)                           0x0000000000000001(1)                           
s1(x9)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a0(x10)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a1(x11)             0x0000000080018f1f(2147585823)                  0x0000000080018f1f(2147585823)                  
a2(x12)             0x8000000000000000(9223372036854775808)         0x8000000000000000(9223372036854775808)         
a3(x13)             0x000000008018031b(2149057307)                  0x000000008018031b(2149057307)                  
a4(x14)             0x000000008017feae(2149056174)                  0x000000008017feae(2149056174)                  
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x0000000080180308(2149057288)                  0x0000000080180308(2149057288)                  
s4(x20)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s5(x21)             0x000000007ffff82a(2147481642)                  0x000000007ffff82a(2147481642)                  
s6(x22)             0x000000005eb0d73c(1588647740)                  0x000000005eb0d73c(1588647740)                  
s7(x23)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x0000000080180036(2149056566)                  0x0000000080180036(2149056566)                  
s10(x26)            0x000000008017fe1f(2149056031)                  0x000000008017fe1f(2149056031)                  
s11(x27)            0x0000000080000698(2147485336)                  0x0000000080000698(2147485336)                  
t3(x28)             0x0000000000000030(48)                          0x0000000000000030(48)                          
t4(x29)             0x0000000080000154(2147483988)                  0x0000000080000154(2147483988)                  
t5(x30)             0x00000000000000f1(241)                         0x00000000000000f1(241)                         
t6(x31)             0x000000007ffffd2f(2147482927)                  0x000000007ffffd2f(2147482927)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            fbe32dc8477810c6cbc430d9fe0393fdf0058b8d        fbe32dc8477810c6cbc430d9fe0393fdf0058b8d        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000720(2147485472)                  0x0000000080000720(2147485472)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000030(48)                          0x0000000000000030(48)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff4f000004(2147484672.0_s)              0xffffffff4f000004(2147484672.0_s)              
f7                  0xffffffff8018052a(-2.2059044243616265e-39_s)   0xffffffff8018052a(-2.2059044243616265e-39_s)   
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff40c00000(6.0_s)                       0xffffffff40c00000(6.0_s)                       
f10                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0297(3.9517879486083984e-05_h)    X
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x41ca00c8f9800000(872518131.0_d)               0x41ca00c8f9800000(872518131.0_d)               
f19                 0xffffffff4f002792(2150076928.0_s)              0xffffffff4f002792(2150076928.0_s)              
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xa9b3f7d1640197a9(-8.502310728454118e-108_d)   0xa9b3f7d1640197a9(-8.502310728454118e-108_d)   
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xde3ef548ddafb13d(-9.664353833149178e+145_d)   0xde3ef548ddafb13d(-9.664353833149178e+145_d)   
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x2109604617cf8c6a(1.5504455516706233e-149_d)   0x2109604617cf8c6a(1.5504455516706233e-149_d)   
f28                 0x4018000000000000(6.0_d)                       0x4018000000000000(6.0_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

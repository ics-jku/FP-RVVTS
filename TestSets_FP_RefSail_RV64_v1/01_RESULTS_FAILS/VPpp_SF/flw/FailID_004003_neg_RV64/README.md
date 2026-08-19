# FailID_004003 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4003
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x16,0xe2,0x3c,0xc1,0x24,0xb5,0x2a,0xd6
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x3f,0x71,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x2a,0x05,0x18,0x80,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f9: .byte 0x00,0x00,0xc0,0x40,0xff,0xff,0xff,0xff
_reg_f10:.byte 0xc7,0xf8,0x78,0x3a,0xec,0x2a,0x97,0xf2
_reg_f11:.byte 0x05,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0xd8,0x42,0xe4,0x52,0x42,0xa0,0x93,0x6c
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

    // restore fcsr = {'nx': True, 'uf': True, 'of': True, 'dz': True, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x7f
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x0                   // sp
    li x3, 0x6b                  // gp
    li x4, 0x195b1724            // tp
    li x5, 0x7ffffc2a            // t0
    li x6, 0x80279192            // t1
    li x7, 0x75cce760            // t2
    li x8, 0x7fffffffffffffff    // fp
    li x9, 0x0                   // s1
    li x10, 0x80180541           // a0
    li x11, 0x40                 // a1
    li x12, 0x801afb3a           // a2
    li x13, 0x6000               // a3
    li x14, 0x0                  // a4
    li x15, 0x8028053d           // a5
    li x16, 0x800b713f           // a6
    li x17, 0x800004fb           // a7
    li x18, 0x3ff000008000061c   // s2
    li x19, 0x80280530           // s3
    li x20, 0x55171750           // s4
    li x21, 0x1                  // s5
    li x22, 0x91f3               // s6
    li x23, 0x340191f3           // s7
    li x24, 0x6000               // s8
    li x25, 0x7                  // s9
    li x26, 0x800004bb           // s10
    li x27, 0x200                // s11
    li x28, 0x0                  // t3
    li x29, 0x0                  // t4
    li x30, 0x7ffffb5e           // t5
    li x31, 0x7fffffffffffffff   // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x19', 'fcsr.rm'}, 'clob': {'f8', 'x19', 'x7'}})
    
    li x7, 0x1ffffc
    and x19, x19, x7
    li x7, 0x800005ab
    add x19, x19, x7
    flw f8, -0x5ab(x19)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f8                  0x3ff0000000000000(1.0_d)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f8, -0x5ab(x19)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'underflow', 'overflow', 'div-by-0', 'inexact'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f8                  0x3ff0000000000000(1.0_d)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x5, x19
t0(x5)              0x000000007ffffc2a(2147482666)                  0x000000007ffffc2a(2147482666)
s3(x19)             0x0000000080080adb(2148010715)                  0x0000000080080adb(2148010715)
f8                  0x3ff0000000000000(1.0_d)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x000000000000006b(107)                         0x000000000000006b(107)                         
tp(x4)              0x00000000195b1724(425400100)                   0x00000000195b1724(425400100)                   
t0(x5)              0x000000007ffffc2a(2147482666)                  0x000000007ffffc2a(2147482666)                  
t1(x6)              0x0000000080279192(2150076818)                  0x0000000080279192(2150076818)                  
t2(x7)              0x00000000800005ab(2147485099)                  0x00000000800005ab(2147485099)                  
fp(x8)              0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x0000000080180541(2149057857)                  0x0000000080180541(2149057857)                  
a1(x11)             0x0000000000000040(64)                          0x0000000000000040(64)                          
a2(x12)             0x00000000801afb3a(2149251898)                  0x00000000801afb3a(2149251898)                  
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x000000008028053d(2150106429)                  0x000000008028053d(2150106429)                  
a6(x16)             0x00000000800b713f(2148233535)                  0x00000000800b713f(2148233535)                  
a7(x17)             0x00000000800004fb(2147484923)                  0x00000000800004fb(2147484923)                  
s2(x18)             0x3ff000008000061c(4607182420947502620)         0x3ff000008000061c(4607182420947502620)         
s3(x19)             0x0000000080080adb(2148010715)                  0x0000000080080adb(2148010715)                  
s4(x20)             0x0000000055171750(1427576656)                  0x0000000055171750(1427576656)                  
s5(x21)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s6(x22)             0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
s7(x23)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x0000000000000007(7)                           0x0000000000000007(7)                           
s10(x26)            0x00000000800004bb(2147484859)                  0x00000000800004bb(2147484859)                  
s11(x27)            0x0000000000000200(512)                         0x0000000000000200(512)                         
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x000000007ffffb5e(2147482462)                  0x000000007ffffb5e(2147482462)                  
t6(x31)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         

STATE               REF                                             DUT                                             DIFF
xmemhash            2b901fad3140209e91e0880fa259adda0472a718        2b901fad3140209e91e0880fa259adda0472a718        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000724(2147485476)                  0x0000000080000724(2147485476)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000007f(127)                         0x000000000000007f(127)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            True                                            True                                            
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f2                  0xd62ab524c13ce216(-1.2250765096343867e+107_d)  0xd62ab524c13ce216(-1.2250765096343867e+107_d)  
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffffffff713f(10744.0_h)                   0xffffffffffff713f(10744.0_h)                   
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff8018052a(-2.2059044243616265e-39_s)   0xffffffff8018052a(-2.2059044243616265e-39_s)   
f8                  0x3ff0000000000000(1.0_d)                       0xffffffff00000000(0.0_s)                       X
f9                  0xffffffff40c00000(6.0_s)                       0xffffffff40c00000(6.0_s)                       
f10                 0xf2972aec3a78f8c7(-9.886869653030081e+243_d)   0xf2972aec3a78f8c7(-9.886869653030081e+243_d)   
f11                 0xffffffff4f001805(2149057792.0_s)              0xffffffff4f001805(2149057792.0_s)              
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x6c93a04252e442d8(1.0571314220529383e+215_d)   0x6c93a04252e442d8(1.0571314220529383e+215_d)   
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
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
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

# FailID_003587 VP++ SF neg RV64 flh

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3587
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f2: .byte 0x00,0x00,0xd0,0x42,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f6: .byte 0x00,0x00,0x00,0xfc,0xfa,0x87,0xae,0xc1
_reg_f7: .byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x02,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xfa,0x27,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xfa,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0x40,0xfb,0xff,0xff,0xdf,0x41
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x80,0x46,0x00,0x00,0xe0,0x41
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x63,0x40
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x41
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x100                 // sp
    li x3, 0xb69a1718            // gp
    li x4, 0x1                   // tp
    li x5, 0x0                   // t0
    li x6, 0x800000c7            // t1
    li x7, 0x800002fa            // t2
    li x8, 0x80180376            // fp
    li x9, 0x800000c7            // s1
    li x10, 0x432                // a0
    li x11, 0x8000054f           // a1
    li x12, 0x800003ab           // a2
    li x13, 0x6000               // a3
    li x14, 0x400001d580000000   // a4
    li x15, 0x800002fa           // a5
    li x16, 0x801ff3fe           // a6
    li x17, 0x0                  // a7
    li x18, 0x8023ff39           // s2
    li x19, 0x7fffa54f           // s3
    li x20, 0x6000               // s4
    li x21, 0x801802df           // s5
    li x22, 0x8017fa95           // s6
    li x23, 0xffffffffa8e54000   // s7
    li x24, 0x80000385           // s8
    li x25, 0x4ea5c000           // s9
    li x26, 0x8017fcfe           // s10
    li x27, 0xffffffff96529000   // s11
    li x28, 0x7ffffe48           // t3
    li x29, 0x8000025f           // t4
    li x30, 0x7ffffd68           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x28'}, 'clob': {'x13', 'f29', 'x28'}})
    
    li x13, 0x1ffffe
    and x28, x28, x13
    li x13, 0x8000053a
    add x28, x28, x13
    flh f29, -0x53a(x28)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f29                 0x41e0000046800000(2147484212.0_d)              0xffffffffffff0000(0.0_h)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flh f29, -0x53a(x28)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f29                 0x41e0000046800000(2147484212.0_d)              0xffffffffffff0000(0.0_h)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f29, x53, x28
t3(x28)             0x0000000080200382(2149581698)                  0x0000000080200382(2149581698)
f29                 0x41e0000046800000(2147484212.0_d)              0xffffffffffff0000(0.0_h)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x0000000000000100(256)                         0x0000000000000100(256)                         
gp(x3)              0x00000000b69a1718(3063551768)                  0x00000000b69a1718(3063551768)                  
tp(x4)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x00000000800000c7(2147483847)                  0x00000000800000c7(2147483847)                  
t2(x7)              0x00000000800002fa(2147484410)                  0x00000000800002fa(2147484410)                  
fp(x8)              0x0000000080180376(2149057398)                  0x0000000080180376(2149057398)                  
s1(x9)              0x00000000800000c7(2147483847)                  0x00000000800000c7(2147483847)                  
a0(x10)             0x0000000000000432(1074)                        0x0000000000000432(1074)                        
a1(x11)             0x000000008000054f(2147485007)                  0x000000008000054f(2147485007)                  
a2(x12)             0x00000000800003ab(2147484587)                  0x00000000800003ab(2147484587)                  
a3(x13)             0x000000008000053a(2147484986)                  0x000000008000053a(2147484986)                  
a4(x14)             0x400001d580000000(4611688034914533376)         0x400001d580000000(4611688034914533376)         
a5(x15)             0x00000000800002fa(2147484410)                  0x00000000800002fa(2147484410)                  
a6(x16)             0x00000000801ff3fe(2149577726)                  0x00000000801ff3fe(2149577726)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x000000008023ff39(2149842745)                  0x000000008023ff39(2149842745)                  
s3(x19)             0x000000007fffa54f(2147460431)                  0x000000007fffa54f(2147460431)                  
s4(x20)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s5(x21)             0x00000000801802df(2149057247)                  0x00000000801802df(2149057247)                  
s6(x22)             0x000000008017fa95(2149055125)                  0x000000008017fa95(2149055125)                  
s7(x23)             0xffffffffa8e54000(18446744072248180736)        0xffffffffa8e54000(18446744072248180736)        
s8(x24)             0x0000000080000385(2147484549)                  0x0000000080000385(2147484549)                  
s9(x25)             0x000000004ea5c000(1319485440)                  0x000000004ea5c000(1319485440)                  
s10(x26)            0x000000008017fcfe(2149055742)                  0x000000008017fcfe(2149055742)                  
s11(x27)            0xffffffff96529000(18446744071936577536)        0xffffffff96529000(18446744071936577536)        
t3(x28)             0x0000000080200382(2149581698)                  0x0000000080200382(2149581698)                  
t4(x29)             0x000000008000025f(2147484255)                  0x000000008000025f(2147484255)                  
t5(x30)             0x000000007ffffd68(2147482984)                  0x000000007ffffd68(2147482984)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            2ae315d9a46deb27e7588d9078949502b2525bdf        2ae315d9a46deb27e7588d9078949502b2525bdf        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000041(65)                          0x0000000000000041(65)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f2                  0xffffffff42d00000(104.0_s)                     0xffffffff42d00000(104.0_s)                     
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f6                  0xc1ae87fafc000000(-256114046.0_d)              0xc1ae87fafc000000(-256114046.0_d)              
f7                  0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff4f000002(2147484160.0_s)              0xffffffff4f000002(2147484160.0_s)              
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff4f0027fa(2150103552.0_s)              0xffffffff4f0027fa(2150103552.0_s)              
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff4f0017fa(2149054976.0_s)              0xffffffff4f0017fa(2149054976.0_s)              
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0x41dffffffb400000(2147483629.0_d)              0x41dffffffb400000(2147483629.0_d)              
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x41e0000046800000(2147484212.0_d)              0xffffffffffff0000(0.0_h)                       X
f30                 0x4063000000000000(152.0_d)                     0x4063000000000000(152.0_d)                     
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

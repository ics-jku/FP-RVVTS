# FailID_001176 VP++ FF neg RV64 flh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1176
* Isolated failing instruction: `flh`
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0xda,0xfe,0xf9,0xdf,0xc1
_reg_f8: .byte 0x44,0xf7,0xe8,0x0e,0x00,0x00,0x00,0x00
_reg_f9: .byte 0xf4,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0xf3,0x04,0xb5,0x41,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x44,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x81
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7ffffdaa            // ra
    li x2, 0x0                   // sp
    li x3, 0x7353e760            // gp
    li x4, 0xffffffffffffffed    // tp
    li x5, 0x25                  // t0
    li x6, 0x80200ba2            // t1
    li x7, 0x800007a5            // t2
    li x8, 0x4                   // fp
    li x9, 0x4013f               // s1
    li x10, 0x8000057c           // a0
    li x11, 0x800008f3           // a1
    li x12, 0x8000640a           // a2
    li x13, 0x800004d0           // a3
    li x14, 0x80200289           // a4
    li x15, 0xfffffffff758c000   // a5
    li x16, 0x0                  // a6
    li x17, 0x0                  // a7
    li x18, 0x8017fa9d           // s2
    li x19, 0x3d                 // s3
    li x20, 0x80180741           // s4
    li x21, 0x8007f5f3           // s5
    li x22, 0x8017fba0           // s6
    li x23, 0x7f726000           // s7
    li x24, 0xb4                 // s8
    li x25, 0x0                  // s9
    li x26, 0x8                  // s10
    li x27, 0x38                 // s11
    li x28, 0x80180647           // t3
    li x29, 0x400c               // t4
    li x30, 0x8027fb88           // t5
    li x31, 0x4d                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x28'}, 'clob': {'x17', 'f24', 'x28'}})
    
    li x17, 0x1ffffe
    and x28, x28, x17
    li x17, 0x7ffffb24
    add x28, x28, x17
    flh f24, 0x4dc(x28)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f24                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flh f24, 0x4dc(x28)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f24                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f24, x4, x28
tp(x4)              0xffffffffffffffed(18446744073709551597)        0xffffffffffffffed(18446744073709551597)
t3(x28)             0x000000008018016a(2149056874)                  0x000000008018016a(2149056874)
f24                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffffdaa(2147483050)                  0x000000007ffffdaa(2147483050)                  
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x000000007353e760(1934878560)                  0x000000007353e760(1934878560)                  
tp(x4)              0xffffffffffffffed(18446744073709551597)        0xffffffffffffffed(18446744073709551597)        
t0(x5)              0x0000000000000025(37)                          0x0000000000000025(37)                          
t1(x6)              0x0000000080200ba2(2149583778)                  0x0000000080200ba2(2149583778)                  
t2(x7)              0x00000000800007a5(2147485605)                  0x00000000800007a5(2147485605)                  
fp(x8)              0x0000000000000004(4)                           0x0000000000000004(4)                           
s1(x9)              0x000000000004013f(262463)                      0x000000000004013f(262463)                      
a0(x10)             0x000000008000057c(2147485052)                  0x000000008000057c(2147485052)                  
a1(x11)             0x00000000800008f3(2147485939)                  0x00000000800008f3(2147485939)                  
a2(x12)             0x000000008000640a(2147509258)                  0x000000008000640a(2147509258)                  
a3(x13)             0x00000000800004d0(2147484880)                  0x00000000800004d0(2147484880)                  
a4(x14)             0x0000000080200289(2149581449)                  0x0000000080200289(2149581449)                  
a5(x15)             0xfffffffff758c000(18446744073564372992)        0xfffffffff758c000(18446744073564372992)        
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x000000007ffffb24(2147482404)                  0x000000007ffffb24(2147482404)                  
s2(x18)             0x000000008017fa9d(2149055133)                  0x000000008017fa9d(2149055133)                  
s3(x19)             0x000000000000003d(61)                          0x000000000000003d(61)                          
s4(x20)             0x0000000080180741(2149058369)                  0x0000000080180741(2149058369)                  
s5(x21)             0x000000008007f5f3(2148005363)                  0x000000008007f5f3(2148005363)                  
s6(x22)             0x000000008017fba0(2149055392)                  0x000000008017fba0(2149055392)                  
s7(x23)             0x000000007f726000(2138202112)                  0x000000007f726000(2138202112)                  
s8(x24)             0x00000000000000b4(180)                         0x00000000000000b4(180)                         
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000008(8)                           0x0000000000000008(8)                           
s11(x27)            0x0000000000000038(56)                          0x0000000000000038(56)                          
t3(x28)             0x000000008018016a(2149056874)                  0x000000008018016a(2149056874)                  
t4(x29)             0x000000000000400c(16396)                       0x000000000000400c(16396)                       
t5(x30)             0x000000008027fb88(2150103944)                  0x000000008027fb88(2150103944)                  
t6(x31)             0x000000000000004d(77)                          0x000000000000004d(77)                          

STATE               REF                                             DUT                                             DIFF
xmemhash            a29ef744c45e21b48915e60de2021652fff6646c        a29ef744c45e21b48915e60de2021652fff6646c        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000081(129)                         0x0000000000000081(129)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xc1dff9feda000000(-2145909608.0_d)             0xc1dff9feda000000(-2145909608.0_d)             
f8                  0x000000000ee8f744(1.23589867e-315_d)           0x000000000ee8f744(1.23589867e-315_d)           
f9                  0xffffffff4efffff4(2147482112.0_s)              0xffffffff4efffff4(2147482112.0_s)              
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f14                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff41b504f3(22.627416610717773_s)        0xffffffff41b504f3(22.627416610717773_s)        
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffffffff0000(0.0_h)                       X
f25                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)                     
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
STATES DIFFER: True
```

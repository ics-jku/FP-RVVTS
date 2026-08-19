# FailID_003532 VP++ SF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3532
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x36,0x40
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x5e,0x7f,0xa1,0xed,0x95,0x85,0x1b,0xf4
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x77,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x20,0x80,0xc4,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0xbf,0x0b,0xc8,0x5c,0x72,0xf9,0x61,0x90
_reg_f13:.byte 0xbc,0x2f,0x3f,0x6e,0x84,0x9f,0x8f,0xcf
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xa5,0x29,0x75,0x24,0xfc,0x3c,0x4c,0xc2
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x40,0x65,0x40
_reg_f19:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x77,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0xff
_reg_f24:.byte 0xab,0xd7,0x5b,0x29,0x8d,0x26,0x10,0xff
_reg_f25:.byte 0xfd,0x6b,0x17,0x75,0xd2,0xa7,0xec,0xd2
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x07,0xf0,0xc5,0x81,0xbe,0x4c,0x74,0x4f
_reg_f28:.byte 0x26,0x37,0xf7,0xe3,0x83,0x6b,0x15,0x75
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x09,0x55,0xa2,0xaa,0x61,0x9b,0xe8,0x6f
_reg_f31:.byte 0xa7,0xca,0x5a,0xda,0x64,0x33,0xd0,0x0c
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x8d
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8018004f            // ra
    li x2, 0x8017fd53            // sp
    li x3, 0x1                   // gp
    li x4, 0x6000                // tp
    li x5, 0x1002ff21            // t0
    li x6, 0x80180610            // t1
    li x7, 0x0                   // t2
    li x8, 0x801805f7            // fp
    li x9, 0xb98c9734            // s1
    li x10, 0x0                  // a0
    li x11, 0x8017f90d           // a1
    li x12, 0x0                  // a2
    li x13, 0x8000038e           // a3
    li x14, 0x4c8bc0b0           // a4
    li x15, 0xfffffffffffffbff   // a5
    li x16, 0x6000               // a6
    li x17, 0x800101b6           // a7
    li x18, 0x8017fab8           // s2
    li x19, 0x1                  // s3
    li x20, 0x1                  // s4
    li x21, 0x0                  // s5
    li x22, 0x6000               // s6
    li x23, 0x801ffea5           // s7
    li x24, 0x801800c8           // s8
    li x25, 0x16                 // s9
    li x26, 0x1                  // s10
    li x27, 0x0                  // s11
    li x28, 0x1                  // t3
    li x29, 0x37003000           // t4
    li x30, 0x8018041f           // t5
    li x31, 0x8017fcff           // t6
    // INSTRUCTION ({'dep': {'x5', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'x5', 'f2', 'x20'}})
    
    li x20, 0x1ffff8
    and x5, x5, x20
    li x20, 0x7ffffae7
    add x5, x5, x20
    fld f2, 0x519(x5)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f2                  0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f2, 0x519(x5)
+========================================================================================================================+
Attributes:  fcsr ['overflow', 'div-by-0', 'inexact'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f2                  0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f2, x519, x5
t0(x5)              0x000000008002fa07(2147678727)                  0x000000008002fa07(2147678727)
f2                  0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008018004f(2149056591)                  0x000000008018004f(2149056591)                  
sp(x2)              0x000000008017fd53(2149055827)                  0x000000008017fd53(2149055827)                  
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t0(x5)              0x000000008002fa07(2147678727)                  0x000000008002fa07(2147678727)                  
t1(x6)              0x0000000080180610(2149058064)                  0x0000000080180610(2149058064)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x00000000801805f7(2149058039)                  0x00000000801805f7(2149058039)                  
s1(x9)              0x00000000b98c9734(3112998708)                  0x00000000b98c9734(3112998708)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x000000008017f90d(2149054733)                  0x000000008017f90d(2149054733)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x000000008000038e(2147484558)                  0x000000008000038e(2147484558)                  
a4(x14)             0x000000004c8bc0b0(1284227248)                  0x000000004c8bc0b0(1284227248)                  
a5(x15)             0xfffffffffffffbff(18446744073709550591)        0xfffffffffffffbff(18446744073709550591)        
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x00000000800101b6(2147549622)                  0x00000000800101b6(2147549622)                  
s2(x18)             0x000000008017fab8(2149055160)                  0x000000008017fab8(2149055160)                  
s3(x19)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s4(x20)             0x000000007ffffae7(2147482343)                  0x000000007ffffae7(2147482343)                  
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s7(x23)             0x00000000801ffea5(2149580453)                  0x00000000801ffea5(2149580453)                  
s8(x24)             0x00000000801800c8(2149056712)                  0x00000000801800c8(2149056712)                  
s9(x25)             0x0000000000000016(22)                          0x0000000000000016(22)                          
s10(x26)            0x0000000000000001(1)                           0x0000000000000001(1)                           
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x0000000037003000(922759168)                   0x0000000037003000(922759168)                   
t5(x30)             0x000000008018041f(2149057567)                  0x000000008018041f(2149057567)                  
t6(x31)             0x000000008017fcff(2149055743)                  0x000000008017fcff(2149055743)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            a941eb34ad8def470bf35f23621ffd9b74af5d84        a941eb34ad8def470bf35f23621ffd9b74af5d84        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000008d(141)                         0x000000000000008d(141)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0x4036000000000000(22.0_d)                      0x4036000000000000(22.0_d)                      
f2                  0x7ff8000000000000(nan_d)                       0x0000000000000000(0.0_d)                       X
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f6                  0xf41b8595eda17f5e(-1.9704868231073644e+251_d)  0xf41b8595eda17f5e(-1.9704868231073644e+251_d)  
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0xffffffff00000077(1.6675451725465323e-43_s)    0xffffffff00000077(1.6675451725465323e-43_s)    
f10                 0xffffffffc4802000(-1025.0_s)                   0xffffffffc4802000(-1025.0_s)                   
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x9061f9725cc80bbf(-9.262063416224988e-230_d)   0x9061f9725cc80bbf(-9.262063416224988e-230_d)   
f13                 0xcf8f9f846e3f2fbc(-1.7879426240184053e+75_d)   0xcf8f9f846e3f2fbc(-1.7879426240184053e+75_d)   
f14                 0x7ff0000000000000(inf_d)                       0x7ff0000000000000(inf_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xc24c3cfc247529a5(-242564483306.32535_d)       0xc24c3cfc247529a5(-242564483306.32535_d)       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x4065400000000000(170.0_d)                     0x4065400000000000(170.0_d)                     
f19                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f20                 0xffffffff00000077(1.6675451725465323e-43_s)    0xffffffff00000077(1.6675451725465323e-43_s)    
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xfff0000000000000(-inf_d)                      0xfff0000000000000(-inf_d)                      
f24                 0xff10268d295bd7ab(-1.1075518562926623e+304_d)  0xff10268d295bd7ab(-1.1075518562926623e+304_d)  
f25                 0xd2eca7d275176bfd(-2.918619830470266e+91_d)    0xd2eca7d275176bfd(-2.918619830470266e+91_d)    
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x4f744cbe81c5f007(5.738657611920474e+74_d)     0x4f744cbe81c5f007(5.738657611920474e+74_d)     
f28                 0x75156b83e3f73726(1.0050679351614462e+256_d)   0x75156b83e3f73726(1.0050679351614462e+256_d)   
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x6fe89b61aaa25509(1.1938359087469714e+231_d)   0x6fe89b61aaa25509(1.1938359087469714e+231_d)   
f31                 0x0cd03364da5acaa7(5.792671351716269e-247_d)    0x0cd03364da5acaa7(5.792671351716269e-247_d)    
STATES DIFFER: True
```

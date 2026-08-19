# FailID_004534 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4534
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
_reg_f0: .byte 0xb0,0xc0,0x8b,0x4c,0xf7,0xd6,0x4a,0xf3
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x25,0x37,0xf7,0xe3,0x83,0x6b,0x15,0x75
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0xb8,0x06,0x18,0x80,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x5e,0x7f,0xa1,0xed,0x95,0x85,0x1b,0xf4
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x4e,0x4a,0xe0,0xdc,0xac,0xaa,0x93,0x89
_reg_f10:.byte 0xfe,0x0c,0x05,0x6e,0x36,0x6a,0x91,0xa0
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0xbf,0x0b,0xc8,0x5c,0x72,0xf9,0x61,0x90
_reg_f13:.byte 0xbc,0x2f,0x3f,0x6e,0x84,0x9f,0x8f,0xcf
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xa5,0x29,0x75,0x24,0xfc,0x3c,0x4c,0xc2
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0xb6,0xd8,0xaa,0x6f,0xe6,0xed,0x3b,0x10
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x77,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xb0,0x16,0x49,0x53,0xc3,0x2f,0xd5,0x8b
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0xab,0x8b,0xdc,0x54,0x5c,0xdf,0x7a,0xcb
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'dyn(0b111)', 'res': 0}
    li t0, 0xe2
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x100300fc60000       // ra
    li x2, 0x3f4f3000            // sp
    li x3, 0x801807e3            // gp
    li x4, 0x1fffffffc           // tp
    li x5, 0x801805b0            // t0
    li x6, 0x6000                // t1
    li x7, 0x97                  // t2
    li x8, 0x66c000              // fp
    li x9, 0x600                 // s1
    li x10, 0x800002cf           // a0
    li x11, 0x0                  // a1
    li x12, 0x8017fd33           // a2
    li x13, 0x0                  // a3
    li x14, 0x8007f537           // a4
    li x15, 0x290                // a5
    li x16, 0x0                  // a6
    li x17, 0x100                // a7
    li x18, 0x1                  // s2
    li x19, 0x7ffffa14           // s3
    li x20, 0x8017f23e           // s4
    li x21, 0x0                  // s5
    li x22, 0x1                  // s6
    li x23, 0x336                // s7
    li x24, 0x7fffffff           // s8
    li x25, 0x77                 // s9
    li x26, 0x41                 // s10
    li x27, 0x8988c740           // s11
    li x28, 0xfffffffffed56d96   // t3
    li x29, 0xfe                 // t4
    li x30, 0x8017fca4           // t5
    li x31, 0x6000               // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'f14', 'fcsr.rm', 'x14'}, 'clob': {'x14', 'x17'}})
    
    li x17, 0xffff8
    and x14, x14, x17
    li x17, 0x8017f9f1
    add x14, x14, x17
    fsd f14, 0x60f(x14)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        387f444d97c701e64ba54d95fd37461292765bc5        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f14, 0x60f(x14)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['inf']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        387f444d97c701e64ba54d95fd37461292765bc5        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x60, x14
a4(x14)             0x00000000801fef21(2149576481)                  0x00000000801fef21(2149576481)
f14                 0x7ff0000000000000(inf_d)                       0x7ff0000000000000(inf_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000100300fc60000(281681399775232)             0x000100300fc60000(281681399775232)             
sp(x2)              0x000000003f4f3000(1062154240)                  0x000000003f4f3000(1062154240)                  
gp(x3)              0x00000000801807e3(2149058531)                  0x00000000801807e3(2149058531)                  
tp(x4)              0x00000001fffffffc(8589934588)                  0x00000001fffffffc(8589934588)                  
t0(x5)              0x00000000801805b0(2149057968)                  0x00000000801805b0(2149057968)                  
t1(x6)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t2(x7)              0x0000000000000097(151)                         0x0000000000000097(151)                         
fp(x8)              0x000000000066c000(6733824)                     0x000000000066c000(6733824)                     
s1(x9)              0x0000000000000600(1536)                        0x0000000000000600(1536)                        
a0(x10)             0x00000000800002cf(2147484367)                  0x00000000800002cf(2147484367)                  
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x000000008017fd33(2149055795)                  0x000000008017fd33(2149055795)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x00000000801fef21(2149576481)                  0x00000000801fef21(2149576481)                  
a5(x15)             0x0000000000000290(656)                         0x0000000000000290(656)                         
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x000000008017f9f1(2149054961)                  0x000000008017f9f1(2149054961)                  
s2(x18)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s3(x19)             0x000000007ffffa14(2147482132)                  0x000000007ffffa14(2147482132)                  
s4(x20)             0x000000008017f23e(2149052990)                  0x000000008017f23e(2149052990)                  
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s7(x23)             0x0000000000000336(822)                         0x0000000000000336(822)                         
s8(x24)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s9(x25)             0x0000000000000077(119)                         0x0000000000000077(119)                         
s10(x26)            0x0000000000000041(65)                          0x0000000000000041(65)                          
s11(x27)            0x000000008988c740(2307442496)                  0x000000008988c740(2307442496)                  
t3(x28)             0xfffffffffed56d96(18446744073689984406)        0xfffffffffed56d96(18446744073689984406)        
t4(x29)             0x00000000000000fe(254)                         0x00000000000000fe(254)                         
t5(x30)             0x000000008017fca4(2149055652)                  0x000000008017fca4(2149055652)                  
t6(x31)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       

STATE               REF                                             DUT                                             DIFF
xmemhash            3376f168a212f79a33d0825dc9e7668f8c7b3381        3376f168a212f79a33d0825dc9e7668f8c7b3381        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        387f444d97c701e64ba54d95fd37461292765bc5        X
lastPC              0x0000000080000718(2147485464)                  0x0000000080000718(2147485464)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000e2(226)                         0x00000000000000e2(226)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            dyn(0b111)                                      dyn(0b111)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xf34ad6f74c8bc0b0(-2.3457638673490832e+247_d)  0xf34ad6f74c8bc0b0(-2.3457638673490832e+247_d)  
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x75156b83e3f73725(1.005067935161446e+256_d)    0x75156b83e3f73725(1.005067935161446e+256_d)    
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff801806b8(-2.2064621411504278e-39_s)   0xffffffff801806b8(-2.2064621411504278e-39_s)   
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xf41b8595eda17f5e(-1.9704868231073644e+251_d)  0xf41b8595eda17f5e(-1.9704868231073644e+251_d)  
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0x8993aaacdce04a4e(-1.561403996397809e-262_d)   0x8993aaacdce04a4e(-1.561403996397809e-262_d)   
f10                 0xa0916a366e050cfe(-8.312717186065277e-152_d)   0xa0916a366e050cfe(-8.312717186065277e-152_d)   
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x9061f9725cc80bbf(-9.262063416224988e-230_d)   0x9061f9725cc80bbf(-9.262063416224988e-230_d)   
f13                 0xcf8f9f846e3f2fbc(-1.7879426240184053e+75_d)   0xcf8f9f846e3f2fbc(-1.7879426240184053e+75_d)   
f14                 0x7ff0000000000000(inf_d)                       0x7ff0000000000000(inf_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xc24c3cfc247529a5(-242564483306.32535_d)       0xc24c3cfc247529a5(-242564483306.32535_d)       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x103bede66faad8b6(1.798967597600698e-230_d)    0x103bede66faad8b6(1.798967597600698e-230_d)    
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff00000077(1.6675451725465323e-43_s)    0xffffffff00000077(1.6675451725465323e-43_s)    
f21                 0x8bd52fc3534916b0(-1.1559109331652503e-251_d)  0x8bd52fc3534916b0(-1.1559109331652503e-251_d)  
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xcb7adf5c54dc8bab(-4.1181990432051295e+55_d)   0xcb7adf5c54dc8bab(-4.1181990432051295e+55_d)   
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

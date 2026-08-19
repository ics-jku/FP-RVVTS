# FailID_004485 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4485
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x37,0xdd,0x64,0x28,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x07,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0xd7,0xdd,0x7c,0x96,0xf4,0x9b,0x21,0xc6
_reg_f10:.byte 0x07,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x48,0x40
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f15:.byte 0x49,0x2c,0x32,0x33,0x61,0x83,0x13,0x28
_reg_f16:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f17:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x39,0xfe,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x39,0xfe,0x17,0x80,0xff,0xff,0xff,0xff
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
    li x1, 0xffffffff93df9d34    // ra
    li x2, 0x1                   // sp
    li x3, 0x6c206000            // gp
    li x4, 0x8017f937            // tp
    li x5, 0xffffffffffff91f3    // t0
    li x6, 0x801807e9            // t1
    li x7, 0x7ffffdfd            // t2
    li x8, 0x800003bd            // fp
    li x9, 0xb1                  // s1
    li x10, 0x7ffffca1           // a0
    li x11, 0x801862e7           // a1
    li x12, 0x7ffffe65           // a2
    li x13, 0x8017ff9f           // a3
    li x14, 0x7ffffa92           // a4
    li x15, 0x8011b538           // a5
    li x16, 0x6000               // a6
    li x17, 0x7ffff93b           // a7
    li x18, 0x800006b10000000    // s2
    li x19, 0x1                  // s3
    li x20, 0x64b70281b383       // s4
    li x21, 0xffff               // s5
    li x22, 0x264fb740           // s6
    li x23, 0x6000               // s7
    li x24, 0x364722             // s8
    li x25, 0x800002c6           // s9
    li x26, 0x18                 // s10
    li x27, 0xffffffffd14cd000   // s11
    li x28, 0x7ffffa92           // t3
    li x29, 0x8000007c           // t4
    li x30, 0xfffffffffffffef7   // t5
    li x31, 0xfffffffffb3e0000   // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x6', 'fcsr.rm', 'f9'}, 'clob': {'x6', 'x8'}})
    
    li x8, 0xffff8
    and x6, x6, x8
    li x8, 0x8017fa01
    add x6, x6, x8
    fsd f9, 0x5ff(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        9c29cc403b0d2565b3eb2456b9a5a1e693c3b048        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f9, 0x5ff(x6)
+========================================================================================================================+
Attributes:  fcsr ['invalid']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        9c29cc403b0d2565b3eb2456b9a5a1e693c3b048        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x5, x6
t0(x5)              0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)
t1(x6)              0x00000000802001e9(2149581289)                  0x00000000802001e9(2149581289)
f9                  0xc6219bf4967cddd7(-6.97572313911571e+29_d)     0xc6219bf4967cddd7(-6.97572313911571e+29_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xffffffff93df9d34(18446744071895489844)        0xffffffff93df9d34(18446744071895489844)        
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)                           
gp(x3)              0x000000006c206000(1814061056)                  0x000000006c206000(1814061056)                  
tp(x4)              0x000000008017f937(2149054775)                  0x000000008017f937(2149054775)                  
t0(x5)              0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)        
t1(x6)              0x00000000802001e9(2149581289)                  0x00000000802001e9(2149581289)                  
t2(x7)              0x000000007ffffdfd(2147483133)                  0x000000007ffffdfd(2147483133)                  
fp(x8)              0x000000008017fa01(2149054977)                  0x000000008017fa01(2149054977)                  
s1(x9)              0x00000000000000b1(177)                         0x00000000000000b1(177)                         
a0(x10)             0x000000007ffffca1(2147482785)                  0x000000007ffffca1(2147482785)                  
a1(x11)             0x00000000801862e7(2149081831)                  0x00000000801862e7(2149081831)                  
a2(x12)             0x000000007ffffe65(2147483237)                  0x000000007ffffe65(2147483237)                  
a3(x13)             0x000000008017ff9f(2149056415)                  0x000000008017ff9f(2149056415)                  
a4(x14)             0x000000007ffffa92(2147482258)                  0x000000007ffffa92(2147482258)                  
a5(x15)             0x000000008011b538(2148644152)                  0x000000008011b538(2148644152)                  
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x000000007ffff93b(2147481915)                  0x000000007ffff93b(2147481915)                  
s2(x18)             0x0800006b10000000(576461212133359616)          0x0800006b10000000(576461212133359616)          
s3(x19)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s4(x20)             0x000064b70281b383(110737183847299)             0x000064b70281b383(110737183847299)             
s5(x21)             0x000000000000ffff(65535)                       0x000000000000ffff(65535)                       
s6(x22)             0x00000000264fb740(642758464)                   0x00000000264fb740(642758464)                   
s7(x23)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s8(x24)             0x0000000000364722(3557154)                     0x0000000000364722(3557154)                     
s9(x25)             0x00000000800002c6(2147484358)                  0x00000000800002c6(2147484358)                  
s10(x26)            0x0000000000000018(24)                          0x0000000000000018(24)                          
s11(x27)            0xffffffffd14cd000(18446744072926056448)        0xffffffffd14cd000(18446744072926056448)        
t3(x28)             0x000000007ffffa92(2147482258)                  0x000000007ffffa92(2147482258)                  
t4(x29)             0x000000008000007c(2147483772)                  0x000000008000007c(2147483772)                  
t5(x30)             0xfffffffffffffef7(18446744073709551351)        0xfffffffffffffef7(18446744073709551351)        
t6(x31)             0xfffffffffb3e0000(18446744073629728768)        0xfffffffffb3e0000(18446744073629728768)        

STATE               REF                                             DUT                                             DIFF
xmemhash            8cbd69140f16d7595c3c63dede8c7174ab9911b7        8cbd69140f16d7595c3c63dede8c7174ab9911b7        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        9c29cc403b0d2565b3eb2456b9a5a1e693c3b048        X
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
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
f1                  0xffffffff2864dd37(1.2704510803562743e-14_s)    0xffffffff2864dd37(1.2704510803562743e-14_s)    
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff4f000007(2147485440.0_s)              0xffffffff4f000007(2147485440.0_s)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0xc6219bf4967cddd7(-6.97572313911571e+29_d)     0xc6219bf4967cddd7(-6.97572313911571e+29_d)     
f10                 0xffffffff4f000007(2147485440.0_s)              0xffffffff4f000007(2147485440.0_s)              
f11                 0x4048000000000000(48.0_d)                      0x4048000000000000(48.0_d)                      
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f15                 0x2813836133322c49(1.238084287307389e-115_d)    0x2813836133322c49(1.238084287307389e-115_d)    
f16                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f17                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f25                 0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f28                 0x7fffffff4f000001(nan_d)                       0x7fffffff4f000001(nan_d)                       
f29                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f30                 0xffffffff8017fe39(-2.2034143169905213e-39_s)   0xffffffff8017fe39(-2.2034143169905213e-39_s)   
f31                 0xffffffff8017fe39(-2.2034143169905213e-39_s)   0xffffffff8017fe39(-2.2034143169905213e-39_s)   
STATES DIFFER: True
```

# FailID_000970 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 970
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x02,0x18,0x00,0xcf,0xff,0xff,0xff,0xff
_reg_f2: .byte 0xf6,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x91,0x01,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x01,0x20,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x03,0x18,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x60,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x54,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x60,0xd5,0x0a,0x03,0xe0,0x41
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x01,0x20,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x54,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xc2
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xffffffffffffffff    // ra
    li x2, 0x0                   // sp
    li x3, 0x0                   // gp
    li x4, 0xc2                  // tp
    li x5, 0x800bbe75            // t0
    li x6, 0x80180053            // t1
    li x7, 0x801ffb3f            // t2
    li x8, 0x8017fb1f            // fp
    li x9, 0x800fc032            // s1
    li x10, 0x15121750           // a0
    li x11, 0x0                  // a1
    li x12, 0x0                  // a2
    li x13, 0x80200030           // a3
    li x14, 0x80000214           // a4
    li x15, 0x8017fa82           // a5
    li x16, 0xc6d83764           // a6
    li x17, 0x2                  // a7
    li x18, 0x0                  // s2
    li x19, 0x382                // s3
    li x20, 0x800007fd           // s4
    li x21, 0x800006f9           // s5
    li x22, 0x0                  // s6
    li x23, 0x8002973c           // s7
    li x24, 0xfffffffff66a4000   // s8
    li x25, 0xffffffffffffffff   // s9
    li x26, 0x8018018b           // s10
    li x27, 0x80180749           // s11
    li x28, 0x80000032           // t3
    li x29, 0x0                  // t4
    li x30, 0x83                 // t5
    li x31, 0x80200637           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x19'}, 'clob': {'x4', 'x19', 'f8'}})
    
    li x4, 0x1ffff8
    and x19, x19, x4
    li x4, 0x7ffffb29
    add x19, x19, x4
    fld f8, 0x4d7(x19)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f8                  0x7fffffff4f001803(nan_d)                       0xffffffff4f000191(2147586304.0_s)              X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f8, 0x4d7(x19)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f8                  0x7fffffff4f001803(nan_d)                       0xffffffff4f000191(2147586304.0_s)              X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x4, d7, x19
tp(x4)              0x000000007ffffb29(2147482409)                  0x000000007ffffb29(2147482409)
s3(x19)             0x000000007ffffea9(2147483305)                  0x000000007ffffea9(2147483305)
f8                  0x7fffffff4f001803(nan_d)                       0xffffffff4f000191(2147586304.0_s)              X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x000000007ffffb29(2147482409)                  0x000000007ffffb29(2147482409)                  
t0(x5)              0x00000000800bbe75(2148253301)                  0x00000000800bbe75(2148253301)                  
t1(x6)              0x0000000080180053(2149056595)                  0x0000000080180053(2149056595)                  
t2(x7)              0x00000000801ffb3f(2149579583)                  0x00000000801ffb3f(2149579583)                  
fp(x8)              0x000000008017fb1f(2149055263)                  0x000000008017fb1f(2149055263)                  
s1(x9)              0x00000000800fc032(2148515890)                  0x00000000800fc032(2148515890)                  
a0(x10)             0x0000000015121750(353507152)                   0x0000000015121750(353507152)                   
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x0000000080200030(2149580848)                  0x0000000080200030(2149580848)                  
a4(x14)             0x0000000080000214(2147484180)                  0x0000000080000214(2147484180)                  
a5(x15)             0x000000008017fa82(2149055106)                  0x000000008017fa82(2149055106)                  
a6(x16)             0x00000000c6d83764(3336058724)                  0x00000000c6d83764(3336058724)                  
a7(x17)             0x0000000000000002(2)                           0x0000000000000002(2)                           
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000007ffffea9(2147483305)                  0x000000007ffffea9(2147483305)                  
s4(x20)             0x00000000800007fd(2147485693)                  0x00000000800007fd(2147485693)                  
s5(x21)             0x00000000800006f9(2147485433)                  0x00000000800006f9(2147485433)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x000000008002973c(2147653436)                  0x000000008002973c(2147653436)                  
s8(x24)             0xfffffffff66a4000(18446744073548742656)        0xfffffffff66a4000(18446744073548742656)        
s9(x25)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s10(x26)            0x000000008018018b(2149056907)                  0x000000008018018b(2149056907)                  
s11(x27)            0x0000000080180749(2149058377)                  0x0000000080180749(2149058377)                  
t3(x28)             0x0000000080000032(2147483698)                  0x0000000080000032(2147483698)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x0000000000000083(131)                         0x0000000000000083(131)                         
t6(x31)             0x0000000080200637(2149582391)                  0x0000000080200637(2149582391)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            e5494a4f92ca6e3228ffd8c0b7701c5819a037fb        e5494a4f92ca6e3228ffd8c0b7701c5819a037fb        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000c2(194)                         0x00000000000000c2(194)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffffcf001802(-2149057024.0_s)             0xffffffffcf001802(-2149057024.0_s)             
f2                  0xffffffff4efffff6(2147482368.0_s)              0xffffffff4efffff6(2147482368.0_s)              
f3                  0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f4                  0xffffffff4f000191(2147586304.0_s)              0xffffffff4f000191(2147586304.0_s)              
f5                  0xffffffff4f002001(2149581056.0_s)              0xffffffff4f002001(2149581056.0_s)              
f6                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7fffffff4f001803(nan_d)                       0xffffffff4f000191(2147586304.0_s)              X
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff4f001860(2149081088.0_s)              0xffffffff4f001860(2149081088.0_s)              
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f13                 0xfffffffffffffe54(nan_h)                       0xfffffffffffffe54(nan_h)                       
f14                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x41e0030ad5600000(2149078699.0_d)              0x41e0030ad5600000(2149078699.0_d)              
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f22                 0xffffffff4f002001(2149581056.0_s)              0xffffffff4f002001(2149581056.0_s)              
f23                 0xfffffffffffffe54(nan_h)                       0xfffffffffffffe54(nan_h)                       
f24                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f25                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

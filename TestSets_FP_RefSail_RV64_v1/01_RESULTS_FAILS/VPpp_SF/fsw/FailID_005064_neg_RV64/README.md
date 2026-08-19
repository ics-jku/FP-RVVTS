# FailID_005064 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 5064
* Isolated failing instruction: `fsw`
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0xd6,0x62,0x54,0xad,0x9b,0x11,0x0e,0x6d
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0xd7,0xdd,0x7c,0x96,0xf4,0x9b,0x21,0xc6
_reg_f10:.byte 0xcf,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x49,0x2c,0x32,0x33,0x61,0x83,0x13,0x28
_reg_f16:.byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x39,0xfe,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0xa0,0x64,0xff,0x02,0xe0,0x41
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x8
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017fb4e            // ra
    li x2, 0x91                  // sp
    li x3, 0x200                 // gp
    li x4, 0x200                 // tp
    li x5, 0x801ff306            // t0
    li x6, 0x802002              // t1
    li x7, 0xfffffffffffffff8    // t2
    li x8, 0x7ffff94b            // fp
    li x9, 0x8008fc5d            // s1
    li x10, 0x0                  // a0
    li x11, 0x8000004b           // a1
    li x12, 0x200                // a2
    li x13, 0x1                  // a3
    li x14, 0x1                  // a4
    li x15, 0x80205fd7           // a5
    li x16, 0x8017fb4d           // a6
    li x17, 0x0                  // a7
    li x18, 0x8017fab5           // s2
    li x19, 0x802002f1           // s3
    li x20, 0x222                // s4
    li x21, 0x0                  // s5
    li x22, 0xca                 // s6
    li x23, 0x300                // s7
    li x24, 0x801d4ab5           // s8
    li x25, 0x0                  // s9
    li x26, 0x2864d768           // s10
    li x27, 0x18594a             // s11
    li x28, 0x801807cc           // t3
    li x29, 0x7ffffc5d           // t4
    li x30, 0x8017fd7e           // t5
    li x31, 0x7ffff661           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f25', 'x30'}, 'clob': {'x12', 'x30'}})
    
    li x12, 0xffffc
    and x30, x30, x12
    li x12, 0x8017f939
    add x30, x30, x12
    fsw f25, 0x6c7(x30)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ad747444bcb9494c65f3501c1ab3cc8b2e4935f8        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f25, 0x6c7(x30)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ad747444bcb9494c65f3501c1ab3cc8b2e4935f8        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, x6, c7, x30
t1(x6)              0x0000000000802002(8396802)                     0x0000000000802002(8396802)
t5(x30)             0x00000000801ff6b5(2149578421)                  0x00000000801ff6b5(2149578421)
f25                 0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fb4e(2149055310)                  0x000000008017fb4e(2149055310)                  
sp(x2)              0x0000000000000091(145)                         0x0000000000000091(145)                         
gp(x3)              0x0000000000000200(512)                         0x0000000000000200(512)                         
tp(x4)              0x0000000000000200(512)                         0x0000000000000200(512)                         
t0(x5)              0x00000000801ff306(2149577478)                  0x00000000801ff306(2149577478)                  
t1(x6)              0x0000000000802002(8396802)                     0x0000000000802002(8396802)                     
t2(x7)              0xfffffffffffffff8(18446744073709551608)        0xfffffffffffffff8(18446744073709551608)        
fp(x8)              0x000000007ffff94b(2147481931)                  0x000000007ffff94b(2147481931)                  
s1(x9)              0x000000008008fc5d(2148072541)                  0x000000008008fc5d(2148072541)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x000000008000004b(2147483723)                  0x000000008000004b(2147483723)                  
a2(x12)             0x000000008017f939(2149054777)                  0x000000008017f939(2149054777)                  
a3(x13)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a4(x14)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a5(x15)             0x0000000080205fd7(2149605335)                  0x0000000080205fd7(2149605335)                  
a6(x16)             0x000000008017fb4d(2149055309)                  0x000000008017fb4d(2149055309)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x000000008017fab5(2149055157)                  0x000000008017fab5(2149055157)                  
s3(x19)             0x00000000802002f1(2149581553)                  0x00000000802002f1(2149581553)                  
s4(x20)             0x0000000000000222(546)                         0x0000000000000222(546)                         
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x00000000000000ca(202)                         0x00000000000000ca(202)                         
s7(x23)             0x0000000000000300(768)                         0x0000000000000300(768)                         
s8(x24)             0x00000000801d4ab5(2149403317)                  0x00000000801d4ab5(2149403317)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x000000002864d768(677697384)                   0x000000002864d768(677697384)                   
s11(x27)            0x000000000018594a(1595722)                     0x000000000018594a(1595722)                     
t3(x28)             0x00000000801807cc(2149058508)                  0x00000000801807cc(2149058508)                  
t4(x29)             0x000000007ffffc5d(2147482717)                  0x000000007ffffc5d(2147482717)                  
t5(x30)             0x00000000801ff6b5(2149578421)                  0x00000000801ff6b5(2149578421)                  
t6(x31)             0x000000007ffff661(2147481185)                  0x000000007ffff661(2147481185)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            7fffd042ec72338e335be32b06bbe82f56672359        7fffd042ec72338e335be32b06bbe82f56672359        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ad747444bcb9494c65f3501c1ab3cc8b2e4935f8        X
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000008(8)                           0x0000000000000008(8)                           
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x6d0e119bad5462d6(2.073111797459765e+217_d)    0x6d0e119bad5462d6(2.073111797459765e+217_d)    
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0xc6219bf4967cddd7(-6.97572313911571e+29_d)     0xc6219bf4967cddd7(-6.97572313911571e+29_d)     
f10                 0xffffffff800000cf(-2.9006878211523713e-43_s)   0xffffffff800000cf(-2.9006878211523713e-43_s)   
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x2813836133322c49(1.238084287307389e-115_d)    0x2813836133322c49(1.238084287307389e-115_d)    
f16                 0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f17                 0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f25                 0xffffffff4f000001(2147483904.0_s)              0xffffffff4f000001(2147483904.0_s)              
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f30                 0xffffffff8017fe39(-2.2034143169905213e-39_s)   0xffffffff8017fe39(-2.2034143169905213e-39_s)   
f31                 0x41e002ff64a00000(2149055269.0_d)              0x41e002ff64a00000(2149055269.0_d)              
STATES DIFFER: True
```

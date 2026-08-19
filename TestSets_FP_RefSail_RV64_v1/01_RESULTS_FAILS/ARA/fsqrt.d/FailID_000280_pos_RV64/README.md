# FailID_000280 ARA pos RV64 fsqrt.d

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 280
* Isolated failing instruction: `fsqrt.d`
* Minimized failing test case: [cblock_minimized_test_case.json](cblock_minimized_test_case.json)
* Resulting REF machine state: [mstate_RefSail.json](mstate_RefSail.json)
* Resulting DUT machine state: [mstate_DUT_ARA.json](mstate_DUT_ARA.json)
* Automated failure characterization report: [AFC_FP_report.log](AFC_FP_report.log)

## Report

### Minimized Failing Test Case
```
    // FLOATINGPOINT STATE DATA
    j _float_data_end
    .align 4
_reg_f0: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f1: .byte 0xa0,0x25,0x68,0x0c,0xca,0x72,0x87,0x1a
_reg_f2: .byte 0x9e,0xd2,0x40,0x81,0x33,0x8c,0x5f,0x3b
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0xe3,0x20,0x38,0xe3,0xf1,0x95,0xc7,0x86
_reg_f5: .byte 0x6e,0x59,0xb1,0x90,0x25,0x31,0x0b,0x41
_reg_f6: .byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x9e,0x7f,0x8c,0xc5,0x7c,0x6d,0xe5,0x68
_reg_f8: .byte 0x97,0x0d,0xbc,0x6b,0x40,0xe3,0xdc,0x43
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f10:.byte 0x00,0x00,0x80,0x4b,0xea,0x1c,0xc0,0xc1
_reg_f11:.byte 0x00,0x00,0xc0,0x98,0x36,0xd3,0xd0,0x41
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x80
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x3b,0x4e,0xdf,0x1b,0x0c,0x9b,0x46,0x38
_reg_f18:.byte 0x58,0xa1,0xd9,0x1d,0xbf,0x7c,0x43,0x0d
_reg_f19:.byte 0x6f,0x60,0x83,0x70,0xf6,0x7b,0x76,0x3d
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x22,0xb5,0x05,0xcd,0xa7,0x18,0x14,0xad
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x06,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0xeb,0x2a,0x09,0x07,0x87,0x98,0x0d,0x58
_reg_f28:.byte 0x96,0x3c,0xf5,0x1f,0x8f,0x32,0x1a,0xcd
_reg_f29:.byte 0x97,0x0d,0xbc,0x6b,0x40,0xe3,0xdc,0x43
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0xf4,0x48,0x6a,0x78,0x1a,0x4c,0xb4,0x66
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x61
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x80073320            // ra
    li x2, 0x200                 // sp
    li x3, 0x222a6000            // gp
    li x4, 0x80180463            // tp
    li x5, 0x1                   // t0
    li x6, 0x738d01aef0365afe    // t1
    li x7, 0xc1c01cea4b800000    // t2
    li x8, 0x2                   // fp
    li x9, 0xffffffffe26cf000    // s1
    li x10, 0x245ea409e391100a   // a0
    li x11, 0x80180665           // a1
    li x12, 0x8006174d           // a2
    li x13, 0x1df8341db894d0ae   // a3
    li x14, 0x40                 // a4
    li x15, 0x200                // a5
    li x16, 0x0                  // a6
    li x17, 0x7ed0337d44c1e123   // a7
    li x18, 0x191                // s2
    li x19, 0x0                  // s3
    li x20, 0x6e9dc84c           // s4
    li x21, 0x8017fda0           // s5
    li x22, 0x7fffffffffffffff   // s6
    li x23, 0x801800ed           // s7
    li x24, 0x8000079d           // s8
    li x25, 0x0                  // s9
    li x26, 0x0                  // s10
    li x27, 0x222a6191           // s11
    li x28, 0x3462f54edfc62b69   // t3
    li x29, 0x473fdc245aa218f7   // t4
    li x30, 0x0                  // t5
    li x31, 0x8017fba0           // t6
    // INSTRUCTION ({'dep': {'f18', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'f14'}})
    fsqrt.d f14, f18, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f14                 0x2698f8cb322e5e6f(9.443924457299442e-123_d)    0x2698f8cb322e5e6e(9.443924457299441e-123_d)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.d f14, f18, dyn
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f14                 0x2698f8cb322e5e6f(9.443924457299442e-123_d)    0x2698f8cb322e5e6e(9.443924457299441e-123_d)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, f18
f14                 0x2698f8cb322e5e6f(9.443924457299442e-123_d)    0x2698f8cb322e5e6e(9.443924457299441e-123_d)    X
f18                 0x0d437cbf1dd9a158(8.918770915517855e-245_d)    0x0d437cbf1dd9a158(8.918770915517855e-245_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080073320(2147955488)                  0x0000000080073320(2147955488)                  
sp(x2)              0x0000000000000200(512)                         0x0000000000000200(512)                         
gp(x3)              0x00000000222a6000(573202432)                   0x00000000222a6000(573202432)                   
tp(x4)              0x0000000080180463(2149057635)                  0x0000000080180463(2149057635)                  
t0(x5)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t1(x6)              0x738d01aef0365afe(8326313136943946494)         0x738d01aef0365afe(8326313136943946494)         
t2(x7)              0xc1c01cea4b800000(13961190637463142400)        0xc1c01cea4b800000(13961190637463142400)        
fp(x8)              0x0000000000000002(2)                           0x0000000000000002(2)                           
s1(x9)              0xffffffffe26cf000(18446744073213374464)        0xffffffffe26cf000(18446744073213374464)        
a0(x10)             0x245ea409e391100a(2620712395555803146)         0x245ea409e391100a(2620712395555803146)         
a1(x11)             0x0000000080180665(2149058149)                  0x0000000080180665(2149058149)                  
a2(x12)             0x000000008006174d(2147882829)                  0x000000008006174d(2147882829)                  
a3(x13)             0x1df8341db894d0ae(2159533323579609262)         0x1df8341db894d0ae(2159533323579609262)         
a4(x14)             0x0000000000000040(64)                          0x0000000000000040(64)                          
a5(x15)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x7ed0337d44c1e123(9137860257052221731)         0x7ed0337d44c1e123(9137860257052221731)         
s2(x18)             0x0000000000000191(401)                         0x0000000000000191(401)                         
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000006e9dc84c(1855834188)                  0x000000006e9dc84c(1855834188)                  
s5(x21)             0x000000008017fda0(2149055904)                  0x000000008017fda0(2149055904)                  
s6(x22)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s7(x23)             0x00000000801800ed(2149056749)                  0x00000000801800ed(2149056749)                  
s8(x24)             0x000000008000079d(2147485597)                  0x000000008000079d(2147485597)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x00000000222a6191(573202833)                   0x00000000222a6191(573202833)                   
t3(x28)             0x3462f54edfc62b69(3774849156800457577)         0x3462f54edfc62b69(3774849156800457577)         
t4(x29)             0x473fdc245aa218f7(5134064148923160823)         0x473fdc245aa218f7(5134064148923160823)         
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x000000008017fba0(2149055392)                  0x000000008017fba0(2149055392)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            f368b965e916c4f12cd55187c10c9fc32f7adb43        f368b965e916c4f12cd55187c10c9fc32f7adb43        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000079c(2147485596)                  0x000000008000079c(2147485596)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000061(97)                          0x0000000000000061(97)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f1                  0x1a8772ca0c6825a0(7.063594269516845e-181_d)    0x1a8772ca0c6825a0(7.063594269516845e-181_d)    
f2                  0x3b5f8c338140d29e(1.0438245387923162e-22_d)    0x3b5f8c338140d29e(1.0438245387923162e-22_d)    
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x86c795f1e33820e3(-5.322101624578317e-276_d)   0x86c795f1e33820e3(-5.322101624578317e-276_d)   
f5                  0x410b312590b1596e(222756.695650767_d)          0x410b312590b1596e(222756.695650767_d)          
f6                  0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f7                  0x68e56d7cc58c7f9e(2.0021768378121024e+197_d)   0x68e56d7cc58c7f9e(2.0021768378121024e+197_d)   
f8                  0x43dce3406bbc0d97(8.326313136943947e+18_d)     0x43dce3406bbc0d97(8.326313136943947e+18_d)     
f9                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f10                 0xc1c01cea4b800000(-540660887.0_d)              0xc1c01cea4b800000(-540660887.0_d)              
f11                 0x41d0d33698c00000(1129110115.0_d)              0x41d0d33698c00000(1129110115.0_d)              
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x2698f8cb322e5e6f(9.443924457299442e-123_d)    0x2698f8cb322e5e6e(9.443924457299441e-123_d)    X
f15                 0x8000000000000000(-0.0_d)                      0x8000000000000000(-0.0_d)                      
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x38469b0c1bdf4e3b(1.3286409002814279e-37_d)    0x38469b0c1bdf4e3b(1.3286409002814279e-37_d)    
f18                 0x0d437cbf1dd9a158(8.918770915517855e-245_d)    0x0d437cbf1dd9a158(8.918770915517855e-245_d)    
f19                 0x3d767bf67083606f(1.2780804535406168e-12_d)    0x3d767bf67083606f(1.2780804535406168e-12_d)    
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xad1418a7cd05b522(-1.5414791601257482e-91_d)   0xad1418a7cd05b522(-1.5414791601257482e-91_d)   
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0xffffffff4f000006(2147485184.0_s)              0xffffffff4f000006(2147485184.0_s)              
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x580d988707092aeb(1.4576678787876398e+116_d)   0x580d988707092aeb(1.4576678787876398e+116_d)   
f28                 0xcd1a328f1ff53c96(-2.6942562334889358e+63_d)   0xcd1a328f1ff53c96(-2.6942562334889358e+63_d)   
f29                 0x43dce3406bbc0d97(8.326313136943947e+18_d)     0x43dce3406bbc0d97(8.326313136943947e+18_d)     
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x66b44c1a786a48f4(5.519695860571659e+186_d)    0x66b44c1a786a48f4(5.519695860571659e+186_d)    
STATES DIFFER: True
```

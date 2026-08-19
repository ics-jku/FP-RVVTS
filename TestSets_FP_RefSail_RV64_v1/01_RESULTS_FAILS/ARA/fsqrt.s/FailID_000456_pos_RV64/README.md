# FailID_000456 ARA pos RV64 fsqrt.s

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 456
* Isolated failing instruction: `fsqrt.s`
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
_reg_f0: .byte 0x08,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x50,0xc1
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0xff,0xfd,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x87,0xb5,0x02,0x00,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0xe0,0xb2,0xfe,0x02,0xe0,0x41
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x51
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x1                   // ra
    li x2, 0x800006e6            // sp
    li x3, 0x0                   // gp
    li x4, 0x7af20000            // tp
    li x5, 0x8000080d            // t0
    li x6, 0x0                   // t1
    li x7, 0x40                  // t2
    li x8, 0x80000321            // fp
    li x9, 0xf6                  // s1
    li x10, 0x1                  // a0
    li x11, 0x0                  // a1
    li x12, 0x7fffffffffffffff   // a2
    li x13, 0x40                 // a3
    li x14, 0x1                  // a4
    li x15, 0x80249d2c           // a5
    li x16, 0x0                  // a6
    li x17, 0x10                 // a7
    li x18, 0x200                // s2
    li x19, 0x588                // s3
    li x20, 0x51b023340191f3     // s4
    li x21, 0x0                  // s5
    li x22, 0xfffffffffffffbaf   // s6
    li x23, 0x0                  // s7
    li x24, 0x0                  // s8
    li x25, 0x800008e6           // s9
    li x26, 0xb5132740           // s10
    li x27, 0x801801b7           // s11
    li x28, 0xd46196f4           // t3
    li x29, 0x200                // t4
    li x30, 0xfffffffffffffdde   // t5
    li x31, 0xfffffd4c3286dc00   // t6
    // INSTRUCTION ({'dep': {'f23', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'f17'}})
    fsqrt.s f17, f23, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f17                 0xffffffff1e94f904(1.5773099972815944e-20_s)    0xffffffff1e94f905(1.5773101588403078e-20_s)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.s f17, f23, dyn
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f17                 0xffffffff1e94f904(1.5773099972815944e-20_s)    0xffffffff1e94f905(1.5773101588403078e-20_s)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f17, f23
f17                 0xffffffff1e94f904(1.5773099972815944e-20_s)    0xffffffff1e94f905(1.5773101588403078e-20_s)    X
f23                 0xffffffff0002b587(2.48790733251621e-40_s)      0xffffffff0002b587(2.48790733251621e-40_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000001(1)                           0x0000000000000001(1)                           
sp(x2)              0x00000000800006e6(2147485414)                  0x00000000800006e6(2147485414)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x000000007af20000(2062680064)                  0x000000007af20000(2062680064)                  
t0(x5)              0x000000008000080d(2147485709)                  0x000000008000080d(2147485709)                  
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000000000040(64)                          0x0000000000000040(64)                          
fp(x8)              0x0000000080000321(2147484449)                  0x0000000080000321(2147484449)                  
s1(x9)              0x00000000000000f6(246)                         0x00000000000000f6(246)                         
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
a3(x13)             0x0000000000000040(64)                          0x0000000000000040(64)                          
a4(x14)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a5(x15)             0x0000000080249d2c(2149883180)                  0x0000000080249d2c(2149883180)                  
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x0000000000000010(16)                          0x0000000000000010(16)                          
s2(x18)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s3(x19)             0x0000000000000588(1416)                        0x0000000000000588(1416)                        
s4(x20)             0x0051b023340191f3(22993138356425203)           0x0051b023340191f3(22993138356425203)           
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0xfffffffffffffbaf(18446744073709550511)        0xfffffffffffffbaf(18446744073709550511)        
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x00000000800008e6(2147485926)                  0x00000000800008e6(2147485926)                  
s10(x26)            0x00000000b5132740(3037931328)                  0x00000000b5132740(3037931328)                  
s11(x27)            0x00000000801801b7(2149056951)                  0x00000000801801b7(2149056951)                  
t3(x28)             0x00000000d46196f4(3563165428)                  0x00000000d46196f4(3563165428)                  
t4(x29)             0x0000000000000200(512)                         0x0000000000000200(512)                         
t5(x30)             0xfffffffffffffdde(18446744073709551070)        0xfffffffffffffdde(18446744073709551070)        
t6(x31)             0xfffffd4c3286dc00(18446741102439881728)        0xfffffd4c3286dc00(18446741102439881728)        

STATE               REF                                             DUT                                             DIFF
xmemhash            70bf1cacd4f5252a9c7a0ff0d743255536e05d0e        70bf1cacd4f5252a9c7a0ff0d743255536e05d0e        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800006f8(2147485432)                  0x00000000800006f8(2147485432)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000051(81)                          0x0000000000000051(81)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff4f000008(2147485696.0_s)              0xffffffff4f000008(2147485696.0_s)              
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xc150000000000000(-4194304.0_d)                0xc150000000000000(-4194304.0_d)                
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f16                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f17                 0xffffffff1e94f904(1.5773099972815944e-20_s)    0xffffffff1e94f905(1.5773101588403078e-20_s)    X
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7ffffdff(nan_s)                       0xffffffff7ffffdff(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffff0002b587(2.48790733251621e-40_s)      0xffffffff0002b587(2.48790733251621e-40_s)      
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x41e002feb2e00000(2149053847.0_d)              0x41e002feb2e00000(2149053847.0_d)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

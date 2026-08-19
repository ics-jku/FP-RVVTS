# FailID_003292 VP++ SF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3292
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
_reg_f0: .byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x40,0xed,0x38,0xce,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x40
_reg_f12:.byte 0x00,0x00,0xc0,0xfe,0xff,0xff,0xdf,0x41
_reg_f13:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x8e,0xfe,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x96,0x38,0xfa,0xff,0xff,0xff,0xef,0x43
_reg_f24:.byte 0x23,0xb4,0x61,0x00,0x23,0xb8,0x71,0x00
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x40,0x00,0x03,0xe0,0x41
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x42
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xfffffffffffff941    // ra
    li x2, 0x7ffff895            // sp
    li x3, 0x7ffffc6b            // gp
    li x4, 0x0                   // tp
    li x5, 0x801805c6            // t0
    li x6, 0xffffffff7fe7fc99    // t1
    li x7, 0x8713673c            // t2
    li x8, 0x42                  // fp
    li x9, 0x0                   // s1
    li x10, 0x801806e9           // a0
    li x11, 0xec3776c            // a1
    li x12, 0x8017fc08           // a2
    li x13, 0x80000592           // a3
    li x14, 0x80180200           // a4
    li x15, 0x801802e4           // a5
    li x16, 0x80180200           // a6
    li x17, 0x0                  // a7
    li x18, 0x7ffffe8e           // s2
    li x19, 0xfffffffffec00000   // s3
    li x20, 0x8                  // s4
    li x21, 0x801866e9           // s5
    li x22, 0x400002             // s6
    li x23, 0xffffffff00000000   // s7
    li x24, 0x80200a5d           // s8
    li x25, 0x8017fc08           // s9
    li x26, 0x6000               // s10
    li x27, 0x801801cd           // s11
    li x28, 0x0                  // t3
    li x29, 0x1                  // t4
    li x30, 0x7fffffff           // t5
    li x31, 0x801801ae           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x27', 'fcsr.rm'}, 'clob': {'x5', 'x27', 'f6'}})
    
    li x5, 0x1ffff8
    and x27, x27, x5
    li x5, 0x8000064d
    add x27, x27, x5
    fld f6, -0x64d(x27)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f6                  0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f6, -0x64d(x27)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f6                  0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f6, x64, x27
s11(x27)            0x0000000080180815(2149058581)                  0x0000000080180815(2149058581)
f6                  0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xfffffffffffff941(18446744073709549889)        0xfffffffffffff941(18446744073709549889)        
sp(x2)              0x000000007ffff895(2147481749)                  0x000000007ffff895(2147481749)                  
gp(x3)              0x000000007ffffc6b(2147482731)                  0x000000007ffffc6b(2147482731)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x000000008000064d(2147485261)                  0x000000008000064d(2147485261)                  
t1(x6)              0xffffffff7fe7fc99(18446744071560494233)        0xffffffff7fe7fc99(18446744071560494233)        
t2(x7)              0x000000008713673c(2266195772)                  0x000000008713673c(2266195772)                  
fp(x8)              0x0000000000000042(66)                          0x0000000000000042(66)                          
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x00000000801806e9(2149058281)                  0x00000000801806e9(2149058281)                  
a1(x11)             0x000000000ec3776c(247691116)                   0x000000000ec3776c(247691116)                   
a2(x12)             0x000000008017fc08(2149055496)                  0x000000008017fc08(2149055496)                  
a3(x13)             0x0000000080000592(2147485074)                  0x0000000080000592(2147485074)                  
a4(x14)             0x0000000080180200(2149057024)                  0x0000000080180200(2149057024)                  
a5(x15)             0x00000000801802e4(2149057252)                  0x00000000801802e4(2149057252)                  
a6(x16)             0x0000000080180200(2149057024)                  0x0000000080180200(2149057024)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x000000007ffffe8e(2147483278)                  0x000000007ffffe8e(2147483278)                  
s3(x19)             0xfffffffffec00000(18446744073688580096)        0xfffffffffec00000(18446744073688580096)        
s4(x20)             0x0000000000000008(8)                           0x0000000000000008(8)                           
s5(x21)             0x00000000801866e9(2149082857)                  0x00000000801866e9(2149082857)                  
s6(x22)             0x0000000000400002(4194306)                     0x0000000000400002(4194306)                     
s7(x23)             0xffffffff00000000(18446744069414584320)        0xffffffff00000000(18446744069414584320)        
s8(x24)             0x0000000080200a5d(2149583453)                  0x0000000080200a5d(2149583453)                  
s9(x25)             0x000000008017fc08(2149055496)                  0x000000008017fc08(2149055496)                  
s10(x26)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s11(x27)            0x0000000080180815(2149058581)                  0x0000000080180815(2149058581)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
t6(x31)             0x00000000801801ae(2149056942)                  0x00000000801801ae(2149056942)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            e2b350af2fde1f0c1cb0b7f0198a8c260492f58b        e2b350af2fde1f0c1cb0b7f0198a8c260492f58b        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000754(2147485524)                  0x0000000080000754(2147485524)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000042(66)                          0x0000000000000042(66)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f1                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f4                  0xffffffffce38ed40(-775639040.0_s)              0xffffffffce38ed40(-775639040.0_s)              
f5                  0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f6                  0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xfffffffffffffe00(nan_h)                       0xfffffffffffffe00(nan_h)                       
f11                 0x4000000000000000(2.0_d)                       0x4000000000000000(2.0_d)                       
f12                 0x41dffffffec00000(2147483643.0_d)              0x41dffffffec00000(2147483643.0_d)              
f13                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f20                 0xffffffff7ffffe8e(nan_s)                       0xffffffff7ffffe8e(nan_s)                       
f21                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x43effffffffa3896(1.8446744072933913e+19_d)    0x43effffffffa3896(1.8446744072933913e+19_d)    
f24                 0x0071b8230061b423(1.577068631947372e-306_d)    0x0071b8230061b423(1.577068631947372e-306_d)    
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x41e0030040000000(2149057024.0_d)              0x41e0030040000000(2149057024.0_d)              
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

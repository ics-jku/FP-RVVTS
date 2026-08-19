# FailID_000779 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 779
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0xfe,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x01,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0xf4,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x0b,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x0f,0xff,0xff,0x7f,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xc8
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017f8bb            // ra
    li x2, 0x202cd000000         // sp
    li x3, 0x8017f85b            // gp
    li x4, 0x7ffffcec            // tp
    li x5, 0x80180609            // t0
    li x6, 0xffffffff7fc00000    // t1
    li x7, 0x1                   // t2
    li x8, 0x8000078f            // fp
    li x9, 0x7ffffbcd            // s1
    li x10, 0x4059a000           // a0
    li x11, 0x0                  // a1
    li x12, 0x801fff92           // a2
    li x13, 0x8000027d           // a3
    li x14, 0x8027fea1           // a4
    li x15, 0x86                 // a5
    li x16, 0x80180721           // a6
    li x17, 0x74d0771c           // a7
    li x18, 0x7ffff84f           // s2
    li x19, 0x8017f9d1           // s3
    li x20, 0x0                  // s4
    li x21, 0x8017fef7           // s5
    li x22, 0x7ffffb6e           // s6
    li x23, 0xffffffffe77e4948   // s7
    li x24, 0x80000242           // s8
    li x25, 0x801ffa05           // s9
    li x26, 0x801af975           // s10
    li x27, 0x7ffffe5e           // s11
    li x28, 0x7ffffcd4           // t3
    li x29, 0x1                  // t4
    li x30, 0x8015658c           // t5
    li x31, 0xffffffff677debae   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x24'}, 'clob': {'f23', 'x24', 'x15'}})
    
    li x15, 0x1ffff8
    and x24, x24, x15
    li x15, 0x7ffffedb
    add x24, x24, x15
    fld f23, 0x125(x24)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f23                 0x0000000000000000(0.0_d)                       0x0051bc2300000393(3.946148252711382e-307_d)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f23, 0x125(x24)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f23                 0x0000000000000000(0.0_d)                       0x0051bc2300000393(3.946148252711382e-307_d)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f23, x125, x24
s8(x24)             0x000000008000011b(2147483931)                  0x000000008000011b(2147483931)
f23                 0x0000000000000000(0.0_d)                       0x0051bc2300000393(3.946148252711382e-307_d)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017f8bb(2149054651)                  0x000000008017f8bb(2149054651)                  
sp(x2)              0x00000202cd000000(2211052519424)               0x00000202cd000000(2211052519424)               
gp(x3)              0x000000008017f85b(2149054555)                  0x000000008017f85b(2149054555)                  
tp(x4)              0x000000007ffffcec(2147482860)                  0x000000007ffffcec(2147482860)                  
t0(x5)              0x0000000080180609(2149058057)                  0x0000000080180609(2149058057)                  
t1(x6)              0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
t2(x7)              0x0000000000000001(1)                           0x0000000000000001(1)                           
fp(x8)              0x000000008000078f(2147485583)                  0x000000008000078f(2147485583)                  
s1(x9)              0x000000007ffffbcd(2147482573)                  0x000000007ffffbcd(2147482573)                  
a0(x10)             0x000000004059a000(1079615488)                  0x000000004059a000(1079615488)                  
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x00000000801fff92(2149580690)                  0x00000000801fff92(2149580690)                  
a3(x13)             0x000000008000027d(2147484285)                  0x000000008000027d(2147484285)                  
a4(x14)             0x000000008027fea1(2150104737)                  0x000000008027fea1(2150104737)                  
a5(x15)             0x000000007ffffedb(2147483355)                  0x000000007ffffedb(2147483355)                  
a6(x16)             0x0000000080180721(2149058337)                  0x0000000080180721(2149058337)                  
a7(x17)             0x0000000074d0771c(1959819036)                  0x0000000074d0771c(1959819036)                  
s2(x18)             0x000000007ffff84f(2147481679)                  0x000000007ffff84f(2147481679)                  
s3(x19)             0x000000008017f9d1(2149054929)                  0x000000008017f9d1(2149054929)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x000000008017fef7(2149056247)                  0x000000008017fef7(2149056247)                  
s6(x22)             0x000000007ffffb6e(2147482478)                  0x000000007ffffb6e(2147482478)                  
s7(x23)             0xffffffffe77e4948(18446744073298397512)        0xffffffffe77e4948(18446744073298397512)        
s8(x24)             0x000000008000011b(2147483931)                  0x000000008000011b(2147483931)                  
s9(x25)             0x00000000801ffa05(2149579269)                  0x00000000801ffa05(2149579269)                  
s10(x26)            0x00000000801af975(2149251445)                  0x00000000801af975(2149251445)                  
s11(x27)            0x000000007ffffe5e(2147483230)                  0x000000007ffffe5e(2147483230)                  
t3(x28)             0x000000007ffffcd4(2147482836)                  0x000000007ffffcd4(2147482836)                  
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x000000008015658c(2148885900)                  0x000000008015658c(2148885900)                  
t6(x31)             0xffffffff677debae(18446744071150889902)        0xffffffff677debae(18446744071150889902)        

STATE               REF                                             DUT                                             DIFF
xmemhash            e4fddadcd558100dbdfe7c06c61b0d892889a624        e4fddadcd558100dbdfe7c06c61b0d892889a624        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000075c(2147485532)                  0x000000008000075c(2147485532)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000c8(200)                         0x00000000000000c8(200)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff4efffffe(2147483392.0_s)              0xffffffff4efffffe(2147483392.0_s)              
f3                  0x0000000000000001(5e-324_d)                    0x0000000000000001(5e-324_d)                    
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff4f0017f4(2149053440.0_s)              0xffffffff4f0017f4(2149053440.0_s)              
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff8000000b(-1.5414283107572988e-44_s)   0xffffffff8000000b(-1.5414283107572988e-44_s)   
f22                 0x000000007fffff0f(1.0609977764e-314_d)         0x000000007fffff0f(1.0609977764e-314_d)         
f23                 0x0000000000000000(0.0_d)                       0x0051bc2300000393(3.946148252711382e-307_d)    X
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

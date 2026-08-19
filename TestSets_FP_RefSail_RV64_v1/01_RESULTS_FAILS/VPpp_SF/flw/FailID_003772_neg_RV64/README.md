# FailID_003772 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3772
* Isolated failing instruction: `flw`
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f15:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x23,0xb4,0x61,0x00,0x23,0xb8,0x71,0x00
_reg_f25:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xdf,0x43
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x80,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0xac,0xf9,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x90
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801805b1            // ra
    li x2, 0x801eadb3            // sp
    li x3, 0x80180671            // gp
    li x4, 0x80180778            // tp
    li x5, 0x0                   // t0
    li x6, 0x8007f86f            // t1
    li x7, 0x8005d9ad            // t2
    li x8, 0x8017fbbe            // fp
    li x9, 0xfd030764            // s1
    li x10, 0x801ff430           // a0
    li x11, 0x1                  // a1
    li x12, 0x8017f8a8           // a2
    li x13, 0x80000397           // a3
    li x14, 0x91f3               // a4
    li x15, 0x0                  // a5
    li x16, 0x8005d9ad           // a6
    li x17, 0x0                  // a7
    li x18, 0x8017fad0           // s2
    li x19, 0x801c416d           // s3
    li x20, 0x80000397           // s4
    li x21, 0x8005dbad           // s5
    li x22, 0x18                 // s6
    li x23, 0x0                  // s7
    li x24, 0xffffffff7fe7fc61   // s8
    li x25, 0x1                  // s9
    li x26, 0x80000184           // s10
    li x27, 0x868a6778           // s11
    li x28, 0x80000229           // t3
    li x29, 0x0                  // t4
    li x30, 0xfffffffffffffbfb   // t5
    li x31, 0x801801ae           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x3'}, 'clob': {'x15', 'f27', 'x3'}})
    
    li x15, 0x1ffffc
    and x3, x3, x15
    li x15, 0x7ffffa81
    add x3, x3, x15
    flw f27, 0x57f(x3)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f27                 0xffffffff00000080(1.793662034335766e-43_s)     0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f27, 0x57f(x3)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f27                 0xffffffff00000080(1.793662034335766e-43_s)     0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f27, x57, x3
gp(x3)              0x00000000801800f1(2149056753)                  0x00000000801800f1(2149056753)
f27                 0xffffffff00000080(1.793662034335766e-43_s)     0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801805b1(2149057969)                  0x00000000801805b1(2149057969)                  
sp(x2)              0x00000000801eadb3(2149494195)                  0x00000000801eadb3(2149494195)                  
gp(x3)              0x00000000801800f1(2149056753)                  0x00000000801800f1(2149056753)                  
tp(x4)              0x0000000080180778(2149058424)                  0x0000000080180778(2149058424)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x000000008007f86f(2148005999)                  0x000000008007f86f(2148005999)                  
t2(x7)              0x000000008005d9ad(2147867053)                  0x000000008005d9ad(2147867053)                  
fp(x8)              0x000000008017fbbe(2149055422)                  0x000000008017fbbe(2149055422)                  
s1(x9)              0x00000000fd030764(4244834148)                  0x00000000fd030764(4244834148)                  
a0(x10)             0x00000000801ff430(2149577776)                  0x00000000801ff430(2149577776)                  
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x000000008017f8a8(2149054632)                  0x000000008017f8a8(2149054632)                  
a3(x13)             0x0000000080000397(2147484567)                  0x0000000080000397(2147484567)                  
a4(x14)             0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
a5(x15)             0x000000007ffffa81(2147482241)                  0x000000007ffffa81(2147482241)                  
a6(x16)             0x000000008005d9ad(2147867053)                  0x000000008005d9ad(2147867053)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x000000008017fad0(2149055184)                  0x000000008017fad0(2149055184)                  
s3(x19)             0x00000000801c416d(2149335405)                  0x00000000801c416d(2149335405)                  
s4(x20)             0x0000000080000397(2147484567)                  0x0000000080000397(2147484567)                  
s5(x21)             0x000000008005dbad(2147867565)                  0x000000008005dbad(2147867565)                  
s6(x22)             0x0000000000000018(24)                          0x0000000000000018(24)                          
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0xffffffff7fe7fc61(18446744071560494177)        0xffffffff7fe7fc61(18446744071560494177)        
s9(x25)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s10(x26)            0x0000000080000184(2147484036)                  0x0000000080000184(2147484036)                  
s11(x27)            0x00000000868a6778(2257217400)                  0x00000000868a6778(2257217400)                  
t3(x28)             0x0000000080000229(2147484201)                  0x0000000080000229(2147484201)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0xfffffffffffffbfb(18446744073709550587)        0xfffffffffffffbfb(18446744073709550587)        
t6(x31)             0x00000000801801ae(2149056942)                  0x00000000801801ae(2149056942)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            8f7c5eee0f00e8c55bd5e14a27a5c46bf89a4015        8f7c5eee0f00e8c55bd5e14a27a5c46bf89a4015        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000780(2147485568)                  0x0000000080000780(2147485568)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000090(144)                         0x0000000000000090(144)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f15                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x0071b8230061b423(1.577068631947372e-306_d)    0x0071b8230061b423(1.577068631947372e-306_d)    
f25                 0x43dfffffffffffff(9.223372036854775e+18_d)     0x43dfffffffffffff(9.223372036854775e+18_d)     
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff00000080(1.793662034335766e-43_s)     0xffffffff00000000(0.0_s)                       X
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff7ffff9ac(nan_s)                       0xffffffff7ffff9ac(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
STATES DIFFER: True
```

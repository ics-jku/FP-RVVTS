# FailID_005076 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 5076
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
_reg_f2: .byte 0x8d,0xf9,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f28:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x81
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801808a9            // ra
    li x2, 0x1                   // sp
    li x3, 0x8020ff5f            // gp
    li x4, 0xfffffffffffffff7    // tp
    li x5, 0x1                   // t0
    li x6, 0x80200380            // t1
    li x7, 0x80005b04            // t2
    li x8, 0xfffffffffffff84d    // fp
    li x9, 0x0                   // s1
    li x10, 0x801ff725           // a0
    li x11, 0x7ffffef6           // a1
    li x12, 0x497                // a2
    li x13, 0x7ffffc1b           // a3
    li x14, 0x200                // a4
    li x15, 0x6000               // a5
    li x16, 0x80000118           // a6
    li x17, 0xb7cba734           // a7
    li x18, 0xd8                 // s2
    li x19, 0x80180521           // s3
    li x20, 0x80000389           // s4
    li x21, 0xfffffffffffffcc5   // s5
    li x22, 0x2                  // s6
    li x23, 0x44                 // s7
    li x24, 0x8017ffa2           // s8
    li x25, 0x8018064c           // s9
    li x26, 0x801804df           // s10
    li x27, 0x10031f50400        // s11
    li x28, 0x800000fc           // t3
    li x29, 0x80000504           // t4
    li x30, 0xb3                 // t5
    li x31, 0x200601d48          // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x27', 'f14', 'fcsr.rm'}, 'clob': {'x1', 'x27'}})
    
    li x1, 0xffffc
    and x27, x27, x1
    li x1, 0x8017f808
    add x27, x27, x1
    fsw f14, 0x7f8(x27)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        adc5069c7516ed6a010b9679d7d2614d95efa4aa        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f14, 0x7f8(x27)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        adc5069c7516ed6a010b9679d7d2614d95efa4aa        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x7, f8, x27
t2(x7)              0x0000000080005b04(2147506948)                  0x0000000080005b04(2147506948)
s11(x27)            0x00000000801cfc08(2149383176)                  0x00000000801cfc08(2149383176)
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
f14                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017f808(2149054472)                  0x000000008017f808(2149054472)                  
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)                           
gp(x3)              0x000000008020ff5f(2149646175)                  0x000000008020ff5f(2149646175)                  
tp(x4)              0xfffffffffffffff7(18446744073709551607)        0xfffffffffffffff7(18446744073709551607)        
t0(x5)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t1(x6)              0x0000000080200380(2149581696)                  0x0000000080200380(2149581696)                  
t2(x7)              0x0000000080005b04(2147506948)                  0x0000000080005b04(2147506948)                  
fp(x8)              0xfffffffffffff84d(18446744073709549645)        0xfffffffffffff84d(18446744073709549645)        
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x00000000801ff725(2149578533)                  0x00000000801ff725(2149578533)                  
a1(x11)             0x000000007ffffef6(2147483382)                  0x000000007ffffef6(2147483382)                  
a2(x12)             0x0000000000000497(1175)                        0x0000000000000497(1175)                        
a3(x13)             0x000000007ffffc1b(2147482651)                  0x000000007ffffc1b(2147482651)                  
a4(x14)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x0000000080000118(2147483928)                  0x0000000080000118(2147483928)                  
a7(x17)             0x00000000b7cba734(3083577140)                  0x00000000b7cba734(3083577140)                  
s2(x18)             0x00000000000000d8(216)                         0x00000000000000d8(216)                         
s3(x19)             0x0000000080180521(2149057825)                  0x0000000080180521(2149057825)                  
s4(x20)             0x0000000080000389(2147484553)                  0x0000000080000389(2147484553)                  
s5(x21)             0xfffffffffffffcc5(18446744073709550789)        0xfffffffffffffcc5(18446744073709550789)        
s6(x22)             0x0000000000000002(2)                           0x0000000000000002(2)                           
s7(x23)             0x0000000000000044(68)                          0x0000000000000044(68)                          
s8(x24)             0x000000008017ffa2(2149056418)                  0x000000008017ffa2(2149056418)                  
s9(x25)             0x000000008018064c(2149058124)                  0x000000008018064c(2149058124)                  
s10(x26)            0x00000000801804df(2149057759)                  0x00000000801804df(2149057759)                  
s11(x27)            0x00000000801cfc08(2149383176)                  0x00000000801cfc08(2149383176)                  
t3(x28)             0x00000000800000fc(2147483900)                  0x00000000800000fc(2147483900)                  
t4(x29)             0x0000000080000504(2147484932)                  0x0000000080000504(2147484932)                  
t5(x30)             0x00000000000000b3(179)                         0x00000000000000b3(179)                         
t6(x31)             0x0000000200601d48(8596233544)                  0x0000000200601d48(8596233544)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            99641978fa08425eae321a86e6ed38694ba30be1        99641978fa08425eae321a86e6ed38694ba30be1        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        adc5069c7516ed6a010b9679d7d2614d95efa4aa        X
lastPC              0x000000008000074c(2147485516)                  0x000000008000074c(2147485516)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000081(129)                         0x0000000000000081(129)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff7ffff98d(nan_s)                       0xffffffff7ffff98d(nan_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f28                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

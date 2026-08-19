# FailID_004973 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4973
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
_reg_f0: .byte 0x00,0x00,0xe0,0xdd,0x00,0x03,0xe0,0x41
_reg_f1: .byte 0x01,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xa0,0xaf,0xff,0x03,0xe0,0x41
_reg_f3: .byte 0x04,0x01,0x20,0x80,0x00,0x00,0x00,0x00
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x80,0xff,0x03,0xe0,0x41
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f16:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xdf,0x41
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x20,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x52,0x14,0x01,0x80,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'res0(0b101)', 'res': 0}
    li t0, 0xa8
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x800802c7            // ra
    li x2, 0x80180671            // sp
    li x3, 0x801804fa            // gp
    li x4, 0x0                   // tp
    li x5, 0x800000e0            // t0
    li x6, 0x6000                // t1
    li x7, 0x1                   // t2
    li x8, 0x6fc83000            // fp
    li x9, 0xa8                  // s1
    li x10, 0x0                  // a0
    li x11, 0x7fffffff           // a1
    li x12, 0x0                  // a2
    li x13, 0x0                  // a3
    li x14, 0x6000               // a4
    li x15, 0x0                  // a5
    li x16, 0x1                  // a6
    li x17, 0x8017fd0a           // a7
    li x18, 0x0                  // s2
    li x19, 0x200                // s3
    li x20, 0x800003a7           // s4
    li x21, 0x80000544           // s5
    li x22, 0xbc                 // s6
    li x23, 0x0                  // s7
    li x24, 0x0                  // s8
    li x25, 0x0                  // s9
    li x26, 0x800005d0           // s10
    li x27, 0x1                  // s11
    li x28, 0x8018024e           // t3
    li x29, 0x8027fc02           // t4
    li x30, 0x801806ef           // t5
    li x31, 0x7fffffff           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x22', 'f8'}, 'clob': {'x10', 'x22'}})
    
    li x10, 0xffffc
    and x22, x22, x10
    li x10, 0x8017fe09
    add x22, x22, x10
    fsw f8, 0x1f7(x22)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ec49ded61d4de2c8dd171fa0e284079d12137f74        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f8, 0x1f7(x22)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ec49ded61d4de2c8dd171fa0e284079d12137f74        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x1, f7, x22
ra(x1)              0x00000000800802c7(2148008647)                  0x00000000800802c7(2148008647)
s6(x22)             0x000000008017fec5(2149056197)                  0x000000008017fec5(2149056197)
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
f8                  0xffffffff80000000(-0.0_s)                      0xffffffff80000000(-0.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000800802c7(2148008647)                  0x00000000800802c7(2148008647)                  
sp(x2)              0x0000000080180671(2149058161)                  0x0000000080180671(2149058161)                  
gp(x3)              0x00000000801804fa(2149057786)                  0x00000000801804fa(2149057786)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x00000000800000e0(2147483872)                  0x00000000800000e0(2147483872)                  
t1(x6)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t2(x7)              0x0000000000000001(1)                           0x0000000000000001(1)                           
fp(x8)              0x000000006fc83000(1875390464)                  0x000000006fc83000(1875390464)                  
s1(x9)              0x00000000000000a8(168)                         0x00000000000000a8(168)                         
a0(x10)             0x000000008017fe09(2149056009)                  0x000000008017fe09(2149056009)                  
a1(x11)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a7(x17)             0x000000008017fd0a(2149055754)                  0x000000008017fd0a(2149055754)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s4(x20)             0x00000000800003a7(2147484583)                  0x00000000800003a7(2147484583)                  
s5(x21)             0x0000000080000544(2147484996)                  0x0000000080000544(2147484996)                  
s6(x22)             0x000000008017fec5(2149056197)                  0x000000008017fec5(2149056197)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x00000000800005d0(2147485136)                  0x00000000800005d0(2147485136)                  
s11(x27)            0x0000000000000001(1)                           0x0000000000000001(1)                           
t3(x28)             0x000000008018024e(2149057102)                  0x000000008018024e(2149057102)                  
t4(x29)             0x000000008027fc02(2150104066)                  0x000000008027fc02(2150104066)                  
t5(x30)             0x00000000801806ef(2149058287)                  0x00000000801806ef(2149058287)                  
t6(x31)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            ac488e764ce5ae6bc8f34b42e06ab073d13e8704        ac488e764ce5ae6bc8f34b42e06ab073d13e8704        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ec49ded61d4de2c8dd171fa0e284079d12137f74        X
lastPC              0x0000000080000714(2147485460)                  0x0000000080000714(2147485460)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000a8(168)                         0x00000000000000a8(168)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            res0(0b101)                                     res0(0b101)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x41e00300dde00000(2149058287.0_d)              0x41e00300dde00000(2149058287.0_d)              
f1                  0xffffffff00000001(1.401298464324817e-45_s)     0xffffffff00000001(1.401298464324817e-45_s)     
f2                  0x41e003ffafa00000(2149580157.0_d)              0x41e003ffafa00000(2149580157.0_d)              
f3                  0x0000000080200104(1.0620341547e-314_d)         0x0000000080200104(1.0620341547e-314_d)         
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff80000000(-0.0_s)                      0xffffffff80000000(-0.0_s)                      
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0x41e003ff80000000(2149579776.0_d)              0x41e003ff80000000(2149579776.0_d)              
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f16                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x41dfffffffc00000(2147483647.0_d)              0x41dfffffffc00000(2147483647.0_d)              
f22                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x0000000000000020(1.6e-322_d)                  0x0000000000000020(1.6e-322_d)                  
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f29                 0xffffffff80011452(-9.91250507694089e-41_s)     0xffffffff80011452(-9.91250507694089e-41_s)     
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
STATES DIFFER: True
```

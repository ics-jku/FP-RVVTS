# FailID_004276 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4276
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
_reg_f0: .byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x41,0xf9,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x6d,0x41,0x1c,0x80,0x00,0x00,0x00,0x00
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f15:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x41,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x23,0xb4,0x61,0x00,0x23,0xb8,0x71,0x00
_reg_f25:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x54
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801805b1            // ra
    li x2, 0x6000                // sp
    li x3, 0x8020083e            // gp
    li x4, 0xffffffffcf90b000    // tp
    li x5, 0x0                   // t0
    li x6, 0x0                   // t1
    li x7, 0x7ffffc22            // t2
    li x8, 0xffffffffd1c4b000    // fp
    li x9, 0x80180456            // s1
    li x10, 0x801ff430           // a0
    li x11, 0x40e7d738           // a1
    li x12, 0x8017f8a8           // a2
    li x13, 0x8017f941           // a3
    li x14, 0x91f3               // a4
    li x15, 0x7ffffa81           // a5
    li x16, 0x6000               // a6
    li x17, 0x0                  // a7
    li x18, 0x8017fad0           // s2
    li x19, 0x801c416d           // s3
    li x20, 0x8                  // s4
    li x21, 0x802001c6           // s5
    li x22, 0x8018074e           // s6
    li x23, 0xffffffffcf90b000   // s7
    li x24, 0x801fffad           // s8
    li x25, 0x400c00             // s9
    li x26, 0x80000184           // s10
    li x27, 0x0                  // s11
    li x28, 0x15f                // t3
    li x29, 0x8017fd24           // t4
    li x30, 0xfffffffffffffbfb   // t5
    li x31, 0x801801ae           // t6
    // INSTRUCTION ({'dep': {'x5', 'fcsr.rm', 'f8', 'mstatus.fs/vs.fs'}, 'clob': {'x5', 'x2'}})
    
    li x2, 0xffff8
    and x5, x5, x2
    li x2, 0x801805c6
    add x5, x5, x2
    fsd f8, -0x5c6(x5)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        25abcd80ac5d48264d381b330ca1c9012b83da53        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f8, -0x5c6(x5)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        25abcd80ac5d48264d381b330ca1c9012b83da53        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x5, c6, x5
t0(x5)              0x00000000801805c6(2149057990)                  0x00000000801805c6(2149057990)
f8                  0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801805b1(2149057969)                  0x00000000801805b1(2149057969)                  
sp(x2)              0x00000000801805c6(2149057990)                  0x00000000801805c6(2149057990)                  
gp(x3)              0x000000008020083e(2149582910)                  0x000000008020083e(2149582910)                  
tp(x4)              0xffffffffcf90b000(18446744072896950272)        0xffffffffcf90b000(18446744072896950272)        
t0(x5)              0x00000000801805c6(2149057990)                  0x00000000801805c6(2149057990)                  
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x000000007ffffc22(2147482658)                  0x000000007ffffc22(2147482658)                  
fp(x8)              0xffffffffd1c4b000(18446744072933912576)        0xffffffffd1c4b000(18446744072933912576)        
s1(x9)              0x0000000080180456(2149057622)                  0x0000000080180456(2149057622)                  
a0(x10)             0x00000000801ff430(2149577776)                  0x00000000801ff430(2149577776)                  
a1(x11)             0x0000000040e7d738(1088935736)                  0x0000000040e7d738(1088935736)                  
a2(x12)             0x000000008017f8a8(2149054632)                  0x000000008017f8a8(2149054632)                  
a3(x13)             0x000000008017f941(2149054785)                  0x000000008017f941(2149054785)                  
a4(x14)             0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
a5(x15)             0x000000007ffffa81(2147482241)                  0x000000007ffffa81(2147482241)                  
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x000000008017fad0(2149055184)                  0x000000008017fad0(2149055184)                  
s3(x19)             0x00000000801c416d(2149335405)                  0x00000000801c416d(2149335405)                  
s4(x20)             0x0000000000000008(8)                           0x0000000000000008(8)                           
s5(x21)             0x00000000802001c6(2149581254)                  0x00000000802001c6(2149581254)                  
s6(x22)             0x000000008018074e(2149058382)                  0x000000008018074e(2149058382)                  
s7(x23)             0xffffffffcf90b000(18446744072896950272)        0xffffffffcf90b000(18446744072896950272)        
s8(x24)             0x00000000801fffad(2149580717)                  0x00000000801fffad(2149580717)                  
s9(x25)             0x0000000000400c00(4197376)                     0x0000000000400c00(4197376)                     
s10(x26)            0x0000000080000184(2147484036)                  0x0000000080000184(2147484036)                  
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x000000000000015f(351)                         0x000000000000015f(351)                         
t4(x29)             0x000000008017fd24(2149055780)                  0x000000008017fd24(2149055780)                  
t5(x30)             0xfffffffffffffbfb(18446744073709550587)        0xfffffffffffffbfb(18446744073709550587)        
t6(x31)             0x00000000801801ae(2149056942)                  0x00000000801801ae(2149056942)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            460caf2437a232eda44a09212d081962c9254316        460caf2437a232eda44a09212d081962c9254316        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        25abcd80ac5d48264d381b330ca1c9012b83da53        X
lastPC              0x0000000080000748(2147485512)                  0x0000000080000748(2147485512)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000054(84)                          0x0000000000000054(84)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff8017f941(-2.2016318653439e-39_s)      0xffffffff8017f941(-2.2016318653439e-39_s)      
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f6                  0x00000000801c416d(1.061912785e-314_d)          0x00000000801c416d(1.061912785e-314_d)          
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xfffffffffffffe00(nan_h)                       0xfffffffffffffe00(nan_h)                       
f11                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f15                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff41000000(8.0_s)                       0xffffffff41000000(8.0_s)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x0071b8230061b423(1.577068631947372e-306_d)    0x0071b8230061b423(1.577068631947372e-306_d)    
f25                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff00000080(1.793662034335766e-43_s)     0xffffffff00000080(1.793662034335766e-43_s)     
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff7ffff9ac(nan_s)                       0xffffffff7ffff9ac(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
STATES DIFFER: True
```

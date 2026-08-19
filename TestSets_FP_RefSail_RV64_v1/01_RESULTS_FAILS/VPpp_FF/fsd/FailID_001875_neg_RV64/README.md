# FailID_001875 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1875
* Isolated failing instruction: `fsd`
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x90,0xfe,0xff,0x7f,0x41
_reg_f13:.byte 0x00,0x00,0x00,0x50,0xff,0xff,0xdf,0x41
_reg_f14:.byte 0x0b,0xb0,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0x00,0x00,0x00,0x2d,0x00,0x00,0xe0,0x41
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f22:.byte 0xfa,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f28:.byte 0x00,0x00,0xe0,0xc6,0xff,0x02,0x10,0x43
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': False, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x55
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x6000                // ra
    li x2, 0x200                 // sp
    li x3, 0x7ffffd40            // gp
    li x4, 0x0                   // tp
    li x5, 0x1                   // t0
    li x6, 0x400bff1b80000       // t1
    li x7, 0x8027fa2a            // t2
    li x8, 0x7fffffff            // fp
    li x9, 0x7fffffff            // s1
    li x10, 0x7ffffd40           // a0
    li x11, 0x7fffffffffffffff   // a1
    li x12, 0x8020039f           // a2
    li x13, 0x8018009e           // a3
    li x14, 0x8000050f           // a4
    li x15, 0xffffffffffffffff   // a5
    li x16, 0x8027f657           // a6
    li x17, 0x0                  // a7
    li x18, 0x200                // s2
    li x19, 0x80000241           // s3
    li x20, 0x801804b5           // s4
    li x21, 0x7ff8000000000000   // s5
    li x22, 0x8017fa2c           // s6
    li x23, 0x4ee1d000           // s7
    li x24, 0x5e                 // s8
    li x25, 0x800004fb           // s9
    li x26, 0x801fffe7           // s10
    li x27, 0xffffffff7ffffb0b   // s11
    li x28, 0x8017fd87           // t3
    li x29, 0xffffffffffffb00b   // t4
    li x30, 0x6000               // t5
    li x31, 0x80000543           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f23', 'mstatus.fs/vs.fs', 'x4'}, 'clob': {'x4', 'x13'}})
    
    li x13, 0xffff8
    and x4, x4, x13
    li x13, 0x801804bf
    add x4, x4, x13
    fsd f23, -0x4bf(x4)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5871a0e2b5463641eb5587b9e29814822e3a2ec9        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f23, -0x4bf(x4)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5871a0e2b5463641eb5587b9e29814822e3a2ec9        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f23, x4, x4
tp(x4)              0x00000000801804bf(2149057727)                  0x00000000801804bf(2149057727)
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
sp(x2)              0x0000000000000200(512)                         0x0000000000000200(512)                         
gp(x3)              0x000000007ffffd40(2147482944)                  0x000000007ffffd40(2147482944)                  
tp(x4)              0x00000000801804bf(2149057727)                  0x00000000801804bf(2149057727)                  
t0(x5)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t1(x6)              0x000400bff1b80000(1126724300963840)            0x000400bff1b80000(1126724300963840)            
t2(x7)              0x000000008027fa2a(2150103594)                  0x000000008027fa2a(2150103594)                  
fp(x8)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s1(x9)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a0(x10)             0x000000007ffffd40(2147482944)                  0x000000007ffffd40(2147482944)                  
a1(x11)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
a2(x12)             0x000000008020039f(2149581727)                  0x000000008020039f(2149581727)                  
a3(x13)             0x00000000801804bf(2149057727)                  0x00000000801804bf(2149057727)                  
a4(x14)             0x000000008000050f(2147484943)                  0x000000008000050f(2147484943)                  
a5(x15)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a6(x16)             0x000000008027f657(2150102615)                  0x000000008027f657(2150102615)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s3(x19)             0x0000000080000241(2147484225)                  0x0000000080000241(2147484225)                  
s4(x20)             0x00000000801804b5(2149057717)                  0x00000000801804b5(2149057717)                  
s5(x21)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
s6(x22)             0x000000008017fa2c(2149055020)                  0x000000008017fa2c(2149055020)                  
s7(x23)             0x000000004ee1d000(1323421696)                  0x000000004ee1d000(1323421696)                  
s8(x24)             0x000000000000005e(94)                          0x000000000000005e(94)                          
s9(x25)             0x00000000800004fb(2147484923)                  0x00000000800004fb(2147484923)                  
s10(x26)            0x00000000801fffe7(2149580775)                  0x00000000801fffe7(2149580775)                  
s11(x27)            0xffffffff7ffffb0b(18446744071562066699)        0xffffffff7ffffb0b(18446744071562066699)        
t3(x28)             0x000000008017fd87(2149055879)                  0x000000008017fd87(2149055879)                  
t4(x29)             0xffffffffffffb00b(18446744073709531147)        0xffffffffffffb00b(18446744073709531147)        
t5(x30)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t6(x31)             0x0000000080000543(2147484995)                  0x0000000080000543(2147484995)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            355153faa6b849bb30f9a7dc3a1a6206a3aa8eb3        355153faa6b849bb30f9a7dc3a1a6206a3aa8eb3        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5871a0e2b5463641eb5587b9e29814822e3a2ec9        X
lastPC              0x000000008000074c(2147485516)                  0x000000008000074c(2147485516)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000055(85)                          0x0000000000000055(85)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x417ffffe90000000(33554409.0_d)                0x417ffffe90000000(33554409.0_d)                
f13                 0x41dfffff50000000(2147482944.0_d)              0x41dfffff50000000(2147482944.0_d)              
f14                 0xffffffffceffb00b(-2144863616.0_s)             0xffffffffceffb00b(-2144863616.0_s)             
f15                 0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f16                 0x41e000002d000000(2147484008.0_d)              0x41e000002d000000(2147484008.0_d)              
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f22                 0xffffffff4efffffa(2147482880.0_s)              0xffffffff4efffffa(2147482880.0_s)              
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f28                 0x431002ffc6e00000(1126724300963840.0_d)        0x431002ffc6e00000(1126724300963840.0_d)        
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

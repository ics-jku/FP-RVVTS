# FailID_001874 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1874
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
_reg_f1: .byte 0xff,0x7b,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x90,0xfe,0xff,0x7f,0x41
_reg_f13:.byte 0x00,0x00,0x00,0x50,0xff,0xff,0xdf,0x41
_reg_f14:.byte 0x0b,0xb0,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x1f,0x0e,0x49,0xca,0x93,0x07,0x92,0xd1
_reg_f16:.byte 0x00,0x00,0x00,0x2d,0x00,0x00,0xe0,0x41
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0xfa,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f28:.byte 0x00,0x00,0xe0,0xc6,0xff,0x02,0x10,0x43
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f30:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x45
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
    li x5, 0xffffffffffffffff    // t0
    li x6, 0x400bff1b80000       // t1
    li x7, 0xffffffffffffffff    // t2
    li x8, 0x7fffffff            // fp
    li x9, 0x80019082            // s1
    li x10, 0x200                // a0
    li x11, 0x7ff8000000000000   // a1
    li x12, 0x7ffffe92           // a2
    li x13, 0x8018009e           // a3
    li x14, 0x6000               // a4
    li x15, 0xffffffffffffffff   // a5
    li x16, 0x7ffff8d2           // a6
    li x17, 0x7fffffffffffffff   // a7
    li x18, 0x200                // s2
    li x19, 0x80000241           // s3
    li x20, 0x1                  // s4
    li x21, 0x80000012           // s5
    li x22, 0x8027f893           // s6
    li x23, 0x80000277           // s7
    li x24, 0x5e                 // s8
    li x25, 0x2000015            // s9
    li x26, 0x7fffffffffffffff   // s10
    li x27, 0x0                  // s11
    li x28, 0x80180186           // t3
    li x29, 0xc00                // t4
    li x30, 0x801861ca           // t5
    li x31, 0x80000543           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f27', 'x20'}, 'clob': {'x20', 'x28'}})
    
    li x28, 0xffff8
    and x20, x20, x28
    li x28, 0x801804b5
    add x20, x20, x28
    fsd f27, -0x4b5(x20)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        96418fd75cebfcb8d454897c1e98d2b1b358dd75        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f27, -0x4b5(x20)
+========================================================================================================================+
Attributes:  fcsr ['overflow', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        96418fd75cebfcb8d454897c1e98d2b1b358dd75        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f27, x4, b5, x20
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)
s4(x20)             0x00000000801804b5(2149057717)                  0x00000000801804b5(2149057717)
f27                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
sp(x2)              0x0000000000000200(512)                         0x0000000000000200(512)                         
gp(x3)              0x000000007ffffd40(2147482944)                  0x000000007ffffd40(2147482944)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t1(x6)              0x000400bff1b80000(1126724300963840)            0x000400bff1b80000(1126724300963840)            
t2(x7)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
fp(x8)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s1(x9)              0x0000000080019082(2147586178)                  0x0000000080019082(2147586178)                  
a0(x10)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a1(x11)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
a2(x12)             0x000000007ffffe92(2147483282)                  0x000000007ffffe92(2147483282)                  
a3(x13)             0x000000008018009e(2149056670)                  0x000000008018009e(2149056670)                  
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a6(x16)             0x000000007ffff8d2(2147481810)                  0x000000007ffff8d2(2147481810)                  
a7(x17)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s2(x18)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s3(x19)             0x0000000080000241(2147484225)                  0x0000000080000241(2147484225)                  
s4(x20)             0x00000000801804b5(2149057717)                  0x00000000801804b5(2149057717)                  
s5(x21)             0x0000000080000012(2147483666)                  0x0000000080000012(2147483666)                  
s6(x22)             0x000000008027f893(2150103187)                  0x000000008027f893(2150103187)                  
s7(x23)             0x0000000080000277(2147484279)                  0x0000000080000277(2147484279)                  
s8(x24)             0x000000000000005e(94)                          0x000000000000005e(94)                          
s9(x25)             0x0000000002000015(33554453)                    0x0000000002000015(33554453)                    
s10(x26)            0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x00000000801804b5(2149057717)                  0x00000000801804b5(2149057717)                  
t4(x29)             0x0000000000000c00(3072)                        0x0000000000000c00(3072)                        
t5(x30)             0x00000000801861ca(2149081546)                  0x00000000801861ca(2149081546)                  
t6(x31)             0x0000000080000543(2147484995)                  0x0000000080000543(2147484995)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            724be807b7d015300dffd288771b0236494c36e8        724be807b7d015300dffd288771b0236494c36e8        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        96418fd75cebfcb8d454897c1e98d2b1b358dd75        X
lastPC              0x0000000080000734(2147485492)                  0x0000000080000734(2147485492)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000045(69)                          0x0000000000000045(69)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffffffff7bff(65504.0_h)                   0xffffffffffff7bff(65504.0_h)                   
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7fffffff46c00000(nan_d)                       0x7fffffff46c00000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x417ffffe90000000(33554409.0_d)                0x417ffffe90000000(33554409.0_d)                
f13                 0x41dfffff50000000(2147482944.0_d)              0x41dfffff50000000(2147482944.0_d)              
f14                 0xffffffffceffb00b(-2144863616.0_s)             0xffffffffceffb00b(-2144863616.0_s)             
f15                 0xd1920793ca490e1f(-8.756385205883228e+84_d)    0xd1920793ca490e1f(-8.756385205883228e+84_d)    
f16                 0x41e000002d000000(2147484008.0_d)              0x41e000002d000000(2147484008.0_d)              
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff4efffffa(2147482880.0_s)              0xffffffff4efffffa(2147482880.0_s)              
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f28                 0x431002ffc6e00000(1126724300963840.0_d)        0x431002ffc6e00000(1126724300963840.0_d)        
f29                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f30                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

# FailID_001916 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1916
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
_reg_f1: .byte 0x37,0xdd,0x64,0x28,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f15:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f16:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f17:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f23:.byte 0x01,0x00,0x00,0xcf,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x01,0x00,0x00,0x4f,0xff,0xff,0xff,0x7f
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
    li x1, 0x100                 // ra
    li x2, 0x80000639            // sp
    li x3, 0xffffffffffffffff    // gp
    li x4, 0x80193224            // tp
    li x5, 0x0                   // t0
    li x6, 0x6000                // t1
    li x7, 0x7ffffe12            // t2
    li x8, 0x42                  // fp
    li x9, 0x0                   // s1
    li x10, 0x801ffab2           // a0
    li x11, 0x80180281           // a1
    li x12, 0x800000d0           // a2
    li x13, 0x8017fdcc           // a3
    li x14, 0x7ffffa92           // a4
    li x15, 0xd5                 // a5
    li x16, 0x80005fa7           // a6
    li x17, 0x12                 // a7
    li x18, 0x17                 // s2
    li x19, 0xffffffffe49d2000   // s3
    li x20, 0x7fffffa7           // s4
    li x21, 0xb37db784           // s5
    li x22, 0x8027b660           // s6
    li x23, 0x7ffffca1           // s7
    li x24, 0x1                  // s8
    li x25, 0xffffffffffffffff   // s9
    li x26, 0xffffffffffffffff   // s10
    li x27, 0x8017fb0c           // s11
    li x28, 0x80000639           // t3
    li x29, 0x8017faec           // t4
    li x30, 0x0                  // t5
    li x31, 0x41db081800000000   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f31', 'x31'}, 'clob': {'x31', 'x20'}})
    
    li x20, 0xffff8
    and x31, x31, x20
    li x20, 0x8017fc3a
    add x31, x31, x20
    fsd f31, 0x3c6(x31)
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
Instruction: fsd f31, 0x3c6(x31)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5871a0e2b5463641eb5587b9e29814822e3a2ec9        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f31, x3, c6, x31
gp(x3)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)
t6(x31)             0x000000008017fc3a(2149055546)                  0x000000008017fc3a(2149055546)
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000100(256)                         0x0000000000000100(256)                         
sp(x2)              0x0000000080000639(2147485241)                  0x0000000080000639(2147485241)                  
gp(x3)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
tp(x4)              0x0000000080193224(2149134884)                  0x0000000080193224(2149134884)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t2(x7)              0x000000007ffffe12(2147483154)                  0x000000007ffffe12(2147483154)                  
fp(x8)              0x0000000000000042(66)                          0x0000000000000042(66)                          
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x00000000801ffab2(2149579442)                  0x00000000801ffab2(2149579442)                  
a1(x11)             0x0000000080180281(2149057153)                  0x0000000080180281(2149057153)                  
a2(x12)             0x00000000800000d0(2147483856)                  0x00000000800000d0(2147483856)                  
a3(x13)             0x000000008017fdcc(2149055948)                  0x000000008017fdcc(2149055948)                  
a4(x14)             0x000000007ffffa92(2147482258)                  0x000000007ffffa92(2147482258)                  
a5(x15)             0x00000000000000d5(213)                         0x00000000000000d5(213)                         
a6(x16)             0x0000000080005fa7(2147508135)                  0x0000000080005fa7(2147508135)                  
a7(x17)             0x0000000000000012(18)                          0x0000000000000012(18)                          
s2(x18)             0x0000000000000017(23)                          0x0000000000000017(23)                          
s3(x19)             0xffffffffe49d2000(18446744073250086912)        0xffffffffe49d2000(18446744073250086912)        
s4(x20)             0x000000008017fc3a(2149055546)                  0x000000008017fc3a(2149055546)                  
s5(x21)             0x00000000b37db784(3011360644)                  0x00000000b37db784(3011360644)                  
s6(x22)             0x000000008027b660(2150086240)                  0x000000008027b660(2150086240)                  
s7(x23)             0x000000007ffffca1(2147482785)                  0x000000007ffffca1(2147482785)                  
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s10(x26)            0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s11(x27)            0x000000008017fb0c(2149055244)                  0x000000008017fb0c(2149055244)                  
t3(x28)             0x0000000080000639(2147485241)                  0x0000000080000639(2147485241)                  
t4(x29)             0x000000008017faec(2149055212)                  0x000000008017faec(2149055212)                  
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x000000008017fc3a(2149055546)                  0x000000008017fc3a(2149055546)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            2c013ed6337d443aa217b5683a55fd01179bbfa6        2c013ed6337d443aa217b5683a55fd01179bbfa6        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5871a0e2b5463641eb5587b9e29814822e3a2ec9        X
lastPC              0x0000000080000730(2147485488)                  0x0000000080000730(2147485488)                  
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
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff2864dd37(1.2704510803562743e-14_s)    0xffffffff2864dd37(1.2704510803562743e-14_s)    
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f15                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f16                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f17                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f18                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f23                 0xffffffffcf000001(-2147483904.0_s)             0xffffffffcf000001(-2147483904.0_s)             
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f27                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f28                 0x7fffffff4f000001(nan_d)                       0x7fffffff4f000001(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

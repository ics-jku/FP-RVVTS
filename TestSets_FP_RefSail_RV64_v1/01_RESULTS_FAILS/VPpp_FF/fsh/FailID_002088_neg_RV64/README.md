# FailID_002088 VP++ FF neg RV64 fsh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2088
* Isolated failing instruction: `fsh`
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
_reg_f1: .byte 0x78,0x57,0x04,0x6e,0xff,0xff,0xff,0x7f
_reg_f2: .byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0xf0,0xe1,0xd1,0xc1
_reg_f4: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xdf,0x41
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x78,0x57,0x04,0x6e,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f12:.byte 0xfa,0xf4,0x27,0x80,0x00,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0x00,0x44,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x20,0x74,0x00,0x03,0xe0,0x41
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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
    li x1, 0x0                   // ra
    li x2, 0x801ff958            // sp
    li x3, 0x8023b013            // gp
    li x4, 0x1                   // tp
    li x5, 0x80180b63            // t0
    li x6, 0x8018079b            // t1
    li x7, 0x8018079b            // t2
    li x8, 0x7ffff919            // fp
    li x9, 0x801803f2            // s1
    li x10, 0xffffffffcc776000   // a0
    li x11, 0x7ffffc96           // a1
    li x12, 0x8018020a           // a2
    li x13, 0x7fc00000           // a3
    li x14, 0x80000310           // a4
    li x15, 0x6b039000           // a5
    li x16, 0x82                 // a6
    li x17, 0x0                  // a7
    li x18, 0x8018020a           // s2
    li x19, 0x7ffff962           // s3
    li x20, 0x33c3c20c           // s4
    li x21, 0x7ffffd8e           // s5
    li x22, 0x8000045a           // s6
    li x23, 0x33c3c75c           // s7
    li x24, 0x6000               // s8
    li x25, 0x400c010500000000   // s9
    li x26, 0x8017f9fd           // s10
    li x27, 0x1a                 // s11
    li x28, 0x8018064a           // t3
    li x29, 0x3232774            // t4
    li x30, 0x7ffffd72           // t5
    li x31, 0x7ffff8c5           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f4', 'x21'}, 'clob': {'x18', 'x21'}})
    
    li x18, 0xffffe
    and x21, x21, x18
    li x18, 0x8017fa2b
    add x21, x21, x18
    fsh f4, 0x5d5(x21)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsh f4, 0x5d5(x21)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f4, x5, d5, x21
t0(x5)              0x0000000080180b63(2149059427)                  0x0000000080180b63(2149059427)
s5(x21)             0x000000008027f7b9(2150102969)                  0x000000008027f7b9(2150102969)
f4                  0x41dfffffffc00000(2147483647.0_d)              0x41dfffffffc00000(2147483647.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x00000000801ff958(2149579096)                  0x00000000801ff958(2149579096)                  
gp(x3)              0x000000008023b013(2149822483)                  0x000000008023b013(2149822483)                  
tp(x4)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t0(x5)              0x0000000080180b63(2149059427)                  0x0000000080180b63(2149059427)                  
t1(x6)              0x000000008018079b(2149058459)                  0x000000008018079b(2149058459)                  
t2(x7)              0x000000008018079b(2149058459)                  0x000000008018079b(2149058459)                  
fp(x8)              0x000000007ffff919(2147481881)                  0x000000007ffff919(2147481881)                  
s1(x9)              0x00000000801803f2(2149057522)                  0x00000000801803f2(2149057522)                  
a0(x10)             0xffffffffcc776000(18446744072844959744)        0xffffffffcc776000(18446744072844959744)        
a1(x11)             0x000000007ffffc96(2147482774)                  0x000000007ffffc96(2147482774)                  
a2(x12)             0x000000008018020a(2149057034)                  0x000000008018020a(2149057034)                  
a3(x13)             0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
a4(x14)             0x0000000080000310(2147484432)                  0x0000000080000310(2147484432)                  
a5(x15)             0x000000006b039000(1795395584)                  0x000000006b039000(1795395584)                  
a6(x16)             0x0000000000000082(130)                         0x0000000000000082(130)                         
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x000000008017fa2b(2149055019)                  0x000000008017fa2b(2149055019)                  
s3(x19)             0x000000007ffff962(2147481954)                  0x000000007ffff962(2147481954)                  
s4(x20)             0x0000000033c3c20c(868467212)                   0x0000000033c3c20c(868467212)                   
s5(x21)             0x000000008027f7b9(2150102969)                  0x000000008027f7b9(2150102969)                  
s6(x22)             0x000000008000045a(2147484762)                  0x000000008000045a(2147484762)                  
s7(x23)             0x0000000033c3c75c(868468572)                   0x0000000033c3c75c(868468572)                   
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x400c010500000000(4615064839134380032)         0x400c010500000000(4615064839134380032)         
s10(x26)            0x000000008017f9fd(2149054973)                  0x000000008017f9fd(2149054973)                  
s11(x27)            0x000000000000001a(26)                          0x000000000000001a(26)                          
t3(x28)             0x000000008018064a(2149058122)                  0x000000008018064a(2149058122)                  
t4(x29)             0x0000000003232774(52635508)                    0x0000000003232774(52635508)                    
t5(x30)             0x000000007ffffd72(2147482994)                  0x000000007ffffd72(2147482994)                  
t6(x31)             0x000000007ffff8c5(2147481797)                  0x000000007ffff8c5(2147481797)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            6271ff317e344198b30e2b36258867e875578c79        6271ff317e344198b30e2b36258867e875578c79        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000748(2147485512)                  0x0000000080000748(2147485512)                  
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
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7fffffff6e045778(nan_d)                       0x7fffffff6e045778(nan_d)                       
f2                  0xfffffffffffffe00(nan_h)                       0xfffffffffffffe00(nan_h)                       
f3                  0xc1d1e1f000000000(-1200078848.0_d)             0xc1d1e1f000000000(-1200078848.0_d)             
f4                  0x41dfffffffc00000(2147483647.0_d)              0x41dfffffffc00000(2147483647.0_d)              
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff6e045778(1.0239441131675492e+28_s)    0xffffffff6e045778(1.0239441131675492e+28_s)    
f10                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f11                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
f12                 0x000000008027f4fa(1.0622916647e-314_d)         0x000000008027f4fa(1.0622916647e-314_d)         
f13                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)                     
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x41e0030074200000(2149057441.0_d)              0x41e0030074200000(2149057441.0_d)              
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f23                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
f24                 0x7fffffff42140000(nan_d)                       0x7fffffff42140000(nan_d)                       
f25                 0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

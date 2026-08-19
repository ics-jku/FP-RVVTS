# FailID_001827 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1827
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
_reg_f0: .byte 0x00,0x00,0x00,0xb2,0xff,0x02,0xe0,0x41
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0xdc,0x97,0x40
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x4f,0x7c,0xac,0x4e,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f11:.byte 0xff,0x7b,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f12:.byte 0xf3,0xcf,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x80,0xf1,0xec,0xcf,0xea,0x41
_reg_f15:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0xa0,0x77,0x4c,0x00,0x00,0x00,0x00
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0xc0,0x9d,0xff,0xff,0xdf,0x41
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x40,0x52,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x70
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017f8e7            // ra
    li x2, 0x801806a2            // sp
    li x3, 0xa59696d0            // gp
    li x4, 0x3b                  // tp
    li x5, 0x80000846            // t0
    li x6, 0x801ff3e0            // t1
    li x7, 0x80103514            // t2
    li x8, 0x0                   // fp
    li x9, 0x80185f15            // s1
    li x10, 0x8017fab0           // a0
    li x11, 0x8017ff15           // a1
    li x12, 0x80000514           // a2
    li x13, 0x0                  // a3
    li x14, 0x80180160           // a4
    li x15, 0x1                  // a5
    li x16, 0x0                  // a6
    li x17, 0x89                 // a7
    li x18, 0x8017fa75           // s2
    li x19, 0x45                 // s3
    li x20, 0xffffffff7fe7fd75   // s4
    li x21, 0x4d                 // s5
    li x22, 0x1                  // s6
    li x23, 0x8018061e           // s7
    li x24, 0x7ffffbf9           // s8
    li x25, 0x0                  // s9
    li x26, 0x1                  // s10
    li x27, 0x801ff8d3           // s11
    li x28, 0x1                  // t3
    li x29, 0x8018052a           // t4
    li x30, 0x7fffffd1           // t5
    li x31, 0x8017fa91           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x9', 'f31'}, 'clob': {'x9', 'x23'}})
    
    li x23, 0xffff8
    and x9, x9, x23
    li x23, 0x8018051e
    add x9, x9, x23
    fsd f31, -0x51e(x9)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        3d5ef88f8a5538a2bfaebe5bbc42092cc88d3f47        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f31, -0x51e(x9)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        3d5ef88f8a5538a2bfaebe5bbc42092cc88d3f47        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f31, x51, x9
s1(x9)              0x000000008020642e(2149606446)                  0x000000008020642e(2149606446)
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017f8e7(2149054695)                  0x000000008017f8e7(2149054695)                  
sp(x2)              0x00000000801806a2(2149058210)                  0x00000000801806a2(2149058210)                  
gp(x3)              0x00000000a59696d0(2778109648)                  0x00000000a59696d0(2778109648)                  
tp(x4)              0x000000000000003b(59)                          0x000000000000003b(59)                          
t0(x5)              0x0000000080000846(2147485766)                  0x0000000080000846(2147485766)                  
t1(x6)              0x00000000801ff3e0(2149577696)                  0x00000000801ff3e0(2149577696)                  
t2(x7)              0x0000000080103514(2148545812)                  0x0000000080103514(2148545812)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x000000008020642e(2149606446)                  0x000000008020642e(2149606446)                  
a0(x10)             0x000000008017fab0(2149055152)                  0x000000008017fab0(2149055152)                  
a1(x11)             0x000000008017ff15(2149056277)                  0x000000008017ff15(2149056277)                  
a2(x12)             0x0000000080000514(2147484948)                  0x0000000080000514(2147484948)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x0000000080180160(2149056864)                  0x0000000080180160(2149056864)                  
a5(x15)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x0000000000000089(137)                         0x0000000000000089(137)                         
s2(x18)             0x000000008017fa75(2149055093)                  0x000000008017fa75(2149055093)                  
s3(x19)             0x0000000000000045(69)                          0x0000000000000045(69)                          
s4(x20)             0xffffffff7fe7fd75(18446744071560494453)        0xffffffff7fe7fd75(18446744071560494453)        
s5(x21)             0x000000000000004d(77)                          0x000000000000004d(77)                          
s6(x22)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s7(x23)             0x000000008018051e(2149057822)                  0x000000008018051e(2149057822)                  
s8(x24)             0x000000007ffffbf9(2147482617)                  0x000000007ffffbf9(2147482617)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000001(1)                           0x0000000000000001(1)                           
s11(x27)            0x00000000801ff8d3(2149578963)                  0x00000000801ff8d3(2149578963)                  
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x000000008018052a(2149057834)                  0x000000008018052a(2149057834)                  
t5(x30)             0x000000007fffffd1(2147483601)                  0x000000007fffffd1(2147483601)                  
t6(x31)             0x000000008017fa91(2149055121)                  0x000000008017fa91(2149055121)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            7dca62ffad64112bc90742f9b8d9d0972d356571        7dca62ffad64112bc90742f9b8d9d0972d356571        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        3d5ef88f8a5538a2bfaebe5bbc42092cc88d3f47        X
lastPC              0x0000000080000764(2147485540)                  0x0000000080000764(2147485540)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000070(112)                         0x0000000000000070(112)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x41e002ffb2000000(2149055888.0_d)              0x41e002ffb2000000(2149055888.0_d)              
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x4097dc0000000000(1527.0_d)                    0x4097dc0000000000(1527.0_d)                    
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f8                  0xffffffff4eac7c4f(1446913920.0_s)              0xffffffff4eac7c4f(1446913920.0_s)              
f9                  0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f10                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f11                 0xffffffffffff7bff(65504.0_h)                   0xffffffffffff7bff(65504.0_h)                   
f12                 0xffffffffceffcff3(-2145909120.0_s)             0xffffffffceffcff3(-2145909120.0_s)             
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41eacfecf1800000(3598673804.0_d)              0x41eacfecf1800000(3598673804.0_d)              
f15                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f16                 0x000000004c77a000(6.338408486e-315_d)          0x000000004c77a000(6.338408486e-315_d)          
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x41dfffff9dc00000(2147483255.0_d)              0x41dfffff9dc00000(2147483255.0_d)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff52400000(206158430208.0_s)            0xffffffff52400000(206158430208.0_s)            
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

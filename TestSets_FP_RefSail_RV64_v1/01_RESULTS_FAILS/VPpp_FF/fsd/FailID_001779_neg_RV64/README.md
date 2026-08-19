# FailID_001779 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1779
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x01,0x00,0x31,0xcf,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x1b,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x04,0x43,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x30,0x40
_reg_f14:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0xc1
_reg_f15:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0xff,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0xfa,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0x41
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x21
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7b                  // ra
    li x2, 0x63                  // sp
    li x3, 0x2d240000            // gp
    li x4, 0x7ffffd39            // tp
    li x5, 0x800d4bf1            // t0
    li x6, 0x802004dd            // t1
    li x7, 0x7ffffaad            // t2
    li x8, 0x7ffffaad            // fp
    li x9, 0x8000112a            // s1
    li x10, 0x4                  // a0
    li x11, 0x1                  // a1
    li x12, 0x8017ffe6           // a2
    li x13, 0x803fffff           // a3
    li x14, 0x80200c90           // a4
    li x15, 0x1                  // a5
    li x16, 0x8017fefa           // a6
    li x17, 0x0                  // a7
    li x18, 0xa01a973c           // s2
    li x19, 0xffffffff7ffffdd2   // s3
    li x20, 0x80180169           // s4
    li x21, 0x1                  // s5
    li x22, 0x1                  // s6
    li x23, 0x1                  // s7
    li x24, 0x18                 // s8
    li x25, 0x0                  // s9
    li x26, 0x8000012a           // s10
    li x27, 0x80187fb7           // s11
    li x28, 0x1                  // t3
    li x29, 0x8017ff03           // t4
    li x30, 0x802006a0           // t5
    li x31, 0x801ff8e2           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x22', 'mstatus.fs/vs.fs', 'f7'}, 'clob': {'x22', 'x9'}})
    
    li x9, 0xffff8
    and x22, x22, x9
    li x9, 0x8017ff40
    add x22, x22, x9
    fsd f7, 0xc0(x22)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        df2f4e453f8699ccff3a9cb883497152cd9e8831        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f7, 0xc0(x22)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        df2f4e453f8699ccff3a9cb883497152cd9e8831        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f7, xc0, x22
s6(x22)             0x000000008017ff40(2149056320)                  0x000000008017ff40(2149056320)
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000000000007b(123)                         0x000000000000007b(123)                         
sp(x2)              0x0000000000000063(99)                          0x0000000000000063(99)                          
gp(x3)              0x000000002d240000(757334016)                   0x000000002d240000(757334016)                   
tp(x4)              0x000000007ffffd39(2147482937)                  0x000000007ffffd39(2147482937)                  
t0(x5)              0x00000000800d4bf1(2148355057)                  0x00000000800d4bf1(2148355057)                  
t1(x6)              0x00000000802004dd(2149582045)                  0x00000000802004dd(2149582045)                  
t2(x7)              0x000000007ffffaad(2147482285)                  0x000000007ffffaad(2147482285)                  
fp(x8)              0x000000007ffffaad(2147482285)                  0x000000007ffffaad(2147482285)                  
s1(x9)              0x000000008017ff40(2149056320)                  0x000000008017ff40(2149056320)                  
a0(x10)             0x0000000000000004(4)                           0x0000000000000004(4)                           
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x000000008017ffe6(2149056486)                  0x000000008017ffe6(2149056486)                  
a3(x13)             0x00000000803fffff(2151677951)                  0x00000000803fffff(2151677951)                  
a4(x14)             0x0000000080200c90(2149584016)                  0x0000000080200c90(2149584016)                  
a5(x15)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a6(x16)             0x000000008017fefa(2149056250)                  0x000000008017fefa(2149056250)                  
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x00000000a01a973c(2686097212)                  0x00000000a01a973c(2686097212)                  
s3(x19)             0xffffffff7ffffdd2(18446744071562067410)        0xffffffff7ffffdd2(18446744071562067410)        
s4(x20)             0x0000000080180169(2149056873)                  0x0000000080180169(2149056873)                  
s5(x21)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s6(x22)             0x000000008017ff40(2149056320)                  0x000000008017ff40(2149056320)                  
s7(x23)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s8(x24)             0x0000000000000018(24)                          0x0000000000000018(24)                          
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x000000008000012a(2147483946)                  0x000000008000012a(2147483946)                  
s11(x27)            0x0000000080187fb7(2149089207)                  0x0000000080187fb7(2149089207)                  
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x000000008017ff03(2149056259)                  0x000000008017ff03(2149056259)                  
t5(x30)             0x00000000802006a0(2149582496)                  0x00000000802006a0(2149582496)                  
t6(x31)             0x00000000801ff8e2(2149578978)                  0x00000000801ff8e2(2149578978)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            4eff4a9c3e122cb6e2a672b0300b7cc9929e9115        4eff4a9c3e122cb6e2a672b0300b7cc9929e9115        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        df2f4e453f8699ccff3a9cb883497152cd9e8831        X
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000021(33)                          0x0000000000000021(33)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f5                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f6                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffffcf310001(-2969567488.0_s)             0xffffffffcf310001(-2969567488.0_s)             
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0x000000000000001b(1.33e-322_d)                 0x000000000000001b(1.33e-322_d)                 
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff43040000(132.0_s)                     0xffffffff43040000(132.0_s)                     
f13                 0x4030000000000000(16.0_d)                      0x4030000000000000(16.0_d)                      
f14                 0xc1e0030003200000(-2149056537.0_d)             0xc1e0030003200000(-2149056537.0_d)             
f15                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f16                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f20                 0xffffffff4effffff(2147483520.0_s)              0xffffffff4effffff(2147483520.0_s)              
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff4efffffa(2147482880.0_s)              0xffffffff4efffffa(2147482880.0_s)              
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x41e0030003200000(2149056537.0_d)              0x41e0030003200000(2149056537.0_d)              
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
STATES DIFFER: True
```

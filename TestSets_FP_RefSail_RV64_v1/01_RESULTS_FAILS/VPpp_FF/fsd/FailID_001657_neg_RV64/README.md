# FailID_001657 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1657
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
_reg_f0: .byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0xf1,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x93,0x17,0x00,0x4f,0xff,0xff,0xff,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0xfc,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0xbc,0x6d,0x47,0xe2,0xcd,0xd0,0x0c,0x74
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x62
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x2006012bc000        // ra
    li x2, 0x8022bd43            // sp
    li x3, 0x6d                  // gp
    li x4, 0x32                  // tp
    li x5, 0x802065db            // t0
    li x6, 0x802000ec            // t1
    li x7, 0xc0000000000         // t2
    li x8, 0x0                   // fp
    li x9, 0x91                  // s1
    li x10, 0x200                // a0
    li x11, 0x801805ee           // a1
    li x12, 0x0                  // a2
    li x13, 0x8017fecd           // a3
    li x14, 0x6000               // a4
    li x15, 0x9d30f748           // a5
    li x16, 0x6000               // a6
    li x17, 0x800004e3           // a7
    li x18, 0x5f17e000           // s2
    li x19, 0x800005e5           // s3
    li x20, 0x801805f9           // s4
    li x21, 0x6000               // s5
    li x22, 0x8017f9b5           // s6
    li x23, 0x7ffff9f8           // s7
    li x24, 0x80200bc7           // s8
    li x25, 0x801807e9           // s9
    li x26, 0x801805ee           // s10
    li x27, 0x6000               // s11
    li x28, 0x8025060d           // t3
    li x29, 0xc80000000          // t4
    li x30, 0x800004ab           // t5
    li x31, 0x800006f4           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f8', 'mstatus.fs/vs.fs', 'x4'}, 'clob': {'x4', 'x18'}})
    
    li x18, 0xffff8
    and x4, x4, x18
    li x18, 0x801802d5
    add x4, x4, x18
    fsd f8, -0x2d5(x4)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c1438185479687c4ced47ac2851a7333b8c5842e        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f8, -0x2d5(x4)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c1438185479687c4ced47ac2851a7333b8c5842e        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x2, d5, x4
sp(x2)              0x000000008022bd43(2149760323)                  0x000000008022bd43(2149760323)
tp(x4)              0x0000000080180305(2149057285)                  0x0000000080180305(2149057285)
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00002006012bc000(35210161537024)              0x00002006012bc000(35210161537024)              
sp(x2)              0x000000008022bd43(2149760323)                  0x000000008022bd43(2149760323)                  
gp(x3)              0x000000000000006d(109)                         0x000000000000006d(109)                         
tp(x4)              0x0000000080180305(2149057285)                  0x0000000080180305(2149057285)                  
t0(x5)              0x00000000802065db(2149606875)                  0x00000000802065db(2149606875)                  
t1(x6)              0x00000000802000ec(2149581036)                  0x00000000802000ec(2149581036)                  
t2(x7)              0x00000c0000000000(13194139533312)              0x00000c0000000000(13194139533312)              
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x0000000000000091(145)                         0x0000000000000091(145)                         
a0(x10)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a1(x11)             0x00000000801805ee(2149058030)                  0x00000000801805ee(2149058030)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x000000008017fecd(2149056205)                  0x000000008017fecd(2149056205)                  
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x000000009d30f748(2637231944)                  0x000000009d30f748(2637231944)                  
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x00000000800004e3(2147484899)                  0x00000000800004e3(2147484899)                  
s2(x18)             0x00000000801802d5(2149057237)                  0x00000000801802d5(2149057237)                  
s3(x19)             0x00000000800005e5(2147485157)                  0x00000000800005e5(2147485157)                  
s4(x20)             0x00000000801805f9(2149058041)                  0x00000000801805f9(2149058041)                  
s5(x21)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s6(x22)             0x000000008017f9b5(2149054901)                  0x000000008017f9b5(2149054901)                  
s7(x23)             0x000000007ffff9f8(2147482104)                  0x000000007ffff9f8(2147482104)                  
s8(x24)             0x0000000080200bc7(2149583815)                  0x0000000080200bc7(2149583815)                  
s9(x25)             0x00000000801807e9(2149058537)                  0x00000000801807e9(2149058537)                  
s10(x26)            0x00000000801805ee(2149058030)                  0x00000000801805ee(2149058030)                  
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x000000008025060d(2149910029)                  0x000000008025060d(2149910029)                  
t4(x29)             0x0000000c80000000(53687091200)                 0x0000000c80000000(53687091200)                 
t5(x30)             0x00000000800004ab(2147484843)                  0x00000000800004ab(2147484843)                  
t6(x31)             0x00000000800006f4(2147485428)                  0x00000000800006f4(2147485428)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            358fa1757eed7be8766bdbebb0cc5175659379b7        358fa1757eed7be8766bdbebb0cc5175659379b7        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c1438185479687c4ced47ac2851a7333b8c5842e        X
lastPC              0x0000000080000760(2147485536)                  0x0000000080000760(2147485536)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000062(98)                          0x0000000000000062(98)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff4f0017fd(2149055744.0_s)              0xffffffff4f0017fd(2149055744.0_s)              
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff4efffff1(2147481728.0_s)              0xffffffff4efffff1(2147481728.0_s)              
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7fffffff4f001793(nan_d)                       0x7fffffff4f001793(nan_d)                       
f22                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xfffffffffffffc00(-inf_h)                      0xfffffffffffffc00(-inf_h)                      
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x740cd0cde2476dbc(1.0315604867321677e+251_d)   0x740cd0cde2476dbc(1.0315604867321677e+251_d)   
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

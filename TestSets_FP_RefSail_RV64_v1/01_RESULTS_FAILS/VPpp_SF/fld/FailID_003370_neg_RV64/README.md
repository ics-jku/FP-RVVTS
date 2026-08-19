# FailID_003370 VP++ SF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3370
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0xbf
_reg_f2: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x02,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f13:.byte 0xc2,0xfc,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x92,0x07,0x18,0x80,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x80,0xbf,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x48
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80005d98            // ra
    li x2, 0x800067f1            // sp
    li x3, 0x1                   // gp
    li x4, 0x80180689            // tp
    li x5, 0x1fff                // t0
    li x6, 0x8017fc3c            // t1
    li x7, 0xfffffffff0000000    // t2
    li x8, 0x0                   // fp
    li x9, 0x0                   // s1
    li x10, 0xffffffffffffffff   // a0
    li x11, 0x6000               // a1
    li x12, 0x80180457           // a2
    li x13, 0x801ff902           // a3
    li x14, 0xfffffffffffffd5d   // a4
    li x15, 0x40                 // a5
    li x16, 0x8000071e           // a6
    li x17, 0x7ffffd98           // a7
    li x18, 0x80000132           // s2
    li x19, 0x48                 // s3
    li x20, 0x8017fba2           // s4
    li x21, 0x80200411           // s5
    li x22, 0x0                  // s6
    li x23, 0x80185c3c           // s7
    li x24, 0x7ffffd04           // s8
    li x25, 0x7ffffe21           // s9
    li x26, 0x80000667           // s10
    li x27, 0x800004e2           // s11
    li x28, 0x6c                 // t3
    li x29, 0x0                  // t4
    li x30, 0x7ffffb29           // t5
    li x31, 0x800007f1           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x18'}, 'clob': {'f30', 'x18', 'x25'}})
    
    li x25, 0x1ffff8
    and x18, x18, x25
    li x25, 0x7ffffcf2
    add x18, x18, x25
    fld f30, 0x30e(x18)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f30                 0x7ff8000000000000(nan_d)                       0x3002a073000062b7(2.01079742186191e-77_d)      X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f30, 0x30e(x18)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f30                 0x7ff8000000000000(nan_d)                       0x3002a073000062b7(2.01079742186191e-77_d)      X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f30, x30, x18
s2(x18)             0x000000007ffffe22(2147483170)                  0x000000007ffffe22(2147483170)
t5(x30)             0x000000007ffffb29(2147482409)                  0x000000007ffffb29(2147482409)
f30                 0x7ff8000000000000(nan_d)                       0x3002a073000062b7(2.01079742186191e-77_d)      X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080005d98(2147507608)                  0x0000000080005d98(2147507608)                  
sp(x2)              0x00000000800067f1(2147510257)                  0x00000000800067f1(2147510257)                  
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x0000000080180689(2149058185)                  0x0000000080180689(2149058185)                  
t0(x5)              0x0000000000001fff(8191)                        0x0000000000001fff(8191)                        
t1(x6)              0x000000008017fc3c(2149055548)                  0x000000008017fc3c(2149055548)                  
t2(x7)              0xfffffffff0000000(18446744073441116160)        0xfffffffff0000000(18446744073441116160)        
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a1(x11)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a2(x12)             0x0000000080180457(2149057623)                  0x0000000080180457(2149057623)                  
a3(x13)             0x00000000801ff902(2149579010)                  0x00000000801ff902(2149579010)                  
a4(x14)             0xfffffffffffffd5d(18446744073709550941)        0xfffffffffffffd5d(18446744073709550941)        
a5(x15)             0x0000000000000040(64)                          0x0000000000000040(64)                          
a6(x16)             0x000000008000071e(2147485470)                  0x000000008000071e(2147485470)                  
a7(x17)             0x000000007ffffd98(2147483032)                  0x000000007ffffd98(2147483032)                  
s2(x18)             0x000000007ffffe22(2147483170)                  0x000000007ffffe22(2147483170)                  
s3(x19)             0x0000000000000048(72)                          0x0000000000000048(72)                          
s4(x20)             0x000000008017fba2(2149055394)                  0x000000008017fba2(2149055394)                  
s5(x21)             0x0000000080200411(2149581841)                  0x0000000080200411(2149581841)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000080185c3c(2149080124)                  0x0000000080185c3c(2149080124)                  
s8(x24)             0x000000007ffffd04(2147482884)                  0x000000007ffffd04(2147482884)                  
s9(x25)             0x000000007ffffcf2(2147482866)                  0x000000007ffffcf2(2147482866)                  
s10(x26)            0x0000000080000667(2147485287)                  0x0000000080000667(2147485287)                  
s11(x27)            0x00000000800004e2(2147484898)                  0x00000000800004e2(2147484898)                  
t3(x28)             0x000000000000006c(108)                         0x000000000000006c(108)                         
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x000000007ffffb29(2147482409)                  0x000000007ffffb29(2147482409)                  
t6(x31)             0x00000000800007f1(2147485681)                  0x00000000800007f1(2147485681)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            6f2a894cbebce6b448ac475ea10fafa5ba7fc0bb        6f2a894cbebce6b448ac475ea10fafa5ba7fc0bb        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000730(2147485488)                  0x0000000080000730(2147485488)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000048(72)                          0x0000000000000048(72)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f1                  0xbff0000000000000(-1.0_d)                      0xbff0000000000000(-1.0_d)                      
f2                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff4f000002(2147484160.0_s)              0xffffffff4f000002(2147484160.0_s)              
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f11                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f12                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f13                 0xffffffff8017fcc2(-2.2028888300663995e-39_s)   0xffffffff8017fcc2(-2.2028888300663995e-39_s)   
f14                 0xffffffff80180792(-2.2067676242156506e-39_s)   0xffffffff80180792(-2.2067676242156506e-39_s)   
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffffbf800000(-1.0_s)                      0xffffffffbf800000(-1.0_s)                      
f17                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x3002a073000062b7(2.01079742186191e-77_d)      X
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

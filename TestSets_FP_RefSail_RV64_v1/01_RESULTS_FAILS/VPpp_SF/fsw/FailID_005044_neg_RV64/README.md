# FailID_005044 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 5044
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x82,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x08,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0xb0,0x25,0xbc,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x3d,0xb1,0xaf,0xdd,0x48,0xf5,0x3e,0xde
_reg_f24:.byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x18,0x40
_reg_f29:.byte 0x83,0x03,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x3e,0xf9,0x17,0x80,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x82
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x400c025e0           // ra
    li x2, 0x802001a9            // sp
    li x3, 0x8018049c            // gp
    li x4, 0x8018075f            // tp
    li x5, 0x100000              // t0
    li x6, 0x80000383            // t1
    li x7, 0x1004016e6           // t2
    li x8, 0x8                   // fp
    li x9, 0x8017f96f            // s1
    li x10, 0x1                  // a0
    li x11, 0x649                // a1
    li x12, 0xb0                 // a2
    li x13, 0x17                 // a3
    li x14, 0x82                 // a4
    li x15, 0xffffffffbc25b000   // a5
    li x16, 0x80180f89           // a6
    li x17, 0xffffffffffffffff   // a7
    li x18, 0x1                  // s2
    li x19, 0x80005fff           // s3
    li x20, 0x0                  // s4
    li x21, 0x80180587           // s5
    li x22, 0x0                  // s6
    li x23, 0x1                  // s7
    li x24, 0x6000               // s8
    li x25, 0x759d0c10           // s9
    li x26, 0x0                  // s10
    li x27, 0x100000             // s11
    li x28, 0xffffffff8a62f000   // t3
    li x29, 0x6000               // t4
    li x30, 0x8028075d           // t5
    li x31, 0x801ff826           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x2', 'f28'}, 'clob': {'x1', 'x2'}})
    
    li x1, 0xffffc
    and x2, x2, x1
    li x1, 0x8017fd27
    add x2, x2, x1
    fsw f28, 0x2d9(x2)
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
Instruction: fsw f28, 0x2d9(x2)
+========================================================================================================================+
Attributes:  fcsr ['underflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f28, x2, d9, x2
sp(x2)              0x000000008017fecf(2149056207)                  0x000000008017fecf(2149056207)
f28                 0x4018000000000000(6.0_d)                       0x4018000000000000(6.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fd27(2149055783)                  0x000000008017fd27(2149055783)                  
sp(x2)              0x000000008017fecf(2149056207)                  0x000000008017fecf(2149056207)                  
gp(x3)              0x000000008018049c(2149057692)                  0x000000008018049c(2149057692)                  
tp(x4)              0x000000008018075f(2149058399)                  0x000000008018075f(2149058399)                  
t0(x5)              0x0000000000100000(1048576)                     0x0000000000100000(1048576)                     
t1(x6)              0x0000000080000383(2147484547)                  0x0000000080000383(2147484547)                  
t2(x7)              0x00000001004016e6(4299167462)                  0x00000001004016e6(4299167462)                  
fp(x8)              0x0000000000000008(8)                           0x0000000000000008(8)                           
s1(x9)              0x000000008017f96f(2149054831)                  0x000000008017f96f(2149054831)                  
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x0000000000000649(1609)                        0x0000000000000649(1609)                        
a2(x12)             0x00000000000000b0(176)                         0x00000000000000b0(176)                         
a3(x13)             0x0000000000000017(23)                          0x0000000000000017(23)                          
a4(x14)             0x0000000000000082(130)                         0x0000000000000082(130)                         
a5(x15)             0xffffffffbc25b000(18446744072571170816)        0xffffffffbc25b000(18446744072571170816)        
a6(x16)             0x0000000080180f89(2149060489)                  0x0000000080180f89(2149060489)                  
a7(x17)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s2(x18)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s3(x19)             0x0000000080005fff(2147508223)                  0x0000000080005fff(2147508223)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x0000000080180587(2149057927)                  0x0000000080180587(2149057927)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x00000000759d0c10(1973226512)                  0x00000000759d0c10(1973226512)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x0000000000100000(1048576)                     0x0000000000100000(1048576)                     
t3(x28)             0xffffffff8a62f000(18446744071736324096)        0xffffffff8a62f000(18446744071736324096)        
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x000000008028075d(2150106973)                  0x000000008028075d(2150106973)                  
t6(x31)             0x00000000801ff826(2149578790)                  0x00000000801ff826(2149578790)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            b909420684d7f4b35d061b14fc292cf993b0a38e        b909420684d7f4b35d061b14fc292cf993b0a38e        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000720(2147485472)                  0x0000000080000720(2147485472)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000082(130)                         0x0000000000000082(130)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x0000000000000082(6.4e-322_d)                  0x0000000000000082(6.4e-322_d)                  
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff42140000(37.0_s)                      0xffffffff42140000(37.0_s)                      
f18                 0xffffffff4f001808(2149058560.0_s)              0xffffffff4f001808(2149058560.0_s)              
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffffbc25b000(-0.010112762451171875_s)     0xffffffffbc25b000(-0.010112762451171875_s)     
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0xde3ef548ddafb13d(-9.664353833149178e+145_d)   0xde3ef548ddafb13d(-9.664353833149178e+145_d)   
f24                 0x7fffffff42140000(nan_d)                       0x7fffffff42140000(nan_d)                       
f25                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x4018000000000000(6.0_d)                       0x4018000000000000(6.0_d)                       
f29                 0xffffffff80000383(-1.2597673194280105e-42_s)   0xffffffff80000383(-1.2597673194280105e-42_s)   
f30                 0x000000008017f93e(1.061774139e-314_d)          0x000000008017f93e(1.061774139e-314_d)          
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

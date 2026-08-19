# FailID_004342 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4342
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x23,0xbc,0x51,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x11,0x43,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0xa0,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0xc1
_reg_f15:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0xc1
_reg_f16:.byte 0x00,0x00,0x55,0x43,0xff,0xff,0xff,0xff
_reg_f17:.byte 0xc0,0x01,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f19:.byte 0xff,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f20:.byte 0xff,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x00,0xa2,0xde,0x03,0xe0,0x41
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x10
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801ffd7c            // ra
    li x2, 0x800001b3            // sp
    li x3, 0x8c                  // gp
    li x4, 0x2                   // tp
    li x5, 0x7fffffff            // t0
    li x6, 0x7fffffd5            // t1
    li x7, 0x8000063a            // t2
    li x8, 0x800002dd            // fp
    li x9, 0x80180088            // s1
    li x10, 0x17fad0             // a0
    li x11, 0x8007f221           // a1
    li x12, 0x0                  // a2
    li x13, 0x800006fb           // a3
    li x14, 0x80200d7c           // a4
    li x15, 0xffffffff80be5000   // a5
    li x16, 0x7fffff75           // a6
    li x17, 0xc0                 // a7
    li x18, 0x7f41af22           // s2
    li x19, 0x297                // s3
    li x20, 0x80280468           // s4
    li x21, 0x800002a2           // s5
    li x22, 0x1994e748           // s6
    li x23, 0x800000dd           // s7
    li x24, 0x1                  // s8
    li x25, 0x1                  // s9
    li x26, 0x801ffc5b           // s10
    li x27, 0x8017fe78           // s11
    li x28, 0x0                  // t3
    li x29, 0x0                  // t4
    li x30, 0x7f                 // t5
    li x31, 0x11                 // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'f6', 'fcsr.rm', 'x28'}, 'clob': {'x28', 'x30'}})
    
    li x30, 0xffff8
    and x28, x28, x30
    li x30, 0x80180443
    add x28, x28, x30
    fsd f6, -0x443(x28)
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
Instruction: fsd f6, -0x443(x28)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5871a0e2b5463641eb5587b9e29814822e3a2ec9        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f6, x443, x28
t3(x28)             0x0000000080180443(2149057603)                  0x0000000080180443(2149057603)
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801ffd7c(2149580156)                  0x00000000801ffd7c(2149580156)                  
sp(x2)              0x00000000800001b3(2147484083)                  0x00000000800001b3(2147484083)                  
gp(x3)              0x000000000000008c(140)                         0x000000000000008c(140)                         
tp(x4)              0x0000000000000002(2)                           0x0000000000000002(2)                           
t0(x5)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
t1(x6)              0x000000007fffffd5(2147483605)                  0x000000007fffffd5(2147483605)                  
t2(x7)              0x000000008000063a(2147485242)                  0x000000008000063a(2147485242)                  
fp(x8)              0x00000000800002dd(2147484381)                  0x00000000800002dd(2147484381)                  
s1(x9)              0x0000000080180088(2149056648)                  0x0000000080180088(2149056648)                  
a0(x10)             0x000000000017fad0(1571536)                     0x000000000017fad0(1571536)                     
a1(x11)             0x000000008007f221(2148004385)                  0x000000008007f221(2148004385)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x00000000800006fb(2147485435)                  0x00000000800006fb(2147485435)                  
a4(x14)             0x0000000080200d7c(2149584252)                  0x0000000080200d7c(2149584252)                  
a5(x15)             0xffffffff80be5000(18446744071574540288)        0xffffffff80be5000(18446744071574540288)        
a6(x16)             0x000000007fffff75(2147483509)                  0x000000007fffff75(2147483509)                  
a7(x17)             0x00000000000000c0(192)                         0x00000000000000c0(192)                         
s2(x18)             0x000000007f41af22(2135011106)                  0x000000007f41af22(2135011106)                  
s3(x19)             0x0000000000000297(663)                         0x0000000000000297(663)                         
s4(x20)             0x0000000080280468(2150106216)                  0x0000000080280468(2150106216)                  
s5(x21)             0x00000000800002a2(2147484322)                  0x00000000800002a2(2147484322)                  
s6(x22)             0x000000001994e748(429188936)                   0x000000001994e748(429188936)                   
s7(x23)             0x00000000800000dd(2147483869)                  0x00000000800000dd(2147483869)                  
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s10(x26)            0x00000000801ffc5b(2149579867)                  0x00000000801ffc5b(2149579867)                  
s11(x27)            0x000000008017fe78(2149056120)                  0x000000008017fe78(2149056120)                  
t3(x28)             0x0000000080180443(2149057603)                  0x0000000080180443(2149057603)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x0000000080180443(2149057603)                  0x0000000080180443(2149057603)                  
t6(x31)             0x0000000000000011(17)                          0x0000000000000011(17)                          

STATE               REF                                             DUT                                             DIFF
xmemhash            8d9507b17f21cf10bf720b6cc26662c2513081d9        8d9507b17f21cf10bf720b6cc26662c2513081d9        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        5871a0e2b5463641eb5587b9e29814822e3a2ec9        X
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000010(16)                          0x0000000000000010(16)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0xffffffff0051bc23(7.506165926734564e-39_s)     0xffffffff0051bc23(7.506165926734564e-39_s)     
f2                  0xffffffff43110000(145.0_s)                     0xffffffff43110000(145.0_s)                     
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0xfffffffffffffea0(nan_h)                       0xfffffffffffffea0(nan_h)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xc1e0030003200000(-2149056537.0_d)             0xc1e0030003200000(-2149056537.0_d)             
f15                 0xc1e0030003200000(-2149056537.0_d)             0xc1e0030003200000(-2149056537.0_d)             
f16                 0xffffffff43550000(213.0_s)                     0xffffffff43550000(213.0_s)                     
f17                 0x00000000801801c0(1.061775215e-314_d)          0x00000000801801c0(1.061775215e-314_d)          
f18                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f19                 0xffffffff4effffff(2147483520.0_s)              0xffffffff4effffff(2147483520.0_s)              
f20                 0xffffffff4effffff(2147483520.0_s)              0xffffffff4effffff(2147483520.0_s)              
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f24                 0x41e003dea2000000(2149512464.0_d)              0x41e003dea2000000(2149512464.0_d)              
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

# FailID_001408 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1408
* Isolated failing instruction: `flw`
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
_reg_f0: .byte 0xb4,0xd0,0xa5,0xba,0xfa,0x00,0xfd,0xb3
_reg_f1: .byte 0x1c,0x01,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f2: .byte 0xad,0x01,0xc4,0x3c,0x92,0x90,0x3f,0xa4
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x80,0xb0,0xfe,0xff,0xdf,0x41
_reg_f6: .byte 0x00,0x00,0x40,0x13,0xff,0xff,0xdf,0x41
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0xd7,0xc9,0xb6,0x57,0xe4,0x7d,0xf9,0x4c
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x6b,0x25,0xda,0x9f,0x8b,0xfb,0xec,0x35
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x23,0xb0,0x61,0x06,0xff,0xff,0xff,0xff
_reg_f13:.byte 0xff,0x10,0xae,0x23,0x80,0x14,0x7c,0xde
_reg_f14:.byte 0x00,0x00,0xc0,0x30,0x01,0xfa,0xdf,0xc1
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xd3,0xff,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0xff,0x10,0xae,0x23,0x80,0x14,0x7c,0xde
_reg_f20:.byte 0x00,0x00,0x00,0xac,0xbb,0x34,0xcd,0x41
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x40,0x39,0xff,0xff,0xdf,0xc1
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x40,0xac,0x90,0x41
_reg_f26:.byte 0xf7,0x7d,0x2f,0x4f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0xe9,0x41,0xb9,0x5e,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x78,0x2a,0xdc,0x41
_reg_f29:.byte 0x23,0xb0,0x61,0x06,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x1c,0x01,0x18,0x80,0x00,0x00,0x00,0x00
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
    li x1, 0x100300605           // ra
    li x2, 0x432                 // sp
    li x3, 0x8000038e            // gp
    li x4, 0x8018002a            // tp
    li x5, 0x801802fe            // t0
    li x6, 0xfffffffffffffe0c    // t1
    li x7, 0x8027fdaa            // t2
    li x8, 0x8017fd6b            // fp
    li x9, 0x400c0               // s1
    li x10, 0x1e                 // a0
    li x11, 0x1                  // a1
    li x12, 0x801ff60a           // a2
    li x13, 0x801802db           // a3
    li x14, 0x6000               // a4
    li x15, 0xeb                 // a5
    li x16, 0x801803a2           // a6
    li x17, 0x8018029a           // a7
    li x18, 0x0                  // s2
    li x19, 0x5e                 // s3
    li x20, 0x3e35c000           // s4
    li x21, 0x800002c7           // s5
    li x22, 0x801ffc36           // s6
    li x23, 0x0                  // s7
    li x24, 0x7ffffb9d           // s8
    li x25, 0x8017f8ae           // s9
    li x26, 0x80180314           // s10
    li x27, 0x8018017e           // s11
    li x28, 0x801ff6a0           // t3
    li x29, 0x0                  // t4
    li x30, 0x0                  // t5
    li x31, 0x801f079a           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x18'}, 'clob': {'x18', 'x25', 'f30'}})
    
    li x25, 0x1ffffc
    and x18, x18, x25
    li x25, 0x8000022a
    add x18, x18, x25
    flw f30, -0x22a(x18)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f30                 0x000000008018011c(1.061775134e-314_d)          0xffffffff2140006f(6.505270420568022e-19_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f30, -0x22a(x18)
+========================================================================================================================+
Attributes:  fcsr ['underflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f30                 0x000000008018011c(1.061775134e-314_d)          0xffffffff2140006f(6.505270420568022e-19_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f30, x22, x18
s2(x18)             0x000000008000022a(2147484202)                  0x000000008000022a(2147484202)
s6(x22)             0x00000000801ffc36(2149579830)                  0x00000000801ffc36(2149579830)
f30                 0x000000008018011c(1.061775134e-314_d)          0xffffffff2140006f(6.505270420568022e-19_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000100300605(4298114565)                  0x0000000100300605(4298114565)                  
sp(x2)              0x0000000000000432(1074)                        0x0000000000000432(1074)                        
gp(x3)              0x000000008000038e(2147484558)                  0x000000008000038e(2147484558)                  
tp(x4)              0x000000008018002a(2149056554)                  0x000000008018002a(2149056554)                  
t0(x5)              0x00000000801802fe(2149057278)                  0x00000000801802fe(2149057278)                  
t1(x6)              0xfffffffffffffe0c(18446744073709551116)        0xfffffffffffffe0c(18446744073709551116)        
t2(x7)              0x000000008027fdaa(2150104490)                  0x000000008027fdaa(2150104490)                  
fp(x8)              0x000000008017fd6b(2149055851)                  0x000000008017fd6b(2149055851)                  
s1(x9)              0x00000000000400c0(262336)                      0x00000000000400c0(262336)                      
a0(x10)             0x000000000000001e(30)                          0x000000000000001e(30)                          
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x00000000801ff60a(2149578250)                  0x00000000801ff60a(2149578250)                  
a3(x13)             0x00000000801802db(2149057243)                  0x00000000801802db(2149057243)                  
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x00000000000000eb(235)                         0x00000000000000eb(235)                         
a6(x16)             0x00000000801803a2(2149057442)                  0x00000000801803a2(2149057442)                  
a7(x17)             0x000000008018029a(2149057178)                  0x000000008018029a(2149057178)                  
s2(x18)             0x000000008000022a(2147484202)                  0x000000008000022a(2147484202)                  
s3(x19)             0x000000000000005e(94)                          0x000000000000005e(94)                          
s4(x20)             0x000000003e35c000(1043709952)                  0x000000003e35c000(1043709952)                  
s5(x21)             0x00000000800002c7(2147484359)                  0x00000000800002c7(2147484359)                  
s6(x22)             0x00000000801ffc36(2149579830)                  0x00000000801ffc36(2149579830)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x000000007ffffb9d(2147482525)                  0x000000007ffffb9d(2147482525)                  
s9(x25)             0x000000008000022a(2147484202)                  0x000000008000022a(2147484202)                  
s10(x26)            0x0000000080180314(2149057300)                  0x0000000080180314(2149057300)                  
s11(x27)            0x000000008018017e(2149056894)                  0x000000008018017e(2149056894)                  
t3(x28)             0x00000000801ff6a0(2149578400)                  0x00000000801ff6a0(2149578400)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x00000000801f079a(2149517210)                  0x00000000801f079a(2149517210)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            5f5111d4ffaa35eb5a84fbc4b2657f687674ff44        5f5111d4ffaa35eb5a84fbc4b2657f687674ff44        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000075c(2147485532)                  0x000000008000075c(2147485532)                  
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
f0                  0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    
f1                  0x000000008018011c(1.061775134e-314_d)          0x000000008018011c(1.061775134e-314_d)          
f2                  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x41dffffeb0800000(2147482306.0_d)              0x41dffffeb0800000(2147482306.0_d)              
f6                  0x41dfffff13400000(2147482701.0_d)              0x41dfffff13400000(2147482701.0_d)              
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x4cf97de457b6c9d7(6.554190042954392e+62_d)     0x4cf97de457b6c9d7(6.554190042954392e+62_d)     
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x35ecfb8b9fda256b(6.197093478488027e-49_d)     0x35ecfb8b9fda256b(6.197093478488027e-49_d)     
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff0661b023(4.2447201453266725e-35_s)    0xffffffff0661b023(4.2447201453266725e-35_s)    
f13                 0xde7c148023ae10ff(-1.4025431970955475e+147_d)  0xde7c148023ae10ff(-1.4025431970955475e+147_d)  
f14                 0xc1dffa0130c00000(-2145912003.0_d)             0xc1dffa0130c00000(-2145912003.0_d)             
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff8017ffd3(-2.2039888493608945e-39_s)   0xffffffff8017ffd3(-2.2039888493608945e-39_s)   
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xde7c148023ae10ff(-1.4025431970955475e+147_d)  0xde7c148023ae10ff(-1.4025431970955475e+147_d)  
f20                 0x41cd34bbac000000(979990360.0_d)               0x41cd34bbac000000(979990360.0_d)               
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0xc1dfffff39400000(-2147482853.0_d)             0xc1dfffff39400000(-2147482853.0_d)             
f25                 0x4190ac4000000000(69931008.0_d)                0x4190ac4000000000(69931008.0_d)                
f26                 0xffffffff4f2f7df7(2944268032.0_s)              0xffffffff4f2f7df7(2944268032.0_s)              
f27                 0xffffffff5eb941e9(6.674603478356066e+18_s)     0xffffffff5eb941e9(6.674603478356066e+18_s)     
f28                 0x41dc2a7800000000(1890181120.0_d)              0x41dc2a7800000000(1890181120.0_d)              
f29                 0xffffffff0661b023(4.2447201453266725e-35_s)    0xffffffff0661b023(4.2447201453266725e-35_s)    
f30                 0x000000008018011c(1.061775134e-314_d)          0xffffffff2140006f(6.505270420568022e-19_s)     X
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

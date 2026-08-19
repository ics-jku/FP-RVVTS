# FailID_002459 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2459
* Isolated failing instruction: `fsw`
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x8d,0xf9,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f28:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x81
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xc00                 // ra
    li x2, 0x801ff250            // sp
    li x3, 0xffffffffffffffff    // gp
    li x4, 0x1867788             // tp
    li x5, 0x801ff7f6            // t0
    li x6, 0x78710000            // t1
    li x7, 0x6000                // t2
    li x8, 0x269a0728            // fp
    li x9, 0x8018671d            // s1
    li x10, 0x7ffffeec           // a0
    li x11, 0x7ffffb16           // a1
    li x12, 0x801c1187           // a2
    li x13, 0x6000               // a3
    li x14, 0x60000000000        // a4
    li x15, 0x8017f9d7           // a5
    li x16, 0x10                 // a6
    li x17, 0x96                 // a7
    li x18, 0x8017fe7f           // s2
    li x19, 0x100300976000       // s3
    li x20, 0x1                  // s4
    li x21, 0x80180333           // s5
    li x22, 0xc77271c            // s6
    li x23, 0x0                  // s7
    li x24, 0x4a1db000           // s8
    li x25, 0x1867eeb            // s9
    li x26, 0x80200173           // s10
    li x27, 0x7ffff976           // s11
    li x28, 0x6000               // t3
    li x29, 0x0                  // t4
    li x30, 0x70                 // t5
    li x31, 0x8017fc40           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x6', 'f16'}, 'clob': {'x18', 'x6'}})
    
    li x18, 0xffffc
    and x6, x6, x18
    li x18, 0x8017ffc5
    add x6, x6, x18
    fsw f16, 0x3b(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ab17dedbe2648c47f52e9cdbd82c52c29fbc994a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f16, 0x3b(x6)
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ab17dedbe2648c47f52e9cdbd82c52c29fbc994a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f16, x3, x6
gp(x3)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)
t1(x6)              0x000000008018ffc5(2149121989)                  0x000000008018ffc5(2149121989)
f16                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000c00(3072)                        0x0000000000000c00(3072)                        
sp(x2)              0x00000000801ff250(2149577296)                  0x00000000801ff250(2149577296)                  
gp(x3)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
tp(x4)              0x0000000001867788(25589640)                    0x0000000001867788(25589640)                    
t0(x5)              0x00000000801ff7f6(2149578742)                  0x00000000801ff7f6(2149578742)                  
t1(x6)              0x000000008018ffc5(2149121989)                  0x000000008018ffc5(2149121989)                  
t2(x7)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
fp(x8)              0x00000000269a0728(647628584)                   0x00000000269a0728(647628584)                   
s1(x9)              0x000000008018671d(2149082909)                  0x000000008018671d(2149082909)                  
a0(x10)             0x000000007ffffeec(2147483372)                  0x000000007ffffeec(2147483372)                  
a1(x11)             0x000000007ffffb16(2147482390)                  0x000000007ffffb16(2147482390)                  
a2(x12)             0x00000000801c1187(2149323143)                  0x00000000801c1187(2149323143)                  
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x0000060000000000(6597069766656)               0x0000060000000000(6597069766656)               
a5(x15)             0x000000008017f9d7(2149054935)                  0x000000008017f9d7(2149054935)                  
a6(x16)             0x0000000000000010(16)                          0x0000000000000010(16)                          
a7(x17)             0x0000000000000096(150)                         0x0000000000000096(150)                         
s2(x18)             0x000000008017ffc5(2149056453)                  0x000000008017ffc5(2149056453)                  
s3(x19)             0x0000100300976000(17605080866816)              0x0000100300976000(17605080866816)              
s4(x20)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s5(x21)             0x0000000080180333(2149057331)                  0x0000000080180333(2149057331)                  
s6(x22)             0x000000000c77271c(209135388)                   0x000000000c77271c(209135388)                   
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x000000004a1db000(1243459584)                  0x000000004a1db000(1243459584)                  
s9(x25)             0x0000000001867eeb(25591531)                    0x0000000001867eeb(25591531)                    
s10(x26)            0x0000000080200173(2149581171)                  0x0000000080200173(2149581171)                  
s11(x27)            0x000000007ffff976(2147481974)                  0x000000007ffff976(2147481974)                  
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x0000000000000070(112)                         0x0000000000000070(112)                         
t6(x31)             0x000000008017fc40(2149055552)                  0x000000008017fc40(2149055552)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            5d89df350a093e1156cc46b67d3cf1e9c42e518d        5d89df350a093e1156cc46b67d3cf1e9c42e518d        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        ab17dedbe2648c47f52e9cdbd82c52c29fbc994a        X
lastPC              0x0000000080000734(2147485492)                  0x0000000080000734(2147485492)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000081(129)                         0x0000000000000081(129)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff7ffff98d(nan_s)                       0xffffffff7ffff98d(nan_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f28                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

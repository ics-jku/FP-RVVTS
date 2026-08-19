# FailID_001062 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1062
* Isolated failing instruction: `fld`
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
_reg_f1: .byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0xfd,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xf0,0xe0,0xc2,0x41
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0xfc,0xff,0xff,0xce,0xff,0xff,0xff,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xfc,0xff,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x83,0xb2,0x01,0x00,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xe0,0xaf,0xff,0x03,0xe0,0x41
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x24,0xfb,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x64
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8000018a            // ra
    li x2, 0x34                  // sp
    li x3, 0xffffffffffffffdb    // gp
    li x4, 0x8018008d            // tp
    li x5, 0x80185f51            // t0
    li x6, 0x7fffff03            // t1
    li x7, 0x8027f768            // t2
    li x8, 0x8017fa44            // fp
    li x9, 0x185d03              // s1
    li x10, 0x8017f84f           // a0
    li x11, 0x1002ff1b2000000    // a1
    li x12, 0x9caaa72c           // a2
    li x13, 0x8017fd58           // a3
    li x14, 0x6000               // a4
    li x15, 0x801ff9e0           // a5
    li x16, 0x8017fb7e           // a6
    li x17, 0x7ffff8fe           // a7
    li x18, 0x7fffffc3           // s2
    li x19, 0x0                  // s3
    li x20, 0x7ffffc37           // s4
    li x21, 0x802197d5           // s5
    li x22, 0x1                  // s6
    li x23, 0x0                  // s7
    li x24, 0x8027f1bb           // s8
    li x25, 0xffff               // s9
    li x26, 0x3fffff81           // s10
    li x27, 0x800002ae           // s11
    li x28, 0x584                // t3
    li x29, 0x7ffffd1f           // t4
    li x30, 0x200                // t5
    li x31, 0x7ffffa37           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x27'}, 'clob': {'x25', 'x27', 'f18'}})
    
    li x25, 0x1ffff8
    and x27, x27, x25
    li x25, 0x800006f4
    add x27, x27, x25
    fld f18, -0x6f4(x27)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f18                 0x7ff8000000000000(nan_d)                       0xd2000ad3d2000a53(-9.972757350740306e+86_d)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f18, -0x6f4(x27)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f18                 0x7ff8000000000000(nan_d)                       0xd2000ad3d2000a53(-9.972757350740306e+86_d)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f18, x6, f4, x27
t1(x6)              0x000000007fffff03(2147483395)                  0x000000007fffff03(2147483395)
s11(x27)            0x000000008000099c(2147486108)                  0x000000008000099c(2147486108)
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
f18                 0x7ff8000000000000(nan_d)                       0xd2000ad3d2000a53(-9.972757350740306e+86_d)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008000018a(2147484042)                  0x000000008000018a(2147484042)                  
sp(x2)              0x0000000000000034(52)                          0x0000000000000034(52)                          
gp(x3)              0xffffffffffffffdb(18446744073709551579)        0xffffffffffffffdb(18446744073709551579)        
tp(x4)              0x000000008018008d(2149056653)                  0x000000008018008d(2149056653)                  
t0(x5)              0x0000000080185f51(2149080913)                  0x0000000080185f51(2149080913)                  
t1(x6)              0x000000007fffff03(2147483395)                  0x000000007fffff03(2147483395)                  
t2(x7)              0x000000008027f768(2150102888)                  0x000000008027f768(2150102888)                  
fp(x8)              0x000000008017fa44(2149055044)                  0x000000008017fa44(2149055044)                  
s1(x9)              0x0000000000185d03(1596675)                     0x0000000000185d03(1596675)                     
a0(x10)             0x000000008017f84f(2149054543)                  0x000000008017f84f(2149054543)                  
a1(x11)             0x01002ff1b2000000(72110309157896192)           0x01002ff1b2000000(72110309157896192)           
a2(x12)             0x000000009caaa72c(2628429612)                  0x000000009caaa72c(2628429612)                  
a3(x13)             0x000000008017fd58(2149055832)                  0x000000008017fd58(2149055832)                  
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x00000000801ff9e0(2149579232)                  0x00000000801ff9e0(2149579232)                  
a6(x16)             0x000000008017fb7e(2149055358)                  0x000000008017fb7e(2149055358)                  
a7(x17)             0x000000007ffff8fe(2147481854)                  0x000000007ffff8fe(2147481854)                  
s2(x18)             0x000000007fffffc3(2147483587)                  0x000000007fffffc3(2147483587)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000007ffffc37(2147482679)                  0x000000007ffffc37(2147482679)                  
s5(x21)             0x00000000802197d5(2149685205)                  0x00000000802197d5(2149685205)                  
s6(x22)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x000000008027f1bb(2150101435)                  0x000000008027f1bb(2150101435)                  
s9(x25)             0x00000000800006f4(2147485428)                  0x00000000800006f4(2147485428)                  
s10(x26)            0x000000003fffff81(1073741697)                  0x000000003fffff81(1073741697)                  
s11(x27)            0x000000008000099c(2147486108)                  0x000000008000099c(2147486108)                  
t3(x28)             0x0000000000000584(1412)                        0x0000000000000584(1412)                        
t4(x29)             0x000000007ffffd1f(2147482911)                  0x000000007ffffd1f(2147482911)                  
t5(x30)             0x0000000000000200(512)                         0x0000000000000200(512)                         
t6(x31)             0x000000007ffffa37(2147482167)                  0x000000007ffffa37(2147482167)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            1266781fec0012a7b034e15ee0259a46220c33ad        1266781fec0012a7b034e15ee0259a46220c33ad        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000758(2147485528)                  0x0000000080000758(2147485528)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000064(100)                         0x0000000000000064(100)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff4f0017fd(2149055744.0_s)              0xffffffff4f0017fd(2149055744.0_s)              
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff4f0017fd(2149055744.0_s)              0xffffffff4f0017fd(2149055744.0_s)              
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x41c2e0f000000000(633462784.0_d)               0x41c2e0f000000000(633462784.0_d)               
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7fffffffcefffffc(nan_d)                       0x7fffffffcefffffc(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffffcefffffc(-2147483136.0_s)             0xffffffffcefffffc(-2147483136.0_s)             
f13                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f14                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f15                 0xffffffff0001b283(1.5587343467917103e-40_s)    0xffffffff0001b283(1.5587343467917103e-40_s)    
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0xd2000ad3d2000a53(-9.972757350740306e+86_d)    X
f19                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x41e003ffafe00000(2149580159.0_d)              0x41e003ffafe00000(2149580159.0_d)              
f28                 0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff8017fb24(-2.202308692502169e-39_s)    0xffffffff8017fb24(-2.202308692502169e-39_s)    
f31                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
STATES DIFFER: True
```

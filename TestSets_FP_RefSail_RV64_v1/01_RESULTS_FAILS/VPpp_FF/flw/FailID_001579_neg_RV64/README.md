# FailID_001579 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1579
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xe0,0x31,0x00,0x00,0xe0,0x41
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x93,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0xfa,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x4
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017feb0            // ra
    li x2, 0x6000                // sp
    li x3, 0x80200060            // gp
    li x4, 0x8017ff5f            // tp
    li x5, 0x0                   // t0
    li x6, 0x0                   // t1
    li x7, 0x200                 // t2
    li x8, 0x80059f22            // fp
    li x9, 0x800001af            // s1
    li x10, 0x8017fdee           // a0
    li x11, 0x6000               // a1
    li x12, 0x8017f8d4           // a2
    li x13, 0x56                 // a3
    li x14, 0x80000185           // a4
    li x15, 0x8017fba3           // a5
    li x16, 0x80260188           // a6
    li x17, 0x801a0602           // a7
    li x18, 0xa4                 // s2
    li x19, 0x0                  // s3
    li x20, 0x801ffc8b           // s4
    li x21, 0x7ffff887           // s5
    li x22, 0x801800ee           // s6
    li x23, 0x80200661           // s7
    li x24, 0x7ffff99c           // s8
    li x25, 0x801851af           // s9
    li x26, 0x0                  // s10
    li x27, 0x7ffff8ab           // s11
    li x28, 0x0                  // t3
    li x29, 0x0                  // t4
    li x30, 0xffff               // t5
    li x31, 0x1                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x23'}, 'clob': {'f12', 'x6', 'x23'}})
    
    li x6, 0x1ffffc
    and x23, x23, x6
    li x6, 0x800002a3
    add x23, x23, x6
    flw f12, -0x2a3(x23)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f12                 0x7ff8000000000000(nan_d)                       0xffffffffdee50513(-8.251308650144989e+18_s)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f12, -0x2a3(x23)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f12                 0x7ff8000000000000(nan_d)                       0xffffffffdee50513(-8.251308650144989e+18_s)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f12, x2, a3, x23
sp(x2)              0x0000000000006000(24576)                       0x0000000000006000(24576)
s7(x23)             0x0000000080000903(2147485955)                  0x0000000080000903(2147485955)
f12                 0x7ff8000000000000(nan_d)                       0xffffffffdee50513(-8.251308650144989e+18_s)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017feb0(2149056176)                  0x000000008017feb0(2149056176)                  
sp(x2)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
gp(x3)              0x0000000080200060(2149580896)                  0x0000000080200060(2149580896)                  
tp(x4)              0x000000008017ff5f(2149056351)                  0x000000008017ff5f(2149056351)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x00000000800002a3(2147484323)                  0x00000000800002a3(2147484323)                  
t2(x7)              0x0000000000000200(512)                         0x0000000000000200(512)                         
fp(x8)              0x0000000080059f22(2147852066)                  0x0000000080059f22(2147852066)                  
s1(x9)              0x00000000800001af(2147484079)                  0x00000000800001af(2147484079)                  
a0(x10)             0x000000008017fdee(2149055982)                  0x000000008017fdee(2149055982)                  
a1(x11)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a2(x12)             0x000000008017f8d4(2149054676)                  0x000000008017f8d4(2149054676)                  
a3(x13)             0x0000000000000056(86)                          0x0000000000000056(86)                          
a4(x14)             0x0000000080000185(2147484037)                  0x0000000080000185(2147484037)                  
a5(x15)             0x000000008017fba3(2149055395)                  0x000000008017fba3(2149055395)                  
a6(x16)             0x0000000080260188(2149974408)                  0x0000000080260188(2149974408)                  
a7(x17)             0x00000000801a0602(2149189122)                  0x00000000801a0602(2149189122)                  
s2(x18)             0x00000000000000a4(164)                         0x00000000000000a4(164)                         
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x00000000801ffc8b(2149579915)                  0x00000000801ffc8b(2149579915)                  
s5(x21)             0x000000007ffff887(2147481735)                  0x000000007ffff887(2147481735)                  
s6(x22)             0x00000000801800ee(2149056750)                  0x00000000801800ee(2149056750)                  
s7(x23)             0x0000000080000903(2147485955)                  0x0000000080000903(2147485955)                  
s8(x24)             0x000000007ffff99c(2147482012)                  0x000000007ffff99c(2147482012)                  
s9(x25)             0x00000000801851af(2149077423)                  0x00000000801851af(2149077423)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000007ffff8ab(2147481771)                  0x000000007ffff8ab(2147481771)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x000000000000ffff(65535)                       0x000000000000ffff(65535)                       
t6(x31)             0x0000000000000001(1)                           0x0000000000000001(1)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            5ec4ef5a0aeb728aa519ed383393ee8c63e62218        5ec4ef5a0aeb728aa519ed383393ee8c63e62218        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000744(2147485508)                  0x0000000080000744(2147485508)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000004(4)                           0x0000000000000004(4)                           
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x41e0000031e00000(2147484047.0_d)              0x41e0000031e00000(2147484047.0_d)              
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff00000293(9.234556879900544e-43_s)     0xffffffff00000293(9.234556879900544e-43_s)     
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff4efffffa(2147482880.0_s)              0xffffffff4efffffa(2147482880.0_s)              
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0xffffffffdee50513(-8.251308650144989e+18_s)    X
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f20                 0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x7ffffffffffffe00(nan_d)                       0x7ffffffffffffe00(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ffffffffffffe00(nan_d)                       0x7ffffffffffffe00(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

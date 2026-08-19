# FailID_004022 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4022
* Isolated failing instruction: `flw`
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
_reg_f1: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0xf0,0xe1,0xd1,0xc1
_reg_f4: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xdf,0x41
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0xcd,0xb4,0xfb,0xad,0xbd,0xa2,0xe6,0x40
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0xc4,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x20,0x74,0x00,0x03,0xe0,0x41
_reg_f20:.byte 0x00,0x00,0xda,0x42,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x03,0xfb,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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
    li x1, 0x8027f5dd            // ra
    li x2, 0x6d                  // sp
    li x3, 0x0                   // gp
    li x4, 0x80180395            // tp
    li x5, 0x8000069a            // t0
    li x6, 0x8017fa66            // t1
    li x7, 0x0                   // t2
    li x8, 0xfffffffffffffc2f    // fp
    li x9, 0x8018007e            // s1
    li x10, 0x73                 // a0
    li x11, 0x8018607e           // a1
    li x12, 0x801802b6           // a2
    li x13, 0x188                // a3
    li x14, 0x1                  // a4
    li x15, 0x8017f876           // a5
    li x16, 0x80180446           // a6
    li x17, 0x80185fc2           // a7
    li x18, 0x801ff79b           // s2
    li x19, 0x801802b6           // s3
    li x20, 0x7fffff28           // s4
    li x21, 0x2798775c           // s5
    li x22, 0x80180446           // s6
    li x23, 0x7ffffdd1           // s7
    li x24, 0x801804e6           // s8
    li x25, 0x801802b6           // s9
    li x26, 0xffffffff7fc00000   // s10
    li x27, 0x802802f5           // s11
    li x28, 0x6000               // t3
    li x29, 0x64                 // t4
    li x30, 0x800d591d           // t5
    li x31, 0x2ffe750            // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x24', 'fcsr.rm'}, 'clob': {'x24', 'x3', 'f1'}})
    
    li x3, 0x1ffffc
    and x24, x24, x3
    li x3, 0x7ffff874
    add x24, x24, x3
    flw f1, 0x78c(x24)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f1                  0xffffffffffc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f1, 0x78c(x24)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f1                  0xffffffffffc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f1, x78, x24
s8(x24)             0x000000008017fd58(2149055832)                  0x000000008017fd58(2149055832)
f1                  0xffffffffffc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008027f5dd(2150102493)                  0x000000008027f5dd(2150102493)                  
sp(x2)              0x000000000000006d(109)                         0x000000000000006d(109)                         
gp(x3)              0x000000007ffff874(2147481716)                  0x000000007ffff874(2147481716)                  
tp(x4)              0x0000000080180395(2149057429)                  0x0000000080180395(2149057429)                  
t0(x5)              0x000000008000069a(2147485338)                  0x000000008000069a(2147485338)                  
t1(x6)              0x000000008017fa66(2149055078)                  0x000000008017fa66(2149055078)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0xfffffffffffffc2f(18446744073709550639)        0xfffffffffffffc2f(18446744073709550639)        
s1(x9)              0x000000008018007e(2149056638)                  0x000000008018007e(2149056638)                  
a0(x10)             0x0000000000000073(115)                         0x0000000000000073(115)                         
a1(x11)             0x000000008018607e(2149081214)                  0x000000008018607e(2149081214)                  
a2(x12)             0x00000000801802b6(2149057206)                  0x00000000801802b6(2149057206)                  
a3(x13)             0x0000000000000188(392)                         0x0000000000000188(392)                         
a4(x14)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a5(x15)             0x000000008017f876(2149054582)                  0x000000008017f876(2149054582)                  
a6(x16)             0x0000000080180446(2149057606)                  0x0000000080180446(2149057606)                  
a7(x17)             0x0000000080185fc2(2149081026)                  0x0000000080185fc2(2149081026)                  
s2(x18)             0x00000000801ff79b(2149578651)                  0x00000000801ff79b(2149578651)                  
s3(x19)             0x00000000801802b6(2149057206)                  0x00000000801802b6(2149057206)                  
s4(x20)             0x000000007fffff28(2147483432)                  0x000000007fffff28(2147483432)                  
s5(x21)             0x000000002798775c(664303452)                   0x000000002798775c(664303452)                   
s6(x22)             0x0000000080180446(2149057606)                  0x0000000080180446(2149057606)                  
s7(x23)             0x000000007ffffdd1(2147483089)                  0x000000007ffffdd1(2147483089)                  
s8(x24)             0x000000008017fd58(2149055832)                  0x000000008017fd58(2149055832)                  
s9(x25)             0x00000000801802b6(2149057206)                  0x00000000801802b6(2149057206)                  
s10(x26)            0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
s11(x27)            0x00000000802802f5(2150105845)                  0x00000000802802f5(2150105845)                  
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x0000000000000064(100)                         0x0000000000000064(100)                         
t5(x30)             0x00000000800d591d(2148358429)                  0x00000000800d591d(2148358429)                  
t6(x31)             0x0000000002ffe750(50325328)                    0x0000000002ffe750(50325328)                    

STATE               REF                                             DUT                                             DIFF
xmemhash            235566ea83c54c53102ad2bf1c973a560d513610        235566ea83c54c53102ad2bf1c973a560d513610        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000076c(2147485548)                  0x000000008000076c(2147485548)                  
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
f1                  0xffffffffffc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xc1d1e1f000000000(-1200078848.0_d)             0xc1d1e1f000000000(-1200078848.0_d)             
f4                  0x41dfffffffc00000(2147483647.0_d)              0x41dfffffffc00000(2147483647.0_d)              
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x40e6a2bdadfbb4cd(46357.92748818696_d)         0x40e6a2bdadfbb4cd(46357.92748818696_d)         
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffffc4000000(-512.0_s)                    0xffffffffc4000000(-512.0_s)                    
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x41e0030074200000(2149057441.0_d)              0x41e0030074200000(2149057441.0_d)              
f20                 0xffffffff42da0000(109.0_s)                     0xffffffff42da0000(109.0_s)                     
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7ffffb03(nan_s)                       0xffffffff7ffffb03(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
STATES DIFFER: True
```

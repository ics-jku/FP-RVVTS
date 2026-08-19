# FailID_004695 VP++ SF neg RV64 fsh

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4695
* Isolated failing instruction: `fsh`
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
_reg_f9: .byte 0xcd,0xb4,0xfb,0xad,0xbd,0xa2,0xe6,0x40
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
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x03,0xfb,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x84
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8027f5dd            // ra
    li x2, 0x80000505            // sp
    li x3, 0xe3                  // gp
    li x4, 0x80180395            // tp
    li x5, 0x80180388            // t0
    li x6, 0x801ff672            // t1
    li x7, 0x0                   // t2
    li x8, 0xffff9be6            // fp
    li x9, 0x5e                  // s1
    li x10, 0x7ffffa6f           // a0
    li x11, 0x7fffff7d           // a1
    li x12, 0x1                  // a2
    li x13, 0x188                // a3
    li x14, 0x1                  // a4
    li x15, 0x8017f876           // a5
    li x16, 0xffffffffffffffff   // a6
    li x17, 0x8000655d           // a7
    li x18, 0x7ffffa0c           // s2
    li x19, 0x0                  // s3
    li x20, 0x7fffff28           // s4
    li x21, 0x8017fe91           // s5
    li x22, 0x800007bc           // s6
    li x23, 0x7ffffdd1           // s7
    li x24, 0x801ff605           // s8
    li x25, 0x0                  // s9
    li x26, 0x6e                 // s10
    li x27, 0x802802f5           // s11
    li x28, 0xffff               // t3
    li x29, 0x6000               // t4
    li x30, 0x800d591d           // t5
    li x31, 0xc1                 // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'f21', 'fcsr.rm', 'x3'}, 'clob': {'x31', 'x3'}})
    
    li x31, 0xffffe
    and x3, x3, x31
    li x31, 0x801803f6
    add x3, x3, x31
    fsh f21, -0x3f6(x3)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        80d56436cbd0e73b8f6489a4505a30b9569121e9        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsh f21, -0x3f6(x3)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        80d56436cbd0e73b8f6489a4505a30b9569121e9        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f21, x3, f6, x3
gp(x3)              0x00000000801804d8(2149057752)                  0x00000000801804d8(2149057752)
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
f21                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008027f5dd(2150102493)                  0x000000008027f5dd(2150102493)                  
sp(x2)              0x0000000080000505(2147484933)                  0x0000000080000505(2147484933)                  
gp(x3)              0x00000000801804d8(2149057752)                  0x00000000801804d8(2149057752)                  
tp(x4)              0x0000000080180395(2149057429)                  0x0000000080180395(2149057429)                  
t0(x5)              0x0000000080180388(2149057416)                  0x0000000080180388(2149057416)                  
t1(x6)              0x00000000801ff672(2149578354)                  0x00000000801ff672(2149578354)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x00000000ffff9be6(4294941670)                  0x00000000ffff9be6(4294941670)                  
s1(x9)              0x000000000000005e(94)                          0x000000000000005e(94)                          
a0(x10)             0x000000007ffffa6f(2147482223)                  0x000000007ffffa6f(2147482223)                  
a1(x11)             0x000000007fffff7d(2147483517)                  0x000000007fffff7d(2147483517)                  
a2(x12)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a3(x13)             0x0000000000000188(392)                         0x0000000000000188(392)                         
a4(x14)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a5(x15)             0x000000008017f876(2149054582)                  0x000000008017f876(2149054582)                  
a6(x16)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a7(x17)             0x000000008000655d(2147509597)                  0x000000008000655d(2147509597)                  
s2(x18)             0x000000007ffffa0c(2147482124)                  0x000000007ffffa0c(2147482124)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000007fffff28(2147483432)                  0x000000007fffff28(2147483432)                  
s5(x21)             0x000000008017fe91(2149056145)                  0x000000008017fe91(2149056145)                  
s6(x22)             0x00000000800007bc(2147485628)                  0x00000000800007bc(2147485628)                  
s7(x23)             0x000000007ffffdd1(2147483089)                  0x000000007ffffdd1(2147483089)                  
s8(x24)             0x00000000801ff605(2149578245)                  0x00000000801ff605(2149578245)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x000000000000006e(110)                         0x000000000000006e(110)                         
s11(x27)            0x00000000802802f5(2150105845)                  0x00000000802802f5(2150105845)                  
t3(x28)             0x000000000000ffff(65535)                       0x000000000000ffff(65535)                       
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x00000000800d591d(2148358429)                  0x00000000800d591d(2148358429)                  
t6(x31)             0x00000000801803f6(2149057526)                  0x00000000801803f6(2149057526)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            f138f5fa09f668cd6bd92ae4a7a9c584cbd83f03        f138f5fa09f668cd6bd92ae4a7a9c584cbd83f03        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        80d56436cbd0e73b8f6489a4505a30b9569121e9        X
lastPC              0x0000000080000744(2147485508)                  0x0000000080000744(2147485508)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000084(132)                         0x0000000000000084(132)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xc1d1e1f000000000(-1200078848.0_d)             0xc1d1e1f000000000(-1200078848.0_d)             
f4                  0x41dfffffffc00000(2147483647.0_d)              0x41dfffffffc00000(2147483647.0_d)              
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x40e6a2bdadfbb4cd(46357.92748818696_d)         0x40e6a2bdadfbb4cd(46357.92748818696_d)         
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
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
f22                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x7fffffff42140000(nan_d)                       0x7fffffff42140000(nan_d)                       
f25                 0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7ffffb03(nan_s)                       0xffffffff7ffffb03(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
STATES DIFFER: True
```

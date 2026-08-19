# FailID_002443 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2443
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
    li x2, 0xffffffffffffffff    // sp
    li x3, 0x0                   // gp
    li x4, 0x8e                  // tp
    li x5, 0x80180388            // t0
    li x6, 0x8017fdfd            // t1
    li x7, 0x0                   // t2
    li x8, 0xffff9be6            // fp
    li x9, 0x80180032            // s1
    li x10, 0x7ffffa6f           // a0
    li x11, 0x6d05d250           // a1
    li x12, 0x53                 // a2
    li x13, 0x7ffffc5a           // a3
    li x14, 0x0                  // a4
    li x15, 0x0                  // a5
    li x16, 0xffffffffffffffff   // a6
    li x17, 0x8000655d           // a7
    li x18, 0x8017fdfd           // s2
    li x19, 0x11c000             // s3
    li x20, 0x0                  // s4
    li x21, 0xffe7f9e7           // s5
    li x22, 0x800007bc           // s6
    li x23, 0xffffffffffffffff   // s7
    li x24, 0x7ffffd3c           // s8
    li x25, 0x0                  // s9
    li x26, 0x84                 // s10
    li x27, 0x7ffffed8           // s11
    li x28, 0xffff               // t3
    li x29, 0x54fb000            // t4
    li x30, 0x800d591d           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f24', 'x23'}, 'clob': {'x21', 'x23'}})
    
    li x21, 0xffffc
    and x23, x23, x21
    li x21, 0x801806b9
    add x23, x23, x21
    fsw f24, -0x6b9(x23)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        37723c9adb0ab2605e9558d2c0fa3ef424b668bc        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f24, -0x6b9(x23)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        37723c9adb0ab2605e9558d2c0fa3ef424b668bc        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f24, x6, b9, x23
t1(x6)              0x000000008017fdfd(2149055997)                  0x000000008017fdfd(2149055997)
s7(x23)             0x00000000802806b5(2150106805)                  0x00000000802806b5(2150106805)
f24                 0x7fffffff42140000(nan_d)                       0x7fffffff42140000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008027f5dd(2150102493)                  0x000000008027f5dd(2150102493)                  
sp(x2)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x000000000000008e(142)                         0x000000000000008e(142)                         
t0(x5)              0x0000000080180388(2149057416)                  0x0000000080180388(2149057416)                  
t1(x6)              0x000000008017fdfd(2149055997)                  0x000000008017fdfd(2149055997)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x00000000ffff9be6(4294941670)                  0x00000000ffff9be6(4294941670)                  
s1(x9)              0x0000000080180032(2149056562)                  0x0000000080180032(2149056562)                  
a0(x10)             0x000000007ffffa6f(2147482223)                  0x000000007ffffa6f(2147482223)                  
a1(x11)             0x000000006d05d250(1829098064)                  0x000000006d05d250(1829098064)                  
a2(x12)             0x0000000000000053(83)                          0x0000000000000053(83)                          
a3(x13)             0x000000007ffffc5a(2147482714)                  0x000000007ffffc5a(2147482714)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a7(x17)             0x000000008000655d(2147509597)                  0x000000008000655d(2147509597)                  
s2(x18)             0x000000008017fdfd(2149055997)                  0x000000008017fdfd(2149055997)                  
s3(x19)             0x000000000011c000(1163264)                     0x000000000011c000(1163264)                     
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x00000000801806b9(2149058233)                  0x00000000801806b9(2149058233)                  
s6(x22)             0x00000000800007bc(2147485628)                  0x00000000800007bc(2147485628)                  
s7(x23)             0x00000000802806b5(2150106805)                  0x00000000802806b5(2150106805)                  
s8(x24)             0x000000007ffffd3c(2147482940)                  0x000000007ffffd3c(2147482940)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000084(132)                         0x0000000000000084(132)                         
s11(x27)            0x000000007ffffed8(2147483352)                  0x000000007ffffed8(2147483352)                  
t3(x28)             0x000000000000ffff(65535)                       0x000000000000ffff(65535)                       
t4(x29)             0x00000000054fb000(89108480)                    0x00000000054fb000(89108480)                    
t5(x30)             0x00000000800d591d(2148358429)                  0x00000000800d591d(2148358429)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            cd274e87d3e44830eb0a1f1b076eb1d870fc662d        cd274e87d3e44830eb0a1f1b076eb1d870fc662d        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        37723c9adb0ab2605e9558d2c0fa3ef424b668bc        X
lastPC              0x0000000080000724(2147485476)                  0x0000000080000724(2147485476)                  
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

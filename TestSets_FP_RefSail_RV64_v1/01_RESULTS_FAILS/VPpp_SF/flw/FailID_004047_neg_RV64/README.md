# FailID_004047 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4047
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x1a,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x80,0x5f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x80,0x4f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x80,0x5f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f28:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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
    li x1, 0xffffffffda301000    // ra
    li x2, 0x53                  // sp
    li x3, 0xffffffffffffffff    // gp
    li x4, 0x0                   // tp
    li x5, 0x0                   // t0
    li x6, 0x7fffffffffffffff    // t1
    li x7, 0x8028020c            // t2
    li x8, 0x200                 // fp
    li x9, 0xffffffffffffffff    // s1
    li x10, 0x0                  // a0
    li x11, 0x3706c010           // a1
    li x12, 0xffffffff00000000   // a2
    li x13, 0xa1                 // a3
    li x14, 0x10                 // a4
    li x15, 0x0                  // a5
    li x16, 0x8017fb3a           // a6
    li x17, 0x8018011e           // a7
    li x18, 0x10                 // s2
    li x19, 0x0                  // s3
    li x20, 0xffffffffffff8000   // s4
    li x21, 0x0                  // s5
    li x22, 0x8017f93a           // s6
    li x23, 0x1002ff             // s7
    li x24, 0x8018049d           // s8
    li x25, 0x3706c000           // s9
    li x26, 0x6000               // s10
    li x27, 0x8018663f           // s11
    li x28, 0x7fffffff           // t3
    li x29, 0xffffffffffffffff   // t4
    li x30, 0xb0                 // t5
    li x31, 0x26200728           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x13'}, 'clob': {'x12', 'x13', 'f19'}})
    
    li x12, 0x1ffffc
    and x13, x13, x12
    li x12, 0x800001d3
    add x13, x13, x12
    flw f19, -0x1d3(x13)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff08c1b823(1.1659055311619432e-33_s)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f19, -0x1d3(x13)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff08c1b823(1.1659055311619432e-33_s)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f19, x1, d3, x13
ra(x1)              0xffffffffda301000(18446744073075167232)        0xffffffffda301000(18446744073075167232)
a3(x13)             0x0000000080000273(2147484275)                  0x0000000080000273(2147484275)
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff08c1b823(1.1659055311619432e-33_s)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xffffffffda301000(18446744073075167232)        0xffffffffda301000(18446744073075167232)        
sp(x2)              0x0000000000000053(83)                          0x0000000000000053(83)                          
gp(x3)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
t2(x7)              0x000000008028020c(2150105612)                  0x000000008028020c(2150105612)                  
fp(x8)              0x0000000000000200(512)                         0x0000000000000200(512)                         
s1(x9)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x000000003706c010(923189264)                   0x000000003706c010(923189264)                   
a2(x12)             0x00000000800001d3(2147484115)                  0x00000000800001d3(2147484115)                  
a3(x13)             0x0000000080000273(2147484275)                  0x0000000080000273(2147484275)                  
a4(x14)             0x0000000000000010(16)                          0x0000000000000010(16)                          
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x000000008017fb3a(2149055290)                  0x000000008017fb3a(2149055290)                  
a7(x17)             0x000000008018011e(2149056798)                  0x000000008018011e(2149056798)                  
s2(x18)             0x0000000000000010(16)                          0x0000000000000010(16)                          
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0xffffffffffff8000(18446744073709518848)        0xffffffffffff8000(18446744073709518848)        
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x000000008017f93a(2149054778)                  0x000000008017f93a(2149054778)                  
s7(x23)             0x00000000001002ff(1049343)                     0x00000000001002ff(1049343)                     
s8(x24)             0x000000008018049d(2149057693)                  0x000000008018049d(2149057693)                  
s9(x25)             0x000000003706c000(923189248)                   0x000000003706c000(923189248)                   
s10(x26)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s11(x27)            0x000000008018663f(2149082687)                  0x000000008018663f(2149082687)                  
t3(x28)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
t4(x29)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t5(x30)             0x00000000000000b0(176)                         0x00000000000000b0(176)                         
t6(x31)             0x0000000026200728(639633192)                   0x0000000026200728(639633192)                   

STATE               REF                                             DUT                                             DIFF
xmemhash            7d6a2afd41f42bdf6691fc08f8780bda885442bc        7d6a2afd41f42bdf6691fc08f8780bda885442bc        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800006f8(2147485432)                  0x00000000800006f8(2147485432)                  
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
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff0000001a(3.6433760072445244e-44_s)    0xffffffff0000001a(3.6433760072445244e-44_s)    
f3                  0xffffffff5f800000(1.8446744073709552e+19_s)    0xffffffff5f800000(1.8446744073709552e+19_s)    
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff4f800000(4294967296.0_s)              0xffffffff4f800000(4294967296.0_s)              
f10                 0xffffffff5f800000(1.8446744073709552e+19_s)    0xffffffff5f800000(1.8446744073709552e+19_s)    
f11                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f14                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff08c1b823(1.1659055311619432e-33_s)    X
f20                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f26                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f27                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f28                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

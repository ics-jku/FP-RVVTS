# FailID_000829 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 829
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
_reg_f0: .byte 0x00,0x00,0x80,0x94,0x8a,0xfd,0xdf,0xc1
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x2f,0x06,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x20,0x68,0x40
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x80,0xbf,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xe0,0x20,0x00,0x04,0xe0,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xf3,0x91,0x01,0x34,0x00,0x00,0x00,0x00
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x6f,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x10,0x40
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0xd6,0x09,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x80,0xf9,0xc8,0x00,0xca,0x41
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0xf7,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x41
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017fec7            // ra
    li x2, 0x4                   // sp
    li x3, 0x8017fc0f            // gp
    li x4, 0x0                   // tp
    li x5, 0x801fee0d            // t0
    li x6, 0x8028066a            // t1
    li x7, 0x80000628            // t2
    li x8, 0x8009d5ae            // fp
    li x9, 0x80000628            // s1
    li x10, 0xa8bde730           // a0
    li x11, 0xffffffffffff9073   // a1
    li x12, 0x6000               // a2
    li x13, 0x802001d3           // a3
    li x14, 0x41                 // a4
    li x15, 0x1003190d6          // a5
    li x16, 0x6000               // a6
    li x17, 0xffffffff7fc00000   // a7
    li x18, 0x40                 // s2
    li x19, 0xffffffffffffffff   // s3
    li x20, 0x0                  // s4
    li x21, 0x801991dc           // s5
    li x22, 0x8017faef           // s6
    li x23, 0x0                  // s7
    li x24, 0x7ffffb85           // s8
    li x25, 0x7ffff9e4           // s9
    li x26, 0x7ffffb99           // s10
    li x27, 0x801800b8           // s11
    li x28, 0x8017f9b4           // t3
    li x29, 0x7ffff941           // t4
    li x30, 0x54                 // t5
    li x31, 0x7ffffb99           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x9'}, 'clob': {'x9', 'x18', 'f29'}})
    
    li x18, 0x1ffff8
    and x9, x9, x18
    li x18, 0x7ffffc24
    add x9, x9, x18
    fld f29, 0x3dc(x9)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f29                 0xffffffff4efffff7(2147482496.0_s)              0x00c292931ff2829b(5.289639943572843e-305_d)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f29, 0x3dc(x9)
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f29                 0xffffffff4efffff7(2147482496.0_s)              0x00c292931ff2829b(5.289639943572843e-305_d)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f29, x3, x9
gp(x3)              0x000000008017fc0f(2149055503)                  0x000000008017fc0f(2149055503)
s1(x9)              0x000000008000024c(2147484236)                  0x000000008000024c(2147484236)
f29                 0xffffffff4efffff7(2147482496.0_s)              0x00c292931ff2829b(5.289639943572843e-305_d)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fec7(2149056199)                  0x000000008017fec7(2149056199)                  
sp(x2)              0x0000000000000004(4)                           0x0000000000000004(4)                           
gp(x3)              0x000000008017fc0f(2149055503)                  0x000000008017fc0f(2149055503)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x00000000801fee0d(2149576205)                  0x00000000801fee0d(2149576205)                  
t1(x6)              0x000000008028066a(2150106730)                  0x000000008028066a(2150106730)                  
t2(x7)              0x0000000080000628(2147485224)                  0x0000000080000628(2147485224)                  
fp(x8)              0x000000008009d5ae(2148128174)                  0x000000008009d5ae(2148128174)                  
s1(x9)              0x000000008000024c(2147484236)                  0x000000008000024c(2147484236)                  
a0(x10)             0x00000000a8bde730(2831017776)                  0x00000000a8bde730(2831017776)                  
a1(x11)             0xffffffffffff9073(18446744073709523059)        0xffffffffffff9073(18446744073709523059)        
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x00000000802001d3(2149581267)                  0x00000000802001d3(2149581267)                  
a4(x14)             0x0000000000000041(65)                          0x0000000000000041(65)                          
a5(x15)             0x00000001003190d6(4298215638)                  0x00000001003190d6(4298215638)                  
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
s2(x18)             0x000000007ffffc24(2147482660)                  0x000000007ffffc24(2147482660)                  
s3(x19)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x00000000801991dc(2149159388)                  0x00000000801991dc(2149159388)                  
s6(x22)             0x000000008017faef(2149055215)                  0x000000008017faef(2149055215)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x000000007ffffb85(2147482501)                  0x000000007ffffb85(2147482501)                  
s9(x25)             0x000000007ffff9e4(2147482084)                  0x000000007ffff9e4(2147482084)                  
s10(x26)            0x000000007ffffb99(2147482521)                  0x000000007ffffb99(2147482521)                  
s11(x27)            0x00000000801800b8(2149056696)                  0x00000000801800b8(2149056696)                  
t3(x28)             0x000000008017f9b4(2149054900)                  0x000000008017f9b4(2149054900)                  
t4(x29)             0x000000007ffff941(2147481921)                  0x000000007ffff941(2147481921)                  
t5(x30)             0x0000000000000054(84)                          0x0000000000000054(84)                          
t6(x31)             0x000000007ffffb99(2147482521)                  0x000000007ffffb99(2147482521)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            067180ea84ae925282c400c0a1a5141c35dad1fe        067180ea84ae925282c400c0a1a5141c35dad1fe        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000748(2147485512)                  0x0000000080000748(2147485512)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000041(65)                          0x0000000000000041(65)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xc1dffd8a94800000(-2146839122.0_d)             0xc1dffd8a94800000(-2146839122.0_d)             
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffff8000062f(-2.2182554690261854e-42_s)   0xffffffff8000062f(-2.2182554690261854e-42_s)   
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x4068200000000000(193.0_d)                     0x4068200000000000(193.0_d)                     
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffffbf800000(-1.0_s)                      0xffffffffbf800000(-1.0_s)                      
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41e0040020e00000(2149581063.0_d)              0x41e0040020e00000(2149581063.0_d)              
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x00000000340191f3(4.31081234e-315_d)           0x00000000340191f3(4.31081234e-315_d)           
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffffffff006f(6.616115570068359e-06_h)     0xffffffffffff006f(6.616115570068359e-06_h)     
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x4010000000000000(4.0_d)                       0x4010000000000000(4.0_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff4f0009d6(2148128256.0_s)              0xffffffff4f0009d6(2148128256.0_s)              
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x41ca00c8f9800000(872518131.0_d)               0x41ca00c8f9800000(872518131.0_d)               
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff4efffff7(2147482496.0_s)              0x00c292931ff2829b(5.289639943572843e-305_d)    X
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

# FailID_004014 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4014
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x05,0x43,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0xf0,0xe1,0xd1,0xc1
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0xbc,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f12:.byte 0xfa,0xf4,0x27,0x80,0x00,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x23,0xb8,0x41,0x04,0x23,0xbc,0x51,0x04
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x65,0x02,0x20,0x80,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x80,0x49,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x83,0x03,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'res0(0b101)', 'res': 0}
    li t0, 0xa2
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7fffffff            // ra
    li x2, 0x801ffeaa            // sp
    li x3, 0x200                 // gp
    li x4, 0x100                 // tp
    li x5, 0x8aef72c             // t0
    li x6, 0x8000000             // t1
    li x7, 0x6000                // t2
    li x8, 0x73                  // fp
    li x9, 0x1                   // s1
    li x10, 0x6000               // a0
    li x11, 0x8017ff75           // a1
    li x12, 0x0                  // a2
    li x13, 0xffffffffac3bf000   // a3
    li x14, 0x800008a9           // a4
    li x15, 0xffffffff80000383   // a5
    li x16, 0xe5f3a718           // a6
    li x17, 0x801ffe6d           // a7
    li x18, 0x8000026d           // s2
    li x19, 0x0                  // s3
    li x20, 0x0                  // s4
    li x21, 0xffffffffffff7e00   // s5
    li x22, 0x200                // s6
    li x23, 0xffffffffffffffff   // s7
    li x24, 0x0                  // s8
    li x25, 0x0                  // s9
    li x26, 0x401001d5000        // s10
    li x27, 0xf2b98728           // s11
    li x28, 0x80000718           // t3
    li x29, 0x200                // t4
    li x30, 0x80005974           // t5
    li x31, 0x8017f955           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x17'}, 'clob': {'x24', 'x17', 'f11'}})
    
    li x24, 0x1ffffc
    and x17, x17, x24
    li x24, 0x7ffff9cc
    add x17, x17, x24
    flw f11, 0x634(x17)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f11                 0xffffffffffff7c00(inf_h)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f11, 0x634(x17)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['inf', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f11                 0xffffffffffff7c00(inf_h)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f11, x634, x17
a7(x17)             0x00000000801ff838(2149578808)                  0x00000000801ff838(2149578808)
f11                 0xffffffffffff7c00(inf_h)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
sp(x2)              0x00000000801ffeaa(2149580458)                  0x00000000801ffeaa(2149580458)                  
gp(x3)              0x0000000000000200(512)                         0x0000000000000200(512)                         
tp(x4)              0x0000000000000100(256)                         0x0000000000000100(256)                         
t0(x5)              0x0000000008aef72c(145684268)                   0x0000000008aef72c(145684268)                   
t1(x6)              0x0000000008000000(134217728)                   0x0000000008000000(134217728)                   
t2(x7)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
fp(x8)              0x0000000000000073(115)                         0x0000000000000073(115)                         
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a1(x11)             0x000000008017ff75(2149056373)                  0x000000008017ff75(2149056373)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0xffffffffac3bf000(18446744072304193536)        0xffffffffac3bf000(18446744072304193536)        
a4(x14)             0x00000000800008a9(2147485865)                  0x00000000800008a9(2147485865)                  
a5(x15)             0xffffffff80000383(18446744071562068867)        0xffffffff80000383(18446744071562068867)        
a6(x16)             0x00000000e5f3a718(3857950488)                  0x00000000e5f3a718(3857950488)                  
a7(x17)             0x00000000801ff838(2149578808)                  0x00000000801ff838(2149578808)                  
s2(x18)             0x000000008000026d(2147484269)                  0x000000008000026d(2147484269)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0xffffffffffff7e00(18446744073709518336)        0xffffffffffff7e00(18446744073709518336)        
s6(x22)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s7(x23)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s8(x24)             0x000000007ffff9cc(2147482060)                  0x000000007ffff9cc(2147482060)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x00000401001d5000(4402343399424)               0x00000401001d5000(4402343399424)               
s11(x27)            0x00000000f2b98728(4072245032)                  0x00000000f2b98728(4072245032)                  
t3(x28)             0x0000000080000718(2147485464)                  0x0000000080000718(2147485464)                  
t4(x29)             0x0000000000000200(512)                         0x0000000000000200(512)                         
t5(x30)             0x0000000080005974(2147506548)                  0x0000000080005974(2147506548)                  
t6(x31)             0x000000008017f955(2149054805)                  0x000000008017f955(2149054805)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            fb92f3f7aa358433bc434a80dc6c184a9ca65ac4        fb92f3f7aa358433bc434a80dc6c184a9ca65ac4        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000710(2147485456)                  0x0000000080000710(2147485456)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000a2(162)                         0x00000000000000a2(162)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            res0(0b101)                                     res0(0b101)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff43050000(133.0_s)                     0xffffffff43050000(133.0_s)                     
f3                  0xc1d1e1f000000000(-1200078848.0_d)             0xc1d1e1f000000000(-1200078848.0_d)             
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f8                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff000000bc(2.634441112930656e-43_s)     0xffffffff000000bc(2.634441112930656e-43_s)     
f11                 0xffffffffffff7c00(inf_h)                       0xffffffff00000000(0.0_s)                       X
f12                 0x000000008027f4fa(1.0622916647e-314_d)         0x000000008027f4fa(1.0622916647e-314_d)         
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x0451bc230441b823(7.27935879360729e-288_d)     0x0451bc230441b823(7.27935879360729e-288_d)     
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0x0000000080200265(1.062034329e-314_d)          0x0000000080200265(1.062034329e-314_d)          
f24                 0x7fffffff42140000(nan_d)                       0x7fffffff42140000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f28                 0xffffffff49800000(1048576.0_s)                 0xffffffff49800000(1048576.0_s)                 
f29                 0xffffffff80000383(-1.2597673194280105e-42_s)   0xffffffff80000383(-1.2597673194280105e-42_s)   
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
STATES DIFFER: True
```

# FailID_004300 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4300
* Isolated failing instruction: `fsd`
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
_reg_f1: .byte 0x4f,0x3d,0x2e,0xd9,0x1b,0xd4,0x66,0x93
_reg_f2: .byte 0x23,0x3b,0xd3,0x4e,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0xa1,0xb3,0x8b,0xc1,0xa2,0x07,0x90,0x3d
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f6: .byte 0x03,0xb4,0x94,0x38,0x63,0x35,0xb7,0x8d
_reg_f7: .byte 0x93,0x0c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x59,0x52,0x66,0xea,0x97,0xaa,0x8a,0x3b
_reg_f9: .byte 0xec,0xfa,0xc7,0x5c,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0xf1,0x46,0xb2,0x9e,0xf5,0x51,0xcc,0x69
_reg_f12:.byte 0xeb,0x91,0x9d,0x69,0x42,0xa5,0x64,0x47
_reg_f13:.byte 0xcf,0x94,0xde,0xb1,0xcc,0x26,0xc8,0xde
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0x40,0xb8,0xda,0x90,0xd6,0xc1
_reg_f16:.byte 0x00,0x00,0x00,0x9f,0x4a,0x25,0xc3,0xc3
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x92,0x08,0xb0,0xb6,0x40,0x70,0x23,0x9a
_reg_f19:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f20:.byte 0xbb,0x8c,0xf6,0x70,0x93,0xca,0x45,0x90
_reg_f21:.byte 0xbb,0x8c,0xf6,0x70,0x93,0xca,0x45,0x90
_reg_f22:.byte 0xc6,0x35,0x94,0x66,0x66,0xa2,0x56,0xd5
_reg_f23:.byte 0x00,0x00,0xd0,0x42,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x80,0x56,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x8b,0x3b,0xa6,0x01,0x35,0xcc,0xe9,0xdb
_reg_f27:.byte 0x9d,0xa5,0x63,0xd5,0x67,0xe5,0xf2,0x7b
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f30:.byte 0x85,0x5f,0x1c,0xbc,0xed,0x2f,0x76,0x0c
_reg_f31:.byte 0x33,0x5a,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': True, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x79
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80005822            // ra
    li x2, 0x8024907e            // sp
    li x3, 0x8017fef1            // gp
    li x4, 0x7ffffcc4            // tp
    li x5, 0x71f22000            // t0
    li x6, 0xffffffffa3999000    // t1
    li x7, 0x0                   // t2
    li x8, 0x63fd75c2ecd2659     // fp
    li x9, 0xffffffffffffffff    // s1
    li x10, 0x8017fc5d           // a0
    li x11, 0xd9b56ac200000000   // a1
    li x12, 0x801a0d17           // a2
    li x13, 0x0                  // a3
    li x14, 0xc86cc86c           // a4
    li x15, 0x58e8a8ba13aefcbe   // a5
    li x16, 0xffffffffffffffff   // a6
    li x17, 0xffffffff96859000   // a7
    li x18, 0xfffec47180225a33   // s2
    li x19, 0x7ffffcc4           // s3
    li x20, 0x80000311           // s4
    li x21, 0x73                 // s5
    li x22, 0x800002b7           // s6
    li x23, 0x800062b7           // s7
    li x24, 0x69                 // s8
    li x25, 0x0                  // s9
    li x26, 0x0                  // s10
    li x27, 0xf0674fb3b36ad584   // s11
    li x28, 0x7ffffc05           // t3
    li x29, 0x7ffffcc4           // t4
    li x30, 0x8017fb60           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x19', 'fcsr.rm', 'f26'}, 'clob': {'x19', 'x24'}})
    
    li x24, 0xffff8
    and x19, x19, x24
    li x24, 0x8017faa1
    add x19, x19, x24
    fsd f26, 0x55f(x19)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        64e83dae9d13e640cbe42447d3135c2ee7e02bc7        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f26, 0x55f(x19)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'div-by-0', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        64e83dae9d13e640cbe42447d3135c2ee7e02bc7        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f26, x55, x19
s3(x19)             0x000000008027f761(2150102881)                  0x000000008027f761(2150102881)
f26                 0xdbe9cc3501a63b8b(-5.859611122888421e+134_d)   0xdbe9cc3501a63b8b(-5.859611122888421e+134_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080005822(2147506210)                  0x0000000080005822(2147506210)                  
sp(x2)              0x000000008024907e(2149879934)                  0x000000008024907e(2149879934)                  
gp(x3)              0x000000008017fef1(2149056241)                  0x000000008017fef1(2149056241)                  
tp(x4)              0x000000007ffffcc4(2147482820)                  0x000000007ffffcc4(2147482820)                  
t0(x5)              0x0000000071f22000(1911693312)                  0x0000000071f22000(1911693312)                  
t1(x6)              0xffffffffa3999000(18446744072159334400)        0xffffffffa3999000(18446744072159334400)        
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x063fd75c2ecd2659(450315278682498649)          0x063fd75c2ecd2659(450315278682498649)          
s1(x9)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a0(x10)             0x000000008017fc5d(2149055581)                  0x000000008017fc5d(2149055581)                  
a1(x11)             0xd9b56ac200000000(15687562258471190528)        0xd9b56ac200000000(15687562258471190528)        
a2(x12)             0x00000000801a0d17(2149190935)                  0x00000000801a0d17(2149190935)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x00000000c86cc86c(3362572396)                  0x00000000c86cc86c(3362572396)                  
a5(x15)             0x58e8a8ba13aefcbe(6406555987082149054)         0x58e8a8ba13aefcbe(6406555987082149054)         
a6(x16)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a7(x17)             0xffffffff96859000(18446744071939919872)        0xffffffff96859000(18446744071939919872)        
s2(x18)             0xfffec47180225a33(18446397115516213811)        0xfffec47180225a33(18446397115516213811)        
s3(x19)             0x000000008027f761(2150102881)                  0x000000008027f761(2150102881)                  
s4(x20)             0x0000000080000311(2147484433)                  0x0000000080000311(2147484433)                  
s5(x21)             0x0000000000000073(115)                         0x0000000000000073(115)                         
s6(x22)             0x00000000800002b7(2147484343)                  0x00000000800002b7(2147484343)                  
s7(x23)             0x00000000800062b7(2147508919)                  0x00000000800062b7(2147508919)                  
s8(x24)             0x000000008017faa1(2149055137)                  0x000000008017faa1(2149055137)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0xf0674fb3b36ad584(17322902124931765636)        0xf0674fb3b36ad584(17322902124931765636)        
t3(x28)             0x000000007ffffc05(2147482629)                  0x000000007ffffc05(2147482629)                  
t4(x29)             0x000000007ffffcc4(2147482820)                  0x000000007ffffcc4(2147482820)                  
t5(x30)             0x000000008017fb60(2149055328)                  0x000000008017fb60(2149055328)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            08f8b8c72321c8919d0607f07988387773a20d92        08f8b8c72321c8919d0607f07988387773a20d92        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        64e83dae9d13e640cbe42447d3135c2ee7e02bc7        X
lastPC              0x0000000080000788(2147485576)                  0x0000000080000788(2147485576)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000079(121)                         0x0000000000000079(121)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x9366d41bd92e3d4f(-3.3110934255220594e-215_d)  0x9366d41bd92e3d4f(-3.3110934255220594e-215_d)  
f2                  0xffffffff4ed33b23(1771934080.0_s)              0xffffffff4ed33b23(1771934080.0_s)              
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x3d9007a2c18bb3a1(3.6447607294693166e-12_d)    0x3d9007a2c18bb3a1(3.6447607294693166e-12_d)    
f5                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f6                  0x8db735633894b403(-1.3596008341984277e-242_d)  0x8db735633894b403(-1.3596008341984277e-242_d)  
f7                  0xffffffffffff0c93(0.0002791881561279297_h)     0xffffffffffff0c93(0.0002791881561279297_h)     
f8                  0x3b8aaa97ea665259(7.058532158926849e-22_d)     0x3b8aaa97ea665259(7.058532158926849e-22_d)     
f9                  0xffffffff5cc7faec(4.503152950771712e+17_s)     0xffffffff5cc7faec(4.503152950771712e+17_s)     
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x69cc51f59eb246f1(4.335535323009277e+201_d)    0x69cc51f59eb246f1(4.335535323009277e+201_d)    
f12                 0x4764a542699d91eb(8.575823720035319e+35_d)     0x4764a542699d91eb(8.575823720035319e+35_d)     
f13                 0xdec826ccb1de94cf(-3.8602291308163043e+148_d)  0xdec826ccb1de94cf(-3.8602291308163043e+148_d)  
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xc1d690dab8400000(-1514367713.0_d)             0xc1d690dab8400000(-1514367713.0_d)             
f16                 0xc3c3254a9f000000(-2.759181815238361e+18_d)    0xc3c3254a9f000000(-2.759181815238361e+18_d)    
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x9a237040b6b00892(-9.14945255019502e-183_d)    0x9a237040b6b00892(-9.14945255019502e-183_d)    
f19                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f20                 0x9045ca9370f68cbb(-2.807221684975501e-230_d)   0x9045ca9370f68cbb(-2.807221684975501e-230_d)   
f21                 0x9045ca9370f68cbb(-2.807221684975501e-230_d)   0x9045ca9370f68cbb(-2.807221684975501e-230_d)   
f22                 0xd556a266669435c6(-1.2673805605654955e+103_d)  0xd556a266669435c6(-1.2673805605654955e+103_d)  
f23                 0xffffffff42d00000(104.0_s)                     0xffffffff42d00000(104.0_s)                     
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffffffff5680(104.0_h)                     0xffffffffffff5680(104.0_h)                     
f26                 0xdbe9cc3501a63b8b(-5.859611122888421e+134_d)   0xdbe9cc3501a63b8b(-5.859611122888421e+134_d)   
f27                 0x7bf2e567d563a59d(1.1509286272135676e+289_d)   0x7bf2e567d563a59d(1.1509286272135676e+289_d)   
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f30                 0x0c762fedbc1c5f85(1.2395570086590742e-248_d)   0x0c762fedbc1c5f85(1.2395570086590742e-248_d)   
f31                 0xffffffffffff5a33(198.375_h)                   0xffffffffffff5a33(198.375_h)                   
STATES DIFFER: True
```

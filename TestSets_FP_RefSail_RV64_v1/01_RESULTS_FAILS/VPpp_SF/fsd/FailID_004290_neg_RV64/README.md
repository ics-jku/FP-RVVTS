# FailID_004290 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4290
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
_reg_f0: .byte 0xb1,0x0b,0x66,0x75,0x55,0xeb,0x95,0x3b
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0xcc,0xe4,0x92,0x11,0xa3,0xfb,0x6d,0x2f
_reg_f3: .byte 0xa2,0xf8,0xce,0xf1,0xec,0x65,0x6f,0x2a
_reg_f4: .byte 0x65,0xd7,0xe7,0x3b,0xe2,0x68,0x11,0x6e
_reg_f5: .byte 0xf6,0x8e,0xac,0xc7,0x0c,0xcd,0x79,0x53
_reg_f6: .byte 0xda,0x6c,0x24,0x80,0xff,0xff,0xff,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f8: .byte 0xcd,0xe4,0x92,0x11,0xa3,0xfb,0x6d,0x2f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0xc1,0x6e,0xc6,0x6f,0x87,0x38,0xdb,0x0f
_reg_f11:.byte 0x96,0xf1,0x31,0x6f,0x8c,0x95,0xb4,0xe6
_reg_f12:.byte 0x34,0xcb,0x62,0x79,0x17,0x41,0xae,0x14
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x34,0xcb,0x62,0x79,0x17,0x41,0xae,0x14
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xd0,0xbb,0x9f,0x12,0x15,0x25,0x50,0xca
_reg_f17:.byte 0x05,0x5e,0x5c,0xc5,0x99,0xaf,0x31,0x89
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0xda,0x6c,0x24,0x80,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0xb8,0xfb,0xaa,0x64,0x01,0xa9,0x7e,0xd0
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x74,0xfd,0x62,0x8b,0xb4,0xb7,0x5c,0xdb
_reg_f26:.byte 0x38,0x5b,0xa1,0x4e,0x69,0x32,0xfc,0xbc
_reg_f27:.byte 0xbc,0xca,0xe2,0x8e,0x8b,0x06,0xdd,0x6f
_reg_f28:.byte 0x2c,0x89,0xd5,0x5b,0xab,0xaa,0xd9,0xa6
_reg_f29:.byte 0x34,0xcb,0x62,0x79,0x17,0x41,0xae,0x14
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x22
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x802004a7            // ra
    li x2, 0x1fffff8             // sp
    li x3, 0x6000                // gp
    li x4, 0x0                   // tp
    li x5, 0xd4371758            // t0
    li x6, 0x0                   // t1
    li x7, 0xfffffffffffffd23    // t2
    li x8, 0x6000                // fp
    li x9, 0x7ffffe34            // s1
    li x10, 0x8000014b           // a0
    li x11, 0x8027f400           // a1
    li x12, 0x400                // a2
    li x13, 0x80000731           // a3
    li x14, 0x340191f3           // a4
    li x15, 0x8017f907           // a5
    li x16, 0x80200415           // a6
    li x17, 0x801ffc60           // a7
    li x18, 0x8017fdd5           // s2
    li x19, 0x8000014b           // s3
    li x20, 0x1                  // s4
    li x21, 0x8017fa42           // s5
    li x22, 0x0                  // s6
    li x23, 0x8027f400           // s7
    li x24, 0x7ffff975           // s8
    li x25, 0x59                 // s9
    li x26, 0x0                  // s10
    li x27, 0x7ffffda9           // s11
    li x28, 0x1                  // t3
    li x29, 0x1                  // t4
    li x30, 0x80180782           // t5
    li x31, 0x800000f7           // t6
    // INSTRUCTION ({'dep': {'x5', 'fcsr.rm', 'f9', 'mstatus.fs/vs.fs'}, 'clob': {'x13', 'x5'}})
    
    li x13, 0xffff8
    and x5, x5, x13
    li x13, 0x801806e6
    add x5, x5, x13
    fsd f9, -0x6e6(x5)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        33b0eed566495d35417c2eb1cb4773aa1cb699ea        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f9, -0x6e6(x5)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        33b0eed566495d35417c2eb1cb4773aa1cb699ea        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x6, e6, x5
t0(x5)              0x00000000801f1e3e(2149523006)                  0x00000000801f1e3e(2149523006)
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000802004a7(2149581991)                  0x00000000802004a7(2149581991)                  
sp(x2)              0x0000000001fffff8(33554424)                    0x0000000001fffff8(33554424)                    
gp(x3)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x00000000801f1e3e(2149523006)                  0x00000000801f1e3e(2149523006)                  
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0xfffffffffffffd23(18446744073709550883)        0xfffffffffffffd23(18446744073709550883)        
fp(x8)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s1(x9)              0x000000007ffffe34(2147483188)                  0x000000007ffffe34(2147483188)                  
a0(x10)             0x000000008000014b(2147483979)                  0x000000008000014b(2147483979)                  
a1(x11)             0x000000008027f400(2150102016)                  0x000000008027f400(2150102016)                  
a2(x12)             0x0000000000000400(1024)                        0x0000000000000400(1024)                        
a3(x13)             0x00000000801806e6(2149058278)                  0x00000000801806e6(2149058278)                  
a4(x14)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
a5(x15)             0x000000008017f907(2149054727)                  0x000000008017f907(2149054727)                  
a6(x16)             0x0000000080200415(2149581845)                  0x0000000080200415(2149581845)                  
a7(x17)             0x00000000801ffc60(2149579872)                  0x00000000801ffc60(2149579872)                  
s2(x18)             0x000000008017fdd5(2149055957)                  0x000000008017fdd5(2149055957)                  
s3(x19)             0x000000008000014b(2147483979)                  0x000000008000014b(2147483979)                  
s4(x20)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s5(x21)             0x000000008017fa42(2149055042)                  0x000000008017fa42(2149055042)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x000000008027f400(2150102016)                  0x000000008027f400(2150102016)                  
s8(x24)             0x000000007ffff975(2147481973)                  0x000000007ffff975(2147481973)                  
s9(x25)             0x0000000000000059(89)                          0x0000000000000059(89)                          
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000007ffffda9(2147483049)                  0x000000007ffffda9(2147483049)                  
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x0000000080180782(2149058434)                  0x0000000080180782(2149058434)                  
t6(x31)             0x00000000800000f7(2147483895)                  0x00000000800000f7(2147483895)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            c4fff48fea14ee23510928edb935ff709e774c04        c4fff48fea14ee23510928edb935ff709e774c04        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        33b0eed566495d35417c2eb1cb4773aa1cb699ea        X
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000022(34)                          0x0000000000000022(34)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x3b95eb5575660bb1(1.1603966371566636e-21_d)    0x3b95eb5575660bb1(1.1603966371566636e-21_d)    
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x2f6dfba31192e4cc(3.1608626740755325e-80_d)    0x2f6dfba31192e4cc(3.1608626740755325e-80_d)    
f3                  0x2a6f65ecf1cef8a2(2.7380131401189653e-104_d)   0x2a6f65ecf1cef8a2(2.7380131401189653e-104_d)   
f4                  0x6e1168e23be7d765(1.5732877320277818e+222_d)   0x6e1168e23be7d765(1.5732877320277818e+222_d)   
f5                  0x5379cd0cc7ac8ef6(1.3454724316159919e+94_d)    0x5379cd0cc7ac8ef6(1.3454724316159919e+94_d)    
f6                  0x7fffffff80246cda(nan_d)                       0x7fffffff80246cda(nan_d)                       
f7                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f8                  0x2f6dfba31192e4cd(3.160862674075533e-80_d)     0x2f6dfba31192e4cd(3.160862674075533e-80_d)     
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x0fdb38876fc66ec1(2.7395832709851377e-232_d)   0x0fdb38876fc66ec1(2.7395832709851377e-232_d)   
f11                 0xe6b4958c6f31f196(-5.597714902849015e+186_d)   0xe6b4958c6f31f196(-5.597714902849015e+186_d)   
f12                 0x14ae41177962cb34(4.601290157299096e-209_d)    0x14ae41177962cb34(4.601290157299096e-209_d)    
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x14ae41177962cb34(4.601290157299096e-209_d)    0x14ae41177962cb34(4.601290157299096e-209_d)    
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xca502515129fbbd0(-9.438291517535915e+49_d)    0xca502515129fbbd0(-9.438291517535915e+49_d)    
f17                 0x8931af99c55c5e05(-2.1939764707558864e-264_d)  0x8931af99c55c5e05(-2.1939764707558864e-264_d)  
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff80246cda(-3.345126444694559e-39_s)    0xffffffff80246cda(-3.345126444694559e-39_s)    
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xd07ea90164aafbb8(-5.680329616258332e+79_d)    0xd07ea90164aafbb8(-5.680329616258332e+79_d)    
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xdb5cb7b48b62fd74(-1.2739906469983861e+132_d)  0xdb5cb7b48b62fd74(-1.2739906469983861e+132_d)  
f26                 0xbcfc32694ea15b38(-6.2609738193014745e-15_d)   0xbcfc32694ea15b38(-6.2609738193014745e-15_d)   
f27                 0x6fdd068b8ee2cabc(7.041049670107697e+230_d)    0x6fdd068b8ee2cabc(7.041049670107697e+230_d)    
f28                 0xa6d9aaab5bd5892c(-1.5530713548288991e-121_d)  0xa6d9aaab5bd5892c(-1.5530713548288991e-121_d)  
f29                 0x14ae41177962cb34(4.601290157299096e-209_d)    0x14ae41177962cb34(4.601290157299096e-209_d)    
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

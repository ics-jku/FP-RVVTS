# FailID_000816 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 816
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
_reg_f0: .byte 0xb1,0x0b,0x66,0x75,0x55,0xeb,0x95,0x3b
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0xcc,0xe4,0x92,0x11,0xa3,0xfb,0x6d,0x2f
_reg_f3: .byte 0xa2,0xf8,0xce,0xf1,0xec,0x65,0x6f,0x2a
_reg_f4: .byte 0x65,0xd7,0xe7,0x3b,0xe2,0x68,0x11,0x6e
_reg_f5: .byte 0xf6,0x8e,0xac,0xc7,0x0c,0xcd,0x79,0x53
_reg_f6: .byte 0xda,0x6c,0x24,0x80,0xff,0xff,0xff,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0xcd,0xe4,0x92,0x11,0xa3,0xfb,0x6d,0x2f
_reg_f9: .byte 0x8c,0x2b,0xa7,0x24,0xa3,0x13,0xf3,0xfb
_reg_f10:.byte 0xc1,0x6e,0xc6,0x6f,0x87,0x38,0xdb,0x0f
_reg_f11:.byte 0x96,0xf1,0x31,0x6f,0x8c,0x95,0xb4,0xe6
_reg_f12:.byte 0x34,0xcb,0x62,0x79,0x17,0x41,0xae,0x14
_reg_f13:.byte 0xa6,0x86,0x7c,0x5e,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x92,0xe3,0xf6,0x59,0x6d,0xf5,0x07,0x6a
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xd0,0xbb,0x9f,0x12,0x15,0x25,0x50,0xca
_reg_f17:.byte 0x05,0x5e,0x5c,0xc5,0x99,0xaf,0x31,0x89
_reg_f18:.byte 0x08,0xd6,0xa3,0x84,0x00,0x84,0xc4,0xf7
_reg_f19:.byte 0xda,0x6c,0x24,0x80,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0xd1,0x8a,0x95,0x72,0x4f,0x67,0xe1
_reg_f23:.byte 0xb8,0xfb,0xaa,0x64,0x01,0xa9,0x7e,0xd0
_reg_f24:.byte 0x96,0xf1,0x31,0x6f,0x8c,0x95,0xb4,0xe6
_reg_f25:.byte 0x74,0xfd,0x62,0x8b,0xb4,0xb7,0x5c,0xdb
_reg_f26:.byte 0x38,0x5b,0xa1,0x4e,0x69,0x32,0xfc,0xbc
_reg_f27:.byte 0xbc,0xca,0xe2,0x8e,0x8b,0x06,0xdd,0x6f
_reg_f28:.byte 0x2c,0x89,0xd5,0x5b,0xab,0xaa,0xd9,0xa6
_reg_f29:.byte 0x34,0xcb,0x62,0x79,0x17,0x41,0xae,0x14
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x25,0x07,0x79,0xfe,0xdc,0x5e,0x8b,0x69
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x68
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80180e2c            // ra
    li x2, 0x0                   // sp
    li x3, 0x200801              // gp
    li x4, 0xffffffff7fdfc6d9    // tp
    li x5, 0x80000794            // t0
    li x6, 0x801fffec            // t1
    li x7, 0x6000                // t2
    li x8, 0x1000007             // fp
    li x9, 0x1                   // s1
    li x10, 0x1                  // a0
    li x11, 0x7ffffa92           // a1
    li x12, 0x80183e22           // a2
    li x13, 0x1                  // a3
    li x14, 0xfffc36             // a4
    li x15, 0x7ffff9ef           // a5
    li x16, 0x7ffffe77           // a6
    li x17, 0x80180602           // a7
    li x18, 0x100000b8e000       // s2
    li x19, 0x801ffdc1           // s3
    li x20, 0xeec00770           // s4
    li x21, 0x800006a000         // s5
    li x22, 0x7fffffac           // s6
    li x23, 0x1000067            // s7
    li x24, 0x8017feaf           // s8
    li x25, 0x80018b05           // s9
    li x26, 0x7ffff9f6           // s10
    li x27, 0x200                // s11
    li x28, 0x8025dbb4           // t3
    li x29, 0x0                  // t4
    li x30, 0x8017fc9f           // t5
    li x31, 0x801806aa           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x6'}, 'clob': {'f22', 'x6', 'x1'}})
    
    li x1, 0x1ffff8
    and x6, x6, x1
    li x1, 0x7ffffd57
    add x6, x6, x1
    fld f22, 0x2a9(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f22                 0xe1674f72958ad100(-1.6386128113013533e+161_d)  0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f22, 0x2a9(x6)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f22                 0xe1674f72958ad100(-1.6386128113013533e+161_d)  0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f22, x2, a9, x6
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)
t1(x6)              0x00000000801ffd3f(2149580095)                  0x00000000801ffd3f(2149580095)
f22                 0xe1674f72958ad100(-1.6386128113013533e+161_d)  0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffffd57(2147482967)                  0x000000007ffffd57(2147482967)                  
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000000200801(2099201)                     0x0000000000200801(2099201)                     
tp(x4)              0xffffffff7fdfc6d9(18446744071559956185)        0xffffffff7fdfc6d9(18446744071559956185)        
t0(x5)              0x0000000080000794(2147485588)                  0x0000000080000794(2147485588)                  
t1(x6)              0x00000000801ffd3f(2149580095)                  0x00000000801ffd3f(2149580095)                  
t2(x7)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
fp(x8)              0x0000000001000007(16777223)                    0x0000000001000007(16777223)                    
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x000000007ffffa92(2147482258)                  0x000000007ffffa92(2147482258)                  
a2(x12)             0x0000000080183e22(2149072418)                  0x0000000080183e22(2149072418)                  
a3(x13)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a4(x14)             0x0000000000fffc36(16776246)                    0x0000000000fffc36(16776246)                    
a5(x15)             0x000000007ffff9ef(2147482095)                  0x000000007ffff9ef(2147482095)                  
a6(x16)             0x000000007ffffe77(2147483255)                  0x000000007ffffe77(2147483255)                  
a7(x17)             0x0000000080180602(2149058050)                  0x0000000080180602(2149058050)                  
s2(x18)             0x0000100000b8e000(17592198160384)              0x0000100000b8e000(17592198160384)              
s3(x19)             0x00000000801ffdc1(2149580225)                  0x00000000801ffdc1(2149580225)                  
s4(x20)             0x00000000eec00770(4005562224)                  0x00000000eec00770(4005562224)                  
s5(x21)             0x000000800006a000(549756248064)                0x000000800006a000(549756248064)                
s6(x22)             0x000000007fffffac(2147483564)                  0x000000007fffffac(2147483564)                  
s7(x23)             0x0000000001000067(16777319)                    0x0000000001000067(16777319)                    
s8(x24)             0x000000008017feaf(2149056175)                  0x000000008017feaf(2149056175)                  
s9(x25)             0x0000000080018b05(2147584773)                  0x0000000080018b05(2147584773)                  
s10(x26)            0x000000007ffff9f6(2147482102)                  0x000000007ffff9f6(2147482102)                  
s11(x27)            0x0000000000000200(512)                         0x0000000000000200(512)                         
t3(x28)             0x000000008025dbb4(2149964724)                  0x000000008025dbb4(2149964724)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x000000008017fc9f(2149055647)                  0x000000008017fc9f(2149055647)                  
t6(x31)             0x00000000801806aa(2149058218)                  0x00000000801806aa(2149058218)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            045954e674aebc489dcea354d44698e3bc227562        045954e674aebc489dcea354d44698e3bc227562        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000754(2147485524)                  0x0000000080000754(2147485524)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000068(104)                         0x0000000000000068(104)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x3b95eb5575660bb1(1.1603966371566636e-21_d)    0x3b95eb5575660bb1(1.1603966371566636e-21_d)    
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x2f6dfba31192e4cc(3.1608626740755325e-80_d)    0x2f6dfba31192e4cc(3.1608626740755325e-80_d)    
f3                  0x2a6f65ecf1cef8a2(2.7380131401189653e-104_d)   0x2a6f65ecf1cef8a2(2.7380131401189653e-104_d)   
f4                  0x6e1168e23be7d765(1.5732877320277818e+222_d)   0x6e1168e23be7d765(1.5732877320277818e+222_d)   
f5                  0x5379cd0cc7ac8ef6(1.3454724316159919e+94_d)    0x5379cd0cc7ac8ef6(1.3454724316159919e+94_d)    
f6                  0x7fffffff80246cda(nan_d)                       0x7fffffff80246cda(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x2f6dfba31192e4cd(3.160862674075533e-80_d)     0x2f6dfba31192e4cd(3.160862674075533e-80_d)     
f9                  0xfbf313a324a72b8c(-1.1619281931686081e+289_d)  0xfbf313a324a72b8c(-1.1619281931686081e+289_d)  
f10                 0x0fdb38876fc66ec1(2.7395832709851377e-232_d)   0x0fdb38876fc66ec1(2.7395832709851377e-232_d)   
f11                 0xe6b4958c6f31f196(-5.597714902849015e+186_d)   0xe6b4958c6f31f196(-5.597714902849015e+186_d)   
f12                 0x14ae41177962cb34(4.601290157299096e-209_d)    0x14ae41177962cb34(4.601290157299096e-209_d)    
f13                 0xffffffff5e7c86a6(4.5491034658418196e+18_s)    0xffffffff5e7c86a6(4.5491034658418196e+18_s)    
f14                 0x6a07f56d59f6e392(5.868543734736942e+202_d)    0x6a07f56d59f6e392(5.868543734736942e+202_d)    
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xca502515129fbbd0(-9.438291517535915e+49_d)    0xca502515129fbbd0(-9.438291517535915e+49_d)    
f17                 0x8931af99c55c5e05(-2.1939764707558864e-264_d)  0x8931af99c55c5e05(-2.1939764707558864e-264_d)  
f18                 0xf7c4840084a3d608(-8.467419271097752e+268_d)   0xf7c4840084a3d608(-8.467419271097752e+268_d)   
f19                 0xffffffff80246cda(-3.345126444694559e-39_s)    0xffffffff80246cda(-3.345126444694559e-39_s)    
f20                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f21                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f22                 0xe1674f72958ad100(-1.6386128113013533e+161_d)  0x0000000000000000(0.0_d)                       X
f23                 0xd07ea90164aafbb8(-5.680329616258332e+79_d)    0xd07ea90164aafbb8(-5.680329616258332e+79_d)    
f24                 0xe6b4958c6f31f196(-5.597714902849015e+186_d)   0xe6b4958c6f31f196(-5.597714902849015e+186_d)   
f25                 0xdb5cb7b48b62fd74(-1.2739906469983861e+132_d)  0xdb5cb7b48b62fd74(-1.2739906469983861e+132_d)  
f26                 0xbcfc32694ea15b38(-6.2609738193014745e-15_d)   0xbcfc32694ea15b38(-6.2609738193014745e-15_d)   
f27                 0x6fdd068b8ee2cabc(7.041049670107697e+230_d)    0x6fdd068b8ee2cabc(7.041049670107697e+230_d)    
f28                 0xa6d9aaab5bd5892c(-1.5530713548288991e-121_d)  0xa6d9aaab5bd5892c(-1.5530713548288991e-121_d)  
f29                 0x14ae41177962cb34(4.601290157299096e-209_d)    0x14ae41177962cb34(4.601290157299096e-209_d)    
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x698b5edcfe790725(2.6188511256722263e+200_d)   0x698b5edcfe790725(2.6188511256722263e+200_d)   
STATES DIFFER: True
```

# FailID_000285 ARA pos RV64 fsqrt.d

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: pos/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 285
* Isolated failing instruction: `fsqrt.d`
* Minimized failing test case: [cblock_minimized_test_case.json](cblock_minimized_test_case.json)
* Resulting REF machine state: [mstate_RefSail.json](mstate_RefSail.json)
* Resulting DUT machine state: [mstate_DUT_ARA.json](mstate_DUT_ARA.json)
* Automated failure characterization report: [AFC_FP_report.log](AFC_FP_report.log)

## Report

### Minimized Failing Test Case
```
    // FLOATINGPOINT STATE DATA
    j _float_data_end
    .align 4
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f3: .byte 0xe5,0xe8,0x5b,0xcd,0x97,0x44,0xc3,0x75
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x41,0xcb,0xa3,0xe8,0xbb,0xf2,0x0a,0x93
_reg_f6: .byte 0x85,0x37,0xba,0xd8,0x6b,0x6d,0x1b,0x16
_reg_f7: .byte 0x07,0x6d,0x62,0xdd,0x4d,0x81,0x3b,0x64
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x0a,0xe2,0xbb,0x74,0x5c,0xdd,0x2b,0xde
_reg_f10:.byte 0x85,0xd6,0x56,0x43,0x93,0x01,0xe5,0x43
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0xae,0xad,0x9d,0x3c,0x80,0x4f,0x31,0x7e
_reg_f14:.byte 0xcc,0x66,0xb2,0x4e,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xe0,0x60,0xff,0x02,0xe0,0x41
_reg_f16:.byte 0xe5,0xe8,0x5b,0xcd,0x97,0x44,0xc3,0x75
_reg_f17:.byte 0x00,0x00,0xc0,0x79,0xfe,0xff,0xdf,0x41
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xa9,0x4e,0xf5,0x10,0xcf,0x09,0x04,0x34
_reg_f22:.byte 0x32,0x95,0x86,0x86,0xf2,0xb3,0xc6,0x98
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0xbf,0x3c,0xc3,0x72,0x37,0x94,0x57,0x74
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x9b,0x05,0x84,0x3a,0xdf,0x17,0x19,0xa7
_reg_f29:.byte 0xf4,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f30:.byte 0xbf,0x3c,0xc3,0x72,0x37,0x94,0x57,0x74
_reg_f31:.byte 0x57,0xd1,0xba,0xde,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x71
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0xa297548000000000    // ra
    li x2, 0xa80c9a1ab6b4203d    // sp
    li x3, 0x39db9860            // gp
    li x4, 0xde0db4d55ef1f92a    // tp
    li x5, 0x0                   // t0
    li x6, 0x3a84059b            // t1
    li x7, 0x8017fb07            // t2
    li x8, 0xe34a7c123ecb940a    // fp
    li x9, 0xa6181dbceaca7c1b    // s1
    li x10, 0x0                  // a0
    li x11, 0x64d73974b45feab6   // a1
    li x12, 0x0                  // a2
    li x13, 0x375b649550d26fda   // a3
    li x14, 0xa29754583bdd0f05   // a4
    li x15, 0x0                  // a5
    li x16, 0x40                 // a6
    li x17, 0x7ffff9e7           // a7
    li x18, 0x802680f7           // s2
    li x19, 0xe3df2e955b8c0a06   // s3
    li x20, 0xffffffffffffffff   // s4
    li x21, 0x800398cb           // s5
    li x22, 0xf9e6898d59336583   // s6
    li x23, 0xffffffff00000000   // s7
    li x24, 0x6000               // s8
    li x25, 0x80000464           // s9
    li x26, 0xfffffffffffff885   // s10
    li x27, 0xff029d1a39bc8ef0   // s11
    li x28, 0x200                // t3
    li x29, 0x0                  // t4
    li x30, 0x8017f985           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'f21', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'f25'}})
    fsqrt.d f25, f21, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f25                 0x39f9528b9b93c6e5(1.9975885106075398e-29_d)    0x39f9528b9b93c6e4(1.9975885106075395e-29_d)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.d f25, f21, dyn
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f25                 0x39f9528b9b93c6e5(1.9975885106075398e-29_d)    0x39f9528b9b93c6e4(1.9975885106075395e-29_d)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, f21
f21                 0x340409cf10f54ea9(3.990359857711249e-58_d)     0x340409cf10f54ea9(3.990359857711249e-58_d)
f25                 0x39f9528b9b93c6e5(1.9975885106075398e-29_d)    0x39f9528b9b93c6e4(1.9975885106075395e-29_d)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xa297548000000000(11715925864360181760)        0xa297548000000000(11715925864360181760)        
sp(x2)              0xa80c9a1ab6b4203d(12109222937617506365)        0xa80c9a1ab6b4203d(12109222937617506365)        
gp(x3)              0x0000000039db9860(970692704)                   0x0000000039db9860(970692704)                   
tp(x4)              0xde0db4d55ef1f92a(16000643879631190314)        0xde0db4d55ef1f92a(16000643879631190314)        
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x000000003a84059b(981730715)                   0x000000003a84059b(981730715)                   
t2(x7)              0x000000008017fb07(2149055239)                  0x000000008017fb07(2149055239)                  
fp(x8)              0xe34a7c123ecb940a(16378039412691014666)        0xe34a7c123ecb940a(16378039412691014666)        
s1(x9)              0xa6181dbceaca7c1b(11968348706967288859)        0xa6181dbceaca7c1b(11968348706967288859)        
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x64d73974b45feab6(7266339697190759094)         0x64d73974b45feab6(7266339697190759094)         
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x375b649550d26fda(3988892487435579354)         0x375b649550d26fda(3988892487435579354)         
a4(x14)             0xa29754583bdd0f05(11715925693565832965)        0xa29754583bdd0f05(11715925693565832965)        
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x0000000000000040(64)                          0x0000000000000040(64)                          
a7(x17)             0x000000007ffff9e7(2147482087)                  0x000000007ffff9e7(2147482087)                  
s2(x18)             0x00000000802680f7(2150007031)                  0x00000000802680f7(2150007031)                  
s3(x19)             0xe3df2e955b8c0a06(16419893985437026822)        0xe3df2e955b8c0a06(16419893985437026822)        
s4(x20)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s5(x21)             0x00000000800398cb(2147719371)                  0x00000000800398cb(2147719371)                  
s6(x22)             0xf9e6898d59336583(18007231400267441539)        0xf9e6898d59336583(18007231400267441539)        
s7(x23)             0xffffffff00000000(18446744069414584320)        0xffffffff00000000(18446744069414584320)        
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x0000000080000464(2147484772)                  0x0000000080000464(2147484772)                  
s10(x26)            0xfffffffffffff885(18446744073709549701)        0xfffffffffffff885(18446744073709549701)        
s11(x27)            0xff029d1a39bc8ef0(18375422165588414192)        0xff029d1a39bc8ef0(18375422165588414192)        
t3(x28)             0x0000000000000200(512)                         0x0000000000000200(512)                         
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x000000008017f985(2149054853)                  0x000000008017f985(2149054853)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            bd1e2dbe9f5168ebfe60df91c0ad23c06dc6b582        bd1e2dbe9f5168ebfe60df91c0ad23c06dc6b582        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800007d8(2147485656)                  0x00000000800007d8(2147485656)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000071(113)                         0x0000000000000071(113)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f3                  0x75c34497cd5be8e5(1.851576239328676e+259_d)    0x75c34497cd5be8e5(1.851576239328676e+259_d)    
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x930af2bbe8a3cb41(-6.107206019006025e-217_d)   0x930af2bbe8a3cb41(-6.107206019006025e-217_d)   
f6                  0x161b6d6bd8ba3785(3.4991937344581397e-202_d)   0x161b6d6bd8ba3785(3.4991937344581397e-202_d)   
f7                  0x643b814ddd626d07(6.8028460336568025e+174_d)   0x643b814ddd626d07(6.8028460336568025e+174_d)   
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xde2bdd5c74bbe20a(-4.349328095372005e+145_d)   0xde2bdd5c74bbe20a(-4.349328095372005e+145_d)   
f10                 0x43e501934356d685(1.2109222937617508e+19_d)    0x43e501934356d685(1.2109222937617508e+19_d)    
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x7e314f803c9dadae(7.24547025117768e+299_d)     0x7e314f803c9dadae(7.24547025117768e+299_d)     
f14                 0xffffffff4eb266cc(1496540672.0_s)              0xffffffff4eb266cc(1496540672.0_s)              
f15                 0x41e002ff60e00000(2149055239.0_d)              0x41e002ff60e00000(2149055239.0_d)              
f16                 0x75c34497cd5be8e5(1.851576239328676e+259_d)    0x75c34497cd5be8e5(1.851576239328676e+259_d)    
f17                 0x41dffffe79c00000(2147482087.0_d)              0x41dffffe79c00000(2147482087.0_d)              
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x340409cf10f54ea9(3.990359857711249e-58_d)     0x340409cf10f54ea9(3.990359857711249e-58_d)     
f22                 0x98c6b3f286869532(-2.5477361141978013e-189_d)  0x98c6b3f286869532(-2.5477361141978013e-189_d)  
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x7457943772c33cbf(2.701103548314535e+252_d)    0x7457943772c33cbf(2.701103548314535e+252_d)    
f25                 0x39f9528b9b93c6e5(1.9975885106075398e-29_d)    0x39f9528b9b93c6e4(1.9975885106075395e-29_d)    X
f26                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xa71917df3a84059b(-2.4293979216255902e-120_d)  0xa71917df3a84059b(-2.4293979216255902e-120_d)  
f29                 0xffffffff4efffff4(2147482112.0_s)              0xffffffff4efffff4(2147482112.0_s)              
f30                 0x7457943772c33cbf(2.701103548314535e+252_d)    0x7457943772c33cbf(2.701103548314535e+252_d)    
f31                 0xffffffffdebad157(-6.73081820934937e+18_s)     0xffffffffdebad157(-6.73081820934937e+18_s)     
STATES DIFFER: True
```

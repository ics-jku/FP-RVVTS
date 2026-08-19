# FailID_001512 VP++ FF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1512
* Isolated failing instruction: `flw`
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
_reg_f0: .byte 0x98,0x11,0x1c,0xe3,0x74,0x2d,0x4b,0x76
_reg_f1: .byte 0x7e,0x7e,0x78,0x9f,0x1c,0x79,0xbe,0x8a
_reg_f2: .byte 0x16,0xe2,0x3c,0xc1,0x24,0xb5,0x2a,0xd6
_reg_f3: .byte 0x48,0x8d,0x6f,0xfe,0x19,0x48,0x15,0x65
_reg_f4: .byte 0x81,0x16,0x59,0x90,0x3a,0xa3,0xca,0xf3
_reg_f5: .byte 0x6a,0x50,0x42,0x1c,0xe4,0xfb,0x6d,0xa1
_reg_f6: .byte 0x0e,0x24,0x3a,0xee,0xf0,0x13,0x61,0x13
_reg_f7: .byte 0x11,0x18,0xef,0x3d,0xe1,0xb3,0x71,0x3b
_reg_f8: .byte 0xe7,0x2b,0x06,0x4d,0x5a,0x00,0x42,0xf4
_reg_f9: .byte 0xef,0xfb,0xc9,0x74,0xf3,0xec,0x65,0xc2
_reg_f10:.byte 0xc7,0xf8,0x78,0x3a,0xec,0x2a,0x97,0xf2
_reg_f11:.byte 0x57,0x15,0x76,0x38,0xfa,0xef,0xc8,0xf8
_reg_f12:.byte 0xd5,0xe1,0x4f,0x76,0x82,0xe6,0xbd,0x10
_reg_f13:.byte 0x1c,0xaf,0x58,0xb3,0xa1,0x7d,0x74,0xe1
_reg_f14:.byte 0xd8,0x42,0xe4,0x52,0x42,0xa0,0x93,0x6c
_reg_f15:.byte 0x06,0xad,0x4a,0xc6,0x9d,0x30,0xc2,0x6c
_reg_f16:.byte 0xf8,0xeb,0x69,0x54,0xf6,0x54,0xb8,0x2e
_reg_f17:.byte 0x03,0x63,0xf8,0x77,0xa3,0x7a,0x24,0xaf
_reg_f18:.byte 0x5b,0x0a,0x6c,0xc0,0xc1,0xc8,0xe4,0x37
_reg_f19:.byte 0x60,0x3a,0xf0,0x67,0x6b,0x1e,0x76,0x8d
_reg_f20:.byte 0x76,0xe5,0x18,0xc6,0x24,0xc8,0x32,0x59
_reg_f21:.byte 0xa9,0x97,0x01,0x64,0xd1,0xf7,0xb3,0xa9
_reg_f22:.byte 0x58,0x73,0x92,0xba,0x70,0x66,0xec,0xdb
_reg_f23:.byte 0x3d,0xb1,0xaf,0xdd,0x48,0xf5,0x3e,0xde
_reg_f24:.byte 0x7b,0x32,0x96,0x96,0x3e,0x10,0xe7,0x2c
_reg_f25:.byte 0x86,0x26,0x13,0xce,0x21,0x7c,0x6c,0xf3
_reg_f26:.byte 0x26,0xeb,0xf2,0xf8,0xec,0x33,0xe2,0xe3
_reg_f27:.byte 0x6a,0x8c,0xcf,0x17,0x46,0x60,0x09,0x21
_reg_f28:.byte 0x1d,0xc0,0xa2,0x83,0x28,0xa9,0x4c,0xee
_reg_f29:.byte 0x91,0xd7,0xb2,0x0d,0x6e,0x4b,0xaa,0xbc
_reg_f30:.byte 0x29,0xa6,0xc2,0x7c,0xe4,0xfc,0x60,0xb3
_reg_f31:.byte 0x0b,0x5c,0x08,0x7f,0x42,0x73,0x3d,0x9c
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
    li x1, 0xffffffff80000401    // ra
    li x2, 0x7ffff9d2            // sp
    li x3, 0x35                  // gp
    li x4, 0x8017fea1            // tp
    li x5, 0x7ffff9d2            // t0
    li x6, 0x80006120            // t1
    li x7, 0x0                   // t2
    li x8, 0x801692fa            // fp
    li x9, 0x1                   // s1
    li x10, 0x7ffff9c3           // a0
    li x11, 0x809458f847f69c91   // a1
    li x12, 0xffffffffb3602000   // a2
    li x13, 0x80027d57           // a3
    li x14, 0xffffffffef0c9000   // a4
    li x15, 0x0                  // a5
    li x16, 0x103162542d8b78cd   // a6
    li x17, 0x8018629e           // a7
    li x18, 0x7ffffdb7           // s2
    li x19, 0x8020074b           // s3
    li x20, 0x8017ff88           // s4
    li x21, 0x8018029e           // s5
    li x22, 0x801ff699           // s6
    li x23, 0x8180346eea52fb36   // s7
    li x24, 0x800002d5           // s8
    li x25, 0x7ffffd92           // s9
    li x26, 0x792bddd3159925c3   // s10
    li x27, 0x0                  // s11
    li x28, 0x801807cb           // t3
    li x29, 0x80000120           // t4
    li x30, 0x86d4222cea66d87c   // t5
    li x31, 0x80180119           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x10'}, 'clob': {'x10', 'f21', 'x17'}})
    
    li x17, 0x1ffffc
    and x10, x10, x17
    li x17, 0x7ffffd41
    add x10, x10, x17
    flw f21, 0x2bf(x10)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f21                 0xa9b3f7d1640197a9(-8.502310728454118e-108_d)   0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f21, 0x2bf(x10)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f21                 0xa9b3f7d1640197a9(-8.502310728454118e-108_d)   0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f21, x2, x10
sp(x2)              0x000000007ffff9d2(2147482066)                  0x000000007ffff9d2(2147482066)
a0(x10)             0x00000000801ff701(2149578497)                  0x00000000801ff701(2149578497)
f21                 0xa9b3f7d1640197a9(-8.502310728454118e-108_d)   0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xffffffff80000401(18446744071562068993)        0xffffffff80000401(18446744071562068993)        
sp(x2)              0x000000007ffff9d2(2147482066)                  0x000000007ffff9d2(2147482066)                  
gp(x3)              0x0000000000000035(53)                          0x0000000000000035(53)                          
tp(x4)              0x000000008017fea1(2149056161)                  0x000000008017fea1(2149056161)                  
t0(x5)              0x000000007ffff9d2(2147482066)                  0x000000007ffff9d2(2147482066)                  
t1(x6)              0x0000000080006120(2147508512)                  0x0000000080006120(2147508512)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x00000000801692fa(2148963066)                  0x00000000801692fa(2148963066)                  
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x00000000801ff701(2149578497)                  0x00000000801ff701(2149578497)                  
a1(x11)             0x809458f847f69c91(9265128156790430865)         0x809458f847f69c91(9265128156790430865)         
a2(x12)             0xffffffffb3602000(18446744072424005632)        0xffffffffb3602000(18446744072424005632)        
a3(x13)             0x0000000080027d57(2147646807)                  0x0000000080027d57(2147646807)                  
a4(x14)             0xffffffffef0c9000(18446744073425162240)        0xffffffffef0c9000(18446744073425162240)        
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x103162542d8b78cd(1166821892146559181)         0x103162542d8b78cd(1166821892146559181)         
a7(x17)             0x000000007ffffd41(2147482945)                  0x000000007ffffd41(2147482945)                  
s2(x18)             0x000000007ffffdb7(2147483063)                  0x000000007ffffdb7(2147483063)                  
s3(x19)             0x000000008020074b(2149582667)                  0x000000008020074b(2149582667)                  
s4(x20)             0x000000008017ff88(2149056392)                  0x000000008017ff88(2149056392)                  
s5(x21)             0x000000008018029e(2149057182)                  0x000000008018029e(2149057182)                  
s6(x22)             0x00000000801ff699(2149578393)                  0x00000000801ff699(2149578393)                  
s7(x23)             0x8180346eea52fb36(9331516078894021430)         0x8180346eea52fb36(9331516078894021430)         
s8(x24)             0x00000000800002d5(2147484373)                  0x00000000800002d5(2147484373)                  
s9(x25)             0x000000007ffffd92(2147483026)                  0x000000007ffffd92(2147483026)                  
s10(x26)            0x792bddd3159925c3(8731316201258034627)         0x792bddd3159925c3(8731316201258034627)         
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x00000000801807cb(2149058507)                  0x00000000801807cb(2149058507)                  
t4(x29)             0x0000000080000120(2147483936)                  0x0000000080000120(2147483936)                  
t5(x30)             0x86d4222cea66d87c(9715427872451516540)         0x86d4222cea66d87c(9715427872451516540)         
t6(x31)             0x0000000080180119(2149056793)                  0x0000000080180119(2149056793)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            12f4659475c91d612d8b3d5b212e747fd88b1c58        12f4659475c91d612d8b3d5b212e747fd88b1c58        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800007c4(2147485636)                  0x00000000800007c4(2147485636)                  
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
f0                  0x764b2d74e31c1198(6.685852472095025e+261_d)    0x764b2d74e31c1198(6.685852472095025e+261_d)    
f1                  0x8abe791c9f787e7e(-6.342204606431999e-257_d)   0x8abe791c9f787e7e(-6.342204606431999e-257_d)   
f2                  0xd62ab524c13ce216(-1.2250765096343867e+107_d)  0xd62ab524c13ce216(-1.2250765096343867e+107_d)  
f3                  0x65154819fe6f8d48(8.623879301222084e+178_d)    0x65154819fe6f8d48(8.623879301222084e+178_d)    
f4                  0xf3caa33a90591681(-5.959937664828583e+249_d)   0xf3caa33a90591681(-5.959937664828583e+249_d)   
f5                  0xa16dfbe41c42506a(-1.1724679354921434e-147_d)  0xa16dfbe41c42506a(-1.1724679354921434e-147_d)  
f6                  0x136113f0ee3a240e(2.477008229552581e-215_d)    0x136113f0ee3a240e(2.477008229552581e-215_d)    
f7                  0x3b71b3e13def1811(2.3429269696278177e-22_d)    0x3b71b3e13def1811(2.3429269696278177e-22_d)    
f8                  0xf442005a4d062be7(-1.0310794631261e+252_d)     0xf442005a4d062be7(-1.0310794631261e+252_d)     
f9                  0xc265ecf374c9fbef(-753357530703.8729_d)        0xc265ecf374c9fbef(-753357530703.8729_d)        
f10                 0xf2972aec3a78f8c7(-9.886869653030081e+243_d)   0xf2972aec3a78f8c7(-9.886869653030081e+243_d)   
f11                 0xf8c8effa38761557(-6.745240720017734e+273_d)   0xf8c8effa38761557(-6.745240720017734e+273_d)   
f12                 0x10bde682764fe1d5(4.9303835206551954e-228_d)   0x10bde682764fe1d5(4.9303835206551954e-228_d)   
f13                 0xe1747da1b358af1c(-2.8808159862245657e+161_d)  0xe1747da1b358af1c(-2.8808159862245657e+161_d)  
f14                 0x6c93a04252e442d8(1.0571314220529383e+215_d)   0x6c93a04252e442d8(1.0571314220529383e+215_d)   
f15                 0x6cc2309dc64aad06(7.838219077080749e+215_d)    0x6cc2309dc64aad06(7.838219077080749e+215_d)    
f16                 0x2eb854f65469ebf8(1.2524977257284519e-83_d)    0x2eb854f65469ebf8(1.2524977257284519e-83_d)    
f17                 0xaf247aa377f86303(-1.349339192677445e-81_d)    0xaf247aa377f86303(-1.349339192677445e-81_d)    
f18                 0x37e4c8c1c06c0a5b(1.9087279084208514e-39_d)    0x37e4c8c1c06c0a5b(1.9087279084208514e-39_d)    
f19                 0x8d761e6b67f03a60(-8.098518910560484e-244_d)   0x8d761e6b67f03a60(-8.098518910560484e-244_d)   
f20                 0x5932c824c618e576(4.849932948500033e+121_d)    0x5932c824c618e576(4.849932948500033e+121_d)    
f21                 0xa9b3f7d1640197a9(-8.502310728454118e-108_d)   0xffffffff00000000(0.0_s)                       X
f22                 0xdbec6670ba927358(-6.450729476052083e+134_d)   0xdbec6670ba927358(-6.450729476052083e+134_d)   
f23                 0xde3ef548ddafb13d(-9.664353833149178e+145_d)   0xde3ef548ddafb13d(-9.664353833149178e+145_d)   
f24                 0x2ce7103e9696327b(2.2113409439211327e-92_d)    0x2ce7103e9696327b(2.2113409439211327e-92_d)    
f25                 0xf36c7c21ce132686(-9.958203752559971e+247_d)   0xf36c7c21ce132686(-9.958203752559971e+247_d)   
f26                 0xe3e233ecf8f2eb26(-1.40691075158795e+173_d)    0xe3e233ecf8f2eb26(-1.40691075158795e+173_d)    
f27                 0x2109604617cf8c6a(1.5504455516706233e-149_d)   0x2109604617cf8c6a(1.5504455516706233e-149_d)   
f28                 0xee4ca92883a2c01d(-2.0720237339543465e+223_d)  0xee4ca92883a2c01d(-2.0720237339543465e+223_d)  
f29                 0xbcaa4b6e0db2d791(-1.824557729436319e-16_d)    0xbcaa4b6e0db2d791(-1.824557729436319e-16_d)    
f30                 0xb360fce47cc2a629(-3.3036162900177544e-61_d)   0xb360fce47cc2a629(-3.3036162900177544e-61_d)   
f31                 0x9c3d73427f085c0b(-1.1907243600628238e-172_d)  0x9c3d73427f085c0b(-1.1907243600628238e-172_d)  
STATES DIFFER: True
```

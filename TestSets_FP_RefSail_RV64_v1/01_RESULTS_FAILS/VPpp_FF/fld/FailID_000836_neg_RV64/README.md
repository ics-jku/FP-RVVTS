# FailID_000836 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 836
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
_reg_f0: .byte 0x83,0x11,0xcf,0x6a,0x78,0x0b,0xb5,0xe5
_reg_f1: .byte 0x4f,0x3d,0x2e,0xd9,0x1b,0xd4,0x66,0x93
_reg_f2: .byte 0x76,0x20,0x69,0x6b,0x91,0xd7,0x69,0x44
_reg_f3: .byte 0x6d,0xd9,0x2a,0x4f,0xfa,0x89,0x2f,0x6b
_reg_f4: .byte 0xa1,0xb3,0x8b,0xc1,0xa2,0x07,0x90,0x3d
_reg_f5: .byte 0x73,0x4b,0x74,0x88,0x92,0x1b,0xb2,0x8a
_reg_f6: .byte 0x03,0xb4,0x94,0x38,0x63,0x35,0xb7,0x8d
_reg_f7: .byte 0x95,0xeb,0x5e,0xf7,0x1c,0x8d,0xd9,0xda
_reg_f8: .byte 0x59,0x52,0x66,0xea,0x97,0xaa,0x8a,0x3b
_reg_f9: .byte 0x2b,0x1b,0x98,0xf9,0x18,0x84,0x9f,0xe8
_reg_f10:.byte 0x0a,0xeb,0xaa,0x8c,0xd4,0x20,0x5b,0x17
_reg_f11:.byte 0x24,0x7d,0x84,0x98,0x60,0x9f,0xdd,0x67
_reg_f12:.byte 0xeb,0x91,0x9d,0x69,0x42,0xa5,0x64,0x47
_reg_f13:.byte 0xcf,0x94,0xde,0xb1,0xcc,0x26,0xc8,0xde
_reg_f14:.byte 0x8a,0x86,0x2d,0xbb,0xa1,0xf7,0x97,0xc6
_reg_f15:.byte 0xf8,0x37,0x16,0xd8,0x0e,0xc7,0x15,0xbb
_reg_f16:.byte 0x7c,0x6b,0x12,0xb1,0xbf,0x2e,0xeb,0xd0
_reg_f17:.byte 0x85,0x5f,0x1c,0xbc,0xed,0x2f,0x76,0x0c
_reg_f18:.byte 0x92,0x08,0xb0,0xb6,0x40,0x70,0x23,0x9a
_reg_f19:.byte 0xe5,0xc2,0x8c,0x98,0x6b,0x64,0xd4,0xc1
_reg_f20:.byte 0x0e,0x52,0x1c,0x2a,0x14,0x2f,0xdf,0x4a
_reg_f21:.byte 0xbb,0x8c,0xf6,0x70,0x93,0xca,0x45,0x90
_reg_f22:.byte 0xc6,0x35,0x94,0x66,0x66,0xa2,0x56,0xd5
_reg_f23:.byte 0x40,0x1c,0xb8,0x29,0xa9,0xb5,0xa8,0x08
_reg_f24:.byte 0x5b,0x81,0xb8,0xf2,0xab,0xa0,0x76,0x71
_reg_f25:.byte 0xe9,0x5e,0x86,0x37,0x90,0x13,0xec,0x80
_reg_f26:.byte 0x8b,0x3b,0xa6,0x01,0x35,0xcc,0xe9,0xdb
_reg_f27:.byte 0x9d,0xa5,0x63,0xd5,0x67,0xe5,0xf2,0x7b
_reg_f28:.byte 0xf1,0x46,0xb2,0x9e,0xf5,0x51,0xcc,0xe9
_reg_f29:.byte 0xfa,0xcb,0x22,0x87,0x03,0xa2,0x1a,0x9c
_reg_f30:.byte 0x48,0x4f,0xf1,0x67,0x3c,0x0b,0x98,0x15
_reg_f31:.byte 0x8c,0x60,0xda,0x29,0xb2,0x97,0xd0,0x8c
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x40
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xdea4afe7cfbebbc0    // ra
    li x2, 0xcb2d5333a5bc951f    // sp
    li x3, 0x5a5046cc199a11d5    // gp
    li x4, 0xcee535ebf2255db4    // tp
    li x5, 0xbc17db5814d22588    // t0
    li x6, 0x84fc2b439af91522    // t1
    li x7, 0x8df9dcbc3e7c2f2d    // t2
    li x8, 0x63fd75c2ecd2659     // fp
    li x9, 0x99c9bfd8b85494e9    // s1
    li x10, 0x82bbc45bdb725e9a   // a0
    li x11, 0x53d731003b583f92   // a1
    li x12, 0x21e98e4404281401   // a2
    li x13, 0xf1940902e93c5112   // a3
    li x14, 0xed955d3ccad8980c   // a4
    li x15, 0x58e8a8ba13aefcbe   // a5
    li x16, 0xbf699225d26dba38   // a6
    li x17, 0x8e4ad43f6d0c72a2   // a7
    li x18, 0x470c4848bcd7e8fd   // s2
    li x19, 0x480748fc09aaae4a   // s3
    li x20, 0xa5dc3fe1480326cd   // s4
    li x21, 0xad932cf0fd4daae    // s5
    li x22, 0xa0fb2d85db6d9800   // s6
    li x23, 0xac9d9e591eb6303b   // s7
    li x24, 0x4cfe3ca04d276ac3   // s8
    li x25, 0x535e963a74f97a0b   // s9
    li x26, 0xf707faee17c3c776   // s10
    li x27, 0xf0674fb3b36ad584   // s11
    li x28, 0xb11c6008968ccd3c   // t3
    li x29, 0x595c700ad1a07d70   // t4
    li x30, 0xe6ec80d6f10b2c39   // t5
    li x31, 0x5104e51dce4072c1   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x3'}, 'clob': {'f12', 'x3', 'x14'}})
    
    li x14, 0x1ffff8
    and x3, x3, x14
    li x14, 0x7ffffc5f
    add x3, x3, x14
    fld f12, 0x3a1(x3)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f12                 0x4764a542699d91eb(8.575823720035319e+35_d)     0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f12, 0x3a1(x3)
+========================================================================================================================+
Attributes:  special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f12                 0x4764a542699d91eb(8.575823720035319e+35_d)     0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f12, x3, a1, x3
gp(x3)              0x00000000801a0e2f(2149191215)                  0x00000000801a0e2f(2149191215)
f12                 0x4764a542699d91eb(8.575823720035319e+35_d)     0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xdea4afe7cfbebbc0(16043141182758239168)        0xdea4afe7cfbebbc0(16043141182758239168)        
sp(x2)              0xcb2d5333a5bc951f(14640449444940387615)        0xcb2d5333a5bc951f(14640449444940387615)        
gp(x3)              0x00000000801a0e2f(2149191215)                  0x00000000801a0e2f(2149191215)                  
tp(x4)              0xcee535ebf2255db4(14908381428976016820)        0xcee535ebf2255db4(14908381428976016820)        
t0(x5)              0xbc17db5814d22588(13553542774947718536)        0xbc17db5814d22588(13553542774947718536)        
t1(x6)              0x84fc2b439af91522(9582581676500391202)         0x84fc2b439af91522(9582581676500391202)         
t2(x7)              0x8df9dcbc3e7c2f2d(10230450729609080621)        0x8df9dcbc3e7c2f2d(10230450729609080621)        
fp(x8)              0x063fd75c2ecd2659(450315278682498649)          0x063fd75c2ecd2659(450315278682498649)          
s1(x9)              0x99c9bfd8b85494e9(11081599295648208105)        0x99c9bfd8b85494e9(11081599295648208105)        
a0(x10)             0x82bbc45bdb725e9a(9420338944378298010)         0x82bbc45bdb725e9a(9420338944378298010)         
a1(x11)             0x53d731003b583f92(6041351302206209938)         0x53d731003b583f92(6041351302206209938)         
a2(x12)             0x21e98e4404281401(2443640695603860481)         0x21e98e4404281401(2443640695603860481)         
a3(x13)             0xf1940902e93c5112(17407548367801438482)        0xf1940902e93c5112(17407548367801438482)        
a4(x14)             0x000000007ffffc5f(2147482719)                  0x000000007ffffc5f(2147482719)                  
a5(x15)             0x58e8a8ba13aefcbe(6406555987082149054)         0x58e8a8ba13aefcbe(6406555987082149054)         
a6(x16)             0xbf699225d26dba38(13792716024940706360)        0xbf699225d26dba38(13792716024940706360)        
a7(x17)             0x8e4ad43f6d0c72a2(10253240870539915938)        0x8e4ad43f6d0c72a2(10253240870539915938)        
s2(x18)             0x470c4848bcd7e8fd(5119546353656523005)         0x470c4848bcd7e8fd(5119546353656523005)         
s3(x19)             0x480748fc09aaae4a(5190197342898925130)         0x480748fc09aaae4a(5190197342898925130)         
s4(x20)             0xa5dc3fe1480326cd(11951497747942811341)        0xa5dc3fe1480326cd(11951497747942811341)        
s5(x21)             0x0ad932cf0fd4daae(781711875230718638)          0x0ad932cf0fd4daae(781711875230718638)          
s6(x22)             0xa0fb2d85db6d9800(11599915318158137344)        0xa0fb2d85db6d9800(11599915318158137344)        
s7(x23)             0xac9d9e591eb6303b(12438271851471712315)        0xac9d9e591eb6303b(12438271851471712315)        
s8(x24)             0x4cfe3ca04d276ac3(5547938450153892547)         0x4cfe3ca04d276ac3(5547938450153892547)         
s9(x25)             0x535e963a74f97a0b(6007404130773596683)         0x535e963a74f97a0b(6007404130773596683)         
s10(x26)            0xf707faee17c3c776(17800471952713041782)        0xf707faee17c3c776(17800471952713041782)        
s11(x27)            0xf0674fb3b36ad584(17322902124931765636)        0xf0674fb3b36ad584(17322902124931765636)        
t3(x28)             0xb11c6008968ccd3c(12762181034062957884)        0xb11c6008968ccd3c(12762181034062957884)        
t4(x29)             0x595c700ad1a07d70(6439144759001906544)         0x595c700ad1a07d70(6439144759001906544)         
t5(x30)             0xe6ec80d6f10b2c39(16639816383882538041)        0xe6ec80d6f10b2c39(16639816383882538041)        
t6(x31)             0x5104e51dce4072c1(5838042933156147905)         0x5104e51dce4072c1(5838042933156147905)         

STATE               REF                                             DUT                                             DIFF
xmemhash            e8b86098122b9149d128c699c23c5eeeac6efa80        e8b86098122b9149d128c699c23c5eeeac6efa80        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800009f4(2147486196)                  0x00000000800009f4(2147486196)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000040(64)                          0x0000000000000040(64)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xe5b50b786acf1183(-8.732575085061292e+181_d)   0xe5b50b786acf1183(-8.732575085061292e+181_d)   
f1                  0x9366d41bd92e3d4f(-3.3110934255220594e-215_d)  0x9366d41bd92e3d4f(-3.3110934255220594e-215_d)  
f2                  0x4469d7916b692076(3.8136153322542135e+21_d)    0x4469d7916b692076(3.8136153322542135e+21_d)    
f3                  0x6b2f89fa4f2ad96d(2.0251379174662537e+208_d)   0x6b2f89fa4f2ad96d(2.0251379174662537e+208_d)   
f4                  0x3d9007a2c18bb3a1(3.6447607294693166e-12_d)    0x3d9007a2c18bb3a1(3.6447607294693166e-12_d)    
f5                  0x8ab21b9288744b73(-3.768661354559941e-257_d)   0x8ab21b9288744b73(-3.768661354559941e-257_d)   
f6                  0x8db735633894b403(-1.3596008341984277e-242_d)  0x8db735633894b403(-1.3596008341984277e-242_d)  
f7                  0xdad98d1cf75eeb95(-4.4278188954227777e+129_d)  0xdad98d1cf75eeb95(-4.4278188954227777e+129_d)  
f8                  0x3b8aaa97ea665259(7.058532158926849e-22_d)     0x3b8aaa97ea665259(7.058532158926849e-22_d)     
f9                  0xe89f8418f9981b2b(-9.202554001965086e+195_d)   0xe89f8418f9981b2b(-9.202554001965086e+195_d)   
f10                 0x175b20d48caaeb0a(3.629146555941224e-196_d)    0x175b20d48caaeb0a(3.629146555941224e-196_d)    
f11                 0x67dd9f6098847d24(2.111737593781895e+192_d)    0x67dd9f6098847d24(2.111737593781895e+192_d)    
f12                 0x4764a542699d91eb(8.575823720035319e+35_d)     0x0000000000000000(0.0_d)                       X
f13                 0xdec826ccb1de94cf(-3.8602291308163043e+148_d)  0xdec826ccb1de94cf(-3.8602291308163043e+148_d)  
f14                 0xc697f7a1bb2d868a(-1.2152870759892738e+32_d)   0xc697f7a1bb2d868a(-1.2152870759892738e+32_d)   
f15                 0xbb15c70ed81637f8(-4.503495975411748e-24_d)    0xbb15c70ed81637f8(-4.503495975411748e-24_d)    
f16                 0xd0eb2ebfb1126b7c(-6.446144492211081e+81_d)    0xd0eb2ebfb1126b7c(-6.446144492211081e+81_d)    
f17                 0x0c762fedbc1c5f85(1.2395570086590742e-248_d)   0x0c762fedbc1c5f85(1.2395570086590742e-248_d)   
f18                 0x9a237040b6b00892(-9.14945255019502e-183_d)    0x9a237040b6b00892(-9.14945255019502e-183_d)    
f19                 0xc1d4646b988cc2e5(-1368501858.1993954_d)       0xc1d4646b988cc2e5(-1368501858.1993954_d)       
f20                 0x4adf2f142a1c520e(4.6669130758905514e+52_d)    0x4adf2f142a1c520e(4.6669130758905514e+52_d)    
f21                 0x9045ca9370f68cbb(-2.807221684975501e-230_d)   0x9045ca9370f68cbb(-2.807221684975501e-230_d)   
f22                 0xd556a266669435c6(-1.2673805605654955e+103_d)  0xd556a266669435c6(-1.2673805605654955e+103_d)  
f23                 0x08a8b5a929b81c40(5.9868694639295475e-267_d)   0x08a8b5a929b81c40(5.9868694639295475e-267_d)   
f24                 0x7176a0abf2b8815b(3.68362601435912e+238_d)     0x7176a0abf2b8815b(3.68362601435912e+238_d)     
f25                 0x80ec139037865ee9(-3.1985718620627694e-304_d)  0x80ec139037865ee9(-3.1985718620627694e-304_d)  
f26                 0xdbe9cc3501a63b8b(-5.859611122888421e+134_d)   0xdbe9cc3501a63b8b(-5.859611122888421e+134_d)   
f27                 0x7bf2e567d563a59d(1.1509286272135676e+289_d)   0x7bf2e567d563a59d(1.1509286272135676e+289_d)   
f28                 0xe9cc51f59eb246f1(-4.335535323009277e+201_d)   0xe9cc51f59eb246f1(-4.335535323009277e+201_d)   
f29                 0x9c1aa2038722cbfa(-2.6920332248350926e-173_d)  0x9c1aa2038722cbfa(-2.6920332248350926e-173_d)  
f30                 0x15980b3c67f14f48(1.198250718626497e-204_d)    0x15980b3c67f14f48(1.198250718626497e-204_d)    
f31                 0x8cd097b229da608c(-5.932763297392054e-247_d)   0x8cd097b229da608c(-5.932763297392054e-247_d)   
STATES DIFFER: True
```

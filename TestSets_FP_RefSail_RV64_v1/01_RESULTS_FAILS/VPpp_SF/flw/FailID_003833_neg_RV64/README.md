# FailID_003833 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3833
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
_reg_f0: .byte 0x48,0x47,0xe3,0xe9,0x8f,0xad,0x05,0xe5
_reg_f1: .byte 0x40,0x2b,0x38,0x6e,0x19,0xc8,0xc1,0x9e
_reg_f2: .byte 0xef,0x9d,0x11,0x89,0x0a,0x13,0x15,0x41
_reg_f3: .byte 0x06,0x79,0xd4,0xd7,0x42,0x4a,0x0c,0xb6
_reg_f4: .byte 0x98,0x2e,0x3f,0xd6,0x95,0x61,0x6f,0x49
_reg_f5: .byte 0xd2,0x32,0xfe,0xe3,0xc0,0x8d,0x25,0x53
_reg_f6: .byte 0x81,0xcc,0x89,0xec,0xac,0x74,0x38,0x04
_reg_f7: .byte 0x2b,0x87,0xd2,0xab,0x9d,0xbb,0x10,0x6c
_reg_f8: .byte 0x47,0x87,0x9f,0x34,0x64,0x22,0x37,0xdc
_reg_f9: .byte 0xc6,0x3b,0x35,0x37,0xe0,0x1e,0xea,0x62
_reg_f10:.byte 0x4d,0xc2,0x2b,0x45,0x6c,0x01,0xa5,0x6a
_reg_f11:.byte 0x04,0xcd,0x72,0xd0,0xcf,0x04,0x34,0xc1
_reg_f12:.byte 0xe7,0x52,0x19,0x56,0x63,0xb7,0x4a,0xb9
_reg_f13:.byte 0x5b,0x42,0x9e,0xba,0x81,0xf2,0x8c,0xca
_reg_f14:.byte 0xd3,0x64,0xd4,0x05,0xc7,0x7d,0x7c,0x12
_reg_f15:.byte 0x4c,0x02,0x96,0x3c,0x91,0x84,0xca,0xee
_reg_f16:.byte 0x59,0xbc,0xea,0xdd,0x8b,0x9e,0x9e,0x22
_reg_f17:.byte 0xd9,0x54,0x40,0xc8,0x54,0x9e,0x08,0x85
_reg_f18:.byte 0x6d,0xb4,0x88,0x69,0xc0,0xd8,0x6a,0x0f
_reg_f19:.byte 0xc4,0x6e,0x43,0xe5,0x39,0x25,0x84,0x89
_reg_f20:.byte 0x04,0xa2,0xa2,0xeb,0x53,0xb8,0x0d,0xbc
_reg_f21:.byte 0xed,0x50,0x1f,0x0a,0xef,0xe9,0x62,0x94
_reg_f22:.byte 0xf1,0x76,0x6f,0x87,0x14,0xb3,0xb8,0xc8
_reg_f23:.byte 0x3e,0x45,0x49,0xb3,0x63,0x6c,0xf4,0x35
_reg_f24:.byte 0xd6,0x02,0x42,0x8d,0x02,0xf2,0xef,0x7d
_reg_f25:.byte 0x07,0x54,0x85,0x65,0x5c,0x4b,0x45,0xc7
_reg_f26:.byte 0x11,0x67,0xe5,0xbe,0x53,0x84,0xcf,0x0d
_reg_f27:.byte 0xcf,0x74,0xd5,0x63,0x6b,0x2c,0xbe,0x91
_reg_f28:.byte 0x1c,0xaf,0xcd,0xa8,0x30,0x6e,0x0a,0xfd
_reg_f29:.byte 0x4a,0x27,0xaf,0x20,0x52,0x12,0xb7,0x57
_reg_f30:.byte 0xca,0x13,0x93,0x38,0x51,0x0c,0x97,0xd6
_reg_f31:.byte 0x51,0xdc,0x63,0x1f,0xfb,0x78,0x12,0xab
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x80
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x33a5601765b05908    // sp
    li x3, 0x0                   // gp
    li x4, 0x3ce4e356c8c49c9     // tp
    li x5, 0x801eac77            // t0
    li x6, 0x93b0e99e2a85c9cd    // t1
    li x7, 0xf91af8ea26b91905    // t2
    li x8, 0xad81844571b2f67c    // fp
    li x9, 0x1c0fa47d2cfa7e10    // s1
    li x10, 0x85adf40e1a4001dd   // a0
    li x11, 0x4e65c132f09fdc16   // a1
    li x12, 0x4370eb28d84948b5   // a2
    li x13, 0x8a9137d6df94fa1    // a3
    li x14, 0xcf910d001e58d25e   // a4
    li x15, 0x7ffffdef           // a5
    li x16, 0x80168405           // a6
    li x17, 0x7fa234718bfc8b14   // a7
    li x18, 0xdd69f93d1b19f1ef   // s2
    li x19, 0x3ac81d121443fbf4   // s3
    li x20, 0x719d8621b59b4449   // s4
    li x21, 0x8a56aa763a9a89ec   // s5
    li x22, 0x76a1fced61bffab9   // s6
    li x23, 0x81dfae14d8155784   // s7
    li x24, 0x3fbd33261da647f    // s8
    li x25, 0xab7d23bd441b35c0   // s9
    li x26, 0x3d4952bd0fd0568a   // s10
    li x27, 0x2e7f538305d3a794   // s11
    li x28, 0xf17eb71f10de6afe   // t3
    li x29, 0x8d73ebe2ac8ca5a0   // t4
    li x30, 0x7ffff8c3           // t5
    li x31, 0xb00dd4042efd2b7f   // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x13'}, 'clob': {'x13', 'f0', 'x25'}})
    
    li x25, 0x1ffffc
    and x13, x13, x25
    li x25, 0x7ffffe9a
    add x13, x13, x25
    flw f0, 0x166(x13)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f0                  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f0, 0x166(x13)
+========================================================================================================================+
Attributes:  special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f0                  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f0, x166, x13
a3(x13)             0x0000000080194e3a(2149142074)                  0x0000000080194e3a(2149142074)
f0                  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x33a5601765b05908(3721486320698153224)         0x33a5601765b05908(3721486320698153224)         
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x03ce4e356c8c49c9(274242618677545417)          0x03ce4e356c8c49c9(274242618677545417)          
t0(x5)              0x00000000801eac77(2149493879)                  0x00000000801eac77(2149493879)                  
t1(x6)              0x93b0e99e2a85c9cd(10642262785003997645)        0x93b0e99e2a85c9cd(10642262785003997645)        
t2(x7)              0xf91af8ea26b91905(17949932949394233605)        0xf91af8ea26b91905(17949932949394233605)        
fp(x8)              0xad81844571b2f67c(12502419474352371324)        0xad81844571b2f67c(12502419474352371324)        
s1(x9)              0x1c0fa47d2cfa7e10(2022015615245123088)         0x1c0fa47d2cfa7e10(2022015615245123088)         
a0(x10)             0x85adf40e1a4001dd(9632623519422480861)         0x85adf40e1a4001dd(9632623519422480861)         
a1(x11)             0x4e65c132f09fdc16(5649133732135689238)         0x4e65c132f09fdc16(5649133732135689238)         
a2(x12)             0x4370eb28d84948b5(4859642558592665781)         0x4370eb28d84948b5(4859642558592665781)         
a3(x13)             0x0000000080194e3a(2149142074)                  0x0000000080194e3a(2149142074)                  
a4(x14)             0xcf910d001e58d25e(14956750131634426462)        0xcf910d001e58d25e(14956750131634426462)        
a5(x15)             0x000000007ffffdef(2147483119)                  0x000000007ffffdef(2147483119)                  
a6(x16)             0x0000000080168405(2148959237)                  0x0000000080168405(2148959237)                  
a7(x17)             0x7fa234718bfc8b14(9196971051328506644)         0x7fa234718bfc8b14(9196971051328506644)         
s2(x18)             0xdd69f93d1b19f1ef(15954557195779699183)        0xdd69f93d1b19f1ef(15954557195779699183)        
s3(x19)             0x3ac81d121443fbf4(4235667413028568052)         0x3ac81d121443fbf4(4235667413028568052)         
s4(x20)             0x719d8621b59b4449(8186847176968324169)         0x719d8621b59b4449(8186847176968324169)         
s5(x21)             0x8a56aa763a9a89ec(9968342249997240812)         0x8a56aa763a9a89ec(9968342249997240812)         
s6(x22)             0x76a1fced61bffab9(8548391664203332281)         0x76a1fced61bffab9(8548391664203332281)         
s7(x23)             0x81dfae14d8155784(9358389955247036292)         0x81dfae14d8155784(9358389955247036292)         
s8(x24)             0x03fbd33261da647f(287055214611686527)          0x03fbd33261da647f(287055214611686527)          
s9(x25)             0x000000007ffffe9a(2147483290)                  0x000000007ffffe9a(2147483290)                  
s10(x26)            0x3d4952bd0fd0568a(4416151881581090442)         0x3d4952bd0fd0568a(4416151881581090442)         
s11(x27)            0x2e7f538305d3a794(3350488469990516628)         0x2e7f538305d3a794(3350488469990516628)         
t3(x28)             0xf17eb71f10de6afe(17401547354261056254)        0xf17eb71f10de6afe(17401547354261056254)        
t4(x29)             0x8d73ebe2ac8ca5a0(10192749740459599264)        0x8d73ebe2ac8ca5a0(10192749740459599264)        
t5(x30)             0x000000007ffff8c3(2147481795)                  0x000000007ffff8c3(2147481795)                  
t6(x31)             0xb00dd4042efd2b7f(12686028839805856639)        0xb00dd4042efd2b7f(12686028839805856639)        

STATE               REF                                             DUT                                             DIFF
xmemhash            5bf5d79b62e00b63a38fbafb704e3e7c83331dbc        5bf5d79b62e00b63a38fbafb704e3e7c83331dbc        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000954(2147486036)                  0x0000000080000954(2147486036)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000080(128)                         0x0000000000000080(128)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  0xffffffff00000000(0.0_s)                       X
f1                  0x9ec1c8196e382b40(-1.580971661282594e-160_d)   0x9ec1c8196e382b40(-1.580971661282594e-160_d)   
f2                  0x4115130a89119def(345282.63385626575_d)        0x4115130a89119def(345282.63385626575_d)        
f3                  0xb60c4a42d7d47906(-2.4196074881082802e-48_d)   0xb60c4a42d7d47906(-2.4196074881082802e-48_d)   
f4                  0x496f6195d63f2e98(5.598591837962817e+45_d)     0x496f6195d63f2e98(5.598591837962817e+45_d)     
f5                  0x53258dc0e3fe32d2(3.512456982830312e+92_d)     0x53258dc0e3fe32d2(3.512456982830312e+92_d)     
f6                  0x043874acec89cc81(2.50948954357864e-288_d)     0x043874acec89cc81(2.50948954357864e-288_d)     
f7                  0x6c10bb9dabd2872b(3.520687781263141e+212_d)    0x6c10bb9dabd2872b(3.520687781263141e+212_d)    
f8                  0xdc372264349f8747(-1.6814935274538292e+136_d)  0xdc372264349f8747(-1.6814935274538292e+136_d)  
f9                  0x62ea1ee037353bc6(3.080568624107483e+168_d)    0x62ea1ee037353bc6(3.080568624107483e+168_d)    
f10                 0x6aa5016c452bc24d(5.268673489679908e+205_d)    0x6aa5016c452bc24d(5.268673489679908e+205_d)    
f11                 0xc13404cfd072cd04(-1311951.8142517218_d)       0xc13404cfd072cd04(-1311951.8142517218_d)       
f12                 0xb94ab763561952e7(-1.0290767353988184e-32_d)   0xb94ab763561952e7(-1.0290767353988184e-32_d)   
f13                 0xca8cf281ba9e425b(-1.3538084692695443e+51_d)   0xca8cf281ba9e425b(-1.3538084692695443e+51_d)   
f14                 0x127c7dc705d464d3(1.2611179739675923e-219_d)   0x127c7dc705d464d3(1.2611179739675923e-219_d)   
f15                 0xeeca84913c96024c(-4.907778278804439e+225_d)   0xeeca84913c96024c(-4.907778278804439e+225_d)   
f16                 0x229e9e8bddeabc59(6.2773684592087685e-142_d)   0x229e9e8bddeabc59(6.2773684592087685e-142_d)   
f17                 0x85089e54c84054d9(-2.0694520211768955e-284_d)  0x85089e54c84054d9(-2.0694520211768955e-284_d)  
f18                 0x0f6ad8c06988b46d(2.1108825482638558e-234_d)   0x0f6ad8c06988b46d(2.1108825482638558e-234_d)   
f19                 0x89842539e5436ec4(-7.997053569172173e-263_d)   0x89842539e5436ec4(-7.997053569172173e-263_d)   
f20                 0xbc0db853eba2a204(-2.013907603808987e-19_d)    0xbc0db853eba2a204(-2.013907603808987e-19_d)    
f21                 0x9462e9ef0a1f50ed(-1.7978436354045786e-210_d)  0x9462e9ef0a1f50ed(-1.7978436354045786e-210_d)  
f22                 0xc8b8b314876f76f1(-2.1516326938218565e+42_d)   0xc8b8b314876f76f1(-2.1516326938218565e+42_d)   
f23                 0x35f46c63b349453e(8.733909265279227e-49_d)     0x35f46c63b349453e(8.733909265279227e-49_d)     
f24                 0x7deff2028d4202d6(4.178432498114332e+298_d)    0x7deff2028d4202d6(4.178432498114332e+298_d)    
f25                 0xc7454b5c65855407(-2.21133470319253e+35_d)     0xc7454b5c65855407(-2.21133470319253e+35_d)     
f26                 0x0dcf8453bee56711(3.6926405312250583e-242_d)   0x0dcf8453bee56711(3.6926405312250583e-242_d)   
f27                 0x91be2c6b63d574cf(-3.2606869983951326e-223_d)  0x91be2c6b63d574cf(-3.2606869983951326e-223_d)  
f28                 0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  0xfd0a6e30a8cdaf1c(-2.1100367023637902e+294_d)  
f29                 0x57b7125220af274a(3.551038958765134e+114_d)    0x57b7125220af274a(3.551038958765134e+114_d)    
f30                 0xd6970c51389313ca(-1.353236949152047e+109_d)   0xd6970c51389313ca(-1.353236949152047e+109_d)   
f31                 0xab1278fb1f63dc51(-3.299051267616785e-101_d)   0xab1278fb1f63dc51(-3.299051267616785e-101_d)   
STATES DIFFER: True
```

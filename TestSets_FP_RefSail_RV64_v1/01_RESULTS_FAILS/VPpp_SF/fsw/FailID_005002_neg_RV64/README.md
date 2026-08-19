# FailID_005002 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 5002
* Isolated failing instruction: `fsw`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0xbb,0x9f,0x0f,0x0b,0xc6,0x70,0x56,0xdf
_reg_f2: .byte 0x57,0x6a,0x24,0x58,0xe6,0xbf,0x71,0x1a
_reg_f3: .byte 0x75,0xa1,0xa7,0x04,0xc3,0x65,0x6b,0xc2
_reg_f4: .byte 0x25,0x74,0x3a,0xcc,0x66,0x9f,0xf9,0x92
_reg_f5: .byte 0xfa,0xfb,0xd2,0xc2,0xa7,0xff,0x83,0x57
_reg_f6: .byte 0xfe,0x23,0x18,0x60,0xca,0xd9,0x45,0x61
_reg_f7: .byte 0x95,0xcf,0x3e,0x47,0xdd,0x85,0xa9,0x3b
_reg_f8: .byte 0x17,0x43,0x64,0x81,0x03,0xe0,0x8c,0xc1
_reg_f9: .byte 0x5e,0xa8,0x2a,0x48,0xf4,0xb7,0xd9,0xce
_reg_f10:.byte 0x5a,0x7c,0x7c,0x84,0x6d,0x5a,0x28,0xba
_reg_f11:.byte 0x76,0x3f,0x2c,0xbd,0xce,0xff,0xb7,0xbf
_reg_f12:.byte 0xff,0x09,0x99,0xc5,0x1e,0xc2,0xaf,0x50
_reg_f13:.byte 0xfb,0x9f,0xd7,0xf6,0xf6,0x34,0xd1,0x47
_reg_f14:.byte 0x1f,0x0e,0x49,0xca,0x93,0x07,0x92,0xd1
_reg_f15:.byte 0x04,0xd7,0x03,0x59,0x0c,0x28,0x5a,0x18
_reg_f16:.byte 0xdb,0x1b,0xb6,0x3c,0xae,0xb5,0x4f,0x1c
_reg_f17:.byte 0x59,0xba,0x5a,0xa6,0x19,0x9b,0xc5,0x35
_reg_f18:.byte 0x12,0x31,0x7a,0xd8,0xc3,0x97,0x7b,0x61
_reg_f19:.byte 0xc1,0x80,0x3a,0xeb,0xf4,0xf0,0x38,0xeb
_reg_f20:.byte 0xe7,0x1f,0xb3,0x8c,0xe2,0xc6,0x9b,0x22
_reg_f21:.byte 0xc9,0x04,0x05,0xf7,0xbf,0x0c,0xea,0x0c
_reg_f22:.byte 0x44,0x53,0x8e,0x0e,0x33,0x02,0xb8,0x29
_reg_f23:.byte 0x41,0x44,0x32,0x3c,0x2e,0x4e,0x76,0x4e
_reg_f24:.byte 0x33,0x07,0x9a,0x3b,0xe2,0xdf,0x5b,0x1c
_reg_f25:.byte 0x65,0x13,0xef,0x7d,0x42,0xf7,0xd6,0x1d
_reg_f26:.byte 0x7f,0x5c,0x28,0x46,0x0b,0xb7,0x05,0x42
_reg_f27:.byte 0x67,0xa0,0xa1,0xe8,0x3f,0x0d,0xc2,0x1d
_reg_f28:.byte 0x5e,0x69,0xd8,0x61,0x05,0xf4,0xa0,0xf7
_reg_f29:.byte 0x2a,0x5b,0x73,0xc6,0x61,0x7d,0xaa,0x3f
_reg_f30:.byte 0x4c,0x84,0x8f,0xe4,0xea,0x38,0x36,0xbb
_reg_f31:.byte 0x2f,0x32,0xaf,0x8d,0x85,0xc6,0xfb,0xb9
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x81
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xfc03ddf6acf3434     // ra
    li x2, 0x1                   // sp
    li x3, 0x801803f3            // gp
    li x4, 0xbff9262cdea724b2    // tp
    li x5, 0x801fc987            // t0
    li x6, 0xfd7f295dbf383378    // t1
    li x7, 0x5233606f25aea370    // t2
    li x8, 0xccb8e43359f8681d    // fp
    li x9, 0xfdab24985a085864    // s1
    li x10, 0x1eda5e6710270313   // a0
    li x11, 0x6b42b03763b3e262   // a1
    li x12, 0x318d756a21594311   // a2
    li x13, 0x51383213b4a01eb6   // a3
    li x14, 0xc76c000            // a4
    li x15, 0x8010c7a1000000     // a5
    li x16, 0x4f                 // a6
    li x17, 0xb86796caab3d5607   // a7
    li x18, 0xd4bd5bb4feeebd8    // s2
    li x19, 0x6000               // s3
    li x20, 0x8010c7a1           // s4
    li x21, 0xfdab37da7f09596d   // s5
    li x22, 0xdc748521537a3b3c   // s6
    li x23, 0xfa6f481b9b91ed2b   // s7
    li x24, 0x0                  // s8
    li x25, 0x593f60a641b9eb5d   // s9
    li x26, 0xc82cda109163fffb   // s10
    li x27, 0xf18c1aa1ecc8635c   // s11
    li x28, 0x8021f01b           // t3
    li x29, 0xbf                 // t4
    li x30, 0xfee6237e3baabe72   // t5
    li x31, 0x1c0237d23f09012d   // t6
    // INSTRUCTION ({'dep': {'x16', 'fcsr.rm', 'f9', 'mstatus.fs/vs.fs'}, 'clob': {'x16', 'x24'}})
    
    li x24, 0xffffc
    and x16, x16, x24
    li x24, 0x801802d7
    add x16, x16, x24
    fsw f9, -0x2d7(x16)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        da5cf192e77d2a2a48be366eafa94e295a46ff49        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f9, -0x2d7(x16)
+========================================================================================================================+
Attributes:  fcsr ['inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        da5cf192e77d2a2a48be366eafa94e295a46ff49        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x2, d7, x16
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)
a6(x16)             0x0000000080180323(2149057315)                  0x0000000080180323(2149057315)
f9                  0xced9b7f4482aa85e(-7.100122191866003e+71_d)    0xced9b7f4482aa85e(-7.100122191866003e+71_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0fc03ddf6acf3434(1134975135876330548)         0x0fc03ddf6acf3434(1134975135876330548)         
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)                           
gp(x3)              0x00000000801803f3(2149057523)                  0x00000000801803f3(2149057523)                  
tp(x4)              0xbff9262cdea724b2(13833129704601101490)        0xbff9262cdea724b2(13833129704601101490)        
t0(x5)              0x00000000801fc987(2149566855)                  0x00000000801fc987(2149566855)                  
t1(x6)              0xfd7f295dbf383378(18266364096254849912)        0xfd7f295dbf383378(18266364096254849912)        
t2(x7)              0x5233606f25aea370(5923183965412172656)         0x5233606f25aea370(5923183965412172656)         
fp(x8)              0xccb8e43359f8681d(14751791488655976477)        0xccb8e43359f8681d(14751791488655976477)        
s1(x9)              0xfdab24985a085864(18278743749377415268)        0xfdab24985a085864(18278743749377415268)        
a0(x10)             0x1eda5e6710270313(2223193162806395667)         0x1eda5e6710270313(2223193162806395667)         
a1(x11)             0x6b42b03763b3e262(7728933662463615586)         0x6b42b03763b3e262(7728933662463615586)         
a2(x12)             0x318d756a21594311(3570639178261152529)         0x318d756a21594311(3570639178261152529)         
a3(x13)             0x51383213b4a01eb6(5852482775984119478)         0x51383213b4a01eb6(5852482775984119478)         
a4(x14)             0x000000000c76c000(209108992)                   0x000000000c76c000(209108992)                   
a5(x15)             0x008010c7a1000000(36047246604632064)           0x008010c7a1000000(36047246604632064)           
a6(x16)             0x0000000080180323(2149057315)                  0x0000000080180323(2149057315)                  
a7(x17)             0xb86796caab3d5607(13287755022780421639)        0xb86796caab3d5607(13287755022780421639)        
s2(x18)             0x0d4bd5bb4feeebd8(958094346223021016)          0x0d4bd5bb4feeebd8(958094346223021016)          
s3(x19)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s4(x20)             0x000000008010c7a1(2148583329)                  0x000000008010c7a1(2148583329)                  
s5(x21)             0xfdab37da7f09596d(18278764924187007341)        0xfdab37da7f09596d(18278764924187007341)        
s6(x22)             0xdc748521537a3b3c(15885468163823516476)        0xdc748521537a3b3c(15885468163823516476)        
s7(x23)             0xfa6f481b9b91ed2b(18045721515308215595)        0xfa6f481b9b91ed2b(18045721515308215595)        
s8(x24)             0x00000000801802d7(2149057239)                  0x00000000801802d7(2149057239)                  
s9(x25)             0x593f60a641b9eb5d(6430965060091898717)         0x593f60a641b9eb5d(6430965060091898717)         
s10(x26)            0xc82cda109163fffb(14424143471254437883)        0xc82cda109163fffb(14424143471254437883)        
s11(x27)            0xf18c1aa1ecc8635c(17405315942644736860)        0xf18c1aa1ecc8635c(17405315942644736860)        
t3(x28)             0x000000008021f01b(2149707803)                  0x000000008021f01b(2149707803)                  
t4(x29)             0x00000000000000bf(191)                         0x00000000000000bf(191)                         
t5(x30)             0xfee6237e3baabe72(18367407155351043698)        0xfee6237e3baabe72(18367407155351043698)        
t6(x31)             0x1c0237d23f09012d(2018236959155618093)         0x1c0237d23f09012d(2018236959155618093)         

STATE               REF                                             DUT                                             DIFF
xmemhash            fc71e711b7c2a1fa3bfdfc0f16c7c0d123d91481        fc71e711b7c2a1fa3bfdfc0f16c7c0d123d91481        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        da5cf192e77d2a2a48be366eafa94e295a46ff49        X
lastPC              0x00000000800008e8(2147485928)                  0x00000000800008e8(2147485928)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000081(129)                         0x0000000000000081(129)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0xdf5670c60b0f9fbb(-1.8364148405546734e+151_d)  0xdf5670c60b0f9fbb(-1.8364148405546734e+151_d)  
f2                  0x1a71bfe658246a57(2.673445886413179e-181_d)    0x1a71bfe658246a57(2.673445886413179e-181_d)    
f3                  0xc26b65c304a7a175(-941371172157.0455_d)        0xc26b65c304a7a175(-941371172157.0455_d)        
f4                  0x92f99f66cc3a7425(-2.9034034753751416e-217_d)  0x92f99f66cc3a7425(-2.9034034753751416e-217_d)  
f5                  0x5783ffa7c2d2fbfa(3.847593126398991e+113_d)    0x5783ffa7c2d2fbfa(3.847593126398991e+113_d)    
f6                  0x6145d9ca601823fe(3.8400240133247844e+160_d)   0x6145d9ca601823fe(3.8400240133247844e+160_d)   
f7                  0x3ba985dd473ecf95(2.7023429652824568e-21_d)    0x3ba985dd473ecf95(2.7023429652824568e-21_d)    
f8                  0xc18ce00381644317(-60555376.17395609_d)        0xc18ce00381644317(-60555376.17395609_d)        
f9                  0xced9b7f4482aa85e(-7.100122191866003e+71_d)    0xced9b7f4482aa85e(-7.100122191866003e+71_d)    
f10                 0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   
f11                 0xbfb7ffcebd2c3f76(-0.0937470638129961_d)       0xbfb7ffcebd2c3f76(-0.0937470638129961_d)       
f12                 0x50afc21ec59909ff(4.707018020049733e+80_d)     0x50afc21ec59909ff(4.707018020049733e+80_d)     
f13                 0x47d134f6f6d79ffb(9.148753757844216e+37_d)     0x47d134f6f6d79ffb(9.148753757844216e+37_d)     
f14                 0xd1920793ca490e1f(-8.756385205883228e+84_d)    0xd1920793ca490e1f(-8.756385205883228e+84_d)    
f15                 0x185a280c5903d704(2.2931970498551383e-191_d)   0x185a280c5903d704(2.2931970498551383e-191_d)   
f16                 0x1c4fb5ae3cb61bdb(2.564156262967477e-172_d)    0x1c4fb5ae3cb61bdb(2.564156262967477e-172_d)    
f17                 0x35c59b19a65aba59(1.1549476100121743e-49_d)    0x35c59b19a65aba59(1.1549476100121743e-49_d)    
f18                 0x617b97c3d87a3112(3.8793054075414955e+161_d)   0x617b97c3d87a3112(3.8793054075414955e+161_d)   
f19                 0xeb38f0f4eb3a80c1(-3.202985767625313e+208_d)   0xeb38f0f4eb3a80c1(-3.202985767625313e+208_d)   
f20                 0x229bc6e28cb31fe7(5.694633027608313e-142_d)    0x229bc6e28cb31fe7(5.694633027608313e-142_d)    
f21                 0x0cea0cbff70504c9(1.8628505844926626e-246_d)   0x0cea0cbff70504c9(1.8628505844926626e-246_d)   
f22                 0x29b802330e8e5344(1.0222761870252597e-107_d)   0x29b802330e8e5344(1.0222761870252597e-107_d)   
f23                 0x4e764e2e3c324441(9.621635287386913e+69_d)     0x4e764e2e3c324441(9.621635287386913e+69_d)     
f24                 0x1c5bdfe23b9a0733(4.508066234129458e-172_d)    0x1c5bdfe23b9a0733(4.508066234129458e-172_d)    
f25                 0x1dd6f7427def1365(6.231391913634826e-165_d)    0x1dd6f7427def1365(6.231391913634826e-165_d)    
f26                 0x4205b70b46285c7f(11658160325.045164_d)        0x4205b70b46285c7f(11658160325.045164_d)        
f27                 0x1dc20d3fe8a1a067(2.4490173050100153e-165_d)   0x1dc20d3fe8a1a067(2.4490173050100153e-165_d)   
f28                 0xf7a0f40561d8695e(-1.749274728489661e+268_d)   0xf7a0f40561d8695e(-1.749274728489661e+268_d)   
f29                 0x3faa7d61c6735b2a(0.05173783824436946_d)       0x3faa7d61c6735b2a(0.05173783824436946_d)       
f30                 0xbb3638eae48f844c(-1.8381883999299958e-23_d)   0xbb3638eae48f844c(-1.8381883999299958e-23_d)   
f31                 0xb9fbc6858daf322f(-2.1910986638582034e-29_d)   0xb9fbc6858daf322f(-2.1910986638582034e-29_d)   
STATES DIFFER: True
```

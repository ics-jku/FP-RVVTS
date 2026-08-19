# FailID_003885 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3885
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
_reg_f0: .byte 0xb4,0xd0,0xa5,0xba,0xfa,0x00,0xfd,0xb3
_reg_f1: .byte 0xea,0xa4,0x61,0x0b,0x2d,0xa0,0xd6,0xd0
_reg_f2: .byte 0xad,0x01,0xc4,0x3c,0x92,0x90,0x3f,0xa4
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x6f,0x51,0x9b,0x4d,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x5b,0x49,0x45,0x63,0x22,0x76,0x65,0x2c
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x03,0x18,0x68,0x4f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0xd7,0xc9,0xb6,0x57,0xe4,0x7d,0xf9,0x4c
_reg_f9: .byte 0xd7,0x37,0x55,0xf1,0xcd,0x7e,0xce,0xc8
_reg_f10:.byte 0x46,0x20,0x18,0x04,0x87,0x16,0xa3,0xbd
_reg_f11:.byte 0xd1,0x2d,0x6a,0x13,0x9e,0x8f,0x57,0x4b
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0xff,0x10,0xae,0x23,0x80,0x14,0x7c,0xde
_reg_f14:.byte 0xa4,0x74,0xa8,0xf2,0xba,0x30,0xc3,0x71
_reg_f15:.byte 0x76,0xa4,0xa2,0xb8,0x5f,0x5f,0x97,0xe6
_reg_f16:.byte 0x4e,0x4c,0x58,0xd3,0xfa,0x6f,0x0d,0x6a
_reg_f17:.byte 0x1c,0x0d,0x72,0x89,0x7c,0xaf,0x95,0xa2
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x24,0xa4,0x63,0x38,0xcd,0x2d,0xd1,0x4b
_reg_f21:.byte 0x4f,0xe7,0xe2,0x89,0xa4,0x08,0x97,0x0b
_reg_f22:.byte 0x00,0x00,0x00,0x72,0x35,0x7a,0xbf,0x41
_reg_f23:.byte 0x96,0x08,0x22,0x7f,0xf8,0x90,0xf3,0x75
_reg_f24:.byte 0xcb,0x5a,0x66,0xb8,0xef,0xeb,0xae,0x44
_reg_f25:.byte 0x0e,0x08,0xae,0x95,0x1a,0x75,0xd8,0x8d
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x40,0x11,0xae,0xf6,0xdf,0xc1
_reg_f31:.byte 0x98,0xa3,0xed,0x57,0x97,0x73,0x65,0xd5
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x1
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8017ffa3            // ra
    li x2, 0x136a2dd1            // sp
    li x3, 0x7ffffada            // gp
    li x4, 0x0                   // tp
    li x5, 0x0                   // t0
    li x6, 0x8018056e            // t1
    li x7, 0x6000                // t2
    li x8, 0xd479ad352b4328b8    // fp
    li x9, 0x8017fd3b            // s1
    li x10, 0xbda3168704182046   // a0
    li x11, 0xee9aeef2dd9e3d3b   // a1
    li x12, 0x65e0d0c24aab6ebe   // a2
    li x13, 0x801c22fe           // a3
    li x14, 0xda5d41e8a55b0b80   // a4
    li x15, 0x8a9e6fcf4c121bce   // a5
    li x16, 0xf38983130859ea9    // a6
    li x17, 0x1091b8231f7a3572   // a7
    li x18, 0x8017fd3b           // s2
    li x19, 0x15832480cddbbabd   // s3
    li x20, 0x800fc7da           // s4
    li x21, 0x4930c186dd1978ca   // s5
    li x22, 0x7ff8000000000000   // s6
    li x23, 0x8017fe2e           // s7
    li x24, 0x5ca0f48955b4c515   // s8
    li x25, 0x37ddb4514f73fcda   // s9
    li x26, 0x801f6c6e           // s10
    li x27, 0x8017fdbb           // s11
    li x28, 0x0                  // t3
    li x29, 0x207848dc           // t4
    li x30, 0x200                // t5
    li x31, 0x800fc663           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x8'}, 'clob': {'x8', 'f11', 'x18'}})
    
    li x18, 0x1ffffc
    and x8, x8, x18
    li x18, 0x800002b9
    add x8, x8, x18
    flw f11, -0x2b9(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f11                 0x4b578f9e136a2dd1(9.026784080126072e+54_d)     0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f11, -0x2b9(x8)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f11                 0x4b578f9e136a2dd1(9.026784080126072e+54_d)     0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f11, x2, b9, x8
sp(x2)              0x00000000136a2dd1(325725649)                   0x00000000136a2dd1(325725649)
fp(x8)              0x0000000080032b71(2147691377)                  0x0000000080032b71(2147691377)
f11                 0x4b578f9e136a2dd1(9.026784080126072e+54_d)     0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017ffa3(2149056419)                  0x000000008017ffa3(2149056419)                  
sp(x2)              0x00000000136a2dd1(325725649)                   0x00000000136a2dd1(325725649)                   
gp(x3)              0x000000007ffffada(2147482330)                  0x000000007ffffada(2147482330)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x000000008018056e(2149057902)                  0x000000008018056e(2149057902)                  
t2(x7)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
fp(x8)              0x0000000080032b71(2147691377)                  0x0000000080032b71(2147691377)                  
s1(x9)              0x000000008017fd3b(2149055803)                  0x000000008017fd3b(2149055803)                  
a0(x10)             0xbda3168704182046(13664790463517302854)        0xbda3168704182046(13664790463517302854)        
a1(x11)             0xee9aeef2dd9e3d3b(17193317254307921211)        0xee9aeef2dd9e3d3b(17193317254307921211)        
a2(x12)             0x65e0d0c24aab6ebe(7341096925508890302)         0x65e0d0c24aab6ebe(7341096925508890302)         
a3(x13)             0x00000000801c22fe(2149327614)                  0x00000000801c22fe(2149327614)                  
a4(x14)             0xda5d41e8a55b0b80(15734805140564806528)        0xda5d41e8a55b0b80(15734805140564806528)        
a5(x15)             0x8a9e6fcf4c121bce(9988543959679507406)         0x8a9e6fcf4c121bce(9988543959679507406)         
a6(x16)             0x0f38983130859ea9(1096793846299598505)         0x0f38983130859ea9(1096793846299598505)         
a7(x17)             0x1091b8231f7a3572(1193937837221361010)         0x1091b8231f7a3572(1193937837221361010)         
s2(x18)             0x00000000800002b9(2147484345)                  0x00000000800002b9(2147484345)                  
s3(x19)             0x15832480cddbbabd(1550122832373725885)         0x15832480cddbbabd(1550122832373725885)         
s4(x20)             0x00000000800fc7da(2148517850)                  0x00000000800fc7da(2148517850)                  
s5(x21)             0x4930c186dd1978ca(5273927948630063306)         0x4930c186dd1978ca(5273927948630063306)         
s6(x22)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
s7(x23)             0x000000008017fe2e(2149056046)                  0x000000008017fe2e(2149056046)                  
s8(x24)             0x5ca0f48955b4c515(6674603518448682261)         0x5ca0f48955b4c515(6674603518448682261)         
s9(x25)             0x37ddb4514f73fcda(4025571903257443546)         0x37ddb4514f73fcda(4025571903257443546)         
s10(x26)            0x00000000801f6c6e(2149543022)                  0x00000000801f6c6e(2149543022)                  
s11(x27)            0x000000008017fdbb(2149055931)                  0x000000008017fdbb(2149055931)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x00000000207848dc(544753884)                   0x00000000207848dc(544753884)                   
t5(x30)             0x0000000000000200(512)                         0x0000000000000200(512)                         
t6(x31)             0x00000000800fc663(2148517475)                  0x00000000800fc663(2148517475)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            ef113652373f7656853702d976bf507e6025b697        ef113652373f7656853702d976bf507e6025b697        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000870(2147485808)                  0x0000000080000870(2147485808)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000001(1)                           0x0000000000000001(1)                           
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    
f1                  0xd0d6a02d0b61a4ea(-2.6827526201998193e+81_d)   0xd0d6a02d0b61a4ea(-2.6827526201998193e+81_d)   
f2                  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff4d9b516f(325725664.0_s)               0xffffffff4d9b516f(325725664.0_s)               
f5                  0x2c6576226345495b(8.038049615433958e-95_d)     0x2c6576226345495b(8.038049615433958e-95_d)     
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff4f681803(3893887744.0_s)              0xffffffff4f681803(3893887744.0_s)              
f8                  0x4cf97de457b6c9d7(6.554190042954392e+62_d)     0x4cf97de457b6c9d7(6.554190042954392e+62_d)     
f9                  0xc8ce7ecdf15537d7(-5.313035801991907e+42_d)    0xc8ce7ecdf15537d7(-5.313035801991907e+42_d)    
f10                 0xbda3168704182046(-8.680216378961315e-12_d)    0xbda3168704182046(-8.680216378961315e-12_d)    
f11                 0x4b578f9e136a2dd1(9.026784080126072e+54_d)     0xffffffff00000000(0.0_s)                       X
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xde7c148023ae10ff(-1.4025431970955475e+147_d)  0xde7c148023ae10ff(-1.4025431970955475e+147_d)  
f14                 0x71c330baf2a874a4(9.996995945124462e+239_d)    0x71c330baf2a874a4(9.996995945124462e+239_d)    
f15                 0xe6975f5fb8a2a476(-1.5889986046966891e+186_d)  0xe6975f5fb8a2a476(-1.5889986046966891e+186_d)  
f16                 0x6a0d6ffad3584c4e(7.210524533161241e+202_d)    0x6a0d6ffad3584c4e(7.210524533161241e+202_d)    
f17                 0xa295af7c89720d1c(-4.445814887693426e-142_d)   0xa295af7c89720d1c(-4.445814887693426e-142_d)   
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0x4bd12dcd3863a424(1.6849028513723058e+57_d)    0x4bd12dcd3863a424(1.6849028513723058e+57_d)    
f21                 0x0b9708a489e2e74f(7.854318363103068e-253_d)    0x0b9708a489e2e74f(7.854318363103068e-253_d)    
f22                 0x41bf7a3572000000(528102770.0_d)               0x41bf7a3572000000(528102770.0_d)               
f23                 0x75f390f87f220896(1.5041972699749784e+260_d)   0x75f390f87f220896(1.5041972699749784e+260_d)   
f24                 0x44aeebefb8665acb(7.301162650616101e+22_d)     0x44aeebefb8665acb(7.301162650616101e+22_d)     
f25                 0x8dd8751a95ae080e(-5.7310531554960516e-242_d)  0x8dd8751a95ae080e(-5.7310531554960516e-242_d)  
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xc1dff6ae11400000(-2145040453.0_d)             0xc1dff6ae11400000(-2145040453.0_d)             
f31                 0xd565739757eda398(-2.402297360108333e+103_d)   0xd565739757eda398(-2.402297360108333e+103_d)   
STATES DIFFER: True
```

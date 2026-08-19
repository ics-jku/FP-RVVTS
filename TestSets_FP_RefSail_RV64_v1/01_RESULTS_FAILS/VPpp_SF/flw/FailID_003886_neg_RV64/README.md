# FailID_003886 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3886
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0xad,0x01,0xc4,0x3c,0x92,0x90,0x3f,0xa4
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x6f,0x51,0x9b,0x4d,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x5b,0x49,0x45,0x63,0x22,0x76,0x65,0x2c
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0xd7,0xc9,0xb6,0x57,0xe4,0x7d,0xf9,0x4c
_reg_f9: .byte 0xd7,0x37,0x55,0xf1,0xcd,0x7e,0xce,0xc8
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0xd1,0x2d,0x6a,0x13,0x9e,0x8f,0x57,0x4b
_reg_f12:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0xff,0x10,0xae,0x23,0x80,0x14,0x7c,0xde
_reg_f14:.byte 0xa4,0x74,0xa8,0xf2,0xba,0x30,0xc3,0x71
_reg_f15:.byte 0x76,0xa4,0xa2,0xb8,0x5f,0x5f,0x97,0xe6
_reg_f16:.byte 0xd3,0xff,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x1c,0x0d,0x72,0x89,0x7c,0xaf,0x95,0xa2
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x24,0xa4,0x63,0x38,0xcd,0x2d,0xd1,0x4b
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x72,0x35,0x7a,0xbf,0x41
_reg_f23:.byte 0x96,0x08,0x22,0x7f,0xf8,0x90,0xf3,0x75
_reg_f24:.byte 0xcb,0x5a,0x66,0xb8,0xef,0xeb,0xae,0x44
_reg_f25:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x72,0x35,0x7a,0xbf,0x41
_reg_f27:.byte 0xe9,0x41,0xb9,0x5e,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0xd3,0xff,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x40,0x11,0xae,0xf6,0xdf,0xc1
_reg_f31:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x28
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x3863a424            // ra
    li x2, 0x136a2dd1            // sp
    li x3, 0x7ffffada            // gp
    li x4, 0x1                   // tp
    li x5, 0x0                   // t0
    li x6, 0x8000064a            // t1
    li x7, 0x6000                // t2
    li x8, 0x2eb1000             // fp
    li x9, 0x28                  // s1
    li x10, 0x8017feaf           // a0
    li x11, 0x8000064a           // a1
    li x12, 0x65e0d0c24aab6ebe   // a2
    li x13, 0x0                  // a3
    li x14, 0x801b0a42           // a4
    li x15, 0x0                  // a5
    li x16, 0x44aeebefb8665acb   // a6
    li x17, 0x1091b8231f7a3572   // a7
    li x18, 0xad108850           // s2
    li x19, 0x15832480cddbbabd   // s3
    li x20, 0x801807ec           // s4
    li x21, 0x8000007c           // s5
    li x22, 0x7ff8000000000000   // s6
    li x23, 0x801803c8           // s7
    li x24, 0x801cc8dc           // s8
    li x25, 0x37ddb4514f73fcda   // s9
    li x26, 0x801f6c6e           // s10
    li x27, 0x6000               // s11
    li x28, 0x7ffff980           // t3
    li x29, 0x7ffff980           // t4
    li x30, 0x5d90a7dc           // t5
    li x31, 0x6000               // t6
    // INSTRUCTION ({'dep': {'x12', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'x12', 'x29', 'f23'}})
    
    li x29, 0x1ffffc
    and x12, x12, x29
    li x29, 0x8000027b
    add x12, x12, x29
    flw f23, -0x27b(x12)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f23                 0x75f390f87f220896(1.5041972699749784e+260_d)   0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f23, -0x27b(x12)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f23                 0x75f390f87f220896(1.5041972699749784e+260_d)   0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f23, x27, x12
a2(x12)             0x00000000800b7137(2148233527)                  0x00000000800b7137(2148233527)
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)
f23                 0x75f390f87f220896(1.5041972699749784e+260_d)   0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000003863a424(946054180)                   0x000000003863a424(946054180)                   
sp(x2)              0x00000000136a2dd1(325725649)                   0x00000000136a2dd1(325725649)                   
gp(x3)              0x000000007ffffada(2147482330)                  0x000000007ffffada(2147482330)                  
tp(x4)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x000000008000064a(2147485258)                  0x000000008000064a(2147485258)                  
t2(x7)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
fp(x8)              0x0000000002eb1000(48959488)                    0x0000000002eb1000(48959488)                    
s1(x9)              0x0000000000000028(40)                          0x0000000000000028(40)                          
a0(x10)             0x000000008017feaf(2149056175)                  0x000000008017feaf(2149056175)                  
a1(x11)             0x000000008000064a(2147485258)                  0x000000008000064a(2147485258)                  
a2(x12)             0x00000000800b7137(2148233527)                  0x00000000800b7137(2148233527)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x00000000801b0a42(2149255746)                  0x00000000801b0a42(2149255746)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x44aeebefb8665acb(4949152455350180555)         0x44aeebefb8665acb(4949152455350180555)         
a7(x17)             0x1091b8231f7a3572(1193937837221361010)         0x1091b8231f7a3572(1193937837221361010)         
s2(x18)             0x00000000ad108850(2903541840)                  0x00000000ad108850(2903541840)                  
s3(x19)             0x15832480cddbbabd(1550122832373725885)         0x15832480cddbbabd(1550122832373725885)         
s4(x20)             0x00000000801807ec(2149058540)                  0x00000000801807ec(2149058540)                  
s5(x21)             0x000000008000007c(2147483772)                  0x000000008000007c(2147483772)                  
s6(x22)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
s7(x23)             0x00000000801803c8(2149057480)                  0x00000000801803c8(2149057480)                  
s8(x24)             0x00000000801cc8dc(2149370076)                  0x00000000801cc8dc(2149370076)                  
s9(x25)             0x37ddb4514f73fcda(4025571903257443546)         0x37ddb4514f73fcda(4025571903257443546)         
s10(x26)            0x00000000801f6c6e(2149543022)                  0x00000000801f6c6e(2149543022)                  
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x000000007ffff980(2147481984)                  0x000000007ffff980(2147481984)                  
t4(x29)             0x000000008000027b(2147484283)                  0x000000008000027b(2147484283)                  
t5(x30)             0x000000005d90a7dc(1569761244)                  0x000000005d90a7dc(1569761244)                  
t6(x31)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       

STATE               REF                                             DUT                                             DIFF
xmemhash            f7302bf9cc70846ac46385b943c62bcf847d8be4        f7302bf9cc70846ac46385b943c62bcf847d8be4        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800007ac(2147485612)                  0x00000000800007ac(2147485612)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000028(40)                          0x0000000000000028(40)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    0xb3fd00fabaa5d0b4(-2.887860019341169e-58_d)    
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff4d9b516f(325725664.0_s)               0xffffffff4d9b516f(325725664.0_s)               
f5                  0x2c6576226345495b(8.038049615433958e-95_d)     0x2c6576226345495b(8.038049615433958e-95_d)     
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x4cf97de457b6c9d7(6.554190042954392e+62_d)     0x4cf97de457b6c9d7(6.554190042954392e+62_d)     
f9                  0xc8ce7ecdf15537d7(-5.313035801991907e+42_d)    0xc8ce7ecdf15537d7(-5.313035801991907e+42_d)    
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x4b578f9e136a2dd1(9.026784080126072e+54_d)     0x4b578f9e136a2dd1(9.026784080126072e+54_d)     
f12                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f13                 0xde7c148023ae10ff(-1.4025431970955475e+147_d)  0xde7c148023ae10ff(-1.4025431970955475e+147_d)  
f14                 0x71c330baf2a874a4(9.996995945124462e+239_d)    0x71c330baf2a874a4(9.996995945124462e+239_d)    
f15                 0xe6975f5fb8a2a476(-1.5889986046966891e+186_d)  0xe6975f5fb8a2a476(-1.5889986046966891e+186_d)  
f16                 0xffffffff8017ffd3(-2.2039888493608945e-39_s)   0xffffffff8017ffd3(-2.2039888493608945e-39_s)   
f17                 0xa295af7c89720d1c(-4.445814887693426e-142_d)   0xa295af7c89720d1c(-4.445814887693426e-142_d)   
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0x4bd12dcd3863a424(1.6849028513723058e+57_d)    0x4bd12dcd3863a424(1.6849028513723058e+57_d)    
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x41bf7a3572000000(528102770.0_d)               0x41bf7a3572000000(528102770.0_d)               
f23                 0x75f390f87f220896(1.5041972699749784e+260_d)   0xffffffff00000000(0.0_s)                       X
f24                 0x44aeebefb8665acb(7.301162650616101e+22_d)     0x44aeebefb8665acb(7.301162650616101e+22_d)     
f25                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f26                 0x41bf7a3572000000(528102770.0_d)               0x41bf7a3572000000(528102770.0_d)               
f27                 0xffffffff5eb941e9(6.674603478356066e+18_s)     0xffffffff5eb941e9(6.674603478356066e+18_s)     
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff8017ffd3(-2.2039888493608945e-39_s)   0xffffffff8017ffd3(-2.2039888493608945e-39_s)   
f30                 0xc1dff6ae11400000(-2145040453.0_d)             0xc1dff6ae11400000(-2145040453.0_d)             
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

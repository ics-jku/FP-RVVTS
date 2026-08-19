# FailID_004928 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4928
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
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x53,0x08,0x00,0xd2,0xff,0xff,0xff,0xff
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
    li x1, 0x8017fab6            // ra
    li x2, 0x10018061f           // sp
    li x3, 0x7ffffada            // gp
    li x4, 0x0                   // tp
    li x5, 0x8007ec50            // t0
    li x6, 0x0                   // t1
    li x7, 0x0                   // t2
    li x8, 0xb2                  // fp
    li x9, 0x801807d7            // s1
    li x10, 0x7ffff880           // a0
    li x11, 0xfb                 // a1
    li x12, 0x0                  // a2
    li x13, 0x400bf              // a3
    li x14, 0x0                  // a4
    li x15, 0x70a9e000           // a5
    li x16, 0x0                  // a6
    li x17, 0xffffffffb78b3000   // a7
    li x18, 0x8018072f           // s2
    li x19, 0x8017fb93           // s3
    li x20, 0x514867ac           // s4
    li x21, 0x802003ef           // s5
    li x22, 0x68                 // s6
    li x23, 0xd20008d3d2000853   // s7
    li x24, 0x801804d6           // s8
    li x25, 0x801800e0           // s9
    li x26, 0x1002ff6c           // s10
    li x27, 0x80180132           // s11
    li x28, 0x180cfd             // t3
    li x29, 0x8017fb61           // t4
    li x30, 0x801808b7           // t5
    li x31, 0x8018597c           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x19', 'fcsr.rm', 'f2'}, 'clob': {'x19', 'x2'}})
    
    li x2, 0xffffc
    and x19, x19, x2
    li x2, 0x8018047e
    add x19, x19, x2
    fsw f2, -0x47e(x19)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2db5f202ab7a46e9340de805a00442c24643cf6a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f2, -0x47e(x19)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2db5f202ab7a46e9340de805a00442c24643cf6a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f2, x47, x19
s3(x19)             0x000000008020000e(2149580814)                  0x000000008020000e(2149580814)
f2                  0xa43f90923cc401ad(-4.3427421173394577e-134_d)  0xa43f90923cc401ad(-4.3427421173394577e-134_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008017fab6(2149055158)                  0x000000008017fab6(2149055158)                  
sp(x2)              0x000000008018047e(2149057662)                  0x000000008018047e(2149057662)                  
gp(x3)              0x000000007ffffada(2147482330)                  0x000000007ffffada(2147482330)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x000000008007ec50(2148002896)                  0x000000008007ec50(2148002896)                  
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x00000000000000b2(178)                         0x00000000000000b2(178)                         
s1(x9)              0x00000000801807d7(2149058519)                  0x00000000801807d7(2149058519)                  
a0(x10)             0x000000007ffff880(2147481728)                  0x000000007ffff880(2147481728)                  
a1(x11)             0x00000000000000fb(251)                         0x00000000000000fb(251)                         
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x00000000000400bf(262335)                      0x00000000000400bf(262335)                      
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000070a9e000(1890181120)                  0x0000000070a9e000(1890181120)                  
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0xffffffffb78b3000(18446744072493936640)        0xffffffffb78b3000(18446744072493936640)        
s2(x18)             0x000000008018072f(2149058351)                  0x000000008018072f(2149058351)                  
s3(x19)             0x000000008020000e(2149580814)                  0x000000008020000e(2149580814)                  
s4(x20)             0x00000000514867ac(1363699628)                  0x00000000514867ac(1363699628)                  
s5(x21)             0x00000000802003ef(2149581807)                  0x00000000802003ef(2149581807)                  
s6(x22)             0x0000000000000068(104)                         0x0000000000000068(104)                         
s7(x23)             0xd20008d3d2000853(15132104453819205715)        0xd20008d3d2000853(15132104453819205715)        
s8(x24)             0x00000000801804d6(2149057750)                  0x00000000801804d6(2149057750)                  
s9(x25)             0x00000000801800e0(2149056736)                  0x00000000801800e0(2149056736)                  
s10(x26)            0x000000001002ff6c(268631916)                   0x000000001002ff6c(268631916)                   
s11(x27)            0x0000000080180132(2149056818)                  0x0000000080180132(2149056818)                  
t3(x28)             0x0000000000180cfd(1576189)                     0x0000000000180cfd(1576189)                     
t4(x29)             0x000000008017fb61(2149055329)                  0x000000008017fb61(2149055329)                  
t5(x30)             0x00000000801808b7(2149058743)                  0x00000000801808b7(2149058743)                  
t6(x31)             0x000000008018597c(2149079420)                  0x000000008018597c(2149079420)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            a0acf6de4d249d97d426a8812f2e69514afd21ad        a0acf6de4d249d97d426a8812f2e69514afd21ad        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        2db5f202ab7a46e9340de805a00442c24643cf6a        X
lastPC              0x0000000080000764(2147485540)                  0x0000000080000764(2147485540)                  
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
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffffd2000853(-137473867776.0_s)           0xffffffffd2000853(-137473867776.0_s)           
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x41bf7a3572000000(528102770.0_d)               0x41bf7a3572000000(528102770.0_d)               
f23                 0x75f390f87f220896(1.5041972699749784e+260_d)   0x75f390f87f220896(1.5041972699749784e+260_d)   
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

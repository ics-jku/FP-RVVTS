# FailID_004494 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4494
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x8d,0xf9,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0xaa,0x00,0x03,0xe0,0x41
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f28:.byte 0x83,0xb2,0x01,0x00,0x03,0xb3,0x81,0x00
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
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
    li x1, 0x0                   // ra
    li x2, 0x7ffffcd7            // sp
    li x3, 0x8020ff5f            // gp
    li x4, 0x80280742            // tp
    li x5, 0x1                   // t0
    li x6, 0x8027fb7c            // t1
    li x7, 0x80005b04            // t2
    li x8, 0x0                   // fp
    li x9, 0x0                   // s1
    li x10, 0xf0                 // a0
    li x11, 0x7ffffef6           // a1
    li x12, 0x0                  // a2
    li x13, 0x7ffffc1b           // a3
    li x14, 0x200                // a4
    li x15, 0x6000               // a5
    li x16, 0x8017f6cc           // a6
    li x17, 0x7ffffb90           // a7
    li x18, 0x5fb                // s2
    li x19, 0x80180521           // s3
    li x20, 0x80234e2c           // s4
    li x21, 0x7fffff34           // s5
    li x22, 0x80180493           // s6
    li x23, 0x44                 // s7
    li x24, 0x8017ffa2           // s8
    li x25, 0x8017ff7c           // s9
    li x26, 0x8017ffba           // s10
    li x27, 0x0                  // s11
    li x28, 0x801806e4           // t3
    li x29, 0x7ffffd48           // t4
    li x30, 0x80180493           // t5
    li x31, 0x7ffffae2           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f9', 'x18'}, 'clob': {'x18', 'x20'}})
    
    li x20, 0xffff8
    and x18, x18, x20
    li x20, 0x8017fb76
    add x18, x18, x20
    fsd f9, 0x48a(x18)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        39c0d0d7431350ee7497213d8e01f4c4b38e4362        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f9, 0x48a(x18)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        39c0d0d7431350ee7497213d8e01f4c4b38e4362        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x48, x18
s2(x18)             0x000000008018016e(2149056878)                  0x000000008018016e(2149056878)
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x000000007ffffcd7(2147482839)                  0x000000007ffffcd7(2147482839)                  
gp(x3)              0x000000008020ff5f(2149646175)                  0x000000008020ff5f(2149646175)                  
tp(x4)              0x0000000080280742(2150106946)                  0x0000000080280742(2150106946)                  
t0(x5)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t1(x6)              0x000000008027fb7c(2150103932)                  0x000000008027fb7c(2150103932)                  
t2(x7)              0x0000000080005b04(2147506948)                  0x0000000080005b04(2147506948)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x00000000000000f0(240)                         0x00000000000000f0(240)                         
a1(x11)             0x000000007ffffef6(2147483382)                  0x000000007ffffef6(2147483382)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x000000007ffffc1b(2147482651)                  0x000000007ffffc1b(2147482651)                  
a4(x14)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x000000008017f6cc(2149054156)                  0x000000008017f6cc(2149054156)                  
a7(x17)             0x000000007ffffb90(2147482512)                  0x000000007ffffb90(2147482512)                  
s2(x18)             0x000000008018016e(2149056878)                  0x000000008018016e(2149056878)                  
s3(x19)             0x0000000080180521(2149057825)                  0x0000000080180521(2149057825)                  
s4(x20)             0x000000008017fb76(2149055350)                  0x000000008017fb76(2149055350)                  
s5(x21)             0x000000007fffff34(2147483444)                  0x000000007fffff34(2147483444)                  
s6(x22)             0x0000000080180493(2149057683)                  0x0000000080180493(2149057683)                  
s7(x23)             0x0000000000000044(68)                          0x0000000000000044(68)                          
s8(x24)             0x000000008017ffa2(2149056418)                  0x000000008017ffa2(2149056418)                  
s9(x25)             0x000000008017ff7c(2149056380)                  0x000000008017ff7c(2149056380)                  
s10(x26)            0x000000008017ffba(2149056442)                  0x000000008017ffba(2149056442)                  
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x00000000801806e4(2149058276)                  0x00000000801806e4(2149058276)                  
t4(x29)             0x000000007ffffd48(2147482952)                  0x000000007ffffd48(2147482952)                  
t5(x30)             0x0000000080180493(2149057683)                  0x0000000080180493(2149057683)                  
t6(x31)             0x000000007ffffae2(2147482338)                  0x000000007ffffae2(2147482338)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            9c44dadd60bd4546b5e01c91621e30561a23c945        9c44dadd60bd4546b5e01c91621e30561a23c945        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        39c0d0d7431350ee7497213d8e01f4c4b38e4362        X
lastPC              0x0000000080000750(2147485520)                  0x0000000080000750(2147485520)                  
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
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff7ffff98d(nan_s)                       0xffffffff7ffff98d(nan_s)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x41e00300aa000000(2149057872.0_d)              0x41e00300aa000000(2149057872.0_d)              
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f23                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f24                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f28                 0x0081b3030001b283(3.150573665064223e-306_d)    0x0081b3030001b283(3.150573665064223e-306_d)    
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

# FailID_001940 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1940
* Isolated failing instruction: `fsd`
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0xda,0xfe,0xf9,0xdf,0xc1
_reg_f8: .byte 0x44,0xf7,0xe8,0x0e,0x00,0x00,0x00,0x00
_reg_f9: .byte 0xf4,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0xf3,0x04,0xb5,0x41,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x44,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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
    li x1, 0x80000209            // ra
    li x2, 0xffffffff7fc00000    // sp
    li x3, 0x1                   // gp
    li x4, 0x200                 // tp
    li x5, 0x80000512            // t0
    li x6, 0x8017ff41            // t1
    li x7, 0x8017fc30            // t2
    li x8, 0x800007af            // fp
    li x9, 0x80000209            // s1
    li x10, 0x80011783           // a0
    li x11, 0x800007cf           // a1
    li x12, 0x8000008f           // a2
    li x13, 0x801802dc           // a3
    li x14, 0xfffffffff808b000   // a4
    li x15, 0x8017ffb7           // a5
    li x16, 0x800004ad           // a6
    li x17, 0x8017fb45           // a7
    li x18, 0x0                  // s2
    li x19, 0x1002ff0da00000     // s3
    li x20, 0x800003a8           // s4
    li x21, 0x801da2cd           // s5
    li x22, 0x8020017f           // s6
    li x23, 0x0                  // s7
    li x24, 0x801e9661           // s8
    li x25, 0x0                  // s9
    li x26, 0x80019414           // s10
    li x27, 0x0                  // s11
    li x28, 0x8020037f           // t3
    li x29, 0x8000608f           // t4
    li x30, 0x8017fb4d           // t5
    li x31, 0x10                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x8', 'mstatus.fs/vs.fs', 'f24'}, 'clob': {'x8', 'x24'}})
    
    li x24, 0xffff8
    and x8, x8, x24
    li x24, 0x801802d4
    add x8, x8, x24
    fsd f24, -0x2d4(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        0440aa20f8e15eb2cdba619f4ddefcb70620a66a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f24, -0x2d4(x8)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        0440aa20f8e15eb2cdba619f4ddefcb70620a66a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f24, x2, d4, x8
sp(x2)              0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)
fp(x8)              0x0000000080180a7c(2149059196)                  0x0000000080180a7c(2149059196)
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080000209(2147484169)                  0x0000000080000209(2147484169)                  
sp(x2)              0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x0000000000000200(512)                         0x0000000000000200(512)                         
t0(x5)              0x0000000080000512(2147484946)                  0x0000000080000512(2147484946)                  
t1(x6)              0x000000008017ff41(2149056321)                  0x000000008017ff41(2149056321)                  
t2(x7)              0x000000008017fc30(2149055536)                  0x000000008017fc30(2149055536)                  
fp(x8)              0x0000000080180a7c(2149059196)                  0x0000000080180a7c(2149059196)                  
s1(x9)              0x0000000080000209(2147484169)                  0x0000000080000209(2147484169)                  
a0(x10)             0x0000000080011783(2147555203)                  0x0000000080011783(2147555203)                  
a1(x11)             0x00000000800007cf(2147485647)                  0x00000000800007cf(2147485647)                  
a2(x12)             0x000000008000008f(2147483791)                  0x000000008000008f(2147483791)                  
a3(x13)             0x00000000801802dc(2149057244)                  0x00000000801802dc(2149057244)                  
a4(x14)             0xfffffffff808b000(18446744073575903232)        0xfffffffff808b000(18446744073575903232)        
a5(x15)             0x000000008017ffb7(2149056439)                  0x000000008017ffb7(2149056439)                  
a6(x16)             0x00000000800004ad(2147484845)                  0x00000000800004ad(2147484845)                  
a7(x17)             0x000000008017fb45(2149055301)                  0x000000008017fb45(2149055301)                  
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x001002ff0da00000(4506894095876096)            0x001002ff0da00000(4506894095876096)            
s4(x20)             0x00000000800003a8(2147484584)                  0x00000000800003a8(2147484584)                  
s5(x21)             0x00000000801da2cd(2149425869)                  0x00000000801da2cd(2149425869)                  
s6(x22)             0x000000008020017f(2149581183)                  0x000000008020017f(2149581183)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x00000000801802d4(2149057236)                  0x00000000801802d4(2149057236)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000080019414(2147587092)                  0x0000000080019414(2147587092)                  
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x000000008020037f(2149581695)                  0x000000008020037f(2149581695)                  
t4(x29)             0x000000008000608f(2147508367)                  0x000000008000608f(2147508367)                  
t5(x30)             0x000000008017fb4d(2149055309)                  0x000000008017fb4d(2149055309)                  
t6(x31)             0x0000000000000010(16)                          0x0000000000000010(16)                          

STATE               REF                                             DUT                                             DIFF
xmemhash            eb691a3b02859664a980209c54e20a2c185cccc4        eb691a3b02859664a980209c54e20a2c185cccc4        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        0440aa20f8e15eb2cdba619f4ddefcb70620a66a        X
lastPC              0x0000000080000780(2147485568)                  0x0000000080000780(2147485568)                  
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
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xc1dff9feda000000(-2145909608.0_d)             0xc1dff9feda000000(-2145909608.0_d)             
f8                  0x000000000ee8f744(1.23589867e-315_d)           0x000000000ee8f744(1.23589867e-315_d)           
f9                  0xffffffff4efffff4(2147482112.0_s)              0xffffffff4efffff4(2147482112.0_s)              
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f14                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff41b504f3(22.627416610717773_s)        0xffffffff41b504f3(22.627416610717773_s)        
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)                     
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
STATES DIFFER: True
```

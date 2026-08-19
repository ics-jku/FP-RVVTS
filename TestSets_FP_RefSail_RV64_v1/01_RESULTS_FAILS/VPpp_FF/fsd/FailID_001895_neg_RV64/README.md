# FailID_001895 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1895
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x82,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x08,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0xb0,0x25,0xbc,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x3d,0xb1,0xaf,0xdd,0x48,0xf5,0x3e,0xde
_reg_f24:.byte 0x00,0x00,0x14,0x42,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x18,0x40
_reg_f29:.byte 0x83,0x03,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x3e,0xf9,0x17,0x80,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x82
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x6000                // ra
    li x2, 0x2d9b6714            // sp
    li x3, 0x188ac700            // gp
    li x4, 0x8018075f            // tp
    li x5, 0x100000              // t0
    li x6, 0x80000383            // t1
    li x7, 0x1004016e6           // t2
    li x8, 0x59                  // fp
    li x9, 0x8017f96f            // s1
    li x10, 0x1                  // a0
    li x11, 0x8017fcda           // a1
    li x12, 0xffffffffe0b5c000   // a2
    li x13, 0x801ff896           // a3
    li x14, 0x80180066           // a4
    li x15, 0x6f                 // a5
    li x16, 0x87                 // a6
    li x17, 0xffffffffffffffff   // a7
    li x18, 0x1                  // s2
    li x19, 0x4                  // s3
    li x20, 0x1                  // s4
    li x21, 0x48                 // s5
    li x22, 0x0                  // s6
    li x23, 0x0                  // s7
    li x24, 0xfffffffffffffa46   // s8
    li x25, 0x8017fe1a           // s9
    li x26, 0xffffffffb8784000   // s10
    li x27, 0x100000             // s11
    li x28, 0x1                  // t3
    li x29, 0x0                  // t4
    li x30, 0x1                  // t5
    li x31, 0x8027f4fa           // t6
    // INSTRUCTION ({'dep': {'f0', 'mstatus.fs/vs.fs', 'fcsr.rm', 'x23'}, 'clob': {'x16', 'x23'}})
    
    li x16, 0xffff8
    and x23, x23, x16
    li x16, 0x8017fdb6
    add x23, x23, x16
    fsd f0, 0x24a(x23)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        62ca3486298f70a21f191cd85cef9af4c6a0ac08        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f0, 0x24a(x23)
+========================================================================================================================+
Attributes:  fcsr ['underflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        62ca3486298f70a21f191cd85cef9af4c6a0ac08        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f0, x24, x23
s7(x23)             0x000000008017fdb6(2149055926)                  0x000000008017fdb6(2149055926)
s8(x24)             0xfffffffffffffa46(18446744073709550150)        0xfffffffffffffa46(18446744073709550150)
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
sp(x2)              0x000000002d9b6714(765159188)                   0x000000002d9b6714(765159188)                   
gp(x3)              0x00000000188ac700(411748096)                   0x00000000188ac700(411748096)                   
tp(x4)              0x000000008018075f(2149058399)                  0x000000008018075f(2149058399)                  
t0(x5)              0x0000000000100000(1048576)                     0x0000000000100000(1048576)                     
t1(x6)              0x0000000080000383(2147484547)                  0x0000000080000383(2147484547)                  
t2(x7)              0x00000001004016e6(4299167462)                  0x00000001004016e6(4299167462)                  
fp(x8)              0x0000000000000059(89)                          0x0000000000000059(89)                          
s1(x9)              0x000000008017f96f(2149054831)                  0x000000008017f96f(2149054831)                  
a0(x10)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a1(x11)             0x000000008017fcda(2149055706)                  0x000000008017fcda(2149055706)                  
a2(x12)             0xffffffffe0b5c000(18446744073184591872)        0xffffffffe0b5c000(18446744073184591872)        
a3(x13)             0x00000000801ff896(2149578902)                  0x00000000801ff896(2149578902)                  
a4(x14)             0x0000000080180066(2149056614)                  0x0000000080180066(2149056614)                  
a5(x15)             0x000000000000006f(111)                         0x000000000000006f(111)                         
a6(x16)             0x000000008017fdb6(2149055926)                  0x000000008017fdb6(2149055926)                  
a7(x17)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s2(x18)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s3(x19)             0x0000000000000004(4)                           0x0000000000000004(4)                           
s4(x20)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s5(x21)             0x0000000000000048(72)                          0x0000000000000048(72)                          
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x000000008017fdb6(2149055926)                  0x000000008017fdb6(2149055926)                  
s8(x24)             0xfffffffffffffa46(18446744073709550150)        0xfffffffffffffa46(18446744073709550150)        
s9(x25)             0x000000008017fe1a(2149056026)                  0x000000008017fe1a(2149056026)                  
s10(x26)            0xffffffffb8784000(18446744072509472768)        0xffffffffb8784000(18446744072509472768)        
s11(x27)            0x0000000000100000(1048576)                     0x0000000000100000(1048576)                     
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t6(x31)             0x000000008027f4fa(2150102266)                  0x000000008027f4fa(2150102266)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            6a2077c46fe04d97698b7d16f3f7b04bc3abdaef        6a2077c46fe04d97698b7d16f3f7b04bc3abdaef        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        62ca3486298f70a21f191cd85cef9af4c6a0ac08        X
lastPC              0x0000000080000704(2147485444)                  0x0000000080000704(2147485444)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000082(130)                         0x0000000000000082(130)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0x0000000000000082(6.4e-322_d)                  0x0000000000000082(6.4e-322_d)                  
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff42140000(37.0_s)                      0xffffffff42140000(37.0_s)                      
f18                 0xffffffff4f001808(2149058560.0_s)              0xffffffff4f001808(2149058560.0_s)              
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffffbc25b000(-0.010112762451171875_s)     0xffffffffbc25b000(-0.010112762451171875_s)     
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0xde3ef548ddafb13d(-9.664353833149178e+145_d)   0xde3ef548ddafb13d(-9.664353833149178e+145_d)   
f24                 0x7fffffff42140000(nan_d)                       0x7fffffff42140000(nan_d)                       
f25                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x4018000000000000(6.0_d)                       0x4018000000000000(6.0_d)                       
f29                 0xffffffff80000383(-1.2597673194280105e-42_s)   0xffffffff80000383(-1.2597673194280105e-42_s)   
f30                 0x000000008017f93e(1.061774139e-314_d)          0x000000008017f93e(1.061774139e-314_d)          
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

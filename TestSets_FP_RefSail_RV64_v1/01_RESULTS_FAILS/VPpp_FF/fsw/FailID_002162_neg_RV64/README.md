# FailID_002162 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2162
* Isolated failing instruction: `fsw`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x60,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x01,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0xa5,0xf9,0x17,0x80,0xff,0xff,0xff,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0x7f
_reg_f25:.byte 0x1d,0xb7,0x27,0x2d,0xb2,0x99,0x1d,0xbe
_reg_f26:.byte 0x00,0x00,0x00,0xe9,0x00,0x03,0xe0,0x41
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x05,0x6a,0xda,0x22,0xa6,0x51,0x64,0x40
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xa0,0xec,0xff,0x02,0xe0,0x41
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x4
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x800003cf            // ra
    li x2, 0x0                   // sp
    li x3, 0x7ffffb37            // gp
    li x4, 0x8018065a            // tp
    li x5, 0x6000                // t0
    li x6, 0x8018045a            // t1
    li x7, 0x8028003f            // t2
    li x8, 0xffffffffffffffff    // fp
    li x9, 0x7fffffff            // s1
    li x10, 0x6000               // a0
    li x11, 0x7ffffb1e           // a1
    li x12, 0x0                  // a2
    li x13, 0xffffffffffffffff   // a3
    li x14, 0x64                 // a4
    li x15, 0x60                 // a5
    li x16, 0x801806d2           // a6
    li x17, 0x4                  // a7
    li x18, 0x0                  // s2
    li x19, 0x2d27b71d           // s3
    li x20, 0x0                  // s4
    li x21, 0x1                  // s5
    li x22, 0xffffffffafa5a000   // s6
    li x23, 0x801805e0           // s7
    li x24, 0x80180748           // s8
    li x25, 0x2                  // s9
    li x26, 0xffffffffffffffff   // s10
    li x27, 0x1                  // s11
    li x28, 0x765cd748           // t3
    li x29, 0xffffffffffffffff   // t4
    li x30, 0x801801b6           // t5
    li x31, 0xffffffffffffffcf   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f9', 'x15'}, 'clob': {'x5', 'x15'}})
    
    li x5, 0xffffc
    and x15, x15, x5
    li x5, 0x80180556
    add x15, x15, x5
    fsw f9, -0x556(x15)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f9, -0x556(x15)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x556, x15
a5(x15)             0x00000000801805b6(2149057974)                  0x00000000801805b6(2149057974)
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000800003cf(2147484623)                  0x00000000800003cf(2147484623)                  
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x000000007ffffb37(2147482423)                  0x000000007ffffb37(2147482423)                  
tp(x4)              0x000000008018065a(2149058138)                  0x000000008018065a(2149058138)                  
t0(x5)              0x0000000080180556(2149057878)                  0x0000000080180556(2149057878)                  
t1(x6)              0x000000008018045a(2149057626)                  0x000000008018045a(2149057626)                  
t2(x7)              0x000000008028003f(2150105151)                  0x000000008028003f(2150105151)                  
fp(x8)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s1(x9)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a0(x10)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a1(x11)             0x000000007ffffb1e(2147482398)                  0x000000007ffffb1e(2147482398)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a4(x14)             0x0000000000000064(100)                         0x0000000000000064(100)                         
a5(x15)             0x00000000801805b6(2149057974)                  0x00000000801805b6(2149057974)                  
a6(x16)             0x00000000801806d2(2149058258)                  0x00000000801806d2(2149058258)                  
a7(x17)             0x0000000000000004(4)                           0x0000000000000004(4)                           
s2(x18)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s3(x19)             0x000000002d27b71d(757577501)                   0x000000002d27b71d(757577501)                   
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s6(x22)             0xffffffffafa5a000(18446744072361451520)        0xffffffffafa5a000(18446744072361451520)        
s7(x23)             0x00000000801805e0(2149058016)                  0x00000000801805e0(2149058016)                  
s8(x24)             0x0000000080180748(2149058376)                  0x0000000080180748(2149058376)                  
s9(x25)             0x0000000000000002(2)                           0x0000000000000002(2)                           
s10(x26)            0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s11(x27)            0x0000000000000001(1)                           0x0000000000000001(1)                           
t3(x28)             0x00000000765cd748(1985795912)                  0x00000000765cd748(1985795912)                  
t4(x29)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t5(x30)             0x00000000801801b6(2149056950)                  0x00000000801801b6(2149056950)                  
t6(x31)             0xffffffffffffffcf(18446744073709551567)        0xffffffffffffffcf(18446744073709551567)        

STATE               REF                                             DUT                                             DIFF
xmemhash            96e22399eeaf9b1d31823a7c0b6f32b24b4d9ec9        96e22399eeaf9b1d31823a7c0b6f32b24b4d9ec9        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000708(2147485448)                  0x0000000080000708(2147485448)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000004(4)                           0x0000000000000004(4)                           
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xffffffff80006000(-3.4438311059246704e-41_s)   0xffffffff80006000(-3.4438311059246704e-41_s)   
f7                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x0000000000000001(5e-324_d)                    0x0000000000000001(5e-324_d)                    
f13                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f19                 0x7fffffff8017f9a5(nan_d)                       0x7fffffff8017f9a5(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7fffffffffc00000(nan_d)                       0x7fffffffffc00000(nan_d)                       
f25                 0xbe1d99b22d27b71d(-1.7229685912554313e-09_d)   0xbe1d99b22d27b71d(-1.7229685912554313e-09_d)   
f26                 0x41e00300e9000000(2149058376.0_d)              0x41e00300e9000000(2149058376.0_d)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x406451a622da6a05(162.55153029116642_d)        0x406451a622da6a05(162.55153029116642_d)        
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x41e002ffeca00000(2149056357.0_d)              0x41e002ffeca00000(2149056357.0_d)              
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

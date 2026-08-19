# FailID_003612 VP++ SF neg RV64 flh

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3612
* Isolated failing instruction: `flh`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f3: .byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x01,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f11:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x20,0xfe,0xff,0xdf,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0xd9,0xfc,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x58
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x100300da8000        // ra
    li x2, 0x8017fd13            // sp
    li x3, 0x801801b2            // gp
    li x4, 0x801858b3            // tp
    li x5, 0x8017f8e0            // t0
    li x6, 0x7ffffcc7            // t1
    li x7, 0x7fffffff            // t2
    li x8, 0x0                   // fp
    li x9, 0x80180031            // s1
    li x10, 0x100380dffb65       // a0
    li x11, 0x7ffffdb3           // a1
    li x12, 0x6000               // a2
    li x13, 0x3f                 // a3
    li x14, 0x400bfdb2800000     // a4
    li x15, 0x8027f66b           // a5
    li x16, 0x7fffffe8           // a6
    li x17, 0x8027eca0           // a7
    li x18, 0x7ffffce3           // s2
    li x19, 0x0                  // s3
    li x20, 0x1                  // s4
    li x21, 0x7fc00000           // s5
    li x22, 0x0                  // s6
    li x23, 0x1                  // s7
    li x24, 0x80180017           // s8
    li x25, 0xe938773c           // s9
    li x26, 0x7fffffff           // s10
    li x27, 0xd9                 // s11
    li x28, 0x7fffffffffffffff   // t3
    li x29, 0x801ffa6a           // t4
    li x30, 0x8017fa8a           // t5
    li x31, 0x6000               // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x27', 'fcsr.rm'}, 'clob': {'x5', 'x27', 'f1'}})
    
    li x5, 0x1ffffe
    and x27, x27, x5
    li x5, 0x8000001f
    add x27, x27, x5
    flh f1, -0x1f(x27)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f1                  0x7ff8000000000000(nan_d)                       0xffffffffffffb023(-0.1292724609375_h)          X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flh f1, -0x1f(x27)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f1                  0x7ff8000000000000(nan_d)                       0xffffffffffffb023(-0.1292724609375_h)          X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f1, x1, x27
ra(x1)              0x0000100300da8000(17605085265920)              0x0000100300da8000(17605085265920)
s11(x27)            0x00000000800000f7(2147483895)                  0x00000000800000f7(2147483895)
f1                  0x7ff8000000000000(nan_d)                       0xffffffffffffb023(-0.1292724609375_h)          X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000100300da8000(17605085265920)              0x0000100300da8000(17605085265920)              
sp(x2)              0x000000008017fd13(2149055763)                  0x000000008017fd13(2149055763)                  
gp(x3)              0x00000000801801b2(2149056946)                  0x00000000801801b2(2149056946)                  
tp(x4)              0x00000000801858b3(2149079219)                  0x00000000801858b3(2149079219)                  
t0(x5)              0x000000008000001f(2147483679)                  0x000000008000001f(2147483679)                  
t1(x6)              0x000000007ffffcc7(2147482823)                  0x000000007ffffcc7(2147482823)                  
t2(x7)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x0000000080180031(2149056561)                  0x0000000080180031(2149056561)                  
a0(x10)             0x0000100380dffb65(17607233108837)              0x0000100380dffb65(17607233108837)              
a1(x11)             0x000000007ffffdb3(2147483059)                  0x000000007ffffdb3(2147483059)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x000000000000003f(63)                          0x000000000000003f(63)                          
a4(x14)             0x00400bfdb2800000(18027582758846464)           0x00400bfdb2800000(18027582758846464)           
a5(x15)             0x000000008027f66b(2150102635)                  0x000000008027f66b(2150102635)                  
a6(x16)             0x000000007fffffe8(2147483624)                  0x000000007fffffe8(2147483624)                  
a7(x17)             0x000000008027eca0(2150100128)                  0x000000008027eca0(2150100128)                  
s2(x18)             0x000000007ffffce3(2147482851)                  0x000000007ffffce3(2147482851)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s5(x21)             0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s8(x24)             0x0000000080180017(2149056535)                  0x0000000080180017(2149056535)                  
s9(x25)             0x00000000e938773c(3912791868)                  0x00000000e938773c(3912791868)                  
s10(x26)            0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s11(x27)            0x00000000800000f7(2147483895)                  0x00000000800000f7(2147483895)                  
t3(x28)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
t4(x29)             0x00000000801ffa6a(2149579370)                  0x00000000801ffa6a(2149579370)                  
t5(x30)             0x000000008017fa8a(2149055114)                  0x000000008017fa8a(2149055114)                  
t6(x31)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       

STATE               REF                                             DUT                                             DIFF
xmemhash            3dfd87aebbf91fea5502ae4422baae8b83a498ad        3dfd87aebbf91fea5502ae4422baae8b83a498ad        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000758(2147485528)                  0x0000000080000758(2147485528)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000058(88)                          0x0000000000000058(88)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0x7ff8000000000000(nan_d)                       0xffffffffffffb023(-0.1292724609375_h)          X
f2                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f3                  0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x0000000000000001(5e-324_d)                    0x0000000000000001(5e-324_d)                    
f11                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f12                 0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x41dffffe20000000(2147481728.0_d)              0x41dffffe20000000(2147481728.0_d)              
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xfffffffffffffcd9(nan_h)                       0xfffffffffffffcd9(nan_h)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f20                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f29                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
STATES DIFFER: True
```

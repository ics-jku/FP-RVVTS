# FailID_004520 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4520
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
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0xda,0xfe,0xf9,0xdf,0xc1
_reg_f8: .byte 0x44,0xf7,0xe8,0x0e,0x00,0x00,0x00,0x00
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x68,0x9d,0xc0
_reg_f13:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x40,0x8d,0xcb,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f19:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x5a,0xfe,0x27,0x80,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x44,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f28:.byte 0x63,0x05,0x00,0x80,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': True, 'nv': True, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x3a
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x100000ac60000000    // ra
    li x2, 0x2b                  // sp
    li x3, 0x800002cf            // gp
    li x4, 0x1                   // tp
    li x5, 0x80180378            // t0
    li x6, 0x1a                  // t1
    li x7, 0x80000563            // t2
    li x8, 0x800007e2            // fp
    li x9, 0x8027fe5a            // s1
    li x10, 0x8000057c           // a0
    li x11, 0x1                  // a1
    li x12, 0x6000               // a2
    li x13, 0x801ff84f           // a3
    li x14, 0x801fffac           // a4
    li x15, 0x3ffffee58000       // a5
    li x16, 0x7fffffffffffffff   // a6
    li x17, 0x6000               // a7
    li x18, 0x7fffffffffffffff   // s2
    li x19, 0x200                // s3
    li x20, 0x81b303             // s4
    li x21, 0x8007f5f3           // s5
    li x22, 0xffffffffb0bed000   // s6
    li x23, 0x0                  // s7
    li x24, 0xfffffffffffffff3   // s8
    li x25, 0x0                  // s9
    li x26, 0x0                  // s10
    li x27, 0x8000081a           // s11
    li x28, 0x6000               // t3
    li x29, 0xffffffff7ffffdd6   // t4
    li x30, 0xffffffffffffffff   // t5
    li x31, 0x7fffffff           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x22', 'f25'}, 'clob': {'x22', 'x2'}})
    
    li x2, 0xffff8
    and x22, x22, x2
    li x2, 0x8017f907
    add x22, x22, x2
    fsd f25, 0x6f9(x22)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        61f2446dbf5f73430658abfca486945652f77d77        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f25, 0x6f9(x22)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'underflow', 'div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        61f2446dbf5f73430658abfca486945652f77d77        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, x6, f9, x22
t1(x6)              0x000000000000001a(26)                          0x000000000000001a(26)
s6(x22)             0x000000008026c907(2150025479)                  0x000000008026c907(2150025479)
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
f25                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x100000ac60000000(1152922244951834624)         0x100000ac60000000(1152922244951834624)         
sp(x2)              0x000000008017f907(2149054727)                  0x000000008017f907(2149054727)                  
gp(x3)              0x00000000800002cf(2147484367)                  0x00000000800002cf(2147484367)                  
tp(x4)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t0(x5)              0x0000000080180378(2149057400)                  0x0000000080180378(2149057400)                  
t1(x6)              0x000000000000001a(26)                          0x000000000000001a(26)                          
t2(x7)              0x0000000080000563(2147485027)                  0x0000000080000563(2147485027)                  
fp(x8)              0x00000000800007e2(2147485666)                  0x00000000800007e2(2147485666)                  
s1(x9)              0x000000008027fe5a(2150104666)                  0x000000008027fe5a(2150104666)                  
a0(x10)             0x000000008000057c(2147485052)                  0x000000008000057c(2147485052)                  
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x00000000801ff84f(2149578831)                  0x00000000801ff84f(2149578831)                  
a4(x14)             0x00000000801fffac(2149580716)                  0x00000000801fffac(2149580716)                  
a5(x15)             0x00003ffffee58000(70368725663744)              0x00003ffffee58000(70368725663744)              
a6(x16)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
a7(x17)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s2(x18)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s3(x19)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s4(x20)             0x000000000081b303(8499971)                     0x000000000081b303(8499971)                     
s5(x21)             0x000000008007f5f3(2148005363)                  0x000000008007f5f3(2148005363)                  
s6(x22)             0x000000008026c907(2150025479)                  0x000000008026c907(2150025479)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0xfffffffffffffff3(18446744073709551603)        0xfffffffffffffff3(18446744073709551603)        
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000008000081a(2147485722)                  0x000000008000081a(2147485722)                  
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0xffffffff7ffffdd6(18446744071562067414)        0xffffffff7ffffdd6(18446744071562067414)        
t5(x30)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t6(x31)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            f133611daeda863ab081596340fe215053504aec        f133611daeda863ab081596340fe215053504aec        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        61f2446dbf5f73430658abfca486945652f77d77        X
lastPC              0x000000008000072c(2147485484)                  0x000000008000072c(2147485484)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000003a(58)                          0x000000000000003a(58)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xc1dff9feda000000(-2145909608.0_d)             0xc1dff9feda000000(-2145909608.0_d)             
f8                  0x000000000ee8f744(1.23589867e-315_d)           0x000000000ee8f744(1.23589867e-315_d)           
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f12                 0xc09d680000000000(-1882.0_d)                   0xc09d680000000000(-1882.0_d)                   
f13                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f14                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffffcb8d4000(-18513920.0_s)               0xffffffffcb8d4000(-18513920.0_s)               
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f19                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x000000008027fe5a(1.0622928504e-314_d)         0x000000008027fe5a(1.0622928504e-314_d)         
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff44000000(512.0_s)                     0xffffffff44000000(512.0_s)                     
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f28                 0xffffffff80000563(-1.9323905823039227e-42_s)   0xffffffff80000563(-1.9323905823039227e-42_s)   
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
STATES DIFFER: True
```

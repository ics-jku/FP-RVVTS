# FailID_001795 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1795
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f13:.byte 0xc2,0xfc,0x17,0x80,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x80,0xbf,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x24
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80005d98            // ra
    li x2, 0x7fffffff            // sp
    li x3, 0x1                   // gp
    li x4, 0x80180689            // tp
    li x5, 0x1fff                // t0
    li x6, 0x8017fc3c            // t1
    li x7, 0xfffffffff0000000    // t2
    li x8, 0x1c                  // fp
    li x9, 0x6000                // s1
    li x10, 0xffffffffffffffff   // a0
    li x11, 0x6000               // a1
    li x12, 0x80180733           // a2
    li x13, 0x7fffffff           // a3
    li x14, 0x200                // a4
    li x15, 0x0                  // a5
    li x16, 0x80201277           // a6
    li x17, 0x801801c2           // a7
    li x18, 0x80000550           // s2
    li x19, 0x8017fede           // s3
    li x20, 0x8017fba2           // s4
    li x21, 0x80200411           // s5
    li x22, 0x7ffffc50           // s6
    li x23, 0x0                  // s7
    li x24, 0x7ffffd04           // s8
    li x25, 0xffffffffffffffff   // s9
    li x26, 0x801801d2           // s10
    li x27, 0x800004e2           // s11
    li x28, 0x200                // t3
    li x29, 0x0                  // t4
    li x30, 0x24                 // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f25', 'x9'}, 'clob': {'x30', 'x9'}})
    
    li x30, 0xffff8
    and x9, x9, x30
    li x30, 0x801800cd
    add x9, x9, x30
    fsd f25, -0xcd(x9)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c706c43a694d240ba15ce28ae82a4ae5732875d2        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f25, -0xcd(x9)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c706c43a694d240ba15ce28ae82a4ae5732875d2        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, x9
s1(x9)              0x00000000801860cd(2149081293)                  0x00000000801860cd(2149081293)
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080005d98(2147507608)                  0x0000000080005d98(2147507608)                  
sp(x2)              0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x0000000080180689(2149058185)                  0x0000000080180689(2149058185)                  
t0(x5)              0x0000000000001fff(8191)                        0x0000000000001fff(8191)                        
t1(x6)              0x000000008017fc3c(2149055548)                  0x000000008017fc3c(2149055548)                  
t2(x7)              0xfffffffff0000000(18446744073441116160)        0xfffffffff0000000(18446744073441116160)        
fp(x8)              0x000000000000001c(28)                          0x000000000000001c(28)                          
s1(x9)              0x00000000801860cd(2149081293)                  0x00000000801860cd(2149081293)                  
a0(x10)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a1(x11)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a2(x12)             0x0000000080180733(2149058355)                  0x0000000080180733(2149058355)                  
a3(x13)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
a4(x14)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x0000000080201277(2149585527)                  0x0000000080201277(2149585527)                  
a7(x17)             0x00000000801801c2(2149056962)                  0x00000000801801c2(2149056962)                  
s2(x18)             0x0000000080000550(2147485008)                  0x0000000080000550(2147485008)                  
s3(x19)             0x000000008017fede(2149056222)                  0x000000008017fede(2149056222)                  
s4(x20)             0x000000008017fba2(2149055394)                  0x000000008017fba2(2149055394)                  
s5(x21)             0x0000000080200411(2149581841)                  0x0000000080200411(2149581841)                  
s6(x22)             0x000000007ffffc50(2147482704)                  0x000000007ffffc50(2147482704)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x000000007ffffd04(2147482884)                  0x000000007ffffd04(2147482884)                  
s9(x25)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s10(x26)            0x00000000801801d2(2149056978)                  0x00000000801801d2(2149056978)                  
s11(x27)            0x00000000800004e2(2147484898)                  0x00000000800004e2(2147484898)                  
t3(x28)             0x0000000000000200(512)                         0x0000000000000200(512)                         
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x00000000801800cd(2149056717)                  0x00000000801800cd(2149056717)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            c9399497ea0179f578963400abbc8bdc7c437faa        c9399497ea0179f578963400abbc8bdc7c437faa        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c706c43a694d240ba15ce28ae82a4ae5732875d2        X
lastPC              0x0000000080000730(2147485488)                  0x0000000080000730(2147485488)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000024(36)                          0x0000000000000024(36)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f13                 0xffffffff8017fcc2(-2.2028888300663995e-39_s)   0xffffffff8017fcc2(-2.2028888300663995e-39_s)   
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f16                 0xffffffffbf800000(-1.0_s)                      0xffffffffbf800000(-1.0_s)                      
f17                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

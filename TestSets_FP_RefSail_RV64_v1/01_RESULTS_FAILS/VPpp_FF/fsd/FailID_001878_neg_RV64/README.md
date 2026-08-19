# FailID_001878 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1878
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
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x50,0xff,0xff,0xdf,0x41
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x60,0xc5,0x00,0x00,0xe0,0x41
_reg_f11:.byte 0x00,0x00,0xc0,0x50,0x00,0xfa,0xdf,0xc1
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f17:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x50,0xff,0xff,0xdf,0x41
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': False, 'nv': True, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x15
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xffffffff7fc00000    // ra
    li x2, 0x200                 // sp
    li x3, 0x8017fdaf            // gp
    li x4, 0x6000                // tp
    li x5, 0x800001ba            // t0
    li x6, 0x80185f93            // t1
    li x7, 0x1                   // t2
    li x8, 0x7ffffbd5            // fp
    li x9, 0x0                   // s1
    li x10, 0x0                  // a0
    li x11, 0x80000056           // a1
    li x12, 0x6000               // a2
    li x13, 0x7fc00000           // a3
    li x14, 0xfffffffffffffff3   // a4
    li x15, 0x61                 // a5
    li x16, 0x8027f657           // a6
    li x17, 0x200                // a7
    li x18, 0x7fffffff           // s2
    li x19, 0x7ffffdb3           // s3
    li x20, 0x0                  // s4
    li x21, 0x80008ee2           // s5
    li x22, 0x0                  // s6
    li x23, 0x0                  // s7
    li x24, 0x1                  // s8
    li x25, 0xffffffff7fc00000   // s9
    li x26, 0x0                  // s10
    li x27, 0x801801e3           // s11
    li x28, 0x8017fd28           // t3
    li x29, 0x8017fb16           // t4
    li x30, 0x0                  // t5
    li x31, 0xffffffffc28b6000   // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f13', 'mstatus.fs/vs.fs', 'x2'}, 'clob': {'x2', 'x30'}})
    
    li x30, 0xffff8
    and x2, x2, x30
    li x30, 0x80180362
    add x2, x2, x30
    fsd f13, -0x362(x2)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        d87b1106312b599166649b6d5cc7c8cf96768e8f        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f13, -0x362(x2)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        d87b1106312b599166649b6d5cc7c8cf96768e8f        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x362, x2
sp(x2)              0x0000000080180562(2149057890)                  0x0000000080180562(2149057890)
f13                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
sp(x2)              0x0000000080180562(2149057890)                  0x0000000080180562(2149057890)                  
gp(x3)              0x000000008017fdaf(2149055919)                  0x000000008017fdaf(2149055919)                  
tp(x4)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t0(x5)              0x00000000800001ba(2147484090)                  0x00000000800001ba(2147484090)                  
t1(x6)              0x0000000080185f93(2149080979)                  0x0000000080185f93(2149080979)                  
t2(x7)              0x0000000000000001(1)                           0x0000000000000001(1)                           
fp(x8)              0x000000007ffffbd5(2147482581)                  0x000000007ffffbd5(2147482581)                  
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x0000000080000056(2147483734)                  0x0000000080000056(2147483734)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
a4(x14)             0xfffffffffffffff3(18446744073709551603)        0xfffffffffffffff3(18446744073709551603)        
a5(x15)             0x0000000000000061(97)                          0x0000000000000061(97)                          
a6(x16)             0x000000008027f657(2150102615)                  0x000000008027f657(2150102615)                  
a7(x17)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s2(x18)             0x000000007fffffff(2147483647)                  0x000000007fffffff(2147483647)                  
s3(x19)             0x000000007ffffdb3(2147483059)                  0x000000007ffffdb3(2147483059)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x0000000080008ee2(2147520226)                  0x0000000080008ee2(2147520226)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x00000000801801e3(2149056995)                  0x00000000801801e3(2149056995)                  
t3(x28)             0x000000008017fd28(2149055784)                  0x000000008017fd28(2149055784)                  
t4(x29)             0x000000008017fb16(2149055254)                  0x000000008017fb16(2149055254)                  
t5(x30)             0x0000000080180362(2149057378)                  0x0000000080180362(2149057378)                  
t6(x31)             0xffffffffc28b6000(18446744072678498304)        0xffffffffc28b6000(18446744072678498304)        

STATE               REF                                             DUT                                             DIFF
xmemhash            9dd237af2160353f4f7148cd84a952a9674a1675        9dd237af2160353f4f7148cd84a952a9674a1675        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        d87b1106312b599166649b6d5cc7c8cf96768e8f        X
lastPC              0x0000000080000710(2147485456)                  0x0000000080000710(2147485456)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000015(21)                          0x0000000000000015(21)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0x41dfffff50000000(2147482944.0_d)              0x41dfffff50000000(2147482944.0_d)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0x41e00000c5600000(2147485227.0_d)              0x41e00000c5600000(2147485227.0_d)              
f11                 0xc1dffa0050c00000(-2145911107.0_d)             0xc1dffa0050c00000(-2145911107.0_d)             
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f16                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f17                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x41dfffff50000000(2147482944.0_d)              0x41dfffff50000000(2147482944.0_d)              
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

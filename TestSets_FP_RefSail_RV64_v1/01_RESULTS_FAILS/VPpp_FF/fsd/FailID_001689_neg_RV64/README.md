# FailID_001689 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1689
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
_reg_f1: .byte 0xfd,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0xfe,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x40,0xd6,0xff,0x02,0xe0,0x41
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x03,0xae,0x07,0x1f,0x9a,0x48,0x48,0xaa
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x60,0x40
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0xfd,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0xbe,0xab,0xb2,0xfd,0xb8,0xa7,0x1b,0x13
_reg_f17:.byte 0x62,0x69,0xc0,0x9f,0x89,0x79,0x90,0xe5
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0xbe,0xab,0xb2,0xfd,0xb8,0xa7,0x1b,0x13
_reg_f20:.byte 0x57,0xa2,0x73,0x0b,0x9c,0x3d,0xa7,0x40
_reg_f21:.byte 0x00,0x00,0xa0,0xbc,0xff,0x02,0xe0,0x41
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x01,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x5c,0x99,0x40
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0xba,0x6c,0x66,0x23,0xbd,0x5d,0x9c,0x86
_reg_f29:.byte 0xba,0x6c,0x66,0x23,0xbd,0x5d,0x9c,0x86
_reg_f30:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': True, 'nv': False, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x68
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xffffffff98fef000    // ra
    li x2, 0x0                   // sp
    li x3, 0xe1                  // gp
    li x4, 0x6000                // tp
    li x5, 0x1bbe9754            // t0
    li x6, 0xffffffffffffffff    // t1
    li x7, 0x8017f9e6            // t2
    li x8, 0x1                   // fp
    li x9, 0xfffffffffdb2abb     // s1
    li x10, 0x7ff8000000000000   // a0
    li x11, 0x64                 // a1
    li x12, 0x8000041a           // a2
    li x13, 0x80180080           // a3
    li x14, 0xc8e1575c           // a4
    li x15, 0x1                  // a5
    li x16, 0x7ffff8af           // a6
    li x17, 0x1                  // a7
    li x18, 0x1                  // s2
    li x19, 0x5                  // s3
    li x20, 0xfffffffffdb2abbe   // s4
    li x21, 0x8027fa44           // s5
    li x22, 0x8000641a           // s6
    li x23, 0x8017fc1a           // s7
    li x24, 0x323855d7000        // s8
    li x25, 0x801ff61f           // s9
    li x26, 0x30                 // s10
    li x27, 0x1                  // s11
    li x28, 0x7ffffa79           // t3
    li x29, 0x1                  // t4
    li x30, 0x8017fea0           // t5
    li x31, 0x8018042a           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x16', 'mstatus.fs/vs.fs', 'f27'}, 'clob': {'x16', 'x29'}})
    
    li x29, 0xffff8
    and x16, x16, x29
    li x29, 0x8017fddf
    add x16, x16, x29
    fsd f27, 0x221(x16)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        bb8891a4cb2884ce44aa83fdd0fe67bb3c1dd747        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f27, 0x221(x16)
+========================================================================================================================+
Attributes:  fcsr ['div-by-0'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        bb8891a4cb2884ce44aa83fdd0fe67bb3c1dd747        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f27, x221, x16
a6(x16)             0x000000008027f687(2150102663)                  0x000000008027f687(2150102663)
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0xffffffff98fef000(18446744071981428736)        0xffffffff98fef000(18446744071981428736)        
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x00000000000000e1(225)                         0x00000000000000e1(225)                         
tp(x4)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t0(x5)              0x000000001bbe9754(465475412)                   0x000000001bbe9754(465475412)                   
t1(x6)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t2(x7)              0x000000008017f9e6(2149054950)                  0x000000008017f9e6(2149054950)                  
fp(x8)              0x0000000000000001(1)                           0x0000000000000001(1)                           
s1(x9)              0x0fffffffffdb2abb(1152921504604433083)         0x0fffffffffdb2abb(1152921504604433083)         
a0(x10)             0x7ff8000000000000(9221120237041090560)         0x7ff8000000000000(9221120237041090560)         
a1(x11)             0x0000000000000064(100)                         0x0000000000000064(100)                         
a2(x12)             0x000000008000041a(2147484698)                  0x000000008000041a(2147484698)                  
a3(x13)             0x0000000080180080(2149056640)                  0x0000000080180080(2149056640)                  
a4(x14)             0x00000000c8e1575c(3370211164)                  0x00000000c8e1575c(3370211164)                  
a5(x15)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a6(x16)             0x000000008027f687(2150102663)                  0x000000008027f687(2150102663)                  
a7(x17)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s2(x18)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s3(x19)             0x0000000000000005(5)                           0x0000000000000005(5)                           
s4(x20)             0xfffffffffdb2abbe(18446744073670929342)        0xfffffffffdb2abbe(18446744073670929342)        
s5(x21)             0x000000008027fa44(2150103620)                  0x000000008027fa44(2150103620)                  
s6(x22)             0x000000008000641a(2147509274)                  0x000000008000641a(2147509274)                  
s7(x23)             0x000000008017fc1a(2149055514)                  0x000000008017fc1a(2149055514)                  
s8(x24)             0x00000323855d7000(3451096231936)               0x00000323855d7000(3451096231936)               
s9(x25)             0x00000000801ff61f(2149578271)                  0x00000000801ff61f(2149578271)                  
s10(x26)            0x0000000000000030(48)                          0x0000000000000030(48)                          
s11(x27)            0x0000000000000001(1)                           0x0000000000000001(1)                           
t3(x28)             0x000000007ffffa79(2147482233)                  0x000000007ffffa79(2147482233)                  
t4(x29)             0x000000008017fddf(2149055967)                  0x000000008017fddf(2149055967)                  
t5(x30)             0x000000008017fea0(2149056160)                  0x000000008017fea0(2149056160)                  
t6(x31)             0x000000008018042a(2149057578)                  0x000000008018042a(2149057578)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            1d3928b56383c933a966ef515dc397dda746cf7d        1d3928b56383c933a966ef515dc397dda746cf7d        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        bb8891a4cb2884ce44aa83fdd0fe67bb3c1dd747        X
lastPC              0x000000008000073c(2147485500)                  0x000000008000073c(2147485500)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000068(104)                         0x0000000000000068(104)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            False                                           False                                           
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff4efffffd(2147483264.0_s)              0xffffffff4efffffd(2147483264.0_s)              
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f4                  0xfffffffffffffe00(nan_h)                       0xfffffffffffffe00(nan_h)                       
f5                  0x41e002ffd6400000(2149056178.0_d)              0x41e002ffd6400000(2149056178.0_d)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xaa48489a1f07ae03(-5.294008362103327e-105_d)   0xaa48489a1f07ae03(-5.294008362103327e-105_d)   
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x4060000000000000(128.0_d)                     0x4060000000000000(128.0_d)                     
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff4efffffd(2147483264.0_s)              0xffffffff4efffffd(2147483264.0_s)              
f15                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f16                 0x131ba7b8fdb2abbe(1.253485769659883e-216_d)    0x131ba7b8fdb2abbe(1.253485769659883e-216_d)    
f17                 0xe59079899fc06962(-1.70905643633674e+181_d)    0xe59079899fc06962(-1.70905643633674e+181_d)    
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x131ba7b8fdb2abbe(1.253485769659883e-216_d)    0x131ba7b8fdb2abbe(1.253485769659883e-216_d)    
f20                 0x40a73d9c0b73a257(2974.8047748695058_d)        0x40a73d9c0b73a257(2974.8047748695058_d)        
f21                 0x41e002ffbca00000(2149055973.0_d)              0x41e002ffbca00000(2149055973.0_d)              
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x0000000000000001(5e-324_d)                    0x0000000000000001(5e-324_d)                    
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x40995c0000000000(1623.0_d)                    0x40995c0000000000(1623.0_d)                    
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x869c5dbd23666cba(-8.001007128548176e-277_d)   0x869c5dbd23666cba(-8.001007128548176e-277_d)   
f29                 0x869c5dbd23666cba(-8.001007128548176e-277_d)   0x869c5dbd23666cba(-8.001007128548176e-277_d)   
f30                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f31                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
STATES DIFFER: True
```

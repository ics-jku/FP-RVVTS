# FailID_002003 VP++ FF neg RV64 fsh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2003
* Isolated failing instruction: `fsh`
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
_reg_f0: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x80,0x40
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xe0,0x66,0x00,0x00,0xe0,0x41
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x60,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0xf9,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x1
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x6000                // ra
    li x2, 0x1                   // sp
    li x3, 0x8018057             // gp
    li x4, 0x3fff                // tp
    li x5, 0x0                   // t0
    li x6, 0x80180577            // t1
    li x7, 0x80180301            // t2
    li x8, 0x0                   // fp
    li x9, 0x200                 // s1
    li x10, 0x4f657000           // a0
    li x11, 0x8017fa34           // a1
    li x12, 0x801dface           // a2
    li x13, 0x80071937           // a3
    li x14, 0x40038              // a4
    li x15, 0x800003             // a5
    li x16, 0xffffffff00000000   // a6
    li x17, 0x5945e000           // a7
    li x18, 0x801e01e0           // s2
    li x19, 0x20080367c000       // s3
    li x20, 0x7ffff968           // s4
    li x21, 0x8017f9ca           // s5
    li x22, 0x801ff95c           // s6
    li x23, 0x800003dd           // s7
    li x24, 0x9420000            // s8
    li x25, 0x8018078c           // s9
    li x26, 0xe                  // s10
    li x27, 0x5789f758           // s11
    li x28, 0x7ffffab3           // t3
    li x29, 0x6000               // t4
    li x30, 0xfffffffffffffa79   // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f31', 'x15'}, 'clob': {'x12', 'x15'}})
    
    li x12, 0xffffe
    and x15, x15, x12
    li x12, 0x8017fd86
    add x15, x15, x12
    fsh f31, 0x27a(x15)
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
Instruction: fsh f31, 0x27a(x15)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f31, x27, x15
a5(x15)             0x000000008017fd88(2149055880)                  0x000000008017fd88(2149055880)
s11(x27)            0x000000005789f758(1468659544)                  0x000000005789f758(1468659544)
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)                           
gp(x3)              0x0000000008018057(134316119)                   0x0000000008018057(134316119)                   
tp(x4)              0x0000000000003fff(16383)                       0x0000000000003fff(16383)                       
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x0000000080180577(2149057911)                  0x0000000080180577(2149057911)                  
t2(x7)              0x0000000080180301(2149057281)                  0x0000000080180301(2149057281)                  
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x0000000000000200(512)                         0x0000000000000200(512)                         
a0(x10)             0x000000004f657000(1332047872)                  0x000000004f657000(1332047872)                  
a1(x11)             0x000000008017fa34(2149055028)                  0x000000008017fa34(2149055028)                  
a2(x12)             0x000000008017fd86(2149055878)                  0x000000008017fd86(2149055878)                  
a3(x13)             0x0000000080071937(2147948855)                  0x0000000080071937(2147948855)                  
a4(x14)             0x0000000000040038(262200)                      0x0000000000040038(262200)                      
a5(x15)             0x000000008017fd88(2149055880)                  0x000000008017fd88(2149055880)                  
a6(x16)             0xffffffff00000000(18446744069414584320)        0xffffffff00000000(18446744069414584320)        
a7(x17)             0x000000005945e000(1497751552)                  0x000000005945e000(1497751552)                  
s2(x18)             0x00000000801e01e0(2149450208)                  0x00000000801e01e0(2149450208)                  
s3(x19)             0x000020080367c000(35218788958208)              0x000020080367c000(35218788958208)              
s4(x20)             0x000000007ffff968(2147481960)                  0x000000007ffff968(2147481960)                  
s5(x21)             0x000000008017f9ca(2149054922)                  0x000000008017f9ca(2149054922)                  
s6(x22)             0x00000000801ff95c(2149579100)                  0x00000000801ff95c(2149579100)                  
s7(x23)             0x00000000800003dd(2147484637)                  0x00000000800003dd(2147484637)                  
s8(x24)             0x0000000009420000(155320320)                   0x0000000009420000(155320320)                   
s9(x25)             0x000000008018078c(2149058444)                  0x000000008018078c(2149058444)                  
s10(x26)            0x000000000000000e(14)                          0x000000000000000e(14)                          
s11(x27)            0x000000005789f758(1468659544)                  0x000000005789f758(1468659544)                  
t3(x28)             0x000000007ffffab3(2147482291)                  0x000000007ffffab3(2147482291)                  
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0xfffffffffffffa79(18446744073709550201)        0xfffffffffffffa79(18446744073709550201)        
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            fa79945dac3e7b0211cbc47282ad5447bf21e8dd        fa79945dac3e7b0211cbc47282ad5447bf21e8dd        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000738(2147485496)                  0x0000000080000738(2147485496)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000001(1)                           0x0000000000000001(1)                           
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x4080000000000000(512.0_d)                     0x4080000000000000(512.0_d)                     
f10                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0x41e0000066e00000(2147484471.0_d)              0x41e0000066e00000(2147484471.0_d)              
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0xffffffffffff6000(512.0_h)                     0xffffffffffff6000(512.0_h)                     
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff4efffff9(2147482752.0_s)              0xffffffff4efffff9(2147482752.0_s)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

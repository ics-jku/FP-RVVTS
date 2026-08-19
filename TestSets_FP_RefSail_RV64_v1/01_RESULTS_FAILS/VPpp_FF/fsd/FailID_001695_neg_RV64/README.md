# FailID_001695 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1695
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
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x28,0xfc,0x94,0xc5,0xc1
_reg_f8: .byte 0x03,0xae,0x07,0x1f,0x9a,0x48,0x48,0xaa
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0xfd,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0xfd,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x5c,0x99,0x40
_reg_f27:.byte 0x00,0x00,0x80,0x4f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xc4
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0xc9                  // ra
    li x2, 0x20060               // sp
    li x3, 0xd5b90764            // gp
    li x4, 0x80180320            // tp
    li x5, 0x0                   // t0
    li x6, 0x0                   // t1
    li x7, 0xfffffffffffffc49    // t2
    li x8, 0x8027f7ca            // fp
    li x9, 0x80180412            // s1
    li x10, 0x8017fb2c           // a0
    li x11, 0x0                  // a1
    li x12, 0x80180412           // a2
    li x13, 0x80180409           // a3
    li x14, 0x7ffffc9a           // a4
    li x15, 0xffffffffff32e000   // a5
    li x16, 0xffffffffbfb49000   // a6
    li x17, 0x6000               // a7
    li x18, 0x6000               // s2
    li x19, 0x8017ff7c           // s3
    li x20, 0x8017fa27           // s4
    li x21, 0xfffffffffffffb7c   // s5
    li x22, 0xc8fa2768           // s6
    li x23, 0x6000               // s7
    li x24, 0x7ffffe85           // s8
    li x25, 0xcd                 // s9
    li x26, 0x200601             // s10
    li x27, 0x8018042f           // s11
    li x28, 0x801801c9           // t3
    li x29, 0x8017fd3c           // t4
    li x30, 0x0                  // t5
    li x31, 0x48e22448           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f13', 'mstatus.fs/vs.fs', 'x7'}, 'clob': {'x9', 'x7'}})
    
    li x9, 0xffff8
    and x7, x7, x9
    li x9, 0x8018053f
    add x7, x7, x9
    fsd f13, -0x53f(x7)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c903d8c6172d7345d86fc34ddaab9adc9ce67d21        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f13, -0x53f(x7)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c903d8c6172d7345d86fc34ddaab9adc9ce67d21        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x53, x7
t2(x7)              0x0000000080280187(2150105479)                  0x0000000080280187(2150105479)
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000000000c9(201)                         0x00000000000000c9(201)                         
sp(x2)              0x0000000000020060(131168)                      0x0000000000020060(131168)                      
gp(x3)              0x00000000d5b90764(3585673060)                  0x00000000d5b90764(3585673060)                  
tp(x4)              0x0000000080180320(2149057312)                  0x0000000080180320(2149057312)                  
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t2(x7)              0x0000000080280187(2150105479)                  0x0000000080280187(2150105479)                  
fp(x8)              0x000000008027f7ca(2150102986)                  0x000000008027f7ca(2150102986)                  
s1(x9)              0x000000008018053f(2149057855)                  0x000000008018053f(2149057855)                  
a0(x10)             0x000000008017fb2c(2149055276)                  0x000000008017fb2c(2149055276)                  
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x0000000080180412(2149057554)                  0x0000000080180412(2149057554)                  
a3(x13)             0x0000000080180409(2149057545)                  0x0000000080180409(2149057545)                  
a4(x14)             0x000000007ffffc9a(2147482778)                  0x000000007ffffc9a(2147482778)                  
a5(x15)             0xffffffffff32e000(18446744073696108544)        0xffffffffff32e000(18446744073696108544)        
a6(x16)             0xffffffffbfb49000(18446744072630865920)        0xffffffffbfb49000(18446744072630865920)        
a7(x17)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s2(x18)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s3(x19)             0x000000008017ff7c(2149056380)                  0x000000008017ff7c(2149056380)                  
s4(x20)             0x000000008017fa27(2149055015)                  0x000000008017fa27(2149055015)                  
s5(x21)             0xfffffffffffffb7c(18446744073709550460)        0xfffffffffffffb7c(18446744073709550460)        
s6(x22)             0x00000000c8fa2768(3371837288)                  0x00000000c8fa2768(3371837288)                  
s7(x23)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s8(x24)             0x000000007ffffe85(2147483269)                  0x000000007ffffe85(2147483269)                  
s9(x25)             0x00000000000000cd(205)                         0x00000000000000cd(205)                         
s10(x26)            0x0000000000200601(2098689)                     0x0000000000200601(2098689)                     
s11(x27)            0x000000008018042f(2149057583)                  0x000000008018042f(2149057583)                  
t3(x28)             0x00000000801801c9(2149056969)                  0x00000000801801c9(2149056969)                  
t4(x29)             0x000000008017fd3c(2149055804)                  0x000000008017fd3c(2149055804)                  
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x0000000048e22448(1222779976)                  0x0000000048e22448(1222779976)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            3684345928cb162246eb795de8a8a7aa79608a2c        3684345928cb162246eb795de8a8a7aa79608a2c        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        c903d8c6172d7345d86fc34ddaab9adc9ce67d21        X
lastPC              0x0000000080000748(2147485512)                  0x0000000080000748(2147485512)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000c4(196)                         0x00000000000000c4(196)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xc1c594fc28000000(-724170832.0_d)              0xc1c594fc28000000(-724170832.0_d)              
f8                  0xaa48489a1f07ae03(-5.294008362103327e-105_d)   0xaa48489a1f07ae03(-5.294008362103327e-105_d)   
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff4efffffd(2147483264.0_s)              0xffffffff4efffffd(2147483264.0_s)              
f15                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff4efffffd(2147483264.0_s)              0xffffffff4efffffd(2147483264.0_s)              
f18                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x40995c0000000000(1623.0_d)                    0x40995c0000000000(1623.0_d)                    
f27                 0xffffffff4f800000(4294967296.0_s)              0xffffffff4f800000(4294967296.0_s)              
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f30                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

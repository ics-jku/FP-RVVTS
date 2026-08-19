# FailID_003842 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3842
* Isolated failing instruction: `flw`
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
_reg_f0: .byte 0x48,0x47,0xe3,0xe9,0x8f,0xad,0x05,0xe5
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0xef,0x9d,0x11,0x89,0x0a,0x13,0x15,0x41
_reg_f3: .byte 0x00,0x00,0x20,0xc3,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0xc0,0x9d,0xff,0x03,0xe0,0x41
_reg_f15:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x77,0xc9,0x94,0xce,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0xfb,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f31:.byte 0x6f,0x00,0x40,0x21,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': False, 'nv': True, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x35
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801804a2            // ra
    li x2, 0x1                   // sp
    li x3, 0x0                   // gp
    li x4, 0x8017fb63            // tp
    li x5, 0x7fffffb1            // t0
    li x6, 0x8017fbaf            // t1
    li x7, 0x0                   // t2
    li x8, 0x801ffd00            // fp
    li x9, 0x801ffcee            // s1
    li x10, 0x80186618           // a0
    li x11, 0x801fff18           // a1
    li x12, 0x6000               // a2
    li x13, 0x7fc00000           // a3
    li x14, 0xffffffffffffffff   // a4
    li x15, 0x97c63714           // a5
    li x16, 0x8017fc5b           // a6
    li x17, 0x80000195           // a7
    li x18, 0x200                // s2
    li x19, 0x200                // s3
    li x20, 0x7fffff36           // s4
    li x21, 0x0                  // s5
    li x22, 0x80000540           // s6
    li x23, 0x7fffffffffffffff   // s7
    li x24, 0xba                 // s8
    li x25, 0xffffffffffffffff   // s9
    li x26, 0x7ffffdf5           // s10
    li x27, 0x800811e4           // s11
    li x28, 0x6000               // t3
    li x29, 0x8017fd06           // t4
    li x30, 0xffffffffffffffff   // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x19', 'fcsr.rm'}, 'clob': {'x19', 'x14', 'f23'}})
    
    li x14, 0x1ffffc
    and x19, x19, x14
    li x14, 0x800007ae
    add x19, x19, x14
    flw f23, -0x7ae(x19)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f23                 0x7ff8000000000000(nan_d)                       0xffffffff0001b283(1.5587343467917103e-40_s)    X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f23, -0x7ae(x19)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f23                 0x7ff8000000000000(nan_d)                       0xffffffff0001b283(1.5587343467917103e-40_s)    X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f23, x7, x19
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)
s3(x19)             0x00000000800009ae(2147486126)                  0x00000000800009ae(2147486126)
f23                 0x7ff8000000000000(nan_d)                       0xffffffff0001b283(1.5587343467917103e-40_s)    X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801804a2(2149057698)                  0x00000000801804a2(2149057698)                  
sp(x2)              0x0000000000000001(1)                           0x0000000000000001(1)                           
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x000000008017fb63(2149055331)                  0x000000008017fb63(2149055331)                  
t0(x5)              0x000000007fffffb1(2147483569)                  0x000000007fffffb1(2147483569)                  
t1(x6)              0x000000008017fbaf(2149055407)                  0x000000008017fbaf(2149055407)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x00000000801ffd00(2149580032)                  0x00000000801ffd00(2149580032)                  
s1(x9)              0x00000000801ffcee(2149580014)                  0x00000000801ffcee(2149580014)                  
a0(x10)             0x0000000080186618(2149082648)                  0x0000000080186618(2149082648)                  
a1(x11)             0x00000000801fff18(2149580568)                  0x00000000801fff18(2149580568)                  
a2(x12)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a3(x13)             0x000000007fc00000(2143289344)                  0x000000007fc00000(2143289344)                  
a4(x14)             0x00000000800007ae(2147485614)                  0x00000000800007ae(2147485614)                  
a5(x15)             0x0000000097c63714(2546349844)                  0x0000000097c63714(2546349844)                  
a6(x16)             0x000000008017fc5b(2149055579)                  0x000000008017fc5b(2149055579)                  
a7(x17)             0x0000000080000195(2147484053)                  0x0000000080000195(2147484053)                  
s2(x18)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s3(x19)             0x00000000800009ae(2147486126)                  0x00000000800009ae(2147486126)                  
s4(x20)             0x000000007fffff36(2147483446)                  0x000000007fffff36(2147483446)                  
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000080000540(2147484992)                  0x0000000080000540(2147484992)                  
s7(x23)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s8(x24)             0x00000000000000ba(186)                         0x00000000000000ba(186)                         
s9(x25)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s10(x26)            0x000000007ffffdf5(2147483125)                  0x000000007ffffdf5(2147483125)                  
s11(x27)            0x00000000800811e4(2148012516)                  0x00000000800811e4(2148012516)                  
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x000000008017fd06(2149055750)                  0x000000008017fd06(2149055750)                  
t5(x30)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            f22af5266fa41fd1436b5246d6751f242f1c6428        f22af5266fa41fd1436b5246d6751f242f1c6428        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000730(2147485488)                  0x0000000080000730(2147485488)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000035(53)                          0x0000000000000035(53)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  0xe505ad8fe9e34748(-4.3922414005583935e+178_d)  
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x4115130a89119def(345282.63385626575_d)        0x4115130a89119def(345282.63385626575_d)        
f3                  0xffffffffc3200000(-160.0_s)                    0xffffffffc3200000(-160.0_s)                    
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f9                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f10                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f11                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f12                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41e003ff9dc00000(2149580014.0_d)              0x41e003ff9dc00000(2149580014.0_d)              
f15                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffffce94c977(-1248115584.0_s)             0xffffffffce94c977(-1248115584.0_s)             
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0xffffffff0001b283(1.5587343467917103e-40_s)    X
f24                 0xffffffff4efffffb(2147483008.0_s)              0xffffffff4efffffb(2147483008.0_s)              
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff2140006f(6.505270420568022e-19_s)     0xffffffff2140006f(6.505270420568022e-19_s)     
STATES DIFFER: True
```

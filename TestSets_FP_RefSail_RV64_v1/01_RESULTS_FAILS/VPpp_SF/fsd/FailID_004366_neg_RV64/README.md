# FailID_004366 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4366
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
    li x2, 0x8017fac0            // sp
    li x3, 0x0                   // gp
    li x4, 0x80180689            // tp
    li x5, 0x1fff                // t0
    li x6, 0x80200707            // t1
    li x7, 0x800001d8            // t2
    li x8, 0x8018034b            // fp
    li x9, 0x0                   // s1
    li x10, 0x6000               // a0
    li x11, 0x0                  // a1
    li x12, 0x80200bac           // a2
    li x13, 0x6000               // a3
    li x14, 0x7ffffc07           // a4
    li x15, 0x80000503           // a5
    li x16, 0x7ffffd4b           // a6
    li x17, 0x7ffffd21           // a7
    li x18, 0x801804fc           // s2
    li x19, 0x8017f83c           // s3
    li x20, 0x8002c0ea           // s4
    li x21, 0x7ffffd21           // s5
    li x22, 0x7ffffc50           // s6
    li x23, 0x7ffff964           // s7
    li x24, 0x1c77               // s8
    li x25, 0x801ff1aa           // s9
    li x26, 0x0                  // s10
    li x27, 0x7ffffd4b           // s11
    li x28, 0x8018581b           // t3
    li x29, 0x32e7f000           // t4
    li x30, 0x6000               // t5
    li x31, 0x7ffff91a           // t6
    // INSTRUCTION ({'dep': {'x16', 'f14', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'x16', 'x10'}})
    
    li x10, 0xffff8
    and x16, x16, x10
    li x10, 0x8017fede
    add x16, x16, x10
    fsd f14, 0x122(x16)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        749384b8c5a073862c3776ebaa5851b299dc6c9c        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f14, 0x122(x16)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        749384b8c5a073862c3776ebaa5851b299dc6c9c        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x122, x16
a6(x16)             0x000000008027fc26(2150104102)                  0x000000008027fc26(2150104102)
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080005d98(2147507608)                  0x0000000080005d98(2147507608)                  
sp(x2)              0x000000008017fac0(2149055168)                  0x000000008017fac0(2149055168)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x0000000080180689(2149058185)                  0x0000000080180689(2149058185)                  
t0(x5)              0x0000000000001fff(8191)                        0x0000000000001fff(8191)                        
t1(x6)              0x0000000080200707(2149582599)                  0x0000000080200707(2149582599)                  
t2(x7)              0x00000000800001d8(2147484120)                  0x00000000800001d8(2147484120)                  
fp(x8)              0x000000008018034b(2149057355)                  0x000000008018034b(2149057355)                  
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x000000008017fede(2149056222)                  0x000000008017fede(2149056222)                  
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x0000000080200bac(2149583788)                  0x0000000080200bac(2149583788)                  
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x000000007ffffc07(2147482631)                  0x000000007ffffc07(2147482631)                  
a5(x15)             0x0000000080000503(2147484931)                  0x0000000080000503(2147484931)                  
a6(x16)             0x000000008027fc26(2150104102)                  0x000000008027fc26(2150104102)                  
a7(x17)             0x000000007ffffd21(2147482913)                  0x000000007ffffd21(2147482913)                  
s2(x18)             0x00000000801804fc(2149057788)                  0x00000000801804fc(2149057788)                  
s3(x19)             0x000000008017f83c(2149054524)                  0x000000008017f83c(2149054524)                  
s4(x20)             0x000000008002c0ea(2147664106)                  0x000000008002c0ea(2147664106)                  
s5(x21)             0x000000007ffffd21(2147482913)                  0x000000007ffffd21(2147482913)                  
s6(x22)             0x000000007ffffc50(2147482704)                  0x000000007ffffc50(2147482704)                  
s7(x23)             0x000000007ffff964(2147481956)                  0x000000007ffff964(2147481956)                  
s8(x24)             0x0000000000001c77(7287)                        0x0000000000001c77(7287)                        
s9(x25)             0x00000000801ff1aa(2149577130)                  0x00000000801ff1aa(2149577130)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x000000007ffffd4b(2147482955)                  0x000000007ffffd4b(2147482955)                  
t3(x28)             0x000000008018581b(2149079067)                  0x000000008018581b(2149079067)                  
t4(x29)             0x0000000032e7f000(854061056)                   0x0000000032e7f000(854061056)                   
t5(x30)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t6(x31)             0x000000007ffff91a(2147481882)                  0x000000007ffff91a(2147481882)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            98b7ea1ef3bc0f266a825e249c375ef1744d89b6        98b7ea1ef3bc0f266a825e249c375ef1744d89b6        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        749384b8c5a073862c3776ebaa5851b299dc6c9c        X
lastPC              0x0000000080000750(2147485520)                  0x0000000080000750(2147485520)                  
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

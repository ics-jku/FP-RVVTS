# FailID_004314 VP++ SF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4314
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
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x63,0x40
_reg_f7: .byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f10:.byte 0x02,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x7c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0xfa,0x27,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xfa,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0x40,0xfb,0xff,0xff,0xdf,0x41
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x63,0x40
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

    // restore fcsr = {'nx': True, 'uf': True, 'of': True, 'dz': False, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x77
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8018059e            // ra
    li x2, 0xa6                  // sp
    li x3, 0xffffffff999c5000    // gp
    li x4, 0x6000                // tp
    li x5, 0x80180445            // t0
    li x6, 0x400c00620000000     // t1
    li x7, 0x80180008            // t2
    li x8, 0x8017fd20            // fp
    li x9, 0x8000037a            // s1
    li x10, 0x0                  // a0
    li x11, 0x458fb780           // a1
    li x12, 0x0                  // a2
    li x13, 0x800063ef           // a3
    li x14, 0x0                  // a4
    li x15, 0x1                  // a5
    li x16, 0x80000055           // a6
    li x17, 0x1                  // a7
    li x18, 0x8017f94a           // s2
    li x19, 0x367                // s3
    li x20, 0x68                 // s4
    li x21, 0x801c4ad2           // s5
    li x22, 0x8014ee1b           // s6
    li x23, 0x800003ef           // s7
    li x24, 0x801800c4           // s8
    li x25, 0x80184d0e           // s9
    li x26, 0xd15f000            // s10
    li x27, 0x8014f65c           // s11
    li x28, 0x6000               // t3
    li x29, 0x801800c4           // t4
    li x30, 0xde                 // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'f14', 'fcsr.rm', 'x26'}, 'clob': {'x26', 'x23'}})
    
    li x23, 0xffff8
    and x26, x26, x23
    li x23, 0x8017fb6b
    add x26, x26, x23
    fsd f14, 0x495(x26)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b03af1e563e6427d00fd76db19a41cde5d93e9f1        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f14, 0x495(x26)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'underflow', 'overflow', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b03af1e563e6427d00fd76db19a41cde5d93e9f1        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x495, x26
s10(x26)            0x00000000801deb6b(2149444459)                  0x00000000801deb6b(2149444459)
f14                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008018059e(2149057950)                  0x000000008018059e(2149057950)                  
sp(x2)              0x00000000000000a6(166)                         0x00000000000000a6(166)                         
gp(x3)              0xffffffff999c5000(18446744071991742464)        0xffffffff999c5000(18446744071991742464)        
tp(x4)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t0(x5)              0x0000000080180445(2149057605)                  0x0000000080180445(2149057605)                  
t1(x6)              0x0400c00620000000(288441508690919424)          0x0400c00620000000(288441508690919424)          
t2(x7)              0x0000000080180008(2149056520)                  0x0000000080180008(2149056520)                  
fp(x8)              0x000000008017fd20(2149055776)                  0x000000008017fd20(2149055776)                  
s1(x9)              0x000000008000037a(2147484538)                  0x000000008000037a(2147484538)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x00000000458fb780(1167046528)                  0x00000000458fb780(1167046528)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0x00000000800063ef(2147509231)                  0x00000000800063ef(2147509231)                  
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a6(x16)             0x0000000080000055(2147483733)                  0x0000000080000055(2147483733)                  
a7(x17)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s2(x18)             0x000000008017f94a(2149054794)                  0x000000008017f94a(2149054794)                  
s3(x19)             0x0000000000000367(871)                         0x0000000000000367(871)                         
s4(x20)             0x0000000000000068(104)                         0x0000000000000068(104)                         
s5(x21)             0x00000000801c4ad2(2149337810)                  0x00000000801c4ad2(2149337810)                  
s6(x22)             0x000000008014ee1b(2148855323)                  0x000000008014ee1b(2148855323)                  
s7(x23)             0x000000008017fb6b(2149055339)                  0x000000008017fb6b(2149055339)                  
s8(x24)             0x00000000801800c4(2149056708)                  0x00000000801800c4(2149056708)                  
s9(x25)             0x0000000080184d0e(2149076238)                  0x0000000080184d0e(2149076238)                  
s10(x26)            0x00000000801deb6b(2149444459)                  0x00000000801deb6b(2149444459)                  
s11(x27)            0x000000008014f65c(2148857436)                  0x000000008014f65c(2148857436)                  
t3(x28)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t4(x29)             0x00000000801800c4(2149056708)                  0x00000000801800c4(2149056708)                  
t5(x30)             0x00000000000000de(222)                         0x00000000000000de(222)                         
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            61a01a308e1f89090787b914643b4df7580076cc        61a01a308e1f89090787b914643b4df7580076cc        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b03af1e563e6427d00fd76db19a41cde5d93e9f1        X
lastPC              0x000000008000074c(2147485516)                  0x000000008000074c(2147485516)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000077(119)                         0x0000000000000077(119)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            True                                            True                                            
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f4                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f5                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f6                  0x4063000000000000(152.0_d)                     0x4063000000000000(152.0_d)                     
f7                  0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f10                 0xffffffff4f000002(2147484160.0_s)              0xffffffff4f000002(2147484160.0_s)              
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffffffff7c00(inf_h)                       0xffffffffffff7c00(inf_h)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f15                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f16                 0xffffffff4f0027fa(2150103552.0_s)              0xffffffff4f0027fa(2150103552.0_s)              
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff4f0017fa(2149054976.0_s)              0xffffffff4f0017fa(2149054976.0_s)              
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0x41dffffffb400000(2147483629.0_d)              0x41dffffffb400000(2147483629.0_d)              
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x4063000000000000(152.0_d)                     0x4063000000000000(152.0_d)                     
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

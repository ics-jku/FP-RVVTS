# FailID_002015 VP++ FF neg RV64 fsh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2015
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0xa0,0x68,0x40
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0xfd,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x80,0x3f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f19:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x30
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7ffffc01            // ra
    li x2, 0x22                  // sp
    li x3, 0x1                   // gp
    li x4, 0x801                 // tp
    li x5, 0x8017f91d            // t0
    li x6, 0x8017fbdd            // t1
    li x7, 0x51                  // t2
    li x8, 0x0                   // fp
    li x9, 0x80000057            // s1
    li x10, 0x8017fd28           // a0
    li x11, 0x800003a3           // a1
    li x12, 0x80180791           // a2
    li x13, 0x801802ff           // a3
    li x14, 0x8000034c           // a4
    li x15, 0x8017ff1f           // a5
    li x16, 0x8027fc74           // a6
    li x17, 0xb8d                // a7
    li x18, 0x800007d8           // s2
    li x19, 0x0                  // s3
    li x20, 0x8017ff1f           // s4
    li x21, 0x61f                // s5
    li x22, 0x4068a000           // s6
    li x23, 0x6000               // s7
    li x24, 0x1                  // s8
    li x25, 0x8017fd24           // s9
    li x26, 0x1                  // s10
    li x27, 0x6000               // s11
    li x28, 0xfffffffffffff473   // t3
    li x29, 0x493de000           // t4
    li x30, 0x8020006a           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'f7', 'x14'}, 'clob': {'x10', 'x14'}})
    
    li x10, 0xffffe
    and x14, x14, x10
    li x10, 0x8017fc7c
    add x14, x14, x10
    fsh f7, 0x384(x14)
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
Instruction: fsh f7, 0x384(x14)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f7, x384, x14
a4(x14)             0x000000008017ffc8(2149056456)                  0x000000008017ffc8(2149056456)
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffffc01(2147482625)                  0x000000007ffffc01(2147482625)                  
sp(x2)              0x0000000000000022(34)                          0x0000000000000022(34)                          
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x0000000000000801(2049)                        0x0000000000000801(2049)                        
t0(x5)              0x000000008017f91d(2149054749)                  0x000000008017f91d(2149054749)                  
t1(x6)              0x000000008017fbdd(2149055453)                  0x000000008017fbdd(2149055453)                  
t2(x7)              0x0000000000000051(81)                          0x0000000000000051(81)                          
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x0000000080000057(2147483735)                  0x0000000080000057(2147483735)                  
a0(x10)             0x000000008017fc7c(2149055612)                  0x000000008017fc7c(2149055612)                  
a1(x11)             0x00000000800003a3(2147484579)                  0x00000000800003a3(2147484579)                  
a2(x12)             0x0000000080180791(2149058449)                  0x0000000080180791(2149058449)                  
a3(x13)             0x00000000801802ff(2149057279)                  0x00000000801802ff(2149057279)                  
a4(x14)             0x000000008017ffc8(2149056456)                  0x000000008017ffc8(2149056456)                  
a5(x15)             0x000000008017ff1f(2149056287)                  0x000000008017ff1f(2149056287)                  
a6(x16)             0x000000008027fc74(2150104180)                  0x000000008027fc74(2150104180)                  
a7(x17)             0x0000000000000b8d(2957)                        0x0000000000000b8d(2957)                        
s2(x18)             0x00000000800007d8(2147485656)                  0x00000000800007d8(2147485656)                  
s3(x19)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s4(x20)             0x000000008017ff1f(2149056287)                  0x000000008017ff1f(2149056287)                  
s5(x21)             0x000000000000061f(1567)                        0x000000000000061f(1567)                        
s6(x22)             0x000000004068a000(1080598528)                  0x000000004068a000(1080598528)                  
s7(x23)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s8(x24)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s9(x25)             0x000000008017fd24(2149055780)                  0x000000008017fd24(2149055780)                  
s10(x26)            0x0000000000000001(1)                           0x0000000000000001(1)                           
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0xfffffffffffff473(18446744073709548659)        0xfffffffffffff473(18446744073709548659)        
t4(x29)             0x00000000493de000(1228791808)                  0x00000000493de000(1228791808)                  
t5(x30)             0x000000008020006a(2149580906)                  0x000000008020006a(2149580906)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            8b0efa5af7583b189e0020387134d0d0c477b129        8b0efa5af7583b189e0020387134d0d0c477b129        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000073c(2147485500)                  0x000000008000073c(2147485500)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000030(48)                          0x0000000000000030(48)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x4068a00000000000(197.0_d)                     0x4068a00000000000(197.0_d)                     
f2                  0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f10                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff4efffffd(2147483264.0_s)              0xffffffff4efffffd(2147483264.0_s)              
f15                 0xffffffff3f800000(1.0_s)                       0xffffffff3f800000(1.0_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f19                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

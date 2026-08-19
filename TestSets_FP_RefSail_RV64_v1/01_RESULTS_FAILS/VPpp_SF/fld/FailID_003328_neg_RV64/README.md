# FailID_003328 VP++ SF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3328
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f1: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xd0,0x42,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x63,0x40
_reg_f19:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0xfa,0x17,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0x00,0x00,0x80,0x46,0x00,0x00,0xe0,0x41
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rne(0b000)', 'res': 0}
    li t0, 0x4
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x800004c9            // ra
    li x2, 0x801ff55f            // sp
    li x3, 0x800007b8            // gp
    li x4, 0x40                  // tp
    li x5, 0x644fa000            // t0
    li x6, 0x7ffffd6c            // t1
    li x7, 0x612                 // t2
    li x8, 0x80                  // fp
    li x9, 0xfffffffffffffdf6    // s1
    li x10, 0x32cc871c           // a0
    li x11, 0x8017fa92           // a1
    li x12, 0x1b                 // a2
    li x13, 0x0                  // a3
    li x14, 0x8017fd17           // a4
    li x15, 0x81                 // a5
    li x16, 0x8000012c           // a6
    li x17, 0xffffffffffffffff   // a7
    li x18, 0x80006008           // s2
    li x19, 0x1                  // s3
    li x20, 0x80185e86           // s4
    li x21, 0xffffffffffffffff   // s5
    li x22, 0x16                 // s6
    li x23, 0xfc06c714           // s7
    li x24, 0x4                  // s8
    li x25, 0x4ea5c000           // s9
    li x26, 0x6000               // s10
    li x27, 0x80000838           // s11
    li x28, 0x8017f8e4           // t3
    li x29, 0x0                  // t4
    li x30, 0x6000               // t5
    li x31, 0x8007f5d8           // t6
    // INSTRUCTION ({'dep': {'x5', 'fcsr.rm', 'mstatus.fs/vs.fs'}, 'clob': {'x13', 'x5', 'f30'}})
    
    li x13, 0x1ffff8
    and x5, x5, x13
    li x13, 0x7fffff37
    add x5, x5, x13
    fld f30, 0xc9(x5)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f30                 0x4063000000000000(152.0_d)                     0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f30, 0xc9(x5)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f30                 0x4063000000000000(152.0_d)                     0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f30, xc9, x5
t0(x5)              0x00000000800f9f37(2148507447)                  0x00000000800f9f37(2148507447)
f30                 0x4063000000000000(152.0_d)                     0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000800004c9(2147484873)                  0x00000000800004c9(2147484873)                  
sp(x2)              0x00000000801ff55f(2149578079)                  0x00000000801ff55f(2149578079)                  
gp(x3)              0x00000000800007b8(2147485624)                  0x00000000800007b8(2147485624)                  
tp(x4)              0x0000000000000040(64)                          0x0000000000000040(64)                          
t0(x5)              0x00000000800f9f37(2148507447)                  0x00000000800f9f37(2148507447)                  
t1(x6)              0x000000007ffffd6c(2147482988)                  0x000000007ffffd6c(2147482988)                  
t2(x7)              0x0000000000000612(1554)                        0x0000000000000612(1554)                        
fp(x8)              0x0000000000000080(128)                         0x0000000000000080(128)                         
s1(x9)              0xfffffffffffffdf6(18446744073709551094)        0xfffffffffffffdf6(18446744073709551094)        
a0(x10)             0x0000000032cc871c(852264732)                   0x0000000032cc871c(852264732)                   
a1(x11)             0x000000008017fa92(2149055122)                  0x000000008017fa92(2149055122)                  
a2(x12)             0x000000000000001b(27)                          0x000000000000001b(27)                          
a3(x13)             0x000000007fffff37(2147483447)                  0x000000007fffff37(2147483447)                  
a4(x14)             0x000000008017fd17(2149055767)                  0x000000008017fd17(2149055767)                  
a5(x15)             0x0000000000000081(129)                         0x0000000000000081(129)                         
a6(x16)             0x000000008000012c(2147483948)                  0x000000008000012c(2147483948)                  
a7(x17)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s2(x18)             0x0000000080006008(2147508232)                  0x0000000080006008(2147508232)                  
s3(x19)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s4(x20)             0x0000000080185e86(2149080710)                  0x0000000080185e86(2149080710)                  
s5(x21)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s6(x22)             0x0000000000000016(22)                          0x0000000000000016(22)                          
s7(x23)             0x00000000fc06c714(4228302612)                  0x00000000fc06c714(4228302612)                  
s8(x24)             0x0000000000000004(4)                           0x0000000000000004(4)                           
s9(x25)             0x000000004ea5c000(1319485440)                  0x000000004ea5c000(1319485440)                  
s10(x26)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s11(x27)            0x0000000080000838(2147485752)                  0x0000000080000838(2147485752)                  
t3(x28)             0x000000008017f8e4(2149054692)                  0x000000008017f8e4(2149054692)                  
t4(x29)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t5(x30)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t6(x31)             0x000000008007f5d8(2148005336)                  0x000000008007f5d8(2148005336)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            74a1157eced103953c0a72e0a407f749811f2a07        74a1157eced103953c0a72e0a407f749811f2a07        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x000000008000071c(2147485468)                  0x000000008000071c(2147485468)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000004(4)                           0x0000000000000004(4)                           
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rne(0b000)                                      rne(0b000)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f1                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f2                  0xffffffff42d00000(104.0_s)                     0xffffffff42d00000(104.0_s)                     
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x4063000000000000(152.0_d)                     0x4063000000000000(152.0_d)                     
f19                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff4f0017fa(2149054976.0_s)              0xffffffff4f0017fa(2149054976.0_s)              
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0x41e0000046800000(2147484212.0_d)              0x41e0000046800000(2147484212.0_d)              
f30                 0x4063000000000000(152.0_d)                     0x0000000000000000(0.0_d)                       X
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

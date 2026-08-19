# FailID_001669 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1669
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
_reg_f0: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x60,0xd7,0xc4,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0xfe,0x1f,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f14:.byte 0xff,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xca,0x42,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x80,0x41,0x40
_reg_f23:.byte 0x2c,0x02,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
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
    li x1, 0x7ffffdaa            // ra
    li x2, 0xa6                  // sp
    li x3, 0x7ffffdaa            // gp
    li x4, 0x1                   // tp
    li x5, 0x2005                // t0
    li x6, 0x1                   // t1
    li x7, 0x0                   // t2
    li x8, 0x6000                // fp
    li x9, 0x0                   // s1
    li x10, 0x0                  // a0
    li x11, 0x801ffd1a           // a1
    li x12, 0x80000306           // a2
    li x13, 0xffffffffffffffff   // a3
    li x14, 0x6000               // a4
    li x15, 0x8017f91e           // a5
    li x16, 0x6000               // a6
    li x17, 0x801ffeee           // a7
    li x18, 0x460000000          // s2
    li x19, 0x8017f9ec           // s3
    li x20, 0x65                 // s4
    li x21, 0xffffffffc7b93000   // s5
    li x22, 0x0                  // s6
    li x23, 0xffffffffc7b930     // s7
    li x24, 0x50                 // s8
    li x25, 0x6000               // s9
    li x26, 0x0                  // s10
    li x27, 0x0                  // s11
    li x28, 0x8017f91e           // t3
    li x29, 0x8018066d           // t4
    li x30, 0x0                  // t5
    li x31, 0x7f                 // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'f11', 'mstatus.fs/vs.fs', 'x15'}, 'clob': {'x4', 'x15'}})
    
    li x4, 0xffff8
    and x15, x15, x4
    li x4, 0x8017fbcd
    add x15, x15, x4
    fsd f11, 0x433(x15)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b50cb903156cfbe0bd1cc90581b16e7aa06191e8        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f11, 0x433(x15)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b50cb903156cfbe0bd1cc90581b16e7aa06191e8        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f11, x433, x15
a5(x15)             0x00000000801ff4e5(2149577957)                  0x00000000801ff4e5(2149577957)
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007ffffdaa(2147483050)                  0x000000007ffffdaa(2147483050)                  
sp(x2)              0x00000000000000a6(166)                         0x00000000000000a6(166)                         
gp(x3)              0x000000007ffffdaa(2147483050)                  0x000000007ffffdaa(2147483050)                  
tp(x4)              0x000000008017fbcd(2149055437)                  0x000000008017fbcd(2149055437)                  
t0(x5)              0x0000000000002005(8197)                        0x0000000000002005(8197)                        
t1(x6)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x00000000801ffd1a(2149580058)                  0x00000000801ffd1a(2149580058)                  
a2(x12)             0x0000000080000306(2147484422)                  0x0000000080000306(2147484422)                  
a3(x13)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a4(x14)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a5(x15)             0x00000000801ff4e5(2149577957)                  0x00000000801ff4e5(2149577957)                  
a6(x16)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a7(x17)             0x00000000801ffeee(2149580526)                  0x00000000801ffeee(2149580526)                  
s2(x18)             0x0000000460000000(18790481920)                 0x0000000460000000(18790481920)                 
s3(x19)             0x000000008017f9ec(2149054956)                  0x000000008017f9ec(2149054956)                  
s4(x20)             0x0000000000000065(101)                         0x0000000000000065(101)                         
s5(x21)             0xffffffffc7b93000(18446744072765386752)        0xffffffffc7b93000(18446744072765386752)        
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x00ffffffffc7b930(72057594034239792)           0x00ffffffffc7b930(72057594034239792)           
s8(x24)             0x0000000000000050(80)                          0x0000000000000050(80)                          
s9(x25)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x000000008017f91e(2149054750)                  0x000000008017f91e(2149054750)                  
t4(x29)             0x000000008018066d(2149058157)                  0x000000008018066d(2149058157)                  
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x000000000000007f(127)                         0x000000000000007f(127)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            f1b1ede7328309222d44b8fe3a55c0d736241068        f1b1ede7328309222d44b8fe3a55c0d736241068        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b50cb903156cfbe0bd1cc90581b16e7aa06191e8        X
lastPC              0x0000000080000700(2147485440)                  0x0000000080000700(2147485440)                  
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
f0                  0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f1                  0xffffffffc4d76000(-1723.0_s)                   0xffffffffc4d76000(-1723.0_s)                   
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f5                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff4f001ffe(2149580288.0_s)              0xffffffff4f001ffe(2149580288.0_s)              
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f14                 0xffffffff4effffff(2147483520.0_s)              0xffffffff4effffff(2147483520.0_s)              
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0xffffffff42ca0000(101.0_s)                     0xffffffff42ca0000(101.0_s)                     
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x4041800000000000(35.0_d)                      0x4041800000000000(35.0_d)                      
f23                 0x000000008018022c(1.0617752683e-314_d)         0x000000008018022c(1.0617752683e-314_d)         
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

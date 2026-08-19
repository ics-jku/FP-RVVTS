# FailID_000827 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 827
* Isolated failing instruction: `fld`
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
_reg_f0: .byte 0xb1,0x0b,0x66,0x75,0x55,0xeb,0x95,0x3b
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x2f,0x06,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x34,0xcb,0x62,0x79,0x17,0x41,0xae,0x14
_reg_f15:.byte 0x2f,0x06,0x00,0x80,0xff,0xff,0xff,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f17:.byte 0x92,0xff,0x7f,0x4f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x27,0xb8,0x21,0x14,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x74,0xfd,0x62,0x8b,0xb4,0xb7,0x5c,0xdb
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x80,0xf9,0xc8,0x00,0xca,0x41
_reg_f28:.byte 0x27,0xb8,0x21,0x14,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x80,0xbf,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x7d
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x801801a7            // ra
    li x2, 0xffffffffffffffff    // sp
    li x3, 0x6000                // gp
    li x4, 0x0                   // tp
    li x5, 0x0                   // t0
    li x6, 0xffffffffffffffff    // t1
    li x7, 0x8000062f            // t2
    li x8, 0x7fffffffffffffff    // fp
    li x9, 0x7ffffe34            // s1
    li x10, 0xffffffffffffffff   // a0
    li x11, 0x7ffffab4           // a1
    li x12, 0xfffffffff9800000   // a2
    li x13, 0x801806e6           // a3
    li x14, 0x1ff                // a4
    li x15, 0x8017ffe2           // a5
    li x16, 0x80186327           // a6
    li x17, 0xffffffffffff91f3   // a7
    li x18, 0x200                // s2
    li x19, 0x80180327           // s3
    li x20, 0x0                  // s4
    li x21, 0x0                  // s5
    li x22, 0x0                  // s6
    li x23, 0x8027f400           // s7
    li x24, 0x0                  // s8
    li x25, 0x1                  // s9
    li x26, 0x6000               // s10
    li x27, 0x801ff836           // s11
    li x28, 0x8017fefa           // t3
    li x29, 0x1                  // t4
    li x30, 0x340191f3           // t5
    li x31, 0x2005ffbe80000      // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x11'}, 'clob': {'f13', 'x26', 'x11'}})
    
    li x26, 0x1ffff8
    and x11, x11, x26
    li x26, 0x800001c0
    add x11, x11, x26
    fld f13, -0x1c0(x11)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f13, -0x1c0(x11)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f13                 0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f13, x1, c0, x11
ra(x1)              0x00000000801801a7(2149056935)                  0x00000000801801a7(2149056935)
a1(x11)             0x00000000801ffc70(2149579888)                  0x00000000801ffc70(2149579888)
f13                 0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000801801a7(2149056935)                  0x00000000801801a7(2149056935)                  
sp(x2)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
gp(x3)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t1(x6)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t2(x7)              0x000000008000062f(2147485231)                  0x000000008000062f(2147485231)                  
fp(x8)              0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
s1(x9)              0x000000007ffffe34(2147483188)                  0x000000007ffffe34(2147483188)                  
a0(x10)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a1(x11)             0x00000000801ffc70(2149579888)                  0x00000000801ffc70(2149579888)                  
a2(x12)             0xfffffffff9800000(18446744073600499712)        0xfffffffff9800000(18446744073600499712)        
a3(x13)             0x00000000801806e6(2149058278)                  0x00000000801806e6(2149058278)                  
a4(x14)             0x00000000000001ff(511)                         0x00000000000001ff(511)                         
a5(x15)             0x000000008017ffe2(2149056482)                  0x000000008017ffe2(2149056482)                  
a6(x16)             0x0000000080186327(2149081895)                  0x0000000080186327(2149081895)                  
a7(x17)             0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)        
s2(x18)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s3(x19)             0x0000000080180327(2149057319)                  0x0000000080180327(2149057319)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x000000008027f400(2150102016)                  0x000000008027f400(2150102016)                  
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s10(x26)            0x00000000800001c0(2147484096)                  0x00000000800001c0(2147484096)                  
s11(x27)            0x00000000801ff836(2149578806)                  0x00000000801ff836(2149578806)                  
t3(x28)             0x000000008017fefa(2149056250)                  0x000000008017fefa(2149056250)                  
t4(x29)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t5(x30)             0x00000000340191f3(872518131)                   0x00000000340191f3(872518131)                   
t6(x31)             0x0002005ffbe80000(563362201600000)             0x0002005ffbe80000(563362201600000)             

STATE               REF                                             DUT                                             DIFF
xmemhash            42bf17cf92d5f54e6de669be166779ebdea7114b        42bf17cf92d5f54e6de669be166779ebdea7114b        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000718(2147485464)                  0x0000000080000718(2147485464)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000007d(125)                         0x000000000000007d(125)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x3b95eb5575660bb1(1.1603966371566636e-21_d)    0x3b95eb5575660bb1(1.1603966371566636e-21_d)    
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f3                  0xffffffff8000062f(-2.2182554690261854e-42_s)   0xffffffff8000062f(-2.2182554690261854e-42_s)   
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f12                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f13                 0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
f14                 0x14ae41177962cb34(4.601290157299096e-209_d)    0x14ae41177962cb34(4.601290157299096e-209_d)    
f15                 0x7fffffff8000062f(nan_d)                       0x7fffffff8000062f(nan_d)                       
f16                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f17                 0xffffffff4f7fff92(4294939136.0_s)              0xffffffff4f7fff92(4294939136.0_s)              
f18                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffff1421b827(8.164740413544605e-27_s)     0xffffffff1421b827(8.164740413544605e-27_s)     
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xdb5cb7b48b62fd74(-1.2739906469983861e+132_d)  0xdb5cb7b48b62fd74(-1.2739906469983861e+132_d)  
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x41ca00c8f9800000(872518131.0_d)               0x41ca00c8f9800000(872518131.0_d)               
f28                 0xffffffff1421b827(8.164740413544605e-27_s)     0xffffffff1421b827(8.164740413544605e-27_s)     
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffffbf800000(-1.0_s)                      0xffffffffbf800000(-1.0_s)                      
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

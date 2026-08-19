# FailID_003985 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3985
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0xa0,0xa9,0x00,0x00,0xe0,0x41
_reg_f12:.byte 0x00,0x00,0x00,0x90,0xfe,0xff,0x7f,0x41
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x1f,0x0e,0x49,0xca,0x93,0x07,0x92,0xd1
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f16:.byte 0x00,0x00,0x00,0x2d,0x00,0x00,0xe0,0x41
_reg_f17:.byte 0x5a,0x7c,0x7c,0x84,0x6d,0x5a,0x28,0xba
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x00,0xe0,0x42,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x44,0x53,0x8e,0x0e,0x33,0x02,0xb8,0x29
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x70
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
    li x3, 0x1                   // gp
    li x4, 0x7ffff919            // tp
    li x5, 0x8018035c            // t0
    li x6, 0x801804e9            // t1
    li x7, 0x8018034d            // t2
    li x8, 0x800d722b            // fp
    li x9, 0x82                  // s1
    li x10, 0x80200619           // a0
    li x11, 0x800061b2           // a1
    li x12, 0x7ffff949           // a2
    li x13, 0x0                  // a3
    li x14, 0x8018034d           // a4
    li x15, 0x1                  // a5
    li x16, 0x3b                 // a6
    li x17, 0x0                  // a7
    li x18, 0x200                // s2
    li x19, 0x800006e7           // s3
    li x20, 0x800004d4           // s4
    li x21, 0x0                  // s5
    li x22, 0x80200691           // s6
    li x23, 0x0                  // s7
    li x24, 0x8000011a           // s8
    li x25, 0x8018021f           // s9
    li x26, 0x97                 // s10
    li x27, 0x0                  // s11
    li x28, 0x8000054d           // t3
    li x29, 0x7ffffe19           // t4
    li x30, 0x854871c            // t5
    li x31, 0x80180625           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x25'}, 'clob': {'x25', 'f25', 'x2'}})
    
    li x2, 0x1ffffc
    and x25, x25, x2
    li x2, 0x7ffffa0e
    add x25, x25, x2
    flw f25, 0x5f2(x25)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f25                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f25, 0x5f2(x25)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f25                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f25, x5, f2, x25
t0(x5)              0x000000008018035c(2149057372)                  0x000000008018035c(2149057372)
s9(x25)             0x000000008017fc2a(2149055530)                  0x000000008017fc2a(2149055530)
f2                  0xffffffff80000000(-0.0_s)                      0xffffffff80000000(-0.0_s)
f25                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
sp(x2)              0x000000007ffffa0e(2147482126)                  0x000000007ffffa0e(2147482126)                  
gp(x3)              0x0000000000000001(1)                           0x0000000000000001(1)                           
tp(x4)              0x000000007ffff919(2147481881)                  0x000000007ffff919(2147481881)                  
t0(x5)              0x000000008018035c(2149057372)                  0x000000008018035c(2149057372)                  
t1(x6)              0x00000000801804e9(2149057769)                  0x00000000801804e9(2149057769)                  
t2(x7)              0x000000008018034d(2149057357)                  0x000000008018034d(2149057357)                  
fp(x8)              0x00000000800d722b(2148364843)                  0x00000000800d722b(2148364843)                  
s1(x9)              0x0000000000000082(130)                         0x0000000000000082(130)                         
a0(x10)             0x0000000080200619(2149582361)                  0x0000000080200619(2149582361)                  
a1(x11)             0x00000000800061b2(2147508658)                  0x00000000800061b2(2147508658)                  
a2(x12)             0x000000007ffff949(2147481929)                  0x000000007ffff949(2147481929)                  
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x000000008018034d(2149057357)                  0x000000008018034d(2149057357)                  
a5(x15)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a6(x16)             0x000000000000003b(59)                          0x000000000000003b(59)                          
a7(x17)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s2(x18)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s3(x19)             0x00000000800006e7(2147485415)                  0x00000000800006e7(2147485415)                  
s4(x20)             0x00000000800004d4(2147484884)                  0x00000000800004d4(2147484884)                  
s5(x21)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s6(x22)             0x0000000080200691(2149582481)                  0x0000000080200691(2149582481)                  
s7(x23)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s8(x24)             0x000000008000011a(2147483930)                  0x000000008000011a(2147483930)                  
s9(x25)             0x000000008017fc2a(2149055530)                  0x000000008017fc2a(2149055530)                  
s10(x26)            0x0000000000000097(151)                         0x0000000000000097(151)                         
s11(x27)            0x0000000000000000(0)                           0x0000000000000000(0)                           
t3(x28)             0x000000008000054d(2147485005)                  0x000000008000054d(2147485005)                  
t4(x29)             0x000000007ffffe19(2147483161)                  0x000000007ffffe19(2147483161)                  
t5(x30)             0x000000000854871c(139757340)                   0x000000000854871c(139757340)                   
t6(x31)             0x0000000080180625(2149058085)                  0x0000000080180625(2149058085)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            53d8fce822bbcca273a3f285f9dcd0ff33078739        53d8fce822bbcca273a3f285f9dcd0ff33078739        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000730(2147485488)                  0x0000000080000730(2147485488)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000070(112)                         0x0000000000000070(112)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff80000000(-0.0_s)                      0xffffffff80000000(-0.0_s)                      
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7fffffff46c00000(nan_d)                       0x7fffffff46c00000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x41e00000a9a00000(2147485005.0_d)              0x41e00000a9a00000(2147485005.0_d)              
f12                 0x417ffffe90000000(33554409.0_d)                0x417ffffe90000000(33554409.0_d)                
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xd1920793ca490e1f(-8.756385205883228e+84_d)    0xd1920793ca490e1f(-8.756385205883228e+84_d)    
f15                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f16                 0x41e000002d000000(2147484008.0_d)              0x41e000002d000000(2147484008.0_d)              
f17                 0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   0xba285a6d847c7c5a(-1.5369051125236202e-28_d)   
f18                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f19                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f20                 0xffffffff42e00000(112.0_s)                     0xffffffff42e00000(112.0_s)                     
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0x29b802330e8e5344(1.0222761870252597e-107_d)   0x29b802330e8e5344(1.0222761870252597e-107_d)   
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0x7ff8000000000000(nan_d)                       0xffffffff00000000(0.0_s)                       X
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffffffff0000(0.0_h)                       0xffffffffffff0000(0.0_h)                       
f30                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f31                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
STATES DIFFER: True
```

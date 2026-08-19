# FailID_003925 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3925
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
_reg_f0: .byte 0x00,0x00,0x00,0xb2,0xff,0x02,0xe0,0x41
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0xdc,0x97,0x40
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x4f,0x7c,0xac,0x4e,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xd8,0x40
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0xff
_reg_f11:.byte 0xff,0x7b,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f12:.byte 0xf3,0xcf,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f14:.byte 0x00,0x00,0x80,0xf1,0xec,0xcf,0xea,0x41
_reg_f15:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f16:.byte 0x00,0xa0,0x77,0x4c,0x00,0x00,0x00,0x00
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f18:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0xc0,0x9d,0xff,0xff,0xdf,0x41
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x40,0x52,0xff,0xff,0xff,0xff
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
    li x1, 0x4000009b            // ra
    li x2, 0x51                  // sp
    li x3, 0xa59696d0            // gp
    li x4, 0x3b                  // tp
    li x5, 0x80000846            // t0
    li x6, 0x7ffffa28            // t1
    li x7, 0x0                   // t2
    li x8, 0x1                   // fp
    li x9, 0x0                   // s1
    li x10, 0x200                // a0
    li x11, 0x7ffffa1b           // a1
    li x12, 0x200                // a2
    li x13, 0x0                  // a3
    li x14, 0x0                  // a4
    li x15, 0x6000               // a5
    li x16, 0x1d0d66f4           // a6
    li x17, 0xcc                 // a7
    li x18, 0x4c                 // s2
    li x19, 0x1                  // s3
    li x20, 0xd5                 // s4
    li x21, 0x4c77a000           // s5
    li x22, 0x200                // s6
    li x23, 0x801ffa17           // s7
    li x24, 0x6000               // s8
    li x25, 0x800002e0           // s9
    li x26, 0x80180efc           // s10
    li x27, 0x801ff8d3           // s11
    li x28, 0x80000710           // t3
    li x29, 0x11                 // t4
    li x30, 0x8018017d           // t5
    li x31, 0x8027689d           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'x6', 'fcsr.rm'}, 'clob': {'x6', 'x17', 'f8'}})
    
    li x17, 0x1ffffc
    and x6, x6, x17
    li x17, 0x7ffff9b8
    add x6, x6, x17
    flw f8, 0x648(x6)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f8                  0xffffffff4eac7c4f(1446913920.0_s)              0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f8, 0x648(x6)
+========================================================================================================================+
Attributes:  fcsr ['invalid'], special values ['zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f8                  0xffffffff4eac7c4f(1446913920.0_s)              0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f8, x648, x6
t1(x6)              0x00000000801ff3e0(2149577696)                  0x00000000801ff3e0(2149577696)
f8                  0xffffffff4eac7c4f(1446913920.0_s)              0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000004000009b(1073741979)                  0x000000004000009b(1073741979)                  
sp(x2)              0x0000000000000051(81)                          0x0000000000000051(81)                          
gp(x3)              0x00000000a59696d0(2778109648)                  0x00000000a59696d0(2778109648)                  
tp(x4)              0x000000000000003b(59)                          0x000000000000003b(59)                          
t0(x5)              0x0000000080000846(2147485766)                  0x0000000080000846(2147485766)                  
t1(x6)              0x00000000801ff3e0(2149577696)                  0x00000000801ff3e0(2149577696)                  
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x0000000000000001(1)                           0x0000000000000001(1)                           
s1(x9)              0x0000000000000000(0)                           0x0000000000000000(0)                           
a0(x10)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a1(x11)             0x000000007ffffa1b(2147482139)                  0x000000007ffffa1b(2147482139)                  
a2(x12)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a3(x13)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x000000001d0d66f4(487417588)                   0x000000001d0d66f4(487417588)                   
a7(x17)             0x000000007ffff9b8(2147482040)                  0x000000007ffff9b8(2147482040)                  
s2(x18)             0x000000000000004c(76)                          0x000000000000004c(76)                          
s3(x19)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s4(x20)             0x00000000000000d5(213)                         0x00000000000000d5(213)                         
s5(x21)             0x000000004c77a000(1282908160)                  0x000000004c77a000(1282908160)                  
s6(x22)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s7(x23)             0x00000000801ffa17(2149579287)                  0x00000000801ffa17(2149579287)                  
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x00000000800002e0(2147484384)                  0x00000000800002e0(2147484384)                  
s10(x26)            0x0000000080180efc(2149060348)                  0x0000000080180efc(2149060348)                  
s11(x27)            0x00000000801ff8d3(2149578963)                  0x00000000801ff8d3(2149578963)                  
t3(x28)             0x0000000080000710(2147485456)                  0x0000000080000710(2147485456)                  
t4(x29)             0x0000000000000011(17)                          0x0000000000000011(17)                          
t5(x30)             0x000000008018017d(2149056893)                  0x000000008018017d(2149056893)                  
t6(x31)             0x000000008027689d(2150066333)                  0x000000008027689d(2150066333)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            d87f061ae3c17d5c830d2f0267c215d8ac545ea2        d87f061ae3c17d5c830d2f0267c215d8ac545ea2        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x00000000800006fc(2147485436)                  0x00000000800006fc(2147485436)                  
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
f0                  0x41e002ffb2000000(2149055888.0_d)              0x41e002ffb2000000(2149055888.0_d)              
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x4097dc0000000000(1527.0_d)                    0x4097dc0000000000(1527.0_d)                    
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f8                  0xffffffff4eac7c4f(1446913920.0_s)              0xffffffff00000000(0.0_s)                       X
f9                  0x40d8000000000000(24576.0_d)                   0x40d8000000000000(24576.0_d)                   
f10                 0xfff8000000000000(nan_d)                       0xfff8000000000000(nan_d)                       
f11                 0xffffffffffff7bff(65504.0_h)                   0xffffffffffff7bff(65504.0_h)                   
f12                 0xffffffffceffcff3(-2145909120.0_s)             0xffffffffceffcff3(-2145909120.0_s)             
f13                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f14                 0x41eacfecf1800000(3598673804.0_d)              0x41eacfecf1800000(3598673804.0_d)              
f15                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f16                 0x000000004c77a000(6.338408486e-315_d)          0x000000004c77a000(6.338408486e-315_d)          
f17                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f18                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x41dfffff9dc00000(2147483255.0_d)              0x41dfffff9dc00000(2147483255.0_d)              
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff52400000(206158430208.0_s)            0xffffffff52400000(206158430208.0_s)            
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

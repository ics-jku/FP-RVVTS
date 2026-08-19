# FailID_003945 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3945
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
_reg_f0: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x04,0x01,0x20,0x80,0x00,0x00,0x00,0x00
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f5: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x80,0xff,0x03,0xe0,0x41
_reg_f11:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0x00,0x80,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f16:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f20:.byte 0x20,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f21:.byte 0x1f,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x20,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': False, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x21
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8000008f            // ra
    li x2, 0x80180671            // sp
    li x3, 0x801fffea            // gp
    li x4, 0x8018007f            // tp
    li x5, 0x80000629            // t0
    li x6, 0x80180bf6            // t1
    li x7, 0x8001107b            // t2
    li x8, 0x0                   // fp
    li x9, 0x800000b0            // s1
    li x10, 0x8017faff           // a0
    li x11, 0x1                  // a1
    li x12, 0x1                  // a2
    li x13, 0x200                // a3
    li x14, 0x8018016b           // a4
    li x15, 0x801800e9           // a5
    li x16, 0x801802fd           // a6
    li x17, 0x8017f858           // a7
    li x18, 0x8017fc93           // s2
    li x19, 0x8017fe20           // s3
    li x20, 0x8                  // s4
    li x21, 0x7ffffc900          // s5
    li x22, 0x0                  // s6
    li x23, 0x2000017            // s7
    li x24, 0x7ffffe69           // s8
    li x25, 0x8017fd65           // s9
    li x26, 0x80000366           // s10
    li x27, 0x6000               // s11
    li x28, 0x801805d5           // t3
    li x29, 0x801ffd7d           // t4
    li x30, 0x801ff6e7           // t5
    li x31, 0xd3                 // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x7'}, 'clob': {'f30', 'x8', 'x7'}})
    
    li x8, 0x1ffffc
    and x7, x7, x8
    li x8, 0x800003da
    add x7, x7, x8
    flw f30, -0x3da(x7)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f30, -0x3da(x7)
+========================================================================================================================+
Attributes:  fcsr ['inexact'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f30, x3, x7
gp(x3)              0x00000000801fffea(2149580778)                  0x00000000801fffea(2149580778)
t2(x7)              0x0000000080011452(2147554386)                  0x0000000080011452(2147554386)
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008000008f(2147483791)                  0x000000008000008f(2147483791)                  
sp(x2)              0x0000000080180671(2149058161)                  0x0000000080180671(2149058161)                  
gp(x3)              0x00000000801fffea(2149580778)                  0x00000000801fffea(2149580778)                  
tp(x4)              0x000000008018007f(2149056639)                  0x000000008018007f(2149056639)                  
t0(x5)              0x0000000080000629(2147485225)                  0x0000000080000629(2147485225)                  
t1(x6)              0x0000000080180bf6(2149059574)                  0x0000000080180bf6(2149059574)                  
t2(x7)              0x0000000080011452(2147554386)                  0x0000000080011452(2147554386)                  
fp(x8)              0x00000000800003da(2147484634)                  0x00000000800003da(2147484634)                  
s1(x9)              0x00000000800000b0(2147483824)                  0x00000000800000b0(2147483824)                  
a0(x10)             0x000000008017faff(2149055231)                  0x000000008017faff(2149055231)                  
a1(x11)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a2(x12)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a3(x13)             0x0000000000000200(512)                         0x0000000000000200(512)                         
a4(x14)             0x000000008018016b(2149056875)                  0x000000008018016b(2149056875)                  
a5(x15)             0x00000000801800e9(2149056745)                  0x00000000801800e9(2149056745)                  
a6(x16)             0x00000000801802fd(2149057277)                  0x00000000801802fd(2149057277)                  
a7(x17)             0x000000008017f858(2149054552)                  0x000000008017f858(2149054552)                  
s2(x18)             0x000000008017fc93(2149055635)                  0x000000008017fc93(2149055635)                  
s3(x19)             0x000000008017fe20(2149056032)                  0x000000008017fe20(2149056032)                  
s4(x20)             0x0000000000000008(8)                           0x0000000000000008(8)                           
s5(x21)             0x00000007ffffc900(34359724288)                 0x00000007ffffc900(34359724288)                 
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000002000017(33554455)                    0x0000000002000017(33554455)                    
s8(x24)             0x000000007ffffe69(2147483241)                  0x000000007ffffe69(2147483241)                  
s9(x25)             0x000000008017fd65(2149055845)                  0x000000008017fd65(2149055845)                  
s10(x26)            0x0000000080000366(2147484518)                  0x0000000080000366(2147484518)                  
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x00000000801805d5(2149058005)                  0x00000000801805d5(2149058005)                  
t4(x29)             0x00000000801ffd7d(2149580157)                  0x00000000801ffd7d(2149580157)                  
t5(x30)             0x00000000801ff6e7(2149578471)                  0x00000000801ff6e7(2149578471)                  
t6(x31)             0x00000000000000d3(211)                         0x00000000000000d3(211)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            9aedd75866c518b656bed7fafce3734b32fbc4a2        9aedd75866c518b656bed7fafce3734b32fbc4a2        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000780(2147485568)                  0x0000000080000780(2147485568)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000021(33)                          0x0000000000000021(33)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0xffffffff4f001800(2149056512.0_s)              0xffffffff4f001800(2149056512.0_s)              
f2                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f3                  0x0000000080200104(1.0620341547e-314_d)         0x0000000080200104(1.0620341547e-314_d)         
f4                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f5                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x41e003ff80000000(2149579776.0_d)              0x41e003ff80000000(2149579776.0_d)              
f11                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff80000000(-0.0_s)                      0xffffffff80000000(-0.0_s)                      
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f16                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f19                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f20                 0x0000000000000020(1.6e-322_d)                  0x0000000000000020(1.6e-322_d)                  
f21                 0xffffffff0000001f(4.344025239406933e-44_s)     0xffffffff0000001f(4.344025239406933e-44_s)     
f22                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x0000000000000020(1.6e-322_d)                  0x0000000000000020(1.6e-322_d)                  
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff00000000(0.0_s)                       X
f31                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
STATES DIFFER: True
```

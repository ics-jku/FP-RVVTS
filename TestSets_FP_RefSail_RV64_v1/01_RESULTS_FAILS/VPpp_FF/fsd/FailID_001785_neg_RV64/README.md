# FailID_001785 VP++ FF neg RV64 fsd

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 1785
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0xe0,0xb5,0xff,0x02,0xe0,0x41
_reg_f4: .byte 0x2c,0x46,0xac,0x3c,0x1f,0x11,0x3b,0x09
_reg_f5: .byte 0xa3,0x21,0xca,0x65,0x8e,0x35,0x7b,0xce
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x09,0xc0,0xff,0xce,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xe0,0x9d,0xfe,0x04,0xe0,0x41
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0xa9,0xcf,0x62,0x49,0x57,0xe7,0xda,0x97
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x90,0x0d,0x95,0x9b,0x78,0xd2,0xcd,0xed
_reg_f15:.byte 0xa3,0x21,0xca,0x65,0x8e,0x35,0x7b,0x4e
_reg_f16:.byte 0x00,0x00,0x80,0x5f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0xee,0x00,0x18,0x80,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x50,0x40
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xe0,0xb5,0xff,0x02,0xe0,0xc1
_reg_f30:.byte 0xa3,0x21,0xca,0x65,0x8e,0x35,0x7b,0xce
_reg_f31:.byte 0x00,0x00,0x00,0x48,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'res1(0b110)', 'res': 0}
    li t0, 0xc4
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x7227a000            // ra
    li x2, 0x801806ff            // sp
    li x3, 0x8018063c            // gp
    li x4, 0x7ffffcd7            // tp
    li x5, 0x802801ab            // t0
    li x6, 0x1                   // t1
    li x7, 0x801ced6c            // t2
    li x8, 0x800007f7            // fp
    li x9, 0x415                 // s1
    li x10, 0x80000767           // a0
    li x11, 0x91f3               // a1
    li x12, 0x8017fa2d           // a2
    li x13, 0x1                  // a3
    li x14, 0x801800ee           // a4
    li x15, 0x1003001dc          // a5
    li x16, 0x801866ff           // a6
    li x17, 0x4                  // a7
    li x18, 0xbd                 // s2
    li x19, 0x8017ffc6           // s3
    li x20, 0x4000               // s4
    li x21, 0x7ffffeb6           // s5
    li x22, 0x3d                 // s6
    li x23, 0x0                  // s7
    li x24, 0x7ffffd0b           // s8
    li x25, 0x8017f969           // s9
    li x26, 0x0                  // s10
    li x27, 0x1                  // s11
    li x28, 0x80186088           // t3
    li x29, 0x80242edb           // t4
    li x30, 0x80180283           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x8', 'mstatus.fs/vs.fs', 'f20'}, 'clob': {'x8', 'x23'}})
    
    li x23, 0xffff8
    and x8, x8, x23
    li x23, 0x8017feb4
    add x8, x8, x23
    fsd f20, 0x14c(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        4fc1289b455aa04192fd10b96838b0612cb5cc8a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsd f20, 0x14c(x8)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        4fc1289b455aa04192fd10b96838b0612cb5cc8a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f20, x14, x8
fp(x8)              0x00000000801806a4(2149058212)                  0x00000000801806a4(2149058212)
a4(x14)             0x00000000801800ee(2149056750)                  0x00000000801800ee(2149056750)
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000007227a000(1915199488)                  0x000000007227a000(1915199488)                  
sp(x2)              0x00000000801806ff(2149058303)                  0x00000000801806ff(2149058303)                  
gp(x3)              0x000000008018063c(2149058108)                  0x000000008018063c(2149058108)                  
tp(x4)              0x000000007ffffcd7(2147482839)                  0x000000007ffffcd7(2147482839)                  
t0(x5)              0x00000000802801ab(2150105515)                  0x00000000802801ab(2150105515)                  
t1(x6)              0x0000000000000001(1)                           0x0000000000000001(1)                           
t2(x7)              0x00000000801ced6c(2149379436)                  0x00000000801ced6c(2149379436)                  
fp(x8)              0x00000000801806a4(2149058212)                  0x00000000801806a4(2149058212)                  
s1(x9)              0x0000000000000415(1045)                        0x0000000000000415(1045)                        
a0(x10)             0x0000000080000767(2147485543)                  0x0000000080000767(2147485543)                  
a1(x11)             0x00000000000091f3(37363)                       0x00000000000091f3(37363)                       
a2(x12)             0x000000008017fa2d(2149055021)                  0x000000008017fa2d(2149055021)                  
a3(x13)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a4(x14)             0x00000000801800ee(2149056750)                  0x00000000801800ee(2149056750)                  
a5(x15)             0x00000001003001dc(4298113500)                  0x00000001003001dc(4298113500)                  
a6(x16)             0x00000000801866ff(2149082879)                  0x00000000801866ff(2149082879)                  
a7(x17)             0x0000000000000004(4)                           0x0000000000000004(4)                           
s2(x18)             0x00000000000000bd(189)                         0x00000000000000bd(189)                         
s3(x19)             0x000000008017ffc6(2149056454)                  0x000000008017ffc6(2149056454)                  
s4(x20)             0x0000000000004000(16384)                       0x0000000000004000(16384)                       
s5(x21)             0x000000007ffffeb6(2147483318)                  0x000000007ffffeb6(2147483318)                  
s6(x22)             0x000000000000003d(61)                          0x000000000000003d(61)                          
s7(x23)             0x000000008017feb4(2149056180)                  0x000000008017feb4(2149056180)                  
s8(x24)             0x000000007ffffd0b(2147482891)                  0x000000007ffffd0b(2147482891)                  
s9(x25)             0x000000008017f969(2149054825)                  0x000000008017f969(2149054825)                  
s10(x26)            0x0000000000000000(0)                           0x0000000000000000(0)                           
s11(x27)            0x0000000000000001(1)                           0x0000000000000001(1)                           
t3(x28)             0x0000000080186088(2149081224)                  0x0000000080186088(2149081224)                  
t4(x29)             0x0000000080242edb(2149854939)                  0x0000000080242edb(2149854939)                  
t5(x30)             0x0000000080180283(2149057155)                  0x0000000080180283(2149057155)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            a944a235f5e196d17707c96d939e0abe0639008a        a944a235f5e196d17707c96d939e0abe0639008a        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        4fc1289b455aa04192fd10b96838b0612cb5cc8a        X
lastPC              0x0000000080000754(2147485524)                  0x0000000080000754(2147485524)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000c4(196)                         0x00000000000000c4(196)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            res1(0b110)                                     res1(0b110)                                     
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f3                  0x41e002ffb5e00000(2149055919.0_d)              0x41e002ffb5e00000(2149055919.0_d)              
f4                  0x093b111f3cac462c(3.3577013057289645e-264_d)   0x093b111f3cac462c(3.3577013057289645e-264_d)   
f5                  0xce7b358e65ca21a3(-1.173693904724524e+70_d)    0xce7b358e65ca21a3(-1.173693904724524e+70_d)    
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffffceffc009(-2145387648.0_s)             0xffffffffceffc009(-2145387648.0_s)             
f8                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x41e004fe9de00000(2150102255.0_d)              0x41e004fe9de00000(2150102255.0_d)              
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0x97dae7574962cfa9(-9.213707466843409e-194_d)   0x97dae7574962cfa9(-9.213707466843409e-194_d)   
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xedcdd2789b950d90(-8.421817586531674e+220_d)   0xedcdd2789b950d90(-8.421817586531674e+220_d)   
f15                 0x4e7b358e65ca21a3(1.173693904724524e+70_d)     0x4e7b358e65ca21a3(1.173693904724524e+70_d)     
f16                 0xffffffff5f800000(1.8446744073709552e+19_s)    0xffffffff5f800000(1.8446744073709552e+19_s)    
f17                 0x00000000801800ee(1.061775111e-314_d)          0x00000000801800ee(1.061775111e-314_d)          
f18                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f24                 0x4050000000000000(64.0_d)                      0x4050000000000000(64.0_d)                      
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xc1e002ffb5e00000(-2149055919.0_d)             0xc1e002ffb5e00000(-2149055919.0_d)             
f30                 0xce7b358e65ca21a3(-1.173693904724524e+70_d)    0xce7b358e65ca21a3(-1.173693904724524e+70_d)    
f31                 0xffffffff48000000(131072.0_s)                  0xffffffff48000000(131072.0_s)                  
STATES DIFFER: True
```

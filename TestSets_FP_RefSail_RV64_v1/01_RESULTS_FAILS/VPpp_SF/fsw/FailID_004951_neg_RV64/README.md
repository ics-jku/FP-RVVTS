# FailID_004951 VP++ SF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 4951
* Isolated failing instruction: `fsw`
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
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x1e,0x42,0xb6,0x95,0xa0,0x48,0x46,0x9f
_reg_f3: .byte 0x0a,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0xae,0x9c,0x87,0xb5,0x7e,0xde,0x85,0x11
_reg_f5: .byte 0x05,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x9b,0x25,0x85,0xc7,0xb6,0xdb,0x93,0x15
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0xca,0x6f,0x89,0x02,0x46,0xc1,0xc1,0x18
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x40
_reg_f12:.byte 0x00,0x00,0x60,0x34,0x01,0x00,0xe0,0x41
_reg_f13:.byte 0x00,0x02,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0x7f
_reg_f15:.byte 0xbf,0x78,0xa6,0x02,0x5a,0x84,0x3c,0xb6
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x5e,0x38,0x71,0x04,0x60,0x21,0xb3,0x96
_reg_f18:.byte 0xbf,0x78,0xa6,0x02,0x5a,0x84,0x3c,0xb6
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x10,0x01,0x8c,0xce,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0xf8,0x45,0xc7,0xd5,0xcc,0x51,0xb3,0x76
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x10,0x01,0x8c,0xce,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x60,0x66,0x00,0x04,0xe0,0x41
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

    // restore fcsr = {'nx': True, 'uf': False, 'of': True, 'dz': True, 'nv': True, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x5d
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x80180389            // ra
    li x2, 0x8018067d            // sp
    li x3, 0x0                   // gp
    li x4, 0x5d                  // tp
    li x5, 0x6000                // t0
    li x6, 0xffffffff7fc00000    // t1
    li x7, 0x8000038f0000000     // t2
    li x8, 0xff98ad9c7c4320fe    // fp
    li x9, 0x8017fb50            // s1
    li x10, 0xb9ff7878           // a0
    li x11, 0x8018029c           // a1
    li x12, 0x1                  // a2
    li x13, 0x8018029c           // a3
    li x14, 0xf0                 // a4
    li x15, 0x1                  // a5
    li x16, 0x0                  // a6
    li x17, 0x8000038f0000000    // a7
    li x18, 0x200                // s2
    li x19, 0x8000038f           // s3
    li x20, 0x7589c6ba2de1c000   // s4
    li x21, 0x800005c8           // s5
    li x22, 0x80180589           // s6
    li x23, 0xffffffffffffffff   // s7
    li x24, 0x800                // s8
    li x25, 0x8b                 // s9
    li x26, 0x801912ce           // s10
    li x27, 0x6000               // s11
    li x28, 0x200                // t3
    li x29, 0x800005f3           // t4
    li x30, 0x800007d2           // t5
    li x31, 0x7ffffc7d           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x8', 'f9'}, 'clob': {'x29', 'x8'}})
    
    li x29, 0xffffc
    and x8, x8, x29
    li x29, 0x801806a8
    add x8, x8, x29
    fsw f9, -0x6a8(x8)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b7a13159b03084fc5b63edc698731fc65ba2920f        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f9, -0x6a8(x8)
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'overflow', 'div-by-0', 'inexact'], special values ['nan']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b7a13159b03084fc5b63edc698731fc65ba2920f        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f9, x6, a8, x8
t1(x6)              0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)
fp(x8)              0x00000000801b27a4(2149263268)                  0x00000000801b27a4(2149263268)
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000080180389(2149057417)                  0x0000000080180389(2149057417)                  
sp(x2)              0x000000008018067d(2149058173)                  0x000000008018067d(2149058173)                  
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x000000000000005d(93)                          0x000000000000005d(93)                          
t0(x5)              0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t1(x6)              0xffffffff7fc00000(18446744071557873664)        0xffffffff7fc00000(18446744071557873664)        
t2(x7)              0x08000038f0000000(576460996848123904)          0x08000038f0000000(576460996848123904)          
fp(x8)              0x00000000801b27a4(2149263268)                  0x00000000801b27a4(2149263268)                  
s1(x9)              0x000000008017fb50(2149055312)                  0x000000008017fb50(2149055312)                  
a0(x10)             0x00000000b9ff7878(3120527480)                  0x00000000b9ff7878(3120527480)                  
a1(x11)             0x000000008018029c(2149057180)                  0x000000008018029c(2149057180)                  
a2(x12)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a3(x13)             0x000000008018029c(2149057180)                  0x000000008018029c(2149057180)                  
a4(x14)             0x00000000000000f0(240)                         0x00000000000000f0(240)                         
a5(x15)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a6(x16)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a7(x17)             0x08000038f0000000(576460996848123904)          0x08000038f0000000(576460996848123904)          
s2(x18)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s3(x19)             0x000000008000038f(2147484559)                  0x000000008000038f(2147484559)                  
s4(x20)             0x7589c6ba2de1c000(8469519077182914560)         0x7589c6ba2de1c000(8469519077182914560)         
s5(x21)             0x00000000800005c8(2147485128)                  0x00000000800005c8(2147485128)                  
s6(x22)             0x0000000080180589(2149057929)                  0x0000000080180589(2149057929)                  
s7(x23)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s8(x24)             0x0000000000000800(2048)                        0x0000000000000800(2048)                        
s9(x25)             0x000000000000008b(139)                         0x000000000000008b(139)                         
s10(x26)            0x00000000801912ce(2149126862)                  0x00000000801912ce(2149126862)                  
s11(x27)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t3(x28)             0x0000000000000200(512)                         0x0000000000000200(512)                         
t4(x29)             0x00000000801806a8(2149058216)                  0x00000000801806a8(2149058216)                  
t5(x30)             0x00000000800007d2(2147485650)                  0x00000000800007d2(2147485650)                  
t6(x31)             0x000000007ffffc7d(2147482749)                  0x000000007ffffc7d(2147482749)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            49fec5162c731a6ff7d3c678b4b883a791a0d567        49fec5162c731a6ff7d3c678b4b883a791a0d567        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        b7a13159b03084fc5b63edc698731fc65ba2920f        X
lastPC              0x0000000080000768(2147485544)                  0x0000000080000768(2147485544)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000005d(93)                          0x000000000000005d(93)                          
 fcsr.nx            True                                            True                                            
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x9f4648a095b6421e(-5.072004083601017e-158_d)   0x9f4648a095b6421e(-5.072004083601017e-158_d)   
f3                  0xffffffff4f00000a(2147486208.0_s)              0xffffffff4f00000a(2147486208.0_s)              
f4                  0x1185de7eb5879cae(2.954095731229236e-224_d)    0x1185de7eb5879cae(2.954095731229236e-224_d)    
f5                  0xffffffff4f000005(2147484928.0_s)              0xffffffff4f000005(2147484928.0_s)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0x1593dbb6c785259b(9.896556315150118e-205_d)    0x1593dbb6c785259b(9.896556315150118e-205_d)    
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0x18c1c14602896fca(1.9924745797911558e-189_d)   0x18c1c14602896fca(1.9924745797911558e-189_d)   
f11                 0x4000000000000000(2.0_d)                       0x4000000000000000(2.0_d)                       
f12                 0x41e0000134600000(2147486115.0_d)              0x41e0000134600000(2147486115.0_d)              
f13                 0x0000000000000200(2.53e-321_d)                 0x0000000000000200(2.53e-321_d)                 
f14                 0x7fffffff7fc00000(nan_d)                       0x7fffffff7fc00000(nan_d)                       
f15                 0xb63c845a02a678bf(-1.9512122135603192e-47_d)   0xb63c845a02a678bf(-1.9512122135603192e-47_d)   
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x96b321600471385e(-2.4992303129212855e-199_d)  0x96b321600471385e(-2.4992303129212855e-199_d)  
f18                 0xb63c845a02a678bf(-1.9512122135603192e-47_d)   0xb63c845a02a678bf(-1.9512122135603192e-47_d)   
f19                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffffce8c0110(-1174439936.0_s)             0xffffffffce8c0110(-1174439936.0_s)             
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0x76b351ccd5c745f8(6.083490244268807e+263_d)    0x76b351ccd5c745f8(6.083490244268807e+263_d)    
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffffce8c0110(-1174439936.0_s)             0xffffffffce8c0110(-1174439936.0_s)             
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x41e0040066600000(2149581619.0_d)              0x41e0040066600000(2149581619.0_d)              
STATES DIFFER: True
```

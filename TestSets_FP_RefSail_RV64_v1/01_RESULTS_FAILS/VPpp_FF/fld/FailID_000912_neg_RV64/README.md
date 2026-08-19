# FailID_000912 VP++ FF neg RV64 fld

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 912
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
_reg_f0: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x9b,0x25,0x85,0xc7,0xb6,0xdb,0x93,0x15
_reg_f2: .byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x0a,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0xae,0x9c,0x87,0xb5,0x7e,0xde,0x85,0x11
_reg_f5: .byte 0x05,0x00,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x9b,0x25,0x85,0xc7,0xb6,0xdb,0x93,0x15
_reg_f8: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f9: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x26,0xfc,0x17,0x80,0x00,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0xbf,0x78,0xa6,0x02,0x5a,0x84,0x3c,0xb6
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x20,0xc5,0x00,0x00,0xe0,0x41
_reg_f19:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f20:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x70,0xc5,0xf1,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x12,0x19,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': True, 'dz': False, 'nv': False, 'rm': 'rdn(0b010)', 'res': 0}
    li t0, 0x44
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8000069c            // ra
    li x2, 0x0                   // sp
    li x3, 0x0                   // gp
    li x4, 0x400                 // tp
    li x5, 0x8018069f            // t0
    li x6, 0xffffffffffff91f3    // t1
    li x7, 0x0                   // t2
    li x8, 0x0                   // fp
    li x9, 0x1                   // s1
    li x10, 0x7ffffc14           // a0
    li x11, 0x8b433728           // a1
    li x12, 0x80180627           // a2
    li x13, 0x800003e4           // a3
    li x14, 0x1                  // a4
    li x15, 0x6000               // a5
    li x16, 0xb                  // a6
    li x17, 0x8018077a           // a7
    li x18, 0x1                  // s2
    li x19, 0x8017fd0c           // s3
    li x20, 0x1                  // s4
    li x21, 0x80180229           // s5
    li x22, 0x80180627           // s6
    li x23, 0x8017fe26           // s7
    li x24, 0x8017fbec           // s8
    li x25, 0x7ffffc14           // s9
    li x26, 0x8000585f           // s10
    li x27, 0x800c2b28           // s11
    li x28, 0xfffffffff2381000   // t3
    li x29, 0x801fff7c           // t4
    li x30, 0xf8                 // t5
    li x31, 0x8017fd88           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'mstatus.fs/vs.fs', 'x10'}, 'clob': {'x10', 'f14', 'x27'}})
    
    li x27, 0x1ffff8
    and x10, x10, x27
    li x27, 0x7ffffda3
    add x10, x10, x27
    fld f14, 0x25d(x10)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f14                 0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fld f14, 0x25d(x10)
+========================================================================================================================+
Attributes:  fcsr ['overflow'], special values ['nan', 'zero']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f14                 0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f14, x25, x10
a0(x10)             0x00000000801ff9b3(2149579187)                  0x00000000801ff9b3(2149579187)
s9(x25)             0x000000007ffffc14(2147482644)                  0x000000007ffffc14(2147482644)
f14                 0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008000069c(2147485340)                  0x000000008000069c(2147485340)                  
sp(x2)              0x0000000000000000(0)                           0x0000000000000000(0)                           
gp(x3)              0x0000000000000000(0)                           0x0000000000000000(0)                           
tp(x4)              0x0000000000000400(1024)                        0x0000000000000400(1024)                        
t0(x5)              0x000000008018069f(2149058207)                  0x000000008018069f(2149058207)                  
t1(x6)              0xffffffffffff91f3(18446744073709523443)        0xffffffffffff91f3(18446744073709523443)        
t2(x7)              0x0000000000000000(0)                           0x0000000000000000(0)                           
fp(x8)              0x0000000000000000(0)                           0x0000000000000000(0)                           
s1(x9)              0x0000000000000001(1)                           0x0000000000000001(1)                           
a0(x10)             0x00000000801ff9b3(2149579187)                  0x00000000801ff9b3(2149579187)                  
a1(x11)             0x000000008b433728(2336438056)                  0x000000008b433728(2336438056)                  
a2(x12)             0x0000000080180627(2149058087)                  0x0000000080180627(2149058087)                  
a3(x13)             0x00000000800003e4(2147484644)                  0x00000000800003e4(2147484644)                  
a4(x14)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a5(x15)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a6(x16)             0x000000000000000b(11)                          0x000000000000000b(11)                          
a7(x17)             0x000000008018077a(2149058426)                  0x000000008018077a(2149058426)                  
s2(x18)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s3(x19)             0x000000008017fd0c(2149055756)                  0x000000008017fd0c(2149055756)                  
s4(x20)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s5(x21)             0x0000000080180229(2149057065)                  0x0000000080180229(2149057065)                  
s6(x22)             0x0000000080180627(2149058087)                  0x0000000080180627(2149058087)                  
s7(x23)             0x000000008017fe26(2149056038)                  0x000000008017fe26(2149056038)                  
s8(x24)             0x000000008017fbec(2149055468)                  0x000000008017fbec(2149055468)                  
s9(x25)             0x000000007ffffc14(2147482644)                  0x000000007ffffc14(2147482644)                  
s10(x26)            0x000000008000585f(2147506271)                  0x000000008000585f(2147506271)                  
s11(x27)            0x000000007ffffda3(2147483043)                  0x000000007ffffda3(2147483043)                  
t3(x28)             0xfffffffff2381000(18446744073478344704)        0xfffffffff2381000(18446744073478344704)        
t4(x29)             0x00000000801fff7c(2149580668)                  0x00000000801fff7c(2149580668)                  
t5(x30)             0x00000000000000f8(248)                         0x00000000000000f8(248)                         
t6(x31)             0x000000008017fd88(2149055880)                  0x000000008017fd88(2149055880)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            634575572b0d313e68d11c84f792220ffc6a23e0        634575572b0d313e68d11c84f792220ffc6a23e0        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000744(2147485508)                  0x0000000080000744(2147485508)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000044(68)                          0x0000000000000044(68)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            True                                            True                                            
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rdn(0b010)                                      rdn(0b010)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f1                  0x1593dbb6c785259b(9.896556315150118e-205_d)    0x1593dbb6c785259b(9.896556315150118e-205_d)    
f2                  0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f3                  0xffffffff4f00000a(2147486208.0_s)              0xffffffff4f00000a(2147486208.0_s)              
f4                  0x1185de7eb5879cae(2.954095731229236e-224_d)    0x1185de7eb5879cae(2.954095731229236e-224_d)    
f5                  0xffffffff4f000005(2147484928.0_s)              0xffffffff4f000005(2147484928.0_s)              
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x1593dbb6c785259b(9.896556315150118e-205_d)    0x1593dbb6c785259b(9.896556315150118e-205_d)    
f8                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f9                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f10                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f11                 0x000000008017fc26(1.0617745064e-314_d)         0x000000008017fc26(1.0617745064e-314_d)         
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0xffffffff7fc00000(nan_s)                       0x0000000000000000(0.0_d)                       X
f15                 0xb63c845a02a678bf(-1.9512122135603192e-47_d)   0xb63c845a02a678bf(-1.9512122135603192e-47_d)   
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x41e00000c5200000(2147485225.0_d)              0x41e00000c5200000(2147485225.0_d)              
f19                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f20                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f21                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f22                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f23                 0xfffffffff1c57000(-1.9553262920512581e+30_s)   0xfffffffff1c57000(-1.9553262920512581e+30_s)   
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f26                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0xffffffff4f001912(2149126656.0_s)              0xffffffff4f001912(2149126656.0_s)              
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x41e0040066600000(2149581619.0_d)              0x41e0040066600000(2149581619.0_d)              
STATES DIFFER: True
```

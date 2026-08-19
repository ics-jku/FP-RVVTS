# FailID_002016 VP++ FF neg RV64 fsh

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2016
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
_reg_f0: .byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x02,0x18,0x00,0x4f,0xff,0xff,0xff,0xff
_reg_f6: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f7: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x02,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f15:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f16:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0xff,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x23,0xb4,0x61,0x00,0x23,0xb8,0x71,0x00
_reg_f25:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xdf,0x43
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x80,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f29:.byte 0xac,0xf9,0xff,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0xff,0xff,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'rmm(0b100)', 'res': 0}
    li t0, 0x90
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x0                   // ra
    li x2, 0x8000000000000201    // sp
    li x3, 0x80000343            // gp
    li x4, 0x0                   // tp
    li x5, 0xffffffffffffffff    // t0
    li x6, 0x8017fbad            // t1
    li x7, 0x800061d7            // t2
    li x8, 0x8000054b            // fp
    li x9, 0x200                 // s1
    li x10, 0x7ffffffffffffff    // a0
    li x11, 0x0                  // a1
    li x12, 0x80000548           // a2
    li x13, 0x6000               // a3
    li x14, 0x80                 // a4
    li x15, 0xc3                 // a5
    li x16, 0xffffffffb2cdd000   // a6
    li x17, 0x200                // a7
    li x18, 0x8017feee           // s2
    li x19, 0x8017f843           // s3
    li x20, 0x0                  // s4
    li x21, 0xffffffffffffffff   // s5
    li x22, 0x8000020b           // s6
    li x23, 0x6000               // s7
    li x24, 0x8000072d           // s8
    li x25, 0x0                  // s9
    li x26, 0x8000072d           // s10
    li x27, 0x7ffff9ac           // s11
    li x28, 0x801ff423           // t3
    li x29, 0xffffffffffffffff   // t4
    li x30, 0x1                  // t5
    li x31, 0xac4c6714           // t6
    // INSTRUCTION ({'dep': {'fcsr.rm', 'x24', 'mstatus.fs/vs.fs', 'f5'}, 'clob': {'x24', 'x7'}})
    
    li x7, 0xffffe
    and x24, x24, x7
    li x7, 0x8017fdc1
    add x24, x24, x7
    fsh f5, 0x23f(x24)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        cf98cf9219093f35c41ae8edaeeb826b1b9ca22a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsh f5, 0x23f(x24)
+========================================================================================================================+
Attributes:  fcsr ['invalid']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        cf98cf9219093f35c41ae8edaeeb826b1b9ca22a        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f5, x23, x24
s7(x23)             0x0000000000006000(24576)                       0x0000000000006000(24576)
s8(x24)             0x00000000801804ed(2149057773)                  0x00000000801804ed(2149057773)
f5                  0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000000(0)                           0x0000000000000000(0)                           
sp(x2)              0x8000000000000201(9223372036854776321)         0x8000000000000201(9223372036854776321)         
gp(x3)              0x0000000080000343(2147484483)                  0x0000000080000343(2147484483)                  
tp(x4)              0x0000000000000000(0)                           0x0000000000000000(0)                           
t0(x5)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t1(x6)              0x000000008017fbad(2149055405)                  0x000000008017fbad(2149055405)                  
t2(x7)              0x000000008017fdc1(2149055937)                  0x000000008017fdc1(2149055937)                  
fp(x8)              0x000000008000054b(2147485003)                  0x000000008000054b(2147485003)                  
s1(x9)              0x0000000000000200(512)                         0x0000000000000200(512)                         
a0(x10)             0x07ffffffffffffff(576460752303423487)          0x07ffffffffffffff(576460752303423487)          
a1(x11)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a2(x12)             0x0000000080000548(2147485000)                  0x0000000080000548(2147485000)                  
a3(x13)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
a4(x14)             0x0000000000000080(128)                         0x0000000000000080(128)                         
a5(x15)             0x00000000000000c3(195)                         0x00000000000000c3(195)                         
a6(x16)             0xffffffffb2cdd000(18446744072414416896)        0xffffffffb2cdd000(18446744072414416896)        
a7(x17)             0x0000000000000200(512)                         0x0000000000000200(512)                         
s2(x18)             0x000000008017feee(2149056238)                  0x000000008017feee(2149056238)                  
s3(x19)             0x000000008017f843(2149054531)                  0x000000008017f843(2149054531)                  
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s6(x22)             0x000000008000020b(2147484171)                  0x000000008000020b(2147484171)                  
s7(x23)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s8(x24)             0x00000000801804ed(2149057773)                  0x00000000801804ed(2149057773)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x000000008000072d(2147485485)                  0x000000008000072d(2147485485)                  
s11(x27)            0x000000007ffff9ac(2147482028)                  0x000000007ffff9ac(2147482028)                  
t3(x28)             0x00000000801ff423(2149577763)                  0x00000000801ff423(2149577763)                  
t4(x29)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
t5(x30)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t6(x31)             0x00000000ac4c6714(2890688276)                  0x00000000ac4c6714(2890688276)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            1d56b2fe5c1c90968e1ff0d0f08db78be8495e08        1d56b2fe5c1c90968e1ff0d0f08db78be8495e08        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        cf98cf9219093f35c41ae8edaeeb826b1b9ca22a        X
lastPC              0x0000000080000724(2147485476)                  0x0000000080000724(2147485476)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000090(144)                         0x0000000000000090(144)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            rmm(0b100)                                      rmm(0b100)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f1                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f2                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0xffffffff4f001802(2149057024.0_s)              0xffffffff4f001802(2149057024.0_s)              
f6                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f7                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f8                  0xffffffff00000200(7.174648137343064e-43_s)     0xffffffff00000200(7.174648137343064e-43_s)     
f9                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f12                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f13                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f14                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f15                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f16                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f17                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffffffc00000(nan_s)                       0xffffffffffc00000(nan_s)                       
f20                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x0071b8230061b423(1.577068631947372e-306_d)    0x0071b8230061b423(1.577068631947372e-306_d)    
f25                 0x43dfffffffffffff(9.223372036854775e+18_d)     0x43dfffffffffffff(9.223372036854775e+18_d)     
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0xffffffff00000080(1.793662034335766e-43_s)     0xffffffff00000080(1.793662034335766e-43_s)     
f28                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f29                 0xffffffff7ffff9ac(nan_s)                       0xffffffff7ffff9ac(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffffffffffff(nan_h)                       0xffffffffffffffff(nan_h)                       
STATES DIFFER: True
```

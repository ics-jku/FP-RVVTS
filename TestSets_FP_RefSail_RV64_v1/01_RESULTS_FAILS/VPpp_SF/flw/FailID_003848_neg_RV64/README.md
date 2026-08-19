# FailID_003848 VP++ SF neg RV64 flw

* Reference model (REF): Sail RISC-V
* DUT: VP++ SF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 3848
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
_reg_f1: .byte 0x23,0xbc,0x51,0x00,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x11,0x43,0xff,0xff,0xff,0xff
_reg_f3: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f4: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0x41
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f12:.byte 0x00,0x00,0x04,0x43,0xff,0xff,0xff,0xff
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0xc1
_reg_f15:.byte 0x00,0x00,0x20,0x03,0x00,0x03,0xe0,0xc1
_reg_f16:.byte 0x00,0x00,0x55,0x43,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x3e,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f18:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0x7f
_reg_f19:.byte 0xff,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f20:.byte 0xff,0xff,0xff,0x4e,0xff,0xff,0xff,0xff
_reg_f21:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f23:.byte 0x00,0x60,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f24:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f27:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': False, 'uf': True, 'of': False, 'dz': False, 'nv': False, 'rm': 'rtz(0b001)', 'res': 0}
    li t0, 0x22
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x800000dd            // ra
    li x2, 0x7ffffac1            // sp
    li x3, 0x0                   // gp
    li x4, 0x7ffffabd            // tp
    li x5, 0x400bfe148000        // t0
    li x6, 0x60018c00000000      // t1
    li x7, 0x80180063            // t2
    li x8, 0x8017fe7c            // fp
    li x9, 0x22                  // s1
    li x10, 0x7fffffffffffffff   // a0
    li x11, 0x7ffff88e           // a1
    li x12, 0x8000001e           // a2
    li x13, 0x8000062a           // a3
    li x14, 0x7fffff1b           // a4
    li x15, 0x0                  // a5
    li x16, 0x8018041a           // a6
    li x17, 0x8017fa63           // a7
    li x18, 0x75                 // s2
    li x19, 0x8017fa83           // s3
    li x20, 0x1                  // s4
    li x21, 0x3e                 // s5
    li x22, 0x7ffffe87           // s6
    li x23, 0x800000dd           // s7
    li x24, 0x6000               // s8
    li x25, 0x1                  // s9
    li x26, 0x8018009f           // s10
    li x27, 0x7ffffd7e           // s11
    li x28, 0x1                  // t3
    li x29, 0x8019928f           // t4
    li x30, 0x6000               // t5
    li x31, 0x84                 // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'x3'}, 'clob': {'x16', 'x3', 'f1'}})
    
    li x16, 0x1ffffc
    and x3, x3, x16
    li x16, 0x8000067f
    add x3, x3, x16
    flw f1, -0x67f(x3)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f1                  0xffffffff0051bc23(7.506165926734564e-39_s)     0xffffffff2140006f(6.505270420568022e-19_s)     X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: flw f1, -0x67f(x3)
+========================================================================================================================+
Attributes:  fcsr ['underflow']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
f1                  0xffffffff0051bc23(7.506165926734564e-39_s)     0xffffffff2140006f(6.505270420568022e-19_s)     X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f1, x67, x3
gp(x3)              0x000000008000067f(2147485311)                  0x000000008000067f(2147485311)
f1                  0xffffffff0051bc23(7.506165926734564e-39_s)     0xffffffff2140006f(6.505270420568022e-19_s)     X
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x00000000800000dd(2147483869)                  0x00000000800000dd(2147483869)                  
sp(x2)              0x000000007ffffac1(2147482305)                  0x000000007ffffac1(2147482305)                  
gp(x3)              0x000000008000067f(2147485311)                  0x000000008000067f(2147485311)                  
tp(x4)              0x000000007ffffabd(2147482301)                  0x000000007ffffabd(2147482301)                  
t0(x5)              0x0000400bfe148000(70420251574272)              0x0000400bfe148000(70420251574272)              
t1(x6)              0x0060018c00000000(27023298571272192)           0x0060018c00000000(27023298571272192)           
t2(x7)              0x0000000080180063(2149056611)                  0x0000000080180063(2149056611)                  
fp(x8)              0x000000008017fe7c(2149056124)                  0x000000008017fe7c(2149056124)                  
s1(x9)              0x0000000000000022(34)                          0x0000000000000022(34)                          
a0(x10)             0x7fffffffffffffff(9223372036854775807)         0x7fffffffffffffff(9223372036854775807)         
a1(x11)             0x000000007ffff88e(2147481742)                  0x000000007ffff88e(2147481742)                  
a2(x12)             0x000000008000001e(2147483678)                  0x000000008000001e(2147483678)                  
a3(x13)             0x000000008000062a(2147485226)                  0x000000008000062a(2147485226)                  
a4(x14)             0x000000007fffff1b(2147483419)                  0x000000007fffff1b(2147483419)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x000000008000067f(2147485311)                  0x000000008000067f(2147485311)                  
a7(x17)             0x000000008017fa63(2149055075)                  0x000000008017fa63(2149055075)                  
s2(x18)             0x0000000000000075(117)                         0x0000000000000075(117)                         
s3(x19)             0x000000008017fa83(2149055107)                  0x000000008017fa83(2149055107)                  
s4(x20)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s5(x21)             0x000000000000003e(62)                          0x000000000000003e(62)                          
s6(x22)             0x000000007ffffe87(2147483271)                  0x000000007ffffe87(2147483271)                  
s7(x23)             0x00000000800000dd(2147483869)                  0x00000000800000dd(2147483869)                  
s8(x24)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s9(x25)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s10(x26)            0x000000008018009f(2149056671)                  0x000000008018009f(2149056671)                  
s11(x27)            0x000000007ffffd7e(2147483006)                  0x000000007ffffd7e(2147483006)                  
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x000000008019928f(2149159567)                  0x000000008019928f(2149159567)                  
t5(x30)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t6(x31)             0x0000000000000084(132)                         0x0000000000000084(132)                         

STATE               REF                                             DUT                                             DIFF
xmemhash            0f688b18badbaa61c6a26ff2599b32cef3112911        0f688b18badbaa61c6a26ff2599b32cef3112911        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000740(2147485504)                  0x0000000080000740(2147485504)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x0000000000000022(34)                          0x0000000000000022(34)                          
 fcsr.nx            False                                           False                                           
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            False                                           False                                           
 fcsr.rm            rtz(0b001)                                      rtz(0b001)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f1                  0xffffffff0051bc23(7.506165926734564e-39_s)     0xffffffff2140006f(6.505270420568022e-19_s)     X
f2                  0xffffffff43110000(145.0_s)                     0xffffffff43110000(145.0_s)                     
f3                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f4                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f8                  0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f9                  0x41e0030003200000(2149056537.0_d)              0x41e0030003200000(2149056537.0_d)              
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f12                 0xffffffff43040000(132.0_s)                     0xffffffff43040000(132.0_s)                     
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xc1e0030003200000(-2149056537.0_d)             0xc1e0030003200000(-2149056537.0_d)             
f15                 0xc1e0030003200000(-2149056537.0_d)             0xc1e0030003200000(-2149056537.0_d)             
f16                 0xffffffff43550000(213.0_s)                     0xffffffff43550000(213.0_s)                     
f17                 0x000000000000003e(3.06e-322_d)                 0x000000000000003e(3.06e-322_d)                 
f18                 0x7fffffff00000000(nan_d)                       0x7fffffff00000000(nan_d)                       
f19                 0xffffffff4effffff(2147483520.0_s)              0xffffffff4effffff(2147483520.0_s)              
f20                 0xffffffff4effffff(2147483520.0_s)              0xffffffff4effffff(2147483520.0_s)              
f21                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f22                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f23                 0x0000000000006000(1.2142e-319_d)               0x0000000000006000(1.2142e-319_d)               
f24                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f25                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f26                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f27                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
STATES DIFFER: True
```

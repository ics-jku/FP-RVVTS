# FailID_000086 ARA neg RV64 fsqrt.s

* Reference model (REF): Sail RISC-V
* DUT: ARA
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 86
* Isolated failing instruction: `fsqrt.s`
* Minimized failing test case: [cblock_minimized_test_case.json](cblock_minimized_test_case.json)
* Resulting REF machine state: [mstate_RefSail.json](mstate_RefSail.json)
* Resulting DUT machine state: [mstate_DUT_ARA.json](mstate_DUT_ARA.json)
* Automated failure characterization report: [AFC_FP_report.log](AFC_FP_report.log)

## Report

### Minimized Failing Test Case
```
    // FLOATINGPOINT STATE DATA
    j _float_data_end
    .align 4
_reg_f0: .byte 0x01,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f1: .byte 0x4f,0x3d,0x2e,0xd9,0x1b,0xd4,0x66,0x93
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f3: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x81,0x02,0x18,0x80,0xff,0xff,0xff,0xff
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f6: .byte 0x03,0xb4,0x94,0x38,0x63,0x35,0xb7,0x8d
_reg_f7: .byte 0x93,0x0c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f8: .byte 0x59,0x52,0x66,0xea,0x97,0xaa,0x8a,0x3b
_reg_f9: .byte 0x00,0x60,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f10:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f11:.byte 0xf1,0x46,0xb2,0x9e,0xf5,0x51,0xcc,0x69
_reg_f12:.byte 0xeb,0x91,0x9d,0x69,0x42,0xa5,0x64,0x47
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f15:.byte 0x00,0x00,0x40,0xb8,0xda,0x90,0xd6,0xc1
_reg_f16:.byte 0x93,0x0c,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0xd0,0x42,0xff,0xff,0xff,0x7f
_reg_f19:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f20:.byte 0xbb,0x8c,0xf6,0x70,0x93,0xca,0x45,0x90
_reg_f21:.byte 0xbb,0x8c,0xf6,0x70,0x93,0xca,0x45,0x90
_reg_f22:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f23:.byte 0x00,0x00,0xd0,0x42,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f25:.byte 0x80,0x56,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f26:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f27:.byte 0x9d,0xa5,0x63,0xd5,0x67,0xe5,0xf2,0x7b
_reg_f28:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f29:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f30:.byte 0x85,0x5f,0x1c,0xbc,0xed,0x2f,0x76,0x0c
_reg_f31:.byte 0x33,0x5a,0xff,0xff,0xff,0xff,0xff,0xff
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

    // restore fcsr = {'nx': True, 'uf': True, 'of': False, 'dz': True, 'nv': True, 'rm': 'rup(0b011)', 'res': 0}
    li t0, 0x7b
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'dirty', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x6000
    csrs mstatus, t0

    // restore registers
    li x1, 0x736                 // ra
    li x2, 0xffffffffffffffff    // sp
    li x3, 0x802002ec            // gp
    li x4, 0xffffffff86443000    // tp
    li x5, 0xf9c028a38d54b659    // t0
    li x6, 0x801989b6            // t1
    li x7, 0x80000398            // t2
    li x8, 0x80180544            // fp
    li x9, 0x800002d3            // s1
    li x10, 0x0                  // a0
    li x11, 0x5ce23000           // a1
    li x12, 0x8027fd05           // a2
    li x13, 0x751767b4           // a3
    li x14, 0x80180281           // a4
    li x15, 0x0                  // a5
    li x16, 0xffffffffffffffff   // a6
    li x17, 0xffffffffe3f62000   // a7
    li x18, 0x801803fc           // s2
    li x19, 0x7ffff9e6           // s3
    li x20, 0x800003f7           // s4
    li x21, 0xfffffffffffffe94   // s5
    li x22, 0x800002b7           // s6
    li x23, 0x6000               // s7
    li x24, 0x7ffff9b6           // s8
    li x25, 0x0                  // s9
    li x26, 0x6000               // s10
    li x27, 0x200                // s11
    li x28, 0x1                  // t3
    li x29, 0x6000               // t4
    li x30, 0x0                  // t5
    li x31, 0x80180362           // t6
    // INSTRUCTION ({'dep': {'mstatus.fs/vs.fs', 'fcsr.rm', 'f23'}, 'clob': {'f16'}})
    fsqrt.s f16, f23, dyn
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
f16                 0xffffffff41232b2b(10.198039054870605_s)        0xffffffff41232b2a(10.198038101196289_s)        X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsqrt.s f16, f23, dyn
+========================================================================================================================+
Attributes:  fcsr ['invalid', 'underflow', 'div-by-0', 'inexact']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
f16                 0xffffffff41232b2b(10.198039054870605_s)        0xffffffff41232b2a(10.198038101196289_s)        X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f16, f23
f16                 0xffffffff41232b2b(10.198039054870605_s)        0xffffffff41232b2a(10.198038101196289_s)        X
f23                 0xffffffff42d00000(104.0_s)                     0xffffffff42d00000(104.0_s)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x0000000000000736(1846)                        0x0000000000000736(1846)                        
sp(x2)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
gp(x3)              0x00000000802002ec(2149581548)                  0x00000000802002ec(2149581548)                  
tp(x4)              0xffffffff86443000(18446744071667200000)        0xffffffff86443000(18446744071667200000)        
t0(x5)              0xf9c028a38d54b659(17996428793888421465)        0xf9c028a38d54b659(17996428793888421465)        
t1(x6)              0x00000000801989b6(2149157302)                  0x00000000801989b6(2149157302)                  
t2(x7)              0x0000000080000398(2147484568)                  0x0000000080000398(2147484568)                  
fp(x8)              0x0000000080180544(2149057860)                  0x0000000080180544(2149057860)                  
s1(x9)              0x00000000800002d3(2147484371)                  0x00000000800002d3(2147484371)                  
a0(x10)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a1(x11)             0x000000005ce23000(1558327296)                  0x000000005ce23000(1558327296)                  
a2(x12)             0x000000008027fd05(2150104325)                  0x000000008027fd05(2150104325)                  
a3(x13)             0x00000000751767b4(1964468148)                  0x00000000751767b4(1964468148)                  
a4(x14)             0x0000000080180281(2149057153)                  0x0000000080180281(2149057153)                  
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
a7(x17)             0xffffffffe3f62000(18446744073239142400)        0xffffffffe3f62000(18446744073239142400)        
s2(x18)             0x00000000801803fc(2149057532)                  0x00000000801803fc(2149057532)                  
s3(x19)             0x000000007ffff9e6(2147482086)                  0x000000007ffff9e6(2147482086)                  
s4(x20)             0x00000000800003f7(2147484663)                  0x00000000800003f7(2147484663)                  
s5(x21)             0xfffffffffffffe94(18446744073709551252)        0xfffffffffffffe94(18446744073709551252)        
s6(x22)             0x00000000800002b7(2147484343)                  0x00000000800002b7(2147484343)                  
s7(x23)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s8(x24)             0x000000007ffff9b6(2147482038)                  0x000000007ffff9b6(2147482038)                  
s9(x25)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s10(x26)            0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s11(x27)            0x0000000000000200(512)                         0x0000000000000200(512)                         
t3(x28)             0x0000000000000001(1)                           0x0000000000000001(1)                           
t4(x29)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
t5(x30)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t6(x31)             0x0000000080180362(2149057378)                  0x0000000080180362(2149057378)                  

STATE               REF                                             DUT                                             DIFF
xmemhash            5e56784a15275b0ac34076f79052d993ae1fff52        5e56784a15275b0ac34076f79052d993ae1fff52        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        95823c334fce55968e8d2827ccd1cf77cee19abd        
lastPC              0x0000000080000710(2147485456)                  0x0000000080000710(2147485456)                  
#exceptions         0x0000000000000000(0)                           0x0000000000000000(0)                           
mstatus.fs/vs       0x0000000000006000(24576)                       0x0000000000006000(24576)                       
 mstatus.fs/vs.fs   dirty                                           dirty                                           
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x000000000000007b(123)                         0x000000000000007b(123)                         
 fcsr.nx            True                                            True                                            
 fcsr.uf            True                                            True                                            
 fcsr.of            False                                           False                                           
 fcsr.dz            True                                            True                                            
 fcsr.nv            True                                            True                                            
 fcsr.rm            rup(0b011)                                      rup(0b011)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0xffffffff00000001(1.401298464324817e-45_s)     0xffffffff00000001(1.401298464324817e-45_s)     
f1                  0x9366d41bd92e3d4f(-3.3110934255220594e-215_d)  0x9366d41bd92e3d4f(-3.3110934255220594e-215_d)  
f2                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f3                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f4                  0xffffffff80180281(-2.2049501401074213e-39_s)   0xffffffff80180281(-2.2049501401074213e-39_s)   
f5                  0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f6                  0x8db735633894b403(-1.3596008341984277e-242_d)  0x8db735633894b403(-1.3596008341984277e-242_d)  
f7                  0xffffffffffff0c93(0.0002791881561279297_h)     0xffffffffffff0c93(0.0002791881561279297_h)     
f8                  0x3b8aaa97ea665259(7.058532158926849e-22_d)     0x3b8aaa97ea665259(7.058532158926849e-22_d)     
f9                  0xffffffff00006000(3.4438311059246704e-41_s)    0xffffffff00006000(3.4438311059246704e-41_s)    
f10                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f11                 0x69cc51f59eb246f1(4.335535323009277e+201_d)    0x69cc51f59eb246f1(4.335535323009277e+201_d)    
f12                 0x4764a542699d91eb(8.575823720035319e+35_d)     0x4764a542699d91eb(8.575823720035319e+35_d)     
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f15                 0xc1d690dab8400000(-1514367713.0_d)             0xc1d690dab8400000(-1514367713.0_d)             
f16                 0xffffffff41232b2b(10.198039054870605_s)        0xffffffff41232b2a(10.198038101196289_s)        X
f17                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f18                 0x7fffffff42d00000(nan_d)                       0x7fffffff42d00000(nan_d)                       
f19                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f20                 0x9045ca9370f68cbb(-2.807221684975501e-230_d)   0x9045ca9370f68cbb(-2.807221684975501e-230_d)   
f21                 0x9045ca9370f68cbb(-2.807221684975501e-230_d)   0x9045ca9370f68cbb(-2.807221684975501e-230_d)   
f22                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f23                 0xffffffff42d00000(104.0_s)                     0xffffffff42d00000(104.0_s)                     
f24                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f25                 0xffffffffffff5680(104.0_h)                     0xffffffffffff5680(104.0_h)                     
f26                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f27                 0x7bf2e567d563a59d(1.1509286272135676e+289_d)   0x7bf2e567d563a59d(1.1509286272135676e+289_d)   
f28                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f29                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f30                 0x0c762fedbc1c5f85(1.2395570086590742e-248_d)   0x0c762fedbc1c5f85(1.2395570086590742e-248_d)   
f31                 0xffffffffffff5a33(198.375_h)                   0xffffffffffff5a33(198.375_h)                   
STATES DIFFER: True
```

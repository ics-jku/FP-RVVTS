# FailID_002307 VP++ FF neg RV64 fsw

* Reference model (REF): Sail RISC-V
* DUT: VP++ FF
* Source test set: neg/RV64
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* FailID: 2307
* Isolated failing instruction: `fsw`
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
_reg_f0: .byte 0x00,0x00,0x20,0xa2,0x00,0x03,0xe0,0x41
_reg_f1: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f2: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f3: .byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f4: .byte 0x00,0x00,0x00,0x00,0x00,0x80,0x64,0x40
_reg_f5: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f6: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f7: .byte 0x00,0x00,0x00,0x96,0xfe,0xff,0xdf,0x41
_reg_f8: .byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f9: .byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
_reg_f10:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f11:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0x00,0x00
_reg_f12:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f13:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f14:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f15:.byte 0x00,0x00,0x20,0xa2,0x00,0x03,0xe0,0x41
_reg_f16:.byte 0x00,0x00,0xc0,0x46,0xff,0xff,0xff,0xff
_reg_f17:.byte 0x00,0x00,0x00,0x00,0xff,0xff,0xff,0xff
_reg_f18:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f19:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f20:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f21:.byte 0x00,0x7e,0xff,0xff,0xff,0xff,0xff,0xff
_reg_f22:.byte 0x00,0x00,0x80,0xc8,0xff,0xff,0xdf,0x41
_reg_f23:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f24:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f25:.byte 0x00,0x00,0x20,0xa2,0x00,0x03,0xe0,0x41
_reg_f26:.byte 0x6f,0x00,0x40,0x21,0x13,0x00,0x00,0x00
_reg_f27:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f28:.byte 0x00,0x00,0x00,0x00,0xe8,0xfc,0x1b,0x42
_reg_f29:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf8,0x7f
_reg_f30:.byte 0x00,0x00,0xc0,0x7f,0xff,0xff,0xff,0xff
_reg_f31:.byte 0x00,0x00,0x00,0x00,0x00,0x00,0xf0,0x3f
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

    // restore fcsr = {'nx': False, 'uf': False, 'of': False, 'dz': False, 'nv': True, 'rm': 'dyn(0b111)', 'res': 0}
    li t0, 0xf0
    csrrw zero, fcsr, t0

    // STATE

    // restore mstatus.fs/vs = {'fs': 'off', 'vs': 'off'}
    li t0, 0x6600
    csrc mstatus, t0
    li t0, 0x0
    csrs mstatus, t0

    // restore registers
    li x1, 0x8000006f            // ra
    li x2, 0x58e6                // sp
    li x3, 0x800001c3            // gp
    li x4, 0x8018017a            // tp
    li x5, 0x903f000             // t0
    li x6, 0x800006b5            // t1
    li x7, 0x8017fc93            // t2
    li x8, 0xffffffffffffffff    // fp
    li x9, 0xffffffffc9724000    // s1
    li x10, 0x7fffff22           // a0
    li x11, 0x8019c06f           // a1
    li x12, 0x0                  // a2
    li x13, 0xffffffff9bd71000   // a3
    li x14, 0x0                  // a4
    li x15, 0x0                  // a5
    li x16, 0x1                  // a6
    li x17, 0x6000               // a7
    li x18, 0x8017fc9300         // s2
    li x19, 0xfffffffffffffff3   // s3
    li x20, 0x0                  // s4
    li x21, 0x8018014b           // s5
    li x22, 0x0                  // s6
    li x23, 0x1                  // s7
    li x24, 0x0                  // s8
    li x25, 0x7ffffa84           // s9
    li x26, 0x8028007d           // s10
    li x27, 0x80180411           // s11
    li x28, 0x0                  // t3
    li x29, 0x80180b6            // t4
    li x30, 0x80180b6f           // t5
    li x31, 0x0                  // t6
    // INSTRUCTION ({'dep': {'f0', 'mstatus.fs/vs.fs', 'fcsr.rm', 'x4'}, 'clob': {'x10', 'x4'}})
    
    li x10, 0xffffc
    and x4, x4, x10
    li x10, 0x8018004b
    add x4, x4, x10
    fsw f0, -0x4b(x4)
```

### Resulting Machine State Diff
```
REG                 REF                                             DUT                                             DIFF

STATE               REF                                             DUT                                             DIFF
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        6bbd4d32b5737dd6cd9e07f4c9aba2adb7e0ce77        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
STATES DIFFER: True
```

### Automated Failure Characterization Report
```
+========================================================================================================================+
Instruction: fsw f0, -0x4b(x4)
+========================================================================================================================+
Attributes:  fcsr ['invalid']
+------------------------------------------------------------------------------------------------------------------------+
REG                 REF                                             DUT                                             DIFF 
+------------------------------------------------------------------------------------------------------------------------+
diffs:
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        6bbd4d32b5737dd6cd9e07f4c9aba2adb7e0ce77        X
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
+------------------------------------------------------------------------------------------------------------------------+
Registers: f0, x4, x4
tp(x4)              0x00000000802001c3(2149581251)                  0x00000000802001c3(2149581251)
f0                  0x41e00300a2200000(2149057809.0_d)              0x41e00300a2200000(2149057809.0_d)
+========================================================================================================================+
```

### Resulting Full Machine State Diff
```
REG                 REF                                             DUT                                             DIFF
zero(x0)            0x0000000000000000(0)                           0x0000000000000000(0)                           
ra(x1)              0x000000008000006f(2147483759)                  0x000000008000006f(2147483759)                  
sp(x2)              0x00000000000058e6(22758)                       0x00000000000058e6(22758)                       
gp(x3)              0x00000000800001c3(2147484099)                  0x00000000800001c3(2147484099)                  
tp(x4)              0x00000000802001c3(2149581251)                  0x00000000802001c3(2149581251)                  
t0(x5)              0x000000000903f000(151252992)                   0x000000000903f000(151252992)                   
t1(x6)              0x00000000800006b5(2147485365)                  0x00000000800006b5(2147485365)                  
t2(x7)              0x000000008017fc93(2149055635)                  0x000000008017fc93(2149055635)                  
fp(x8)              0xffffffffffffffff(18446744073709551615)        0xffffffffffffffff(18446744073709551615)        
s1(x9)              0xffffffffc9724000(18446744072794292224)        0xffffffffc9724000(18446744072794292224)        
a0(x10)             0x000000008018004b(2149056587)                  0x000000008018004b(2149056587)                  
a1(x11)             0x000000008019c06f(2149171311)                  0x000000008019c06f(2149171311)                  
a2(x12)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a3(x13)             0xffffffff9bd71000(18446744072029147136)        0xffffffff9bd71000(18446744072029147136)        
a4(x14)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a5(x15)             0x0000000000000000(0)                           0x0000000000000000(0)                           
a6(x16)             0x0000000000000001(1)                           0x0000000000000001(1)                           
a7(x17)             0x0000000000006000(24576)                       0x0000000000006000(24576)                       
s2(x18)             0x0000008017fc9300(550158242560)                0x0000008017fc9300(550158242560)                
s3(x19)             0xfffffffffffffff3(18446744073709551603)        0xfffffffffffffff3(18446744073709551603)        
s4(x20)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s5(x21)             0x000000008018014b(2149056843)                  0x000000008018014b(2149056843)                  
s6(x22)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s7(x23)             0x0000000000000001(1)                           0x0000000000000001(1)                           
s8(x24)             0x0000000000000000(0)                           0x0000000000000000(0)                           
s9(x25)             0x000000007ffffa84(2147482244)                  0x000000007ffffa84(2147482244)                  
s10(x26)            0x000000008028007d(2150105213)                  0x000000008028007d(2150105213)                  
s11(x27)            0x0000000080180411(2149057553)                  0x0000000080180411(2149057553)                  
t3(x28)             0x0000000000000000(0)                           0x0000000000000000(0)                           
t4(x29)             0x00000000080180b6(134316214)                   0x00000000080180b6(134316214)                   
t5(x30)             0x0000000080180b6f(2149059439)                  0x0000000080180b6f(2149059439)                  
t6(x31)             0x0000000000000000(0)                           0x0000000000000000(0)                           

STATE               REF                                             DUT                                             DIFF
xmemhash            02b3175713750f3bbecdac16ee279376dbd1a3f6        02b3175713750f3bbecdac16ee279376dbd1a3f6        
dmemhash            95823c334fce55968e8d2827ccd1cf77cee19abd        6bbd4d32b5737dd6cd9e07f4c9aba2adb7e0ce77        X
lastPC              0x0000000080000720(2147485472)                  0x0000000080000720(2147485472)                  
#exceptions         0x0000000000000001(1)                           0x0000000000000000(0)                           X
mstatus.fs/vs       0x0000000000000000(0)                           0x0000000000000000(0)                           
 mstatus.fs/vs.fs   off                                             off                                             
 mstatus.fs/vs.vs   off                                             off                                             
fcsr                0x00000000000000f0(240)                         0x00000000000000f0(240)                         
 fcsr.nx            False                                           False                                           
 fcsr.uf            False                                           False                                           
 fcsr.of            False                                           False                                           
 fcsr.dz            False                                           False                                           
 fcsr.nv            True                                            True                                            
 fcsr.rm            dyn(0b111)                                      dyn(0b111)                                      
 fcsr.res           0x0000000000000000(0)                           0x0000000000000000(0)                           
f0                  0x41e00300a2200000(2149057809.0_d)              0x41e00300a2200000(2149057809.0_d)              
f1                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f2                  0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f3                  0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f4                  0x4064800000000000(164.0_d)                     0x4064800000000000(164.0_d)                     
f5                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f6                  0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f7                  0x41dffffe96000000(2147482200.0_d)              0x41dffffe96000000(2147482200.0_d)              
f8                  0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f9                  0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
f10                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f11                 0x0000000000000000(0.0_d)                       0x0000000000000000(0.0_d)                       
f12                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f13                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f14                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f15                 0x41e00300a2200000(2149057809.0_d)              0x41e00300a2200000(2149057809.0_d)              
f16                 0xffffffff46c00000(24576.0_s)                   0xffffffff46c00000(24576.0_s)                   
f17                 0xffffffff00000000(0.0_s)                       0xffffffff00000000(0.0_s)                       
f18                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f19                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f20                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f21                 0xffffffffffff7e00(nan_h)                       0xffffffffffff7e00(nan_h)                       
f22                 0x41dfffffc8800000(2147483426.0_d)              0x41dfffffc8800000(2147483426.0_d)              
f23                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f24                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f25                 0x41e00300a2200000(2149057809.0_d)              0x41e00300a2200000(2149057809.0_d)              
f26                 0x000000132140006f(4.05935308646e-313_d)        0x000000132140006f(4.05935308646e-313_d)        
f27                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f28                 0x421bfce800000000(30051794944.0_d)             0x421bfce800000000(30051794944.0_d)             
f29                 0x7ff8000000000000(nan_d)                       0x7ff8000000000000(nan_d)                       
f30                 0xffffffff7fc00000(nan_s)                       0xffffffff7fc00000(nan_s)                       
f31                 0x3ff0000000000000(1.0_d)                       0x3ff0000000000000(1.0_d)                       
STATES DIFFER: True
```

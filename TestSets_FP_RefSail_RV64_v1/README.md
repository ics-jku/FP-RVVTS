# FP-RVVTS Test Sets and Results: Sail RISC-V Reference, RV64

This report summarizes the pre-generated FP-RVVTS RV64 test sets and the archived result reports for Sail-guided verification of RISC-V floating-point implementations. It accompanies the paper [FP-RVVTS: Sail-guided Verification of RISC-V Floating-Point Implementations](https://ics.jku.at/files/2026FDL_FP-RVVTS.pdf).

## Test Setup

* Reference model (REF): Sail RISC-V.
* Test framework: FP-RVVTS, integrated into RVVTS.
* Target: RV64 with the RISC-V F, D, and Zfh floating-point extensions.
* Test sets: [00_GENERATED_TESTSETS](00_GENERATED_TESTSETS).
* Result reports: [01_RESULTS_FAILS](01_RESULTS_FAILS).
* `pos` contains valid non-trapping sequences for positive testing.
* `neg` contains invalid/trap-triggering sequences for negative testing.

## DUTs

| DUT | Description |
| --- | --- |
| Spike SF | Spike with the SoftFloat-based floating-point implementation. |
| Spike FF | Spike with the FloppyFloat-based floating-point implementation. |
| VP++ SF | RISC-V VP++ with the SoftFloat-based floating-point implementation. |
| VP++ FF | RISC-V VP++ with the FloppyFloat-based floating-point implementation. |
| QEMU | QEMU RISC-V system emulator. |
| ARA | PULP Ara RISC-V vector processor using its scalar floating-point unit. |

## Test Sets Pre-Generated with FP-RVVTS

| Test set | Test cases | FP instructions | Functional coverage (F, D) |
| --- | ---: | ---: | ---: |
| [Negative Testing (`neg`) RV64](00_GENERATED_TESTSETS/RV64/neg) | 5,108 | 40,575 | 99.94% |
| [Positive Testing (`pos`) RV64](00_GENERATED_TESTSETS/RV64/pos) | 5,271 | 39,934 | 98.87% |

## Result Summary

The following table follows the structure of Table I in the [FP-RVVTS paper](https://ics.jku.at/files/2026FDL_FP-RVVTS.pdf). Counts are calculated from the archived result directories. `unknown` failures are ignored (1 ignored).

* Total reported failures: 5,547.
* neg failures: 3,996.
* pos failures: 1,551.

| Instruction | Spike SF pos | Spike SF neg | Spike FF pos | Spike FF neg | VP++ SF pos | VP++ SF neg | VP++ FF pos | VP++ FF neg | QEMU pos | QEMU neg | ARA pos | ARA neg |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| **Total** | **-** | **-** | **[2](01_RESULTS_FAILS/Spike_FF)** | **[1](01_RESULTS_FAILS/Spike_FF)** | **[418](01_RESULTS_FAILS/VPpp_SF)** | **[1,920](01_RESULTS_FAILS/VPpp_SF)** | **[692](01_RESULTS_FAILS/VPpp_FF)** | **[1,948](01_RESULTS_FAILS/VPpp_FF)** | **-** | **-** | **[439](01_RESULTS_FAILS/ARA)** | **[127](01_RESULTS_FAILS/ARA)** |
| `fcvt.wu.d` | - | - | - | - | - | - | [368](01_RESULTS_FAILS/VPpp_FF/fcvt.wu.d) | [69](01_RESULTS_FAILS/VPpp_FF/fcvt.wu.d) | - | - | - | - |
| `fcvt.wu.s` | - | - | - | - | - | - | [324](01_RESULTS_FAILS/VPpp_FF/fcvt.wu.s) | [84](01_RESULTS_FAILS/VPpp_FF/fcvt.wu.s) | - | - | - | - |
| `fdiv.d` | - | - | - | [1](01_RESULTS_FAILS/Spike_FF/fdiv.d) | - | - | - | - | - | - | [5](01_RESULTS_FAILS/ARA/fdiv.d) | [4](01_RESULTS_FAILS/ARA/fdiv.d) |
| `fdiv.h` | - | - | - | - | - | - | - | - | - | - | - | [3](01_RESULTS_FAILS/ARA/fdiv.h) |
| `fdiv.s` | - | - | - | - | - | - | - | - | - | - | [142](01_RESULTS_FAILS/ARA/fdiv.s) | [36](01_RESULTS_FAILS/ARA/fdiv.s) |
| `fld` | - | - | - | - | - | [344](01_RESULTS_FAILS/VPpp_SF/fld) | - | [343](01_RESULTS_FAILS/VPpp_FF/fld) | - | - | - | - |
| `flh` | - | - | - | - | - | [125](01_RESULTS_FAILS/VPpp_SF/flh) | - | [125](01_RESULTS_FAILS/VPpp_FF/flh) | - | - | - | - |
| `flw` | - | - | - | - | - | [418](01_RESULTS_FAILS/VPpp_SF/flw) | - | [418](01_RESULTS_FAILS/VPpp_FF/flw) | - | - | - | - |
| `fmax.d` | - | - | - | - | [95](01_RESULTS_FAILS/VPpp_SF/fmax.d) | [27](01_RESULTS_FAILS/VPpp_SF/fmax.d) | - | - | - | - | - | - |
| `fmax.s` | - | - | - | - | [108](01_RESULTS_FAILS/VPpp_SF/fmax.s) | [20](01_RESULTS_FAILS/VPpp_SF/fmax.s) | - | - | - | - | - | - |
| `fmin.d` | - | - | - | - | [107](01_RESULTS_FAILS/VPpp_SF/fmin.d) | [19](01_RESULTS_FAILS/VPpp_SF/fmin.d) | - | - | - | - | - | - |
| `fmin.s` | - | - | - | - | [108](01_RESULTS_FAILS/VPpp_SF/fmin.s) | [15](01_RESULTS_FAILS/VPpp_SF/fmin.s) | - | - | - | - | - | - |
| `fmul.d` | - | - | [1](01_RESULTS_FAILS/Spike_FF/fmul.d) | - | - | - | - | - | - | - | - | - |
| `fmv.x.h` | - | - | - | - | - | [23](01_RESULTS_FAILS/VPpp_SF/fmv.x.h) | - | [22](01_RESULTS_FAILS/VPpp_FF/fmv.x.h) | - | - | - | - |
| `fnmsub.d` | - | - | [1](01_RESULTS_FAILS/Spike_FF/fnmsub.d) | - | - | - | - | - | - | - | - | - |
| `fsd` | - | - | - | - | - | [352](01_RESULTS_FAILS/VPpp_SF/fsd) | - | [352](01_RESULTS_FAILS/VPpp_FF/fsd) | - | - | - | - |
| `fsh` | - | - | - | - | - | [179](01_RESULTS_FAILS/VPpp_SF/fsh) | - | [138](01_RESULTS_FAILS/VPpp_FF/fsh) | - | - | - | - |
| `fsw` | - | - | - | - | - | [398](01_RESULTS_FAILS/VPpp_SF/fsw) | - | [397](01_RESULTS_FAILS/VPpp_FF/fsw) | - | - | - | - |
| `fsqrt.d` | - | - | - | - | - | - | - | - | - | - | [23](01_RESULTS_FAILS/ARA/fsqrt.d) | [5](01_RESULTS_FAILS/ARA/fsqrt.d) |
| `fsqrt.h` | - | - | - | - | - | - | - | - | - | - | - | [16](01_RESULTS_FAILS/ARA/fsqrt.h) |
| `fsqrt.s` | - | - | - | - | - | - | - | - | - | - | [269](01_RESULTS_FAILS/ARA/fsqrt.s) | [63](01_RESULTS_FAILS/ARA/fsqrt.s) |

Note: The ARA results were updated after the paper table was created.

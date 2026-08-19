# FP-RVVTS: Sail-Guided RISC-V Floating-Point Test Results

This repository contains FP-RVVTS test sets, reports, and categorized failure cases for Sail RISC-V vs. floating-point designs under test (DUTs) discussed in the paper [FP-RVVTS: Sail-guided Verification of RISC-V Floating-Point Implementations](https://ics.jku.at/files/2026FDL_FP-RVVTS.pdf) by Katharina Ruep, Manfred Schlägl, and Daniel Große.

**Note:** **The FP-RVVTS framework announced in the paper has since been integrated into the main [RVVTS repository](https://github.com/ics-jku/RVVTS). This repository contains the pre-generated FP-RVVTS test sets and the archived result reports for the RV64 artifact.**

FP-RVVTS extends RVVTS with Sail-guided generation of RISC-V floating-point tests. It creates positive tests from valid instructions and negative tests from invalid operand combinations, uses Sail RISC-V as the executable specification during generation, minimizes failing programs to isolated instructions, and classifies the resulting machine-state differences. The artifact material in this repository contains the RV64 F, D, and Zfh test sets and archived failure reports for a selected set of DUTs: Spike SF (SoftFloat), Spike FF (FloppyFloat), RISC-V VP++ SF (SoftFloat), RISC-V VP++ FF (FloppyFloat), QEMU, and PULP Ara (ARA).

## Test Sets and Results

| Artifact report | Reference model | Target | Notes |
| --- | --- | --- | --- |
| [FP-RVVTS RV64 test sets and results generated with Sail RISC-V](TestSets_FP_RefSail_RV64_v1/README.md) | Sail RISC-V | RV64 F/D/Zfh | Pre-generated positive and negative FP-RVVTS test cases and archived failure reports. |

## Citation

If you use this material or find it useful, please cite our papers as follows:

* [Katharina Ruep, Manfred Schlägl, and Daniel Große. FP-RVVTS: Sail-guided Verification of RISC-V Floating-Point Implementations. In Forum on Specification and Design Languages (FDL), 2026.](https://ics.jku.at/files/2026FDL_FP-RVVTS.pdf)
  ```bibtex
  @inproceedings{RSG:2026b,
    author =        {Katharina Ruep and Manfred Schl{\"{a}}gl and Daniel Gro{\ss}e},
    title =         {{FP-RVVTS:} {Sail}-guided Verification of {RISC-V} Floating-Point Implementations},
    booktitle =     {Forum on Specification and Design Languages (FDL)},
    url =           {https://ics.jku.at/files/2026FDL_FP-RVVTS.pdf},
    year =          {2026},
  }
  ```

* [Manfred Schlägl and Daniel Große. Single instruction isolation for RISC-V vector test failures. In IEEE/ACM International Conference on Computer-Aided Design (ICCAD), pages 156:1-156:9, 2024.](https://ics.jku.at/files/2024ICCAD_Single-Instruction-Isolation-for-RISC-V-Vector-Test-Failures.pdf)
  ```bibtex
  @inproceedings{SG:2024b,
    author = {Manfred Schl{\"{a}}gl and Daniel Gro{\ss}e},
    title = {Single Instruction Isolation for {RISC-V} Vector Test Failures},
    booktitle = {IEEE/ACM International Conference on Computer-Aided Design (ICCAD)},
    year = {2024},
    pages = {156:1--156:9},
    doi = {10.1145/3676536.3676755},
    code = {https://github.com/ics-jku/RVVTS},
    url = {https://ics.jku.at/files/2024ICCAD_Single-Instruction-Isolation-for-RISC-V-Vector-Test-Failures.pdf}
  }
  ```

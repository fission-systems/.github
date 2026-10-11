<div align="center">

<img src="https://raw.githubusercontent.com/fission-systems/.github/main/profile/logo.png" alt="Fission — reverse engineering workspace" width="480" />

**A Rust-native platform for binary analysis, reverse engineering, and program understanding**

[![CI](https://github.com/fission-systems/Fission/actions/workflows/ci.yml/badge.svg)](https://github.com/fission-systems/Fission/actions/workflows/ci.yml)
[![Latest Release](https://img.shields.io/github/v/release/fission-systems/Fission?color=5b7cf6&label=release)](https://github.com/fission-systems/Fission/releases/latest)
[![License](https://img.shields.io/badge/license-Apache--2.0-5b7cf6)](https://github.com/fission-systems/Fission/blob/main/LICENSE)
[![Rust](https://img.shields.io/badge/built%20with-Rust-orange?logo=rust)](https://github.com/fission-systems/Fission)

</div>

---

## [Fission](https://github.com/fission-systems/Fission)

A Rust-native reverse-engineering workspace. It loads binaries, lifts instruction semantics through Ghidra-style Sleigh specifications, and owns everything after that: its own IR, structuring, type recovery, and rendering.

The long-term goal is **restoration, not just readability**: taking a compiled binary back to a project that builds and runs again. That goal is **not reached yet**, and the project documents the gap openly.

<table>
<tr>
<td width="50%" valign="top">

**Analysis**
- Binary loading and Sleigh → P-code lifting
- NIR (exact semantics) / HIR (readable pseudocode) output layers
- Structuring: Ghidra-style collapse, angr Phoenix-style fold, and DREAM-style reaching conditions, competing per function
- Static analysis: xrefs, strings, function discovery, signature matching

</td>
<td width="50%" valign="top">

**Execution & Verification**
- P-code emulator (`fission-emulator`)
- Execution-based checking of decompiled bodies (`fission-dir`): run the original machine code, run the decompiled body, compare
- Unproven results are reported as assumptions, not hidden

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Evaluation**
- Scored on [DecBench](https://decbench.com): structure (CFG edit distance), types (vs. DWARF), and byte match (recompile and diff)
- Findings and rejected approaches are published in the repo's changelog and `docs/EVALUATION.md`

</td>
<td width="50%" valign="top">

**Interface: CLI agent-first**
- [`fission-cli`](https://github.com/fission-systems/Fission): command-line interface built to be driven by AI agents and scripts as well as people
- Commands: `info`, `list`, `disasm`, `decomp`, `xrefs`, with `--json` output for machine consumption

</td>
</tr>
</table>

---

## Repositories

| Repository | Description |
|---|---|
| [**Fission**](https://github.com/fission-systems/Fission) | Core workspace: loader, Sleigh lifting, NIR/HIR, decompiler, emulator, agent-first CLI |
| [**fission-benchmark**](https://github.com/fission-systems/fission-benchmark) | Multi-decompiler benchmark comparing Fission with Ghidra, angr, Radare2, Boomerang, Snowman, rev.ng, Reko, and RetDec, with a [live dashboard](https://fission-benchmark.vercel.app) |
| [**fission-research**](https://github.com/fission-systems/fission-research) | Experiments in semantic recovery: FSL/FIR, multi-architecture semantic patterns, and a pattern corpus |

---

## Principles

- **Correctness before presentation**: semantic evidence first
- **Reproducibility by default**: verifiable builds and results
- **Transparent evaluation**: failures stay visible
- **Measured quality claims**: no estimates as evidence
- **Open development**: decisions and limitations documented publicly

---

<div align="center">

**Built in Rust · Benchmarked against real binaries · Open development**

[Releases](https://github.com/fission-systems/Fission/releases) · [Benchmark Results](https://fission-benchmark.vercel.app) · [Contributing](https://github.com/fission-systems/Fission/blob/main/CONTRIBUTING.md)

</div>

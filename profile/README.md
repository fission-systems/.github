<div align="center">

<img src="https://raw.githubusercontent.com/fission-systems/.github/main/profile/logo.png" alt="Fission — reverse engineering workspace" width="480" />

**A Rust-native platform for binary analysis, reverse engineering, and program understanding**

[![CI](https://github.com/fission-systems/Fission/actions/workflows/ci.yml/badge.svg)](https://github.com/fission-systems/Fission/actions/workflows/ci.yml)
[![Latest Release](https://img.shields.io/github/v/release/fission-systems/Fission?color=5b7cf6&label=release)](https://github.com/fission-systems/Fission/releases/latest)
[![License](https://img.shields.io/badge/license-AGPL--3.0-5b7cf6)](https://github.com/fission-systems/Fission/blob/main/LICENSE)
[![Rust](https://img.shields.io/badge/built%20with-Rust-orange?logo=rust)](https://github.com/fission-systems/Fission)

</div>

---

## [Fission](https://github.com/fission-systems/Fission)

A multi-layered reverse engineering workspace built in Rust.

<table>
<tr>
<td width="50%" valign="top">

**Analysis**
- Binary lifting via Ghidra SLEIGH → P-code
- NIR/HIR structuring and pseudocode output
- Static analysis: xrefs, strings, discovery
- Function signature matching (FID)
- PE, ELF, Mach-O — x86 / x86-64 primary

</td>
<td width="50%" valign="top">

**Execution & Verification**
- P-code emulator with OS HLE
- Dynamic analysis and unpacker engine
- Time-travel debugging (TTD) snapshots
- Solver + emulator backed HIR verification
- Symbolic equivalence checking

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Automation & AI**
- Multi-provider AI agent pipeline
- Rhai-based binary automation scripting
- Quality lanes and regression tracking
- Plugin runtime facade

</td>
<td width="50%" valign="top">

**Interfaces**
- [`fission-cli`](https://github.com/fission-systems/Fission) — command-line
- [`fission-tui`](https://github.com/fission-systems/Fission) — terminal UI
- [`fission-dioxus`](https://github.com/fission-systems/Fission) — native desktop GUI
- [`fission-web`](https://github.com/fission-systems/fission-web) — browser WASM *(coming soon)*

</td>
</tr>
</table>

---

## [fission-benchmark](https://github.com/fission-systems/fission-benchmark)

Reproducible benchmark suite for decompiler quality evaluation.

- Source-semantic correctness scoring against real binaries
- Ghidra comparison lane
- Docker-based reproducible runner
- Public results dashboard

---

## Principles

- **Correctness before presentation** — semantic evidence first
- **Reproducibility by default** — verifiable builds and results
- **Transparent evaluation** — failures stay visible
- **Measured quality claims** — no estimates as evidence
- **Open development** — decisions and limitations documented publicly

---

<div align="center">

**Built in Rust · Benchmarked against real binaries · Open development**

[Releases](https://github.com/fission-systems/Fission/releases) · [Benchmark Results](https://fission-benchmark.vercel.app) · [Contributing](https://github.com/fission-systems/Fission/blob/main/CONTRIBUTING.md)

</div>

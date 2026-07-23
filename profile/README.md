<div align="center">

<img src="https://raw.githubusercontent.com/fission-systems/.github/main/profile/logo.png" alt="Fission — reverse engineering workspace" width="480" />

# Fission Systems

**Open-source decompiler and binary analysis infrastructure**

[![Fission CI](https://github.com/fission-systems/Fission/actions/workflows/ci.yml/badge.svg)](https://github.com/fission-systems/Fission/actions/workflows/ci.yml)
[![Latest Release](https://img.shields.io/github/v/release/fission-systems/Fission?color=5b7cf6&label=release)](https://github.com/fission-systems/Fission/releases/latest)
[![License](https://img.shields.io/badge/license-AGPL--3.0-5b7cf6)](https://github.com/fission-systems/Fission/blob/main/LICENSE)
[![Rust](https://img.shields.io/badge/built%20with-Rust-orange?logo=rust)](https://github.com/fission-systems/Fission)

</div>

---

## Projects

<table>
<tr>
<td width="50%" valign="top">

### [Fission](https://github.com/fission-systems/Fission)

A Rust-native decompiler and binary analysis framework.

- Ghidra SLEIGH-based P-code lifting
- NIR/HIR structuring and pseudocode output
- PE, ELF, Mach-O support
- x86 / x86-64 primary target

</td>
<td width="50%" valign="top">

### [fission-benchmark](https://github.com/fission-systems/fission-benchmark)

Reproducible benchmark suite for decompiler quality evaluation.

- Source-semantic correctness scoring
- Ghidra comparison lane
- Docker-based reproducible runner
- Public results dashboard

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [fission-web](https://github.com/fission-systems/fission-web) *(coming soon)*

Browser-native decompiler interface.

- Dioxus + WebAssembly
- All computation runs locally
- No binary data leaves your device
- Deployed via Vercel

</td>
<td width="50%" valign="top">

### Philosophy

- **Correctness before presentation** — semantic evidence first
- **Reproducibility by default** — verifiable builds and results
- **Transparent evaluation** — failures stay visible
- **Measured quality claims** — no estimates as evidence

</td>
</tr>
</table>

---

## Architecture

```
Binary (PE/ELF/Mach-O)
  └── fission-loader       — binary parsing, symbols, relocations
        └── fission-sleigh     — Ghidra SLEIGH lift → P-code
              └── fission-pcode    — NIR normalization, structuring
                    └── fission-decompiler — orchestration → pseudocode
                          ├── fission-cli      — command-line interface
                          ├── fission-dioxus   — native desktop GUI
                          └── fission-web      — browser WASM interface
```

---

<div align="center">

**Built in Rust · Benchmarked against real binaries · Open development**

[Releases](https://github.com/fission-systems/Fission/releases) · [Benchmark Results](https://fission-benchmark.vercel.app) · [Contributing](https://github.com/fission-systems/Fission/blob/main/CONTRIBUTING.md)

</div>

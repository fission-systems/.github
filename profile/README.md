<div align="center">

<img src="https://raw.githubusercontent.com/fission-systems/Fission/main/image/fission-logo.svg" alt="Fission Systems" width="680" />

# Fission Systems

**Agent-first reverse engineering infrastructure, built in Rust.**

Binary analysis · Decompilation · Semantic verification · Reproducible evaluation

[![Fission CI](https://github.com/fission-systems/Fission/actions/workflows/ci.yml/badge.svg)](https://github.com/fission-systems/Fission/actions/workflows/ci.yml)
[![Fission release](https://img.shields.io/github/v/release/fission-systems/Fission?sort=semver)](https://github.com/fission-systems/Fission/releases/latest)
[![License: Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](https://github.com/fission-systems/Fission/blob/main/LICENSE)
[![Rust](https://img.shields.io/badge/built%20with-Rust-orange?logo=rust)](https://github.com/fission-systems/Fission)

</div>

---

We build open-source tools for examining compiled programs, recovering understandable code, and testing results against observable behavior. Our focus is **independent analysis pipelines, automation-friendly interfaces, and evidence-backed engineering**.

## Fission: binary analysis and decompilation for agents

[**Fission**](https://github.com/fission-systems/Fission) is a Rust-native CLI for reverse engineering binaries. It reads ELF, PE, and Mach-O files, lifts instructions using Ghidra Sleigh processor specifications through its **own Rust runtime**, and implements downstream analysis and C output in Rust. **It does not run Ghidra.**

```text
Binary (ELF / PE / Mach-O)
    │
    ▼
Loader & static analysis
    │
    ▼
Rust Sleigh runtime → P-code
    │
    ▼
SSA · normalization · type recovery · CFG structuring
    │
    ▼
C output · inspection · automation
```

| Capability | What it provides |
| --- | --- |
| **Decompilation** | C output, control-flow structuring, type recovery, function and reference analysis |
| **Binary inspection** | Disassembly, strings, call graphs, cross-references, signatures, and patching |
| **Execution & verification** | Emulation and bounded checks of decompiled behavior against machine-code execution; solver-backed checks for eligible cases |
| **Agent-first CLI** | JSON output, versioned `--contract v1`, JSON Schema, stable error codes, and a built-in `skill` guide |
| **Debugging & internals** | Native debugging where supported, sandboxing, and inspection of raw P-code and intermediate stages |

Fission's current architecture combines published control-flow structuring approaches. Verification explicitly reports divergences and unsupported or inconclusive cases; it is **not** a blanket proof of correctness. Architecture support is measured per format and target; consult the [support matrix](https://github.com/fission-systems/Fission#what-it-reads).

### Get started

Install with [Homebrew](https://github.com/fission-systems/Fission#install) on macOS or Linux:

```bash
brew install fission-systems/tap/fission-cli
```

Then inspect a binary and decompile a function:

```bash
fission_cli info ./app
fission_cli list ./app
fission_cli decomp ./app --addr 0x401130
fission_cli --contract v1 decomp ./app --addr 0x401130 --json
```

Other installation paths include a verified install script, Cargo, and prebuilt releases. See the [quick start](https://github.com/fission-systems/Fission#quick-start), [CLI reference](https://github.com/fission-systems/Fission/blob/main/docs/CLI.md), and [agent interface](https://github.com/fission-systems/Fission#for-agents).

## Ecosystem

| Repository | Scope |
| --- | --- |
| [**Fission**](https://github.com/fission-systems/Fission) | Product decompiler, binary analysis CLI, emulation, and verification |
| [**fission-benchmark**](https://github.com/fission-systems/fission-benchmark) | **Fission-only**, locally run DecBench-style evaluation; [published results](https://fission-systems.github.io/fission-benchmark/) |
| [**fission-research**](https://github.com/fission-systems/fission-research) | Experimental FSL/FIR semantics, owned instruction specifications, and bounded reconstruction/recompilation research; **not** a production replacement for the current Sleigh pipeline |
| [**fission-forge**](https://github.com/fission-systems/fission-forge) | Rust/Candle research into a neural decompiler trained from scratch; training prototype, **not** a generally useful released model |

## How we work

- **Correctness before presentation.** A plausible decompilation is not automatically a behaviorally correct one.
- **Reproducibility by default.** Keep the corpus, toolchain, configuration, and evidence inspectable.
- **Transparent evaluation.** Report unsupported cases, failures, and limitations alongside successes.
- **Independent, composable tools.** Favor inspectable Rust components and interfaces that work for people, scripts, and agents.
- **Research claims stay scoped.** Experimental FSL/FIR and neural work are distinct from shipped Fission capabilities.

Our long-term work includes better semantic recovery and behavior-preserving reconstruction. Full source-project restoration and universal semantic equivalence are **not** current product guarantees.

## Contribute and explore

Contributions, reproducible failures, and technical discussions are welcome. Start with [Fission's contributor guide](https://github.com/fission-systems/Fission/blob/main/CONTRIBUTING.md) and [agent/development rules](https://github.com/fission-systems/Fission/blob/main/AGENTS.md). Report security issues according to the [security policy](https://github.com/fission-systems/Fission/blob/main/SECURITY.md).

<div align="center">

**Built in Rust · Designed for agents · Evaluated on real binaries**

[Source](https://github.com/fission-systems/Fission) · [Releases](https://github.com/fission-systems/Fission/releases) · [Evaluation](https://github.com/fission-systems/Fission/blob/main/docs/EVALUATION.md) · [Roadmap](https://github.com/fission-systems/Fission/blob/main/docs/roadmap/1.0-criteria.md)

</div>

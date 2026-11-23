# Fission Systems

**Agent-first reverse engineering infrastructure, built in Rust.**

Fission Systems develops open-source binary-analysis, decompilation, semantic-verification, and evaluation tooling. The organization's public GitHub landing page is defined by [`profile/README.md`](profile/README.md).

## Projects

| Repository | Role |
| --- | --- |
| [Fission](https://github.com/fission-systems/Fission) | Rust-native, agent-first binary analysis and decompilation CLI |
| [fission-benchmark](https://github.com/fission-systems/fission-benchmark) | Local, Fission-only DecBench-style evaluation and published results |
| [fission-research](https://github.com/fission-systems/fission-research) | Experimental FSL/FIR semantic recovery and owned-specification research |
| [fission-forge](https://github.com/fission-systems/fission-forge) | Experimental Rust/Candle neural decompiler training |

The shipped Fission pipeline uses its own Rust Sleigh runtime and downstream analysis. The FSL/FIR replacement path and neural decompilation are **research projects**, not shipped Fission capabilities.

## Where to start

- [Organization profile](profile/README.md) — overview of the ecosystem, principles, and quick start.
- [Fission README](https://github.com/fission-systems/Fission#readme) — installation, commands, current support, and architecture.
- [Fission CLI reference](https://github.com/fission-systems/Fission/blob/main/docs/CLI.md) — available commands and machine-readable contract.
- [Evaluation and limits](https://github.com/fission-systems/Fission/blob/main/docs/EVALUATION.md) — measured quality and known gaps.
- [Contributing](https://github.com/fission-systems/Fission/blob/main/CONTRIBUTING.md) — development and collaboration.

**Principles:** correctness before presentation, reproducible measurements, explicit limitations, and open development.

For exact commands, platform support, and release claims, follow the [Fission repository](https://github.com/fission-systems/Fission) as the source of truth.

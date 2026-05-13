# High-Performance Coding Skill

A Claude Code skill encoding universal high-performance computing principles. When active, Claude applies these patterns when writing or optimizing performance-critical code.

## Install

```bash
# Install as a Claude Code skill
cp -r high-performance-coding ~/.claude/skills/
```

Or install via plugin marketplace (once published).

## What It Covers

11 universal principles, ordered from diagnosis to implementation:

| # | Principle | Core Idea |
|---|-----------|-----------|
| 0 | Identify the Bottleneck | Roofline model, Amdahl's Law, Little's Law — is it compute or bandwidth bound? |
| 1 | Resource-Aware Parallelism | CPU/memory/IO/GPU/container — check actual server state, not theoretical capacity |
| 2 | Async Pipeline Design | Event loop, framework concurrency models, LLM/embedding throughput |
| 3 | GPU Acceleration | Benchmark methodology, CUDA/PyTorch profiling, sparse vs dense, gradient accumulation |
| 4 | Validate Before Scaling | Subset → verify → medium → verify → full |
| 5 | Fast Paths | Lock-free check, single-owner skip, power-of-two, relaxed ordering |
| 6 | Memory Access Patterns | Cache lines, false sharing, AoS vs SoA, NUMA |
| 7 | Error Resilience | Timeouts, graceful degradation, retry strategy |
| 8 | Design for Interruption | 5-level checkpoint/resume: skip-existing → tracked IDs → structured checkpoints → auto-recovery → survive process death |
| 9 | Compile-Time Optimization | Rust/C++/Go build flags |
| 10 | Data Structures | RCU, SPSC ring buffer, LSM-tree, radix tree, neighbor sampling |

## Languages

Patterns cover Python, Rust, C++, CUDA C, and Go with concrete API references.

## Quick Reference

The skill includes a 23-entry lookup table mapping constraints to strategies — e.g., "CPU-bound → Process pool, start conservative on *free* cores" or "GPU timing → sync → run → sync → clock."

## License

MIT

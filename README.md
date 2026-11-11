# Pratham Desai

**Low-latency C++ / HFT engineer.** I build live trading, market-data and risk systems for NSE derivatives: feed handlers, lock-free infrastructure, and real-time Greeks and margin engines. Currently at ANV Fintech (Arham Share), Surat.

[Portfolio](https://prathamdesai07.github.io/portfolio/) · [Email](mailto:prathamdesai071204@gmail.com)

| 1.15M+ packets/sec | 50–150 ns p50 | 80–150 ns p50 | ~0.3 µs |
|:---:|:---:|:---:|:---:|
| MTBT feed handler | pre-trade risk check | cross-process IPC hop | arbitrage gateway compute |

## Experience

**Trading Systems Engineer, C++ — ANV Fintech (Arham Share Pvt Ltd)** · May 2025 – Present

- **MTBT feed handler**: ~1.15M packets/sec with NIC-level parsing, O(1) order book updates, lock-free ring buffers and a cache-friendly layout.
- **Risk engine**: SPAN, MTM, AEL, physical delivery, peak margin and VaR. CAS-based reservation gives lock-free pre-trade checks at 50–150 ns p50 and 500 ns–2 µs p99.
- **Greeks pricing engine**: allocation-free C++ for live Greeks on NSE derivatives. AVX2 recomputation at ~176 µs per tick using dirty-flag invalidation.
- **Cross-exchange arbitrage gateway**: opportunity scanning, order routing, position limits and pre-trade checks at ~0.3 µs compute.
- **Performance work**: multi-threaded C++ on Linux tuned with perf, CPU affinity and NUMA-aware placement.

## Research

**[Online Likelihood Estimation of Near-critical Hawkes Processes: Logarithmic Regret and Loss of Identifiability](https://doi.org/10.2139/ssrn.7676119)** — SSRN, October 2026.
Online estimation for Hawkes processes close to criticality, with a logarithmic regret bound and a loss-of-identifiability result. Notes, proofs and simulation code are in [Hawkes](https://github.com/PrathamDesai07/Hawkes).

## Projects

| Project | What it is | Stack |
|---|---|---|
| **NUMA-aware lock-free IPC bus** | Disruptor-style single-writer, multi-reader shared-memory ring for trading systems. 80–150 ns p50 and 200–400 ns p99 per cross-process hop, 1.15M+ messages/sec, zero steady-state syscalls | C++17 |
| **GPU Monte Carlo exotic option pricer** | European, Asian, barrier and American (Longstaff–Schwartz) options with Sobol sequences, antithetic sampling and control variates. ~50–100× GPU speedup, ~30–60× variance reduction | C++, CUDA |
| **[mtbt_go](https://github.com/PrathamDesai07/mtbt_go)** | Order book builder for NSE's tick-by-tick futures and options feed: pinned-core multicast receivers, lock-free queues, sequence merging and gap recovery | Go |
| **[CryptoTradingSystem](https://github.com/PrathamDesai07/CryptoTradingSystem)** | Real-time system on Binance market data: candle aggregation, strategy engine, pre-trade risk checks, order reconciliation and a live dashboard | Python, JavaScript |
| **[LowLatencyOrderBook](https://github.com/PrathamDesai07/LowLatencyOrderBook)** | NSE market data forwarder and order book | C++ |

## Open source

Contributor to **[CVXPY](https://github.com/cvxpy/cvxpy)**, the Python modelling language for convex optimisation.

- Merged: [partial_trace and partial_transpose propagate DCP attributes (#3409)](https://github.com/cvxpy/cvxpy/pull/3409)
- Open: [O(n) canonicalisation for quantum_rel_entr (#3372)](https://github.com/cvxpy/cvxpy/pull/3372)

## Toolkit

- **Languages**: C++17, C, Python, Bash
- **Systems and performance**: Linux systems programming, CPU and cache behaviour, NUMA, IRQ and CPU pinning, hugepages, tail-latency profiling (perf, tcpdump)
- **Networking**: AF_XDP, DPDK, kernel-bypass TCP/UDP, NIC tuning
- **Trading and risk**: SPAN, MTM, AEL, peak margin, VaR, pre-trade risk checks

## Education

**B.Tech in Computer Science, Sarvajanik College of Engineering and Technology** · 2022 – 2026 · CGPA 9.38/10

- GATE 2026 (Computer Science): AIR 987, top 0.5% nationally
- Gold and bronze medalist, Mathematics and Informatics Olympiads
- Co-author of a Wiley chapter on quantum-secured identifiers for 6G

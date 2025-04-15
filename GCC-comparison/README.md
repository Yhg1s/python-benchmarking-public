# GCC x86_64 Comparisons on CPython

Ad-hoc comparison between different GCC versions, since I had this data
available. All measurements done at the same commit
([1f5682f3a27516833f7c317707dd359280dba6e7](https://github.com/python/cpython/commit/1f5682f3a27516833f7c317707dd359280dba6e7)
with https://github.com/python/cpython/pull/132530 applied).

GCC versions used:

- 5.4.0 from Ubuntu 16.04
- 7.5.0 from Ubuntu 18.04
- 9.4.0 from Ubuntu 20.04
- 10.2.1 from Debian
- 11.4.0 from Ubuntu 22.04
- 12.4.0 from Debian
- 13.3.0 from Debian
- 14.2.0 from Debian
- 15-20250406-1 from Debian experimental

The majority of the [Faster
CPython](https://github.com/faster-cpython/benchmarking-public) and
[Meta](https://github.com/facebookexperimental/free-threading-benchmarking)
benchmarks for x86_64-linux use GCC 9.4 (presumably from Ubuntu), so I've
used GCC 9.4 as the baseline for the compiler comparisons below. While the
_compilers_ are from different Ubuntu/Debian versions, the rest of the
system is entirely the same. I run a slightly smaller set of the benchmarks
(eliminating the most noisy ones) in an effort to get more stable results.

## Regular builds (baseline is GCC 9.4)

| commit | change |
| -- | -- |
| bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5 | 1.022x ↓[📄](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5-vs-bm-20250414-centurion-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5-vs-bm-20250414-centurion-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5-vs-bm-20250414-centurion-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7 | 1.025x ↓[📄](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7-vs-bm-20250414-centurion-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7-vs-bm-20250414-centurion-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7-vs-bm-20250414-centurion-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc10 | 1.015x ↓[📄](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc10-vs-bm-20250414-centurion-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc10-vs-bm-20250414-centurion-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc10-vs-bm-20250414-centurion-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11 | 1.003x ↓[📄](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11-vs-bm-20250414-centurion-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11-vs-bm-20250414-centurion-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11-vs-bm-20250414-centurion-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12 | 1.003x ↓[📄](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12-vs-bm-20250414-centurion-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12-vs-bm-20250414-centurion-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12-vs-bm-20250414-centurion-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13 | 1.003x ↓[📄](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13-vs-bm-20250414-centurion-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13-vs-bm-20250414-centurion-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13-vs-bm-20250414-centurion-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14 | 1.034x ↓[📄](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14-vs-bm-20250414-centurion-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14-vs-bm-20250414-centurion-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14-vs-bm-20250414-centurion-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15 | 1.010x ↑[📄](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15-vs-bm-20250414-centurion-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15-vs-bm-20250414-centurion-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15-vs-bm-20250414-centurion-x86_64-python-main-3.14-mem.svg) |

## Free-threaded (baseline is GCC 9.4)

| commit | change |
| -- | -- |
| bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5 | 1.138x ↓[📄](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.md)[📈](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7 | 1.050x ↓[📄](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.md)[📈](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10 | 1.011x ↓[📄](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.md)[📈](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11 | 1.002x ↓[📄](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.md)[📈](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12 | 1.065x ↓[📄](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.md)[📈](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13 | 1.070x ↓[📄](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.md)[📈](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14 | 1.077x ↓[📄](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.md)[📈](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14-mem.svg) |
| bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15 | 1.008x ↑[📄](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.md)[📈](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14.svg)[🧠](bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15-vs-bm-20250414-centurion-x86_64-python-NOGIL-3.14-mem.svg) |

# Regular versus Free-Threaded (same compiler)

| commit | change |
| -- | -- |
| bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL | 1.158x ↓[📄](bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc5-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc5-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc5-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL | 1.069x ↓[📄](bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc7-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc7-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc7-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL | 1.045x ↓[📄](bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc9-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc9-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc9-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL | 1.041x ↓[📄](bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc10-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc10-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc10-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL | 1.044x ↓[📄](bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc11-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc11-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc11-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL | 1.104x ↓[📄](bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc12-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc12-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc12-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL | 1.109x ↓[📄](bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc13-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc13-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc13-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL | 1.087x ↓[📄](bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc14-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc14-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc14-x86_64-python-main-3.14-mem.svg) |
| bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL | 1.045x ↓[📄](bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc15-x86_64-python-main-3.14.md)[📈](bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc15-x86_64-python-main-3.14.svg)[🧠](bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL-vs-bm-20250414-centurion_gcc15-x86_64-python-main-3.14-mem.svg) |

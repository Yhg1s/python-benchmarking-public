# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL
- machine: unknown-unknown
- commit hash: 7890b77
- commit date: 2025-04-14
- overall geometric mean: 1.109x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.50x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 193 ms                                                          | 220 ms: 1.14x slower                                           |
| docutils       | 2.02 sec                                                        | 2.18 sec: 1.08x slower                                         |
| html5lib       | 45.9 ms                                                         | 50.4 ms: 1.10x slower                                          |
| sphinx         | 766 ms                                                          | 841 ms: 1.10x slower                                           |
| Geometric mean | (ref)                                                           | 1.10x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_none_tg              | 219 ms                                                          | 188 ms: 1.16x faster                                           |
| async_tree_memoization_tg       | 275 ms                                                          | 251 ms: 1.10x faster                                           |
| async_tree_cpu_io_mixed_tg      | 419 ms                                                          | 394 ms: 1.06x faster                                           |
| async_tree_none                 | 234 ms                                                          | 223 ms: 1.05x faster                                           |
| async_tree_eager_memoization_tg | 235 ms                                                          | 226 ms: 1.04x faster                                           |
| async_tree_cpu_io_mixed         | 421 ms                                                          | 424 ms: 1.01x slower                                           |
| coroutines                      | 14.7 ms                                                         | 15.2 ms: 1.04x slower                                          |
| async_tree_memoization          | 269 ms                                                          | 280 ms: 1.04x slower                                           |
| async_tree_eager_cpu_io_mixed   | 322 ms                                                          | 340 ms: 1.05x slower                                           |
| async_generators                | 234 ms                                                          | 263 ms: 1.13x slower                                           |
| async_tree_eager                | 79.2 ms                                                         | 102 ms: 1.28x slower                                           |
| Geometric mean                  | (ref)                                                           | 1.01x slower                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 181 ms                                                          | 179 ms: 1.02x faster                                           |
| float          | 47.6 ms                                                         | 53.6 ms: 1.13x slower                                          |
| Geometric mean | (ref)                                                           | 1.05x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_dna      | 143 ms                                                          | 146 ms: 1.02x slower                                           |
| regex_v8       | 14.7 ms                                                         | 15.6 ms: 1.06x slower                                          |
| regex_compile  | 91.9 ms                                                         | 114 ms: 1.24x slower                                           |
| Geometric mean | (ref)                                                           | 1.10x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 68.5 ms                                                         | 59.3 ms: 1.16x faster                                          |
| xml_etree_parse      | 97.9 ms                                                         | 96.8 ms: 1.01x faster                                          |
| json_loads           | 17.8 us                                                         | 19.7 us: 1.11x slower                                          |
| xml_etree_generate   | 67.0 ms                                                         | 75.1 ms: 1.12x slower                                          |
| xml_etree_process    | 48.1 ms                                                         | 54.6 ms: 1.14x slower                                          |
| unpickle_pure_python | 158 us                                                          | 183 us: 1.16x slower                                           |
| json_dumps           | 7.58 ms                                                         | 8.80 ms: 1.16x slower                                          |
| pickle_pure_python   | 228 us                                                          | 267 us: 1.17x slower                                           |
| tomli_loads          | 1.36 sec                                                        | 1.68 sec: 1.23x slower                                         |
| Geometric mean       | (ref)                                                           | 1.10x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL |
|------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                         | 12.8 ms: 1.19x slower                                          |
| python_startup_no_site | 7.47 ms                                                         | 9.38 ms: 1.26x slower                                          |
| Geometric mean         | (ref)                                                           | 1.22x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL |
|-----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| django_template | 28.9 ms                                                         | 34.3 ms: 1.19x slower                                          |
| genshi_xml      | 38.0 ms                                                         | 47.8 ms: 1.26x slower                                          |
| genshi_text     | 16.1 ms                                                         | 21.8 ms: 1.36x slower                                          |
| mako            | 7.54 ms                                                         | 11.6 ms: 1.53x slower                                          |
| Geometric mean  | (ref)                                                           | 1.33x slower                                                   |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc13-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal                    | 3.15 ms                                                         | 1.32 ms: 2.39x faster                                          |
| create_gc_cycles                | 1.74 ms                                                         | 1.14 ms: 1.53x faster                                          |
| async_tree_none_tg              | 219 ms                                                          | 188 ms: 1.16x faster                                           |
| xml_etree_iterparse             | 68.5 ms                                                         | 59.3 ms: 1.16x faster                                          |
| async_tree_memoization_tg       | 275 ms                                                          | 251 ms: 1.10x faster                                           |
| async_tree_cpu_io_mixed_tg      | 419 ms                                                          | 394 ms: 1.06x faster                                           |
| async_tree_none                 | 234 ms                                                          | 223 ms: 1.05x faster                                           |
| async_tree_eager_memoization_tg | 235 ms                                                          | 226 ms: 1.04x faster                                           |
| sqlite_synth                    | 1.58 us                                                         | 1.54 us: 1.03x faster                                          |
| pidigits                        | 181 ms                                                          | 179 ms: 1.02x faster                                           |
| xml_etree_parse                 | 97.9 ms                                                         | 96.8 ms: 1.01x faster                                          |
| async_tree_cpu_io_mixed         | 421 ms                                                          | 424 ms: 1.01x slower                                           |
| regex_dna                       | 143 ms                                                          | 146 ms: 1.02x slower                                           |
| coroutines                      | 14.7 ms                                                         | 15.2 ms: 1.04x slower                                          |
| async_tree_memoization          | 269 ms                                                          | 280 ms: 1.04x slower                                           |
| json                            | 3.43 ms                                                         | 3.58 ms: 1.05x slower                                          |
| async_tree_eager_cpu_io_mixed   | 322 ms                                                          | 340 ms: 1.05x slower                                           |
| regex_v8                        | 14.7 ms                                                         | 15.6 ms: 1.06x slower                                          |
| bpe_tokeniser                   | 3.08 sec                                                        | 3.31 sec: 1.07x slower                                         |
| docutils                        | 2.02 sec                                                        | 2.18 sec: 1.08x slower                                         |
| many_optionals                  | 726 us                                                          | 787 us: 1.08x slower                                           |
| mdp                             | 925 ms                                                          | 1.00 sec: 1.09x slower                                         |
| dulwich_log                     | 42.8 ms                                                         | 46.6 ms: 1.09x slower                                          |
| html5lib                        | 45.9 ms                                                         | 50.4 ms: 1.10x slower                                          |
| sphinx                          | 766 ms                                                          | 841 ms: 1.10x slower                                           |
| json_loads                      | 17.8 us                                                         | 19.7 us: 1.11x slower                                          |
| sympy_sum                       | 103 ms                                                          | 116 ms: 1.12x slower                                           |
| xml_etree_generate              | 67.0 ms                                                         | 75.1 ms: 1.12x slower                                          |
| async_generators                | 234 ms                                                          | 263 ms: 1.13x slower                                           |
| float                           | 47.6 ms                                                         | 53.6 ms: 1.13x slower                                          |
| subparsers                      | 17.0 ms                                                         | 19.3 ms: 1.14x slower                                          |
| xml_etree_process               | 48.1 ms                                                         | 54.6 ms: 1.14x slower                                          |
| 2to3                            | 193 ms                                                          | 220 ms: 1.14x slower                                           |
| sqlglot_v2_optimize             | 38.2 ms                                                         | 43.7 ms: 1.14x slower                                          |
| sqlalchemy_imperative           | 14.4 ms                                                         | 16.4 ms: 1.14x slower                                          |
| telco                           | 5.36 ms                                                         | 6.14 ms: 1.15x slower                                          |
| unpickle_pure_python            | 158 us                                                          | 183 us: 1.16x slower                                           |
| sympy_integrate                 | 14.8 ms                                                         | 17.1 ms: 1.16x slower                                          |
| sqlalchemy_declarative          | 97.8 ms                                                         | 114 ms: 1.16x slower                                           |
| json_dumps                      | 7.58 ms                                                         | 8.80 ms: 1.16x slower                                          |
| sympy_str                       | 190 ms                                                          | 220 ms: 1.16x slower                                           |
| sympy_expand                    | 324 ms                                                          | 377 ms: 1.16x slower                                           |
| connected_components            | 430 ms                                                          | 501 ms: 1.17x slower                                           |
| pickle_pure_python              | 228 us                                                          | 267 us: 1.17x slower                                           |
| sqlglot_v2_normalize            | 76.4 ms                                                         | 89.6 ms: 1.17x slower                                          |
| shortest_path                   | 441 ms                                                          | 522 ms: 1.19x slower                                           |
| django_template                 | 28.9 ms                                                         | 34.3 ms: 1.19x slower                                          |
| python_startup                  | 10.8 ms                                                         | 12.8 ms: 1.19x slower                                          |
| nqueens                         | 56.5 ms                                                         | 68.1 ms: 1.20x slower                                          |
| meteor_contest                  | 84.0 ms                                                         | 102 ms: 1.21x slower                                           |
| deepcopy                        | 194 us                                                          | 234 us: 1.21x slower                                           |
| deepcopy_reduce                 | 2.03 us                                                         | 2.49 us: 1.23x slower                                          |
| sqlglot_v2_transpile            | 1.14 ms                                                         | 1.41 ms: 1.23x slower                                          |
| pprint_safe_repr                | 498 ms                                                          | 614 ms: 1.23x slower                                           |
| tomli_loads                     | 1.36 sec                                                        | 1.68 sec: 1.23x slower                                         |
| comprehensions                  | 11.4 us                                                         | 14.2 us: 1.24x slower                                          |
| regex_compile                   | 91.9 ms                                                         | 114 ms: 1.24x slower                                           |
| pyflate                         | 298 ms                                                          | 372 ms: 1.25x slower                                           |
| crypto_pyaes                    | 52.3 ms                                                         | 65.5 ms: 1.25x slower                                          |
| python_startup_no_site          | 7.47 ms                                                         | 9.38 ms: 1.26x slower                                          |
| genshi_xml                      | 38.0 ms                                                         | 47.8 ms: 1.26x slower                                          |
| pprint_pformat                  | 1.01 sec                                                        | 1.28 sec: 1.27x slower                                         |
| raytrace                        | 189 ms                                                          | 241 ms: 1.28x slower                                           |
| async_tree_eager                | 79.2 ms                                                         | 102 ms: 1.28x slower                                           |
| sqlglot_v2_parse                | 885 us                                                          | 1.16 ms: 1.31x slower                                          |
| hexiom                          | 3.97 ms                                                         | 5.31 ms: 1.34x slower                                          |
| deltablue                       | 2.17 ms                                                         | 2.94 ms: 1.35x slower                                          |
| genshi_text                     | 16.1 ms                                                         | 21.8 ms: 1.36x slower                                          |
| typing_runtime_protocols        | 102 us                                                          | 142 us: 1.39x slower                                           |
| deepcopy_memo                   | 18.5 us                                                         | 25.9 us: 1.40x slower                                          |
| coverage                        | 54.5 ms                                                         | 77.7 ms: 1.42x slower                                          |
| richards                        | 30.3 ms                                                         | 45.7 ms: 1.51x slower                                          |
| mako                            | 7.54 ms                                                         | 11.6 ms: 1.53x slower                                          |
| Geometric mean                  | (ref)                                                           | 1.12x slower                                                   |

Benchmark hidden because not significant (1): pathlib

- Geometric mean (including insignificant results): 1.109x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.50x
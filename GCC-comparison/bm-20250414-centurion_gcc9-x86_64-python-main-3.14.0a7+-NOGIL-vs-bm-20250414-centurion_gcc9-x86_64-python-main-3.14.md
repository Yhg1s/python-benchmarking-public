# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.045x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.48x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 194 ms                                                         | 207 ms: 1.06x slower                                          |
| docutils       | 1.95 sec                                                       | 2.02 sec: 1.04x slower                                        |
| html5lib       | 46.6 ms                                                        | 47.1 ms: 1.01x slower                                         |
| sphinx         | 755 ms                                                         | 788 ms: 1.04x slower                                          |
| Geometric mean | (ref)                                                          | 1.04x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none_tg              | 220 ms                                                         | 169 ms: 1.30x faster                                          |
| async_tree_memoization_tg       | 276 ms                                                         | 227 ms: 1.22x faster                                          |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                         | 345 ms: 1.14x faster                                          |
| async_tree_none                 | 232 ms                                                         | 205 ms: 1.13x faster                                          |
| async_tree_eager_memoization_tg | 236 ms                                                         | 211 ms: 1.11x faster                                          |
| async_tree_memoization          | 270 ms                                                         | 254 ms: 1.06x faster                                          |
| async_tree_cpu_io_mixed         | 395 ms                                                         | 374 ms: 1.06x faster                                          |
| coroutines                      | 14.5 ms                                                        | 14.4 ms: 1.01x faster                                         |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                         | 305 ms: 1.02x slower                                          |
| async_generators                | 215 ms                                                         | 238 ms: 1.11x slower                                          |
| async_tree_eager                | 81.0 ms                                                        | 94.7 ms: 1.17x slower                                         |
| Geometric mean                  | (ref)                                                          | 1.06x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 184 ms                                                         | 181 ms: 1.02x faster                                          |
| Geometric mean | (ref)                                                          | 1.01x faster                                                  |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_v8       | 15.2 ms                                                        | 14.9 ms: 1.02x faster                                         |
| regex_dna      | 156 ms                                                         | 158 ms: 1.01x slower                                          |
| regex_compile  | 90.1 ms                                                        | 102 ms: 1.13x slower                                          |
| Geometric mean | (ref)                                                          | 1.04x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 77.8 ms                                                        | 64.7 ms: 1.20x faster                                         |
| unpickle_pure_python | 155 us                                                         | 155 us: 1.00x faster                                          |
| xml_etree_parse      | 92.9 ms                                                        | 94.4 ms: 1.02x slower                                         |
| xml_etree_process    | 44.9 ms                                                        | 46.6 ms: 1.04x slower                                         |
| xml_etree_generate   | 62.2 ms                                                        | 64.9 ms: 1.04x slower                                         |
| pickle_pure_python   | 224 us                                                         | 243 us: 1.08x slower                                          |
| tomli_loads          | 1.40 sec                                                       | 1.53 sec: 1.09x slower                                        |
| json_dumps           | 7.27 ms                                                        | 7.98 ms: 1.10x slower                                         |
| json_loads           | 17.4 us                                                        | 19.5 us: 1.12x slower                                         |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL |
|------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                        | 13.0 ms: 1.20x slower                                         |
| python_startup_no_site | 7.53 ms                                                        | 9.52 ms: 1.26x slower                                         |
| Geometric mean         | (ref)                                                          | 1.23x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL |
|-----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| genshi_xml      | 39.4 ms                                                        | 41.7 ms: 1.06x slower                                         |
| django_template | 27.9 ms                                                        | 30.8 ms: 1.10x slower                                         |
| genshi_text     | 16.0 ms                                                        | 18.7 ms: 1.18x slower                                         |
| mako            | 7.37 ms                                                        | 10.7 ms: 1.45x slower                                         |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                  |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc9-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| gc_traversal                    | 3.06 ms                                                        | 1.48 ms: 2.07x faster                                         |
| create_gc_cycles                | 1.77 ms                                                        | 1.16 ms: 1.52x faster                                         |
| async_tree_none_tg              | 220 ms                                                         | 169 ms: 1.30x faster                                          |
| async_tree_memoization_tg       | 276 ms                                                         | 227 ms: 1.22x faster                                          |
| xml_etree_iterparse             | 77.8 ms                                                        | 64.7 ms: 1.20x faster                                         |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                         | 345 ms: 1.14x faster                                          |
| async_tree_none                 | 232 ms                                                         | 205 ms: 1.13x faster                                          |
| async_tree_eager_memoization_tg | 236 ms                                                         | 211 ms: 1.11x faster                                          |
| sqlite_synth                    | 1.56 us                                                        | 1.47 us: 1.06x faster                                         |
| async_tree_memoization          | 270 ms                                                         | 254 ms: 1.06x faster                                          |
| deltablue                       | 2.65 ms                                                        | 2.50 ms: 1.06x faster                                         |
| async_tree_cpu_io_mixed         | 395 ms                                                         | 374 ms: 1.06x faster                                          |
| mdp                             | 945 ms                                                         | 925 ms: 1.02x faster                                          |
| pidigits                        | 184 ms                                                         | 181 ms: 1.02x faster                                          |
| regex_v8                        | 15.2 ms                                                        | 14.9 ms: 1.02x faster                                         |
| coroutines                      | 14.5 ms                                                        | 14.4 ms: 1.01x faster                                         |
| unpickle_pure_python            | 155 us                                                         | 155 us: 1.00x faster                                          |
| pathlib                         | 13.0 ms                                                        | 13.1 ms: 1.01x slower                                         |
| bpe_tokeniser                   | 3.11 sec                                                       | 3.13 sec: 1.01x slower                                        |
| html5lib                        | 46.6 ms                                                        | 47.1 ms: 1.01x slower                                         |
| regex_dna                       | 156 ms                                                         | 158 ms: 1.01x slower                                          |
| xml_etree_parse                 | 92.9 ms                                                        | 94.4 ms: 1.02x slower                                         |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                         | 305 ms: 1.02x slower                                          |
| sqlglot_v2_normalize            | 78.5 ms                                                        | 80.1 ms: 1.02x slower                                         |
| many_optionals                  | 731 us                                                         | 751 us: 1.03x slower                                          |
| sqlglot_v2_optimize             | 38.6 ms                                                        | 39.7 ms: 1.03x slower                                         |
| docutils                        | 1.95 sec                                                       | 2.02 sec: 1.04x slower                                        |
| xml_etree_process               | 44.9 ms                                                        | 46.6 ms: 1.04x slower                                         |
| json                            | 3.35 ms                                                        | 3.48 ms: 1.04x slower                                         |
| subparsers                      | 17.6 ms                                                        | 18.4 ms: 1.04x slower                                         |
| sphinx                          | 755 ms                                                         | 788 ms: 1.04x slower                                          |
| xml_etree_generate              | 62.2 ms                                                        | 64.9 ms: 1.04x slower                                         |
| genshi_xml                      | 39.4 ms                                                        | 41.7 ms: 1.06x slower                                         |
| sympy_sum                       | 105 ms                                                         | 112 ms: 1.06x slower                                          |
| dulwich_log                     | 42.7 ms                                                        | 45.2 ms: 1.06x slower                                         |
| 2to3                            | 194 ms                                                         | 207 ms: 1.06x slower                                          |
| pickle_pure_python              | 224 us                                                         | 243 us: 1.08x slower                                          |
| tomli_loads                     | 1.40 sec                                                       | 1.53 sec: 1.09x slower                                        |
| sympy_integrate                 | 15.2 ms                                                        | 16.6 ms: 1.09x slower                                         |
| pyflate                         | 310 ms                                                         | 339 ms: 1.09x slower                                          |
| json_dumps                      | 7.27 ms                                                        | 7.98 ms: 1.10x slower                                         |
| sympy_str                       | 192 ms                                                         | 211 ms: 1.10x slower                                          |
| sympy_expand                    | 327 ms                                                         | 360 ms: 1.10x slower                                          |
| django_template                 | 27.9 ms                                                        | 30.8 ms: 1.10x slower                                         |
| sqlglot_v2_transpile            | 1.14 ms                                                        | 1.26 ms: 1.10x slower                                         |
| async_generators                | 215 ms                                                         | 238 ms: 1.11x slower                                          |
| comprehensions                  | 10.8 us                                                        | 11.9 us: 1.11x slower                                         |
| json_loads                      | 17.4 us                                                        | 19.5 us: 1.12x slower                                         |
| connected_components            | 433 ms                                                         | 486 ms: 1.12x slower                                          |
| deepcopy_reduce                 | 1.98 us                                                        | 2.23 us: 1.13x slower                                         |
| regex_compile                   | 90.1 ms                                                        | 102 ms: 1.13x slower                                          |
| crypto_pyaes                    | 52.7 ms                                                        | 59.5 ms: 1.13x slower                                         |
| sqlalchemy_declarative          | 96.2 ms                                                        | 109 ms: 1.14x slower                                          |
| hexiom                          | 4.08 ms                                                        | 4.64 ms: 1.14x slower                                         |
| nqueens                         | 54.0 ms                                                        | 61.6 ms: 1.14x slower                                         |
| deepcopy                        | 185 us                                                         | 211 us: 1.14x slower                                          |
| pprint_safe_repr                | 464 ms                                                         | 530 ms: 1.14x slower                                          |
| sqlalchemy_imperative           | 14.1 ms                                                        | 16.2 ms: 1.15x slower                                         |
| shortest_path                   | 442 ms                                                         | 507 ms: 1.15x slower                                          |
| sqlglot_v2_parse                | 894 us                                                         | 1.03 ms: 1.15x slower                                         |
| meteor_contest                  | 84.6 ms                                                        | 97.9 ms: 1.16x slower                                         |
| richards                        | 31.0 ms                                                        | 36.1 ms: 1.17x slower                                         |
| raytrace                        | 186 ms                                                         | 217 ms: 1.17x slower                                          |
| async_tree_eager                | 81.0 ms                                                        | 94.7 ms: 1.17x slower                                         |
| telco                           | 5.15 ms                                                        | 6.04 ms: 1.17x slower                                         |
| genshi_text                     | 16.0 ms                                                        | 18.7 ms: 1.18x slower                                         |
| pprint_pformat                  | 943 ms                                                         | 1.12 sec: 1.18x slower                                        |
| deepcopy_memo                   | 18.0 us                                                        | 21.4 us: 1.19x slower                                         |
| python_startup                  | 10.9 ms                                                        | 13.0 ms: 1.20x slower                                         |
| typing_runtime_protocols        | 107 us                                                         | 132 us: 1.24x slower                                          |
| python_startup_no_site          | 7.53 ms                                                        | 9.52 ms: 1.26x slower                                         |
| coverage                        | 54.6 ms                                                        | 78.4 ms: 1.44x slower                                         |
| mako                            | 7.37 ms                                                        | 10.7 ms: 1.45x slower                                         |
| Geometric mean                  | (ref)                                                          | 1.05x slower                                                  |

Benchmark hidden because not significant (1): float

- Geometric mean (including insignificant results): 1.045x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.48x
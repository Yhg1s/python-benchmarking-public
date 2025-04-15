# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.011x slower
- HPT reliability: 99.41%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| 2to3           | 207 ms                                                   | 206 ms: 1.00x faster                                      |
| docutils       | 2.02 sec                                                 | 2.13 sec: 1.06x slower                                    |
| html5lib       | 47.1 ms                                                  | 46.9 ms: 1.00x faster                                     |
| sphinx         | 788 ms                                                   | 817 ms: 1.04x slower                                      |
| Geometric mean | (ref)                                                    | 1.02x slower                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| async_tree_eager                | 94.7 ms                                                  | 95.7 ms: 1.01x slower                                     |
| async_tree_none                 | 205 ms                                                   | 207 ms: 1.01x slower                                      |
| async_tree_eager_memoization_tg | 211 ms                                                   | 216 ms: 1.02x slower                                      |
| async_tree_memoization          | 254 ms                                                   | 261 ms: 1.03x slower                                      |
| async_tree_memoization_tg       | 227 ms                                                   | 236 ms: 1.04x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 177 ms: 1.05x slower                                      |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 322 ms: 1.06x slower                                      |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 396 ms: 1.06x slower                                      |
| async_generators                | 238 ms                                                   | 253 ms: 1.07x slower                                      |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 371 ms: 1.07x slower                                      |
| Geometric mean                  | (ref)                                                    | 1.04x slower                                              |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| regex_v8       | 14.9 ms                                                  | 14.2 ms: 1.05x faster                                     |
| regex_dna      | 158 ms                                                   | 154 ms: 1.03x faster                                      |
| regex_compile  | 102 ms                                                   | 103 ms: 1.02x slower                                      |
| Geometric mean | (ref)                                                    | 1.02x faster                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| xml_etree_iterparse  | 64.7 ms                                                  | 58.2 ms: 1.11x faster                                     |
| tomli_loads          | 1.53 sec                                                 | 1.46 sec: 1.05x faster                                    |
| pickle_pure_python   | 243 us                                                   | 236 us: 1.03x faster                                      |
| unpickle_pure_python | 155 us                                                   | 159 us: 1.03x slower                                      |
| xml_etree_parse      | 94.4 ms                                                  | 97.6 ms: 1.03x slower                                     |
| json_loads           | 19.5 us                                                  | 20.4 us: 1.05x slower                                     |
| json_dumps           | 7.98 ms                                                  | 8.40 ms: 1.05x slower                                     |
| xml_etree_generate   | 64.9 ms                                                  | 69.6 ms: 1.07x slower                                     |
| xml_etree_process    | 46.6 ms                                                  | 50.5 ms: 1.08x slower                                     |
| Geometric mean       | (ref)                                                    | 1.01x slower                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| python_startup_no_site | 9.52 ms                                                  | 9.35 ms: 1.02x faster                                     |
| python_startup         | 13.0 ms                                                  | 12.9 ms: 1.01x faster                                     |
| Geometric mean         | (ref)                                                    | 1.01x faster                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| mako            | 10.7 ms                                                  | 10.9 ms: 1.02x slower                                     |
| genshi_xml      | 41.7 ms                                                  | 42.7 ms: 1.03x slower                                     |
| genshi_text     | 18.7 ms                                                  | 19.4 ms: 1.04x slower                                     |
| django_template | 30.8 ms                                                  | 32.0 ms: 1.04x slower                                     |
| Geometric mean  | (ref)                                                    | 1.03x slower                                              |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc10 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| xml_etree_iterparse             | 64.7 ms                                                  | 58.2 ms: 1.11x faster                                     |
| pathlib                         | 13.1 ms                                                  | 12.3 ms: 1.07x faster                                     |
| create_gc_cycles                | 1.16 ms                                                  | 1.10 ms: 1.06x faster                                     |
| regex_v8                        | 14.9 ms                                                  | 14.2 ms: 1.05x faster                                     |
| tomli_loads                     | 1.53 sec                                                 | 1.46 sec: 1.05x faster                                    |
| dulwich_log                     | 45.2 ms                                                  | 43.8 ms: 1.03x faster                                     |
| pickle_pure_python              | 243 us                                                   | 236 us: 1.03x faster                                      |
| regex_dna                       | 158 ms                                                   | 154 ms: 1.03x faster                                      |
| gc_traversal                    | 1.48 ms                                                  | 1.44 ms: 1.03x faster                                     |
| subparsers                      | 18.4 ms                                                  | 18.0 ms: 1.02x faster                                     |
| sqlalchemy_imperative           | 16.2 ms                                                  | 15.8 ms: 1.02x faster                                     |
| raytrace                        | 217 ms                                                   | 212 ms: 1.02x faster                                      |
| sympy_integrate                 | 16.6 ms                                                  | 16.3 ms: 1.02x faster                                     |
| pyflate                         | 339 ms                                                   | 333 ms: 1.02x faster                                      |
| python_startup_no_site          | 9.52 ms                                                  | 9.35 ms: 1.02x faster                                     |
| hexiom                          | 4.64 ms                                                  | 4.56 ms: 1.02x faster                                     |
| deltablue                       | 2.50 ms                                                  | 2.46 ms: 1.02x faster                                     |
| sympy_sum                       | 112 ms                                                   | 110 ms: 1.01x faster                                      |
| nqueens                         | 61.6 ms                                                  | 60.9 ms: 1.01x faster                                     |
| coverage                        | 78.4 ms                                                  | 77.5 ms: 1.01x faster                                     |
| python_startup                  | 13.0 ms                                                  | 12.9 ms: 1.01x faster                                     |
| pprint_pformat                  | 1.12 sec                                                 | 1.11 sec: 1.01x faster                                    |
| sympy_str                       | 211 ms                                                   | 210 ms: 1.01x faster                                      |
| many_optionals                  | 751 us                                                   | 747 us: 1.00x faster                                      |
| sqlglot_v2_transpile            | 1.26 ms                                                  | 1.25 ms: 1.00x faster                                     |
| html5lib                        | 47.1 ms                                                  | 46.9 ms: 1.00x faster                                     |
| 2to3                            | 207 ms                                                   | 206 ms: 1.00x faster                                      |
| pprint_safe_repr                | 530 ms                                                   | 532 ms: 1.00x slower                                      |
| sympy_expand                    | 360 ms                                                   | 362 ms: 1.00x slower                                      |
| async_tree_eager                | 94.7 ms                                                  | 95.7 ms: 1.01x slower                                     |
| async_tree_none                 | 205 ms                                                   | 207 ms: 1.01x slower                                      |
| richards                        | 36.1 ms                                                  | 36.6 ms: 1.01x slower                                     |
| shortest_path                   | 507 ms                                                   | 514 ms: 1.01x slower                                      |
| connected_components            | 486 ms                                                   | 494 ms: 1.02x slower                                      |
| regex_compile                   | 102 ms                                                   | 103 ms: 1.02x slower                                      |
| typing_runtime_protocols        | 132 us                                                   | 135 us: 1.02x slower                                      |
| mako                            | 10.7 ms                                                  | 10.9 ms: 1.02x slower                                     |
| telco                           | 6.04 ms                                                  | 6.17 ms: 1.02x slower                                     |
| async_tree_eager_memoization_tg | 211 ms                                                   | 216 ms: 1.02x slower                                      |
| bpe_tokeniser                   | 3.13 sec                                                 | 3.20 sec: 1.02x slower                                    |
| genshi_xml                      | 41.7 ms                                                  | 42.7 ms: 1.03x slower                                     |
| unpickle_pure_python            | 155 us                                                   | 159 us: 1.03x slower                                      |
| crypto_pyaes                    | 59.5 ms                                                  | 61.1 ms: 1.03x slower                                     |
| sqlglot_v2_optimize             | 39.7 ms                                                  | 40.8 ms: 1.03x slower                                     |
| async_tree_memoization          | 254 ms                                                   | 261 ms: 1.03x slower                                      |
| meteor_contest                  | 97.9 ms                                                  | 101 ms: 1.03x slower                                      |
| mdp                             | 925 ms                                                   | 956 ms: 1.03x slower                                      |
| xml_etree_parse                 | 94.4 ms                                                  | 97.6 ms: 1.03x slower                                     |
| sphinx                          | 788 ms                                                   | 817 ms: 1.04x slower                                      |
| genshi_text                     | 18.7 ms                                                  | 19.4 ms: 1.04x slower                                     |
| django_template                 | 30.8 ms                                                  | 32.0 ms: 1.04x slower                                     |
| deepcopy                        | 211 us                                                   | 220 us: 1.04x slower                                      |
| async_tree_memoization_tg       | 227 ms                                                   | 236 ms: 1.04x slower                                      |
| sqlglot_v2_normalize            | 80.1 ms                                                  | 83.4 ms: 1.04x slower                                     |
| sqlite_synth                    | 1.47 us                                                  | 1.53 us: 1.04x slower                                     |
| async_tree_none_tg              | 169 ms                                                   | 177 ms: 1.05x slower                                      |
| json_loads                      | 19.5 us                                                  | 20.4 us: 1.05x slower                                     |
| json_dumps                      | 7.98 ms                                                  | 8.40 ms: 1.05x slower                                     |
| comprehensions                  | 11.9 us                                                  | 12.6 us: 1.05x slower                                     |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 322 ms: 1.06x slower                                      |
| docutils                        | 2.02 sec                                                 | 2.13 sec: 1.06x slower                                    |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 396 ms: 1.06x slower                                      |
| deepcopy_memo                   | 21.4 us                                                  | 22.7 us: 1.06x slower                                     |
| async_generators                | 238 ms                                                   | 253 ms: 1.07x slower                                      |
| deepcopy_reduce                 | 2.23 us                                                  | 2.39 us: 1.07x slower                                     |
| xml_etree_generate              | 64.9 ms                                                  | 69.6 ms: 1.07x slower                                     |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 371 ms: 1.07x slower                                      |
| xml_etree_process               | 46.6 ms                                                  | 50.5 ms: 1.08x slower                                     |
| json                            | 3.48 ms                                                  | 3.79 ms: 1.09x slower                                     |
| Geometric mean                  | (ref)                                                    | 1.01x slower                                              |

Benchmark hidden because not significant (5): coroutines, float, pidigits, sqlglot_v2_parse, sqlalchemy_declarative

- Geometric mean (including insignificant results): 1.011x slower

# HPT report

- Reliability score: 99.41% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x
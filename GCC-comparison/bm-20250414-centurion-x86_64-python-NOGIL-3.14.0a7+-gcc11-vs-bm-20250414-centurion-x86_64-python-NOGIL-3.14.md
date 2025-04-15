# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.002x slower
- HPT reliability: 98.41%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| docutils       | 2.02 sec                                                 | 2.04 sec: 1.01x slower                                    |
| html5lib       | 47.1 ms                                                  | 47.3 ms: 1.00x slower                                     |
| sphinx         | 788 ms                                                   | 796 ms: 1.01x slower                                      |
| Geometric mean | (ref)                                                    | 1.01x slower                                              |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 305 ms: 1.00x slower                                      |
| async_tree_memoization_tg       | 227 ms                                                   | 229 ms: 1.01x slower                                      |
| async_tree_eager_memoization_tg | 211 ms                                                   | 213 ms: 1.01x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 171 ms: 1.01x slower                                      |
| async_tree_eager                | 94.7 ms                                                  | 95.7 ms: 1.01x slower                                     |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 378 ms: 1.01x slower                                      |
| coroutines                      | 14.4 ms                                                  | 14.6 ms: 1.02x slower                                     |
| async_tree_memoization          | 254 ms                                                   | 258 ms: 1.02x slower                                      |
| Geometric mean                  | (ref)                                                    | 1.01x slower                                              |

Benchmark hidden because not significant (3): async_generators, async_tree_none, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| pidigits       | 181 ms                                                   | 184 ms: 1.02x slower                                      |
| float          | 46.5 ms                                                  | 48.6 ms: 1.05x slower                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| regex_v8       | 14.9 ms                                                  | 14.2 ms: 1.05x faster                                     |
| regex_dna      | 158 ms                                                   | 152 ms: 1.04x faster                                      |
| regex_compile  | 102 ms                                                   | 104 ms: 1.02x slower                                      |
| Geometric mean | (ref)                                                    | 1.03x faster                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| xml_etree_iterparse  | 64.7 ms                                                  | 56.8 ms: 1.14x faster                                     |
| xml_etree_parse      | 94.4 ms                                                  | 90.0 ms: 1.05x faster                                     |
| tomli_loads          | 1.53 sec                                                 | 1.49 sec: 1.02x faster                                    |
| pickle_pure_python   | 243 us                                                   | 240 us: 1.01x faster                                      |
| unpickle_pure_python | 155 us                                                   | 154 us: 1.01x faster                                      |
| xml_etree_generate   | 64.9 ms                                                  | 65.7 ms: 1.01x slower                                     |
| json_loads           | 19.5 us                                                  | 19.7 us: 1.01x slower                                     |
| json_dumps           | 7.98 ms                                                  | 8.13 ms: 1.02x slower                                     |
| xml_etree_process    | 46.6 ms                                                  | 47.9 ms: 1.03x slower                                     |
| Geometric mean       | (ref)                                                    | 1.02x faster                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| python_startup_no_site | 9.52 ms                                                  | 9.35 ms: 1.02x faster                                     |
| python_startup         | 13.0 ms                                                  | 12.8 ms: 1.02x faster                                     |
| Geometric mean         | (ref)                                                    | 1.02x faster                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| genshi_xml     | 41.7 ms                                                  | 41.8 ms: 1.00x slower                                     |
| mako           | 10.7 ms                                                  | 10.9 ms: 1.02x slower                                     |
| genshi_text    | 18.7 ms                                                  | 19.2 ms: 1.03x slower                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                              |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc11 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| xml_etree_iterparse             | 64.7 ms                                                  | 56.8 ms: 1.14x faster                                     |
| gc_traversal                    | 1.48 ms                                                  | 1.32 ms: 1.12x faster                                     |
| pathlib                         | 13.1 ms                                                  | 11.9 ms: 1.10x faster                                     |
| regex_v8                        | 14.9 ms                                                  | 14.2 ms: 1.05x faster                                     |
| xml_etree_parse                 | 94.4 ms                                                  | 90.0 ms: 1.05x faster                                     |
| regex_dna                       | 158 ms                                                   | 152 ms: 1.04x faster                                      |
| hexiom                          | 4.64 ms                                                  | 4.46 ms: 1.04x faster                                     |
| pyflate                         | 339 ms                                                   | 326 ms: 1.04x faster                                      |
| raytrace                        | 217 ms                                                   | 209 ms: 1.04x faster                                      |
| subparsers                      | 18.4 ms                                                  | 18.0 ms: 1.02x faster                                     |
| tomli_loads                     | 1.53 sec                                                 | 1.49 sec: 1.02x faster                                    |
| nqueens                         | 61.6 ms                                                  | 60.5 ms: 1.02x faster                                     |
| bpe_tokeniser                   | 3.13 sec                                                 | 3.07 sec: 1.02x faster                                    |
| python_startup_no_site          | 9.52 ms                                                  | 9.35 ms: 1.02x faster                                     |
| python_startup                  | 13.0 ms                                                  | 12.8 ms: 1.02x faster                                     |
| sqlalchemy_imperative           | 16.2 ms                                                  | 15.9 ms: 1.02x faster                                     |
| coverage                        | 78.4 ms                                                  | 77.1 ms: 1.02x faster                                     |
| pickle_pure_python              | 243 us                                                   | 240 us: 1.01x faster                                      |
| many_optionals                  | 751 us                                                   | 742 us: 1.01x faster                                      |
| dulwich_log                     | 45.2 ms                                                  | 44.7 ms: 1.01x faster                                     |
| create_gc_cycles                | 1.16 ms                                                  | 1.15 ms: 1.01x faster                                     |
| unpickle_pure_python            | 155 us                                                   | 154 us: 1.01x faster                                      |
| deltablue                       | 2.50 ms                                                  | 2.49 ms: 1.01x faster                                     |
| sympy_integrate                 | 16.6 ms                                                  | 16.5 ms: 1.00x faster                                     |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 305 ms: 1.00x slower                                      |
| html5lib                        | 47.1 ms                                                  | 47.3 ms: 1.00x slower                                     |
| genshi_xml                      | 41.7 ms                                                  | 41.8 ms: 1.00x slower                                     |
| meteor_contest                  | 97.9 ms                                                  | 98.4 ms: 1.01x slower                                     |
| async_tree_memoization_tg       | 227 ms                                                   | 229 ms: 1.01x slower                                      |
| async_tree_eager_memoization_tg | 211 ms                                                   | 213 ms: 1.01x slower                                      |
| sphinx                          | 788 ms                                                   | 796 ms: 1.01x slower                                      |
| sympy_str                       | 211 ms                                                   | 213 ms: 1.01x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 171 ms: 1.01x slower                                      |
| async_tree_eager                | 94.7 ms                                                  | 95.7 ms: 1.01x slower                                     |
| docutils                        | 2.02 sec                                                 | 2.04 sec: 1.01x slower                                    |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 378 ms: 1.01x slower                                      |
| xml_etree_generate              | 64.9 ms                                                  | 65.7 ms: 1.01x slower                                     |
| json_loads                      | 19.5 us                                                  | 19.7 us: 1.01x slower                                     |
| sqlglot_v2_parse                | 1.03 ms                                                  | 1.04 ms: 1.01x slower                                     |
| sympy_sum                       | 112 ms                                                   | 113 ms: 1.01x slower                                      |
| pprint_pformat                  | 1.12 sec                                                 | 1.13 sec: 1.02x slower                                    |
| crypto_pyaes                    | 59.5 ms                                                  | 60.5 ms: 1.02x slower                                     |
| coroutines                      | 14.4 ms                                                  | 14.6 ms: 1.02x slower                                     |
| pidigits                        | 181 ms                                                   | 184 ms: 1.02x slower                                      |
| async_tree_memoization          | 254 ms                                                   | 258 ms: 1.02x slower                                      |
| regex_compile                   | 102 ms                                                   | 104 ms: 1.02x slower                                      |
| json_dumps                      | 7.98 ms                                                  | 8.13 ms: 1.02x slower                                     |
| pprint_safe_repr                | 530 ms                                                   | 542 ms: 1.02x slower                                      |
| mako                            | 10.7 ms                                                  | 10.9 ms: 1.02x slower                                     |
| sympy_expand                    | 360 ms                                                   | 369 ms: 1.02x slower                                      |
| genshi_text                     | 18.7 ms                                                  | 19.2 ms: 1.03x slower                                     |
| json                            | 3.48 ms                                                  | 3.58 ms: 1.03x slower                                     |
| xml_etree_process               | 46.6 ms                                                  | 47.9 ms: 1.03x slower                                     |
| sqlglot_v2_normalize            | 80.1 ms                                                  | 82.4 ms: 1.03x slower                                     |
| sqlglot_v2_optimize             | 39.7 ms                                                  | 40.9 ms: 1.03x slower                                     |
| sqlglot_v2_transpile            | 1.26 ms                                                  | 1.30 ms: 1.03x slower                                     |
| comprehensions                  | 11.9 us                                                  | 12.4 us: 1.04x slower                                     |
| mdp                             | 925 ms                                                   | 957 ms: 1.04x slower                                      |
| shortest_path                   | 507 ms                                                   | 526 ms: 1.04x slower                                      |
| telco                           | 6.04 ms                                                  | 6.27 ms: 1.04x slower                                     |
| connected_components            | 486 ms                                                   | 505 ms: 1.04x slower                                      |
| deepcopy_memo                   | 21.4 us                                                  | 22.3 us: 1.04x slower                                     |
| float                           | 46.5 ms                                                  | 48.6 ms: 1.05x slower                                     |
| deepcopy                        | 211 us                                                   | 222 us: 1.05x slower                                      |
| deepcopy_reduce                 | 2.23 us                                                  | 2.35 us: 1.05x slower                                     |
| richards                        | 36.1 ms                                                  | 38.2 ms: 1.06x slower                                     |
| sqlite_synth                    | 1.47 us                                                  | 1.56 us: 1.06x slower                                     |
| Geometric mean                  | (ref)                                                    | 1.00x slower                                              |

Benchmark hidden because not significant (7): async_generators, django_template, async_tree_none, sqlalchemy_declarative, typing_runtime_protocols, 2to3, async_tree_cpu_io_mixed_tg

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 98.41% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x
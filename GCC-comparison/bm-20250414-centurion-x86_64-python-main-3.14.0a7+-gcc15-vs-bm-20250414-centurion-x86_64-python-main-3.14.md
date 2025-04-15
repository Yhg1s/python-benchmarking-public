# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.010x faster
- HPT reliability: 98.76%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 194 ms                                                  | 193 ms: 1.01x faster                                     |
| docutils       | 1.95 sec                                                | 1.99 sec: 1.02x slower                                   |
| html5lib       | 46.6 ms                                                 | 45.1 ms: 1.03x faster                                    |
| Geometric mean | (ref)                                                   | 1.01x faster                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15 |
|---------------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager                | 81.0 ms                                                 | 77.3 ms: 1.05x faster                                    |
| async_tree_none_tg              | 220 ms                                                  | 214 ms: 1.03x faster                                     |
| async_tree_memoization          | 270 ms                                                  | 263 ms: 1.03x faster                                     |
| async_tree_memoization_tg       | 276 ms                                                  | 270 ms: 1.02x faster                                     |
| async_tree_eager_memoization_tg | 236 ms                                                  | 231 ms: 1.02x faster                                     |
| async_tree_none                 | 232 ms                                                  | 228 ms: 1.02x faster                                     |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                  | 414 ms: 1.05x slower                                     |
| async_tree_cpu_io_mixed         | 395 ms                                                  | 416 ms: 1.05x slower                                     |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                  | 321 ms: 1.07x slower                                     |
| async_generators                | 215 ms                                                  | 231 ms: 1.08x slower                                     |
| Geometric mean                  | (ref)                                                   | 1.01x slower                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 46.7 ms                                                 | 45.7 ms: 1.02x faster                                    |
| pidigits       | 184 ms                                                  | 181 ms: 1.02x faster                                     |
| Geometric mean | (ref)                                                   | 1.02x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 156 ms                                                  | 143 ms: 1.09x faster                                     |
| regex_v8       | 15.2 ms                                                 | 14.4 ms: 1.05x faster                                    |
| regex_compile  | 90.1 ms                                                 | 89.1 ms: 1.01x faster                                    |
| Geometric mean | (ref)                                                   | 1.05x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15 |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse  | 77.8 ms                                                 | 67.3 ms: 1.16x faster                                    |
| tomli_loads          | 1.40 sec                                                | 1.34 sec: 1.05x faster                                   |
| unpickle_pure_python | 155 us                                                  | 158 us: 1.02x slower                                     |
| json_loads           | 17.4 us                                                 | 17.9 us: 1.02x slower                                    |
| xml_etree_generate   | 62.2 ms                                                 | 65.2 ms: 1.05x slower                                    |
| xml_etree_process    | 44.9 ms                                                 | 47.4 ms: 1.06x slower                                    |
| json_dumps           | 7.27 ms                                                 | 7.71 ms: 1.06x slower                                    |
| xml_etree_parse      | 92.9 ms                                                 | 99.5 ms: 1.07x slower                                    |
| Geometric mean       | (ref)                                                   | 1.01x slower                                             |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15 |
|------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 10.9 ms                                                 | 10.7 ms: 1.01x faster                                    |
| python_startup_no_site | 7.53 ms                                                 | 7.47 ms: 1.01x faster                                    |
| Geometric mean         | (ref)                                                   | 1.01x faster                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml     | 39.4 ms                                                 | 37.8 ms: 1.04x faster                                    |
| mako           | 7.37 ms                                                 | 7.19 ms: 1.03x faster                                    |
| genshi_text    | 16.0 ms                                                 | 15.7 ms: 1.02x faster                                    |
| Geometric mean | (ref)                                                   | 1.02x faster                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc15 |
|---------------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse             | 77.8 ms                                                 | 67.3 ms: 1.16x faster                                    |
| deltablue                       | 2.65 ms                                                 | 2.31 ms: 1.15x faster                                    |
| regex_dna                       | 156 ms                                                  | 143 ms: 1.09x faster                                     |
| sqlglot_v2_normalize            | 78.5 ms                                                 | 74.0 ms: 1.06x faster                                    |
| pyflate                         | 310 ms                                                  | 293 ms: 1.06x faster                                     |
| crypto_pyaes                    | 52.7 ms                                                 | 49.8 ms: 1.06x faster                                    |
| pathlib                         | 13.0 ms                                                 | 12.3 ms: 1.05x faster                                    |
| hexiom                          | 4.08 ms                                                 | 3.87 ms: 1.05x faster                                    |
| regex_v8                        | 15.2 ms                                                 | 14.4 ms: 1.05x faster                                    |
| async_tree_eager                | 81.0 ms                                                 | 77.3 ms: 1.05x faster                                    |
| sympy_integrate                 | 15.2 ms                                                 | 14.5 ms: 1.05x faster                                    |
| tomli_loads                     | 1.40 sec                                                | 1.34 sec: 1.05x faster                                   |
| genshi_xml                      | 39.4 ms                                                 | 37.8 ms: 1.04x faster                                    |
| typing_runtime_protocols        | 107 us                                                  | 102 us: 1.04x faster                                     |
| mdp                             | 945 ms                                                  | 908 ms: 1.04x faster                                     |
| subparsers                      | 17.6 ms                                                 | 17.0 ms: 1.03x faster                                    |
| html5lib                        | 46.6 ms                                                 | 45.1 ms: 1.03x faster                                    |
| sympy_sum                       | 105 ms                                                  | 102 ms: 1.03x faster                                     |
| sympy_str                       | 192 ms                                                  | 187 ms: 1.03x faster                                     |
| async_tree_none_tg              | 220 ms                                                  | 214 ms: 1.03x faster                                     |
| async_tree_memoization          | 270 ms                                                  | 263 ms: 1.03x faster                                     |
| mako                            | 7.37 ms                                                 | 7.19 ms: 1.03x faster                                    |
| async_tree_memoization_tg       | 276 ms                                                  | 270 ms: 1.02x faster                                     |
| sqlalchemy_imperative           | 14.1 ms                                                 | 13.8 ms: 1.02x faster                                    |
| float                           | 46.7 ms                                                 | 45.7 ms: 1.02x faster                                    |
| sqlglot_v2_parse                | 894 us                                                  | 877 us: 1.02x faster                                     |
| async_tree_eager_memoization_tg | 236 ms                                                  | 231 ms: 1.02x faster                                     |
| deepcopy_reduce                 | 1.98 us                                                 | 1.94 us: 1.02x faster                                    |
| pidigits                        | 184 ms                                                  | 181 ms: 1.02x faster                                     |
| deepcopy_memo                   | 18.0 us                                                 | 17.7 us: 1.02x faster                                    |
| sqlglot_v2_optimize             | 38.6 ms                                                 | 37.9 ms: 1.02x faster                                    |
| async_tree_none                 | 232 ms                                                  | 228 ms: 1.02x faster                                     |
| genshi_text                     | 16.0 ms                                                 | 15.7 ms: 1.02x faster                                    |
| sympy_expand                    | 327 ms                                                  | 323 ms: 1.01x faster                                     |
| richards                        | 31.0 ms                                                 | 30.5 ms: 1.01x faster                                    |
| python_startup                  | 10.9 ms                                                 | 10.7 ms: 1.01x faster                                    |
| regex_compile                   | 90.1 ms                                                 | 89.1 ms: 1.01x faster                                    |
| create_gc_cycles                | 1.77 ms                                                 | 1.75 ms: 1.01x faster                                    |
| sqlglot_v2_transpile            | 1.14 ms                                                 | 1.13 ms: 1.01x faster                                    |
| 2to3                            | 194 ms                                                  | 193 ms: 1.01x faster                                     |
| dulwich_log                     | 42.7 ms                                                 | 42.3 ms: 1.01x faster                                    |
| python_startup_no_site          | 7.53 ms                                                 | 7.47 ms: 1.01x faster                                    |
| many_optionals                  | 731 us                                                  | 726 us: 1.01x faster                                     |
| bpe_tokeniser                   | 3.11 sec                                                | 3.09 sec: 1.00x faster                                   |
| raytrace                        | 186 ms                                                  | 185 ms: 1.00x faster                                     |
| sqlalchemy_declarative          | 96.2 ms                                                 | 95.8 ms: 1.00x faster                                    |
| meteor_contest                  | 84.6 ms                                                 | 84.3 ms: 1.00x faster                                    |
| telco                           | 5.15 ms                                                 | 5.21 ms: 1.01x slower                                    |
| pprint_safe_repr                | 464 ms                                                  | 470 ms: 1.01x slower                                     |
| unpickle_pure_python            | 155 us                                                  | 158 us: 1.02x slower                                     |
| connected_components            | 433 ms                                                  | 441 ms: 1.02x slower                                     |
| docutils                        | 1.95 sec                                                | 1.99 sec: 1.02x slower                                   |
| nqueens                         | 54.0 ms                                                 | 55.2 ms: 1.02x slower                                    |
| json_loads                      | 17.4 us                                                 | 17.9 us: 1.02x slower                                    |
| pprint_pformat                  | 943 ms                                                  | 967 ms: 1.03x slower                                     |
| comprehensions                  | 10.8 us                                                 | 11.1 us: 1.03x slower                                    |
| gc_traversal                    | 3.06 ms                                                 | 3.15 ms: 1.03x slower                                    |
| sqlite_synth                    | 1.56 us                                                 | 1.64 us: 1.05x slower                                    |
| xml_etree_generate              | 62.2 ms                                                 | 65.2 ms: 1.05x slower                                    |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                  | 414 ms: 1.05x slower                                     |
| async_tree_cpu_io_mixed         | 395 ms                                                  | 416 ms: 1.05x slower                                     |
| xml_etree_process               | 44.9 ms                                                 | 47.4 ms: 1.06x slower                                    |
| json_dumps                      | 7.27 ms                                                 | 7.71 ms: 1.06x slower                                    |
| json                            | 3.35 ms                                                 | 3.56 ms: 1.06x slower                                    |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                  | 321 ms: 1.07x slower                                     |
| xml_etree_parse                 | 92.9 ms                                                 | 99.5 ms: 1.07x slower                                    |
| async_generators                | 215 ms                                                  | 231 ms: 1.08x slower                                     |
| Geometric mean                  | (ref)                                                   | 1.01x faster                                             |

Benchmark hidden because not significant (7): coroutines, sphinx, pickle_pure_python, deepcopy, django_template, shortest_path, coverage

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 98.76% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x
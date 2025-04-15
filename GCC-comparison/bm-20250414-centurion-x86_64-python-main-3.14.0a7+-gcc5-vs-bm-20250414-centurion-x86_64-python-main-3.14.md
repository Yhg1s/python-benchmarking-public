# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.022x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5 |
|----------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| 2to3           | 194 ms                                                  | 197 ms: 1.01x slower                                    |
| docutils       | 1.95 sec                                                | 1.94 sec: 1.01x faster                                  |
| html5lib       | 46.6 ms                                                 | 45.9 ms: 1.02x faster                                   |
| Geometric mean | (ref)                                                   | 1.00x faster                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5 |
|---------------------------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| async_tree_none_tg              | 220 ms                                                  | 223 ms: 1.01x slower                                    |
| async_generators                | 215 ms                                                  | 218 ms: 1.02x slower                                    |
| async_tree_memoization_tg       | 276 ms                                                  | 280 ms: 1.02x slower                                    |
| async_tree_memoization          | 270 ms                                                  | 277 ms: 1.02x slower                                    |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                  | 405 ms: 1.03x slower                                    |
| async_tree_none                 | 232 ms                                                  | 238 ms: 1.03x slower                                    |
| async_tree_cpu_io_mixed         | 395 ms                                                  | 409 ms: 1.03x slower                                    |
| async_tree_eager_memoization_tg | 236 ms                                                  | 245 ms: 1.04x slower                                    |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                  | 313 ms: 1.04x slower                                    |
| coroutines                      | 14.5 ms                                                 | 15.2 ms: 1.05x slower                                   |
| async_tree_eager                | 81.0 ms                                                 | 86.6 ms: 1.07x slower                                   |
| Geometric mean                  | (ref)                                                   | 1.03x slower                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5 |
|----------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| float          | 46.7 ms                                                 | 47.4 ms: 1.02x slower                                   |
| pidigits       | 184 ms                                                  | 189 ms: 1.02x slower                                    |
| Geometric mean | (ref)                                                   | 1.02x slower                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5 |
|----------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| regex_dna      | 156 ms                                                  | 143 ms: 1.09x faster                                    |
| regex_v8       | 15.2 ms                                                 | 14.9 ms: 1.02x faster                                   |
| regex_compile  | 90.1 ms                                                 | 93.3 ms: 1.04x slower                                   |
| Geometric mean | (ref)                                                   | 1.03x faster                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5 |
|----------------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| xml_etree_iterparse  | 77.8 ms                                                 | 75.1 ms: 1.04x faster                                   |
| xml_etree_parse      | 92.9 ms                                                 | 90.5 ms: 1.03x faster                                   |
| unpickle_pure_python | 155 us                                                  | 158 us: 1.01x slower                                    |
| xml_etree_process    | 44.9 ms                                                 | 45.9 ms: 1.02x slower                                   |
| pickle_pure_python   | 224 us                                                  | 232 us: 1.04x slower                                    |
| xml_etree_generate   | 62.2 ms                                                 | 64.9 ms: 1.04x slower                                   |
| json_dumps           | 7.27 ms                                                 | 8.13 ms: 1.12x slower                                   |
| json_loads           | 17.4 us                                                 | 24.2 us: 1.39x slower                                   |
| Geometric mean       | (ref)                                                   | 1.06x slower                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5 |
|------------------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| python_startup_no_site | 7.53 ms                                                 | 7.47 ms: 1.01x faster                                   |
| python_startup         | 10.9 ms                                                 | 10.8 ms: 1.01x faster                                   |
| Geometric mean         | (ref)                                                   | 1.01x faster                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5 |
|-----------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| django_template | 27.9 ms                                                 | 28.0 ms: 1.00x slower                                   |
| genshi_text     | 16.0 ms                                                 | 16.3 ms: 1.02x slower                                   |
| mako            | 7.37 ms                                                 | 7.79 ms: 1.06x slower                                   |
| Geometric mean  | (ref)                                                   | 1.02x slower                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc5 |
|---------------------------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| deltablue                       | 2.65 ms                                                 | 2.21 ms: 1.20x faster                                   |
| regex_dna                       | 156 ms                                                  | 143 ms: 1.09x faster                                    |
| xml_etree_iterparse             | 77.8 ms                                                 | 75.1 ms: 1.04x faster                                   |
| sympy_integrate                 | 15.2 ms                                                 | 14.8 ms: 1.03x faster                                   |
| xml_etree_parse                 | 92.9 ms                                                 | 90.5 ms: 1.03x faster                                   |
| regex_v8                        | 15.2 ms                                                 | 14.9 ms: 1.02x faster                                   |
| html5lib                        | 46.6 ms                                                 | 45.9 ms: 1.02x faster                                   |
| bpe_tokeniser                   | 3.11 sec                                                | 3.06 sec: 1.02x faster                                  |
| comprehensions                  | 10.8 us                                                 | 10.6 us: 1.01x faster                                   |
| sympy_sum                       | 105 ms                                                  | 104 ms: 1.01x faster                                    |
| raytrace                        | 186 ms                                                  | 184 ms: 1.01x faster                                    |
| sqlglot_v2_normalize            | 78.5 ms                                                 | 77.8 ms: 1.01x faster                                   |
| hexiom                          | 4.08 ms                                                 | 4.04 ms: 1.01x faster                                   |
| sqlglot_v2_optimize             | 38.6 ms                                                 | 38.3 ms: 1.01x faster                                   |
| python_startup_no_site          | 7.53 ms                                                 | 7.47 ms: 1.01x faster                                   |
| mdp                             | 945 ms                                                  | 939 ms: 1.01x faster                                    |
| docutils                        | 1.95 sec                                                | 1.94 sec: 1.01x faster                                  |
| python_startup                  | 10.9 ms                                                 | 10.8 ms: 1.01x faster                                   |
| sqlalchemy_declarative          | 96.2 ms                                                 | 95.8 ms: 1.00x faster                                   |
| django_template                 | 27.9 ms                                                 | 28.0 ms: 1.00x slower                                   |
| many_optionals                  | 731 us                                                  | 733 us: 1.00x slower                                    |
| sqlalchemy_imperative           | 14.1 ms                                                 | 14.2 ms: 1.01x slower                                   |
| dulwich_log                     | 42.7 ms                                                 | 42.9 ms: 1.01x slower                                   |
| pyflate                         | 310 ms                                                  | 313 ms: 1.01x slower                                    |
| create_gc_cycles                | 1.77 ms                                                 | 1.79 ms: 1.01x slower                                   |
| shortest_path                   | 442 ms                                                  | 447 ms: 1.01x slower                                    |
| async_tree_none_tg              | 220 ms                                                  | 223 ms: 1.01x slower                                    |
| sympy_str                       | 192 ms                                                  | 195 ms: 1.01x slower                                    |
| 2to3                            | 194 ms                                                  | 197 ms: 1.01x slower                                    |
| sqlglot_v2_parse                | 894 us                                                  | 907 us: 1.01x slower                                    |
| unpickle_pure_python            | 155 us                                                  | 158 us: 1.01x slower                                    |
| sqlglot_v2_transpile            | 1.14 ms                                                 | 1.16 ms: 1.01x slower                                   |
| pathlib                         | 13.0 ms                                                 | 13.2 ms: 1.02x slower                                   |
| async_generators                | 215 ms                                                  | 218 ms: 1.02x slower                                    |
| float                           | 46.7 ms                                                 | 47.4 ms: 1.02x slower                                   |
| async_tree_memoization_tg       | 276 ms                                                  | 280 ms: 1.02x slower                                    |
| meteor_contest                  | 84.6 ms                                                 | 86.0 ms: 1.02x slower                                   |
| subparsers                      | 17.6 ms                                                 | 17.9 ms: 1.02x slower                                   |
| connected_components            | 433 ms                                                  | 440 ms: 1.02x slower                                    |
| coverage                        | 54.6 ms                                                 | 55.5 ms: 1.02x slower                                   |
| xml_etree_process               | 44.9 ms                                                 | 45.9 ms: 1.02x slower                                   |
| genshi_text                     | 16.0 ms                                                 | 16.3 ms: 1.02x slower                                   |
| pidigits                        | 184 ms                                                  | 189 ms: 1.02x slower                                    |
| async_tree_memoization          | 270 ms                                                  | 277 ms: 1.02x slower                                    |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                  | 405 ms: 1.03x slower                                    |
| sympy_expand                    | 327 ms                                                  | 336 ms: 1.03x slower                                    |
| typing_runtime_protocols        | 107 us                                                  | 109 us: 1.03x slower                                    |
| async_tree_none                 | 232 ms                                                  | 238 ms: 1.03x slower                                    |
| async_tree_cpu_io_mixed         | 395 ms                                                  | 409 ms: 1.03x slower                                    |
| regex_compile                   | 90.1 ms                                                 | 93.3 ms: 1.04x slower                                   |
| pickle_pure_python              | 224 us                                                  | 232 us: 1.04x slower                                    |
| async_tree_eager_memoization_tg | 236 ms                                                  | 245 ms: 1.04x slower                                    |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                  | 313 ms: 1.04x slower                                    |
| deepcopy_memo                   | 18.0 us                                                 | 18.8 us: 1.04x slower                                   |
| xml_etree_generate              | 62.2 ms                                                 | 64.9 ms: 1.04x slower                                   |
| nqueens                         | 54.0 ms                                                 | 56.5 ms: 1.05x slower                                   |
| coroutines                      | 14.5 ms                                                 | 15.2 ms: 1.05x slower                                   |
| deepcopy                        | 185 us                                                  | 194 us: 1.05x slower                                    |
| mako                            | 7.37 ms                                                 | 7.79 ms: 1.06x slower                                   |
| gc_traversal                    | 3.06 ms                                                 | 3.24 ms: 1.06x slower                                   |
| richards                        | 31.0 ms                                                 | 33.0 ms: 1.07x slower                                   |
| async_tree_eager                | 81.0 ms                                                 | 86.6 ms: 1.07x slower                                   |
| sqlite_synth                    | 1.56 us                                                 | 1.68 us: 1.07x slower                                   |
| pprint_safe_repr                | 464 ms                                                  | 504 ms: 1.09x slower                                    |
| telco                           | 5.15 ms                                                 | 5.60 ms: 1.09x slower                                   |
| crypto_pyaes                    | 52.7 ms                                                 | 57.4 ms: 1.09x slower                                   |
| pprint_pformat                  | 943 ms                                                  | 1.04 sec: 1.11x slower                                  |
| json_dumps                      | 7.27 ms                                                 | 8.13 ms: 1.12x slower                                   |
| json                            | 3.35 ms                                                 | 4.15 ms: 1.24x slower                                   |
| json_loads                      | 17.4 us                                                 | 24.2 us: 1.39x slower                                   |
| Geometric mean                  | (ref)                                                   | 1.02x slower                                            |

Benchmark hidden because not significant (4): genshi_xml, sphinx, deepcopy_reduce, tomli_loads

- Geometric mean (including insignificant results): 1.022x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x
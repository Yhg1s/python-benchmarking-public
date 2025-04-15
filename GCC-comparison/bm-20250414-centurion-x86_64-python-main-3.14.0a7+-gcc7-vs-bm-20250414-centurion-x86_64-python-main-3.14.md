# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.025x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7 |
|----------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| 2to3           | 194 ms                                                  | 198 ms: 1.02x slower                                    |
| docutils       | 1.95 sec                                                | 1.95 sec: 1.00x slower                                  |
| sphinx         | 755 ms                                                  | 765 ms: 1.01x slower                                    |
| Geometric mean | (ref)                                                   | 1.01x slower                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7 |
|---------------------------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| async_tree_none_tg              | 220 ms                                                  | 223 ms: 1.01x slower                                    |
| async_tree_memoization          | 270 ms                                                  | 276 ms: 1.02x slower                                    |
| async_tree_eager_memoization_tg | 236 ms                                                  | 243 ms: 1.03x slower                                    |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                  | 407 ms: 1.03x slower                                    |
| async_tree_none                 | 232 ms                                                  | 239 ms: 1.03x slower                                    |
| async_generators                | 215 ms                                                  | 223 ms: 1.04x slower                                    |
| async_tree_cpu_io_mixed         | 395 ms                                                  | 412 ms: 1.04x slower                                    |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                  | 314 ms: 1.05x slower                                    |
| coroutines                      | 14.5 ms                                                 | 15.3 ms: 1.05x slower                                   |
| async_tree_eager                | 81.0 ms                                                 | 86.0 ms: 1.06x slower                                   |
| Geometric mean                  | (ref)                                                   | 1.04x slower                                            |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7 |
|----------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| pidigits       | 184 ms                                                  | 189 ms: 1.03x slower                                    |
| float          | 46.7 ms                                                 | 48.7 ms: 1.04x slower                                   |
| Geometric mean | (ref)                                                   | 1.03x slower                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7 |
|----------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| regex_dna      | 156 ms                                                  | 134 ms: 1.16x faster                                    |
| regex_v8       | 15.2 ms                                                 | 14.9 ms: 1.02x faster                                   |
| regex_compile  | 90.1 ms                                                 | 93.5 ms: 1.04x slower                                   |
| Geometric mean | (ref)                                                   | 1.05x faster                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7 |
|----------------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| xml_etree_iterparse  | 77.8 ms                                                 | 75.9 ms: 1.02x faster                                   |
| unpickle_pure_python | 155 us                                                  | 158 us: 1.01x slower                                    |
| pickle_pure_python   | 224 us                                                  | 228 us: 1.02x slower                                    |
| xml_etree_parse      | 92.9 ms                                                 | 94.9 ms: 1.02x slower                                   |
| xml_etree_process    | 44.9 ms                                                 | 48.0 ms: 1.07x slower                                   |
| xml_etree_generate   | 62.2 ms                                                 | 66.7 ms: 1.07x slower                                   |
| json_loads           | 17.4 us                                                 | 18.9 us: 1.08x slower                                   |
| json_dumps           | 7.27 ms                                                 | 8.28 ms: 1.14x slower                                   |
| Geometric mean       | (ref)                                                   | 1.04x slower                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7 |
|------------------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| python_startup         | 10.9 ms                                                 | 11.0 ms: 1.01x slower                                   |
| python_startup_no_site | 7.53 ms                                                 | 7.63 ms: 1.01x slower                                   |
| Geometric mean         | (ref)                                                   | 1.01x slower                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7 |
|-----------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| genshi_text     | 16.0 ms                                                 | 16.2 ms: 1.02x slower                                   |
| django_template | 27.9 ms                                                 | 28.6 ms: 1.03x slower                                   |
| genshi_xml      | 39.4 ms                                                 | 40.7 ms: 1.03x slower                                   |
| mako            | 7.37 ms                                                 | 7.99 ms: 1.08x slower                                   |
| Geometric mean  | (ref)                                                   | 1.04x slower                                            |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc7 |
|---------------------------------|:-------------------------------------------------------:|:-------------------------------------------------------:|
| deltablue                       | 2.65 ms                                                 | 2.21 ms: 1.20x faster                                   |
| regex_dna                       | 156 ms                                                  | 134 ms: 1.16x faster                                    |
| xml_etree_iterparse             | 77.8 ms                                                 | 75.9 ms: 1.02x faster                                   |
| regex_v8                        | 15.2 ms                                                 | 14.9 ms: 1.02x faster                                   |
| pyflate                         | 310 ms                                                  | 306 ms: 1.01x faster                                    |
| sympy_integrate                 | 15.2 ms                                                 | 15.0 ms: 1.01x faster                                   |
| meteor_contest                  | 84.6 ms                                                 | 84.8 ms: 1.00x slower                                   |
| sqlglot_v2_normalize            | 78.5 ms                                                 | 78.7 ms: 1.00x slower                                   |
| docutils                        | 1.95 sec                                                | 1.95 sec: 1.00x slower                                  |
| sqlglot_v2_optimize             | 38.6 ms                                                 | 38.7 ms: 1.00x slower                                   |
| deepcopy_memo                   | 18.0 us                                                 | 18.1 us: 1.01x slower                                   |
| connected_components            | 433 ms                                                  | 437 ms: 1.01x slower                                    |
| python_startup                  | 10.9 ms                                                 | 11.0 ms: 1.01x slower                                   |
| sqlalchemy_imperative           | 14.1 ms                                                 | 14.3 ms: 1.01x slower                                   |
| many_optionals                  | 731 us                                                  | 740 us: 1.01x slower                                    |
| python_startup_no_site          | 7.53 ms                                                 | 7.63 ms: 1.01x slower                                   |
| sphinx                          | 755 ms                                                  | 765 ms: 1.01x slower                                    |
| create_gc_cycles                | 1.77 ms                                                 | 1.79 ms: 1.01x slower                                   |
| unpickle_pure_python            | 155 us                                                  | 158 us: 1.01x slower                                    |
| async_tree_none_tg              | 220 ms                                                  | 223 ms: 1.01x slower                                    |
| sqlglot_v2_transpile            | 1.14 ms                                                 | 1.16 ms: 1.02x slower                                   |
| pathlib                         | 13.0 ms                                                 | 13.2 ms: 1.02x slower                                   |
| genshi_text                     | 16.0 ms                                                 | 16.2 ms: 1.02x slower                                   |
| sqlalchemy_declarative          | 96.2 ms                                                 | 97.9 ms: 1.02x slower                                   |
| pickle_pure_python              | 224 us                                                  | 228 us: 1.02x slower                                    |
| 2to3                            | 194 ms                                                  | 198 ms: 1.02x slower                                    |
| bpe_tokeniser                   | 3.11 sec                                                | 3.17 sec: 1.02x slower                                  |
| xml_etree_parse                 | 92.9 ms                                                 | 94.9 ms: 1.02x slower                                   |
| dulwich_log                     | 42.7 ms                                                 | 43.6 ms: 1.02x slower                                   |
| async_tree_memoization          | 270 ms                                                  | 276 ms: 1.02x slower                                    |
| subparsers                      | 17.6 ms                                                 | 18.0 ms: 1.02x slower                                   |
| hexiom                          | 4.08 ms                                                 | 4.17 ms: 1.02x slower                                   |
| pidigits                        | 184 ms                                                  | 189 ms: 1.03x slower                                    |
| raytrace                        | 186 ms                                                  | 191 ms: 1.03x slower                                    |
| django_template                 | 27.9 ms                                                 | 28.6 ms: 1.03x slower                                   |
| sympy_sum                       | 105 ms                                                  | 108 ms: 1.03x slower                                    |
| deepcopy_reduce                 | 1.98 us                                                 | 2.04 us: 1.03x slower                                   |
| sqlglot_v2_parse                | 894 us                                                  | 920 us: 1.03x slower                                    |
| gc_traversal                    | 3.06 ms                                                 | 3.15 ms: 1.03x slower                                   |
| async_tree_eager_memoization_tg | 236 ms                                                  | 243 ms: 1.03x slower                                    |
| coverage                        | 54.6 ms                                                 | 56.3 ms: 1.03x slower                                   |
| mdp                             | 945 ms                                                  | 976 ms: 1.03x slower                                    |
| genshi_xml                      | 39.4 ms                                                 | 40.7 ms: 1.03x slower                                   |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                  | 407 ms: 1.03x slower                                    |
| async_tree_none                 | 232 ms                                                  | 239 ms: 1.03x slower                                    |
| regex_compile                   | 90.1 ms                                                 | 93.5 ms: 1.04x slower                                   |
| async_generators                | 215 ms                                                  | 223 ms: 1.04x slower                                    |
| richards                        | 31.0 ms                                                 | 32.2 ms: 1.04x slower                                   |
| sympy_str                       | 192 ms                                                  | 200 ms: 1.04x slower                                    |
| nqueens                         | 54.0 ms                                                 | 56.3 ms: 1.04x slower                                   |
| async_tree_cpu_io_mixed         | 395 ms                                                  | 412 ms: 1.04x slower                                    |
| float                           | 46.7 ms                                                 | 48.7 ms: 1.04x slower                                   |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                  | 314 ms: 1.05x slower                                    |
| sympy_expand                    | 327 ms                                                  | 343 ms: 1.05x slower                                    |
| coroutines                      | 14.5 ms                                                 | 15.3 ms: 1.05x slower                                   |
| deepcopy                        | 185 us                                                  | 196 us: 1.06x slower                                    |
| async_tree_eager                | 81.0 ms                                                 | 86.0 ms: 1.06x slower                                   |
| json                            | 3.35 ms                                                 | 3.57 ms: 1.06x slower                                   |
| xml_etree_process               | 44.9 ms                                                 | 48.0 ms: 1.07x slower                                   |
| xml_etree_generate              | 62.2 ms                                                 | 66.7 ms: 1.07x slower                                   |
| crypto_pyaes                    | 52.7 ms                                                 | 56.9 ms: 1.08x slower                                   |
| mako                            | 7.37 ms                                                 | 7.99 ms: 1.08x slower                                   |
| json_loads                      | 17.4 us                                                 | 18.9 us: 1.08x slower                                   |
| typing_runtime_protocols        | 107 us                                                  | 116 us: 1.09x slower                                    |
| pprint_safe_repr                | 464 ms                                                  | 506 ms: 1.09x slower                                    |
| pprint_pformat                  | 943 ms                                                  | 1.03 sec: 1.09x slower                                  |
| telco                           | 5.15 ms                                                 | 5.70 ms: 1.11x slower                                   |
| sqlite_synth                    | 1.56 us                                                 | 1.73 us: 1.11x slower                                   |
| json_dumps                      | 7.27 ms                                                 | 8.28 ms: 1.14x slower                                   |
| Geometric mean                  | (ref)                                                   | 1.03x slower                                            |

Benchmark hidden because not significant (5): tomli_loads, html5lib, comprehensions, shortest_path, async_tree_memoization_tg

- Geometric mean (including insignificant results): 1.025x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.00x
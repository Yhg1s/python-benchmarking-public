# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.034x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 194 ms                                                  | 200 ms: 1.03x slower                                     |
| docutils       | 1.95 sec                                                | 2.04 sec: 1.05x slower                                   |
| html5lib       | 46.6 ms                                                 | 46.9 ms: 1.01x slower                                    |
| sphinx         | 755 ms                                                  | 782 ms: 1.04x slower                                     |
| Geometric mean | (ref)                                                   | 1.03x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14 |
|---------------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_memoization_tg       | 276 ms                                                  | 281 ms: 1.02x slower                                     |
| async_tree_none_tg              | 220 ms                                                  | 225 ms: 1.02x slower                                     |
| async_tree_memoization          | 270 ms                                                  | 276 ms: 1.02x slower                                     |
| async_tree_eager_memoization_tg | 236 ms                                                  | 242 ms: 1.03x slower                                     |
| async_tree_none                 | 232 ms                                                  | 238 ms: 1.03x slower                                     |
| async_tree_eager                | 81.0 ms                                                 | 83.6 ms: 1.03x slower                                    |
| coroutines                      | 14.5 ms                                                 | 15.6 ms: 1.07x slower                                    |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                  | 426 ms: 1.08x slower                                     |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                  | 326 ms: 1.09x slower                                     |
| async_tree_cpu_io_mixed         | 395 ms                                                  | 430 ms: 1.09x slower                                     |
| async_generators                | 215 ms                                                  | 246 ms: 1.14x slower                                     |
| Geometric mean                  | (ref)                                                   | 1.06x slower                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 184 ms                                                  | 181 ms: 1.02x faster                                     |
| float          | 46.7 ms                                                 | 49.5 ms: 1.06x slower                                    |
| Geometric mean | (ref)                                                   | 1.02x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 156 ms                                                  | 144 ms: 1.08x faster                                     |
| regex_v8       | 15.2 ms                                                 | 15.0 ms: 1.01x faster                                    |
| regex_compile  | 90.1 ms                                                 | 94.5 ms: 1.05x slower                                    |
| Geometric mean | (ref)                                                   | 1.02x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14 |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| tomli_loads          | 1.40 sec                                                | 1.41 sec: 1.01x slower                                   |
| json_loads           | 17.4 us                                                 | 18.2 us: 1.04x slower                                    |
| unpickle_pure_python | 155 us                                                  | 162 us: 1.05x slower                                     |
| pickle_pure_python   | 224 us                                                  | 236 us: 1.05x slower                                     |
| xml_etree_parse      | 92.9 ms                                                 | 100 ms: 1.08x slower                                     |
| json_dumps           | 7.27 ms                                                 | 7.86 ms: 1.08x slower                                    |
| xml_etree_process    | 44.9 ms                                                 | 50.7 ms: 1.13x slower                                    |
| xml_etree_generate   | 62.2 ms                                                 | 70.3 ms: 1.13x slower                                    |
| Geometric mean       | (ref)                                                   | 1.06x slower                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14 |
|------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 7.53 ms                                                 | 7.47 ms: 1.01x faster                                    |
| python_startup         | 10.9 ms                                                 | 10.8 ms: 1.01x faster                                    |
| Geometric mean         | (ref)                                                   | 1.01x faster                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14 |
|-----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 39.4 ms                                                 | 40.6 ms: 1.03x slower                                    |
| mako            | 7.37 ms                                                 | 7.60 ms: 1.03x slower                                    |
| django_template | 27.9 ms                                                 | 29.7 ms: 1.06x slower                                    |
| genshi_text     | 16.0 ms                                                 | 17.3 ms: 1.09x slower                                    |
| Geometric mean  | (ref)                                                   | 1.05x slower                                             |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc14 |
|---------------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| deltablue                       | 2.65 ms                                                 | 2.34 ms: 1.13x faster                                    |
| regex_dna                       | 156 ms                                                  | 144 ms: 1.08x faster                                     |
| create_gc_cycles                | 1.77 ms                                                 | 1.74 ms: 1.02x faster                                    |
| pathlib                         | 13.0 ms                                                 | 12.8 ms: 1.02x faster                                    |
| pidigits                        | 184 ms                                                  | 181 ms: 1.02x faster                                     |
| subparsers                      | 17.6 ms                                                 | 17.3 ms: 1.02x faster                                    |
| regex_v8                        | 15.2 ms                                                 | 15.0 ms: 1.01x faster                                    |
| python_startup_no_site          | 7.53 ms                                                 | 7.47 ms: 1.01x faster                                    |
| python_startup                  | 10.9 ms                                                 | 10.8 ms: 1.01x faster                                    |
| sympy_integrate                 | 15.2 ms                                                 | 15.1 ms: 1.01x faster                                    |
| connected_components            | 433 ms                                                  | 435 ms: 1.00x slower                                     |
| html5lib                        | 46.6 ms                                                 | 46.9 ms: 1.01x slower                                    |
| mdp                             | 945 ms                                                  | 952 ms: 1.01x slower                                     |
| tomli_loads                     | 1.40 sec                                                | 1.41 sec: 1.01x slower                                   |
| typing_runtime_protocols        | 107 us                                                  | 107 us: 1.01x slower                                     |
| shortest_path                   | 442 ms                                                  | 447 ms: 1.01x slower                                     |
| sympy_str                       | 192 ms                                                  | 195 ms: 1.01x slower                                     |
| coverage                        | 54.6 ms                                                 | 55.3 ms: 1.01x slower                                    |
| sympy_sum                       | 105 ms                                                  | 107 ms: 1.02x slower                                     |
| sympy_expand                    | 327 ms                                                  | 333 ms: 1.02x slower                                     |
| sqlglot_v2_normalize            | 78.5 ms                                                 | 79.8 ms: 1.02x slower                                    |
| dulwich_log                     | 42.7 ms                                                 | 43.5 ms: 1.02x slower                                    |
| many_optionals                  | 731 us                                                  | 745 us: 1.02x slower                                     |
| sqlalchemy_imperative           | 14.1 ms                                                 | 14.4 ms: 1.02x slower                                    |
| async_tree_memoization_tg       | 276 ms                                                  | 281 ms: 1.02x slower                                     |
| async_tree_none_tg              | 220 ms                                                  | 225 ms: 1.02x slower                                     |
| sqlglot_v2_optimize             | 38.6 ms                                                 | 39.5 ms: 1.02x slower                                    |
| async_tree_memoization          | 270 ms                                                  | 276 ms: 1.02x slower                                     |
| hexiom                          | 4.08 ms                                                 | 4.19 ms: 1.03x slower                                    |
| async_tree_eager_memoization_tg | 236 ms                                                  | 242 ms: 1.03x slower                                     |
| 2to3                            | 194 ms                                                  | 200 ms: 1.03x slower                                     |
| genshi_xml                      | 39.4 ms                                                 | 40.6 ms: 1.03x slower                                    |
| async_tree_none                 | 232 ms                                                  | 238 ms: 1.03x slower                                     |
| mako                            | 7.37 ms                                                 | 7.60 ms: 1.03x slower                                    |
| gc_traversal                    | 3.06 ms                                                 | 3.15 ms: 1.03x slower                                    |
| async_tree_eager                | 81.0 ms                                                 | 83.6 ms: 1.03x slower                                    |
| sphinx                          | 755 ms                                                  | 782 ms: 1.04x slower                                     |
| sqlalchemy_declarative          | 96.2 ms                                                 | 99.9 ms: 1.04x slower                                    |
| sqlglot_v2_transpile            | 1.14 ms                                                 | 1.19 ms: 1.04x slower                                    |
| deepcopy_reduce                 | 1.98 us                                                 | 2.06 us: 1.04x slower                                    |
| json_loads                      | 17.4 us                                                 | 18.2 us: 1.04x slower                                    |
| meteor_contest                  | 84.6 ms                                                 | 88.2 ms: 1.04x slower                                    |
| sqlglot_v2_parse                | 894 us                                                  | 934 us: 1.04x slower                                     |
| unpickle_pure_python            | 155 us                                                  | 162 us: 1.05x slower                                     |
| regex_compile                   | 90.1 ms                                                 | 94.5 ms: 1.05x slower                                    |
| docutils                        | 1.95 sec                                                | 2.04 sec: 1.05x slower                                   |
| json                            | 3.35 ms                                                 | 3.52 ms: 1.05x slower                                    |
| pickle_pure_python              | 224 us                                                  | 236 us: 1.05x slower                                     |
| bpe_tokeniser                   | 3.11 sec                                                | 3.26 sec: 1.05x slower                                   |
| richards                        | 31.0 ms                                                 | 32.5 ms: 1.05x slower                                    |
| deepcopy_memo                   | 18.0 us                                                 | 19.0 us: 1.05x slower                                    |
| float                           | 46.7 ms                                                 | 49.5 ms: 1.06x slower                                    |
| django_template                 | 27.9 ms                                                 | 29.7 ms: 1.06x slower                                    |
| telco                           | 5.15 ms                                                 | 5.47 ms: 1.06x slower                                    |
| sqlite_synth                    | 1.56 us                                                 | 1.66 us: 1.06x slower                                    |
| raytrace                        | 186 ms                                                  | 198 ms: 1.07x slower                                     |
| coroutines                      | 14.5 ms                                                 | 15.6 ms: 1.07x slower                                    |
| deepcopy                        | 185 us                                                  | 199 us: 1.08x slower                                     |
| async_tree_cpu_io_mixed_tg      | 395 ms                                                  | 426 ms: 1.08x slower                                     |
| xml_etree_parse                 | 92.9 ms                                                 | 100 ms: 1.08x slower                                     |
| json_dumps                      | 7.27 ms                                                 | 7.86 ms: 1.08x slower                                    |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                  | 326 ms: 1.09x slower                                     |
| genshi_text                     | 16.0 ms                                                 | 17.3 ms: 1.09x slower                                    |
| async_tree_cpu_io_mixed         | 395 ms                                                  | 430 ms: 1.09x slower                                     |
| pprint_safe_repr                | 464 ms                                                  | 506 ms: 1.09x slower                                     |
| comprehensions                  | 10.8 us                                                 | 11.8 us: 1.09x slower                                    |
| nqueens                         | 54.0 ms                                                 | 59.8 ms: 1.11x slower                                    |
| pprint_pformat                  | 943 ms                                                  | 1.05 sec: 1.11x slower                                   |
| xml_etree_process               | 44.9 ms                                                 | 50.7 ms: 1.13x slower                                    |
| xml_etree_generate              | 62.2 ms                                                 | 70.3 ms: 1.13x slower                                    |
| async_generators                | 215 ms                                                  | 246 ms: 1.14x slower                                     |
| Geometric mean                  | (ref)                                                   | 1.04x slower                                             |

Benchmark hidden because not significant (3): pyflate, xml_etree_iterparse, crypto_pyaes

- Geometric mean (including insignificant results): 1.034x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.97x
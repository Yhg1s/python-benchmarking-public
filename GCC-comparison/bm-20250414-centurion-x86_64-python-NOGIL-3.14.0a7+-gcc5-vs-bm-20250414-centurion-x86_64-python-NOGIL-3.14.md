# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.138x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 207 ms                                                   | 242 ms: 1.17x slower                                     |
| docutils       | 2.02 sec                                                 | 2.21 sec: 1.10x slower                                   |
| html5lib       | 47.1 ms                                                  | 54.9 ms: 1.17x slower                                    |
| sphinx         | 788 ms                                                   | 880 ms: 1.12x slower                                     |
| Geometric mean | (ref)                                                    | 1.14x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5 |
|---------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 348 ms: 1.14x slower                                     |
| async_generators                | 238 ms                                                   | 272 ms: 1.14x slower                                     |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 396 ms: 1.15x slower                                     |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 431 ms: 1.15x slower                                     |
| async_tree_eager_memoization_tg | 211 ms                                                   | 246 ms: 1.16x slower                                     |
| async_tree_none                 | 205 ms                                                   | 239 ms: 1.17x slower                                     |
| async_tree_none_tg              | 169 ms                                                   | 198 ms: 1.17x slower                                     |
| async_tree_memoization_tg       | 227 ms                                                   | 268 ms: 1.18x slower                                     |
| async_tree_memoization          | 254 ms                                                   | 302 ms: 1.19x slower                                     |
| async_tree_eager                | 94.7 ms                                                  | 118 ms: 1.25x slower                                     |
| coroutines                      | 14.4 ms                                                  | 18.3 ms: 1.27x slower                                    |
| Geometric mean                  | (ref)                                                    | 1.18x slower                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 181 ms                                                   | 185 ms: 1.02x slower                                     |
| float          | 46.5 ms                                                  | 59.3 ms: 1.28x slower                                    |
| Geometric mean | (ref)                                                    | 1.14x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 158 ms                                                   | 146 ms: 1.09x faster                                     |
| regex_v8       | 14.9 ms                                                  | 15.1 ms: 1.01x slower                                    |
| regex_compile  | 102 ms                                                   | 121 ms: 1.19x slower                                     |
| Geometric mean | (ref)                                                    | 1.03x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5 |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_parse      | 94.4 ms                                                  | 92.3 ms: 1.02x faster                                    |
| xml_etree_iterparse  | 64.7 ms                                                  | 65.9 ms: 1.02x slower                                    |
| xml_etree_generate   | 64.9 ms                                                  | 74.9 ms: 1.15x slower                                    |
| json_dumps           | 7.98 ms                                                  | 9.24 ms: 1.16x slower                                    |
| xml_etree_process    | 46.6 ms                                                  | 55.2 ms: 1.19x slower                                    |
| pickle_pure_python   | 243 us                                                   | 305 us: 1.26x slower                                     |
| tomli_loads          | 1.53 sec                                                 | 1.93 sec: 1.27x slower                                   |
| unpickle_pure_python | 155 us                                                   | 198 us: 1.28x slower                                     |
| json_loads           | 19.5 us                                                  | 26.6 us: 1.37x slower                                    |
| Geometric mean       | (ref)                                                    | 1.18x slower                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5 |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 9.52 ms                                                  | 9.47 ms: 1.01x faster                                    |
| Geometric mean         | (ref)                                                    | 1.00x faster                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5 |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 10.7 ms                                                  | 12.7 ms: 1.19x slower                                    |
| django_template | 30.8 ms                                                  | 37.8 ms: 1.23x slower                                    |
| genshi_text     | 18.7 ms                                                  | 24.2 ms: 1.29x slower                                    |
| genshi_xml      | 41.7 ms                                                  | 54.4 ms: 1.31x slower                                    |
| Geometric mean  | (ref)                                                    | 1.25x slower                                             |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc5 |
|---------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| gc_traversal                    | 1.48 ms                                                  | 1.35 ms: 1.10x faster                                    |
| regex_dna                       | 158 ms                                                   | 146 ms: 1.09x faster                                     |
| xml_etree_parse                 | 94.4 ms                                                  | 92.3 ms: 1.02x faster                                    |
| python_startup_no_site          | 9.52 ms                                                  | 9.47 ms: 1.01x faster                                    |
| create_gc_cycles                | 1.16 ms                                                  | 1.16 ms: 1.00x faster                                    |
| regex_v8                        | 14.9 ms                                                  | 15.1 ms: 1.01x slower                                    |
| xml_etree_iterparse             | 64.7 ms                                                  | 65.9 ms: 1.02x slower                                    |
| pidigits                        | 181 ms                                                   | 185 ms: 1.02x slower                                     |
| coverage                        | 78.4 ms                                                  | 81.0 ms: 1.03x slower                                    |
| meteor_contest                  | 97.9 ms                                                  | 104 ms: 1.06x slower                                     |
| sqlalchemy_imperative           | 16.2 ms                                                  | 17.2 ms: 1.06x slower                                    |
| shortest_path                   | 507 ms                                                   | 541 ms: 1.07x slower                                     |
| pathlib                         | 13.1 ms                                                  | 14.0 ms: 1.07x slower                                    |
| connected_components            | 486 ms                                                   | 523 ms: 1.08x slower                                     |
| sqlalchemy_declarative          | 109 ms                                                   | 118 ms: 1.08x slower                                     |
| bpe_tokeniser                   | 3.13 sec                                                 | 3.39 sec: 1.08x slower                                   |
| sqlite_synth                    | 1.47 us                                                  | 1.59 us: 1.09x slower                                    |
| sympy_integrate                 | 16.6 ms                                                  | 18.1 ms: 1.09x slower                                    |
| docutils                        | 2.02 sec                                                 | 2.21 sec: 1.10x slower                                   |
| dulwich_log                     | 45.2 ms                                                  | 49.7 ms: 1.10x slower                                    |
| many_optionals                  | 751 us                                                   | 836 us: 1.11x slower                                     |
| sphinx                          | 788 ms                                                   | 880 ms: 1.12x slower                                     |
| pyflate                         | 339 ms                                                   | 381 ms: 1.12x slower                                     |
| sympy_sum                       | 112 ms                                                   | 127 ms: 1.13x slower                                     |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 348 ms: 1.14x slower                                     |
| async_generators                | 238 ms                                                   | 272 ms: 1.14x slower                                     |
| subparsers                      | 18.4 ms                                                  | 21.1 ms: 1.15x slower                                    |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 396 ms: 1.15x slower                                     |
| sympy_str                       | 211 ms                                                   | 243 ms: 1.15x slower                                     |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 431 ms: 1.15x slower                                     |
| xml_etree_generate              | 64.9 ms                                                  | 74.9 ms: 1.15x slower                                    |
| json_dumps                      | 7.98 ms                                                  | 9.24 ms: 1.16x slower                                    |
| async_tree_eager_memoization_tg | 211 ms                                                   | 246 ms: 1.16x slower                                     |
| sympy_expand                    | 360 ms                                                   | 419 ms: 1.16x slower                                     |
| html5lib                        | 47.1 ms                                                  | 54.9 ms: 1.17x slower                                    |
| telco                           | 6.04 ms                                                  | 7.06 ms: 1.17x slower                                    |
| async_tree_none                 | 205 ms                                                   | 239 ms: 1.17x slower                                     |
| 2to3                            | 207 ms                                                   | 242 ms: 1.17x slower                                     |
| async_tree_none_tg              | 169 ms                                                   | 198 ms: 1.17x slower                                     |
| async_tree_memoization_tg       | 227 ms                                                   | 268 ms: 1.18x slower                                     |
| xml_etree_process               | 46.6 ms                                                  | 55.2 ms: 1.19x slower                                    |
| mako                            | 10.7 ms                                                  | 12.7 ms: 1.19x slower                                    |
| mdp                             | 925 ms                                                   | 1.10 sec: 1.19x slower                                   |
| typing_runtime_protocols        | 132 us                                                   | 157 us: 1.19x slower                                     |
| regex_compile                   | 102 ms                                                   | 121 ms: 1.19x slower                                     |
| async_tree_memoization          | 254 ms                                                   | 302 ms: 1.19x slower                                     |
| raytrace                        | 217 ms                                                   | 259 ms: 1.20x slower                                     |
| sqlglot_v2_transpile            | 1.26 ms                                                  | 1.53 ms: 1.21x slower                                    |
| sqlglot_v2_optimize             | 39.7 ms                                                  | 48.4 ms: 1.22x slower                                    |
| nqueens                         | 61.6 ms                                                  | 75.4 ms: 1.22x slower                                    |
| django_template                 | 30.8 ms                                                  | 37.8 ms: 1.23x slower                                    |
| sqlglot_v2_parse                | 1.03 ms                                                  | 1.27 ms: 1.23x slower                                    |
| hexiom                          | 4.64 ms                                                  | 5.78 ms: 1.25x slower                                    |
| async_tree_eager                | 94.7 ms                                                  | 118 ms: 1.25x slower                                     |
| deltablue                       | 2.50 ms                                                  | 3.13 ms: 1.25x slower                                    |
| crypto_pyaes                    | 59.5 ms                                                  | 74.6 ms: 1.25x slower                                    |
| pickle_pure_python              | 243 us                                                   | 305 us: 1.26x slower                                     |
| tomli_loads                     | 1.53 sec                                                 | 1.93 sec: 1.27x slower                                   |
| coroutines                      | 14.4 ms                                                  | 18.3 ms: 1.27x slower                                    |
| richards                        | 36.1 ms                                                  | 45.9 ms: 1.27x slower                                    |
| sqlglot_v2_normalize            | 80.1 ms                                                  | 102 ms: 1.27x slower                                     |
| deepcopy_reduce                 | 2.23 us                                                  | 2.85 us: 1.28x slower                                    |
| float                           | 46.5 ms                                                  | 59.3 ms: 1.28x slower                                    |
| unpickle_pure_python            | 155 us                                                   | 198 us: 1.28x slower                                     |
| json                            | 3.48 ms                                                  | 4.50 ms: 1.29x slower                                    |
| genshi_text                     | 18.7 ms                                                  | 24.2 ms: 1.29x slower                                    |
| genshi_xml                      | 41.7 ms                                                  | 54.4 ms: 1.31x slower                                    |
| deepcopy                        | 211 us                                                   | 276 us: 1.31x slower                                     |
| pprint_pformat                  | 1.12 sec                                                 | 1.47 sec: 1.31x slower                                   |
| deepcopy_memo                   | 21.4 us                                                  | 28.5 us: 1.33x slower                                    |
| pprint_safe_repr                | 530 ms                                                   | 715 ms: 1.35x slower                                     |
| comprehensions                  | 11.9 us                                                  | 16.2 us: 1.35x slower                                    |
| json_loads                      | 19.5 us                                                  | 26.6 us: 1.37x slower                                    |
| Geometric mean                  | (ref)                                                    | 1.16x slower                                             |

Benchmark hidden because not significant (1): python_startup

- Geometric mean (including insignificant results): 1.138x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 0.99x
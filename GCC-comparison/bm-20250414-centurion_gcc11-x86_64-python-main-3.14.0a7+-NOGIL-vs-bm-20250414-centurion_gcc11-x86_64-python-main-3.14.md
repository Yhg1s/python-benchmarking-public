# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.044x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.50x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 195 ms                                                          | 207 ms: 1.06x slower                                           |
| docutils       | 1.96 sec                                                        | 2.04 sec: 1.04x slower                                         |
| sphinx         | 757 ms                                                          | 796 ms: 1.05x slower                                           |
| Geometric mean | (ref)                                                           | 1.04x slower                                                   |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_none_tg              | 217 ms                                                          | 171 ms: 1.27x faster                                           |
| async_tree_memoization_tg       | 272 ms                                                          | 229 ms: 1.19x faster                                           |
| async_tree_none                 | 232 ms                                                          | 205 ms: 1.13x faster                                           |
| async_tree_cpu_io_mixed_tg      | 390 ms                                                          | 347 ms: 1.13x faster                                           |
| async_tree_eager_memoization_tg | 237 ms                                                          | 213 ms: 1.11x faster                                           |
| coroutines                      | 15.2 ms                                                         | 14.6 ms: 1.04x faster                                          |
| async_tree_cpu_io_mixed         | 392 ms                                                          | 378 ms: 1.04x faster                                           |
| async_tree_memoization          | 265 ms                                                          | 258 ms: 1.02x faster                                           |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                          | 305 ms: 1.02x slower                                           |
| async_generators                | 215 ms                                                          | 237 ms: 1.10x slower                                           |
| async_tree_eager                | 80.9 ms                                                         | 95.7 ms: 1.18x slower                                          |
| Geometric mean                  | (ref)                                                           | 1.05x faster                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 186 ms                                                          | 184 ms: 1.01x faster                                           |
| float          | 46.8 ms                                                         | 48.6 ms: 1.04x slower                                          |
| Geometric mean | (ref)                                                           | 1.02x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_v8       | 15.1 ms                                                         | 14.2 ms: 1.06x faster                                          |
| regex_dna      | 150 ms                                                          | 152 ms: 1.02x slower                                           |
| regex_compile  | 91.7 ms                                                         | 104 ms: 1.13x slower                                           |
| Geometric mean | (ref)                                                           | 1.03x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 68.3 ms                                                         | 56.8 ms: 1.20x faster                                          |
| xml_etree_parse      | 93.9 ms                                                         | 90.0 ms: 1.04x faster                                          |
| unpickle_pure_python | 158 us                                                          | 154 us: 1.03x faster                                           |
| pickle_pure_python   | 227 us                                                          | 240 us: 1.05x slower                                           |
| xml_etree_process    | 45.2 ms                                                         | 47.9 ms: 1.06x slower                                          |
| xml_etree_generate   | 61.5 ms                                                         | 65.7 ms: 1.07x slower                                          |
| json_loads           | 18.1 us                                                         | 19.7 us: 1.09x slower                                          |
| tomli_loads          | 1.37 sec                                                        | 1.49 sec: 1.09x slower                                         |
| json_dumps           | 7.35 ms                                                         | 8.13 ms: 1.11x slower                                          |
| Geometric mean       | (ref)                                                           | 1.02x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL |
|------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                         | 12.8 ms: 1.19x slower                                          |
| python_startup_no_site | 7.45 ms                                                         | 9.35 ms: 1.25x slower                                          |
| Geometric mean         | (ref)                                                           | 1.22x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL |
|-----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 39.2 ms                                                         | 41.8 ms: 1.07x slower                                          |
| django_template | 28.7 ms                                                         | 30.7 ms: 1.07x slower                                          |
| genshi_text     | 16.5 ms                                                         | 19.2 ms: 1.17x slower                                          |
| mako            | 8.03 ms                                                         | 10.9 ms: 1.36x slower                                          |
| Geometric mean  | (ref)                                                           | 1.16x slower                                                   |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc11-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal                    | 3.06 ms                                                         | 1.32 ms: 2.32x faster                                          |
| create_gc_cycles                | 1.75 ms                                                         | 1.15 ms: 1.52x faster                                          |
| async_tree_none_tg              | 217 ms                                                          | 171 ms: 1.27x faster                                           |
| xml_etree_iterparse             | 68.3 ms                                                         | 56.8 ms: 1.20x faster                                          |
| async_tree_memoization_tg       | 272 ms                                                          | 229 ms: 1.19x faster                                           |
| async_tree_none                 | 232 ms                                                          | 205 ms: 1.13x faster                                           |
| async_tree_cpu_io_mixed_tg      | 390 ms                                                          | 347 ms: 1.13x faster                                           |
| async_tree_eager_memoization_tg | 237 ms                                                          | 213 ms: 1.11x faster                                           |
| regex_v8                        | 15.1 ms                                                         | 14.2 ms: 1.06x faster                                          |
| xml_etree_parse                 | 93.9 ms                                                         | 90.0 ms: 1.04x faster                                          |
| sqlite_synth                    | 1.62 us                                                         | 1.56 us: 1.04x faster                                          |
| coroutines                      | 15.2 ms                                                         | 14.6 ms: 1.04x faster                                          |
| async_tree_cpu_io_mixed         | 392 ms                                                          | 378 ms: 1.04x faster                                           |
| pathlib                         | 12.3 ms                                                         | 11.9 ms: 1.04x faster                                          |
| unpickle_pure_python            | 158 us                                                          | 154 us: 1.03x faster                                           |
| async_tree_memoization          | 265 ms                                                          | 258 ms: 1.02x faster                                           |
| pidigits                        | 186 ms                                                          | 184 ms: 1.01x faster                                           |
| bpe_tokeniser                   | 3.08 sec                                                        | 3.07 sec: 1.00x faster                                         |
| mdp                             | 947 ms                                                          | 957 ms: 1.01x slower                                           |
| regex_dna                       | 150 ms                                                          | 152 ms: 1.02x slower                                           |
| async_tree_eager_cpu_io_mixed   | 300 ms                                                          | 305 ms: 1.02x slower                                           |
| many_optionals                  | 726 us                                                          | 742 us: 1.02x slower                                           |
| deltablue                       | 2.40 ms                                                         | 2.49 ms: 1.04x slower                                          |
| float                           | 46.8 ms                                                         | 48.6 ms: 1.04x slower                                          |
| docutils                        | 1.96 sec                                                        | 2.04 sec: 1.04x slower                                         |
| subparsers                      | 17.2 ms                                                         | 18.0 ms: 1.04x slower                                          |
| sqlglot_v2_normalize            | 78.9 ms                                                         | 82.4 ms: 1.05x slower                                          |
| sqlglot_v2_optimize             | 39.0 ms                                                         | 40.9 ms: 1.05x slower                                          |
| sphinx                          | 757 ms                                                          | 796 ms: 1.05x slower                                           |
| pickle_pure_python              | 227 us                                                          | 240 us: 1.05x slower                                           |
| xml_etree_process               | 45.2 ms                                                         | 47.9 ms: 1.06x slower                                          |
| 2to3                            | 195 ms                                                          | 207 ms: 1.06x slower                                           |
| dulwich_log                     | 42.1 ms                                                         | 44.7 ms: 1.06x slower                                          |
| pyflate                         | 306 ms                                                          | 326 ms: 1.07x slower                                           |
| genshi_xml                      | 39.2 ms                                                         | 41.8 ms: 1.07x slower                                          |
| xml_etree_generate              | 61.5 ms                                                         | 65.7 ms: 1.07x slower                                          |
| django_template                 | 28.7 ms                                                         | 30.7 ms: 1.07x slower                                          |
| sympy_sum                       | 106 ms                                                          | 113 ms: 1.07x slower                                           |
| json_loads                      | 18.1 us                                                         | 19.7 us: 1.09x slower                                          |
| hexiom                          | 4.10 ms                                                         | 4.46 ms: 1.09x slower                                          |
| tomli_loads                     | 1.37 sec                                                        | 1.49 sec: 1.09x slower                                         |
| async_generators                | 215 ms                                                          | 237 ms: 1.10x slower                                           |
| sympy_integrate                 | 15.0 ms                                                         | 16.5 ms: 1.10x slower                                          |
| nqueens                         | 54.8 ms                                                         | 60.5 ms: 1.10x slower                                          |
| json_dumps                      | 7.35 ms                                                         | 8.13 ms: 1.11x slower                                          |
| sympy_str                       | 193 ms                                                          | 213 ms: 1.11x slower                                           |
| sympy_expand                    | 333 ms                                                          | 369 ms: 1.11x slower                                           |
| comprehensions                  | 11.1 us                                                         | 12.4 us: 1.12x slower                                          |
| sqlalchemy_imperative           | 14.2 ms                                                         | 15.9 ms: 1.12x slower                                          |
| pprint_safe_repr                | 480 ms                                                          | 542 ms: 1.13x slower                                           |
| sqlalchemy_declarative          | 96.7 ms                                                         | 109 ms: 1.13x slower                                           |
| regex_compile                   | 91.7 ms                                                         | 104 ms: 1.13x slower                                           |
| sqlglot_v2_transpile            | 1.15 ms                                                         | 1.30 ms: 1.13x slower                                          |
| raytrace                        | 185 ms                                                          | 209 ms: 1.13x slower                                           |
| sqlglot_v2_parse                | 911 us                                                          | 1.04 ms: 1.14x slower                                          |
| pprint_pformat                  | 988 ms                                                          | 1.13 sec: 1.15x slower                                         |
| deepcopy                        | 193 us                                                          | 222 us: 1.15x slower                                           |
| crypto_pyaes                    | 52.3 ms                                                         | 60.5 ms: 1.16x slower                                          |
| deepcopy_reduce                 | 2.02 us                                                         | 2.35 us: 1.17x slower                                          |
| genshi_text                     | 16.5 ms                                                         | 19.2 ms: 1.17x slower                                          |
| connected_components            | 432 ms                                                          | 505 ms: 1.17x slower                                           |
| async_tree_eager                | 80.9 ms                                                         | 95.7 ms: 1.18x slower                                          |
| python_startup                  | 10.7 ms                                                         | 12.8 ms: 1.19x slower                                          |
| meteor_contest                  | 82.8 ms                                                         | 98.4 ms: 1.19x slower                                          |
| telco                           | 5.27 ms                                                         | 6.27 ms: 1.19x slower                                          |
| shortest_path                   | 438 ms                                                          | 526 ms: 1.20x slower                                           |
| deepcopy_memo                   | 18.6 us                                                         | 22.3 us: 1.20x slower                                          |
| richards                        | 31.8 ms                                                         | 38.2 ms: 1.20x slower                                          |
| typing_runtime_protocols        | 109 us                                                          | 132 us: 1.22x slower                                           |
| python_startup_no_site          | 7.45 ms                                                         | 9.35 ms: 1.25x slower                                          |
| mako                            | 8.03 ms                                                         | 10.9 ms: 1.36x slower                                          |
| coverage                        | 55.3 ms                                                         | 77.1 ms: 1.39x slower                                          |
| Geometric mean                  | (ref)                                                           | 1.05x slower                                                   |

Benchmark hidden because not significant (2): json, html5lib

- Geometric mean (including insignificant results): 1.044x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.50x
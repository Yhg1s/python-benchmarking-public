# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL
- machine: unknown-unknown
- commit hash: 7890b77
- commit date: 2025-04-14
- overall geometric mean: 1.087x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.50x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 200 ms                                                          | 221 ms: 1.10x slower                                           |
| docutils       | 2.04 sec                                                        | 2.19 sec: 1.07x slower                                         |
| html5lib       | 46.9 ms                                                         | 50.5 ms: 1.08x slower                                          |
| sphinx         | 782 ms                                                          | 844 ms: 1.08x slower                                           |
| Geometric mean | (ref)                                                           | 1.08x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_none_tg              | 225 ms                                                          | 191 ms: 1.18x faster                                           |
| async_tree_memoization_tg       | 281 ms                                                          | 253 ms: 1.11x faster                                           |
| async_tree_cpu_io_mixed_tg      | 426 ms                                                          | 400 ms: 1.07x faster                                           |
| async_tree_eager_memoization_tg | 242 ms                                                          | 229 ms: 1.06x faster                                           |
| async_tree_none                 | 238 ms                                                          | 226 ms: 1.05x faster                                           |
| coroutines                      | 15.6 ms                                                         | 15.2 ms: 1.03x faster                                          |
| async_tree_memoization          | 276 ms                                                          | 287 ms: 1.04x slower                                           |
| async_tree_eager_cpu_io_mixed   | 326 ms                                                          | 345 ms: 1.06x slower                                           |
| async_generators                | 246 ms                                                          | 269 ms: 1.09x slower                                           |
| async_tree_eager                | 83.6 ms                                                         | 103 ms: 1.23x slower                                           |
| Geometric mean                  | (ref)                                                           | 1.01x faster                                                   |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 181 ms                                                          | 179 ms: 1.01x faster                                           |
| float          | 49.5 ms                                                         | 55.0 ms: 1.11x slower                                          |
| Geometric mean | (ref)                                                           | 1.05x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_dna      | 144 ms                                                          | 146 ms: 1.01x slower                                           |
| regex_v8       | 15.0 ms                                                         | 15.5 ms: 1.03x slower                                          |
| regex_compile  | 94.5 ms                                                         | 113 ms: 1.20x slower                                           |
| Geometric mean | (ref)                                                           | 1.08x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 77.8 ms                                                         | 60.0 ms: 1.30x faster                                          |
| xml_etree_parse      | 100 ms                                                          | 98.0 ms: 1.03x faster                                          |
| xml_etree_generate   | 70.3 ms                                                         | 75.1 ms: 1.07x slower                                          |
| xml_etree_process    | 50.7 ms                                                         | 54.4 ms: 1.07x slower                                          |
| json_loads           | 18.2 us                                                         | 19.5 us: 1.07x slower                                          |
| json_dumps           | 7.86 ms                                                         | 8.64 ms: 1.10x slower                                          |
| unpickle_pure_python | 162 us                                                          | 187 us: 1.15x slower                                           |
| pickle_pure_python   | 236 us                                                          | 278 us: 1.18x slower                                           |
| tomli_loads          | 1.41 sec                                                        | 1.72 sec: 1.22x slower                                         |
| Geometric mean       | (ref)                                                           | 1.06x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL |
|------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                         | 12.9 ms: 1.20x slower                                          |
| python_startup_no_site | 7.47 ms                                                         | 9.41 ms: 1.26x slower                                          |
| Geometric mean         | (ref)                                                           | 1.23x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL |
|-----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| django_template | 29.7 ms                                                         | 34.8 ms: 1.17x slower                                          |
| genshi_xml      | 40.6 ms                                                         | 47.9 ms: 1.18x slower                                          |
| genshi_text     | 17.3 ms                                                         | 21.6 ms: 1.25x slower                                          |
| mako            | 7.60 ms                                                         | 11.8 ms: 1.55x slower                                          |
| Geometric mean  | (ref)                                                           | 1.28x slower                                                   |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc14-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal                    | 3.15 ms                                                         | 1.33 ms: 2.36x faster                                          |
| create_gc_cycles                | 1.74 ms                                                         | 1.14 ms: 1.52x faster                                          |
| xml_etree_iterparse             | 77.8 ms                                                         | 60.0 ms: 1.30x faster                                          |
| async_tree_none_tg              | 225 ms                                                          | 191 ms: 1.18x faster                                           |
| async_tree_memoization_tg       | 281 ms                                                          | 253 ms: 1.11x faster                                           |
| async_tree_cpu_io_mixed_tg      | 426 ms                                                          | 400 ms: 1.07x faster                                           |
| sqlite_synth                    | 1.66 us                                                         | 1.56 us: 1.06x faster                                          |
| async_tree_eager_memoization_tg | 242 ms                                                          | 229 ms: 1.06x faster                                           |
| async_tree_none                 | 238 ms                                                          | 226 ms: 1.05x faster                                           |
| coroutines                      | 15.6 ms                                                         | 15.2 ms: 1.03x faster                                          |
| xml_etree_parse                 | 100 ms                                                          | 98.0 ms: 1.03x faster                                          |
| pidigits                        | 181 ms                                                          | 179 ms: 1.01x faster                                           |
| pathlib                         | 12.8 ms                                                         | 12.7 ms: 1.01x faster                                          |
| regex_dna                       | 144 ms                                                          | 146 ms: 1.01x slower                                           |
| json                            | 3.52 ms                                                         | 3.62 ms: 1.03x slower                                          |
| regex_v8                        | 15.0 ms                                                         | 15.5 ms: 1.03x slower                                          |
| async_tree_memoization          | 276 ms                                                          | 287 ms: 1.04x slower                                           |
| async_tree_eager_cpu_io_mixed   | 326 ms                                                          | 345 ms: 1.06x slower                                           |
| dulwich_log                     | 43.5 ms                                                         | 46.2 ms: 1.06x slower                                          |
| mdp                             | 952 ms                                                          | 1.01 sec: 1.06x slower                                         |
| many_optionals                  | 745 us                                                          | 792 us: 1.06x slower                                           |
| xml_etree_generate              | 70.3 ms                                                         | 75.1 ms: 1.07x slower                                          |
| docutils                        | 2.04 sec                                                        | 2.19 sec: 1.07x slower                                         |
| bpe_tokeniser                   | 3.26 sec                                                        | 3.50 sec: 1.07x slower                                         |
| xml_etree_process               | 50.7 ms                                                         | 54.4 ms: 1.07x slower                                          |
| json_loads                      | 18.2 us                                                         | 19.5 us: 1.07x slower                                          |
| html5lib                        | 46.9 ms                                                         | 50.5 ms: 1.08x slower                                          |
| sphinx                          | 782 ms                                                          | 844 ms: 1.08x slower                                           |
| sympy_sum                       | 107 ms                                                          | 117 ms: 1.09x slower                                           |
| async_generators                | 246 ms                                                          | 269 ms: 1.09x slower                                           |
| json_dumps                      | 7.86 ms                                                         | 8.64 ms: 1.10x slower                                          |
| subparsers                      | 17.3 ms                                                         | 19.1 ms: 1.10x slower                                          |
| 2to3                            | 200 ms                                                          | 221 ms: 1.10x slower                                           |
| float                           | 49.5 ms                                                         | 55.0 ms: 1.11x slower                                          |
| sqlglot_v2_normalize            | 79.8 ms                                                         | 89.1 ms: 1.12x slower                                          |
| sqlglot_v2_optimize             | 39.5 ms                                                         | 44.2 ms: 1.12x slower                                          |
| nqueens                         | 59.8 ms                                                         | 67.5 ms: 1.13x slower                                          |
| sqlalchemy_imperative           | 14.4 ms                                                         | 16.4 ms: 1.14x slower                                          |
| telco                           | 5.47 ms                                                         | 6.23 ms: 1.14x slower                                          |
| sympy_str                       | 195 ms                                                          | 222 ms: 1.14x slower                                           |
| sympy_expand                    | 333 ms                                                          | 382 ms: 1.15x slower                                           |
| sympy_integrate                 | 15.1 ms                                                         | 17.4 ms: 1.15x slower                                          |
| sqlalchemy_declarative          | 99.9 ms                                                         | 115 ms: 1.15x slower                                           |
| unpickle_pure_python            | 162 us                                                          | 187 us: 1.15x slower                                           |
| connected_components            | 435 ms                                                          | 505 ms: 1.16x slower                                           |
| django_template                 | 29.7 ms                                                         | 34.8 ms: 1.17x slower                                          |
| shortest_path                   | 447 ms                                                          | 526 ms: 1.18x slower                                           |
| meteor_contest                  | 88.2 ms                                                         | 104 ms: 1.18x slower                                           |
| pickle_pure_python              | 236 us                                                          | 278 us: 1.18x slower                                           |
| genshi_xml                      | 40.6 ms                                                         | 47.9 ms: 1.18x slower                                          |
| deepcopy                        | 199 us                                                          | 237 us: 1.19x slower                                           |
| sqlglot_v2_transpile            | 1.19 ms                                                         | 1.41 ms: 1.19x slower                                          |
| crypto_pyaes                    | 52.8 ms                                                         | 63.1 ms: 1.19x slower                                          |
| python_startup                  | 10.8 ms                                                         | 12.9 ms: 1.20x slower                                          |
| pprint_safe_repr                | 506 ms                                                          | 607 ms: 1.20x slower                                           |
| regex_compile                   | 94.5 ms                                                         | 113 ms: 1.20x slower                                           |
| comprehensions                  | 11.8 us                                                         | 14.3 us: 1.22x slower                                          |
| tomli_loads                     | 1.41 sec                                                        | 1.72 sec: 1.22x slower                                         |
| pyflate                         | 310 ms                                                          | 380 ms: 1.22x slower                                           |
| pprint_pformat                  | 1.05 sec                                                        | 1.28 sec: 1.23x slower                                         |
| async_tree_eager                | 83.6 ms                                                         | 103 ms: 1.23x slower                                           |
| sqlglot_v2_parse                | 934 us                                                          | 1.15 ms: 1.23x slower                                          |
| deepcopy_reduce                 | 2.06 us                                                         | 2.55 us: 1.24x slower                                          |
| raytrace                        | 198 ms                                                          | 245 ms: 1.24x slower                                           |
| genshi_text                     | 17.3 ms                                                         | 21.6 ms: 1.25x slower                                          |
| python_startup_no_site          | 7.47 ms                                                         | 9.41 ms: 1.26x slower                                          |
| deltablue                       | 2.34 ms                                                         | 2.98 ms: 1.27x slower                                          |
| hexiom                          | 4.19 ms                                                         | 5.34 ms: 1.28x slower                                          |
| typing_runtime_protocols        | 107 us                                                          | 142 us: 1.33x slower                                           |
| richards                        | 32.5 ms                                                         | 43.5 ms: 1.34x slower                                          |
| deepcopy_memo                   | 19.0 us                                                         | 25.8 us: 1.36x slower                                          |
| coverage                        | 55.3 ms                                                         | 77.8 ms: 1.41x slower                                          |
| mako                            | 7.60 ms                                                         | 11.8 ms: 1.55x slower                                          |
| Geometric mean                  | (ref)                                                           | 1.10x slower                                                   |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

- Geometric mean (including insignificant results): 1.087x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.50x
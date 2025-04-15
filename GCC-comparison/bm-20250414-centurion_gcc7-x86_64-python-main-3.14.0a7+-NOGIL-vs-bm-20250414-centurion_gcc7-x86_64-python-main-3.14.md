# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.069x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.48x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 198 ms                                                         | 219 ms: 1.10x slower                                          |
| docutils       | 1.95 sec                                                       | 2.09 sec: 1.07x slower                                        |
| html5lib       | 46.4 ms                                                        | 48.1 ms: 1.04x slower                                         |
| sphinx         | 765 ms                                                         | 828 ms: 1.08x slower                                          |
| Geometric mean | (ref)                                                          | 1.07x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none_tg              | 223 ms                                                         | 175 ms: 1.28x faster                                          |
| async_tree_memoization_tg       | 279 ms                                                         | 236 ms: 1.18x faster                                          |
| async_tree_cpu_io_mixed_tg      | 407 ms                                                         | 363 ms: 1.12x faster                                          |
| async_tree_none                 | 239 ms                                                         | 215 ms: 1.11x faster                                          |
| async_tree_eager_memoization_tg | 243 ms                                                         | 222 ms: 1.09x faster                                          |
| async_tree_cpu_io_mixed         | 412 ms                                                         | 398 ms: 1.04x faster                                          |
| async_tree_memoization          | 276 ms                                                         | 271 ms: 1.02x faster                                          |
| coroutines                      | 15.3 ms                                                        | 15.6 ms: 1.02x slower                                         |
| async_tree_eager_cpu_io_mixed   | 314 ms                                                         | 328 ms: 1.04x slower                                          |
| async_generators                | 223 ms                                                         | 246 ms: 1.10x slower                                          |
| async_tree_eager                | 86.0 ms                                                        | 107 ms: 1.24x slower                                          |
| Geometric mean                  | (ref)                                                          | 1.04x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 189 ms                                                         | 186 ms: 1.02x faster                                          |
| float          | 48.7 ms                                                        | 52.2 ms: 1.07x slower                                         |
| Geometric mean | (ref)                                                          | 1.03x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_v8       | 14.9 ms                                                        | 14.7 ms: 1.01x faster                                         |
| regex_dna      | 134 ms                                                         | 142 ms: 1.06x slower                                          |
| regex_compile  | 93.5 ms                                                        | 107 ms: 1.14x slower                                          |
| Geometric mean | (ref)                                                          | 1.06x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 75.9 ms                                                        | 63.6 ms: 1.19x faster                                         |
| xml_etree_parse      | 94.9 ms                                                        | 91.4 ms: 1.04x faster                                         |
| xml_etree_generate   | 66.7 ms                                                        | 72.0 ms: 1.08x slower                                         |
| unpickle_pure_python | 158 us                                                         | 171 us: 1.08x slower                                          |
| xml_etree_process    | 48.0 ms                                                        | 52.0 ms: 1.08x slower                                         |
| tomli_loads          | 1.39 sec                                                       | 1.53 sec: 1.10x slower                                        |
| json_dumps           | 8.28 ms                                                        | 9.19 ms: 1.11x slower                                         |
| pickle_pure_python   | 228 us                                                         | 259 us: 1.14x slower                                          |
| json_loads           | 18.9 us                                                        | 22.7 us: 1.20x slower                                         |
| Geometric mean       | (ref)                                                          | 1.06x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL |
|------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                        | 13.0 ms: 1.19x slower                                         |
| python_startup_no_site | 7.63 ms                                                        | 9.55 ms: 1.25x slower                                         |
| Geometric mean         | (ref)                                                          | 1.22x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL |
|-----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| django_template | 28.6 ms                                                        | 32.5 ms: 1.13x slower                                         |
| genshi_xml      | 40.7 ms                                                        | 46.3 ms: 1.14x slower                                         |
| genshi_text     | 16.2 ms                                                        | 20.8 ms: 1.28x slower                                         |
| mako            | 7.99 ms                                                        | 11.5 ms: 1.44x slower                                         |
| Geometric mean  | (ref)                                                          | 1.24x slower                                                  |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc7-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| gc_traversal                    | 3.15 ms                                                        | 1.39 ms: 2.26x faster                                         |
| create_gc_cycles                | 1.79 ms                                                        | 1.17 ms: 1.53x faster                                         |
| async_tree_none_tg              | 223 ms                                                         | 175 ms: 1.28x faster                                          |
| xml_etree_iterparse             | 75.9 ms                                                        | 63.6 ms: 1.19x faster                                         |
| async_tree_memoization_tg       | 279 ms                                                         | 236 ms: 1.18x faster                                          |
| async_tree_cpu_io_mixed_tg      | 407 ms                                                         | 363 ms: 1.12x faster                                          |
| async_tree_none                 | 239 ms                                                         | 215 ms: 1.11x faster                                          |
| async_tree_eager_memoization_tg | 243 ms                                                         | 222 ms: 1.09x faster                                          |
| sqlite_synth                    | 1.73 us                                                        | 1.66 us: 1.05x faster                                         |
| xml_etree_parse                 | 94.9 ms                                                        | 91.4 ms: 1.04x faster                                         |
| async_tree_cpu_io_mixed         | 412 ms                                                         | 398 ms: 1.04x faster                                          |
| async_tree_memoization          | 276 ms                                                         | 271 ms: 1.02x faster                                          |
| pidigits                        | 189 ms                                                         | 186 ms: 1.02x faster                                          |
| regex_v8                        | 14.9 ms                                                        | 14.7 ms: 1.01x faster                                         |
| pathlib                         | 13.2 ms                                                        | 13.3 ms: 1.00x slower                                         |
| coroutines                      | 15.3 ms                                                        | 15.6 ms: 1.02x slower                                         |
| bpe_tokeniser                   | 3.17 sec                                                       | 3.26 sec: 1.03x slower                                        |
| mdp                             | 976 ms                                                         | 1.01 sec: 1.03x slower                                        |
| html5lib                        | 46.4 ms                                                        | 48.1 ms: 1.04x slower                                         |
| async_tree_eager_cpu_io_mixed   | 314 ms                                                         | 328 ms: 1.04x slower                                          |
| regex_dna                       | 134 ms                                                         | 142 ms: 1.06x slower                                          |
| docutils                        | 1.95 sec                                                       | 2.09 sec: 1.07x slower                                        |
| float                           | 48.7 ms                                                        | 52.2 ms: 1.07x slower                                         |
| many_optionals                  | 740 us                                                         | 794 us: 1.07x slower                                          |
| pyflate                         | 306 ms                                                         | 329 ms: 1.08x slower                                          |
| xml_etree_generate              | 66.7 ms                                                        | 72.0 ms: 1.08x slower                                         |
| sphinx                          | 765 ms                                                         | 828 ms: 1.08x slower                                          |
| unpickle_pure_python            | 158 us                                                         | 171 us: 1.08x slower                                          |
| xml_etree_process               | 48.0 ms                                                        | 52.0 ms: 1.08x slower                                         |
| json                            | 3.57 ms                                                        | 3.87 ms: 1.08x slower                                         |
| subparsers                      | 18.0 ms                                                        | 19.7 ms: 1.09x slower                                         |
| dulwich_log                     | 43.6 ms                                                        | 47.6 ms: 1.09x slower                                         |
| tomli_loads                     | 1.39 sec                                                       | 1.53 sec: 1.10x slower                                        |
| async_generators                | 223 ms                                                         | 246 ms: 1.10x slower                                          |
| sympy_sum                       | 108 ms                                                         | 119 ms: 1.10x slower                                          |
| 2to3                            | 198 ms                                                         | 219 ms: 1.10x slower                                          |
| json_dumps                      | 8.28 ms                                                        | 9.19 ms: 1.11x slower                                         |
| connected_components            | 437 ms                                                         | 488 ms: 1.12x slower                                          |
| sqlglot_v2_optimize             | 38.7 ms                                                        | 43.4 ms: 1.12x slower                                         |
| nqueens                         | 56.3 ms                                                        | 63.4 ms: 1.13x slower                                         |
| sympy_str                       | 200 ms                                                         | 226 ms: 1.13x slower                                          |
| sympy_integrate                 | 15.0 ms                                                        | 16.9 ms: 1.13x slower                                         |
| pprint_safe_repr                | 506 ms                                                         | 571 ms: 1.13x slower                                          |
| sqlglot_v2_normalize            | 78.7 ms                                                        | 89.2 ms: 1.13x slower                                         |
| django_template                 | 28.6 ms                                                        | 32.5 ms: 1.13x slower                                         |
| pickle_pure_python              | 228 us                                                         | 259 us: 1.14x slower                                          |
| genshi_xml                      | 40.7 ms                                                        | 46.3 ms: 1.14x slower                                         |
| sqlalchemy_declarative          | 97.9 ms                                                        | 112 ms: 1.14x slower                                          |
| regex_compile                   | 93.5 ms                                                        | 107 ms: 1.14x slower                                          |
| sympy_expand                    | 343 ms                                                         | 391 ms: 1.14x slower                                          |
| hexiom                          | 4.17 ms                                                        | 4.76 ms: 1.14x slower                                         |
| meteor_contest                  | 84.8 ms                                                        | 97.3 ms: 1.15x slower                                         |
| deltablue                       | 2.21 ms                                                        | 2.53 ms: 1.15x slower                                         |
| sqlglot_v2_transpile            | 1.16 ms                                                        | 1.34 ms: 1.15x slower                                         |
| sqlalchemy_imperative           | 14.3 ms                                                        | 16.5 ms: 1.15x slower                                         |
| raytrace                        | 191 ms                                                         | 220 ms: 1.15x slower                                          |
| pprint_pformat                  | 1.03 sec                                                       | 1.19 sec: 1.16x slower                                        |
| shortest_path                   | 442 ms                                                         | 513 ms: 1.16x slower                                          |
| crypto_pyaes                    | 56.9 ms                                                        | 67.4 ms: 1.19x slower                                         |
| richards                        | 32.2 ms                                                        | 38.2 ms: 1.19x slower                                         |
| comprehensions                  | 10.8 us                                                        | 12.8 us: 1.19x slower                                         |
| python_startup                  | 11.0 ms                                                        | 13.0 ms: 1.19x slower                                         |
| sqlglot_v2_parse                | 920 us                                                         | 1.10 ms: 1.19x slower                                         |
| json_loads                      | 18.9 us                                                        | 22.7 us: 1.20x slower                                         |
| deepcopy                        | 196 us                                                         | 240 us: 1.22x slower                                          |
| typing_runtime_protocols        | 116 us                                                         | 143 us: 1.23x slower                                          |
| async_tree_eager                | 86.0 ms                                                        | 107 ms: 1.24x slower                                          |
| telco                           | 5.70 ms                                                        | 7.09 ms: 1.24x slower                                         |
| deepcopy_memo                   | 18.1 us                                                        | 22.5 us: 1.24x slower                                         |
| python_startup_no_site          | 7.63 ms                                                        | 9.55 ms: 1.25x slower                                         |
| deepcopy_reduce                 | 2.04 us                                                        | 2.59 us: 1.27x slower                                         |
| genshi_text                     | 16.2 ms                                                        | 20.8 ms: 1.28x slower                                         |
| coverage                        | 56.3 ms                                                        | 77.0 ms: 1.37x slower                                         |
| mako                            | 7.99 ms                                                        | 11.5 ms: 1.44x slower                                         |
| Geometric mean                  | (ref)                                                          | 1.08x slower                                                  |

- Geometric mean (including insignificant results): 1.069x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.48x
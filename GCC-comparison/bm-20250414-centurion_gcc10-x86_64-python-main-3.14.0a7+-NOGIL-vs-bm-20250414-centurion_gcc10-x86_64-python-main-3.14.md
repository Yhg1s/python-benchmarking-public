# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.041x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.50x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 196 ms                                                          | 206 ms: 1.05x slower                                           |
| docutils       | 2.05 sec                                                        | 2.13 sec: 1.04x slower                                         |
| html5lib       | 46.5 ms                                                         | 46.9 ms: 1.01x slower                                          |
| sphinx         | 780 ms                                                          | 817 ms: 1.05x slower                                           |
| Geometric mean | (ref)                                                           | 1.04x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_none_tg              | 220 ms                                                          | 177 ms: 1.25x faster                                           |
| async_tree_memoization_tg       | 277 ms                                                          | 236 ms: 1.18x faster                                           |
| async_tree_none                 | 236 ms                                                          | 207 ms: 1.14x faster                                           |
| async_tree_cpu_io_mixed_tg      | 416 ms                                                          | 371 ms: 1.12x faster                                           |
| async_tree_eager_memoization_tg | 240 ms                                                          | 216 ms: 1.11x faster                                           |
| async_tree_cpu_io_mixed         | 420 ms                                                          | 396 ms: 1.06x faster                                           |
| async_tree_memoization          | 274 ms                                                          | 261 ms: 1.05x faster                                           |
| coroutines                      | 15.0 ms                                                         | 14.4 ms: 1.05x faster                                          |
| async_tree_eager_cpu_io_mixed   | 319 ms                                                          | 322 ms: 1.01x slower                                           |
| async_generators                | 240 ms                                                          | 253 ms: 1.05x slower                                           |
| async_tree_eager                | 80.3 ms                                                         | 95.7 ms: 1.19x slower                                          |
| Geometric mean                  | (ref)                                                           | 1.06x faster                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| float          | 47.6 ms                                                         | 46.5 ms: 1.02x faster                                          |
| pidigits       | 185 ms                                                          | 181 ms: 1.02x faster                                           |
| Geometric mean | (ref)                                                           | 1.02x faster                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_v8       | 14.5 ms                                                         | 14.2 ms: 1.02x faster                                          |
| regex_dna      | 151 ms                                                          | 154 ms: 1.02x slower                                           |
| regex_compile  | 94.1 ms                                                         | 103 ms: 1.10x slower                                           |
| Geometric mean | (ref)                                                           | 1.03x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 68.9 ms                                                         | 58.2 ms: 1.18x faster                                          |
| xml_etree_parse      | 101 ms                                                          | 97.6 ms: 1.03x faster                                          |
| pickle_pure_python   | 230 us                                                          | 236 us: 1.02x slower                                           |
| unpickle_pure_python | 155 us                                                          | 159 us: 1.03x slower                                           |
| xml_etree_generate   | 67.2 ms                                                         | 69.6 ms: 1.04x slower                                          |
| xml_etree_process    | 48.3 ms                                                         | 50.5 ms: 1.05x slower                                          |
| tomli_loads          | 1.35 sec                                                        | 1.46 sec: 1.08x slower                                         |
| json_loads           | 18.4 us                                                         | 20.4 us: 1.11x slower                                          |
| json_dumps           | 7.56 ms                                                         | 8.40 ms: 1.11x slower                                          |
| Geometric mean       | (ref)                                                           | 1.02x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL |
|------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                         | 12.9 ms: 1.19x slower                                          |
| python_startup_no_site | 7.50 ms                                                         | 9.35 ms: 1.25x slower                                          |
| Geometric mean         | (ref)                                                           | 1.22x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL |
|-----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 39.3 ms                                                         | 42.7 ms: 1.09x slower                                          |
| django_template | 28.8 ms                                                         | 32.0 ms: 1.11x slower                                          |
| genshi_text     | 17.2 ms                                                         | 19.4 ms: 1.13x slower                                          |
| mako            | 7.47 ms                                                         | 10.9 ms: 1.46x slower                                          |
| Geometric mean  | (ref)                                                           | 1.19x slower                                                   |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc10-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal                    | 2.94 ms                                                         | 1.44 ms: 2.04x faster                                          |
| create_gc_cycles                | 1.68 ms                                                         | 1.10 ms: 1.53x faster                                          |
| async_tree_none_tg              | 220 ms                                                          | 177 ms: 1.25x faster                                           |
| xml_etree_iterparse             | 68.9 ms                                                         | 58.2 ms: 1.18x faster                                          |
| async_tree_memoization_tg       | 277 ms                                                          | 236 ms: 1.18x faster                                           |
| async_tree_none                 | 236 ms                                                          | 207 ms: 1.14x faster                                           |
| async_tree_cpu_io_mixed_tg      | 416 ms                                                          | 371 ms: 1.12x faster                                           |
| async_tree_eager_memoization_tg | 240 ms                                                          | 216 ms: 1.11x faster                                           |
| async_tree_cpu_io_mixed         | 420 ms                                                          | 396 ms: 1.06x faster                                           |
| async_tree_memoization          | 274 ms                                                          | 261 ms: 1.05x faster                                           |
| sqlite_synth                    | 1.61 us                                                         | 1.53 us: 1.05x faster                                          |
| coroutines                      | 15.0 ms                                                         | 14.4 ms: 1.05x faster                                          |
| xml_etree_parse                 | 101 ms                                                          | 97.6 ms: 1.03x faster                                          |
| pathlib                         | 12.6 ms                                                         | 12.3 ms: 1.03x faster                                          |
| float                           | 47.6 ms                                                         | 46.5 ms: 1.02x faster                                          |
| regex_v8                        | 14.5 ms                                                         | 14.2 ms: 1.02x faster                                          |
| pidigits                        | 185 ms                                                          | 181 ms: 1.02x faster                                           |
| raytrace                        | 211 ms                                                          | 212 ms: 1.01x slower                                           |
| html5lib                        | 46.5 ms                                                         | 46.9 ms: 1.01x slower                                          |
| async_tree_eager_cpu_io_mixed   | 319 ms                                                          | 322 ms: 1.01x slower                                           |
| bpe_tokeniser                   | 3.15 sec                                                        | 3.20 sec: 1.02x slower                                         |
| dulwich_log                     | 43.1 ms                                                         | 43.8 ms: 1.02x slower                                          |
| many_optionals                  | 734 us                                                          | 747 us: 1.02x slower                                           |
| regex_dna                       | 151 ms                                                          | 154 ms: 1.02x slower                                           |
| mdp                             | 937 ms                                                          | 956 ms: 1.02x slower                                           |
| subparsers                      | 17.6 ms                                                         | 18.0 ms: 1.02x slower                                          |
| pickle_pure_python              | 230 us                                                          | 236 us: 1.02x slower                                           |
| unpickle_pure_python            | 155 us                                                          | 159 us: 1.03x slower                                           |
| xml_etree_generate              | 67.2 ms                                                         | 69.6 ms: 1.04x slower                                          |
| docutils                        | 2.05 sec                                                        | 2.13 sec: 1.04x slower                                         |
| xml_etree_process               | 48.3 ms                                                         | 50.5 ms: 1.05x slower                                          |
| sqlglot_v2_optimize             | 39.0 ms                                                         | 40.8 ms: 1.05x slower                                          |
| sphinx                          | 780 ms                                                          | 817 ms: 1.05x slower                                           |
| deltablue                       | 2.35 ms                                                         | 2.46 ms: 1.05x slower                                          |
| 2to3                            | 196 ms                                                          | 206 ms: 1.05x slower                                           |
| sympy_sum                       | 105 ms                                                          | 110 ms: 1.05x slower                                           |
| async_generators                | 240 ms                                                          | 253 ms: 1.05x slower                                           |
| nqueens                         | 57.7 ms                                                         | 60.9 ms: 1.05x slower                                          |
| sqlglot_v2_normalize            | 79.0 ms                                                         | 83.4 ms: 1.05x slower                                          |
| json                            | 3.58 ms                                                         | 3.79 ms: 1.06x slower                                          |
| tomli_loads                     | 1.35 sec                                                        | 1.46 sec: 1.08x slower                                         |
| pyflate                         | 307 ms                                                          | 333 ms: 1.08x slower                                           |
| genshi_xml                      | 39.3 ms                                                         | 42.7 ms: 1.09x slower                                          |
| sympy_integrate                 | 14.8 ms                                                         | 16.3 ms: 1.10x slower                                          |
| sympy_str                       | 191 ms                                                          | 210 ms: 1.10x slower                                           |
| regex_compile                   | 94.1 ms                                                         | 103 ms: 1.10x slower                                           |
| comprehensions                  | 11.5 us                                                         | 12.6 us: 1.10x slower                                          |
| sympy_expand                    | 327 ms                                                          | 362 ms: 1.11x slower                                           |
| sqlglot_v2_transpile            | 1.13 ms                                                         | 1.25 ms: 1.11x slower                                          |
| sqlalchemy_imperative           | 14.3 ms                                                         | 15.8 ms: 1.11x slower                                          |
| json_loads                      | 18.4 us                                                         | 20.4 us: 1.11x slower                                          |
| sqlalchemy_declarative          | 98.7 ms                                                         | 109 ms: 1.11x slower                                           |
| django_template                 | 28.8 ms                                                         | 32.0 ms: 1.11x slower                                          |
| json_dumps                      | 7.56 ms                                                         | 8.40 ms: 1.11x slower                                          |
| hexiom                          | 4.09 ms                                                         | 4.56 ms: 1.11x slower                                          |
| pprint_safe_repr                | 476 ms                                                          | 532 ms: 1.12x slower                                           |
| deepcopy                        | 197 us                                                          | 220 us: 1.12x slower                                           |
| pprint_pformat                  | 989 ms                                                          | 1.11 sec: 1.12x slower                                         |
| genshi_text                     | 17.2 ms                                                         | 19.4 ms: 1.13x slower                                          |
| sqlglot_v2_parse                | 898 us                                                          | 1.03 ms: 1.14x slower                                          |
| connected_components            | 430 ms                                                          | 494 ms: 1.15x slower                                           |
| deepcopy_reduce                 | 2.05 us                                                         | 2.39 us: 1.16x slower                                          |
| richards                        | 31.3 ms                                                         | 36.6 ms: 1.17x slower                                          |
| meteor_contest                  | 86.3 ms                                                         | 101 ms: 1.17x slower                                           |
| crypto_pyaes                    | 52.1 ms                                                         | 61.1 ms: 1.17x slower                                          |
| shortest_path                   | 438 ms                                                          | 514 ms: 1.17x slower                                           |
| telco                           | 5.23 ms                                                         | 6.17 ms: 1.18x slower                                          |
| python_startup                  | 10.8 ms                                                         | 12.9 ms: 1.19x slower                                          |
| async_tree_eager                | 80.3 ms                                                         | 95.7 ms: 1.19x slower                                          |
| python_startup_no_site          | 7.50 ms                                                         | 9.35 ms: 1.25x slower                                          |
| deepcopy_memo                   | 18.2 us                                                         | 22.7 us: 1.25x slower                                          |
| typing_runtime_protocols        | 106 us                                                          | 135 us: 1.28x slower                                           |
| coverage                        | 58.0 ms                                                         | 77.5 ms: 1.34x slower                                          |
| mako                            | 7.47 ms                                                         | 10.9 ms: 1.46x slower                                          |
| Geometric mean                  | (ref)                                                           | 1.04x slower                                                   |

- Geometric mean (including insignificant results): 1.041x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.50x
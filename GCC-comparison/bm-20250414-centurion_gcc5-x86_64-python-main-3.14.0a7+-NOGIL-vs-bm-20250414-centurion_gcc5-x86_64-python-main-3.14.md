# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.158x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.48x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 197 ms                                                         | 242 ms: 1.23x slower                                          |
| docutils       | 1.94 sec                                                       | 2.21 sec: 1.14x slower                                        |
| html5lib       | 45.9 ms                                                        | 54.9 ms: 1.20x slower                                         |
| sphinx         | 757 ms                                                         | 880 ms: 1.16x slower                                          |
| Geometric mean | (ref)                                                          | 1.18x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL |
|-------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none_tg            | 223 ms                                                         | 198 ms: 1.12x faster                                          |
| async_tree_memoization_tg     | 280 ms                                                         | 268 ms: 1.05x faster                                          |
| async_tree_cpu_io_mixed_tg    | 405 ms                                                         | 396 ms: 1.02x faster                                          |
| async_tree_cpu_io_mixed       | 409 ms                                                         | 431 ms: 1.05x slower                                          |
| async_tree_memoization        | 277 ms                                                         | 302 ms: 1.09x slower                                          |
| async_tree_eager_cpu_io_mixed | 313 ms                                                         | 348 ms: 1.11x slower                                          |
| coroutines                    | 15.2 ms                                                        | 18.3 ms: 1.20x slower                                         |
| async_generators              | 218 ms                                                         | 272 ms: 1.25x slower                                          |
| async_tree_eager              | 86.6 ms                                                        | 118 ms: 1.36x slower                                          |
| Geometric mean                | (ref)                                                          | 1.07x slower                                                  |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| pidigits       | 189 ms                                                         | 185 ms: 1.02x faster                                          |
| float          | 47.4 ms                                                        | 59.3 ms: 1.25x slower                                         |
| Geometric mean | (ref)                                                          | 1.11x slower                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_v8       | 14.9 ms                                                        | 15.1 ms: 1.02x slower                                         |
| regex_dna      | 143 ms                                                         | 146 ms: 1.02x slower                                          |
| regex_compile  | 93.3 ms                                                        | 121 ms: 1.30x slower                                          |
| Geometric mean | (ref)                                                          | 1.10x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| xml_etree_iterparse  | 75.1 ms                                                        | 65.9 ms: 1.14x faster                                         |
| xml_etree_parse      | 90.5 ms                                                        | 92.3 ms: 1.02x slower                                         |
| json_loads           | 24.2 us                                                        | 26.6 us: 1.10x slower                                         |
| json_dumps           | 8.13 ms                                                        | 9.24 ms: 1.14x slower                                         |
| xml_etree_generate   | 64.9 ms                                                        | 74.9 ms: 1.16x slower                                         |
| xml_etree_process    | 45.9 ms                                                        | 55.2 ms: 1.20x slower                                         |
| unpickle_pure_python | 158 us                                                         | 198 us: 1.26x slower                                          |
| pickle_pure_python   | 232 us                                                         | 305 us: 1.31x slower                                          |
| tomli_loads          | 1.41 sec                                                       | 1.93 sec: 1.37x slower                                        |
| Geometric mean       | (ref)                                                          | 1.15x slower                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL |
|------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                        | 13.0 ms: 1.20x slower                                         |
| python_startup_no_site | 7.47 ms                                                        | 9.47 ms: 1.27x slower                                         |
| Geometric mean         | (ref)                                                          | 1.23x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL |
|-----------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| django_template | 28.0 ms                                                        | 37.8 ms: 1.35x slower                                         |
| genshi_xml      | 39.3 ms                                                        | 54.4 ms: 1.39x slower                                         |
| genshi_text     | 16.3 ms                                                        | 24.2 ms: 1.49x slower                                         |
| mako            | 7.79 ms                                                        | 12.7 ms: 1.63x slower                                         |
| Geometric mean  | (ref)                                                          | 1.46x slower                                                  |

All benchmarks:
===============

| Benchmark                     | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc5-x86_64-python-main-3.14.0a7+-NOGIL |
|-------------------------------|:--------------------------------------------------------------:|:-------------------------------------------------------------:|
| gc_traversal                  | 3.24 ms                                                        | 1.35 ms: 2.41x faster                                         |
| create_gc_cycles              | 1.79 ms                                                        | 1.16 ms: 1.54x faster                                         |
| xml_etree_iterparse           | 75.1 ms                                                        | 65.9 ms: 1.14x faster                                         |
| async_tree_none_tg            | 223 ms                                                         | 198 ms: 1.12x faster                                          |
| sqlite_synth                  | 1.68 us                                                        | 1.59 us: 1.05x faster                                         |
| async_tree_memoization_tg     | 280 ms                                                         | 268 ms: 1.05x faster                                          |
| async_tree_cpu_io_mixed_tg    | 405 ms                                                         | 396 ms: 1.02x faster                                          |
| pidigits                      | 189 ms                                                         | 185 ms: 1.02x faster                                          |
| regex_v8                      | 14.9 ms                                                        | 15.1 ms: 1.02x slower                                         |
| regex_dna                     | 143 ms                                                         | 146 ms: 1.02x slower                                          |
| xml_etree_parse               | 90.5 ms                                                        | 92.3 ms: 1.02x slower                                         |
| async_tree_cpu_io_mixed       | 409 ms                                                         | 431 ms: 1.05x slower                                          |
| pathlib                       | 13.2 ms                                                        | 14.0 ms: 1.06x slower                                         |
| json                          | 4.15 ms                                                        | 4.50 ms: 1.09x slower                                         |
| async_tree_memoization        | 277 ms                                                         | 302 ms: 1.09x slower                                          |
| json_loads                    | 24.2 us                                                        | 26.6 us: 1.10x slower                                         |
| bpe_tokeniser                 | 3.06 sec                                                       | 3.39 sec: 1.11x slower                                        |
| async_tree_eager_cpu_io_mixed | 313 ms                                                         | 348 ms: 1.11x slower                                          |
| json_dumps                    | 8.13 ms                                                        | 9.24 ms: 1.14x slower                                         |
| many_optionals                | 733 us                                                         | 836 us: 1.14x slower                                          |
| docutils                      | 1.94 sec                                                       | 2.21 sec: 1.14x slower                                        |
| xml_etree_generate            | 64.9 ms                                                        | 74.9 ms: 1.16x slower                                         |
| dulwich_log                   | 42.9 ms                                                        | 49.7 ms: 1.16x slower                                         |
| sphinx                        | 757 ms                                                         | 880 ms: 1.16x slower                                          |
| mdp                           | 939 ms                                                         | 1.10 sec: 1.17x slower                                        |
| subparsers                    | 17.9 ms                                                        | 21.1 ms: 1.18x slower                                         |
| connected_components          | 440 ms                                                         | 523 ms: 1.19x slower                                          |
| html5lib                      | 45.9 ms                                                        | 54.9 ms: 1.20x slower                                         |
| coroutines                    | 15.2 ms                                                        | 18.3 ms: 1.20x slower                                         |
| xml_etree_process             | 45.9 ms                                                        | 55.2 ms: 1.20x slower                                         |
| python_startup                | 10.8 ms                                                        | 13.0 ms: 1.20x slower                                         |
| shortest_path                 | 447 ms                                                         | 541 ms: 1.21x slower                                          |
| meteor_contest                | 86.0 ms                                                        | 104 ms: 1.21x slower                                          |
| sqlalchemy_imperative         | 14.2 ms                                                        | 17.2 ms: 1.21x slower                                         |
| sympy_sum                     | 104 ms                                                         | 127 ms: 1.21x slower                                          |
| pyflate                       | 313 ms                                                         | 381 ms: 1.22x slower                                          |
| sympy_integrate               | 14.8 ms                                                        | 18.1 ms: 1.23x slower                                         |
| 2to3                          | 197 ms                                                         | 242 ms: 1.23x slower                                          |
| sqlalchemy_declarative        | 95.8 ms                                                        | 118 ms: 1.23x slower                                          |
| async_generators              | 218 ms                                                         | 272 ms: 1.25x slower                                          |
| sympy_str                     | 195 ms                                                         | 243 ms: 1.25x slower                                          |
| sympy_expand                  | 336 ms                                                         | 419 ms: 1.25x slower                                          |
| float                         | 47.4 ms                                                        | 59.3 ms: 1.25x slower                                         |
| unpickle_pure_python          | 158 us                                                         | 198 us: 1.26x slower                                          |
| telco                         | 5.60 ms                                                        | 7.06 ms: 1.26x slower                                         |
| sqlglot_v2_optimize           | 38.3 ms                                                        | 48.4 ms: 1.26x slower                                         |
| python_startup_no_site        | 7.47 ms                                                        | 9.47 ms: 1.27x slower                                         |
| regex_compile                 | 93.3 ms                                                        | 121 ms: 1.30x slower                                          |
| crypto_pyaes                  | 57.4 ms                                                        | 74.6 ms: 1.30x slower                                         |
| sqlglot_v2_normalize          | 77.8 ms                                                        | 102 ms: 1.31x slower                                          |
| pickle_pure_python            | 232 us                                                         | 305 us: 1.31x slower                                          |
| sqlglot_v2_transpile          | 1.16 ms                                                        | 1.53 ms: 1.32x slower                                         |
| nqueens                       | 56.5 ms                                                        | 75.4 ms: 1.34x slower                                         |
| django_template               | 28.0 ms                                                        | 37.8 ms: 1.35x slower                                         |
| async_tree_eager              | 86.6 ms                                                        | 118 ms: 1.36x slower                                          |
| tomli_loads                   | 1.41 sec                                                       | 1.93 sec: 1.37x slower                                        |
| genshi_xml                    | 39.3 ms                                                        | 54.4 ms: 1.39x slower                                         |
| richards                      | 33.0 ms                                                        | 45.9 ms: 1.39x slower                                         |
| sqlglot_v2_parse              | 907 us                                                         | 1.27 ms: 1.40x slower                                         |
| pprint_pformat                | 1.04 sec                                                       | 1.47 sec: 1.40x slower                                        |
| raytrace                      | 184 ms                                                         | 259 ms: 1.41x slower                                          |
| deltablue                     | 2.21 ms                                                        | 3.13 ms: 1.42x slower                                         |
| pprint_safe_repr              | 504 ms                                                         | 715 ms: 1.42x slower                                          |
| deepcopy                      | 194 us                                                         | 276 us: 1.42x slower                                          |
| hexiom                        | 4.04 ms                                                        | 5.78 ms: 1.43x slower                                         |
| deepcopy_reduce               | 1.99 us                                                        | 2.85 us: 1.43x slower                                         |
| typing_runtime_protocols      | 109 us                                                         | 157 us: 1.44x slower                                          |
| coverage                      | 55.5 ms                                                        | 81.0 ms: 1.46x slower                                         |
| genshi_text                   | 16.3 ms                                                        | 24.2 ms: 1.49x slower                                         |
| deepcopy_memo                 | 18.8 us                                                        | 28.5 us: 1.52x slower                                         |
| comprehensions                | 10.6 us                                                        | 16.2 us: 1.52x slower                                         |
| mako                          | 7.79 ms                                                        | 12.7 ms: 1.63x slower                                         |
| Geometric mean                | (ref)                                                          | 1.19x slower                                                  |

Benchmark hidden because not significant (2): async_tree_eager_memoization_tg, async_tree_none

- Geometric mean (including insignificant results): 1.158x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.48x
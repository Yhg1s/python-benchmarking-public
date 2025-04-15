# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL
- machine: unknown-unknown
- commit hash: 7890b77
- commit date: 2025-04-14
- overall geometric mean: 1.104x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.50x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 193 ms                                                          | 219 ms: 1.13x slower                                           |
| docutils       | 2.02 sec                                                        | 2.19 sec: 1.08x slower                                         |
| html5lib       | 46.2 ms                                                         | 50.7 ms: 1.10x slower                                          |
| sphinx         | 775 ms                                                          | 846 ms: 1.09x slower                                           |
| Geometric mean | (ref)                                                           | 1.10x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_none_tg              | 218 ms                                                          | 187 ms: 1.17x faster                                           |
| async_tree_memoization_tg       | 274 ms                                                          | 248 ms: 1.10x faster                                           |
| async_tree_cpu_io_mixed_tg      | 417 ms                                                          | 396 ms: 1.05x faster                                           |
| async_tree_eager_memoization_tg | 237 ms                                                          | 226 ms: 1.05x faster                                           |
| async_tree_none                 | 233 ms                                                          | 222 ms: 1.05x faster                                           |
| async_tree_cpu_io_mixed         | 420 ms                                                          | 426 ms: 1.02x slower                                           |
| async_tree_memoization          | 269 ms                                                          | 278 ms: 1.03x slower                                           |
| async_tree_eager_cpu_io_mixed   | 323 ms                                                          | 339 ms: 1.05x slower                                           |
| async_generators                | 233 ms                                                          | 266 ms: 1.14x slower                                           |
| async_tree_eager                | 80.9 ms                                                         | 101 ms: 1.25x slower                                           |
| Geometric mean                  | (ref)                                                           | 1.01x slower                                                   |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 182 ms                                                          | 178 ms: 1.02x faster                                           |
| float          | 46.9 ms                                                         | 52.7 ms: 1.12x slower                                          |
| Geometric mean | (ref)                                                           | 1.05x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_dna      | 143 ms                                                          | 144 ms: 1.01x slower                                           |
| regex_v8       | 14.4 ms                                                         | 15.1 ms: 1.05x slower                                          |
| regex_compile  | 91.5 ms                                                         | 113 ms: 1.23x slower                                           |
| Geometric mean | (ref)                                                           | 1.09x slower                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 68.7 ms                                                         | 59.0 ms: 1.16x faster                                          |
| xml_etree_generate   | 67.0 ms                                                         | 73.1 ms: 1.09x slower                                          |
| xml_etree_process    | 48.5 ms                                                         | 53.4 ms: 1.10x slower                                          |
| json_loads           | 17.7 us                                                         | 19.5 us: 1.10x slower                                          |
| json_dumps           | 7.71 ms                                                         | 8.51 ms: 1.10x slower                                          |
| unpickle_pure_python | 159 us                                                          | 179 us: 1.13x slower                                           |
| pickle_pure_python   | 228 us                                                          | 268 us: 1.18x slower                                           |
| tomli_loads          | 1.37 sec                                                        | 1.67 sec: 1.22x slower                                         |
| Geometric mean       | (ref)                                                           | 1.08x slower                                                   |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL |
|------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                         | 12.8 ms: 1.19x slower                                          |
| python_startup_no_site | 7.50 ms                                                         | 9.37 ms: 1.25x slower                                          |
| Geometric mean         | (ref)                                                           | 1.22x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL |
|-----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| django_template | 28.8 ms                                                         | 33.8 ms: 1.17x slower                                          |
| genshi_xml      | 38.4 ms                                                         | 46.5 ms: 1.21x slower                                          |
| genshi_text     | 16.0 ms                                                         | 21.4 ms: 1.33x slower                                          |
| mako            | 7.56 ms                                                         | 11.6 ms: 1.54x slower                                          |
| Geometric mean  | (ref)                                                           | 1.31x slower                                                   |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc12-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal                    | 3.03 ms                                                         | 1.39 ms: 2.18x faster                                          |
| create_gc_cycles                | 1.75 ms                                                         | 1.16 ms: 1.51x faster                                          |
| async_tree_none_tg              | 218 ms                                                          | 187 ms: 1.17x faster                                           |
| xml_etree_iterparse             | 68.7 ms                                                         | 59.0 ms: 1.16x faster                                          |
| async_tree_memoization_tg       | 274 ms                                                          | 248 ms: 1.10x faster                                           |
| async_tree_cpu_io_mixed_tg      | 417 ms                                                          | 396 ms: 1.05x faster                                           |
| async_tree_eager_memoization_tg | 237 ms                                                          | 226 ms: 1.05x faster                                           |
| async_tree_none                 | 233 ms                                                          | 222 ms: 1.05x faster                                           |
| sqlite_synth                    | 1.57 us                                                         | 1.53 us: 1.03x faster                                          |
| pidigits                        | 182 ms                                                          | 178 ms: 1.02x faster                                           |
| pathlib                         | 12.6 ms                                                         | 12.6 ms: 1.01x faster                                          |
| json                            | 3.49 ms                                                         | 3.52 ms: 1.01x slower                                          |
| regex_dna                       | 143 ms                                                          | 144 ms: 1.01x slower                                           |
| async_tree_cpu_io_mixed         | 420 ms                                                          | 426 ms: 1.02x slower                                           |
| async_tree_memoization          | 269 ms                                                          | 278 ms: 1.03x slower                                           |
| regex_v8                        | 14.4 ms                                                         | 15.1 ms: 1.05x slower                                          |
| async_tree_eager_cpu_io_mixed   | 323 ms                                                          | 339 ms: 1.05x slower                                           |
| bpe_tokeniser                   | 3.11 sec                                                        | 3.31 sec: 1.06x slower                                         |
| many_optionals                  | 728 us                                                          | 778 us: 1.07x slower                                           |
| dulwich_log                     | 42.3 ms                                                         | 45.5 ms: 1.07x slower                                          |
| mdp                             | 929 ms                                                          | 1.00 sec: 1.08x slower                                         |
| docutils                        | 2.02 sec                                                        | 2.19 sec: 1.08x slower                                         |
| sphinx                          | 775 ms                                                          | 846 ms: 1.09x slower                                           |
| xml_etree_generate              | 67.0 ms                                                         | 73.1 ms: 1.09x slower                                          |
| html5lib                        | 46.2 ms                                                         | 50.7 ms: 1.10x slower                                          |
| xml_etree_process               | 48.5 ms                                                         | 53.4 ms: 1.10x slower                                          |
| json_loads                      | 17.7 us                                                         | 19.5 us: 1.10x slower                                          |
| subparsers                      | 17.2 ms                                                         | 19.0 ms: 1.10x slower                                          |
| json_dumps                      | 7.71 ms                                                         | 8.51 ms: 1.10x slower                                          |
| sympy_sum                       | 104 ms                                                          | 116 ms: 1.11x slower                                           |
| float                           | 46.9 ms                                                         | 52.7 ms: 1.12x slower                                          |
| unpickle_pure_python            | 159 us                                                          | 179 us: 1.13x slower                                           |
| 2to3                            | 193 ms                                                          | 219 ms: 1.13x slower                                           |
| sqlglot_v2_optimize             | 38.4 ms                                                         | 43.7 ms: 1.14x slower                                          |
| async_generators                | 233 ms                                                          | 266 ms: 1.14x slower                                           |
| sqlalchemy_declarative          | 97.5 ms                                                         | 112 ms: 1.15x slower                                           |
| sympy_integrate                 | 14.7 ms                                                         | 17.0 ms: 1.16x slower                                          |
| connected_components            | 429 ms                                                          | 496 ms: 1.16x slower                                           |
| sqlalchemy_imperative           | 14.2 ms                                                         | 16.4 ms: 1.16x slower                                          |
| sqlglot_v2_normalize            | 77.3 ms                                                         | 89.8 ms: 1.16x slower                                          |
| nqueens                         | 57.0 ms                                                         | 66.6 ms: 1.17x slower                                          |
| sympy_str                       | 190 ms                                                          | 222 ms: 1.17x slower                                           |
| shortest_path                   | 441 ms                                                          | 518 ms: 1.17x slower                                           |
| django_template                 | 28.8 ms                                                         | 33.8 ms: 1.17x slower                                          |
| pickle_pure_python              | 228 us                                                          | 268 us: 1.18x slower                                           |
| sympy_expand                    | 324 ms                                                          | 383 ms: 1.18x slower                                           |
| python_startup                  | 10.8 ms                                                         | 12.8 ms: 1.19x slower                                          |
| telco                           | 5.18 ms                                                         | 6.16 ms: 1.19x slower                                          |
| deepcopy_reduce                 | 2.05 us                                                         | 2.46 us: 1.20x slower                                          |
| meteor_contest                  | 84.2 ms                                                         | 101 ms: 1.20x slower                                           |
| genshi_xml                      | 38.4 ms                                                         | 46.5 ms: 1.21x slower                                          |
| comprehensions                  | 11.5 us                                                         | 14.1 us: 1.22x slower                                          |
| deepcopy                        | 191 us                                                          | 233 us: 1.22x slower                                           |
| tomli_loads                     | 1.37 sec                                                        | 1.67 sec: 1.22x slower                                         |
| sqlglot_v2_transpile            | 1.14 ms                                                         | 1.40 ms: 1.23x slower                                          |
| regex_compile                   | 91.5 ms                                                         | 113 ms: 1.23x slower                                           |
| pprint_safe_repr                | 487 ms                                                          | 601 ms: 1.23x slower                                           |
| pyflate                         | 297 ms                                                          | 368 ms: 1.24x slower                                           |
| crypto_pyaes                    | 53.0 ms                                                         | 66.0 ms: 1.25x slower                                          |
| python_startup_no_site          | 7.50 ms                                                         | 9.37 ms: 1.25x slower                                          |
| async_tree_eager                | 80.9 ms                                                         | 101 ms: 1.25x slower                                           |
| pprint_pformat                  | 996 ms                                                          | 1.26 sec: 1.26x slower                                         |
| raytrace                        | 190 ms                                                          | 242 ms: 1.28x slower                                           |
| deltablue                       | 2.21 ms                                                         | 2.86 ms: 1.29x slower                                          |
| sqlglot_v2_parse                | 887 us                                                          | 1.16 ms: 1.31x slower                                          |
| hexiom                          | 3.94 ms                                                         | 5.21 ms: 1.32x slower                                          |
| genshi_text                     | 16.0 ms                                                         | 21.4 ms: 1.33x slower                                          |
| typing_runtime_protocols        | 102 us                                                          | 140 us: 1.36x slower                                           |
| deepcopy_memo                   | 18.1 us                                                         | 25.4 us: 1.40x slower                                          |
| richards                        | 30.7 ms                                                         | 43.7 ms: 1.42x slower                                          |
| coverage                        | 54.9 ms                                                         | 78.3 ms: 1.42x slower                                          |
| mako                            | 7.56 ms                                                         | 11.6 ms: 1.54x slower                                          |
| Geometric mean                  | (ref)                                                           | 1.12x slower                                                   |

Benchmark hidden because not significant (2): xml_etree_parse, coroutines

- Geometric mean (including insignificant results): 1.104x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.50x
# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13
- machine: unknown-unknown
- commit hash: 7890b77
- commit date: 2025-04-14
- overall geometric mean: 1.070x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| 2to3           | 207 ms                                                   | 220 ms: 1.06x slower                                      |
| docutils       | 2.02 sec                                                 | 2.18 sec: 1.08x slower                                    |
| html5lib       | 47.1 ms                                                  | 50.4 ms: 1.07x slower                                     |
| sphinx         | 788 ms                                                   | 841 ms: 1.07x slower                                      |
| Geometric mean | (ref)                                                    | 1.07x slower                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| coroutines                      | 14.4 ms                                                  | 15.2 ms: 1.06x slower                                     |
| async_tree_eager_memoization_tg | 211 ms                                                   | 226 ms: 1.07x slower                                      |
| async_tree_eager                | 94.7 ms                                                  | 102 ms: 1.07x slower                                      |
| async_tree_none                 | 205 ms                                                   | 223 ms: 1.09x slower                                      |
| async_tree_memoization          | 254 ms                                                   | 280 ms: 1.10x slower                                      |
| async_tree_memoization_tg       | 227 ms                                                   | 251 ms: 1.11x slower                                      |
| async_generators                | 238 ms                                                   | 263 ms: 1.11x slower                                      |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 340 ms: 1.11x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 188 ms: 1.12x slower                                      |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 424 ms: 1.13x slower                                      |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 394 ms: 1.14x slower                                      |
| Geometric mean                  | (ref)                                                    | 1.10x slower                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| pidigits       | 181 ms                                                   | 179 ms: 1.01x faster                                      |
| float          | 46.5 ms                                                  | 53.6 ms: 1.15x slower                                     |
| Geometric mean | (ref)                                                    | 1.07x slower                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| regex_dna      | 158 ms                                                   | 146 ms: 1.08x faster                                      |
| regex_v8       | 14.9 ms                                                  | 15.6 ms: 1.04x slower                                     |
| regex_compile  | 102 ms                                                   | 114 ms: 1.12x slower                                      |
| Geometric mean | (ref)                                                    | 1.03x slower                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| xml_etree_iterparse  | 64.7 ms                                                  | 59.3 ms: 1.09x faster                                     |
| json_loads           | 19.5 us                                                  | 19.7 us: 1.01x slower                                     |
| xml_etree_parse      | 94.4 ms                                                  | 96.8 ms: 1.03x slower                                     |
| pickle_pure_python   | 243 us                                                   | 267 us: 1.10x slower                                      |
| tomli_loads          | 1.53 sec                                                 | 1.68 sec: 1.10x slower                                    |
| json_dumps           | 7.98 ms                                                  | 8.80 ms: 1.10x slower                                     |
| xml_etree_generate   | 64.9 ms                                                  | 75.1 ms: 1.16x slower                                     |
| xml_etree_process    | 46.6 ms                                                  | 54.6 ms: 1.17x slower                                     |
| unpickle_pure_python | 155 us                                                   | 183 us: 1.18x slower                                      |
| Geometric mean       | (ref)                                                    | 1.08x slower                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| python_startup_no_site | 9.52 ms                                                  | 9.38 ms: 1.01x faster                                     |
| python_startup         | 13.0 ms                                                  | 12.8 ms: 1.01x faster                                     |
| Geometric mean         | (ref)                                                    | 1.01x faster                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| mako            | 10.7 ms                                                  | 11.6 ms: 1.08x slower                                     |
| django_template | 30.8 ms                                                  | 34.3 ms: 1.11x slower                                     |
| genshi_xml      | 41.7 ms                                                  | 47.8 ms: 1.15x slower                                     |
| genshi_text     | 18.7 ms                                                  | 21.8 ms: 1.16x slower                                     |
| Geometric mean  | (ref)                                                    | 1.13x slower                                              |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc13 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| gc_traversal                    | 1.48 ms                                                  | 1.32 ms: 1.12x faster                                     |
| xml_etree_iterparse             | 64.7 ms                                                  | 59.3 ms: 1.09x faster                                     |
| regex_dna                       | 158 ms                                                   | 146 ms: 1.08x faster                                      |
| pathlib                         | 13.1 ms                                                  | 12.5 ms: 1.04x faster                                     |
| create_gc_cycles                | 1.16 ms                                                  | 1.14 ms: 1.02x faster                                     |
| python_startup_no_site          | 9.52 ms                                                  | 9.38 ms: 1.01x faster                                     |
| pidigits                        | 181 ms                                                   | 179 ms: 1.01x faster                                      |
| python_startup                  | 13.0 ms                                                  | 12.8 ms: 1.01x faster                                     |
| coverage                        | 78.4 ms                                                  | 77.7 ms: 1.01x faster                                     |
| json_loads                      | 19.5 us                                                  | 19.7 us: 1.01x slower                                     |
| sqlalchemy_imperative           | 16.2 ms                                                  | 16.4 ms: 1.02x slower                                     |
| telco                           | 6.04 ms                                                  | 6.14 ms: 1.02x slower                                     |
| xml_etree_parse                 | 94.4 ms                                                  | 96.8 ms: 1.03x slower                                     |
| sympy_integrate                 | 16.6 ms                                                  | 17.1 ms: 1.03x slower                                     |
| json                            | 3.48 ms                                                  | 3.58 ms: 1.03x slower                                     |
| dulwich_log                     | 45.2 ms                                                  | 46.6 ms: 1.03x slower                                     |
| shortest_path                   | 507 ms                                                   | 522 ms: 1.03x slower                                      |
| connected_components            | 486 ms                                                   | 501 ms: 1.03x slower                                      |
| meteor_contest                  | 97.9 ms                                                  | 102 ms: 1.04x slower                                      |
| sympy_sum                       | 112 ms                                                   | 116 ms: 1.04x slower                                      |
| sqlalchemy_declarative          | 109 ms                                                   | 114 ms: 1.04x slower                                      |
| sympy_str                       | 211 ms                                                   | 220 ms: 1.04x slower                                      |
| regex_v8                        | 14.9 ms                                                  | 15.6 ms: 1.04x slower                                     |
| sympy_expand                    | 360 ms                                                   | 377 ms: 1.05x slower                                      |
| many_optionals                  | 751 us                                                   | 787 us: 1.05x slower                                      |
| subparsers                      | 18.4 ms                                                  | 19.3 ms: 1.05x slower                                     |
| sqlite_synth                    | 1.47 us                                                  | 1.54 us: 1.05x slower                                     |
| bpe_tokeniser                   | 3.13 sec                                                 | 3.31 sec: 1.06x slower                                    |
| coroutines                      | 14.4 ms                                                  | 15.2 ms: 1.06x slower                                     |
| 2to3                            | 207 ms                                                   | 220 ms: 1.06x slower                                      |
| sphinx                          | 788 ms                                                   | 841 ms: 1.07x slower                                      |
| async_tree_eager_memoization_tg | 211 ms                                                   | 226 ms: 1.07x slower                                      |
| html5lib                        | 47.1 ms                                                  | 50.4 ms: 1.07x slower                                     |
| async_tree_eager                | 94.7 ms                                                  | 102 ms: 1.07x slower                                      |
| typing_runtime_protocols        | 132 us                                                   | 142 us: 1.07x slower                                      |
| mako                            | 10.7 ms                                                  | 11.6 ms: 1.08x slower                                     |
| docutils                        | 2.02 sec                                                 | 2.18 sec: 1.08x slower                                    |
| mdp                             | 925 ms                                                   | 1.00 sec: 1.09x slower                                    |
| async_tree_none                 | 205 ms                                                   | 223 ms: 1.09x slower                                      |
| pyflate                         | 339 ms                                                   | 372 ms: 1.10x slower                                      |
| pickle_pure_python              | 243 us                                                   | 267 us: 1.10x slower                                      |
| crypto_pyaes                    | 59.5 ms                                                  | 65.5 ms: 1.10x slower                                     |
| tomli_loads                     | 1.53 sec                                                 | 1.68 sec: 1.10x slower                                    |
| sqlglot_v2_optimize             | 39.7 ms                                                  | 43.7 ms: 1.10x slower                                     |
| async_tree_memoization          | 254 ms                                                   | 280 ms: 1.10x slower                                      |
| json_dumps                      | 7.98 ms                                                  | 8.80 ms: 1.10x slower                                     |
| nqueens                         | 61.6 ms                                                  | 68.1 ms: 1.10x slower                                     |
| async_tree_memoization_tg       | 227 ms                                                   | 251 ms: 1.11x slower                                      |
| async_generators                | 238 ms                                                   | 263 ms: 1.11x slower                                      |
| deepcopy                        | 211 us                                                   | 234 us: 1.11x slower                                      |
| raytrace                        | 217 ms                                                   | 241 ms: 1.11x slower                                      |
| django_template                 | 30.8 ms                                                  | 34.3 ms: 1.11x slower                                     |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 340 ms: 1.11x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 188 ms: 1.12x slower                                      |
| deepcopy_reduce                 | 2.23 us                                                  | 2.49 us: 1.12x slower                                     |
| sqlglot_v2_normalize            | 80.1 ms                                                  | 89.6 ms: 1.12x slower                                     |
| sqlglot_v2_transpile            | 1.26 ms                                                  | 1.41 ms: 1.12x slower                                     |
| regex_compile                   | 102 ms                                                   | 114 ms: 1.12x slower                                      |
| sqlglot_v2_parse                | 1.03 ms                                                  | 1.16 ms: 1.13x slower                                     |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 424 ms: 1.13x slower                                      |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 394 ms: 1.14x slower                                      |
| hexiom                          | 4.64 ms                                                  | 5.31 ms: 1.14x slower                                     |
| pprint_pformat                  | 1.12 sec                                                 | 1.28 sec: 1.14x slower                                    |
| genshi_xml                      | 41.7 ms                                                  | 47.8 ms: 1.15x slower                                     |
| float                           | 46.5 ms                                                  | 53.6 ms: 1.15x slower                                     |
| xml_etree_generate              | 64.9 ms                                                  | 75.1 ms: 1.16x slower                                     |
| pprint_safe_repr                | 530 ms                                                   | 614 ms: 1.16x slower                                      |
| genshi_text                     | 18.7 ms                                                  | 21.8 ms: 1.16x slower                                     |
| xml_etree_process               | 46.6 ms                                                  | 54.6 ms: 1.17x slower                                     |
| deltablue                       | 2.50 ms                                                  | 2.94 ms: 1.18x slower                                     |
| unpickle_pure_python            | 155 us                                                   | 183 us: 1.18x slower                                      |
| comprehensions                  | 11.9 us                                                  | 14.2 us: 1.19x slower                                     |
| deepcopy_memo                   | 21.4 us                                                  | 25.9 us: 1.21x slower                                     |
| richards                        | 36.1 ms                                                  | 45.7 ms: 1.26x slower                                     |
| Geometric mean                  | (ref)                                                    | 1.08x slower                                              |

- Geometric mean (including insignificant results): 1.070x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.98x
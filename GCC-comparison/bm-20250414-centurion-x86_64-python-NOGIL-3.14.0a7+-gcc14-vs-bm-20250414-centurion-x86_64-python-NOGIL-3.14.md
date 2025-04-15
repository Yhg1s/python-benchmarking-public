# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14
- machine: unknown-unknown
- commit hash: 7890b77
- commit date: 2025-04-14
- overall geometric mean: 1.077x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| 2to3           | 207 ms                                                   | 221 ms: 1.07x slower                                      |
| docutils       | 2.02 sec                                                 | 2.19 sec: 1.09x slower                                    |
| html5lib       | 47.1 ms                                                  | 50.5 ms: 1.07x slower                                     |
| sphinx         | 788 ms                                                   | 844 ms: 1.07x slower                                      |
| Geometric mean | (ref)                                                    | 1.07x slower                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| coroutines                      | 14.4 ms                                                  | 15.2 ms: 1.06x slower                                     |
| async_tree_eager_memoization_tg | 211 ms                                                   | 229 ms: 1.08x slower                                      |
| async_tree_eager                | 94.7 ms                                                  | 103 ms: 1.09x slower                                      |
| async_tree_none                 | 205 ms                                                   | 226 ms: 1.10x slower                                      |
| async_tree_memoization_tg       | 227 ms                                                   | 253 ms: 1.12x slower                                      |
| async_tree_memoization          | 254 ms                                                   | 287 ms: 1.13x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 191 ms: 1.13x slower                                      |
| async_generators                | 238 ms                                                   | 269 ms: 1.13x slower                                      |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 345 ms: 1.13x slower                                      |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 433 ms: 1.16x slower                                      |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 400 ms: 1.16x slower                                      |
| Geometric mean                  | (ref)                                                    | 1.12x slower                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| pidigits       | 181 ms                                                   | 179 ms: 1.01x faster                                      |
| float          | 46.5 ms                                                  | 55.0 ms: 1.18x slower                                     |
| Geometric mean | (ref)                                                    | 1.08x slower                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| regex_dna      | 158 ms                                                   | 146 ms: 1.08x faster                                      |
| regex_v8       | 14.9 ms                                                  | 15.5 ms: 1.04x slower                                     |
| regex_compile  | 102 ms                                                   | 113 ms: 1.11x slower                                      |
| Geometric mean | (ref)                                                    | 1.02x slower                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| xml_etree_iterparse  | 64.7 ms                                                  | 60.0 ms: 1.08x faster                                     |
| json_loads           | 19.5 us                                                  | 19.5 us: 1.00x slower                                     |
| xml_etree_parse      | 94.4 ms                                                  | 98.0 ms: 1.04x slower                                     |
| json_dumps           | 7.98 ms                                                  | 8.64 ms: 1.08x slower                                     |
| tomli_loads          | 1.53 sec                                                 | 1.72 sec: 1.13x slower                                    |
| pickle_pure_python   | 243 us                                                   | 278 us: 1.14x slower                                      |
| xml_etree_generate   | 64.9 ms                                                  | 75.1 ms: 1.16x slower                                     |
| xml_etree_process    | 46.6 ms                                                  | 54.4 ms: 1.17x slower                                     |
| unpickle_pure_python | 155 us                                                   | 187 us: 1.21x slower                                      |
| Geometric mean       | (ref)                                                    | 1.09x slower                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| python_startup_no_site | 9.52 ms                                                  | 9.41 ms: 1.01x faster                                     |
| python_startup         | 13.0 ms                                                  | 12.9 ms: 1.01x faster                                     |
| Geometric mean         | (ref)                                                    | 1.01x faster                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| mako            | 10.7 ms                                                  | 11.8 ms: 1.10x slower                                     |
| django_template | 30.8 ms                                                  | 34.8 ms: 1.13x slower                                     |
| genshi_xml      | 41.7 ms                                                  | 47.9 ms: 1.15x slower                                     |
| genshi_text     | 18.7 ms                                                  | 21.6 ms: 1.15x slower                                     |
| Geometric mean  | (ref)                                                    | 1.13x slower                                              |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc14 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| gc_traversal                    | 1.48 ms                                                  | 1.33 ms: 1.11x faster                                     |
| regex_dna                       | 158 ms                                                   | 146 ms: 1.08x faster                                      |
| xml_etree_iterparse             | 64.7 ms                                                  | 60.0 ms: 1.08x faster                                     |
| pathlib                         | 13.1 ms                                                  | 12.7 ms: 1.03x faster                                     |
| create_gc_cycles                | 1.16 ms                                                  | 1.14 ms: 1.02x faster                                     |
| pidigits                        | 181 ms                                                   | 179 ms: 1.01x faster                                      |
| python_startup_no_site          | 9.52 ms                                                  | 9.41 ms: 1.01x faster                                     |
| python_startup                  | 13.0 ms                                                  | 12.9 ms: 1.01x faster                                     |
| coverage                        | 78.4 ms                                                  | 77.8 ms: 1.01x faster                                     |
| json_loads                      | 19.5 us                                                  | 19.5 us: 1.00x slower                                     |
| sqlalchemy_imperative           | 16.2 ms                                                  | 16.4 ms: 1.01x slower                                     |
| dulwich_log                     | 45.2 ms                                                  | 46.2 ms: 1.02x slower                                     |
| telco                           | 6.04 ms                                                  | 6.23 ms: 1.03x slower                                     |
| regex_v8                        | 14.9 ms                                                  | 15.5 ms: 1.04x slower                                     |
| shortest_path                   | 507 ms                                                   | 526 ms: 1.04x slower                                      |
| xml_etree_parse                 | 94.4 ms                                                  | 98.0 ms: 1.04x slower                                     |
| json                            | 3.48 ms                                                  | 3.62 ms: 1.04x slower                                     |
| connected_components            | 486 ms                                                   | 505 ms: 1.04x slower                                      |
| subparsers                      | 18.4 ms                                                  | 19.1 ms: 1.04x slower                                     |
| sympy_integrate                 | 16.6 ms                                                  | 17.4 ms: 1.05x slower                                     |
| sympy_sum                       | 112 ms                                                   | 117 ms: 1.05x slower                                      |
| sympy_str                       | 211 ms                                                   | 222 ms: 1.05x slower                                      |
| sqlalchemy_declarative          | 109 ms                                                   | 115 ms: 1.05x slower                                      |
| many_optionals                  | 751 us                                                   | 792 us: 1.05x slower                                      |
| coroutines                      | 14.4 ms                                                  | 15.2 ms: 1.06x slower                                     |
| crypto_pyaes                    | 59.5 ms                                                  | 63.1 ms: 1.06x slower                                     |
| sympy_expand                    | 360 ms                                                   | 382 ms: 1.06x slower                                      |
| meteor_contest                  | 97.9 ms                                                  | 104 ms: 1.06x slower                                      |
| sqlite_synth                    | 1.47 us                                                  | 1.56 us: 1.07x slower                                     |
| 2to3                            | 207 ms                                                   | 221 ms: 1.07x slower                                      |
| sphinx                          | 788 ms                                                   | 844 ms: 1.07x slower                                      |
| html5lib                        | 47.1 ms                                                  | 50.5 ms: 1.07x slower                                     |
| typing_runtime_protocols        | 132 us                                                   | 142 us: 1.07x slower                                      |
| json_dumps                      | 7.98 ms                                                  | 8.64 ms: 1.08x slower                                     |
| async_tree_eager_memoization_tg | 211 ms                                                   | 229 ms: 1.08x slower                                      |
| docutils                        | 2.02 sec                                                 | 2.19 sec: 1.09x slower                                    |
| async_tree_eager                | 94.7 ms                                                  | 103 ms: 1.09x slower                                      |
| mdp                             | 925 ms                                                   | 1.01 sec: 1.09x slower                                    |
| nqueens                         | 61.6 ms                                                  | 67.5 ms: 1.10x slower                                     |
| mako                            | 10.7 ms                                                  | 11.8 ms: 1.10x slower                                     |
| async_tree_none                 | 205 ms                                                   | 226 ms: 1.10x slower                                      |
| sqlglot_v2_normalize            | 80.1 ms                                                  | 89.1 ms: 1.11x slower                                     |
| regex_compile                   | 102 ms                                                   | 113 ms: 1.11x slower                                      |
| sqlglot_v2_optimize             | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                     |
| async_tree_memoization_tg       | 227 ms                                                   | 253 ms: 1.12x slower                                      |
| bpe_tokeniser                   | 3.13 sec                                                 | 3.50 sec: 1.12x slower                                    |
| pyflate                         | 339 ms                                                   | 380 ms: 1.12x slower                                      |
| sqlglot_v2_parse                | 1.03 ms                                                  | 1.15 ms: 1.12x slower                                     |
| sqlglot_v2_transpile            | 1.26 ms                                                  | 1.41 ms: 1.12x slower                                     |
| deepcopy                        | 211 us                                                   | 237 us: 1.12x slower                                      |
| tomli_loads                     | 1.53 sec                                                 | 1.72 sec: 1.13x slower                                    |
| async_tree_memoization          | 254 ms                                                   | 287 ms: 1.13x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 191 ms: 1.13x slower                                      |
| django_template                 | 30.8 ms                                                  | 34.8 ms: 1.13x slower                                     |
| async_generators                | 238 ms                                                   | 269 ms: 1.13x slower                                      |
| raytrace                        | 217 ms                                                   | 245 ms: 1.13x slower                                      |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 345 ms: 1.13x slower                                      |
| deepcopy_reduce                 | 2.23 us                                                  | 2.55 us: 1.14x slower                                     |
| pickle_pure_python              | 243 us                                                   | 278 us: 1.14x slower                                      |
| pprint_safe_repr                | 530 ms                                                   | 607 ms: 1.15x slower                                      |
| pprint_pformat                  | 1.12 sec                                                 | 1.28 sec: 1.15x slower                                    |
| genshi_xml                      | 41.7 ms                                                  | 47.9 ms: 1.15x slower                                     |
| hexiom                          | 4.64 ms                                                  | 5.34 ms: 1.15x slower                                     |
| genshi_text                     | 18.7 ms                                                  | 21.6 ms: 1.15x slower                                     |
| xml_etree_generate              | 64.9 ms                                                  | 75.1 ms: 1.16x slower                                     |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 433 ms: 1.16x slower                                      |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 400 ms: 1.16x slower                                      |
| xml_etree_process               | 46.6 ms                                                  | 54.4 ms: 1.17x slower                                     |
| float                           | 46.5 ms                                                  | 55.0 ms: 1.18x slower                                     |
| deltablue                       | 2.50 ms                                                  | 2.98 ms: 1.19x slower                                     |
| comprehensions                  | 11.9 us                                                  | 14.3 us: 1.20x slower                                     |
| richards                        | 36.1 ms                                                  | 43.5 ms: 1.20x slower                                     |
| deepcopy_memo                   | 21.4 us                                                  | 25.8 us: 1.21x slower                                     |
| unpickle_pure_python            | 155 us                                                   | 187 us: 1.21x slower                                      |
| Geometric mean                  | (ref)                                                    | 1.08x slower                                              |

- Geometric mean (including insignificant results): 1.077x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.98x
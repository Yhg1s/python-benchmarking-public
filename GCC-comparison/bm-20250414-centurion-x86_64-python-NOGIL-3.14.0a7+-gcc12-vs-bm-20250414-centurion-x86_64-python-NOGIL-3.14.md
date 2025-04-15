# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12
- machine: unknown-unknown
- commit hash: 7890b77
- commit date: 2025-04-14
- overall geometric mean: 1.065x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| 2to3           | 207 ms                                                   | 219 ms: 1.06x slower                                      |
| docutils       | 2.02 sec                                                 | 2.19 sec: 1.09x slower                                    |
| html5lib       | 47.1 ms                                                  | 50.7 ms: 1.08x slower                                     |
| sphinx         | 788 ms                                                   | 846 ms: 1.07x slower                                      |
| Geometric mean | (ref)                                                    | 1.07x slower                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| coroutines                      | 14.4 ms                                                  | 15.0 ms: 1.04x slower                                     |
| async_tree_eager                | 94.7 ms                                                  | 101 ms: 1.07x slower                                      |
| async_tree_eager_memoization_tg | 211 ms                                                   | 226 ms: 1.07x slower                                      |
| async_tree_none                 | 205 ms                                                   | 222 ms: 1.09x slower                                      |
| async_tree_memoization          | 254 ms                                                   | 278 ms: 1.09x slower                                      |
| async_tree_memoization_tg       | 227 ms                                                   | 248 ms: 1.10x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 187 ms: 1.11x slower                                      |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 339 ms: 1.11x slower                                      |
| async_generators                | 238 ms                                                   | 266 ms: 1.12x slower                                      |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 426 ms: 1.14x slower                                      |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 396 ms: 1.15x slower                                      |
| Geometric mean                  | (ref)                                                    | 1.10x slower                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| pidigits       | 181 ms                                                   | 178 ms: 1.02x faster                                      |
| float          | 46.5 ms                                                  | 52.7 ms: 1.13x slower                                     |
| Geometric mean | (ref)                                                    | 1.06x slower                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| regex_dna      | 158 ms                                                   | 144 ms: 1.10x faster                                      |
| regex_v8       | 14.9 ms                                                  | 15.1 ms: 1.01x slower                                     |
| regex_compile  | 102 ms                                                   | 113 ms: 1.11x slower                                      |
| Geometric mean | (ref)                                                    | 1.01x slower                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| xml_etree_iterparse  | 64.7 ms                                                  | 59.0 ms: 1.10x faster                                     |
| json_loads           | 19.5 us                                                  | 19.5 us: 1.00x slower                                     |
| xml_etree_parse      | 94.4 ms                                                  | 97.8 ms: 1.04x slower                                     |
| json_dumps           | 7.98 ms                                                  | 8.51 ms: 1.07x slower                                     |
| tomli_loads          | 1.53 sec                                                 | 1.67 sec: 1.10x slower                                    |
| pickle_pure_python   | 243 us                                                   | 268 us: 1.10x slower                                      |
| xml_etree_generate   | 64.9 ms                                                  | 73.1 ms: 1.13x slower                                     |
| xml_etree_process    | 46.6 ms                                                  | 53.4 ms: 1.15x slower                                     |
| unpickle_pure_python | 155 us                                                   | 179 us: 1.16x slower                                      |
| Geometric mean       | (ref)                                                    | 1.07x slower                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| python_startup_no_site | 9.52 ms                                                  | 9.37 ms: 1.02x faster                                     |
| python_startup         | 13.0 ms                                                  | 12.8 ms: 1.01x faster                                     |
| Geometric mean         | (ref)                                                    | 1.01x faster                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| mako            | 10.7 ms                                                  | 11.6 ms: 1.09x slower                                     |
| django_template | 30.8 ms                                                  | 33.8 ms: 1.10x slower                                     |
| genshi_xml      | 41.7 ms                                                  | 46.5 ms: 1.12x slower                                     |
| genshi_text     | 18.7 ms                                                  | 21.4 ms: 1.14x slower                                     |
| Geometric mean  | (ref)                                                    | 1.11x slower                                              |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc12 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| xml_etree_iterparse             | 64.7 ms                                                  | 59.0 ms: 1.10x faster                                     |
| regex_dna                       | 158 ms                                                   | 144 ms: 1.10x faster                                      |
| gc_traversal                    | 1.48 ms                                                  | 1.39 ms: 1.06x faster                                     |
| pathlib                         | 13.1 ms                                                  | 12.6 ms: 1.04x faster                                     |
| python_startup_no_site          | 9.52 ms                                                  | 9.37 ms: 1.02x faster                                     |
| pidigits                        | 181 ms                                                   | 178 ms: 1.02x faster                                      |
| python_startup                  | 13.0 ms                                                  | 12.8 ms: 1.01x faster                                     |
| json_loads                      | 19.5 us                                                  | 19.5 us: 1.00x slower                                     |
| dulwich_log                     | 45.2 ms                                                  | 45.5 ms: 1.01x slower                                     |
| json                            | 3.48 ms                                                  | 3.52 ms: 1.01x slower                                     |
| regex_v8                        | 14.9 ms                                                  | 15.1 ms: 1.01x slower                                     |
| sqlalchemy_imperative           | 16.2 ms                                                  | 16.4 ms: 1.01x slower                                     |
| telco                           | 6.04 ms                                                  | 6.16 ms: 1.02x slower                                     |
| connected_components            | 486 ms                                                   | 496 ms: 1.02x slower                                      |
| shortest_path                   | 507 ms                                                   | 518 ms: 1.02x slower                                      |
| sqlalchemy_declarative          | 109 ms                                                   | 112 ms: 1.02x slower                                      |
| sympy_integrate                 | 16.6 ms                                                  | 17.0 ms: 1.03x slower                                     |
| subparsers                      | 18.4 ms                                                  | 19.0 ms: 1.03x slower                                     |
| meteor_contest                  | 97.9 ms                                                  | 101 ms: 1.03x slower                                      |
| xml_etree_parse                 | 94.4 ms                                                  | 97.8 ms: 1.04x slower                                     |
| many_optionals                  | 751 us                                                   | 778 us: 1.04x slower                                      |
| sympy_sum                       | 112 ms                                                   | 116 ms: 1.04x slower                                      |
| sqlite_synth                    | 1.47 us                                                  | 1.53 us: 1.04x slower                                     |
| coroutines                      | 14.4 ms                                                  | 15.0 ms: 1.04x slower                                     |
| sympy_str                       | 211 ms                                                   | 222 ms: 1.05x slower                                      |
| typing_runtime_protocols        | 132 us                                                   | 140 us: 1.05x slower                                      |
| bpe_tokeniser                   | 3.13 sec                                                 | 3.31 sec: 1.06x slower                                    |
| 2to3                            | 207 ms                                                   | 219 ms: 1.06x slower                                      |
| sympy_expand                    | 360 ms                                                   | 383 ms: 1.06x slower                                      |
| json_dumps                      | 7.98 ms                                                  | 8.51 ms: 1.07x slower                                     |
| async_tree_eager                | 94.7 ms                                                  | 101 ms: 1.07x slower                                      |
| async_tree_eager_memoization_tg | 211 ms                                                   | 226 ms: 1.07x slower                                      |
| sphinx                          | 788 ms                                                   | 846 ms: 1.07x slower                                      |
| html5lib                        | 47.1 ms                                                  | 50.7 ms: 1.08x slower                                     |
| nqueens                         | 61.6 ms                                                  | 66.6 ms: 1.08x slower                                     |
| pyflate                         | 339 ms                                                   | 368 ms: 1.08x slower                                      |
| mdp                             | 925 ms                                                   | 1.00 sec: 1.09x slower                                    |
| async_tree_none                 | 205 ms                                                   | 222 ms: 1.09x slower                                      |
| docutils                        | 2.02 sec                                                 | 2.19 sec: 1.09x slower                                    |
| mako                            | 10.7 ms                                                  | 11.6 ms: 1.09x slower                                     |
| async_tree_memoization          | 254 ms                                                   | 278 ms: 1.09x slower                                      |
| async_tree_memoization_tg       | 227 ms                                                   | 248 ms: 1.10x slower                                      |
| tomli_loads                     | 1.53 sec                                                 | 1.67 sec: 1.10x slower                                    |
| django_template                 | 30.8 ms                                                  | 33.8 ms: 1.10x slower                                     |
| sqlglot_v2_optimize             | 39.7 ms                                                  | 43.7 ms: 1.10x slower                                     |
| deepcopy_reduce                 | 2.23 us                                                  | 2.46 us: 1.10x slower                                     |
| pickle_pure_python              | 243 us                                                   | 268 us: 1.10x slower                                      |
| deepcopy                        | 211 us                                                   | 233 us: 1.10x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 187 ms: 1.11x slower                                      |
| crypto_pyaes                    | 59.5 ms                                                  | 66.0 ms: 1.11x slower                                     |
| regex_compile                   | 102 ms                                                   | 113 ms: 1.11x slower                                      |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 339 ms: 1.11x slower                                      |
| sqlglot_v2_transpile            | 1.26 ms                                                  | 1.40 ms: 1.11x slower                                     |
| genshi_xml                      | 41.7 ms                                                  | 46.5 ms: 1.12x slower                                     |
| raytrace                        | 217 ms                                                   | 242 ms: 1.12x slower                                      |
| async_generators                | 238 ms                                                   | 266 ms: 1.12x slower                                      |
| sqlglot_v2_normalize            | 80.1 ms                                                  | 89.8 ms: 1.12x slower                                     |
| hexiom                          | 4.64 ms                                                  | 5.21 ms: 1.12x slower                                     |
| xml_etree_generate              | 64.9 ms                                                  | 73.1 ms: 1.13x slower                                     |
| pprint_pformat                  | 1.12 sec                                                 | 1.26 sec: 1.13x slower                                    |
| sqlglot_v2_parse                | 1.03 ms                                                  | 1.16 ms: 1.13x slower                                     |
| pprint_safe_repr                | 530 ms                                                   | 601 ms: 1.13x slower                                      |
| float                           | 46.5 ms                                                  | 52.7 ms: 1.13x slower                                     |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 426 ms: 1.14x slower                                      |
| deltablue                       | 2.50 ms                                                  | 2.86 ms: 1.14x slower                                     |
| genshi_text                     | 18.7 ms                                                  | 21.4 ms: 1.14x slower                                     |
| xml_etree_process               | 46.6 ms                                                  | 53.4 ms: 1.15x slower                                     |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 396 ms: 1.15x slower                                      |
| unpickle_pure_python            | 155 us                                                   | 179 us: 1.16x slower                                      |
| comprehensions                  | 11.9 us                                                  | 14.1 us: 1.18x slower                                     |
| deepcopy_memo                   | 21.4 us                                                  | 25.4 us: 1.19x slower                                     |
| richards                        | 36.1 ms                                                  | 43.7 ms: 1.21x slower                                     |
| Geometric mean                  | (ref)                                                    | 1.07x slower                                              |

Benchmark hidden because not significant (2): coverage, create_gc_cycles

- Geometric mean (including insignificant results): 1.065x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 0.99x
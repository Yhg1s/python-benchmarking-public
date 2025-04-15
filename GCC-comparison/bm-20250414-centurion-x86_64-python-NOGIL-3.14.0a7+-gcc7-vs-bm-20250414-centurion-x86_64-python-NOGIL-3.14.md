# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.050x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 207 ms                                                   | 219 ms: 1.06x slower                                     |
| docutils       | 2.02 sec                                                 | 2.09 sec: 1.04x slower                                   |
| html5lib       | 47.1 ms                                                  | 48.1 ms: 1.02x slower                                    |
| sphinx         | 788 ms                                                   | 828 ms: 1.05x slower                                     |
| Geometric mean | (ref)                                                    | 1.04x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7 |
|---------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| async_generators                | 238 ms                                                   | 246 ms: 1.03x slower                                     |
| async_tree_none_tg              | 169 ms                                                   | 175 ms: 1.03x slower                                     |
| async_tree_memoization_tg       | 227 ms                                                   | 236 ms: 1.04x slower                                     |
| async_tree_none                 | 205 ms                                                   | 215 ms: 1.05x slower                                     |
| async_tree_eager_memoization_tg | 211 ms                                                   | 222 ms: 1.05x slower                                     |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 363 ms: 1.05x slower                                     |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 398 ms: 1.06x slower                                     |
| async_tree_memoization          | 254 ms                                                   | 271 ms: 1.07x slower                                     |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 328 ms: 1.07x slower                                     |
| coroutines                      | 14.4 ms                                                  | 15.6 ms: 1.08x slower                                    |
| async_tree_eager                | 94.7 ms                                                  | 107 ms: 1.13x slower                                     |
| Geometric mean                  | (ref)                                                    | 1.06x slower                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 181 ms                                                   | 186 ms: 1.02x slower                                     |
| float          | 46.5 ms                                                  | 52.2 ms: 1.12x slower                                    |
| Geometric mean | (ref)                                                    | 1.07x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7 |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 158 ms                                                   | 142 ms: 1.11x faster                                     |
| regex_v8       | 14.9 ms                                                  | 14.7 ms: 1.01x faster                                    |
| regex_compile  | 102 ms                                                   | 107 ms: 1.05x slower                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7 |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_parse      | 94.4 ms                                                  | 91.4 ms: 1.03x faster                                    |
| xml_etree_iterparse  | 64.7 ms                                                  | 63.6 ms: 1.02x faster                                    |
| pickle_pure_python   | 243 us                                                   | 259 us: 1.07x slower                                     |
| unpickle_pure_python | 155 us                                                   | 171 us: 1.10x slower                                     |
| xml_etree_generate   | 64.9 ms                                                  | 72.0 ms: 1.11x slower                                    |
| xml_etree_process    | 46.6 ms                                                  | 52.0 ms: 1.12x slower                                    |
| json_dumps           | 7.98 ms                                                  | 9.19 ms: 1.15x slower                                    |
| json_loads           | 19.5 us                                                  | 22.7 us: 1.17x slower                                    |
| Geometric mean       | (ref)                                                    | 1.07x slower                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7 |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 9.52 ms                                                  | 9.55 ms: 1.00x slower                                    |
| python_startup         | 13.0 ms                                                  | 13.0 ms: 1.00x slower                                    |
| Geometric mean         | (ref)                                                    | 1.00x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7 |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| django_template | 30.8 ms                                                  | 32.5 ms: 1.06x slower                                    |
| mako            | 10.7 ms                                                  | 11.5 ms: 1.07x slower                                    |
| genshi_text     | 18.7 ms                                                  | 20.8 ms: 1.11x slower                                    |
| genshi_xml      | 41.7 ms                                                  | 46.3 ms: 1.11x slower                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                             |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc7 |
|---------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna                       | 158 ms                                                   | 142 ms: 1.11x faster                                     |
| gc_traversal                    | 1.48 ms                                                  | 1.39 ms: 1.06x faster                                    |
| xml_etree_parse                 | 94.4 ms                                                  | 91.4 ms: 1.03x faster                                    |
| pyflate                         | 339 ms                                                   | 329 ms: 1.03x faster                                     |
| xml_etree_iterparse             | 64.7 ms                                                  | 63.6 ms: 1.02x faster                                    |
| coverage                        | 78.4 ms                                                  | 77.0 ms: 1.02x faster                                    |
| regex_v8                        | 14.9 ms                                                  | 14.7 ms: 1.01x faster                                    |
| meteor_contest                  | 97.9 ms                                                  | 97.3 ms: 1.01x faster                                    |
| python_startup_no_site          | 9.52 ms                                                  | 9.55 ms: 1.00x slower                                    |
| connected_components            | 486 ms                                                   | 488 ms: 1.00x slower                                     |
| python_startup                  | 13.0 ms                                                  | 13.0 ms: 1.00x slower                                    |
| create_gc_cycles                | 1.16 ms                                                  | 1.17 ms: 1.01x slower                                    |
| shortest_path                   | 507 ms                                                   | 513 ms: 1.01x slower                                     |
| deltablue                       | 2.50 ms                                                  | 2.53 ms: 1.01x slower                                    |
| raytrace                        | 217 ms                                                   | 220 ms: 1.01x slower                                     |
| pathlib                         | 13.1 ms                                                  | 13.3 ms: 1.01x slower                                    |
| sqlalchemy_imperative           | 16.2 ms                                                  | 16.5 ms: 1.02x slower                                    |
| sympy_integrate                 | 16.6 ms                                                  | 16.9 ms: 1.02x slower                                    |
| sqlalchemy_declarative          | 109 ms                                                   | 112 ms: 1.02x slower                                     |
| html5lib                        | 47.1 ms                                                  | 48.1 ms: 1.02x slower                                    |
| pidigits                        | 181 ms                                                   | 186 ms: 1.02x slower                                     |
| hexiom                          | 4.64 ms                                                  | 4.76 ms: 1.03x slower                                    |
| nqueens                         | 61.6 ms                                                  | 63.4 ms: 1.03x slower                                    |
| async_generators                | 238 ms                                                   | 246 ms: 1.03x slower                                     |
| async_tree_none_tg              | 169 ms                                                   | 175 ms: 1.03x slower                                     |
| docutils                        | 2.02 sec                                                 | 2.09 sec: 1.04x slower                                   |
| bpe_tokeniser                   | 3.13 sec                                                 | 3.26 sec: 1.04x slower                                   |
| async_tree_memoization_tg       | 227 ms                                                   | 236 ms: 1.04x slower                                     |
| regex_compile                   | 102 ms                                                   | 107 ms: 1.05x slower                                     |
| async_tree_none                 | 205 ms                                                   | 215 ms: 1.05x slower                                     |
| async_tree_eager_memoization_tg | 211 ms                                                   | 222 ms: 1.05x slower                                     |
| sphinx                          | 788 ms                                                   | 828 ms: 1.05x slower                                     |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 363 ms: 1.05x slower                                     |
| dulwich_log                     | 45.2 ms                                                  | 47.6 ms: 1.05x slower                                    |
| deepcopy_memo                   | 21.4 us                                                  | 22.5 us: 1.05x slower                                    |
| django_template                 | 30.8 ms                                                  | 32.5 ms: 1.06x slower                                    |
| many_optionals                  | 751 us                                                   | 794 us: 1.06x slower                                     |
| richards                        | 36.1 ms                                                  | 38.2 ms: 1.06x slower                                    |
| 2to3                            | 207 ms                                                   | 219 ms: 1.06x slower                                     |
| sqlglot_v2_transpile            | 1.26 ms                                                  | 1.34 ms: 1.06x slower                                    |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 398 ms: 1.06x slower                                     |
| async_tree_memoization          | 254 ms                                                   | 271 ms: 1.07x slower                                     |
| pickle_pure_python              | 243 us                                                   | 259 us: 1.07x slower                                     |
| pprint_pformat                  | 1.12 sec                                                 | 1.19 sec: 1.07x slower                                   |
| sqlglot_v2_parse                | 1.03 ms                                                  | 1.10 ms: 1.07x slower                                    |
| subparsers                      | 18.4 ms                                                  | 19.7 ms: 1.07x slower                                    |
| sympy_str                       | 211 ms                                                   | 226 ms: 1.07x slower                                     |
| sympy_sum                       | 112 ms                                                   | 119 ms: 1.07x slower                                     |
| comprehensions                  | 11.9 us                                                  | 12.8 us: 1.07x slower                                    |
| mako                            | 10.7 ms                                                  | 11.5 ms: 1.07x slower                                    |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 328 ms: 1.07x slower                                     |
| pprint_safe_repr                | 530 ms                                                   | 571 ms: 1.08x slower                                     |
| typing_runtime_protocols        | 132 us                                                   | 143 us: 1.08x slower                                     |
| coroutines                      | 14.4 ms                                                  | 15.6 ms: 1.08x slower                                    |
| sympy_expand                    | 360 ms                                                   | 391 ms: 1.09x slower                                     |
| mdp                             | 925 ms                                                   | 1.01 sec: 1.09x slower                                   |
| sqlglot_v2_optimize             | 39.7 ms                                                  | 43.4 ms: 1.09x slower                                    |
| unpickle_pure_python            | 155 us                                                   | 171 us: 1.10x slower                                     |
| xml_etree_generate              | 64.9 ms                                                  | 72.0 ms: 1.11x slower                                    |
| json                            | 3.48 ms                                                  | 3.87 ms: 1.11x slower                                    |
| genshi_text                     | 18.7 ms                                                  | 20.8 ms: 1.11x slower                                    |
| genshi_xml                      | 41.7 ms                                                  | 46.3 ms: 1.11x slower                                    |
| sqlglot_v2_normalize            | 80.1 ms                                                  | 89.2 ms: 1.11x slower                                    |
| xml_etree_process               | 46.6 ms                                                  | 52.0 ms: 1.12x slower                                    |
| float                           | 46.5 ms                                                  | 52.2 ms: 1.12x slower                                    |
| async_tree_eager                | 94.7 ms                                                  | 107 ms: 1.13x slower                                     |
| sqlite_synth                    | 1.47 us                                                  | 1.66 us: 1.13x slower                                    |
| crypto_pyaes                    | 59.5 ms                                                  | 67.4 ms: 1.13x slower                                    |
| deepcopy                        | 211 us                                                   | 240 us: 1.14x slower                                     |
| json_dumps                      | 7.98 ms                                                  | 9.19 ms: 1.15x slower                                    |
| deepcopy_reduce                 | 2.23 us                                                  | 2.59 us: 1.16x slower                                    |
| json_loads                      | 19.5 us                                                  | 22.7 us: 1.17x slower                                    |
| telco                           | 6.04 ms                                                  | 7.09 ms: 1.17x slower                                    |
| Geometric mean                  | (ref)                                                    | 1.05x slower                                             |

Benchmark hidden because not significant (1): tomli_loads

- Geometric mean (including insignificant results): 1.050x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.00x
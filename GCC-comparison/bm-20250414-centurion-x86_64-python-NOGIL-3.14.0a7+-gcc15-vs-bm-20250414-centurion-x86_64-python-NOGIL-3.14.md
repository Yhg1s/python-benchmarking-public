# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15
- machine: unknown-unknown
- commit hash: 7890b77
- commit date: 2025-04-14
- overall geometric mean: 1.008x faster
- HPT reliability: 93.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| 2to3           | 207 ms                                                   | 203 ms: 1.02x faster                                      |
| docutils       | 2.02 sec                                                 | 2.09 sec: 1.04x slower                                    |
| html5lib       | 47.1 ms                                                  | 45.8 ms: 1.03x faster                                     |
| sphinx         | 788 ms                                                   | 799 ms: 1.01x slower                                      |
| Geometric mean | (ref)                                                    | 1.00x slower                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| coroutines                      | 14.4 ms                                                  | 13.7 ms: 1.05x faster                                     |
| async_tree_eager                | 94.7 ms                                                  | 91.7 ms: 1.03x faster                                     |
| async_tree_eager_memoization_tg | 211 ms                                                   | 208 ms: 1.01x faster                                      |
| async_tree_none                 | 205 ms                                                   | 202 ms: 1.01x faster                                      |
| async_tree_memoization_tg       | 227 ms                                                   | 229 ms: 1.01x slower                                      |
| async_tree_memoization          | 254 ms                                                   | 257 ms: 1.01x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 172 ms: 1.02x slower                                      |
| async_generators                | 238 ms                                                   | 254 ms: 1.07x slower                                      |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 400 ms: 1.07x slower                                      |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 329 ms: 1.08x slower                                      |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 373 ms: 1.08x slower                                      |
| Geometric mean                  | (ref)                                                    | 1.02x slower                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| pidigits       | 181 ms                                                   | 178 ms: 1.02x faster                                      |
| float          | 46.5 ms                                                  | 48.2 ms: 1.04x slower                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| regex_dna      | 158 ms                                                   | 153 ms: 1.03x faster                                      |
| regex_v8       | 14.9 ms                                                  | 14.5 ms: 1.03x faster                                     |
| regex_compile  | 102 ms                                                   | 101 ms: 1.01x faster                                      |
| Geometric mean | (ref)                                                    | 1.02x faster                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| xml_etree_iterparse  | 64.7 ms                                                  | 57.9 ms: 1.12x faster                                     |
| tomli_loads          | 1.53 sec                                                 | 1.47 sec: 1.04x faster                                    |
| pickle_pure_python   | 243 us                                                   | 237 us: 1.03x faster                                      |
| json_loads           | 19.5 us                                                  | 19.2 us: 1.01x faster                                     |
| unpickle_pure_python | 155 us                                                   | 154 us: 1.00x faster                                      |
| xml_etree_parse      | 94.4 ms                                                  | 97.5 ms: 1.03x slower                                     |
| json_dumps           | 7.98 ms                                                  | 8.38 ms: 1.05x slower                                     |
| xml_etree_process    | 46.6 ms                                                  | 49.5 ms: 1.06x slower                                     |
| xml_etree_generate   | 64.9 ms                                                  | 69.8 ms: 1.08x slower                                     |
| Geometric mean       | (ref)                                                    | 1.00x slower                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| python_startup_no_site | 9.52 ms                                                  | 9.34 ms: 1.02x faster                                     |
| python_startup         | 13.0 ms                                                  | 12.8 ms: 1.02x faster                                     |
| Geometric mean         | (ref)                                                    | 1.02x faster                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| genshi_xml      | 41.7 ms                                                  | 40.2 ms: 1.04x faster                                     |
| genshi_text     | 18.7 ms                                                  | 18.3 ms: 1.02x faster                                     |
| mako            | 10.7 ms                                                  | 10.5 ms: 1.01x faster                                     |
| django_template | 30.8 ms                                                  | 30.4 ms: 1.01x faster                                     |
| Geometric mean  | (ref)                                                    | 1.02x faster                                              |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-NOGIL-3.14.0a7+-gcc15 |
|---------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------:|
| gc_traversal                    | 1.48 ms                                                  | 1.30 ms: 1.13x faster                                     |
| xml_etree_iterparse             | 64.7 ms                                                  | 57.9 ms: 1.12x faster                                     |
| pathlib                         | 13.1 ms                                                  | 12.2 ms: 1.07x faster                                     |
| coverage                        | 78.4 ms                                                  | 73.9 ms: 1.06x faster                                     |
| hexiom                          | 4.64 ms                                                  | 4.41 ms: 1.05x faster                                     |
| subparsers                      | 18.4 ms                                                  | 17.5 ms: 1.05x faster                                     |
| coroutines                      | 14.4 ms                                                  | 13.7 ms: 1.05x faster                                     |
| raytrace                        | 217 ms                                                   | 208 ms: 1.04x faster                                      |
| create_gc_cycles                | 1.16 ms                                                  | 1.12 ms: 1.04x faster                                     |
| deltablue                       | 2.50 ms                                                  | 2.41 ms: 1.04x faster                                     |
| tomli_loads                     | 1.53 sec                                                 | 1.47 sec: 1.04x faster                                    |
| genshi_xml                      | 41.7 ms                                                  | 40.2 ms: 1.04x faster                                     |
| sqlalchemy_imperative           | 16.2 ms                                                  | 15.6 ms: 1.04x faster                                     |
| pprint_pformat                  | 1.12 sec                                                 | 1.08 sec: 1.03x faster                                    |
| pyflate                         | 339 ms                                                   | 328 ms: 1.03x faster                                      |
| typing_runtime_protocols        | 132 us                                                   | 128 us: 1.03x faster                                      |
| regex_dna                       | 158 ms                                                   | 153 ms: 1.03x faster                                      |
| async_tree_eager                | 94.7 ms                                                  | 91.7 ms: 1.03x faster                                     |
| regex_v8                        | 14.9 ms                                                  | 14.5 ms: 1.03x faster                                     |
| sympy_integrate                 | 16.6 ms                                                  | 16.1 ms: 1.03x faster                                     |
| dulwich_log                     | 45.2 ms                                                  | 44.0 ms: 1.03x faster                                     |
| html5lib                        | 47.1 ms                                                  | 45.8 ms: 1.03x faster                                     |
| pickle_pure_python              | 243 us                                                   | 237 us: 1.03x faster                                      |
| pprint_safe_repr                | 530 ms                                                   | 517 ms: 1.03x faster                                      |
| genshi_text                     | 18.7 ms                                                  | 18.3 ms: 1.02x faster                                     |
| sqlglot_v2_normalize            | 80.1 ms                                                  | 78.3 ms: 1.02x faster                                     |
| sympy_str                       | 211 ms                                                   | 207 ms: 1.02x faster                                      |
| sympy_sum                       | 112 ms                                                   | 109 ms: 1.02x faster                                      |
| 2to3                            | 207 ms                                                   | 203 ms: 1.02x faster                                      |
| python_startup_no_site          | 9.52 ms                                                  | 9.34 ms: 1.02x faster                                     |
| pidigits                        | 181 ms                                                   | 178 ms: 1.02x faster                                      |
| python_startup                  | 13.0 ms                                                  | 12.8 ms: 1.02x faster                                     |
| sqlglot_v2_parse                | 1.03 ms                                                  | 1.01 ms: 1.02x faster                                     |
| nqueens                         | 61.6 ms                                                  | 60.6 ms: 1.02x faster                                     |
| mako                            | 10.7 ms                                                  | 10.5 ms: 1.01x faster                                     |
| many_optionals                  | 751 us                                                   | 740 us: 1.01x faster                                      |
| async_tree_eager_memoization_tg | 211 ms                                                   | 208 ms: 1.01x faster                                      |
| sympy_expand                    | 360 ms                                                   | 355 ms: 1.01x faster                                      |
| deepcopy_memo                   | 21.4 us                                                  | 21.1 us: 1.01x faster                                     |
| async_tree_none                 | 205 ms                                                   | 202 ms: 1.01x faster                                      |
| sqlalchemy_declarative          | 109 ms                                                   | 108 ms: 1.01x faster                                      |
| django_template                 | 30.8 ms                                                  | 30.4 ms: 1.01x faster                                     |
| sqlglot_v2_optimize             | 39.7 ms                                                  | 39.2 ms: 1.01x faster                                     |
| json_loads                      | 19.5 us                                                  | 19.2 us: 1.01x faster                                     |
| sqlglot_v2_transpile            | 1.26 ms                                                  | 1.25 ms: 1.01x faster                                     |
| regex_compile                   | 102 ms                                                   | 101 ms: 1.01x faster                                      |
| deepcopy                        | 211 us                                                   | 209 us: 1.01x faster                                      |
| richards                        | 36.1 ms                                                  | 35.9 ms: 1.01x faster                                     |
| meteor_contest                  | 97.9 ms                                                  | 97.4 ms: 1.01x faster                                     |
| unpickle_pure_python            | 155 us                                                   | 154 us: 1.00x faster                                      |
| crypto_pyaes                    | 59.5 ms                                                  | 59.8 ms: 1.00x slower                                     |
| telco                           | 6.04 ms                                                  | 6.07 ms: 1.01x slower                                     |
| json                            | 3.48 ms                                                  | 3.51 ms: 1.01x slower                                     |
| mdp                             | 925 ms                                                   | 934 ms: 1.01x slower                                      |
| async_tree_memoization_tg       | 227 ms                                                   | 229 ms: 1.01x slower                                      |
| deepcopy_reduce                 | 2.23 us                                                  | 2.26 us: 1.01x slower                                     |
| async_tree_memoization          | 254 ms                                                   | 257 ms: 1.01x slower                                      |
| sphinx                          | 788 ms                                                   | 799 ms: 1.01x slower                                      |
| async_tree_none_tg              | 169 ms                                                   | 172 ms: 1.02x slower                                      |
| shortest_path                   | 507 ms                                                   | 517 ms: 1.02x slower                                      |
| connected_components            | 486 ms                                                   | 499 ms: 1.03x slower                                      |
| bpe_tokeniser                   | 3.13 sec                                                 | 3.24 sec: 1.03x slower                                    |
| xml_etree_parse                 | 94.4 ms                                                  | 97.5 ms: 1.03x slower                                     |
| comprehensions                  | 11.9 us                                                  | 12.4 us: 1.03x slower                                     |
| docutils                        | 2.02 sec                                                 | 2.09 sec: 1.04x slower                                    |
| float                           | 46.5 ms                                                  | 48.2 ms: 1.04x slower                                     |
| json_dumps                      | 7.98 ms                                                  | 8.38 ms: 1.05x slower                                     |
| xml_etree_process               | 46.6 ms                                                  | 49.5 ms: 1.06x slower                                     |
| sqlite_synth                    | 1.47 us                                                  | 1.56 us: 1.07x slower                                     |
| async_generators                | 238 ms                                                   | 254 ms: 1.07x slower                                      |
| async_tree_cpu_io_mixed         | 374 ms                                                   | 400 ms: 1.07x slower                                      |
| xml_etree_generate              | 64.9 ms                                                  | 69.8 ms: 1.08x slower                                     |
| async_tree_eager_cpu_io_mixed   | 305 ms                                                   | 329 ms: 1.08x slower                                      |
| async_tree_cpu_io_mixed_tg      | 345 ms                                                   | 373 ms: 1.08x slower                                      |
| Geometric mean                  | (ref)                                                    | 1.01x faster                                              |

- Geometric mean (including insignificant results): 1.008x faster

# HPT report

- Reliability score: 93.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x
# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL
- machine: unknown-unknown
- commit hash: 7890b77
- commit date: 2025-04-14
- overall geometric mean: 1.045x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.50x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| 2to3           | 193 ms                                                          | 203 ms: 1.05x slower                                           |
| docutils       | 1.99 sec                                                        | 2.09 sec: 1.05x slower                                         |
| html5lib       | 45.1 ms                                                         | 45.8 ms: 1.02x slower                                          |
| sphinx         | 754 ms                                                          | 799 ms: 1.06x slower                                           |
| Geometric mean | (ref)                                                           | 1.04x slower                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                       | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| async_tree_none_tg              | 214 ms                                                          | 172 ms: 1.24x faster                                           |
| async_tree_memoization_tg       | 270 ms                                                          | 229 ms: 1.18x faster                                           |
| async_tree_none                 | 228 ms                                                          | 202 ms: 1.13x faster                                           |
| async_tree_cpu_io_mixed_tg      | 414 ms                                                          | 373 ms: 1.11x faster                                           |
| async_tree_eager_memoization_tg | 231 ms                                                          | 208 ms: 1.11x faster                                           |
| coroutines                      | 14.5 ms                                                         | 13.7 ms: 1.06x faster                                          |
| async_tree_cpu_io_mixed         | 416 ms                                                          | 400 ms: 1.04x faster                                           |
| async_tree_memoization          | 263 ms                                                          | 257 ms: 1.02x faster                                           |
| async_tree_eager_cpu_io_mixed   | 321 ms                                                          | 329 ms: 1.02x slower                                           |
| async_generators                | 231 ms                                                          | 254 ms: 1.10x slower                                           |
| async_tree_eager                | 77.3 ms                                                         | 91.7 ms: 1.19x slower                                          |
| Geometric mean                  | (ref)                                                           | 1.05x faster                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| pidigits       | 181 ms                                                          | 178 ms: 1.02x faster                                           |
| float          | 45.7 ms                                                         | 48.2 ms: 1.05x slower                                          |
| Geometric mean | (ref)                                                           | 1.02x slower                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| regex_dna      | 143 ms                                                          | 153 ms: 1.07x slower                                           |
| regex_compile  | 89.1 ms                                                         | 101 ms: 1.13x slower                                           |
| Geometric mean | (ref)                                                           | 1.07x slower                                                   |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL |
|----------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| xml_etree_iterparse  | 67.3 ms                                                         | 57.9 ms: 1.16x faster                                          |
| unpickle_pure_python | 158 us                                                          | 154 us: 1.02x faster                                           |
| xml_etree_parse      | 99.5 ms                                                         | 97.5 ms: 1.02x faster                                          |
| xml_etree_process    | 47.4 ms                                                         | 49.5 ms: 1.04x slower                                          |
| pickle_pure_python   | 224 us                                                          | 237 us: 1.06x slower                                           |
| xml_etree_generate   | 65.2 ms                                                         | 69.8 ms: 1.07x slower                                          |
| json_loads           | 17.9 us                                                         | 19.2 us: 1.08x slower                                          |
| json_dumps           | 7.71 ms                                                         | 8.38 ms: 1.09x slower                                          |
| tomli_loads          | 1.34 sec                                                        | 1.47 sec: 1.10x slower                                         |
| Geometric mean       | (ref)                                                           | 1.02x slower                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL |
|------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                         | 12.8 ms: 1.19x slower                                          |
| python_startup_no_site | 7.47 ms                                                         | 9.34 ms: 1.25x slower                                          |
| Geometric mean         | (ref)                                                           | 1.22x slower                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL |
|-----------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| genshi_xml      | 37.8 ms                                                         | 40.2 ms: 1.06x slower                                          |
| django_template | 27.9 ms                                                         | 30.4 ms: 1.09x slower                                          |
| genshi_text     | 15.7 ms                                                         | 18.3 ms: 1.17x slower                                          |
| mako            | 7.19 ms                                                         | 10.5 ms: 1.47x slower                                          |
| Geometric mean  | (ref)                                                           | 1.19x slower                                                   |

All benchmarks:
===============

| Benchmark                       | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-000000 | bm-20250414-centurion_gcc15-x86_64-python-main-3.14.0a7+-NOGIL |
|---------------------------------|:---------------------------------------------------------------:|:--------------------------------------------------------------:|
| gc_traversal                    | 3.15 ms                                                         | 1.30 ms: 2.42x faster                                          |
| create_gc_cycles                | 1.75 ms                                                         | 1.12 ms: 1.57x faster                                          |
| async_tree_none_tg              | 214 ms                                                          | 172 ms: 1.24x faster                                           |
| async_tree_memoization_tg       | 270 ms                                                          | 229 ms: 1.18x faster                                           |
| xml_etree_iterparse             | 67.3 ms                                                         | 57.9 ms: 1.16x faster                                          |
| async_tree_none                 | 228 ms                                                          | 202 ms: 1.13x faster                                           |
| async_tree_cpu_io_mixed_tg      | 414 ms                                                          | 373 ms: 1.11x faster                                           |
| async_tree_eager_memoization_tg | 231 ms                                                          | 208 ms: 1.11x faster                                           |
| coroutines                      | 14.5 ms                                                         | 13.7 ms: 1.06x faster                                          |
| sqlite_synth                    | 1.64 us                                                         | 1.56 us: 1.05x faster                                          |
| async_tree_cpu_io_mixed         | 416 ms                                                          | 400 ms: 1.04x faster                                           |
| async_tree_memoization          | 263 ms                                                          | 257 ms: 1.02x faster                                           |
| unpickle_pure_python            | 158 us                                                          | 154 us: 1.02x faster                                           |
| xml_etree_parse                 | 99.5 ms                                                         | 97.5 ms: 1.02x faster                                          |
| pidigits                        | 181 ms                                                          | 178 ms: 1.02x faster                                           |
| json                            | 3.56 ms                                                         | 3.51 ms: 1.01x faster                                          |
| pathlib                         | 12.3 ms                                                         | 12.2 ms: 1.01x faster                                          |
| html5lib                        | 45.1 ms                                                         | 45.8 ms: 1.02x slower                                          |
| many_optionals                  | 726 us                                                          | 740 us: 1.02x slower                                           |
| async_tree_eager_cpu_io_mixed   | 321 ms                                                          | 329 ms: 1.02x slower                                           |
| subparsers                      | 17.0 ms                                                         | 17.5 ms: 1.03x slower                                          |
| mdp                             | 908 ms                                                          | 934 ms: 1.03x slower                                           |
| sqlglot_v2_optimize             | 37.9 ms                                                         | 39.2 ms: 1.04x slower                                          |
| dulwich_log                     | 42.3 ms                                                         | 44.0 ms: 1.04x slower                                          |
| deltablue                       | 2.31 ms                                                         | 2.41 ms: 1.04x slower                                          |
| xml_etree_process               | 47.4 ms                                                         | 49.5 ms: 1.04x slower                                          |
| bpe_tokeniser                   | 3.09 sec                                                        | 3.24 sec: 1.05x slower                                         |
| docutils                        | 1.99 sec                                                        | 2.09 sec: 1.05x slower                                         |
| 2to3                            | 193 ms                                                          | 203 ms: 1.05x slower                                           |
| float                           | 45.7 ms                                                         | 48.2 ms: 1.05x slower                                          |
| pickle_pure_python              | 224 us                                                          | 237 us: 1.06x slower                                           |
| sqlglot_v2_normalize            | 74.0 ms                                                         | 78.3 ms: 1.06x slower                                          |
| sphinx                          | 754 ms                                                          | 799 ms: 1.06x slower                                           |
| genshi_xml                      | 37.8 ms                                                         | 40.2 ms: 1.06x slower                                          |
| regex_dna                       | 143 ms                                                          | 153 ms: 1.07x slower                                           |
| xml_etree_generate              | 65.2 ms                                                         | 69.8 ms: 1.07x slower                                          |
| sympy_sum                       | 102 ms                                                          | 109 ms: 1.07x slower                                           |
| json_loads                      | 17.9 us                                                         | 19.2 us: 1.08x slower                                          |
| json_dumps                      | 7.71 ms                                                         | 8.38 ms: 1.09x slower                                          |
| django_template                 | 27.9 ms                                                         | 30.4 ms: 1.09x slower                                          |
| async_generators                | 231 ms                                                          | 254 ms: 1.10x slower                                           |
| tomli_loads                     | 1.34 sec                                                        | 1.47 sec: 1.10x slower                                         |
| nqueens                         | 55.2 ms                                                         | 60.6 ms: 1.10x slower                                          |
| pprint_safe_repr                | 470 ms                                                          | 517 ms: 1.10x slower                                           |
| sympy_expand                    | 323 ms                                                          | 355 ms: 1.10x slower                                           |
| sqlglot_v2_transpile            | 1.13 ms                                                         | 1.25 ms: 1.10x slower                                          |
| sympy_str                       | 187 ms                                                          | 207 ms: 1.11x slower                                           |
| sympy_integrate                 | 14.5 ms                                                         | 16.1 ms: 1.11x slower                                          |
| comprehensions                  | 11.1 us                                                         | 12.4 us: 1.11x slower                                          |
| pprint_pformat                  | 967 ms                                                          | 1.08 sec: 1.12x slower                                         |
| pyflate                         | 293 ms                                                          | 328 ms: 1.12x slower                                           |
| raytrace                        | 185 ms                                                          | 208 ms: 1.13x slower                                           |
| sqlalchemy_declarative          | 95.8 ms                                                         | 108 ms: 1.13x slower                                           |
| regex_compile                   | 89.1 ms                                                         | 101 ms: 1.13x slower                                           |
| deepcopy                        | 185 us                                                          | 209 us: 1.13x slower                                           |
| sqlalchemy_imperative           | 13.8 ms                                                         | 15.6 ms: 1.13x slower                                          |
| connected_components            | 441 ms                                                          | 499 ms: 1.13x slower                                           |
| hexiom                          | 3.87 ms                                                         | 4.41 ms: 1.14x slower                                          |
| sqlglot_v2_parse                | 877 us                                                          | 1.01 ms: 1.15x slower                                          |
| meteor_contest                  | 84.3 ms                                                         | 97.4 ms: 1.15x slower                                          |
| deepcopy_reduce                 | 1.94 us                                                         | 2.26 us: 1.16x slower                                          |
| telco                           | 5.21 ms                                                         | 6.07 ms: 1.16x slower                                          |
| genshi_text                     | 15.7 ms                                                         | 18.3 ms: 1.17x slower                                          |
| shortest_path                   | 443 ms                                                          | 517 ms: 1.17x slower                                           |
| richards                        | 30.5 ms                                                         | 35.9 ms: 1.18x slower                                          |
| async_tree_eager                | 77.3 ms                                                         | 91.7 ms: 1.19x slower                                          |
| python_startup                  | 10.7 ms                                                         | 12.8 ms: 1.19x slower                                          |
| deepcopy_memo                   | 17.7 us                                                         | 21.1 us: 1.19x slower                                          |
| crypto_pyaes                    | 49.8 ms                                                         | 59.8 ms: 1.20x slower                                          |
| python_startup_no_site          | 7.47 ms                                                         | 9.34 ms: 1.25x slower                                          |
| typing_runtime_protocols        | 102 us                                                          | 128 us: 1.25x slower                                           |
| coverage                        | 54.9 ms                                                         | 73.9 ms: 1.35x slower                                          |
| mako                            | 7.19 ms                                                         | 10.5 ms: 1.47x slower                                          |
| Geometric mean                  | (ref)                                                           | 1.05x slower                                                   |

Benchmark hidden because not significant (1): regex_v8

- Geometric mean (including insignificant results): 1.045x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.50x
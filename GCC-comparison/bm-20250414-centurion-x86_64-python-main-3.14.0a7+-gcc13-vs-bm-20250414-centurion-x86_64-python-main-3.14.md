# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.003x slower
- HPT reliability: 73.19%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 194 ms                                                  | 193 ms: 1.01x faster                                     |
| docutils       | 1.95 sec                                                | 2.02 sec: 1.04x slower                                   |
| html5lib       | 46.6 ms                                                 | 45.9 ms: 1.01x faster                                    |
| sphinx         | 755 ms                                                  | 766 ms: 1.01x slower                                     |
| Geometric mean | (ref)                                                   | 1.01x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13 |
|-------------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_eager              | 81.0 ms                                                 | 79.2 ms: 1.02x faster                                    |
| async_tree_none               | 232 ms                                                  | 234 ms: 1.01x slower                                     |
| coroutines                    | 14.5 ms                                                 | 14.7 ms: 1.01x slower                                    |
| async_tree_cpu_io_mixed_tg    | 395 ms                                                  | 419 ms: 1.06x slower                                     |
| async_tree_cpu_io_mixed       | 395 ms                                                  | 421 ms: 1.06x slower                                     |
| async_tree_eager_cpu_io_mixed | 300 ms                                                  | 322 ms: 1.07x slower                                     |
| async_generators              | 215 ms                                                  | 234 ms: 1.09x slower                                     |
| Geometric mean                | (ref)                                                   | 1.02x slower                                             |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_memoization, async_tree_eager_memoization_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 184 ms                                                  | 181 ms: 1.02x faster                                     |
| float          | 46.7 ms                                                 | 47.6 ms: 1.02x slower                                    |
| Geometric mean | (ref)                                                   | 1.00x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 156 ms                                                  | 143 ms: 1.09x faster                                     |
| regex_v8       | 15.2 ms                                                 | 14.7 ms: 1.03x faster                                    |
| regex_compile  | 90.1 ms                                                 | 91.9 ms: 1.02x slower                                    |
| Geometric mean | (ref)                                                   | 1.03x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13 |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse  | 77.8 ms                                                 | 68.5 ms: 1.14x faster                                    |
| tomli_loads          | 1.40 sec                                                | 1.36 sec: 1.03x faster                                   |
| pickle_pure_python   | 224 us                                                  | 228 us: 1.02x slower                                     |
| unpickle_pure_python | 155 us                                                  | 158 us: 1.02x slower                                     |
| json_loads           | 17.4 us                                                 | 17.8 us: 1.02x slower                                    |
| json_dumps           | 7.27 ms                                                 | 7.58 ms: 1.04x slower                                    |
| xml_etree_parse      | 92.9 ms                                                 | 97.9 ms: 1.05x slower                                    |
| xml_etree_process    | 44.9 ms                                                 | 48.1 ms: 1.07x slower                                    |
| xml_etree_generate   | 62.2 ms                                                 | 67.0 ms: 1.08x slower                                    |
| Geometric mean       | (ref)                                                   | 1.02x slower                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13 |
|------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 7.53 ms                                                 | 7.47 ms: 1.01x faster                                    |
| python_startup         | 10.9 ms                                                 | 10.8 ms: 1.01x faster                                    |
| Geometric mean         | (ref)                                                   | 1.01x faster                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13 |
|-----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 39.4 ms                                                 | 38.0 ms: 1.04x faster                                    |
| genshi_text     | 16.0 ms                                                 | 16.1 ms: 1.01x slower                                    |
| mako            | 7.37 ms                                                 | 7.54 ms: 1.02x slower                                    |
| django_template | 27.9 ms                                                 | 28.9 ms: 1.03x slower                                    |
| Geometric mean  | (ref)                                                   | 1.01x slower                                             |

All benchmarks:
===============

| Benchmark                     | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc13 |
|-------------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| deltablue                     | 2.65 ms                                                 | 2.17 ms: 1.22x faster                                    |
| xml_etree_iterparse           | 77.8 ms                                                 | 68.5 ms: 1.14x faster                                    |
| regex_dna                     | 156 ms                                                  | 143 ms: 1.09x faster                                     |
| typing_runtime_protocols      | 107 us                                                  | 102 us: 1.04x faster                                     |
| pyflate                       | 310 ms                                                  | 298 ms: 1.04x faster                                     |
| pathlib                       | 13.0 ms                                                 | 12.5 ms: 1.04x faster                                    |
| subparsers                    | 17.6 ms                                                 | 17.0 ms: 1.04x faster                                    |
| genshi_xml                    | 39.4 ms                                                 | 38.0 ms: 1.04x faster                                    |
| regex_v8                      | 15.2 ms                                                 | 14.7 ms: 1.03x faster                                    |
| sympy_integrate               | 15.2 ms                                                 | 14.8 ms: 1.03x faster                                    |
| tomli_loads                   | 1.40 sec                                                | 1.36 sec: 1.03x faster                                   |
| sqlglot_v2_normalize          | 78.5 ms                                                 | 76.4 ms: 1.03x faster                                    |
| hexiom                        | 4.08 ms                                                 | 3.97 ms: 1.03x faster                                    |
| async_tree_eager              | 81.0 ms                                                 | 79.2 ms: 1.02x faster                                    |
| richards                      | 31.0 ms                                                 | 30.3 ms: 1.02x faster                                    |
| mdp                           | 945 ms                                                  | 925 ms: 1.02x faster                                     |
| sympy_sum                     | 105 ms                                                  | 103 ms: 1.02x faster                                     |
| pidigits                      | 184 ms                                                  | 181 ms: 1.02x faster                                     |
| html5lib                      | 46.6 ms                                                 | 45.9 ms: 1.01x faster                                    |
| sympy_str                     | 192 ms                                                  | 190 ms: 1.01x faster                                     |
| create_gc_cycles              | 1.77 ms                                                 | 1.74 ms: 1.01x faster                                    |
| sqlglot_v2_parse              | 894 us                                                  | 885 us: 1.01x faster                                     |
| sympy_expand                  | 327 ms                                                  | 324 ms: 1.01x faster                                     |
| 2to3                          | 194 ms                                                  | 193 ms: 1.01x faster                                     |
| sqlglot_v2_optimize           | 38.6 ms                                                 | 38.2 ms: 1.01x faster                                    |
| connected_components          | 433 ms                                                  | 430 ms: 1.01x faster                                     |
| python_startup_no_site        | 7.53 ms                                                 | 7.47 ms: 1.01x faster                                    |
| crypto_pyaes                  | 52.7 ms                                                 | 52.3 ms: 1.01x faster                                    |
| bpe_tokeniser                 | 3.11 sec                                                | 3.08 sec: 1.01x faster                                   |
| python_startup                | 10.9 ms                                                 | 10.8 ms: 1.01x faster                                    |
| meteor_contest                | 84.6 ms                                                 | 84.0 ms: 1.01x faster                                    |
| many_optionals                | 731 us                                                  | 726 us: 1.01x faster                                     |
| genshi_text                   | 16.0 ms                                                 | 16.1 ms: 1.01x slower                                    |
| async_tree_none               | 232 ms                                                  | 234 ms: 1.01x slower                                     |
| coroutines                    | 14.5 ms                                                 | 14.7 ms: 1.01x slower                                    |
| sphinx                        | 755 ms                                                  | 766 ms: 1.01x slower                                     |
| sqlite_synth                  | 1.56 us                                                 | 1.58 us: 1.01x slower                                    |
| pickle_pure_python            | 224 us                                                  | 228 us: 1.02x slower                                     |
| raytrace                      | 186 ms                                                  | 189 ms: 1.02x slower                                     |
| sqlalchemy_imperative         | 14.1 ms                                                 | 14.4 ms: 1.02x slower                                    |
| sqlalchemy_declarative        | 96.2 ms                                                 | 97.8 ms: 1.02x slower                                    |
| unpickle_pure_python          | 155 us                                                  | 158 us: 1.02x slower                                     |
| regex_compile                 | 90.1 ms                                                 | 91.9 ms: 1.02x slower                                    |
| float                         | 46.7 ms                                                 | 47.6 ms: 1.02x slower                                    |
| json_loads                    | 17.4 us                                                 | 17.8 us: 1.02x slower                                    |
| json                          | 3.35 ms                                                 | 3.43 ms: 1.02x slower                                    |
| mako                          | 7.37 ms                                                 | 7.54 ms: 1.02x slower                                    |
| deepcopy_reduce               | 1.98 us                                                 | 2.03 us: 1.02x slower                                    |
| deepcopy_memo                 | 18.0 us                                                 | 18.5 us: 1.02x slower                                    |
| gc_traversal                  | 3.06 ms                                                 | 3.15 ms: 1.03x slower                                    |
| django_template               | 27.9 ms                                                 | 28.9 ms: 1.03x slower                                    |
| docutils                      | 1.95 sec                                                | 2.02 sec: 1.04x slower                                   |
| telco                         | 5.15 ms                                                 | 5.36 ms: 1.04x slower                                    |
| json_dumps                    | 7.27 ms                                                 | 7.58 ms: 1.04x slower                                    |
| deepcopy                      | 185 us                                                  | 194 us: 1.05x slower                                     |
| nqueens                       | 54.0 ms                                                 | 56.5 ms: 1.05x slower                                    |
| xml_etree_parse               | 92.9 ms                                                 | 97.9 ms: 1.05x slower                                    |
| comprehensions                | 10.8 us                                                 | 11.4 us: 1.06x slower                                    |
| async_tree_cpu_io_mixed_tg    | 395 ms                                                  | 419 ms: 1.06x slower                                     |
| async_tree_cpu_io_mixed       | 395 ms                                                  | 421 ms: 1.06x slower                                     |
| pprint_pformat                | 943 ms                                                  | 1.01 sec: 1.07x slower                                   |
| xml_etree_process             | 44.9 ms                                                 | 48.1 ms: 1.07x slower                                    |
| async_tree_eager_cpu_io_mixed | 300 ms                                                  | 322 ms: 1.07x slower                                     |
| pprint_safe_repr              | 464 ms                                                  | 498 ms: 1.07x slower                                     |
| xml_etree_generate            | 62.2 ms                                                 | 67.0 ms: 1.08x slower                                    |
| async_generators              | 215 ms                                                  | 234 ms: 1.09x slower                                     |
| Geometric mean                | (ref)                                                   | 1.00x slower                                             |

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_memoization, shortest_path, async_tree_eager_memoization_tg, async_tree_memoization_tg, coverage, sqlglot_v2_transpile, dulwich_log

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 73.19% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x
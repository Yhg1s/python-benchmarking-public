# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.003x slower
- HPT reliability: 56.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 194 ms                                                  | 193 ms: 1.01x faster                                     |
| docutils       | 1.95 sec                                                | 2.02 sec: 1.04x slower                                   |
| html5lib       | 46.6 ms                                                 | 46.2 ms: 1.01x faster                                    |
| sphinx         | 755 ms                                                  | 775 ms: 1.03x slower                                     |
| Geometric mean | (ref)                                                   | 1.01x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12 |
|-------------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_none_tg            | 220 ms                                                  | 218 ms: 1.01x faster                                     |
| async_tree_none               | 232 ms                                                  | 233 ms: 1.00x slower                                     |
| coroutines                    | 14.5 ms                                                 | 15.0 ms: 1.03x slower                                    |
| async_tree_cpu_io_mixed_tg    | 395 ms                                                  | 417 ms: 1.06x slower                                     |
| async_tree_cpu_io_mixed       | 395 ms                                                  | 420 ms: 1.06x slower                                     |
| async_tree_eager_cpu_io_mixed | 300 ms                                                  | 323 ms: 1.08x slower                                     |
| async_generators              | 215 ms                                                  | 233 ms: 1.08x slower                                     |
| Geometric mean                | (ref)                                                   | 1.03x slower                                             |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_memoization, async_tree_eager, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 184 ms                                                  | 182 ms: 1.02x faster                                     |
| Geometric mean | (ref)                                                   | 1.01x faster                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 156 ms                                                  | 143 ms: 1.09x faster                                     |
| regex_v8       | 15.2 ms                                                 | 14.4 ms: 1.05x faster                                    |
| regex_compile  | 90.1 ms                                                 | 91.5 ms: 1.02x slower                                    |
| Geometric mean | (ref)                                                   | 1.04x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12 |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse  | 77.8 ms                                                 | 68.7 ms: 1.13x faster                                    |
| tomli_loads          | 1.40 sec                                                | 1.37 sec: 1.02x faster                                   |
| pickle_pure_python   | 224 us                                                  | 228 us: 1.02x slower                                     |
| json_loads           | 17.4 us                                                 | 17.7 us: 1.02x slower                                    |
| unpickle_pure_python | 155 us                                                  | 159 us: 1.02x slower                                     |
| xml_etree_parse      | 92.9 ms                                                 | 97.9 ms: 1.05x slower                                    |
| json_dumps           | 7.27 ms                                                 | 7.71 ms: 1.06x slower                                    |
| xml_etree_generate   | 62.2 ms                                                 | 67.0 ms: 1.08x slower                                    |
| xml_etree_process    | 44.9 ms                                                 | 48.5 ms: 1.08x slower                                    |
| Geometric mean       | (ref)                                                   | 1.02x slower                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12 |
|------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 10.9 ms                                                 | 10.8 ms: 1.00x faster                                    |
| python_startup_no_site | 7.53 ms                                                 | 7.50 ms: 1.00x faster                                    |
| Geometric mean         | (ref)                                                   | 1.00x faster                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12 |
|-----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 39.4 ms                                                 | 38.4 ms: 1.03x faster                                    |
| genshi_text     | 16.0 ms                                                 | 16.0 ms: 1.01x slower                                    |
| mako            | 7.37 ms                                                 | 7.56 ms: 1.03x slower                                    |
| django_template | 27.9 ms                                                 | 28.8 ms: 1.03x slower                                    |
| Geometric mean  | (ref)                                                   | 1.01x slower                                             |

All benchmarks:
===============

| Benchmark                     | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc12 |
|-------------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| deltablue                     | 2.65 ms                                                 | 2.21 ms: 1.20x faster                                    |
| xml_etree_iterparse           | 77.8 ms                                                 | 68.7 ms: 1.13x faster                                    |
| regex_dna                     | 156 ms                                                  | 143 ms: 1.09x faster                                     |
| regex_v8                      | 15.2 ms                                                 | 14.4 ms: 1.05x faster                                    |
| pyflate                       | 310 ms                                                  | 297 ms: 1.05x faster                                     |
| typing_runtime_protocols      | 107 us                                                  | 102 us: 1.04x faster                                     |
| hexiom                        | 4.08 ms                                                 | 3.94 ms: 1.04x faster                                    |
| sympy_integrate               | 15.2 ms                                                 | 14.7 ms: 1.03x faster                                    |
| pathlib                       | 13.0 ms                                                 | 12.6 ms: 1.03x faster                                    |
| genshi_xml                    | 39.4 ms                                                 | 38.4 ms: 1.03x faster                                    |
| subparsers                    | 17.6 ms                                                 | 17.2 ms: 1.02x faster                                    |
| tomli_loads                   | 1.40 sec                                                | 1.37 sec: 1.02x faster                                   |
| mdp                           | 945 ms                                                  | 929 ms: 1.02x faster                                     |
| sqlglot_v2_normalize          | 78.5 ms                                                 | 77.3 ms: 1.02x faster                                    |
| pidigits                      | 184 ms                                                  | 182 ms: 1.02x faster                                     |
| sympy_str                     | 192 ms                                                  | 190 ms: 1.01x faster                                     |
| sympy_sum                     | 105 ms                                                  | 104 ms: 1.01x faster                                     |
| sympy_expand                  | 327 ms                                                  | 324 ms: 1.01x faster                                     |
| connected_components          | 433 ms                                                  | 429 ms: 1.01x faster                                     |
| html5lib                      | 46.6 ms                                                 | 46.2 ms: 1.01x faster                                    |
| async_tree_none_tg            | 220 ms                                                  | 218 ms: 1.01x faster                                     |
| sqlglot_v2_parse              | 894 us                                                  | 887 us: 1.01x faster                                     |
| create_gc_cycles              | 1.77 ms                                                 | 1.75 ms: 1.01x faster                                    |
| gc_traversal                  | 3.06 ms                                                 | 3.03 ms: 1.01x faster                                    |
| dulwich_log                   | 42.7 ms                                                 | 42.3 ms: 1.01x faster                                    |
| 2to3                          | 194 ms                                                  | 193 ms: 1.01x faster                                     |
| sqlglot_v2_optimize           | 38.6 ms                                                 | 38.4 ms: 1.01x faster                                    |
| python_startup                | 10.9 ms                                                 | 10.8 ms: 1.00x faster                                    |
| python_startup_no_site        | 7.53 ms                                                 | 7.50 ms: 1.00x faster                                    |
| meteor_contest                | 84.6 ms                                                 | 84.2 ms: 1.00x faster                                    |
| many_optionals                | 731 us                                                  | 728 us: 1.00x faster                                     |
| sqlglot_v2_transpile          | 1.14 ms                                                 | 1.14 ms: 1.00x faster                                    |
| bpe_tokeniser                 | 3.11 sec                                                | 3.11 sec: 1.00x slower                                   |
| sqlalchemy_imperative         | 14.1 ms                                                 | 14.2 ms: 1.00x slower                                    |
| async_tree_none               | 232 ms                                                  | 233 ms: 1.00x slower                                     |
| genshi_text                   | 16.0 ms                                                 | 16.0 ms: 1.01x slower                                    |
| crypto_pyaes                  | 52.7 ms                                                 | 53.0 ms: 1.01x slower                                    |
| deepcopy_memo                 | 18.0 us                                                 | 18.1 us: 1.01x slower                                    |
| telco                         | 5.15 ms                                                 | 5.18 ms: 1.01x slower                                    |
| sqlite_synth                  | 1.56 us                                                 | 1.57 us: 1.01x slower                                    |
| sqlalchemy_declarative        | 96.2 ms                                                 | 97.5 ms: 1.01x slower                                    |
| regex_compile                 | 90.1 ms                                                 | 91.5 ms: 1.02x slower                                    |
| pickle_pure_python            | 224 us                                                  | 228 us: 1.02x slower                                     |
| json_loads                    | 17.4 us                                                 | 17.7 us: 1.02x slower                                    |
| raytrace                      | 186 ms                                                  | 190 ms: 1.02x slower                                     |
| unpickle_pure_python          | 155 us                                                  | 159 us: 1.02x slower                                     |
| mako                          | 7.37 ms                                                 | 7.56 ms: 1.03x slower                                    |
| sphinx                        | 755 ms                                                  | 775 ms: 1.03x slower                                     |
| deepcopy                      | 185 us                                                  | 191 us: 1.03x slower                                     |
| django_template               | 27.9 ms                                                 | 28.8 ms: 1.03x slower                                    |
| coroutines                    | 14.5 ms                                                 | 15.0 ms: 1.03x slower                                    |
| deepcopy_reduce               | 1.98 us                                                 | 2.05 us: 1.04x slower                                    |
| docutils                      | 1.95 sec                                                | 2.02 sec: 1.04x slower                                   |
| json                          | 3.35 ms                                                 | 3.49 ms: 1.04x slower                                    |
| pprint_safe_repr              | 464 ms                                                  | 487 ms: 1.05x slower                                     |
| xml_etree_parse               | 92.9 ms                                                 | 97.9 ms: 1.05x slower                                    |
| async_tree_cpu_io_mixed_tg    | 395 ms                                                  | 417 ms: 1.06x slower                                     |
| nqueens                       | 54.0 ms                                                 | 57.0 ms: 1.06x slower                                    |
| pprint_pformat                | 943 ms                                                  | 996 ms: 1.06x slower                                     |
| json_dumps                    | 7.27 ms                                                 | 7.71 ms: 1.06x slower                                    |
| async_tree_cpu_io_mixed       | 395 ms                                                  | 420 ms: 1.06x slower                                     |
| comprehensions                | 10.8 us                                                 | 11.5 us: 1.07x slower                                    |
| async_tree_eager_cpu_io_mixed | 300 ms                                                  | 323 ms: 1.08x slower                                     |
| xml_etree_generate            | 62.2 ms                                                 | 67.0 ms: 1.08x slower                                    |
| xml_etree_process             | 44.9 ms                                                 | 48.5 ms: 1.08x slower                                    |
| async_generators              | 215 ms                                                  | 233 ms: 1.08x slower                                     |
| Geometric mean                | (ref)                                                   | 1.00x slower                                             |

Benchmark hidden because not significant (8): richards, async_tree_memoization_tg, async_tree_memoization, async_tree_eager, shortest_path, float, coverage, async_tree_eager_memoization_tg

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 56.87% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x
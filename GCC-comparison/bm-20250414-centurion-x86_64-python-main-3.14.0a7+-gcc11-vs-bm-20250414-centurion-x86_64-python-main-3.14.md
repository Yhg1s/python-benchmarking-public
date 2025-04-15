# Results vs. base

- fork: unknown
- ref: bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11
- machine: unknown-unknown
- commit hash: 087f134
- commit date: 2025-04-14
- overall geometric mean: 1.003x slower
- HPT reliability: 54.92%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 194 ms                                                  | 195 ms: 1.01x slower                                     |
| docutils       | 1.95 sec                                                | 1.96 sec: 1.00x slower                                   |
| html5lib       | 46.6 ms                                                 | 47.1 ms: 1.01x slower                                    |
| Geometric mean | (ref)                                                   | 1.01x slower                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11 |
|----------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_memoization     | 270 ms                                                  | 265 ms: 1.02x faster                                     |
| async_tree_none_tg         | 220 ms                                                  | 217 ms: 1.01x faster                                     |
| async_tree_cpu_io_mixed_tg | 395 ms                                                  | 390 ms: 1.01x faster                                     |
| async_tree_cpu_io_mixed    | 395 ms                                                  | 392 ms: 1.01x faster                                     |
| coroutines                 | 14.5 ms                                                 | 15.2 ms: 1.04x slower                                    |
| Geometric mean             | (ref)                                                   | 1.00x faster                                             |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_none, async_generators, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 184 ms                                                  | 186 ms: 1.01x slower                                     |
| Geometric mean | (ref)                                                   | 1.00x slower                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11 |
|----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 156 ms                                                  | 150 ms: 1.04x faster                                     |
| regex_v8       | 15.2 ms                                                 | 15.1 ms: 1.01x faster                                    |
| regex_compile  | 90.1 ms                                                 | 91.7 ms: 1.02x slower                                    |
| Geometric mean | (ref)                                                   | 1.01x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11 |
|----------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse  | 77.8 ms                                                 | 68.3 ms: 1.14x faster                                    |
| tomli_loads          | 1.40 sec                                                | 1.37 sec: 1.02x faster                                   |
| xml_etree_generate   | 62.2 ms                                                 | 61.5 ms: 1.01x faster                                    |
| xml_etree_process    | 44.9 ms                                                 | 45.2 ms: 1.01x slower                                    |
| xml_etree_parse      | 92.9 ms                                                 | 93.9 ms: 1.01x slower                                    |
| json_dumps           | 7.27 ms                                                 | 7.35 ms: 1.01x slower                                    |
| pickle_pure_python   | 224 us                                                  | 227 us: 1.01x slower                                     |
| unpickle_pure_python | 155 us                                                  | 158 us: 1.02x slower                                     |
| json_loads           | 17.4 us                                                 | 18.1 us: 1.04x slower                                    |
| Geometric mean       | (ref)                                                   | 1.01x faster                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11 |
|------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 10.9 ms                                                 | 10.7 ms: 1.01x faster                                    |
| python_startup_no_site | 7.53 ms                                                 | 7.45 ms: 1.01x faster                                    |
| Geometric mean         | (ref)                                                   | 1.01x faster                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11 |
|-----------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 39.4 ms                                                 | 39.2 ms: 1.01x faster                                    |
| django_template | 27.9 ms                                                 | 28.7 ms: 1.03x slower                                    |
| genshi_text     | 16.0 ms                                                 | 16.5 ms: 1.03x slower                                    |
| mako            | 7.37 ms                                                 | 8.03 ms: 1.09x slower                                    |
| Geometric mean  | (ref)                                                   | 1.04x slower                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc9 | bm-20250414-centurion-x86_64-python-main-3.14.0a7+-gcc11 |
|----------------------------|:-------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_iterparse        | 77.8 ms                                                 | 68.3 ms: 1.14x faster                                    |
| deltablue                  | 2.65 ms                                                 | 2.40 ms: 1.11x faster                                    |
| pathlib                    | 13.0 ms                                                 | 12.3 ms: 1.05x faster                                    |
| regex_dna                  | 156 ms                                                  | 150 ms: 1.04x faster                                     |
| subparsers                 | 17.6 ms                                                 | 17.2 ms: 1.02x faster                                    |
| tomli_loads                | 1.40 sec                                                | 1.37 sec: 1.02x faster                                   |
| meteor_contest             | 84.6 ms                                                 | 82.8 ms: 1.02x faster                                    |
| async_tree_memoization     | 270 ms                                                  | 265 ms: 1.02x faster                                     |
| sympy_integrate            | 15.2 ms                                                 | 15.0 ms: 1.01x faster                                    |
| pyflate                    | 310 ms                                                  | 306 ms: 1.01x faster                                     |
| dulwich_log                | 42.7 ms                                                 | 42.1 ms: 1.01x faster                                    |
| python_startup             | 10.9 ms                                                 | 10.7 ms: 1.01x faster                                    |
| python_startup_no_site     | 7.53 ms                                                 | 7.45 ms: 1.01x faster                                    |
| async_tree_none_tg         | 220 ms                                                  | 217 ms: 1.01x faster                                     |
| xml_etree_generate         | 62.2 ms                                                 | 61.5 ms: 1.01x faster                                    |
| async_tree_cpu_io_mixed_tg | 395 ms                                                  | 390 ms: 1.01x faster                                     |
| shortest_path              | 442 ms                                                  | 438 ms: 1.01x faster                                     |
| bpe_tokeniser              | 3.11 sec                                                | 3.08 sec: 1.01x faster                                   |
| crypto_pyaes               | 52.7 ms                                                 | 52.3 ms: 1.01x faster                                    |
| async_tree_cpu_io_mixed    | 395 ms                                                  | 392 ms: 1.01x faster                                     |
| create_gc_cycles           | 1.77 ms                                                 | 1.75 ms: 1.01x faster                                    |
| regex_v8                   | 15.2 ms                                                 | 15.1 ms: 1.01x faster                                    |
| many_optionals             | 731 us                                                  | 726 us: 1.01x faster                                     |
| genshi_xml                 | 39.4 ms                                                 | 39.2 ms: 1.01x faster                                    |
| raytrace                   | 186 ms                                                  | 185 ms: 1.00x faster                                     |
| docutils                   | 1.95 sec                                                | 1.96 sec: 1.00x slower                                   |
| sqlalchemy_declarative     | 96.2 ms                                                 | 96.7 ms: 1.00x slower                                    |
| hexiom                     | 4.08 ms                                                 | 4.10 ms: 1.00x slower                                    |
| sqlglot_v2_normalize       | 78.5 ms                                                 | 78.9 ms: 1.01x slower                                    |
| 2to3                       | 194 ms                                                  | 195 ms: 1.01x slower                                     |
| sqlalchemy_imperative      | 14.1 ms                                                 | 14.2 ms: 1.01x slower                                    |
| sqlglot_v2_transpile       | 1.14 ms                                                 | 1.15 ms: 1.01x slower                                    |
| xml_etree_process          | 44.9 ms                                                 | 45.2 ms: 1.01x slower                                    |
| pidigits                   | 184 ms                                                  | 186 ms: 1.01x slower                                     |
| sqlglot_v2_optimize        | 38.6 ms                                                 | 39.0 ms: 1.01x slower                                    |
| html5lib                   | 46.6 ms                                                 | 47.1 ms: 1.01x slower                                    |
| xml_etree_parse            | 92.9 ms                                                 | 93.9 ms: 1.01x slower                                    |
| json_dumps                 | 7.27 ms                                                 | 7.35 ms: 1.01x slower                                    |
| coverage                   | 54.6 ms                                                 | 55.3 ms: 1.01x slower                                    |
| pickle_pure_python         | 224 us                                                  | 227 us: 1.01x slower                                     |
| nqueens                    | 54.0 ms                                                 | 54.8 ms: 1.02x slower                                    |
| unpickle_pure_python       | 155 us                                                  | 158 us: 1.02x slower                                     |
| regex_compile              | 90.1 ms                                                 | 91.7 ms: 1.02x slower                                    |
| sympy_expand               | 327 ms                                                  | 333 ms: 1.02x slower                                     |
| sqlglot_v2_parse           | 894 us                                                  | 911 us: 1.02x slower                                     |
| deepcopy_reduce            | 1.98 us                                                 | 2.02 us: 1.02x slower                                    |
| typing_runtime_protocols   | 107 us                                                  | 109 us: 1.02x slower                                     |
| telco                      | 5.15 ms                                                 | 5.27 ms: 1.02x slower                                    |
| comprehensions             | 10.8 us                                                 | 11.1 us: 1.03x slower                                    |
| richards                   | 31.0 ms                                                 | 31.8 ms: 1.03x slower                                    |
| django_template            | 27.9 ms                                                 | 28.7 ms: 1.03x slower                                    |
| deepcopy_memo              | 18.0 us                                                 | 18.6 us: 1.03x slower                                    |
| genshi_text                | 16.0 ms                                                 | 16.5 ms: 1.03x slower                                    |
| pprint_safe_repr           | 464 ms                                                  | 480 ms: 1.04x slower                                     |
| json_loads                 | 17.4 us                                                 | 18.1 us: 1.04x slower                                    |
| sqlite_synth               | 1.56 us                                                 | 1.62 us: 1.04x slower                                    |
| coroutines                 | 14.5 ms                                                 | 15.2 ms: 1.04x slower                                    |
| deepcopy                   | 185 us                                                  | 193 us: 1.04x slower                                     |
| pprint_pformat             | 943 ms                                                  | 988 ms: 1.05x slower                                     |
| json                       | 3.35 ms                                                 | 3.58 ms: 1.07x slower                                    |
| mako                       | 7.37 ms                                                 | 8.03 ms: 1.09x slower                                    |
| Geometric mean             | (ref)                                                   | 1.00x slower                                             |

Benchmark hidden because not significant (13): async_tree_memoization_tg, connected_components, async_tree_eager, async_tree_eager_cpu_io_mixed, gc_traversal, async_tree_none, mdp, sympy_sum, sympy_str, float, sphinx, async_generators, async_tree_eager_memoization_tg

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 54.92% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x
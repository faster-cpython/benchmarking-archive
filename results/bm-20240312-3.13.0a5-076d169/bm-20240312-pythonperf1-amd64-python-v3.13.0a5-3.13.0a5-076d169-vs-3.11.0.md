# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a5
- machine: windows-amd64
- commit hash: 076d169
- commit date: 2024-03-12
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 216 ms: 1.01x slower                                            |
| chameleon      | 5.26 ms                                                     | 4.84 ms: 1.09x faster                                           |
| docutils       | 1.64 sec                                                    | 1.54 sec: 1.07x faster                                          |
| html5lib       | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                           |
| tornado_http   | 92.8 ms                                                     | 84.8 ms: 1.09x faster                                           |
| Geometric mean | (ref)                                                       | 1.06x faster                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 270 ms: 1.23x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 340 ms: 1.17x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 454 ms: 1.17x faster                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 349 ms: 1.16x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 274 ms: 1.13x faster                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 474 ms: 1.10x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 758 ms: 1.09x faster                                            |
| async_tree_io              | 808 ms                                                      | 738 ms: 1.09x faster                                            |
| Geometric mean             | (ref)                                                       | 1.14x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 50.8 ms: 1.07x faster                                           |
| nbody          | 70.3 ms                                                     | 68.2 ms: 1.03x faster                                           |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                            |
| Geometric mean | (ref)                                                       | 1.04x faster                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 78.2 ms: 1.16x faster                                           |
| regex_dna      | 116 ms                                                      | 118 ms: 1.02x slower                                            |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                           |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.10x slower                                           |
| Geometric mean | (ref)                                                       | 1.00x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.63 ms: 1.44x faster                                           |
| unpickle_pure_python | 157 us                                                      | 125 us: 1.26x faster                                            |
| pickle_pure_python   | 208 us                                                      | 180 us: 1.16x faster                                            |
| xml_etree_parse      | 97.6 ms                                                     | 93.6 ms: 1.04x faster                                           |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.9 ms: 1.04x faster                                           |
| tomli_loads          | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                          |
| xml_etree_process    | 37.2 ms                                                     | 36.7 ms: 1.01x faster                                           |
| xml_etree_generate   | 52.5 ms                                                     | 53.8 ms: 1.02x slower                                           |
| unpickle_list        | 2.59 us                                                     | 2.68 us: 1.04x slower                                           |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                           |
| pickle_list          | 2.70 us                                                     | 2.90 us: 1.07x slower                                           |
| pickle               | 6.64 us                                                     | 7.17 us: 1.08x slower                                           |
| unpickle             | 7.57 us                                                     | 8.29 us: 1.09x slower                                           |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                    |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                           |
| python_startup_no_site | 16.8 ms                                                     | 18.1 ms: 1.08x slower                                           |
| Geometric mean         | (ref)                                                       | 1.05x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.21 ms: 1.22x faster                                           |
| genshi_text     | 18.4 ms                                                     | 15.8 ms: 1.17x faster                                           |
| genshi_xml      | 39.9 ms                                                     | 34.6 ms: 1.15x faster                                           |
| django_template | 24.4 ms                                                     | 22.1 ms: 1.11x faster                                           |
| Geometric mean  | (ref)                                                       | 1.16x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1-amd64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 75.1 us: 4.34x faster                                           |
| generators                 | 34.0 ms                                                     | 20.6 ms: 1.65x faster                                           |
| pylint                     | 323 ms                                                      | 206 ms: 1.57x faster                                            |
| asyncio_tcp                | 726 ms                                                      | 478 ms: 1.52x faster                                            |
| json_dumps                 | 8.09 ms                                                     | 5.63 ms: 1.44x faster                                           |
| comprehensions             | 15.6 us                                                     | 11.0 us: 1.42x faster                                           |
| deltablue                  | 2.70 ms                                                     | 1.98 ms: 1.37x faster                                           |
| logging_silent             | 71.8 ns                                                     | 53.5 ns: 1.34x faster                                           |
| raytrace                   | 213 ms                                                      | 160 ms: 1.33x faster                                            |
| richards_super             | 38.7 ms                                                     | 30.6 ms: 1.26x faster                                           |
| chaos                      | 48.4 ms                                                     | 38.4 ms: 1.26x faster                                           |
| unpickle_pure_python       | 157 us                                                      | 125 us: 1.26x faster                                            |
| sqlglot_parse              | 953 us                                                      | 762 us: 1.25x faster                                            |
| async_tree_none            | 332 ms                                                      | 270 ms: 1.23x faster                                            |
| mako                       | 7.58 ms                                                     | 6.21 ms: 1.22x faster                                           |
| sympy_sum                  | 100 ms                                                      | 82.9 ms: 1.21x faster                                           |
| sqlglot_transpile          | 1.16 ms                                                     | 980 us: 1.19x faster                                            |
| sympy_str                  | 185 ms                                                      | 158 ms: 1.17x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 340 ms: 1.17x faster                                            |
| go                         | 101 ms                                                      | 86.1 ms: 1.17x faster                                           |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 454 ms: 1.17x faster                                            |
| genshi_text                | 18.4 ms                                                     | 15.8 ms: 1.17x faster                                           |
| deepcopy_memo              | 26.0 us                                                     | 22.3 us: 1.16x faster                                           |
| regex_compile              | 91.0 ms                                                     | 78.2 ms: 1.16x faster                                           |
| hexiom                     | 4.55 ms                                                     | 3.91 ms: 1.16x faster                                           |
| mdp                        | 1.59 sec                                                    | 1.37 sec: 1.16x faster                                          |
| async_tree_memoization_tg  | 405 ms                                                      | 349 ms: 1.16x faster                                            |
| pickle_pure_python         | 208 us                                                      | 180 us: 1.16x faster                                            |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.2 ms: 1.16x faster                                           |
| genshi_xml                 | 39.9 ms                                                     | 34.6 ms: 1.15x faster                                           |
| dulwich_log                | 46.4 ms                                                     | 40.4 ms: 1.15x faster                                           |
| logging_simple             | 6.86 us                                                     | 5.97 us: 1.15x faster                                           |
| crypto_pyaes               | 48.9 ms                                                     | 42.6 ms: 1.15x faster                                           |
| spectral_norm              | 68.3 ms                                                     | 59.7 ms: 1.15x faster                                           |
| richards                   | 31.4 ms                                                     | 27.5 ms: 1.14x faster                                           |
| nqueens                    | 68.3 ms                                                     | 59.9 ms: 1.14x faster                                           |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.14x faster                                           |
| sympy_integrate            | 14.0 ms                                                     | 12.3 ms: 1.14x faster                                           |
| scimark_lu                 | 62.8 ms                                                     | 55.5 ms: 1.13x faster                                           |
| async_tree_none_tg         | 309 ms                                                      | 274 ms: 1.13x faster                                            |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.80 sec: 1.12x faster                                          |
| deepcopy                   | 246 us                                                      | 220 us: 1.12x faster                                            |
| logging_format             | 7.16 us                                                     | 6.41 us: 1.12x faster                                           |
| sqlite_synth               | 1.77 us                                                     | 1.59 us: 1.11x faster                                           |
| mypy2                      | 459 ms                                                      | 413 ms: 1.11x faster                                            |
| pyflate                    | 312 ms                                                      | 281 ms: 1.11x faster                                            |
| sympy_expand               | 299 ms                                                      | 270 ms: 1.11x faster                                            |
| django_template            | 24.4 ms                                                     | 22.1 ms: 1.11x faster                                           |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 474 ms: 1.10x faster                                            |
| sqlglot_normalize          | 190 ms                                                      | 172 ms: 1.10x faster                                            |
| pprint_pformat             | 1.09 sec                                                    | 992 ms: 1.10x faster                                            |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.35 ms: 1.10x faster                                           |
| tornado_http               | 92.8 ms                                                     | 84.8 ms: 1.09x faster                                           |
| async_tree_io_tg           | 829 ms                                                      | 758 ms: 1.09x faster                                            |
| async_tree_io              | 808 ms                                                      | 738 ms: 1.09x faster                                            |
| chameleon                  | 5.26 ms                                                     | 4.84 ms: 1.09x faster                                           |
| pprint_safe_repr           | 529 ms                                                      | 487 ms: 1.09x faster                                            |
| float                      | 54.4 ms                                                     | 50.8 ms: 1.07x faster                                           |
| docutils                   | 1.64 sec                                                    | 1.54 sec: 1.07x faster                                          |
| html5lib                   | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                           |
| deepcopy_reduce            | 2.06 us                                                     | 1.95 us: 1.06x faster                                           |
| sqlglot_optimize           | 34.5 ms                                                     | 32.6 ms: 1.06x faster                                           |
| bench_thread_pool          | 872 us                                                      | 831 us: 1.05x faster                                            |
| xml_etree_parse            | 97.6 ms                                                     | 93.6 ms: 1.04x faster                                           |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.9 ms: 1.04x faster                                           |
| fannkuch                   | 253 ms                                                      | 243 ms: 1.04x faster                                            |
| scimark_fft                | 179 ms                                                      | 172 ms: 1.04x faster                                            |
| pycparser                  | 720 ms                                                      | 693 ms: 1.04x faster                                            |
| scimark_sor                | 78.1 ms                                                     | 75.4 ms: 1.04x faster                                           |
| meteor_contest             | 75.2 ms                                                     | 72.8 ms: 1.03x faster                                           |
| nbody                      | 70.3 ms                                                     | 68.2 ms: 1.03x faster                                           |
| tomli_loads                | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                          |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                            |
| xml_etree_process          | 37.2 ms                                                     | 36.7 ms: 1.01x faster                                           |
| 2to3                       | 214 ms                                                      | 216 ms: 1.01x slower                                            |
| aiohttp                    | 883 us                                                      | 896 us: 1.01x slower                                            |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.02x slower                                            |
| xml_etree_generate         | 52.5 ms                                                     | 53.8 ms: 1.02x slower                                           |
| python_startup             | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                           |
| unpickle_list              | 2.59 us                                                     | 2.68 us: 1.04x slower                                           |
| create_gc_cycles           | 713 us                                                      | 745 us: 1.04x slower                                            |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                           |
| bench_mp_pool              | 63.2 ms                                                     | 66.6 ms: 1.05x slower                                           |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                           |
| pickle_list                | 2.70 us                                                     | 2.90 us: 1.07x slower                                           |
| python_startup_no_site     | 16.8 ms                                                     | 18.1 ms: 1.08x slower                                           |
| pickle                     | 6.64 us                                                     | 7.17 us: 1.08x slower                                           |
| coverage                   | 43.4 ms                                                     | 47.1 ms: 1.09x slower                                           |
| json                       | 2.98 ms                                                     | 3.23 ms: 1.09x slower                                           |
| unpickle                   | 7.57 us                                                     | 8.29 us: 1.09x slower                                           |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.10x slower                                           |
| pathlib                    | 70.9 ms                                                     | 80.3 ms: 1.13x slower                                           |
| telco                      | 4.06 ms                                                     | 4.75 ms: 1.17x slower                                           |
| async_generators           | 177 ms                                                      | 224 ms: 1.27x slower                                            |
| thrift                     | 494 us                                                      | 8.19 ms: 16.59x slower                                          |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                    |

Benchmark hidden because not significant (3): flaskblogging, pickle_dict, gc_traversal
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown
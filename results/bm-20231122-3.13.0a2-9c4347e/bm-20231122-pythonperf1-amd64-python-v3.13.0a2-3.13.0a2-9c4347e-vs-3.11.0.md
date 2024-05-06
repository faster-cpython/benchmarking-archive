# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a2
- machine: windows-amd64
- commit hash: 9c4347e
- commit date: 2023-11-22
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1-amd64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 210 ms: 1.02x faster                                            |
| chameleon      | 5.26 ms                                                     | 4.81 ms: 1.09x faster                                           |
| docutils       | 1.64 sec                                                    | 1.55 sec: 1.06x faster                                          |
| html5lib       | 38.9 ms                                                     | 36.6 ms: 1.06x faster                                           |
| tornado_http   | 92.8 ms                                                     | 86.1 ms: 1.08x faster                                           |
| Geometric mean | (ref)                                                       | 1.06x faster                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1-amd64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 264 ms: 1.26x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 341 ms: 1.17x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 453 ms: 1.17x faster                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 361 ms: 1.12x faster                                            |
| async_tree_io              | 808 ms                                                      | 731 ms: 1.11x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 281 ms: 1.10x faster                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 482 ms: 1.08x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 769 ms: 1.08x faster                                            |
| Geometric mean             | (ref)                                                       | 1.13x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1-amd64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 52.3 ms: 1.04x faster                                           |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                            |
| nbody          | 70.3 ms                                                     | 72.0 ms: 1.02x slower                                           |
| Geometric mean | (ref)                                                       | 1.01x faster                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1-amd64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 78.9 ms: 1.15x faster                                           |
| regex_dna      | 116 ms                                                      | 122 ms: 1.05x slower                                            |
| regex_v8       | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                           |
| regex_effbot   | 1.50 ms                                                     | 1.62 ms: 1.08x slower                                           |
| Geometric mean | (ref)                                                       | 1.02x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1-amd64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.50 ms: 1.47x faster                                           |
| unpickle_pure_python | 157 us                                                      | 128 us: 1.23x faster                                            |
| pickle_pure_python   | 208 us                                                      | 179 us: 1.17x faster                                            |
| tomli_loads          | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                          |
| xml_etree_parse      | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                           |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                           |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.5 ms: 1.02x faster                                           |
| xml_etree_generate   | 52.5 ms                                                     | 53.2 ms: 1.01x slower                                           |
| json_loads           | 13.0 us                                                     | 13.4 us: 1.03x slower                                           |
| unpickle_list        | 2.59 us                                                     | 2.70 us: 1.05x slower                                           |
| pickle               | 6.64 us                                                     | 6.94 us: 1.05x slower                                           |
| pickle_list          | 2.70 us                                                     | 2.83 us: 1.05x slower                                           |
| unpickle             | 7.57 us                                                     | 8.09 us: 1.07x slower                                           |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                    |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1-amd64-python-v3.13.0a2-3.13.0a2-9c4347e |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.6 ms: 1.05x slower                                           |
| Geometric mean         | (ref)                                                       | 1.03x slower                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1-amd64-python-v3.13.0a2-3.13.0a2-9c4347e |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 15.0 ms: 1.23x faster                                           |
| genshi_xml      | 39.9 ms                                                     | 33.1 ms: 1.21x faster                                           |
| mako            | 7.58 ms                                                     | 6.48 ms: 1.17x faster                                           |
| django_template | 24.4 ms                                                     | 21.9 ms: 1.11x faster                                           |
| Geometric mean  | (ref)                                                       | 1.18x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1-amd64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 73.9 us: 4.41x faster                                           |
| generators                 | 34.0 ms                                                     | 20.0 ms: 1.70x faster                                           |
| pylint                     | 323 ms                                                      | 202 ms: 1.60x faster                                            |
| asyncio_tcp                | 726 ms                                                      | 465 ms: 1.56x faster                                            |
| comprehensions             | 15.6 us                                                     | 10.3 us: 1.52x faster                                           |
| json_dumps                 | 8.09 ms                                                     | 5.50 ms: 1.47x faster                                           |
| deltablue                  | 2.70 ms                                                     | 2.01 ms: 1.34x faster                                           |
| logging_silent             | 71.8 ns                                                     | 54.1 ns: 1.33x faster                                           |
| raytrace                   | 213 ms                                                      | 163 ms: 1.31x faster                                            |
| sqlglot_parse              | 953 us                                                      | 752 us: 1.27x faster                                            |
| async_tree_none            | 332 ms                                                      | 264 ms: 1.26x faster                                            |
| richards_super             | 38.7 ms                                                     | 30.8 ms: 1.26x faster                                           |
| chaos                      | 48.4 ms                                                     | 39.2 ms: 1.23x faster                                           |
| genshi_text                | 18.4 ms                                                     | 15.0 ms: 1.23x faster                                           |
| unpickle_pure_python       | 157 us                                                      | 128 us: 1.23x faster                                            |
| sympy_sum                  | 100 ms                                                      | 82.3 ms: 1.22x faster                                           |
| sqlglot_transpile          | 1.16 ms                                                     | 965 us: 1.21x faster                                            |
| genshi_xml                 | 39.9 ms                                                     | 33.1 ms: 1.21x faster                                           |
| go                         | 101 ms                                                      | 84.3 ms: 1.20x faster                                           |
| hexiom                     | 4.55 ms                                                     | 3.81 ms: 1.20x faster                                           |
| sympy_str                  | 185 ms                                                      | 156 ms: 1.18x faster                                            |
| mdp                        | 1.59 sec                                                    | 1.36 sec: 1.17x faster                                          |
| nqueens                    | 68.3 ms                                                     | 58.2 ms: 1.17x faster                                           |
| async_tree_memoization     | 399 ms                                                      | 341 ms: 1.17x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 453 ms: 1.17x faster                                            |
| mako                       | 7.58 ms                                                     | 6.48 ms: 1.17x faster                                           |
| pickle_pure_python         | 208 us                                                      | 179 us: 1.17x faster                                            |
| regex_compile              | 91.0 ms                                                     | 78.9 ms: 1.15x faster                                           |
| sympy_integrate            | 14.0 ms                                                     | 12.2 ms: 1.15x faster                                           |
| richards                   | 31.4 ms                                                     | 27.3 ms: 1.15x faster                                           |
| sqlite_synth               | 1.77 us                                                     | 1.56 us: 1.13x faster                                           |
| logging_simple             | 6.86 us                                                     | 6.07 us: 1.13x faster                                           |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                           |
| deepcopy                   | 246 us                                                      | 218 us: 1.13x faster                                            |
| crypto_pyaes               | 48.9 ms                                                     | 43.3 ms: 1.13x faster                                           |
| async_tree_memoization_tg  | 405 ms                                                      | 361 ms: 1.12x faster                                            |
| dulwich_log                | 46.4 ms                                                     | 41.4 ms: 1.12x faster                                           |
| django_template            | 24.4 ms                                                     | 21.9 ms: 1.11x faster                                           |
| scimark_lu                 | 62.8 ms                                                     | 56.4 ms: 1.11x faster                                           |
| sympy_expand               | 299 ms                                                      | 269 ms: 1.11x faster                                            |
| pprint_pformat             | 1.09 sec                                                    | 979 ms: 1.11x faster                                            |
| sqlglot_normalize          | 190 ms                                                      | 171 ms: 1.11x faster                                            |
| scimark_monte_carlo        | 45.3 ms                                                     | 40.9 ms: 1.11x faster                                           |
| pprint_safe_repr           | 529 ms                                                      | 479 ms: 1.11x faster                                            |
| async_tree_io              | 808 ms                                                      | 731 ms: 1.11x faster                                            |
| deepcopy_memo              | 26.0 us                                                     | 23.5 us: 1.10x faster                                           |
| logging_format             | 7.16 us                                                     | 6.51 us: 1.10x faster                                           |
| async_tree_none_tg         | 309 ms                                                      | 281 ms: 1.10x faster                                            |
| chameleon                  | 5.26 ms                                                     | 4.81 ms: 1.09x faster                                           |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 482 ms: 1.08x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 769 ms: 1.08x faster                                            |
| tornado_http               | 92.8 ms                                                     | 86.1 ms: 1.08x faster                                           |
| pyflate                    | 312 ms                                                      | 291 ms: 1.07x faster                                            |
| spectral_norm              | 68.3 ms                                                     | 63.6 ms: 1.07x faster                                           |
| tomli_loads                | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                          |
| sqlglot_optimize           | 34.5 ms                                                     | 32.5 ms: 1.06x faster                                           |
| html5lib                   | 38.9 ms                                                     | 36.6 ms: 1.06x faster                                           |
| docutils                   | 1.64 sec                                                    | 1.55 sec: 1.06x faster                                          |
| xml_etree_parse            | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                           |
| deepcopy_reduce            | 2.06 us                                                     | 1.95 us: 1.06x faster                                           |
| fannkuch                   | 253 ms                                                      | 241 ms: 1.05x faster                                            |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.46 ms: 1.05x faster                                           |
| float                      | 54.4 ms                                                     | 52.3 ms: 1.04x faster                                           |
| meteor_contest             | 75.2 ms                                                     | 72.6 ms: 1.04x faster                                           |
| bench_thread_pool          | 872 us                                                      | 848 us: 1.03x faster                                            |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                           |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                            |
| 2to3                       | 214 ms                                                      | 210 ms: 1.02x faster                                            |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.5 ms: 1.02x faster                                           |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                          |
| xml_etree_generate         | 52.5 ms                                                     | 53.2 ms: 1.01x slower                                           |
| bench_mp_pool              | 63.2 ms                                                     | 64.0 ms: 1.01x slower                                           |
| gc_traversal               | 1.49 ms                                                     | 1.52 ms: 1.02x slower                                           |
| nbody                      | 70.3 ms                                                     | 72.0 ms: 1.02x slower                                           |
| scimark_fft                | 179 ms                                                      | 184 ms: 1.03x slower                                            |
| json_loads                 | 13.0 us                                                     | 13.4 us: 1.03x slower                                           |
| unpickle_list              | 2.59 us                                                     | 2.70 us: 1.05x slower                                           |
| create_gc_cycles           | 713 us                                                      | 746 us: 1.05x slower                                            |
| pickle                     | 6.64 us                                                     | 6.94 us: 1.05x slower                                           |
| python_startup_no_site     | 16.8 ms                                                     | 17.6 ms: 1.05x slower                                           |
| pickle_list                | 2.70 us                                                     | 2.83 us: 1.05x slower                                           |
| regex_dna                  | 116 ms                                                      | 122 ms: 1.05x slower                                            |
| coverage                   | 43.4 ms                                                     | 45.8 ms: 1.05x slower                                           |
| unpickle                   | 7.57 us                                                     | 8.09 us: 1.07x slower                                           |
| regex_v8                   | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                           |
| regex_effbot               | 1.50 ms                                                     | 1.62 ms: 1.08x slower                                           |
| scimark_sor                | 78.1 ms                                                     | 85.4 ms: 1.09x slower                                           |
| telco                      | 4.06 ms                                                     | 4.57 ms: 1.12x slower                                           |
| pathlib                    | 70.9 ms                                                     | 79.9 ms: 1.13x slower                                           |
| mypy2                      | 459 ms                                                      | 584 ms: 1.27x slower                                            |
| async_generators           | 177 ms                                                      | 227 ms: 1.28x slower                                            |
| thrift                     | 494 us                                                      | 8.35 ms: 16.91x slower                                          |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                    |

Benchmark hidden because not significant (6): json, asyncio_tcp_ssl, pycparser, aiohttp, python_startup, pickle_dict
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown
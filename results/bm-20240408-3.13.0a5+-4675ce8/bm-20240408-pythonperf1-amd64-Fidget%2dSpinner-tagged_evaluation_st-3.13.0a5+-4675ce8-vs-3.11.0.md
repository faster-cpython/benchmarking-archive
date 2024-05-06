# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-amd64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.04x faster
- HPT reliability: 99.71%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 220 ms: 1.03x slower                                                                  |
| chameleon      | 5.26 ms                                                     | 5.55 ms: 1.05x slower                                                                 |
| docutils       | 1.64 sec                                                    | 1.70 sec: 1.04x slower                                                                |
| html5lib       | 38.9 ms                                                     | 38.0 ms: 1.02x faster                                                                 |
| tornado_http   | 92.8 ms                                                     | 84.1 ms: 1.10x faster                                                                 |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 280 ms: 1.45x faster                                                                  |
| async_tree_none            | 332 ms                                                      | 232 ms: 1.43x faster                                                                  |
| async_tree_memoization     | 399 ms                                                      | 281 ms: 1.42x faster                                                                  |
| async_tree_io              | 808 ms                                                      | 581 ms: 1.39x faster                                                                  |
| async_tree_none_tg         | 309 ms                                                      | 229 ms: 1.35x faster                                                                  |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 391 ms: 1.34x faster                                                                  |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 403 ms: 1.31x faster                                                                  |
| async_tree_io_tg           | 829 ms                                                      | 631 ms: 1.31x faster                                                                  |
| Geometric mean             | (ref)                                                       | 1.37x faster                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 53.0 ms: 1.03x faster                                                                 |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                                  |
| nbody          | 70.3 ms                                                     | 76.0 ms: 1.08x slower                                                                 |
| Geometric mean | (ref)                                                       | 1.01x slower                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 82.6 ms: 1.10x faster                                                                 |
| regex_dna      | 116 ms                                                      | 119 ms: 1.02x slower                                                                  |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.04x slower                                                                 |
| regex_v8       | 14.2 ms                                                     | 18.0 ms: 1.27x slower                                                                 |
| Geometric mean | (ref)                                                       | 1.05x slower                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 6.07 ms: 1.33x faster                                                                 |
| unpickle_pure_python | 157 us                                                      | 139 us: 1.13x faster                                                                  |
| xml_etree_parse      | 97.6 ms                                                     | 90.9 ms: 1.07x faster                                                                 |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.6 ms: 1.02x faster                                                                 |
| pickle_pure_python   | 208 us                                                      | 206 us: 1.01x faster                                                                  |
| tomli_loads          | 1.46 sec                                                    | 1.45 sec: 1.01x faster                                                                |
| pickle_dict          | 18.5 us                                                     | 18.9 us: 1.02x slower                                                                 |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                                 |
| unpickle_list        | 2.59 us                                                     | 2.85 us: 1.10x slower                                                                 |
| pickle               | 6.64 us                                                     | 7.35 us: 1.11x slower                                                                 |
| pickle_list          | 2.70 us                                                     | 3.00 us: 1.11x slower                                                                 |
| unpickle             | 7.57 us                                                     | 8.48 us: 1.12x slower                                                                 |
| xml_etree_generate   | 52.5 ms                                                     | 59.0 ms: 1.12x slower                                                                 |
| xml_etree_process    | 37.2 ms                                                     | 41.7 ms: 1.12x slower                                                                 |
| Geometric mean       | (ref)                                                       | 1.02x slower                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 20.1 ms: 1.02x slower                                                                 |
| python_startup_no_site | 16.8 ms                                                     | 17.9 ms: 1.06x slower                                                                 |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 6.46 ms: 1.17x faster                                                                 |
| genshi_xml     | 39.9 ms                                                     | 37.7 ms: 1.06x faster                                                                 |
| genshi_text    | 18.4 ms                                                     | 17.9 ms: 1.03x faster                                                                 |
| Geometric mean | (ref)                                                       | 1.09x faster                                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 75.9 us: 4.29x faster                                                                 |
| pylint                     | 323 ms                                                      | 193 ms: 1.68x faster                                                                  |
| asyncio_tcp                | 726 ms                                                      | 476 ms: 1.52x faster                                                                  |
| generators                 | 34.0 ms                                                     | 23.4 ms: 1.45x faster                                                                 |
| async_tree_memoization_tg  | 405 ms                                                      | 280 ms: 1.45x faster                                                                  |
| async_tree_none            | 332 ms                                                      | 232 ms: 1.43x faster                                                                  |
| async_tree_memoization     | 399 ms                                                      | 281 ms: 1.42x faster                                                                  |
| async_tree_io              | 808 ms                                                      | 581 ms: 1.39x faster                                                                  |
| async_tree_none_tg         | 309 ms                                                      | 229 ms: 1.35x faster                                                                  |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 391 ms: 1.34x faster                                                                  |
| json_dumps                 | 8.09 ms                                                     | 6.07 ms: 1.33x faster                                                                 |
| deltablue                  | 2.70 ms                                                     | 2.05 ms: 1.32x faster                                                                 |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 403 ms: 1.31x faster                                                                  |
| async_tree_io_tg           | 829 ms                                                      | 631 ms: 1.31x faster                                                                  |
| logging_silent             | 71.8 ns                                                     | 55.7 ns: 1.29x faster                                                                 |
| comprehensions             | 15.6 us                                                     | 12.2 us: 1.28x faster                                                                 |
| richards_super             | 38.7 ms                                                     | 30.9 ms: 1.25x faster                                                                 |
| raytrace                   | 213 ms                                                      | 174 ms: 1.23x faster                                                                  |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.72 sec: 1.18x faster                                                                |
| sqlglot_parse              | 953 us                                                      | 811 us: 1.18x faster                                                                  |
| mako                       | 7.58 ms                                                     | 6.46 ms: 1.17x faster                                                                 |
| go                         | 101 ms                                                      | 88.0 ms: 1.15x faster                                                                 |
| chaos                      | 48.4 ms                                                     | 42.1 ms: 1.15x faster                                                                 |
| richards                   | 31.4 ms                                                     | 27.5 ms: 1.14x faster                                                                 |
| sqlglot_transpile          | 1.16 ms                                                     | 1.03 ms: 1.13x faster                                                                 |
| deepcopy_memo              | 26.0 us                                                     | 22.9 us: 1.13x faster                                                                 |
| unpickle_pure_python       | 157 us                                                      | 139 us: 1.13x faster                                                                  |
| sympy_sum                  | 100 ms                                                      | 88.8 ms: 1.13x faster                                                                 |
| hexiom                     | 4.55 ms                                                     | 4.07 ms: 1.12x faster                                                                 |
| tornado_http               | 92.8 ms                                                     | 84.1 ms: 1.10x faster                                                                 |
| regex_compile              | 91.0 ms                                                     | 82.6 ms: 1.10x faster                                                                 |
| logging_simple             | 6.86 us                                                     | 6.24 us: 1.10x faster                                                                 |
| sympy_str                  | 185 ms                                                      | 170 ms: 1.09x faster                                                                  |
| dulwich_log                | 46.4 ms                                                     | 42.6 ms: 1.09x faster                                                                 |
| sympy_integrate            | 14.0 ms                                                     | 12.9 ms: 1.09x faster                                                                 |
| mdp                        | 1.59 sec                                                    | 1.47 sec: 1.08x faster                                                                |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.9 ms: 1.08x faster                                                                 |
| spectral_norm              | 68.3 ms                                                     | 63.3 ms: 1.08x faster                                                                 |
| xml_etree_parse            | 97.6 ms                                                     | 90.9 ms: 1.07x faster                                                                 |
| logging_format             | 7.16 us                                                     | 6.67 us: 1.07x faster                                                                 |
| bench_thread_pool          | 872 us                                                      | 822 us: 1.06x faster                                                                  |
| genshi_xml                 | 39.9 ms                                                     | 37.7 ms: 1.06x faster                                                                 |
| mypy2                      | 459 ms                                                      | 435 ms: 1.05x faster                                                                  |
| scimark_lu                 | 62.8 ms                                                     | 59.6 ms: 1.05x faster                                                                 |
| deepcopy                   | 246 us                                                      | 235 us: 1.05x faster                                                                  |
| pyflate                    | 312 ms                                                      | 299 ms: 1.04x faster                                                                  |
| sympy_expand               | 299 ms                                                      | 287 ms: 1.04x faster                                                                  |
| sqlite_synth               | 1.77 us                                                     | 1.71 us: 1.04x faster                                                                 |
| nqueens                    | 68.3 ms                                                     | 66.3 ms: 1.03x faster                                                                 |
| genshi_text                | 18.4 ms                                                     | 17.9 ms: 1.03x faster                                                                 |
| float                      | 54.4 ms                                                     | 53.0 ms: 1.03x faster                                                                 |
| html5lib                   | 38.9 ms                                                     | 38.0 ms: 1.02x faster                                                                 |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                                  |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.6 ms: 1.02x faster                                                                 |
| pickle_pure_python         | 208 us                                                      | 206 us: 1.01x faster                                                                  |
| tomli_loads                | 1.46 sec                                                    | 1.45 sec: 1.01x faster                                                                |
| sqlglot_normalize          | 190 ms                                                      | 191 ms: 1.00x slower                                                                  |
| crypto_pyaes               | 48.9 ms                                                     | 49.1 ms: 1.01x slower                                                                 |
| coroutines                 | 15.0 ms                                                     | 15.2 ms: 1.01x slower                                                                 |
| python_startup             | 19.8 ms                                                     | 20.1 ms: 1.02x slower                                                                 |
| meteor_contest             | 75.2 ms                                                     | 76.5 ms: 1.02x slower                                                                 |
| scimark_sor                | 78.1 ms                                                     | 79.5 ms: 1.02x slower                                                                 |
| scimark_fft                | 179 ms                                                      | 183 ms: 1.02x slower                                                                  |
| pickle_dict                | 18.5 us                                                     | 18.9 us: 1.02x slower                                                                 |
| aiohttp                    | 883 us                                                      | 901 us: 1.02x slower                                                                  |
| bench_mp_pool              | 63.2 ms                                                     | 64.5 ms: 1.02x slower                                                                 |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.02x slower                                                                  |
| pprint_pformat             | 1.09 sec                                                    | 1.11 sec: 1.02x slower                                                                |
| gc_traversal               | 1.49 ms                                                     | 1.53 ms: 1.03x slower                                                                 |
| pprint_safe_repr           | 529 ms                                                      | 544 ms: 1.03x slower                                                                  |
| 2to3                       | 214 ms                                                      | 220 ms: 1.03x slower                                                                  |
| docutils                   | 1.64 sec                                                    | 1.70 sec: 1.04x slower                                                                |
| sqlglot_optimize           | 34.5 ms                                                     | 35.9 ms: 1.04x slower                                                                 |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.68 ms: 1.04x slower                                                                 |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.04x slower                                                                 |
| chameleon                  | 5.26 ms                                                     | 5.55 ms: 1.05x slower                                                                 |
| deepcopy_reduce            | 2.06 us                                                     | 2.18 us: 1.06x slower                                                                 |
| python_startup_no_site     | 16.8 ms                                                     | 17.9 ms: 1.06x slower                                                                 |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                                 |
| nbody                      | 70.3 ms                                                     | 76.0 ms: 1.08x slower                                                                 |
| coverage                   | 43.4 ms                                                     | 47.7 ms: 1.10x slower                                                                 |
| unpickle_list              | 2.59 us                                                     | 2.85 us: 1.10x slower                                                                 |
| pathlib                    | 70.9 ms                                                     | 78.2 ms: 1.10x slower                                                                 |
| pickle                     | 6.64 us                                                     | 7.35 us: 1.11x slower                                                                 |
| pickle_list                | 2.70 us                                                     | 3.00 us: 1.11x slower                                                                 |
| unpickle                   | 7.57 us                                                     | 8.48 us: 1.12x slower                                                                 |
| xml_etree_generate         | 52.5 ms                                                     | 59.0 ms: 1.12x slower                                                                 |
| xml_etree_process          | 37.2 ms                                                     | 41.7 ms: 1.12x slower                                                                 |
| fannkuch                   | 253 ms                                                      | 297 ms: 1.17x slower                                                                  |
| create_gc_cycles           | 713 us                                                      | 887 us: 1.24x slower                                                                  |
| regex_v8                   | 14.2 ms                                                     | 18.0 ms: 1.27x slower                                                                 |
| telco                      | 4.06 ms                                                     | 5.40 ms: 1.33x slower                                                                 |
| async_generators           | 177 ms                                                      | 238 ms: 1.34x slower                                                                  |
| thrift                     | 494 us                                                      | 8.77 ms: 17.77x slower                                                                |
| Geometric mean             | (ref)                                                       | 1.04x faster                                                                          |

Benchmark hidden because not significant (2): json, pycparser
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.71% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
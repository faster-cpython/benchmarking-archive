# Results vs. 3.12.0

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-amd64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.01x faster
- HPT reliability: 79.03%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 220 ms: 1.01x slower                                                                  |
| chameleon      | 4.98 ms                                                     | 5.55 ms: 1.11x slower                                                                 |
| docutils       | 1.66 sec                                                    | 1.70 sec: 1.02x slower                                                                |
| tornado_http   | 89.5 ms                                                     | 84.1 ms: 1.06x faster                                                                 |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 280 ms: 1.31x faster                                                                  |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 391 ms: 1.29x faster                                                                  |
| async_tree_io              | 731 ms                                                      | 581 ms: 1.26x faster                                                                  |
| async_tree_none            | 291 ms                                                      | 232 ms: 1.25x faster                                                                  |
| async_tree_none_tg         | 285 ms                                                      | 229 ms: 1.25x faster                                                                  |
| async_tree_io_tg           | 771 ms                                                      | 631 ms: 1.22x faster                                                                  |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 403 ms: 1.21x faster                                                                  |
| async_tree_memoization     | 339 ms                                                      | 281 ms: 1.21x faster                                                                  |
| Geometric mean             | (ref)                                                       | 1.25x faster                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 53.0 ms: 1.07x faster                                                                 |
| pidigits       | 152 ms                                                      | 147 ms: 1.03x faster                                                                  |
| nbody          | 71.9 ms                                                     | 76.0 ms: 1.06x slower                                                                 |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 119 ms: 1.06x faster                                                                  |
| regex_compile  | 87.5 ms                                                     | 82.6 ms: 1.06x faster                                                                 |
| regex_effbot   | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                                 |
| regex_v8       | 14.2 ms                                                     | 18.0 ms: 1.26x slower                                                                 |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| xml_etree_parse      | 93.0 ms                                                     | 90.9 ms: 1.02x faster                                                                 |
| pickle               | 7.43 us                                                     | 7.35 us: 1.01x faster                                                                 |
| xml_etree_iterparse  | 65.2 ms                                                     | 64.6 ms: 1.01x faster                                                                 |
| pickle_dict          | 18.4 us                                                     | 18.9 us: 1.02x slower                                                                 |
| unpickle             | 8.18 us                                                     | 8.48 us: 1.04x slower                                                                 |
| unpickle_list        | 2.75 us                                                     | 2.85 us: 1.04x slower                                                                 |
| unpickle_pure_python | 133 us                                                      | 139 us: 1.04x slower                                                                  |
| pickle_pure_python   | 195 us                                                      | 206 us: 1.05x slower                                                                  |
| xml_etree_generate   | 55.8 ms                                                     | 59.0 ms: 1.06x slower                                                                 |
| tomli_loads          | 1.37 sec                                                    | 1.45 sec: 1.06x slower                                                                |
| pickle_list          | 2.83 us                                                     | 3.00 us: 1.06x slower                                                                 |
| json_dumps           | 5.70 ms                                                     | 6.07 ms: 1.07x slower                                                                 |
| xml_etree_process    | 37.7 ms                                                     | 41.7 ms: 1.11x slower                                                                 |
| Geometric mean       | (ref)                                                       | 1.04x slower                                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 20.1 ms: 1.03x slower                                                                 |
| python_startup_no_site | 16.2 ms                                                     | 17.9 ms: 1.10x slower                                                                 |
| Geometric mean         | (ref)                                                       | 1.07x slower                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-----------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 6.46 ms: 1.10x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 280 ms: 1.31x faster                                                                  |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 391 ms: 1.29x faster                                                                  |
| async_tree_io              | 731 ms                                                      | 581 ms: 1.26x faster                                                                  |
| async_tree_none            | 291 ms                                                      | 232 ms: 1.25x faster                                                                  |
| typing_runtime_protocols   | 95.1 us                                                     | 75.9 us: 1.25x faster                                                                 |
| async_tree_none_tg         | 285 ms                                                      | 229 ms: 1.25x faster                                                                  |
| async_tree_io_tg           | 771 ms                                                      | 631 ms: 1.22x faster                                                                  |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.72 sec: 1.22x faster                                                                |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 403 ms: 1.21x faster                                                                  |
| async_tree_memoization     | 339 ms                                                      | 281 ms: 1.21x faster                                                                  |
| mypy2                      | 509 ms                                                      | 435 ms: 1.17x faster                                                                  |
| comprehensions             | 14.1 us                                                     | 12.2 us: 1.16x faster                                                                 |
| raytrace                   | 192 ms                                                      | 174 ms: 1.10x faster                                                                  |
| mako                       | 7.09 ms                                                     | 6.46 ms: 1.10x faster                                                                 |
| logging_silent             | 60.5 ns                                                     | 55.7 ns: 1.09x faster                                                                 |
| float                      | 56.8 ms                                                     | 53.0 ms: 1.07x faster                                                                 |
| bench_mp_pool              | 69.2 ms                                                     | 64.5 ms: 1.07x faster                                                                 |
| tornado_http               | 89.5 ms                                                     | 84.1 ms: 1.06x faster                                                                 |
| regex_dna                  | 126 ms                                                      | 119 ms: 1.06x faster                                                                  |
| regex_compile              | 87.5 ms                                                     | 82.6 ms: 1.06x faster                                                                 |
| spectral_norm              | 66.9 ms                                                     | 63.3 ms: 1.06x faster                                                                 |
| deltablue                  | 2.16 ms                                                     | 2.05 ms: 1.05x faster                                                                 |
| scimark_monte_carlo        | 43.7 ms                                                     | 41.9 ms: 1.04x faster                                                                 |
| bench_thread_pool          | 857 us                                                      | 822 us: 1.04x faster                                                                  |
| go                         | 91.6 ms                                                     | 88.0 ms: 1.04x faster                                                                 |
| dulwich_log                | 44.3 ms                                                     | 42.6 ms: 1.04x faster                                                                 |
| richards_super             | 32.1 ms                                                     | 30.9 ms: 1.04x faster                                                                 |
| regex_effbot               | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                                 |
| deepcopy_memo              | 23.7 us                                                     | 22.9 us: 1.03x faster                                                                 |
| richards                   | 28.4 ms                                                     | 27.5 ms: 1.03x faster                                                                 |
| sqlite_synth               | 1.76 us                                                     | 1.71 us: 1.03x faster                                                                 |
| pidigits                   | 152 ms                                                      | 147 ms: 1.03x faster                                                                  |
| sympy_sum                  | 91.5 ms                                                     | 88.8 ms: 1.03x faster                                                                 |
| sympy_str                  | 175 ms                                                      | 170 ms: 1.03x faster                                                                  |
| pathlib                    | 80.5 ms                                                     | 78.2 ms: 1.03x faster                                                                 |
| chaos                      | 43.3 ms                                                     | 42.1 ms: 1.03x faster                                                                 |
| xml_etree_parse            | 93.0 ms                                                     | 90.9 ms: 1.02x faster                                                                 |
| deepcopy                   | 238 us                                                      | 235 us: 1.01x faster                                                                  |
| pickle                     | 7.43 us                                                     | 7.35 us: 1.01x faster                                                                 |
| scimark_fft                | 184 ms                                                      | 183 ms: 1.01x faster                                                                  |
| json                       | 3.05 ms                                                     | 3.02 ms: 1.01x faster                                                                 |
| xml_etree_iterparse        | 65.2 ms                                                     | 64.6 ms: 1.01x faster                                                                 |
| async_generators           | 239 ms                                                      | 238 ms: 1.01x faster                                                                  |
| hexiom                     | 4.10 ms                                                     | 4.07 ms: 1.01x faster                                                                 |
| logging_format             | 6.72 us                                                     | 6.67 us: 1.01x faster                                                                 |
| logging_simple             | 6.28 us                                                     | 6.24 us: 1.01x faster                                                                 |
| sympy_integrate            | 13.0 ms                                                     | 12.9 ms: 1.00x faster                                                                 |
| sqlglot_transpile          | 1.02 ms                                                     | 1.03 ms: 1.01x slower                                                                 |
| gc_traversal               | 1.52 ms                                                     | 1.53 ms: 1.01x slower                                                                 |
| sqlglot_parse              | 804 us                                                      | 811 us: 1.01x slower                                                                  |
| scimark_sor                | 78.8 ms                                                     | 79.5 ms: 1.01x slower                                                                 |
| 2to3                       | 218 ms                                                      | 220 ms: 1.01x slower                                                                  |
| sympy_expand               | 284 ms                                                      | 287 ms: 1.01x slower                                                                  |
| scimark_lu                 | 58.9 ms                                                     | 59.6 ms: 1.01x slower                                                                 |
| crypto_pyaes               | 48.5 ms                                                     | 49.1 ms: 1.01x slower                                                                 |
| pyflate                    | 295 ms                                                      | 299 ms: 1.02x slower                                                                  |
| aiohttp                    | 884 us                                                      | 901 us: 1.02x slower                                                                  |
| sqlglot_normalize          | 187 ms                                                      | 191 ms: 1.02x slower                                                                  |
| docutils                   | 1.66 sec                                                    | 1.70 sec: 1.02x slower                                                                |
| pickle_dict                | 18.4 us                                                     | 18.9 us: 1.02x slower                                                                 |
| meteor_contest             | 74.6 ms                                                     | 76.5 ms: 1.03x slower                                                                 |
| python_startup             | 19.5 ms                                                     | 20.1 ms: 1.03x slower                                                                 |
| unpickle                   | 8.18 us                                                     | 8.48 us: 1.04x slower                                                                 |
| generators                 | 22.5 ms                                                     | 23.4 ms: 1.04x slower                                                                 |
| unpickle_list              | 2.75 us                                                     | 2.85 us: 1.04x slower                                                                 |
| sqlglot_optimize           | 34.5 ms                                                     | 35.9 ms: 1.04x slower                                                                 |
| deepcopy_reduce            | 2.09 us                                                     | 2.18 us: 1.04x slower                                                                 |
| unpickle_pure_python       | 133 us                                                      | 139 us: 1.04x slower                                                                  |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.68 ms: 1.05x slower                                                                 |
| pickle_pure_python         | 195 us                                                      | 206 us: 1.05x slower                                                                  |
| nqueens                    | 62.8 ms                                                     | 66.3 ms: 1.06x slower                                                                 |
| xml_etree_generate         | 55.8 ms                                                     | 59.0 ms: 1.06x slower                                                                 |
| nbody                      | 71.9 ms                                                     | 76.0 ms: 1.06x slower                                                                 |
| tomli_loads                | 1.37 sec                                                    | 1.45 sec: 1.06x slower                                                                |
| pprint_safe_repr           | 513 ms                                                      | 544 ms: 1.06x slower                                                                  |
| pickle_list                | 2.83 us                                                     | 3.00 us: 1.06x slower                                                                 |
| pycparser                  | 699 ms                                                      | 742 ms: 1.06x slower                                                                  |
| coroutines                 | 14.3 ms                                                     | 15.2 ms: 1.06x slower                                                                 |
| pprint_pformat             | 1.05 sec                                                    | 1.11 sec: 1.06x slower                                                                |
| json_dumps                 | 5.70 ms                                                     | 6.07 ms: 1.07x slower                                                                 |
| mdp                        | 1.37 sec                                                    | 1.47 sec: 1.07x slower                                                                |
| python_startup_no_site     | 16.2 ms                                                     | 17.9 ms: 1.10x slower                                                                 |
| xml_etree_process          | 37.7 ms                                                     | 41.7 ms: 1.11x slower                                                                 |
| chameleon                  | 4.98 ms                                                     | 5.55 ms: 1.11x slower                                                                 |
| coverage                   | 40.8 ms                                                     | 47.7 ms: 1.17x slower                                                                 |
| create_gc_cycles           | 752 us                                                      | 887 us: 1.18x slower                                                                  |
| fannkuch                   | 247 ms                                                      | 297 ms: 1.20x slower                                                                  |
| regex_v8                   | 14.2 ms                                                     | 18.0 ms: 1.26x slower                                                                 |
| telco                      | 4.13 ms                                                     | 5.40 ms: 1.31x slower                                                                 |
| Geometric mean             | (ref)                                                       | 1.01x faster                                                                          |

Benchmark hidden because not significant (2): asyncio_tcp, json_loads
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240408-3.13.0a5+-4675ce8/bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 79.03% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
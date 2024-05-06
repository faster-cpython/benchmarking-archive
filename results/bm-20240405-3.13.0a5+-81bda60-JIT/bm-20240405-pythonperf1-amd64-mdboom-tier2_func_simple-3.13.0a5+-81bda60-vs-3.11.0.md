# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple
- machine: windows-amd64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 219 ms: 1.02x slower                                                     |
| chameleon      | 5.26 ms                                                     | 4.70 ms: 1.12x faster                                                    |
| docutils       | 1.64 sec                                                    | 1.68 sec: 1.03x slower                                                   |
| html5lib       | 38.9 ms                                                     | 35.7 ms: 1.09x faster                                                    |
| tornado_http   | 92.8 ms                                                     | 84.2 ms: 1.10x faster                                                    |
| Geometric mean | (ref)                                                       | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 262 ms: 1.54x faster                                                     |
| async_tree_none            | 332 ms                                                      | 222 ms: 1.50x faster                                                     |
| async_tree_memoization     | 399 ms                                                      | 274 ms: 1.46x faster                                                     |
| async_tree_none_tg         | 309 ms                                                      | 214 ms: 1.44x faster                                                     |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 612 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 393 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.34x faster                                                     |
| Geometric mean             | (ref)                                                       | 1.42x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 56.9 ms: 1.24x faster                                                    |
| float          | 54.4 ms                                                     | 46.5 ms: 1.17x faster                                                    |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                       | 1.14x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 87.0 ms: 1.05x faster                                                    |
| regex_v8       | 14.2 ms                                                     | 14.1 ms: 1.01x faster                                                    |
| regex_dna      | 116 ms                                                      | 118 ms: 1.02x slower                                                     |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                       | 1.00x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.51 ms: 1.47x faster                                                    |
| tomli_loads          | 1.46 sec                                                    | 1.18 sec: 1.24x faster                                                   |
| unpickle_pure_python | 157 us                                                      | 129 us: 1.21x faster                                                     |
| pickle_pure_python   | 208 us                                                      | 174 us: 1.20x faster                                                     |
| xml_etree_parse      | 97.6 ms                                                     | 92.9 ms: 1.05x faster                                                    |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.6 ms: 1.05x faster                                                    |
| xml_etree_process    | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                    |
| xml_etree_generate   | 52.5 ms                                                     | 52.8 ms: 1.00x slower                                                    |
| pickle_dict          | 18.5 us                                                     | 18.6 us: 1.01x slower                                                    |
| unpickle_list        | 2.59 us                                                     | 2.74 us: 1.06x slower                                                    |
| json_loads           | 13.0 us                                                     | 14.0 us: 1.07x slower                                                    |
| pickle               | 6.64 us                                                     | 7.16 us: 1.08x slower                                                    |
| pickle_list          | 2.70 us                                                     | 2.93 us: 1.09x slower                                                    |
| unpickle             | 7.57 us                                                     | 9.17 us: 1.21x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 21.6 ms: 1.09x slower                                                    |
| python_startup_no_site | 16.8 ms                                                     | 19.5 ms: 1.16x slower                                                    |
| Geometric mean         | (ref)                                                       | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 5.68 ms: 1.34x faster                                                    |
| genshi_xml     | 39.9 ms                                                     | 33.2 ms: 1.20x faster                                                    |
| genshi_text    | 18.4 ms                                                     | 15.3 ms: 1.20x faster                                                    |
| Geometric mean | (ref)                                                       | 1.25x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 70.7 us: 4.61x faster                                                    |
| generators                 | 34.0 ms                                                     | 19.8 ms: 1.71x faster                                                    |
| pylint                     | 323 ms                                                      | 194 ms: 1.67x faster                                                     |
| asyncio_tcp                | 726 ms                                                      | 470 ms: 1.54x faster                                                     |
| async_tree_memoization_tg  | 405 ms                                                      | 262 ms: 1.54x faster                                                     |
| async_tree_none            | 332 ms                                                      | 222 ms: 1.50x faster                                                     |
| json_dumps                 | 8.09 ms                                                     | 5.51 ms: 1.47x faster                                                    |
| async_tree_memoization     | 399 ms                                                      | 274 ms: 1.46x faster                                                     |
| async_tree_none_tg         | 309 ms                                                      | 214 ms: 1.44x faster                                                     |
| comprehensions             | 15.6 us                                                     | 11.0 us: 1.42x faster                                                    |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                                     |
| logging_silent             | 71.8 ns                                                     | 52.9 ns: 1.36x faster                                                    |
| async_tree_io_tg           | 829 ms                                                      | 612 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 393 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.34x faster                                                     |
| mako                       | 7.58 ms                                                     | 5.68 ms: 1.34x faster                                                    |
| spectral_norm              | 68.3 ms                                                     | 51.4 ms: 1.33x faster                                                    |
| raytrace                   | 213 ms                                                      | 161 ms: 1.32x faster                                                     |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.58 sec: 1.29x faster                                                   |
| chaos                      | 48.4 ms                                                     | 38.3 ms: 1.26x faster                                                    |
| deltablue                  | 2.70 ms                                                     | 2.16 ms: 1.25x faster                                                    |
| richards_super             | 38.7 ms                                                     | 31.1 ms: 1.24x faster                                                    |
| tomli_loads                | 1.46 sec                                                    | 1.18 sec: 1.24x faster                                                   |
| nbody                      | 70.3 ms                                                     | 56.9 ms: 1.24x faster                                                    |
| deepcopy_memo              | 26.0 us                                                     | 21.0 us: 1.24x faster                                                    |
| sqlglot_parse              | 953 us                                                      | 781 us: 1.22x faster                                                     |
| unpickle_pure_python       | 157 us                                                      | 129 us: 1.21x faster                                                     |
| genshi_xml                 | 39.9 ms                                                     | 33.2 ms: 1.20x faster                                                    |
| logging_simple             | 6.86 us                                                     | 5.70 us: 1.20x faster                                                    |
| genshi_text                | 18.4 ms                                                     | 15.3 ms: 1.20x faster                                                    |
| pickle_pure_python         | 208 us                                                      | 174 us: 1.20x faster                                                     |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.2 ms: 1.19x faster                                                    |
| float                      | 54.4 ms                                                     | 46.5 ms: 1.17x faster                                                    |
| sqlglot_transpile          | 1.16 ms                                                     | 998 us: 1.17x faster                                                     |
| logging_format             | 7.16 us                                                     | 6.15 us: 1.16x faster                                                    |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.23 ms: 1.16x faster                                                    |
| coroutines                 | 15.0 ms                                                     | 13.0 ms: 1.15x faster                                                    |
| pyflate                    | 312 ms                                                      | 272 ms: 1.15x faster                                                     |
| nqueens                    | 68.3 ms                                                     | 60.1 ms: 1.14x faster                                                    |
| pprint_pformat             | 1.09 sec                                                    | 958 ms: 1.14x faster                                                     |
| richards                   | 31.4 ms                                                     | 27.7 ms: 1.13x faster                                                    |
| dulwich_log                | 46.4 ms                                                     | 41.0 ms: 1.13x faster                                                    |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.13x faster                                                    |
| deepcopy                   | 246 us                                                      | 220 us: 1.12x faster                                                     |
| sympy_sum                  | 100 ms                                                      | 89.2 ms: 1.12x faster                                                    |
| chameleon                  | 5.26 ms                                                     | 4.70 ms: 1.12x faster                                                    |
| fannkuch                   | 253 ms                                                      | 228 ms: 1.11x faster                                                     |
| sympy_str                  | 185 ms                                                      | 167 ms: 1.11x faster                                                     |
| crypto_pyaes               | 48.9 ms                                                     | 44.1 ms: 1.11x faster                                                    |
| pprint_safe_repr           | 529 ms                                                      | 479 ms: 1.11x faster                                                     |
| tornado_http               | 92.8 ms                                                     | 84.2 ms: 1.10x faster                                                    |
| go                         | 101 ms                                                      | 92.1 ms: 1.10x faster                                                    |
| html5lib                   | 38.9 ms                                                     | 35.7 ms: 1.09x faster                                                    |
| mdp                        | 1.59 sec                                                    | 1.46 sec: 1.09x faster                                                   |
| bench_thread_pool          | 872 us                                                      | 806 us: 1.08x faster                                                     |
| scimark_fft                | 179 ms                                                      | 167 ms: 1.07x faster                                                     |
| sympy_expand               | 299 ms                                                      | 283 ms: 1.06x faster                                                     |
| sympy_integrate            | 14.0 ms                                                     | 13.3 ms: 1.06x faster                                                    |
| sqlglot_normalize          | 190 ms                                                      | 180 ms: 1.06x faster                                                     |
| xml_etree_parse            | 97.6 ms                                                     | 92.9 ms: 1.05x faster                                                    |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.6 ms: 1.05x faster                                                    |
| regex_compile              | 91.0 ms                                                     | 87.0 ms: 1.05x faster                                                    |
| meteor_contest             | 75.2 ms                                                     | 72.1 ms: 1.04x faster                                                    |
| deepcopy_reduce            | 2.06 us                                                     | 1.98 us: 1.04x faster                                                    |
| pycparser                  | 720 ms                                                      | 694 ms: 1.04x faster                                                     |
| hexiom                     | 4.55 ms                                                     | 4.42 ms: 1.03x faster                                                    |
| mypy2                      | 459 ms                                                      | 449 ms: 1.02x faster                                                     |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                     |
| xml_etree_process          | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                    |
| regex_v8                   | 14.2 ms                                                     | 14.1 ms: 1.01x faster                                                    |
| xml_etree_generate         | 52.5 ms                                                     | 52.8 ms: 1.00x slower                                                    |
| pickle_dict                | 18.5 us                                                     | 18.6 us: 1.01x slower                                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 34.8 ms: 1.01x slower                                                    |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.02x slower                                                     |
| 2to3                       | 214 ms                                                      | 219 ms: 1.02x slower                                                     |
| docutils                   | 1.64 sec                                                    | 1.68 sec: 1.03x slower                                                   |
| aiohttp                    | 883 us                                                      | 911 us: 1.03x slower                                                     |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                    |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                    |
| scimark_sor                | 78.1 ms                                                     | 82.8 ms: 1.06x slower                                                    |
| unpickle_list              | 2.59 us                                                     | 2.74 us: 1.06x slower                                                    |
| bench_mp_pool              | 63.2 ms                                                     | 67.7 ms: 1.07x slower                                                    |
| json_loads                 | 13.0 us                                                     | 14.0 us: 1.07x slower                                                    |
| pickle                     | 6.64 us                                                     | 7.16 us: 1.08x slower                                                    |
| pickle_list                | 2.70 us                                                     | 2.93 us: 1.09x slower                                                    |
| python_startup             | 19.8 ms                                                     | 21.6 ms: 1.09x slower                                                    |
| coverage                   | 43.4 ms                                                     | 47.5 ms: 1.09x slower                                                    |
| pathlib                    | 70.9 ms                                                     | 78.0 ms: 1.10x slower                                                    |
| scimark_lu                 | 62.8 ms                                                     | 71.4 ms: 1.14x slower                                                    |
| python_startup_no_site     | 16.8 ms                                                     | 19.5 ms: 1.16x slower                                                    |
| telco                      | 4.06 ms                                                     | 4.75 ms: 1.17x slower                                                    |
| unpickle                   | 7.57 us                                                     | 9.17 us: 1.21x slower                                                    |
| create_gc_cycles           | 713 us                                                      | 898 us: 1.26x slower                                                     |
| async_generators           | 177 ms                                                      | 233 ms: 1.32x slower                                                     |
| thrift                     | 494 us                                                      | 8.79 ms: 17.80x slower                                                   |
| Geometric mean             | (ref)                                                       | 1.10x faster                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown
# Results vs. 3.11.0

- fork: savannahostrowski
- ref: llvm_18
- machine: windows-amd64
- commit hash: 8d9855f
- commit date: 2024-04-26
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 228 ms: 1.07x slower                                                      |
| chameleon      | 5.26 ms                                                     | 4.77 ms: 1.10x faster                                                     |
| docutils       | 1.64 sec                                                    | 1.72 sec: 1.05x slower                                                    |
| html5lib       | 38.9 ms                                                     | 35.4 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                       | 1.01x faster                                                              |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 271 ms: 1.49x faster                                                      |
| async_tree_none            | 332 ms                                                      | 224 ms: 1.48x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 272 ms: 1.47x faster                                                      |
| async_tree_none_tg         | 309 ms                                                      | 217 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                      |
| async_tree_io              | 808 ms                                                      | 599 ms: 1.35x faster                                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 396 ms: 1.34x faster                                                      |
| async_tree_io_tg           | 829 ms                                                      | 625 ms: 1.33x faster                                                      |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 45.9 ms: 1.18x faster                                                     |
| nbody          | 70.3 ms                                                     | 62.4 ms: 1.13x faster                                                     |
| pidigits       | 150 ms                                                      | 148 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                       | 1.11x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 88.0 ms: 1.03x faster                                                     |
| regex_dna      | 116 ms                                                      | 120 ms: 1.03x slower                                                      |
| regex_effbot   | 1.50 ms                                                     | 1.60 ms: 1.07x slower                                                     |
| regex_v8       | 14.2 ms                                                     | 15.6 ms: 1.10x slower                                                     |
| Geometric mean | (ref)                                                       | 1.04x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.67 ms: 1.43x faster                                                     |
| unpickle_pure_python | 157 us                                                      | 123 us: 1.27x faster                                                      |
| tomli_loads          | 1.46 sec                                                    | 1.18 sec: 1.23x faster                                                    |
| pickle_pure_python   | 208 us                                                      | 173 us: 1.20x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.6 ms: 1.07x faster                                                     |
| xml_etree_parse      | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                                     |
| xml_etree_process    | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                                     |
| pickle_dict          | 18.5 us                                                     | 18.7 us: 1.01x slower                                                     |
| xml_etree_generate   | 52.5 ms                                                     | 54.3 ms: 1.03x slower                                                     |
| unpickle_list        | 2.59 us                                                     | 2.79 us: 1.08x slower                                                     |
| json_loads           | 13.0 us                                                     | 14.3 us: 1.10x slower                                                     |
| pickle               | 6.64 us                                                     | 7.39 us: 1.11x slower                                                     |
| unpickle             | 7.57 us                                                     | 8.56 us: 1.13x slower                                                     |
| pickle_list          | 2.70 us                                                     | 3.12 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 18.5 ms: 1.10x slower                                                     |
| python_startup         | 19.8 ms                                                     | 22.4 ms: 1.13x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.12x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.34 ms: 1.42x faster                                                     |
| genshi_text     | 18.4 ms                                                     | 16.7 ms: 1.11x faster                                                     |
| django_template | 24.4 ms                                                     | 22.8 ms: 1.07x faster                                                     |
| genshi_xml      | 39.9 ms                                                     | 39.1 ms: 1.02x faster                                                     |
| Geometric mean  | (ref)                                                       | 1.15x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 113 us: 2.89x faster                                                      |
| generators                 | 34.0 ms                                                     | 20.3 ms: 1.68x faster                                                     |
| async_tree_memoization_tg  | 405 ms                                                      | 271 ms: 1.49x faster                                                      |
| async_tree_none            | 332 ms                                                      | 224 ms: 1.48x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 272 ms: 1.47x faster                                                      |
| comprehensions             | 15.6 us                                                     | 10.7 us: 1.46x faster                                                     |
| pylint                     | 323 ms                                                      | 224 ms: 1.44x faster                                                      |
| json_dumps                 | 8.09 ms                                                     | 5.67 ms: 1.43x faster                                                     |
| async_tree_none_tg         | 309 ms                                                      | 217 ms: 1.42x faster                                                      |
| mako                       | 7.58 ms                                                     | 5.34 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                      |
| spectral_norm              | 68.3 ms                                                     | 50.4 ms: 1.35x faster                                                     |
| async_tree_io              | 808 ms                                                      | 599 ms: 1.35x faster                                                      |
| logging_silent             | 71.8 ns                                                     | 53.4 ns: 1.34x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 396 ms: 1.34x faster                                                      |
| async_tree_io_tg           | 829 ms                                                      | 625 ms: 1.33x faster                                                      |
| richards_super             | 38.7 ms                                                     | 30.2 ms: 1.28x faster                                                     |
| raytrace                   | 213 ms                                                      | 167 ms: 1.28x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 123 us: 1.27x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 770 us: 1.24x faster                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.18 sec: 1.23x faster                                                    |
| deltablue                  | 2.70 ms                                                     | 2.21 ms: 1.22x faster                                                     |
| pickle_pure_python         | 208 us                                                      | 173 us: 1.20x faster                                                      |
| pprint_safe_repr           | 529 ms                                                      | 440 ms: 1.20x faster                                                      |
| pprint_pformat             | 1.09 sec                                                    | 905 ms: 1.20x faster                                                      |
| chaos                      | 48.4 ms                                                     | 40.4 ms: 1.20x faster                                                     |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.2 ms: 1.19x faster                                                     |
| float                      | 54.4 ms                                                     | 45.9 ms: 1.18x faster                                                     |
| deepcopy_memo              | 26.0 us                                                     | 22.0 us: 1.18x faster                                                     |
| sqlglot_transpile          | 1.16 ms                                                     | 993 us: 1.17x faster                                                      |
| coroutines                 | 15.0 ms                                                     | 12.8 ms: 1.17x faster                                                     |
| pyflate                    | 312 ms                                                      | 268 ms: 1.17x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.91 us: 1.16x faster                                                     |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.22 ms: 1.16x faster                                                     |
| richards                   | 31.4 ms                                                     | 27.1 ms: 1.16x faster                                                     |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.76 sec: 1.15x faster                                                    |
| logging_format             | 7.16 us                                                     | 6.34 us: 1.13x faster                                                     |
| nbody                      | 70.3 ms                                                     | 62.4 ms: 1.13x faster                                                     |
| dulwich_log                | 46.4 ms                                                     | 41.2 ms: 1.13x faster                                                     |
| sympy_sum                  | 100 ms                                                      | 89.8 ms: 1.11x faster                                                     |
| genshi_text                | 18.4 ms                                                     | 16.7 ms: 1.11x faster                                                     |
| mdp                        | 1.59 sec                                                    | 1.44 sec: 1.11x faster                                                    |
| crypto_pyaes               | 48.9 ms                                                     | 44.3 ms: 1.10x faster                                                     |
| chameleon                  | 5.26 ms                                                     | 4.77 ms: 1.10x faster                                                     |
| html5lib                   | 38.9 ms                                                     | 35.4 ms: 1.10x faster                                                     |
| fannkuch                   | 253 ms                                                      | 231 ms: 1.10x faster                                                      |
| deepcopy                   | 246 us                                                      | 226 us: 1.09x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.63 us: 1.09x faster                                                     |
| sympy_str                  | 185 ms                                                      | 171 ms: 1.08x faster                                                      |
| asyncio_tcp                | 726 ms                                                      | 670 ms: 1.08x faster                                                      |
| django_template            | 24.4 ms                                                     | 22.8 ms: 1.07x faster                                                     |
| scimark_fft                | 179 ms                                                      | 167 ms: 1.07x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.6 ms: 1.07x faster                                                     |
| deepcopy_reduce            | 2.06 us                                                     | 1.94 us: 1.06x faster                                                     |
| xml_etree_parse            | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                                     |
| nqueens                    | 68.3 ms                                                     | 65.0 ms: 1.05x faster                                                     |
| go                         | 101 ms                                                      | 97.2 ms: 1.04x faster                                                     |
| sqlglot_normalize          | 190 ms                                                      | 183 ms: 1.04x faster                                                      |
| regex_compile              | 91.0 ms                                                     | 88.0 ms: 1.03x faster                                                     |
| sympy_integrate            | 14.0 ms                                                     | 13.6 ms: 1.03x faster                                                     |
| sympy_expand               | 299 ms                                                      | 289 ms: 1.03x faster                                                      |
| bench_thread_pool          | 872 us                                                      | 847 us: 1.03x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 73.2 ms: 1.03x faster                                                     |
| genshi_xml                 | 39.9 ms                                                     | 39.1 ms: 1.02x faster                                                     |
| pidigits                   | 150 ms                                                      | 148 ms: 1.02x faster                                                      |
| xml_etree_process          | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                                     |
| pickle_dict                | 18.5 us                                                     | 18.7 us: 1.01x slower                                                     |
| sqlglot_optimize           | 34.5 ms                                                     | 35.1 ms: 1.01x slower                                                     |
| mypy2                      | 459 ms                                                      | 471 ms: 1.02x slower                                                      |
| coverage                   | 43.4 ms                                                     | 44.7 ms: 1.03x slower                                                     |
| hexiom                     | 4.55 ms                                                     | 4.70 ms: 1.03x slower                                                     |
| xml_etree_generate         | 52.5 ms                                                     | 54.3 ms: 1.03x slower                                                     |
| regex_dna                  | 116 ms                                                      | 120 ms: 1.03x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.72 sec: 1.05x slower                                                    |
| gc_traversal               | 1.49 ms                                                     | 1.58 ms: 1.06x slower                                                     |
| regex_effbot               | 1.50 ms                                                     | 1.60 ms: 1.07x slower                                                     |
| scimark_sor                | 78.1 ms                                                     | 83.4 ms: 1.07x slower                                                     |
| 2to3                       | 214 ms                                                      | 228 ms: 1.07x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.79 us: 1.08x slower                                                     |
| aiohttp                    | 883 us                                                      | 963 us: 1.09x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 15.6 ms: 1.10x slower                                                     |
| json_loads                 | 13.0 us                                                     | 14.3 us: 1.10x slower                                                     |
| bench_mp_pool              | 63.2 ms                                                     | 69.5 ms: 1.10x slower                                                     |
| python_startup_no_site     | 16.8 ms                                                     | 18.5 ms: 1.10x slower                                                     |
| scimark_lu                 | 62.8 ms                                                     | 69.6 ms: 1.11x slower                                                     |
| pickle                     | 6.64 us                                                     | 7.39 us: 1.11x slower                                                     |
| json                       | 2.98 ms                                                     | 3.32 ms: 1.12x slower                                                     |
| unpickle                   | 7.57 us                                                     | 8.56 us: 1.13x slower                                                     |
| python_startup             | 19.8 ms                                                     | 22.4 ms: 1.13x slower                                                     |
| pathlib                    | 70.9 ms                                                     | 80.9 ms: 1.14x slower                                                     |
| pickle_list                | 2.70 us                                                     | 3.12 us: 1.16x slower                                                     |
| telco                      | 4.06 ms                                                     | 4.72 ms: 1.16x slower                                                     |
| create_gc_cycles           | 713 us                                                      | 932 us: 1.31x slower                                                      |
| async_generators           | 177 ms                                                      | 241 ms: 1.36x slower                                                      |
| thrift                     | 494 us                                                      | 9.13 ms: 18.50x slower                                                    |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                              |

Benchmark hidden because not significant (2): pycparser, tornado_http
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown
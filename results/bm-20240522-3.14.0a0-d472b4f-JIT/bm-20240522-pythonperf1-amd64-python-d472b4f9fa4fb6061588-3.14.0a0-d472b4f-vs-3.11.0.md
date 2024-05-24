# Results vs. 3.11.0

- fork: python
- ref: d472b4f9fa4fb6061588
- machine: windows-amd64
- commit hash: d472b4f
- commit date: 2024-05-22
- overall geometric mean: 1.11x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 235 ms: 1.10x slower                                                       |
| chameleon      | 5.26 ms                                                     | 5.13 ms: 1.03x faster                                                      |
| docutils       | 1.64 sec                                                    | 1.79 sec: 1.09x slower                                                     |
| html5lib       | 38.9 ms                                                     | 37.6 ms: 1.03x faster                                                      |
| tornado_http   | 92.8 ms                                                     | 86.0 ms: 1.08x faster                                                      |
| Geometric mean | (ref)                                                       | 1.01x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 212 ms: 1.45x faster                                                       |
| async_tree_none            | 332 ms                                                      | 232 ms: 1.43x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 281 ms: 1.42x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 390 ms: 1.34x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 623 ms: 1.33x faster                                                       |
| async_tree_io              | 808 ms                                                      | 610 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 403 ms: 1.31x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 51.2 ms: 1.37x faster                                                      |
| float          | 54.4 ms                                                     | 45.2 ms: 1.20x faster                                                      |
| pidigits       | 150 ms                                                      | 149 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                       | 1.19x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 89.3 ms: 1.02x faster                                                      |
| regex_dna      | 116 ms                                                      | 122 ms: 1.05x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.60 ms: 1.06x slower                                                      |
| regex_v8       | 14.2 ms                                                     | 16.2 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                       | 1.06x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.66 ms: 1.43x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 129 us: 1.21x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.23 sec: 1.18x faster                                                     |
| xml_etree_iterparse  | 65.6 ms                                                     | 59.8 ms: 1.10x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 89.4 ms: 1.09x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 18.0 us: 1.03x faster                                                      |
| xml_etree_process    | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 51.7 ms: 1.02x faster                                                      |
| pickle_list          | 2.70 us                                                     | 2.80 us: 1.04x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.79 us: 1.08x slower                                                      |
| json_loads           | 13.0 us                                                     | 14.2 us: 1.09x slower                                                      |
| pickle               | 6.64 us                                                     | 7.35 us: 1.11x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.57 us: 1.13x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 18.1 ms: 1.08x slower                                                      |
| python_startup         | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.09x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.03 ms: 1.51x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 18.3 ms: 1.01x faster                                                      |
| django_template | 24.4 ms                                                     | 26.1 ms: 1.07x slower                                                      |
| genshi_xml      | 39.9 ms                                                     | 45.6 ms: 1.14x slower                                                      |
| Geometric mean  | (ref)                                                       | 1.06x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1-amd64-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 114 us: 2.87x faster                                                       |
| generators                 | 34.0 ms                                                     | 21.8 ms: 1.56x faster                                                      |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.53x faster                                                      |
| asyncio_tcp                | 726 ms                                                      | 478 ms: 1.52x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.03 ms: 1.51x faster                                                      |
| spectral_norm              | 68.3 ms                                                     | 45.4 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 212 ms: 1.45x faster                                                       |
| async_tree_none            | 332 ms                                                      | 232 ms: 1.43x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.66 ms: 1.43x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 281 ms: 1.42x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.45 sec: 1.40x faster                                                     |
| nbody                      | 70.3 ms                                                     | 51.2 ms: 1.37x faster                                                      |
| pylint                     | 323 ms                                                      | 238 ms: 1.36x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 390 ms: 1.34x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 623 ms: 1.33x faster                                                       |
| async_tree_io              | 808 ms                                                      | 610 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 403 ms: 1.31x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 56.8 ns: 1.26x faster                                                      |
| deepcopy_memo              | 26.0 us                                                     | 20.9 us: 1.24x faster                                                      |
| scimark_fft                | 179 ms                                                      | 147 ms: 1.22x faster                                                       |
| chaos                      | 48.4 ms                                                     | 39.8 ms: 1.21x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 129 us: 1.21x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.13 ms: 1.21x faster                                                      |
| raytrace                   | 213 ms                                                      | 177 ms: 1.21x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                       |
| pyflate                    | 312 ms                                                      | 259 ms: 1.21x faster                                                       |
| float                      | 54.4 ms                                                     | 45.2 ms: 1.20x faster                                                      |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.1 ms: 1.19x faster                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 41.1 ms: 1.19x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.80 us: 1.18x faster                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.23 sec: 1.18x faster                                                     |
| sqlglot_parse              | 953 us                                                      | 813 us: 1.17x faster                                                       |
| fannkuch                   | 253 ms                                                      | 218 ms: 1.16x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 941 ms: 1.15x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 460 ms: 1.15x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.22 us: 1.15x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.40 sec: 1.14x faster                                                     |
| richards_super             | 38.7 ms                                                     | 34.1 ms: 1.14x faster                                                      |
| deltablue                  | 2.70 ms                                                     | 2.38 ms: 1.13x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.13x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 1.05 ms: 1.11x faster                                                      |
| coroutines                 | 15.0 ms                                                     | 13.6 ms: 1.10x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 59.8 ms: 1.10x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 89.4 ms: 1.09x faster                                                      |
| nqueens                    | 68.3 ms                                                     | 62.7 ms: 1.09x faster                                                      |
| go                         | 101 ms                                                      | 93.6 ms: 1.08x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 86.0 ms: 1.08x faster                                                      |
| sympy_sum                  | 100 ms                                                      | 94.9 ms: 1.05x faster                                                      |
| richards                   | 31.4 ms                                                     | 29.9 ms: 1.05x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 72.0 ms: 1.04x faster                                                      |
| deepcopy                   | 246 us                                                      | 237 us: 1.04x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 37.6 ms: 1.03x faster                                                      |
| sympy_str                  | 185 ms                                                      | 179 ms: 1.03x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 18.0 us: 1.03x faster                                                      |
| chameleon                  | 5.26 ms                                                     | 5.13 ms: 1.03x faster                                                      |
| regex_compile              | 91.0 ms                                                     | 89.3 ms: 1.02x faster                                                      |
| xml_etree_process          | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 51.7 ms: 1.02x faster                                                      |
| genshi_text                | 18.4 ms                                                     | 18.3 ms: 1.01x faster                                                      |
| pidigits                   | 150 ms                                                      | 149 ms: 1.01x faster                                                       |
| coverage                   | 43.4 ms                                                     | 44.4 ms: 1.02x slower                                                      |
| hexiom                     | 4.55 ms                                                     | 4.71 ms: 1.03x slower                                                      |
| pickle_list                | 2.70 us                                                     | 2.80 us: 1.04x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                      |
| thrift                     | 494 us                                                      | 516 us: 1.04x slower                                                       |
| regex_dna                  | 116 ms                                                      | 122 ms: 1.05x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 82.4 ms: 1.06x slower                                                      |
| sympy_expand               | 299 ms                                                      | 315 ms: 1.06x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.60 ms: 1.06x slower                                                      |
| django_template            | 24.4 ms                                                     | 26.1 ms: 1.07x slower                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 18.1 ms: 1.08x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.79 us: 1.08x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 37.3 ms: 1.08x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.79 sec: 1.09x slower                                                     |
| json_loads                 | 13.0 us                                                     | 14.2 us: 1.09x slower                                                      |
| 2to3                       | 214 ms                                                      | 235 ms: 1.10x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.35 us: 1.11x slower                                                      |
| python_startup             | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 70.4 ms: 1.11x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.56 ms: 1.12x slower                                                      |
| pathlib                    | 70.9 ms                                                     | 79.5 ms: 1.12x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.57 us: 1.13x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 16.2 ms: 1.14x slower                                                      |
| genshi_xml                 | 39.9 ms                                                     | 45.6 ms: 1.14x slower                                                      |
| scimark_lu                 | 62.8 ms                                                     | 73.1 ms: 1.16x slower                                                      |
| create_gc_cycles           | 713 us                                                      | 890 us: 1.25x slower                                                       |
| async_generators           | 177 ms                                                      | 252 ms: 1.42x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                               |

Benchmark hidden because not significant (6): bench_thread_pool, json, deepcopy_reduce, flaskblogging, sympy_integrate, pycparser
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown
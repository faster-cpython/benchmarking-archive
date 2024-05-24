# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: 0081bcd
- commit date: 2024-05-23
- overall geometric mean: 1.11x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1-amd64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 233 ms: 1.09x slower                                                     |
| chameleon      | 5.26 ms                                                     | 5.08 ms: 1.04x faster                                                    |
| docutils       | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                                   |
| html5lib       | 38.9 ms                                                     | 37.6 ms: 1.03x faster                                                    |
| tornado_http   | 92.8 ms                                                     | 85.4 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                       | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1-amd64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 275 ms: 1.47x faster                                                     |
| async_tree_none            | 332 ms                                                      | 233 ms: 1.43x faster                                                     |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.42x faster                                                     |
| async_tree_memoization     | 399 ms                                                      | 283 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.34x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 625 ms: 1.33x faster                                                     |
| async_tree_io              | 808 ms                                                      | 611 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 404 ms: 1.31x faster                                                     |
| Geometric mean             | (ref)                                                       | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1-amd64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 51.1 ms: 1.38x faster                                                    |
| float          | 54.4 ms                                                     | 44.6 ms: 1.22x faster                                                    |
| pidigits       | 150 ms                                                      | 149 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                       | 1.19x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1-amd64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 87.4 ms: 1.04x faster                                                    |
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                                     |
| regex_v8       | 14.2 ms                                                     | 14.8 ms: 1.04x slower                                                    |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                       | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1-amd64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.65 ms: 1.43x faster                                                    |
| unpickle_pure_python | 157 us                                                      | 127 us: 1.23x faster                                                     |
| pickle_pure_python   | 208 us                                                      | 173 us: 1.21x faster                                                     |
| tomli_loads          | 1.46 sec                                                    | 1.24 sec: 1.18x faster                                                   |
| xml_etree_iterparse  | 65.6 ms                                                     | 59.8 ms: 1.10x faster                                                    |
| xml_etree_parse      | 97.6 ms                                                     | 89.9 ms: 1.09x faster                                                    |
| pickle_dict          | 18.5 us                                                     | 17.8 us: 1.04x faster                                                    |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                    |
| xml_etree_generate   | 52.5 ms                                                     | 51.5 ms: 1.02x faster                                                    |
| pickle_list          | 2.70 us                                                     | 2.84 us: 1.05x slower                                                    |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                    |
| unpickle_list        | 2.59 us                                                     | 2.79 us: 1.08x slower                                                    |
| pickle               | 6.64 us                                                     | 7.55 us: 1.14x slower                                                    |
| unpickle             | 7.57 us                                                     | 8.68 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1-amd64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 18.2 ms: 1.08x slower                                                    |
| python_startup         | 19.8 ms                                                     | 21.8 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                       | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1-amd64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|-----------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.00 ms: 1.52x faster                                                    |
| genshi_text     | 18.4 ms                                                     | 18.9 ms: 1.03x slower                                                    |
| django_template | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                    |
| genshi_xml      | 39.9 ms                                                     | 46.2 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                       | 1.05x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1-amd64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:-----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 113 us: 2.90x faster                                                     |
| generators                 | 34.0 ms                                                     | 21.3 ms: 1.60x faster                                                    |
| comprehensions             | 15.6 us                                                     | 10.3 us: 1.52x faster                                                    |
| mako                       | 7.58 ms                                                     | 5.00 ms: 1.52x faster                                                    |
| asyncio_tcp                | 726 ms                                                      | 478 ms: 1.52x faster                                                     |
| async_tree_memoization_tg  | 405 ms                                                      | 275 ms: 1.47x faster                                                     |
| json_dumps                 | 8.09 ms                                                     | 5.65 ms: 1.43x faster                                                    |
| spectral_norm              | 68.3 ms                                                     | 47.8 ms: 1.43x faster                                                    |
| async_tree_none            | 332 ms                                                      | 233 ms: 1.43x faster                                                     |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.42x faster                                                     |
| async_tree_memoization     | 399 ms                                                      | 283 ms: 1.41x faster                                                     |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.45 sec: 1.40x faster                                                   |
| nbody                      | 70.3 ms                                                     | 51.1 ms: 1.38x faster                                                    |
| pylint                     | 323 ms                                                      | 237 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.34x faster                                                     |
| async_tree_io_tg           | 829 ms                                                      | 625 ms: 1.33x faster                                                     |
| async_tree_io              | 808 ms                                                      | 611 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 404 ms: 1.31x faster                                                     |
| logging_silent             | 71.8 ns                                                     | 55.5 ns: 1.29x faster                                                    |
| deepcopy_memo              | 26.0 us                                                     | 20.3 us: 1.28x faster                                                    |
| unpickle_pure_python       | 157 us                                                      | 127 us: 1.23x faster                                                     |
| float                      | 54.4 ms                                                     | 44.6 ms: 1.22x faster                                                    |
| raytrace                   | 213 ms                                                      | 176 ms: 1.21x faster                                                     |
| chaos                      | 48.4 ms                                                     | 39.9 ms: 1.21x faster                                                    |
| pyflate                    | 312 ms                                                      | 259 ms: 1.21x faster                                                     |
| pickle_pure_python         | 208 us                                                      | 173 us: 1.21x faster                                                     |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.14 ms: 1.21x faster                                                    |
| scimark_fft                | 179 ms                                                      | 149 ms: 1.20x faster                                                     |
| scimark_monte_carlo        | 45.3 ms                                                     | 37.9 ms: 1.19x faster                                                    |
| crypto_pyaes               | 48.9 ms                                                     | 41.0 ms: 1.19x faster                                                    |
| sqlglot_parse              | 953 us                                                      | 803 us: 1.19x faster                                                     |
| logging_simple             | 6.86 us                                                     | 5.79 us: 1.19x faster                                                    |
| pprint_pformat             | 1.09 sec                                                    | 920 ms: 1.18x faster                                                     |
| tomli_loads                | 1.46 sec                                                    | 1.24 sec: 1.18x faster                                                   |
| pprint_safe_repr           | 529 ms                                                      | 453 ms: 1.17x faster                                                     |
| richards_super             | 38.7 ms                                                     | 33.4 ms: 1.16x faster                                                    |
| logging_format             | 7.16 us                                                     | 6.23 us: 1.15x faster                                                    |
| deltablue                  | 2.70 ms                                                     | 2.37 ms: 1.14x faster                                                    |
| nqueens                    | 68.3 ms                                                     | 60.1 ms: 1.14x faster                                                    |
| sqlglot_transpile          | 1.16 ms                                                     | 1.03 ms: 1.13x faster                                                    |
| fannkuch                   | 253 ms                                                      | 230 ms: 1.10x faster                                                     |
| xml_etree_iterparse        | 65.6 ms                                                     | 59.8 ms: 1.10x faster                                                    |
| coroutines                 | 15.0 ms                                                     | 13.7 ms: 1.10x faster                                                    |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                    |
| tornado_http               | 92.8 ms                                                     | 85.4 ms: 1.09x faster                                                    |
| xml_etree_parse            | 97.6 ms                                                     | 89.9 ms: 1.09x faster                                                    |
| sympy_sum                  | 100 ms                                                      | 93.3 ms: 1.07x faster                                                    |
| mdp                        | 1.59 sec                                                    | 1.49 sec: 1.07x faster                                                   |
| go                         | 101 ms                                                      | 94.5 ms: 1.07x faster                                                    |
| richards                   | 31.4 ms                                                     | 29.5 ms: 1.06x faster                                                    |
| bench_thread_pool          | 872 us                                                      | 833 us: 1.05x faster                                                     |
| meteor_contest             | 75.2 ms                                                     | 72.1 ms: 1.04x faster                                                    |
| regex_compile              | 91.0 ms                                                     | 87.4 ms: 1.04x faster                                                    |
| sympy_str                  | 185 ms                                                      | 178 ms: 1.04x faster                                                     |
| chameleon                  | 5.26 ms                                                     | 5.08 ms: 1.04x faster                                                    |
| pickle_dict                | 18.5 us                                                     | 17.8 us: 1.04x faster                                                    |
| html5lib                   | 38.9 ms                                                     | 37.6 ms: 1.03x faster                                                    |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                    |
| xml_etree_generate         | 52.5 ms                                                     | 51.5 ms: 1.02x faster                                                    |
| deepcopy                   | 246 us                                                      | 242 us: 1.02x faster                                                     |
| sympy_integrate            | 14.0 ms                                                     | 13.9 ms: 1.01x faster                                                    |
| pidigits                   | 150 ms                                                      | 149 ms: 1.00x faster                                                     |
| deepcopy_reduce            | 2.06 us                                                     | 2.09 us: 1.01x slower                                                    |
| hexiom                     | 4.55 ms                                                     | 4.66 ms: 1.02x slower                                                    |
| thrift                     | 494 us                                                      | 506 us: 1.02x slower                                                     |
| genshi_text                | 18.4 ms                                                     | 18.9 ms: 1.03x slower                                                    |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                    |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                                     |
| sympy_expand               | 299 ms                                                      | 312 ms: 1.04x slower                                                     |
| regex_v8                   | 14.2 ms                                                     | 14.8 ms: 1.04x slower                                                    |
| django_template            | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                    |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                    |
| pickle_list                | 2.70 us                                                     | 2.84 us: 1.05x slower                                                    |
| coverage                   | 43.4 ms                                                     | 46.0 ms: 1.06x slower                                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 36.7 ms: 1.06x slower                                                    |
| scimark_sor                | 78.1 ms                                                     | 83.4 ms: 1.07x slower                                                    |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                    |
| unpickle_list              | 2.59 us                                                     | 2.79 us: 1.08x slower                                                    |
| scimark_lu                 | 62.8 ms                                                     | 67.8 ms: 1.08x slower                                                    |
| docutils                   | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                                   |
| python_startup_no_site     | 16.8 ms                                                     | 18.2 ms: 1.08x slower                                                    |
| 2to3                       | 214 ms                                                      | 233 ms: 1.09x slower                                                     |
| python_startup             | 19.8 ms                                                     | 21.8 ms: 1.10x slower                                                    |
| bench_mp_pool              | 63.2 ms                                                     | 70.1 ms: 1.11x slower                                                    |
| pathlib                    | 70.9 ms                                                     | 78.7 ms: 1.11x slower                                                    |
| pycparser                  | 720 ms                                                      | 803 ms: 1.12x slower                                                     |
| telco                      | 4.06 ms                                                     | 4.57 ms: 1.12x slower                                                    |
| pickle                     | 6.64 us                                                     | 7.55 us: 1.14x slower                                                    |
| unpickle                   | 7.57 us                                                     | 8.68 us: 1.15x slower                                                    |
| genshi_xml                 | 39.9 ms                                                     | 46.2 ms: 1.16x slower                                                    |
| create_gc_cycles           | 713 us                                                      | 904 us: 1.27x slower                                                     |
| async_generators           | 177 ms                                                      | 254 ms: 1.44x slower                                                     |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                             |

Benchmark hidden because not significant (2): json, flaskblogging
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown
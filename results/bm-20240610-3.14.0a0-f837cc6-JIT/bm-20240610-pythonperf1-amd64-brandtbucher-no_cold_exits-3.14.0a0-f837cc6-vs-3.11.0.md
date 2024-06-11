# Results vs. 3.11.0

- fork: brandtbucher
- ref: no_cold_exits
- machine: windows-amd64
- commit hash: f837cc6
- commit date: 2024-06-10
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1-amd64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 230 ms: 1.08x slower                                                      |
| docutils       | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                                    |
| html5lib       | 38.9 ms                                                     | 37.2 ms: 1.04x faster                                                     |
| tornado_http   | 92.8 ms                                                     | 85.5 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                       | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1-amd64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 271 ms: 1.49x faster                                                      |
| async_tree_none_tg         | 309 ms                                                      | 213 ms: 1.45x faster                                                      |
| async_tree_none            | 332 ms                                                      | 232 ms: 1.43x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 280 ms: 1.43x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 386 ms: 1.36x faster                                                      |
| async_tree_io_tg           | 829 ms                                                      | 619 ms: 1.34x faster                                                      |
| async_tree_io              | 808 ms                                                      | 610 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 402 ms: 1.32x faster                                                      |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1-amd64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 56.2 ms: 1.25x faster                                                     |
| float          | 54.4 ms                                                     | 44.0 ms: 1.24x faster                                                     |
| Geometric mean | (ref)                                                       | 1.16x faster                                                              |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1-amd64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 88.3 ms: 1.03x faster                                                     |
| regex_v8       | 14.2 ms                                                     | 14.4 ms: 1.01x slower                                                     |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                       | 1.01x slower                                                              |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1-amd64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.62 ms: 1.44x faster                                                     |
| unpickle_pure_python | 157 us                                                      | 128 us: 1.23x faster                                                      |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                      |
| tomli_loads          | 1.46 sec                                                    | 1.22 sec: 1.19x faster                                                    |
| xml_etree_parse      | 97.6 ms                                                     | 92.5 ms: 1.06x faster                                                     |
| pickle_dict          | 18.5 us                                                     | 17.6 us: 1.05x faster                                                     |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                     |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.2 ms: 1.02x faster                                                     |
| xml_etree_generate   | 52.5 ms                                                     | 51.7 ms: 1.02x faster                                                     |
| pickle_list          | 2.70 us                                                     | 2.82 us: 1.05x slower                                                     |
| pickle               | 6.64 us                                                     | 7.25 us: 1.09x slower                                                     |
| json_loads           | 13.0 us                                                     | 14.2 us: 1.10x slower                                                     |
| unpickle_list        | 2.59 us                                                     | 2.87 us: 1.11x slower                                                     |
| unpickle             | 7.57 us                                                     | 8.81 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1-amd64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup | 19.8 ms                                                     | 20.5 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                       | 1.02x slower                                                              |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1-amd64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.25 ms: 1.44x faster                                                     |
| genshi_text     | 18.4 ms                                                     | 18.0 ms: 1.03x faster                                                     |
| django_template | 24.4 ms                                                     | 26.1 ms: 1.07x slower                                                     |
| genshi_xml      | 39.9 ms                                                     | 45.7 ms: 1.14x slower                                                     |
| Geometric mean  | (ref)                                                       | 1.05x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1-amd64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 115 us: 2.84x faster                                                      |
| generators                 | 34.0 ms                                                     | 21.1 ms: 1.61x faster                                                     |
| asyncio_tcp                | 726 ms                                                      | 471 ms: 1.54x faster                                                      |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.53x faster                                                     |
| spectral_norm              | 68.3 ms                                                     | 45.4 ms: 1.50x faster                                                     |
| async_tree_memoization_tg  | 405 ms                                                      | 271 ms: 1.49x faster                                                      |
| async_tree_none_tg         | 309 ms                                                      | 213 ms: 1.45x faster                                                      |
| mako                       | 7.58 ms                                                     | 5.25 ms: 1.44x faster                                                     |
| json_dumps                 | 8.09 ms                                                     | 5.62 ms: 1.44x faster                                                     |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.42 sec: 1.43x faster                                                    |
| async_tree_none            | 332 ms                                                      | 232 ms: 1.43x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 280 ms: 1.43x faster                                                      |
| pylint                     | 323 ms                                                      | 236 ms: 1.37x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 386 ms: 1.36x faster                                                      |
| async_tree_io_tg           | 829 ms                                                      | 619 ms: 1.34x faster                                                      |
| async_tree_io              | 808 ms                                                      | 610 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 402 ms: 1.32x faster                                                      |
| logging_silent             | 71.8 ns                                                     | 54.8 ns: 1.31x faster                                                     |
| deepcopy_memo              | 26.0 us                                                     | 20.7 us: 1.26x faster                                                     |
| nbody                      | 70.3 ms                                                     | 56.2 ms: 1.25x faster                                                     |
| float                      | 54.4 ms                                                     | 44.0 ms: 1.24x faster                                                     |
| richards_super             | 38.7 ms                                                     | 31.4 ms: 1.23x faster                                                     |
| unpickle_pure_python       | 157 us                                                      | 128 us: 1.23x faster                                                      |
| raytrace                   | 213 ms                                                      | 175 ms: 1.22x faster                                                      |
| chaos                      | 48.4 ms                                                     | 39.7 ms: 1.22x faster                                                     |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                      |
| scimark_fft                | 179 ms                                                      | 148 ms: 1.21x faster                                                      |
| pyflate                    | 312 ms                                                      | 259 ms: 1.21x faster                                                      |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.14 ms: 1.20x faster                                                     |
| tomli_loads                | 1.46 sec                                                    | 1.22 sec: 1.19x faster                                                    |
| sqlglot_parse              | 953 us                                                      | 799 us: 1.19x faster                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 41.0 ms: 1.19x faster                                                     |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.2 ms: 1.19x faster                                                     |
| logging_simple             | 6.86 us                                                     | 5.92 us: 1.16x faster                                                     |
| deltablue                  | 2.70 ms                                                     | 2.34 ms: 1.16x faster                                                     |
| pprint_pformat             | 1.09 sec                                                    | 954 ms: 1.14x faster                                                      |
| fannkuch                   | 253 ms                                                      | 223 ms: 1.14x faster                                                      |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.14x faster                                                     |
| mdp                        | 1.59 sec                                                    | 1.40 sec: 1.14x faster                                                    |
| pprint_safe_repr           | 529 ms                                                      | 467 ms: 1.13x faster                                                      |
| richards                   | 31.4 ms                                                     | 27.8 ms: 1.13x faster                                                     |
| sqlglot_transpile          | 1.16 ms                                                     | 1.03 ms: 1.13x faster                                                     |
| logging_format             | 7.16 us                                                     | 6.36 us: 1.13x faster                                                     |
| nqueens                    | 68.3 ms                                                     | 60.8 ms: 1.12x faster                                                     |
| sqlite_synth               | 1.77 us                                                     | 1.59 us: 1.11x faster                                                     |
| go                         | 101 ms                                                      | 92.4 ms: 1.09x faster                                                     |
| tornado_http               | 92.8 ms                                                     | 85.5 ms: 1.09x faster                                                     |
| sympy_sum                  | 100 ms                                                      | 93.3 ms: 1.07x faster                                                     |
| bench_thread_pool          | 872 us                                                      | 817 us: 1.07x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 92.5 ms: 1.06x faster                                                     |
| pickle_dict                | 18.5 us                                                     | 17.6 us: 1.05x faster                                                     |
| html5lib                   | 38.9 ms                                                     | 37.2 ms: 1.04x faster                                                     |
| sympy_str                  | 185 ms                                                      | 178 ms: 1.04x faster                                                      |
| deepcopy                   | 246 us                                                      | 237 us: 1.04x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 72.7 ms: 1.03x faster                                                     |
| regex_compile              | 91.0 ms                                                     | 88.3 ms: 1.03x faster                                                     |
| genshi_text                | 18.4 ms                                                     | 18.0 ms: 1.03x faster                                                     |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                     |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.2 ms: 1.02x faster                                                     |
| xml_etree_generate         | 52.5 ms                                                     | 51.7 ms: 1.02x faster                                                     |
| hexiom                     | 4.55 ms                                                     | 4.60 ms: 1.01x slower                                                     |
| regex_v8                   | 14.2 ms                                                     | 14.4 ms: 1.01x slower                                                     |
| coverage                   | 43.4 ms                                                     | 44.1 ms: 1.02x slower                                                     |
| deepcopy_reduce            | 2.06 us                                                     | 2.11 us: 1.02x slower                                                     |
| sympy_expand               | 299 ms                                                      | 309 ms: 1.03x slower                                                      |
| thrift                     | 494 us                                                      | 511 us: 1.04x slower                                                      |
| python_startup             | 19.8 ms                                                     | 20.5 ms: 1.04x slower                                                     |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                     |
| pickle_list                | 2.70 us                                                     | 2.82 us: 1.05x slower                                                     |
| pycparser                  | 720 ms                                                      | 754 ms: 1.05x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.57 ms: 1.05x slower                                                     |
| sqlglot_optimize           | 34.5 ms                                                     | 36.6 ms: 1.06x slower                                                     |
| pathlib                    | 70.9 ms                                                     | 75.3 ms: 1.06x slower                                                     |
| django_template            | 24.4 ms                                                     | 26.1 ms: 1.07x slower                                                     |
| scimark_sor                | 78.1 ms                                                     | 83.8 ms: 1.07x slower                                                     |
| 2to3                       | 214 ms                                                      | 230 ms: 1.08x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                                    |
| bench_mp_pool              | 63.2 ms                                                     | 68.4 ms: 1.08x slower                                                     |
| pickle                     | 6.64 us                                                     | 7.25 us: 1.09x slower                                                     |
| json_loads                 | 13.0 us                                                     | 14.2 us: 1.10x slower                                                     |
| unpickle_list              | 2.59 us                                                     | 2.87 us: 1.11x slower                                                     |
| scimark_lu                 | 62.8 ms                                                     | 70.4 ms: 1.12x slower                                                     |
| genshi_xml                 | 39.9 ms                                                     | 45.7 ms: 1.14x slower                                                     |
| telco                      | 4.06 ms                                                     | 4.68 ms: 1.15x slower                                                     |
| unpickle                   | 7.57 us                                                     | 8.81 us: 1.16x slower                                                     |
| create_gc_cycles           | 713 us                                                      | 907 us: 1.27x slower                                                      |
| async_generators           | 177 ms                                                      | 257 ms: 1.45x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                              |

Benchmark hidden because not significant (5): sympy_integrate, regex_dna, pidigits, python_startup_no_site, json
Ignored benchmarks (10) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown
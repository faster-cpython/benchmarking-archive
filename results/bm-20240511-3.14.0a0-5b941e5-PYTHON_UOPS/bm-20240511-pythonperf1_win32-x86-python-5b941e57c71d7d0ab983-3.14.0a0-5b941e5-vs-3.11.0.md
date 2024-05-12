# Results vs. 3.11.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: windows-x86
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 255 ms: 1.11x faster                                                           |
| chameleon      | 8.08 ms                                                         | 6.18 ms: 1.31x faster                                                          |
| docutils       | 2.10 sec                                                        | 2.01 sec: 1.05x faster                                                         |
| html5lib       | 54.3 ms                                                         | 50.5 ms: 1.07x faster                                                          |
| tornado_http   | 118 ms                                                          | 99.3 ms: 1.19x faster                                                          |
| Geometric mean | (ref)                                                           | 1.14x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 234 ms: 1.47x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 283 ms: 1.44x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.43x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                           |
| async_tree_io              | 754 ms                                                          | 542 ms: 1.39x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 540 ms: 1.38x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 444 ms: 1.30x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.39x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 75.9 ms: 1.66x faster                                                          |
| float          | 76.1 ms                                                         | 51.9 ms: 1.47x faster                                                          |
| pidigits       | 203 ms                                                          | 198 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                           | 1.35x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 123 ms: 1.20x faster                                                           |
| regex_dna      | 122 ms                                                          | 120 ms: 1.02x faster                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                          |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                          |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.31 sec                                                        | 1.61 sec: 1.44x faster                                                         |
| json_dumps           | 9.80 ms                                                         | 6.92 ms: 1.42x faster                                                          |
| unpickle_pure_python | 231 us                                                          | 168 us: 1.37x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 43.2 ms: 1.27x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 243 us: 1.27x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 60.3 ms: 1.19x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 64.7 ms: 1.17x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 104 ms: 1.10x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 3.02 us: 1.08x faster                                                          |
| pickle               | 7.99 us                                                         | 8.17 us: 1.02x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| json_loads           | 20.0 us                                                         | 20.7 us: 1.04x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.58 us: 1.10x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.3 us: 1.11x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.13x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 19.1 ms: 1.01x slower                                                          |
| python_startup         | 22.0 ms                                                         | 23.0 ms: 1.05x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.03x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.08 ms: 1.45x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 47.7 ms: 1.28x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 21.2 ms: 1.26x faster                                                          |
| django_template | 37.4 ms                                                         | 32.2 ms: 1.16x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.29x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 149 us: 3.22x faster                                                           |
| generators                 | 52.2 ms                                                         | 23.2 ms: 2.25x faster                                                          |
| pylint                     | 418 ms                                                          | 244 ms: 1.72x faster                                                           |
| spectral_norm              | 122 ms                                                          | 72.3 ms: 1.68x faster                                                          |
| nbody                      | 126 ms                                                          | 75.9 ms: 1.66x faster                                                          |
| comprehensions             | 22.1 us                                                         | 13.3 us: 1.65x faster                                                          |
| richards_super             | 58.7 ms                                                         | 35.5 ms: 1.65x faster                                                          |
| logging_silent             | 119 ns                                                          | 74.1 ns: 1.61x faster                                                          |
| chaos                      | 84.4 ms                                                         | 53.4 ms: 1.58x faster                                                          |
| richards                   | 48.8 ms                                                         | 31.0 ms: 1.57x faster                                                          |
| raytrace                   | 327 ms                                                          | 209 ms: 1.57x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 997 us: 1.50x faster                                                           |
| async_tree_none            | 343 ms                                                          | 234 ms: 1.47x faster                                                           |
| float                      | 76.1 ms                                                         | 51.9 ms: 1.47x faster                                                          |
| mako                       | 10.3 ms                                                         | 7.08 ms: 1.45x faster                                                          |
| coroutines                 | 23.7 ms                                                         | 16.4 ms: 1.45x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 27.6 us: 1.45x faster                                                          |
| scimark_sor                | 135 ms                                                          | 93.5 ms: 1.45x faster                                                          |
| fannkuch                   | 399 ms                                                          | 276 ms: 1.45x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.84 ms: 1.44x faster                                                          |
| tomli_loads                | 2.31 sec                                                        | 1.61 sec: 1.44x faster                                                         |
| async_tree_memoization     | 408 ms                                                          | 283 ms: 1.44x faster                                                           |
| scimark_fft                | 291 ms                                                          | 202 ms: 1.44x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.94 ms: 1.44x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.43x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.24 ms: 1.43x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.92 ms: 1.42x faster                                                          |
| nqueens                    | 111 ms                                                          | 79.0 ms: 1.41x faster                                                          |
| logging_simple             | 10.8 us                                                         | 7.70 us: 1.40x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 50.8 ms: 1.39x faster                                                          |
| async_tree_io              | 754 ms                                                          | 542 ms: 1.39x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 540 ms: 1.38x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.32 us: 1.38x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 168 us: 1.37x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 58.5 ms: 1.36x faster                                                          |
| scimark_lu                 | 102 ms                                                          | 77.3 ms: 1.32x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 5.72 ms: 1.31x faster                                                          |
| pprint_pformat             | 1.70 sec                                                        | 1.29 sec: 1.31x faster                                                         |
| pyflate                    | 471 ms                                                          | 360 ms: 1.31x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.18 ms: 1.31x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 630 ms: 1.30x faster                                                           |
| go                         | 147 ms                                                          | 113 ms: 1.30x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 444 ms: 1.30x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 47.7 ms: 1.28x faster                                                          |
| xml_etree_process          | 55.0 ms                                                         | 43.2 ms: 1.27x faster                                                          |
| mdp                        | 2.07 sec                                                        | 1.62 sec: 1.27x faster                                                         |
| pickle_pure_python         | 309 us                                                          | 243 us: 1.27x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 118 ms: 1.27x faster                                                           |
| deepcopy                   | 381 us                                                          | 301 us: 1.27x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 21.2 ms: 1.26x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 854 ms: 1.22x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.73 us: 1.21x faster                                                          |
| sympy_integrate            | 19.9 ms                                                         | 16.5 ms: 1.21x faster                                                          |
| regex_compile              | 148 ms                                                          | 123 ms: 1.20x faster                                                           |
| tornado_http               | 118 ms                                                          | 99.3 ms: 1.19x faster                                                          |
| sqlglot_optimize           | 51.8 ms                                                         | 43.6 ms: 1.19x faster                                                          |
| sympy_str                  | 283 ms                                                          | 238 ms: 1.19x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 60.3 ms: 1.19x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 77.7 ms: 1.17x faster                                                          |
| coverage                   | 58.0 ms                                                         | 49.7 ms: 1.17x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 64.7 ms: 1.17x faster                                                          |
| django_template            | 37.4 ms                                                         | 32.2 ms: 1.16x faster                                                          |
| json                       | 4.78 ms                                                         | 4.23 ms: 1.13x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.92 us: 1.12x faster                                                          |
| 2to3                       | 282 ms                                                          | 255 ms: 1.11x faster                                                           |
| thrift                     | 801 us                                                          | 723 us: 1.11x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 711 ms: 1.11x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 104 ms: 1.10x faster                                                           |
| sympy_expand               | 462 ms                                                          | 423 ms: 1.09x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.05 ms: 1.09x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 3.02 us: 1.08x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 50.5 ms: 1.07x faster                                                          |
| docutils                   | 2.10 sec                                                        | 2.01 sec: 1.05x faster                                                         |
| pidigits                   | 203 ms                                                          | 198 ms: 1.02x faster                                                           |
| regex_dna                  | 122 ms                                                          | 120 ms: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 17.0 sec: 1.01x faster                                                         |
| python_startup_no_site     | 18.8 ms                                                         | 19.1 ms: 1.01x slower                                                          |
| pickle                     | 7.99 us                                                         | 8.17 us: 1.02x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 72.7 ms: 1.02x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| json_loads                 | 20.0 us                                                         | 20.7 us: 1.04x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.05x slower                                                          |
| python_startup             | 22.0 ms                                                         | 23.0 ms: 1.05x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                          |
| pathlib                    | 79.9 ms                                                         | 87.3 ms: 1.09x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.58 us: 1.10x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.3 us: 1.11x slower                                                          |
| async_generators           | 260 ms                                                          | 295 ms: 1.14x slower                                                           |
| telco                      | 5.29 ms                                                         | 6.08 ms: 1.15x slower                                                          |
| create_gc_cycles           | 618 us                                                          | 758 us: 1.23x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 226 ms: 2.00x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.24x faster                                                                   |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.23x
- 95% likely to have a speedup of 1.21x
- 99% likely to have a speedup of 1.19x

# Memory
- memory change: unknown
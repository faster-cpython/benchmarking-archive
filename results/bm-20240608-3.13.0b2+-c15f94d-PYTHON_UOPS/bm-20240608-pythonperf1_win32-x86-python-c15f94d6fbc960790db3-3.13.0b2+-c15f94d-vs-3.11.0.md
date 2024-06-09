# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: windows-x86
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 254 ms: 1.11x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.31 ms: 1.28x faster                                                           |
| docutils       | 2.10 sec                                                        | 2.01 sec: 1.04x faster                                                          |
| html5lib       | 54.3 ms                                                         | 50.9 ms: 1.07x faster                                                           |
| tornado_http   | 118 ms                                                          | 100 ms: 1.18x faster                                                            |
| Geometric mean | (ref)                                                           | 1.13x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 244 ms: 1.41x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 274 ms: 1.38x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 219 ms: 1.38x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 304 ms: 1.34x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 557 ms: 1.34x faster                                                            |
| async_tree_io              | 754 ms                                                          | 567 ms: 1.33x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 458 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 487 ms: 1.21x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.33x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 74.7 ms: 1.69x faster                                                           |
| float          | 76.1 ms                                                         | 53.1 ms: 1.43x faster                                                           |
| pidigits       | 203 ms                                                          | 201 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.35x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 125 ms: 1.18x faster                                                            |
| regex_dna      | 122 ms                                                          | 119 ms: 1.03x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.89 ms: 1.04x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.31 sec                                                        | 1.60 sec: 1.45x faster                                                          |
| json_dumps           | 9.80 ms                                                         | 7.13 ms: 1.37x faster                                                           |
| unpickle_pure_python | 231 us                                                          | 171 us: 1.35x faster                                                            |
| pickle_pure_python   | 309 us                                                          | 241 us: 1.28x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 44.3 ms: 1.24x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 64.6 ms: 1.17x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 61.5 ms: 1.16x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.90 us: 1.13x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 102 ms: 1.12x faster                                                            |
| pickle               | 7.99 us                                                         | 7.94 us: 1.01x faster                                                           |
| pickle_dict          | 20.1 us                                                         | 20.6 us: 1.02x slower                                                           |
| json_loads           | 20.0 us                                                         | 21.1 us: 1.05x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.65 us: 1.12x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.4 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.13x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.5 ms: 1.02x faster                                                           |
| python_startup         | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.00x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.12 ms: 1.44x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 48.8 ms: 1.25x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 21.8 ms: 1.23x faster                                                           |
| django_template | 37.4 ms                                                         | 33.7 ms: 1.11x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.25x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 149 us: 3.21x faster                                                            |
| generators                 | 52.2 ms                                                         | 23.8 ms: 2.19x faster                                                           |
| pylint                     | 418 ms                                                          | 242 ms: 1.73x faster                                                            |
| spectral_norm              | 122 ms                                                          | 71.7 ms: 1.70x faster                                                           |
| nbody                      | 126 ms                                                          | 74.7 ms: 1.69x faster                                                           |
| richards_super             | 58.7 ms                                                         | 35.4 ms: 1.66x faster                                                           |
| chaos                      | 84.4 ms                                                         | 51.5 ms: 1.64x faster                                                           |
| comprehensions             | 22.1 us                                                         | 13.6 us: 1.62x faster                                                           |
| logging_silent             | 119 ns                                                          | 73.8 ns: 1.62x faster                                                           |
| richards                   | 48.8 ms                                                         | 31.3 ms: 1.56x faster                                                           |
| raytrace                   | 327 ms                                                          | 211 ms: 1.55x faster                                                            |
| coroutines                 | 23.7 ms                                                         | 15.6 ms: 1.53x faster                                                           |
| nqueens                    | 111 ms                                                          | 73.1 ms: 1.52x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 1.00 ms: 1.49x faster                                                           |
| scimark_fft                | 291 ms                                                          | 201 ms: 1.45x faster                                                            |
| fannkuch                   | 399 ms                                                          | 275 ms: 1.45x faster                                                            |
| tomli_loads                | 2.31 sec                                                        | 1.60 sec: 1.45x faster                                                          |
| deltablue                  | 4.10 ms                                                         | 2.84 ms: 1.44x faster                                                           |
| mako                       | 10.3 ms                                                         | 7.12 ms: 1.44x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 27.8 us: 1.44x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.95 ms: 1.43x faster                                                           |
| float                      | 76.1 ms                                                         | 53.1 ms: 1.43x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 49.8 ms: 1.42x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.26 ms: 1.41x faster                                                           |
| async_tree_none            | 343 ms                                                          | 244 ms: 1.41x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 56.4 ms: 1.41x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.72 us: 1.40x faster                                                           |
| scimark_sor                | 135 ms                                                          | 97.1 ms: 1.39x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 274 ms: 1.38x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 219 ms: 1.38x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 7.13 ms: 1.37x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.38 us: 1.37x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 171 us: 1.35x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 304 ms: 1.34x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 557 ms: 1.34x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.27 sec: 1.34x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 5.65 ms: 1.33x faster                                                           |
| async_tree_io              | 754 ms                                                          | 567 ms: 1.33x faster                                                            |
| pprint_safe_repr           | 819 ms                                                          | 620 ms: 1.32x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 79.0 ms: 1.29x faster                                                           |
| go                         | 147 ms                                                          | 115 ms: 1.28x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 116 ms: 1.28x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 241 us: 1.28x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 6.31 ms: 1.28x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 619 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 458 ms: 1.26x faster                                                            |
| pyflate                    | 471 ms                                                          | 375 ms: 1.26x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 48.8 ms: 1.25x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 44.3 ms: 1.24x faster                                                           |
| deepcopy                   | 381 us                                                          | 309 us: 1.23x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 21.8 ms: 1.23x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 487 ms: 1.21x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 16.4 ms: 1.21x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 866 ms: 1.21x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.72 sec: 1.20x faster                                                          |
| sympy_str                  | 283 ms                                                          | 237 ms: 1.19x faster                                                            |
| deepcopy_reduce            | 3.32 us                                                         | 2.80 us: 1.18x faster                                                           |
| regex_compile              | 148 ms                                                          | 125 ms: 1.18x faster                                                            |
| tornado_http               | 118 ms                                                          | 100 ms: 1.18x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 44.1 ms: 1.17x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 64.6 ms: 1.17x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 61.5 ms: 1.16x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 78.7 ms: 1.15x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.90 us: 1.13x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.12x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 102 ms: 1.12x faster                                                            |
| 2to3                       | 282 ms                                                          | 254 ms: 1.11x faster                                                            |
| json                       | 4.78 ms                                                         | 4.30 ms: 1.11x faster                                                           |
| django_template            | 37.4 ms                                                         | 33.7 ms: 1.11x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.95 us: 1.10x faster                                                           |
| sympy_expand               | 462 ms                                                          | 422 ms: 1.10x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 50.9 ms: 1.07x faster                                                           |
| docutils                   | 2.10 sec                                                        | 2.01 sec: 1.04x faster                                                          |
| regex_dna                  | 122 ms                                                          | 119 ms: 1.03x faster                                                            |
| python_startup_no_site     | 18.8 ms                                                         | 18.5 ms: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                                          |
| pidigits                   | 203 ms                                                          | 201 ms: 1.01x faster                                                            |
| pickle                     | 7.99 us                                                         | 7.94 us: 1.01x faster                                                           |
| flaskblogging              | 2.03 sec                                                        | 2.03 sec: 1.00x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 71.5 ms: 1.01x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.6 us: 1.02x slower                                                           |
| python_startup             | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.89 ms: 1.04x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                           |
| json_loads                 | 20.0 us                                                         | 21.1 us: 1.05x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 84.3 ms: 1.05x slower                                                           |
| telco                      | 5.29 ms                                                         | 5.62 ms: 1.06x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.47 ms: 1.07x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.65 us: 1.12x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.4 us: 1.12x slower                                                           |
| async_generators           | 260 ms                                                          | 294 ms: 1.13x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 760 us: 1.23x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 232 ms: 2.05x slower                                                            |
| coverage                   | 58.0 ms                                                         | 333 ms: 5.74x slower                                                            |
| thrift                     | 801 us                                                          | 11.5 ms: 14.33x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.18x faster                                                                    |
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown
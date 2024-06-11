# Results vs. 3.11.0

- fork: python
- ref: e83ce850f433fd8bbf8f
- machine: windows-x86
- commit hash: e83ce85
- commit date: 2024-06-05
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 242 ms: 1.17x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.85 sec: 1.13x faster                                                         |
| html5lib       | 54.3 ms                                                         | 46.0 ms: 1.18x faster                                                          |
| tornado_http   | 118 ms                                                          | 96.4 ms: 1.23x faster                                                          |
| Geometric mean | (ref)                                                           | 1.18x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 230 ms: 1.49x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 207 ms: 1.46x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 280 ms: 1.46x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 261 ms: 1.45x faster                                                           |
| async_tree_io              | 754 ms                                                          | 534 ms: 1.41x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 537 ms: 1.39x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 484 ms: 1.19x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 504 ms: 1.17x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.37x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 52.9 ms: 2.38x faster                                                          |
| float          | 76.1 ms                                                         | 41.4 ms: 1.84x faster                                                          |
| pidigits       | 203 ms                                                          | 198 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                           | 1.65x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 96.7 ms: 1.52x faster                                                          |
| regex_dna      | 122 ms                                                          | 123 ms: 1.01x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                          |
| regex_effbot   | 1.82 ms                                                         | 1.98 ms: 1.08x slower                                                          |
| Geometric mean | (ref)                                                           | 1.07x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 135 us: 1.71x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.43 sec: 1.62x faster                                                         |
| pickle_pure_python   | 309 us                                                          | 199 us: 1.55x faster                                                           |
| json_dumps           | 9.80 ms                                                         | 6.51 ms: 1.51x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 40.4 ms: 1.36x faster                                                          |
| xml_etree_generate   | 71.6 ms                                                         | 55.2 ms: 1.30x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 61.2 ms: 1.23x faster                                                          |
| unpickle_list        | 3.28 us                                                         | 2.90 us: 1.13x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 102 ms: 1.12x faster                                                           |
| pickle               | 7.99 us                                                         | 8.23 us: 1.03x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| json_loads           | 20.0 us                                                         | 20.7 us: 1.03x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.5 us: 1.14x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.72 us: 1.14x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.20x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.2 ms: 1.07x slower                                                          |
| python_startup         | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.09x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.34 ms: 1.92x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 21.0 ms: 1.27x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 51.6 ms: 1.19x faster                                                          |
| django_template | 37.4 ms                                                         | 31.7 ms: 1.18x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.36x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-e83ce850f433fd8bbf8f-3.14.0a0-e83ce85 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 135 us: 3.53x faster                                                           |
| spectral_norm              | 122 ms                                                          | 47.6 ms: 2.55x faster                                                          |
| nbody                      | 126 ms                                                          | 52.9 ms: 2.38x faster                                                          |
| generators                 | 52.2 ms                                                         | 23.0 ms: 2.27x faster                                                          |
| logging_silent             | 119 ns                                                          | 53.9 ns: 2.21x faster                                                          |
| comprehensions             | 22.1 us                                                         | 11.0 us: 2.01x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 20.7 us: 1.94x faster                                                          |
| mako                       | 10.3 ms                                                         | 5.34 ms: 1.92x faster                                                          |
| float                      | 76.1 ms                                                         | 41.4 ms: 1.84x faster                                                          |
| fannkuch                   | 399 ms                                                          | 219 ms: 1.82x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.34 ms: 1.81x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 39.8 ms: 1.78x faster                                                          |
| pylint                     | 418 ms                                                          | 235 ms: 1.78x faster                                                           |
| scimark_fft                | 291 ms                                                          | 164 ms: 1.77x faster                                                           |
| pyflate                    | 471 ms                                                          | 271 ms: 1.74x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 135 us: 1.71x faster                                                           |
| chaos                      | 84.4 ms                                                         | 50.1 ms: 1.68x faster                                                          |
| richards_super             | 58.7 ms                                                         | 35.1 ms: 1.67x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 47.9 ms: 1.66x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 4.53 ms: 1.66x faster                                                          |
| sqlglot_parse              | 1.49 ms                                                         | 900 us: 1.66x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.43 sec: 1.62x faster                                                         |
| deltablue                  | 4.10 ms                                                         | 2.54 ms: 1.62x faster                                                          |
| raytrace                   | 327 ms                                                          | 205 ms: 1.59x faster                                                           |
| nqueens                    | 111 ms                                                          | 70.2 ms: 1.59x faster                                                          |
| richards                   | 48.8 ms                                                         | 31.3 ms: 1.56x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 199 us: 1.55x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.16 ms: 1.54x faster                                                          |
| regex_compile              | 148 ms                                                          | 96.7 ms: 1.52x faster                                                          |
| coroutines                 | 23.7 ms                                                         | 15.7 ms: 1.51x faster                                                          |
| json_dumps                 | 9.80 ms                                                         | 6.51 ms: 1.51x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 546 ms: 1.50x faster                                                           |
| scimark_sor                | 135 ms                                                          | 90.4 ms: 1.50x faster                                                          |
| pprint_pformat             | 1.70 sec                                                        | 1.13 sec: 1.49x faster                                                         |
| async_tree_none            | 343 ms                                                          | 230 ms: 1.49x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.27 us: 1.49x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 207 ms: 1.46x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 280 ms: 1.46x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 261 ms: 1.45x faster                                                           |
| logging_format             | 11.5 us                                                         | 7.92 us: 1.45x faster                                                          |
| scimark_lu                 | 102 ms                                                          | 71.1 ms: 1.44x faster                                                          |
| async_tree_io              | 754 ms                                                          | 534 ms: 1.41x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 106 ms: 1.40x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 537 ms: 1.39x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 40.4 ms: 1.36x faster                                                          |
| sympy_str                  | 283 ms                                                          | 208 ms: 1.36x faster                                                           |
| go                         | 147 ms                                                          | 109 ms: 1.34x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 600 ms: 1.31x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 798 ms: 1.31x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 55.2 ms: 1.30x faster                                                          |
| sympy_integrate            | 19.9 ms                                                         | 15.5 ms: 1.29x faster                                                          |
| genshi_text                | 26.8 ms                                                         | 21.0 ms: 1.27x faster                                                          |
| deepcopy                   | 381 us                                                          | 300 us: 1.27x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.63 sec: 1.27x faster                                                         |
| meteor_contest             | 90.9 ms                                                         | 72.3 ms: 1.26x faster                                                          |
| sqlglot_optimize           | 51.8 ms                                                         | 41.3 ms: 1.26x faster                                                          |
| sympy_expand               | 462 ms                                                          | 370 ms: 1.25x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 61.2 ms: 1.23x faster                                                          |
| tornado_http               | 118 ms                                                          | 96.4 ms: 1.23x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.74 us: 1.21x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 484 ms: 1.19x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 51.6 ms: 1.19x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 46.0 ms: 1.18x faster                                                          |
| django_template            | 37.4 ms                                                         | 31.7 ms: 1.18x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 504 ms: 1.17x faster                                                           |
| 2to3                       | 282 ms                                                          | 242 ms: 1.17x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 984 us: 1.16x faster                                                           |
| thrift                     | 801 us                                                          | 699 us: 1.15x faster                                                           |
| coverage                   | 58.0 ms                                                         | 50.6 ms: 1.15x faster                                                          |
| docutils                   | 2.10 sec                                                        | 1.85 sec: 1.13x faster                                                         |
| sqlite_synth               | 2.15 us                                                         | 1.90 us: 1.13x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 2.90 us: 1.13x faster                                                          |
| json                       | 4.78 ms                                                         | 4.24 ms: 1.13x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 102 ms: 1.12x faster                                                           |
| pidigits                   | 203 ms                                                          | 198 ms: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.01x faster                                                         |
| regex_dna                  | 122 ms                                                          | 123 ms: 1.01x slower                                                           |
| pickle                     | 7.99 us                                                         | 8.23 us: 1.03x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| pathlib                    | 79.9 ms                                                         | 82.4 ms: 1.03x slower                                                          |
| json_loads                 | 20.0 us                                                         | 20.7 us: 1.03x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.04x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 74.1 ms: 1.04x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                          |
| telco                      | 5.29 ms                                                         | 5.64 ms: 1.07x slower                                                          |
| python_startup_no_site     | 18.8 ms                                                         | 20.2 ms: 1.07x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.98 ms: 1.08x slower                                                          |
| python_startup             | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.5 us: 1.14x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.72 us: 1.14x slower                                                          |
| async_generators           | 260 ms                                                          | 305 ms: 1.17x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 757 us: 1.23x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 218 ms: 1.93x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.34x faster                                                                   |
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: unknown
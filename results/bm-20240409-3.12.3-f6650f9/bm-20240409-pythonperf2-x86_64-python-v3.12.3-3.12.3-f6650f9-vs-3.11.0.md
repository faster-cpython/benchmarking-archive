# Results vs. 3.11.0

- fork: python
- ref: v3.12.3
- machine: linux-x86_64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 279 ms: 1.03x faster                                         |
| chameleon      | 7.92 ms                                                      | 7.22 ms: 1.10x faster                                        |
| html5lib       | 72.2 ms                                                      | 69.7 ms: 1.04x faster                                        |
| tornado_http   | 124 ms                                                       | 120 ms: 1.04x faster                                         |
| Geometric mean | (ref)                                                        | 1.04x faster                                                 |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization     | 629 ms                                                       | 545 ms: 1.15x faster                                         |
| async_tree_none            | 518 ms                                                       | 451 ms: 1.15x faster                                         |
| async_tree_io              | 1.17 sec                                                     | 1.04 sec: 1.12x faster                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 538 ms: 1.11x faster                                         |
| async_tree_none_tg         | 474 ms                                                       | 428 ms: 1.11x faster                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 1.05 sec: 1.10x faster                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 693 ms: 1.09x faster                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 694 ms: 1.08x faster                                         |
| Geometric mean             | (ref)                                                        | 1.11x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 86.3 ms: 1.08x faster                                        |
| float          | 74.9 ms                                                      | 77.7 ms: 1.04x slower                                        |
| pidigits       | 251 ms                                                       | 264 ms: 1.05x slower                                         |
| Geometric mean | (ref)                                                        | 1.00x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 144 ms: 1.08x faster                                         |
| regex_v8       | 24.4 ms                                                      | 23.8 ms: 1.03x faster                                        |
| regex_effbot   | 3.34 ms                                                      | 3.45 ms: 1.03x slower                                        |
| regex_dna      | 227 ms                                                       | 237 ms: 1.04x slower                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.3 ms: 1.28x faster                                        |
| unpickle_pure_python | 238 us                                                       | 205 us: 1.16x faster                                         |
| pickle_dict          | 32.3 us                                                      | 30.6 us: 1.06x faster                                        |
| tomli_loads          | 2.25 sec                                                     | 2.17 sec: 1.04x faster                                       |
| xml_etree_parse      | 155 ms                                                       | 149 ms: 1.04x faster                                         |
| json_loads           | 28.9 us                                                      | 28.2 us: 1.03x faster                                        |
| xml_etree_iterparse  | 107 ms                                                       | 105 ms: 1.02x faster                                         |
| pickle_pure_python   | 316 us                                                       | 312 us: 1.01x faster                                         |
| pickle               | 9.89 us                                                      | 10.2 us: 1.03x slower                                        |
| unpickle_list        | 4.60 us                                                      | 4.78 us: 1.04x slower                                        |
| xml_etree_process    | 55.9 ms                                                      | 58.1 ms: 1.04x slower                                        |
| xml_etree_generate   | 79.7 ms                                                      | 86.8 ms: 1.09x slower                                        |
| unpickle             | 13.3 us                                                      | 14.7 us: 1.11x slower                                        |
| pickle_list          | 3.94 us                                                      | 4.41 us: 1.12x slower                                        |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 11.6 ms: 1.08x slower                                        |
| python_startup_no_site | 7.73 ms                                                      | 8.57 ms: 1.11x slower                                        |
| Geometric mean         | (ref)                                                        | 1.09x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.96 ms: 1.10x faster                                        |
| genshi_xml      | 57.1 ms                                                      | 53.0 ms: 1.08x faster                                        |
| django_template | 39.3 ms                                                      | 38.0 ms: 1.03x faster                                        |
| genshi_text     | 25.5 ms                                                      | 24.7 ms: 1.03x faster                                        |
| Geometric mean  | (ref)                                                        | 1.06x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 125 us: 4.27x faster                                         |
| asyncio_tcp                | 747 ms                                                       | 378 ms: 1.98x faster                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.56 sec: 1.96x faster                                       |
| comprehensions             | 25.1 us                                                      | 16.6 us: 1.51x faster                                        |
| generators                 | 54.6 ms                                                      | 36.9 ms: 1.48x faster                                        |
| pylint                     | 514 ms                                                       | 349 ms: 1.47x faster                                         |
| json_dumps                 | 13.3 ms                                                      | 10.3 ms: 1.28x faster                                        |
| richards_super             | 63.6 ms                                                      | 49.6 ms: 1.28x faster                                        |
| fannkuch                   | 416 ms                                                       | 333 ms: 1.25x faster                                         |
| deltablue                  | 3.97 ms                                                      | 3.23 ms: 1.23x faster                                        |
| sympy_sum                  | 186 ms                                                       | 152 ms: 1.22x faster                                         |
| coroutines                 | 27.8 ms                                                      | 22.9 ms: 1.21x faster                                        |
| chaos                      | 74.9 ms                                                      | 62.3 ms: 1.20x faster                                        |
| hexiom                     | 6.98 ms                                                      | 5.84 ms: 1.20x faster                                        |
| sympy_str                  | 337 ms                                                       | 287 ms: 1.17x faster                                         |
| nqueens                    | 103 ms                                                       | 87.7 ms: 1.17x faster                                        |
| unpickle_pure_python       | 238 us                                                       | 205 us: 1.16x faster                                         |
| async_tree_memoization     | 629 ms                                                       | 545 ms: 1.15x faster                                         |
| scimark_lu                 | 114 ms                                                       | 99.0 ms: 1.15x faster                                        |
| async_tree_none            | 518 ms                                                       | 451 ms: 1.15x faster                                         |
| sympy_expand               | 553 ms                                                       | 483 ms: 1.15x faster                                         |
| richards                   | 49.7 ms                                                      | 43.8 ms: 1.13x faster                                        |
| sympy_integrate            | 25.8 ms                                                      | 23.0 ms: 1.12x faster                                        |
| async_tree_io              | 1.17 sec                                                     | 1.04 sec: 1.12x faster                                       |
| gc_traversal               | 4.15 ms                                                      | 3.72 ms: 1.12x faster                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 538 ms: 1.11x faster                                         |
| async_tree_none_tg         | 474 ms                                                       | 428 ms: 1.11x faster                                         |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                       |
| mako                       | 11.0 ms                                                      | 9.96 ms: 1.10x faster                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 1.05 sec: 1.10x faster                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.38 ms: 1.10x faster                                        |
| chameleon                  | 7.92 ms                                                      | 7.22 ms: 1.10x faster                                        |
| logging_simple             | 7.24 us                                                      | 6.65 us: 1.09x faster                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 693 ms: 1.09x faster                                         |
| regex_compile              | 156 ms                                                       | 144 ms: 1.08x faster                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 694 ms: 1.08x faster                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.77 ms: 1.08x faster                                        |
| deepcopy                   | 391 us                                                       | 363 us: 1.08x faster                                         |
| logging_silent             | 100 ns                                                       | 93.1 ns: 1.08x faster                                        |
| go                         | 158 ms                                                       | 146 ms: 1.08x faster                                         |
| nbody                      | 92.9 ms                                                      | 86.3 ms: 1.08x faster                                        |
| genshi_xml                 | 57.1 ms                                                      | 53.0 ms: 1.08x faster                                        |
| sqlalchemy_imperative      | 19.8 ms                                                      | 18.5 ms: 1.07x faster                                        |
| bench_mp_pool              | 4.70 ms                                                      | 4.41 ms: 1.06x faster                                        |
| logging_format             | 7.71 us                                                      | 7.26 us: 1.06x faster                                        |
| pickle_dict                | 32.3 us                                                      | 30.6 us: 1.06x faster                                        |
| crypto_pyaes               | 83.3 ms                                                      | 79.1 ms: 1.05x faster                                        |
| sqlglot_normalize          | 122 ms                                                       | 116 ms: 1.05x faster                                         |
| deepcopy_memo              | 37.5 us                                                      | 35.6 us: 1.05x faster                                        |
| dask                       | 410 ms                                                       | 390 ms: 1.05x faster                                         |
| thrift                     | 931 us                                                       | 890 us: 1.05x faster                                         |
| bench_thread_pool          | 1.00 ms                                                      | 958 us: 1.04x faster                                         |
| tornado_http               | 124 ms                                                       | 120 ms: 1.04x faster                                         |
| pyflate                    | 449 ms                                                       | 432 ms: 1.04x faster                                         |
| dulwich_log                | 67.4 ms                                                      | 64.8 ms: 1.04x faster                                        |
| mypy2                      | 762 ms                                                       | 734 ms: 1.04x faster                                         |
| tomli_loads                | 2.25 sec                                                     | 2.17 sec: 1.04x faster                                       |
| xml_etree_parse            | 155 ms                                                       | 149 ms: 1.04x faster                                         |
| html5lib                   | 72.2 ms                                                      | 69.7 ms: 1.04x faster                                        |
| django_template            | 39.3 ms                                                      | 38.0 ms: 1.03x faster                                        |
| genshi_text                | 25.5 ms                                                      | 24.7 ms: 1.03x faster                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 67.8 ms: 1.03x faster                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.53 ms: 1.03x faster                                        |
| json_loads                 | 28.9 us                                                      | 28.2 us: 1.03x faster                                        |
| 2to3                       | 287 ms                                                       | 279 ms: 1.03x faster                                         |
| regex_v8                   | 24.4 ms                                                      | 23.8 ms: 1.03x faster                                        |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.03x faster                                       |
| meteor_contest             | 131 ms                                                       | 127 ms: 1.02x faster                                         |
| raytrace                   | 309 ms                                                       | 302 ms: 1.02x faster                                         |
| pprint_pformat             | 1.67 sec                                                     | 1.63 sec: 1.02x faster                                       |
| deepcopy_reduce            | 3.40 us                                                      | 3.32 us: 1.02x faster                                        |
| xml_etree_iterparse        | 107 ms                                                       | 105 ms: 1.02x faster                                         |
| sqlglot_optimize           | 59.0 ms                                                      | 58.0 ms: 1.02x faster                                        |
| scimark_sor                | 110 ms                                                       | 108 ms: 1.01x faster                                         |
| pickle_pure_python         | 316 us                                                       | 312 us: 1.01x faster                                         |
| pathlib                    | 18.9 ms                                                      | 18.7 ms: 1.01x faster                                        |
| pprint_safe_repr           | 805 ms                                                       | 797 ms: 1.01x faster                                         |
| spectral_norm              | 95.1 ms                                                      | 94.6 ms: 1.00x faster                                        |
| coverage                   | 66.1 ms                                                      | 66.5 ms: 1.01x slower                                        |
| telco                      | 6.81 ms                                                      | 6.95 ms: 1.02x slower                                        |
| pickle                     | 9.89 us                                                      | 10.2 us: 1.03x slower                                        |
| regex_effbot               | 3.34 ms                                                      | 3.45 ms: 1.03x slower                                        |
| sqlalchemy_declarative     | 154 ms                                                       | 160 ms: 1.03x slower                                         |
| aiohttp                    | 986 us                                                       | 1.02 ms: 1.04x slower                                        |
| float                      | 74.9 ms                                                      | 77.7 ms: 1.04x slower                                        |
| gunicorn                   | 966 us                                                       | 1.00 ms: 1.04x slower                                        |
| regex_dna                  | 227 ms                                                       | 237 ms: 1.04x slower                                         |
| unpickle_list              | 4.60 us                                                      | 4.78 us: 1.04x slower                                        |
| xml_etree_process          | 55.9 ms                                                      | 58.1 ms: 1.04x slower                                        |
| pidigits                   | 251 ms                                                       | 264 ms: 1.05x slower                                         |
| scimark_fft                | 281 ms                                                       | 297 ms: 1.06x slower                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.37 ms: 1.07x slower                                        |
| python_startup             | 10.7 ms                                                      | 11.6 ms: 1.08x slower                                        |
| sqlite_synth               | 2.52 us                                                      | 2.74 us: 1.09x slower                                        |
| xml_etree_generate         | 79.7 ms                                                      | 86.8 ms: 1.09x slower                                        |
| python_startup_no_site     | 7.73 ms                                                      | 8.57 ms: 1.11x slower                                        |
| unpickle                   | 13.3 us                                                      | 14.7 us: 1.11x slower                                        |
| pickle_list                | 3.94 us                                                      | 4.41 us: 1.12x slower                                        |
| async_generators           | 322 ms                                                       | 381 ms: 1.19x slower                                         |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                 |

Benchmark hidden because not significant (3): json, asyncio_websockets, docutils
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.02x
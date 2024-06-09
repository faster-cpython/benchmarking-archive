# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: linux-x86_64
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 345 ms: 1.20x slower                                                         |
| chameleon      | 7.92 ms                                                      | 8.61 ms: 1.09x slower                                                        |
| docutils       | 2.85 sec                                                     | 3.47 sec: 1.22x slower                                                       |
| html5lib       | 72.2 ms                                                      | 88.0 ms: 1.22x slower                                                        |
| tornado_http   | 124 ms                                                       | 129 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                        | 1.15x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization     | 629 ms                                                       | 475 ms: 1.32x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 454 ms: 1.32x faster                                                         |
| async_tree_none            | 518 ms                                                       | 398 ms: 1.30x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 366 ms: 1.30x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 943 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 613 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 654 ms: 1.15x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 254 ms: 1.01x slower                                                         |
| float          | 74.9 ms                                                      | 96.2 ms: 1.28x slower                                                        |
| nbody          | 92.9 ms                                                      | 125 ms: 1.34x slower                                                         |
| Geometric mean | (ref)                                                        | 1.20x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                        |
| regex_effbot   | 3.34 ms                                                      | 3.56 ms: 1.07x slower                                                        |
| regex_dna      | 227 ms                                                       | 255 ms: 1.12x slower                                                         |
| regex_compile  | 156 ms                                                       | 216 ms: 1.39x slower                                                         |
| Geometric mean | (ref)                                                        | 1.15x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                      | 24.4 us: 1.19x faster                                                        |
| json_dumps           | 13.3 ms                                                      | 11.3 ms: 1.17x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 145 ms: 1.07x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 31.3 us: 1.03x faster                                                        |
| unpickle_list        | 4.60 us                                                      | 4.73 us: 1.03x slower                                                        |
| xml_etree_iterparse  | 107 ms                                                       | 113 ms: 1.06x slower                                                         |
| pickle               | 9.89 us                                                      | 10.5 us: 1.06x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.0 us: 1.13x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.56 us: 1.16x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 97.0 ms: 1.22x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 68.8 ms: 1.23x slower                                                        |
| unpickle_pure_python | 238 us                                                       | 307 us: 1.29x slower                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.91 sec: 1.29x slower                                                       |
| pickle_pure_python   | 316 us                                                       | 434 us: 1.37x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.91 ms: 1.15x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 39.3 ms                                                      | 45.5 ms: 1.16x slower                                                        |
| genshi_xml      | 57.1 ms                                                      | 67.7 ms: 1.19x slower                                                        |
| genshi_text     | 25.5 ms                                                      | 33.0 ms: 1.30x slower                                                        |
| mako            | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 197 us: 2.70x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 388 ms: 1.92x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.92x faster                                                       |
| generators                 | 54.6 ms                                                      | 34.1 ms: 1.60x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 475 ms: 1.32x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 454 ms: 1.32x faster                                                         |
| pylint                     | 514 ms                                                       | 394 ms: 1.30x faster                                                         |
| async_tree_none            | 518 ms                                                       | 398 ms: 1.30x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 366 ms: 1.30x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 943 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 613 ms: 1.22x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.8 ms: 1.22x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.4 us: 1.19x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 11.3 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 654 ms: 1.15x faster                                                         |
| xml_etree_parse            | 155 ms                                                       | 145 ms: 1.07x faster                                                         |
| logging_simple             | 7.24 us                                                      | 6.82 us: 1.06x faster                                                        |
| logging_format             | 7.71 us                                                      | 7.39 us: 1.04x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 18.3 ms: 1.04x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 31.3 us: 1.03x faster                                                        |
| thrift                     | 931 us                                                       | 906 us: 1.03x faster                                                         |
| json                       | 5.58 ms                                                      | 5.48 ms: 1.02x faster                                                        |
| asyncio_websockets         | 390 ms                                                       | 386 ms: 1.01x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.77 sec: 1.00x faster                                                       |
| pidigits                   | 251 ms                                                       | 254 ms: 1.01x slower                                                         |
| sympy_sum                  | 186 ms                                                       | 189 ms: 1.02x slower                                                         |
| bench_thread_pool          | 1.00 ms                                                      | 1.02 ms: 1.02x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.73 us: 1.03x slower                                                        |
| tornado_http               | 124 ms                                                       | 129 ms: 1.04x slower                                                         |
| dask                       | 410 ms                                                       | 427 ms: 1.04x slower                                                         |
| bench_mp_pool              | 4.70 ms                                                      | 4.97 ms: 1.06x slower                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 113 ms: 1.06x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.5 us: 1.06x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.56 ms: 1.07x slower                                                        |
| richards_super             | 63.6 ms                                                      | 68.3 ms: 1.07x slower                                                        |
| chaos                      | 74.9 ms                                                      | 80.7 ms: 1.08x slower                                                        |
| chameleon                  | 7.92 ms                                                      | 8.61 ms: 1.09x slower                                                        |
| sympy_integrate            | 25.8 ms                                                      | 28.1 ms: 1.09x slower                                                        |
| raytrace                   | 309 ms                                                       | 338 ms: 1.09x slower                                                         |
| meteor_contest             | 131 ms                                                       | 143 ms: 1.10x slower                                                         |
| sympy_str                  | 337 ms                                                       | 371 ms: 1.10x slower                                                         |
| comprehensions             | 25.1 us                                                      | 27.6 us: 1.10x slower                                                        |
| pycparser                  | 1.31 sec                                                     | 1.45 sec: 1.11x slower                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 92.4 ms: 1.11x slower                                                        |
| regex_dna                  | 227 ms                                                       | 255 ms: 1.12x slower                                                         |
| unpickle                   | 13.3 us                                                      | 15.0 us: 1.13x slower                                                        |
| sympy_expand               | 553 ms                                                       | 628 ms: 1.14x slower                                                         |
| nqueens                    | 103 ms                                                       | 117 ms: 1.14x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.72 ms: 1.14x slower                                                        |
| deltablue                  | 3.97 ms                                                      | 4.54 ms: 1.14x slower                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 2.20 ms: 1.15x slower                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.74 ms: 1.15x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 8.91 ms: 1.15x slower                                                        |
| fannkuch                   | 416 ms                                                       | 479 ms: 1.15x slower                                                         |
| django_template            | 39.3 ms                                                      | 45.5 ms: 1.16x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 141 ms: 1.16x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.56 us: 1.16x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 78.3 ms: 1.16x slower                                                        |
| mypy2                      | 762 ms                                                       | 897 ms: 1.18x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.97 us: 1.18x slower                                                        |
| genshi_xml                 | 57.1 ms                                                      | 67.7 ms: 1.19x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 4.07 us: 1.20x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 70.7 ms: 1.20x slower                                                        |
| 2to3                       | 287 ms                                                       | 345 ms: 1.20x slower                                                         |
| gunicorn                   | 966 us                                                       | 1.16 ms: 1.21x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.19 ms: 1.21x slower                                                        |
| deepcopy                   | 391 us                                                       | 475 us: 1.22x slower                                                         |
| xml_etree_generate         | 79.7 ms                                                      | 97.0 ms: 1.22x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 88.0 ms: 1.22x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.47 sec: 1.22x slower                                                       |
| async_generators           | 322 ms                                                       | 395 ms: 1.23x slower                                                         |
| richards                   | 49.7 ms                                                      | 61.2 ms: 1.23x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 68.8 ms: 1.23x slower                                                        |
| coverage                   | 66.1 ms                                                      | 83.4 ms: 1.26x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 2.11 sec: 1.27x slower                                                       |
| scimark_lu                 | 114 ms                                                       | 145 ms: 1.27x slower                                                         |
| flaskblogging              | 3.88 ms                                                      | 4.96 ms: 1.28x slower                                                        |
| go                         | 158 ms                                                       | 202 ms: 1.28x slower                                                         |
| float                      | 74.9 ms                                                      | 96.2 ms: 1.28x slower                                                        |
| unpickle_pure_python       | 238 us                                                       | 307 us: 1.29x slower                                                         |
| pprint_safe_repr           | 805 ms                                                       | 1.04 sec: 1.29x slower                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.91 sec: 1.29x slower                                                       |
| genshi_text                | 25.5 ms                                                      | 33.0 ms: 1.30x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 2.06 ms: 1.31x slower                                                        |
| mako                       | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                        |
| nbody                      | 92.9 ms                                                      | 125 ms: 1.34x slower                                                         |
| pickle_pure_python         | 316 us                                                       | 434 us: 1.37x slower                                                         |
| telco                      | 6.81 ms                                                      | 9.41 ms: 1.38x slower                                                        |
| regex_compile              | 156 ms                                                       | 216 ms: 1.39x slower                                                         |
| pyflate                    | 449 ms                                                       | 637 ms: 1.42x slower                                                         |
| scimark_monte_carlo        | 69.8 ms                                                      | 99.7 ms: 1.43x slower                                                        |
| scimark_sor                | 110 ms                                                       | 163 ms: 1.48x slower                                                         |
| hexiom                     | 6.98 ms                                                      | 10.6 ms: 1.52x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 57.7 us: 1.54x slower                                                        |
| spectral_norm              | 95.1 ms                                                      | 147 ms: 1.54x slower                                                         |
| scimark_fft                | 281 ms                                                       | 433 ms: 1.54x slower                                                         |
| logging_silent             | 100 ns                                                       | 157 ns: 1.57x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.80 ms: 1.67x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.09x slower                                                                 |
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.05x
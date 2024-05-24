# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 0081bcd
- commit date: 2024-05-23
- overall geometric mean: 1.06x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf2-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 305 ms: 1.06x slower                                                      |
| chameleon      | 7.92 ms                                                      | 7.66 ms: 1.03x faster                                                     |
| html5lib       | 72.2 ms                                                      | 73.3 ms: 1.01x slower                                                     |
| tornado_http   | 124 ms                                                       | 123 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                        | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf2-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 431 ms: 1.39x faster                                                      |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                      |
| async_tree_none_tg         | 474 ms                                                       | 347 ms: 1.37x faster                                                      |
| async_tree_memoization     | 629 ms                                                       | 480 ms: 1.31x faster                                                      |
| async_tree_io              | 1.17 sec                                                     | 909 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                      |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 627 ms: 1.20x faster                                                      |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf2-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 84.1 ms: 1.10x faster                                                     |
| float          | 74.9 ms                                                      | 77.6 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                        | 1.02x faster                                                              |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf2-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 139 ms: 1.13x faster                                                      |
| regex_v8       | 24.4 ms                                                      | 25.5 ms: 1.05x slower                                                     |
| regex_dna      | 227 ms                                                       | 243 ms: 1.07x slower                                                      |
| regex_effbot   | 3.34 ms                                                      | 3.65 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                        | 1.02x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf2-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                     |
| json_loads           | 28.9 us                                                      | 24.6 us: 1.17x faster                                                     |
| unpickle_pure_python | 238 us                                                       | 213 us: 1.12x faster                                                      |
| tomli_loads          | 2.25 sec                                                     | 2.08 sec: 1.08x faster                                                    |
| xml_etree_iterparse  | 107 ms                                                       | 100 ms: 1.07x faster                                                      |
| xml_etree_parse      | 155 ms                                                       | 146 ms: 1.06x faster                                                      |
| pickle_pure_python   | 316 us                                                       | 311 us: 1.02x faster                                                      |
| unpickle_list        | 4.60 us                                                      | 4.66 us: 1.01x slower                                                     |
| xml_etree_generate   | 79.7 ms                                                      | 82.2 ms: 1.03x slower                                                     |
| xml_etree_process    | 55.9 ms                                                      | 59.2 ms: 1.06x slower                                                     |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                     |
| pickle_list          | 3.94 us                                                      | 4.40 us: 1.12x slower                                                     |
| unpickle             | 13.3 us                                                      | 14.9 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                              |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf2-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.45 ms: 1.22x slower                                                     |
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.24x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf2-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.10 ms: 1.21x faster                                                     |
| django_template | 39.3 ms                                                      | 41.2 ms: 1.05x slower                                                     |
| genshi_text     | 25.5 ms                                                      | 28.2 ms: 1.11x slower                                                     |
| genshi_xml      | 57.1 ms                                                      | 64.8 ms: 1.14x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf2-x86_64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 185 us: 2.88x faster                                                      |
| asyncio_tcp                | 747 ms                                                       | 377 ms: 1.98x faster                                                      |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                    |
| generators                 | 54.6 ms                                                      | 34.8 ms: 1.57x faster                                                     |
| comprehensions             | 25.1 us                                                      | 18.0 us: 1.39x faster                                                     |
| async_tree_memoization_tg  | 600 ms                                                       | 431 ms: 1.39x faster                                                      |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                      |
| async_tree_none_tg         | 474 ms                                                       | 347 ms: 1.37x faster                                                      |
| pylint                     | 514 ms                                                       | 381 ms: 1.35x faster                                                      |
| async_tree_memoization     | 629 ms                                                       | 480 ms: 1.31x faster                                                      |
| coroutines                 | 27.8 ms                                                      | 21.3 ms: 1.31x faster                                                     |
| async_tree_io              | 1.17 sec                                                     | 909 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                      |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                      |
| richards_super             | 63.6 ms                                                      | 50.9 ms: 1.25x faster                                                     |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                     |
| mako                       | 11.0 ms                                                      | 9.10 ms: 1.21x faster                                                     |
| fannkuch                   | 416 ms                                                       | 345 ms: 1.21x faster                                                      |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 627 ms: 1.20x faster                                                      |
| json_loads                 | 28.9 us                                                      | 24.6 us: 1.17x faster                                                     |
| crypto_pyaes               | 83.3 ms                                                      | 71.1 ms: 1.17x faster                                                     |
| spectral_norm              | 95.1 ms                                                      | 82.2 ms: 1.16x faster                                                     |
| pathlib                    | 18.9 ms                                                      | 16.4 ms: 1.15x faster                                                     |
| richards                   | 49.7 ms                                                      | 43.8 ms: 1.13x faster                                                     |
| chaos                      | 74.9 ms                                                      | 66.1 ms: 1.13x faster                                                     |
| regex_compile              | 156 ms                                                       | 139 ms: 1.13x faster                                                      |
| sympy_sum                  | 186 ms                                                       | 166 ms: 1.12x faster                                                      |
| unpickle_pure_python       | 238 us                                                       | 213 us: 1.12x faster                                                      |
| nbody                      | 92.9 ms                                                      | 84.1 ms: 1.10x faster                                                     |
| logging_simple             | 7.24 us                                                      | 6.58 us: 1.10x faster                                                     |
| mdp                        | 2.77 sec                                                     | 2.55 sec: 1.09x faster                                                    |
| tomli_loads                | 2.25 sec                                                     | 2.08 sec: 1.08x faster                                                    |
| sympy_str                  | 337 ms                                                       | 312 ms: 1.08x faster                                                      |
| raytrace                   | 309 ms                                                       | 288 ms: 1.08x faster                                                      |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                     |
| logging_format             | 7.71 us                                                      | 7.22 us: 1.07x faster                                                     |
| xml_etree_iterparse        | 107 ms                                                       | 100 ms: 1.07x faster                                                      |
| scimark_monte_carlo        | 69.8 ms                                                      | 65.6 ms: 1.07x faster                                                     |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                      |
| json                       | 5.58 ms                                                      | 5.28 ms: 1.06x faster                                                     |
| deltablue                  | 3.97 ms                                                      | 3.75 ms: 1.06x faster                                                     |
| bench_thread_pool          | 1.00 ms                                                      | 948 us: 1.05x faster                                                      |
| sqlglot_transpile          | 1.91 ms                                                      | 1.82 ms: 1.05x faster                                                     |
| nqueens                    | 103 ms                                                       | 97.8 ms: 1.05x faster                                                     |
| sympy_expand               | 553 ms                                                       | 528 ms: 1.05x faster                                                      |
| pycparser                  | 1.31 sec                                                     | 1.25 sec: 1.04x faster                                                    |
| hexiom                     | 6.98 ms                                                      | 6.74 ms: 1.03x faster                                                     |
| chameleon                  | 7.92 ms                                                      | 7.66 ms: 1.03x faster                                                     |
| pprint_pformat             | 1.67 sec                                                     | 1.63 sec: 1.02x faster                                                    |
| meteor_contest             | 131 ms                                                       | 128 ms: 1.02x faster                                                      |
| thrift                     | 931 us                                                       | 916 us: 1.02x faster                                                      |
| pickle_pure_python         | 316 us                                                       | 311 us: 1.02x faster                                                      |
| dulwich_log                | 67.4 ms                                                      | 66.5 ms: 1.01x faster                                                     |
| tornado_http               | 124 ms                                                       | 123 ms: 1.01x faster                                                      |
| sympy_integrate            | 25.8 ms                                                      | 25.6 ms: 1.01x faster                                                     |
| unpickle_list              | 4.60 us                                                      | 4.66 us: 1.01x slower                                                     |
| html5lib                   | 72.2 ms                                                      | 73.3 ms: 1.01x slower                                                     |
| go                         | 158 ms                                                       | 160 ms: 1.02x slower                                                      |
| logging_silent             | 100 ns                                                       | 103 ns: 1.02x slower                                                      |
| bench_mp_pool              | 4.70 ms                                                      | 4.82 ms: 1.03x slower                                                     |
| xml_etree_generate         | 79.7 ms                                                      | 82.2 ms: 1.03x slower                                                     |
| float                      | 74.9 ms                                                      | 77.6 ms: 1.04x slower                                                     |
| scimark_fft                | 281 ms                                                       | 291 ms: 1.04x slower                                                      |
| regex_v8                   | 24.4 ms                                                      | 25.5 ms: 1.05x slower                                                     |
| django_template            | 39.3 ms                                                      | 41.2 ms: 1.05x slower                                                     |
| deepcopy                   | 391 us                                                       | 411 us: 1.05x slower                                                      |
| xml_etree_process          | 55.9 ms                                                      | 59.2 ms: 1.06x slower                                                     |
| 2to3                       | 287 ms                                                       | 305 ms: 1.06x slower                                                      |
| pickle                     | 9.89 us                                                      | 10.6 us: 1.07x slower                                                     |
| regex_dna                  | 227 ms                                                       | 243 ms: 1.07x slower                                                      |
| sqlglot_normalize          | 122 ms                                                       | 131 ms: 1.08x slower                                                      |
| sqlglot_optimize           | 59.0 ms                                                      | 63.5 ms: 1.08x slower                                                     |
| regex_effbot               | 3.34 ms                                                      | 3.65 ms: 1.09x slower                                                     |
| deepcopy_reduce            | 3.40 us                                                      | 3.71 us: 1.09x slower                                                     |
| sqlite_synth               | 2.52 us                                                      | 2.76 us: 1.10x slower                                                     |
| genshi_text                | 25.5 ms                                                      | 28.2 ms: 1.11x slower                                                     |
| pickle_list                | 3.94 us                                                      | 4.40 us: 1.12x slower                                                     |
| unpickle                   | 13.3 us                                                      | 14.9 us: 1.13x slower                                                     |
| genshi_xml                 | 57.1 ms                                                      | 64.8 ms: 1.14x slower                                                     |
| async_generators           | 322 ms                                                       | 381 ms: 1.19x slower                                                      |
| scimark_sor                | 110 ms                                                       | 130 ms: 1.19x slower                                                      |
| gc_traversal               | 4.15 ms                                                      | 4.94 ms: 1.19x slower                                                     |
| telco                      | 6.81 ms                                                      | 8.14 ms: 1.20x slower                                                     |
| python_startup_no_site     | 7.73 ms                                                      | 9.45 ms: 1.22x slower                                                     |
| coverage                   | 66.1 ms                                                      | 82.6 ms: 1.25x slower                                                     |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                     |
| create_gc_cycles           | 1.58 ms                                                      | 1.99 ms: 1.26x slower                                                     |
| flaskblogging              | 3.88 ms                                                      | 4.91 ms: 1.26x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                              |

Benchmark hidden because not significant (9): dask, pyflate, deepcopy_memo, pprint_safe_repr, asyncio_websockets, pidigits, scimark_sparse_mat_mult, pickle_dict, scimark_lu
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, docutils, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x
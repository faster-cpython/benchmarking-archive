# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 7a3c89e
- commit date: 2024-04-04
- overall geometric mean: 1.05x faster
- HPT reliability: 79.34%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 300 ms: 1.05x slower                                                      |
| chameleon      | 7.92 ms                                                      | 7.26 ms: 1.09x faster                                                     |
| docutils       | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                                    |
| html5lib       | 72.2 ms                                                      | 73.6 ms: 1.02x slower                                                     |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                        | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 358 ms: 1.44x faster                                                      |
| async_tree_memoization     | 629 ms                                                       | 440 ms: 1.43x faster                                                      |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.40x faster                                                      |
| async_tree_memoization_tg  | 600 ms                                                       | 437 ms: 1.37x faster                                                      |
| async_tree_io              | 1.17 sec                                                     | 886 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 576 ms: 1.30x faster                                                      |
| async_tree_io_tg           | 1.15 sec                                                     | 910 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 595 ms: 1.27x faster                                                      |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 76.4 ms: 1.02x slower                                                     |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                      |
| nbody          | 92.9 ms                                                      | 97.8 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                        | 1.04x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 148 ms: 1.05x faster                                                      |
| regex_v8       | 24.4 ms                                                      | 25.5 ms: 1.04x slower                                                     |
| regex_dna      | 227 ms                                                       | 242 ms: 1.06x slower                                                      |
| regex_effbot   | 3.34 ms                                                      | 3.72 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                        | 1.04x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.8 ms: 1.22x faster                                                     |
| json_loads           | 28.9 us                                                      | 25.3 us: 1.14x faster                                                     |
| xml_etree_parse      | 155 ms                                                       | 143 ms: 1.08x faster                                                      |
| tomli_loads          | 2.25 sec                                                     | 2.16 sec: 1.04x faster                                                    |
| pickle_pure_python   | 316 us                                                       | 305 us: 1.04x faster                                                      |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.03x faster                                                      |
| unpickle_pure_python | 238 us                                                       | 233 us: 1.02x faster                                                      |
| unpickle_list        | 4.60 us                                                      | 4.63 us: 1.01x slower                                                     |
| pickle_dict          | 32.3 us                                                      | 32.9 us: 1.02x slower                                                     |
| xml_etree_process    | 55.9 ms                                                      | 59.0 ms: 1.06x slower                                                     |
| xml_etree_generate   | 79.7 ms                                                      | 84.9 ms: 1.06x slower                                                     |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                     |
| pickle_list          | 3.94 us                                                      | 4.41 us: 1.12x slower                                                     |
| unpickle             | 13.3 us                                                      | 15.1 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                     |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.96 ms: 1.11x faster                                                     |
| genshi_xml      | 57.1 ms                                                      | 57.5 ms: 1.01x slower                                                     |
| django_template | 39.3 ms                                                      | 39.9 ms: 1.01x slower                                                     |
| genshi_text     | 25.5 ms                                                      | 26.4 ms: 1.04x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 120 us: 4.44x faster                                                      |
| asyncio_tcp                | 747 ms                                                       | 372 ms: 2.01x faster                                                      |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                    |
| generators                 | 54.6 ms                                                      | 33.5 ms: 1.63x faster                                                     |
| async_tree_none            | 518 ms                                                       | 358 ms: 1.44x faster                                                      |
| async_tree_memoization     | 629 ms                                                       | 440 ms: 1.43x faster                                                      |
| pylint                     | 514 ms                                                       | 363 ms: 1.41x faster                                                      |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.40x faster                                                      |
| async_tree_memoization_tg  | 600 ms                                                       | 437 ms: 1.37x faster                                                      |
| async_tree_io              | 1.17 sec                                                     | 886 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 576 ms: 1.30x faster                                                      |
| comprehensions             | 25.1 us                                                      | 19.7 us: 1.27x faster                                                     |
| async_tree_io_tg           | 1.15 sec                                                     | 910 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 595 ms: 1.27x faster                                                      |
| coroutines                 | 27.8 ms                                                      | 22.4 ms: 1.24x faster                                                     |
| json_dumps                 | 13.3 ms                                                      | 10.8 ms: 1.22x faster                                                     |
| sympy_sum                  | 186 ms                                                       | 161 ms: 1.15x faster                                                      |
| json_loads                 | 28.9 us                                                      | 25.3 us: 1.14x faster                                                     |
| chaos                      | 74.9 ms                                                      | 66.6 ms: 1.13x faster                                                     |
| sympy_str                  | 337 ms                                                       | 301 ms: 1.12x faster                                                      |
| richards_super             | 63.6 ms                                                      | 57.1 ms: 1.11x faster                                                     |
| mako                       | 11.0 ms                                                      | 9.96 ms: 1.11x faster                                                     |
| sympy_expand               | 553 ms                                                       | 507 ms: 1.09x faster                                                      |
| chameleon                  | 7.92 ms                                                      | 7.26 ms: 1.09x faster                                                     |
| logging_simple             | 7.24 us                                                      | 6.64 us: 1.09x faster                                                     |
| xml_etree_parse            | 155 ms                                                       | 143 ms: 1.08x faster                                                      |
| fannkuch                   | 416 ms                                                       | 384 ms: 1.08x faster                                                      |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                                     |
| crypto_pyaes               | 83.3 ms                                                      | 77.4 ms: 1.08x faster                                                     |
| sqlglot_transpile          | 1.91 ms                                                      | 1.79 ms: 1.07x faster                                                     |
| deltablue                  | 3.97 ms                                                      | 3.72 ms: 1.07x faster                                                     |
| logging_format             | 7.71 us                                                      | 7.29 us: 1.06x faster                                                     |
| regex_compile              | 156 ms                                                       | 148 ms: 1.05x faster                                                      |
| pycparser                  | 1.31 sec                                                     | 1.25 sec: 1.05x faster                                                    |
| mdp                        | 2.77 sec                                                     | 2.65 sec: 1.05x faster                                                    |
| tomli_loads                | 2.25 sec                                                     | 2.16 sec: 1.04x faster                                                    |
| thrift                     | 931 us                                                       | 893 us: 1.04x faster                                                      |
| json                       | 5.58 ms                                                      | 5.37 ms: 1.04x faster                                                     |
| pickle_pure_python         | 316 us                                                       | 305 us: 1.04x faster                                                      |
| logging_silent             | 100 ns                                                       | 97.0 ns: 1.03x faster                                                     |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.03x faster                                                      |
| sympy_integrate            | 25.8 ms                                                      | 25.0 ms: 1.03x faster                                                     |
| unpickle_pure_python       | 238 us                                                       | 233 us: 1.02x faster                                                      |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                      |
| deepcopy                   | 391 us                                                       | 384 us: 1.02x faster                                                      |
| raytrace                   | 309 ms                                                       | 305 ms: 1.01x faster                                                      |
| dask                       | 410 ms                                                       | 406 ms: 1.01x faster                                                      |
| spectral_norm              | 95.1 ms                                                      | 94.3 ms: 1.01x faster                                                     |
| sqlglot_normalize          | 122 ms                                                       | 122 ms: 1.00x slower                                                      |
| unpickle_list              | 4.60 us                                                      | 4.63 us: 1.01x slower                                                     |
| genshi_xml                 | 57.1 ms                                                      | 57.5 ms: 1.01x slower                                                     |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.09 ms: 1.01x slower                                                     |
| richards                   | 49.7 ms                                                      | 50.2 ms: 1.01x slower                                                     |
| django_template            | 39.3 ms                                                      | 39.9 ms: 1.01x slower                                                     |
| deepcopy_reduce            | 3.40 us                                                      | 3.45 us: 1.01x slower                                                     |
| meteor_contest             | 131 ms                                                       | 132 ms: 1.01x slower                                                      |
| pickle_dict                | 32.3 us                                                      | 32.9 us: 1.02x slower                                                     |
| deepcopy_memo              | 37.5 us                                                      | 38.2 us: 1.02x slower                                                     |
| html5lib                   | 72.2 ms                                                      | 73.6 ms: 1.02x slower                                                     |
| float                      | 74.9 ms                                                      | 76.4 ms: 1.02x slower                                                     |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                     |
| pprint_pformat             | 1.67 sec                                                     | 1.71 sec: 1.03x slower                                                    |
| dulwich_log                | 67.4 ms                                                      | 69.7 ms: 1.03x slower                                                     |
| pprint_safe_repr           | 805 ms                                                       | 834 ms: 1.04x slower                                                      |
| genshi_text                | 25.5 ms                                                      | 26.4 ms: 1.04x slower                                                     |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                      |
| regex_v8                   | 24.4 ms                                                      | 25.5 ms: 1.04x slower                                                     |
| scimark_lu                 | 114 ms                                                       | 119 ms: 1.05x slower                                                      |
| gc_traversal               | 4.15 ms                                                      | 4.35 ms: 1.05x slower                                                     |
| 2to3                       | 287 ms                                                       | 300 ms: 1.05x slower                                                      |
| nbody                      | 92.9 ms                                                      | 97.8 ms: 1.05x slower                                                     |
| scimark_monte_carlo        | 69.8 ms                                                      | 73.7 ms: 1.06x slower                                                     |
| xml_etree_process          | 55.9 ms                                                      | 59.0 ms: 1.06x slower                                                     |
| sqlglot_optimize           | 59.0 ms                                                      | 62.8 ms: 1.06x slower                                                     |
| xml_etree_generate         | 79.7 ms                                                      | 84.9 ms: 1.06x slower                                                     |
| regex_dna                  | 227 ms                                                       | 242 ms: 1.06x slower                                                      |
| sqlite_synth               | 2.52 us                                                      | 2.70 us: 1.07x slower                                                     |
| docutils                   | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                                    |
| hexiom                     | 6.98 ms                                                      | 7.52 ms: 1.08x slower                                                     |
| mypy2                      | 762 ms                                                       | 824 ms: 1.08x slower                                                      |
| bench_mp_pool              | 4.70 ms                                                      | 5.14 ms: 1.09x slower                                                     |
| go                         | 158 ms                                                       | 173 ms: 1.10x slower                                                      |
| pyflate                    | 449 ms                                                       | 496 ms: 1.10x slower                                                      |
| pickle                     | 9.89 us                                                      | 10.9 us: 1.10x slower                                                     |
| regex_effbot               | 3.34 ms                                                      | 3.72 ms: 1.11x slower                                                     |
| scimark_fft                | 281 ms                                                       | 313 ms: 1.11x slower                                                      |
| pickle_list                | 3.94 us                                                      | 4.41 us: 1.12x slower                                                     |
| bench_thread_pool          | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                     |
| gunicorn                   | 966 us                                                       | 1.09 ms: 1.13x slower                                                     |
| unpickle                   | 13.3 us                                                      | 15.1 us: 1.14x slower                                                     |
| create_gc_cycles           | 1.58 ms                                                      | 1.79 ms: 1.14x slower                                                     |
| aiohttp                    | 986 us                                                       | 1.12 ms: 1.14x slower                                                     |
| async_generators           | 322 ms                                                       | 385 ms: 1.20x slower                                                      |
| telco                      | 6.81 ms                                                      | 8.22 ms: 1.21x slower                                                     |
| coverage                   | 66.1 ms                                                      | 80.6 ms: 1.22x slower                                                     |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                     |
| scimark_sor                | 110 ms                                                       | 153 ms: 1.39x slower                                                      |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                              |

Benchmark hidden because not significant (2): asyncio_websockets, nqueens
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 79.34% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
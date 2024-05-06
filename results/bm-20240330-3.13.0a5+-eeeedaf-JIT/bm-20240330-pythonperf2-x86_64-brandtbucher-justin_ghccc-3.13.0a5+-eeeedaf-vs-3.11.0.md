# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.05x faster
- HPT reliability: 92.33%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 300 ms: 1.05x slower                                                       |
| chameleon      | 7.92 ms                                                      | 7.36 ms: 1.08x faster                                                      |
| docutils       | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                                     |
| Geometric mean | (ref)                                                        | 1.01x slower                                                               |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 358 ms: 1.44x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 441 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 341 ms: 1.39x faster                                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 439 ms: 1.37x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 885 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 579 ms: 1.30x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 593 ms: 1.27x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 910 ms: 1.27x faster                                                       |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 75.4 ms: 1.01x slower                                                      |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 146 ms: 1.07x faster                                                       |
| regex_v8       | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                      |
| regex_dna      | 227 ms                                                       | 239 ms: 1.05x slower                                                       |
| regex_effbot   | 3.34 ms                                                      | 3.54 ms: 1.06x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                                      |
| json_loads           | 28.9 us                                                      | 25.5 us: 1.13x faster                                                      |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.07x faster                                                       |
| tomli_loads          | 2.25 sec                                                     | 2.10 sec: 1.07x faster                                                     |
| pickle_dict          | 32.3 us                                                      | 30.9 us: 1.05x faster                                                      |
| unpickle_pure_python | 238 us                                                       | 229 us: 1.04x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.03x faster                                                       |
| pickle_pure_python   | 316 us                                                       | 312 us: 1.01x faster                                                       |
| unpickle_list        | 4.60 us                                                      | 4.64 us: 1.01x slower                                                      |
| xml_etree_generate   | 79.7 ms                                                      | 83.3 ms: 1.05x slower                                                      |
| xml_etree_process    | 55.9 ms                                                      | 58.5 ms: 1.05x slower                                                      |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                      |
| pickle_list          | 3.94 us                                                      | 4.28 us: 1.09x slower                                                      |
| unpickle             | 13.3 us                                                      | 15.3 us: 1.15x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                      |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.29 ms: 1.18x faster                                                      |
| genshi_text     | 25.5 ms                                                      | 26.0 ms: 1.02x slower                                                      |
| django_template | 39.3 ms                                                      | 40.4 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.03x faster                                                               |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 120 us: 4.44x faster                                                       |
| asyncio_tcp                | 747 ms                                                       | 375 ms: 1.99x faster                                                       |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                     |
| generators                 | 54.6 ms                                                      | 33.1 ms: 1.65x faster                                                      |
| pylint                     | 514 ms                                                       | 337 ms: 1.53x faster                                                       |
| async_tree_none            | 518 ms                                                       | 358 ms: 1.44x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 441 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 341 ms: 1.39x faster                                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 439 ms: 1.37x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 885 ms: 1.32x faster                                                       |
| comprehensions             | 25.1 us                                                      | 19.0 us: 1.32x faster                                                      |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 579 ms: 1.30x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 593 ms: 1.27x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 910 ms: 1.27x faster                                                       |
| json_dumps                 | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                                      |
| coroutines                 | 27.8 ms                                                      | 22.6 ms: 1.23x faster                                                      |
| chaos                      | 74.9 ms                                                      | 62.8 ms: 1.19x faster                                                      |
| fannkuch                   | 416 ms                                                       | 349 ms: 1.19x faster                                                       |
| mako                       | 11.0 ms                                                      | 9.29 ms: 1.18x faster                                                      |
| spectral_norm              | 95.1 ms                                                      | 81.9 ms: 1.16x faster                                                      |
| sympy_sum                  | 186 ms                                                       | 161 ms: 1.15x faster                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 72.5 ms: 1.15x faster                                                      |
| json_loads                 | 28.9 us                                                      | 25.5 us: 1.13x faster                                                      |
| richards_super             | 63.6 ms                                                      | 56.7 ms: 1.12x faster                                                      |
| sympy_str                  | 337 ms                                                       | 303 ms: 1.11x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                                      |
| logging_simple             | 7.24 us                                                      | 6.72 us: 1.08x faster                                                      |
| sympy_expand               | 553 ms                                                       | 513 ms: 1.08x faster                                                       |
| chameleon                  | 7.92 ms                                                      | 7.36 ms: 1.08x faster                                                      |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.07x faster                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.10 sec: 1.07x faster                                                     |
| deltablue                  | 3.97 ms                                                      | 3.71 ms: 1.07x faster                                                      |
| regex_compile              | 156 ms                                                       | 146 ms: 1.07x faster                                                       |
| mdp                        | 2.77 sec                                                     | 2.60 sec: 1.07x faster                                                     |
| sqlglot_transpile          | 1.91 ms                                                      | 1.81 ms: 1.06x faster                                                      |
| pickle_dict                | 32.3 us                                                      | 30.9 us: 1.05x faster                                                      |
| logging_format             | 7.71 us                                                      | 7.38 us: 1.04x faster                                                      |
| scimark_monte_carlo        | 69.8 ms                                                      | 66.9 ms: 1.04x faster                                                      |
| unpickle_pure_python       | 238 us                                                       | 229 us: 1.04x faster                                                       |
| thrift                     | 931 us                                                       | 897 us: 1.04x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.03x faster                                                     |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.03x faster                                                       |
| sympy_integrate            | 25.8 ms                                                      | 25.2 ms: 1.02x faster                                                      |
| raytrace                   | 309 ms                                                       | 303 ms: 1.02x faster                                                       |
| json                       | 5.58 ms                                                      | 5.48 ms: 1.02x faster                                                      |
| logging_silent             | 100 ns                                                       | 98.6 ns: 1.02x faster                                                      |
| deepcopy_reduce            | 3.40 us                                                      | 3.34 us: 1.02x faster                                                      |
| dask                       | 410 ms                                                       | 404 ms: 1.02x faster                                                       |
| pickle_pure_python         | 316 us                                                       | 312 us: 1.01x faster                                                       |
| pprint_pformat             | 1.67 sec                                                     | 1.65 sec: 1.01x faster                                                     |
| deepcopy                   | 391 us                                                       | 389 us: 1.01x faster                                                       |
| float                      | 74.9 ms                                                      | 75.4 ms: 1.01x slower                                                      |
| scimark_lu                 | 114 ms                                                       | 115 ms: 1.01x slower                                                       |
| pprint_safe_repr           | 805 ms                                                       | 811 ms: 1.01x slower                                                       |
| pyflate                    | 449 ms                                                       | 454 ms: 1.01x slower                                                       |
| unpickle_list              | 4.60 us                                                      | 4.64 us: 1.01x slower                                                      |
| meteor_contest             | 131 ms                                                       | 133 ms: 1.02x slower                                                       |
| hexiom                     | 6.98 ms                                                      | 7.09 ms: 1.02x slower                                                      |
| richards                   | 49.7 ms                                                      | 50.5 ms: 1.02x slower                                                      |
| genshi_text                | 25.5 ms                                                      | 26.0 ms: 1.02x slower                                                      |
| dulwich_log                | 67.4 ms                                                      | 68.9 ms: 1.02x slower                                                      |
| sqlglot_normalize          | 122 ms                                                       | 125 ms: 1.02x slower                                                       |
| deepcopy_memo              | 37.5 us                                                      | 38.5 us: 1.03x slower                                                      |
| django_template            | 39.3 ms                                                      | 40.4 ms: 1.03x slower                                                      |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.19 ms: 1.03x slower                                                      |
| scimark_fft                | 281 ms                                                       | 290 ms: 1.03x slower                                                       |
| pathlib                    | 18.9 ms                                                      | 19.7 ms: 1.04x slower                                                      |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                       |
| regex_v8                   | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                      |
| 2to3                       | 287 ms                                                       | 300 ms: 1.05x slower                                                       |
| xml_etree_generate         | 79.7 ms                                                      | 83.3 ms: 1.05x slower                                                      |
| xml_etree_process          | 55.9 ms                                                      | 58.5 ms: 1.05x slower                                                      |
| regex_dna                  | 227 ms                                                       | 239 ms: 1.05x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.54 ms: 1.06x slower                                                      |
| sqlite_synth               | 2.52 us                                                      | 2.68 us: 1.06x slower                                                      |
| pickle                     | 9.89 us                                                      | 10.6 us: 1.07x slower                                                      |
| docutils                   | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                                     |
| sqlglot_optimize           | 59.0 ms                                                      | 63.6 ms: 1.08x slower                                                      |
| bench_mp_pool              | 4.70 ms                                                      | 5.07 ms: 1.08x slower                                                      |
| pickle_list                | 3.94 us                                                      | 4.28 us: 1.09x slower                                                      |
| mypy2                      | 762 ms                                                       | 832 ms: 1.09x slower                                                       |
| go                         | 158 ms                                                       | 175 ms: 1.11x slower                                                       |
| bench_thread_pool          | 1.00 ms                                                      | 1.11 ms: 1.11x slower                                                      |
| gunicorn                   | 966 us                                                       | 1.09 ms: 1.13x slower                                                      |
| aiohttp                    | 986 us                                                       | 1.12 ms: 1.14x slower                                                      |
| create_gc_cycles           | 1.58 ms                                                      | 1.82 ms: 1.15x slower                                                      |
| unpickle                   | 13.3 us                                                      | 15.3 us: 1.15x slower                                                      |
| gc_traversal               | 4.15 ms                                                      | 4.81 ms: 1.16x slower                                                      |
| telco                      | 6.81 ms                                                      | 8.04 ms: 1.18x slower                                                      |
| coverage                   | 66.1 ms                                                      | 79.7 ms: 1.21x slower                                                      |
| async_generators           | 322 ms                                                       | 395 ms: 1.23x slower                                                       |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                      |
| scimark_sor                | 110 ms                                                       | 148 ms: 1.35x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                      |
| unpack_sequence            | 45.7 ns                                                      | 89.5 ns: 1.96x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                               |

Benchmark hidden because not significant (6): tornado_http, nqueens, nbody, genshi_xml, asyncio_websockets, html5lib
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 92.33% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
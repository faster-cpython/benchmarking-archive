# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.04x faster
- HPT reliability: 69.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 299 ms: 1.04x slower                                                       |
| chameleon      | 7.92 ms                                                      | 7.12 ms: 1.11x faster                                                      |
| docutils       | 2.85 sec                                                     | 3.06 sec: 1.08x slower                                                     |
| Geometric mean | (ref)                                                        | 1.00x slower                                                               |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 358 ms: 1.45x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 441 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 337 ms: 1.41x faster                                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 882 ms: 1.33x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 576 ms: 1.30x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 594 ms: 1.27x faster                                                       |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                       |
| float          | 74.9 ms                                                      | 78.0 ms: 1.04x slower                                                      |
| nbody          | 92.9 ms                                                      | 97.3 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                        | 1.04x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 147 ms: 1.06x faster                                                       |
| regex_effbot   | 3.34 ms                                                      | 3.46 ms: 1.04x slower                                                      |
| regex_dna      | 227 ms                                                       | 238 ms: 1.05x slower                                                       |
| regex_v8       | 24.4 ms                                                      | 26.2 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                      |
| json_loads           | 28.9 us                                                      | 25.3 us: 1.14x faster                                                      |
| xml_etree_parse      | 155 ms                                                       | 143 ms: 1.08x faster                                                       |
| tomli_loads          | 2.25 sec                                                     | 2.14 sec: 1.05x faster                                                     |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.04x faster                                                       |
| unpickle_pure_python | 238 us                                                       | 235 us: 1.01x faster                                                       |
| xml_etree_process    | 55.9 ms                                                      | 58.1 ms: 1.04x slower                                                      |
| pickle_dict          | 32.3 us                                                      | 33.6 us: 1.04x slower                                                      |
| xml_etree_generate   | 79.7 ms                                                      | 83.4 ms: 1.05x slower                                                      |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                      |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.11x slower                                                      |
| pickle_list          | 3.94 us                                                      | 4.50 us: 1.14x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                               |

Benchmark hidden because not significant (2): pickle_pure_python, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.25x slower                                                      |
| python_startup_no_site | 7.73 ms                                                      | 11.7 ms: 1.52x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 9.91 ms: 1.11x faster                                                      |
| genshi_xml     | 57.1 ms                                                      | 57.9 ms: 1.01x slower                                                      |
| genshi_text    | 25.5 ms                                                      | 26.6 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                        | 1.01x faster                                                               |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 117 us: 4.54x faster                                                       |
| asyncio_tcp                | 747 ms                                                       | 368 ms: 2.03x faster                                                       |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                                     |
| generators                 | 54.6 ms                                                      | 34.3 ms: 1.59x faster                                                      |
| pylint                     | 514 ms                                                       | 337 ms: 1.52x faster                                                       |
| async_tree_none            | 518 ms                                                       | 358 ms: 1.45x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 441 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 337 ms: 1.41x faster                                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 882 ms: 1.33x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 576 ms: 1.30x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 594 ms: 1.27x faster                                                       |
| comprehensions             | 25.1 us                                                      | 19.9 us: 1.26x faster                                                      |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                      |
| coroutines                 | 27.8 ms                                                      | 23.7 ms: 1.17x faster                                                      |
| sympy_sum                  | 186 ms                                                       | 162 ms: 1.15x faster                                                       |
| json_loads                 | 28.9 us                                                      | 25.3 us: 1.14x faster                                                      |
| chaos                      | 74.9 ms                                                      | 66.8 ms: 1.12x faster                                                      |
| sympy_str                  | 337 ms                                                       | 301 ms: 1.12x faster                                                       |
| chameleon                  | 7.92 ms                                                      | 7.12 ms: 1.11x faster                                                      |
| mako                       | 11.0 ms                                                      | 9.91 ms: 1.11x faster                                                      |
| richards_super             | 63.6 ms                                                      | 57.8 ms: 1.10x faster                                                      |
| fannkuch                   | 416 ms                                                       | 378 ms: 1.10x faster                                                       |
| logging_simple             | 7.24 us                                                      | 6.60 us: 1.10x faster                                                      |
| xml_etree_parse            | 155 ms                                                       | 143 ms: 1.08x faster                                                       |
| sympy_expand               | 553 ms                                                       | 512 ms: 1.08x faster                                                       |
| logging_format             | 7.71 us                                                      | 7.19 us: 1.07x faster                                                      |
| deltablue                  | 3.97 ms                                                      | 3.71 ms: 1.07x faster                                                      |
| thrift                     | 931 us                                                       | 873 us: 1.07x faster                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 78.2 ms: 1.06x faster                                                      |
| regex_compile              | 156 ms                                                       | 147 ms: 1.06x faster                                                       |
| mdp                        | 2.77 sec                                                     | 2.62 sec: 1.06x faster                                                     |
| sqlglot_parse              | 1.51 ms                                                      | 1.44 ms: 1.05x faster                                                      |
| tomli_loads                | 2.25 sec                                                     | 2.14 sec: 1.05x faster                                                     |
| sqlglot_transpile          | 1.91 ms                                                      | 1.83 ms: 1.04x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.04x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.04x faster                                                     |
| json                       | 5.58 ms                                                      | 5.39 ms: 1.04x faster                                                      |
| deepcopy                   | 391 us                                                       | 379 us: 1.03x faster                                                       |
| sympy_integrate            | 25.8 ms                                                      | 25.1 ms: 1.03x faster                                                      |
| spectral_norm              | 95.1 ms                                                      | 93.5 ms: 1.02x faster                                                      |
| logging_silent             | 100 ns                                                       | 98.8 ns: 1.02x faster                                                      |
| dask                       | 410 ms                                                       | 404 ms: 1.01x faster                                                       |
| unpickle_pure_python       | 238 us                                                       | 235 us: 1.01x faster                                                       |
| sqlglot_normalize          | 122 ms                                                       | 122 ms: 1.00x slower                                                       |
| meteor_contest             | 131 ms                                                       | 132 ms: 1.01x slower                                                       |
| pathlib                    | 18.9 ms                                                      | 19.1 ms: 1.01x slower                                                      |
| genshi_xml                 | 57.1 ms                                                      | 57.9 ms: 1.01x slower                                                      |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.14 ms: 1.02x slower                                                      |
| dulwich_log                | 67.4 ms                                                      | 68.9 ms: 1.02x slower                                                      |
| richards                   | 49.7 ms                                                      | 50.9 ms: 1.02x slower                                                      |
| nqueens                    | 103 ms                                                       | 105 ms: 1.03x slower                                                       |
| pprint_safe_repr           | 805 ms                                                       | 831 ms: 1.03x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.46 ms: 1.04x slower                                                      |
| pprint_pformat             | 1.67 sec                                                     | 1.73 sec: 1.04x slower                                                     |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                       |
| xml_etree_process          | 55.9 ms                                                      | 58.1 ms: 1.04x slower                                                      |
| float                      | 74.9 ms                                                      | 78.0 ms: 1.04x slower                                                      |
| pickle_dict                | 32.3 us                                                      | 33.6 us: 1.04x slower                                                      |
| 2to3                       | 287 ms                                                       | 299 ms: 1.04x slower                                                       |
| genshi_text                | 25.5 ms                                                      | 26.6 ms: 1.05x slower                                                      |
| xml_etree_generate         | 79.7 ms                                                      | 83.4 ms: 1.05x slower                                                      |
| regex_dna                  | 227 ms                                                       | 238 ms: 1.05x slower                                                       |
| nbody                      | 92.9 ms                                                      | 97.3 ms: 1.05x slower                                                      |
| sqlite_synth               | 2.52 us                                                      | 2.67 us: 1.06x slower                                                      |
| sqlglot_optimize           | 59.0 ms                                                      | 62.8 ms: 1.07x slower                                                      |
| scimark_monte_carlo        | 69.8 ms                                                      | 74.6 ms: 1.07x slower                                                      |
| scimark_lu                 | 114 ms                                                       | 122 ms: 1.07x slower                                                       |
| regex_v8                   | 24.4 ms                                                      | 26.2 ms: 1.07x slower                                                      |
| bench_mp_pool              | 4.70 ms                                                      | 5.05 ms: 1.07x slower                                                      |
| docutils                   | 2.85 sec                                                     | 3.06 sec: 1.08x slower                                                     |
| hexiom                     | 6.98 ms                                                      | 7.53 ms: 1.08x slower                                                      |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.08x slower                                                      |
| mypy2                      | 762 ms                                                       | 828 ms: 1.09x slower                                                       |
| gc_traversal               | 4.15 ms                                                      | 4.55 ms: 1.10x slower                                                      |
| go                         | 158 ms                                                       | 173 ms: 1.10x slower                                                       |
| pyflate                    | 449 ms                                                       | 496 ms: 1.10x slower                                                       |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.11x slower                                                      |
| gunicorn                   | 966 us                                                       | 1.08 ms: 1.12x slower                                                      |
| bench_thread_pool          | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                      |
| create_gc_cycles           | 1.58 ms                                                      | 1.79 ms: 1.14x slower                                                      |
| pickle_list                | 3.94 us                                                      | 4.50 us: 1.14x slower                                                      |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.15x slower                                                      |
| scimark_fft                | 281 ms                                                       | 322 ms: 1.15x slower                                                       |
| telco                      | 6.81 ms                                                      | 8.14 ms: 1.20x slower                                                      |
| async_generators           | 322 ms                                                       | 392 ms: 1.22x slower                                                       |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.25x slower                                                      |
| unpack_sequence            | 45.7 ns                                                      | 59.2 ns: 1.30x slower                                                      |
| coverage                   | 66.1 ms                                                      | 86.2 ms: 1.30x slower                                                      |
| scimark_sor                | 110 ms                                                       | 153 ms: 1.39x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 11.7 ms: 1.52x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                               |

Benchmark hidden because not significant (9): deepcopy_reduce, django_template, deepcopy_memo, pickle_pure_python, raytrace, unpickle_list, tornado_http, asyncio_websockets, html5lib
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 69.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x
# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.02x faster
- HPT reliability: 61.01%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 303 ms: 1.06x slower                                                       |
| chameleon      | 7.92 ms                                                      | 7.52 ms: 1.05x faster                                                      |
| docutils       | 2.85 sec                                                     | 3.11 sec: 1.09x slower                                                     |
| html5lib       | 72.2 ms                                                      | 74.2 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 362 ms: 1.43x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 446 ms: 1.41x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 343 ms: 1.38x faster                                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 443 ms: 1.35x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 891 ms: 1.31x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 584 ms: 1.28x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 912 ms: 1.27x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 600 ms: 1.25x faster                                                       |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                                       |
| float          | 74.9 ms                                                      | 78.6 ms: 1.05x slower                                                      |
| nbody          | 92.9 ms                                                      | 103 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                        | 1.07x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 151 ms: 1.03x faster                                                       |
| regex_v8       | 24.4 ms                                                      | 25.8 ms: 1.05x slower                                                      |
| regex_dna      | 227 ms                                                       | 245 ms: 1.08x slower                                                       |
| regex_effbot   | 3.34 ms                                                      | 3.69 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                        | 1.05x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                      |
| json_loads           | 28.9 us                                                      | 25.6 us: 1.13x faster                                                      |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.07x faster                                                       |
| pickle_dict          | 32.3 us                                                      | 30.7 us: 1.05x faster                                                      |
| pickle_pure_python   | 316 us                                                       | 313 us: 1.01x faster                                                       |
| unpickle_list        | 4.60 us                                                      | 4.56 us: 1.01x faster                                                      |
| unpickle_pure_python | 238 us                                                       | 244 us: 1.02x slower                                                       |
| tomli_loads          | 2.25 sec                                                     | 2.36 sec: 1.05x slower                                                     |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                                      |
| xml_etree_process    | 55.9 ms                                                      | 58.9 ms: 1.05x slower                                                      |
| xml_etree_generate   | 79.7 ms                                                      | 86.0 ms: 1.08x slower                                                      |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.11x slower                                                      |
| pickle_list          | 3.94 us                                                      | 4.49 us: 1.14x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                               |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                      |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.2 ms: 1.07x faster                                                      |
| django_template | 39.3 ms                                                      | 39.7 ms: 1.01x slower                                                      |
| genshi_xml      | 57.1 ms                                                      | 58.6 ms: 1.03x slower                                                      |
| genshi_text     | 25.5 ms                                                      | 26.6 ms: 1.04x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 119 us: 4.46x faster                                                       |
| asyncio_tcp                | 747 ms                                                       | 372 ms: 2.01x faster                                                       |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                     |
| generators                 | 54.6 ms                                                      | 33.1 ms: 1.65x faster                                                      |
| pylint                     | 514 ms                                                       | 340 ms: 1.51x faster                                                       |
| async_tree_none            | 518 ms                                                       | 362 ms: 1.43x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 446 ms: 1.41x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 343 ms: 1.38x faster                                                       |
| async_tree_memoization_tg  | 600 ms                                                       | 443 ms: 1.35x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 891 ms: 1.31x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 584 ms: 1.28x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 912 ms: 1.27x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 600 ms: 1.25x faster                                                       |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                      |
| coroutines                 | 27.8 ms                                                      | 22.5 ms: 1.24x faster                                                      |
| comprehensions             | 25.1 us                                                      | 20.4 us: 1.23x faster                                                      |
| sympy_sum                  | 186 ms                                                       | 162 ms: 1.14x faster                                                       |
| json_loads                 | 28.9 us                                                      | 25.6 us: 1.13x faster                                                      |
| sympy_str                  | 337 ms                                                       | 302 ms: 1.12x faster                                                       |
| sympy_expand               | 553 ms                                                       | 505 ms: 1.09x faster                                                       |
| thrift                     | 931 us                                                       | 861 us: 1.08x faster                                                       |
| logging_simple             | 7.24 us                                                      | 6.73 us: 1.08x faster                                                      |
| mako                       | 11.0 ms                                                      | 10.2 ms: 1.07x faster                                                      |
| chaos                      | 74.9 ms                                                      | 69.8 ms: 1.07x faster                                                      |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.07x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                      |
| richards_super             | 63.6 ms                                                      | 60.2 ms: 1.06x faster                                                      |
| chameleon                  | 7.92 ms                                                      | 7.52 ms: 1.05x faster                                                      |
| pickle_dict                | 32.3 us                                                      | 30.7 us: 1.05x faster                                                      |
| sqlglot_transpile          | 1.91 ms                                                      | 1.83 ms: 1.05x faster                                                      |
| deltablue                  | 3.97 ms                                                      | 3.80 ms: 1.05x faster                                                      |
| logging_format             | 7.71 us                                                      | 7.38 us: 1.04x faster                                                      |
| mdp                        | 2.77 sec                                                     | 2.65 sec: 1.04x faster                                                     |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.04x faster                                                     |
| regex_compile              | 156 ms                                                       | 151 ms: 1.03x faster                                                       |
| json                       | 5.58 ms                                                      | 5.40 ms: 1.03x faster                                                      |
| crypto_pyaes               | 83.3 ms                                                      | 81.1 ms: 1.03x faster                                                      |
| fannkuch                   | 416 ms                                                       | 408 ms: 1.02x faster                                                       |
| sympy_integrate            | 25.8 ms                                                      | 25.4 ms: 1.02x faster                                                      |
| logging_silent             | 100 ns                                                       | 99.0 ns: 1.01x faster                                                      |
| raytrace                   | 309 ms                                                       | 306 ms: 1.01x faster                                                       |
| pickle_pure_python         | 316 us                                                       | 313 us: 1.01x faster                                                       |
| dask                       | 410 ms                                                       | 406 ms: 1.01x faster                                                       |
| unpickle_list              | 4.60 us                                                      | 4.56 us: 1.01x faster                                                      |
| sqlglot_normalize          | 122 ms                                                       | 121 ms: 1.01x faster                                                       |
| deepcopy                   | 391 us                                                       | 395 us: 1.01x slower                                                       |
| django_template            | 39.3 ms                                                      | 39.7 ms: 1.01x slower                                                      |
| pathlib                    | 18.9 ms                                                      | 19.2 ms: 1.01x slower                                                      |
| unpickle_pure_python       | 238 us                                                       | 244 us: 1.02x slower                                                       |
| genshi_xml                 | 57.1 ms                                                      | 58.6 ms: 1.03x slower                                                      |
| deepcopy_memo              | 37.5 us                                                      | 38.5 us: 1.03x slower                                                      |
| html5lib                   | 72.2 ms                                                      | 74.2 ms: 1.03x slower                                                      |
| meteor_contest             | 131 ms                                                       | 134 ms: 1.03x slower                                                       |
| dulwich_log                | 67.4 ms                                                      | 69.4 ms: 1.03x slower                                                      |
| spectral_norm              | 95.1 ms                                                      | 99.0 ms: 1.04x slower                                                      |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                                       |
| genshi_text                | 25.5 ms                                                      | 26.6 ms: 1.04x slower                                                      |
| float                      | 74.9 ms                                                      | 78.6 ms: 1.05x slower                                                      |
| tomli_loads                | 2.25 sec                                                     | 2.36 sec: 1.05x slower                                                     |
| gc_traversal               | 4.15 ms                                                      | 4.36 ms: 1.05x slower                                                      |
| pickle                     | 9.89 us                                                      | 10.4 us: 1.05x slower                                                      |
| xml_etree_process          | 55.9 ms                                                      | 58.9 ms: 1.05x slower                                                      |
| regex_v8                   | 24.4 ms                                                      | 25.8 ms: 1.05x slower                                                      |
| bench_mp_pool              | 4.70 ms                                                      | 4.96 ms: 1.05x slower                                                      |
| 2to3                       | 287 ms                                                       | 303 ms: 1.06x slower                                                       |
| nqueens                    | 103 ms                                                       | 109 ms: 1.06x slower                                                       |
| sqlglot_optimize           | 59.0 ms                                                      | 62.9 ms: 1.07x slower                                                      |
| regex_dna                  | 227 ms                                                       | 245 ms: 1.08x slower                                                       |
| pprint_pformat             | 1.67 sec                                                     | 1.79 sec: 1.08x slower                                                     |
| xml_etree_generate         | 79.7 ms                                                      | 86.0 ms: 1.08x slower                                                      |
| richards                   | 49.7 ms                                                      | 53.7 ms: 1.08x slower                                                      |
| sqlite_synth               | 2.52 us                                                      | 2.74 us: 1.09x slower                                                      |
| mypy2                      | 762 ms                                                       | 831 ms: 1.09x slower                                                       |
| docutils                   | 2.85 sec                                                     | 3.11 sec: 1.09x slower                                                     |
| regex_effbot               | 3.34 ms                                                      | 3.69 ms: 1.10x slower                                                      |
| nbody                      | 92.9 ms                                                      | 103 ms: 1.11x slower                                                       |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.50 ms: 1.11x slower                                                      |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.11x slower                                                      |
| scimark_monte_carlo        | 69.8 ms                                                      | 77.9 ms: 1.12x slower                                                      |
| bench_thread_pool          | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                      |
| pprint_safe_repr           | 805 ms                                                       | 902 ms: 1.12x slower                                                       |
| gunicorn                   | 966 us                                                       | 1.09 ms: 1.13x slower                                                      |
| scimark_lu                 | 114 ms                                                       | 130 ms: 1.14x slower                                                       |
| pickle_list                | 3.94 us                                                      | 4.49 us: 1.14x slower                                                      |
| create_gc_cycles           | 1.58 ms                                                      | 1.80 ms: 1.14x slower                                                      |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.14x slower                                                      |
| hexiom                     | 6.98 ms                                                      | 8.00 ms: 1.15x slower                                                      |
| go                         | 158 ms                                                       | 182 ms: 1.15x slower                                                       |
| pyflate                    | 449 ms                                                       | 522 ms: 1.16x slower                                                       |
| telco                      | 6.81 ms                                                      | 8.10 ms: 1.19x slower                                                      |
| async_generators           | 322 ms                                                       | 389 ms: 1.21x slower                                                       |
| scimark_fft                | 281 ms                                                       | 341 ms: 1.21x slower                                                       |
| coverage                   | 66.1 ms                                                      | 80.3 ms: 1.21x slower                                                      |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                      |
| scimark_sor                | 110 ms                                                       | 160 ms: 1.46x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                      |
| unpack_sequence            | 45.7 ns                                                      | 107 ns: 2.33x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                               |

Benchmark hidden because not significant (4): xml_etree_iterparse, deepcopy_reduce, tornado_http, asyncio_websockets
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 61.01% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x
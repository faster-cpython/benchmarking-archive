# Results vs. 3.11.0

- fork: brandtbucher
- ref: no_cold_exits
- machine: linux-x86_64
- commit hash: f837cc6
- commit date: 2024-06-10
- overall geometric mean: 1.07x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf2-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 304 ms: 1.06x slower                                                       |
| docutils       | 2.85 sec                                                     | 3.09 sec: 1.09x slower                                                     |
| html5lib       | 72.2 ms                                                      | 73.3 ms: 1.02x slower                                                      |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                        | 1.03x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf2-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                       |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 347 ms: 1.37x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 476 ms: 1.32x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 886 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 581 ms: 1.29x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 914 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 620 ms: 1.22x faster                                                       |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf2-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 84.1 ms: 1.10x faster                                                      |
| pidigits       | 251 ms                                                       | 250 ms: 1.00x faster                                                       |
| float          | 74.9 ms                                                      | 75.5 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                        | 1.03x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf2-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 136 ms: 1.15x faster                                                       |
| regex_effbot   | 3.34 ms                                                      | 3.49 ms: 1.04x slower                                                      |
| regex_dna      | 227 ms                                                       | 239 ms: 1.05x slower                                                       |
| regex_v8       | 24.4 ms                                                      | 26.5 ms: 1.09x slower                                                      |
| Geometric mean | (ref)                                                        | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf2-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.23x faster                                                      |
| json_loads           | 28.9 us                                                      | 25.0 us: 1.16x faster                                                      |
| unpickle_pure_python | 238 us                                                       | 217 us: 1.10x faster                                                       |
| xml_etree_parse      | 155 ms                                                       | 143 ms: 1.08x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 99.0 ms: 1.08x faster                                                      |
| tomli_loads          | 2.25 sec                                                     | 2.10 sec: 1.07x faster                                                     |
| pickle_dict          | 32.3 us                                                      | 31.1 us: 1.04x faster                                                      |
| pickle_pure_python   | 316 us                                                       | 315 us: 1.00x faster                                                       |
| xml_etree_generate   | 79.7 ms                                                      | 81.8 ms: 1.03x slower                                                      |
| xml_etree_process    | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                      |
| pickle               | 9.89 us                                                      | 10.5 us: 1.06x slower                                                      |
| unpickle_list        | 4.60 us                                                      | 4.93 us: 1.07x slower                                                      |
| pickle_list          | 3.94 us                                                      | 4.48 us: 1.14x slower                                                      |
| unpickle             | 13.3 us                                                      | 16.0 us: 1.20x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf2-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.86 ms: 1.15x slower                                                      |
| python_startup         | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf2-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.15 ms: 1.20x faster                                                      |
| django_template | 39.3 ms                                                      | 41.0 ms: 1.04x slower                                                      |
| genshi_text     | 25.5 ms                                                      | 28.1 ms: 1.10x slower                                                      |
| genshi_xml      | 57.1 ms                                                      | 64.9 ms: 1.14x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf2-x86_64-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 187 us: 2.85x faster                                                       |
| asyncio_tcp                | 747 ms                                                       | 381 ms: 1.96x faster                                                       |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                     |
| generators                 | 54.6 ms                                                      | 34.8 ms: 1.57x faster                                                      |
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                       |
| comprehensions             | 25.1 us                                                      | 18.1 us: 1.39x faster                                                      |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 347 ms: 1.37x faster                                                       |
| pylint                     | 514 ms                                                       | 377 ms: 1.36x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 476 ms: 1.32x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 886 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 581 ms: 1.29x faster                                                       |
| coroutines                 | 27.8 ms                                                      | 21.9 ms: 1.27x faster                                                      |
| async_tree_io_tg           | 1.15 sec                                                     | 914 ms: 1.26x faster                                                       |
| richards_super             | 63.6 ms                                                      | 51.3 ms: 1.24x faster                                                      |
| fannkuch                   | 416 ms                                                       | 336 ms: 1.24x faster                                                       |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.23x faster                                                      |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 620 ms: 1.22x faster                                                       |
| mako                       | 11.0 ms                                                      | 9.15 ms: 1.20x faster                                                      |
| crypto_pyaes               | 83.3 ms                                                      | 70.5 ms: 1.18x faster                                                      |
| pathlib                    | 18.9 ms                                                      | 16.2 ms: 1.17x faster                                                      |
| json_loads                 | 28.9 us                                                      | 25.0 us: 1.16x faster                                                      |
| regex_compile              | 156 ms                                                       | 136 ms: 1.15x faster                                                       |
| richards                   | 49.7 ms                                                      | 43.2 ms: 1.15x faster                                                      |
| spectral_norm              | 95.1 ms                                                      | 83.0 ms: 1.14x faster                                                      |
| chaos                      | 74.9 ms                                                      | 65.7 ms: 1.14x faster                                                      |
| logging_simple             | 7.24 us                                                      | 6.39 us: 1.13x faster                                                      |
| sympy_sum                  | 186 ms                                                       | 164 ms: 1.13x faster                                                       |
| nbody                      | 92.9 ms                                                      | 84.1 ms: 1.10x faster                                                      |
| unpickle_pure_python       | 238 us                                                       | 217 us: 1.10x faster                                                       |
| logging_format             | 7.71 us                                                      | 7.02 us: 1.10x faster                                                      |
| sympy_str                  | 337 ms                                                       | 310 ms: 1.09x faster                                                       |
| mdp                        | 2.77 sec                                                     | 2.56 sec: 1.08x faster                                                     |
| raytrace                   | 309 ms                                                       | 286 ms: 1.08x faster                                                       |
| nqueens                    | 103 ms                                                       | 94.9 ms: 1.08x faster                                                      |
| xml_etree_parse            | 155 ms                                                       | 143 ms: 1.08x faster                                                       |
| xml_etree_iterparse        | 107 ms                                                       | 99.0 ms: 1.08x faster                                                      |
| tomli_loads                | 2.25 sec                                                     | 2.10 sec: 1.07x faster                                                     |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                      |
| deltablue                  | 3.97 ms                                                      | 3.74 ms: 1.06x faster                                                      |
| sympy_expand               | 553 ms                                                       | 525 ms: 1.05x faster                                                       |
| sqlglot_transpile          | 1.91 ms                                                      | 1.82 ms: 1.05x faster                                                      |
| json                       | 5.58 ms                                                      | 5.34 ms: 1.05x faster                                                      |
| hexiom                     | 6.98 ms                                                      | 6.68 ms: 1.04x faster                                                      |
| pickle_dict                | 32.3 us                                                      | 31.1 us: 1.04x faster                                                      |
| scimark_monte_carlo        | 69.8 ms                                                      | 67.3 ms: 1.04x faster                                                      |
| bench_thread_pool          | 1.00 ms                                                      | 965 us: 1.04x faster                                                       |
| pprint_pformat             | 1.67 sec                                                     | 1.61 sec: 1.03x faster                                                     |
| dulwich_log                | 67.4 ms                                                      | 65.4 ms: 1.03x faster                                                      |
| deepcopy_memo              | 37.5 us                                                      | 36.5 us: 1.03x faster                                                      |
| thrift                     | 931 us                                                       | 910 us: 1.02x faster                                                       |
| pprint_safe_repr           | 805 ms                                                       | 787 ms: 1.02x faster                                                       |
| dask                       | 410 ms                                                       | 401 ms: 1.02x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.02x faster                                                     |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                       |
| meteor_contest             | 131 ms                                                       | 128 ms: 1.02x faster                                                       |
| sympy_integrate            | 25.8 ms                                                      | 25.4 ms: 1.02x faster                                                      |
| pidigits                   | 251 ms                                                       | 250 ms: 1.00x faster                                                       |
| pickle_pure_python         | 316 us                                                       | 315 us: 1.00x faster                                                       |
| float                      | 74.9 ms                                                      | 75.5 ms: 1.01x slower                                                      |
| pyflate                    | 449 ms                                                       | 453 ms: 1.01x slower                                                       |
| html5lib                   | 72.2 ms                                                      | 73.3 ms: 1.02x slower                                                      |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.13 ms: 1.02x slower                                                      |
| logging_silent             | 100 ns                                                       | 102 ns: 1.02x slower                                                       |
| go                         | 158 ms                                                       | 161 ms: 1.02x slower                                                       |
| scimark_lu                 | 114 ms                                                       | 117 ms: 1.02x slower                                                       |
| xml_etree_generate         | 79.7 ms                                                      | 81.8 ms: 1.03x slower                                                      |
| deepcopy                   | 391 us                                                       | 408 us: 1.04x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.49 ms: 1.04x slower                                                      |
| scimark_fft                | 281 ms                                                       | 293 ms: 1.04x slower                                                       |
| django_template            | 39.3 ms                                                      | 41.0 ms: 1.04x slower                                                      |
| xml_etree_process          | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                      |
| regex_dna                  | 227 ms                                                       | 239 ms: 1.05x slower                                                       |
| 2to3                       | 287 ms                                                       | 304 ms: 1.06x slower                                                       |
| pickle                     | 9.89 us                                                      | 10.5 us: 1.06x slower                                                      |
| sqlglot_normalize          | 122 ms                                                       | 130 ms: 1.07x slower                                                       |
| unpickle_list              | 4.60 us                                                      | 4.93 us: 1.07x slower                                                      |
| deepcopy_reduce            | 3.40 us                                                      | 3.64 us: 1.07x slower                                                      |
| regex_v8                   | 24.4 ms                                                      | 26.5 ms: 1.09x slower                                                      |
| docutils                   | 2.85 sec                                                     | 3.09 sec: 1.09x slower                                                     |
| sqlglot_optimize           | 59.0 ms                                                      | 64.0 ms: 1.09x slower                                                      |
| sqlite_synth               | 2.52 us                                                      | 2.77 us: 1.10x slower                                                      |
| genshi_text                | 25.5 ms                                                      | 28.1 ms: 1.10x slower                                                      |
| genshi_xml                 | 57.1 ms                                                      | 64.9 ms: 1.14x slower                                                      |
| pickle_list                | 3.94 us                                                      | 4.48 us: 1.14x slower                                                      |
| python_startup_no_site     | 7.73 ms                                                      | 8.86 ms: 1.15x slower                                                      |
| gc_traversal               | 4.15 ms                                                      | 4.88 ms: 1.18x slower                                                      |
| unpickle                   | 13.3 us                                                      | 16.0 us: 1.20x slower                                                      |
| coverage                   | 66.1 ms                                                      | 79.6 ms: 1.20x slower                                                      |
| telco                      | 6.81 ms                                                      | 8.23 ms: 1.21x slower                                                      |
| async_generators           | 322 ms                                                       | 391 ms: 1.21x slower                                                       |
| python_startup             | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                      |
| scimark_sor                | 110 ms                                                       | 137 ms: 1.25x slower                                                       |
| create_gc_cycles           | 1.58 ms                                                      | 1.97 ms: 1.25x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                               |

Benchmark hidden because not significant (2): asyncio_websockets, bench_mp_pool
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x
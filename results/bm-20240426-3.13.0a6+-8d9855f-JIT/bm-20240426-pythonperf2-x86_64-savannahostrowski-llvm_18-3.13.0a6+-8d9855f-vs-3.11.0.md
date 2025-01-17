# Results vs. 3.11.0

- fork: savannahostrowski
- ref: llvm_18
- machine: linux-x86_64
- commit hash: 8d9855f
- commit date: 2024-04-26
- overall geometric mean: 1.05x faster
- HPT reliability: 92.42%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 302 ms: 1.05x slower                                                       |
| chameleon      | 7.92 ms                                                      | 7.46 ms: 1.06x faster                                                      |
| docutils       | 2.85 sec                                                     | 3.09 sec: 1.08x slower                                                     |
| html5lib       | 72.2 ms                                                      | 74.6 ms: 1.03x slower                                                      |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                        | 1.02x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 418 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.40x faster                                                       |
| async_tree_none            | 518 ms                                                       | 371 ms: 1.40x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 464 ms: 1.36x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 852 ms: 1.36x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 883 ms: 1.33x faster                                                       |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 589 ms: 1.27x faster                                                       |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 614 ms: 1.23x faster                                                       |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 76.0 ms: 1.01x slower                                                      |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                       |
| nbody          | 92.9 ms                                                      | 98.9 ms: 1.06x slower                                                      |
| Geometric mean | (ref)                                                        | 1.04x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 143 ms: 1.09x faster                                                       |
| regex_dna      | 227 ms                                                       | 238 ms: 1.04x slower                                                       |
| regex_effbot   | 3.34 ms                                                      | 3.51 ms: 1.05x slower                                                      |
| regex_v8       | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                      |
| json_loads           | 28.9 us                                                      | 24.6 us: 1.18x faster                                                      |
| unpickle_pure_python | 238 us                                                       | 214 us: 1.11x faster                                                       |
| xml_etree_parse      | 155 ms                                                       | 142 ms: 1.09x faster                                                       |
| tomli_loads          | 2.25 sec                                                     | 2.09 sec: 1.08x faster                                                     |
| xml_etree_iterparse  | 107 ms                                                       | 100 ms: 1.07x faster                                                       |
| pickle_dict          | 32.3 us                                                      | 30.5 us: 1.06x faster                                                      |
| unpickle_list        | 4.60 us                                                      | 4.73 us: 1.03x slower                                                      |
| xml_etree_process    | 55.9 ms                                                      | 57.6 ms: 1.03x slower                                                      |
| xml_etree_generate   | 79.7 ms                                                      | 83.0 ms: 1.04x slower                                                      |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                      |
| pickle_list          | 3.94 us                                                      | 4.50 us: 1.14x slower                                                      |
| unpickle             | 13.3 us                                                      | 15.6 us: 1.18x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                               |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.43 ms: 1.22x slower                                                      |
| python_startup         | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.24x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.65 ms: 1.14x faster                                                      |
| django_template | 39.3 ms                                                      | 40.4 ms: 1.03x slower                                                      |
| genshi_xml      | 57.1 ms                                                      | 62.3 ms: 1.09x slower                                                      |
| genshi_text     | 25.5 ms                                                      | 29.1 ms: 1.14x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 185 us: 2.88x faster                                                       |
| asyncio_tcp                | 747 ms                                                       | 374 ms: 2.00x faster                                                       |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                                     |
| generators                 | 54.6 ms                                                      | 34.4 ms: 1.59x faster                                                      |
| async_tree_memoization_tg  | 600 ms                                                       | 418 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.40x faster                                                       |
| async_tree_none            | 518 ms                                                       | 371 ms: 1.40x faster                                                       |
| pylint                     | 514 ms                                                       | 370 ms: 1.39x faster                                                       |
| async_tree_memoization     | 629 ms                                                       | 464 ms: 1.36x faster                                                       |
| async_tree_io_tg           | 1.15 sec                                                     | 852 ms: 1.36x faster                                                       |
| async_tree_io              | 1.17 sec                                                     | 883 ms: 1.33x faster                                                       |
| comprehensions             | 25.1 us                                                      | 19.3 us: 1.30x faster                                                      |
| coroutines                 | 27.8 ms                                                      | 21.6 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 589 ms: 1.27x faster                                                       |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                      |
| richards_super             | 63.6 ms                                                      | 51.2 ms: 1.24x faster                                                      |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 614 ms: 1.23x faster                                                       |
| json_loads                 | 28.9 us                                                      | 24.6 us: 1.18x faster                                                      |
| chaos                      | 74.9 ms                                                      | 65.7 ms: 1.14x faster                                                      |
| mako                       | 11.0 ms                                                      | 9.65 ms: 1.14x faster                                                      |
| sympy_sum                  | 186 ms                                                       | 165 ms: 1.13x faster                                                       |
| unpickle_pure_python       | 238 us                                                       | 214 us: 1.11x faster                                                       |
| logging_simple             | 7.24 us                                                      | 6.52 us: 1.11x faster                                                      |
| fannkuch                   | 416 ms                                                       | 376 ms: 1.11x faster                                                       |
| raytrace                   | 309 ms                                                       | 281 ms: 1.10x faster                                                       |
| sympy_str                  | 337 ms                                                       | 308 ms: 1.09x faster                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 76.3 ms: 1.09x faster                                                      |
| xml_etree_parse            | 155 ms                                                       | 142 ms: 1.09x faster                                                       |
| regex_compile              | 156 ms                                                       | 143 ms: 1.09x faster                                                       |
| richards                   | 49.7 ms                                                      | 45.8 ms: 1.08x faster                                                      |
| pathlib                    | 18.9 ms                                                      | 17.6 ms: 1.08x faster                                                      |
| mdp                        | 2.77 sec                                                     | 2.57 sec: 1.08x faster                                                     |
| sympy_expand               | 553 ms                                                       | 513 ms: 1.08x faster                                                       |
| logging_format             | 7.71 us                                                      | 7.15 us: 1.08x faster                                                      |
| tomli_loads                | 2.25 sec                                                     | 2.09 sec: 1.08x faster                                                     |
| xml_etree_iterparse        | 107 ms                                                       | 100 ms: 1.07x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                      |
| bench_thread_pool          | 1.00 ms                                                      | 941 us: 1.06x faster                                                       |
| chameleon                  | 7.92 ms                                                      | 7.46 ms: 1.06x faster                                                      |
| thrift                     | 931 us                                                       | 877 us: 1.06x faster                                                       |
| pickle_dict                | 32.3 us                                                      | 30.5 us: 1.06x faster                                                      |
| logging_silent             | 100 ns                                                       | 95.4 ns: 1.05x faster                                                      |
| json                       | 5.58 ms                                                      | 5.31 ms: 1.05x faster                                                      |
| sqlglot_transpile          | 1.91 ms                                                      | 1.82 ms: 1.05x faster                                                      |
| spectral_norm              | 95.1 ms                                                      | 90.9 ms: 1.05x faster                                                      |
| deltablue                  | 3.97 ms                                                      | 3.80 ms: 1.04x faster                                                      |
| nqueens                    | 103 ms                                                       | 100 ms: 1.03x faster                                                       |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                       |
| dask                       | 410 ms                                                       | 402 ms: 1.02x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.29 sec: 1.01x faster                                                     |
| scimark_monte_carlo        | 69.8 ms                                                      | 69.1 ms: 1.01x faster                                                      |
| sympy_integrate            | 25.8 ms                                                      | 25.6 ms: 1.01x faster                                                      |
| deepcopy                   | 391 us                                                       | 393 us: 1.01x slower                                                       |
| hexiom                     | 6.98 ms                                                      | 7.02 ms: 1.01x slower                                                      |
| pprint_pformat             | 1.67 sec                                                     | 1.68 sec: 1.01x slower                                                     |
| sqlglot_normalize          | 122 ms                                                       | 123 ms: 1.01x slower                                                       |
| deepcopy_reduce            | 3.40 us                                                      | 3.44 us: 1.01x slower                                                      |
| float                      | 74.9 ms                                                      | 76.0 ms: 1.01x slower                                                      |
| django_template            | 39.3 ms                                                      | 40.4 ms: 1.03x slower                                                      |
| unpickle_list              | 4.60 us                                                      | 4.73 us: 1.03x slower                                                      |
| xml_etree_process          | 55.9 ms                                                      | 57.6 ms: 1.03x slower                                                      |
| html5lib                   | 72.2 ms                                                      | 74.6 ms: 1.03x slower                                                      |
| meteor_contest             | 131 ms                                                       | 135 ms: 1.04x slower                                                       |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                       |
| xml_etree_generate         | 79.7 ms                                                      | 83.0 ms: 1.04x slower                                                      |
| pprint_safe_repr           | 805 ms                                                       | 839 ms: 1.04x slower                                                       |
| pickle                     | 9.89 us                                                      | 10.3 us: 1.04x slower                                                      |
| regex_dna                  | 227 ms                                                       | 238 ms: 1.04x slower                                                       |
| scimark_lu                 | 114 ms                                                       | 119 ms: 1.05x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.51 ms: 1.05x slower                                                      |
| 2to3                       | 287 ms                                                       | 302 ms: 1.05x slower                                                       |
| nbody                      | 92.9 ms                                                      | 98.9 ms: 1.06x slower                                                      |
| gc_traversal               | 4.15 ms                                                      | 4.43 ms: 1.07x slower                                                      |
| sqlglot_optimize           | 59.0 ms                                                      | 63.1 ms: 1.07x slower                                                      |
| regex_v8                   | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                                      |
| sqlite_synth               | 2.52 us                                                      | 2.71 us: 1.07x slower                                                      |
| docutils                   | 2.85 sec                                                     | 3.09 sec: 1.08x slower                                                     |
| genshi_xml                 | 57.1 ms                                                      | 62.3 ms: 1.09x slower                                                      |
| go                         | 158 ms                                                       | 173 ms: 1.10x slower                                                       |
| pyflate                    | 449 ms                                                       | 494 ms: 1.10x slower                                                       |
| mypy2                      | 762 ms                                                       | 843 ms: 1.11x slower                                                       |
| scimark_fft                | 281 ms                                                       | 318 ms: 1.13x slower                                                       |
| gunicorn                   | 966 us                                                       | 1.10 ms: 1.14x slower                                                      |
| genshi_text                | 25.5 ms                                                      | 29.1 ms: 1.14x slower                                                      |
| pickle_list                | 3.94 us                                                      | 4.50 us: 1.14x slower                                                      |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.15x slower                                                      |
| unpickle                   | 13.3 us                                                      | 15.6 us: 1.18x slower                                                      |
| telco                      | 6.81 ms                                                      | 8.05 ms: 1.18x slower                                                      |
| create_gc_cycles           | 1.58 ms                                                      | 1.89 ms: 1.20x slower                                                      |
| coverage                   | 66.1 ms                                                      | 79.6 ms: 1.20x slower                                                      |
| async_generators           | 322 ms                                                       | 389 ms: 1.21x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 9.43 ms: 1.22x slower                                                      |
| python_startup             | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                      |
| scimark_sor                | 110 ms                                                       | 151 ms: 1.38x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                               |

Benchmark hidden because not significant (6): deepcopy_memo, scimark_sparse_mat_mult, dulwich_log, pickle_pure_python, asyncio_websockets, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 92.42% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x
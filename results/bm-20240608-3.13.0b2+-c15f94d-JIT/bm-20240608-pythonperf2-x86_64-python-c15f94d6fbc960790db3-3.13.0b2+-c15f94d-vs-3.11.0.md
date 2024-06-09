# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: linux-x86_64
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.05x faster
- HPT reliability: 99.54%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 306 ms: 1.07x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.67 ms: 1.03x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.13 sec: 1.10x slower                                                       |
| html5lib       | 72.2 ms                                                      | 73.9 ms: 1.02x slower                                                        |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization     | 629 ms                                                       | 447 ms: 1.41x faster                                                         |
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 843 ms: 1.37x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 438 ms: 1.37x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 350 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 883 ms: 1.33x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 586 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 627 ms: 1.20x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 84.0 ms: 1.11x faster                                                        |
| float          | 74.9 ms                                                      | 73.3 ms: 1.02x faster                                                        |
| pidigits       | 251 ms                                                       | 250 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                        | 1.04x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 140 ms: 1.11x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 25.2 ms: 1.03x slower                                                        |
| regex_effbot   | 3.34 ms                                                      | 3.62 ms: 1.08x slower                                                        |
| regex_dna      | 227 ms                                                       | 251 ms: 1.10x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.7 us: 1.17x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 221 us: 1.08x faster                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.09 sec: 1.08x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 100 ms: 1.06x faster                                                         |
| unpickle_list        | 4.60 us                                                      | 4.70 us: 1.02x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 82.9 ms: 1.04x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 58.4 ms: 1.05x slower                                                        |
| pickle_dict          | 32.3 us                                                      | 34.0 us: 1.05x slower                                                        |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.12x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.54 us: 1.15x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.44 ms: 1.22x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.8 ms: 1.29x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.25x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.15 ms: 1.20x faster                                                        |
| django_template | 39.3 ms                                                      | 41.9 ms: 1.07x slower                                                        |
| genshi_xml      | 57.1 ms                                                      | 62.4 ms: 1.09x slower                                                        |
| genshi_text     | 25.5 ms                                                      | 28.0 ms: 1.10x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 182 us: 2.92x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 380 ms: 1.97x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 34.3 ms: 1.59x faster                                                        |
| async_tree_memoization     | 629 ms                                                       | 447 ms: 1.41x faster                                                         |
| comprehensions             | 25.1 us                                                      | 18.1 us: 1.39x faster                                                        |
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 843 ms: 1.37x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 438 ms: 1.37x faster                                                         |
| pylint                     | 514 ms                                                       | 376 ms: 1.37x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 350 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 883 ms: 1.33x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 586 ms: 1.28x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 21.8 ms: 1.27x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| richards_super             | 63.6 ms                                                      | 52.4 ms: 1.21x faster                                                        |
| fannkuch                   | 416 ms                                                       | 343 ms: 1.21x faster                                                         |
| mako                       | 11.0 ms                                                      | 9.15 ms: 1.20x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 627 ms: 1.20x faster                                                         |
| json_loads                 | 28.9 us                                                      | 24.7 us: 1.17x faster                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 71.1 ms: 1.17x faster                                                        |
| spectral_norm              | 95.1 ms                                                      | 81.6 ms: 1.16x faster                                                        |
| chaos                      | 74.9 ms                                                      | 65.6 ms: 1.14x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.41 us: 1.13x faster                                                        |
| regex_compile              | 156 ms                                                       | 140 ms: 1.11x faster                                                         |
| sympy_sum                  | 186 ms                                                       | 167 ms: 1.11x faster                                                         |
| nbody                      | 92.9 ms                                                      | 84.0 ms: 1.11x faster                                                        |
| logging_format             | 7.71 us                                                      | 7.02 us: 1.10x faster                                                        |
| richards                   | 49.7 ms                                                      | 45.4 ms: 1.09x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.56 sec: 1.08x faster                                                       |
| xml_etree_parse            | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| sympy_str                  | 337 ms                                                       | 312 ms: 1.08x faster                                                         |
| unpickle_pure_python       | 238 us                                                       | 221 us: 1.08x faster                                                         |
| tomli_loads                | 2.25 sec                                                     | 2.09 sec: 1.08x faster                                                       |
| pathlib                    | 18.9 ms                                                      | 17.6 ms: 1.08x faster                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 100 ms: 1.06x faster                                                         |
| deltablue                  | 3.97 ms                                                      | 3.74 ms: 1.06x faster                                                        |
| nqueens                    | 103 ms                                                       | 96.9 ms: 1.06x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.23 sec: 1.06x faster                                                       |
| scimark_monte_carlo        | 69.8 ms                                                      | 66.3 ms: 1.05x faster                                                        |
| hexiom                     | 6.98 ms                                                      | 6.65 ms: 1.05x faster                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 954 us: 1.05x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.82 ms: 1.05x faster                                                        |
| json                       | 5.58 ms                                                      | 5.33 ms: 1.05x faster                                                        |
| sympy_expand               | 553 ms                                                       | 529 ms: 1.05x faster                                                         |
| raytrace                   | 309 ms                                                       | 298 ms: 1.04x faster                                                         |
| chameleon                  | 7.92 ms                                                      | 7.67 ms: 1.03x faster                                                        |
| dulwich_log                | 67.4 ms                                                      | 65.9 ms: 1.02x faster                                                        |
| float                      | 74.9 ms                                                      | 73.3 ms: 1.02x faster                                                        |
| deepcopy_memo              | 37.5 us                                                      | 36.9 us: 1.02x faster                                                        |
| thrift                     | 931 us                                                       | 915 us: 1.02x faster                                                         |
| dask                       | 410 ms                                                       | 403 ms: 1.02x faster                                                         |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| pprint_pformat             | 1.67 sec                                                     | 1.65 sec: 1.01x faster                                                       |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.02 ms: 1.01x faster                                                        |
| sympy_integrate            | 25.8 ms                                                      | 25.7 ms: 1.01x faster                                                        |
| pidigits                   | 251 ms                                                       | 250 ms: 1.00x faster                                                         |
| meteor_contest             | 131 ms                                                       | 131 ms: 1.00x slower                                                         |
| unpickle_list              | 4.60 us                                                      | 4.70 us: 1.02x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 73.9 ms: 1.02x slower                                                        |
| pyflate                    | 449 ms                                                       | 463 ms: 1.03x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 25.2 ms: 1.03x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 82.9 ms: 1.04x slower                                                        |
| go                         | 158 ms                                                       | 164 ms: 1.04x slower                                                         |
| xml_etree_process          | 55.9 ms                                                      | 58.4 ms: 1.05x slower                                                        |
| scimark_fft                | 281 ms                                                       | 295 ms: 1.05x slower                                                         |
| pickle_dict                | 32.3 us                                                      | 34.0 us: 1.05x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 128 ms: 1.05x slower                                                         |
| 2to3                       | 287 ms                                                       | 306 ms: 1.07x slower                                                         |
| django_template            | 39.3 ms                                                      | 41.9 ms: 1.07x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 63.0 ms: 1.07x slower                                                        |
| deepcopy                   | 391 us                                                       | 418 us: 1.07x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.44 ms: 1.07x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.62 ms: 1.08x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.68 us: 1.08x slower                                                        |
| genshi_xml                 | 57.1 ms                                                      | 62.4 ms: 1.09x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 28.0 ms: 1.10x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.13 sec: 1.10x slower                                                       |
| regex_dna                  | 227 ms                                                       | 251 ms: 1.10x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.79 us: 1.10x slower                                                        |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.12x slower                                                        |
| mypy2                      | 762 ms                                                       | 855 ms: 1.12x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.54 us: 1.15x slower                                                        |
| async_generators           | 322 ms                                                       | 378 ms: 1.17x slower                                                         |
| aiohttp                    | 986 us                                                       | 1.17 ms: 1.19x slower                                                        |
| logging_silent             | 100 ns                                                       | 120 ns: 1.20x slower                                                         |
| telco                      | 6.81 ms                                                      | 8.19 ms: 1.20x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.16 ms: 1.20x slower                                                        |
| coverage                   | 66.1 ms                                                      | 80.5 ms: 1.22x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 9.44 ms: 1.22x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.94 ms: 1.23x slower                                                        |
| scimark_sor                | 110 ms                                                       | 138 ms: 1.26x slower                                                         |
| flaskblogging              | 3.88 ms                                                      | 4.90 ms: 1.26x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.8 ms: 1.29x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                 |

Benchmark hidden because not significant (5): scimark_lu, asyncio_websockets, pickle_pure_python, pprint_safe_repr, bench_mp_pool
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.54% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x
# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: windows-amd64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.01x faster
- HPT reliability: 96.14%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 239 ms: 1.12x slower                                                       |
| chameleon      | 5.26 ms                                                     | 5.39 ms: 1.02x slower                                                      |
| docutils       | 1.64 sec                                                    | 1.85 sec: 1.13x slower                                                     |
| html5lib       | 38.9 ms                                                     | 41.9 ms: 1.08x slower                                                      |
| tornado_http   | 92.8 ms                                                     | 87.2 ms: 1.06x faster                                                      |
| Geometric mean | (ref)                                                       | 1.06x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 279 ms: 1.45x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 221 ms: 1.40x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 290 ms: 1.38x faster                                                       |
| async_tree_none            | 332 ms                                                      | 242 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 390 ms: 1.34x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 635 ms: 1.31x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 410 ms: 1.29x faster                                                       |
| async_tree_io              | 808 ms                                                      | 627 ms: 1.29x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.35x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                      | 151 ms: 1.01x slower                                                       |
| float          | 54.4 ms                                                     | 55.9 ms: 1.03x slower                                                      |
| nbody          | 70.3 ms                                                     | 81.2 ms: 1.15x slower                                                      |
| Geometric mean | (ref)                                                       | 1.06x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 116 ms                                                      | 119 ms: 1.03x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.62 ms: 1.08x slower                                                      |
| regex_v8       | 14.2 ms                                                     | 17.1 ms: 1.21x slower                                                      |
| regex_compile  | 91.0 ms                                                     | 111 ms: 1.22x slower                                                       |
| Geometric mean | (ref)                                                       | 1.13x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.82 ms: 1.39x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 92.5 ms: 1.06x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 67.4 ms: 1.03x slower                                                      |
| tomli_loads          | 1.46 sec                                                    | 1.53 sec: 1.05x slower                                                     |
| unpickle_pure_python | 157 us                                                      | 167 us: 1.07x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.77 us: 1.07x slower                                                      |
| json_loads           | 13.0 us                                                     | 14.1 us: 1.08x slower                                                      |
| xml_etree_process    | 37.2 ms                                                     | 40.4 ms: 1.09x slower                                                      |
| pickle_pure_python   | 208 us                                                      | 227 us: 1.09x slower                                                       |
| pickle               | 6.64 us                                                     | 7.26 us: 1.09x slower                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 57.9 ms: 1.10x slower                                                      |
| pickle_list          | 2.70 us                                                     | 3.02 us: 1.12x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.72 us: 1.15x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.04x slower                                                               |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup | 19.8 ms                                                     | 20.5 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                       | 1.01x slower                                                               |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 38.9 ms: 1.03x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 18.2 ms: 1.02x faster                                                      |
| django_template | 24.4 ms                                                     | 25.3 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                       | 1.00x faster                                                               |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1-amd64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 119 us: 2.74x faster                                                       |
| generators                 | 34.0 ms                                                     | 19.7 ms: 1.73x faster                                                      |
| asyncio_tcp                | 726 ms                                                      | 488 ms: 1.49x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.37 sec: 1.48x faster                                                     |
| async_tree_memoization_tg  | 405 ms                                                      | 279 ms: 1.45x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 221 ms: 1.40x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.82 ms: 1.39x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 290 ms: 1.38x faster                                                       |
| async_tree_none            | 332 ms                                                      | 242 ms: 1.37x faster                                                       |
| pylint                     | 323 ms                                                      | 236 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 390 ms: 1.34x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 635 ms: 1.31x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 410 ms: 1.29x faster                                                       |
| async_tree_io              | 808 ms                                                      | 627 ms: 1.29x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.7 ms: 1.18x faster                                                      |
| richards_super             | 38.7 ms                                                     | 33.5 ms: 1.16x faster                                                      |
| raytrace                   | 213 ms                                                      | 188 ms: 1.13x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.25 us: 1.10x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.64 us: 1.08x faster                                                      |
| comprehensions             | 15.6 us                                                     | 14.5 us: 1.08x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 87.2 ms: 1.06x faster                                                      |
| chaos                      | 48.4 ms                                                     | 45.7 ms: 1.06x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 92.5 ms: 1.06x faster                                                      |
| richards                   | 31.4 ms                                                     | 30.0 ms: 1.05x faster                                                      |
| bench_thread_pool          | 872 us                                                      | 848 us: 1.03x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 927 us: 1.03x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 38.9 ms: 1.03x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.57 sec: 1.02x faster                                                     |
| genshi_text                | 18.4 ms                                                     | 18.2 ms: 1.02x faster                                                      |
| pidigits                   | 150 ms                                                      | 151 ms: 1.01x slower                                                       |
| sympy_sum                  | 100 ms                                                      | 102 ms: 1.02x slower                                                       |
| chameleon                  | 5.26 ms                                                     | 5.39 ms: 1.02x slower                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 67.4 ms: 1.03x slower                                                      |
| float                      | 54.4 ms                                                     | 55.9 ms: 1.03x slower                                                      |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.03x slower                                                       |
| go                         | 101 ms                                                      | 104 ms: 1.03x slower                                                       |
| coverage                   | 43.4 ms                                                     | 44.8 ms: 1.03x slower                                                      |
| django_template            | 24.4 ms                                                     | 25.3 ms: 1.03x slower                                                      |
| python_startup             | 19.8 ms                                                     | 20.5 ms: 1.04x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                      |
| thrift                     | 494 us                                                      | 517 us: 1.05x slower                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.53 sec: 1.05x slower                                                     |
| nqueens                    | 68.3 ms                                                     | 71.7 ms: 1.05x slower                                                      |
| meteor_contest             | 75.2 ms                                                     | 79.0 ms: 1.05x slower                                                      |
| sympy_integrate            | 14.0 ms                                                     | 14.9 ms: 1.06x slower                                                      |
| unpickle_pure_python       | 157 us                                                      | 167 us: 1.07x slower                                                       |
| sympy_str                  | 185 ms                                                      | 197 ms: 1.07x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.77 us: 1.07x slower                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 52.3 ms: 1.07x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 68.1 ms: 1.08x slower                                                      |
| pprint_pformat             | 1.09 sec                                                    | 1.17 sec: 1.08x slower                                                     |
| logging_silent             | 71.8 ns                                                     | 77.4 ns: 1.08x slower                                                      |
| html5lib                   | 38.9 ms                                                     | 41.9 ms: 1.08x slower                                                      |
| deepcopy                   | 246 us                                                      | 266 us: 1.08x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.62 ms: 1.08x slower                                                      |
| json_loads                 | 13.0 us                                                     | 14.1 us: 1.08x slower                                                      |
| pyflate                    | 312 ms                                                      | 339 ms: 1.09x slower                                                       |
| xml_etree_process          | 37.2 ms                                                     | 40.4 ms: 1.09x slower                                                      |
| pickle_pure_python         | 208 us                                                      | 227 us: 1.09x slower                                                       |
| pprint_safe_repr           | 529 ms                                                      | 577 ms: 1.09x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.26 us: 1.09x slower                                                      |
| deepcopy_reduce            | 2.06 us                                                     | 2.26 us: 1.09x slower                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 57.9 ms: 1.10x slower                                                      |
| fannkuch                   | 253 ms                                                      | 280 ms: 1.11x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 79.1 ms: 1.12x slower                                                      |
| 2to3                       | 214 ms                                                      | 239 ms: 1.12x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.02 us: 1.12x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 38.9 ms: 1.13x slower                                                      |
| sympy_expand               | 299 ms                                                      | 337 ms: 1.13x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.85 sec: 1.13x slower                                                     |
| scimark_fft                | 179 ms                                                      | 204 ms: 1.14x slower                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 51.9 ms: 1.15x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.72 us: 1.15x slower                                                      |
| nbody                      | 70.3 ms                                                     | 81.2 ms: 1.15x slower                                                      |
| pycparser                  | 720 ms                                                      | 831 ms: 1.15x slower                                                       |
| spectral_norm              | 68.3 ms                                                     | 80.8 ms: 1.18x slower                                                      |
| scimark_sor                | 78.1 ms                                                     | 93.2 ms: 1.19x slower                                                      |
| deepcopy_memo              | 26.0 us                                                     | 31.2 us: 1.20x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 17.1 ms: 1.21x slower                                                      |
| regex_compile              | 91.0 ms                                                     | 111 ms: 1.22x slower                                                       |
| telco                      | 4.06 ms                                                     | 5.04 ms: 1.24x slower                                                      |
| hexiom                     | 4.55 ms                                                     | 5.76 ms: 1.26x slower                                                      |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 3.29 ms: 1.28x slower                                                      |
| create_gc_cycles           | 713 us                                                      | 926 us: 1.30x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 83.1 ms: 1.32x slower                                                      |
| async_generators           | 177 ms                                                      | 254 ms: 1.43x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.01x faster                                                               |

Benchmark hidden because not significant (7): json, python_startup_no_site, mako, pickle_dict, deltablue, flaskblogging, sqlglot_transpile
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 96.14% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown
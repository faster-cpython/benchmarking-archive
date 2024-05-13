# Results vs. 3.11.0

- fork: python
- ref: 44995aab499b09a550de
- machine: windows-amd64
- commit hash: 44995aa
- commit date: 2024-05-13
- overall geometric mean: 1.01x faster
- HPT reliability: 78.61%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 234 ms: 1.09x slower                                                        |
| chameleon      | 5.26 ms                                                     | 5.12 ms: 1.03x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.83 sec: 1.11x slower                                                      |
| html5lib       | 38.9 ms                                                     | 41.3 ms: 1.06x slower                                                       |
| tornado_http   | 92.8 ms                                                     | 87.9 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 232 ms: 1.43x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 216 ms: 1.43x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 280 ms: 1.43x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 388 ms: 1.35x faster                                                        |
| async_tree_io              | 808 ms                                                      | 604 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 401 ms: 1.32x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 628 ms: 1.32x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 51.7 ms: 1.05x faster                                                       |
| nbody          | 70.3 ms                                                     | 72.7 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.10x slower                                                       |
| regex_compile  | 91.0 ms                                                     | 107 ms: 1.18x slower                                                        |
| Geometric mean | (ref)                                                       | 1.08x slower                                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.71 ms: 1.42x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 88.5 ms: 1.10x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.42 sec: 1.02x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.2 ms: 1.02x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 155 us: 1.01x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 212 us: 1.02x slower                                                        |
| xml_etree_process    | 37.2 ms                                                     | 38.9 ms: 1.05x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.73 us: 1.06x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 56.1 ms: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.16 us: 1.08x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.1 us: 1.08x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.36 us: 1.10x slower                                                       |
| pickle_list          | 2.70 us                                                     | 3.11 us: 1.15x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text    | 18.4 ms                                                     | 16.7 ms: 1.11x faster                                                       |
| genshi_xml     | 39.9 ms                                                     | 36.5 ms: 1.10x faster                                                       |
| mako           | 7.58 ms                                                     | 7.20 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 115 us: 2.83x faster                                                        |
| generators                 | 34.0 ms                                                     | 19.4 ms: 1.75x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 232 ms: 1.43x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 216 ms: 1.43x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 280 ms: 1.43x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.71 ms: 1.42x faster                                                       |
| pylint                     | 323 ms                                                      | 232 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 388 ms: 1.35x faster                                                        |
| async_tree_io              | 808 ms                                                      | 604 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 401 ms: 1.32x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 628 ms: 1.32x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.55 sec: 1.31x faster                                                      |
| asyncio_tcp                | 726 ms                                                      | 578 ms: 1.26x faster                                                        |
| comprehensions             | 15.6 us                                                     | 13.1 us: 1.20x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.6 ms: 1.19x faster                                                       |
| richards_super             | 38.7 ms                                                     | 32.6 ms: 1.19x faster                                                       |
| raytrace                   | 213 ms                                                      | 182 ms: 1.17x faster                                                        |
| chaos                      | 48.4 ms                                                     | 43.3 ms: 1.12x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.17 us: 1.11x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 16.7 ms: 1.11x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 88.5 ms: 1.10x faster                                                       |
| richards                   | 31.4 ms                                                     | 28.5 ms: 1.10x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 869 us: 1.10x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 36.5 ms: 1.10x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.60 us: 1.08x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.54 ms: 1.06x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 87.9 ms: 1.06x faster                                                       |
| mako                       | 7.58 ms                                                     | 7.20 ms: 1.05x faster                                                       |
| float                      | 54.4 ms                                                     | 51.7 ms: 1.05x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1.11 ms: 1.05x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.52 sec: 1.05x faster                                                      |
| nqueens                    | 68.3 ms                                                     | 65.3 ms: 1.05x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 69.1 ns: 1.04x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 5.12 ms: 1.03x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.42 sec: 1.02x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.2 ms: 1.02x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 98.4 ms: 1.02x faster                                                       |
| go                         | 101 ms                                                      | 99.6 ms: 1.01x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 155 us: 1.01x faster                                                        |
| dulwich_log                | 46.4 ms                                                     | 46.0 ms: 1.01x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| pprint_safe_repr           | 529 ms                                                      | 532 ms: 1.00x slower                                                        |
| deepcopy                   | 246 us                                                      | 248 us: 1.01x slower                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 49.3 ms: 1.01x slower                                                       |
| pickle_pure_python         | 208 us                                                      | 212 us: 1.02x slower                                                        |
| python_startup             | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                                       |
| pyflate                    | 312 ms                                                      | 321 ms: 1.03x slower                                                        |
| coverage                   | 43.4 ms                                                     | 44.6 ms: 1.03x slower                                                       |
| fannkuch                   | 253 ms                                                      | 261 ms: 1.03x slower                                                        |
| nbody                      | 70.3 ms                                                     | 72.7 ms: 1.03x slower                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.13 us: 1.03x slower                                                       |
| sympy_integrate            | 14.0 ms                                                     | 14.6 ms: 1.04x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                       |
| xml_etree_process          | 37.2 ms                                                     | 38.9 ms: 1.05x slower                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 47.4 ms: 1.05x slower                                                       |
| sympy_str                  | 185 ms                                                      | 194 ms: 1.05x slower                                                        |
| gc_traversal               | 1.49 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.73 us: 1.06x slower                                                       |
| scimark_fft                | 179 ms                                                      | 190 ms: 1.06x slower                                                        |
| html5lib                   | 38.9 ms                                                     | 41.3 ms: 1.06x slower                                                       |
| pycparser                  | 720 ms                                                      | 768 ms: 1.07x slower                                                        |
| xml_etree_generate         | 52.5 ms                                                     | 56.1 ms: 1.07x slower                                                       |
| deepcopy_memo              | 26.0 us                                                     | 27.8 us: 1.07x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.16 us: 1.08x slower                                                       |
| aiohttp                    | 883 us                                                      | 953 us: 1.08x slower                                                        |
| bench_mp_pool              | 63.2 ms                                                     | 68.3 ms: 1.08x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.1 us: 1.08x slower                                                       |
| 2to3                       | 214 ms                                                      | 234 ms: 1.09x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.10x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.36 us: 1.10x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 38.2 ms: 1.11x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 86.8 ms: 1.11x slower                                                       |
| sympy_expand               | 299 ms                                                      | 332 ms: 1.11x slower                                                        |
| spectral_norm              | 68.3 ms                                                     | 76.0 ms: 1.11x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.83 sec: 1.11x slower                                                      |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.88 ms: 1.12x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 79.9 ms: 1.13x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 5.23 ms: 1.15x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.11 us: 1.15x slower                                                       |
| regex_compile              | 91.0 ms                                                     | 107 ms: 1.18x slower                                                        |
| scimark_lu                 | 62.8 ms                                                     | 74.9 ms: 1.19x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.88 ms: 1.20x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 914 us: 1.28x slower                                                        |
| async_generators           | 177 ms                                                      | 241 ms: 1.36x slower                                                        |
| thrift                     | 494 us                                                      | 9.71 ms: 19.66x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (9): json, python_startup_no_site, bench_thread_pool, pickle_dict, pidigits, django_template, regex_dna, pprint_pformat, meteor_contest
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 78.61% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
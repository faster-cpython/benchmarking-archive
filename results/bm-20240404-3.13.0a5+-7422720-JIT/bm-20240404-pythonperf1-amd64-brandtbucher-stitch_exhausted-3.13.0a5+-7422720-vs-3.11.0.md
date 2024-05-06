# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 222 ms: 1.04x slower                                                          |
| chameleon      | 5.26 ms                                                     | 4.81 ms: 1.09x faster                                                         |
| docutils       | 1.64 sec                                                    | 1.72 sec: 1.05x slower                                                        |
| html5lib       | 38.9 ms                                                     | 35.6 ms: 1.09x faster                                                         |
| tornado_http   | 92.8 ms                                                     | 83.6 ms: 1.11x faster                                                         |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 264 ms: 1.53x faster                                                          |
| async_tree_none            | 332 ms                                                      | 222 ms: 1.50x faster                                                          |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                          |
| async_tree_none_tg         | 309 ms                                                      | 215 ms: 1.44x faster                                                          |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 386 ms: 1.37x faster                                                          |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                                          |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                                          |
| async_tree_io_tg           | 829 ms                                                      | 616 ms: 1.35x faster                                                          |
| Geometric mean             | (ref)                                                       | 1.43x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 59.0 ms: 1.19x faster                                                         |
| float          | 54.4 ms                                                     | 46.6 ms: 1.17x faster                                                         |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 86.6 ms: 1.05x faster                                                         |
| regex_dna      | 116 ms                                                      | 116 ms: 1.00x slower                                                          |
| regex_v8       | 14.2 ms                                                     | 14.4 ms: 1.02x slower                                                         |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.53 ms: 1.46x faster                                                         |
| unpickle_pure_python | 157 us                                                      | 129 us: 1.22x faster                                                          |
| pickle_pure_python   | 208 us                                                      | 173 us: 1.20x faster                                                          |
| tomli_loads          | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 90.3 ms: 1.08x faster                                                         |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.3 ms: 1.07x faster                                                         |
| xml_etree_process    | 37.2 ms                                                     | 36.6 ms: 1.02x faster                                                         |
| xml_etree_generate   | 52.5 ms                                                     | 53.1 ms: 1.01x slower                                                         |
| json_loads           | 13.0 us                                                     | 13.6 us: 1.04x slower                                                         |
| unpickle_list        | 2.59 us                                                     | 2.82 us: 1.09x slower                                                         |
| pickle               | 6.64 us                                                     | 7.29 us: 1.10x slower                                                         |
| unpickle             | 7.57 us                                                     | 8.55 us: 1.13x slower                                                         |
| pickle_list          | 2.70 us                                                     | 3.16 us: 1.17x slower                                                         |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                  |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                         |
| python_startup_no_site | 16.8 ms                                                     | 19.7 ms: 1.17x slower                                                         |
| Geometric mean         | (ref)                                                       | 1.14x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 5.64 ms: 1.34x faster                                                         |
| genshi_text    | 18.4 ms                                                     | 15.4 ms: 1.20x faster                                                         |
| genshi_xml     | 39.9 ms                                                     | 35.7 ms: 1.12x faster                                                         |
| Geometric mean | (ref)                                                       | 1.22x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 75.2 us: 4.33x faster                                                         |
| generators                 | 34.0 ms                                                     | 19.3 ms: 1.76x faster                                                         |
| pylint                     | 323 ms                                                      | 198 ms: 1.63x faster                                                          |
| async_tree_memoization_tg  | 405 ms                                                      | 264 ms: 1.53x faster                                                          |
| asyncio_tcp                | 726 ms                                                      | 481 ms: 1.51x faster                                                          |
| async_tree_none            | 332 ms                                                      | 222 ms: 1.50x faster                                                          |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                          |
| json_dumps                 | 8.09 ms                                                     | 5.53 ms: 1.46x faster                                                         |
| async_tree_none_tg         | 309 ms                                                      | 215 ms: 1.44x faster                                                          |
| comprehensions             | 15.6 us                                                     | 11.3 us: 1.38x faster                                                         |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 386 ms: 1.37x faster                                                          |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                                          |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                                          |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.49 sec: 1.36x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 53.1 ns: 1.35x faster                                                         |
| async_tree_io_tg           | 829 ms                                                      | 616 ms: 1.35x faster                                                          |
| mako                       | 7.58 ms                                                     | 5.64 ms: 1.34x faster                                                         |
| spectral_norm              | 68.3 ms                                                     | 51.9 ms: 1.32x faster                                                         |
| richards_super             | 38.7 ms                                                     | 29.9 ms: 1.29x faster                                                         |
| raytrace                   | 213 ms                                                      | 167 ms: 1.28x faster                                                          |
| deltablue                  | 2.70 ms                                                     | 2.15 ms: 1.26x faster                                                         |
| sqlglot_parse              | 953 us                                                      | 774 us: 1.23x faster                                                          |
| unpickle_pure_python       | 157 us                                                      | 129 us: 1.22x faster                                                          |
| chaos                      | 48.4 ms                                                     | 40.0 ms: 1.21x faster                                                         |
| pickle_pure_python         | 208 us                                                      | 173 us: 1.20x faster                                                          |
| tomli_loads                | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 15.4 ms: 1.20x faster                                                         |
| nbody                      | 70.3 ms                                                     | 59.0 ms: 1.19x faster                                                         |
| deepcopy_memo              | 26.0 us                                                     | 21.9 us: 1.19x faster                                                         |
| richards                   | 31.4 ms                                                     | 26.5 ms: 1.19x faster                                                         |
| logging_simple             | 6.86 us                                                     | 5.86 us: 1.17x faster                                                         |
| sqlglot_transpile          | 1.16 ms                                                     | 997 us: 1.17x faster                                                          |
| float                      | 54.4 ms                                                     | 46.6 ms: 1.17x faster                                                         |
| coroutines                 | 15.0 ms                                                     | 12.9 ms: 1.16x faster                                                         |
| pyflate                    | 312 ms                                                      | 270 ms: 1.16x faster                                                          |
| pprint_pformat             | 1.09 sec                                                    | 952 ms: 1.14x faster                                                          |
| logging_format             | 7.16 us                                                     | 6.27 us: 1.14x faster                                                         |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.7 ms: 1.14x faster                                                         |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.26 ms: 1.14x faster                                                         |
| sqlite_synth               | 1.77 us                                                     | 1.56 us: 1.13x faster                                                         |
| dulwich_log                | 46.4 ms                                                     | 41.2 ms: 1.13x faster                                                         |
| pprint_safe_repr           | 529 ms                                                      | 471 ms: 1.12x faster                                                          |
| go                         | 101 ms                                                      | 89.9 ms: 1.12x faster                                                         |
| genshi_xml                 | 39.9 ms                                                     | 35.7 ms: 1.12x faster                                                         |
| tornado_http               | 92.8 ms                                                     | 83.6 ms: 1.11x faster                                                         |
| fannkuch                   | 253 ms                                                      | 230 ms: 1.10x faster                                                          |
| sympy_sum                  | 100 ms                                                      | 90.9 ms: 1.10x faster                                                         |
| crypto_pyaes               | 48.9 ms                                                     | 44.5 ms: 1.10x faster                                                         |
| chameleon                  | 5.26 ms                                                     | 4.81 ms: 1.09x faster                                                         |
| html5lib                   | 38.9 ms                                                     | 35.6 ms: 1.09x faster                                                         |
| bench_thread_pool          | 872 us                                                      | 803 us: 1.09x faster                                                          |
| xml_etree_parse            | 97.6 ms                                                     | 90.3 ms: 1.08x faster                                                         |
| nqueens                    | 68.3 ms                                                     | 63.3 ms: 1.08x faster                                                         |
| sympy_str                  | 185 ms                                                      | 172 ms: 1.08x faster                                                          |
| deepcopy                   | 246 us                                                      | 229 us: 1.08x faster                                                          |
| scimark_fft                | 179 ms                                                      | 167 ms: 1.07x faster                                                          |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.3 ms: 1.07x faster                                                         |
| pycparser                  | 720 ms                                                      | 677 ms: 1.06x faster                                                          |
| regex_compile              | 91.0 ms                                                     | 86.6 ms: 1.05x faster                                                         |
| deepcopy_reduce            | 2.06 us                                                     | 1.97 us: 1.05x faster                                                         |
| mdp                        | 1.59 sec                                                    | 1.53 sec: 1.04x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 186 ms: 1.02x faster                                                          |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                          |
| sympy_expand               | 299 ms                                                      | 293 ms: 1.02x faster                                                          |
| sympy_integrate            | 14.0 ms                                                     | 13.8 ms: 1.02x faster                                                         |
| xml_etree_process          | 37.2 ms                                                     | 36.6 ms: 1.02x faster                                                         |
| regex_dna                  | 116 ms                                                      | 116 ms: 1.00x slower                                                          |
| xml_etree_generate         | 52.5 ms                                                     | 53.1 ms: 1.01x slower                                                         |
| meteor_contest             | 75.2 ms                                                     | 76.1 ms: 1.01x slower                                                         |
| mypy2                      | 459 ms                                                      | 467 ms: 1.02x slower                                                          |
| regex_v8                   | 14.2 ms                                                     | 14.4 ms: 1.02x slower                                                         |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                         |
| aiohttp                    | 883 us                                                      | 911 us: 1.03x slower                                                          |
| scimark_sor                | 78.1 ms                                                     | 80.9 ms: 1.04x slower                                                         |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                         |
| 2to3                       | 214 ms                                                      | 222 ms: 1.04x slower                                                          |
| sqlglot_optimize           | 34.5 ms                                                     | 36.0 ms: 1.04x slower                                                         |
| json_loads                 | 13.0 us                                                     | 13.6 us: 1.04x slower                                                         |
| docutils                   | 1.64 sec                                                    | 1.72 sec: 1.05x slower                                                        |
| hexiom                     | 4.55 ms                                                     | 4.81 ms: 1.06x slower                                                         |
| bench_mp_pool              | 63.2 ms                                                     | 67.7 ms: 1.07x slower                                                         |
| unpickle_list              | 2.59 us                                                     | 2.82 us: 1.09x slower                                                         |
| coverage                   | 43.4 ms                                                     | 47.5 ms: 1.09x slower                                                         |
| pickle                     | 6.64 us                                                     | 7.29 us: 1.10x slower                                                         |
| pathlib                    | 70.9 ms                                                     | 77.9 ms: 1.10x slower                                                         |
| python_startup             | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                         |
| scimark_lu                 | 62.8 ms                                                     | 70.7 ms: 1.13x slower                                                         |
| unpickle                   | 7.57 us                                                     | 8.55 us: 1.13x slower                                                         |
| pickle_list                | 2.70 us                                                     | 3.16 us: 1.17x slower                                                         |
| python_startup_no_site     | 16.8 ms                                                     | 19.7 ms: 1.17x slower                                                         |
| telco                      | 4.06 ms                                                     | 4.76 ms: 1.17x slower                                                         |
| create_gc_cycles           | 713 us                                                      | 891 us: 1.25x slower                                                          |
| async_generators           | 177 ms                                                      | 243 ms: 1.37x slower                                                          |
| thrift                     | 494 us                                                      | 9.17 ms: 18.56x slower                                                        |
| Geometric mean             | (ref)                                                       | 1.09x faster                                                                  |

Benchmark hidden because not significant (2): json, pickle_dict
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown
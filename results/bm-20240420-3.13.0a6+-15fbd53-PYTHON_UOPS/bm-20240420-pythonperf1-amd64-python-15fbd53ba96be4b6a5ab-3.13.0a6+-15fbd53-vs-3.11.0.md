# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.02x faster
- HPT reliability: 70.96%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 224 ms: 1.05x slower                                                        |
| chameleon      | 5.26 ms                                                     | 5.02 ms: 1.05x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.74 sec: 1.06x slower                                                      |
| html5lib       | 38.9 ms                                                     | 40.5 ms: 1.04x slower                                                       |
| tornado_http   | 92.8 ms                                                     | 84.1 ms: 1.10x faster                                                       |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 275 ms: 1.47x faster                                                        |
| async_tree_none            | 332 ms                                                      | 228 ms: 1.45x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 276 ms: 1.45x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 226 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                        |
| async_tree_io              | 808 ms                                                      | 594 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 395 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 625 ms: 1.33x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                      | 148 ms: 1.02x faster                                                        |
| float          | 54.4 ms                                                     | 57.9 ms: 1.07x slower                                                       |
| nbody          | 70.3 ms                                                     | 83.1 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                       | 1.07x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                                       |
| regex_compile  | 91.0 ms                                                     | 103 ms: 1.13x slower                                                        |
| Geometric mean | (ref)                                                       | 1.08x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.70 ms: 1.42x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 185 us: 1.13x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 90.0 ms: 1.08x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.6 us: 1.00x slower                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 66.5 ms: 1.01x slower                                                       |
| xml_etree_process    | 37.2 ms                                                     | 38.7 ms: 1.04x slower                                                       |
| unpickle_pure_python | 157 us                                                      | 166 us: 1.06x slower                                                        |
| json_loads           | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 56.5 ms: 1.07x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.86 us: 1.11x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.54 us: 1.13x slower                                                       |
| pickle               | 6.64 us                                                     | 7.53 us: 1.13x slower                                                       |
| pickle_list          | 2.70 us                                                     | 3.06 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.3 ms: 1.03x faster                                                       |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 16.4 ms: 1.12x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 35.8 ms: 1.12x faster                                                       |
| django_template | 24.4 ms                                                     | 23.3 ms: 1.05x faster                                                       |
| mako            | 7.58 ms                                                     | 7.41 ms: 1.02x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.08x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 75.7 us: 4.31x faster                                                       |
| generators                 | 34.0 ms                                                     | 20.7 ms: 1.64x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 477 ms: 1.52x faster                                                        |
| pylint                     | 323 ms                                                      | 219 ms: 1.48x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 275 ms: 1.47x faster                                                        |
| async_tree_none            | 332 ms                                                      | 228 ms: 1.45x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 276 ms: 1.45x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.70 ms: 1.42x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 226 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                        |
| async_tree_io              | 808 ms                                                      | 594 ms: 1.36x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.49 sec: 1.36x faster                                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 395 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 625 ms: 1.33x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 57.1 ns: 1.26x faster                                                       |
| raytrace                   | 213 ms                                                      | 176 ms: 1.21x faster                                                        |
| richards_super             | 38.7 ms                                                     | 32.4 ms: 1.19x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 827 us: 1.15x faster                                                        |
| coroutines                 | 15.0 ms                                                     | 13.0 ms: 1.15x faster                                                       |
| comprehensions             | 15.6 us                                                     | 13.8 us: 1.14x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.06 us: 1.13x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 185 us: 1.13x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 16.4 ms: 1.12x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 35.8 ms: 1.12x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1.04 ms: 1.12x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.45 us: 1.11x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 84.1 ms: 1.10x faster                                                       |
| richards                   | 31.4 ms                                                     | 28.6 ms: 1.10x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.49 ms: 1.09x faster                                                       |
| chaos                      | 48.4 ms                                                     | 44.6 ms: 1.09x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 90.0 ms: 1.08x faster                                                       |
| deepcopy                   | 246 us                                                      | 229 us: 1.08x faster                                                        |
| mdp                        | 1.59 sec                                                    | 1.49 sec: 1.07x faster                                                      |
| dulwich_log                | 46.4 ms                                                     | 43.4 ms: 1.07x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 94.7 ms: 1.06x faster                                                       |
| django_template            | 24.4 ms                                                     | 23.3 ms: 1.05x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 24.8 us: 1.05x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 5.02 ms: 1.05x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 835 us: 1.05x faster                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 16.3 ms: 1.03x faster                                                       |
| mako                       | 7.58 ms                                                     | 7.41 ms: 1.02x faster                                                       |
| sympy_str                  | 185 ms                                                      | 181 ms: 1.02x faster                                                        |
| pidigits                   | 150 ms                                                      | 148 ms: 1.02x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 13.8 ms: 1.02x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 187 ms: 1.02x faster                                                        |
| deepcopy_reduce            | 2.06 us                                                     | 2.04 us: 1.01x faster                                                       |
| mypy2                      | 459 ms                                                      | 457 ms: 1.01x faster                                                        |
| pickle_dict                | 18.5 us                                                     | 18.6 us: 1.00x slower                                                       |
| go                         | 101 ms                                                      | 102 ms: 1.01x slower                                                        |
| xml_etree_iterparse        | 65.6 ms                                                     | 66.5 ms: 1.01x slower                                                       |
| meteor_contest             | 75.2 ms                                                     | 76.4 ms: 1.02x slower                                                       |
| pprint_pformat             | 1.09 sec                                                    | 1.11 sec: 1.02x slower                                                      |
| sympy_expand               | 299 ms                                                      | 304 ms: 1.02x slower                                                        |
| pprint_safe_repr           | 529 ms                                                      | 542 ms: 1.02x slower                                                        |
| aiohttp                    | 883 us                                                      | 907 us: 1.03x slower                                                        |
| bench_mp_pool              | 63.2 ms                                                     | 65.2 ms: 1.03x slower                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 50.5 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| xml_etree_process          | 37.2 ms                                                     | 38.7 ms: 1.04x slower                                                       |
| html5lib                   | 38.9 ms                                                     | 40.5 ms: 1.04x slower                                                       |
| 2to3                       | 214 ms                                                      | 224 ms: 1.05x slower                                                        |
| unpickle_pure_python       | 157 us                                                      | 166 us: 1.06x slower                                                        |
| regex_effbot               | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 36.6 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.74 sec: 1.06x slower                                                      |
| float                      | 54.4 ms                                                     | 57.9 ms: 1.07x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 56.5 ms: 1.07x slower                                                       |
| pyflate                    | 312 ms                                                      | 336 ms: 1.08x slower                                                        |
| pathlib                    | 70.9 ms                                                     | 76.5 ms: 1.08x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.86 us: 1.11x slower                                                       |
| fannkuch                   | 253 ms                                                      | 285 ms: 1.12x slower                                                        |
| unpickle                   | 7.57 us                                                     | 8.54 us: 1.13x slower                                                       |
| coverage                   | 43.4 ms                                                     | 49.1 ms: 1.13x slower                                                       |
| regex_compile              | 91.0 ms                                                     | 103 ms: 1.13x slower                                                        |
| pickle                     | 6.64 us                                                     | 7.53 us: 1.13x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.06 us: 1.14x slower                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 51.6 ms: 1.14x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 5.24 ms: 1.15x slower                                                       |
| scimark_fft                | 179 ms                                                      | 208 ms: 1.16x slower                                                        |
| scimark_sor                | 78.1 ms                                                     | 91.1 ms: 1.17x slower                                                       |
| nbody                      | 70.3 ms                                                     | 83.1 ms: 1.18x slower                                                       |
| spectral_norm              | 68.3 ms                                                     | 81.7 ms: 1.20x slower                                                       |
| telco                      | 4.06 ms                                                     | 5.00 ms: 1.23x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 78.3 ms: 1.25x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 900 us: 1.26x slower                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 3.30 ms: 1.28x slower                                                       |
| async_generators           | 177 ms                                                      | 243 ms: 1.37x slower                                                        |
| thrift                     | 494 us                                                      | 9.18 ms: 18.59x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.02x faster                                                                |

Benchmark hidden because not significant (5): nqueens, tomli_loads, python_startup, pycparser, json
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 70.96% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
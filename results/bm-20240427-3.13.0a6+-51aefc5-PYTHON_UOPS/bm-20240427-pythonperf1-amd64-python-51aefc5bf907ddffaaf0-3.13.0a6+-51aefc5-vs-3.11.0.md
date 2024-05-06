# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-amd64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.00x slower
- HPT reliability: 64.92%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 232 ms: 1.09x slower                                                        |
| chameleon      | 5.26 ms                                                     | 5.08 ms: 1.03x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.79 sec: 1.09x slower                                                      |
| tornado_http   | 92.8 ms                                                     | 94.8 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 282 ms: 1.43x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 285 ms: 1.40x faster                                                        |
| async_tree_none            | 332 ms                                                      | 238 ms: 1.40x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 227 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 392 ms: 1.33x faster                                                        |
| async_tree_io              | 808 ms                                                      | 609 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 405 ms: 1.31x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 646 ms: 1.28x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.35x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                      | 149 ms: 1.01x faster                                                        |
| nbody          | 70.3 ms                                                     | 74.3 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 116 ms                                                      | 118 ms: 1.01x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| regex_compile  | 91.0 ms                                                     | 106 ms: 1.17x slower                                                        |
| regex_v8       | 14.2 ms                                                     | 20.0 ms: 1.41x slower                                                       |
| Geometric mean | (ref)                                                       | 1.15x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.81 ms: 1.39x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 186 us: 1.12x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 93.7 ms: 1.04x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 159 us: 1.01x slower                                                        |
| xml_etree_iterparse  | 65.6 ms                                                     | 67.8 ms: 1.03x slower                                                       |
| xml_etree_process    | 37.2 ms                                                     | 38.8 ms: 1.04x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 57.3 ms: 1.09x slower                                                       |
| pickle_dict          | 18.5 us                                                     | 20.2 us: 1.10x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.97 us: 1.10x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.85 us: 1.10x slower                                                       |
| pickle               | 6.64 us                                                     | 7.45 us: 1.12x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.6 us: 1.13x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.83 us: 1.17x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.02x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.7 ms: 1.01x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.5 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.96 ms: 1.09x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 37.3 ms: 1.07x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 17.8 ms: 1.03x faster                                                       |
| django_template | 24.4 ms                                                     | 24.2 ms: 1.01x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.05x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 116 us: 2.81x faster                                                        |
| generators                 | 34.0 ms                                                     | 22.7 ms: 1.49x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 282 ms: 1.43x faster                                                        |
| pylint                     | 323 ms                                                      | 227 ms: 1.42x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 285 ms: 1.40x faster                                                        |
| async_tree_none            | 332 ms                                                      | 238 ms: 1.40x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.81 ms: 1.39x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 227 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 392 ms: 1.33x faster                                                        |
| async_tree_io              | 808 ms                                                      | 609 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 405 ms: 1.31x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 646 ms: 1.28x faster                                                        |
| richards_super             | 38.7 ms                                                     | 30.7 ms: 1.26x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 57.8 ns: 1.24x faster                                                       |
| raytrace                   | 213 ms                                                      | 177 ms: 1.20x faster                                                        |
| comprehensions             | 15.6 us                                                     | 13.3 us: 1.18x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.73 sec: 1.17x faster                                                      |
| richards                   | 31.4 ms                                                     | 27.3 ms: 1.15x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.15x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 186 us: 1.12x faster                                                        |
| logging_simple             | 6.86 us                                                     | 6.20 us: 1.11x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1.06 ms: 1.10x faster                                                       |
| chaos                      | 48.4 ms                                                     | 44.1 ms: 1.10x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 23.8 us: 1.09x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.56 us: 1.09x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 874 us: 1.09x faster                                                        |
| mako                       | 7.58 ms                                                     | 6.96 ms: 1.09x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.64 us: 1.08x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 676 ms: 1.07x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 37.3 ms: 1.07x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.52 ms: 1.07x faster                                                       |
| deepcopy                   | 246 us                                                      | 231 us: 1.07x faster                                                        |
| mdp                        | 1.59 sec                                                    | 1.51 sec: 1.06x faster                                                      |
| sympy_sum                  | 100 ms                                                      | 95.6 ms: 1.05x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 93.7 ms: 1.04x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 5.08 ms: 1.03x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 44.9 ms: 1.03x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 17.8 ms: 1.03x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                                      |
| coverage                   | 43.4 ms                                                     | 42.8 ms: 1.01x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 1.07 sec: 1.01x faster                                                      |
| pprint_safe_repr           | 529 ms                                                      | 523 ms: 1.01x faster                                                        |
| django_template            | 24.4 ms                                                     | 24.2 ms: 1.01x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.04 us: 1.01x faster                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 16.7 ms: 1.01x faster                                                       |
| pidigits                   | 150 ms                                                      | 149 ms: 1.01x faster                                                        |
| go                         | 101 ms                                                      | 102 ms: 1.01x slower                                                        |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.01x slower                                                        |
| unpickle_pure_python       | 157 us                                                      | 159 us: 1.01x slower                                                        |
| meteor_contest             | 75.2 ms                                                     | 76.3 ms: 1.01x slower                                                       |
| tornado_http               | 92.8 ms                                                     | 94.8 ms: 1.02x slower                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 50.0 ms: 1.02x slower                                                       |
| sqlglot_normalize          | 190 ms                                                      | 195 ms: 1.03x slower                                                        |
| xml_etree_iterparse        | 65.6 ms                                                     | 67.8 ms: 1.03x slower                                                       |
| python_startup             | 19.8 ms                                                     | 20.5 ms: 1.03x slower                                                       |
| nqueens                    | 68.3 ms                                                     | 70.7 ms: 1.04x slower                                                       |
| pyflate                    | 312 ms                                                      | 324 ms: 1.04x slower                                                        |
| sympy_expand               | 299 ms                                                      | 311 ms: 1.04x slower                                                        |
| xml_etree_process          | 37.2 ms                                                     | 38.8 ms: 1.04x slower                                                       |
| mypy2                      | 459 ms                                                      | 480 ms: 1.05x slower                                                        |
| nbody                      | 70.3 ms                                                     | 74.3 ms: 1.06x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| fannkuch                   | 253 ms                                                      | 268 ms: 1.06x slower                                                        |
| gc_traversal               | 1.49 ms                                                     | 1.58 ms: 1.06x slower                                                       |
| pycparser                  | 720 ms                                                      | 767 ms: 1.07x slower                                                        |
| json                       | 2.98 ms                                                     | 3.17 ms: 1.07x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 67.7 ms: 1.07x slower                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 48.7 ms: 1.08x slower                                                       |
| 2to3                       | 214 ms                                                      | 232 ms: 1.09x slower                                                        |
| docutils                   | 1.64 sec                                                    | 1.79 sec: 1.09x slower                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 57.3 ms: 1.09x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 37.7 ms: 1.09x slower                                                       |
| spectral_norm              | 68.3 ms                                                     | 74.6 ms: 1.09x slower                                                       |
| pickle_dict                | 18.5 us                                                     | 20.2 us: 1.10x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.97 us: 1.10x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.85 us: 1.10x slower                                                       |
| aiohttp                    | 883 us                                                      | 986 us: 1.12x slower                                                        |
| pickle                     | 6.64 us                                                     | 7.45 us: 1.12x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.6 us: 1.13x slower                                                       |
| scimark_fft                | 179 ms                                                      | 202 ms: 1.13x slower                                                        |
| hexiom                     | 4.55 ms                                                     | 5.29 ms: 1.16x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 82.3 ms: 1.16x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.83 us: 1.17x slower                                                       |
| regex_compile              | 91.0 ms                                                     | 106 ms: 1.17x slower                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 3.02 ms: 1.17x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 92.9 ms: 1.19x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.95 ms: 1.22x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 80.8 ms: 1.29x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 929 us: 1.30x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 20.0 ms: 1.41x slower                                                       |
| async_generators           | 177 ms                                                      | 251 ms: 1.42x slower                                                        |
| thrift                     | 494 us                                                      | 10.1 ms: 20.41x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (5): bench_thread_pool, sympy_integrate, html5lib, sympy_str, float
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 64.92% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
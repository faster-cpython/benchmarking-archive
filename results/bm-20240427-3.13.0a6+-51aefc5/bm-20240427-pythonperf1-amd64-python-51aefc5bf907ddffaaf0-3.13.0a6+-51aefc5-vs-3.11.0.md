# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-amd64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 5.26 ms                                                     | 4.80 ms: 1.10x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.67 sec: 1.01x slower                                                      |
| html5lib       | 38.9 ms                                                     | 36.5 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 274 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 231 ms: 1.44x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.44x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 224 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 398 ms: 1.33x faster                                                        |
| async_tree_io              | 808 ms                                                      | 612 ms: 1.32x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 631 ms: 1.31x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.38x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 51.6 ms: 1.05x faster                                                       |
| pidigits       | 150 ms                                                      | 148 ms: 1.01x faster                                                        |
| nbody          | 70.3 ms                                                     | 70.9 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 80.0 ms: 1.14x faster                                                       |
| regex_dna      | 116 ms                                                      | 125 ms: 1.08x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.62 ms: 1.08x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.76 ms: 1.41x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 130 us: 1.21x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 180 us: 1.16x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 91.4 ms: 1.07x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.3 ms: 1.02x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                                      |
| xml_etree_process    | 37.2 ms                                                     | 37.8 ms: 1.02x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 55.2 ms: 1.05x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.77 us: 1.07x slower                                                       |
| pickle_dict          | 18.5 us                                                     | 19.8 us: 1.07x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.2 us: 1.09x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.97 us: 1.10x slower                                                       |
| pickle               | 6.64 us                                                     | 7.37 us: 1.11x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.45 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.3 ms: 1.03x slower                                                       |
| python_startup         | 19.8 ms                                                     | 21.0 ms: 1.06x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 33.4 ms: 1.20x faster                                                       |
| mako            | 7.58 ms                                                     | 6.35 ms: 1.19x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 16.0 ms: 1.15x faster                                                       |
| django_template | 24.4 ms                                                     | 23.0 ms: 1.06x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.15x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 108 us: 3.02x faster                                                        |
| generators                 | 34.0 ms                                                     | 21.5 ms: 1.58x faster                                                       |
| pylint                     | 323 ms                                                      | 212 ms: 1.52x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 274 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 231 ms: 1.44x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.44x faster                                                        |
| comprehensions             | 15.6 us                                                     | 11.1 us: 1.41x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.76 ms: 1.41x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 224 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| deltablue                  | 2.70 ms                                                     | 2.00 ms: 1.35x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 53.2 ns: 1.35x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 398 ms: 1.33x faster                                                        |
| async_tree_io              | 808 ms                                                      | 612 ms: 1.32x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 631 ms: 1.31x faster                                                        |
| raytrace                   | 213 ms                                                      | 166 ms: 1.29x faster                                                        |
| chaos                      | 48.4 ms                                                     | 39.0 ms: 1.24x faster                                                       |
| richards_super             | 38.7 ms                                                     | 31.3 ms: 1.24x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 771 us: 1.24x faster                                                        |
| unpickle_pure_python       | 157 us                                                      | 130 us: 1.21x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 33.4 ms: 1.20x faster                                                       |
| mako                       | 7.58 ms                                                     | 6.35 ms: 1.19x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 987 us: 1.18x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 22.1 us: 1.18x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 85.5 ms: 1.17x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 180 us: 1.16x faster                                                        |
| hexiom                     | 4.55 ms                                                     | 3.94 ms: 1.16x faster                                                       |
| go                         | 101 ms                                                      | 87.5 ms: 1.15x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 16.0 ms: 1.15x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.3 ms: 1.15x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.39 sec: 1.15x faster                                                      |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.14x faster                                                       |
| richards                   | 31.4 ms                                                     | 27.6 ms: 1.14x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 80.0 ms: 1.14x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 60.1 ms: 1.14x faster                                                       |
| sympy_str                  | 185 ms                                                      | 164 ms: 1.13x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 12.6 ms: 1.12x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 61.4 ms: 1.11x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.18 us: 1.11x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.84 sec: 1.10x faster                                                      |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.2 ms: 1.10x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.53 us: 1.10x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 993 ms: 1.10x faster                                                        |
| chameleon                  | 5.26 ms                                                     | 4.80 ms: 1.10x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 57.4 ms: 1.09x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 664 ms: 1.09x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.63 us: 1.09x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 487 ms: 1.09x faster                                                        |
| deepcopy                   | 246 us                                                      | 227 us: 1.08x faster                                                        |
| sympy_expand               | 299 ms                                                      | 279 ms: 1.07x faster                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 45.6 ms: 1.07x faster                                                       |
| mypy2                      | 459 ms                                                      | 429 ms: 1.07x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 91.4 ms: 1.07x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 36.5 ms: 1.07x faster                                                       |
| django_template            | 24.4 ms                                                     | 23.0 ms: 1.06x faster                                                       |
| pyflate                    | 312 ms                                                      | 295 ms: 1.06x faster                                                        |
| float                      | 54.4 ms                                                     | 51.6 ms: 1.05x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 181 ms: 1.05x faster                                                        |
| bench_thread_pool          | 872 us                                                      | 836 us: 1.04x faster                                                        |
| meteor_contest             | 75.2 ms                                                     | 72.6 ms: 1.04x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.3 ms: 1.02x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                                      |
| pidigits                   | 150 ms                                                      | 148 ms: 1.01x faster                                                        |
| deepcopy_reduce            | 2.06 us                                                     | 2.04 us: 1.01x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.56 ms: 1.01x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 34.3 ms: 1.01x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 77.8 ms: 1.00x faster                                                       |
| nbody                      | 70.3 ms                                                     | 70.9 ms: 1.01x slower                                                       |
| scimark_fft                | 179 ms                                                      | 181 ms: 1.01x slower                                                        |
| docutils                   | 1.64 sec                                                    | 1.67 sec: 1.01x slower                                                      |
| xml_etree_process          | 37.2 ms                                                     | 37.8 ms: 1.02x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 17.3 ms: 1.03x slower                                                       |
| coverage                   | 43.4 ms                                                     | 45.2 ms: 1.04x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 55.2 ms: 1.05x slower                                                       |
| python_startup             | 19.8 ms                                                     | 21.0 ms: 1.06x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.77 us: 1.07x slower                                                       |
| pickle_dict                | 18.5 us                                                     | 19.8 us: 1.07x slower                                                       |
| regex_dna                  | 116 ms                                                      | 125 ms: 1.08x slower                                                        |
| aiohttp                    | 883 us                                                      | 955 us: 1.08x slower                                                        |
| regex_effbot               | 1.50 ms                                                     | 1.62 ms: 1.08x slower                                                       |
| pycparser                  | 720 ms                                                      | 780 ms: 1.08x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.2 us: 1.09x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.97 us: 1.10x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 69.7 ms: 1.10x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.37 us: 1.11x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.45 us: 1.12x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 81.3 ms: 1.15x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.89 ms: 1.20x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 910 us: 1.28x slower                                                        |
| async_generators           | 177 ms                                                      | 239 ms: 1.35x slower                                                        |
| thrift                     | 494 us                                                      | 8.10 ms: 16.40x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                                |

Benchmark hidden because not significant (4): tornado_http, fannkuch, 2to3, json
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown
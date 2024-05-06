# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 211 ms: 1.01x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.91 ms: 1.07x faster                                                       |
| html5lib       | 38.9 ms                                                     | 36.3 ms: 1.07x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                                       |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 227 ms: 1.46x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 275 ms: 1.45x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 223 ms: 1.38x faster                                                        |
| async_tree_io              | 808 ms                                                      | 592 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 387 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 398 ms: 1.33x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 628 ms: 1.32x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 53.0 ms: 1.03x faster                                                       |
| pidigits       | 150 ms                                                      | 148 ms: 1.02x faster                                                        |
| nbody          | 70.3 ms                                                     | 72.4 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 79.7 ms: 1.14x faster                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.60 ms: 1.07x slower                                                       |
| regex_dna      | 116 ms                                                      | 125 ms: 1.07x slower                                                        |
| regex_v8       | 14.2 ms                                                     | 15.4 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.76 ms: 1.41x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 135 us: 1.16x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 183 us: 1.14x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 92.9 ms: 1.05x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.42 sec: 1.03x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 65.0 ms: 1.01x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.4 us: 1.00x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 38.2 ms: 1.03x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.72 us: 1.05x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 56.2 ms: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.20 us: 1.09x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.54 us: 1.13x slower                                                       |
| pickle_list          | 2.70 us                                                     | 3.22 us: 1.19x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 19.8 ms                                                     | 20.4 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.46 ms: 1.17x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 35.0 ms: 1.14x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 16.5 ms: 1.12x faster                                                       |
| django_template | 24.4 ms                                                     | 22.4 ms: 1.09x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.13x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 74.9 us: 4.35x faster                                                       |
| generators                 | 34.0 ms                                                     | 20.7 ms: 1.64x faster                                                       |
| pylint                     | 323 ms                                                      | 208 ms: 1.55x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 474 ms: 1.53x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 227 ms: 1.46x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 275 ms: 1.45x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.76 ms: 1.41x faster                                                       |
| comprehensions             | 15.6 us                                                     | 11.1 us: 1.40x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 223 ms: 1.38x faster                                                        |
| async_tree_io              | 808 ms                                                      | 592 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 387 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 398 ms: 1.33x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 628 ms: 1.32x faster                                                        |
| deltablue                  | 2.70 ms                                                     | 2.10 ms: 1.28x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 57.4 ns: 1.25x faster                                                       |
| raytrace                   | 213 ms                                                      | 172 ms: 1.24x faster                                                        |
| sqlglot_parse              | 953 us                                                      | 781 us: 1.22x faster                                                        |
| chaos                      | 48.4 ms                                                     | 39.8 ms: 1.22x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.72 sec: 1.18x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 988 us: 1.18x faster                                                        |
| sympy_sum                  | 100 ms                                                      | 85.0 ms: 1.18x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.36 sec: 1.17x faster                                                      |
| mako                       | 7.58 ms                                                     | 6.46 ms: 1.17x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 39.7 ms: 1.17x faster                                                       |
| richards_super             | 38.7 ms                                                     | 33.2 ms: 1.17x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 135 us: 1.16x faster                                                        |
| nqueens                    | 68.3 ms                                                     | 59.2 ms: 1.15x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 79.7 ms: 1.14x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 3.99 ms: 1.14x faster                                                       |
| sympy_str                  | 185 ms                                                      | 162 ms: 1.14x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 35.0 ms: 1.14x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.03 us: 1.14x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 183 us: 1.14x faster                                                        |
| tornado_http               | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 23.1 us: 1.12x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 16.5 ms: 1.12x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.6 ms: 1.12x faster                                                       |
| mypy2                      | 459 ms                                                      | 415 ms: 1.11x faster                                                        |
| logging_format             | 7.16 us                                                     | 6.47 us: 1.11x faster                                                       |
| go                         | 101 ms                                                      | 91.4 ms: 1.11x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.6 ms: 1.10x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 56.9 ms: 1.10x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.61 us: 1.10x faster                                                       |
| django_template            | 24.4 ms                                                     | 22.4 ms: 1.09x faster                                                       |
| deepcopy                   | 246 us                                                      | 226 us: 1.09x faster                                                        |
| sympy_expand               | 299 ms                                                      | 275 ms: 1.09x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 1.01 sec: 1.08x faster                                                      |
| scimark_monte_carlo        | 45.3 ms                                                     | 42.1 ms: 1.08x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 494 ms: 1.07x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 36.3 ms: 1.07x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.91 ms: 1.07x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 178 ms: 1.07x faster                                                        |
| bench_thread_pool          | 872 us                                                      | 815 us: 1.07x faster                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 45.7 ms: 1.07x faster                                                       |
| richards                   | 31.4 ms                                                     | 29.5 ms: 1.07x faster                                                       |
| pyflate                    | 312 ms                                                      | 293 ms: 1.07x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 64.2 ms: 1.06x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 92.9 ms: 1.05x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.42 sec: 1.03x faster                                                      |
| float                      | 54.4 ms                                                     | 53.0 ms: 1.03x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 33.6 ms: 1.03x faster                                                       |
| pidigits                   | 150 ms                                                      | 148 ms: 1.02x faster                                                        |
| deepcopy_reduce            | 2.06 us                                                     | 2.03 us: 1.01x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 74.3 ms: 1.01x faster                                                       |
| 2to3                       | 214 ms                                                      | 211 ms: 1.01x faster                                                        |
| xml_etree_iterparse        | 65.6 ms                                                     | 65.0 ms: 1.01x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 18.4 us: 1.00x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 79.1 ms: 1.01x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 64.3 ms: 1.02x slower                                                       |
| fannkuch                   | 253 ms                                                      | 259 ms: 1.02x slower                                                        |
| xml_etree_process          | 37.2 ms                                                     | 38.2 ms: 1.03x slower                                                       |
| nbody                      | 70.3 ms                                                     | 72.4 ms: 1.03x slower                                                       |
| python_startup             | 19.8 ms                                                     | 20.4 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                       |
| scimark_fft                | 179 ms                                                      | 185 ms: 1.03x slower                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.70 ms: 1.05x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.72 us: 1.05x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                                       |
| coverage                   | 43.4 ms                                                     | 45.8 ms: 1.05x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 75.4 ms: 1.06x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.60 ms: 1.07x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 56.2 ms: 1.07x slower                                                       |
| regex_dna                  | 116 ms                                                      | 125 ms: 1.07x slower                                                        |
| pickle                     | 6.64 us                                                     | 7.20 us: 1.09x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.4 ms: 1.09x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.54 us: 1.13x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.22 us: 1.19x slower                                                       |
| telco                      | 4.06 ms                                                     | 5.00 ms: 1.23x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 901 us: 1.26x slower                                                        |
| async_generators           | 177 ms                                                      | 231 ms: 1.30x slower                                                        |
| thrift                     | 494 us                                                      | 8.13 ms: 16.47x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                                |

Benchmark hidden because not significant (5): json, docutils, python_startup_no_site, aiohttp, pycparser
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown
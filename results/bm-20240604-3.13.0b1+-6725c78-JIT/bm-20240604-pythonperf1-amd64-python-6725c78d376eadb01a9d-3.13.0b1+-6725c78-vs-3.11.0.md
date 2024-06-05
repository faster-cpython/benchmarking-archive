# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: windows-amd64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.08x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 229 ms: 1.07x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.94 ms: 1.07x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.78 sec: 1.08x slower                                                      |
| html5lib       | 38.9 ms                                                     | 37.5 ms: 1.04x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 86.1 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 230 ms: 1.45x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.43x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 216 ms: 1.43x faster                                                        |
| async_tree_io              | 808 ms                                                      | 589 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 625 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 402 ms: 1.32x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 51.1 ms: 1.38x faster                                                       |
| float          | 54.4 ms                                                     | 43.7 ms: 1.24x faster                                                       |
| Geometric mean | (ref)                                                       | 1.20x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 87.7 ms: 1.04x faster                                                       |
| regex_dna      | 116 ms                                                      | 124 ms: 1.07x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.62 ms: 1.08x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| Geometric mean | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.74 ms: 1.41x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 126 us: 1.24x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.22 sec: 1.19x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.5 ms: 1.08x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 90.2 ms: 1.08x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 17.9 us: 1.03x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 51.1 ms: 1.03x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.3 ms: 1.02x faster                                                       |
| pickle_list          | 2.70 us                                                     | 2.81 us: 1.04x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.1 us: 1.08x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.85 us: 1.10x slower                                                       |
| pickle               | 6.64 us                                                     | 7.42 us: 1.12x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.54 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.9 ms: 1.07x slower                                                       |
| python_startup         | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.09x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.02 ms: 1.51x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 17.8 ms: 1.03x faster                                                       |
| django_template | 24.4 ms                                                     | 25.8 ms: 1.05x slower                                                       |
| genshi_xml      | 39.9 ms                                                     | 44.6 ms: 1.12x slower                                                       |
| Geometric mean  | (ref)                                                       | 1.07x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 113 us: 2.89x faster                                                        |
| generators                 | 34.0 ms                                                     | 21.5 ms: 1.58x faster                                                       |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.54x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 44.8 ms: 1.53x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.02 ms: 1.51x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 481 ms: 1.51x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 230 ms: 1.45x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.43x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 216 ms: 1.43x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.74 ms: 1.41x faster                                                       |
| nbody                      | 70.3 ms                                                     | 51.1 ms: 1.38x faster                                                       |
| pylint                     | 323 ms                                                      | 235 ms: 1.37x faster                                                        |
| async_tree_io              | 808 ms                                                      | 589 ms: 1.37x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.49 sec: 1.36x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 625 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 402 ms: 1.32x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 55.3 ns: 1.30x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 20.3 us: 1.28x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.04 ms: 1.26x faster                                                       |
| float                      | 54.4 ms                                                     | 43.7 ms: 1.24x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 126 us: 1.24x faster                                                        |
| chaos                      | 48.4 ms                                                     | 39.1 ms: 1.24x faster                                                       |
| scimark_fft                | 179 ms                                                      | 147 ms: 1.22x faster                                                        |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                        |
| pyflate                    | 312 ms                                                      | 259 ms: 1.21x faster                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 40.8 ms: 1.20x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 37.9 ms: 1.20x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.22 sec: 1.19x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 807 us: 1.18x faster                                                        |
| raytrace                   | 213 ms                                                      | 181 ms: 1.18x faster                                                        |
| logging_simple             | 6.86 us                                                     | 5.82 us: 1.18x faster                                                       |
| fannkuch                   | 253 ms                                                      | 215 ms: 1.18x faster                                                        |
| richards_super             | 38.7 ms                                                     | 33.1 ms: 1.17x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 452 ms: 1.17x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 930 ms: 1.17x faster                                                        |
| deltablue                  | 2.70 ms                                                     | 2.35 ms: 1.15x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.5 ms: 1.14x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.29 us: 1.14x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.14x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.13x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 60.7 ms: 1.13x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1.04 ms: 1.12x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.5 ms: 1.08x faster                                                       |
| go                         | 101 ms                                                      | 93.2 ms: 1.08x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 90.2 ms: 1.08x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.48 sec: 1.08x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 86.1 ms: 1.08x faster                                                       |
| richards                   | 31.4 ms                                                     | 29.4 ms: 1.07x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.94 ms: 1.07x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 94.0 ms: 1.06x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 820 us: 1.06x faster                                                        |
| meteor_contest             | 75.2 ms                                                     | 72.1 ms: 1.04x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 87.7 ms: 1.04x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 37.5 ms: 1.04x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 17.8 ms: 1.03x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 17.9 us: 1.03x faster                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 51.1 ms: 1.03x faster                                                       |
| sympy_str                  | 185 ms                                                      | 180 ms: 1.03x faster                                                        |
| deepcopy                   | 246 us                                                      | 241 us: 1.02x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.3 ms: 1.02x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.04 sec: 1.00x slower                                                      |
| hexiom                     | 4.55 ms                                                     | 4.68 ms: 1.03x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 80.7 ms: 1.03x slower                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.14 us: 1.04x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.81 us: 1.04x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                       |
| coverage                   | 43.4 ms                                                     | 45.7 ms: 1.05x slower                                                       |
| aiohttp                    | 883 us                                                      | 930 us: 1.05x slower                                                        |
| django_template            | 24.4 ms                                                     | 25.8 ms: 1.05x slower                                                       |
| mypy2                      | 459 ms                                                      | 485 ms: 1.06x slower                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 17.9 ms: 1.07x slower                                                       |
| sympy_expand               | 299 ms                                                      | 319 ms: 1.07x slower                                                        |
| regex_dna                  | 116 ms                                                      | 124 ms: 1.07x slower                                                        |
| pathlib                    | 70.9 ms                                                     | 75.7 ms: 1.07x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 37.0 ms: 1.07x slower                                                       |
| 2to3                       | 214 ms                                                      | 229 ms: 1.07x slower                                                        |
| regex_effbot               | 1.50 ms                                                     | 1.62 ms: 1.08x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.78 sec: 1.08x slower                                                      |
| json_loads                 | 13.0 us                                                     | 14.1 us: 1.08x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.85 us: 1.10x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 69.6 ms: 1.10x slower                                                       |
| python_startup             | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.52 ms: 1.11x slower                                                       |
| genshi_xml                 | 39.9 ms                                                     | 44.6 ms: 1.12x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 70.2 ms: 1.12x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.42 us: 1.12x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.54 us: 1.13x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 923 us: 1.29x slower                                                        |
| async_generators           | 177 ms                                                      | 252 ms: 1.42x slower                                                        |
| thrift                     | 494 us                                                      | 9.25 ms: 18.73x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                                |

Benchmark hidden because not significant (4): json, pidigits, sympy_integrate, pycparser
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown
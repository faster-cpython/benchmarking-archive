# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: windows-amd64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 208 ms: 1.03x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| html5lib       | 38.9 ms                                                     | 35.6 ms: 1.09x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 82.3 ms: 1.13x faster                                                       |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 261 ms: 1.55x faster                                                        |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 263 ms: 1.52x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 203 ms: 1.52x faster                                                        |
| async_tree_io              | 808 ms                                                      | 584 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 385 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 611 ms: 1.36x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.45x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 50.2 ms: 1.08x faster                                                       |
| nbody          | 70.3 ms                                                     | 69.4 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 78.2 ms: 1.16x faster                                                       |
| regex_dna      | 116 ms                                                      | 120 ms: 1.03x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.68 ms: 1.42x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 124 us: 1.27x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 178 us: 1.17x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.36 sec: 1.07x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 91.9 ms: 1.06x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.7 ms: 1.05x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.7 us: 1.01x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.5 ms: 1.02x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.92 us: 1.08x slower                                                       |
| pickle               | 6.64 us                                                     | 7.32 us: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.42 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.1 ms: 1.05x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.1 ms: 1.02x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 31.7 ms: 1.26x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 14.7 ms: 1.26x faster                                                       |
| mako            | 7.58 ms                                                     | 6.40 ms: 1.18x faster                                                       |
| django_template | 24.4 ms                                                     | 21.2 ms: 1.15x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.21x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 101 us: 3.24x faster                                                        |
| generators                 | 34.0 ms                                                     | 19.9 ms: 1.70x faster                                                       |
| pylint                     | 323 ms                                                      | 204 ms: 1.59x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 261 ms: 1.55x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 472 ms: 1.54x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.53x faster                                                       |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 263 ms: 1.52x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 203 ms: 1.52x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.68 ms: 1.42x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 1.90 ms: 1.42x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.43 sec: 1.41x faster                                                      |
| async_tree_io              | 808 ms                                                      | 584 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 385 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 611 ms: 1.36x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 53.0 ns: 1.35x faster                                                       |
| raytrace                   | 213 ms                                                      | 161 ms: 1.33x faster                                                        |
| unpickle_pure_python       | 157 us                                                      | 124 us: 1.27x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 31.7 ms: 1.26x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 757 us: 1.26x faster                                                        |
| chaos                      | 48.4 ms                                                     | 38.4 ms: 1.26x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 14.7 ms: 1.26x faster                                                       |
| richards_super             | 38.7 ms                                                     | 31.0 ms: 1.25x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 55.9 ms: 1.22x faster                                                       |
| go                         | 101 ms                                                      | 82.7 ms: 1.22x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 3.75 ms: 1.21x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.31 sec: 1.21x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.70 us: 1.21x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 38.5 ms: 1.20x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 970 us: 1.20x faster                                                        |
| sympy_sum                  | 100 ms                                                      | 84.0 ms: 1.19x faster                                                       |
| mako                       | 7.58 ms                                                     | 6.40 ms: 1.18x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 53.0 ms: 1.18x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.7 ms: 1.18x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 178 us: 1.17x faster                                                        |
| logging_format             | 7.16 us                                                     | 6.13 us: 1.17x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 78.2 ms: 1.16x faster                                                       |
| sympy_str                  | 185 ms                                                      | 159 ms: 1.16x faster                                                        |
| django_template            | 24.4 ms                                                     | 21.2 ms: 1.15x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.2 ms: 1.15x faster                                                       |
| richards                   | 31.4 ms                                                     | 27.5 ms: 1.14x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.9 ms: 1.13x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 22.9 us: 1.13x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 82.3 ms: 1.13x faster                                                       |
| pyflate                    | 312 ms                                                      | 279 ms: 1.12x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 171 ms: 1.11x faster                                                        |
| deepcopy                   | 246 us                                                      | 222 us: 1.11x faster                                                        |
| chameleon                  | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 981 ms: 1.11x faster                                                        |
| mypy2                      | 459 ms                                                      | 415 ms: 1.11x faster                                                        |
| sympy_expand               | 299 ms                                                      | 270 ms: 1.10x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.60 us: 1.10x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 62.1 ms: 1.10x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 481 ms: 1.10x faster                                                        |
| bench_thread_pool          | 872 us                                                      | 798 us: 1.09x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 35.6 ms: 1.09x faster                                                       |
| float                      | 54.4 ms                                                     | 50.2 ms: 1.08x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 45.5 ms: 1.08x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.36 sec: 1.07x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 91.9 ms: 1.06x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 32.7 ms: 1.06x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.45 ms: 1.05x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 74.6 ms: 1.05x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.7 ms: 1.05x faster                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 16.1 ms: 1.05x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.97 us: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 72.0 ms: 1.04x faster                                                       |
| scimark_fft                | 179 ms                                                      | 173 ms: 1.03x faster                                                        |
| 2to3                       | 214 ms                                                      | 208 ms: 1.03x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                       |
| fannkuch                   | 253 ms                                                      | 249 ms: 1.02x faster                                                        |
| docutils                   | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| nbody                      | 70.3 ms                                                     | 69.4 ms: 1.01x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| coverage                   | 43.4 ms                                                     | 43.7 ms: 1.01x slower                                                       |
| pickle_dict                | 18.5 us                                                     | 18.7 us: 1.01x slower                                                       |
| aiohttp                    | 883 us                                                      | 894 us: 1.01x slower                                                        |
| python_startup             | 19.8 ms                                                     | 20.1 ms: 1.02x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 53.5 ms: 1.02x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 65.0 ms: 1.03x slower                                                       |
| regex_dna                  | 116 ms                                                      | 120 ms: 1.03x slower                                                        |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.04x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 74.8 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.92 us: 1.08x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.10x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.32 us: 1.10x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.42 us: 1.11x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.71 ms: 1.16x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 909 us: 1.27x slower                                                        |
| async_generators           | 177 ms                                                      | 228 ms: 1.29x slower                                                        |
| thrift                     | 494 us                                                      | 8.02 ms: 16.24x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (4): json, pidigits, unpickle_list, pycparser
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown
# Results vs. 3.11.0

- fork: faster-cpython
- ref: call_cmethod
- machine: windows-amd64
- commit hash: e985127
- commit date: 2024-04-10
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 212 ms: 1.01x faster                                                          |
| chameleon      | 5.26 ms                                                     | 4.84 ms: 1.09x faster                                                         |
| docutils       | 1.64 sec                                                    | 1.63 sec: 1.01x faster                                                        |
| html5lib       | 38.9 ms                                                     | 35.8 ms: 1.09x faster                                                         |
| tornado_http   | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                                         |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.51x faster                                                          |
| async_tree_none            | 332 ms                                                      | 223 ms: 1.49x faster                                                          |
| async_tree_memoization     | 399 ms                                                      | 269 ms: 1.49x faster                                                          |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.42x faster                                                          |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                          |
| async_tree_io              | 808 ms                                                      | 592 ms: 1.36x faster                                                          |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 389 ms: 1.36x faster                                                          |
| async_tree_io_tg           | 829 ms                                                      | 617 ms: 1.34x faster                                                          |
| Geometric mean             | (ref)                                                       | 1.42x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 52.0 ms: 1.05x faster                                                         |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                          |
| nbody          | 70.3 ms                                                     | 72.2 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 80.0 ms: 1.14x faster                                                         |
| regex_dna      | 116 ms                                                      | 115 ms: 1.01x faster                                                          |
| regex_effbot   | 1.50 ms                                                     | 1.55 ms: 1.03x slower                                                         |
| regex_v8       | 14.2 ms                                                     | 16.2 ms: 1.14x slower                                                         |
| Geometric mean | (ref)                                                       | 1.01x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.72 ms: 1.41x faster                                                         |
| unpickle_pure_python | 157 us                                                      | 132 us: 1.19x faster                                                          |
| pickle_pure_python   | 208 us                                                      | 180 us: 1.16x faster                                                          |
| xml_etree_parse      | 97.6 ms                                                     | 93.2 ms: 1.05x faster                                                         |
| tomli_loads          | 1.46 sec                                                    | 1.42 sec: 1.02x faster                                                        |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.9 ms: 1.01x faster                                                         |
| pickle_dict          | 18.5 us                                                     | 18.6 us: 1.01x slower                                                         |
| xml_etree_process    | 37.2 ms                                                     | 37.8 ms: 1.02x slower                                                         |
| xml_etree_generate   | 52.5 ms                                                     | 54.5 ms: 1.04x slower                                                         |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                         |
| unpickle_list        | 2.59 us                                                     | 2.79 us: 1.08x slower                                                         |
| pickle_list          | 2.70 us                                                     | 2.94 us: 1.09x slower                                                         |
| pickle               | 6.64 us                                                     | 7.36 us: 1.11x slower                                                         |
| unpickle             | 7.57 us                                                     | 8.40 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                                         |
| Geometric mean         | (ref)                                                       | 1.03x slower                                                                  |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 6.39 ms: 1.19x faster                                                         |
| genshi_text    | 18.4 ms                                                     | 16.2 ms: 1.14x faster                                                         |
| genshi_xml     | 39.9 ms                                                     | 35.5 ms: 1.13x faster                                                         |
| Geometric mean | (ref)                                                       | 1.15x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 75.2 us: 4.33x faster                                                         |
| pylint                     | 323 ms                                                      | 187 ms: 1.73x faster                                                          |
| asyncio_tcp                | 726 ms                                                      | 473 ms: 1.54x faster                                                          |
| generators                 | 34.0 ms                                                     | 22.2 ms: 1.53x faster                                                         |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.51x faster                                                          |
| async_tree_none            | 332 ms                                                      | 223 ms: 1.49x faster                                                          |
| async_tree_memoization     | 399 ms                                                      | 269 ms: 1.49x faster                                                          |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.42x faster                                                          |
| json_dumps                 | 8.09 ms                                                     | 5.72 ms: 1.41x faster                                                         |
| comprehensions             | 15.6 us                                                     | 11.2 us: 1.40x faster                                                         |
| deltablue                  | 2.70 ms                                                     | 1.97 ms: 1.37x faster                                                         |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                          |
| async_tree_io              | 808 ms                                                      | 592 ms: 1.36x faster                                                          |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 389 ms: 1.36x faster                                                          |
| async_tree_io_tg           | 829 ms                                                      | 617 ms: 1.34x faster                                                          |
| raytrace                   | 213 ms                                                      | 159 ms: 1.34x faster                                                          |
| logging_silent             | 71.8 ns                                                     | 56.8 ns: 1.26x faster                                                         |
| chaos                      | 48.4 ms                                                     | 39.1 ms: 1.24x faster                                                         |
| sqlglot_parse              | 953 us                                                      | 774 us: 1.23x faster                                                          |
| richards_super             | 38.7 ms                                                     | 31.9 ms: 1.21x faster                                                         |
| mako                       | 7.58 ms                                                     | 6.39 ms: 1.19x faster                                                         |
| unpickle_pure_python       | 157 us                                                      | 132 us: 1.19x faster                                                          |
| hexiom                     | 4.55 ms                                                     | 3.85 ms: 1.18x faster                                                         |
| sqlglot_transpile          | 1.16 ms                                                     | 987 us: 1.18x faster                                                          |
| go                         | 101 ms                                                      | 85.7 ms: 1.18x faster                                                         |
| deepcopy_memo              | 26.0 us                                                     | 22.1 us: 1.18x faster                                                         |
| richards                   | 31.4 ms                                                     | 26.8 ms: 1.17x faster                                                         |
| sympy_sum                  | 100 ms                                                      | 85.6 ms: 1.17x faster                                                         |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.74 sec: 1.17x faster                                                        |
| pickle_pure_python         | 208 us                                                      | 180 us: 1.16x faster                                                          |
| dulwich_log                | 46.4 ms                                                     | 40.3 ms: 1.15x faster                                                         |
| coroutines                 | 15.0 ms                                                     | 13.0 ms: 1.15x faster                                                         |
| regex_compile              | 91.0 ms                                                     | 80.0 ms: 1.14x faster                                                         |
| genshi_text                | 18.4 ms                                                     | 16.2 ms: 1.14x faster                                                         |
| tornado_http               | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                                         |
| logging_simple             | 6.86 us                                                     | 6.06 us: 1.13x faster                                                         |
| sympy_str                  | 185 ms                                                      | 164 ms: 1.13x faster                                                          |
| mdp                        | 1.59 sec                                                    | 1.42 sec: 1.13x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 35.5 ms: 1.13x faster                                                         |
| nqueens                    | 68.3 ms                                                     | 61.7 ms: 1.11x faster                                                         |
| logging_format             | 7.16 us                                                     | 6.47 us: 1.11x faster                                                         |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.0 ms: 1.10x faster                                                         |
| sqlite_synth               | 1.77 us                                                     | 1.60 us: 1.10x faster                                                         |
| sympy_integrate            | 14.0 ms                                                     | 12.8 ms: 1.10x faster                                                         |
| bench_thread_pool          | 872 us                                                      | 794 us: 1.10x faster                                                          |
| deepcopy                   | 246 us                                                      | 225 us: 1.09x faster                                                          |
| pprint_pformat             | 1.09 sec                                                    | 997 ms: 1.09x faster                                                          |
| mypy2                      | 459 ms                                                      | 421 ms: 1.09x faster                                                          |
| scimark_lu                 | 62.8 ms                                                     | 57.7 ms: 1.09x faster                                                         |
| chameleon                  | 5.26 ms                                                     | 4.84 ms: 1.09x faster                                                         |
| html5lib                   | 38.9 ms                                                     | 35.8 ms: 1.09x faster                                                         |
| pyflate                    | 312 ms                                                      | 289 ms: 1.08x faster                                                          |
| sympy_expand               | 299 ms                                                      | 278 ms: 1.08x faster                                                          |
| pprint_safe_repr           | 529 ms                                                      | 493 ms: 1.07x faster                                                          |
| crypto_pyaes               | 48.9 ms                                                     | 46.1 ms: 1.06x faster                                                         |
| spectral_norm              | 68.3 ms                                                     | 65.0 ms: 1.05x faster                                                         |
| xml_etree_parse            | 97.6 ms                                                     | 93.2 ms: 1.05x faster                                                         |
| float                      | 54.4 ms                                                     | 52.0 ms: 1.05x faster                                                         |
| sqlglot_normalize          | 190 ms                                                      | 184 ms: 1.03x faster                                                          |
| tomli_loads                | 1.46 sec                                                    | 1.42 sec: 1.02x faster                                                        |
| meteor_contest             | 75.2 ms                                                     | 73.5 ms: 1.02x faster                                                         |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                          |
| regex_dna                  | 116 ms                                                      | 115 ms: 1.01x faster                                                          |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.9 ms: 1.01x faster                                                         |
| docutils                   | 1.64 sec                                                    | 1.63 sec: 1.01x faster                                                        |
| 2to3                       | 214 ms                                                      | 212 ms: 1.01x faster                                                          |
| pickle_dict                | 18.5 us                                                     | 18.6 us: 1.01x slower                                                         |
| scimark_sor                | 78.1 ms                                                     | 78.7 ms: 1.01x slower                                                         |
| aiohttp                    | 883 us                                                      | 890 us: 1.01x slower                                                          |
| sqlglot_optimize           | 34.5 ms                                                     | 34.8 ms: 1.01x slower                                                         |
| bench_mp_pool              | 63.2 ms                                                     | 63.8 ms: 1.01x slower                                                         |
| xml_etree_process          | 37.2 ms                                                     | 37.8 ms: 1.02x slower                                                         |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.62 ms: 1.02x slower                                                         |
| nbody                      | 70.3 ms                                                     | 72.2 ms: 1.03x slower                                                         |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                         |
| regex_effbot               | 1.50 ms                                                     | 1.55 ms: 1.03x slower                                                         |
| scimark_fft                | 179 ms                                                      | 186 ms: 1.04x slower                                                          |
| xml_etree_generate         | 52.5 ms                                                     | 54.5 ms: 1.04x slower                                                         |
| python_startup_no_site     | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                                         |
| pathlib                    | 70.9 ms                                                     | 75.3 ms: 1.06x slower                                                         |
| coverage                   | 43.4 ms                                                     | 46.4 ms: 1.07x slower                                                         |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                         |
| unpickle_list              | 2.59 us                                                     | 2.79 us: 1.08x slower                                                         |
| pickle_list                | 2.70 us                                                     | 2.94 us: 1.09x slower                                                         |
| pickle                     | 6.64 us                                                     | 7.36 us: 1.11x slower                                                         |
| unpickle                   | 7.57 us                                                     | 8.40 us: 1.11x slower                                                         |
| regex_v8                   | 14.2 ms                                                     | 16.2 ms: 1.14x slower                                                         |
| create_gc_cycles           | 713 us                                                      | 881 us: 1.24x slower                                                          |
| telco                      | 4.06 ms                                                     | 5.02 ms: 1.24x slower                                                         |
| async_generators           | 177 ms                                                      | 231 ms: 1.31x slower                                                          |
| thrift                     | 494 us                                                      | 8.07 ms: 16.35x slower                                                        |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                                  |

Benchmark hidden because not significant (5): json, deepcopy_reduce, fannkuch, python_startup, pycparser
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown
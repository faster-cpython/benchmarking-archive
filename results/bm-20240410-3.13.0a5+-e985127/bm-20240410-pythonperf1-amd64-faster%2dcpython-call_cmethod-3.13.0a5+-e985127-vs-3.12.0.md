# Results vs. 3.12.0

- fork: faster-cpython
- ref: call_cmethod
- machine: windows-amd64
- commit hash: e985127
- commit date: 2024-04-10
- overall geometric mean: 1.05x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 212 ms: 1.03x faster                                                          |
| chameleon      | 4.98 ms                                                     | 4.84 ms: 1.03x faster                                                         |
| docutils       | 1.66 sec                                                    | 1.63 sec: 1.02x faster                                                        |
| tornado_http   | 89.5 ms                                                     | 81.8 ms: 1.09x faster                                                         |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.37x faster                                                          |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                          |
| async_tree_none_tg         | 285 ms                                                      | 218 ms: 1.31x faster                                                          |
| async_tree_none            | 291 ms                                                      | 223 ms: 1.31x faster                                                          |
| async_tree_memoization     | 339 ms                                                      | 269 ms: 1.26x faster                                                          |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 389 ms: 1.26x faster                                                          |
| async_tree_io_tg           | 771 ms                                                      | 617 ms: 1.25x faster                                                          |
| async_tree_io              | 731 ms                                                      | 592 ms: 1.24x faster                                                          |
| Geometric mean             | (ref)                                                       | 1.29x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 52.0 ms: 1.09x faster                                                         |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                          |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                  |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 115 ms: 1.10x faster                                                          |
| regex_compile  | 87.5 ms                                                     | 80.0 ms: 1.09x faster                                                         |
| regex_effbot   | 1.62 ms                                                     | 1.55 ms: 1.05x faster                                                         |
| regex_v8       | 14.2 ms                                                     | 16.2 ms: 1.14x slower                                                         |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 180 us: 1.09x faster                                                          |
| xml_etree_generate   | 55.8 ms                                                     | 54.5 ms: 1.02x faster                                                         |
| pickle               | 7.43 us                                                     | 7.36 us: 1.01x faster                                                         |
| unpickle_pure_python | 133 us                                                      | 132 us: 1.01x faster                                                          |
| pickle_dict          | 18.4 us                                                     | 18.6 us: 1.01x slower                                                         |
| unpickle_list        | 2.75 us                                                     | 2.79 us: 1.01x slower                                                         |
| unpickle             | 8.18 us                                                     | 8.40 us: 1.03x slower                                                         |
| tomli_loads          | 1.37 sec                                                    | 1.42 sec: 1.04x slower                                                        |
| pickle_list          | 2.83 us                                                     | 2.94 us: 1.04x slower                                                         |
| Geometric mean       | (ref)                                                       | 1.00x slower                                                                  |

Benchmark hidden because not significant (5): xml_etree_iterparse, json_loads, xml_etree_parse, xml_etree_process, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 19.9 ms: 1.02x slower                                                         |
| python_startup_no_site | 16.2 ms                                                     | 17.8 ms: 1.10x slower                                                         |
| Geometric mean         | (ref)                                                       | 1.06x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|-----------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 6.39 ms: 1.11x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 267 ms: 1.37x faster                                                          |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                          |
| async_tree_none_tg         | 285 ms                                                      | 218 ms: 1.31x faster                                                          |
| async_tree_none            | 291 ms                                                      | 223 ms: 1.31x faster                                                          |
| typing_runtime_protocols   | 95.1 us                                                     | 75.2 us: 1.27x faster                                                         |
| comprehensions             | 14.1 us                                                     | 11.2 us: 1.26x faster                                                         |
| async_tree_memoization     | 339 ms                                                      | 269 ms: 1.26x faster                                                          |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 389 ms: 1.26x faster                                                          |
| async_tree_io_tg           | 771 ms                                                      | 617 ms: 1.25x faster                                                          |
| async_tree_io              | 731 ms                                                      | 592 ms: 1.24x faster                                                          |
| mypy2                      | 509 ms                                                      | 421 ms: 1.21x faster                                                          |
| raytrace                   | 192 ms                                                      | 159 ms: 1.21x faster                                                          |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.74 sec: 1.20x faster                                                        |
| mako                       | 7.09 ms                                                     | 6.39 ms: 1.11x faster                                                         |
| chaos                      | 43.3 ms                                                     | 39.1 ms: 1.11x faster                                                         |
| regex_dna                  | 126 ms                                                      | 115 ms: 1.10x faster                                                          |
| sqlite_synth               | 1.76 us                                                     | 1.60 us: 1.10x faster                                                         |
| dulwich_log                | 44.3 ms                                                     | 40.3 ms: 1.10x faster                                                         |
| deltablue                  | 2.16 ms                                                     | 1.97 ms: 1.10x faster                                                         |
| tornado_http               | 89.5 ms                                                     | 81.8 ms: 1.09x faster                                                         |
| regex_compile              | 87.5 ms                                                     | 80.0 ms: 1.09x faster                                                         |
| coroutines                 | 14.3 ms                                                     | 13.0 ms: 1.09x faster                                                         |
| float                      | 56.8 ms                                                     | 52.0 ms: 1.09x faster                                                         |
| pickle_pure_python         | 195 us                                                      | 180 us: 1.09x faster                                                          |
| bench_mp_pool              | 69.2 ms                                                     | 63.8 ms: 1.08x faster                                                         |
| bench_thread_pool          | 857 us                                                      | 794 us: 1.08x faster                                                          |
| deepcopy_memo              | 23.7 us                                                     | 22.1 us: 1.07x faster                                                         |
| sympy_sum                  | 91.5 ms                                                     | 85.6 ms: 1.07x faster                                                         |
| go                         | 91.6 ms                                                     | 85.7 ms: 1.07x faster                                                         |
| pathlib                    | 80.5 ms                                                     | 75.3 ms: 1.07x faster                                                         |
| sympy_str                  | 175 ms                                                      | 164 ms: 1.07x faster                                                          |
| scimark_monte_carlo        | 43.7 ms                                                     | 41.0 ms: 1.07x faster                                                         |
| hexiom                     | 4.10 ms                                                     | 3.85 ms: 1.07x faster                                                         |
| logging_silent             | 60.5 ns                                                     | 56.8 ns: 1.06x faster                                                         |
| richards                   | 28.4 ms                                                     | 26.8 ms: 1.06x faster                                                         |
| deepcopy                   | 238 us                                                      | 225 us: 1.06x faster                                                          |
| crypto_pyaes               | 48.5 ms                                                     | 46.1 ms: 1.05x faster                                                         |
| pprint_pformat             | 1.05 sec                                                    | 997 ms: 1.05x faster                                                          |
| regex_effbot               | 1.62 ms                                                     | 1.55 ms: 1.05x faster                                                         |
| pprint_safe_repr           | 513 ms                                                      | 493 ms: 1.04x faster                                                          |
| sqlglot_parse              | 804 us                                                      | 774 us: 1.04x faster                                                          |
| logging_format             | 6.72 us                                                     | 6.47 us: 1.04x faster                                                         |
| sqlglot_transpile          | 1.02 ms                                                     | 987 us: 1.04x faster                                                          |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                          |
| async_generators           | 239 ms                                                      | 231 ms: 1.04x faster                                                          |
| logging_simple             | 6.28 us                                                     | 6.06 us: 1.03x faster                                                         |
| json                       | 3.05 ms                                                     | 2.95 ms: 1.03x faster                                                         |
| asyncio_tcp                | 487 ms                                                      | 473 ms: 1.03x faster                                                          |
| spectral_norm              | 66.9 ms                                                     | 65.0 ms: 1.03x faster                                                         |
| chameleon                  | 4.98 ms                                                     | 4.84 ms: 1.03x faster                                                         |
| 2to3                       | 218 ms                                                      | 212 ms: 1.03x faster                                                          |
| xml_etree_generate         | 55.8 ms                                                     | 54.5 ms: 1.02x faster                                                         |
| sympy_expand               | 284 ms                                                      | 278 ms: 1.02x faster                                                          |
| deepcopy_reduce            | 2.09 us                                                     | 2.05 us: 1.02x faster                                                         |
| docutils                   | 1.66 sec                                                    | 1.63 sec: 1.02x faster                                                        |
| scimark_lu                 | 58.9 ms                                                     | 57.7 ms: 1.02x faster                                                         |
| pyflate                    | 295 ms                                                      | 289 ms: 1.02x faster                                                          |
| nqueens                    | 62.8 ms                                                     | 61.7 ms: 1.02x faster                                                         |
| generators                 | 22.5 ms                                                     | 22.2 ms: 1.02x faster                                                         |
| meteor_contest             | 74.6 ms                                                     | 73.5 ms: 1.01x faster                                                         |
| sympy_integrate            | 13.0 ms                                                     | 12.8 ms: 1.01x faster                                                         |
| sqlglot_normalize          | 187 ms                                                      | 184 ms: 1.01x faster                                                          |
| pickle                     | 7.43 us                                                     | 7.36 us: 1.01x faster                                                         |
| unpickle_pure_python       | 133 us                                                      | 132 us: 1.01x faster                                                          |
| richards_super             | 32.1 ms                                                     | 31.9 ms: 1.01x faster                                                         |
| scimark_fft                | 184 ms                                                      | 186 ms: 1.01x slower                                                          |
| sqlglot_optimize           | 34.5 ms                                                     | 34.8 ms: 1.01x slower                                                         |
| pickle_dict                | 18.4 us                                                     | 18.6 us: 1.01x slower                                                         |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                         |
| unpickle_list              | 2.75 us                                                     | 2.79 us: 1.01x slower                                                         |
| python_startup             | 19.5 ms                                                     | 19.9 ms: 1.02x slower                                                         |
| fannkuch                   | 247 ms                                                      | 252 ms: 1.02x slower                                                          |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.62 ms: 1.03x slower                                                         |
| unpickle                   | 8.18 us                                                     | 8.40 us: 1.03x slower                                                         |
| mdp                        | 1.37 sec                                                    | 1.42 sec: 1.03x slower                                                        |
| tomli_loads                | 1.37 sec                                                    | 1.42 sec: 1.04x slower                                                        |
| pickle_list                | 2.83 us                                                     | 2.94 us: 1.04x slower                                                         |
| python_startup_no_site     | 16.2 ms                                                     | 17.8 ms: 1.10x slower                                                         |
| regex_v8                   | 14.2 ms                                                     | 16.2 ms: 1.14x slower                                                         |
| coverage                   | 40.8 ms                                                     | 46.4 ms: 1.14x slower                                                         |
| create_gc_cycles           | 752 us                                                      | 881 us: 1.17x slower                                                          |
| telco                      | 4.13 ms                                                     | 5.02 ms: 1.22x slower                                                         |
| Geometric mean             | (ref)                                                       | 1.05x faster                                                                  |

Benchmark hidden because not significant (9): xml_etree_iterparse, scimark_sor, json_loads, xml_etree_parse, xml_etree_process, nbody, json_dumps, aiohttp, pycparser
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240410-3.13.0a5+-e985127/bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown
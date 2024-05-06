# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-amd64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.03x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| chameleon      | 4.98 ms                                                     | 5.05 ms: 1.01x slower                                                        |
| tornado_http   | 89.5 ms                                                     | 90.9 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                 |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 280 ms: 1.31x faster                                                         |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 386 ms: 1.30x faster                                                         |
| async_tree_none_tg         | 285 ms                                                      | 224 ms: 1.27x faster                                                         |
| async_tree_none            | 291 ms                                                      | 233 ms: 1.25x faster                                                         |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 402 ms: 1.22x faster                                                         |
| async_tree_io_tg           | 771 ms                                                      | 635 ms: 1.21x faster                                                         |
| async_tree_memoization     | 339 ms                                                      | 282 ms: 1.20x faster                                                         |
| async_tree_io              | 731 ms                                                      | 612 ms: 1.20x faster                                                         |
| Geometric mean             | (ref)                                                       | 1.24x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 51.5 ms: 1.10x faster                                                        |
| pidigits       | 152 ms                                                      | 149 ms: 1.02x faster                                                         |
| nbody          | 71.9 ms                                                     | 72.9 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 114 ms: 1.11x faster                                                         |
| regex_compile  | 87.5 ms                                                     | 79.4 ms: 1.10x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                        |
| regex_v8       | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python | 195 us                                                      | 176 us: 1.11x faster                                                         |
| pickle             | 7.43 us                                                     | 7.27 us: 1.02x faster                                                        |
| json_loads         | 13.9 us                                                     | 13.7 us: 1.02x faster                                                        |
| xml_etree_generate | 55.8 ms                                                     | 55.2 ms: 1.01x faster                                                        |
| xml_etree_parse    | 93.0 ms                                                     | 92.3 ms: 1.01x faster                                                        |
| unpickle_list      | 2.75 us                                                     | 2.78 us: 1.01x slower                                                        |
| json_dumps         | 5.70 ms                                                     | 5.83 ms: 1.02x slower                                                        |
| unpickle           | 8.18 us                                                     | 8.57 us: 1.05x slower                                                        |
| tomli_loads        | 1.37 sec                                                    | 1.45 sec: 1.06x slower                                                       |
| pickle_list        | 2.83 us                                                     | 3.11 us: 1.10x slower                                                        |
| Geometric mean     | (ref)                                                       | 1.00x slower                                                                 |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle_pure_python, xml_etree_process, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 16.7 ms: 1.03x slower                                                        |
| python_startup         | 19.5 ms                                                     | 20.6 ms: 1.06x slower                                                        |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 6.37 ms: 1.11x faster                                                        |
| django_template | 22.9 ms                                                     | 22.4 ms: 1.02x faster                                                        |
| Geometric mean  | (ref)                                                       | 1.07x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| comprehensions             | 14.1 us                                                     | 10.7 us: 1.31x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 280 ms: 1.31x faster                                                         |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 386 ms: 1.30x faster                                                         |
| async_tree_none_tg         | 285 ms                                                      | 224 ms: 1.27x faster                                                         |
| async_tree_none            | 291 ms                                                      | 233 ms: 1.25x faster                                                         |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 402 ms: 1.22x faster                                                         |
| async_tree_io_tg           | 771 ms                                                      | 635 ms: 1.21x faster                                                         |
| async_tree_memoization     | 339 ms                                                      | 282 ms: 1.20x faster                                                         |
| async_tree_io              | 731 ms                                                      | 612 ms: 1.20x faster                                                         |
| mypy2                      | 509 ms                                                      | 428 ms: 1.19x faster                                                         |
| raytrace                   | 192 ms                                                      | 166 ms: 1.16x faster                                                         |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.84 sec: 1.14x faster                                                       |
| mako                       | 7.09 ms                                                     | 6.37 ms: 1.11x faster                                                        |
| dulwich_log                | 44.3 ms                                                     | 39.9 ms: 1.11x faster                                                        |
| pickle_pure_python         | 195 us                                                      | 176 us: 1.11x faster                                                         |
| chaos                      | 43.3 ms                                                     | 39.1 ms: 1.11x faster                                                        |
| regex_dna                  | 126 ms                                                      | 114 ms: 1.11x faster                                                         |
| float                      | 56.8 ms                                                     | 51.5 ms: 1.10x faster                                                        |
| logging_silent             | 60.5 ns                                                     | 54.9 ns: 1.10x faster                                                        |
| regex_compile              | 87.5 ms                                                     | 79.4 ms: 1.10x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.1 ms: 1.08x faster                                                        |
| sympy_str                  | 175 ms                                                      | 162 ms: 1.08x faster                                                         |
| deepcopy                   | 238 us                                                      | 221 us: 1.08x faster                                                         |
| sympy_sum                  | 91.5 ms                                                     | 85.7 ms: 1.07x faster                                                        |
| crypto_pyaes               | 48.5 ms                                                     | 45.4 ms: 1.07x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.67 us: 1.06x faster                                                        |
| hexiom                     | 4.10 ms                                                     | 3.88 ms: 1.06x faster                                                        |
| deltablue                  | 2.16 ms                                                     | 2.05 ms: 1.06x faster                                                        |
| bench_mp_pool              | 69.2 ms                                                     | 65.6 ms: 1.06x faster                                                        |
| pprint_pformat             | 1.05 sec                                                    | 999 ms: 1.05x faster                                                         |
| pprint_safe_repr           | 513 ms                                                      | 492 ms: 1.04x faster                                                         |
| deepcopy_memo              | 23.7 us                                                     | 22.9 us: 1.04x faster                                                        |
| logging_simple             | 6.28 us                                                     | 6.05 us: 1.04x faster                                                        |
| sympy_integrate            | 13.0 ms                                                     | 12.5 ms: 1.04x faster                                                        |
| sympy_expand               | 284 ms                                                      | 274 ms: 1.04x faster                                                         |
| nqueens                    | 62.8 ms                                                     | 60.6 ms: 1.04x faster                                                        |
| sqlglot_normalize          | 187 ms                                                      | 181 ms: 1.03x faster                                                         |
| regex_effbot               | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                        |
| sqlglot_parse              | 804 us                                                      | 781 us: 1.03x faster                                                         |
| sqlglot_transpile          | 1.02 ms                                                     | 994 us: 1.03x faster                                                         |
| logging_format             | 6.72 us                                                     | 6.53 us: 1.03x faster                                                        |
| django_template            | 22.9 ms                                                     | 22.4 ms: 1.02x faster                                                        |
| pidigits                   | 152 ms                                                      | 149 ms: 1.02x faster                                                         |
| pickle                     | 7.43 us                                                     | 7.27 us: 1.02x faster                                                        |
| pyflate                    | 295 ms                                                      | 288 ms: 1.02x faster                                                         |
| spectral_norm              | 66.9 ms                                                     | 65.5 ms: 1.02x faster                                                        |
| scimark_monte_carlo        | 43.7 ms                                                     | 42.8 ms: 1.02x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 2.05 us: 1.02x faster                                                        |
| json_loads                 | 13.9 us                                                     | 13.7 us: 1.02x faster                                                        |
| scimark_sor                | 78.8 ms                                                     | 77.7 ms: 1.01x faster                                                        |
| scimark_lu                 | 58.9 ms                                                     | 58.1 ms: 1.01x faster                                                        |
| xml_etree_generate         | 55.8 ms                                                     | 55.2 ms: 1.01x faster                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 34.2 ms: 1.01x faster                                                        |
| go                         | 91.6 ms                                                     | 90.7 ms: 1.01x faster                                                        |
| generators                 | 22.5 ms                                                     | 22.3 ms: 1.01x faster                                                        |
| xml_etree_parse            | 93.0 ms                                                     | 92.3 ms: 1.01x faster                                                        |
| richards_super             | 32.1 ms                                                     | 32.4 ms: 1.01x slower                                                        |
| async_generators           | 239 ms                                                      | 242 ms: 1.01x slower                                                         |
| unpickle_list              | 2.75 us                                                     | 2.78 us: 1.01x slower                                                        |
| richards                   | 28.4 ms                                                     | 28.7 ms: 1.01x slower                                                        |
| nbody                      | 71.9 ms                                                     | 72.9 ms: 1.01x slower                                                        |
| chameleon                  | 4.98 ms                                                     | 5.05 ms: 1.01x slower                                                        |
| tornado_http               | 89.5 ms                                                     | 90.9 ms: 1.02x slower                                                        |
| pathlib                    | 80.5 ms                                                     | 82.3 ms: 1.02x slower                                                        |
| json_dumps                 | 5.70 ms                                                     | 5.83 ms: 1.02x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                        |
| gc_traversal               | 1.52 ms                                                     | 1.56 ms: 1.03x slower                                                        |
| python_startup_no_site     | 16.2 ms                                                     | 16.7 ms: 1.03x slower                                                        |
| mdp                        | 1.37 sec                                                    | 1.43 sec: 1.04x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.57 us: 1.05x slower                                                        |
| fannkuch                   | 247 ms                                                      | 259 ms: 1.05x slower                                                         |
| aiohttp                    | 884 us                                                      | 933 us: 1.06x slower                                                         |
| tomli_loads                | 1.37 sec                                                    | 1.45 sec: 1.06x slower                                                       |
| python_startup             | 19.5 ms                                                     | 20.6 ms: 1.06x slower                                                        |
| pycparser                  | 699 ms                                                      | 740 ms: 1.06x slower                                                         |
| scimark_fft                | 184 ms                                                      | 197 ms: 1.07x slower                                                         |
| pickle_list                | 2.83 us                                                     | 3.11 us: 1.10x slower                                                        |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.88 ms: 1.13x slower                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 109 us: 1.14x slower                                                         |
| telco                      | 4.13 ms                                                     | 4.83 ms: 1.17x slower                                                        |
| create_gc_cycles           | 752 us                                                      | 901 us: 1.20x slower                                                         |
| coverage                   | 40.8 ms                                                     | 50.6 ms: 1.24x slower                                                        |
| asyncio_tcp                | 487 ms                                                      | 664 ms: 1.36x slower                                                         |
| Geometric mean             | (ref)                                                       | 1.03x faster                                                                 |

Benchmark hidden because not significant (9): bench_thread_pool, xml_etree_iterparse, docutils, 2to3, unpickle_pure_python, xml_etree_process, json, pickle_dict, meteor_contest
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
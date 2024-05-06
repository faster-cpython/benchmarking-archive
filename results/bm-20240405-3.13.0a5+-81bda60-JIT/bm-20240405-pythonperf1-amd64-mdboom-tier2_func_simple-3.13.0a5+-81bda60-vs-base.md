# Results vs. base

- fork: mdboom
- ref: tier2_func_simple
- machine: windows-amd64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.00x faster
- HPT reliability: 77.64%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 220 ms                                                                      | 219 ms: 1.01x faster                                                     |
| docutils       | 1.70 sec                                                                    | 1.68 sec: 1.01x faster                                                   |
| html5lib       | 35.3 ms                                                                     | 35.7 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                             |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg | 603 ms                                                                      | 612 ms: 1.02x slower                                                     |
| Geometric mean   | (ref)                                                                       | 1.01x slower                                                             |

Benchmark hidden because not significant (7): async_tree_memoization_tg, async_tree_none_tg, async_tree_io, async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 57.9 ms                                                                     | 56.9 ms: 1.02x faster                                                    |
| pidigits       | 146 ms                                                                      | 147 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 15.1 ms                                                                     | 14.1 ms: 1.07x faster                                                    |
| regex_effbot   | 1.62 ms                                                                     | 1.56 ms: 1.04x faster                                                    |
| regex_dna      | 121 ms                                                                      | 118 ms: 1.03x faster                                                     |
| regex_compile  | 86.3 ms                                                                     | 87.0 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_list        | 2.88 us                                                                     | 2.74 us: 1.05x faster                                                    |
| pickle               | 7.36 us                                                                     | 7.16 us: 1.03x faster                                                    |
| tomli_loads          | 1.19 sec                                                                    | 1.18 sec: 1.01x faster                                                   |
| json_dumps           | 5.56 ms                                                                     | 5.51 ms: 1.01x faster                                                    |
| pickle_dict          | 18.5 us                                                                     | 18.6 us: 1.00x slower                                                    |
| xml_etree_process    | 36.3 ms                                                                     | 36.5 ms: 1.01x slower                                                    |
| unpickle_pure_python | 127 us                                                                      | 129 us: 1.02x slower                                                     |
| pickle_pure_python   | 171 us                                                                      | 174 us: 1.02x slower                                                     |
| xml_etree_iterparse  | 61.2 ms                                                                     | 62.6 ms: 1.02x slower                                                    |
| xml_etree_parse      | 90.3 ms                                                                     | 92.9 ms: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                                       | 1.00x faster                                                             |

Benchmark hidden because not significant (4): unpickle, json_loads, xml_etree_generate, pickle_list

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml     | 34.6 ms                                                                     | 33.2 ms: 1.04x faster                                                    |
| genshi_text    | 15.2 ms                                                                     | 15.3 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-pythonperf1-amd64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|--------------------------|:---------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8                 | 15.1 ms                                                                     | 14.1 ms: 1.07x faster                                                    |
| unpickle_list            | 2.88 us                                                                     | 2.74 us: 1.05x faster                                                    |
| genshi_xml               | 34.6 ms                                                                     | 33.2 ms: 1.04x faster                                                    |
| regex_effbot             | 1.62 ms                                                                     | 1.56 ms: 1.04x faster                                                    |
| asyncio_tcp              | 485 ms                                                                      | 470 ms: 1.03x faster                                                     |
| pickle                   | 7.36 us                                                                     | 7.16 us: 1.03x faster                                                    |
| generators               | 20.4 ms                                                                     | 19.8 ms: 1.03x faster                                                    |
| nqueens                  | 61.8 ms                                                                     | 60.1 ms: 1.03x faster                                                    |
| regex_dna                | 121 ms                                                                      | 118 ms: 1.03x faster                                                     |
| sqlglot_normalize        | 184 ms                                                                      | 180 ms: 1.02x faster                                                     |
| typing_runtime_protocols | 72.0 us                                                                     | 70.7 us: 1.02x faster                                                    |
| nbody                    | 57.9 ms                                                                     | 56.9 ms: 1.02x faster                                                    |
| meteor_contest           | 73.2 ms                                                                     | 72.1 ms: 1.02x faster                                                    |
| tomli_loads              | 1.19 sec                                                                    | 1.18 sec: 1.01x faster                                                   |
| sqlglot_optimize         | 35.3 ms                                                                     | 34.8 ms: 1.01x faster                                                    |
| docutils                 | 1.70 sec                                                                    | 1.68 sec: 1.01x faster                                                   |
| thrift                   | 8.89 ms                                                                     | 8.79 ms: 1.01x faster                                                    |
| hexiom                   | 4.46 ms                                                                     | 4.42 ms: 1.01x faster                                                    |
| json_dumps               | 5.56 ms                                                                     | 5.51 ms: 1.01x faster                                                    |
| json                     | 2.89 ms                                                                     | 2.87 ms: 1.01x faster                                                    |
| async_generators         | 235 ms                                                                      | 233 ms: 1.01x faster                                                     |
| scimark_sparse_mat_mult  | 2.24 ms                                                                     | 2.23 ms: 1.01x faster                                                    |
| dulwich_log              | 41.2 ms                                                                     | 41.0 ms: 1.01x faster                                                    |
| telco                    | 4.78 ms                                                                     | 4.75 ms: 1.01x faster                                                    |
| 2to3                     | 220 ms                                                                      | 219 ms: 1.01x faster                                                     |
| pprint_pformat           | 963 ms                                                                      | 958 ms: 1.01x faster                                                     |
| scimark_monte_carlo      | 38.3 ms                                                                     | 38.2 ms: 1.00x faster                                                    |
| crypto_pyaes             | 44.3 ms                                                                     | 44.1 ms: 1.00x faster                                                    |
| sympy_expand             | 282 ms                                                                      | 283 ms: 1.00x slower                                                     |
| pickle_dict              | 18.5 us                                                                     | 18.6 us: 1.00x slower                                                    |
| scimark_sor              | 82.4 ms                                                                     | 82.8 ms: 1.00x slower                                                    |
| mypy2                    | 447 ms                                                                      | 449 ms: 1.00x slower                                                     |
| go                       | 91.6 ms                                                                     | 92.1 ms: 1.00x slower                                                    |
| pidigits                 | 146 ms                                                                      | 147 ms: 1.01x slower                                                     |
| xml_etree_process        | 36.3 ms                                                                     | 36.5 ms: 1.01x slower                                                    |
| sqlite_synth             | 1.56 us                                                                     | 1.57 us: 1.01x slower                                                    |
| fannkuch                 | 226 ms                                                                      | 228 ms: 1.01x slower                                                     |
| regex_compile            | 86.3 ms                                                                     | 87.0 ms: 1.01x slower                                                    |
| pathlib                  | 77.3 ms                                                                     | 78.0 ms: 1.01x slower                                                    |
| deltablue                | 2.14 ms                                                                     | 2.16 ms: 1.01x slower                                                    |
| sqlglot_transpile        | 989 us                                                                      | 998 us: 1.01x slower                                                     |
| genshi_text              | 15.2 ms                                                                     | 15.3 ms: 1.01x slower                                                    |
| deepcopy_memo            | 20.8 us                                                                     | 21.0 us: 1.01x slower                                                    |
| html5lib                 | 35.3 ms                                                                     | 35.7 ms: 1.01x slower                                                    |
| sqlglot_parse            | 773 us                                                                      | 781 us: 1.01x slower                                                     |
| pyflate                  | 269 ms                                                                      | 272 ms: 1.01x slower                                                     |
| deepcopy_reduce          | 1.95 us                                                                     | 1.98 us: 1.01x slower                                                    |
| sympy_sum                | 88.1 ms                                                                     | 89.2 ms: 1.01x slower                                                    |
| spectral_norm            | 50.7 ms                                                                     | 51.4 ms: 1.01x slower                                                    |
| scimark_fft              | 165 ms                                                                      | 167 ms: 1.01x slower                                                     |
| async_tree_io_tg         | 603 ms                                                                      | 612 ms: 1.02x slower                                                     |
| unpickle_pure_python     | 127 us                                                                      | 129 us: 1.02x slower                                                     |
| pickle_pure_python       | 171 us                                                                      | 174 us: 1.02x slower                                                     |
| xml_etree_iterparse      | 61.2 ms                                                                     | 62.6 ms: 1.02x slower                                                    |
| mdp                      | 1.43 sec                                                                    | 1.46 sec: 1.02x slower                                                   |
| coverage                 | 46.4 ms                                                                     | 47.5 ms: 1.02x slower                                                    |
| xml_etree_parse          | 90.3 ms                                                                     | 92.9 ms: 1.03x slower                                                    |
| scimark_lu               | 69.0 ms                                                                     | 71.4 ms: 1.04x slower                                                    |
| richards_super           | 29.9 ms                                                                     | 31.1 ms: 1.04x slower                                                    |
| richards                 | 26.4 ms                                                                     | 27.7 ms: 1.05x slower                                                    |
| Geometric mean           | (ref)                                                                       | 1.00x faster                                                             |

Benchmark hidden because not significant (36): asyncio_tcp_ssl, logging_silent, unpickle, pycparser, json_loads, float, create_gc_cycles, python_startup, logging_simple, comprehensions, pylint, bench_mp_pool, xml_etree_generate, logging_format, deepcopy, pickle_list, async_tree_memoization_tg, python_startup_no_site, sympy_integrate, coroutines, pprint_safe_repr, async_tree_none_tg, async_tree_io, aiohttp, sympy_str, raytrace, gc_traversal, chameleon, mako, chaos, tornado_http, bench_thread_pool, async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization

# HPT report

- Reliability score: 77.64% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown
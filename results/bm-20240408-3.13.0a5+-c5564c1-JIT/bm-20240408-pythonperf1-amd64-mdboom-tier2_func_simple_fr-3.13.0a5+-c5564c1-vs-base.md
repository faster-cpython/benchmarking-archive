# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.00x slower
- HPT reliability: 97.27%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 4.68 ms                                                                     | 4.74 ms: 1.01x slower                                                       |
| docutils       | 1.70 sec                                                                    | 1.70 sec: 1.00x faster                                                      |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg | 603 ms                                                                      | 618 ms: 1.02x slower                                                        |
| Geometric mean   | (ref)                                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (7): async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_none, async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 146 ms                                                                      | 147 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.1 ms                                                                     | 14.9 ms: 1.02x faster                                                       |
| regex_effbot   | 1.62 ms                                                                     | 1.61 ms: 1.01x faster                                                       |
| regex_dna      | 121 ms                                                                      | 121 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads         | 14.2 us                                                                     | 13.9 us: 1.02x faster                                                       |
| pickle             | 7.36 us                                                                     | 7.26 us: 1.01x faster                                                       |
| pickle_dict        | 18.5 us                                                                     | 18.5 us: 1.00x faster                                                       |
| xml_etree_process  | 36.3 ms                                                                     | 36.4 ms: 1.00x slower                                                       |
| xml_etree_parse    | 90.3 ms                                                                     | 90.9 ms: 1.01x slower                                                       |
| json_dumps         | 5.56 ms                                                                     | 5.60 ms: 1.01x slower                                                       |
| tomli_loads        | 1.19 sec                                                                    | 1.20 sec: 1.01x slower                                                      |
| pickle_pure_python | 171 us                                                                      | 174 us: 1.01x slower                                                        |
| Geometric mean     | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (6): xml_etree_iterparse, unpickle, xml_etree_generate, unpickle_pure_python, unpickle_list, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 21.7 ms                                                                     | 21.9 ms: 1.01x slower                                                       |
| python_startup_no_site | 19.5 ms                                                                     | 19.7 ms: 1.01x slower                                                       |
| Geometric mean         | (ref)                                                                       | 1.01x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text    | 15.2 ms                                                                     | 15.4 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| generators               | 20.4 ms                                                                     | 19.5 ms: 1.05x faster                                                       |
| coverage                 | 46.4 ms                                                                     | 45.1 ms: 1.03x faster                                                       |
| asyncio_tcp              | 485 ms                                                                      | 473 ms: 1.03x faster                                                        |
| comprehensions           | 11.1 us                                                                     | 10.8 us: 1.02x faster                                                       |
| json_loads               | 14.2 us                                                                     | 13.9 us: 1.02x faster                                                       |
| typing_runtime_protocols | 72.0 us                                                                     | 70.8 us: 1.02x faster                                                       |
| sqlglot_normalize        | 184 ms                                                                      | 180 ms: 1.02x faster                                                        |
| regex_v8                 | 15.1 ms                                                                     | 14.9 ms: 1.02x faster                                                       |
| nqueens                  | 61.8 ms                                                                     | 60.9 ms: 1.01x faster                                                       |
| pickle                   | 7.36 us                                                                     | 7.26 us: 1.01x faster                                                       |
| regex_effbot             | 1.62 ms                                                                     | 1.61 ms: 1.01x faster                                                       |
| crypto_pyaes             | 44.3 ms                                                                     | 44.0 ms: 1.01x faster                                                       |
| sqlglot_optimize         | 35.3 ms                                                                     | 35.0 ms: 1.01x faster                                                       |
| thrift                   | 8.89 ms                                                                     | 8.84 ms: 1.01x faster                                                       |
| chaos                    | 38.1 ms                                                                     | 37.9 ms: 1.01x faster                                                       |
| regex_dna                | 121 ms                                                                      | 121 ms: 1.00x faster                                                        |
| pickle_dict              | 18.5 us                                                                     | 18.5 us: 1.00x faster                                                       |
| meteor_contest           | 73.2 ms                                                                     | 73.1 ms: 1.00x faster                                                       |
| docutils                 | 1.70 sec                                                                    | 1.70 sec: 1.00x faster                                                      |
| deepcopy_reduce          | 1.95 us                                                                     | 1.96 us: 1.00x slower                                                       |
| xml_etree_process        | 36.3 ms                                                                     | 36.4 ms: 1.00x slower                                                       |
| scimark_fft              | 165 ms                                                                      | 166 ms: 1.01x slower                                                        |
| pidigits                 | 146 ms                                                                      | 147 ms: 1.01x slower                                                        |
| xml_etree_parse          | 90.3 ms                                                                     | 90.9 ms: 1.01x slower                                                       |
| json_dumps               | 5.56 ms                                                                     | 5.60 ms: 1.01x slower                                                       |
| sqlite_synth             | 1.56 us                                                                     | 1.57 us: 1.01x slower                                                       |
| python_startup           | 21.7 ms                                                                     | 21.9 ms: 1.01x slower                                                       |
| tomli_loads              | 1.19 sec                                                                    | 1.20 sec: 1.01x slower                                                      |
| async_generators         | 235 ms                                                                      | 237 ms: 1.01x slower                                                        |
| python_startup_no_site   | 19.5 ms                                                                     | 19.7 ms: 1.01x slower                                                       |
| scimark_sparse_mat_mult  | 2.24 ms                                                                     | 2.26 ms: 1.01x slower                                                       |
| pathlib                  | 77.3 ms                                                                     | 78.1 ms: 1.01x slower                                                       |
| raytrace                 | 161 ms                                                                      | 163 ms: 1.01x slower                                                        |
| coroutines               | 13.0 ms                                                                     | 13.1 ms: 1.01x slower                                                       |
| deepcopy_memo            | 20.8 us                                                                     | 21.0 us: 1.01x slower                                                       |
| telco                    | 4.78 ms                                                                     | 4.84 ms: 1.01x slower                                                       |
| scimark_sor              | 82.4 ms                                                                     | 83.5 ms: 1.01x slower                                                       |
| richards                 | 26.4 ms                                                                     | 26.8 ms: 1.01x slower                                                       |
| chameleon                | 4.68 ms                                                                     | 4.74 ms: 1.01x slower                                                       |
| pprint_pformat           | 963 ms                                                                      | 976 ms: 1.01x slower                                                        |
| pickle_pure_python       | 171 us                                                                      | 174 us: 1.01x slower                                                        |
| genshi_text              | 15.2 ms                                                                     | 15.4 ms: 1.01x slower                                                       |
| fannkuch                 | 226 ms                                                                      | 230 ms: 1.01x slower                                                        |
| logging_format           | 6.15 us                                                                     | 6.26 us: 1.02x slower                                                       |
| bench_mp_pool            | 67.8 ms                                                                     | 68.9 ms: 1.02x slower                                                       |
| scimark_monte_carlo      | 38.3 ms                                                                     | 39.0 ms: 1.02x slower                                                       |
| logging_simple           | 5.72 us                                                                     | 5.83 us: 1.02x slower                                                       |
| richards_super           | 29.9 ms                                                                     | 30.6 ms: 1.02x slower                                                       |
| async_tree_io_tg         | 603 ms                                                                      | 618 ms: 1.02x slower                                                        |
| spectral_norm            | 50.7 ms                                                                     | 52.2 ms: 1.03x slower                                                       |
| mdp                      | 1.43 sec                                                                    | 1.53 sec: 1.07x slower                                                      |
| scimark_lu               | 69.0 ms                                                                     | 75.0 ms: 1.09x slower                                                       |
| Geometric mean           | (ref)                                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (44): logging_silent, asyncio_tcp_ssl, genshi_xml, xml_etree_iterparse, async_tree_io, aiohttp, unpickle, pyflate, xml_etree_generate, deltablue, go, async_tree_none_tg, mako, unpickle_pure_python, gc_traversal, sqlglot_parse, pylint, html5lib, sympy_integrate, regex_compile, mypy2, deepcopy, async_tree_cpu_io_mixed_tg, json, sympy_str, sympy_sum, sympy_expand, hexiom, async_tree_memoization, sqlglot_transpile, tornado_http, pprint_safe_repr, 2to3, nbody, unpickle_list, float, dulwich_log, async_tree_none, create_gc_cycles, pickle_list, pycparser, async_tree_memoization_tg, async_tree_cpu_io_mixed, bench_thread_pool

# HPT report

- Reliability score: 97.27% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown
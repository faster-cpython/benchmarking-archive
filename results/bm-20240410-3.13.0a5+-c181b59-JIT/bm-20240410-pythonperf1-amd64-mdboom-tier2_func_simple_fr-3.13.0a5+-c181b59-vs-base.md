# Results vs. base

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.00x faster
- HPT reliability: 95.97%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| docutils       | 1.70 sec                                                                    | 1.69 sec: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (4): 2to3, chameleon, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_io_tg, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 146 ms                                                                      | 147 ms: 1.00x slower                                                        |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.1 ms                                                                     | 14.3 ms: 1.06x faster                                                       |
| regex_dna      | 121 ms                                                                      | 116 ms: 1.05x faster                                                        |
| regex_effbot   | 1.62 ms                                                                     | 1.55 ms: 1.04x faster                                                       |
| regex_compile  | 86.3 ms                                                                     | 86.6 ms: 1.00x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.03x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| unpickle_list        | 2.88 us                                                                     | 2.78 us: 1.03x faster                                                       |
| json_loads           | 14.2 us                                                                     | 13.8 us: 1.03x faster                                                       |
| pickle               | 7.36 us                                                                     | 7.22 us: 1.02x faster                                                       |
| xml_etree_iterparse  | 61.2 ms                                                                     | 60.6 ms: 1.01x faster                                                       |
| json_dumps           | 5.56 ms                                                                     | 5.59 ms: 1.00x slower                                                       |
| tomli_loads          | 1.19 sec                                                                    | 1.21 sec: 1.01x slower                                                      |
| pickle_dict          | 18.5 us                                                                     | 18.8 us: 1.01x slower                                                       |
| xml_etree_process    | 36.3 ms                                                                     | 36.8 ms: 1.01x slower                                                       |
| unpickle_pure_python | 127 us                                                                      | 132 us: 1.04x slower                                                        |
| Geometric mean       | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (5): unpickle, xml_etree_generate, xml_etree_parse, pickle_pure_python, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 21.7 ms                                                                     | 21.5 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text    | 15.2 ms                                                                     | 15.4 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                | bm-20240405-pythonperf1-amd64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------------|:---------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp_ssl          | 1.63 sec                                                                    | 1.52 sec: 1.07x faster                                                      |
| regex_v8                 | 15.1 ms                                                                     | 14.3 ms: 1.06x faster                                                       |
| regex_dna                | 121 ms                                                                      | 116 ms: 1.05x faster                                                        |
| regex_effbot             | 1.62 ms                                                                     | 1.55 ms: 1.04x faster                                                       |
| asyncio_tcp              | 485 ms                                                                      | 468 ms: 1.04x faster                                                        |
| generators               | 20.4 ms                                                                     | 19.7 ms: 1.04x faster                                                       |
| unpickle_list            | 2.88 us                                                                     | 2.78 us: 1.03x faster                                                       |
| pathlib                  | 77.3 ms                                                                     | 74.9 ms: 1.03x faster                                                       |
| json_loads               | 14.2 us                                                                     | 13.8 us: 1.03x faster                                                       |
| comprehensions           | 11.1 us                                                                     | 10.8 us: 1.02x faster                                                       |
| thrift                   | 8.89 ms                                                                     | 8.68 ms: 1.02x faster                                                       |
| coverage                 | 46.4 ms                                                                     | 45.3 ms: 1.02x faster                                                       |
| pickle                   | 7.36 us                                                                     | 7.22 us: 1.02x faster                                                       |
| pprint_pformat           | 963 ms                                                                      | 945 ms: 1.02x faster                                                        |
| pprint_safe_repr         | 478 ms                                                                      | 470 ms: 1.02x faster                                                        |
| telco                    | 4.78 ms                                                                     | 4.71 ms: 1.02x faster                                                       |
| meteor_contest           | 73.2 ms                                                                     | 72.3 ms: 1.01x faster                                                       |
| sqlglot_normalize        | 184 ms                                                                      | 181 ms: 1.01x faster                                                        |
| hexiom                   | 4.46 ms                                                                     | 4.41 ms: 1.01x faster                                                       |
| xml_etree_iterparse      | 61.2 ms                                                                     | 60.6 ms: 1.01x faster                                                       |
| aiohttp                  | 910 us                                                                      | 902 us: 1.01x faster                                                        |
| docutils                 | 1.70 sec                                                                    | 1.69 sec: 1.01x faster                                                      |
| python_startup           | 21.7 ms                                                                     | 21.5 ms: 1.01x faster                                                       |
| sqlglot_optimize         | 35.3 ms                                                                     | 35.0 ms: 1.01x faster                                                       |
| logging_format           | 6.15 us                                                                     | 6.12 us: 1.01x faster                                                       |
| dulwich_log              | 41.2 ms                                                                     | 41.0 ms: 1.00x faster                                                       |
| coroutines               | 13.0 ms                                                                     | 13.0 ms: 1.00x slower                                                       |
| pylint                   | 194 ms                                                                      | 195 ms: 1.00x slower                                                        |
| pidigits                 | 146 ms                                                                      | 147 ms: 1.00x slower                                                        |
| regex_compile            | 86.3 ms                                                                     | 86.6 ms: 1.00x slower                                                       |
| json_dumps               | 5.56 ms                                                                     | 5.59 ms: 1.00x slower                                                       |
| crypto_pyaes             | 44.3 ms                                                                     | 44.5 ms: 1.00x slower                                                       |
| scimark_fft              | 165 ms                                                                      | 166 ms: 1.01x slower                                                        |
| mypy2                    | 447 ms                                                                      | 450 ms: 1.01x slower                                                        |
| scimark_sor              | 82.4 ms                                                                     | 83.0 ms: 1.01x slower                                                       |
| deepcopy_reduce          | 1.95 us                                                                     | 1.97 us: 1.01x slower                                                       |
| sqlite_synth             | 1.56 us                                                                     | 1.57 us: 1.01x slower                                                       |
| scimark_sparse_mat_mult  | 2.24 ms                                                                     | 2.26 ms: 1.01x slower                                                       |
| sympy_sum                | 88.1 ms                                                                     | 88.9 ms: 1.01x slower                                                       |
| sqlglot_parse            | 773 us                                                                      | 780 us: 1.01x slower                                                        |
| richards                 | 26.4 ms                                                                     | 26.7 ms: 1.01x slower                                                       |
| richards_super           | 29.9 ms                                                                     | 30.2 ms: 1.01x slower                                                       |
| go                       | 91.6 ms                                                                     | 92.7 ms: 1.01x slower                                                       |
| tomli_loads              | 1.19 sec                                                                    | 1.21 sec: 1.01x slower                                                      |
| bench_thread_pool        | 800 us                                                                      | 811 us: 1.01x slower                                                        |
| typing_runtime_protocols | 72.0 us                                                                     | 73.1 us: 1.01x slower                                                       |
| async_generators         | 235 ms                                                                      | 238 ms: 1.01x slower                                                        |
| pickle_dict              | 18.5 us                                                                     | 18.8 us: 1.01x slower                                                       |
| xml_etree_process        | 36.3 ms                                                                     | 36.8 ms: 1.01x slower                                                       |
| chaos                    | 38.1 ms                                                                     | 38.7 ms: 1.02x slower                                                       |
| sqlglot_transpile        | 989 us                                                                      | 1.00 ms: 1.02x slower                                                       |
| deepcopy_memo            | 20.8 us                                                                     | 21.1 us: 1.02x slower                                                       |
| spectral_norm            | 50.7 ms                                                                     | 51.6 ms: 1.02x slower                                                       |
| genshi_text              | 15.2 ms                                                                     | 15.4 ms: 1.02x slower                                                       |
| pyflate                  | 269 ms                                                                      | 274 ms: 1.02x slower                                                        |
| deepcopy                 | 220 us                                                                      | 224 us: 1.02x slower                                                        |
| raytrace                 | 161 ms                                                                      | 165 ms: 1.02x slower                                                        |
| fannkuch                 | 226 ms                                                                      | 232 ms: 1.02x slower                                                        |
| scimark_lu               | 69.0 ms                                                                     | 71.0 ms: 1.03x slower                                                       |
| unpickle_pure_python     | 127 us                                                                      | 132 us: 1.04x slower                                                        |
| Geometric mean           | (ref)                                                                       | 1.00x faster                                                                |

Benchmark hidden because not significant (36): unpickle, logging_silent, pycparser, nbody, float, create_gc_cycles, json, bench_mp_pool, async_tree_cpu_io_mixed_tg, html5lib, 2to3, logging_simple, sympy_str, mdp, scimark_monte_carlo, chameleon, async_tree_cpu_io_mixed, tornado_http, genshi_xml, sympy_expand, sympy_integrate, xml_etree_generate, async_tree_memoization, python_startup_no_site, xml_etree_parse, async_tree_io, pickle_pure_python, gc_traversal, nqueens, deltablue, async_tree_none_tg, async_tree_io_tg, mako, async_tree_none, async_tree_memoization_tg, pickle_list

# HPT report

- Reliability score: 95.97% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown
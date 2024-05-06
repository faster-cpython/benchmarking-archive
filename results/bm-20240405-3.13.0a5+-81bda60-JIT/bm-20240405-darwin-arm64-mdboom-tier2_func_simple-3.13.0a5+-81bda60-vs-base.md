# Results vs. base

- fork: mdboom
- ref: tier2_func_simple
- machine: darwin-arm64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.00x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| html5lib       | 32.9 ms                                                                | 33.2 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (4): 2to3, chameleon, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark           | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|---------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_eager_tg | 42.7 ms                                                                | 43.1 ms: 1.01x slower                                               |
| async_tree_eager    | 64.1 ms                                                                | 64.6 ms: 1.01x slower                                               |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (14): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io_tg, async_tree_eager_cpu_io_mixed, async_tree_memoization_tg, async_tree_none_tg, async_tree_eager_memoization_tg, async_tree_memoization, async_tree_eager_io, async_tree_none, async_tree_eager_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 49.0 ms                                                                | 48.9 ms: 1.00x faster                                               |
| pidigits       | 282 ms                                                                 | 282 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 85.8 ms                                                                | 84.6 ms: 1.01x faster                                               |
| regex_dna      | 152 ms                                                                 | 153 ms: 1.00x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle               | 7.50 us                                                                | 7.44 us: 1.01x faster                                               |
| pickle_list          | 2.94 us                                                                | 2.96 us: 1.00x slower                                               |
| xml_etree_process    | 37.1 ms                                                                | 37.3 ms: 1.01x slower                                               |
| xml_etree_generate   | 54.3 ms                                                                | 54.6 ms: 1.01x slower                                               |
| xml_etree_iterparse  | 72.1 ms                                                                | 72.6 ms: 1.01x slower                                               |
| tomli_loads          | 1.27 sec                                                               | 1.28 sec: 1.01x slower                                              |
| json_dumps           | 6.33 ms                                                                | 6.38 ms: 1.01x slower                                               |
| unpickle_pure_python | 140 us                                                                 | 141 us: 1.01x slower                                                |
| unpickle             | 9.30 us                                                                | 9.62 us: 1.03x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (5): unpickle_list, xml_etree_parse, pickle_dict, pickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 11.6 ms                                                                | 11.7 ms: 1.00x slower                                               |
| python_startup         | 13.4 ms                                                                | 13.5 ms: 1.01x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml     | 31.4 ms                                                                | 31.1 ms: 1.01x faster                                               |
| genshi_text    | 14.7 ms                                                                | 14.8 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark               | bm-20240405-darwin-arm64-python-687616877ba540a44f82-3.13.0a5+-6876168 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| dask                    | 223 ms                                                                 | 220 ms: 1.02x faster                                                |
| regex_compile           | 85.8 ms                                                                | 84.6 ms: 1.01x faster                                               |
| pprint_pformat          | 1000 ms                                                                | 986 ms: 1.01x faster                                                |
| pprint_safe_repr        | 492 ms                                                                 | 488 ms: 1.01x faster                                                |
| genshi_xml              | 31.4 ms                                                                | 31.1 ms: 1.01x faster                                               |
| pickle                  | 7.50 us                                                                | 7.44 us: 1.01x faster                                               |
| sqlglot_transpile       | 937 us                                                                 | 931 us: 1.01x faster                                                |
| sqlglot_parse           | 766 us                                                                 | 761 us: 1.01x faster                                                |
| go                      | 107 ms                                                                 | 106 ms: 1.00x faster                                                |
| float                   | 49.0 ms                                                                | 48.9 ms: 1.00x faster                                               |
| pidigits                | 282 ms                                                                 | 282 ms: 1.00x faster                                                |
| chaos                   | 37.9 ms                                                                | 38.0 ms: 1.00x slower                                               |
| regex_dna               | 152 ms                                                                 | 153 ms: 1.00x slower                                                |
| sympy_expand            | 238 ms                                                                 | 238 ms: 1.00x slower                                                |
| scimark_lu              | 82.1 ms                                                                | 82.4 ms: 1.00x slower                                               |
| nqueens                 | 60.5 ms                                                                | 60.6 ms: 1.00x slower                                               |
| mdp                     | 1.58 sec                                                               | 1.58 sec: 1.00x slower                                              |
| generators              | 26.1 ms                                                                | 26.2 ms: 1.00x slower                                               |
| gc_traversal            | 2.45 ms                                                                | 2.46 ms: 1.00x slower                                               |
| sqlglot_optimize        | 33.6 ms                                                                | 33.7 ms: 1.00x slower                                               |
| python_startup_no_site  | 11.6 ms                                                                | 11.7 ms: 1.00x slower                                               |
| deepcopy_reduce         | 1.86 us                                                                | 1.86 us: 1.00x slower                                               |
| pickle_list             | 2.94 us                                                                | 2.96 us: 1.00x slower                                               |
| deepcopy_memo           | 24.1 us                                                                | 24.2 us: 1.01x slower                                               |
| xml_etree_process       | 37.1 ms                                                                | 37.3 ms: 1.01x slower                                               |
| genshi_text             | 14.7 ms                                                                | 14.8 ms: 1.01x slower                                               |
| scimark_sor             | 106 ms                                                                 | 106 ms: 1.01x slower                                                |
| crypto_pyaes            | 46.3 ms                                                                | 46.6 ms: 1.01x slower                                               |
| xml_etree_generate      | 54.3 ms                                                                | 54.6 ms: 1.01x slower                                               |
| sympy_sum               | 76.3 ms                                                                | 76.8 ms: 1.01x slower                                               |
| sqlite_synth            | 1.58 us                                                                | 1.59 us: 1.01x slower                                               |
| dulwich_log             | 28.7 ms                                                                | 28.9 ms: 1.01x slower                                               |
| xml_etree_iterparse     | 72.1 ms                                                                | 72.6 ms: 1.01x slower                                               |
| sympy_integrate         | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                               |
| deepcopy                | 211 us                                                                 | 212 us: 1.01x slower                                                |
| meteor_contest          | 73.5 ms                                                                | 74.0 ms: 1.01x slower                                               |
| tomli_loads             | 1.27 sec                                                               | 1.28 sec: 1.01x slower                                              |
| async_tree_eager_tg     | 42.7 ms                                                                | 43.1 ms: 1.01x slower                                               |
| async_tree_eager        | 64.1 ms                                                                | 64.6 ms: 1.01x slower                                               |
| json_dumps              | 6.33 ms                                                                | 6.38 ms: 1.01x slower                                               |
| sympy_str               | 141 ms                                                                 | 143 ms: 1.01x slower                                                |
| create_gc_cycles        | 892 us                                                                 | 900 us: 1.01x slower                                                |
| pylint                  | 153 ms                                                                 | 155 ms: 1.01x slower                                                |
| python_startup          | 13.4 ms                                                                | 13.5 ms: 1.01x slower                                               |
| logging_simple          | 3.13 us                                                                | 3.17 us: 1.01x slower                                               |
| coverage                | 46.0 ms                                                                | 46.6 ms: 1.01x slower                                               |
| html5lib                | 32.9 ms                                                                | 33.2 ms: 1.01x slower                                               |
| comprehensions          | 11.9 us                                                                | 12.1 us: 1.01x slower                                               |
| scimark_fft             | 200 ms                                                                 | 203 ms: 1.01x slower                                                |
| scimark_monte_carlo     | 43.2 ms                                                                | 43.7 ms: 1.01x slower                                               |
| fannkuch                | 258 ms                                                                 | 262 ms: 1.01x slower                                                |
| unpickle_pure_python    | 140 us                                                                 | 141 us: 1.01x slower                                                |
| logging_format          | 3.39 us                                                                | 3.44 us: 1.01x slower                                               |
| scimark_sparse_mat_mult | 3.12 ms                                                                | 3.18 ms: 1.02x slower                                               |
| spectral_norm           | 73.7 ms                                                                | 75.1 ms: 1.02x slower                                               |
| json                    | 2.96 ms                                                                | 3.03 ms: 1.02x slower                                               |
| pathlib                 | 24.6 ms                                                                | 25.2 ms: 1.02x slower                                               |
| logging_silent          | 63.9 ns                                                                | 65.4 ns: 1.02x slower                                               |
| telco                   | 4.63 ms                                                                | 4.75 ms: 1.03x slower                                               |
| unpickle                | 9.30 us                                                                | 9.62 us: 1.03x slower                                               |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (47): tornado_http, asyncio_tcp, coroutines, async_tree_cpu_io_mixed_tg, unpickle_list, async_tree_cpu_io_mixed, xml_etree_parse, 2to3, deltablue, pickle_dict, async_tree_io_tg, asyncio_tcp_ssl, async_tree_eager_cpu_io_mixed_tg, richards_super, chameleon, docutils, mako, async_tree_eager_io_tg, sqlglot_normalize, richards, raytrace, async_tree_eager_cpu_io_mixed, nbody, pyflate, async_generators, pickle_pure_python, async_tree_memoization_tg, asyncio_websockets, bench_mp_pool, hexiom, async_tree_none_tg, bench_thread_pool, regex_v8, json_loads, mypy2, typing_runtime_protocols, async_tree_eager_memoization_tg, async_tree_memoization, async_tree_eager_io, pycparser, thrift, async_tree_none, async_tree_eager_memoization, async_tree_io, aiohttp, regex_effbot, gunicorn

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
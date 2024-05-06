# Results vs. base

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.00x faster
- HPT reliability: 66.26%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 278 ms                                                                 | 279 ms: 1.00x slower                                              |
| chameleon      | 6.82 ms                                                                | 6.88 ms: 1.01x slower                                             |
| docutils       | 2.92 sec                                                               | 2.91 sec: 1.00x faster                                            |
| html5lib       | 67.9 ms                                                                | 65.7 ms: 1.03x faster                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_none_tg, async_tree_none, async_tree_memoization, async_tree_memoization_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 206 ms                                                                 | 194 ms: 1.06x faster                                              |
| float          | 76.9 ms                                                                | 78.1 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 147 ms                                                                 | 145 ms: 1.01x faster                                              |
| regex_v8       | 25.9 ms                                                                | 26.1 ms: 1.01x slower                                             |
| regex_effbot   | 3.71 ms                                                                | 3.75 ms: 1.01x slower                                             |
| regex_dna      | 229 ms                                                                 | 233 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle               | 12.5 us                                                                | 11.8 us: 1.06x faster                                             |
| pickle_list          | 5.31 us                                                                | 5.06 us: 1.05x faster                                             |
| pickle_dict          | 35.6 us                                                                | 34.1 us: 1.04x faster                                             |
| pickle_pure_python   | 302 us                                                                 | 304 us: 1.01x slower                                              |
| unpickle_pure_python | 238 us                                                                 | 240 us: 1.01x slower                                              |
| json_loads           | 28.3 us                                                                | 28.6 us: 1.01x slower                                             |
| xml_etree_generate   | 86.4 ms                                                                | 87.4 ms: 1.01x slower                                             |
| xml_etree_process    | 59.6 ms                                                                | 60.6 ms: 1.02x slower                                             |
| xml_etree_parse      | 160 ms                                                                 | 162 ms: 1.02x slower                                              |
| unpickle_list        | 5.15 us                                                                | 5.24 us: 1.02x slower                                             |
| unpickle             | 15.2 us                                                                | 15.9 us: 1.05x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (3): tomli_loads, json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                             |
| python_startup_no_site | 9.47 ms                                                                | 9.55 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml     | 54.4 ms                                                                | 53.2 ms: 1.02x faster                                             |
| mako           | 10.7 ms                                                                | 10.9 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpack_sequence          | 95.5 ns                                                                | 89.6 ns: 1.07x faster                                             |
| pidigits                 | 206 ms                                                                 | 194 ms: 1.06x faster                                              |
| pickle                   | 12.5 us                                                                | 11.8 us: 1.06x faster                                             |
| pickle_list              | 5.31 us                                                                | 5.06 us: 1.05x faster                                             |
| pickle_dict              | 35.6 us                                                                | 34.1 us: 1.04x faster                                             |
| mdp                      | 2.81 sec                                                               | 2.70 sec: 1.04x faster                                            |
| html5lib                 | 67.9 ms                                                                | 65.7 ms: 1.03x faster                                             |
| scimark_sparse_mat_mult  | 5.02 ms                                                                | 4.89 ms: 1.03x faster                                             |
| deepcopy_memo            | 39.0 us                                                                | 38.0 us: 1.02x faster                                             |
| comprehensions           | 18.2 us                                                                | 17.8 us: 1.02x faster                                             |
| scimark_fft              | 346 ms                                                                 | 338 ms: 1.02x faster                                              |
| genshi_xml               | 54.4 ms                                                                | 53.2 ms: 1.02x faster                                             |
| nqueens                  | 91.0 ms                                                                | 89.0 ms: 1.02x faster                                             |
| go                       | 153 ms                                                                 | 150 ms: 1.02x faster                                              |
| hexiom                   | 7.05 ms                                                                | 6.93 ms: 1.02x faster                                             |
| deepcopy                 | 359 us                                                                 | 353 us: 1.02x faster                                              |
| fannkuch                 | 405 ms                                                                 | 399 ms: 1.01x faster                                              |
| regex_compile            | 147 ms                                                                 | 145 ms: 1.01x faster                                              |
| scimark_lu               | 133 ms                                                                 | 131 ms: 1.01x faster                                              |
| coroutines               | 22.4 ms                                                                | 22.1 ms: 1.01x faster                                             |
| sqlglot_transpile        | 1.65 ms                                                                | 1.63 ms: 1.01x faster                                             |
| logging_silent           | 102 ns                                                                 | 101 ns: 1.01x faster                                              |
| logging_format           | 6.64 us                                                                | 6.59 us: 1.01x faster                                             |
| raytrace                 | 280 ms                                                                 | 278 ms: 1.01x faster                                              |
| create_gc_cycles         | 1.76 ms                                                                | 1.75 ms: 1.01x faster                                             |
| pathlib                  | 19.1 ms                                                                | 19.1 ms: 1.00x faster                                             |
| docutils                 | 2.92 sec                                                               | 2.91 sec: 1.00x faster                                            |
| sqlglot_optimize         | 57.8 ms                                                                | 57.6 ms: 1.00x faster                                             |
| asyncio_tcp              | 514 ms                                                                 | 513 ms: 1.00x faster                                              |
| sympy_integrate          | 22.0 ms                                                                | 21.9 ms: 1.00x faster                                             |
| pylint                   | 298 ms                                                                 | 298 ms: 1.00x faster                                              |
| 2to3                     | 278 ms                                                                 | 279 ms: 1.00x slower                                              |
| dulwich_log              | 70.9 ms                                                                | 71.3 ms: 1.00x slower                                             |
| sympy_expand             | 493 ms                                                                 | 496 ms: 1.01x slower                                              |
| pickle_pure_python       | 302 us                                                                 | 304 us: 1.01x slower                                              |
| thrift                   | 822 us                                                                 | 827 us: 1.01x slower                                              |
| unpickle_pure_python     | 238 us                                                                 | 240 us: 1.01x slower                                              |
| async_generators         | 456 ms                                                                 | 459 ms: 1.01x slower                                              |
| regex_v8                 | 25.9 ms                                                                | 26.1 ms: 1.01x slower                                             |
| chameleon                | 6.82 ms                                                                | 6.88 ms: 1.01x slower                                             |
| python_startup           | 11.0 ms                                                                | 11.1 ms: 1.01x slower                                             |
| json_loads               | 28.3 us                                                                | 28.6 us: 1.01x slower                                             |
| json                     | 5.35 ms                                                                | 5.39 ms: 1.01x slower                                             |
| python_startup_no_site   | 9.47 ms                                                                | 9.55 ms: 1.01x slower                                             |
| meteor_contest           | 111 ms                                                                 | 112 ms: 1.01x slower                                              |
| mako                     | 10.7 ms                                                                | 10.9 ms: 1.01x slower                                             |
| logging_simple           | 6.01 us                                                                | 6.08 us: 1.01x slower                                             |
| xml_etree_generate       | 86.4 ms                                                                | 87.4 ms: 1.01x slower                                             |
| regex_effbot             | 3.71 ms                                                                | 3.75 ms: 1.01x slower                                             |
| richards_super           | 52.4 ms                                                                | 53.1 ms: 1.01x slower                                             |
| crypto_pyaes             | 74.3 ms                                                                | 75.4 ms: 1.01x slower                                             |
| scimark_sor              | 129 ms                                                                 | 130 ms: 1.02x slower                                              |
| xml_etree_process        | 59.6 ms                                                                | 60.6 ms: 1.02x slower                                             |
| float                    | 76.9 ms                                                                | 78.1 ms: 1.02x slower                                             |
| xml_etree_parse          | 160 ms                                                                 | 162 ms: 1.02x slower                                              |
| deepcopy_reduce          | 3.19 us                                                                | 3.24 us: 1.02x slower                                             |
| regex_dna                | 229 ms                                                                 | 233 ms: 1.02x slower                                              |
| unpickle_list            | 5.15 us                                                                | 5.24 us: 1.02x slower                                             |
| typing_runtime_protocols | 111 us                                                                 | 113 us: 1.02x slower                                              |
| telco                    | 8.44 ms                                                                | 8.65 ms: 1.02x slower                                             |
| coverage                 | 97.8 ms                                                                | 101 ms: 1.03x slower                                              |
| unpickle                 | 15.2 us                                                                | 15.9 us: 1.05x slower                                             |
| deltablue                | 3.38 ms                                                                | 3.76 ms: 1.11x slower                                             |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (37): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, genshi_text, sympy_str, async_tree_io_tg, async_tree_none_tg, async_tree_none, nbody, async_tree_memoization, gunicorn, mypy2, pprint_safe_repr, sqlglot_parse, tornado_http, scimark_monte_carlo, bench_thread_pool, tomli_loads, sqlglot_normalize, asyncio_tcp_ssl, aiohttp, json_dumps, chaos, gc_traversal, spectral_norm, asyncio_websockets, xml_etree_iterparse, pycparser, bench_mp_pool, generators, async_tree_memoization_tg, sqlite_synth, sympy_sum, pyflate, dask, richards, pprint_pformat, async_tree_io

# HPT report

- Reliability score: 66.26% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
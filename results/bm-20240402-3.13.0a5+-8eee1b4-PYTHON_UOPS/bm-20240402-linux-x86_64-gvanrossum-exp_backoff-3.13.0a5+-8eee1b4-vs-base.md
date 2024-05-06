# Results vs. base

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.00x faster
- HPT reliability: 97.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 317 ms                                                                 | 313 ms: 1.01x faster                                              |
| chameleon      | 7.81 ms                                                                | 7.85 ms: 1.01x slower                                             |
| docutils       | 3.18 sec                                                               | 3.16 sec: 1.00x faster                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none_tg, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 209 ms                                                                 | 197 ms: 1.06x faster                                              |
| float          | 95.3 ms                                                                | 94.6 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 201 ms                                                                 | 194 ms: 1.03x faster                                              |
| regex_dna      | 223 ms                                                                 | 227 ms: 1.02x slower                                              |
| regex_v8       | 26.0 ms                                                                | 26.7 ms: 1.03x slower                                             |
| regex_effbot   | 3.68 ms                                                                | 3.79 ms: 1.03x slower                                             |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| unpickle_pure_python | 334 us                                                                 | 309 us: 1.08x faster                                              |
| tomli_loads          | 2.94 sec                                                               | 2.78 sec: 1.06x faster                                            |
| pickle               | 12.3 us                                                                | 11.9 us: 1.04x faster                                             |
| json_dumps           | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                             |
| xml_etree_process    | 65.4 ms                                                                | 65.8 ms: 1.01x slower                                             |
| pickle_dict          | 33.8 us                                                                | 34.1 us: 1.01x slower                                             |
| xml_etree_generate   | 95.4 ms                                                                | 96.8 ms: 1.01x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                      |

Benchmark hidden because not significant (7): json_loads, unpickle_list, unpickle, pickle_list, pickle_pure_python, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 9.07 ms                                                                | 9.10 ms: 1.00x slower                                             |
| python_startup         | 10.7 ms                                                                | 10.7 ms: 1.00x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml     | 64.7 ms                                                                | 62.7 ms: 1.03x faster                                             |
| genshi_text    | 26.8 ms                                                                | 26.0 ms: 1.03x faster                                             |
| mako           | 14.1 ms                                                                | 13.9 ms: 1.02x faster                                             |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                      |

All benchmarks:
===============

| Benchmark                | bm-20240402-linux-x86_64-python-e569f9132b5bdc1c1031-3.13.0a5+-e569f91 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| scimark_monte_carlo      | 99.5 ms                                                                | 90.2 ms: 1.10x faster                                             |
| unpickle_pure_python     | 334 us                                                                 | 309 us: 1.08x faster                                              |
| nqueens                  | 129 ms                                                                 | 121 ms: 1.06x faster                                              |
| pidigits                 | 209 ms                                                                 | 197 ms: 1.06x faster                                              |
| tomli_loads              | 2.94 sec                                                               | 2.78 sec: 1.06x faster                                            |
| fannkuch                 | 525 ms                                                                 | 497 ms: 1.06x faster                                              |
| scimark_sor              | 160 ms                                                                 | 151 ms: 1.06x faster                                              |
| raytrace                 | 393 ms                                                                 | 373 ms: 1.05x faster                                              |
| mdp                      | 2.98 sec                                                               | 2.84 sec: 1.05x faster                                            |
| meteor_contest           | 132 ms                                                                 | 127 ms: 1.04x faster                                              |
| pickle                   | 12.3 us                                                                | 11.9 us: 1.04x faster                                             |
| hexiom                   | 10.6 ms                                                                | 10.2 ms: 1.04x faster                                             |
| richards_super           | 70.5 ms                                                                | 68.0 ms: 1.04x faster                                             |
| richards                 | 63.1 ms                                                                | 61.1 ms: 1.03x faster                                             |
| regex_compile            | 201 ms                                                                 | 194 ms: 1.03x faster                                              |
| genshi_xml               | 64.7 ms                                                                | 62.7 ms: 1.03x faster                                             |
| genshi_text              | 26.8 ms                                                                | 26.0 ms: 1.03x faster                                             |
| comprehensions           | 26.7 us                                                                | 25.9 us: 1.03x faster                                             |
| pprint_safe_repr         | 1.16 sec                                                               | 1.13 sec: 1.03x faster                                            |
| pprint_pformat           | 2.41 sec                                                               | 2.35 sec: 1.03x faster                                            |
| logging_silent           | 111 ns                                                                 | 108 ns: 1.03x faster                                              |
| go                       | 188 ms                                                                 | 185 ms: 1.02x faster                                              |
| coroutines               | 22.7 ms                                                                | 22.3 ms: 1.02x faster                                             |
| mako                     | 14.1 ms                                                                | 13.9 ms: 1.02x faster                                             |
| json                     | 5.57 ms                                                                | 5.47 ms: 1.02x faster                                             |
| sqlglot_transpile        | 1.90 ms                                                                | 1.88 ms: 1.01x faster                                             |
| logging_format           | 7.46 us                                                                | 7.37 us: 1.01x faster                                             |
| 2to3                     | 317 ms                                                                 | 313 ms: 1.01x faster                                              |
| chaos                    | 80.7 ms                                                                | 79.9 ms: 1.01x faster                                             |
| sqlglot_parse            | 1.57 ms                                                                | 1.55 ms: 1.01x faster                                             |
| deepcopy_reduce          | 3.37 us                                                                | 3.35 us: 1.01x faster                                             |
| deepcopy                 | 394 us                                                                 | 391 us: 1.01x faster                                              |
| float                    | 95.3 ms                                                                | 94.6 ms: 1.01x faster                                             |
| crypto_pyaes             | 93.9 ms                                                                | 93.4 ms: 1.01x faster                                             |
| sqlglot_optimize         | 67.9 ms                                                                | 67.5 ms: 1.01x faster                                             |
| docutils                 | 3.18 sec                                                               | 3.16 sec: 1.00x faster                                            |
| dulwich_log              | 76.5 ms                                                                | 76.3 ms: 1.00x faster                                             |
| bench_thread_pool        | 899 us                                                                 | 897 us: 1.00x faster                                              |
| python_startup_no_site   | 9.07 ms                                                                | 9.10 ms: 1.00x slower                                             |
| python_startup           | 10.7 ms                                                                | 10.7 ms: 1.00x slower                                             |
| chameleon                | 7.81 ms                                                                | 7.85 ms: 1.01x slower                                             |
| typing_runtime_protocols | 128 us                                                                 | 129 us: 1.01x slower                                              |
| pylint                   | 313 ms                                                                 | 315 ms: 1.01x slower                                              |
| json_dumps               | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                             |
| xml_etree_process        | 65.4 ms                                                                | 65.8 ms: 1.01x slower                                             |
| generators               | 29.8 ms                                                                | 30.0 ms: 1.01x slower                                             |
| sqlglot_normalize        | 130 ms                                                                 | 131 ms: 1.01x slower                                              |
| pickle_dict              | 33.8 us                                                                | 34.1 us: 1.01x slower                                             |
| coverage                 | 97.3 ms                                                                | 98.2 ms: 1.01x slower                                             |
| async_generators         | 478 ms                                                                 | 483 ms: 1.01x slower                                              |
| xml_etree_generate       | 95.4 ms                                                                | 96.8 ms: 1.01x slower                                             |
| gc_traversal             | 3.94 ms                                                                | 4.00 ms: 1.01x slower                                             |
| regex_dna                | 223 ms                                                                 | 227 ms: 1.02x slower                                              |
| telco                    | 9.48 ms                                                                | 9.69 ms: 1.02x slower                                             |
| pyflate                  | 636 ms                                                                 | 651 ms: 1.02x slower                                              |
| regex_v8                 | 26.0 ms                                                                | 26.7 ms: 1.03x slower                                             |
| pycparser                | 1.41 sec                                                               | 1.45 sec: 1.03x slower                                            |
| regex_effbot             | 3.68 ms                                                                | 3.79 ms: 1.03x slower                                             |
| spectral_norm            | 149 ms                                                                 | 153 ms: 1.03x slower                                              |
| scimark_sparse_mat_mult  | 6.07 ms                                                                | 6.33 ms: 1.04x slower                                             |
| scimark_lu               | 167 ms                                                                 | 176 ms: 1.05x slower                                              |
| deltablue                | 4.05 ms                                                                | 4.53 ms: 1.12x slower                                             |
| unpack_sequence          | 62.1 ns                                                                | 79.3 ns: 1.28x slower                                             |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                      |

Benchmark hidden because not significant (37): async_tree_none, sqlite_synth, async_tree_cpu_io_mixed, sympy_str, logging_simple, json_loads, aiohttp, tornado_http, gunicorn, async_tree_memoization_tg, async_tree_none_tg, create_gc_cycles, bench_mp_pool, asyncio_tcp, unpickle_list, sympy_sum, sympy_expand, async_tree_io, unpickle, pathlib, asyncio_tcp_ssl, dask, nbody, async_tree_cpu_io_mixed_tg, async_tree_memoization, html5lib, scimark_fft, sympy_integrate, mypy2, deepcopy_memo, asyncio_websockets, pickle_list, thrift, pickle_pure_python, xml_etree_parse, xml_etree_iterparse, async_tree_io_tg

# HPT report

- Reliability score: 97.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
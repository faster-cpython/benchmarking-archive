# Results vs. base

- fork: faster-cpython
- ref: faster_trashcan
- machine: linux-x86_64
- commit hash: 29e2a03
- commit date: 2024-04-11
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6+-02f1385 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 272 ms                                                                 | 268 ms: 1.01x faster                                                        |
| chameleon      | 6.93 ms                                                                | 6.80 ms: 1.02x faster                                                       |
| docutils       | 2.83 sec                                                               | 2.81 sec: 1.00x faster                                                      |
| html5lib       | 66.5 ms                                                                | 68.1 ms: 1.02x slower                                                       |
| tornado_http   | 95.0 ms                                                                | 94.2 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6+-02f1385 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 90.2 ms                                                                | 88.0 ms: 1.02x faster                                                       |
| float          | 79.7 ms                                                                | 78.0 ms: 1.02x faster                                                       |
| pidigits       | 193 ms                                                                 | 203 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6+-02f1385 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                 | 135 ms: 1.02x faster                                                        |
| regex_effbot   | 3.85 ms                                                                | 3.81 ms: 1.01x faster                                                       |
| regex_dna      | 224 ms                                                                 | 223 ms: 1.01x faster                                                        |
| regex_v8       | 25.5 ms                                                                | 25.9 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6+-02f1385 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_list          | 5.29 us                                                                | 4.94 us: 1.07x faster                                                       |
| pickle_dict          | 36.0 us                                                                | 34.2 us: 1.05x faster                                                       |
| pickle               | 12.0 us                                                                | 11.6 us: 1.03x faster                                                       |
| xml_etree_generate   | 88.9 ms                                                                | 87.2 ms: 1.02x faster                                                       |
| pickle_pure_python   | 302 us                                                                 | 298 us: 1.01x faster                                                        |
| xml_etree_iterparse  | 108 ms                                                                 | 107 ms: 1.01x faster                                                        |
| unpickle_pure_python | 226 us                                                                 | 224 us: 1.01x faster                                                        |
| xml_etree_process    | 60.9 ms                                                                | 60.5 ms: 1.01x faster                                                       |
| unpickle_list        | 5.17 us                                                                | 5.34 us: 1.03x slower                                                       |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                |

Benchmark hidden because not significant (5): unpickle, xml_etree_parse, tomli_loads, json_dumps, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6+-02f1385 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.09 ms                                                                | 7.06 ms: 1.00x faster                                                       |
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                       |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6+-02f1385 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 10.9 ms                                                                | 10.7 ms: 1.02x faster                                                       |
| genshi_xml     | 51.9 ms                                                                | 51.3 ms: 1.01x faster                                                       |
| genshi_text    | 23.7 ms                                                                | 23.4 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                |

All benchmarks:
===============

| Benchmark               | bm-20240411-linux-x86_64-python-02f1385f8ad6bf453763-3.13.0a6+-02f1385 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| logging_silent          | 104 ns                                                                 | 96.0 ns: 1.08x faster                                                       |
| pickle_list             | 5.29 us                                                                | 4.94 us: 1.07x faster                                                       |
| pickle_dict             | 36.0 us                                                                | 34.2 us: 1.05x faster                                                       |
| deepcopy_memo           | 39.1 us                                                                | 37.6 us: 1.04x faster                                                       |
| pickle                  | 12.0 us                                                                | 11.6 us: 1.03x faster                                                       |
| scimark_sor             | 126 ms                                                                 | 122 ms: 1.03x faster                                                        |
| deltablue               | 3.25 ms                                                                | 3.17 ms: 1.02x faster                                                       |
| nbody                   | 90.2 ms                                                                | 88.0 ms: 1.02x faster                                                       |
| float                   | 79.7 ms                                                                | 78.0 ms: 1.02x faster                                                       |
| raytrace                | 267 ms                                                                 | 261 ms: 1.02x faster                                                        |
| async_generators        | 448 ms                                                                 | 439 ms: 1.02x faster                                                        |
| mako                    | 10.9 ms                                                                | 10.7 ms: 1.02x faster                                                       |
| xml_etree_generate      | 88.9 ms                                                                | 87.2 ms: 1.02x faster                                                       |
| telco                   | 8.90 ms                                                                | 8.74 ms: 1.02x faster                                                       |
| chameleon               | 6.93 ms                                                                | 6.80 ms: 1.02x faster                                                       |
| comprehensions          | 17.0 us                                                                | 16.7 us: 1.02x faster                                                       |
| richards                | 47.3 ms                                                                | 46.5 ms: 1.02x faster                                                       |
| logging_simple          | 5.84 us                                                                | 5.74 us: 1.02x faster                                                       |
| spectral_norm           | 115 ms                                                                 | 113 ms: 1.02x faster                                                        |
| regex_compile           | 137 ms                                                                 | 135 ms: 1.02x faster                                                        |
| 2to3                    | 272 ms                                                                 | 268 ms: 1.01x faster                                                        |
| pickle_pure_python      | 302 us                                                                 | 298 us: 1.01x faster                                                        |
| logging_format          | 6.45 us                                                                | 6.37 us: 1.01x faster                                                       |
| scimark_monte_carlo     | 69.3 ms                                                                | 68.5 ms: 1.01x faster                                                       |
| go                      | 143 ms                                                                 | 142 ms: 1.01x faster                                                        |
| genshi_xml              | 51.9 ms                                                                | 51.3 ms: 1.01x faster                                                       |
| genshi_text             | 23.7 ms                                                                | 23.4 ms: 1.01x faster                                                       |
| chaos                   | 60.7 ms                                                                | 60.0 ms: 1.01x faster                                                       |
| pylint                  | 280 ms                                                                 | 277 ms: 1.01x faster                                                        |
| regex_effbot            | 3.85 ms                                                                | 3.81 ms: 1.01x faster                                                       |
| sympy_integrate         | 20.6 ms                                                                | 20.4 ms: 1.01x faster                                                       |
| xml_etree_iterparse     | 108 ms                                                                 | 107 ms: 1.01x faster                                                        |
| hexiom                  | 6.32 ms                                                                | 6.26 ms: 1.01x faster                                                       |
| sympy_sum               | 157 ms                                                                 | 155 ms: 1.01x faster                                                        |
| tornado_http            | 95.0 ms                                                                | 94.2 ms: 1.01x faster                                                       |
| pprint_safe_repr        | 752 ms                                                                 | 746 ms: 1.01x faster                                                        |
| sqlglot_normalize       | 111 ms                                                                 | 110 ms: 1.01x faster                                                        |
| richards_super          | 53.3 ms                                                                | 52.9 ms: 1.01x faster                                                       |
| regex_dna               | 224 ms                                                                 | 223 ms: 1.01x faster                                                        |
| unpickle_pure_python    | 226 us                                                                 | 224 us: 1.01x faster                                                        |
| xml_etree_process       | 60.9 ms                                                                | 60.5 ms: 1.01x faster                                                       |
| sqlglot_optimize        | 55.5 ms                                                                | 55.2 ms: 1.01x faster                                                       |
| asyncio_tcp             | 508 ms                                                                 | 505 ms: 1.01x faster                                                        |
| python_startup_no_site  | 7.09 ms                                                                | 7.06 ms: 1.00x faster                                                       |
| thrift                  | 814 us                                                                 | 811 us: 1.00x faster                                                        |
| docutils                | 2.83 sec                                                               | 2.81 sec: 1.00x faster                                                      |
| mdp                     | 2.59 sec                                                               | 2.58 sec: 1.00x faster                                                      |
| python_startup          | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                       |
| bench_thread_pool       | 838 us                                                                 | 836 us: 1.00x faster                                                        |
| sympy_expand            | 470 ms                                                                 | 469 ms: 1.00x faster                                                        |
| asyncio_tcp_ssl         | 1.84 sec                                                               | 1.84 sec: 1.00x slower                                                      |
| deepcopy                | 358 us                                                                 | 360 us: 1.01x slower                                                        |
| fannkuch                | 387 ms                                                                 | 390 ms: 1.01x slower                                                        |
| pyflate                 | 474 ms                                                                 | 479 ms: 1.01x slower                                                        |
| generators              | 30.0 ms                                                                | 30.3 ms: 1.01x slower                                                       |
| coverage                | 96.4 ms                                                                | 97.6 ms: 1.01x slower                                                       |
| regex_v8                | 25.5 ms                                                                | 25.9 ms: 1.01x slower                                                       |
| sqlite_synth            | 2.93 us                                                                | 2.99 us: 1.02x slower                                                       |
| scimark_fft             | 369 ms                                                                 | 378 ms: 1.02x slower                                                        |
| html5lib                | 66.5 ms                                                                | 68.1 ms: 1.02x slower                                                       |
| coroutines              | 22.5 ms                                                                | 23.2 ms: 1.03x slower                                                       |
| unpickle_list           | 5.17 us                                                                | 5.34 us: 1.03x slower                                                       |
| scimark_sparse_mat_mult | 5.09 ms                                                                | 5.33 ms: 1.05x slower                                                       |
| pidigits                | 193 ms                                                                 | 203 ms: 1.05x slower                                                        |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                                |

Benchmark hidden because not significant (35): async_tree_io, pycparser, unpickle, xml_etree_parse, async_tree_memoization_tg, async_tree_none_tg, tomli_loads, async_tree_none, mypy2, gunicorn, nqueens, sympy_str, bench_mp_pool, pprint_pformat, crypto_pyaes, aiohttp, json, dulwich_log, json_dumps, scimark_lu, sqlglot_transpile, gc_traversal, dask, create_gc_cycles, asyncio_websockets, sqlglot_parse, meteor_contest, deepcopy_reduce, async_tree_memoization, pathlib, typing_runtime_protocols, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io_tg, json_loads

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
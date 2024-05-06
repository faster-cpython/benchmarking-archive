# Results vs. base

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 846a7ef
- commit date: 2024-05-01
- overall geometric mean: 1.01x slower
- HPT reliability: 99.43%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6+-7595511 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 269 ms                                                                 | 272 ms: 1.01x slower                                                             |
| chameleon      | 7.11 ms                                                                | 7.03 ms: 1.01x faster                                                            |
| html5lib       | 68.5 ms                                                                | 69.5 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6+-7595511 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg | 336 ms                                                                 | 341 ms: 1.02x slower                                                             |
| Geometric mean     | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (7): async_tree_io, async_tree_memoization, async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6+-7595511 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.6 ms                                                                | 78.2 ms: 1.01x faster                                                            |
| nbody          | 85.9 ms                                                                | 89.6 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6+-7595511 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 25.0 ms                                                                | 24.4 ms: 1.02x faster                                                            |
| regex_dna      | 225 ms                                                                 | 221 ms: 1.02x faster                                                             |
| regex_compile  | 134 ms                                                                 | 134 ms: 1.00x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6+-7595511 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.17 us                                                                | 5.00 us: 1.03x faster                                                            |
| xml_etree_parse      | 161 ms                                                                 | 158 ms: 1.02x faster                                                             |
| pickle               | 11.8 us                                                                | 11.6 us: 1.02x faster                                                            |
| unpickle_list        | 5.23 us                                                                | 5.18 us: 1.01x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                                 | 107 ms: 1.01x faster                                                             |
| pickle_dict          | 34.7 us                                                                | 34.8 us: 1.01x slower                                                            |
| unpickle             | 14.9 us                                                                | 15.0 us: 1.01x slower                                                            |
| xml_etree_generate   | 87.6 ms                                                                | 88.4 ms: 1.01x slower                                                            |
| json_loads           | 28.2 us                                                                | 28.6 us: 1.01x slower                                                            |
| unpickle_pure_python | 215 us                                                                 | 218 us: 1.01x slower                                                             |
| xml_etree_process    | 60.9 ms                                                                | 61.8 ms: 1.01x slower                                                            |
| json_dumps           | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                            |
| pickle_pure_python   | 305 us                                                                 | 318 us: 1.04x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6+-7595511 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x slower                                                            |
| python_startup_no_site | 7.07 ms                                                                | 7.09 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6+-7595511 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                                | 50.6 ms: 1.02x faster                                                            |
| genshi_text     | 23.8 ms                                                                | 23.3 ms: 1.02x faster                                                            |
| django_template | 34.7 ms                                                                | 34.9 ms: 1.01x slower                                                            |
| mako            | 10.8 ms                                                                | 11.4 ms: 1.06x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20240501-linux-x86_64-python-75955110a643875b5d09-3.13.0a6+-7595511 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| go                       | 142 ms                                                                 | 119 ms: 1.19x faster                                                             |
| gc_traversal             | 4.02 ms                                                                | 3.75 ms: 1.07x faster                                                            |
| pickle_list              | 5.17 us                                                                | 5.00 us: 1.03x faster                                                            |
| genshi_xml               | 51.8 ms                                                                | 50.6 ms: 1.02x faster                                                            |
| regex_v8                 | 25.0 ms                                                                | 24.4 ms: 1.02x faster                                                            |
| genshi_text              | 23.8 ms                                                                | 23.3 ms: 1.02x faster                                                            |
| regex_dna                | 225 ms                                                                 | 221 ms: 1.02x faster                                                             |
| xml_etree_parse          | 161 ms                                                                 | 158 ms: 1.02x faster                                                             |
| pickle                   | 11.8 us                                                                | 11.6 us: 1.02x faster                                                            |
| mdp                      | 2.62 sec                                                               | 2.59 sec: 1.01x faster                                                           |
| pprint_safe_repr         | 759 ms                                                                 | 751 ms: 1.01x faster                                                             |
| chameleon                | 7.11 ms                                                                | 7.03 ms: 1.01x faster                                                            |
| unpickle_list            | 5.23 us                                                                | 5.18 us: 1.01x faster                                                            |
| typing_runtime_protocols | 162 us                                                                 | 161 us: 1.01x faster                                                             |
| deepcopy                 | 357 us                                                                 | 354 us: 1.01x faster                                                             |
| xml_etree_iterparse      | 108 ms                                                                 | 107 ms: 1.01x faster                                                             |
| meteor_contest           | 111 ms                                                                 | 110 ms: 1.01x faster                                                             |
| asyncio_tcp              | 515 ms                                                                 | 511 ms: 1.01x faster                                                             |
| pprint_pformat           | 1.55 sec                                                               | 1.54 sec: 1.01x faster                                                           |
| float                    | 78.6 ms                                                                | 78.2 ms: 1.01x faster                                                            |
| coroutines               | 22.6 ms                                                                | 22.5 ms: 1.01x faster                                                            |
| sympy_sum                | 154 ms                                                                 | 154 ms: 1.00x faster                                                             |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.84 sec: 1.00x faster                                                           |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x slower                                                            |
| python_startup_no_site   | 7.07 ms                                                                | 7.09 ms: 1.00x slower                                                            |
| regex_compile            | 134 ms                                                                 | 134 ms: 1.00x slower                                                             |
| bench_thread_pool        | 828 us                                                                 | 831 us: 1.00x slower                                                             |
| dulwich_log              | 65.8 ms                                                                | 66.1 ms: 1.00x slower                                                            |
| async_generators         | 444 ms                                                                 | 446 ms: 1.00x slower                                                             |
| pickle_dict              | 34.7 us                                                                | 34.8 us: 1.01x slower                                                            |
| aiohttp                  | 1.17 ms                                                                | 1.17 ms: 1.01x slower                                                            |
| sympy_str                | 278 ms                                                                 | 279 ms: 1.01x slower                                                             |
| richards_super           | 53.4 ms                                                                | 53.7 ms: 1.01x slower                                                            |
| unpickle                 | 14.9 us                                                                | 15.0 us: 1.01x slower                                                            |
| sqlglot_optimize         | 54.7 ms                                                                | 55.1 ms: 1.01x slower                                                            |
| logging_format           | 6.40 us                                                                | 6.44 us: 1.01x slower                                                            |
| django_template          | 34.7 ms                                                                | 34.9 ms: 1.01x slower                                                            |
| richards                 | 47.5 ms                                                                | 47.9 ms: 1.01x slower                                                            |
| generators               | 29.0 ms                                                                | 29.2 ms: 1.01x slower                                                            |
| sqlglot_normalize        | 110 ms                                                                 | 111 ms: 1.01x slower                                                             |
| scimark_lu               | 113 ms                                                                 | 114 ms: 1.01x slower                                                             |
| xml_etree_generate       | 87.6 ms                                                                | 88.4 ms: 1.01x slower                                                            |
| comprehensions           | 16.5 us                                                                | 16.7 us: 1.01x slower                                                            |
| 2to3                     | 269 ms                                                                 | 272 ms: 1.01x slower                                                             |
| scimark_fft              | 363 ms                                                                 | 367 ms: 1.01x slower                                                             |
| sqlite_synth             | 2.92 us                                                                | 2.96 us: 1.01x slower                                                            |
| json_loads               | 28.2 us                                                                | 28.6 us: 1.01x slower                                                            |
| deepcopy_reduce          | 3.19 us                                                                | 3.23 us: 1.01x slower                                                            |
| unpickle_pure_python     | 215 us                                                                 | 218 us: 1.01x slower                                                             |
| html5lib                 | 68.5 ms                                                                | 69.5 ms: 1.01x slower                                                            |
| xml_etree_process        | 60.9 ms                                                                | 61.8 ms: 1.01x slower                                                            |
| hexiom                   | 6.19 ms                                                                | 6.28 ms: 1.01x slower                                                            |
| raytrace                 | 262 ms                                                                 | 266 ms: 1.02x slower                                                             |
| thrift                   | 820 us                                                                 | 833 us: 1.02x slower                                                             |
| json_dumps               | 10.6 ms                                                                | 10.8 ms: 1.02x slower                                                            |
| sympy_expand             | 465 ms                                                                 | 473 ms: 1.02x slower                                                             |
| async_tree_none_tg       | 336 ms                                                                 | 341 ms: 1.02x slower                                                             |
| deltablue                | 3.16 ms                                                                | 3.23 ms: 1.02x slower                                                            |
| telco                    | 8.44 ms                                                                | 8.62 ms: 1.02x slower                                                            |
| deepcopy_memo            | 37.1 us                                                                | 38.1 us: 1.03x slower                                                            |
| spectral_norm            | 110 ms                                                                 | 113 ms: 1.03x slower                                                             |
| json                     | 5.20 ms                                                                | 5.39 ms: 1.04x slower                                                            |
| fannkuch                 | 386 ms                                                                 | 402 ms: 1.04x slower                                                             |
| nbody                    | 85.9 ms                                                                | 89.6 ms: 1.04x slower                                                            |
| pickle_pure_python       | 305 us                                                                 | 318 us: 1.04x slower                                                             |
| coverage                 | 91.8 ms                                                                | 96.8 ms: 1.05x slower                                                            |
| logging_silent           | 97.8 ns                                                                | 103 ns: 1.06x slower                                                             |
| mako                     | 10.8 ms                                                                | 11.4 ms: 1.06x slower                                                            |
| scimark_monte_carlo      | 68.1 ms                                                                | 73.9 ms: 1.09x slower                                                            |
| scimark_sor              | 121 ms                                                                 | 132 ms: 1.09x slower                                                             |
| crypto_pyaes             | 73.0 ms                                                                | 83.5 ms: 1.14x slower                                                            |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (30): async_tree_io, async_tree_memoization, scimark_sparse_mat_mult, logging_simple, djangocms, create_gc_cycles, async_tree_io_tg, tornado_http, regex_effbot, pidigits, chaos, asyncio_websockets, async_tree_none, pyflate, nqueens, sqlglot_transpile, tomli_loads, pathlib, gunicorn, sympy_integrate, bench_mp_pool, docutils, async_tree_cpu_io_mixed, dask, sqlglot_parse, pylint, mypy2, pycparser, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

# HPT report

- Reliability score: 99.43% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
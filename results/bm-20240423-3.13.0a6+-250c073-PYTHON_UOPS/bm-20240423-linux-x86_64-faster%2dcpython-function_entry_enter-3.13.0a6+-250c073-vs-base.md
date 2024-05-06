# Results vs. base

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 250c073
- commit date: 2024-04-23
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 303 ms: 1.03x faster                                                             |
| chameleon      | 7.90 ms                                                                | 8.01 ms: 1.01x slower                                                            |
| docutils       | 3.18 sec                                                               | 3.09 sec: 1.03x faster                                                           |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg | 360 ms                                                                 | 353 ms: 1.02x faster                                                             |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (7): async_tree_none, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 193 ms                                                                 | 212 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                     |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                                 | 182 ms: 1.05x faster                                                             |
| regex_v8       | 25.7 ms                                                                | 25.1 ms: 1.03x faster                                                            |
| regex_dna      | 226 ms                                                                 | 224 ms: 1.01x faster                                                             |
| regex_effbot   | 3.69 ms                                                                | 3.67 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 2.67 sec                                                               | 2.53 sec: 1.06x faster                                                           |
| unpickle_pure_python | 297 us                                                                 | 286 us: 1.04x faster                                                             |
| xml_etree_generate   | 95.5 ms                                                                | 92.9 ms: 1.03x faster                                                            |
| xml_etree_parse      | 154 ms                                                                 | 151 ms: 1.02x faster                                                             |
| xml_etree_process    | 64.5 ms                                                                | 64.0 ms: 1.01x faster                                                            |
| pickle_pure_python   | 314 us                                                                 | 318 us: 1.01x slower                                                             |
| json_loads           | 27.9 us                                                                | 28.2 us: 1.01x slower                                                            |
| unpickle_list        | 5.31 us                                                                | 5.41 us: 1.02x slower                                                            |
| pickle_dict          | 34.7 us                                                                | 35.5 us: 1.02x slower                                                            |
| pickle               | 11.6 us                                                                | 11.9 us: 1.03x slower                                                            |
| unpickle             | 15.1 us                                                                | 15.7 us: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (3): pickle_list, json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                                | 7.18 ms: 1.00x slower                                                            |
| python_startup         | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 42.8 ms                                                                | 40.9 ms: 1.05x faster                                                            |
| genshi_xml      | 61.7 ms                                                                | 59.0 ms: 1.05x faster                                                            |
| genshi_text     | 26.0 ms                                                                | 25.2 ms: 1.03x faster                                                            |
| mako            | 13.1 ms                                                                | 13.7 ms: 1.04x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pyflate                  | 712 ms                                                                 | 595 ms: 1.20x faster                                                             |
| nqueens                  | 129 ms                                                                 | 108 ms: 1.19x faster                                                             |
| pprint_pformat           | 2.27 sec                                                               | 1.97 sec: 1.15x faster                                                           |
| pprint_safe_repr         | 1.09 sec                                                               | 952 ms: 1.15x faster                                                             |
| scimark_monte_carlo      | 103 ms                                                                 | 90.5 ms: 1.14x faster                                                            |
| richards_super           | 70.7 ms                                                                | 62.3 ms: 1.13x faster                                                            |
| richards                 | 62.6 ms                                                                | 55.6 ms: 1.13x faster                                                            |
| crypto_pyaes             | 103 ms                                                                 | 92.5 ms: 1.12x faster                                                            |
| deepcopy_memo            | 49.3 us                                                                | 44.6 us: 1.11x faster                                                            |
| raytrace                 | 350 ms                                                                 | 322 ms: 1.09x faster                                                             |
| chaos                    | 85.4 ms                                                                | 78.9 ms: 1.08x faster                                                            |
| hexiom                   | 10.2 ms                                                                | 9.53 ms: 1.07x faster                                                            |
| comprehensions           | 24.7 us                                                                | 23.2 us: 1.06x faster                                                            |
| scimark_sor              | 166 ms                                                                 | 157 ms: 1.06x faster                                                             |
| tomli_loads              | 2.67 sec                                                               | 2.53 sec: 1.06x faster                                                           |
| sqlglot_optimize         | 67.1 ms                                                                | 63.5 ms: 1.06x faster                                                            |
| fannkuch                 | 524 ms                                                                 | 498 ms: 1.05x faster                                                             |
| django_template          | 42.8 ms                                                                | 40.9 ms: 1.05x faster                                                            |
| genshi_xml               | 61.7 ms                                                                | 59.0 ms: 1.05x faster                                                            |
| regex_compile            | 190 ms                                                                 | 182 ms: 1.05x faster                                                             |
| deltablue                | 4.39 ms                                                                | 4.21 ms: 1.04x faster                                                            |
| telco                    | 9.67 ms                                                                | 9.30 ms: 1.04x faster                                                            |
| unpickle_pure_python     | 297 us                                                                 | 286 us: 1.04x faster                                                             |
| typing_runtime_protocols | 127 us                                                                 | 123 us: 1.03x faster                                                             |
| sqlite_synth             | 3.09 us                                                                | 2.99 us: 1.03x faster                                                            |
| sqlglot_parse            | 1.55 ms                                                                | 1.50 ms: 1.03x faster                                                            |
| genshi_text              | 26.0 ms                                                                | 25.2 ms: 1.03x faster                                                            |
| sqlglot_transpile        | 1.87 ms                                                                | 1.82 ms: 1.03x faster                                                            |
| async_generators         | 489 ms                                                                 | 475 ms: 1.03x faster                                                             |
| sympy_sum                | 184 ms                                                                 | 178 ms: 1.03x faster                                                             |
| docutils                 | 3.18 sec                                                               | 3.09 sec: 1.03x faster                                                           |
| pycparser                | 1.31 sec                                                               | 1.27 sec: 1.03x faster                                                           |
| xml_etree_generate       | 95.5 ms                                                                | 92.9 ms: 1.03x faster                                                            |
| bench_thread_pool        | 904 us                                                                 | 880 us: 1.03x faster                                                             |
| logging_silent           | 106 ns                                                                 | 104 ns: 1.03x faster                                                             |
| sympy_str                | 334 ms                                                                 | 326 ms: 1.03x faster                                                             |
| regex_v8                 | 25.7 ms                                                                | 25.1 ms: 1.03x faster                                                            |
| logging_simple           | 6.56 us                                                                | 6.40 us: 1.03x faster                                                            |
| 2to3                     | 310 ms                                                                 | 303 ms: 1.03x faster                                                             |
| sqlglot_normalize        | 128 ms                                                                 | 125 ms: 1.03x faster                                                             |
| meteor_contest           | 125 ms                                                                 | 122 ms: 1.02x faster                                                             |
| xml_etree_parse          | 154 ms                                                                 | 151 ms: 1.02x faster                                                             |
| dulwich_log              | 74.6 ms                                                                | 73.2 ms: 1.02x faster                                                            |
| async_tree_none_tg       | 360 ms                                                                 | 353 ms: 1.02x faster                                                             |
| thrift                   | 842 us                                                                 | 827 us: 1.02x faster                                                             |
| pathlib                  | 18.7 ms                                                                | 18.4 ms: 1.02x faster                                                            |
| mdp                      | 2.83 sec                                                               | 2.78 sec: 1.02x faster                                                           |
| aiohttp                  | 1.25 ms                                                                | 1.23 ms: 1.02x faster                                                            |
| gunicorn                 | 1.34 ms                                                                | 1.33 ms: 1.01x faster                                                            |
| deepcopy                 | 387 us                                                                 | 381 us: 1.01x faster                                                             |
| scimark_lu               | 170 ms                                                                 | 168 ms: 1.01x faster                                                             |
| coverage                 | 98.2 ms                                                                | 97.3 ms: 1.01x faster                                                            |
| regex_dna                | 226 ms                                                                 | 224 ms: 1.01x faster                                                             |
| logging_format           | 7.34 us                                                                | 7.28 us: 1.01x faster                                                            |
| xml_etree_process        | 64.5 ms                                                                | 64.0 ms: 1.01x faster                                                            |
| sympy_integrate          | 24.1 ms                                                                | 23.9 ms: 1.01x faster                                                            |
| regex_effbot             | 3.69 ms                                                                | 3.67 ms: 1.01x faster                                                            |
| python_startup_no_site   | 7.16 ms                                                                | 7.18 ms: 1.00x slower                                                            |
| sympy_expand             | 548 ms                                                                 | 550 ms: 1.00x slower                                                             |
| python_startup           | 10.6 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.87 sec: 1.01x slower                                                           |
| scimark_sparse_mat_mult  | 6.05 ms                                                                | 6.12 ms: 1.01x slower                                                            |
| pickle_pure_python       | 314 us                                                                 | 318 us: 1.01x slower                                                             |
| json_loads               | 27.9 us                                                                | 28.2 us: 1.01x slower                                                            |
| chameleon                | 7.90 ms                                                                | 8.01 ms: 1.01x slower                                                            |
| scimark_fft              | 452 ms                                                                 | 460 ms: 1.02x slower                                                             |
| deepcopy_reduce          | 3.30 us                                                                | 3.36 us: 1.02x slower                                                            |
| unpickle_list            | 5.31 us                                                                | 5.41 us: 1.02x slower                                                            |
| spectral_norm            | 140 ms                                                                 | 142 ms: 1.02x slower                                                             |
| pickle_dict              | 34.7 us                                                                | 35.5 us: 1.02x slower                                                            |
| asyncio_tcp              | 514 ms                                                                 | 528 ms: 1.03x slower                                                             |
| pickle                   | 11.6 us                                                                | 11.9 us: 1.03x slower                                                            |
| coroutines               | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                            |
| unpickle                 | 15.1 us                                                                | 15.7 us: 1.04x slower                                                            |
| mako                     | 13.1 ms                                                                | 13.7 ms: 1.04x slower                                                            |
| gc_traversal             | 3.76 ms                                                                | 3.96 ms: 1.05x slower                                                            |
| pidigits                 | 193 ms                                                                 | 212 ms: 1.10x slower                                                             |
| Geometric mean           | (ref)                                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (24): async_tree_none, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_io, async_tree_cpu_io_mixed, pickle_list, djangocms, mypy2, async_tree_cpu_io_mixed_tg, float, go, asyncio_websockets, generators, bench_mp_pool, nbody, create_gc_cycles, html5lib, pylint, dask, json_dumps, json, xml_etree_iterparse, tornado_http

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
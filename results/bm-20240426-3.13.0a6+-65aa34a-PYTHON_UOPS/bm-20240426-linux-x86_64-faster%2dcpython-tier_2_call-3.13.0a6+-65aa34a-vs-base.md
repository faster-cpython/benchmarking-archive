# Results vs. base

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 334 ms                                                                 | 305 ms: 1.09x faster                                                    |
| chameleon      | 7.98 ms                                                                | 7.57 ms: 1.05x faster                                                   |
| html5lib       | 75.0 ms                                                                | 72.7 ms: 1.03x faster                                                   |
| tornado_http   | 105 ms                                                                 | 102 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none           | 394 ms                                                                 | 372 ms: 1.06x faster                                                    |
| async_tree_none_tg        | 365 ms                                                                 | 347 ms: 1.05x faster                                                    |
| async_tree_memoization    | 527 ms                                                                 | 503 ms: 1.05x faster                                                    |
| async_tree_io_tg          | 1.00 sec                                                               | 964 ms: 1.04x faster                                                    |
| async_tree_memoization_tg | 478 ms                                                                 | 459 ms: 1.04x faster                                                    |
| async_tree_cpu_io_mixed   | 653 ms                                                                 | 634 ms: 1.03x faster                                                    |
| async_tree_io             | 978 ms                                                                 | 957 ms: 1.02x faster                                                    |
| Geometric mean            | (ref)                                                                  | 1.04x faster                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 196 ms                                                                 | 129 ms: 1.52x faster                                                    |
| float          | 126 ms                                                                 | 91.7 ms: 1.38x faster                                                   |
| pidigits       | 194 ms                                                                 | 191 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.28x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 218 ms                                                                 | 182 ms: 1.20x faster                                                    |
| regex_v8       | 26.4 ms                                                                | 24.8 ms: 1.06x faster                                                   |
| regex_effbot   | 3.75 ms                                                                | 3.70 ms: 1.01x faster                                                   |
| regex_dna      | 226 ms                                                                 | 224 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 397 us                                                                 | 295 us: 1.35x faster                                                    |
| tomli_loads          | 3.38 sec                                                               | 2.54 sec: 1.33x faster                                                  |
| xml_etree_iterparse  | 125 ms                                                                 | 110 ms: 1.13x faster                                                    |
| xml_etree_process    | 72.5 ms                                                                | 65.2 ms: 1.11x faster                                                   |
| xml_etree_generate   | 102 ms                                                                 | 92.7 ms: 1.10x faster                                                   |
| unpickle_list        | 5.31 us                                                                | 5.17 us: 1.03x faster                                                   |
| unpickle             | 15.6 us                                                                | 15.4 us: 1.01x faster                                                   |
| pickle_list          | 5.21 us                                                                | 5.15 us: 1.01x faster                                                   |
| json_loads           | 27.8 us                                                                | 27.7 us: 1.01x faster                                                   |
| pickle_pure_python   | 319 us                                                                 | 321 us: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (4): xml_etree_parse, pickle_dict, json_dumps, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                                | 10.5 ms: 1.01x faster                                                   |
| python_startup_no_site | 7.21 ms                                                                | 7.13 ms: 1.01x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 20.2 ms                                                                | 13.9 ms: 1.45x faster                                                   |
| genshi_text     | 34.6 ms                                                                | 28.9 ms: 1.20x faster                                                   |
| genshi_xml      | 72.8 ms                                                                | 65.5 ms: 1.11x faster                                                   |
| django_template | 45.2 ms                                                                | 41.4 ms: 1.09x faster                                                   |
| Geometric mean  | (ref)                                                                  | 1.21x faster                                                            |

All benchmarks:
===============

| Benchmark                 | bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody                     | 196 ms                                                                 | 129 ms: 1.52x faster                                                    |
| spectral_norm             | 218 ms                                                                 | 144 ms: 1.51x faster                                                    |
| comprehensions            | 36.6 us                                                                | 24.7 us: 1.48x faster                                                   |
| hexiom                    | 14.9 ms                                                                | 10.2 ms: 1.47x faster                                                   |
| mako                      | 20.2 ms                                                                | 13.9 ms: 1.45x faster                                                   |
| scimark_monte_carlo       | 134 ms                                                                 | 92.1 ms: 1.45x faster                                                   |
| pyflate                   | 849 ms                                                                 | 592 ms: 1.43x faster                                                    |
| fannkuch                  | 708 ms                                                                 | 499 ms: 1.42x faster                                                    |
| float                     | 126 ms                                                                 | 91.7 ms: 1.38x faster                                                   |
| scimark_sparse_mat_mult   | 8.59 ms                                                                | 6.32 ms: 1.36x faster                                                   |
| pprint_safe_repr          | 1.29 sec                                                               | 953 ms: 1.36x faster                                                    |
| pprint_pformat            | 2.69 sec                                                               | 1.98 sec: 1.36x faster                                                  |
| nqueens                   | 149 ms                                                                 | 111 ms: 1.35x faster                                                    |
| unpickle_pure_python      | 397 us                                                                 | 295 us: 1.35x faster                                                    |
| tomli_loads               | 3.38 sec                                                               | 2.54 sec: 1.33x faster                                                  |
| crypto_pyaes              | 124 ms                                                                 | 93.6 ms: 1.32x faster                                                   |
| scimark_fft               | 596 ms                                                                 | 454 ms: 1.31x faster                                                    |
| chaos                     | 102 ms                                                                 | 79.8 ms: 1.28x faster                                                   |
| richards                  | 72.3 ms                                                                | 56.7 ms: 1.28x faster                                                   |
| richards_super            | 78.9 ms                                                                | 63.5 ms: 1.24x faster                                                   |
| regex_compile             | 218 ms                                                                 | 182 ms: 1.20x faster                                                    |
| deltablue                 | 5.32 ms                                                                | 4.45 ms: 1.20x faster                                                   |
| genshi_text               | 34.6 ms                                                                | 28.9 ms: 1.20x faster                                                   |
| scimark_lu                | 201 ms                                                                 | 168 ms: 1.20x faster                                                    |
| meteor_contest            | 144 ms                                                                 | 123 ms: 1.17x faster                                                    |
| raytrace                  | 376 ms                                                                 | 330 ms: 1.14x faster                                                    |
| xml_etree_iterparse       | 125 ms                                                                 | 110 ms: 1.13x faster                                                    |
| scimark_sor               | 179 ms                                                                 | 157 ms: 1.13x faster                                                    |
| typing_runtime_protocols  | 221 us                                                                 | 196 us: 1.13x faster                                                    |
| genshi_xml                | 72.8 ms                                                                | 65.5 ms: 1.11x faster                                                   |
| xml_etree_process         | 72.5 ms                                                                | 65.2 ms: 1.11x faster                                                   |
| xml_etree_generate        | 102 ms                                                                 | 92.7 ms: 1.10x faster                                                   |
| 2to3                      | 334 ms                                                                 | 305 ms: 1.09x faster                                                    |
| django_template           | 45.2 ms                                                                | 41.4 ms: 1.09x faster                                                   |
| sqlglot_optimize          | 71.2 ms                                                                | 65.3 ms: 1.09x faster                                                   |
| go                        | 230 ms                                                                 | 212 ms: 1.09x faster                                                    |
| pycparser                 | 1.38 sec                                                               | 1.28 sec: 1.08x faster                                                  |
| sympy_integrate           | 25.6 ms                                                                | 23.8 ms: 1.08x faster                                                   |
| logging_silent            | 108 ns                                                                 | 101 ns: 1.07x faster                                                    |
| sympy_sum                 | 192 ms                                                                 | 180 ms: 1.06x faster                                                    |
| regex_v8                  | 26.4 ms                                                                | 24.8 ms: 1.06x faster                                                   |
| async_tree_none           | 394 ms                                                                 | 372 ms: 1.06x faster                                                    |
| sqlglot_normalize         | 136 ms                                                                 | 129 ms: 1.06x faster                                                    |
| sqlglot_parse             | 1.60 ms                                                                | 1.52 ms: 1.06x faster                                                   |
| sympy_str                 | 350 ms                                                                 | 331 ms: 1.05x faster                                                    |
| sqlglot_transpile         | 1.95 ms                                                                | 1.85 ms: 1.05x faster                                                   |
| chameleon                 | 7.98 ms                                                                | 7.57 ms: 1.05x faster                                                   |
| async_tree_none_tg        | 365 ms                                                                 | 347 ms: 1.05x faster                                                    |
| deepcopy_memo             | 49.7 us                                                                | 47.3 us: 1.05x faster                                                   |
| async_tree_memoization    | 527 ms                                                                 | 503 ms: 1.05x faster                                                    |
| dulwich_log               | 77.3 ms                                                                | 73.9 ms: 1.05x faster                                                   |
| async_tree_io_tg          | 1.00 sec                                                               | 964 ms: 1.04x faster                                                    |
| mdp                       | 3.14 sec                                                               | 3.01 sec: 1.04x faster                                                  |
| async_tree_memoization_tg | 478 ms                                                                 | 459 ms: 1.04x faster                                                    |
| thrift                    | 862 us                                                                 | 833 us: 1.04x faster                                                    |
| async_generators          | 493 ms                                                                 | 477 ms: 1.03x faster                                                    |
| html5lib                  | 75.0 ms                                                                | 72.7 ms: 1.03x faster                                                   |
| bench_thread_pool         | 930 us                                                                 | 902 us: 1.03x faster                                                    |
| async_tree_cpu_io_mixed   | 653 ms                                                                 | 634 ms: 1.03x faster                                                    |
| tornado_http              | 105 ms                                                                 | 102 ms: 1.03x faster                                                    |
| logging_format            | 7.88 us                                                                | 7.66 us: 1.03x faster                                                   |
| unpickle_list             | 5.31 us                                                                | 5.17 us: 1.03x faster                                                   |
| telco                     | 9.56 ms                                                                | 9.32 ms: 1.03x faster                                                   |
| logging_simple            | 7.07 us                                                                | 6.90 us: 1.02x faster                                                   |
| djangocms                 | 33.3 us                                                                | 32.6 us: 1.02x faster                                                   |
| pathlib                   | 18.9 ms                                                                | 18.5 ms: 1.02x faster                                                   |
| async_tree_io             | 978 ms                                                                 | 957 ms: 1.02x faster                                                    |
| aiohttp                   | 1.27 ms                                                                | 1.24 ms: 1.02x faster                                                   |
| sympy_expand              | 559 ms                                                                 | 549 ms: 1.02x faster                                                    |
| gunicorn                  | 1.36 ms                                                                | 1.34 ms: 1.02x faster                                                   |
| dask                      | 395 ms                                                                 | 390 ms: 1.01x faster                                                    |
| unpickle                  | 15.6 us                                                                | 15.4 us: 1.01x faster                                                   |
| pidigits                  | 194 ms                                                                 | 191 ms: 1.01x faster                                                    |
| regex_effbot              | 3.75 ms                                                                | 3.70 ms: 1.01x faster                                                   |
| pickle_list               | 5.21 us                                                                | 5.15 us: 1.01x faster                                                   |
| python_startup            | 10.7 ms                                                                | 10.5 ms: 1.01x faster                                                   |
| python_startup_no_site    | 7.21 ms                                                                | 7.13 ms: 1.01x faster                                                   |
| regex_dna                 | 226 ms                                                                 | 224 ms: 1.01x faster                                                    |
| sqlite_synth              | 3.08 us                                                                | 3.06 us: 1.01x faster                                                   |
| coverage                  | 98.2 ms                                                                | 97.6 ms: 1.01x faster                                                   |
| asyncio_tcp               | 533 ms                                                                 | 530 ms: 1.01x faster                                                    |
| json_loads                | 27.8 us                                                                | 27.7 us: 1.01x faster                                                   |
| create_gc_cycles          | 1.79 ms                                                                | 1.78 ms: 1.00x faster                                                   |
| pickle_pure_python        | 319 us                                                                 | 321 us: 1.01x slower                                                    |
| deepcopy_reduce           | 3.31 us                                                                | 3.41 us: 1.03x slower                                                   |
| gc_traversal              | 3.83 ms                                                                | 4.05 ms: 1.06x slower                                                   |
| Geometric mean            | (ref)                                                                  | 1.11x faster                                                            |

Benchmark hidden because not significant (12): async_tree_cpu_io_mixed_tg, xml_etree_parse, generators, bench_mp_pool, deepcopy, pickle_dict, asyncio_tcp_ssl, asyncio_websockets, json_dumps, pickle, coroutines, json
Ignored benchmarks (3) of results/bm-20240425-3.13.0a6+-2c45148-PYTHON_UOPS/bm-20240425-linux-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148.json: docutils, mypy2, pylint

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.00x
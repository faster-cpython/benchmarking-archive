# Results vs. base

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 62ff43c
- commit date: 2024-05-03
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 371 ms                                                                 | 327 ms: 1.14x faster                                                    |
| chameleon      | 8.71 ms                                                                | 8.06 ms: 1.08x faster                                                   |
| html5lib       | 82.8 ms                                                                | 77.8 ms: 1.06x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none           | 401 ms                                                                 | 380 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed   | 669 ms                                                                 | 640 ms: 1.05x faster                                                    |
| async_tree_memoization    | 534 ms                                                                 | 512 ms: 1.04x faster                                                    |
| async_tree_io_tg          | 1.02 sec                                                               | 976 ms: 1.04x faster                                                    |
| async_tree_none_tg        | 370 ms                                                                 | 358 ms: 1.03x faster                                                    |
| async_tree_memoization_tg | 483 ms                                                                 | 468 ms: 1.03x faster                                                    |
| Geometric mean            | (ref)                                                                  | 1.04x faster                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 203 ms                                                                 | 122 ms: 1.67x faster                                                    |
| float          | 128 ms                                                                 | 90.6 ms: 1.42x faster                                                   |
| pidigits       | 195 ms                                                                 | 196 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.33x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 238 ms                                                                 | 190 ms: 1.25x faster                                                    |
| regex_v8       | 25.4 ms                                                                | 25.6 ms: 1.01x slower                                                   |
| regex_dna      | 222 ms                                                                 | 227 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_pure_python | 402 us                                                                 | 285 us: 1.41x faster                                                    |
| tomli_loads          | 3.60 sec                                                               | 2.65 sec: 1.36x faster                                                  |
| xml_etree_generate   | 116 ms                                                                 | 97.6 ms: 1.19x faster                                                   |
| xml_etree_process    | 80.3 ms                                                                | 68.4 ms: 1.17x faster                                                   |
| xml_etree_iterparse  | 127 ms                                                                 | 111 ms: 1.15x faster                                                    |
| pickle_dict          | 36.1 us                                                                | 34.0 us: 1.06x faster                                                   |
| pickle               | 12.2 us                                                                | 11.9 us: 1.03x faster                                                   |
| xml_etree_parse      | 155 ms                                                                 | 152 ms: 1.02x faster                                                    |
| unpickle_list        | 5.28 us                                                                | 5.23 us: 1.01x faster                                                   |
| json_loads           | 27.7 us                                                                | 27.8 us: 1.01x slower                                                   |
| pickle_list          | 5.07 us                                                                | 5.13 us: 1.01x slower                                                   |
| json_dumps           | 10.9 ms                                                                | 11.1 ms: 1.02x slower                                                   |
| pickle_pure_python   | 329 us                                                                 | 405 us: 1.23x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.20 ms                                                                | 7.23 ms: 1.00x slower                                                   |
| python_startup         | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                   |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 20.8 ms                                                                | 14.0 ms: 1.49x faster                                                   |
| genshi_text     | 39.3 ms                                                                | 32.0 ms: 1.23x faster                                                   |
| genshi_xml      | 81.8 ms                                                                | 72.9 ms: 1.12x faster                                                   |
| django_template | 46.5 ms                                                                | 44.5 ms: 1.05x faster                                                   |
| Geometric mean  | (ref)                                                                  | 1.21x faster                                                            |

All benchmarks:
===============

| Benchmark                 | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|---------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody                     | 203 ms                                                                 | 122 ms: 1.67x faster                                                    |
| hexiom                    | 15.2 ms                                                                | 9.66 ms: 1.58x faster                                                   |
| spectral_norm             | 217 ms                                                                 | 140 ms: 1.55x faster                                                    |
| comprehensions            | 38.1 us                                                                | 25.1 us: 1.52x faster                                                   |
| scimark_monte_carlo       | 137 ms                                                                 | 90.1 ms: 1.52x faster                                                   |
| mako                      | 20.8 ms                                                                | 14.0 ms: 1.49x faster                                                   |
| fannkuch                  | 715 ms                                                                 | 487 ms: 1.47x faster                                                    |
| scimark_sparse_mat_mult   | 8.87 ms                                                                | 6.17 ms: 1.44x faster                                                   |
| float                     | 128 ms                                                                 | 90.6 ms: 1.42x faster                                                   |
| unpickle_pure_python      | 402 us                                                                 | 285 us: 1.41x faster                                                    |
| richards                  | 82.9 ms                                                                | 59.4 ms: 1.40x faster                                                   |
| crypto_pyaes              | 128 ms                                                                 | 91.9 ms: 1.39x faster                                                   |
| pyflate                   | 839 ms                                                                 | 609 ms: 1.38x faster                                                    |
| scimark_fft               | 606 ms                                                                 | 443 ms: 1.37x faster                                                    |
| tomli_loads               | 3.60 sec                                                               | 2.65 sec: 1.36x faster                                                  |
| richards_super            | 89.2 ms                                                                | 66.6 ms: 1.34x faster                                                   |
| nqueens                   | 146 ms                                                                 | 109 ms: 1.34x faster                                                    |
| pprint_pformat            | 2.67 sec                                                               | 1.99 sec: 1.34x faster                                                  |
| pprint_safe_repr          | 1.29 sec                                                               | 968 ms: 1.33x faster                                                    |
| regex_compile             | 238 ms                                                                 | 190 ms: 1.25x faster                                                    |
| genshi_text               | 39.3 ms                                                                | 32.0 ms: 1.23x faster                                                   |
| chaos                     | 103 ms                                                                 | 84.4 ms: 1.22x faster                                                   |
| deltablue                 | 5.31 ms                                                                | 4.37 ms: 1.21x faster                                                   |
| scimark_lu                | 202 ms                                                                 | 167 ms: 1.21x faster                                                    |
| meteor_contest            | 147 ms                                                                 | 123 ms: 1.19x faster                                                    |
| xml_etree_generate        | 116 ms                                                                 | 97.6 ms: 1.19x faster                                                   |
| xml_etree_process         | 80.3 ms                                                                | 68.4 ms: 1.17x faster                                                   |
| raytrace                  | 383 ms                                                                 | 331 ms: 1.16x faster                                                    |
| go                        | 208 ms                                                                 | 181 ms: 1.15x faster                                                    |
| xml_etree_iterparse       | 127 ms                                                                 | 111 ms: 1.15x faster                                                    |
| 2to3                      | 371 ms                                                                 | 327 ms: 1.14x faster                                                    |
| gc_traversal              | 4.10 ms                                                                | 3.62 ms: 1.14x faster                                                   |
| scimark_sor               | 180 ms                                                                 | 159 ms: 1.13x faster                                                    |
| sympy_integrate           | 28.0 ms                                                                | 24.8 ms: 1.13x faster                                                   |
| genshi_xml                | 81.8 ms                                                                | 72.9 ms: 1.12x faster                                                   |
| typing_runtime_protocols  | 214 us                                                                 | 194 us: 1.11x faster                                                    |
| sqlglot_optimize          | 73.4 ms                                                                | 66.6 ms: 1.10x faster                                                   |
| mdp                       | 3.09 sec                                                               | 2.81 sec: 1.10x faster                                                  |
| bench_thread_pool         | 994 us                                                                 | 914 us: 1.09x faster                                                    |
| chameleon                 | 8.71 ms                                                                | 8.06 ms: 1.08x faster                                                   |
| sympy_sum                 | 197 ms                                                                 | 184 ms: 1.07x faster                                                    |
| async_generators          | 503 ms                                                                 | 471 ms: 1.07x faster                                                    |
| sympy_str                 | 367 ms                                                                 | 344 ms: 1.07x faster                                                    |
| html5lib                  | 82.8 ms                                                                | 77.8 ms: 1.06x faster                                                   |
| pickle_dict               | 36.1 us                                                                | 34.0 us: 1.06x faster                                                   |
| async_tree_none           | 401 ms                                                                 | 380 ms: 1.05x faster                                                    |
| generators                | 32.0 ms                                                                | 30.6 ms: 1.05x faster                                                   |
| django_template           | 46.5 ms                                                                | 44.5 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed   | 669 ms                                                                 | 640 ms: 1.05x faster                                                    |
| sqlite_synth              | 3.13 us                                                                | 3.00 us: 1.04x faster                                                   |
| async_tree_memoization    | 534 ms                                                                 | 512 ms: 1.04x faster                                                    |
| sympy_expand              | 602 ms                                                                 | 578 ms: 1.04x faster                                                    |
| async_tree_io_tg          | 1.02 sec                                                               | 976 ms: 1.04x faster                                                    |
| dulwich_log               | 78.2 ms                                                                | 75.5 ms: 1.04x faster                                                   |
| async_tree_none_tg        | 370 ms                                                                 | 358 ms: 1.03x faster                                                    |
| pickle                    | 12.2 us                                                                | 11.9 us: 1.03x faster                                                   |
| async_tree_memoization_tg | 483 ms                                                                 | 468 ms: 1.03x faster                                                    |
| logging_simple            | 6.76 us                                                                | 6.55 us: 1.03x faster                                                   |
| mypy2                     | 881 ms                                                                 | 859 ms: 1.03x faster                                                    |
| sqlglot_normalize         | 140 ms                                                                 | 137 ms: 1.03x faster                                                    |
| xml_etree_parse           | 155 ms                                                                 | 152 ms: 1.02x faster                                                    |
| logging_format            | 7.45 us                                                                | 7.30 us: 1.02x faster                                                   |
| coverage                  | 93.7 ms                                                                | 92.7 ms: 1.01x faster                                                   |
| pathlib                   | 18.8 ms                                                                | 18.6 ms: 1.01x faster                                                   |
| telco                     | 9.69 ms                                                                | 9.60 ms: 1.01x faster                                                   |
| unpickle_list             | 5.28 us                                                                | 5.23 us: 1.01x faster                                                   |
| asyncio_websockets        | 568 ms                                                                 | 563 ms: 1.01x faster                                                    |
| asyncio_tcp               | 534 ms                                                                 | 532 ms: 1.00x faster                                                    |
| asyncio_tcp_ssl           | 1.88 sec                                                               | 1.87 sec: 1.00x faster                                                  |
| pidigits                  | 195 ms                                                                 | 196 ms: 1.00x slower                                                    |
| python_startup_no_site    | 7.20 ms                                                                | 7.23 ms: 1.00x slower                                                   |
| json_loads                | 27.7 us                                                                | 27.8 us: 1.01x slower                                                   |
| python_startup            | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                   |
| regex_v8                  | 25.4 ms                                                                | 25.6 ms: 1.01x slower                                                   |
| pickle_list               | 5.07 us                                                                | 5.13 us: 1.01x slower                                                   |
| thrift                    | 839 us                                                                 | 851 us: 1.01x slower                                                    |
| json                      | 5.16 ms                                                                | 5.24 ms: 1.02x slower                                                   |
| json_dumps                | 10.9 ms                                                                | 11.1 ms: 1.02x slower                                                   |
| regex_dna                 | 222 ms                                                                 | 227 ms: 1.02x slower                                                    |
| deepcopy_memo             | 50.3 us                                                                | 51.4 us: 1.02x slower                                                   |
| coroutines                | 24.3 ms                                                                | 24.9 ms: 1.03x slower                                                   |
| sqlglot_parse             | 1.62 ms                                                                | 1.67 ms: 1.03x slower                                                   |
| sqlglot_transpile         | 1.97 ms                                                                | 2.05 ms: 1.04x slower                                                   |
| pycparser                 | 1.34 sec                                                               | 1.42 sec: 1.06x slower                                                  |
| deepcopy_reduce           | 3.36 us                                                                | 3.84 us: 1.14x slower                                                   |
| deepcopy                  | 401 us                                                                 | 459 us: 1.15x slower                                                    |
| pickle_pure_python        | 329 us                                                                 | 405 us: 1.23x slower                                                    |
| logging_silent            | 113 ns                                                                 | 146 ns: 1.30x slower                                                    |
| Geometric mean            | (ref)                                                                  | 1.10x faster                                                            |

Benchmark hidden because not significant (12): pylint, async_tree_cpu_io_mixed_tg, async_tree_io, djangocms, aiohttp, tornado_http, regex_effbot, bench_mp_pool, create_gc_cycles, dask, gunicorn, unpickle

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.00x
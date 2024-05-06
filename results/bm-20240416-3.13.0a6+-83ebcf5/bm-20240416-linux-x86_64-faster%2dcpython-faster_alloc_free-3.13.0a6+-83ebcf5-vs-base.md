# Results vs. base

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: 83ebcf5
- commit date: 2024-04-16
- overall geometric mean: 1.00x slower
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 270 ms                                                                 | 271 ms: 1.00x slower                                                          |
| chameleon      | 6.94 ms                                                                | 7.07 ms: 1.02x slower                                                         |
| html5lib       | 67.3 ms                                                                | 68.2 ms: 1.01x slower                                                         |
| tornado_http   | 93.9 ms                                                                | 94.1 ms: 1.00x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 206 ms                                                                 | 190 ms: 1.09x faster                                                          |
| float          | 78.7 ms                                                                | 79.8 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                  |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 25.4 ms                                                                | 24.8 ms: 1.03x faster                                                         |
| regex_effbot   | 3.74 ms                                                                | 3.65 ms: 1.02x faster                                                         |
| regex_compile  | 136 ms                                                                 | 137 ms: 1.01x slower                                                          |
| regex_dna      | 218 ms                                                                 | 226 ms: 1.04x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_list          | 5.33 us                                                                | 5.03 us: 1.06x faster                                                         |
| pickle_dict          | 35.4 us                                                                | 33.9 us: 1.04x faster                                                         |
| pickle               | 11.8 us                                                                | 11.5 us: 1.03x faster                                                         |
| unpickle             | 15.2 us                                                                | 15.1 us: 1.01x faster                                                         |
| xml_etree_generate   | 88.8 ms                                                                | 88.5 ms: 1.00x faster                                                         |
| xml_etree_process    | 60.8 ms                                                                | 61.2 ms: 1.01x slower                                                         |
| json_dumps           | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                         |
| pickle_pure_python   | 299 us                                                                 | 302 us: 1.01x slower                                                          |
| json_loads           | 27.6 us                                                                | 28.0 us: 1.01x slower                                                         |
| tomli_loads          | 2.17 sec                                                               | 2.22 sec: 1.02x slower                                                        |
| unpickle_pure_python | 217 us                                                                 | 223 us: 1.02x slower                                                          |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                  |

Benchmark hidden because not significant (3): unpickle_list, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.11 ms                                                                | 7.09 ms: 1.00x faster                                                         |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.1 ms                                                                | 11.0 ms: 1.01x faster                                                         |
| django_template | 35.8 ms                                                                | 35.6 ms: 1.01x faster                                                         |
| genshi_text     | 23.4 ms                                                                | 23.8 ms: 1.01x slower                                                         |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits                 | 206 ms                                                                 | 190 ms: 1.09x faster                                                          |
| pickle_list              | 5.33 us                                                                | 5.03 us: 1.06x faster                                                         |
| pickle_dict              | 35.4 us                                                                | 33.9 us: 1.04x faster                                                         |
| generators               | 30.9 ms                                                                | 30.1 ms: 1.03x faster                                                         |
| gc_traversal             | 3.87 ms                                                                | 3.76 ms: 1.03x faster                                                         |
| regex_v8                 | 25.4 ms                                                                | 24.8 ms: 1.03x faster                                                         |
| pickle                   | 11.8 us                                                                | 11.5 us: 1.03x faster                                                         |
| regex_effbot             | 3.74 ms                                                                | 3.65 ms: 1.02x faster                                                         |
| typing_runtime_protocols | 115 us                                                                 | 113 us: 1.02x faster                                                          |
| create_gc_cycles         | 1.75 ms                                                                | 1.73 ms: 1.01x faster                                                         |
| coverage                 | 98.6 ms                                                                | 97.6 ms: 1.01x faster                                                         |
| mako                     | 11.1 ms                                                                | 11.0 ms: 1.01x faster                                                         |
| crypto_pyaes             | 76.3 ms                                                                | 75.6 ms: 1.01x faster                                                         |
| thrift                   | 818 us                                                                 | 811 us: 1.01x faster                                                          |
| django_template          | 35.8 ms                                                                | 35.6 ms: 1.01x faster                                                         |
| unpickle                 | 15.2 us                                                                | 15.1 us: 1.01x faster                                                         |
| asyncio_tcp              | 507 ms                                                                 | 505 ms: 1.00x faster                                                          |
| bench_thread_pool        | 841 us                                                                 | 838 us: 1.00x faster                                                          |
| xml_etree_generate       | 88.8 ms                                                                | 88.5 ms: 1.00x faster                                                         |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.84 sec: 1.00x faster                                                        |
| python_startup_no_site   | 7.11 ms                                                                | 7.09 ms: 1.00x faster                                                         |
| raytrace                 | 264 ms                                                                 | 265 ms: 1.00x slower                                                          |
| tornado_http             | 93.9 ms                                                                | 94.1 ms: 1.00x slower                                                         |
| 2to3                     | 270 ms                                                                 | 271 ms: 1.00x slower                                                          |
| richards_super           | 53.7 ms                                                                | 54.0 ms: 1.00x slower                                                         |
| pathlib                  | 17.5 ms                                                                | 17.6 ms: 1.01x slower                                                         |
| async_generators         | 445 ms                                                                 | 448 ms: 1.01x slower                                                          |
| pprint_pformat           | 1.53 sec                                                               | 1.54 sec: 1.01x slower                                                        |
| richards                 | 47.9 ms                                                                | 48.2 ms: 1.01x slower                                                         |
| sqlglot_optimize         | 55.6 ms                                                                | 56.0 ms: 1.01x slower                                                         |
| xml_etree_process        | 60.8 ms                                                                | 61.2 ms: 1.01x slower                                                         |
| sympy_str                | 282 ms                                                                 | 284 ms: 1.01x slower                                                          |
| deepcopy_reduce          | 3.23 us                                                                | 3.26 us: 1.01x slower                                                         |
| sympy_sum                | 157 ms                                                                 | 158 ms: 1.01x slower                                                          |
| nqueens                  | 81.7 ms                                                                | 82.4 ms: 1.01x slower                                                         |
| sympy_expand             | 475 ms                                                                 | 479 ms: 1.01x slower                                                          |
| deltablue                | 3.26 ms                                                                | 3.29 ms: 1.01x slower                                                         |
| json_dumps               | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                         |
| sympy_integrate          | 20.3 ms                                                                | 20.6 ms: 1.01x slower                                                         |
| pickle_pure_python       | 299 us                                                                 | 302 us: 1.01x slower                                                          |
| regex_compile            | 136 ms                                                                 | 137 ms: 1.01x slower                                                          |
| json                     | 5.15 ms                                                                | 5.21 ms: 1.01x slower                                                         |
| sqlite_synth             | 2.93 us                                                                | 2.97 us: 1.01x slower                                                         |
| html5lib                 | 67.3 ms                                                                | 68.2 ms: 1.01x slower                                                         |
| deepcopy                 | 356 us                                                                 | 361 us: 1.01x slower                                                          |
| scimark_sor              | 123 ms                                                                 | 125 ms: 1.01x slower                                                          |
| genshi_text              | 23.4 ms                                                                | 23.8 ms: 1.01x slower                                                         |
| float                    | 78.7 ms                                                                | 79.8 ms: 1.01x slower                                                         |
| json_loads               | 27.6 us                                                                | 28.0 us: 1.01x slower                                                         |
| coroutines               | 22.7 ms                                                                | 23.2 ms: 1.02x slower                                                         |
| chameleon                | 6.94 ms                                                                | 7.07 ms: 1.02x slower                                                         |
| deepcopy_memo            | 37.7 us                                                                | 38.5 us: 1.02x slower                                                         |
| comprehensions           | 16.9 us                                                                | 17.2 us: 1.02x slower                                                         |
| fannkuch                 | 391 ms                                                                 | 399 ms: 1.02x slower                                                          |
| tomli_loads              | 2.17 sec                                                               | 2.22 sec: 1.02x slower                                                        |
| pycparser                | 1.15 sec                                                               | 1.18 sec: 1.02x slower                                                        |
| spectral_norm            | 113 ms                                                                 | 115 ms: 1.02x slower                                                          |
| unpickle_pure_python     | 217 us                                                                 | 223 us: 1.02x slower                                                          |
| mdp                      | 2.60 sec                                                               | 2.67 sec: 1.03x slower                                                        |
| scimark_fft              | 369 ms                                                                 | 380 ms: 1.03x slower                                                          |
| scimark_monte_carlo      | 68.4 ms                                                                | 70.3 ms: 1.03x slower                                                         |
| chaos                    | 60.2 ms                                                                | 62.2 ms: 1.03x slower                                                         |
| regex_dna                | 218 ms                                                                 | 226 ms: 1.04x slower                                                          |
| telco                    | 8.55 ms                                                                | 8.85 ms: 1.04x slower                                                         |
| scimark_lu               | 117 ms                                                                 | 121 ms: 1.04x slower                                                          |
| scimark_sparse_mat_mult  | 5.20 ms                                                                | 5.46 ms: 1.05x slower                                                         |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                                  |

Benchmark hidden because not significant (35): async_tree_io, dask, async_tree_cpu_io_mixed, genshi_xml, hexiom, async_tree_cpu_io_mixed_tg, pyflate, bench_mp_pool, logging_simple, unpickle_list, dulwich_log, asyncio_websockets, async_tree_none_tg, xml_etree_parse, go, aiohttp, sqlglot_transpile, python_startup, async_tree_memoization_tg, sqlglot_parse, sqlglot_normalize, gunicorn, pprint_safe_repr, pylint, docutils, logging_silent, async_tree_io_tg, meteor_contest, xml_etree_iterparse, async_tree_memoization, nbody, logging_format, djangocms, mypy2, async_tree_none

# HPT report

- Reliability score: 99.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
# Results vs. base

- fork: gaogaotiantian
- ref: optimize_sys_settrac
- machine: linux-x86_64
- commit hash: a65be06
- commit date: 2024-03-27
- overall geometric mean: 1.00x slower
- HPT reliability: 99.12%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5+-262fb91 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 277 ms                                                                 | 280 ms: 1.01x slower                                                           |
| docutils       | 2.88 sec                                                               | 2.89 sec: 1.00x slower                                                         |
| html5lib       | 67.3 ms                                                                | 68.0 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                   |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5+-262fb91 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 388 ms                                                                 | 357 ms: 1.09x faster                                                           |
| async_tree_io_tg           | 923 ms                                                                 | 900 ms: 1.03x faster                                                           |
| async_tree_cpu_io_mixed_tg | 583 ms                                                                 | 596 ms: 1.02x slower                                                           |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                                   |

Benchmark hidden because not significant (5): async_tree_io, async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5+-262fb91 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 76.9 ms                                                                | 76.4 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                   |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5+-262fb91 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.80 ms                                                                | 3.62 ms: 1.05x faster                                                          |
| regex_dna      | 226 ms                                                                 | 219 ms: 1.03x faster                                                           |
| regex_v8       | 25.9 ms                                                                | 25.5 ms: 1.02x faster                                                          |
| regex_compile  | 146 ms                                                                 | 147 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5+-262fb91 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_list          | 5.20 us                                                                | 5.04 us: 1.03x faster                                                          |
| unpickle_list        | 5.19 us                                                                | 5.21 us: 1.00x slower                                                          |
| xml_etree_iterparse  | 107 ms                                                                 | 108 ms: 1.00x slower                                                           |
| pickle               | 11.9 us                                                                | 11.9 us: 1.01x slower                                                          |
| xml_etree_process    | 60.2 ms                                                                | 60.8 ms: 1.01x slower                                                          |
| xml_etree_generate   | 87.7 ms                                                                | 88.8 ms: 1.01x slower                                                          |
| unpickle_pure_python | 240 us                                                                 | 245 us: 1.02x slower                                                           |
| xml_etree_parse      | 159 ms                                                                 | 162 ms: 1.02x slower                                                           |
| pickle_pure_python   | 305 us                                                                 | 311 us: 1.02x slower                                                           |
| json_loads           | 28.5 us                                                                | 29.3 us: 1.03x slower                                                          |
| json_dumps           | 10.4 ms                                                                | 10.7 ms: 1.03x slower                                                          |
| pickle_dict          | 34.4 us                                                                | 36.0 us: 1.04x slower                                                          |
| unpickle             | 14.7 us                                                                | 15.5 us: 1.05x slower                                                          |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                                   |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5+-262fb91 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 9.53 ms                                                                | 9.56 ms: 1.00x slower                                                          |
| python_startup         | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                          |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5+-262fb91 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.8 ms                                                                | 10.9 ms: 1.00x slower                                                          |
| django_template | 35.6 ms                                                                | 36.0 ms: 1.01x slower                                                          |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                                   |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240327-linux-x86_64-python-262fb911ab7df8e890eb-3.13.0a5+-262fb91 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpack_sequence            | 94.4 ns                                                                | 85.5 ns: 1.10x faster                                                          |
| async_tree_none            | 388 ms                                                                 | 357 ms: 1.09x faster                                                           |
| regex_effbot               | 3.80 ms                                                                | 3.62 ms: 1.05x faster                                                          |
| regex_dna                  | 226 ms                                                                 | 219 ms: 1.03x faster                                                           |
| pickle_list                | 5.20 us                                                                | 5.04 us: 1.03x faster                                                          |
| pycparser                  | 1.22 sec                                                               | 1.19 sec: 1.03x faster                                                         |
| async_tree_io_tg           | 923 ms                                                                 | 900 ms: 1.03x faster                                                           |
| typing_runtime_protocols   | 113 us                                                                 | 111 us: 1.02x faster                                                           |
| coroutines                 | 23.1 ms                                                                | 22.8 ms: 1.02x faster                                                          |
| chaos                      | 64.4 ms                                                                | 63.4 ms: 1.02x faster                                                          |
| crypto_pyaes               | 76.0 ms                                                                | 74.8 ms: 1.02x faster                                                          |
| regex_v8                   | 25.9 ms                                                                | 25.5 ms: 1.02x faster                                                          |
| telco                      | 8.68 ms                                                                | 8.59 ms: 1.01x faster                                                          |
| go                         | 156 ms                                                                 | 155 ms: 1.01x faster                                                           |
| asyncio_tcp                | 510 ms                                                                 | 506 ms: 1.01x faster                                                           |
| float                      | 76.9 ms                                                                | 76.4 ms: 1.01x faster                                                          |
| deepcopy_reduce            | 3.23 us                                                                | 3.21 us: 1.01x faster                                                          |
| pathlib                    | 18.9 ms                                                                | 18.8 ms: 1.01x faster                                                          |
| asyncio_tcp_ssl            | 1.86 sec                                                               | 1.85 sec: 1.00x faster                                                         |
| python_startup_no_site     | 9.53 ms                                                                | 9.56 ms: 1.00x slower                                                          |
| unpickle_list              | 5.19 us                                                                | 5.21 us: 1.00x slower                                                          |
| python_startup             | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                          |
| xml_etree_iterparse        | 107 ms                                                                 | 108 ms: 1.00x slower                                                           |
| mako                       | 10.8 ms                                                                | 10.9 ms: 1.00x slower                                                          |
| docutils                   | 2.88 sec                                                               | 2.89 sec: 1.00x slower                                                         |
| sympy_integrate            | 21.8 ms                                                                | 21.9 ms: 1.00x slower                                                          |
| scimark_fft                | 342 ms                                                                 | 343 ms: 1.01x slower                                                           |
| spectral_norm              | 114 ms                                                                 | 115 ms: 1.01x slower                                                           |
| sympy_expand               | 492 ms                                                                 | 495 ms: 1.01x slower                                                           |
| pickle                     | 11.9 us                                                                | 11.9 us: 1.01x slower                                                          |
| deepcopy                   | 358 us                                                                 | 360 us: 1.01x slower                                                           |
| coverage                   | 97.4 ms                                                                | 98.1 ms: 1.01x slower                                                          |
| pyflate                    | 484 ms                                                                 | 488 ms: 1.01x slower                                                           |
| bench_thread_pool          | 853 us                                                                 | 860 us: 1.01x slower                                                           |
| json                       | 5.35 ms                                                                | 5.40 ms: 1.01x slower                                                          |
| regex_compile              | 146 ms                                                                 | 147 ms: 1.01x slower                                                           |
| 2to3                       | 277 ms                                                                 | 280 ms: 1.01x slower                                                           |
| sqlglot_parse              | 1.33 ms                                                                | 1.34 ms: 1.01x slower                                                          |
| xml_etree_process          | 60.2 ms                                                                | 60.8 ms: 1.01x slower                                                          |
| html5lib                   | 67.3 ms                                                                | 68.0 ms: 1.01x slower                                                          |
| sqlglot_transpile          | 1.64 ms                                                                | 1.66 ms: 1.01x slower                                                          |
| generators                 | 29.8 ms                                                                | 30.1 ms: 1.01x slower                                                          |
| django_template            | 35.6 ms                                                                | 36.0 ms: 1.01x slower                                                          |
| sympy_sum                  | 164 ms                                                                 | 166 ms: 1.01x slower                                                           |
| aiohttp                    | 1.20 ms                                                                | 1.22 ms: 1.01x slower                                                          |
| xml_etree_generate         | 87.7 ms                                                                | 88.8 ms: 1.01x slower                                                          |
| sqlglot_optimize           | 57.2 ms                                                                | 58.0 ms: 1.01x slower                                                          |
| meteor_contest             | 111 ms                                                                 | 112 ms: 1.02x slower                                                           |
| async_generators           | 457 ms                                                                 | 464 ms: 1.02x slower                                                           |
| unpickle_pure_python       | 240 us                                                                 | 245 us: 1.02x slower                                                           |
| xml_etree_parse            | 159 ms                                                                 | 162 ms: 1.02x slower                                                           |
| raytrace                   | 290 ms                                                                 | 296 ms: 1.02x slower                                                           |
| sqlglot_normalize          | 111 ms                                                                 | 114 ms: 1.02x slower                                                           |
| pickle_pure_python         | 305 us                                                                 | 311 us: 1.02x slower                                                           |
| async_tree_cpu_io_mixed_tg | 583 ms                                                                 | 596 ms: 1.02x slower                                                           |
| hexiom                     | 7.13 ms                                                                | 7.29 ms: 1.02x slower                                                          |
| json_loads                 | 28.5 us                                                                | 29.3 us: 1.03x slower                                                          |
| thrift                     | 810 us                                                                 | 831 us: 1.03x slower                                                           |
| richards_super             | 51.8 ms                                                                | 53.2 ms: 1.03x slower                                                          |
| deltablue                  | 3.43 ms                                                                | 3.53 ms: 1.03x slower                                                          |
| richards                   | 45.8 ms                                                                | 47.2 ms: 1.03x slower                                                          |
| json_dumps                 | 10.4 ms                                                                | 10.7 ms: 1.03x slower                                                          |
| djangocms                  | 31.1 us                                                                | 32.0 us: 1.03x slower                                                          |
| fannkuch                   | 391 ms                                                                 | 403 ms: 1.03x slower                                                           |
| logging_silent             | 101 ns                                                                 | 105 ns: 1.03x slower                                                           |
| pickle_dict                | 34.4 us                                                                | 36.0 us: 1.04x slower                                                          |
| unpickle                   | 14.7 us                                                                | 15.5 us: 1.05x slower                                                          |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                                   |

Benchmark hidden because not significant (35): async_tree_io, pprint_pformat, genshi_xml, chameleon, scimark_lu, genshi_text, bench_mp_pool, scimark_monte_carlo, deepcopy_memo, nqueens, create_gc_cycles, gc_traversal, asyncio_websockets, pidigits, scimark_sor, dulwich_log, async_tree_memoization_tg, comprehensions, sqlite_synth, sympy_str, mdp, logging_format, tornado_http, nbody, pprint_safe_repr, pylint, logging_simple, gunicorn, tomli_loads, scimark_sparse_mat_mult, dask, mypy2, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none_tg

# HPT report

- Reliability score: 99.12% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
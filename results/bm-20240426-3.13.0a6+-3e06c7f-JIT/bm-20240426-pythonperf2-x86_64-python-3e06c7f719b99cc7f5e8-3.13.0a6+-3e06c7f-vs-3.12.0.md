# Results vs. 3.12.0

- fork: python
- ref: 3e06c7f719b99cc7f5e8
- machine: linux-x86_64
- commit hash: 3e06c7f
- commit date: 2024-04-26
- overall geometric mean: 1.02x slower
- HPT reliability: 98.69%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 304 ms: 1.06x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.58 ms: 1.05x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.10 sec: 1.08x slower                                                       |
| tornado_http   | 121 ms                                                       | 124 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 424 ms: 1.27x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 343 ms: 1.26x faster                                                         |
| async_tree_none            | 452 ms                                                       | 376 ms: 1.20x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 881 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 595 ms: 1.17x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 472 ms: 1.15x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 909 ms: 1.15x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 622 ms: 1.12x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.19x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                         |
| float          | 76.6 ms                                                      | 76.2 ms: 1.01x faster                                                        |
| nbody          | 88.0 ms                                                      | 99.1 ms: 1.13x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.44 ms: 1.04x faster                                                        |
| regex_compile  | 144 ms                                                       | 143 ms: 1.01x faster                                                         |
| regex_dna      | 239 ms                                                       | 240 ms: 1.01x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                        | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.8 us: 1.06x faster                                                        |
| xml_etree_generate   | 86.1 ms                                                      | 83.6 ms: 1.03x faster                                                        |
| pickle               | 10.5 us                                                      | 10.3 us: 1.02x faster                                                        |
| pickle_pure_python   | 318 us                                                       | 312 us: 1.02x faster                                                         |
| tomli_loads          | 2.16 sec                                                     | 2.12 sec: 1.02x faster                                                       |
| xml_etree_iterparse  | 103 ms                                                       | 101 ms: 1.01x faster                                                         |
| xml_etree_parse      | 144 ms                                                       | 143 ms: 1.01x faster                                                         |
| unpickle_list        | 4.66 us                                                      | 4.64 us: 1.00x faster                                                        |
| pickle_list          | 4.43 us                                                      | 4.50 us: 1.02x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.1 us: 1.02x slower                                                        |
| json_loads           | 24.4 us                                                      | 24.9 us: 1.02x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 223 us: 1.06x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 9.44 ms: 1.09x slower                                                        |
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.13x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.84 ms: 1.02x faster                                                        |
| django_template | 38.2 ms                                                      | 41.4 ms: 1.09x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 424 ms: 1.27x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 343 ms: 1.26x faster                                                         |
| async_tree_none            | 452 ms                                                       | 376 ms: 1.20x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 881 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 595 ms: 1.17x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 472 ms: 1.15x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 909 ms: 1.15x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 622 ms: 1.12x faster                                                         |
| comprehensions             | 21.9 us                                                      | 19.6 us: 1.12x faster                                                        |
| generators                 | 37.4 ms                                                      | 34.3 ms: 1.09x faster                                                        |
| raytrace                   | 298 ms                                                       | 275 ms: 1.08x faster                                                         |
| pathlib                    | 18.9 ms                                                      | 17.5 ms: 1.08x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.00 us: 1.07x faster                                                        |
| pickle_dict                | 32.5 us                                                      | 30.8 us: 1.06x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 21.9 ms: 1.05x faster                                                        |
| logging_simple             | 6.71 us                                                      | 6.42 us: 1.05x faster                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.67 us: 1.04x faster                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.44 ms: 1.04x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 77.8 ms: 1.03x faster                                                        |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.08 ms: 1.03x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 83.6 ms: 1.03x faster                                                        |
| pickle                     | 10.5 us                                                      | 10.3 us: 1.02x faster                                                        |
| async_generators           | 390 ms                                                       | 382 ms: 1.02x faster                                                         |
| pickle_pure_python         | 318 us                                                       | 312 us: 1.02x faster                                                         |
| mako                       | 10.0 ms                                                      | 9.84 ms: 1.02x faster                                                        |
| tomli_loads                | 2.16 sec                                                     | 2.12 sec: 1.02x faster                                                       |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                         |
| xml_etree_iterparse        | 103 ms                                                       | 101 ms: 1.01x faster                                                         |
| regex_compile              | 144 ms                                                       | 143 ms: 1.01x faster                                                         |
| xml_etree_parse            | 144 ms                                                       | 143 ms: 1.01x faster                                                         |
| asyncio_tcp                | 378 ms                                                       | 376 ms: 1.01x faster                                                         |
| float                      | 76.6 ms                                                      | 76.2 ms: 1.01x faster                                                        |
| unpickle_list              | 4.66 us                                                      | 4.64 us: 1.00x faster                                                        |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.00x faster                                                       |
| logging_silent             | 94.4 ns                                                      | 94.8 ns: 1.00x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.58 sec: 1.00x slower                                                       |
| regex_dna                  | 239 ms                                                       | 240 ms: 1.01x slower                                                         |
| spectral_norm              | 91.6 ms                                                      | 92.8 ms: 1.01x slower                                                        |
| pickle_list                | 4.43 us                                                      | 4.50 us: 1.02x slower                                                        |
| richards                   | 45.7 ms                                                      | 46.6 ms: 1.02x slower                                                        |
| sympy_sum                  | 162 ms                                                       | 165 ms: 1.02x slower                                                         |
| unpickle                   | 14.8 us                                                      | 15.1 us: 1.02x slower                                                        |
| tornado_http               | 121 ms                                                       | 124 ms: 1.02x slower                                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 70.5 ms: 1.02x slower                                                        |
| json_loads                 | 24.4 us                                                      | 24.9 us: 1.02x slower                                                        |
| chaos                      | 64.0 ms                                                      | 65.5 ms: 1.02x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 67.0 ms: 1.02x slower                                                        |
| sqlglot_transpile          | 1.78 ms                                                      | 1.82 ms: 1.03x slower                                                        |
| scimark_fft                | 301 ms                                                       | 309 ms: 1.03x slower                                                         |
| pprint_safe_repr           | 807 ms                                                       | 830 ms: 1.03x slower                                                         |
| richards_super             | 51.3 ms                                                      | 52.8 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.70 sec: 1.03x slower                                                       |
| sqlglot_parse              | 1.38 ms                                                      | 1.42 ms: 1.03x slower                                                        |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                                        |
| deepcopy_reduce            | 3.37 us                                                      | 3.48 us: 1.03x slower                                                        |
| pycparser                  | 1.23 sec                                                     | 1.28 sec: 1.04x slower                                                       |
| dask                       | 392 ms                                                       | 406 ms: 1.04x slower                                                         |
| asyncio_websockets         | 387 ms                                                       | 401 ms: 1.04x slower                                                         |
| sympy_str                  | 302 ms                                                       | 313 ms: 1.04x slower                                                         |
| meteor_contest             | 128 ms                                                       | 134 ms: 1.05x slower                                                         |
| json                       | 5.12 ms                                                      | 5.36 ms: 1.05x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 38.6 us: 1.05x slower                                                        |
| chameleon                  | 7.23 ms                                                      | 7.58 ms: 1.05x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 223 us: 1.06x slower                                                         |
| 2to3                       | 285 ms                                                       | 304 ms: 1.06x slower                                                         |
| sympy_integrate            | 23.9 ms                                                      | 25.7 ms: 1.07x slower                                                        |
| fannkuch                   | 350 ms                                                       | 377 ms: 1.08x slower                                                         |
| docutils                   | 2.87 sec                                                     | 3.10 sec: 1.08x slower                                                       |
| django_template            | 38.2 ms                                                      | 41.4 ms: 1.09x slower                                                        |
| pyflate                    | 439 ms                                                       | 479 ms: 1.09x slower                                                         |
| python_startup_no_site     | 8.64 ms                                                      | 9.44 ms: 1.09x slower                                                        |
| sympy_expand               | 484 ms                                                       | 531 ms: 1.10x slower                                                         |
| sqlglot_normalize          | 116 ms                                                       | 128 ms: 1.11x slower                                                         |
| deepcopy                   | 368 us                                                       | 408 us: 1.11x slower                                                         |
| gunicorn                   | 1.00 ms                                                      | 1.11 ms: 1.11x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 101 ms: 1.12x slower                                                         |
| sqlglot_optimize           | 57.5 ms                                                      | 64.7 ms: 1.13x slower                                                        |
| nbody                      | 88.0 ms                                                      | 99.1 ms: 1.13x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 113 ms: 1.15x slower                                                         |
| telco                      | 6.96 ms                                                      | 8.00 ms: 1.15x slower                                                        |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| go                         | 150 ms                                                       | 174 ms: 1.16x slower                                                         |
| coverage                   | 66.7 ms                                                      | 78.0 ms: 1.17x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 3.83 ms: 1.18x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.90 ms: 1.20x slower                                                        |
| hexiom                     | 5.96 ms                                                      | 7.31 ms: 1.23x slower                                                        |
| typing_runtime_protocols   | 152 us                                                       | 186 us: 1.23x slower                                                         |
| gc_traversal               | 3.48 ms                                                      | 4.34 ms: 1.25x slower                                                        |
| scimark_sor                | 109 ms                                                       | 151 ms: 1.39x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (4): xml_etree_process, bench_thread_pool, mypy2, bench_mp_pool
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240426-3.13.0a6+-3e06c7f-JIT/bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.69% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
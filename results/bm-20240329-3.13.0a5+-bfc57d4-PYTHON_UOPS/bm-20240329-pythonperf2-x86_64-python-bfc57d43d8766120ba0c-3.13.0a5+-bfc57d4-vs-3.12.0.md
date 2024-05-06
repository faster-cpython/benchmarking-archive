# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.14x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 325 ms: 1.14x slower                                                         |
| chameleon      | 7.23 ms                                                      | 8.14 ms: 1.13x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.28 sec: 1.14x slower                                                       |
| tornado_http   | 121 ms                                                       | 129 ms: 1.06x slower                                                         |
| Geometric mean | (ref)                                                        | 1.12x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 359 ms: 1.20x faster                                                         |
| async_tree_none            | 452 ms                                                       | 383 ms: 1.18x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 461 ms: 1.17x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 470 ms: 1.16x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 606 ms: 1.15x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 923 ms: 1.13x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 944 ms: 1.12x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 629 ms: 1.11x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.15x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 76.6 ms                                                      | 102 ms: 1.33x slower                                                         |
| nbody          | 88.0 ms                                                      | 129 ms: 1.47x slower                                                         |
| Geometric mean | (ref)                                                        | 1.25x slower                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.47 ms: 1.03x faster                                                        |
| regex_dna      | 239 ms                                                       | 242 ms: 1.01x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 25.9 ms: 1.10x slower                                                        |
| regex_compile  | 144 ms                                                       | 209 ms: 1.45x slower                                                         |
| Geometric mean | (ref)                                                        | 1.12x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_list        | 4.66 us                                                      | 4.59 us: 1.02x faster                                                        |
| pickle_list          | 4.43 us                                                      | 4.46 us: 1.01x slower                                                        |
| xml_etree_parse      | 144 ms                                                       | 146 ms: 1.02x slower                                                         |
| pickle_pure_python   | 318 us                                                       | 328 us: 1.03x slower                                                         |
| pickle               | 10.5 us                                                      | 10.9 us: 1.04x slower                                                        |
| json_loads           | 24.4 us                                                      | 25.8 us: 1.06x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.9 ms: 1.06x slower                                                        |
| xml_etree_generate   | 86.1 ms                                                      | 92.4 ms: 1.07x slower                                                        |
| pickle_dict          | 32.5 us                                                      | 35.2 us: 1.08x slower                                                        |
| xml_etree_process    | 58.4 ms                                                      | 63.4 ms: 1.09x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                       | 113 ms: 1.10x slower                                                         |
| tomli_loads          | 2.16 sec                                                     | 2.98 sec: 1.38x slower                                                       |
| unpickle_pure_python | 210 us                                                       | 319 us: 1.52x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                                 |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.2 ms: 1.29x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.20x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 42.3 ms: 1.11x slower                                                        |
| mako            | 10.0 ms                                                      | 14.4 ms: 1.44x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 359 ms: 1.20x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 128 us: 1.18x faster                                                         |
| async_tree_none            | 452 ms                                                       | 383 ms: 1.18x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 461 ms: 1.17x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 470 ms: 1.16x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 606 ms: 1.15x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 923 ms: 1.13x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 944 ms: 1.12x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 629 ms: 1.11x faster                                                         |
| generators                 | 37.4 ms                                                      | 34.9 ms: 1.07x faster                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.47 ms: 1.03x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 22.5 ms: 1.02x faster                                                        |
| unpickle_list              | 4.66 us                                                      | 4.59 us: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                       | 379 ms: 1.00x slower                                                         |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.60 sec: 1.01x slower                                                       |
| asyncio_websockets         | 387 ms                                                       | 390 ms: 1.01x slower                                                         |
| pickle_list                | 4.43 us                                                      | 4.46 us: 1.01x slower                                                        |
| regex_dna                  | 239 ms                                                       | 242 ms: 1.01x slower                                                         |
| logging_format             | 7.48 us                                                      | 7.60 us: 1.02x slower                                                        |
| xml_etree_parse            | 144 ms                                                       | 146 ms: 1.02x slower                                                         |
| async_generators           | 390 ms                                                       | 400 ms: 1.02x slower                                                         |
| pickle_pure_python         | 318 us                                                       | 328 us: 1.03x slower                                                         |
| logging_simple             | 6.71 us                                                      | 6.93 us: 1.03x slower                                                        |
| pickle                     | 10.5 us                                                      | 10.9 us: 1.04x slower                                                        |
| deepcopy_reduce            | 3.37 us                                                      | 3.53 us: 1.05x slower                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.91 us: 1.05x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.71 sec: 1.05x slower                                                       |
| json_loads                 | 24.4 us                                                      | 25.8 us: 1.06x slower                                                        |
| tornado_http               | 121 ms                                                       | 129 ms: 1.06x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.9 ms: 1.06x slower                                                        |
| dask                       | 392 ms                                                       | 418 ms: 1.07x slower                                                         |
| xml_etree_generate         | 86.1 ms                                                      | 92.4 ms: 1.07x slower                                                        |
| pickle_dict                | 32.5 us                                                      | 35.2 us: 1.08x slower                                                        |
| xml_etree_process          | 58.4 ms                                                      | 63.4 ms: 1.09x slower                                                        |
| json                       | 5.12 ms                                                      | 5.60 ms: 1.09x slower                                                        |
| bench_mp_pool              | 4.76 ms                                                      | 5.22 ms: 1.10x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 25.9 ms: 1.10x slower                                                        |
| deepcopy                   | 368 us                                                       | 405 us: 1.10x slower                                                         |
| xml_etree_iterparse        | 103 ms                                                       | 113 ms: 1.10x slower                                                         |
| logging_silent             | 94.4 ns                                                      | 104 ns: 1.10x slower                                                         |
| django_template            | 38.2 ms                                                      | 42.3 ms: 1.11x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.11 ms: 1.11x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 21.0 ms: 1.11x slower                                                        |
| python_startup             | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| meteor_contest             | 128 ms                                                       | 143 ms: 1.12x slower                                                         |
| sympy_sum                  | 162 ms                                                       | 181 ms: 1.12x slower                                                         |
| chameleon                  | 7.23 ms                                                      | 8.14 ms: 1.13x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.15 ms: 1.13x slower                                                        |
| sympy_integrate            | 23.9 ms                                                      | 27.0 ms: 1.13x slower                                                        |
| sqlglot_normalize          | 116 ms                                                       | 131 ms: 1.13x slower                                                         |
| 2to3                       | 285 ms                                                       | 325 ms: 1.14x slower                                                         |
| docutils                   | 2.87 sec                                                     | 3.28 sec: 1.14x slower                                                       |
| sqlglot_transpile          | 1.78 ms                                                      | 2.04 ms: 1.15x slower                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 92.5 ms: 1.15x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.84 ms: 1.16x slower                                                        |
| sympy_str                  | 302 ms                                                       | 350 ms: 1.16x slower                                                         |
| sqlglot_parse              | 1.38 ms                                                      | 1.61 ms: 1.17x slower                                                        |
| raytrace                   | 298 ms                                                       | 352 ms: 1.18x slower                                                         |
| dulwich_log                | 65.4 ms                                                      | 77.3 ms: 1.18x slower                                                        |
| pycparser                  | 1.23 sec                                                     | 1.47 sec: 1.19x slower                                                       |
| sqlglot_optimize           | 57.5 ms                                                      | 68.5 ms: 1.19x slower                                                        |
| bench_thread_pool          | 950 us                                                       | 1.14 ms: 1.20x slower                                                        |
| unpack_sequence            | 53.2 ns                                                      | 64.4 ns: 1.21x slower                                                        |
| chaos                      | 64.0 ms                                                      | 77.7 ms: 1.21x slower                                                        |
| sympy_expand               | 484 ms                                                       | 587 ms: 1.21x slower                                                         |
| comprehensions             | 21.9 us                                                      | 26.8 us: 1.22x slower                                                        |
| telco                      | 6.96 ms                                                      | 8.54 ms: 1.23x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 45.4 us: 1.23x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 2.06 sec: 1.25x slower                                                       |
| pprint_safe_repr           | 807 ms                                                       | 1.01 sec: 1.25x slower                                                       |
| coverage                   | 66.7 ms                                                      | 83.9 ms: 1.26x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.39 ms: 1.26x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 4.15 ms: 1.28x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 11.2 ms: 1.29x slower                                                        |
| richards_super             | 51.3 ms                                                      | 68.0 ms: 1.32x slower                                                        |
| float                      | 76.6 ms                                                      | 102 ms: 1.33x slower                                                         |
| richards                   | 45.7 ms                                                      | 61.1 ms: 1.34x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 122 ms: 1.36x slower                                                         |
| go                         | 150 ms                                                       | 204 ms: 1.36x slower                                                         |
| tomli_loads                | 2.16 sec                                                     | 2.98 sec: 1.38x slower                                                       |
| mako                       | 10.0 ms                                                      | 14.4 ms: 1.44x slower                                                        |
| fannkuch                   | 350 ms                                                       | 507 ms: 1.45x slower                                                         |
| regex_compile              | 144 ms                                                       | 209 ms: 1.45x slower                                                         |
| nbody                      | 88.0 ms                                                      | 129 ms: 1.47x slower                                                         |
| scimark_fft                | 301 ms                                                       | 446 ms: 1.48x slower                                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 102 ms: 1.48x slower                                                         |
| pyflate                    | 439 ms                                                       | 666 ms: 1.52x slower                                                         |
| unpickle_pure_python       | 210 us                                                       | 319 us: 1.52x slower                                                         |
| scimark_sor                | 109 ms                                                       | 167 ms: 1.53x slower                                                         |
| scimark_lu                 | 98.8 ms                                                      | 152 ms: 1.54x slower                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 6.79 ms: 1.61x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 158 ms: 1.72x slower                                                         |
| hexiom                     | 5.96 ms                                                      | 11.0 ms: 1.84x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                                 |

Benchmark hidden because not significant (3): unpickle, pidigits, mypy2
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-bfc57d4-PYTHON_UOPS/bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 0.91x
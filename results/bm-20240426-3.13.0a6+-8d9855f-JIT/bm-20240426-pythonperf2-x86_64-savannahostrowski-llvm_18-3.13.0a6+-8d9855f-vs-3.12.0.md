# Results vs. 3.12.0

- fork: savannahostrowski
- ref: llvm_18
- machine: linux-x86_64
- commit hash: 8d9855f
- commit date: 2024-04-26
- overall geometric mean: 1.02x slower
- HPT reliability: 90.18%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 302 ms: 1.06x slower                                                       |
| chameleon      | 7.23 ms                                                      | 7.46 ms: 1.03x slower                                                      |
| docutils       | 2.87 sec                                                     | 3.09 sec: 1.08x slower                                                     |
| Geometric mean | (ref)                                                        | 1.04x slower                                                               |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 418 ms: 1.29x faster                                                       |
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.28x faster                                                       |
| async_tree_io_tg           | 1.05 sec                                                     | 852 ms: 1.24x faster                                                       |
| async_tree_none            | 452 ms                                                       | 371 ms: 1.22x faster                                                       |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 589 ms: 1.18x faster                                                       |
| async_tree_io              | 1.04 sec                                                     | 883 ms: 1.18x faster                                                       |
| async_tree_memoization     | 544 ms                                                       | 464 ms: 1.17x faster                                                       |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 614 ms: 1.13x faster                                                       |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.02x faster                                                       |
| float          | 76.6 ms                                                      | 76.0 ms: 1.01x faster                                                      |
| nbody          | 88.0 ms                                                      | 98.9 ms: 1.12x slower                                                      |
| Geometric mean | (ref)                                                        | 1.03x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.51 ms: 1.02x faster                                                      |
| regex_dna      | 239 ms                                                       | 238 ms: 1.00x faster                                                       |
| regex_v8       | 23.6 ms                                                      | 26.1 ms: 1.11x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.5 us: 1.07x faster                                                      |
| xml_etree_generate   | 86.1 ms                                                      | 83.0 ms: 1.04x faster                                                      |
| tomli_loads          | 2.16 sec                                                     | 2.09 sec: 1.03x faster                                                     |
| xml_etree_iterparse  | 103 ms                                                       | 100 ms: 1.03x faster                                                       |
| pickle               | 10.5 us                                                      | 10.3 us: 1.02x faster                                                      |
| xml_etree_process    | 58.4 ms                                                      | 57.6 ms: 1.01x faster                                                      |
| xml_etree_parse      | 144 ms                                                       | 142 ms: 1.01x faster                                                       |
| pickle_pure_python   | 318 us                                                       | 317 us: 1.00x faster                                                       |
| json_loads           | 24.4 us                                                      | 24.6 us: 1.01x slower                                                      |
| unpickle_list        | 4.66 us                                                      | 4.73 us: 1.01x slower                                                      |
| pickle_list          | 4.43 us                                                      | 4.50 us: 1.02x slower                                                      |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                       |
| json_dumps           | 10.2 ms                                                      | 10.7 ms: 1.04x slower                                                      |
| unpickle             | 14.8 us                                                      | 15.6 us: 1.06x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 9.43 ms: 1.09x slower                                                      |
| python_startup         | 11.6 ms                                                      | 13.4 ms: 1.16x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.12x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.65 ms: 1.04x faster                                                      |
| django_template | 38.2 ms                                                      | 40.4 ms: 1.06x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 418 ms: 1.29x faster                                                       |
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.28x faster                                                       |
| async_tree_io_tg           | 1.05 sec                                                     | 852 ms: 1.24x faster                                                       |
| async_tree_none            | 452 ms                                                       | 371 ms: 1.22x faster                                                       |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 589 ms: 1.18x faster                                                       |
| async_tree_io              | 1.04 sec                                                     | 883 ms: 1.18x faster                                                       |
| async_tree_memoization     | 544 ms                                                       | 464 ms: 1.17x faster                                                       |
| comprehensions             | 21.9 us                                                      | 19.3 us: 1.13x faster                                                      |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 614 ms: 1.13x faster                                                       |
| generators                 | 37.4 ms                                                      | 34.4 ms: 1.09x faster                                                      |
| pathlib                    | 18.9 ms                                                      | 17.6 ms: 1.08x faster                                                      |
| pickle_dict                | 32.5 us                                                      | 30.5 us: 1.07x faster                                                      |
| coroutines                 | 23.0 ms                                                      | 21.6 ms: 1.06x faster                                                      |
| raytrace                   | 298 ms                                                       | 281 ms: 1.06x faster                                                       |
| crypto_pyaes               | 80.3 ms                                                      | 76.3 ms: 1.05x faster                                                      |
| logging_format             | 7.48 us                                                      | 7.15 us: 1.05x faster                                                      |
| xml_etree_generate         | 86.1 ms                                                      | 83.0 ms: 1.04x faster                                                      |
| mako                       | 10.0 ms                                                      | 9.65 ms: 1.04x faster                                                      |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.06 ms: 1.04x faster                                                      |
| tomli_loads                | 2.16 sec                                                     | 2.09 sec: 1.03x faster                                                     |
| logging_simple             | 6.71 us                                                      | 6.52 us: 1.03x faster                                                      |
| xml_etree_iterparse        | 103 ms                                                       | 100 ms: 1.03x faster                                                       |
| sqlite_synth               | 2.77 us                                                      | 2.71 us: 1.02x faster                                                      |
| pickle                     | 10.5 us                                                      | 10.3 us: 1.02x faster                                                      |
| regex_effbot               | 3.57 ms                                                      | 3.51 ms: 1.02x faster                                                      |
| pidigits                   | 265 ms                                                       | 261 ms: 1.02x faster                                                       |
| xml_etree_process          | 58.4 ms                                                      | 57.6 ms: 1.01x faster                                                      |
| xml_etree_parse            | 144 ms                                                       | 142 ms: 1.01x faster                                                       |
| asyncio_tcp                | 378 ms                                                       | 374 ms: 1.01x faster                                                       |
| float                      | 76.6 ms                                                      | 76.0 ms: 1.01x faster                                                      |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                     |
| spectral_norm              | 91.6 ms                                                      | 90.9 ms: 1.01x faster                                                      |
| async_generators           | 390 ms                                                       | 389 ms: 1.00x faster                                                       |
| pickle_pure_python         | 318 us                                                       | 317 us: 1.00x faster                                                       |
| regex_dna                  | 239 ms                                                       | 238 ms: 1.00x faster                                                       |
| json_loads                 | 24.4 us                                                      | 24.6 us: 1.01x slower                                                      |
| asyncio_websockets         | 387 ms                                                       | 391 ms: 1.01x slower                                                       |
| logging_silent             | 94.4 ns                                                      | 95.4 ns: 1.01x slower                                                      |
| unpickle_list              | 4.66 us                                                      | 4.73 us: 1.01x slower                                                      |
| sympy_sum                  | 162 ms                                                       | 165 ms: 1.02x slower                                                       |
| pprint_pformat             | 1.65 sec                                                     | 1.68 sec: 1.02x slower                                                     |
| deepcopy_memo              | 36.8 us                                                      | 37.4 us: 1.02x slower                                                      |
| pickle_list                | 4.43 us                                                      | 4.50 us: 1.02x slower                                                      |
| sympy_str                  | 302 ms                                                       | 308 ms: 1.02x slower                                                       |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                                       |
| deepcopy_reduce            | 3.37 us                                                      | 3.44 us: 1.02x slower                                                      |
| dask                       | 392 ms                                                       | 402 ms: 1.02x slower                                                       |
| chaos                      | 64.0 ms                                                      | 65.7 ms: 1.03x slower                                                      |
| sqlglot_transpile          | 1.78 ms                                                      | 1.82 ms: 1.03x slower                                                      |
| dulwich_log                | 65.4 ms                                                      | 67.4 ms: 1.03x slower                                                      |
| sqlglot_parse              | 1.38 ms                                                      | 1.42 ms: 1.03x slower                                                      |
| chameleon                  | 7.23 ms                                                      | 7.46 ms: 1.03x slower                                                      |
| json                       | 5.12 ms                                                      | 5.31 ms: 1.04x slower                                                      |
| pprint_safe_repr           | 807 ms                                                       | 839 ms: 1.04x slower                                                       |
| json_dumps                 | 10.2 ms                                                      | 10.7 ms: 1.04x slower                                                      |
| pycparser                  | 1.23 sec                                                     | 1.29 sec: 1.05x slower                                                     |
| scimark_fft                | 301 ms                                                       | 318 ms: 1.06x slower                                                       |
| meteor_contest             | 128 ms                                                       | 135 ms: 1.06x slower                                                       |
| unpickle                   | 14.8 us                                                      | 15.6 us: 1.06x slower                                                      |
| 2to3                       | 285 ms                                                       | 302 ms: 1.06x slower                                                       |
| django_template            | 38.2 ms                                                      | 40.4 ms: 1.06x slower                                                      |
| sympy_expand               | 484 ms                                                       | 513 ms: 1.06x slower                                                       |
| sqlglot_normalize          | 116 ms                                                       | 123 ms: 1.06x slower                                                       |
| deepcopy                   | 368 us                                                       | 393 us: 1.07x slower                                                       |
| sympy_integrate            | 23.9 ms                                                      | 25.6 ms: 1.07x slower                                                      |
| fannkuch                   | 350 ms                                                       | 376 ms: 1.07x slower                                                       |
| docutils                   | 2.87 sec                                                     | 3.09 sec: 1.08x slower                                                     |
| python_startup_no_site     | 8.64 ms                                                      | 9.43 ms: 1.09x slower                                                      |
| sqlglot_optimize           | 57.5 ms                                                      | 63.1 ms: 1.10x slower                                                      |
| gunicorn                   | 1.00 ms                                                      | 1.10 ms: 1.10x slower                                                      |
| regex_v8                   | 23.6 ms                                                      | 26.1 ms: 1.11x slower                                                      |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                                      |
| nqueens                    | 89.9 ms                                                      | 100 ms: 1.11x slower                                                       |
| nbody                      | 88.0 ms                                                      | 98.9 ms: 1.12x slower                                                      |
| pyflate                    | 439 ms                                                       | 494 ms: 1.13x slower                                                       |
| go                         | 150 ms                                                       | 173 ms: 1.15x slower                                                       |
| python_startup             | 11.6 ms                                                      | 13.4 ms: 1.16x slower                                                      |
| telco                      | 6.96 ms                                                      | 8.05 ms: 1.16x slower                                                      |
| deltablue                  | 3.24 ms                                                      | 3.80 ms: 1.18x slower                                                      |
| hexiom                     | 5.96 ms                                                      | 7.02 ms: 1.18x slower                                                      |
| create_gc_cycles           | 1.59 ms                                                      | 1.89 ms: 1.19x slower                                                      |
| coverage                   | 66.7 ms                                                      | 79.6 ms: 1.19x slower                                                      |
| scimark_lu                 | 98.8 ms                                                      | 119 ms: 1.21x slower                                                       |
| typing_runtime_protocols   | 152 us                                                       | 185 us: 1.22x slower                                                       |
| gc_traversal               | 3.48 ms                                                      | 4.43 ms: 1.27x slower                                                      |
| scimark_sor                | 109 ms                                                       | 151 ms: 1.39x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (9): bench_thread_pool, regex_compile, richards_super, mdp, richards, scimark_monte_carlo, tornado_http, bench_mp_pool, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240426-3.13.0a6+-8d9855f-JIT/bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 90.18% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.02x slower
- HPT reliability: 96.80%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 300 ms: 1.05x slower                                                       |
| chameleon      | 7.23 ms                                                      | 7.36 ms: 1.02x slower                                                      |
| docutils       | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                     |
| tornado_http   | 121 ms                                                       | 123 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                        | 1.04x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 341 ms: 1.26x faster                                                       |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                       |
| async_tree_memoization     | 544 ms                                                       | 441 ms: 1.23x faster                                                       |
| async_tree_memoization_tg  | 540 ms                                                       | 439 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 579 ms: 1.20x faster                                                       |
| async_tree_io              | 1.04 sec                                                     | 885 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 593 ms: 1.17x faster                                                       |
| async_tree_io_tg           | 1.05 sec                                                     | 910 ms: 1.16x faster                                                       |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 76.6 ms                                                      | 75.4 ms: 1.02x faster                                                      |
| pidigits       | 265 ms                                                       | 261 ms: 1.02x faster                                                       |
| nbody          | 88.0 ms                                                      | 93.1 ms: 1.06x slower                                                      |
| Geometric mean | (ref)                                                        | 1.01x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.54 ms: 1.01x faster                                                      |
| regex_dna      | 239 ms                                                       | 239 ms: 1.00x slower                                                       |
| regex_compile  | 144 ms                                                       | 146 ms: 1.01x slower                                                       |
| regex_v8       | 23.6 ms                                                      | 25.4 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.9 us: 1.05x faster                                                      |
| pickle_list          | 4.43 us                                                      | 4.28 us: 1.04x faster                                                      |
| xml_etree_generate   | 86.1 ms                                                      | 83.3 ms: 1.03x faster                                                      |
| tomli_loads          | 2.16 sec                                                     | 2.10 sec: 1.03x faster                                                     |
| pickle_pure_python   | 318 us                                                       | 312 us: 1.02x faster                                                       |
| pickle               | 10.5 us                                                      | 10.6 us: 1.00x slower                                                      |
| unpickle             | 14.8 us                                                      | 15.3 us: 1.03x slower                                                      |
| json_loads           | 24.4 us                                                      | 25.5 us: 1.05x slower                                                      |
| json_dumps           | 10.2 ms                                                      | 10.8 ms: 1.05x slower                                                      |
| unpickle_pure_python | 210 us                                                       | 229 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                               |

Benchmark hidden because not significant (4): unpickle_list, xml_etree_parse, xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                      |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.29 ms: 1.08x faster                                                      |
| django_template | 38.2 ms                                                      | 40.4 ms: 1.06x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 152 us                                                       | 120 us: 1.27x faster                                                       |
| async_tree_none_tg         | 431 ms                                                       | 341 ms: 1.26x faster                                                       |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                       |
| async_tree_memoization     | 544 ms                                                       | 441 ms: 1.23x faster                                                       |
| async_tree_memoization_tg  | 540 ms                                                       | 439 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 579 ms: 1.20x faster                                                       |
| async_tree_io              | 1.04 sec                                                     | 885 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 593 ms: 1.17x faster                                                       |
| async_tree_io_tg           | 1.05 sec                                                     | 910 ms: 1.16x faster                                                       |
| comprehensions             | 21.9 us                                                      | 19.0 us: 1.15x faster                                                      |
| generators                 | 37.4 ms                                                      | 33.1 ms: 1.13x faster                                                      |
| spectral_norm              | 91.6 ms                                                      | 81.9 ms: 1.12x faster                                                      |
| crypto_pyaes               | 80.3 ms                                                      | 72.5 ms: 1.11x faster                                                      |
| mako                       | 10.0 ms                                                      | 9.29 ms: 1.08x faster                                                      |
| pickle_dict                | 32.5 us                                                      | 30.9 us: 1.05x faster                                                      |
| scimark_fft                | 301 ms                                                       | 290 ms: 1.04x faster                                                       |
| sqlite_synth               | 2.77 us                                                      | 2.68 us: 1.04x faster                                                      |
| pickle_list                | 4.43 us                                                      | 4.28 us: 1.04x faster                                                      |
| xml_etree_generate         | 86.1 ms                                                      | 83.3 ms: 1.03x faster                                                      |
| scimark_monte_carlo        | 69.0 ms                                                      | 66.9 ms: 1.03x faster                                                      |
| tomli_loads                | 2.16 sec                                                     | 2.10 sec: 1.03x faster                                                     |
| chaos                      | 64.0 ms                                                      | 62.8 ms: 1.02x faster                                                      |
| pickle_pure_python         | 318 us                                                       | 312 us: 1.02x faster                                                       |
| coroutines                 | 23.0 ms                                                      | 22.6 ms: 1.02x faster                                                      |
| float                      | 76.6 ms                                                      | 75.4 ms: 1.02x faster                                                      |
| pidigits                   | 265 ms                                                       | 261 ms: 1.02x faster                                                       |
| logging_format             | 7.48 us                                                      | 7.38 us: 1.01x faster                                                      |
| regex_effbot               | 3.57 ms                                                      | 3.54 ms: 1.01x faster                                                      |
| asyncio_tcp                | 378 ms                                                       | 375 ms: 1.01x faster                                                       |
| deepcopy_reduce            | 3.37 us                                                      | 3.34 us: 1.01x faster                                                      |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.19 ms: 1.01x faster                                                      |
| sympy_sum                  | 162 ms                                                       | 161 ms: 1.00x faster                                                       |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.00x faster                                                     |
| pprint_pformat             | 1.65 sec                                                     | 1.65 sec: 1.00x faster                                                     |
| regex_dna                  | 239 ms                                                       | 239 ms: 1.00x slower                                                       |
| pickle                     | 10.5 us                                                      | 10.6 us: 1.00x slower                                                      |
| pprint_safe_repr           | 807 ms                                                       | 811 ms: 1.01x slower                                                       |
| mdp                        | 2.57 sec                                                     | 2.60 sec: 1.01x slower                                                     |
| async_generators           | 390 ms                                                       | 395 ms: 1.01x slower                                                       |
| regex_compile              | 144 ms                                                       | 146 ms: 1.01x slower                                                       |
| asyncio_websockets         | 387 ms                                                       | 393 ms: 1.02x slower                                                       |
| sqlglot_transpile          | 1.78 ms                                                      | 1.81 ms: 1.02x slower                                                      |
| chameleon                  | 7.23 ms                                                      | 7.36 ms: 1.02x slower                                                      |
| raytrace                   | 298 ms                                                       | 303 ms: 1.02x slower                                                       |
| tornado_http               | 121 ms                                                       | 123 ms: 1.02x slower                                                       |
| sqlglot_parse              | 1.38 ms                                                      | 1.40 ms: 1.02x slower                                                      |
| pycparser                  | 1.23 sec                                                     | 1.26 sec: 1.02x slower                                                     |
| dask                       | 392 ms                                                       | 404 ms: 1.03x slower                                                       |
| pyflate                    | 439 ms                                                       | 454 ms: 1.03x slower                                                       |
| meteor_contest             | 128 ms                                                       | 133 ms: 1.03x slower                                                       |
| unpickle                   | 14.8 us                                                      | 15.3 us: 1.03x slower                                                      |
| pathlib                    | 18.9 ms                                                      | 19.7 ms: 1.04x slower                                                      |
| logging_silent             | 94.4 ns                                                      | 98.6 ns: 1.04x slower                                                      |
| json_loads                 | 24.4 us                                                      | 25.5 us: 1.05x slower                                                      |
| deepcopy_memo              | 36.8 us                                                      | 38.5 us: 1.05x slower                                                      |
| 2to3                       | 285 ms                                                       | 300 ms: 1.05x slower                                                       |
| json_dumps                 | 10.2 ms                                                      | 10.8 ms: 1.05x slower                                                      |
| sympy_integrate            | 23.9 ms                                                      | 25.2 ms: 1.05x slower                                                      |
| dulwich_log                | 65.4 ms                                                      | 68.9 ms: 1.05x slower                                                      |
| deepcopy                   | 368 us                                                       | 389 us: 1.05x slower                                                       |
| nbody                      | 88.0 ms                                                      | 93.1 ms: 1.06x slower                                                      |
| django_template            | 38.2 ms                                                      | 40.4 ms: 1.06x slower                                                      |
| sympy_expand               | 484 ms                                                       | 513 ms: 1.06x slower                                                       |
| bench_mp_pool              | 4.76 ms                                                      | 5.07 ms: 1.07x slower                                                      |
| docutils                   | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                     |
| json                       | 5.12 ms                                                      | 5.48 ms: 1.07x slower                                                      |
| regex_v8                   | 23.6 ms                                                      | 25.4 ms: 1.07x slower                                                      |
| sqlglot_normalize          | 116 ms                                                       | 125 ms: 1.08x slower                                                       |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.09x slower                                                      |
| unpickle_pure_python       | 210 us                                                       | 229 us: 1.09x slower                                                       |
| aiohttp                    | 1.02 ms                                                      | 1.12 ms: 1.10x slower                                                      |
| richards                   | 45.7 ms                                                      | 50.5 ms: 1.10x slower                                                      |
| richards_super             | 51.3 ms                                                      | 56.7 ms: 1.10x slower                                                      |
| sqlglot_optimize           | 57.5 ms                                                      | 63.6 ms: 1.11x slower                                                      |
| nqueens                    | 89.9 ms                                                      | 102 ms: 1.14x slower                                                       |
| create_gc_cycles           | 1.59 ms                                                      | 1.82 ms: 1.14x slower                                                      |
| deltablue                  | 3.24 ms                                                      | 3.71 ms: 1.15x slower                                                      |
| telco                      | 6.96 ms                                                      | 8.04 ms: 1.15x slower                                                      |
| scimark_lu                 | 98.8 ms                                                      | 115 ms: 1.16x slower                                                       |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                      |
| go                         | 150 ms                                                       | 175 ms: 1.17x slower                                                       |
| bench_thread_pool          | 950 us                                                       | 1.11 ms: 1.17x slower                                                      |
| hexiom                     | 5.96 ms                                                      | 7.09 ms: 1.19x slower                                                      |
| coverage                   | 66.7 ms                                                      | 79.7 ms: 1.20x slower                                                      |
| scimark_sor                | 109 ms                                                       | 148 ms: 1.36x slower                                                       |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                      |
| gc_traversal               | 3.48 ms                                                      | 4.81 ms: 1.38x slower                                                      |
| unpack_sequence            | 53.2 ns                                                      | 89.5 ns: 1.68x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (8): unpickle_list, fannkuch, logging_simple, xml_etree_parse, sympy_str, xml_etree_process, mypy2, xml_etree_iterparse
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 96.80% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x
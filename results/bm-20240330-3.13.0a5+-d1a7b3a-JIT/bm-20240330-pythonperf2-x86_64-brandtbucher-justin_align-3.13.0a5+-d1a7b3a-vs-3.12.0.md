# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.03x slower
- HPT reliability: 99.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 299 ms: 1.05x slower                                                       |
| chameleon      | 7.23 ms                                                      | 7.12 ms: 1.02x faster                                                      |
| docutils       | 2.87 sec                                                     | 3.06 sec: 1.07x slower                                                     |
| tornado_http   | 121 ms                                                       | 125 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                        | 1.03x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 337 ms: 1.28x faster                                                       |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                       |
| async_tree_memoization_tg  | 540 ms                                                       | 432 ms: 1.25x faster                                                       |
| async_tree_memoization     | 544 ms                                                       | 441 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 576 ms: 1.21x faster                                                       |
| async_tree_io              | 1.04 sec                                                     | 882 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 594 ms: 1.17x faster                                                       |
| async_tree_io_tg           | 1.05 sec                                                     | 904 ms: 1.17x faster                                                       |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                       |
| float          | 76.6 ms                                                      | 78.0 ms: 1.02x slower                                                      |
| nbody          | 88.0 ms                                                      | 97.3 ms: 1.11x slower                                                      |
| Geometric mean | (ref)                                                        | 1.04x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.46 ms: 1.03x faster                                                      |
| regex_compile  | 144 ms                                                       | 147 ms: 1.02x slower                                                       |
| regex_v8       | 23.6 ms                                                      | 26.2 ms: 1.11x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_generate   | 86.1 ms                                                      | 83.4 ms: 1.03x faster                                                      |
| unpickle_list        | 4.66 us                                                      | 4.60 us: 1.01x faster                                                      |
| pickle_pure_python   | 318 us                                                       | 315 us: 1.01x faster                                                       |
| tomli_loads          | 2.16 sec                                                     | 2.14 sec: 1.01x faster                                                     |
| xml_etree_parse      | 144 ms                                                       | 143 ms: 1.01x faster                                                       |
| xml_etree_process    | 58.4 ms                                                      | 58.1 ms: 1.00x faster                                                      |
| pickle_list          | 4.43 us                                                      | 4.50 us: 1.02x slower                                                      |
| pickle               | 10.5 us                                                      | 10.7 us: 1.02x slower                                                      |
| pickle_dict          | 32.5 us                                                      | 33.6 us: 1.03x slower                                                      |
| json_loads           | 24.4 us                                                      | 25.3 us: 1.04x slower                                                      |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                      |
| unpickle_pure_python | 210 us                                                       | 235 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                               |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                      |
| python_startup_no_site | 8.64 ms                                                      | 11.7 ms: 1.36x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.25x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.91 ms: 1.01x faster                                                      |
| django_template | 38.2 ms                                                      | 39.1 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 152 us                                                       | 117 us: 1.29x faster                                                       |
| async_tree_none_tg         | 431 ms                                                       | 337 ms: 1.28x faster                                                       |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                       |
| async_tree_memoization_tg  | 540 ms                                                       | 432 ms: 1.25x faster                                                       |
| async_tree_memoization     | 544 ms                                                       | 441 ms: 1.23x faster                                                       |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 576 ms: 1.21x faster                                                       |
| async_tree_io              | 1.04 sec                                                     | 882 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 594 ms: 1.17x faster                                                       |
| async_tree_io_tg           | 1.05 sec                                                     | 904 ms: 1.17x faster                                                       |
| comprehensions             | 21.9 us                                                      | 19.9 us: 1.10x faster                                                      |
| generators                 | 37.4 ms                                                      | 34.3 ms: 1.09x faster                                                      |
| logging_format             | 7.48 us                                                      | 7.19 us: 1.04x faster                                                      |
| sqlite_synth               | 2.77 us                                                      | 2.67 us: 1.04x faster                                                      |
| xml_etree_generate         | 86.1 ms                                                      | 83.4 ms: 1.03x faster                                                      |
| regex_effbot               | 3.57 ms                                                      | 3.46 ms: 1.03x faster                                                      |
| crypto_pyaes               | 80.3 ms                                                      | 78.2 ms: 1.03x faster                                                      |
| asyncio_tcp                | 378 ms                                                       | 368 ms: 1.03x faster                                                       |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.14 ms: 1.02x faster                                                      |
| logging_simple             | 6.71 us                                                      | 6.60 us: 1.02x faster                                                      |
| chameleon                  | 7.23 ms                                                      | 7.12 ms: 1.02x faster                                                      |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                       |
| unpickle_list              | 4.66 us                                                      | 4.60 us: 1.01x faster                                                      |
| pickle_pure_python         | 318 us                                                       | 315 us: 1.01x faster                                                       |
| mako                       | 10.0 ms                                                      | 9.91 ms: 1.01x faster                                                      |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                     |
| tomli_loads                | 2.16 sec                                                     | 2.14 sec: 1.01x faster                                                     |
| xml_etree_parse            | 144 ms                                                       | 143 ms: 1.01x faster                                                       |
| xml_etree_process          | 58.4 ms                                                      | 58.1 ms: 1.00x faster                                                      |
| async_generators           | 390 ms                                                       | 392 ms: 1.00x slower                                                       |
| asyncio_websockets         | 387 ms                                                       | 391 ms: 1.01x slower                                                       |
| pathlib                    | 18.9 ms                                                      | 19.1 ms: 1.01x slower                                                      |
| pickle_list                | 4.43 us                                                      | 4.50 us: 1.02x slower                                                      |
| pickle                     | 10.5 us                                                      | 10.7 us: 1.02x slower                                                      |
| float                      | 76.6 ms                                                      | 78.0 ms: 1.02x slower                                                      |
| deepcopy_memo              | 36.8 us                                                      | 37.4 us: 1.02x slower                                                      |
| regex_compile              | 144 ms                                                       | 147 ms: 1.02x slower                                                       |
| mdp                        | 2.57 sec                                                     | 2.62 sec: 1.02x slower                                                     |
| pycparser                  | 1.23 sec                                                     | 1.26 sec: 1.02x slower                                                     |
| spectral_norm              | 91.6 ms                                                      | 93.5 ms: 1.02x slower                                                      |
| django_template            | 38.2 ms                                                      | 39.1 ms: 1.03x slower                                                      |
| deepcopy                   | 368 us                                                       | 379 us: 1.03x slower                                                       |
| tornado_http               | 121 ms                                                       | 125 ms: 1.03x slower                                                       |
| meteor_contest             | 128 ms                                                       | 132 ms: 1.03x slower                                                       |
| pprint_safe_repr           | 807 ms                                                       | 831 ms: 1.03x slower                                                       |
| dask                       | 392 ms                                                       | 404 ms: 1.03x slower                                                       |
| coroutines                 | 23.0 ms                                                      | 23.7 ms: 1.03x slower                                                      |
| sqlglot_transpile          | 1.78 ms                                                      | 1.83 ms: 1.03x slower                                                      |
| pickle_dict                | 32.5 us                                                      | 33.6 us: 1.03x slower                                                      |
| json_loads                 | 24.4 us                                                      | 25.3 us: 1.04x slower                                                      |
| raytrace                   | 298 ms                                                       | 310 ms: 1.04x slower                                                       |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                      |
| chaos                      | 64.0 ms                                                      | 66.8 ms: 1.04x slower                                                      |
| pprint_pformat             | 1.65 sec                                                     | 1.73 sec: 1.05x slower                                                     |
| logging_silent             | 94.4 ns                                                      | 98.8 ns: 1.05x slower                                                      |
| sqlglot_parse              | 1.38 ms                                                      | 1.44 ms: 1.05x slower                                                      |
| sympy_integrate            | 23.9 ms                                                      | 25.1 ms: 1.05x slower                                                      |
| 2to3                       | 285 ms                                                       | 299 ms: 1.05x slower                                                       |
| json                       | 5.12 ms                                                      | 5.39 ms: 1.05x slower                                                      |
| dulwich_log                | 65.4 ms                                                      | 68.9 ms: 1.05x slower                                                      |
| sqlglot_normalize          | 116 ms                                                       | 122 ms: 1.06x slower                                                       |
| sympy_expand               | 484 ms                                                       | 512 ms: 1.06x slower                                                       |
| bench_mp_pool              | 4.76 ms                                                      | 5.05 ms: 1.06x slower                                                      |
| docutils                   | 2.87 sec                                                     | 3.06 sec: 1.07x slower                                                     |
| scimark_fft                | 301 ms                                                       | 322 ms: 1.07x slower                                                       |
| fannkuch                   | 350 ms                                                       | 378 ms: 1.08x slower                                                       |
| scimark_monte_carlo        | 69.0 ms                                                      | 74.6 ms: 1.08x slower                                                      |
| gunicorn                   | 1.00 ms                                                      | 1.08 ms: 1.08x slower                                                      |
| sqlglot_optimize           | 57.5 ms                                                      | 62.8 ms: 1.09x slower                                                      |
| nbody                      | 88.0 ms                                                      | 97.3 ms: 1.11x slower                                                      |
| regex_v8                   | 23.6 ms                                                      | 26.2 ms: 1.11x slower                                                      |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                                      |
| richards                   | 45.7 ms                                                      | 50.9 ms: 1.11x slower                                                      |
| unpack_sequence            | 53.2 ns                                                      | 59.2 ns: 1.11x slower                                                      |
| unpickle_pure_python       | 210 us                                                       | 235 us: 1.12x slower                                                       |
| richards_super             | 51.3 ms                                                      | 57.8 ms: 1.13x slower                                                      |
| create_gc_cycles           | 1.59 ms                                                      | 1.79 ms: 1.13x slower                                                      |
| pyflate                    | 439 ms                                                       | 496 ms: 1.13x slower                                                       |
| deltablue                  | 3.24 ms                                                      | 3.71 ms: 1.15x slower                                                      |
| go                         | 150 ms                                                       | 173 ms: 1.16x slower                                                       |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                      |
| telco                      | 6.96 ms                                                      | 8.14 ms: 1.17x slower                                                      |
| nqueens                    | 89.9 ms                                                      | 105 ms: 1.17x slower                                                       |
| bench_thread_pool          | 950 us                                                       | 1.12 ms: 1.18x slower                                                      |
| scimark_lu                 | 98.8 ms                                                      | 122 ms: 1.23x slower                                                       |
| hexiom                     | 5.96 ms                                                      | 7.53 ms: 1.26x slower                                                      |
| coverage                   | 66.7 ms                                                      | 86.2 ms: 1.29x slower                                                      |
| gc_traversal               | 3.48 ms                                                      | 4.55 ms: 1.31x slower                                                      |
| python_startup_no_site     | 8.64 ms                                                      | 11.7 ms: 1.36x slower                                                      |
| scimark_sor                | 109 ms                                                       | 153 ms: 1.40x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                               |

Benchmark hidden because not significant (7): xml_etree_iterparse, sympy_str, sympy_sum, mypy2, regex_dna, unpickle, deepcopy_reduce
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.83% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x
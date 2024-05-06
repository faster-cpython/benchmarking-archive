# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 252 ms: 1.11x faster                                                          |
| chameleon      | 7.75 ms                                                         | 6.20 ms: 1.25x faster                                                         |
| docutils       | 1.98 sec                                                        | 1.93 sec: 1.03x faster                                                        |
| tornado_http   | 105 ms                                                          | 96.9 ms: 1.08x faster                                                         |
| Geometric mean | (ref)                                                           | 1.11x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 278 ms                                                          | 209 ms: 1.33x faster                                                          |
| async_tree_memoization_tg  | 350 ms                                                          | 264 ms: 1.33x faster                                                          |
| async_tree_memoization     | 364 ms                                                          | 285 ms: 1.28x faster                                                          |
| async_tree_none            | 298 ms                                                          | 234 ms: 1.27x faster                                                          |
| async_tree_io              | 693 ms                                                          | 548 ms: 1.27x faster                                                          |
| async_tree_io_tg           | 677 ms                                                          | 547 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 450 ms: 1.21x faster                                                          |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 473 ms: 1.19x faster                                                          |
| Geometric mean             | (ref)                                                           | 1.26x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.6 ms: 1.43x faster                                                         |
| nbody          | 127 ms                                                          | 92.1 ms: 1.38x faster                                                         |
| pidigits       | 199 ms                                                          | 202 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                           | 1.25x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 115 ms: 1.12x faster                                                          |
| regex_dna      | 127 ms                                                          | 119 ms: 1.06x faster                                                          |
| regex_effbot   | 2.04 ms                                                         | 1.92 ms: 1.06x faster                                                         |
| regex_v8       | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 2.20 sec                                                        | 1.67 sec: 1.31x faster                                                        |
| pickle_pure_python   | 286 us                                                          | 221 us: 1.29x faster                                                          |
| unpickle_pure_python | 210 us                                                          | 166 us: 1.26x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 42.6 ms: 1.25x faster                                                         |
| xml_etree_iterparse  | 77.6 ms                                                         | 64.8 ms: 1.20x faster                                                         |
| xml_etree_generate   | 72.1 ms                                                         | 60.8 ms: 1.19x faster                                                         |
| json_dumps           | 7.40 ms                                                         | 6.70 ms: 1.10x faster                                                         |
| pickle_list          | 3.37 us                                                         | 3.18 us: 1.06x faster                                                         |
| xml_etree_parse      | 113 ms                                                          | 108 ms: 1.05x faster                                                          |
| unpickle_list        | 2.95 us                                                         | 2.90 us: 1.02x faster                                                         |
| pickle_dict          | 19.9 us                                                         | 19.6 us: 1.02x faster                                                         |
| json_loads           | 20.4 us                                                         | 20.1 us: 1.01x faster                                                         |
| unpickle             | 9.71 us                                                         | 9.81 us: 1.01x slower                                                         |
| pickle               | 7.79 us                                                         | 8.04 us: 1.03x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.12x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.2 ms: 1.08x slower                                                         |
| python_startup_no_site | 19.1 ms                                                         | 21.8 ms: 1.14x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.11x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 7.05 ms: 1.41x faster                                                         |
| django_template | 36.9 ms                                                         | 33.0 ms: 1.12x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.26x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                          | 60.7 ns: 1.67x faster                                                         |
| generators                 | 38.5 ms                                                         | 23.2 ms: 1.66x faster                                                         |
| deepcopy_memo              | 38.4 us                                                         | 25.5 us: 1.51x faster                                                         |
| spectral_norm              | 104 ms                                                          | 70.4 ms: 1.48x faster                                                         |
| float                      | 76.7 ms                                                         | 53.6 ms: 1.43x faster                                                         |
| mako                       | 9.96 ms                                                         | 7.05 ms: 1.41x faster                                                         |
| deltablue                  | 3.58 ms                                                         | 2.55 ms: 1.41x faster                                                         |
| coroutines                 | 20.9 ms                                                         | 14.9 ms: 1.40x faster                                                         |
| nbody                      | 127 ms                                                          | 92.1 ms: 1.38x faster                                                         |
| unpack_sequence            | 62.5 ns                                                         | 45.9 ns: 1.36x faster                                                         |
| scimark_sor                | 130 ms                                                          | 95.6 ms: 1.36x faster                                                         |
| async_tree_none_tg         | 278 ms                                                          | 209 ms: 1.33x faster                                                          |
| async_tree_memoization_tg  | 350 ms                                                          | 264 ms: 1.33x faster                                                          |
| typing_runtime_protocols   | 126 us                                                          | 95.3 us: 1.32x faster                                                         |
| tomli_loads                | 2.20 sec                                                        | 1.67 sec: 1.31x faster                                                        |
| pickle_pure_python         | 286 us                                                          | 221 us: 1.29x faster                                                          |
| async_tree_memoization     | 364 ms                                                          | 285 ms: 1.28x faster                                                          |
| comprehensions             | 19.2 us                                                         | 15.1 us: 1.27x faster                                                         |
| async_tree_none            | 298 ms                                                          | 234 ms: 1.27x faster                                                          |
| sqlglot_parse              | 1.25 ms                                                         | 983 us: 1.27x faster                                                          |
| async_tree_io              | 693 ms                                                          | 548 ms: 1.27x faster                                                          |
| unpickle_pure_python       | 210 us                                                          | 166 us: 1.26x faster                                                          |
| xml_etree_process          | 53.2 ms                                                         | 42.6 ms: 1.25x faster                                                         |
| chameleon                  | 7.75 ms                                                         | 6.20 ms: 1.25x faster                                                         |
| sqlglot_transpile          | 1.53 ms                                                         | 1.24 ms: 1.24x faster                                                         |
| async_tree_io_tg           | 677 ms                                                          | 547 ms: 1.24x faster                                                          |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.12 ms: 1.24x faster                                                         |
| deepcopy_reduce            | 3.23 us                                                         | 2.62 us: 1.23x faster                                                         |
| deepcopy                   | 360 us                                                          | 294 us: 1.23x faster                                                          |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 450 ms: 1.21x faster                                                          |
| xml_etree_iterparse        | 77.6 ms                                                         | 64.8 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 473 ms: 1.19x faster                                                          |
| xml_etree_generate         | 72.1 ms                                                         | 60.8 ms: 1.19x faster                                                         |
| logging_simple             | 9.75 us                                                         | 8.34 us: 1.17x faster                                                         |
| logging_format             | 10.4 us                                                         | 8.92 us: 1.17x faster                                                         |
| raytrace                   | 308 ms                                                          | 265 ms: 1.16x faster                                                          |
| pyflate                    | 424 ms                                                          | 364 ms: 1.16x faster                                                          |
| scimark_fft                | 271 ms                                                          | 236 ms: 1.15x faster                                                          |
| go                         | 137 ms                                                          | 121 ms: 1.14x faster                                                          |
| pycparser                  | 978 ms                                                          | 865 ms: 1.13x faster                                                          |
| sympy_sum                  | 123 ms                                                          | 109 ms: 1.13x faster                                                          |
| chaos                      | 69.4 ms                                                         | 61.8 ms: 1.12x faster                                                         |
| regex_compile              | 129 ms                                                          | 115 ms: 1.12x faster                                                          |
| richards                   | 41.3 ms                                                         | 37.0 ms: 1.12x faster                                                         |
| django_template            | 36.9 ms                                                         | 33.0 ms: 1.12x faster                                                         |
| fannkuch                   | 354 ms                                                          | 317 ms: 1.12x faster                                                          |
| 2to3                       | 280 ms                                                          | 252 ms: 1.11x faster                                                          |
| sympy_str                  | 240 ms                                                          | 216 ms: 1.11x faster                                                          |
| json_dumps                 | 7.40 ms                                                         | 6.70 ms: 1.10x faster                                                         |
| richards_super             | 46.5 ms                                                         | 42.1 ms: 1.10x faster                                                         |
| crypto_pyaes               | 69.2 ms                                                         | 63.2 ms: 1.09x faster                                                         |
| bench_thread_pool          | 1.10 ms                                                         | 1.01 ms: 1.09x faster                                                         |
| mdp                        | 1.91 sec                                                        | 1.76 sec: 1.09x faster                                                        |
| sympy_integrate            | 17.5 ms                                                         | 16.2 ms: 1.08x faster                                                         |
| tornado_http               | 105 ms                                                          | 96.9 ms: 1.08x faster                                                         |
| scimark_lu                 | 93.2 ms                                                         | 86.1 ms: 1.08x faster                                                         |
| sqlite_synth               | 2.07 us                                                         | 1.92 us: 1.08x faster                                                         |
| hexiom                     | 6.82 ms                                                         | 6.36 ms: 1.07x faster                                                         |
| async_generators           | 313 ms                                                          | 294 ms: 1.07x faster                                                          |
| meteor_contest             | 86.9 ms                                                         | 81.6 ms: 1.06x faster                                                         |
| scimark_monte_carlo        | 66.4 ms                                                         | 62.5 ms: 1.06x faster                                                         |
| regex_dna                  | 127 ms                                                          | 119 ms: 1.06x faster                                                          |
| asyncio_tcp                | 662 ms                                                          | 623 ms: 1.06x faster                                                          |
| regex_effbot               | 2.04 ms                                                         | 1.92 ms: 1.06x faster                                                         |
| sqlglot_optimize           | 48.5 ms                                                         | 45.7 ms: 1.06x faster                                                         |
| pickle_list                | 3.37 us                                                         | 3.18 us: 1.06x faster                                                         |
| sympy_expand               | 398 ms                                                          | 377 ms: 1.06x faster                                                          |
| pathlib                    | 91.4 ms                                                         | 86.7 ms: 1.05x faster                                                         |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                        |
| xml_etree_parse            | 113 ms                                                          | 108 ms: 1.05x faster                                                          |
| bench_mp_pool              | 75.4 ms                                                         | 72.1 ms: 1.05x faster                                                         |
| nqueens                    | 93.7 ms                                                         | 90.5 ms: 1.04x faster                                                         |
| docutils                   | 1.98 sec                                                        | 1.93 sec: 1.03x faster                                                        |
| unpickle_list              | 2.95 us                                                         | 2.90 us: 1.02x faster                                                         |
| pickle_dict                | 19.9 us                                                         | 19.6 us: 1.02x faster                                                         |
| json_loads                 | 20.4 us                                                         | 20.1 us: 1.01x faster                                                         |
| pprint_pformat             | 1.50 sec                                                        | 1.48 sec: 1.01x faster                                                        |
| pprint_safe_repr           | 721 ms                                                          | 727 ms: 1.01x slower                                                          |
| json                       | 4.15 ms                                                         | 4.19 ms: 1.01x slower                                                         |
| unpickle                   | 9.71 us                                                         | 9.81 us: 1.01x slower                                                         |
| pidigits                   | 199 ms                                                          | 202 ms: 1.01x slower                                                          |
| pickle                     | 7.79 us                                                         | 8.04 us: 1.03x slower                                                         |
| regex_v8                   | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                         |
| python_startup             | 22.4 ms                                                         | 24.2 ms: 1.08x slower                                                         |
| create_gc_cycles           | 652 us                                                          | 738 us: 1.13x slower                                                          |
| python_startup_no_site     | 19.1 ms                                                         | 21.8 ms: 1.14x slower                                                         |
| telco                      | 5.51 ms                                                         | 6.41 ms: 1.16x slower                                                         |
| sqlglot_normalize          | 100 ms                                                          | 238 ms: 2.37x slower                                                          |
| coverage                   | 48.4 ms                                                         | 477 ms: 9.85x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.10x faster                                                                  |

Benchmark hidden because not significant (1): gc_traversal
Ignored benchmarks (6) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown
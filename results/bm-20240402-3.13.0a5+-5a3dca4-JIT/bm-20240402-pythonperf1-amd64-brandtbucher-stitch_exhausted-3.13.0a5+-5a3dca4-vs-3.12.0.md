# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.05x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 222 ms: 1.02x slower                                                          |
| chameleon      | 4.98 ms                                                     | 4.75 ms: 1.05x faster                                                         |
| docutils       | 1.66 sec                                                    | 1.73 sec: 1.04x slower                                                        |
| tornado_http   | 89.5 ms                                                     | 85.2 ms: 1.05x faster                                                         |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 206 ms: 1.38x faster                                                          |
| async_tree_memoization_tg  | 367 ms                                                      | 270 ms: 1.36x faster                                                          |
| async_tree_none            | 291 ms                                                      | 220 ms: 1.32x faster                                                          |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 381 ms: 1.32x faster                                                          |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 379 ms: 1.29x faster                                                          |
| async_tree_io              | 731 ms                                                      | 575 ms: 1.27x faster                                                          |
| async_tree_io_tg           | 771 ms                                                      | 615 ms: 1.25x faster                                                          |
| async_tree_memoization     | 339 ms                                                      | 273 ms: 1.24x faster                                                          |
| Geometric mean             | (ref)                                                       | 1.31x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 57.4 ms: 1.25x faster                                                         |
| float          | 56.8 ms                                                     | 46.6 ms: 1.22x faster                                                         |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                          |
| Geometric mean | (ref)                                                       | 1.17x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 116 ms: 1.09x faster                                                          |
| regex_effbot   | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                         |
| regex_v8       | 14.2 ms                                                     | 15.4 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.21 sec: 1.13x faster                                                        |
| pickle_pure_python   | 195 us                                                      | 178 us: 1.10x faster                                                          |
| json_dumps           | 5.70 ms                                                     | 5.51 ms: 1.03x faster                                                         |
| json_loads           | 13.9 us                                                     | 13.7 us: 1.02x faster                                                         |
| xml_etree_iterparse  | 65.2 ms                                                     | 64.1 ms: 1.02x faster                                                         |
| xml_etree_process    | 37.7 ms                                                     | 37.1 ms: 1.02x faster                                                         |
| unpickle_pure_python | 133 us                                                      | 131 us: 1.02x faster                                                          |
| xml_etree_generate   | 55.8 ms                                                     | 55.0 ms: 1.02x faster                                                         |
| xml_etree_parse      | 93.0 ms                                                     | 92.1 ms: 1.01x faster                                                         |
| pickle               | 7.43 us                                                     | 7.40 us: 1.00x faster                                                         |
| pickle_dict          | 18.4 us                                                     | 18.8 us: 1.02x slower                                                         |
| unpickle_list        | 2.75 us                                                     | 2.84 us: 1.03x slower                                                         |
| unpickle             | 8.18 us                                                     | 8.48 us: 1.04x slower                                                         |
| pickle_list          | 2.83 us                                                     | 3.17 us: 1.12x slower                                                         |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 21.9 ms: 1.13x slower                                                         |
| python_startup_no_site | 16.2 ms                                                     | 19.6 ms: 1.21x slower                                                         |
| Geometric mean         | (ref)                                                       | 1.17x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 7.09 ms                                                     | 5.71 ms: 1.24x faster                                                         |
| django_template | 22.9 ms                                                     | 24.3 ms: 1.06x slower                                                         |
| Geometric mean  | (ref)                                                       | 1.08x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.44 sec: 1.45x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 206 ms: 1.38x faster                                                          |
| async_tree_memoization_tg  | 367 ms                                                      | 270 ms: 1.36x faster                                                          |
| async_tree_none            | 291 ms                                                      | 220 ms: 1.32x faster                                                          |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 381 ms: 1.32x faster                                                          |
| spectral_norm              | 66.9 ms                                                     | 51.2 ms: 1.31x faster                                                         |
| typing_runtime_protocols   | 95.1 us                                                     | 73.0 us: 1.30x faster                                                         |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 379 ms: 1.29x faster                                                          |
| comprehensions             | 14.1 us                                                     | 11.1 us: 1.28x faster                                                         |
| async_tree_io              | 731 ms                                                      | 575 ms: 1.27x faster                                                          |
| async_tree_io_tg           | 771 ms                                                      | 615 ms: 1.25x faster                                                          |
| nbody                      | 71.9 ms                                                     | 57.4 ms: 1.25x faster                                                         |
| async_tree_memoization     | 339 ms                                                      | 273 ms: 1.24x faster                                                          |
| mako                       | 7.09 ms                                                     | 5.71 ms: 1.24x faster                                                         |
| float                      | 56.8 ms                                                     | 46.6 ms: 1.22x faster                                                         |
| tomli_loads                | 1.37 sec                                                    | 1.21 sec: 1.13x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.57 us: 1.12x faster                                                         |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.30 ms: 1.11x faster                                                         |
| deepcopy_memo              | 23.7 us                                                     | 21.5 us: 1.10x faster                                                         |
| generators                 | 22.5 ms                                                     | 20.4 ms: 1.10x faster                                                         |
| pprint_safe_repr           | 513 ms                                                      | 465 ms: 1.10x faster                                                          |
| scimark_fft                | 184 ms                                                      | 168 ms: 1.10x faster                                                          |
| logging_silent             | 60.5 ns                                                     | 55.0 ns: 1.10x faster                                                         |
| chaos                      | 43.3 ms                                                     | 39.5 ms: 1.10x faster                                                         |
| pickle_pure_python         | 195 us                                                      | 178 us: 1.10x faster                                                          |
| regex_dna                  | 126 ms                                                      | 116 ms: 1.09x faster                                                          |
| pprint_pformat             | 1.05 sec                                                    | 961 ms: 1.09x faster                                                          |
| dulwich_log                | 44.3 ms                                                     | 40.9 ms: 1.08x faster                                                         |
| mypy2                      | 509 ms                                                      | 471 ms: 1.08x faster                                                          |
| coroutines                 | 14.3 ms                                                     | 13.2 ms: 1.08x faster                                                         |
| crypto_pyaes               | 48.5 ms                                                     | 45.0 ms: 1.08x faster                                                         |
| fannkuch                   | 247 ms                                                      | 232 ms: 1.06x faster                                                          |
| scimark_monte_carlo        | 43.7 ms                                                     | 41.1 ms: 1.06x faster                                                         |
| json                       | 3.05 ms                                                     | 2.87 ms: 1.06x faster                                                         |
| logging_simple             | 6.28 us                                                     | 5.92 us: 1.06x faster                                                         |
| logging_format             | 6.72 us                                                     | 6.36 us: 1.06x faster                                                         |
| deepcopy                   | 238 us                                                      | 225 us: 1.06x faster                                                          |
| deepcopy_reduce            | 2.09 us                                                     | 1.99 us: 1.05x faster                                                         |
| tornado_http               | 89.5 ms                                                     | 85.2 ms: 1.05x faster                                                         |
| chameleon                  | 4.98 ms                                                     | 4.75 ms: 1.05x faster                                                         |
| deltablue                  | 2.16 ms                                                     | 2.06 ms: 1.05x faster                                                         |
| pyflate                    | 295 ms                                                      | 283 ms: 1.04x faster                                                          |
| raytrace                   | 192 ms                                                      | 185 ms: 1.04x faster                                                          |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                          |
| regex_effbot               | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                         |
| asyncio_tcp                | 487 ms                                                      | 471 ms: 1.04x faster                                                          |
| json_dumps                 | 5.70 ms                                                     | 5.51 ms: 1.03x faster                                                         |
| pathlib                    | 80.5 ms                                                     | 77.8 ms: 1.03x faster                                                         |
| sqlglot_parse              | 804 us                                                      | 780 us: 1.03x faster                                                          |
| bench_thread_pool          | 857 us                                                      | 833 us: 1.03x faster                                                          |
| richards_super             | 32.1 ms                                                     | 31.3 ms: 1.03x faster                                                         |
| pycparser                  | 699 ms                                                      | 684 ms: 1.02x faster                                                          |
| bench_mp_pool              | 69.2 ms                                                     | 67.8 ms: 1.02x faster                                                         |
| sympy_str                  | 175 ms                                                      | 172 ms: 1.02x faster                                                          |
| json_loads                 | 13.9 us                                                     | 13.7 us: 1.02x faster                                                         |
| xml_etree_iterparse        | 65.2 ms                                                     | 64.1 ms: 1.02x faster                                                         |
| sympy_sum                  | 91.5 ms                                                     | 90.1 ms: 1.02x faster                                                         |
| xml_etree_process          | 37.7 ms                                                     | 37.1 ms: 1.02x faster                                                         |
| unpickle_pure_python       | 133 us                                                      | 131 us: 1.02x faster                                                          |
| xml_etree_generate         | 55.8 ms                                                     | 55.0 ms: 1.02x faster                                                         |
| sqlglot_transpile          | 1.02 ms                                                     | 1.01 ms: 1.01x faster                                                         |
| xml_etree_parse            | 93.0 ms                                                     | 92.1 ms: 1.01x faster                                                         |
| richards                   | 28.4 ms                                                     | 28.2 ms: 1.01x faster                                                         |
| pickle                     | 7.43 us                                                     | 7.40 us: 1.00x faster                                                         |
| meteor_contest             | 74.6 ms                                                     | 75.1 ms: 1.01x slower                                                         |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                         |
| async_generators           | 239 ms                                                      | 242 ms: 1.01x slower                                                          |
| scimark_sor                | 78.8 ms                                                     | 80.0 ms: 1.02x slower                                                         |
| 2to3                       | 218 ms                                                      | 222 ms: 1.02x slower                                                          |
| aiohttp                    | 884 us                                                      | 903 us: 1.02x slower                                                          |
| pickle_dict                | 18.4 us                                                     | 18.8 us: 1.02x slower                                                         |
| unpickle_list              | 2.75 us                                                     | 2.84 us: 1.03x slower                                                         |
| unpickle                   | 8.18 us                                                     | 8.48 us: 1.04x slower                                                         |
| sqlglot_optimize           | 34.5 ms                                                     | 35.9 ms: 1.04x slower                                                         |
| docutils                   | 1.66 sec                                                    | 1.73 sec: 1.04x slower                                                        |
| sympy_expand               | 284 ms                                                      | 296 ms: 1.04x slower                                                          |
| sympy_integrate            | 13.0 ms                                                     | 13.6 ms: 1.05x slower                                                         |
| django_template            | 22.9 ms                                                     | 24.3 ms: 1.06x slower                                                         |
| go                         | 91.6 ms                                                     | 97.7 ms: 1.07x slower                                                         |
| regex_v8                   | 14.2 ms                                                     | 15.4 ms: 1.08x slower                                                         |
| mdp                        | 1.37 sec                                                    | 1.49 sec: 1.09x slower                                                        |
| pickle_list                | 2.83 us                                                     | 3.17 us: 1.12x slower                                                         |
| python_startup             | 19.5 ms                                                     | 21.9 ms: 1.13x slower                                                         |
| coverage                   | 40.8 ms                                                     | 46.3 ms: 1.13x slower                                                         |
| create_gc_cycles           | 752 us                                                      | 856 us: 1.14x slower                                                          |
| telco                      | 4.13 ms                                                     | 4.72 ms: 1.14x slower                                                         |
| unpack_sequence            | 37.5 ns                                                     | 44.7 ns: 1.19x slower                                                         |
| hexiom                     | 4.10 ms                                                     | 4.92 ms: 1.20x slower                                                         |
| python_startup_no_site     | 16.2 ms                                                     | 19.6 ms: 1.21x slower                                                         |
| scimark_lu                 | 58.9 ms                                                     | 73.2 ms: 1.24x slower                                                         |
| Geometric mean             | (ref)                                                       | 1.05x faster                                                                  |

Benchmark hidden because not significant (3): nqueens, regex_compile, sqlglot_normalize
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: unknown
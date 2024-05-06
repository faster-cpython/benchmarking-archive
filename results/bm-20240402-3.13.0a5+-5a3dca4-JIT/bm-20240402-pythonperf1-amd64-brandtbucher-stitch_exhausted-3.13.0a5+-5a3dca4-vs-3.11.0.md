# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 222 ms: 1.04x slower                                                          |
| chameleon      | 5.26 ms                                                     | 4.75 ms: 1.11x faster                                                         |
| docutils       | 1.64 sec                                                    | 1.73 sec: 1.05x slower                                                        |
| html5lib       | 38.9 ms                                                     | 36.8 ms: 1.05x faster                                                         |
| tornado_http   | 92.8 ms                                                     | 85.2 ms: 1.09x faster                                                         |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 220 ms: 1.51x faster                                                          |
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                          |
| async_tree_none_tg         | 309 ms                                                      | 206 ms: 1.50x faster                                                          |
| async_tree_memoization     | 399 ms                                                      | 273 ms: 1.46x faster                                                          |
| async_tree_io              | 808 ms                                                      | 575 ms: 1.40x faster                                                          |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 379 ms: 1.40x faster                                                          |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                          |
| async_tree_io_tg           | 829 ms                                                      | 615 ms: 1.35x faster                                                          |
| Geometric mean             | (ref)                                                       | 1.44x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 57.4 ms: 1.23x faster                                                         |
| float          | 54.4 ms                                                     | 46.6 ms: 1.17x faster                                                         |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                       | 1.14x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 87.5 ms: 1.04x faster                                                         |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                         |
| regex_v8       | 14.2 ms                                                     | 15.4 ms: 1.09x slower                                                         |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                  |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.51 ms: 1.47x faster                                                         |
| tomli_loads          | 1.46 sec                                                    | 1.21 sec: 1.21x faster                                                        |
| unpickle_pure_python | 157 us                                                      | 131 us: 1.20x faster                                                          |
| pickle_pure_python   | 208 us                                                      | 178 us: 1.17x faster                                                          |
| xml_etree_parse      | 97.6 ms                                                     | 92.1 ms: 1.06x faster                                                         |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.1 ms: 1.02x faster                                                         |
| pickle_dict          | 18.5 us                                                     | 18.8 us: 1.02x slower                                                         |
| xml_etree_generate   | 52.5 ms                                                     | 55.0 ms: 1.05x slower                                                         |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                                         |
| unpickle_list        | 2.59 us                                                     | 2.84 us: 1.10x slower                                                         |
| pickle               | 6.64 us                                                     | 7.40 us: 1.11x slower                                                         |
| unpickle             | 7.57 us                                                     | 8.48 us: 1.12x slower                                                         |
| pickle_list          | 2.70 us                                                     | 3.17 us: 1.17x slower                                                         |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                                  |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                         |
| python_startup_no_site | 16.8 ms                                                     | 19.6 ms: 1.17x slower                                                         |
| Geometric mean         | (ref)                                                       | 1.14x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.71 ms: 1.33x faster                                                         |
| genshi_text     | 18.4 ms                                                     | 15.6 ms: 1.18x faster                                                         |
| genshi_xml      | 39.9 ms                                                     | 34.6 ms: 1.15x faster                                                         |
| django_template | 24.4 ms                                                     | 24.3 ms: 1.00x faster                                                         |
| Geometric mean  | (ref)                                                       | 1.16x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 73.0 us: 4.46x faster                                                         |
| generators                 | 34.0 ms                                                     | 20.4 ms: 1.66x faster                                                         |
| pylint                     | 323 ms                                                      | 202 ms: 1.60x faster                                                          |
| asyncio_tcp                | 726 ms                                                      | 471 ms: 1.54x faster                                                          |
| async_tree_none            | 332 ms                                                      | 220 ms: 1.51x faster                                                          |
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                          |
| async_tree_none_tg         | 309 ms                                                      | 206 ms: 1.50x faster                                                          |
| json_dumps                 | 8.09 ms                                                     | 5.51 ms: 1.47x faster                                                         |
| async_tree_memoization     | 399 ms                                                      | 273 ms: 1.46x faster                                                          |
| comprehensions             | 15.6 us                                                     | 11.1 us: 1.41x faster                                                         |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.44 sec: 1.41x faster                                                        |
| async_tree_io              | 808 ms                                                      | 575 ms: 1.40x faster                                                          |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 379 ms: 1.40x faster                                                          |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                          |
| async_tree_io_tg           | 829 ms                                                      | 615 ms: 1.35x faster                                                          |
| spectral_norm              | 68.3 ms                                                     | 51.2 ms: 1.33x faster                                                         |
| mako                       | 7.58 ms                                                     | 5.71 ms: 1.33x faster                                                         |
| deltablue                  | 2.70 ms                                                     | 2.06 ms: 1.31x faster                                                         |
| logging_silent             | 71.8 ns                                                     | 55.0 ns: 1.30x faster                                                         |
| richards_super             | 38.7 ms                                                     | 31.3 ms: 1.24x faster                                                         |
| nbody                      | 70.3 ms                                                     | 57.4 ms: 1.23x faster                                                         |
| chaos                      | 48.4 ms                                                     | 39.5 ms: 1.23x faster                                                         |
| sqlglot_parse              | 953 us                                                      | 780 us: 1.22x faster                                                          |
| deepcopy_memo              | 26.0 us                                                     | 21.5 us: 1.21x faster                                                         |
| tomli_loads                | 1.46 sec                                                    | 1.21 sec: 1.21x faster                                                        |
| unpickle_pure_python       | 157 us                                                      | 131 us: 1.20x faster                                                          |
| genshi_text                | 18.4 ms                                                     | 15.6 ms: 1.18x faster                                                         |
| pickle_pure_python         | 208 us                                                      | 178 us: 1.17x faster                                                          |
| float                      | 54.4 ms                                                     | 46.6 ms: 1.17x faster                                                         |
| logging_simple             | 6.86 us                                                     | 5.92 us: 1.16x faster                                                         |
| sqlglot_transpile          | 1.16 ms                                                     | 1.01 ms: 1.16x faster                                                         |
| genshi_xml                 | 39.9 ms                                                     | 34.6 ms: 1.15x faster                                                         |
| raytrace                   | 213 ms                                                      | 185 ms: 1.15x faster                                                          |
| pprint_safe_repr           | 529 ms                                                      | 465 ms: 1.14x faster                                                          |
| dulwich_log                | 46.4 ms                                                     | 40.9 ms: 1.13x faster                                                         |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                                         |
| pprint_pformat             | 1.09 sec                                                    | 961 ms: 1.13x faster                                                          |
| logging_format             | 7.16 us                                                     | 6.36 us: 1.13x faster                                                         |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.12x faster                                                         |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.30 ms: 1.12x faster                                                         |
| richards                   | 31.4 ms                                                     | 28.2 ms: 1.11x faster                                                         |
| sympy_sum                  | 100 ms                                                      | 90.1 ms: 1.11x faster                                                         |
| chameleon                  | 5.26 ms                                                     | 4.75 ms: 1.11x faster                                                         |
| pyflate                    | 312 ms                                                      | 283 ms: 1.10x faster                                                          |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.1 ms: 1.10x faster                                                         |
| deepcopy                   | 246 us                                                      | 225 us: 1.09x faster                                                          |
| fannkuch                   | 253 ms                                                      | 232 ms: 1.09x faster                                                          |
| nqueens                    | 68.3 ms                                                     | 62.5 ms: 1.09x faster                                                         |
| tornado_http               | 92.8 ms                                                     | 85.2 ms: 1.09x faster                                                         |
| crypto_pyaes               | 48.9 ms                                                     | 45.0 ms: 1.09x faster                                                         |
| sympy_str                  | 185 ms                                                      | 172 ms: 1.08x faster                                                          |
| mdp                        | 1.59 sec                                                    | 1.49 sec: 1.07x faster                                                        |
| scimark_fft                | 179 ms                                                      | 168 ms: 1.07x faster                                                          |
| xml_etree_parse            | 97.6 ms                                                     | 92.1 ms: 1.06x faster                                                         |
| html5lib                   | 38.9 ms                                                     | 36.8 ms: 1.05x faster                                                         |
| pycparser                  | 720 ms                                                      | 684 ms: 1.05x faster                                                          |
| unpack_sequence            | 46.9 ns                                                     | 44.7 ns: 1.05x faster                                                         |
| bench_thread_pool          | 872 us                                                      | 833 us: 1.05x faster                                                          |
| regex_compile              | 91.0 ms                                                     | 87.5 ms: 1.04x faster                                                         |
| deepcopy_reduce            | 2.06 us                                                     | 1.99 us: 1.04x faster                                                         |
| go                         | 101 ms                                                      | 97.7 ms: 1.03x faster                                                         |
| sympy_integrate            | 14.0 ms                                                     | 13.6 ms: 1.03x faster                                                         |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                          |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.1 ms: 1.02x faster                                                         |
| sqlglot_normalize          | 190 ms                                                      | 187 ms: 1.02x faster                                                          |
| sympy_expand               | 299 ms                                                      | 296 ms: 1.01x faster                                                          |
| django_template            | 24.4 ms                                                     | 24.3 ms: 1.00x faster                                                         |
| pickle_dict                | 18.5 us                                                     | 18.8 us: 1.02x slower                                                         |
| aiohttp                    | 883 us                                                      | 903 us: 1.02x slower                                                          |
| scimark_sor                | 78.1 ms                                                     | 80.0 ms: 1.02x slower                                                         |
| mypy2                      | 459 ms                                                      | 471 ms: 1.03x slower                                                          |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                         |
| sqlglot_optimize           | 34.5 ms                                                     | 35.9 ms: 1.04x slower                                                         |
| 2to3                       | 214 ms                                                      | 222 ms: 1.04x slower                                                          |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                         |
| xml_etree_generate         | 52.5 ms                                                     | 55.0 ms: 1.05x slower                                                         |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                                         |
| docutils                   | 1.64 sec                                                    | 1.73 sec: 1.05x slower                                                        |
| coverage                   | 43.4 ms                                                     | 46.3 ms: 1.07x slower                                                         |
| bench_mp_pool              | 63.2 ms                                                     | 67.8 ms: 1.07x slower                                                         |
| hexiom                     | 4.55 ms                                                     | 4.92 ms: 1.08x slower                                                         |
| regex_v8                   | 14.2 ms                                                     | 15.4 ms: 1.09x slower                                                         |
| pathlib                    | 70.9 ms                                                     | 77.8 ms: 1.10x slower                                                         |
| unpickle_list              | 2.59 us                                                     | 2.84 us: 1.10x slower                                                         |
| python_startup             | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                         |
| pickle                     | 6.64 us                                                     | 7.40 us: 1.11x slower                                                         |
| unpickle                   | 7.57 us                                                     | 8.48 us: 1.12x slower                                                         |
| telco                      | 4.06 ms                                                     | 4.72 ms: 1.16x slower                                                         |
| scimark_lu                 | 62.8 ms                                                     | 73.2 ms: 1.17x slower                                                         |
| python_startup_no_site     | 16.8 ms                                                     | 19.6 ms: 1.17x slower                                                         |
| pickle_list                | 2.70 us                                                     | 3.17 us: 1.17x slower                                                         |
| create_gc_cycles           | 713 us                                                      | 856 us: 1.20x slower                                                          |
| async_generators           | 177 ms                                                      | 242 ms: 1.37x slower                                                          |
| thrift                     | 494 us                                                      | 9.22 ms: 18.67x slower                                                        |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                                  |

Benchmark hidden because not significant (4): json, meteor_contest, regex_dna, xml_etree_process
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown
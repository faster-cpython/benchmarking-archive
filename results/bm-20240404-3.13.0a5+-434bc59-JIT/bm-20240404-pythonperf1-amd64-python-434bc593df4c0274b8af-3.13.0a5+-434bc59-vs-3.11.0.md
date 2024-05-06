# Results vs. 3.11.0

- fork: python
- ref: 434bc593df4c0274b8af
- machine: windows-amd64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 218 ms: 1.02x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.69 ms: 1.12x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                      |
| html5lib       | 38.9 ms                                                     | 35.1 ms: 1.11x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 82.8 ms: 1.12x faster                                                       |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 262 ms: 1.54x faster                                                        |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 266 ms: 1.50x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 212 ms: 1.46x faster                                                        |
| async_tree_io              | 808 ms                                                      | 581 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 384 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.44x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 57.0 ms: 1.23x faster                                                       |
| float          | 54.4 ms                                                     | 46.7 ms: 1.17x faster                                                       |
| pidigits       | 150 ms                                                      | 146 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                       | 1.14x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 86.5 ms: 1.05x faster                                                       |
| regex_dna      | 116 ms                                                      | 119 ms: 1.03x slower                                                        |
| regex_v8       | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.58 ms: 1.45x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.17 sec: 1.24x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 129 us: 1.22x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                        |
| xml_etree_iterparse  | 65.6 ms                                                     | 59.7 ms: 1.10x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 89.5 ms: 1.09x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.2 ms: 1.03x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.6 us: 1.00x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.77 us: 1.07x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.89 us: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.33 us: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.66 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.06x faster                                                                |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                       |
| python_startup_no_site | 16.8 ms                                                     | 19.7 ms: 1.17x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.14x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 5.73 ms: 1.32x faster                                                       |
| genshi_text    | 18.4 ms                                                     | 14.8 ms: 1.25x faster                                                       |
| genshi_xml     | 39.9 ms                                                     | 32.4 ms: 1.23x faster                                                       |
| Geometric mean | (ref)                                                       | 1.27x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 71.8 us: 4.54x faster                                                       |
| generators                 | 34.0 ms                                                     | 19.6 ms: 1.73x faster                                                       |
| pylint                     | 323 ms                                                      | 193 ms: 1.67x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 262 ms: 1.54x faster                                                        |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 476 ms: 1.52x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 266 ms: 1.50x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 212 ms: 1.46x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.58 ms: 1.45x faster                                                       |
| comprehensions             | 15.6 us                                                     | 11.1 us: 1.41x faster                                                       |
| async_tree_io              | 808 ms                                                      | 581 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 384 ms: 1.38x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.47 sec: 1.38x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 50.7 ms: 1.35x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 53.4 ns: 1.34x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.73 ms: 1.32x faster                                                       |
| raytrace                   | 213 ms                                                      | 164 ms: 1.30x faster                                                        |
| richards_super             | 38.7 ms                                                     | 30.2 ms: 1.28x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.14 ms: 1.26x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.3 ms: 1.26x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 14.8 ms: 1.25x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.17 sec: 1.24x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 769 us: 1.24x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 21.0 us: 1.24x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 32.4 ms: 1.23x faster                                                       |
| nbody                      | 70.3 ms                                                     | 57.0 ms: 1.23x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 129 us: 1.22x faster                                                        |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                        |
| logging_simple             | 6.86 us                                                     | 5.68 us: 1.21x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 985 us: 1.18x faster                                                        |
| richards                   | 31.4 ms                                                     | 26.7 ms: 1.18x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.10 us: 1.17x faster                                                       |
| float                      | 54.4 ms                                                     | 46.7 ms: 1.17x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.0 ms: 1.16x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.22 ms: 1.16x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.38 sec: 1.16x faster                                                      |
| pprint_pformat             | 1.09 sec                                                    | 942 ms: 1.15x faster                                                        |
| coroutines                 | 15.0 ms                                                     | 13.0 ms: 1.15x faster                                                       |
| pyflate                    | 312 ms                                                      | 271 ms: 1.15x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 463 ms: 1.14x faster                                                        |
| sympy_sum                  | 100 ms                                                      | 87.7 ms: 1.14x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.9 ms: 1.13x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.13x faster                                                       |
| deepcopy                   | 246 us                                                      | 219 us: 1.13x faster                                                        |
| chameleon                  | 5.26 ms                                                     | 4.69 ms: 1.12x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 82.8 ms: 1.12x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 61.0 ms: 1.12x faster                                                       |
| sympy_str                  | 185 ms                                                      | 166 ms: 1.11x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 35.1 ms: 1.11x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 59.7 ms: 1.10x faster                                                       |
| go                         | 101 ms                                                      | 92.1 ms: 1.10x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 44.5 ms: 1.10x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 89.5 ms: 1.09x faster                                                       |
| fannkuch                   | 253 ms                                                      | 234 ms: 1.08x faster                                                        |
| bench_thread_pool          | 872 us                                                      | 808 us: 1.08x faster                                                        |
| scimark_fft                | 179 ms                                                      | 166 ms: 1.08x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 178 ms: 1.07x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 13.2 ms: 1.06x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.95 us: 1.06x faster                                                       |
| sympy_expand               | 299 ms                                                      | 283 ms: 1.06x faster                                                        |
| regex_compile              | 91.0 ms                                                     | 86.5 ms: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 71.5 ms: 1.05x faster                                                       |
| pycparser                  | 720 ms                                                      | 690 ms: 1.04x faster                                                        |
| hexiom                     | 4.55 ms                                                     | 4.41 ms: 1.03x faster                                                       |
| mypy2                      | 459 ms                                                      | 446 ms: 1.03x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.2 ms: 1.03x faster                                                       |
| pidigits                   | 150 ms                                                      | 146 ms: 1.03x faster                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 34.4 ms: 1.00x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 18.6 us: 1.00x slower                                                       |
| aiohttp                    | 883 us                                                      | 893 us: 1.01x slower                                                        |
| 2to3                       | 214 ms                                                      | 218 ms: 1.02x slower                                                        |
| scimark_sor                | 78.1 ms                                                     | 80.0 ms: 1.02x slower                                                       |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.03x slower                                                        |
| docutils                   | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.77 us: 1.07x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 67.7 ms: 1.07x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.89 us: 1.07x slower                                                       |
| coverage                   | 43.4 ms                                                     | 46.7 ms: 1.08x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 77.6 ms: 1.09x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.33 us: 1.10x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 69.5 ms: 1.11x slower                                                       |
| python_startup             | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.66 us: 1.14x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 19.7 ms: 1.17x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.80 ms: 1.18x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 904 us: 1.27x slower                                                        |
| async_generators           | 177 ms                                                      | 234 ms: 1.32x slower                                                        |
| thrift                     | 494 us                                                      | 8.76 ms: 17.75x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (2): json, xml_etree_generate
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown
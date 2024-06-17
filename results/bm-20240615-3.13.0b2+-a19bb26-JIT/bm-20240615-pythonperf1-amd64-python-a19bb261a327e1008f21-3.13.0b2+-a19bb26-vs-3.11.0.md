# Results vs. 3.11.0

- fork: python
- ref: a19bb261a327e1008f21
- machine: windows-amd64
- commit hash: a19bb26
- commit date: 2024-06-15
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 229 ms: 1.07x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.95 ms: 1.06x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.78 sec: 1.08x slower                                                      |
| html5lib       | 38.9 ms                                                     | 37.8 ms: 1.03x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 85.7 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 228 ms: 1.46x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 276 ms: 1.45x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 214 ms: 1.44x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| async_tree_io              | 808 ms                                                      | 603 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 397 ms: 1.33x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 622 ms: 1.33x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 51.4 ms: 1.37x faster                                                       |
| float          | 54.4 ms                                                     | 43.5 ms: 1.25x faster                                                       |
| Geometric mean | (ref)                                                       | 1.20x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 88.9 ms: 1.02x faster                                                       |
| regex_dna      | 116 ms                                                      | 119 ms: 1.02x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 22.7 ms: 1.61x slower                                                       |
| Geometric mean | (ref)                                                       | 1.14x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.69 ms: 1.42x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 125 us: 1.25x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 91.7 ms: 1.06x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 17.5 us: 1.06x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 51.3 ms: 1.02x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.6 ms: 1.02x faster                                                       |
| pickle_list          | 2.70 us                                                     | 2.86 us: 1.06x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.28 us: 1.10x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.85 us: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.98 us: 1.19x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                                       |
| python_startup         | 19.8 ms                                                     | 22.0 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.09x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.18 ms: 1.47x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 18.0 ms: 1.03x faster                                                       |
| django_template | 24.4 ms                                                     | 25.4 ms: 1.04x slower                                                       |
| genshi_xml      | 39.9 ms                                                     | 44.6 ms: 1.12x slower                                                       |
| Geometric mean  | (ref)                                                       | 1.07x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 110 us: 2.96x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 471 ms: 1.54x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.54x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 45.1 ms: 1.52x faster                                                       |
| generators                 | 34.0 ms                                                     | 22.5 ms: 1.51x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| mako                       | 7.58 ms                                                     | 5.18 ms: 1.47x faster                                                       |
| async_tree_none            | 332 ms                                                      | 228 ms: 1.46x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 276 ms: 1.45x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 214 ms: 1.44x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.69 ms: 1.42x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.45 sec: 1.40x faster                                                      |
| pylint                     | 323 ms                                                      | 236 ms: 1.37x faster                                                        |
| nbody                      | 70.3 ms                                                     | 51.4 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| async_tree_io              | 808 ms                                                      | 603 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 397 ms: 1.33x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 622 ms: 1.33x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 20.1 us: 1.29x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 55.6 ns: 1.29x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 125 us: 1.25x faster                                                        |
| float                      | 54.4 ms                                                     | 43.5 ms: 1.25x faster                                                       |
| chaos                      | 48.4 ms                                                     | 39.2 ms: 1.23x faster                                                       |
| raytrace                   | 213 ms                                                      | 175 ms: 1.22x faster                                                        |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                        |
| pyflate                    | 312 ms                                                      | 259 ms: 1.21x faster                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.14 ms: 1.20x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 41.0 ms: 1.19x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.77 us: 1.19x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.2 ms: 1.19x faster                                                       |
| scimark_fft                | 179 ms                                                      | 152 ms: 1.18x faster                                                        |
| sqlglot_parse              | 953 us                                                      | 809 us: 1.18x faster                                                        |
| mdp                        | 1.59 sec                                                    | 1.36 sec: 1.17x faster                                                      |
| richards_super             | 38.7 ms                                                     | 33.0 ms: 1.17x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 452 ms: 1.17x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 929 ms: 1.17x faster                                                        |
| logging_format             | 7.16 us                                                     | 6.19 us: 1.16x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.36 ms: 1.14x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.7 ms: 1.14x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 60.5 ms: 1.13x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.58 us: 1.12x faster                                                       |
| fannkuch                   | 253 ms                                                      | 226 ms: 1.12x faster                                                        |
| sqlglot_transpile          | 1.16 ms                                                     | 1.04 ms: 1.12x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.5 ms: 1.11x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 792 us: 1.10x faster                                                        |
| go                         | 101 ms                                                      | 93.2 ms: 1.08x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 85.7 ms: 1.08x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| richards                   | 31.4 ms                                                     | 29.1 ms: 1.08x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 93.6 ms: 1.07x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 91.7 ms: 1.06x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.95 ms: 1.06x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 17.5 us: 1.06x faster                                                       |
| deepcopy                   | 246 us                                                      | 237 us: 1.04x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 18.0 ms: 1.03x faster                                                       |
| sympy_str                  | 185 ms                                                      | 180 ms: 1.03x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 37.8 ms: 1.03x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 88.9 ms: 1.02x faster                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 51.3 ms: 1.02x faster                                                       |
| xml_etree_process          | 37.2 ms                                                     | 36.6 ms: 1.02x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 74.1 ms: 1.01x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.04 sec: 1.00x slower                                                      |
| deepcopy_reduce            | 2.06 us                                                     | 2.08 us: 1.01x slower                                                       |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.02x slower                                                        |
| coverage                   | 43.4 ms                                                     | 44.5 ms: 1.03x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 4.68 ms: 1.03x slower                                                       |
| django_template            | 24.4 ms                                                     | 25.4 ms: 1.04x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| aiohttp                    | 883 us                                                      | 932 us: 1.05x slower                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                                       |
| sympy_expand               | 299 ms                                                      | 316 ms: 1.06x slower                                                        |
| scimark_sor                | 78.1 ms                                                     | 82.7 ms: 1.06x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.86 us: 1.06x slower                                                       |
| pycparser                  | 720 ms                                                      | 764 ms: 1.06x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 36.9 ms: 1.07x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 76.0 ms: 1.07x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                       |
| 2to3                       | 214 ms                                                      | 229 ms: 1.07x slower                                                        |
| docutils                   | 1.64 sec                                                    | 1.78 sec: 1.08x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 68.9 ms: 1.09x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.28 us: 1.10x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.85 us: 1.10x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 69.6 ms: 1.11x slower                                                       |
| python_startup             | 19.8 ms                                                     | 22.0 ms: 1.11x slower                                                       |
| genshi_xml                 | 39.9 ms                                                     | 44.6 ms: 1.12x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.56 ms: 1.12x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.98 us: 1.19x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 917 us: 1.29x slower                                                        |
| async_generators           | 177 ms                                                      | 250 ms: 1.41x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 22.7 ms: 1.61x slower                                                       |
| thrift                     | 494 us                                                      | 8.96 ms: 18.14x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                                |

Benchmark hidden because not significant (3): json, pidigits, sympy_integrate
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown
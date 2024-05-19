# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: windows-amd64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.04x faster
- HPT reliability: 54.88%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 229 ms: 1.07x slower                                                       |
| chameleon      | 5.26 ms                                                     | 5.12 ms: 1.03x faster                                                      |
| docutils       | 1.64 sec                                                    | 1.83 sec: 1.11x slower                                                     |
| html5lib       | 38.9 ms                                                     | 41.5 ms: 1.07x slower                                                      |
| tornado_http   | 92.8 ms                                                     | 87.0 ms: 1.07x faster                                                      |
| Geometric mean | (ref)                                                       | 1.03x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 272 ms: 1.49x faster                                                       |
| async_tree_none            | 332 ms                                                      | 231 ms: 1.44x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 217 ms: 1.42x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 388 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 400 ms: 1.32x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 628 ms: 1.32x faster                                                       |
| async_tree_io              | 808 ms                                                      | 612 ms: 1.32x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 53.6 ms: 1.01x faster                                                      |
| pidigits       | 150 ms                                                      | 151 ms: 1.01x slower                                                       |
| nbody          | 70.3 ms                                                     | 75.0 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                       | 1.02x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 116 ms                                                      | 119 ms: 1.03x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                      |
| regex_v8       | 14.2 ms                                                     | 15.9 ms: 1.12x slower                                                      |
| regex_compile  | 91.0 ms                                                     | 106 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                       | 1.09x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.81 ms: 1.39x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 90.3 ms: 1.08x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 155 us: 1.01x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.4 us: 1.01x faster                                                      |
| tomli_loads          | 1.46 sec                                                    | 1.47 sec: 1.01x slower                                                     |
| pickle_pure_python   | 208 us                                                      | 217 us: 1.04x slower                                                       |
| xml_etree_process    | 37.2 ms                                                     | 39.5 ms: 1.06x slower                                                      |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                      |
| pickle               | 6.64 us                                                     | 7.11 us: 1.07x slower                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 56.6 ms: 1.08x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.81 us: 1.09x slower                                                      |
| pickle_list          | 2.70 us                                                     | 2.93 us: 1.09x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.58 us: 1.13x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.01x slower                                                               |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                      |
| python_startup         | 19.8 ms                                                     | 20.0 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 37.6 ms: 1.06x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 17.4 ms: 1.06x faster                                                      |
| mako            | 7.58 ms                                                     | 7.35 ms: 1.03x faster                                                      |
| django_template | 24.4 ms                                                     | 25.1 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                       | 1.03x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 116 us: 2.82x faster                                                       |
| generators                 | 34.0 ms                                                     | 19.9 ms: 1.71x faster                                                      |
| asyncio_tcp                | 726 ms                                                      | 474 ms: 1.53x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 272 ms: 1.49x faster                                                       |
| async_tree_none            | 332 ms                                                      | 231 ms: 1.44x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 217 ms: 1.42x faster                                                       |
| pylint                     | 323 ms                                                      | 232 ms: 1.39x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.81 ms: 1.39x faster                                                      |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.50 sec: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 388 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 400 ms: 1.32x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 628 ms: 1.32x faster                                                       |
| async_tree_io              | 808 ms                                                      | 612 ms: 1.32x faster                                                       |
| richards_super             | 38.7 ms                                                     | 32.0 ms: 1.21x faster                                                      |
| comprehensions             | 15.6 us                                                     | 13.1 us: 1.19x faster                                                      |
| raytrace                   | 213 ms                                                      | 180 ms: 1.18x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.8 ms: 1.17x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.40 sec: 1.14x faster                                                     |
| chaos                      | 48.4 ms                                                     | 43.2 ms: 1.12x faster                                                      |
| richards                   | 31.4 ms                                                     | 28.2 ms: 1.11x faster                                                      |
| logging_simple             | 6.86 us                                                     | 6.23 us: 1.10x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.63 us: 1.09x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 881 us: 1.08x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 90.3 ms: 1.08x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.67 us: 1.07x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 87.0 ms: 1.07x faster                                                      |
| genshi_xml                 | 39.9 ms                                                     | 37.6 ms: 1.06x faster                                                      |
| genshi_text                | 18.4 ms                                                     | 17.4 ms: 1.06x faster                                                      |
| logging_silent             | 71.8 ns                                                     | 68.2 ns: 1.05x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 1.12 ms: 1.04x faster                                                      |
| deltablue                  | 2.70 ms                                                     | 2.59 ms: 1.04x faster                                                      |
| bench_thread_pool          | 872 us                                                      | 839 us: 1.04x faster                                                       |
| mako                       | 7.58 ms                                                     | 7.35 ms: 1.03x faster                                                      |
| nqueens                    | 68.3 ms                                                     | 66.4 ms: 1.03x faster                                                      |
| chameleon                  | 5.26 ms                                                     | 5.12 ms: 1.03x faster                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                      |
| float                      | 54.4 ms                                                     | 53.6 ms: 1.01x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 155 us: 1.01x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 99.3 ms: 1.01x faster                                                      |
| pickle_dict                | 18.5 us                                                     | 18.4 us: 1.01x faster                                                      |
| go                         | 101 ms                                                      | 100 ms: 1.01x faster                                                       |
| pidigits                   | 150 ms                                                      | 151 ms: 1.01x slower                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 49.2 ms: 1.01x slower                                                      |
| python_startup             | 19.8 ms                                                     | 20.0 ms: 1.01x slower                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.47 sec: 1.01x slower                                                     |
| deepcopy                   | 246 us                                                      | 249 us: 1.01x slower                                                       |
| meteor_contest             | 75.2 ms                                                     | 76.7 ms: 1.02x slower                                                      |
| django_template            | 24.4 ms                                                     | 25.1 ms: 1.03x slower                                                      |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.03x slower                                                       |
| coverage                   | 43.4 ms                                                     | 44.8 ms: 1.03x slower                                                      |
| sympy_integrate            | 14.0 ms                                                     | 14.5 ms: 1.03x slower                                                      |
| thrift                     | 494 us                                                      | 511 us: 1.04x slower                                                       |
| pyflate                    | 312 ms                                                      | 324 ms: 1.04x slower                                                       |
| pickle_pure_python         | 208 us                                                      | 217 us: 1.04x slower                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.15 us: 1.04x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                      |
| scimark_monte_carlo        | 45.3 ms                                                     | 47.6 ms: 1.05x slower                                                      |
| sympy_str                  | 185 ms                                                      | 195 ms: 1.05x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                      |
| fannkuch                   | 253 ms                                                      | 267 ms: 1.06x slower                                                       |
| xml_etree_process          | 37.2 ms                                                     | 39.5 ms: 1.06x slower                                                      |
| nbody                      | 70.3 ms                                                     | 75.0 ms: 1.07x slower                                                      |
| html5lib                   | 38.9 ms                                                     | 41.5 ms: 1.07x slower                                                      |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 67.6 ms: 1.07x slower                                                      |
| pickle                     | 6.64 us                                                     | 7.11 us: 1.07x slower                                                      |
| 2to3                       | 214 ms                                                      | 229 ms: 1.07x slower                                                       |
| deepcopy_memo              | 26.0 us                                                     | 28.0 us: 1.08x slower                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 56.6 ms: 1.08x slower                                                      |
| pycparser                  | 720 ms                                                      | 777 ms: 1.08x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.81 us: 1.09x slower                                                      |
| pickle_list                | 2.70 us                                                     | 2.93 us: 1.09x slower                                                      |
| scimark_fft                | 179 ms                                                      | 195 ms: 1.09x slower                                                       |
| spectral_norm              | 68.3 ms                                                     | 74.5 ms: 1.09x slower                                                      |
| scimark_sor                | 78.1 ms                                                     | 86.3 ms: 1.10x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.83 sec: 1.11x slower                                                     |
| sqlglot_optimize           | 34.5 ms                                                     | 38.6 ms: 1.12x slower                                                      |
| pathlib                    | 70.9 ms                                                     | 79.2 ms: 1.12x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 15.9 ms: 1.12x slower                                                      |
| sympy_expand               | 299 ms                                                      | 337 ms: 1.13x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.58 us: 1.13x slower                                                      |
| hexiom                     | 4.55 ms                                                     | 5.23 ms: 1.15x slower                                                      |
| regex_compile              | 91.0 ms                                                     | 106 ms: 1.16x slower                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 3.01 ms: 1.17x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.91 ms: 1.21x slower                                                      |
| scimark_lu                 | 62.8 ms                                                     | 77.2 ms: 1.23x slower                                                      |
| create_gc_cycles           | 713 us                                                      | 912 us: 1.28x slower                                                       |
| async_generators           | 177 ms                                                      | 245 ms: 1.38x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.04x faster                                                               |

Benchmark hidden because not significant (5): json, xml_etree_iterparse, pprint_pformat, flaskblogging, pprint_safe_repr
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 54.88% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
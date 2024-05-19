# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: windows-amd64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 232 ms: 1.09x slower                                                       |
| chameleon      | 5.26 ms                                                     | 5.11 ms: 1.03x faster                                                      |
| docutils       | 1.64 sec                                                    | 1.76 sec: 1.07x slower                                                     |
| html5lib       | 38.9 ms                                                     | 37.2 ms: 1.04x faster                                                      |
| tornado_http   | 92.8 ms                                                     | 84.9 ms: 1.09x faster                                                      |
| Geometric mean | (ref)                                                       | 1.00x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 269 ms: 1.51x faster                                                       |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 272 ms: 1.47x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 211 ms: 1.46x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 612 ms: 1.35x faster                                                       |
| async_tree_io              | 808 ms                                                      | 598 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 388 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 394 ms: 1.34x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.41x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 50.5 ms: 1.39x faster                                                      |
| float          | 54.4 ms                                                     | 44.2 ms: 1.23x faster                                                      |
| pidigits       | 150 ms                                                      | 149 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                       | 1.20x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 87.2 ms: 1.04x faster                                                      |
| regex_v8       | 14.2 ms                                                     | 14.3 ms: 1.01x slower                                                      |
| regex_dna      | 116 ms                                                      | 119 ms: 1.03x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                       | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.75 ms: 1.41x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 125 us: 1.25x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 173 us: 1.20x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.23 sec: 1.18x faster                                                     |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.1 ms: 1.09x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 91.5 ms: 1.07x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 17.5 us: 1.05x faster                                                      |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 51.8 ms: 1.02x faster                                                      |
| pickle_list          | 2.70 us                                                     | 2.90 us: 1.08x slower                                                      |
| json_loads           | 13.0 us                                                     | 14.1 us: 1.09x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.87 us: 1.11x slower                                                      |
| pickle               | 6.64 us                                                     | 7.37 us: 1.11x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.69 us: 1.15x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 18.1 ms: 1.08x slower                                                      |
| python_startup         | 19.8 ms                                                     | 21.8 ms: 1.10x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.09x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.17 ms: 1.47x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 17.8 ms: 1.03x faster                                                      |
| django_template | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                      |
| genshi_xml      | 39.9 ms                                                     | 44.7 ms: 1.12x slower                                                      |
| Geometric mean  | (ref)                                                       | 1.07x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 111 us: 2.94x faster                                                       |
| generators                 | 34.0 ms                                                     | 21.6 ms: 1.57x faster                                                      |
| comprehensions             | 15.6 us                                                     | 10.3 us: 1.52x faster                                                      |
| spectral_norm              | 68.3 ms                                                     | 45.1 ms: 1.52x faster                                                      |
| asyncio_tcp                | 726 ms                                                      | 481 ms: 1.51x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 269 ms: 1.51x faster                                                       |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 272 ms: 1.47x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.17 ms: 1.47x faster                                                      |
| async_tree_none_tg         | 309 ms                                                      | 211 ms: 1.46x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.75 ms: 1.41x faster                                                      |
| nbody                      | 70.3 ms                                                     | 50.5 ms: 1.39x faster                                                      |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.46 sec: 1.39x faster                                                     |
| pylint                     | 323 ms                                                      | 236 ms: 1.37x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 612 ms: 1.35x faster                                                       |
| async_tree_io              | 808 ms                                                      | 598 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 388 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 394 ms: 1.34x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 56.0 ns: 1.28x faster                                                      |
| deepcopy_memo              | 26.0 us                                                     | 20.6 us: 1.26x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 125 us: 1.25x faster                                                       |
| chaos                      | 48.4 ms                                                     | 39.2 ms: 1.23x faster                                                      |
| float                      | 54.4 ms                                                     | 44.2 ms: 1.23x faster                                                      |
| pyflate                    | 312 ms                                                      | 257 ms: 1.21x faster                                                       |
| raytrace                   | 213 ms                                                      | 176 ms: 1.21x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 173 us: 1.20x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.75 us: 1.19x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 799 us: 1.19x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 41.0 ms: 1.19x faster                                                      |
| scimark_fft                | 179 ms                                                      | 151 ms: 1.19x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.17 ms: 1.18x faster                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.23 sec: 1.18x faster                                                     |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.5 ms: 1.18x faster                                                      |
| richards_super             | 38.7 ms                                                     | 33.3 ms: 1.16x faster                                                      |
| deltablue                  | 2.70 ms                                                     | 2.33 ms: 1.16x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.21 us: 1.15x faster                                                      |
| pprint_safe_repr           | 529 ms                                                      | 459 ms: 1.15x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 945 ms: 1.15x faster                                                       |
| fannkuch                   | 253 ms                                                      | 222 ms: 1.14x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.14x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.56 us: 1.13x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 1.03 ms: 1.13x faster                                                      |
| nqueens                    | 68.3 ms                                                     | 61.0 ms: 1.12x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 84.9 ms: 1.09x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.1 ms: 1.09x faster                                                      |
| sympy_sum                  | 100 ms                                                      | 92.5 ms: 1.08x faster                                                      |
| go                         | 101 ms                                                      | 93.8 ms: 1.08x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.48 sec: 1.07x faster                                                     |
| xml_etree_parse            | 97.6 ms                                                     | 91.5 ms: 1.07x faster                                                      |
| richards                   | 31.4 ms                                                     | 29.5 ms: 1.07x faster                                                      |
| pickle_dict                | 18.5 us                                                     | 17.5 us: 1.05x faster                                                      |
| sympy_str                  | 185 ms                                                      | 177 ms: 1.05x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 37.2 ms: 1.04x faster                                                      |
| regex_compile              | 91.0 ms                                                     | 87.2 ms: 1.04x faster                                                      |
| bench_thread_pool          | 872 us                                                      | 842 us: 1.04x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 17.8 ms: 1.03x faster                                                      |
| deepcopy                   | 246 us                                                      | 238 us: 1.03x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 5.11 ms: 1.03x faster                                                      |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 51.8 ms: 1.02x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 74.5 ms: 1.01x faster                                                      |
| pidigits                   | 150 ms                                                      | 149 ms: 1.00x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                     |
| regex_v8                   | 14.2 ms                                                     | 14.3 ms: 1.01x slower                                                      |
| hexiom                     | 4.55 ms                                                     | 4.65 ms: 1.02x slower                                                      |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.03x slower                                                       |
| sympy_expand               | 299 ms                                                      | 309 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                      |
| pycparser                  | 720 ms                                                      | 750 ms: 1.04x slower                                                       |
| thrift                     | 494 us                                                      | 516 us: 1.05x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| django_template            | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                      |
| coverage                   | 43.4 ms                                                     | 45.8 ms: 1.06x slower                                                      |
| scimark_sor                | 78.1 ms                                                     | 82.8 ms: 1.06x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 36.7 ms: 1.06x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.76 sec: 1.07x slower                                                     |
| python_startup_no_site     | 16.8 ms                                                     | 18.1 ms: 1.08x slower                                                      |
| pickle_list                | 2.70 us                                                     | 2.90 us: 1.08x slower                                                      |
| json_loads                 | 13.0 us                                                     | 14.1 us: 1.09x slower                                                      |
| 2to3                       | 214 ms                                                      | 232 ms: 1.09x slower                                                       |
| python_startup             | 19.8 ms                                                     | 21.8 ms: 1.10x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.48 ms: 1.10x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.87 us: 1.11x slower                                                      |
| pickle                     | 6.64 us                                                     | 7.37 us: 1.11x slower                                                      |
| scimark_lu                 | 62.8 ms                                                     | 69.9 ms: 1.11x slower                                                      |
| pathlib                    | 70.9 ms                                                     | 78.8 ms: 1.11x slower                                                      |
| genshi_xml                 | 39.9 ms                                                     | 44.7 ms: 1.12x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 71.3 ms: 1.13x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.69 us: 1.15x slower                                                      |
| create_gc_cycles           | 713 us                                                      | 907 us: 1.27x slower                                                       |
| async_generators           | 177 ms                                                      | 257 ms: 1.45x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                               |

Benchmark hidden because not significant (3): json, sympy_integrate, deepcopy_reduce
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown
# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: windows-amd64
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.14x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 207 ms: 1.03x faster                                                       |
| chameleon      | 5.26 ms                                                     | 4.79 ms: 1.10x faster                                                      |
| docutils       | 1.64 sec                                                    | 1.60 sec: 1.02x faster                                                     |
| html5lib       | 38.9 ms                                                     | 35.6 ms: 1.09x faster                                                      |
| tornado_http   | 92.8 ms                                                     | 82.3 ms: 1.13x faster                                                      |
| Geometric mean | (ref)                                                       | 1.07x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 252 ms: 1.61x faster                                                       |
| async_tree_none            | 332 ms                                                      | 215 ms: 1.55x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 260 ms: 1.53x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 205 ms: 1.51x faster                                                       |
| async_tree_io              | 808 ms                                                      | 578 ms: 1.40x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 598 ms: 1.39x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 384 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.46x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 51.2 ms: 1.06x faster                                                      |
| nbody          | 70.3 ms                                                     | 69.4 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                       | 1.02x faster                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 77.9 ms: 1.17x faster                                                      |
| regex_dna      | 116 ms                                                      | 119 ms: 1.02x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 14.8 ms: 1.04x slower                                                      |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                      |
| Geometric mean | (ref)                                                       | 1.01x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.57 ms: 1.45x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 126 us: 1.25x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 176 us: 1.18x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 90.5 ms: 1.08x faster                                                      |
| tomli_loads          | 1.46 sec                                                    | 1.36 sec: 1.07x faster                                                     |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.8 ms: 1.04x faster                                                      |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 18.2 us: 1.02x faster                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 52.9 ms: 1.01x slower                                                      |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.81 us: 1.09x slower                                                      |
| pickle               | 6.64 us                                                     | 7.25 us: 1.09x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.56 us: 1.13x slower                                                      |
| pickle_list          | 2.70 us                                                     | 3.23 us: 1.20x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.4 ms: 1.02x faster                                                      |
| python_startup         | 19.8 ms                                                     | 20.0 ms: 1.01x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 31.5 ms: 1.27x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 14.8 ms: 1.25x faster                                                      |
| mako            | 7.58 ms                                                     | 6.53 ms: 1.16x faster                                                      |
| django_template | 24.4 ms                                                     | 21.8 ms: 1.12x faster                                                      |
| Geometric mean  | (ref)                                                       | 1.20x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1-amd64-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 99.7 us: 3.27x faster                                                      |
| generators                 | 34.0 ms                                                     | 20.1 ms: 1.69x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 252 ms: 1.61x faster                                                       |
| pylint                     | 323 ms                                                      | 206 ms: 1.57x faster                                                       |
| async_tree_none            | 332 ms                                                      | 215 ms: 1.55x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 260 ms: 1.53x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 476 ms: 1.53x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 205 ms: 1.51x faster                                                       |
| comprehensions             | 15.6 us                                                     | 10.4 us: 1.50x faster                                                      |
| json_dumps                 | 8.09 ms                                                     | 5.57 ms: 1.45x faster                                                      |
| async_tree_io              | 808 ms                                                      | 578 ms: 1.40x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 1.94 ms: 1.39x faster                                                      |
| async_tree_io_tg           | 829 ms                                                      | 598 ms: 1.39x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 384 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.49 sec: 1.36x faster                                                     |
| logging_silent             | 71.8 ns                                                     | 53.6 ns: 1.34x faster                                                      |
| raytrace                   | 213 ms                                                      | 161 ms: 1.32x faster                                                       |
| richards_super             | 38.7 ms                                                     | 29.8 ms: 1.30x faster                                                      |
| genshi_xml                 | 39.9 ms                                                     | 31.5 ms: 1.27x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 754 us: 1.26x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 126 us: 1.25x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.7 ms: 1.25x faster                                                      |
| genshi_text                | 18.4 ms                                                     | 14.8 ms: 1.25x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.67 us: 1.21x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 963 us: 1.21x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 3.77 ms: 1.21x faster                                                      |
| go                         | 101 ms                                                      | 84.3 ms: 1.20x faster                                                      |
| nqueens                    | 68.3 ms                                                     | 57.1 ms: 1.20x faster                                                      |
| sympy_sum                  | 100 ms                                                      | 83.9 ms: 1.19x faster                                                      |
| pickle_pure_python         | 208 us                                                      | 176 us: 1.18x faster                                                       |
| richards                   | 31.4 ms                                                     | 26.6 ms: 1.18x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.35 sec: 1.18x faster                                                     |
| logging_format             | 7.16 us                                                     | 6.08 us: 1.18x faster                                                      |
| coroutines                 | 15.0 ms                                                     | 12.8 ms: 1.17x faster                                                      |
| regex_compile              | 91.0 ms                                                     | 77.9 ms: 1.17x faster                                                      |
| mako                       | 7.58 ms                                                     | 6.53 ms: 1.16x faster                                                      |
| sympy_str                  | 185 ms                                                      | 162 ms: 1.15x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.3 ms: 1.14x faster                                                      |
| deepcopy_memo              | 26.0 us                                                     | 23.0 us: 1.13x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 82.3 ms: 1.13x faster                                                      |
| deepcopy                   | 246 us                                                      | 219 us: 1.13x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 55.8 ms: 1.12x faster                                                      |
| django_template            | 24.4 ms                                                     | 21.8 ms: 1.12x faster                                                      |
| sympy_expand               | 299 ms                                                      | 270 ms: 1.11x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 173 ms: 1.10x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.1 ms: 1.10x faster                                                      |
| pprint_pformat             | 1.09 sec                                                    | 989 ms: 1.10x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.79 ms: 1.10x faster                                                      |
| pyflate                    | 312 ms                                                      | 286 ms: 1.09x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 35.6 ms: 1.09x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                      |
| pprint_safe_repr           | 529 ms                                                      | 485 ms: 1.09x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 804 us: 1.08x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 90.5 ms: 1.08x faster                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.36 sec: 1.07x faster                                                     |
| float                      | 54.4 ms                                                     | 51.2 ms: 1.06x faster                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 32.8 ms: 1.05x faster                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 46.5 ms: 1.05x faster                                                      |
| spectral_norm              | 68.3 ms                                                     | 65.1 ms: 1.05x faster                                                      |
| deepcopy_reduce            | 2.06 us                                                     | 1.97 us: 1.05x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.8 ms: 1.04x faster                                                      |
| 2to3                       | 214 ms                                                      | 207 ms: 1.03x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 73.4 ms: 1.02x faster                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 16.4 ms: 1.02x faster                                                      |
| docutils                   | 1.64 sec                                                    | 1.60 sec: 1.02x faster                                                     |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                      |
| pickle_dict                | 18.5 us                                                     | 18.2 us: 1.02x faster                                                      |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.54 ms: 1.01x faster                                                      |
| nbody                      | 70.3 ms                                                     | 69.4 ms: 1.01x faster                                                      |
| thrift                     | 494 us                                                      | 489 us: 1.01x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 77.3 ms: 1.01x faster                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 52.9 ms: 1.01x slower                                                      |
| scimark_fft                | 179 ms                                                      | 181 ms: 1.01x slower                                                       |
| python_startup             | 19.8 ms                                                     | 20.0 ms: 1.01x slower                                                      |
| fannkuch                   | 253 ms                                                      | 256 ms: 1.01x slower                                                       |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.02x slower                                                       |
| coverage                   | 43.4 ms                                                     | 44.5 ms: 1.02x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 14.8 ms: 1.04x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 66.0 ms: 1.04x slower                                                      |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                      |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.81 us: 1.09x slower                                                      |
| pickle                     | 6.64 us                                                     | 7.25 us: 1.09x slower                                                      |
| pathlib                    | 70.9 ms                                                     | 79.2 ms: 1.12x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.56 us: 1.13x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.68 ms: 1.15x slower                                                      |
| pickle_list                | 2.70 us                                                     | 3.23 us: 1.20x slower                                                      |
| create_gc_cycles           | 713 us                                                      | 888 us: 1.24x slower                                                       |
| async_generators           | 177 ms                                                      | 228 ms: 1.29x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.14x faster                                                               |

Benchmark hidden because not significant (4): pidigits, flaskblogging, pycparser, json
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown
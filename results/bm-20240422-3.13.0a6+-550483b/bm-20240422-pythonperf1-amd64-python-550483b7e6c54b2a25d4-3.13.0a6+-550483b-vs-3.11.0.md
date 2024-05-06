# Results vs. 3.11.0

- fork: python
- ref: 550483b7e6c54b2a25d4
- machine: windows-amd64
- commit hash: 550483b
- commit date: 2024-04-22
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 211 ms: 1.01x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.69 ms: 1.12x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.66 sec: 1.01x slower                                                      |
| html5lib       | 38.9 ms                                                     | 35.7 ms: 1.09x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 81.7 ms: 1.14x faster                                                       |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 269 ms: 1.50x faster                                                        |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 273 ms: 1.46x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 222 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| async_tree_io              | 808 ms                                                      | 597 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 394 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 624 ms: 1.33x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 51.9 ms: 1.05x faster                                                       |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| nbody          | 70.3 ms                                                     | 69.6 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 77.8 ms: 1.17x faster                                                       |
| regex_dna      | 116 ms                                                      | 115 ms: 1.01x faster                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.64 ms: 1.43x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 128 us: 1.23x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 179 us: 1.16x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 91.7 ms: 1.06x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.40 sec: 1.04x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 63.6 ms: 1.03x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 37.6 ms: 1.01x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 55.0 ms: 1.05x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.78 us: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.17 us: 1.08x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.24 us: 1.09x slower                                                       |
| pickle_list          | 2.70 us                                                     | 3.06 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.2 ms: 1.04x faster                                                       |
| Geometric mean         | (ref)                                                       | 1.02x faster                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.30 ms: 1.20x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 33.8 ms: 1.18x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 15.8 ms: 1.17x faster                                                       |
| django_template | 24.4 ms                                                     | 21.9 ms: 1.11x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.17x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 74.1 us: 4.40x faster                                                       |
| pylint                     | 323 ms                                                      | 207 ms: 1.56x faster                                                        |
| generators                 | 34.0 ms                                                     | 22.1 ms: 1.54x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 477 ms: 1.52x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 269 ms: 1.50x faster                                                        |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 273 ms: 1.46x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.8 us: 1.44x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.64 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 222 ms: 1.39x faster                                                        |
| deltablue                  | 2.70 ms                                                     | 1.98 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| async_tree_io              | 808 ms                                                      | 597 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 394 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 624 ms: 1.33x faster                                                        |
| raytrace                   | 213 ms                                                      | 161 ms: 1.33x faster                                                        |
| sqlglot_parse              | 953 us                                                      | 760 us: 1.25x faster                                                        |
| chaos                      | 48.4 ms                                                     | 38.7 ms: 1.25x faster                                                       |
| richards_super             | 38.7 ms                                                     | 31.5 ms: 1.23x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 128 us: 1.23x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 59.1 ns: 1.21x faster                                                       |
| mako                       | 7.58 ms                                                     | 6.30 ms: 1.20x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 21.7 us: 1.20x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 972 us: 1.20x faster                                                        |
| hexiom                     | 4.55 ms                                                     | 3.84 ms: 1.19x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 84.6 ms: 1.18x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 33.8 ms: 1.18x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 39.6 ms: 1.17x faster                                                       |
| go                         | 101 ms                                                      | 86.3 ms: 1.17x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.73 sec: 1.17x faster                                                      |
| regex_compile              | 91.0 ms                                                     | 77.8 ms: 1.17x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 58.5 ms: 1.17x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 15.8 ms: 1.17x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 179 us: 1.16x faster                                                        |
| logging_simple             | 6.86 us                                                     | 5.95 us: 1.15x faster                                                       |
| sympy_str                  | 185 ms                                                      | 161 ms: 1.15x faster                                                        |
| tornado_http               | 92.8 ms                                                     | 81.7 ms: 1.14x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                                       |
| richards                   | 31.4 ms                                                     | 27.7 ms: 1.13x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 40.0 ms: 1.13x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.5 ms: 1.13x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.69 ms: 1.12x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.41 us: 1.12x faster                                                       |
| django_template            | 24.4 ms                                                     | 21.9 ms: 1.11x faster                                                       |
| deepcopy                   | 246 us                                                      | 222 us: 1.11x faster                                                        |
| scimark_lu                 | 62.8 ms                                                     | 56.5 ms: 1.11x faster                                                       |
| mypy2                      | 459 ms                                                      | 418 ms: 1.10x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 994 ms: 1.09x faster                                                        |
| sympy_expand               | 299 ms                                                      | 273 ms: 1.09x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.46 sec: 1.09x faster                                                      |
| html5lib                   | 38.9 ms                                                     | 35.7 ms: 1.09x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 489 ms: 1.08x faster                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 45.4 ms: 1.08x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 810 us: 1.08x faster                                                        |
| pyflate                    | 312 ms                                                      | 291 ms: 1.07x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 63.8 ms: 1.07x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 179 ms: 1.07x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 91.7 ms: 1.06x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 74.2 ms: 1.05x faster                                                       |
| float                      | 54.4 ms                                                     | 51.9 ms: 1.05x faster                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 16.2 ms: 1.04x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.40 sec: 1.04x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 63.6 ms: 1.03x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 73.0 ms: 1.03x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 33.6 ms: 1.03x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.01 us: 1.03x faster                                                       |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| 2to3                       | 214 ms                                                      | 211 ms: 1.01x faster                                                        |
| aiohttp                    | 883 us                                                      | 874 us: 1.01x faster                                                        |
| nbody                      | 70.3 ms                                                     | 69.6 ms: 1.01x faster                                                       |
| regex_dna                  | 116 ms                                                      | 115 ms: 1.01x faster                                                        |
| bench_mp_pool              | 63.2 ms                                                     | 63.7 ms: 1.01x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.66 sec: 1.01x slower                                                      |
| xml_etree_process          | 37.2 ms                                                     | 37.6 ms: 1.01x slower                                                       |
| scimark_fft                | 179 ms                                                      | 182 ms: 1.01x slower                                                        |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 55.0 ms: 1.05x slower                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.70 ms: 1.05x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                                       |
| coverage                   | 43.4 ms                                                     | 46.0 ms: 1.06x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.78 us: 1.07x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 76.5 ms: 1.08x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.17 us: 1.08x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.24 us: 1.09x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.06 us: 1.13x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.89 ms: 1.20x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 898 us: 1.26x slower                                                        |
| async_generators           | 177 ms                                                      | 230 ms: 1.30x slower                                                        |
| thrift                     | 494 us                                                      | 8.01 ms: 16.22x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.09x faster                                                                |

Benchmark hidden because not significant (5): python_startup, pickle_dict, fannkuch, json, pycparser
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown
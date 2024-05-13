# Results vs. 3.11.0

- fork: python
- ref: 44995aab499b09a550de
- machine: windows-amd64
- commit hash: 44995aa
- commit date: 2024-05-13
- overall geometric mean: 1.07x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 234 ms: 1.10x slower                                                        |
| chameleon      | 5.26 ms                                                     | 5.07 ms: 1.04x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.79 sec: 1.09x slower                                                      |
| html5lib       | 38.9 ms                                                     | 37.0 ms: 1.05x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 85.9 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 272 ms: 1.49x faster                                                        |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 213 ms: 1.45x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.44x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.35x faster                                                        |
| async_tree_io              | 808 ms                                                      | 600 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 623 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 399 ms: 1.33x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 51.5 ms: 1.37x faster                                                       |
| float          | 54.4 ms                                                     | 43.4 ms: 1.25x faster                                                       |
| Geometric mean | (ref)                                                       | 1.20x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 88.6 ms: 1.03x faster                                                       |
| regex_dna      | 116 ms                                                      | 119 ms: 1.02x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 16.0 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.70 ms: 1.42x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 126 us: 1.24x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 174 us: 1.20x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.25 sec: 1.17x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.0 ms: 1.09x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 90.3 ms: 1.08x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 17.6 us: 1.05x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 51.6 ms: 1.02x faster                                                       |
| pickle               | 6.64 us                                                     | 7.17 us: 1.08x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.2 us: 1.09x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.82 us: 1.09x slower                                                       |
| pickle_list          | 2.70 us                                                     | 3.05 us: 1.13x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.60 us: 1.14x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 18.2 ms: 1.08x slower                                                       |
| python_startup         | 19.8 ms                                                     | 22.0 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.10x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 4.93 ms: 1.54x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 18.7 ms: 1.01x slower                                                       |
| django_template | 24.4 ms                                                     | 25.8 ms: 1.06x slower                                                       |
| genshi_xml      | 39.9 ms                                                     | 45.6 ms: 1.14x slower                                                       |
| Geometric mean  | (ref)                                                       | 1.06x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 112 us: 2.90x faster                                                        |
| generators                 | 34.0 ms                                                     | 21.6 ms: 1.57x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 44.1 ms: 1.55x faster                                                       |
| mako                       | 7.58 ms                                                     | 4.93 ms: 1.54x faster                                                       |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.53x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 272 ms: 1.49x faster                                                        |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 213 ms: 1.45x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.44x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.70 ms: 1.42x faster                                                       |
| nbody                      | 70.3 ms                                                     | 51.5 ms: 1.37x faster                                                       |
| pylint                     | 323 ms                                                      | 238 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 389 ms: 1.35x faster                                                        |
| async_tree_io              | 808 ms                                                      | 600 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 623 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 399 ms: 1.33x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.58 sec: 1.29x faster                                                      |
| logging_silent             | 71.8 ns                                                     | 55.9 ns: 1.28x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 572 ms: 1.27x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 20.6 us: 1.26x faster                                                       |
| float                      | 54.4 ms                                                     | 43.4 ms: 1.25x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 126 us: 1.24x faster                                                        |
| chaos                      | 48.4 ms                                                     | 39.2 ms: 1.23x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.10 ms: 1.23x faster                                                       |
| pyflate                    | 312 ms                                                      | 257 ms: 1.22x faster                                                        |
| raytrace                   | 213 ms                                                      | 175 ms: 1.22x faster                                                        |
| scimark_fft                | 179 ms                                                      | 150 ms: 1.20x faster                                                        |
| pickle_pure_python         | 208 us                                                      | 174 us: 1.20x faster                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 41.0 ms: 1.19x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 800 us: 1.19x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 446 ms: 1.19x faster                                                        |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.2 ms: 1.19x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 924 ms: 1.18x faster                                                        |
| richards_super             | 38.7 ms                                                     | 33.0 ms: 1.17x faster                                                       |
| fannkuch                   | 253 ms                                                      | 216 ms: 1.17x faster                                                        |
| logging_simple             | 6.86 us                                                     | 5.87 us: 1.17x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.25 sec: 1.17x faster                                                      |
| deltablue                  | 2.70 ms                                                     | 2.37 ms: 1.14x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.29 us: 1.14x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1.03 ms: 1.13x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.59 us: 1.11x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 61.4 ms: 1.11x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 42.1 ms: 1.10x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.0 ms: 1.09x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.46 sec: 1.09x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 90.3 ms: 1.08x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 85.9 ms: 1.08x faster                                                       |
| go                         | 101 ms                                                      | 93.6 ms: 1.08x faster                                                       |
| richards                   | 31.4 ms                                                     | 29.1 ms: 1.08x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 93.1 ms: 1.07x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 17.6 us: 1.05x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 37.0 ms: 1.05x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 5.07 ms: 1.04x faster                                                       |
| deepcopy                   | 246 us                                                      | 238 us: 1.04x faster                                                        |
| sympy_str                  | 185 ms                                                      | 179 ms: 1.03x faster                                                        |
| meteor_contest             | 75.2 ms                                                     | 72.8 ms: 1.03x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 88.6 ms: 1.03x faster                                                       |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 51.6 ms: 1.02x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| genshi_text                | 18.4 ms                                                     | 18.7 ms: 1.01x slower                                                       |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.02x slower                                                        |
| coverage                   | 43.4 ms                                                     | 44.5 ms: 1.02x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 4.67 ms: 1.03x slower                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.14 us: 1.04x slower                                                       |
| sympy_expand               | 299 ms                                                      | 311 ms: 1.04x slower                                                        |
| pycparser                  | 720 ms                                                      | 756 ms: 1.05x slower                                                        |
| gc_traversal               | 1.49 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 82.2 ms: 1.05x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                       |
| django_template            | 24.4 ms                                                     | 25.8 ms: 1.06x slower                                                       |
| mypy2                      | 459 ms                                                      | 488 ms: 1.06x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 36.7 ms: 1.06x slower                                                       |
| aiohttp                    | 883 us                                                      | 940 us: 1.06x slower                                                        |
| pickle                     | 6.64 us                                                     | 7.17 us: 1.08x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 18.2 ms: 1.08x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.79 sec: 1.09x slower                                                      |
| json_loads                 | 13.0 us                                                     | 14.2 us: 1.09x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.82 us: 1.09x slower                                                       |
| 2to3                       | 214 ms                                                      | 234 ms: 1.10x slower                                                        |
| python_startup             | 19.8 ms                                                     | 22.0 ms: 1.11x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.55 ms: 1.12x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 80.2 ms: 1.13x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.05 us: 1.13x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 16.0 ms: 1.13x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.60 us: 1.14x slower                                                       |
| genshi_xml                 | 39.9 ms                                                     | 45.6 ms: 1.14x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 72.2 ms: 1.15x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 73.9 ms: 1.17x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 920 us: 1.29x slower                                                        |
| async_generators           | 177 ms                                                      | 248 ms: 1.40x slower                                                        |
| thrift                     | 494 us                                                      | 9.28 ms: 18.79x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                                |

Benchmark hidden because not significant (4): sympy_integrate, pidigits, json, bench_thread_pool
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown
# Results vs. 3.11.0

- fork: python
- ref: 44995aab499b09a550de
- machine: windows-amd64
- commit hash: 44995aa
- commit date: 2024-05-13
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 208 ms: 1.03x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.71 ms: 1.12x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| html5lib       | 38.9 ms                                                     | 35.2 ms: 1.10x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 81.6 ms: 1.14x faster                                                       |
| Geometric mean | (ref)                                                       | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 262 ms: 1.54x faster                                                        |
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 204 ms: 1.51x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 265 ms: 1.51x faster                                                        |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 609 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 390 ms: 1.36x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.44x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 48.2 ms: 1.13x faster                                                       |
| nbody          | 70.3 ms                                                     | 66.2 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 76.9 ms: 1.18x faster                                                       |
| regex_dna      | 116 ms                                                      | 118 ms: 1.02x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.57 ms: 1.45x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 120 us: 1.31x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 173 us: 1.21x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.35 sec: 1.08x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 91.3 ms: 1.07x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.8 ms: 1.06x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 35.9 ms: 1.04x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 52.9 ms: 1.01x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.62 us: 1.01x slower                                                       |
| pickle_dict          | 18.5 us                                                     | 19.4 us: 1.05x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.0 us: 1.08x slower                                                       |
| pickle               | 6.64 us                                                     | 7.18 us: 1.08x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.94 us: 1.09x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.45 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.2 ms: 1.02x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.00x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 14.5 ms: 1.28x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 31.7 ms: 1.26x faster                                                       |
| mako            | 7.58 ms                                                     | 6.28 ms: 1.21x faster                                                       |
| django_template | 24.4 ms                                                     | 21.1 ms: 1.16x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.23x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1-amd64-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 100 us: 3.26x faster                                                        |
| generators                 | 34.0 ms                                                     | 19.3 ms: 1.76x faster                                                       |
| pylint                     | 323 ms                                                      | 206 ms: 1.57x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.1 us: 1.55x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 262 ms: 1.54x faster                                                        |
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 204 ms: 1.51x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 265 ms: 1.51x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.57 ms: 1.45x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 1.90 ms: 1.42x faster                                                       |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 609 ms: 1.36x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 52.8 ns: 1.36x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 390 ms: 1.36x faster                                                        |
| raytrace                   | 213 ms                                                      | 161 ms: 1.33x faster                                                        |
| richards_super             | 38.7 ms                                                     | 29.3 ms: 1.32x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.55 sec: 1.31x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 120 us: 1.31x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 566 ms: 1.28x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 14.5 ms: 1.28x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 749 us: 1.27x faster                                                        |
| chaos                      | 48.4 ms                                                     | 38.2 ms: 1.27x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 31.7 ms: 1.26x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 3.64 ms: 1.25x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 55.5 ms: 1.23x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 954 us: 1.22x faster                                                        |
| richards                   | 31.4 ms                                                     | 25.8 ms: 1.22x faster                                                       |
| go                         | 101 ms                                                      | 83.5 ms: 1.21x faster                                                       |
| mako                       | 7.58 ms                                                     | 6.28 ms: 1.21x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 173 us: 1.21x faster                                                        |
| logging_simple             | 6.86 us                                                     | 5.73 us: 1.20x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.33 sec: 1.19x faster                                                      |
| sympy_sum                  | 100 ms                                                      | 83.8 ms: 1.19x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 21.7 us: 1.19x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 39.1 ms: 1.19x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 76.9 ms: 1.18x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.7 ms: 1.18x faster                                                       |
| sympy_str                  | 185 ms                                                      | 158 ms: 1.17x faster                                                        |
| logging_format             | 7.16 us                                                     | 6.12 us: 1.17x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 53.7 ms: 1.17x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.1 ms: 1.16x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.1 ms: 1.16x faster                                                       |
| django_template            | 24.4 ms                                                     | 21.1 ms: 1.16x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 81.6 ms: 1.14x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 60.1 ms: 1.14x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 959 ms: 1.13x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 467 ms: 1.13x faster                                                        |
| pyflate                    | 312 ms                                                      | 276 ms: 1.13x faster                                                        |
| deepcopy                   | 246 us                                                      | 218 us: 1.13x faster                                                        |
| float                      | 54.4 ms                                                     | 48.2 ms: 1.13x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 170 ms: 1.12x faster                                                        |
| chameleon                  | 5.26 ms                                                     | 4.71 ms: 1.12x faster                                                       |
| sympy_expand               | 299 ms                                                      | 267 ms: 1.12x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 35.2 ms: 1.10x faster                                                       |
| mypy2                      | 459 ms                                                      | 417 ms: 1.10x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.61 us: 1.10x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 44.9 ms: 1.09x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 808 us: 1.08x faster                                                        |
| tomli_loads                | 1.46 sec                                                    | 1.35 sec: 1.08x faster                                                      |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.39 ms: 1.08x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 73.1 ms: 1.07x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 91.3 ms: 1.07x faster                                                       |
| nbody                      | 70.3 ms                                                     | 66.2 ms: 1.06x faster                                                       |
| fannkuch                   | 253 ms                                                      | 238 ms: 1.06x faster                                                        |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.8 ms: 1.06x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 71.0 ms: 1.06x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 32.6 ms: 1.06x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.97 us: 1.04x faster                                                       |
| scimark_fft                | 179 ms                                                      | 172 ms: 1.04x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 35.9 ms: 1.04x faster                                                       |
| 2to3                       | 214 ms                                                      | 208 ms: 1.03x faster                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                       |
| docutils                   | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 52.9 ms: 1.01x slower                                                       |
| aiohttp                    | 883 us                                                      | 894 us: 1.01x slower                                                        |
| unpickle_list              | 2.59 us                                                     | 2.62 us: 1.01x slower                                                       |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.02x slower                                                        |
| python_startup             | 19.8 ms                                                     | 20.2 ms: 1.02x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 66.2 ms: 1.05x slower                                                       |
| pickle_dict                | 18.5 us                                                     | 19.4 us: 1.05x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.0 us: 1.08x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.18 us: 1.08x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.94 us: 1.09x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.09x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.45 us: 1.12x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 79.3 ms: 1.12x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.59 ms: 1.13x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 903 us: 1.27x slower                                                        |
| async_generators           | 177 ms                                                      | 226 ms: 1.28x slower                                                        |
| thrift                     | 494 us                                                      | 8.07 ms: 16.35x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (4): pycparser, pidigits, coverage, json
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: unknown
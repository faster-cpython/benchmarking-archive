# Results vs. 3.11.0

- fork: python
- ref: a19bb261a327e1008f21
- machine: windows-amd64
- commit hash: a19bb26
- commit date: 2024-06-15
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 207 ms: 1.03x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.71 ms: 1.12x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.63 sec: 1.01x faster                                                      |
| html5lib       | 38.9 ms                                                     | 35.5 ms: 1.10x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 82.1 ms: 1.13x faster                                                       |
| Geometric mean | (ref)                                                       | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 260 ms: 1.56x faster                                                        |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 263 ms: 1.52x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 205 ms: 1.51x faster                                                        |
| async_tree_io              | 808 ms                                                      | 584 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 385 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 615 ms: 1.35x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.45x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 50.9 ms: 1.07x faster                                                       |
| nbody          | 70.3 ms                                                     | 69.4 ms: 1.01x faster                                                       |
| pidigits       | 150 ms                                                      | 149 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 77.0 ms: 1.18x faster                                                       |
| regex_dna      | 116 ms                                                      | 118 ms: 1.02x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 16.2 ms: 1.15x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.51 ms: 1.47x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 124 us: 1.26x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 176 us: 1.18x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 91.3 ms: 1.07x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.38 sec: 1.06x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.9 ms: 1.04x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.5 ms: 1.02x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.66 us: 1.03x slower                                                       |
| pickle_dict          | 18.5 us                                                     | 19.2 us: 1.04x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.0 us: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.27 us: 1.10x slower                                                       |
| pickle_list          | 2.70 us                                                     | 3.02 us: 1.12x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.79 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.1 ms: 1.04x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.2 ms: 1.02x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 31.1 ms: 1.28x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 14.8 ms: 1.25x faster                                                       |
| mako            | 7.58 ms                                                     | 6.39 ms: 1.19x faster                                                       |
| django_template | 24.4 ms                                                     | 21.9 ms: 1.12x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.21x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240615-pythonperf1-amd64-python-a19bb261a327e1008f21-3.13.0b2+-a19bb26 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 104 us: 3.13x faster                                                        |
| generators                 | 34.0 ms                                                     | 20.1 ms: 1.69x faster                                                       |
| pylint                     | 323 ms                                                      | 205 ms: 1.58x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 260 ms: 1.56x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.53x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 474 ms: 1.53x faster                                                        |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 263 ms: 1.52x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 205 ms: 1.51x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.51 ms: 1.47x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 1.89 ms: 1.43x faster                                                       |
| async_tree_io              | 808 ms                                                      | 584 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 385 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 53.0 ns: 1.35x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 615 ms: 1.35x faster                                                        |
| raytrace                   | 213 ms                                                      | 159 ms: 1.34x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.54 sec: 1.32x faster                                                      |
| richards_super             | 38.7 ms                                                     | 30.1 ms: 1.29x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 31.1 ms: 1.28x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.2 ms: 1.27x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 124 us: 1.26x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 14.8 ms: 1.25x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 765 us: 1.25x faster                                                        |
| hexiom                     | 4.55 ms                                                     | 3.70 ms: 1.23x faster                                                       |
| go                         | 101 ms                                                      | 82.5 ms: 1.23x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 57.0 ms: 1.20x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 975 us: 1.19x faster                                                        |
| dulwich_log                | 46.4 ms                                                     | 38.9 ms: 1.19x faster                                                       |
| mako                       | 7.58 ms                                                     | 6.39 ms: 1.19x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.79 us: 1.19x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 176 us: 1.18x faster                                                        |
| regex_compile              | 91.0 ms                                                     | 77.0 ms: 1.18x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 84.9 ms: 1.18x faster                                                       |
| richards                   | 31.4 ms                                                     | 26.6 ms: 1.18x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 54.0 ms: 1.16x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.20 us: 1.15x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 22.6 us: 1.15x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.39 sec: 1.14x faster                                                      |
| sympy_str                  | 185 ms                                                      | 162 ms: 1.14x faster                                                        |
| bench_thread_pool          | 872 us                                                      | 763 us: 1.14x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 12.4 ms: 1.13x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 82.1 ms: 1.13x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.3 ms: 1.12x faster                                                       |
| django_template            | 24.4 ms                                                     | 21.9 ms: 1.12x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.71 ms: 1.12x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 476 ms: 1.11x faster                                                        |
| pyflate                    | 312 ms                                                      | 281 ms: 1.11x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 980 ms: 1.11x faster                                                        |
| deepcopy                   | 246 us                                                      | 223 us: 1.10x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 62.0 ms: 1.10x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 35.5 ms: 1.10x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 44.8 ms: 1.09x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.6 ms: 1.09x faster                                                       |
| sympy_expand               | 299 ms                                                      | 275 ms: 1.09x faster                                                        |
| mypy2                      | 459 ms                                                      | 423 ms: 1.08x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 176 ms: 1.08x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 91.3 ms: 1.07x faster                                                       |
| float                      | 54.4 ms                                                     | 50.9 ms: 1.07x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.38 sec: 1.06x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 71.6 ms: 1.05x faster                                                       |
| fannkuch                   | 253 ms                                                      | 241 ms: 1.05x faster                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.46 ms: 1.05x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.9 ms: 1.04x faster                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 16.1 ms: 1.04x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 33.3 ms: 1.04x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 75.5 ms: 1.03x faster                                                       |
| 2to3                       | 214 ms                                                      | 207 ms: 1.03x faster                                                        |
| scimark_fft                | 179 ms                                                      | 175 ms: 1.02x faster                                                        |
| nbody                      | 70.3 ms                                                     | 69.4 ms: 1.01x faster                                                       |
| xml_etree_process          | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                                       |
| docutils                   | 1.64 sec                                                    | 1.63 sec: 1.01x faster                                                      |
| deepcopy_reduce            | 2.06 us                                                     | 2.05 us: 1.01x faster                                                       |
| pidigits                   | 150 ms                                                      | 149 ms: 1.01x faster                                                        |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.02x slower                                                        |
| aiohttp                    | 883 us                                                      | 899 us: 1.02x slower                                                        |
| xml_etree_generate         | 52.5 ms                                                     | 53.5 ms: 1.02x slower                                                       |
| python_startup             | 19.8 ms                                                     | 20.2 ms: 1.02x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 64.5 ms: 1.02x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.66 us: 1.03x slower                                                       |
| pickle_dict                | 18.5 us                                                     | 19.2 us: 1.04x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                       |
| coverage                   | 43.4 ms                                                     | 45.4 ms: 1.05x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 75.1 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.0 us: 1.07x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.27 us: 1.10x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.02 us: 1.12x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 16.2 ms: 1.15x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.79 us: 1.16x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.76 ms: 1.17x slower                                                       |
| async_generators           | 177 ms                                                      | 223 ms: 1.26x slower                                                        |
| create_gc_cycles           | 713 us                                                      | 913 us: 1.28x slower                                                        |
| thrift                     | 494 us                                                      | 7.96 ms: 16.11x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (2): pycparser, json
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown
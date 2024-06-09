# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: windows-amd64
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.08x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 231 ms: 1.08x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.96 ms: 1.06x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                                      |
| html5lib       | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 86.3 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 276 ms: 1.45x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 214 ms: 1.44x faster                                                        |
| async_tree_io              | 808 ms                                                      | 595 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 391 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 620 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 400 ms: 1.32x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 50.4 ms: 1.40x faster                                                       |
| float          | 54.4 ms                                                     | 44.3 ms: 1.23x faster                                                       |
| pidigits       | 150 ms                                                      | 149 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                       | 1.20x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 88.0 ms: 1.03x faster                                                       |
| regex_dna      | 116 ms                                                      | 120 ms: 1.03x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 16.9 ms: 1.19x slower                                                       |
| Geometric mean | (ref)                                                       | 1.06x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.77 ms: 1.40x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 126 us: 1.25x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 171 us: 1.22x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.23 sec: 1.18x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 90.7 ms: 1.08x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.4 ms: 1.07x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 17.6 us: 1.05x faster                                                       |
| pickle_list          | 2.70 us                                                     | 2.80 us: 1.04x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.70 us: 1.04x slower                                                       |
| pickle               | 6.64 us                                                     | 7.18 us: 1.08x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.3 us: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.50 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.06x faster                                                                |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                                       |
| python_startup         | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.07 ms: 1.50x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 18.3 ms: 1.01x faster                                                       |
| django_template | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                       |
| genshi_xml      | 39.9 ms                                                     | 44.6 ms: 1.12x slower                                                       |
| Geometric mean  | (ref)                                                       | 1.07x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 111 us: 2.93x faster                                                        |
| generators                 | 34.0 ms                                                     | 21.5 ms: 1.58x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 44.4 ms: 1.54x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 474 ms: 1.53x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.53x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.07 ms: 1.50x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 276 ms: 1.45x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 214 ms: 1.44x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.77 ms: 1.40x faster                                                       |
| nbody                      | 70.3 ms                                                     | 50.4 ms: 1.40x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.46 sec: 1.39x faster                                                      |
| pylint                     | 323 ms                                                      | 235 ms: 1.38x faster                                                        |
| async_tree_io              | 808 ms                                                      | 595 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 391 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 620 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 400 ms: 1.32x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 20.1 us: 1.29x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 56.5 ns: 1.27x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 126 us: 1.25x faster                                                        |
| chaos                      | 48.4 ms                                                     | 39.3 ms: 1.23x faster                                                       |
| float                      | 54.4 ms                                                     | 44.3 ms: 1.23x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 171 us: 1.22x faster                                                        |
| scimark_fft                | 179 ms                                                      | 148 ms: 1.21x faster                                                        |
| pyflate                    | 312 ms                                                      | 257 ms: 1.21x faster                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.14 ms: 1.20x faster                                                       |
| fannkuch                   | 253 ms                                                      | 211 ms: 1.20x faster                                                        |
| richards_super             | 38.7 ms                                                     | 32.3 ms: 1.20x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 800 us: 1.19x faster                                                        |
| logging_simple             | 6.86 us                                                     | 5.78 us: 1.19x faster                                                       |
| raytrace                   | 213 ms                                                      | 180 ms: 1.19x faster                                                        |
| tomli_loads                | 1.46 sec                                                    | 1.23 sec: 1.18x faster                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 41.4 ms: 1.18x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 59.1 ms: 1.16x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.4 ms: 1.15x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 947 ms: 1.15x faster                                                        |
| logging_format             | 7.16 us                                                     | 6.24 us: 1.15x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 462 ms: 1.14x faster                                                        |
| dulwich_log                | 46.4 ms                                                     | 40.5 ms: 1.14x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.37 ms: 1.14x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.41 sec: 1.13x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 1.03 ms: 1.13x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.58 us: 1.12x faster                                                       |
| richards                   | 31.4 ms                                                     | 28.6 ms: 1.10x faster                                                       |
| go                         | 101 ms                                                      | 93.6 ms: 1.08x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 90.7 ms: 1.08x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 86.3 ms: 1.07x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.4 ms: 1.07x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 93.9 ms: 1.07x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.96 ms: 1.06x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 824 us: 1.06x faster                                                        |
| pickle_dict                | 18.5 us                                                     | 17.6 us: 1.05x faster                                                       |
| deepcopy                   | 246 us                                                      | 237 us: 1.04x faster                                                        |
| regex_compile              | 91.0 ms                                                     | 88.0 ms: 1.03x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 72.8 ms: 1.03x faster                                                       |
| sympy_str                  | 185 ms                                                      | 179 ms: 1.03x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 18.3 ms: 1.01x faster                                                       |
| pidigits                   | 150 ms                                                      | 149 ms: 1.00x faster                                                        |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| sympy_integrate            | 14.0 ms                                                     | 14.1 ms: 1.01x slower                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.09 us: 1.01x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 4.66 ms: 1.02x slower                                                       |
| regex_dna                  | 116 ms                                                      | 120 ms: 1.03x slower                                                        |
| pickle_list                | 2.70 us                                                     | 2.80 us: 1.04x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 81.1 ms: 1.04x slower                                                       |
| sympy_expand               | 299 ms                                                      | 312 ms: 1.04x slower                                                        |
| unpickle_list              | 2.59 us                                                     | 2.70 us: 1.04x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                       |
| django_template            | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                       |
| aiohttp                    | 883 us                                                      | 929 us: 1.05x slower                                                        |
| mypy2                      | 459 ms                                                      | 484 ms: 1.05x slower                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| pycparser                  | 720 ms                                                      | 762 ms: 1.06x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 36.7 ms: 1.06x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 75.7 ms: 1.07x slower                                                       |
| coverage                   | 43.4 ms                                                     | 46.8 ms: 1.08x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                                      |
| 2to3                       | 214 ms                                                      | 231 ms: 1.08x slower                                                        |
| pickle                     | 6.64 us                                                     | 7.18 us: 1.08x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.3 us: 1.10x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 69.4 ms: 1.10x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 69.0 ms: 1.10x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.49 ms: 1.10x slower                                                       |
| python_startup             | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                       |
| genshi_xml                 | 39.9 ms                                                     | 44.6 ms: 1.12x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.50 us: 1.12x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 16.9 ms: 1.19x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 924 us: 1.29x slower                                                        |
| async_generators           | 177 ms                                                      | 249 ms: 1.41x slower                                                        |
| thrift                     | 494 us                                                      | 9.10 ms: 18.43x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                                |

Benchmark hidden because not significant (3): xml_etree_process, xml_etree_generate, json
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown
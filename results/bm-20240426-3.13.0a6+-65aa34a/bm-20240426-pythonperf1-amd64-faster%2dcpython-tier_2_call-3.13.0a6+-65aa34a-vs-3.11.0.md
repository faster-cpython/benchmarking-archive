# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-amd64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 217 ms: 1.02x slower                                                         |
| chameleon      | 5.26 ms                                                     | 5.05 ms: 1.04x faster                                                        |
| html5lib       | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                                        |
| tornado_http   | 92.8 ms                                                     | 90.9 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 280 ms: 1.45x faster                                                         |
| async_tree_none            | 332 ms                                                      | 233 ms: 1.43x faster                                                         |
| async_tree_memoization     | 399 ms                                                      | 282 ms: 1.41x faster                                                         |
| async_tree_none_tg         | 309 ms                                                      | 224 ms: 1.38x faster                                                         |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 386 ms: 1.35x faster                                                         |
| async_tree_io              | 808 ms                                                      | 612 ms: 1.32x faster                                                         |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 402 ms: 1.32x faster                                                         |
| async_tree_io_tg           | 829 ms                                                      | 635 ms: 1.31x faster                                                         |
| Geometric mean             | (ref)                                                       | 1.37x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 51.5 ms: 1.06x faster                                                        |
| pidigits       | 150 ms                                                      | 149 ms: 1.01x faster                                                         |
| nbody          | 70.3 ms                                                     | 72.9 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 79.4 ms: 1.15x faster                                                        |
| regex_dna      | 116 ms                                                      | 114 ms: 1.02x faster                                                         |
| regex_v8       | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.83 ms: 1.39x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 176 us: 1.18x faster                                                         |
| unpickle_pure_python | 157 us                                                      | 133 us: 1.18x faster                                                         |
| xml_etree_parse      | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                                        |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.7 ms: 1.01x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.45 sec: 1.01x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.4 us: 1.00x faster                                                        |
| xml_etree_process    | 37.2 ms                                                     | 37.6 ms: 1.01x slower                                                        |
| xml_etree_generate   | 52.5 ms                                                     | 55.2 ms: 1.05x slower                                                        |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                                        |
| unpickle_list        | 2.59 us                                                     | 2.78 us: 1.08x slower                                                        |
| pickle               | 6.64 us                                                     | 7.27 us: 1.09x slower                                                        |
| unpickle             | 7.57 us                                                     | 8.57 us: 1.13x slower                                                        |
| pickle_list          | 2.70 us                                                     | 3.11 us: 1.15x slower                                                        |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup | 19.8 ms                                                     | 20.6 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.37 ms: 1.19x faster                                                        |
| genshi_xml      | 39.9 ms                                                     | 34.4 ms: 1.16x faster                                                        |
| genshi_text     | 18.4 ms                                                     | 16.2 ms: 1.14x faster                                                        |
| django_template | 24.4 ms                                                     | 22.4 ms: 1.09x faster                                                        |
| Geometric mean  | (ref)                                                       | 1.15x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 109 us: 3.00x faster                                                         |
| pylint                     | 323 ms                                                      | 212 ms: 1.52x faster                                                         |
| generators                 | 34.0 ms                                                     | 22.3 ms: 1.52x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.7 us: 1.46x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 280 ms: 1.45x faster                                                         |
| async_tree_none            | 332 ms                                                      | 233 ms: 1.43x faster                                                         |
| async_tree_memoization     | 399 ms                                                      | 282 ms: 1.41x faster                                                         |
| json_dumps                 | 8.09 ms                                                     | 5.83 ms: 1.39x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 224 ms: 1.38x faster                                                         |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 386 ms: 1.35x faster                                                         |
| async_tree_io              | 808 ms                                                      | 612 ms: 1.32x faster                                                         |
| deltablue                  | 2.70 ms                                                     | 2.05 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 402 ms: 1.32x faster                                                         |
| logging_silent             | 71.8 ns                                                     | 54.9 ns: 1.31x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 635 ms: 1.31x faster                                                         |
| raytrace                   | 213 ms                                                      | 166 ms: 1.28x faster                                                         |
| chaos                      | 48.4 ms                                                     | 39.1 ms: 1.24x faster                                                        |
| sqlglot_parse              | 953 us                                                      | 781 us: 1.22x faster                                                         |
| richards_super             | 38.7 ms                                                     | 32.4 ms: 1.19x faster                                                        |
| mako                       | 7.58 ms                                                     | 6.37 ms: 1.19x faster                                                        |
| pickle_pure_python         | 208 us                                                      | 176 us: 1.18x faster                                                         |
| unpickle_pure_python       | 157 us                                                      | 133 us: 1.18x faster                                                         |
| sqlglot_transpile          | 1.16 ms                                                     | 994 us: 1.17x faster                                                         |
| hexiom                     | 4.55 ms                                                     | 3.88 ms: 1.17x faster                                                        |
| sympy_sum                  | 100 ms                                                      | 85.7 ms: 1.17x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 34.4 ms: 1.16x faster                                                        |
| dulwich_log                | 46.4 ms                                                     | 39.9 ms: 1.16x faster                                                        |
| regex_compile              | 91.0 ms                                                     | 79.4 ms: 1.15x faster                                                        |
| sympy_str                  | 185 ms                                                      | 162 ms: 1.14x faster                                                         |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.14x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 16.2 ms: 1.14x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 22.9 us: 1.14x faster                                                        |
| logging_simple             | 6.86 us                                                     | 6.05 us: 1.13x faster                                                        |
| nqueens                    | 68.3 ms                                                     | 60.6 ms: 1.13x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 12.5 ms: 1.12x faster                                                        |
| mdp                        | 1.59 sec                                                    | 1.43 sec: 1.12x faster                                                       |
| deepcopy                   | 246 us                                                      | 221 us: 1.12x faster                                                         |
| go                         | 101 ms                                                      | 90.7 ms: 1.11x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.84 sec: 1.10x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.53 us: 1.10x faster                                                        |
| richards                   | 31.4 ms                                                     | 28.7 ms: 1.09x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 664 ms: 1.09x faster                                                         |
| django_template            | 24.4 ms                                                     | 22.4 ms: 1.09x faster                                                        |
| sympy_expand               | 299 ms                                                      | 274 ms: 1.09x faster                                                         |
| pprint_pformat             | 1.09 sec                                                    | 999 ms: 1.09x faster                                                         |
| pyflate                    | 312 ms                                                      | 288 ms: 1.08x faster                                                         |
| scimark_lu                 | 62.8 ms                                                     | 58.1 ms: 1.08x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 492 ms: 1.08x faster                                                         |
| crypto_pyaes               | 48.9 ms                                                     | 45.4 ms: 1.08x faster                                                        |
| mypy2                      | 459 ms                                                      | 428 ms: 1.07x faster                                                         |
| html5lib                   | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.67 us: 1.06x faster                                                        |
| scimark_monte_carlo        | 45.3 ms                                                     | 42.8 ms: 1.06x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 92.3 ms: 1.06x faster                                                        |
| float                      | 54.4 ms                                                     | 51.5 ms: 1.06x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 181 ms: 1.05x faster                                                         |
| spectral_norm              | 68.3 ms                                                     | 65.5 ms: 1.04x faster                                                        |
| chameleon                  | 5.26 ms                                                     | 5.05 ms: 1.04x faster                                                        |
| tornado_http               | 92.8 ms                                                     | 90.9 ms: 1.02x faster                                                        |
| regex_dna                  | 116 ms                                                      | 114 ms: 1.02x faster                                                         |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.7 ms: 1.01x faster                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 34.2 ms: 1.01x faster                                                        |
| pidigits                   | 150 ms                                                      | 149 ms: 1.01x faster                                                         |
| tomli_loads                | 1.46 sec                                                    | 1.45 sec: 1.01x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 74.8 ms: 1.01x faster                                                        |
| scimark_sor                | 78.1 ms                                                     | 77.7 ms: 1.01x faster                                                        |
| pickle_dict                | 18.5 us                                                     | 18.4 us: 1.00x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 37.6 ms: 1.01x slower                                                        |
| 2to3                       | 214 ms                                                      | 217 ms: 1.02x slower                                                         |
| fannkuch                   | 253 ms                                                      | 259 ms: 1.02x slower                                                         |
| regex_v8                   | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                        |
| nbody                      | 70.3 ms                                                     | 72.9 ms: 1.04x slower                                                        |
| bench_mp_pool              | 63.2 ms                                                     | 65.6 ms: 1.04x slower                                                        |
| python_startup             | 19.8 ms                                                     | 20.6 ms: 1.04x slower                                                        |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                        |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                        |
| xml_etree_generate         | 52.5 ms                                                     | 55.2 ms: 1.05x slower                                                        |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                                        |
| aiohttp                    | 883 us                                                      | 933 us: 1.06x slower                                                         |
| unpickle_list              | 2.59 us                                                     | 2.78 us: 1.08x slower                                                        |
| pickle                     | 6.64 us                                                     | 7.27 us: 1.09x slower                                                        |
| scimark_fft                | 179 ms                                                      | 197 ms: 1.10x slower                                                         |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.88 ms: 1.12x slower                                                        |
| unpickle                   | 7.57 us                                                     | 8.57 us: 1.13x slower                                                        |
| pickle_list                | 2.70 us                                                     | 3.11 us: 1.15x slower                                                        |
| pathlib                    | 70.9 ms                                                     | 82.3 ms: 1.16x slower                                                        |
| coverage                   | 43.4 ms                                                     | 50.6 ms: 1.17x slower                                                        |
| telco                      | 4.06 ms                                                     | 4.83 ms: 1.19x slower                                                        |
| create_gc_cycles           | 713 us                                                      | 901 us: 1.26x slower                                                         |
| async_generators           | 177 ms                                                      | 242 ms: 1.37x slower                                                         |
| thrift                     | 494 us                                                      | 8.42 ms: 17.05x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.06x faster                                                                 |

Benchmark hidden because not significant (6): bench_thread_pool, python_startup_no_site, deepcopy_reduce, docutils, json, pycparser
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown
# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 221 ms: 1.03x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.70 sec: 1.04x slower                                                      |
| html5lib       | 38.9 ms                                                     | 35.3 ms: 1.10x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 83.9 ms: 1.11x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 265 ms: 1.53x faster                                                        |
| async_tree_none            | 332 ms                                                      | 221 ms: 1.50x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 214 ms: 1.44x faster                                                        |
| async_tree_io              | 808 ms                                                      | 584 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 392 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 618 ms: 1.34x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.42x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 58.1 ms: 1.21x faster                                                       |
| float          | 54.4 ms                                                     | 47.1 ms: 1.15x faster                                                       |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 86.4 ms: 1.05x faster                                                       |
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| regex_v8       | 14.2 ms                                                     | 14.9 ms: 1.05x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.61 ms: 1.07x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.60 ms: 1.45x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 127 us: 1.23x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.20 sec: 1.21x faster                                                      |
| pickle_pure_python   | 208 us                                                      | 174 us: 1.20x faster                                                        |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.9 ms: 1.08x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 90.9 ms: 1.07x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                       |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.94 us: 1.09x slower                                                       |
| pickle               | 6.64 us                                                     | 7.26 us: 1.09x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.89 us: 1.12x slower                                                       |
| unpickle             | 7.57 us                                                     | 9.30 us: 1.23x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (2): pickle_dict, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                       |
| python_startup_no_site | 16.8 ms                                                     | 19.7 ms: 1.17x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.14x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 5.64 ms: 1.35x faster                                                       |
| genshi_text    | 18.4 ms                                                     | 15.4 ms: 1.20x faster                                                       |
| genshi_xml     | 39.9 ms                                                     | 34.3 ms: 1.16x faster                                                       |
| Geometric mean | (ref)                                                       | 1.23x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 70.8 us: 4.61x faster                                                       |
| generators                 | 34.0 ms                                                     | 19.5 ms: 1.74x faster                                                       |
| pylint                     | 323 ms                                                      | 194 ms: 1.67x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 473 ms: 1.53x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 265 ms: 1.53x faster                                                        |
| async_tree_none            | 332 ms                                                      | 221 ms: 1.50x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.60 ms: 1.45x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 214 ms: 1.44x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.8 us: 1.44x faster                                                       |
| async_tree_io              | 808 ms                                                      | 584 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 53.0 ns: 1.35x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 392 ms: 1.35x faster                                                        |
| mako                       | 7.58 ms                                                     | 5.64 ms: 1.35x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 618 ms: 1.34x faster                                                        |
| raytrace                   | 213 ms                                                      | 163 ms: 1.31x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 52.2 ms: 1.31x faster                                                       |
| chaos                      | 48.4 ms                                                     | 37.9 ms: 1.28x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.60 sec: 1.27x faster                                                      |
| richards_super             | 38.7 ms                                                     | 30.6 ms: 1.27x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.14 ms: 1.26x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 772 us: 1.23x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 21.0 us: 1.23x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 127 us: 1.23x faster                                                        |
| tomli_loads                | 1.46 sec                                                    | 1.20 sec: 1.21x faster                                                      |
| nbody                      | 70.3 ms                                                     | 58.1 ms: 1.21x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 174 us: 1.20x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 15.4 ms: 1.20x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.83 us: 1.18x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 992 us: 1.17x faster                                                        |
| richards                   | 31.4 ms                                                     | 26.8 ms: 1.17x faster                                                       |
| pyflate                    | 312 ms                                                      | 268 ms: 1.17x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 34.3 ms: 1.16x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.0 ms: 1.16x faster                                                       |
| float                      | 54.4 ms                                                     | 47.1 ms: 1.15x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.26 us: 1.15x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.14x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.26 ms: 1.14x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 88.2 ms: 1.13x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.13x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 60.9 ms: 1.12x faster                                                       |
| deepcopy                   | 246 us                                                      | 220 us: 1.12x faster                                                        |
| dulwich_log                | 46.4 ms                                                     | 41.4 ms: 1.12x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 976 ms: 1.11x faster                                                        |
| chameleon                  | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 44.0 ms: 1.11x faster                                                       |
| sympy_str                  | 185 ms                                                      | 167 ms: 1.11x faster                                                        |
| go                         | 101 ms                                                      | 91.4 ms: 1.11x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 83.9 ms: 1.11x faster                                                       |
| fannkuch                   | 253 ms                                                      | 230 ms: 1.10x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 480 ms: 1.10x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 35.3 ms: 1.10x faster                                                       |
| scimark_fft                | 179 ms                                                      | 166 ms: 1.08x faster                                                        |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.9 ms: 1.08x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 90.9 ms: 1.07x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 818 us: 1.07x faster                                                        |
| sympy_expand               | 299 ms                                                      | 282 ms: 1.06x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 13.3 ms: 1.06x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 180 ms: 1.05x faster                                                        |
| regex_compile              | 91.0 ms                                                     | 86.4 ms: 1.05x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.96 us: 1.05x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.53 sec: 1.04x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 73.1 ms: 1.03x faster                                                       |
| mypy2                      | 459 ms                                                      | 448 ms: 1.03x faster                                                        |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 4.47 ms: 1.02x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 35.0 ms: 1.01x slower                                                       |
| aiohttp                    | 883 us                                                      | 907 us: 1.03x slower                                                        |
| 2to3                       | 214 ms                                                      | 221 ms: 1.03x slower                                                        |
| docutils                   | 1.64 sec                                                    | 1.70 sec: 1.04x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| coverage                   | 43.4 ms                                                     | 45.1 ms: 1.04x slower                                                       |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 14.9 ms: 1.05x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 83.5 ms: 1.07x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.61 ms: 1.07x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 68.9 ms: 1.09x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.94 us: 1.09x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.26 us: 1.09x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 78.1 ms: 1.10x slower                                                       |
| python_startup             | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.89 us: 1.12x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 19.7 ms: 1.17x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.84 ms: 1.19x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 75.0 ms: 1.19x slower                                                       |
| unpickle                   | 7.57 us                                                     | 9.30 us: 1.23x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 909 us: 1.27x slower                                                        |
| async_generators           | 177 ms                                                      | 237 ms: 1.34x slower                                                        |
| thrift                     | 494 us                                                      | 8.84 ms: 17.89x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.09x faster                                                                |

Benchmark hidden because not significant (4): json, pycparser, pickle_dict, xml_etree_generate
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown
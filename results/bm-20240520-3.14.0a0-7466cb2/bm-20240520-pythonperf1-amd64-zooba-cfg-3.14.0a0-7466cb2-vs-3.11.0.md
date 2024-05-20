# Results vs. 3.11.0

- fork: zooba
- ref: cfg
- machine: windows-amd64
- commit hash: 7466cb2
- commit date: 2024-05-20
- overall geometric mean: 1.06x faster
- HPT reliability: 96.88%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-pythonperf1-amd64-zooba-cfg-3.14.0a0-7466cb2 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 215 ms: 1.01x slower                                     |
| chameleon      | 5.26 ms                                                     | 5.03 ms: 1.05x faster                                    |
| docutils       | 1.64 sec                                                    | 1.74 sec: 1.06x slower                                   |
| tornado_http   | 92.8 ms                                                     | 86.1 ms: 1.08x faster                                    |
| Geometric mean | (ref)                                                       | 1.01x faster                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-pythonperf1-amd64-zooba-cfg-3.14.0a0-7466cb2 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 279 ms: 1.45x faster                                     |
| async_tree_none            | 332 ms                                                      | 234 ms: 1.42x faster                                     |
| async_tree_memoization     | 399 ms                                                      | 282 ms: 1.42x faster                                     |
| async_tree_none_tg         | 309 ms                                                      | 220 ms: 1.40x faster                                     |
| async_tree_io              | 808 ms                                                      | 618 ms: 1.31x faster                                     |
| async_tree_io_tg           | 829 ms                                                      | 640 ms: 1.30x faster                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 405 ms: 1.29x faster                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 420 ms: 1.26x faster                                     |
| Geometric mean             | (ref)                                                       | 1.35x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-pythonperf1-amd64-zooba-cfg-3.14.0a0-7466cb2 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------:|
| pidigits       | 150 ms                                                      | 151 ms: 1.01x slower                                     |
| float          | 54.4 ms                                                     | 55.6 ms: 1.02x slower                                    |
| nbody          | 70.3 ms                                                     | 72.4 ms: 1.03x slower                                    |
| Geometric mean | (ref)                                                       | 1.02x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-pythonperf1-amd64-zooba-cfg-3.14.0a0-7466cb2 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 85.5 ms: 1.06x faster                                    |
| regex_dna      | 116 ms                                                      | 119 ms: 1.03x slower                                     |
| regex_v8       | 14.2 ms                                                     | 15.0 ms: 1.06x slower                                    |
| regex_effbot   | 1.50 ms                                                     | 1.66 ms: 1.11x slower                                    |
| Geometric mean | (ref)                                                       | 1.03x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-pythonperf1-amd64-zooba-cfg-3.14.0a0-7466cb2 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 6.08 ms: 1.33x faster                                    |
| unpickle_pure_python | 157 us                                                      | 137 us: 1.14x faster                                     |
| pickle_pure_python   | 208 us                                                      | 192 us: 1.09x faster                                     |
| pickle_dict          | 18.5 us                                                     | 18.7 us: 1.01x slower                                    |
| xml_etree_parse      | 97.6 ms                                                     | 104 ms: 1.06x slower                                     |
| xml_etree_process    | 37.2 ms                                                     | 39.7 ms: 1.07x slower                                    |
| xml_etree_iterparse  | 65.6 ms                                                     | 70.9 ms: 1.08x slower                                    |
| pickle               | 6.64 us                                                     | 7.23 us: 1.09x slower                                    |
| xml_etree_generate   | 52.5 ms                                                     | 58.2 ms: 1.11x slower                                    |
| unpickle_list        | 2.59 us                                                     | 2.90 us: 1.12x slower                                    |
| json_loads           | 13.0 us                                                     | 14.8 us: 1.14x slower                                    |
| pickle_list          | 2.70 us                                                     | 3.14 us: 1.16x slower                                    |
| unpickle             | 7.57 us                                                     | 9.08 us: 1.20x slower                                    |
| Geometric mean       | (ref)                                                       | 1.03x slower                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-pythonperf1-amd64-zooba-cfg-3.14.0a0-7466cb2 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                    |
| python_startup         | 19.8 ms                                                     | 21.7 ms: 1.10x slower                                    |
| Geometric mean         | (ref)                                                       | 1.08x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-pythonperf1-amd64-zooba-cfg-3.14.0a0-7466cb2 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 32.8 ms: 1.22x faster                                    |
| genshi_text     | 18.4 ms                                                     | 15.3 ms: 1.20x faster                                    |
| mako            | 7.58 ms                                                     | 6.96 ms: 1.09x faster                                    |
| django_template | 24.4 ms                                                     | 23.0 ms: 1.06x faster                                    |
| Geometric mean  | (ref)                                                       | 1.14x faster                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240520-pythonperf1-amd64-zooba-cfg-3.14.0a0-7466cb2 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 109 us: 2.99x faster                                     |
| generators                 | 34.0 ms                                                     | 20.1 ms: 1.69x faster                                    |
| asyncio_tcp                | 726 ms                                                      | 478 ms: 1.52x faster                                     |
| pylint                     | 323 ms                                                      | 218 ms: 1.48x faster                                     |
| async_tree_memoization_tg  | 405 ms                                                      | 279 ms: 1.45x faster                                     |
| async_tree_none            | 332 ms                                                      | 234 ms: 1.42x faster                                     |
| async_tree_memoization     | 399 ms                                                      | 282 ms: 1.42x faster                                     |
| comprehensions             | 15.6 us                                                     | 11.1 us: 1.41x faster                                    |
| async_tree_none_tg         | 309 ms                                                      | 220 ms: 1.40x faster                                     |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.51 sec: 1.34x faster                                   |
| json_dumps                 | 8.09 ms                                                     | 6.08 ms: 1.33x faster                                    |
| async_tree_io              | 808 ms                                                      | 618 ms: 1.31x faster                                     |
| deltablue                  | 2.70 ms                                                     | 2.07 ms: 1.31x faster                                    |
| async_tree_io_tg           | 829 ms                                                      | 640 ms: 1.30x faster                                     |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 405 ms: 1.29x faster                                     |
| raytrace                   | 213 ms                                                      | 166 ms: 1.28x faster                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 420 ms: 1.26x faster                                     |
| logging_silent             | 71.8 ns                                                     | 58.1 ns: 1.24x faster                                    |
| richards_super             | 38.7 ms                                                     | 31.5 ms: 1.23x faster                                    |
| chaos                      | 48.4 ms                                                     | 39.5 ms: 1.22x faster                                    |
| genshi_xml                 | 39.9 ms                                                     | 32.8 ms: 1.22x faster                                    |
| sqlglot_parse              | 953 us                                                      | 792 us: 1.20x faster                                     |
| genshi_text                | 18.4 ms                                                     | 15.3 ms: 1.20x faster                                    |
| go                         | 101 ms                                                      | 85.9 ms: 1.18x faster                                    |
| sqlglot_transpile          | 1.16 ms                                                     | 1.01 ms: 1.15x faster                                    |
| nqueens                    | 68.3 ms                                                     | 59.4 ms: 1.15x faster                                    |
| unpickle_pure_python       | 157 us                                                      | 137 us: 1.14x faster                                     |
| logging_simple             | 6.86 us                                                     | 6.01 us: 1.14x faster                                    |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.14x faster                                    |
| hexiom                     | 4.55 ms                                                     | 4.04 ms: 1.13x faster                                    |
| richards                   | 31.4 ms                                                     | 28.1 ms: 1.12x faster                                    |
| logging_format             | 7.16 us                                                     | 6.44 us: 1.11x faster                                    |
| mako                       | 7.58 ms                                                     | 6.96 ms: 1.09x faster                                    |
| pickle_pure_python         | 208 us                                                      | 192 us: 1.09x faster                                     |
| sympy_sum                  | 100 ms                                                      | 92.3 ms: 1.08x faster                                    |
| tornado_http               | 92.8 ms                                                     | 86.1 ms: 1.08x faster                                    |
| sympy_integrate            | 14.0 ms                                                     | 13.2 ms: 1.07x faster                                    |
| regex_compile              | 91.0 ms                                                     | 85.5 ms: 1.06x faster                                    |
| django_template            | 24.4 ms                                                     | 23.0 ms: 1.06x faster                                    |
| deepcopy                   | 246 us                                                      | 235 us: 1.05x faster                                     |
| pycparser                  | 720 ms                                                      | 687 ms: 1.05x faster                                     |
| chameleon                  | 5.26 ms                                                     | 5.03 ms: 1.05x faster                                    |
| sqlite_synth               | 1.77 us                                                     | 1.69 us: 1.04x faster                                    |
| deepcopy_memo              | 26.0 us                                                     | 24.9 us: 1.04x faster                                    |
| scimark_monte_carlo        | 45.3 ms                                                     | 43.8 ms: 1.04x faster                                    |
| pyflate                    | 312 ms                                                      | 302 ms: 1.04x faster                                     |
| bench_thread_pool          | 872 us                                                      | 844 us: 1.03x faster                                     |
| sympy_str                  | 185 ms                                                      | 179 ms: 1.03x faster                                     |
| sqlglot_normalize          | 190 ms                                                      | 184 ms: 1.03x faster                                     |
| pprint_pformat             | 1.09 sec                                                    | 1.05 sec: 1.03x faster                                   |
| pprint_safe_repr           | 529 ms                                                      | 518 ms: 1.02x faster                                     |
| meteor_contest             | 75.2 ms                                                     | 74.3 ms: 1.01x faster                                    |
| pidigits                   | 150 ms                                                      | 151 ms: 1.01x slower                                     |
| mdp                        | 1.59 sec                                                    | 1.61 sec: 1.01x slower                                   |
| 2to3                       | 214 ms                                                      | 215 ms: 1.01x slower                                     |
| pickle_dict                | 18.5 us                                                     | 18.7 us: 1.01x slower                                    |
| sqlglot_optimize           | 34.5 ms                                                     | 35.0 ms: 1.01x slower                                    |
| scimark_lu                 | 62.8 ms                                                     | 63.9 ms: 1.02x slower                                    |
| deepcopy_reduce            | 2.06 us                                                     | 2.10 us: 1.02x slower                                    |
| float                      | 54.4 ms                                                     | 55.6 ms: 1.02x slower                                    |
| spectral_norm              | 68.3 ms                                                     | 70.0 ms: 1.02x slower                                    |
| crypto_pyaes               | 48.9 ms                                                     | 50.1 ms: 1.03x slower                                    |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.03x slower                                     |
| sympy_expand               | 299 ms                                                      | 307 ms: 1.03x slower                                     |
| nbody                      | 70.3 ms                                                     | 72.4 ms: 1.03x slower                                    |
| fannkuch                   | 253 ms                                                      | 265 ms: 1.05x slower                                     |
| thrift                     | 494 us                                                      | 521 us: 1.05x slower                                     |
| regex_v8                   | 14.2 ms                                                     | 15.0 ms: 1.06x slower                                    |
| docutils                   | 1.64 sec                                                    | 1.74 sec: 1.06x slower                                   |
| python_startup_no_site     | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                    |
| xml_etree_parse            | 97.6 ms                                                     | 104 ms: 1.06x slower                                     |
| xml_etree_process          | 37.2 ms                                                     | 39.7 ms: 1.07x slower                                    |
| scimark_sor                | 78.1 ms                                                     | 83.8 ms: 1.07x slower                                    |
| json                       | 2.98 ms                                                     | 3.21 ms: 1.08x slower                                    |
| xml_etree_iterparse        | 65.6 ms                                                     | 70.9 ms: 1.08x slower                                    |
| coverage                   | 43.4 ms                                                     | 46.9 ms: 1.08x slower                                    |
| pickle                     | 6.64 us                                                     | 7.23 us: 1.09x slower                                    |
| python_startup             | 19.8 ms                                                     | 21.7 ms: 1.10x slower                                    |
| regex_effbot               | 1.50 ms                                                     | 1.66 ms: 1.11x slower                                    |
| xml_etree_generate         | 52.5 ms                                                     | 58.2 ms: 1.11x slower                                    |
| bench_mp_pool              | 63.2 ms                                                     | 70.6 ms: 1.12x slower                                    |
| unpickle_list              | 2.59 us                                                     | 2.90 us: 1.12x slower                                    |
| pathlib                    | 70.9 ms                                                     | 79.8 ms: 1.13x slower                                    |
| json_loads                 | 13.0 us                                                     | 14.8 us: 1.14x slower                                    |
| pickle_list                | 2.70 us                                                     | 3.14 us: 1.16x slower                                    |
| scimark_fft                | 179 ms                                                      | 212 ms: 1.18x slower                                     |
| unpickle                   | 7.57 us                                                     | 9.08 us: 1.20x slower                                    |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 3.14 ms: 1.22x slower                                    |
| telco                      | 4.06 ms                                                     | 5.05 ms: 1.24x slower                                    |
| async_generators           | 177 ms                                                      | 253 ms: 1.43x slower                                     |
| create_gc_cycles           | 713 us                                                      | 1.08 ms: 1.51x slower                                    |
| gc_traversal               | 1.49 ms                                                     | 2.80 ms: 1.88x slower                                    |
| Geometric mean             | (ref)                                                       | 1.06x faster                                             |

Benchmark hidden because not significant (3): flaskblogging, tomli_loads, html5lib
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.88% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
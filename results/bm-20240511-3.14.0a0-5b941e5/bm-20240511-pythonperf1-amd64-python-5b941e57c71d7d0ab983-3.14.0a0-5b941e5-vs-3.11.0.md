# Results vs. 3.11.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: windows-amd64
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.13x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 209 ms: 1.02x faster                                                       |
| chameleon      | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                      |
| docutils       | 1.64 sec                                                    | 1.62 sec: 1.01x faster                                                     |
| html5lib       | 38.9 ms                                                     | 34.1 ms: 1.14x faster                                                      |
| tornado_http   | 92.8 ms                                                     | 82.5 ms: 1.12x faster                                                      |
| Geometric mean | (ref)                                                       | 1.08x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 266 ms: 1.52x faster                                                       |
| async_tree_none            | 332 ms                                                      | 220 ms: 1.51x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 206 ms: 1.50x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 267 ms: 1.50x faster                                                       |
| async_tree_io              | 808 ms                                                      | 587 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 386 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 607 ms: 1.37x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.44x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 48.8 ms: 1.11x faster                                                      |
| nbody          | 70.3 ms                                                     | 68.4 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                       | 1.05x faster                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 77.4 ms: 1.18x faster                                                      |
| regex_dna      | 116 ms                                                      | 119 ms: 1.03x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.63 ms: 1.09x slower                                                      |
| regex_v8       | 14.2 ms                                                     | 15.5 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                       | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.53 ms: 1.46x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 119 us: 1.31x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 177 us: 1.18x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 90.1 ms: 1.08x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.5 ms: 1.07x faster                                                      |
| tomli_loads          | 1.46 sec                                                    | 1.38 sec: 1.05x faster                                                     |
| xml_etree_process    | 37.2 ms                                                     | 36.3 ms: 1.02x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 18.3 us: 1.01x faster                                                      |
| json_loads           | 13.0 us                                                     | 14.0 us: 1.08x slower                                                      |
| pickle               | 6.64 us                                                     | 7.17 us: 1.08x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.83 us: 1.09x slower                                                      |
| pickle_list          | 2.70 us                                                     | 3.11 us: 1.15x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.88 us: 1.17x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                               |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.1 ms: 1.02x slower                                                      |
| python_startup         | 19.8 ms                                                     | 20.5 ms: 1.04x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.03x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 14.7 ms: 1.25x faster                                                      |
| genshi_xml      | 39.9 ms                                                     | 32.1 ms: 1.25x faster                                                      |
| mako            | 7.58 ms                                                     | 6.20 ms: 1.22x faster                                                      |
| django_template | 24.4 ms                                                     | 22.0 ms: 1.11x faster                                                      |
| Geometric mean  | (ref)                                                       | 1.21x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 99.6 us: 3.27x faster                                                      |
| generators                 | 34.0 ms                                                     | 19.1 ms: 1.78x faster                                                      |
| pylint                     | 323 ms                                                      | 206 ms: 1.57x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 266 ms: 1.52x faster                                                       |
| comprehensions             | 15.6 us                                                     | 10.3 us: 1.52x faster                                                      |
| async_tree_none            | 332 ms                                                      | 220 ms: 1.51x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 206 ms: 1.50x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 267 ms: 1.50x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.53 ms: 1.46x faster                                                      |
| deltablue                  | 2.70 ms                                                     | 1.92 ms: 1.41x faster                                                      |
| async_tree_io              | 808 ms                                                      | 587 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 386 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 607 ms: 1.37x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 52.9 ns: 1.36x faster                                                      |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.50 sec: 1.35x faster                                                     |
| unpickle_pure_python       | 157 us                                                      | 119 us: 1.31x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 564 ms: 1.29x faster                                                       |
| raytrace                   | 213 ms                                                      | 167 ms: 1.27x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.3 ms: 1.26x faster                                                      |
| genshi_text                | 18.4 ms                                                     | 14.7 ms: 1.25x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 764 us: 1.25x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 32.1 ms: 1.25x faster                                                      |
| go                         | 101 ms                                                      | 81.4 ms: 1.24x faster                                                      |
| richards_super             | 38.7 ms                                                     | 31.3 ms: 1.24x faster                                                      |
| hexiom                     | 4.55 ms                                                     | 3.68 ms: 1.24x faster                                                      |
| mako                       | 7.58 ms                                                     | 6.20 ms: 1.22x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 973 us: 1.20x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 57.4 ms: 1.19x faster                                                      |
| sympy_sum                  | 100 ms                                                      | 84.9 ms: 1.18x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.82 us: 1.18x faster                                                      |
| pickle_pure_python         | 208 us                                                      | 177 us: 1.18x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 77.4 ms: 1.18x faster                                                      |
| coroutines                 | 15.0 ms                                                     | 12.8 ms: 1.17x faster                                                      |
| deepcopy_memo              | 26.0 us                                                     | 22.3 us: 1.16x faster                                                      |
| sympy_str                  | 185 ms                                                      | 160 ms: 1.16x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.2 ms: 1.15x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.27 us: 1.14x faster                                                      |
| richards                   | 31.4 ms                                                     | 27.5 ms: 1.14x faster                                                      |
| scimark_lu                 | 62.8 ms                                                     | 55.1 ms: 1.14x faster                                                      |
| html5lib                   | 38.9 ms                                                     | 34.1 ms: 1.14x faster                                                      |
| deepcopy                   | 246 us                                                      | 218 us: 1.13x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 963 ms: 1.13x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 82.5 ms: 1.12x faster                                                      |
| pprint_safe_repr           | 529 ms                                                      | 471 ms: 1.12x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.43 sec: 1.11x faster                                                     |
| float                      | 54.4 ms                                                     | 48.8 ms: 1.11x faster                                                      |
| chameleon                  | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                      |
| django_template            | 24.4 ms                                                     | 22.0 ms: 1.11x faster                                                      |
| pyflate                    | 312 ms                                                      | 282 ms: 1.11x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 62.1 ms: 1.10x faster                                                      |
| sympy_expand               | 299 ms                                                      | 272 ms: 1.10x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                      |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.7 ms: 1.09x faster                                                      |
| sqlglot_normalize          | 190 ms                                                      | 175 ms: 1.09x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 90.1 ms: 1.08x faster                                                      |
| bench_thread_pool          | 872 us                                                      | 818 us: 1.07x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.5 ms: 1.07x faster                                                      |
| scimark_sor                | 78.1 ms                                                     | 74.1 ms: 1.05x faster                                                      |
| deepcopy_reduce            | 2.06 us                                                     | 1.96 us: 1.05x faster                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.38 sec: 1.05x faster                                                     |
| meteor_contest             | 75.2 ms                                                     | 72.4 ms: 1.04x faster                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 33.3 ms: 1.04x faster                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 47.5 ms: 1.03x faster                                                      |
| nbody                      | 70.3 ms                                                     | 68.4 ms: 1.03x faster                                                      |
| xml_etree_process          | 37.2 ms                                                     | 36.3 ms: 1.02x faster                                                      |
| 2to3                       | 214 ms                                                      | 209 ms: 1.02x faster                                                       |
| docutils                   | 1.64 sec                                                    | 1.62 sec: 1.01x faster                                                     |
| fannkuch                   | 253 ms                                                      | 251 ms: 1.01x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 18.3 us: 1.01x faster                                                      |
| coverage                   | 43.4 ms                                                     | 43.2 ms: 1.00x faster                                                      |
| scimark_fft                | 179 ms                                                      | 182 ms: 1.02x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 17.1 ms: 1.02x slower                                                      |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                      |
| python_startup             | 19.8 ms                                                     | 20.5 ms: 1.04x slower                                                      |
| json                       | 2.98 ms                                                     | 3.13 ms: 1.05x slower                                                      |
| json_loads                 | 13.0 us                                                     | 14.0 us: 1.08x slower                                                      |
| pickle                     | 6.64 us                                                     | 7.17 us: 1.08x slower                                                      |
| regex_effbot               | 1.50 ms                                                     | 1.63 ms: 1.09x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.83 us: 1.09x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 15.5 ms: 1.10x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 69.7 ms: 1.10x slower                                                      |
| pathlib                    | 70.9 ms                                                     | 79.9 ms: 1.13x slower                                                      |
| pickle_list                | 2.70 us                                                     | 3.11 us: 1.15x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.88 us: 1.17x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.77 ms: 1.17x slower                                                      |
| create_gc_cycles           | 713 us                                                      | 892 us: 1.25x slower                                                       |
| async_generators           | 177 ms                                                      | 230 ms: 1.30x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.13x faster                                                               |

Benchmark hidden because not significant (6): pycparser, scimark_sparse_mat_mult, thrift, flaskblogging, pidigits, xml_etree_generate
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown
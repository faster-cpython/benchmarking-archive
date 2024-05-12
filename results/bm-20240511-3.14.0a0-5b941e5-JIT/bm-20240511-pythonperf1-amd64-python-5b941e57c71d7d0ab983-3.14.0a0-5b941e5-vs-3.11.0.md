# Results vs. 3.11.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: windows-amd64
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 232 ms: 1.09x slower                                                       |
| chameleon      | 5.26 ms                                                     | 4.99 ms: 1.05x faster                                                      |
| docutils       | 1.64 sec                                                    | 1.76 sec: 1.07x slower                                                     |
| html5lib       | 38.9 ms                                                     | 37.0 ms: 1.05x faster                                                      |
| tornado_http   | 92.8 ms                                                     | 85.4 ms: 1.09x faster                                                      |
| Geometric mean | (ref)                                                       | 1.01x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                       |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 275 ms: 1.45x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 213 ms: 1.45x faster                                                       |
| async_tree_io              | 808 ms                                                      | 589 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 387 ms: 1.35x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 619 ms: 1.34x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 396 ms: 1.34x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.41x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 49.9 ms: 1.41x faster                                                      |
| float          | 54.4 ms                                                     | 43.4 ms: 1.25x faster                                                      |
| Geometric mean | (ref)                                                       | 1.21x faster                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 86.6 ms: 1.05x faster                                                      |
| regex_dna      | 116 ms                                                      | 114 ms: 1.02x faster                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                      |
| regex_v8       | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                      |
| Geometric mean | (ref)                                                       | 1.01x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.65 ms: 1.43x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 124 us: 1.26x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.23 sec: 1.19x faster                                                     |
| xml_etree_iterparse  | 65.6 ms                                                     | 59.9 ms: 1.09x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 91.6 ms: 1.07x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 17.5 us: 1.06x faster                                                      |
| xml_etree_process    | 37.2 ms                                                     | 36.1 ms: 1.03x faster                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 51.1 ms: 1.03x faster                                                      |
| pickle_list          | 2.70 us                                                     | 2.80 us: 1.04x slower                                                      |
| json_loads           | 13.0 us                                                     | 14.3 us: 1.10x slower                                                      |
| pickle               | 6.64 us                                                     | 7.35 us: 1.11x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.88 us: 1.11x slower                                                      |
| unpickle             | 7.57 us                                                     | 8.69 us: 1.15x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 18.2 ms: 1.08x slower                                                      |
| python_startup         | 19.8 ms                                                     | 22.0 ms: 1.11x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.10x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 4.94 ms: 1.53x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 17.8 ms: 1.04x faster                                                      |
| django_template | 24.4 ms                                                     | 25.4 ms: 1.04x slower                                                      |
| genshi_xml      | 39.9 ms                                                     | 44.8 ms: 1.12x slower                                                      |
| Geometric mean  | (ref)                                                       | 1.08x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 112 us: 2.90x faster                                                       |
| generators                 | 34.0 ms                                                     | 22.0 ms: 1.55x faster                                                      |
| mako                       | 7.58 ms                                                     | 4.94 ms: 1.53x faster                                                      |
| comprehensions             | 15.6 us                                                     | 10.3 us: 1.52x faster                                                      |
| spectral_norm              | 68.3 ms                                                     | 44.9 ms: 1.52x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                       |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 275 ms: 1.45x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 213 ms: 1.45x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.65 ms: 1.43x faster                                                      |
| nbody                      | 70.3 ms                                                     | 49.9 ms: 1.41x faster                                                      |
| async_tree_io              | 808 ms                                                      | 589 ms: 1.37x faster                                                       |
| pylint                     | 323 ms                                                      | 238 ms: 1.36x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 387 ms: 1.35x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 619 ms: 1.34x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 396 ms: 1.34x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.52 sec: 1.34x faster                                                     |
| asyncio_tcp                | 726 ms                                                      | 545 ms: 1.33x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 54.5 ns: 1.32x faster                                                      |
| deepcopy_memo              | 26.0 us                                                     | 20.5 us: 1.27x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 124 us: 1.26x faster                                                       |
| float                      | 54.4 ms                                                     | 43.4 ms: 1.25x faster                                                      |
| chaos                      | 48.4 ms                                                     | 39.4 ms: 1.23x faster                                                      |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.14 ms: 1.20x faster                                                      |
| richards_super             | 38.7 ms                                                     | 32.3 ms: 1.20x faster                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 40.8 ms: 1.20x faster                                                      |
| scimark_monte_carlo        | 45.3 ms                                                     | 37.9 ms: 1.20x faster                                                      |
| raytrace                   | 213 ms                                                      | 179 ms: 1.20x faster                                                       |
| scimark_fft                | 179 ms                                                      | 150 ms: 1.19x faster                                                       |
| pyflate                    | 312 ms                                                      | 262 ms: 1.19x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 803 us: 1.19x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.23 sec: 1.19x faster                                                     |
| pprint_safe_repr           | 529 ms                                                      | 450 ms: 1.18x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 924 ms: 1.18x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.88 us: 1.17x faster                                                      |
| deltablue                  | 2.70 ms                                                     | 2.32 ms: 1.16x faster                                                      |
| fannkuch                   | 253 ms                                                      | 223 ms: 1.14x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.31 us: 1.14x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 1.04 ms: 1.12x faster                                                      |
| coroutines                 | 15.0 ms                                                     | 13.3 ms: 1.12x faster                                                      |
| nqueens                    | 68.3 ms                                                     | 61.1 ms: 1.12x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.58 us: 1.12x faster                                                      |
| richards                   | 31.4 ms                                                     | 28.5 ms: 1.10x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 59.9 ms: 1.09x faster                                                      |
| go                         | 101 ms                                                      | 92.6 ms: 1.09x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 85.4 ms: 1.09x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.47 sec: 1.08x faster                                                     |
| sympy_sum                  | 100 ms                                                      | 93.6 ms: 1.07x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 91.6 ms: 1.07x faster                                                      |
| deepcopy                   | 246 us                                                      | 233 us: 1.06x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 17.5 us: 1.06x faster                                                      |
| chameleon                  | 5.26 ms                                                     | 4.99 ms: 1.05x faster                                                      |
| regex_compile              | 91.0 ms                                                     | 86.6 ms: 1.05x faster                                                      |
| html5lib                   | 38.9 ms                                                     | 37.0 ms: 1.05x faster                                                      |
| bench_thread_pool          | 872 us                                                      | 832 us: 1.05x faster                                                       |
| sympy_str                  | 185 ms                                                      | 178 ms: 1.04x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 17.8 ms: 1.04x faster                                                      |
| xml_etree_process          | 37.2 ms                                                     | 36.1 ms: 1.03x faster                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 51.1 ms: 1.03x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 73.2 ms: 1.03x faster                                                      |
| regex_dna                  | 116 ms                                                      | 114 ms: 1.02x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.04 us: 1.01x faster                                                      |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                     |
| hexiom                     | 4.55 ms                                                     | 4.65 ms: 1.02x slower                                                      |
| sympy_expand               | 299 ms                                                      | 309 ms: 1.03x slower                                                       |
| coverage                   | 43.4 ms                                                     | 45.1 ms: 1.04x slower                                                      |
| django_template            | 24.4 ms                                                     | 25.4 ms: 1.04x slower                                                      |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                      |
| pickle_list                | 2.70 us                                                     | 2.80 us: 1.04x slower                                                      |
| pycparser                  | 720 ms                                                      | 754 ms: 1.05x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| scimark_sor                | 78.1 ms                                                     | 82.6 ms: 1.06x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.76 sec: 1.07x slower                                                     |
| sqlglot_optimize           | 34.5 ms                                                     | 37.1 ms: 1.07x slower                                                      |
| scimark_lu                 | 62.8 ms                                                     | 67.5 ms: 1.07x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                      |
| thrift                     | 494 us                                                      | 533 us: 1.08x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 18.2 ms: 1.08x slower                                                      |
| 2to3                       | 214 ms                                                      | 232 ms: 1.09x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.3 us: 1.10x slower                                                      |
| pickle                     | 6.64 us                                                     | 7.35 us: 1.11x slower                                                      |
| python_startup             | 19.8 ms                                                     | 22.0 ms: 1.11x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.88 us: 1.11x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 70.5 ms: 1.11x slower                                                      |
| genshi_xml                 | 39.9 ms                                                     | 44.8 ms: 1.12x slower                                                      |
| pathlib                    | 70.9 ms                                                     | 79.6 ms: 1.12x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.63 ms: 1.14x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.69 us: 1.15x slower                                                      |
| create_gc_cycles           | 713 us                                                      | 906 us: 1.27x slower                                                       |
| async_generators           | 177 ms                                                      | 259 ms: 1.46x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                               |

Benchmark hidden because not significant (3): pidigits, sympy_integrate, json
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown
# Results vs. 3.11.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: windows-amd64
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.01x faster
- HPT reliability: 95.05%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 237 ms: 1.11x slower                                                       |
| chameleon      | 5.26 ms                                                     | 5.39 ms: 1.02x slower                                                      |
| docutils       | 1.64 sec                                                    | 1.85 sec: 1.12x slower                                                     |
| html5lib       | 38.9 ms                                                     | 40.9 ms: 1.05x slower                                                      |
| tornado_http   | 92.8 ms                                                     | 87.9 ms: 1.06x faster                                                      |
| Geometric mean | (ref)                                                       | 1.05x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 279 ms: 1.45x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 285 ms: 1.40x faster                                                       |
| async_tree_none            | 332 ms                                                      | 238 ms: 1.40x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 221 ms: 1.39x faster                                                       |
| async_tree_io              | 808 ms                                                      | 599 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 390 ms: 1.34x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 407 ms: 1.30x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 639 ms: 1.30x faster                                                       |
| Geometric mean             | (ref)                                                       | 1.37x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                      | 151 ms: 1.01x slower                                                       |
| nbody          | 70.3 ms                                                     | 75.7 ms: 1.08x slower                                                      |
| Geometric mean | (ref)                                                       | 1.03x slower                                                               |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| regex_v8       | 14.2 ms                                                     | 14.9 ms: 1.05x slower                                                      |
| regex_compile  | 91.0 ms                                                     | 112 ms: 1.23x slower                                                       |
| Geometric mean | (ref)                                                       | 1.08x slower                                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.76 ms: 1.40x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 90.1 ms: 1.08x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 18.3 us: 1.01x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 66.4 ms: 1.01x slower                                                      |
| tomli_loads          | 1.46 sec                                                    | 1.55 sec: 1.07x slower                                                     |
| unpickle_pure_python | 157 us                                                      | 167 us: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.13 us: 1.07x slower                                                      |
| json_loads           | 13.0 us                                                     | 14.0 us: 1.08x slower                                                      |
| unpickle_list        | 2.59 us                                                     | 2.80 us: 1.08x slower                                                      |
| xml_etree_process    | 37.2 ms                                                     | 40.3 ms: 1.08x slower                                                      |
| xml_etree_generate   | 52.5 ms                                                     | 57.4 ms: 1.09x slower                                                      |
| pickle_pure_python   | 208 us                                                      | 228 us: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.55 us: 1.13x slower                                                      |
| pickle_list          | 2.70 us                                                     | 3.11 us: 1.15x slower                                                      |
| Geometric mean       | (ref)                                                       | 1.03x slower                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.5 ms: 1.02x faster                                                      |
| python_startup         | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                                      |
| Geometric mean         | (ref)                                                       | 1.00x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|-----------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 37.0 ms: 1.08x faster                                                      |
| genshi_text     | 18.4 ms                                                     | 17.8 ms: 1.04x faster                                                      |
| django_template | 24.4 ms                                                     | 25.2 ms: 1.03x slower                                                      |
| mako            | 7.58 ms                                                     | 7.85 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                       | 1.01x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1-amd64-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:-----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 116 us: 2.82x faster                                                       |
| generators                 | 34.0 ms                                                     | 20.7 ms: 1.64x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 279 ms: 1.45x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.76 ms: 1.40x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 285 ms: 1.40x faster                                                       |
| async_tree_none            | 332 ms                                                      | 238 ms: 1.40x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 221 ms: 1.39x faster                                                       |
| pylint                     | 323 ms                                                      | 235 ms: 1.38x faster                                                       |
| async_tree_io              | 808 ms                                                      | 599 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 390 ms: 1.34x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.53 sec: 1.32x faster                                                     |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 407 ms: 1.30x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 639 ms: 1.30x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 572 ms: 1.27x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.9 ms: 1.16x faster                                                      |
| raytrace                   | 213 ms                                                      | 190 ms: 1.12x faster                                                       |
| richards_super             | 38.7 ms                                                     | 34.7 ms: 1.12x faster                                                      |
| logging_simple             | 6.86 us                                                     | 6.21 us: 1.10x faster                                                      |
| comprehensions             | 15.6 us                                                     | 14.3 us: 1.09x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.47 sec: 1.09x faster                                                     |
| xml_etree_parse            | 97.6 ms                                                     | 90.1 ms: 1.08x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.63 us: 1.08x faster                                                      |
| genshi_xml                 | 39.9 ms                                                     | 37.0 ms: 1.08x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.65 us: 1.08x faster                                                      |
| chaos                      | 48.4 ms                                                     | 45.6 ms: 1.06x faster                                                      |
| tornado_http               | 92.8 ms                                                     | 87.9 ms: 1.06x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 919 us: 1.04x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 17.8 ms: 1.04x faster                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 16.5 ms: 1.02x faster                                                      |
| richards                   | 31.4 ms                                                     | 30.9 ms: 1.02x faster                                                      |
| pickle_dict                | 18.5 us                                                     | 18.3 us: 1.01x faster                                                      |
| sqlglot_transpile          | 1.16 ms                                                     | 1.16 ms: 1.01x faster                                                      |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                     |
| sympy_sum                  | 100 ms                                                      | 101 ms: 1.01x slower                                                       |
| pidigits                   | 150 ms                                                      | 151 ms: 1.01x slower                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 66.4 ms: 1.01x slower                                                      |
| deltablue                  | 2.70 ms                                                     | 2.75 ms: 1.02x slower                                                      |
| chameleon                  | 5.26 ms                                                     | 5.39 ms: 1.02x slower                                                      |
| python_startup             | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                                      |
| go                         | 101 ms                                                      | 104 ms: 1.03x slower                                                       |
| django_template            | 24.4 ms                                                     | 25.2 ms: 1.03x slower                                                      |
| mako                       | 7.58 ms                                                     | 7.85 ms: 1.03x slower                                                      |
| meteor_contest             | 75.2 ms                                                     | 78.1 ms: 1.04x slower                                                      |
| nqueens                    | 68.3 ms                                                     | 71.2 ms: 1.04x slower                                                      |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| html5lib                   | 38.9 ms                                                     | 40.9 ms: 1.05x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 14.9 ms: 1.05x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.57 ms: 1.05x slower                                                      |
| sympy_integrate            | 14.0 ms                                                     | 14.9 ms: 1.06x slower                                                      |
| coverage                   | 43.4 ms                                                     | 46.0 ms: 1.06x slower                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.55 sec: 1.07x slower                                                     |
| logging_silent             | 71.8 ns                                                     | 76.5 ns: 1.07x slower                                                      |
| thrift                     | 494 us                                                      | 527 us: 1.07x slower                                                       |
| sympy_str                  | 185 ms                                                      | 198 ms: 1.07x slower                                                       |
| unpickle_pure_python       | 157 us                                                      | 167 us: 1.07x slower                                                       |
| pprint_pformat             | 1.09 sec                                                    | 1.17 sec: 1.07x slower                                                     |
| pickle                     | 6.64 us                                                     | 7.13 us: 1.07x slower                                                      |
| nbody                      | 70.3 ms                                                     | 75.7 ms: 1.08x slower                                                      |
| pprint_safe_repr           | 529 ms                                                      | 570 ms: 1.08x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.0 us: 1.08x slower                                                      |
| deepcopy                   | 246 us                                                      | 266 us: 1.08x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.80 us: 1.08x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 68.5 ms: 1.08x slower                                                      |
| xml_etree_process          | 37.2 ms                                                     | 40.3 ms: 1.08x slower                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 53.1 ms: 1.09x slower                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 57.4 ms: 1.09x slower                                                      |
| pickle_pure_python         | 208 us                                                      | 228 us: 1.10x slower                                                       |
| pycparser                  | 720 ms                                                      | 788 ms: 1.10x slower                                                       |
| pyflate                    | 312 ms                                                      | 343 ms: 1.10x slower                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.27 us: 1.10x slower                                                      |
| 2to3                       | 214 ms                                                      | 237 ms: 1.11x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.85 sec: 1.12x slower                                                     |
| pathlib                    | 70.9 ms                                                     | 80.0 ms: 1.13x slower                                                      |
| unpickle                   | 7.57 us                                                     | 8.55 us: 1.13x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 39.1 ms: 1.13x slower                                                      |
| sympy_expand               | 299 ms                                                      | 338 ms: 1.13x slower                                                       |
| fannkuch                   | 253 ms                                                      | 289 ms: 1.14x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.11 us: 1.15x slower                                                      |
| scimark_fft                | 179 ms                                                      | 207 ms: 1.16x slower                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 52.7 ms: 1.16x slower                                                      |
| scimark_sor                | 78.1 ms                                                     | 92.5 ms: 1.18x slower                                                      |
| telco                      | 4.06 ms                                                     | 4.84 ms: 1.19x slower                                                      |
| spectral_norm              | 68.3 ms                                                     | 81.6 ms: 1.19x slower                                                      |
| deepcopy_memo              | 26.0 us                                                     | 31.2 us: 1.20x slower                                                      |
| regex_compile              | 91.0 ms                                                     | 112 ms: 1.23x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 896 us: 1.26x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 5.76 ms: 1.27x slower                                                      |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 3.29 ms: 1.28x slower                                                      |
| scimark_lu                 | 62.8 ms                                                     | 81.6 ms: 1.30x slower                                                      |
| async_generators           | 177 ms                                                      | 247 ms: 1.39x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.01x faster                                                               |

Benchmark hidden because not significant (4): bench_thread_pool, regex_dna, float, json
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 95.05% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown
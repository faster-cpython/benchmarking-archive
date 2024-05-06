# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.03x slower
- HPT reliability: 99.90%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 225 ms: 1.03x slower                                                        |
| chameleon      | 4.98 ms                                                     | 5.11 ms: 1.03x slower                                                       |
| docutils       | 1.66 sec                                                    | 1.74 sec: 1.05x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 85.6 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 285 ms                                                      | 207 ms: 1.38x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 270 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 377 ms: 1.33x faster                                                        |
| async_tree_none            | 291 ms                                                      | 222 ms: 1.31x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 381 ms: 1.28x faster                                                        |
| async_tree_io              | 731 ms                                                      | 580 ms: 1.26x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 273 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 627 ms: 1.23x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.30x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 152 ms                                                      | 147 ms: 1.03x faster                                                        |
| float          | 56.8 ms                                                     | 59.3 ms: 1.04x slower                                                       |
| nbody          | 71.9 ms                                                     | 84.9 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                       | 1.06x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 122 ms: 1.03x faster                                                        |
| regex_compile  | 87.5 ms                                                     | 103 ms: 1.18x slower                                                        |
| regex_v8       | 14.2 ms                                                     | 17.4 ms: 1.22x slower                                                       |
| Geometric mean | (ref)                                                       | 1.09x slower                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle               | 7.43 us                                                     | 7.04 us: 1.06x faster                                                       |
| pickle_pure_python   | 195 us                                                      | 189 us: 1.04x faster                                                        |
| xml_etree_parse      | 93.0 ms                                                     | 90.3 ms: 1.03x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.1 us: 1.01x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.73 ms: 1.01x slower                                                       |
| pickle_list          | 2.83 us                                                     | 2.85 us: 1.01x slower                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 56.4 ms: 1.01x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.79 us: 1.01x slower                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 66.5 ms: 1.02x slower                                                       |
| xml_etree_process    | 37.7 ms                                                     | 39.0 ms: 1.03x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.57 us: 1.05x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.51 sec: 1.10x slower                                                      |
| unpickle_pure_python | 133 us                                                      | 167 us: 1.25x slower                                                        |
| Geometric mean       | (ref)                                                       | 1.02x slower                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 20.5 ms: 1.06x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 18.1 ms: 1.12x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.09x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 22.9 ms                                                     | 23.6 ms: 1.03x slower                                                       |
| mako            | 7.09 ms                                                     | 7.56 ms: 1.07x slower                                                       |
| Geometric mean  | (ref)                                                       | 1.05x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.49 sec: 1.41x faster                                                      |
| async_tree_none_tg         | 285 ms                                                      | 207 ms: 1.38x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 270 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 377 ms: 1.33x faster                                                        |
| async_tree_none            | 291 ms                                                      | 222 ms: 1.31x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 72.8 us: 1.31x faster                                                       |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 381 ms: 1.28x faster                                                        |
| async_tree_io              | 731 ms                                                      | 580 ms: 1.26x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 273 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 627 ms: 1.23x faster                                                        |
| mypy2                      | 509 ms                                                      | 458 ms: 1.11x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.64 us: 1.08x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 65.1 ms: 1.06x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 57.2 ns: 1.06x faster                                                       |
| asyncio_tcp                | 487 ms                                                      | 461 ms: 1.06x faster                                                        |
| pickle                     | 7.43 us                                                     | 7.04 us: 1.06x faster                                                       |
| coroutines                 | 14.3 ms                                                     | 13.5 ms: 1.05x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 85.6 ms: 1.05x faster                                                       |
| generators                 | 22.5 ms                                                     | 21.7 ms: 1.04x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 189 us: 1.04x faster                                                        |
| pidigits                   | 152 ms                                                      | 147 ms: 1.03x faster                                                        |
| regex_dna                  | 126 ms                                                      | 122 ms: 1.03x faster                                                        |
| xml_etree_parse            | 93.0 ms                                                     | 90.3 ms: 1.03x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 78.5 ms: 1.03x faster                                                       |
| pickle_dict                | 18.4 us                                                     | 18.1 us: 1.01x faster                                                       |
| deepcopy                   | 238 us                                                      | 236 us: 1.01x faster                                                        |
| dulwich_log                | 44.3 ms                                                     | 44.5 ms: 1.00x slower                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.73 ms: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.53 ms: 1.01x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.85 us: 1.01x slower                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 56.4 ms: 1.01x slower                                                       |
| unpickle_list              | 2.75 us                                                     | 2.79 us: 1.01x slower                                                       |
| logging_format             | 6.72 us                                                     | 6.83 us: 1.02x slower                                                       |
| logging_simple             | 6.28 us                                                     | 6.40 us: 1.02x slower                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 66.5 ms: 1.02x slower                                                       |
| sympy_sum                  | 91.5 ms                                                     | 93.9 ms: 1.03x slower                                                       |
| comprehensions             | 14.1 us                                                     | 14.5 us: 1.03x slower                                                       |
| raytrace                   | 192 ms                                                      | 197 ms: 1.03x slower                                                        |
| chameleon                  | 4.98 ms                                                     | 5.11 ms: 1.03x slower                                                       |
| django_template            | 22.9 ms                                                     | 23.6 ms: 1.03x slower                                                       |
| aiohttp                    | 884 us                                                      | 913 us: 1.03x slower                                                        |
| 2to3                       | 218 ms                                                      | 225 ms: 1.03x slower                                                        |
| xml_etree_process          | 37.7 ms                                                     | 39.0 ms: 1.03x slower                                                       |
| meteor_contest             | 74.6 ms                                                     | 77.2 ms: 1.03x slower                                                       |
| sympy_str                  | 175 ms                                                      | 181 ms: 1.03x slower                                                        |
| mdp                        | 1.37 sec                                                    | 1.42 sec: 1.04x slower                                                      |
| sqlglot_normalize          | 187 ms                                                      | 194 ms: 1.04x slower                                                        |
| float                      | 56.8 ms                                                     | 59.3 ms: 1.04x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.57 us: 1.05x slower                                                       |
| docutils                   | 1.66 sec                                                    | 1.74 sec: 1.05x slower                                                      |
| sqlglot_parse              | 804 us                                                      | 843 us: 1.05x slower                                                        |
| chaos                      | 43.3 ms                                                     | 45.4 ms: 1.05x slower                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 1.07 ms: 1.05x slower                                                       |
| deltablue                  | 2.16 ms                                                     | 2.27 ms: 1.05x slower                                                       |
| python_startup             | 19.5 ms                                                     | 20.5 ms: 1.06x slower                                                       |
| deepcopy_memo              | 23.7 us                                                     | 25.2 us: 1.06x slower                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 51.6 ms: 1.06x slower                                                       |
| async_generators           | 239 ms                                                      | 255 ms: 1.06x slower                                                        |
| richards_super             | 32.1 ms                                                     | 34.2 ms: 1.06x slower                                                       |
| mako                       | 7.09 ms                                                     | 7.56 ms: 1.07x slower                                                       |
| pycparser                  | 699 ms                                                      | 746 ms: 1.07x slower                                                        |
| pprint_safe_repr           | 513 ms                                                      | 550 ms: 1.07x slower                                                        |
| richards                   | 28.4 ms                                                     | 30.5 ms: 1.07x slower                                                       |
| sympy_integrate            | 13.0 ms                                                     | 13.9 ms: 1.08x slower                                                       |
| pprint_pformat             | 1.05 sec                                                    | 1.13 sec: 1.08x slower                                                      |
| sympy_expand               | 284 ms                                                      | 306 ms: 1.08x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 37.5 ms: 1.09x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.51 sec: 1.10x slower                                                      |
| python_startup_no_site     | 16.2 ms                                                     | 18.1 ms: 1.12x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 850 us: 1.13x slower                                                        |
| go                         | 91.6 ms                                                     | 104 ms: 1.13x slower                                                        |
| unpack_sequence            | 37.5 ns                                                     | 42.5 ns: 1.13x slower                                                       |
| coverage                   | 40.8 ms                                                     | 46.3 ms: 1.13x slower                                                       |
| nqueens                    | 62.8 ms                                                     | 73.6 ms: 1.17x slower                                                       |
| scimark_fft                | 184 ms                                                      | 216 ms: 1.17x slower                                                        |
| regex_compile              | 87.5 ms                                                     | 103 ms: 1.18x slower                                                        |
| nbody                      | 71.9 ms                                                     | 84.9 ms: 1.18x slower                                                       |
| fannkuch                   | 247 ms                                                      | 294 ms: 1.19x slower                                                        |
| telco                      | 4.13 ms                                                     | 4.93 ms: 1.19x slower                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 52.4 ms: 1.20x slower                                                       |
| pyflate                    | 295 ms                                                      | 354 ms: 1.20x slower                                                        |
| scimark_sor                | 78.8 ms                                                     | 95.0 ms: 1.21x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 17.4 ms: 1.22x slower                                                       |
| unpickle_pure_python       | 133 us                                                      | 167 us: 1.25x slower                                                        |
| spectral_norm              | 66.9 ms                                                     | 85.5 ms: 1.28x slower                                                       |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 3.29 ms: 1.29x slower                                                       |
| json                       | 3.05 ms                                                     | 3.99 ms: 1.31x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 5.57 ms: 1.36x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 85.4 ms: 1.45x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.03x slower                                                                |

Benchmark hidden because not significant (4): bench_thread_pool, deepcopy_reduce, regex_effbot, json_loads
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-bfc57d4-PYTHON_UOPS/bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.90% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown
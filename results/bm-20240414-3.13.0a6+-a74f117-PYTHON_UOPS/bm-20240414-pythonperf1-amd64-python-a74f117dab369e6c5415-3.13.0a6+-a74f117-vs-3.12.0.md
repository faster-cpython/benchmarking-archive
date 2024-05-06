# Results vs. 3.12.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.00x slower
- HPT reliability: 95.22%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 222 ms: 1.02x slower                                                        |
| chameleon      | 4.98 ms                                                     | 4.90 ms: 1.02x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.75 sec: 1.06x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 83.9 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 273 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 382 ms: 1.31x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 220 ms: 1.30x faster                                                        |
| async_tree_none            | 291 ms                                                      | 226 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 392 ms: 1.25x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 621 ms: 1.24x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 275 ms: 1.23x faster                                                        |
| async_tree_io              | 731 ms                                                      | 596 ms: 1.23x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.27x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| nbody          | 71.9 ms                                                     | 79.3 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 121 ms: 1.05x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.59 ms: 1.02x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| regex_compile  | 87.5 ms                                                     | 103 ms: 1.18x slower                                                        |
| Geometric mean | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 182 us: 1.07x faster                                                        |
| pickle               | 7.43 us                                                     | 7.17 us: 1.04x faster                                                       |
| xml_etree_parse      | 93.0 ms                                                     | 92.1 ms: 1.01x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.66 ms: 1.01x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.7 us: 1.01x slower                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 56.9 ms: 1.02x slower                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 66.6 ms: 1.02x slower                                                       |
| xml_etree_process    | 37.7 ms                                                     | 39.1 ms: 1.04x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.88 us: 1.05x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.46 sec: 1.06x slower                                                      |
| unpickle             | 8.18 us                                                     | 8.83 us: 1.08x slower                                                       |
| unpickle_pure_python | 133 us                                                      | 155 us: 1.16x slower                                                        |
| Geometric mean       | (ref)                                                       | 1.02x slower                                                                |

Benchmark hidden because not significant (2): json_loads, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 16.1 ms: 1.01x faster                                                       |
| python_startup         | 19.5 ms                                                     | 19.7 ms: 1.01x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.00x faster                                                                |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 273 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 382 ms: 1.31x faster                                                        |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.61 sec: 1.30x faster                                                      |
| async_tree_none_tg         | 285 ms                                                      | 220 ms: 1.30x faster                                                        |
| async_tree_none            | 291 ms                                                      | 226 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 392 ms: 1.25x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 621 ms: 1.24x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 76.6 us: 1.24x faster                                                       |
| async_tree_memoization     | 339 ms                                                      | 275 ms: 1.23x faster                                                        |
| async_tree_io              | 731 ms                                                      | 596 ms: 1.23x faster                                                        |
| mypy2                      | 509 ms                                                      | 454 ms: 1.12x faster                                                        |
| raytrace                   | 192 ms                                                      | 175 ms: 1.10x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.2 ms: 1.08x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 182 us: 1.07x faster                                                        |
| sqlite_synth               | 1.76 us                                                     | 1.65 us: 1.07x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 83.9 ms: 1.07x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 56.8 ns: 1.06x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 75.7 ms: 1.06x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 65.2 ms: 1.06x faster                                                       |
| regex_dna                  | 126 ms                                                      | 121 ms: 1.05x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 2.01 us: 1.04x faster                                                       |
| richards                   | 28.4 ms                                                     | 27.3 ms: 1.04x faster                                                       |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                        |
| pickle                     | 7.43 us                                                     | 7.17 us: 1.04x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 827 us: 1.04x faster                                                        |
| deepcopy                   | 238 us                                                      | 231 us: 1.03x faster                                                        |
| richards_super             | 32.1 ms                                                     | 31.2 ms: 1.03x faster                                                       |
| logging_simple             | 6.28 us                                                     | 6.14 us: 1.02x faster                                                       |
| comprehensions             | 14.1 us                                                     | 13.9 us: 1.02x faster                                                       |
| chameleon                  | 4.98 ms                                                     | 4.90 ms: 1.02x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.59 ms: 1.02x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.62 us: 1.01x faster                                                       |
| python_startup_no_site     | 16.2 ms                                                     | 16.1 ms: 1.01x faster                                                       |
| xml_etree_parse            | 93.0 ms                                                     | 92.1 ms: 1.01x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 23.5 us: 1.01x faster                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.66 ms: 1.01x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 74.9 ms: 1.00x slower                                                       |
| sqlglot_normalize          | 187 ms                                                      | 189 ms: 1.01x slower                                                        |
| python_startup             | 19.5 ms                                                     | 19.7 ms: 1.01x slower                                                       |
| pickle_dict                | 18.4 us                                                     | 18.7 us: 1.01x slower                                                       |
| 2to3                       | 218 ms                                                      | 222 ms: 1.02x slower                                                        |
| xml_etree_generate         | 55.8 ms                                                     | 56.9 ms: 1.02x slower                                                       |
| chaos                      | 43.3 ms                                                     | 44.2 ms: 1.02x slower                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 49.5 ms: 1.02x slower                                                       |
| async_generators           | 239 ms                                                      | 245 ms: 1.02x slower                                                        |
| xml_etree_iterparse        | 65.2 ms                                                     | 66.6 ms: 1.02x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.56 ms: 1.02x slower                                                       |
| sympy_sum                  | 91.5 ms                                                     | 93.8 ms: 1.03x slower                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 1.05 ms: 1.03x slower                                                       |
| aiohttp                    | 884 us                                                      | 911 us: 1.03x slower                                                        |
| sqlglot_parse              | 804 us                                                      | 829 us: 1.03x slower                                                        |
| pprint_safe_repr           | 513 ms                                                      | 532 ms: 1.04x slower                                                        |
| xml_etree_process          | 37.7 ms                                                     | 39.1 ms: 1.04x slower                                                       |
| sympy_str                  | 175 ms                                                      | 182 ms: 1.04x slower                                                        |
| unpickle_list              | 2.75 us                                                     | 2.88 us: 1.05x slower                                                       |
| pprint_pformat             | 1.05 sec                                                    | 1.09 sec: 1.05x slower                                                      |
| docutils                   | 1.66 sec                                                    | 1.75 sec: 1.06x slower                                                      |
| pycparser                  | 699 ms                                                      | 743 ms: 1.06x slower                                                        |
| tomli_loads                | 1.37 sec                                                    | 1.46 sec: 1.06x slower                                                      |
| sympy_integrate            | 13.0 ms                                                     | 13.8 ms: 1.07x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 36.8 ms: 1.07x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.83 us: 1.08x slower                                                       |
| sympy_expand               | 284 ms                                                      | 307 ms: 1.08x slower                                                        |
| scimark_fft                | 184 ms                                                      | 199 ms: 1.08x slower                                                        |
| nbody                      | 71.9 ms                                                     | 79.3 ms: 1.10x slower                                                       |
| go                         | 91.6 ms                                                     | 101 ms: 1.11x slower                                                        |
| fannkuch                   | 247 ms                                                      | 274 ms: 1.11x slower                                                        |
| scimark_monte_carlo        | 43.7 ms                                                     | 49.0 ms: 1.12x slower                                                       |
| deltablue                  | 2.16 ms                                                     | 2.44 ms: 1.13x slower                                                       |
| pyflate                    | 295 ms                                                      | 332 ms: 1.13x slower                                                        |
| nqueens                    | 62.8 ms                                                     | 71.2 ms: 1.13x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.56 sec: 1.14x slower                                                      |
| scimark_sor                | 78.8 ms                                                     | 89.4 ms: 1.14x slower                                                       |
| coverage                   | 40.8 ms                                                     | 46.4 ms: 1.14x slower                                                       |
| unpickle_pure_python       | 133 us                                                      | 155 us: 1.16x slower                                                        |
| regex_compile              | 87.5 ms                                                     | 103 ms: 1.18x slower                                                        |
| spectral_norm              | 66.9 ms                                                     | 79.0 ms: 1.18x slower                                                       |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 3.08 ms: 1.21x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 909 us: 1.21x slower                                                        |
| telco                      | 4.13 ms                                                     | 5.03 ms: 1.22x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 5.19 ms: 1.27x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 78.6 ms: 1.33x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (8): json, asyncio_tcp, json_loads, mako, pickle_list, dulwich_log, generators, float
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 95.22% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown
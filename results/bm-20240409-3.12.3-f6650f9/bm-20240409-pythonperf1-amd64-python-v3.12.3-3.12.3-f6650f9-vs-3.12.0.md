# Results vs. 3.12.0

- fork: python
- ref: v3.12.3
- machine: windows-amd64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 210 ms: 1.04x faster                                        |
| chameleon      | 4.98 ms                                                     | 4.94 ms: 1.01x faster                                       |
| docutils       | 1.66 sec                                                    | 1.61 sec: 1.03x faster                                      |
| tornado_http   | 89.5 ms                                                     | 84.8 ms: 1.06x faster                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 346 ms: 1.06x faster                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 484 ms: 1.04x faster                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 475 ms: 1.03x faster                                        |
| async_tree_none_tg         | 285 ms                                                      | 278 ms: 1.03x faster                                        |
| async_tree_io_tg           | 771 ms                                                      | 756 ms: 1.02x faster                                        |
| async_tree_none            | 291 ms                                                      | 287 ms: 1.02x faster                                        |
| async_tree_memoization     | 339 ms                                                      | 334 ms: 1.01x faster                                        |
| Geometric mean             | (ref)                                                       | 1.03x faster                                                |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| pidigits       | 152 ms                                                      | 148 ms: 1.03x faster                                        |
| float          | 56.8 ms                                                     | 55.1 ms: 1.03x faster                                       |
| nbody          | 71.9 ms                                                     | 74.4 ms: 1.04x slower                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 121 ms: 1.05x faster                                        |
| regex_v8       | 14.2 ms                                                     | 13.8 ms: 1.03x faster                                       |
| regex_compile  | 87.5 ms                                                     | 87.1 ms: 1.00x faster                                       |
| regex_effbot   | 1.62 ms                                                     | 1.64 ms: 1.02x slower                                       |
| Geometric mean | (ref)                                                       | 1.02x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 65.2 ms                                                     | 63.0 ms: 1.04x faster                                       |
| unpickle_pure_python | 133 us                                                      | 130 us: 1.02x faster                                        |
| pickle_pure_python   | 195 us                                                      | 192 us: 1.02x faster                                        |
| json_loads           | 13.9 us                                                     | 13.7 us: 1.02x faster                                       |
| xml_etree_parse      | 93.0 ms                                                     | 91.6 ms: 1.02x faster                                       |
| pickle               | 7.43 us                                                     | 7.33 us: 1.01x faster                                       |
| json_dumps           | 5.70 ms                                                     | 5.62 ms: 1.01x faster                                       |
| xml_etree_process    | 37.7 ms                                                     | 37.5 ms: 1.01x faster                                       |
| unpickle             | 8.18 us                                                     | 8.24 us: 1.01x slower                                       |
| pickle_dict          | 18.4 us                                                     | 18.7 us: 1.02x slower                                       |
| unpickle_list        | 2.75 us                                                     | 2.82 us: 1.03x slower                                       |
| pickle_list          | 2.83 us                                                     | 2.95 us: 1.04x slower                                       |
| Geometric mean       | (ref)                                                       | 1.00x faster                                                |

Benchmark hidden because not significant (2): tomli_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 19.1 ms: 1.02x faster                                       |
| python_startup_no_site | 16.2 ms                                                     | 16.0 ms: 1.02x faster                                       |
| Geometric mean         | (ref)                                                       | 1.02x faster                                                |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| comprehensions             | 14.1 us                                                     | 10.9 us: 1.30x faster                                       |
| typing_runtime_protocols   | 95.1 us                                                     | 75.5 us: 1.26x faster                                       |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.89 sec: 1.11x faster                                      |
| sympy_sum                  | 91.5 ms                                                     | 84.5 ms: 1.08x faster                                       |
| richards                   | 28.4 ms                                                     | 26.4 ms: 1.07x faster                                       |
| coverage                   | 40.8 ms                                                     | 38.0 ms: 1.07x faster                                       |
| richards_super             | 32.1 ms                                                     | 30.0 ms: 1.07x faster                                       |
| sympy_str                  | 175 ms                                                      | 164 ms: 1.06x faster                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 346 ms: 1.06x faster                                        |
| go                         | 91.6 ms                                                     | 86.4 ms: 1.06x faster                                       |
| pathlib                    | 80.5 ms                                                     | 76.0 ms: 1.06x faster                                       |
| telco                      | 4.13 ms                                                     | 3.90 ms: 1.06x faster                                       |
| tornado_http               | 89.5 ms                                                     | 84.8 ms: 1.06x faster                                       |
| bench_mp_pool              | 69.2 ms                                                     | 65.6 ms: 1.05x faster                                       |
| scimark_lu                 | 58.9 ms                                                     | 55.9 ms: 1.05x faster                                       |
| scimark_fft                | 184 ms                                                      | 175 ms: 1.05x faster                                        |
| spectral_norm              | 66.9 ms                                                     | 63.8 ms: 1.05x faster                                       |
| bench_thread_pool          | 857 us                                                      | 817 us: 1.05x faster                                        |
| regex_dna                  | 126 ms                                                      | 121 ms: 1.05x faster                                        |
| deepcopy                   | 238 us                                                      | 228 us: 1.05x faster                                        |
| scimark_monte_carlo        | 43.7 ms                                                     | 41.9 ms: 1.04x faster                                       |
| aiohttp                    | 884 us                                                      | 847 us: 1.04x faster                                        |
| async_generators           | 239 ms                                                      | 230 ms: 1.04x faster                                        |
| sympy_integrate            | 13.0 ms                                                     | 12.4 ms: 1.04x faster                                       |
| 2to3                       | 218 ms                                                      | 210 ms: 1.04x faster                                        |
| dulwich_log                | 44.3 ms                                                     | 42.7 ms: 1.04x faster                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 484 ms: 1.04x faster                                        |
| deepcopy_reduce            | 2.09 us                                                     | 2.02 us: 1.04x faster                                       |
| meteor_contest             | 74.6 ms                                                     | 72.1 ms: 1.04x faster                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 63.0 ms: 1.04x faster                                       |
| fannkuch                   | 247 ms                                                      | 238 ms: 1.03x faster                                        |
| regex_v8                   | 14.2 ms                                                     | 13.8 ms: 1.03x faster                                       |
| sqlalchemy_declarative     | 86.4 ms                                                     | 83.6 ms: 1.03x faster                                       |
| docutils                   | 1.66 sec                                                    | 1.61 sec: 1.03x faster                                      |
| pidigits                   | 152 ms                                                      | 148 ms: 1.03x faster                                        |
| sqlglot_normalize          | 187 ms                                                      | 181 ms: 1.03x faster                                        |
| float                      | 56.8 ms                                                     | 55.1 ms: 1.03x faster                                       |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 475 ms: 1.03x faster                                        |
| asyncio_tcp                | 487 ms                                                      | 474 ms: 1.03x faster                                        |
| dask                       | 263 ms                                                      | 255 ms: 1.03x faster                                        |
| async_tree_none_tg         | 285 ms                                                      | 278 ms: 1.03x faster                                        |
| coroutines                 | 14.3 ms                                                     | 13.9 ms: 1.03x faster                                       |
| create_gc_cycles           | 752 us                                                      | 733 us: 1.03x faster                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 33.7 ms: 1.02x faster                                       |
| scimark_sor                | 78.8 ms                                                     | 76.9 ms: 1.02x faster                                       |
| crypto_pyaes               | 48.5 ms                                                     | 47.4 ms: 1.02x faster                                       |
| json                       | 3.05 ms                                                     | 2.98 ms: 1.02x faster                                       |
| deepcopy_memo              | 23.7 us                                                     | 23.2 us: 1.02x faster                                       |
| hexiom                     | 4.10 ms                                                     | 4.01 ms: 1.02x faster                                       |
| mdp                        | 1.37 sec                                                    | 1.34 sec: 1.02x faster                                      |
| unpickle_pure_python       | 133 us                                                      | 130 us: 1.02x faster                                        |
| pickle_pure_python         | 195 us                                                      | 192 us: 1.02x faster                                        |
| sqlalchemy_imperative      | 9.29 ms                                                     | 9.11 ms: 1.02x faster                                       |
| python_startup             | 19.5 ms                                                     | 19.1 ms: 1.02x faster                                       |
| async_tree_io_tg           | 771 ms                                                      | 756 ms: 1.02x faster                                        |
| json_loads                 | 13.9 us                                                     | 13.7 us: 1.02x faster                                       |
| pprint_pformat             | 1.05 sec                                                    | 1.03 sec: 1.02x faster                                      |
| python_startup_no_site     | 16.2 ms                                                     | 16.0 ms: 1.02x faster                                       |
| pprint_safe_repr           | 513 ms                                                      | 505 ms: 1.02x faster                                        |
| xml_etree_parse            | 93.0 ms                                                     | 91.6 ms: 1.02x faster                                       |
| async_tree_none            | 291 ms                                                      | 287 ms: 1.02x faster                                        |
| nqueens                    | 62.8 ms                                                     | 61.9 ms: 1.02x faster                                       |
| async_tree_memoization     | 339 ms                                                      | 334 ms: 1.01x faster                                        |
| gc_traversal               | 1.52 ms                                                     | 1.50 ms: 1.01x faster                                       |
| pickle                     | 7.43 us                                                     | 7.33 us: 1.01x faster                                       |
| json_dumps                 | 5.70 ms                                                     | 5.62 ms: 1.01x faster                                       |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.52 ms: 1.01x faster                                       |
| sympy_expand               | 284 ms                                                      | 281 ms: 1.01x faster                                        |
| chaos                      | 43.3 ms                                                     | 42.9 ms: 1.01x faster                                       |
| chameleon                  | 4.98 ms                                                     | 4.94 ms: 1.01x faster                                       |
| xml_etree_process          | 37.7 ms                                                     | 37.5 ms: 1.01x faster                                       |
| raytrace                   | 192 ms                                                      | 191 ms: 1.01x faster                                        |
| regex_compile              | 87.5 ms                                                     | 87.1 ms: 1.00x faster                                       |
| deltablue                  | 2.16 ms                                                     | 2.17 ms: 1.00x slower                                       |
| logging_format             | 6.72 us                                                     | 6.75 us: 1.01x slower                                       |
| unpickle                   | 8.18 us                                                     | 8.24 us: 1.01x slower                                       |
| sqlglot_parse              | 804 us                                                      | 811 us: 1.01x slower                                        |
| logging_simple             | 6.28 us                                                     | 6.34 us: 1.01x slower                                       |
| regex_effbot               | 1.62 ms                                                     | 1.64 ms: 1.02x slower                                       |
| pickle_dict                | 18.4 us                                                     | 18.7 us: 1.02x slower                                       |
| unpickle_list              | 2.75 us                                                     | 2.82 us: 1.03x slower                                       |
| logging_silent             | 60.5 ns                                                     | 62.6 ns: 1.03x slower                                       |
| nbody                      | 71.9 ms                                                     | 74.4 ms: 1.04x slower                                       |
| pickle_list                | 2.83 us                                                     | 2.95 us: 1.04x slower                                       |
| generators                 | 22.5 ms                                                     | 23.5 ms: 1.05x slower                                       |
| pycparser                  | 699 ms                                                      | 739 ms: 1.06x slower                                        |
| Geometric mean             | (ref)                                                       | 1.03x faster                                                |

Benchmark hidden because not significant (9): mypy2, async_tree_io, django_template, sqlglot_transpile, tomli_loads, mako, sqlite_synth, pyflate, xml_etree_generate
Ignored benchmarks (1) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: unpack_sequence
Ignored benchmarks (5) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown
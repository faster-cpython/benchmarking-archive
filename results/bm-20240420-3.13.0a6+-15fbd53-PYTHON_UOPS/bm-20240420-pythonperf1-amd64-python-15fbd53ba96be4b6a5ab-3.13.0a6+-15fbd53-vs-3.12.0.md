# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x slower
- HPT reliability: 98.57%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 224 ms: 1.03x slower                                                        |
| chameleon      | 4.98 ms                                                     | 5.02 ms: 1.01x slower                                                       |
| docutils       | 1.66 sec                                                    | 1.74 sec: 1.05x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 84.1 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                       | 1.01x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 275 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 384 ms: 1.31x faster                                                        |
| async_tree_none            | 291 ms                                                      | 228 ms: 1.28x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 226 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 395 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 625 ms: 1.23x faster                                                        |
| async_tree_io              | 731 ms                                                      | 594 ms: 1.23x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 276 ms: 1.23x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.26x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 152 ms                                                      | 148 ms: 1.03x faster                                                        |
| float          | 56.8 ms                                                     | 57.9 ms: 1.02x slower                                                       |
| nbody          | 71.9 ms                                                     | 83.1 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 121 ms: 1.05x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.59 ms: 1.02x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                                       |
| regex_compile  | 87.5 ms                                                     | 103 ms: 1.18x slower                                                        |
| Geometric mean | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 195 us                                                      | 185 us: 1.06x faster                                                        |
| xml_etree_parse      | 93.0 ms                                                     | 90.0 ms: 1.03x faster                                                       |
| json_loads           | 13.9 us                                                     | 13.8 us: 1.01x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 56.5 ms: 1.01x slower                                                       |
| pickle               | 7.43 us                                                     | 7.53 us: 1.01x slower                                                       |
| xml_etree_iterparse  | 65.2 ms                                                     | 66.5 ms: 1.02x slower                                                       |
| xml_etree_process    | 37.7 ms                                                     | 38.7 ms: 1.03x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.86 us: 1.04x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.54 us: 1.04x slower                                                       |
| tomli_loads          | 1.37 sec                                                    | 1.46 sec: 1.07x slower                                                      |
| pickle_list          | 2.83 us                                                     | 3.06 us: 1.08x slower                                                       |
| unpickle_pure_python | 133 us                                                      | 166 us: 1.24x slower                                                        |
| Geometric mean       | (ref)                                                       | 1.03x slower                                                                |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 19.5 ms                                                     | 19.9 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 22.9 ms                                                     | 23.3 ms: 1.02x slower                                                       |
| mako            | 7.09 ms                                                     | 7.41 ms: 1.05x slower                                                       |
| Geometric mean  | (ref)                                                       | 1.03x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.49 sec: 1.40x faster                                                      |
| async_tree_memoization_tg  | 367 ms                                                      | 275 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 384 ms: 1.31x faster                                                        |
| async_tree_none            | 291 ms                                                      | 228 ms: 1.28x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 226 ms: 1.26x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 75.7 us: 1.26x faster                                                       |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 395 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 625 ms: 1.23x faster                                                        |
| async_tree_io              | 731 ms                                                      | 594 ms: 1.23x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 276 ms: 1.23x faster                                                        |
| mypy2                      | 509 ms                                                      | 457 ms: 1.12x faster                                                        |
| coroutines                 | 14.3 ms                                                     | 13.0 ms: 1.09x faster                                                       |
| raytrace                   | 192 ms                                                      | 176 ms: 1.09x faster                                                        |
| generators                 | 22.5 ms                                                     | 20.7 ms: 1.09x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.62 us: 1.09x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 84.1 ms: 1.06x faster                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 65.2 ms: 1.06x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 57.1 ns: 1.06x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 185 us: 1.06x faster                                                        |
| pathlib                    | 80.5 ms                                                     | 76.5 ms: 1.05x faster                                                       |
| regex_dna                  | 126 ms                                                      | 121 ms: 1.05x faster                                                        |
| logging_format             | 6.72 us                                                     | 6.45 us: 1.04x faster                                                       |
| deepcopy                   | 238 us                                                      | 229 us: 1.04x faster                                                        |
| logging_simple             | 6.28 us                                                     | 6.06 us: 1.04x faster                                                       |
| xml_etree_parse            | 93.0 ms                                                     | 90.0 ms: 1.03x faster                                                       |
| pidigits                   | 152 ms                                                      | 148 ms: 1.03x faster                                                        |
| deepcopy_reduce            | 2.09 us                                                     | 2.04 us: 1.03x faster                                                       |
| bench_thread_pool          | 857 us                                                      | 835 us: 1.03x faster                                                        |
| comprehensions             | 14.1 us                                                     | 13.8 us: 1.03x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 43.4 ms: 1.02x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.59 ms: 1.02x faster                                                       |
| json_loads                 | 13.9 us                                                     | 13.8 us: 1.01x faster                                                       |
| richards                   | 28.4 ms                                                     | 28.6 ms: 1.01x slower                                                       |
| pickle_dict                | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| chameleon                  | 4.98 ms                                                     | 5.02 ms: 1.01x slower                                                       |
| richards_super             | 32.1 ms                                                     | 32.4 ms: 1.01x slower                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 56.5 ms: 1.01x slower                                                       |
| pickle                     | 7.43 us                                                     | 7.53 us: 1.01x slower                                                       |
| django_template            | 22.9 ms                                                     | 23.3 ms: 1.02x slower                                                       |
| async_generators           | 239 ms                                                      | 243 ms: 1.02x slower                                                        |
| gc_traversal               | 1.52 ms                                                     | 1.55 ms: 1.02x slower                                                       |
| float                      | 56.8 ms                                                     | 57.9 ms: 1.02x slower                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 66.5 ms: 1.02x slower                                                       |
| python_startup             | 19.5 ms                                                     | 19.9 ms: 1.02x slower                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 1.04 ms: 1.02x slower                                                       |
| meteor_contest             | 74.6 ms                                                     | 76.4 ms: 1.02x slower                                                       |
| xml_etree_process          | 37.7 ms                                                     | 38.7 ms: 1.03x slower                                                       |
| aiohttp                    | 884 us                                                      | 907 us: 1.03x slower                                                        |
| 2to3                       | 218 ms                                                      | 224 ms: 1.03x slower                                                        |
| sqlglot_parse              | 804 us                                                      | 827 us: 1.03x slower                                                        |
| chaos                      | 43.3 ms                                                     | 44.6 ms: 1.03x slower                                                       |
| sympy_sum                  | 91.5 ms                                                     | 94.7 ms: 1.03x slower                                                       |
| sympy_str                  | 175 ms                                                      | 181 ms: 1.04x slower                                                        |
| unpickle_list              | 2.75 us                                                     | 2.86 us: 1.04x slower                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 50.5 ms: 1.04x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.54 us: 1.04x slower                                                       |
| deepcopy_memo              | 23.7 us                                                     | 24.8 us: 1.04x slower                                                       |
| mako                       | 7.09 ms                                                     | 7.41 ms: 1.05x slower                                                       |
| docutils                   | 1.66 sec                                                    | 1.74 sec: 1.05x slower                                                      |
| pprint_safe_repr           | 513 ms                                                      | 542 ms: 1.06x slower                                                        |
| pprint_pformat             | 1.05 sec                                                    | 1.11 sec: 1.06x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 36.6 ms: 1.06x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                                       |
| sympy_integrate            | 13.0 ms                                                     | 13.8 ms: 1.07x slower                                                       |
| tomli_loads                | 1.37 sec                                                    | 1.46 sec: 1.07x slower                                                      |
| pycparser                  | 699 ms                                                      | 747 ms: 1.07x slower                                                        |
| sympy_expand               | 284 ms                                                      | 304 ms: 1.07x slower                                                        |
| pickle_list                | 2.83 us                                                     | 3.06 us: 1.08x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.49 sec: 1.08x slower                                                      |
| nqueens                    | 62.8 ms                                                     | 68.6 ms: 1.09x slower                                                       |
| go                         | 91.6 ms                                                     | 102 ms: 1.11x slower                                                        |
| scimark_fft                | 184 ms                                                      | 208 ms: 1.13x slower                                                        |
| pyflate                    | 295 ms                                                      | 336 ms: 1.14x slower                                                        |
| deltablue                  | 2.16 ms                                                     | 2.49 ms: 1.15x slower                                                       |
| fannkuch                   | 247 ms                                                      | 285 ms: 1.15x slower                                                        |
| nbody                      | 71.9 ms                                                     | 83.1 ms: 1.16x slower                                                       |
| scimark_sor                | 78.8 ms                                                     | 91.1 ms: 1.16x slower                                                       |
| regex_compile              | 87.5 ms                                                     | 103 ms: 1.18x slower                                                        |
| scimark_monte_carlo        | 43.7 ms                                                     | 51.6 ms: 1.18x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 900 us: 1.20x slower                                                        |
| coverage                   | 40.8 ms                                                     | 49.1 ms: 1.20x slower                                                       |
| telco                      | 4.13 ms                                                     | 5.00 ms: 1.21x slower                                                       |
| spectral_norm              | 66.9 ms                                                     | 81.7 ms: 1.22x slower                                                       |
| unpickle_pure_python       | 133 us                                                      | 166 us: 1.24x slower                                                        |
| hexiom                     | 4.10 ms                                                     | 5.24 ms: 1.28x slower                                                       |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 3.30 ms: 1.29x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 78.3 ms: 1.33x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (5): asyncio_tcp, python_startup_no_site, json_dumps, sqlglot_normalize, json
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.57% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown
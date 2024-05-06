# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.06x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 222 ms: 1.02x slower                                                          |
| chameleon      | 4.98 ms                                                     | 4.81 ms: 1.04x faster                                                         |
| docutils       | 1.66 sec                                                    | 1.72 sec: 1.04x slower                                                        |
| tornado_http   | 89.5 ms                                                     | 83.6 ms: 1.07x faster                                                         |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 264 ms: 1.39x faster                                                          |
| async_tree_none_tg         | 285 ms                                                      | 215 ms: 1.33x faster                                                          |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 382 ms: 1.32x faster                                                          |
| async_tree_none            | 291 ms                                                      | 222 ms: 1.31x faster                                                          |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 386 ms: 1.27x faster                                                          |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.26x faster                                                          |
| async_tree_io_tg           | 771 ms                                                      | 616 ms: 1.25x faster                                                          |
| async_tree_io              | 731 ms                                                      | 588 ms: 1.24x faster                                                          |
| Geometric mean             | (ref)                                                       | 1.30x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 46.6 ms: 1.22x faster                                                         |
| nbody          | 71.9 ms                                                     | 59.0 ms: 1.22x faster                                                         |
| pidigits       | 152 ms                                                      | 147 ms: 1.04x faster                                                          |
| Geometric mean | (ref)                                                       | 1.16x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 116 ms: 1.08x faster                                                          |
| regex_effbot   | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                         |
| regex_compile  | 87.5 ms                                                     | 86.6 ms: 1.01x faster                                                         |
| regex_v8       | 14.2 ms                                                     | 14.4 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.21 sec: 1.13x faster                                                        |
| pickle_pure_python   | 195 us                                                      | 173 us: 1.13x faster                                                          |
| xml_etree_iterparse  | 65.2 ms                                                     | 61.3 ms: 1.06x faster                                                         |
| xml_etree_generate   | 55.8 ms                                                     | 53.1 ms: 1.05x faster                                                         |
| unpickle_pure_python | 133 us                                                      | 129 us: 1.04x faster                                                          |
| xml_etree_process    | 37.7 ms                                                     | 36.6 ms: 1.03x faster                                                         |
| json_dumps           | 5.70 ms                                                     | 5.53 ms: 1.03x faster                                                         |
| xml_etree_parse      | 93.0 ms                                                     | 90.3 ms: 1.03x faster                                                         |
| json_loads           | 13.9 us                                                     | 13.6 us: 1.02x faster                                                         |
| pickle               | 7.43 us                                                     | 7.29 us: 1.02x faster                                                         |
| pickle_dict          | 18.4 us                                                     | 18.5 us: 1.01x slower                                                         |
| unpickle_list        | 2.75 us                                                     | 2.82 us: 1.03x slower                                                         |
| unpickle             | 8.18 us                                                     | 8.55 us: 1.04x slower                                                         |
| pickle_list          | 2.83 us                                                     | 3.16 us: 1.12x slower                                                         |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 21.9 ms: 1.12x slower                                                         |
| python_startup_no_site | 16.2 ms                                                     | 19.7 ms: 1.21x slower                                                         |
| Geometric mean         | (ref)                                                       | 1.17x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-----------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 5.64 ms: 1.26x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.49 sec: 1.41x faster                                                        |
| async_tree_memoization_tg  | 367 ms                                                      | 264 ms: 1.39x faster                                                          |
| async_tree_none_tg         | 285 ms                                                      | 215 ms: 1.33x faster                                                          |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 382 ms: 1.32x faster                                                          |
| async_tree_none            | 291 ms                                                      | 222 ms: 1.31x faster                                                          |
| spectral_norm              | 66.9 ms                                                     | 51.9 ms: 1.29x faster                                                         |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 386 ms: 1.27x faster                                                          |
| typing_runtime_protocols   | 95.1 us                                                     | 75.2 us: 1.26x faster                                                         |
| async_tree_memoization     | 339 ms                                                      | 268 ms: 1.26x faster                                                          |
| mako                       | 7.09 ms                                                     | 5.64 ms: 1.26x faster                                                         |
| async_tree_io_tg           | 771 ms                                                      | 616 ms: 1.25x faster                                                          |
| comprehensions             | 14.1 us                                                     | 11.3 us: 1.25x faster                                                         |
| async_tree_io              | 731 ms                                                      | 588 ms: 1.24x faster                                                          |
| float                      | 56.8 ms                                                     | 46.6 ms: 1.22x faster                                                         |
| nbody                      | 71.9 ms                                                     | 59.0 ms: 1.22x faster                                                         |
| generators                 | 22.5 ms                                                     | 19.3 ms: 1.17x faster                                                         |
| raytrace                   | 192 ms                                                      | 167 ms: 1.15x faster                                                          |
| logging_silent             | 60.5 ns                                                     | 53.1 ns: 1.14x faster                                                         |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.26 ms: 1.13x faster                                                         |
| tomli_loads                | 1.37 sec                                                    | 1.21 sec: 1.13x faster                                                        |
| pickle_pure_python         | 195 us                                                      | 173 us: 1.13x faster                                                          |
| sqlite_synth               | 1.76 us                                                     | 1.56 us: 1.13x faster                                                         |
| coroutines                 | 14.3 ms                                                     | 12.9 ms: 1.10x faster                                                         |
| scimark_fft                | 184 ms                                                      | 167 ms: 1.10x faster                                                          |
| scimark_monte_carlo        | 43.7 ms                                                     | 39.7 ms: 1.10x faster                                                         |
| pprint_pformat             | 1.05 sec                                                    | 952 ms: 1.10x faster                                                          |
| pyflate                    | 295 ms                                                      | 270 ms: 1.09x faster                                                          |
| mypy2                      | 509 ms                                                      | 467 ms: 1.09x faster                                                          |
| pprint_safe_repr           | 513 ms                                                      | 471 ms: 1.09x faster                                                          |
| crypto_pyaes               | 48.5 ms                                                     | 44.5 ms: 1.09x faster                                                         |
| regex_dna                  | 126 ms                                                      | 116 ms: 1.08x faster                                                          |
| chaos                      | 43.3 ms                                                     | 40.0 ms: 1.08x faster                                                         |
| deepcopy_memo              | 23.7 us                                                     | 21.9 us: 1.08x faster                                                         |
| fannkuch                   | 247 ms                                                      | 230 ms: 1.07x faster                                                          |
| dulwich_log                | 44.3 ms                                                     | 41.2 ms: 1.07x faster                                                         |
| richards_super             | 32.1 ms                                                     | 29.9 ms: 1.07x faster                                                         |
| richards                   | 28.4 ms                                                     | 26.5 ms: 1.07x faster                                                         |
| logging_format             | 6.72 us                                                     | 6.27 us: 1.07x faster                                                         |
| tornado_http               | 89.5 ms                                                     | 83.6 ms: 1.07x faster                                                         |
| logging_simple             | 6.28 us                                                     | 5.86 us: 1.07x faster                                                         |
| bench_thread_pool          | 857 us                                                      | 803 us: 1.07x faster                                                          |
| xml_etree_iterparse        | 65.2 ms                                                     | 61.3 ms: 1.06x faster                                                         |
| deepcopy_reduce            | 2.09 us                                                     | 1.97 us: 1.06x faster                                                         |
| json                       | 3.05 ms                                                     | 2.89 ms: 1.06x faster                                                         |
| xml_etree_generate         | 55.8 ms                                                     | 53.1 ms: 1.05x faster                                                         |
| deepcopy                   | 238 us                                                      | 229 us: 1.04x faster                                                          |
| regex_effbot               | 1.62 ms                                                     | 1.56 ms: 1.04x faster                                                         |
| sqlglot_parse              | 804 us                                                      | 774 us: 1.04x faster                                                          |
| pidigits                   | 152 ms                                                      | 147 ms: 1.04x faster                                                          |
| chameleon                  | 4.98 ms                                                     | 4.81 ms: 1.04x faster                                                         |
| unpickle_pure_python       | 133 us                                                      | 129 us: 1.04x faster                                                          |
| pathlib                    | 80.5 ms                                                     | 77.9 ms: 1.03x faster                                                         |
| pycparser                  | 699 ms                                                      | 677 ms: 1.03x faster                                                          |
| xml_etree_process          | 37.7 ms                                                     | 36.6 ms: 1.03x faster                                                         |
| json_dumps                 | 5.70 ms                                                     | 5.53 ms: 1.03x faster                                                         |
| xml_etree_parse            | 93.0 ms                                                     | 90.3 ms: 1.03x faster                                                         |
| sqlglot_transpile          | 1.02 ms                                                     | 997 us: 1.02x faster                                                          |
| json_loads                 | 13.9 us                                                     | 13.6 us: 1.02x faster                                                         |
| bench_mp_pool              | 69.2 ms                                                     | 67.7 ms: 1.02x faster                                                         |
| pickle                     | 7.43 us                                                     | 7.29 us: 1.02x faster                                                         |
| sympy_str                  | 175 ms                                                      | 172 ms: 1.02x faster                                                          |
| go                         | 91.6 ms                                                     | 89.9 ms: 1.02x faster                                                         |
| regex_compile              | 87.5 ms                                                     | 86.6 ms: 1.01x faster                                                         |
| sqlglot_normalize          | 187 ms                                                      | 186 ms: 1.01x faster                                                          |
| deltablue                  | 2.16 ms                                                     | 2.15 ms: 1.01x faster                                                         |
| sympy_sum                  | 91.5 ms                                                     | 90.9 ms: 1.01x faster                                                         |
| pickle_dict                | 18.4 us                                                     | 18.5 us: 1.01x slower                                                         |
| nqueens                    | 62.8 ms                                                     | 63.3 ms: 1.01x slower                                                         |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                         |
| regex_v8                   | 14.2 ms                                                     | 14.4 ms: 1.01x slower                                                         |
| async_generators           | 239 ms                                                      | 243 ms: 1.02x slower                                                          |
| 2to3                       | 218 ms                                                      | 222 ms: 1.02x slower                                                          |
| meteor_contest             | 74.6 ms                                                     | 76.1 ms: 1.02x slower                                                         |
| scimark_sor                | 78.8 ms                                                     | 80.9 ms: 1.03x slower                                                         |
| unpickle_list              | 2.75 us                                                     | 2.82 us: 1.03x slower                                                         |
| aiohttp                    | 884 us                                                      | 911 us: 1.03x slower                                                          |
| sympy_expand               | 284 ms                                                      | 293 ms: 1.03x slower                                                          |
| docutils                   | 1.66 sec                                                    | 1.72 sec: 1.04x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 36.0 ms: 1.04x slower                                                         |
| unpickle                   | 8.18 us                                                     | 8.55 us: 1.04x slower                                                         |
| sympy_integrate            | 13.0 ms                                                     | 13.8 ms: 1.06x slower                                                         |
| mdp                        | 1.37 sec                                                    | 1.53 sec: 1.12x slower                                                        |
| pickle_list                | 2.83 us                                                     | 3.16 us: 1.12x slower                                                         |
| python_startup             | 19.5 ms                                                     | 21.9 ms: 1.12x slower                                                         |
| telco                      | 4.13 ms                                                     | 4.76 ms: 1.15x slower                                                         |
| coverage                   | 40.8 ms                                                     | 47.5 ms: 1.16x slower                                                         |
| hexiom                     | 4.10 ms                                                     | 4.81 ms: 1.17x slower                                                         |
| create_gc_cycles           | 752 us                                                      | 891 us: 1.18x slower                                                          |
| scimark_lu                 | 58.9 ms                                                     | 70.7 ms: 1.20x slower                                                         |
| python_startup_no_site     | 16.2 ms                                                     | 19.7 ms: 1.21x slower                                                         |
| Geometric mean             | (ref)                                                       | 1.06x faster                                                                  |

Benchmark hidden because not significant (1): asyncio_tcp
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown
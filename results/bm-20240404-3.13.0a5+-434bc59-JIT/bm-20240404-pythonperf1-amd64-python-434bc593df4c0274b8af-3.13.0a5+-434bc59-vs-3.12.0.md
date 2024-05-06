# Results vs. 3.12.0

- fork: python
- ref: 434bc593df4c0274b8af
- machine: windows-amd64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 4.98 ms                                                     | 4.69 ms: 1.06x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.69 sec: 1.01x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 82.8 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 262 ms: 1.40x faster                                                        |
| async_tree_none            | 291 ms                                                      | 217 ms: 1.35x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 212 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 381 ms: 1.32x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 266 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 605 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 384 ms: 1.27x faster                                                        |
| async_tree_io              | 731 ms                                                      | 581 ms: 1.26x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.31x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 57.0 ms: 1.26x faster                                                       |
| float          | 56.8 ms                                                     | 46.7 ms: 1.22x faster                                                       |
| pidigits       | 152 ms                                                      | 146 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.17x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 119 ms: 1.06x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                       |
| regex_compile  | 87.5 ms                                                     | 86.5 ms: 1.01x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.17 sec: 1.17x faster                                                      |
| pickle_pure_python   | 195 us                                                      | 172 us: 1.13x faster                                                        |
| xml_etree_iterparse  | 65.2 ms                                                     | 59.7 ms: 1.09x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 52.4 ms: 1.07x faster                                                       |
| xml_etree_process    | 37.7 ms                                                     | 36.2 ms: 1.04x faster                                                       |
| xml_etree_parse      | 93.0 ms                                                     | 89.5 ms: 1.04x faster                                                       |
| unpickle_pure_python | 133 us                                                      | 129 us: 1.03x faster                                                        |
| json_dumps           | 5.70 ms                                                     | 5.58 ms: 1.02x faster                                                       |
| json_loads           | 13.9 us                                                     | 13.7 us: 1.02x faster                                                       |
| pickle               | 7.43 us                                                     | 7.33 us: 1.01x faster                                                       |
| pickle_dict          | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| pickle_list          | 2.83 us                                                     | 2.89 us: 1.02x slower                                                       |
| unpickle             | 8.18 us                                                     | 8.66 us: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 21.9 ms: 1.13x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 19.7 ms: 1.21x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.17x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|-----------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 5.73 ms: 1.24x faster                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.47 sec: 1.42x faster                                                      |
| async_tree_memoization_tg  | 367 ms                                                      | 262 ms: 1.40x faster                                                        |
| async_tree_none            | 291 ms                                                      | 217 ms: 1.35x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 212 ms: 1.35x faster                                                        |
| typing_runtime_protocols   | 95.1 us                                                     | 71.8 us: 1.33x faster                                                       |
| spectral_norm              | 66.9 ms                                                     | 50.7 ms: 1.32x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 381 ms: 1.32x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 266 ms: 1.28x faster                                                        |
| comprehensions             | 14.1 us                                                     | 11.1 us: 1.28x faster                                                       |
| async_tree_io_tg           | 771 ms                                                      | 605 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 384 ms: 1.27x faster                                                        |
| nbody                      | 71.9 ms                                                     | 57.0 ms: 1.26x faster                                                       |
| async_tree_io              | 731 ms                                                      | 581 ms: 1.26x faster                                                        |
| mako                       | 7.09 ms                                                     | 5.73 ms: 1.24x faster                                                       |
| float                      | 56.8 ms                                                     | 46.7 ms: 1.22x faster                                                       |
| raytrace                   | 192 ms                                                      | 164 ms: 1.17x faster                                                        |
| tomli_loads                | 1.37 sec                                                    | 1.17 sec: 1.17x faster                                                      |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.22 ms: 1.15x faster                                                       |
| generators                 | 22.5 ms                                                     | 19.6 ms: 1.15x faster                                                       |
| mypy2                      | 509 ms                                                      | 446 ms: 1.14x faster                                                        |
| pickle_pure_python         | 195 us                                                      | 172 us: 1.13x faster                                                        |
| logging_silent             | 60.5 ns                                                     | 53.4 ns: 1.13x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 21.0 us: 1.13x faster                                                       |
| chaos                      | 43.3 ms                                                     | 38.3 ms: 1.13x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.57 us: 1.12x faster                                                       |
| scimark_monte_carlo        | 43.7 ms                                                     | 39.0 ms: 1.12x faster                                                       |
| pprint_pformat             | 1.05 sec                                                    | 942 ms: 1.11x faster                                                        |
| scimark_fft                | 184 ms                                                      | 166 ms: 1.11x faster                                                        |
| pprint_safe_repr           | 513 ms                                                      | 463 ms: 1.11x faster                                                        |
| logging_simple             | 6.28 us                                                     | 5.68 us: 1.10x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.10 us: 1.10x faster                                                       |
| coroutines                 | 14.3 ms                                                     | 13.0 ms: 1.10x faster                                                       |
| xml_etree_iterparse        | 65.2 ms                                                     | 59.7 ms: 1.09x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 44.5 ms: 1.09x faster                                                       |
| pyflate                    | 295 ms                                                      | 271 ms: 1.09x faster                                                        |
| deepcopy                   | 238 us                                                      | 219 us: 1.09x faster                                                        |
| dulwich_log                | 44.3 ms                                                     | 40.9 ms: 1.08x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 82.8 ms: 1.08x faster                                                       |
| deepcopy_reduce            | 2.09 us                                                     | 1.95 us: 1.08x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 52.4 ms: 1.07x faster                                                       |
| json                       | 3.05 ms                                                     | 2.86 ms: 1.07x faster                                                       |
| richards                   | 28.4 ms                                                     | 26.7 ms: 1.06x faster                                                       |
| chameleon                  | 4.98 ms                                                     | 4.69 ms: 1.06x faster                                                       |
| richards_super             | 32.1 ms                                                     | 30.2 ms: 1.06x faster                                                       |
| regex_dna                  | 126 ms                                                      | 119 ms: 1.06x faster                                                        |
| bench_thread_pool          | 857 us                                                      | 808 us: 1.06x faster                                                        |
| sympy_str                  | 175 ms                                                      | 166 ms: 1.05x faster                                                        |
| fannkuch                   | 247 ms                                                      | 234 ms: 1.05x faster                                                        |
| sqlglot_normalize          | 187 ms                                                      | 178 ms: 1.05x faster                                                        |
| sqlglot_parse              | 804 us                                                      | 769 us: 1.05x faster                                                        |
| sympy_sum                  | 91.5 ms                                                     | 87.7 ms: 1.04x faster                                                       |
| xml_etree_process          | 37.7 ms                                                     | 36.2 ms: 1.04x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 71.5 ms: 1.04x faster                                                       |
| pidigits                   | 152 ms                                                      | 146 ms: 1.04x faster                                                        |
| xml_etree_parse            | 93.0 ms                                                     | 89.5 ms: 1.04x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 985 us: 1.04x faster                                                        |
| pathlib                    | 80.5 ms                                                     | 77.6 ms: 1.04x faster                                                       |
| unpickle_pure_python       | 133 us                                                      | 129 us: 1.03x faster                                                        |
| nqueens                    | 62.8 ms                                                     | 61.0 ms: 1.03x faster                                                       |
| regex_effbot               | 1.62 ms                                                     | 1.57 ms: 1.03x faster                                                       |
| async_generators           | 239 ms                                                      | 234 ms: 1.02x faster                                                        |
| bench_mp_pool              | 69.2 ms                                                     | 67.7 ms: 1.02x faster                                                       |
| json_dumps                 | 5.70 ms                                                     | 5.58 ms: 1.02x faster                                                       |
| json_loads                 | 13.9 us                                                     | 13.7 us: 1.02x faster                                                       |
| pickle                     | 7.43 us                                                     | 7.33 us: 1.01x faster                                                       |
| regex_compile              | 87.5 ms                                                     | 86.5 ms: 1.01x faster                                                       |
| deltablue                  | 2.16 ms                                                     | 2.14 ms: 1.01x faster                                                       |
| go                         | 91.6 ms                                                     | 92.1 ms: 1.01x slower                                                       |
| pickle_dict                | 18.4 us                                                     | 18.6 us: 1.01x slower                                                       |
| aiohttp                    | 884 us                                                      | 893 us: 1.01x slower                                                        |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                       |
| docutils                   | 1.66 sec                                                    | 1.69 sec: 1.01x slower                                                      |
| scimark_sor                | 78.8 ms                                                     | 80.0 ms: 1.02x slower                                                       |
| sympy_integrate            | 13.0 ms                                                     | 13.2 ms: 1.02x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.89 us: 1.02x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                       |
| unpickle                   | 8.18 us                                                     | 8.66 us: 1.06x slower                                                       |
| hexiom                     | 4.10 ms                                                     | 4.41 ms: 1.07x slower                                                       |
| python_startup             | 19.5 ms                                                     | 21.9 ms: 1.13x slower                                                       |
| coverage                   | 40.8 ms                                                     | 46.7 ms: 1.14x slower                                                       |
| telco                      | 4.13 ms                                                     | 4.80 ms: 1.16x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 69.5 ms: 1.18x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 904 us: 1.20x slower                                                        |
| python_startup_no_site     | 16.2 ms                                                     | 19.7 ms: 1.21x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                                |

Benchmark hidden because not significant (7): asyncio_tcp, pycparser, sqlglot_optimize, sympy_expand, 2to3, mdp, unpickle_list
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-434bc59-JIT/bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown
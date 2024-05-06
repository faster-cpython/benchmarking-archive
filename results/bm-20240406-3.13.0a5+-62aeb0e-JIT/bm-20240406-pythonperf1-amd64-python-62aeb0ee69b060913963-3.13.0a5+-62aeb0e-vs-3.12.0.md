# Results vs. 3.12.0

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 221 ms: 1.01x slower                                                        |
| chameleon      | 4.98 ms                                                     | 4.70 ms: 1.06x faster                                                       |
| docutils       | 1.66 sec                                                    | 1.70 sec: 1.02x slower                                                      |
| tornado_http   | 89.5 ms                                                     | 83.6 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 262 ms: 1.40x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 212 ms: 1.35x faster                                                        |
| async_tree_none            | 291 ms                                                      | 217 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| async_tree_memoization     | 339 ms                                                      | 265 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 605 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 387 ms: 1.26x faster                                                        |
| async_tree_io              | 731 ms                                                      | 582 ms: 1.26x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.31x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 71.9 ms                                                     | 57.8 ms: 1.24x faster                                                       |
| float          | 56.8 ms                                                     | 46.8 ms: 1.21x faster                                                       |
| pidigits       | 152 ms                                                      | 146 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.16x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 119 ms: 1.06x faster                                                        |
| regex_effbot   | 1.62 ms                                                     | 1.55 ms: 1.04x faster                                                       |
| regex_v8       | 14.2 ms                                                     | 14.1 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.19 sec: 1.15x faster                                                      |
| pickle_pure_python   | 195 us                                                      | 172 us: 1.14x faster                                                        |
| xml_etree_iterparse  | 65.2 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| xml_etree_generate   | 55.8 ms                                                     | 53.1 ms: 1.05x faster                                                       |
| unpickle_pure_python | 133 us                                                      | 129 us: 1.03x faster                                                        |
| xml_etree_process    | 37.7 ms                                                     | 36.6 ms: 1.03x faster                                                       |
| json_dumps           | 5.70 ms                                                     | 5.54 ms: 1.03x faster                                                       |
| xml_etree_parse      | 93.0 ms                                                     | 90.9 ms: 1.02x faster                                                       |
| json_loads           | 13.9 us                                                     | 13.7 us: 1.02x faster                                                       |
| pickle               | 7.43 us                                                     | 7.39 us: 1.01x faster                                                       |
| pickle_list          | 2.83 us                                                     | 2.85 us: 1.01x slower                                                       |
| pickle_dict          | 18.4 us                                                     | 19.0 us: 1.03x slower                                                       |
| unpickle_list        | 2.75 us                                                     | 2.90 us: 1.06x slower                                                       |
| unpickle             | 8.18 us                                                     | 9.09 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.5 ms                                                     | 22.2 ms: 1.14x slower                                                       |
| python_startup_no_site | 16.2 ms                                                     | 20.2 ms: 1.24x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.19x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|-----------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako      | 7.09 ms                                                     | 5.63 ms: 1.26x faster                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 262 ms: 1.40x faster                                                        |
| async_tree_none_tg         | 285 ms                                                      | 212 ms: 1.35x faster                                                        |
| async_tree_none            | 291 ms                                                      | 217 ms: 1.34x faster                                                        |
| spectral_norm              | 66.9 ms                                                     | 50.4 ms: 1.33x faster                                                       |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.58 sec: 1.32x faster                                                      |
| typing_runtime_protocols   | 95.1 us                                                     | 72.5 us: 1.31x faster                                                       |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 383 ms: 1.31x faster                                                        |
| comprehensions             | 14.1 us                                                     | 10.9 us: 1.30x faster                                                       |
| async_tree_memoization     | 339 ms                                                      | 265 ms: 1.28x faster                                                        |
| async_tree_io_tg           | 771 ms                                                      | 605 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 387 ms: 1.26x faster                                                        |
| mako                       | 7.09 ms                                                     | 5.63 ms: 1.26x faster                                                       |
| async_tree_io              | 731 ms                                                      | 582 ms: 1.26x faster                                                        |
| nbody                      | 71.9 ms                                                     | 57.8 ms: 1.24x faster                                                       |
| float                      | 56.8 ms                                                     | 46.8 ms: 1.21x faster                                                       |
| raytrace                   | 192 ms                                                      | 164 ms: 1.17x faster                                                        |
| tomli_loads                | 1.37 sec                                                    | 1.19 sec: 1.15x faster                                                      |
| generators                 | 22.5 ms                                                     | 19.6 ms: 1.15x faster                                                       |
| pickle_pure_python         | 195 us                                                      | 172 us: 1.14x faster                                                        |
| mypy2                      | 509 ms                                                      | 449 ms: 1.14x faster                                                        |
| scimark_monte_carlo        | 43.7 ms                                                     | 38.7 ms: 1.13x faster                                                       |
| logging_silent             | 60.5 ns                                                     | 53.6 ns: 1.13x faster                                                       |
| deepcopy_memo              | 23.7 us                                                     | 21.0 us: 1.13x faster                                                       |
| chaos                      | 43.3 ms                                                     | 38.5 ms: 1.13x faster                                                       |
| crypto_pyaes               | 48.5 ms                                                     | 43.6 ms: 1.11x faster                                                       |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.30 ms: 1.11x faster                                                       |
| sqlite_synth               | 1.76 us                                                     | 1.59 us: 1.10x faster                                                       |
| logging_format             | 6.72 us                                                     | 6.11 us: 1.10x faster                                                       |
| pyflate                    | 295 ms                                                      | 268 ms: 1.10x faster                                                        |
| logging_simple             | 6.28 us                                                     | 5.72 us: 1.10x faster                                                       |
| coroutines                 | 14.3 ms                                                     | 13.0 ms: 1.10x faster                                                       |
| dulwich_log                | 44.3 ms                                                     | 40.4 ms: 1.10x faster                                                       |
| scimark_fft                | 184 ms                                                      | 169 ms: 1.09x faster                                                        |
| deepcopy                   | 238 us                                                      | 219 us: 1.09x faster                                                        |
| bench_thread_pool          | 857 us                                                      | 795 us: 1.08x faster                                                        |
| xml_etree_iterparse        | 65.2 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| deepcopy_reduce            | 2.09 us                                                     | 1.95 us: 1.07x faster                                                       |
| richards                   | 28.4 ms                                                     | 26.5 ms: 1.07x faster                                                       |
| tornado_http               | 89.5 ms                                                     | 83.6 ms: 1.07x faster                                                       |
| pprint_pformat             | 1.05 sec                                                    | 979 ms: 1.07x faster                                                        |
| fannkuch                   | 247 ms                                                      | 231 ms: 1.07x faster                                                        |
| pprint_safe_repr           | 513 ms                                                      | 481 ms: 1.07x faster                                                        |
| richards_super             | 32.1 ms                                                     | 30.1 ms: 1.07x faster                                                       |
| regex_dna                  | 126 ms                                                      | 119 ms: 1.06x faster                                                        |
| chameleon                  | 4.98 ms                                                     | 4.70 ms: 1.06x faster                                                       |
| json                       | 3.05 ms                                                     | 2.89 ms: 1.06x faster                                                       |
| xml_etree_generate         | 55.8 ms                                                     | 53.1 ms: 1.05x faster                                                       |
| pathlib                    | 80.5 ms                                                     | 76.8 ms: 1.05x faster                                                       |
| sympy_str                  | 175 ms                                                      | 168 ms: 1.04x faster                                                        |
| sqlglot_normalize          | 187 ms                                                      | 180 ms: 1.04x faster                                                        |
| regex_effbot               | 1.62 ms                                                     | 1.55 ms: 1.04x faster                                                       |
| pidigits                   | 152 ms                                                      | 146 ms: 1.04x faster                                                        |
| sympy_sum                  | 91.5 ms                                                     | 88.0 ms: 1.04x faster                                                       |
| unpickle_pure_python       | 133 us                                                      | 129 us: 1.03x faster                                                        |
| xml_etree_process          | 37.7 ms                                                     | 36.6 ms: 1.03x faster                                                       |
| meteor_contest             | 74.6 ms                                                     | 72.5 ms: 1.03x faster                                                       |
| sqlglot_transpile          | 1.02 ms                                                     | 994 us: 1.03x faster                                                        |
| json_dumps                 | 5.70 ms                                                     | 5.54 ms: 1.03x faster                                                       |
| sqlglot_parse              | 804 us                                                      | 785 us: 1.02x faster                                                        |
| xml_etree_parse            | 93.0 ms                                                     | 90.9 ms: 1.02x faster                                                       |
| nqueens                    | 62.8 ms                                                     | 61.5 ms: 1.02x faster                                                       |
| async_generators           | 239 ms                                                      | 235 ms: 1.02x faster                                                        |
| json_loads                 | 13.9 us                                                     | 13.7 us: 1.02x faster                                                       |
| regex_v8                   | 14.2 ms                                                     | 14.1 ms: 1.01x faster                                                       |
| pickle                     | 7.43 us                                                     | 7.39 us: 1.01x faster                                                       |
| sympy_expand               | 284 ms                                                      | 285 ms: 1.00x slower                                                        |
| go                         | 91.6 ms                                                     | 92.0 ms: 1.01x slower                                                       |
| pickle_list                | 2.83 us                                                     | 2.85 us: 1.01x slower                                                       |
| bench_mp_pool              | 69.2 ms                                                     | 69.9 ms: 1.01x slower                                                       |
| gc_traversal               | 1.52 ms                                                     | 1.54 ms: 1.01x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 35.0 ms: 1.01x slower                                                       |
| 2to3                       | 218 ms                                                      | 221 ms: 1.01x slower                                                        |
| aiohttp                    | 884 us                                                      | 900 us: 1.02x slower                                                        |
| docutils                   | 1.66 sec                                                    | 1.70 sec: 1.02x slower                                                      |
| sympy_integrate            | 13.0 ms                                                     | 13.3 ms: 1.03x slower                                                       |
| pickle_dict                | 18.4 us                                                     | 19.0 us: 1.03x slower                                                       |
| unpickle_list              | 2.75 us                                                     | 2.90 us: 1.06x slower                                                       |
| scimark_sor                | 78.8 ms                                                     | 83.4 ms: 1.06x slower                                                       |
| mdp                        | 1.37 sec                                                    | 1.47 sec: 1.07x slower                                                      |
| hexiom                     | 4.10 ms                                                     | 4.45 ms: 1.09x slower                                                       |
| unpickle                   | 8.18 us                                                     | 9.09 us: 1.11x slower                                                       |
| python_startup             | 19.5 ms                                                     | 22.2 ms: 1.14x slower                                                       |
| telco                      | 4.13 ms                                                     | 4.74 ms: 1.15x slower                                                       |
| coverage                   | 40.8 ms                                                     | 47.2 ms: 1.16x slower                                                       |
| create_gc_cycles           | 752 us                                                      | 900 us: 1.20x slower                                                        |
| python_startup_no_site     | 16.2 ms                                                     | 20.2 ms: 1.24x slower                                                       |
| scimark_lu                 | 58.9 ms                                                     | 73.2 ms: 1.24x slower                                                       |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                                |

Benchmark hidden because not significant (4): pycparser, asyncio_tcp, deltablue, regex_compile
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown
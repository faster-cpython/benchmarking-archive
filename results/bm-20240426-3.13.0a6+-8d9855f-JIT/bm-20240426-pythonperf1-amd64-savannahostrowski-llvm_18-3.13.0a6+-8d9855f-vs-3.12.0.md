# Results vs. 3.12.0

- fork: savannahostrowski
- ref: llvm_18
- machine: windows-amd64
- commit hash: 8d9855f
- commit date: 2024-04-26
- overall geometric mean: 1.04x faster
- HPT reliability: 99.85%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                      | 228 ms: 1.05x slower                                                      |
| chameleon      | 4.98 ms                                                     | 4.77 ms: 1.04x faster                                                     |
| docutils       | 1.66 sec                                                    | 1.72 sec: 1.04x slower                                                    |
| tornado_http   | 89.5 ms                                                     | 93.0 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                       | 1.02x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 271 ms: 1.36x faster                                                      |
| async_tree_none_tg         | 285 ms                                                      | 217 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 385 ms: 1.30x faster                                                      |
| async_tree_none            | 291 ms                                                      | 224 ms: 1.30x faster                                                      |
| async_tree_memoization     | 339 ms                                                      | 272 ms: 1.25x faster                                                      |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 396 ms: 1.23x faster                                                      |
| async_tree_io_tg           | 771 ms                                                      | 625 ms: 1.23x faster                                                      |
| async_tree_io              | 731 ms                                                      | 599 ms: 1.22x faster                                                      |
| Geometric mean             | (ref)                                                       | 1.28x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 56.8 ms                                                     | 45.9 ms: 1.24x faster                                                     |
| nbody          | 71.9 ms                                                     | 62.4 ms: 1.15x faster                                                     |
| pidigits       | 152 ms                                                      | 148 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                       | 1.14x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 126 ms                                                      | 120 ms: 1.05x faster                                                      |
| regex_effbot   | 1.62 ms                                                     | 1.60 ms: 1.01x faster                                                     |
| regex_v8       | 14.2 ms                                                     | 15.6 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                       | 1.01x slower                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 1.37 sec                                                    | 1.18 sec: 1.16x faster                                                    |
| pickle_pure_python   | 195 us                                                      | 173 us: 1.13x faster                                                      |
| unpickle_pure_python | 133 us                                                      | 123 us: 1.08x faster                                                      |
| xml_etree_iterparse  | 65.2 ms                                                     | 61.6 ms: 1.06x faster                                                     |
| xml_etree_generate   | 55.8 ms                                                     | 54.3 ms: 1.03x faster                                                     |
| xml_etree_process    | 37.7 ms                                                     | 36.8 ms: 1.02x faster                                                     |
| xml_etree_parse      | 93.0 ms                                                     | 92.3 ms: 1.01x faster                                                     |
| pickle               | 7.43 us                                                     | 7.39 us: 1.01x faster                                                     |
| unpickle_list        | 2.75 us                                                     | 2.79 us: 1.02x slower                                                     |
| pickle_dict          | 18.4 us                                                     | 18.7 us: 1.02x slower                                                     |
| json_loads           | 13.9 us                                                     | 14.3 us: 1.03x slower                                                     |
| unpickle             | 8.18 us                                                     | 8.56 us: 1.05x slower                                                     |
| pickle_list          | 2.83 us                                                     | 3.12 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                              |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                     | 18.5 ms: 1.14x slower                                                     |
| python_startup         | 19.5 ms                                                     | 22.4 ms: 1.15x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.14x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako           | 7.09 ms                                                     | 5.34 ms: 1.33x faster                                                     |
| Geometric mean | (ref)                                                       | 1.15x faster                                                              |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 367 ms                                                      | 271 ms: 1.36x faster                                                      |
| spectral_norm              | 66.9 ms                                                     | 50.4 ms: 1.33x faster                                                     |
| mako                       | 7.09 ms                                                     | 5.34 ms: 1.33x faster                                                     |
| comprehensions             | 14.1 us                                                     | 10.7 us: 1.32x faster                                                     |
| async_tree_none_tg         | 285 ms                                                      | 217 ms: 1.32x faster                                                      |
| async_tree_cpu_io_mixed_tg | 502 ms                                                      | 385 ms: 1.30x faster                                                      |
| async_tree_none            | 291 ms                                                      | 224 ms: 1.30x faster                                                      |
| async_tree_memoization     | 339 ms                                                      | 272 ms: 1.25x faster                                                      |
| float                      | 56.8 ms                                                     | 45.9 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 489 ms                                                      | 396 ms: 1.23x faster                                                      |
| async_tree_io_tg           | 771 ms                                                      | 625 ms: 1.23x faster                                                      |
| async_tree_io              | 731 ms                                                      | 599 ms: 1.22x faster                                                      |
| asyncio_tcp_ssl            | 2.10 sec                                                    | 1.76 sec: 1.19x faster                                                    |
| pprint_safe_repr           | 513 ms                                                      | 440 ms: 1.17x faster                                                      |
| tomli_loads                | 1.37 sec                                                    | 1.18 sec: 1.16x faster                                                    |
| pprint_pformat             | 1.05 sec                                                    | 905 ms: 1.16x faster                                                      |
| nbody                      | 71.9 ms                                                     | 62.4 ms: 1.15x faster                                                     |
| raytrace                   | 192 ms                                                      | 167 ms: 1.15x faster                                                      |
| scimark_sparse_mat_mult    | 2.56 ms                                                     | 2.22 ms: 1.15x faster                                                     |
| scimark_monte_carlo        | 43.7 ms                                                     | 38.2 ms: 1.15x faster                                                     |
| logging_silent             | 60.5 ns                                                     | 53.4 ns: 1.13x faster                                                     |
| pickle_pure_python         | 195 us                                                      | 173 us: 1.13x faster                                                      |
| coroutines                 | 14.3 ms                                                     | 12.8 ms: 1.12x faster                                                     |
| generators                 | 22.5 ms                                                     | 20.3 ms: 1.11x faster                                                     |
| scimark_fft                | 184 ms                                                      | 167 ms: 1.10x faster                                                      |
| pyflate                    | 295 ms                                                      | 268 ms: 1.10x faster                                                      |
| crypto_pyaes               | 48.5 ms                                                     | 44.3 ms: 1.10x faster                                                     |
| sqlite_synth               | 1.76 us                                                     | 1.63 us: 1.08x faster                                                     |
| mypy2                      | 509 ms                                                      | 471 ms: 1.08x faster                                                      |
| deepcopy_reduce            | 2.09 us                                                     | 1.94 us: 1.08x faster                                                     |
| unpickle_pure_python       | 133 us                                                      | 123 us: 1.08x faster                                                      |
| deepcopy_memo              | 23.7 us                                                     | 22.0 us: 1.08x faster                                                     |
| dulwich_log                | 44.3 ms                                                     | 41.2 ms: 1.08x faster                                                     |
| chaos                      | 43.3 ms                                                     | 40.4 ms: 1.07x faster                                                     |
| fannkuch                   | 247 ms                                                      | 231 ms: 1.07x faster                                                      |
| richards_super             | 32.1 ms                                                     | 30.2 ms: 1.06x faster                                                     |
| logging_simple             | 6.28 us                                                     | 5.91 us: 1.06x faster                                                     |
| logging_format             | 6.72 us                                                     | 6.34 us: 1.06x faster                                                     |
| xml_etree_iterparse        | 65.2 ms                                                     | 61.6 ms: 1.06x faster                                                     |
| deepcopy                   | 238 us                                                      | 226 us: 1.05x faster                                                      |
| regex_dna                  | 126 ms                                                      | 120 ms: 1.05x faster                                                      |
| richards                   | 28.4 ms                                                     | 27.1 ms: 1.05x faster                                                     |
| sqlglot_parse              | 804 us                                                      | 770 us: 1.04x faster                                                      |
| chameleon                  | 4.98 ms                                                     | 4.77 ms: 1.04x faster                                                     |
| pidigits                   | 152 ms                                                      | 148 ms: 1.03x faster                                                      |
| sqlglot_transpile          | 1.02 ms                                                     | 993 us: 1.03x faster                                                      |
| xml_etree_generate         | 55.8 ms                                                     | 54.3 ms: 1.03x faster                                                     |
| sympy_str                  | 175 ms                                                      | 171 ms: 1.03x faster                                                      |
| xml_etree_process          | 37.7 ms                                                     | 36.8 ms: 1.02x faster                                                     |
| sqlglot_normalize          | 187 ms                                                      | 183 ms: 1.02x faster                                                      |
| sympy_sum                  | 91.5 ms                                                     | 89.8 ms: 1.02x faster                                                     |
| meteor_contest             | 74.6 ms                                                     | 73.2 ms: 1.02x faster                                                     |
| regex_effbot               | 1.62 ms                                                     | 1.60 ms: 1.01x faster                                                     |
| xml_etree_parse            | 93.0 ms                                                     | 92.3 ms: 1.01x faster                                                     |
| pickle                     | 7.43 us                                                     | 7.39 us: 1.01x faster                                                     |
| async_generators           | 239 ms                                                      | 241 ms: 1.01x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 35.1 ms: 1.02x slower                                                     |
| unpickle_list              | 2.75 us                                                     | 2.79 us: 1.02x slower                                                     |
| pickle_dict                | 18.4 us                                                     | 18.7 us: 1.02x slower                                                     |
| sympy_expand               | 284 ms                                                      | 289 ms: 1.02x slower                                                      |
| deltablue                  | 2.16 ms                                                     | 2.21 ms: 1.02x slower                                                     |
| json_loads                 | 13.9 us                                                     | 14.3 us: 1.03x slower                                                     |
| gc_traversal               | 1.52 ms                                                     | 1.58 ms: 1.04x slower                                                     |
| nqueens                    | 62.8 ms                                                     | 65.0 ms: 1.04x slower                                                     |
| docutils                   | 1.66 sec                                                    | 1.72 sec: 1.04x slower                                                    |
| tornado_http               | 89.5 ms                                                     | 93.0 ms: 1.04x slower                                                     |
| unpickle                   | 8.18 us                                                     | 8.56 us: 1.05x slower                                                     |
| 2to3                       | 218 ms                                                      | 228 ms: 1.05x slower                                                      |
| sympy_integrate            | 13.0 ms                                                     | 13.6 ms: 1.05x slower                                                     |
| mdp                        | 1.37 sec                                                    | 1.44 sec: 1.05x slower                                                    |
| scimark_sor                | 78.8 ms                                                     | 83.4 ms: 1.06x slower                                                     |
| go                         | 91.6 ms                                                     | 97.2 ms: 1.06x slower                                                     |
| json                       | 3.05 ms                                                     | 3.32 ms: 1.09x slower                                                     |
| aiohttp                    | 884 us                                                      | 963 us: 1.09x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 15.6 ms: 1.09x slower                                                     |
| coverage                   | 40.8 ms                                                     | 44.7 ms: 1.09x slower                                                     |
| pickle_list                | 2.83 us                                                     | 3.12 us: 1.10x slower                                                     |
| python_startup_no_site     | 16.2 ms                                                     | 18.5 ms: 1.14x slower                                                     |
| telco                      | 4.13 ms                                                     | 4.72 ms: 1.14x slower                                                     |
| hexiom                     | 4.10 ms                                                     | 4.70 ms: 1.15x slower                                                     |
| python_startup             | 19.5 ms                                                     | 22.4 ms: 1.15x slower                                                     |
| scimark_lu                 | 58.9 ms                                                     | 69.6 ms: 1.18x slower                                                     |
| typing_runtime_protocols   | 95.1 us                                                     | 113 us: 1.19x slower                                                      |
| create_gc_cycles           | 752 us                                                      | 932 us: 1.24x slower                                                      |
| asyncio_tcp                | 487 ms                                                      | 670 ms: 1.38x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.04x faster                                                              |

Benchmark hidden because not significant (7): bench_thread_pool, json_dumps, django_template, bench_mp_pool, regex_compile, pathlib, pycparser
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1-amd64-python-v3.12.0-3.12.0-0fb18b0.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240426-3.13.0a6+-8d9855f-JIT/bm-20240426-pythonperf1-amd64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.85% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
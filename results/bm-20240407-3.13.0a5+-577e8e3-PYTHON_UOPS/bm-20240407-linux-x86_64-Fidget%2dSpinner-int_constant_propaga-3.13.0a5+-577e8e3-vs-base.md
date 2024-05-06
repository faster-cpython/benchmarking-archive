# Results vs. base

- fork: Fidget-Spinner
- ref: int_constant_propaga
- machine: linux-x86_64
- commit hash: 577e8e3
- commit date: 2024-04-07
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 332 ms                                                                 | 320 ms: 1.04x faster                                                             |
| chameleon      | 8.03 ms                                                                | 7.95 ms: 1.01x faster                                                            |
| docutils       | 3.25 sec                                                               | 3.18 sec: 1.02x faster                                                           |
| html5lib       | 74.2 ms                                                                | 74.9 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io  | 1.01 sec                                                               | 976 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_none, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 205 ms                                                                 | 134 ms: 1.53x faster                                                             |
| float          | 135 ms                                                                 | 96.6 ms: 1.40x faster                                                            |
| pidigits       | 199 ms                                                                 | 202 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.28x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 223 ms                                                                 | 208 ms: 1.07x faster                                                             |
| regex_dna      | 224 ms                                                                 | 227 ms: 1.01x slower                                                             |
| regex_effbot   | 3.64 ms                                                                | 3.78 ms: 1.04x slower                                                            |
| regex_v8       | 25.5 ms                                                                | 26.9 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 3.48 sec                                                               | 2.72 sec: 1.28x faster                                                           |
| unpickle_pure_python | 415 us                                                                 | 333 us: 1.25x faster                                                             |
| xml_etree_iterparse  | 133 ms                                                                 | 115 ms: 1.16x faster                                                             |
| xml_etree_process    | 70.3 ms                                                                | 66.2 ms: 1.06x faster                                                            |
| xml_etree_generate   | 104 ms                                                                 | 98.1 ms: 1.06x faster                                                            |
| pickle_list          | 5.20 us                                                                | 5.02 us: 1.04x faster                                                            |
| json_loads           | 29.2 us                                                                | 28.5 us: 1.03x faster                                                            |
| json_dumps           | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                            |
| pickle_pure_python   | 314 us                                                                 | 318 us: 1.01x slower                                                             |
| pickle_dict          | 34.1 us                                                                | 34.8 us: 1.02x slower                                                            |
| pickle               | 11.7 us                                                                | 12.0 us: 1.02x slower                                                            |
| unpickle             | 15.0 us                                                                | 16.7 us: 1.12x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.05x faster                                                                     |

Benchmark hidden because not significant (2): unpickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 9.15 ms                                                                | 9.09 ms: 1.01x faster                                                            |
| python_startup         | 10.7 ms                                                                | 10.7 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 20.9 ms                                                                | 14.3 ms: 1.46x faster                                                            |
| genshi_text    | 26.5 ms                                                                | 26.1 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.14x faster                                                                     |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20240406-linux-x86_64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody                   | 205 ms                                                                 | 134 ms: 1.53x faster                                                             |
| spectral_norm           | 234 ms                                                                 | 153 ms: 1.53x faster                                                             |
| hexiom                  | 15.3 ms                                                                | 10.4 ms: 1.47x faster                                                            |
| scimark_monte_carlo     | 142 ms                                                                 | 97.3 ms: 1.46x faster                                                            |
| mako                    | 20.9 ms                                                                | 14.3 ms: 1.46x faster                                                            |
| fannkuch                | 763 ms                                                                 | 524 ms: 1.46x faster                                                             |
| comprehensions          | 35.7 us                                                                | 25.3 us: 1.41x faster                                                            |
| scimark_sparse_mat_mult | 8.95 ms                                                                | 6.38 ms: 1.40x faster                                                            |
| float                   | 135 ms                                                                 | 96.6 ms: 1.40x faster                                                            |
| pyflate                 | 891 ms                                                                 | 641 ms: 1.39x faster                                                             |
| scimark_fft             | 631 ms                                                                 | 470 ms: 1.34x faster                                                             |
| crypto_pyaes            | 127 ms                                                                 | 96.7 ms: 1.32x faster                                                            |
| tomli_loads             | 3.48 sec                                                               | 2.72 sec: 1.28x faster                                                           |
| unpickle_pure_python    | 415 us                                                                 | 333 us: 1.25x faster                                                             |
| chaos                   | 100 ms                                                                 | 82.2 ms: 1.22x faster                                                            |
| scimark_lu              | 208 ms                                                                 | 178 ms: 1.17x faster                                                             |
| richards                | 75.6 ms                                                                | 64.8 ms: 1.17x faster                                                            |
| deltablue               | 4.96 ms                                                                | 4.28 ms: 1.16x faster                                                            |
| xml_etree_iterparse     | 133 ms                                                                 | 115 ms: 1.16x faster                                                             |
| go                      | 228 ms                                                                 | 198 ms: 1.15x faster                                                             |
| richards_super          | 82.8 ms                                                                | 72.2 ms: 1.15x faster                                                            |
| pprint_pformat          | 2.67 sec                                                               | 2.40 sec: 1.12x faster                                                           |
| nqueens                 | 155 ms                                                                 | 139 ms: 1.11x faster                                                             |
| mdp                     | 3.22 sec                                                               | 2.94 sec: 1.10x faster                                                           |
| pprint_safe_repr        | 1.29 sec                                                               | 1.18 sec: 1.10x faster                                                           |
| scimark_sor             | 173 ms                                                                 | 160 ms: 1.08x faster                                                             |
| meteor_contest          | 145 ms                                                                 | 134 ms: 1.08x faster                                                             |
| raytrace                | 377 ms                                                                 | 350 ms: 1.08x faster                                                             |
| regex_compile           | 223 ms                                                                 | 208 ms: 1.07x faster                                                             |
| xml_etree_process       | 70.3 ms                                                                | 66.2 ms: 1.06x faster                                                            |
| xml_etree_generate      | 104 ms                                                                 | 98.1 ms: 1.06x faster                                                            |
| deepcopy_memo           | 50.4 us                                                                | 47.8 us: 1.06x faster                                                            |
| sqlglot_parse           | 1.64 ms                                                                | 1.56 ms: 1.05x faster                                                            |
| sympy_sum               | 191 ms                                                                 | 183 ms: 1.05x faster                                                             |
| sympy_integrate         | 25.6 ms                                                                | 24.5 ms: 1.04x faster                                                            |
| sqlglot_transpile       | 1.98 ms                                                                | 1.90 ms: 1.04x faster                                                            |
| 2to3                    | 332 ms                                                                 | 320 ms: 1.04x faster                                                             |
| sympy_str               | 349 ms                                                                 | 337 ms: 1.04x faster                                                             |
| pickle_list             | 5.20 us                                                                | 5.02 us: 1.04x faster                                                            |
| async_generators        | 502 ms                                                                 | 486 ms: 1.03x faster                                                             |
| async_tree_io           | 1.01 sec                                                               | 976 ms: 1.03x faster                                                             |
| sqlglot_optimize        | 70.9 ms                                                                | 68.8 ms: 1.03x faster                                                            |
| json_loads              | 29.2 us                                                                | 28.5 us: 1.03x faster                                                            |
| docutils                | 3.25 sec                                                               | 3.18 sec: 1.02x faster                                                           |
| bench_thread_pool       | 935 us                                                                 | 917 us: 1.02x faster                                                             |
| pylint                  | 319 ms                                                                 | 312 ms: 1.02x faster                                                             |
| genshi_text             | 26.5 ms                                                                | 26.1 ms: 1.02x faster                                                            |
| deepcopy_reduce         | 3.38 us                                                                | 3.34 us: 1.01x faster                                                            |
| chameleon               | 8.03 ms                                                                | 7.95 ms: 1.01x faster                                                            |
| sympy_expand            | 560 ms                                                                 | 556 ms: 1.01x faster                                                             |
| python_startup_no_site  | 9.15 ms                                                                | 9.09 ms: 1.01x faster                                                            |
| logging_simple          | 6.65 us                                                                | 6.61 us: 1.01x faster                                                            |
| python_startup          | 10.7 ms                                                                | 10.7 ms: 1.00x faster                                                            |
| generators              | 30.1 ms                                                                | 30.3 ms: 1.00x slower                                                            |
| create_gc_cycles        | 1.75 ms                                                                | 1.76 ms: 1.01x slower                                                            |
| json_dumps              | 10.7 ms                                                                | 10.8 ms: 1.01x slower                                                            |
| deepcopy                | 391 us                                                                 | 394 us: 1.01x slower                                                             |
| asyncio_tcp             | 514 ms                                                                 | 518 ms: 1.01x slower                                                             |
| html5lib                | 74.2 ms                                                                | 74.9 ms: 1.01x slower                                                            |
| thrift                  | 834 us                                                                 | 843 us: 1.01x slower                                                             |
| pidigits                | 199 ms                                                                 | 202 ms: 1.01x slower                                                             |
| pickle_pure_python      | 314 us                                                                 | 318 us: 1.01x slower                                                             |
| regex_dna               | 224 ms                                                                 | 227 ms: 1.01x slower                                                             |
| pickle_dict             | 34.1 us                                                                | 34.8 us: 1.02x slower                                                            |
| pickle                  | 11.7 us                                                                | 12.0 us: 1.02x slower                                                            |
| telco                   | 9.64 ms                                                                | 9.89 ms: 1.03x slower                                                            |
| regex_effbot            | 3.64 ms                                                                | 3.78 ms: 1.04x slower                                                            |
| pycparser               | 1.33 sec                                                               | 1.39 sec: 1.04x slower                                                           |
| regex_v8                | 25.5 ms                                                                | 26.9 ms: 1.06x slower                                                            |
| coroutines              | 22.7 ms                                                                | 24.3 ms: 1.07x slower                                                            |
| gc_traversal            | 3.75 ms                                                                | 4.03 ms: 1.07x slower                                                            |
| unpickle                | 15.0 us                                                                | 16.7 us: 1.12x slower                                                            |
| Geometric mean          | (ref)                                                                  | 1.07x faster                                                                     |

Benchmark hidden because not significant (27): async_tree_memoization, async_tree_none, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, unpickle_list, mypy2, async_tree_cpu_io_mixed, gunicorn, async_tree_cpu_io_mixed_tg, genshi_xml, logging_format, typing_runtime_protocols, coverage, dulwich_log, asyncio_websockets, asyncio_tcp_ssl, dask, xml_etree_parse, sqlglot_normalize, aiohttp, pathlib, json, bench_mp_pool, tornado_http, logging_silent, sqlite_synth

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x
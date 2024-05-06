# Results vs. base

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: d04d9ac
- commit date: 2024-04-23
- overall geometric mean: 1.01x faster
- HPT reliability: 99.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 306 ms: 1.01x faster                                                             |
| chameleon      | 7.90 ms                                                                | 8.10 ms: 1.02x slower                                                            |
| docutils       | 3.18 sec                                                               | 3.13 sec: 1.02x faster                                                           |
| html5lib       | 71.6 ms                                                                | 73.3 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 193 ms                                                                 | 199 ms: 1.03x slower                                                             |
| float          | 91.1 ms                                                                | 94.9 ms: 1.04x slower                                                            |
| nbody          | 123 ms                                                                 | 128 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                                 | 186 ms: 1.02x faster                                                             |
| regex_v8       | 25.7 ms                                                                | 25.5 ms: 1.01x faster                                                            |
| regex_dna      | 226 ms                                                                 | 227 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 154 ms                                                                 | 150 ms: 1.03x faster                                                             |
| tomli_loads          | 2.67 sec                                                               | 2.62 sec: 1.02x faster                                                           |
| pickle_list          | 5.14 us                                                                | 5.08 us: 1.01x faster                                                            |
| json_loads           | 27.9 us                                                                | 27.8 us: 1.00x faster                                                            |
| unpickle_pure_python | 297 us                                                                 | 298 us: 1.00x slower                                                             |
| unpickle_list        | 5.31 us                                                                | 5.35 us: 1.01x slower                                                            |
| unpickle             | 15.1 us                                                                | 15.3 us: 1.01x slower                                                            |
| xml_etree_process    | 64.5 ms                                                                | 65.6 ms: 1.02x slower                                                            |
| pickle_pure_python   | 314 us                                                                 | 321 us: 1.02x slower                                                             |
| pickle               | 11.6 us                                                                | 11.9 us: 1.02x slower                                                            |
| pickle_dict          | 34.7 us                                                                | 35.5 us: 1.02x slower                                                            |
| xml_etree_iterparse  | 111 ms                                                                 | 114 ms: 1.03x slower                                                             |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (2): json_dumps, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                                | 7.14 ms: 1.00x faster                                                            |
| python_startup         | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 42.8 ms                                                                | 41.5 ms: 1.03x faster                                                            |
| genshi_xml      | 61.7 ms                                                                | 59.9 ms: 1.03x faster                                                            |
| genshi_text     | 26.0 ms                                                                | 25.7 ms: 1.01x faster                                                            |
| mako            | 13.1 ms                                                                | 14.5 ms: 1.11x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                                     |

All benchmarks:
===============

| Benchmark               | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|-------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nqueens                 | 129 ms                                                                 | 111 ms: 1.16x faster                                                             |
| pyflate                 | 712 ms                                                                 | 639 ms: 1.11x faster                                                             |
| pprint_safe_repr        | 1.09 sec                                                               | 983 ms: 1.11x faster                                                             |
| pprint_pformat          | 2.27 sec                                                               | 2.04 sec: 1.11x faster                                                           |
| richards_super          | 70.7 ms                                                                | 63.7 ms: 1.11x faster                                                            |
| scimark_monte_carlo     | 103 ms                                                                 | 93.9 ms: 1.10x faster                                                            |
| richards                | 62.6 ms                                                                | 57.3 ms: 1.09x faster                                                            |
| crypto_pyaes            | 103 ms                                                                 | 95.3 ms: 1.08x faster                                                            |
| deepcopy_memo           | 49.3 us                                                                | 46.1 us: 1.07x faster                                                            |
| raytrace                | 350 ms                                                                 | 330 ms: 1.06x faster                                                             |
| chaos                   | 85.4 ms                                                                | 80.9 ms: 1.06x faster                                                            |
| sqlglot_optimize        | 67.1 ms                                                                | 64.5 ms: 1.04x faster                                                            |
| telco                   | 9.67 ms                                                                | 9.36 ms: 1.03x faster                                                            |
| django_template         | 42.8 ms                                                                | 41.5 ms: 1.03x faster                                                            |
| scimark_sor             | 166 ms                                                                 | 161 ms: 1.03x faster                                                             |
| sympy_sum               | 184 ms                                                                 | 178 ms: 1.03x faster                                                             |
| genshi_xml              | 61.7 ms                                                                | 59.9 ms: 1.03x faster                                                            |
| xml_etree_parse         | 154 ms                                                                 | 150 ms: 1.03x faster                                                             |
| sqlglot_transpile       | 1.87 ms                                                                | 1.82 ms: 1.03x faster                                                            |
| sqlglot_parse           | 1.55 ms                                                                | 1.50 ms: 1.03x faster                                                            |
| sqlite_synth            | 3.09 us                                                                | 3.01 us: 1.03x faster                                                            |
| fannkuch                | 524 ms                                                                 | 511 ms: 1.03x faster                                                             |
| logging_format          | 7.34 us                                                                | 7.16 us: 1.03x faster                                                            |
| logging_simple          | 6.56 us                                                                | 6.43 us: 1.02x faster                                                            |
| tomli_loads             | 2.67 sec                                                               | 2.62 sec: 1.02x faster                                                           |
| meteor_contest          | 125 ms                                                                 | 122 ms: 1.02x faster                                                             |
| docutils                | 3.18 sec                                                               | 3.13 sec: 1.02x faster                                                           |
| sqlglot_normalize       | 128 ms                                                                 | 126 ms: 1.02x faster                                                             |
| regex_compile           | 190 ms                                                                 | 186 ms: 1.02x faster                                                             |
| pathlib                 | 18.7 ms                                                                | 18.4 ms: 1.02x faster                                                            |
| gunicorn                | 1.34 ms                                                                | 1.32 ms: 1.02x faster                                                            |
| async_generators        | 489 ms                                                                 | 482 ms: 1.02x faster                                                             |
| genshi_text             | 26.0 ms                                                                | 25.7 ms: 1.01x faster                                                            |
| pycparser               | 1.31 sec                                                               | 1.29 sec: 1.01x faster                                                           |
| aiohttp                 | 1.25 ms                                                                | 1.23 ms: 1.01x faster                                                            |
| 2to3                    | 310 ms                                                                 | 306 ms: 1.01x faster                                                             |
| bench_thread_pool       | 904 us                                                                 | 892 us: 1.01x faster                                                             |
| hexiom                  | 10.2 ms                                                                | 10.1 ms: 1.01x faster                                                            |
| pickle_list             | 5.14 us                                                                | 5.08 us: 1.01x faster                                                            |
| sympy_str               | 334 ms                                                                 | 330 ms: 1.01x faster                                                             |
| json                    | 5.26 ms                                                                | 5.20 ms: 1.01x faster                                                            |
| dulwich_log             | 74.6 ms                                                                | 73.9 ms: 1.01x faster                                                            |
| coverage                | 98.2 ms                                                                | 97.4 ms: 1.01x faster                                                            |
| regex_v8                | 25.7 ms                                                                | 25.5 ms: 1.01x faster                                                            |
| deepcopy                | 387 us                                                                 | 384 us: 1.01x faster                                                             |
| json_loads              | 27.9 us                                                                | 27.8 us: 1.00x faster                                                            |
| comprehensions          | 24.7 us                                                                | 24.6 us: 1.00x faster                                                            |
| python_startup_no_site  | 7.16 ms                                                                | 7.14 ms: 1.00x faster                                                            |
| python_startup          | 10.6 ms                                                                | 10.6 ms: 1.00x slower                                                            |
| unpickle_pure_python    | 297 us                                                                 | 298 us: 1.00x slower                                                             |
| sympy_integrate         | 24.1 ms                                                                | 24.1 ms: 1.00x slower                                                            |
| scimark_lu              | 170 ms                                                                 | 170 ms: 1.01x slower                                                             |
| generators              | 30.2 ms                                                                | 30.3 ms: 1.01x slower                                                            |
| regex_dna               | 226 ms                                                                 | 227 ms: 1.01x slower                                                             |
| unpickle_list           | 5.31 us                                                                | 5.35 us: 1.01x slower                                                            |
| sympy_expand            | 548 ms                                                                 | 552 ms: 1.01x slower                                                             |
| create_gc_cycles        | 1.77 ms                                                                | 1.79 ms: 1.01x slower                                                            |
| asyncio_tcp_ssl         | 1.86 sec                                                               | 1.88 sec: 1.01x slower                                                           |
| unpickle                | 15.1 us                                                                | 15.3 us: 1.01x slower                                                            |
| deepcopy_reduce         | 3.30 us                                                                | 3.35 us: 1.01x slower                                                            |
| xml_etree_process       | 64.5 ms                                                                | 65.6 ms: 1.02x slower                                                            |
| pickle_pure_python      | 314 us                                                                 | 321 us: 1.02x slower                                                             |
| pickle                  | 11.6 us                                                                | 11.9 us: 1.02x slower                                                            |
| pickle_dict             | 34.7 us                                                                | 35.5 us: 1.02x slower                                                            |
| html5lib                | 71.6 ms                                                                | 73.3 ms: 1.02x slower                                                            |
| chameleon               | 7.90 ms                                                                | 8.10 ms: 1.02x slower                                                            |
| asyncio_tcp             | 514 ms                                                                 | 528 ms: 1.03x slower                                                             |
| xml_etree_iterparse     | 111 ms                                                                 | 114 ms: 1.03x slower                                                             |
| logging_silent          | 106 ns                                                                 | 110 ns: 1.03x slower                                                             |
| pidigits                | 193 ms                                                                 | 199 ms: 1.03x slower                                                             |
| coroutines              | 23.3 ms                                                                | 24.2 ms: 1.04x slower                                                            |
| float                   | 91.1 ms                                                                | 94.9 ms: 1.04x slower                                                            |
| nbody                   | 123 ms                                                                 | 128 ms: 1.04x slower                                                             |
| go                      | 193 ms                                                                 | 201 ms: 1.04x slower                                                             |
| scimark_fft             | 452 ms                                                                 | 473 ms: 1.05x slower                                                             |
| gc_traversal            | 3.76 ms                                                                | 3.96 ms: 1.05x slower                                                            |
| mdp                     | 2.83 sec                                                               | 3.02 sec: 1.07x slower                                                           |
| scimark_sparse_mat_mult | 6.05 ms                                                                | 6.54 ms: 1.08x slower                                                            |
| spectral_norm           | 140 ms                                                                 | 153 ms: 1.10x slower                                                             |
| mako                    | 13.1 ms                                                                | 14.5 ms: 1.11x slower                                                            |
| Geometric mean          | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (21): async_tree_io_tg, deltablue, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_none, async_tree_cpu_io_mixed_tg, json_dumps, async_tree_memoization, async_tree_memoization_tg, thrift, xml_etree_generate, regex_effbot, async_tree_io, asyncio_websockets, typing_runtime_protocols, mypy2, dask, bench_mp_pool, tornado_http, pylint, djangocms

# HPT report

- Reliability score: 99.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
# Results vs. base

- fork: nineteendo
- ref: use_PyTuple_Pack
- machine: linux-x86_64
- commit hash: 59ac30f
- commit date: 2024-04-29
- overall geometric mean: 1.00x faster
- HPT reliability: 85.04%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| chameleon      | 6.95 ms                                                                | 6.98 ms: 1.01x slower                                                  |
| docutils       | 2.81 sec                                                               | 2.79 sec: 1.00x faster                                                 |
| html5lib       | 66.2 ms                                                                | 67.4 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io  | 927 ms                                                                 | 898 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 225 ms                                                                 | 218 ms: 1.03x faster                                                   |
| regex_v8       | 24.9 ms                                                                | 24.4 ms: 1.02x faster                                                  |
| regex_compile  | 134 ms                                                                 | 134 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 35.4 us                                                                | 34.6 us: 1.02x faster                                                  |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                  |
| pickle               | 11.7 us                                                                | 11.7 us: 1.00x faster                                                  |
| pickle_pure_python   | 301 us                                                                 | 300 us: 1.00x faster                                                   |
| pickle_list          | 5.00 us                                                                | 5.02 us: 1.00x slower                                                  |
| tomli_loads          | 2.14 sec                                                               | 2.15 sec: 1.01x slower                                                 |
| xml_etree_process    | 59.4 ms                                                                | 59.8 ms: 1.01x slower                                                  |
| xml_etree_generate   | 86.3 ms                                                                | 87.2 ms: 1.01x slower                                                  |
| unpickle_pure_python | 212 us                                                                 | 215 us: 1.01x slower                                                   |
| unpickle_list        | 5.17 us                                                                | 5.38 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (4): xml_etree_iterparse, json_loads, xml_etree_parse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                  |
| python_startup_no_site | 7.11 ms                                                                | 7.09 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 52.0 ms                                                                | 51.1 ms: 1.02x faster                                                  |
| mako            | 10.9 ms                                                                | 10.7 ms: 1.02x faster                                                  |
| django_template | 35.0 ms                                                                | 34.5 ms: 1.01x faster                                                  |
| genshi_text     | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark               | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|-------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| logging_silent          | 101 ns                                                                 | 97.2 ns: 1.04x faster                                                  |
| regex_dna               | 225 ms                                                                 | 218 ms: 1.03x faster                                                   |
| async_tree_io           | 927 ms                                                                 | 898 ms: 1.03x faster                                                   |
| mdp                     | 2.64 sec                                                               | 2.57 sec: 1.02x faster                                                 |
| pickle_dict             | 35.4 us                                                                | 34.6 us: 1.02x faster                                                  |
| spectral_norm           | 111 ms                                                                 | 108 ms: 1.02x faster                                                   |
| telco                   | 8.62 ms                                                                | 8.45 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult | 5.22 ms                                                                | 5.12 ms: 1.02x faster                                                  |
| genshi_xml              | 52.0 ms                                                                | 51.1 ms: 1.02x faster                                                  |
| regex_v8                | 24.9 ms                                                                | 24.4 ms: 1.02x faster                                                  |
| mako                    | 10.9 ms                                                                | 10.7 ms: 1.02x faster                                                  |
| richards                | 47.3 ms                                                                | 46.6 ms: 1.02x faster                                                  |
| django_template         | 35.0 ms                                                                | 34.5 ms: 1.01x faster                                                  |
| nqueens                 | 81.9 ms                                                                | 80.7 ms: 1.01x faster                                                  |
| comprehensions          | 16.9 us                                                                | 16.7 us: 1.01x faster                                                  |
| pycparser               | 1.15 sec                                                               | 1.14 sec: 1.01x faster                                                 |
| deepcopy_memo           | 37.6 us                                                                | 37.2 us: 1.01x faster                                                  |
| raytrace                | 261 ms                                                                 | 259 ms: 1.01x faster                                                   |
| deepcopy_reduce         | 3.21 us                                                                | 3.17 us: 1.01x faster                                                  |
| richards_super          | 53.7 ms                                                                | 53.1 ms: 1.01x faster                                                  |
| generators              | 29.9 ms                                                                | 29.7 ms: 1.01x faster                                                  |
| sqlglot_transpile       | 1.59 ms                                                                | 1.57 ms: 1.01x faster                                                  |
| json_dumps              | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                  |
| pathlib                 | 17.6 ms                                                                | 17.5 ms: 1.01x faster                                                  |
| meteor_contest          | 110 ms                                                                 | 110 ms: 1.01x faster                                                   |
| deltablue               | 3.21 ms                                                                | 3.19 ms: 1.01x faster                                                  |
| go                      | 142 ms                                                                 | 141 ms: 1.01x faster                                                   |
| pprint_pformat          | 1.51 sec                                                               | 1.50 sec: 1.01x faster                                                 |
| chaos                   | 60.4 ms                                                                | 60.1 ms: 1.01x faster                                                  |
| async_generators        | 446 ms                                                                 | 444 ms: 1.00x faster                                                   |
| docutils                | 2.81 sec                                                               | 2.79 sec: 1.00x faster                                                 |
| pickle                  | 11.7 us                                                                | 11.7 us: 1.00x faster                                                  |
| sqlglot_optimize        | 54.6 ms                                                                | 54.4 ms: 1.00x faster                                                  |
| pickle_pure_python      | 301 us                                                                 | 300 us: 1.00x faster                                                   |
| asyncio_tcp_ssl         | 1.84 sec                                                               | 1.84 sec: 1.00x faster                                                 |
| scimark_fft             | 366 ms                                                                 | 365 ms: 1.00x faster                                                   |
| python_startup          | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                  |
| python_startup_no_site  | 7.11 ms                                                                | 7.09 ms: 1.00x faster                                                  |
| hexiom                  | 6.13 ms                                                                | 6.15 ms: 1.00x slower                                                  |
| sympy_integrate         | 20.1 ms                                                                | 20.2 ms: 1.00x slower                                                  |
| pprint_safe_repr        | 732 ms                                                                 | 735 ms: 1.00x slower                                                   |
| pickle_list             | 5.00 us                                                                | 5.02 us: 1.00x slower                                                  |
| bench_thread_pool       | 827 us                                                                 | 831 us: 1.00x slower                                                   |
| chameleon               | 6.95 ms                                                                | 6.98 ms: 1.01x slower                                                  |
| sympy_expand            | 464 ms                                                                 | 467 ms: 1.01x slower                                                   |
| tomli_loads             | 2.14 sec                                                               | 2.15 sec: 1.01x slower                                                 |
| xml_etree_process       | 59.4 ms                                                                | 59.8 ms: 1.01x slower                                                  |
| coverage                | 91.0 ms                                                                | 91.6 ms: 1.01x slower                                                  |
| sympy_sum               | 153 ms                                                                 | 154 ms: 1.01x slower                                                   |
| regex_compile           | 134 ms                                                                 | 134 ms: 1.01x slower                                                   |
| gunicorn                | 1.26 ms                                                                | 1.27 ms: 1.01x slower                                                  |
| thrift                  | 815 us                                                                 | 821 us: 1.01x slower                                                   |
| crypto_pyaes            | 74.7 ms                                                                | 75.4 ms: 1.01x slower                                                  |
| aiohttp                 | 1.16 ms                                                                | 1.17 ms: 1.01x slower                                                  |
| create_gc_cycles        | 1.74 ms                                                                | 1.76 ms: 1.01x slower                                                  |
| json                    | 5.13 ms                                                                | 5.18 ms: 1.01x slower                                                  |
| pyflate                 | 461 ms                                                                 | 466 ms: 1.01x slower                                                   |
| xml_etree_generate      | 86.3 ms                                                                | 87.2 ms: 1.01x slower                                                  |
| genshi_text             | 23.2 ms                                                                | 23.5 ms: 1.01x slower                                                  |
| bench_mp_pool           | 23.6 ms                                                                | 23.9 ms: 1.01x slower                                                  |
| scimark_monte_carlo     | 68.6 ms                                                                | 69.4 ms: 1.01x slower                                                  |
| unpickle_pure_python    | 212 us                                                                 | 215 us: 1.01x slower                                                   |
| fannkuch                | 385 ms                                                                 | 390 ms: 1.01x slower                                                   |
| scimark_sor             | 122 ms                                                                 | 124 ms: 1.02x slower                                                   |
| logging_simple          | 5.73 us                                                                | 5.84 us: 1.02x slower                                                  |
| html5lib                | 66.2 ms                                                                | 67.4 ms: 1.02x slower                                                  |
| logging_format          | 6.33 us                                                                | 6.46 us: 1.02x slower                                                  |
| unpickle_list           | 5.17 us                                                                | 5.38 us: 1.04x slower                                                  |
| gc_traversal            | 3.70 ms                                                                | 4.02 ms: 1.09x slower                                                  |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (32): async_tree_memoization, djangocms, async_tree_cpu_io_mixed, sqlglot_parse, async_tree_none, float, sqlglot_normalize, async_tree_io_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg, deepcopy, asyncio_tcp, xml_etree_iterparse, async_tree_memoization_tg, coroutines, nbody, pidigits, 2to3, sympy_str, regex_effbot, mypy2, sqlite_synth, async_tree_none_tg, pylint, dulwich_log, tornado_http, json_loads, typing_runtime_protocols, xml_etree_parse, dask, scimark_lu, unpickle

# HPT report

- Reliability score: 85.04% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
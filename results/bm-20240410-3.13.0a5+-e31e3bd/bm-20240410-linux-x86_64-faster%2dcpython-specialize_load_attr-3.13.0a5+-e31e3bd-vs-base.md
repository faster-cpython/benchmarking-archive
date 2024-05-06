# Results vs. base

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: e31e3bd
- commit date: 2024-04-10
- overall geometric mean: 1.00x slower
- HPT reliability: 77.87%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 272 ms                                                                 | 273 ms: 1.00x slower                                                             |
| chameleon      | 6.94 ms                                                                | 7.05 ms: 1.02x slower                                                            |
| html5lib       | 67.0 ms                                                                | 67.8 ms: 1.01x slower                                                            |
| tornado_http   | 94.8 ms                                                                | 93.9 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                                | 88.2 ms: 1.01x faster                                                            |
| float          | 78.9 ms                                                                | 78.6 ms: 1.00x faster                                                            |
| pidigits       | 191 ms                                                                 | 190 ms: 1.00x faster                                                             |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                | 25.8 ms: 1.01x faster                                                            |
| regex_dna      | 226 ms                                                                 | 225 ms: 1.00x faster                                                             |
| regex_effbot   | 3.74 ms                                                                | 3.75 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_dict          | 34.5 us                                                                | 32.1 us: 1.07x faster                                                            |
| pickle_list          | 5.23 us                                                                | 4.92 us: 1.06x faster                                                            |
| xml_etree_parse      | 163 ms                                                                 | 159 ms: 1.02x faster                                                             |
| xml_etree_iterparse  | 110 ms                                                                 | 108 ms: 1.02x faster                                                             |
| xml_etree_process    | 60.3 ms                                                                | 60.6 ms: 1.00x slower                                                            |
| xml_etree_generate   | 87.5 ms                                                                | 88.0 ms: 1.01x slower                                                            |
| json_loads           | 28.5 us                                                                | 28.8 us: 1.01x slower                                                            |
| json_dumps           | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| pickle               | 11.8 us                                                                | 11.9 us: 1.01x slower                                                            |
| unpickle_pure_python | 225 us                                                                 | 228 us: 1.01x slower                                                             |
| unpickle_list        | 5.09 us                                                                | 5.27 us: 1.03x slower                                                            |
| unpickle             | 15.1 us                                                                | 15.9 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): tomli_loads, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| python_startup_no_site | 8.96 ms                                                                | 8.93 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 52.3 ms                                                                | 53.6 ms: 1.03x slower                                                            |
| genshi_text    | 23.8 ms                                                                | 24.6 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                     |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_dict              | 34.5 us                                                                | 32.1 us: 1.07x faster                                                            |
| pickle_list              | 5.23 us                                                                | 4.92 us: 1.06x faster                                                            |
| pycparser                | 1.21 sec                                                               | 1.17 sec: 1.04x faster                                                           |
| spectral_norm            | 116 ms                                                                 | 112 ms: 1.04x faster                                                             |
| gc_traversal             | 3.88 ms                                                                | 3.75 ms: 1.03x faster                                                            |
| xml_etree_parse          | 163 ms                                                                 | 159 ms: 1.02x faster                                                             |
| thrift                   | 819 us                                                                 | 801 us: 1.02x faster                                                             |
| xml_etree_iterparse      | 110 ms                                                                 | 108 ms: 1.02x faster                                                             |
| telco                    | 8.75 ms                                                                | 8.62 ms: 1.02x faster                                                            |
| fannkuch                 | 397 ms                                                                 | 392 ms: 1.01x faster                                                             |
| create_gc_cycles         | 1.74 ms                                                                | 1.72 ms: 1.01x faster                                                            |
| nbody                    | 89.3 ms                                                                | 88.2 ms: 1.01x faster                                                            |
| async_generators         | 449 ms                                                                 | 444 ms: 1.01x faster                                                             |
| regex_v8                 | 26.1 ms                                                                | 25.8 ms: 1.01x faster                                                            |
| tornado_http             | 94.8 ms                                                                | 93.9 ms: 1.01x faster                                                            |
| crypto_pyaes             | 74.6 ms                                                                | 74.0 ms: 1.01x faster                                                            |
| scimark_fft              | 374 ms                                                                 | 372 ms: 1.01x faster                                                             |
| float                    | 78.9 ms                                                                | 78.6 ms: 1.00x faster                                                            |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| sqlglot_optimize         | 55.7 ms                                                                | 55.5 ms: 1.00x faster                                                            |
| scimark_monte_carlo      | 68.0 ms                                                                | 67.8 ms: 1.00x faster                                                            |
| regex_dna                | 226 ms                                                                 | 225 ms: 1.00x faster                                                             |
| pprint_pformat           | 1.55 sec                                                               | 1.54 sec: 1.00x faster                                                           |
| pidigits                 | 191 ms                                                                 | 190 ms: 1.00x faster                                                             |
| python_startup_no_site   | 8.96 ms                                                                | 8.93 ms: 1.00x faster                                                            |
| meteor_contest           | 111 ms                                                                 | 111 ms: 1.00x faster                                                             |
| pylint                   | 280 ms                                                                 | 280 ms: 1.00x faster                                                             |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.85 sec: 1.00x slower                                                           |
| 2to3                     | 272 ms                                                                 | 273 ms: 1.00x slower                                                             |
| regex_effbot             | 3.74 ms                                                                | 3.75 ms: 1.00x slower                                                            |
| sqlglot_transpile        | 1.59 ms                                                                | 1.60 ms: 1.00x slower                                                            |
| sympy_integrate          | 20.4 ms                                                                | 20.5 ms: 1.00x slower                                                            |
| sqlglot_normalize        | 112 ms                                                                 | 112 ms: 1.00x slower                                                             |
| xml_etree_process        | 60.3 ms                                                                | 60.6 ms: 1.00x slower                                                            |
| coroutines               | 22.3 ms                                                                | 22.4 ms: 1.00x slower                                                            |
| richards                 | 47.7 ms                                                                | 48.0 ms: 1.01x slower                                                            |
| xml_etree_generate       | 87.5 ms                                                                | 88.0 ms: 1.01x slower                                                            |
| nqueens                  | 82.1 ms                                                                | 82.7 ms: 1.01x slower                                                            |
| pyflate                  | 477 ms                                                                 | 481 ms: 1.01x slower                                                             |
| json_loads               | 28.5 us                                                                | 28.8 us: 1.01x slower                                                            |
| pprint_safe_repr         | 750 ms                                                                 | 756 ms: 1.01x slower                                                             |
| json_dumps               | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| pickle                   | 11.8 us                                                                | 11.9 us: 1.01x slower                                                            |
| deepcopy                 | 354 us                                                                 | 358 us: 1.01x slower                                                             |
| logging_simple           | 5.80 us                                                                | 5.86 us: 1.01x slower                                                            |
| unpickle_pure_python     | 225 us                                                                 | 228 us: 1.01x slower                                                             |
| html5lib                 | 67.0 ms                                                                | 67.8 ms: 1.01x slower                                                            |
| scimark_sor              | 123 ms                                                                 | 124 ms: 1.01x slower                                                             |
| logging_format           | 6.39 us                                                                | 6.49 us: 1.01x slower                                                            |
| logging_silent           | 103 ns                                                                 | 105 ns: 1.01x slower                                                             |
| asyncio_tcp              | 499 ms                                                                 | 507 ms: 1.02x slower                                                             |
| chameleon                | 6.94 ms                                                                | 7.05 ms: 1.02x slower                                                            |
| deltablue                | 3.23 ms                                                                | 3.29 ms: 1.02x slower                                                            |
| hexiom                   | 6.36 ms                                                                | 6.48 ms: 1.02x slower                                                            |
| mdp                      | 2.62 sec                                                               | 2.66 sec: 1.02x slower                                                           |
| deepcopy_memo            | 38.2 us                                                                | 38.9 us: 1.02x slower                                                            |
| genshi_xml               | 52.3 ms                                                                | 53.6 ms: 1.03x slower                                                            |
| genshi_text              | 23.8 ms                                                                | 24.6 ms: 1.03x slower                                                            |
| generators               | 29.7 ms                                                                | 30.7 ms: 1.03x slower                                                            |
| typing_runtime_protocols | 113 us                                                                 | 117 us: 1.03x slower                                                             |
| unpickle_list            | 5.09 us                                                                | 5.27 us: 1.03x slower                                                            |
| scimark_lu               | 114 ms                                                                 | 119 ms: 1.04x slower                                                             |
| unpickle                 | 15.1 us                                                                | 15.9 us: 1.05x slower                                                            |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (36): async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, json, async_tree_none, mypy2, async_tree_cpu_io_mixed, async_tree_memoization, tomli_loads, dask, comprehensions, sympy_sum, scimark_sparse_mat_mult, go, chaos, gunicorn, bench_thread_pool, dulwich_log, sympy_expand, bench_mp_pool, richards_super, mako, aiohttp, sqlglot_parse, docutils, raytrace, asyncio_websockets, regex_compile, deepcopy_reduce, sqlite_synth, pathlib, sympy_str, coverage, pickle_pure_python, async_tree_io, async_tree_io_tg

# HPT report

- Reliability score: 77.87% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
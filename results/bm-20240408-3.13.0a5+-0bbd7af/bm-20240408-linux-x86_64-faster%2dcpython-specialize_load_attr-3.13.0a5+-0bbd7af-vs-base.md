# Results vs. base

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 0bbd7af
- commit date: 2024-04-08
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 272 ms                                                                 | 269 ms: 1.01x faster                                                             |
| chameleon      | 6.94 ms                                                                | 6.83 ms: 1.02x faster                                                            |
| html5lib       | 67.0 ms                                                                | 67.7 ms: 1.01x slower                                                            |
| tornado_http   | 94.8 ms                                                                | 94.5 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                                | 77.6 ms: 1.02x faster                                                            |
| nbody          | 89.3 ms                                                                | 87.9 ms: 1.02x faster                                                            |
| pidigits       | 191 ms                                                                 | 197 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                | 24.8 ms: 1.05x faster                                                            |
| regex_effbot   | 3.74 ms                                                                | 3.66 ms: 1.02x faster                                                            |
| regex_compile  | 136 ms                                                                 | 134 ms: 1.02x faster                                                             |
| regex_dna      | 226 ms                                                                 | 227 ms: 1.00x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 110 ms                                                                 | 107 ms: 1.03x faster                                                             |
| tomli_loads          | 2.18 sec                                                               | 2.12 sec: 1.03x faster                                                           |
| unpickle_pure_python | 225 us                                                                 | 220 us: 1.02x faster                                                             |
| xml_etree_parse      | 163 ms                                                                 | 160 ms: 1.02x faster                                                             |
| unpickle_list        | 5.09 us                                                                | 5.01 us: 1.02x faster                                                            |
| pickle_pure_python   | 302 us                                                                 | 298 us: 1.01x faster                                                             |
| pickle_list          | 5.23 us                                                                | 5.19 us: 1.01x faster                                                            |
| xml_etree_generate   | 87.5 ms                                                                | 88.0 ms: 1.01x slower                                                            |
| xml_etree_process    | 60.3 ms                                                                | 60.9 ms: 1.01x slower                                                            |
| json_loads           | 28.5 us                                                                | 28.8 us: 1.01x slower                                                            |
| pickle               | 11.8 us                                                                | 12.1 us: 1.03x slower                                                            |
| pickle_dict          | 34.5 us                                                                | 36.4 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): unpickle, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| python_startup_no_site | 8.96 ms                                                                | 8.95 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.1 ms                                                                | 10.7 ms: 1.04x faster                                                            |
| genshi_xml     | 52.3 ms                                                                | 51.5 ms: 1.02x faster                                                            |
| genshi_text    | 23.8 ms                                                                | 23.6 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| spectral_norm            | 116 ms                                                                 | 109 ms: 1.06x faster                                                             |
| regex_v8                 | 26.1 ms                                                                | 24.8 ms: 1.05x faster                                                            |
| deepcopy_memo            | 38.2 us                                                                | 36.4 us: 1.05x faster                                                            |
| pycparser                | 1.21 sec                                                               | 1.16 sec: 1.05x faster                                                           |
| mako                     | 11.1 ms                                                                | 10.7 ms: 1.04x faster                                                            |
| fannkuch                 | 397 ms                                                                 | 383 ms: 1.04x faster                                                             |
| pprint_pformat           | 1.55 sec                                                               | 1.50 sec: 1.03x faster                                                           |
| gc_traversal             | 3.88 ms                                                                | 3.75 ms: 1.03x faster                                                            |
| logging_silent           | 103 ns                                                                 | 101 ns: 1.03x faster                                                             |
| xml_etree_iterparse      | 110 ms                                                                 | 107 ms: 1.03x faster                                                             |
| pprint_safe_repr         | 750 ms                                                                 | 732 ms: 1.03x faster                                                             |
| tomli_loads              | 2.18 sec                                                               | 2.12 sec: 1.03x faster                                                           |
| scimark_monte_carlo      | 68.0 ms                                                                | 66.4 ms: 1.02x faster                                                            |
| logging_simple           | 5.80 us                                                                | 5.66 us: 1.02x faster                                                            |
| unpickle_pure_python     | 225 us                                                                 | 220 us: 1.02x faster                                                             |
| regex_effbot             | 3.74 ms                                                                | 3.66 ms: 1.02x faster                                                            |
| hexiom                   | 6.36 ms                                                                | 6.23 ms: 1.02x faster                                                            |
| pyflate                  | 477 ms                                                                 | 467 ms: 1.02x faster                                                             |
| nqueens                  | 82.1 ms                                                                | 80.6 ms: 1.02x faster                                                            |
| xml_etree_parse          | 163 ms                                                                 | 160 ms: 1.02x faster                                                             |
| regex_compile            | 136 ms                                                                 | 134 ms: 1.02x faster                                                             |
| go                       | 144 ms                                                                 | 141 ms: 1.02x faster                                                             |
| comprehensions           | 17.0 us                                                                | 16.7 us: 1.02x faster                                                            |
| float                    | 78.9 ms                                                                | 77.6 ms: 1.02x faster                                                            |
| nbody                    | 89.3 ms                                                                | 87.9 ms: 1.02x faster                                                            |
| richards_super           | 53.9 ms                                                                | 53.1 ms: 1.02x faster                                                            |
| chameleon                | 6.94 ms                                                                | 6.83 ms: 1.02x faster                                                            |
| unpickle_list            | 5.09 us                                                                | 5.01 us: 1.02x faster                                                            |
| deepcopy_reduce          | 3.21 us                                                                | 3.16 us: 1.02x faster                                                            |
| genshi_xml               | 52.3 ms                                                                | 51.5 ms: 1.02x faster                                                            |
| thrift                   | 819 us                                                                 | 807 us: 1.01x faster                                                             |
| typing_runtime_protocols | 113 us                                                                 | 112 us: 1.01x faster                                                             |
| sympy_expand             | 474 ms                                                                 | 468 ms: 1.01x faster                                                             |
| richards                 | 47.7 ms                                                                | 47.1 ms: 1.01x faster                                                            |
| async_generators         | 449 ms                                                                 | 443 ms: 1.01x faster                                                             |
| logging_format           | 6.39 us                                                                | 6.31 us: 1.01x faster                                                            |
| deltablue                | 3.23 ms                                                                | 3.19 ms: 1.01x faster                                                            |
| create_gc_cycles         | 1.74 ms                                                                | 1.72 ms: 1.01x faster                                                            |
| chaos                    | 60.6 ms                                                                | 59.9 ms: 1.01x faster                                                            |
| deepcopy                 | 354 us                                                                 | 350 us: 1.01x faster                                                             |
| pickle_pure_python       | 302 us                                                                 | 298 us: 1.01x faster                                                             |
| pathlib                  | 18.7 ms                                                                | 18.5 ms: 1.01x faster                                                            |
| mdp                      | 2.62 sec                                                               | 2.59 sec: 1.01x faster                                                           |
| sqlite_synth             | 2.94 us                                                                | 2.92 us: 1.01x faster                                                            |
| scimark_fft              | 374 ms                                                                 | 371 ms: 1.01x faster                                                             |
| genshi_text              | 23.8 ms                                                                | 23.6 ms: 1.01x faster                                                            |
| 2to3                     | 272 ms                                                                 | 269 ms: 1.01x faster                                                             |
| raytrace                 | 262 ms                                                                 | 259 ms: 1.01x faster                                                             |
| sqlglot_normalize        | 112 ms                                                                 | 111 ms: 1.01x faster                                                             |
| sympy_str                | 281 ms                                                                 | 278 ms: 1.01x faster                                                             |
| pickle_list              | 5.23 us                                                                | 5.19 us: 1.01x faster                                                            |
| sqlglot_optimize         | 55.7 ms                                                                | 55.3 ms: 1.01x faster                                                            |
| coverage                 | 96.9 ms                                                                | 96.3 ms: 1.01x faster                                                            |
| coroutines               | 22.3 ms                                                                | 22.1 ms: 1.01x faster                                                            |
| sympy_sum                | 157 ms                                                                 | 156 ms: 1.01x faster                                                             |
| bench_thread_pool        | 838 us                                                                 | 834 us: 1.00x faster                                                             |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.84 sec: 1.00x faster                                                           |
| sympy_integrate          | 20.4 ms                                                                | 20.4 ms: 1.00x faster                                                            |
| pylint                   | 280 ms                                                                 | 279 ms: 1.00x faster                                                             |
| tornado_http             | 94.8 ms                                                                | 94.5 ms: 1.00x faster                                                            |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| python_startup_no_site   | 8.96 ms                                                                | 8.95 ms: 1.00x faster                                                            |
| sqlglot_transpile        | 1.59 ms                                                                | 1.60 ms: 1.00x slower                                                            |
| regex_dna                | 226 ms                                                                 | 227 ms: 1.00x slower                                                             |
| xml_etree_generate       | 87.5 ms                                                                | 88.0 ms: 1.01x slower                                                            |
| scimark_sor              | 123 ms                                                                 | 124 ms: 1.01x slower                                                             |
| xml_etree_process        | 60.3 ms                                                                | 60.9 ms: 1.01x slower                                                            |
| json                     | 5.37 ms                                                                | 5.43 ms: 1.01x slower                                                            |
| json_loads               | 28.5 us                                                                | 28.8 us: 1.01x slower                                                            |
| html5lib                 | 67.0 ms                                                                | 67.7 ms: 1.01x slower                                                            |
| asyncio_tcp              | 499 ms                                                                 | 505 ms: 1.01x slower                                                             |
| scimark_lu               | 114 ms                                                                 | 115 ms: 1.01x slower                                                             |
| pickle                   | 11.8 us                                                                | 12.1 us: 1.03x slower                                                            |
| pidigits                 | 191 ms                                                                 | 197 ms: 1.04x slower                                                             |
| pickle_dict              | 34.5 us                                                                | 36.4 us: 1.05x slower                                                            |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (24): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, mypy2, dask, scimark_sparse_mat_mult, sqlglot_parse, asyncio_websockets, gunicorn, generators, docutils, aiohttp, meteor_contest, crypto_pyaes, unpickle, async_tree_io, bench_mp_pool, dulwich_log, json_dumps, telco, async_tree_io_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
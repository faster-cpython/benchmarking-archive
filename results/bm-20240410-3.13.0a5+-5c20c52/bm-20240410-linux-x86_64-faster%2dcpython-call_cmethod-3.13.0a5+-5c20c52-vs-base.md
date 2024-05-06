# Results vs. base

- fork: faster-cpython
- ref: call_cmethod
- machine: linux-x86_64
- commit hash: 5c20c52
- commit date: 2024-04-10
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 272 ms                                                                 | 271 ms: 1.01x faster                                                     |
| chameleon      | 6.94 ms                                                                | 7.03 ms: 1.01x slower                                                    |
| docutils       | 2.83 sec                                                               | 2.84 sec: 1.01x slower                                                   |
| html5lib       | 67.0 ms                                                                | 67.8 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization, async_tree_io_tg, async_tree_memoization_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                                | 88.5 ms: 1.01x faster                                                    |
| pidigits       | 191 ms                                                                 | 190 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                | 24.2 ms: 1.08x faster                                                    |
| regex_dna      | 226 ms                                                                 | 218 ms: 1.04x faster                                                     |
| regex_effbot   | 3.74 ms                                                                | 3.70 ms: 1.01x faster                                                    |
| regex_compile  | 136 ms                                                                 | 135 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_list          | 5.23 us                                                                | 5.07 us: 1.03x faster                                                    |
| xml_etree_iterparse  | 110 ms                                                                 | 107 ms: 1.03x faster                                                     |
| xml_etree_parse      | 163 ms                                                                 | 160 ms: 1.02x faster                                                     |
| pickle               | 11.8 us                                                                | 11.6 us: 1.01x faster                                                    |
| unpickle_pure_python | 225 us                                                                 | 222 us: 1.01x faster                                                     |
| tomli_loads          | 2.18 sec                                                               | 2.15 sec: 1.01x faster                                                   |
| json_loads           | 28.5 us                                                                | 28.4 us: 1.00x faster                                                    |
| xml_etree_generate   | 87.5 ms                                                                | 88.3 ms: 1.01x slower                                                    |
| pickle_dict          | 34.5 us                                                                | 34.9 us: 1.01x slower                                                    |
| xml_etree_process    | 60.3 ms                                                                | 61.1 ms: 1.01x slower                                                    |
| unpickle_list        | 5.09 us                                                                | 5.25 us: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (3): unpickle, json_dumps, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                    |
| python_startup_no_site | 8.96 ms                                                                | 8.95 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 11.1 ms                                                                | 10.8 ms: 1.03x faster                                                    |
| genshi_xml     | 52.3 ms                                                                | 52.9 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8                 | 26.1 ms                                                                | 24.2 ms: 1.08x faster                                                    |
| pycparser                | 1.21 sec                                                               | 1.15 sec: 1.06x faster                                                   |
| scimark_fft              | 374 ms                                                                 | 360 ms: 1.04x faster                                                     |
| regex_dna                | 226 ms                                                                 | 218 ms: 1.04x faster                                                     |
| pickle_list              | 5.23 us                                                                | 5.07 us: 1.03x faster                                                    |
| go                       | 144 ms                                                                 | 140 ms: 1.03x faster                                                     |
| hexiom                   | 6.36 ms                                                                | 6.18 ms: 1.03x faster                                                    |
| mako                     | 11.1 ms                                                                | 10.8 ms: 1.03x faster                                                    |
| xml_etree_iterparse      | 110 ms                                                                 | 107 ms: 1.03x faster                                                     |
| logging_silent           | 103 ns                                                                 | 101 ns: 1.02x faster                                                     |
| gc_traversal             | 3.88 ms                                                                | 3.79 ms: 1.02x faster                                                    |
| comprehensions           | 17.0 us                                                                | 16.6 us: 1.02x faster                                                    |
| fannkuch                 | 397 ms                                                                 | 389 ms: 1.02x faster                                                     |
| richards_super           | 53.9 ms                                                                | 52.9 ms: 1.02x faster                                                    |
| xml_etree_parse          | 163 ms                                                                 | 160 ms: 1.02x faster                                                     |
| nqueens                  | 82.1 ms                                                                | 80.9 ms: 1.02x faster                                                    |
| richards                 | 47.7 ms                                                                | 47.0 ms: 1.02x faster                                                    |
| pickle                   | 11.8 us                                                                | 11.6 us: 1.01x faster                                                    |
| deltablue                | 3.23 ms                                                                | 3.19 ms: 1.01x faster                                                    |
| unpickle_pure_python     | 225 us                                                                 | 222 us: 1.01x faster                                                     |
| tomli_loads              | 2.18 sec                                                               | 2.15 sec: 1.01x faster                                                   |
| scimark_lu               | 114 ms                                                                 | 113 ms: 1.01x faster                                                     |
| regex_effbot             | 3.74 ms                                                                | 3.70 ms: 1.01x faster                                                    |
| pprint_pformat           | 1.55 sec                                                               | 1.53 sec: 1.01x faster                                                   |
| sqlglot_optimize         | 55.7 ms                                                                | 55.2 ms: 1.01x faster                                                    |
| nbody                    | 89.3 ms                                                                | 88.5 ms: 1.01x faster                                                    |
| async_generators         | 449 ms                                                                 | 445 ms: 1.01x faster                                                     |
| scimark_monte_carlo      | 68.0 ms                                                                | 67.4 ms: 1.01x faster                                                    |
| regex_compile            | 136 ms                                                                 | 135 ms: 1.01x faster                                                     |
| sqlglot_normalize        | 112 ms                                                                 | 111 ms: 1.01x faster                                                     |
| deepcopy_reduce          | 3.21 us                                                                | 3.19 us: 1.01x faster                                                    |
| pylint                   | 280 ms                                                                 | 279 ms: 1.01x faster                                                     |
| sqlglot_parse            | 1.29 ms                                                                | 1.29 ms: 1.01x faster                                                    |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.84 sec: 1.01x faster                                                   |
| 2to3                     | 272 ms                                                                 | 271 ms: 1.01x faster                                                     |
| bench_thread_pool        | 838 us                                                                 | 833 us: 1.00x faster                                                     |
| dulwich_log              | 67.2 ms                                                                | 66.9 ms: 1.00x faster                                                    |
| json_loads               | 28.5 us                                                                | 28.4 us: 1.00x faster                                                    |
| pidigits                 | 191 ms                                                                 | 190 ms: 1.00x faster                                                     |
| meteor_contest           | 111 ms                                                                 | 111 ms: 1.00x faster                                                     |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                    |
| python_startup_no_site   | 8.96 ms                                                                | 8.95 ms: 1.00x faster                                                    |
| docutils                 | 2.83 sec                                                               | 2.84 sec: 1.01x slower                                                   |
| logging_simple           | 5.80 us                                                                | 5.85 us: 1.01x slower                                                    |
| scimark_sparse_mat_mult  | 5.25 ms                                                                | 5.30 ms: 1.01x slower                                                    |
| deepcopy_memo            | 38.2 us                                                                | 38.5 us: 1.01x slower                                                    |
| xml_etree_generate       | 87.5 ms                                                                | 88.3 ms: 1.01x slower                                                    |
| coroutines               | 22.3 ms                                                                | 22.5 ms: 1.01x slower                                                    |
| pickle_dict              | 34.5 us                                                                | 34.9 us: 1.01x slower                                                    |
| html5lib                 | 67.0 ms                                                                | 67.8 ms: 1.01x slower                                                    |
| genshi_xml               | 52.3 ms                                                                | 52.9 ms: 1.01x slower                                                    |
| xml_etree_process        | 60.3 ms                                                                | 61.1 ms: 1.01x slower                                                    |
| chameleon                | 6.94 ms                                                                | 7.03 ms: 1.01x slower                                                    |
| deepcopy                 | 354 us                                                                 | 359 us: 1.01x slower                                                     |
| pathlib                  | 18.7 ms                                                                | 19.0 ms: 1.01x slower                                                    |
| crypto_pyaes             | 74.6 ms                                                                | 76.6 ms: 1.03x slower                                                    |
| typing_runtime_protocols | 113 us                                                                 | 117 us: 1.03x slower                                                     |
| unpickle_list            | 5.09 us                                                                | 5.25 us: 1.03x slower                                                    |
| mdp                      | 2.62 sec                                                               | 2.77 sec: 1.06x slower                                                   |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (40): async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization, async_tree_io_tg, mypy2, async_tree_memoization_tg, telco, thrift, sqlite_synth, sympy_str, sympy_expand, asyncio_tcp, float, unpickle, sympy_sum, aiohttp, asyncio_websockets, pprint_safe_repr, pyflate, json, sqlglot_transpile, sympy_integrate, generators, logging_format, coverage, async_tree_io, json_dumps, dask, raytrace, bench_mp_pool, gunicorn, pickle_pure_python, tornado_http, create_gc_cycles, chaos, spectral_norm, genshi_text, scimark_sor

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
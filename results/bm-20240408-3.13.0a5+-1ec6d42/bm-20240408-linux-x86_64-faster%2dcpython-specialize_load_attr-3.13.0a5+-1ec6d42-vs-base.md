# Results vs. base

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 1ec6d42
- commit date: 2024-04-08
- overall geometric mean: 1.00x slower
- HPT reliability: 85.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 272 ms                                                                 | 271 ms: 1.00x faster                                                             |
| chameleon      | 6.94 ms                                                                | 7.01 ms: 1.01x slower                                                            |
| html5lib       | 67.0 ms                                                                | 68.9 ms: 1.03x slower                                                            |
| tornado_http   | 94.8 ms                                                                | 94.5 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg | 339 ms                                                                 | 333 ms: 1.02x faster                                                             |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (7): async_tree_memoization, async_tree_none, async_tree_memoization_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                                 | 190 ms: 1.00x faster                                                             |
| float          | 78.9 ms                                                                | 79.3 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 26.1 ms                                                                | 25.4 ms: 1.03x faster                                                            |
| regex_compile  | 136 ms                                                                 | 136 ms: 1.00x faster                                                             |
| regex_dna      | 226 ms                                                                 | 232 ms: 1.03x slower                                                             |
| regex_effbot   | 3.74 ms                                                                | 3.86 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 110 ms                                                                 | 107 ms: 1.02x faster                                                             |
| unpickle_list        | 5.09 us                                                                | 5.00 us: 1.02x faster                                                            |
| xml_etree_parse      | 163 ms                                                                 | 160 ms: 1.02x faster                                                             |
| tomli_loads          | 2.18 sec                                                               | 2.16 sec: 1.01x faster                                                           |
| xml_etree_generate   | 87.5 ms                                                                | 87.9 ms: 1.00x slower                                                            |
| unpickle_pure_python | 225 us                                                                 | 226 us: 1.01x slower                                                             |
| json_dumps           | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| unpickle             | 15.1 us                                                                | 15.2 us: 1.01x slower                                                            |
| json_loads           | 28.5 us                                                                | 28.7 us: 1.01x slower                                                            |
| pickle_pure_python   | 302 us                                                                 | 305 us: 1.01x slower                                                             |
| pickle               | 11.8 us                                                                | 11.9 us: 1.01x slower                                                            |
| pickle_list          | 5.23 us                                                                | 5.35 us: 1.02x slower                                                            |
| pickle_dict          | 34.5 us                                                                | 35.4 us: 1.02x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| python_startup_no_site | 8.96 ms                                                                | 8.93 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.1 ms                                                                | 11.0 ms: 1.01x faster                                                            |
| genshi_xml     | 52.3 ms                                                                | 52.6 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240408-linux-x86_64-python-e1eeb990bd169491075e-3.13.0a5+-e1eeb99 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| spectral_norm            | 116 ms                                                                 | 112 ms: 1.03x faster                                                             |
| scimark_fft              | 374 ms                                                                 | 362 ms: 1.03x faster                                                             |
| gc_traversal             | 3.88 ms                                                                | 3.76 ms: 1.03x faster                                                            |
| regex_v8                 | 26.1 ms                                                                | 25.4 ms: 1.03x faster                                                            |
| telco                    | 8.75 ms                                                                | 8.54 ms: 1.02x faster                                                            |
| xml_etree_iterparse      | 110 ms                                                                 | 107 ms: 1.02x faster                                                             |
| scimark_sparse_mat_mult  | 5.25 ms                                                                | 5.15 ms: 1.02x faster                                                            |
| unpickle_list            | 5.09 us                                                                | 5.00 us: 1.02x faster                                                            |
| async_tree_none_tg       | 339 ms                                                                 | 333 ms: 1.02x faster                                                             |
| xml_etree_parse          | 163 ms                                                                 | 160 ms: 1.02x faster                                                             |
| pyflate                  | 477 ms                                                                 | 469 ms: 1.02x faster                                                             |
| logging_silent           | 103 ns                                                                 | 102 ns: 1.02x faster                                                             |
| comprehensions           | 17.0 us                                                                | 16.8 us: 1.01x faster                                                            |
| create_gc_cycles         | 1.74 ms                                                                | 1.73 ms: 1.01x faster                                                            |
| fannkuch                 | 397 ms                                                                 | 393 ms: 1.01x faster                                                             |
| coroutines               | 22.3 ms                                                                | 22.1 ms: 1.01x faster                                                            |
| thrift                   | 819 us                                                                 | 811 us: 1.01x faster                                                             |
| tomli_loads              | 2.18 sec                                                               | 2.16 sec: 1.01x faster                                                           |
| richards                 | 47.7 ms                                                                | 47.4 ms: 1.01x faster                                                            |
| mako                     | 11.1 ms                                                                | 11.0 ms: 1.01x faster                                                            |
| richards_super           | 53.9 ms                                                                | 53.7 ms: 1.00x faster                                                            |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                            |
| python_startup_no_site   | 8.96 ms                                                                | 8.93 ms: 1.00x faster                                                            |
| pidigits                 | 191 ms                                                                 | 190 ms: 1.00x faster                                                             |
| regex_compile            | 136 ms                                                                 | 136 ms: 1.00x faster                                                             |
| meteor_contest           | 111 ms                                                                 | 111 ms: 1.00x faster                                                             |
| tornado_http             | 94.8 ms                                                                | 94.5 ms: 1.00x faster                                                            |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.84 sec: 1.00x faster                                                           |
| 2to3                     | 272 ms                                                                 | 271 ms: 1.00x faster                                                             |
| sqlglot_optimize         | 55.7 ms                                                                | 55.9 ms: 1.00x slower                                                            |
| chaos                    | 60.6 ms                                                                | 60.8 ms: 1.00x slower                                                            |
| sqlglot_transpile        | 1.59 ms                                                                | 1.60 ms: 1.00x slower                                                            |
| pylint                   | 280 ms                                                                 | 282 ms: 1.00x slower                                                             |
| xml_etree_generate       | 87.5 ms                                                                | 87.9 ms: 1.00x slower                                                            |
| float                    | 78.9 ms                                                                | 79.3 ms: 1.00x slower                                                            |
| scimark_lu               | 114 ms                                                                 | 114 ms: 1.01x slower                                                             |
| unpickle_pure_python     | 225 us                                                                 | 226 us: 1.01x slower                                                             |
| genshi_xml               | 52.3 ms                                                                | 52.6 ms: 1.01x slower                                                            |
| dulwich_log              | 67.2 ms                                                                | 67.6 ms: 1.01x slower                                                            |
| json_dumps               | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                            |
| unpickle                 | 15.1 us                                                                | 15.2 us: 1.01x slower                                                            |
| json_loads               | 28.5 us                                                                | 28.7 us: 1.01x slower                                                            |
| pprint_pformat           | 1.55 sec                                                               | 1.56 sec: 1.01x slower                                                           |
| typing_runtime_protocols | 113 us                                                                 | 114 us: 1.01x slower                                                             |
| sqlglot_normalize        | 112 ms                                                                 | 112 ms: 1.01x slower                                                             |
| generators               | 29.7 ms                                                                | 30.0 ms: 1.01x slower                                                            |
| sympy_integrate          | 20.4 ms                                                                | 20.6 ms: 1.01x slower                                                            |
| chameleon                | 6.94 ms                                                                | 7.01 ms: 1.01x slower                                                            |
| pickle_pure_python       | 302 us                                                                 | 305 us: 1.01x slower                                                             |
| pickle                   | 11.8 us                                                                | 11.9 us: 1.01x slower                                                            |
| deltablue                | 3.23 ms                                                                | 3.27 ms: 1.01x slower                                                            |
| logging_simple           | 5.80 us                                                                | 5.88 us: 1.01x slower                                                            |
| pprint_safe_repr         | 750 ms                                                                 | 761 ms: 1.01x slower                                                             |
| raytrace                 | 262 ms                                                                 | 265 ms: 1.01x slower                                                             |
| mdp                      | 2.62 sec                                                               | 2.65 sec: 1.01x slower                                                           |
| scimark_sor              | 123 ms                                                                 | 125 ms: 1.02x slower                                                             |
| hexiom                   | 6.36 ms                                                                | 6.47 ms: 1.02x slower                                                            |
| nqueens                  | 82.1 ms                                                                | 83.7 ms: 1.02x slower                                                            |
| crypto_pyaes             | 74.6 ms                                                                | 76.0 ms: 1.02x slower                                                            |
| pickle_list              | 5.23 us                                                                | 5.35 us: 1.02x slower                                                            |
| logging_format           | 6.39 us                                                                | 6.55 us: 1.02x slower                                                            |
| pickle_dict              | 34.5 us                                                                | 35.4 us: 1.02x slower                                                            |
| regex_dna                | 226 ms                                                                 | 232 ms: 1.03x slower                                                             |
| asyncio_tcp              | 499 ms                                                                 | 513 ms: 1.03x slower                                                             |
| html5lib                 | 67.0 ms                                                                | 68.9 ms: 1.03x slower                                                            |
| deepcopy                 | 354 us                                                                 | 364 us: 1.03x slower                                                             |
| regex_effbot             | 3.74 ms                                                                | 3.86 ms: 1.03x slower                                                            |
| deepcopy_reduce          | 3.21 us                                                                | 3.32 us: 1.03x slower                                                            |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (31): async_tree_memoization, async_tree_none, async_tree_memoization_tg, async_tree_io_tg, dask, sympy_expand, pycparser, sqlite_synth, asyncio_websockets, async_tree_cpu_io_mixed, async_generators, mypy2, async_tree_cpu_io_mixed_tg, bench_mp_pool, gunicorn, scimark_monte_carlo, genshi_text, sympy_sum, bench_thread_pool, aiohttp, go, json, nbody, deepcopy_memo, docutils, sqlglot_parse, xml_etree_process, sympy_str, coverage, pathlib, async_tree_io

# HPT report

- Reliability score: 85.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
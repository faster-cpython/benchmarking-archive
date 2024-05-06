# Results vs. base

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: a7b858b
- commit date: 2024-05-02
- overall geometric mean: 1.00x faster
- HPT reliability: 62.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6+-f8e088d | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 269 ms                                                                 | 272 ms: 1.01x slower                                                             |
| chameleon      | 7.25 ms                                                                | 7.22 ms: 1.00x faster                                                            |
| docutils       | 2.80 sec                                                               | 2.82 sec: 1.01x slower                                                           |
| html5lib       | 68.9 ms                                                                | 70.3 ms: 1.02x slower                                                            |
| tornado_http   | 93.6 ms                                                                | 93.2 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io, async_tree_none, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6+-f8e088d | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 91.0 ms                                                                | 89.5 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6+-f8e088d | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.90 ms                                                                | 3.62 ms: 1.08x faster                                                            |
| regex_v8       | 26.1 ms                                                                | 24.6 ms: 1.06x faster                                                            |
| regex_dna      | 232 ms                                                                 | 224 ms: 1.04x faster                                                             |
| regex_compile  | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6+-f8e088d | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_generate   | 89.2 ms                                                                | 88.0 ms: 1.01x faster                                                            |
| tomli_loads          | 2.16 sec                                                               | 2.13 sec: 1.01x faster                                                           |
| xml_etree_process    | 61.6 ms                                                                | 61.0 ms: 1.01x faster                                                            |
| json_dumps           | 10.6 ms                                                                | 10.6 ms: 1.01x faster                                                            |
| pickle               | 12.0 us                                                                | 11.9 us: 1.00x faster                                                            |
| unpickle_pure_python | 218 us                                                                 | 220 us: 1.01x slower                                                             |
| unpickle_list        | 5.13 us                                                                | 5.19 us: 1.01x slower                                                            |
| pickle_list          | 5.08 us                                                                | 5.16 us: 1.02x slower                                                            |
| json_loads           | 27.5 us                                                                | 28.5 us: 1.04x slower                                                            |
| pickle_pure_python   | 306 us                                                                 | 320 us: 1.05x slower                                                             |
| pickle_dict          | 33.8 us                                                                | 35.9 us: 1.06x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (3): unpickle, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6+-f8e088d | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 35.3 ms                                                                | 34.7 ms: 1.02x faster                                                            |
| mako            | 11.1 ms                                                                | 11.3 ms: 1.02x slower                                                            |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240502-linux-x86_64-python-f8e088df2a87f613ee23-3.13.0a6+-f8e088d | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| go                       | 146 ms                                                                 | 119 ms: 1.22x faster                                                             |
| regex_effbot             | 3.90 ms                                                                | 3.62 ms: 1.08x faster                                                            |
| regex_v8                 | 26.1 ms                                                                | 24.6 ms: 1.06x faster                                                            |
| coroutines               | 23.1 ms                                                                | 22.2 ms: 1.04x faster                                                            |
| pycparser                | 1.20 sec                                                               | 1.15 sec: 1.04x faster                                                           |
| regex_dna                | 232 ms                                                                 | 224 ms: 1.04x faster                                                             |
| gc_traversal             | 3.94 ms                                                                | 3.81 ms: 1.04x faster                                                            |
| djangocms                | 31.8 us                                                                | 31.2 us: 1.02x faster                                                            |
| logging_simple           | 5.81 us                                                                | 5.70 us: 1.02x faster                                                            |
| spectral_norm            | 114 ms                                                                 | 112 ms: 1.02x faster                                                             |
| scimark_fft              | 375 ms                                                                 | 368 ms: 1.02x faster                                                             |
| typing_runtime_protocols | 168 us                                                                 | 165 us: 1.02x faster                                                             |
| nbody                    | 91.0 ms                                                                | 89.5 ms: 1.02x faster                                                            |
| raytrace                 | 266 ms                                                                 | 262 ms: 1.02x faster                                                             |
| django_template          | 35.3 ms                                                                | 34.7 ms: 1.02x faster                                                            |
| xml_etree_generate       | 89.2 ms                                                                | 88.0 ms: 1.01x faster                                                            |
| nqueens                  | 80.8 ms                                                                | 79.6 ms: 1.01x faster                                                            |
| sympy_sum                | 156 ms                                                                 | 155 ms: 1.01x faster                                                             |
| sqlite_synth             | 2.94 us                                                                | 2.90 us: 1.01x faster                                                            |
| tomli_loads              | 2.16 sec                                                               | 2.13 sec: 1.01x faster                                                           |
| xml_etree_process        | 61.6 ms                                                                | 61.0 ms: 1.01x faster                                                            |
| hexiom                   | 6.27 ms                                                                | 6.22 ms: 1.01x faster                                                            |
| pathlib                  | 17.7 ms                                                                | 17.6 ms: 1.01x faster                                                            |
| logging_silent           | 102 ns                                                                 | 101 ns: 1.01x faster                                                             |
| logging_format           | 6.38 us                                                                | 6.33 us: 1.01x faster                                                            |
| json_dumps               | 10.6 ms                                                                | 10.6 ms: 1.01x faster                                                            |
| fannkuch                 | 397 ms                                                                 | 394 ms: 1.01x faster                                                             |
| meteor_contest           | 109 ms                                                                 | 108 ms: 1.01x faster                                                             |
| sympy_integrate          | 20.4 ms                                                                | 20.3 ms: 1.01x faster                                                            |
| async_generators         | 444 ms                                                                 | 442 ms: 1.01x faster                                                             |
| tornado_http             | 93.6 ms                                                                | 93.2 ms: 1.00x faster                                                            |
| chameleon                | 7.25 ms                                                                | 7.22 ms: 1.00x faster                                                            |
| dulwich_log              | 65.7 ms                                                                | 65.5 ms: 1.00x faster                                                            |
| richards_super           | 53.7 ms                                                                | 53.5 ms: 1.00x faster                                                            |
| pickle                   | 12.0 us                                                                | 11.9 us: 1.00x faster                                                            |
| deepcopy_memo            | 37.7 us                                                                | 37.6 us: 1.00x faster                                                            |
| asyncio_tcp_ssl          | 1.84 sec                                                               | 1.84 sec: 1.00x faster                                                           |
| asyncio_tcp              | 507 ms                                                                 | 506 ms: 1.00x faster                                                             |
| bench_thread_pool        | 830 us                                                                 | 828 us: 1.00x faster                                                             |
| richards                 | 47.3 ms                                                                | 47.4 ms: 1.00x slower                                                            |
| deepcopy                 | 357 us                                                                 | 358 us: 1.00x slower                                                             |
| sympy_expand             | 471 ms                                                                 | 473 ms: 1.00x slower                                                             |
| pyflate                  | 468 ms                                                                 | 470 ms: 1.01x slower                                                             |
| pprint_pformat           | 1.54 sec                                                               | 1.55 sec: 1.01x slower                                                           |
| scimark_lu               | 115 ms                                                                 | 116 ms: 1.01x slower                                                             |
| regex_compile            | 134 ms                                                                 | 135 ms: 1.01x slower                                                             |
| docutils                 | 2.80 sec                                                               | 2.82 sec: 1.01x slower                                                           |
| sqlglot_transpile        | 1.59 ms                                                                | 1.60 ms: 1.01x slower                                                            |
| pprint_safe_repr         | 755 ms                                                                 | 761 ms: 1.01x slower                                                             |
| sqlglot_parse            | 1.28 ms                                                                | 1.29 ms: 1.01x slower                                                            |
| generators               | 29.2 ms                                                                | 29.4 ms: 1.01x slower                                                            |
| create_gc_cycles         | 1.75 ms                                                                | 1.76 ms: 1.01x slower                                                            |
| 2to3                     | 269 ms                                                                 | 272 ms: 1.01x slower                                                             |
| unpickle_pure_python     | 218 us                                                                 | 220 us: 1.01x slower                                                             |
| unpickle_list            | 5.13 us                                                                | 5.19 us: 1.01x slower                                                            |
| sqlglot_optimize         | 54.9 ms                                                                | 55.5 ms: 1.01x slower                                                            |
| pickle_list              | 5.08 us                                                                | 5.16 us: 1.02x slower                                                            |
| scimark_sor              | 131 ms                                                                 | 134 ms: 1.02x slower                                                             |
| mako                     | 11.1 ms                                                                | 11.3 ms: 1.02x slower                                                            |
| comprehensions           | 16.3 us                                                                | 16.7 us: 1.02x slower                                                            |
| scimark_sparse_mat_mult  | 5.09 ms                                                                | 5.20 ms: 1.02x slower                                                            |
| html5lib                 | 68.9 ms                                                                | 70.3 ms: 1.02x slower                                                            |
| coverage                 | 91.9 ms                                                                | 93.8 ms: 1.02x slower                                                            |
| json                     | 5.18 ms                                                                | 5.33 ms: 1.03x slower                                                            |
| json_loads               | 27.5 us                                                                | 28.5 us: 1.04x slower                                                            |
| pickle_pure_python       | 306 us                                                                 | 320 us: 1.05x slower                                                             |
| pickle_dict              | 33.8 us                                                                | 35.9 us: 1.06x slower                                                            |
| scimark_monte_carlo      | 69.1 ms                                                                | 74.2 ms: 1.07x slower                                                            |
| mdp                      | 2.59 sec                                                               | 2.79 sec: 1.08x slower                                                           |
| crypto_pyaes             | 76.5 ms                                                                | 83.7 ms: 1.09x slower                                                            |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (31): unpickle, async_tree_cpu_io_mixed, pylint, gunicorn, aiohttp, genshi_text, async_tree_memoization, async_tree_io, deepcopy_reduce, float, async_tree_none, bench_mp_pool, pidigits, python_startup, xml_etree_iterparse, asyncio_websockets, python_startup_no_site, chaos, sqlglot_normalize, deltablue, genshi_xml, thrift, dask, mypy2, telco, sympy_str, xml_etree_parse, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg

# HPT report

- Reliability score: 62.94% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
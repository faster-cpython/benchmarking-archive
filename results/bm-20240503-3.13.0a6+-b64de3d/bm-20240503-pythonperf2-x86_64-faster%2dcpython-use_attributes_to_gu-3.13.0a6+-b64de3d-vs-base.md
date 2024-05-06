# Results vs. base

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: b64de3d
- commit date: 2024-05-03
- overall geometric mean: 1.00x slower
- HPT reliability: 85.67%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| chameleon      | 7.42 ms                                                                      | 7.52 ms: 1.01x slower                                                                  |
| docutils       | 3.01 sec                                                                     | 3.02 sec: 1.00x slower                                                                 |
| html5lib       | 74.0 ms                                                                      | 75.9 ms: 1.03x slower                                                                  |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_none, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 87.7 ms                                                                      | 91.0 ms: 1.04x slower                                                                  |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_v8       | 25.9 ms                                                                      | 25.6 ms: 1.01x faster                                                                  |
| regex_effbot   | 3.56 ms                                                                      | 3.52 ms: 1.01x faster                                                                  |
| regex_compile  | 144 ms                                                                       | 143 ms: 1.00x faster                                                                   |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| unpickle_pure_python | 229 us                                                                       | 213 us: 1.07x faster                                                                   |
| unpickle_list        | 4.83 us                                                                      | 4.68 us: 1.03x faster                                                                  |
| json_loads           | 25.0 us                                                                      | 24.6 us: 1.02x faster                                                                  |
| xml_etree_process    | 59.9 ms                                                                      | 59.1 ms: 1.01x faster                                                                  |
| pickle_list          | 4.54 us                                                                      | 4.49 us: 1.01x faster                                                                  |
| xml_etree_generate   | 85.3 ms                                                                      | 84.7 ms: 1.01x faster                                                                  |
| pickle_dict          | 33.1 us                                                                      | 32.9 us: 1.01x faster                                                                  |
| json_dumps           | 10.9 ms                                                                      | 11.1 ms: 1.01x slower                                                                  |
| xml_etree_iterparse  | 102 ms                                                                       | 104 ms: 1.02x slower                                                                   |
| unpickle             | 14.9 us                                                                      | 15.1 us: 1.02x slower                                                                  |
| xml_etree_parse      | 141 ms                                                                       | 145 ms: 1.03x slower                                                                   |
| pickle               | 10.5 us                                                                      | 10.9 us: 1.03x slower                                                                  |
| pickle_pure_python   | 315 us                                                                       | 326 us: 1.03x slower                                                                   |
| tomli_loads          | 2.25 sec                                                                     | 2.38 sec: 1.06x slower                                                                 |
| Geometric mean       | (ref)                                                                        | 1.00x slower                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup_no_site | 8.81 ms                                                                      | 8.80 ms: 1.00x faster                                                                  |
| python_startup         | 12.8 ms                                                                      | 12.8 ms: 1.00x slower                                                                  |
| Geometric mean         | (ref)                                                                        | 1.00x faster                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|-----------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| genshi_xml      | 55.0 ms                                                                      | 53.3 ms: 1.03x faster                                                                  |
| genshi_text     | 25.2 ms                                                                      | 24.8 ms: 1.02x faster                                                                  |
| mako            | 10.3 ms                                                                      | 10.4 ms: 1.01x slower                                                                  |
| django_template | 38.7 ms                                                                      | 39.6 ms: 1.02x slower                                                                  |
| Geometric mean  | (ref)                                                                        | 1.00x faster                                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240503-pythonperf2-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|--------------------------|:----------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| go                       | 160 ms                                                                       | 134 ms: 1.19x faster                                                                   |
| unpickle_pure_python     | 229 us                                                                       | 213 us: 1.07x faster                                                                   |
| coverage                 | 82.6 ms                                                                      | 77.4 ms: 1.07x faster                                                                  |
| pyflate                  | 497 ms                                                                       | 474 ms: 1.05x faster                                                                   |
| genshi_xml               | 55.0 ms                                                                      | 53.3 ms: 1.03x faster                                                                  |
| unpickle_list            | 4.83 us                                                                      | 4.68 us: 1.03x faster                                                                  |
| coroutines               | 22.0 ms                                                                      | 21.5 ms: 1.03x faster                                                                  |
| richards                 | 52.4 ms                                                                      | 51.2 ms: 1.02x faster                                                                  |
| richards_super           | 59.9 ms                                                                      | 58.8 ms: 1.02x faster                                                                  |
| genshi_text              | 25.2 ms                                                                      | 24.8 ms: 1.02x faster                                                                  |
| json_loads               | 25.0 us                                                                      | 24.6 us: 1.02x faster                                                                  |
| json                     | 5.47 ms                                                                      | 5.38 ms: 1.02x faster                                                                  |
| pycparser                | 1.28 sec                                                                     | 1.26 sec: 1.01x faster                                                                 |
| mdp                      | 2.54 sec                                                                     | 2.50 sec: 1.01x faster                                                                 |
| xml_etree_process        | 59.9 ms                                                                      | 59.1 ms: 1.01x faster                                                                  |
| regex_v8                 | 25.9 ms                                                                      | 25.6 ms: 1.01x faster                                                                  |
| pprint_safe_repr         | 825 ms                                                                       | 814 ms: 1.01x faster                                                                   |
| dulwich_log              | 67.0 ms                                                                      | 66.2 ms: 1.01x faster                                                                  |
| pickle_list              | 4.54 us                                                                      | 4.49 us: 1.01x faster                                                                  |
| regex_effbot             | 3.56 ms                                                                      | 3.52 ms: 1.01x faster                                                                  |
| aiohttp                  | 1.10 ms                                                                      | 1.09 ms: 1.01x faster                                                                  |
| sqlglot_parse            | 1.41 ms                                                                      | 1.39 ms: 1.01x faster                                                                  |
| generators               | 33.9 ms                                                                      | 33.6 ms: 1.01x faster                                                                  |
| pprint_pformat           | 1.67 sec                                                                     | 1.66 sec: 1.01x faster                                                                 |
| xml_etree_generate       | 85.3 ms                                                                      | 84.7 ms: 1.01x faster                                                                  |
| pickle_dict              | 33.1 us                                                                      | 32.9 us: 1.01x faster                                                                  |
| asyncio_tcp              | 375 ms                                                                       | 373 ms: 1.01x faster                                                                   |
| sqlglot_transpile        | 1.79 ms                                                                      | 1.78 ms: 1.00x faster                                                                  |
| regex_compile            | 144 ms                                                                       | 143 ms: 1.00x faster                                                                   |
| asyncio_tcp_ssl          | 1.58 sec                                                                     | 1.58 sec: 1.00x faster                                                                 |
| python_startup_no_site   | 8.81 ms                                                                      | 8.80 ms: 1.00x faster                                                                  |
| python_startup           | 12.8 ms                                                                      | 12.8 ms: 1.00x slower                                                                  |
| sqlglot_normalize        | 121 ms                                                                       | 122 ms: 1.00x slower                                                                   |
| pathlib                  | 17.4 ms                                                                      | 17.5 ms: 1.00x slower                                                                  |
| docutils                 | 3.01 sec                                                                     | 3.02 sec: 1.00x slower                                                                 |
| sympy_str                | 297 ms                                                                       | 298 ms: 1.00x slower                                                                   |
| sympy_expand             | 504 ms                                                                       | 506 ms: 1.01x slower                                                                   |
| telco                    | 8.22 ms                                                                      | 8.27 ms: 1.01x slower                                                                  |
| deepcopy_reduce          | 3.40 us                                                                      | 3.43 us: 1.01x slower                                                                  |
| raytrace                 | 267 ms                                                                       | 270 ms: 1.01x slower                                                                   |
| asyncio_websockets       | 390 ms                                                                       | 395 ms: 1.01x slower                                                                   |
| deltablue                | 3.42 ms                                                                      | 3.46 ms: 1.01x slower                                                                  |
| sqlglot_optimize         | 59.4 ms                                                                      | 60.1 ms: 1.01x slower                                                                  |
| json_dumps               | 10.9 ms                                                                      | 11.1 ms: 1.01x slower                                                                  |
| chameleon                | 7.42 ms                                                                      | 7.52 ms: 1.01x slower                                                                  |
| deepcopy_memo            | 37.0 us                                                                      | 37.5 us: 1.01x slower                                                                  |
| mako                     | 10.3 ms                                                                      | 10.4 ms: 1.01x slower                                                                  |
| scimark_lu               | 98.0 ms                                                                      | 99.5 ms: 1.02x slower                                                                  |
| async_generators         | 363 ms                                                                       | 368 ms: 1.02x slower                                                                   |
| xml_etree_iterparse      | 102 ms                                                                       | 104 ms: 1.02x slower                                                                   |
| unpickle                 | 14.9 us                                                                      | 15.1 us: 1.02x slower                                                                  |
| hexiom                   | 6.27 ms                                                                      | 6.38 ms: 1.02x slower                                                                  |
| scimark_sparse_mat_mult  | 4.22 ms                                                                      | 4.29 ms: 1.02x slower                                                                  |
| typing_runtime_protocols | 171 us                                                                       | 175 us: 1.02x slower                                                                   |
| spectral_norm            | 98.9 ms                                                                      | 101 ms: 1.02x slower                                                                   |
| django_template          | 38.7 ms                                                                      | 39.6 ms: 1.02x slower                                                                  |
| html5lib                 | 74.0 ms                                                                      | 75.9 ms: 1.03x slower                                                                  |
| scimark_fft              | 309 ms                                                                       | 317 ms: 1.03x slower                                                                   |
| nqueens                  | 87.8 ms                                                                      | 90.2 ms: 1.03x slower                                                                  |
| xml_etree_parse          | 141 ms                                                                       | 145 ms: 1.03x slower                                                                   |
| meteor_contest           | 127 ms                                                                       | 131 ms: 1.03x slower                                                                   |
| pickle                   | 10.5 us                                                                      | 10.9 us: 1.03x slower                                                                  |
| pickle_pure_python       | 315 us                                                                       | 326 us: 1.03x slower                                                                   |
| create_gc_cycles         | 1.94 ms                                                                      | 2.01 ms: 1.04x slower                                                                  |
| nbody                    | 87.7 ms                                                                      | 91.0 ms: 1.04x slower                                                                  |
| tomli_loads              | 2.25 sec                                                                     | 2.38 sec: 1.06x slower                                                                 |
| logging_simple           | 6.42 us                                                                      | 6.81 us: 1.06x slower                                                                  |
| gc_traversal             | 4.54 ms                                                                      | 4.82 ms: 1.06x slower                                                                  |
| logging_format           | 7.16 us                                                                      | 7.67 us: 1.07x slower                                                                  |
| scimark_monte_carlo      | 68.1 ms                                                                      | 73.8 ms: 1.08x slower                                                                  |
| scimark_sor              | 120 ms                                                                       | 130 ms: 1.09x slower                                                                   |
| crypto_pyaes             | 74.2 ms                                                                      | 82.0 ms: 1.10x slower                                                                  |
| Geometric mean           | (ref)                                                                        | 1.00x slower                                                                           |

Benchmark hidden because not significant (29): async_tree_io, gunicorn, tornado_http, fannkuch, chaos, sympy_sum, async_tree_none, sympy_integrate, pidigits, 2to3, deepcopy, comprehensions, regex_dna, dask, logging_silent, pylint, thrift, async_tree_cpu_io_mixed, float, sqlite_synth, async_tree_memoization, async_tree_none_tg, flaskblogging, mypy2, bench_thread_pool, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, bench_mp_pool

# HPT report

- Reliability score: 85.67% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x
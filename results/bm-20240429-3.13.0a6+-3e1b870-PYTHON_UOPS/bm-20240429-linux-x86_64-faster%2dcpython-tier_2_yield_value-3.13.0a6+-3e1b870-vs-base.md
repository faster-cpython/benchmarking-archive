# Results vs. base

- fork: faster-cpython
- ref: tier_2_yield_value
- machine: linux-x86_64
- commit hash: 3e1b870
- commit date: 2024-04-29
- overall geometric mean: 1.00x slower
- HPT reliability: 99.75%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 361 ms                                                                 | 361 ms: 1.00x slower                                                           |
| chameleon      | 8.68 ms                                                                | 8.81 ms: 1.01x slower                                                          |
| html5lib       | 79.8 ms                                                                | 81.2 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_io, async_tree_none, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 198 ms                                                                 | 197 ms: 1.01x faster                                                           |
| float          | 122 ms                                                                 | 129 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                   |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.73 ms                                                                | 3.74 ms: 1.00x slower                                                          |
| regex_compile  | 220 ms                                                                 | 223 ms: 1.01x slower                                                           |
| regex_v8       | 25.6 ms                                                                | 26.4 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle               | 12.0 us                                                                | 11.6 us: 1.03x faster                                                          |
| unpickle             | 15.3 us                                                                | 14.9 us: 1.02x faster                                                          |
| xml_etree_generate   | 104 ms                                                                 | 103 ms: 1.01x faster                                                           |
| json_dumps           | 10.8 ms                                                                | 10.7 ms: 1.01x faster                                                          |
| pickle_dict          | 35.3 us                                                                | 35.1 us: 1.00x faster                                                          |
| unpickle_pure_python | 396 us                                                                 | 398 us: 1.01x slower                                                           |
| xml_etree_iterparse  | 126 ms                                                                 | 127 ms: 1.01x slower                                                           |
| xml_etree_parse      | 151 ms                                                                 | 154 ms: 1.02x slower                                                           |
| unpickle_list        | 5.13 us                                                                | 5.33 us: 1.04x slower                                                          |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                   |

Benchmark hidden because not significant (5): pickle_pure_python, json_loads, xml_etree_process, tomli_loads, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                          |
| python_startup_no_site | 7.19 ms                                                                | 7.12 ms: 1.01x faster                                                          |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_text     | 39.3 ms                                                                | 38.7 ms: 1.01x faster                                                          |
| django_template | 47.3 ms                                                                | 47.5 ms: 1.00x slower                                                          |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                                   |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|--------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| gc_traversal             | 3.93 ms                                                                | 3.61 ms: 1.09x faster                                                          |
| pickle                   | 12.0 us                                                                | 11.6 us: 1.03x faster                                                          |
| unpickle                 | 15.3 us                                                                | 14.9 us: 1.02x faster                                                          |
| coroutines               | 24.5 ms                                                                | 24.1 ms: 1.02x faster                                                          |
| genshi_text              | 39.3 ms                                                                | 38.7 ms: 1.01x faster                                                          |
| create_gc_cycles         | 1.81 ms                                                                | 1.78 ms: 1.01x faster                                                          |
| sqlite_synth             | 3.11 us                                                                | 3.08 us: 1.01x faster                                                          |
| xml_etree_generate       | 104 ms                                                                 | 103 ms: 1.01x faster                                                           |
| python_startup           | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                                          |
| python_startup_no_site   | 7.19 ms                                                                | 7.12 ms: 1.01x faster                                                          |
| thrift                   | 854 us                                                                 | 847 us: 1.01x faster                                                           |
| nbody                    | 198 ms                                                                 | 197 ms: 1.01x faster                                                           |
| json_dumps               | 10.8 ms                                                                | 10.7 ms: 1.01x faster                                                          |
| scimark_sor              | 178 ms                                                                 | 176 ms: 1.01x faster                                                           |
| sqlglot_normalize        | 142 ms                                                                 | 141 ms: 1.01x faster                                                           |
| pickle_dict              | 35.3 us                                                                | 35.1 us: 1.00x faster                                                          |
| asyncio_tcp_ssl          | 1.88 sec                                                               | 1.87 sec: 1.00x faster                                                         |
| sympy_integrate          | 27.7 ms                                                                | 27.6 ms: 1.00x faster                                                          |
| sqlglot_optimize         | 73.5 ms                                                                | 73.3 ms: 1.00x faster                                                          |
| 2to3                     | 361 ms                                                                 | 361 ms: 1.00x slower                                                           |
| scimark_fft              | 596 ms                                                                 | 597 ms: 1.00x slower                                                           |
| pprint_pformat           | 2.65 sec                                                               | 2.66 sec: 1.00x slower                                                         |
| bench_thread_pool        | 973 us                                                                 | 976 us: 1.00x slower                                                           |
| raytrace                 | 376 ms                                                                 | 377 ms: 1.00x slower                                                           |
| regex_effbot             | 3.73 ms                                                                | 3.74 ms: 1.00x slower                                                          |
| pprint_safe_repr         | 1.28 sec                                                               | 1.29 sec: 1.00x slower                                                         |
| django_template          | 47.3 ms                                                                | 47.5 ms: 1.00x slower                                                          |
| go                       | 260 ms                                                                 | 261 ms: 1.00x slower                                                           |
| deepcopy                 | 409 us                                                                 | 411 us: 1.01x slower                                                           |
| unpickle_pure_python     | 396 us                                                                 | 398 us: 1.01x slower                                                           |
| dulwich_log              | 77.4 ms                                                                | 77.9 ms: 1.01x slower                                                          |
| sympy_str                | 360 ms                                                                 | 362 ms: 1.01x slower                                                           |
| scimark_monte_carlo      | 134 ms                                                                 | 135 ms: 1.01x slower                                                           |
| logging_silent           | 108 ns                                                                 | 108 ns: 1.01x slower                                                           |
| comprehensions           | 37.2 us                                                                | 37.5 us: 1.01x slower                                                          |
| typing_runtime_protocols | 217 us                                                                 | 219 us: 1.01x slower                                                           |
| generators               | 31.8 ms                                                                | 32.1 ms: 1.01x slower                                                          |
| logging_format           | 7.88 us                                                                | 7.96 us: 1.01x slower                                                          |
| scimark_lu               | 201 ms                                                                 | 203 ms: 1.01x slower                                                           |
| meteor_contest           | 143 ms                                                                 | 144 ms: 1.01x slower                                                           |
| nqueens                  | 151 ms                                                                 | 153 ms: 1.01x slower                                                           |
| xml_etree_iterparse      | 126 ms                                                                 | 127 ms: 1.01x slower                                                           |
| hexiom                   | 15.0 ms                                                                | 15.2 ms: 1.01x slower                                                          |
| regex_compile            | 220 ms                                                                 | 223 ms: 1.01x slower                                                           |
| deepcopy_memo            | 50.1 us                                                                | 50.7 us: 1.01x slower                                                          |
| chameleon                | 8.68 ms                                                                | 8.81 ms: 1.01x slower                                                          |
| async_generators         | 496 ms                                                                 | 504 ms: 1.02x slower                                                           |
| html5lib                 | 79.8 ms                                                                | 81.2 ms: 1.02x slower                                                          |
| logging_simple           | 7.08 us                                                                | 7.21 us: 1.02x slower                                                          |
| fannkuch                 | 693 ms                                                                 | 705 ms: 1.02x slower                                                           |
| spectral_norm            | 211 ms                                                                 | 215 ms: 1.02x slower                                                           |
| asyncio_tcp              | 530 ms                                                                 | 539 ms: 1.02x slower                                                           |
| xml_etree_parse          | 151 ms                                                                 | 154 ms: 1.02x slower                                                           |
| pycparser                | 1.34 sec                                                               | 1.38 sec: 1.03x slower                                                         |
| crypto_pyaes             | 122 ms                                                                 | 125 ms: 1.03x slower                                                           |
| regex_v8                 | 25.6 ms                                                                | 26.4 ms: 1.03x slower                                                          |
| unpickle_list            | 5.13 us                                                                | 5.33 us: 1.04x slower                                                          |
| pyflate                  | 828 ms                                                                 | 862 ms: 1.04x slower                                                           |
| float                    | 122 ms                                                                 | 129 ms: 1.05x slower                                                           |
| mdp                      | 3.13 sec                                                               | 3.33 sec: 1.06x slower                                                         |
| scimark_sparse_mat_mult  | 8.26 ms                                                                | 8.81 ms: 1.07x slower                                                          |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                                   |

Benchmark hidden because not significant (40): async_tree_io_tg, tornado_http, coverage, sympy_expand, pylint, pickle_pure_python, json_loads, xml_etree_process, dask, tomli_loads, aiohttp, mako, gunicorn, bench_mp_pool, asyncio_websockets, richards_super, telco, sqlglot_parse, json, sqlglot_transpile, mypy2, pidigits, deepcopy_reduce, genshi_xml, docutils, async_tree_none_tg, regex_dna, async_tree_memoization, chaos, pathlib, async_tree_io, async_tree_none, richards, sympy_sum, djangocms, pickle_list, async_tree_memoization_tg, deltablue, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

# HPT report

- Reliability score: 99.75% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x
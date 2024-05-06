# Results vs. base

- fork: gvanrossum
- ref: tier2_flag
- machine: linux-x86_64
- commit hash: 8cb71dd
- commit date: 2024-04-26
- overall geometric mean: 1.01x faster
- HPT reliability: 98.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 269 ms                                                                 | 267 ms: 1.01x faster                                             |
| chameleon      | 7.05 ms                                                                | 6.96 ms: 1.01x faster                                            |
| html5lib       | 67.6 ms                                                                | 66.8 ms: 1.01x faster                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                     |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none, async_tree_memoization_tg, async_tree_none_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 88.7 ms                                                                | 85.7 ms: 1.03x faster                                            |
| pidigits       | 197 ms                                                                 | 193 ms: 1.02x faster                                             |
| float          | 78.9 ms                                                                | 77.5 ms: 1.02x faster                                            |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 133 ms                                                                 | 132 ms: 1.01x faster                                             |
| regex_v8       | 25.8 ms                                                                | 25.7 ms: 1.01x faster                                            |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                     |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| unpickle_list        | 5.37 us                                                                | 5.23 us: 1.03x faster                                            |
| json_loads           | 28.1 us                                                                | 27.8 us: 1.01x faster                                            |
| json_dumps           | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                            |
| unpickle_pure_python | 215 us                                                                 | 214 us: 1.01x faster                                             |
| pickle_pure_python   | 303 us                                                                 | 305 us: 1.01x slower                                             |
| pickle_dict          | 34.5 us                                                                | 34.7 us: 1.01x slower                                            |
| pickle               | 11.6 us                                                                | 11.8 us: 1.02x slower                                            |
| unpickle             | 15.3 us                                                                | 16.1 us: 1.06x slower                                            |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                     |

Benchmark hidden because not significant (6): tomli_loads, xml_etree_iterparse, xml_etree_process, pickle_list, xml_etree_generate, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup_no_site | 7.11 ms                                                                | 7.09 ms: 1.00x faster                                            |
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                            |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| genshi_xml      | 52.7 ms                                                                | 51.5 ms: 1.02x faster                                            |
| mako            | 10.9 ms                                                                | 10.7 ms: 1.02x faster                                            |
| genshi_text     | 23.5 ms                                                                | 23.2 ms: 1.01x faster                                            |
| django_template | 35.1 ms                                                                | 34.8 ms: 1.01x faster                                            |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                     |

All benchmarks:
===============

| Benchmark                | bm-20240426-linux-x86_64-python-b43c7e1070e515b3e940-3.13.0a6+-b43c7e1 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|--------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------:|
| scimark_sor              | 130 ms                                                                 | 119 ms: 1.09x faster                                             |
| hexiom                   | 6.32 ms                                                                | 5.95 ms: 1.06x faster                                            |
| pyflate                  | 479 ms                                                                 | 453 ms: 1.06x faster                                             |
| deepcopy_memo            | 38.3 us                                                                | 36.8 us: 1.04x faster                                            |
| nbody                    | 88.7 ms                                                                | 85.7 ms: 1.03x faster                                            |
| logging_silent           | 103 ns                                                                 | 99.7 ns: 1.03x faster                                            |
| deepcopy                 | 361 us                                                                 | 350 us: 1.03x faster                                             |
| mdp                      | 2.80 sec                                                               | 2.71 sec: 1.03x faster                                           |
| nqueens                  | 81.0 ms                                                                | 78.8 ms: 1.03x faster                                            |
| unpickle_list            | 5.37 us                                                                | 5.23 us: 1.03x faster                                            |
| scimark_fft              | 372 ms                                                                 | 362 ms: 1.03x faster                                             |
| comprehensions           | 16.7 us                                                                | 16.3 us: 1.03x faster                                            |
| pprint_safe_repr         | 755 ms                                                                 | 738 ms: 1.02x faster                                             |
| pprint_pformat           | 1.54 sec                                                               | 1.51 sec: 1.02x faster                                           |
| genshi_xml               | 52.7 ms                                                                | 51.5 ms: 1.02x faster                                            |
| spectral_norm            | 114 ms                                                                 | 111 ms: 1.02x faster                                             |
| mako                     | 10.9 ms                                                                | 10.7 ms: 1.02x faster                                            |
| pidigits                 | 197 ms                                                                 | 193 ms: 1.02x faster                                             |
| sqlglot_parse            | 1.30 ms                                                                | 1.28 ms: 1.02x faster                                            |
| bench_thread_pool        | 837 us                                                                 | 820 us: 1.02x faster                                             |
| logging_simple           | 5.82 us                                                                | 5.70 us: 1.02x faster                                            |
| chaos                    | 60.3 ms                                                                | 59.1 ms: 1.02x faster                                            |
| scimark_sparse_mat_mult  | 5.16 ms                                                                | 5.06 ms: 1.02x faster                                            |
| float                    | 78.9 ms                                                                | 77.5 ms: 1.02x faster                                            |
| meteor_contest           | 110 ms                                                                 | 108 ms: 1.02x faster                                             |
| scimark_lu               | 115 ms                                                                 | 113 ms: 1.01x faster                                             |
| chameleon                | 7.05 ms                                                                | 6.96 ms: 1.01x faster                                            |
| go                       | 142 ms                                                                 | 140 ms: 1.01x faster                                             |
| sqlglot_transpile        | 1.60 ms                                                                | 1.58 ms: 1.01x faster                                            |
| html5lib                 | 67.6 ms                                                                | 66.8 ms: 1.01x faster                                            |
| sqlite_synth             | 2.94 us                                                                | 2.90 us: 1.01x faster                                            |
| genshi_text              | 23.5 ms                                                                | 23.2 ms: 1.01x faster                                            |
| json_loads               | 28.1 us                                                                | 27.8 us: 1.01x faster                                            |
| deepcopy_reduce          | 3.22 us                                                                | 3.19 us: 1.01x faster                                            |
| regex_compile            | 133 ms                                                                 | 132 ms: 1.01x faster                                             |
| json                     | 5.17 ms                                                                | 5.13 ms: 1.01x faster                                            |
| 2to3                     | 269 ms                                                                 | 267 ms: 1.01x faster                                             |
| deltablue                | 3.18 ms                                                                | 3.16 ms: 1.01x faster                                            |
| django_template          | 35.1 ms                                                                | 34.8 ms: 1.01x faster                                            |
| json_dumps               | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                            |
| unpickle_pure_python     | 215 us                                                                 | 214 us: 1.01x faster                                             |
| typing_runtime_protocols | 165 us                                                                 | 163 us: 1.01x faster                                             |
| generators               | 29.4 ms                                                                | 29.2 ms: 1.01x faster                                            |
| scimark_monte_carlo      | 68.3 ms                                                                | 67.9 ms: 1.01x faster                                            |
| raytrace                 | 261 ms                                                                 | 259 ms: 1.01x faster                                             |
| sqlglot_normalize        | 110 ms                                                                 | 109 ms: 1.01x faster                                             |
| regex_v8                 | 25.8 ms                                                                | 25.7 ms: 1.01x faster                                            |
| create_gc_cycles         | 1.76 ms                                                                | 1.76 ms: 1.00x faster                                            |
| sqlglot_optimize         | 54.8 ms                                                                | 54.6 ms: 1.00x faster                                            |
| python_startup_no_site   | 7.11 ms                                                                | 7.09 ms: 1.00x faster                                            |
| python_startup           | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                            |
| asyncio_tcp_ssl          | 1.84 sec                                                               | 1.85 sec: 1.00x slower                                           |
| sympy_integrate          | 20.2 ms                                                                | 20.3 ms: 1.00x slower                                            |
| async_generators         | 441 ms                                                                 | 442 ms: 1.00x slower                                             |
| pathlib                  | 17.6 ms                                                                | 17.6 ms: 1.00x slower                                            |
| pickle_pure_python       | 303 us                                                                 | 305 us: 1.01x slower                                             |
| pickle_dict              | 34.5 us                                                                | 34.7 us: 1.01x slower                                            |
| gunicorn                 | 1.26 ms                                                                | 1.27 ms: 1.01x slower                                            |
| dulwich_log              | 66.2 ms                                                                | 66.7 ms: 1.01x slower                                            |
| thrift                   | 813 us                                                                 | 821 us: 1.01x slower                                             |
| coverage                 | 91.5 ms                                                                | 92.8 ms: 1.01x slower                                            |
| telco                    | 8.43 ms                                                                | 8.56 ms: 1.02x slower                                            |
| pickle                   | 11.6 us                                                                | 11.8 us: 1.02x slower                                            |
| asyncio_tcp              | 505 ms                                                                 | 515 ms: 1.02x slower                                             |
| coroutines               | 22.9 ms                                                                | 23.4 ms: 1.02x slower                                            |
| crypto_pyaes             | 72.9 ms                                                                | 74.7 ms: 1.02x slower                                            |
| unpickle                 | 15.3 us                                                                | 16.1 us: 1.06x slower                                            |
| gc_traversal             | 3.78 ms                                                                | 4.02 ms: 1.06x slower                                            |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                     |

Benchmark hidden because not significant (33): djangocms, async_tree_io_tg, sympy_str, pycparser, tomli_loads, logging_format, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, regex_dna, fannkuch, richards, regex_effbot, mypy2, bench_mp_pool, pylint, tornado_http, richards_super, xml_etree_process, async_tree_cpu_io_mixed, pickle_list, sympy_sum, asyncio_websockets, async_tree_memoization, aiohttp, docutils, xml_etree_generate, sympy_expand, dask, xml_etree_parse, async_tree_none, async_tree_memoization_tg, async_tree_none_tg, async_tree_io

# HPT report

- Reliability score: 98.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
# Results vs. base

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: d59145b
- commit date: 2024-04-26
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6+-5da0280 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 270 ms                                                                 | 267 ms: 1.01x faster                                                             |
| html5lib       | 68.1 ms                                                                | 65.8 ms: 1.03x faster                                                            |
| tornado_http   | 94.2 ms                                                                | 93.8 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): chameleon, docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6+-5da0280 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                                | 90.4 ms: 1.03x faster                                                            |
| pidigits       | 194 ms                                                                 | 189 ms: 1.03x faster                                                             |
| float          | 79.7 ms                                                                | 77.8 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6+-5da0280 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                                | 25.7 ms: 1.01x faster                                                            |
| regex_effbot   | 3.70 ms                                                                | 3.73 ms: 1.01x slower                                                            |
| regex_dna      | 225 ms                                                                 | 230 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6+-5da0280 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_pure_python | 220 us                                                                 | 213 us: 1.03x faster                                                             |
| pickle_pure_python   | 307 us                                                                 | 300 us: 1.02x faster                                                             |
| xml_etree_generate   | 88.1 ms                                                                | 86.3 ms: 1.02x faster                                                            |
| xml_etree_process    | 60.7 ms                                                                | 60.0 ms: 1.01x faster                                                            |
| json_dumps           | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                                            |
| pickle_list          | 5.06 us                                                                | 5.03 us: 1.01x faster                                                            |
| pickle_dict          | 35.7 us                                                                | 35.9 us: 1.00x slower                                                            |
| json_loads           | 27.6 us                                                                | 27.8 us: 1.01x slower                                                            |
| unpickle_list        | 5.23 us                                                                | 5.35 us: 1.02x slower                                                            |
| pickle               | 11.6 us                                                                | 12.1 us: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_iterparse, unpickle, tomli_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6+-5da0280 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                            |
| genshi_text    | 23.5 ms                                                                | 23.8 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240425-linux-x86_64-python-5da0280648b5f1c5142d-3.13.0a6+-5da0280 | bm-20240426-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a6+-d59145b |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| scimark_sparse_mat_mult  | 5.29 ms                                                                | 4.89 ms: 1.08x faster                                                            |
| scimark_sor              | 130 ms                                                                 | 121 ms: 1.07x faster                                                             |
| logging_silent           | 104 ns                                                                 | 98.0 ns: 1.06x faster                                                            |
| typing_runtime_protocols | 167 us                                                                 | 159 us: 1.05x faster                                                             |
| raytrace                 | 268 ms                                                                 | 257 ms: 1.04x faster                                                             |
| richards_super           | 54.6 ms                                                                | 52.5 ms: 1.04x faster                                                            |
| richards                 | 47.8 ms                                                                | 46.0 ms: 1.04x faster                                                            |
| go                       | 144 ms                                                                 | 139 ms: 1.04x faster                                                             |
| deltablue                | 3.27 ms                                                                | 3.16 ms: 1.04x faster                                                            |
| html5lib                 | 68.1 ms                                                                | 65.8 ms: 1.03x faster                                                            |
| unpickle_pure_python     | 220 us                                                                 | 213 us: 1.03x faster                                                             |
| logging_format           | 6.57 us                                                                | 6.36 us: 1.03x faster                                                            |
| logging_simple           | 5.97 us                                                                | 5.78 us: 1.03x faster                                                            |
| nbody                    | 92.9 ms                                                                | 90.4 ms: 1.03x faster                                                            |
| scimark_fft              | 381 ms                                                                 | 371 ms: 1.03x faster                                                             |
| pidigits                 | 194 ms                                                                 | 189 ms: 1.03x faster                                                             |
| float                    | 79.7 ms                                                                | 77.8 ms: 1.02x faster                                                            |
| scimark_lu               | 120 ms                                                                 | 117 ms: 1.02x faster                                                             |
| deepcopy_reduce          | 3.19 us                                                                | 3.13 us: 1.02x faster                                                            |
| pickle_pure_python       | 307 us                                                                 | 300 us: 1.02x faster                                                             |
| xml_etree_generate       | 88.1 ms                                                                | 86.3 ms: 1.02x faster                                                            |
| crypto_pyaes             | 75.2 ms                                                                | 73.7 ms: 1.02x faster                                                            |
| chaos                    | 60.6 ms                                                                | 59.4 ms: 1.02x faster                                                            |
| async_generators         | 452 ms                                                                 | 443 ms: 1.02x faster                                                             |
| telco                    | 8.64 ms                                                                | 8.50 ms: 1.02x faster                                                            |
| sympy_sum                | 155 ms                                                                 | 153 ms: 1.02x faster                                                             |
| sympy_expand             | 470 ms                                                                 | 463 ms: 1.01x faster                                                             |
| sympy_str                | 278 ms                                                                 | 274 ms: 1.01x faster                                                             |
| sympy_integrate          | 20.3 ms                                                                | 20.0 ms: 1.01x faster                                                            |
| deepcopy_memo            | 38.4 us                                                                | 37.9 us: 1.01x faster                                                            |
| hexiom                   | 6.33 ms                                                                | 6.25 ms: 1.01x faster                                                            |
| sqlglot_parse            | 1.29 ms                                                                | 1.27 ms: 1.01x faster                                                            |
| regex_v8                 | 26.0 ms                                                                | 25.7 ms: 1.01x faster                                                            |
| coroutines               | 22.9 ms                                                                | 22.6 ms: 1.01x faster                                                            |
| mako                     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                            |
| 2to3                     | 270 ms                                                                 | 267 ms: 1.01x faster                                                             |
| bench_thread_pool        | 837 us                                                                 | 827 us: 1.01x faster                                                             |
| sqlglot_optimize         | 55.1 ms                                                                | 54.5 ms: 1.01x faster                                                            |
| sqlglot_normalize        | 110 ms                                                                 | 109 ms: 1.01x faster                                                             |
| xml_etree_process        | 60.7 ms                                                                | 60.0 ms: 1.01x faster                                                            |
| sqlglot_transpile        | 1.59 ms                                                                | 1.58 ms: 1.01x faster                                                            |
| json_dumps               | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                                            |
| generators               | 29.5 ms                                                                | 29.3 ms: 1.01x faster                                                            |
| gunicorn                 | 1.27 ms                                                                | 1.26 ms: 1.01x faster                                                            |
| pprint_pformat           | 1.54 sec                                                               | 1.53 sec: 1.01x faster                                                           |
| mdp                      | 2.78 sec                                                               | 2.76 sec: 1.01x faster                                                           |
| dulwich_log              | 66.4 ms                                                                | 65.9 ms: 1.01x faster                                                            |
| pickle_list              | 5.06 us                                                                | 5.03 us: 1.01x faster                                                            |
| pprint_safe_repr         | 752 ms                                                                 | 748 ms: 1.01x faster                                                             |
| create_gc_cycles         | 1.76 ms                                                                | 1.75 ms: 1.01x faster                                                            |
| tornado_http             | 94.2 ms                                                                | 93.8 ms: 1.00x faster                                                            |
| asyncio_tcp_ssl          | 1.85 sec                                                               | 1.84 sec: 1.00x faster                                                           |
| pickle_dict              | 35.7 us                                                                | 35.9 us: 1.00x slower                                                            |
| asyncio_tcp              | 506 ms                                                                 | 508 ms: 1.00x slower                                                             |
| meteor_contest           | 110 ms                                                                 | 111 ms: 1.01x slower                                                             |
| json_loads               | 27.6 us                                                                | 27.8 us: 1.01x slower                                                            |
| pyflate                  | 471 ms                                                                 | 474 ms: 1.01x slower                                                             |
| regex_effbot             | 3.70 ms                                                                | 3.73 ms: 1.01x slower                                                            |
| comprehensions           | 16.9 us                                                                | 17.0 us: 1.01x slower                                                            |
| sqlite_synth             | 2.92 us                                                                | 2.94 us: 1.01x slower                                                            |
| scimark_monte_carlo      | 68.9 ms                                                                | 69.4 ms: 1.01x slower                                                            |
| genshi_text              | 23.5 ms                                                                | 23.8 ms: 1.01x slower                                                            |
| pathlib                  | 17.5 ms                                                                | 17.8 ms: 1.02x slower                                                            |
| regex_dna                | 225 ms                                                                 | 230 ms: 1.02x slower                                                             |
| unpickle_list            | 5.23 us                                                                | 5.35 us: 1.02x slower                                                            |
| pickle                   | 11.6 us                                                                | 12.1 us: 1.04x slower                                                            |
| gc_traversal             | 3.56 ms                                                                | 3.78 ms: 1.06x slower                                                            |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (34): async_tree_io_tg, pylint, async_tree_none, mypy2, async_tree_cpu_io_mixed, djangocms, dask, async_tree_io, async_tree_cpu_io_mixed_tg, aiohttp, async_tree_none_tg, xml_etree_parse, xml_etree_iterparse, unpickle, pycparser, python_startup, regex_compile, chameleon, python_startup_no_site, spectral_norm, nqueens, thrift, docutils, django_template, async_tree_memoization_tg, fannkuch, asyncio_websockets, bench_mp_pool, coverage, tomli_loads, json, genshi_xml, deepcopy, async_tree_memoization

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
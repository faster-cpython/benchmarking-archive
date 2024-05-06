# Results vs. base

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 7819b1c
- commit date: 2024-05-03
- overall geometric mean: 1.00x faster
- HPT reliability: 89.19%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| chameleon      | 7.20 ms                                                                | 6.96 ms: 1.03x faster                                                   |
| tornado_http   | 94.4 ms                                                                | 94.1 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (3): 2to3, docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization_tg, async_tree_io, async_tree_memoization, async_tree_none_tg, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                                | 85.7 ms: 1.03x faster                                                   |
| pidigits       | 193 ms                                                                 | 190 ms: 1.01x faster                                                    |
| float          | 78.7 ms                                                                | 79.2 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 134 ms                                                                 | 134 ms: 1.00x slower                                                    |
| regex_dna      | 223 ms                                                                 | 229 ms: 1.03x slower                                                    |
| regex_effbot   | 3.72 ms                                                                | 3.84 ms: 1.03x slower                                                   |
| regex_v8       | 24.6 ms                                                                | 25.9 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpickle_list        | 5.41 us                                                                | 5.14 us: 1.05x faster                                                   |
| tomli_loads          | 2.19 sec                                                               | 2.17 sec: 1.01x faster                                                  |
| unpickle_pure_python | 218 us                                                                 | 216 us: 1.01x faster                                                    |
| json_dumps           | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                                   |
| json_loads           | 27.8 us                                                                | 27.6 us: 1.01x faster                                                   |
| xml_etree_process    | 60.8 ms                                                                | 61.1 ms: 1.00x slower                                                   |
| pickle               | 11.7 us                                                                | 11.8 us: 1.00x slower                                                   |
| pickle_dict          | 35.3 us                                                                | 35.7 us: 1.01x slower                                                   |
| xml_etree_generate   | 86.9 ms                                                                | 88.0 ms: 1.01x slower                                                   |
| pickle_list          | 5.09 us                                                                | 5.32 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (4): xml_etree_parse, pickle_pure_python, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.12 ms                                                                | 7.09 ms: 1.00x faster                                                   |
| python_startup         | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 52.4 ms                                                                | 50.9 ms: 1.03x faster                                                   |
| genshi_text    | 23.4 ms                                                                | 23.2 ms: 1.01x faster                                                   |
| mako           | 10.9 ms                                                                | 10.8 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20240503-linux-x86_64-python-f201628073f22a785a09-3.13.0a6+-f201628 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal             | 3.94 ms                                                                | 3.74 ms: 1.05x faster                                                   |
| unpickle_list            | 5.41 us                                                                | 5.14 us: 1.05x faster                                                   |
| generators               | 30.0 ms                                                                | 29.0 ms: 1.04x faster                                                   |
| chameleon                | 7.20 ms                                                                | 6.96 ms: 1.03x faster                                                   |
| nbody                    | 88.3 ms                                                                | 85.7 ms: 1.03x faster                                                   |
| genshi_xml               | 52.4 ms                                                                | 50.9 ms: 1.03x faster                                                   |
| logging_format           | 6.51 us                                                                | 6.34 us: 1.03x faster                                                   |
| pyflate                  | 489 ms                                                                 | 477 ms: 1.03x faster                                                    |
| logging_simple           | 5.90 us                                                                | 5.76 us: 1.02x faster                                                   |
| fannkuch                 | 400 ms                                                                 | 392 ms: 1.02x faster                                                    |
| logging_silent           | 104 ns                                                                 | 102 ns: 1.02x faster                                                    |
| pidigits                 | 193 ms                                                                 | 190 ms: 1.01x faster                                                    |
| scimark_monte_carlo      | 68.6 ms                                                                | 67.6 ms: 1.01x faster                                                   |
| raytrace                 | 269 ms                                                                 | 265 ms: 1.01x faster                                                    |
| richards_super           | 54.9 ms                                                                | 54.2 ms: 1.01x faster                                                   |
| tomli_loads              | 2.19 sec                                                               | 2.17 sec: 1.01x faster                                                  |
| scimark_sor              | 134 ms                                                                 | 132 ms: 1.01x faster                                                    |
| genshi_text              | 23.4 ms                                                                | 23.2 ms: 1.01x faster                                                   |
| mako                     | 10.9 ms                                                                | 10.8 ms: 1.01x faster                                                   |
| unpickle_pure_python     | 218 us                                                                 | 216 us: 1.01x faster                                                    |
| crypto_pyaes             | 74.7 ms                                                                | 74.1 ms: 1.01x faster                                                   |
| typing_runtime_protocols | 167 us                                                                 | 166 us: 1.01x faster                                                    |
| json_dumps               | 10.7 ms                                                                | 10.6 ms: 1.01x faster                                                   |
| richards                 | 48.3 ms                                                                | 47.9 ms: 1.01x faster                                                   |
| sqlite_synth             | 2.94 us                                                                | 2.92 us: 1.01x faster                                                   |
| pathlib                  | 17.5 ms                                                                | 17.4 ms: 1.01x faster                                                   |
| sqlglot_normalize        | 110 ms                                                                 | 110 ms: 1.01x faster                                                    |
| json_loads               | 27.8 us                                                                | 27.6 us: 1.01x faster                                                   |
| sqlglot_optimize         | 55.1 ms                                                                | 54.8 ms: 1.01x faster                                                   |
| python_startup_no_site   | 7.12 ms                                                                | 7.09 ms: 1.00x faster                                                   |
| tornado_http             | 94.4 ms                                                                | 94.1 ms: 1.00x faster                                                   |
| asyncio_tcp              | 507 ms                                                                 | 506 ms: 1.00x faster                                                    |
| python_startup           | 10.6 ms                                                                | 10.5 ms: 1.00x faster                                                   |
| bench_thread_pool        | 828 us                                                                 | 831 us: 1.00x slower                                                    |
| regex_compile            | 134 ms                                                                 | 134 ms: 1.00x slower                                                    |
| dulwich_log              | 66.7 ms                                                                | 67.0 ms: 1.00x slower                                                   |
| xml_etree_process        | 60.8 ms                                                                | 61.1 ms: 1.00x slower                                                   |
| pickle                   | 11.7 us                                                                | 11.8 us: 1.00x slower                                                   |
| nqueens                  | 78.9 ms                                                                | 79.3 ms: 1.01x slower                                                   |
| scimark_lu               | 115 ms                                                                 | 116 ms: 1.01x slower                                                    |
| float                    | 78.7 ms                                                                | 79.2 ms: 1.01x slower                                                   |
| pprint_pformat           | 1.53 sec                                                               | 1.54 sec: 1.01x slower                                                  |
| meteor_contest           | 111 ms                                                                 | 111 ms: 1.01x slower                                                    |
| async_generators         | 438 ms                                                                 | 442 ms: 1.01x slower                                                    |
| deepcopy                 | 356 us                                                                 | 359 us: 1.01x slower                                                    |
| spectral_norm            | 115 ms                                                                 | 116 ms: 1.01x slower                                                    |
| pickle_dict              | 35.3 us                                                                | 35.7 us: 1.01x slower                                                   |
| pprint_safe_repr         | 744 ms                                                                 | 753 ms: 1.01x slower                                                    |
| xml_etree_generate       | 86.9 ms                                                                | 88.0 ms: 1.01x slower                                                   |
| deepcopy_reduce          | 3.23 us                                                                | 3.27 us: 1.01x slower                                                   |
| deepcopy_memo            | 38.0 us                                                                | 38.5 us: 1.01x slower                                                   |
| djangocms                | 31.5 us                                                                | 32.2 us: 1.02x slower                                                   |
| regex_dna                | 223 ms                                                                 | 229 ms: 1.03x slower                                                    |
| regex_effbot             | 3.72 ms                                                                | 3.84 ms: 1.03x slower                                                   |
| pycparser                | 1.16 sec                                                               | 1.21 sec: 1.04x slower                                                  |
| pickle_list              | 5.09 us                                                                | 5.32 us: 1.05x slower                                                   |
| regex_v8                 | 24.6 ms                                                                | 25.9 ms: 1.05x slower                                                   |
| mdp                      | 2.57 sec                                                               | 2.75 sec: 1.07x slower                                                  |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (44): async_tree_memoization_tg, async_tree_io, xml_etree_parse, async_tree_memoization, async_tree_none_tg, sympy_str, aiohttp, docutils, sqlglot_parse, mypy2, create_gc_cycles, comprehensions, dask, json, pickle_pure_python, pylint, django_template, xml_etree_iterparse, go, gunicorn, hexiom, sympy_integrate, 2to3, asyncio_tcp_ssl, coverage, async_tree_none, sqlglot_transpile, asyncio_websockets, thrift, async_tree_io_tg, coroutines, scimark_sparse_mat_mult, deltablue, sympy_expand, html5lib, flaskblogging, bench_mp_pool, chaos, telco, sympy_sum, unpickle, scimark_fft, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

# HPT report

- Reliability score: 89.19% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x
# Results vs. base

- fork: faster-cpython
- ref: return_gen_tier_2
- machine: linux-x86_64
- commit hash: fad1c67
- commit date: 2024-04-23
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 301 ms: 1.03x faster                                                          |
| chameleon      | 7.90 ms                                                                | 7.62 ms: 1.04x faster                                                         |
| docutils       | 3.18 sec                                                               | 3.07 sec: 1.04x faster                                                        |
| html5lib       | 71.6 ms                                                                | 72.4 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                  |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|--------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none    | 383 ms                                                                 | 373 ms: 1.03x faster                                                          |
| async_tree_none_tg | 360 ms                                                                 | 351 ms: 1.02x faster                                                          |
| Geometric mean     | (ref)                                                                  | 1.02x faster                                                                  |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 123 ms                                                                 | 120 ms: 1.02x faster                                                          |
| float          | 91.1 ms                                                                | 89.3 ms: 1.02x faster                                                         |
| pidigits       | 193 ms                                                                 | 218 ms: 1.13x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                                 | 179 ms: 1.06x faster                                                          |
| regex_v8       | 25.7 ms                                                                | 25.4 ms: 1.01x faster                                                         |
| regex_dna      | 226 ms                                                                 | 228 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                  |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 2.67 sec                                                               | 2.53 sec: 1.05x faster                                                        |
| unpickle_pure_python | 297 us                                                                 | 283 us: 1.05x faster                                                          |
| xml_etree_generate   | 95.5 ms                                                                | 93.3 ms: 1.02x faster                                                         |
| json_loads           | 27.9 us                                                                | 27.5 us: 1.01x faster                                                         |
| xml_etree_iterparse  | 111 ms                                                                 | 110 ms: 1.01x faster                                                          |
| unpickle_list        | 5.31 us                                                                | 5.26 us: 1.01x faster                                                         |
| xml_etree_process    | 64.5 ms                                                                | 64.2 ms: 1.00x faster                                                         |
| pickle_list          | 5.14 us                                                                | 5.19 us: 1.01x slower                                                         |
| pickle_dict          | 34.7 us                                                                | 35.0 us: 1.01x slower                                                         |
| pickle               | 11.6 us                                                                | 11.9 us: 1.03x slower                                                         |
| unpickle             | 15.1 us                                                                | 15.7 us: 1.04x slower                                                         |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 10.6 ms                                                                | 10.6 ms: 1.00x faster                                                         |
| python_startup_no_site | 7.16 ms                                                                | 7.15 ms: 1.00x faster                                                         |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| django_template | 42.8 ms                                                                | 39.8 ms: 1.08x faster                                                         |
| genshi_xml      | 61.7 ms                                                                | 58.7 ms: 1.05x faster                                                         |
| genshi_text     | 26.0 ms                                                                | 25.6 ms: 1.02x faster                                                         |
| mako            | 13.1 ms                                                                | 13.8 ms: 1.05x slower                                                         |
| Geometric mean  | (ref)                                                                  | 1.02x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nqueens                  | 129 ms                                                                 | 105 ms: 1.23x faster                                                          |
| pyflate                  | 712 ms                                                                 | 588 ms: 1.21x faster                                                          |
| scimark_monte_carlo      | 103 ms                                                                 | 86.0 ms: 1.20x faster                                                         |
| pprint_pformat           | 2.27 sec                                                               | 1.94 sec: 1.17x faster                                                        |
| pprint_safe_repr         | 1.09 sec                                                               | 939 ms: 1.16x faster                                                          |
| richards_super           | 70.7 ms                                                                | 61.8 ms: 1.14x faster                                                         |
| deepcopy_memo            | 49.3 us                                                                | 43.8 us: 1.13x faster                                                         |
| richards                 | 62.6 ms                                                                | 55.6 ms: 1.12x faster                                                         |
| crypto_pyaes             | 103 ms                                                                 | 92.0 ms: 1.12x faster                                                         |
| scimark_sor              | 166 ms                                                                 | 149 ms: 1.11x faster                                                          |
| raytrace                 | 350 ms                                                                 | 319 ms: 1.10x faster                                                          |
| comprehensions           | 24.7 us                                                                | 22.6 us: 1.09x faster                                                         |
| chaos                    | 85.4 ms                                                                | 78.4 ms: 1.09x faster                                                         |
| hexiom                   | 10.2 ms                                                                | 9.45 ms: 1.08x faster                                                         |
| django_template          | 42.8 ms                                                                | 39.8 ms: 1.08x faster                                                         |
| fannkuch                 | 524 ms                                                                 | 487 ms: 1.07x faster                                                          |
| regex_compile            | 190 ms                                                                 | 179 ms: 1.06x faster                                                          |
| sqlglot_optimize         | 67.1 ms                                                                | 63.3 ms: 1.06x faster                                                         |
| telco                    | 9.67 ms                                                                | 9.13 ms: 1.06x faster                                                         |
| deltablue                | 4.39 ms                                                                | 4.15 ms: 1.06x faster                                                         |
| tomli_loads              | 2.67 sec                                                               | 2.53 sec: 1.05x faster                                                        |
| genshi_xml               | 61.7 ms                                                                | 58.7 ms: 1.05x faster                                                         |
| unpickle_pure_python     | 297 us                                                                 | 283 us: 1.05x faster                                                          |
| go                       | 193 ms                                                                 | 185 ms: 1.05x faster                                                          |
| sqlglot_parse            | 1.55 ms                                                                | 1.48 ms: 1.04x faster                                                         |
| meteor_contest           | 125 ms                                                                 | 119 ms: 1.04x faster                                                          |
| scimark_lu               | 170 ms                                                                 | 163 ms: 1.04x faster                                                          |
| sympy_str                | 334 ms                                                                 | 321 ms: 1.04x faster                                                          |
| sympy_integrate          | 24.1 ms                                                                | 23.1 ms: 1.04x faster                                                         |
| sqlglot_normalize        | 128 ms                                                                 | 123 ms: 1.04x faster                                                          |
| docutils                 | 3.18 sec                                                               | 3.07 sec: 1.04x faster                                                        |
| sqlglot_transpile        | 1.87 ms                                                                | 1.80 ms: 1.04x faster                                                         |
| chameleon                | 7.90 ms                                                                | 7.62 ms: 1.04x faster                                                         |
| scimark_fft              | 452 ms                                                                 | 436 ms: 1.04x faster                                                          |
| scimark_sparse_mat_mult  | 6.05 ms                                                                | 5.85 ms: 1.03x faster                                                         |
| sympy_sum                | 184 ms                                                                 | 177 ms: 1.03x faster                                                          |
| typing_runtime_protocols | 127 us                                                                 | 123 us: 1.03x faster                                                          |
| 2to3                     | 310 ms                                                                 | 301 ms: 1.03x faster                                                          |
| gc_traversal             | 3.76 ms                                                                | 3.64 ms: 1.03x faster                                                         |
| pathlib                  | 18.7 ms                                                                | 18.2 ms: 1.03x faster                                                         |
| sqlite_synth             | 3.09 us                                                                | 3.00 us: 1.03x faster                                                         |
| deepcopy                 | 387 us                                                                 | 376 us: 1.03x faster                                                          |
| pycparser                | 1.31 sec                                                               | 1.27 sec: 1.03x faster                                                        |
| async_tree_none          | 383 ms                                                                 | 373 ms: 1.03x faster                                                          |
| logging_simple           | 6.56 us                                                                | 6.40 us: 1.03x faster                                                         |
| sympy_expand             | 548 ms                                                                 | 534 ms: 1.03x faster                                                          |
| thrift                   | 842 us                                                                 | 821 us: 1.03x faster                                                          |
| async_generators         | 489 ms                                                                 | 478 ms: 1.02x faster                                                          |
| nbody                    | 123 ms                                                                 | 120 ms: 1.02x faster                                                          |
| logging_format           | 7.34 us                                                                | 7.17 us: 1.02x faster                                                         |
| bench_thread_pool        | 904 us                                                                 | 883 us: 1.02x faster                                                          |
| async_tree_none_tg       | 360 ms                                                                 | 351 ms: 1.02x faster                                                          |
| xml_etree_generate       | 95.5 ms                                                                | 93.3 ms: 1.02x faster                                                         |
| asyncio_websockets       | 567 ms                                                                 | 555 ms: 1.02x faster                                                          |
| float                    | 91.1 ms                                                                | 89.3 ms: 1.02x faster                                                         |
| coroutines               | 23.3 ms                                                                | 22.8 ms: 1.02x faster                                                         |
| genshi_text              | 26.0 ms                                                                | 25.6 ms: 1.02x faster                                                         |
| logging_silent           | 106 ns                                                                 | 105 ns: 1.01x faster                                                          |
| json_loads               | 27.9 us                                                                | 27.5 us: 1.01x faster                                                         |
| mdp                      | 2.83 sec                                                               | 2.79 sec: 1.01x faster                                                        |
| regex_v8                 | 25.7 ms                                                                | 25.4 ms: 1.01x faster                                                         |
| xml_etree_iterparse      | 111 ms                                                                 | 110 ms: 1.01x faster                                                          |
| spectral_norm            | 140 ms                                                                 | 138 ms: 1.01x faster                                                          |
| dulwich_log              | 74.6 ms                                                                | 73.8 ms: 1.01x faster                                                         |
| unpickle_list            | 5.31 us                                                                | 5.26 us: 1.01x faster                                                         |
| gunicorn                 | 1.34 ms                                                                | 1.33 ms: 1.01x faster                                                         |
| deepcopy_reduce          | 3.30 us                                                                | 3.28 us: 1.01x faster                                                         |
| create_gc_cycles         | 1.77 ms                                                                | 1.76 ms: 1.01x faster                                                         |
| xml_etree_process        | 64.5 ms                                                                | 64.2 ms: 1.00x faster                                                         |
| python_startup           | 10.6 ms                                                                | 10.6 ms: 1.00x faster                                                         |
| python_startup_no_site   | 7.16 ms                                                                | 7.15 ms: 1.00x faster                                                         |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.87 sec: 1.00x slower                                                        |
| asyncio_tcp              | 514 ms                                                                 | 517 ms: 1.01x slower                                                          |
| pickle_list              | 5.14 us                                                                | 5.19 us: 1.01x slower                                                         |
| regex_dna                | 226 ms                                                                 | 228 ms: 1.01x slower                                                          |
| coverage                 | 98.2 ms                                                                | 99.3 ms: 1.01x slower                                                         |
| pickle_dict              | 34.7 us                                                                | 35.0 us: 1.01x slower                                                         |
| html5lib                 | 71.6 ms                                                                | 72.4 ms: 1.01x slower                                                         |
| pickle                   | 11.6 us                                                                | 11.9 us: 1.03x slower                                                         |
| unpickle                 | 15.1 us                                                                | 15.7 us: 1.04x slower                                                         |
| mako                     | 13.1 ms                                                                | 13.8 ms: 1.05x slower                                                         |
| pidigits                 | 193 ms                                                                 | 218 ms: 1.13x slower                                                          |
| Geometric mean           | (ref)                                                                  | 1.03x faster                                                                  |

Benchmark hidden because not significant (19): async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed, mypy2, pylint, async_tree_cpu_io_mixed_tg, async_tree_io, aiohttp, dask, pickle_pure_python, xml_etree_parse, tornado_http, djangocms, json, generators, regex_effbot, json_dumps, bench_mp_pool

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x
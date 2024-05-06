# Results vs. base

- fork: faster-cpython
- ref: tier_2_for_iter_gen
- machine: linux-x86_64
- commit hash: 5fbcbf4
- commit date: 2024-04-24
- overall geometric mean: 1.03x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 302 ms: 1.03x faster                                                            |
| chameleon      | 7.90 ms                                                                | 7.46 ms: 1.06x faster                                                           |
| docutils       | 3.18 sec                                                               | 3.07 sec: 1.04x faster                                                          |
| html5lib       | 71.6 ms                                                                | 70.1 ms: 1.02x faster                                                           |
| tornado_http   | 102 ms                                                                 | 101 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|--------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none    | 383 ms                                                                 | 373 ms: 1.03x faster                                                            |
| async_tree_none_tg | 360 ms                                                                 | 350 ms: 1.03x faster                                                            |
| Geometric mean     | (ref)                                                                  | 1.02x faster                                                                    |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 91.1 ms                                                                | 88.4 ms: 1.03x faster                                                           |
| pidigits       | 193 ms                                                                 | 195 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                                 | 178 ms: 1.07x faster                                                            |
| regex_effbot   | 3.69 ms                                                                | 3.64 ms: 1.01x faster                                                           |
| regex_v8       | 25.7 ms                                                                | 25.4 ms: 1.01x faster                                                           |
| regex_dna      | 226 ms                                                                 | 227 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.67 sec                                                               | 2.49 sec: 1.07x faster                                                          |
| unpickle_pure_python | 297 us                                                                 | 281 us: 1.06x faster                                                            |
| unpickle_list        | 5.31 us                                                                | 5.15 us: 1.03x faster                                                           |
| xml_etree_generate   | 95.5 ms                                                                | 93.3 ms: 1.02x faster                                                           |
| pickle_list          | 5.14 us                                                                | 5.03 us: 1.02x faster                                                           |
| json_loads           | 27.9 us                                                                | 27.6 us: 1.01x faster                                                           |
| pickle               | 11.6 us                                                                | 11.8 us: 1.02x slower                                                           |
| pickle_dict          | 34.7 us                                                                | 35.4 us: 1.02x slower                                                           |
| unpickle             | 15.1 us                                                                | 16.7 us: 1.10x slower                                                           |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (5): xml_etree_parse, json_dumps, xml_etree_process, pickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                                | 7.13 ms: 1.00x faster                                                           |
| python_startup         | 10.6 ms                                                                | 10.6 ms: 1.00x faster                                                           |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| django_template | 42.8 ms                                                                | 39.5 ms: 1.08x faster                                                           |
| genshi_xml      | 61.7 ms                                                                | 62.1 ms: 1.01x slower                                                           |
| genshi_text     | 26.0 ms                                                                | 27.3 ms: 1.05x slower                                                           |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240422-linux-x86_64-python-a6647d16abf4dd659978-3.13.0a6+-a6647d1 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pyflate                  | 712 ms                                                                 | 571 ms: 1.25x faster                                                            |
| nqueens                  | 129 ms                                                                 | 106 ms: 1.21x faster                                                            |
| scimark_monte_carlo      | 103 ms                                                                 | 87.4 ms: 1.18x faster                                                           |
| pprint_safe_repr         | 1.09 sec                                                               | 944 ms: 1.16x faster                                                            |
| pprint_pformat           | 2.27 sec                                                               | 1.97 sec: 1.15x faster                                                          |
| crypto_pyaes             | 103 ms                                                                 | 89.8 ms: 1.15x faster                                                           |
| deepcopy_memo            | 49.3 us                                                                | 43.2 us: 1.14x faster                                                           |
| richards_super           | 70.7 ms                                                                | 62.0 ms: 1.14x faster                                                           |
| richards                 | 62.6 ms                                                                | 55.3 ms: 1.13x faster                                                           |
| scimark_sor              | 166 ms                                                                 | 147 ms: 1.13x faster                                                            |
| hexiom                   | 10.2 ms                                                                | 9.27 ms: 1.10x faster                                                           |
| raytrace                 | 350 ms                                                                 | 319 ms: 1.10x faster                                                            |
| comprehensions           | 24.7 us                                                                | 22.6 us: 1.09x faster                                                           |
| django_template          | 42.8 ms                                                                | 39.5 ms: 1.08x faster                                                           |
| fannkuch                 | 524 ms                                                                 | 483 ms: 1.08x faster                                                            |
| chaos                    | 85.4 ms                                                                | 78.9 ms: 1.08x faster                                                           |
| tomli_loads              | 2.67 sec                                                               | 2.49 sec: 1.07x faster                                                          |
| regex_compile            | 190 ms                                                                 | 178 ms: 1.07x faster                                                            |
| deltablue                | 4.39 ms                                                                | 4.14 ms: 1.06x faster                                                           |
| sqlglot_optimize         | 67.1 ms                                                                | 63.3 ms: 1.06x faster                                                           |
| chameleon                | 7.90 ms                                                                | 7.46 ms: 1.06x faster                                                           |
| telco                    | 9.67 ms                                                                | 9.15 ms: 1.06x faster                                                           |
| unpickle_pure_python     | 297 us                                                                 | 281 us: 1.06x faster                                                            |
| sqlglot_parse            | 1.55 ms                                                                | 1.47 ms: 1.05x faster                                                           |
| go                       | 193 ms                                                                 | 184 ms: 1.05x faster                                                            |
| sympy_integrate          | 24.1 ms                                                                | 23.0 ms: 1.04x faster                                                           |
| meteor_contest           | 125 ms                                                                 | 120 ms: 1.04x faster                                                            |
| sqlglot_normalize        | 128 ms                                                                 | 123 ms: 1.04x faster                                                            |
| sympy_sum                | 184 ms                                                                 | 177 ms: 1.04x faster                                                            |
| scimark_lu               | 170 ms                                                                 | 163 ms: 1.04x faster                                                            |
| docutils                 | 3.18 sec                                                               | 3.07 sec: 1.04x faster                                                          |
| sympy_str                | 334 ms                                                                 | 322 ms: 1.04x faster                                                            |
| sqlglot_transpile        | 1.87 ms                                                                | 1.80 ms: 1.04x faster                                                           |
| typing_runtime_protocols | 127 us                                                                 | 123 us: 1.03x faster                                                            |
| async_generators         | 489 ms                                                                 | 473 ms: 1.03x faster                                                            |
| pycparser                | 1.31 sec                                                               | 1.27 sec: 1.03x faster                                                          |
| logging_simple           | 6.56 us                                                                | 6.36 us: 1.03x faster                                                           |
| float                    | 91.1 ms                                                                | 88.4 ms: 1.03x faster                                                           |
| unpickle_list            | 5.31 us                                                                | 5.15 us: 1.03x faster                                                           |
| coroutines               | 23.3 ms                                                                | 22.6 ms: 1.03x faster                                                           |
| sqlite_synth             | 3.09 us                                                                | 3.00 us: 1.03x faster                                                           |
| 2to3                     | 310 ms                                                                 | 302 ms: 1.03x faster                                                            |
| async_tree_none          | 383 ms                                                                 | 373 ms: 1.03x faster                                                            |
| async_tree_none_tg       | 360 ms                                                                 | 350 ms: 1.03x faster                                                            |
| deepcopy                 | 387 us                                                                 | 376 us: 1.03x faster                                                            |
| sympy_expand             | 548 ms                                                                 | 534 ms: 1.03x faster                                                            |
| logging_format           | 7.34 us                                                                | 7.15 us: 1.03x faster                                                           |
| mypy2                    | 820 ms                                                                 | 800 ms: 1.03x faster                                                            |
| pathlib                  | 18.7 ms                                                                | 18.3 ms: 1.02x faster                                                           |
| xml_etree_generate       | 95.5 ms                                                                | 93.3 ms: 1.02x faster                                                           |
| pickle_list              | 5.14 us                                                                | 5.03 us: 1.02x faster                                                           |
| html5lib                 | 71.6 ms                                                                | 70.1 ms: 1.02x faster                                                           |
| scimark_fft              | 452 ms                                                                 | 443 ms: 1.02x faster                                                            |
| logging_silent           | 106 ns                                                                 | 105 ns: 1.02x faster                                                            |
| regex_effbot             | 3.69 ms                                                                | 3.64 ms: 1.01x faster                                                           |
| dulwich_log              | 74.6 ms                                                                | 73.6 ms: 1.01x faster                                                           |
| regex_v8                 | 25.7 ms                                                                | 25.4 ms: 1.01x faster                                                           |
| bench_thread_pool        | 904 us                                                                 | 893 us: 1.01x faster                                                            |
| tornado_http             | 102 ms                                                                 | 101 ms: 1.01x faster                                                            |
| json_loads               | 27.9 us                                                                | 27.6 us: 1.01x faster                                                           |
| gc_traversal             | 3.76 ms                                                                | 3.72 ms: 1.01x faster                                                           |
| gunicorn                 | 1.34 ms                                                                | 1.33 ms: 1.01x faster                                                           |
| thrift                   | 842 us                                                                 | 834 us: 1.01x faster                                                            |
| aiohttp                  | 1.25 ms                                                                | 1.24 ms: 1.01x faster                                                           |
| create_gc_cycles         | 1.77 ms                                                                | 1.77 ms: 1.00x faster                                                           |
| python_startup_no_site   | 7.16 ms                                                                | 7.13 ms: 1.00x faster                                                           |
| python_startup           | 10.6 ms                                                                | 10.6 ms: 1.00x faster                                                           |
| asyncio_tcp_ssl          | 1.86 sec                                                               | 1.87 sec: 1.00x slower                                                          |
| deepcopy_reduce          | 3.30 us                                                                | 3.32 us: 1.01x slower                                                           |
| genshi_xml               | 61.7 ms                                                                | 62.1 ms: 1.01x slower                                                           |
| regex_dna                | 226 ms                                                                 | 227 ms: 1.01x slower                                                            |
| coverage                 | 98.2 ms                                                                | 99.0 ms: 1.01x slower                                                           |
| pidigits                 | 193 ms                                                                 | 195 ms: 1.01x slower                                                            |
| pickle                   | 11.6 us                                                                | 11.8 us: 1.02x slower                                                           |
| pickle_dict              | 34.7 us                                                                | 35.4 us: 1.02x slower                                                           |
| generators               | 30.2 ms                                                                | 30.8 ms: 1.02x slower                                                           |
| scimark_sparse_mat_mult  | 6.05 ms                                                                | 6.21 ms: 1.03x slower                                                           |
| genshi_text              | 26.0 ms                                                                | 27.3 ms: 1.05x slower                                                           |
| unpickle                 | 15.1 us                                                                | 16.7 us: 1.10x slower                                                           |
| Geometric mean           | (ref)                                                                  | 1.03x faster                                                                    |

Benchmark hidden because not significant (22): async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, pylint, async_tree_cpu_io_mixed, xml_etree_parse, dask, json, async_tree_cpu_io_mixed_tg, nbody, async_tree_io, json_dumps, mdp, bench_mp_pool, xml_etree_process, pickle_pure_python, mako, spectral_norm, asyncio_websockets, xml_etree_iterparse, asyncio_tcp, djangocms

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x
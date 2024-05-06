# Results vs. 3.10.4

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 313 ms: 1.11x faster                                              |
| chameleon      | 9.68 ms                                                | 7.85 ms: 1.23x faster                                             |
| docutils       | 3.30 sec                                               | 3.16 sec: 1.04x faster                                            |
| html5lib       | 88.9 ms                                                | 73.9 ms: 1.20x faster                                             |
| tornado_http   | 136 ms                                                 | 103 ms: 1.32x faster                                              |
| Geometric mean | (ref)                                                  | 1.18x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 382 ms: 1.91x faster                                              |
| async_tree_io           | 1.77 sec                                               | 982 ms: 1.80x faster                                              |
| async_tree_memoization  | 870 ms                                                 | 515 ms: 1.69x faster                                              |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 643 ms: 1.58x faster                                              |
| Geometric mean          | (ref)                                                  | 1.74x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 117 ms                                                 | 94.6 ms: 1.24x faster                                             |
| nbody          | 154 ms                                                 | 132 ms: 1.16x faster                                              |
| pidigits       | 191 ms                                                 | 197 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                  | 1.12x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 26.7 ms: 1.04x faster                                             |
| regex_dna      | 227 ms                                                 | 227 ms: 1.00x slower                                              |
| regex_compile  | 188 ms                                                 | 194 ms: 1.03x slower                                              |
| regex_effbot   | 3.63 ms                                                | 3.79 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                  | 1.01x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 316 us: 1.54x faster                                              |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.31x faster                                             |
| xml_etree_process    | 79.1 ms                                                | 65.8 ms: 1.20x faster                                             |
| tomli_loads          | 3.14 sec                                               | 2.78 sec: 1.13x faster                                            |
| json_loads           | 31.2 us                                                | 28.5 us: 1.09x faster                                             |
| unpickle_pure_python | 331 us                                                 | 309 us: 1.07x faster                                              |
| xml_etree_parse      | 168 ms                                                 | 163 ms: 1.03x faster                                              |
| xml_etree_generate   | 99.4 ms                                                | 96.8 ms: 1.03x faster                                             |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                             |
| unpickle             | 14.4 us                                                | 15.4 us: 1.07x slower                                             |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                             |
| pickle_dict          | 29.6 us                                                | 34.1 us: 1.15x slower                                             |
| Geometric mean       | (ref)                                                  | 1.07x faster                                                      |

Benchmark hidden because not significant (2): unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.7 ms: 1.36x faster                                             |
| python_startup_no_site | 5.93 ms                                                | 9.10 ms: 1.53x slower                                             |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text    | 31.8 ms                                                | 26.0 ms: 1.22x faster                                             |
| mako           | 16.3 ms                                                | 13.9 ms: 1.18x faster                                             |
| genshi_xml     | 66.0 ms                                                | 62.7 ms: 1.05x faster                                             |
| Geometric mean | (ref)                                                  | 1.15x faster                                                      |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 129 us: 4.22x faster                                              |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                             |
| async_tree_none          | 728 ms                                                 | 382 ms: 1.91x faster                                              |
| async_tree_io            | 1.77 sec                                               | 982 ms: 1.80x faster                                              |
| asyncio_tcp              | 922 ms                                                 | 517 ms: 1.78x faster                                              |
| logging_silent           | 190 ns                                                 | 108 ns: 1.76x faster                                              |
| pylint                   | 551 ms                                                 | 315 ms: 1.75x faster                                              |
| deltablue                | 7.91 ms                                                | 4.53 ms: 1.75x faster                                             |
| async_tree_memoization   | 870 ms                                                 | 515 ms: 1.69x faster                                              |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 643 ms: 1.58x faster                                              |
| coroutines               | 35.1 ms                                                | 22.3 ms: 1.57x faster                                             |
| pickle_pure_python       | 484 us                                                 | 316 us: 1.54x faster                                              |
| scimark_sor              | 220 ms                                                 | 151 ms: 1.45x faster                                              |
| chaos                    | 115 ms                                                 | 79.9 ms: 1.45x faster                                             |
| sqlglot_parse            | 2.17 ms                                                | 1.55 ms: 1.40x faster                                             |
| richards_super           | 94.7 ms                                                | 68.0 ms: 1.39x faster                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.38x faster                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.88 ms: 1.37x faster                                             |
| crypto_pyaes             | 128 ms                                                 | 93.4 ms: 1.37x faster                                             |
| python_startup           | 14.6 ms                                                | 10.7 ms: 1.36x faster                                             |
| raytrace                 | 507 ms                                                 | 373 ms: 1.36x faster                                              |
| tornado_http             | 136 ms                                                 | 103 ms: 1.32x faster                                              |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.31x faster                                             |
| scimark_monte_carlo      | 118 ms                                                 | 90.2 ms: 1.31x faster                                             |
| go                       | 240 ms                                                 | 185 ms: 1.30x faster                                              |
| richards                 | 79.3 ms                                                | 61.1 ms: 1.30x faster                                             |
| thrift                   | 1.07 ms                                                | 850 us: 1.26x faster                                              |
| deepcopy_reduce          | 4.17 us                                                | 3.35 us: 1.25x faster                                             |
| logging_simple           | 8.30 us                                                | 6.68 us: 1.24x faster                                             |
| float                    | 117 ms                                                 | 94.6 ms: 1.24x faster                                             |
| logging_format           | 9.09 us                                                | 7.37 us: 1.23x faster                                             |
| chameleon                | 9.68 ms                                                | 7.85 ms: 1.23x faster                                             |
| deepcopy                 | 479 us                                                 | 391 us: 1.22x faster                                              |
| genshi_text              | 31.8 ms                                                | 26.0 ms: 1.22x faster                                             |
| xml_etree_process        | 79.1 ms                                                | 65.8 ms: 1.20x faster                                             |
| html5lib                 | 88.9 ms                                                | 73.9 ms: 1.20x faster                                             |
| mako                     | 16.3 ms                                                | 13.9 ms: 1.18x faster                                             |
| deepcopy_memo            | 58.5 us                                                | 49.9 us: 1.17x faster                                             |
| nbody                    | 154 ms                                                 | 132 ms: 1.16x faster                                              |
| aiohttp                  | 1.44 ms                                                | 1.25 ms: 1.15x faster                                             |
| dask                     | 441 ms                                                 | 384 ms: 1.15x faster                                              |
| tomli_loads              | 3.14 sec                                               | 2.78 sec: 1.13x faster                                            |
| gunicorn                 | 1.53 ms                                                | 1.36 ms: 1.13x faster                                             |
| 2to3                     | 348 ms                                                 | 313 ms: 1.11x faster                                              |
| spectral_norm            | 170 ms                                                 | 153 ms: 1.11x faster                                              |
| comprehensions           | 28.8 us                                                | 25.9 us: 1.11x faster                                             |
| dulwich_log              | 84.3 ms                                                | 76.3 ms: 1.11x faster                                             |
| bench_thread_pool        | 986 us                                                 | 897 us: 1.10x faster                                              |
| pyflate                  | 716 ms                                                 | 651 ms: 1.10x faster                                              |
| json_loads               | 31.2 us                                                | 28.5 us: 1.09x faster                                             |
| pycparser                | 1.58 sec                                               | 1.45 sec: 1.09x faster                                            |
| sqlglot_normalize        | 143 ms                                                 | 131 ms: 1.09x faster                                              |
| sympy_integrate          | 25.8 ms                                                | 24.1 ms: 1.07x faster                                             |
| mypy2                    | 894 ms                                                 | 836 ms: 1.07x faster                                              |
| fannkuch                 | 532 ms                                                 | 497 ms: 1.07x faster                                              |
| unpickle_pure_python     | 331 us                                                 | 309 us: 1.07x faster                                              |
| sympy_sum                | 196 ms                                                 | 184 ms: 1.07x faster                                              |
| genshi_xml               | 66.0 ms                                                | 62.7 ms: 1.05x faster                                             |
| docutils                 | 3.30 sec                                               | 3.16 sec: 1.04x faster                                            |
| json                     | 5.69 ms                                                | 5.47 ms: 1.04x faster                                             |
| regex_v8                 | 27.8 ms                                                | 26.7 ms: 1.04x faster                                             |
| xml_etree_parse          | 168 ms                                                 | 163 ms: 1.03x faster                                              |
| xml_etree_generate       | 99.4 ms                                                | 96.8 ms: 1.03x faster                                             |
| sqlglot_optimize         | 69.2 ms                                                | 67.5 ms: 1.02x faster                                             |
| sympy_str                | 346 ms                                                 | 338 ms: 1.02x faster                                              |
| sympy_expand             | 566 ms                                                 | 554 ms: 1.02x faster                                              |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.33 ms: 1.02x faster                                             |
| hexiom                   | 10.4 ms                                                | 10.2 ms: 1.02x faster                                             |
| pickle_list              | 5.08 us                                                | 5.00 us: 1.02x faster                                             |
| scimark_fft              | 466 ms                                                 | 463 ms: 1.01x faster                                              |
| mdp                      | 2.85 sec                                               | 2.84 sec: 1.00x faster                                            |
| regex_dna                | 227 ms                                                 | 227 ms: 1.00x slower                                              |
| asyncio_websockets       | 559 ms                                                 | 565 ms: 1.01x slower                                              |
| sqlite_synth             | 3.02 us                                                | 3.09 us: 1.02x slower                                             |
| regex_compile            | 188 ms                                                 | 194 ms: 1.03x slower                                              |
| pidigits                 | 191 ms                                                 | 197 ms: 1.03x slower                                              |
| regex_effbot             | 3.63 ms                                                | 3.79 ms: 1.04x slower                                             |
| meteor_contest           | 120 ms                                                 | 127 ms: 1.06x slower                                              |
| unpickle                 | 14.4 us                                                | 15.4 us: 1.07x slower                                             |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                             |
| async_generators         | 444 ms                                                 | 483 ms: 1.09x slower                                              |
| gc_traversal             | 3.62 ms                                                | 4.00 ms: 1.10x slower                                             |
| pprint_safe_repr         | 1.02 sec                                               | 1.13 sec: 1.11x slower                                            |
| pprint_pformat           | 2.10 sec                                               | 2.35 sec: 1.12x slower                                            |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                             |
| nqueens                  | 106 ms                                                 | 121 ms: 1.15x slower                                              |
| pickle_dict              | 29.6 us                                                | 34.1 us: 1.15x slower                                             |
| coverage                 | 79.4 ms                                                | 98.2 ms: 1.24x slower                                             |
| unpack_sequence          | 60.0 ns                                                | 79.3 ns: 1.32x slower                                             |
| telco                    | 7.27 ms                                                | 9.69 ms: 1.33x slower                                             |
| python_startup_no_site   | 5.93 ms                                                | 9.10 ms: 1.53x slower                                             |
| Geometric mean           | (ref)                                                  | 1.16x faster                                                      |

Benchmark hidden because not significant (5): unpickle_list, scimark_lu, bench_mp_pool, pathlib, xml_etree_iterparse
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-8eee1b4-PYTHON_UOPS/bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.10x
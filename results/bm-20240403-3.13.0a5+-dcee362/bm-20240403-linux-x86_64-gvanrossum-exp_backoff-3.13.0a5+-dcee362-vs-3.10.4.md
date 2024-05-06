# Results vs. 3.10.4

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 270 ms: 1.29x faster                                              |
| chameleon      | 9.68 ms                                                | 6.92 ms: 1.40x faster                                             |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                            |
| html5lib       | 88.9 ms                                                | 68.2 ms: 1.30x faster                                             |
| tornado_http   | 136 ms                                                 | 94.2 ms: 1.45x faster                                             |
| Geometric mean | (ref)                                                  | 1.32x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 350 ms: 2.08x faster                                              |
| async_tree_io           | 1.77 sec                                               | 913 ms: 1.94x faster                                              |
| async_tree_memoization  | 870 ms                                                 | 461 ms: 1.89x faster                                              |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 609 ms: 1.67x faster                                              |
| Geometric mean          | (ref)                                                  | 1.89x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 90.1 ms: 1.70x faster                                             |
| float          | 117 ms                                                 | 79.2 ms: 1.48x faster                                             |
| pidigits       | 191 ms                                                 | 194 ms: 1.02x slower                                              |
| Geometric mean | (ref)                                                  | 1.35x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.39x faster                                              |
| regex_v8       | 27.8 ms                                                | 25.5 ms: 1.09x faster                                             |
| regex_dna      | 227 ms                                                 | 224 ms: 1.01x faster                                              |
| regex_effbot   | 3.63 ms                                                | 3.72 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                  | 1.11x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 303 us: 1.60x faster                                              |
| unpickle_pure_python | 331 us                                                 | 226 us: 1.46x faster                                              |
| tomli_loads          | 3.14 sec                                               | 2.16 sec: 1.45x faster                                            |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                             |
| xml_etree_process    | 79.1 ms                                                | 60.4 ms: 1.31x faster                                             |
| xml_etree_generate   | 99.4 ms                                                | 87.9 ms: 1.13x faster                                             |
| json_loads           | 31.2 us                                                | 28.5 us: 1.10x faster                                             |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                              |
| pickle_list          | 5.08 us                                                | 4.79 us: 1.06x faster                                             |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                              |
| unpickle_list        | 5.20 us                                                | 5.02 us: 1.03x faster                                             |
| unpickle             | 14.4 us                                                | 14.9 us: 1.04x slower                                             |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                             |
| pickle_dict          | 29.6 us                                                | 32.9 us: 1.11x slower                                             |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                             |
| python_startup_no_site | 5.93 ms                                                | 8.98 ms: 1.51x slower                                             |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.7 ms: 1.53x faster                                             |
| genshi_text    | 31.8 ms                                                | 24.0 ms: 1.33x faster                                             |
| genshi_xml     | 66.0 ms                                                | 52.1 ms: 1.27x faster                                             |
| Geometric mean | (ref)                                                  | 1.37x faster                                                      |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.77x faster                                              |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                             |
| deltablue                | 7.91 ms                                                | 3.20 ms: 2.47x faster                                             |
| async_tree_none          | 728 ms                                                 | 350 ms: 2.08x faster                                              |
| pylint                   | 551 ms                                                 | 281 ms: 1.96x faster                                              |
| async_tree_io            | 1.77 sec                                               | 913 ms: 1.94x faster                                              |
| raytrace                 | 507 ms                                                 | 264 ms: 1.92x faster                                              |
| logging_silent           | 190 ns                                                 | 99.5 ns: 1.91x faster                                             |
| chaos                    | 115 ms                                                 | 60.9 ms: 1.89x faster                                             |
| async_tree_memoization   | 870 ms                                                 | 461 ms: 1.89x faster                                              |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                              |
| scimark_sor              | 220 ms                                                 | 123 ms: 1.79x faster                                              |
| richards_super           | 94.7 ms                                                | 53.1 ms: 1.78x faster                                             |
| comprehensions           | 28.8 us                                                | 16.5 us: 1.74x faster                                             |
| scimark_monte_carlo      | 118 ms                                                 | 68.9 ms: 1.72x faster                                             |
| nbody                    | 154 ms                                                 | 90.1 ms: 1.70x faster                                             |
| go                       | 240 ms                                                 | 142 ms: 1.70x faster                                              |
| richards                 | 79.3 ms                                                | 47.0 ms: 1.69x faster                                             |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                             |
| crypto_pyaes             | 128 ms                                                 | 76.3 ms: 1.68x faster                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 609 ms: 1.67x faster                                              |
| hexiom                   | 10.4 ms                                                | 6.28 ms: 1.66x faster                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                             |
| pickle_pure_python       | 484 us                                                 | 303 us: 1.60x faster                                              |
| coroutines               | 35.1 ms                                                | 22.2 ms: 1.58x faster                                             |
| scimark_lu               | 176 ms                                                 | 114 ms: 1.54x faster                                              |
| deepcopy_memo            | 58.5 us                                                | 37.9 us: 1.54x faster                                             |
| pyflate                  | 716 ms                                                 | 465 ms: 1.54x faster                                              |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.53x faster                                             |
| spectral_norm            | 170 ms                                                 | 112 ms: 1.51x faster                                              |
| float                    | 117 ms                                                 | 79.2 ms: 1.48x faster                                             |
| unpickle_pure_python     | 331 us                                                 | 226 us: 1.46x faster                                              |
| tomli_loads              | 3.14 sec                                               | 2.16 sec: 1.45x faster                                            |
| tornado_http             | 136 ms                                                 | 94.2 ms: 1.45x faster                                             |
| logging_simple           | 8.30 us                                                | 5.76 us: 1.44x faster                                             |
| logging_format           | 9.09 us                                                | 6.36 us: 1.43x faster                                             |
| chameleon                | 9.68 ms                                                | 6.92 ms: 1.40x faster                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                            |
| regex_compile            | 188 ms                                                 | 135 ms: 1.39x faster                                              |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                             |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.37x faster                                            |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                            |
| pprint_safe_repr         | 1.02 sec                                               | 751 ms: 1.36x faster                                              |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                             |
| fannkuch                 | 532 ms                                                 | 396 ms: 1.34x faster                                              |
| deepcopy                 | 479 us                                                 | 359 us: 1.33x faster                                              |
| thrift                   | 1.07 ms                                                | 804 us: 1.33x faster                                              |
| genshi_text              | 31.8 ms                                                | 24.0 ms: 1.33x faster                                             |
| xml_etree_process        | 79.1 ms                                                | 60.4 ms: 1.31x faster                                             |
| html5lib                 | 88.9 ms                                                | 68.2 ms: 1.30x faster                                             |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                              |
| deepcopy_reduce          | 4.17 us                                                | 3.22 us: 1.29x faster                                             |
| 2to3                     | 348 ms                                                 | 270 ms: 1.29x faster                                              |
| genshi_xml               | 66.0 ms                                                | 52.1 ms: 1.27x faster                                             |
| nqueens                  | 106 ms                                                 | 83.5 ms: 1.27x faster                                             |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.26x faster                                             |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                              |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.15 ms: 1.26x faster                                             |
| dulwich_log              | 84.3 ms                                                | 67.3 ms: 1.25x faster                                             |
| sqlglot_optimize         | 69.2 ms                                                | 55.2 ms: 1.25x faster                                             |
| scimark_fft              | 466 ms                                                 | 374 ms: 1.25x faster                                              |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                              |
| aiohttp                  | 1.44 ms                                                | 1.16 ms: 1.24x faster                                             |
| gunicorn                 | 1.53 ms                                                | 1.26 ms: 1.22x faster                                             |
| mypy2                    | 894 ms                                                 | 737 ms: 1.21x faster                                              |
| sympy_expand             | 566 ms                                                 | 470 ms: 1.20x faster                                              |
| dask                     | 441 ms                                                 | 369 ms: 1.19x faster                                              |
| bench_thread_pool        | 986 us                                                 | 833 us: 1.18x faster                                              |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                            |
| xml_etree_generate       | 99.4 ms                                                | 87.9 ms: 1.13x faster                                             |
| json_loads               | 31.2 us                                                | 28.5 us: 1.10x faster                                             |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.09x faster                                              |
| regex_v8                 | 27.8 ms                                                | 25.5 ms: 1.09x faster                                             |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                              |
| mdp                      | 2.85 sec                                               | 2.65 sec: 1.08x faster                                            |
| pathlib                  | 20.5 ms                                                | 19.1 ms: 1.07x faster                                             |
| pickle_list              | 5.08 us                                                | 4.79 us: 1.06x faster                                             |
| json                     | 5.69 ms                                                | 5.39 ms: 1.06x faster                                             |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                              |
| unpickle_list            | 5.20 us                                                | 5.02 us: 1.03x faster                                             |
| sqlite_synth             | 3.02 us                                                | 2.95 us: 1.02x faster                                             |
| regex_dna                | 227 ms                                                 | 224 ms: 1.01x faster                                              |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.00x faster                                             |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                              |
| pidigits                 | 191 ms                                                 | 194 ms: 1.02x slower                                              |
| regex_effbot             | 3.63 ms                                                | 3.72 ms: 1.02x slower                                             |
| unpickle                 | 14.4 us                                                | 14.9 us: 1.04x slower                                             |
| create_gc_cycles         | 1.62 ms                                                | 1.73 ms: 1.06x slower                                             |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                             |
| gc_traversal             | 3.62 ms                                                | 3.97 ms: 1.10x slower                                             |
| pickle_dict              | 29.6 us                                                | 32.9 us: 1.11x slower                                             |
| telco                    | 7.27 ms                                                | 8.65 ms: 1.19x slower                                             |
| coverage                 | 79.4 ms                                                | 96.2 ms: 1.21x slower                                             |
| python_startup_no_site   | 5.93 ms                                                | 8.98 ms: 1.51x slower                                             |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                      |

Benchmark hidden because not significant (1): async_generators
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240403-3.13.0a5+-dcee362/bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.09x
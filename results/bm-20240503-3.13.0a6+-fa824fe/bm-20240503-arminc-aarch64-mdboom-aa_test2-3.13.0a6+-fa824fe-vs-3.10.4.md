# Results vs. 3.10.4

- fork: mdboom
- ref: aa_test2
- machine: linux-aarch64
- commit hash: fa824fe
- commit date: 2024-05-03
- overall geometric mean: 1.29x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 381 ms                                                                | 302 ms: 1.26x faster                                         |
| chameleon      | 10.8 ms                                                               | 9.17 ms: 1.18x faster                                        |
| docutils       | 3.53 sec                                                              | 3.10 sec: 1.14x faster                                       |
| html5lib       | 86.5 ms                                                               | 66.0 ms: 1.31x faster                                        |
| tornado_http   | 178 ms                                                                | 128 ms: 1.40x faster                                         |
| Geometric mean | (ref)                                                                 | 1.25x faster                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|-------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none         | 950 ms                                                                | 494 ms: 1.92x faster                                         |
| async_tree_io           | 2.28 sec                                                              | 1.23 sec: 1.85x faster                                       |
| async_tree_memoization  | 1.13 sec                                                              | 650 ms: 1.74x faster                                         |
| async_tree_cpu_io_mixed | 1.27 sec                                                              | 792 ms: 1.61x faster                                         |
| Geometric mean          | (ref)                                                                 | 1.78x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 166 ms                                                                | 111 ms: 1.49x faster                                         |
| float          | 135 ms                                                                | 91.0 ms: 1.48x faster                                        |
| pidigits       | 235 ms                                                                | 233 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                                 | 1.31x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                | 128 ms: 1.38x faster                                         |
| regex_dna      | 257 ms                                                                | 249 ms: 1.03x faster                                         |
| regex_v8       | 32.2 ms                                                               | 31.1 ms: 1.03x faster                                        |
| regex_effbot   | 4.25 ms                                                               | 4.88 ms: 1.15x slower                                        |
| Geometric mean | (ref)                                                                 | 1.06x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| unpickle_pure_python | 366 us                                                                | 248 us: 1.48x faster                                         |
| pickle_pure_python   | 529 us                                                                | 363 us: 1.46x faster                                         |
| tomli_loads          | 3.36 sec                                                              | 2.53 sec: 1.33x faster                                       |
| json_dumps           | 16.7 ms                                                               | 13.1 ms: 1.27x faster                                        |
| xml_etree_process    | 99.5 ms                                                               | 80.5 ms: 1.24x faster                                        |
| xml_etree_parse      | 212 ms                                                                | 188 ms: 1.13x faster                                         |
| unpickle_list        | 6.99 us                                                               | 6.32 us: 1.11x faster                                        |
| xml_etree_generate   | 123 ms                                                                | 114 ms: 1.08x faster                                         |
| xml_etree_iterparse  | 156 ms                                                                | 148 ms: 1.06x faster                                         |
| pickle_list          | 5.24 us                                                               | 5.36 us: 1.02x slower                                        |
| json_loads           | 30.9 us                                                               | 32.2 us: 1.04x slower                                        |
| pickle_dict          | 35.1 us                                                               | 37.6 us: 1.07x slower                                        |
| pickle               | 12.5 us                                                               | 13.5 us: 1.08x slower                                        |
| unpickle             | 17.5 us                                                               | 19.9 us: 1.14x slower                                        |
| Geometric mean       | (ref)                                                                 | 1.11x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 11.2 ms                                                               | 12.5 ms: 1.11x slower                                        |
| python_startup_no_site | 6.89 ms                                                               | 8.35 ms: 1.21x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.16x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 18.9 ms                                                               | 13.2 ms: 1.44x faster                                        |
| django_template | 53.3 ms                                                               | 41.9 ms: 1.27x faster                                        |
| genshi_text     | 35.2 ms                                                               | 27.8 ms: 1.27x faster                                        |
| genshi_xml      | 69.8 ms                                                               | 60.6 ms: 1.15x faster                                        |
| Geometric mean  | (ref)                                                                 | 1.28x faster                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|--------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols | 661 us                                                                | 193 us: 3.43x faster                                         |
| deltablue                | 8.94 ms                                                               | 3.88 ms: 2.30x faster                                        |
| bench_mp_pool            | 14.5 ms                                                               | 7.14 ms: 2.04x faster                                        |
| raytrace                 | 573 ms                                                                | 297 ms: 1.93x faster                                         |
| async_tree_none          | 950 ms                                                                | 494 ms: 1.92x faster                                         |
| async_tree_io            | 2.28 sec                                                              | 1.23 sec: 1.85x faster                                       |
| generators               | 68.1 ms                                                               | 37.7 ms: 1.80x faster                                        |
| chaos                    | 121 ms                                                                | 68.1 ms: 1.78x faster                                        |
| richards_super           | 107 ms                                                                | 61.0 ms: 1.76x faster                                        |
| async_tree_memoization   | 1.13 sec                                                              | 650 ms: 1.74x faster                                         |
| sqlglot_parse            | 2.40 ms                                                               | 1.38 ms: 1.74x faster                                        |
| asyncio_tcp              | 944 ms                                                                | 561 ms: 1.68x faster                                         |
| scimark_lu               | 227 ms                                                                | 136 ms: 1.67x faster                                         |
| sqlglot_transpile        | 2.84 ms                                                               | 1.71 ms: 1.66x faster                                        |
| crypto_pyaes             | 134 ms                                                                | 80.7 ms: 1.66x faster                                        |
| richards                 | 91.7 ms                                                               | 55.5 ms: 1.65x faster                                        |
| logging_silent           | 222 ns                                                                | 134 ns: 1.65x faster                                         |
| go                       | 264 ms                                                                | 160 ms: 1.65x faster                                         |
| comprehensions           | 33.1 us                                                               | 20.5 us: 1.62x faster                                        |
| async_tree_cpu_io_mixed  | 1.27 sec                                                              | 792 ms: 1.61x faster                                         |
| scimark_sor              | 246 ms                                                                | 159 ms: 1.55x faster                                         |
| scimark_monte_carlo      | 128 ms                                                                | 82.5 ms: 1.55x faster                                        |
| hexiom                   | 10.9 ms                                                               | 7.07 ms: 1.54x faster                                        |
| nbody                    | 166 ms                                                                | 111 ms: 1.49x faster                                         |
| asyncio_tcp_ssl          | 3.28 sec                                                              | 2.21 sec: 1.48x faster                                       |
| float                    | 135 ms                                                                | 91.0 ms: 1.48x faster                                        |
| unpickle_pure_python     | 366 us                                                                | 248 us: 1.48x faster                                         |
| pickle_pure_python       | 529 us                                                                | 363 us: 1.46x faster                                         |
| mako                     | 18.9 ms                                                               | 13.2 ms: 1.44x faster                                        |
| pyflate                  | 795 ms                                                                | 558 ms: 1.42x faster                                         |
| pylint                   | 485 ms                                                                | 342 ms: 1.42x faster                                         |
| tornado_http             | 178 ms                                                                | 128 ms: 1.40x faster                                         |
| pycparser                | 1.69 sec                                                              | 1.22 sec: 1.38x faster                                       |
| logging_simple           | 9.78 us                                                               | 7.09 us: 1.38x faster                                        |
| regex_compile            | 177 ms                                                                | 128 ms: 1.38x faster                                         |
| logging_format           | 10.6 us                                                               | 7.76 us: 1.37x faster                                        |
| thrift                   | 1.26 ms                                                               | 942 us: 1.34x faster                                         |
| spectral_norm            | 186 ms                                                                | 141 ms: 1.33x faster                                         |
| tomli_loads              | 3.36 sec                                                              | 2.53 sec: 1.33x faster                                       |
| html5lib                 | 86.5 ms                                                               | 66.0 ms: 1.31x faster                                        |
| dulwich_log              | 73.5 ms                                                               | 57.1 ms: 1.29x faster                                        |
| coroutines               | 37.2 ms                                                               | 29.0 ms: 1.28x faster                                        |
| django_template          | 53.3 ms                                                               | 41.9 ms: 1.27x faster                                        |
| json_dumps               | 16.7 ms                                                               | 13.1 ms: 1.27x faster                                        |
| sympy_sum                | 184 ms                                                                | 145 ms: 1.27x faster                                         |
| genshi_text              | 35.2 ms                                                               | 27.8 ms: 1.27x faster                                        |
| bench_thread_pool        | 1.59 ms                                                               | 1.26 ms: 1.26x faster                                        |
| sympy_integrate          | 26.5 ms                                                               | 21.1 ms: 1.26x faster                                        |
| 2to3                     | 381 ms                                                                | 302 ms: 1.26x faster                                         |
| deepcopy_memo            | 61.7 us                                                               | 49.4 us: 1.25x faster                                        |
| sympy_str                | 329 ms                                                                | 265 ms: 1.24x faster                                         |
| xml_etree_process        | 99.5 ms                                                               | 80.5 ms: 1.24x faster                                        |
| sqlglot_normalize        | 156 ms                                                                | 127 ms: 1.23x faster                                         |
| pprint_pformat           | 2.36 sec                                                              | 1.93 sec: 1.22x faster                                       |
| pprint_safe_repr         | 1.15 sec                                                              | 939 ms: 1.22x faster                                         |
| dask                     | 450 ms                                                                | 369 ms: 1.22x faster                                         |
| sqlglot_optimize         | 75.4 ms                                                               | 61.9 ms: 1.22x faster                                        |
| gunicorn                 | 1.45 ms                                                               | 1.21 ms: 1.20x faster                                        |
| fannkuch                 | 546 ms                                                                | 456 ms: 1.20x faster                                         |
| nqueens                  | 117 ms                                                                | 98.3 ms: 1.19x faster                                        |
| sympy_expand             | 543 ms                                                                | 455 ms: 1.19x faster                                         |
| aiohttp                  | 1.39 ms                                                               | 1.17 ms: 1.19x faster                                        |
| chameleon                | 10.8 ms                                                               | 9.17 ms: 1.18x faster                                        |
| scimark_sparse_mat_mult  | 7.62 ms                                                               | 6.52 ms: 1.17x faster                                        |
| pathlib                  | 26.3 ms                                                               | 22.7 ms: 1.16x faster                                        |
| genshi_xml               | 69.8 ms                                                               | 60.6 ms: 1.15x faster                                        |
| deepcopy                 | 511 us                                                                | 445 us: 1.15x faster                                         |
| docutils                 | 3.53 sec                                                              | 3.10 sec: 1.14x faster                                       |
| xml_etree_parse          | 212 ms                                                                | 188 ms: 1.13x faster                                         |
| deepcopy_reduce          | 4.60 us                                                               | 4.08 us: 1.13x faster                                        |
| scimark_fft              | 500 ms                                                                | 445 ms: 1.13x faster                                         |
| mdp                      | 3.70 sec                                                              | 3.31 sec: 1.12x faster                                       |
| meteor_contest           | 126 ms                                                                | 113 ms: 1.11x faster                                         |
| unpickle_list            | 6.99 us                                                               | 6.32 us: 1.11x faster                                        |
| xml_etree_generate       | 123 ms                                                                | 114 ms: 1.08x faster                                         |
| sqlite_synth             | 4.12 us                                                               | 3.88 us: 1.06x faster                                        |
| xml_etree_iterparse      | 156 ms                                                                | 148 ms: 1.06x faster                                         |
| regex_dna                | 257 ms                                                                | 249 ms: 1.03x faster                                         |
| regex_v8                 | 32.2 ms                                                               | 31.1 ms: 1.03x faster                                        |
| json                     | 5.88 ms                                                               | 5.72 ms: 1.03x faster                                        |
| flaskblogging            | 4.83 ms                                                               | 4.73 ms: 1.02x faster                                        |
| pidigits                 | 235 ms                                                                | 233 ms: 1.01x faster                                         |
| pickle_list              | 5.24 us                                                               | 5.36 us: 1.02x slower                                        |
| json_loads               | 30.9 us                                                               | 32.2 us: 1.04x slower                                        |
| async_generators         | 452 ms                                                                | 484 ms: 1.07x slower                                         |
| pickle_dict              | 35.1 us                                                               | 37.6 us: 1.07x slower                                        |
| pickle                   | 12.5 us                                                               | 13.5 us: 1.08x slower                                        |
| python_startup           | 11.2 ms                                                               | 12.5 ms: 1.11x slower                                        |
| unpickle                 | 17.5 us                                                               | 19.9 us: 1.14x slower                                        |
| regex_effbot             | 4.25 ms                                                               | 4.88 ms: 1.15x slower                                        |
| coverage                 | 83.6 ms                                                               | 99.0 ms: 1.18x slower                                        |
| telco                    | 8.49 ms                                                               | 10.1 ms: 1.19x slower                                        |
| gc_traversal             | 4.15 ms                                                               | 5.01 ms: 1.21x slower                                        |
| python_startup_no_site   | 6.89 ms                                                               | 8.35 ms: 1.21x slower                                        |
| Geometric mean           | (ref)                                                                 | 1.29x faster                                                 |

Benchmark hidden because not significant (2): asyncio_websockets, create_gc_cycles
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240503-3.13.0a6+-fa824fe/bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.23x
- 95% likely to have a speedup of 1.22x
- 99% likely to have a speedup of 1.21x

# Memory
- memory change: 1.11x
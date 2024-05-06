# Results vs. 3.10.4

- fork: mdboom
- ref: aa_test_apr_2024
- machine: linux-x86_64
- commit hash: 73d6faa
- commit date: 2024-04-23
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 271 ms: 1.29x faster                                               |
| chameleon      | 9.68 ms                                                | 6.90 ms: 1.40x faster                                              |
| docutils       | 3.30 sec                                               | 2.81 sec: 1.17x faster                                             |
| html5lib       | 88.9 ms                                                | 67.4 ms: 1.32x faster                                              |
| tornado_http   | 136 ms                                                 | 94.1 ms: 1.45x faster                                              |
| Geometric mean | (ref)                                                  | 1.32x faster                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                               |
| async_tree_io           | 1.77 sec                                               | 908 ms: 1.95x faster                                               |
| async_tree_memoization  | 870 ms                                                 | 461 ms: 1.89x faster                                               |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 613 ms: 1.66x faster                                               |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 95.5 ms: 1.61x faster                                              |
| float          | 117 ms                                                 | 79.2 ms: 1.48x faster                                              |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                  | 1.34x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 136 ms: 1.39x faster                                               |
| regex_v8       | 27.8 ms                                                | 25.8 ms: 1.08x faster                                              |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                               |
| regex_effbot   | 3.63 ms                                                | 3.73 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                  | 1.10x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 306 us: 1.58x faster                                               |
| unpickle_pure_python | 331 us                                                 | 219 us: 1.51x faster                                               |
| tomli_loads          | 3.14 sec                                               | 2.21 sec: 1.42x faster                                             |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                              |
| xml_etree_process    | 79.1 ms                                                | 60.4 ms: 1.31x faster                                              |
| xml_etree_generate   | 99.4 ms                                                | 87.7 ms: 1.13x faster                                              |
| json_loads           | 31.2 us                                                | 27.8 us: 1.12x faster                                              |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                               |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.06x faster                                               |
| unpickle_list        | 5.20 us                                                | 5.11 us: 1.02x faster                                              |
| unpickle             | 14.4 us                                                | 15.6 us: 1.08x slower                                              |
| pickle               | 10.7 us                                                | 12.1 us: 1.14x slower                                              |
| pickle_dict          | 29.6 us                                                | 35.3 us: 1.19x slower                                              |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                       |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                              |
| python_startup_no_site | 5.93 ms                                                | 7.09 ms: 1.19x slower                                              |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.9 ms: 1.50x faster                                              |
| django_template | 48.2 ms                                                | 35.0 ms: 1.38x faster                                              |
| genshi_text     | 31.8 ms                                                | 23.9 ms: 1.33x faster                                              |
| genshi_xml      | 66.0 ms                                                | 51.9 ms: 1.27x faster                                              |
| Geometric mean  | (ref)                                                  | 1.37x faster                                                       |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.80x faster                                               |
| generators               | 80.1 ms                                                | 29.8 ms: 2.69x faster                                              |
| deltablue                | 7.91 ms                                                | 3.27 ms: 2.42x faster                                              |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                               |
| async_tree_io            | 1.77 sec                                               | 908 ms: 1.95x faster                                               |
| raytrace                 | 507 ms                                                 | 264 ms: 1.92x faster                                               |
| async_tree_memoization   | 870 ms                                                 | 461 ms: 1.89x faster                                               |
| chaos                    | 115 ms                                                 | 61.8 ms: 1.87x faster                                              |
| asyncio_tcp              | 922 ms                                                 | 505 ms: 1.83x faster                                               |
| scimark_sor              | 220 ms                                                 | 124 ms: 1.77x faster                                               |
| logging_silent           | 190 ns                                                 | 108 ns: 1.76x faster                                               |
| richards_super           | 94.7 ms                                                | 54.4 ms: 1.74x faster                                              |
| pylint                   | 551 ms                                                 | 319 ms: 1.73x faster                                               |
| crypto_pyaes             | 128 ms                                                 | 75.1 ms: 1.70x faster                                              |
| comprehensions           | 28.8 us                                                | 17.0 us: 1.69x faster                                              |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                              |
| scimark_monte_carlo      | 118 ms                                                 | 70.6 ms: 1.67x faster                                              |
| go                       | 240 ms                                                 | 144 ms: 1.67x faster                                               |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 613 ms: 1.66x faster                                               |
| richards                 | 79.3 ms                                                | 48.2 ms: 1.64x faster                                              |
| hexiom                   | 10.4 ms                                                | 6.35 ms: 1.64x faster                                              |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                              |
| nbody                    | 154 ms                                                 | 95.5 ms: 1.61x faster                                              |
| pickle_pure_python       | 484 us                                                 | 306 us: 1.58x faster                                               |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                              |
| pyflate                  | 716 ms                                                 | 469 ms: 1.53x faster                                               |
| deepcopy_memo            | 58.5 us                                                | 38.5 us: 1.52x faster                                              |
| unpickle_pure_python     | 331 us                                                 | 219 us: 1.51x faster                                               |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.50x faster                                              |
| scimark_lu               | 176 ms                                                 | 119 ms: 1.48x faster                                               |
| float                    | 117 ms                                                 | 79.2 ms: 1.48x faster                                              |
| spectral_norm            | 170 ms                                                 | 116 ms: 1.47x faster                                               |
| tornado_http             | 136 ms                                                 | 94.1 ms: 1.45x faster                                              |
| logging_simple           | 8.30 us                                                | 5.83 us: 1.42x faster                                              |
| tomli_loads              | 3.14 sec                                               | 2.21 sec: 1.42x faster                                             |
| chameleon                | 9.68 ms                                                | 6.90 ms: 1.40x faster                                              |
| logging_format           | 9.09 us                                                | 6.49 us: 1.40x faster                                              |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                             |
| regex_compile            | 188 ms                                                 | 136 ms: 1.39x faster                                               |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                              |
| django_template          | 48.2 ms                                                | 35.0 ms: 1.38x faster                                              |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.37x faster                                             |
| pprint_safe_repr         | 1.02 sec                                               | 752 ms: 1.35x faster                                               |
| fannkuch                 | 532 ms                                                 | 396 ms: 1.34x faster                                               |
| deepcopy                 | 479 us                                                 | 357 us: 1.34x faster                                               |
| genshi_text              | 31.8 ms                                                | 23.9 ms: 1.33x faster                                              |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                              |
| thrift                   | 1.07 ms                                                | 809 us: 1.32x faster                                               |
| html5lib                 | 88.9 ms                                                | 67.4 ms: 1.32x faster                                              |
| nqueens                  | 106 ms                                                 | 80.5 ms: 1.31x faster                                              |
| pycparser                | 1.58 sec                                               | 1.20 sec: 1.31x faster                                             |
| xml_etree_process        | 79.1 ms                                                | 60.4 ms: 1.31x faster                                              |
| deepcopy_reduce          | 4.17 us                                                | 3.19 us: 1.31x faster                                              |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                               |
| 2to3                     | 348 ms                                                 | 271 ms: 1.29x faster                                               |
| genshi_xml               | 66.0 ms                                                | 51.9 ms: 1.27x faster                                              |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.27x faster                                              |
| dulwich_log              | 84.3 ms                                                | 66.8 ms: 1.26x faster                                              |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.25x faster                                               |
| sqlglot_optimize         | 69.2 ms                                                | 55.2 ms: 1.25x faster                                              |
| sympy_str                | 346 ms                                                 | 281 ms: 1.23x faster                                               |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                              |
| scimark_fft              | 466 ms                                                 | 382 ms: 1.22x faster                                               |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.33 ms: 1.21x faster                                              |
| mypy2                    | 894 ms                                                 | 737 ms: 1.21x faster                                               |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                              |
| djangocms                | 38.4 us                                                | 31.9 us: 1.21x faster                                              |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                               |
| sympy_expand             | 566 ms                                                 | 475 ms: 1.19x faster                                               |
| bench_thread_pool        | 986 us                                                 | 833 us: 1.18x faster                                               |
| docutils                 | 3.30 sec                                               | 2.81 sec: 1.17x faster                                             |
| pathlib                  | 20.5 ms                                                | 17.6 ms: 1.16x faster                                              |
| xml_etree_generate       | 99.4 ms                                                | 87.7 ms: 1.13x faster                                              |
| json_loads               | 31.2 us                                                | 27.8 us: 1.12x faster                                              |
| json                     | 5.69 ms                                                | 5.13 ms: 1.11x faster                                              |
| mdp                      | 2.85 sec                                               | 2.60 sec: 1.09x faster                                             |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                               |
| regex_v8                 | 27.8 ms                                                | 25.8 ms: 1.08x faster                                              |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                               |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.06x faster                                               |
| sqlite_synth             | 3.02 us                                                | 2.95 us: 1.03x faster                                              |
| unpickle_list            | 5.20 us                                                | 5.11 us: 1.02x faster                                              |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                               |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                               |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.00x faster                                              |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                               |
| regex_effbot             | 3.63 ms                                                | 3.73 ms: 1.03x slower                                              |
| gc_traversal             | 3.62 ms                                                | 3.87 ms: 1.07x slower                                              |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                              |
| unpickle                 | 14.4 us                                                | 15.6 us: 1.08x slower                                              |
| pickle                   | 10.7 us                                                | 12.1 us: 1.14x slower                                              |
| pickle_dict              | 29.6 us                                                | 35.3 us: 1.19x slower                                              |
| python_startup_no_site   | 5.93 ms                                                | 7.09 ms: 1.19x slower                                              |
| telco                    | 7.27 ms                                                | 8.78 ms: 1.21x slower                                              |
| coverage                 | 79.4 ms                                                | 98.3 ms: 1.24x slower                                              |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                       |

Benchmark hidden because not significant (2): pickle_list, async_generators
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240423-3.13.0a6+-73d6faa/bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x
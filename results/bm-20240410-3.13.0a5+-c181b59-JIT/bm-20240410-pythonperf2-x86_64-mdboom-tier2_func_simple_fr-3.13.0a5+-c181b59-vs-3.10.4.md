# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 300 ms: 1.17x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.65 ms: 1.23x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.10 sec: 1.10x faster                                                       |
| html5lib       | 94.6 ms                                                      | 75.3 ms: 1.26x faster                                                        |
| tornado_http   | 157 ms                                                       | 122 ms: 1.28x faster                                                         |
| Geometric mean | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization  | 819 ms                                                       | 446 ms: 1.84x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 871 ms: 1.84x faster                                                         |
| async_tree_none         | 692 ms                                                       | 378 ms: 1.83x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 609 ms: 1.54x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.75x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 76.1 ms: 1.46x faster                                                        |
| nbody          | 134 ms                                                       | 96.2 ms: 1.39x faster                                                        |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.28x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 148 ms: 1.28x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.5 ms: 1.07x faster                                                        |
| regex_dna      | 261 ms                                                       | 245 ms: 1.06x faster                                                         |
| regex_effbot   | 3.09 ms                                                      | 3.71 ms: 1.20x slower                                                        |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 311 us: 1.46x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.4 ms: 1.40x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.13 sec: 1.37x faster                                                       |
| unpickle_pure_python | 312 us                                                       | 232 us: 1.34x faster                                                         |
| xml_etree_process    | 75.9 ms                                                      | 59.0 ms: 1.29x faster                                                        |
| json_loads           | 30.3 us                                                      | 25.5 us: 1.19x faster                                                        |
| xml_etree_generate   | 92.3 ms                                                      | 84.6 ms: 1.09x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 102 ms: 1.08x faster                                                         |
| xml_etree_parse      | 160 ms                                                       | 148 ms: 1.08x faster                                                         |
| pickle_list          | 4.12 us                                                      | 4.39 us: 1.06x slower                                                        |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 32.6 us: 1.11x slower                                                        |
| unpickle             | 13.5 us                                                      | 15.0 us: 1.11x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 10.1 ms: 1.46x faster                                                        |
| genshi_text    | 31.4 ms                                                      | 28.0 ms: 1.12x faster                                                        |
| genshi_xml     | 63.3 ms                                                      | 61.8 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                        | 1.19x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 124 us: 4.32x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 374 ms: 2.08x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.80 ms: 1.98x faster                                                        |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                       |
| async_tree_memoization   | 819 ms                                                       | 446 ms: 1.84x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 871 ms: 1.84x faster                                                         |
| async_tree_none          | 692 ms                                                       | 378 ms: 1.83x faster                                                         |
| raytrace                 | 489 ms                                                       | 272 ms: 1.80x faster                                                         |
| generators               | 57.3 ms                                                      | 33.2 ms: 1.73x faster                                                        |
| pylint                   | 566 ms                                                       | 333 ms: 1.70x faster                                                         |
| logging_silent           | 167 ns                                                       | 98.9 ns: 1.69x faster                                                        |
| richards_super           | 90.6 ms                                                      | 53.7 ms: 1.69x faster                                                        |
| chaos                    | 109 ms                                                       | 64.8 ms: 1.67x faster                                                        |
| richards                 | 75.1 ms                                                      | 46.7 ms: 1.61x faster                                                        |
| sqlglot_parse            | 2.24 ms                                                      | 1.42 ms: 1.57x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 76.9 ms: 1.55x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 609 ms: 1.54x faster                                                         |
| pyflate                  | 733 ms                                                       | 483 ms: 1.52x faster                                                         |
| go                       | 262 ms                                                       | 175 ms: 1.50x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 72.0 ms: 1.49x faster                                                        |
| spectral_norm            | 139 ms                                                       | 93.8 ms: 1.48x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 1.82 ms: 1.47x faster                                                        |
| pickle_pure_python       | 455 us                                                       | 311 us: 1.46x faster                                                         |
| float                    | 111 ms                                                       | 76.1 ms: 1.46x faster                                                        |
| mako                     | 14.7 ms                                                      | 10.1 ms: 1.46x faster                                                        |
| logging_simple           | 8.88 us                                                      | 6.27 us: 1.42x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.4 ms: 1.40x faster                                                        |
| comprehensions           | 26.7 us                                                      | 19.1 us: 1.39x faster                                                        |
| nbody                    | 134 ms                                                       | 96.2 ms: 1.39x faster                                                        |
| logging_format           | 9.64 us                                                      | 6.95 us: 1.39x faster                                                        |
| scimark_lu               | 167 ms                                                       | 121 ms: 1.38x faster                                                         |
| coroutines               | 30.3 ms                                                      | 22.1 ms: 1.37x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.13 sec: 1.37x faster                                                       |
| bench_mp_pool            | 6.37 ms                                                      | 4.70 ms: 1.36x faster                                                        |
| unpickle_pure_python     | 312 us                                                       | 232 us: 1.34x faster                                                         |
| pycparser                | 1.67 sec                                                     | 1.27 sec: 1.31x faster                                                       |
| hexiom                   | 9.42 ms                                                      | 7.17 ms: 1.31x faster                                                        |
| thrift                   | 1.18 ms                                                      | 897 us: 1.31x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 59.0 ms: 1.29x faster                                                        |
| deepcopy_memo            | 49.8 us                                                      | 38.8 us: 1.28x faster                                                        |
| tornado_http             | 157 ms                                                       | 122 ms: 1.28x faster                                                         |
| regex_compile            | 190 ms                                                       | 148 ms: 1.28x faster                                                         |
| pprint_safe_repr         | 1.05 sec                                                     | 827 ms: 1.27x faster                                                         |
| html5lib                 | 94.6 ms                                                      | 75.3 ms: 1.26x faster                                                        |
| pprint_pformat           | 2.15 sec                                                     | 1.72 sec: 1.25x faster                                                       |
| fannkuch                 | 483 ms                                                       | 389 ms: 1.24x faster                                                         |
| chameleon                | 9.44 ms                                                      | 7.65 ms: 1.23x faster                                                        |
| bench_thread_pool        | 1.14 ms                                                      | 930 us: 1.23x faster                                                         |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.18 ms: 1.22x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 68.2 ms: 1.19x faster                                                        |
| scimark_sor              | 180 ms                                                       | 152 ms: 1.19x faster                                                         |
| json_loads               | 30.3 us                                                      | 25.5 us: 1.19x faster                                                        |
| dask                     | 472 ms                                                       | 400 ms: 1.18x faster                                                         |
| sympy_sum                | 193 ms                                                       | 164 ms: 1.18x faster                                                         |
| 2to3                     | 350 ms                                                       | 300 ms: 1.17x faster                                                         |
| deepcopy                 | 468 us                                                       | 401 us: 1.17x faster                                                         |
| sympy_str                | 360 ms                                                       | 309 ms: 1.17x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 124 ms: 1.16x faster                                                         |
| sympy_expand             | 600 ms                                                       | 518 ms: 1.16x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.59 sec: 1.16x faster                                                       |
| nqueens                  | 115 ms                                                       | 99.8 ms: 1.15x faster                                                        |
| scimark_fft              | 361 ms                                                       | 317 ms: 1.14x faster                                                         |
| mypy2                    | 933 ms                                                       | 828 ms: 1.13x faster                                                         |
| genshi_text              | 31.4 ms                                                      | 28.0 ms: 1.12x faster                                                        |
| sympy_integrate          | 28.2 ms                                                      | 25.1 ms: 1.12x faster                                                        |
| sqlglot_optimize         | 70.1 ms                                                      | 62.9 ms: 1.12x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.10 sec: 1.10x faster                                                       |
| sqlite_synth             | 2.99 us                                                      | 2.71 us: 1.10x faster                                                        |
| async_generators         | 421 ms                                                       | 384 ms: 1.10x faster                                                         |
| xml_etree_generate       | 92.3 ms                                                      | 84.6 ms: 1.09x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 19.6 ms: 1.09x faster                                                        |
| json                     | 5.86 ms                                                      | 5.40 ms: 1.09x faster                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 102 ms: 1.08x faster                                                         |
| xml_etree_parse          | 160 ms                                                       | 148 ms: 1.08x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.72 us: 1.08x faster                                                        |
| regex_v8                 | 27.2 ms                                                      | 25.5 ms: 1.07x faster                                                        |
| regex_dna                | 261 ms                                                       | 245 ms: 1.06x faster                                                         |
| gunicorn                 | 1.16 ms                                                      | 1.10 ms: 1.05x faster                                                        |
| meteor_contest           | 138 ms                                                       | 132 ms: 1.05x faster                                                         |
| aiohttp                  | 1.19 ms                                                      | 1.15 ms: 1.04x faster                                                        |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| genshi_xml               | 63.3 ms                                                      | 61.8 ms: 1.02x faster                                                        |
| create_gc_cycles         | 1.76 ms                                                      | 1.87 ms: 1.06x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.39 us: 1.06x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 32.6 us: 1.11x slower                                                        |
| unpickle                 | 13.5 us                                                      | 15.0 us: 1.11x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.29 ms: 1.15x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.4 ms: 1.17x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.71 ms: 1.20x slower                                                        |
| coverage                 | 63.3 ms                                                      | 78.8 ms: 1.25x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.38 ms: 1.28x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                                 |

Benchmark hidden because not significant (2): unpickle_list, asyncio_websockets
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240410-3.13.0a5+-c181b59-JIT/bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.19x
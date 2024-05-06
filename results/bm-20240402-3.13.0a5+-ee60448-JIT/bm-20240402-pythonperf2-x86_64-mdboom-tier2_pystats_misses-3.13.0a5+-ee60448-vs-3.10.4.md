# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_pystats_misses
- machine: linux-x86_64
- commit hash: ee60448
- commit date: 2024-04-02
- overall geometric mean: 1.25x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 300 ms: 1.17x faster                                                         |
| chameleon      | 9.44 ms                                                      | 7.54 ms: 1.25x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.11 sec: 1.10x faster                                                       |
| html5lib       | 94.6 ms                                                      | 72.6 ms: 1.30x faster                                                        |
| tornado_http   | 157 ms                                                       | 125 ms: 1.26x faster                                                         |
| Geometric mean | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io           | 1.60 sec                                                     | 858 ms: 1.86x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 440 ms: 1.86x faster                                                         |
| async_tree_none         | 692 ms                                                       | 377 ms: 1.84x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 602 ms: 1.56x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.77x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 76.6 ms: 1.45x faster                                                        |
| nbody          | 134 ms                                                       | 95.6 ms: 1.40x faster                                                        |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.28x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 150 ms: 1.27x faster                                                         |
| regex_dna      | 261 ms                                                       | 249 ms: 1.05x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.9 ms: 1.05x faster                                                        |
| regex_effbot   | 3.09 ms                                                      | 3.51 ms: 1.14x slower                                                        |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 311 us: 1.46x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.5 ms: 1.39x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.13 sec: 1.37x faster                                                       |
| unpickle_pure_python | 312 us                                                       | 232 us: 1.35x faster                                                         |
| xml_etree_process    | 75.9 ms                                                      | 58.8 ms: 1.29x faster                                                        |
| json_loads           | 30.3 us                                                      | 25.4 us: 1.19x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 145 ms: 1.10x faster                                                         |
| xml_etree_generate   | 92.3 ms                                                      | 84.9 ms: 1.09x faster                                                        |
| xml_etree_iterparse  | 110 ms                                                       | 102 ms: 1.08x faster                                                         |
| unpickle_list        | 4.65 us                                                      | 4.69 us: 1.01x slower                                                        |
| pickle_list          | 4.12 us                                                      | 4.40 us: 1.07x slower                                                        |
| unpickle             | 13.5 us                                                      | 14.5 us: 1.08x slower                                                        |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 32.8 us: 1.11x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.7 ms: 1.19x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.9 ms: 1.62x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.39x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 14.7 ms                                                      | 9.96 ms: 1.48x faster                                                        |
| genshi_text    | 31.4 ms                                                      | 28.5 ms: 1.10x faster                                                        |
| genshi_xml     | 63.3 ms                                                      | 61.8 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                        | 1.19x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 124 us: 4.34x faster                                                         |
| deltablue                | 7.50 ms                                                      | 3.58 ms: 2.09x faster                                                        |
| asyncio_tcp              | 779 ms                                                       | 376 ms: 2.07x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                       |
| async_tree_io            | 1.60 sec                                                     | 858 ms: 1.86x faster                                                         |
| async_tree_memoization   | 819 ms                                                       | 440 ms: 1.86x faster                                                         |
| async_tree_none          | 692 ms                                                       | 377 ms: 1.84x faster                                                         |
| logging_silent           | 167 ns                                                       | 95.7 ns: 1.75x faster                                                        |
| generators               | 57.3 ms                                                      | 33.2 ms: 1.72x faster                                                        |
| raytrace                 | 489 ms                                                       | 287 ms: 1.70x faster                                                         |
| chaos                    | 109 ms                                                       | 64.1 ms: 1.70x faster                                                        |
| pylint                   | 566 ms                                                       | 340 ms: 1.67x faster                                                         |
| sqlglot_parse            | 2.24 ms                                                      | 1.43 ms: 1.57x faster                                                        |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 602 ms: 1.56x faster                                                         |
| richards_super           | 90.6 ms                                                      | 58.3 ms: 1.56x faster                                                        |
| crypto_pyaes             | 119 ms                                                       | 76.9 ms: 1.55x faster                                                        |
| scimark_monte_carlo      | 107 ms                                                       | 70.6 ms: 1.52x faster                                                        |
| pyflate                  | 733 ms                                                       | 485 ms: 1.51x faster                                                         |
| spectral_norm            | 139 ms                                                       | 92.6 ms: 1.50x faster                                                        |
| richards                 | 75.1 ms                                                      | 50.6 ms: 1.48x faster                                                        |
| mako                     | 14.7 ms                                                      | 9.96 ms: 1.48x faster                                                        |
| go                       | 262 ms                                                       | 177 ms: 1.48x faster                                                         |
| pickle_pure_python       | 455 us                                                       | 311 us: 1.46x faster                                                         |
| sqlglot_transpile        | 2.68 ms                                                      | 1.84 ms: 1.46x faster                                                        |
| float                    | 111 ms                                                       | 76.6 ms: 1.45x faster                                                        |
| nbody                    | 134 ms                                                       | 95.6 ms: 1.40x faster                                                        |
| comprehensions           | 26.7 us                                                      | 19.2 us: 1.39x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.5 ms: 1.39x faster                                                        |
| logging_simple           | 8.88 us                                                      | 6.43 us: 1.38x faster                                                        |
| coroutines               | 30.3 ms                                                      | 22.1 ms: 1.37x faster                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.13 sec: 1.37x faster                                                       |
| logging_format           | 9.64 us                                                      | 7.10 us: 1.36x faster                                                        |
| thrift                   | 1.18 ms                                                      | 871 us: 1.35x faster                                                         |
| unpickle_pure_python     | 312 us                                                       | 232 us: 1.35x faster                                                         |
| scimark_lu               | 167 ms                                                       | 126 ms: 1.32x faster                                                         |
| pycparser                | 1.67 sec                                                     | 1.28 sec: 1.31x faster                                                       |
| html5lib                 | 94.6 ms                                                      | 72.6 ms: 1.30x faster                                                        |
| xml_etree_process        | 75.9 ms                                                      | 58.8 ms: 1.29x faster                                                        |
| hexiom                   | 9.42 ms                                                      | 7.33 ms: 1.29x faster                                                        |
| regex_compile            | 190 ms                                                       | 150 ms: 1.27x faster                                                         |
| deepcopy_memo            | 49.8 us                                                      | 39.4 us: 1.26x faster                                                        |
| tornado_http             | 157 ms                                                       | 125 ms: 1.26x faster                                                         |
| chameleon                | 9.44 ms                                                      | 7.54 ms: 1.25x faster                                                        |
| fannkuch                 | 483 ms                                                       | 386 ms: 1.25x faster                                                         |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.11 ms: 1.24x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 5.17 ms: 1.23x faster                                                        |
| pprint_safe_repr         | 1.05 sec                                                     | 852 ms: 1.23x faster                                                         |
| pprint_pformat           | 2.15 sec                                                     | 1.76 sec: 1.22x faster                                                       |
| json_loads               | 30.3 us                                                      | 25.4 us: 1.19x faster                                                        |
| scimark_sor              | 180 ms                                                       | 152 ms: 1.19x faster                                                         |
| deepcopy                 | 468 us                                                       | 395 us: 1.18x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 122 ms: 1.18x faster                                                         |
| 2to3                     | 350 ms                                                       | 300 ms: 1.17x faster                                                         |
| dask                     | 472 ms                                                       | 405 ms: 1.17x faster                                                         |
| sympy_expand             | 600 ms                                                       | 518 ms: 1.16x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.60 sec: 1.15x faster                                                       |
| scimark_fft              | 361 ms                                                       | 313 ms: 1.15x faster                                                         |
| sympy_sum                | 193 ms                                                       | 167 ms: 1.15x faster                                                         |
| sympy_str                | 360 ms                                                       | 312 ms: 1.15x faster                                                         |
| deepcopy_reduce          | 4.01 us                                                      | 3.51 us: 1.14x faster                                                        |
| dulwich_log              | 81.1 ms                                                      | 71.7 ms: 1.13x faster                                                        |
| sqlglot_optimize         | 70.1 ms                                                      | 62.4 ms: 1.12x faster                                                        |
| mypy2                    | 933 ms                                                       | 834 ms: 1.12x faster                                                         |
| sqlite_synth             | 2.99 us                                                      | 2.68 us: 1.12x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 145 ms: 1.10x faster                                                         |
| genshi_text              | 31.4 ms                                                      | 28.5 ms: 1.10x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.11 sec: 1.10x faster                                                       |
| nqueens                  | 115 ms                                                       | 105 ms: 1.09x faster                                                         |
| sympy_integrate          | 28.2 ms                                                      | 25.9 ms: 1.09x faster                                                        |
| xml_etree_generate       | 92.3 ms                                                      | 84.9 ms: 1.09x faster                                                        |
| pathlib                  | 21.4 ms                                                      | 19.7 ms: 1.08x faster                                                        |
| xml_etree_iterparse      | 110 ms                                                       | 102 ms: 1.08x faster                                                         |
| async_generators         | 421 ms                                                       | 393 ms: 1.07x faster                                                         |
| json                     | 5.86 ms                                                      | 5.48 ms: 1.07x faster                                                        |
| regex_dna                | 261 ms                                                       | 249 ms: 1.05x faster                                                         |
| regex_v8                 | 27.2 ms                                                      | 25.9 ms: 1.05x faster                                                        |
| aiohttp                  | 1.19 ms                                                      | 1.14 ms: 1.04x faster                                                        |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                         |
| gunicorn                 | 1.16 ms                                                      | 1.12 ms: 1.04x faster                                                        |
| meteor_contest           | 138 ms                                                       | 134 ms: 1.03x faster                                                         |
| bench_thread_pool        | 1.14 ms                                                      | 1.11 ms: 1.02x faster                                                        |
| genshi_xml               | 63.3 ms                                                      | 61.8 ms: 1.02x faster                                                        |
| unpickle_list            | 4.65 us                                                      | 4.69 us: 1.01x slower                                                        |
| asyncio_websockets       | 390 ms                                                       | 395 ms: 1.01x slower                                                         |
| create_gc_cycles         | 1.76 ms                                                      | 1.88 ms: 1.07x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.40 us: 1.07x slower                                                        |
| unpickle                 | 13.5 us                                                      | 14.5 us: 1.08x slower                                                        |
| pickle                   | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.01 ms: 1.11x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 32.8 us: 1.11x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.51 ms: 1.14x slower                                                        |
| python_startup           | 11.5 ms                                                      | 13.7 ms: 1.19x slower                                                        |
| coverage                 | 63.3 ms                                                      | 82.9 ms: 1.31x slower                                                        |
| gc_traversal             | 3.42 ms                                                      | 4.84 ms: 1.42x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.9 ms: 1.62x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.25x faster                                                                 |
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-ee60448-JIT/bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.20x
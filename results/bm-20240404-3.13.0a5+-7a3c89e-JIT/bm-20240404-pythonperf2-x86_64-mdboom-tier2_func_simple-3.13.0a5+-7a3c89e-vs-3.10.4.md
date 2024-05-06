# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 7a3c89e
- commit date: 2024-04-04
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 300 ms: 1.16x faster                                                      |
| chameleon      | 9.44 ms                                                      | 7.26 ms: 1.30x faster                                                     |
| docutils       | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                    |
| html5lib       | 94.6 ms                                                      | 73.6 ms: 1.29x faster                                                     |
| tornado_http   | 157 ms                                                       | 122 ms: 1.28x faster                                                      |
| Geometric mean | (ref)                                                        | 1.23x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|-------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 358 ms: 1.93x faster                                                      |
| async_tree_memoization  | 819 ms                                                       | 440 ms: 1.86x faster                                                      |
| async_tree_io           | 1.60 sec                                                     | 886 ms: 1.80x faster                                                      |
| async_tree_cpu_io_mixed | 936 ms                                                       | 595 ms: 1.57x faster                                                      |
| Geometric mean          | (ref)                                                        | 1.79x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 76.4 ms: 1.45x faster                                                     |
| nbody          | 134 ms                                                       | 97.8 ms: 1.37x faster                                                     |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                      |
| Geometric mean | (ref)                                                        | 1.27x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 148 ms: 1.28x faster                                                      |
| regex_dna      | 261 ms                                                       | 242 ms: 1.08x faster                                                      |
| regex_v8       | 27.2 ms                                                      | 25.5 ms: 1.07x faster                                                     |
| regex_effbot   | 3.09 ms                                                      | 3.72 ms: 1.20x slower                                                     |
| Geometric mean | (ref)                                                        | 1.05x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 305 us: 1.49x faster                                                      |
| tomli_loads          | 2.92 sec                                                     | 2.16 sec: 1.35x faster                                                    |
| json_dumps           | 14.5 ms                                                      | 10.8 ms: 1.34x faster                                                     |
| unpickle_pure_python | 312 us                                                       | 233 us: 1.34x faster                                                      |
| xml_etree_process    | 75.9 ms                                                      | 59.0 ms: 1.29x faster                                                     |
| json_loads           | 30.3 us                                                      | 25.3 us: 1.20x faster                                                     |
| xml_etree_parse      | 160 ms                                                       | 143 ms: 1.12x faster                                                      |
| xml_etree_generate   | 92.3 ms                                                      | 84.9 ms: 1.09x faster                                                     |
| xml_etree_iterparse  | 110 ms                                                       | 103 ms: 1.07x faster                                                      |
| pickle_list          | 4.12 us                                                      | 4.41 us: 1.07x slower                                                     |
| pickle               | 9.89 us                                                      | 10.9 us: 1.11x slower                                                     |
| pickle_dict          | 29.5 us                                                      | 32.9 us: 1.11x slower                                                     |
| unpickle             | 13.5 us                                                      | 15.1 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                              |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                     |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.96 ms: 1.48x faster                                                     |
| django_template | 50.2 ms                                                      | 39.9 ms: 1.26x faster                                                     |
| genshi_text     | 31.4 ms                                                      | 26.4 ms: 1.19x faster                                                     |
| genshi_xml      | 63.3 ms                                                      | 57.5 ms: 1.10x faster                                                     |
| Geometric mean  | (ref)                                                        | 1.25x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 120 us: 4.48x faster                                                      |
| asyncio_tcp              | 779 ms                                                       | 372 ms: 2.10x faster                                                      |
| deltablue                | 7.50 ms                                                      | 3.72 ms: 2.01x faster                                                     |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                    |
| async_tree_none          | 692 ms                                                       | 358 ms: 1.93x faster                                                      |
| async_tree_memoization   | 819 ms                                                       | 440 ms: 1.86x faster                                                      |
| async_tree_io            | 1.60 sec                                                     | 886 ms: 1.80x faster                                                      |
| logging_silent           | 167 ns                                                       | 97.0 ns: 1.72x faster                                                     |
| generators               | 57.3 ms                                                      | 33.5 ms: 1.71x faster                                                     |
| chaos                    | 109 ms                                                       | 66.6 ms: 1.63x faster                                                     |
| raytrace                 | 489 ms                                                       | 305 ms: 1.60x faster                                                      |
| sqlglot_parse            | 2.24 ms                                                      | 1.40 ms: 1.60x faster                                                     |
| richards_super           | 90.6 ms                                                      | 57.1 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 595 ms: 1.57x faster                                                      |
| pylint                   | 566 ms                                                       | 363 ms: 1.56x faster                                                      |
| crypto_pyaes             | 119 ms                                                       | 77.4 ms: 1.54x faster                                                     |
| go                       | 262 ms                                                       | 173 ms: 1.52x faster                                                      |
| sqlglot_transpile        | 2.68 ms                                                      | 1.79 ms: 1.50x faster                                                     |
| richards                 | 75.1 ms                                                      | 50.2 ms: 1.50x faster                                                     |
| pickle_pure_python       | 455 us                                                       | 305 us: 1.49x faster                                                      |
| pyflate                  | 733 ms                                                       | 496 ms: 1.48x faster                                                      |
| mako                     | 14.7 ms                                                      | 9.96 ms: 1.48x faster                                                     |
| spectral_norm            | 139 ms                                                       | 94.3 ms: 1.47x faster                                                     |
| scimark_monte_carlo      | 107 ms                                                       | 73.7 ms: 1.46x faster                                                     |
| float                    | 111 ms                                                       | 76.4 ms: 1.45x faster                                                     |
| scimark_lu               | 167 ms                                                       | 119 ms: 1.40x faster                                                      |
| nbody                    | 134 ms                                                       | 97.8 ms: 1.37x faster                                                     |
| coroutines               | 30.3 ms                                                      | 22.4 ms: 1.36x faster                                                     |
| comprehensions           | 26.7 us                                                      | 19.7 us: 1.35x faster                                                     |
| tomli_loads              | 2.92 sec                                                     | 2.16 sec: 1.35x faster                                                    |
| pycparser                | 1.67 sec                                                     | 1.25 sec: 1.34x faster                                                    |
| json_dumps               | 14.5 ms                                                      | 10.8 ms: 1.34x faster                                                     |
| unpickle_pure_python     | 312 us                                                       | 233 us: 1.34x faster                                                      |
| logging_simple           | 8.88 us                                                      | 6.64 us: 1.34x faster                                                     |
| logging_format           | 9.64 us                                                      | 7.29 us: 1.32x faster                                                     |
| thrift                   | 1.18 ms                                                      | 893 us: 1.32x faster                                                      |
| deepcopy_memo            | 49.8 us                                                      | 38.2 us: 1.30x faster                                                     |
| chameleon                | 9.44 ms                                                      | 7.26 ms: 1.30x faster                                                     |
| xml_etree_process        | 75.9 ms                                                      | 59.0 ms: 1.29x faster                                                     |
| html5lib                 | 94.6 ms                                                      | 73.6 ms: 1.29x faster                                                     |
| tornado_http             | 157 ms                                                       | 122 ms: 1.28x faster                                                      |
| regex_compile            | 190 ms                                                       | 148 ms: 1.28x faster                                                      |
| django_template          | 50.2 ms                                                      | 39.9 ms: 1.26x faster                                                     |
| pprint_safe_repr         | 1.05 sec                                                     | 834 ms: 1.26x faster                                                      |
| fannkuch                 | 483 ms                                                       | 384 ms: 1.26x faster                                                      |
| pprint_pformat           | 2.15 sec                                                     | 1.71 sec: 1.26x faster                                                    |
| hexiom                   | 9.42 ms                                                      | 7.52 ms: 1.25x faster                                                     |
| bench_mp_pool            | 6.37 ms                                                      | 5.14 ms: 1.24x faster                                                     |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.09 ms: 1.24x faster                                                     |
| deepcopy                 | 468 us                                                       | 384 us: 1.22x faster                                                      |
| json_loads               | 30.3 us                                                      | 25.3 us: 1.20x faster                                                     |
| sympy_sum                | 193 ms                                                       | 161 ms: 1.19x faster                                                      |
| sympy_str                | 360 ms                                                       | 301 ms: 1.19x faster                                                      |
| genshi_text              | 31.4 ms                                                      | 26.4 ms: 1.19x faster                                                     |
| sympy_expand             | 600 ms                                                       | 507 ms: 1.18x faster                                                      |
| scimark_sor              | 180 ms                                                       | 153 ms: 1.18x faster                                                      |
| sqlglot_normalize        | 144 ms                                                       | 122 ms: 1.18x faster                                                      |
| 2to3                     | 350 ms                                                       | 300 ms: 1.16x faster                                                      |
| dulwich_log              | 81.1 ms                                                      | 69.7 ms: 1.16x faster                                                     |
| deepcopy_reduce          | 4.01 us                                                      | 3.45 us: 1.16x faster                                                     |
| dask                     | 472 ms                                                       | 406 ms: 1.16x faster                                                      |
| scimark_fft              | 361 ms                                                       | 313 ms: 1.16x faster                                                      |
| mdp                      | 3.01 sec                                                     | 2.65 sec: 1.13x faster                                                    |
| mypy2                    | 933 ms                                                       | 824 ms: 1.13x faster                                                      |
| sympy_integrate          | 28.2 ms                                                      | 25.0 ms: 1.13x faster                                                     |
| xml_etree_parse          | 160 ms                                                       | 143 ms: 1.12x faster                                                      |
| nqueens                  | 115 ms                                                       | 103 ms: 1.12x faster                                                      |
| sqlglot_optimize         | 70.1 ms                                                      | 62.8 ms: 1.12x faster                                                     |
| docutils                 | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                    |
| sqlite_synth             | 2.99 us                                                      | 2.70 us: 1.11x faster                                                     |
| genshi_xml               | 63.3 ms                                                      | 57.5 ms: 1.10x faster                                                     |
| pathlib                  | 21.4 ms                                                      | 19.4 ms: 1.10x faster                                                     |
| json                     | 5.86 ms                                                      | 5.37 ms: 1.09x faster                                                     |
| async_generators         | 421 ms                                                       | 385 ms: 1.09x faster                                                      |
| xml_etree_generate       | 92.3 ms                                                      | 84.9 ms: 1.09x faster                                                     |
| regex_dna                | 261 ms                                                       | 242 ms: 1.08x faster                                                      |
| xml_etree_iterparse      | 110 ms                                                       | 103 ms: 1.07x faster                                                      |
| regex_v8                 | 27.2 ms                                                      | 25.5 ms: 1.07x faster                                                     |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.06x faster                                                     |
| aiohttp                  | 1.19 ms                                                      | 1.12 ms: 1.06x faster                                                     |
| meteor_contest           | 138 ms                                                       | 132 ms: 1.04x faster                                                      |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                      |
| bench_thread_pool        | 1.14 ms                                                      | 1.12 ms: 1.02x faster                                                     |
| create_gc_cycles         | 1.76 ms                                                      | 1.79 ms: 1.02x slower                                                     |
| pickle_list              | 4.12 us                                                      | 4.41 us: 1.07x slower                                                     |
| pickle                   | 9.89 us                                                      | 10.9 us: 1.11x slower                                                     |
| pickle_dict              | 29.5 us                                                      | 32.9 us: 1.11x slower                                                     |
| unpickle                 | 13.5 us                                                      | 15.1 us: 1.12x slower                                                     |
| telco                    | 7.23 ms                                                      | 8.22 ms: 1.14x slower                                                     |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                     |
| regex_effbot             | 3.09 ms                                                      | 3.72 ms: 1.20x slower                                                     |
| gc_traversal             | 3.42 ms                                                      | 4.35 ms: 1.27x slower                                                     |
| coverage                 | 63.3 ms                                                      | 80.6 ms: 1.27x slower                                                     |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.60x slower                                                     |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                              |

Benchmark hidden because not significant (2): asyncio_websockets, unpickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-7a3c89e-JIT/bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.19x
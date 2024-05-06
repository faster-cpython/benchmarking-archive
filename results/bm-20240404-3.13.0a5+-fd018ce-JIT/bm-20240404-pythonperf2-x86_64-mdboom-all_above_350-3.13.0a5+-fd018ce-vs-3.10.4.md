# Results vs. 3.10.4

- fork: mdboom
- ref: all_above_350
- machine: linux-x86_64
- commit hash: fd018ce
- commit date: 2024-04-04
- overall geometric mean: 1.25x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 302 ms: 1.16x faster                                                  |
| chameleon      | 9.44 ms                                                      | 7.34 ms: 1.29x faster                                                 |
| docutils       | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                |
| html5lib       | 94.6 ms                                                      | 72.8 ms: 1.30x faster                                                 |
| tornado_http   | 157 ms                                                       | 124 ms: 1.26x faster                                                  |
| Geometric mean | (ref)                                                        | 1.22x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|-------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 359 ms: 1.93x faster                                                  |
| async_tree_memoization  | 819 ms                                                       | 442 ms: 1.86x faster                                                  |
| async_tree_io           | 1.60 sec                                                     | 889 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed | 936 ms                                                       | 597 ms: 1.57x faster                                                  |
| Geometric mean          | (ref)                                                        | 1.78x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 134 ms                                                       | 94.6 ms: 1.42x faster                                                 |
| float          | 111 ms                                                       | 79.5 ms: 1.40x faster                                                 |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                        | 1.27x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 150 ms: 1.27x faster                                                  |
| regex_dna      | 261 ms                                                       | 242 ms: 1.08x faster                                                  |
| regex_v8       | 27.2 ms                                                      | 26.1 ms: 1.04x faster                                                 |
| regex_effbot   | 3.09 ms                                                      | 3.63 ms: 1.18x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 307 us: 1.48x faster                                                  |
| json_dumps           | 14.5 ms                                                      | 10.9 ms: 1.34x faster                                                 |
| xml_etree_process    | 75.9 ms                                                      | 58.2 ms: 1.30x faster                                                 |
| tomli_loads          | 2.92 sec                                                     | 2.24 sec: 1.30x faster                                                |
| unpickle_pure_python | 312 us                                                       | 243 us: 1.29x faster                                                  |
| json_loads           | 30.3 us                                                      | 25.3 us: 1.20x faster                                                 |
| xml_etree_parse      | 160 ms                                                       | 142 ms: 1.13x faster                                                  |
| xml_etree_generate   | 92.3 ms                                                      | 83.6 ms: 1.10x faster                                                 |
| xml_etree_iterparse  | 110 ms                                                       | 103 ms: 1.07x faster                                                  |
| unpickle_list        | 4.65 us                                                      | 4.71 us: 1.01x slower                                                 |
| pickle_dict          | 29.5 us                                                      | 31.0 us: 1.05x slower                                                 |
| pickle               | 9.89 us                                                      | 10.5 us: 1.06x slower                                                 |
| pickle_list          | 4.12 us                                                      | 4.45 us: 1.08x slower                                                 |
| unpickle             | 13.5 us                                                      | 15.0 us: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                 |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.87 ms: 1.49x faster                                                 |
| django_template | 50.2 ms                                                      | 40.9 ms: 1.23x faster                                                 |
| genshi_text     | 31.4 ms                                                      | 27.3 ms: 1.15x faster                                                 |
| genshi_xml      | 63.3 ms                                                      | 58.1 ms: 1.09x faster                                                 |
| Geometric mean  | (ref)                                                        | 1.23x faster                                                          |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|--------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 120 us: 4.47x faster                                                  |
| asyncio_tcp              | 779 ms                                                       | 373 ms: 2.09x faster                                                  |
| deltablue                | 7.50 ms                                                      | 3.79 ms: 1.98x faster                                                 |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                |
| async_tree_none          | 692 ms                                                       | 359 ms: 1.93x faster                                                  |
| async_tree_memoization   | 819 ms                                                       | 442 ms: 1.86x faster                                                  |
| async_tree_io            | 1.60 sec                                                     | 889 ms: 1.80x faster                                                  |
| logging_silent           | 167 ns                                                       | 97.4 ns: 1.72x faster                                                 |
| generators               | 57.3 ms                                                      | 33.6 ms: 1.71x faster                                                 |
| chaos                    | 109 ms                                                       | 67.0 ms: 1.62x faster                                                 |
| raytrace                 | 489 ms                                                       | 308 ms: 1.59x faster                                                  |
| sqlglot_parse            | 2.24 ms                                                      | 1.43 ms: 1.57x faster                                                 |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 597 ms: 1.57x faster                                                  |
| pylint                   | 566 ms                                                       | 365 ms: 1.55x faster                                                  |
| richards_super           | 90.6 ms                                                      | 58.9 ms: 1.54x faster                                                 |
| crypto_pyaes             | 119 ms                                                       | 78.7 ms: 1.52x faster                                                 |
| mako                     | 14.7 ms                                                      | 9.87 ms: 1.49x faster                                                 |
| pickle_pure_python       | 455 us                                                       | 307 us: 1.48x faster                                                  |
| sqlglot_transpile        | 2.68 ms                                                      | 1.82 ms: 1.48x faster                                                 |
| go                       | 262 ms                                                       | 178 ms: 1.47x faster                                                  |
| spectral_norm            | 139 ms                                                       | 95.4 ms: 1.46x faster                                                 |
| pyflate                  | 733 ms                                                       | 507 ms: 1.45x faster                                                  |
| scimark_monte_carlo      | 107 ms                                                       | 74.8 ms: 1.44x faster                                                 |
| richards                 | 75.1 ms                                                      | 52.4 ms: 1.43x faster                                                 |
| nbody                    | 134 ms                                                       | 94.6 ms: 1.42x faster                                                 |
| float                    | 111 ms                                                       | 79.5 ms: 1.40x faster                                                 |
| coroutines               | 30.3 ms                                                      | 22.1 ms: 1.37x faster                                                 |
| comprehensions           | 26.7 us                                                      | 19.7 us: 1.36x faster                                                 |
| logging_format           | 9.64 us                                                      | 7.15 us: 1.35x faster                                                 |
| logging_simple           | 8.88 us                                                      | 6.62 us: 1.34x faster                                                 |
| json_dumps               | 14.5 ms                                                      | 10.9 ms: 1.34x faster                                                 |
| thrift                   | 1.18 ms                                                      | 878 us: 1.34x faster                                                  |
| scimark_lu               | 167 ms                                                       | 125 ms: 1.33x faster                                                  |
| pycparser                | 1.67 sec                                                     | 1.27 sec: 1.32x faster                                                |
| deepcopy_memo            | 49.8 us                                                      | 38.1 us: 1.31x faster                                                 |
| xml_etree_process        | 75.9 ms                                                      | 58.2 ms: 1.30x faster                                                 |
| html5lib                 | 94.6 ms                                                      | 72.8 ms: 1.30x faster                                                 |
| tomli_loads              | 2.92 sec                                                     | 2.24 sec: 1.30x faster                                                |
| chameleon                | 9.44 ms                                                      | 7.34 ms: 1.29x faster                                                 |
| unpickle_pure_python     | 312 us                                                       | 243 us: 1.29x faster                                                  |
| regex_compile            | 190 ms                                                       | 150 ms: 1.27x faster                                                  |
| tornado_http             | 157 ms                                                       | 124 ms: 1.26x faster                                                  |
| pprint_pformat           | 2.15 sec                                                     | 1.72 sec: 1.25x faster                                                |
| pprint_safe_repr         | 1.05 sec                                                     | 843 ms: 1.24x faster                                                  |
| bench_mp_pool            | 6.37 ms                                                      | 5.13 ms: 1.24x faster                                                 |
| fannkuch                 | 483 ms                                                       | 392 ms: 1.23x faster                                                  |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.13 ms: 1.23x faster                                                 |
| django_template          | 50.2 ms                                                      | 40.9 ms: 1.23x faster                                                 |
| hexiom                   | 9.42 ms                                                      | 7.74 ms: 1.22x faster                                                 |
| deepcopy                 | 468 us                                                       | 387 us: 1.21x faster                                                  |
| json_loads               | 30.3 us                                                      | 25.3 us: 1.20x faster                                                 |
| deepcopy_reduce          | 4.01 us                                                      | 3.36 us: 1.19x faster                                                 |
| sympy_sum                | 193 ms                                                       | 163 ms: 1.19x faster                                                  |
| sympy_str                | 360 ms                                                       | 304 ms: 1.18x faster                                                  |
| dask                     | 472 ms                                                       | 402 ms: 1.17x faster                                                  |
| dulwich_log              | 81.1 ms                                                      | 69.6 ms: 1.17x faster                                                 |
| sympy_expand             | 600 ms                                                       | 515 ms: 1.17x faster                                                  |
| scimark_sor              | 180 ms                                                       | 155 ms: 1.17x faster                                                  |
| 2to3                     | 350 ms                                                       | 302 ms: 1.16x faster                                                  |
| genshi_text              | 31.4 ms                                                      | 27.3 ms: 1.15x faster                                                 |
| sqlglot_normalize        | 144 ms                                                       | 125 ms: 1.15x faster                                                  |
| mdp                      | 3.01 sec                                                     | 2.66 sec: 1.13x faster                                                |
| xml_etree_parse          | 160 ms                                                       | 142 ms: 1.13x faster                                                  |
| scimark_fft              | 361 ms                                                       | 321 ms: 1.12x faster                                                  |
| mypy2                    | 933 ms                                                       | 831 ms: 1.12x faster                                                  |
| sympy_integrate          | 28.2 ms                                                      | 25.3 ms: 1.11x faster                                                 |
| docutils                 | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                |
| xml_etree_generate       | 92.3 ms                                                      | 83.6 ms: 1.10x faster                                                 |
| sqlite_synth             | 2.99 us                                                      | 2.72 us: 1.10x faster                                                 |
| json                     | 5.86 ms                                                      | 5.34 ms: 1.10x faster                                                 |
| sqlglot_optimize         | 70.1 ms                                                      | 63.9 ms: 1.10x faster                                                 |
| pathlib                  | 21.4 ms                                                      | 19.5 ms: 1.09x faster                                                 |
| genshi_xml               | 63.3 ms                                                      | 58.1 ms: 1.09x faster                                                 |
| nqueens                  | 115 ms                                                       | 106 ms: 1.08x faster                                                  |
| regex_dna                | 261 ms                                                       | 242 ms: 1.08x faster                                                  |
| async_generators         | 421 ms                                                       | 391 ms: 1.08x faster                                                  |
| xml_etree_iterparse      | 110 ms                                                       | 103 ms: 1.07x faster                                                  |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.07x faster                                                 |
| aiohttp                  | 1.19 ms                                                      | 1.11 ms: 1.07x faster                                                 |
| regex_v8                 | 27.2 ms                                                      | 26.1 ms: 1.04x faster                                                 |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                  |
| bench_thread_pool        | 1.14 ms                                                      | 1.11 ms: 1.03x faster                                                 |
| meteor_contest           | 138 ms                                                       | 135 ms: 1.02x faster                                                  |
| asyncio_websockets       | 390 ms                                                       | 385 ms: 1.01x faster                                                  |
| unpickle_list            | 4.65 us                                                      | 4.71 us: 1.01x slower                                                 |
| create_gc_cycles         | 1.76 ms                                                      | 1.79 ms: 1.02x slower                                                 |
| pickle_dict              | 29.5 us                                                      | 31.0 us: 1.05x slower                                                 |
| pickle                   | 9.89 us                                                      | 10.5 us: 1.06x slower                                                 |
| pickle_list              | 4.12 us                                                      | 4.45 us: 1.08x slower                                                 |
| unpickle                 | 13.5 us                                                      | 15.0 us: 1.11x slower                                                 |
| telco                    | 7.23 ms                                                      | 8.10 ms: 1.12x slower                                                 |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                 |
| regex_effbot             | 3.09 ms                                                      | 3.63 ms: 1.18x slower                                                 |
| coverage                 | 63.3 ms                                                      | 80.3 ms: 1.27x slower                                                 |
| gc_traversal             | 3.42 ms                                                      | 4.36 ms: 1.28x slower                                                 |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                 |
| Geometric mean           | (ref)                                                        | 1.25x faster                                                          |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-fd018ce-JIT/bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.19x
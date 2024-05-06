# Results vs. 3.10.4

- fork: man-group
- ref: io_flush_full_buffer
- machine: linux-x86_64
- commit hash: 9cf294a
- commit date: 2024-03-26
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 278 ms: 1.25x faster                                                        |
| chameleon      | 9.68 ms                                                | 6.93 ms: 1.40x faster                                                       |
| docutils       | 3.30 sec                                               | 2.87 sec: 1.15x faster                                                      |
| html5lib       | 88.9 ms                                                | 66.0 ms: 1.35x faster                                                       |
| tornado_http   | 136 ms                                                 | 96.4 ms: 1.41x faster                                                       |
| Geometric mean | (ref)                                                  | 1.31x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|-------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 374 ms: 1.95x faster                                                        |
| async_tree_io           | 1.77 sec                                               | 919 ms: 1.92x faster                                                        |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                        |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 594 ms: 1.71x faster                                                        |
| Geometric mean          | (ref)                                                  | 1.86x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 93.8 ms: 1.64x faster                                                       |
| float          | 117 ms                                                 | 77.5 ms: 1.51x faster                                                       |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                  | 1.36x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 146 ms: 1.29x faster                                                        |
| regex_v8       | 27.8 ms                                                | 26.2 ms: 1.06x faster                                                       |
| regex_dna      | 227 ms                                                 | 230 ms: 1.01x slower                                                        |
| regex_effbot   | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                  | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 309 us: 1.57x faster                                                        |
| tomli_loads          | 3.14 sec                                               | 2.09 sec: 1.50x faster                                                      |
| unpickle_pure_python | 331 us                                                 | 243 us: 1.36x faster                                                        |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                       |
| xml_etree_process    | 79.1 ms                                                | 61.0 ms: 1.30x faster                                                       |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                       |
| json_loads           | 31.2 us                                                | 28.3 us: 1.10x faster                                                       |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                        |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                        |
| unpickle_list        | 5.20 us                                                | 5.11 us: 1.02x faster                                                       |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                       |
| unpickle             | 14.4 us                                                | 15.2 us: 1.05x slower                                                       |
| pickle               | 10.7 us                                                | 11.8 us: 1.11x slower                                                       |
| pickle_dict          | 29.6 us                                                | 33.5 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                       |
| python_startup_no_site | 5.93 ms                                                | 9.50 ms: 1.60x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                       |
| django_template | 48.2 ms                                                | 36.3 ms: 1.33x faster                                                       |
| genshi_text     | 31.8 ms                                                | 25.3 ms: 1.26x faster                                                       |
| genshi_xml      | 66.0 ms                                                | 56.3 ms: 1.17x faster                                                       |
| Geometric mean  | (ref)                                                  | 1.31x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|--------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.80x faster                                                        |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                                       |
| deltablue                | 7.91 ms                                                | 3.47 ms: 2.28x faster                                                       |
| async_tree_none          | 728 ms                                                 | 374 ms: 1.95x faster                                                        |
| async_tree_io            | 1.77 sec                                               | 919 ms: 1.92x faster                                                        |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                        |
| logging_silent           | 190 ns                                                 | 102 ns: 1.85x faster                                                        |
| asyncio_tcp              | 922 ms                                                 | 504 ms: 1.83x faster                                                        |
| richards_super           | 94.7 ms                                                | 52.3 ms: 1.81x faster                                                       |
| chaos                    | 115 ms                                                 | 64.6 ms: 1.79x faster                                                       |
| raytrace                 | 507 ms                                                 | 293 ms: 1.73x faster                                                        |
| crypto_pyaes             | 128 ms                                                 | 74.6 ms: 1.71x faster                                                       |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 594 ms: 1.71x faster                                                        |
| richards                 | 79.3 ms                                                | 46.4 ms: 1.71x faster                                                       |
| scimark_monte_carlo      | 118 ms                                                 | 71.4 ms: 1.66x faster                                                       |
| scimark_sor              | 220 ms                                                 | 133 ms: 1.65x faster                                                        |
| pylint                   | 551 ms                                                 | 337 ms: 1.64x faster                                                        |
| nbody                    | 154 ms                                                 | 93.8 ms: 1.64x faster                                                       |
| sqlglot_parse            | 2.17 ms                                                | 1.34 ms: 1.62x faster                                                       |
| comprehensions           | 28.8 us                                                | 18.2 us: 1.58x faster                                                       |
| pickle_pure_python       | 484 us                                                 | 309 us: 1.57x faster                                                        |
| coroutines               | 35.1 ms                                                | 22.5 ms: 1.56x faster                                                       |
| sqlglot_transpile        | 2.57 ms                                                | 1.66 ms: 1.55x faster                                                       |
| go                       | 240 ms                                                 | 156 ms: 1.54x faster                                                        |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                       |
| float                    | 117 ms                                                 | 77.5 ms: 1.51x faster                                                       |
| tomli_loads              | 3.14 sec                                               | 2.09 sec: 1.50x faster                                                      |
| pyflate                  | 716 ms                                                 | 480 ms: 1.49x faster                                                        |
| spectral_norm            | 170 ms                                                 | 114 ms: 1.49x faster                                                        |
| deepcopy_memo            | 58.5 us                                                | 39.8 us: 1.47x faster                                                       |
| hexiom                   | 10.4 ms                                                | 7.20 ms: 1.44x faster                                                       |
| tornado_http             | 136 ms                                                 | 96.4 ms: 1.41x faster                                                       |
| chameleon                | 9.68 ms                                                | 6.93 ms: 1.40x faster                                                       |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                      |
| logging_simple           | 8.30 us                                                | 6.00 us: 1.38x faster                                                       |
| logging_format           | 9.09 us                                                | 6.62 us: 1.37x faster                                                       |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.37x faster                                                      |
| unpickle_pure_python     | 331 us                                                 | 243 us: 1.36x faster                                                        |
| pprint_safe_repr         | 1.02 sec                                               | 748 ms: 1.36x faster                                                        |
| html5lib                 | 88.9 ms                                                | 66.0 ms: 1.35x faster                                                       |
| scimark_fft              | 466 ms                                                 | 347 ms: 1.34x faster                                                        |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                       |
| fannkuch                 | 532 ms                                                 | 397 ms: 1.34x faster                                                        |
| django_template          | 48.2 ms                                                | 36.3 ms: 1.33x faster                                                       |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                       |
| scimark_lu               | 176 ms                                                 | 133 ms: 1.32x faster                                                        |
| deepcopy                 | 479 us                                                 | 364 us: 1.31x faster                                                        |
| deepcopy_reduce          | 4.17 us                                                | 3.17 us: 1.31x faster                                                       |
| thrift                   | 1.07 ms                                                | 818 us: 1.31x faster                                                        |
| xml_etree_process        | 79.1 ms                                                | 61.0 ms: 1.30x faster                                                       |
| regex_compile            | 188 ms                                                 | 146 ms: 1.29x faster                                                        |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.04 ms: 1.28x faster                                                       |
| pycparser                | 1.58 sec                                               | 1.23 sec: 1.28x faster                                                      |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.27x faster                                                        |
| genshi_text              | 31.8 ms                                                | 25.3 ms: 1.26x faster                                                       |
| 2to3                     | 348 ms                                                 | 278 ms: 1.25x faster                                                        |
| djangocms                | 38.4 us                                                | 31.2 us: 1.23x faster                                                       |
| sqlglot_optimize         | 69.2 ms                                                | 57.9 ms: 1.20x faster                                                       |
| dulwich_log              | 84.3 ms                                                | 70.6 ms: 1.19x faster                                                       |
| sympy_sum                | 196 ms                                                 | 165 ms: 1.19x faster                                                        |
| sympy_integrate          | 25.8 ms                                                | 21.8 ms: 1.19x faster                                                       |
| sympy_str                | 346 ms                                                 | 292 ms: 1.18x faster                                                        |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                       |
| dask                     | 441 ms                                                 | 374 ms: 1.18x faster                                                        |
| genshi_xml               | 66.0 ms                                                | 56.3 ms: 1.17x faster                                                       |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                                       |
| nqueens                  | 106 ms                                                 | 90.4 ms: 1.17x faster                                                       |
| bench_thread_pool        | 986 us                                                 | 858 us: 1.15x faster                                                        |
| docutils                 | 3.30 sec                                               | 2.87 sec: 1.15x faster                                                      |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                       |
| sympy_expand             | 566 ms                                                 | 494 ms: 1.15x faster                                                        |
| mypy2                    | 894 ms                                                 | 787 ms: 1.14x faster                                                        |
| json_loads               | 31.2 us                                                | 28.3 us: 1.10x faster                                                       |
| pathlib                  | 20.5 ms                                                | 18.9 ms: 1.08x faster                                                       |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                        |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                        |
| json                     | 5.69 ms                                                | 5.29 ms: 1.08x faster                                                       |
| mdp                      | 2.85 sec                                               | 2.65 sec: 1.07x faster                                                      |
| regex_v8                 | 27.8 ms                                                | 26.2 ms: 1.06x faster                                                       |
| sqlite_synth             | 3.02 us                                                | 2.87 us: 1.05x faster                                                       |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                        |
| unpickle_list            | 5.20 us                                                | 5.11 us: 1.02x faster                                                       |
| pickle_list              | 5.08 us                                                | 5.02 us: 1.01x faster                                                       |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                        |
| regex_dna                | 227 ms                                                 | 230 ms: 1.01x slower                                                        |
| regex_effbot             | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                       |
| asyncio_websockets       | 559 ms                                                 | 570 ms: 1.02x slower                                                        |
| async_generators         | 444 ms                                                 | 462 ms: 1.04x slower                                                        |
| create_gc_cycles         | 1.62 ms                                                | 1.69 ms: 1.04x slower                                                       |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.05x slower                                                       |
| gc_traversal             | 3.62 ms                                                | 3.94 ms: 1.09x slower                                                       |
| pickle                   | 10.7 us                                                | 11.8 us: 1.11x slower                                                       |
| pickle_dict              | 29.6 us                                                | 33.5 us: 1.13x slower                                                       |
| telco                    | 7.27 ms                                                | 8.59 ms: 1.18x slower                                                       |
| coverage                 | 79.4 ms                                                | 98.7 ms: 1.24x slower                                                       |
| python_startup_no_site   | 5.93 ms                                                | 9.50 ms: 1.60x slower                                                       |
| Geometric mean           | (ref)                                                  | 1.31x faster                                                                |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240326-3.13.0a5+-9cf294a-JIT/bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x
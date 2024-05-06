# Results vs. 3.10.4

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 34584c3
- commit date: 2024-04-16
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 271 ms: 1.29x faster                                                |
| chameleon      | 9.68 ms                                                | 6.96 ms: 1.39x faster                                               |
| docutils       | 3.30 sec                                               | 2.83 sec: 1.16x faster                                              |
| html5lib       | 88.9 ms                                                | 67.2 ms: 1.32x faster                                               |
| tornado_http   | 136 ms                                                 | 94.2 ms: 1.45x faster                                               |
| Geometric mean | (ref)                                                  | 1.32x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 357 ms: 2.04x faster                                                |
| async_tree_io           | 1.77 sec                                               | 930 ms: 1.90x faster                                                |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 608 ms: 1.67x faster                                                |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 91.1 ms: 1.69x faster                                               |
| float          | 117 ms                                                 | 78.9 ms: 1.48x faster                                               |
| pidigits       | 191 ms                                                 | 193 ms: 1.01x slower                                                |
| Geometric mean | (ref)                                                  | 1.35x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 136 ms: 1.39x faster                                                |
| regex_v8       | 27.8 ms                                                | 24.9 ms: 1.11x faster                                               |
| regex_dna      | 227 ms                                                 | 222 ms: 1.02x faster                                                |
| regex_effbot   | 3.63 ms                                                | 3.71 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                  | 1.12x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 302 us: 1.60x faster                                                |
| unpickle_pure_python | 331 us                                                 | 220 us: 1.50x faster                                                |
| tomli_loads          | 3.14 sec                                               | 2.21 sec: 1.42x faster                                              |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                               |
| xml_etree_process    | 79.1 ms                                                | 60.8 ms: 1.30x faster                                               |
| json_loads           | 31.2 us                                                | 27.8 us: 1.12x faster                                               |
| xml_etree_generate   | 99.4 ms                                                | 88.7 ms: 1.12x faster                                               |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                |
| xml_etree_parse      | 168 ms                                                 | 162 ms: 1.04x faster                                                |
| unpickle_list        | 5.20 us                                                | 5.03 us: 1.03x faster                                               |
| pickle_list          | 5.08 us                                                | 5.40 us: 1.06x slower                                               |
| pickle               | 10.7 us                                                | 12.0 us: 1.13x slower                                               |
| unpickle             | 14.4 us                                                | 17.0 us: 1.18x slower                                               |
| pickle_dict          | 29.6 us                                                | 35.4 us: 1.20x slower                                               |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                               |
| python_startup_no_site | 5.93 ms                                                | 7.13 ms: 1.20x slower                                               |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.0 ms: 1.48x faster                                               |
| django_template | 48.2 ms                                                | 35.1 ms: 1.37x faster                                               |
| genshi_text     | 31.8 ms                                                | 23.9 ms: 1.33x faster                                               |
| genshi_xml      | 66.0 ms                                                | 52.9 ms: 1.25x faster                                               |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 116 us: 4.70x faster                                                |
| generators               | 80.1 ms                                                | 29.7 ms: 2.70x faster                                               |
| deltablue                | 7.91 ms                                                | 3.29 ms: 2.40x faster                                               |
| async_tree_none          | 728 ms                                                 | 357 ms: 2.04x faster                                                |
| raytrace                 | 507 ms                                                 | 263 ms: 1.93x faster                                                |
| chaos                    | 115 ms                                                 | 60.2 ms: 1.92x faster                                               |
| async_tree_io            | 1.77 sec                                               | 930 ms: 1.90x faster                                                |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                |
| asyncio_tcp              | 922 ms                                                 | 507 ms: 1.82x faster                                                |
| scimark_sor              | 220 ms                                                 | 122 ms: 1.80x faster                                                |
| richards_super           | 94.7 ms                                                | 54.4 ms: 1.74x faster                                               |
| scimark_monte_carlo      | 118 ms                                                 | 68.5 ms: 1.73x faster                                               |
| pylint                   | 551 ms                                                 | 320 ms: 1.72x faster                                                |
| crypto_pyaes             | 128 ms                                                 | 74.7 ms: 1.71x faster                                               |
| nbody                    | 154 ms                                                 | 91.1 ms: 1.69x faster                                               |
| comprehensions           | 28.8 us                                                | 17.1 us: 1.68x faster                                               |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                               |
| go                       | 240 ms                                                 | 143 ms: 1.67x faster                                                |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 608 ms: 1.67x faster                                                |
| richards                 | 79.3 ms                                                | 48.4 ms: 1.64x faster                                               |
| hexiom                   | 10.4 ms                                                | 6.37 ms: 1.63x faster                                               |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                               |
| pickle_pure_python       | 484 us                                                 | 302 us: 1.60x faster                                                |
| pyflate                  | 716 ms                                                 | 467 ms: 1.53x faster                                                |
| scimark_lu               | 176 ms                                                 | 115 ms: 1.53x faster                                                |
| coroutines               | 35.1 ms                                                | 23.0 ms: 1.53x faster                                               |
| deepcopy_memo            | 58.5 us                                                | 38.3 us: 1.53x faster                                               |
| unpickle_pure_python     | 331 us                                                 | 220 us: 1.50x faster                                                |
| spectral_norm            | 170 ms                                                 | 113 ms: 1.50x faster                                                |
| mako                     | 16.3 ms                                                | 11.0 ms: 1.48x faster                                               |
| float                    | 117 ms                                                 | 78.9 ms: 1.48x faster                                               |
| tornado_http             | 136 ms                                                 | 94.2 ms: 1.45x faster                                               |
| logging_simple           | 8.30 us                                                | 5.78 us: 1.44x faster                                               |
| tomli_loads              | 3.14 sec                                               | 2.21 sec: 1.42x faster                                              |
| logging_format           | 9.09 us                                                | 6.42 us: 1.42x faster                                               |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                              |
| chameleon                | 9.68 ms                                                | 6.96 ms: 1.39x faster                                               |
| regex_compile            | 188 ms                                                 | 136 ms: 1.39x faster                                                |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                               |
| fannkuch                 | 532 ms                                                 | 387 ms: 1.37x faster                                                |
| django_template          | 48.2 ms                                                | 35.1 ms: 1.37x faster                                               |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                              |
| pprint_pformat           | 2.10 sec                                               | 1.55 sec: 1.36x faster                                              |
| deepcopy                 | 479 us                                                 | 354 us: 1.36x faster                                                |
| pprint_safe_repr         | 1.02 sec                                               | 754 ms: 1.35x faster                                                |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                               |
| genshi_text              | 31.8 ms                                                | 23.9 ms: 1.33x faster                                               |
| html5lib                 | 88.9 ms                                                | 67.2 ms: 1.32x faster                                               |
| deepcopy_reduce          | 4.17 us                                                | 3.18 us: 1.31x faster                                               |
| thrift                   | 1.07 ms                                                | 823 us: 1.30x faster                                                |
| xml_etree_process        | 79.1 ms                                                | 60.8 ms: 1.30x faster                                               |
| nqueens                  | 106 ms                                                 | 81.6 ms: 1.30x faster                                               |
| 2to3                     | 348 ms                                                 | 271 ms: 1.29x faster                                                |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.28x faster                                                |
| dulwich_log              | 84.3 ms                                                | 66.7 ms: 1.26x faster                                               |
| sympy_integrate          | 25.8 ms                                                | 20.5 ms: 1.26x faster                                               |
| scimark_fft              | 466 ms                                                 | 370 ms: 1.26x faster                                                |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.17 ms: 1.25x faster                                               |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.25x faster                                                |
| genshi_xml               | 66.0 ms                                                | 52.9 ms: 1.25x faster                                               |
| sqlglot_optimize         | 69.2 ms                                                | 55.6 ms: 1.24x faster                                               |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                               |
| sympy_str                | 346 ms                                                 | 282 ms: 1.23x faster                                                |
| djangocms                | 38.4 us                                                | 31.9 us: 1.21x faster                                               |
| mypy2                    | 894 ms                                                 | 741 ms: 1.21x faster                                                |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                               |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                |
| sympy_expand             | 566 ms                                                 | 473 ms: 1.20x faster                                                |
| bench_thread_pool        | 986 us                                                 | 838 us: 1.18x faster                                                |
| pathlib                  | 20.5 ms                                                | 17.5 ms: 1.17x faster                                               |
| docutils                 | 3.30 sec                                               | 2.83 sec: 1.16x faster                                              |
| json_loads               | 31.2 us                                                | 27.8 us: 1.12x faster                                               |
| xml_etree_generate       | 99.4 ms                                                | 88.7 ms: 1.12x faster                                               |
| regex_v8                 | 27.8 ms                                                | 24.9 ms: 1.11x faster                                               |
| mdp                      | 2.85 sec                                               | 2.59 sec: 1.10x faster                                              |
| json                     | 5.69 ms                                                | 5.25 ms: 1.08x faster                                               |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.07x faster                                                |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                |
| xml_etree_parse          | 168 ms                                                 | 162 ms: 1.04x faster                                                |
| unpickle_list            | 5.20 us                                                | 5.03 us: 1.03x faster                                               |
| sqlite_synth             | 3.02 us                                                | 2.94 us: 1.03x faster                                               |
| regex_dna                | 227 ms                                                 | 222 ms: 1.02x faster                                                |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                               |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                |
| pidigits                 | 191 ms                                                 | 193 ms: 1.01x slower                                                |
| regex_effbot             | 3.63 ms                                                | 3.71 ms: 1.02x slower                                               |
| pickle_list              | 5.08 us                                                | 5.40 us: 1.06x slower                                               |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                               |
| gc_traversal             | 3.62 ms                                                | 3.96 ms: 1.09x slower                                               |
| pickle                   | 10.7 us                                                | 12.0 us: 1.13x slower                                               |
| unpickle                 | 14.4 us                                                | 17.0 us: 1.18x slower                                               |
| telco                    | 7.27 ms                                                | 8.65 ms: 1.19x slower                                               |
| pickle_dict              | 29.6 us                                                | 35.4 us: 1.20x slower                                               |
| python_startup_no_site   | 5.93 ms                                                | 7.13 ms: 1.20x slower                                               |
| coverage                 | 79.4 ms                                                | 96.8 ms: 1.22x slower                                               |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                        |

Benchmark hidden because not significant (1): async_generators
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240416-3.13.0a6+-34584c3/bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x
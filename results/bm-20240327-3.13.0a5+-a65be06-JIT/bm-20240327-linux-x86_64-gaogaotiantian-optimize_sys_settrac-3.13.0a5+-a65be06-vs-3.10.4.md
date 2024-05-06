# Results vs. 3.10.4

- fork: gaogaotiantian
- ref: optimize_sys_settrac
- machine: linux-x86_64
- commit hash: a65be06
- commit date: 2024-03-27
- overall geometric mean: 1.30x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 280 ms: 1.25x faster                                                           |
| chameleon      | 9.68 ms                                                | 7.00 ms: 1.38x faster                                                          |
| docutils       | 3.30 sec                                               | 2.89 sec: 1.14x faster                                                         |
| html5lib       | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                          |
| tornado_http   | 136 ms                                                 | 96.9 ms: 1.41x faster                                                          |
| Geometric mean | (ref)                                                  | 1.29x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 357 ms: 2.04x faster                                                           |
| async_tree_io           | 1.77 sec                                               | 923 ms: 1.92x faster                                                           |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                           |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 611 ms: 1.66x faster                                                           |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 92.5 ms: 1.66x faster                                                          |
| float          | 117 ms                                                 | 76.4 ms: 1.53x faster                                                          |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 147 ms: 1.28x faster                                                           |
| regex_v8       | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                          |
| regex_dna      | 227 ms                                                 | 219 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                   |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 311 us: 1.56x faster                                                           |
| tomli_loads          | 3.14 sec                                               | 2.09 sec: 1.50x faster                                                         |
| unpickle_pure_python | 331 us                                                 | 245 us: 1.35x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                          |
| xml_etree_process    | 79.1 ms                                                | 60.8 ms: 1.30x faster                                                          |
| xml_etree_generate   | 99.4 ms                                                | 88.8 ms: 1.12x faster                                                          |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                           |
| json_loads           | 31.2 us                                                | 29.3 us: 1.07x faster                                                          |
| xml_etree_parse      | 168 ms                                                 | 162 ms: 1.03x faster                                                           |
| pickle_list          | 5.08 us                                                | 5.04 us: 1.01x faster                                                          |
| unpickle             | 14.4 us                                                | 15.5 us: 1.08x slower                                                          |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                          |
| pickle_dict          | 29.6 us                                                | 36.0 us: 1.22x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.12x faster                                                                   |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                          |
| python_startup_no_site | 5.93 ms                                                | 9.56 ms: 1.61x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.11x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                          |
| django_template | 48.2 ms                                                | 36.0 ms: 1.34x faster                                                          |
| genshi_text     | 31.8 ms                                                | 25.0 ms: 1.27x faster                                                          |
| genshi_xml      | 66.0 ms                                                | 55.8 ms: 1.18x faster                                                          |
| Geometric mean  | (ref)                                                  | 1.32x faster                                                                   |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 111 us: 4.91x faster                                                           |
| generators               | 80.1 ms                                                | 30.1 ms: 2.66x faster                                                          |
| deltablue                | 7.91 ms                                                | 3.53 ms: 2.24x faster                                                          |
| async_tree_none          | 728 ms                                                 | 357 ms: 2.04x faster                                                           |
| async_tree_io            | 1.77 sec                                               | 923 ms: 1.92x faster                                                           |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                           |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                                           |
| chaos                    | 115 ms                                                 | 63.4 ms: 1.82x faster                                                          |
| logging_silent           | 190 ns                                                 | 105 ns: 1.81x faster                                                           |
| richards_super           | 94.7 ms                                                | 53.2 ms: 1.78x faster                                                          |
| raytrace                 | 507 ms                                                 | 296 ms: 1.71x faster                                                           |
| crypto_pyaes             | 128 ms                                                 | 74.8 ms: 1.71x faster                                                          |
| scimark_monte_carlo      | 118 ms                                                 | 70.3 ms: 1.68x faster                                                          |
| richards                 | 79.3 ms                                                | 47.2 ms: 1.68x faster                                                          |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 611 ms: 1.66x faster                                                           |
| nbody                    | 154 ms                                                 | 92.5 ms: 1.66x faster                                                          |
| pylint                   | 551 ms                                                 | 336 ms: 1.64x faster                                                           |
| scimark_sor              | 220 ms                                                 | 134 ms: 1.64x faster                                                           |
| sqlglot_parse            | 2.17 ms                                                | 1.34 ms: 1.62x faster                                                          |
| comprehensions           | 28.8 us                                                | 18.4 us: 1.56x faster                                                          |
| pickle_pure_python       | 484 us                                                 | 311 us: 1.56x faster                                                           |
| sqlglot_transpile        | 2.57 ms                                                | 1.66 ms: 1.55x faster                                                          |
| go                       | 240 ms                                                 | 155 ms: 1.55x faster                                                           |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                          |
| float                    | 117 ms                                                 | 76.4 ms: 1.53x faster                                                          |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                          |
| tomli_loads              | 3.14 sec                                               | 2.09 sec: 1.50x faster                                                         |
| spectral_norm            | 170 ms                                                 | 115 ms: 1.48x faster                                                           |
| deepcopy_memo            | 58.5 us                                                | 39.7 us: 1.47x faster                                                          |
| pyflate                  | 716 ms                                                 | 488 ms: 1.47x faster                                                           |
| hexiom                   | 10.4 ms                                                | 7.29 ms: 1.43x faster                                                          |
| tornado_http             | 136 ms                                                 | 96.9 ms: 1.41x faster                                                          |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                         |
| pprint_pformat           | 2.10 sec                                               | 1.52 sec: 1.39x faster                                                         |
| chameleon                | 9.68 ms                                                | 7.00 ms: 1.38x faster                                                          |
| logging_simple           | 8.30 us                                                | 6.01 us: 1.38x faster                                                          |
| logging_format           | 9.09 us                                                | 6.64 us: 1.37x faster                                                          |
| pprint_safe_repr         | 1.02 sec                                               | 748 ms: 1.36x faster                                                           |
| scimark_fft              | 466 ms                                                 | 343 ms: 1.36x faster                                                           |
| unpickle_pure_python     | 331 us                                                 | 245 us: 1.35x faster                                                           |
| django_template          | 48.2 ms                                                | 36.0 ms: 1.34x faster                                                          |
| deepcopy                 | 479 us                                                 | 360 us: 1.33x faster                                                           |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                          |
| pycparser                | 1.58 sec                                               | 1.19 sec: 1.33x faster                                                         |
| scimark_lu               | 176 ms                                                 | 133 ms: 1.33x faster                                                           |
| fannkuch                 | 532 ms                                                 | 403 ms: 1.32x faster                                                           |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                          |
| html5lib                 | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                          |
| xml_etree_process        | 79.1 ms                                                | 60.8 ms: 1.30x faster                                                          |
| deepcopy_reduce          | 4.17 us                                                | 3.21 us: 1.30x faster                                                          |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.01 ms: 1.29x faster                                                          |
| thrift                   | 1.07 ms                                                | 831 us: 1.29x faster                                                           |
| regex_compile            | 188 ms                                                 | 147 ms: 1.28x faster                                                           |
| genshi_text              | 31.8 ms                                                | 25.0 ms: 1.27x faster                                                          |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.26x faster                                                           |
| 2to3                     | 348 ms                                                 | 280 ms: 1.25x faster                                                           |
| djangocms                | 38.4 us                                                | 32.0 us: 1.20x faster                                                          |
| dulwich_log              | 84.3 ms                                                | 70.7 ms: 1.19x faster                                                          |
| sqlglot_optimize         | 69.2 ms                                                | 58.0 ms: 1.19x faster                                                          |
| sympy_str                | 346 ms                                                 | 291 ms: 1.19x faster                                                           |
| sympy_sum                | 196 ms                                                 | 166 ms: 1.18x faster                                                           |
| genshi_xml               | 66.0 ms                                                | 55.8 ms: 1.18x faster                                                          |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                          |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                                          |
| nqueens                  | 106 ms                                                 | 90.2 ms: 1.17x faster                                                          |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                                          |
| dask                     | 441 ms                                                 | 378 ms: 1.16x faster                                                           |
| bench_thread_pool        | 986 us                                                 | 860 us: 1.15x faster                                                           |
| sympy_expand             | 566 ms                                                 | 495 ms: 1.14x faster                                                           |
| docutils                 | 3.30 sec                                               | 2.89 sec: 1.14x faster                                                         |
| mypy2                    | 894 ms                                                 | 787 ms: 1.14x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 88.8 ms: 1.12x faster                                                          |
| regex_v8                 | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                          |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                          |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                           |
| mdp                      | 2.85 sec                                               | 2.66 sec: 1.07x faster                                                         |
| json_loads               | 31.2 us                                                | 29.3 us: 1.07x faster                                                          |
| meteor_contest           | 120 ms                                                 | 112 ms: 1.06x faster                                                           |
| json                     | 5.69 ms                                                | 5.40 ms: 1.05x faster                                                          |
| sqlite_synth             | 3.02 us                                                | 2.89 us: 1.05x faster                                                          |
| regex_dna                | 227 ms                                                 | 219 ms: 1.04x faster                                                           |
| xml_etree_parse          | 168 ms                                                 | 162 ms: 1.03x faster                                                           |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                           |
| pickle_list              | 5.08 us                                                | 5.04 us: 1.01x faster                                                          |
| asyncio_websockets       | 559 ms                                                 | 569 ms: 1.02x slower                                                           |
| async_generators         | 444 ms                                                 | 464 ms: 1.05x slower                                                           |
| create_gc_cycles         | 1.62 ms                                                | 1.70 ms: 1.05x slower                                                          |
| unpickle                 | 14.4 us                                                | 15.5 us: 1.08x slower                                                          |
| gc_traversal             | 3.62 ms                                                | 3.95 ms: 1.09x slower                                                          |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                          |
| telco                    | 7.27 ms                                                | 8.59 ms: 1.18x slower                                                          |
| pickle_dict              | 29.6 us                                                | 36.0 us: 1.22x slower                                                          |
| coverage                 | 79.4 ms                                                | 98.1 ms: 1.23x slower                                                          |
| unpack_sequence          | 60.0 ns                                                | 85.5 ns: 1.42x slower                                                          |
| python_startup_no_site   | 5.93 ms                                                | 9.56 ms: 1.61x slower                                                          |
| Geometric mean           | (ref)                                                  | 1.30x faster                                                                   |

Benchmark hidden because not significant (3): regex_effbot, bench_mp_pool, unpickle_list
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240327-3.13.0a5+-a65be06-JIT/bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x
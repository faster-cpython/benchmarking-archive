# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 7819b1c
- commit date: 2024-05-03
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 270 ms: 1.29x faster                                                    |
| chameleon      | 9.68 ms                                                | 6.96 ms: 1.39x faster                                                   |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                  |
| html5lib       | 88.9 ms                                                | 67.0 ms: 1.33x faster                                                   |
| tornado_http   | 136 ms                                                 | 94.1 ms: 1.45x faster                                                   |
| Geometric mean | (ref)                                                  | 1.32x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 353 ms: 2.06x faster                                                    |
| async_tree_io           | 1.77 sec                                               | 923 ms: 1.92x faster                                                    |
| async_tree_memoization  | 870 ms                                                 | 457 ms: 1.90x faster                                                    |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 617 ms: 1.65x faster                                                    |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 85.7 ms: 1.79x faster                                                   |
| float          | 117 ms                                                 | 79.2 ms: 1.48x faster                                                   |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                  | 1.39x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.41x faster                                                    |
| regex_v8       | 27.8 ms                                                | 25.9 ms: 1.07x faster                                                   |
| regex_dna      | 227 ms                                                 | 229 ms: 1.01x slower                                                    |
| regex_effbot   | 3.63 ms                                                | 3.84 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.09x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 305 us: 1.59x faster                                                    |
| unpickle_pure_python | 331 us                                                 | 216 us: 1.53x faster                                                    |
| tomli_loads          | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                  |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                   |
| xml_etree_process    | 79.1 ms                                                | 61.1 ms: 1.29x faster                                                   |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                   |
| xml_etree_generate   | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                   |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.09x faster                                                    |
| xml_etree_parse      | 168 ms                                                 | 158 ms: 1.06x faster                                                    |
| unpickle_list        | 5.20 us                                                | 5.14 us: 1.01x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.32 us: 1.05x slower                                                   |
| unpickle             | 14.4 us                                                | 15.2 us: 1.05x slower                                                   |
| pickle               | 10.7 us                                                | 11.8 us: 1.10x slower                                                   |
| pickle_dict          | 29.6 us                                                | 35.7 us: 1.21x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                   |
| python_startup_no_site | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                   |
| django_template | 48.2 ms                                                | 34.6 ms: 1.39x faster                                                   |
| genshi_text     | 31.8 ms                                                | 23.2 ms: 1.37x faster                                                   |
| genshi_xml      | 66.0 ms                                                | 50.9 ms: 1.30x faster                                                   |
| Geometric mean  | (ref)                                                  | 1.39x faster                                                            |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 166 us: 3.28x faster                                                    |
| generators               | 80.1 ms                                                | 29.0 ms: 2.77x faster                                                   |
| deltablue                | 7.91 ms                                                | 3.24 ms: 2.44x faster                                                   |
| async_tree_none          | 728 ms                                                 | 353 ms: 2.06x faster                                                    |
| async_tree_io            | 1.77 sec                                               | 923 ms: 1.92x faster                                                    |
| raytrace                 | 507 ms                                                 | 265 ms: 1.91x faster                                                    |
| chaos                    | 115 ms                                                 | 60.6 ms: 1.91x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 457 ms: 1.90x faster                                                    |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                    |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                                    |
| nbody                    | 154 ms                                                 | 85.7 ms: 1.79x faster                                                   |
| richards_super           | 94.7 ms                                                | 54.2 ms: 1.75x faster                                                   |
| scimark_monte_carlo      | 118 ms                                                 | 67.6 ms: 1.75x faster                                                   |
| comprehensions           | 28.8 us                                                | 16.5 us: 1.74x faster                                                   |
| pylint                   | 551 ms                                                 | 320 ms: 1.73x faster                                                    |
| crypto_pyaes             | 128 ms                                                 | 74.1 ms: 1.72x faster                                                   |
| hexiom                   | 10.4 ms                                                | 6.12 ms: 1.70x faster                                                   |
| go                       | 240 ms                                                 | 144 ms: 1.67x faster                                                    |
| sqlglot_parse            | 2.17 ms                                                | 1.30 ms: 1.66x faster                                                   |
| scimark_sor              | 220 ms                                                 | 132 ms: 1.66x faster                                                    |
| richards                 | 79.3 ms                                                | 47.9 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 617 ms: 1.65x faster                                                    |
| sqlglot_transpile        | 2.57 ms                                                | 1.61 ms: 1.59x faster                                                   |
| pickle_pure_python       | 484 us                                                 | 305 us: 1.59x faster                                                    |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                   |
| unpickle_pure_python     | 331 us                                                 | 216 us: 1.53x faster                                                    |
| scimark_lu               | 176 ms                                                 | 116 ms: 1.52x faster                                                    |
| deepcopy_memo            | 58.5 us                                                | 38.5 us: 1.52x faster                                                   |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                   |
| pyflate                  | 716 ms                                                 | 477 ms: 1.50x faster                                                    |
| float                    | 117 ms                                                 | 79.2 ms: 1.48x faster                                                   |
| spectral_norm            | 170 ms                                                 | 116 ms: 1.46x faster                                                    |
| tornado_http             | 136 ms                                                 | 94.1 ms: 1.45x faster                                                   |
| tomli_loads              | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                  |
| logging_simple           | 8.30 us                                                | 5.76 us: 1.44x faster                                                   |
| logging_format           | 9.09 us                                                | 6.34 us: 1.43x faster                                                   |
| regex_compile            | 188 ms                                                 | 134 ms: 1.41x faster                                                    |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.39x faster                                                  |
| django_template          | 48.2 ms                                                | 34.6 ms: 1.39x faster                                                   |
| chameleon                | 9.68 ms                                                | 6.96 ms: 1.39x faster                                                   |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                   |
| genshi_text              | 31.8 ms                                                | 23.2 ms: 1.37x faster                                                   |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.37x faster                                                  |
| fannkuch                 | 532 ms                                                 | 392 ms: 1.36x faster                                                    |
| pprint_safe_repr         | 1.02 sec                                               | 753 ms: 1.35x faster                                                    |
| deepcopy                 | 479 us                                                 | 359 us: 1.34x faster                                                    |
| nqueens                  | 106 ms                                                 | 79.3 ms: 1.33x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                   |
| html5lib                 | 88.9 ms                                                | 67.0 ms: 1.33x faster                                                   |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.31x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                    |
| genshi_xml               | 66.0 ms                                                | 50.9 ms: 1.30x faster                                                   |
| thrift                   | 1.07 ms                                                | 826 us: 1.30x faster                                                    |
| xml_etree_process        | 79.1 ms                                                | 61.1 ms: 1.29x faster                                                   |
| 2to3                     | 348 ms                                                 | 270 ms: 1.29x faster                                                    |
| deepcopy_reduce          | 4.17 us                                                | 3.27 us: 1.28x faster                                                   |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.27x faster                                                   |
| sqlglot_optimize         | 69.2 ms                                                | 54.8 ms: 1.26x faster                                                   |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                                    |
| dulwich_log              | 84.3 ms                                                | 67.0 ms: 1.26x faster                                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.15 ms: 1.26x faster                                                   |
| scimark_fft              | 466 ms                                                 | 371 ms: 1.26x faster                                                    |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                    |
| aiohttp                  | 1.44 ms                                                | 1.18 ms: 1.22x faster                                                   |
| mypy2                    | 894 ms                                                 | 738 ms: 1.21x faster                                                    |
| sympy_expand             | 566 ms                                                 | 471 ms: 1.20x faster                                                    |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                    |
| gunicorn                 | 1.53 ms                                                | 1.28 ms: 1.20x faster                                                   |
| djangocms                | 38.4 us                                                | 32.2 us: 1.19x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 831 us: 1.19x faster                                                    |
| pathlib                  | 20.5 ms                                                | 17.4 ms: 1.17x faster                                                   |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                  |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                   |
| xml_etree_generate       | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                   |
| json                     | 5.69 ms                                                | 5.21 ms: 1.09x faster                                                   |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.09x faster                                                    |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.07x faster                                                    |
| regex_v8                 | 27.8 ms                                                | 25.9 ms: 1.07x faster                                                   |
| xml_etree_parse          | 168 ms                                                 | 158 ms: 1.06x faster                                                    |
| sqlite_synth             | 3.02 us                                                | 2.92 us: 1.03x faster                                                   |
| mdp                      | 2.85 sec                                               | 2.75 sec: 1.03x faster                                                  |
| unpickle_list            | 5.20 us                                                | 5.14 us: 1.01x faster                                                   |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                    |
| async_generators         | 444 ms                                                 | 442 ms: 1.00x faster                                                    |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                   |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                    |
| regex_dna                | 227 ms                                                 | 229 ms: 1.01x slower                                                    |
| gc_traversal             | 3.62 ms                                                | 3.74 ms: 1.03x slower                                                   |
| flaskblogging            | 8.58 ms                                                | 8.93 ms: 1.04x slower                                                   |
| pickle_list              | 5.08 us                                                | 5.32 us: 1.05x slower                                                   |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.05x slower                                                   |
| regex_effbot             | 3.63 ms                                                | 3.84 ms: 1.06x slower                                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                   |
| pickle                   | 10.7 us                                                | 11.8 us: 1.10x slower                                                   |
| coverage                 | 79.4 ms                                                | 92.5 ms: 1.16x slower                                                   |
| telco                    | 7.27 ms                                                | 8.55 ms: 1.18x slower                                                   |
| python_startup_no_site   | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                   |
| pickle_dict              | 29.6 us                                                | 35.7 us: 1.21x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                            |
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240503-3.13.0a6+-7819b1c/bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: 1.10x
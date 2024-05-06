# Results vs. 3.10.4

- fork: gvanrossum
- ref: tier2_flag
- machine: linux-x86_64
- commit hash: 8cb71dd
- commit date: 2024-04-26
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 267 ms: 1.31x faster                                             |
| chameleon      | 9.68 ms                                                | 6.96 ms: 1.39x faster                                            |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                           |
| html5lib       | 88.9 ms                                                | 66.8 ms: 1.33x faster                                            |
| tornado_http   | 136 ms                                                 | 94.2 ms: 1.45x faster                                            |
| Geometric mean | (ref)                                                  | 1.33x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 353 ms: 2.06x faster                                             |
| async_tree_io           | 1.77 sec                                               | 919 ms: 1.92x faster                                             |
| async_tree_memoization  | 870 ms                                                 | 461 ms: 1.89x faster                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 611 ms: 1.66x faster                                             |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 85.7 ms: 1.79x faster                                            |
| float          | 117 ms                                                 | 77.5 ms: 1.51x faster                                            |
| pidigits       | 191 ms                                                 | 193 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                  | 1.39x faster                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 132 ms: 1.43x faster                                             |
| regex_v8       | 27.8 ms                                                | 25.7 ms: 1.08x faster                                            |
| regex_dna      | 227 ms                                                 | 226 ms: 1.00x faster                                             |
| regex_effbot   | 3.63 ms                                                | 3.74 ms: 1.03x slower                                            |
| Geometric mean | (ref)                                                  | 1.11x faster                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 305 us: 1.59x faster                                             |
| unpickle_pure_python | 331 us                                                 | 214 us: 1.55x faster                                             |
| tomli_loads          | 3.14 sec                                               | 2.16 sec: 1.45x faster                                           |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                            |
| xml_etree_process    | 79.1 ms                                                | 60.6 ms: 1.31x faster                                            |
| xml_etree_generate   | 99.4 ms                                                | 87.5 ms: 1.14x faster                                            |
| json_loads           | 31.2 us                                                | 27.8 us: 1.12x faster                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                             |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                             |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                            |
| pickle               | 10.7 us                                                | 11.8 us: 1.11x slower                                            |
| unpickle             | 14.4 us                                                | 16.1 us: 1.12x slower                                            |
| pickle_dict          | 29.6 us                                                | 34.7 us: 1.17x slower                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                     |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                            |
| python_startup_no_site | 5.93 ms                                                | 7.09 ms: 1.20x slower                                            |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.52x faster                                            |
| django_template | 48.2 ms                                                | 34.8 ms: 1.38x faster                                            |
| genshi_text     | 31.8 ms                                                | 23.2 ms: 1.37x faster                                            |
| genshi_xml      | 66.0 ms                                                | 51.5 ms: 1.28x faster                                            |
| Geometric mean  | (ref)                                                  | 1.39x faster                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 163 us: 3.33x faster                                             |
| generators               | 80.1 ms                                                | 29.2 ms: 2.75x faster                                            |
| deltablue                | 7.91 ms                                                | 3.16 ms: 2.51x faster                                            |
| async_tree_none          | 728 ms                                                 | 353 ms: 2.06x faster                                             |
| raytrace                 | 507 ms                                                 | 259 ms: 1.96x faster                                             |
| chaos                    | 115 ms                                                 | 59.1 ms: 1.95x faster                                            |
| async_tree_io            | 1.77 sec                                               | 919 ms: 1.92x faster                                             |
| logging_silent           | 190 ns                                                 | 99.7 ns: 1.90x faster                                            |
| async_tree_memoization   | 870 ms                                                 | 461 ms: 1.89x faster                                             |
| scimark_sor              | 220 ms                                                 | 119 ms: 1.84x faster                                             |
| nbody                    | 154 ms                                                 | 85.7 ms: 1.79x faster                                            |
| asyncio_tcp              | 922 ms                                                 | 515 ms: 1.79x faster                                             |
| richards_super           | 94.7 ms                                                | 53.6 ms: 1.77x faster                                            |
| comprehensions           | 28.8 us                                                | 16.3 us: 1.76x faster                                            |
| hexiom                   | 10.4 ms                                                | 5.95 ms: 1.75x faster                                            |
| scimark_monte_carlo      | 118 ms                                                 | 67.9 ms: 1.74x faster                                            |
| pylint                   | 551 ms                                                 | 318 ms: 1.73x faster                                             |
| go                       | 240 ms                                                 | 140 ms: 1.71x faster                                             |
| crypto_pyaes             | 128 ms                                                 | 74.7 ms: 1.71x faster                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.28 ms: 1.70x faster                                            |
| richards                 | 79.3 ms                                                | 46.8 ms: 1.70x faster                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 611 ms: 1.66x faster                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.58 ms: 1.63x faster                                            |
| deepcopy_memo            | 58.5 us                                                | 36.8 us: 1.59x faster                                            |
| pickle_pure_python       | 484 us                                                 | 305 us: 1.59x faster                                             |
| pyflate                  | 716 ms                                                 | 453 ms: 1.58x faster                                             |
| scimark_lu               | 176 ms                                                 | 113 ms: 1.56x faster                                             |
| unpickle_pure_python     | 331 us                                                 | 214 us: 1.55x faster                                             |
| spectral_norm            | 170 ms                                                 | 111 ms: 1.53x faster                                             |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.52x faster                                            |
| float                    | 117 ms                                                 | 77.5 ms: 1.51x faster                                            |
| coroutines               | 35.1 ms                                                | 23.4 ms: 1.50x faster                                            |
| logging_simple           | 8.30 us                                                | 5.70 us: 1.46x faster                                            |
| tomli_loads              | 3.14 sec                                               | 2.16 sec: 1.45x faster                                           |
| tornado_http             | 136 ms                                                 | 94.2 ms: 1.45x faster                                            |
| logging_format           | 9.09 us                                                | 6.33 us: 1.44x faster                                            |
| regex_compile            | 188 ms                                                 | 132 ms: 1.43x faster                                             |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.39x faster                                           |
| chameleon                | 9.68 ms                                                | 6.96 ms: 1.39x faster                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                           |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                            |
| django_template          | 48.2 ms                                                | 34.8 ms: 1.38x faster                                            |
| pprint_safe_repr         | 1.02 sec                                               | 738 ms: 1.38x faster                                             |
| genshi_text              | 31.8 ms                                                | 23.2 ms: 1.37x faster                                            |
| deepcopy                 | 479 us                                                 | 350 us: 1.37x faster                                             |
| fannkuch                 | 532 ms                                                 | 389 ms: 1.37x faster                                             |
| nqueens                  | 106 ms                                                 | 78.8 ms: 1.34x faster                                            |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                            |
| html5lib                 | 88.9 ms                                                | 66.8 ms: 1.33x faster                                            |
| pycparser                | 1.58 sec                                               | 1.19 sec: 1.32x faster                                           |
| deepcopy_reduce          | 4.17 us                                                | 3.19 us: 1.31x faster                                            |
| sqlglot_normalize        | 143 ms                                                 | 109 ms: 1.31x faster                                             |
| thrift                   | 1.07 ms                                                | 821 us: 1.31x faster                                             |
| 2to3                     | 348 ms                                                 | 267 ms: 1.31x faster                                             |
| xml_etree_process        | 79.1 ms                                                | 60.6 ms: 1.31x faster                                            |
| scimark_fft              | 466 ms                                                 | 362 ms: 1.29x faster                                             |
| genshi_xml               | 66.0 ms                                                | 51.5 ms: 1.28x faster                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.06 ms: 1.28x faster                                            |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                            |
| sympy_sum                | 196 ms                                                 | 155 ms: 1.27x faster                                             |
| sqlglot_optimize         | 69.2 ms                                                | 54.6 ms: 1.27x faster                                            |
| dulwich_log              | 84.3 ms                                                | 66.7 ms: 1.26x faster                                            |
| sympy_str                | 346 ms                                                 | 277 ms: 1.25x faster                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                            |
| djangocms                | 38.4 us                                                | 31.4 us: 1.22x faster                                            |
| mypy2                    | 894 ms                                                 | 733 ms: 1.22x faster                                             |
| sympy_expand             | 566 ms                                                 | 469 ms: 1.21x faster                                             |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                            |
| bench_thread_pool        | 986 us                                                 | 820 us: 1.20x faster                                             |
| dask                     | 441 ms                                                 | 369 ms: 1.19x faster                                             |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                           |
| pathlib                  | 20.5 ms                                                | 17.6 ms: 1.16x faster                                            |
| xml_etree_generate       | 99.4 ms                                                | 87.5 ms: 1.14x faster                                            |
| json_loads               | 31.2 us                                                | 27.8 us: 1.12x faster                                            |
| json                     | 5.69 ms                                                | 5.13 ms: 1.11x faster                                            |
| meteor_contest           | 120 ms                                                 | 108 ms: 1.10x faster                                             |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                             |
| regex_v8                 | 27.8 ms                                                | 25.7 ms: 1.08x faster                                            |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                             |
| mdp                      | 2.85 sec                                               | 2.71 sec: 1.05x faster                                           |
| sqlite_synth             | 3.02 us                                                | 2.90 us: 1.04x faster                                            |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                            |
| regex_dna                | 227 ms                                                 | 226 ms: 1.00x faster                                             |
| async_generators         | 444 ms                                                 | 442 ms: 1.00x faster                                             |
| pickle_list              | 5.08 us                                                | 5.12 us: 1.01x slower                                            |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                             |
| pidigits                 | 191 ms                                                 | 193 ms: 1.01x slower                                             |
| regex_effbot             | 3.63 ms                                                | 3.74 ms: 1.03x slower                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.08x slower                                            |
| pickle                   | 10.7 us                                                | 11.8 us: 1.11x slower                                            |
| gc_traversal             | 3.62 ms                                                | 4.02 ms: 1.11x slower                                            |
| unpickle                 | 14.4 us                                                | 16.1 us: 1.12x slower                                            |
| coverage                 | 79.4 ms                                                | 92.8 ms: 1.17x slower                                            |
| pickle_dict              | 29.6 us                                                | 34.7 us: 1.17x slower                                            |
| telco                    | 7.27 ms                                                | 8.56 ms: 1.18x slower                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.09 ms: 1.20x slower                                            |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                     |

Benchmark hidden because not significant (1): unpickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-8cb71dd/bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: 1.10x
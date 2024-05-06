# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 277 ms: 1.26x faster                                                   |
| chameleon      | 9.68 ms                                                | 7.09 ms: 1.37x faster                                                  |
| docutils       | 3.30 sec                                               | 2.89 sec: 1.14x faster                                                 |
| html5lib       | 88.9 ms                                                | 66.5 ms: 1.34x faster                                                  |
| tornado_http   | 136 ms                                                 | 94.9 ms: 1.44x faster                                                  |
| Geometric mean | (ref)                                                  | 1.30x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 356 ms: 2.05x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 925 ms: 1.91x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 461 ms: 1.89x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 610 ms: 1.67x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 94.3 ms: 1.63x faster                                                  |
| float          | 117 ms                                                 | 76.6 ms: 1.53x faster                                                  |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.36x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 140 ms: 1.35x faster                                                   |
| regex_v8       | 27.8 ms                                                | 25.2 ms: 1.10x faster                                                  |
| regex_dna      | 227 ms                                                 | 228 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 304 us: 1.60x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.07 sec: 1.52x faster                                                 |
| unpickle_pure_python | 331 us                                                 | 233 us: 1.42x faster                                                   |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                  |
| json_loads           | 31.2 us                                                | 27.7 us: 1.13x faster                                                  |
| xml_etree_parse      | 168 ms                                                 | 152 ms: 1.11x faster                                                   |
| xml_etree_iterparse  | 115 ms                                                 | 104 ms: 1.11x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                                  |
| unpickle_list        | 5.20 us                                                | 5.32 us: 1.02x slower                                                  |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                  |
| unpickle             | 14.4 us                                                | 16.2 us: 1.13x slower                                                  |
| pickle_dict          | 29.6 us                                                | 35.1 us: 1.18x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.33x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.57 ms: 1.28x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.52x faster                                                  |
| django_template | 48.2 ms                                                | 36.7 ms: 1.31x faster                                                  |
| genshi_text     | 31.8 ms                                                | 24.3 ms: 1.31x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 53.8 ms: 1.23x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.34x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.84x faster                                                   |
| generators               | 80.1 ms                                                | 30.0 ms: 2.67x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.61 ms: 2.19x faster                                                  |
| async_tree_none          | 728 ms                                                 | 356 ms: 2.05x faster                                                   |
| richards_super           | 94.7 ms                                                | 48.8 ms: 1.94x faster                                                  |
| async_tree_io            | 1.77 sec                                               | 925 ms: 1.91x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 461 ms: 1.89x faster                                                   |
| raytrace                 | 507 ms                                                 | 270 ms: 1.88x faster                                                   |
| richards                 | 79.3 ms                                                | 42.6 ms: 1.86x faster                                                  |
| chaos                    | 115 ms                                                 | 62.3 ms: 1.85x faster                                                  |
| logging_silent           | 190 ns                                                 | 104 ns: 1.82x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 509 ms: 1.81x faster                                                   |
| crypto_pyaes             | 128 ms                                                 | 74.4 ms: 1.72x faster                                                  |
| scimark_monte_carlo      | 118 ms                                                 | 69.1 ms: 1.71x faster                                                  |
| scimark_sor              | 220 ms                                                 | 131 ms: 1.68x faster                                                   |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 610 ms: 1.67x faster                                                   |
| pylint                   | 551 ms                                                 | 333 ms: 1.66x faster                                                   |
| sqlglot_parse            | 2.17 ms                                                | 1.31 ms: 1.65x faster                                                  |
| nbody                    | 154 ms                                                 | 94.3 ms: 1.63x faster                                                  |
| comprehensions           | 28.8 us                                                | 17.9 us: 1.60x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 304 us: 1.60x faster                                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.62 ms: 1.59x faster                                                  |
| go                       | 240 ms                                                 | 153 ms: 1.56x faster                                                   |
| coroutines               | 35.1 ms                                                | 22.7 ms: 1.54x faster                                                  |
| hexiom                   | 10.4 ms                                                | 6.80 ms: 1.53x faster                                                  |
| float                    | 117 ms                                                 | 76.6 ms: 1.53x faster                                                  |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.52x faster                                                  |
| deepcopy_memo            | 58.5 us                                                | 38.5 us: 1.52x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.07 sec: 1.52x faster                                                 |
| spectral_norm            | 170 ms                                                 | 112 ms: 1.51x faster                                                   |
| pyflate                  | 716 ms                                                 | 476 ms: 1.50x faster                                                   |
| tornado_http             | 136 ms                                                 | 94.9 ms: 1.44x faster                                                  |
| logging_simple           | 8.30 us                                                | 5.82 us: 1.43x faster                                                  |
| unpickle_pure_python     | 331 us                                                 | 233 us: 1.42x faster                                                   |
| logging_format           | 9.09 us                                                | 6.45 us: 1.41x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                 |
| scimark_fft              | 466 ms                                                 | 339 ms: 1.37x faster                                                   |
| fannkuch                 | 532 ms                                                 | 388 ms: 1.37x faster                                                   |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.37x faster                                                 |
| chameleon                | 9.68 ms                                                | 7.09 ms: 1.37x faster                                                  |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.78 ms: 1.35x faster                                                  |
| pprint_safe_repr         | 1.02 sec                                               | 753 ms: 1.35x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                  |
| regex_compile            | 188 ms                                                 | 140 ms: 1.35x faster                                                   |
| pycparser                | 1.58 sec                                               | 1.17 sec: 1.34x faster                                                 |
| html5lib                 | 88.9 ms                                                | 66.5 ms: 1.34x faster                                                  |
| deepcopy                 | 479 us                                                 | 359 us: 1.33x faster                                                   |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.33x faster                                                  |
| thrift                   | 1.07 ms                                                | 806 us: 1.33x faster                                                   |
| scimark_lu               | 176 ms                                                 | 133 ms: 1.33x faster                                                   |
| xml_etree_process        | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                  |
| django_template          | 48.2 ms                                                | 36.7 ms: 1.31x faster                                                  |
| genshi_text              | 31.8 ms                                                | 24.3 ms: 1.31x faster                                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.19 us: 1.31x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 112 ms: 1.28x faster                                                   |
| 2to3                     | 348 ms                                                 | 277 ms: 1.26x faster                                                   |
| dulwich_log              | 84.3 ms                                                | 68.7 ms: 1.23x faster                                                  |
| genshi_xml               | 66.0 ms                                                | 53.8 ms: 1.23x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 56.9 ms: 1.22x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.20 ms: 1.20x faster                                                  |
| djangocms                | 38.4 us                                                | 32.0 us: 1.20x faster                                                  |
| sympy_sum                | 196 ms                                                 | 166 ms: 1.19x faster                                                   |
| nqueens                  | 106 ms                                                 | 89.2 ms: 1.19x faster                                                  |
| dask                     | 441 ms                                                 | 372 ms: 1.18x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.29 ms: 1.18x faster                                                  |
| sympy_str                | 346 ms                                                 | 292 ms: 1.18x faster                                                   |
| sympy_integrate          | 25.8 ms                                                | 21.8 ms: 1.18x faster                                                  |
| bench_thread_pool        | 986 us                                                 | 852 us: 1.16x faster                                                   |
| pathlib                  | 20.5 ms                                                | 17.7 ms: 1.16x faster                                                  |
| sympy_expand             | 566 ms                                                 | 490 ms: 1.15x faster                                                   |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                  |
| mypy2                    | 894 ms                                                 | 782 ms: 1.14x faster                                                   |
| docutils                 | 3.30 sec                                               | 2.89 sec: 1.14x faster                                                 |
| json_loads               | 31.2 us                                                | 27.7 us: 1.13x faster                                                  |
| xml_etree_parse          | 168 ms                                                 | 152 ms: 1.11x faster                                                   |
| json                     | 5.69 ms                                                | 5.13 ms: 1.11x faster                                                  |
| xml_etree_iterparse      | 115 ms                                                 | 104 ms: 1.11x faster                                                   |
| regex_v8                 | 27.8 ms                                                | 25.2 ms: 1.10x faster                                                  |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                  |
| pickle_list              | 5.08 us                                                | 5.00 us: 1.02x faster                                                  |
| gc_traversal             | 3.62 ms                                                | 3.57 ms: 1.01x faster                                                  |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                   |
| regex_dna                | 227 ms                                                 | 228 ms: 1.01x slower                                                   |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.02x slower                                                   |
| unpickle_list            | 5.20 us                                                | 5.32 us: 1.02x slower                                                  |
| async_generators         | 444 ms                                                 | 458 ms: 1.03x slower                                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                  |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                  |
| unpickle                 | 14.4 us                                                | 16.2 us: 1.13x slower                                                  |
| telco                    | 7.27 ms                                                | 8.56 ms: 1.18x slower                                                  |
| pickle_dict              | 29.6 us                                                | 35.1 us: 1.18x slower                                                  |
| coverage                 | 79.4 ms                                                | 97.3 ms: 1.23x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 7.57 ms: 1.28x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                           |

Benchmark hidden because not significant (3): mdp, bench_mp_pool, regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.19x
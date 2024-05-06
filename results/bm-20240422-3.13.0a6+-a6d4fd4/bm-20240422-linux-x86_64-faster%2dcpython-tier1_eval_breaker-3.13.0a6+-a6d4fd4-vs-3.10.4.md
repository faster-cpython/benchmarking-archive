# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 273 ms: 1.28x faster                                                           |
| chameleon      | 9.68 ms                                                | 7.17 ms: 1.35x faster                                                          |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                         |
| html5lib       | 88.9 ms                                                | 66.5 ms: 1.34x faster                                                          |
| tornado_http   | 136 ms                                                 | 94.7 ms: 1.44x faster                                                          |
| Geometric mean | (ref)                                                  | 1.31x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 356 ms: 2.05x faster                                                           |
| async_tree_io           | 1.77 sec                                               | 929 ms: 1.90x faster                                                           |
| async_tree_memoization  | 870 ms                                                 | 470 ms: 1.85x faster                                                           |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 609 ms: 1.67x faster                                                           |
| Geometric mean          | (ref)                                                  | 1.86x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 92.6 ms: 1.66x faster                                                          |
| float          | 117 ms                                                 | 78.9 ms: 1.48x faster                                                          |
| pidigits       | 191 ms                                                 | 193 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                  | 1.35x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 137 ms: 1.37x faster                                                           |
| regex_v8       | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                          |
| regex_dna      | 227 ms                                                 | 233 ms: 1.03x slower                                                           |
| regex_effbot   | 3.63 ms                                                | 3.83 ms: 1.06x slower                                                          |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 308 us: 1.57x faster                                                           |
| unpickle_pure_python | 331 us                                                 | 224 us: 1.48x faster                                                           |
| tomli_loads          | 3.14 sec                                               | 2.20 sec: 1.43x faster                                                         |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                          |
| xml_etree_process    | 79.1 ms                                                | 61.2 ms: 1.29x faster                                                          |
| json_loads           | 31.2 us                                                | 27.5 us: 1.13x faster                                                          |
| xml_etree_generate   | 99.4 ms                                                | 88.6 ms: 1.12x faster                                                          |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                           |
| xml_etree_parse      | 168 ms                                                 | 158 ms: 1.06x faster                                                           |
| pickle_list          | 5.08 us                                                | 5.21 us: 1.03x slower                                                          |
| unpickle_list        | 5.20 us                                                | 5.35 us: 1.03x slower                                                          |
| unpickle             | 14.4 us                                                | 15.1 us: 1.05x slower                                                          |
| pickle               | 10.7 us                                                | 11.9 us: 1.11x slower                                                          |
| pickle_dict          | 29.6 us                                                | 35.4 us: 1.20x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                          |
| python_startup_no_site | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.3 ms: 1.45x faster                                                          |
| django_template | 48.2 ms                                                | 35.6 ms: 1.35x faster                                                          |
| genshi_text     | 31.8 ms                                                | 24.0 ms: 1.32x faster                                                          |
| genshi_xml      | 66.0 ms                                                | 52.2 ms: 1.27x faster                                                          |
| Geometric mean  | (ref)                                                  | 1.35x faster                                                                   |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 116 us: 4.68x faster                                                           |
| generators               | 80.1 ms                                                | 30.3 ms: 2.64x faster                                                          |
| deltablue                | 7.91 ms                                                | 3.34 ms: 2.37x faster                                                          |
| async_tree_none          | 728 ms                                                 | 356 ms: 2.05x faster                                                           |
| raytrace                 | 507 ms                                                 | 263 ms: 1.93x faster                                                           |
| async_tree_io            | 1.77 sec                                               | 929 ms: 1.90x faster                                                           |
| chaos                    | 115 ms                                                 | 61.0 ms: 1.89x faster                                                          |
| logging_silent           | 190 ns                                                 | 102 ns: 1.87x faster                                                           |
| async_tree_memoization   | 870 ms                                                 | 470 ms: 1.85x faster                                                           |
| asyncio_tcp              | 922 ms                                                 | 511 ms: 1.80x faster                                                           |
| scimark_sor              | 220 ms                                                 | 123 ms: 1.79x faster                                                           |
| richards_super           | 94.7 ms                                                | 53.3 ms: 1.78x faster                                                          |
| pylint                   | 551 ms                                                 | 320 ms: 1.72x faster                                                           |
| scimark_monte_carlo      | 118 ms                                                 | 68.8 ms: 1.72x faster                                                          |
| richards                 | 79.3 ms                                                | 46.9 ms: 1.69x faster                                                          |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                          |
| go                       | 240 ms                                                 | 143 ms: 1.68x faster                                                           |
| crypto_pyaes             | 128 ms                                                 | 76.3 ms: 1.67x faster                                                          |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 609 ms: 1.67x faster                                                           |
| comprehensions           | 28.8 us                                                | 17.3 us: 1.66x faster                                                          |
| nbody                    | 154 ms                                                 | 92.6 ms: 1.66x faster                                                          |
| hexiom                   | 10.4 ms                                                | 6.45 ms: 1.61x faster                                                          |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.60x faster                                                          |
| pickle_pure_python       | 484 us                                                 | 308 us: 1.57x faster                                                           |
| coroutines               | 35.1 ms                                                | 22.5 ms: 1.56x faster                                                          |
| scimark_lu               | 176 ms                                                 | 117 ms: 1.51x faster                                                           |
| float                    | 117 ms                                                 | 78.9 ms: 1.48x faster                                                          |
| deepcopy_memo            | 58.5 us                                                | 39.4 us: 1.48x faster                                                          |
| unpickle_pure_python     | 331 us                                                 | 224 us: 1.48x faster                                                           |
| spectral_norm            | 170 ms                                                 | 117 ms: 1.45x faster                                                           |
| mako                     | 16.3 ms                                                | 11.3 ms: 1.45x faster                                                          |
| pyflate                  | 716 ms                                                 | 495 ms: 1.45x faster                                                           |
| tornado_http             | 136 ms                                                 | 94.7 ms: 1.44x faster                                                          |
| tomli_loads              | 3.14 sec                                               | 2.20 sec: 1.43x faster                                                         |
| logging_simple           | 8.30 us                                                | 5.84 us: 1.42x faster                                                          |
| logging_format           | 9.09 us                                                | 6.48 us: 1.40x faster                                                          |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                         |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                          |
| regex_compile            | 188 ms                                                 | 137 ms: 1.37x faster                                                           |
| django_template          | 48.2 ms                                                | 35.6 ms: 1.35x faster                                                          |
| chameleon                | 9.68 ms                                                | 7.17 ms: 1.35x faster                                                          |
| pprint_pformat           | 2.10 sec                                               | 1.56 sec: 1.35x faster                                                         |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                          |
| pprint_safe_repr         | 1.02 sec                                               | 760 ms: 1.34x faster                                                           |
| html5lib                 | 88.9 ms                                                | 66.5 ms: 1.34x faster                                                          |
| thrift                   | 1.07 ms                                                | 804 us: 1.33x faster                                                           |
| deepcopy                 | 479 us                                                 | 360 us: 1.33x faster                                                           |
| genshi_text              | 31.8 ms                                                | 24.0 ms: 1.32x faster                                                          |
| deepcopy_reduce          | 4.17 us                                                | 3.18 us: 1.31x faster                                                          |
| fannkuch                 | 532 ms                                                 | 406 ms: 1.31x faster                                                           |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                           |
| pycparser                | 1.58 sec                                               | 1.22 sec: 1.30x faster                                                         |
| xml_etree_process        | 79.1 ms                                                | 61.2 ms: 1.29x faster                                                          |
| nqueens                  | 106 ms                                                 | 81.9 ms: 1.29x faster                                                          |
| 2to3                     | 348 ms                                                 | 273 ms: 1.28x faster                                                           |
| genshi_xml               | 66.0 ms                                                | 52.2 ms: 1.27x faster                                                          |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.27x faster                                                          |
| dulwich_log              | 84.3 ms                                                | 66.8 ms: 1.26x faster                                                          |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                                           |
| sqlglot_optimize         | 69.2 ms                                                | 55.6 ms: 1.24x faster                                                          |
| scimark_fft              | 466 ms                                                 | 379 ms: 1.23x faster                                                           |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                          |
| sympy_str                | 346 ms                                                 | 283 ms: 1.22x faster                                                           |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.33 ms: 1.21x faster                                                          |
| djangocms                | 38.4 us                                                | 31.8 us: 1.21x faster                                                          |
| mypy2                    | 894 ms                                                 | 741 ms: 1.21x faster                                                           |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                          |
| dask                     | 441 ms                                                 | 371 ms: 1.19x faster                                                           |
| sympy_expand             | 566 ms                                                 | 477 ms: 1.18x faster                                                           |
| bench_thread_pool        | 986 us                                                 | 836 us: 1.18x faster                                                           |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                         |
| pathlib                  | 20.5 ms                                                | 17.8 ms: 1.15x faster                                                          |
| json_loads               | 31.2 us                                                | 27.5 us: 1.13x faster                                                          |
| xml_etree_generate       | 99.4 ms                                                | 88.6 ms: 1.12x faster                                                          |
| json                     | 5.69 ms                                                | 5.20 ms: 1.09x faster                                                          |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                           |
| regex_v8                 | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                          |
| meteor_contest           | 120 ms                                                 | 112 ms: 1.07x faster                                                           |
| xml_etree_parse          | 168 ms                                                 | 158 ms: 1.06x faster                                                           |
| mdp                      | 2.85 sec                                               | 2.79 sec: 1.02x faster                                                         |
| sqlite_synth             | 3.02 us                                                | 2.97 us: 1.02x faster                                                          |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                          |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                           |
| pidigits                 | 191 ms                                                 | 193 ms: 1.01x slower                                                           |
| async_generators         | 444 ms                                                 | 451 ms: 1.02x slower                                                           |
| pickle_list              | 5.08 us                                                | 5.21 us: 1.03x slower                                                          |
| regex_dna                | 227 ms                                                 | 233 ms: 1.03x slower                                                           |
| unpickle_list            | 5.20 us                                                | 5.35 us: 1.03x slower                                                          |
| unpickle                 | 14.4 us                                                | 15.1 us: 1.05x slower                                                          |
| regex_effbot             | 3.63 ms                                                | 3.83 ms: 1.06x slower                                                          |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.09x slower                                                          |
| gc_traversal             | 3.62 ms                                                | 3.98 ms: 1.10x slower                                                          |
| pickle                   | 10.7 us                                                | 11.9 us: 1.11x slower                                                          |
| telco                    | 7.27 ms                                                | 8.65 ms: 1.19x slower                                                          |
| pickle_dict              | 29.6 us                                                | 35.4 us: 1.20x slower                                                          |
| python_startup_no_site   | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                          |
| coverage                 | 79.4 ms                                                | 98.8 ms: 1.24x slower                                                          |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                                   |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.24x

# Memory
- memory change: 1.10x
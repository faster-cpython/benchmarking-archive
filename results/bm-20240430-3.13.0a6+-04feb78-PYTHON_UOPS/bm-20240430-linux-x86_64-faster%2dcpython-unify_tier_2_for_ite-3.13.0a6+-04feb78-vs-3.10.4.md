# Results vs. 3.10.4

- fork: faster-cpython
- ref: unify_tier_2_for_ite
- machine: linux-x86_64
- commit hash: 04feb78
- commit date: 2024-04-30
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 321 ms: 1.08x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.94 ms: 1.22x faster                                                            |
| docutils       | 3.30 sec                                               | 3.19 sec: 1.03x faster                                                           |
| html5lib       | 88.9 ms                                                | 76.3 ms: 1.16x faster                                                            |
| tornado_http   | 136 ms                                                 | 104 ms: 1.32x faster                                                             |
| Geometric mean | (ref)                                                  | 1.16x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 373 ms: 1.95x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 964 ms: 1.83x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 499 ms: 1.74x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 633 ms: 1.61x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.78x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 91.9 ms: 1.27x faster                                                            |
| nbody          | 154 ms                                                 | 125 ms: 1.23x faster                                                             |
| pidigits       | 191 ms                                                 | 213 ms: 1.11x slower                                                             |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                            |
| regex_compile  | 188 ms                                                 | 181 ms: 1.04x faster                                                             |
| regex_dna      | 227 ms                                                 | 221 ms: 1.02x faster                                                             |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 321 us: 1.51x faster                                                             |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| tomli_loads          | 3.14 sec                                               | 2.54 sec: 1.24x faster                                                           |
| xml_etree_process    | 79.1 ms                                                | 67.5 ms: 1.17x faster                                                            |
| unpickle_pure_python | 331 us                                                 | 286 us: 1.16x faster                                                             |
| json_loads           | 31.2 us                                                | 27.7 us: 1.13x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 153 ms: 1.10x faster                                                             |
| xml_etree_iterparse  | 115 ms                                                 | 111 ms: 1.04x faster                                                             |
| xml_etree_generate   | 99.4 ms                                                | 96.3 ms: 1.03x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                            |
| unpickle_list        | 5.20 us                                                | 5.28 us: 1.02x slower                                                            |
| pickle               | 10.7 us                                                | 12.1 us: 1.14x slower                                                            |
| unpickle             | 14.4 us                                                | 16.5 us: 1.14x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.2 us: 1.19x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.17 ms: 1.21x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 48.2 ms                                                | 40.7 ms: 1.18x faster                                                            |
| mako            | 16.3 ms                                                | 14.0 ms: 1.17x faster                                                            |
| genshi_text     | 31.8 ms                                                | 31.2 ms: 1.02x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 70.8 ms: 1.07x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 190 us: 2.87x faster                                                             |
| generators               | 80.1 ms                                                | 31.2 ms: 2.57x faster                                                            |
| async_tree_none          | 728 ms                                                 | 373 ms: 1.95x faster                                                             |
| deltablue                | 7.91 ms                                                | 4.29 ms: 1.85x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 964 ms: 1.83x faster                                                             |
| logging_silent           | 190 ns                                                 | 108 ns: 1.76x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 528 ms: 1.75x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 499 ms: 1.74x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 633 ms: 1.61x faster                                                             |
| raytrace                 | 507 ms                                                 | 334 ms: 1.52x faster                                                             |
| pylint                   | 551 ms                                                 | 365 ms: 1.51x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 321 us: 1.51x faster                                                             |
| chaos                    | 115 ms                                                 | 78.6 ms: 1.47x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.49 ms: 1.45x faster                                                            |
| coroutines               | 35.1 ms                                                | 24.3 ms: 1.45x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 89.6 ms: 1.43x faster                                                            |
| richards_super           | 94.7 ms                                                | 66.5 ms: 1.42x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.82 ms: 1.41x faster                                                            |
| scimark_sor              | 220 ms                                                 | 159 ms: 1.38x faster                                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.38x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                            |
| richards                 | 79.3 ms                                                | 59.7 ms: 1.33x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 89.5 ms: 1.32x faster                                                            |
| tornado_http             | 136 ms                                                 | 104 ms: 1.32x faster                                                             |
| logging_simple           | 8.30 us                                                | 6.44 us: 1.29x faster                                                            |
| thrift                   | 1.07 ms                                                | 831 us: 1.29x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 45.5 us: 1.28x faster                                                            |
| logging_format           | 9.09 us                                                | 7.09 us: 1.28x faster                                                            |
| float                    | 117 ms                                                 | 91.9 ms: 1.27x faster                                                            |
| spectral_norm            | 170 ms                                                 | 137 ms: 1.24x faster                                                             |
| tomli_loads              | 3.14 sec                                               | 2.54 sec: 1.24x faster                                                           |
| deepcopy_reduce          | 4.17 us                                                | 3.38 us: 1.24x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.28 sec: 1.23x faster                                                           |
| nbody                    | 154 ms                                                 | 125 ms: 1.23x faster                                                             |
| deepcopy                 | 479 us                                                 | 389 us: 1.23x faster                                                             |
| chameleon                | 9.68 ms                                                | 7.94 ms: 1.22x faster                                                            |
| pyflate                  | 716 ms                                                 | 595 ms: 1.20x faster                                                             |
| django_template          | 48.2 ms                                                | 40.7 ms: 1.18x faster                                                            |
| go                       | 240 ms                                                 | 203 ms: 1.18x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 67.5 ms: 1.17x faster                                                            |
| mako                     | 16.3 ms                                                | 14.0 ms: 1.17x faster                                                            |
| comprehensions           | 28.8 us                                                | 24.6 us: 1.17x faster                                                            |
| html5lib                 | 88.9 ms                                                | 76.3 ms: 1.16x faster                                                            |
| djangocms                | 38.4 us                                                | 33.0 us: 1.16x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 286 us: 1.16x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.26 ms: 1.14x faster                                                            |
| dask                     | 441 ms                                                 | 386 ms: 1.14x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.35 ms: 1.13x faster                                                            |
| json_loads               | 31.2 us                                                | 27.7 us: 1.13x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.2 ms: 1.12x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 75.1 ms: 1.12x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                            |
| sqlglot_normalize        | 143 ms                                                 | 129 ms: 1.11x faster                                                             |
| fannkuch                 | 532 ms                                                 | 481 ms: 1.10x faster                                                             |
| json                     | 5.69 ms                                                | 5.16 ms: 1.10x faster                                                            |
| sympy_sum                | 196 ms                                                 | 179 ms: 1.10x faster                                                             |
| xml_etree_parse          | 168 ms                                                 | 153 ms: 1.10x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.97 ms: 1.08x faster                                                            |
| 2to3                     | 348 ms                                                 | 321 ms: 1.08x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 912 us: 1.08x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 24.2 ms: 1.07x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 65.0 ms: 1.06x faster                                                            |
| hexiom                   | 10.4 ms                                                | 9.77 ms: 1.06x faster                                                            |
| mypy2                    | 894 ms                                                 | 842 ms: 1.06x faster                                                             |
| pprint_safe_repr         | 1.02 sec                                               | 965 ms: 1.06x faster                                                             |
| pprint_pformat           | 2.10 sec                                               | 2.00 sec: 1.05x faster                                                           |
| scimark_lu               | 176 ms                                                 | 168 ms: 1.05x faster                                                             |
| scimark_fft              | 466 ms                                                 | 445 ms: 1.05x faster                                                             |
| sympy_str                | 346 ms                                                 | 332 ms: 1.04x faster                                                             |
| regex_compile            | 188 ms                                                 | 181 ms: 1.04x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 111 ms: 1.04x faster                                                             |
| docutils                 | 3.30 sec                                               | 3.19 sec: 1.03x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 96.3 ms: 1.03x faster                                                            |
| regex_dna                | 227 ms                                                 | 221 ms: 1.02x faster                                                             |
| genshi_text              | 31.8 ms                                                | 31.2 ms: 1.02x faster                                                            |
| pickle_list              | 5.08 us                                                | 5.02 us: 1.01x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.82 sec: 1.01x faster                                                           |
| sympy_expand             | 566 ms                                                 | 561 ms: 1.01x faster                                                             |
| unpickle_list            | 5.20 us                                                | 5.28 us: 1.02x slower                                                            |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.02x slower                                                             |
| meteor_contest           | 120 ms                                                 | 122 ms: 1.02x slower                                                             |
| nqueens                  | 106 ms                                                 | 109 ms: 1.03x slower                                                             |
| genshi_xml               | 66.0 ms                                                | 70.8 ms: 1.07x slower                                                            |
| async_generators         | 444 ms                                                 | 476 ms: 1.07x slower                                                             |
| create_gc_cycles         | 1.62 ms                                                | 1.78 ms: 1.10x slower                                                            |
| pidigits                 | 191 ms                                                 | 213 ms: 1.11x slower                                                             |
| gc_traversal             | 3.62 ms                                                | 4.06 ms: 1.12x slower                                                            |
| pickle                   | 10.7 us                                                | 12.1 us: 1.14x slower                                                            |
| unpickle                 | 14.4 us                                                | 16.5 us: 1.14x slower                                                            |
| coverage                 | 79.4 ms                                                | 93.6 ms: 1.18x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.2 us: 1.19x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.17 ms: 1.21x slower                                                            |
| telco                    | 7.27 ms                                                | 9.32 ms: 1.28x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.18x faster                                                                     |

Benchmark hidden because not significant (3): bench_mp_pool, sqlite_synth, regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240430-3.13.0a6+-04feb78-PYTHON_UOPS/bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.11x
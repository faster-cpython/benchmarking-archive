# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_for_iter_gen
- machine: linux-x86_64
- commit hash: 5fbcbf4
- commit date: 2024-04-24
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 302 ms: 1.16x faster                                                            |
| chameleon      | 9.68 ms                                                | 7.46 ms: 1.30x faster                                                           |
| docutils       | 3.30 sec                                               | 3.07 sec: 1.08x faster                                                          |
| html5lib       | 88.9 ms                                                | 70.1 ms: 1.27x faster                                                           |
| tornado_http   | 136 ms                                                 | 101 ms: 1.35x faster                                                            |
| Geometric mean | (ref)                                                  | 1.22x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 373 ms: 1.95x faster                                                            |
| async_tree_io           | 1.77 sec                                               | 972 ms: 1.82x faster                                                            |
| async_tree_memoization  | 870 ms                                                 | 500 ms: 1.74x faster                                                            |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 636 ms: 1.60x faster                                                            |
| Geometric mean          | (ref)                                                  | 1.77x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 88.4 ms: 1.32x faster                                                           |
| nbody          | 154 ms                                                 | 122 ms: 1.26x faster                                                            |
| pidigits       | 191 ms                                                 | 195 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                  | 1.18x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                           |
| regex_compile  | 188 ms                                                 | 178 ms: 1.06x faster                                                            |
| regex_dna      | 227 ms                                                 | 227 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                    |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 314 us: 1.54x faster                                                            |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                           |
| tomli_loads          | 3.14 sec                                               | 2.49 sec: 1.26x faster                                                          |
| xml_etree_process    | 79.1 ms                                                | 64.4 ms: 1.23x faster                                                           |
| unpickle_pure_python | 331 us                                                 | 281 us: 1.18x faster                                                            |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                           |
| xml_etree_parse      | 168 ms                                                 | 153 ms: 1.10x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 93.3 ms: 1.07x faster                                                           |
| xml_etree_iterparse  | 115 ms                                                 | 111 ms: 1.04x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.03 us: 1.01x faster                                                           |
| pickle               | 10.7 us                                                | 11.8 us: 1.11x slower                                                           |
| unpickle             | 14.4 us                                                | 16.7 us: 1.16x slower                                                           |
| pickle_dict          | 29.6 us                                                | 35.4 us: 1.20x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                                    |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                           |
| python_startup_no_site | 5.93 ms                                                | 7.13 ms: 1.20x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 13.1 ms: 1.24x faster                                                           |
| django_template | 48.2 ms                                                | 39.5 ms: 1.22x faster                                                           |
| genshi_text     | 31.8 ms                                                | 27.3 ms: 1.17x faster                                                           |
| genshi_xml      | 66.0 ms                                                | 62.1 ms: 1.06x faster                                                           |
| Geometric mean  | (ref)                                                  | 1.17x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 123 us: 4.42x faster                                                            |
| generators               | 80.1 ms                                                | 30.8 ms: 2.60x faster                                                           |
| async_tree_none          | 728 ms                                                 | 373 ms: 1.95x faster                                                            |
| deltablue                | 7.91 ms                                                | 4.14 ms: 1.91x faster                                                           |
| async_tree_io            | 1.77 sec                                               | 972 ms: 1.82x faster                                                            |
| logging_silent           | 190 ns                                                 | 105 ns: 1.81x faster                                                            |
| asyncio_tcp              | 922 ms                                                 | 515 ms: 1.79x faster                                                            |
| async_tree_memoization   | 870 ms                                                 | 500 ms: 1.74x faster                                                            |
| pylint                   | 551 ms                                                 | 343 ms: 1.61x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 636 ms: 1.60x faster                                                            |
| raytrace                 | 507 ms                                                 | 319 ms: 1.59x faster                                                            |
| coroutines               | 35.1 ms                                                | 22.6 ms: 1.55x faster                                                           |
| pickle_pure_python       | 484 us                                                 | 314 us: 1.54x faster                                                            |
| richards_super           | 94.7 ms                                                | 62.0 ms: 1.53x faster                                                           |
| scimark_sor              | 220 ms                                                 | 147 ms: 1.49x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.47 ms: 1.47x faster                                                           |
| chaos                    | 115 ms                                                 | 78.9 ms: 1.46x faster                                                           |
| richards                 | 79.3 ms                                                | 55.3 ms: 1.43x faster                                                           |
| sqlglot_transpile        | 2.57 ms                                                | 1.80 ms: 1.43x faster                                                           |
| crypto_pyaes             | 128 ms                                                 | 89.8 ms: 1.42x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                           |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.38x faster                                                          |
| deepcopy_memo            | 58.5 us                                                | 43.2 us: 1.35x faster                                                           |
| scimark_monte_carlo      | 118 ms                                                 | 87.4 ms: 1.35x faster                                                           |
| tornado_http             | 136 ms                                                 | 101 ms: 1.35x faster                                                            |
| float                    | 117 ms                                                 | 88.4 ms: 1.32x faster                                                           |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                           |
| logging_simple           | 8.30 us                                                | 6.36 us: 1.30x faster                                                           |
| go                       | 240 ms                                                 | 184 ms: 1.30x faster                                                            |
| chameleon                | 9.68 ms                                                | 7.46 ms: 1.30x faster                                                           |
| thrift                   | 1.07 ms                                                | 834 us: 1.28x faster                                                            |
| deepcopy                 | 479 us                                                 | 376 us: 1.27x faster                                                            |
| comprehensions           | 28.8 us                                                | 22.6 us: 1.27x faster                                                           |
| logging_format           | 9.09 us                                                | 7.15 us: 1.27x faster                                                           |
| html5lib                 | 88.9 ms                                                | 70.1 ms: 1.27x faster                                                           |
| tomli_loads              | 3.14 sec                                               | 2.49 sec: 1.26x faster                                                          |
| nbody                    | 154 ms                                                 | 122 ms: 1.26x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.32 us: 1.26x faster                                                           |
| pyflate                  | 716 ms                                                 | 571 ms: 1.25x faster                                                            |
| mako                     | 16.3 ms                                                | 13.1 ms: 1.24x faster                                                           |
| pycparser                | 1.58 sec                                               | 1.27 sec: 1.24x faster                                                          |
| xml_etree_process        | 79.1 ms                                                | 64.4 ms: 1.23x faster                                                           |
| django_template          | 48.2 ms                                                | 39.5 ms: 1.22x faster                                                           |
| spectral_norm            | 170 ms                                                 | 140 ms: 1.22x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 281 us: 1.18x faster                                                            |
| djangocms                | 38.4 us                                                | 32.9 us: 1.17x faster                                                           |
| genshi_text              | 31.8 ms                                                | 27.3 ms: 1.17x faster                                                           |
| aiohttp                  | 1.44 ms                                                | 1.24 ms: 1.16x faster                                                           |
| sqlglot_normalize        | 143 ms                                                 | 123 ms: 1.16x faster                                                            |
| dask                     | 441 ms                                                 | 381 ms: 1.16x faster                                                            |
| 2to3                     | 348 ms                                                 | 302 ms: 1.16x faster                                                            |
| gunicorn                 | 1.53 ms                                                | 1.33 ms: 1.15x faster                                                           |
| dulwich_log              | 84.3 ms                                                | 73.6 ms: 1.15x faster                                                           |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                           |
| hexiom                   | 10.4 ms                                                | 9.27 ms: 1.12x faster                                                           |
| sympy_integrate          | 25.8 ms                                                | 23.0 ms: 1.12x faster                                                           |
| pathlib                  | 20.5 ms                                                | 18.3 ms: 1.12x faster                                                           |
| mypy2                    | 894 ms                                                 | 800 ms: 1.12x faster                                                            |
| sympy_sum                | 196 ms                                                 | 177 ms: 1.11x faster                                                            |
| bench_thread_pool        | 986 us                                                 | 893 us: 1.10x faster                                                            |
| fannkuch                 | 532 ms                                                 | 483 ms: 1.10x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 153 ms: 1.10x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                           |
| sqlglot_optimize         | 69.2 ms                                                | 63.3 ms: 1.09x faster                                                           |
| json                     | 5.69 ms                                                | 5.23 ms: 1.09x faster                                                           |
| scimark_lu               | 176 ms                                                 | 163 ms: 1.08x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 944 ms: 1.08x faster                                                            |
| docutils                 | 3.30 sec                                               | 3.07 sec: 1.08x faster                                                          |
| sympy_str                | 346 ms                                                 | 322 ms: 1.07x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.97 sec: 1.07x faster                                                          |
| xml_etree_generate       | 99.4 ms                                                | 93.3 ms: 1.07x faster                                                           |
| genshi_xml               | 66.0 ms                                                | 62.1 ms: 1.06x faster                                                           |
| sympy_expand             | 566 ms                                                 | 534 ms: 1.06x faster                                                            |
| regex_compile            | 188 ms                                                 | 178 ms: 1.06x faster                                                            |
| scimark_fft              | 466 ms                                                 | 443 ms: 1.05x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.21 ms: 1.04x faster                                                           |
| xml_etree_iterparse      | 115 ms                                                 | 111 ms: 1.04x faster                                                            |
| pickle_list              | 5.08 us                                                | 5.03 us: 1.01x faster                                                           |
| sqlite_synth             | 3.02 us                                                | 3.00 us: 1.01x faster                                                           |
| mdp                      | 2.85 sec                                               | 2.83 sec: 1.01x faster                                                          |
| regex_dna                | 227 ms                                                 | 227 ms: 1.00x slower                                                            |
| nqueens                  | 106 ms                                                 | 106 ms: 1.01x slower                                                            |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                            |
| pidigits                 | 191 ms                                                 | 195 ms: 1.02x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.72 ms: 1.03x slower                                                           |
| async_generators         | 444 ms                                                 | 473 ms: 1.07x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.09x slower                                                           |
| pickle                   | 10.7 us                                                | 11.8 us: 1.11x slower                                                           |
| unpickle                 | 14.4 us                                                | 16.7 us: 1.16x slower                                                           |
| pickle_dict              | 29.6 us                                                | 35.4 us: 1.20x slower                                                           |
| python_startup_no_site   | 5.93 ms                                                | 7.13 ms: 1.20x slower                                                           |
| coverage                 | 79.4 ms                                                | 99.0 ms: 1.25x slower                                                           |
| telco                    | 7.27 ms                                                | 9.15 ms: 1.26x slower                                                           |
| Geometric mean           | (ref)                                                  | 1.22x faster                                                                    |

Benchmark hidden because not significant (4): unpickle_list, bench_mp_pool, meteor_contest, regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240424-3.13.0a6+-5fbcbf4-PYTHON_UOPS/bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.11x
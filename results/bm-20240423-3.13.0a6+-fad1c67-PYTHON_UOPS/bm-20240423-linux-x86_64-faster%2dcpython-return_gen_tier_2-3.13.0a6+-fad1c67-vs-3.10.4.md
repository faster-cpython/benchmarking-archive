# Results vs. 3.10.4

- fork: faster-cpython
- ref: return_gen_tier_2
- machine: linux-x86_64
- commit hash: fad1c67
- commit date: 2024-04-23
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 301 ms: 1.16x faster                                                          |
| chameleon      | 9.68 ms                                                | 7.62 ms: 1.27x faster                                                         |
| docutils       | 3.30 sec                                               | 3.07 sec: 1.07x faster                                                        |
| html5lib       | 88.9 ms                                                | 72.4 ms: 1.23x faster                                                         |
| tornado_http   | 136 ms                                                 | 102 ms: 1.33x faster                                                          |
| Geometric mean | (ref)                                                  | 1.21x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 373 ms: 1.95x faster                                                          |
| async_tree_io           | 1.77 sec                                               | 966 ms: 1.83x faster                                                          |
| async_tree_memoization  | 870 ms                                                 | 499 ms: 1.74x faster                                                          |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 632 ms: 1.61x faster                                                          |
| Geometric mean          | (ref)                                                  | 1.78x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 89.3 ms: 1.31x faster                                                         |
| nbody          | 154 ms                                                 | 120 ms: 1.28x faster                                                          |
| pidigits       | 191 ms                                                 | 218 ms: 1.14x slower                                                          |
| Geometric mean | (ref)                                                  | 1.14x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                         |
| regex_compile  | 188 ms                                                 | 179 ms: 1.06x faster                                                          |
| regex_dna      | 227 ms                                                 | 228 ms: 1.01x slower                                                          |
| regex_effbot   | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 314 us: 1.54x faster                                                          |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                         |
| tomli_loads          | 3.14 sec                                               | 2.53 sec: 1.24x faster                                                        |
| xml_etree_process    | 79.1 ms                                                | 64.2 ms: 1.23x faster                                                         |
| unpickle_pure_python | 331 us                                                 | 283 us: 1.17x faster                                                          |
| json_loads           | 31.2 us                                                | 27.5 us: 1.13x faster                                                         |
| xml_etree_parse      | 168 ms                                                 | 154 ms: 1.09x faster                                                          |
| xml_etree_generate   | 99.4 ms                                                | 93.3 ms: 1.07x faster                                                         |
| xml_etree_iterparse  | 115 ms                                                 | 110 ms: 1.05x faster                                                          |
| unpickle_list        | 5.20 us                                                | 5.26 us: 1.01x slower                                                         |
| pickle_list          | 5.08 us                                                | 5.19 us: 1.02x slower                                                         |
| unpickle             | 14.4 us                                                | 15.7 us: 1.09x slower                                                         |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                         |
| pickle_dict          | 29.6 us                                                | 35.0 us: 1.18x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                         |
| python_startup_no_site | 5.93 ms                                                | 7.15 ms: 1.20x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                | 25.6 ms: 1.24x faster                                                         |
| django_template | 48.2 ms                                                | 39.8 ms: 1.21x faster                                                         |
| mako            | 16.3 ms                                                | 13.8 ms: 1.18x faster                                                         |
| genshi_xml      | 66.0 ms                                                | 58.7 ms: 1.13x faster                                                         |
| Geometric mean  | (ref)                                                  | 1.19x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 123 us: 4.41x faster                                                          |
| generators               | 80.1 ms                                                | 30.2 ms: 2.66x faster                                                         |
| async_tree_none          | 728 ms                                                 | 373 ms: 1.95x faster                                                          |
| deltablue                | 7.91 ms                                                | 4.15 ms: 1.91x faster                                                         |
| async_tree_io            | 1.77 sec                                               | 966 ms: 1.83x faster                                                          |
| logging_silent           | 190 ns                                                 | 105 ns: 1.81x faster                                                          |
| asyncio_tcp              | 922 ms                                                 | 517 ms: 1.78x faster                                                          |
| async_tree_memoization   | 870 ms                                                 | 499 ms: 1.74x faster                                                          |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 632 ms: 1.61x faster                                                          |
| pylint                   | 551 ms                                                 | 343 ms: 1.61x faster                                                          |
| raytrace                 | 507 ms                                                 | 319 ms: 1.59x faster                                                          |
| pickle_pure_python       | 484 us                                                 | 314 us: 1.54x faster                                                          |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                         |
| richards_super           | 94.7 ms                                                | 61.8 ms: 1.53x faster                                                         |
| chaos                    | 115 ms                                                 | 78.4 ms: 1.47x faster                                                         |
| scimark_sor              | 220 ms                                                 | 149 ms: 1.47x faster                                                          |
| sqlglot_parse            | 2.17 ms                                                | 1.48 ms: 1.47x faster                                                         |
| sqlglot_transpile        | 2.57 ms                                                | 1.80 ms: 1.43x faster                                                         |
| richards                 | 79.3 ms                                                | 55.6 ms: 1.43x faster                                                         |
| crypto_pyaes             | 128 ms                                                 | 92.0 ms: 1.39x faster                                                         |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                         |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.38x faster                                                        |
| scimark_monte_carlo      | 118 ms                                                 | 86.0 ms: 1.37x faster                                                         |
| deepcopy_memo            | 58.5 us                                                | 43.8 us: 1.34x faster                                                         |
| tornado_http             | 136 ms                                                 | 102 ms: 1.33x faster                                                          |
| float                    | 117 ms                                                 | 89.3 ms: 1.31x faster                                                         |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                         |
| thrift                   | 1.07 ms                                                | 821 us: 1.30x faster                                                          |
| go                       | 240 ms                                                 | 185 ms: 1.30x faster                                                          |
| logging_simple           | 8.30 us                                                | 6.40 us: 1.30x faster                                                         |
| nbody                    | 154 ms                                                 | 120 ms: 1.28x faster                                                          |
| deepcopy                 | 479 us                                                 | 376 us: 1.27x faster                                                          |
| deepcopy_reduce          | 4.17 us                                                | 3.28 us: 1.27x faster                                                         |
| chameleon                | 9.68 ms                                                | 7.62 ms: 1.27x faster                                                         |
| comprehensions           | 28.8 us                                                | 22.6 us: 1.27x faster                                                         |
| logging_format           | 9.09 us                                                | 7.17 us: 1.27x faster                                                         |
| genshi_text              | 31.8 ms                                                | 25.6 ms: 1.24x faster                                                         |
| tomli_loads              | 3.14 sec                                               | 2.53 sec: 1.24x faster                                                        |
| pycparser                | 1.58 sec                                               | 1.27 sec: 1.24x faster                                                        |
| xml_etree_process        | 79.1 ms                                                | 64.2 ms: 1.23x faster                                                         |
| spectral_norm            | 170 ms                                                 | 138 ms: 1.23x faster                                                          |
| html5lib                 | 88.9 ms                                                | 72.4 ms: 1.23x faster                                                         |
| pyflate                  | 716 ms                                                 | 588 ms: 1.22x faster                                                          |
| django_template          | 48.2 ms                                                | 39.8 ms: 1.21x faster                                                         |
| mako                     | 16.3 ms                                                | 13.8 ms: 1.18x faster                                                         |
| djangocms                | 38.4 us                                                | 32.7 us: 1.18x faster                                                         |
| unpickle_pure_python     | 331 us                                                 | 283 us: 1.17x faster                                                          |
| 2to3                     | 348 ms                                                 | 301 ms: 1.16x faster                                                          |
| sqlglot_normalize        | 143 ms                                                 | 123 ms: 1.16x faster                                                          |
| aiohttp                  | 1.44 ms                                                | 1.25 ms: 1.15x faster                                                         |
| dask                     | 441 ms                                                 | 382 ms: 1.15x faster                                                          |
| gunicorn                 | 1.53 ms                                                | 1.33 ms: 1.15x faster                                                         |
| dulwich_log              | 84.3 ms                                                | 73.8 ms: 1.14x faster                                                         |
| json_loads               | 31.2 us                                                | 27.5 us: 1.13x faster                                                         |
| genshi_xml               | 66.0 ms                                                | 58.7 ms: 1.13x faster                                                         |
| pathlib                  | 20.5 ms                                                | 18.2 ms: 1.12x faster                                                         |
| bench_thread_pool        | 986 us                                                 | 883 us: 1.12x faster                                                          |
| sympy_integrate          | 25.8 ms                                                | 23.1 ms: 1.12x faster                                                         |
| mypy2                    | 894 ms                                                 | 807 ms: 1.11x faster                                                          |
| sympy_sum                | 196 ms                                                 | 177 ms: 1.11x faster                                                          |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.85 ms: 1.11x faster                                                         |
| hexiom                   | 10.4 ms                                                | 9.45 ms: 1.10x faster                                                         |
| regex_v8                 | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                         |
| sqlglot_optimize         | 69.2 ms                                                | 63.3 ms: 1.09x faster                                                         |
| fannkuch                 | 532 ms                                                 | 487 ms: 1.09x faster                                                          |
| xml_etree_parse          | 168 ms                                                 | 154 ms: 1.09x faster                                                          |
| pprint_safe_repr         | 1.02 sec                                               | 939 ms: 1.08x faster                                                          |
| pprint_pformat           | 2.10 sec                                               | 1.94 sec: 1.08x faster                                                        |
| scimark_lu               | 176 ms                                                 | 163 ms: 1.08x faster                                                          |
| json                     | 5.69 ms                                                | 5.26 ms: 1.08x faster                                                         |
| sympy_str                | 346 ms                                                 | 321 ms: 1.08x faster                                                          |
| docutils                 | 3.30 sec                                               | 3.07 sec: 1.07x faster                                                        |
| scimark_fft              | 466 ms                                                 | 436 ms: 1.07x faster                                                          |
| xml_etree_generate       | 99.4 ms                                                | 93.3 ms: 1.07x faster                                                         |
| sympy_expand             | 566 ms                                                 | 534 ms: 1.06x faster                                                          |
| regex_compile            | 188 ms                                                 | 179 ms: 1.06x faster                                                          |
| xml_etree_iterparse      | 115 ms                                                 | 110 ms: 1.05x faster                                                          |
| mdp                      | 2.85 sec                                               | 2.79 sec: 1.02x faster                                                        |
| nqueens                  | 106 ms                                                 | 105 ms: 1.01x faster                                                          |
| asyncio_websockets       | 559 ms                                                 | 555 ms: 1.01x faster                                                          |
| gc_traversal             | 3.62 ms                                                | 3.64 ms: 1.00x slower                                                         |
| regex_dna                | 227 ms                                                 | 228 ms: 1.01x slower                                                          |
| unpickle_list            | 5.20 us                                                | 5.26 us: 1.01x slower                                                         |
| regex_effbot             | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                         |
| pickle_list              | 5.08 us                                                | 5.19 us: 1.02x slower                                                         |
| async_generators         | 444 ms                                                 | 478 ms: 1.08x slower                                                          |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                         |
| unpickle                 | 14.4 us                                                | 15.7 us: 1.09x slower                                                         |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                         |
| pidigits                 | 191 ms                                                 | 218 ms: 1.14x slower                                                          |
| pickle_dict              | 29.6 us                                                | 35.0 us: 1.18x slower                                                         |
| python_startup_no_site   | 5.93 ms                                                | 7.15 ms: 1.20x slower                                                         |
| coverage                 | 79.4 ms                                                | 99.3 ms: 1.25x slower                                                         |
| telco                    | 7.27 ms                                                | 9.13 ms: 1.26x slower                                                         |
| Geometric mean           | (ref)                                                  | 1.22x faster                                                                  |

Benchmark hidden because not significant (3): sqlite_synth, meteor_contest, bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240423-3.13.0a6+-fad1c67-PYTHON_UOPS/bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.13x
- 95% likely to have a speedup of 1.12x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.11x
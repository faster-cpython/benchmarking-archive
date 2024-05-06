# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 305 ms: 1.14x faster                                                    |
| chameleon      | 9.68 ms                                                | 7.57 ms: 1.28x faster                                                   |
| html5lib       | 88.9 ms                                                | 72.7 ms: 1.22x faster                                                   |
| tornado_http   | 136 ms                                                 | 102 ms: 1.33x faster                                                    |
| Geometric mean | (ref)                                                  | 1.24x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 372 ms: 1.96x faster                                                    |
| async_tree_io           | 1.77 sec                                               | 957 ms: 1.85x faster                                                    |
| async_tree_memoization  | 870 ms                                                 | 503 ms: 1.73x faster                                                    |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 634 ms: 1.60x faster                                                    |
| Geometric mean          | (ref)                                                  | 1.78x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 117 ms                                                 | 91.7 ms: 1.28x faster                                                   |
| nbody          | 154 ms                                                 | 129 ms: 1.19x faster                                                    |
| pidigits       | 191 ms                                                 | 191 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                  | 1.15x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                   |
| regex_compile  | 188 ms                                                 | 182 ms: 1.04x faster                                                    |
| regex_dna      | 227 ms                                                 | 224 ms: 1.01x faster                                                    |
| regex_effbot   | 3.63 ms                                                | 3.70 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 321 us: 1.51x faster                                                    |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.54 sec: 1.23x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 65.2 ms: 1.21x faster                                                   |
| json_loads           | 31.2 us                                                | 27.7 us: 1.13x faster                                                   |
| unpickle_pure_python | 331 us                                                 | 295 us: 1.12x faster                                                    |
| xml_etree_parse      | 168 ms                                                 | 151 ms: 1.11x faster                                                    |
| xml_etree_generate   | 99.4 ms                                                | 92.7 ms: 1.07x faster                                                   |
| xml_etree_iterparse  | 115 ms                                                 | 110 ms: 1.05x faster                                                    |
| pickle_list          | 5.08 us                                                | 5.15 us: 1.01x slower                                                   |
| unpickle             | 14.4 us                                                | 15.4 us: 1.07x slower                                                   |
| pickle               | 10.7 us                                                | 12.1 us: 1.14x slower                                                   |
| pickle_dict          | 29.6 us                                                | 35.2 us: 1.19x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                            |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                   |
| python_startup_no_site | 5.93 ms                                                | 7.13 ms: 1.20x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 13.9 ms: 1.18x faster                                                   |
| django_template | 48.2 ms                                                | 41.4 ms: 1.16x faster                                                   |
| genshi_text     | 31.8 ms                                                | 28.9 ms: 1.10x faster                                                   |
| genshi_xml      | 66.0 ms                                                | 65.5 ms: 1.01x faster                                                   |
| Geometric mean  | (ref)                                                  | 1.11x faster                                                            |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 196 us: 2.78x faster                                                    |
| generators               | 80.1 ms                                                | 29.6 ms: 2.70x faster                                                   |
| async_tree_none          | 728 ms                                                 | 372 ms: 1.96x faster                                                    |
| logging_silent           | 190 ns                                                 | 101 ns: 1.88x faster                                                    |
| async_tree_io            | 1.77 sec                                               | 957 ms: 1.85x faster                                                    |
| deltablue                | 7.91 ms                                                | 4.45 ms: 1.78x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 530 ms: 1.74x faster                                                    |
| async_tree_memoization   | 870 ms                                                 | 503 ms: 1.73x faster                                                    |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 634 ms: 1.60x faster                                                    |
| raytrace                 | 507 ms                                                 | 330 ms: 1.54x faster                                                    |
| pickle_pure_python       | 484 us                                                 | 321 us: 1.51x faster                                                    |
| richards_super           | 94.7 ms                                                | 63.5 ms: 1.49x faster                                                   |
| chaos                    | 115 ms                                                 | 79.8 ms: 1.45x faster                                                   |
| coroutines               | 35.1 ms                                                | 24.3 ms: 1.44x faster                                                   |
| sqlglot_parse            | 2.17 ms                                                | 1.52 ms: 1.43x faster                                                   |
| richards                 | 79.3 ms                                                | 56.7 ms: 1.40x faster                                                   |
| scimark_sor              | 220 ms                                                 | 157 ms: 1.39x faster                                                    |
| sqlglot_transpile        | 2.57 ms                                                | 1.85 ms: 1.39x faster                                                   |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                   |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.37x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 93.6 ms: 1.37x faster                                                   |
| tornado_http             | 136 ms                                                 | 102 ms: 1.33x faster                                                    |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                   |
| thrift                   | 1.07 ms                                                | 833 us: 1.29x faster                                                    |
| scimark_monte_carlo      | 118 ms                                                 | 92.1 ms: 1.28x faster                                                   |
| chameleon                | 9.68 ms                                                | 7.57 ms: 1.28x faster                                                   |
| float                    | 117 ms                                                 | 91.7 ms: 1.28x faster                                                   |
| deepcopy_memo            | 58.5 us                                                | 47.3 us: 1.24x faster                                                   |
| pycparser                | 1.58 sec                                               | 1.28 sec: 1.23x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.54 sec: 1.23x faster                                                  |
| html5lib                 | 88.9 ms                                                | 72.7 ms: 1.22x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.41 us: 1.22x faster                                                   |
| xml_etree_process        | 79.1 ms                                                | 65.2 ms: 1.21x faster                                                   |
| pyflate                  | 716 ms                                                 | 592 ms: 1.21x faster                                                    |
| logging_simple           | 8.30 us                                                | 6.90 us: 1.20x faster                                                   |
| deepcopy                 | 479 us                                                 | 401 us: 1.20x faster                                                    |
| nbody                    | 154 ms                                                 | 129 ms: 1.19x faster                                                    |
| logging_format           | 9.09 us                                                | 7.66 us: 1.19x faster                                                   |
| djangocms                | 38.4 us                                                | 32.6 us: 1.18x faster                                                   |
| mako                     | 16.3 ms                                                | 13.9 ms: 1.18x faster                                                   |
| spectral_norm            | 170 ms                                                 | 144 ms: 1.18x faster                                                    |
| comprehensions           | 28.8 us                                                | 24.7 us: 1.16x faster                                                   |
| django_template          | 48.2 ms                                                | 41.4 ms: 1.16x faster                                                   |
| aiohttp                  | 1.44 ms                                                | 1.24 ms: 1.16x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.34 ms: 1.15x faster                                                   |
| 2to3                     | 348 ms                                                 | 305 ms: 1.14x faster                                                    |
| dulwich_log              | 84.3 ms                                                | 73.9 ms: 1.14x faster                                                   |
| go                       | 240 ms                                                 | 212 ms: 1.13x faster                                                    |
| dask                     | 441 ms                                                 | 390 ms: 1.13x faster                                                    |
| json_loads               | 31.2 us                                                | 27.7 us: 1.13x faster                                                   |
| unpickle_pure_python     | 331 us                                                 | 295 us: 1.12x faster                                                    |
| regex_v8                 | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                   |
| xml_etree_parse          | 168 ms                                                 | 151 ms: 1.11x faster                                                    |
| pathlib                  | 20.5 ms                                                | 18.5 ms: 1.11x faster                                                   |
| sqlglot_normalize        | 143 ms                                                 | 129 ms: 1.11x faster                                                    |
| genshi_text              | 31.8 ms                                                | 28.9 ms: 1.10x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 902 us: 1.09x faster                                                    |
| sympy_sum                | 196 ms                                                 | 180 ms: 1.09x faster                                                    |
| json                     | 5.69 ms                                                | 5.23 ms: 1.09x faster                                                   |
| sympy_integrate          | 25.8 ms                                                | 23.8 ms: 1.08x faster                                                   |
| xml_etree_generate       | 99.4 ms                                                | 92.7 ms: 1.07x faster                                                   |
| pprint_safe_repr         | 1.02 sec                                               | 953 ms: 1.07x faster                                                    |
| fannkuch                 | 532 ms                                                 | 499 ms: 1.07x faster                                                    |
| pprint_pformat           | 2.10 sec                                               | 1.98 sec: 1.06x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 65.3 ms: 1.06x faster                                                   |
| scimark_lu               | 176 ms                                                 | 168 ms: 1.05x faster                                                    |
| xml_etree_iterparse      | 115 ms                                                 | 110 ms: 1.05x faster                                                    |
| sympy_str                | 346 ms                                                 | 331 ms: 1.04x faster                                                    |
| regex_compile            | 188 ms                                                 | 182 ms: 1.04x faster                                                    |
| sympy_expand             | 566 ms                                                 | 549 ms: 1.03x faster                                                    |
| scimark_fft              | 466 ms                                                 | 454 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.32 ms: 1.02x faster                                                   |
| hexiom                   | 10.4 ms                                                | 10.2 ms: 1.02x faster                                                   |
| regex_dna                | 227 ms                                                 | 224 ms: 1.01x faster                                                    |
| genshi_xml               | 66.0 ms                                                | 65.5 ms: 1.01x faster                                                   |
| pidigits                 | 191 ms                                                 | 191 ms: 1.00x slower                                                    |
| sqlite_synth             | 3.02 us                                                | 3.06 us: 1.01x slower                                                   |
| pickle_list              | 5.08 us                                                | 5.15 us: 1.01x slower                                                   |
| asyncio_websockets       | 559 ms                                                 | 568 ms: 1.02x slower                                                    |
| regex_effbot             | 3.63 ms                                                | 3.70 ms: 1.02x slower                                                   |
| meteor_contest           | 120 ms                                                 | 123 ms: 1.03x slower                                                    |
| nqueens                  | 106 ms                                                 | 111 ms: 1.04x slower                                                    |
| mdp                      | 2.85 sec                                               | 3.01 sec: 1.06x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.4 us: 1.07x slower                                                   |
| async_generators         | 444 ms                                                 | 477 ms: 1.07x slower                                                    |
| create_gc_cycles         | 1.62 ms                                                | 1.78 ms: 1.10x slower                                                   |
| gc_traversal             | 3.62 ms                                                | 4.05 ms: 1.12x slower                                                   |
| pickle                   | 10.7 us                                                | 12.1 us: 1.14x slower                                                   |
| pickle_dict              | 29.6 us                                                | 35.2 us: 1.19x slower                                                   |
| python_startup_no_site   | 5.93 ms                                                | 7.13 ms: 1.20x slower                                                   |
| coverage                 | 79.4 ms                                                | 97.6 ms: 1.23x slower                                                   |
| telco                    | 7.27 ms                                                | 9.32 ms: 1.28x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.18x faster                                                            |

Benchmark hidden because not significant (2): unpickle_list, bench_mp_pool
Ignored benchmarks (7) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: docutils, flaskblogging, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-65aa34a-PYTHON_UOPS/bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.11x
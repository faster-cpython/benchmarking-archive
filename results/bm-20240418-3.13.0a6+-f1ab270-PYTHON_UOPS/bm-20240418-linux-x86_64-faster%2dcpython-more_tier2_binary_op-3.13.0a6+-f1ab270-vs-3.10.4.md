# Results vs. 3.10.4

- fork: faster-cpython
- ref: more_tier2_binary_op
- machine: linux-x86_64
- commit hash: f1ab270
- commit date: 2024-04-18
- overall geometric mean: 1.08x faster
- HPT reliability: 91.62%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 330 ms: 1.06x faster                                                             |
| chameleon      | 9.68 ms                                                | 8.18 ms: 1.18x faster                                                            |
| docutils       | 3.30 sec                                               | 3.27 sec: 1.01x faster                                                           |
| html5lib       | 88.9 ms                                                | 73.7 ms: 1.21x faster                                                            |
| tornado_http   | 136 ms                                                 | 103 ms: 1.32x faster                                                             |
| Geometric mean | (ref)                                                  | 1.15x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 397 ms: 1.83x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 1.01 sec: 1.75x faster                                                           |
| async_tree_memoization  | 870 ms                                                 | 530 ms: 1.64x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 661 ms: 1.54x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.69x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                 | 202 ms: 1.06x slower                                                             |
| float          | 117 ms                                                 | 135 ms: 1.15x slower                                                             |
| nbody          | 154 ms                                                 | 209 ms: 1.36x slower                                                             |
| Geometric mean | (ref)                                                  | 1.18x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                            |
| regex_dna      | 227 ms                                                 | 226 ms: 1.00x faster                                                             |
| regex_compile  | 188 ms                                                 | 220 ms: 1.17x slower                                                             |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 316 us: 1.53x faster                                                             |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 70.8 ms: 1.12x faster                                                            |
| json_loads           | 31.2 us                                                | 27.9 us: 1.12x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 154 ms: 1.09x faster                                                             |
| unpickle_list        | 5.20 us                                                | 5.08 us: 1.02x faster                                                            |
| pickle_list          | 5.08 us                                                | 4.97 us: 1.02x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 104 ms: 1.05x slower                                                             |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                            |
| tomli_loads          | 3.14 sec                                               | 3.52 sec: 1.12x slower                                                           |
| xml_etree_iterparse  | 115 ms                                                 | 130 ms: 1.13x slower                                                             |
| pickle_dict          | 29.6 us                                                | 34.4 us: 1.16x slower                                                            |
| unpickle             | 14.4 us                                                | 17.0 us: 1.18x slower                                                            |
| unpickle_pure_python | 331 us                                                 | 404 us: 1.22x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                | 26.9 ms: 1.18x faster                                                            |
| django_template | 48.2 ms                                                | 43.3 ms: 1.11x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 64.0 ms: 1.03x faster                                                            |
| mako            | 16.3 ms                                                | 21.1 ms: 1.29x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 130 us: 4.18x faster                                                             |
| generators               | 80.1 ms                                                | 29.7 ms: 2.69x faster                                                            |
| async_tree_none          | 728 ms                                                 | 397 ms: 1.83x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 514 ms: 1.79x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 1.01 sec: 1.75x faster                                                           |
| logging_silent           | 190 ns                                                 | 109 ns: 1.74x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 530 ms: 1.64x faster                                                             |
| deltablue                | 7.91 ms                                                | 5.02 ms: 1.58x faster                                                            |
| coroutines               | 35.1 ms                                                | 22.5 ms: 1.56x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 661 ms: 1.54x faster                                                             |
| pylint                   | 551 ms                                                 | 360 ms: 1.53x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 316 us: 1.53x faster                                                             |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.38x faster                                                           |
| raytrace                 | 507 ms                                                 | 378 ms: 1.34x faster                                                             |
| sqlglot_parse            | 2.17 ms                                                | 1.63 ms: 1.33x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                            |
| tornado_http             | 136 ms                                                 | 103 ms: 1.32x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.97 ms: 1.30x faster                                                            |
| thrift                   | 1.07 ms                                                | 836 us: 1.28x faster                                                             |
| logging_simple           | 8.30 us                                                | 6.58 us: 1.26x faster                                                            |
| scimark_sor              | 220 ms                                                 | 174 ms: 1.26x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.39 us: 1.23x faster                                                            |
| logging_format           | 9.09 us                                                | 7.39 us: 1.23x faster                                                            |
| deepcopy                 | 479 us                                                 | 395 us: 1.21x faster                                                             |
| djangocms                | 38.4 us                                                | 31.8 us: 1.21x faster                                                            |
| html5lib                 | 88.9 ms                                                | 73.7 ms: 1.21x faster                                                            |
| genshi_text              | 31.8 ms                                                | 26.9 ms: 1.18x faster                                                            |
| chameleon                | 9.68 ms                                                | 8.18 ms: 1.18x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 49.9 us: 1.17x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.35 sec: 1.17x faster                                                           |
| richards_super           | 94.7 ms                                                | 81.6 ms: 1.16x faster                                                            |
| aiohttp                  | 1.44 ms                                                | 1.25 ms: 1.15x faster                                                            |
| gunicorn                 | 1.53 ms                                                | 1.34 ms: 1.14x faster                                                            |
| dask                     | 441 ms                                                 | 388 ms: 1.14x faster                                                             |
| chaos                    | 115 ms                                                 | 103 ms: 1.12x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 70.8 ms: 1.12x faster                                                            |
| json_loads               | 31.2 us                                                | 27.9 us: 1.12x faster                                                            |
| django_template          | 48.2 ms                                                | 43.3 ms: 1.11x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 75.8 ms: 1.11x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.5 ms: 1.11x faster                                                            |
| json                     | 5.69 ms                                                | 5.16 ms: 1.10x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 154 ms: 1.09x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                            |
| mypy2                    | 894 ms                                                 | 831 ms: 1.08x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 133 ms: 1.07x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 928 us: 1.06x faster                                                             |
| 2to3                     | 348 ms                                                 | 330 ms: 1.06x faster                                                             |
| richards                 | 79.3 ms                                                | 75.2 ms: 1.05x faster                                                            |
| go                       | 240 ms                                                 | 229 ms: 1.05x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 64.0 ms: 1.03x faster                                                            |
| sympy_sum                | 196 ms                                                 | 191 ms: 1.03x faster                                                             |
| unpickle_list            | 5.20 us                                                | 5.08 us: 1.02x faster                                                            |
| pickle_list              | 5.08 us                                                | 4.97 us: 1.02x faster                                                            |
| sympy_integrate          | 25.8 ms                                                | 25.3 ms: 1.02x faster                                                            |
| sympy_expand             | 566 ms                                                 | 556 ms: 1.02x faster                                                             |
| docutils                 | 3.30 sec                                               | 3.27 sec: 1.01x faster                                                           |
| regex_dna                | 227 ms                                                 | 226 ms: 1.00x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 128 ms: 1.00x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 70.4 ms: 1.02x slower                                                            |
| sqlite_synth             | 3.02 us                                                | 3.15 us: 1.04x slower                                                            |
| xml_etree_generate       | 99.4 ms                                                | 104 ms: 1.05x slower                                                             |
| mdp                      | 2.85 sec                                               | 3.01 sec: 1.06x slower                                                           |
| pidigits                 | 191 ms                                                 | 202 ms: 1.06x slower                                                             |
| gc_traversal             | 3.62 ms                                                | 3.90 ms: 1.08x slower                                                            |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.79 ms: 1.10x slower                                                            |
| tomli_loads              | 3.14 sec                                               | 3.52 sec: 1.12x slower                                                           |
| xml_etree_iterparse      | 115 ms                                                 | 130 ms: 1.13x slower                                                             |
| async_generators         | 444 ms                                                 | 503 ms: 1.13x slower                                                             |
| float                    | 117 ms                                                 | 135 ms: 1.15x slower                                                             |
| pickle_dict              | 29.6 us                                                | 34.4 us: 1.16x slower                                                            |
| regex_compile            | 188 ms                                                 | 220 ms: 1.17x slower                                                             |
| scimark_lu               | 176 ms                                                 | 208 ms: 1.18x slower                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 139 ms: 1.18x slower                                                             |
| unpickle                 | 14.4 us                                                | 17.0 us: 1.18x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                            |
| meteor_contest           | 120 ms                                                 | 145 ms: 1.21x slower                                                             |
| unpickle_pure_python     | 331 us                                                 | 404 us: 1.22x slower                                                             |
| pyflate                  | 716 ms                                                 | 878 ms: 1.23x slower                                                             |
| pprint_safe_repr         | 1.02 sec                                               | 1.25 sec: 1.23x slower                                                           |
| pprint_pformat           | 2.10 sec                                               | 2.60 sec: 1.24x slower                                                           |
| coverage                 | 79.4 ms                                                | 98.5 ms: 1.24x slower                                                            |
| comprehensions           | 28.8 us                                                | 36.1 us: 1.26x slower                                                            |
| mako                     | 16.3 ms                                                | 21.1 ms: 1.29x slower                                                            |
| telco                    | 7.27 ms                                                | 9.78 ms: 1.35x slower                                                            |
| scimark_fft              | 466 ms                                                 | 633 ms: 1.36x slower                                                             |
| nbody                    | 154 ms                                                 | 209 ms: 1.36x slower                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 9.00 ms: 1.39x slower                                                            |
| spectral_norm            | 170 ms                                                 | 242 ms: 1.43x slower                                                             |
| fannkuch                 | 532 ms                                                 | 764 ms: 1.44x slower                                                             |
| nqueens                  | 106 ms                                                 | 153 ms: 1.44x slower                                                             |
| hexiom                   | 10.4 ms                                                | 15.1 ms: 1.46x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.08x faster                                                                     |

Benchmark hidden because not significant (3): regex_effbot, bench_mp_pool, sympy_str
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240418-3.13.0a6+-f1ab270-PYTHON_UOPS/bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 91.62% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x
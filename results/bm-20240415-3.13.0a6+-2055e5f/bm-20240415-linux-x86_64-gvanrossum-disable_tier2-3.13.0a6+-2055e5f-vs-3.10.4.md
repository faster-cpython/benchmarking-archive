# Results vs. 3.10.4

- fork: gvanrossum
- ref: disable_tier2
- machine: linux-x86_64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.36x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 268 ms: 1.30x faster                                                |
| chameleon      | 9.68 ms                                                | 6.91 ms: 1.40x faster                                               |
| docutils       | 3.30 sec                                               | 2.79 sec: 1.18x faster                                              |
| html5lib       | 88.9 ms                                                | 67.5 ms: 1.32x faster                                               |
| tornado_http   | 136 ms                                                 | 94.3 ms: 1.45x faster                                               |
| Geometric mean | (ref)                                                  | 1.33x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                                |
| async_tree_io           | 1.77 sec                                               | 916 ms: 1.93x faster                                                |
| async_tree_memoization  | 870 ms                                                 | 465 ms: 1.87x faster                                                |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 610 ms: 1.67x faster                                                |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 85.7 ms: 1.79x faster                                               |
| float          | 117 ms                                                 | 77.7 ms: 1.51x faster                                               |
| pidigits       | 191 ms                                                 | 198 ms: 1.04x slower                                                |
| Geometric mean | (ref)                                                  | 1.38x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.41x faster                                                |
| regex_v8       | 27.8 ms                                                | 25.9 ms: 1.07x faster                                               |
| regex_dna      | 227 ms                                                 | 226 ms: 1.00x faster                                                |
| regex_effbot   | 3.63 ms                                                | 3.82 ms: 1.05x slower                                               |
| Geometric mean | (ref)                                                  | 1.10x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 298 us: 1.62x faster                                                |
| unpickle_pure_python | 331 us                                                 | 212 us: 1.56x faster                                                |
| tomli_loads          | 3.14 sec                                               | 2.09 sec: 1.50x faster                                              |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                               |
| xml_etree_process    | 79.1 ms                                                | 59.9 ms: 1.32x faster                                               |
| xml_etree_generate   | 99.4 ms                                                | 86.9 ms: 1.14x faster                                               |
| json_loads           | 31.2 us                                                | 27.9 us: 1.12x faster                                               |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                |
| xml_etree_parse      | 168 ms                                                 | 161 ms: 1.04x faster                                                |
| unpickle_list        | 5.20 us                                                | 5.07 us: 1.03x faster                                               |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                               |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                               |
| pickle_dict          | 29.6 us                                                | 34.0 us: 1.15x slower                                               |
| unpickle             | 14.4 us                                                | 17.0 us: 1.18x slower                                               |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                               |
| python_startup_no_site | 5.93 ms                                                | 7.12 ms: 1.20x slower                                               |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.8 ms: 1.52x faster                                               |
| django_template | 48.2 ms                                                | 34.4 ms: 1.40x faster                                               |
| genshi_text     | 31.8 ms                                                | 23.7 ms: 1.34x faster                                               |
| genshi_xml      | 66.0 ms                                                | 52.4 ms: 1.26x faster                                               |
| Geometric mean  | (ref)                                                  | 1.38x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 115 us: 4.75x faster                                                |
| generators               | 80.1 ms                                                | 29.4 ms: 2.72x faster                                               |
| deltablue                | 7.91 ms                                                | 3.14 ms: 2.52x faster                                               |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                                |
| logging_silent           | 190 ns                                                 | 96.2 ns: 1.97x faster                                               |
| raytrace                 | 507 ms                                                 | 259 ms: 1.96x faster                                                |
| chaos                    | 115 ms                                                 | 59.5 ms: 1.94x faster                                               |
| async_tree_io            | 1.77 sec                                               | 916 ms: 1.93x faster                                                |
| async_tree_memoization   | 870 ms                                                 | 465 ms: 1.87x faster                                                |
| asyncio_tcp              | 922 ms                                                 | 505 ms: 1.83x faster                                                |
| scimark_sor              | 220 ms                                                 | 120 ms: 1.82x faster                                                |
| richards_super           | 94.7 ms                                                | 52.2 ms: 1.82x faster                                               |
| nbody                    | 154 ms                                                 | 85.7 ms: 1.79x faster                                               |
| comprehensions           | 28.8 us                                                | 16.2 us: 1.78x faster                                               |
| scimark_monte_carlo      | 118 ms                                                 | 67.3 ms: 1.76x faster                                               |
| pylint                   | 551 ms                                                 | 319 ms: 1.73x faster                                                |
| go                       | 240 ms                                                 | 140 ms: 1.72x faster                                                |
| richards                 | 79.3 ms                                                | 46.3 ms: 1.71x faster                                               |
| sqlglot_parse            | 2.17 ms                                                | 1.27 ms: 1.71x faster                                               |
| crypto_pyaes             | 128 ms                                                 | 74.8 ms: 1.71x faster                                               |
| hexiom                   | 10.4 ms                                                | 6.13 ms: 1.70x faster                                               |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 610 ms: 1.67x faster                                                |
| pickle_pure_python       | 484 us                                                 | 298 us: 1.62x faster                                                |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                               |
| deepcopy_memo            | 58.5 us                                                | 37.1 us: 1.57x faster                                               |
| unpickle_pure_python     | 331 us                                                 | 212 us: 1.56x faster                                                |
| pyflate                  | 716 ms                                                 | 463 ms: 1.55x faster                                                |
| spectral_norm            | 170 ms                                                 | 111 ms: 1.53x faster                                                |
| scimark_lu               | 176 ms                                                 | 115 ms: 1.53x faster                                                |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.52x faster                                               |
| coroutines               | 35.1 ms                                                | 23.1 ms: 1.52x faster                                               |
| float                    | 117 ms                                                 | 77.7 ms: 1.51x faster                                               |
| tomli_loads              | 3.14 sec                                               | 2.09 sec: 1.50x faster                                              |
| logging_simple           | 8.30 us                                                | 5.64 us: 1.47x faster                                               |
| logging_format           | 9.09 us                                                | 6.26 us: 1.45x faster                                               |
| tornado_http             | 136 ms                                                 | 94.3 ms: 1.45x faster                                               |
| regex_compile            | 188 ms                                                 | 134 ms: 1.41x faster                                                |
| chameleon                | 9.68 ms                                                | 6.91 ms: 1.40x faster                                               |
| django_template          | 48.2 ms                                                | 34.4 ms: 1.40x faster                                               |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                              |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                               |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.37x faster                                              |
| deepcopy                 | 479 us                                                 | 351 us: 1.36x faster                                                |
| fannkuch                 | 532 ms                                                 | 391 ms: 1.36x faster                                                |
| pprint_safe_repr         | 1.02 sec                                               | 749 ms: 1.36x faster                                                |
| genshi_text              | 31.8 ms                                                | 23.7 ms: 1.34x faster                                               |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                               |
| nqueens                  | 106 ms                                                 | 79.6 ms: 1.33x faster                                               |
| xml_etree_process        | 79.1 ms                                                | 59.9 ms: 1.32x faster                                               |
| deepcopy_reduce          | 4.17 us                                                | 3.16 us: 1.32x faster                                               |
| html5lib                 | 88.9 ms                                                | 67.5 ms: 1.32x faster                                               |
| pycparser                | 1.58 sec                                               | 1.20 sec: 1.31x faster                                              |
| thrift                   | 1.07 ms                                                | 818 us: 1.31x faster                                                |
| sqlglot_normalize        | 143 ms                                                 | 109 ms: 1.31x faster                                                |
| 2to3                     | 348 ms                                                 | 268 ms: 1.30x faster                                                |
| dulwich_log              | 84.3 ms                                                | 65.9 ms: 1.28x faster                                               |
| sympy_integrate          | 25.8 ms                                                | 20.2 ms: 1.28x faster                                               |
| sympy_sum                | 196 ms                                                 | 154 ms: 1.27x faster                                                |
| sqlglot_optimize         | 69.2 ms                                                | 54.7 ms: 1.26x faster                                               |
| scimark_fft              | 466 ms                                                 | 369 ms: 1.26x faster                                                |
| genshi_xml               | 66.0 ms                                                | 52.4 ms: 1.26x faster                                               |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.17 ms: 1.25x faster                                               |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                               |
| djangocms                | 38.4 us                                                | 31.3 us: 1.23x faster                                               |
| mypy2                    | 894 ms                                                 | 738 ms: 1.21x faster                                                |
| dask                     | 441 ms                                                 | 366 ms: 1.20x faster                                                |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                               |
| sympy_expand             | 566 ms                                                 | 470 ms: 1.20x faster                                                |
| bench_thread_pool        | 986 us                                                 | 834 us: 1.18x faster                                                |
| docutils                 | 3.30 sec                                               | 2.79 sec: 1.18x faster                                              |
| pathlib                  | 20.5 ms                                                | 17.8 ms: 1.15x faster                                               |
| xml_etree_generate       | 99.4 ms                                                | 86.9 ms: 1.14x faster                                               |
| json_loads               | 31.2 us                                                | 27.9 us: 1.12x faster                                               |
| mdp                      | 2.85 sec                                               | 2.56 sec: 1.11x faster                                              |
| json                     | 5.69 ms                                                | 5.16 ms: 1.10x faster                                               |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                |
| regex_v8                 | 27.8 ms                                                | 25.9 ms: 1.07x faster                                               |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                |
| xml_etree_parse          | 168 ms                                                 | 161 ms: 1.04x faster                                                |
| sqlite_synth             | 3.02 us                                                | 2.94 us: 1.03x faster                                               |
| unpickle_list            | 5.20 us                                                | 5.07 us: 1.03x faster                                               |
| pickle_list              | 5.08 us                                                | 5.00 us: 1.02x faster                                               |
| regex_dna                | 227 ms                                                 | 226 ms: 1.00x faster                                                |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                |
| pidigits                 | 191 ms                                                 | 198 ms: 1.04x slower                                                |
| regex_effbot             | 3.63 ms                                                | 3.82 ms: 1.05x slower                                               |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                               |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                               |
| gc_traversal             | 3.62 ms                                                | 4.01 ms: 1.11x slower                                               |
| pickle_dict              | 29.6 us                                                | 34.0 us: 1.15x slower                                               |
| unpickle                 | 14.4 us                                                | 17.0 us: 1.18x slower                                               |
| telco                    | 7.27 ms                                                | 8.69 ms: 1.20x slower                                               |
| python_startup_no_site   | 5.93 ms                                                | 7.12 ms: 1.20x slower                                               |
| coverage                 | 79.4 ms                                                | 96.4 ms: 1.21x slower                                               |
| Geometric mean           | (ref)                                                  | 1.36x faster                                                        |

Benchmark hidden because not significant (2): bench_mp_pool, async_generators
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240415-3.13.0a6+-2055e5f/bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: 1.10x
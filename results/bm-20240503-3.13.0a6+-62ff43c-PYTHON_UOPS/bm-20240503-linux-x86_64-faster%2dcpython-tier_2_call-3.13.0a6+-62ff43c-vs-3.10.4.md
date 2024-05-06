# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 62ff43c
- commit date: 2024-05-03
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 327 ms: 1.07x faster                                                    |
| chameleon      | 9.68 ms                                                | 8.06 ms: 1.20x faster                                                   |
| html5lib       | 88.9 ms                                                | 77.8 ms: 1.14x faster                                                   |
| tornado_http   | 136 ms                                                 | 105 ms: 1.29x faster                                                    |
| Geometric mean | (ref)                                                  | 1.17x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 380 ms: 1.91x faster                                                    |
| async_tree_io           | 1.77 sec                                               | 985 ms: 1.80x faster                                                    |
| async_tree_memoization  | 870 ms                                                 | 512 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 640 ms: 1.59x faster                                                    |
| Geometric mean          | (ref)                                                  | 1.75x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 117 ms                                                 | 90.6 ms: 1.29x faster                                                   |
| nbody          | 154 ms                                                 | 122 ms: 1.26x faster                                                    |
| pidigits       | 191 ms                                                 | 196 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                  | 1.17x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.6 ms: 1.09x faster                                                   |
| regex_compile  | 188 ms                                                 | 190 ms: 1.01x slower                                                    |
| regex_effbot   | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 14.2 ms                                                | 11.1 ms: 1.27x faster                                                   |
| pickle_pure_python   | 484 us                                                 | 405 us: 1.20x faster                                                    |
| tomli_loads          | 3.14 sec                                               | 2.65 sec: 1.18x faster                                                  |
| unpickle_pure_python | 331 us                                                 | 285 us: 1.16x faster                                                    |
| xml_etree_process    | 79.1 ms                                                | 68.4 ms: 1.16x faster                                                   |
| json_loads           | 31.2 us                                                | 27.8 us: 1.12x faster                                                   |
| xml_etree_parse      | 168 ms                                                 | 152 ms: 1.11x faster                                                    |
| xml_etree_iterparse  | 115 ms                                                 | 111 ms: 1.04x faster                                                    |
| xml_etree_generate   | 99.4 ms                                                | 97.6 ms: 1.02x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.13 us: 1.01x slower                                                   |
| unpickle             | 14.4 us                                                | 15.7 us: 1.09x slower                                                   |
| pickle               | 10.7 us                                                | 11.9 us: 1.11x slower                                                   |
| pickle_dict          | 29.6 us                                                | 34.0 us: 1.15x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.06x faster                                                            |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.7 ms: 1.36x faster                                                   |
| python_startup_no_site | 5.93 ms                                                | 7.23 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.06x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 14.0 ms: 1.17x faster                                                   |
| django_template | 48.2 ms                                                | 44.5 ms: 1.08x faster                                                   |
| genshi_text     | 31.8 ms                                                | 32.0 ms: 1.00x slower                                                   |
| genshi_xml      | 66.0 ms                                                | 72.9 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                            |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 194 us: 2.81x faster                                                    |
| generators               | 80.1 ms                                                | 30.6 ms: 2.62x faster                                                   |
| async_tree_none          | 728 ms                                                 | 380 ms: 1.91x faster                                                    |
| deltablue                | 7.91 ms                                                | 4.37 ms: 1.81x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 985 ms: 1.80x faster                                                    |
| asyncio_tcp              | 922 ms                                                 | 532 ms: 1.73x faster                                                    |
| async_tree_memoization   | 870 ms                                                 | 512 ms: 1.70x faster                                                    |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 640 ms: 1.59x faster                                                    |
| raytrace                 | 507 ms                                                 | 331 ms: 1.53x faster                                                    |
| pylint                   | 551 ms                                                 | 367 ms: 1.50x faster                                                    |
| richards_super           | 94.7 ms                                                | 66.6 ms: 1.42x faster                                                   |
| coroutines               | 35.1 ms                                                | 24.9 ms: 1.41x faster                                                   |
| crypto_pyaes             | 128 ms                                                 | 91.9 ms: 1.39x faster                                                   |
| scimark_sor              | 220 ms                                                 | 159 ms: 1.38x faster                                                    |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.37x faster                                                  |
| chaos                    | 115 ms                                                 | 84.4 ms: 1.37x faster                                                   |
| python_startup           | 14.6 ms                                                | 10.7 ms: 1.36x faster                                                   |
| richards                 | 79.3 ms                                                | 59.4 ms: 1.34x faster                                                   |
| go                       | 240 ms                                                 | 181 ms: 1.32x faster                                                    |
| scimark_monte_carlo      | 118 ms                                                 | 90.1 ms: 1.31x faster                                                   |
| sqlglot_parse            | 2.17 ms                                                | 1.67 ms: 1.30x faster                                                   |
| logging_silent           | 190 ns                                                 | 146 ns: 1.30x faster                                                    |
| tornado_http             | 136 ms                                                 | 105 ms: 1.29x faster                                                    |
| float                    | 117 ms                                                 | 90.6 ms: 1.29x faster                                                   |
| json_dumps               | 14.2 ms                                                | 11.1 ms: 1.27x faster                                                   |
| logging_simple           | 8.30 us                                                | 6.55 us: 1.27x faster                                                   |
| thrift                   | 1.07 ms                                                | 851 us: 1.26x faster                                                    |
| nbody                    | 154 ms                                                 | 122 ms: 1.26x faster                                                    |
| sqlglot_transpile        | 2.57 ms                                                | 2.05 ms: 1.26x faster                                                   |
| logging_format           | 9.09 us                                                | 7.30 us: 1.25x faster                                                   |
| spectral_norm            | 170 ms                                                 | 140 ms: 1.21x faster                                                    |
| chameleon                | 9.68 ms                                                | 8.06 ms: 1.20x faster                                                   |
| pickle_pure_python       | 484 us                                                 | 405 us: 1.20x faster                                                    |
| tomli_loads              | 3.14 sec                                               | 2.65 sec: 1.18x faster                                                  |
| pyflate                  | 716 ms                                                 | 609 ms: 1.18x faster                                                    |
| mako                     | 16.3 ms                                                | 14.0 ms: 1.17x faster                                                   |
| unpickle_pure_python     | 331 us                                                 | 285 us: 1.16x faster                                                    |
| xml_etree_process        | 79.1 ms                                                | 68.4 ms: 1.16x faster                                                   |
| djangocms                | 38.4 us                                                | 33.2 us: 1.16x faster                                                   |
| comprehensions           | 28.8 us                                                | 25.1 us: 1.15x faster                                                   |
| html5lib                 | 88.9 ms                                                | 77.8 ms: 1.14x faster                                                   |
| deepcopy_memo            | 58.5 us                                                | 51.4 us: 1.14x faster                                                   |
| aiohttp                  | 1.44 ms                                                | 1.28 ms: 1.13x faster                                                   |
| dask                     | 441 ms                                                 | 393 ms: 1.12x faster                                                    |
| json_loads               | 31.2 us                                                | 27.8 us: 1.12x faster                                                   |
| dulwich_log              | 84.3 ms                                                | 75.5 ms: 1.12x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.38 ms: 1.11x faster                                                   |
| pycparser                | 1.58 sec                                               | 1.42 sec: 1.11x faster                                                  |
| xml_etree_parse          | 168 ms                                                 | 152 ms: 1.11x faster                                                    |
| pathlib                  | 20.5 ms                                                | 18.6 ms: 1.10x faster                                                   |
| fannkuch                 | 532 ms                                                 | 487 ms: 1.09x faster                                                    |
| json                     | 5.69 ms                                                | 5.24 ms: 1.09x faster                                                   |
| regex_v8                 | 27.8 ms                                                | 25.6 ms: 1.09x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.84 us: 1.09x faster                                                   |
| django_template          | 48.2 ms                                                | 44.5 ms: 1.08x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 914 us: 1.08x faster                                                    |
| hexiom                   | 10.4 ms                                                | 9.66 ms: 1.08x faster                                                   |
| 2to3                     | 348 ms                                                 | 327 ms: 1.07x faster                                                    |
| sympy_sum                | 196 ms                                                 | 184 ms: 1.07x faster                                                    |
| scimark_lu               | 176 ms                                                 | 167 ms: 1.06x faster                                                    |
| pprint_pformat           | 2.10 sec                                               | 1.99 sec: 1.06x faster                                                  |
| pprint_safe_repr         | 1.02 sec                                               | 968 ms: 1.05x faster                                                    |
| scimark_fft              | 466 ms                                                 | 443 ms: 1.05x faster                                                    |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.17 ms: 1.05x faster                                                   |
| sqlglot_normalize        | 143 ms                                                 | 137 ms: 1.05x faster                                                    |
| xml_etree_iterparse      | 115 ms                                                 | 111 ms: 1.04x faster                                                    |
| deepcopy                 | 479 us                                                 | 459 us: 1.04x faster                                                    |
| sympy_integrate          | 25.8 ms                                                | 24.8 ms: 1.04x faster                                                   |
| mypy2                    | 894 ms                                                 | 859 ms: 1.04x faster                                                    |
| sqlglot_optimize         | 69.2 ms                                                | 66.6 ms: 1.04x faster                                                   |
| xml_etree_generate       | 99.4 ms                                                | 97.6 ms: 1.02x faster                                                   |
| mdp                      | 2.85 sec                                               | 2.81 sec: 1.01x faster                                                  |
| sqlite_synth             | 3.02 us                                                | 3.00 us: 1.01x faster                                                   |
| sympy_str                | 346 ms                                                 | 344 ms: 1.01x faster                                                    |
| genshi_text              | 31.8 ms                                                | 32.0 ms: 1.00x slower                                                   |
| regex_compile            | 188 ms                                                 | 190 ms: 1.01x slower                                                    |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                    |
| pickle_list              | 5.08 us                                                | 5.13 us: 1.01x slower                                                   |
| regex_effbot             | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                   |
| sympy_expand             | 566 ms                                                 | 578 ms: 1.02x slower                                                    |
| pidigits                 | 191 ms                                                 | 196 ms: 1.03x slower                                                    |
| nqueens                  | 106 ms                                                 | 109 ms: 1.03x slower                                                    |
| meteor_contest           | 120 ms                                                 | 123 ms: 1.03x slower                                                    |
| async_generators         | 444 ms                                                 | 471 ms: 1.06x slower                                                    |
| unpickle                 | 14.4 us                                                | 15.7 us: 1.09x slower                                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.79 ms: 1.10x slower                                                   |
| genshi_xml               | 66.0 ms                                                | 72.9 ms: 1.10x slower                                                   |
| pickle                   | 10.7 us                                                | 11.9 us: 1.11x slower                                                   |
| pickle_dict              | 29.6 us                                                | 34.0 us: 1.15x slower                                                   |
| coverage                 | 79.4 ms                                                | 92.7 ms: 1.17x slower                                                   |
| python_startup_no_site   | 5.93 ms                                                | 7.23 ms: 1.22x slower                                                   |
| telco                    | 7.27 ms                                                | 9.60 ms: 1.32x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.16x faster                                                            |

Benchmark hidden because not significant (4): gc_traversal, regex_dna, bench_mp_pool, unpickle_list
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: docutils, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240503-3.13.0a6+-62ff43c-PYTHON_UOPS/bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.11x
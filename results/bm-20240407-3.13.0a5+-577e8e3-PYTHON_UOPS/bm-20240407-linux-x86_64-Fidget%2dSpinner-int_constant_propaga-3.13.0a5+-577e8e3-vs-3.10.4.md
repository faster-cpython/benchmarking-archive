# Results vs. 3.10.4

- fork: Fidget-Spinner
- ref: int_constant_propaga
- machine: linux-x86_64
- commit hash: 577e8e3
- commit date: 2024-04-07
- overall geometric mean: 1.15x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 320 ms: 1.09x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.95 ms: 1.22x faster                                                            |
| docutils       | 3.30 sec                                               | 3.18 sec: 1.04x faster                                                           |
| html5lib       | 88.9 ms                                                | 74.9 ms: 1.19x faster                                                            |
| tornado_http   | 136 ms                                                 | 104 ms: 1.31x faster                                                             |
| Geometric mean | (ref)                                                  | 1.16x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 385 ms: 1.89x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 976 ms: 1.81x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 515 ms: 1.69x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 648 ms: 1.57x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.74x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 96.6 ms: 1.21x faster                                                            |
| nbody          | 154 ms                                                 | 134 ms: 1.14x faster                                                             |
| pidigits       | 191 ms                                                 | 202 ms: 1.06x slower                                                             |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 26.9 ms: 1.03x faster                                                            |
| regex_effbot   | 3.63 ms                                                | 3.78 ms: 1.04x slower                                                            |
| regex_compile  | 188 ms                                                 | 208 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                     |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 318 us: 1.53x faster                                                             |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 66.2 ms: 1.20x faster                                                            |
| tomli_loads          | 3.14 sec                                               | 2.72 sec: 1.15x faster                                                           |
| json_loads           | 31.2 us                                                | 28.5 us: 1.10x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 163 ms: 1.03x faster                                                             |
| xml_etree_generate   | 99.4 ms                                                | 98.1 ms: 1.01x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 115 ms: 1.01x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 333 us: 1.01x slower                                                             |
| pickle               | 10.7 us                                                | 12.0 us: 1.12x slower                                                            |
| unpickle             | 14.4 us                                                | 16.7 us: 1.16x slower                                                            |
| pickle_dict          | 29.6 us                                                | 34.8 us: 1.18x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.05x faster                                                                     |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.7 ms: 1.37x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 9.09 ms: 1.53x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 31.8 ms                                                | 26.1 ms: 1.22x faster                                                            |
| mako           | 16.3 ms                                                | 14.3 ms: 1.14x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 62.9 ms: 1.05x faster                                                            |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 127 us: 4.29x faster                                                             |
| generators               | 80.1 ms                                                | 30.3 ms: 2.65x faster                                                            |
| async_tree_none          | 728 ms                                                 | 385 ms: 1.89x faster                                                             |
| deltablue                | 7.91 ms                                                | 4.28 ms: 1.85x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 976 ms: 1.81x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 518 ms: 1.78x faster                                                             |
| pylint                   | 551 ms                                                 | 312 ms: 1.76x faster                                                             |
| logging_silent           | 190 ns                                                 | 112 ns: 1.69x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 515 ms: 1.69x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 648 ms: 1.57x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 318 us: 1.53x faster                                                             |
| raytrace                 | 507 ms                                                 | 350 ms: 1.45x faster                                                             |
| coroutines               | 35.1 ms                                                | 24.3 ms: 1.44x faster                                                            |
| chaos                    | 115 ms                                                 | 82.2 ms: 1.40x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.56 ms: 1.39x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                           |
| scimark_sor              | 220 ms                                                 | 160 ms: 1.37x faster                                                             |
| python_startup           | 14.6 ms                                                | 10.7 ms: 1.37x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.90 ms: 1.35x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 96.7 ms: 1.32x faster                                                            |
| richards_super           | 94.7 ms                                                | 72.2 ms: 1.31x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                            |
| tornado_http             | 136 ms                                                 | 104 ms: 1.31x faster                                                             |
| thrift                   | 1.07 ms                                                | 843 us: 1.27x faster                                                             |
| logging_simple           | 8.30 us                                                | 6.61 us: 1.26x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.34 us: 1.25x faster                                                            |
| logging_format           | 9.09 us                                                | 7.32 us: 1.24x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 47.8 us: 1.22x faster                                                            |
| richards                 | 79.3 ms                                                | 64.8 ms: 1.22x faster                                                            |
| genshi_text              | 31.8 ms                                                | 26.1 ms: 1.22x faster                                                            |
| chameleon                | 9.68 ms                                                | 7.95 ms: 1.22x faster                                                            |
| deepcopy                 | 479 us                                                 | 394 us: 1.22x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 97.3 ms: 1.22x faster                                                            |
| go                       | 240 ms                                                 | 198 ms: 1.21x faster                                                             |
| float                    | 117 ms                                                 | 96.6 ms: 1.21x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 66.2 ms: 1.20x faster                                                            |
| html5lib                 | 88.9 ms                                                | 74.9 ms: 1.19x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.72 sec: 1.15x faster                                                           |
| nbody                    | 154 ms                                                 | 134 ms: 1.14x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.26 ms: 1.14x faster                                                            |
| mako                     | 16.3 ms                                                | 14.3 ms: 1.14x faster                                                            |
| comprehensions           | 28.8 us                                                | 25.3 us: 1.14x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.39 sec: 1.14x faster                                                           |
| dask                     | 441 ms                                                 | 388 ms: 1.14x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.35 ms: 1.13x faster                                                            |
| pyflate                  | 716 ms                                                 | 641 ms: 1.12x faster                                                             |
| spectral_norm            | 170 ms                                                 | 153 ms: 1.11x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 76.5 ms: 1.10x faster                                                            |
| json_loads               | 31.2 us                                                | 28.5 us: 1.10x faster                                                            |
| 2to3                     | 348 ms                                                 | 320 ms: 1.09x faster                                                             |
| mypy2                    | 894 ms                                                 | 827 ms: 1.08x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 917 us: 1.08x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 133 ms: 1.07x faster                                                             |
| sympy_sum                | 196 ms                                                 | 183 ms: 1.07x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 24.5 ms: 1.05x faster                                                            |
| json                     | 5.69 ms                                                | 5.41 ms: 1.05x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 62.9 ms: 1.05x faster                                                            |
| docutils                 | 3.30 sec                                               | 3.18 sec: 1.04x faster                                                           |
| regex_v8                 | 27.8 ms                                                | 26.9 ms: 1.03x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 163 ms: 1.03x faster                                                             |
| sympy_str                | 346 ms                                                 | 337 ms: 1.03x faster                                                             |
| sympy_expand             | 566 ms                                                 | 556 ms: 1.02x faster                                                             |
| fannkuch                 | 532 ms                                                 | 524 ms: 1.01x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.38 ms: 1.01x faster                                                            |
| xml_etree_generate       | 99.4 ms                                                | 98.1 ms: 1.01x faster                                                            |
| pickle_list              | 5.08 us                                                | 5.02 us: 1.01x faster                                                            |
| xml_etree_iterparse      | 115 ms                                                 | 115 ms: 1.01x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 68.8 ms: 1.00x faster                                                            |
| pathlib                  | 20.5 ms                                                | 20.6 ms: 1.01x slower                                                            |
| unpickle_pure_python     | 331 us                                                 | 333 us: 1.01x slower                                                             |
| scimark_fft              | 466 ms                                                 | 470 ms: 1.01x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                             |
| scimark_lu               | 176 ms                                                 | 178 ms: 1.01x slower                                                             |
| mdp                      | 2.85 sec                                               | 2.94 sec: 1.03x slower                                                           |
| sqlite_synth             | 3.02 us                                                | 3.15 us: 1.04x slower                                                            |
| regex_effbot             | 3.63 ms                                                | 3.78 ms: 1.04x slower                                                            |
| pidigits                 | 191 ms                                                 | 202 ms: 1.06x slower                                                             |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                            |
| async_generators         | 444 ms                                                 | 486 ms: 1.10x slower                                                             |
| regex_compile            | 188 ms                                                 | 208 ms: 1.10x slower                                                             |
| gc_traversal             | 3.62 ms                                                | 4.03 ms: 1.11x slower                                                            |
| pickle                   | 10.7 us                                                | 12.0 us: 1.12x slower                                                            |
| meteor_contest           | 120 ms                                                 | 134 ms: 1.12x slower                                                             |
| pprint_pformat           | 2.10 sec                                               | 2.40 sec: 1.14x slower                                                           |
| pprint_safe_repr         | 1.02 sec                                               | 1.18 sec: 1.16x slower                                                           |
| unpickle                 | 14.4 us                                                | 16.7 us: 1.16x slower                                                            |
| pickle_dict              | 29.6 us                                                | 34.8 us: 1.18x slower                                                            |
| coverage                 | 79.4 ms                                                | 98.1 ms: 1.24x slower                                                            |
| nqueens                  | 106 ms                                                 | 139 ms: 1.32x slower                                                             |
| telco                    | 7.27 ms                                                | 9.89 ms: 1.36x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 9.09 ms: 1.53x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.15x faster                                                                     |

Benchmark hidden because not significant (4): regex_dna, hexiom, bench_mp_pool, unpickle_list
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240407-3.13.0a5+-577e8e3-PYTHON_UOPS/bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x
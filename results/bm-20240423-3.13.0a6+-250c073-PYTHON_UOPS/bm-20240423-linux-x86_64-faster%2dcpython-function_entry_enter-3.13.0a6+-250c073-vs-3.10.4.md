# Results vs. 3.10.4

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 250c073
- commit date: 2024-04-23
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 303 ms: 1.15x faster                                                             |
| chameleon      | 9.68 ms                                                | 8.01 ms: 1.21x faster                                                            |
| docutils       | 3.30 sec                                               | 3.09 sec: 1.07x faster                                                           |
| html5lib       | 88.9 ms                                                | 71.8 ms: 1.24x faster                                                            |
| tornado_http   | 136 ms                                                 | 103 ms: 1.32x faster                                                             |
| Geometric mean | (ref)                                                  | 1.19x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 375 ms: 1.94x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 966 ms: 1.83x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 502 ms: 1.73x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 638 ms: 1.59x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.77x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 91.1 ms: 1.29x faster                                                            |
| nbody          | 154 ms                                                 | 123 ms: 1.25x faster                                                             |
| pidigits       | 191 ms                                                 | 212 ms: 1.11x slower                                                             |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.1 ms: 1.11x faster                                                            |
| regex_compile  | 188 ms                                                 | 182 ms: 1.04x faster                                                             |
| regex_dna      | 227 ms                                                 | 224 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 318 us: 1.52x faster                                                             |
| json_dumps           | 14.2 ms                                                | 10.9 ms: 1.30x faster                                                            |
| tomli_loads          | 3.14 sec                                               | 2.53 sec: 1.24x faster                                                           |
| xml_etree_process    | 79.1 ms                                                | 64.0 ms: 1.24x faster                                                            |
| unpickle_pure_python | 331 us                                                 | 286 us: 1.15x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 151 ms: 1.11x faster                                                             |
| json_loads           | 31.2 us                                                | 28.2 us: 1.10x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 92.9 ms: 1.07x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 112 ms: 1.03x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                                            |
| unpickle_list        | 5.20 us                                                | 5.41 us: 1.04x slower                                                            |
| unpickle             | 14.4 us                                                | 15.7 us: 1.09x slower                                                            |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.5 us: 1.20x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.18 ms: 1.21x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                | 25.2 ms: 1.26x faster                                                            |
| mako            | 16.3 ms                                                | 13.7 ms: 1.19x faster                                                            |
| django_template | 48.2 ms                                                | 40.9 ms: 1.18x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 59.0 ms: 1.12x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.19x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 123 us: 4.42x faster                                                             |
| generators               | 80.1 ms                                                | 30.2 ms: 2.65x faster                                                            |
| async_tree_none          | 728 ms                                                 | 375 ms: 1.94x faster                                                             |
| deltablue                | 7.91 ms                                                | 4.21 ms: 1.88x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 966 ms: 1.83x faster                                                             |
| logging_silent           | 190 ns                                                 | 104 ns: 1.83x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 528 ms: 1.75x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 502 ms: 1.73x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 638 ms: 1.59x faster                                                             |
| pylint                   | 551 ms                                                 | 349 ms: 1.58x faster                                                             |
| raytrace                 | 507 ms                                                 | 322 ms: 1.57x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 318 us: 1.52x faster                                                             |
| richards_super           | 94.7 ms                                                | 62.3 ms: 1.52x faster                                                            |
| chaos                    | 115 ms                                                 | 78.9 ms: 1.46x faster                                                            |
| coroutines               | 35.1 ms                                                | 24.0 ms: 1.46x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.50 ms: 1.45x faster                                                            |
| richards                 | 79.3 ms                                                | 55.6 ms: 1.43x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.82 ms: 1.42x faster                                                            |
| scimark_sor              | 220 ms                                                 | 157 ms: 1.40x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 92.5 ms: 1.38x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.37x faster                                                           |
| tornado_http             | 136 ms                                                 | 103 ms: 1.32x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 44.6 us: 1.31x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 90.5 ms: 1.31x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.9 ms: 1.30x faster                                                            |
| logging_simple           | 8.30 us                                                | 6.40 us: 1.30x faster                                                            |
| thrift                   | 1.07 ms                                                | 827 us: 1.30x faster                                                             |
| float                    | 117 ms                                                 | 91.1 ms: 1.29x faster                                                            |
| genshi_text              | 31.8 ms                                                | 25.2 ms: 1.26x faster                                                            |
| deepcopy                 | 479 us                                                 | 381 us: 1.26x faster                                                             |
| logging_format           | 9.09 us                                                | 7.28 us: 1.25x faster                                                            |
| nbody                    | 154 ms                                                 | 123 ms: 1.25x faster                                                             |
| go                       | 240 ms                                                 | 193 ms: 1.24x faster                                                             |
| tomli_loads              | 3.14 sec                                               | 2.53 sec: 1.24x faster                                                           |
| deepcopy_reduce          | 4.17 us                                                | 3.36 us: 1.24x faster                                                            |
| comprehensions           | 28.8 us                                                | 23.2 us: 1.24x faster                                                            |
| html5lib                 | 88.9 ms                                                | 71.8 ms: 1.24x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.27 sec: 1.24x faster                                                           |
| xml_etree_process        | 79.1 ms                                                | 64.0 ms: 1.24x faster                                                            |
| chameleon                | 9.68 ms                                                | 8.01 ms: 1.21x faster                                                            |
| pyflate                  | 716 ms                                                 | 595 ms: 1.20x faster                                                             |
| spectral_norm            | 170 ms                                                 | 142 ms: 1.19x faster                                                             |
| mako                     | 16.3 ms                                                | 13.7 ms: 1.19x faster                                                            |
| djangocms                | 38.4 us                                                | 32.5 us: 1.18x faster                                                            |
| django_template          | 48.2 ms                                                | 40.9 ms: 1.18x faster                                                            |
| aiohttp                  | 1.44 ms                                                | 1.23 ms: 1.17x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 286 us: 1.15x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.33 ms: 1.15x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 73.2 ms: 1.15x faster                                                            |
| 2to3                     | 348 ms                                                 | 303 ms: 1.15x faster                                                             |
| dask                     | 441 ms                                                 | 385 ms: 1.14x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 125 ms: 1.14x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 880 us: 1.12x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 59.0 ms: 1.12x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 151 ms: 1.11x faster                                                             |
| pathlib                  | 20.5 ms                                                | 18.4 ms: 1.11x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 25.1 ms: 1.11x faster                                                            |
| json_loads               | 31.2 us                                                | 28.2 us: 1.10x faster                                                            |
| sympy_sum                | 196 ms                                                 | 178 ms: 1.10x faster                                                             |
| mypy2                    | 894 ms                                                 | 818 ms: 1.09x faster                                                             |
| hexiom                   | 10.4 ms                                                | 9.53 ms: 1.09x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 63.5 ms: 1.09x faster                                                            |
| sympy_integrate          | 25.8 ms                                                | 23.9 ms: 1.08x faster                                                            |
| json                     | 5.69 ms                                                | 5.30 ms: 1.07x faster                                                            |
| xml_etree_generate       | 99.4 ms                                                | 92.9 ms: 1.07x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 952 ms: 1.07x faster                                                             |
| fannkuch                 | 532 ms                                                 | 498 ms: 1.07x faster                                                             |
| pprint_pformat           | 2.10 sec                                               | 1.97 sec: 1.07x faster                                                           |
| docutils                 | 3.30 sec                                               | 3.09 sec: 1.07x faster                                                           |
| sympy_str                | 346 ms                                                 | 326 ms: 1.06x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.12 ms: 1.06x faster                                                            |
| scimark_lu               | 176 ms                                                 | 168 ms: 1.05x faster                                                             |
| regex_compile            | 188 ms                                                 | 182 ms: 1.04x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 112 ms: 1.03x faster                                                             |
| sympy_expand             | 566 ms                                                 | 550 ms: 1.03x faster                                                             |
| mdp                      | 2.85 sec                                               | 2.78 sec: 1.02x faster                                                           |
| scimark_fft              | 466 ms                                                 | 460 ms: 1.01x faster                                                             |
| sqlite_synth             | 3.02 us                                                | 2.99 us: 1.01x faster                                                            |
| regex_dna                | 227 ms                                                 | 224 ms: 1.01x faster                                                             |
| pickle_list              | 5.08 us                                                | 5.12 us: 1.01x slower                                                            |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.02x slower                                                             |
| nqueens                  | 106 ms                                                 | 108 ms: 1.02x slower                                                             |
| meteor_contest           | 120 ms                                                 | 122 ms: 1.02x slower                                                             |
| unpickle_list            | 5.20 us                                                | 5.41 us: 1.04x slower                                                            |
| async_generators         | 444 ms                                                 | 475 ms: 1.07x slower                                                             |
| unpickle                 | 14.4 us                                                | 15.7 us: 1.09x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.96 ms: 1.09x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.78 ms: 1.10x slower                                                            |
| pidigits                 | 191 ms                                                 | 212 ms: 1.11x slower                                                             |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.5 us: 1.20x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.18 ms: 1.21x slower                                                            |
| coverage                 | 79.4 ms                                                | 97.3 ms: 1.22x slower                                                            |
| telco                    | 7.27 ms                                                | 9.30 ms: 1.28x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.20x faster                                                                     |

Benchmark hidden because not significant (2): bench_mp_pool, regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240423-3.13.0a6+-250c073-PYTHON_UOPS/bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.11x
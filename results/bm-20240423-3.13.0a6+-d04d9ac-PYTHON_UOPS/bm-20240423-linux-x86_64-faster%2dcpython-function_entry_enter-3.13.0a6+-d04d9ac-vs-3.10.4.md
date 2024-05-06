# Results vs. 3.10.4

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: d04d9ac
- commit date: 2024-04-23
- overall geometric mean: 1.19x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 306 ms: 1.14x faster                                                             |
| chameleon      | 9.68 ms                                                | 8.10 ms: 1.20x faster                                                            |
| docutils       | 3.30 sec                                               | 3.13 sec: 1.05x faster                                                           |
| html5lib       | 88.9 ms                                                | 73.3 ms: 1.21x faster                                                            |
| tornado_http   | 136 ms                                                 | 103 ms: 1.32x faster                                                             |
| Geometric mean | (ref)                                                  | 1.18x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 380 ms: 1.92x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 975 ms: 1.81x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 508 ms: 1.71x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 638 ms: 1.59x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.75x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 94.9 ms: 1.23x faster                                                            |
| nbody          | 154 ms                                                 | 128 ms: 1.20x faster                                                             |
| pidigits       | 191 ms                                                 | 199 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                            |
| regex_compile  | 188 ms                                                 | 186 ms: 1.01x faster                                                             |
| regex_dna      | 227 ms                                                 | 227 ms: 1.00x slower                                                             |
| regex_effbot   | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 321 us: 1.51x faster                                                             |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 65.6 ms: 1.21x faster                                                            |
| tomli_loads          | 3.14 sec                                               | 2.62 sec: 1.20x faster                                                           |
| json_loads           | 31.2 us                                                | 27.8 us: 1.12x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 150 ms: 1.12x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 298 us: 1.11x faster                                                             |
| xml_etree_generate   | 99.4 ms                                                | 95.3 ms: 1.04x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 114 ms: 1.01x faster                                                             |
| unpickle_list        | 5.20 us                                                | 5.35 us: 1.03x slower                                                            |
| unpickle             | 14.4 us                                                | 15.3 us: 1.06x slower                                                            |
| pickle               | 10.7 us                                                | 11.9 us: 1.11x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.5 us: 1.20x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                                     |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.14 ms: 1.20x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                | 25.7 ms: 1.24x faster                                                            |
| django_template | 48.2 ms                                                | 41.5 ms: 1.16x faster                                                            |
| mako            | 16.3 ms                                                | 14.5 ms: 1.12x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 59.9 ms: 1.10x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.16x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 128 us: 4.27x faster                                                             |
| generators               | 80.1 ms                                                | 30.3 ms: 2.64x faster                                                            |
| async_tree_none          | 728 ms                                                 | 380 ms: 1.92x faster                                                             |
| deltablue                | 7.91 ms                                                | 4.33 ms: 1.83x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 975 ms: 1.81x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 528 ms: 1.75x faster                                                             |
| logging_silent           | 190 ns                                                 | 110 ns: 1.73x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 508 ms: 1.71x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 638 ms: 1.59x faster                                                             |
| pylint                   | 551 ms                                                 | 351 ms: 1.57x faster                                                             |
| raytrace                 | 507 ms                                                 | 330 ms: 1.54x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 321 us: 1.51x faster                                                             |
| richards_super           | 94.7 ms                                                | 63.7 ms: 1.49x faster                                                            |
| coroutines               | 35.1 ms                                                | 24.2 ms: 1.45x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.50 ms: 1.44x faster                                                            |
| chaos                    | 115 ms                                                 | 80.9 ms: 1.43x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.82 ms: 1.42x faster                                                            |
| richards                 | 79.3 ms                                                | 57.3 ms: 1.38x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.88 sec: 1.37x faster                                                           |
| scimark_sor              | 220 ms                                                 | 161 ms: 1.36x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 95.3 ms: 1.34x faster                                                            |
| tornado_http             | 136 ms                                                 | 103 ms: 1.32x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.31x faster                                                            |
| logging_simple           | 8.30 us                                                | 6.43 us: 1.29x faster                                                            |
| thrift                   | 1.07 ms                                                | 841 us: 1.27x faster                                                             |
| logging_format           | 9.09 us                                                | 7.16 us: 1.27x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 46.1 us: 1.27x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 93.9 ms: 1.26x faster                                                            |
| deepcopy                 | 479 us                                                 | 384 us: 1.25x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.35 us: 1.25x faster                                                            |
| genshi_text              | 31.8 ms                                                | 25.7 ms: 1.24x faster                                                            |
| float                    | 117 ms                                                 | 94.9 ms: 1.23x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.29 sec: 1.22x faster                                                           |
| html5lib                 | 88.9 ms                                                | 73.3 ms: 1.21x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 65.6 ms: 1.21x faster                                                            |
| nbody                    | 154 ms                                                 | 128 ms: 1.20x faster                                                             |
| tomli_loads              | 3.14 sec                                               | 2.62 sec: 1.20x faster                                                           |
| chameleon                | 9.68 ms                                                | 8.10 ms: 1.20x faster                                                            |
| go                       | 240 ms                                                 | 201 ms: 1.19x faster                                                             |
| comprehensions           | 28.8 us                                                | 24.6 us: 1.17x faster                                                            |
| aiohttp                  | 1.44 ms                                                | 1.23 ms: 1.17x faster                                                            |
| djangocms                | 38.4 us                                                | 33.0 us: 1.16x faster                                                            |
| django_template          | 48.2 ms                                                | 41.5 ms: 1.16x faster                                                            |
| gunicorn                 | 1.53 ms                                                | 1.32 ms: 1.16x faster                                                            |
| dask                     | 441 ms                                                 | 384 ms: 1.15x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 73.9 ms: 1.14x faster                                                            |
| 2to3                     | 348 ms                                                 | 306 ms: 1.14x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 126 ms: 1.13x faster                                                             |
| json_loads               | 31.2 us                                                | 27.8 us: 1.12x faster                                                            |
| mako                     | 16.3 ms                                                | 14.5 ms: 1.12x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 150 ms: 1.12x faster                                                             |
| pyflate                  | 716 ms                                                 | 639 ms: 1.12x faster                                                             |
| pathlib                  | 20.5 ms                                                | 18.4 ms: 1.11x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 298 us: 1.11x faster                                                             |
| spectral_norm            | 170 ms                                                 | 153 ms: 1.11x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 892 us: 1.11x faster                                                             |
| sympy_sum                | 196 ms                                                 | 178 ms: 1.10x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 59.9 ms: 1.10x faster                                                            |
| json                     | 5.69 ms                                                | 5.20 ms: 1.09x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                            |
| mypy2                    | 894 ms                                                 | 821 ms: 1.09x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 64.5 ms: 1.07x faster                                                            |
| sympy_integrate          | 25.8 ms                                                | 24.1 ms: 1.07x faster                                                            |
| docutils                 | 3.30 sec                                               | 3.13 sec: 1.05x faster                                                           |
| sympy_str                | 346 ms                                                 | 330 ms: 1.05x faster                                                             |
| xml_etree_generate       | 99.4 ms                                                | 95.3 ms: 1.04x faster                                                            |
| fannkuch                 | 532 ms                                                 | 511 ms: 1.04x faster                                                             |
| pprint_safe_repr         | 1.02 sec                                               | 983 ms: 1.04x faster                                                             |
| scimark_lu               | 176 ms                                                 | 170 ms: 1.03x faster                                                             |
| hexiom                   | 10.4 ms                                                | 10.1 ms: 1.03x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 2.04 sec: 1.03x faster                                                           |
| sympy_expand             | 566 ms                                                 | 552 ms: 1.02x faster                                                             |
| regex_compile            | 188 ms                                                 | 186 ms: 1.01x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 114 ms: 1.01x faster                                                             |
| regex_dna                | 227 ms                                                 | 227 ms: 1.00x slower                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.54 ms: 1.01x slower                                                            |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                             |
| scimark_fft              | 466 ms                                                 | 473 ms: 1.01x slower                                                             |
| regex_effbot             | 3.63 ms                                                | 3.69 ms: 1.02x slower                                                            |
| meteor_contest           | 120 ms                                                 | 122 ms: 1.02x slower                                                             |
| unpickle_list            | 5.20 us                                                | 5.35 us: 1.03x slower                                                            |
| pidigits                 | 191 ms                                                 | 199 ms: 1.04x slower                                                             |
| nqueens                  | 106 ms                                                 | 111 ms: 1.05x slower                                                             |
| mdp                      | 2.85 sec                                               | 3.02 sec: 1.06x slower                                                           |
| unpickle                 | 14.4 us                                                | 15.3 us: 1.06x slower                                                            |
| async_generators         | 444 ms                                                 | 482 ms: 1.09x slower                                                             |
| gc_traversal             | 3.62 ms                                                | 3.96 ms: 1.09x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.79 ms: 1.11x slower                                                            |
| pickle                   | 10.7 us                                                | 11.9 us: 1.11x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.5 us: 1.20x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.14 ms: 1.20x slower                                                            |
| coverage                 | 79.4 ms                                                | 97.4 ms: 1.23x slower                                                            |
| telco                    | 7.27 ms                                                | 9.36 ms: 1.29x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.19x faster                                                                     |

Benchmark hidden because not significant (3): sqlite_synth, pickle_list, bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240423-3.13.0a6+-d04d9ac-PYTHON_UOPS/bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.11x
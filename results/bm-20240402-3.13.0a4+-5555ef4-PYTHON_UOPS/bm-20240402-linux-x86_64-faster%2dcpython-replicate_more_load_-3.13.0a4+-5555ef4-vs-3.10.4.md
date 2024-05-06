# Results vs. 3.10.4

- fork: faster-cpython
- ref: replicate_more_load_
- machine: linux-x86_64
- commit hash: 5555ef4
- commit date: 2024-04-02
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 300 ms: 1.16x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.08 ms: 1.37x faster                                                            |
| docutils       | 3.30 sec                                               | 2.87 sec: 1.15x faster                                                           |
| html5lib       | 88.9 ms                                                | 71.1 ms: 1.25x faster                                                            |
| tornado_http   | 136 ms                                                 | 103 ms: 1.32x faster                                                             |
| Geometric mean | (ref)                                                  | 1.25x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 463 ms: 1.57x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 594 ms: 1.46x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 1.24 sec: 1.42x faster                                                           |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 747 ms: 1.36x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.45x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 123 ms: 1.25x faster                                                             |
| float          | 117 ms                                                 | 94.7 ms: 1.24x faster                                                            |
| Geometric mean | (ref)                                                  | 1.16x faster                                                                     |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.1 ms: 1.11x faster                                                            |
| regex_dna      | 227 ms                                                 | 213 ms: 1.06x faster                                                             |
| regex_compile  | 188 ms                                                 | 178 ms: 1.06x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.55 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                  | 1.06x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 314 us: 1.54x faster                                                             |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 62.8 ms: 1.26x faster                                                            |
| tomli_loads          | 3.14 sec                                               | 2.53 sec: 1.24x faster                                                           |
| unpickle_pure_python | 331 us                                                 | 278 us: 1.19x faster                                                             |
| json_loads           | 31.2 us                                                | 28.4 us: 1.10x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 91.6 ms: 1.09x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 161 ms: 1.04x faster                                                             |
| xml_etree_iterparse  | 115 ms                                                 | 113 ms: 1.03x faster                                                             |
| unpickle_list        | 5.20 us                                                | 5.12 us: 1.02x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.25 us: 1.03x slower                                                            |
| unpickle             | 14.4 us                                                | 15.4 us: 1.07x slower                                                            |
| pickle               | 10.7 us                                                | 12.0 us: 1.12x slower                                                            |
| pickle_dict          | 29.6 us                                                | 34.9 us: 1.18x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 9.07 ms: 1.53x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 48.2 ms                                                | 34.5 ms: 1.40x faster                                                            |
| mako            | 16.3 ms                                                | 12.9 ms: 1.27x faster                                                            |
| genshi_text     | 31.8 ms                                                | 28.0 ms: 1.14x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 64.9 ms: 1.02x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.20x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 118 us: 4.61x faster                                                             |
| generators               | 80.1 ms                                                | 30.4 ms: 2.64x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.88 ms: 2.04x faster                                                            |
| logging_silent           | 190 ns                                                 | 104 ns: 1.82x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 510 ms: 1.81x faster                                                             |
| pylint                   | 551 ms                                                 | 333 ms: 1.66x faster                                                             |
| async_tree_none          | 728 ms                                                 | 463 ms: 1.57x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 314 us: 1.54x faster                                                             |
| chaos                    | 115 ms                                                 | 75.2 ms: 1.54x faster                                                            |
| richards_super           | 94.7 ms                                                | 63.0 ms: 1.50x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 85.4 ms: 1.50x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.47 ms: 1.48x faster                                                            |
| raytrace                 | 507 ms                                                 | 346 ms: 1.47x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 594 ms: 1.46x faster                                                             |
| coroutines               | 35.1 ms                                                | 24.0 ms: 1.46x faster                                                            |
| scimark_sor              | 220 ms                                                 | 154 ms: 1.43x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 1.24 sec: 1.42x faster                                                           |
| sqlglot_transpile        | 2.57 ms                                                | 1.81 ms: 1.42x faster                                                            |
| richards                 | 79.3 ms                                                | 56.3 ms: 1.41x faster                                                            |
| django_template          | 48.2 ms                                                | 34.5 ms: 1.40x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 42.2 us: 1.39x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                           |
| scimark_monte_carlo      | 118 ms                                                 | 85.9 ms: 1.38x faster                                                            |
| comprehensions           | 28.8 us                                                | 20.9 us: 1.37x faster                                                            |
| chameleon                | 9.68 ms                                                | 7.08 ms: 1.37x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 747 ms: 1.36x faster                                                             |
| go                       | 240 ms                                                 | 179 ms: 1.34x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.11 us: 1.34x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| tornado_http             | 136 ms                                                 | 103 ms: 1.32x faster                                                             |
| deepcopy                 | 479 us                                                 | 367 us: 1.31x faster                                                             |
| logging_simple           | 8.30 us                                                | 6.37 us: 1.30x faster                                                            |
| thrift                   | 1.07 ms                                                | 834 us: 1.28x faster                                                             |
| mako                     | 16.3 ms                                                | 12.9 ms: 1.27x faster                                                            |
| logging_format           | 9.09 us                                                | 7.19 us: 1.26x faster                                                            |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.26x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 62.8 ms: 1.26x faster                                                            |
| html5lib                 | 88.9 ms                                                | 71.1 ms: 1.25x faster                                                            |
| nbody                    | 154 ms                                                 | 123 ms: 1.25x faster                                                             |
| tomli_loads              | 3.14 sec                                               | 2.53 sec: 1.24x faster                                                           |
| float                    | 117 ms                                                 | 94.7 ms: 1.24x faster                                                            |
| spectral_norm            | 170 ms                                                 | 140 ms: 1.22x faster                                                             |
| pyflate                  | 716 ms                                                 | 593 ms: 1.21x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 21.5 ms: 1.20x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 278 us: 1.19x faster                                                             |
| djangocms                | 38.4 us                                                | 32.4 us: 1.18x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.33 sec: 1.18x faster                                                           |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                            |
| sympy_sum                | 196 ms                                                 | 166 ms: 1.18x faster                                                             |
| pprint_safe_repr         | 1.02 sec                                               | 866 ms: 1.18x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                                            |
| dask                     | 441 ms                                                 | 379 ms: 1.16x faster                                                             |
| 2to3                     | 348 ms                                                 | 300 ms: 1.16x faster                                                             |
| pprint_pformat           | 2.10 sec                                               | 1.82 sec: 1.16x faster                                                           |
| docutils                 | 3.30 sec                                               | 2.87 sec: 1.15x faster                                                           |
| hexiom                   | 10.4 ms                                                | 9.07 ms: 1.15x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 73.7 ms: 1.14x faster                                                            |
| genshi_text              | 31.8 ms                                                | 28.0 ms: 1.14x faster                                                            |
| sympy_str                | 346 ms                                                 | 306 ms: 1.13x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 61.2 ms: 1.13x faster                                                            |
| bench_thread_pool        | 986 us                                                 | 873 us: 1.13x faster                                                             |
| fannkuch                 | 532 ms                                                 | 480 ms: 1.11x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 25.1 ms: 1.11x faster                                                            |
| json_loads               | 31.2 us                                                | 28.4 us: 1.10x faster                                                            |
| sympy_expand             | 566 ms                                                 | 514 ms: 1.10x faster                                                             |
| scimark_lu               | 176 ms                                                 | 160 ms: 1.10x faster                                                             |
| xml_etree_generate       | 99.4 ms                                                | 91.6 ms: 1.09x faster                                                            |
| unpack_sequence          | 60.0 ns                                                | 56.1 ns: 1.07x faster                                                            |
| regex_dna                | 227 ms                                                 | 213 ms: 1.06x faster                                                             |
| json                     | 5.69 ms                                                | 5.35 ms: 1.06x faster                                                            |
| pathlib                  | 20.5 ms                                                | 19.3 ms: 1.06x faster                                                            |
| regex_compile            | 188 ms                                                 | 178 ms: 1.06x faster                                                             |
| create_gc_cycles         | 1.62 ms                                                | 1.55 ms: 1.05x faster                                                            |
| nqueens                  | 106 ms                                                 | 101 ms: 1.04x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.20 ms: 1.04x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 161 ms: 1.04x faster                                                             |
| mdp                      | 2.85 sec                                               | 2.75 sec: 1.04x faster                                                           |
| scimark_fft              | 466 ms                                                 | 450 ms: 1.04x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 113 ms: 1.03x faster                                                             |
| sqlite_synth             | 3.02 us                                                | 2.95 us: 1.03x faster                                                            |
| regex_effbot             | 3.63 ms                                                | 3.55 ms: 1.02x faster                                                            |
| meteor_contest           | 120 ms                                                 | 117 ms: 1.02x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 64.9 ms: 1.02x faster                                                            |
| unpickle_list            | 5.20 us                                                | 5.12 us: 1.02x faster                                                            |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                            |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                             |
| pickle_list              | 5.08 us                                                | 5.25 us: 1.03x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.85 ms: 1.06x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.4 us: 1.07x slower                                                            |
| async_generators         | 444 ms                                                 | 480 ms: 1.08x slower                                                             |
| pickle                   | 10.7 us                                                | 12.0 us: 1.12x slower                                                            |
| pickle_dict              | 29.6 us                                                | 34.9 us: 1.18x slower                                                            |
| telco                    | 7.27 ms                                                | 8.85 ms: 1.22x slower                                                            |
| coverage                 | 79.4 ms                                                | 97.8 ms: 1.23x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 9.07 ms: 1.53x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.22x faster                                                                     |

Benchmark hidden because not significant (2): pidigits, mypy2
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240402-3.13.0a4+-5555ef4-PYTHON_UOPS/bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.08x
# Results vs. 3.10.4

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 0bbd7af
- commit date: 2024-04-08
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 269 ms: 1.29x faster                                                             |
| chameleon      | 9.68 ms                                                | 6.83 ms: 1.42x faster                                                            |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                           |
| html5lib       | 88.9 ms                                                | 67.7 ms: 1.31x faster                                                            |
| tornado_http   | 136 ms                                                 | 94.5 ms: 1.44x faster                                                            |
| Geometric mean | (ref)                                                  | 1.32x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 350 ms: 2.08x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 922 ms: 1.92x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 457 ms: 1.90x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 606 ms: 1.68x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.89x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 87.9 ms: 1.75x faster                                                            |
| float          | 117 ms                                                 | 77.6 ms: 1.51x faster                                                            |
| pidigits       | 191 ms                                                 | 197 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                  | 1.37x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.41x faster                                                             |
| regex_v8       | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                            |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                     |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 298 us: 1.62x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 220 us: 1.50x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.12 sec: 1.48x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 60.9 ms: 1.30x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| json_loads           | 31.2 us                                                | 28.8 us: 1.08x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| unpickle_list        | 5.20 us                                                | 5.01 us: 1.04x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.19 us: 1.02x slower                                                            |
| unpickle             | 14.4 us                                                | 15.1 us: 1.05x slower                                                            |
| pickle               | 10.7 us                                                | 12.1 us: 1.13x slower                                                            |
| pickle_dict          | 29.6 us                                                | 36.4 us: 1.23x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 8.95 ms: 1.51x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                            |
| genshi_text    | 31.8 ms                                                | 23.6 ms: 1.35x faster                                                            |
| genshi_xml     | 66.0 ms                                                | 51.5 ms: 1.28x faster                                                            |
| Geometric mean | (ref)                                                  | 1.38x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 112 us: 4.86x faster                                                             |
| generators               | 80.1 ms                                                | 29.7 ms: 2.70x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.19 ms: 2.48x faster                                                            |
| async_tree_none          | 728 ms                                                 | 350 ms: 2.08x faster                                                             |
| pylint                   | 551 ms                                                 | 279 ms: 1.97x faster                                                             |
| raytrace                 | 507 ms                                                 | 259 ms: 1.95x faster                                                             |
| chaos                    | 115 ms                                                 | 59.9 ms: 1.93x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 922 ms: 1.92x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 457 ms: 1.90x faster                                                             |
| logging_silent           | 190 ns                                                 | 101 ns: 1.89x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 505 ms: 1.83x faster                                                             |
| richards_super           | 94.7 ms                                                | 53.1 ms: 1.78x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 66.4 ms: 1.78x faster                                                            |
| scimark_sor              | 220 ms                                                 | 124 ms: 1.78x faster                                                             |
| nbody                    | 154 ms                                                 | 87.9 ms: 1.75x faster                                                            |
| comprehensions           | 28.8 us                                                | 16.7 us: 1.72x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 74.6 ms: 1.71x faster                                                            |
| go                       | 240 ms                                                 | 141 ms: 1.70x faster                                                             |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                            |
| richards                 | 79.3 ms                                                | 47.1 ms: 1.68x faster                                                            |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 606 ms: 1.68x faster                                                             |
| hexiom                   | 10.4 ms                                                | 6.23 ms: 1.67x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 298 us: 1.62x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 36.4 us: 1.61x faster                                                            |
| coroutines               | 35.1 ms                                                | 22.1 ms: 1.58x faster                                                            |
| spectral_norm            | 170 ms                                                 | 109 ms: 1.56x faster                                                             |
| pyflate                  | 716 ms                                                 | 467 ms: 1.53x faster                                                             |
| scimark_lu               | 176 ms                                                 | 115 ms: 1.53x faster                                                             |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                            |
| float                    | 117 ms                                                 | 77.6 ms: 1.51x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 220 us: 1.50x faster                                                             |
| tomli_loads              | 3.14 sec                                               | 2.12 sec: 1.48x faster                                                           |
| logging_simple           | 8.30 us                                                | 5.66 us: 1.47x faster                                                            |
| tornado_http             | 136 ms                                                 | 94.5 ms: 1.44x faster                                                            |
| logging_format           | 9.09 us                                                | 6.31 us: 1.44x faster                                                            |
| chameleon                | 9.68 ms                                                | 6.83 ms: 1.42x faster                                                            |
| regex_compile            | 188 ms                                                 | 134 ms: 1.41x faster                                                             |
| pprint_pformat           | 2.10 sec                                               | 1.50 sec: 1.40x faster                                                           |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| pprint_safe_repr         | 1.02 sec                                               | 732 ms: 1.39x faster                                                             |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| fannkuch                 | 532 ms                                                 | 383 ms: 1.39x faster                                                             |
| deepcopy                 | 479 us                                                 | 350 us: 1.37x faster                                                             |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                                           |
| genshi_text              | 31.8 ms                                                | 23.6 ms: 1.35x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| thrift                   | 1.07 ms                                                | 807 us: 1.33x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.16 us: 1.32x faster                                                            |
| html5lib                 | 88.9 ms                                                | 67.7 ms: 1.31x faster                                                            |
| nqueens                  | 106 ms                                                 | 80.6 ms: 1.31x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 60.9 ms: 1.30x faster                                                            |
| 2to3                     | 348 ms                                                 | 269 ms: 1.29x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 51.5 ms: 1.28x faster                                                            |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.27x faster                                                            |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                                             |
| scimark_fft              | 466 ms                                                 | 371 ms: 1.26x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 67.3 ms: 1.25x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 55.3 ms: 1.25x faster                                                            |
| sympy_str                | 346 ms                                                 | 278 ms: 1.24x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.22 ms: 1.24x faster                                                            |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| sympy_expand             | 566 ms                                                 | 468 ms: 1.21x faster                                                             |
| mypy2                    | 894 ms                                                 | 740 ms: 1.21x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                            |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 834 us: 1.18x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                           |
| xml_etree_generate       | 99.4 ms                                                | 88.0 ms: 1.13x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.5 ms: 1.10x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.59 sec: 1.10x faster                                                           |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| json_loads               | 31.2 us                                                | 28.8 us: 1.08x faster                                                            |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                             |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                             |
| json                     | 5.69 ms                                                | 5.43 ms: 1.05x faster                                                            |
| sqlite_synth             | 3.02 us                                                | 2.92 us: 1.04x faster                                                            |
| unpickle_list            | 5.20 us                                                | 5.01 us: 1.04x faster                                                            |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                                             |
| pickle_list              | 5.08 us                                                | 5.19 us: 1.02x slower                                                            |
| pidigits                 | 191 ms                                                 | 197 ms: 1.03x slower                                                             |
| gc_traversal             | 3.62 ms                                                | 3.75 ms: 1.04x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.1 us: 1.05x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.72 ms: 1.06x slower                                                            |
| pickle                   | 10.7 us                                                | 12.1 us: 1.13x slower                                                            |
| telco                    | 7.27 ms                                                | 8.80 ms: 1.21x slower                                                            |
| coverage                 | 79.4 ms                                                | 96.3 ms: 1.21x slower                                                            |
| pickle_dict              | 29.6 us                                                | 36.4 us: 1.23x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 8.95 ms: 1.51x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                                     |

Benchmark hidden because not significant (4): bench_mp_pool, async_generators, regex_dna, regex_effbot
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-0bbd7af/bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x
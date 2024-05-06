# Results vs. 3.10.4

- fork: faster-cpython
- ref: call_cmethod
- machine: linux-x86_64
- commit hash: 5c20c52
- commit date: 2024-04-10
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 271 ms: 1.29x faster                                                     |
| chameleon      | 9.68 ms                                                | 7.03 ms: 1.38x faster                                                    |
| docutils       | 3.30 sec                                               | 2.84 sec: 1.16x faster                                                   |
| html5lib       | 88.9 ms                                                | 67.8 ms: 1.31x faster                                                    |
| tornado_http   | 136 ms                                                 | 94.8 ms: 1.44x faster                                                    |
| Geometric mean | (ref)                                                  | 1.31x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 346 ms: 2.10x faster                                                     |
| async_tree_io           | 1.77 sec                                               | 920 ms: 1.92x faster                                                     |
| async_tree_memoization  | 870 ms                                                 | 459 ms: 1.90x faster                                                     |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 606 ms: 1.68x faster                                                     |
| Geometric mean          | (ref)                                                  | 1.89x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.5 ms: 1.74x faster                                                    |
| float          | 117 ms                                                 | 78.7 ms: 1.49x faster                                                    |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                  | 1.37x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.39x faster                                                     |
| regex_v8       | 27.8 ms                                                | 24.2 ms: 1.15x faster                                                    |
| regex_dna      | 227 ms                                                 | 218 ms: 1.04x faster                                                     |
| regex_effbot   | 3.63 ms                                                | 3.70 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                  | 1.13x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 302 us: 1.60x faster                                                     |
| unpickle_pure_python | 331 us                                                 | 222 us: 1.49x faster                                                     |
| tomli_loads          | 3.14 sec                                               | 2.15 sec: 1.46x faster                                                   |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                    |
| xml_etree_process    | 79.1 ms                                                | 61.1 ms: 1.29x faster                                                    |
| xml_etree_generate   | 99.4 ms                                                | 88.3 ms: 1.13x faster                                                    |
| json_loads           | 31.2 us                                                | 28.4 us: 1.10x faster                                                    |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                     |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                     |
| unpickle             | 14.4 us                                                | 15.1 us: 1.05x slower                                                    |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                    |
| pickle_dict          | 29.6 us                                                | 34.9 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                             |

Benchmark hidden because not significant (2): pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                    |
| python_startup_no_site | 5.93 ms                                                | 8.95 ms: 1.51x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                    |
| genshi_text    | 31.8 ms                                                | 23.9 ms: 1.33x faster                                                    |
| genshi_xml     | 66.0 ms                                                | 52.9 ms: 1.25x faster                                                    |
| Geometric mean | (ref)                                                  | 1.36x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 117 us: 4.66x faster                                                     |
| generators               | 80.1 ms                                                | 29.7 ms: 2.70x faster                                                    |
| deltablue                | 7.91 ms                                                | 3.19 ms: 2.48x faster                                                    |
| async_tree_none          | 728 ms                                                 | 346 ms: 2.10x faster                                                     |
| pylint                   | 551 ms                                                 | 279 ms: 1.98x faster                                                     |
| raytrace                 | 507 ms                                                 | 262 ms: 1.94x faster                                                     |
| async_tree_io            | 1.77 sec                                               | 920 ms: 1.92x faster                                                     |
| chaos                    | 115 ms                                                 | 60.6 ms: 1.90x faster                                                    |
| async_tree_memoization   | 870 ms                                                 | 459 ms: 1.90x faster                                                     |
| logging_silent           | 190 ns                                                 | 101 ns: 1.88x faster                                                     |
| asyncio_tcp              | 922 ms                                                 | 498 ms: 1.85x faster                                                     |
| richards_super           | 94.7 ms                                                | 52.9 ms: 1.79x faster                                                    |
| scimark_sor              | 220 ms                                                 | 123 ms: 1.78x faster                                                     |
| scimark_monte_carlo      | 118 ms                                                 | 67.4 ms: 1.75x faster                                                    |
| nbody                    | 154 ms                                                 | 88.5 ms: 1.74x faster                                                    |
| comprehensions           | 28.8 us                                                | 16.6 us: 1.73x faster                                                    |
| go                       | 240 ms                                                 | 140 ms: 1.72x faster                                                     |
| richards                 | 79.3 ms                                                | 47.0 ms: 1.69x faster                                                    |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.69x faster                                                    |
| hexiom                   | 10.4 ms                                                | 6.18 ms: 1.68x faster                                                    |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 606 ms: 1.68x faster                                                     |
| crypto_pyaes             | 128 ms                                                 | 76.6 ms: 1.67x faster                                                    |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                                    |
| pickle_pure_python       | 484 us                                                 | 302 us: 1.60x faster                                                     |
| scimark_lu               | 176 ms                                                 | 113 ms: 1.57x faster                                                     |
| coroutines               | 35.1 ms                                                | 22.5 ms: 1.56x faster                                                    |
| deepcopy_memo            | 58.5 us                                                | 38.5 us: 1.52x faster                                                    |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                    |
| pyflate                  | 716 ms                                                 | 476 ms: 1.50x faster                                                     |
| float                    | 117 ms                                                 | 78.7 ms: 1.49x faster                                                    |
| unpickle_pure_python     | 331 us                                                 | 222 us: 1.49x faster                                                     |
| spectral_norm            | 170 ms                                                 | 116 ms: 1.46x faster                                                     |
| tomli_loads              | 3.14 sec                                               | 2.15 sec: 1.46x faster                                                   |
| tornado_http             | 136 ms                                                 | 94.8 ms: 1.44x faster                                                    |
| logging_format           | 9.09 us                                                | 6.39 us: 1.42x faster                                                    |
| logging_simple           | 8.30 us                                                | 5.85 us: 1.42x faster                                                    |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                   |
| regex_compile            | 188 ms                                                 | 135 ms: 1.39x faster                                                     |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                    |
| chameleon                | 9.68 ms                                                | 7.03 ms: 1.38x faster                                                    |
| pycparser                | 1.58 sec                                               | 1.15 sec: 1.37x faster                                                   |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.37x faster                                                   |
| fannkuch                 | 532 ms                                                 | 389 ms: 1.37x faster                                                     |
| pprint_safe_repr         | 1.02 sec                                               | 749 ms: 1.36x faster                                                     |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                    |
| deepcopy                 | 479 us                                                 | 359 us: 1.34x faster                                                     |
| genshi_text              | 31.8 ms                                                | 23.9 ms: 1.33x faster                                                    |
| thrift                   | 1.07 ms                                                | 815 us: 1.32x faster                                                     |
| html5lib                 | 88.9 ms                                                | 67.8 ms: 1.31x faster                                                    |
| deepcopy_reduce          | 4.17 us                                                | 3.19 us: 1.31x faster                                                    |
| nqueens                  | 106 ms                                                 | 80.9 ms: 1.31x faster                                                    |
| xml_etree_process        | 79.1 ms                                                | 61.1 ms: 1.29x faster                                                    |
| scimark_fft              | 466 ms                                                 | 360 ms: 1.29x faster                                                     |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                     |
| 2to3                     | 348 ms                                                 | 271 ms: 1.29x faster                                                     |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.26x faster                                                    |
| dulwich_log              | 84.3 ms                                                | 66.9 ms: 1.26x faster                                                    |
| sqlglot_optimize         | 69.2 ms                                                | 55.2 ms: 1.25x faster                                                    |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.25x faster                                                     |
| genshi_xml               | 66.0 ms                                                | 52.9 ms: 1.25x faster                                                    |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                     |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                    |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.30 ms: 1.22x faster                                                    |
| mypy2                    | 894 ms                                                 | 738 ms: 1.21x faster                                                     |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                    |
| sympy_expand             | 566 ms                                                 | 473 ms: 1.20x faster                                                     |
| dask                     | 441 ms                                                 | 369 ms: 1.19x faster                                                     |
| bench_thread_pool        | 986 us                                                 | 833 us: 1.18x faster                                                     |
| docutils                 | 3.30 sec                                               | 2.84 sec: 1.16x faster                                                   |
| regex_v8                 | 27.8 ms                                                | 24.2 ms: 1.15x faster                                                    |
| xml_etree_generate       | 99.4 ms                                                | 88.3 ms: 1.13x faster                                                    |
| json_loads               | 31.2 us                                                | 28.4 us: 1.10x faster                                                    |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                     |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                     |
| pathlib                  | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                    |
| json                     | 5.69 ms                                                | 5.36 ms: 1.06x faster                                                    |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                     |
| regex_dna                | 227 ms                                                 | 218 ms: 1.04x faster                                                     |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                    |
| mdp                      | 2.85 sec                                               | 2.77 sec: 1.03x faster                                                   |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                                     |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                    |
| async_generators         | 444 ms                                                 | 445 ms: 1.00x slower                                                     |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                     |
| regex_effbot             | 3.63 ms                                                | 3.70 ms: 1.02x slower                                                    |
| gc_traversal             | 3.62 ms                                                | 3.79 ms: 1.05x slower                                                    |
| unpickle                 | 14.4 us                                                | 15.1 us: 1.05x slower                                                    |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                    |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                    |
| pickle_dict              | 29.6 us                                                | 34.9 us: 1.18x slower                                                    |
| telco                    | 7.27 ms                                                | 8.70 ms: 1.20x slower                                                    |
| coverage                 | 79.4 ms                                                | 96.8 ms: 1.22x slower                                                    |
| python_startup_no_site   | 5.93 ms                                                | 8.95 ms: 1.51x slower                                                    |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                             |

Benchmark hidden because not significant (2): pickle_list, unpickle_list
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240410-3.13.0a5+-5c20c52/bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.09x
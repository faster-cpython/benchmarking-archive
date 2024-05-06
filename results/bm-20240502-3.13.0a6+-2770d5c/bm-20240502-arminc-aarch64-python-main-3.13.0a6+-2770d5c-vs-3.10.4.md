# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-aarch64
- commit hash: 2770d5c
- commit date: 2024-05-02
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 381 ms                                                                | 298 ms: 1.28x faster                                     |
| chameleon      | 10.8 ms                                                               | 9.06 ms: 1.20x faster                                    |
| docutils       | 3.53 sec                                                              | 3.06 sec: 1.15x faster                                   |
| html5lib       | 86.5 ms                                                               | 65.6 ms: 1.32x faster                                    |
| tornado_http   | 178 ms                                                                | 126 ms: 1.42x faster                                     |
| Geometric mean | (ref)                                                                 | 1.27x faster                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|-------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_none         | 950 ms                                                                | 486 ms: 1.95x faster                                     |
| async_tree_io           | 2.28 sec                                                              | 1.22 sec: 1.88x faster                                   |
| async_tree_memoization  | 1.13 sec                                                              | 642 ms: 1.77x faster                                     |
| async_tree_cpu_io_mixed | 1.27 sec                                                              | 783 ms: 1.63x faster                                     |
| Geometric mean          | (ref)                                                                 | 1.80x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| nbody          | 166 ms                                                                | 106 ms: 1.57x faster                                     |
| float          | 135 ms                                                                | 88.7 ms: 1.52x faster                                    |
| pidigits       | 235 ms                                                                | 233 ms: 1.01x faster                                     |
| Geometric mean | (ref)                                                                 | 1.34x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_compile  | 177 ms                                                                | 127 ms: 1.39x faster                                     |
| regex_dna      | 257 ms                                                                | 248 ms: 1.04x faster                                     |
| regex_v8       | 32.2 ms                                                               | 31.2 ms: 1.03x faster                                    |
| regex_effbot   | 4.25 ms                                                               | 4.86 ms: 1.14x slower                                    |
| Geometric mean | (ref)                                                                 | 1.07x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| pickle_pure_python   | 529 us                                                                | 350 us: 1.51x faster                                     |
| unpickle_pure_python | 366 us                                                                | 248 us: 1.47x faster                                     |
| tomli_loads          | 3.36 sec                                                              | 2.49 sec: 1.35x faster                                   |
| json_dumps           | 16.7 ms                                                               | 12.8 ms: 1.30x faster                                    |
| xml_etree_process    | 99.5 ms                                                               | 79.4 ms: 1.25x faster                                    |
| xml_etree_parse      | 212 ms                                                                | 186 ms: 1.14x faster                                     |
| unpickle_list        | 6.99 us                                                               | 6.25 us: 1.12x faster                                    |
| xml_etree_generate   | 123 ms                                                                | 111 ms: 1.11x faster                                     |
| xml_etree_iterparse  | 156 ms                                                                | 146 ms: 1.07x faster                                     |
| pickle_list          | 5.24 us                                                               | 5.29 us: 1.01x slower                                    |
| json_loads           | 30.9 us                                                               | 31.9 us: 1.03x slower                                    |
| pickle               | 12.5 us                                                               | 13.3 us: 1.07x slower                                    |
| pickle_dict          | 35.1 us                                                               | 37.9 us: 1.08x slower                                    |
| unpickle             | 17.5 us                                                               | 19.6 us: 1.12x slower                                    |
| Geometric mean       | (ref)                                                                 | 1.13x faster                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 11.2 ms                                                               | 12.1 ms: 1.08x slower                                    |
| python_startup_no_site | 6.89 ms                                                               | 8.29 ms: 1.20x slower                                    |
| Geometric mean         | (ref)                                                                 | 1.14x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 18.9 ms                                                               | 13.1 ms: 1.44x faster                                    |
| django_template | 53.3 ms                                                               | 40.5 ms: 1.32x faster                                    |
| genshi_text     | 35.2 ms                                                               | 27.3 ms: 1.29x faster                                    |
| genshi_xml      | 69.8 ms                                                               | 59.8 ms: 1.17x faster                                    |
| Geometric mean  | (ref)                                                                 | 1.30x faster                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|--------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| typing_runtime_protocols | 661 us                                                                | 191 us: 3.47x faster                                     |
| deltablue                | 8.94 ms                                                               | 3.80 ms: 2.35x faster                                    |
| bench_mp_pool            | 14.5 ms                                                               | 6.95 ms: 2.09x faster                                    |
| raytrace                 | 573 ms                                                                | 291 ms: 1.97x faster                                     |
| async_tree_none          | 950 ms                                                                | 486 ms: 1.95x faster                                     |
| async_tree_io            | 2.28 sec                                                              | 1.22 sec: 1.88x faster                                   |
| generators               | 68.1 ms                                                               | 37.2 ms: 1.83x faster                                    |
| chaos                    | 121 ms                                                                | 66.5 ms: 1.82x faster                                    |
| richards_super           | 107 ms                                                                | 59.4 ms: 1.81x faster                                    |
| asyncio_tcp              | 944 ms                                                                | 530 ms: 1.78x faster                                     |
| async_tree_memoization   | 1.13 sec                                                              | 642 ms: 1.77x faster                                     |
| sqlglot_parse            | 2.40 ms                                                               | 1.37 ms: 1.76x faster                                    |
| richards                 | 91.7 ms                                                               | 52.8 ms: 1.74x faster                                    |
| logging_silent           | 222 ns                                                                | 131 ns: 1.69x faster                                     |
| sqlglot_transpile        | 2.84 ms                                                               | 1.68 ms: 1.69x faster                                    |
| scimark_lu               | 227 ms                                                                | 134 ms: 1.69x faster                                     |
| go                       | 264 ms                                                                | 159 ms: 1.66x faster                                     |
| comprehensions           | 33.1 us                                                               | 19.9 us: 1.66x faster                                    |
| crypto_pyaes             | 134 ms                                                                | 82.2 ms: 1.63x faster                                    |
| async_tree_cpu_io_mixed  | 1.27 sec                                                              | 783 ms: 1.63x faster                                     |
| scimark_sor              | 246 ms                                                                | 155 ms: 1.59x faster                                     |
| scimark_monte_carlo      | 128 ms                                                                | 80.6 ms: 1.59x faster                                    |
| nbody                    | 166 ms                                                                | 106 ms: 1.57x faster                                     |
| hexiom                   | 10.9 ms                                                               | 7.01 ms: 1.56x faster                                    |
| asyncio_tcp_ssl          | 3.28 sec                                                              | 2.12 sec: 1.54x faster                                   |
| float                    | 135 ms                                                                | 88.7 ms: 1.52x faster                                    |
| pickle_pure_python       | 529 us                                                                | 350 us: 1.51x faster                                     |
| unpickle_pure_python     | 366 us                                                                | 248 us: 1.47x faster                                     |
| pylint                   | 485 ms                                                                | 336 ms: 1.45x faster                                     |
| mako                     | 18.9 ms                                                               | 13.1 ms: 1.44x faster                                    |
| pyflate                  | 795 ms                                                                | 555 ms: 1.43x faster                                     |
| tornado_http             | 178 ms                                                                | 126 ms: 1.42x faster                                     |
| logging_simple           | 9.78 us                                                               | 6.97 us: 1.40x faster                                    |
| logging_format           | 10.6 us                                                               | 7.56 us: 1.40x faster                                    |
| pycparser                | 1.69 sec                                                              | 1.21 sec: 1.40x faster                                   |
| regex_compile            | 177 ms                                                                | 127 ms: 1.39x faster                                     |
| tomli_loads              | 3.36 sec                                                              | 2.49 sec: 1.35x faster                                   |
| thrift                   | 1.26 ms                                                               | 936 us: 1.35x faster                                     |
| spectral_norm            | 186 ms                                                                | 139 ms: 1.35x faster                                     |
| html5lib                 | 86.5 ms                                                               | 65.6 ms: 1.32x faster                                    |
| django_template          | 53.3 ms                                                               | 40.5 ms: 1.32x faster                                    |
| json_dumps               | 16.7 ms                                                               | 12.8 ms: 1.30x faster                                    |
| dulwich_log              | 73.5 ms                                                               | 56.7 ms: 1.30x faster                                    |
| coroutines               | 37.2 ms                                                               | 28.7 ms: 1.30x faster                                    |
| genshi_text              | 35.2 ms                                                               | 27.3 ms: 1.29x faster                                    |
| sympy_sum                | 184 ms                                                                | 144 ms: 1.28x faster                                     |
| sympy_integrate          | 26.5 ms                                                               | 20.8 ms: 1.28x faster                                    |
| 2to3                     | 381 ms                                                                | 298 ms: 1.28x faster                                     |
| deepcopy_memo            | 61.7 us                                                               | 48.6 us: 1.27x faster                                    |
| bench_thread_pool        | 1.59 ms                                                               | 1.26 ms: 1.27x faster                                    |
| xml_etree_process        | 99.5 ms                                                               | 79.4 ms: 1.25x faster                                    |
| sqlglot_normalize        | 156 ms                                                                | 125 ms: 1.25x faster                                     |
| pprint_pformat           | 2.36 sec                                                              | 1.89 sec: 1.25x faster                                   |
| sympy_str                | 329 ms                                                                | 264 ms: 1.25x faster                                     |
| pprint_safe_repr         | 1.15 sec                                                              | 923 ms: 1.24x faster                                     |
| sqlglot_optimize         | 75.4 ms                                                               | 61.0 ms: 1.24x faster                                    |
| nqueens                  | 117 ms                                                                | 95.7 ms: 1.23x faster                                    |
| dask                     | 450 ms                                                                | 372 ms: 1.21x faster                                     |
| fannkuch                 | 546 ms                                                                | 453 ms: 1.20x faster                                     |
| sympy_expand             | 543 ms                                                                | 451 ms: 1.20x faster                                     |
| chameleon                | 10.8 ms                                                               | 9.06 ms: 1.20x faster                                    |
| scimark_sparse_mat_mult  | 7.62 ms                                                               | 6.47 ms: 1.18x faster                                    |
| genshi_xml               | 69.8 ms                                                               | 59.8 ms: 1.17x faster                                    |
| deepcopy                 | 511 us                                                                | 442 us: 1.16x faster                                     |
| pathlib                  | 26.3 ms                                                               | 22.8 ms: 1.15x faster                                    |
| docutils                 | 3.53 sec                                                              | 3.06 sec: 1.15x faster                                   |
| deepcopy_reduce          | 4.60 us                                                               | 4.00 us: 1.15x faster                                    |
| scimark_fft              | 500 ms                                                                | 438 ms: 1.14x faster                                     |
| xml_etree_parse          | 212 ms                                                                | 186 ms: 1.14x faster                                     |
| mdp                      | 3.70 sec                                                              | 3.29 sec: 1.13x faster                                   |
| unpickle_list            | 6.99 us                                                               | 6.25 us: 1.12x faster                                    |
| meteor_contest           | 126 ms                                                                | 113 ms: 1.11x faster                                     |
| xml_etree_generate       | 123 ms                                                                | 111 ms: 1.11x faster                                     |
| sqlite_synth             | 4.12 us                                                               | 3.78 us: 1.09x faster                                    |
| xml_etree_iterparse      | 156 ms                                                                | 146 ms: 1.07x faster                                     |
| json                     | 5.88 ms                                                               | 5.59 ms: 1.05x faster                                    |
| regex_dna                | 257 ms                                                                | 248 ms: 1.04x faster                                     |
| regex_v8                 | 32.2 ms                                                               | 31.2 ms: 1.03x faster                                    |
| pidigits                 | 235 ms                                                                | 233 ms: 1.01x faster                                     |
| pickle_list              | 5.24 us                                                               | 5.29 us: 1.01x slower                                    |
| create_gc_cycles         | 2.26 ms                                                               | 2.31 ms: 1.02x slower                                    |
| json_loads               | 30.9 us                                                               | 31.9 us: 1.03x slower                                    |
| async_generators         | 452 ms                                                                | 476 ms: 1.05x slower                                     |
| pickle                   | 12.5 us                                                               | 13.3 us: 1.07x slower                                    |
| pickle_dict              | 35.1 us                                                               | 37.9 us: 1.08x slower                                    |
| python_startup           | 11.2 ms                                                               | 12.1 ms: 1.08x slower                                    |
| telco                    | 8.49 ms                                                               | 9.38 ms: 1.10x slower                                    |
| unpickle                 | 17.5 us                                                               | 19.6 us: 1.12x slower                                    |
| regex_effbot             | 4.25 ms                                                               | 4.86 ms: 1.14x slower                                    |
| coverage                 | 83.6 ms                                                               | 98.4 ms: 1.18x slower                                    |
| python_startup_no_site   | 6.89 ms                                                               | 8.29 ms: 1.20x slower                                    |
| gc_traversal             | 4.15 ms                                                               | 5.10 ms: 1.23x slower                                    |
| Geometric mean           | (ref)                                                                 | 1.31x faster                                             |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240502-3.13.0a6+-2770d5c/bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.23x

# Memory
- memory change: 1.11x
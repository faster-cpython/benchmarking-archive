# Results vs. 3.10.4

- fork: python
- ref: deaf509e8fc6e0363bd6
- machine: linux-aarch64
- commit hash: deaf509
- commit date: 2022-10-24
- overall geometric mean: 1.23x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 381 ms                                                                | 300 ms: 1.27x faster                                                  |
| chameleon      | 10.8 ms                                                               | 8.29 ms: 1.31x faster                                                 |
| docutils       | 3.53 sec                                                              | 2.92 sec: 1.21x faster                                                |
| html5lib       | 86.5 ms                                                               | 65.3 ms: 1.32x faster                                                 |
| tornado_http   | 178 ms                                                                | 140 ms: 1.28x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.28x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|-------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io           | 2.28 sec                                                              | 1.61 sec: 1.42x faster                                                |
| async_tree_none         | 950 ms                                                                | 701 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed | 1.27 sec                                                              | 955 ms: 1.33x faster                                                  |
| async_tree_memoization  | 1.13 sec                                                              | 872 ms: 1.30x faster                                                  |
| Geometric mean          | (ref)                                                                 | 1.35x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 135 ms                                                                | 89.6 ms: 1.50x faster                                                 |
| nbody          | 166 ms                                                                | 113 ms: 1.47x faster                                                  |
| pidigits       | 235 ms                                                                | 242 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.29x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                | 137 ms: 1.29x faster                                                  |
| regex_v8       | 32.2 ms                                                               | 29.1 ms: 1.11x faster                                                 |
| regex_dna      | 257 ms                                                                | 239 ms: 1.08x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.11x faster                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 529 us                                                                | 374 us: 1.42x faster                                                  |
| unpickle_pure_python | 366 us                                                                | 278 us: 1.31x faster                                                  |
| xml_etree_process    | 99.5 ms                                                               | 76.1 ms: 1.31x faster                                                 |
| tomli_loads          | 3.36 sec                                                              | 2.62 sec: 1.28x faster                                                |
| xml_etree_generate   | 123 ms                                                                | 104 ms: 1.18x faster                                                  |
| json_dumps           | 16.7 ms                                                               | 15.4 ms: 1.08x faster                                                 |
| pickle_list          | 5.24 us                                                               | 5.01 us: 1.04x faster                                                 |
| unpickle             | 17.5 us                                                               | 16.9 us: 1.04x faster                                                 |
| xml_etree_iterparse  | 156 ms                                                                | 152 ms: 1.03x faster                                                  |
| json_loads           | 30.9 us                                                               | 30.3 us: 1.02x faster                                                 |
| unpickle_list        | 6.99 us                                                               | 6.86 us: 1.02x faster                                                 |
| xml_etree_parse      | 212 ms                                                                | 209 ms: 1.01x faster                                                  |
| pickle               | 12.5 us                                                               | 12.8 us: 1.03x slower                                                 |
| pickle_dict          | 35.1 us                                                               | 37.6 us: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.11x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.2 ms                                                               | 10.2 ms: 1.10x faster                                                 |
| python_startup_no_site | 6.89 ms                                                               | 7.35 ms: 1.07x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 18.9 ms                                                               | 13.3 ms: 1.43x faster                                                 |
| django_template | 53.3 ms                                                               | 41.8 ms: 1.28x faster                                                 |
| genshi_text     | 35.2 ms                                                               | 28.2 ms: 1.25x faster                                                 |
| genshi_xml      | 69.8 ms                                                               | 62.2 ms: 1.12x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.26x faster                                                          |

All benchmarks:
===============

| Benchmark                | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|--------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| bench_mp_pool            | 14.5 ms                                                               | 7.44 ms: 1.95x faster                                                 |
| deltablue                | 8.94 ms                                                               | 4.75 ms: 1.88x faster                                                 |
| scimark_sor              | 246 ms                                                                | 145 ms: 1.69x faster                                                  |
| logging_silent           | 222 ns                                                                | 133 ns: 1.68x faster                                                  |
| raytrace                 | 573 ms                                                                | 351 ms: 1.64x faster                                                  |
| go                       | 264 ms                                                                | 163 ms: 1.62x faster                                                  |
| scimark_lu               | 227 ms                                                                | 140 ms: 1.62x faster                                                  |
| richards                 | 91.7 ms                                                               | 58.1 ms: 1.58x faster                                                 |
| crypto_pyaes             | 134 ms                                                                | 86.5 ms: 1.55x faster                                                 |
| pyflate                  | 795 ms                                                                | 516 ms: 1.54x faster                                                  |
| scimark_monte_carlo      | 128 ms                                                                | 83.2 ms: 1.54x faster                                                 |
| chaos                    | 121 ms                                                                | 78.8 ms: 1.54x faster                                                 |
| richards_super           | 107 ms                                                                | 70.2 ms: 1.53x faster                                                 |
| float                    | 135 ms                                                                | 89.6 ms: 1.50x faster                                                 |
| nbody                    | 166 ms                                                                | 113 ms: 1.47x faster                                                  |
| sqlglot_parse            | 2.40 ms                                                               | 1.65 ms: 1.46x faster                                                 |
| hexiom                   | 10.9 ms                                                               | 7.57 ms: 1.44x faster                                                 |
| mako                     | 18.9 ms                                                               | 13.3 ms: 1.43x faster                                                 |
| async_tree_io            | 2.28 sec                                                              | 1.61 sec: 1.42x faster                                                |
| spectral_norm            | 186 ms                                                                | 131 ms: 1.42x faster                                                  |
| sqlglot_transpile        | 2.84 ms                                                               | 2.00 ms: 1.42x faster                                                 |
| pickle_pure_python       | 529 us                                                                | 374 us: 1.42x faster                                                  |
| thrift                   | 1.26 ms                                                               | 910 us: 1.38x faster                                                  |
| pycparser                | 1.69 sec                                                              | 1.25 sec: 1.36x faster                                                |
| async_tree_none          | 950 ms                                                                | 701 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed  | 1.27 sec                                                              | 955 ms: 1.33x faster                                                  |
| html5lib                 | 86.5 ms                                                               | 65.3 ms: 1.32x faster                                                 |
| unpickle_pure_python     | 366 us                                                                | 278 us: 1.31x faster                                                  |
| xml_etree_process        | 99.5 ms                                                               | 76.1 ms: 1.31x faster                                                 |
| chameleon                | 10.8 ms                                                               | 8.29 ms: 1.31x faster                                                 |
| async_tree_memoization   | 1.13 sec                                                              | 872 ms: 1.30x faster                                                  |
| logging_simple           | 9.78 us                                                               | 7.57 us: 1.29x faster                                                 |
| regex_compile            | 177 ms                                                                | 137 ms: 1.29x faster                                                  |
| logging_format           | 10.6 us                                                               | 8.22 us: 1.29x faster                                                 |
| tomli_loads              | 3.36 sec                                                              | 2.62 sec: 1.28x faster                                                |
| tornado_http             | 178 ms                                                                | 140 ms: 1.28x faster                                                  |
| django_template          | 53.3 ms                                                               | 41.8 ms: 1.28x faster                                                 |
| pprint_pformat           | 2.36 sec                                                              | 1.85 sec: 1.27x faster                                                |
| pprint_safe_repr         | 1.15 sec                                                              | 903 ms: 1.27x faster                                                  |
| mypy2                    | 936 ms                                                                | 737 ms: 1.27x faster                                                  |
| 2to3                     | 381 ms                                                                | 300 ms: 1.27x faster                                                  |
| sqlalchemy_declarative   | 197 ms                                                                | 157 ms: 1.26x faster                                                  |
| deepcopy_memo            | 61.7 us                                                               | 49.0 us: 1.26x faster                                                 |
| sqlalchemy_imperative    | 20.5 ms                                                               | 16.4 ms: 1.25x faster                                                 |
| genshi_text              | 35.2 ms                                                               | 28.2 ms: 1.25x faster                                                 |
| scimark_fft              | 500 ms                                                                | 402 ms: 1.24x faster                                                  |
| aiohttp                  | 1.39 ms                                                               | 1.13 ms: 1.23x faster                                                 |
| pylint                   | 485 ms                                                                | 397 ms: 1.22x faster                                                  |
| gunicorn                 | 1.45 ms                                                               | 1.19 ms: 1.22x faster                                                 |
| scimark_sparse_mat_mult  | 7.62 ms                                                               | 6.29 ms: 1.21x faster                                                 |
| fannkuch                 | 546 ms                                                                | 451 ms: 1.21x faster                                                  |
| docutils                 | 3.53 sec                                                              | 2.92 sec: 1.21x faster                                                |
| create_gc_cycles         | 2.26 ms                                                               | 1.87 ms: 1.21x faster                                                 |
| async_generators         | 452 ms                                                                | 378 ms: 1.20x faster                                                  |
| sqlglot_optimize         | 75.4 ms                                                               | 63.4 ms: 1.19x faster                                                 |
| deepcopy_reduce          | 4.60 us                                                               | 3.89 us: 1.18x faster                                                 |
| xml_etree_generate       | 123 ms                                                                | 104 ms: 1.18x faster                                                  |
| sqlglot_normalize        | 156 ms                                                                | 132 ms: 1.18x faster                                                  |
| bench_thread_pool        | 1.59 ms                                                               | 1.36 ms: 1.17x faster                                                 |
| deepcopy                 | 511 us                                                                | 435 us: 1.17x faster                                                  |
| dask                     | 450 ms                                                                | 385 ms: 1.17x faster                                                  |
| dulwich_log              | 73.5 ms                                                               | 63.2 ms: 1.16x faster                                                 |
| sqlite_synth             | 4.12 us                                                               | 3.56 us: 1.16x faster                                                 |
| flaskblogging            | 4.83 ms                                                               | 4.19 ms: 1.15x faster                                                 |
| nqueens                  | 117 ms                                                                | 102 ms: 1.15x faster                                                  |
| sympy_integrate          | 26.5 ms                                                               | 23.2 ms: 1.15x faster                                                 |
| comprehensions           | 33.1 us                                                               | 29.0 us: 1.14x faster                                                 |
| sympy_expand             | 543 ms                                                                | 482 ms: 1.13x faster                                                  |
| genshi_xml               | 69.8 ms                                                               | 62.2 ms: 1.12x faster                                                 |
| coroutines               | 37.2 ms                                                               | 33.3 ms: 1.12x faster                                                 |
| sympy_str                | 329 ms                                                                | 295 ms: 1.12x faster                                                  |
| regex_v8                 | 32.2 ms                                                               | 29.1 ms: 1.11x faster                                                 |
| mdp                      | 3.70 sec                                                              | 3.35 sec: 1.10x faster                                                |
| python_startup           | 11.2 ms                                                               | 10.2 ms: 1.10x faster                                                 |
| sympy_sum                | 184 ms                                                                | 168 ms: 1.09x faster                                                  |
| meteor_contest           | 126 ms                                                                | 115 ms: 1.09x faster                                                  |
| telco                    | 8.49 ms                                                               | 7.80 ms: 1.09x faster                                                 |
| json_dumps               | 16.7 ms                                                               | 15.4 ms: 1.08x faster                                                 |
| regex_dna                | 257 ms                                                                | 239 ms: 1.08x faster                                                  |
| json                     | 5.88 ms                                                               | 5.52 ms: 1.06x faster                                                 |
| pathlib                  | 26.3 ms                                                               | 24.8 ms: 1.06x faster                                                 |
| generators               | 68.1 ms                                                               | 64.2 ms: 1.06x faster                                                 |
| pickle_list              | 5.24 us                                                               | 5.01 us: 1.04x faster                                                 |
| unpickle                 | 17.5 us                                                               | 16.9 us: 1.04x faster                                                 |
| asyncio_tcp_ssl          | 3.28 sec                                                              | 3.19 sec: 1.03x faster                                                |
| xml_etree_iterparse      | 156 ms                                                                | 152 ms: 1.03x faster                                                  |
| asyncio_tcp              | 944 ms                                                                | 920 ms: 1.03x faster                                                  |
| json_loads               | 30.9 us                                                               | 30.3 us: 1.02x faster                                                 |
| unpickle_list            | 6.99 us                                                               | 6.86 us: 1.02x faster                                                 |
| xml_etree_parse          | 212 ms                                                                | 209 ms: 1.01x faster                                                  |
| typing_runtime_protocols | 661 us                                                                | 653 us: 1.01x faster                                                  |
| coverage                 | 83.6 ms                                                               | 84.1 ms: 1.01x slower                                                 |
| pickle                   | 12.5 us                                                               | 12.8 us: 1.03x slower                                                 |
| pidigits                 | 235 ms                                                                | 242 ms: 1.03x slower                                                  |
| gc_traversal             | 4.15 ms                                                               | 4.33 ms: 1.04x slower                                                 |
| python_startup_no_site   | 6.89 ms                                                               | 7.35 ms: 1.07x slower                                                 |
| pickle_dict              | 35.1 us                                                               | 37.6 us: 1.07x slower                                                 |
| Geometric mean           | (ref)                                                                 | 1.23x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, regex_effbot
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: 1.09x
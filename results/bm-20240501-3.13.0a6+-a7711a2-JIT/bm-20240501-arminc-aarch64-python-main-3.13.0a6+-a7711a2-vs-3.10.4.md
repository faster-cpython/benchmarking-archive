# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-aarch64
- commit hash: a7711a2
- commit date: 2024-05-01
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 381 ms                                                                | 348 ms: 1.09x faster                                     |
| chameleon      | 10.8 ms                                                               | 9.13 ms: 1.19x faster                                    |
| docutils       | 3.53 sec                                                              | 3.41 sec: 1.03x faster                                   |
| html5lib       | 86.5 ms                                                               | 70.3 ms: 1.23x faster                                    |
| tornado_http   | 178 ms                                                                | 139 ms: 1.29x faster                                     |
| Geometric mean | (ref)                                                                 | 1.16x faster                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|-------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_io           | 2.28 sec                                                              | 1.23 sec: 1.86x faster                                   |
| async_tree_none         | 950 ms                                                                | 511 ms: 1.86x faster                                     |
| async_tree_memoization  | 1.13 sec                                                              | 661 ms: 1.71x faster                                     |
| async_tree_cpu_io_mixed | 1.27 sec                                                              | 809 ms: 1.57x faster                                     |
| Geometric mean          | (ref)                                                                 | 1.75x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| nbody          | 166 ms                                                                | 108 ms: 1.54x faster                                     |
| float          | 135 ms                                                                | 90.3 ms: 1.49x faster                                    |
| pidigits       | 235 ms                                                                | 233 ms: 1.01x faster                                     |
| Geometric mean | (ref)                                                                 | 1.32x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_compile  | 177 ms                                                                | 159 ms: 1.11x faster                                     |
| regex_v8       | 32.2 ms                                                               | 30.3 ms: 1.06x faster                                    |
| regex_dna      | 257 ms                                                                | 246 ms: 1.04x faster                                     |
| regex_effbot   | 4.25 ms                                                               | 4.84 ms: 1.14x slower                                    |
| Geometric mean | (ref)                                                                 | 1.02x faster                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| pickle_pure_python   | 529 us                                                                | 356 us: 1.49x faster                                     |
| unpickle_pure_python | 366 us                                                                | 277 us: 1.32x faster                                     |
| tomli_loads          | 3.36 sec                                                              | 2.56 sec: 1.31x faster                                   |
| json_dumps           | 16.7 ms                                                               | 12.9 ms: 1.30x faster                                    |
| xml_etree_process    | 99.5 ms                                                               | 80.3 ms: 1.24x faster                                    |
| xml_etree_parse      | 212 ms                                                                | 186 ms: 1.14x faster                                     |
| xml_etree_generate   | 123 ms                                                                | 114 ms: 1.08x faster                                     |
| unpickle_list        | 6.99 us                                                               | 6.48 us: 1.08x faster                                    |
| xml_etree_iterparse  | 156 ms                                                                | 148 ms: 1.05x faster                                     |
| pickle_list          | 5.24 us                                                               | 5.26 us: 1.00x slower                                    |
| json_loads           | 30.9 us                                                               | 31.8 us: 1.03x slower                                    |
| pickle_dict          | 35.1 us                                                               | 37.7 us: 1.07x slower                                    |
| pickle               | 12.5 us                                                               | 13.5 us: 1.09x slower                                    |
| unpickle             | 17.5 us                                                               | 19.8 us: 1.13x slower                                    |
| Geometric mean       | (ref)                                                                 | 1.11x faster                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup         | 11.2 ms                                                               | 14.7 ms: 1.31x slower                                    |
| python_startup_no_site | 6.89 ms                                                               | 10.7 ms: 1.55x slower                                    |
| Geometric mean         | (ref)                                                                 | 1.42x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 18.9 ms                                                               | 13.0 ms: 1.46x faster                                    |
| django_template | 53.3 ms                                                               | 48.5 ms: 1.10x faster                                    |
| genshi_text     | 35.2 ms                                                               | 33.6 ms: 1.05x faster                                    |
| genshi_xml      | 69.8 ms                                                               | 78.3 ms: 1.12x slower                                    |
| Geometric mean  | (ref)                                                                 | 1.11x faster                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|--------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| typing_runtime_protocols | 661 us                                                                | 215 us: 3.07x faster                                     |
| deltablue                | 8.94 ms                                                               | 4.58 ms: 1.95x faster                                    |
| bench_mp_pool            | 14.5 ms                                                               | 7.46 ms: 1.95x faster                                    |
| async_tree_io            | 2.28 sec                                                              | 1.23 sec: 1.86x faster                                   |
| async_tree_none          | 950 ms                                                                | 511 ms: 1.86x faster                                     |
| raytrace                 | 573 ms                                                                | 316 ms: 1.81x faster                                     |
| richards_super           | 107 ms                                                                | 59.4 ms: 1.81x faster                                    |
| generators               | 68.1 ms                                                               | 38.1 ms: 1.79x faster                                    |
| richards                 | 91.7 ms                                                               | 52.3 ms: 1.75x faster                                    |
| async_tree_memoization   | 1.13 sec                                                              | 661 ms: 1.71x faster                                     |
| logging_silent           | 222 ns                                                                | 134 ns: 1.66x faster                                     |
| sqlglot_parse            | 2.40 ms                                                               | 1.52 ms: 1.58x faster                                    |
| async_tree_cpu_io_mixed  | 1.27 sec                                                              | 809 ms: 1.57x faster                                     |
| nbody                    | 166 ms                                                                | 108 ms: 1.54x faster                                     |
| asyncio_tcp              | 944 ms                                                                | 614 ms: 1.54x faster                                     |
| crypto_pyaes             | 134 ms                                                                | 87.2 ms: 1.54x faster                                    |
| sqlglot_transpile        | 2.84 ms                                                               | 1.89 ms: 1.51x faster                                    |
| scimark_monte_carlo      | 128 ms                                                                | 84.8 ms: 1.51x faster                                    |
| float                    | 135 ms                                                                | 90.3 ms: 1.49x faster                                    |
| pickle_pure_python       | 529 us                                                                | 356 us: 1.49x faster                                     |
| chaos                    | 121 ms                                                                | 82.8 ms: 1.46x faster                                    |
| mako                     | 18.9 ms                                                               | 13.0 ms: 1.46x faster                                    |
| asyncio_tcp_ssl          | 3.28 sec                                                              | 2.26 sec: 1.45x faster                                   |
| go                       | 264 ms                                                                | 186 ms: 1.42x faster                                     |
| comprehensions           | 33.1 us                                                               | 23.4 us: 1.42x faster                                    |
| scimark_sor              | 246 ms                                                                | 181 ms: 1.36x faster                                     |
| pyflate                  | 795 ms                                                                | 598 ms: 1.33x faster                                     |
| pycparser                | 1.69 sec                                                              | 1.28 sec: 1.32x faster                                   |
| unpickle_pure_python     | 366 us                                                                | 277 us: 1.32x faster                                     |
| spectral_norm            | 186 ms                                                                | 142 ms: 1.31x faster                                     |
| tomli_loads              | 3.36 sec                                                              | 2.56 sec: 1.31x faster                                   |
| thrift                   | 1.26 ms                                                               | 971 us: 1.30x faster                                     |
| json_dumps               | 16.7 ms                                                               | 12.9 ms: 1.30x faster                                    |
| tornado_http             | 178 ms                                                                | 139 ms: 1.29x faster                                     |
| logging_format           | 10.6 us                                                               | 8.27 us: 1.28x faster                                    |
| logging_simple           | 9.78 us                                                               | 7.65 us: 1.28x faster                                    |
| scimark_lu               | 227 ms                                                                | 178 ms: 1.27x faster                                     |
| xml_etree_process        | 99.5 ms                                                               | 80.3 ms: 1.24x faster                                    |
| coroutines               | 37.2 ms                                                               | 30.0 ms: 1.24x faster                                    |
| html5lib                 | 86.5 ms                                                               | 70.3 ms: 1.23x faster                                    |
| deepcopy_memo            | 61.7 us                                                               | 50.3 us: 1.23x faster                                    |
| hexiom                   | 10.9 ms                                                               | 8.94 ms: 1.22x faster                                    |
| bench_thread_pool        | 1.59 ms                                                               | 1.31 ms: 1.21x faster                                    |
| pylint                   | 485 ms                                                                | 406 ms: 1.20x faster                                     |
| fannkuch                 | 546 ms                                                                | 460 ms: 1.19x faster                                     |
| chameleon                | 10.8 ms                                                               | 9.13 ms: 1.19x faster                                    |
| sqlglot_normalize        | 156 ms                                                                | 137 ms: 1.14x faster                                     |
| xml_etree_parse          | 212 ms                                                                | 186 ms: 1.14x faster                                     |
| dask                     | 450 ms                                                                | 397 ms: 1.13x faster                                     |
| pathlib                  | 26.3 ms                                                               | 23.3 ms: 1.13x faster                                    |
| deepcopy_reduce          | 4.60 us                                                               | 4.11 us: 1.12x faster                                    |
| deepcopy                 | 511 us                                                                | 460 us: 1.11x faster                                     |
| regex_compile            | 177 ms                                                                | 159 ms: 1.11x faster                                     |
| sqlglot_optimize         | 75.4 ms                                                               | 68.1 ms: 1.11x faster                                    |
| scimark_fft              | 500 ms                                                                | 454 ms: 1.10x faster                                     |
| django_template          | 53.3 ms                                                               | 48.5 ms: 1.10x faster                                    |
| 2to3                     | 381 ms                                                                | 348 ms: 1.09x faster                                     |
| scimark_sparse_mat_mult  | 7.62 ms                                                               | 7.02 ms: 1.09x faster                                    |
| xml_etree_generate       | 123 ms                                                                | 114 ms: 1.08x faster                                     |
| unpickle_list            | 6.99 us                                                               | 6.48 us: 1.08x faster                                    |
| sympy_str                | 329 ms                                                                | 306 ms: 1.07x faster                                     |
| mdp                      | 3.70 sec                                                              | 3.44 sec: 1.07x faster                                   |
| sqlite_synth             | 4.12 us                                                               | 3.85 us: 1.07x faster                                    |
| regex_v8                 | 32.2 ms                                                               | 30.3 ms: 1.06x faster                                    |
| meteor_contest           | 126 ms                                                                | 120 ms: 1.05x faster                                     |
| xml_etree_iterparse      | 156 ms                                                                | 148 ms: 1.05x faster                                     |
| json                     | 5.88 ms                                                               | 5.59 ms: 1.05x faster                                    |
| sympy_sum                | 184 ms                                                                | 175 ms: 1.05x faster                                     |
| genshi_text              | 35.2 ms                                                               | 33.6 ms: 1.05x faster                                    |
| sympy_expand             | 543 ms                                                                | 519 ms: 1.05x faster                                     |
| regex_dna                | 257 ms                                                                | 246 ms: 1.04x faster                                     |
| sympy_integrate          | 26.5 ms                                                               | 25.5 ms: 1.04x faster                                    |
| dulwich_log              | 73.5 ms                                                               | 70.7 ms: 1.04x faster                                    |
| docutils                 | 3.53 sec                                                              | 3.41 sec: 1.03x faster                                   |
| pidigits                 | 235 ms                                                                | 233 ms: 1.01x faster                                     |
| asyncio_websockets       | 657 ms                                                                | 659 ms: 1.00x slower                                     |
| pickle_list              | 5.24 us                                                               | 5.26 us: 1.00x slower                                    |
| pprint_safe_repr         | 1.15 sec                                                              | 1.17 sec: 1.02x slower                                   |
| nqueens                  | 117 ms                                                                | 120 ms: 1.02x slower                                     |
| create_gc_cycles         | 2.26 ms                                                               | 2.32 ms: 1.03x slower                                    |
| pprint_pformat           | 2.36 sec                                                              | 2.42 sec: 1.03x slower                                   |
| json_loads               | 30.9 us                                                               | 31.8 us: 1.03x slower                                    |
| pickle_dict              | 35.1 us                                                               | 37.7 us: 1.07x slower                                    |
| pickle                   | 12.5 us                                                               | 13.5 us: 1.09x slower                                    |
| async_generators         | 452 ms                                                                | 501 ms: 1.11x slower                                     |
| genshi_xml               | 69.8 ms                                                               | 78.3 ms: 1.12x slower                                    |
| unpickle                 | 17.5 us                                                               | 19.8 us: 1.13x slower                                    |
| regex_effbot             | 4.25 ms                                                               | 4.84 ms: 1.14x slower                                    |
| telco                    | 8.49 ms                                                               | 9.88 ms: 1.16x slower                                    |
| coverage                 | 83.6 ms                                                               | 99.2 ms: 1.19x slower                                    |
| gc_traversal             | 4.15 ms                                                               | 5.05 ms: 1.22x slower                                    |
| python_startup           | 11.2 ms                                                               | 14.7 ms: 1.31x slower                                    |
| python_startup_no_site   | 6.89 ms                                                               | 10.7 ms: 1.55x slower                                    |
| Geometric mean           | (ref)                                                                 | 1.21x faster                                             |
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240501-3.13.0a6+-a7711a2-JIT/bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.22x
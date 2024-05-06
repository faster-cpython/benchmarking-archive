# Results vs. 3.10.4

- fork: python
- ref: c408c36e9b346f9f15a3
- machine: linux-aarch64
- commit hash: c408c36
- commit date: 2024-05-01
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 381 ms                                                                | 348 ms: 1.09x faster                                                     |
| chameleon      | 10.8 ms                                                               | 9.37 ms: 1.16x faster                                                    |
| docutils       | 3.53 sec                                                              | 3.40 sec: 1.04x faster                                                   |
| html5lib       | 86.5 ms                                                               | 70.4 ms: 1.23x faster                                                    |
| tornado_http   | 178 ms                                                                | 140 ms: 1.28x faster                                                     |
| Geometric mean | (ref)                                                                 | 1.16x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|-------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none         | 950 ms                                                                | 508 ms: 1.87x faster                                                     |
| async_tree_io           | 2.28 sec                                                              | 1.24 sec: 1.84x faster                                                   |
| async_tree_memoization  | 1.13 sec                                                              | 659 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed | 1.27 sec                                                              | 804 ms: 1.58x faster                                                     |
| Geometric mean          | (ref)                                                                 | 1.75x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 166 ms                                                                | 107 ms: 1.55x faster                                                     |
| float          | 135 ms                                                                | 89.2 ms: 1.51x faster                                                    |
| pidigits       | 235 ms                                                                | 233 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                 | 1.33x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 177 ms                                                                | 160 ms: 1.10x faster                                                     |
| regex_v8       | 32.2 ms                                                               | 30.2 ms: 1.06x faster                                                    |
| regex_dna      | 257 ms                                                                | 247 ms: 1.04x faster                                                     |
| regex_effbot   | 4.25 ms                                                               | 4.85 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 529 us                                                                | 354 us: 1.50x faster                                                     |
| unpickle_pure_python | 366 us                                                                | 276 us: 1.32x faster                                                     |
| tomli_loads          | 3.36 sec                                                              | 2.57 sec: 1.31x faster                                                   |
| json_dumps           | 16.7 ms                                                               | 12.8 ms: 1.30x faster                                                    |
| xml_etree_process    | 99.5 ms                                                               | 80.3 ms: 1.24x faster                                                    |
| xml_etree_parse      | 212 ms                                                                | 188 ms: 1.13x faster                                                     |
| unpickle_list        | 6.99 us                                                               | 6.31 us: 1.11x faster                                                    |
| xml_etree_generate   | 123 ms                                                                | 113 ms: 1.09x faster                                                     |
| xml_etree_iterparse  | 156 ms                                                                | 147 ms: 1.06x faster                                                     |
| json_loads           | 30.9 us                                                               | 31.9 us: 1.03x slower                                                    |
| pickle_dict          | 35.1 us                                                               | 37.8 us: 1.08x slower                                                    |
| pickle               | 12.5 us                                                               | 13.4 us: 1.08x slower                                                    |
| unpickle             | 17.5 us                                                               | 19.7 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.11x faster                                                             |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.2 ms                                                               | 14.7 ms: 1.31x slower                                                    |
| python_startup_no_site | 6.89 ms                                                               | 10.7 ms: 1.55x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.43x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 18.9 ms                                                               | 12.8 ms: 1.48x faster                                                    |
| django_template | 53.3 ms                                                               | 48.3 ms: 1.10x faster                                                    |
| genshi_text     | 35.2 ms                                                               | 33.8 ms: 1.04x faster                                                    |
| genshi_xml      | 69.8 ms                                                               | 79.5 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.11x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|--------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 661 us                                                                | 213 us: 3.10x faster                                                     |
| deltablue                | 8.94 ms                                                               | 4.59 ms: 1.95x faster                                                    |
| async_tree_none          | 950 ms                                                                | 508 ms: 1.87x faster                                                     |
| async_tree_io            | 2.28 sec                                                              | 1.24 sec: 1.84x faster                                                   |
| raytrace                 | 573 ms                                                                | 317 ms: 1.81x faster                                                     |
| richards_super           | 107 ms                                                                | 59.3 ms: 1.81x faster                                                    |
| generators               | 68.1 ms                                                               | 38.1 ms: 1.79x faster                                                    |
| richards                 | 91.7 ms                                                               | 52.5 ms: 1.75x faster                                                    |
| async_tree_memoization   | 1.13 sec                                                              | 659 ms: 1.72x faster                                                     |
| bench_mp_pool            | 14.5 ms                                                               | 8.69 ms: 1.67x faster                                                    |
| logging_silent           | 222 ns                                                                | 133 ns: 1.67x faster                                                     |
| sqlglot_parse            | 2.40 ms                                                               | 1.51 ms: 1.59x faster                                                    |
| async_tree_cpu_io_mixed  | 1.27 sec                                                              | 804 ms: 1.58x faster                                                     |
| nbody                    | 166 ms                                                                | 107 ms: 1.55x faster                                                     |
| crypto_pyaes             | 134 ms                                                                | 87.5 ms: 1.53x faster                                                    |
| asyncio_tcp              | 944 ms                                                                | 622 ms: 1.52x faster                                                     |
| scimark_monte_carlo      | 128 ms                                                                | 84.4 ms: 1.51x faster                                                    |
| float                    | 135 ms                                                                | 89.2 ms: 1.51x faster                                                    |
| sqlglot_transpile        | 2.84 ms                                                               | 1.88 ms: 1.51x faster                                                    |
| pickle_pure_python       | 529 us                                                                | 354 us: 1.50x faster                                                     |
| mako                     | 18.9 ms                                                               | 12.8 ms: 1.48x faster                                                    |
| chaos                    | 121 ms                                                                | 82.1 ms: 1.47x faster                                                    |
| asyncio_tcp_ssl          | 3.28 sec                                                              | 2.27 sec: 1.44x faster                                                   |
| go                       | 264 ms                                                                | 187 ms: 1.41x faster                                                     |
| comprehensions           | 33.1 us                                                               | 23.5 us: 1.41x faster                                                    |
| scimark_sor              | 246 ms                                                                | 183 ms: 1.35x faster                                                     |
| pyflate                  | 795 ms                                                                | 592 ms: 1.34x faster                                                     |
| unpickle_pure_python     | 366 us                                                                | 276 us: 1.32x faster                                                     |
| pycparser                | 1.69 sec                                                              | 1.28 sec: 1.32x faster                                                   |
| spectral_norm            | 186 ms                                                                | 143 ms: 1.31x faster                                                     |
| tomli_loads              | 3.36 sec                                                              | 2.57 sec: 1.31x faster                                                   |
| json_dumps               | 16.7 ms                                                               | 12.8 ms: 1.30x faster                                                    |
| logging_simple           | 9.78 us                                                               | 7.61 us: 1.28x faster                                                    |
| thrift                   | 1.26 ms                                                               | 985 us: 1.28x faster                                                     |
| tornado_http             | 178 ms                                                                | 140 ms: 1.28x faster                                                     |
| logging_format           | 10.6 us                                                               | 8.34 us: 1.27x faster                                                    |
| scimark_lu               | 227 ms                                                                | 181 ms: 1.25x faster                                                     |
| coroutines               | 37.2 ms                                                               | 29.9 ms: 1.24x faster                                                    |
| xml_etree_process        | 99.5 ms                                                               | 80.3 ms: 1.24x faster                                                    |
| html5lib                 | 86.5 ms                                                               | 70.4 ms: 1.23x faster                                                    |
| hexiom                   | 10.9 ms                                                               | 8.94 ms: 1.22x faster                                                    |
| deepcopy_memo            | 61.7 us                                                               | 50.8 us: 1.22x faster                                                    |
| bench_thread_pool        | 1.59 ms                                                               | 1.33 ms: 1.20x faster                                                    |
| pylint                   | 485 ms                                                                | 408 ms: 1.19x faster                                                     |
| fannkuch                 | 546 ms                                                                | 461 ms: 1.18x faster                                                     |
| chameleon                | 10.8 ms                                                               | 9.37 ms: 1.16x faster                                                    |
| dask                     | 450 ms                                                                | 394 ms: 1.14x faster                                                     |
| sqlglot_normalize        | 156 ms                                                                | 137 ms: 1.14x faster                                                     |
| pathlib                  | 26.3 ms                                                               | 23.3 ms: 1.13x faster                                                    |
| xml_etree_parse          | 212 ms                                                                | 188 ms: 1.13x faster                                                     |
| sqlglot_optimize         | 75.4 ms                                                               | 68.0 ms: 1.11x faster                                                    |
| unpickle_list            | 6.99 us                                                               | 6.31 us: 1.11x faster                                                    |
| deepcopy                 | 511 us                                                                | 461 us: 1.11x faster                                                     |
| django_template          | 53.3 ms                                                               | 48.3 ms: 1.10x faster                                                    |
| scimark_fft              | 500 ms                                                                | 453 ms: 1.10x faster                                                     |
| regex_compile            | 177 ms                                                                | 160 ms: 1.10x faster                                                     |
| scimark_sparse_mat_mult  | 7.62 ms                                                               | 6.96 ms: 1.10x faster                                                    |
| 2to3                     | 381 ms                                                                | 348 ms: 1.09x faster                                                     |
| deepcopy_reduce          | 4.60 us                                                               | 4.22 us: 1.09x faster                                                    |
| xml_etree_generate       | 123 ms                                                                | 113 ms: 1.09x faster                                                     |
| sqlite_synth             | 4.12 us                                                               | 3.81 us: 1.08x faster                                                    |
| mdp                      | 3.70 sec                                                              | 3.43 sec: 1.08x faster                                                   |
| sympy_str                | 329 ms                                                                | 307 ms: 1.07x faster                                                     |
| regex_v8                 | 32.2 ms                                                               | 30.2 ms: 1.06x faster                                                    |
| meteor_contest           | 126 ms                                                                | 119 ms: 1.06x faster                                                     |
| xml_etree_iterparse      | 156 ms                                                                | 147 ms: 1.06x faster                                                     |
| sympy_sum                | 184 ms                                                                | 174 ms: 1.05x faster                                                     |
| sympy_expand             | 543 ms                                                                | 520 ms: 1.04x faster                                                     |
| dulwich_log              | 73.5 ms                                                               | 70.5 ms: 1.04x faster                                                    |
| genshi_text              | 35.2 ms                                                               | 33.8 ms: 1.04x faster                                                    |
| regex_dna                | 257 ms                                                                | 247 ms: 1.04x faster                                                     |
| sympy_integrate          | 26.5 ms                                                               | 25.5 ms: 1.04x faster                                                    |
| docutils                 | 3.53 sec                                                              | 3.40 sec: 1.04x faster                                                   |
| json                     | 5.88 ms                                                               | 5.66 ms: 1.04x faster                                                    |
| pidigits                 | 235 ms                                                                | 233 ms: 1.01x faster                                                     |
| create_gc_cycles         | 2.26 ms                                                               | 2.30 ms: 1.02x slower                                                    |
| nqueens                  | 117 ms                                                                | 120 ms: 1.02x slower                                                     |
| pprint_safe_repr         | 1.15 sec                                                              | 1.18 sec: 1.03x slower                                                   |
| pprint_pformat           | 2.36 sec                                                              | 2.43 sec: 1.03x slower                                                   |
| json_loads               | 30.9 us                                                               | 31.9 us: 1.03x slower                                                    |
| pickle_dict              | 35.1 us                                                               | 37.8 us: 1.08x slower                                                    |
| pickle                   | 12.5 us                                                               | 13.4 us: 1.08x slower                                                    |
| async_generators         | 452 ms                                                                | 510 ms: 1.13x slower                                                     |
| unpickle                 | 17.5 us                                                               | 19.7 us: 1.13x slower                                                    |
| genshi_xml               | 69.8 ms                                                               | 79.5 ms: 1.14x slower                                                    |
| regex_effbot             | 4.25 ms                                                               | 4.85 ms: 1.14x slower                                                    |
| coverage                 | 83.6 ms                                                               | 99.2 ms: 1.19x slower                                                    |
| telco                    | 8.49 ms                                                               | 10.3 ms: 1.22x slower                                                    |
| gc_traversal             | 4.15 ms                                                               | 5.05 ms: 1.22x slower                                                    |
| python_startup           | 11.2 ms                                                               | 14.7 ms: 1.31x slower                                                    |
| python_startup_no_site   | 6.89 ms                                                               | 10.7 ms: 1.55x slower                                                    |
| Geometric mean           | (ref)                                                                 | 1.21x faster                                                             |

Benchmark hidden because not significant (2): pickle_list, asyncio_websockets
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-arminc-aarch64-python-9d38120e335357a3b294-3.10.4-9d38120.json: aiohttp, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240501-3.13.0a6+-c408c36-JIT/bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.12x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.10x

# Memory
- memory change: 1.22x
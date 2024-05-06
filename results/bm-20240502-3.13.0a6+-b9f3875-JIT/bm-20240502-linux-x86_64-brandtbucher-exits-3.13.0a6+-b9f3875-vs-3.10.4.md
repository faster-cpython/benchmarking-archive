# Results vs. 3.10.4

- fork: brandtbucher
- ref: exits
- machine: linux-x86_64
- commit hash: b9f3875
- commit date: 2024-05-02
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 280 ms: 1.24x faster                                          |
| chameleon      | 9.68 ms                                                | 7.05 ms: 1.37x faster                                         |
| docutils       | 3.30 sec                                               | 2.93 sec: 1.13x faster                                        |
| html5lib       | 88.9 ms                                                | 66.6 ms: 1.33x faster                                         |
| tornado_http   | 136 ms                                                 | 96.2 ms: 1.42x faster                                         |
| Geometric mean | (ref)                                                  | 1.29x faster                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 355 ms: 2.05x faster                                          |
| async_tree_io           | 1.77 sec                                               | 935 ms: 1.89x faster                                          |
| async_tree_memoization  | 870 ms                                                 | 465 ms: 1.87x faster                                          |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 617 ms: 1.65x faster                                          |
| Geometric mean          | (ref)                                                  | 1.86x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 80.0 ms: 1.92x faster                                         |
| float          | 117 ms                                                 | 73.5 ms: 1.59x faster                                         |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                          |
| Geometric mean | (ref)                                                  | 1.46x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 139 ms: 1.36x faster                                          |
| regex_v8       | 27.8 ms                                                | 24.1 ms: 1.15x faster                                         |
| regex_dna      | 227 ms                                                 | 223 ms: 1.01x faster                                          |
| Geometric mean | (ref)                                                  | 1.12x faster                                                  |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| tomli_loads          | 3.14 sec                                               | 1.92 sec: 1.63x faster                                        |
| pickle_pure_python   | 484 us                                                 | 307 us: 1.58x faster                                          |
| unpickle_pure_python | 331 us                                                 | 218 us: 1.52x faster                                          |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.36x faster                                         |
| xml_etree_process    | 79.1 ms                                                | 59.3 ms: 1.33x faster                                         |
| xml_etree_generate   | 99.4 ms                                                | 86.6 ms: 1.15x faster                                         |
| xml_etree_iterparse  | 115 ms                                                 | 101 ms: 1.15x faster                                          |
| json_loads           | 31.2 us                                                | 27.5 us: 1.13x faster                                         |
| xml_etree_parse      | 168 ms                                                 | 150 ms: 1.12x faster                                          |
| pickle_list          | 5.08 us                                                | 4.99 us: 1.02x faster                                         |
| unpickle_list        | 5.20 us                                                | 5.30 us: 1.02x slower                                         |
| pickle               | 10.7 us                                                | 11.9 us: 1.11x slower                                         |
| unpickle             | 14.4 us                                                | 16.1 us: 1.12x slower                                         |
| pickle_dict          | 29.6 us                                                | 34.7 us: 1.17x slower                                         |
| Geometric mean       | (ref)                                                  | 1.16x faster                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.32x faster                                         |
| python_startup_no_site | 5.93 ms                                                | 7.60 ms: 1.28x slower                                         |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 9.69 ms: 1.69x faster                                         |
| django_template | 48.2 ms                                                | 36.9 ms: 1.30x faster                                         |
| genshi_text     | 31.8 ms                                                | 25.4 ms: 1.25x faster                                         |
| genshi_xml      | 66.0 ms                                                | 59.3 ms: 1.11x faster                                         |
| Geometric mean  | (ref)                                                  | 1.32x faster                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 174 us: 3.12x faster                                          |
| generators               | 80.1 ms                                                | 30.3 ms: 2.64x faster                                         |
| deltablue                | 7.91 ms                                                | 3.76 ms: 2.10x faster                                         |
| async_tree_none          | 728 ms                                                 | 355 ms: 2.05x faster                                          |
| richards_super           | 94.7 ms                                                | 49.0 ms: 1.93x faster                                         |
| nbody                    | 154 ms                                                 | 80.0 ms: 1.92x faster                                         |
| logging_silent           | 190 ns                                                 | 99.1 ns: 1.91x faster                                         |
| chaos                    | 115 ms                                                 | 60.8 ms: 1.90x faster                                         |
| async_tree_io            | 1.77 sec                                               | 935 ms: 1.89x faster                                          |
| richards                 | 79.3 ms                                                | 42.3 ms: 1.87x faster                                         |
| async_tree_memoization   | 870 ms                                                 | 465 ms: 1.87x faster                                          |
| raytrace                 | 507 ms                                                 | 275 ms: 1.84x faster                                          |
| scimark_monte_carlo      | 118 ms                                                 | 64.6 ms: 1.83x faster                                         |
| crypto_pyaes             | 128 ms                                                 | 70.1 ms: 1.82x faster                                         |
| spectral_norm            | 170 ms                                                 | 94.8 ms: 1.79x faster                                         |
| asyncio_tcp              | 922 ms                                                 | 532 ms: 1.73x faster                                          |
| comprehensions           | 28.8 us                                                | 16.8 us: 1.71x faster                                         |
| mako                     | 16.3 ms                                                | 9.69 ms: 1.69x faster                                         |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 617 ms: 1.65x faster                                          |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.64x faster                                         |
| tomli_loads              | 3.14 sec                                               | 1.92 sec: 1.63x faster                                        |
| scimark_sor              | 220 ms                                                 | 138 ms: 1.60x faster                                          |
| float                    | 117 ms                                                 | 73.5 ms: 1.59x faster                                         |
| pyflate                  | 716 ms                                                 | 453 ms: 1.58x faster                                          |
| pickle_pure_python       | 484 us                                                 | 307 us: 1.58x faster                                          |
| hexiom                   | 10.4 ms                                                | 6.62 ms: 1.57x faster                                         |
| pylint                   | 551 ms                                                 | 353 ms: 1.56x faster                                          |
| sqlglot_transpile        | 2.57 ms                                                | 1.65 ms: 1.56x faster                                         |
| go                       | 240 ms                                                 | 154 ms: 1.56x faster                                          |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                         |
| fannkuch                 | 532 ms                                                 | 349 ms: 1.52x faster                                          |
| unpickle_pure_python     | 331 us                                                 | 218 us: 1.52x faster                                          |
| scimark_fft              | 466 ms                                                 | 314 ms: 1.48x faster                                          |
| deepcopy_memo            | 58.5 us                                                | 39.9 us: 1.46x faster                                         |
| logging_simple           | 8.30 us                                                | 5.81 us: 1.43x faster                                         |
| logging_format           | 9.09 us                                                | 6.37 us: 1.43x faster                                         |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.55 ms: 1.42x faster                                         |
| tornado_http             | 136 ms                                                 | 96.2 ms: 1.42x faster                                         |
| pprint_safe_repr         | 1.02 sec                                               | 731 ms: 1.39x faster                                          |
| scimark_lu               | 176 ms                                                 | 127 ms: 1.39x faster                                          |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                        |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.37x faster                                        |
| chameleon                | 9.68 ms                                                | 7.05 ms: 1.37x faster                                         |
| regex_compile            | 188 ms                                                 | 139 ms: 1.36x faster                                          |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.36x faster                                         |
| pycparser                | 1.58 sec                                               | 1.18 sec: 1.34x faster                                        |
| html5lib                 | 88.9 ms                                                | 66.6 ms: 1.33x faster                                         |
| xml_etree_process        | 79.1 ms                                                | 59.3 ms: 1.33x faster                                         |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.32x faster                                         |
| thrift                   | 1.07 ms                                                | 814 us: 1.32x faster                                          |
| django_template          | 48.2 ms                                                | 36.9 ms: 1.30x faster                                         |
| deepcopy                 | 479 us                                                 | 368 us: 1.30x faster                                          |
| deepcopy_reduce          | 4.17 us                                                | 3.24 us: 1.29x faster                                         |
| genshi_text              | 31.8 ms                                                | 25.4 ms: 1.25x faster                                         |
| 2to3                     | 348 ms                                                 | 280 ms: 1.24x faster                                          |
| sqlglot_normalize        | 143 ms                                                 | 115 ms: 1.24x faster                                          |
| dulwich_log              | 84.3 ms                                                | 69.2 ms: 1.22x faster                                         |
| sqlglot_optimize         | 69.2 ms                                                | 57.3 ms: 1.21x faster                                         |
| djangocms                | 38.4 us                                                | 32.3 us: 1.19x faster                                         |
| nqueens                  | 106 ms                                                 | 89.0 ms: 1.19x faster                                         |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                         |
| sympy_sum                | 196 ms                                                 | 168 ms: 1.17x faster                                          |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                         |
| dask                     | 441 ms                                                 | 378 ms: 1.17x faster                                          |
| sympy_str                | 346 ms                                                 | 297 ms: 1.16x faster                                          |
| sympy_integrate          | 25.8 ms                                                | 22.3 ms: 1.16x faster                                         |
| regex_v8                 | 27.8 ms                                                | 24.1 ms: 1.15x faster                                         |
| xml_etree_generate       | 99.4 ms                                                | 86.6 ms: 1.15x faster                                         |
| xml_etree_iterparse      | 115 ms                                                 | 101 ms: 1.15x faster                                          |
| bench_thread_pool        | 986 us                                                 | 864 us: 1.14x faster                                          |
| pathlib                  | 20.5 ms                                                | 18.0 ms: 1.14x faster                                         |
| json_loads               | 31.2 us                                                | 27.5 us: 1.13x faster                                         |
| docutils                 | 3.30 sec                                               | 2.93 sec: 1.13x faster                                        |
| json                     | 5.69 ms                                                | 5.09 ms: 1.12x faster                                         |
| xml_etree_parse          | 168 ms                                                 | 150 ms: 1.12x faster                                          |
| sympy_expand             | 566 ms                                                 | 507 ms: 1.12x faster                                          |
| genshi_xml               | 66.0 ms                                                | 59.3 ms: 1.11x faster                                         |
| mdp                      | 2.85 sec                                               | 2.59 sec: 1.10x faster                                        |
| mypy2                    | 894 ms                                                 | 818 ms: 1.09x faster                                          |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.08x faster                                          |
| sqlite_synth             | 3.02 us                                                | 2.86 us: 1.06x faster                                         |
| pickle_list              | 5.08 us                                                | 4.99 us: 1.02x faster                                         |
| regex_dna                | 227 ms                                                 | 223 ms: 1.01x faster                                          |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                          |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                          |
| unpickle_list            | 5.20 us                                                | 5.30 us: 1.02x slower                                         |
| async_generators         | 444 ms                                                 | 466 ms: 1.05x slower                                          |
| gc_traversal             | 3.62 ms                                                | 3.81 ms: 1.05x slower                                         |
| create_gc_cycles         | 1.62 ms                                                | 1.78 ms: 1.10x slower                                         |
| pickle                   | 10.7 us                                                | 11.9 us: 1.11x slower                                         |
| unpickle                 | 14.4 us                                                | 16.1 us: 1.12x slower                                         |
| pickle_dict              | 29.6 us                                                | 34.7 us: 1.17x slower                                         |
| coverage                 | 79.4 ms                                                | 93.2 ms: 1.17x slower                                         |
| telco                    | 7.27 ms                                                | 8.55 ms: 1.18x slower                                         |
| python_startup_no_site   | 5.93 ms                                                | 7.60 ms: 1.28x slower                                         |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                  |

Benchmark hidden because not significant (2): regex_effbot, bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240502-3.13.0a6+-b9f3875-JIT/bm-20240502-linux-x86_64-brandtbucher-exits-3.13.0a6+-b9f3875.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.21x

# Memory
- memory change: 1.20x
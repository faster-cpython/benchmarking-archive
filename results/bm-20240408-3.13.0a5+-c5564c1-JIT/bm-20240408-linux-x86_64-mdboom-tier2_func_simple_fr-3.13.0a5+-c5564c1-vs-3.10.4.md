# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 278 ms: 1.25x faster                                                   |
| chameleon      | 9.68 ms                                                | 7.12 ms: 1.36x faster                                                  |
| docutils       | 3.30 sec                                               | 2.94 sec: 1.12x faster                                                 |
| html5lib       | 88.9 ms                                                | 68.5 ms: 1.30x faster                                                  |
| tornado_http   | 136 ms                                                 | 96.7 ms: 1.41x faster                                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 357 ms: 2.04x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 464 ms: 1.87x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 956 ms: 1.85x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 615 ms: 1.65x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.85x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 90.9 ms: 1.69x faster                                                  |
| float          | 117 ms                                                 | 78.4 ms: 1.49x faster                                                  |
| pidigits       | 191 ms                                                 | 211 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.32x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 145 ms: 1.30x faster                                                   |
| regex_v8       | 27.8 ms                                                | 26.0 ms: 1.07x faster                                                  |
| regex_dna      | 227 ms                                                 | 230 ms: 1.01x slower                                                   |
| regex_effbot   | 3.63 ms                                                | 3.80 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 309 us: 1.57x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.07 sec: 1.52x faster                                                 |
| unpickle_pure_python | 331 us                                                 | 240 us: 1.37x faster                                                   |
| json_dumps           | 14.2 ms                                                | 10.4 ms: 1.36x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 60.2 ms: 1.32x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 87.7 ms: 1.13x faster                                                  |
| json_loads           | 31.2 us                                                | 28.2 us: 1.11x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| unpickle_list        | 5.20 us                                                | 5.32 us: 1.02x slower                                                  |
| pickle_list          | 5.08 us                                                | 5.28 us: 1.04x slower                                                  |
| unpickle             | 14.4 us                                                | 15.0 us: 1.04x slower                                                  |
| pickle               | 10.7 us                                                | 11.8 us: 1.11x slower                                                  |
| pickle_dict          | 29.6 us                                                | 35.4 us: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.33x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 9.51 ms: 1.60x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                  |
| genshi_text    | 31.8 ms                                                | 25.0 ms: 1.27x faster                                                  |
| genshi_xml     | 66.0 ms                                                | 53.7 ms: 1.23x faster                                                  |
| Geometric mean | (ref)                                                  | 1.33x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.81x faster                                                   |
| generators               | 80.1 ms                                                | 29.8 ms: 2.69x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.68 ms: 2.15x faster                                                  |
| async_tree_none          | 728 ms                                                 | 357 ms: 2.04x faster                                                   |
| richards_super           | 94.7 ms                                                | 49.8 ms: 1.90x faster                                                  |
| async_tree_memoization   | 870 ms                                                 | 464 ms: 1.87x faster                                                   |
| pylint                   | 551 ms                                                 | 296 ms: 1.86x faster                                                   |
| chaos                    | 115 ms                                                 | 62.2 ms: 1.86x faster                                                  |
| raytrace                 | 507 ms                                                 | 274 ms: 1.85x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 956 ms: 1.85x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 501 ms: 1.84x faster                                                   |
| logging_silent           | 190 ns                                                 | 103 ns: 1.84x faster                                                   |
| richards                 | 79.3 ms                                                | 44.1 ms: 1.80x faster                                                  |
| scimark_monte_carlo      | 118 ms                                                 | 68.9 ms: 1.72x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 75.6 ms: 1.69x faster                                                  |
| nbody                    | 154 ms                                                 | 90.9 ms: 1.69x faster                                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 615 ms: 1.65x faster                                                   |
| scimark_sor              | 220 ms                                                 | 134 ms: 1.64x faster                                                   |
| sqlglot_parse            | 2.17 ms                                                | 1.33 ms: 1.63x faster                                                  |
| comprehensions           | 28.8 us                                                | 17.9 us: 1.60x faster                                                  |
| coroutines               | 35.1 ms                                                | 22.1 ms: 1.58x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 309 us: 1.57x faster                                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.65 ms: 1.56x faster                                                  |
| go                       | 240 ms                                                 | 157 ms: 1.53x faster                                                   |
| pyflate                  | 716 ms                                                 | 471 ms: 1.52x faster                                                   |
| tomli_loads              | 3.14 sec                                               | 2.07 sec: 1.52x faster                                                 |
| deepcopy_memo            | 58.5 us                                                | 38.5 us: 1.52x faster                                                  |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                  |
| float                    | 117 ms                                                 | 78.4 ms: 1.49x faster                                                  |
| spectral_norm            | 170 ms                                                 | 115 ms: 1.48x faster                                                   |
| hexiom                   | 10.4 ms                                                | 7.04 ms: 1.48x faster                                                  |
| logging_simple           | 8.30 us                                                | 5.84 us: 1.42x faster                                                  |
| tornado_http             | 136 ms                                                 | 96.7 ms: 1.41x faster                                                  |
| logging_format           | 9.09 us                                                | 6.51 us: 1.40x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                 |
| unpickle_pure_python     | 331 us                                                 | 240 us: 1.37x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.4 ms: 1.36x faster                                                  |
| chameleon                | 9.68 ms                                                | 7.12 ms: 1.36x faster                                                  |
| fannkuch                 | 532 ms                                                 | 397 ms: 1.34x faster                                                   |
| pprint_safe_repr         | 1.02 sec                                               | 762 ms: 1.34x faster                                                   |
| scimark_fft              | 466 ms                                                 | 349 ms: 1.33x faster                                                   |
| pprint_pformat           | 2.10 sec                                               | 1.58 sec: 1.33x faster                                                 |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.33x faster                                                  |
| deepcopy                 | 479 us                                                 | 362 us: 1.32x faster                                                   |
| scimark_lu               | 176 ms                                                 | 134 ms: 1.32x faster                                                   |
| xml_etree_process        | 79.1 ms                                                | 60.2 ms: 1.32x faster                                                  |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.93 ms: 1.31x faster                                                  |
| thrift                   | 1.07 ms                                                | 820 us: 1.31x faster                                                   |
| regex_compile            | 188 ms                                                 | 145 ms: 1.30x faster                                                   |
| html5lib                 | 88.9 ms                                                | 68.5 ms: 1.30x faster                                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.25 us: 1.28x faster                                                  |
| pycparser                | 1.58 sec                                               | 1.23 sec: 1.28x faster                                                 |
| genshi_text              | 31.8 ms                                                | 25.0 ms: 1.27x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.26x faster                                                   |
| 2to3                     | 348 ms                                                 | 278 ms: 1.25x faster                                                   |
| genshi_xml               | 66.0 ms                                                | 53.7 ms: 1.23x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 57.4 ms: 1.21x faster                                                  |
| dulwich_log              | 84.3 ms                                                | 70.2 ms: 1.20x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                  |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                                  |
| dask                     | 441 ms                                                 | 376 ms: 1.17x faster                                                   |
| sympy_sum                | 196 ms                                                 | 168 ms: 1.17x faster                                                   |
| nqueens                  | 106 ms                                                 | 90.9 ms: 1.16x faster                                                  |
| sympy_integrate          | 25.8 ms                                                | 22.2 ms: 1.16x faster                                                  |
| sympy_str                | 346 ms                                                 | 298 ms: 1.16x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 856 us: 1.15x faster                                                   |
| mypy2                    | 894 ms                                                 | 786 ms: 1.14x faster                                                   |
| sympy_expand             | 566 ms                                                 | 498 ms: 1.13x faster                                                   |
| xml_etree_generate       | 99.4 ms                                                | 87.7 ms: 1.13x faster                                                  |
| docutils                 | 3.30 sec                                               | 2.94 sec: 1.12x faster                                                 |
| json_loads               | 31.2 us                                                | 28.2 us: 1.11x faster                                                  |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| json                     | 5.69 ms                                                | 5.29 ms: 1.08x faster                                                  |
| pathlib                  | 20.5 ms                                                | 19.1 ms: 1.07x faster                                                  |
| regex_v8                 | 27.8 ms                                                | 26.0 ms: 1.07x faster                                                  |
| meteor_contest           | 120 ms                                                 | 113 ms: 1.06x faster                                                   |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.89 us: 1.05x faster                                                  |
| mdp                      | 2.85 sec                                               | 2.83 sec: 1.01x faster                                                 |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                   |
| regex_dna                | 227 ms                                                 | 230 ms: 1.01x slower                                                   |
| unpickle_list            | 5.20 us                                                | 5.32 us: 1.02x slower                                                  |
| async_generators         | 444 ms                                                 | 459 ms: 1.03x slower                                                   |
| pickle_list              | 5.08 us                                                | 5.28 us: 1.04x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.0 us: 1.04x slower                                                  |
| regex_effbot             | 3.63 ms                                                | 3.80 ms: 1.05x slower                                                  |
| gc_traversal             | 3.62 ms                                                | 3.88 ms: 1.07x slower                                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.08x slower                                                  |
| pidigits                 | 191 ms                                                 | 211 ms: 1.11x slower                                                   |
| pickle                   | 10.7 us                                                | 11.8 us: 1.11x slower                                                  |
| telco                    | 7.27 ms                                                | 8.68 ms: 1.19x slower                                                  |
| pickle_dict              | 29.6 us                                                | 35.4 us: 1.19x slower                                                  |
| coverage                 | 79.4 ms                                                | 98.3 ms: 1.24x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 9.51 ms: 1.60x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.31x faster                                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-c5564c1-JIT/bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x
# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.32x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 279 ms: 1.25x faster                                                   |
| chameleon      | 9.68 ms                                                | 7.06 ms: 1.37x faster                                                  |
| docutils       | 3.30 sec                                               | 2.92 sec: 1.13x faster                                                 |
| html5lib       | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                  |
| tornado_http   | 136 ms                                                 | 96.9 ms: 1.41x faster                                                  |
| Geometric mean | (ref)                                                  | 1.29x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 353 ms: 2.06x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 923 ms: 1.92x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 457 ms: 1.90x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 613 ms: 1.66x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 91.4 ms: 1.68x faster                                                  |
| float          | 117 ms                                                 | 78.0 ms: 1.50x faster                                                  |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.37x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 144 ms: 1.31x faster                                                   |
| regex_v8       | 27.8 ms                                                | 25.1 ms: 1.11x faster                                                  |
| regex_dna      | 227 ms                                                 | 221 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 307 us: 1.58x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.07 sec: 1.52x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.4 ms: 1.37x faster                                                  |
| unpickle_pure_python | 331 us                                                 | 242 us: 1.36x faster                                                   |
| xml_etree_process    | 79.1 ms                                                | 61.5 ms: 1.29x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 88.7 ms: 1.12x faster                                                  |
| json_loads           | 31.2 us                                                | 28.4 us: 1.10x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.01 us: 1.01x faster                                                  |
| unpickle             | 14.4 us                                                | 14.9 us: 1.04x slower                                                  |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                  |
| pickle_dict          | 29.6 us                                                | 35.1 us: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                           |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 9.50 ms: 1.60x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.7 ms: 1.52x faster                                                  |
| genshi_text    | 31.8 ms                                                | 24.2 ms: 1.31x faster                                                  |
| genshi_xml     | 66.0 ms                                                | 53.5 ms: 1.23x faster                                                  |
| Geometric mean | (ref)                                                  | 1.35x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.81x faster                                                   |
| generators               | 80.1 ms                                                | 30.2 ms: 2.65x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.69 ms: 2.14x faster                                                  |
| async_tree_none          | 728 ms                                                 | 353 ms: 2.06x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 923 ms: 1.92x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 457 ms: 1.90x faster                                                   |
| richards_super           | 94.7 ms                                                | 50.1 ms: 1.89x faster                                                  |
| pylint                   | 551 ms                                                 | 296 ms: 1.86x faster                                                   |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                   |
| chaos                    | 115 ms                                                 | 62.6 ms: 1.84x faster                                                  |
| raytrace                 | 507 ms                                                 | 278 ms: 1.82x faster                                                   |
| richards                 | 79.3 ms                                                | 44.0 ms: 1.80x faster                                                  |
| asyncio_tcp              | 922 ms                                                 | 512 ms: 1.80x faster                                                   |
| scimark_monte_carlo      | 118 ms                                                 | 69.0 ms: 1.71x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 75.6 ms: 1.69x faster                                                  |
| nbody                    | 154 ms                                                 | 91.4 ms: 1.68x faster                                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 613 ms: 1.66x faster                                                   |
| scimark_sor              | 220 ms                                                 | 134 ms: 1.64x faster                                                   |
| sqlglot_parse            | 2.17 ms                                                | 1.33 ms: 1.64x faster                                                  |
| comprehensions           | 28.8 us                                                | 17.9 us: 1.61x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 307 us: 1.58x faster                                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.64 ms: 1.56x faster                                                  |
| go                       | 240 ms                                                 | 155 ms: 1.55x faster                                                   |
| pyflate                  | 716 ms                                                 | 464 ms: 1.54x faster                                                   |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                  |
| deepcopy_memo            | 58.5 us                                                | 38.4 us: 1.52x faster                                                  |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.52x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.07 sec: 1.52x faster                                                 |
| float                    | 117 ms                                                 | 78.0 ms: 1.50x faster                                                  |
| hexiom                   | 10.4 ms                                                | 7.04 ms: 1.48x faster                                                  |
| spectral_norm            | 170 ms                                                 | 116 ms: 1.47x faster                                                   |
| logging_simple           | 8.30 us                                                | 5.80 us: 1.43x faster                                                  |
| logging_format           | 9.09 us                                                | 6.40 us: 1.42x faster                                                  |
| tornado_http             | 136 ms                                                 | 96.9 ms: 1.41x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                 |
| chameleon                | 9.68 ms                                                | 7.06 ms: 1.37x faster                                                  |
| json_dumps               | 14.2 ms                                                | 10.4 ms: 1.37x faster                                                  |
| unpickle_pure_python     | 331 us                                                 | 242 us: 1.36x faster                                                   |
| scimark_fft              | 466 ms                                                 | 342 ms: 1.36x faster                                                   |
| pprint_pformat           | 2.10 sec                                               | 1.56 sec: 1.35x faster                                                 |
| pycparser                | 1.58 sec                                               | 1.19 sec: 1.33x faster                                                 |
| fannkuch                 | 532 ms                                                 | 400 ms: 1.33x faster                                                   |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                  |
| deepcopy                 | 479 us                                                 | 363 us: 1.32x faster                                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.91 ms: 1.32x faster                                                  |
| scimark_lu               | 176 ms                                                 | 134 ms: 1.32x faster                                                   |
| genshi_text              | 31.8 ms                                                | 24.2 ms: 1.31x faster                                                  |
| pprint_safe_repr         | 1.02 sec                                               | 775 ms: 1.31x faster                                                   |
| thrift                   | 1.07 ms                                                | 817 us: 1.31x faster                                                   |
| regex_compile            | 188 ms                                                 | 144 ms: 1.31x faster                                                   |
| html5lib                 | 88.9 ms                                                | 68.0 ms: 1.31x faster                                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.21 us: 1.30x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 61.5 ms: 1.29x faster                                                  |
| 2to3                     | 348 ms                                                 | 279 ms: 1.25x faster                                                   |
| sqlglot_normalize        | 143 ms                                                 | 115 ms: 1.24x faster                                                   |
| genshi_xml               | 66.0 ms                                                | 53.5 ms: 1.23x faster                                                  |
| dulwich_log              | 84.3 ms                                                | 70.6 ms: 1.19x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 58.2 ms: 1.19x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                  |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                                  |
| dask                     | 441 ms                                                 | 375 ms: 1.17x faster                                                   |
| sympy_sum                | 196 ms                                                 | 168 ms: 1.17x faster                                                   |
| sympy_integrate          | 25.8 ms                                                | 22.1 ms: 1.17x faster                                                  |
| nqueens                  | 106 ms                                                 | 90.9 ms: 1.16x faster                                                  |
| sympy_str                | 346 ms                                                 | 297 ms: 1.16x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 858 us: 1.15x faster                                                   |
| sympy_expand             | 566 ms                                                 | 497 ms: 1.14x faster                                                   |
| mypy2                    | 894 ms                                                 | 789 ms: 1.13x faster                                                   |
| docutils                 | 3.30 sec                                               | 2.92 sec: 1.13x faster                                                 |
| xml_etree_generate       | 99.4 ms                                                | 88.7 ms: 1.12x faster                                                  |
| regex_v8                 | 27.8 ms                                                | 25.1 ms: 1.11x faster                                                  |
| json_loads               | 31.2 us                                                | 28.4 us: 1.10x faster                                                  |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.09x faster                                                   |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| json                     | 5.69 ms                                                | 5.29 ms: 1.08x faster                                                  |
| pathlib                  | 20.5 ms                                                | 19.3 ms: 1.06x faster                                                  |
| sqlite_synth             | 3.02 us                                                | 2.87 us: 1.05x faster                                                  |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| regex_dna                | 227 ms                                                 | 221 ms: 1.03x faster                                                   |
| pickle_list              | 5.08 us                                                | 5.01 us: 1.01x faster                                                  |
| mdp                      | 2.85 sec                                               | 2.82 sec: 1.01x faster                                                 |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                   |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.02x slower                                                   |
| unpickle                 | 14.4 us                                                | 14.9 us: 1.04x slower                                                  |
| async_generators         | 444 ms                                                 | 462 ms: 1.04x slower                                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                  |
| gc_traversal             | 3.62 ms                                                | 3.96 ms: 1.09x slower                                                  |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                  |
| pickle_dict              | 29.6 us                                                | 35.1 us: 1.19x slower                                                  |
| telco                    | 7.27 ms                                                | 8.79 ms: 1.21x slower                                                  |
| coverage                 | 79.4 ms                                                | 99.0 ms: 1.25x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 9.50 ms: 1.60x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.32x faster                                                           |

Benchmark hidden because not significant (3): regex_effbot, unpickle_list, bench_mp_pool
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240410-3.13.0a5+-c181b59-JIT/bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.18x
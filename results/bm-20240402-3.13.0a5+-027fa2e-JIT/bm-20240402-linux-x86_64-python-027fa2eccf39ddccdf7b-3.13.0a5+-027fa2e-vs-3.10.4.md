# Results vs. 3.10.4

- fork: python
- ref: 027fa2eccf39ddccdf7b
- machine: linux-x86_64
- commit hash: 027fa2e
- commit date: 2024-04-02
- overall geometric mean: 1.32x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 277 ms: 1.26x faster                                                   |
| chameleon      | 9.68 ms                                                | 6.86 ms: 1.41x faster                                                  |
| docutils       | 3.30 sec                                               | 2.90 sec: 1.13x faster                                                 |
| html5lib       | 88.9 ms                                                | 65.5 ms: 1.36x faster                                                  |
| tornado_http   | 136 ms                                                 | 96.1 ms: 1.42x faster                                                  |
| Geometric mean | (ref)                                                  | 1.31x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 355 ms: 2.05x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 454 ms: 1.92x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 933 ms: 1.90x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 617 ms: 1.65x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 91.7 ms: 1.67x faster                                                  |
| float          | 117 ms                                                 | 76.2 ms: 1.54x faster                                                  |
| pidigits       | 191 ms                                                 | 202 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                  | 1.34x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 146 ms: 1.29x faster                                                   |
| regex_v8       | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                  |
| regex_dna      | 227 ms                                                 | 220 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 305 us: 1.59x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.07 sec: 1.52x faster                                                 |
| unpickle_pure_python | 331 us                                                 | 236 us: 1.40x faster                                                   |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 59.7 ms: 1.33x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                  |
| json_loads           | 31.2 us                                                | 28.8 us: 1.09x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.06x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| unpickle             | 14.4 us                                                | 14.8 us: 1.03x slower                                                  |
| pickle               | 10.7 us                                                | 12.0 us: 1.13x slower                                                  |
| pickle_dict          | 29.6 us                                                | 34.0 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                           |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 9.49 ms: 1.60x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                  |
| genshi_text    | 31.8 ms                                                | 24.6 ms: 1.29x faster                                                  |
| genshi_xml     | 66.0 ms                                                | 55.0 ms: 1.20x faster                                                  |
| Geometric mean | (ref)                                                  | 1.33x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 111 us: 4.90x faster                                                   |
| generators               | 80.1 ms                                                | 29.7 ms: 2.70x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.42 ms: 2.31x faster                                                  |
| async_tree_none          | 728 ms                                                 | 355 ms: 2.05x faster                                                   |
| logging_silent           | 190 ns                                                 | 97.9 ns: 1.94x faster                                                  |
| async_tree_memoization   | 870 ms                                                 | 454 ms: 1.92x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 933 ms: 1.90x faster                                                   |
| chaos                    | 115 ms                                                 | 62.1 ms: 1.86x faster                                                  |
| pylint                   | 551 ms                                                 | 298 ms: 1.85x faster                                                   |
| richards_super           | 94.7 ms                                                | 52.2 ms: 1.82x faster                                                  |
| raytrace                 | 507 ms                                                 | 280 ms: 1.81x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 520 ms: 1.77x faster                                                   |
| richards                 | 79.3 ms                                                | 45.9 ms: 1.73x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 74.9 ms: 1.71x faster                                                  |
| scimark_monte_carlo      | 118 ms                                                 | 69.3 ms: 1.71x faster                                                  |
| nbody                    | 154 ms                                                 | 91.7 ms: 1.67x faster                                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 617 ms: 1.65x faster                                                   |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.64x faster                                                  |
| scimark_sor              | 220 ms                                                 | 135 ms: 1.62x faster                                                   |
| comprehensions           | 28.8 us                                                | 17.9 us: 1.61x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 305 us: 1.59x faster                                                   |
| coroutines               | 35.1 ms                                                | 22.2 ms: 1.58x faster                                                  |
| sqlglot_transpile        | 2.57 ms                                                | 1.64 ms: 1.57x faster                                                  |
| go                       | 240 ms                                                 | 153 ms: 1.57x faster                                                   |
| float                    | 117 ms                                                 | 76.2 ms: 1.54x faster                                                  |
| pyflate                  | 716 ms                                                 | 469 ms: 1.53x faster                                                   |
| tomli_loads              | 3.14 sec                                               | 2.07 sec: 1.52x faster                                                 |
| deepcopy_memo            | 58.5 us                                                | 38.5 us: 1.52x faster                                                  |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.50x faster                                                  |
| spectral_norm            | 170 ms                                                 | 115 ms: 1.48x faster                                                   |
| hexiom                   | 10.4 ms                                                | 7.08 ms: 1.47x faster                                                  |
| tornado_http             | 136 ms                                                 | 96.1 ms: 1.42x faster                                                  |
| chameleon                | 9.68 ms                                                | 6.86 ms: 1.41x faster                                                  |
| unpickle_pure_python     | 331 us                                                 | 236 us: 1.40x faster                                                   |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.39x faster                                                 |
| pprint_safe_repr         | 1.02 sec                                               | 733 ms: 1.39x faster                                                   |
| logging_simple           | 8.30 us                                                | 5.98 us: 1.39x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                 |
| logging_format           | 9.09 us                                                | 6.61 us: 1.38x faster                                                  |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                                 |
| html5lib                 | 88.9 ms                                                | 65.5 ms: 1.36x faster                                                  |
| scimark_fft              | 466 ms                                                 | 346 ms: 1.35x faster                                                   |
| fannkuch                 | 532 ms                                                 | 398 ms: 1.34x faster                                                   |
| scimark_lu               | 176 ms                                                 | 132 ms: 1.33x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 59.7 ms: 1.33x faster                                                  |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                  |
| deepcopy                 | 479 us                                                 | 364 us: 1.31x faster                                                   |
| thrift                   | 1.07 ms                                                | 826 us: 1.30x faster                                                   |
| genshi_text              | 31.8 ms                                                | 24.6 ms: 1.29x faster                                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.23 us: 1.29x faster                                                  |
| regex_compile            | 188 ms                                                 | 146 ms: 1.29x faster                                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.02 ms: 1.29x faster                                                  |
| 2to3                     | 348 ms                                                 | 277 ms: 1.26x faster                                                   |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.25x faster                                                   |
| genshi_xml               | 66.0 ms                                                | 55.0 ms: 1.20x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 58.0 ms: 1.19x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                  |
| dulwich_log              | 84.3 ms                                                | 71.2 ms: 1.18x faster                                                  |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                                  |
| sympy_str                | 346 ms                                                 | 294 ms: 1.17x faster                                                   |
| sympy_integrate          | 25.8 ms                                                | 22.0 ms: 1.17x faster                                                  |
| sympy_sum                | 196 ms                                                 | 167 ms: 1.17x faster                                                   |
| dask                     | 441 ms                                                 | 376 ms: 1.17x faster                                                   |
| nqueens                  | 106 ms                                                 | 91.4 ms: 1.16x faster                                                  |
| bench_thread_pool        | 986 us                                                 | 859 us: 1.15x faster                                                   |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                  |
| sympy_expand             | 566 ms                                                 | 494 ms: 1.14x faster                                                   |
| mypy2                    | 894 ms                                                 | 786 ms: 1.14x faster                                                   |
| docutils                 | 3.30 sec                                               | 2.90 sec: 1.13x faster                                                 |
| regex_v8                 | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                  |
| json_loads               | 31.2 us                                                | 28.8 us: 1.09x faster                                                  |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| mdp                      | 2.85 sec                                               | 2.63 sec: 1.08x faster                                                 |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                   |
| pathlib                  | 20.5 ms                                                | 19.1 ms: 1.07x faster                                                  |
| sqlite_synth             | 3.02 us                                                | 2.85 us: 1.06x faster                                                  |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.06x faster                                                   |
| json                     | 5.69 ms                                                | 5.44 ms: 1.05x faster                                                  |
| regex_dna                | 227 ms                                                 | 220 ms: 1.03x faster                                                   |
| pickle_list              | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                   |
| unpickle                 | 14.4 us                                                | 14.8 us: 1.03x slower                                                  |
| async_generators         | 444 ms                                                 | 460 ms: 1.04x slower                                                   |
| gc_traversal             | 3.62 ms                                                | 3.79 ms: 1.05x slower                                                  |
| pidigits                 | 191 ms                                                 | 202 ms: 1.06x slower                                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                  |
| pickle                   | 10.7 us                                                | 12.0 us: 1.13x slower                                                  |
| pickle_dict              | 29.6 us                                                | 34.0 us: 1.15x slower                                                  |
| telco                    | 7.27 ms                                                | 8.51 ms: 1.17x slower                                                  |
| coverage                 | 79.4 ms                                                | 98.1 ms: 1.23x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 9.49 ms: 1.60x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.32x faster                                                           |

Benchmark hidden because not significant (3): regex_effbot, unpickle_list, bench_mp_pool
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-027fa2e-JIT/bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.19x
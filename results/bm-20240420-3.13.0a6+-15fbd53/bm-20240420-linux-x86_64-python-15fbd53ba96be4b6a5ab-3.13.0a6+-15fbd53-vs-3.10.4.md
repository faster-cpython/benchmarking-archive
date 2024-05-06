# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 268 ms: 1.30x faster                                                   |
| chameleon      | 9.68 ms                                                | 7.04 ms: 1.38x faster                                                  |
| docutils       | 3.30 sec                                               | 2.80 sec: 1.18x faster                                                 |
| html5lib       | 88.9 ms                                                | 67.3 ms: 1.32x faster                                                  |
| tornado_http   | 136 ms                                                 | 94.2 ms: 1.45x faster                                                  |
| Geometric mean | (ref)                                                  | 1.32x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 352 ms: 2.07x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 926 ms: 1.91x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 460 ms: 1.89x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 612 ms: 1.66x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.7 ms: 1.73x faster                                                  |
| float          | 117 ms                                                 | 78.8 ms: 1.49x faster                                                  |
| pidigits       | 191 ms                                                 | 193 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.36x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 135 ms: 1.39x faster                                                   |
| regex_v8       | 27.8 ms                                                | 24.6 ms: 1.13x faster                                                  |
| regex_dna      | 227 ms                                                 | 221 ms: 1.02x faster                                                   |
| regex_effbot   | 3.63 ms                                                | 3.74 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 302 us: 1.60x faster                                                   |
| unpickle_pure_python | 331 us                                                 | 213 us: 1.55x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.18 sec: 1.44x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 60.6 ms: 1.30x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 87.1 ms: 1.14x faster                                                  |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                                   |
| xml_etree_parse      | 168 ms                                                 | 157 ms: 1.07x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.16 us: 1.02x slower                                                  |
| unpickle_list        | 5.20 us                                                | 5.46 us: 1.05x slower                                                  |
| unpickle             | 14.4 us                                                | 15.2 us: 1.06x slower                                                  |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                  |
| pickle_dict          | 29.6 us                                                | 35.6 us: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.08 ms: 1.19x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.52x faster                                                  |
| django_template | 48.2 ms                                                | 35.0 ms: 1.37x faster                                                  |
| genshi_text     | 31.8 ms                                                | 24.3 ms: 1.31x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 52.9 ms: 1.25x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 117 us: 4.66x faster                                                   |
| generators               | 80.1 ms                                                | 29.9 ms: 2.68x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.24 ms: 2.44x faster                                                  |
| async_tree_none          | 728 ms                                                 | 352 ms: 2.07x faster                                                   |
| raytrace                 | 507 ms                                                 | 262 ms: 1.94x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 926 ms: 1.91x faster                                                   |
| chaos                    | 115 ms                                                 | 60.6 ms: 1.91x faster                                                  |
| logging_silent           | 190 ns                                                 | 100 ns: 1.89x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 460 ms: 1.89x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 505 ms: 1.83x faster                                                   |
| richards_super           | 94.7 ms                                                | 53.0 ms: 1.79x faster                                                  |
| pylint                   | 551 ms                                                 | 318 ms: 1.73x faster                                                   |
| comprehensions           | 28.8 us                                                | 16.6 us: 1.73x faster                                                  |
| nbody                    | 154 ms                                                 | 88.7 ms: 1.73x faster                                                  |
| scimark_monte_carlo      | 118 ms                                                 | 68.7 ms: 1.72x faster                                                  |
| scimark_sor              | 220 ms                                                 | 129 ms: 1.70x faster                                                   |
| crypto_pyaes             | 128 ms                                                 | 75.4 ms: 1.70x faster                                                  |
| richards                 | 79.3 ms                                                | 47.0 ms: 1.69x faster                                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                  |
| hexiom                   | 10.4 ms                                                | 6.23 ms: 1.67x faster                                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 612 ms: 1.66x faster                                                   |
| go                       | 240 ms                                                 | 145 ms: 1.66x faster                                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 302 us: 1.60x faster                                                   |
| deepcopy_memo            | 58.5 us                                                | 37.4 us: 1.56x faster                                                  |
| unpickle_pure_python     | 331 us                                                 | 213 us: 1.55x faster                                                   |
| coroutines               | 35.1 ms                                                | 22.7 ms: 1.55x faster                                                  |
| scimark_lu               | 176 ms                                                 | 114 ms: 1.54x faster                                                   |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.52x faster                                                  |
| spectral_norm            | 170 ms                                                 | 113 ms: 1.51x faster                                                   |
| float                    | 117 ms                                                 | 78.8 ms: 1.49x faster                                                  |
| pyflate                  | 716 ms                                                 | 483 ms: 1.48x faster                                                   |
| tornado_http             | 136 ms                                                 | 94.2 ms: 1.45x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.18 sec: 1.44x faster                                                 |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                 |
| regex_compile            | 188 ms                                                 | 135 ms: 1.39x faster                                                   |
| logging_simple           | 8.30 us                                                | 5.95 us: 1.39x faster                                                  |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.39x faster                                                 |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| logging_format           | 9.09 us                                                | 6.57 us: 1.38x faster                                                  |
| pprint_safe_repr         | 1.02 sec                                               | 740 ms: 1.38x faster                                                   |
| chameleon                | 9.68 ms                                                | 7.04 ms: 1.38x faster                                                  |
| django_template          | 48.2 ms                                                | 35.0 ms: 1.37x faster                                                  |
| pycparser                | 1.58 sec                                               | 1.15 sec: 1.37x faster                                                 |
| fannkuch                 | 532 ms                                                 | 393 ms: 1.35x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                  |
| deepcopy                 | 479 us                                                 | 358 us: 1.34x faster                                                   |
| nqueens                  | 106 ms                                                 | 79.9 ms: 1.32x faster                                                  |
| thrift                   | 1.07 ms                                                | 810 us: 1.32x faster                                                   |
| html5lib                 | 88.9 ms                                                | 67.3 ms: 1.32x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 109 ms: 1.32x faster                                                   |
| genshi_text              | 31.8 ms                                                | 24.3 ms: 1.31x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 60.6 ms: 1.30x faster                                                  |
| 2to3                     | 348 ms                                                 | 268 ms: 1.30x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.25 us: 1.28x faster                                                  |
| dulwich_log              | 84.3 ms                                                | 66.0 ms: 1.28x faster                                                  |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 54.7 ms: 1.26x faster                                                  |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.25x faster                                                   |
| genshi_xml               | 66.0 ms                                                | 52.9 ms: 1.25x faster                                                  |
| scimark_fft              | 466 ms                                                 | 374 ms: 1.24x faster                                                   |
| sympy_str                | 346 ms                                                 | 279 ms: 1.24x faster                                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.23 ms: 1.24x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                  |
| mypy2                    | 894 ms                                                 | 735 ms: 1.22x faster                                                   |
| djangocms                | 38.4 us                                                | 31.7 us: 1.21x faster                                                  |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                  |
| sympy_expand             | 566 ms                                                 | 469 ms: 1.21x faster                                                   |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 830 us: 1.19x faster                                                   |
| docutils                 | 3.30 sec                                               | 2.80 sec: 1.18x faster                                                 |
| pathlib                  | 20.5 ms                                                | 17.7 ms: 1.16x faster                                                  |
| xml_etree_generate       | 99.4 ms                                                | 87.1 ms: 1.14x faster                                                  |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                  |
| regex_v8                 | 27.8 ms                                                | 24.6 ms: 1.13x faster                                                  |
| json                     | 5.69 ms                                                | 5.15 ms: 1.10x faster                                                  |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.09x faster                                                   |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                                   |
| xml_etree_parse          | 168 ms                                                 | 157 ms: 1.07x faster                                                   |
| mdp                      | 2.85 sec                                               | 2.73 sec: 1.04x faster                                                 |
| regex_dna                | 227 ms                                                 | 221 ms: 1.02x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.97 us: 1.02x faster                                                  |
| async_generators         | 444 ms                                                 | 442 ms: 1.00x faster                                                   |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                   |
| pidigits                 | 191 ms                                                 | 193 ms: 1.01x slower                                                   |
| pickle_list              | 5.08 us                                                | 5.16 us: 1.02x slower                                                  |
| regex_effbot             | 3.63 ms                                                | 3.74 ms: 1.03x slower                                                  |
| gc_traversal             | 3.62 ms                                                | 3.78 ms: 1.04x slower                                                  |
| unpickle_list            | 5.20 us                                                | 5.46 us: 1.05x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.06x slower                                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.74 ms: 1.08x slower                                                  |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 7.08 ms: 1.19x slower                                                  |
| telco                    | 7.27 ms                                                | 8.74 ms: 1.20x slower                                                  |
| pickle_dict              | 29.6 us                                                | 35.6 us: 1.20x slower                                                  |
| coverage                 | 79.4 ms                                                | 97.5 ms: 1.23x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x
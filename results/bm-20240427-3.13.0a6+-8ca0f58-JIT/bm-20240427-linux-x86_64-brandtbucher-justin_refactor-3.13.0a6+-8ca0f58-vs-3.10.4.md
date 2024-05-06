# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_refactor
- machine: linux-x86_64
- commit hash: 8ca0f58
- commit date: 2024-04-27
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 276 ms: 1.26x faster                                                    |
| chameleon      | 9.68 ms                                                | 7.02 ms: 1.38x faster                                                   |
| docutils       | 3.30 sec                                               | 2.90 sec: 1.14x faster                                                  |
| html5lib       | 88.9 ms                                                | 67.5 ms: 1.32x faster                                                   |
| tornado_http   | 136 ms                                                 | 95.6 ms: 1.43x faster                                                   |
| Geometric mean | (ref)                                                  | 1.30x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|-------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 355 ms: 2.05x faster                                                    |
| async_tree_io           | 1.77 sec                                               | 930 ms: 1.90x faster                                                    |
| async_tree_memoization  | 870 ms                                                 | 465 ms: 1.87x faster                                                    |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 610 ms: 1.67x faster                                                    |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 89.9 ms: 1.71x faster                                                   |
| float          | 117 ms                                                 | 77.2 ms: 1.52x faster                                                   |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                  | 1.38x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 140 ms: 1.35x faster                                                    |
| regex_v8       | 27.8 ms                                                | 26.2 ms: 1.06x faster                                                   |
| regex_effbot   | 3.63 ms                                                | 3.70 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                  | 1.09x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 301 us: 1.61x faster                                                    |
| tomli_loads          | 3.14 sec                                               | 2.04 sec: 1.54x faster                                                  |
| unpickle_pure_python | 331 us                                                 | 233 us: 1.42x faster                                                    |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                   |
| xml_etree_process    | 79.1 ms                                                | 59.6 ms: 1.33x faster                                                   |
| xml_etree_generate   | 99.4 ms                                                | 87.0 ms: 1.14x faster                                                   |
| json_loads           | 31.2 us                                                | 28.0 us: 1.11x faster                                                   |
| xml_etree_iterparse  | 115 ms                                                 | 104 ms: 1.11x faster                                                    |
| xml_etree_parse      | 168 ms                                                 | 153 ms: 1.10x faster                                                    |
| pickle               | 10.7 us                                                | 11.5 us: 1.08x slower                                                   |
| unpickle             | 14.4 us                                                | 16.3 us: 1.13x slower                                                   |
| pickle_dict          | 29.6 us                                                | 35.1 us: 1.19x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                            |

Benchmark hidden because not significant (2): unpickle_list, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.33x faster                                                   |
| python_startup_no_site | 5.93 ms                                                | 7.57 ms: 1.28x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                   |
| django_template | 48.2 ms                                                | 35.7 ms: 1.35x faster                                                   |
| genshi_text     | 31.8 ms                                                | 24.4 ms: 1.31x faster                                                   |
| genshi_xml      | 66.0 ms                                                | 53.3 ms: 1.24x faster                                                   |
| Geometric mean  | (ref)                                                  | 1.35x faster                                                            |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.80x faster                                                    |
| generators               | 80.1 ms                                                | 29.8 ms: 2.69x faster                                                   |
| deltablue                | 7.91 ms                                                | 3.62 ms: 2.18x faster                                                   |
| async_tree_none          | 728 ms                                                 | 355 ms: 2.05x faster                                                    |
| logging_silent           | 190 ns                                                 | 98.0 ns: 1.94x faster                                                   |
| richards_super           | 94.7 ms                                                | 49.0 ms: 1.93x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 930 ms: 1.90x faster                                                    |
| async_tree_memoization   | 870 ms                                                 | 465 ms: 1.87x faster                                                    |
| raytrace                 | 507 ms                                                 | 272 ms: 1.86x faster                                                    |
| richards                 | 79.3 ms                                                | 43.1 ms: 1.84x faster                                                   |
| chaos                    | 115 ms                                                 | 63.2 ms: 1.83x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 509 ms: 1.81x faster                                                    |
| crypto_pyaes             | 128 ms                                                 | 73.7 ms: 1.73x faster                                                   |
| scimark_monte_carlo      | 118 ms                                                 | 69.1 ms: 1.71x faster                                                   |
| nbody                    | 154 ms                                                 | 89.9 ms: 1.71x faster                                                   |
| scimark_sor              | 220 ms                                                 | 130 ms: 1.69x faster                                                    |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 610 ms: 1.67x faster                                                    |
| pylint                   | 551 ms                                                 | 334 ms: 1.65x faster                                                    |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.65x faster                                                   |
| pickle_pure_python       | 484 us                                                 | 301 us: 1.61x faster                                                    |
| comprehensions           | 28.8 us                                                | 17.9 us: 1.61x faster                                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.57x faster                                                   |
| go                       | 240 ms                                                 | 153 ms: 1.57x faster                                                    |
| pyflate                  | 716 ms                                                 | 459 ms: 1.56x faster                                                    |
| coroutines               | 35.1 ms                                                | 22.6 ms: 1.55x faster                                                   |
| deepcopy_memo            | 58.5 us                                                | 37.9 us: 1.54x faster                                                   |
| tomli_loads              | 3.14 sec                                               | 2.04 sec: 1.54x faster                                                  |
| float                    | 117 ms                                                 | 77.2 ms: 1.52x faster                                                   |
| hexiom                   | 10.4 ms                                                | 6.86 ms: 1.52x faster                                                   |
| spectral_norm            | 170 ms                                                 | 112 ms: 1.51x faster                                                    |
| mako                     | 16.3 ms                                                | 10.8 ms: 1.51x faster                                                   |
| logging_simple           | 8.30 us                                                | 5.77 us: 1.44x faster                                                   |
| tornado_http             | 136 ms                                                 | 95.6 ms: 1.43x faster                                                   |
| unpickle_pure_python     | 331 us                                                 | 233 us: 1.42x faster                                                    |
| logging_format           | 9.09 us                                                | 6.43 us: 1.41x faster                                                   |
| scimark_fft              | 466 ms                                                 | 336 ms: 1.38x faster                                                    |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                  |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.69 ms: 1.38x faster                                                   |
| chameleon                | 9.68 ms                                                | 7.02 ms: 1.38x faster                                                   |
| pprint_safe_repr         | 1.02 sec                                               | 740 ms: 1.38x faster                                                    |
| fannkuch                 | 532 ms                                                 | 387 ms: 1.37x faster                                                    |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.36x faster                                                  |
| deepcopy                 | 479 us                                                 | 353 us: 1.36x faster                                                    |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                   |
| scimark_lu               | 176 ms                                                 | 130 ms: 1.35x faster                                                    |
| django_template          | 48.2 ms                                                | 35.7 ms: 1.35x faster                                                   |
| regex_compile            | 188 ms                                                 | 140 ms: 1.35x faster                                                    |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.33x faster                                                   |
| xml_etree_process        | 79.1 ms                                                | 59.6 ms: 1.33x faster                                                   |
| html5lib                 | 88.9 ms                                                | 67.5 ms: 1.32x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.17 us: 1.31x faster                                                   |
| thrift                   | 1.07 ms                                                | 817 us: 1.31x faster                                                    |
| genshi_text              | 31.8 ms                                                | 24.4 ms: 1.31x faster                                                   |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.30x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.28x faster                                                    |
| 2to3                     | 348 ms                                                 | 276 ms: 1.26x faster                                                    |
| genshi_xml               | 66.0 ms                                                | 53.3 ms: 1.24x faster                                                   |
| dulwich_log              | 84.3 ms                                                | 69.1 ms: 1.22x faster                                                   |
| sqlglot_optimize         | 69.2 ms                                                | 56.7 ms: 1.22x faster                                                   |
| nqueens                  | 106 ms                                                 | 88.6 ms: 1.19x faster                                                   |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                   |
| sympy_str                | 346 ms                                                 | 291 ms: 1.19x faster                                                    |
| sympy_sum                | 196 ms                                                 | 165 ms: 1.19x faster                                                    |
| sympy_integrate          | 25.8 ms                                                | 21.8 ms: 1.18x faster                                                   |
| djangocms                | 38.4 us                                                | 32.4 us: 1.18x faster                                                   |
| dask                     | 441 ms                                                 | 373 ms: 1.18x faster                                                    |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.18x faster                                                   |
| pathlib                  | 20.5 ms                                                | 17.7 ms: 1.16x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 852 us: 1.16x faster                                                    |
| sympy_expand             | 566 ms                                                 | 489 ms: 1.16x faster                                                    |
| mypy2                    | 894 ms                                                 | 780 ms: 1.15x faster                                                    |
| xml_etree_generate       | 99.4 ms                                                | 87.0 ms: 1.14x faster                                                   |
| docutils                 | 3.30 sec                                               | 2.90 sec: 1.14x faster                                                  |
| json_loads               | 31.2 us                                                | 28.0 us: 1.11x faster                                                   |
| json                     | 5.69 ms                                                | 5.12 ms: 1.11x faster                                                   |
| xml_etree_iterparse      | 115 ms                                                 | 104 ms: 1.11x faster                                                    |
| xml_etree_parse          | 168 ms                                                 | 153 ms: 1.10x faster                                                    |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.09x faster                                                    |
| regex_v8                 | 27.8 ms                                                | 26.2 ms: 1.06x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.89 us: 1.05x faster                                                   |
| mdp                      | 2.85 sec                                               | 2.78 sec: 1.03x faster                                                  |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                    |
| asyncio_websockets       | 559 ms                                                 | 566 ms: 1.01x slower                                                    |
| regex_effbot             | 3.63 ms                                                | 3.70 ms: 1.02x slower                                                   |
| async_generators         | 444 ms                                                 | 462 ms: 1.04x slower                                                    |
| pickle                   | 10.7 us                                                | 11.5 us: 1.08x slower                                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                   |
| gc_traversal             | 3.62 ms                                                | 4.01 ms: 1.11x slower                                                   |
| unpickle                 | 14.4 us                                                | 16.3 us: 1.13x slower                                                   |
| telco                    | 7.27 ms                                                | 8.56 ms: 1.18x slower                                                   |
| pickle_dict              | 29.6 us                                                | 35.1 us: 1.19x slower                                                   |
| coverage                 | 79.4 ms                                                | 98.7 ms: 1.24x slower                                                   |
| python_startup_no_site   | 5.93 ms                                                | 7.57 ms: 1.28x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.33x faster                                                            |

Benchmark hidden because not significant (4): unpickle_list, regex_dna, pickle_list, bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-8ca0f58-JIT/bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.25x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: 1.19x
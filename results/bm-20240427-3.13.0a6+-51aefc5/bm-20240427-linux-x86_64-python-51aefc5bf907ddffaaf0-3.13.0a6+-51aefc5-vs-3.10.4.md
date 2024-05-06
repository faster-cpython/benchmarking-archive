# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 271 ms: 1.29x faster                                                   |
| chameleon      | 9.68 ms                                                | 7.29 ms: 1.33x faster                                                  |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                 |
| html5lib       | 88.9 ms                                                | 68.3 ms: 1.30x faster                                                  |
| tornado_http   | 136 ms                                                 | 94.4 ms: 1.44x faster                                                  |
| Geometric mean | (ref)                                                  | 1.30x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 353 ms: 2.06x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 908 ms: 1.95x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.66x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.88x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 92.5 ms: 1.66x faster                                                  |
| float          | 117 ms                                                 | 78.9 ms: 1.48x faster                                                  |
| pidigits       | 191 ms                                                 | 194 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                  | 1.34x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 136 ms: 1.38x faster                                                   |
| regex_v8       | 27.8 ms                                                | 24.9 ms: 1.12x faster                                                  |
| regex_dna      | 227 ms                                                 | 227 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 306 us: 1.59x faster                                                   |
| unpickle_pure_python | 331 us                                                 | 219 us: 1.51x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.20 sec: 1.43x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 60.7 ms: 1.30x faster                                                  |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 87.8 ms: 1.13x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| unpickle_list        | 5.20 us                                                | 5.32 us: 1.02x slower                                                  |
| unpickle             | 14.4 us                                                | 15.3 us: 1.07x slower                                                  |
| pickle               | 10.7 us                                                | 12.0 us: 1.13x slower                                                  |
| pickle_dict          | 29.6 us                                                | 35.8 us: 1.21x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.0 ms: 1.48x faster                                                  |
| django_template | 48.2 ms                                                | 34.9 ms: 1.38x faster                                                  |
| genshi_text     | 31.8 ms                                                | 24.8 ms: 1.28x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 54.0 ms: 1.22x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.34x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 167 us: 3.26x faster                                                   |
| generators               | 80.1 ms                                                | 29.6 ms: 2.71x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.23 ms: 2.45x faster                                                  |
| async_tree_none          | 728 ms                                                 | 353 ms: 2.06x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 908 ms: 1.95x faster                                                   |
| raytrace                 | 507 ms                                                 | 263 ms: 1.92x faster                                                   |
| chaos                    | 115 ms                                                 | 60.5 ms: 1.91x faster                                                  |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                   |
| logging_silent           | 190 ns                                                 | 102 ns: 1.86x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 509 ms: 1.81x faster                                                   |
| scimark_sor              | 220 ms                                                 | 126 ms: 1.75x faster                                                   |
| richards_super           | 94.7 ms                                                | 54.3 ms: 1.74x faster                                                  |
| pylint                   | 551 ms                                                 | 319 ms: 1.73x faster                                                   |
| comprehensions           | 28.8 us                                                | 16.8 us: 1.71x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 74.8 ms: 1.71x faster                                                  |
| scimark_monte_carlo      | 118 ms                                                 | 69.3 ms: 1.70x faster                                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.28 ms: 1.69x faster                                                  |
| go                       | 240 ms                                                 | 143 ms: 1.68x faster                                                   |
| nbody                    | 154 ms                                                 | 92.5 ms: 1.66x faster                                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.66x faster                                                   |
| richards                 | 79.3 ms                                                | 48.0 ms: 1.65x faster                                                  |
| hexiom                   | 10.4 ms                                                | 6.37 ms: 1.63x faster                                                  |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 306 us: 1.59x faster                                                   |
| coroutines               | 35.1 ms                                                | 23.0 ms: 1.52x faster                                                  |
| unpickle_pure_python     | 331 us                                                 | 219 us: 1.51x faster                                                   |
| deepcopy_memo            | 58.5 us                                                | 39.1 us: 1.50x faster                                                  |
| spectral_norm            | 170 ms                                                 | 114 ms: 1.49x faster                                                   |
| scimark_lu               | 176 ms                                                 | 118 ms: 1.49x faster                                                   |
| mako                     | 16.3 ms                                                | 11.0 ms: 1.48x faster                                                  |
| float                    | 117 ms                                                 | 78.9 ms: 1.48x faster                                                  |
| pyflate                  | 716 ms                                                 | 484 ms: 1.48x faster                                                   |
| tornado_http             | 136 ms                                                 | 94.4 ms: 1.44x faster                                                  |
| logging_simple           | 8.30 us                                                | 5.77 us: 1.44x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.20 sec: 1.43x faster                                                 |
| logging_format           | 9.09 us                                                | 6.41 us: 1.42x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                 |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                  |
| regex_compile            | 188 ms                                                 | 136 ms: 1.38x faster                                                   |
| django_template          | 48.2 ms                                                | 34.9 ms: 1.38x faster                                                  |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                                 |
| pprint_pformat           | 2.10 sec                                               | 1.55 sec: 1.36x faster                                                 |
| pprint_safe_repr         | 1.02 sec                                               | 759 ms: 1.34x faster                                                   |
| chameleon                | 9.68 ms                                                | 7.29 ms: 1.33x faster                                                  |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                  |
| deepcopy                 | 479 us                                                 | 361 us: 1.33x faster                                                   |
| fannkuch                 | 532 ms                                                 | 401 ms: 1.33x faster                                                   |
| thrift                   | 1.07 ms                                                | 810 us: 1.32x faster                                                   |
| nqueens                  | 106 ms                                                 | 80.6 ms: 1.31x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 60.7 ms: 1.30x faster                                                  |
| html5lib                 | 88.9 ms                                                | 68.3 ms: 1.30x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                   |
| 2to3                     | 348 ms                                                 | 271 ms: 1.29x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.24 us: 1.29x faster                                                  |
| genshi_text              | 31.8 ms                                                | 24.8 ms: 1.28x faster                                                  |
| dulwich_log              | 84.3 ms                                                | 65.8 ms: 1.28x faster                                                  |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                  |
| scimark_fft              | 466 ms                                                 | 369 ms: 1.26x faster                                                   |
| sympy_sum                | 196 ms                                                 | 156 ms: 1.26x faster                                                   |
| sqlglot_optimize         | 69.2 ms                                                | 55.3 ms: 1.25x faster                                                  |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.20 ms: 1.24x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.24x faster                                                  |
| sympy_str                | 346 ms                                                 | 280 ms: 1.23x faster                                                   |
| genshi_xml               | 66.0 ms                                                | 54.0 ms: 1.22x faster                                                  |
| mypy2                    | 894 ms                                                 | 737 ms: 1.21x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.26 ms: 1.21x faster                                                  |
| djangocms                | 38.4 us                                                | 31.7 us: 1.21x faster                                                  |
| sympy_expand             | 566 ms                                                 | 472 ms: 1.20x faster                                                   |
| dask                     | 441 ms                                                 | 370 ms: 1.19x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 835 us: 1.18x faster                                                   |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                 |
| pathlib                  | 20.5 ms                                                | 17.7 ms: 1.16x faster                                                  |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                  |
| xml_etree_generate       | 99.4 ms                                                | 87.8 ms: 1.13x faster                                                  |
| regex_v8                 | 27.8 ms                                                | 24.9 ms: 1.12x faster                                                  |
| json                     | 5.69 ms                                                | 5.16 ms: 1.10x faster                                                  |
| mdp                      | 2.85 sec                                               | 2.62 sec: 1.09x faster                                                 |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| meteor_contest           | 120 ms                                                 | 112 ms: 1.07x faster                                                   |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.92 us: 1.04x faster                                                  |
| pickle_list              | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                  |
| regex_dna                | 227 ms                                                 | 227 ms: 1.00x slower                                                   |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                   |
| pidigits                 | 191 ms                                                 | 194 ms: 1.02x slower                                                   |
| unpickle_list            | 5.20 us                                                | 5.32 us: 1.02x slower                                                  |
| gc_traversal             | 3.62 ms                                                | 3.77 ms: 1.04x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.3 us: 1.07x slower                                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.08x slower                                                  |
| pickle                   | 10.7 us                                                | 12.0 us: 1.13x slower                                                  |
| coverage                 | 79.4 ms                                                | 92.7 ms: 1.17x slower                                                  |
| telco                    | 7.27 ms                                                | 8.68 ms: 1.19x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                  |
| pickle_dict              | 29.6 us                                                | 35.8 us: 1.21x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                           |

Benchmark hidden because not significant (2): async_generators, regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x
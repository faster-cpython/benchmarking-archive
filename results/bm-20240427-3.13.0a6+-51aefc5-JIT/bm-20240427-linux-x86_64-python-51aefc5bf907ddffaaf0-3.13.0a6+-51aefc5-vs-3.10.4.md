# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 282 ms: 1.24x faster                                                   |
| chameleon      | 9.68 ms                                                | 7.03 ms: 1.38x faster                                                  |
| docutils       | 3.30 sec                                               | 2.96 sec: 1.11x faster                                                 |
| html5lib       | 88.9 ms                                                | 68.5 ms: 1.30x faster                                                  |
| tornado_http   | 136 ms                                                 | 96.6 ms: 1.41x faster                                                  |
| Geometric mean | (ref)                                                  | 1.28x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 361 ms: 2.02x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 947 ms: 1.87x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 467 ms: 1.86x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.66x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.85x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 92.8 ms: 1.65x faster                                                  |
| float          | 117 ms                                                 | 76.9 ms: 1.52x faster                                                  |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.36x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 143 ms: 1.32x faster                                                   |
| regex_v8       | 27.8 ms                                                | 24.3 ms: 1.14x faster                                                  |
| regex_dna      | 227 ms                                                 | 218 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.12x faster                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 311 us: 1.56x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.04 sec: 1.54x faster                                                 |
| unpickle_pure_python | 331 us                                                 | 235 us: 1.41x faster                                                   |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.34x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 60.6 ms: 1.31x faster                                                  |
| json_loads           | 31.2 us                                                | 27.3 us: 1.14x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 87.9 ms: 1.13x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 104 ms: 1.11x faster                                                   |
| xml_etree_parse      | 168 ms                                                 | 152 ms: 1.11x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.11 us: 1.01x slower                                                  |
| unpickle_list        | 5.20 us                                                | 5.36 us: 1.03x slower                                                  |
| unpickle             | 14.4 us                                                | 15.2 us: 1.06x slower                                                  |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                  |
| pickle_dict          | 29.6 us                                                | 34.7 us: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.61 ms: 1.28x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                  |
| django_template | 48.2 ms                                                | 37.0 ms: 1.30x faster                                                  |
| genshi_text     | 31.8 ms                                                | 26.5 ms: 1.20x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 57.9 ms: 1.14x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.29x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 175 us: 3.12x faster                                                   |
| generators               | 80.1 ms                                                | 30.4 ms: 2.64x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.85 ms: 2.06x faster                                                  |
| async_tree_none          | 728 ms                                                 | 361 ms: 2.02x faster                                                   |
| richards_super           | 94.7 ms                                                | 49.0 ms: 1.93x faster                                                  |
| async_tree_io            | 1.77 sec                                               | 947 ms: 1.87x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 467 ms: 1.86x faster                                                   |
| logging_silent           | 190 ns                                                 | 103 ns: 1.85x faster                                                   |
| richards                 | 79.3 ms                                                | 43.2 ms: 1.84x faster                                                  |
| raytrace                 | 507 ms                                                 | 279 ms: 1.82x faster                                                   |
| chaos                    | 115 ms                                                 | 63.7 ms: 1.81x faster                                                  |
| asyncio_tcp              | 922 ms                                                 | 522 ms: 1.76x faster                                                   |
| crypto_pyaes             | 128 ms                                                 | 74.3 ms: 1.72x faster                                                  |
| scimark_monte_carlo      | 118 ms                                                 | 69.2 ms: 1.71x faster                                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.66x faster                                                   |
| nbody                    | 154 ms                                                 | 92.8 ms: 1.65x faster                                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.33 ms: 1.63x faster                                                  |
| pylint                   | 551 ms                                                 | 346 ms: 1.59x faster                                                   |
| comprehensions           | 28.8 us                                                | 18.3 us: 1.57x faster                                                  |
| scimark_sor              | 220 ms                                                 | 140 ms: 1.57x faster                                                   |
| pickle_pure_python       | 484 us                                                 | 311 us: 1.56x faster                                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.66 ms: 1.55x faster                                                  |
| pyflate                  | 716 ms                                                 | 463 ms: 1.55x faster                                                   |
| tomli_loads              | 3.14 sec                                               | 2.04 sec: 1.54x faster                                                 |
| go                       | 240 ms                                                 | 156 ms: 1.54x faster                                                   |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                  |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.53x faster                                                  |
| float                    | 117 ms                                                 | 76.9 ms: 1.52x faster                                                  |
| deepcopy_memo            | 58.5 us                                                | 39.3 us: 1.49x faster                                                  |
| spectral_norm            | 170 ms                                                 | 114 ms: 1.48x faster                                                   |
| hexiom                   | 10.4 ms                                                | 7.16 ms: 1.45x faster                                                  |
| tornado_http             | 136 ms                                                 | 96.6 ms: 1.41x faster                                                  |
| unpickle_pure_python     | 331 us                                                 | 235 us: 1.41x faster                                                   |
| logging_simple           | 8.30 us                                                | 5.97 us: 1.39x faster                                                  |
| fannkuch                 | 532 ms                                                 | 383 ms: 1.39x faster                                                   |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                 |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.38x faster                                                 |
| chameleon                | 9.68 ms                                                | 7.03 ms: 1.38x faster                                                  |
| pprint_safe_repr         | 1.02 sec                                               | 740 ms: 1.38x faster                                                   |
| logging_format           | 9.09 us                                                | 6.63 us: 1.37x faster                                                  |
| scimark_fft              | 466 ms                                                 | 344 ms: 1.35x faster                                                   |
| pycparser                | 1.58 sec                                               | 1.17 sec: 1.35x faster                                                 |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.34x faster                                                  |
| python_startup           | 14.6 ms                                                | 11.0 ms: 1.32x faster                                                  |
| regex_compile            | 188 ms                                                 | 143 ms: 1.32x faster                                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.94 ms: 1.31x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 60.6 ms: 1.31x faster                                                  |
| thrift                   | 1.07 ms                                                | 821 us: 1.31x faster                                                   |
| django_template          | 48.2 ms                                                | 37.0 ms: 1.30x faster                                                  |
| deepcopy                 | 479 us                                                 | 369 us: 1.30x faster                                                   |
| scimark_lu               | 176 ms                                                 | 136 ms: 1.30x faster                                                   |
| html5lib                 | 88.9 ms                                                | 68.5 ms: 1.30x faster                                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.25 us: 1.28x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 115 ms: 1.25x faster                                                   |
| 2to3                     | 348 ms                                                 | 282 ms: 1.24x faster                                                   |
| dulwich_log              | 84.3 ms                                                | 69.6 ms: 1.21x faster                                                  |
| genshi_text              | 31.8 ms                                                | 26.5 ms: 1.20x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 58.3 ms: 1.19x faster                                                  |
| djangocms                | 38.4 us                                                | 32.5 us: 1.18x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                  |
| dask                     | 441 ms                                                 | 376 ms: 1.17x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                                  |
| sympy_str                | 346 ms                                                 | 299 ms: 1.16x faster                                                   |
| pathlib                  | 20.5 ms                                                | 17.7 ms: 1.15x faster                                                  |
| sympy_sum                | 196 ms                                                 | 170 ms: 1.15x faster                                                   |
| nqueens                  | 106 ms                                                 | 92.1 ms: 1.15x faster                                                  |
| sympy_integrate          | 25.8 ms                                                | 22.6 ms: 1.14x faster                                                  |
| json_loads               | 31.2 us                                                | 27.3 us: 1.14x faster                                                  |
| regex_v8                 | 27.8 ms                                                | 24.3 ms: 1.14x faster                                                  |
| genshi_xml               | 66.0 ms                                                | 57.9 ms: 1.14x faster                                                  |
| bench_thread_pool        | 986 us                                                 | 870 us: 1.13x faster                                                   |
| xml_etree_generate       | 99.4 ms                                                | 87.9 ms: 1.13x faster                                                  |
| sympy_expand             | 566 ms                                                 | 502 ms: 1.13x faster                                                   |
| json                     | 5.69 ms                                                | 5.10 ms: 1.12x faster                                                  |
| docutils                 | 3.30 sec                                               | 2.96 sec: 1.11x faster                                                 |
| xml_etree_iterparse      | 115 ms                                                 | 104 ms: 1.11x faster                                                   |
| xml_etree_parse          | 168 ms                                                 | 152 ms: 1.11x faster                                                   |
| mypy2                    | 894 ms                                                 | 813 ms: 1.10x faster                                                   |
| mdp                      | 2.85 sec                                               | 2.62 sec: 1.09x faster                                                 |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.07x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.85 us: 1.06x faster                                                  |
| regex_dna                | 227 ms                                                 | 218 ms: 1.04x faster                                                   |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                   |
| pickle_list              | 5.08 us                                                | 5.11 us: 1.01x slower                                                  |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                   |
| unpickle_list            | 5.20 us                                                | 5.36 us: 1.03x slower                                                  |
| async_generators         | 444 ms                                                 | 465 ms: 1.05x slower                                                   |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.06x slower                                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.78 ms: 1.10x slower                                                  |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                  |
| gc_traversal             | 3.62 ms                                                | 4.02 ms: 1.11x slower                                                  |
| coverage                 | 79.4 ms                                                | 92.2 ms: 1.16x slower                                                  |
| pickle_dict              | 29.6 us                                                | 34.7 us: 1.17x slower                                                  |
| telco                    | 7.27 ms                                                | 8.66 ms: 1.19x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 7.61 ms: 1.28x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.31x faster                                                           |

Benchmark hidden because not significant (2): bench_mp_pool, regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.24x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.19x
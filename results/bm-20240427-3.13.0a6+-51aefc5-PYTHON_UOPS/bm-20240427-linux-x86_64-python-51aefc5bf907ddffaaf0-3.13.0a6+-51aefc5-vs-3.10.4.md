# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.19x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 314 ms: 1.11x faster                                                   |
| chameleon      | 9.68 ms                                                | 7.49 ms: 1.29x faster                                                  |
| docutils       | 3.30 sec                                               | 3.15 sec: 1.05x faster                                                 |
| html5lib       | 88.9 ms                                                | 71.8 ms: 1.24x faster                                                  |
| tornado_http   | 136 ms                                                 | 102 ms: 1.33x faster                                                   |
| Geometric mean | (ref)                                                  | 1.20x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 376 ms: 1.93x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 967 ms: 1.83x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 502 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 638 ms: 1.59x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.77x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 117 ms                                                 | 90.3 ms: 1.30x faster                                                  |
| nbody          | 154 ms                                                 | 127 ms: 1.21x faster                                                   |
| pidigits       | 191 ms                                                 | 212 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 178 ms: 1.06x faster                                                   |
| regex_v8       | 27.8 ms                                                | 26.4 ms: 1.05x faster                                                  |
| regex_dna      | 227 ms                                                 | 233 ms: 1.03x slower                                                   |
| regex_effbot   | 3.63 ms                                                | 3.89 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 319 us: 1.52x faster                                                   |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                  |
| tomli_loads          | 3.14 sec                                               | 2.53 sec: 1.24x faster                                                 |
| xml_etree_process    | 79.1 ms                                                | 65.2 ms: 1.21x faster                                                  |
| unpickle_pure_python | 331 us                                                 | 289 us: 1.14x faster                                                   |
| json_loads           | 31.2 us                                                | 27.5 us: 1.14x faster                                                  |
| xml_etree_parse      | 168 ms                                                 | 152 ms: 1.11x faster                                                   |
| xml_etree_generate   | 99.4 ms                                                | 94.0 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 112 ms: 1.03x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                                  |
| unpickle_list        | 5.20 us                                                | 5.29 us: 1.02x slower                                                  |
| unpickle             | 14.4 us                                                | 15.5 us: 1.07x slower                                                  |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                  |
| pickle_dict          | 29.6 us                                                | 34.9 us: 1.18x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.14 ms: 1.20x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 13.5 ms: 1.21x faster                                                  |
| django_template | 48.2 ms                                                | 40.2 ms: 1.20x faster                                                  |
| genshi_text     | 31.8 ms                                                | 30.8 ms: 1.03x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 69.1 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.09x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 197 us: 2.76x faster                                                   |
| generators               | 80.1 ms                                                | 31.4 ms: 2.55x faster                                                  |
| async_tree_none          | 728 ms                                                 | 376 ms: 1.93x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 967 ms: 1.83x faster                                                   |
| logging_silent           | 190 ns                                                 | 104 ns: 1.82x faster                                                   |
| deltablue                | 7.91 ms                                                | 4.40 ms: 1.80x faster                                                  |
| asyncio_tcp              | 922 ms                                                 | 530 ms: 1.74x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 502 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 638 ms: 1.59x faster                                                   |
| pylint                   | 551 ms                                                 | 350 ms: 1.57x faster                                                   |
| raytrace                 | 507 ms                                                 | 324 ms: 1.56x faster                                                   |
| pickle_pure_python       | 484 us                                                 | 319 us: 1.52x faster                                                   |
| richards_super           | 94.7 ms                                                | 62.4 ms: 1.52x faster                                                  |
| coroutines               | 35.1 ms                                                | 24.0 ms: 1.46x faster                                                  |
| chaos                    | 115 ms                                                 | 79.3 ms: 1.46x faster                                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.49 ms: 1.45x faster                                                  |
| richards                 | 79.3 ms                                                | 55.5 ms: 1.43x faster                                                  |
| sqlglot_transpile        | 2.57 ms                                                | 1.81 ms: 1.42x faster                                                  |
| scimark_sor              | 220 ms                                                 | 157 ms: 1.40x faster                                                   |
| crypto_pyaes             | 128 ms                                                 | 92.3 ms: 1.39x faster                                                  |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.38x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.37x faster                                                 |
| deepcopy_memo            | 58.5 us                                                | 43.0 us: 1.36x faster                                                  |
| tornado_http             | 136 ms                                                 | 102 ms: 1.33x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                  |
| scimark_monte_carlo      | 118 ms                                                 | 90.6 ms: 1.31x faster                                                  |
| float                    | 117 ms                                                 | 90.3 ms: 1.30x faster                                                  |
| chameleon                | 9.68 ms                                                | 7.49 ms: 1.29x faster                                                  |
| thrift                   | 1.07 ms                                                | 844 us: 1.27x faster                                                   |
| deepcopy                 | 479 us                                                 | 380 us: 1.26x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.33 us: 1.25x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.53 sec: 1.24x faster                                                 |
| html5lib                 | 88.9 ms                                                | 71.8 ms: 1.24x faster                                                  |
| logging_simple           | 8.30 us                                                | 6.81 us: 1.22x faster                                                  |
| go                       | 240 ms                                                 | 197 ms: 1.22x faster                                                   |
| xml_etree_process        | 79.1 ms                                                | 65.2 ms: 1.21x faster                                                  |
| nbody                    | 154 ms                                                 | 127 ms: 1.21x faster                                                   |
| mako                     | 16.3 ms                                                | 13.5 ms: 1.21x faster                                                  |
| djangocms                | 38.4 us                                                | 31.9 us: 1.20x faster                                                  |
| django_template          | 48.2 ms                                                | 40.2 ms: 1.20x faster                                                  |
| logging_format           | 9.09 us                                                | 7.62 us: 1.19x faster                                                  |
| spectral_norm            | 170 ms                                                 | 143 ms: 1.19x faster                                                   |
| pyflate                  | 716 ms                                                 | 606 ms: 1.18x faster                                                   |
| pycparser                | 1.58 sec                                               | 1.34 sec: 1.18x faster                                                 |
| aiohttp                  | 1.44 ms                                                | 1.24 ms: 1.16x faster                                                  |
| comprehensions           | 28.8 us                                                | 24.9 us: 1.16x faster                                                  |
| gunicorn                 | 1.53 ms                                                | 1.34 ms: 1.14x faster                                                  |
| unpickle_pure_python     | 331 us                                                 | 289 us: 1.14x faster                                                   |
| dask                     | 441 ms                                                 | 387 ms: 1.14x faster                                                   |
| json_loads               | 31.2 us                                                | 27.5 us: 1.14x faster                                                  |
| dulwich_log              | 84.3 ms                                                | 75.0 ms: 1.12x faster                                                  |
| pathlib                  | 20.5 ms                                                | 18.2 ms: 1.12x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 128 ms: 1.12x faster                                                   |
| sympy_sum                | 196 ms                                                 | 176 ms: 1.12x faster                                                   |
| 2to3                     | 348 ms                                                 | 314 ms: 1.11x faster                                                   |
| sympy_integrate          | 25.8 ms                                                | 23.3 ms: 1.11x faster                                                  |
| xml_etree_parse          | 168 ms                                                 | 152 ms: 1.11x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 902 us: 1.09x faster                                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.94 ms: 1.09x faster                                                  |
| json                     | 5.69 ms                                                | 5.24 ms: 1.09x faster                                                  |
| mypy2                    | 894 ms                                                 | 823 ms: 1.09x faster                                                   |
| sympy_str                | 346 ms                                                 | 322 ms: 1.07x faster                                                   |
| sqlglot_optimize         | 69.2 ms                                                | 64.5 ms: 1.07x faster                                                  |
| fannkuch                 | 532 ms                                                 | 497 ms: 1.07x faster                                                   |
| pprint_safe_repr         | 1.02 sec                                               | 956 ms: 1.06x faster                                                   |
| xml_etree_generate       | 99.4 ms                                                | 94.0 ms: 1.06x faster                                                  |
| regex_compile            | 188 ms                                                 | 178 ms: 1.06x faster                                                   |
| pprint_pformat           | 2.10 sec                                               | 1.99 sec: 1.06x faster                                                 |
| sympy_expand             | 566 ms                                                 | 537 ms: 1.05x faster                                                   |
| regex_v8                 | 27.8 ms                                                | 26.4 ms: 1.05x faster                                                  |
| docutils                 | 3.30 sec                                               | 3.15 sec: 1.05x faster                                                 |
| hexiom                   | 10.4 ms                                                | 9.97 ms: 1.04x faster                                                  |
| genshi_text              | 31.8 ms                                                | 30.8 ms: 1.03x faster                                                  |
| xml_etree_iterparse      | 115 ms                                                 | 112 ms: 1.03x faster                                                   |
| scimark_fft              | 466 ms                                                 | 452 ms: 1.03x faster                                                   |
| scimark_lu               | 176 ms                                                 | 172 ms: 1.02x faster                                                   |
| mdp                      | 2.85 sec                                               | 2.83 sec: 1.01x faster                                                 |
| pickle_list              | 5.08 us                                                | 5.12 us: 1.01x slower                                                  |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.02x slower                                                   |
| unpickle_list            | 5.20 us                                                | 5.29 us: 1.02x slower                                                  |
| meteor_contest           | 120 ms                                                 | 123 ms: 1.03x slower                                                   |
| regex_dna                | 227 ms                                                 | 233 ms: 1.03x slower                                                   |
| nqueens                  | 106 ms                                                 | 110 ms: 1.04x slower                                                   |
| genshi_xml               | 66.0 ms                                                | 69.1 ms: 1.05x slower                                                  |
| async_generators         | 444 ms                                                 | 475 ms: 1.07x slower                                                   |
| regex_effbot             | 3.63 ms                                                | 3.89 ms: 1.07x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.5 us: 1.07x slower                                                  |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.78 ms: 1.10x slower                                                  |
| pidigits                 | 191 ms                                                 | 212 ms: 1.11x slower                                                   |
| gc_traversal             | 3.62 ms                                                | 4.06 ms: 1.12x slower                                                  |
| coverage                 | 79.4 ms                                                | 92.7 ms: 1.17x slower                                                  |
| pickle_dict              | 29.6 us                                                | 34.9 us: 1.18x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 7.14 ms: 1.20x slower                                                  |
| telco                    | 7.27 ms                                                | 9.18 ms: 1.26x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.19x faster                                                           |

Benchmark hidden because not significant (2): bench_mp_pool, sqlite_synth
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-linux-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.11x
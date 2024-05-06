# Results vs. 3.10.4

- fork: nineteendo
- ref: use_PyTuple_Pack
- machine: linux-x86_64
- commit hash: 59ac30f
- commit date: 2024-04-29
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 267 ms: 1.30x faster                                                   |
| chameleon      | 9.68 ms                                                | 6.98 ms: 1.39x faster                                                  |
| docutils       | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                 |
| html5lib       | 88.9 ms                                                | 67.4 ms: 1.32x faster                                                  |
| tornado_http   | 136 ms                                                 | 93.9 ms: 1.45x faster                                                  |
| Geometric mean | (ref)                                                  | 1.32x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 349 ms: 2.09x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 898 ms: 1.97x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 462 ms: 1.88x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 609 ms: 1.67x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.90x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.1 ms: 1.74x faster                                                  |
| float          | 117 ms                                                 | 77.7 ms: 1.51x faster                                                  |
| pidigits       | 191 ms                                                 | 212 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                  | 1.33x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.40x faster                                                   |
| regex_v8       | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                  |
| regex_dna      | 227 ms                                                 | 218 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.13x faster                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 300 us: 1.62x faster                                                   |
| unpickle_pure_python | 331 us                                                 | 215 us: 1.54x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.15 sec: 1.46x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                  |
| json_loads           | 31.2 us                                                | 27.4 us: 1.14x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| xml_etree_parse      | 168 ms                                                 | 159 ms: 1.05x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| unpickle_list        | 5.20 us                                                | 5.38 us: 1.04x slower                                                  |
| unpickle             | 14.4 us                                                | 15.5 us: 1.08x slower                                                  |
| pickle               | 10.7 us                                                | 11.7 us: 1.10x slower                                                  |
| pickle_dict          | 29.6 us                                                | 34.6 us: 1.17x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.15x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.52x faster                                                  |
| django_template | 48.2 ms                                                | 34.5 ms: 1.40x faster                                                  |
| genshi_text     | 31.8 ms                                                | 23.5 ms: 1.35x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 51.1 ms: 1.29x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.39x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 165 us: 3.30x faster                                                   |
| generators               | 80.1 ms                                                | 29.7 ms: 2.70x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.19 ms: 2.48x faster                                                  |
| async_tree_none          | 728 ms                                                 | 349 ms: 2.09x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 898 ms: 1.97x faster                                                   |
| raytrace                 | 507 ms                                                 | 259 ms: 1.96x faster                                                   |
| logging_silent           | 190 ns                                                 | 97.2 ns: 1.95x faster                                                  |
| chaos                    | 115 ms                                                 | 60.1 ms: 1.92x faster                                                  |
| async_tree_memoization   | 870 ms                                                 | 462 ms: 1.88x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                                   |
| richards_super           | 94.7 ms                                                | 53.1 ms: 1.78x faster                                                  |
| scimark_sor              | 220 ms                                                 | 124 ms: 1.77x faster                                                   |
| nbody                    | 154 ms                                                 | 88.1 ms: 1.74x faster                                                  |
| pylint                   | 551 ms                                                 | 318 ms: 1.74x faster                                                   |
| comprehensions           | 28.8 us                                                | 16.7 us: 1.72x faster                                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.27 ms: 1.71x faster                                                  |
| go                       | 240 ms                                                 | 141 ms: 1.71x faster                                                   |
| scimark_monte_carlo      | 118 ms                                                 | 69.4 ms: 1.70x faster                                                  |
| richards                 | 79.3 ms                                                | 46.6 ms: 1.70x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 75.4 ms: 1.70x faster                                                  |
| hexiom                   | 10.4 ms                                                | 6.15 ms: 1.69x faster                                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 609 ms: 1.67x faster                                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.57 ms: 1.63x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 300 us: 1.62x faster                                                   |
| deepcopy_memo            | 58.5 us                                                | 37.2 us: 1.57x faster                                                  |
| coroutines               | 35.1 ms                                                | 22.4 ms: 1.57x faster                                                  |
| spectral_norm            | 170 ms                                                 | 108 ms: 1.57x faster                                                   |
| unpickle_pure_python     | 331 us                                                 | 215 us: 1.54x faster                                                   |
| pyflate                  | 716 ms                                                 | 466 ms: 1.54x faster                                                   |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.52x faster                                                  |
| scimark_lu               | 176 ms                                                 | 116 ms: 1.52x faster                                                   |
| float                    | 117 ms                                                 | 77.7 ms: 1.51x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.15 sec: 1.46x faster                                                 |
| tornado_http             | 136 ms                                                 | 93.9 ms: 1.45x faster                                                  |
| logging_simple           | 8.30 us                                                | 5.84 us: 1.42x faster                                                  |
| logging_format           | 9.09 us                                                | 6.46 us: 1.41x faster                                                  |
| pprint_pformat           | 2.10 sec                                               | 1.50 sec: 1.40x faster                                                 |
| regex_compile            | 188 ms                                                 | 134 ms: 1.40x faster                                                   |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                 |
| django_template          | 48.2 ms                                                | 34.5 ms: 1.40x faster                                                  |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| chameleon                | 9.68 ms                                                | 6.98 ms: 1.39x faster                                                  |
| pycparser                | 1.58 sec                                               | 1.14 sec: 1.39x faster                                                 |
| pprint_safe_repr         | 1.02 sec                                               | 735 ms: 1.38x faster                                                   |
| fannkuch                 | 532 ms                                                 | 390 ms: 1.36x faster                                                   |
| deepcopy                 | 479 us                                                 | 353 us: 1.36x faster                                                   |
| genshi_text              | 31.8 ms                                                | 23.5 ms: 1.35x faster                                                  |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                  |
| html5lib                 | 88.9 ms                                                | 67.4 ms: 1.32x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 109 ms: 1.31x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.17 us: 1.31x faster                                                  |
| nqueens                  | 106 ms                                                 | 80.7 ms: 1.31x faster                                                  |
| thrift                   | 1.07 ms                                                | 821 us: 1.31x faster                                                   |
| 2to3                     | 348 ms                                                 | 267 ms: 1.30x faster                                                   |
| genshi_xml               | 66.0 ms                                                | 51.1 ms: 1.29x faster                                                  |
| sympy_integrate          | 25.8 ms                                                | 20.2 ms: 1.28x faster                                                  |
| scimark_fft              | 466 ms                                                 | 365 ms: 1.28x faster                                                   |
| sympy_sum                | 196 ms                                                 | 154 ms: 1.27x faster                                                   |
| dulwich_log              | 84.3 ms                                                | 66.3 ms: 1.27x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 54.4 ms: 1.27x faster                                                  |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.12 ms: 1.26x faster                                                  |
| sympy_str                | 346 ms                                                 | 277 ms: 1.25x faster                                                   |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                  |
| mypy2                    | 894 ms                                                 | 733 ms: 1.22x faster                                                   |
| djangocms                | 38.4 us                                                | 31.5 us: 1.22x faster                                                  |
| sympy_expand             | 566 ms                                                 | 467 ms: 1.21x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.20x faster                                                  |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 831 us: 1.19x faster                                                   |
| docutils                 | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                 |
| pathlib                  | 20.5 ms                                                | 17.5 ms: 1.17x faster                                                  |
| xml_etree_generate       | 99.4 ms                                                | 87.2 ms: 1.14x faster                                                  |
| json_loads               | 31.2 us                                                | 27.4 us: 1.14x faster                                                  |
| regex_v8                 | 27.8 ms                                                | 24.4 ms: 1.14x faster                                                  |
| mdp                      | 2.85 sec                                               | 2.57 sec: 1.11x faster                                                 |
| json                     | 5.69 ms                                                | 5.18 ms: 1.10x faster                                                  |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.09x faster                                                   |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| xml_etree_parse          | 168 ms                                                 | 159 ms: 1.05x faster                                                   |
| regex_dna                | 227 ms                                                 | 218 ms: 1.04x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                  |
| pickle_list              | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                   |
| unpickle_list            | 5.20 us                                                | 5.38 us: 1.04x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.5 us: 1.08x slower                                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                  |
| pickle                   | 10.7 us                                                | 11.7 us: 1.10x slower                                                  |
| pidigits                 | 191 ms                                                 | 212 ms: 1.11x slower                                                   |
| gc_traversal             | 3.62 ms                                                | 4.02 ms: 1.11x slower                                                  |
| coverage                 | 79.4 ms                                                | 91.6 ms: 1.15x slower                                                  |
| telco                    | 7.27 ms                                                | 8.45 ms: 1.16x slower                                                  |
| pickle_dict              | 29.6 us                                                | 34.6 us: 1.17x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 7.09 ms: 1.20x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                           |

Benchmark hidden because not significant (2): async_generators, regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240429-3.13.0a6+-59ac30f/bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: 1.10x
# Results vs. 3.10.4

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 752e183
- commit date: 2024-03-31
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 269 ms: 1.29x faster                                   |
| chameleon      | 9.68 ms                                                | 6.85 ms: 1.41x faster                                  |
| docutils       | 3.30 sec                                               | 2.76 sec: 1.19x faster                                 |
| html5lib       | 88.9 ms                                                | 67.0 ms: 1.33x faster                                  |
| tornado_http   | 136 ms                                                 | 95.0 ms: 1.43x faster                                  |
| Geometric mean | (ref)                                                  | 1.33x faster                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_memoization  | 870 ms                                                 | 448 ms: 1.94x faster                                   |
| async_tree_io           | 1.77 sec                                               | 934 ms: 1.89x faster                                   |
| async_tree_none         | 728 ms                                                 | 386 ms: 1.89x faster                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 596 ms: 1.71x faster                                   |
| Geometric mean          | (ref)                                                  | 1.85x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| nbody          | 154 ms                                                 | 89.5 ms: 1.72x faster                                  |
| float          | 117 ms                                                 | 77.2 ms: 1.52x faster                                  |
| pidigits       | 191 ms                                                 | 190 ms: 1.01x faster                                   |
| Geometric mean | (ref)                                                  | 1.38x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.41x faster                                   |
| regex_v8       | 27.8 ms                                                | 26.2 ms: 1.06x faster                                  |
| regex_dna      | 227 ms                                                 | 222 ms: 1.02x faster                                   |
| regex_effbot   | 3.63 ms                                                | 3.76 ms: 1.03x slower                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 303 us: 1.60x faster                                   |
| unpickle_pure_python | 331 us                                                 | 220 us: 1.51x faster                                   |
| tomli_loads          | 3.14 sec                                               | 2.22 sec: 1.41x faster                                 |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.36x faster                                  |
| xml_etree_process    | 79.1 ms                                                | 59.9 ms: 1.32x faster                                  |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                  |
| json_loads           | 31.2 us                                                | 28.6 us: 1.09x faster                                  |
| xml_etree_iterparse  | 115 ms                                                 | 108 ms: 1.07x faster                                   |
| xml_etree_parse      | 168 ms                                                 | 163 ms: 1.03x faster                                   |
| pickle_list          | 5.08 us                                                | 4.96 us: 1.02x faster                                  |
| unpickle_list        | 5.20 us                                                | 5.13 us: 1.01x faster                                  |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                  |
| pickle_dict          | 29.6 us                                                | 33.6 us: 1.13x slower                                  |
| unpickle             | 14.4 us                                                | 18.5 us: 1.28x slower                                  |
| Geometric mean       | (ref)                                                  | 1.13x faster                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.37x faster                                  |
| python_startup_no_site | 5.93 ms                                                | 8.99 ms: 1.52x slower                                  |
| Geometric mean         | (ref)                                                  | 1.05x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.9 ms: 1.50x faster                                  |
| django_template | 48.2 ms                                                | 34.2 ms: 1.41x faster                                  |
| genshi_text     | 31.8 ms                                                | 24.3 ms: 1.31x faster                                  |
| genshi_xml      | 66.0 ms                                                | 52.6 ms: 1.25x faster                                  |
| Geometric mean  | (ref)                                                  | 1.37x faster                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 112 us: 4.84x faster                                   |
| generators               | 80.1 ms                                                | 29.8 ms: 2.69x faster                                  |
| deltablue                | 7.91 ms                                                | 3.21 ms: 2.47x faster                                  |
| pylint                   | 551 ms                                                 | 280 ms: 1.97x faster                                   |
| async_tree_memoization   | 870 ms                                                 | 448 ms: 1.94x faster                                   |
| chaos                    | 115 ms                                                 | 60.4 ms: 1.91x faster                                  |
| raytrace                 | 507 ms                                                 | 268 ms: 1.89x faster                                   |
| async_tree_io            | 1.77 sec                                               | 934 ms: 1.89x faster                                   |
| logging_silent           | 190 ns                                                 | 100 ns: 1.89x faster                                   |
| async_tree_none          | 728 ms                                                 | 386 ms: 1.89x faster                                   |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                   |
| richards_super           | 94.7 ms                                                | 52.6 ms: 1.80x faster                                  |
| crypto_pyaes             | 128 ms                                                 | 72.1 ms: 1.77x faster                                  |
| scimark_sor              | 220 ms                                                 | 124 ms: 1.77x faster                                   |
| comprehensions           | 28.8 us                                                | 16.4 us: 1.75x faster                                  |
| scimark_monte_carlo      | 118 ms                                                 | 67.6 ms: 1.75x faster                                  |
| richards                 | 79.3 ms                                                | 45.9 ms: 1.73x faster                                  |
| go                       | 240 ms                                                 | 140 ms: 1.72x faster                                   |
| nbody                    | 154 ms                                                 | 89.5 ms: 1.72x faster                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 596 ms: 1.71x faster                                   |
| sqlglot_parse            | 2.17 ms                                                | 1.28 ms: 1.69x faster                                  |
| hexiom                   | 10.4 ms                                                | 6.18 ms: 1.68x faster                                  |
| sqlglot_transpile        | 2.57 ms                                                | 1.59 ms: 1.62x faster                                  |
| pickle_pure_python       | 484 us                                                 | 303 us: 1.60x faster                                   |
| pyflate                  | 716 ms                                                 | 460 ms: 1.56x faster                                   |
| deepcopy_memo            | 58.5 us                                                | 38.3 us: 1.53x faster                                  |
| spectral_norm            | 170 ms                                                 | 112 ms: 1.52x faster                                   |
| float                    | 117 ms                                                 | 77.2 ms: 1.52x faster                                  |
| unpickle_pure_python     | 331 us                                                 | 220 us: 1.51x faster                                   |
| scimark_lu               | 176 ms                                                 | 117 ms: 1.51x faster                                   |
| mako                     | 16.3 ms                                                | 10.9 ms: 1.50x faster                                  |
| coroutines               | 35.1 ms                                                | 23.5 ms: 1.49x faster                                  |
| tornado_http             | 136 ms                                                 | 95.0 ms: 1.43x faster                                  |
| chameleon                | 9.68 ms                                                | 6.85 ms: 1.41x faster                                  |
| tomli_loads              | 3.14 sec                                               | 2.22 sec: 1.41x faster                                 |
| django_template          | 48.2 ms                                                | 34.2 ms: 1.41x faster                                  |
| regex_compile            | 188 ms                                                 | 134 ms: 1.41x faster                                   |
| logging_simple           | 8.30 us                                                | 5.90 us: 1.41x faster                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.83 sec: 1.40x faster                                 |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.40x faster                                 |
| logging_format           | 9.09 us                                                | 6.56 us: 1.39x faster                                  |
| pprint_safe_repr         | 1.02 sec                                               | 735 ms: 1.39x faster                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.71 ms: 1.37x faster                                  |
| fannkuch                 | 532 ms                                                 | 387 ms: 1.37x faster                                   |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.37x faster                                  |
| deepcopy                 | 479 us                                                 | 353 us: 1.36x faster                                   |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.36x faster                                  |
| nqueens                  | 106 ms                                                 | 79.6 ms: 1.33x faster                                  |
| html5lib                 | 88.9 ms                                                | 67.0 ms: 1.33x faster                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.15 us: 1.32x faster                                  |
| xml_etree_process        | 79.1 ms                                                | 59.9 ms: 1.32x faster                                  |
| thrift                   | 1.07 ms                                                | 816 us: 1.31x faster                                   |
| genshi_text              | 31.8 ms                                                | 24.3 ms: 1.31x faster                                  |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                   |
| 2to3                     | 348 ms                                                 | 269 ms: 1.29x faster                                   |
| pycparser                | 1.58 sec                                               | 1.22 sec: 1.29x faster                                 |
| sympy_integrate          | 25.8 ms                                                | 20.0 ms: 1.29x faster                                  |
| sympy_sum                | 196 ms                                                 | 154 ms: 1.28x faster                                   |
| sympy_str                | 346 ms                                                 | 274 ms: 1.26x faster                                   |
| sqlglot_optimize         | 69.2 ms                                                | 54.8 ms: 1.26x faster                                  |
| genshi_xml               | 66.0 ms                                                | 52.6 ms: 1.25x faster                                  |
| dulwich_log              | 84.3 ms                                                | 67.6 ms: 1.25x faster                                  |
| scimark_fft              | 466 ms                                                 | 381 ms: 1.22x faster                                   |
| aiohttp                  | 1.44 ms                                                | 1.18 ms: 1.22x faster                                  |
| sympy_expand             | 566 ms                                                 | 464 ms: 1.22x faster                                   |
| mypy2                    | 894 ms                                                 | 737 ms: 1.21x faster                                   |
| djangocms                | 38.4 us                                                | 31.9 us: 1.21x faster                                  |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                   |
| gunicorn                 | 1.53 ms                                                | 1.28 ms: 1.20x faster                                  |
| docutils                 | 3.30 sec                                               | 2.76 sec: 1.19x faster                                 |
| bench_thread_pool        | 986 us                                                 | 830 us: 1.19x faster                                   |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                  |
| unpack_sequence          | 60.0 ns                                                | 53.9 ns: 1.11x faster                                  |
| meteor_contest           | 120 ms                                                 | 108 ms: 1.10x faster                                   |
| mdp                      | 2.85 sec                                               | 2.60 sec: 1.10x faster                                 |
| json_loads               | 31.2 us                                                | 28.6 us: 1.09x faster                                  |
| pathlib                  | 20.5 ms                                                | 19.0 ms: 1.07x faster                                  |
| xml_etree_iterparse      | 115 ms                                                 | 108 ms: 1.07x faster                                   |
| json                     | 5.69 ms                                                | 5.33 ms: 1.07x faster                                  |
| regex_v8                 | 27.8 ms                                                | 26.2 ms: 1.06x faster                                  |
| sqlite_synth             | 3.02 us                                                | 2.90 us: 1.04x faster                                  |
| xml_etree_parse          | 168 ms                                                 | 163 ms: 1.03x faster                                   |
| pickle_list              | 5.08 us                                                | 4.96 us: 1.02x faster                                  |
| regex_dna                | 227 ms                                                 | 222 ms: 1.02x faster                                   |
| unpickle_list            | 5.20 us                                                | 5.13 us: 1.01x faster                                  |
| pidigits                 | 191 ms                                                 | 190 ms: 1.01x faster                                   |
| bench_mp_pool            | 24.0 ms                                                | 23.8 ms: 1.01x faster                                  |
| asyncio_websockets       | 559 ms                                                 | 569 ms: 1.02x slower                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.67 ms: 1.03x slower                                  |
| regex_effbot             | 3.63 ms                                                | 3.76 ms: 1.03x slower                                  |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                  |
| gc_traversal             | 3.62 ms                                                | 4.00 ms: 1.10x slower                                  |
| pickle_dict              | 29.6 us                                                | 33.6 us: 1.13x slower                                  |
| telco                    | 7.27 ms                                                | 8.54 ms: 1.17x slower                                  |
| coverage                 | 79.4 ms                                                | 97.6 ms: 1.23x slower                                  |
| unpickle                 | 14.4 us                                                | 18.5 us: 1.28x slower                                  |
| python_startup_no_site   | 5.93 ms                                                | 8.99 ms: 1.52x slower                                  |
| Geometric mean           | (ref)                                                  | 1.34x faster                                           |

Benchmark hidden because not significant (1): async_generators
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240331-3.13.0a5+-752e183/bm-20240331-linux-x86_64-python-main-3.13.0a5+-752e183.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: 1.09x
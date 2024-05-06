# Results vs. 3.10.4

- fork: python
- ref: c520bf9bdf77d43c3d5d
- machine: linux-x86_64
- commit hash: c520bf9
- commit date: 2024-04-16
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 270 ms: 1.29x faster                                                   |
| chameleon      | 9.68 ms                                                | 6.94 ms: 1.40x faster                                                  |
| docutils       | 3.30 sec                                               | 2.83 sec: 1.16x faster                                                 |
| html5lib       | 88.9 ms                                                | 67.3 ms: 1.32x faster                                                  |
| tornado_http   | 136 ms                                                 | 93.9 ms: 1.45x faster                                                  |
| Geometric mean | (ref)                                                  | 1.32x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 354 ms: 2.06x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 936 ms: 1.89x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 464 ms: 1.88x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 611 ms: 1.66x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 90.0 ms: 1.71x faster                                                  |
| float          | 117 ms                                                 | 78.7 ms: 1.49x faster                                                  |
| pidigits       | 191 ms                                                 | 206 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.33x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 136 ms: 1.39x faster                                                   |
| regex_v8       | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                  |
| regex_dna      | 227 ms                                                 | 218 ms: 1.04x faster                                                   |
| regex_effbot   | 3.63 ms                                                | 3.74 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 299 us: 1.62x faster                                                   |
| unpickle_pure_python | 331 us                                                 | 217 us: 1.52x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 60.8 ms: 1.30x faster                                                  |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 88.8 ms: 1.12x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| unpickle_list        | 5.20 us                                                | 4.99 us: 1.04x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.33 us: 1.05x slower                                                  |
| unpickle             | 14.4 us                                                | 15.2 us: 1.06x slower                                                  |
| pickle               | 10.7 us                                                | 11.8 us: 1.11x slower                                                  |
| pickle_dict          | 29.6 us                                                | 35.4 us: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.1 ms: 1.47x faster                                                  |
| genshi_text     | 31.8 ms                                                | 23.4 ms: 1.36x faster                                                  |
| django_template | 48.2 ms                                                | 35.8 ms: 1.35x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 52.1 ms: 1.27x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.36x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 115 us: 4.73x faster                                                   |
| generators               | 80.1 ms                                                | 30.9 ms: 2.59x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.26 ms: 2.43x faster                                                  |
| async_tree_none          | 728 ms                                                 | 354 ms: 2.06x faster                                                   |
| raytrace                 | 507 ms                                                 | 264 ms: 1.92x faster                                                   |
| chaos                    | 115 ms                                                 | 60.2 ms: 1.92x faster                                                  |
| async_tree_io            | 1.77 sec                                               | 936 ms: 1.89x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 464 ms: 1.88x faster                                                   |
| logging_silent           | 190 ns                                                 | 104 ns: 1.83x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 507 ms: 1.82x faster                                                   |
| scimark_sor              | 220 ms                                                 | 123 ms: 1.79x faster                                                   |
| richards_super           | 94.7 ms                                                | 53.7 ms: 1.76x faster                                                  |
| scimark_monte_carlo      | 118 ms                                                 | 68.4 ms: 1.73x faster                                                  |
| pylint                   | 551 ms                                                 | 320 ms: 1.72x faster                                                   |
| nbody                    | 154 ms                                                 | 90.0 ms: 1.71x faster                                                  |
| comprehensions           | 28.8 us                                                | 16.9 us: 1.70x faster                                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 76.3 ms: 1.68x faster                                                  |
| go                       | 240 ms                                                 | 144 ms: 1.67x faster                                                   |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 611 ms: 1.66x faster                                                   |
| richards                 | 79.3 ms                                                | 47.9 ms: 1.66x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 299 us: 1.62x faster                                                   |
| hexiom                   | 10.4 ms                                                | 6.43 ms: 1.62x faster                                                  |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                  |
| deepcopy_memo            | 58.5 us                                                | 37.7 us: 1.55x faster                                                  |
| coroutines               | 35.1 ms                                                | 22.7 ms: 1.54x faster                                                  |
| unpickle_pure_python     | 331 us                                                 | 217 us: 1.52x faster                                                   |
| pyflate                  | 716 ms                                                 | 471 ms: 1.52x faster                                                   |
| scimark_lu               | 176 ms                                                 | 117 ms: 1.51x faster                                                   |
| spectral_norm            | 170 ms                                                 | 113 ms: 1.51x faster                                                   |
| float                    | 117 ms                                                 | 78.7 ms: 1.49x faster                                                  |
| mako                     | 16.3 ms                                                | 11.1 ms: 1.47x faster                                                  |
| tornado_http             | 136 ms                                                 | 93.9 ms: 1.45x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                 |
| logging_simple           | 8.30 us                                                | 5.80 us: 1.43x faster                                                  |
| logging_format           | 9.09 us                                                | 6.40 us: 1.42x faster                                                  |
| chameleon                | 9.68 ms                                                | 6.94 ms: 1.40x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                 |
| regex_compile            | 188 ms                                                 | 136 ms: 1.39x faster                                                   |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| pycparser                | 1.58 sec                                               | 1.15 sec: 1.37x faster                                                 |
| pprint_pformat           | 2.10 sec                                               | 1.53 sec: 1.37x faster                                                 |
| fannkuch                 | 532 ms                                                 | 391 ms: 1.36x faster                                                   |
| genshi_text              | 31.8 ms                                                | 23.4 ms: 1.36x faster                                                  |
| pprint_safe_repr         | 1.02 sec                                               | 754 ms: 1.35x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                  |
| django_template          | 48.2 ms                                                | 35.8 ms: 1.35x faster                                                  |
| deepcopy                 | 479 us                                                 | 356 us: 1.35x faster                                                   |
| html5lib                 | 88.9 ms                                                | 67.3 ms: 1.32x faster                                                  |
| thrift                   | 1.07 ms                                                | 818 us: 1.31x faster                                                   |
| xml_etree_process        | 79.1 ms                                                | 60.8 ms: 1.30x faster                                                  |
| nqueens                  | 106 ms                                                 | 81.7 ms: 1.29x faster                                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.23 us: 1.29x faster                                                  |
| 2to3                     | 348 ms                                                 | 270 ms: 1.29x faster                                                   |
| sqlglot_normalize        | 143 ms                                                 | 112 ms: 1.28x faster                                                   |
| dulwich_log              | 84.3 ms                                                | 66.4 ms: 1.27x faster                                                  |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                  |
| genshi_xml               | 66.0 ms                                                | 52.1 ms: 1.27x faster                                                  |
| scimark_fft              | 466 ms                                                 | 369 ms: 1.26x faster                                                   |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.26x faster                                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.20 ms: 1.25x faster                                                  |
| sqlglot_optimize         | 69.2 ms                                                | 55.6 ms: 1.24x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                  |
| sympy_str                | 346 ms                                                 | 282 ms: 1.23x faster                                                   |
| djangocms                | 38.4 us                                                | 31.5 us: 1.22x faster                                                  |
| mypy2                    | 894 ms                                                 | 737 ms: 1.21x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                  |
| sympy_expand             | 566 ms                                                 | 475 ms: 1.19x faster                                                   |
| dask                     | 441 ms                                                 | 371 ms: 1.19x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 841 us: 1.17x faster                                                   |
| pathlib                  | 20.5 ms                                                | 17.5 ms: 1.17x faster                                                  |
| docutils                 | 3.30 sec                                               | 2.83 sec: 1.16x faster                                                 |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                  |
| xml_etree_generate       | 99.4 ms                                                | 88.8 ms: 1.12x faster                                                  |
| json                     | 5.69 ms                                                | 5.15 ms: 1.11x faster                                                  |
| mdp                      | 2.85 sec                                               | 2.60 sec: 1.09x faster                                                 |
| regex_v8                 | 27.8 ms                                                | 25.4 ms: 1.09x faster                                                  |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                   |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                   |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| unpickle_list            | 5.20 us                                                | 4.99 us: 1.04x faster                                                  |
| regex_dna                | 227 ms                                                 | 218 ms: 1.04x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.93 us: 1.03x faster                                                  |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| async_generators         | 444 ms                                                 | 445 ms: 1.00x slower                                                   |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                   |
| regex_effbot             | 3.63 ms                                                | 3.74 ms: 1.03x slower                                                  |
| pickle_list              | 5.08 us                                                | 5.33 us: 1.05x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.2 us: 1.06x slower                                                  |
| gc_traversal             | 3.62 ms                                                | 3.87 ms: 1.07x slower                                                  |
| pidigits                 | 191 ms                                                 | 206 ms: 1.08x slower                                                   |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                  |
| pickle                   | 10.7 us                                                | 11.8 us: 1.11x slower                                                  |
| telco                    | 7.27 ms                                                | 8.55 ms: 1.18x slower                                                  |
| pickle_dict              | 29.6 us                                                | 35.4 us: 1.19x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                  |
| coverage                 | 79.4 ms                                                | 98.6 ms: 1.24x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                           |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240416-3.13.0a6+-c520bf9/bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x
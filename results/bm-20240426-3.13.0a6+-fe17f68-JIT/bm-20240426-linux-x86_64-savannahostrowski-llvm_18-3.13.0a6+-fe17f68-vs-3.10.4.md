# Results vs. 3.10.4

- fork: savannahostrowski
- ref: llvm_18
- machine: linux-x86_64
- commit hash: fe17f68
- commit date: 2024-04-26
- overall geometric mean: 1.32x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 280 ms: 1.25x faster                                                 |
| chameleon      | 9.68 ms                                                | 7.16 ms: 1.35x faster                                                |
| docutils       | 3.30 sec                                               | 2.95 sec: 1.12x faster                                               |
| html5lib       | 88.9 ms                                                | 68.5 ms: 1.30x faster                                                |
| tornado_http   | 136 ms                                                 | 96.2 ms: 1.42x faster                                                |
| Geometric mean | (ref)                                                  | 1.28x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 359 ms: 2.03x faster                                                 |
| async_tree_io           | 1.77 sec                                               | 935 ms: 1.89x faster                                                 |
| async_tree_memoization  | 870 ms                                                 | 468 ms: 1.86x faster                                                 |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 620 ms: 1.64x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.85x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 90.9 ms: 1.69x faster                                                |
| float          | 117 ms                                                 | 76.5 ms: 1.53x faster                                                |
| pidigits       | 191 ms                                                 | 210 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.33x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 140 ms: 1.35x faster                                                 |
| regex_v8       | 27.8 ms                                                | 25.2 ms: 1.10x faster                                                |
| regex_dna      | 227 ms                                                 | 223 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.11x faster                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 306 us: 1.58x faster                                                 |
| tomli_loads          | 3.14 sec                                               | 2.03 sec: 1.55x faster                                               |
| unpickle_pure_python | 331 us                                                 | 231 us: 1.43x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                |
| xml_etree_process    | 79.1 ms                                                | 60.3 ms: 1.31x faster                                                |
| xml_etree_generate   | 99.4 ms                                                | 87.5 ms: 1.14x faster                                                |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                |
| xml_etree_iterparse  | 115 ms                                                 | 103 ms: 1.12x faster                                                 |
| xml_etree_parse      | 168 ms                                                 | 151 ms: 1.11x faster                                                 |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                |
| unpickle_list        | 5.20 us                                                | 5.27 us: 1.01x slower                                                |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                                |
| unpickle             | 14.4 us                                                | 16.4 us: 1.14x slower                                                |
| pickle_dict          | 29.6 us                                                | 35.0 us: 1.18x slower                                                |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                |
| python_startup_no_site | 5.93 ms                                                | 7.63 ms: 1.29x slower                                                |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.4 ms: 1.57x faster                                                |
| django_template | 48.2 ms                                                | 36.8 ms: 1.31x faster                                                |
| genshi_text     | 31.8 ms                                                | 25.7 ms: 1.24x faster                                                |
| genshi_xml      | 66.0 ms                                                | 57.2 ms: 1.15x faster                                                |
| Geometric mean  | (ref)                                                  | 1.31x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 173 us: 3.15x faster                                                 |
| generators               | 80.1 ms                                                | 30.1 ms: 2.66x faster                                                |
| deltablue                | 7.91 ms                                                | 3.89 ms: 2.03x faster                                                |
| async_tree_none          | 728 ms                                                 | 359 ms: 2.03x faster                                                 |
| richards_super           | 94.7 ms                                                | 48.5 ms: 1.95x faster                                                |
| async_tree_io            | 1.77 sec                                               | 935 ms: 1.89x faster                                                 |
| logging_silent           | 190 ns                                                 | 101 ns: 1.87x faster                                                 |
| richards                 | 79.3 ms                                                | 42.4 ms: 1.87x faster                                                |
| async_tree_memoization   | 870 ms                                                 | 468 ms: 1.86x faster                                                 |
| raytrace                 | 507 ms                                                 | 278 ms: 1.82x faster                                                 |
| chaos                    | 115 ms                                                 | 63.5 ms: 1.82x faster                                                |
| asyncio_tcp              | 922 ms                                                 | 523 ms: 1.76x faster                                                 |
| scimark_monte_carlo      | 118 ms                                                 | 67.8 ms: 1.74x faster                                                |
| crypto_pyaes             | 128 ms                                                 | 73.9 ms: 1.73x faster                                                |
| nbody                    | 154 ms                                                 | 90.9 ms: 1.69x faster                                                |
| scimark_sor              | 220 ms                                                 | 131 ms: 1.68x faster                                                 |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 620 ms: 1.64x faster                                                 |
| sqlglot_parse            | 2.17 ms                                                | 1.33 ms: 1.64x faster                                                |
| pylint                   | 551 ms                                                 | 343 ms: 1.61x faster                                                 |
| comprehensions           | 28.8 us                                                | 18.0 us: 1.60x faster                                                |
| pickle_pure_python       | 484 us                                                 | 306 us: 1.58x faster                                                 |
| mako                     | 16.3 ms                                                | 10.4 ms: 1.57x faster                                                |
| sqlglot_transpile        | 2.57 ms                                                | 1.65 ms: 1.56x faster                                                |
| spectral_norm            | 170 ms                                                 | 109 ms: 1.55x faster                                                 |
| tomli_loads              | 3.14 sec                                               | 2.03 sec: 1.55x faster                                               |
| go                       | 240 ms                                                 | 155 ms: 1.55x faster                                                 |
| float                    | 117 ms                                                 | 76.5 ms: 1.53x faster                                                |
| pyflate                  | 716 ms                                                 | 468 ms: 1.53x faster                                                 |
| hexiom                   | 10.4 ms                                                | 6.90 ms: 1.51x faster                                                |
| coroutines               | 35.1 ms                                                | 23.3 ms: 1.51x faster                                                |
| deepcopy_memo            | 58.5 us                                                | 38.9 us: 1.50x faster                                                |
| unpickle_pure_python     | 331 us                                                 | 231 us: 1.43x faster                                                 |
| fannkuch                 | 532 ms                                                 | 372 ms: 1.43x faster                                                 |
| tornado_http             | 136 ms                                                 | 96.2 ms: 1.42x faster                                                |
| logging_simple           | 8.30 us                                                | 5.89 us: 1.41x faster                                                |
| logging_format           | 9.09 us                                                | 6.52 us: 1.39x faster                                                |
| pprint_pformat           | 2.10 sec                                               | 1.52 sec: 1.38x faster                                               |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                               |
| scimark_fft              | 466 ms                                                 | 338 ms: 1.38x faster                                                 |
| pprint_safe_repr         | 1.02 sec                                               | 744 ms: 1.37x faster                                                 |
| chameleon                | 9.68 ms                                                | 7.16 ms: 1.35x faster                                                |
| regex_compile            | 188 ms                                                 | 140 ms: 1.35x faster                                                 |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.34x faster                                                |
| pycparser                | 1.58 sec                                               | 1.18 sec: 1.34x faster                                               |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                |
| scimark_lu               | 176 ms                                                 | 134 ms: 1.32x faster                                                 |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.93 ms: 1.31x faster                                                |
| xml_etree_process        | 79.1 ms                                                | 60.3 ms: 1.31x faster                                                |
| django_template          | 48.2 ms                                                | 36.8 ms: 1.31x faster                                                |
| deepcopy                 | 479 us                                                 | 367 us: 1.31x faster                                                 |
| html5lib                 | 88.9 ms                                                | 68.5 ms: 1.30x faster                                                |
| deepcopy_reduce          | 4.17 us                                                | 3.22 us: 1.30x faster                                                |
| thrift                   | 1.07 ms                                                | 828 us: 1.29x faster                                                 |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.26x faster                                                 |
| 2to3                     | 348 ms                                                 | 280 ms: 1.25x faster                                                 |
| genshi_text              | 31.8 ms                                                | 25.7 ms: 1.24x faster                                                |
| dulwich_log              | 84.3 ms                                                | 69.8 ms: 1.21x faster                                                |
| sqlglot_optimize         | 69.2 ms                                                | 57.4 ms: 1.21x faster                                                |
| djangocms                | 38.4 us                                                | 32.4 us: 1.18x faster                                                |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                |
| nqueens                  | 106 ms                                                 | 90.2 ms: 1.17x faster                                                |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                                |
| sympy_sum                | 196 ms                                                 | 168 ms: 1.17x faster                                                 |
| dask                     | 441 ms                                                 | 377 ms: 1.17x faster                                                 |
| sympy_str                | 346 ms                                                 | 297 ms: 1.17x faster                                                 |
| sympy_integrate          | 25.8 ms                                                | 22.3 ms: 1.16x faster                                                |
| pathlib                  | 20.5 ms                                                | 17.7 ms: 1.16x faster                                                |
| genshi_xml               | 66.0 ms                                                | 57.2 ms: 1.15x faster                                                |
| bench_thread_pool        | 986 us                                                 | 863 us: 1.14x faster                                                 |
| xml_etree_generate       | 99.4 ms                                                | 87.5 ms: 1.14x faster                                                |
| sympy_expand             | 566 ms                                                 | 498 ms: 1.14x faster                                                 |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                |
| xml_etree_iterparse      | 115 ms                                                 | 103 ms: 1.12x faster                                                 |
| docutils                 | 3.30 sec                                               | 2.95 sec: 1.12x faster                                               |
| xml_etree_parse          | 168 ms                                                 | 151 ms: 1.11x faster                                                 |
| mypy2                    | 894 ms                                                 | 806 ms: 1.11x faster                                                 |
| json                     | 5.69 ms                                                | 5.15 ms: 1.10x faster                                                |
| regex_v8                 | 27.8 ms                                                | 25.2 ms: 1.10x faster                                                |
| mdp                      | 2.85 sec                                               | 2.63 sec: 1.08x faster                                               |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                 |
| sqlite_synth             | 3.02 us                                                | 2.88 us: 1.05x faster                                                |
| regex_dna                | 227 ms                                                 | 223 ms: 1.01x faster                                                 |
| pickle_list              | 5.08 us                                                | 5.02 us: 1.01x faster                                                |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                 |
| unpickle_list            | 5.20 us                                                | 5.27 us: 1.01x slower                                                |
| gc_traversal             | 3.62 ms                                                | 3.79 ms: 1.05x slower                                                |
| async_generators         | 444 ms                                                 | 465 ms: 1.05x slower                                                 |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.09x slower                                                |
| pidigits                 | 191 ms                                                 | 210 ms: 1.10x slower                                                 |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                                |
| unpickle                 | 14.4 us                                                | 16.4 us: 1.14x slower                                                |
| coverage                 | 79.4 ms                                                | 92.6 ms: 1.17x slower                                                |
| telco                    | 7.27 ms                                                | 8.48 ms: 1.17x slower                                                |
| pickle_dict              | 29.6 us                                                | 35.0 us: 1.18x slower                                                |
| python_startup_no_site   | 5.93 ms                                                | 7.63 ms: 1.29x slower                                                |
| Geometric mean           | (ref)                                                  | 1.32x faster                                                         |

Benchmark hidden because not significant (2): bench_mp_pool, regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-fe17f68-JIT/bm-20240426-linux-x86_64-savannahostrowski-llvm_18-3.13.0a6+-fe17f68.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.19x
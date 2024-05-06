# Results vs. 3.10.4

- fork: python
- ref: ab6eda0ee59587e84cb4
- machine: linux-x86_64
- commit hash: ab6eda0
- commit date: 2024-04-29
- overall geometric mean: 1.06x faster
- HPT reliability: 50.79%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 361 ms: 1.03x slower                                                   |
| chameleon      | 9.68 ms                                                | 8.68 ms: 1.12x faster                                                  |
| docutils       | 3.30 sec                                               | 3.37 sec: 1.02x slower                                                 |
| html5lib       | 88.9 ms                                                | 79.8 ms: 1.11x faster                                                  |
| tornado_http   | 136 ms                                                 | 105 ms: 1.29x faster                                                   |
| Geometric mean | (ref)                                                  | 1.09x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 393 ms: 1.85x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 1.00 sec: 1.77x faster                                                 |
| async_tree_memoization  | 870 ms                                                 | 526 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 651 ms: 1.56x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.71x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 191 ms                                                 | 194 ms: 1.02x slower                                                   |
| float          | 117 ms                                                 | 122 ms: 1.04x slower                                                   |
| nbody          | 154 ms                                                 | 198 ms: 1.29x slower                                                   |
| Geometric mean | (ref)                                                  | 1.11x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.6 ms: 1.09x faster                                                  |
| regex_dna      | 227 ms                                                 | 226 ms: 1.00x faster                                                   |
| regex_effbot   | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                  |
| regex_compile  | 188 ms                                                 | 220 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 318 us: 1.52x faster                                                   |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.32x faster                                                  |
| json_loads           | 31.2 us                                                | 27.6 us: 1.13x faster                                                  |
| xml_etree_parse      | 168 ms                                                 | 151 ms: 1.11x faster                                                   |
| xml_etree_process    | 79.1 ms                                                | 74.1 ms: 1.07x faster                                                  |
| unpickle_list        | 5.20 us                                                | 5.13 us: 1.01x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.11 us: 1.01x slower                                                  |
| xml_etree_generate   | 99.4 ms                                                | 104 ms: 1.04x slower                                                   |
| unpickle             | 14.4 us                                                | 15.3 us: 1.06x slower                                                  |
| tomli_loads          | 3.14 sec                                               | 3.38 sec: 1.08x slower                                                 |
| xml_etree_iterparse  | 115 ms                                                 | 126 ms: 1.09x slower                                                   |
| pickle               | 10.7 us                                                | 12.0 us: 1.12x slower                                                  |
| pickle_dict          | 29.6 us                                                | 35.3 us: 1.19x slower                                                  |
| unpickle_pure_python | 331 us                                                 | 396 us: 1.20x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.19 ms: 1.21x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 48.2 ms                                                | 47.3 ms: 1.02x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 80.6 ms: 1.22x slower                                                  |
| genshi_text     | 31.8 ms                                                | 39.3 ms: 1.23x slower                                                  |
| mako            | 16.3 ms                                                | 20.3 ms: 1.25x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.16x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| generators               | 80.1 ms                                                | 31.8 ms: 2.52x faster                                                  |
| typing_runtime_protocols | 544 us                                                 | 217 us: 2.50x faster                                                   |
| async_tree_none          | 728 ms                                                 | 393 ms: 1.85x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 1.00 sec: 1.77x faster                                                 |
| logging_silent           | 190 ns                                                 | 108 ns: 1.76x faster                                                   |
| asyncio_tcp              | 922 ms                                                 | 530 ms: 1.74x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 526 ms: 1.66x faster                                                   |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 651 ms: 1.56x faster                                                   |
| pickle_pure_python       | 484 us                                                 | 318 us: 1.52x faster                                                   |
| deltablue                | 7.91 ms                                                | 5.41 ms: 1.46x faster                                                  |
| coroutines               | 35.1 ms                                                | 24.5 ms: 1.43x faster                                                  |
| pylint                   | 551 ms                                                 | 387 ms: 1.43x faster                                                   |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.88 sec: 1.37x faster                                                 |
| sqlglot_parse            | 2.17 ms                                                | 1.59 ms: 1.36x faster                                                  |
| raytrace                 | 507 ms                                                 | 376 ms: 1.35x faster                                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.94 ms: 1.32x faster                                                  |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.32x faster                                                  |
| tornado_http             | 136 ms                                                 | 105 ms: 1.29x faster                                                   |
| thrift                   | 1.07 ms                                                | 854 us: 1.25x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.34 us: 1.25x faster                                                  |
| scimark_sor              | 220 ms                                                 | 178 ms: 1.24x faster                                                   |
| richards_super           | 94.7 ms                                                | 78.6 ms: 1.20x faster                                                  |
| pycparser                | 1.58 sec                                               | 1.34 sec: 1.18x faster                                                 |
| logging_simple           | 8.30 us                                                | 7.08 us: 1.17x faster                                                  |
| deepcopy                 | 479 us                                                 | 409 us: 1.17x faster                                                   |
| deepcopy_memo            | 58.5 us                                                | 50.1 us: 1.17x faster                                                  |
| djangocms                | 38.4 us                                                | 33.1 us: 1.16x faster                                                  |
| logging_format           | 9.09 us                                                | 7.88 us: 1.15x faster                                                  |
| json_loads               | 31.2 us                                                | 27.6 us: 1.13x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.28 ms: 1.13x faster                                                  |
| chaos                    | 115 ms                                                 | 103 ms: 1.12x faster                                                   |
| chameleon                | 9.68 ms                                                | 8.68 ms: 1.12x faster                                                  |
| gunicorn                 | 1.53 ms                                                | 1.37 ms: 1.12x faster                                                  |
| html5lib                 | 88.9 ms                                                | 79.8 ms: 1.11x faster                                                  |
| xml_etree_parse          | 168 ms                                                 | 151 ms: 1.11x faster                                                   |
| dask                     | 441 ms                                                 | 397 ms: 1.11x faster                                                   |
| richards                 | 79.3 ms                                                | 71.6 ms: 1.11x faster                                                  |
| json                     | 5.69 ms                                                | 5.21 ms: 1.09x faster                                                  |
| dulwich_log              | 84.3 ms                                                | 77.4 ms: 1.09x faster                                                  |
| regex_v8                 | 27.8 ms                                                | 25.6 ms: 1.09x faster                                                  |
| pathlib                  | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 74.1 ms: 1.07x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 122 ms: 1.05x faster                                                   |
| sympy_sum                | 196 ms                                                 | 192 ms: 1.03x faster                                                   |
| mypy2                    | 894 ms                                                 | 874 ms: 1.02x faster                                                   |
| django_template          | 48.2 ms                                                | 47.3 ms: 1.02x faster                                                  |
| bench_thread_pool        | 986 us                                                 | 973 us: 1.01x faster                                                   |
| unpickle_list            | 5.20 us                                                | 5.13 us: 1.01x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 142 ms: 1.01x faster                                                   |
| regex_dna                | 227 ms                                                 | 226 ms: 1.00x faster                                                   |
| pickle_list              | 5.08 us                                                | 5.11 us: 1.01x slower                                                  |
| pidigits                 | 191 ms                                                 | 194 ms: 1.02x slower                                                   |
| asyncio_websockets       | 559 ms                                                 | 568 ms: 1.02x slower                                                   |
| docutils                 | 3.30 sec                                               | 3.37 sec: 1.02x slower                                                 |
| regex_effbot             | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                  |
| sqlite_synth             | 3.02 us                                                | 3.11 us: 1.03x slower                                                  |
| sympy_expand             | 566 ms                                                 | 585 ms: 1.03x slower                                                   |
| 2to3                     | 348 ms                                                 | 361 ms: 1.03x slower                                                   |
| sympy_str                | 346 ms                                                 | 360 ms: 1.04x slower                                                   |
| xml_etree_generate       | 99.4 ms                                                | 104 ms: 1.04x slower                                                   |
| float                    | 117 ms                                                 | 122 ms: 1.04x slower                                                   |
| sqlglot_optimize         | 69.2 ms                                                | 73.5 ms: 1.06x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.3 us: 1.06x slower                                                  |
| sympy_integrate          | 25.8 ms                                                | 27.7 ms: 1.07x slower                                                  |
| tomli_loads              | 3.14 sec                                               | 3.38 sec: 1.08x slower                                                 |
| go                       | 240 ms                                                 | 260 ms: 1.08x slower                                                   |
| gc_traversal             | 3.62 ms                                                | 3.93 ms: 1.08x slower                                                  |
| xml_etree_iterparse      | 115 ms                                                 | 126 ms: 1.09x slower                                                   |
| mdp                      | 2.85 sec                                               | 3.13 sec: 1.10x slower                                                 |
| create_gc_cycles         | 1.62 ms                                                | 1.81 ms: 1.11x slower                                                  |
| async_generators         | 444 ms                                                 | 496 ms: 1.12x slower                                                   |
| pickle                   | 10.7 us                                                | 12.0 us: 1.12x slower                                                  |
| scimark_monte_carlo      | 118 ms                                                 | 134 ms: 1.13x slower                                                   |
| scimark_lu               | 176 ms                                                 | 201 ms: 1.14x slower                                                   |
| pyflate                  | 716 ms                                                 | 828 ms: 1.16x slower                                                   |
| coverage                 | 79.4 ms                                                | 92.7 ms: 1.17x slower                                                  |
| regex_compile            | 188 ms                                                 | 220 ms: 1.17x slower                                                   |
| pickle_dict              | 29.6 us                                                | 35.3 us: 1.19x slower                                                  |
| meteor_contest           | 120 ms                                                 | 143 ms: 1.19x slower                                                   |
| unpickle_pure_python     | 331 us                                                 | 396 us: 1.20x slower                                                   |
| python_startup_no_site   | 5.93 ms                                                | 7.19 ms: 1.21x slower                                                  |
| genshi_xml               | 66.0 ms                                                | 80.6 ms: 1.22x slower                                                  |
| genshi_text              | 31.8 ms                                                | 39.3 ms: 1.23x slower                                                  |
| spectral_norm            | 170 ms                                                 | 211 ms: 1.24x slower                                                   |
| mako                     | 16.3 ms                                                | 20.3 ms: 1.25x slower                                                  |
| pprint_pformat           | 2.10 sec                                               | 2.65 sec: 1.26x slower                                                 |
| pprint_safe_repr         | 1.02 sec                                               | 1.28 sec: 1.26x slower                                                 |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 8.26 ms: 1.28x slower                                                  |
| scimark_fft              | 466 ms                                                 | 596 ms: 1.28x slower                                                   |
| nbody                    | 154 ms                                                 | 198 ms: 1.29x slower                                                   |
| comprehensions           | 28.8 us                                                | 37.2 us: 1.29x slower                                                  |
| fannkuch                 | 532 ms                                                 | 693 ms: 1.30x slower                                                   |
| telco                    | 7.27 ms                                                | 9.64 ms: 1.33x slower                                                  |
| nqueens                  | 106 ms                                                 | 151 ms: 1.43x slower                                                   |
| hexiom                   | 10.4 ms                                                | 15.0 ms: 1.45x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240429-3.13.0a6+-ab6eda0-PYTHON_UOPS/bm-20240429-linux-x86_64-python-ab6eda0ee59587e84cb4-3.13.0a6+-ab6eda0.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 50.79% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x
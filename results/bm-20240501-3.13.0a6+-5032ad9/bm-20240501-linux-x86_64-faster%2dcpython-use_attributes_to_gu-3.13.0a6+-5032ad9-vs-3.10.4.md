# Results vs. 3.10.4

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 5032ad9
- commit date: 2024-05-01
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 272 ms: 1.28x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.26 ms: 1.33x faster                                                            |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                           |
| html5lib       | 88.9 ms                                                | 68.6 ms: 1.30x faster                                                            |
| tornado_http   | 136 ms                                                 | 93.6 ms: 1.46x faster                                                            |
| Geometric mean | (ref)                                                  | 1.30x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 356 ms: 2.05x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 920 ms: 1.92x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 468 ms: 1.86x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 613 ms: 1.66x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.3 ms: 1.74x faster                                                            |
| float          | 117 ms                                                 | 77.9 ms: 1.50x faster                                                            |
| pidigits       | 191 ms                                                 | 191 ms: 1.00x faster                                                             |
| Geometric mean | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.40x faster                                                             |
| regex_v8       | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                            |
| regex_dna      | 227 ms                                                 | 230 ms: 1.02x slower                                                             |
| regex_effbot   | 3.63 ms                                                | 3.89 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 311 us: 1.56x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 217 us: 1.52x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 61.8 ms: 1.28x faster                                                            |
| xml_etree_generate   | 99.4 ms                                                | 89.0 ms: 1.12x faster                                                            |
| json_loads           | 31.2 us                                                | 28.4 us: 1.10x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| xml_etree_parse      | 168 ms                                                 | 158 ms: 1.06x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.05 us: 1.00x faster                                                            |
| unpickle_list        | 5.20 us                                                | 5.28 us: 1.02x slower                                                            |
| unpickle             | 14.4 us                                                | 15.3 us: 1.06x slower                                                            |
| pickle               | 10.7 us                                                | 12.0 us: 1.12x slower                                                            |
| pickle_dict          | 29.6 us                                                | 34.7 us: 1.17x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.09 ms: 1.19x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.5 ms: 1.43x faster                                                            |
| django_template | 48.2 ms                                                | 34.6 ms: 1.39x faster                                                            |
| genshi_text     | 31.8 ms                                                | 23.0 ms: 1.38x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 51.4 ms: 1.28x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.37x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 164 us: 3.31x faster                                                             |
| generators               | 80.1 ms                                                | 29.1 ms: 2.75x faster                                                            |
| deltablue                | 7.91 ms                                                | 3.22 ms: 2.46x faster                                                            |
| async_tree_none          | 728 ms                                                 | 356 ms: 2.05x faster                                                             |
| logging_silent           | 190 ns                                                 | 98.1 ns: 1.93x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 920 ms: 1.92x faster                                                             |
| chaos                    | 115 ms                                                 | 60.6 ms: 1.90x faster                                                            |
| raytrace                 | 507 ms                                                 | 267 ms: 1.90x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 468 ms: 1.86x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 511 ms: 1.80x faster                                                             |
| comprehensions           | 28.8 us                                                | 16.4 us: 1.75x faster                                                            |
| nbody                    | 154 ms                                                 | 88.3 ms: 1.74x faster                                                            |
| richards_super           | 94.7 ms                                                | 54.6 ms: 1.73x faster                                                            |
| pylint                   | 551 ms                                                 | 319 ms: 1.73x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 75.6 ms: 1.69x faster                                                            |
| hexiom                   | 10.4 ms                                                | 6.16 ms: 1.69x faster                                                            |
| scimark_sor              | 220 ms                                                 | 131 ms: 1.68x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 70.5 ms: 1.68x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.29 ms: 1.68x faster                                                            |
| go                       | 240 ms                                                 | 144 ms: 1.66x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 613 ms: 1.66x faster                                                             |
| richards                 | 79.3 ms                                                | 48.3 ms: 1.64x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.60 ms: 1.61x faster                                                            |
| coroutines               | 35.1 ms                                                | 22.0 ms: 1.59x faster                                                            |
| pickle_pure_python       | 484 us                                                 | 311 us: 1.56x faster                                                             |
| spectral_norm            | 170 ms                                                 | 110 ms: 1.55x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 38.0 us: 1.54x faster                                                            |
| unpickle_pure_python     | 331 us                                                 | 217 us: 1.52x faster                                                             |
| float                    | 117 ms                                                 | 77.9 ms: 1.50x faster                                                            |
| scimark_lu               | 176 ms                                                 | 118 ms: 1.50x faster                                                             |
| pyflate                  | 716 ms                                                 | 480 ms: 1.49x faster                                                             |
| tornado_http             | 136 ms                                                 | 93.6 ms: 1.46x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.17 sec: 1.45x faster                                                           |
| logging_simple           | 8.30 us                                                | 5.80 us: 1.43x faster                                                            |
| mako                     | 16.3 ms                                                | 11.5 ms: 1.43x faster                                                            |
| logging_format           | 9.09 us                                                | 6.39 us: 1.42x faster                                                            |
| regex_compile            | 188 ms                                                 | 134 ms: 1.40x faster                                                             |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                                           |
| django_template          | 48.2 ms                                                | 34.6 ms: 1.39x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| genshi_text              | 31.8 ms                                                | 23.0 ms: 1.38x faster                                                            |
| pprint_pformat           | 2.10 sec                                               | 1.55 sec: 1.35x faster                                                           |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 758 ms: 1.34x faster                                                             |
| chameleon                | 9.68 ms                                                | 7.26 ms: 1.33x faster                                                            |
| nqueens                  | 106 ms                                                 | 79.6 ms: 1.33x faster                                                            |
| deepcopy                 | 479 us                                                 | 361 us: 1.33x faster                                                             |
| fannkuch                 | 532 ms                                                 | 403 ms: 1.32x faster                                                             |
| thrift                   | 1.07 ms                                                | 814 us: 1.32x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 110 ms: 1.30x faster                                                             |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.30x faster                                                           |
| html5lib                 | 88.9 ms                                                | 68.6 ms: 1.30x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.22 us: 1.29x faster                                                            |
| dulwich_log              | 84.3 ms                                                | 65.6 ms: 1.28x faster                                                            |
| genshi_xml               | 66.0 ms                                                | 51.4 ms: 1.28x faster                                                            |
| 2to3                     | 348 ms                                                 | 272 ms: 1.28x faster                                                             |
| xml_etree_process        | 79.1 ms                                                | 61.8 ms: 1.28x faster                                                            |
| sympy_sum                | 196 ms                                                 | 155 ms: 1.27x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 20.3 ms: 1.27x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 54.9 ms: 1.26x faster                                                            |
| sympy_str                | 346 ms                                                 | 278 ms: 1.24x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.21 ms: 1.24x faster                                                            |
| scimark_fft              | 466 ms                                                 | 377 ms: 1.24x faster                                                             |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                            |
| mypy2                    | 894 ms                                                 | 738 ms: 1.21x faster                                                             |
| djangocms                | 38.4 us                                                | 31.9 us: 1.21x faster                                                            |
| sympy_expand             | 566 ms                                                 | 470 ms: 1.20x faster                                                             |
| gunicorn                 | 1.53 ms                                                | 1.28 ms: 1.20x faster                                                            |
| dask                     | 441 ms                                                 | 368 ms: 1.20x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 824 us: 1.20x faster                                                             |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                                           |
| pathlib                  | 20.5 ms                                                | 17.6 ms: 1.17x faster                                                            |
| xml_etree_generate       | 99.4 ms                                                | 89.0 ms: 1.12x faster                                                            |
| json_loads               | 31.2 us                                                | 28.4 us: 1.10x faster                                                            |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.08x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 25.8 ms: 1.08x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 158 ms: 1.06x faster                                                             |
| json                     | 5.69 ms                                                | 5.37 ms: 1.06x faster                                                            |
| mdp                      | 2.85 sec                                               | 2.72 sec: 1.05x faster                                                           |
| sqlite_synth             | 3.02 us                                                | 2.95 us: 1.03x faster                                                            |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| pickle_list              | 5.08 us                                                | 5.05 us: 1.00x faster                                                            |
| pidigits                 | 191 ms                                                 | 191 ms: 1.00x faster                                                             |
| async_generators         | 444 ms                                                 | 445 ms: 1.00x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                             |
| unpickle_list            | 5.20 us                                                | 5.28 us: 1.02x slower                                                            |
| regex_dna                | 227 ms                                                 | 230 ms: 1.02x slower                                                             |
| unpickle                 | 14.4 us                                                | 15.3 us: 1.06x slower                                                            |
| regex_effbot             | 3.63 ms                                                | 3.89 ms: 1.07x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.98 ms: 1.10x slower                                                            |
| pickle                   | 10.7 us                                                | 12.0 us: 1.12x slower                                                            |
| coverage                 | 79.4 ms                                                | 93.0 ms: 1.17x slower                                                            |
| pickle_dict              | 29.6 us                                                | 34.7 us: 1.17x slower                                                            |
| telco                    | 7.27 ms                                                | 8.53 ms: 1.17x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.09 ms: 1.19x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                                     |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240501-3.13.0a6+-5032ad9/bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: 1.10x
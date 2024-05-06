# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 313 ms: 1.11x faster                                                   |
| chameleon      | 9.68 ms                                                | 7.93 ms: 1.22x faster                                                  |
| docutils       | 3.30 sec                                               | 3.14 sec: 1.05x faster                                                 |
| html5lib       | 88.9 ms                                                | 73.7 ms: 1.21x faster                                                  |
| tornado_http   | 136 ms                                                 | 103 ms: 1.32x faster                                                   |
| Geometric mean | (ref)                                                  | 1.18x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 380 ms: 1.92x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 996 ms: 1.78x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 501 ms: 1.74x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 639 ms: 1.59x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.75x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 117 ms: 1.31x faster                                                   |
| float          | 117 ms                                                 | 91.6 ms: 1.28x faster                                                  |
| pidigits       | 191 ms                                                 | 196 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                  | 1.18x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                  |
| regex_dna      | 227 ms                                                 | 219 ms: 1.04x faster                                                   |
| regex_compile  | 188 ms                                                 | 190 ms: 1.01x slower                                                   |
| regex_effbot   | 3.63 ms                                                | 3.80 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 317 us: 1.53x faster                                                   |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 64.9 ms: 1.22x faster                                                  |
| tomli_loads          | 3.14 sec                                               | 2.63 sec: 1.19x faster                                                 |
| json_loads           | 31.2 us                                                | 27.5 us: 1.14x faster                                                  |
| xml_etree_parse      | 168 ms                                                 | 152 ms: 1.10x faster                                                   |
| xml_etree_iterparse  | 115 ms                                                 | 110 ms: 1.05x faster                                                   |
| xml_etree_generate   | 99.4 ms                                                | 95.6 ms: 1.04x faster                                                  |
| unpickle_list        | 5.20 us                                                | 5.12 us: 1.02x faster                                                  |
| unpickle_pure_python | 331 us                                                 | 334 us: 1.01x slower                                                   |
| pickle_list          | 5.08 us                                                | 5.15 us: 1.01x slower                                                  |
| pickle               | 10.7 us                                                | 11.7 us: 1.09x slower                                                  |
| unpickle             | 14.4 us                                                | 15.9 us: 1.11x slower                                                  |
| pickle_dict          | 29.6 us                                                | 34.5 us: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 13.4 ms: 1.22x faster                                                  |
| genshi_text     | 31.8 ms                                                | 26.2 ms: 1.21x faster                                                  |
| django_template | 48.2 ms                                                | 43.2 ms: 1.12x faster                                                  |
| genshi_xml      | 66.0 ms                                                | 62.5 ms: 1.06x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.15x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 124 us: 4.38x faster                                                   |
| generators               | 80.1 ms                                                | 30.3 ms: 2.64x faster                                                  |
| async_tree_none          | 728 ms                                                 | 380 ms: 1.92x faster                                                   |
| deltablue                | 7.91 ms                                                | 4.33 ms: 1.83x faster                                                  |
| asyncio_tcp              | 922 ms                                                 | 519 ms: 1.78x faster                                                   |
| async_tree_io            | 1.77 sec                                               | 996 ms: 1.78x faster                                                   |
| logging_silent           | 190 ns                                                 | 107 ns: 1.77x faster                                                   |
| async_tree_memoization   | 870 ms                                                 | 501 ms: 1.74x faster                                                   |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 639 ms: 1.59x faster                                                   |
| pylint                   | 551 ms                                                 | 348 ms: 1.58x faster                                                   |
| coroutines               | 35.1 ms                                                | 22.3 ms: 1.57x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 317 us: 1.53x faster                                                   |
| richards_super           | 94.7 ms                                                | 65.7 ms: 1.44x faster                                                  |
| raytrace                 | 507 ms                                                 | 352 ms: 1.44x faster                                                   |
| chaos                    | 115 ms                                                 | 80.8 ms: 1.43x faster                                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.54 ms: 1.41x faster                                                  |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                  |
| sqlglot_transpile        | 2.57 ms                                                | 1.87 ms: 1.38x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.38x faster                                                 |
| crypto_pyaes             | 128 ms                                                 | 93.0 ms: 1.37x faster                                                  |
| richards                 | 79.3 ms                                                | 58.3 ms: 1.36x faster                                                  |
| scimark_sor              | 220 ms                                                 | 162 ms: 1.36x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                  |
| tornado_http             | 136 ms                                                 | 103 ms: 1.32x faster                                                   |
| nbody                    | 154 ms                                                 | 117 ms: 1.31x faster                                                   |
| scimark_monte_carlo      | 118 ms                                                 | 92.3 ms: 1.28x faster                                                  |
| float                    | 117 ms                                                 | 91.6 ms: 1.28x faster                                                  |
| thrift                   | 1.07 ms                                                | 848 us: 1.26x faster                                                   |
| logging_simple           | 8.30 us                                                | 6.69 us: 1.24x faster                                                  |
| go                       | 240 ms                                                 | 194 ms: 1.24x faster                                                   |
| logging_format           | 9.09 us                                                | 7.41 us: 1.23x faster                                                  |
| deepcopy                 | 479 us                                                 | 392 us: 1.22x faster                                                   |
| chameleon                | 9.68 ms                                                | 7.93 ms: 1.22x faster                                                  |
| deepcopy_reduce          | 4.17 us                                                | 3.42 us: 1.22x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 64.9 ms: 1.22x faster                                                  |
| mako                     | 16.3 ms                                                | 13.4 ms: 1.22x faster                                                  |
| genshi_text              | 31.8 ms                                                | 26.2 ms: 1.21x faster                                                  |
| pycparser                | 1.58 sec                                               | 1.31 sec: 1.21x faster                                                 |
| html5lib                 | 88.9 ms                                                | 73.7 ms: 1.21x faster                                                  |
| deepcopy_memo            | 58.5 us                                                | 48.9 us: 1.20x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.63 sec: 1.19x faster                                                 |
| djangocms                | 38.4 us                                                | 33.1 us: 1.16x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.25 ms: 1.15x faster                                                  |
| dask                     | 441 ms                                                 | 384 ms: 1.15x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.34 ms: 1.14x faster                                                  |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.67 ms: 1.14x faster                                                  |
| json_loads               | 31.2 us                                                | 27.5 us: 1.14x faster                                                  |
| pyflate                  | 716 ms                                                 | 633 ms: 1.13x faster                                                   |
| comprehensions           | 28.8 us                                                | 25.6 us: 1.12x faster                                                  |
| regex_v8                 | 27.8 ms                                                | 24.8 ms: 1.12x faster                                                  |
| dulwich_log              | 84.3 ms                                                | 75.4 ms: 1.12x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 128 ms: 1.12x faster                                                   |
| django_template          | 48.2 ms                                                | 43.2 ms: 1.12x faster                                                  |
| 2to3                     | 348 ms                                                 | 313 ms: 1.11x faster                                                   |
| pathlib                  | 20.5 ms                                                | 18.4 ms: 1.11x faster                                                  |
| xml_etree_parse          | 168 ms                                                 | 152 ms: 1.10x faster                                                   |
| json                     | 5.69 ms                                                | 5.17 ms: 1.10x faster                                                  |
| mypy2                    | 894 ms                                                 | 819 ms: 1.09x faster                                                   |
| sympy_integrate          | 25.8 ms                                                | 23.8 ms: 1.09x faster                                                  |
| sympy_sum                | 196 ms                                                 | 181 ms: 1.09x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 910 us: 1.08x faster                                                   |
| genshi_xml               | 66.0 ms                                                | 62.5 ms: 1.06x faster                                                  |
| xml_etree_iterparse      | 115 ms                                                 | 110 ms: 1.05x faster                                                   |
| docutils                 | 3.30 sec                                               | 3.14 sec: 1.05x faster                                                 |
| sympy_str                | 346 ms                                                 | 331 ms: 1.05x faster                                                   |
| sqlglot_optimize         | 69.2 ms                                                | 66.2 ms: 1.04x faster                                                  |
| xml_etree_generate       | 99.4 ms                                                | 95.6 ms: 1.04x faster                                                  |
| regex_dna                | 227 ms                                                 | 219 ms: 1.04x faster                                                   |
| sympy_expand             | 566 ms                                                 | 548 ms: 1.03x faster                                                   |
| scimark_lu               | 176 ms                                                 | 172 ms: 1.03x faster                                                   |
| unpickle_list            | 5.20 us                                                | 5.12 us: 1.02x faster                                                  |
| hexiom                   | 10.4 ms                                                | 10.3 ms: 1.01x faster                                                  |
| gc_traversal             | 3.62 ms                                                | 3.64 ms: 1.00x slower                                                  |
| regex_compile            | 188 ms                                                 | 190 ms: 1.01x slower                                                   |
| unpickle_pure_python     | 331 us                                                 | 334 us: 1.01x slower                                                   |
| fannkuch                 | 532 ms                                                 | 537 ms: 1.01x slower                                                   |
| pickle_list              | 5.08 us                                                | 5.15 us: 1.01x slower                                                  |
| asyncio_websockets       | 559 ms                                                 | 568 ms: 1.02x slower                                                   |
| sqlite_synth             | 3.02 us                                                | 3.08 us: 1.02x slower                                                  |
| mdp                      | 2.85 sec                                               | 2.93 sec: 1.03x slower                                                 |
| meteor_contest           | 120 ms                                                 | 123 ms: 1.03x slower                                                   |
| pidigits                 | 191 ms                                                 | 196 ms: 1.03x slower                                                   |
| regex_effbot             | 3.63 ms                                                | 3.80 ms: 1.05x slower                                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                  |
| async_generators         | 444 ms                                                 | 485 ms: 1.09x slower                                                   |
| pickle                   | 10.7 us                                                | 11.7 us: 1.09x slower                                                  |
| pprint_safe_repr         | 1.02 sec                                               | 1.12 sec: 1.10x slower                                                 |
| pprint_pformat           | 2.10 sec                                               | 2.31 sec: 1.10x slower                                                 |
| unpickle                 | 14.4 us                                                | 15.9 us: 1.11x slower                                                  |
| pickle_dict              | 29.6 us                                                | 34.5 us: 1.16x slower                                                  |
| scimark_fft              | 466 ms                                                 | 543 ms: 1.17x slower                                                   |
| nqueens                  | 106 ms                                                 | 125 ms: 1.18x slower                                                   |
| spectral_norm            | 170 ms                                                 | 203 ms: 1.19x slower                                                   |
| python_startup_no_site   | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                  |
| coverage                 | 79.4 ms                                                | 96.9 ms: 1.22x slower                                                  |
| telco                    | 7.27 ms                                                | 9.47 ms: 1.30x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.18x faster                                                           |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.11x
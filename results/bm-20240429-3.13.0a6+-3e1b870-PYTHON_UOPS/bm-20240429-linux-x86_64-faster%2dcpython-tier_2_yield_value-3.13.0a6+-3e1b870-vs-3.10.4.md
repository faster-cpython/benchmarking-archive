# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_yield_value
- machine: linux-x86_64
- commit hash: 3e1b870
- commit date: 2024-04-29
- overall geometric mean: 1.06x faster
- HPT reliability: 51.51%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 361 ms: 1.04x slower                                                           |
| chameleon      | 9.68 ms                                                | 8.81 ms: 1.10x faster                                                          |
| docutils       | 3.30 sec                                               | 3.37 sec: 1.02x slower                                                         |
| html5lib       | 88.9 ms                                                | 81.2 ms: 1.09x faster                                                          |
| tornado_http   | 136 ms                                                 | 105 ms: 1.30x faster                                                           |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 393 ms: 1.85x faster                                                           |
| async_tree_io           | 1.77 sec                                               | 1.00 sec: 1.77x faster                                                         |
| async_tree_memoization  | 870 ms                                                 | 526 ms: 1.65x faster                                                           |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 658 ms: 1.55x faster                                                           |
| Geometric mean          | (ref)                                                  | 1.70x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                 | 194 ms: 1.01x slower                                                           |
| float          | 117 ms                                                 | 129 ms: 1.10x slower                                                           |
| nbody          | 154 ms                                                 | 197 ms: 1.28x slower                                                           |
| Geometric mean | (ref)                                                  | 1.13x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 26.4 ms: 1.05x faster                                                          |
| regex_dna      | 227 ms                                                 | 226 ms: 1.00x faster                                                           |
| regex_effbot   | 3.63 ms                                                | 3.74 ms: 1.03x slower                                                          |
| regex_compile  | 188 ms                                                 | 223 ms: 1.18x slower                                                           |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 317 us: 1.53x faster                                                           |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                          |
| json_loads           | 31.2 us                                                | 27.5 us: 1.13x faster                                                          |
| xml_etree_parse      | 168 ms                                                 | 154 ms: 1.09x faster                                                           |
| xml_etree_process    | 79.1 ms                                                | 74.0 ms: 1.07x faster                                                          |
| pickle_list          | 5.08 us                                                | 5.13 us: 1.01x slower                                                          |
| unpickle_list        | 5.20 us                                                | 5.33 us: 1.02x slower                                                          |
| xml_etree_generate   | 99.4 ms                                                | 103 ms: 1.03x slower                                                           |
| unpickle             | 14.4 us                                                | 14.9 us: 1.04x slower                                                          |
| tomli_loads          | 3.14 sec                                               | 3.37 sec: 1.07x slower                                                         |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                          |
| xml_etree_iterparse  | 115 ms                                                 | 127 ms: 1.10x slower                                                           |
| pickle_dict          | 29.6 us                                                | 35.1 us: 1.19x slower                                                          |
| unpickle_pure_python | 331 us                                                 | 398 us: 1.20x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                          |
| python_startup_no_site | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| django_template | 48.2 ms                                                | 47.5 ms: 1.01x faster                                                          |
| genshi_text     | 31.8 ms                                                | 38.7 ms: 1.22x slower                                                          |
| genshi_xml      | 66.0 ms                                                | 80.6 ms: 1.22x slower                                                          |
| mako            | 16.3 ms                                                | 20.3 ms: 1.24x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.16x slower                                                                   |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| generators               | 80.1 ms                                                | 32.1 ms: 2.49x faster                                                          |
| typing_runtime_protocols | 544 us                                                 | 219 us: 2.48x faster                                                           |
| async_tree_none          | 728 ms                                                 | 393 ms: 1.85x faster                                                           |
| async_tree_io            | 1.77 sec                                               | 1.00 sec: 1.77x faster                                                         |
| logging_silent           | 190 ns                                                 | 108 ns: 1.75x faster                                                           |
| asyncio_tcp              | 922 ms                                                 | 539 ms: 1.71x faster                                                           |
| async_tree_memoization   | 870 ms                                                 | 526 ms: 1.65x faster                                                           |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 658 ms: 1.55x faster                                                           |
| pickle_pure_python       | 484 us                                                 | 317 us: 1.53x faster                                                           |
| coroutines               | 35.1 ms                                                | 24.1 ms: 1.46x faster                                                          |
| deltablue                | 7.91 ms                                                | 5.46 ms: 1.45x faster                                                          |
| pylint                   | 551 ms                                                 | 385 ms: 1.43x faster                                                           |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                          |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.87 sec: 1.37x faster                                                         |
| sqlglot_parse            | 2.17 ms                                                | 1.59 ms: 1.36x faster                                                          |
| raytrace                 | 507 ms                                                 | 377 ms: 1.34x faster                                                           |
| sqlglot_transpile        | 2.57 ms                                                | 1.94 ms: 1.33x faster                                                          |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                          |
| tornado_http             | 136 ms                                                 | 105 ms: 1.30x faster                                                           |
| thrift                   | 1.07 ms                                                | 847 us: 1.27x faster                                                           |
| deepcopy_reduce          | 4.17 us                                                | 3.34 us: 1.25x faster                                                          |
| scimark_sor              | 220 ms                                                 | 176 ms: 1.24x faster                                                           |
| richards_super           | 94.7 ms                                                | 78.6 ms: 1.21x faster                                                          |
| deepcopy                 | 479 us                                                 | 411 us: 1.17x faster                                                           |
| djangocms                | 38.4 us                                                | 33.2 us: 1.16x faster                                                          |
| deepcopy_memo            | 58.5 us                                                | 50.7 us: 1.15x faster                                                          |
| logging_simple           | 8.30 us                                                | 7.21 us: 1.15x faster                                                          |
| pycparser                | 1.58 sec                                               | 1.38 sec: 1.14x faster                                                         |
| logging_format           | 9.09 us                                                | 7.96 us: 1.14x faster                                                          |
| json_loads               | 31.2 us                                                | 27.5 us: 1.13x faster                                                          |
| aiohttp                  | 1.44 ms                                                | 1.28 ms: 1.13x faster                                                          |
| gunicorn                 | 1.53 ms                                                | 1.37 ms: 1.12x faster                                                          |
| chaos                    | 115 ms                                                 | 103 ms: 1.12x faster                                                           |
| dask                     | 441 ms                                                 | 396 ms: 1.11x faster                                                           |
| richards                 | 79.3 ms                                                | 71.7 ms: 1.11x faster                                                          |
| chameleon                | 9.68 ms                                                | 8.81 ms: 1.10x faster                                                          |
| html5lib                 | 88.9 ms                                                | 81.2 ms: 1.09x faster                                                          |
| json                     | 5.69 ms                                                | 5.20 ms: 1.09x faster                                                          |
| xml_etree_parse          | 168 ms                                                 | 154 ms: 1.09x faster                                                           |
| dulwich_log              | 84.3 ms                                                | 77.9 ms: 1.08x faster                                                          |
| xml_etree_process        | 79.1 ms                                                | 74.0 ms: 1.07x faster                                                          |
| pathlib                  | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                          |
| regex_v8                 | 27.8 ms                                                | 26.4 ms: 1.05x faster                                                          |
| sympy_sum                | 196 ms                                                 | 192 ms: 1.02x faster                                                           |
| mypy2                    | 894 ms                                                 | 874 ms: 1.02x faster                                                           |
| crypto_pyaes             | 128 ms                                                 | 125 ms: 1.02x faster                                                           |
| django_template          | 48.2 ms                                                | 47.5 ms: 1.01x faster                                                          |
| sqlglot_normalize        | 143 ms                                                 | 141 ms: 1.01x faster                                                           |
| bench_thread_pool        | 986 us                                                 | 976 us: 1.01x faster                                                           |
| gc_traversal             | 3.62 ms                                                | 3.61 ms: 1.00x faster                                                          |
| regex_dna                | 227 ms                                                 | 226 ms: 1.00x faster                                                           |
| pickle_list              | 5.08 us                                                | 5.13 us: 1.01x slower                                                          |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                           |
| pidigits                 | 191 ms                                                 | 194 ms: 1.01x slower                                                           |
| sqlite_synth             | 3.02 us                                                | 3.08 us: 1.02x slower                                                          |
| docutils                 | 3.30 sec                                               | 3.37 sec: 1.02x slower                                                         |
| unpickle_list            | 5.20 us                                                | 5.33 us: 1.02x slower                                                          |
| sympy_expand             | 566 ms                                                 | 583 ms: 1.03x slower                                                           |
| regex_effbot             | 3.63 ms                                                | 3.74 ms: 1.03x slower                                                          |
| xml_etree_generate       | 99.4 ms                                                | 103 ms: 1.03x slower                                                           |
| 2to3                     | 348 ms                                                 | 361 ms: 1.04x slower                                                           |
| unpickle                 | 14.4 us                                                | 14.9 us: 1.04x slower                                                          |
| sympy_str                | 346 ms                                                 | 362 ms: 1.05x slower                                                           |
| sqlglot_optimize         | 69.2 ms                                                | 73.3 ms: 1.06x slower                                                          |
| sympy_integrate          | 25.8 ms                                                | 27.6 ms: 1.07x slower                                                          |
| tomli_loads              | 3.14 sec                                               | 3.37 sec: 1.07x slower                                                         |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                          |
| go                       | 240 ms                                                 | 261 ms: 1.09x slower                                                           |
| float                    | 117 ms                                                 | 129 ms: 1.10x slower                                                           |
| create_gc_cycles         | 1.62 ms                                                | 1.78 ms: 1.10x slower                                                          |
| xml_etree_iterparse      | 115 ms                                                 | 127 ms: 1.10x slower                                                           |
| async_generators         | 444 ms                                                 | 504 ms: 1.14x slower                                                           |
| scimark_monte_carlo      | 118 ms                                                 | 135 ms: 1.14x slower                                                           |
| scimark_lu               | 176 ms                                                 | 203 ms: 1.16x slower                                                           |
| coverage                 | 79.4 ms                                                | 92.3 ms: 1.16x slower                                                          |
| mdp                      | 2.85 sec                                               | 3.33 sec: 1.17x slower                                                         |
| regex_compile            | 188 ms                                                 | 223 ms: 1.18x slower                                                           |
| pickle_dict              | 29.6 us                                                | 35.1 us: 1.19x slower                                                          |
| python_startup_no_site   | 5.93 ms                                                | 7.12 ms: 1.20x slower                                                          |
| pyflate                  | 716 ms                                                 | 862 ms: 1.20x slower                                                           |
| unpickle_pure_python     | 331 us                                                 | 398 us: 1.20x slower                                                           |
| meteor_contest           | 120 ms                                                 | 144 ms: 1.20x slower                                                           |
| genshi_text              | 31.8 ms                                                | 38.7 ms: 1.22x slower                                                          |
| genshi_xml               | 66.0 ms                                                | 80.6 ms: 1.22x slower                                                          |
| mako                     | 16.3 ms                                                | 20.3 ms: 1.24x slower                                                          |
| spectral_norm            | 170 ms                                                 | 215 ms: 1.27x slower                                                           |
| pprint_pformat           | 2.10 sec                                               | 2.66 sec: 1.27x slower                                                         |
| pprint_safe_repr         | 1.02 sec                                               | 1.29 sec: 1.27x slower                                                         |
| nbody                    | 154 ms                                                 | 197 ms: 1.28x slower                                                           |
| scimark_fft              | 466 ms                                                 | 597 ms: 1.28x slower                                                           |
| comprehensions           | 28.8 us                                                | 37.5 us: 1.30x slower                                                          |
| telco                    | 7.27 ms                                                | 9.63 ms: 1.33x slower                                                          |
| fannkuch                 | 532 ms                                                 | 705 ms: 1.33x slower                                                           |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 8.81 ms: 1.36x slower                                                          |
| nqueens                  | 106 ms                                                 | 153 ms: 1.44x slower                                                           |
| hexiom                   | 10.4 ms                                                | 15.2 ms: 1.46x slower                                                          |
| Geometric mean           | (ref)                                                  | 1.06x faster                                                                   |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240429-3.13.0a6+-3e1b870-PYTHON_UOPS/bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 51.51% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x
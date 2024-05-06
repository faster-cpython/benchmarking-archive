# Results vs. 3.10.4

- fork: faster-cpython
- ref: move_set_ip_to_exits
- machine: linux-x86_64
- commit hash: ed60e2e
- commit date: 2024-04-19
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 311 ms: 1.12x faster                                                             |
| chameleon      | 9.68 ms                                                | 8.08 ms: 1.20x faster                                                            |
| docutils       | 3.30 sec                                               | 3.15 sec: 1.05x faster                                                           |
| html5lib       | 88.9 ms                                                | 72.9 ms: 1.22x faster                                                            |
| tornado_http   | 136 ms                                                 | 104 ms: 1.32x faster                                                             |
| Geometric mean | (ref)                                                  | 1.18x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 383 ms: 1.90x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 968 ms: 1.83x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 511 ms: 1.70x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 646 ms: 1.57x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.75x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 93.3 ms: 1.25x faster                                                            |
| nbody          | 154 ms                                                 | 127 ms: 1.21x faster                                                             |
| pidigits       | 191 ms                                                 | 200 ms: 1.05x slower                                                             |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 26.0 ms: 1.07x faster                                                            |
| regex_compile  | 188 ms                                                 | 191 ms: 1.01x slower                                                             |
| regex_effbot   | 3.63 ms                                                | 3.68 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 310 us: 1.56x faster                                                             |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| xml_etree_process    | 79.1 ms                                                | 65.0 ms: 1.22x faster                                                            |
| tomli_loads          | 3.14 sec                                               | 2.69 sec: 1.17x faster                                                           |
| json_loads           | 31.2 us                                                | 27.7 us: 1.13x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 152 ms: 1.10x faster                                                             |
| unpickle_pure_python | 331 us                                                 | 303 us: 1.09x faster                                                             |
| xml_etree_iterparse  | 115 ms                                                 | 110 ms: 1.05x faster                                                             |
| xml_etree_generate   | 99.4 ms                                                | 96.0 ms: 1.04x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.11 us: 1.01x slower                                                            |
| unpickle             | 14.4 us                                                | 15.1 us: 1.05x slower                                                            |
| unpickle_list        | 5.20 us                                                | 5.46 us: 1.05x slower                                                            |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.2 us: 1.19x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.10 ms: 1.20x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                | 26.7 ms: 1.19x faster                                                            |
| mako            | 16.3 ms                                                | 13.7 ms: 1.19x faster                                                            |
| django_template | 48.2 ms                                                | 42.8 ms: 1.13x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 63.1 ms: 1.05x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.14x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 129 us: 4.23x faster                                                             |
| generators               | 80.1 ms                                                | 29.9 ms: 2.68x faster                                                            |
| async_tree_none          | 728 ms                                                 | 383 ms: 1.90x faster                                                             |
| deltablue                | 7.91 ms                                                | 4.23 ms: 1.87x faster                                                            |
| async_tree_io            | 1.77 sec                                               | 968 ms: 1.83x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 514 ms: 1.79x faster                                                             |
| logging_silent           | 190 ns                                                 | 107 ns: 1.78x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 511 ms: 1.70x faster                                                             |
| pylint                   | 551 ms                                                 | 348 ms: 1.59x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 646 ms: 1.57x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 310 us: 1.56x faster                                                             |
| raytrace                 | 507 ms                                                 | 343 ms: 1.48x faster                                                             |
| coroutines               | 35.1 ms                                                | 23.8 ms: 1.47x faster                                                            |
| richards_super           | 94.7 ms                                                | 65.0 ms: 1.46x faster                                                            |
| scimark_sor              | 220 ms                                                 | 151 ms: 1.45x faster                                                             |
| sqlglot_parse            | 2.17 ms                                                | 1.55 ms: 1.40x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| chaos                    | 115 ms                                                 | 83.3 ms: 1.39x faster                                                            |
| richards                 | 79.3 ms                                                | 57.3 ms: 1.38x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                           |
| sqlglot_transpile        | 2.57 ms                                                | 1.88 ms: 1.37x faster                                                            |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.33x faster                                                            |
| tornado_http             | 136 ms                                                 | 104 ms: 1.32x faster                                                             |
| logging_simple           | 8.30 us                                                | 6.46 us: 1.29x faster                                                            |
| thrift                   | 1.07 ms                                                | 841 us: 1.27x faster                                                             |
| crypto_pyaes             | 128 ms                                                 | 100 ms: 1.27x faster                                                             |
| logging_format           | 9.09 us                                                | 7.16 us: 1.27x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 46.3 us: 1.26x faster                                                            |
| go                       | 240 ms                                                 | 191 ms: 1.26x faster                                                             |
| float                    | 117 ms                                                 | 93.3 ms: 1.25x faster                                                            |
| deepcopy_reduce          | 4.17 us                                                | 3.38 us: 1.24x faster                                                            |
| deepcopy                 | 479 us                                                 | 390 us: 1.23x faster                                                             |
| html5lib                 | 88.9 ms                                                | 72.9 ms: 1.22x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 65.0 ms: 1.22x faster                                                            |
| nbody                    | 154 ms                                                 | 127 ms: 1.21x faster                                                             |
| spectral_norm            | 170 ms                                                 | 141 ms: 1.20x faster                                                             |
| chameleon                | 9.68 ms                                                | 8.08 ms: 1.20x faster                                                            |
| genshi_text              | 31.8 ms                                                | 26.7 ms: 1.19x faster                                                            |
| mako                     | 16.3 ms                                                | 13.7 ms: 1.19x faster                                                            |
| pycparser                | 1.58 sec                                               | 1.32 sec: 1.19x faster                                                           |
| comprehensions           | 28.8 us                                                | 24.3 us: 1.18x faster                                                            |
| djangocms                | 38.4 us                                                | 32.9 us: 1.17x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.69 sec: 1.17x faster                                                           |
| aiohttp                  | 1.44 ms                                                | 1.24 ms: 1.16x faster                                                            |
| gunicorn                 | 1.53 ms                                                | 1.33 ms: 1.15x faster                                                            |
| dask                     | 441 ms                                                 | 383 ms: 1.15x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 74.3 ms: 1.13x faster                                                            |
| django_template          | 48.2 ms                                                | 42.8 ms: 1.13x faster                                                            |
| json_loads               | 31.2 us                                                | 27.7 us: 1.13x faster                                                            |
| 2to3                     | 348 ms                                                 | 311 ms: 1.12x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 106 ms: 1.12x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 128 ms: 1.12x faster                                                             |
| bench_thread_pool        | 986 us                                                 | 889 us: 1.11x faster                                                             |
| json                     | 5.69 ms                                                | 5.13 ms: 1.11x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.5 ms: 1.11x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 152 ms: 1.10x faster                                                             |
| sympy_integrate          | 25.8 ms                                                | 23.5 ms: 1.10x faster                                                            |
| mypy2                    | 894 ms                                                 | 817 ms: 1.09x faster                                                             |
| sympy_sum                | 196 ms                                                 | 180 ms: 1.09x faster                                                             |
| unpickle_pure_python     | 331 us                                                 | 303 us: 1.09x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 26.0 ms: 1.07x faster                                                            |
| pyflate                  | 716 ms                                                 | 672 ms: 1.07x faster                                                             |
| sympy_str                | 346 ms                                                 | 328 ms: 1.05x faster                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 65.9 ms: 1.05x faster                                                            |
| docutils                 | 3.30 sec                                               | 3.15 sec: 1.05x faster                                                           |
| xml_etree_iterparse      | 115 ms                                                 | 110 ms: 1.05x faster                                                             |
| genshi_xml               | 66.0 ms                                                | 63.1 ms: 1.05x faster                                                            |
| scimark_fft              | 466 ms                                                 | 448 ms: 1.04x faster                                                             |
| xml_etree_generate       | 99.4 ms                                                | 96.0 ms: 1.04x faster                                                            |
| sympy_expand             | 566 ms                                                 | 546 ms: 1.04x faster                                                             |
| fannkuch                 | 532 ms                                                 | 515 ms: 1.03x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.30 ms: 1.03x faster                                                            |
| hexiom                   | 10.4 ms                                                | 10.2 ms: 1.02x faster                                                            |
| scimark_lu               | 176 ms                                                 | 172 ms: 1.02x faster                                                             |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| pickle_list              | 5.08 us                                                | 5.11 us: 1.01x slower                                                            |
| regex_compile            | 188 ms                                                 | 191 ms: 1.01x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                             |
| regex_effbot             | 3.63 ms                                                | 3.68 ms: 1.02x slower                                                            |
| mdp                      | 2.85 sec                                               | 2.90 sec: 1.02x slower                                                           |
| sqlite_synth             | 3.02 us                                                | 3.14 us: 1.04x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 3.78 ms: 1.04x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.1 us: 1.05x slower                                                            |
| pidigits                 | 191 ms                                                 | 200 ms: 1.05x slower                                                             |
| pprint_safe_repr         | 1.02 sec                                               | 1.07 sec: 1.05x slower                                                           |
| unpickle_list            | 5.20 us                                                | 5.46 us: 1.05x slower                                                            |
| pprint_pformat           | 2.10 sec                                               | 2.26 sec: 1.07x slower                                                           |
| async_generators         | 444 ms                                                 | 479 ms: 1.08x slower                                                             |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                            |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.09x slower                                                            |
| meteor_contest           | 120 ms                                                 | 131 ms: 1.10x slower                                                             |
| nqueens                  | 106 ms                                                 | 117 ms: 1.10x slower                                                             |
| pickle_dict              | 29.6 us                                                | 35.2 us: 1.19x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.10 ms: 1.20x slower                                                            |
| coverage                 | 79.4 ms                                                | 98.8 ms: 1.24x slower                                                            |
| telco                    | 7.27 ms                                                | 9.60 ms: 1.32x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.18x faster                                                                     |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240419-3.13.0a6+-ed60e2e-PYTHON_UOPS/bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.11x
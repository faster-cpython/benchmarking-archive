# Results vs. 3.10.4

- fork: faster-cpython
- ref: convert_deopts_to_ex
- machine: linux-x86_64
- commit hash: 458d82f
- commit date: 2024-04-19
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 305 ms: 1.14x faster                                                             |
| chameleon      | 9.68 ms                                                | 7.61 ms: 1.27x faster                                                            |
| docutils       | 3.30 sec                                               | 3.14 sec: 1.05x faster                                                           |
| html5lib       | 88.9 ms                                                | 72.2 ms: 1.23x faster                                                            |
| tornado_http   | 136 ms                                                 | 102 ms: 1.33x faster                                                             |
| Geometric mean | (ref)                                                  | 1.20x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 376 ms: 1.94x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 976 ms: 1.81x faster                                                             |
| async_tree_memoization  | 870 ms                                                 | 503 ms: 1.73x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 635 ms: 1.60x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.77x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 117 ms                                                 | 89.2 ms: 1.31x faster                                                            |
| nbody          | 154 ms                                                 | 122 ms: 1.26x faster                                                             |
| pidigits       | 191 ms                                                 | 192 ms: 1.00x slower                                                             |
| Geometric mean | (ref)                                                  | 1.18x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.2 ms: 1.10x faster                                                            |
| regex_compile  | 188 ms                                                 | 181 ms: 1.04x faster                                                             |
| regex_dna      | 227 ms                                                 | 224 ms: 1.01x faster                                                             |
| regex_effbot   | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 316 us: 1.53x faster                                                             |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                            |
| tomli_loads          | 3.14 sec                                               | 2.55 sec: 1.23x faster                                                           |
| xml_etree_process    | 79.1 ms                                                | 65.1 ms: 1.21x faster                                                            |
| unpickle_pure_python | 331 us                                                 | 282 us: 1.17x faster                                                             |
| json_loads           | 31.2 us                                                | 27.8 us: 1.12x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 152 ms: 1.11x faster                                                             |
| xml_etree_generate   | 99.4 ms                                                | 93.5 ms: 1.06x faster                                                            |
| pickle_list          | 5.08 us                                                | 4.83 us: 1.05x faster                                                            |
| xml_etree_iterparse  | 115 ms                                                 | 111 ms: 1.04x faster                                                             |
| unpickle_list        | 5.20 us                                                | 5.33 us: 1.03x slower                                                            |
| unpickle             | 14.4 us                                                | 15.6 us: 1.09x slower                                                            |
| pickle_dict          | 29.6 us                                                | 32.8 us: 1.11x slower                                                            |
| pickle               | 10.7 us                                                | 12.1 us: 1.13x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 13.6 ms: 1.20x faster                                                            |
| django_template | 48.2 ms                                                | 41.3 ms: 1.17x faster                                                            |
| genshi_text     | 31.8 ms                                                | 28.7 ms: 1.11x faster                                                            |
| genshi_xml      | 66.0 ms                                                | 64.7 ms: 1.02x faster                                                            |
| Geometric mean  | (ref)                                                  | 1.12x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 124 us: 4.40x faster                                                             |
| generators               | 80.1 ms                                                | 29.8 ms: 2.69x faster                                                            |
| async_tree_none          | 728 ms                                                 | 376 ms: 1.94x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 976 ms: 1.81x faster                                                             |
| deltablue                | 7.91 ms                                                | 4.37 ms: 1.81x faster                                                            |
| logging_silent           | 190 ns                                                 | 106 ns: 1.79x faster                                                             |
| async_tree_memoization   | 870 ms                                                 | 503 ms: 1.73x faster                                                             |
| asyncio_tcp              | 922 ms                                                 | 533 ms: 1.73x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 635 ms: 1.60x faster                                                             |
| pylint                   | 551 ms                                                 | 350 ms: 1.57x faster                                                             |
| raytrace                 | 507 ms                                                 | 326 ms: 1.55x faster                                                             |
| pickle_pure_python       | 484 us                                                 | 316 us: 1.53x faster                                                             |
| richards_super           | 94.7 ms                                                | 62.9 ms: 1.51x faster                                                            |
| sqlglot_parse            | 2.17 ms                                                | 1.48 ms: 1.47x faster                                                            |
| coroutines               | 35.1 ms                                                | 24.3 ms: 1.45x faster                                                            |
| chaos                    | 115 ms                                                 | 80.9 ms: 1.43x faster                                                            |
| sqlglot_transpile        | 2.57 ms                                                | 1.81 ms: 1.42x faster                                                            |
| richards                 | 79.3 ms                                                | 56.3 ms: 1.41x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                           |
| scimark_sor              | 220 ms                                                 | 159 ms: 1.38x faster                                                             |
| deepcopy_memo            | 58.5 us                                                | 42.9 us: 1.36x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 94.1 ms: 1.36x faster                                                            |
| scimark_monte_carlo      | 118 ms                                                 | 88.3 ms: 1.34x faster                                                            |
| tornado_http             | 136 ms                                                 | 102 ms: 1.33x faster                                                             |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                            |
| float                    | 117 ms                                                 | 89.2 ms: 1.31x faster                                                            |
| chameleon                | 9.68 ms                                                | 7.61 ms: 1.27x faster                                                            |
| thrift                   | 1.07 ms                                                | 847 us: 1.27x faster                                                             |
| nbody                    | 154 ms                                                 | 122 ms: 1.26x faster                                                             |
| go                       | 240 ms                                                 | 191 ms: 1.26x faster                                                             |
| deepcopy_reduce          | 4.17 us                                                | 3.34 us: 1.25x faster                                                            |
| deepcopy                 | 479 us                                                 | 384 us: 1.25x faster                                                             |
| pycparser                | 1.58 sec                                               | 1.27 sec: 1.24x faster                                                           |
| html5lib                 | 88.9 ms                                                | 72.2 ms: 1.23x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.55 sec: 1.23x faster                                                           |
| logging_simple           | 8.30 us                                                | 6.76 us: 1.23x faster                                                            |
| xml_etree_process        | 79.1 ms                                                | 65.1 ms: 1.21x faster                                                            |
| logging_format           | 9.09 us                                                | 7.54 us: 1.21x faster                                                            |
| comprehensions           | 28.8 us                                                | 23.9 us: 1.20x faster                                                            |
| mako                     | 16.3 ms                                                | 13.6 ms: 1.20x faster                                                            |
| pyflate                  | 716 ms                                                 | 600 ms: 1.19x faster                                                             |
| spectral_norm            | 170 ms                                                 | 144 ms: 1.18x faster                                                             |
| unpickle_pure_python     | 331 us                                                 | 282 us: 1.17x faster                                                             |
| django_template          | 48.2 ms                                                | 41.3 ms: 1.17x faster                                                            |
| aiohttp                  | 1.44 ms                                                | 1.24 ms: 1.16x faster                                                            |
| djangocms                | 38.4 us                                                | 33.4 us: 1.15x faster                                                            |
| gunicorn                 | 1.53 ms                                                | 1.33 ms: 1.15x faster                                                            |
| 2to3                     | 348 ms                                                 | 305 ms: 1.14x faster                                                             |
| sqlglot_normalize        | 143 ms                                                 | 126 ms: 1.14x faster                                                             |
| dask                     | 441 ms                                                 | 389 ms: 1.13x faster                                                             |
| dulwich_log              | 84.3 ms                                                | 75.1 ms: 1.12x faster                                                            |
| json_loads               | 31.2 us                                                | 27.8 us: 1.12x faster                                                            |
| bench_thread_pool        | 986 us                                                 | 886 us: 1.11x faster                                                             |
| genshi_text              | 31.8 ms                                                | 28.7 ms: 1.11x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 152 ms: 1.11x faster                                                             |
| json                     | 5.69 ms                                                | 5.14 ms: 1.11x faster                                                            |
| sympy_sum                | 196 ms                                                 | 178 ms: 1.10x faster                                                             |
| regex_v8                 | 27.8 ms                                                | 25.2 ms: 1.10x faster                                                            |
| sympy_integrate          | 25.8 ms                                                | 23.5 ms: 1.10x faster                                                            |
| pathlib                  | 20.5 ms                                                | 18.7 ms: 1.10x faster                                                            |
| mypy2                    | 894 ms                                                 | 829 ms: 1.08x faster                                                             |
| hexiom                   | 10.4 ms                                                | 9.65 ms: 1.08x faster                                                            |
| sqlglot_optimize         | 69.2 ms                                                | 64.2 ms: 1.08x faster                                                            |
| sympy_str                | 346 ms                                                 | 325 ms: 1.06x faster                                                             |
| xml_etree_generate       | 99.4 ms                                                | 93.5 ms: 1.06x faster                                                            |
| fannkuch                 | 532 ms                                                 | 501 ms: 1.06x faster                                                             |
| pickle_list              | 5.08 us                                                | 4.83 us: 1.05x faster                                                            |
| docutils                 | 3.30 sec                                               | 3.14 sec: 1.05x faster                                                           |
| pprint_safe_repr         | 1.02 sec                                               | 974 ms: 1.05x faster                                                             |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.20 ms: 1.04x faster                                                            |
| regex_compile            | 188 ms                                                 | 181 ms: 1.04x faster                                                             |
| sympy_expand             | 566 ms                                                 | 544 ms: 1.04x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 111 ms: 1.04x faster                                                             |
| pprint_pformat           | 2.10 sec                                               | 2.02 sec: 1.04x faster                                                           |
| genshi_xml               | 66.0 ms                                                | 64.7 ms: 1.02x faster                                                            |
| scimark_lu               | 176 ms                                                 | 173 ms: 1.02x faster                                                             |
| scimark_fft              | 466 ms                                                 | 457 ms: 1.02x faster                                                             |
| regex_dna                | 227 ms                                                 | 224 ms: 1.01x faster                                                             |
| pidigits                 | 191 ms                                                 | 192 ms: 1.00x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 568 ms: 1.02x slower                                                             |
| unpickle_list            | 5.20 us                                                | 5.33 us: 1.03x slower                                                            |
| nqueens                  | 106 ms                                                 | 109 ms: 1.03x slower                                                             |
| regex_effbot             | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                            |
| meteor_contest           | 120 ms                                                 | 125 ms: 1.04x slower                                                             |
| gc_traversal             | 3.62 ms                                                | 3.80 ms: 1.05x slower                                                            |
| async_generators         | 444 ms                                                 | 468 ms: 1.05x slower                                                             |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.09x slower                                                            |
| unpickle                 | 14.4 us                                                | 15.6 us: 1.09x slower                                                            |
| pickle_dict              | 29.6 us                                                | 32.8 us: 1.11x slower                                                            |
| pickle                   | 10.7 us                                                | 12.1 us: 1.13x slower                                                            |
| python_startup_no_site   | 5.93 ms                                                | 7.11 ms: 1.20x slower                                                            |
| coverage                 | 79.4 ms                                                | 97.9 ms: 1.23x slower                                                            |
| telco                    | 7.27 ms                                                | 9.11 ms: 1.25x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.20x faster                                                                     |

Benchmark hidden because not significant (3): sqlite_synth, mdp, bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240419-3.13.0a6+-458d82f-PYTHON_UOPS/bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.11x
# Results vs. 3.10.4

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 6ccc646
- commit date: 2024-04-23
- overall geometric mean: 1.03x faster
- HPT reliability: 56.08%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 352 ms: 1.01x slower                                                             |
| chameleon      | 9.68 ms                                                | 10.0 ms: 1.04x slower                                                            |
| docutils       | 3.30 sec                                               | 3.61 sec: 1.10x slower                                                           |
| html5lib       | 88.9 ms                                                | 103 ms: 1.16x slower                                                             |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 457 ms: 1.59x faster                                                             |
| async_tree_io           | 1.77 sec                                               | 1.11 sec: 1.59x faster                                                           |
| async_tree_memoization  | 870 ms                                                 | 608 ms: 1.43x faster                                                             |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 734 ms: 1.38x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.50x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 122 ms: 1.25x faster                                                             |
| float          | 117 ms                                                 | 94.3 ms: 1.24x faster                                                            |
| pidigits       | 191 ms                                                 | 194 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                  | 1.15x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 25.6 ms: 1.08x faster                                                            |
| regex_effbot   | 3.63 ms                                                | 3.72 ms: 1.02x slower                                                            |
| regex_compile  | 188 ms                                                 | 231 ms: 1.23x slower                                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 14.2 ms                                                | 12.7 ms: 1.12x faster                                                            |
| json_loads           | 31.2 us                                                | 28.5 us: 1.09x faster                                                            |
| xml_etree_parse      | 168 ms                                                 | 155 ms: 1.08x faster                                                             |
| tomli_loads          | 3.14 sec                                               | 2.99 sec: 1.05x faster                                                           |
| xml_etree_iterparse  | 115 ms                                                 | 112 ms: 1.03x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.17 us: 1.02x slower                                                            |
| unpickle_pure_python | 331 us                                                 | 337 us: 1.02x slower                                                             |
| xml_etree_process    | 79.1 ms                                                | 81.4 ms: 1.03x slower                                                            |
| pickle_pure_python   | 484 us                                                 | 500 us: 1.03x slower                                                             |
| unpickle_list        | 5.20 us                                                | 5.42 us: 1.04x slower                                                            |
| unpickle             | 14.4 us                                                | 15.8 us: 1.10x slower                                                            |
| xml_etree_generate   | 99.4 ms                                                | 111 ms: 1.11x slower                                                             |
| pickle               | 10.7 us                                                | 12.0 us: 1.13x slower                                                            |
| pickle_dict          | 29.6 us                                                | 35.4 us: 1.20x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.7 ms: 1.37x faster                                                            |
| python_startup_no_site | 5.93 ms                                                | 7.18 ms: 1.21x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 13.8 ms: 1.18x faster                                                            |
| genshi_text     | 31.8 ms                                                | 32.4 ms: 1.02x slower                                                            |
| genshi_xml      | 66.0 ms                                                | 74.2 ms: 1.12x slower                                                            |
| django_template | 48.2 ms                                                | 60.9 ms: 1.27x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 154 us: 3.53x faster                                                             |
| generators               | 80.1 ms                                                | 31.7 ms: 2.53x faster                                                            |
| asyncio_tcp              | 922 ms                                                 | 569 ms: 1.62x faster                                                             |
| async_tree_none          | 728 ms                                                 | 457 ms: 1.59x faster                                                             |
| async_tree_io            | 1.77 sec                                               | 1.11 sec: 1.59x faster                                                           |
| async_tree_memoization   | 870 ms                                                 | 608 ms: 1.43x faster                                                             |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 734 ms: 1.38x faster                                                             |
| coroutines               | 35.1 ms                                                | 25.5 ms: 1.37x faster                                                            |
| python_startup           | 14.6 ms                                                | 10.7 ms: 1.37x faster                                                            |
| crypto_pyaes             | 128 ms                                                 | 93.4 ms: 1.37x faster                                                            |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.91 sec: 1.34x faster                                                           |
| pylint                   | 551 ms                                                 | 416 ms: 1.33x faster                                                             |
| logging_silent           | 190 ns                                                 | 147 ns: 1.29x faster                                                             |
| scimark_monte_carlo      | 118 ms                                                 | 93.1 ms: 1.27x faster                                                            |
| deltablue                | 7.91 ms                                                | 6.30 ms: 1.26x faster                                                            |
| nbody                    | 154 ms                                                 | 122 ms: 1.25x faster                                                             |
| float                    | 117 ms                                                 | 94.3 ms: 1.24x faster                                                            |
| mako                     | 16.3 ms                                                | 13.8 ms: 1.18x faster                                                            |
| spectral_norm            | 170 ms                                                 | 144 ms: 1.18x faster                                                             |
| comprehensions           | 28.8 us                                                | 25.2 us: 1.14x faster                                                            |
| richards_super           | 94.7 ms                                                | 84.5 ms: 1.12x faster                                                            |
| chaos                    | 115 ms                                                 | 103 ms: 1.12x faster                                                             |
| json_dumps               | 14.2 ms                                                | 12.7 ms: 1.12x faster                                                            |
| scimark_sor              | 220 ms                                                 | 199 ms: 1.10x faster                                                             |
| pyflate                  | 716 ms                                                 | 652 ms: 1.10x faster                                                             |
| json_loads               | 31.2 us                                                | 28.5 us: 1.09x faster                                                            |
| regex_v8                 | 27.8 ms                                                | 25.6 ms: 1.08x faster                                                            |
| xml_etree_parse          | 168 ms                                                 | 155 ms: 1.08x faster                                                             |
| raytrace                 | 507 ms                                                 | 474 ms: 1.07x faster                                                             |
| sqlglot_parse            | 2.17 ms                                                | 2.04 ms: 1.06x faster                                                            |
| deepcopy_memo            | 58.5 us                                                | 55.0 us: 1.06x faster                                                            |
| fannkuch                 | 532 ms                                                 | 505 ms: 1.05x faster                                                             |
| djangocms                | 38.4 us                                                | 36.5 us: 1.05x faster                                                            |
| tomli_loads              | 3.14 sec                                               | 2.99 sec: 1.05x faster                                                           |
| json                     | 5.69 ms                                                | 5.42 ms: 1.05x faster                                                            |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 6.19 ms: 1.05x faster                                                            |
| richards                 | 79.3 ms                                                | 76.0 ms: 1.04x faster                                                            |
| go                       | 240 ms                                                 | 230 ms: 1.04x faster                                                             |
| xml_etree_iterparse      | 115 ms                                                 | 112 ms: 1.03x faster                                                             |
| sqlglot_transpile        | 2.57 ms                                                | 2.52 ms: 1.02x faster                                                            |
| scimark_fft              | 466 ms                                                 | 458 ms: 1.02x faster                                                             |
| 2to3                     | 348 ms                                                 | 352 ms: 1.01x slower                                                             |
| bench_thread_pool        | 986 us                                                 | 998 us: 1.01x slower                                                             |
| pidigits                 | 191 ms                                                 | 194 ms: 1.01x slower                                                             |
| pickle_list              | 5.08 us                                                | 5.17 us: 1.02x slower                                                            |
| pathlib                  | 20.5 ms                                                | 20.8 ms: 1.02x slower                                                            |
| genshi_text              | 31.8 ms                                                | 32.4 ms: 1.02x slower                                                            |
| unpickle_pure_python     | 331 us                                                 | 337 us: 1.02x slower                                                             |
| asyncio_websockets       | 559 ms                                                 | 571 ms: 1.02x slower                                                             |
| pycparser                | 1.58 sec                                               | 1.61 sec: 1.02x slower                                                           |
| regex_effbot             | 3.63 ms                                                | 3.72 ms: 1.02x slower                                                            |
| xml_etree_process        | 79.1 ms                                                | 81.4 ms: 1.03x slower                                                            |
| meteor_contest           | 120 ms                                                 | 123 ms: 1.03x slower                                                             |
| pickle_pure_python       | 484 us                                                 | 500 us: 1.03x slower                                                             |
| chameleon                | 9.68 ms                                                | 10.0 ms: 1.04x slower                                                            |
| bench_mp_pool            | 24.0 ms                                                | 25.0 ms: 1.04x slower                                                            |
| unpickle_list            | 5.20 us                                                | 5.42 us: 1.04x slower                                                            |
| hexiom                   | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                            |
| aiohttp                  | 1.44 ms                                                | 1.50 ms: 1.04x slower                                                            |
| sqlite_synth             | 3.02 us                                                | 3.16 us: 1.05x slower                                                            |
| mdp                      | 2.85 sec                                               | 2.99 sec: 1.05x slower                                                           |
| gunicorn                 | 1.53 ms                                                | 1.61 ms: 1.05x slower                                                            |
| scimark_lu               | 176 ms                                                 | 190 ms: 1.08x slower                                                             |
| dask                     | 441 ms                                                 | 481 ms: 1.09x slower                                                             |
| sympy_integrate          | 25.8 ms                                                | 28.3 ms: 1.10x slower                                                            |
| docutils                 | 3.30 sec                                               | 3.61 sec: 1.10x slower                                                           |
| unpickle                 | 14.4 us                                                | 15.8 us: 1.10x slower                                                            |
| sympy_sum                | 196 ms                                                 | 216 ms: 1.10x slower                                                             |
| dulwich_log              | 84.3 ms                                                | 93.7 ms: 1.11x slower                                                            |
| mypy2                    | 894 ms                                                 | 994 ms: 1.11x slower                                                             |
| create_gc_cycles         | 1.62 ms                                                | 1.80 ms: 1.11x slower                                                            |
| gc_traversal             | 3.62 ms                                                | 4.03 ms: 1.11x slower                                                            |
| xml_etree_generate       | 99.4 ms                                                | 111 ms: 1.11x slower                                                             |
| genshi_xml               | 66.0 ms                                                | 74.2 ms: 1.12x slower                                                            |
| pickle                   | 10.7 us                                                | 12.0 us: 1.13x slower                                                            |
| async_generators         | 444 ms                                                 | 504 ms: 1.14x slower                                                             |
| deepcopy                 | 479 us                                                 | 553 us: 1.15x slower                                                             |
| html5lib                 | 88.9 ms                                                | 103 ms: 1.16x slower                                                             |
| sqlglot_normalize        | 143 ms                                                 | 166 ms: 1.16x slower                                                             |
| sympy_str                | 346 ms                                                 | 403 ms: 1.17x slower                                                             |
| sqlglot_optimize         | 69.2 ms                                                | 81.2 ms: 1.17x slower                                                            |
| pickle_dict              | 29.6 us                                                | 35.4 us: 1.20x slower                                                            |
| sympy_expand             | 566 ms                                                 | 679 ms: 1.20x slower                                                             |
| python_startup_no_site   | 5.93 ms                                                | 7.18 ms: 1.21x slower                                                            |
| deepcopy_reduce          | 4.17 us                                                | 5.09 us: 1.22x slower                                                            |
| pprint_safe_repr         | 1.02 sec                                               | 1.24 sec: 1.22x slower                                                           |
| pprint_pformat           | 2.10 sec                                               | 2.58 sec: 1.23x slower                                                           |
| regex_compile            | 188 ms                                                 | 231 ms: 1.23x slower                                                             |
| coverage                 | 79.4 ms                                                | 98.5 ms: 1.24x slower                                                            |
| django_template          | 48.2 ms                                                | 60.9 ms: 1.27x slower                                                            |
| logging_simple           | 8.30 us                                                | 10.5 us: 1.27x slower                                                            |
| logging_format           | 9.09 us                                                | 11.7 us: 1.28x slower                                                            |
| nqueens                  | 106 ms                                                 | 139 ms: 1.32x slower                                                             |
| telco                    | 7.27 ms                                                | 9.65 ms: 1.33x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (3): tornado_http, regex_dna, thrift
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240423-3.13.0a6+-6ccc646-PYTHON_UOPS/bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 56.08% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x
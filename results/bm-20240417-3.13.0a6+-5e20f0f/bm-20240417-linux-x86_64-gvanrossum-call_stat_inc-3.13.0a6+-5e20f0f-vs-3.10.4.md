# Results vs. 3.10.4

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 269 ms: 1.30x faster                                                |
| chameleon      | 9.68 ms                                                | 7.10 ms: 1.36x faster                                               |
| docutils       | 3.30 sec                                               | 2.82 sec: 1.17x faster                                              |
| html5lib       | 88.9 ms                                                | 65.8 ms: 1.35x faster                                               |
| tornado_http   | 136 ms                                                 | 93.9 ms: 1.45x faster                                               |
| Geometric mean | (ref)                                                  | 1.32x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 353 ms: 2.06x faster                                                |
| async_tree_memoization  | 870 ms                                                 | 460 ms: 1.89x faster                                                |
| async_tree_io           | 1.77 sec                                               | 943 ms: 1.88x faster                                                |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 612 ms: 1.66x faster                                                |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 87.2 ms: 1.76x faster                                               |
| float          | 117 ms                                                 | 78.3 ms: 1.50x faster                                               |
| pidigits       | 191 ms                                                 | 190 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                  | 1.38x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 134 ms: 1.40x faster                                                |
| regex_v8       | 27.8 ms                                                | 25.0 ms: 1.11x faster                                               |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                                |
| regex_effbot   | 3.63 ms                                                | 3.73 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                  | 1.11x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 302 us: 1.60x faster                                                |
| unpickle_pure_python | 331 us                                                 | 214 us: 1.54x faster                                                |
| tomli_loads          | 3.14 sec                                               | 2.17 sec: 1.44x faster                                              |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.34x faster                                               |
| xml_etree_process    | 79.1 ms                                                | 60.9 ms: 1.30x faster                                               |
| xml_etree_generate   | 99.4 ms                                                | 87.8 ms: 1.13x faster                                               |
| json_loads           | 31.2 us                                                | 27.7 us: 1.13x faster                                               |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                |
| xml_etree_parse      | 168 ms                                                 | 161 ms: 1.04x faster                                                |
| unpickle_list        | 5.20 us                                                | 5.03 us: 1.03x faster                                               |
| pickle_list          | 5.08 us                                                | 5.13 us: 1.01x slower                                               |
| pickle               | 10.7 us                                                | 11.9 us: 1.12x slower                                               |
| unpickle             | 14.4 us                                                | 16.6 us: 1.16x slower                                               |
| pickle_dict          | 29.6 us                                                | 34.3 us: 1.16x slower                                               |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.5 ms: 1.39x faster                                               |
| python_startup_no_site | 5.93 ms                                                | 7.08 ms: 1.19x slower                                               |
| Geometric mean         | (ref)                                                  | 1.08x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.7 ms: 1.52x faster                                               |
| genshi_text     | 31.8 ms                                                | 23.3 ms: 1.37x faster                                               |
| django_template | 48.2 ms                                                | 35.5 ms: 1.36x faster                                               |
| genshi_xml      | 66.0 ms                                                | 51.4 ms: 1.29x faster                                               |
| Geometric mean  | (ref)                                                  | 1.38x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 113 us: 4.80x faster                                                |
| generators               | 80.1 ms                                                | 29.7 ms: 2.69x faster                                               |
| deltablue                | 7.91 ms                                                | 3.21 ms: 2.46x faster                                               |
| async_tree_none          | 728 ms                                                 | 353 ms: 2.06x faster                                                |
| raytrace                 | 507 ms                                                 | 264 ms: 1.92x faster                                                |
| chaos                    | 115 ms                                                 | 60.5 ms: 1.91x faster                                               |
| async_tree_memoization   | 870 ms                                                 | 460 ms: 1.89x faster                                                |
| logging_silent           | 190 ns                                                 | 101 ns: 1.89x faster                                                |
| async_tree_io            | 1.77 sec                                               | 943 ms: 1.88x faster                                                |
| asyncio_tcp              | 922 ms                                                 | 506 ms: 1.82x faster                                                |
| richards_super           | 94.7 ms                                                | 52.7 ms: 1.80x faster                                               |
| scimark_sor              | 220 ms                                                 | 123 ms: 1.79x faster                                                |
| nbody                    | 154 ms                                                 | 87.2 ms: 1.76x faster                                               |
| crypto_pyaes             | 128 ms                                                 | 73.5 ms: 1.74x faster                                               |
| scimark_monte_carlo      | 118 ms                                                 | 68.2 ms: 1.73x faster                                               |
| pylint                   | 551 ms                                                 | 319 ms: 1.73x faster                                                |
| comprehensions           | 28.8 us                                                | 16.8 us: 1.71x faster                                               |
| sqlglot_parse            | 2.17 ms                                                | 1.28 ms: 1.70x faster                                               |
| go                       | 240 ms                                                 | 141 ms: 1.70x faster                                                |
| hexiom                   | 10.4 ms                                                | 6.14 ms: 1.69x faster                                               |
| richards                 | 79.3 ms                                                | 47.3 ms: 1.68x faster                                               |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 612 ms: 1.66x faster                                                |
| sqlglot_transpile        | 2.57 ms                                                | 1.58 ms: 1.63x faster                                               |
| pickle_pure_python       | 484 us                                                 | 302 us: 1.60x faster                                                |
| deepcopy_memo            | 58.5 us                                                | 37.0 us: 1.58x faster                                               |
| coroutines               | 35.1 ms                                                | 22.7 ms: 1.55x faster                                               |
| unpickle_pure_python     | 331 us                                                 | 214 us: 1.54x faster                                                |
| pyflate                  | 716 ms                                                 | 465 ms: 1.54x faster                                                |
| scimark_lu               | 176 ms                                                 | 115 ms: 1.53x faster                                                |
| mako                     | 16.3 ms                                                | 10.7 ms: 1.52x faster                                               |
| float                    | 117 ms                                                 | 78.3 ms: 1.50x faster                                               |
| spectral_norm            | 170 ms                                                 | 115 ms: 1.47x faster                                                |
| tornado_http             | 136 ms                                                 | 93.9 ms: 1.45x faster                                               |
| tomli_loads              | 3.14 sec                                               | 2.17 sec: 1.44x faster                                              |
| logging_simple           | 8.30 us                                                | 5.85 us: 1.42x faster                                               |
| regex_compile            | 188 ms                                                 | 134 ms: 1.40x faster                                                |
| logging_format           | 9.09 us                                                | 6.50 us: 1.40x faster                                               |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.84 sec: 1.40x faster                                              |
| python_startup           | 14.6 ms                                                | 10.5 ms: 1.39x faster                                               |
| genshi_text              | 31.8 ms                                                | 23.3 ms: 1.37x faster                                               |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.37x faster                                              |
| chameleon                | 9.68 ms                                                | 7.10 ms: 1.36x faster                                               |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                              |
| django_template          | 48.2 ms                                                | 35.5 ms: 1.36x faster                                               |
| html5lib                 | 88.9 ms                                                | 65.8 ms: 1.35x faster                                               |
| fannkuch                 | 532 ms                                                 | 394 ms: 1.35x faster                                                |
| pprint_safe_repr         | 1.02 sec                                               | 756 ms: 1.35x faster                                                |
| deepcopy                 | 479 us                                                 | 356 us: 1.34x faster                                                |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.34x faster                                               |
| thrift                   | 1.07 ms                                                | 816 us: 1.31x faster                                                |
| xml_etree_process        | 79.1 ms                                                | 60.9 ms: 1.30x faster                                               |
| 2to3                     | 348 ms                                                 | 269 ms: 1.30x faster                                                |
| deepcopy_reduce          | 4.17 us                                                | 3.22 us: 1.30x faster                                               |
| nqueens                  | 106 ms                                                 | 81.9 ms: 1.29x faster                                               |
| sqlglot_normalize        | 143 ms                                                 | 111 ms: 1.29x faster                                                |
| genshi_xml               | 66.0 ms                                                | 51.4 ms: 1.29x faster                                               |
| dulwich_log              | 84.3 ms                                                | 66.0 ms: 1.28x faster                                               |
| sympy_integrate          | 25.8 ms                                                | 20.4 ms: 1.26x faster                                               |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 5.17 ms: 1.25x faster                                               |
| sympy_sum                | 196 ms                                                 | 157 ms: 1.25x faster                                                |
| sqlglot_optimize         | 69.2 ms                                                | 55.3 ms: 1.25x faster                                               |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                               |
| scimark_fft              | 466 ms                                                 | 378 ms: 1.23x faster                                                |
| sympy_str                | 346 ms                                                 | 282 ms: 1.23x faster                                                |
| djangocms                | 38.4 us                                                | 31.4 us: 1.22x faster                                               |
| mypy2                    | 894 ms                                                 | 736 ms: 1.22x faster                                                |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                               |
| dask                     | 441 ms                                                 | 367 ms: 1.20x faster                                                |
| sympy_expand             | 566 ms                                                 | 475 ms: 1.19x faster                                                |
| bench_thread_pool        | 986 us                                                 | 836 us: 1.18x faster                                                |
| docutils                 | 3.30 sec                                               | 2.82 sec: 1.17x faster                                              |
| pathlib                  | 20.5 ms                                                | 17.8 ms: 1.15x faster                                               |
| xml_etree_generate       | 99.4 ms                                                | 87.8 ms: 1.13x faster                                               |
| json_loads               | 31.2 us                                                | 27.7 us: 1.13x faster                                               |
| regex_v8                 | 27.8 ms                                                | 25.0 ms: 1.11x faster                                               |
| json                     | 5.69 ms                                                | 5.18 ms: 1.10x faster                                               |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                |
| mdp                      | 2.85 sec                                               | 2.68 sec: 1.06x faster                                              |
| xml_etree_parse          | 168 ms                                                 | 161 ms: 1.04x faster                                                |
| unpickle_list            | 5.20 us                                                | 5.03 us: 1.03x faster                                               |
| sqlite_synth             | 3.02 us                                                | 2.98 us: 1.01x faster                                               |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                                |
| pidigits                 | 191 ms                                                 | 190 ms: 1.00x faster                                                |
| async_generators         | 444 ms                                                 | 447 ms: 1.01x slower                                                |
| pickle_list              | 5.08 us                                                | 5.13 us: 1.01x slower                                               |
| gc_traversal             | 3.62 ms                                                | 3.68 ms: 1.02x slower                                               |
| asyncio_websockets       | 559 ms                                                 | 569 ms: 1.02x slower                                                |
| regex_effbot             | 3.63 ms                                                | 3.73 ms: 1.03x slower                                               |
| create_gc_cycles         | 1.62 ms                                                | 1.74 ms: 1.08x slower                                               |
| pickle                   | 10.7 us                                                | 11.9 us: 1.12x slower                                               |
| unpickle                 | 14.4 us                                                | 16.6 us: 1.16x slower                                               |
| pickle_dict              | 29.6 us                                                | 34.3 us: 1.16x slower                                               |
| python_startup_no_site   | 5.93 ms                                                | 7.08 ms: 1.19x slower                                               |
| telco                    | 7.27 ms                                                | 8.71 ms: 1.20x slower                                               |
| coverage                 | 79.4 ms                                                | 98.0 ms: 1.23x slower                                               |
| Geometric mean           | (ref)                                                  | 1.35x faster                                                        |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240417-3.13.0a6+-5e20f0f/bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: 1.10x
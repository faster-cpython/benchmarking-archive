# Results vs. 3.10.4

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.07x faster
- HPT reliability: 88.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 332 ms: 1.05x faster                                                |
| chameleon      | 9.68 ms                                                | 8.07 ms: 1.20x faster                                               |
| docutils       | 3.30 sec                                               | 3.28 sec: 1.00x faster                                              |
| html5lib       | 88.9 ms                                                | 75.6 ms: 1.18x faster                                               |
| tornado_http   | 136 ms                                                 | 104 ms: 1.31x faster                                                |
| Geometric mean | (ref)                                                  | 1.14x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 400 ms: 1.82x faster                                                |
| async_tree_io           | 1.77 sec                                               | 995 ms: 1.78x faster                                                |
| async_tree_memoization  | 870 ms                                                 | 529 ms: 1.65x faster                                                |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 660 ms: 1.54x faster                                                |
| Geometric mean          | (ref)                                                  | 1.69x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 191 ms                                                 | 195 ms: 1.02x slower                                                |
| float          | 117 ms                                                 | 139 ms: 1.19x slower                                                |
| nbody          | 154 ms                                                 | 203 ms: 1.32x slower                                                |
| Geometric mean | (ref)                                                  | 1.17x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_v8       | 27.8 ms                                                | 27.2 ms: 1.02x faster                                               |
| regex_dna      | 227 ms                                                 | 235 ms: 1.04x slower                                                |
| regex_effbot   | 3.63 ms                                                | 3.88 ms: 1.07x slower                                               |
| regex_compile  | 188 ms                                                 | 223 ms: 1.18x slower                                                |
| Geometric mean | (ref)                                                  | 1.06x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 314 us: 1.54x faster                                                |
| json_dumps           | 14.2 ms                                                | 10.8 ms: 1.32x faster                                               |
| xml_etree_process    | 79.1 ms                                                | 70.4 ms: 1.12x faster                                               |
| json_loads           | 31.2 us                                                | 27.9 us: 1.12x faster                                               |
| xml_etree_parse      | 168 ms                                                 | 163 ms: 1.03x faster                                                |
| pickle_list          | 5.08 us                                                | 5.20 us: 1.02x slower                                               |
| xml_etree_generate   | 99.4 ms                                                | 105 ms: 1.06x slower                                                |
| tomli_loads          | 3.14 sec                                               | 3.41 sec: 1.09x slower                                              |
| pickle               | 10.7 us                                                | 12.1 us: 1.14x slower                                               |
| xml_etree_iterparse  | 115 ms                                                 | 133 ms: 1.15x slower                                                |
| unpickle             | 14.4 us                                                | 16.8 us: 1.17x slower                                               |
| pickle_dict          | 29.6 us                                                | 35.8 us: 1.21x slower                                               |
| unpickle_pure_python | 331 us                                                 | 406 us: 1.23x slower                                                |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                        |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.38x faster                                               |
| python_startup_no_site | 5.93 ms                                                | 7.13 ms: 1.20x slower                                               |
| Geometric mean         | (ref)                                                  | 1.07x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_text     | 31.8 ms                                                | 27.3 ms: 1.16x faster                                               |
| django_template | 48.2 ms                                                | 42.9 ms: 1.12x faster                                               |
| genshi_xml      | 66.0 ms                                                | 64.7 ms: 1.02x faster                                               |
| mako            | 16.3 ms                                                | 20.9 ms: 1.28x slower                                               |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 130 us: 4.19x faster                                                |
| generators               | 80.1 ms                                                | 29.7 ms: 2.69x faster                                               |
| async_tree_none          | 728 ms                                                 | 400 ms: 1.82x faster                                                |
| asyncio_tcp              | 922 ms                                                 | 513 ms: 1.80x faster                                                |
| async_tree_io            | 1.77 sec                                               | 995 ms: 1.78x faster                                                |
| logging_silent           | 190 ns                                                 | 109 ns: 1.73x faster                                                |
| async_tree_memoization   | 870 ms                                                 | 529 ms: 1.65x faster                                                |
| deltablue                | 7.91 ms                                                | 4.94 ms: 1.60x faster                                               |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                               |
| pickle_pure_python       | 484 us                                                 | 314 us: 1.54x faster                                                |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 660 ms: 1.54x faster                                                |
| pylint                   | 551 ms                                                 | 360 ms: 1.53x faster                                                |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                              |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.38x faster                                               |
| raytrace                 | 507 ms                                                 | 374 ms: 1.35x faster                                                |
| sqlglot_parse            | 2.17 ms                                                | 1.63 ms: 1.33x faster                                               |
| json_dumps               | 14.2 ms                                                | 10.8 ms: 1.32x faster                                               |
| tornado_http             | 136 ms                                                 | 104 ms: 1.31x faster                                                |
| sqlglot_transpile        | 2.57 ms                                                | 1.97 ms: 1.31x faster                                               |
| thrift                   | 1.07 ms                                                | 846 us: 1.27x faster                                                |
| scimark_sor              | 220 ms                                                 | 174 ms: 1.27x faster                                                |
| logging_simple           | 8.30 us                                                | 6.72 us: 1.24x faster                                               |
| logging_format           | 9.09 us                                                | 7.42 us: 1.22x faster                                               |
| deepcopy_reduce          | 4.17 us                                                | 3.41 us: 1.22x faster                                               |
| deepcopy                 | 479 us                                                 | 395 us: 1.21x faster                                                |
| chameleon                | 9.68 ms                                                | 8.07 ms: 1.20x faster                                               |
| djangocms                | 38.4 us                                                | 32.1 us: 1.20x faster                                               |
| html5lib                 | 88.9 ms                                                | 75.6 ms: 1.18x faster                                               |
| richards_super           | 94.7 ms                                                | 81.1 ms: 1.17x faster                                               |
| genshi_text              | 31.8 ms                                                | 27.3 ms: 1.16x faster                                               |
| deepcopy_memo            | 58.5 us                                                | 50.5 us: 1.16x faster                                               |
| chaos                    | 115 ms                                                 | 101 ms: 1.14x faster                                                |
| aiohttp                  | 1.44 ms                                                | 1.26 ms: 1.14x faster                                               |
| dask                     | 441 ms                                                 | 388 ms: 1.14x faster                                                |
| pycparser                | 1.58 sec                                               | 1.39 sec: 1.13x faster                                              |
| gunicorn                 | 1.53 ms                                                | 1.36 ms: 1.13x faster                                               |
| xml_etree_process        | 79.1 ms                                                | 70.4 ms: 1.12x faster                                               |
| django_template          | 48.2 ms                                                | 42.9 ms: 1.12x faster                                               |
| json_loads               | 31.2 us                                                | 27.9 us: 1.12x faster                                               |
| dulwich_log              | 84.3 ms                                                | 75.8 ms: 1.11x faster                                               |
| json                     | 5.69 ms                                                | 5.20 ms: 1.09x faster                                               |
| pathlib                  | 20.5 ms                                                | 18.8 ms: 1.09x faster                                               |
| mypy2                    | 894 ms                                                 | 833 ms: 1.07x faster                                                |
| sqlglot_normalize        | 143 ms                                                 | 134 ms: 1.07x faster                                                |
| richards                 | 79.3 ms                                                | 74.5 ms: 1.06x faster                                               |
| go                       | 240 ms                                                 | 226 ms: 1.06x faster                                                |
| bench_thread_pool        | 986 us                                                 | 933 us: 1.06x faster                                                |
| 2to3                     | 348 ms                                                 | 332 ms: 1.05x faster                                                |
| xml_etree_parse          | 168 ms                                                 | 163 ms: 1.03x faster                                                |
| sympy_sum                | 196 ms                                                 | 192 ms: 1.03x faster                                                |
| regex_v8                 | 27.8 ms                                                | 27.2 ms: 1.02x faster                                               |
| genshi_xml               | 66.0 ms                                                | 64.7 ms: 1.02x faster                                               |
| sympy_integrate          | 25.8 ms                                                | 25.5 ms: 1.01x faster                                               |
| sympy_expand             | 566 ms                                                 | 562 ms: 1.01x faster                                                |
| docutils                 | 3.30 sec                                               | 3.28 sec: 1.00x faster                                              |
| sympy_str                | 346 ms                                                 | 349 ms: 1.01x slower                                                |
| asyncio_websockets       | 559 ms                                                 | 568 ms: 1.02x slower                                                |
| pidigits                 | 191 ms                                                 | 195 ms: 1.02x slower                                                |
| pickle_list              | 5.08 us                                                | 5.20 us: 1.02x slower                                               |
| sqlglot_optimize         | 69.2 ms                                                | 71.1 ms: 1.03x slower                                               |
| regex_dna                | 227 ms                                                 | 235 ms: 1.04x slower                                                |
| sqlite_synth             | 3.02 us                                                | 3.16 us: 1.04x slower                                               |
| mdp                      | 2.85 sec                                               | 2.99 sec: 1.05x slower                                              |
| xml_etree_generate       | 99.4 ms                                                | 105 ms: 1.06x slower                                                |
| regex_effbot             | 3.63 ms                                                | 3.88 ms: 1.07x slower                                               |
| tomli_loads              | 3.14 sec                                               | 3.41 sec: 1.09x slower                                              |
| gc_traversal             | 3.62 ms                                                | 3.95 ms: 1.09x slower                                               |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.09x slower                                               |
| pickle                   | 10.7 us                                                | 12.1 us: 1.14x slower                                               |
| async_generators         | 444 ms                                                 | 507 ms: 1.14x slower                                                |
| xml_etree_iterparse      | 115 ms                                                 | 133 ms: 1.15x slower                                                |
| scimark_monte_carlo      | 118 ms                                                 | 138 ms: 1.17x slower                                                |
| unpickle                 | 14.4 us                                                | 16.8 us: 1.17x slower                                               |
| scimark_lu               | 176 ms                                                 | 208 ms: 1.18x slower                                                |
| regex_compile            | 188 ms                                                 | 223 ms: 1.18x slower                                                |
| float                    | 117 ms                                                 | 139 ms: 1.19x slower                                                |
| python_startup_no_site   | 5.93 ms                                                | 7.13 ms: 1.20x slower                                               |
| meteor_contest           | 120 ms                                                 | 144 ms: 1.20x slower                                                |
| pickle_dict              | 29.6 us                                                | 35.8 us: 1.21x slower                                               |
| pprint_safe_repr         | 1.02 sec                                               | 1.24 sec: 1.22x slower                                              |
| comprehensions           | 28.8 us                                                | 35.2 us: 1.23x slower                                               |
| unpickle_pure_python     | 331 us                                                 | 406 us: 1.23x slower                                                |
| pyflate                  | 716 ms                                                 | 880 ms: 1.23x slower                                                |
| pprint_pformat           | 2.10 sec                                               | 2.59 sec: 1.23x slower                                              |
| coverage                 | 79.4 ms                                                | 99.3 ms: 1.25x slower                                               |
| mako                     | 16.3 ms                                                | 20.9 ms: 1.28x slower                                               |
| nbody                    | 154 ms                                                 | 203 ms: 1.32x slower                                                |
| telco                    | 7.27 ms                                                | 9.71 ms: 1.34x slower                                               |
| scimark_fft              | 466 ms                                                 | 630 ms: 1.35x slower                                                |
| spectral_norm            | 170 ms                                                 | 237 ms: 1.39x slower                                                |
| fannkuch                 | 532 ms                                                 | 754 ms: 1.42x slower                                                |
| nqueens                  | 106 ms                                                 | 151 ms: 1.43x slower                                                |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 9.27 ms: 1.43x slower                                               |
| hexiom                   | 10.4 ms                                                | 15.1 ms: 1.45x slower                                               |
| Geometric mean           | (ref)                                                  | 1.07x faster                                                        |

Benchmark hidden because not significant (3): crypto_pyaes, bench_mp_pool, unpickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240417-3.13.0a6+-5e20f0f-PYTHON_UOPS/bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 88.77% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x
# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_cache
- machine: linux-x86_64
- commit hash: f4c10d5
- commit date: 2024-04-18
- overall geometric mean: 1.32x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 278 ms: 1.25x faster                                                 |
| chameleon      | 9.68 ms                                                | 7.08 ms: 1.37x faster                                                |
| docutils       | 3.30 sec                                               | 2.92 sec: 1.13x faster                                               |
| html5lib       | 88.9 ms                                                | 67.4 ms: 1.32x faster                                                |
| tornado_http   | 136 ms                                                 | 96.6 ms: 1.41x faster                                                |
| Geometric mean | (ref)                                                  | 1.29x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 362 ms: 2.01x faster                                                 |
| async_tree_io           | 1.77 sec                                               | 941 ms: 1.88x faster                                                 |
| async_tree_memoization  | 870 ms                                                 | 468 ms: 1.86x faster                                                 |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 620 ms: 1.64x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.84x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 87.3 ms: 1.76x faster                                                |
| float          | 117 ms                                                 | 77.7 ms: 1.51x faster                                                |
| pidigits       | 191 ms                                                 | 210 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.34x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 144 ms: 1.31x faster                                                 |
| regex_v8       | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                |
| regex_dna      | 227 ms                                                 | 221 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.10x faster                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 305 us: 1.59x faster                                                 |
| tomli_loads          | 3.14 sec                                               | 2.01 sec: 1.56x faster                                               |
| unpickle_pure_python | 331 us                                                 | 236 us: 1.40x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                |
| xml_etree_process    | 79.1 ms                                                | 60.4 ms: 1.31x faster                                                |
| xml_etree_generate   | 99.4 ms                                                | 88.1 ms: 1.13x faster                                                |
| json_loads           | 31.2 us                                                | 27.7 us: 1.13x faster                                                |
| xml_etree_iterparse  | 115 ms                                                 | 109 ms: 1.06x faster                                                 |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                 |
| unpickle_list        | 5.20 us                                                | 5.27 us: 1.01x slower                                                |
| pickle_list          | 5.08 us                                                | 5.33 us: 1.05x slower                                                |
| unpickle             | 14.4 us                                                | 15.7 us: 1.10x slower                                                |
| pickle               | 10.7 us                                                | 12.0 us: 1.13x slower                                                |
| pickle_dict          | 29.6 us                                                | 36.0 us: 1.22x slower                                                |
| Geometric mean       | (ref)                                                  | 1.13x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                |
| python_startup_no_site | 5.93 ms                                                | 7.69 ms: 1.30x slower                                                |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.5 ms: 1.42x faster                                                |
| django_template | 48.2 ms                                                | 36.2 ms: 1.33x faster                                                |
| genshi_text     | 31.8 ms                                                | 24.4 ms: 1.30x faster                                                |
| genshi_xml      | 66.0 ms                                                | 54.9 ms: 1.20x faster                                                |
| Geometric mean  | (ref)                                                  | 1.31x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 112 us: 4.87x faster                                                 |
| generators               | 80.1 ms                                                | 30.5 ms: 2.63x faster                                                |
| deltablue                | 7.91 ms                                                | 3.69 ms: 2.15x faster                                                |
| async_tree_none          | 728 ms                                                 | 362 ms: 2.01x faster                                                 |
| richards_super           | 94.7 ms                                                | 49.0 ms: 1.93x faster                                                |
| async_tree_io            | 1.77 sec                                               | 941 ms: 1.88x faster                                                 |
| async_tree_memoization   | 870 ms                                                 | 468 ms: 1.86x faster                                                 |
| logging_silent           | 190 ns                                                 | 103 ns: 1.84x faster                                                 |
| raytrace                 | 507 ms                                                 | 275 ms: 1.84x faster                                                 |
| chaos                    | 115 ms                                                 | 63.3 ms: 1.82x faster                                                |
| richards                 | 79.3 ms                                                | 43.6 ms: 1.82x faster                                                |
| asyncio_tcp              | 922 ms                                                 | 512 ms: 1.80x faster                                                 |
| nbody                    | 154 ms                                                 | 87.3 ms: 1.76x faster                                                |
| scimark_monte_carlo      | 118 ms                                                 | 67.9 ms: 1.74x faster                                                |
| crypto_pyaes             | 128 ms                                                 | 73.9 ms: 1.73x faster                                                |
| scimark_sor              | 220 ms                                                 | 132 ms: 1.66x faster                                                 |
| pylint                   | 551 ms                                                 | 335 ms: 1.65x faster                                                 |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 620 ms: 1.64x faster                                                 |
| sqlglot_parse            | 2.17 ms                                                | 1.33 ms: 1.63x faster                                                |
| go                       | 240 ms                                                 | 148 ms: 1.63x faster                                                 |
| pickle_pure_python       | 484 us                                                 | 305 us: 1.59x faster                                                 |
| comprehensions           | 28.8 us                                                | 18.3 us: 1.57x faster                                                |
| tomli_loads              | 3.14 sec                                               | 2.01 sec: 1.56x faster                                               |
| sqlglot_transpile        | 2.57 ms                                                | 1.65 ms: 1.56x faster                                                |
| deepcopy_memo            | 58.5 us                                                | 38.2 us: 1.53x faster                                                |
| coroutines               | 35.1 ms                                                | 23.1 ms: 1.52x faster                                                |
| float                    | 117 ms                                                 | 77.7 ms: 1.51x faster                                                |
| pyflate                  | 716 ms                                                 | 479 ms: 1.50x faster                                                 |
| spectral_norm            | 170 ms                                                 | 116 ms: 1.47x faster                                                 |
| hexiom                   | 10.4 ms                                                | 7.09 ms: 1.47x faster                                                |
| logging_simple           | 8.30 us                                                | 5.75 us: 1.44x faster                                                |
| logging_format           | 9.09 us                                                | 6.36 us: 1.43x faster                                                |
| mako                     | 16.3 ms                                                | 11.5 ms: 1.42x faster                                                |
| tornado_http             | 136 ms                                                 | 96.6 ms: 1.41x faster                                                |
| unpickle_pure_python     | 331 us                                                 | 236 us: 1.40x faster                                                 |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                               |
| pprint_pformat           | 2.10 sec                                               | 1.54 sec: 1.37x faster                                               |
| chameleon                | 9.68 ms                                                | 7.08 ms: 1.37x faster                                                |
| fannkuch                 | 532 ms                                                 | 389 ms: 1.37x faster                                                 |
| scimark_fft              | 466 ms                                                 | 341 ms: 1.37x faster                                                 |
| pprint_safe_repr         | 1.02 sec                                               | 751 ms: 1.36x faster                                                 |
| pycparser                | 1.58 sec                                               | 1.17 sec: 1.35x faster                                               |
| deepcopy                 | 479 us                                                 | 356 us: 1.34x faster                                                 |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.83 ms: 1.34x faster                                                |
| json_dumps               | 14.2 ms                                                | 10.6 ms: 1.33x faster                                                |
| django_template          | 48.2 ms                                                | 36.2 ms: 1.33x faster                                                |
| html5lib                 | 88.9 ms                                                | 67.4 ms: 1.32x faster                                                |
| scimark_lu               | 176 ms                                                 | 134 ms: 1.31x faster                                                 |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.31x faster                                                |
| xml_etree_process        | 79.1 ms                                                | 60.4 ms: 1.31x faster                                                |
| deepcopy_reduce          | 4.17 us                                                | 3.19 us: 1.31x faster                                                |
| regex_compile            | 188 ms                                                 | 144 ms: 1.31x faster                                                 |
| thrift                   | 1.07 ms                                                | 821 us: 1.31x faster                                                 |
| genshi_text              | 31.8 ms                                                | 24.4 ms: 1.30x faster                                                |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.26x faster                                                 |
| 2to3                     | 348 ms                                                 | 278 ms: 1.25x faster                                                 |
| dulwich_log              | 84.3 ms                                                | 69.9 ms: 1.21x faster                                                |
| genshi_xml               | 66.0 ms                                                | 54.9 ms: 1.20x faster                                                |
| sqlglot_optimize         | 69.2 ms                                                | 57.8 ms: 1.20x faster                                                |
| djangocms                | 38.4 us                                                | 32.2 us: 1.19x faster                                                |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                |
| dask                     | 441 ms                                                 | 374 ms: 1.18x faster                                                 |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                                |
| sympy_integrate          | 25.8 ms                                                | 22.1 ms: 1.17x faster                                                |
| sympy_sum                | 196 ms                                                 | 170 ms: 1.16x faster                                                 |
| sympy_str                | 346 ms                                                 | 299 ms: 1.16x faster                                                 |
| pathlib                  | 20.5 ms                                                | 17.8 ms: 1.15x faster                                                |
| mypy2                    | 894 ms                                                 | 782 ms: 1.14x faster                                                 |
| bench_thread_pool        | 986 us                                                 | 863 us: 1.14x faster                                                 |
| nqueens                  | 106 ms                                                 | 93.0 ms: 1.14x faster                                                |
| sympy_expand             | 566 ms                                                 | 501 ms: 1.13x faster                                                 |
| xml_etree_generate       | 99.4 ms                                                | 88.1 ms: 1.13x faster                                                |
| docutils                 | 3.30 sec                                               | 2.92 sec: 1.13x faster                                               |
| json_loads               | 31.2 us                                                | 27.7 us: 1.13x faster                                                |
| json                     | 5.69 ms                                                | 5.09 ms: 1.12x faster                                                |
| regex_v8                 | 27.8 ms                                                | 25.0 ms: 1.11x faster                                                |
| mdp                      | 2.85 sec                                               | 2.64 sec: 1.08x faster                                               |
| meteor_contest           | 120 ms                                                 | 113 ms: 1.06x faster                                                 |
| xml_etree_iterparse      | 115 ms                                                 | 109 ms: 1.06x faster                                                 |
| sqlite_synth             | 3.02 us                                                | 2.88 us: 1.05x faster                                                |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                 |
| regex_dna                | 227 ms                                                 | 221 ms: 1.03x faster                                                 |
| unpickle_list            | 5.20 us                                                | 5.27 us: 1.01x slower                                                |
| asyncio_websockets       | 559 ms                                                 | 568 ms: 1.02x slower                                                 |
| async_generators         | 444 ms                                                 | 460 ms: 1.04x slower                                                 |
| pickle_list              | 5.08 us                                                | 5.33 us: 1.05x slower                                                |
| gc_traversal             | 3.62 ms                                                | 3.85 ms: 1.06x slower                                                |
| create_gc_cycles         | 1.62 ms                                                | 1.77 ms: 1.09x slower                                                |
| unpickle                 | 14.4 us                                                | 15.7 us: 1.10x slower                                                |
| pidigits                 | 191 ms                                                 | 210 ms: 1.10x slower                                                 |
| pickle                   | 10.7 us                                                | 12.0 us: 1.13x slower                                                |
| telco                    | 7.27 ms                                                | 8.56 ms: 1.18x slower                                                |
| pickle_dict              | 29.6 us                                                | 36.0 us: 1.22x slower                                                |
| coverage                 | 79.4 ms                                                | 98.2 ms: 1.24x slower                                                |
| python_startup_no_site   | 5.93 ms                                                | 7.69 ms: 1.30x slower                                                |
| Geometric mean           | (ref)                                                  | 1.32x faster                                                         |

Benchmark hidden because not significant (2): bench_mp_pool, regex_effbot
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240418-3.13.0a6+-f4c10d5-JIT/bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.26x
- 95% likely to have a speedup of 1.24x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: 1.23x
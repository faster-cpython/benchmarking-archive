# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.30x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 282 ms: 1.24x faster                                                     |
| chameleon      | 9.68 ms                                                | 7.06 ms: 1.37x faster                                                    |
| docutils       | 3.30 sec                                               | 2.94 sec: 1.12x faster                                                   |
| html5lib       | 88.9 ms                                                | 67.6 ms: 1.31x faster                                                    |
| tornado_http   | 136 ms                                                 | 96.5 ms: 1.41x faster                                                    |
| Geometric mean | (ref)                                                  | 1.29x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 357 ms: 2.04x faster                                                     |
| async_tree_io           | 1.77 sec                                               | 928 ms: 1.91x faster                                                     |
| async_tree_memoization  | 870 ms                                                 | 458 ms: 1.90x faster                                                     |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.66x faster                                                     |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 92.4 ms: 1.66x faster                                                    |
| float          | 117 ms                                                 | 77.0 ms: 1.52x faster                                                    |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                  | 1.37x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 149 ms: 1.26x faster                                                     |
| regex_v8       | 27.8 ms                                                | 24.7 ms: 1.13x faster                                                    |
| regex_dna      | 227 ms                                                 | 221 ms: 1.02x faster                                                     |
| regex_effbot   | 3.63 ms                                                | 3.75 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                  | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 308 us: 1.57x faster                                                     |
| tomli_loads          | 3.14 sec                                               | 2.06 sec: 1.53x faster                                                   |
| unpickle_pure_python | 331 us                                                 | 238 us: 1.39x faster                                                     |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                    |
| xml_etree_process    | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                    |
| xml_etree_generate   | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                    |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                     |
| json_loads           | 31.2 us                                                | 29.0 us: 1.08x faster                                                    |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                     |
| pickle_list          | 5.08 us                                                | 4.96 us: 1.02x faster                                                    |
| unpickle             | 14.4 us                                                | 15.0 us: 1.05x slower                                                    |
| pickle               | 10.7 us                                                | 11.8 us: 1.10x slower                                                    |
| pickle_dict          | 29.6 us                                                | 34.1 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                             |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                    |
| python_startup_no_site | 5.93 ms                                                | 9.51 ms: 1.60x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 11.0 ms: 1.49x faster                                                    |
| django_template | 48.2 ms                                                | 37.1 ms: 1.30x faster                                                    |
| genshi_text     | 31.8 ms                                                | 24.8 ms: 1.29x faster                                                    |
| genshi_xml      | 66.0 ms                                                | 55.7 ms: 1.19x faster                                                    |
| Geometric mean  | (ref)                                                  | 1.31x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.79x faster                                                     |
| generators               | 80.1 ms                                                | 30.1 ms: 2.66x faster                                                    |
| deltablue                | 7.91 ms                                                | 3.48 ms: 2.27x faster                                                    |
| async_tree_none          | 728 ms                                                 | 357 ms: 2.04x faster                                                     |
| async_tree_io            | 1.77 sec                                               | 928 ms: 1.91x faster                                                     |
| async_tree_memoization   | 870 ms                                                 | 458 ms: 1.90x faster                                                     |
| logging_silent           | 190 ns                                                 | 103 ns: 1.85x faster                                                     |
| pylint                   | 551 ms                                                 | 306 ms: 1.80x faster                                                     |
| chaos                    | 115 ms                                                 | 64.1 ms: 1.80x faster                                                    |
| richards_super           | 94.7 ms                                                | 53.0 ms: 1.79x faster                                                    |
| asyncio_tcp              | 922 ms                                                 | 518 ms: 1.78x faster                                                     |
| raytrace                 | 507 ms                                                 | 296 ms: 1.71x faster                                                     |
| richards                 | 79.3 ms                                                | 46.4 ms: 1.71x faster                                                    |
| crypto_pyaes             | 128 ms                                                 | 75.3 ms: 1.70x faster                                                    |
| scimark_monte_carlo      | 118 ms                                                 | 70.8 ms: 1.67x faster                                                    |
| nbody                    | 154 ms                                                 | 92.4 ms: 1.66x faster                                                    |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.66x faster                                                     |
| sqlglot_parse            | 2.17 ms                                                | 1.32 ms: 1.65x faster                                                    |
| scimark_sor              | 220 ms                                                 | 138 ms: 1.59x faster                                                     |
| pickle_pure_python       | 484 us                                                 | 308 us: 1.57x faster                                                     |
| sqlglot_transpile        | 2.57 ms                                                | 1.64 ms: 1.57x faster                                                    |
| comprehensions           | 28.8 us                                                | 18.5 us: 1.55x faster                                                    |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                    |
| tomli_loads              | 3.14 sec                                               | 2.06 sec: 1.53x faster                                                   |
| float                    | 117 ms                                                 | 77.0 ms: 1.52x faster                                                    |
| go                       | 240 ms                                                 | 158 ms: 1.52x faster                                                     |
| spectral_norm            | 170 ms                                                 | 114 ms: 1.49x faster                                                     |
| deepcopy_memo            | 58.5 us                                                | 39.3 us: 1.49x faster                                                    |
| mako                     | 16.3 ms                                                | 11.0 ms: 1.49x faster                                                    |
| pyflate                  | 716 ms                                                 | 491 ms: 1.46x faster                                                     |
| logging_simple           | 8.30 us                                                | 5.84 us: 1.42x faster                                                    |
| hexiom                   | 10.4 ms                                                | 7.33 ms: 1.42x faster                                                    |
| logging_format           | 9.09 us                                                | 6.42 us: 1.42x faster                                                    |
| tornado_http             | 136 ms                                                 | 96.5 ms: 1.41x faster                                                    |
| unpickle_pure_python     | 331 us                                                 | 238 us: 1.39x faster                                                     |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                   |
| chameleon                | 9.68 ms                                                | 7.06 ms: 1.37x faster                                                    |
| fannkuch                 | 532 ms                                                 | 390 ms: 1.36x faster                                                     |
| scimark_fft              | 466 ms                                                 | 343 ms: 1.36x faster                                                     |
| pprint_pformat           | 2.10 sec                                               | 1.55 sec: 1.36x faster                                                   |
| scimark_lu               | 176 ms                                                 | 130 ms: 1.35x faster                                                     |
| deepcopy                 | 479 us                                                 | 359 us: 1.33x faster                                                     |
| pycparser                | 1.58 sec                                               | 1.18 sec: 1.33x faster                                                   |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.87 ms: 1.33x faster                                                    |
| pprint_safe_repr         | 1.02 sec                                               | 766 ms: 1.33x faster                                                     |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                    |
| xml_etree_process        | 79.1 ms                                                | 59.8 ms: 1.32x faster                                                    |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                    |
| thrift                   | 1.07 ms                                                | 814 us: 1.32x faster                                                     |
| html5lib                 | 88.9 ms                                                | 67.6 ms: 1.31x faster                                                    |
| deepcopy_reduce          | 4.17 us                                                | 3.18 us: 1.31x faster                                                    |
| django_template          | 48.2 ms                                                | 37.1 ms: 1.30x faster                                                    |
| genshi_text              | 31.8 ms                                                | 24.8 ms: 1.29x faster                                                    |
| regex_compile            | 188 ms                                                 | 149 ms: 1.26x faster                                                     |
| sqlglot_normalize        | 143 ms                                                 | 114 ms: 1.26x faster                                                     |
| 2to3                     | 348 ms                                                 | 282 ms: 1.24x faster                                                     |
| sqlglot_optimize         | 69.2 ms                                                | 58.0 ms: 1.19x faster                                                    |
| genshi_xml               | 66.0 ms                                                | 55.7 ms: 1.19x faster                                                    |
| djangocms                | 38.4 us                                                | 32.5 us: 1.18x faster                                                    |
| dulwich_log              | 84.3 ms                                                | 71.4 ms: 1.18x faster                                                    |
| aiohttp                  | 1.44 ms                                                | 1.22 ms: 1.18x faster                                                    |
| sympy_str                | 346 ms                                                 | 294 ms: 1.18x faster                                                     |
| sympy_sum                | 196 ms                                                 | 167 ms: 1.17x faster                                                     |
| dask                     | 441 ms                                                 | 378 ms: 1.17x faster                                                     |
| gunicorn                 | 1.53 ms                                                | 1.32 ms: 1.16x faster                                                    |
| sympy_integrate          | 25.8 ms                                                | 22.3 ms: 1.16x faster                                                    |
| bench_thread_pool        | 986 us                                                 | 859 us: 1.15x faster                                                     |
| xml_etree_generate       | 99.4 ms                                                | 86.7 ms: 1.15x faster                                                    |
| nqueens                  | 106 ms                                                 | 93.5 ms: 1.13x faster                                                    |
| sympy_expand             | 566 ms                                                 | 501 ms: 1.13x faster                                                     |
| regex_v8                 | 27.8 ms                                                | 24.7 ms: 1.13x faster                                                    |
| docutils                 | 3.30 sec                                               | 2.94 sec: 1.12x faster                                                   |
| mypy2                    | 894 ms                                                 | 812 ms: 1.10x faster                                                     |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                     |
| json_loads               | 31.2 us                                                | 29.0 us: 1.08x faster                                                    |
| meteor_contest           | 120 ms                                                 | 111 ms: 1.07x faster                                                     |
| pathlib                  | 20.5 ms                                                | 19.1 ms: 1.07x faster                                                    |
| sqlite_synth             | 3.02 us                                                | 2.86 us: 1.06x faster                                                    |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                     |
| json                     | 5.69 ms                                                | 5.54 ms: 1.03x faster                                                    |
| regex_dna                | 227 ms                                                 | 221 ms: 1.02x faster                                                     |
| pickle_list              | 5.08 us                                                | 4.96 us: 1.02x faster                                                    |
| mdp                      | 2.85 sec                                               | 2.82 sec: 1.01x faster                                                   |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                     |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                     |
| regex_effbot             | 3.63 ms                                                | 3.75 ms: 1.03x slower                                                    |
| async_generators         | 444 ms                                                 | 458 ms: 1.03x slower                                                     |
| create_gc_cycles         | 1.62 ms                                                | 1.68 ms: 1.04x slower                                                    |
| unpickle                 | 14.4 us                                                | 15.0 us: 1.05x slower                                                    |
| gc_traversal             | 3.62 ms                                                | 3.99 ms: 1.10x slower                                                    |
| pickle                   | 10.7 us                                                | 11.8 us: 1.10x slower                                                    |
| pickle_dict              | 29.6 us                                                | 34.1 us: 1.15x slower                                                    |
| telco                    | 7.27 ms                                                | 8.71 ms: 1.20x slower                                                    |
| coverage                 | 79.4 ms                                                | 95.8 ms: 1.21x slower                                                    |
| unpack_sequence          | 60.0 ns                                                | 85.6 ns: 1.43x slower                                                    |
| python_startup_no_site   | 5.93 ms                                                | 9.51 ms: 1.60x slower                                                    |
| Geometric mean           | (ref)                                                  | 1.30x faster                                                             |

Benchmark hidden because not significant (2): unpickle_list, bench_mp_pool
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.19x

# Memory
- memory change: 1.20x
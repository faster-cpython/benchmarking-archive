# Results vs. 3.10.4

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 281 ms: 1.24x faster                                                     |
| chameleon      | 9.68 ms                                                | 6.90 ms: 1.40x faster                                                    |
| docutils       | 3.30 sec                                               | 2.97 sec: 1.11x faster                                                   |
| html5lib       | 88.9 ms                                                | 68.6 ms: 1.30x faster                                                    |
| tornado_http   | 136 ms                                                 | 97.2 ms: 1.40x faster                                                    |
| Geometric mean | (ref)                                                  | 1.29x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 358 ms: 2.03x faster                                                     |
| async_tree_memoization  | 870 ms                                                 | 460 ms: 1.89x faster                                                     |
| async_tree_io           | 1.77 sec                                               | 940 ms: 1.88x faster                                                     |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 617 ms: 1.65x faster                                                     |
| Geometric mean          | (ref)                                                  | 1.86x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 91.3 ms: 1.68x faster                                                    |
| float          | 117 ms                                                 | 76.5 ms: 1.53x faster                                                    |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                  | 1.37x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 145 ms: 1.30x faster                                                     |
| regex_v8       | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                    |
| regex_dna      | 227 ms                                                 | 223 ms: 1.02x faster                                                     |
| regex_effbot   | 3.63 ms                                                | 3.70 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                  | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 305 us: 1.59x faster                                                     |
| tomli_loads          | 3.14 sec                                               | 2.06 sec: 1.53x faster                                                   |
| unpickle_pure_python | 331 us                                                 | 242 us: 1.36x faster                                                     |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.36x faster                                                    |
| xml_etree_process    | 79.1 ms                                                | 60.2 ms: 1.31x faster                                                    |
| xml_etree_generate   | 99.4 ms                                                | 87.8 ms: 1.13x faster                                                    |
| json_loads           | 31.2 us                                                | 28.1 us: 1.11x faster                                                    |
| xml_etree_iterparse  | 115 ms                                                 | 107 ms: 1.08x faster                                                     |
| pickle_list          | 5.08 us                                                | 4.90 us: 1.04x faster                                                    |
| xml_etree_parse      | 168 ms                                                 | 162 ms: 1.04x faster                                                     |
| unpickle_list        | 5.20 us                                                | 5.32 us: 1.02x slower                                                    |
| unpickle             | 14.4 us                                                | 15.6 us: 1.09x slower                                                    |
| pickle               | 10.7 us                                                | 11.6 us: 1.09x slower                                                    |
| pickle_dict          | 29.6 us                                                | 34.2 us: 1.15x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                    |
| python_startup_no_site | 5.93 ms                                                | 9.57 ms: 1.61x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 10.6 ms: 1.54x faster                                                    |
| genshi_text    | 31.8 ms                                                | 24.7 ms: 1.29x faster                                                    |
| genshi_xml     | 66.0 ms                                                | 55.4 ms: 1.19x faster                                                    |
| Geometric mean | (ref)                                                  | 1.33x faster                                                             |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 116 us: 4.70x faster                                                     |
| generators               | 80.1 ms                                                | 30.1 ms: 2.66x faster                                                    |
| deltablue                | 7.91 ms                                                | 3.82 ms: 2.07x faster                                                    |
| async_tree_none          | 728 ms                                                 | 358 ms: 2.03x faster                                                     |
| richards_super           | 94.7 ms                                                | 49.7 ms: 1.91x faster                                                    |
| async_tree_memoization   | 870 ms                                                 | 460 ms: 1.89x faster                                                     |
| async_tree_io            | 1.77 sec                                               | 940 ms: 1.88x faster                                                     |
| logging_silent           | 190 ns                                                 | 101 ns: 1.87x faster                                                     |
| raytrace                 | 507 ms                                                 | 276 ms: 1.84x faster                                                     |
| richards                 | 79.3 ms                                                | 43.3 ms: 1.83x faster                                                    |
| chaos                    | 115 ms                                                 | 63.1 ms: 1.83x faster                                                    |
| pylint                   | 551 ms                                                 | 304 ms: 1.82x faster                                                     |
| asyncio_tcp              | 922 ms                                                 | 527 ms: 1.75x faster                                                     |
| scimark_monte_carlo      | 118 ms                                                 | 68.2 ms: 1.73x faster                                                    |
| crypto_pyaes             | 128 ms                                                 | 76.0 ms: 1.68x faster                                                    |
| nbody                    | 154 ms                                                 | 91.3 ms: 1.68x faster                                                    |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 617 ms: 1.65x faster                                                     |
| sqlglot_parse            | 2.17 ms                                                | 1.33 ms: 1.63x faster                                                    |
| go                       | 240 ms                                                 | 149 ms: 1.61x faster                                                     |
| scimark_sor              | 220 ms                                                 | 138 ms: 1.59x faster                                                     |
| pickle_pure_python       | 484 us                                                 | 305 us: 1.59x faster                                                     |
| sqlglot_transpile        | 2.57 ms                                                | 1.65 ms: 1.56x faster                                                    |
| coroutines               | 35.1 ms                                                | 22.5 ms: 1.56x faster                                                    |
| comprehensions           | 28.8 us                                                | 18.6 us: 1.55x faster                                                    |
| mako                     | 16.3 ms                                                | 10.6 ms: 1.54x faster                                                    |
| float                    | 117 ms                                                 | 76.5 ms: 1.53x faster                                                    |
| tomli_loads              | 3.14 sec                                               | 2.06 sec: 1.53x faster                                                   |
| spectral_norm            | 170 ms                                                 | 113 ms: 1.51x faster                                                     |
| pyflate                  | 716 ms                                                 | 478 ms: 1.50x faster                                                     |
| deepcopy_memo            | 58.5 us                                                | 39.2 us: 1.49x faster                                                    |
| hexiom                   | 10.4 ms                                                | 7.17 ms: 1.45x faster                                                    |
| chameleon                | 9.68 ms                                                | 6.90 ms: 1.40x faster                                                    |
| tornado_http             | 136 ms                                                 | 97.2 ms: 1.40x faster                                                    |
| logging_simple           | 8.30 us                                                | 5.93 us: 1.40x faster                                                    |
| logging_format           | 9.09 us                                                | 6.54 us: 1.39x faster                                                    |
| scimark_fft              | 466 ms                                                 | 337 ms: 1.38x faster                                                     |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                   |
| unpickle_pure_python     | 331 us                                                 | 242 us: 1.36x faster                                                     |
| pprint_pformat           | 2.10 sec                                               | 1.55 sec: 1.36x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.36x faster                                                    |
| scimark_lu               | 176 ms                                                 | 130 ms: 1.35x faster                                                     |
| pprint_safe_repr         | 1.02 sec                                               | 754 ms: 1.35x faster                                                     |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.86 ms: 1.33x faster                                                    |
| fannkuch                 | 532 ms                                                 | 403 ms: 1.32x faster                                                     |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                    |
| xml_etree_process        | 79.1 ms                                                | 60.2 ms: 1.31x faster                                                    |
| thrift                   | 1.07 ms                                                | 816 us: 1.31x faster                                                     |
| regex_compile            | 188 ms                                                 | 145 ms: 1.30x faster                                                     |
| html5lib                 | 88.9 ms                                                | 68.6 ms: 1.30x faster                                                    |
| deepcopy                 | 479 us                                                 | 370 us: 1.30x faster                                                     |
| genshi_text              | 31.8 ms                                                | 24.7 ms: 1.29x faster                                                    |
| pycparser                | 1.58 sec                                               | 1.23 sec: 1.28x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.27 us: 1.27x faster                                                    |
| sqlglot_normalize        | 143 ms                                                 | 115 ms: 1.24x faster                                                     |
| 2to3                     | 348 ms                                                 | 281 ms: 1.24x faster                                                     |
| dulwich_log              | 84.3 ms                                                | 70.4 ms: 1.20x faster                                                    |
| genshi_xml               | 66.0 ms                                                | 55.4 ms: 1.19x faster                                                    |
| sqlglot_optimize         | 69.2 ms                                                | 58.1 ms: 1.19x faster                                                    |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                    |
| gunicorn                 | 1.53 ms                                                | 1.31 ms: 1.17x faster                                                    |
| dask                     | 441 ms                                                 | 379 ms: 1.16x faster                                                     |
| sympy_str                | 346 ms                                                 | 300 ms: 1.15x faster                                                     |
| sympy_sum                | 196 ms                                                 | 171 ms: 1.15x faster                                                     |
| bench_thread_pool        | 986 us                                                 | 864 us: 1.14x faster                                                     |
| sympy_integrate          | 25.8 ms                                                | 22.6 ms: 1.14x faster                                                    |
| nqueens                  | 106 ms                                                 | 93.1 ms: 1.14x faster                                                    |
| xml_etree_generate       | 99.4 ms                                                | 87.8 ms: 1.13x faster                                                    |
| sympy_expand             | 566 ms                                                 | 504 ms: 1.12x faster                                                     |
| json_loads               | 31.2 us                                                | 28.1 us: 1.11x faster                                                    |
| docutils                 | 3.30 sec                                               | 2.97 sec: 1.11x faster                                                   |
| mypy2                    | 894 ms                                                 | 812 ms: 1.10x faster                                                     |
| regex_v8                 | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                    |
| json                     | 5.69 ms                                                | 5.26 ms: 1.08x faster                                                    |
| xml_etree_iterparse      | 115 ms                                                 | 107 ms: 1.08x faster                                                     |
| mdp                      | 2.85 sec                                               | 2.66 sec: 1.07x faster                                                   |
| meteor_contest           | 120 ms                                                 | 113 ms: 1.06x faster                                                     |
| pathlib                  | 20.5 ms                                                | 19.5 ms: 1.05x faster                                                    |
| sqlite_synth             | 3.02 us                                                | 2.90 us: 1.04x faster                                                    |
| pickle_list              | 5.08 us                                                | 4.90 us: 1.04x faster                                                    |
| xml_etree_parse          | 168 ms                                                 | 162 ms: 1.04x faster                                                     |
| regex_dna                | 227 ms                                                 | 223 ms: 1.02x faster                                                     |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                     |
| gc_traversal             | 3.62 ms                                                | 3.61 ms: 1.00x faster                                                    |
| asyncio_websockets       | 559 ms                                                 | 567 ms: 1.01x slower                                                     |
| regex_effbot             | 3.63 ms                                                | 3.70 ms: 1.02x slower                                                    |
| unpickle_list            | 5.20 us                                                | 5.32 us: 1.02x slower                                                    |
| async_generators         | 444 ms                                                 | 464 ms: 1.05x slower                                                     |
| create_gc_cycles         | 1.62 ms                                                | 1.76 ms: 1.08x slower                                                    |
| unpickle                 | 14.4 us                                                | 15.6 us: 1.09x slower                                                    |
| pickle                   | 10.7 us                                                | 11.6 us: 1.09x slower                                                    |
| pickle_dict              | 29.6 us                                                | 34.2 us: 1.15x slower                                                    |
| telco                    | 7.27 ms                                                | 8.58 ms: 1.18x slower                                                    |
| coverage                 | 79.4 ms                                                | 99.0 ms: 1.25x slower                                                    |
| python_startup_no_site   | 5.93 ms                                                | 9.57 ms: 1.61x slower                                                    |
| Geometric mean           | (ref)                                                  | 1.31x faster                                                             |

Benchmark hidden because not significant (1): bench_mp_pool
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.24x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.19x

# Memory
- memory change: 1.18x
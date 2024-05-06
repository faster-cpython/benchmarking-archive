# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_pystats_misses
- machine: linux-x86_64
- commit hash: ee60448
- commit date: 2024-04-02
- overall geometric mean: 1.36x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 267 ms: 1.30x faster                                                   |
| chameleon      | 9.68 ms                                                | 6.90 ms: 1.40x faster                                                  |
| docutils       | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                 |
| html5lib       | 88.9 ms                                                | 67.1 ms: 1.32x faster                                                  |
| tornado_http   | 136 ms                                                 | 94.4 ms: 1.44x faster                                                  |
| Geometric mean | (ref)                                                  | 1.33x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 348 ms: 2.10x faster                                                   |
| async_tree_io           | 1.77 sec                                               | 916 ms: 1.93x faster                                                   |
| async_tree_memoization  | 870 ms                                                 | 455 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 608 ms: 1.67x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.90x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 88.1 ms: 1.74x faster                                                  |
| float          | 117 ms                                                 | 77.3 ms: 1.52x faster                                                  |
| pidigits       | 191 ms                                                 | 189 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.39x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 132 ms: 1.42x faster                                                   |
| regex_v8       | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                  |
| regex_dna      | 227 ms                                                 | 224 ms: 1.01x faster                                                   |
| regex_effbot   | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 484 us                                                 | 299 us: 1.62x faster                                                   |
| unpickle_pure_python | 331 us                                                 | 216 us: 1.53x faster                                                   |
| tomli_loads          | 3.14 sec                                               | 2.15 sec: 1.46x faster                                                 |
| json_dumps           | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                  |
| xml_etree_process    | 79.1 ms                                                | 59.4 ms: 1.33x faster                                                  |
| xml_etree_generate   | 99.4 ms                                                | 86.3 ms: 1.15x faster                                                  |
| xml_etree_iterparse  | 115 ms                                                 | 106 ms: 1.09x faster                                                   |
| json_loads           | 31.2 us                                                | 28.8 us: 1.08x faster                                                  |
| xml_etree_parse      | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| unpickle_list        | 5.20 us                                                | 5.07 us: 1.03x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.26 us: 1.04x slower                                                  |
| unpickle             | 14.4 us                                                | 15.7 us: 1.09x slower                                                  |
| pickle               | 10.7 us                                                | 12.0 us: 1.13x slower                                                  |
| pickle_dict          | 29.6 us                                                | 35.2 us: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.14x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                  |
| python_startup_no_site | 5.93 ms                                                | 9.00 ms: 1.52x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 16.3 ms                                                | 11.0 ms: 1.49x faster                                                  |
| genshi_text    | 31.8 ms                                                | 23.9 ms: 1.33x faster                                                  |
| genshi_xml     | 66.0 ms                                                | 52.0 ms: 1.27x faster                                                  |
| Geometric mean | (ref)                                                  | 1.36x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 114 us: 4.77x faster                                                   |
| generators               | 80.1 ms                                                | 29.8 ms: 2.69x faster                                                  |
| deltablue                | 7.91 ms                                                | 3.13 ms: 2.53x faster                                                  |
| async_tree_none          | 728 ms                                                 | 348 ms: 2.10x faster                                                   |
| raytrace                 | 507 ms                                                 | 254 ms: 2.00x faster                                                   |
| pylint                   | 551 ms                                                 | 278 ms: 1.98x faster                                                   |
| chaos                    | 115 ms                                                 | 59.4 ms: 1.94x faster                                                  |
| async_tree_io            | 1.77 sec                                               | 916 ms: 1.93x faster                                                   |
| logging_silent           | 190 ns                                                 | 98.6 ns: 1.92x faster                                                  |
| async_tree_memoization   | 870 ms                                                 | 455 ms: 1.91x faster                                                   |
| richards_super           | 94.7 ms                                                | 51.8 ms: 1.83x faster                                                  |
| asyncio_tcp              | 922 ms                                                 | 507 ms: 1.82x faster                                                   |
| scimark_monte_carlo      | 118 ms                                                 | 66.7 ms: 1.77x faster                                                  |
| crypto_pyaes             | 128 ms                                                 | 72.3 ms: 1.77x faster                                                  |
| nbody                    | 154 ms                                                 | 88.1 ms: 1.74x faster                                                  |
| richards                 | 79.3 ms                                                | 45.7 ms: 1.74x faster                                                  |
| sqlglot_parse            | 2.17 ms                                                | 1.25 ms: 1.73x faster                                                  |
| scimark_sor              | 220 ms                                                 | 127 ms: 1.73x faster                                                   |
| comprehensions           | 28.8 us                                                | 16.6 us: 1.73x faster                                                  |
| go                       | 240 ms                                                 | 141 ms: 1.70x faster                                                   |
| hexiom                   | 10.4 ms                                                | 6.12 ms: 1.70x faster                                                  |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 608 ms: 1.67x faster                                                   |
| sqlglot_transpile        | 2.57 ms                                                | 1.57 ms: 1.64x faster                                                  |
| pickle_pure_python       | 484 us                                                 | 299 us: 1.62x faster                                                   |
| scimark_lu               | 176 ms                                                 | 112 ms: 1.58x faster                                                   |
| deepcopy_memo            | 58.5 us                                                | 37.2 us: 1.57x faster                                                  |
| spectral_norm            | 170 ms                                                 | 109 ms: 1.56x faster                                                   |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                  |
| pyflate                  | 716 ms                                                 | 465 ms: 1.54x faster                                                   |
| unpickle_pure_python     | 331 us                                                 | 216 us: 1.53x faster                                                   |
| float                    | 117 ms                                                 | 77.3 ms: 1.52x faster                                                  |
| mako                     | 16.3 ms                                                | 11.0 ms: 1.49x faster                                                  |
| tomli_loads              | 3.14 sec                                               | 2.15 sec: 1.46x faster                                                 |
| tornado_http             | 136 ms                                                 | 94.4 ms: 1.44x faster                                                  |
| logging_simple           | 8.30 us                                                | 5.79 us: 1.43x faster                                                  |
| regex_compile            | 188 ms                                                 | 132 ms: 1.42x faster                                                   |
| logging_format           | 9.09 us                                                | 6.42 us: 1.42x faster                                                  |
| chameleon                | 9.68 ms                                                | 6.90 ms: 1.40x faster                                                  |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.85 sec: 1.39x faster                                                 |
| pprint_pformat           | 2.10 sec                                               | 1.51 sec: 1.39x faster                                                 |
| pprint_safe_repr         | 1.02 sec                                               | 737 ms: 1.38x faster                                                   |
| fannkuch                 | 532 ms                                                 | 386 ms: 1.38x faster                                                   |
| python_startup           | 14.6 ms                                                | 10.6 ms: 1.37x faster                                                  |
| deepcopy                 | 479 us                                                 | 349 us: 1.37x faster                                                   |
| json_dumps               | 14.2 ms                                                | 10.5 ms: 1.35x faster                                                  |
| xml_etree_process        | 79.1 ms                                                | 59.4 ms: 1.33x faster                                                  |
| genshi_text              | 31.8 ms                                                | 23.9 ms: 1.33x faster                                                  |
| sqlglot_normalize        | 143 ms                                                 | 107 ms: 1.33x faster                                                   |
| nqueens                  | 106 ms                                                 | 79.7 ms: 1.33x faster                                                  |
| html5lib                 | 88.9 ms                                                | 67.1 ms: 1.32x faster                                                  |
| thrift                   | 1.07 ms                                                | 810 us: 1.32x faster                                                   |
| deepcopy_reduce          | 4.17 us                                                | 3.19 us: 1.31x faster                                                  |
| 2to3                     | 348 ms                                                 | 267 ms: 1.30x faster                                                   |
| pycparser                | 1.58 sec                                               | 1.21 sec: 1.30x faster                                                 |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.98 ms: 1.30x faster                                                  |
| scimark_fft              | 466 ms                                                 | 361 ms: 1.29x faster                                                   |
| sympy_integrate          | 25.8 ms                                                | 20.0 ms: 1.29x faster                                                  |
| sympy_sum                | 196 ms                                                 | 153 ms: 1.28x faster                                                   |
| sqlglot_optimize         | 69.2 ms                                                | 54.1 ms: 1.28x faster                                                  |
| genshi_xml               | 66.0 ms                                                | 52.0 ms: 1.27x faster                                                  |
| sympy_str                | 346 ms                                                 | 275 ms: 1.26x faster                                                   |
| dulwich_log              | 84.3 ms                                                | 68.3 ms: 1.24x faster                                                  |
| aiohttp                  | 1.44 ms                                                | 1.17 ms: 1.23x faster                                                  |
| sympy_expand             | 566 ms                                                 | 461 ms: 1.23x faster                                                   |
| mypy2                    | 894 ms                                                 | 733 ms: 1.22x faster                                                   |
| gunicorn                 | 1.53 ms                                                | 1.27 ms: 1.21x faster                                                  |
| dask                     | 441 ms                                                 | 366 ms: 1.21x faster                                                   |
| bench_thread_pool        | 986 us                                                 | 826 us: 1.19x faster                                                   |
| docutils                 | 3.30 sec                                               | 2.79 sec: 1.18x faster                                                 |
| xml_etree_generate       | 99.4 ms                                                | 86.3 ms: 1.15x faster                                                  |
| pathlib                  | 20.5 ms                                                | 18.5 ms: 1.11x faster                                                  |
| meteor_contest           | 120 ms                                                 | 109 ms: 1.10x faster                                                   |
| xml_etree_iterparse      | 115 ms                                                 | 106 ms: 1.09x faster                                                   |
| mdp                      | 2.85 sec                                               | 2.62 sec: 1.09x faster                                                 |
| regex_v8                 | 27.8 ms                                                | 25.5 ms: 1.09x faster                                                  |
| json_loads               | 31.2 us                                                | 28.8 us: 1.08x faster                                                  |
| xml_etree_parse          | 168 ms                                                 | 160 ms: 1.05x faster                                                   |
| sqlite_synth             | 3.02 us                                                | 2.92 us: 1.03x faster                                                  |
| json                     | 5.69 ms                                                | 5.53 ms: 1.03x faster                                                  |
| unpickle_list            | 5.20 us                                                | 5.07 us: 1.03x faster                                                  |
| regex_dna                | 227 ms                                                 | 224 ms: 1.01x faster                                                   |
| async_generators         | 444 ms                                                 | 438 ms: 1.01x faster                                                   |
| pidigits                 | 191 ms                                                 | 189 ms: 1.01x faster                                                   |
| bench_mp_pool            | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                  |
| asyncio_websockets       | 559 ms                                                 | 563 ms: 1.01x slower                                                   |
| regex_effbot             | 3.63 ms                                                | 3.73 ms: 1.03x slower                                                  |
| pickle_list              | 5.08 us                                                | 5.26 us: 1.04x slower                                                  |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                  |
| unpickle                 | 14.4 us                                                | 15.7 us: 1.09x slower                                                  |
| gc_traversal             | 3.62 ms                                                | 4.01 ms: 1.11x slower                                                  |
| pickle                   | 10.7 us                                                | 12.0 us: 1.13x slower                                                  |
| telco                    | 7.27 ms                                                | 8.39 ms: 1.16x slower                                                  |
| pickle_dict              | 29.6 us                                                | 35.2 us: 1.19x slower                                                  |
| coverage                 | 79.4 ms                                                | 96.4 ms: 1.21x slower                                                  |
| python_startup_no_site   | 5.93 ms                                                | 9.00 ms: 1.52x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.36x faster                                                           |
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240402-3.13.0a5+-ee60448/bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: 1.09x
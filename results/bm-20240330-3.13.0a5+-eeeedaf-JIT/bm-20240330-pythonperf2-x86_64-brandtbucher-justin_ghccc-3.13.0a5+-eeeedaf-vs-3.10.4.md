# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 300 ms: 1.17x faster                                                       |
| chameleon      | 9.44 ms                                                      | 7.36 ms: 1.28x faster                                                      |
| docutils       | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                     |
| html5lib       | 94.6 ms                                                      | 73.0 ms: 1.30x faster                                                      |
| tornado_http   | 157 ms                                                       | 123 ms: 1.27x faster                                                       |
| Geometric mean | (ref)                                                        | 1.22x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 358 ms: 1.93x faster                                                       |
| async_tree_memoization  | 819 ms                                                       | 441 ms: 1.86x faster                                                       |
| async_tree_io           | 1.60 sec                                                     | 885 ms: 1.81x faster                                                       |
| async_tree_cpu_io_mixed | 936 ms                                                       | 593 ms: 1.58x faster                                                       |
| Geometric mean          | (ref)                                                        | 1.79x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 75.4 ms: 1.47x faster                                                      |
| nbody          | 134 ms                                                       | 93.1 ms: 1.44x faster                                                      |
| pidigits       | 271 ms                                                       | 261 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                        | 1.30x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 146 ms: 1.30x faster                                                       |
| regex_dna      | 261 ms                                                       | 239 ms: 1.09x faster                                                       |
| regex_v8       | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                      |
| regex_effbot   | 3.09 ms                                                      | 3.54 ms: 1.15x slower                                                      |
| Geometric mean | (ref)                                                        | 1.07x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 312 us: 1.46x faster                                                       |
| tomli_loads          | 2.92 sec                                                     | 2.10 sec: 1.39x faster                                                     |
| unpickle_pure_python | 312 us                                                       | 229 us: 1.36x faster                                                       |
| json_dumps           | 14.5 ms                                                      | 10.8 ms: 1.35x faster                                                      |
| xml_etree_process    | 75.9 ms                                                      | 58.5 ms: 1.30x faster                                                      |
| json_loads           | 30.3 us                                                      | 25.5 us: 1.19x faster                                                      |
| xml_etree_parse      | 160 ms                                                       | 144 ms: 1.11x faster                                                       |
| xml_etree_generate   | 92.3 ms                                                      | 83.3 ms: 1.11x faster                                                      |
| xml_etree_iterparse  | 110 ms                                                       | 103 ms: 1.07x faster                                                       |
| pickle_list          | 4.12 us                                                      | 4.28 us: 1.04x slower                                                      |
| pickle_dict          | 29.5 us                                                      | 30.9 us: 1.05x slower                                                      |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                      |
| unpickle             | 13.5 us                                                      | 15.3 us: 1.14x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.13x faster                                                               |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                      |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 9.29 ms: 1.58x faster                                                      |
| django_template | 50.2 ms                                                      | 40.4 ms: 1.24x faster                                                      |
| genshi_text     | 31.4 ms                                                      | 26.0 ms: 1.21x faster                                                      |
| genshi_xml      | 63.3 ms                                                      | 57.2 ms: 1.11x faster                                                      |
| Geometric mean  | (ref)                                                        | 1.27x faster                                                               |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 120 us: 4.48x faster                                                       |
| asyncio_tcp              | 779 ms                                                       | 375 ms: 2.08x faster                                                       |
| deltablue                | 7.50 ms                                                      | 3.71 ms: 2.02x faster                                                      |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.96x faster                                                     |
| async_tree_none          | 692 ms                                                       | 358 ms: 1.93x faster                                                       |
| async_tree_memoization   | 819 ms                                                       | 441 ms: 1.86x faster                                                       |
| async_tree_io            | 1.60 sec                                                     | 885 ms: 1.81x faster                                                       |
| generators               | 57.3 ms                                                      | 33.1 ms: 1.73x faster                                                      |
| chaos                    | 109 ms                                                       | 62.8 ms: 1.73x faster                                                      |
| spectral_norm            | 139 ms                                                       | 81.9 ms: 1.70x faster                                                      |
| logging_silent           | 167 ns                                                       | 98.6 ns: 1.70x faster                                                      |
| pylint                   | 566 ms                                                       | 337 ms: 1.68x faster                                                       |
| crypto_pyaes             | 119 ms                                                       | 72.5 ms: 1.64x faster                                                      |
| pyflate                  | 733 ms                                                       | 454 ms: 1.62x faster                                                       |
| raytrace                 | 489 ms                                                       | 303 ms: 1.61x faster                                                       |
| scimark_monte_carlo      | 107 ms                                                       | 66.9 ms: 1.61x faster                                                      |
| richards_super           | 90.6 ms                                                      | 56.7 ms: 1.60x faster                                                      |
| sqlglot_parse            | 2.24 ms                                                      | 1.40 ms: 1.59x faster                                                      |
| mako                     | 14.7 ms                                                      | 9.29 ms: 1.58x faster                                                      |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 593 ms: 1.58x faster                                                       |
| go                       | 262 ms                                                       | 175 ms: 1.50x faster                                                       |
| richards                 | 75.1 ms                                                      | 50.5 ms: 1.49x faster                                                      |
| sqlglot_transpile        | 2.68 ms                                                      | 1.81 ms: 1.49x faster                                                      |
| float                    | 111 ms                                                       | 75.4 ms: 1.47x faster                                                      |
| pickle_pure_python       | 455 us                                                       | 312 us: 1.46x faster                                                       |
| scimark_lu               | 167 ms                                                       | 115 ms: 1.45x faster                                                       |
| nbody                    | 134 ms                                                       | 93.1 ms: 1.44x faster                                                      |
| comprehensions           | 26.7 us                                                      | 19.0 us: 1.41x faster                                                      |
| tomli_loads              | 2.92 sec                                                     | 2.10 sec: 1.39x faster                                                     |
| fannkuch                 | 483 ms                                                       | 349 ms: 1.38x faster                                                       |
| unpickle_pure_python     | 312 us                                                       | 229 us: 1.36x faster                                                       |
| json_dumps               | 14.5 ms                                                      | 10.8 ms: 1.35x faster                                                      |
| coroutines               | 30.3 ms                                                      | 22.6 ms: 1.34x faster                                                      |
| hexiom                   | 9.42 ms                                                      | 7.09 ms: 1.33x faster                                                      |
| pycparser                | 1.67 sec                                                     | 1.26 sec: 1.32x faster                                                     |
| logging_simple           | 8.88 us                                                      | 6.72 us: 1.32x faster                                                      |
| thrift                   | 1.18 ms                                                      | 897 us: 1.31x faster                                                       |
| logging_format           | 9.64 us                                                      | 7.38 us: 1.31x faster                                                      |
| pprint_pformat           | 2.15 sec                                                     | 1.65 sec: 1.31x faster                                                     |
| regex_compile            | 190 ms                                                       | 146 ms: 1.30x faster                                                       |
| xml_etree_process        | 75.9 ms                                                      | 58.5 ms: 1.30x faster                                                      |
| html5lib                 | 94.6 ms                                                      | 73.0 ms: 1.30x faster                                                      |
| pprint_safe_repr         | 1.05 sec                                                     | 811 ms: 1.29x faster                                                       |
| deepcopy_memo            | 49.8 us                                                      | 38.5 us: 1.29x faster                                                      |
| chameleon                | 9.44 ms                                                      | 7.36 ms: 1.28x faster                                                      |
| tornado_http             | 157 ms                                                       | 123 ms: 1.27x faster                                                       |
| bench_mp_pool            | 6.37 ms                                                      | 5.07 ms: 1.26x faster                                                      |
| scimark_fft              | 361 ms                                                       | 290 ms: 1.25x faster                                                       |
| django_template          | 50.2 ms                                                      | 40.4 ms: 1.24x faster                                                      |
| scimark_sor              | 180 ms                                                       | 148 ms: 1.21x faster                                                       |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.19 ms: 1.21x faster                                                      |
| genshi_text              | 31.4 ms                                                      | 26.0 ms: 1.21x faster                                                      |
| deepcopy                 | 468 us                                                       | 389 us: 1.20x faster                                                       |
| deepcopy_reduce          | 4.01 us                                                      | 3.34 us: 1.20x faster                                                      |
| sympy_sum                | 193 ms                                                       | 161 ms: 1.19x faster                                                       |
| sympy_str                | 360 ms                                                       | 303 ms: 1.19x faster                                                       |
| json_loads               | 30.3 us                                                      | 25.5 us: 1.19x faster                                                      |
| dulwich_log              | 81.1 ms                                                      | 68.9 ms: 1.18x faster                                                      |
| dask                     | 472 ms                                                       | 404 ms: 1.17x faster                                                       |
| sympy_expand             | 600 ms                                                       | 513 ms: 1.17x faster                                                       |
| 2to3                     | 350 ms                                                       | 300 ms: 1.17x faster                                                       |
| mdp                      | 3.01 sec                                                     | 2.60 sec: 1.16x faster                                                     |
| sqlglot_normalize        | 144 ms                                                       | 125 ms: 1.15x faster                                                       |
| nqueens                  | 115 ms                                                       | 102 ms: 1.12x faster                                                       |
| mypy2                    | 933 ms                                                       | 832 ms: 1.12x faster                                                       |
| sympy_integrate          | 28.2 ms                                                      | 25.2 ms: 1.12x faster                                                      |
| sqlite_synth             | 2.99 us                                                      | 2.68 us: 1.12x faster                                                      |
| docutils                 | 3.41 sec                                                     | 3.07 sec: 1.11x faster                                                     |
| xml_etree_parse          | 160 ms                                                       | 144 ms: 1.11x faster                                                       |
| xml_etree_generate       | 92.3 ms                                                      | 83.3 ms: 1.11x faster                                                      |
| genshi_xml               | 63.3 ms                                                      | 57.2 ms: 1.11x faster                                                      |
| sqlglot_optimize         | 70.1 ms                                                      | 63.6 ms: 1.10x faster                                                      |
| regex_dna                | 261 ms                                                       | 239 ms: 1.09x faster                                                       |
| pathlib                  | 21.4 ms                                                      | 19.7 ms: 1.09x faster                                                      |
| xml_etree_iterparse      | 110 ms                                                       | 103 ms: 1.07x faster                                                       |
| json                     | 5.86 ms                                                      | 5.48 ms: 1.07x faster                                                      |
| regex_v8                 | 27.2 ms                                                      | 25.4 ms: 1.07x faster                                                      |
| async_generators         | 421 ms                                                       | 395 ms: 1.06x faster                                                       |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.06x faster                                                      |
| aiohttp                  | 1.19 ms                                                      | 1.12 ms: 1.06x faster                                                      |
| meteor_contest           | 138 ms                                                       | 133 ms: 1.04x faster                                                       |
| pidigits                 | 271 ms                                                       | 261 ms: 1.04x faster                                                       |
| bench_thread_pool        | 1.14 ms                                                      | 1.11 ms: 1.02x faster                                                      |
| create_gc_cycles         | 1.76 ms                                                      | 1.82 ms: 1.03x slower                                                      |
| pickle_list              | 4.12 us                                                      | 4.28 us: 1.04x slower                                                      |
| pickle_dict              | 29.5 us                                                      | 30.9 us: 1.05x slower                                                      |
| pickle                   | 9.89 us                                                      | 10.6 us: 1.07x slower                                                      |
| telco                    | 7.23 ms                                                      | 8.04 ms: 1.11x slower                                                      |
| unpickle                 | 13.5 us                                                      | 15.3 us: 1.14x slower                                                      |
| regex_effbot             | 3.09 ms                                                      | 3.54 ms: 1.15x slower                                                      |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.17x slower                                                      |
| coverage                 | 63.3 ms                                                      | 79.7 ms: 1.26x slower                                                      |
| gc_traversal             | 3.42 ms                                                      | 4.81 ms: 1.41x slower                                                      |
| unpack_sequence          | 59.9 ns                                                      | 89.5 ns: 1.49x slower                                                      |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                      |
| Geometric mean           | (ref)                                                        | 1.26x faster                                                               |

Benchmark hidden because not significant (2): unpickle_list, asyncio_websockets
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-pythonperf2-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: 1.19x
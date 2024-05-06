# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.23x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 303 ms: 1.15x faster                                                       |
| chameleon      | 9.44 ms                                                      | 7.52 ms: 1.26x faster                                                      |
| docutils       | 3.41 sec                                                     | 3.11 sec: 1.10x faster                                                     |
| html5lib       | 94.6 ms                                                      | 74.2 ms: 1.27x faster                                                      |
| tornado_http   | 157 ms                                                       | 124 ms: 1.27x faster                                                       |
| Geometric mean | (ref)                                                        | 1.21x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 362 ms: 1.91x faster                                                       |
| async_tree_memoization  | 819 ms                                                       | 446 ms: 1.84x faster                                                       |
| async_tree_io           | 1.60 sec                                                     | 891 ms: 1.79x faster                                                       |
| async_tree_cpu_io_mixed | 936 ms                                                       | 600 ms: 1.56x faster                                                       |
| Geometric mean          | (ref)                                                        | 1.77x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 78.6 ms: 1.41x faster                                                      |
| nbody          | 134 ms                                                       | 103 ms: 1.30x faster                                                       |
| pidigits       | 271 ms                                                       | 262 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                        | 1.24x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 190 ms                                                       | 151 ms: 1.26x faster                                                       |
| regex_dna      | 261 ms                                                       | 245 ms: 1.07x faster                                                       |
| regex_v8       | 27.2 ms                                                      | 25.8 ms: 1.05x faster                                                      |
| regex_effbot   | 3.09 ms                                                      | 3.69 ms: 1.19x slower                                                      |
| Geometric mean | (ref)                                                        | 1.04x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 313 us: 1.46x faster                                                       |
| json_dumps           | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                      |
| xml_etree_process    | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                      |
| unpickle_pure_python | 312 us                                                       | 244 us: 1.28x faster                                                       |
| tomli_loads          | 2.92 sec                                                     | 2.36 sec: 1.23x faster                                                     |
| json_loads           | 30.3 us                                                      | 25.6 us: 1.19x faster                                                      |
| xml_etree_parse      | 160 ms                                                       | 144 ms: 1.11x faster                                                       |
| xml_etree_generate   | 92.3 ms                                                      | 86.0 ms: 1.07x faster                                                      |
| xml_etree_iterparse  | 110 ms                                                       | 105 ms: 1.05x faster                                                       |
| unpickle_list        | 4.65 us                                                      | 4.56 us: 1.02x faster                                                      |
| pickle_dict          | 29.5 us                                                      | 30.7 us: 1.04x slower                                                      |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                                      |
| pickle_list          | 4.12 us                                                      | 4.49 us: 1.09x slower                                                      |
| unpickle             | 13.5 us                                                      | 14.8 us: 1.09x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.12x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 13.5 ms: 1.18x slower                                                      |
| python_startup_no_site | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 14.7 ms                                                      | 10.2 ms: 1.44x faster                                                      |
| django_template | 50.2 ms                                                      | 39.7 ms: 1.26x faster                                                      |
| genshi_text     | 31.4 ms                                                      | 26.6 ms: 1.18x faster                                                      |
| genshi_xml      | 63.3 ms                                                      | 58.6 ms: 1.08x faster                                                      |
| Geometric mean  | (ref)                                                        | 1.23x faster                                                               |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 119 us: 4.50x faster                                                       |
| asyncio_tcp              | 779 ms                                                       | 372 ms: 2.09x faster                                                       |
| deltablue                | 7.50 ms                                                      | 3.80 ms: 1.98x faster                                                      |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.58 sec: 1.97x faster                                                     |
| async_tree_none          | 692 ms                                                       | 362 ms: 1.91x faster                                                       |
| async_tree_memoization   | 819 ms                                                       | 446 ms: 1.84x faster                                                       |
| async_tree_io            | 1.60 sec                                                     | 891 ms: 1.79x faster                                                       |
| generators               | 57.3 ms                                                      | 33.1 ms: 1.73x faster                                                      |
| logging_silent           | 167 ns                                                       | 99.0 ns: 1.69x faster                                                      |
| pylint                   | 566 ms                                                       | 340 ms: 1.67x faster                                                       |
| raytrace                 | 489 ms                                                       | 306 ms: 1.60x faster                                                       |
| sqlglot_parse            | 2.24 ms                                                      | 1.42 ms: 1.57x faster                                                      |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 600 ms: 1.56x faster                                                       |
| chaos                    | 109 ms                                                       | 69.8 ms: 1.56x faster                                                      |
| richards_super           | 90.6 ms                                                      | 60.2 ms: 1.50x faster                                                      |
| crypto_pyaes             | 119 ms                                                       | 81.1 ms: 1.47x faster                                                      |
| sqlglot_transpile        | 2.68 ms                                                      | 1.83 ms: 1.47x faster                                                      |
| pickle_pure_python       | 455 us                                                       | 313 us: 1.46x faster                                                       |
| go                       | 262 ms                                                       | 182 ms: 1.44x faster                                                       |
| mako                     | 14.7 ms                                                      | 10.2 ms: 1.44x faster                                                      |
| float                    | 111 ms                                                       | 78.6 ms: 1.41x faster                                                      |
| spectral_norm            | 139 ms                                                       | 99.0 ms: 1.41x faster                                                      |
| pyflate                  | 733 ms                                                       | 522 ms: 1.40x faster                                                       |
| richards                 | 75.1 ms                                                      | 53.7 ms: 1.40x faster                                                      |
| scimark_monte_carlo      | 107 ms                                                       | 77.9 ms: 1.38x faster                                                      |
| thrift                   | 1.18 ms                                                      | 861 us: 1.37x faster                                                       |
| json_dumps               | 14.5 ms                                                      | 10.7 ms: 1.36x faster                                                      |
| coroutines               | 30.3 ms                                                      | 22.5 ms: 1.35x faster                                                      |
| pycparser                | 1.67 sec                                                     | 1.26 sec: 1.33x faster                                                     |
| logging_simple           | 8.88 us                                                      | 6.73 us: 1.32x faster                                                      |
| comprehensions           | 26.7 us                                                      | 20.4 us: 1.31x faster                                                      |
| logging_format           | 9.64 us                                                      | 7.38 us: 1.31x faster                                                      |
| nbody                    | 134 ms                                                       | 103 ms: 1.30x faster                                                       |
| deepcopy_memo            | 49.8 us                                                      | 38.5 us: 1.29x faster                                                      |
| xml_etree_process        | 75.9 ms                                                      | 58.9 ms: 1.29x faster                                                      |
| scimark_lu               | 167 ms                                                       | 130 ms: 1.29x faster                                                       |
| bench_mp_pool            | 6.37 ms                                                      | 4.96 ms: 1.29x faster                                                      |
| unpickle_pure_python     | 312 us                                                       | 244 us: 1.28x faster                                                       |
| html5lib                 | 94.6 ms                                                      | 74.2 ms: 1.27x faster                                                      |
| tornado_http             | 157 ms                                                       | 124 ms: 1.27x faster                                                       |
| django_template          | 50.2 ms                                                      | 39.7 ms: 1.26x faster                                                      |
| regex_compile            | 190 ms                                                       | 151 ms: 1.26x faster                                                       |
| chameleon                | 9.44 ms                                                      | 7.52 ms: 1.26x faster                                                      |
| tomli_loads              | 2.92 sec                                                     | 2.36 sec: 1.23x faster                                                     |
| pprint_pformat           | 2.15 sec                                                     | 1.79 sec: 1.20x faster                                                     |
| sympy_str                | 360 ms                                                       | 302 ms: 1.19x faster                                                       |
| sqlglot_normalize        | 144 ms                                                       | 121 ms: 1.19x faster                                                       |
| sympy_sum                | 193 ms                                                       | 162 ms: 1.19x faster                                                       |
| deepcopy_reduce          | 4.01 us                                                      | 3.37 us: 1.19x faster                                                      |
| sympy_expand             | 600 ms                                                       | 505 ms: 1.19x faster                                                       |
| json_loads               | 30.3 us                                                      | 25.6 us: 1.19x faster                                                      |
| deepcopy                 | 468 us                                                       | 395 us: 1.19x faster                                                       |
| genshi_text              | 31.4 ms                                                      | 26.6 ms: 1.18x faster                                                      |
| fannkuch                 | 483 ms                                                       | 408 ms: 1.18x faster                                                       |
| hexiom                   | 9.42 ms                                                      | 8.00 ms: 1.18x faster                                                      |
| dulwich_log              | 81.1 ms                                                      | 69.4 ms: 1.17x faster                                                      |
| dask                     | 472 ms                                                       | 406 ms: 1.16x faster                                                       |
| pprint_safe_repr         | 1.05 sec                                                     | 902 ms: 1.16x faster                                                       |
| 2to3                     | 350 ms                                                       | 303 ms: 1.15x faster                                                       |
| mdp                      | 3.01 sec                                                     | 2.65 sec: 1.13x faster                                                     |
| scimark_sor              | 180 ms                                                       | 160 ms: 1.13x faster                                                       |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 4.50 ms: 1.13x faster                                                      |
| mypy2                    | 933 ms                                                       | 831 ms: 1.12x faster                                                       |
| sqlglot_optimize         | 70.1 ms                                                      | 62.9 ms: 1.11x faster                                                      |
| sympy_integrate          | 28.2 ms                                                      | 25.4 ms: 1.11x faster                                                      |
| pathlib                  | 21.4 ms                                                      | 19.2 ms: 1.11x faster                                                      |
| xml_etree_parse          | 160 ms                                                       | 144 ms: 1.11x faster                                                       |
| docutils                 | 3.41 sec                                                     | 3.11 sec: 1.10x faster                                                     |
| sqlite_synth             | 2.99 us                                                      | 2.74 us: 1.09x faster                                                      |
| json                     | 5.86 ms                                                      | 5.40 ms: 1.09x faster                                                      |
| async_generators         | 421 ms                                                       | 389 ms: 1.08x faster                                                       |
| genshi_xml               | 63.3 ms                                                      | 58.6 ms: 1.08x faster                                                      |
| xml_etree_generate       | 92.3 ms                                                      | 86.0 ms: 1.07x faster                                                      |
| regex_dna                | 261 ms                                                       | 245 ms: 1.07x faster                                                       |
| scimark_fft              | 361 ms                                                       | 341 ms: 1.06x faster                                                       |
| gunicorn                 | 1.16 ms                                                      | 1.09 ms: 1.06x faster                                                      |
| nqueens                  | 115 ms                                                       | 109 ms: 1.06x faster                                                       |
| aiohttp                  | 1.19 ms                                                      | 1.13 ms: 1.06x faster                                                      |
| regex_v8                 | 27.2 ms                                                      | 25.8 ms: 1.05x faster                                                      |
| xml_etree_iterparse      | 110 ms                                                       | 105 ms: 1.05x faster                                                       |
| pidigits                 | 271 ms                                                       | 262 ms: 1.03x faster                                                       |
| meteor_contest           | 138 ms                                                       | 134 ms: 1.03x faster                                                       |
| unpickle_list            | 4.65 us                                                      | 4.56 us: 1.02x faster                                                      |
| bench_thread_pool        | 1.14 ms                                                      | 1.12 ms: 1.02x faster                                                      |
| create_gc_cycles         | 1.76 ms                                                      | 1.80 ms: 1.02x slower                                                      |
| pickle_dict              | 29.5 us                                                      | 30.7 us: 1.04x slower                                                      |
| pickle                   | 9.89 us                                                      | 10.4 us: 1.05x slower                                                      |
| pickle_list              | 4.12 us                                                      | 4.49 us: 1.09x slower                                                      |
| unpickle                 | 13.5 us                                                      | 14.8 us: 1.09x slower                                                      |
| telco                    | 7.23 ms                                                      | 8.10 ms: 1.12x slower                                                      |
| python_startup           | 11.5 ms                                                      | 13.5 ms: 1.18x slower                                                      |
| regex_effbot             | 3.09 ms                                                      | 3.69 ms: 1.19x slower                                                      |
| coverage                 | 63.3 ms                                                      | 80.3 ms: 1.27x slower                                                      |
| gc_traversal             | 3.42 ms                                                      | 4.36 ms: 1.28x slower                                                      |
| python_startup_no_site   | 7.33 ms                                                      | 11.8 ms: 1.61x slower                                                      |
| unpack_sequence          | 59.9 ns                                                      | 107 ns: 1.78x slower                                                       |
| Geometric mean           | (ref)                                                        | 1.23x faster                                                               |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.20x
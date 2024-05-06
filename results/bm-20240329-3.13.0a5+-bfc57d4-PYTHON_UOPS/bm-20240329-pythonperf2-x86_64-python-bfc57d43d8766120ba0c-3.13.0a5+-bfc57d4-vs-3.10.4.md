# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.13x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 350 ms                                                       | 325 ms: 1.08x faster                                                         |
| chameleon      | 9.44 ms                                                      | 8.14 ms: 1.16x faster                                                        |
| docutils       | 3.41 sec                                                     | 3.28 sec: 1.04x faster                                                       |
| html5lib       | 94.6 ms                                                      | 80.4 ms: 1.18x faster                                                        |
| tornado_http   | 157 ms                                                       | 129 ms: 1.22x faster                                                         |
| Geometric mean | (ref)                                                        | 1.13x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 692 ms                                                       | 383 ms: 1.81x faster                                                         |
| async_tree_memoization  | 819 ms                                                       | 470 ms: 1.75x faster                                                         |
| async_tree_io           | 1.60 sec                                                     | 923 ms: 1.73x faster                                                         |
| async_tree_cpu_io_mixed | 936 ms                                                       | 629 ms: 1.49x faster                                                         |
| Geometric mean          | (ref)                                                        | 1.69x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 111 ms                                                       | 102 ms: 1.09x faster                                                         |
| nbody          | 134 ms                                                       | 129 ms: 1.04x faster                                                         |
| pidigits       | 271 ms                                                       | 265 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 261 ms                                                       | 242 ms: 1.08x faster                                                         |
| regex_v8       | 27.2 ms                                                      | 25.9 ms: 1.05x faster                                                        |
| regex_compile  | 190 ms                                                       | 209 ms: 1.10x slower                                                         |
| regex_effbot   | 3.09 ms                                                      | 3.47 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 455 us                                                       | 328 us: 1.39x faster                                                         |
| json_dumps           | 14.5 ms                                                      | 10.9 ms: 1.34x faster                                                        |
| xml_etree_process    | 75.9 ms                                                      | 63.4 ms: 1.20x faster                                                        |
| json_loads           | 30.3 us                                                      | 25.8 us: 1.18x faster                                                        |
| xml_etree_parse      | 160 ms                                                       | 146 ms: 1.09x faster                                                         |
| unpickle_list        | 4.65 us                                                      | 4.59 us: 1.01x faster                                                        |
| tomli_loads          | 2.92 sec                                                     | 2.98 sec: 1.02x slower                                                       |
| unpickle_pure_python | 312 us                                                       | 319 us: 1.02x slower                                                         |
| xml_etree_iterparse  | 110 ms                                                       | 113 ms: 1.03x slower                                                         |
| pickle_list          | 4.12 us                                                      | 4.46 us: 1.08x slower                                                        |
| unpickle             | 13.5 us                                                      | 14.8 us: 1.10x slower                                                        |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| pickle_dict          | 29.5 us                                                      | 35.2 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.04x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| python_startup_no_site | 7.33 ms                                                      | 11.2 ms: 1.52x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.31x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 50.2 ms                                                      | 42.3 ms: 1.19x faster                                                        |
| genshi_text     | 31.4 ms                                                      | 27.0 ms: 1.16x faster                                                        |
| genshi_xml      | 63.3 ms                                                      | 61.9 ms: 1.02x faster                                                        |
| mako            | 14.7 ms                                                      | 14.4 ms: 1.02x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.10x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 537 us                                                       | 128 us: 4.19x faster                                                         |
| asyncio_tcp              | 779 ms                                                       | 379 ms: 2.05x faster                                                         |
| asyncio_tcp_ssl          | 3.10 sec                                                     | 1.60 sec: 1.94x faster                                                       |
| async_tree_none          | 692 ms                                                       | 383 ms: 1.81x faster                                                         |
| deltablue                | 7.50 ms                                                      | 4.15 ms: 1.81x faster                                                        |
| async_tree_memoization   | 819 ms                                                       | 470 ms: 1.75x faster                                                         |
| async_tree_io            | 1.60 sec                                                     | 923 ms: 1.73x faster                                                         |
| generators               | 57.3 ms                                                      | 34.9 ms: 1.64x faster                                                        |
| pylint                   | 566 ms                                                       | 351 ms: 1.61x faster                                                         |
| logging_silent           | 167 ns                                                       | 104 ns: 1.61x faster                                                         |
| async_tree_cpu_io_mixed  | 936 ms                                                       | 629 ms: 1.49x faster                                                         |
| chaos                    | 109 ms                                                       | 77.7 ms: 1.40x faster                                                        |
| raytrace                 | 489 ms                                                       | 352 ms: 1.39x faster                                                         |
| pickle_pure_python       | 455 us                                                       | 328 us: 1.39x faster                                                         |
| sqlglot_parse            | 2.24 ms                                                      | 1.61 ms: 1.39x faster                                                        |
| coroutines               | 30.3 ms                                                      | 22.5 ms: 1.35x faster                                                        |
| json_dumps               | 14.5 ms                                                      | 10.9 ms: 1.34x faster                                                        |
| richards_super           | 90.6 ms                                                      | 68.0 ms: 1.33x faster                                                        |
| sqlglot_transpile        | 2.68 ms                                                      | 2.04 ms: 1.32x faster                                                        |
| thrift                   | 1.18 ms                                                      | 900 us: 1.31x faster                                                         |
| crypto_pyaes             | 119 ms                                                       | 92.5 ms: 1.29x faster                                                        |
| go                       | 262 ms                                                       | 204 ms: 1.28x faster                                                         |
| logging_simple           | 8.88 us                                                      | 6.93 us: 1.28x faster                                                        |
| logging_format           | 9.64 us                                                      | 7.60 us: 1.27x faster                                                        |
| richards                 | 75.1 ms                                                      | 61.1 ms: 1.23x faster                                                        |
| bench_mp_pool            | 6.37 ms                                                      | 5.22 ms: 1.22x faster                                                        |
| tornado_http             | 157 ms                                                       | 129 ms: 1.22x faster                                                         |
| xml_etree_process        | 75.9 ms                                                      | 63.4 ms: 1.20x faster                                                        |
| django_template          | 50.2 ms                                                      | 42.3 ms: 1.19x faster                                                        |
| html5lib                 | 94.6 ms                                                      | 80.4 ms: 1.18x faster                                                        |
| json_loads               | 30.3 us                                                      | 25.8 us: 1.18x faster                                                        |
| genshi_text              | 31.4 ms                                                      | 27.0 ms: 1.16x faster                                                        |
| chameleon                | 9.44 ms                                                      | 8.14 ms: 1.16x faster                                                        |
| deepcopy                 | 468 us                                                       | 405 us: 1.16x faster                                                         |
| pycparser                | 1.67 sec                                                     | 1.47 sec: 1.14x faster                                                       |
| deepcopy_reduce          | 4.01 us                                                      | 3.53 us: 1.14x faster                                                        |
| dask                     | 472 ms                                                       | 418 ms: 1.13x faster                                                         |
| mdp                      | 3.01 sec                                                     | 2.71 sec: 1.11x faster                                                       |
| pyflate                  | 733 ms                                                       | 666 ms: 1.10x faster                                                         |
| scimark_lu               | 167 ms                                                       | 152 ms: 1.10x faster                                                         |
| sqlglot_normalize        | 144 ms                                                       | 131 ms: 1.10x faster                                                         |
| deepcopy_memo            | 49.8 us                                                      | 45.4 us: 1.10x faster                                                        |
| xml_etree_parse          | 160 ms                                                       | 146 ms: 1.09x faster                                                         |
| float                    | 111 ms                                                       | 102 ms: 1.09x faster                                                         |
| scimark_sor              | 180 ms                                                       | 167 ms: 1.08x faster                                                         |
| regex_dna                | 261 ms                                                       | 242 ms: 1.08x faster                                                         |
| mypy2                    | 933 ms                                                       | 865 ms: 1.08x faster                                                         |
| 2to3                     | 350 ms                                                       | 325 ms: 1.08x faster                                                         |
| sympy_sum                | 193 ms                                                       | 181 ms: 1.06x faster                                                         |
| async_generators         | 421 ms                                                       | 400 ms: 1.05x faster                                                         |
| scimark_monte_carlo      | 107 ms                                                       | 102 ms: 1.05x faster                                                         |
| dulwich_log              | 81.1 ms                                                      | 77.3 ms: 1.05x faster                                                        |
| regex_v8                 | 27.2 ms                                                      | 25.9 ms: 1.05x faster                                                        |
| json                     | 5.86 ms                                                      | 5.60 ms: 1.05x faster                                                        |
| gunicorn                 | 1.16 ms                                                      | 1.11 ms: 1.05x faster                                                        |
| pprint_pformat           | 2.15 sec                                                     | 2.06 sec: 1.04x faster                                                       |
| sympy_integrate          | 28.2 ms                                                      | 27.0 ms: 1.04x faster                                                        |
| docutils                 | 3.41 sec                                                     | 3.28 sec: 1.04x faster                                                       |
| nbody                    | 134 ms                                                       | 129 ms: 1.04x faster                                                         |
| pprint_safe_repr         | 1.05 sec                                                     | 1.01 sec: 1.04x faster                                                       |
| aiohttp                  | 1.19 ms                                                      | 1.15 ms: 1.04x faster                                                        |
| sympy_str                | 360 ms                                                       | 350 ms: 1.03x faster                                                         |
| sqlite_synth             | 2.99 us                                                      | 2.91 us: 1.03x faster                                                        |
| sqlglot_optimize         | 70.1 ms                                                      | 68.5 ms: 1.02x faster                                                        |
| genshi_xml               | 63.3 ms                                                      | 61.9 ms: 1.02x faster                                                        |
| pidigits                 | 271 ms                                                       | 265 ms: 1.02x faster                                                         |
| sympy_expand             | 600 ms                                                       | 587 ms: 1.02x faster                                                         |
| pathlib                  | 21.4 ms                                                      | 21.0 ms: 1.02x faster                                                        |
| mako                     | 14.7 ms                                                      | 14.4 ms: 1.02x faster                                                        |
| unpickle_list            | 4.65 us                                                      | 4.59 us: 1.01x faster                                                        |
| comprehensions           | 26.7 us                                                      | 26.8 us: 1.00x slower                                                        |
| tomli_loads              | 2.92 sec                                                     | 2.98 sec: 1.02x slower                                                       |
| unpickle_pure_python     | 312 us                                                       | 319 us: 1.02x slower                                                         |
| xml_etree_iterparse      | 110 ms                                                       | 113 ms: 1.03x slower                                                         |
| meteor_contest           | 138 ms                                                       | 143 ms: 1.03x slower                                                         |
| create_gc_cycles         | 1.76 ms                                                      | 1.84 ms: 1.04x slower                                                        |
| fannkuch                 | 483 ms                                                       | 507 ms: 1.05x slower                                                         |
| nqueens                  | 115 ms                                                       | 122 ms: 1.06x slower                                                         |
| unpack_sequence          | 59.9 ns                                                      | 64.4 ns: 1.07x slower                                                        |
| pickle_list              | 4.12 us                                                      | 4.46 us: 1.08x slower                                                        |
| unpickle                 | 13.5 us                                                      | 14.8 us: 1.10x slower                                                        |
| regex_compile            | 190 ms                                                       | 209 ms: 1.10x slower                                                         |
| pickle                   | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| python_startup           | 11.5 ms                                                      | 12.9 ms: 1.12x slower                                                        |
| regex_effbot             | 3.09 ms                                                      | 3.47 ms: 1.12x slower                                                        |
| spectral_norm            | 139 ms                                                       | 158 ms: 1.13x slower                                                         |
| hexiom                   | 9.42 ms                                                      | 11.0 ms: 1.16x slower                                                        |
| telco                    | 7.23 ms                                                      | 8.54 ms: 1.18x slower                                                        |
| pickle_dict              | 29.5 us                                                      | 35.2 us: 1.19x slower                                                        |
| scimark_fft              | 361 ms                                                       | 446 ms: 1.23x slower                                                         |
| gc_traversal             | 3.42 ms                                                      | 4.39 ms: 1.29x slower                                                        |
| coverage                 | 63.3 ms                                                      | 83.9 ms: 1.33x slower                                                        |
| scimark_sparse_mat_mult  | 5.08 ms                                                      | 6.79 ms: 1.34x slower                                                        |
| python_startup_no_site   | 7.33 ms                                                      | 11.2 ms: 1.52x slower                                                        |
| Geometric mean           | (ref)                                                        | 1.13x faster                                                                 |

Benchmark hidden because not significant (3): bench_thread_pool, asyncio_websockets, xml_etree_generate
Ignored benchmarks (3) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf2-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-bfc57d4-PYTHON_UOPS/bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.10x

# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_continue
- machine: windows-amd64
- commit hash: 9e86002
- commit date: 2024-02-13
- overall geometric mean: 1.24x faster \*
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240213-pythonperf1-amd64-brandtbucher-justin_continue-3.13.0a3+-9e86002 |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 214 ms: 1.15x faster                                                         |
| chameleon      | 5.79 ms                                                     | 4.80 ms: 1.20x faster                                                        |
| docutils       | 1.92 sec                                                    | 1.56 sec: 1.23x faster                                                       |
| tornado_http   | 108 ms                                                      | 84.9 ms: 1.28x faster                                                        |
| Geometric mean | (ref)                                                       | 1.21x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240213-pythonperf1-amd64-brandtbucher-justin_continue-3.13.0a3+-9e86002 |
|-------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 261 ms: 1.67x faster                                                         |
| async_tree_memoization  | 526 ms                                                      | 334 ms: 1.57x faster                                                         |
| async_tree_io           | 1.11 sec                                                    | 720 ms: 1.54x faster                                                         |
| async_tree_cpu_io_mixed | 638 ms                                                      | 445 ms: 1.43x faster                                                         |
| Geometric mean          | (ref)                                                       | 1.55x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240213-pythonperf1-amd64-brandtbucher-justin_continue-3.13.0a3+-9e86002 |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 50.2 ms: 1.23x faster                                                        |
| nbody          | 71.3 ms                                                     | 59.5 ms: 1.20x faster                                                        |
| pidigits       | 149 ms                                                      | 151 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240213-pythonperf1-amd64-brandtbucher-justin_continue-3.13.0a3+-9e86002 |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 78.1 ms: 1.36x faster                                                        |
| regex_dna      | 136 ms                                                      | 120 ms: 1.13x faster                                                         |
| regex_v8       | 15.4 ms                                                     | 14.8 ms: 1.04x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.60 ms: 1.04x faster                                                        |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240213-pythonperf1-amd64-brandtbucher-justin_continue-3.13.0a3+-9e86002 |
|----------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.61 ms: 1.63x faster                                                        |
| pickle_pure_python   | 270 us                                                      | 174 us: 1.55x faster                                                         |
| unpickle_pure_python | 183 us                                                      | 126 us: 1.45x faster                                                         |
| tomli_loads          | 1.67 sec                                                    | 1.26 sec: 1.33x faster                                                       |
| xml_etree_process    | 44.5 ms                                                     | 36.0 ms: 1.24x faster                                                        |
| unpickle             | 9.09 us                                                     | 8.58 us: 1.06x faster                                                        |
| xml_etree_generate   | 55.5 ms                                                     | 52.7 ms: 1.05x faster                                                        |
| xml_etree_parse      | 96.8 ms                                                     | 94.4 ms: 1.03x faster                                                        |
| xml_etree_iterparse  | 65.0 ms                                                     | 63.4 ms: 1.02x faster                                                        |
| json_loads           | 14.0 us                                                     | 13.8 us: 1.02x faster                                                        |
| pickle_dict          | 17.2 us                                                     | 17.5 us: 1.02x slower                                                        |
| unpickle_list        | 2.71 us                                                     | 2.79 us: 1.03x slower                                                        |
| pickle               | 6.85 us                                                     | 7.43 us: 1.08x slower                                                        |
| pickle_list          | 2.75 us                                                     | 3.09 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                       | 1.13x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240213-pythonperf1-amd64-brandtbucher-justin_continue-3.13.0a3+-9e86002 |
|------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 20.2 ms: 1.02x faster                                                        |
| python_startup_no_site | 15.5 ms                                                     | 18.1 ms: 1.17x slower                                                        |
| Geometric mean         | (ref)                                                       | 1.07x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240213-pythonperf1-amd64-brandtbucher-justin_continue-3.13.0a3+-9e86002 |
|-----------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako      | 9.03 ms                                                     | 6.15 ms: 1.47x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240213-pythonperf1-amd64-brandtbucher-justin_continue-3.13.0a3+-9e86002 |
|--------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 68.8 us: 4.88x faster                                                        |
| deltablue                | 4.19 ms                                                     | 1.96 ms: 2.13x faster                                                        |
| richards_super           | 52.2 ms                                                     | 28.2 ms: 1.85x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 53.0 ns: 1.78x faster                                                        |
| richards                 | 42.4 ms                                                     | 25.0 ms: 1.70x faster                                                        |
| async_tree_none          | 435 ms                                                      | 261 ms: 1.67x faster                                                         |
| json_dumps               | 9.16 ms                                                     | 5.61 ms: 1.63x faster                                                        |
| raytrace                 | 273 ms                                                      | 167 ms: 1.63x faster                                                         |
| generators               | 32.4 ms                                                     | 19.9 ms: 1.63x faster                                                        |
| sqlglot_parse            | 1.22 ms                                                     | 755 us: 1.61x faster                                                         |
| scimark_lu               | 85.8 ms                                                     | 53.4 ms: 1.61x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 334 ms: 1.57x faster                                                         |
| asyncio_tcp              | 732 ms                                                      | 468 ms: 1.57x faster                                                         |
| pickle_pure_python       | 270 us                                                      | 174 us: 1.55x faster                                                         |
| async_tree_io            | 1.11 sec                                                    | 720 ms: 1.54x faster                                                         |
| sqlglot_transpile        | 1.48 ms                                                     | 965 us: 1.53x faster                                                         |
| chaos                    | 61.7 ms                                                     | 41.6 ms: 1.48x faster                                                        |
| comprehensions           | 16.5 us                                                     | 11.1 us: 1.48x faster                                                        |
| go                       | 139 ms                                                      | 94.3 ms: 1.47x faster                                                        |
| mako                     | 9.03 ms                                                     | 6.15 ms: 1.47x faster                                                        |
| unpickle_pure_python     | 183 us                                                      | 126 us: 1.45x faster                                                         |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 445 ms: 1.43x faster                                                         |
| scimark_sor              | 106 ms                                                      | 74.6 ms: 1.42x faster                                                        |
| pyflate                  | 409 ms                                                      | 291 ms: 1.40x faster                                                         |
| crypto_pyaes             | 62.5 ms                                                     | 44.9 ms: 1.39x faster                                                        |
| pycparser                | 930 ms                                                      | 671 ms: 1.39x faster                                                         |
| regex_compile            | 106 ms                                                      | 78.1 ms: 1.36x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 21.2 us: 1.36x faster                                                        |
| tomli_loads              | 1.67 sec                                                    | 1.26 sec: 1.33x faster                                                       |
| mypy2                    | 555 ms                                                      | 421 ms: 1.32x faster                                                         |
| spectral_norm            | 77.3 ms                                                     | 59.9 ms: 1.29x faster                                                        |
| tornado_http             | 108 ms                                                      | 84.9 ms: 1.28x faster                                                        |
| pprint_pformat           | 1.22 sec                                                    | 967 ms: 1.26x faster                                                         |
| sqlite_synth             | 1.91 us                                                     | 1.52 us: 1.26x faster                                                        |
| pprint_safe_repr         | 592 ms                                                      | 473 ms: 1.25x faster                                                         |
| dulwich_log              | 50.5 ms                                                     | 40.5 ms: 1.25x faster                                                        |
| sympy_sum                | 107 ms                                                      | 86.4 ms: 1.24x faster                                                        |
| xml_etree_process        | 44.5 ms                                                     | 36.0 ms: 1.24x faster                                                        |
| float                    | 61.7 ms                                                     | 50.2 ms: 1.23x faster                                                        |
| coroutines               | 16.0 ms                                                     | 13.0 ms: 1.23x faster                                                        |
| dask                     | 313 ms                                                      | 255 ms: 1.23x faster                                                         |
| docutils                 | 1.92 sec                                                    | 1.56 sec: 1.23x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.72 sec: 1.23x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.80 ms: 1.20x faster                                                        |
| nbody                    | 71.3 ms                                                     | 59.5 ms: 1.20x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 33.3 ms: 1.19x faster                                                        |
| sympy_str                | 194 ms                                                      | 163 ms: 1.19x faster                                                         |
| sqlglot_normalize        | 205 ms                                                      | 172 ms: 1.19x faster                                                         |
| hexiom                   | 5.74 ms                                                     | 4.82 ms: 1.19x faster                                                        |
| bench_thread_pool        | 958 us                                                      | 808 us: 1.19x faster                                                         |
| deepcopy                 | 255 us                                                      | 216 us: 1.19x faster                                                         |
| sympy_integrate          | 15.3 ms                                                     | 12.9 ms: 1.18x faster                                                        |
| scimark_monte_carlo      | 57.3 ms                                                     | 49.2 ms: 1.16x faster                                                        |
| 2to3                     | 246 ms                                                      | 214 ms: 1.15x faster                                                         |
| mdp                      | 1.78 sec                                                    | 1.56 sec: 1.14x faster                                                       |
| sympy_expand             | 314 ms                                                      | 276 ms: 1.14x faster                                                         |
| nqueens                  | 66.6 ms                                                     | 58.8 ms: 1.13x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 1.95 us: 1.13x faster                                                        |
| regex_dna                | 136 ms                                                      | 120 ms: 1.13x faster                                                         |
| fannkuch                 | 256 ms                                                      | 230 ms: 1.11x faster                                                         |
| create_gc_cycles         | 800 us                                                      | 728 us: 1.10x faster                                                         |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.51 ms: 1.09x faster                                                        |
| unpickle                 | 9.09 us                                                     | 8.58 us: 1.06x faster                                                        |
| xml_etree_generate       | 55.5 ms                                                     | 52.7 ms: 1.05x faster                                                        |
| logging_format           | 6.76 us                                                     | 6.42 us: 1.05x faster                                                        |
| regex_v8                 | 15.4 ms                                                     | 14.8 ms: 1.04x faster                                                        |
| regex_effbot             | 1.66 ms                                                     | 1.60 ms: 1.04x faster                                                        |
| logging_simple           | 6.22 us                                                     | 6.00 us: 1.04x faster                                                        |
| meteor_contest           | 75.9 ms                                                     | 73.8 ms: 1.03x faster                                                        |
| xml_etree_parse          | 96.8 ms                                                     | 94.4 ms: 1.03x faster                                                        |
| xml_etree_iterparse      | 65.0 ms                                                     | 63.4 ms: 1.02x faster                                                        |
| unpack_sequence          | 39.6 ns                                                     | 38.8 ns: 1.02x faster                                                        |
| json_loads               | 14.0 us                                                     | 13.8 us: 1.02x faster                                                        |
| python_startup           | 20.6 ms                                                     | 20.2 ms: 1.02x faster                                                        |
| pidigits                 | 149 ms                                                      | 151 ms: 1.01x slower                                                         |
| pathlib                  | 75.7 ms                                                     | 76.9 ms: 1.02x slower                                                        |
| pickle_dict              | 17.2 us                                                     | 17.5 us: 1.02x slower                                                        |
| unpickle_list            | 2.71 us                                                     | 2.79 us: 1.03x slower                                                        |
| gc_traversal             | 1.41 ms                                                     | 1.49 ms: 1.06x slower                                                        |
| bench_mp_pool            | 62.0 ms                                                     | 66.2 ms: 1.07x slower                                                        |
| async_generators         | 222 ms                                                      | 238 ms: 1.07x slower                                                         |
| pickle                   | 6.85 us                                                     | 7.43 us: 1.08x slower                                                        |
| pickle_list              | 2.75 us                                                     | 3.09 us: 1.12x slower                                                        |
| telco                    | 3.94 ms                                                     | 4.58 ms: 1.16x slower                                                        |
| python_startup_no_site   | 15.5 ms                                                     | 18.1 ms: 1.17x slower                                                        |
| coverage                 | 39.0 ms                                                     | 45.6 ms: 1.17x slower                                                        |
| Geometric mean           | (ref)                                                       | 1.24x faster                                                                 |

Benchmark hidden because not significant (2): scimark_fft, json
Ignored benchmarks (10) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: aiohttp, django_template, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, sqlalchemy_declarative, sqlalchemy_imperative, thrift
Ignored benchmarks (4) of results/bm-20240213-3.13.0a3+-9e86002-JIT/bm-20240213-pythonperf1-amd64-brandtbucher-justin_continue-3.13.0a3+-9e86002.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg


# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.18x


# Memory

- memory change: unknown
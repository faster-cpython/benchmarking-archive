# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 208 ms: 1.18x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.72 ms: 1.23x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.61 sec: 1.19x faster                                                      |
| html5lib       | 51.0 ms                                                     | 35.7 ms: 1.43x faster                                                       |
| tornado_http   | 108 ms                                                      | 83.7 ms: 1.29x faster                                                       |
| Geometric mean | (ref)                                                       | 1.26x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 218 ms: 1.99x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 270 ms: 1.95x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 578 ms: 1.92x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 380 ms: 1.68x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.88x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 50.4 ms: 1.22x faster                                                       |
| nbody          | 71.3 ms                                                     | 68.1 ms: 1.05x faster                                                       |
| pidigits       | 149 ms                                                      | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.09x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 75.2 ms: 1.41x faster                                                       |
| regex_dna      | 136 ms                                                      | 120 ms: 1.14x faster                                                        |
| regex_v8       | 15.4 ms                                                     | 14.7 ms: 1.05x faster                                                       |
| regex_effbot   | 1.66 ms                                                     | 1.58 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                       | 1.15x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.58 ms: 1.64x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 175 us: 1.54x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 127 us: 1.45x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 36.5 ms: 1.22x faster                                                       |
| tomli_loads          | 1.67 sec                                                    | 1.41 sec: 1.19x faster                                                      |
| unpickle             | 9.09 us                                                     | 8.38 us: 1.08x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 52.3 ms: 1.06x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 91.2 ms: 1.06x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 62.3 ms: 1.04x faster                                                       |
| unpickle_list        | 2.71 us                                                     | 2.63 us: 1.03x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| pickle               | 6.85 us                                                     | 6.96 us: 1.02x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.84 us: 1.03x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.0 us: 1.05x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.14x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 20.0 ms: 1.03x faster                                                       |
| python_startup_no_site | 15.5 ms                                                     | 18.5 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.26 ms: 1.44x faster                                                       |
| django_template | 28.9 ms                                                     | 21.8 ms: 1.33x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 15.8 ms: 1.25x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 33.7 ms: 1.22x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.31x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 72.1 us: 4.66x faster                                                       |
| deltablue                | 4.19 ms                                                     | 1.98 ms: 2.11x faster                                                       |
| async_tree_none          | 435 ms                                                      | 218 ms: 1.99x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 270 ms: 1.95x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 578 ms: 1.92x faster                                                        |
| pylint                   | 350 ms                                                      | 187 ms: 1.87x faster                                                        |
| richards_super           | 52.2 ms                                                     | 30.0 ms: 1.74x faster                                                       |
| raytrace                 | 273 ms                                                      | 159 ms: 1.72x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 55.1 ns: 1.72x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 50.8 ms: 1.69x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 380 ms: 1.68x faster                                                        |
| chaos                    | 61.7 ms                                                     | 37.1 ms: 1.66x faster                                                       |
| go                       | 139 ms                                                      | 83.6 ms: 1.66x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.58 ms: 1.64x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 745 us: 1.63x faster                                                        |
| richards                 | 42.4 ms                                                     | 26.6 ms: 1.59x faster                                                       |
| comprehensions           | 16.5 us                                                     | 10.4 us: 1.59x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 3.67 ms: 1.57x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 469 ms: 1.56x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 175 us: 1.54x faster                                                        |
| sqlglot_transpile        | 1.48 ms                                                     | 958 us: 1.54x faster                                                        |
| scimark_monte_carlo      | 57.3 ms                                                     | 38.6 ms: 1.48x faster                                                       |
| scimark_sor              | 106 ms                                                      | 72.7 ms: 1.46x faster                                                       |
| pyflate                  | 409 ms                                                      | 280 ms: 1.46x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 43.1 ms: 1.45x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 127 us: 1.45x faster                                                        |
| mako                     | 9.03 ms                                                     | 6.26 ms: 1.44x faster                                                       |
| generators               | 32.4 ms                                                     | 22.6 ms: 1.43x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 35.7 ms: 1.43x faster                                                       |
| regex_compile            | 106 ms                                                      | 75.2 ms: 1.41x faster                                                       |
| pycparser                | 930 ms                                                      | 675 ms: 1.38x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 21.3 us: 1.35x faster                                                       |
| django_template          | 28.9 ms                                                     | 21.8 ms: 1.33x faster                                                       |
| spectral_norm            | 77.3 ms                                                     | 58.4 ms: 1.32x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.37 sec: 1.30x faster                                                      |
| tornado_http             | 108 ms                                                      | 83.7 ms: 1.29x faster                                                       |
| sympy_sum                | 107 ms                                                      | 82.9 ms: 1.29x faster                                                       |
| mypy2                    | 555 ms                                                      | 433 ms: 1.28x faster                                                        |
| dulwich_log              | 50.5 ms                                                     | 40.0 ms: 1.26x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 970 ms: 1.26x faster                                                        |
| genshi_text              | 19.8 ms                                                     | 15.8 ms: 1.25x faster                                                       |
| sympy_integrate          | 15.3 ms                                                     | 12.2 ms: 1.25x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 476 ms: 1.24x faster                                                        |
| sympy_str                | 194 ms                                                      | 158 ms: 1.23x faster                                                        |
| chameleon                | 5.79 ms                                                     | 4.72 ms: 1.23x faster                                                       |
| float                    | 61.7 ms                                                     | 50.4 ms: 1.22x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 36.5 ms: 1.22x faster                                                       |
| genshi_xml               | 41.0 ms                                                     | 33.7 ms: 1.22x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.75 sec: 1.20x faster                                                      |
| sqlglot_optimize         | 39.8 ms                                                     | 33.1 ms: 1.20x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.59 us: 1.20x faster                                                       |
| docutils                 | 1.92 sec                                                    | 1.61 sec: 1.19x faster                                                      |
| tomli_loads              | 1.67 sec                                                    | 1.41 sec: 1.19x faster                                                      |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.29 ms: 1.19x faster                                                       |
| deepcopy                 | 255 us                                                      | 216 us: 1.18x faster                                                        |
| 2to3                     | 246 ms                                                      | 208 ms: 1.18x faster                                                        |
| bench_thread_pool        | 958 us                                                      | 814 us: 1.18x faster                                                        |
| coroutines               | 16.0 ms                                                     | 13.7 ms: 1.17x faster                                                       |
| sqlglot_normalize        | 205 ms                                                      | 175 ms: 1.17x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 57.3 ms: 1.16x faster                                                       |
| sympy_expand             | 314 ms                                                      | 274 ms: 1.15x faster                                                        |
| regex_dna                | 136 ms                                                      | 120 ms: 1.14x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 1.94 us: 1.14x faster                                                       |
| scimark_fft              | 187 ms                                                      | 165 ms: 1.13x faster                                                        |
| aiohttp                  | 995 us                                                      | 895 us: 1.11x faster                                                        |
| unpickle                 | 9.09 us                                                     | 8.38 us: 1.08x faster                                                       |
| unpack_sequence          | 39.6 ns                                                     | 36.7 ns: 1.08x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 70.5 ms: 1.08x faster                                                       |
| json                     | 3.14 ms                                                     | 2.92 ms: 1.07x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 52.3 ms: 1.06x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 91.2 ms: 1.06x faster                                                       |
| fannkuch                 | 256 ms                                                      | 243 ms: 1.05x faster                                                        |
| regex_v8                 | 15.4 ms                                                     | 14.7 ms: 1.05x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.44 us: 1.05x faster                                                       |
| nbody                    | 71.3 ms                                                     | 68.1 ms: 1.05x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.58 ms: 1.05x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.95 us: 1.05x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 62.3 ms: 1.04x faster                                                       |
| unpickle_list            | 2.71 us                                                     | 2.63 us: 1.03x faster                                                       |
| python_startup           | 20.6 ms                                                     | 20.0 ms: 1.03x faster                                                       |
| json_loads               | 14.0 us                                                     | 13.8 us: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 146 ms: 1.02x faster                                                        |
| pickle                   | 6.85 us                                                     | 6.96 us: 1.02x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 63.8 ms: 1.03x slower                                                       |
| pathlib                  | 75.7 ms                                                     | 78.0 ms: 1.03x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.84 us: 1.03x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.0 us: 1.05x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 847 us: 1.06x slower                                                        |
| async_generators         | 222 ms                                                      | 240 ms: 1.08x slower                                                        |
| gc_traversal             | 1.41 ms                                                     | 1.53 ms: 1.09x slower                                                       |
| coverage                 | 39.0 ms                                                     | 46.3 ms: 1.19x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 18.5 ms: 1.19x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.77 ms: 1.21x slower                                                       |
| thrift                   | 617 us                                                      | 8.11 ms: 13.14x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.24x faster                                                                |
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown
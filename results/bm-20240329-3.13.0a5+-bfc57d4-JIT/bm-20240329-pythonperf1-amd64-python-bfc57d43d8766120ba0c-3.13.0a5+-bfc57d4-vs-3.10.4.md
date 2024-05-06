# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 223 ms: 1.10x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.64 ms: 1.25x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.68 sec: 1.14x faster                                                      |
| html5lib       | 51.0 ms                                                     | 36.0 ms: 1.42x faster                                                       |
| tornado_http   | 108 ms                                                      | 84.0 ms: 1.29x faster                                                       |
| Geometric mean | (ref)                                                       | 1.24x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 213 ms: 2.05x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 266 ms: 1.98x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 563 ms: 1.97x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 372 ms: 1.71x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.92x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.8 ms: 1.32x faster                                                       |
| nbody          | 71.3 ms                                                     | 58.8 ms: 1.21x faster                                                       |
| pidigits       | 149 ms                                                      | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.18x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 83.3 ms: 1.27x faster                                                       |
| regex_dna      | 136 ms                                                      | 121 ms: 1.13x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.60 ms: 1.03x faster                                                       |
| regex_v8       | 15.4 ms                                                     | 17.6 ms: 1.14x slower                                                       |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.51 ms: 1.66x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 175 us: 1.54x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 130 us: 1.41x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.19 sec: 1.40x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 36.5 ms: 1.22x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.53 us: 1.07x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 92.4 ms: 1.05x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 62.3 ms: 1.04x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 53.5 ms: 1.04x faster                                                       |
| unpickle_list        | 2.71 us                                                     | 2.67 us: 1.02x faster                                                       |
| pickle               | 6.85 us                                                     | 7.27 us: 1.06x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.4 us: 1.07x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.96 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.14x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 22.5 ms: 1.09x slower                                                       |
| python_startup_no_site | 15.5 ms                                                     | 20.4 ms: 1.31x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.20x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 5.61 ms: 1.61x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 15.4 ms: 1.28x faster                                                       |
| django_template | 28.9 ms                                                     | 22.5 ms: 1.28x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 36.3 ms: 1.13x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.32x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 69.4 us: 4.84x faster                                                       |
| deltablue                | 4.19 ms                                                     | 2.01 ms: 2.08x faster                                                       |
| async_tree_none          | 435 ms                                                      | 213 ms: 2.05x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 266 ms: 1.98x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 563 ms: 1.97x faster                                                        |
| pylint                   | 350 ms                                                      | 194 ms: 1.80x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 52.7 ns: 1.79x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 372 ms: 1.71x faster                                                        |
| json_dumps               | 9.16 ms                                                     | 5.51 ms: 1.66x faster                                                       |
| generators               | 32.4 ms                                                     | 19.5 ms: 1.66x faster                                                       |
| mako                     | 9.03 ms                                                     | 5.61 ms: 1.61x faster                                                       |
| richards_super           | 52.2 ms                                                     | 32.7 ms: 1.60x faster                                                       |
| chaos                    | 61.7 ms                                                     | 38.9 ms: 1.59x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 772 us: 1.57x faster                                                        |
| asyncio_tcp              | 732 ms                                                      | 473 ms: 1.55x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 175 us: 1.54x faster                                                        |
| raytrace                 | 273 ms                                                      | 178 ms: 1.54x faster                                                        |
| spectral_norm            | 77.3 ms                                                     | 51.4 ms: 1.50x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 986 us: 1.50x faster                                                        |
| go                       | 139 ms                                                      | 93.0 ms: 1.49x faster                                                       |
| richards                 | 42.4 ms                                                     | 29.1 ms: 1.46x faster                                                       |
| comprehensions           | 16.5 us                                                     | 11.3 us: 1.46x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 39.4 ms: 1.45x faster                                                       |
| pyflate                  | 409 ms                                                      | 283 ms: 1.45x faster                                                        |
| html5lib                 | 51.0 ms                                                     | 36.0 ms: 1.42x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 130 us: 1.41x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 44.6 ms: 1.40x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.19 sec: 1.40x faster                                                      |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.52 sec: 1.39x faster                                                      |
| pycparser                | 930 ms                                                      | 671 ms: 1.39x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 21.6 us: 1.33x faster                                                       |
| scimark_sor              | 106 ms                                                      | 80.5 ms: 1.32x faster                                                       |
| float                    | 61.7 ms                                                     | 46.8 ms: 1.32x faster                                                       |
| tornado_http             | 108 ms                                                      | 84.0 ms: 1.29x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 15.4 ms: 1.28x faster                                                       |
| django_template          | 28.9 ms                                                     | 22.5 ms: 1.28x faster                                                       |
| regex_compile            | 106 ms                                                      | 83.3 ms: 1.27x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.41 sec: 1.26x faster                                                      |
| pprint_pformat           | 1.22 sec                                                    | 972 ms: 1.25x faster                                                        |
| pprint_safe_repr         | 592 ms                                                      | 475 ms: 1.25x faster                                                        |
| hexiom                   | 5.74 ms                                                     | 4.61 ms: 1.25x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.64 ms: 1.25x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 40.6 ms: 1.24x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 69.1 ms: 1.24x faster                                                       |
| mypy2                    | 555 ms                                                      | 448 ms: 1.24x faster                                                        |
| sympy_sum                | 107 ms                                                      | 86.8 ms: 1.23x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 36.5 ms: 1.22x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.24 ms: 1.22x faster                                                       |
| nbody                    | 71.3 ms                                                     | 58.8 ms: 1.21x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.2 ms: 1.21x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.58 us: 1.21x faster                                                       |
| sympy_str                | 194 ms                                                      | 165 ms: 1.18x faster                                                        |
| bench_thread_pool        | 958 us                                                      | 822 us: 1.17x faster                                                        |
| sympy_integrate          | 15.3 ms                                                     | 13.2 ms: 1.16x faster                                                       |
| deepcopy_reduce          | 2.20 us                                                     | 1.92 us: 1.15x faster                                                       |
| deepcopy                 | 255 us                                                      | 223 us: 1.14x faster                                                        |
| docutils                 | 1.92 sec                                                    | 1.68 sec: 1.14x faster                                                      |
| genshi_xml               | 41.0 ms                                                     | 36.3 ms: 1.13x faster                                                       |
| regex_dna                | 136 ms                                                      | 121 ms: 1.13x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 35.5 ms: 1.12x faster                                                       |
| scimark_fft              | 187 ms                                                      | 167 ms: 1.12x faster                                                        |
| fannkuch                 | 256 ms                                                      | 229 ms: 1.12x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 184 ms: 1.12x faster                                                        |
| aiohttp                  | 995 us                                                      | 898 us: 1.11x faster                                                        |
| sympy_expand             | 314 ms                                                      | 284 ms: 1.11x faster                                                        |
| 2to3                     | 246 ms                                                      | 223 ms: 1.10x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 61.9 ms: 1.08x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.29 us: 1.07x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.53 us: 1.07x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.91 us: 1.05x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 92.4 ms: 1.05x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 62.3 ms: 1.04x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 73.2 ms: 1.04x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 53.5 ms: 1.04x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.60 ms: 1.03x faster                                                       |
| pidigits                 | 149 ms                                                      | 146 ms: 1.02x faster                                                        |
| unpickle_list            | 2.71 us                                                     | 2.67 us: 1.02x faster                                                       |
| pathlib                  | 75.7 ms                                                     | 77.8 ms: 1.03x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.27 us: 1.06x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 853 us: 1.07x slower                                                        |
| pickle_dict              | 17.2 us                                                     | 18.4 us: 1.07x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.96 us: 1.08x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.09x slower                                                       |
| python_startup           | 20.6 ms                                                     | 22.5 ms: 1.09x slower                                                       |
| unpack_sequence          | 39.6 ns                                                     | 44.0 ns: 1.11x slower                                                       |
| async_generators         | 222 ms                                                      | 248 ms: 1.12x slower                                                        |
| bench_mp_pool            | 62.0 ms                                                     | 70.8 ms: 1.14x slower                                                       |
| regex_v8                 | 15.4 ms                                                     | 17.6 ms: 1.14x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.74 ms: 1.20x slower                                                       |
| coverage                 | 39.0 ms                                                     | 47.0 ms: 1.21x slower                                                       |
| json                     | 3.14 ms                                                     | 3.88 ms: 1.24x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 20.4 ms: 1.31x slower                                                       |
| thrift                   | 617 us                                                      | 8.91 ms: 14.44x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.21x faster                                                                |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown
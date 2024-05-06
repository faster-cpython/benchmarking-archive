# Results vs. 3.10.4

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 225 ms: 1.09x faster                                                        |
| chameleon      | 5.79 ms                                                     | 5.11 ms: 1.13x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.74 sec: 1.10x faster                                                      |
| html5lib       | 51.0 ms                                                     | 39.4 ms: 1.30x faster                                                       |
| tornado_http   | 108 ms                                                      | 85.6 ms: 1.27x faster                                                       |
| Geometric mean | (ref)                                                       | 1.17x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 222 ms: 1.96x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 273 ms: 1.93x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 580 ms: 1.91x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 381 ms: 1.67x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.86x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 59.3 ms: 1.04x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.01x faster                                                        |
| nbody          | 71.3 ms                                                     | 84.9 ms: 1.19x slower                                                       |
| Geometric mean | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 136 ms                                                      | 122 ms: 1.11x faster                                                        |
| regex_compile  | 106 ms                                                      | 103 ms: 1.03x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.62 ms: 1.02x faster                                                       |
| regex_v8       | 15.4 ms                                                     | 17.4 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.73 ms: 1.60x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 189 us: 1.43x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 39.0 ms: 1.14x faster                                                       |
| tomli_loads          | 1.67 sec                                                    | 1.51 sec: 1.11x faster                                                      |
| unpickle_pure_python | 183 us                                                      | 167 us: 1.10x faster                                                        |
| xml_etree_parse      | 96.8 ms                                                     | 90.3 ms: 1.07x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.57 us: 1.06x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 56.4 ms: 1.02x slower                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 66.5 ms: 1.02x slower                                                       |
| unpickle_list        | 2.71 us                                                     | 2.79 us: 1.03x slower                                                       |
| pickle               | 6.85 us                                                     | 7.04 us: 1.03x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.85 us: 1.04x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.1 us: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.08x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 15.5 ms                                                     | 18.1 ms: 1.17x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.08x slower                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 28.9 ms                                                     | 23.6 ms: 1.23x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 16.6 ms: 1.20x faster                                                       |
| mako            | 9.03 ms                                                     | 7.56 ms: 1.20x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 37.4 ms: 1.10x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.18x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 72.8 us: 4.61x faster                                                       |
| async_tree_none          | 435 ms                                                      | 222 ms: 1.96x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 273 ms: 1.93x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 580 ms: 1.91x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.27 ms: 1.85x faster                                                       |
| pylint                   | 350 ms                                                      | 199 ms: 1.76x faster                                                        |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 381 ms: 1.67x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 57.2 ns: 1.65x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.73 ms: 1.60x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 461 ms: 1.59x faster                                                        |
| richards_super           | 52.2 ms                                                     | 34.2 ms: 1.53x faster                                                       |
| generators               | 32.4 ms                                                     | 21.7 ms: 1.49x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 843 us: 1.44x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 189 us: 1.43x faster                                                        |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.49 sec: 1.42x faster                                                      |
| richards                 | 42.4 ms                                                     | 30.5 ms: 1.39x faster                                                       |
| raytrace                 | 273 ms                                                      | 197 ms: 1.38x faster                                                        |
| sqlglot_transpile        | 1.48 ms                                                     | 1.07 ms: 1.38x faster                                                       |
| chaos                    | 61.7 ms                                                     | 45.4 ms: 1.36x faster                                                       |
| go                       | 139 ms                                                      | 104 ms: 1.34x faster                                                        |
| html5lib                 | 51.0 ms                                                     | 39.4 ms: 1.30x faster                                                       |
| tornado_http             | 108 ms                                                      | 85.6 ms: 1.27x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.42 sec: 1.25x faster                                                      |
| pycparser                | 930 ms                                                      | 746 ms: 1.25x faster                                                        |
| django_template          | 28.9 ms                                                     | 23.6 ms: 1.23x faster                                                       |
| crypto_pyaes             | 62.5 ms                                                     | 51.6 ms: 1.21x faster                                                       |
| mypy2                    | 555 ms                                                      | 458 ms: 1.21x faster                                                        |
| genshi_text              | 19.8 ms                                                     | 16.6 ms: 1.20x faster                                                       |
| mako                     | 9.03 ms                                                     | 7.56 ms: 1.20x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.5 ms: 1.18x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.64 us: 1.17x faster                                                       |
| pyflate                  | 409 ms                                                      | 354 ms: 1.16x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 25.2 us: 1.14x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 39.0 ms: 1.14x faster                                                       |
| sympy_sum                | 107 ms                                                      | 93.9 ms: 1.14x faster                                                       |
| comprehensions           | 16.5 us                                                     | 14.5 us: 1.14x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 44.5 ms: 1.13x faster                                                       |
| chameleon                | 5.79 ms                                                     | 5.11 ms: 1.13x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 848 us: 1.13x faster                                                        |
| scimark_sor              | 106 ms                                                      | 95.0 ms: 1.12x faster                                                       |
| regex_dna                | 136 ms                                                      | 122 ms: 1.11x faster                                                        |
| tomli_loads              | 1.67 sec                                                    | 1.51 sec: 1.11x faster                                                      |
| docutils                 | 1.92 sec                                                    | 1.74 sec: 1.10x faster                                                      |
| unpickle_pure_python     | 183 us                                                      | 167 us: 1.10x faster                                                        |
| genshi_xml               | 41.0 ms                                                     | 37.4 ms: 1.10x faster                                                       |
| sympy_integrate          | 15.3 ms                                                     | 13.9 ms: 1.10x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 52.4 ms: 1.09x faster                                                       |
| 2to3                     | 246 ms                                                      | 225 ms: 1.09x faster                                                        |
| aiohttp                  | 995 us                                                      | 913 us: 1.09x faster                                                        |
| pprint_pformat           | 1.22 sec                                                    | 1.13 sec: 1.08x faster                                                      |
| deepcopy                 | 255 us                                                      | 236 us: 1.08x faster                                                        |
| pprint_safe_repr         | 592 ms                                                      | 550 ms: 1.08x faster                                                        |
| sympy_str                | 194 ms                                                      | 181 ms: 1.07x faster                                                        |
| xml_etree_parse          | 96.8 ms                                                     | 90.3 ms: 1.07x faster                                                       |
| sqlglot_optimize         | 39.8 ms                                                     | 37.5 ms: 1.06x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.57 us: 1.06x faster                                                       |
| sqlglot_normalize        | 205 ms                                                      | 194 ms: 1.06x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 2.09 us: 1.05x faster                                                       |
| float                    | 61.7 ms                                                     | 59.3 ms: 1.04x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 5.57 ms: 1.03x faster                                                       |
| regex_compile            | 106 ms                                                      | 103 ms: 1.03x faster                                                        |
| sympy_expand             | 314 ms                                                      | 306 ms: 1.03x faster                                                        |
| regex_effbot             | 1.66 ms                                                     | 1.62 ms: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.01x faster                                                        |
| scimark_lu               | 85.8 ms                                                     | 85.4 ms: 1.00x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.83 us: 1.01x slower                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 56.4 ms: 1.02x slower                                                       |
| meteor_contest           | 75.9 ms                                                     | 77.2 ms: 1.02x slower                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 66.5 ms: 1.02x slower                                                       |
| unpickle_list            | 2.71 us                                                     | 2.79 us: 1.03x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.04 us: 1.03x slower                                                       |
| logging_simple           | 6.22 us                                                     | 6.40 us: 1.03x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.85 us: 1.04x slower                                                       |
| pathlib                  | 75.7 ms                                                     | 78.5 ms: 1.04x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 65.1 ms: 1.05x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.1 us: 1.06x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 850 us: 1.06x slower                                                        |
| unpack_sequence          | 39.6 ns                                                     | 42.5 ns: 1.07x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.53 ms: 1.09x slower                                                       |
| nqueens                  | 66.6 ms                                                     | 73.6 ms: 1.10x slower                                                       |
| spectral_norm            | 77.3 ms                                                     | 85.5 ms: 1.11x slower                                                       |
| regex_v8                 | 15.4 ms                                                     | 17.4 ms: 1.13x slower                                                       |
| fannkuch                 | 256 ms                                                      | 294 ms: 1.15x slower                                                        |
| async_generators         | 222 ms                                                      | 255 ms: 1.15x slower                                                        |
| scimark_fft              | 187 ms                                                      | 216 ms: 1.15x slower                                                        |
| python_startup_no_site   | 15.5 ms                                                     | 18.1 ms: 1.17x slower                                                       |
| coverage                 | 39.0 ms                                                     | 46.3 ms: 1.19x slower                                                       |
| nbody                    | 71.3 ms                                                     | 84.9 ms: 1.19x slower                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 3.29 ms: 1.21x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.93 ms: 1.25x slower                                                       |
| json                     | 3.14 ms                                                     | 3.99 ms: 1.27x slower                                                       |
| thrift                   | 617 us                                                      | 9.46 ms: 15.33x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (2): python_startup, json_loads
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (4) of results/bm-20240329-3.13.0a5+-bfc57d4-PYTHON_UOPS/bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown
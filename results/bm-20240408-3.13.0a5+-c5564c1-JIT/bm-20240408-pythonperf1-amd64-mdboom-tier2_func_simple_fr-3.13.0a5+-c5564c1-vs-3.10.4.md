# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 221 ms: 1.11x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.74 ms: 1.22x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.70 sec: 1.13x faster                                                      |
| html5lib       | 51.0 ms                                                     | 35.3 ms: 1.45x faster                                                       |
| tornado_http   | 108 ms                                                      | 83.9 ms: 1.29x faster                                                       |
| Geometric mean | (ref)                                                       | 1.23x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 221 ms: 1.97x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 268 ms: 1.96x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 584 ms: 1.90x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 392 ms: 1.63x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.86x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 47.1 ms: 1.31x faster                                                       |
| nbody          | 71.3 ms                                                     | 58.1 ms: 1.23x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.18x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 86.4 ms: 1.23x faster                                                       |
| regex_dna      | 136 ms                                                      | 121 ms: 1.13x faster                                                        |
| regex_v8       | 15.4 ms                                                     | 14.9 ms: 1.04x faster                                                       |
| regex_effbot   | 1.66 ms                                                     | 1.61 ms: 1.03x faster                                                       |
| Geometric mean | (ref)                                                       | 1.10x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.60 ms: 1.64x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 174 us: 1.55x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 127 us: 1.44x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.20 sec: 1.39x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 36.4 ms: 1.22x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 60.9 ms: 1.07x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 90.9 ms: 1.07x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 52.7 ms: 1.05x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.9 us: 1.01x faster                                                       |
| pickle               | 6.85 us                                                     | 7.26 us: 1.06x slower                                                       |
| unpickle_list        | 2.71 us                                                     | 2.89 us: 1.07x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.94 us: 1.07x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.5 us: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.13x faster                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                       |
| python_startup_no_site | 15.5 ms                                                     | 19.7 ms: 1.27x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.16x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 5.64 ms: 1.60x faster                                                       |
| genshi_text    | 19.8 ms                                                     | 15.4 ms: 1.29x faster                                                       |
| genshi_xml     | 41.0 ms                                                     | 34.3 ms: 1.20x faster                                                       |
| Geometric mean | (ref)                                                       | 1.35x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 70.8 us: 4.75x faster                                                       |
| async_tree_none          | 435 ms                                                      | 221 ms: 1.97x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 268 ms: 1.96x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.14 ms: 1.96x faster                                                       |
| async_tree_io            | 1.11 sec                                                    | 584 ms: 1.90x faster                                                        |
| pylint                   | 350 ms                                                      | 194 ms: 1.81x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 53.0 ns: 1.79x faster                                                       |
| richards_super           | 52.2 ms                                                     | 30.6 ms: 1.71x faster                                                       |
| raytrace                 | 273 ms                                                      | 163 ms: 1.68x faster                                                        |
| generators               | 32.4 ms                                                     | 19.5 ms: 1.66x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.60 ms: 1.64x faster                                                       |
| chaos                    | 61.7 ms                                                     | 37.9 ms: 1.63x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 392 ms: 1.63x faster                                                        |
| mako                     | 9.03 ms                                                     | 5.64 ms: 1.60x faster                                                       |
| richards                 | 42.4 ms                                                     | 26.8 ms: 1.58x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 772 us: 1.57x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 174 us: 1.55x faster                                                        |
| asyncio_tcp              | 732 ms                                                      | 473 ms: 1.55x faster                                                        |
| pyflate                  | 409 ms                                                      | 268 ms: 1.53x faster                                                        |
| comprehensions           | 16.5 us                                                     | 10.8 us: 1.52x faster                                                       |
| go                       | 139 ms                                                      | 91.4 ms: 1.52x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 992 us: 1.49x faster                                                        |
| spectral_norm            | 77.3 ms                                                     | 52.2 ms: 1.48x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 39.0 ms: 1.47x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 35.3 ms: 1.45x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 127 us: 1.44x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 44.0 ms: 1.42x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.20 sec: 1.39x faster                                                      |
| deepcopy_memo            | 28.8 us                                                     | 21.0 us: 1.37x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.60 sec: 1.32x faster                                                      |
| pycparser                | 930 ms                                                      | 709 ms: 1.31x faster                                                        |
| float                    | 61.7 ms                                                     | 47.1 ms: 1.31x faster                                                       |
| tornado_http             | 108 ms                                                      | 83.9 ms: 1.29x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 15.4 ms: 1.29x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 4.47 ms: 1.28x faster                                                       |
| scimark_sor              | 106 ms                                                      | 83.5 ms: 1.27x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 976 ms: 1.25x faster                                                        |
| mypy2                    | 555 ms                                                      | 448 ms: 1.24x faster                                                        |
| pprint_safe_repr         | 592 ms                                                      | 480 ms: 1.23x faster                                                        |
| regex_compile            | 106 ms                                                      | 86.4 ms: 1.23x faster                                                       |
| nbody                    | 71.3 ms                                                     | 58.1 ms: 1.23x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.74 ms: 1.22x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 36.4 ms: 1.22x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.1 ms: 1.22x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 41.4 ms: 1.22x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.57 us: 1.22x faster                                                       |
| sympy_sum                | 107 ms                                                      | 88.2 ms: 1.21x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.26 ms: 1.20x faster                                                       |
| genshi_xml               | 41.0 ms                                                     | 34.3 ms: 1.20x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 818 us: 1.17x faster                                                        |
| sympy_str                | 194 ms                                                      | 167 ms: 1.17x faster                                                        |
| mdp                      | 1.78 sec                                                    | 1.53 sec: 1.16x faster                                                      |
| deepcopy                 | 255 us                                                      | 220 us: 1.16x faster                                                        |
| sympy_integrate          | 15.3 ms                                                     | 13.3 ms: 1.15x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 75.0 ms: 1.14x faster                                                       |
| sqlglot_normalize        | 205 ms                                                      | 180 ms: 1.14x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 35.0 ms: 1.14x faster                                                       |
| regex_dna                | 136 ms                                                      | 121 ms: 1.13x faster                                                        |
| docutils                 | 1.92 sec                                                    | 1.70 sec: 1.13x faster                                                      |
| scimark_fft              | 187 ms                                                      | 166 ms: 1.13x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 1.96 us: 1.12x faster                                                       |
| fannkuch                 | 256 ms                                                      | 230 ms: 1.11x faster                                                        |
| sympy_expand             | 314 ms                                                      | 282 ms: 1.11x faster                                                        |
| 2to3                     | 246 ms                                                      | 221 ms: 1.11x faster                                                        |
| aiohttp                  | 995 us                                                      | 907 us: 1.10x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 60.9 ms: 1.09x faster                                                       |
| json                     | 3.14 ms                                                     | 2.90 ms: 1.08x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.26 us: 1.08x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 60.9 ms: 1.07x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.83 us: 1.07x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 90.9 ms: 1.07x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 52.7 ms: 1.05x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 73.1 ms: 1.04x faster                                                       |
| regex_v8                 | 15.4 ms                                                     | 14.9 ms: 1.04x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.61 ms: 1.03x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| json_loads               | 14.0 us                                                     | 13.9 us: 1.01x faster                                                       |
| pathlib                  | 75.7 ms                                                     | 78.1 ms: 1.03x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.26 us: 1.06x slower                                                       |
| python_startup           | 20.6 ms                                                     | 21.9 ms: 1.06x slower                                                       |
| unpickle_list            | 2.71 us                                                     | 2.89 us: 1.07x slower                                                       |
| async_generators         | 222 ms                                                      | 237 ms: 1.07x slower                                                        |
| pickle_list              | 2.75 us                                                     | 2.94 us: 1.07x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.5 us: 1.08x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.55 ms: 1.10x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 68.9 ms: 1.11x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 909 us: 1.14x slower                                                        |
| coverage                 | 39.0 ms                                                     | 45.1 ms: 1.16x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.84 ms: 1.23x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 19.7 ms: 1.27x slower                                                       |
| thrift                   | 617 us                                                      | 8.84 ms: 14.31x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.21x faster                                                                |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240408-3.13.0a5+-c5564c1-JIT/bm-20240408-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown
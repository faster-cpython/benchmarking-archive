# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.23x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 216 ms: 1.14x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.69 ms: 1.23x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.67 sec: 1.15x faster                                                      |
| html5lib       | 51.0 ms                                                     | 37.3 ms: 1.37x faster                                                       |
| tornado_http   | 108 ms                                                      | 81.7 ms: 1.33x faster                                                       |
| Geometric mean | (ref)                                                       | 1.24x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 216 ms: 2.01x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 263 ms: 2.00x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 585 ms: 1.89x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 383 ms: 1.67x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.89x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.6 ms: 1.32x faster                                                       |
| nbody          | 71.3 ms                                                     | 58.2 ms: 1.23x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.18x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 84.3 ms: 1.26x faster                                                       |
| regex_dna      | 136 ms                                                      | 117 ms: 1.17x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                       |
| regex_v8       | 15.4 ms                                                     | 14.7 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.56 ms: 1.65x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 171 us: 1.57x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 124 us: 1.48x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.17 sec: 1.42x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 36.0 ms: 1.24x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 89.7 ms: 1.08x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 60.5 ms: 1.07x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 52.2 ms: 1.06x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.67 us: 1.05x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.6 us: 1.03x faster                                                       |
| pickle               | 6.85 us                                                     | 7.41 us: 1.08x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| pickle_list          | 2.75 us                                                     | 3.02 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.15x faster                                                                |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 21.5 ms: 1.04x slower                                                       |
| python_startup_no_site | 15.5 ms                                                     | 17.9 ms: 1.15x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.10x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 5.58 ms: 1.62x faster                                                       |
| django_template | 28.9 ms                                                     | 21.5 ms: 1.34x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 15.1 ms: 1.31x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 32.7 ms: 1.25x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.37x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 70.1 us: 4.80x faster                                                       |
| async_tree_none          | 435 ms                                                      | 216 ms: 2.01x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 263 ms: 2.00x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.12 ms: 1.98x faster                                                       |
| async_tree_io            | 1.11 sec                                                    | 585 ms: 1.89x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 53.5 ns: 1.77x faster                                                       |
| raytrace                 | 273 ms                                                      | 161 ms: 1.70x faster                                                        |
| richards_super           | 52.2 ms                                                     | 30.9 ms: 1.69x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 383 ms: 1.67x faster                                                        |
| generators               | 32.4 ms                                                     | 19.5 ms: 1.66x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.56 ms: 1.65x faster                                                       |
| pylint                   | 350 ms                                                      | 213 ms: 1.65x faster                                                        |
| mako                     | 9.03 ms                                                     | 5.58 ms: 1.62x faster                                                       |
| chaos                    | 61.7 ms                                                     | 38.2 ms: 1.62x faster                                                       |
| pickle_pure_python       | 270 us                                                      | 171 us: 1.57x faster                                                        |
| sqlglot_parse            | 1.22 ms                                                     | 772 us: 1.57x faster                                                        |
| comprehensions           | 16.5 us                                                     | 10.6 us: 1.56x faster                                                       |
| pyflate                  | 409 ms                                                      | 264 ms: 1.55x faster                                                        |
| richards                 | 42.4 ms                                                     | 27.4 ms: 1.55x faster                                                       |
| spectral_norm            | 77.3 ms                                                     | 50.0 ms: 1.55x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 477 ms: 1.53x faster                                                        |
| go                       | 139 ms                                                      | 91.0 ms: 1.53x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 985 us: 1.50x faster                                                        |
| scimark_monte_carlo      | 57.3 ms                                                     | 38.6 ms: 1.49x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 124 us: 1.48x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 42.8 ms: 1.46x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.17 sec: 1.42x faster                                                      |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.52 sec: 1.38x faster                                                      |
| html5lib                 | 51.0 ms                                                     | 37.3 ms: 1.37x faster                                                       |
| deepcopy_memo            | 28.8 us                                                     | 21.2 us: 1.35x faster                                                       |
| pycparser                | 930 ms                                                      | 692 ms: 1.34x faster                                                        |
| django_template          | 28.9 ms                                                     | 21.5 ms: 1.34x faster                                                       |
| tornado_http             | 108 ms                                                      | 81.7 ms: 1.33x faster                                                       |
| float                    | 61.7 ms                                                     | 46.6 ms: 1.32x faster                                                       |
| scimark_sor              | 106 ms                                                      | 80.2 ms: 1.32x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 4.35 ms: 1.32x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 15.1 ms: 1.31x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 935 ms: 1.30x faster                                                        |
| pprint_safe_repr         | 592 ms                                                      | 457 ms: 1.30x faster                                                        |
| dulwich_log              | 50.5 ms                                                     | 39.5 ms: 1.28x faster                                                       |
| mypy2                    | 555 ms                                                      | 441 ms: 1.26x faster                                                        |
| regex_compile            | 106 ms                                                      | 84.3 ms: 1.26x faster                                                       |
| genshi_xml               | 41.0 ms                                                     | 32.7 ms: 1.25x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 36.0 ms: 1.24x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.21 ms: 1.23x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.69 ms: 1.23x faster                                                       |
| nbody                    | 71.3 ms                                                     | 58.2 ms: 1.23x faster                                                       |
| sympy_sum                | 107 ms                                                      | 87.9 ms: 1.22x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 787 us: 1.22x faster                                                        |
| coroutines               | 16.0 ms                                                     | 13.2 ms: 1.21x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.48 sec: 1.20x faster                                                      |
| sqlite_synth             | 1.91 us                                                     | 1.61 us: 1.19x faster                                                       |
| deepcopy                 | 255 us                                                      | 215 us: 1.19x faster                                                        |
| sympy_str                | 194 ms                                                      | 166 ms: 1.17x faster                                                        |
| regex_dna                | 136 ms                                                      | 117 ms: 1.17x faster                                                        |
| sympy_integrate          | 15.3 ms                                                     | 13.2 ms: 1.16x faster                                                       |
| deepcopy_reduce          | 2.20 us                                                     | 1.91 us: 1.15x faster                                                       |
| docutils                 | 1.92 sec                                                    | 1.67 sec: 1.15x faster                                                      |
| sqlglot_optimize         | 39.8 ms                                                     | 34.7 ms: 1.15x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 75.0 ms: 1.14x faster                                                       |
| 2to3                     | 246 ms                                                      | 216 ms: 1.14x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 180 ms: 1.14x faster                                                        |
| scimark_fft              | 187 ms                                                      | 165 ms: 1.14x faster                                                        |
| aiohttp                  | 995 us                                                      | 888 us: 1.12x faster                                                        |
| fannkuch                 | 256 ms                                                      | 231 ms: 1.10x faster                                                        |
| sympy_expand             | 314 ms                                                      | 285 ms: 1.10x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 60.4 ms: 1.10x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.16 us: 1.10x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.69 us: 1.09x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 89.7 ms: 1.08x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 60.5 ms: 1.07x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 52.2 ms: 1.06x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                       |
| regex_v8                 | 15.4 ms                                                     | 14.7 ms: 1.05x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.67 us: 1.05x faster                                                       |
| json                     | 3.14 ms                                                     | 3.01 ms: 1.04x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 72.9 ms: 1.04x faster                                                       |
| json_loads               | 14.0 us                                                     | 13.6 us: 1.03x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.02x faster                                                        |
| python_startup           | 20.6 ms                                                     | 21.5 ms: 1.04x slower                                                       |
| async_generators         | 222 ms                                                      | 235 ms: 1.06x slower                                                        |
| pickle                   | 6.85 us                                                     | 7.41 us: 1.08x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 67.2 ms: 1.08x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.6 us: 1.08x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.10x slower                                                       |
| pickle_list              | 2.75 us                                                     | 3.02 us: 1.10x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 891 us: 1.11x slower                                                        |
| python_startup_no_site   | 15.5 ms                                                     | 17.9 ms: 1.15x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.76 ms: 1.21x slower                                                       |
| coverage                 | 39.0 ms                                                     | 48.9 ms: 1.25x slower                                                       |
| thrift                   | 617 us                                                      | 8.70 ms: 14.09x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.23x faster                                                                |

Benchmark hidden because not significant (2): pathlib, unpickle_list
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown
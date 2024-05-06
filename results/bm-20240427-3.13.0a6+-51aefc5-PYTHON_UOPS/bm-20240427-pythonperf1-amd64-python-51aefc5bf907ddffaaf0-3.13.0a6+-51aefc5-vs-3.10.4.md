# Results vs. 3.10.4

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-amd64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 232 ms: 1.06x faster                                                        |
| chameleon      | 5.79 ms                                                     | 5.08 ms: 1.14x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.79 sec: 1.07x faster                                                      |
| html5lib       | 51.0 ms                                                     | 38.9 ms: 1.31x faster                                                       |
| tornado_http   | 108 ms                                                      | 94.8 ms: 1.14x faster                                                       |
| Geometric mean | (ref)                                                       | 1.14x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 285 ms: 1.85x faster                                                        |
| async_tree_none         | 435 ms                                                      | 238 ms: 1.83x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 609 ms: 1.82x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 405 ms: 1.57x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.76x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 54.5 ms: 1.13x faster                                                       |
| nbody          | 71.3 ms                                                     | 74.3 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 136 ms                                                      | 118 ms: 1.16x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.59 ms: 1.04x faster                                                       |
| regex_v8       | 15.4 ms                                                     | 20.0 ms: 1.29x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.81 ms: 1.58x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 186 us: 1.45x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.43 sec: 1.17x faster                                                      |
| unpickle_pure_python | 183 us                                                      | 159 us: 1.15x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 38.8 ms: 1.15x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 93.7 ms: 1.03x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.83 us: 1.03x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 57.3 ms: 1.03x slower                                                       |
| json_loads           | 14.0 us                                                     | 14.6 us: 1.04x slower                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 67.8 ms: 1.04x slower                                                       |
| unpickle_list        | 2.71 us                                                     | 2.85 us: 1.05x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.97 us: 1.08x slower                                                       |
| pickle               | 6.85 us                                                     | 7.45 us: 1.09x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 20.2 us: 1.18x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.06x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 20.5 ms: 1.01x faster                                                       |
| python_startup_no_site | 15.5 ms                                                     | 16.7 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.03x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.96 ms: 1.30x faster                                                       |
| django_template | 28.9 ms                                                     | 24.2 ms: 1.19x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 17.8 ms: 1.11x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 37.3 ms: 1.10x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.17x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 116 us: 2.90x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 285 ms: 1.85x faster                                                        |
| async_tree_none          | 435 ms                                                      | 238 ms: 1.83x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 609 ms: 1.82x faster                                                        |
| richards_super           | 52.2 ms                                                     | 30.7 ms: 1.70x faster                                                       |
| deltablue                | 4.19 ms                                                     | 2.52 ms: 1.66x faster                                                       |
| logging_silent           | 94.6 ns                                                     | 57.8 ns: 1.64x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.81 ms: 1.58x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 405 ms: 1.57x faster                                                        |
| richards                 | 42.4 ms                                                     | 27.3 ms: 1.55x faster                                                       |
| pylint                   | 350 ms                                                      | 227 ms: 1.54x faster                                                        |
| raytrace                 | 273 ms                                                      | 177 ms: 1.54x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 186 us: 1.45x faster                                                        |
| generators               | 32.4 ms                                                     | 22.7 ms: 1.42x faster                                                       |
| chaos                    | 61.7 ms                                                     | 44.1 ms: 1.40x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 1.06 ms: 1.39x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 874 us: 1.39x faster                                                        |
| go                       | 139 ms                                                      | 102 ms: 1.36x faster                                                        |
| html5lib                 | 51.0 ms                                                     | 38.9 ms: 1.31x faster                                                       |
| mako                     | 9.03 ms                                                     | 6.96 ms: 1.30x faster                                                       |
| pyflate                  | 409 ms                                                      | 324 ms: 1.26x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 50.0 ms: 1.25x faster                                                       |
| comprehensions           | 16.5 us                                                     | 13.3 us: 1.24x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.1 ms: 1.22x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.73 sec: 1.22x faster                                                      |
| pycparser                | 930 ms                                                      | 767 ms: 1.21x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 23.8 us: 1.21x faster                                                       |
| django_template          | 28.9 ms                                                     | 24.2 ms: 1.19x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.51 sec: 1.18x faster                                                      |
| scimark_monte_carlo      | 57.3 ms                                                     | 48.7 ms: 1.18x faster                                                       |
| tomli_loads              | 1.67 sec                                                    | 1.43 sec: 1.17x faster                                                      |
| sqlite_synth             | 1.91 us                                                     | 1.64 us: 1.16x faster                                                       |
| regex_dna                | 136 ms                                                      | 118 ms: 1.16x faster                                                        |
| mypy2                    | 555 ms                                                      | 480 ms: 1.16x faster                                                        |
| unpickle_pure_python     | 183 us                                                      | 159 us: 1.15x faster                                                        |
| xml_etree_process        | 44.5 ms                                                     | 38.8 ms: 1.15x faster                                                       |
| scimark_sor              | 106 ms                                                      | 92.9 ms: 1.14x faster                                                       |
| tornado_http             | 108 ms                                                      | 94.8 ms: 1.14x faster                                                       |
| chameleon                | 5.79 ms                                                     | 5.08 ms: 1.14x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 1.07 sec: 1.14x faster                                                      |
| float                    | 61.7 ms                                                     | 54.5 ms: 1.13x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 523 ms: 1.13x faster                                                        |
| dulwich_log              | 50.5 ms                                                     | 44.9 ms: 1.13x faster                                                       |
| sympy_sum                | 107 ms                                                      | 95.6 ms: 1.12x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 17.8 ms: 1.11x faster                                                       |
| deepcopy                 | 255 us                                                      | 231 us: 1.11x faster                                                        |
| bench_thread_pool        | 958 us                                                      | 869 us: 1.10x faster                                                        |
| genshi_xml               | 41.0 ms                                                     | 37.3 ms: 1.10x faster                                                       |
| sympy_integrate          | 15.3 ms                                                     | 14.0 ms: 1.09x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 5.29 ms: 1.09x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 676 ms: 1.08x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 2.04 us: 1.08x faster                                                       |
| docutils                 | 1.92 sec                                                    | 1.79 sec: 1.07x faster                                                      |
| scimark_lu               | 85.8 ms                                                     | 80.8 ms: 1.06x faster                                                       |
| 2to3                     | 246 ms                                                      | 232 ms: 1.06x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 37.7 ms: 1.06x faster                                                       |
| sqlglot_normalize        | 205 ms                                                      | 195 ms: 1.05x faster                                                        |
| sympy_str                | 194 ms                                                      | 185 ms: 1.05x faster                                                        |
| regex_effbot             | 1.66 ms                                                     | 1.59 ms: 1.04x faster                                                       |
| spectral_norm            | 77.3 ms                                                     | 74.6 ms: 1.04x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 93.7 ms: 1.03x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.56 us: 1.03x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.83 us: 1.03x faster                                                       |
| sympy_expand             | 314 ms                                                      | 311 ms: 1.01x faster                                                        |
| aiohttp                  | 995 us                                                      | 986 us: 1.01x faster                                                        |
| python_startup           | 20.6 ms                                                     | 20.5 ms: 1.01x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 76.3 ms: 1.00x slower                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 57.3 ms: 1.03x slower                                                       |
| nbody                    | 71.3 ms                                                     | 74.3 ms: 1.04x slower                                                       |
| json_loads               | 14.0 us                                                     | 14.6 us: 1.04x slower                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 67.8 ms: 1.04x slower                                                       |
| fannkuch                 | 256 ms                                                      | 268 ms: 1.05x slower                                                        |
| unpickle_list            | 2.71 us                                                     | 2.85 us: 1.05x slower                                                       |
| nqueens                  | 66.6 ms                                                     | 70.7 ms: 1.06x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 16.7 ms: 1.08x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.97 us: 1.08x slower                                                       |
| scimark_fft              | 187 ms                                                      | 202 ms: 1.08x slower                                                        |
| pathlib                  | 75.7 ms                                                     | 82.3 ms: 1.09x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.45 us: 1.09x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 67.7 ms: 1.09x slower                                                       |
| coverage                 | 39.0 ms                                                     | 42.8 ms: 1.10x slower                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 3.02 ms: 1.11x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.58 ms: 1.12x slower                                                       |
| async_generators         | 222 ms                                                      | 251 ms: 1.13x slower                                                        |
| create_gc_cycles         | 800 us                                                      | 929 us: 1.16x slower                                                        |
| pickle_dict              | 17.2 us                                                     | 20.2 us: 1.18x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.95 ms: 1.26x slower                                                       |
| regex_v8                 | 15.4 ms                                                     | 20.0 ms: 1.29x slower                                                       |
| thrift                   | 617 us                                                      | 10.1 ms: 16.33x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (4): logging_simple, pidigits, regex_compile, json
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1-amd64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown
# Results vs. 3.10.4

- fork: faster-cpython
- ref: call_cmethod
- machine: windows-amd64
- commit hash: e985127
- commit date: 2024-04-10
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 212 ms: 1.16x faster                                                          |
| chameleon      | 5.79 ms                                                     | 4.84 ms: 1.19x faster                                                         |
| docutils       | 1.92 sec                                                    | 1.63 sec: 1.18x faster                                                        |
| html5lib       | 51.0 ms                                                     | 35.8 ms: 1.43x faster                                                         |
| tornado_http   | 108 ms                                                      | 81.8 ms: 1.32x faster                                                         |
| Geometric mean | (ref)                                                       | 1.25x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|-------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 269 ms: 1.96x faster                                                          |
| async_tree_none         | 435 ms                                                      | 223 ms: 1.95x faster                                                          |
| async_tree_io           | 1.11 sec                                                    | 592 ms: 1.87x faster                                                          |
| async_tree_cpu_io_mixed | 638 ms                                                      | 389 ms: 1.64x faster                                                          |
| Geometric mean          | (ref)                                                       | 1.85x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 52.0 ms: 1.19x faster                                                         |
| pidigits       | 149 ms                                                      | 147 ms: 1.01x faster                                                          |
| nbody          | 71.3 ms                                                     | 72.2 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 80.0 ms: 1.32x faster                                                         |
| regex_dna      | 136 ms                                                      | 115 ms: 1.19x faster                                                          |
| regex_effbot   | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                         |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                  |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.72 ms: 1.60x faster                                                         |
| pickle_pure_python   | 270 us                                                      | 180 us: 1.50x faster                                                          |
| unpickle_pure_python | 183 us                                                      | 132 us: 1.39x faster                                                          |
| tomli_loads          | 1.67 sec                                                    | 1.42 sec: 1.18x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 37.8 ms: 1.18x faster                                                         |
| unpickle             | 9.09 us                                                     | 8.40 us: 1.08x faster                                                         |
| xml_etree_parse      | 96.8 ms                                                     | 93.2 ms: 1.04x faster                                                         |
| xml_etree_generate   | 55.5 ms                                                     | 54.5 ms: 1.02x faster                                                         |
| json_loads           | 14.0 us                                                     | 13.9 us: 1.01x faster                                                         |
| unpickle_list        | 2.71 us                                                     | 2.79 us: 1.03x slower                                                         |
| pickle_list          | 2.75 us                                                     | 2.94 us: 1.07x slower                                                         |
| pickle               | 6.85 us                                                     | 7.36 us: 1.08x slower                                                         |
| pickle_dict          | 17.2 us                                                     | 18.6 us: 1.08x slower                                                         |
| Geometric mean       | (ref)                                                       | 1.11x faster                                                                  |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.9 ms: 1.04x faster                                                         |
| python_startup_no_site | 15.5 ms                                                     | 17.8 ms: 1.15x slower                                                         |
| Geometric mean         | (ref)                                                       | 1.05x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 6.39 ms: 1.41x faster                                                         |
| genshi_text    | 19.8 ms                                                     | 16.2 ms: 1.22x faster                                                         |
| genshi_xml     | 41.0 ms                                                     | 35.5 ms: 1.16x faster                                                         |
| Geometric mean | (ref)                                                       | 1.26x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|--------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 75.2 us: 4.47x faster                                                         |
| deltablue                | 4.19 ms                                                     | 1.97 ms: 2.12x faster                                                         |
| async_tree_memoization   | 526 ms                                                      | 269 ms: 1.96x faster                                                          |
| async_tree_none          | 435 ms                                                      | 223 ms: 1.95x faster                                                          |
| pylint                   | 350 ms                                                      | 187 ms: 1.88x faster                                                          |
| async_tree_io            | 1.11 sec                                                    | 592 ms: 1.87x faster                                                          |
| raytrace                 | 273 ms                                                      | 159 ms: 1.72x faster                                                          |
| logging_silent           | 94.6 ns                                                     | 56.8 ns: 1.67x faster                                                         |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 389 ms: 1.64x faster                                                          |
| richards_super           | 52.2 ms                                                     | 31.9 ms: 1.64x faster                                                         |
| go                       | 139 ms                                                      | 85.7 ms: 1.62x faster                                                         |
| json_dumps               | 9.16 ms                                                     | 5.72 ms: 1.60x faster                                                         |
| richards                 | 42.4 ms                                                     | 26.8 ms: 1.58x faster                                                         |
| chaos                    | 61.7 ms                                                     | 39.1 ms: 1.58x faster                                                         |
| sqlglot_parse            | 1.22 ms                                                     | 774 us: 1.57x faster                                                          |
| asyncio_tcp              | 732 ms                                                      | 473 ms: 1.55x faster                                                          |
| pickle_pure_python       | 270 us                                                      | 180 us: 1.50x faster                                                          |
| sqlglot_transpile        | 1.48 ms                                                     | 987 us: 1.49x faster                                                          |
| hexiom                   | 5.74 ms                                                     | 3.85 ms: 1.49x faster                                                         |
| scimark_lu               | 85.8 ms                                                     | 57.7 ms: 1.49x faster                                                         |
| comprehensions           | 16.5 us                                                     | 11.2 us: 1.48x faster                                                         |
| generators               | 32.4 ms                                                     | 22.2 ms: 1.46x faster                                                         |
| html5lib                 | 51.0 ms                                                     | 35.8 ms: 1.43x faster                                                         |
| pyflate                  | 409 ms                                                      | 289 ms: 1.42x faster                                                          |
| mako                     | 9.03 ms                                                     | 6.39 ms: 1.41x faster                                                         |
| scimark_monte_carlo      | 57.3 ms                                                     | 41.0 ms: 1.40x faster                                                         |
| unpickle_pure_python     | 183 us                                                      | 132 us: 1.39x faster                                                          |
| crypto_pyaes             | 62.5 ms                                                     | 46.1 ms: 1.36x faster                                                         |
| scimark_sor              | 106 ms                                                      | 78.7 ms: 1.35x faster                                                         |
| regex_compile            | 106 ms                                                      | 80.0 ms: 1.32x faster                                                         |
| tornado_http             | 108 ms                                                      | 81.8 ms: 1.32x faster                                                         |
| mypy2                    | 555 ms                                                      | 421 ms: 1.32x faster                                                          |
| deepcopy_memo            | 28.8 us                                                     | 22.1 us: 1.30x faster                                                         |
| pycparser                | 930 ms                                                      | 725 ms: 1.28x faster                                                          |
| mdp                      | 1.78 sec                                                    | 1.42 sec: 1.26x faster                                                        |
| dulwich_log              | 50.5 ms                                                     | 40.3 ms: 1.25x faster                                                         |
| sympy_sum                | 107 ms                                                      | 85.6 ms: 1.25x faster                                                         |
| coroutines               | 16.0 ms                                                     | 13.0 ms: 1.23x faster                                                         |
| pprint_pformat           | 1.22 sec                                                    | 997 ms: 1.22x faster                                                          |
| genshi_text              | 19.8 ms                                                     | 16.2 ms: 1.22x faster                                                         |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.74 sec: 1.21x faster                                                        |
| bench_thread_pool        | 958 us                                                      | 794 us: 1.21x faster                                                          |
| pprint_safe_repr         | 592 ms                                                      | 493 ms: 1.20x faster                                                          |
| sympy_integrate          | 15.3 ms                                                     | 12.8 ms: 1.20x faster                                                         |
| chameleon                | 5.79 ms                                                     | 4.84 ms: 1.19x faster                                                         |
| sqlite_synth             | 1.91 us                                                     | 1.60 us: 1.19x faster                                                         |
| spectral_norm            | 77.3 ms                                                     | 65.0 ms: 1.19x faster                                                         |
| float                    | 61.7 ms                                                     | 52.0 ms: 1.19x faster                                                         |
| regex_dna                | 136 ms                                                      | 115 ms: 1.19x faster                                                          |
| sympy_str                | 194 ms                                                      | 164 ms: 1.18x faster                                                          |
| docutils                 | 1.92 sec                                                    | 1.63 sec: 1.18x faster                                                        |
| tomli_loads              | 1.67 sec                                                    | 1.42 sec: 1.18x faster                                                        |
| xml_etree_process        | 44.5 ms                                                     | 37.8 ms: 1.18x faster                                                         |
| 2to3                     | 246 ms                                                      | 212 ms: 1.16x faster                                                          |
| genshi_xml               | 41.0 ms                                                     | 35.5 ms: 1.16x faster                                                         |
| sqlglot_optimize         | 39.8 ms                                                     | 34.8 ms: 1.14x faster                                                         |
| deepcopy                 | 255 us                                                      | 225 us: 1.13x faster                                                          |
| sympy_expand             | 314 ms                                                      | 278 ms: 1.13x faster                                                          |
| aiohttp                  | 995 us                                                      | 890 us: 1.12x faster                                                          |
| sqlglot_normalize        | 205 ms                                                      | 184 ms: 1.11x faster                                                          |
| unpickle                 | 9.09 us                                                     | 8.40 us: 1.08x faster                                                         |
| nqueens                  | 66.6 ms                                                     | 61.7 ms: 1.08x faster                                                         |
| deepcopy_reduce          | 2.20 us                                                     | 2.05 us: 1.08x faster                                                         |
| regex_effbot             | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                         |
| json                     | 3.14 ms                                                     | 2.95 ms: 1.06x faster                                                         |
| logging_format           | 6.76 us                                                     | 6.47 us: 1.04x faster                                                         |
| xml_etree_parse          | 96.8 ms                                                     | 93.2 ms: 1.04x faster                                                         |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.62 ms: 1.04x faster                                                         |
| python_startup           | 20.6 ms                                                     | 19.9 ms: 1.04x faster                                                         |
| meteor_contest           | 75.9 ms                                                     | 73.5 ms: 1.03x faster                                                         |
| logging_simple           | 6.22 us                                                     | 6.06 us: 1.03x faster                                                         |
| xml_etree_generate       | 55.5 ms                                                     | 54.5 ms: 1.02x faster                                                         |
| pidigits                 | 149 ms                                                      | 147 ms: 1.01x faster                                                          |
| fannkuch                 | 256 ms                                                      | 252 ms: 1.01x faster                                                          |
| json_loads               | 14.0 us                                                     | 13.9 us: 1.01x faster                                                         |
| scimark_fft              | 187 ms                                                      | 186 ms: 1.01x faster                                                          |
| nbody                    | 71.3 ms                                                     | 72.2 ms: 1.01x slower                                                         |
| unpickle_list            | 2.71 us                                                     | 2.79 us: 1.03x slower                                                         |
| bench_mp_pool            | 62.0 ms                                                     | 63.8 ms: 1.03x slower                                                         |
| async_generators         | 222 ms                                                      | 231 ms: 1.04x slower                                                          |
| pickle_list              | 2.75 us                                                     | 2.94 us: 1.07x slower                                                         |
| pickle                   | 6.85 us                                                     | 7.36 us: 1.08x slower                                                         |
| pickle_dict              | 17.2 us                                                     | 18.6 us: 1.08x slower                                                         |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.09x slower                                                         |
| create_gc_cycles         | 800 us                                                      | 881 us: 1.10x slower                                                          |
| python_startup_no_site   | 15.5 ms                                                     | 17.8 ms: 1.15x slower                                                         |
| coverage                 | 39.0 ms                                                     | 46.4 ms: 1.19x slower                                                         |
| telco                    | 3.94 ms                                                     | 5.02 ms: 1.27x slower                                                         |
| thrift                   | 617 us                                                      | 8.07 ms: 13.08x slower                                                        |
| Geometric mean           | (ref)                                                       | 1.20x faster                                                                  |

Benchmark hidden because not significant (3): pathlib, xml_etree_iterparse, regex_v8
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240410-3.13.0a5+-e985127/bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown
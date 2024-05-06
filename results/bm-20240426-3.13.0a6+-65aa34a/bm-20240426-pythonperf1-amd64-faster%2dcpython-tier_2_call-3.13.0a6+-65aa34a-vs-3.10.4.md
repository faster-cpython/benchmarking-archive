# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-amd64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 217 ms: 1.13x faster                                                         |
| chameleon      | 5.79 ms                                                     | 5.05 ms: 1.15x faster                                                        |
| docutils       | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                       |
| html5lib       | 51.0 ms                                                     | 36.5 ms: 1.40x faster                                                        |
| tornado_http   | 108 ms                                                      | 90.9 ms: 1.19x faster                                                        |
| Geometric mean | (ref)                                                       | 1.20x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 233 ms: 1.87x faster                                                         |
| async_tree_memoization  | 526 ms                                                      | 282 ms: 1.87x faster                                                         |
| async_tree_io           | 1.11 sec                                                    | 612 ms: 1.81x faster                                                         |
| async_tree_cpu_io_mixed | 638 ms                                                      | 402 ms: 1.59x faster                                                         |
| Geometric mean          | (ref)                                                       | 1.78x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 51.5 ms: 1.20x faster                                                        |
| nbody          | 71.3 ms                                                     | 72.9 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 79.4 ms: 1.34x faster                                                        |
| regex_dna      | 136 ms                                                      | 114 ms: 1.19x faster                                                         |
| regex_effbot   | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                        |
| regex_v8       | 15.4 ms                                                     | 14.6 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                       | 1.15x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.83 ms: 1.57x faster                                                        |
| pickle_pure_python   | 270 us                                                      | 176 us: 1.53x faster                                                         |
| unpickle_pure_python | 183 us                                                      | 133 us: 1.38x faster                                                         |
| xml_etree_process    | 44.5 ms                                                     | 37.6 ms: 1.18x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.45 sec: 1.16x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.57 us: 1.06x faster                                                        |
| xml_etree_parse      | 96.8 ms                                                     | 92.3 ms: 1.05x faster                                                        |
| json_loads           | 14.0 us                                                     | 13.7 us: 1.02x faster                                                        |
| xml_etree_generate   | 55.5 ms                                                     | 55.2 ms: 1.01x faster                                                        |
| unpickle_list        | 2.71 us                                                     | 2.78 us: 1.03x slower                                                        |
| pickle               | 6.85 us                                                     | 7.27 us: 1.06x slower                                                        |
| pickle_dict          | 17.2 us                                                     | 18.4 us: 1.07x slower                                                        |
| pickle_list          | 2.75 us                                                     | 3.11 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                       | 1.10x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 15.5 ms                                                     | 16.7 ms: 1.08x slower                                                        |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                                 |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.37 ms: 1.42x faster                                                        |
| django_template | 28.9 ms                                                     | 22.4 ms: 1.29x faster                                                        |
| genshi_text     | 19.8 ms                                                     | 16.2 ms: 1.22x faster                                                        |
| genshi_xml      | 41.0 ms                                                     | 34.4 ms: 1.19x faster                                                        |
| Geometric mean  | (ref)                                                       | 1.28x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:-----------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 109 us: 3.10x faster                                                         |
| deltablue                | 4.19 ms                                                     | 2.05 ms: 2.05x faster                                                        |
| async_tree_none          | 435 ms                                                      | 233 ms: 1.87x faster                                                         |
| async_tree_memoization   | 526 ms                                                      | 282 ms: 1.87x faster                                                         |
| async_tree_io            | 1.11 sec                                                    | 612 ms: 1.81x faster                                                         |
| logging_silent           | 94.6 ns                                                     | 54.9 ns: 1.73x faster                                                        |
| pylint                   | 350 ms                                                      | 212 ms: 1.65x faster                                                         |
| raytrace                 | 273 ms                                                      | 166 ms: 1.64x faster                                                         |
| richards_super           | 52.2 ms                                                     | 32.4 ms: 1.61x faster                                                        |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 402 ms: 1.59x faster                                                         |
| chaos                    | 61.7 ms                                                     | 39.1 ms: 1.58x faster                                                        |
| json_dumps               | 9.16 ms                                                     | 5.83 ms: 1.57x faster                                                        |
| sqlglot_parse            | 1.22 ms                                                     | 781 us: 1.56x faster                                                         |
| comprehensions           | 16.5 us                                                     | 10.7 us: 1.54x faster                                                        |
| go                       | 139 ms                                                      | 90.7 ms: 1.53x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 176 us: 1.53x faster                                                         |
| sqlglot_transpile        | 1.48 ms                                                     | 994 us: 1.48x faster                                                         |
| hexiom                   | 5.74 ms                                                     | 3.88 ms: 1.48x faster                                                        |
| richards                 | 42.4 ms                                                     | 28.7 ms: 1.48x faster                                                        |
| scimark_lu               | 85.8 ms                                                     | 58.1 ms: 1.48x faster                                                        |
| generators               | 32.4 ms                                                     | 22.3 ms: 1.45x faster                                                        |
| pyflate                  | 409 ms                                                      | 288 ms: 1.42x faster                                                         |
| mako                     | 9.03 ms                                                     | 6.37 ms: 1.42x faster                                                        |
| html5lib                 | 51.0 ms                                                     | 36.5 ms: 1.40x faster                                                        |
| unpickle_pure_python     | 183 us                                                      | 133 us: 1.38x faster                                                         |
| crypto_pyaes             | 62.5 ms                                                     | 45.4 ms: 1.38x faster                                                        |
| scimark_sor              | 106 ms                                                      | 77.7 ms: 1.37x faster                                                        |
| scimark_monte_carlo      | 57.3 ms                                                     | 42.8 ms: 1.34x faster                                                        |
| regex_compile            | 106 ms                                                      | 79.4 ms: 1.34x faster                                                        |
| mypy2                    | 555 ms                                                      | 428 ms: 1.30x faster                                                         |
| django_template          | 28.9 ms                                                     | 22.4 ms: 1.29x faster                                                        |
| dulwich_log              | 50.5 ms                                                     | 39.9 ms: 1.26x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 22.9 us: 1.26x faster                                                        |
| pycparser                | 930 ms                                                      | 740 ms: 1.26x faster                                                         |
| sympy_sum                | 107 ms                                                      | 85.7 ms: 1.25x faster                                                        |
| mdp                      | 1.78 sec                                                    | 1.43 sec: 1.25x faster                                                       |
| sympy_integrate          | 15.3 ms                                                     | 12.5 ms: 1.22x faster                                                        |
| genshi_text              | 19.8 ms                                                     | 16.2 ms: 1.22x faster                                                        |
| pprint_pformat           | 1.22 sec                                                    | 999 ms: 1.22x faster                                                         |
| coroutines               | 16.0 ms                                                     | 13.1 ms: 1.22x faster                                                        |
| pprint_safe_repr         | 592 ms                                                      | 492 ms: 1.20x faster                                                         |
| sympy_str                | 194 ms                                                      | 162 ms: 1.20x faster                                                         |
| float                    | 61.7 ms                                                     | 51.5 ms: 1.20x faster                                                        |
| genshi_xml               | 41.0 ms                                                     | 34.4 ms: 1.19x faster                                                        |
| tornado_http             | 108 ms                                                      | 90.9 ms: 1.19x faster                                                        |
| regex_dna                | 136 ms                                                      | 114 ms: 1.19x faster                                                         |
| xml_etree_process        | 44.5 ms                                                     | 37.6 ms: 1.18x faster                                                        |
| spectral_norm            | 77.3 ms                                                     | 65.5 ms: 1.18x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 34.2 ms: 1.16x faster                                                        |
| docutils                 | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                       |
| deepcopy                 | 255 us                                                      | 221 us: 1.16x faster                                                         |
| tomli_loads              | 1.67 sec                                                    | 1.45 sec: 1.16x faster                                                       |
| sympy_expand             | 314 ms                                                      | 274 ms: 1.15x faster                                                         |
| sqlite_synth             | 1.91 us                                                     | 1.67 us: 1.15x faster                                                        |
| chameleon                | 5.79 ms                                                     | 5.05 ms: 1.15x faster                                                        |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.84 sec: 1.15x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 843 us: 1.14x faster                                                         |
| sqlglot_normalize        | 205 ms                                                      | 181 ms: 1.13x faster                                                         |
| 2to3                     | 246 ms                                                      | 217 ms: 1.13x faster                                                         |
| asyncio_tcp              | 732 ms                                                      | 664 ms: 1.10x faster                                                         |
| nqueens                  | 66.6 ms                                                     | 60.6 ms: 1.10x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 2.05 us: 1.07x faster                                                        |
| aiohttp                  | 995 us                                                      | 933 us: 1.07x faster                                                         |
| unpickle                 | 9.09 us                                                     | 8.57 us: 1.06x faster                                                        |
| regex_effbot             | 1.66 ms                                                     | 1.57 ms: 1.06x faster                                                        |
| regex_v8                 | 15.4 ms                                                     | 14.6 ms: 1.06x faster                                                        |
| xml_etree_parse          | 96.8 ms                                                     | 92.3 ms: 1.05x faster                                                        |
| logging_format           | 6.76 us                                                     | 6.53 us: 1.03x faster                                                        |
| logging_simple           | 6.22 us                                                     | 6.05 us: 1.03x faster                                                        |
| json_loads               | 14.0 us                                                     | 13.7 us: 1.02x faster                                                        |
| meteor_contest           | 75.9 ms                                                     | 74.8 ms: 1.02x faster                                                        |
| xml_etree_generate       | 55.5 ms                                                     | 55.2 ms: 1.01x faster                                                        |
| fannkuch                 | 256 ms                                                      | 259 ms: 1.01x slower                                                         |
| nbody                    | 71.3 ms                                                     | 72.9 ms: 1.02x slower                                                        |
| unpickle_list            | 2.71 us                                                     | 2.78 us: 1.03x slower                                                        |
| scimark_fft              | 187 ms                                                      | 197 ms: 1.05x slower                                                         |
| bench_mp_pool            | 62.0 ms                                                     | 65.6 ms: 1.06x slower                                                        |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.88 ms: 1.06x slower                                                        |
| pickle                   | 6.85 us                                                     | 7.27 us: 1.06x slower                                                        |
| pickle_dict              | 17.2 us                                                     | 18.4 us: 1.07x slower                                                        |
| python_startup_no_site   | 15.5 ms                                                     | 16.7 ms: 1.08x slower                                                        |
| pathlib                  | 75.7 ms                                                     | 82.3 ms: 1.09x slower                                                        |
| async_generators         | 222 ms                                                      | 242 ms: 1.09x slower                                                         |
| gc_traversal             | 1.41 ms                                                     | 1.56 ms: 1.11x slower                                                        |
| create_gc_cycles         | 800 us                                                      | 901 us: 1.13x slower                                                         |
| pickle_list              | 2.75 us                                                     | 3.11 us: 1.13x slower                                                        |
| telco                    | 3.94 ms                                                     | 4.83 ms: 1.23x slower                                                        |
| coverage                 | 39.0 ms                                                     | 50.6 ms: 1.30x slower                                                        |
| thrift                   | 617 us                                                      | 8.42 ms: 13.64x slower                                                       |
| Geometric mean           | (ref)                                                       | 1.18x faster                                                                 |

Benchmark hidden because not significant (4): json, xml_etree_iterparse, pidigits, python_startup
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown
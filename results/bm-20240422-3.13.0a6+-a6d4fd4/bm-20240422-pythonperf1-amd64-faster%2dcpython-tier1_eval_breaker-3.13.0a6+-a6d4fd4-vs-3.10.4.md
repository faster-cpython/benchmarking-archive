# Results vs. 3.10.4

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-amd64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 213 ms: 1.16x faster                                                                |
| chameleon      | 5.79 ms                                                     | 4.97 ms: 1.16x faster                                                               |
| docutils       | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                              |
| html5lib       | 51.0 ms                                                     | 35.6 ms: 1.43x faster                                                               |
| tornado_http   | 108 ms                                                      | 81.8 ms: 1.32x faster                                                               |
| Geometric mean | (ref)                                                       | 1.24x faster                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 224 ms: 1.94x faster                                                                |
| async_tree_memoization  | 526 ms                                                      | 274 ms: 1.92x faster                                                                |
| async_tree_io           | 1.11 sec                                                    | 597 ms: 1.86x faster                                                                |
| async_tree_cpu_io_mixed | 638 ms                                                      | 394 ms: 1.62x faster                                                                |
| Geometric mean          | (ref)                                                       | 1.83x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 51.7 ms: 1.19x faster                                                               |
| nbody          | 71.3 ms                                                     | 69.8 ms: 1.02x faster                                                               |
| pidigits       | 149 ms                                                      | 147 ms: 1.01x faster                                                                |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 80.5 ms: 1.32x faster                                                               |
| regex_dna      | 136 ms                                                      | 121 ms: 1.12x faster                                                                |
| regex_effbot   | 1.66 ms                                                     | 1.61 ms: 1.03x faster                                                               |
| Geometric mean | (ref)                                                       | 1.10x faster                                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.66 ms: 1.62x faster                                                               |
| pickle_pure_python   | 270 us                                                      | 184 us: 1.46x faster                                                                |
| unpickle_pure_python | 183 us                                                      | 133 us: 1.38x faster                                                                |
| tomli_loads          | 1.67 sec                                                    | 1.40 sec: 1.20x faster                                                              |
| xml_etree_process    | 44.5 ms                                                     | 37.9 ms: 1.17x faster                                                               |
| xml_etree_parse      | 96.8 ms                                                     | 90.2 ms: 1.07x faster                                                               |
| unpickle             | 9.09 us                                                     | 8.49 us: 1.07x faster                                                               |
| json_loads           | 14.0 us                                                     | 13.8 us: 1.02x faster                                                               |
| xml_etree_iterparse  | 65.0 ms                                                     | 63.9 ms: 1.02x faster                                                               |
| xml_etree_generate   | 55.5 ms                                                     | 55.0 ms: 1.01x faster                                                               |
| unpickle_list        | 2.71 us                                                     | 2.76 us: 1.02x slower                                                               |
| pickle               | 6.85 us                                                     | 7.24 us: 1.06x slower                                                               |
| pickle_list          | 2.75 us                                                     | 2.92 us: 1.06x slower                                                               |
| pickle_dict          | 17.2 us                                                     | 18.8 us: 1.10x slower                                                               |
| Geometric mean       | (ref)                                                       | 1.11x faster                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.8 ms: 1.04x faster                                                               |
| python_startup_no_site | 15.5 ms                                                     | 16.3 ms: 1.05x slower                                                               |
| Geometric mean         | (ref)                                                       | 1.01x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.56 ms: 1.38x faster                                                               |
| django_template | 28.9 ms                                                     | 22.5 ms: 1.28x faster                                                               |
| genshi_text     | 19.8 ms                                                     | 15.8 ms: 1.26x faster                                                               |
| genshi_xml      | 41.0 ms                                                     | 33.6 ms: 1.22x faster                                                               |
| Geometric mean  | (ref)                                                       | 1.28x faster                                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|--------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 74.8 us: 4.49x faster                                                               |
| deltablue                | 4.19 ms                                                     | 2.00 ms: 2.09x faster                                                               |
| async_tree_none          | 435 ms                                                      | 224 ms: 1.94x faster                                                                |
| async_tree_memoization   | 526 ms                                                      | 274 ms: 1.92x faster                                                                |
| async_tree_io            | 1.11 sec                                                    | 597 ms: 1.86x faster                                                                |
| richards_super           | 52.2 ms                                                     | 30.5 ms: 1.71x faster                                                               |
| raytrace                 | 273 ms                                                      | 160 ms: 1.71x faster                                                                |
| logging_silent           | 94.6 ns                                                     | 56.4 ns: 1.68x faster                                                               |
| pylint                   | 350 ms                                                      | 209 ms: 1.68x faster                                                                |
| json_dumps               | 9.16 ms                                                     | 5.66 ms: 1.62x faster                                                               |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 394 ms: 1.62x faster                                                                |
| go                       | 139 ms                                                      | 86.1 ms: 1.61x faster                                                               |
| sqlglot_parse            | 1.22 ms                                                     | 760 us: 1.60x faster                                                                |
| richards                 | 42.4 ms                                                     | 26.7 ms: 1.59x faster                                                               |
| chaos                    | 61.7 ms                                                     | 39.0 ms: 1.58x faster                                                               |
| generators               | 32.4 ms                                                     | 21.0 ms: 1.54x faster                                                               |
| asyncio_tcp              | 732 ms                                                      | 480 ms: 1.52x faster                                                                |
| sqlglot_transpile        | 1.48 ms                                                     | 968 us: 1.52x faster                                                                |
| scimark_lu               | 85.8 ms                                                     | 57.9 ms: 1.48x faster                                                               |
| comprehensions           | 16.5 us                                                     | 11.2 us: 1.48x faster                                                               |
| hexiom                   | 5.74 ms                                                     | 3.90 ms: 1.47x faster                                                               |
| pickle_pure_python       | 270 us                                                      | 184 us: 1.46x faster                                                                |
| html5lib                 | 51.0 ms                                                     | 35.6 ms: 1.43x faster                                                               |
| pyflate                  | 409 ms                                                      | 295 ms: 1.39x faster                                                                |
| mako                     | 9.03 ms                                                     | 6.56 ms: 1.38x faster                                                               |
| unpickle_pure_python     | 183 us                                                      | 133 us: 1.38x faster                                                                |
| scimark_sor              | 106 ms                                                      | 77.5 ms: 1.37x faster                                                               |
| crypto_pyaes             | 62.5 ms                                                     | 46.2 ms: 1.35x faster                                                               |
| pycparser                | 930 ms                                                      | 696 ms: 1.34x faster                                                                |
| mdp                      | 1.78 sec                                                    | 1.34 sec: 1.33x faster                                                              |
| tornado_http             | 108 ms                                                      | 81.8 ms: 1.32x faster                                                               |
| regex_compile            | 106 ms                                                      | 80.5 ms: 1.32x faster                                                               |
| mypy2                    | 555 ms                                                      | 424 ms: 1.31x faster                                                                |
| scimark_monte_carlo      | 57.3 ms                                                     | 44.1 ms: 1.30x faster                                                               |
| django_template          | 28.9 ms                                                     | 22.5 ms: 1.28x faster                                                               |
| sympy_sum                | 107 ms                                                      | 85.0 ms: 1.26x faster                                                               |
| genshi_text              | 19.8 ms                                                     | 15.8 ms: 1.26x faster                                                               |
| deepcopy_memo            | 28.8 us                                                     | 23.0 us: 1.25x faster                                                               |
| dulwich_log              | 50.5 ms                                                     | 40.5 ms: 1.25x faster                                                               |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.70 sec: 1.24x faster                                                              |
| pprint_pformat           | 1.22 sec                                                    | 986 ms: 1.24x faster                                                                |
| genshi_xml               | 41.0 ms                                                     | 33.6 ms: 1.22x faster                                                               |
| pprint_safe_repr         | 592 ms                                                      | 486 ms: 1.22x faster                                                                |
| coroutines               | 16.0 ms                                                     | 13.2 ms: 1.21x faster                                                               |
| sympy_integrate          | 15.3 ms                                                     | 12.6 ms: 1.21x faster                                                               |
| spectral_norm            | 77.3 ms                                                     | 64.1 ms: 1.21x faster                                                               |
| tomli_loads              | 1.67 sec                                                    | 1.40 sec: 1.20x faster                                                              |
| float                    | 61.7 ms                                                     | 51.7 ms: 1.19x faster                                                               |
| bench_thread_pool        | 958 us                                                      | 810 us: 1.18x faster                                                                |
| sympy_str                | 194 ms                                                      | 165 ms: 1.18x faster                                                                |
| sqlglot_optimize         | 39.8 ms                                                     | 33.8 ms: 1.18x faster                                                               |
| xml_etree_process        | 44.5 ms                                                     | 37.9 ms: 1.17x faster                                                               |
| chameleon                | 5.79 ms                                                     | 4.97 ms: 1.16x faster                                                               |
| docutils                 | 1.92 sec                                                    | 1.65 sec: 1.16x faster                                                              |
| sqlglot_normalize        | 205 ms                                                      | 177 ms: 1.16x faster                                                                |
| 2to3                     | 246 ms                                                      | 213 ms: 1.16x faster                                                                |
| sqlite_synth             | 1.91 us                                                     | 1.66 us: 1.15x faster                                                               |
| deepcopy                 | 255 us                                                      | 223 us: 1.14x faster                                                                |
| aiohttp                  | 995 us                                                      | 882 us: 1.13x faster                                                                |
| regex_dna                | 136 ms                                                      | 121 ms: 1.12x faster                                                                |
| sympy_expand             | 314 ms                                                      | 281 ms: 1.12x faster                                                                |
| nqueens                  | 66.6 ms                                                     | 60.0 ms: 1.11x faster                                                               |
| json                     | 3.14 ms                                                     | 2.87 ms: 1.09x faster                                                               |
| deepcopy_reduce          | 2.20 us                                                     | 2.04 us: 1.08x faster                                                               |
| xml_etree_parse          | 96.8 ms                                                     | 90.2 ms: 1.07x faster                                                               |
| unpickle                 | 9.09 us                                                     | 8.49 us: 1.07x faster                                                               |
| logging_format           | 6.76 us                                                     | 6.35 us: 1.06x faster                                                               |
| logging_simple           | 6.22 us                                                     | 5.94 us: 1.05x faster                                                               |
| python_startup           | 20.6 ms                                                     | 19.8 ms: 1.04x faster                                                               |
| regex_effbot             | 1.66 ms                                                     | 1.61 ms: 1.03x faster                                                               |
| nbody                    | 71.3 ms                                                     | 69.8 ms: 1.02x faster                                                               |
| meteor_contest           | 75.9 ms                                                     | 74.3 ms: 1.02x faster                                                               |
| json_loads               | 14.0 us                                                     | 13.8 us: 1.02x faster                                                               |
| xml_etree_iterparse      | 65.0 ms                                                     | 63.9 ms: 1.02x faster                                                               |
| pidigits                 | 149 ms                                                      | 147 ms: 1.01x faster                                                                |
| xml_etree_generate       | 55.5 ms                                                     | 55.0 ms: 1.01x faster                                                               |
| scimark_fft              | 187 ms                                                      | 189 ms: 1.01x slower                                                                |
| pathlib                  | 75.7 ms                                                     | 76.5 ms: 1.01x slower                                                               |
| fannkuch                 | 256 ms                                                      | 259 ms: 1.01x slower                                                                |
| unpickle_list            | 2.71 us                                                     | 2.76 us: 1.02x slower                                                               |
| bench_mp_pool            | 62.0 ms                                                     | 64.0 ms: 1.03x slower                                                               |
| python_startup_no_site   | 15.5 ms                                                     | 16.3 ms: 1.05x slower                                                               |
| pickle                   | 6.85 us                                                     | 7.24 us: 1.06x slower                                                               |
| pickle_list              | 2.75 us                                                     | 2.92 us: 1.06x slower                                                               |
| async_generators         | 222 ms                                                      | 240 ms: 1.08x slower                                                                |
| pickle_dict              | 17.2 us                                                     | 18.8 us: 1.10x slower                                                               |
| gc_traversal             | 1.41 ms                                                     | 1.55 ms: 1.10x slower                                                               |
| create_gc_cycles         | 800 us                                                      | 888 us: 1.11x slower                                                                |
| coverage                 | 39.0 ms                                                     | 48.1 ms: 1.23x slower                                                               |
| telco                    | 3.94 ms                                                     | 5.18 ms: 1.31x slower                                                               |
| thrift                   | 617 us                                                      | 8.32 ms: 13.48x slower                                                              |
| Geometric mean           | (ref)                                                       | 1.20x faster                                                                        |

Benchmark hidden because not significant (2): scimark_sparse_mat_mult, regex_v8
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown
# Results vs. 3.10.4

- fork: python
- ref: 550483b7e6c54b2a25d4
- machine: windows-amd64
- commit hash: 550483b
- commit date: 2024-04-22
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 211 ms: 1.16x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.69 ms: 1.23x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.66 sec: 1.16x faster                                                      |
| html5lib       | 51.0 ms                                                     | 35.7 ms: 1.43x faster                                                       |
| tornado_http   | 108 ms                                                      | 81.7 ms: 1.33x faster                                                       |
| Geometric mean | (ref)                                                       | 1.26x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 273 ms: 1.93x faster                                                        |
| async_tree_none         | 435 ms                                                      | 226 ms: 1.93x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 597 ms: 1.86x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 394 ms: 1.62x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.83x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 51.9 ms: 1.19x faster                                                       |
| nbody          | 71.3 ms                                                     | 69.6 ms: 1.02x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 77.8 ms: 1.36x faster                                                       |
| regex_dna      | 136 ms                                                      | 115 ms: 1.18x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.56 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.15x faster                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.64 ms: 1.62x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 179 us: 1.51x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 128 us: 1.44x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.40 sec: 1.19x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 37.6 ms: 1.18x faster                                                       |
| unpickle             | 9.09 us                                                     | 8.24 us: 1.10x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 91.7 ms: 1.06x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.7 us: 1.02x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 63.6 ms: 1.02x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 55.0 ms: 1.01x faster                                                       |
| unpickle_list        | 2.71 us                                                     | 2.78 us: 1.02x slower                                                       |
| pickle               | 6.85 us                                                     | 7.17 us: 1.05x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.5 us: 1.08x slower                                                       |
| pickle_list          | 2.75 us                                                     | 3.06 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.12x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.7 ms: 1.05x faster                                                       |
| python_startup_no_site | 15.5 ms                                                     | 16.2 ms: 1.04x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.00x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 6.30 ms: 1.43x faster                                                       |
| django_template | 28.9 ms                                                     | 21.9 ms: 1.32x faster                                                       |
| genshi_text     | 19.8 ms                                                     | 15.8 ms: 1.25x faster                                                       |
| genshi_xml      | 41.0 ms                                                     | 33.8 ms: 1.21x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.30x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 74.1 us: 4.54x faster                                                       |
| deltablue                | 4.19 ms                                                     | 1.98 ms: 2.12x faster                                                       |
| async_tree_memoization   | 526 ms                                                      | 273 ms: 1.93x faster                                                        |
| async_tree_none          | 435 ms                                                      | 226 ms: 1.93x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 597 ms: 1.86x faster                                                        |
| raytrace                 | 273 ms                                                      | 161 ms: 1.70x faster                                                        |
| pylint                   | 350 ms                                                      | 207 ms: 1.69x faster                                                        |
| richards_super           | 52.2 ms                                                     | 31.5 ms: 1.66x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.64 ms: 1.62x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 394 ms: 1.62x faster                                                        |
| go                       | 139 ms                                                      | 86.3 ms: 1.61x faster                                                       |
| logging_silent           | 94.6 ns                                                     | 59.1 ns: 1.60x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 760 us: 1.60x faster                                                        |
| chaos                    | 61.7 ms                                                     | 38.7 ms: 1.60x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 477 ms: 1.54x faster                                                        |
| richards                 | 42.4 ms                                                     | 27.7 ms: 1.53x faster                                                       |
| comprehensions           | 16.5 us                                                     | 10.8 us: 1.52x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 56.5 ms: 1.52x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 972 us: 1.52x faster                                                        |
| pickle_pure_python       | 270 us                                                      | 179 us: 1.51x faster                                                        |
| hexiom                   | 5.74 ms                                                     | 3.84 ms: 1.50x faster                                                       |
| generators               | 32.4 ms                                                     | 22.1 ms: 1.47x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 128 us: 1.44x faster                                                        |
| mako                     | 9.03 ms                                                     | 6.30 ms: 1.43x faster                                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 40.0 ms: 1.43x faster                                                       |
| scimark_sor              | 106 ms                                                      | 74.2 ms: 1.43x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 35.7 ms: 1.43x faster                                                       |
| pyflate                  | 409 ms                                                      | 291 ms: 1.40x faster                                                        |
| crypto_pyaes             | 62.5 ms                                                     | 45.4 ms: 1.38x faster                                                       |
| regex_compile            | 106 ms                                                      | 77.8 ms: 1.36x faster                                                       |
| mypy2                    | 555 ms                                                      | 418 ms: 1.33x faster                                                        |
| deepcopy_memo            | 28.8 us                                                     | 21.7 us: 1.33x faster                                                       |
| tornado_http             | 108 ms                                                      | 81.7 ms: 1.33x faster                                                       |
| django_template          | 28.9 ms                                                     | 21.9 ms: 1.32x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 39.6 ms: 1.28x faster                                                       |
| sympy_sum                | 107 ms                                                      | 84.6 ms: 1.26x faster                                                       |
| pycparser                | 930 ms                                                      | 741 ms: 1.26x faster                                                        |
| genshi_text              | 19.8 ms                                                     | 15.8 ms: 1.25x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.69 ms: 1.23x faster                                                       |
| sympy_integrate          | 15.3 ms                                                     | 12.5 ms: 1.23x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 994 ms: 1.23x faster                                                        |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.73 sec: 1.22x faster                                                      |
| mdp                      | 1.78 sec                                                    | 1.46 sec: 1.22x faster                                                      |
| genshi_xml               | 41.0 ms                                                     | 33.8 ms: 1.21x faster                                                       |
| coroutines               | 16.0 ms                                                     | 13.2 ms: 1.21x faster                                                       |
| spectral_norm            | 77.3 ms                                                     | 63.8 ms: 1.21x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 489 ms: 1.21x faster                                                        |
| sympy_str                | 194 ms                                                      | 161 ms: 1.21x faster                                                        |
| tomli_loads              | 1.67 sec                                                    | 1.40 sec: 1.19x faster                                                      |
| float                    | 61.7 ms                                                     | 51.9 ms: 1.19x faster                                                       |
| sqlglot_optimize         | 39.8 ms                                                     | 33.6 ms: 1.19x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 810 us: 1.18x faster                                                        |
| xml_etree_process        | 44.5 ms                                                     | 37.6 ms: 1.18x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.62 us: 1.18x faster                                                       |
| regex_dna                | 136 ms                                                      | 115 ms: 1.18x faster                                                        |
| 2to3                     | 246 ms                                                      | 211 ms: 1.16x faster                                                        |
| docutils                 | 1.92 sec                                                    | 1.66 sec: 1.16x faster                                                      |
| deepcopy                 | 255 us                                                      | 222 us: 1.15x faster                                                        |
| sympy_expand             | 314 ms                                                      | 273 ms: 1.15x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 179 ms: 1.15x faster                                                        |
| aiohttp                  | 995 us                                                      | 874 us: 1.14x faster                                                        |
| nqueens                  | 66.6 ms                                                     | 58.5 ms: 1.14x faster                                                       |
| unpickle                 | 9.09 us                                                     | 8.24 us: 1.10x faster                                                       |
| deepcopy_reduce          | 2.20 us                                                     | 2.01 us: 1.10x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.56 ms: 1.07x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 91.7 ms: 1.06x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.41 us: 1.05x faster                                                       |
| python_startup           | 20.6 ms                                                     | 19.7 ms: 1.05x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.95 us: 1.04x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 73.0 ms: 1.04x faster                                                       |
| scimark_fft              | 187 ms                                                      | 182 ms: 1.03x faster                                                        |
| json_loads               | 14.0 us                                                     | 13.7 us: 1.02x faster                                                       |
| nbody                    | 71.3 ms                                                     | 69.6 ms: 1.02x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 63.6 ms: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.01x faster                                                        |
| xml_etree_generate       | 55.5 ms                                                     | 55.0 ms: 1.01x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.70 ms: 1.01x faster                                                       |
| pathlib                  | 75.7 ms                                                     | 76.5 ms: 1.01x slower                                                       |
| unpickle_list            | 2.71 us                                                     | 2.78 us: 1.02x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 63.7 ms: 1.03x slower                                                       |
| async_generators         | 222 ms                                                      | 230 ms: 1.04x slower                                                        |
| python_startup_no_site   | 15.5 ms                                                     | 16.2 ms: 1.04x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.17 us: 1.05x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.5 us: 1.08x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.10x slower                                                       |
| pickle_list              | 2.75 us                                                     | 3.06 us: 1.11x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 898 us: 1.12x slower                                                        |
| coverage                 | 39.0 ms                                                     | 46.0 ms: 1.18x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.89 ms: 1.24x slower                                                       |
| thrift                   | 617 us                                                      | 8.01 ms: 12.97x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.21x faster                                                                |

Benchmark hidden because not significant (3): json, regex_v8, fannkuch
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240422-3.13.0a6+-550483b/bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown
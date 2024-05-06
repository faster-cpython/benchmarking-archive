# Results vs. 3.10.4

- fork: python
- ref: v3.12.3
- machine: windows-amd64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 210 ms: 1.17x faster                                        |
| chameleon      | 5.79 ms                                                     | 4.94 ms: 1.17x faster                                       |
| docutils       | 1.92 sec                                                    | 1.61 sec: 1.19x faster                                      |
| html5lib       | 51.0 ms                                                     | 36.7 ms: 1.39x faster                                       |
| tornado_http   | 108 ms                                                      | 84.8 ms: 1.28x faster                                       |
| Geometric mean | (ref)                                                       | 1.24x faster                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|-------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 334 ms: 1.57x faster                                        |
| async_tree_io           | 1.11 sec                                                    | 726 ms: 1.53x faster                                        |
| async_tree_none         | 435 ms                                                      | 287 ms: 1.52x faster                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 475 ms: 1.34x faster                                        |
| Geometric mean          | (ref)                                                       | 1.49x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 61.7 ms                                                     | 55.1 ms: 1.12x faster                                       |
| pidigits       | 149 ms                                                      | 148 ms: 1.01x faster                                        |
| nbody          | 71.3 ms                                                     | 74.4 ms: 1.04x slower                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 87.1 ms: 1.22x faster                                       |
| regex_dna      | 136 ms                                                      | 121 ms: 1.13x faster                                        |
| regex_v8       | 15.4 ms                                                     | 13.8 ms: 1.12x faster                                       |
| regex_effbot   | 1.66 ms                                                     | 1.64 ms: 1.01x faster                                       |
| Geometric mean | (ref)                                                       | 1.12x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.62 ms: 1.63x faster                                       |
| pickle_pure_python   | 270 us                                                      | 192 us: 1.41x faster                                        |
| unpickle_pure_python | 183 us                                                      | 130 us: 1.40x faster                                        |
| tomli_loads          | 1.67 sec                                                    | 1.37 sec: 1.22x faster                                      |
| xml_etree_process    | 44.5 ms                                                     | 37.5 ms: 1.19x faster                                       |
| unpickle             | 9.09 us                                                     | 8.24 us: 1.10x faster                                       |
| xml_etree_parse      | 96.8 ms                                                     | 91.6 ms: 1.06x faster                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 63.0 ms: 1.03x faster                                       |
| json_loads           | 14.0 us                                                     | 13.7 us: 1.03x faster                                       |
| xml_etree_generate   | 55.5 ms                                                     | 56.1 ms: 1.01x slower                                       |
| unpickle_list        | 2.71 us                                                     | 2.82 us: 1.04x slower                                       |
| pickle               | 6.85 us                                                     | 7.33 us: 1.07x slower                                       |
| pickle_list          | 2.75 us                                                     | 2.95 us: 1.07x slower                                       |
| pickle_dict          | 17.2 us                                                     | 18.7 us: 1.09x slower                                       |
| Geometric mean       | (ref)                                                       | 1.11x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.1 ms: 1.08x faster                                       |
| python_startup_no_site | 15.5 ms                                                     | 16.0 ms: 1.03x slower                                       |
| Geometric mean         | (ref)                                                       | 1.02x faster                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| mako            | 9.03 ms                                                     | 7.10 ms: 1.27x faster                                       |
| django_template | 28.9 ms                                                     | 22.9 ms: 1.26x faster                                       |
| genshi_text     | 19.8 ms                                                     | 15.7 ms: 1.26x faster                                       |
| genshi_xml      | 41.0 ms                                                     | 33.5 ms: 1.22x faster                                       |
| Geometric mean  | (ref)                                                       | 1.25x faster                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|--------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 75.5 us: 4.45x faster                                       |
| deltablue                | 4.19 ms                                                     | 2.17 ms: 1.93x faster                                       |
| richards_super           | 52.2 ms                                                     | 30.0 ms: 1.74x faster                                       |
| pylint                   | 350 ms                                                      | 205 ms: 1.71x faster                                        |
| json_dumps               | 9.16 ms                                                     | 5.62 ms: 1.63x faster                                       |
| go                       | 139 ms                                                      | 86.4 ms: 1.61x faster                                       |
| richards                 | 42.4 ms                                                     | 26.4 ms: 1.61x faster                                       |
| async_tree_memoization   | 526 ms                                                      | 334 ms: 1.57x faster                                        |
| asyncio_tcp              | 732 ms                                                      | 474 ms: 1.54x faster                                        |
| scimark_lu               | 85.8 ms                                                     | 55.9 ms: 1.54x faster                                       |
| async_tree_io            | 1.11 sec                                                    | 726 ms: 1.53x faster                                        |
| comprehensions           | 16.5 us                                                     | 10.9 us: 1.52x faster                                       |
| async_tree_none          | 435 ms                                                      | 287 ms: 1.52x faster                                        |
| logging_silent           | 94.6 ns                                                     | 62.6 ns: 1.51x faster                                       |
| sqlglot_parse            | 1.22 ms                                                     | 811 us: 1.50x faster                                        |
| sqlglot_transpile        | 1.48 ms                                                     | 1.02 ms: 1.44x faster                                       |
| chaos                    | 61.7 ms                                                     | 42.9 ms: 1.44x faster                                       |
| hexiom                   | 5.74 ms                                                     | 4.01 ms: 1.43x faster                                       |
| raytrace                 | 273 ms                                                      | 191 ms: 1.43x faster                                        |
| pickle_pure_python       | 270 us                                                      | 192 us: 1.41x faster                                        |
| unpickle_pure_python     | 183 us                                                      | 130 us: 1.40x faster                                        |
| html5lib                 | 51.0 ms                                                     | 36.7 ms: 1.39x faster                                       |
| pyflate                  | 409 ms                                                      | 295 ms: 1.38x faster                                        |
| scimark_sor              | 106 ms                                                      | 76.9 ms: 1.38x faster                                       |
| generators               | 32.4 ms                                                     | 23.5 ms: 1.38x faster                                       |
| scimark_monte_carlo      | 57.3 ms                                                     | 41.9 ms: 1.37x faster                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 475 ms: 1.34x faster                                        |
| mdp                      | 1.78 sec                                                    | 1.34 sec: 1.32x faster                                      |
| crypto_pyaes             | 62.5 ms                                                     | 47.4 ms: 1.32x faster                                       |
| tornado_http             | 108 ms                                                      | 84.8 ms: 1.28x faster                                       |
| mako                     | 9.03 ms                                                     | 7.10 ms: 1.27x faster                                       |
| sympy_sum                | 107 ms                                                      | 84.5 ms: 1.27x faster                                       |
| django_template          | 28.9 ms                                                     | 22.9 ms: 1.26x faster                                       |
| pycparser                | 930 ms                                                      | 739 ms: 1.26x faster                                        |
| genshi_text              | 19.8 ms                                                     | 15.7 ms: 1.26x faster                                       |
| sqlalchemy_imperative    | 11.4 ms                                                     | 9.11 ms: 1.25x faster                                       |
| deepcopy_memo            | 28.8 us                                                     | 23.2 us: 1.24x faster                                       |
| sqlalchemy_declarative   | 103 ms                                                      | 83.6 ms: 1.24x faster                                       |
| sympy_integrate          | 15.3 ms                                                     | 12.4 ms: 1.23x faster                                       |
| dask                     | 313 ms                                                      | 255 ms: 1.22x faster                                        |
| genshi_xml               | 41.0 ms                                                     | 33.5 ms: 1.22x faster                                       |
| tomli_loads              | 1.67 sec                                                    | 1.37 sec: 1.22x faster                                      |
| regex_compile            | 106 ms                                                      | 87.1 ms: 1.22x faster                                       |
| spectral_norm            | 77.3 ms                                                     | 63.8 ms: 1.21x faster                                       |
| thrift                   | 617 us                                                      | 511 us: 1.21x faster                                        |
| docutils                 | 1.92 sec                                                    | 1.61 sec: 1.19x faster                                      |
| xml_etree_process        | 44.5 ms                                                     | 37.5 ms: 1.19x faster                                       |
| pprint_pformat           | 1.22 sec                                                    | 1.03 sec: 1.19x faster                                      |
| sympy_str                | 194 ms                                                      | 164 ms: 1.18x faster                                        |
| dulwich_log              | 50.5 ms                                                     | 42.7 ms: 1.18x faster                                       |
| sqlglot_optimize         | 39.8 ms                                                     | 33.7 ms: 1.18x faster                                       |
| aiohttp                  | 995 us                                                      | 847 us: 1.17x faster                                        |
| bench_thread_pool        | 958 us                                                      | 817 us: 1.17x faster                                        |
| pprint_safe_repr         | 592 ms                                                      | 505 ms: 1.17x faster                                        |
| chameleon                | 5.79 ms                                                     | 4.94 ms: 1.17x faster                                       |
| 2to3                     | 246 ms                                                      | 210 ms: 1.17x faster                                        |
| coroutines               | 16.0 ms                                                     | 13.9 ms: 1.15x faster                                       |
| sqlglot_normalize        | 205 ms                                                      | 181 ms: 1.13x faster                                        |
| regex_dna                | 136 ms                                                      | 121 ms: 1.13x faster                                        |
| mypy2                    | 555 ms                                                      | 494 ms: 1.12x faster                                        |
| deepcopy                 | 255 us                                                      | 228 us: 1.12x faster                                        |
| regex_v8                 | 15.4 ms                                                     | 13.8 ms: 1.12x faster                                       |
| sympy_expand             | 314 ms                                                      | 281 ms: 1.12x faster                                        |
| float                    | 61.7 ms                                                     | 55.1 ms: 1.12x faster                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.89 sec: 1.12x faster                                      |
| unpickle                 | 9.09 us                                                     | 8.24 us: 1.10x faster                                       |
| create_gc_cycles         | 800 us                                                      | 733 us: 1.09x faster                                        |
| deepcopy_reduce          | 2.20 us                                                     | 2.02 us: 1.09x faster                                       |
| sqlite_synth             | 1.91 us                                                     | 1.76 us: 1.08x faster                                       |
| python_startup           | 20.6 ms                                                     | 19.1 ms: 1.08x faster                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.52 ms: 1.08x faster                                       |
| nqueens                  | 66.6 ms                                                     | 61.9 ms: 1.08x faster                                       |
| fannkuch                 | 256 ms                                                      | 238 ms: 1.07x faster                                        |
| scimark_fft              | 187 ms                                                      | 175 ms: 1.07x faster                                        |
| xml_etree_parse          | 96.8 ms                                                     | 91.6 ms: 1.06x faster                                       |
| meteor_contest           | 75.9 ms                                                     | 72.1 ms: 1.05x faster                                       |
| json                     | 3.14 ms                                                     | 2.98 ms: 1.05x faster                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 63.0 ms: 1.03x faster                                       |
| coverage                 | 39.0 ms                                                     | 38.0 ms: 1.03x faster                                       |
| json_loads               | 14.0 us                                                     | 13.7 us: 1.03x faster                                       |
| pidigits                 | 149 ms                                                      | 148 ms: 1.01x faster                                        |
| telco                    | 3.94 ms                                                     | 3.90 ms: 1.01x faster                                       |
| regex_effbot             | 1.66 ms                                                     | 1.64 ms: 1.01x faster                                       |
| xml_etree_generate       | 55.5 ms                                                     | 56.1 ms: 1.01x slower                                       |
| logging_simple           | 6.22 us                                                     | 6.34 us: 1.02x slower                                       |
| python_startup_no_site   | 15.5 ms                                                     | 16.0 ms: 1.03x slower                                       |
| async_generators         | 222 ms                                                      | 230 ms: 1.04x slower                                        |
| unpickle_list            | 2.71 us                                                     | 2.82 us: 1.04x slower                                       |
| nbody                    | 71.3 ms                                                     | 74.4 ms: 1.04x slower                                       |
| bench_mp_pool            | 62.0 ms                                                     | 65.6 ms: 1.06x slower                                       |
| gc_traversal             | 1.41 ms                                                     | 1.50 ms: 1.06x slower                                       |
| pickle                   | 6.85 us                                                     | 7.33 us: 1.07x slower                                       |
| pickle_list              | 2.75 us                                                     | 2.95 us: 1.07x slower                                       |
| pickle_dict              | 17.2 us                                                     | 18.7 us: 1.09x slower                                       |
| Geometric mean           | (ref)                                                       | 1.22x faster                                                |

Benchmark hidden because not significant (2): logging_format, pathlib
Ignored benchmarks (2) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, unpack_sequence
Ignored benchmarks (4) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown
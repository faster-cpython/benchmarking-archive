# Results vs. 3.10.4

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 221 ms: 1.11x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.70 ms: 1.23x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.70 sec: 1.13x faster                                                      |
| html5lib       | 51.0 ms                                                     | 35.4 ms: 1.44x faster                                                       |
| tornado_http   | 108 ms                                                      | 83.6 ms: 1.30x faster                                                       |
| Geometric mean | (ref)                                                       | 1.24x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none         | 435 ms                                                      | 217 ms: 2.00x faster                                                        |
| async_tree_memoization  | 526 ms                                                      | 265 ms: 1.99x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 582 ms: 1.90x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 387 ms: 1.65x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.88x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 46.8 ms: 1.32x faster                                                       |
| nbody          | 71.3 ms                                                     | 57.8 ms: 1.23x faster                                                       |
| pidigits       | 149 ms                                                      | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.18x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 87.0 ms: 1.22x faster                                                       |
| regex_dna      | 136 ms                                                      | 119 ms: 1.14x faster                                                        |
| regex_v8       | 15.4 ms                                                     | 14.1 ms: 1.09x faster                                                       |
| regex_effbot   | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.54 ms: 1.65x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 172 us: 1.57x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 129 us: 1.42x faster                                                        |
| tomli_loads          | 1.67 sec                                                    | 1.19 sec: 1.41x faster                                                      |
| xml_etree_process    | 44.5 ms                                                     | 36.6 ms: 1.22x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 60.6 ms: 1.07x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 90.9 ms: 1.07x faster                                                       |
| xml_etree_generate   | 55.5 ms                                                     | 53.1 ms: 1.05x faster                                                       |
| json_loads           | 14.0 us                                                     | 13.7 us: 1.02x faster                                                       |
| pickle_list          | 2.75 us                                                     | 2.85 us: 1.04x slower                                                       |
| unpickle_list        | 2.71 us                                                     | 2.90 us: 1.07x slower                                                       |
| pickle               | 6.85 us                                                     | 7.39 us: 1.08x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 19.0 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.13x faster                                                                |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 22.2 ms: 1.08x slower                                                       |
| python_startup_no_site | 15.5 ms                                                     | 20.2 ms: 1.30x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.18x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 5.63 ms: 1.60x faster                                                       |
| genshi_text    | 19.8 ms                                                     | 15.6 ms: 1.27x faster                                                       |
| genshi_xml     | 41.0 ms                                                     | 34.8 ms: 1.18x faster                                                       |
| Geometric mean | (ref)                                                       | 1.34x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 72.5 us: 4.64x faster                                                       |
| async_tree_none          | 435 ms                                                      | 217 ms: 2.00x faster                                                        |
| async_tree_memoization   | 526 ms                                                      | 265 ms: 1.99x faster                                                        |
| deltablue                | 4.19 ms                                                     | 2.15 ms: 1.95x faster                                                       |
| async_tree_io            | 1.11 sec                                                    | 582 ms: 1.90x faster                                                        |
| pylint                   | 350 ms                                                      | 194 ms: 1.81x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 53.6 ns: 1.77x faster                                                       |
| richards_super           | 52.2 ms                                                     | 30.1 ms: 1.74x faster                                                       |
| raytrace                 | 273 ms                                                      | 164 ms: 1.66x faster                                                        |
| json_dumps               | 9.16 ms                                                     | 5.54 ms: 1.65x faster                                                       |
| generators               | 32.4 ms                                                     | 19.6 ms: 1.65x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 387 ms: 1.65x faster                                                        |
| mako                     | 9.03 ms                                                     | 5.63 ms: 1.60x faster                                                       |
| chaos                    | 61.7 ms                                                     | 38.5 ms: 1.60x faster                                                       |
| richards                 | 42.4 ms                                                     | 26.5 ms: 1.60x faster                                                       |
| pickle_pure_python       | 270 us                                                      | 172 us: 1.57x faster                                                        |
| sqlglot_parse            | 1.22 ms                                                     | 785 us: 1.55x faster                                                        |
| spectral_norm            | 77.3 ms                                                     | 50.4 ms: 1.53x faster                                                       |
| pyflate                  | 409 ms                                                      | 268 ms: 1.52x faster                                                        |
| asyncio_tcp              | 732 ms                                                      | 482 ms: 1.52x faster                                                        |
| comprehensions           | 16.5 us                                                     | 10.9 us: 1.52x faster                                                       |
| go                       | 139 ms                                                      | 92.0 ms: 1.51x faster                                                       |
| sqlglot_transpile        | 1.48 ms                                                     | 994 us: 1.48x faster                                                        |
| scimark_monte_carlo      | 57.3 ms                                                     | 38.7 ms: 1.48x faster                                                       |
| html5lib                 | 51.0 ms                                                     | 35.4 ms: 1.44x faster                                                       |
| crypto_pyaes             | 62.5 ms                                                     | 43.6 ms: 1.44x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 129 us: 1.42x faster                                                        |
| tomli_loads              | 1.67 sec                                                    | 1.19 sec: 1.41x faster                                                      |
| deepcopy_memo            | 28.8 us                                                     | 21.0 us: 1.37x faster                                                       |
| pycparser                | 930 ms                                                      | 687 ms: 1.35x faster                                                        |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.58 sec: 1.33x faster                                                      |
| float                    | 61.7 ms                                                     | 46.8 ms: 1.32x faster                                                       |
| tornado_http             | 108 ms                                                      | 83.6 ms: 1.30x faster                                                       |
| hexiom                   | 5.74 ms                                                     | 4.45 ms: 1.29x faster                                                       |
| scimark_sor              | 106 ms                                                      | 83.4 ms: 1.27x faster                                                       |
| genshi_text              | 19.8 ms                                                     | 15.6 ms: 1.27x faster                                                       |
| dulwich_log              | 50.5 ms                                                     | 40.4 ms: 1.25x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 979 ms: 1.25x faster                                                        |
| mypy2                    | 555 ms                                                      | 449 ms: 1.24x faster                                                        |
| nbody                    | 71.3 ms                                                     | 57.8 ms: 1.23x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.70 ms: 1.23x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 481 ms: 1.23x faster                                                        |
| coroutines               | 16.0 ms                                                     | 13.0 ms: 1.23x faster                                                       |
| regex_compile            | 106 ms                                                      | 87.0 ms: 1.22x faster                                                       |
| xml_etree_process        | 44.5 ms                                                     | 36.6 ms: 1.22x faster                                                       |
| sympy_sum                | 107 ms                                                      | 88.0 ms: 1.22x faster                                                       |
| mdp                      | 1.78 sec                                                    | 1.47 sec: 1.21x faster                                                      |
| bench_thread_pool        | 958 us                                                      | 795 us: 1.20x faster                                                        |
| sqlite_synth             | 1.91 us                                                     | 1.59 us: 1.20x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.30 ms: 1.18x faster                                                       |
| genshi_xml               | 41.0 ms                                                     | 34.8 ms: 1.18x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 73.2 ms: 1.17x faster                                                       |
| deepcopy                 | 255 us                                                      | 219 us: 1.17x faster                                                        |
| sympy_str                | 194 ms                                                      | 168 ms: 1.16x faster                                                        |
| sympy_integrate          | 15.3 ms                                                     | 13.3 ms: 1.15x faster                                                       |
| regex_dna                | 136 ms                                                      | 119 ms: 1.14x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 180 ms: 1.14x faster                                                        |
| sqlglot_optimize         | 39.8 ms                                                     | 35.0 ms: 1.14x faster                                                       |
| docutils                 | 1.92 sec                                                    | 1.70 sec: 1.13x faster                                                      |
| deepcopy_reduce          | 2.20 us                                                     | 1.95 us: 1.13x faster                                                       |
| 2to3                     | 246 ms                                                      | 221 ms: 1.11x faster                                                        |
| scimark_fft              | 187 ms                                                      | 169 ms: 1.11x faster                                                        |
| fannkuch                 | 256 ms                                                      | 231 ms: 1.11x faster                                                        |
| logging_format           | 6.76 us                                                     | 6.11 us: 1.11x faster                                                       |
| aiohttp                  | 995 us                                                      | 900 us: 1.11x faster                                                        |
| sympy_expand             | 314 ms                                                      | 285 ms: 1.10x faster                                                        |
| regex_v8                 | 15.4 ms                                                     | 14.1 ms: 1.09x faster                                                       |
| logging_simple           | 6.22 us                                                     | 5.72 us: 1.09x faster                                                       |
| json                     | 3.14 ms                                                     | 2.89 ms: 1.09x faster                                                       |
| nqueens                  | 66.6 ms                                                     | 61.5 ms: 1.08x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 60.6 ms: 1.07x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.55 ms: 1.07x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 90.9 ms: 1.07x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 72.5 ms: 1.05x faster                                                       |
| xml_etree_generate       | 55.5 ms                                                     | 53.1 ms: 1.05x faster                                                       |
| json_loads               | 14.0 us                                                     | 13.7 us: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 146 ms: 1.02x faster                                                        |
| pathlib                  | 75.7 ms                                                     | 76.8 ms: 1.01x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.85 us: 1.04x slower                                                       |
| async_generators         | 222 ms                                                      | 235 ms: 1.06x slower                                                        |
| unpickle_list            | 2.71 us                                                     | 2.90 us: 1.07x slower                                                       |
| python_startup           | 20.6 ms                                                     | 22.2 ms: 1.08x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.39 us: 1.08x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.54 ms: 1.09x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 19.0 us: 1.11x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 900 us: 1.13x slower                                                        |
| bench_mp_pool            | 62.0 ms                                                     | 69.9 ms: 1.13x slower                                                       |
| telco                    | 3.94 ms                                                     | 4.74 ms: 1.20x slower                                                       |
| coverage                 | 39.0 ms                                                     | 47.2 ms: 1.21x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 20.2 ms: 1.30x slower                                                       |
| thrift                   | 617 us                                                      | 8.54 ms: 13.84x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.22x faster                                                                |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240406-3.13.0a5+-62aeb0e-JIT/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown
# Results vs. 3.10.4

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                      | 213 ms: 1.15x faster                                                        |
| chameleon      | 5.79 ms                                                     | 4.93 ms: 1.17x faster                                                       |
| docutils       | 1.92 sec                                                    | 1.64 sec: 1.17x faster                                                      |
| html5lib       | 51.0 ms                                                     | 37.3 ms: 1.37x faster                                                       |
| tornado_http   | 108 ms                                                      | 83.5 ms: 1.30x faster                                                       |
| Geometric mean | (ref)                                                       | 1.23x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|-------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization  | 526 ms                                                      | 272 ms: 1.93x faster                                                        |
| async_tree_none         | 435 ms                                                      | 227 ms: 1.92x faster                                                        |
| async_tree_io           | 1.11 sec                                                    | 582 ms: 1.91x faster                                                        |
| async_tree_cpu_io_mixed | 638 ms                                                      | 393 ms: 1.62x faster                                                        |
| Geometric mean          | (ref)                                                       | 1.84x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 61.7 ms                                                     | 51.7 ms: 1.19x faster                                                       |
| nbody          | 71.3 ms                                                     | 69.8 ms: 1.02x faster                                                       |
| pidigits       | 149 ms                                                      | 147 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 106 ms                                                      | 78.5 ms: 1.35x faster                                                       |
| regex_dna      | 136 ms                                                      | 118 ms: 1.15x faster                                                        |
| regex_effbot   | 1.66 ms                                                     | 1.58 ms: 1.05x faster                                                       |
| Geometric mean | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 9.16 ms                                                     | 5.73 ms: 1.60x faster                                                       |
| pickle_pure_python   | 270 us                                                      | 179 us: 1.51x faster                                                        |
| unpickle_pure_python | 183 us                                                      | 134 us: 1.37x faster                                                        |
| xml_etree_process    | 44.5 ms                                                     | 37.9 ms: 1.17x faster                                                       |
| tomli_loads          | 1.67 sec                                                    | 1.45 sec: 1.16x faster                                                      |
| unpickle             | 9.09 us                                                     | 8.58 us: 1.06x faster                                                       |
| xml_etree_parse      | 96.8 ms                                                     | 93.2 ms: 1.04x faster                                                       |
| xml_etree_iterparse  | 65.0 ms                                                     | 63.4 ms: 1.02x faster                                                       |
| unpickle_list        | 2.71 us                                                     | 2.83 us: 1.04x slower                                                       |
| pickle               | 6.85 us                                                     | 7.21 us: 1.05x slower                                                       |
| pickle_list          | 2.75 us                                                     | 2.97 us: 1.08x slower                                                       |
| pickle_dict          | 17.2 us                                                     | 18.7 us: 1.09x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.6 ms                                                     | 19.8 ms: 1.04x faster                                                       |
| python_startup_no_site | 15.5 ms                                                     | 18.4 ms: 1.19x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.07x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 9.03 ms                                                     | 6.38 ms: 1.42x faster                                                       |
| genshi_text    | 19.8 ms                                                     | 16.8 ms: 1.18x faster                                                       |
| genshi_xml     | 41.0 ms                                                     | 36.1 ms: 1.14x faster                                                       |
| Geometric mean | (ref)                                                       | 1.24x faster                                                                |

All benchmarks:
===============

| Benchmark                | bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|--------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 336 us                                                      | 71.4 us: 4.71x faster                                                       |
| deltablue                | 4.19 ms                                                     | 2.07 ms: 2.02x faster                                                       |
| async_tree_memoization   | 526 ms                                                      | 272 ms: 1.93x faster                                                        |
| async_tree_none          | 435 ms                                                      | 227 ms: 1.92x faster                                                        |
| async_tree_io            | 1.11 sec                                                    | 582 ms: 1.91x faster                                                        |
| pylint                   | 350 ms                                                      | 187 ms: 1.87x faster                                                        |
| logging_silent           | 94.6 ns                                                     | 56.1 ns: 1.69x faster                                                       |
| raytrace                 | 273 ms                                                      | 164 ms: 1.67x faster                                                        |
| richards_super           | 52.2 ms                                                     | 32.0 ms: 1.63x faster                                                       |
| async_tree_cpu_io_mixed  | 638 ms                                                      | 393 ms: 1.62x faster                                                        |
| chaos                    | 61.7 ms                                                     | 38.5 ms: 1.60x faster                                                       |
| json_dumps               | 9.16 ms                                                     | 5.73 ms: 1.60x faster                                                       |
| scimark_lu               | 85.8 ms                                                     | 54.1 ms: 1.59x faster                                                       |
| sqlglot_parse            | 1.22 ms                                                     | 776 us: 1.57x faster                                                        |
| generators               | 32.4 ms                                                     | 20.9 ms: 1.55x faster                                                       |
| go                       | 139 ms                                                      | 90.9 ms: 1.53x faster                                                       |
| asyncio_tcp              | 732 ms                                                      | 483 ms: 1.52x faster                                                        |
| hexiom                   | 5.74 ms                                                     | 3.79 ms: 1.51x faster                                                       |
| comprehensions           | 16.5 us                                                     | 10.9 us: 1.51x faster                                                       |
| pickle_pure_python       | 270 us                                                      | 179 us: 1.51x faster                                                        |
| sqlglot_transpile        | 1.48 ms                                                     | 988 us: 1.49x faster                                                        |
| scimark_sor              | 106 ms                                                      | 72.5 ms: 1.46x faster                                                       |
| pyflate                  | 409 ms                                                      | 286 ms: 1.43x faster                                                        |
| scimark_monte_carlo      | 57.3 ms                                                     | 40.3 ms: 1.42x faster                                                       |
| richards                 | 42.4 ms                                                     | 29.8 ms: 1.42x faster                                                       |
| mako                     | 9.03 ms                                                     | 6.38 ms: 1.42x faster                                                       |
| crypto_pyaes             | 62.5 ms                                                     | 45.5 ms: 1.37x faster                                                       |
| pycparser                | 930 ms                                                      | 677 ms: 1.37x faster                                                        |
| html5lib                 | 51.0 ms                                                     | 37.3 ms: 1.37x faster                                                       |
| unpickle_pure_python     | 183 us                                                      | 134 us: 1.37x faster                                                        |
| regex_compile            | 106 ms                                                      | 78.5 ms: 1.35x faster                                                       |
| deepcopy_memo            | 28.8 us                                                     | 21.6 us: 1.33x faster                                                       |
| mypy2                    | 555 ms                                                      | 426 ms: 1.30x faster                                                        |
| tornado_http             | 108 ms                                                      | 83.5 ms: 1.30x faster                                                       |
| asyncio_tcp_ssl          | 2.11 sec                                                    | 1.64 sec: 1.28x faster                                                      |
| mdp                      | 1.78 sec                                                    | 1.41 sec: 1.26x faster                                                      |
| dulwich_log              | 50.5 ms                                                     | 40.1 ms: 1.26x faster                                                       |
| sympy_sum                | 107 ms                                                      | 85.8 ms: 1.25x faster                                                       |
| pprint_pformat           | 1.22 sec                                                    | 989 ms: 1.23x faster                                                        |
| spectral_norm            | 77.3 ms                                                     | 63.0 ms: 1.23x faster                                                       |
| sympy_integrate          | 15.3 ms                                                     | 12.6 ms: 1.22x faster                                                       |
| pprint_safe_repr         | 592 ms                                                      | 488 ms: 1.21x faster                                                        |
| coroutines               | 16.0 ms                                                     | 13.3 ms: 1.20x faster                                                       |
| float                    | 61.7 ms                                                     | 51.7 ms: 1.19x faster                                                       |
| sqlite_synth             | 1.91 us                                                     | 1.61 us: 1.19x faster                                                       |
| bench_thread_pool        | 958 us                                                      | 809 us: 1.18x faster                                                        |
| genshi_text              | 19.8 ms                                                     | 16.8 ms: 1.18x faster                                                       |
| sympy_str                | 194 ms                                                      | 165 ms: 1.18x faster                                                        |
| xml_etree_process        | 44.5 ms                                                     | 37.9 ms: 1.17x faster                                                       |
| chameleon                | 5.79 ms                                                     | 4.93 ms: 1.17x faster                                                       |
| docutils                 | 1.92 sec                                                    | 1.64 sec: 1.17x faster                                                      |
| deepcopy                 | 255 us                                                      | 221 us: 1.16x faster                                                        |
| tomli_loads              | 1.67 sec                                                    | 1.45 sec: 1.16x faster                                                      |
| sqlglot_optimize         | 39.8 ms                                                     | 34.5 ms: 1.15x faster                                                       |
| 2to3                     | 246 ms                                                      | 213 ms: 1.15x faster                                                        |
| regex_dna                | 136 ms                                                      | 118 ms: 1.15x faster                                                        |
| genshi_xml               | 41.0 ms                                                     | 36.1 ms: 1.14x faster                                                       |
| nqueens                  | 66.6 ms                                                     | 58.8 ms: 1.13x faster                                                       |
| aiohttp                  | 995 us                                                      | 885 us: 1.12x faster                                                        |
| sqlglot_normalize        | 205 ms                                                      | 183 ms: 1.12x faster                                                        |
| sympy_expand             | 314 ms                                                      | 282 ms: 1.11x faster                                                        |
| deepcopy_reduce          | 2.20 us                                                     | 1.99 us: 1.11x faster                                                       |
| json                     | 3.14 ms                                                     | 2.92 ms: 1.07x faster                                                       |
| scimark_sparse_mat_mult  | 2.72 ms                                                     | 2.54 ms: 1.07x faster                                                       |
| scimark_fft              | 187 ms                                                      | 176 ms: 1.07x faster                                                        |
| unpickle                 | 9.09 us                                                     | 8.58 us: 1.06x faster                                                       |
| regex_effbot             | 1.66 ms                                                     | 1.58 ms: 1.05x faster                                                       |
| logging_format           | 6.76 us                                                     | 6.45 us: 1.05x faster                                                       |
| python_startup           | 20.6 ms                                                     | 19.8 ms: 1.04x faster                                                       |
| xml_etree_parse          | 96.8 ms                                                     | 93.2 ms: 1.04x faster                                                       |
| logging_simple           | 6.22 us                                                     | 6.01 us: 1.04x faster                                                       |
| meteor_contest           | 75.9 ms                                                     | 73.9 ms: 1.03x faster                                                       |
| xml_etree_iterparse      | 65.0 ms                                                     | 63.4 ms: 1.02x faster                                                       |
| fannkuch                 | 256 ms                                                      | 250 ms: 1.02x faster                                                        |
| nbody                    | 71.3 ms                                                     | 69.8 ms: 1.02x faster                                                       |
| pidigits                 | 149 ms                                                      | 147 ms: 1.01x faster                                                        |
| pathlib                  | 75.7 ms                                                     | 77.8 ms: 1.03x slower                                                       |
| bench_mp_pool            | 62.0 ms                                                     | 64.3 ms: 1.04x slower                                                       |
| async_generators         | 222 ms                                                      | 231 ms: 1.04x slower                                                        |
| unpickle_list            | 2.71 us                                                     | 2.83 us: 1.04x slower                                                       |
| pickle                   | 6.85 us                                                     | 7.21 us: 1.05x slower                                                       |
| pickle_list              | 2.75 us                                                     | 2.97 us: 1.08x slower                                                       |
| pickle_dict              | 17.2 us                                                     | 18.7 us: 1.09x slower                                                       |
| gc_traversal             | 1.41 ms                                                     | 1.55 ms: 1.10x slower                                                       |
| create_gc_cycles         | 800 us                                                      | 884 us: 1.11x slower                                                        |
| coverage                 | 39.0 ms                                                     | 45.7 ms: 1.17x slower                                                       |
| python_startup_no_site   | 15.5 ms                                                     | 18.4 ms: 1.19x slower                                                       |
| telco                    | 3.94 ms                                                     | 5.04 ms: 1.28x slower                                                       |
| thrift                   | 617 us                                                      | 8.04 ms: 13.02x slower                                                      |
| Geometric mean           | (ref)                                                       | 1.21x faster                                                                |

Benchmark hidden because not significant (3): json_loads, xml_etree_generate, regex_v8
Ignored benchmarks (6) of results/bm-20220323-3.10.4-9d38120/bm-20220323-pythonperf1-amd64-python-v3.10.4-3.10.4-9d38120.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240406-3.13.0a5+-62aeb0e/bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: unknown
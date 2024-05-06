# Results vs. 3.11.0

- fork: python
- ref: 5f547585fa56c94c5d83
- machine: windows-amd64
- commit hash: 5f54758
- commit date: 2024-05-04
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-python-5f547585fa56c94c5d83-3.13.0a6+-5f54758 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 207 ms: 1.03x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.64 ms: 1.13x faster                                                       |
| html5lib       | 38.9 ms                                                     | 35.8 ms: 1.08x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                                       |
| Geometric mean | (ref)                                                       | 1.08x faster                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-python-5f547585fa56c94c5d83-3.13.0a6+-5f54758 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 263 ms: 1.54x faster                                                        |
| async_tree_none            | 332 ms                                                      | 219 ms: 1.52x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 212 ms: 1.45x faster                                                        |
| async_tree_io              | 808 ms                                                      | 585 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 388 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 614 ms: 1.35x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.43x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-python-5f547585fa56c94c5d83-3.13.0a6+-5f54758 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 49.9 ms: 1.09x faster                                                       |
| nbody          | 70.3 ms                                                     | 66.1 ms: 1.06x faster                                                       |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-python-5f547585fa56c94c5d83-3.13.0a6+-5f54758 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 77.6 ms: 1.17x faster                                                       |
| regex_dna      | 116 ms                                                      | 124 ms: 1.07x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.61 ms: 1.08x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 17.6 ms: 1.24x slower                                                       |
| Geometric mean | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-python-5f547585fa56c94c5d83-3.13.0a6+-5f54758 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.61 ms: 1.44x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 125 us: 1.25x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 176 us: 1.19x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 91.0 ms: 1.07x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.1 ms: 1.06x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.9 ms: 1.01x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.4 us: 1.00x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.9 ms: 1.03x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.75 us: 1.06x slower                                                       |
| pickle               | 6.64 us                                                     | 7.22 us: 1.09x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.5 us: 1.11x slower                                                       |
| pickle_list          | 2.70 us                                                     | 3.05 us: 1.13x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.58 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-python-5f547585fa56c94c5d83-3.13.0a6+-5f54758 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.1 ms: 1.01x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-python-5f547585fa56c94c5d83-3.13.0a6+-5f54758 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 14.5 ms: 1.28x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 31.5 ms: 1.27x faster                                                       |
| mako            | 7.58 ms                                                     | 6.42 ms: 1.18x faster                                                       |
| django_template | 24.4 ms                                                     | 21.5 ms: 1.14x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.21x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-python-5f547585fa56c94c5d83-3.13.0a6+-5f54758 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 100.0 us: 3.26x faster                                                      |
| generators                 | 34.0 ms                                                     | 18.6 ms: 1.82x faster                                                       |
| pylint                     | 323 ms                                                      | 207 ms: 1.56x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 263 ms: 1.54x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.53x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 476 ms: 1.52x faster                                                        |
| async_tree_none            | 332 ms                                                      | 219 ms: 1.52x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 212 ms: 1.45x faster                                                        |
| deltablue                  | 2.70 ms                                                     | 1.86 ms: 1.45x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.61 ms: 1.44x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 50.3 ns: 1.43x faster                                                       |
| async_tree_io              | 808 ms                                                      | 585 ms: 1.38x faster                                                        |
| raytrace                   | 213 ms                                                      | 156 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 388 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 614 ms: 1.35x faster                                                        |
| richards_super             | 38.7 ms                                                     | 29.3 ms: 1.32x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 14.5 ms: 1.28x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.0 ms: 1.27x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 31.5 ms: 1.27x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.61 sec: 1.26x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 757 us: 1.26x faster                                                        |
| unpickle_pure_python       | 157 us                                                      | 125 us: 1.25x faster                                                        |
| mdp                        | 1.59 sec                                                    | 1.31 sec: 1.21x faster                                                      |
| richards                   | 31.4 ms                                                     | 25.9 ms: 1.21x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.67 us: 1.21x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 963 us: 1.21x faster                                                        |
| go                         | 101 ms                                                      | 84.0 ms: 1.20x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 3.79 ms: 1.20x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 176 us: 1.19x faster                                                        |
| coroutines                 | 15.0 ms                                                     | 12.6 ms: 1.19x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 84.6 ms: 1.18x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 57.8 ms: 1.18x faster                                                       |
| mako                       | 7.58 ms                                                     | 6.42 ms: 1.18x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 77.6 ms: 1.17x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.11 us: 1.17x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 22.3 us: 1.16x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.1 ms: 1.16x faster                                                       |
| sympy_str                  | 185 ms                                                      | 161 ms: 1.15x faster                                                        |
| deepcopy                   | 246 us                                                      | 214 us: 1.15x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 12.3 ms: 1.14x faster                                                       |
| django_template            | 24.4 ms                                                     | 21.5 ms: 1.14x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.64 ms: 1.13x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 964 ms: 1.13x faster                                                        |
| scimark_monte_carlo        | 45.3 ms                                                     | 40.4 ms: 1.12x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 473 ms: 1.12x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 171 ms: 1.12x faster                                                        |
| scimark_lu                 | 62.8 ms                                                     | 56.8 ms: 1.11x faster                                                       |
| pyflate                    | 312 ms                                                      | 283 ms: 1.10x faster                                                        |
| sympy_expand               | 299 ms                                                      | 271 ms: 1.10x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                       |
| float                      | 54.4 ms                                                     | 49.9 ms: 1.09x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 62.8 ms: 1.09x faster                                                       |
| mypy2                      | 459 ms                                                      | 423 ms: 1.09x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 35.8 ms: 1.08x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 91.0 ms: 1.07x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 818 us: 1.07x faster                                                        |
| nbody                      | 70.3 ms                                                     | 66.1 ms: 1.06x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 32.6 ms: 1.06x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.95 us: 1.06x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.1 ms: 1.06x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 74.7 ms: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 72.1 ms: 1.04x faster                                                       |
| fannkuch                   | 253 ms                                                      | 243 ms: 1.04x faster                                                        |
| 2to3                       | 214 ms                                                      | 207 ms: 1.03x faster                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                       |
| scimark_fft                | 179 ms                                                      | 176 ms: 1.02x faster                                                        |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.9 ms: 1.01x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 48.6 ms: 1.01x faster                                                       |
| coverage                   | 43.4 ms                                                     | 43.2 ms: 1.01x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 18.4 us: 1.00x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| python_startup             | 19.8 ms                                                     | 20.1 ms: 1.01x slower                                                       |
| aiohttp                    | 883 us                                                      | 900 us: 1.02x slower                                                        |
| bench_mp_pool              | 63.2 ms                                                     | 64.7 ms: 1.02x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 53.9 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.75 us: 1.06x slower                                                       |
| regex_dna                  | 116 ms                                                      | 124 ms: 1.07x slower                                                        |
| regex_effbot               | 1.50 ms                                                     | 1.61 ms: 1.08x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.22 us: 1.09x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.5 us: 1.11x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 79.1 ms: 1.12x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.05 us: 1.13x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.58 us: 1.13x slower                                                       |
| json                       | 2.98 ms                                                     | 3.38 ms: 1.14x slower                                                       |
| dask                       | 273 ms                                                      | 316 ms: 1.16x slower                                                        |
| telco                      | 4.06 ms                                                     | 4.81 ms: 1.18x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 17.6 ms: 1.24x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 906 us: 1.27x slower                                                        |
| async_generators           | 177 ms                                                      | 244 ms: 1.38x slower                                                        |
| thrift                     | 494 us                                                      | 8.09 ms: 16.38x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (3): docutils, scimark_sparse_mat_mult, pycparser
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown
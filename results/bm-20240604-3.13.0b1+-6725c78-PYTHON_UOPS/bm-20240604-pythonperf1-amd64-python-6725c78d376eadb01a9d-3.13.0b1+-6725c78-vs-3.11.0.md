# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: windows-amd64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.02x slower
- HPT reliability: 96.21%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 236 ms: 1.11x slower                                                        |
| chameleon      | 5.26 ms                                                     | 5.40 ms: 1.03x slower                                                       |
| docutils       | 1.64 sec                                                    | 1.86 sec: 1.13x slower                                                      |
| html5lib       | 38.9 ms                                                     | 41.7 ms: 1.07x slower                                                       |
| tornado_http   | 92.8 ms                                                     | 87.8 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 277 ms: 1.46x faster                                                        |
| async_tree_none            | 332 ms                                                      | 234 ms: 1.42x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.41x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 293 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| async_tree_io              | 808 ms                                                      | 602 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 402 ms: 1.32x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 632 ms: 1.31x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.37x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                      | 151 ms: 1.00x slower                                                        |
| float          | 54.4 ms                                                     | 56.5 ms: 1.04x slower                                                       |
| nbody          | 70.3 ms                                                     | 80.1 ms: 1.14x slower                                                       |
| Geometric mean | (ref)                                                       | 1.06x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.60 ms: 1.07x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.4 ms: 1.09x slower                                                       |
| regex_compile  | 91.0 ms                                                     | 110 ms: 1.21x slower                                                        |
| Geometric mean | (ref)                                                       | 1.10x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.90 ms: 1.37x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 89.8 ms: 1.09x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.3 us: 1.01x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 67.6 ms: 1.03x slower                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.54 sec: 1.06x slower                                                      |
| pickle_list          | 2.70 us                                                     | 2.89 us: 1.07x slower                                                       |
| unpickle_pure_python | 157 us                                                      | 169 us: 1.08x slower                                                        |
| xml_etree_process    | 37.2 ms                                                     | 40.2 ms: 1.08x slower                                                       |
| pickle               | 6.64 us                                                     | 7.19 us: 1.08x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.2 us: 1.09x slower                                                       |
| pickle_pure_python   | 208 us                                                      | 228 us: 1.09x slower                                                        |
| unpickle_list        | 2.59 us                                                     | 2.84 us: 1.10x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 58.0 ms: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.44 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.03x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.5 ms: 1.03x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.00x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 38.5 ms: 1.04x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 18.2 ms: 1.01x faster                                                       |
| mako            | 7.58 ms                                                     | 7.78 ms: 1.03x slower                                                       |
| django_template | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                       |
| Geometric mean  | (ref)                                                       | 1.01x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1-amd64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 116 us: 2.80x faster                                                        |
| generators                 | 34.0 ms                                                     | 19.7 ms: 1.72x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 478 ms: 1.52x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 277 ms: 1.46x faster                                                        |
| async_tree_none            | 332 ms                                                      | 234 ms: 1.42x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.41x faster                                                        |
| pylint                     | 323 ms                                                      | 230 ms: 1.41x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.90 ms: 1.37x faster                                                       |
| async_tree_memoization     | 399 ms                                                      | 293 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 385 ms: 1.36x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.50 sec: 1.35x faster                                                      |
| async_tree_io              | 808 ms                                                      | 602 ms: 1.34x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 402 ms: 1.32x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 632 ms: 1.31x faster                                                        |
| coroutines                 | 15.0 ms                                                     | 12.7 ms: 1.18x faster                                                       |
| raytrace                   | 213 ms                                                      | 186 ms: 1.15x faster                                                        |
| richards_super             | 38.7 ms                                                     | 34.1 ms: 1.14x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.24 us: 1.10x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 89.8 ms: 1.09x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.63 us: 1.09x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.60 us: 1.08x faster                                                       |
| comprehensions             | 15.6 us                                                     | 14.4 us: 1.08x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.48 sec: 1.08x faster                                                      |
| chaos                      | 48.4 ms                                                     | 45.5 ms: 1.06x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 87.8 ms: 1.06x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 44.7 ms: 1.04x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 38.5 ms: 1.04x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 841 us: 1.04x faster                                                        |
| richards                   | 31.4 ms                                                     | 30.4 ms: 1.03x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 926 us: 1.03x faster                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 18.2 ms: 1.01x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 18.3 us: 1.01x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| pidigits                   | 150 ms                                                      | 151 ms: 1.00x slower                                                        |
| nqueens                    | 68.3 ms                                                     | 69.7 ms: 1.02x slower                                                       |
| coverage                   | 43.4 ms                                                     | 44.4 ms: 1.02x slower                                                       |
| go                         | 101 ms                                                      | 104 ms: 1.02x slower                                                        |
| chameleon                  | 5.26 ms                                                     | 5.40 ms: 1.03x slower                                                       |
| mako                       | 7.58 ms                                                     | 7.78 ms: 1.03x slower                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 67.6 ms: 1.03x slower                                                       |
| python_startup             | 19.8 ms                                                     | 20.5 ms: 1.03x slower                                                       |
| float                      | 54.4 ms                                                     | 56.5 ms: 1.04x slower                                                       |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| meteor_contest             | 75.2 ms                                                     | 78.4 ms: 1.04x slower                                                       |
| django_template            | 24.4 ms                                                     | 25.6 ms: 1.05x slower                                                       |
| mypy2                      | 459 ms                                                      | 481 ms: 1.05x slower                                                        |
| sympy_integrate            | 14.0 ms                                                     | 14.8 ms: 1.05x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.58 ms: 1.06x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 67.0 ms: 1.06x slower                                                       |
| aiohttp                    | 883 us                                                      | 937 us: 1.06x slower                                                        |
| tomli_loads                | 1.46 sec                                                    | 1.54 sec: 1.06x slower                                                      |
| logging_silent             | 71.8 ns                                                     | 76.2 ns: 1.06x slower                                                       |
| sympy_str                  | 185 ms                                                      | 197 ms: 1.06x slower                                                        |
| pathlib                    | 70.9 ms                                                     | 75.7 ms: 1.07x slower                                                       |
| deepcopy                   | 246 us                                                      | 263 us: 1.07x slower                                                        |
| regex_effbot               | 1.50 ms                                                     | 1.60 ms: 1.07x slower                                                       |
| pprint_pformat             | 1.09 sec                                                    | 1.16 sec: 1.07x slower                                                      |
| pickle_list                | 2.70 us                                                     | 2.89 us: 1.07x slower                                                       |
| pprint_safe_repr           | 529 ms                                                      | 567 ms: 1.07x slower                                                        |
| html5lib                   | 38.9 ms                                                     | 41.7 ms: 1.07x slower                                                       |
| unpickle_pure_python       | 157 us                                                      | 169 us: 1.08x slower                                                        |
| xml_etree_process          | 37.2 ms                                                     | 40.2 ms: 1.08x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.19 us: 1.08x slower                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 53.0 ms: 1.08x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.4 ms: 1.09x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.2 us: 1.09x slower                                                       |
| pickle_pure_python         | 208 us                                                      | 228 us: 1.09x slower                                                        |
| unpickle_list              | 2.59 us                                                     | 2.84 us: 1.10x slower                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.26 us: 1.10x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 58.0 ms: 1.10x slower                                                       |
| pyflate                    | 312 ms                                                      | 345 ms: 1.10x slower                                                        |
| 2to3                       | 214 ms                                                      | 236 ms: 1.11x slower                                                        |
| unpickle                   | 7.57 us                                                     | 8.44 us: 1.12x slower                                                       |
| fannkuch                   | 253 ms                                                      | 285 ms: 1.12x slower                                                        |
| sympy_expand               | 299 ms                                                      | 336 ms: 1.13x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 38.9 ms: 1.13x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.86 sec: 1.13x slower                                                      |
| spectral_norm              | 68.3 ms                                                     | 77.8 ms: 1.14x slower                                                       |
| nbody                      | 70.3 ms                                                     | 80.1 ms: 1.14x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 90.8 ms: 1.16x slower                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 53.5 ms: 1.18x slower                                                       |
| scimark_fft                | 179 ms                                                      | 212 ms: 1.18x slower                                                        |
| regex_compile              | 91.0 ms                                                     | 110 ms: 1.21x slower                                                        |
| pycparser                  | 720 ms                                                      | 876 ms: 1.22x slower                                                        |
| telco                      | 4.06 ms                                                     | 4.98 ms: 1.23x slower                                                       |
| deepcopy_memo              | 26.0 us                                                     | 31.9 us: 1.23x slower                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 3.20 ms: 1.24x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 5.66 ms: 1.24x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 915 us: 1.28x slower                                                        |
| scimark_lu                 | 62.8 ms                                                     | 81.9 ms: 1.30x slower                                                       |
| async_generators           | 177 ms                                                      | 241 ms: 1.36x slower                                                        |
| thrift                     | 494 us                                                      | 9.82 ms: 19.89x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.02x slower                                                                |

Benchmark hidden because not significant (4): json, sympy_sum, sqlglot_transpile, deltablue
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 96.21% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown
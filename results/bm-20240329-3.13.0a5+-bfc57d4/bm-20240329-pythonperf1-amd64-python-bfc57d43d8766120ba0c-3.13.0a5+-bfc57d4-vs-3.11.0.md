# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.12x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 208 ms: 1.02x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.72 ms: 1.12x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| html5lib       | 38.9 ms                                                     | 35.7 ms: 1.09x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 83.7 ms: 1.11x faster                                                       |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 218 ms: 1.52x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 205 ms: 1.51x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 270 ms: 1.48x faster                                                        |
| async_tree_io              | 808 ms                                                      | 578 ms: 1.40x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 380 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 616 ms: 1.35x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.44x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 50.4 ms: 1.08x faster                                                       |
| nbody          | 70.3 ms                                                     | 68.1 ms: 1.03x faster                                                       |
| pidigits       | 150 ms                                                      | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 75.2 ms: 1.21x faster                                                       |
| regex_dna      | 116 ms                                                      | 120 ms: 1.03x slower                                                        |
| regex_v8       | 14.2 ms                                                     | 14.7 ms: 1.04x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.58 ms: 1.45x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 127 us: 1.24x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 175 us: 1.19x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 91.2 ms: 1.07x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.3 ms: 1.05x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.41 sec: 1.04x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 18.0 us: 1.03x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 52.3 ms: 1.01x faster                                                       |
| unpickle_list        | 2.59 us                                                     | 2.63 us: 1.01x slower                                                       |
| pickle               | 6.64 us                                                     | 6.96 us: 1.05x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.84 us: 1.05x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.38 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 20.0 ms: 1.01x slower                                                       |
| python_startup_no_site | 16.8 ms                                                     | 18.5 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.26 ms: 1.21x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 33.7 ms: 1.18x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 15.8 ms: 1.17x faster                                                       |
| django_template | 24.4 ms                                                     | 21.8 ms: 1.12x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.17x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 72.1 us: 4.52x faster                                                       |
| pylint                     | 323 ms                                                      | 187 ms: 1.73x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 469 ms: 1.55x faster                                                        |
| async_tree_none            | 332 ms                                                      | 218 ms: 1.52x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 205 ms: 1.51x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.4 us: 1.51x faster                                                       |
| generators                 | 34.0 ms                                                     | 22.6 ms: 1.51x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 270 ms: 1.48x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.58 ms: 1.45x faster                                                       |
| async_tree_io              | 808 ms                                                      | 578 ms: 1.40x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 380 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                        |
| deltablue                  | 2.70 ms                                                     | 1.98 ms: 1.36x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 616 ms: 1.35x faster                                                        |
| raytrace                   | 213 ms                                                      | 159 ms: 1.35x faster                                                        |
| chaos                      | 48.4 ms                                                     | 37.1 ms: 1.30x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 55.1 ns: 1.30x faster                                                       |
| richards_super             | 38.7 ms                                                     | 30.0 ms: 1.29x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 745 us: 1.28x faster                                                        |
| unpack_sequence            | 46.9 ns                                                     | 36.7 ns: 1.28x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 3.67 ms: 1.24x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 50.8 ms: 1.24x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 127 us: 1.24x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 21.3 us: 1.22x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 958 us: 1.22x faster                                                        |
| mako                       | 7.58 ms                                                     | 6.26 ms: 1.21x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 75.2 ms: 1.21x faster                                                       |
| go                         | 101 ms                                                      | 83.6 ms: 1.21x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 82.9 ms: 1.21x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 175 us: 1.19x faster                                                        |
| nqueens                    | 68.3 ms                                                     | 57.3 ms: 1.19x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 33.7 ms: 1.18x faster                                                       |
| richards                   | 31.4 ms                                                     | 26.6 ms: 1.18x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.6 ms: 1.17x faster                                                       |
| sympy_str                  | 185 ms                                                      | 158 ms: 1.17x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 58.4 ms: 1.17x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 15.8 ms: 1.17x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.0 ms: 1.16x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.37 sec: 1.16x faster                                                      |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.75 sec: 1.16x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.95 us: 1.15x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.2 ms: 1.15x faster                                                       |
| deepcopy                   | 246 us                                                      | 216 us: 1.14x faster                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 43.1 ms: 1.13x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.29 ms: 1.12x faster                                                       |
| django_template            | 24.4 ms                                                     | 21.8 ms: 1.12x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 970 ms: 1.12x faster                                                        |
| chameleon                  | 5.26 ms                                                     | 4.72 ms: 1.12x faster                                                       |
| pyflate                    | 312 ms                                                      | 280 ms: 1.11x faster                                                        |
| logging_format             | 7.16 us                                                     | 6.44 us: 1.11x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 476 ms: 1.11x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.59 us: 1.11x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 83.7 ms: 1.11x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.7 ms: 1.10x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 35.7 ms: 1.09x faster                                                       |
| sympy_expand               | 299 ms                                                      | 274 ms: 1.09x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 175 ms: 1.09x faster                                                        |
| scimark_fft                | 179 ms                                                      | 165 ms: 1.08x faster                                                        |
| float                      | 54.4 ms                                                     | 50.4 ms: 1.08x faster                                                       |
| scimark_sor                | 78.1 ms                                                     | 72.7 ms: 1.07x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 814 us: 1.07x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 91.2 ms: 1.07x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 70.5 ms: 1.07x faster                                                       |
| pycparser                  | 720 ms                                                      | 675 ms: 1.07x faster                                                        |
| deepcopy_reduce            | 2.06 us                                                     | 1.94 us: 1.06x faster                                                       |
| mypy2                      | 459 ms                                                      | 433 ms: 1.06x faster                                                        |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.3 ms: 1.05x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 33.1 ms: 1.04x faster                                                       |
| fannkuch                   | 253 ms                                                      | 243 ms: 1.04x faster                                                        |
| tomli_loads                | 1.46 sec                                                    | 1.41 sec: 1.04x faster                                                      |
| nbody                      | 70.3 ms                                                     | 68.1 ms: 1.03x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 18.0 us: 1.03x faster                                                       |
| 2to3                       | 214 ms                                                      | 208 ms: 1.02x faster                                                        |
| pidigits                   | 150 ms                                                      | 146 ms: 1.02x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                       |
| docutils                   | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 52.3 ms: 1.01x faster                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 63.8 ms: 1.01x slower                                                       |
| python_startup             | 19.8 ms                                                     | 20.0 ms: 1.01x slower                                                       |
| aiohttp                    | 883 us                                                      | 895 us: 1.01x slower                                                        |
| unpickle_list              | 2.59 us                                                     | 2.63 us: 1.01x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.53 ms: 1.03x slower                                                       |
| regex_dna                  | 116 ms                                                      | 120 ms: 1.03x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 14.7 ms: 1.04x slower                                                       |
| pickle                     | 6.64 us                                                     | 6.96 us: 1.05x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.84 us: 1.05x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| coverage                   | 43.4 ms                                                     | 46.3 ms: 1.07x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 18.5 ms: 1.10x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 78.0 ms: 1.10x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.38 us: 1.11x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.77 ms: 1.17x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 847 us: 1.19x slower                                                        |
| async_generators           | 177 ms                                                      | 240 ms: 1.35x slower                                                        |
| thrift                     | 494 us                                                      | 8.11 ms: 16.43x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.12x faster                                                                |

Benchmark hidden because not significant (1): json
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown
# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 223 ms: 1.04x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.64 ms: 1.13x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.68 sec: 1.02x slower                                                      |
| html5lib       | 38.9 ms                                                     | 36.0 ms: 1.08x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 84.0 ms: 1.10x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 213 ms: 1.56x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 261 ms: 1.55x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 201 ms: 1.54x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 266 ms: 1.50x faster                                                        |
| async_tree_io              | 808 ms                                                      | 563 ms: 1.43x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 372 ms: 1.42x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 600 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.47x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 58.8 ms: 1.20x faster                                                       |
| float          | 54.4 ms                                                     | 46.8 ms: 1.16x faster                                                       |
| pidigits       | 150 ms                                                      | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.12x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 83.3 ms: 1.09x faster                                                       |
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.60 ms: 1.07x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 17.6 ms: 1.25x slower                                                       |
| Geometric mean | (ref)                                                       | 1.06x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.51 ms: 1.47x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.19 sec: 1.22x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 130 us: 1.21x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 175 us: 1.19x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 92.4 ms: 1.06x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.3 ms: 1.05x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.4 us: 1.01x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.5 ms: 1.02x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.67 us: 1.03x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.0 us: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.27 us: 1.10x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.96 us: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.53 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 22.5 ms: 1.14x slower                                                       |
| python_startup_no_site | 16.8 ms                                                     | 20.4 ms: 1.21x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.17x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.61 ms: 1.35x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 15.4 ms: 1.20x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 36.3 ms: 1.10x faster                                                       |
| django_template | 24.4 ms                                                     | 22.5 ms: 1.09x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.18x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 69.4 us: 4.69x faster                                                       |
| generators                 | 34.0 ms                                                     | 19.5 ms: 1.74x faster                                                       |
| pylint                     | 323 ms                                                      | 194 ms: 1.66x faster                                                        |
| async_tree_none            | 332 ms                                                      | 213 ms: 1.56x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 261 ms: 1.55x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 201 ms: 1.54x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 473 ms: 1.53x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 266 ms: 1.50x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.51 ms: 1.47x faster                                                       |
| async_tree_io              | 808 ms                                                      | 563 ms: 1.43x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 372 ms: 1.42x faster                                                        |
| comprehensions             | 15.6 us                                                     | 11.3 us: 1.38x faster                                                       |
| async_tree_io_tg           | 829 ms                                                      | 600 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 52.7 ns: 1.36x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.61 ms: 1.35x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.01 ms: 1.34x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.52 sec: 1.33x faster                                                      |
| spectral_norm              | 68.3 ms                                                     | 51.4 ms: 1.33x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.9 ms: 1.24x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 772 us: 1.24x faster                                                        |
| tomli_loads                | 1.46 sec                                                    | 1.19 sec: 1.22x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 130 us: 1.21x faster                                                        |
| raytrace                   | 213 ms                                                      | 178 ms: 1.20x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 21.6 us: 1.20x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 15.4 ms: 1.20x faster                                                       |
| nbody                      | 70.3 ms                                                     | 58.8 ms: 1.20x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 175 us: 1.19x faster                                                        |
| richards_super             | 38.7 ms                                                     | 32.7 ms: 1.19x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 986 us: 1.18x faster                                                        |
| logging_simple             | 6.86 us                                                     | 5.91 us: 1.16x faster                                                       |
| float                      | 54.4 ms                                                     | 46.8 ms: 1.16x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 86.8 ms: 1.15x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.24 ms: 1.15x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.4 ms: 1.15x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.6 ms: 1.14x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.29 us: 1.14x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.64 ms: 1.13x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.41 sec: 1.13x faster                                                      |
| sympy_str                  | 185 ms                                                      | 165 ms: 1.12x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 972 ms: 1.12x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.58 us: 1.12x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 475 ms: 1.12x faster                                                        |
| fannkuch                   | 253 ms                                                      | 229 ms: 1.11x faster                                                        |
| tornado_http               | 92.8 ms                                                     | 84.0 ms: 1.10x faster                                                       |
| deepcopy                   | 246 us                                                      | 223 us: 1.10x faster                                                        |
| pyflate                    | 312 ms                                                      | 283 ms: 1.10x faster                                                        |
| nqueens                    | 68.3 ms                                                     | 61.9 ms: 1.10x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 36.3 ms: 1.10x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 44.6 ms: 1.10x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 83.3 ms: 1.09x faster                                                       |
| go                         | 101 ms                                                      | 93.0 ms: 1.09x faster                                                       |
| django_template            | 24.4 ms                                                     | 22.5 ms: 1.09x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 36.0 ms: 1.08x faster                                                       |
| richards                   | 31.4 ms                                                     | 29.1 ms: 1.08x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.92 us: 1.07x faster                                                       |
| pycparser                  | 720 ms                                                      | 671 ms: 1.07x faster                                                        |
| scimark_fft                | 179 ms                                                      | 167 ms: 1.07x faster                                                        |
| unpack_sequence            | 46.9 ns                                                     | 44.0 ns: 1.07x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 13.2 ms: 1.07x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 822 us: 1.06x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 92.4 ms: 1.06x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.3 ms: 1.05x faster                                                       |
| sympy_expand               | 299 ms                                                      | 284 ms: 1.05x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 184 ms: 1.03x faster                                                        |
| meteor_contest             | 75.2 ms                                                     | 73.2 ms: 1.03x faster                                                       |
| mypy2                      | 459 ms                                                      | 448 ms: 1.02x faster                                                        |
| pidigits                   | 150 ms                                                      | 146 ms: 1.02x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.5 ms: 1.02x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 18.4 us: 1.01x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 4.61 ms: 1.01x slower                                                       |
| aiohttp                    | 883 us                                                      | 898 us: 1.02x slower                                                        |
| xml_etree_generate         | 52.5 ms                                                     | 53.5 ms: 1.02x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.68 sec: 1.02x slower                                                      |
| sqlglot_optimize           | 34.5 ms                                                     | 35.5 ms: 1.03x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.67 us: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 80.5 ms: 1.03x slower                                                       |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| 2to3                       | 214 ms                                                      | 223 ms: 1.04x slower                                                        |
| regex_effbot               | 1.50 ms                                                     | 1.60 ms: 1.07x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.0 us: 1.07x slower                                                       |
| coverage                   | 43.4 ms                                                     | 47.0 ms: 1.08x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.27 us: 1.10x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.96 us: 1.10x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 77.8 ms: 1.10x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 69.1 ms: 1.10x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 70.8 ms: 1.12x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.53 us: 1.13x slower                                                       |
| python_startup             | 19.8 ms                                                     | 22.5 ms: 1.14x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.74 ms: 1.17x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 853 us: 1.20x slower                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 20.4 ms: 1.21x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 17.6 ms: 1.25x slower                                                       |
| json                       | 2.98 ms                                                     | 3.88 ms: 1.30x slower                                                       |
| async_generators           | 177 ms                                                      | 248 ms: 1.40x slower                                                        |
| thrift                     | 494 us                                                      | 8.91 ms: 18.05x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.09x faster                                                                |
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown
# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: windows-amd64
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.01x faster
- HPT reliability: 55.37%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 232 ms: 1.08x slower                                                        |
| chameleon      | 5.26 ms                                                     | 5.12 ms: 1.03x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.84 sec: 1.12x slower                                                      |
| html5lib       | 38.9 ms                                                     | 41.6 ms: 1.07x slower                                                       |
| tornado_http   | 92.8 ms                                                     | 87.8 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                       | 1.04x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 275 ms: 1.47x faster                                                        |
| async_tree_none            | 332 ms                                                      | 233 ms: 1.42x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.42x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 282 ms: 1.42x faster                                                        |
| async_tree_io              | 808 ms                                                      | 593 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 388 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 622 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 400 ms: 1.32x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.39x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 52.6 ms: 1.03x faster                                                       |
| pidigits       | 150 ms                                                      | 151 ms: 1.00x slower                                                        |
| nbody          | 70.3 ms                                                     | 73.8 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                       | 1.01x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.06x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.0 ms: 1.06x slower                                                       |
| regex_compile  | 91.0 ms                                                     | 106 ms: 1.16x slower                                                        |
| Geometric mean | (ref)                                                       | 1.08x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.81 ms: 1.39x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 91.0 ms: 1.07x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.8 ms: 1.01x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 156 us: 1.01x faster                                                        |
| pickle_dict          | 18.5 us                                                     | 18.4 us: 1.00x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 212 us: 1.02x slower                                                        |
| xml_etree_process    | 37.2 ms                                                     | 39.4 ms: 1.06x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.86 us: 1.06x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 56.5 ms: 1.08x slower                                                       |
| pickle               | 6.64 us                                                     | 7.17 us: 1.08x slower                                                       |
| json_loads           | 13.0 us                                                     | 14.1 us: 1.08x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.84 us: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.51 us: 1.12x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x slower                                                                |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.3 ms: 1.03x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.5 ms: 1.04x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.00x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 17.6 ms: 1.05x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 38.6 ms: 1.04x faster                                                       |
| mako            | 7.58 ms                                                     | 7.34 ms: 1.03x faster                                                       |
| django_template | 24.4 ms                                                     | 25.5 ms: 1.05x slower                                                       |
| Geometric mean  | (ref)                                                       | 1.02x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1-amd64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 113 us: 2.89x faster                                                        |
| generators                 | 34.0 ms                                                     | 19.7 ms: 1.73x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 475 ms: 1.53x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 275 ms: 1.47x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.39 sec: 1.46x faster                                                      |
| async_tree_none            | 332 ms                                                      | 233 ms: 1.42x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.42x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 282 ms: 1.42x faster                                                        |
| pylint                     | 323 ms                                                      | 229 ms: 1.41x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.81 ms: 1.39x faster                                                       |
| async_tree_io              | 808 ms                                                      | 593 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 388 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 622 ms: 1.33x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 400 ms: 1.32x faster                                                        |
| coroutines                 | 15.0 ms                                                     | 12.6 ms: 1.18x faster                                                       |
| comprehensions             | 15.6 us                                                     | 13.3 us: 1.18x faster                                                       |
| raytrace                   | 213 ms                                                      | 182 ms: 1.17x faster                                                        |
| richards_super             | 38.7 ms                                                     | 33.2 ms: 1.17x faster                                                       |
| chaos                      | 48.4 ms                                                     | 43.1 ms: 1.12x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.16 us: 1.11x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.44 sec: 1.11x faster                                                      |
| sqlite_synth               | 1.77 us                                                     | 1.61 us: 1.10x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.56 us: 1.09x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 881 us: 1.08x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 91.0 ms: 1.07x faster                                                       |
| richards                   | 31.4 ms                                                     | 29.3 ms: 1.07x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 87.8 ms: 1.06x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.55 ms: 1.06x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 44.1 ms: 1.05x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 17.6 ms: 1.05x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 68.3 ns: 1.05x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1.12 ms: 1.04x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 38.6 ms: 1.04x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 843 us: 1.03x faster                                                        |
| mako                       | 7.58 ms                                                     | 7.34 ms: 1.03x faster                                                       |
| float                      | 54.4 ms                                                     | 52.6 ms: 1.03x faster                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 16.3 ms: 1.03x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 5.12 ms: 1.03x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 66.6 ms: 1.03x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 98.4 ms: 1.02x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.8 ms: 1.01x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 156 us: 1.01x faster                                                        |
| pickle_dict                | 18.5 us                                                     | 18.4 us: 1.00x faster                                                       |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                      |
| pidigits                   | 150 ms                                                      | 151 ms: 1.00x slower                                                        |
| coverage                   | 43.4 ms                                                     | 43.7 ms: 1.01x slower                                                       |
| go                         | 101 ms                                                      | 102 ms: 1.01x slower                                                        |
| pprint_safe_repr           | 529 ms                                                      | 536 ms: 1.01x slower                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 49.6 ms: 1.01x slower                                                       |
| meteor_contest             | 75.2 ms                                                     | 76.4 ms: 1.02x slower                                                       |
| pickle_pure_python         | 208 us                                                      | 212 us: 1.02x slower                                                        |
| pyflate                    | 312 ms                                                      | 321 ms: 1.03x slower                                                        |
| deepcopy                   | 246 us                                                      | 255 us: 1.04x slower                                                        |
| python_startup             | 19.8 ms                                                     | 20.5 ms: 1.04x slower                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 47.0 ms: 1.04x slower                                                       |
| sympy_integrate            | 14.0 ms                                                     | 14.6 ms: 1.04x slower                                                       |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| django_template            | 24.4 ms                                                     | 25.5 ms: 1.05x slower                                                       |
| fannkuch                   | 253 ms                                                      | 265 ms: 1.05x slower                                                        |
| sympy_str                  | 185 ms                                                      | 194 ms: 1.05x slower                                                        |
| mypy2                      | 459 ms                                                      | 480 ms: 1.05x slower                                                        |
| deepcopy_reduce            | 2.06 us                                                     | 2.16 us: 1.05x slower                                                       |
| nbody                      | 70.3 ms                                                     | 73.8 ms: 1.05x slower                                                       |
| scimark_fft                | 179 ms                                                      | 189 ms: 1.05x slower                                                        |
| gc_traversal               | 1.49 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.06x slower                                                       |
| aiohttp                    | 883 us                                                      | 933 us: 1.06x slower                                                        |
| regex_v8                   | 14.2 ms                                                     | 15.0 ms: 1.06x slower                                                       |
| xml_etree_process          | 37.2 ms                                                     | 39.4 ms: 1.06x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 67.0 ms: 1.06x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.86 us: 1.06x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 75.8 ms: 1.07x slower                                                       |
| html5lib                   | 38.9 ms                                                     | 41.6 ms: 1.07x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 56.5 ms: 1.08x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.17 us: 1.08x slower                                                       |
| json_loads                 | 13.0 us                                                     | 14.1 us: 1.08x slower                                                       |
| 2to3                       | 214 ms                                                      | 232 ms: 1.08x slower                                                        |
| spectral_norm              | 68.3 ms                                                     | 74.1 ms: 1.08x slower                                                       |
| deepcopy_memo              | 26.0 us                                                     | 28.5 us: 1.10x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.84 us: 1.10x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 85.7 ms: 1.10x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 38.3 ms: 1.11x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.84 sec: 1.12x slower                                                      |
| sympy_expand               | 299 ms                                                      | 335 ms: 1.12x slower                                                        |
| unpickle                   | 7.57 us                                                     | 8.51 us: 1.12x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 5.18 ms: 1.14x slower                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.94 ms: 1.14x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.70 ms: 1.16x slower                                                       |
| regex_compile              | 91.0 ms                                                     | 106 ms: 1.16x slower                                                        |
| scimark_lu                 | 62.8 ms                                                     | 73.6 ms: 1.17x slower                                                       |
| pycparser                  | 720 ms                                                      | 876 ms: 1.22x slower                                                        |
| create_gc_cycles           | 713 us                                                      | 917 us: 1.29x slower                                                        |
| async_generators           | 177 ms                                                      | 243 ms: 1.37x slower                                                        |
| thrift                     | 494 us                                                      | 9.56 ms: 19.36x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (3): json, pprint_pformat, tomli_loads
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 55.37% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown
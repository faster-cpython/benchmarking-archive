# Results vs. 3.11.0

- fork: python
- ref: edb6883ef3f7a8ef0c83
- machine: windows-amd64
- commit hash: edb6883
- commit date: 2024-06-01
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf1-amd64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 208 ms: 1.03x faster                                                        |
| chameleon      | 5.26 ms                                                     | 4.86 ms: 1.08x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| html5lib       | 38.9 ms                                                     | 35.4 ms: 1.10x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 82.0 ms: 1.13x faster                                                       |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf1-amd64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 219 ms: 1.51x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.51x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 207 ms: 1.49x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 386 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                                        |
| async_tree_io              | 808 ms                                                      | 594 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 610 ms: 1.36x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.43x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf1-amd64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 49.7 ms: 1.09x faster                                                       |
| nbody          | 70.3 ms                                                     | 70.9 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf1-amd64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 77.9 ms: 1.17x faster                                                       |
| regex_dna      | 116 ms                                                      | 116 ms: 1.00x faster                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.55 ms: 1.03x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 16.4 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf1-amd64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.62 ms: 1.44x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 125 us: 1.25x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 179 us: 1.16x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 90.2 ms: 1.08x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.9 ms: 1.06x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.38 sec: 1.06x faster                                                      |
| xml_etree_process    | 37.2 ms                                                     | 36.3 ms: 1.02x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.1 ms: 1.01x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.69 us: 1.04x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.8 us: 1.07x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.92 us: 1.08x slower                                                       |
| pickle               | 6.64 us                                                     | 7.20 us: 1.08x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.40 us: 1.11x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf1-amd64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.1 ms: 1.05x faster                                                       |
| python_startup         | 19.8 ms                                                     | 20.1 ms: 1.02x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf1-amd64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 31.9 ms: 1.25x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 14.7 ms: 1.25x faster                                                       |
| mako            | 7.58 ms                                                     | 6.51 ms: 1.16x faster                                                       |
| django_template | 24.4 ms                                                     | 21.8 ms: 1.12x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.20x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf1-amd64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 103 us: 3.16x faster                                                        |
| generators                 | 34.0 ms                                                     | 19.2 ms: 1.77x faster                                                       |
| pylint                     | 323 ms                                                      | 204 ms: 1.58x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 472 ms: 1.54x faster                                                        |
| async_tree_none            | 332 ms                                                      | 219 ms: 1.51x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.51x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.3 us: 1.51x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 207 ms: 1.49x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.62 ms: 1.44x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 1.94 ms: 1.39x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 386 ms: 1.37x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.48 sec: 1.37x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                                        |
| async_tree_io              | 808 ms                                                      | 594 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 610 ms: 1.36x faster                                                        |
| raytrace                   | 213 ms                                                      | 160 ms: 1.34x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 54.1 ns: 1.33x faster                                                       |
| richards_super             | 38.7 ms                                                     | 30.4 ms: 1.27x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.3 ms: 1.26x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 759 us: 1.26x faster                                                        |
| genshi_xml                 | 39.9 ms                                                     | 31.9 ms: 1.25x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 14.7 ms: 1.25x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 125 us: 1.25x faster                                                        |
| hexiom                     | 4.55 ms                                                     | 3.77 ms: 1.21x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 56.6 ms: 1.21x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 969 us: 1.20x faster                                                        |
| dulwich_log                | 46.4 ms                                                     | 38.7 ms: 1.20x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 83.5 ms: 1.20x faster                                                       |
| go                         | 101 ms                                                      | 84.5 ms: 1.20x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.7 ms: 1.18x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.83 us: 1.18x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 77.9 ms: 1.17x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 179 us: 1.16x faster                                                        |
| mako                       | 7.58 ms                                                     | 6.51 ms: 1.16x faster                                                       |
| richards                   | 31.4 ms                                                     | 27.0 ms: 1.16x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 54.2 ms: 1.16x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.20 us: 1.15x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 22.5 us: 1.15x faster                                                       |
| sympy_str                  | 185 ms                                                      | 161 ms: 1.15x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 12.3 ms: 1.14x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 82.0 ms: 1.13x faster                                                       |
| deepcopy                   | 246 us                                                      | 218 us: 1.13x faster                                                        |
| django_template            | 24.4 ms                                                     | 21.8 ms: 1.12x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.59 us: 1.11x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 787 us: 1.11x faster                                                        |
| mdp                        | 1.59 sec                                                    | 1.44 sec: 1.10x faster                                                      |
| pyflate                    | 312 ms                                                      | 283 ms: 1.10x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 35.4 ms: 1.10x faster                                                       |
| mypy2                      | 459 ms                                                      | 418 ms: 1.10x faster                                                        |
| sympy_expand               | 299 ms                                                      | 273 ms: 1.09x faster                                                        |
| float                      | 54.4 ms                                                     | 49.7 ms: 1.09x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.5 ms: 1.09x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 90.2 ms: 1.08x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.86 ms: 1.08x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 176 ms: 1.08x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 1.01 sec: 1.08x faster                                                      |
| pprint_safe_repr           | 529 ms                                                      | 494 ms: 1.07x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 63.9 ms: 1.07x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 45.8 ms: 1.07x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.9 ms: 1.06x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.38 sec: 1.06x faster                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 16.1 ms: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 72.1 ms: 1.04x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.98 us: 1.04x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 33.3 ms: 1.04x faster                                                       |
| 2to3                       | 214 ms                                                      | 208 ms: 1.03x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.3 ms: 1.02x faster                                                       |
| docutils                   | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                                      |
| fannkuch                   | 253 ms                                                      | 249 ms: 1.02x faster                                                        |
| scimark_sor                | 78.1 ms                                                     | 76.8 ms: 1.02x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.56 ms: 1.01x faster                                                       |
| regex_dna                  | 116 ms                                                      | 116 ms: 1.00x faster                                                        |
| flaskblogging              | 2.03 sec                                                    | 2.04 sec: 1.00x slower                                                      |
| nbody                      | 70.3 ms                                                     | 70.9 ms: 1.01x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 53.1 ms: 1.01x slower                                                       |
| python_startup             | 19.8 ms                                                     | 20.1 ms: 1.02x slower                                                       |
| scimark_fft                | 179 ms                                                      | 182 ms: 1.02x slower                                                        |
| bench_mp_pool              | 63.2 ms                                                     | 64.8 ms: 1.03x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.55 ms: 1.03x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.69 us: 1.04x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.05x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 74.8 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.8 us: 1.07x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.92 us: 1.08x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.20 us: 1.08x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.40 us: 1.11x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.62 ms: 1.14x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 16.4 ms: 1.16x slower                                                       |
| async_generators           | 177 ms                                                      | 224 ms: 1.26x slower                                                        |
| create_gc_cycles           | 713 us                                                      | 907 us: 1.27x slower                                                        |
| thrift                     | 494 us                                                      | 8.05 ms: 16.30x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (6): pycparser, pidigits, pickle_dict, coverage, aiohttp, json
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown
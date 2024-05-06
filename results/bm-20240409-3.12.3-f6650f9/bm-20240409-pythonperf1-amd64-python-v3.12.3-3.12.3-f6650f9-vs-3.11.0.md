# Results vs. 3.11.0

- fork: python
- ref: v3.12.3
- machine: windows-amd64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 210 ms: 1.02x faster                                        |
| chameleon      | 5.26 ms                                                     | 4.94 ms: 1.07x faster                                       |
| docutils       | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                      |
| html5lib       | 38.9 ms                                                     | 36.7 ms: 1.06x faster                                       |
| tornado_http   | 92.8 ms                                                     | 84.8 ms: 1.09x faster                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_memoization     | 399 ms                                                      | 334 ms: 1.19x faster                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 346 ms: 1.17x faster                                        |
| async_tree_none            | 332 ms                                                      | 287 ms: 1.16x faster                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 475 ms: 1.12x faster                                        |
| async_tree_io              | 808 ms                                                      | 726 ms: 1.11x faster                                        |
| async_tree_none_tg         | 309 ms                                                      | 278 ms: 1.11x faster                                        |
| async_tree_io_tg           | 829 ms                                                      | 756 ms: 1.10x faster                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 484 ms: 1.08x faster                                        |
| Geometric mean             | (ref)                                                       | 1.13x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| pidigits       | 150 ms                                                      | 148 ms: 1.02x faster                                        |
| float          | 54.4 ms                                                     | 55.1 ms: 1.01x slower                                       |
| nbody          | 70.3 ms                                                     | 74.4 ms: 1.06x slower                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 87.1 ms: 1.05x faster                                       |
| regex_v8       | 14.2 ms                                                     | 13.8 ms: 1.03x faster                                       |
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                        |
| regex_effbot   | 1.50 ms                                                     | 1.64 ms: 1.10x slower                                       |
| Geometric mean | (ref)                                                       | 1.01x slower                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.62 ms: 1.44x faster                                       |
| unpickle_pure_python | 157 us                                                      | 130 us: 1.20x faster                                        |
| pickle_pure_python   | 208 us                                                      | 192 us: 1.09x faster                                        |
| xml_etree_parse      | 97.6 ms                                                     | 91.6 ms: 1.07x faster                                       |
| tomli_loads          | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 63.0 ms: 1.04x faster                                       |
| xml_etree_process    | 37.2 ms                                                     | 37.5 ms: 1.01x slower                                       |
| pickle_dict          | 18.5 us                                                     | 18.7 us: 1.01x slower                                       |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                       |
| xml_etree_generate   | 52.5 ms                                                     | 56.1 ms: 1.07x slower                                       |
| unpickle             | 7.57 us                                                     | 8.24 us: 1.09x slower                                       |
| unpickle_list        | 2.59 us                                                     | 2.82 us: 1.09x slower                                       |
| pickle_list          | 2.70 us                                                     | 2.95 us: 1.09x slower                                       |
| pickle               | 6.64 us                                                     | 7.33 us: 1.10x slower                                       |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.0 ms: 1.05x faster                                       |
| python_startup         | 19.8 ms                                                     | 19.1 ms: 1.04x faster                                       |
| Geometric mean         | (ref)                                                       | 1.04x faster                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 33.5 ms: 1.19x faster                                       |
| genshi_text     | 18.4 ms                                                     | 15.7 ms: 1.17x faster                                       |
| mako            | 7.58 ms                                                     | 7.10 ms: 1.07x faster                                       |
| django_template | 24.4 ms                                                     | 22.9 ms: 1.07x faster                                       |
| Geometric mean  | (ref)                                                       | 1.12x faster                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1-amd64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 75.5 us: 4.31x faster                                       |
| pylint                     | 323 ms                                                      | 205 ms: 1.58x faster                                        |
| asyncio_tcp                | 726 ms                                                      | 474 ms: 1.53x faster                                        |
| generators                 | 34.0 ms                                                     | 23.5 ms: 1.44x faster                                       |
| comprehensions             | 15.6 us                                                     | 10.9 us: 1.44x faster                                       |
| json_dumps                 | 8.09 ms                                                     | 5.62 ms: 1.44x faster                                       |
| richards_super             | 38.7 ms                                                     | 30.0 ms: 1.29x faster                                       |
| deltablue                  | 2.70 ms                                                     | 2.17 ms: 1.24x faster                                       |
| unpickle_pure_python       | 157 us                                                      | 130 us: 1.20x faster                                        |
| async_tree_memoization     | 399 ms                                                      | 334 ms: 1.19x faster                                        |
| genshi_xml                 | 39.9 ms                                                     | 33.5 ms: 1.19x faster                                       |
| richards                   | 31.4 ms                                                     | 26.4 ms: 1.19x faster                                       |
| mdp                        | 1.59 sec                                                    | 1.34 sec: 1.19x faster                                      |
| sympy_sum                  | 100 ms                                                      | 84.5 ms: 1.18x faster                                       |
| sqlglot_parse              | 953 us                                                      | 811 us: 1.18x faster                                        |
| genshi_text                | 18.4 ms                                                     | 15.7 ms: 1.17x faster                                       |
| go                         | 101 ms                                                      | 86.4 ms: 1.17x faster                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 346 ms: 1.17x faster                                        |
| async_tree_none            | 332 ms                                                      | 287 ms: 1.16x faster                                        |
| logging_silent             | 71.8 ns                                                     | 62.6 ns: 1.15x faster                                       |
| sqlalchemy_imperative      | 10.4 ms                                                     | 9.11 ms: 1.15x faster                                       |
| coverage                   | 43.4 ms                                                     | 38.0 ms: 1.14x faster                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1.02 ms: 1.14x faster                                       |
| hexiom                     | 4.55 ms                                                     | 4.01 ms: 1.13x faster                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.4 ms: 1.13x faster                                       |
| chaos                      | 48.4 ms                                                     | 42.9 ms: 1.13x faster                                       |
| sympy_str                  | 185 ms                                                      | 164 ms: 1.13x faster                                        |
| scimark_lu                 | 62.8 ms                                                     | 55.9 ms: 1.12x faster                                       |
| deepcopy_memo              | 26.0 us                                                     | 23.2 us: 1.12x faster                                       |
| raytrace                   | 213 ms                                                      | 191 ms: 1.12x faster                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 475 ms: 1.12x faster                                        |
| async_tree_io              | 808 ms                                                      | 726 ms: 1.11x faster                                        |
| async_tree_none_tg         | 309 ms                                                      | 278 ms: 1.11x faster                                        |
| nqueens                    | 68.3 ms                                                     | 61.9 ms: 1.10x faster                                       |
| async_tree_io_tg           | 829 ms                                                      | 756 ms: 1.10x faster                                        |
| tornado_http               | 92.8 ms                                                     | 84.8 ms: 1.09x faster                                       |
| pickle_pure_python         | 208 us                                                      | 192 us: 1.09x faster                                        |
| dulwich_log                | 46.4 ms                                                     | 42.7 ms: 1.09x faster                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 41.9 ms: 1.08x faster                                       |
| logging_simple             | 6.86 us                                                     | 6.34 us: 1.08x faster                                       |
| deepcopy                   | 246 us                                                      | 228 us: 1.08x faster                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 484 ms: 1.08x faster                                        |
| coroutines                 | 15.0 ms                                                     | 13.9 ms: 1.08x faster                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.89 sec: 1.07x faster                                      |
| spectral_norm              | 68.3 ms                                                     | 63.8 ms: 1.07x faster                                       |
| mako                       | 7.58 ms                                                     | 7.10 ms: 1.07x faster                                       |
| dask                       | 273 ms                                                      | 255 ms: 1.07x faster                                        |
| bench_thread_pool          | 872 us                                                      | 817 us: 1.07x faster                                        |
| django_template            | 24.4 ms                                                     | 22.9 ms: 1.07x faster                                       |
| xml_etree_parse            | 97.6 ms                                                     | 91.6 ms: 1.07x faster                                       |
| chameleon                  | 5.26 ms                                                     | 4.94 ms: 1.07x faster                                       |
| sympy_expand               | 299 ms                                                      | 281 ms: 1.06x faster                                        |
| tomli_loads                | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                      |
| fannkuch                   | 253 ms                                                      | 238 ms: 1.06x faster                                        |
| logging_format             | 7.16 us                                                     | 6.75 us: 1.06x faster                                       |
| html5lib                   | 38.9 ms                                                     | 36.7 ms: 1.06x faster                                       |
| pprint_pformat             | 1.09 sec                                                    | 1.03 sec: 1.06x faster                                      |
| pyflate                    | 312 ms                                                      | 295 ms: 1.06x faster                                        |
| python_startup_no_site     | 16.8 ms                                                     | 16.0 ms: 1.05x faster                                       |
| sqlglot_normalize          | 190 ms                                                      | 181 ms: 1.05x faster                                        |
| pprint_safe_repr           | 529 ms                                                      | 505 ms: 1.05x faster                                        |
| regex_compile              | 91.0 ms                                                     | 87.1 ms: 1.05x faster                                       |
| meteor_contest             | 75.2 ms                                                     | 72.1 ms: 1.04x faster                                       |
| aiohttp                    | 883 us                                                      | 847 us: 1.04x faster                                        |
| telco                      | 4.06 ms                                                     | 3.90 ms: 1.04x faster                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 63.0 ms: 1.04x faster                                       |
| python_startup             | 19.8 ms                                                     | 19.1 ms: 1.04x faster                                       |
| crypto_pyaes               | 48.9 ms                                                     | 47.4 ms: 1.03x faster                                       |
| regex_v8                   | 14.2 ms                                                     | 13.8 ms: 1.03x faster                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 33.7 ms: 1.03x faster                                       |
| sqlalchemy_declarative     | 85.6 ms                                                     | 83.6 ms: 1.02x faster                                       |
| scimark_fft                | 179 ms                                                      | 175 ms: 1.02x faster                                        |
| deepcopy_reduce            | 2.06 us                                                     | 2.02 us: 1.02x faster                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.52 ms: 1.02x faster                                       |
| docutils                   | 1.64 sec                                                    | 1.61 sec: 1.02x faster                                      |
| 2to3                       | 214 ms                                                      | 210 ms: 1.02x faster                                        |
| pidigits                   | 150 ms                                                      | 148 ms: 1.02x faster                                        |
| scimark_sor                | 78.1 ms                                                     | 76.9 ms: 1.02x faster                                       |
| gc_traversal               | 1.49 ms                                                     | 1.50 ms: 1.01x slower                                       |
| xml_etree_process          | 37.2 ms                                                     | 37.5 ms: 1.01x slower                                       |
| pickle_dict                | 18.5 us                                                     | 18.7 us: 1.01x slower                                       |
| float                      | 54.4 ms                                                     | 55.1 ms: 1.01x slower                                       |
| create_gc_cycles           | 713 us                                                      | 733 us: 1.03x slower                                        |
| thrift                     | 494 us                                                      | 511 us: 1.03x slower                                        |
| bench_mp_pool              | 63.2 ms                                                     | 65.6 ms: 1.04x slower                                       |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                        |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                       |
| nbody                      | 70.3 ms                                                     | 74.4 ms: 1.06x slower                                       |
| xml_etree_generate         | 52.5 ms                                                     | 56.1 ms: 1.07x slower                                       |
| pathlib                    | 70.9 ms                                                     | 76.0 ms: 1.07x slower                                       |
| mypy2                      | 459 ms                                                      | 494 ms: 1.08x slower                                        |
| unpickle                   | 7.57 us                                                     | 8.24 us: 1.09x slower                                       |
| unpickle_list              | 2.59 us                                                     | 2.82 us: 1.09x slower                                       |
| pickle_list                | 2.70 us                                                     | 2.95 us: 1.09x slower                                       |
| regex_effbot               | 1.50 ms                                                     | 1.64 ms: 1.10x slower                                       |
| pickle                     | 6.64 us                                                     | 7.33 us: 1.10x slower                                       |
| async_generators           | 177 ms                                                      | 230 ms: 1.30x slower                                        |
| Geometric mean             | (ref)                                                       | 1.09x faster                                                |

Benchmark hidden because not significant (3): sqlite_synth, json, pycparser
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown
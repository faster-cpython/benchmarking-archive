# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: windows-amd64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 220 ms: 1.03x slower                                                      |
| chameleon      | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                     |
| docutils       | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                    |
| html5lib       | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                                     |
| tornado_http   | 92.8 ms                                                     | 83.9 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                       | 1.04x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                      |
| async_tree_none_tg         | 309 ms                                                      | 202 ms: 1.53x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.52x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                      |
| async_tree_io              | 808 ms                                                      | 570 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 375 ms: 1.41x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 380 ms: 1.38x faster                                                      |
| async_tree_io_tg           | 829 ms                                                      | 611 ms: 1.36x faster                                                      |
| Geometric mean             | (ref)                                                       | 1.45x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 59.0 ms: 1.19x faster                                                     |
| float          | 54.4 ms                                                     | 47.2 ms: 1.15x faster                                                     |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                       | 1.12x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 89.1 ms: 1.02x faster                                                     |
| regex_dna      | 116 ms                                                      | 118 ms: 1.01x slower                                                      |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                       | 1.01x slower                                                              |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.57 ms: 1.45x faster                                                     |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.21x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 136 us: 1.15x faster                                                      |
| tomli_loads          | 1.46 sec                                                    | 1.32 sec: 1.10x faster                                                    |
| xml_etree_parse      | 97.6 ms                                                     | 89.6 ms: 1.09x faster                                                     |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.3 ms: 1.07x faster                                                     |
| xml_etree_process    | 37.2 ms                                                     | 37.0 ms: 1.00x faster                                                     |
| xml_etree_generate   | 52.5 ms                                                     | 53.0 ms: 1.01x slower                                                     |
| unpickle_list        | 2.59 us                                                     | 2.74 us: 1.06x slower                                                     |
| pickle_list          | 2.70 us                                                     | 2.88 us: 1.07x slower                                                     |
| pickle               | 6.64 us                                                     | 7.16 us: 1.08x slower                                                     |
| json_loads           | 13.0 us                                                     | 14.5 us: 1.12x slower                                                     |
| unpickle             | 7.57 us                                                     | 8.56 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                              |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                     |
| python_startup_no_site | 16.8 ms                                                     | 19.6 ms: 1.16x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.14x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.08 ms: 1.25x faster                                                     |
| genshi_text     | 18.4 ms                                                     | 15.0 ms: 1.23x faster                                                     |
| genshi_xml      | 39.9 ms                                                     | 33.3 ms: 1.20x faster                                                     |
| django_template | 24.4 ms                                                     | 22.5 ms: 1.08x faster                                                     |
| Geometric mean  | (ref)                                                       | 1.19x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 70.6 us: 4.61x faster                                                     |
| generators                 | 34.0 ms                                                     | 20.3 ms: 1.67x faster                                                     |
| pylint                     | 323 ms                                                      | 195 ms: 1.66x faster                                                      |
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                      |
| async_tree_none_tg         | 309 ms                                                      | 202 ms: 1.53x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.52x faster                                                      |
| asyncio_tcp                | 726 ms                                                      | 480 ms: 1.51x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                      |
| json_dumps                 | 8.09 ms                                                     | 5.57 ms: 1.45x faster                                                     |
| async_tree_io              | 808 ms                                                      | 570 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 375 ms: 1.41x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 380 ms: 1.38x faster                                                      |
| async_tree_io_tg           | 829 ms                                                      | 611 ms: 1.36x faster                                                      |
| logging_silent             | 71.8 ns                                                     | 53.1 ns: 1.35x faster                                                     |
| deltablue                  | 2.70 ms                                                     | 2.02 ms: 1.34x faster                                                     |
| comprehensions             | 15.6 us                                                     | 12.0 us: 1.31x faster                                                     |
| mako                       | 7.58 ms                                                     | 6.08 ms: 1.25x faster                                                     |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.63 sec: 1.24x faster                                                    |
| genshi_text                | 18.4 ms                                                     | 15.0 ms: 1.23x faster                                                     |
| spectral_norm              | 68.3 ms                                                     | 55.6 ms: 1.23x faster                                                     |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.21x faster                                                      |
| chaos                      | 48.4 ms                                                     | 40.1 ms: 1.21x faster                                                     |
| genshi_xml                 | 39.9 ms                                                     | 33.3 ms: 1.20x faster                                                     |
| raytrace                   | 213 ms                                                      | 178 ms: 1.20x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 796 us: 1.20x faster                                                      |
| nbody                      | 70.3 ms                                                     | 59.0 ms: 1.19x faster                                                     |
| deepcopy_memo              | 26.0 us                                                     | 22.3 us: 1.17x faster                                                     |
| unpickle_pure_python       | 157 us                                                      | 136 us: 1.15x faster                                                      |
| float                      | 54.4 ms                                                     | 47.2 ms: 1.15x faster                                                     |
| sqlglot_transpile          | 1.16 ms                                                     | 1.01 ms: 1.15x faster                                                     |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.14x faster                                                     |
| sympy_sum                  | 100 ms                                                      | 87.9 ms: 1.14x faster                                                     |
| dulwich_log                | 46.4 ms                                                     | 40.9 ms: 1.13x faster                                                     |
| logging_simple             | 6.86 us                                                     | 6.05 us: 1.13x faster                                                     |
| deepcopy                   | 246 us                                                      | 219 us: 1.12x faster                                                      |
| richards_super             | 38.7 ms                                                     | 34.4 ms: 1.12x faster                                                     |
| chameleon                  | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                     |
| tornado_http               | 92.8 ms                                                     | 83.9 ms: 1.11x faster                                                     |
| sqlite_synth               | 1.77 us                                                     | 1.60 us: 1.11x faster                                                     |
| tomli_loads                | 1.46 sec                                                    | 1.32 sec: 1.10x faster                                                    |
| logging_format             | 7.16 us                                                     | 6.51 us: 1.10x faster                                                     |
| sympy_str                  | 185 ms                                                      | 168 ms: 1.10x faster                                                      |
| xml_etree_parse            | 97.6 ms                                                     | 89.6 ms: 1.09x faster                                                     |
| crypto_pyaes               | 48.9 ms                                                     | 44.9 ms: 1.09x faster                                                     |
| django_template            | 24.4 ms                                                     | 22.5 ms: 1.08x faster                                                     |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.38 ms: 1.08x faster                                                     |
| nqueens                    | 68.3 ms                                                     | 63.6 ms: 1.07x faster                                                     |
| scimark_monte_carlo        | 45.3 ms                                                     | 42.3 ms: 1.07x faster                                                     |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.3 ms: 1.07x faster                                                     |
| pprint_safe_repr           | 529 ms                                                      | 496 ms: 1.07x faster                                                      |
| html5lib                   | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                                     |
| deepcopy_reduce            | 2.06 us                                                     | 1.94 us: 1.06x faster                                                     |
| pyflate                    | 312 ms                                                      | 296 ms: 1.05x faster                                                      |
| bench_thread_pool          | 872 us                                                      | 828 us: 1.05x faster                                                      |
| pprint_pformat             | 1.09 sec                                                    | 1.03 sec: 1.05x faster                                                    |
| sympy_integrate            | 14.0 ms                                                     | 13.4 ms: 1.05x faster                                                     |
| go                         | 101 ms                                                      | 96.7 ms: 1.05x faster                                                     |
| sqlglot_normalize          | 190 ms                                                      | 182 ms: 1.04x faster                                                      |
| mdp                        | 1.59 sec                                                    | 1.54 sec: 1.04x faster                                                    |
| sympy_expand               | 299 ms                                                      | 290 ms: 1.03x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 73.4 ms: 1.02x faster                                                     |
| regex_compile              | 91.0 ms                                                     | 89.1 ms: 1.02x faster                                                     |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                      |
| mypy2                      | 459 ms                                                      | 453 ms: 1.01x faster                                                      |
| richards                   | 31.4 ms                                                     | 31.0 ms: 1.01x faster                                                     |
| scimark_fft                | 179 ms                                                      | 178 ms: 1.01x faster                                                      |
| xml_etree_process          | 37.2 ms                                                     | 37.0 ms: 1.00x faster                                                     |
| xml_etree_generate         | 52.5 ms                                                     | 53.0 ms: 1.01x slower                                                     |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.01x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.52 ms: 1.02x slower                                                     |
| sqlglot_optimize           | 34.5 ms                                                     | 35.3 ms: 1.02x slower                                                     |
| aiohttp                    | 883 us                                                      | 903 us: 1.02x slower                                                      |
| 2to3                       | 214 ms                                                      | 220 ms: 1.03x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                    |
| coverage                   | 43.4 ms                                                     | 44.7 ms: 1.03x slower                                                     |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                                     |
| fannkuch                   | 253 ms                                                      | 263 ms: 1.04x slower                                                      |
| unpickle_list              | 2.59 us                                                     | 2.74 us: 1.06x slower                                                     |
| bench_mp_pool              | 63.2 ms                                                     | 67.3 ms: 1.06x slower                                                     |
| pickle_list                | 2.70 us                                                     | 2.88 us: 1.07x slower                                                     |
| json                       | 2.98 ms                                                     | 3.19 ms: 1.07x slower                                                     |
| scimark_sor                | 78.1 ms                                                     | 84.1 ms: 1.08x slower                                                     |
| pickle                     | 6.64 us                                                     | 7.16 us: 1.08x slower                                                     |
| pathlib                    | 70.9 ms                                                     | 77.5 ms: 1.09x slower                                                     |
| python_startup             | 19.8 ms                                                     | 21.9 ms: 1.11x slower                                                     |
| json_loads                 | 13.0 us                                                     | 14.5 us: 1.12x slower                                                     |
| unpickle                   | 7.57 us                                                     | 8.56 us: 1.13x slower                                                     |
| hexiom                     | 4.55 ms                                                     | 5.22 ms: 1.15x slower                                                     |
| python_startup_no_site     | 16.8 ms                                                     | 19.6 ms: 1.16x slower                                                     |
| create_gc_cycles           | 713 us                                                      | 851 us: 1.19x slower                                                      |
| scimark_lu                 | 62.8 ms                                                     | 75.5 ms: 1.20x slower                                                     |
| telco                      | 4.06 ms                                                     | 4.91 ms: 1.21x slower                                                     |
| unpack_sequence            | 46.9 ns                                                     | 57.5 ns: 1.23x slower                                                     |
| async_generators           | 177 ms                                                      | 244 ms: 1.38x slower                                                      |
| thrift                     | 494 us                                                      | 9.29 ms: 18.81x slower                                                    |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                              |

Benchmark hidden because not significant (3): pickle_dict, regex_v8, pycparser
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: unknown
# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-amd64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 218 ms: 1.02x slower                                                      |
| chameleon      | 5.26 ms                                                     | 4.79 ms: 1.10x faster                                                     |
| docutils       | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                    |
| html5lib       | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                                     |
| tornado_http   | 92.8 ms                                                     | 85.5 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                       | 1.04x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 214 ms: 1.56x faster                                                      |
| async_tree_none_tg         | 309 ms                                                      | 203 ms: 1.52x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.52x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 267 ms: 1.49x faster                                                      |
| async_tree_io              | 808 ms                                                      | 567 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 376 ms: 1.41x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                      |
| async_tree_io_tg           | 829 ms                                                      | 619 ms: 1.34x faster                                                      |
| Geometric mean             | (ref)                                                       | 1.45x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 58.3 ms: 1.21x faster                                                     |
| float          | 54.4 ms                                                     | 46.0 ms: 1.18x faster                                                     |
| pidigits       | 150 ms                                                      | 146 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                       | 1.13x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 83.8 ms: 1.09x faster                                                     |
| regex_v8       | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                     |
| regex_effbot   | 1.50 ms                                                     | 1.55 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                       | 1.01x faster                                                              |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.55 ms: 1.46x faster                                                     |
| unpickle_pure_python | 157 us                                                      | 125 us: 1.25x faster                                                      |
| tomli_loads          | 1.46 sec                                                    | 1.17 sec: 1.25x faster                                                    |
| pickle_pure_python   | 208 us                                                      | 173 us: 1.21x faster                                                      |
| xml_etree_parse      | 97.6 ms                                                     | 90.1 ms: 1.08x faster                                                     |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.7 ms: 1.08x faster                                                     |
| xml_etree_generate   | 52.5 ms                                                     | 53.0 ms: 1.01x slower                                                     |
| pickle_list          | 2.70 us                                                     | 2.86 us: 1.06x slower                                                     |
| unpickle_list        | 2.59 us                                                     | 2.77 us: 1.07x slower                                                     |
| json_loads           | 13.0 us                                                     | 14.0 us: 1.08x slower                                                     |
| pickle               | 6.64 us                                                     | 7.26 us: 1.09x slower                                                     |
| unpickle             | 7.57 us                                                     | 8.50 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                       | 1.06x faster                                                              |

Benchmark hidden because not significant (2): xml_etree_process, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 22.0 ms: 1.11x slower                                                     |
| python_startup_no_site | 16.8 ms                                                     | 19.6 ms: 1.17x slower                                                     |
| Geometric mean         | (ref)                                                       | 1.14x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.22 ms: 1.45x faster                                                     |
| genshi_text     | 18.4 ms                                                     | 15.1 ms: 1.22x faster                                                     |
| genshi_xml      | 39.9 ms                                                     | 34.0 ms: 1.17x faster                                                     |
| django_template | 24.4 ms                                                     | 23.3 ms: 1.05x faster                                                     |
| Geometric mean  | (ref)                                                       | 1.22x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 70.2 us: 4.64x faster                                                     |
| generators                 | 34.0 ms                                                     | 20.0 ms: 1.70x faster                                                     |
| pylint                     | 323 ms                                                      | 195 ms: 1.65x faster                                                      |
| async_tree_none            | 332 ms                                                      | 214 ms: 1.56x faster                                                      |
| asyncio_tcp                | 726 ms                                                      | 475 ms: 1.53x faster                                                      |
| async_tree_none_tg         | 309 ms                                                      | 203 ms: 1.52x faster                                                      |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.52x faster                                                      |
| async_tree_memoization     | 399 ms                                                      | 267 ms: 1.49x faster                                                      |
| spectral_norm              | 68.3 ms                                                     | 46.1 ms: 1.48x faster                                                     |
| json_dumps                 | 8.09 ms                                                     | 5.55 ms: 1.46x faster                                                     |
| mako                       | 7.58 ms                                                     | 5.22 ms: 1.45x faster                                                     |
| comprehensions             | 15.6 us                                                     | 10.8 us: 1.45x faster                                                     |
| async_tree_io              | 808 ms                                                      | 567 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 376 ms: 1.41x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                      |
| logging_silent             | 71.8 ns                                                     | 53.1 ns: 1.35x faster                                                     |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.51 sec: 1.34x faster                                                    |
| async_tree_io_tg           | 829 ms                                                      | 619 ms: 1.34x faster                                                      |
| deltablue                  | 2.70 ms                                                     | 2.06 ms: 1.31x faster                                                     |
| chaos                      | 48.4 ms                                                     | 37.9 ms: 1.28x faster                                                     |
| scimark_monte_carlo        | 45.3 ms                                                     | 36.1 ms: 1.25x faster                                                     |
| unpickle_pure_python       | 157 us                                                      | 125 us: 1.25x faster                                                      |
| tomli_loads                | 1.46 sec                                                    | 1.17 sec: 1.25x faster                                                    |
| genshi_text                | 18.4 ms                                                     | 15.1 ms: 1.22x faster                                                     |
| sqlglot_parse              | 953 us                                                      | 779 us: 1.22x faster                                                      |
| raytrace                   | 213 ms                                                      | 176 ms: 1.21x faster                                                      |
| nbody                      | 70.3 ms                                                     | 58.3 ms: 1.21x faster                                                     |
| pickle_pure_python         | 208 us                                                      | 173 us: 1.21x faster                                                      |
| pyflate                    | 312 ms                                                      | 264 ms: 1.18x faster                                                      |
| richards_super             | 38.7 ms                                                     | 32.7 ms: 1.18x faster                                                     |
| float                      | 54.4 ms                                                     | 46.0 ms: 1.18x faster                                                     |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.19 ms: 1.17x faster                                                     |
| genshi_xml                 | 39.9 ms                                                     | 34.0 ms: 1.17x faster                                                     |
| deepcopy_memo              | 26.0 us                                                     | 22.1 us: 1.17x faster                                                     |
| sqlglot_transpile          | 1.16 ms                                                     | 995 us: 1.17x faster                                                      |
| logging_simple             | 6.86 us                                                     | 5.86 us: 1.17x faster                                                     |
| scimark_fft                | 179 ms                                                      | 153 ms: 1.17x faster                                                      |
| crypto_pyaes               | 48.9 ms                                                     | 41.9 ms: 1.17x faster                                                     |
| fannkuch                   | 253 ms                                                      | 220 ms: 1.15x faster                                                      |
| pprint_pformat             | 1.09 sec                                                    | 951 ms: 1.14x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.27 us: 1.14x faster                                                     |
| sympy_sum                  | 100 ms                                                      | 87.7 ms: 1.14x faster                                                     |
| pprint_safe_repr           | 529 ms                                                      | 466 ms: 1.14x faster                                                      |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                                     |
| nqueens                    | 68.3 ms                                                     | 60.4 ms: 1.13x faster                                                     |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.12x faster                                                     |
| dulwich_log                | 46.4 ms                                                     | 41.5 ms: 1.12x faster                                                     |
| sympy_str                  | 185 ms                                                      | 167 ms: 1.11x faster                                                      |
| chameleon                  | 5.26 ms                                                     | 4.79 ms: 1.10x faster                                                     |
| deepcopy                   | 246 us                                                      | 225 us: 1.10x faster                                                      |
| regex_compile              | 91.0 ms                                                     | 83.8 ms: 1.09x faster                                                     |
| tornado_http               | 92.8 ms                                                     | 85.5 ms: 1.09x faster                                                     |
| xml_etree_parse            | 97.6 ms                                                     | 90.1 ms: 1.08x faster                                                     |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.7 ms: 1.08x faster                                                     |
| richards                   | 31.4 ms                                                     | 29.5 ms: 1.07x faster                                                     |
| html5lib                   | 38.9 ms                                                     | 36.5 ms: 1.06x faster                                                     |
| sympy_integrate            | 14.0 ms                                                     | 13.2 ms: 1.06x faster                                                     |
| go                         | 101 ms                                                      | 95.3 ms: 1.06x faster                                                     |
| mdp                        | 1.59 sec                                                    | 1.51 sec: 1.05x faster                                                    |
| django_template            | 24.4 ms                                                     | 23.3 ms: 1.05x faster                                                     |
| bench_thread_pool          | 872 us                                                      | 833 us: 1.05x faster                                                      |
| meteor_contest             | 75.2 ms                                                     | 72.0 ms: 1.04x faster                                                     |
| deepcopy_reduce            | 2.06 us                                                     | 1.98 us: 1.04x faster                                                     |
| sympy_expand               | 299 ms                                                      | 288 ms: 1.04x faster                                                      |
| sqlglot_normalize          | 190 ms                                                      | 186 ms: 1.02x faster                                                      |
| pidigits                   | 150 ms                                                      | 146 ms: 1.02x faster                                                      |
| hexiom                     | 4.55 ms                                                     | 4.47 ms: 1.02x faster                                                     |
| mypy2                      | 459 ms                                                      | 453 ms: 1.01x faster                                                      |
| xml_etree_generate         | 52.5 ms                                                     | 53.0 ms: 1.01x slower                                                     |
| scimark_sor                | 78.1 ms                                                     | 79.3 ms: 1.01x slower                                                     |
| 2to3                       | 214 ms                                                      | 218 ms: 1.02x slower                                                      |
| regex_v8                   | 14.2 ms                                                     | 14.6 ms: 1.03x slower                                                     |
| aiohttp                    | 883 us                                                      | 909 us: 1.03x slower                                                      |
| docutils                   | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                    |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                     |
| regex_effbot               | 1.50 ms                                                     | 1.55 ms: 1.03x slower                                                     |
| sqlglot_optimize           | 34.5 ms                                                     | 35.8 ms: 1.04x slower                                                     |
| pickle_list                | 2.70 us                                                     | 2.86 us: 1.06x slower                                                     |
| bench_mp_pool              | 63.2 ms                                                     | 67.4 ms: 1.07x slower                                                     |
| unpickle_list              | 2.59 us                                                     | 2.77 us: 1.07x slower                                                     |
| json_loads                 | 13.0 us                                                     | 14.0 us: 1.08x slower                                                     |
| coverage                   | 43.4 ms                                                     | 46.7 ms: 1.08x slower                                                     |
| pathlib                    | 70.9 ms                                                     | 77.4 ms: 1.09x slower                                                     |
| pickle                     | 6.64 us                                                     | 7.26 us: 1.09x slower                                                     |
| python_startup             | 19.8 ms                                                     | 22.0 ms: 1.11x slower                                                     |
| unpickle                   | 7.57 us                                                     | 8.50 us: 1.12x slower                                                     |
| scimark_lu                 | 62.8 ms                                                     | 71.8 ms: 1.14x slower                                                     |
| telco                      | 4.06 ms                                                     | 4.69 ms: 1.15x slower                                                     |
| python_startup_no_site     | 16.8 ms                                                     | 19.6 ms: 1.17x slower                                                     |
| create_gc_cycles           | 713 us                                                      | 850 us: 1.19x slower                                                      |
| unpack_sequence            | 46.9 ns                                                     | 60.8 ns: 1.30x slower                                                     |
| async_generators           | 177 ms                                                      | 247 ms: 1.39x slower                                                      |
| thrift                     | 494 us                                                      | 9.19 ms: 18.62x slower                                                    |
| Geometric mean             | (ref)                                                       | 1.10x faster                                                              |

Benchmark hidden because not significant (5): xml_etree_process, regex_dna, pickle_dict, pycparser, json
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown
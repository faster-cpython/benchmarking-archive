# Results vs. 3.11.0

- fork: python
- ref: 05e0b67a43c5c1778dc2
- machine: windows-amd64
- commit hash: 05e0b67
- commit date: 2024-03-29
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 218 ms: 1.02x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.78 ms: 1.10x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                      |
| html5lib       | 38.9 ms                                                     | 35.8 ms: 1.08x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 84.8 ms: 1.09x faster                                                       |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 265 ms: 1.53x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 202 ms: 1.52x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 376 ms: 1.41x faster                                                        |
| async_tree_io              | 808 ms                                                      | 574 ms: 1.41x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 613 ms: 1.35x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.45x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 58.8 ms: 1.20x faster                                                       |
| float          | 54.4 ms                                                     | 47.0 ms: 1.16x faster                                                       |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.12x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 84.6 ms: 1.08x faster                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.04x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 16.4 ms: 1.16x slower                                                       |
| Geometric mean | (ref)                                                       | 1.03x slower                                                                |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.61 ms: 1.44x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 128 us: 1.22x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                      |
| pickle_pure_python   | 208 us                                                      | 175 us: 1.19x faster                                                        |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.2 ms: 1.07x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 91.6 ms: 1.07x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.6 us: 1.00x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.4 ms: 1.02x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.88 us: 1.07x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.80 us: 1.08x slower                                                       |
| pickle               | 6.64 us                                                     | 7.32 us: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.72 us: 1.15x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 22.6 ms: 1.14x slower                                                       |
| python_startup_no_site | 16.8 ms                                                     | 20.2 ms: 1.20x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.17x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.84 ms: 1.30x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 15.1 ms: 1.22x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 34.2 ms: 1.17x faster                                                       |
| django_template | 24.4 ms                                                     | 22.8 ms: 1.07x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.19x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 70.1 us: 4.65x faster                                                       |
| pylint                     | 323 ms                                                      | 190 ms: 1.70x faster                                                        |
| generators                 | 34.0 ms                                                     | 20.1 ms: 1.69x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 470 ms: 1.54x faster                                                        |
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 265 ms: 1.53x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 202 ms: 1.52x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 268 ms: 1.49x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.61 ms: 1.44x faster                                                       |
| comprehensions             | 15.6 us                                                     | 10.9 us: 1.43x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 376 ms: 1.41x faster                                                        |
| async_tree_io              | 808 ms                                                      | 574 ms: 1.41x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.47 sec: 1.38x faster                                                      |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.36x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 613 ms: 1.35x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 53.6 ns: 1.34x faster                                                       |
| spectral_norm              | 68.3 ms                                                     | 51.1 ms: 1.34x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.06 ms: 1.31x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.84 ms: 1.30x faster                                                       |
| chaos                      | 48.4 ms                                                     | 39.1 ms: 1.24x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 778 us: 1.23x faster                                                        |
| richards_super             | 38.7 ms                                                     | 31.6 ms: 1.23x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 128 us: 1.22x faster                                                        |
| genshi_text                | 18.4 ms                                                     | 15.1 ms: 1.22x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.21 sec: 1.20x faster                                                      |
| nbody                      | 70.3 ms                                                     | 58.8 ms: 1.20x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 175 us: 1.19x faster                                                        |
| raytrace                   | 213 ms                                                      | 180 ms: 1.19x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 21.9 us: 1.19x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 34.2 ms: 1.17x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1000 us: 1.16x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 12.9 ms: 1.16x faster                                                       |
| float                      | 54.4 ms                                                     | 47.0 ms: 1.16x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.96 us: 1.15x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 87.7 ms: 1.14x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.26 ms: 1.14x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.7 ms: 1.14x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.9 ms: 1.13x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.41 sec: 1.13x faster                                                      |
| logging_format             | 7.16 us                                                     | 6.37 us: 1.13x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 60.9 ms: 1.12x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.58 us: 1.12x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 43.9 ms: 1.11x faster                                                       |
| richards                   | 31.4 ms                                                     | 28.2 ms: 1.11x faster                                                       |
| pyflate                    | 312 ms                                                      | 281 ms: 1.11x faster                                                        |
| fannkuch                   | 253 ms                                                      | 228 ms: 1.11x faster                                                        |
| deepcopy                   | 246 us                                                      | 223 us: 1.11x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 479 ms: 1.10x faster                                                        |
| sympy_str                  | 185 ms                                                      | 168 ms: 1.10x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 985 ms: 1.10x faster                                                        |
| chameleon                  | 5.26 ms                                                     | 4.78 ms: 1.10x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 84.8 ms: 1.09x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 35.8 ms: 1.08x faster                                                       |
| go                         | 101 ms                                                      | 93.5 ms: 1.08x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 84.6 ms: 1.08x faster                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.2 ms: 1.07x faster                                                       |
| django_template            | 24.4 ms                                                     | 22.8 ms: 1.07x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.93 us: 1.07x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 91.6 ms: 1.07x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 13.3 ms: 1.06x faster                                                       |
| scimark_fft                | 179 ms                                                      | 171 ms: 1.05x faster                                                        |
| sympy_expand               | 299 ms                                                      | 287 ms: 1.04x faster                                                        |
| bench_thread_pool          | 872 us                                                      | 840 us: 1.04x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 184 ms: 1.03x faster                                                        |
| meteor_contest             | 75.2 ms                                                     | 73.1 ms: 1.03x faster                                                       |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                                       |
| mypy2                      | 459 ms                                                      | 452 ms: 1.02x faster                                                        |
| unpack_sequence            | 46.9 ns                                                     | 46.5 ns: 1.01x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 4.57 ms: 1.00x slower                                                       |
| pickle_dict                | 18.5 us                                                     | 18.6 us: 1.00x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 53.4 ms: 1.02x slower                                                       |
| 2to3                       | 214 ms                                                      | 218 ms: 1.02x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 35.4 ms: 1.02x slower                                                       |
| aiohttp                    | 883 us                                                      | 905 us: 1.02x slower                                                        |
| docutils                   | 1.64 sec                                                    | 1.69 sec: 1.03x slower                                                      |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 81.3 ms: 1.04x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.04x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 67.4 ms: 1.07x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.88 us: 1.07x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.80 us: 1.08x slower                                                       |
| coverage                   | 43.4 ms                                                     | 47.4 ms: 1.09x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 77.9 ms: 1.10x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.32 us: 1.10x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 70.9 ms: 1.13x slower                                                       |
| python_startup             | 19.8 ms                                                     | 22.6 ms: 1.14x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.72 us: 1.15x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.69 ms: 1.15x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 16.4 ms: 1.16x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 855 us: 1.20x slower                                                        |
| python_startup_no_site     | 16.8 ms                                                     | 20.2 ms: 1.20x slower                                                       |
| json                       | 2.98 ms                                                     | 4.10 ms: 1.38x slower                                                       |
| async_generators           | 177 ms                                                      | 247 ms: 1.40x slower                                                        |
| thrift                     | 494 us                                                      | 9.06 ms: 18.34x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.09x faster                                                                |

Benchmark hidden because not significant (2): pycparser, regex_dna
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown
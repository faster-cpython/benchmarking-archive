# Results vs. 3.11.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.03x faster
- HPT reliability: 85.95%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 222 ms: 1.04x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.90 ms: 1.07x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.75 sec: 1.07x slower                                                      |
| html5lib       | 38.9 ms                                                     | 36.9 ms: 1.05x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 83.9 ms: 1.11x faster                                                       |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 275 ms: 1.45x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 220 ms: 1.40x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                                        |
| async_tree_io              | 808 ms                                                      | 596 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 392 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 621 ms: 1.34x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| float          | 54.4 ms                                                     | 57.0 ms: 1.05x slower                                                       |
| nbody          | 70.3 ms                                                     | 79.3 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| regex_compile  | 91.0 ms                                                     | 103 ms: 1.13x slower                                                        |
| Geometric mean | (ref)                                                       | 1.08x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.66 ms: 1.43x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 182 us: 1.14x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 92.1 ms: 1.06x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 155 us: 1.01x faster                                                        |
| pickle_dict          | 18.5 us                                                     | 18.7 us: 1.01x slower                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 66.6 ms: 1.01x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.82 us: 1.05x slower                                                       |
| xml_etree_process    | 37.2 ms                                                     | 39.1 ms: 1.05x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| pickle               | 6.64 us                                                     | 7.17 us: 1.08x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 56.9 ms: 1.08x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.88 us: 1.11x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.83 us: 1.17x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.1 ms: 1.05x faster                                                       |
| Geometric mean         | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml     | 39.9 ms                                                     | 35.8 ms: 1.12x faster                                                       |
| genshi_text    | 18.4 ms                                                     | 16.7 ms: 1.11x faster                                                       |
| mako           | 7.58 ms                                                     | 7.07 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                       | 1.10x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 76.6 us: 4.26x faster                                                       |
| pylint                     | 323 ms                                                      | 198 ms: 1.63x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 479 ms: 1.52x faster                                                        |
| generators                 | 34.0 ms                                                     | 22.6 ms: 1.50x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.48x faster                                                        |
| async_tree_none            | 332 ms                                                      | 226 ms: 1.47x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 275 ms: 1.45x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.66 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 220 ms: 1.40x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                                        |
| async_tree_io              | 808 ms                                                      | 596 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 392 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 621 ms: 1.34x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 56.8 ns: 1.26x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.61 sec: 1.26x faster                                                      |
| richards_super             | 38.7 ms                                                     | 31.2 ms: 1.24x faster                                                       |
| raytrace                   | 213 ms                                                      | 175 ms: 1.22x faster                                                        |
| richards                   | 31.4 ms                                                     | 27.3 ms: 1.15x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 829 us: 1.15x faster                                                        |
| pickle_pure_python         | 208 us                                                      | 182 us: 1.14x faster                                                        |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                                       |
| comprehensions             | 15.6 us                                                     | 13.9 us: 1.13x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.14 us: 1.12x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 35.8 ms: 1.12x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 1.05 ms: 1.11x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.44 ms: 1.11x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 83.9 ms: 1.11x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 16.7 ms: 1.11x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 23.5 us: 1.10x faster                                                       |
| chaos                      | 48.4 ms                                                     | 44.2 ms: 1.09x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.62 us: 1.08x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.90 ms: 1.07x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.65 us: 1.07x faster                                                       |
| mako                       | 7.58 ms                                                     | 7.07 ms: 1.07x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 93.8 ms: 1.07x faster                                                       |
| deepcopy                   | 246 us                                                      | 231 us: 1.07x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 92.1 ms: 1.06x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 827 us: 1.05x faster                                                        |
| html5lib                   | 38.9 ms                                                     | 36.9 ms: 1.05x faster                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 16.1 ms: 1.05x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 44.3 ms: 1.05x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.01 us: 1.03x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.56 sec: 1.02x faster                                                      |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| sympy_str                  | 185 ms                                                      | 182 ms: 1.02x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 13.8 ms: 1.02x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 155 us: 1.01x faster                                                        |
| mypy2                      | 459 ms                                                      | 454 ms: 1.01x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 189 ms: 1.01x faster                                                        |
| meteor_contest             | 75.2 ms                                                     | 74.9 ms: 1.00x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 532 ms: 1.00x slower                                                        |
| pprint_pformat             | 1.09 sec                                                    | 1.09 sec: 1.01x slower                                                      |
| pickle_dict                | 18.5 us                                                     | 18.7 us: 1.01x slower                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 49.5 ms: 1.01x slower                                                       |
| xml_etree_iterparse        | 65.6 ms                                                     | 66.6 ms: 1.01x slower                                                       |
| sympy_expand               | 299 ms                                                      | 307 ms: 1.03x slower                                                        |
| bench_mp_pool              | 63.2 ms                                                     | 65.2 ms: 1.03x slower                                                       |
| aiohttp                    | 883 us                                                      | 911 us: 1.03x slower                                                        |
| 2to3                       | 214 ms                                                      | 222 ms: 1.04x slower                                                        |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| nqueens                    | 68.3 ms                                                     | 71.2 ms: 1.04x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.56 ms: 1.04x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.82 us: 1.05x slower                                                       |
| float                      | 54.4 ms                                                     | 57.0 ms: 1.05x slower                                                       |
| xml_etree_process          | 37.2 ms                                                     | 39.1 ms: 1.05x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| pyflate                    | 312 ms                                                      | 332 ms: 1.06x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 36.8 ms: 1.07x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 75.7 ms: 1.07x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.75 sec: 1.07x slower                                                      |
| coverage                   | 43.4 ms                                                     | 46.4 ms: 1.07x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.17 us: 1.08x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 49.0 ms: 1.08x slower                                                       |
| fannkuch                   | 253 ms                                                      | 274 ms: 1.08x slower                                                        |
| xml_etree_generate         | 52.5 ms                                                     | 56.9 ms: 1.08x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.88 us: 1.11x slower                                                       |
| scimark_fft                | 179 ms                                                      | 199 ms: 1.11x slower                                                        |
| nbody                      | 70.3 ms                                                     | 79.3 ms: 1.13x slower                                                       |
| regex_compile              | 91.0 ms                                                     | 103 ms: 1.13x slower                                                        |
| hexiom                     | 4.55 ms                                                     | 5.19 ms: 1.14x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 89.4 ms: 1.14x slower                                                       |
| spectral_norm              | 68.3 ms                                                     | 79.0 ms: 1.16x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.83 us: 1.17x slower                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 3.08 ms: 1.20x slower                                                       |
| telco                      | 4.06 ms                                                     | 5.03 ms: 1.24x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 78.6 ms: 1.25x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 909 us: 1.27x slower                                                        |
| async_generators           | 177 ms                                                      | 245 ms: 1.38x slower                                                        |
| thrift                     | 494 us                                                      | 9.24 ms: 18.72x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (5): json, python_startup, tomli_loads, go, pycparser
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 85.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown
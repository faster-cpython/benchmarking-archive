# Results vs. 3.11.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 210 ms: 1.02x faster                                                        |
| chameleon      | 5.26 ms                                                     | 5.01 ms: 1.05x faster                                                       |
| html5lib       | 38.9 ms                                                     | 36.2 ms: 1.07x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 82.2 ms: 1.13x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 268 ms: 1.51x faster                                                        |
| async_tree_none            | 332 ms                                                      | 224 ms: 1.48x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 272 ms: 1.47x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 222 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 386 ms: 1.36x faster                                                        |
| async_tree_io              | 808 ms                                                      | 597 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 394 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 620 ms: 1.34x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 51.6 ms: 1.05x faster                                                       |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.02x faster                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 79.8 ms: 1.14x faster                                                       |
| regex_dna      | 116 ms                                                      | 122 ms: 1.05x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 16.0 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.64 ms: 1.43x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 129 us: 1.22x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 179 us: 1.16x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 91.2 ms: 1.07x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.41 sec: 1.03x faster                                                      |
| xml_etree_iterparse  | 65.6 ms                                                     | 64.0 ms: 1.03x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.6 us: 1.00x slower                                                       |
| xml_etree_process    | 37.2 ms                                                     | 37.7 ms: 1.01x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 55.3 ms: 1.05x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| pickle               | 6.64 us                                                     | 7.14 us: 1.08x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.80 us: 1.08x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.94 us: 1.09x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.36 us: 1.10x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.03x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup | 19.8 ms                                                     | 20.3 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 6.38 ms: 1.19x faster                                                       |
| genshi_xml     | 39.9 ms                                                     | 35.6 ms: 1.12x faster                                                       |
| genshi_text    | 18.4 ms                                                     | 16.5 ms: 1.12x faster                                                       |
| Geometric mean | (ref)                                                       | 1.14x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 73.8 us: 4.42x faster                                                       |
| pylint                     | 323 ms                                                      | 188 ms: 1.72x faster                                                        |
| generators                 | 34.0 ms                                                     | 21.7 ms: 1.57x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 481 ms: 1.51x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 268 ms: 1.51x faster                                                        |
| async_tree_none            | 332 ms                                                      | 224 ms: 1.48x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 272 ms: 1.47x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.8 us: 1.45x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.64 ms: 1.43x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 222 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 386 ms: 1.36x faster                                                        |
| async_tree_io              | 808 ms                                                      | 597 ms: 1.35x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 394 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 620 ms: 1.34x faster                                                        |
| deltablue                  | 2.70 ms                                                     | 2.04 ms: 1.33x faster                                                       |
| raytrace                   | 213 ms                                                      | 165 ms: 1.29x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 56.8 ns: 1.26x faster                                                       |
| chaos                      | 48.4 ms                                                     | 39.2 ms: 1.23x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 776 us: 1.23x faster                                                        |
| unpickle_pure_python       | 157 us                                                      | 129 us: 1.22x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.68 sec: 1.21x faster                                                      |
| richards_super             | 38.7 ms                                                     | 32.3 ms: 1.20x faster                                                       |
| mako                       | 7.58 ms                                                     | 6.38 ms: 1.19x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 982 us: 1.19x faster                                                        |
| hexiom                     | 4.55 ms                                                     | 3.87 ms: 1.18x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 85.4 ms: 1.17x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 22.3 us: 1.17x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 179 us: 1.16x faster                                                        |
| dulwich_log                | 46.4 ms                                                     | 40.3 ms: 1.15x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.98 us: 1.15x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 79.8 ms: 1.14x faster                                                       |
| sympy_str                  | 185 ms                                                      | 163 ms: 1.14x faster                                                        |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 82.2 ms: 1.13x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 60.8 ms: 1.12x faster                                                       |
| go                         | 101 ms                                                      | 90.0 ms: 1.12x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 35.6 ms: 1.12x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 40.6 ms: 1.12x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.42 us: 1.12x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 16.5 ms: 1.12x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 12.6 ms: 1.11x faster                                                       |
| deepcopy                   | 246 us                                                      | 222 us: 1.11x faster                                                        |
| richards                   | 31.4 ms                                                     | 28.3 ms: 1.11x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 57.0 ms: 1.10x faster                                                       |
| mypy2                      | 459 ms                                                      | 418 ms: 1.10x faster                                                        |
| sympy_expand               | 299 ms                                                      | 274 ms: 1.09x faster                                                        |
| pprint_pformat             | 1.09 sec                                                    | 1.00 sec: 1.09x faster                                                      |
| pyflate                    | 312 ms                                                      | 289 ms: 1.08x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 63.3 ms: 1.08x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 491 ms: 1.08x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.64 us: 1.08x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 811 us: 1.08x faster                                                        |
| mdp                        | 1.59 sec                                                    | 1.49 sec: 1.07x faster                                                      |
| html5lib                   | 38.9 ms                                                     | 36.2 ms: 1.07x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 91.2 ms: 1.07x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 45.7 ms: 1.07x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 179 ms: 1.06x faster                                                        |
| float                      | 54.4 ms                                                     | 51.6 ms: 1.05x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 5.01 ms: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 72.8 ms: 1.03x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.41 sec: 1.03x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 64.0 ms: 1.03x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 2.02 us: 1.02x faster                                                       |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| scimark_sor                | 78.1 ms                                                     | 76.6 ms: 1.02x faster                                                       |
| 2to3                       | 214 ms                                                      | 210 ms: 1.02x faster                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 34.0 ms: 1.02x faster                                                       |
| pickle_dict                | 18.5 us                                                     | 18.6 us: 1.00x slower                                                       |
| xml_etree_process          | 37.2 ms                                                     | 37.7 ms: 1.01x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 64.2 ms: 1.02x slower                                                       |
| fannkuch                   | 253 ms                                                      | 257 ms: 1.02x slower                                                        |
| python_startup             | 19.8 ms                                                     | 20.3 ms: 1.02x slower                                                       |
| scimark_fft                | 179 ms                                                      | 185 ms: 1.03x slower                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.66 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| regex_dna                  | 116 ms                                                      | 122 ms: 1.05x slower                                                        |
| xml_etree_generate         | 52.5 ms                                                     | 55.3 ms: 1.05x slower                                                       |
| coverage                   | 43.4 ms                                                     | 46.0 ms: 1.06x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 75.2 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                       |
| pycparser                  | 720 ms                                                      | 772 ms: 1.07x slower                                                        |
| pickle                     | 6.64 us                                                     | 7.14 us: 1.08x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.80 us: 1.08x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.94 us: 1.09x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.36 us: 1.10x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 16.0 ms: 1.13x slower                                                       |
| telco                      | 4.06 ms                                                     | 5.05 ms: 1.24x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 895 us: 1.25x slower                                                        |
| async_generators           | 177 ms                                                      | 235 ms: 1.33x slower                                                        |
| thrift                     | 494 us                                                      | 8.03 ms: 16.27x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                                |

Benchmark hidden because not significant (5): nbody, docutils, aiohttp, python_startup_no_site, json
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown
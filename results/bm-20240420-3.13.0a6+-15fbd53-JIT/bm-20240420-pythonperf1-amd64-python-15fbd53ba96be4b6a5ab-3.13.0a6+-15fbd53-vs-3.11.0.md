# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-amd64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 216 ms: 1.01x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.69 ms: 1.12x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.67 sec: 1.02x slower                                                      |
| html5lib       | 38.9 ms                                                     | 37.3 ms: 1.04x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 81.7 ms: 1.14x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 255 ms: 1.58x faster                                                        |
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 263 ms: 1.51x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 211 ms: 1.47x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 383 ms: 1.38x faster                                                        |
| async_tree_io              | 808 ms                                                      | 585 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.45x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 58.2 ms: 1.21x faster                                                       |
| float          | 54.4 ms                                                     | 46.6 ms: 1.17x faster                                                       |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 84.3 ms: 1.08x faster                                                       |
| regex_dna      | 116 ms                                                      | 117 ms: 1.01x slower                                                        |
| regex_v8       | 14.2 ms                                                     | 14.7 ms: 1.03x slower                                                       |
| regex_effbot   | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.56 ms: 1.46x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 124 us: 1.27x faster                                                        |
| tomli_loads          | 1.46 sec                                                    | 1.17 sec: 1.24x faster                                                      |
| pickle_pure_python   | 208 us                                                      | 171 us: 1.22x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 89.7 ms: 1.09x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.5 ms: 1.08x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.0 ms: 1.03x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 52.2 ms: 1.01x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 18.6 us: 1.01x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.6 us: 1.05x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.74 us: 1.06x slower                                                       |
| pickle               | 6.64 us                                                     | 7.41 us: 1.12x slower                                                       |
| pickle_list          | 2.70 us                                                     | 3.02 us: 1.12x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.67 us: 1.15x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.06x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 17.9 ms: 1.06x slower                                                       |
| python_startup         | 19.8 ms                                                     | 21.5 ms: 1.09x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.08x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.58 ms: 1.36x faster                                                       |
| genshi_xml      | 39.9 ms                                                     | 32.7 ms: 1.22x faster                                                       |
| genshi_text     | 18.4 ms                                                     | 15.1 ms: 1.22x faster                                                       |
| django_template | 24.4 ms                                                     | 21.5 ms: 1.14x faster                                                       |
| Geometric mean  | (ref)                                                       | 1.23x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1-amd64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 70.1 us: 4.65x faster                                                       |
| generators                 | 34.0 ms                                                     | 19.5 ms: 1.74x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 255 ms: 1.58x faster                                                        |
| async_tree_none            | 332 ms                                                      | 216 ms: 1.54x faster                                                        |
| pylint                     | 323 ms                                                      | 213 ms: 1.52x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 477 ms: 1.52x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 263 ms: 1.51x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.6 us: 1.48x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 211 ms: 1.47x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.56 ms: 1.46x faster                                                       |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 383 ms: 1.38x faster                                                        |
| async_tree_io              | 808 ms                                                      | 585 ms: 1.38x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 381 ms: 1.37x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 50.0 ms: 1.37x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.58 ms: 1.36x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 53.5 ns: 1.34x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.52 sec: 1.33x faster                                                      |
| raytrace                   | 213 ms                                                      | 161 ms: 1.32x faster                                                        |
| deltablue                  | 2.70 ms                                                     | 2.12 ms: 1.27x faster                                                       |
| unpickle_pure_python       | 157 us                                                      | 124 us: 1.27x faster                                                        |
| chaos                      | 48.4 ms                                                     | 38.2 ms: 1.27x faster                                                       |
| richards_super             | 38.7 ms                                                     | 30.9 ms: 1.25x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.17 sec: 1.24x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 772 us: 1.23x faster                                                        |
| deepcopy_memo              | 26.0 us                                                     | 21.2 us: 1.22x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 32.7 ms: 1.22x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 15.1 ms: 1.22x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 171 us: 1.22x faster                                                        |
| nbody                      | 70.3 ms                                                     | 58.2 ms: 1.21x faster                                                       |
| logging_simple             | 6.86 us                                                     | 5.69 us: 1.21x faster                                                       |
| pyflate                    | 312 ms                                                      | 264 ms: 1.18x faster                                                        |
| sqlglot_transpile          | 1.16 ms                                                     | 985 us: 1.18x faster                                                        |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.6 ms: 1.17x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 39.5 ms: 1.17x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.21 ms: 1.17x faster                                                       |
| float                      | 54.4 ms                                                     | 46.6 ms: 1.17x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.16 us: 1.16x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 935 ms: 1.16x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 457 ms: 1.16x faster                                                        |
| deepcopy                   | 246 us                                                      | 215 us: 1.15x faster                                                        |
| richards                   | 31.4 ms                                                     | 27.4 ms: 1.15x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 42.8 ms: 1.14x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 87.9 ms: 1.14x faster                                                       |
| django_template            | 24.4 ms                                                     | 21.5 ms: 1.14x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 81.7 ms: 1.14x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.14x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 60.4 ms: 1.13x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.69 ms: 1.12x faster                                                       |
| sympy_str                  | 185 ms                                                      | 166 ms: 1.11x faster                                                        |
| go                         | 101 ms                                                      | 91.0 ms: 1.11x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 787 us: 1.11x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.61 us: 1.10x faster                                                       |
| fannkuch                   | 253 ms                                                      | 231 ms: 1.09x faster                                                        |
| xml_etree_parse            | 97.6 ms                                                     | 89.7 ms: 1.09x faster                                                       |
| scimark_fft                | 179 ms                                                      | 165 ms: 1.09x faster                                                        |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.5 ms: 1.08x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 84.3 ms: 1.08x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.91 us: 1.08x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.48 sec: 1.08x faster                                                      |
| sympy_integrate            | 14.0 ms                                                     | 13.2 ms: 1.06x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 180 ms: 1.06x faster                                                        |
| sympy_expand               | 299 ms                                                      | 285 ms: 1.05x faster                                                        |
| hexiom                     | 4.55 ms                                                     | 4.35 ms: 1.05x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 37.3 ms: 1.04x faster                                                       |
| mypy2                      | 459 ms                                                      | 441 ms: 1.04x faster                                                        |
| pycparser                  | 720 ms                                                      | 692 ms: 1.04x faster                                                        |
| xml_etree_process          | 37.2 ms                                                     | 36.0 ms: 1.03x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 72.9 ms: 1.03x faster                                                       |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| xml_etree_generate         | 52.5 ms                                                     | 52.2 ms: 1.01x faster                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 34.7 ms: 1.01x slower                                                       |
| regex_dna                  | 116 ms                                                      | 117 ms: 1.01x slower                                                        |
| pickle_dict                | 18.5 us                                                     | 18.6 us: 1.01x slower                                                       |
| 2to3                       | 214 ms                                                      | 216 ms: 1.01x slower                                                        |
| docutils                   | 1.64 sec                                                    | 1.67 sec: 1.02x slower                                                      |
| scimark_sor                | 78.1 ms                                                     | 80.2 ms: 1.03x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 14.7 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.57 ms: 1.05x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.6 us: 1.05x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.74 us: 1.06x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 67.2 ms: 1.06x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 17.9 ms: 1.06x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 76.0 ms: 1.07x slower                                                       |
| python_startup             | 19.8 ms                                                     | 21.5 ms: 1.09x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.41 us: 1.12x slower                                                       |
| pickle_list                | 2.70 us                                                     | 3.02 us: 1.12x slower                                                       |
| coverage                   | 43.4 ms                                                     | 48.9 ms: 1.13x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.67 us: 1.15x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.76 ms: 1.17x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 75.0 ms: 1.19x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 891 us: 1.25x slower                                                        |
| async_generators           | 177 ms                                                      | 235 ms: 1.33x slower                                                        |
| thrift                     | 494 us                                                      | 8.70 ms: 17.62x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                                |

Benchmark hidden because not significant (2): aiohttp, json
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown
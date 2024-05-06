# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-amd64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| chameleon      | 5.26 ms                                                     | 4.97 ms: 1.06x faster                                                               |
| html5lib       | 38.9 ms                                                     | 35.6 ms: 1.09x faster                                                               |
| tornado_http   | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                                               |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                        |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 271 ms: 1.49x faster                                                                |
| async_tree_none            | 332 ms                                                      | 224 ms: 1.48x faster                                                                |
| async_tree_memoization     | 399 ms                                                      | 274 ms: 1.45x faster                                                                |
| async_tree_none_tg         | 309 ms                                                      | 220 ms: 1.40x faster                                                                |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 387 ms: 1.35x faster                                                                |
| async_tree_io              | 808 ms                                                      | 597 ms: 1.35x faster                                                                |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 394 ms: 1.34x faster                                                                |
| async_tree_io_tg           | 829 ms                                                      | 619 ms: 1.34x faster                                                                |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 51.7 ms: 1.05x faster                                                               |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                                |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                        |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 80.5 ms: 1.13x faster                                                               |
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                                                |
| regex_effbot   | 1.50 ms                                                     | 1.61 ms: 1.08x slower                                                               |
| regex_v8       | 14.2 ms                                                     | 16.1 ms: 1.13x slower                                                               |
| Geometric mean | (ref)                                                       | 1.03x slower                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.66 ms: 1.43x faster                                                               |
| unpickle_pure_python | 157 us                                                      | 133 us: 1.18x faster                                                                |
| pickle_pure_python   | 208 us                                                      | 184 us: 1.13x faster                                                                |
| xml_etree_parse      | 97.6 ms                                                     | 90.2 ms: 1.08x faster                                                               |
| tomli_loads          | 1.46 sec                                                    | 1.40 sec: 1.04x faster                                                              |
| xml_etree_iterparse  | 65.6 ms                                                     | 63.9 ms: 1.03x faster                                                               |
| pickle_dict          | 18.5 us                                                     | 18.8 us: 1.02x slower                                                               |
| xml_etree_process    | 37.2 ms                                                     | 37.9 ms: 1.02x slower                                                               |
| xml_etree_generate   | 52.5 ms                                                     | 55.0 ms: 1.05x slower                                                               |
| json_loads           | 13.0 us                                                     | 13.8 us: 1.06x slower                                                               |
| unpickle_list        | 2.59 us                                                     | 2.76 us: 1.07x slower                                                               |
| pickle_list          | 2.70 us                                                     | 2.92 us: 1.08x slower                                                               |
| pickle               | 6.64 us                                                     | 7.24 us: 1.09x slower                                                               |
| unpickle             | 7.57 us                                                     | 8.49 us: 1.12x slower                                                               |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.3 ms: 1.03x faster                                                               |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                                        |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| genshi_xml      | 39.9 ms                                                     | 33.6 ms: 1.19x faster                                                               |
| genshi_text     | 18.4 ms                                                     | 15.8 ms: 1.17x faster                                                               |
| mako            | 7.58 ms                                                     | 6.56 ms: 1.16x faster                                                               |
| django_template | 24.4 ms                                                     | 22.5 ms: 1.09x faster                                                               |
| Geometric mean  | (ref)                                                       | 1.15x faster                                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:-----------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 74.8 us: 4.36x faster                                                               |
| generators                 | 34.0 ms                                                     | 21.0 ms: 1.62x faster                                                               |
| pylint                     | 323 ms                                                      | 209 ms: 1.55x faster                                                                |
| asyncio_tcp                | 726 ms                                                      | 480 ms: 1.51x faster                                                                |
| async_tree_memoization_tg  | 405 ms                                                      | 271 ms: 1.49x faster                                                                |
| async_tree_none            | 332 ms                                                      | 224 ms: 1.48x faster                                                                |
| async_tree_memoization     | 399 ms                                                      | 274 ms: 1.45x faster                                                                |
| json_dumps                 | 8.09 ms                                                     | 5.66 ms: 1.43x faster                                                               |
| async_tree_none_tg         | 309 ms                                                      | 220 ms: 1.40x faster                                                                |
| comprehensions             | 15.6 us                                                     | 11.2 us: 1.40x faster                                                               |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 387 ms: 1.35x faster                                                                |
| async_tree_io              | 808 ms                                                      | 597 ms: 1.35x faster                                                                |
| deltablue                  | 2.70 ms                                                     | 2.00 ms: 1.35x faster                                                               |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 394 ms: 1.34x faster                                                                |
| async_tree_io_tg           | 829 ms                                                      | 619 ms: 1.34x faster                                                                |
| raytrace                   | 213 ms                                                      | 160 ms: 1.34x faster                                                                |
| logging_silent             | 71.8 ns                                                     | 56.4 ns: 1.27x faster                                                               |
| richards_super             | 38.7 ms                                                     | 30.5 ms: 1.27x faster                                                               |
| sqlglot_parse              | 953 us                                                      | 760 us: 1.25x faster                                                                |
| chaos                      | 48.4 ms                                                     | 39.0 ms: 1.24x faster                                                               |
| sqlglot_transpile          | 1.16 ms                                                     | 968 us: 1.20x faster                                                                |
| mdp                        | 1.59 sec                                                    | 1.34 sec: 1.19x faster                                                              |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.70 sec: 1.19x faster                                                              |
| genshi_xml                 | 39.9 ms                                                     | 33.6 ms: 1.19x faster                                                               |
| unpickle_pure_python       | 157 us                                                      | 133 us: 1.18x faster                                                                |
| sympy_sum                  | 100 ms                                                      | 85.0 ms: 1.18x faster                                                               |
| richards                   | 31.4 ms                                                     | 26.7 ms: 1.18x faster                                                               |
| go                         | 101 ms                                                      | 86.1 ms: 1.17x faster                                                               |
| genshi_text                | 18.4 ms                                                     | 15.8 ms: 1.17x faster                                                               |
| hexiom                     | 4.55 ms                                                     | 3.90 ms: 1.17x faster                                                               |
| logging_simple             | 6.86 us                                                     | 5.94 us: 1.16x faster                                                               |
| mako                       | 7.58 ms                                                     | 6.56 ms: 1.16x faster                                                               |
| dulwich_log                | 46.4 ms                                                     | 40.5 ms: 1.15x faster                                                               |
| nqueens                    | 68.3 ms                                                     | 60.0 ms: 1.14x faster                                                               |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.14x faster                                                               |
| tornado_http               | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                                               |
| regex_compile              | 91.0 ms                                                     | 80.5 ms: 1.13x faster                                                               |
| pickle_pure_python         | 208 us                                                      | 184 us: 1.13x faster                                                                |
| deepcopy_memo              | 26.0 us                                                     | 23.0 us: 1.13x faster                                                               |
| logging_format             | 7.16 us                                                     | 6.35 us: 1.13x faster                                                               |
| sympy_str                  | 185 ms                                                      | 165 ms: 1.12x faster                                                                |
| sympy_integrate            | 14.0 ms                                                     | 12.6 ms: 1.11x faster                                                               |
| deepcopy                   | 246 us                                                      | 223 us: 1.10x faster                                                                |
| pprint_pformat             | 1.09 sec                                                    | 986 ms: 1.10x faster                                                                |
| html5lib                   | 38.9 ms                                                     | 35.6 ms: 1.09x faster                                                               |
| pprint_safe_repr           | 529 ms                                                      | 486 ms: 1.09x faster                                                                |
| django_template            | 24.4 ms                                                     | 22.5 ms: 1.09x faster                                                               |
| scimark_lu                 | 62.8 ms                                                     | 57.9 ms: 1.09x faster                                                               |
| mypy2                      | 459 ms                                                      | 424 ms: 1.08x faster                                                                |
| xml_etree_parse            | 97.6 ms                                                     | 90.2 ms: 1.08x faster                                                               |
| bench_thread_pool          | 872 us                                                      | 810 us: 1.08x faster                                                                |
| sqlglot_normalize          | 190 ms                                                      | 177 ms: 1.07x faster                                                                |
| spectral_norm              | 68.3 ms                                                     | 64.1 ms: 1.07x faster                                                               |
| sqlite_synth               | 1.77 us                                                     | 1.66 us: 1.07x faster                                                               |
| sympy_expand               | 299 ms                                                      | 281 ms: 1.07x faster                                                                |
| pyflate                    | 312 ms                                                      | 295 ms: 1.06x faster                                                                |
| chameleon                  | 5.26 ms                                                     | 4.97 ms: 1.06x faster                                                               |
| crypto_pyaes               | 48.9 ms                                                     | 46.2 ms: 1.06x faster                                                               |
| float                      | 54.4 ms                                                     | 51.7 ms: 1.05x faster                                                               |
| tomli_loads                | 1.46 sec                                                    | 1.40 sec: 1.04x faster                                                              |
| pycparser                  | 720 ms                                                      | 696 ms: 1.03x faster                                                                |
| python_startup_no_site     | 16.8 ms                                                     | 16.3 ms: 1.03x faster                                                               |
| scimark_monte_carlo        | 45.3 ms                                                     | 44.1 ms: 1.03x faster                                                               |
| xml_etree_iterparse        | 65.6 ms                                                     | 63.9 ms: 1.03x faster                                                               |
| sqlglot_optimize           | 34.5 ms                                                     | 33.8 ms: 1.02x faster                                                               |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                                |
| meteor_contest             | 75.2 ms                                                     | 74.3 ms: 1.01x faster                                                               |
| deepcopy_reduce            | 2.06 us                                                     | 2.04 us: 1.01x faster                                                               |
| scimark_sor                | 78.1 ms                                                     | 77.5 ms: 1.01x faster                                                               |
| bench_mp_pool              | 63.2 ms                                                     | 64.0 ms: 1.01x slower                                                               |
| pickle_dict                | 18.5 us                                                     | 18.8 us: 1.02x slower                                                               |
| xml_etree_process          | 37.2 ms                                                     | 37.9 ms: 1.02x slower                                                               |
| fannkuch                   | 253 ms                                                      | 259 ms: 1.02x slower                                                                |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                               |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                                                |
| xml_etree_generate         | 52.5 ms                                                     | 55.0 ms: 1.05x slower                                                               |
| scimark_fft                | 179 ms                                                      | 189 ms: 1.05x slower                                                                |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.72 ms: 1.05x slower                                                               |
| json_loads                 | 13.0 us                                                     | 13.8 us: 1.06x slower                                                               |
| unpickle_list              | 2.59 us                                                     | 2.76 us: 1.07x slower                                                               |
| regex_effbot               | 1.50 ms                                                     | 1.61 ms: 1.08x slower                                                               |
| pathlib                    | 70.9 ms                                                     | 76.5 ms: 1.08x slower                                                               |
| pickle_list                | 2.70 us                                                     | 2.92 us: 1.08x slower                                                               |
| pickle                     | 6.64 us                                                     | 7.24 us: 1.09x slower                                                               |
| coverage                   | 43.4 ms                                                     | 48.1 ms: 1.11x slower                                                               |
| unpickle                   | 7.57 us                                                     | 8.49 us: 1.12x slower                                                               |
| regex_v8                   | 14.2 ms                                                     | 16.1 ms: 1.13x slower                                                               |
| create_gc_cycles           | 713 us                                                      | 888 us: 1.25x slower                                                                |
| telco                      | 4.06 ms                                                     | 5.18 ms: 1.27x slower                                                               |
| async_generators           | 177 ms                                                      | 240 ms: 1.36x slower                                                                |
| thrift                     | 494 us                                                      | 8.32 ms: 16.85x slower                                                              |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                                        |

Benchmark hidden because not significant (6): json, nbody, 2to3, aiohttp, python_startup, docutils
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown
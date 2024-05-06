# Results vs. 3.12.0

- fork: faster-cpython
- ref: dynamic_underflow
- machine: linux-x86_64
- commit hash: b73d4ab
- commit date: 2024-05-03
- overall geometric mean: 1.21x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 0.92x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| chameleon      | 7.23 ms                                                      | 8.91 ms: 1.23x slower                                                               |
| tornado_http   | 121 ms                                                       | 139 ms: 1.15x slower                                                                |
| Geometric mean | (ref)                                                        | 1.19x slower                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 451 ms: 1.20x faster                                                                |
| async_tree_none_tg         | 431 ms                                                       | 363 ms: 1.19x faster                                                                |
| async_tree_io_tg           | 1.05 sec                                                     | 922 ms: 1.14x faster                                                                |
| async_tree_none            | 452 ms                                                       | 399 ms: 1.13x faster                                                                |
| async_tree_io              | 1.04 sec                                                     | 921 ms: 1.13x faster                                                                |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 618 ms: 1.13x faster                                                                |
| async_tree_memoization     | 544 ms                                                       | 502 ms: 1.08x faster                                                                |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 649 ms: 1.07x faster                                                                |
| Geometric mean             | (ref)                                                        | 1.13x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 256 ms: 1.04x faster                                                                |
| float          | 76.6 ms                                                      | 98.7 ms: 1.29x slower                                                               |
| nbody          | 88.0 ms                                                      | 129 ms: 1.46x slower                                                                |
| Geometric mean | (ref)                                                        | 1.22x slower                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.52 ms: 1.01x faster                                                               |
| regex_dna      | 239 ms                                                       | 242 ms: 1.01x slower                                                                |
| regex_v8       | 23.6 ms                                                      | 26.3 ms: 1.11x slower                                                               |
| regex_compile  | 144 ms                                                       | 231 ms: 1.60x slower                                                                |
| Geometric mean | (ref)                                                        | 1.16x slower                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| pickle_list          | 4.43 us                                                      | 4.37 us: 1.01x faster                                                               |
| pickle_dict          | 32.5 us                                                      | 32.7 us: 1.00x slower                                                               |
| xml_etree_parse      | 144 ms                                                       | 146 ms: 1.01x slower                                                                |
| pickle               | 10.5 us                                                      | 10.7 us: 1.02x slower                                                               |
| json_loads           | 24.4 us                                                      | 25.1 us: 1.03x slower                                                               |
| unpickle             | 14.8 us                                                      | 15.2 us: 1.03x slower                                                               |
| unpickle_list        | 4.66 us                                                      | 4.80 us: 1.03x slower                                                               |
| json_dumps           | 10.2 ms                                                      | 11.4 ms: 1.12x slower                                                               |
| xml_etree_iterparse  | 103 ms                                                       | 116 ms: 1.13x slower                                                                |
| xml_etree_generate   | 86.1 ms                                                      | 97.6 ms: 1.13x slower                                                               |
| xml_etree_process    | 58.4 ms                                                      | 69.2 ms: 1.19x slower                                                               |
| pickle_pure_python   | 318 us                                                       | 479 us: 1.50x slower                                                                |
| tomli_loads          | 2.16 sec                                                     | 3.32 sec: 1.54x slower                                                              |
| unpickle_pure_python | 210 us                                                       | 335 us: 1.60x slower                                                                |
| Geometric mean       | (ref)                                                        | 1.15x slower                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 8.93 ms: 1.03x slower                                                               |
| python_startup         | 11.6 ms                                                      | 13.0 ms: 1.12x slower                                                               |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 46.8 ms: 1.23x slower                                                               |
| mako            | 10.0 ms                                                      | 14.2 ms: 1.42x slower                                                               |
| Geometric mean  | (ref)                                                        | 1.32x slower                                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 451 ms: 1.20x faster                                                                |
| async_tree_none_tg         | 431 ms                                                       | 363 ms: 1.19x faster                                                                |
| async_tree_io_tg           | 1.05 sec                                                     | 922 ms: 1.14x faster                                                                |
| async_tree_none            | 452 ms                                                       | 399 ms: 1.13x faster                                                                |
| async_tree_io              | 1.04 sec                                                     | 921 ms: 1.13x faster                                                                |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 618 ms: 1.13x faster                                                                |
| generators                 | 37.4 ms                                                      | 34.2 ms: 1.09x faster                                                               |
| async_tree_memoization     | 544 ms                                                       | 502 ms: 1.08x faster                                                                |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 649 ms: 1.07x faster                                                                |
| pidigits                   | 265 ms                                                       | 256 ms: 1.04x faster                                                                |
| coroutines                 | 23.0 ms                                                      | 22.5 ms: 1.02x faster                                                               |
| pathlib                    | 18.9 ms                                                      | 18.5 ms: 1.02x faster                                                               |
| regex_effbot               | 3.57 ms                                                      | 3.52 ms: 1.01x faster                                                               |
| pickle_list                | 4.43 us                                                      | 4.37 us: 1.01x faster                                                               |
| pickle_dict                | 32.5 us                                                      | 32.7 us: 1.00x slower                                                               |
| asyncio_websockets         | 387 ms                                                       | 390 ms: 1.01x slower                                                                |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.61 sec: 1.01x slower                                                              |
| regex_dna                  | 239 ms                                                       | 242 ms: 1.01x slower                                                                |
| xml_etree_parse            | 144 ms                                                       | 146 ms: 1.01x slower                                                                |
| logging_simple             | 6.71 us                                                      | 6.81 us: 1.01x slower                                                               |
| pickle                     | 10.5 us                                                      | 10.7 us: 1.02x slower                                                               |
| async_generators           | 390 ms                                                       | 398 ms: 1.02x slower                                                                |
| json_loads                 | 24.4 us                                                      | 25.1 us: 1.03x slower                                                               |
| unpickle                   | 14.8 us                                                      | 15.2 us: 1.03x slower                                                               |
| unpickle_list              | 4.66 us                                                      | 4.80 us: 1.03x slower                                                               |
| bench_mp_pool              | 4.76 ms                                                      | 4.92 ms: 1.03x slower                                                               |
| python_startup_no_site     | 8.64 ms                                                      | 8.93 ms: 1.03x slower                                                               |
| asyncio_tcp                | 378 ms                                                       | 392 ms: 1.04x slower                                                                |
| sqlite_synth               | 2.77 us                                                      | 2.95 us: 1.06x slower                                                               |
| mdp                        | 2.57 sec                                                     | 2.77 sec: 1.08x slower                                                              |
| json                       | 5.12 ms                                                      | 5.53 ms: 1.08x slower                                                               |
| bench_thread_pool          | 950 us                                                       | 1.05 ms: 1.11x slower                                                               |
| regex_v8                   | 23.6 ms                                                      | 26.3 ms: 1.11x slower                                                               |
| json_dumps                 | 10.2 ms                                                      | 11.4 ms: 1.12x slower                                                               |
| python_startup             | 11.6 ms                                                      | 13.0 ms: 1.12x slower                                                               |
| dask                       | 392 ms                                                       | 441 ms: 1.13x slower                                                                |
| xml_etree_iterparse        | 103 ms                                                       | 116 ms: 1.13x slower                                                                |
| xml_etree_generate         | 86.1 ms                                                      | 97.6 ms: 1.13x slower                                                               |
| tornado_http               | 121 ms                                                       | 139 ms: 1.15x slower                                                                |
| meteor_contest             | 128 ms                                                       | 148 ms: 1.16x slower                                                                |
| crypto_pyaes               | 80.3 ms                                                      | 92.9 ms: 1.16x slower                                                               |
| xml_etree_process          | 58.4 ms                                                      | 69.2 ms: 1.19x slower                                                               |
| mypy2                      | 830 ms                                                       | 1.01 sec: 1.22x slower                                                              |
| coverage                   | 66.7 ms                                                      | 81.6 ms: 1.22x slower                                                               |
| pycparser                  | 1.23 sec                                                     | 1.51 sec: 1.22x slower                                                              |
| raytrace                   | 298 ms                                                       | 365 ms: 1.22x slower                                                                |
| django_template            | 38.2 ms                                                      | 46.8 ms: 1.23x slower                                                               |
| deepcopy_reduce            | 3.37 us                                                      | 4.14 us: 1.23x slower                                                               |
| chameleon                  | 7.23 ms                                                      | 8.91 ms: 1.23x slower                                                               |
| gunicorn                   | 1.00 ms                                                      | 1.26 ms: 1.26x slower                                                               |
| create_gc_cycles           | 1.59 ms                                                      | 2.01 ms: 1.26x slower                                                               |
| sympy_integrate            | 23.9 ms                                                      | 30.4 ms: 1.27x slower                                                               |
| aiohttp                    | 1.02 ms                                                      | 1.30 ms: 1.27x slower                                                               |
| sqlglot_transpile          | 1.78 ms                                                      | 2.26 ms: 1.27x slower                                                               |
| sqlglot_parse              | 1.38 ms                                                      | 1.76 ms: 1.28x slower                                                               |
| sympy_sum                  | 162 ms                                                       | 208 ms: 1.28x slower                                                                |
| gc_traversal               | 3.48 ms                                                      | 4.47 ms: 1.28x slower                                                               |
| float                      | 76.6 ms                                                      | 98.7 ms: 1.29x slower                                                               |
| comprehensions             | 21.9 us                                                      | 28.3 us: 1.29x slower                                                               |
| sqlglot_optimize           | 57.5 ms                                                      | 74.3 ms: 1.29x slower                                                               |
| chaos                      | 64.0 ms                                                      | 83.5 ms: 1.30x slower                                                               |
| sqlglot_normalize          | 116 ms                                                       | 153 ms: 1.32x slower                                                                |
| nqueens                    | 89.9 ms                                                      | 120 ms: 1.34x slower                                                                |
| telco                      | 6.96 ms                                                      | 9.35 ms: 1.34x slower                                                               |
| deepcopy                   | 368 us                                                       | 495 us: 1.34x slower                                                                |
| typing_runtime_protocols   | 152 us                                                       | 204 us: 1.35x slower                                                                |
| sympy_str                  | 302 ms                                                       | 410 ms: 1.36x slower                                                                |
| dulwich_log                | 65.4 ms                                                      | 88.7 ms: 1.36x slower                                                               |
| pprint_safe_repr           | 807 ms                                                       | 1.10 sec: 1.36x slower                                                              |
| pprint_pformat             | 1.65 sec                                                     | 2.25 sec: 1.36x slower                                                              |
| sympy_expand               | 484 ms                                                       | 685 ms: 1.42x slower                                                                |
| mako                       | 10.0 ms                                                      | 14.2 ms: 1.42x slower                                                               |
| fannkuch                   | 350 ms                                                       | 498 ms: 1.42x slower                                                                |
| go                         | 150 ms                                                       | 216 ms: 1.44x slower                                                                |
| pyflate                    | 439 ms                                                       | 632 ms: 1.44x slower                                                                |
| scimark_fft                | 301 ms                                                       | 437 ms: 1.45x slower                                                                |
| nbody                      | 88.0 ms                                                      | 129 ms: 1.46x slower                                                                |
| pickle_pure_python         | 318 us                                                       | 479 us: 1.50x slower                                                                |
| scimark_lu                 | 98.8 ms                                                      | 149 ms: 1.51x slower                                                                |
| richards_super             | 51.3 ms                                                      | 78.3 ms: 1.52x slower                                                               |
| scimark_sor                | 109 ms                                                       | 167 ms: 1.53x slower                                                                |
| tomli_loads                | 2.16 sec                                                     | 3.32 sec: 1.54x slower                                                              |
| richards                   | 45.7 ms                                                      | 70.8 ms: 1.55x slower                                                               |
| scimark_monte_carlo        | 69.0 ms                                                      | 109 ms: 1.58x slower                                                                |
| spectral_norm              | 91.6 ms                                                      | 146 ms: 1.60x slower                                                                |
| unpickle_pure_python       | 210 us                                                       | 335 us: 1.60x slower                                                                |
| regex_compile              | 144 ms                                                       | 231 ms: 1.60x slower                                                                |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 6.92 ms: 1.65x slower                                                               |
| deepcopy_memo              | 36.8 us                                                      | 62.1 us: 1.69x slower                                                               |
| hexiom                     | 5.96 ms                                                      | 10.9 ms: 1.83x slower                                                               |
| logging_silent             | 94.4 ns                                                      | 174 ns: 1.85x slower                                                                |
| deltablue                  | 3.24 ms                                                      | 6.33 ms: 1.96x slower                                                               |
| Geometric mean             | (ref)                                                        | 1.21x slower                                                                        |

Benchmark hidden because not significant (1): logging_format
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: 2to3, docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (3) of results/bm-20240503-3.13.0a6+-b73d4ab-PYTHON_UOPS/bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab.json: flaskblogging, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 0.92x
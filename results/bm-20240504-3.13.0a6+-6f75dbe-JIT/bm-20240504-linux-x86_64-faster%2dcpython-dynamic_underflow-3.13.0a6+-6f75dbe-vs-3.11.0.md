# Results vs. 3.11.0

- fork: faster-cpython
- ref: dynamic_underflow
- machine: linux-x86_64
- commit hash: 6f75dbe
- commit date: 2024-05-04
- overall geometric mean: 1.04x faster
- HPT reliability: 89.28%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 285 ms: 1.08x slower                                                          |
| chameleon      | 6.70 ms                                                | 7.31 ms: 1.09x slower                                                         |
| html5lib       | 64.8 ms                                                | 70.6 ms: 1.09x slower                                                         |
| tornado_http   | 98.1 ms                                                | 105 ms: 1.07x slower                                                          |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 371 ms: 1.42x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 354 ms: 1.39x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 453 ms: 1.38x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 931 ms: 1.38x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 474 ms: 1.35x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 968 ms: 1.34x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 615 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 639 ms: 1.17x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 79.6 ms: 1.21x faster                                                         |
| float          | 78.9 ms                                                | 73.2 ms: 1.08x faster                                                         |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                          |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 143 ms: 1.01x slower                                                          |
| regex_effbot   | 3.51 ms                                                | 3.71 ms: 1.06x slower                                                         |
| regex_v8       | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                         |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                          |
| Geometric mean | (ref)                                                  | 1.07x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.2 ms: 1.30x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 209 us: 1.16x faster                                                          |
| tomli_loads          | 2.30 sec                                               | 2.02 sec: 1.14x faster                                                        |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                          |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| json_loads           | 29.2 us                                                | 27.6 us: 1.06x faster                                                         |
| unpickle_list        | 5.21 us                                                | 5.26 us: 1.01x slower                                                         |
| pickle_dict          | 34.6 us                                                | 35.0 us: 1.01x slower                                                         |
| xml_etree_process    | 56.9 ms                                                | 58.4 ms: 1.03x slower                                                         |
| xml_etree_generate   | 81.1 ms                                                | 83.9 ms: 1.03x slower                                                         |
| pickle_list          | 4.59 us                                                | 4.92 us: 1.07x slower                                                         |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                         |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.65 ms: 1.27x slower                                                         |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.66 ms: 1.10x faster                                                         |
| genshi_text     | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                         |
| django_template | 33.5 ms                                                | 36.7 ms: 1.10x slower                                                         |
| genshi_xml      | 53.4 ms                                                | 62.7 ms: 1.17x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-linux-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 174 us: 2.99x faster                                                          |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                        |
| asyncio_tcp                | 875 ms                                                 | 530 ms: 1.65x faster                                                          |
| async_tree_none            | 528 ms                                                 | 371 ms: 1.42x faster                                                          |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 354 ms: 1.39x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 453 ms: 1.38x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 931 ms: 1.38x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 474 ms: 1.35x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 968 ms: 1.34x faster                                                          |
| json_dumps                 | 13.3 ms                                                | 10.2 ms: 1.30x faster                                                         |
| chaos                      | 71.9 ms                                                | 57.5 ms: 1.25x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 615 ms: 1.24x faster                                                          |
| nbody                      | 96.0 ms                                                | 79.6 ms: 1.21x faster                                                         |
| richards_super             | 61.9 ms                                                | 51.5 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 639 ms: 1.17x faster                                                          |
| pylint                     | 476 ms                                                 | 409 ms: 1.16x faster                                                          |
| unpickle_pure_python       | 242 us                                                 | 209 us: 1.16x faster                                                          |
| scimark_monte_carlo        | 70.7 ms                                                | 61.6 ms: 1.15x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 2.02 sec: 1.14x faster                                                        |
| logging_silent             | 111 ns                                                 | 98.0 ns: 1.13x faster                                                         |
| raytrace                   | 309 ms                                                 | 273 ms: 1.13x faster                                                          |
| mako                       | 10.7 ms                                                | 9.66 ms: 1.10x faster                                                         |
| coroutines                 | 27.0 ms                                                | 24.5 ms: 1.10x faster                                                         |
| crypto_pyaes               | 76.7 ms                                                | 69.7 ms: 1.10x faster                                                         |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                                          |
| fannkuch                   | 405 ms                                                 | 371 ms: 1.09x faster                                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                         |
| richards                   | 49.8 ms                                                | 45.9 ms: 1.09x faster                                                         |
| float                      | 78.9 ms                                                | 73.2 ms: 1.08x faster                                                         |
| spectral_norm              | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| scimark_fft                | 345 ms                                                 | 322 ms: 1.07x faster                                                          |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                          |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                                        |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.71 ms: 1.07x faster                                                         |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                          |
| json_loads                 | 29.2 us                                                | 27.6 us: 1.06x faster                                                         |
| deepcopy_memo              | 40.2 us                                                | 38.1 us: 1.06x faster                                                         |
| logging_simple             | 6.22 us                                                | 5.92 us: 1.05x faster                                                         |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                         |
| gc_traversal               | 4.01 ms                                                | 3.86 ms: 1.04x faster                                                         |
| nqueens                    | 87.9 ms                                                | 84.7 ms: 1.04x faster                                                         |
| hexiom                     | 6.89 ms                                                | 6.64 ms: 1.04x faster                                                         |
| logging_format             | 6.81 us                                                | 6.58 us: 1.04x faster                                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.70 ms: 1.03x faster                                                         |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                          |
| json                       | 5.24 ms                                                | 5.11 ms: 1.03x faster                                                         |
| go                         | 149 ms                                                 | 146 ms: 1.02x faster                                                          |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                          |
| unpickle_list              | 5.21 us                                                | 5.26 us: 1.01x slower                                                         |
| deepcopy_reduce            | 3.22 us                                                | 3.24 us: 1.01x slower                                                         |
| regex_compile              | 141 ms                                                 | 143 ms: 1.01x slower                                                          |
| pickle_dict                | 34.6 us                                                | 35.0 us: 1.01x slower                                                         |
| thrift                     | 784 us                                                 | 802 us: 1.02x slower                                                          |
| xml_etree_process          | 56.9 ms                                                | 58.4 ms: 1.03x slower                                                         |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                          |
| pyflate                    | 434 ms                                                 | 447 ms: 1.03x slower                                                          |
| xml_etree_generate         | 81.1 ms                                                | 83.9 ms: 1.03x slower                                                         |
| genshi_text                | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                         |
| dask                       | 365 ms                                                 | 383 ms: 1.05x slower                                                          |
| sqlglot_optimize           | 55.3 ms                                                | 58.2 ms: 1.05x slower                                                         |
| bench_thread_pool          | 834 us                                                 | 882 us: 1.06x slower                                                          |
| sqlglot_normalize          | 113 ms                                                 | 119 ms: 1.06x slower                                                          |
| regex_effbot               | 3.51 ms                                                | 3.71 ms: 1.06x slower                                                         |
| sympy_str                  | 297 ms                                                 | 317 ms: 1.07x slower                                                          |
| tornado_http               | 98.1 ms                                                | 105 ms: 1.07x slower                                                          |
| deltablue                  | 3.92 ms                                                | 4.21 ms: 1.07x slower                                                         |
| pickle_list                | 4.59 us                                                | 4.92 us: 1.07x slower                                                         |
| 2to3                       | 264 ms                                                 | 285 ms: 1.08x slower                                                          |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                         |
| html5lib                   | 64.8 ms                                                | 70.6 ms: 1.09x slower                                                         |
| sympy_expand               | 484 ms                                                 | 528 ms: 1.09x slower                                                          |
| sympy_sum                  | 169 ms                                                 | 184 ms: 1.09x slower                                                          |
| chameleon                  | 6.70 ms                                                | 7.31 ms: 1.09x slower                                                         |
| django_template            | 33.5 ms                                                | 36.7 ms: 1.10x slower                                                         |
| sympy_integrate            | 21.5 ms                                                | 23.6 ms: 1.10x slower                                                         |
| regex_v8                   | 22.9 ms                                                | 25.2 ms: 1.10x slower                                                         |
| sqlite_synth               | 2.57 us                                                | 2.84 us: 1.11x slower                                                         |
| scimark_lu                 | 116 ms                                                 | 129 ms: 1.11x slower                                                          |
| coverage                   | 78.8 ms                                                | 87.4 ms: 1.11x slower                                                         |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                          |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                         |
| dulwich_log                | 64.6 ms                                                | 74.4 ms: 1.15x slower                                                         |
| scimark_sor                | 121 ms                                                 | 142 ms: 1.17x slower                                                          |
| aiohttp                    | 1.12 ms                                                | 1.31 ms: 1.17x slower                                                         |
| genshi_xml                 | 53.4 ms                                                | 62.7 ms: 1.17x slower                                                         |
| gunicorn                   | 1.20 ms                                                | 1.43 ms: 1.19x slower                                                         |
| telco                      | 6.86 ms                                                | 8.18 ms: 1.19x slower                                                         |
| async_generators           | 374 ms                                                 | 463 ms: 1.24x slower                                                          |
| python_startup_no_site     | 6.01 ms                                                | 7.65 ms: 1.27x slower                                                         |
| create_gc_cycles           | 1.43 ms                                                | 1.85 ms: 1.29x slower                                                         |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                         |
| flaskblogging              | 7.28 ms                                                | 9.55 ms: 1.31x slower                                                         |
| mypy2                      | 686 ms                                                 | 926 ms: 1.35x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                  |

Benchmark hidden because not significant (6): djangocms, pprint_pformat, pycparser, bench_mp_pool, deepcopy, pprint_safe_repr
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 89.28% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x
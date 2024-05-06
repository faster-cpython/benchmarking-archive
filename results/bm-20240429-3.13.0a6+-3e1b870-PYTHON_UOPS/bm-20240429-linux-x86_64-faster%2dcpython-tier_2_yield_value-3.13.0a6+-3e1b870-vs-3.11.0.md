# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier_2_yield_value
- machine: linux-x86_64
- commit hash: 3e1b870
- commit date: 2024-04-29
- overall geometric mean: 1.18x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 361 ms: 1.37x slower                                                           |
| chameleon      | 6.70 ms                                                | 8.81 ms: 1.31x slower                                                          |
| docutils       | 2.66 sec                                               | 3.37 sec: 1.27x slower                                                         |
| html5lib       | 64.8 ms                                                | 81.2 ms: 1.25x slower                                                          |
| tornado_http   | 98.1 ms                                                | 105 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                  | 1.25x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 393 ms: 1.34x faster                                                           |
| async_tree_none_tg         | 491 ms                                                 | 366 ms: 1.34x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 986 ms: 1.31x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 478 ms: 1.31x faster                                                           |
| async_tree_io              | 1.29 sec                                               | 1.00 sec: 1.28x faster                                                         |
| async_tree_memoization     | 639 ms                                                 | 526 ms: 1.21x faster                                                           |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 643 ms: 1.18x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 658 ms: 1.14x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 194 ms: 1.00x faster                                                           |
| float          | 78.9 ms                                                | 129 ms: 1.63x slower                                                           |
| nbody          | 96.0 ms                                                | 197 ms: 2.05x slower                                                           |
| Geometric mean | (ref)                                                  | 1.49x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                          |
| regex_dna      | 205 ms                                                 | 226 ms: 1.11x slower                                                           |
| regex_v8       | 22.9 ms                                                | 26.4 ms: 1.15x slower                                                          |
| regex_compile  | 141 ms                                                 | 223 ms: 1.58x slower                                                           |
| Geometric mean | (ref)                                                  | 1.21x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 154 ms: 1.06x faster                                                           |
| json_loads           | 29.2 us                                                | 27.5 us: 1.06x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 317 us: 1.01x faster                                                           |
| pickle_dict          | 34.6 us                                                | 35.1 us: 1.02x slower                                                          |
| unpickle_list        | 5.21 us                                                | 5.33 us: 1.02x slower                                                          |
| pickle               | 11.0 us                                                | 11.6 us: 1.05x slower                                                          |
| unpickle             | 13.8 us                                                | 14.9 us: 1.08x slower                                                          |
| pickle_list          | 4.59 us                                                | 5.13 us: 1.12x slower                                                          |
| xml_etree_iterparse  | 108 ms                                                 | 127 ms: 1.18x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 103 ms: 1.26x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 74.0 ms: 1.30x slower                                                          |
| tomli_loads          | 2.30 sec                                               | 3.37 sec: 1.46x slower                                                         |
| unpickle_pure_python | 242 us                                                 | 398 us: 1.65x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                          |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| django_template | 33.5 ms                                                | 47.5 ms: 1.42x slower                                                          |
| genshi_xml      | 53.4 ms                                                | 80.6 ms: 1.51x slower                                                          |
| genshi_text     | 22.5 ms                                                | 38.7 ms: 1.72x slower                                                          |
| mako            | 10.7 ms                                                | 20.3 ms: 1.90x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.63x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 219 us: 2.37x faster                                                           |
| generators                 | 74.9 ms                                                | 32.1 ms: 2.33x faster                                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                         |
| asyncio_tcp                | 875 ms                                                 | 539 ms: 1.62x faster                                                           |
| async_tree_none            | 528 ms                                                 | 393 ms: 1.34x faster                                                           |
| async_tree_none_tg         | 491 ms                                                 | 366 ms: 1.34x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 986 ms: 1.31x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 478 ms: 1.31x faster                                                           |
| async_tree_io              | 1.29 sec                                               | 1.00 sec: 1.28x faster                                                         |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                          |
| pylint                     | 476 ms                                                 | 385 ms: 1.24x faster                                                           |
| async_tree_memoization     | 639 ms                                                 | 526 ms: 1.21x faster                                                           |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 643 ms: 1.18x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 658 ms: 1.14x faster                                                           |
| coroutines                 | 27.0 ms                                                | 24.1 ms: 1.12x faster                                                          |
| gc_traversal               | 4.01 ms                                                | 3.61 ms: 1.11x faster                                                          |
| xml_etree_parse            | 164 ms                                                 | 154 ms: 1.06x faster                                                           |
| json_loads                 | 29.2 us                                                | 27.5 us: 1.06x faster                                                          |
| logging_silent             | 111 ns                                                 | 108 ns: 1.02x faster                                                           |
| pickle_pure_python         | 320 us                                                 | 317 us: 1.01x faster                                                           |
| pidigits                   | 194 ms                                                 | 194 ms: 1.00x faster                                                           |
| pickle_dict                | 34.6 us                                                | 35.1 us: 1.02x slower                                                          |
| unpickle_list              | 5.21 us                                                | 5.33 us: 1.02x slower                                                          |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                           |
| pathlib                    | 18.5 ms                                                | 19.2 ms: 1.03x slower                                                          |
| deepcopy_reduce            | 3.22 us                                                | 3.34 us: 1.04x slower                                                          |
| pickle                     | 11.0 us                                                | 11.6 us: 1.05x slower                                                          |
| regex_effbot               | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                          |
| tornado_http               | 98.1 ms                                                | 105 ms: 1.07x slower                                                           |
| unpickle                   | 13.8 us                                                | 14.9 us: 1.08x slower                                                          |
| thrift                     | 784 us                                                 | 847 us: 1.08x slower                                                           |
| dask                       | 365 ms                                                 | 396 ms: 1.08x slower                                                           |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.11x slower                                                           |
| sqlglot_transpile          | 1.75 ms                                                | 1.94 ms: 1.11x slower                                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.59 ms: 1.11x slower                                                          |
| pickle_list                | 4.59 us                                                | 5.13 us: 1.12x slower                                                          |
| deepcopy                   | 365 us                                                 | 411 us: 1.13x slower                                                           |
| sympy_sum                  | 169 ms                                                 | 192 ms: 1.14x slower                                                           |
| gunicorn                   | 1.20 ms                                                | 1.37 ms: 1.14x slower                                                          |
| aiohttp                    | 1.12 ms                                                | 1.28 ms: 1.14x slower                                                          |
| regex_v8                   | 22.9 ms                                                | 26.4 ms: 1.15x slower                                                          |
| logging_simple             | 6.22 us                                                | 7.21 us: 1.16x slower                                                          |
| pycparser                  | 1.19 sec                                               | 1.38 sec: 1.16x slower                                                         |
| logging_format             | 6.81 us                                                | 7.96 us: 1.17x slower                                                          |
| bench_thread_pool          | 834 us                                                 | 976 us: 1.17x slower                                                           |
| coverage                   | 78.8 ms                                                | 92.3 ms: 1.17x slower                                                          |
| xml_etree_iterparse        | 108 ms                                                 | 127 ms: 1.18x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                          |
| sqlite_synth               | 2.57 us                                                | 3.08 us: 1.20x slower                                                          |
| mdp                        | 2.77 sec                                               | 3.33 sec: 1.20x slower                                                         |
| sympy_expand               | 484 ms                                                 | 583 ms: 1.20x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 77.9 ms: 1.21x slower                                                          |
| sympy_str                  | 297 ms                                                 | 362 ms: 1.22x slower                                                           |
| raytrace                   | 309 ms                                                 | 377 ms: 1.22x slower                                                           |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                          |
| sqlglot_normalize          | 113 ms                                                 | 141 ms: 1.25x slower                                                           |
| html5lib                   | 64.8 ms                                                | 81.2 ms: 1.25x slower                                                          |
| deepcopy_memo              | 40.2 us                                                | 50.7 us: 1.26x slower                                                          |
| xml_etree_generate         | 81.1 ms                                                | 103 ms: 1.26x slower                                                           |
| docutils                   | 2.66 sec                                               | 3.37 sec: 1.27x slower                                                         |
| richards_super             | 61.9 ms                                                | 78.6 ms: 1.27x slower                                                          |
| mypy2                      | 686 ms                                                 | 874 ms: 1.27x slower                                                           |
| sympy_integrate            | 21.5 ms                                                | 27.6 ms: 1.29x slower                                                          |
| xml_etree_process          | 56.9 ms                                                | 74.0 ms: 1.30x slower                                                          |
| chameleon                  | 6.70 ms                                                | 8.81 ms: 1.31x slower                                                          |
| meteor_contest             | 109 ms                                                 | 144 ms: 1.32x slower                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 73.3 ms: 1.33x slower                                                          |
| async_generators           | 374 ms                                                 | 504 ms: 1.35x slower                                                           |
| 2to3                       | 264 ms                                                 | 361 ms: 1.37x slower                                                           |
| deltablue                  | 3.92 ms                                                | 5.46 ms: 1.39x slower                                                          |
| telco                      | 6.86 ms                                                | 9.63 ms: 1.40x slower                                                          |
| django_template            | 33.5 ms                                                | 47.5 ms: 1.42x slower                                                          |
| chaos                      | 71.9 ms                                                | 103 ms: 1.44x slower                                                           |
| richards                   | 49.8 ms                                                | 71.7 ms: 1.44x slower                                                          |
| scimark_sor                | 121 ms                                                 | 176 ms: 1.45x slower                                                           |
| tomli_loads                | 2.30 sec                                               | 3.37 sec: 1.46x slower                                                         |
| genshi_xml                 | 53.4 ms                                                | 80.6 ms: 1.51x slower                                                          |
| regex_compile              | 141 ms                                                 | 223 ms: 1.58x slower                                                           |
| comprehensions             | 23.6 us                                                | 37.5 us: 1.59x slower                                                          |
| float                      | 78.9 ms                                                | 129 ms: 1.63x slower                                                           |
| crypto_pyaes               | 76.7 ms                                                | 125 ms: 1.63x slower                                                           |
| unpickle_pure_python       | 242 us                                                 | 398 us: 1.65x slower                                                           |
| pprint_pformat             | 1.55 sec                                               | 2.66 sec: 1.71x slower                                                         |
| genshi_text                | 22.5 ms                                                | 38.7 ms: 1.72x slower                                                          |
| pprint_safe_repr           | 747 ms                                                 | 1.29 sec: 1.73x slower                                                         |
| scimark_fft                | 345 ms                                                 | 597 ms: 1.73x slower                                                           |
| nqueens                    | 87.9 ms                                                | 153 ms: 1.74x slower                                                           |
| fannkuch                   | 405 ms                                                 | 705 ms: 1.74x slower                                                           |
| scimark_lu                 | 116 ms                                                 | 203 ms: 1.75x slower                                                           |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 8.81 ms: 1.75x slower                                                          |
| go                         | 149 ms                                                 | 261 ms: 1.76x slower                                                           |
| mako                       | 10.7 ms                                                | 20.3 ms: 1.90x slower                                                          |
| scimark_monte_carlo        | 70.7 ms                                                | 135 ms: 1.91x slower                                                           |
| pyflate                    | 434 ms                                                 | 862 ms: 1.99x slower                                                           |
| spectral_norm              | 108 ms                                                 | 215 ms: 1.99x slower                                                           |
| nbody                      | 96.0 ms                                                | 197 ms: 2.05x slower                                                           |
| hexiom                     | 6.89 ms                                                | 15.2 ms: 2.21x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.18x slower                                                                   |

Benchmark hidden because not significant (3): djangocms, json, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.18x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.03x
# Results vs. 3.11.0

- fork: faster-cpython
- ref: stats_for_all_ops
- machine: linux-x86_64
- commit hash: dd7732d
- commit date: 2024-04-04
- overall geometric mean: 1.06x faster
- HPT reliability: 92.48%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.01x slower                                                          |
| chameleon      | 6.70 ms                                                | 6.98 ms: 1.04x slower                                                         |
| docutils       | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                        |
| html5lib       | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                         |
| tornado_http   | 98.1 ms                                                | 94.6 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 351 ms: 1.50x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 606 ms: 1.26x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 198 ms: 1.02x slower                                                          |
| float          | 78.9 ms                                                | 81.3 ms: 1.03x slower                                                         |
| nbody          | 96.0 ms                                                | 127 ms: 1.32x slower                                                          |
| Geometric mean | (ref)                                                  | 1.12x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                          |
| regex_v8       | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                         |
| regex_effbot   | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                         |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                          |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 219 us: 1.11x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                          |
| tomli_loads          | 2.30 sec                                               | 2.26 sec: 1.02x faster                                                        |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.01x faster                                                          |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                         |
| pickle_dict          | 34.6 us                                                | 34.2 us: 1.01x faster                                                         |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                         |
| xml_etree_process    | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                         |
| pickle_list          | 4.59 us                                                | 4.93 us: 1.08x slower                                                         |
| xml_etree_generate   | 81.1 ms                                                | 88.8 ms: 1.10x slower                                                         |
| unpickle             | 13.8 us                                                | 15.3 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                         |
| python_startup_no_site | 6.01 ms                                                | 8.97 ms: 1.49x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 51.0 ms: 1.05x faster                                                         |
| genshi_text    | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                         |
| mako           | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.57x faster                                                          |
| generators                 | 74.9 ms                                                | 29.6 ms: 2.53x faster                                                         |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                          |
| pylint                     | 476 ms                                                 | 278 ms: 1.71x faster                                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                        |
| async_tree_none            | 528 ms                                                 | 351 ms: 1.50x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                          |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 606 ms: 1.26x faster                                                          |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                         |
| deltablue                  | 3.92 ms                                                | 3.17 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                          |
| richards_super             | 61.9 ms                                                | 52.5 ms: 1.18x faster                                                         |
| coroutines                 | 27.0 ms                                                | 23.7 ms: 1.14x faster                                                         |
| gc_traversal               | 4.01 ms                                                | 3.59 ms: 1.12x faster                                                         |
| logging_silent             | 111 ns                                                 | 100 ns: 1.11x faster                                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                         |
| hexiom                     | 6.89 ms                                                | 6.23 ms: 1.11x faster                                                         |
| unpickle_pure_python       | 242 us                                                 | 219 us: 1.11x faster                                                          |
| raytrace                   | 309 ms                                                 | 280 ms: 1.10x faster                                                          |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                          |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                          |
| deepcopy_memo              | 40.2 us                                                | 37.6 us: 1.07x faster                                                         |
| richards                   | 49.8 ms                                                | 46.8 ms: 1.06x faster                                                         |
| logging_simple             | 6.22 us                                                | 5.85 us: 1.06x faster                                                         |
| sympy_str                  | 297 ms                                                 | 281 ms: 1.06x faster                                                          |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                         |
| nqueens                    | 87.9 ms                                                | 83.3 ms: 1.06x faster                                                         |
| genshi_xml                 | 53.4 ms                                                | 51.0 ms: 1.05x faster                                                         |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                          |
| chaos                      | 71.9 ms                                                | 68.9 ms: 1.04x faster                                                         |
| deepcopy                   | 365 us                                                 | 352 us: 1.04x faster                                                          |
| tornado_http               | 98.1 ms                                                | 94.6 ms: 1.04x faster                                                         |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.04x faster                                                        |
| logging_format             | 6.81 us                                                | 6.59 us: 1.03x faster                                                         |
| crypto_pyaes               | 76.7 ms                                                | 74.3 ms: 1.03x faster                                                         |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                          |
| sympy_expand               | 484 ms                                                 | 470 ms: 1.03x faster                                                          |
| go                         | 149 ms                                                 | 145 ms: 1.02x faster                                                          |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.02x faster                                                        |
| tomli_loads                | 2.30 sec                                               | 2.26 sec: 1.02x faster                                                        |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                          |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.01x faster                                                          |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                         |
| pickle_dict                | 34.6 us                                                | 34.2 us: 1.01x faster                                                         |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| pprint_safe_repr           | 747 ms                                                 | 742 ms: 1.01x faster                                                          |
| deepcopy_reduce            | 3.22 us                                                | 3.20 us: 1.01x faster                                                         |
| sqlglot_optimize           | 55.3 ms                                                | 55.1 ms: 1.00x faster                                                         |
| 2to3                       | 264 ms                                                 | 268 ms: 1.01x slower                                                          |
| pidigits                   | 194 ms                                                 | 198 ms: 1.02x slower                                                          |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                          |
| float                      | 78.9 ms                                                | 81.3 ms: 1.03x slower                                                         |
| thrift                     | 784 us                                                 | 809 us: 1.03x slower                                                          |
| fannkuch                   | 405 ms                                                 | 419 ms: 1.03x slower                                                          |
| json                       | 5.24 ms                                                | 5.43 ms: 1.04x slower                                                         |
| aiohttp                    | 1.12 ms                                                | 1.16 ms: 1.04x slower                                                         |
| scimark_monte_carlo        | 70.7 ms                                                | 73.6 ms: 1.04x slower                                                         |
| pathlib                    | 18.5 ms                                                | 19.3 ms: 1.04x slower                                                         |
| chameleon                  | 6.70 ms                                                | 6.98 ms: 1.04x slower                                                         |
| genshi_text                | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                         |
| dulwich_log                | 64.6 ms                                                | 67.5 ms: 1.05x slower                                                         |
| scimark_lu                 | 116 ms                                                 | 122 ms: 1.05x slower                                                          |
| mako                       | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                         |
| html5lib                   | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                         |
| docutils                   | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                        |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                         |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                         |
| regex_v8                   | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                         |
| regex_effbot               | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                         |
| xml_etree_process          | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                         |
| pickle_list                | 4.59 us                                                | 4.93 us: 1.08x slower                                                         |
| mypy2                      | 686 ms                                                 | 737 ms: 1.08x slower                                                          |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                          |
| xml_etree_generate         | 81.1 ms                                                | 88.8 ms: 1.10x slower                                                         |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.11x slower                                                         |
| scimark_sor                | 121 ms                                                 | 136 ms: 1.12x slower                                                          |
| pyflate                    | 434 ms                                                 | 490 ms: 1.13x slower                                                          |
| sqlite_synth               | 2.57 us                                                | 2.96 us: 1.15x slower                                                         |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.81 ms: 1.16x slower                                                         |
| async_generators           | 374 ms                                                 | 441 ms: 1.18x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                         |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                         |
| scimark_fft                | 345 ms                                                 | 429 ms: 1.24x slower                                                          |
| coverage                   | 78.8 ms                                                | 98.1 ms: 1.25x slower                                                         |
| telco                      | 6.86 ms                                                | 8.68 ms: 1.27x slower                                                         |
| spectral_norm              | 108 ms                                                 | 142 ms: 1.32x slower                                                          |
| nbody                      | 96.0 ms                                                | 127 ms: 1.32x slower                                                          |
| python_startup_no_site     | 6.01 ms                                                | 8.97 ms: 1.49x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                  |

Benchmark hidden because not significant (5): bench_thread_pool, mdp, unpickle_list, meteor_contest, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 92.48% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x
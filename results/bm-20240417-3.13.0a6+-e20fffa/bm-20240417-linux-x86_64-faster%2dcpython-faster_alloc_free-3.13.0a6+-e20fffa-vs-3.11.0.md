# Results vs. 3.11.0

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: e20fffa
- commit date: 2024-04-17
- overall geometric mean: 1.07x faster
- HPT reliability: 97.44%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.02x slower                                                          |
| chameleon      | 6.70 ms                                                | 7.20 ms: 1.08x slower                                                         |
| docutils       | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                        |
| html5lib       | 64.8 ms                                                | 66.9 ms: 1.03x slower                                                         |
| tornado_http   | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 358 ms: 1.47x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 927 ms: 1.39x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 937 ms: 1.38x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 607 ms: 1.25x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 85.0 ms: 1.13x faster                                                         |
| float          | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                         |
| pidigits       | 194 ms                                                 | 191 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                  | 1.06x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.04x faster                                                          |
| regex_effbot   | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                         |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                          |
| regex_v8       | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                         |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 219 us: 1.11x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                          |
| json_loads           | 29.2 us                                                | 27.5 us: 1.06x faster                                                         |
| tomli_loads          | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                        |
| pickle_dict          | 34.6 us                                                | 32.7 us: 1.06x faster                                                         |
| unpickle_list        | 5.21 us                                                | 5.08 us: 1.03x faster                                                         |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                          |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                         |
| pickle_list          | 4.59 us                                                | 4.89 us: 1.07x slower                                                         |
| unpickle             | 13.8 us                                                | 14.8 us: 1.07x slower                                                         |
| xml_etree_process    | 56.9 ms                                                | 61.0 ms: 1.07x slower                                                         |
| xml_etree_generate   | 81.1 ms                                                | 88.9 ms: 1.10x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                  |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.06 ms: 1.17x slower                                                         |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.9 ms: 1.01x faster                                                         |
| mako            | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                         |
| django_template | 33.5 ms                                                | 35.0 ms: 1.04x slower                                                         |
| genshi_text     | 22.5 ms                                                | 23.9 ms: 1.06x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-e20fffa |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 115 us: 4.52x faster                                                          |
| generators                 | 74.9 ms                                                | 30.4 ms: 2.46x faster                                                         |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.83 sec: 1.70x faster                                                        |
| pylint                     | 476 ms                                                 | 320 ms: 1.49x faster                                                          |
| async_tree_none            | 528 ms                                                 | 358 ms: 1.47x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 338 ms: 1.45x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                          |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.41x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 927 ms: 1.39x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 937 ms: 1.38x faster                                                          |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 607 ms: 1.25x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                          |
| deltablue                  | 3.92 ms                                                | 3.22 ms: 1.22x faster                                                         |
| coroutines                 | 27.0 ms                                                | 22.4 ms: 1.20x faster                                                         |
| raytrace                   | 309 ms                                                 | 257 ms: 1.20x faster                                                          |
| chaos                      | 71.9 ms                                                | 60.2 ms: 1.19x faster                                                         |
| richards_super             | 61.9 ms                                                | 52.9 ms: 1.17x faster                                                         |
| nbody                      | 96.0 ms                                                | 85.0 ms: 1.13x faster                                                         |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                         |
| unpickle_pure_python       | 242 us                                                 | 219 us: 1.11x faster                                                          |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.10x faster                                                         |
| hexiom                     | 6.89 ms                                                | 6.35 ms: 1.09x faster                                                         |
| logging_simple             | 6.22 us                                                | 5.77 us: 1.08x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                          |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.08x faster                                                        |
| nqueens                    | 87.9 ms                                                | 81.8 ms: 1.07x faster                                                         |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                          |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                          |
| logging_format             | 6.81 us                                                | 6.40 us: 1.06x faster                                                         |
| json_loads                 | 29.2 us                                                | 27.5 us: 1.06x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                        |
| richards                   | 49.8 ms                                                | 47.1 ms: 1.06x faster                                                         |
| pathlib                    | 18.5 ms                                                | 17.5 ms: 1.06x faster                                                         |
| pickle_dict                | 34.6 us                                                | 32.7 us: 1.06x faster                                                         |
| djangocms                  | 33.5 us                                                | 31.8 us: 1.05x faster                                                         |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.05x faster                                                          |
| crypto_pyaes               | 76.7 ms                                                | 72.9 ms: 1.05x faster                                                         |
| deepcopy_memo              | 40.2 us                                                | 38.4 us: 1.05x faster                                                         |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                         |
| regex_compile              | 141 ms                                                 | 135 ms: 1.04x faster                                                          |
| tornado_http               | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                         |
| go                         | 149 ms                                                 | 143 ms: 1.04x faster                                                          |
| fannkuch                   | 405 ms                                                 | 390 ms: 1.04x faster                                                          |
| scimark_monte_carlo        | 70.7 ms                                                | 68.2 ms: 1.04x faster                                                         |
| gc_traversal               | 4.01 ms                                                | 3.88 ms: 1.03x faster                                                         |
| unpickle_list              | 5.21 us                                                | 5.08 us: 1.03x faster                                                         |
| deepcopy                   | 365 us                                                 | 356 us: 1.02x faster                                                          |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                        |
| float                      | 78.9 ms                                                | 77.2 ms: 1.02x faster                                                         |
| sympy_expand               | 484 ms                                                 | 474 ms: 1.02x faster                                                          |
| json                       | 5.24 ms                                                | 5.14 ms: 1.02x faster                                                         |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                          |
| pidigits                   | 194 ms                                                 | 191 ms: 1.02x faster                                                          |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                          |
| genshi_xml                 | 53.4 ms                                                | 52.9 ms: 1.01x faster                                                         |
| deepcopy_reduce            | 3.22 us                                                | 3.19 us: 1.01x faster                                                         |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                         |
| bench_thread_pool          | 834 us                                                 | 837 us: 1.00x slower                                                          |
| sqlglot_optimize           | 55.3 ms                                                | 55.5 ms: 1.00x slower                                                         |
| pprint_pformat             | 1.55 sec                                               | 1.57 sec: 1.01x slower                                                        |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                          |
| scimark_lu                 | 116 ms                                                 | 118 ms: 1.02x slower                                                          |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                          |
| dulwich_log                | 64.6 ms                                                | 66.1 ms: 1.02x slower                                                         |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                         |
| 2to3                       | 264 ms                                                 | 271 ms: 1.02x slower                                                          |
| pprint_safe_repr           | 747 ms                                                 | 766 ms: 1.03x slower                                                          |
| scimark_sor                | 121 ms                                                 | 125 ms: 1.03x slower                                                          |
| html5lib                   | 64.8 ms                                                | 66.9 ms: 1.03x slower                                                         |
| thrift                     | 784 us                                                 | 817 us: 1.04x slower                                                          |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.04x slower                                                          |
| django_template            | 33.5 ms                                                | 35.0 ms: 1.04x slower                                                         |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.26 ms: 1.05x slower                                                         |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                         |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                         |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                         |
| pyflate                    | 434 ms                                                 | 461 ms: 1.06x slower                                                          |
| genshi_text                | 22.5 ms                                                | 23.9 ms: 1.06x slower                                                         |
| pickle_list                | 4.59 us                                                | 4.89 us: 1.07x slower                                                         |
| regex_effbot               | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                         |
| docutils                   | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                        |
| unpickle                   | 13.8 us                                                | 14.8 us: 1.07x slower                                                         |
| xml_etree_process          | 56.9 ms                                                | 61.0 ms: 1.07x slower                                                         |
| chameleon                  | 6.70 ms                                                | 7.20 ms: 1.08x slower                                                         |
| mypy2                      | 686 ms                                                 | 738 ms: 1.08x slower                                                          |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                          |
| scimark_fft                | 345 ms                                                 | 374 ms: 1.08x slower                                                          |
| xml_etree_generate         | 81.1 ms                                                | 88.9 ms: 1.10x slower                                                         |
| regex_v8                   | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                         |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.06 ms: 1.17x slower                                                         |
| async_generators           | 374 ms                                                 | 445 ms: 1.19x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                         |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                         |
| coverage                   | 78.8 ms                                                | 97.9 ms: 1.24x slower                                                         |
| telco                      | 6.86 ms                                                | 8.69 ms: 1.27x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                  |

Benchmark hidden because not significant (2): xml_etree_iterparse, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.44% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x
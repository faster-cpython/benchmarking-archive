# Results vs. 3.11.0

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: 83ebcf5
- commit date: 2024-04-16
- overall geometric mean: 1.06x faster
- HPT reliability: 96.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.03x slower                                                          |
| chameleon      | 6.70 ms                                                | 7.07 ms: 1.06x slower                                                         |
| docutils       | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                        |
| html5lib       | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                         |
| tornado_http   | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 925 ms: 1.39x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 607 ms: 1.23x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.3 ms: 1.06x faster                                                         |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                          |
| float          | 78.9 ms                                                | 79.8 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 137 ms: 1.03x faster                                                          |
| regex_effbot   | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                         |
| regex_v8       | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                         |
| regex_dna      | 205 ms                                                 | 226 ms: 1.10x slower                                                          |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 223 us: 1.09x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                                          |
| unpickle_list        | 5.21 us                                                | 4.98 us: 1.05x faster                                                         |
| json_loads           | 29.2 us                                                | 28.0 us: 1.04x faster                                                         |
| tomli_loads          | 2.30 sec                                               | 2.22 sec: 1.04x faster                                                        |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                          |
| pickle_dict          | 34.6 us                                                | 33.9 us: 1.02x faster                                                         |
| pickle               | 11.0 us                                                | 11.5 us: 1.05x slower                                                         |
| xml_etree_process    | 56.9 ms                                                | 61.2 ms: 1.08x slower                                                         |
| xml_etree_generate   | 81.1 ms                                                | 88.5 ms: 1.09x slower                                                         |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                         |
| pickle_list          | 4.59 us                                                | 5.03 us: 1.10x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                         |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.8 ms: 1.03x faster                                                         |
| mako            | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                         |
| genshi_text     | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                         |
| django_template | 33.5 ms                                                | 35.6 ms: 1.06x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.62x faster                                                          |
| generators                 | 74.9 ms                                                | 30.1 ms: 2.49x faster                                                         |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                        |
| pylint                     | 476 ms                                                 | 321 ms: 1.48x faster                                                          |
| async_tree_none            | 528 ms                                                 | 357 ms: 1.48x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 925 ms: 1.39x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                          |
| comprehensions             | 23.6 us                                                | 17.2 us: 1.37x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                          |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 607 ms: 1.23x faster                                                          |
| deltablue                  | 3.92 ms                                                | 3.29 ms: 1.19x faster                                                         |
| coroutines                 | 27.0 ms                                                | 23.2 ms: 1.17x faster                                                         |
| raytrace                   | 309 ms                                                 | 265 ms: 1.16x faster                                                          |
| chaos                      | 71.9 ms                                                | 62.2 ms: 1.16x faster                                                         |
| richards_super             | 61.9 ms                                                | 54.0 ms: 1.15x faster                                                         |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.10x faster                                                         |
| unpickle_pure_python       | 242 us                                                 | 223 us: 1.09x faster                                                          |
| hexiom                     | 6.89 ms                                                | 6.40 ms: 1.08x faster                                                         |
| logging_simple             | 6.22 us                                                | 5.78 us: 1.08x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 158 ms: 1.07x faster                                                          |
| nqueens                    | 87.9 ms                                                | 82.4 ms: 1.07x faster                                                         |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                          |
| gc_traversal               | 4.01 ms                                                | 3.76 ms: 1.07x faster                                                         |
| nbody                      | 96.0 ms                                                | 90.3 ms: 1.06x faster                                                         |
| logging_format             | 6.81 us                                                | 6.43 us: 1.06x faster                                                         |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                                          |
| djangocms                  | 33.5 us                                                | 31.7 us: 1.06x faster                                                         |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                         |
| unpickle_list              | 5.21 us                                                | 4.98 us: 1.05x faster                                                         |
| sympy_str                  | 297 ms                                                 | 284 ms: 1.05x faster                                                          |
| deepcopy_memo              | 40.2 us                                                | 38.5 us: 1.04x faster                                                         |
| sympy_integrate            | 21.5 ms                                                | 20.6 ms: 1.04x faster                                                         |
| tornado_http               | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                         |
| json_loads                 | 29.2 us                                                | 28.0 us: 1.04x faster                                                         |
| mdp                        | 2.77 sec                                               | 2.67 sec: 1.04x faster                                                        |
| tomli_loads                | 2.30 sec                                               | 2.22 sec: 1.04x faster                                                        |
| richards                   | 49.8 ms                                                | 48.2 ms: 1.03x faster                                                         |
| genshi_xml                 | 53.4 ms                                                | 51.8 ms: 1.03x faster                                                         |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                          |
| regex_compile              | 141 ms                                                 | 137 ms: 1.03x faster                                                          |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                          |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                          |
| pickle_dict                | 34.6 us                                                | 33.9 us: 1.02x faster                                                         |
| fannkuch                   | 405 ms                                                 | 399 ms: 1.02x faster                                                          |
| crypto_pyaes               | 76.7 ms                                                | 75.6 ms: 1.01x faster                                                         |
| sympy_expand               | 484 ms                                                 | 479 ms: 1.01x faster                                                          |
| deepcopy                   | 365 us                                                 | 361 us: 1.01x faster                                                          |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                        |
| sqlglot_normalize          | 113 ms                                                 | 112 ms: 1.01x faster                                                          |
| scimark_monte_carlo        | 70.7 ms                                                | 70.3 ms: 1.01x faster                                                         |
| bench_thread_pool          | 834 us                                                 | 838 us: 1.00x slower                                                          |
| pprint_safe_repr           | 747 ms                                                 | 755 ms: 1.01x slower                                                          |
| float                      | 78.9 ms                                                | 79.8 ms: 1.01x slower                                                         |
| sqlglot_optimize           | 55.3 ms                                                | 56.0 ms: 1.01x slower                                                         |
| deepcopy_reduce            | 3.22 us                                                | 3.26 us: 1.01x slower                                                         |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                          |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.02x slower                                                          |
| dulwich_log                | 64.6 ms                                                | 66.3 ms: 1.03x slower                                                         |
| 2to3                       | 264 ms                                                 | 271 ms: 1.03x slower                                                          |
| scimark_sor                | 121 ms                                                 | 125 ms: 1.03x slower                                                          |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                         |
| thrift                     | 784 us                                                 | 811 us: 1.03x slower                                                          |
| scimark_lu                 | 116 ms                                                 | 121 ms: 1.04x slower                                                          |
| regex_effbot               | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                         |
| pickle                     | 11.0 us                                                | 11.5 us: 1.05x slower                                                         |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                         |
| html5lib                   | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                         |
| chameleon                  | 6.70 ms                                                | 7.07 ms: 1.06x slower                                                         |
| genshi_text                | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                         |
| django_template            | 33.5 ms                                                | 35.6 ms: 1.06x slower                                                         |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                         |
| docutils                   | 2.66 sec                                               | 2.84 sec: 1.07x slower                                                        |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.07x slower                                                          |
| xml_etree_process          | 56.9 ms                                                | 61.2 ms: 1.08x slower                                                         |
| mypy2                      | 686 ms                                                 | 741 ms: 1.08x slower                                                          |
| regex_v8                   | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                         |
| pyflate                    | 434 ms                                                 | 469 ms: 1.08x slower                                                          |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.46 ms: 1.09x slower                                                         |
| xml_etree_generate         | 81.1 ms                                                | 88.5 ms: 1.09x slower                                                         |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                         |
| pickle_list                | 4.59 us                                                | 5.03 us: 1.10x slower                                                         |
| scimark_fft                | 345 ms                                                 | 380 ms: 1.10x slower                                                          |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.10x slower                                                          |
| sqlite_synth               | 2.57 us                                                | 2.97 us: 1.16x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                         |
| async_generators           | 374 ms                                                 | 448 ms: 1.20x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.73 ms: 1.21x slower                                                         |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                         |
| coverage                   | 78.8 ms                                                | 97.6 ms: 1.24x slower                                                         |
| telco                      | 6.86 ms                                                | 8.85 ms: 1.29x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                  |

Benchmark hidden because not significant (4): pycparser, json, xml_etree_iterparse, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.38% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x
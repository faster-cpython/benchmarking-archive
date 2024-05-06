# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 0bbd7af
- commit date: 2024-04-08
- overall geometric mean: 1.08x faster
- HPT reliability: 99.42%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 269 ms: 1.02x slower                                                             |
| chameleon      | 6.70 ms                                                | 6.83 ms: 1.02x slower                                                            |
| docutils       | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                           |
| html5lib       | 64.8 ms                                                | 67.7 ms: 1.04x slower                                                            |
| tornado_http   | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 922 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 606 ms: 1.24x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 87.9 ms: 1.09x faster                                                            |
| float          | 78.9 ms                                                | 77.6 ms: 1.02x faster                                                            |
| pidigits       | 194 ms                                                 | 197 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.06x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.66 ms: 1.04x slower                                                            |
| regex_v8       | 22.9 ms                                                | 24.8 ms: 1.09x slower                                                            |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 220 us: 1.10x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.12 sec: 1.08x faster                                                           |
| pickle_pure_python   | 320 us                                                 | 298 us: 1.07x faster                                                             |
| unpickle_list        | 5.21 us                                                | 5.01 us: 1.04x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                             |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                            |
| pickle_dict          | 34.6 us                                                | 36.4 us: 1.05x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                            |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                            |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.19 us: 1.13x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 8.95 ms: 1.49x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 51.5 ms: 1.04x faster                                                            |
| mako           | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                            |
| genshi_text    | 22.5 ms                                                | 23.6 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 112 us: 4.64x faster                                                             |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                             |
| pylint                     | 476 ms                                                 | 279 ms: 1.70x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 922 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 938 ms: 1.38x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 606 ms: 1.24x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.19 ms: 1.23x faster                                                            |
| coroutines                 | 27.0 ms                                                | 22.1 ms: 1.22x faster                                                            |
| chaos                      | 71.9 ms                                                | 59.9 ms: 1.20x faster                                                            |
| raytrace                   | 309 ms                                                 | 259 ms: 1.19x faster                                                             |
| richards_super             | 61.9 ms                                                | 53.1 ms: 1.17x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.23 ms: 1.11x faster                                                            |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                             |
| deepcopy_memo              | 40.2 us                                                | 36.4 us: 1.10x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 220 us: 1.10x faster                                                             |
| logging_simple             | 6.22 us                                                | 5.66 us: 1.10x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                            |
| nbody                      | 96.0 ms                                                | 87.9 ms: 1.09x faster                                                            |
| nqueens                    | 87.9 ms                                                | 80.6 ms: 1.09x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.12 sec: 1.08x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                             |
| logging_format             | 6.81 us                                                | 6.31 us: 1.08x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 298 us: 1.07x faster                                                             |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                                           |
| gc_traversal               | 4.01 ms                                                | 3.75 ms: 1.07x faster                                                            |
| sympy_str                  | 297 ms                                                 | 278 ms: 1.07x faster                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 66.4 ms: 1.06x faster                                                            |
| richards                   | 49.8 ms                                                | 47.1 ms: 1.06x faster                                                            |
| fannkuch                   | 405 ms                                                 | 383 ms: 1.06x faster                                                             |
| regex_compile              | 141 ms                                                 | 134 ms: 1.06x faster                                                             |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                            |
| go                         | 149 ms                                                 | 141 ms: 1.05x faster                                                             |
| deepcopy                   | 365 us                                                 | 350 us: 1.04x faster                                                             |
| unpickle_list              | 5.21 us                                                | 5.01 us: 1.04x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 51.5 ms: 1.04x faster                                                            |
| tornado_http               | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.50 sec: 1.04x faster                                                           |
| sympy_expand               | 484 ms                                                 | 468 ms: 1.04x faster                                                             |
| crypto_pyaes               | 76.7 ms                                                | 74.6 ms: 1.03x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                             |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.03x faster                                                           |
| pprint_safe_repr           | 747 ms                                                 | 732 ms: 1.02x faster                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.16 us: 1.02x faster                                                            |
| float                      | 78.9 ms                                                | 77.6 ms: 1.02x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                             |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                            |
| scimark_lu                 | 116 ms                                                 | 115 ms: 1.01x faster                                                             |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                            |
| pidigits                   | 194 ms                                                 | 197 ms: 1.02x slower                                                             |
| scimark_sor                | 121 ms                                                 | 124 ms: 1.02x slower                                                             |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                             |
| chameleon                  | 6.70 ms                                                | 6.83 ms: 1.02x slower                                                            |
| 2to3                       | 264 ms                                                 | 269 ms: 1.02x slower                                                             |
| thrift                     | 784 us                                                 | 807 us: 1.03x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                             |
| json                       | 5.24 ms                                                | 5.43 ms: 1.04x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.22 ms: 1.04x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 67.3 ms: 1.04x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.66 ms: 1.04x slower                                                            |
| html5lib                   | 64.8 ms                                                | 67.7 ms: 1.04x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.6 ms: 1.05x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| pickle_dict                | 34.6 us                                                | 36.4 us: 1.05x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                            |
| scimark_fft                | 345 ms                                                 | 371 ms: 1.07x slower                                                             |
| pyflate                    | 434 ms                                                 | 467 ms: 1.08x slower                                                             |
| mypy2                      | 686 ms                                                 | 740 ms: 1.08x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 24.8 ms: 1.09x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                            |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                            |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| pickle_list                | 4.59 us                                                | 5.19 us: 1.13x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.92 us: 1.13x slower                                                            |
| async_generators           | 374 ms                                                 | 443 ms: 1.19x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.72 ms: 1.20x slower                                                            |
| coverage                   | 78.8 ms                                                | 96.3 ms: 1.22x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.80 ms: 1.28x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 8.95 ms: 1.49x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                                     |

Benchmark hidden because not significant (6): bench_mp_pool, bench_thread_pool, pathlib, sqlglot_optimize, dask, spectral_norm
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.42% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x
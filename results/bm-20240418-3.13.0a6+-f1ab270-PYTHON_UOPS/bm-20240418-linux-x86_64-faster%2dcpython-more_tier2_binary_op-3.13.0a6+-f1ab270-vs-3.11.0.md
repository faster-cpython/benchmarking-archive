# Results vs. 3.11.0

- fork: faster-cpython
- ref: more_tier2_binary_op
- machine: linux-x86_64
- commit hash: f1ab270
- commit date: 2024-04-18
- overall geometric mean: 1.16x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 330 ms: 1.25x slower                                                             |
| chameleon      | 6.70 ms                                                | 8.18 ms: 1.22x slower                                                            |
| docutils       | 2.66 sec                                               | 3.27 sec: 1.23x slower                                                           |
| html5lib       | 64.8 ms                                                | 73.7 ms: 1.14x slower                                                            |
| tornado_http   | 98.1 ms                                                | 103 ms: 1.06x slower                                                             |
| Geometric mean | (ref)                                                  | 1.18x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 397 ms: 1.33x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 371 ms: 1.32x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 485 ms: 1.29x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 1.01 sec: 1.28x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 1.02 sec: 1.27x faster                                                           |
| async_tree_memoization     | 639 ms                                                 | 530 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 651 ms: 1.17x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 661 ms: 1.13x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 202 ms: 1.04x slower                                                             |
| float          | 78.9 ms                                                | 135 ms: 1.71x slower                                                             |
| nbody          | 96.0 ms                                                | 209 ms: 2.17x slower                                                             |
| Geometric mean | (ref)                                                  | 1.57x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.61 ms: 1.03x slower                                                            |
| regex_dna      | 205 ms                                                 | 226 ms: 1.10x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                            |
| regex_compile  | 141 ms                                                 | 220 ms: 1.56x slower                                                             |
| Geometric mean | (ref)                                                  | 1.19x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 154 ms: 1.06x faster                                                             |
| json_loads           | 29.2 us                                                | 27.9 us: 1.04x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.08 us: 1.03x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 316 us: 1.01x faster                                                             |
| pickle_dict          | 34.6 us                                                | 34.4 us: 1.01x faster                                                            |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                            |
| pickle_list          | 4.59 us                                                | 4.97 us: 1.08x slower                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 130 ms: 1.21x slower                                                             |
| unpickle             | 13.8 us                                                | 17.0 us: 1.23x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 70.8 ms: 1.24x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 104 ms: 1.28x slower                                                             |
| tomli_loads          | 2.30 sec                                               | 3.52 sec: 1.53x slower                                                           |
| unpickle_pure_python | 242 us                                                 | 404 us: 1.67x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 22.5 ms                                                | 26.9 ms: 1.19x slower                                                            |
| genshi_xml      | 53.4 ms                                                | 64.0 ms: 1.20x slower                                                            |
| django_template | 33.5 ms                                                | 43.3 ms: 1.29x slower                                                            |
| mako            | 10.7 ms                                                | 21.1 ms: 1.98x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.38x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 130 us: 3.99x faster                                                             |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 514 ms: 1.70x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                           |
| async_tree_none            | 528 ms                                                 | 397 ms: 1.33x faster                                                             |
| pylint                     | 476 ms                                                 | 360 ms: 1.32x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 371 ms: 1.32x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 485 ms: 1.29x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 1.01 sec: 1.28x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 1.02 sec: 1.27x faster                                                           |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 530 ms: 1.21x faster                                                             |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 651 ms: 1.17x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 661 ms: 1.13x faster                                                             |
| xml_etree_parse            | 164 ms                                                 | 154 ms: 1.06x faster                                                             |
| djangocms                  | 33.5 us                                                | 31.8 us: 1.05x faster                                                            |
| json_loads                 | 29.2 us                                                | 27.9 us: 1.04x faster                                                            |
| unpickle_list              | 5.21 us                                                | 5.08 us: 1.03x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.90 ms: 1.03x faster                                                            |
| logging_silent             | 111 ns                                                 | 109 ns: 1.02x faster                                                             |
| json                       | 5.24 ms                                                | 5.16 ms: 1.02x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 316 us: 1.01x faster                                                             |
| pickle_dict                | 34.6 us                                                | 34.4 us: 1.01x faster                                                            |
| regex_effbot               | 3.51 ms                                                | 3.61 ms: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                             |
| pidigits                   | 194 ms                                                 | 202 ms: 1.04x slower                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.39 us: 1.05x slower                                                            |
| tornado_http               | 98.1 ms                                                | 103 ms: 1.06x slower                                                             |
| logging_simple             | 6.22 us                                                | 6.58 us: 1.06x slower                                                            |
| dask                       | 365 ms                                                 | 388 ms: 1.06x slower                                                             |
| thrift                     | 784 us                                                 | 836 us: 1.07x slower                                                             |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                            |
| deepcopy                   | 365 us                                                 | 395 us: 1.08x slower                                                             |
| pickle_list                | 4.59 us                                                | 4.97 us: 1.08x slower                                                            |
| mdp                        | 2.77 sec                                               | 3.01 sec: 1.08x slower                                                           |
| logging_format             | 6.81 us                                                | 7.39 us: 1.09x slower                                                            |
| regex_dna                  | 205 ms                                                 | 226 ms: 1.10x slower                                                             |
| bench_thread_pool          | 834 us                                                 | 928 us: 1.11x slower                                                             |
| gunicorn                   | 1.20 ms                                                | 1.34 ms: 1.12x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.25 ms: 1.12x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.97 ms: 1.13x slower                                                            |
| sympy_sum                  | 169 ms                                                 | 191 ms: 1.13x slower                                                             |
| html5lib                   | 64.8 ms                                                | 73.7 ms: 1.14x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.35 sec: 1.14x slower                                                           |
| sqlglot_parse              | 1.43 ms                                                | 1.63 ms: 1.14x slower                                                            |
| sympy_expand               | 484 ms                                                 | 556 ms: 1.15x slower                                                             |
| sympy_str                  | 297 ms                                                 | 347 ms: 1.17x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 75.8 ms: 1.17x slower                                                            |
| sympy_integrate            | 21.5 ms                                                | 25.3 ms: 1.18x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                            |
| sqlglot_normalize          | 113 ms                                                 | 133 ms: 1.18x slower                                                             |
| genshi_text                | 22.5 ms                                                | 26.9 ms: 1.19x slower                                                            |
| genshi_xml                 | 53.4 ms                                                | 64.0 ms: 1.20x slower                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 130 ms: 1.21x slower                                                             |
| mypy2                      | 686 ms                                                 | 831 ms: 1.21x slower                                                             |
| chameleon                  | 6.70 ms                                                | 8.18 ms: 1.22x slower                                                            |
| raytrace                   | 309 ms                                                 | 378 ms: 1.23x slower                                                             |
| docutils                   | 2.66 sec                                               | 3.27 sec: 1.23x slower                                                           |
| sqlite_synth               | 2.57 us                                                | 3.15 us: 1.23x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| unpickle                   | 13.8 us                                                | 17.0 us: 1.23x slower                                                            |
| deepcopy_memo              | 40.2 us                                                | 49.9 us: 1.24x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 70.8 ms: 1.24x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.79 ms: 1.25x slower                                                            |
| 2to3                       | 264 ms                                                 | 330 ms: 1.25x slower                                                             |
| coverage                   | 78.8 ms                                                | 98.5 ms: 1.25x slower                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 70.4 ms: 1.27x slower                                                            |
| deltablue                  | 3.92 ms                                                | 5.02 ms: 1.28x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 104 ms: 1.28x slower                                                             |
| django_template            | 33.5 ms                                                | 43.3 ms: 1.29x slower                                                            |
| richards_super             | 61.9 ms                                                | 81.6 ms: 1.32x slower                                                            |
| meteor_contest             | 109 ms                                                 | 145 ms: 1.33x slower                                                             |
| async_generators           | 374 ms                                                 | 503 ms: 1.35x slower                                                             |
| telco                      | 6.86 ms                                                | 9.78 ms: 1.43x slower                                                            |
| chaos                      | 71.9 ms                                                | 103 ms: 1.43x slower                                                             |
| scimark_sor                | 121 ms                                                 | 174 ms: 1.44x slower                                                             |
| richards                   | 49.8 ms                                                | 75.2 ms: 1.51x slower                                                            |
| tomli_loads                | 2.30 sec                                               | 3.52 sec: 1.53x slower                                                           |
| comprehensions             | 23.6 us                                                | 36.1 us: 1.53x slower                                                            |
| go                         | 149 ms                                                 | 229 ms: 1.54x slower                                                             |
| regex_compile              | 141 ms                                                 | 220 ms: 1.56x slower                                                             |
| unpickle_pure_python       | 242 us                                                 | 404 us: 1.67x slower                                                             |
| crypto_pyaes               | 76.7 ms                                                | 128 ms: 1.67x slower                                                             |
| pprint_pformat             | 1.55 sec                                               | 2.60 sec: 1.67x slower                                                           |
| pprint_safe_repr           | 747 ms                                                 | 1.25 sec: 1.68x slower                                                           |
| float                      | 78.9 ms                                                | 135 ms: 1.71x slower                                                             |
| nqueens                    | 87.9 ms                                                | 153 ms: 1.74x slower                                                             |
| scimark_lu                 | 116 ms                                                 | 208 ms: 1.78x slower                                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 9.00 ms: 1.79x slower                                                            |
| scimark_fft                | 345 ms                                                 | 633 ms: 1.83x slower                                                             |
| fannkuch                   | 405 ms                                                 | 764 ms: 1.89x slower                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 139 ms: 1.97x slower                                                             |
| mako                       | 10.7 ms                                                | 21.1 ms: 1.98x slower                                                            |
| pyflate                    | 434 ms                                                 | 878 ms: 2.02x slower                                                             |
| nbody                      | 96.0 ms                                                | 209 ms: 2.17x slower                                                             |
| hexiom                     | 6.89 ms                                                | 15.1 ms: 2.20x slower                                                            |
| spectral_norm              | 108 ms                                                 | 242 ms: 2.24x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.16x slower                                                                     |

Benchmark hidden because not significant (2): bench_mp_pool, pathlib
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.03x
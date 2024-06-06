# Results vs. 3.11.0

- fork: brandtbucher
- ref: inline_class_call_de
- machine: linux-x86_64
- commit hash: 1108a82
- commit date: 2024-06-05
- overall geometric mean: 1.06x faster
- HPT reliability: 97.76%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-1108a82 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                        |
| docutils       | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                      |
| html5lib       | 64.8 ms                                                | 69.3 ms: 1.07x slower                                                       |
| tornado_http   | 98.1 ms                                                | 97.2 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-1108a82 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 343 ms: 1.43x faster                                                        |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.40x faster                                                        |
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 480 ms: 1.33x faster                                                        |
| async_tree_io              | 1.29 sec                                               | 980 ms: 1.31x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 599 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 638 ms: 1.17x faster                                                        |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-1108a82 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.4 ms: 1.18x faster                                                       |
| float          | 78.9 ms                                                | 72.7 ms: 1.09x faster                                                       |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-1108a82 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 137 ms: 1.03x faster                                                        |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                       |
| regex_effbot   | 3.51 ms                                                | 3.86 ms: 1.10x slower                                                       |
| regex_dna      | 205 ms                                                 | 231 ms: 1.13x slower                                                        |
| Geometric mean | (ref)                                                  | 1.07x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-1108a82 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                       |
| tomli_loads          | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                      |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                                        |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                        |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                                        |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                                        |
| pickle_dict          | 34.6 us                                                | 35.1 us: 1.01x slower                                                       |
| xml_etree_generate   | 81.1 ms                                                | 82.7 ms: 1.02x slower                                                       |
| xml_etree_process    | 56.9 ms                                                | 58.5 ms: 1.03x slower                                                       |
| unpickle_list        | 5.21 us                                                | 5.40 us: 1.04x slower                                                       |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                       |
| pickle               | 11.0 us                                                | 12.2 us: 1.11x slower                                                       |
| pickle_list          | 4.59 us                                                | 5.34 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-1108a82 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                       |
| python_startup         | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-1108a82 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                       |
| django_template | 33.5 ms                                                | 36.6 ms: 1.09x slower                                                       |
| genshi_xml      | 53.4 ms                                                | 58.9 ms: 1.10x slower                                                       |
| genshi_text     | 22.5 ms                                                | 25.1 ms: 1.11x slower                                                       |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-1108a82 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 174 us: 2.98x faster                                                        |
| generators                 | 74.9 ms                                                | 30.6 ms: 2.44x faster                                                       |
| asyncio_tcp                | 875 ms                                                 | 519 ms: 1.69x faster                                                        |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                      |
| async_tree_none_tg         | 491 ms                                                 | 343 ms: 1.43x faster                                                        |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                       |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.40x faster                                                        |
| async_tree_none            | 528 ms                                                 | 380 ms: 1.39x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                        |
| pylint                     | 476 ms                                                 | 352 ms: 1.35x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 480 ms: 1.33x faster                                                        |
| async_tree_io              | 1.29 sec                                               | 980 ms: 1.31x faster                                                        |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                       |
| richards_super             | 61.9 ms                                                | 48.5 ms: 1.28x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 599 ms: 1.27x faster                                                        |
| chaos                      | 71.9 ms                                                | 60.3 ms: 1.19x faster                                                       |
| coroutines                 | 27.0 ms                                                | 22.7 ms: 1.19x faster                                                       |
| richards                   | 49.8 ms                                                | 42.2 ms: 1.18x faster                                                       |
| tomli_loads                | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                      |
| nbody                      | 96.0 ms                                                | 81.4 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 638 ms: 1.17x faster                                                        |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.33 ms: 1.16x faster                                                       |
| fannkuch                   | 405 ms                                                 | 355 ms: 1.14x faster                                                        |
| crypto_pyaes               | 76.7 ms                                                | 67.4 ms: 1.14x faster                                                       |
| scimark_monte_carlo        | 70.7 ms                                                | 62.6 ms: 1.13x faster                                                       |
| pathlib                    | 18.5 ms                                                | 16.7 ms: 1.11x faster                                                       |
| scimark_fft                | 345 ms                                                 | 314 ms: 1.10x faster                                                        |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                       |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                                        |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                        |
| raytrace                   | 309 ms                                                 | 283 ms: 1.09x faster                                                        |
| float                      | 78.9 ms                                                | 72.7 ms: 1.09x faster                                                       |
| logging_simple             | 6.22 us                                                | 5.74 us: 1.08x faster                                                       |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.07x faster                                                      |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                                        |
| pprint_safe_repr           | 747 ms                                                 | 701 ms: 1.07x faster                                                        |
| gc_traversal               | 4.01 ms                                                | 3.76 ms: 1.07x faster                                                       |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                       |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                                        |
| pprint_pformat             | 1.55 sec                                               | 1.47 sec: 1.06x faster                                                      |
| logging_format             | 6.81 us                                                | 6.44 us: 1.06x faster                                                       |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                       |
| deepcopy_memo              | 40.2 us                                                | 38.1 us: 1.05x faster                                                       |
| deltablue                  | 3.92 ms                                                | 3.75 ms: 1.05x faster                                                       |
| spectral_norm              | 108 ms                                                 | 104 ms: 1.04x faster                                                        |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                        |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                        |
| hexiom                     | 6.89 ms                                                | 6.70 ms: 1.03x faster                                                       |
| regex_compile              | 141 ms                                                 | 137 ms: 1.03x faster                                                        |
| tornado_http               | 98.1 ms                                                | 97.2 ms: 1.01x faster                                                       |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                        |
| sqlglot_normalize          | 113 ms                                                 | 113 ms: 1.00x slower                                                        |
| pickle_dict                | 34.6 us                                                | 35.1 us: 1.01x slower                                                       |
| sympy_str                  | 297 ms                                                 | 302 ms: 1.02x slower                                                        |
| sympy_sum                  | 169 ms                                                 | 172 ms: 1.02x slower                                                        |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                      |
| json                       | 5.24 ms                                                | 5.34 ms: 1.02x slower                                                       |
| xml_etree_generate         | 81.1 ms                                                | 82.7 ms: 1.02x slower                                                       |
| xml_etree_process          | 56.9 ms                                                | 58.5 ms: 1.03x slower                                                       |
| sqlglot_optimize           | 55.3 ms                                                | 57.0 ms: 1.03x slower                                                       |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                        |
| deepcopy_reduce            | 3.22 us                                                | 3.32 us: 1.03x slower                                                       |
| unpickle_list              | 5.21 us                                                | 5.40 us: 1.04x slower                                                       |
| thrift                     | 784 us                                                 | 813 us: 1.04x slower                                                        |
| deepcopy                   | 365 us                                                 | 379 us: 1.04x slower                                                        |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                                        |
| sympy_integrate            | 21.5 ms                                                | 22.5 ms: 1.05x slower                                                       |
| bench_thread_pool          | 834 us                                                 | 875 us: 1.05x slower                                                        |
| sympy_expand               | 484 ms                                                 | 510 ms: 1.05x slower                                                        |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                        |
| pyflate                    | 434 ms                                                 | 460 ms: 1.06x slower                                                        |
| dulwich_log                | 64.6 ms                                                | 68.5 ms: 1.06x slower                                                       |
| html5lib                   | 64.8 ms                                                | 69.3 ms: 1.07x slower                                                       |
| scimark_lu                 | 116 ms                                                 | 127 ms: 1.09x slower                                                        |
| django_template            | 33.5 ms                                                | 36.6 ms: 1.09x slower                                                       |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.09x slower                                                        |
| regex_v8                   | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                       |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                       |
| regex_effbot               | 3.51 ms                                                | 3.86 ms: 1.10x slower                                                       |
| genshi_xml                 | 53.4 ms                                                | 58.9 ms: 1.10x slower                                                       |
| sqlite_synth               | 2.57 us                                                | 2.84 us: 1.10x slower                                                       |
| docutils                   | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                      |
| pickle                     | 11.0 us                                                | 12.2 us: 1.11x slower                                                       |
| genshi_text                | 22.5 ms                                                | 25.1 ms: 1.11x slower                                                       |
| regex_dna                  | 205 ms                                                 | 231 ms: 1.13x slower                                                        |
| pickle_list                | 4.59 us                                                | 5.34 us: 1.16x slower                                                       |
| telco                      | 6.86 ms                                                | 8.05 ms: 1.17x slower                                                       |
| coverage                   | 78.8 ms                                                | 93.4 ms: 1.19x slower                                                       |
| async_generators           | 374 ms                                                 | 466 ms: 1.25x slower                                                        |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.26x slower                                                       |
| python_startup_no_site     | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                       |
| python_startup             | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                |

Benchmark hidden because not significant (4): bench_mp_pool, go, nqueens, json_loads
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.76% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x
# Results vs. 3.11.0

- fork: brandtbucher
- ref: inline_class_call_de
- machine: linux-x86_64
- commit hash: ecb7974
- commit date: 2024-06-07
- overall geometric mean: 1.07x faster
- HPT reliability: 95.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-ecb7974 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                                        |
| docutils       | 2.66 sec                                               | 2.93 sec: 1.10x slower                                                      |
| html5lib       | 64.8 ms                                                | 68.3 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-ecb7974 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.44x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 912 ms: 1.42x faster                                                        |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                        |
| async_tree_none            | 528 ms                                                 | 377 ms: 1.40x faster                                                        |
| async_tree_io              | 1.29 sec                                               | 949 ms: 1.36x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 483 ms: 1.32x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 594 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 634 ms: 1.18x faster                                                        |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-ecb7974 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.1 ms: 1.20x faster                                                       |
| float          | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                       |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                        |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-ecb7974 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.02x faster                                                        |
| regex_effbot   | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                       |
| regex_v8       | 22.9 ms                                                | 24.3 ms: 1.06x slower                                                       |
| regex_dna      | 205 ms                                                 | 224 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-ecb7974 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                       |
| tomli_loads          | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                      |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                                        |
| unpickle_pure_python | 242 us                                                 | 225 us: 1.07x faster                                                        |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                        |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.06x faster                                                        |
| json_loads           | 29.2 us                                                | 29.0 us: 1.01x faster                                                       |
| xml_etree_generate   | 81.1 ms                                                | 82.5 ms: 1.02x slower                                                       |
| xml_etree_process    | 56.9 ms                                                | 58.7 ms: 1.03x slower                                                       |
| unpickle_list        | 5.21 us                                                | 5.43 us: 1.04x slower                                                       |
| pickle_dict          | 34.6 us                                                | 36.3 us: 1.05x slower                                                       |
| unpickle             | 13.8 us                                                | 15.0 us: 1.09x slower                                                       |
| pickle               | 11.0 us                                                | 12.3 us: 1.12x slower                                                       |
| pickle_list          | 4.59 us                                                | 5.33 us: 1.16x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-ecb7974 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.64 ms: 1.27x slower                                                       |
| python_startup         | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-ecb7974 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                       |
| django_template | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                       |
| genshi_xml      | 53.4 ms                                                | 57.7 ms: 1.08x slower                                                       |
| genshi_text     | 22.5 ms                                                | 25.3 ms: 1.12x slower                                                       |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-brandtbucher-inline_class_call_de-3.14.0a0-ecb7974 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 173 us: 3.00x faster                                                        |
| generators                 | 74.9 ms                                                | 30.4 ms: 2.46x faster                                                       |
| asyncio_tcp                | 875 ms                                                 | 512 ms: 1.71x faster                                                        |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                      |
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.44x faster                                                        |
| async_tree_io_tg           | 1.29 sec                                               | 912 ms: 1.42x faster                                                        |
| async_tree_memoization_tg  | 626 ms                                                 | 445 ms: 1.41x faster                                                        |
| async_tree_none            | 528 ms                                                 | 377 ms: 1.40x faster                                                        |
| comprehensions             | 23.6 us                                                | 17.1 us: 1.38x faster                                                       |
| async_tree_io              | 1.29 sec                                               | 949 ms: 1.36x faster                                                        |
| pylint                     | 476 ms                                                 | 353 ms: 1.35x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 483 ms: 1.32x faster                                                        |
| richards_super             | 61.9 ms                                                | 47.6 ms: 1.30x faster                                                       |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 594 ms: 1.28x faster                                                        |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                       |
| nbody                      | 96.0 ms                                                | 80.1 ms: 1.20x faster                                                       |
| chaos                      | 71.9 ms                                                | 60.1 ms: 1.20x faster                                                       |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.19x faster                                                       |
| richards                   | 49.8 ms                                                | 41.8 ms: 1.19x faster                                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 634 ms: 1.18x faster                                                        |
| tomli_loads                | 2.30 sec                                               | 1.95 sec: 1.18x faster                                                      |
| fannkuch                   | 405 ms                                                 | 356 ms: 1.14x faster                                                        |
| scimark_monte_carlo        | 70.7 ms                                                | 62.5 ms: 1.13x faster                                                       |
| pathlib                    | 18.5 ms                                                | 16.4 ms: 1.13x faster                                                       |
| crypto_pyaes               | 76.7 ms                                                | 68.4 ms: 1.12x faster                                                       |
| gc_traversal               | 4.01 ms                                                | 3.59 ms: 1.12x faster                                                       |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.51 ms: 1.11x faster                                                       |
| scimark_fft                | 345 ms                                                 | 312 ms: 1.11x faster                                                        |
| raytrace                   | 309 ms                                                 | 279 ms: 1.11x faster                                                        |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                                        |
| logging_simple             | 6.22 us                                                | 5.69 us: 1.09x faster                                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                       |
| float                      | 78.9 ms                                                | 72.5 ms: 1.09x faster                                                       |
| logging_format             | 6.81 us                                                | 6.35 us: 1.07x faster                                                       |
| unpickle_pure_python       | 242 us                                                 | 225 us: 1.07x faster                                                        |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                        |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.06x faster                                                        |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                       |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                       |
| spectral_norm              | 108 ms                                                 | 103 ms: 1.05x faster                                                        |
| pprint_pformat             | 1.55 sec                                               | 1.48 sec: 1.05x faster                                                      |
| deltablue                  | 3.92 ms                                                | 3.74 ms: 1.05x faster                                                       |
| deepcopy_memo              | 40.2 us                                                | 38.3 us: 1.05x faster                                                       |
| pprint_safe_repr           | 747 ms                                                 | 716 ms: 1.04x faster                                                        |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                        |
| hexiom                     | 6.89 ms                                                | 6.70 ms: 1.03x faster                                                       |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                                        |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                      |
| regex_compile              | 141 ms                                                 | 139 ms: 1.02x faster                                                        |
| json_loads                 | 29.2 us                                                | 29.0 us: 1.01x faster                                                       |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                      |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                        |
| deepcopy                   | 365 us                                                 | 369 us: 1.01x slower                                                        |
| go                         | 149 ms                                                 | 151 ms: 1.01x slower                                                        |
| xml_etree_generate         | 81.1 ms                                                | 82.5 ms: 1.02x slower                                                       |
| sympy_str                  | 297 ms                                                 | 303 ms: 1.02x slower                                                        |
| json                       | 5.24 ms                                                | 5.40 ms: 1.03x slower                                                       |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                        |
| xml_etree_process          | 56.9 ms                                                | 58.7 ms: 1.03x slower                                                       |
| sympy_sum                  | 169 ms                                                 | 174 ms: 1.03x slower                                                        |
| sqlglot_optimize           | 55.3 ms                                                | 57.1 ms: 1.03x slower                                                       |
| deepcopy_reduce            | 3.22 us                                                | 3.32 us: 1.03x slower                                                       |
| thrift                     | 784 us                                                 | 811 us: 1.03x slower                                                        |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                                        |
| unpickle_list              | 5.21 us                                                | 5.43 us: 1.04x slower                                                       |
| regex_effbot               | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                       |
| pickle_dict                | 34.6 us                                                | 36.3 us: 1.05x slower                                                       |
| bench_thread_pool          | 834 us                                                 | 878 us: 1.05x slower                                                        |
| html5lib                   | 64.8 ms                                                | 68.3 ms: 1.05x slower                                                       |
| sympy_integrate            | 21.5 ms                                                | 22.7 ms: 1.06x slower                                                       |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.06x slower                                                        |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                                        |
| sympy_expand               | 484 ms                                                 | 514 ms: 1.06x slower                                                        |
| regex_v8                   | 22.9 ms                                                | 24.3 ms: 1.06x slower                                                       |
| pyflate                    | 434 ms                                                 | 463 ms: 1.07x slower                                                        |
| dulwich_log                | 64.6 ms                                                | 69.2 ms: 1.07x slower                                                       |
| django_template            | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                       |
| genshi_xml                 | 53.4 ms                                                | 57.7 ms: 1.08x slower                                                       |
| unpickle                   | 13.8 us                                                | 15.0 us: 1.09x slower                                                       |
| scimark_lu                 | 116 ms                                                 | 126 ms: 1.09x slower                                                        |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.09x slower                                                        |
| docutils                   | 2.66 sec                                               | 2.93 sec: 1.10x slower                                                      |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                                       |
| pickle                     | 11.0 us                                                | 12.3 us: 1.12x slower                                                       |
| genshi_text                | 22.5 ms                                                | 25.3 ms: 1.12x slower                                                       |
| pickle_list                | 4.59 us                                                | 5.33 us: 1.16x slower                                                       |
| telco                      | 6.86 ms                                                | 8.16 ms: 1.19x slower                                                       |
| coverage                   | 78.8 ms                                                | 94.4 ms: 1.20x slower                                                       |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.25x slower                                                       |
| async_generators           | 374 ms                                                 | 470 ms: 1.26x slower                                                        |
| python_startup_no_site     | 6.01 ms                                                | 7.64 ms: 1.27x slower                                                       |
| python_startup             | 8.56 ms                                                | 11.2 ms: 1.31x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                |

Benchmark hidden because not significant (4): nqueens, bench_mp_pool, tornado_http, meteor_contest
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 95.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x
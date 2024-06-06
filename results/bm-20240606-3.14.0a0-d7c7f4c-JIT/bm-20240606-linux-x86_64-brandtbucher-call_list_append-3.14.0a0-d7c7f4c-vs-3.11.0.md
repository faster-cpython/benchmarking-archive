# Results vs. 3.11.0

- fork: brandtbucher
- ref: call_list_append
- machine: linux-x86_64
- commit hash: d7c7f4c
- commit date: 2024-06-06
- overall geometric mean: 1.07x faster
- HPT reliability: 99.12%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-call_list_append-3.14.0a0-d7c7f4c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.06x slower                                                    |
| docutils       | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                  |
| html5lib       | 64.8 ms                                                | 68.4 ms: 1.06x slower                                                   |
| tornado_http   | 98.1 ms                                                | 97.1 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-call_list_append-3.14.0a0-d7c7f4c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 343 ms: 1.43x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 446 ms: 1.40x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 929 ms: 1.39x faster                                                    |
| async_tree_none            | 528 ms                                                 | 384 ms: 1.37x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 474 ms: 1.35x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 999 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 640 ms: 1.17x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.33x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-call_list_append-3.14.0a0-d7c7f4c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 82.5 ms: 1.16x faster                                                   |
| float          | 78.9 ms                                                | 72.6 ms: 1.09x faster                                                   |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                  | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-call_list_append-3.14.0a0-d7c7f4c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 138 ms: 1.02x faster                                                    |
| regex_effbot   | 3.51 ms                                                | 3.56 ms: 1.02x slower                                                   |
| regex_dna      | 205 ms                                                 | 222 ms: 1.09x slower                                                    |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-call_list_append-3.14.0a0-d7c7f4c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.2 ms: 1.30x faster                                                   |
| tomli_loads          | 2.30 sec                                               | 1.96 sec: 1.18x faster                                                  |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                                    |
| unpickle_pure_python | 242 us                                                 | 225 us: 1.08x faster                                                    |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                    |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.04x faster                                                    |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                                   |
| pickle_dict          | 34.6 us                                                | 34.7 us: 1.00x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 82.0 ms: 1.01x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 57.7 ms: 1.01x slower                                                   |
| unpickle_list        | 5.21 us                                                | 5.37 us: 1.03x slower                                                   |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.14 us: 1.12x slower                                                   |
| unpickle             | 13.8 us                                                | 15.6 us: 1.13x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-call_list_append-3.14.0a0-d7c7f4c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.60 ms: 1.26x slower                                                   |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-call_list_append-3.14.0a0-d7c7f4c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                   |
| genshi_xml      | 53.4 ms                                                | 58.9 ms: 1.10x slower                                                   |
| genshi_text     | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                   |
| django_template | 33.5 ms                                                | 37.3 ms: 1.11x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-brandtbucher-call_list_append-3.14.0a0-d7c7f4c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 174 us: 2.98x faster                                                    |
| generators                 | 74.9 ms                                                | 30.9 ms: 2.42x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 518 ms: 1.69x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.67x faster                                                  |
| async_tree_none_tg         | 491 ms                                                 | 343 ms: 1.43x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 446 ms: 1.40x faster                                                    |
| comprehensions             | 23.6 us                                                | 16.9 us: 1.40x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 929 ms: 1.39x faster                                                    |
| async_tree_none            | 528 ms                                                 | 384 ms: 1.37x faster                                                    |
| pylint                     | 476 ms                                                 | 352 ms: 1.35x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 474 ms: 1.35x faster                                                    |
| json_dumps                 | 13.3 ms                                                | 10.2 ms: 1.30x faster                                                   |
| async_tree_io              | 1.29 sec                                               | 999 ms: 1.29x faster                                                    |
| richards_super             | 61.9 ms                                                | 48.4 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                                    |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.19x faster                                                   |
| chaos                      | 71.9 ms                                                | 60.3 ms: 1.19x faster                                                   |
| richards                   | 49.8 ms                                                | 41.8 ms: 1.19x faster                                                   |
| tomli_loads                | 2.30 sec                                               | 1.96 sec: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 640 ms: 1.17x faster                                                    |
| nbody                      | 96.0 ms                                                | 82.5 ms: 1.16x faster                                                   |
| fannkuch                   | 405 ms                                                 | 356 ms: 1.14x faster                                                    |
| scimark_monte_carlo        | 70.7 ms                                                | 62.8 ms: 1.13x faster                                                   |
| pathlib                    | 18.5 ms                                                | 16.5 ms: 1.12x faster                                                   |
| raytrace                   | 309 ms                                                 | 279 ms: 1.11x faster                                                    |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                   |
| crypto_pyaes               | 76.7 ms                                                | 70.2 ms: 1.09x faster                                                   |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                                    |
| logging_simple             | 6.22 us                                                | 5.71 us: 1.09x faster                                                   |
| float                      | 78.9 ms                                                | 72.6 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.64 ms: 1.08x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 225 us: 1.08x faster                                                    |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.08x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.45 sec: 1.07x faster                                                  |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                    |
| scimark_fft                | 345 ms                                                 | 324 ms: 1.07x faster                                                    |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                                   |
| logging_format             | 6.81 us                                                | 6.42 us: 1.06x faster                                                   |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.06x faster                                                   |
| pprint_safe_repr           | 747 ms                                                 | 712 ms: 1.05x faster                                                    |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.04x faster                                                    |
| deepcopy_memo              | 40.2 us                                                | 38.4 us: 1.04x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.77 ms: 1.04x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.87 ms: 1.04x faster                                                   |
| logging_silent             | 111 ns                                                 | 107 ns: 1.04x faster                                                    |
| pycparser                  | 1.19 sec                                               | 1.14 sec: 1.04x faster                                                  |
| hexiom                     | 6.89 ms                                                | 6.66 ms: 1.03x faster                                                   |
| nqueens                    | 87.9 ms                                                | 85.0 ms: 1.03x faster                                                   |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                    |
| spectral_norm              | 108 ms                                                 | 106 ms: 1.02x faster                                                    |
| regex_compile              | 141 ms                                                 | 138 ms: 1.02x faster                                                    |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                                   |
| tornado_http               | 98.1 ms                                                | 97.1 ms: 1.01x faster                                                   |
| pickle_dict                | 34.6 us                                                | 34.7 us: 1.00x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 82.0 ms: 1.01x slower                                                   |
| sympy_str                  | 297 ms                                                 | 301 ms: 1.01x slower                                                    |
| json                       | 5.24 ms                                                | 5.32 ms: 1.01x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 57.7 ms: 1.01x slower                                                   |
| sympy_sum                  | 169 ms                                                 | 171 ms: 1.01x slower                                                    |
| regex_effbot               | 3.51 ms                                                | 3.56 ms: 1.02x slower                                                   |
| pyflate                    | 434 ms                                                 | 446 ms: 1.03x slower                                                    |
| unpickle_list              | 5.21 us                                                | 5.37 us: 1.03x slower                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 57.0 ms: 1.03x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                    |
| deepcopy                   | 365 us                                                 | 378 us: 1.04x slower                                                    |
| deepcopy_reduce            | 3.22 us                                                | 3.34 us: 1.04x slower                                                   |
| dask                       | 365 ms                                                 | 381 ms: 1.04x slower                                                    |
| sympy_integrate            | 21.5 ms                                                | 22.5 ms: 1.05x slower                                                   |
| thrift                     | 784 us                                                 | 826 us: 1.05x slower                                                    |
| html5lib                   | 64.8 ms                                                | 68.4 ms: 1.06x slower                                                   |
| bench_thread_pool          | 834 us                                                 | 881 us: 1.06x slower                                                    |
| sympy_expand               | 484 ms                                                 | 512 ms: 1.06x slower                                                    |
| 2to3                       | 264 ms                                                 | 281 ms: 1.06x slower                                                    |
| scimark_sor                | 121 ms                                                 | 129 ms: 1.06x slower                                                    |
| dulwich_log                | 64.6 ms                                                | 68.9 ms: 1.07x slower                                                   |
| scimark_lu                 | 116 ms                                                 | 126 ms: 1.08x slower                                                    |
| regex_dna                  | 205 ms                                                 | 222 ms: 1.09x slower                                                    |
| regex_v8                   | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                   |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                   |
| genshi_xml                 | 53.4 ms                                                | 58.9 ms: 1.10x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                  |
| genshi_text                | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                   |
| django_template            | 33.5 ms                                                | 37.3 ms: 1.11x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.11x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.14 us: 1.12x slower                                                   |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                                   |
| telco                      | 6.86 ms                                                | 8.06 ms: 1.18x slower                                                   |
| coverage                   | 78.8 ms                                                | 93.5 ms: 1.19x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.26x slower                                                   |
| async_generators           | 374 ms                                                 | 469 ms: 1.26x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 7.60 ms: 1.26x slower                                                   |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (4): meteor_contest, bench_mp_pool, sqlglot_normalize, go
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.12% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x
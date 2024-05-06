# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.16x slower                                                    |
| chameleon      | 6.70 ms                                                | 7.57 ms: 1.13x slower                                                   |
| html5lib       | 64.8 ms                                                | 72.7 ms: 1.12x slower                                                   |
| tornado_http   | 98.1 ms                                                | 102 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                  | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 372 ms: 1.42x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.42x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 459 ms: 1.36x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 957 ms: 1.35x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 964 ms: 1.34x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 503 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 619 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 634 ms: 1.18x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 191 ms: 1.02x faster                                                    |
| float          | 78.9 ms                                                | 91.7 ms: 1.16x slower                                                   |
| nbody          | 96.0 ms                                                | 129 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                  | 1.15x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.70 ms: 1.06x slower                                                   |
| regex_v8       | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                   |
| regex_dna      | 205 ms                                                 | 224 ms: 1.09x slower                                                    |
| regex_compile  | 141 ms                                                 | 182 ms: 1.29x slower                                                    |
| Geometric mean | (ref)                                                  | 1.13x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                   |
| xml_etree_parse      | 164 ms                                                 | 151 ms: 1.09x faster                                                    |
| json_loads           | 29.2 us                                                | 27.7 us: 1.06x faster                                                   |
| pickle_dict          | 34.6 us                                                | 35.2 us: 1.02x slower                                                   |
| xml_etree_iterparse  | 108 ms                                                 | 110 ms: 1.02x slower                                                    |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                   |
| tomli_loads          | 2.30 sec                                               | 2.54 sec: 1.10x slower                                                  |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.15 us: 1.12x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 92.7 ms: 1.14x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 65.2 ms: 1.15x slower                                                   |
| unpickle_pure_python | 242 us                                                 | 295 us: 1.22x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (2): unpickle_list, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.13 ms: 1.19x slower                                                   |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 65.5 ms: 1.23x slower                                                   |
| django_template | 33.5 ms                                                | 41.4 ms: 1.23x slower                                                   |
| genshi_text     | 22.5 ms                                                | 28.9 ms: 1.28x slower                                                   |
| mako            | 10.7 ms                                                | 13.9 ms: 1.30x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 196 us: 2.65x faster                                                    |
| generators                 | 74.9 ms                                                | 29.6 ms: 2.53x faster                                                   |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                                  |
| asyncio_tcp                | 875 ms                                                 | 530 ms: 1.65x faster                                                    |
| async_tree_none            | 528 ms                                                 | 372 ms: 1.42x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.42x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 459 ms: 1.36x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 957 ms: 1.35x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 964 ms: 1.34x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 503 ms: 1.27x faster                                                    |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 619 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 634 ms: 1.18x faster                                                    |
| coroutines                 | 27.0 ms                                                | 24.3 ms: 1.11x faster                                                   |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                    |
| xml_etree_parse            | 164 ms                                                 | 151 ms: 1.09x faster                                                    |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.06x faster                                                   |
| djangocms                  | 33.5 us                                                | 32.6 us: 1.03x faster                                                   |
| pidigits                   | 194 ms                                                 | 191 ms: 1.02x faster                                                    |
| gc_traversal               | 4.01 ms                                                | 4.05 ms: 1.01x slower                                                   |
| pickle_dict                | 34.6 us                                                | 35.2 us: 1.02x slower                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 110 ms: 1.02x slower                                                    |
| richards_super             | 61.9 ms                                                | 63.5 ms: 1.03x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 568 ms: 1.03x slower                                                    |
| tornado_http               | 98.1 ms                                                | 102 ms: 1.05x slower                                                    |
| comprehensions             | 23.6 us                                                | 24.7 us: 1.05x slower                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.85 ms: 1.06x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.70 ms: 1.06x slower                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.52 ms: 1.06x slower                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.41 us: 1.06x slower                                                   |
| thrift                     | 784 us                                                 | 833 us: 1.06x slower                                                    |
| dask                       | 365 ms                                                 | 390 ms: 1.07x slower                                                    |
| sympy_sum                  | 169 ms                                                 | 180 ms: 1.07x slower                                                    |
| raytrace                   | 309 ms                                                 | 330 ms: 1.07x slower                                                    |
| pycparser                  | 1.19 sec                                               | 1.28 sec: 1.08x slower                                                  |
| bench_thread_pool          | 834 us                                                 | 902 us: 1.08x slower                                                    |
| regex_v8                   | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                   |
| mdp                        | 2.77 sec                                               | 3.01 sec: 1.09x slower                                                  |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.09x slower                                                    |
| deepcopy                   | 365 us                                                 | 401 us: 1.10x slower                                                    |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                   |
| tomli_loads                | 2.30 sec                                               | 2.54 sec: 1.10x slower                                                  |
| logging_simple             | 6.22 us                                                | 6.90 us: 1.11x slower                                                   |
| sympy_integrate            | 21.5 ms                                                | 23.8 ms: 1.11x slower                                                   |
| chaos                      | 71.9 ms                                                | 79.8 ms: 1.11x slower                                                   |
| unpickle                   | 13.8 us                                                | 15.4 us: 1.11x slower                                                   |
| aiohttp                    | 1.12 ms                                                | 1.24 ms: 1.11x slower                                                   |
| gunicorn                   | 1.20 ms                                                | 1.34 ms: 1.11x slower                                                   |
| sympy_str                  | 297 ms                                                 | 331 ms: 1.12x slower                                                    |
| pickle_list                | 4.59 us                                                | 5.15 us: 1.12x slower                                                   |
| html5lib                   | 64.8 ms                                                | 72.7 ms: 1.12x slower                                                   |
| logging_format             | 6.81 us                                                | 7.66 us: 1.12x slower                                                   |
| meteor_contest             | 109 ms                                                 | 123 ms: 1.13x slower                                                    |
| chameleon                  | 6.70 ms                                                | 7.57 ms: 1.13x slower                                                   |
| sympy_expand               | 484 ms                                                 | 549 ms: 1.13x slower                                                    |
| deltablue                  | 3.92 ms                                                | 4.45 ms: 1.13x slower                                                   |
| richards                   | 49.8 ms                                                | 56.7 ms: 1.14x slower                                                   |
| dulwich_log                | 64.6 ms                                                | 73.9 ms: 1.14x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 92.7 ms: 1.14x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 65.2 ms: 1.15x slower                                                   |
| sqlglot_normalize          | 113 ms                                                 | 129 ms: 1.15x slower                                                    |
| 2to3                       | 264 ms                                                 | 305 ms: 1.16x slower                                                    |
| float                      | 78.9 ms                                                | 91.7 ms: 1.16x slower                                                   |
| deepcopy_memo              | 40.2 us                                                | 47.3 us: 1.18x slower                                                   |
| sqlglot_optimize           | 55.3 ms                                                | 65.3 ms: 1.18x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.13 ms: 1.19x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 3.06 us: 1.19x slower                                                   |
| unpickle_pure_python       | 242 us                                                 | 295 us: 1.22x slower                                                    |
| crypto_pyaes               | 76.7 ms                                                | 93.6 ms: 1.22x slower                                                   |
| genshi_xml                 | 53.4 ms                                                | 65.5 ms: 1.23x slower                                                   |
| fannkuch                   | 405 ms                                                 | 499 ms: 1.23x slower                                                    |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                   |
| django_template            | 33.5 ms                                                | 41.4 ms: 1.23x slower                                                   |
| coverage                   | 78.8 ms                                                | 97.6 ms: 1.24x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.32 ms: 1.26x slower                                                   |
| nqueens                    | 87.9 ms                                                | 111 ms: 1.26x slower                                                    |
| pprint_pformat             | 1.55 sec                                               | 1.98 sec: 1.27x slower                                                  |
| pprint_safe_repr           | 747 ms                                                 | 953 ms: 1.28x slower                                                    |
| async_generators           | 374 ms                                                 | 477 ms: 1.28x slower                                                    |
| genshi_text                | 22.5 ms                                                | 28.9 ms: 1.28x slower                                                   |
| regex_compile              | 141 ms                                                 | 182 ms: 1.29x slower                                                    |
| scimark_sor                | 121 ms                                                 | 157 ms: 1.30x slower                                                    |
| mako                       | 10.7 ms                                                | 13.9 ms: 1.30x slower                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 92.1 ms: 1.30x slower                                                   |
| scimark_fft                | 345 ms                                                 | 454 ms: 1.32x slower                                                    |
| spectral_norm              | 108 ms                                                 | 144 ms: 1.34x slower                                                    |
| nbody                      | 96.0 ms                                                | 129 ms: 1.34x slower                                                    |
| telco                      | 6.86 ms                                                | 9.32 ms: 1.36x slower                                                   |
| pyflate                    | 434 ms                                                 | 592 ms: 1.37x slower                                                    |
| go                         | 149 ms                                                 | 212 ms: 1.43x slower                                                    |
| scimark_lu                 | 116 ms                                                 | 168 ms: 1.45x slower                                                    |
| hexiom                     | 6.89 ms                                                | 10.2 ms: 1.48x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                            |

Benchmark hidden because not significant (5): unpickle_list, pathlib, json, bench_mp_pool, pickle_pure_python
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: docutils, flaskblogging, mypy2, pylint, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.03x